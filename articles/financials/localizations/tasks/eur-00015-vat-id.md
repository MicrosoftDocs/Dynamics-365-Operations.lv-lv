---
title: EUR-00015 PVN ID iestatīšana
description: Šajā procedūrā parādīti PVN ID reģistrācijas priekšnosacījumi, piemēram, reģistrācijas tipa iestatīšana un reģistrācijas kategorijas piešķiršana.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60b22c3e15a9d7b228ec724ca77a61a18b11b257
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538149"
---
# <a name="eur-00015-set-up-vat-id"></a><span data-ttu-id="3dbc8-103">EUR-00015 PVN ID iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3dbc8-103">EUR-00015 Set up VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3dbc8-104">Šajā procedūrā parādīti PVN ID reģistrācijas priekšnosacījumi, piemēram, reģistrācijas tipa iestatīšana un reģistrācijas kategorijas piešķiršana.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="3dbc8-105">Jūs varat atrast papildus informāciju par reģistrācijas ID un reģistrācijas ID apstrādi, ieskaitot nepieciešamos priekšnosacījumus, Reģistrācijas ID palīdzības tēmā.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="3dbc8-106">Šeit sniegtā informācija attiecas uz visām Eiropas valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="3dbc8-107">Šis uzdevums ir izveidots, izmantojot demonstrācijas uzņēmuma DEMF datus, norādot Vāciju kā juridiskās personas primārās adreses valsti.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="3dbc8-108">Šis uzdevums ir paredzēts sistēmas administratoriem.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-108">This task is intended for system administrators.</span></span> <span data-ttu-id="3dbc8-109">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="3dbc8-110">Dodieties uz Organizācijas administrēšana > Globālā adrešu grāmata > Reģistrācijas tipi > Reģistrācijas tipi.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="3dbc8-111">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="3dbc8-112">Laukā Nosaukums ierakstiet 'PVN ID'.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="3dbc8-113">Laukā Apraksts, PVN numuru.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="3dbc8-114">Laukā Valsts/reģions ievadiet vai atlasiet vērtību DEU</span><span class="sxs-lookup"><span data-stu-id="3dbc8-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="3dbc8-115">Laukā Unikāls atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="3dbc8-116">Atzīmējiet šo izvēles rūtiņu, lai pārbaudītu, vai PVN ID ir unikāls.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="3dbc8-117">Atlasiet Jā laukā Primārais valstij.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="3dbc8-118">Atzīmējiet šo izvēles rūtiņu, ja PVN ID ir spēkā visām adresēm, kas pieder norādītajai valstij/reģionam.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="3dbc8-119">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-119">Click Create.</span></span>
9. <span data-ttu-id="3dbc8-120">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-120">Click Add.</span></span>
10. <span data-ttu-id="3dbc8-121">Laukā Valsts/reģions ievadiet vai atlasiet vērtību ITA</span><span class="sxs-lookup"><span data-stu-id="3dbc8-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="3dbc8-122">Laukā Formāts ierakstiet '###########'.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="3dbc8-123">Ievadot šī tipa reģistrācijas ID atlasītajai valstij/reģionam, reģistrācijas ID tiks pārbaudīts ar šo formātu.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="3dbc8-124">Atzīmējiet izvēles rūtiņu Unikāls.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="3dbc8-125">Atzīmējiet šo izvēles rūtiņu, lai pārbaudītu, vai PVN ID ir unikāls.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="3dbc8-126">Atlasiet Primārais valstij izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="3dbc8-127">Atzīmējiet šo izvēles rūtiņu, ja PVN ID ir spēkā visām adresēm, kas pieder norādītajai valstij/reģionam.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="3dbc8-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-128">Click Save.</span></span>
15. <span data-ttu-id="3dbc8-129">Dodieties uz Organizācijas administrēšana > Globālā adrešu grāmata > Reģistrācijas tipi > Reģistrācijas kategorijas.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="3dbc8-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-130">Click New.</span></span>
17. <span data-ttu-id="3dbc8-131">Laukā Valsts/reģions ievadiet vai atlasiet vērtību PVN ID, DEU</span><span class="sxs-lookup"><span data-stu-id="3dbc8-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="3dbc8-132">Laukā Reģistrācijas kategorija atlasiet 'PVN ID'.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="3dbc8-133">Piešķirt reģistrācijas tipu, ko jūs izveidojāt agrāk iepriekš definētai Reģistrācijas kategorijai.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="3dbc8-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-134">Click New.</span></span>
20. <span data-ttu-id="3dbc8-135">Laukā Valsts/reģions ievadiet vai atlasiet vērtību PVN ID, ITA</span><span class="sxs-lookup"><span data-stu-id="3dbc8-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="3dbc8-136">Laukā Reģistrācijas kategorija atlasiet 'PVN ID'.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="3dbc8-137">Piešķirt reģistrācijas tipu, ko jūs izveidojāt iepriekš definētai reģistrācijas kategorijai.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="3dbc8-138">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-138">Click Save.</span></span>

