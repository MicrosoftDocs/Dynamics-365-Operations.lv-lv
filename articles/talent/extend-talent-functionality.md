---
title: "Microsoft Dynamics 365 for Talent funkcionalitātes paplašināšana"
description: "Ja esat izveidojis kādas Microsoft PowerApps programmas, šīs programmas varat palaist no saitēm programmatūrā Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: lv-lv
ms.lasthandoff: 03/08/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="07004-103">Microsoft Dynamics 365 for Talent funkcionalitātes paplašināšana</span><span class="sxs-lookup"><span data-stu-id="07004-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="07004-104">Ja esat izveidojis kādas Microsoft PowerApps programmas, šīs programmas varat palaist no saitēm programmatūrā Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="07004-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="07004-105">Lai iestatītu piekļuvi savām programmām, ir jāiestata noteikta informācija sadaļā Talent, kas atrodas konfigurācijas lapā, kuru varat atvērt no darbvietas **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="07004-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="07004-106">Iegulto PowerApps programmu konfigurēšana Talent ietvaros</span><span class="sxs-lookup"><span data-stu-id="07004-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="07004-107">Lai Talent lapas konfigurētu PowerApps programmu palaišanai, izmantojiet lapu **Iestatīt iegultas Microsoft PowerApps programmas**.</span><span class="sxs-lookup"><span data-stu-id="07004-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="07004-108">Lai atvērtu lapu **Iestatīt iegultas Microsoft PowerApps programmas**, atveriet darbvietu **Sistēmas administrēšana** un pēc tam atveriet cilni **Saites**. Grupā **Iestatīšana** atlasiet **Microsoft PowerApps**.</span><span class="sxs-lookup"><span data-stu-id="07004-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="07004-109">Šajā lapā tiek ievadīta vai iestatīta tālāk norādītā informācija.</span><span class="sxs-lookup"><span data-stu-id="07004-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="07004-110">Katras PowerApps programmas aprakstošs nosaukums vai identifikators.</span><span class="sxs-lookup"><span data-stu-id="07004-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="07004-111">Unikāls identifikators (GUID) katrai programmai, kuru pievienojat lapai Talent.</span><span class="sxs-lookup"><span data-stu-id="07004-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="07004-112">Šis programmas ID ir pieejams PowerApps vietnē [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="07004-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="07004-113">Lapa, no kuras lietotāji var atvērt kādu programmu vai pārskatu.</span><span class="sxs-lookup"><span data-stu-id="07004-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="07004-114">Ne visas Talent lapas atbalsta iegultās PowerApps programmas un Power BI pārskatus.</span><span class="sxs-lookup"><span data-stu-id="07004-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="07004-115">Ievadiet lapas iekšējo nosaukumu, nevis parādāmo nosaukumu, kurš ir redzams lapas augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="07004-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="07004-116">Lai atrastu iekšējo nosaukumu, atveriet lapu, kuras iekšējais nosaukums jums ir nepieciešams, un ar peles labo pogu noklikšķiniet jebkurā šīs lapas vietā.</span><span class="sxs-lookup"><span data-stu-id="07004-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="07004-117">Kad tiek atvērta izvēlne, virziet peles rādītāju virs vienuma **Formas informācija**.</span><span class="sxs-lookup"><span data-stu-id="07004-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="07004-118">Iekšējais formas nosaukums izvēlnē tiek rādīts blakus vienumam **Formas informācija**.</span><span class="sxs-lookup"><span data-stu-id="07004-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
> - <span data-ttu-id="07004-119">Norādiet formas vadīklu, no kuras programma var izgūt konteksta datus.</span><span class="sxs-lookup"><span data-stu-id="07004-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="07004-120">Piemēram, programma varētu izmantot datus par kādu nodarbināto.</span><span class="sxs-lookup"><span data-stu-id="07004-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="07004-121">Ja laukā **Konteksts** ievadāt lapu **Nodarbinātais**, startējot programmu, tiek atvērta lapa **Nodarbinātais**.</span><span class="sxs-lookup"><span data-stu-id="07004-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="07004-122">Ieraksts laukā **Konteksts** nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="07004-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="07004-123">Iestatiet lielumu dialoglodziņam, kurā darbosies PowerApps programmas.</span><span class="sxs-lookup"><span data-stu-id="07004-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="07004-124">Dialoglodziņa rūtiņas ir norādītas kā “mazs” vai “liels”, lai optimizētu lietotāja interfeisu, kad jūsu programma attiecīgi darbojas tālruni vai lielākā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="07004-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="07004-125">Varat arī norādīt, kurām juridiskajām personām programma būs pieejama, vai varat to padarīt pieejamu visām savām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="07004-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="07004-126">Pēc noklusējuma jūsu PowerApps programmas ir pieejamas visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="07004-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="07004-127">Programmas atvēršana</span><span class="sxs-lookup"><span data-stu-id="07004-127">Opening an application</span></span>
<span data-ttu-id="07004-128">Kad esat konfigurējis iegultās PowerApps programmas, Talent lapās tiek pievienotas saites uz jūsu norādītajām programmām.</span><span class="sxs-lookup"><span data-stu-id="07004-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="07004-129">Noklikšķiniet uz saites, lai atvērtu programmu.</span><span class="sxs-lookup"><span data-stu-id="07004-129">Click a link to open an application.</span></span> 



