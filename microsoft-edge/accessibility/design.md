---
description: Accédez à des ressources pour accéder à des outils de conception inclusive et des meilleures pratiques.
title: Accessibilité-conception
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 8468f8e1-9f4a-426c-a969-76eab9419137
keywords: accessibilité, accessibilité pour les développeurs, sites Web accessibles, Edge, développement Web, ARIA, développeur, UIA, UI Automation
ms.openlocfilehash: 8d31f7b32cb92794ff8592c239436f3b101a3859
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230816"
---
# <span data-ttu-id="a65aa-104">Conception de sites Web accessibles</span><span class="sxs-lookup"><span data-stu-id="a65aa-104">Designing Accessible Websites</span></span>  

<span data-ttu-id="a65aa-105">La création d’une conception inclusive rend la technologie exploitable par tous les utilisateurs, quels que soient leur âge, leur éducation, leur emplacement géographique, leur langue ou leur handicap.</span><span class="sxs-lookup"><span data-stu-id="a65aa-105">Creating an inclusive design makes technology usable by all people no matter their age, education, geographic location, language, or disability.</span></span>  <span data-ttu-id="a65aa-106">Les personnes qui utilisent une technologie et naviguez sur le Web disposent d’une vaste gamme de capacités et de préférences.</span><span class="sxs-lookup"><span data-stu-id="a65aa-106">People using technology and browsing the web have a wide range of abilities and preferences.</span></span>  <span data-ttu-id="a65aa-107">Lors de la conception de votre site Web, gardez à l’esprit les scénarios d’accessibilité clés suivants:</span><span class="sxs-lookup"><span data-stu-id="a65aa-107">As you design your website, keep in mind the following key accessibility scenarios:</span></span>

*   <span data-ttu-id="a65aa-108">Lecteurs d’écran: les utilisateurs aveugles ou malvoyants se fient sur les lecteurs d’écran pour interpréter l’interface utilisateur de votre application et interagir avec celle-ci.</span><span class="sxs-lookup"><span data-stu-id="a65aa-108">Screen readers—Users who are blind or visually impaired rely on screen readers to interpret and interact with the UI of your app.</span></span>  <span data-ttu-id="a65aa-109">L’interprétation consiste à lire les noms des éléments de l’interface utilisateur, les rôles, les valeurs, etc., et à interagir avec l’interface utilisateur, en passant le focus d’un élément à l’autre et en appelant les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="a65aa-109">Interpreting involves reading the UI element names, roles, values, and so on, and interacting with the UI involves moving the focus from one element to another and invoking functionality.</span></span>
*   <span data-ttu-id="a65aa-110">Accessibilité du clavier: de nombreux utilisateurs d’accessibilité reposent sur le clavier pour naviguer et utiliser l’interface utilisateur en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="a65aa-110">Keyboard accessibility—Many accessibility users rely on the keyboard to navigate and operate the UI by:</span></span>
    *   <span data-ttu-id="a65aa-111">Déplacer le focus entre les éléments à l’aide de la touche Tab.</span><span class="sxs-lookup"><span data-stu-id="a65aa-111">Moving focus among elements by using the Tab key.</span></span>
    *   <span data-ttu-id="a65aa-112">Navigation dans les éléments conteneurs tels que les listes, les grilles et les arborescences à l’aide des touches de direction.</span><span class="sxs-lookup"><span data-stu-id="a65aa-112">Navigating in container elements such as lists, grids, and tree views by using the arrow keys.</span></span>
    *   <span data-ttu-id="a65aa-113">Activation de la fonctionnalité \ (appel d’actions \) à l’aide de la touche entrée ou espace.</span><span class="sxs-lookup"><span data-stu-id="a65aa-113">Activating functionality \(invoking actions\) by using the Enter or Space key.</span></span>
    *   <span data-ttu-id="a65aa-114">Utilisation des touches de raccourci pour accéder efficacement aux autres fonctionnalités de l’application.</span><span class="sxs-lookup"><span data-stu-id="a65aa-114">Using shortcut keys to efficiently access other app functionality.</span></span>
