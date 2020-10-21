---
description: Découvrez comment évaluer les performances d’exécution dans Microsoft Edge DevTools.
title: Commencer à analyser les performances de l’exécution
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7cb1d8f073cdb8a43093514dd7dea86d72102011
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124984"
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

# <span data-ttu-id="4b34d-104">Commencer à analyser les performances de l’exécution</span><span class="sxs-lookup"><span data-stu-id="4b34d-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="4b34d-105">Pour plus d’informations sur le chargement plus rapide de vos pages, accédez à [optimiser la vitesse du site Web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="4b34d-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="4b34d-106">La performance du runtime correspond à la façon dont votre page s’exécute lorsque celle-ci est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4b34d-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="4b34d-107">L’article suivant explique comment utiliser le panneau performances de Microsoft Edge DevTools pour analyser les performances de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4b34d-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="4b34d-108">En ce qui concerne le modèle **ferroviaire** , les compétences que vous apprenez dans ce didacticiel sont utiles pour analyser les phases de réponse, d’animation et d’inactivité de votre page.</span><span class="sxs-lookup"><span data-stu-id="4b34d-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="4b34d-109">Prise en main</span><span class="sxs-lookup"><span data-stu-id="4b34d-109">Get started</span></span>  

<span data-ttu-id="4b34d-110">Dans le didacticiel suivant, vous pouvez ouvrir DevTools sur une page en direct et utiliser le volet **performance** pour trouver un goulet d’étranglement de performance dans la page.</span><span class="sxs-lookup"><span data-stu-id="4b34d-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="4b34d-111">Ouvrez Microsoft Edge en **mode InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="4b34d-112">Le mode InPrivate vérifie que Microsoft Edge s’exécute dans un état propre.</span><span class="sxs-lookup"><span data-stu-id="4b34d-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="4b34d-113">Par exemple, si de nombreuses extensions sont installées, les extensions peuvent créer un bruit dans vos mesures de performance.</span><span class="sxs-lookup"><span data-stu-id="4b34d-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="4b34d-114">Chargez la page suivante dans votre fenêtre InPrivate.</span><span class="sxs-lookup"><span data-stu-id="4b34d-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="4b34d-115">Il s’agit de la démonstration que vous allez Profiler.</span><span class="sxs-lookup"><span data-stu-id="4b34d-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="4b34d-116">La page affiche un grand nombre d’icônes déplacées vers le haut et vers le bas.</span><span class="sxs-lookup"><span data-stu-id="4b34d-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="4b34d-117">Sélectionnez `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \) pour ouvrir devtools.</span><span class="sxs-lookup"><span data-stu-id="4b34d-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="4b34d-119">La démonstration à gauche et DevTools sur la droite</span><span class="sxs-lookup"><span data-stu-id="4b34d-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4b34d-120">Pour les autres figures, DevTools est ancré dans [une fenêtre séparée][DevtoolsCustomizePlacement] pour mieux vous concentrer sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="4b34d-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <span data-ttu-id="4b34d-121">Simuler une UC mobile</span><span class="sxs-lookup"><span data-stu-id="4b34d-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="4b34d-122">Les appareils mobiles disposent d’une puissance UC plus réduite que les ordinateurs de bureau et les ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="4b34d-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="4b34d-123">Dès lors que vous profilez une page, utilisez la limitation de l’UC pour simuler l’exécution de votre page sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="4b34d-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="4b34d-124">Dans DevTools, sélectionnez l’onglet **performances** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-124">In DevTools, choose the **Performance** tab.</span></span>  
1.  <span data-ttu-id="4b34d-125">Vérifiez que la case à cocher **captures d’écran** est activée.</span><span class="sxs-lookup"><span data-stu-id="4b34d-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="4b34d-126">Choisir les **paramètres de capture** Paramètres de capture] [ImageCaptureSettingsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4b34d-126">Choose **Capture Settings** \(![Capture Settings][ImageCaptureSettingsIcon]\).</span></span>  <span data-ttu-id="4b34d-127">DevTools révèle les paramètres liés à la manière dont il capture les métriques de performances.</span><span class="sxs-lookup"><span data-stu-id="4b34d-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="4b34d-128">Pour **processeur**, sélectionnez **4x Slowdown**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="4b34d-129">DevTools limite votre processeur de sorte qu’il soit 4 fois plus lent que d’habitude.</span><span class="sxs-lookup"><span data-stu-id="4b34d-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="4b34d-131">Accélérateur d’UC</span><span class="sxs-lookup"><span data-stu-id="4b34d-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4b34d-132">Lors du test d’autres pages; Si vous souhaitez garantir le fonctionnement correct de chaque page sur les appareils mobiles de bas de gamme, définissez la limitation de processeur à **6**fois.</span><span class="sxs-lookup"><span data-stu-id="4b34d-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="4b34d-133">La démonstration ne fonctionne pas correctement avec 6 fois, ce qui signifie qu’elle utilise uniquement 4x pour les opérations d’instructions.</span><span class="sxs-lookup"><span data-stu-id="4b34d-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="4b34d-134">Configurer la démonstration</span><span class="sxs-lookup"><span data-stu-id="4b34d-134">Set up the demo</span></span>  

<span data-ttu-id="4b34d-135">Il est difficile de créer une démonstration de performance d’exécution qui fonctionne de façon cohérente pour tous les utilisateurs du site Web.</span><span class="sxs-lookup"><span data-stu-id="4b34d-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="4b34d-136">La section suivante vous permet de personnaliser la démonstration pour vous assurer que votre interface est relativement cohérente avec les captures d’écran et les descriptions, quelle que soit la configuration de votre choix.</span><span class="sxs-lookup"><span data-stu-id="4b34d-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="4b34d-137">Choisissez le bouton **Ajouter 10** jusqu’à ce que les icônes bleues se déplacent sensiblement plus lentement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="4b34d-138">Sur une machine haut de gamme, il est possible que vous le choisissiez 20 fois.</span><span class="sxs-lookup"><span data-stu-id="4b34d-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="4b34d-139">Sélectionnez **optimiser**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-139">Choose **Optimize**.</span></span>  <span data-ttu-id="4b34d-140">Les icônes bleues doivent se déplacer plus rapidement et plus facilement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4b34d-141">Pour mieux afficher une différence entre les versions optimisées et non optimisées, cliquez sur le bouton **soustraire 10** quelques fois et réessayez.</span><span class="sxs-lookup"><span data-stu-id="4b34d-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="4b34d-142">Si vous ajoutez un trop grand nombre d’icônes bleues, il est possible que vous ayez épuisé le processeur, et que vous n’ayez pas à observer une différence majeure dans les résultats pour les deux versions.</span><span class="sxs-lookup"><span data-stu-id="4b34d-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="4b34d-143">Sélectionnez **Annuler l’optimisation**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="4b34d-144">Les icônes bleues se déplacent plus lentement et plus lente.</span><span class="sxs-lookup"><span data-stu-id="4b34d-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <span data-ttu-id="4b34d-145">Enregistrer les performances d’exécution</span><span class="sxs-lookup"><span data-stu-id="4b34d-145">Record runtime performance</span></span>  

<span data-ttu-id="4b34d-146">Lorsque vous avez exécuté la version optimisée de la page, les icônes bleu se déplacent plus vite.</span><span class="sxs-lookup"><span data-stu-id="4b34d-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="4b34d-147">Pourquoi?</span><span class="sxs-lookup"><span data-stu-id="4b34d-147">Why is that?</span></span>  <span data-ttu-id="4b34d-148">Les deux versions sont supposées déplacer les icônes de la même quantité d’espace sur une même durée.</span><span class="sxs-lookup"><span data-stu-id="4b34d-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="4b34d-149">Prenez un enregistrement dans le panneau performance pour découvrir comment détecter le goulet d’étranglement de performance dans la version non optimisée.</span><span class="sxs-lookup"><span data-stu-id="4b34d-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="4b34d-150">Dans DevTools, sélectionnez **Enregistrer** \ (! [ Record] [ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4b34d-150">In DevTools, choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  <span data-ttu-id="4b34d-151">DevTools capture les métriques de performances lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="4b34d-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="4b34d-153">Profil de la page</span><span class="sxs-lookup"><span data-stu-id="4b34d-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b34d-154">Patientez quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="4b34d-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="4b34d-155">Cliquez sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-155">Choose **Stop**.</span></span>  <span data-ttu-id="4b34d-156">DevTools arrête d’enregistrer, traite les données, puis affiche les résultats dans le panneau performance.</span><span class="sxs-lookup"><span data-stu-id="4b34d-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="4b34d-158">Résultats du profil</span><span class="sxs-lookup"><span data-stu-id="4b34d-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4b34d-159">C’est un volume de données énorme.</span><span class="sxs-lookup"><span data-stu-id="4b34d-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="4b34d-160">ne vous inquiétez pas, le processus va bientôt être plus évocateur.</span><span class="sxs-lookup"><span data-stu-id="4b34d-160">do not worry, soon the process makes more sense.</span></span>  

## <span data-ttu-id="4b34d-161">Analyser les résultats</span><span class="sxs-lookup"><span data-stu-id="4b34d-161">Analyze the results</span></span>  

<span data-ttu-id="4b34d-162">Après avoir enregistré les performances de la page, mesurez la qualité des performances de celle-ci et recherchez les causes éventuelles.</span><span class="sxs-lookup"><span data-stu-id="4b34d-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <span data-ttu-id="4b34d-163">Analyser les images par seconde</span><span class="sxs-lookup"><span data-stu-id="4b34d-163">Analyze frames per second</span></span>  

<span data-ttu-id="4b34d-164">Le principal indicateur de mesure des performances d’une animation est le nombre d’images par seconde (FPS).</span><span class="sxs-lookup"><span data-stu-id="4b34d-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="4b34d-165">Les utilisateurs sont satisfaits lorsque les animations s’exécutent à 60 ips.</span><span class="sxs-lookup"><span data-stu-id="4b34d-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="4b34d-166">Regardez le graphique **fps** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-166">Look at the **FPS** chart.</span></span>  <span data-ttu-id="4b34d-167">Dès lors que vous voyez une barre rouge au-dessus de fps, cela signifie que la fréquence d' **images**a été déplacée et qu’elle est probablement à l’abri de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b34d-167">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="4b34d-168">En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.</span><span class="sxs-lookup"><span data-stu-id="4b34d-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="4b34d-170">Graphique **fps**</span><span class="sxs-lookup"><span data-stu-id="4b34d-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b34d-171">Sous le graphique **fps** , vous pouvez voir le graphique **CPU** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-171">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="4b34d-172">Les couleurs du graphique **UC** correspondent aux couleurs sous l’onglet **Résumé** , au bas du panneau de performance.</span><span class="sxs-lookup"><span data-stu-id="4b34d-172">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="4b34d-173">Le fait que le graphique **UC** est plein de couleur signifie que le processeur a été épuisé lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="4b34d-174">Chaque fois que vous voyez le processeur épuisé pour des périodes longues, il s’agit d’un indicateur pour trouver des moyens d’effectuer moins de tâches.</span><span class="sxs-lookup"><span data-stu-id="4b34d-174">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="4b34d-176">Onglet graphique **UC** et **synthèse**</span><span class="sxs-lookup"><span data-stu-id="4b34d-176">The **CPU** chart and **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b34d-177">Pointez sur les graphiques **fps**, **UC**ou **net** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="4b34d-178">DevTools affiche une capture d’écran de la page à ce moment.</span><span class="sxs-lookup"><span data-stu-id="4b34d-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="4b34d-179">Déplacez votre souris vers la gauche ou la droite pour relire l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="4b34d-180">L’action est référencée en tant que défilement et est utile pour analyser manuellement la progression des animations.</span><span class="sxs-lookup"><span data-stu-id="4b34d-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="4b34d-182">Affichage d’une capture d’écran de la page de l' 2500ms marque de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="4b34d-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b34d-183">Dans la section **trames** , pointez sur l’un des carrés verts.</span><span class="sxs-lookup"><span data-stu-id="4b34d-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="4b34d-184">DevTools vous indique les FPS pour cette image particulière.</span><span class="sxs-lookup"><span data-stu-id="4b34d-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="4b34d-185">Chaque image est probablement bien en dessous de la cible de 60 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="4b34d-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="4b34d-187">Pointer sur un cadre</span><span class="sxs-lookup"><span data-stu-id="4b34d-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4b34d-188">Bien entendu, vous devez constater que la page ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-188">Of course, you should see that the page is not performing well.</span></span>  <span data-ttu-id="4b34d-189">Néanmoins, dans de véritables scénarios, il est possible qu’il n’y ait pas de clarté, de sorte que tous les outils de mesure soient utiles.</span><span class="sxs-lookup"><span data-stu-id="4b34d-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="4b34d-190">Bonus: Ouvrez la jauge FPS</span><span class="sxs-lookup"><span data-stu-id="4b34d-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="4b34d-191">Un autre outil pratique est le Vumètre d’FPS, qui fournit des estimations en temps réel pour les images par seconde lors de l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="4b34d-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="4b34d-192">Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="4b34d-193">Commencez `Rendering` à taper dans le **menu de commandes** et sélectionnez Afficher le **rendu**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="4b34d-194">Dans l’onglet **rendu** , activez l' **indicateur fps**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-194">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="4b34d-195">Une nouvelle superposition s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4b34d-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="4b34d-197">**Vumètre fps**</span><span class="sxs-lookup"><span data-stu-id="4b34d-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="4b34d-198">Désactivez le **compteur fps** et sélectionnez `Escape` pour fermer l’onglet **rendu** .  Dans ce didacticiel, vous n’utilisez pas le **compteur fps** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-198">Disable the **FPS Meter** and select `Escape` to close the **Rendering** tab.  You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <span data-ttu-id="4b34d-199">Détecter le goulet d’étranglement</span><span class="sxs-lookup"><span data-stu-id="4b34d-199">Find the bottleneck</span></span>  

<span data-ttu-id="4b34d-200">Après avoir mesuré et vérifié que l’animation ne fonctionne pas correctement, l’étape suivante consiste à répondre à la question «pourquoi?».</span><span class="sxs-lookup"><span data-stu-id="4b34d-200">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="4b34d-201">Lorsque l’option aucun événement n’est sélectionnée, l’onglet **Résumé** affiche une répartition des activités.</span><span class="sxs-lookup"><span data-stu-id="4b34d-201">When no events are selected, the **Summary** tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="4b34d-202">Page ayant consacré la plupart des heures de rendu.</span><span class="sxs-lookup"><span data-stu-id="4b34d-202">The page spent most of the time rendering.</span></span>  <span data-ttu-id="4b34d-203">Étant donné que les performances constituent une idée d’avoir moins de travail, vous pouvez réduire la durée du travail de rendu.</span><span class="sxs-lookup"><span data-stu-id="4b34d-203">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="4b34d-205">Onglet **Résumé**</span><span class="sxs-lookup"><span data-stu-id="4b34d-205">The **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b34d-206">Développez la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-206">Expand the **Main** section.</span></span>  <span data-ttu-id="4b34d-207">DevTools affiche un graphique d’activité sur le thread principal, au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="4b34d-207">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="4b34d-208">L’axe x représente l’enregistrement au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="4b34d-208">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="4b34d-209">Chaque barre représente un événement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-209">Each bar represents an event.</span></span>  <span data-ttu-id="4b34d-210">Une barre plus large signifie que l’événement a duré plus longtemps.</span><span class="sxs-lookup"><span data-stu-id="4b34d-210">A wider bar means that event took longer.</span></span>  <span data-ttu-id="4b34d-211">L’axe y représente la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="4b34d-211">The y-axis represents the call stack.</span></span>  <span data-ttu-id="4b34d-212">Lorsque des événements sont empilés les uns sur les autres, cela signifie que les événements supérieurs ont entraîné des événements plus faibles.</span><span class="sxs-lookup"><span data-stu-id="4b34d-212">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="4b34d-214">Section **principale**</span><span class="sxs-lookup"><span data-stu-id="4b34d-214">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b34d-215">L’enregistrement comporte un grand nombre de données.</span><span class="sxs-lookup"><span data-stu-id="4b34d-215">There is a lot of data in the recording.</span></span>  <span data-ttu-id="4b34d-216">Pour effectuer un zoom avant sur un seul événement; Maintenez la touche enfoncée, puis faites glisser le curseur sur la **vue d’ensemble**, qui est la section incluant les graphiques **fps**, **UC**et **net** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-216">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="4b34d-217">Les onglets **principales** section et **Résumé** affichent uniquement les informations relatives à la partie sélectionnée de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-217">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="4b34d-219">Effectuer un zoom avant sur un événement</span><span class="sxs-lookup"><span data-stu-id="4b34d-219">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4b34d-220">Pour effectuer un zoom, vous pouvez également mettre le focus sur la section **principale** , sélectionner l’arrière-plan ou un événement, puis sélectionner `W` ,, `A` `S` ou `D` .</span><span class="sxs-lookup"><span data-stu-id="4b34d-220">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="4b34d-221">Focalisez-vous sur le triangle rouge dans le coin supérieur droit du **cadre d’animation** qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-221">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4b34d-222">Dès lors que vous voyez un triangle rouge, il s’agit d’un avertissement indiquant qu’il y a peut-être un problème lié à l’événement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-222">Whenever you see a red triangle, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4b34d-223">Le **Frame d’animation déclenché est déclenché** chaque fois qu’un [ `requestAnimationFrame()` rappel][MDNWebRequestAnimationFrame] est exécuté.</span><span class="sxs-lookup"><span data-stu-id="4b34d-223">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="4b34d-224">Choisissez le **cadre d’animation** qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-224">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4b34d-225">L’onglet **Résumé** affiche maintenant des informations sur cet événement.</span><span class="sxs-lookup"><span data-stu-id="4b34d-225">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="4b34d-226">Notez le lien d' **affichage** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-226">Note the **Reveal** link.</span></span>  <span data-ttu-id="4b34d-227">Après l’avoir sélectionnée, DevTools met en surbrillance l’événement qui a déclenché l’événement déclenché par le cadre de l' **animation** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-227">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4b34d-228">Par ailleurs, le focus se trouve sur le lien **app.js:95** .</span><span class="sxs-lookup"><span data-stu-id="4b34d-228">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="4b34d-229">Une fois que vous avez choisi, la ligne appropriée dans le code source s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4b34d-229">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="4b34d-231">Plus d’informations sur l’événement déclenché par le **cadre d’animation**</span><span class="sxs-lookup"><span data-stu-id="4b34d-231">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4b34d-232">Après avoir sélectionné un événement, utilisez les touches de direction pour sélectionner les événements en regard de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="4b34d-232">After selecting an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="4b34d-233">Sous l’événement **app. Update** , il existe un ensemble d’événements Purple.</span><span class="sxs-lookup"><span data-stu-id="4b34d-233">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="4b34d-234">Si chaque événement pourpre était plus large, il semblerait que chacun d’entre eux ait un triangle rouge.</span><span class="sxs-lookup"><span data-stu-id="4b34d-234">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="4b34d-235">Choisissez l’un des événements de **disposition** Purple.</span><span class="sxs-lookup"><span data-stu-id="4b34d-235">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="4b34d-236">DevTools fournit des informations supplémentaires sur l’événement sous l’onglet **Résumé** .  En effet, il y a un avertissement sur les flux forcés \ (un autre mot pour la disposition \).</span><span class="sxs-lookup"><span data-stu-id="4b34d-236">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="4b34d-237">Sous l’onglet **Résumé** , sélectionnez le lien **app.js:71** sous **disposition forcée**.</span><span class="sxs-lookup"><span data-stu-id="4b34d-237">In the **Summary** tab, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="4b34d-238">DevTools vous permet d’accéder à la ligne de code qui force la mise en page.</span><span class="sxs-lookup"><span data-stu-id="4b34d-238">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="4b34d-240">Ligne de code à l’origine de la disposition forcée.</span><span class="sxs-lookup"><span data-stu-id="4b34d-240">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4b34d-241">Le problème lié au code consiste à modifier le style de chaque icône dans chaque cadre d’animation, puis à interroger la position de chaque icône de la page.</span><span class="sxs-lookup"><span data-stu-id="4b34d-241">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="4b34d-242">Étant donné que les styles ont changé, le navigateur ne sait pas si chaque position de l’icône a changé, donc il doit redisposer l’icône afin de calculer la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="4b34d-242">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="4b34d-243">C’est beaucoup plus important.</span><span class="sxs-lookup"><span data-stu-id="4b34d-243">That was a lot to learn.</span></span>  <span data-ttu-id="4b34d-244">Vous avez à présent une base solide dans le flux de travail de base pour analyser les performances de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4b34d-244">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="4b34d-245">Bien fait.</span><span class="sxs-lookup"><span data-stu-id="4b34d-245">Good job.</span></span>  

### <span data-ttu-id="4b34d-246">Bonus: analysez la version optimisée</span><span class="sxs-lookup"><span data-stu-id="4b34d-246">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="4b34d-247">À l’aide des flux de travail et des outils que vous venez d’apprendre, sélectionnez **optimiser** dans la démonstration pour activer le code optimisé, effectuer un autre enregistrement de performance, puis analyser les résultats.</span><span class="sxs-lookup"><span data-stu-id="4b34d-247">Using the workflows and tools that you just learned, choose **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="4b34d-248">À partir de la fréquence améliorée pour la réduction des événements dans le graphique de flamme de la section **principale** , vous pouvez voir que la version optimisée de l’application est beaucoup moins importante, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="4b34d-248">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you are able to see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="4b34d-249">Même la version optimisée n’est pas idéale, car elle manipule la `top` propriété de chaque icône.</span><span class="sxs-lookup"><span data-stu-id="4b34d-249">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="4b34d-250">Une meilleure approche consiste à respecter les propriétés qui affectent uniquement la composition.</span><span class="sxs-lookup"><span data-stu-id="4b34d-250">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="4b34d-251">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4b34d-251">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="4b34d-252">Pour plus de confort grâce au panneau performances, vous pouvez faire des exercices pratiques.</span><span class="sxs-lookup"><span data-stu-id="4b34d-252">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="4b34d-253">Essayez de Profiler vos pages et d’analyser les résultats.</span><span class="sxs-lookup"><span data-stu-id="4b34d-253">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="4b34d-254">Si vous avez des questions sur les résultats, utilisez l’icône d' **envoi de commentaires** , sélectionnez \ `Alt` + `Shift` + `I` (Windows, Linux \), `Option` + `Shift` + `I` \ (MacOS \) ou [tweeter l’équipe devtools][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="4b34d-254">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="4b34d-255">Incluez des captures d’écran ou des liens vers des pages reproductibles, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4b34d-255">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="La démonstration à gauche et DevTools sur la droite" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="4b34d-257">Icône **Envoyer des commentaires** dans Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="4b34d-257">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="4b34d-258">Enfin, il existe de nombreuses façons d’améliorer les performances de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4b34d-258">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="4b34d-259">Cet article a été axé sur un goulet d’étranglement d’animation particulier pour vous permettre d’effectuer une visite guidée dans le panneau performance, mais ce n’est qu’un des nombreux goulets d’étranglement que vous pouvez rencontrer.</span><span class="sxs-lookup"><span data-stu-id="4b34d-259">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <span data-ttu-id="4b34d-260">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="4b34d-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-publiez un tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> <span data-ttu-id="4b34d-265">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4b34d-265">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4b34d-266">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="4b34d-266">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="4b34d-268">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4b34d-268">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
