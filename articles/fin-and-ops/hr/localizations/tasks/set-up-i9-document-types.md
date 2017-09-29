--- 
title: "I–9 dokumentu tipu iestatīšana"
description: "Šajā procedūrā parādīts, kā skatīt un iestatīt dokumentu tipus, kas tiek izmantoti I-9 pārbaudei."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="88964-103">I–9 dokumentu tipu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="88964-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="88964-104">Šajā procedūrā parādīts, kā skatīt un iestatīt dokumentu tipus, kas tiek izmantoti I-9 pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="88964-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="88964-105">Pirms iestatāt I-9 dokumentu tipus, ir jāiestata arī izdevējiestādes un identifikācijas tipus.</span><span class="sxs-lookup"><span data-stu-id="88964-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="88964-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF, kurā iekļauti izsniegšanas iestāžu un identifikācijas veidu piemēri, kas vajadzīgi, lai veiktu procedūru.</span><span class="sxs-lookup"><span data-stu-id="88964-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="88964-107">Pārejiet uz sadaļu Personāla vadība > Darbinieki > I-9 > I-9 dokumentu veidi.</span><span class="sxs-lookup"><span data-stu-id="88964-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="88964-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="88964-108">Click New.</span></span>
3. <span data-ttu-id="88964-109">Laukā I-9 dokumenta tips ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="88964-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="88964-110">Piemērs: skolas apliecība.</span><span class="sxs-lookup"><span data-stu-id="88964-110">Example: School ID.</span></span>  
4. <span data-ttu-id="88964-111">Atlasiet identifikācijas tipu.</span><span class="sxs-lookup"><span data-stu-id="88964-111">Select the identification type.</span></span>  <span data-ttu-id="88964-112">Piemērs: skolas apliecība</span><span class="sxs-lookup"><span data-stu-id="88964-112">Example:  School ID</span></span>
    * <span data-ttu-id="88964-113">Identifikācijas tips var būt sociālās apdrošināšanas numurs (SAN), vīzas numurs, pases ID vai autovadītāja apliecība.</span><span class="sxs-lookup"><span data-stu-id="88964-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="88964-114">Atlasiet I-9 dokumentu sarakstu, kas tiek izmantots dokumenta tipam.</span><span class="sxs-lookup"><span data-stu-id="88964-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="88964-115">I-9 procesa ietvaros darbiniekiem jāuzrāda dokumentācija, kas parāda darba devējam to identitāti un nodarbinātības atļauju.</span><span class="sxs-lookup"><span data-stu-id="88964-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="88964-116">ASV pilsonības un Imigrācijas dienestu vietnē atrodas informācija par to, kādi dokumenti ir pieņemami un uz kuru sarakstu tie attiecas.</span><span class="sxs-lookup"><span data-stu-id="88964-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="88964-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="88964-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="88964-118">Laukā Forma ievadiet oficiālo dokumenta tipa formas numuru.</span><span class="sxs-lookup"><span data-stu-id="88964-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="88964-119">Piemērs: skolas apliecība.</span><span class="sxs-lookup"><span data-stu-id="88964-119">Example: School ID.</span></span>
    * <span data-ttu-id="88964-120">Oficiālu veidlapu numurus var atrast ASV pilsonības un Imigrācijas dienestu vietnē.</span><span class="sxs-lookup"><span data-stu-id="88964-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="88964-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="88964-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="88964-122">Atzīmējiet izvēles rūtiņu Aktīvs vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="88964-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="88964-123">Laukā Derīgs līdz iestatiet datumu uz “27.10.2019”.</span><span class="sxs-lookup"><span data-stu-id="88964-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="88964-124">Derīguma termiņa beigu datums nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="88964-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="88964-125">Atlasiet iestādi, kas izsniedza dokumenta tipu.</span><span class="sxs-lookup"><span data-stu-id="88964-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="88964-126">Piemērs: rajons/teritorija</span><span class="sxs-lookup"><span data-stu-id="88964-126">Example: Province/territory</span></span>
10. <span data-ttu-id="88964-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="88964-127">Click Save.</span></span>


