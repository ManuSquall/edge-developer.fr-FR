---
description: 'Les principales utilisations de la console Microsoft Edge DevTools: journalisation des messages et exécution de JavaScript.'
title: Présentation de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 32272c3f76f715566ced66d11346985dc95dd290
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125264"
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

# <span data-ttu-id="368e1-104">Présentation de la console</span><span class="sxs-lookup"><span data-stu-id="368e1-104">Console Overview</span></span>  

  

<span data-ttu-id="368e1-105">Cette page décrit la façon dont la console Microsoft Edge DevTools simplifie le développement de pages Web.</span><span class="sxs-lookup"><span data-stu-id="368e1-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="368e1-106">La console a 2 utilisations principales: [afficher les messages enregistrés](#viewing-logged-messages) et [exécuter JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="368e1-106">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="368e1-107">Affichage des messages enregistrés</span><span class="sxs-lookup"><span data-stu-id="368e1-107">Viewing logged messages</span></span>  

<span data-ttu-id="368e1-108">Les développeurs Web enregistrent souvent les messages sur la console pour s’assurer que leur JavaScript fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="368e1-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="368e1-109">Pour enregistrer un message, vous devez insérer une expression telle que `console.log('Hello, Console!')` dans votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="368e1-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="368e1-110">Lorsque le navigateur exécute votre JavaScript et voit une expression semblable à celle-ci, il enregistre le message sur la console.</span><span class="sxs-lookup"><span data-stu-id="368e1-110">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="368e1-111">HTML et JavaScript pour la page.</span><span class="sxs-lookup"><span data-stu-id="368e1-111">The HTML and JavaScript for the page.</span></span>  
      
      ```html
      <!doctype html>
      <html>
          <head>
              <title>Console Demo</title>
          </head>
          <body>
              <h1>Hello, World!</h1>
              <script>
                  console.log('Loading!');
                  const h1 = document.querySelector('h1');
                  console.log(h1.textContent);
                  console.assert(document.querySelector('h2'), 'h2 not found!');
                  const artists = [
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
                  ];
                  console.table(artists);
                  setTimeout(() => {
                      h1.textContent = 'Hello, Console!';
                      console.log(h1.textContent);
                  }, 3000);
              </script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="368e1-112">Dans l’illustration suivante, la **console** affiche les résultats du chargement de la page et l’attente de 3 secondes.</span><span class="sxs-lookup"><span data-stu-id="368e1-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Panneau de la console" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="368e1-114">Panneau de la **console**</span><span class="sxs-lookup"><span data-stu-id="368e1-114">The **Console** panel</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="368e1-115">Essayez de déterminer les lignes de code à l’origine du journal du navigateur.</span><span class="sxs-lookup"><span data-stu-id="368e1-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="368e1-116">Les développeurs Web consignent les messages pour les 2 raisons générales suivantes.</span><span class="sxs-lookup"><span data-stu-id="368e1-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="368e1-117">Vérifier que le code s’exécute dans l’ordre approprié.</span><span class="sxs-lookup"><span data-stu-id="368e1-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="368e1-118">Inspecter les valeurs des variables à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="368e1-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="368e1-119">Pour en savoir plus sur la journalisation, voir [utiliser les messages de journalisation][DevtoolsConsoleLoggingMessages] .</span><span class="sxs-lookup"><span data-stu-id="368e1-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="368e1-120">Pour consulter la liste complète des méthodes, voir la référence de l’API de la [console][DevToolsConsoleAPI] `console` .</span><span class="sxs-lookup"><span data-stu-id="368e1-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="368e1-121">La principale différence entre les méthodes est le mode d’affichage des données qui sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="368e1-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="368e1-122">Exécution de JavaScript</span><span class="sxs-lookup"><span data-stu-id="368e1-122">Running JavaScript</span></span>  

<span data-ttu-id="368e1-123">La **console** est également une [REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="368e1-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="368e1-124">Vous pouvez exécuter JavaScript dans la **console** pour interagir avec la page inspectée.</span><span class="sxs-lookup"><span data-stu-id="368e1-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="368e1-125">Dans l’illustration suivante, la **console** est affichée en regard de la page d’accueil devtools.</span><span class="sxs-lookup"><span data-stu-id="368e1-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Panneau de la console" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="368e1-127">Panneau **console** en regard de la page d’accueil de devtools</span><span class="sxs-lookup"><span data-stu-id="368e1-127">The **Console** panel next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="368e1-128">Dans l’illustration suivante, la même page s’affiche après l’utilisation de la **console** pour modifier le titre supérieur de la page.</span><span class="sxs-lookup"><span data-stu-id="368e1-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Panneau de la console" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="368e1-130">Utiliser la **console** pour modifier le titre supérieur de la page</span><span class="sxs-lookup"><span data-stu-id="368e1-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="368e1-131">La modification de la page à partir de la **console** est possible, car la **console** dispose d’un accès complet à la [fenêtre][MDNWindow] de la page.</span><span class="sxs-lookup"><span data-stu-id="368e1-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="368e1-132">DevTools offre quelques fonctions de commodité qui vous permettent d’inspecter une page plus facilement.</span><span class="sxs-lookup"><span data-stu-id="368e1-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="368e1-133">Par exemple, supposons que votre JavaScript contienne une fonction appelée `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="368e1-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="368e1-134">L’exécution `debug(hideModal)` interrompt votre code sur la première ligne `hideModal` la prochaine fois que vous l’exécutez.</span><span class="sxs-lookup"><span data-stu-id="368e1-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="368e1-135">Pour plus d’informations sur la liste complète des fonctions d’utilitaire, [voir][DevtoolsConsoleUtilitiesDebug]informations de référence sur l’API de la console.</span><span class="sxs-lookup"><span data-stu-id="368e1-135">For more information about the full list of utility functions, navigate to [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="368e1-136">Lorsque vous exécutez JavaScript, vous n’avez pas besoin d’interagir avec la page.</span><span class="sxs-lookup"><span data-stu-id="368e1-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="368e1-137">Vous pouvez utiliser la **console** pour essayer le nouveau code non lié à la page.</span><span class="sxs-lookup"><span data-stu-id="368e1-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="368e1-138">Par exemple, supposons que vous viens d’apprendre sur la méthode intégrée de mappage de tableau JavaScript [()][MDNMap] et que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="368e1-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="368e1-139">La **console** est l’endroit idéal pour tester la fonction.</span><span class="sxs-lookup"><span data-stu-id="368e1-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="368e1-140">Pour plus d’informations sur la façon d’utiliser JavaScript dans la **console**, accédez à la section [commencer à utiliser JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="368e1-140">For more hands-on experience with running JavaScript in the **Console**, navigate to [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

## <span data-ttu-id="368e1-141">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="368e1-141">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Référence sur les API de console | Documents Microsoft"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Commencer à utiliser la journalisation des messages dans la console | Documents Microsoft"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Commencer à utiliser JavaScript dans la console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "XXXXXX xxx xxxxxxx xxx xxxxxxx xxxxx Documents Microsoft"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenêtre | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lecture-eval-imprimer en boucle-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="368e1-149">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="368e1-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="368e1-150">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="368e1-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="368e1-152">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="368e1-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
