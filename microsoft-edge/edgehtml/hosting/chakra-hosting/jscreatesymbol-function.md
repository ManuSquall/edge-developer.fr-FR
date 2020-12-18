---
description: Crée un symbole JavaScript.
title: Fonction JsCreateSymbol | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a2f77f477aeebac150635d93cbd0cd043357256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233191"
---
# <span data-ttu-id="b7cac-103">JsCreateSymbol Function</span><span class="sxs-lookup"><span data-stu-id="b7cac-103">JsCreateSymbol Function</span></span>

<span data-ttu-id="b7cac-104">Crée un symbole JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b7cac-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="b7cac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7cac-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="b7cac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7cac-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="b7cac-107">Description de la chaîne du symbole.</span><span class="sxs-lookup"><span data-stu-id="b7cac-107">The string description of the symbol.</span></span> <span data-ttu-id="b7cac-108">Peut être null.</span><span class="sxs-lookup"><span data-stu-id="b7cac-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="b7cac-109">Le nouveau symbole.</span><span class="sxs-lookup"><span data-stu-id="b7cac-109">The new symbol.</span></span>  
  
## <span data-ttu-id="b7cac-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b7cac-110">Return Value</span></span>  
 <span data-ttu-id="b7cac-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b7cac-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b7cac-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7cac-112">Remarks</span></span>  
 <span data-ttu-id="b7cac-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="b7cac-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="b7cac-114">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b7cac-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="b7cac-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="b7cac-115">Requirements</span></span>  
 <span data-ttu-id="b7cac-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b7cac-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b7cac-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7cac-117">See Also</span></span>  
 [<span data-ttu-id="b7cac-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b7cac-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
