---
description: Exécute un script sérialisé. Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.
title: Fonction JsRunSerializedScriptWithCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ac9ac08357cd479f78e3500bc5eef151fb8e4e6c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233470"
---
# JsRunSerializedScriptWithCallback Function

Exécute un script sérialisé. Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### Paramètres  
 `scriptLoadCallback`  
 Rappel appelé lorsque le code source du script doit être chargé.  
  
 `scriptUnloadCallback`  
 Rappel appelé lorsque le script sérialisé et le code source ne sont plus nécessaires.  
  
 `buffer`  
 Script sérialisé.  
  
 `sourceContext`  
 Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.     Ce contexte est transmis à scriptLoadCallback et scriptUnloadCallback.  
  
 `sourceUrl`  
 Emplacement à partir duquel provient le script.  
  
 `result`  
 Résultat de l’exécution du script, le cas échéant. Ce paramètre peut être null.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
  
> [!NOTE]
>  Cette API n’est pas encore disponible pour les applications du Windows Store.  
  
 Nécessite un contexte de script actif.  
  
 Le runtime sera maintenu sur la mémoire tampon jusqu’à ce que toutes les instances de toutes les fonctions créées à partir de la mémoire tampon soient récupérées par le garbage collector.  Il appelle alors scriptUnloadCallback pour indiquer à l’appelant qu’il est en sécurité.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
