---
title: Pienākumu sadales iestatīšana
description: Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68e1a4419eaa11a59e1b634deb8e76a2bb9b6fdf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548109"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="8f69b-103">Pienākumu sadales iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8f69b-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f69b-104">Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8f69b-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="8f69b-105">Šī koncepcija ir nosaukta par pienākumu sadali.</span><span class="sxs-lookup"><span data-stu-id="8f69b-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="8f69b-106">Piemēram, iespējams, nevēlēsieties, lai viena un tā pati persona apstiprina preču saņemšanu un apstrādātu maksājumus kreditoram.</span><span class="sxs-lookup"><span data-stu-id="8f69b-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="8f69b-107">Pienākumu sadale palīdz samazināt pārkāpumu risku un palīdz arī noteikt kļūdas vai neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="8f69b-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="8f69b-108">Pienākumu sadali var izmantot arī, lai lietotu iekšējās kontroles politikas.</span><span class="sxs-lookup"><span data-stu-id="8f69b-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="8f69b-109">Lai izveidotu nosacījumus, veiciet tālākminēto procedūru.</span><span class="sxs-lookup"><span data-stu-id="8f69b-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="8f69b-110">Lai izpildītu šo procedūru, jums ir jābūt sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="8f69b-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="8f69b-111">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DAT.</span><span class="sxs-lookup"><span data-stu-id="8f69b-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="8f69b-112">Dodieties uz Sistēmas administrēšana > Drošība > Pienākumu sadale > Pienākumu sadales nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="8f69b-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="8f69b-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8f69b-113">Click New.</span></span>
3. <span data-ttu-id="8f69b-114">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8f69b-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8f69b-115">Ievadiet nosacījumu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8f69b-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="8f69b-116">Laukā Pirmais pienākums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8f69b-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8f69b-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8f69b-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8f69b-118">Atlasiet pirmo pienākumu, ko kontrolē nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="8f69b-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="8f69b-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8f69b-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8f69b-120">Laukā Otrais pienākums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8f69b-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8f69b-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8f69b-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8f69b-122">Atlasiet otro pienākumu, ko kontrolē nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="8f69b-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="8f69b-123">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8f69b-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8f69b-124">Laukā Stingrība atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="8f69b-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="8f69b-125">Atlasiet riska smagumu, kas rodas, ja viens un tas pats lietotājs vai loma pilda abus pienākumus.</span><span class="sxs-lookup"><span data-stu-id="8f69b-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="8f69b-126">Laukā Drošības risks ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8f69b-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="8f69b-127">Ievadiet drošības riska aprakstu.</span><span class="sxs-lookup"><span data-stu-id="8f69b-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="8f69b-128">Laukā Drošības mazinājums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8f69b-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="8f69b-129">Ievadiet darbību parakstu, kas jāveic, lai mazinātu drošības risku.</span><span class="sxs-lookup"><span data-stu-id="8f69b-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="8f69b-130">Piemēram, var mazināt risku, veicot detalizētāku procesa pārskatīšanu, veicot ikmēneša vadības pārskatīšanu vai koplietojot resursus ar citām nodaļām.</span><span class="sxs-lookup"><span data-stu-id="8f69b-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="8f69b-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8f69b-131">Click Save.</span></span>

