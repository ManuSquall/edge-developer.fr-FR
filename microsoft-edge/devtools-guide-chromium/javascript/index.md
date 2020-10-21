---
description: Découvrez comment utiliser Microsoft Edge DevTools pour rechercher et corriger les bogues JavaScript.
title: Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bff87ca36c484689134f284514bbab353b8b99b6
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124788"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="dcbdd-104">Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="dcbdd-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="dcbdd-105">Ce didacticiel décrit le flux de travail de base pour le débogage d’un problème JavaScript dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-105">This tutorial teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="dcbdd-106">Étape 1: reproduire le bogue</span><span class="sxs-lookup"><span data-stu-id="dcbdd-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="dcbdd-107">La recherche d’une série d’actions qui reproduit régulièrement un bogue est toujours la première étape du débogage.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-107">Finding a series of actions that consistently reproduces a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="dcbdd-108">Sélectionnez **ouvrir la démonstration**.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="dcbdd-109">Maintenez la touche Windows enfoncée `Control` , `Command` puis ouvrez la démonstration dans un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new tab.</span></span>  
    
    [<span data-ttu-id="dcbdd-110">Ouvrir la démo</span><span class="sxs-lookup"><span data-stu-id="dcbdd-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="dcbdd-111">Entrez `5` dans la zone de texte **numéro 1** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="dcbdd-112">Entrez `1` dans la zone de texte **numéro 2** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="dcbdd-113">Cliquez sur **Ajouter un numéro 1 et sur numéro 2**.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="dcbdd-114">L’étiquette sous le bouton indique `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="dcbdd-115">Le résultat doit être `6` .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-115">The result should be `6`.</span></span>  <span data-ttu-id="dcbdd-116">Voici le bogue que vous allez résoudre.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-116">This is the bug you are going to fix.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       <span data-ttu-id="dcbdd-118">Le résultat de la valeur `5 + 1` `51` , mais doit être</span><span class="sxs-lookup"><span data-stu-id="dcbdd-118">The result of `5 + 1` is `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="dcbdd-119">Étape 2: Familiarisez-vous avec l’interface utilisateur du panneau sources</span><span class="sxs-lookup"><span data-stu-id="dcbdd-119">Step 2: Get familiar with the Sources panel UI</span></span>  

<span data-ttu-id="dcbdd-120">DevTools fournit un grand nombre d’outils différents pour différentes tâches, comme le changement de CSS, la performance de chargement de la page de profil et la surveillance des requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-120">DevTools provides a lot of different tools for different tasks, such as changing CSS, profiling page load performance, and monitoring network requests.</span></span>  <span data-ttu-id="dcbdd-121">Le panneau **sources** vous permet de déboguer JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-121">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="dcbdd-122">Ouvrez devtools en appuyant sur `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-122">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) .</span></span>  <span data-ttu-id="dcbdd-123">Ce raccourci ouvre le panneau de la **console** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-123">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="dcbdd-125">Panneau de la **console**</span><span class="sxs-lookup"><span data-stu-id="dcbdd-125">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="dcbdd-126">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-126">Click the **Sources** tab.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="dcbdd-128">Panneau **sources**</span><span class="sxs-lookup"><span data-stu-id="dcbdd-128">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="dcbdd-129">L’interface utilisateur du panneau **sources** comporte 3 parties.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-129">The **Sources** panel UI has 3 parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="dcbdd-131">Les 3 parties de l’interface utilisateur du panneau **sources**</span><span class="sxs-lookup"><span data-stu-id="dcbdd-131">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="dcbdd-132">Le volet **navigateur de fichiers** \ (section 1 dans l’illustration précédente \).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-132">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="dcbdd-133">Chaque fichier mentionné dans la page est répertorié ici.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-133">Every file that the page requests is listed here.</span></span>  
1.  <span data-ttu-id="dcbdd-134">Le volet de l' **éditeur de code** (section 2 dans l’illustration précédente \).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-134">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="dcbdd-135">Après avoir sélectionné un fichier dans le volet **navigateur de fichiers** , le contenu de ce fichier est affiché ici.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-135">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="dcbdd-136">Le volet de **débogage JavaScript** (section 3 de la figure précédente).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-136">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="dcbdd-137">Différents outils d’examen du code JavaScript pour la page.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-137">Various tools for inspecting the JavaScript for the page.</span></span>  <span data-ttu-id="dcbdd-138">Si votre fenêtre DevTools est large, ce volet est affiché à droite du volet de l' **éditeur de code** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-138">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="dcbdd-139">Étape 3: mettre en pause le code avec un point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="dcbdd-139">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="dcbdd-140">Une méthode courante pour le débogage d’un problème comme celui-ci consiste à insérer un grand nombre d' `console.log()` instructions dans le code afin d’inspecter les valeurs lors de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-140">A common method for debugging a problem like this is to insert a lot of `console.log()` statements into the code, in order to inspect values as the script runs.</span></span>  <span data-ttu-id="dcbdd-141">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="dcbdd-141">For example:</span></span>  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

<span data-ttu-id="dcbdd-142">La `console.log()` méthode peut être exécutée, mais les **points d’arrêt** peuvent être plus productifs.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-142">The `console.log()` method may get the job done, but **breakpoints** are able to get it done faster.</span></span>  <span data-ttu-id="dcbdd-143">Un point d’arrêt vous permet d’interrompre votre code au milieu du runtime et d’examiner toutes les valeurs à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-143">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="dcbdd-144">Les points d’arrêt présentent quelques avantages par rapport à la `console.log()` méthode:</span><span class="sxs-lookup"><span data-stu-id="dcbdd-144">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="dcbdd-145">Avec `console.log()` , vous devez ouvrir manuellement le code source, Rechercher le code approprié, insérer les `console.log()` instructions, puis recharger la page pour afficher les messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-145">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then reload the page in order to see the messages in the Console.</span></span>  <span data-ttu-id="dcbdd-146">Avec les points d’arrêt, vous pouvez mettre en pause le code concerné sans même savoir comment le code est structuré.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-146">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="dcbdd-147">Dans vos `console.log()` instructions, vous devez spécifier explicitement chaque valeur que vous voulez inspecter.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-147">In your `console.log()` statements you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="dcbdd-148">Les points d’arrêt DevTools vous montrent les valeurs de toutes les variables à ce moment précis.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-148">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="dcbdd-149">Parfois, il existe des variables affectant votre code.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-149">Sometimes there are variables affecting your code that you are not even aware of.</span></span>  

<span data-ttu-id="dcbdd-150">En bref, les points d’arrêt permettent de rechercher et de résoudre les bogues plus rapidement que la `console.log()` méthode.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-150">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="dcbdd-151">Si vous vous prenez reculer et réfléchir au fonctionnement de l’application, vous pouvez faire en sorte que la somme incorrecte ( `5 + 1 = 51` ) soit calculée dans l' `click` écouteur d’événements associé au bouton **Ajouter un numéro 1 et 2** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-151">If you take a step back and think about how the app works, you are able to make an educated guess that the incorrect sum (`5 + 1 = 51`) gets computed in the `click` event listener that is associated to the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="dcbdd-152">Par conséquent, il est probable que vous souhaitiez suspendre le code au bout du temps d’exécution de l' `click` écouteur.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-152">Therefore, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="dcbdd-153">Les **points d’arrêt écouteur d’événements** vous permettent d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="dcbdd-153">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="dcbdd-154">Dans le volet **débogage JavaScript** , sélectionnez points d’arrêt de l' **écouteur d’événements** pour développer la section.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-154">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="dcbdd-155">DevTools affiche une liste des catégories d’événements pouvant être développés, telles que l' **animation** et le **presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-155">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="dcbdd-156">En regard de la catégorie d’événement de **souris** , sélectionnez **développer** \ ( ![ icône de développement ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-156">Next to the **Mouse** event category, choose **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="dcbdd-157">DevTools révèle une liste d’événements de souris tels que **Click** et **MouseDown**.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-157">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="dcbdd-158">Une case à cocher est associée à chaque événement.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-158">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="dcbdd-159">Cochez la case **cliquez sur** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-159">Check the **click** checkbox.</span></span>  <span data-ttu-id="dcbdd-160">DevTools est désormais configuré pour s’arrêter automatiquement lors *de l’exécution d’un* `click` écouteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-160">DevTools is now set up to automatically pause when *any* `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="dcbdd-162">La case à cocher **Cliquer** est activée</span><span class="sxs-lookup"><span data-stu-id="dcbdd-162">The **click** checkbox is enabled</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="dcbdd-163">Dans la démonstration, choisissez de nouveau **Ajouter le numéro 1 et le numéro 2** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-163">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="dcbdd-164">DevTools met en pause la démonstration et surligne une ligne de code dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-164">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="dcbdd-165">DevTools doit suspendre la ligne 16 `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-165">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="dcbdd-166">Si vous placez le pointeur sur une autre ligne de code, appuyez sur l' **exécution du script de reprise** , puis appuyez ![ ][ImageResumeIcon] sur la touche reprise.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-166">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="dcbdd-167">Si vous avez interrompu une autre ligne, vous disposez d’une extension de navigateur permettant d’inscrire un `click` écouteur d’événements sur chaque page que vous visitez.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-167">If you paused on a different line, you have a browser extension that registers a `click` event listener on every page that you visit.</span></span>  <span data-ttu-id="dcbdd-168">Vous avez été suspendu dans l' `click` écouteur de l’extension.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-168">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="dcbdd-169">Si vous utilisez le mode InPrivate pour effectuer une **recherche dans Private**, qui désactive toutes les extensions, il est possible que vous deviez suspendre chaque fois la ligne de code souhaitée.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-169">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="dcbdd-170">Les **points d’arrêt écouteur d’événements** ne sont qu’un type de nombreux types de points d’arrêt disponibles dans devtools.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-170">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="dcbdd-171">Il est recommandé de mémoriser tous les types différents, car chaque type de fichier vous permet de déboguer différents scénarios le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-171">It is worth memorizing all the different types, because each type ultimately helps you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="dcbdd-172">Étape 4: parcourir le code</span><span class="sxs-lookup"><span data-stu-id="dcbdd-172">Step 4: Step through the code</span></span>  

<span data-ttu-id="dcbdd-173">L’une des causes les plus fréquentes est qu’un script s’exécute dans un ordre incorrect.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-173">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="dcbdd-174">Le passage en revue de votre code vous permet de parcourir le runtime de votre code, une ligne à la fois, et de rechercher exactement à l’endroit où il s’exécute dans un ordre différent de ce que vous attendiez.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-174">Stepping through your code enables you to walk through the runtime of your code, one line at a time, and figure out exactly where it is running in a different order than you expected.</span></span>  <span data-ttu-id="dcbdd-175">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="dcbdd-175">Try it now:</span></span>  

1.  <span data-ttu-id="dcbdd-176">Choisissez **passer à la fonction suivante** en tant qu’appel ![ ][ImageOverIcon] .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-176">Choose **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="dcbdd-177">DevTools exécute le code suivant sans s’y exécuter.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-177">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="dcbdd-178">DevTools ignore quelques lignes de code.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-178">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="dcbdd-179">Étant donné que l’argument `inputsAreEmpty()` évalue la valeur false, le bloc de code de l' `if` instruction ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-179">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="dcbdd-180">Dans le panneau **sources** de devtools, sélectionnez **appeler la fonction suivante** pour passer à l’appel de fonction suivante dans le ![ cadre du ][ImageIntoIcon] Runtime de la `updateLabel()` fonction, une ligne à la fois.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-180">On the **Sources** panel of DevTools, choose **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="dcbdd-181">Il s’agit de l’idée de base de l’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-181">That is the basic idea of stepping through code.</span></span>  <span data-ttu-id="dcbdd-182">Si vous examinez le code dans `get-started.js` , vous constatez que le bogue est probablement quelque part dans la `updateLabel()` fonction.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-182">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="dcbdd-183">Au lieu de parcourir chaque ligne de code, vous pouvez utiliser un autre type de point d’arrêt pour mettre le code plus près de l’emplacement probable du bogue.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-183">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="dcbdd-184">Étape 5: définir un point d’arrêt de code de ligne</span><span class="sxs-lookup"><span data-stu-id="dcbdd-184">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="dcbdd-185">Les points d’arrêt de la ligne sont le type le plus courant de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-185">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="dcbdd-186">Lorsque vous obtenez la ligne de code spécifique sur laquelle vous voulez mettre en pause, utilisez un point d’arrêt de ligne de code:</span><span class="sxs-lookup"><span data-stu-id="dcbdd-186">When you get the specific line of code that you want to pause on, use a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="dcbdd-187">Regardez la dernière ligne de code dans `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="dcbdd-187">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="dcbdd-188">À gauche du code figure le numéro de ligne de cette ligne de code particulière, qui est **33**.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-188">To the left of the code you see the line number of this particular line of code, which is **33**.</span></span>  <span data-ttu-id="dcbdd-189">Cliquez sur **33**.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-189">Click on **33**.</span></span>  <span data-ttu-id="dcbdd-190">DevTools place une icône rouge à gauche de **33**.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-190">DevTools puts a red icon to the left of **33**.</span></span>  <span data-ttu-id="dcbdd-191">Cela signifie qu’il y a un point d’arrêt de ligne de code sur ce trait.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-191">This means that there is a line-of-code breakpoint on this line.</span></span>  <span data-ttu-id="dcbdd-192">DevTools est à présent mis en pause pour pouvoir exécuter cette ligne de code.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-192">DevTools now always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="dcbdd-193">Sélectionnez **reprendre l’exécution** du script ![ ][ImageResumeIcon] .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-193">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="dcbdd-194">Le script continue de s’exécuter jusqu’à ce qu’il atteigne la ligne 33.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-194">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="dcbdd-195">Sur les lignes 30, 31 et 32, DevTools affiche les valeurs de `addend1` , `addend2` et `sum` à droite du point-virgule sur chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-195">On lines 30, 31, and 32, DevTools prints out the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="dcbdd-197">DevTools s’arrête sur le point d’arrêt de ligne de code de la ligne 32</span><span class="sxs-lookup"><span data-stu-id="dcbdd-197">DevTools pauses on the line-of-code breakpoint on line 32</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="dcbdd-198">Étape 6: vérifier les valeurs des variables</span><span class="sxs-lookup"><span data-stu-id="dcbdd-198">Step 6: Check variable values</span></span>  

<span data-ttu-id="dcbdd-199">Les valeurs de `addend1` , `addend2` et il est `sum` suspect.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-199">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="dcbdd-200">Ils sont encapsulés entre guillemets, ce qui signifie qu’il s’agit de chaînes.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-200">They are wrapped in quotes, which means that they are strings.</span></span>  <span data-ttu-id="dcbdd-201">C’est une bonne hypothèse d’expliquer la cause du bogue.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-201">This is a good hypothesis for the explaining the cause of the bug.</span></span>  <span data-ttu-id="dcbdd-202">Maintenant, il est temps de recueillir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-202">Now it is time to gather more information.</span></span>  <span data-ttu-id="dcbdd-203">DevTools offre un grand nombre d’outils d’examen des valeurs des variables.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-203">DevTools provides a lot of tools for examining variable values.</span></span>  

### <span data-ttu-id="dcbdd-204">Méthode 1: volet d’étendue</span><span class="sxs-lookup"><span data-stu-id="dcbdd-204">Method 1: The Scope pane</span></span>  

<span data-ttu-id="dcbdd-205">Lorsque vous placez le pointeur sur une ligne de code, le volet de l' **étendue** vous indique quelles variables locales et globales sont actuellement définies, ainsi que la valeur de chaque variable.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-205">When you pause on a line of code, the **Scope** pane shows you what local and global variables are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="dcbdd-206">Il affiche également les variables de fermeture, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-206">It also shows closure variables, when applicable.</span></span>  <span data-ttu-id="dcbdd-207">Double-cliquez sur une valeur de variable pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-207">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="dcbdd-208">Lorsque vous n’êtes pas en pause sur une ligne de code, le volet **étendue** est vide.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-208">When you are not paused on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="dcbdd-210">Volet **cadre**</span><span class="sxs-lookup"><span data-stu-id="dcbdd-210">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="dcbdd-211">Méthode 2: espionner les expressions</span><span class="sxs-lookup"><span data-stu-id="dcbdd-211">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="dcbdd-212">L’onglet **expressions espionnes** vous permet de surveiller les valeurs des variables dans le temps.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-212">The **Watch Expressions** tab lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="dcbdd-213">Comme son nom l’indique, les expressions espionnes ne sont pas simplement limitées aux variables.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-213">As the name implies, Watch Expressions are not just limited to variables.</span></span>  <span data-ttu-id="dcbdd-214">Vous pouvez stocker toute expression JavaScript valide dans une expression espionne.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-214">You are able to store any valid JavaScript expression in a Watch Expression.</span></span>  <span data-ttu-id="dcbdd-215">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="dcbdd-215">Try it now:</span></span>  

1.  <span data-ttu-id="dcbdd-216">Cliquez sur l’onglet **Espion** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-216">Click the **Watch** tab.</span></span>  
1.  <span data-ttu-id="dcbdd-217">Sélectionnez **Ajouter une expression** \ ( ![ Ajouter une expression ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-217">Choose **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="dcbdd-218">Entrez `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-218">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="dcbdd-219">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-219">Select `Enter`.</span></span>  <span data-ttu-id="dcbdd-220">DevTools affiche `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-220">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="dcbdd-221">La valeur à droite des deux-points est le résultat de l’expression espionne.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-221">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="dcbdd-222">Dans le volet des expressions espionnes (en bas à droite) dans l’illustration suivante, l' `typeof sum` expression espionne est affichée.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-222">In the Watch Expression pane \(bottom-right\) in in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="dcbdd-223">S’il s’agit d’une fenêtre de DevTools de grande taille, le volet d’expressions espionnes se trouve à droite au-dessus du volet de **points d’arrêt du détecteur d’événements** .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-223">If your DevTools window is large, the Watch Expression pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="dcbdd-225">Volet **expression espionner**</span><span class="sxs-lookup"><span data-stu-id="dcbdd-225">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="dcbdd-226">Comme soupçonné, `sum` est évaluée en tant que chaîne, lorsqu’il devrait s’agir d’un nombre.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-226">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="dcbdd-227">Vous avez vérifié qu’il s’agit de la cause du bogue.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-227">You have now confirmed that this is the cause of the bug.</span></span>  

### <span data-ttu-id="dcbdd-228">Méthode 3: la console</span><span class="sxs-lookup"><span data-stu-id="dcbdd-228">Method 3: The Console</span></span>  

<span data-ttu-id="dcbdd-229">En plus de l’affichage des `console.log()` messages, vous pouvez également utiliser la console pour évaluer des instructions JavaScript arbitraires.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-229">In addition to viewing `console.log()` messages, you may also use the Console to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="dcbdd-230">En termes de débogage, vous pouvez utiliser la console pour tester les correctifs potentiels pour les bogues.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-230">In terms of debugging, you may use the Console to test out potential fixes for bugs.</span></span>  <span data-ttu-id="dcbdd-231">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="dcbdd-231">Try it now:</span></span>  

1.  <span data-ttu-id="dcbdd-232">Si le tiroir de la console n’est pas ouvert, sélectionnez `Escape` -le pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-232">If you do not have the Console drawer open, select `Escape` to open it.</span></span>  <span data-ttu-id="dcbdd-233">Il s’ouvre en bas de la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-233">It opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="dcbdd-234">Dans la console, tapez `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-234">In the Console, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="dcbdd-235">Cette instruction fonctionne, car vous êtes en pause sur une ligne de code où vous vous `addend1` `addend2` trouvez dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-235">This statement works because you are paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="dcbdd-236">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-236">Select `Enter`.</span></span>  <span data-ttu-id="dcbdd-237">DevTools évalue l’instruction et imprime `6` , ce qui correspond au résultat attendu que la démonstration produira.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-237">DevTools evaluates the statement and prints out `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Le résultat de 5 + 1 est 51, mais devrait être 6" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="dcbdd-239">Le tiroir de la **console** , après évaluation</span><span class="sxs-lookup"><span data-stu-id="dcbdd-239">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="dcbdd-240">Étape 7: appliquer un correctif</span><span class="sxs-lookup"><span data-stu-id="dcbdd-240">Step 7: Apply a fix</span></span>  

<span data-ttu-id="dcbdd-241">Si vous trouvez un correctif pour le bogue, essayez de résoudre le problème en modifiant le code et en exécutant de nouveau la démonstration.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-241">If you find a fix for the bug, try out your fix by editing the code and re-running the demo.</span></span>  <span data-ttu-id="dcbdd-242">Vous n’avez pas besoin de quitter DevTools pour appliquer le correctif.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-242">You do not need to leave DevTools to apply the fix.</span></span>  <span data-ttu-id="dcbdd-243">Vous pouvez modifier le code JavaScript directement dans l’interface utilisateur DevTools.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-243">You are able to edit JavaScript code directly within the DevTools UI.</span></span>  <span data-ttu-id="dcbdd-244">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="dcbdd-244">Try it now:</span></span>  

1.  <span data-ttu-id="dcbdd-245">Sélectionnez **reprendre l’exécution** du script ![ ][ImageResumeIcon] .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-245">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="dcbdd-246">Dans l' **éditeur de code**, remplacez ligne 32, `var sum = addend1 + addend2` par `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="dcbdd-246">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="dcbdd-247">Sélectionnez `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-247">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="dcbdd-248">Sélectionnez **Désactiver les points d’arrêt** \ ( ![ Désactiver les points d’arrêt ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-248">Choose **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="dcbdd-249">Il change de bleu pour indiquer qu’il est actif.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-249">It changes blue to indicate that it is active.</span></span>  <span data-ttu-id="dcbdd-250">Si cette valeur est définie, DevTools ignore les points d’arrêt que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-250">While this is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="dcbdd-251">Testez la démonstration avec des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-251">Try out the demo with different values.</span></span>  <span data-ttu-id="dcbdd-252">La démonstration est désormais correctement calculée.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-252">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="dcbdd-253">Ce flux de travail s’applique uniquement au code exécuté dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-253">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="dcbdd-254">Cela ne résout pas le code de tous les utilisateurs visitant votre page.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-254">It does not fix the code for all users that visit your page.</span></span>  <span data-ttu-id="dcbdd-255">Pour ce faire, vous devez résoudre le code qui se trouve sur vos serveurs.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-255">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="dcbdd-256">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="dcbdd-256">Next steps</span></span>  

<span data-ttu-id="dcbdd-257">Félicitations!</span><span class="sxs-lookup"><span data-stu-id="dcbdd-257">Congratulations!</span></span>  <span data-ttu-id="dcbdd-258">Vous savez maintenant comment tirer le meilleur parti de Microsoft Edge DevTools lors du débogage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-258">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="dcbdd-259">Les outils et méthodes que vous avez appris dans ce didacticiel pourront vous épargner des heures de comptage.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-259">The tools and methods you learned in this tutorial may save you countless hours.</span></span>  

<span data-ttu-id="dcbdd-260">Ce didacticiel ne vous a montré que deux manières de définir des points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-260">This tutorial only showed you two ways to set breakpoints.</span></span>  <span data-ttu-id="dcbdd-261">DevTools offre de nombreuses autres manières, notamment les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-261">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="dcbdd-262">Les points d’arrêt conditionnel qui sont uniquement déclenchés lorsque la condition que vous spécifiez est vrai.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-262">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="dcbdd-263">Points d’arrêt sur les exceptions interceptées ou non capturées.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-263">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="dcbdd-264">XHR points d’arrêt qui sont déclenchés lorsque l’URL demandée correspond à une sous-chaîne que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-264">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="dcbdd-265">Pour plus d’informations sur l’utilisation de chaque type, voir [suspendre votre code avec des points d’arrêt][DevtoolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="dcbdd-265">For more information about when and how to use each type, go to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="dcbdd-266">Il y a quelques contrôles d’exécution du code qui n’ont pas été décrits dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-266">There are a couple of code stepping controls that were not explained in this tutorial.</span></span>  <span data-ttu-id="dcbdd-267">Pour plus d’informations, accédez à l' [étape sur la ligne de code][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="dcbdd-267">For more information, go to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <span data-ttu-id="dcbdd-268">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="dcbdd-268">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Code détaillé-référence de débogage JavaScript | Documents Microsoft"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Ouvrir une démonstration | Problème"  

> [!NOTE]
> <span data-ttu-id="dcbdd-272">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dcbdd-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dcbdd-273">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="dcbdd-275">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dcbdd-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
