---
description: Analyse un script sérialisé et retourne une fonction qui représente le script. Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.
title: Fonction JsParseSerializedScriptWithCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b145f01a5c3459100d8402beae63b7cff55db7b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233302"
---
# JsParseSerializedScriptWithCallback Function

Analyse un script sérialisé et retourne une fonction qui représente le script. Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
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
 Fonction qui représente le code de script.  
  
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
