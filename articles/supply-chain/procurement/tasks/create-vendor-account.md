---
title: Piegādātāja konta izveidošana
description: Šajā procedūrā parādīts, kā izveidot kreditora kontu un pievienot adresi un kontaktinformāciju.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aca23db2a0cc86a2c12ea74d3b1e491643b7efec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207696"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="103eb-103">Piegādātāja konta izveidošana</span><span class="sxs-lookup"><span data-stu-id="103eb-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="103eb-104">Šajā procedūrā parādīts, kā izveidot kreditora kontu un pievienot adresi un kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="103eb-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="103eb-105">Procedūrā netiek parādīts, kā aizpildīt visus laukus iepirkuma un finanšu mērķiem.</span><span class="sxs-lookup"><span data-stu-id="103eb-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="103eb-106">Lai uzzinātu vairāk par šiem laukiem, lūdzu, izlasiet lauku aprakstus.</span><span class="sxs-lookup"><span data-stu-id="103eb-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="103eb-107">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="103eb-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="103eb-108">Kreditoru kontus parasti izveido sagādes speciālists vai debitoru parādu personāls.</span><span class="sxs-lookup"><span data-stu-id="103eb-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="103eb-109">Kreditora konta izveide</span><span class="sxs-lookup"><span data-stu-id="103eb-109">Create a vendor account</span></span>
1. <span data-ttu-id="103eb-110">Ejiet uz **Navigācijas rūts > Moduļi > Iepirkumi un ārpakalpojumi > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="103eb-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="103eb-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="103eb-111">Click **New**.</span></span>
3. <span data-ttu-id="103eb-112">Laukā **Kreditora konts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="103eb-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="103eb-113">Vērtībā var tikt ierakstīta automātiski.</span><span class="sxs-lookup"><span data-stu-id="103eb-113">The value may be populated automatically.</span></span> <span data-ttu-id="103eb-114">Ja tā, varat izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="103eb-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="103eb-115">Varat izveidot kreditora kontus personai vai organizācijai.</span><span class="sxs-lookup"><span data-stu-id="103eb-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="103eb-116">Tas ietekmēs, kādi lauki ir pieejami.</span><span class="sxs-lookup"><span data-stu-id="103eb-116">This will affect which fields are available.</span></span> <span data-ttu-id="103eb-117">Šajā piemērā mēs izveidosim kreditora kontu kādai organizācijai.</span><span class="sxs-lookup"><span data-stu-id="103eb-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="103eb-118">Ievadiet vai atlasiet vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="103eb-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="103eb-119">Ja kreditors ir jau reģistrēts jūsu sistēmā, var izmantot nolaižamo sarakstu un atlasīt to šajā laukā un jauns kreditora konts pārmantos jau reģistrētā konta adresi un kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="103eb-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="103eb-120">Laukā **Grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="103eb-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="103eb-121">Kreditoru grupa tiek izmantota, lai grupētu kreditorus, kuriem ir kopīgs kāds no šiem parametriem: apmaksas nosacījumi, apmaksas termiņš, krājumu grāmatošanas virsgrāmatas konti — tostarp pārdošanas nodokļa grupa, noklusējuma virsgrāmatas konti, preču filtra kodi vai piegādes apjoma prognozes konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="103eb-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="103eb-122">Laukā **Darbinieku skaits** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="103eb-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="103eb-123">Laukā **Organizācijas numurs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="103eb-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="103eb-124">Adreses pievienošana</span><span class="sxs-lookup"><span data-stu-id="103eb-124">Add an address</span></span>
1. <span data-ttu-id="103eb-125">Izvērsiet sadaļu **Adreses**.</span><span class="sxs-lookup"><span data-stu-id="103eb-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="103eb-126">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="103eb-126">Click **Add**.</span></span>
3. <span data-ttu-id="103eb-127">Laukā **Nolūks** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="103eb-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="103eb-128">Varat atzīmēt vienu vai vairākus nolūkus.</span><span class="sxs-lookup"><span data-stu-id="103eb-128">You can select one or more purposes.</span></span> <span data-ttu-id="103eb-129">Tie tiek izmantoti, lai atlasītu pareizo adresi konkrētam nolūkam.</span><span class="sxs-lookup"><span data-stu-id="103eb-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="103eb-130">Piemēram, ja nolūks ir "Rēķins", šī adrese tiks izmantota, sūtot rēķinus.</span><span class="sxs-lookup"><span data-stu-id="103eb-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="103eb-131">Laukā **Nosaukums vai apraksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="103eb-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="103eb-132">Laukā **Valsts/reģions** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="103eb-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="103eb-133">Ievadiet adreses detaļas.</span><span class="sxs-lookup"><span data-stu-id="103eb-133">Enter the address details.</span></span> <span data-ttu-id="103eb-134">Atlasītā valsts/reģions noteiks laukus, kuri tiks piedāvāti, atbilstoši valsts/reģiona adreses formātam.</span><span class="sxs-lookup"><span data-stu-id="103eb-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="103eb-135">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="103eb-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="103eb-136">Kontaktinformācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="103eb-136">Add contact information</span></span>
1. <span data-ttu-id="103eb-137">Izvērsiet sadaļu **Kontaktinformācija**.</span><span class="sxs-lookup"><span data-stu-id="103eb-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="103eb-138">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="103eb-138">Click **Add**.</span></span>
3. <span data-ttu-id="103eb-139">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="103eb-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="103eb-140">Atlasiet opciju laukā **Tips**.</span><span class="sxs-lookup"><span data-stu-id="103eb-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="103eb-141">Ierakstiet vērtību laukā **Kontaktpersonas tālrunis/adrese**.</span><span class="sxs-lookup"><span data-stu-id="103eb-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="103eb-142">Varat atzīmēt izvēles rūtiņu Primārs, ja šī ir primārā kontaktpersona.</span><span class="sxs-lookup"><span data-stu-id="103eb-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="103eb-143">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="103eb-143">Click **Save**.</span></span>
7. <span data-ttu-id="103eb-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="103eb-144">Close the page.</span></span>
8. <span data-ttu-id="103eb-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="103eb-145">Close the page.</span></span>