*   <span data-ttu-id="a65aa-115">Accès visuel accessible: les utilisateurs malvoyants ont besoin d’un coefficient de contraste de texte suffisant pour le contenu du texte et d’une bonne interface visuelle avec les thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="a65aa-115">Accessible visual experience—Users who are visually impaired need a sufficient text contrast ratio for text content, and a good visual experience with high contrast themes overall.</span></span>  <span data-ttu-id="a65aa-116">Les utilisateurs qui utilisent des couleurs n’ont pas besoin d’être acheminés en couleur.</span><span class="sxs-lookup"><span data-stu-id="a65aa-116">Users who are color blind need information to be conveyed in ways other than through color.</span></span>

<span data-ttu-id="a65aa-117">De nombreux problèmes d’accessibilité courants sur le Web peuvent être résolus par le biais de bonnes pratiques de codage.</span><span class="sxs-lookup"><span data-stu-id="a65aa-117">Many common accessibility issues on the web can be solved through good coding practice.</span></span>  <span data-ttu-id="a65aa-118">La documentation [2,0 Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/TR/WCAG20) fournit des techniques et des meilleures pratiques pour vous aider à concevoir des applications Web dynamiques plus accessibles.</span><span class="sxs-lookup"><span data-stu-id="a65aa-118">The [Web Content Accessibility Guidelines (WCAG) 2.0](https://www.w3.org/TR/WCAG20) documentation provides techniques and best practices to help you design more accessible dynamic web applications.</span></span>  <span data-ttu-id="a65aa-119">Pour plus d’informations sur la création de sites Web accessibles, accédez à [créer des sites Web accessibles](./build/index.md) .</span><span class="sxs-lookup"><span data-stu-id="a65aa-119">For more information on building accessible websites, navigate to [Building Accessible Websites](./build/index.md) .</span></span>

## <span data-ttu-id="a65aa-120">Ressources</span><span class="sxs-lookup"><span data-stu-id="a65aa-120">Resources</span></span>  

#### [<span data-ttu-id="a65aa-121">Design pour inclusion</span><span class="sxs-lookup"><span data-stu-id="a65aa-121">Designing for Inclusion</span></span>](https://w3.org/WAI/users/Overview.html)  

<span data-ttu-id="a65aa-122">La conception pour une inclusion par l’initiative World Wide Accessibility du W3C fournit des ressources pour vous aider à mieux comprendre les utilisateurs souffrant d’un handicap et comment concevoir votre site Web à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="a65aa-122">Designing for Inclusion by the W3C Web Accessibility Initiative provides resources to help you better understand users with disabilities and how to design your website with them in mind.</span></span>

#### [<span data-ttu-id="a65aa-123">Conception de logiciels inclusifs</span><span class="sxs-lookup"><span data-stu-id="a65aa-123">Designing inclusive software</span></span>](https://msdn.microsoft.com/windows/uwp/accessibility/designing-inclusive-software)  

<span data-ttu-id="a65aa-124">La conception de logiciels inclusifs traite des principes de conception et des pratiques Microsoft pour la plateforme Windows universelle (UWP).</span><span class="sxs-lookup"><span data-stu-id="a65aa-124">Designing inclusive software discusses Microsoft design principles and practices for the Universal Windows Platform (UWP).</span></span>

#### [<span data-ttu-id="a65aa-125">Comment les personnes atteintes de handicaps utilisent le Web</span><span class="sxs-lookup"><span data-stu-id="a65aa-125">How People with Disabilities Use the Web</span></span>](https://www.w3.org/WAI/intro/people-use-web/Overview.html)  

<span data-ttu-id="a65aa-126">Cette ressource par le W3C présente la façon dont les personnes atteintes de handicaps, y compris les personnes souffrant de troubles de l’âge, utilisent le Web.</span><span class="sxs-lookup"><span data-stu-id="a65aa-126">This resource by the W3C introduces how people with disabilities, including people with age-related impairments, use the Web.</span></span>

#### [<span data-ttu-id="a65aa-127">Kit de conception inclusive</span><span class="sxs-lookup"><span data-stu-id="a65aa-127">Inclusive Design Toolkit</span></span>](https://www.microsoft.com/design/practice#howwemake-section)  

<span data-ttu-id="a65aa-128">Microsoft a développé le kit de développement logiciel (Design inclusive) pour montrer la façon dont la diversité humaine peut créer de meilleures contraintes de conception et la manière de se connecter à des solutions de niche d’aspect.</span><span class="sxs-lookup"><span data-stu-id="a65aa-128">Microsoft developed the Inclusive Design Toolkit to show how human diversity can create better design constraints and how to connect seemingly niche solutions to broader markets.</span></span>
