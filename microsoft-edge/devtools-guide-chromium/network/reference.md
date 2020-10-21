---
description: Référence complète des fonctionnalités du panneau réseau de Microsoft Edge DevTools.
title: Référence d’analyse du réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 8123fbebadf1d43fd1460ecebf91190cac793e19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125369"
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

# <span data-ttu-id="41217-104">Référence d’analyse du réseau</span><span class="sxs-lookup"><span data-stu-id="41217-104">Network Analysis reference</span></span>  

<span data-ttu-id="41217-105">Découvrez de nouvelles façons d’analyser le chargement de votre page dans cette référence complète des fonctionnalités d’analyse du réseau Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="41217-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  To verify which version of Microsoft Edge you are running, navigate to `edge://help`.  
-->

## <span data-ttu-id="41217-106">Enregistrer les requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="41217-106">Record network requests</span></span>  

<span data-ttu-id="41217-107">Par défaut, DevTools enregistre toutes les demandes réseau dans le panneau réseau, tant que DevTools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="41217-107">By default, DevTools record all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="41217-109">Panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="41217-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-110">Arrêter l’enregistrement des requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="41217-110">Stop recording network requests</span></span>  

<span data-ttu-id="41217-111">Pour arrêter l’enregistrement de demandes, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="41217-112">Pour arrêter l' **enregistrement du journal du réseau** , cliquez sur arrêter l' ![ enregistrement réseau ][ImageRecordOnIcon] dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="41217-112">Choose **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="41217-113">Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="41217-114">`Control` + `E` Dans le panneau réseau du réseau, sélectionnez \ (Windows, Linux \) ou `Command` + `E` \ (MacOS \). **Network**</span><span class="sxs-lookup"><span data-stu-id="41217-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="41217-115">Supprimer des demandes</span><span class="sxs-lookup"><span data-stu-id="41217-115">Clear requests</span></span>  

<span data-ttu-id="41217-116">**Clear** ![ Dans le volet réseau, sélectionnez Effacer \ (Clear ][ImageClearIcon] \) pour effacer toutes les demandes de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="41217-118">Bouton **Effacer**</span><span class="sxs-lookup"><span data-stu-id="41217-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-119">Enregistrer les demandes lors du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="41217-119">Save requests across page loads</span></span>  

<span data-ttu-id="41217-120">Pour enregistrer les demandes lors du chargement de la page, activez la case à cocher **conservation du journal** dans le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="41217-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="41217-121">DevTools enregistre toutes les demandes jusqu’à ce que vous désactiviez le **Journal de conservation**.</span><span class="sxs-lookup"><span data-stu-id="41217-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="41217-123">Case à cocher **conserver le journal**</span><span class="sxs-lookup"><span data-stu-id="41217-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-124">Capture de captures d’écran pendant le chargement de la page</span><span class="sxs-lookup"><span data-stu-id="41217-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="41217-125">Capture des captures d’écran permettant d’analyser ce qui s’affiche pour les utilisateurs lorsque vous patientez pendant le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="41217-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="41217-126">Pour activer les captures d’écran, choisissez **paramètres du réseau** , puis cochez la case **capturer les captures d’écran** dans le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="41217-126">To enable screenshots, choose **Network settings** and choose **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="41217-127">Actualisez la page lorsque le panneau **réseau** a le focus pour capturer les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="41217-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="41217-128">Après avoir capturé une capture d’écran, vous interagissez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="41217-129">Placez le pointeur de la souris sur une capture d’écran pour afficher le point d’acquisition de cette capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="41217-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="41217-130">Une ligne jaune s’affiche dans le volet **vue d’ensemble** .</span><span class="sxs-lookup"><span data-stu-id="41217-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="41217-131">Sélectionnez la miniature d’un écran pour filtrer toutes les demandes qui se sont produites après la capture de la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="41217-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="41217-132">Double-cliquez sur une miniature pour y effectuer un zoom.</span><span class="sxs-lookup"><span data-stu-id="41217-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="41217-134">Survol d’une capture d’écran</span><span class="sxs-lookup"><span data-stu-id="41217-134">Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Panneau réseau" lightbox="../media/network-replay-xhr.msft.png":::
   Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="41217-135">Changer le comportement de chargement</span><span class="sxs-lookup"><span data-stu-id="41217-135">Change loading behavior</span></span>  

### <span data-ttu-id="41217-136">Émuler un visiteur pour la première fois en désactivant le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="41217-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="41217-137">Pour émuler la façon dont un utilisateur a expériences de votre site pour la première fois, activez la case à cocher **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="41217-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="41217-138">DevTools désactive le cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="41217-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="41217-139">Cette fonctionnalité émule plus précisément l’utilisation de la première utilisation de l’utilisateur, car les requêtes sont servies dans le cache du navigateur lors de plusieurs visites.</span><span class="sxs-lookup"><span data-stu-id="41217-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="41217-141">Case à cocher **désactiver le cache**</span><span class="sxs-lookup"><span data-stu-id="41217-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="41217-142">Désactiver le cache du navigateur dans le tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="41217-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="41217-143">Si vous voulez désactiver le cache lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="41217-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="41217-144">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="41217-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="41217-145">Cochez ou décochez la case **désactiver le cache** .</span><span class="sxs-lookup"><span data-stu-id="41217-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="41217-146">Vider manuellement le cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="41217-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="41217-147">Pour vider manuellement le cache du navigateur à tout moment, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) n’importe où dans la table demandes et sélectionnez **Vider le cache du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="41217-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="41217-149">Sélection de l’option **Vider le cache du navigateur**</span><span class="sxs-lookup"><span data-stu-id="41217-149">Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-150">Émuler hors connexion</span><span class="sxs-lookup"><span data-stu-id="41217-150">Emulate offline</span></span>  

