---
description: Découvrez comment afficher et modifier sessionStorage à l’aide du volet de stockage de session et de la console.
title: Afficher et modifier le stockage de session avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e31e45abc5eac26d297cd9bc9fca43778dd74300
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231194"
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

# Afficher et modifier le stockage de session avec Microsoft Edge DevTools  

Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des paires clé-valeur [sessionStorage][MDNSessionStorage] .  

## Afficher les clés et valeurs de sessionStorage  

1.  Sélectionnez l’onglet **application** pour ouvrir l’outil de l' **application** .  Le volet **manifeste** est affiché par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **manifeste**  
    :::image-end:::  
    
1.  Développez le menu stockage de la **session** .  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Menu de stockage de session" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       Menu de **stockage de session**  
    :::image-end:::  
    
1.  Sélectionnez un domaine pour afficher les paires clé-valeur.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Paires clé-valeur sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       `sessionStorage`Paires clé-valeur  
    :::image-end:::  
    
1.  Choisissez une ligne du tableau pour afficher la valeur de la visionneuse sous le tableau.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Afficher la valeur de la clé x-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Afficher la valeur de la `x-sid` clé  
    :::image-end:::  
    
## Créer une paire clé-valeur sessionStorage  

1.  [Affichez les paires clé-valeur sessionStorage d’un domaine](#view-sessionstorage-keys-and-values).  
1.  Double-cliquez sur la partie vide de la table.  DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur  
    :::image-end:::  
    
## Modifier les clés ou valeurs de sessionStorage  

1.  [Affichez les paires clé-valeur sessionStorage d’un domaine](#view-sessionstorage-keys-and-values).  
1.  Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Modifier une clé de sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Modifier une `sessionStorage` clé  
    :::image-end:::  
    
## Supprimer des paires clé-valeur sessionStorage  

1.  [Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).  
1.  Choisissez la paire clé-valeur que vous voulez supprimer.  DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.  
1.  Sélectionnez la `Delete` clé ou cliquez sur **supprimer** la sélection ![ ][ImageDeleteIcon] .  
    
## Suppression de toutes les paires clé-valeur sessionStorage pour un domaine  

1.  [Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).  
1.  Sélectionnez **Effacer tout** ( ![ Effacer tout ][ImageClearIcon] ).  
    
## Interagir avec sessionStorage à partir de la console  

Dans la mesure où vous pouvez exécuter JavaScript dans la **console**, et dans la mesure où la **console** a accès aux contextes JavaScript de la page, vous pouvez interagir avec celle-ci `sessionStorage` à partir de la **console**.  

1.  Utilisez le menu **contextes JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `sessionStorage` paires clé-valeur d’un domaine autre que celui de la page sur laquelle vous vous trouvez.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Changer le contexte JavaScript de la console" lightbox="../media/storage-console-domain-selection.msft.png":::
       Changer le contexte JavaScript de la **console**  
    :::image-end:::  
    
1.  Exécutez vos `sessionStorage` expressions dans la **console**, de la même manière que dans JavaScript.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interagir avec sessionStorage à partir de la console" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Interagir avec `sessionStorage` à partir de la **console**  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
