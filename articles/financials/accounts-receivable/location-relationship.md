---
title: "Atrašanās vietas un pušu attiecību tipu pievienošana"
description: "Šajā tēmā ir paskaidrots, kā pievienot jaunu atrašanās vietas un pušu attiecību tipu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf971bc6cf4b11de6381e369235d582678d074fc
ms.openlocfilehash: 8de914e0fb853cdc9aa36e55a02156757793abc3
ms.contentlocale: lv-lv
ms.lasthandoff: 06/12/2018

---

# <a name="add-new-location-roles-and-party-relationship-types"></a><span data-ttu-id="fd2c1-103">Jaunu atrašanās vietu lomu un pušu attiecību tipu pievienošana</span><span class="sxs-lookup"><span data-stu-id="fd2c1-103">Add new location roles and party relationship types</span></span> 

## <a name="add-new-location-roles"></a><span data-ttu-id="fd2c1-104">Jaunu atrašanās vietu lomu pievienošana</span><span class="sxs-lookup"><span data-stu-id="fd2c1-104">Add new location roles</span></span>

<span data-ttu-id="fd2c1-105">Pastāv divi tālāk aprakstītie veidi, kā pievienot jaunas atrašanās vietas lomas adresei un kontaktinformācijai.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="fd2c1-106">Pievienojiet šo informāciju lapā **Adreses un kontaktinformācijas nolūks**.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="fd2c1-107">Jaunā loma tiks saglabāta tabulā **LogisticsLocationRole** ar iestatījumu type = 0, kas norāda, ka šī loma nav sistēmas loma, kas tiek definēta uzskaitījumā **LogisticsLocationRoleType** un tā paplašinājumos.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="fd2c1-108">Lietotājs šo lomu varēs izmantot, veidojot adresi vai kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Adreses un kontaktinformācijas nolūks](media/Address-Contact.PNG)

-  <span data-ttu-id="fd2c1-110">Pievienojiet šo vienumu uzskaitījuma **LogisticsLocationRoleType** paplašinājumam un ļaujiet tam aizpildīties, izmantojot datubāzes sinhronizēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="fd2c1-111">Izveidojiet paplašinājumu uzskaitījumam **LogisticsLocationRoleType** un pievienojiet jaunu lomu šajā paplašinājumā.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="fd2c1-113">Izveidojiet jaunu resursu failu jaunajai lomai un pēc tam piešķiriet kādu vērtību tā rekvizītiem.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Jauns resursu fails](media/Resource.PNG)
        
    3.  <span data-ttu-id="fd2c1-115">Izveidojiet datu aizpildīšanas klasi un nodrošiniet apdarinātāja metodi, lai aizpildītu jauno lomu.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Datu aizpildīšana](media/Dirdata.PNG)

    4.  <span data-ttu-id="fd2c1-117">Lai testētu jaunās atrašanās vietas lomas aizpildīšanu, varat izveidot izpildāmu klasi un izsaukt DirDataPopulation::insertLogisticsLocationRoles() funkcijā Main().</span><span class="sxs-lookup"><span data-stu-id="fd2c1-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="fd2c1-118">Pēc šī procesa izpildīšanas jums vajadzētu redzēt, ka jaunā loma ir aizpildīta tabulā **LogisticsLocationRole** ar tipu \> 0.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="fd2c1-119">Jaunā loma tiks rādīta lapā **Adreses un kontaktinformācijas nolūks**.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Jaunas atrašanās vietas ievietošana](media/InsertNewLocation.PNG)

## <a name="add-new-party-relationship-types"></a><span data-ttu-id="fd2c1-121">Jaunu pušu attiecību tipu pievienošana</span><span class="sxs-lookup"><span data-stu-id="fd2c1-121">Add new party relationship types</span></span> 

<span data-ttu-id="fd2c1-122">Pastāv divi tālāk aprakstītie veidi, kā pievienot jaunu attiecību tipu.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="fd2c1-123">Pievienojiet to, izmantojot lapu **Attiecību tipu**.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="fd2c1-124">Jaunās attiecības tiks saglabātas tabulā **DirRelationshipTypeTable** ar iestatījumu systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Attiecību tipi](media/Relationship.PNG)

-  <span data-ttu-id="fd2c1-126">Pievienojiet šo vienumu uzskaitījuma **DirSystemRelationshipType** paplašinājumam un ļaujiet tam aizpildīties, izmantojot datubāzes sinhronizēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="fd2c1-127">Izveidojiet uzskaitījuma **DirSystemRelationshipType** paplašinājumu un pievienojiet jauno attiecību tipu.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="fd2c1-128">Izveidojiet inicializētāju šim jaunajam tipam.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-128">Create an initializer for this new type.</span></span> <span data-ttu-id="fd2c1-129">Kodola kodā ir atrodami vairāki piemēri, viens no tiem ir  **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="fd2c1-130">Šī ir inicializētāja klase pušu attiecību tipam “Bērnelements”.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="fd2c1-131">Varat sākt darbu ar savu inicializētāju, nokopējot un ielīmējot šo kodu, un pēc tam atjaunināt iezīmētos apgabalus.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="fd2c1-133">Lai testētu jaunā attiecību tipa aizpildīšanu, varat izveidot izpildāmu klasi un izsaukt DirDataPopulation::insertDirRelationshipTypes() funkcijā Main().</span><span class="sxs-lookup"><span data-stu-id="fd2c1-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="fd2c1-134">Jums vajadzētu redzēt jauno attiecību tipu tabulā **DirRelationshipTypeTable**, un jaunais attiecību tips būs pieejams lapā **Attiecību tipi**.</span><span class="sxs-lookup"><span data-stu-id="fd2c1-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Izpildāma klase](media/Runnable.PNG)