<span data-ttu-id="41217-151">Une nouvelle classe d’applications Web, appelées [applications Web progressives][DevtoolsProgressiveWebApps], fonctionne en mode hors connexion avec l’aide des **travailleurs de service**.</span><span class="sxs-lookup"><span data-stu-id="41217-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="41217-152">Vous constaterez peut-être qu’il est utile de simuler rapidement un appareil dépourvu de connexion aux données lors de la création de ce type d’application.</span><span class="sxs-lookup"><span data-stu-id="41217-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="41217-153">Sélectionnez le menu déroulant **en ligne** , recherchez sous **présélections**, puis sélectionnez **hors ligne** pour simuler une utilisation du réseau hors connexion.</span><span class="sxs-lookup"><span data-stu-id="41217-153">Select the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="41217-155">Menu déroulant **hors connexion**</span><span class="sxs-lookup"><span data-stu-id="41217-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-156">Émuler une connexion réseau lente</span><span class="sxs-lookup"><span data-stu-id="41217-156">Emulate slow network connections</span></span>  

<span data-ttu-id="41217-157">Émulez des vitesses de connexion 3G, Fast 3G et autres vitesses de connexion dans le menu déroulant **en ligne** .</span><span class="sxs-lookup"><span data-stu-id="41217-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="41217-159">Menu déroulant **limitation**</span><span class="sxs-lookup"><span data-stu-id="41217-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="41217-160">Vous pouvez choisir parmi différents préréglages, par exemple, lente 3G ou Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="41217-160">You may select from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="41217-161">Vous pouvez également ajouter vos propres Présélections personnalisées en ouvrant le menu limitation et **Custom**en sélectionnant  >  **Ajouter**personnalisé.</span><span class="sxs-lookup"><span data-stu-id="41217-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="41217-162">DevTools affiche une icône d’avertissement en regard de l’onglet **réseau** pour vous rappeler que la limitation est activée.</span><span class="sxs-lookup"><span data-stu-id="41217-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="41217-163">Émuler une connexion réseau lente à partir du tiroir du réseau</span><span class="sxs-lookup"><span data-stu-id="41217-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="41217-164">Si vous souhaitez limiter la connexion réseau lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="41217-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="41217-165">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="41217-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="41217-166">Sélectionnez votre vitesse de connexion dans le menu **limitation** .</span><span class="sxs-lookup"><span data-stu-id="41217-166">Select your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="41217-167">Effacement manuel des cookies du navigateur</span><span class="sxs-lookup"><span data-stu-id="41217-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="41217-168">Pour effacer manuellement les cookies du navigateur à tout moment, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) n’importe où dans la table demandes, puis sélectionnez **effacer les cookies du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="41217-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="41217-170">Sélection **effacer les cookies du navigateur**</span><span class="sxs-lookup"><span data-stu-id="41217-170">Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-171">Remplacer l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="41217-171">Override the user agent</span></span>  

<span data-ttu-id="41217-172">Pour remplacer manuellement l’agent utilisateur, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-173">Ouvrez le tiroir de **conditions du réseau** .</span><span class="sxs-lookup"><span data-stu-id="41217-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="41217-174">Décochez l' **option sélectionner automatiquement**.</span><span class="sxs-lookup"><span data-stu-id="41217-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="41217-175">Choisissez une option de l’agent utilisateur dans le menu ou entrez-en un dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="41217-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="41217-176">Demandes de filtre</span><span class="sxs-lookup"><span data-stu-id="41217-176">Filter requests</span></span>  

### <span data-ttu-id="41217-177">Filtrer les demandes par propriétés</span><span class="sxs-lookup"><span data-stu-id="41217-177">Filter requests by properties</span></span>  

