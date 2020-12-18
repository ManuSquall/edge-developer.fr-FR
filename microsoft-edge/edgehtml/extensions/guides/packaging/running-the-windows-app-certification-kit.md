---
description: En savoir plus sur le kit de certification des applications Windows. Cela donne à votre extension une meilleure chance de parvenir à la publication.
title: Extensions-exécution du kit de certification des applications Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b8ca9117e3d35c01a0fbd2ec4defe38180b773cd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233370"
---
# <span data-ttu-id="c005d-105">Exécution du Kit de certification des applications Windows</span><span class="sxs-lookup"><span data-stu-id="c005d-105">Running the Windows App Certification Kit</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="c005d-106">Pour améliorer les chances que votre extension soit publiée sur le Microsoft Store, vous devez installer et exécuter le kit de [certification des applications Windows](https://go.microsoft.com/fwlink/p/?LinkID=309666).</span><span class="sxs-lookup"><span data-stu-id="c005d-106">To improve the chances of your extension getting published to the Microsoft Store, you'll need to install and run the [Windows App Certification Kit](https://go.microsoft.com/fwlink/p/?LinkID=309666).</span></span>
<span data-ttu-id="c005d-107">Ce processus exécute une [série de tests](https://docs.microsoft.com/windows/uwp/debug-test-perf/windows-app-certification-kit-tests) sur votre package d’extension pour vérifier qu’il est prêt pour le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="c005d-107">This runs a [series of tests](https://docs.microsoft.com/windows/uwp/debug-test-perf/windows-app-certification-kit-tests) on your extension package to ensure that it's ready for the Microsoft Store.</span></span>

> [!NOTE]
> <span data-ttu-id="c005d-108">Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="c005d-108">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="c005d-109">Une fois que vous avez créé, emballé et testé votre poste, envoyez une demande sur notre [formulaire de soumission d’extension](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="c005d-109">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>

<span data-ttu-id="c005d-110">Avant d’apprendre à utiliser le kit, assurez-vous que vous remplissez les conditions préalables suivantes:</span><span class="sxs-lookup"><span data-stu-id="c005d-110">Before learning about how to use the kit, make sure you meet the following prerequisites:</span></span> 

- <span data-ttu-id="c005d-111">Vous devez installer et exécuter Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c005d-111">You must install and run Windows 10.</span></span>
- <span data-ttu-id="c005d-112">Vous devez installer le [Kit de certification des applications Windows version10](https://go.microsoft.com/fwlink/p/?LinkID=309666), qui est inclus dans le Kit de développement logiciel (SDK) Windows pour Windows10.</span><span class="sxs-lookup"><span data-stu-id="c005d-112">You must install [Windows App Certification Kit version 10](https://go.microsoft.com/fwlink/p/?LinkID=309666), which is included in the Windows Software Development Kit (SDK) for Windows 10.</span></span>
- <span data-ttu-id="c005d-113">Vous devez [activer votre appareil pour le développement](https://docs.microsoft.com/windows/uwp/get-started/enable-your-device-for-development).</span><span class="sxs-lookup"><span data-stu-id="c005d-113">You must [enable your device for development](https://docs.microsoft.com/windows/uwp/get-started/enable-your-device-for-development).</span></span>
- <span data-ttu-id="c005d-114">Vous devez avoir une extension [empaquetée](../packaging.md) .</span><span class="sxs-lookup"><span data-stu-id="c005d-114">You must have a [packaged](../packaging.md) extension.</span></span>


<span data-ttu-id="c005d-115">Si vous répondez à la configuration requise, reportez-vous à la documentation du [Kit de certification des applications Windows](https://docs.microsoft.com/windows/uwp/debug-test-perf/windows-app-certification-kit#validate-your-windows-app-using-the-windows-app-certification-kit-interactively) pour plus d’informations sur l’utilisation du kit de certification des applications Windows de manière interactive ou à l’aide de la ligne de commande pour tester votre extension.</span><span class="sxs-lookup"><span data-stu-id="c005d-115">If you meet the prerequisites, see the [Windows App Certification Kit](https://docs.microsoft.com/windows/uwp/debug-test-perf/windows-app-certification-kit#validate-your-windows-app-using-the-windows-app-certification-kit-interactively) documentation for info on how to use the Windows App Certification Kit either interactively or with the command line to test your extension.</span></span>
