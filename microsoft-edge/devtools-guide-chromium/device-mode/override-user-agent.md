---
description: Ouvrez l’onglet conditions du réseau, désactivez l’option sélectionner automatiquement, puis choisissez dans la liste ou entrez une chaîne personnalisée.
title: Remplacement de la chaîne de l’agent utilisateur à partir de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: befbe186a5992c651f877a18f1c3232bf212394a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124949"
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

# <span data-ttu-id="f2a86-104">Remplacement de la chaîne de l’agent utilisateur à partir de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f2a86-104">Override the user agent string from Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f2a86-105">Pour remplacer la chaîne de l' [agent utilisateur][MDNUserAgent] à partir de Microsoft Edge devtools:</span><span class="sxs-lookup"><span data-stu-id="f2a86-105">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="f2a86-106">Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="f2a86-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="f2a86-108">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="f2a86-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2a86-109">Tapez `network conditions` , choisissez **afficher les conditions du réseau**, puis cliquez `Enter` sur l’onglet **conditions réseau** pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f2a86-109">Type `network conditions`, choose **Show Network conditions**, and select `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="f2a86-110">Dans la section **agent utilisateur** , désactivez la case à cocher **sélectionner automatiquement** .</span><span class="sxs-lookup"><span data-stu-id="f2a86-110">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       <span data-ttu-id="f2a86-112">Désactiver l' **option sélectionner automatiquement**</span><span class="sxs-lookup"><span data-stu-id="f2a86-112">Disable **Select automatically**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2a86-113">Sélectionnez une chaîne d’agent utilisateur dans la liste ou entrez votre propre chaîne personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f2a86-113">Select a user agent string from the list, or enter your own custom string.</span></span>  
    
## <span data-ttu-id="f2a86-114">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f2a86-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  

> [!NOTE]
> <span data-ttu-id="f2a86-116">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f2a86-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f2a86-117">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="f2a86-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="f2a86-119">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f2a86-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
