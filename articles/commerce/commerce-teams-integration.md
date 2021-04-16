---
title: Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats
description: Šajā tēmā sniegts Microsoft Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b7872757815d4eec0393e8b1c8c6ff5467e9473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842702"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="c66da-103">Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="c66da-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c66da-104">Šajā tēmā sniegts Microsoft Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats.</span><span class="sxs-lookup"><span data-stu-id="c66da-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="c66da-105">Dynamics 365 Commerce ir integrēšana ar Teams, lai palīdzētu klientiem un viņu darbiniekiem uzlabot produktivitāti, sinhronizējot uzdevumu pārvaldību starp divām programmām.</span><span class="sxs-lookup"><span data-stu-id="c66da-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="c66da-106">Efektīvi uzdevumu pārvaldība, ko Commerce and Teams integrācija nodrošina veikalu vadītājiem un darbiniekiem izveidot uzdevumu sarakstus, piešķirt uzdevumus vairākiem veikaliem un izsekot uzdevumu statusu veikalos no jebkura programmas.</span><span class="sxs-lookup"><span data-stu-id="c66da-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="c66da-107">Commerce and Teams integrācija ir pieejama Commerce versijā 10.0.18 laidienā.</span><span class="sxs-lookup"><span data-stu-id="c66da-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="c66da-108">Galvenie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="c66da-108">Key features</span></span>

<span data-ttu-id="c66da-109">Šeit ir dažas galvenās funkcijas, ko nodrošina Commerce un Microsoft Teams integrācija:</span><span class="sxs-lookup"><span data-stu-id="c66da-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="c66da-110">Nodrošināt brigādes, izmantojot labi definētas informācijas priekšrocības no Commerce, piemēram, organizācijas struktūru un informāciju par veikaliem, darbiniekiem, atļaujām un biznesa kontekstu.</span><span class="sxs-lookup"><span data-stu-id="c66da-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="c66da-111">Ērti sinhronizējiet notiekošās izmaiņas (piemēram, jaunu veikalu pievienošana vai jaunu darbinieku nolīgšana) starp Commerce un Teams, bet paturēt Commerce kā galveno organizācijas struktūras datu avotu.</span><span class="sxs-lookup"><span data-stu-id="c66da-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="c66da-112">Integrējiet uzdevumu pārvaldību starp Commerce un Teams, lai palīdzētu uzglabāt darbiniekus, veikalu vadītājus, reģionālos vadītājus un saziņas vadītājus, vadīt uzdevumu pārvaldību no jebkuras lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="c66da-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="c66da-113">Integrācijas līdzekļu lietošanas priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="c66da-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="c66da-114">Pirms varat sākt izmantot Microsoft Teams integrācijas līdzekļus, jābūt šādiem priekšnosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="c66da-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="c66da-115">Microsoft 365 Business Standard licence (šī licence ietver Teams.)</span><span class="sxs-lookup"><span data-stu-id="c66da-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="c66da-116">Azure Active Directory (Azure AD) konti visiem veikala vadītājiem un darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="c66da-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="c66da-117">Pārdošanas punkta (POS) sistēmas, kas ir konfigurētas ar Azure AD autentifikāciju</span><span class="sxs-lookup"><span data-stu-id="c66da-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="c66da-118">Konceptuāla arhitektūra</span><span class="sxs-lookup"><span data-stu-id="c66da-118">Conceptual architecture</span></span>

<span data-ttu-id="c66da-119">Šajā attēlā redzama Dynamics 365 Commerce un Microsoft Teams konceptuālā arhitektūra un integrācija, izmantojot Sanfrancisko veikalu kā piemēru.</span><span class="sxs-lookup"><span data-stu-id="c66da-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="c66da-120">Gan brigādes, gan Commerce POS programma izmanto Microsoft Planner kā repozitoriju, lai no Teams publicētie uzdevumi tiktu parādīti POS programmā, un veikala programmas ekspromta uzdevumos, kas izveidoti POS programmā, tiek parādīti Teams, kā rezultātā ir viengabala uzdevumu pārvaldības pieredze starp programmām.</span><span class="sxs-lookup"><span data-stu-id="c66da-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Commerce un Teams integrācijas arhitektūra](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="c66da-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c66da-122">Additional resources</span></span>

[<span data-ttu-id="c66da-123">Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju</span><span class="sxs-lookup"><span data-stu-id="c66da-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="c66da-124">Nodrošināt Microsoft Teams no Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c66da-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="c66da-125">Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="c66da-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="c66da-126">Lietotāju lomu pārvaldība Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c66da-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="c66da-127">Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c66da-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="c66da-128">Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ</span><span class="sxs-lookup"><span data-stu-id="c66da-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