<span data-ttu-id="41217-178">Utilisez la zone de texte **filtre** pour filtrer les demandes par propriétés, telles que le domaine ou la taille de la requête.</span><span class="sxs-lookup"><span data-stu-id="41217-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="41217-179">Si la zone de texte n’est pas affichée, le volet **filtres** est probablement masqué.</span><span class="sxs-lookup"><span data-stu-id="41217-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="41217-180">Pour plus d’informations, accédez à [la section masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="41217-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="41217-182">Zone de texte **filtre**</span><span class="sxs-lookup"><span data-stu-id="41217-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="41217-183">Vous pouvez utiliser plusieurs propriétés simultanément en séparant chaque propriété d’un espace.</span><span class="sxs-lookup"><span data-stu-id="41217-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="41217-184">Par exemple, `mime-type:image/png larger-than:1K` affiche tous les png dont la taille est supérieure à 1 kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="41217-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="41217-185">Les filtres multi-propriétés sont équivalents aux `AND` opérations.</span><span class="sxs-lookup"><span data-stu-id="41217-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="41217-186">les opérations ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="41217-186">operations are currently not supported.</span></span>  

<span data-ttu-id="41217-187">Liste complète des propriétés prises en charge.</span><span class="sxs-lookup"><span data-stu-id="41217-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="41217-188">Propriété</span><span class="sxs-lookup"><span data-stu-id="41217-188">Property</span></span> | <span data-ttu-id="41217-189">Détails</span><span class="sxs-lookup"><span data-stu-id="41217-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="41217-190">Afficher uniquement les ressources du domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="41217-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="41217-191">Vous pouvez utiliser un caractère générique \ ( `*` \) pour inclure plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="41217-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="41217-192">Par exemple, `*.com` affiche les ressources de tous les noms de domaine se terminant par `.com` .</span><span class="sxs-lookup"><span data-stu-id="41217-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="41217-193">DevTools peuplez le menu déroulant de saisie semi-automatique avec tous les domaines trouvés.</span><span class="sxs-lookup"><span data-stu-id="41217-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="41217-194">Affiche les ressources contenant l’en-tête de réponse HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="41217-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="41217-195">DevTools remplissez la liste déroulante de saisie semi-automatique avec tous les en-têtes de réponse détectés.</span><span class="sxs-lookup"><span data-stu-id="41217-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="41217-196">Utiliser `is:running` pour rechercher des `WebSocket` ressources.</span><span class="sxs-lookup"><span data-stu-id="41217-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="41217-197">Affiche les ressources dont la taille est supérieure à la taille spécifiée, en octets.</span><span class="sxs-lookup"><span data-stu-id="41217-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="41217-198">La définition d’une valeur est égale à la valeur `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="41217-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="41217-199">Affiche les ressources récupérées par le biais d’un type de méthode HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="41217-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="41217-200">DevTools remplissez la liste déroulante avec toutes les méthodes HTTP trouvées.</span><span class="sxs-lookup"><span data-stu-id="41217-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="41217-201">Affiche les ressources d’un type MIME spécifié.</span><span class="sxs-lookup"><span data-stu-id="41217-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="41217-202">DevTools remplissez la liste déroulante à l’aide de tous les types MIME trouvés.</span><span class="sxs-lookup"><span data-stu-id="41217-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="41217-203">Affichez toutes les ressources de contenu mixte \ ( `mixed-content:all` \) ou uniquement celles actuellement affichées \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="41217-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="41217-204">Affiche les ressources récupérées par le biais d’une connexion HTTP \ ( `scheme:http` \) ou protégé https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="41217-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="41217-205">Affiche les ressources qui ont un `Set-Cookie` en-tête avec un `Domain` attribut qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="41217-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="41217-206">DevTools remplir la saisie semi-automatique avec tous les domaines de cookie détectés.</span><span class="sxs-lookup"><span data-stu-id="41217-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="41217-207">Affiche les ressources possédant un `Set-Cookie` en-tête dont le nom correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="41217-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="41217-208">DevTools remplir la saisie semi-automatique à l’aide du nom de cookie détecté.</span><span class="sxs-lookup"><span data-stu-id="41217-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="41217-209">Affiche les ressources dont `Set-Cookie` l’en-tête comporte une valeur qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="41217-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="41217-210">DevTools remplir la saisie semi-automatique avec toutes les valeurs de cookie trouvées.</span><span class="sxs-lookup"><span data-stu-id="41217-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="41217-211">Affiche les ressources qui correspondent au code d’état HTTP spécifique.</span><span class="sxs-lookup"><span data-stu-id="41217-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="41217-212">DevTools remplit le menu déroulant de saisie semi-automatique avec tous les codes d’État trouvés.</span><span class="sxs-lookup"><span data-stu-id="41217-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="41217-213">Filtrer les demandes par type</span><span class="sxs-lookup"><span data-stu-id="41217-213">Filter requests by type</span></span>  

<span data-ttu-id="41217-214">Pour filtrer les demandes par type de requête, sélectionnez l’un des boutons suivants dans le volet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="41217-214">To filter requests by request type, select the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-215">XHR</span><span class="sxs-lookup"><span data-stu-id="41217-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-216">JS</span><span class="sxs-lookup"><span data-stu-id="41217-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-217">CSS</span><span class="sxs-lookup"><span data-stu-id="41217-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-218">IMG</span><span class="sxs-lookup"><span data-stu-id="41217-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-219">Media</span><span class="sxs-lookup"><span data-stu-id="41217-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-220">Police</span><span class="sxs-lookup"><span data-stu-id="41217-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-221">Documentation</span><span class="sxs-lookup"><span data-stu-id="41217-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-222">NOMBRES</span><span class="sxs-lookup"><span data-stu-id="41217-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="41217-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-224">Manifeste</span><span class="sxs-lookup"><span data-stu-id="41217-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-225">Other</span><span class="sxs-lookup"><span data-stu-id="41217-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-226">Tout autre type qui ne figure pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="41217-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="41217-227">Si ce n’est pas le cas, le volet **filtres** est masqué.</span><span class="sxs-lookup"><span data-stu-id="41217-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="41217-228">Pour plus d’informations, accédez à [la section masquer le volet filtres](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="41217-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="41217-229">Pour activer plusieurs filtres de type simultanément, appuyez sur `Control` \ (Windows, Linux \) ou `Command` \ (MacOS \), puis sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="41217-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="41217-231">Utiliser les filtres de type pour afficher les ressources JS, CSS et document</span><span class="sxs-lookup"><span data-stu-id="41217-231">Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-232">Filtrer les demandes par heure</span><span class="sxs-lookup"><span data-stu-id="41217-232">Filter requests by time</span></span>  

<span data-ttu-id="41217-233">Sélectionnez et faites glisser vers la gauche ou la droite dans le volet vue d’ensemble pour afficher uniquement les demandes actives au cours de cette période.</span><span class="sxs-lookup"><span data-stu-id="41217-233">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="41217-234">Le filtre est inclusive.</span><span class="sxs-lookup"><span data-stu-id="41217-234">The filter is inclusive.</span></span>  <span data-ttu-id="41217-235">Toutes les demandes qui ont été actives pendant la durée en surbrillance apparaissent.</span><span class="sxs-lookup"><span data-stu-id="41217-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="41217-237">Filtrage des requêtes inactives de 300 ms</span><span class="sxs-lookup"><span data-stu-id="41217-237">Filtering out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-238">Masquer les URL de données</span><span class="sxs-lookup"><span data-stu-id="41217-238">Hide data URLs</span></span>  

<span data-ttu-id="41217-239">Les [URL de données][MDNHTTPDataURIs] sont des petits fichiers incorporés dans d’autres documents.</span><span class="sxs-lookup"><span data-stu-id="41217-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="41217-240">Toute demande qui s’affiche dans la table demandes qui commence par `data:` est une URL de données.</span><span class="sxs-lookup"><span data-stu-id="41217-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="41217-241">Cochez la case **Masquer les URL de données** pour masquer les demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-241">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="41217-243">Case à cocher **Masquer les URL de données**</span><span class="sxs-lookup"><span data-stu-id="41217-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="41217-244">Demandes de tri</span><span class="sxs-lookup"><span data-stu-id="41217-244">Sort requests</span></span>  

<span data-ttu-id="41217-245">Par défaut, les requêtes dans la table demandes sont triées par heure de début, mais vous pouvez trier le tableau en utilisant d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="41217-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="41217-246">Trier par colonne</span><span class="sxs-lookup"><span data-stu-id="41217-246">Sort by column</span></span>  

<span data-ttu-id="41217-247">Sélectionnez l’en-tête de n’importe quelle colonne dans les requêtes pour trier les demandes en se sur cette colonne.</span><span class="sxs-lookup"><span data-stu-id="41217-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="41217-248">Trier par phase d’activité</span><span class="sxs-lookup"><span data-stu-id="41217-248">Sort by activity phase</span></span>  

<span data-ttu-id="41217-249">Pour modifier la façon dont les demandes de tri d’une cascade sont triées, pointez sur l’en-tête de la table demandes, ouvrez le menu **contextuel, puis**sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="41217-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-250">Heure de début</span><span class="sxs-lookup"><span data-stu-id="41217-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-251">La première requête lancée est en haut.</span><span class="sxs-lookup"><span data-stu-id="41217-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-252">Temps de réponse</span><span class="sxs-lookup"><span data-stu-id="41217-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-253">La première demande qui a démarré le téléchargement est en haut.</span><span class="sxs-lookup"><span data-stu-id="41217-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-254">Heure de fin</span><span class="sxs-lookup"><span data-stu-id="41217-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-255">La première demande qui est terminée est en haut.</span><span class="sxs-lookup"><span data-stu-id="41217-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-256">Durée totale</span><span class="sxs-lookup"><span data-stu-id="41217-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-257">La requête avec les paramètres de connexion les plus courts et la requête ou la réponse est située dans la partie supérieure.</span><span class="sxs-lookup"><span data-stu-id="41217-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-258">Latence</span><span class="sxs-lookup"><span data-stu-id="41217-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-259">La requête qui a attendu le plus court délai d’une réponse est située en haut.</span><span class="sxs-lookup"><span data-stu-id="41217-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="41217-260">Ces descriptions présupposent que chaque option respective est classée du plus court au plus long.</span><span class="sxs-lookup"><span data-stu-id="41217-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="41217-261">La sélection de l’en-tête de la colonne en **cascade** inverse l’ordre.</span><span class="sxs-lookup"><span data-stu-id="41217-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="41217-263">Le tri des cascades en fonction de la durée totale \ (la partie la plus claire de chaque barre est le temps passé en attente et la partie plus foncée est le temps de télécharger les octets \)</span><span class="sxs-lookup"><span data-stu-id="41217-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="41217-264">Analyser les requêtes</span><span class="sxs-lookup"><span data-stu-id="41217-264">Analyze requests</span></span>  

<span data-ttu-id="41217-265">Tant que DevTools est ouvert, il enregistre toutes les demandes dans le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="41217-265">So long as DevTools are open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="41217-266">Utilisez le volet réseau pour analyser les requêtes.</span><span class="sxs-lookup"><span data-stu-id="41217-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="41217-267">Afficher un journal des demandes</span><span class="sxs-lookup"><span data-stu-id="41217-267">View a log of requests</span></span>  

<span data-ttu-id="41217-268">Utilisez le tableau demandes pour afficher un journal de toutes les demandes effectuées lors de l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="41217-268">Use the Requests table to view a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="41217-269">La sélection ou le passage de demandes au-dessus révèle des informations supplémentaires sur chaque élément.</span><span class="sxs-lookup"><span data-stu-id="41217-269">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="41217-271">Table demandes</span><span class="sxs-lookup"><span data-stu-id="41217-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="41217-272">La table demandes affiche les colonnes suivantes par défaut.</span><span class="sxs-lookup"><span data-stu-id="41217-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-273">Nom</span><span class="sxs-lookup"><span data-stu-id="41217-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-274">Nom de fichier ou un identificateur pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="41217-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-275">Statut</span><span class="sxs-lookup"><span data-stu-id="41217-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-276">Code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="41217-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-277">Type</span><span class="sxs-lookup"><span data-stu-id="41217-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-278">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="41217-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-279">Initiateur</span><span class="sxs-lookup"><span data-stu-id="41217-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-280">Les objets ou processus suivants déclenchent des demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="41217-281">**Analyseur**  Analyseur HTML pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="41217-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="41217-282">**Rediriger**  Une redirection HTTP.</span><span class="sxs-lookup"><span data-stu-id="41217-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="41217-283">**Script**  Fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="41217-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="41217-284">**Autres**  Un autre processus ou action, tel que la navigation sur une page à l’aide d’un lien ou la saisie d’une URL dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="41217-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-285">Taille</span><span class="sxs-lookup"><span data-stu-id="41217-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-286">Taille combinée des en-têtes de réponse et du corps de la réponse, tel qu’il est délivré par le serveur.</span><span class="sxs-lookup"><span data-stu-id="41217-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-287">Heure</span><span class="sxs-lookup"><span data-stu-id="41217-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-288">Durée totale, entre le début de la demande et la réception de l’octet final dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="41217-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="41217-289">Cascade</span><span class="sxs-lookup"><span data-stu-id="41217-289">Waterfall</span></span>](#view-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-290">Répartition visuelle de l’activité pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="41217-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="41217-291">Ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="41217-291">Add or remove columns</span></span>  

<span data-ttu-id="41217-292">Placez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez une option pour la masquer ou l’afficher.</span><span class="sxs-lookup"><span data-stu-id="41217-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="41217-293">Les options actuellement affichées disposent de coches en regard de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="41217-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="41217-295">Ajout d’une colonne dans la table demandes</span><span class="sxs-lookup"><span data-stu-id="41217-295">Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="41217-296">Ajouter des colonnes personnalisées</span><span class="sxs-lookup"><span data-stu-id="41217-296">Add custom columns</span></span>  

<span data-ttu-id="41217-297">Pour ajouter une colonne personnalisée dans la table demandes, positionnez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez les **en-têtes de réponse**  >  **gérer les colonnes d’en-tête**.</span><span class="sxs-lookup"><span data-stu-id="41217-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="41217-299">Ajout d’une colonne personnalisée dans la table demandes</span><span class="sxs-lookup"><span data-stu-id="41217-299">Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-300">Afficher la relation de synchronisation des requêtes</span><span class="sxs-lookup"><span data-stu-id="41217-300">View the timing relationship of requests</span></span>  

<span data-ttu-id="41217-301">Utilisez la cascade pour afficher les relations de minutage des requêtes.</span><span class="sxs-lookup"><span data-stu-id="41217-301">Use the Waterfall to view the timing relationships of requests.</span></span>  
<span data-ttu-id="41217-302">L’organisation par défaut de la cascade utilise l’heure de début des requêtes.</span><span class="sxs-lookup"><span data-stu-id="41217-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="41217-303">Par conséquent, les demandes qui sont plus éloignées du volet gauche sont restées plus anciennes que celles qui sont plus éloignées.</span><span class="sxs-lookup"><span data-stu-id="41217-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="41217-304">Pour passer en revue les différentes façons dont vous pouvez trier les cascade, sélectionnez [Trier par phase d’activité](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="41217-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="41217-306">Colonne cascade du volet **demandes**</span><span class="sxs-lookup"><span data-stu-id="41217-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection, use the following steps.  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="Panneau réseau" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="41217-307">Afficher un aperçu d’un corps de réponse</span><span class="sxs-lookup"><span data-stu-id="41217-307">View a preview of a response body</span></span>  

<span data-ttu-id="41217-308">Pour afficher un aperçu du corps de la réponse, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-308">To view a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-309">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-309">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="41217-310">Sélectionnez l’onglet **Aperçu** .</span><span class="sxs-lookup"><span data-stu-id="41217-310">Select the **Preview** tab.</span></span>  

<span data-ttu-id="41217-311">Cet onglet est principalement utile pour afficher des images.</span><span class="sxs-lookup"><span data-stu-id="41217-311">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="41217-313">Onglet **Aperçu**</span><span class="sxs-lookup"><span data-stu-id="41217-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-314">Afficher le corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="41217-314">View a response body</span></span>  

<span data-ttu-id="41217-315">Pour afficher le corps de la réponse d’une demande, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-315">To view the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-316">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-316">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="41217-317">Sélectionnez l’onglet **réponse** .</span><span class="sxs-lookup"><span data-stu-id="41217-317">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="41217-319">Onglet **réponse**</span><span class="sxs-lookup"><span data-stu-id="41217-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-320">Afficher les en-têtes HTTP</span><span class="sxs-lookup"><span data-stu-id="41217-320">View HTTP headers</span></span>  

<span data-ttu-id="41217-321">Pour afficher les données d’en-tête HTTP relatives à une requête, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-321">To view HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-322">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-322">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="41217-323">Sélectionnez l’onglet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="41217-323">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Panneau réseau" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="41217-325">Onglet **en-têtes**</span><span class="sxs-lookup"><span data-stu-id="41217-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="41217-326">Afficher une source d’en-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="41217-326">View HTTP header source</span></span>  

<span data-ttu-id="41217-327">Par défaut, l’onglet en-têtes affiche les noms des en-têtes par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="41217-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="41217-328">Pour afficher les noms d’en-tête HTTP dans l’ordre de réception, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-328">To view the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-329">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="41217-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="41217-330">Pour plus d’informations, accédez à la [section afficher les en-têtes http](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="41217-330">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="41217-331">Sélectionnez **afficher la source**, en regard de la section en **-tête de requête** ou **en-tête de réponse** .</span><span class="sxs-lookup"><span data-stu-id="41217-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="41217-332">Afficher les paramètres de chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="41217-332">View query string parameters</span></span>  

<span data-ttu-id="41217-333">Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’utilisateur, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-333">To view the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-334">Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="41217-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="41217-335">Pour plus d’informations, accédez à la [section afficher les en-têtes http](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="41217-335">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="41217-336">Accédez à la section **paramètres de chaîne de requête** .</span><span class="sxs-lookup"><span data-stu-id="41217-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="41217-338">Section **paramètres de chaîne de requête**</span><span class="sxs-lookup"><span data-stu-id="41217-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="41217-339">Afficher les paramètres de chaîne de requête source</span><span class="sxs-lookup"><span data-stu-id="41217-339">View query string parameters source</span></span>  

<span data-ttu-id="41217-340">Pour afficher la source du paramètre de chaîne de requête d’une demande, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-340">To view the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-341">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="41217-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="41217-342">Pour plus d’informations, accédez à [afficher les paramètres de chaîne de requête](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="41217-342">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="41217-343">Sélectionnez **afficher la source**.</span><span class="sxs-lookup"><span data-stu-id="41217-343">Choose **view source**.</span></span>  

#### <span data-ttu-id="41217-344">Afficher les paramètres de chaîne de requête codés en URL</span><span class="sxs-lookup"><span data-stu-id="41217-344">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="41217-345">Pour afficher les paramètres de chaîne de requête dans un format lisible par l’utilisateur, mais avec les codages prédéfinis, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-345">To view query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-346">Accédez à la section paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="41217-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="41217-347">Pour plus d’informations, accédez à [afficher les paramètres de chaîne de requête](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="41217-347">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="41217-348">Choisissez **affichage URL encodée**.</span><span class="sxs-lookup"><span data-stu-id="41217-348">Choose **view URL encoded**.</span></span>  

### <span data-ttu-id="41217-349">Afficher les cookies</span><span class="sxs-lookup"><span data-stu-id="41217-349">View cookies</span></span>  

<span data-ttu-id="41217-350">Pour afficher les cookies envoyés dans l’en-tête HTTP d’une requête, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-350">To view the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-351">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-351">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="41217-352">Sélectionnez l’onglet **cookies** .</span><span class="sxs-lookup"><span data-stu-id="41217-352">Select the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="41217-354">Onglet cookies</span><span class="sxs-lookup"><span data-stu-id="41217-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-355">Afficher la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="41217-355">View the timing breakdown of a request</span></span>  

<span data-ttu-id="41217-356">Pour afficher la répartition du minutage d’une demande, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-356">To view the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="41217-357">Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-357">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="41217-358">Sélectionnez l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="41217-358">Select the **Timing** tab.</span></span>  

<span data-ttu-id="41217-359">Pour accéder aux données plus rapidement, accédez à aperçu d' [une répartition du minutage](#preview-a-timing-breakdown).</span><span class="sxs-lookup"><span data-stu-id="41217-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="41217-360">Pour plus d’informations sur les différentes phases qui s’affichent dans l’onglet **minutage** , accédez à la [rubrique étapes de répartition du temps](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="41217-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="41217-362">Onglet **minutage**</span><span class="sxs-lookup"><span data-stu-id="41217-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="41217-363">Plus d’informations sur chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="41217-363">More information about each of the phases.</span></span>  

<span data-ttu-id="41217-364">Pour plus d’informations sur l’accès à la vue, accédez à la [section répartition du minutage](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="41217-364">For more information about accessing the view, navigate to [View timing breakdown](#view-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="41217-365">Prévisualiser une répartition de minutage</span><span class="sxs-lookup"><span data-stu-id="41217-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="41217-366">Pour afficher un aperçu de la répartition du minutage d’une requête, dans la colonne en **cascade** de la table demandes, pointez sur l’entrée de la requête.</span><span class="sxs-lookup"><span data-stu-id="41217-366">To view a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="41217-367">Pour plus d’informations sur l’accès aux données sans basculement, accédez à [afficher la répartition du minutage d’une demande](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="41217-367">For more information about how to access the data without hovering, navigate to [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="41217-369">Prévisualisation de la répartition du minutage d’une requête</span><span class="sxs-lookup"><span data-stu-id="41217-369">Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="41217-370">Explication des phases de répartition du temps</span><span class="sxs-lookup"><span data-stu-id="41217-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="41217-371">Plus d’informations sur chacune des phases qui s’affichent dans l’onglet **minutage** .</span><span class="sxs-lookup"><span data-stu-id="41217-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-372">Mise en file d’attente</span><span class="sxs-lookup"><span data-stu-id="41217-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-373">Le navigateur met en file d’attente les demandes lorsque l’une des conditions suivantes est vraie.</span><span class="sxs-lookup"><span data-stu-id="41217-373">The browser queues requests when any of the following are true.</span></span>  
      *   <span data-ttu-id="41217-374">Il existe des demandes de priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="41217-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="41217-375">Six connexions TCP sont ouvertes pour la même origine, qui correspond à la limite.</span><span class="sxs-lookup"><span data-stu-id="41217-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="41217-376">S’applique uniquement aux protocoles HTTP/1.0 et HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="41217-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="41217-377">Le navigateur alloue de l’espace dans le cache disque.</span><span class="sxs-lookup"><span data-stu-id="41217-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-378">Bloquée</span><span class="sxs-lookup"><span data-stu-id="41217-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-379">La requête est bloquée pour l’une des raisons décrites dans la **file d’attente**.</span><span class="sxs-lookup"><span data-stu-id="41217-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-380">Recherche DNS</span><span class="sxs-lookup"><span data-stu-id="41217-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-381">Le navigateur résout l’adresse IP pour la requête.</span><span class="sxs-lookup"><span data-stu-id="41217-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-382">Connexion initiale</span><span class="sxs-lookup"><span data-stu-id="41217-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-383">Le navigateur établit une connexion, y compris les négociations TCP, les tentatives de TCP et négocie une couche de socket sécurisée.</span><span class="sxs-lookup"><span data-stu-id="41217-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-384">Négociation de proxy</span><span class="sxs-lookup"><span data-stu-id="41217-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-385">Le navigateur négocie la requête avec un [serveur proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="41217-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-386">Demande envoyée</span><span class="sxs-lookup"><span data-stu-id="41217-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-387">La requête est en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="41217-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-388">Préparation de ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="41217-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-389">Le navigateur démarre le travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="41217-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-390">Demander à ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="41217-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-391">La demande est envoyée au travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="41217-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-392">En attente \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="41217-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-393">Le navigateur attend le premier octet d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="41217-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="41217-394">TTFB représente le temps à l’octet initial.</span><span class="sxs-lookup"><span data-stu-id="41217-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="41217-395">Ce minutage inclut un aller-retour d’une latence et la durée du serveur pour préparer la réponse.</span><span class="sxs-lookup"><span data-stu-id="41217-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-396">Téléchargement du contenu</span><span class="sxs-lookup"><span data-stu-id="41217-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-397">Le navigateur reçoit la réponse.</span><span class="sxs-lookup"><span data-stu-id="41217-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-398">Réception d’une émission</span><span class="sxs-lookup"><span data-stu-id="41217-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-399">Le navigateur reçoit des données pour cette réponse via le protocole HTTP/2 Server Poussée.</span><span class="sxs-lookup"><span data-stu-id="41217-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-400">Lecture Poussée</span><span class="sxs-lookup"><span data-stu-id="41217-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-401">Le navigateur lit les données locales précédemment reçues.</span><span class="sxs-lookup"><span data-stu-id="41217-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="41217-402">Afficher les initiateurs et les dépendances</span><span class="sxs-lookup"><span data-stu-id="41217-402">View initiators and dependencies</span></span>  

<span data-ttu-id="41217-403">Pour afficher les initiateurs et les dépendances d’une requête, maintenez la touche enfoncée `Shift` et placez le pointeur sur la requête dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-403">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="41217-404">Couleurs de DevTools: les initiateurs apparaissent en vert et les dépendances apparaissent en rouge.</span><span class="sxs-lookup"><span data-stu-id="41217-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="41217-406">Affichage des déclencheurs et des dépendances d’une requête</span><span class="sxs-lookup"><span data-stu-id="41217-406">Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="41217-407">Lorsque la table requêtes est classée dans l’ordre chronologique, si vous pointez sur une ligne, la ligne qui la précède affiche une requête verte.</span><span class="sxs-lookup"><span data-stu-id="41217-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="41217-408">La requête Green est l’initiateur de la dépendance.</span><span class="sxs-lookup"><span data-stu-id="41217-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="41217-409">Si une autre demande verte apparaît sur la ligne avant celle-ci, il s’agit de l’initiateur de l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="41217-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="41217-410">Et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="41217-410">And so on.</span></span>  

### <span data-ttu-id="41217-411">Afficher les événements de chargement</span><span class="sxs-lookup"><span data-stu-id="41217-411">View load events</span></span>  

<span data-ttu-id="41217-412">DevTools affiche le minutage des `DOMContentLoaded` événements et `load` dans plusieurs emplacements du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="41217-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="41217-413">L' `DOMContentLoaded` événement est coloré en bleu et l' `load` événement est rouge.</span><span class="sxs-lookup"><span data-stu-id="41217-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="41217-415">Emplacement des `DOMContentLoaded` `load` événements et dans le volet réseau</span><span class="sxs-lookup"><span data-stu-id="41217-415">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-416">Afficher le nombre total de demandes</span><span class="sxs-lookup"><span data-stu-id="41217-416">View the total number of requests</span></span>  

<span data-ttu-id="41217-417">Le nombre total de demandes est répertorié dans le volet Résumé, au bas du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="41217-417">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="41217-418">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="41217-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="41217-419">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="41217-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="41217-421">Nombre total de demandes depuis l’ouverture de DevTools</span><span class="sxs-lookup"><span data-stu-id="41217-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-422">Affichez la taille totale du téléchargement</span><span class="sxs-lookup"><span data-stu-id="41217-422">View the total download size</span></span>  

<span data-ttu-id="41217-423">La taille de téléchargement totale des demandes figure dans le volet Résumé, en bas du volet réseau.</span><span class="sxs-lookup"><span data-stu-id="41217-423">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="41217-424">Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.</span><span class="sxs-lookup"><span data-stu-id="41217-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="41217-425">Si d’autres requêtes s’est produites avant l’ouverture de DevTools, les requêtes précédentes ne sont pas comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="41217-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="41217-427">La taille de téléchargement totale des requêtes</span><span class="sxs-lookup"><span data-stu-id="41217-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="41217-428">Pour vérifier le nombre de ressources disponibles lorsque le navigateur décompresse chaque élément, naviguez jusqu’à [afficher la taille de la ressource](#view-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="41217-428">To verify how large resources are after the browser uncompresses each item, navigate to [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="41217-429">Afficher la trace de pile ayant entraîné une requête</span><span class="sxs-lookup"><span data-stu-id="41217-429">View the stack trace that caused a request</span></span>  

<span data-ttu-id="41217-430">Après qu’une instruction JavaScript demande une ressource, placez le pointeur sur la colonne **Initiator** pour afficher la trace de pile qui se trouve au début de la requête.</span><span class="sxs-lookup"><span data-stu-id="41217-430">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="41217-432">Trace de pile aboutissant à une demande de ressources</span><span class="sxs-lookup"><span data-stu-id="41217-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-433">Affichage de la taille de la ressource non compressée</span><span class="sxs-lookup"><span data-stu-id="41217-433">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="41217-434">Activez la case à cocher **utiliser des lignes de requête volumineuses** , puis examinez la valeur inférieure de la colonne **taille** .</span><span class="sxs-lookup"><span data-stu-id="41217-434">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="41217-436">Voici un exemple de ressources non compressées \ (la taille du `jquery-3.3.1.min.js` fichier qui a été envoyée par le biais du réseau était `29.9 KB` alors la taille du fichier non compressé `84.9 KB` ).</span><span class="sxs-lookup"><span data-stu-id="41217-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="41217-437">Exporter les données de requête</span><span class="sxs-lookup"><span data-stu-id="41217-437">Export requests data</span></span>  

### <span data-ttu-id="41217-438">Enregistrer toutes les demandes réseau dans un fichier QAR</span><span class="sxs-lookup"><span data-stu-id="41217-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="41217-439">Pour enregistrer toutes les demandes réseau dans un fichier QAR, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="41217-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="41217-440">Positionnez le pointeur sur une requête dans la table demandes et ouvrez le menu contextuel, puis cliquez sur le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="41217-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="41217-441">Choisissez **enregistrer en tant que le contenu**.</span><span class="sxs-lookup"><span data-stu-id="41217-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="41217-442">DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="41217-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="41217-443">Vous ne pouvez pas filtrer les demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-443">You are not able to filter requests.</span></span>  <span data-ttu-id="41217-444">Vous ne pouvez pas non plus enregistrer une demande unique.</span><span class="sxs-lookup"><span data-stu-id="41217-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="41217-445">Lorsque vous enregistrez un fichier QAR, vous pouvez l’importer de nouveau dans DevTools pour analyse.</span><span class="sxs-lookup"><span data-stu-id="41217-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="41217-446">Il suffit de glisser-déplacer le fichier QAR dans la table demandes.</span><span class="sxs-lookup"><span data-stu-id="41217-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="41217-448">Sélection **de l’option Enregistrer sous le contenu de votre fichier**</span><span class="sxs-lookup"><span data-stu-id="41217-448">Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-449">Copier une ou plusieurs demandes dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="41217-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="41217-450">Dans la colonne **nom** de la table demandes, positionnez le pointeur sur une requête, ouvrez le menu contextuel **, puis**sélectionnez l’une des options suivantes...</span><span class="sxs-lookup"><span data-stu-id="41217-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-451">Copier l’adresse du lien</span><span class="sxs-lookup"><span data-stu-id="41217-451">Copy Link Address</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-452">Copiez l’URL de la requête dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="41217-452">Copy the URL of the request to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-453">Copier la réponse</span><span class="sxs-lookup"><span data-stu-id="41217-453">Copy Response</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-454">Copiez le corps de la réponse dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="41217-454">Copy the response body to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-455">Copier en tant qu’extraction</span><span class="sxs-lookup"><span data-stu-id="41217-455">Copy as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-456">Copier sous forme de courbe</span><span class="sxs-lookup"><span data-stu-id="41217-456">Copy as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-457">Copiez la demande en tant que commande en forme de boucle.</span><span class="sxs-lookup"><span data-stu-id="41217-457">Copy the request as a cURL command.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-458">Copy All As Fetch</span><span class="sxs-lookup"><span data-stu-id="41217-458">Copy All as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-459">Tout copier comme courbe</span><span class="sxs-lookup"><span data-stu-id="41217-459">Copy All as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-460">Copiez toutes les demandes comme une chaîne de commandes bouclé.</span><span class="sxs-lookup"><span data-stu-id="41217-460">Copy all requests as a chain of cURL commands.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="41217-461">Tout copier comme.</span><span class="sxs-lookup"><span data-stu-id="41217-461">Copy All as HAR</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="41217-462">Copiez toutes les demandes en tant que données QAR.</span><span class="sxs-lookup"><span data-stu-id="41217-462">Copy all requests as HAR data.</span></span>  
   :::column-end:::
:::row-end:::  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="41217-464">Sélection de l’option **copier la réponse**</span><span class="sxs-lookup"><span data-stu-id="41217-464">Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="41217-465">Modifier la disposition du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="41217-465">Change the layout of the Network panel</span></span>  

<span data-ttu-id="41217-466">Vous pouvez développer ou réduire des sections de l’interface utilisateur du panneau réseau pour cibler les informations importantes.</span><span class="sxs-lookup"><span data-stu-id="41217-466">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="41217-467">Masquer le volet filtres</span><span class="sxs-lookup"><span data-stu-id="41217-467">Hide the Filters pane</span></span>  

<span data-ttu-id="41217-468">Par défaut, DevTools affiche le **volet filtres**.</span><span class="sxs-lookup"><span data-stu-id="41217-468">By default, DevTools show the **Filters pane**.</span></span>  
<span data-ttu-id="41217-469">Choisissez **filtre** \ ( ![ filtre ][ImageFilterIcon] \) pour le masquer.</span><span class="sxs-lookup"><span data-stu-id="41217-469">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="41217-471">Bouton Masquer les filtres</span><span class="sxs-lookup"><span data-stu-id="41217-471">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-472">Utiliser des lignes de requête volumineuses</span><span class="sxs-lookup"><span data-stu-id="41217-472">Use large request rows</span></span>  

<span data-ttu-id="41217-473">Utilisez des lignes de grande taille si vous voulez plus d’espace dans votre tableau de requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="41217-473">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="41217-474">Certaines colonnes fournissent également quelques informations supplémentaires sur l’utilisation de lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="41217-474">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="41217-475">Par exemple, la valeur la plus en bas de la colonne **taille** correspond à la taille de requête non compressée.</span><span class="sxs-lookup"><span data-stu-id="41217-475">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="41217-477">Exemple de longues lignes de requête dans le volet **requêtes**</span><span class="sxs-lookup"><span data-stu-id="41217-477">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="41217-478">Activez la case à cocher **utiliser des lignes de requête volumineuses** pour activer les lignes de grande taille.</span><span class="sxs-lookup"><span data-stu-id="41217-478">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="41217-480">Case à cocher **utiliser de grandes lignes de requête**</span><span class="sxs-lookup"><span data-stu-id="41217-480">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="41217-481">Masquer le volet vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="41217-481">Hide the Overview pane</span></span>  

<span data-ttu-id="41217-482">Par défaut, DevTools affiche le **volet vue d’ensemble**.</span><span class="sxs-lookup"><span data-stu-id="41217-482">By default, DevTools show the **Overview pane**.</span></span>  <span data-ttu-id="41217-483">Désélectionnez la case à cocher **afficher la vue d’ensemble** pour la masquer.</span><span class="sxs-lookup"><span data-stu-id="41217-483">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="41217-485">Case à cocher **afficher la vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="41217-485">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="41217-486">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="41217-486">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Déboguer des applications Web progressives | Documents Microsoft"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL de données | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Serveur proxy-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="41217-490">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="41217-490">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="41217-491">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="41217-491">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="41217-493">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="41217-493">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
