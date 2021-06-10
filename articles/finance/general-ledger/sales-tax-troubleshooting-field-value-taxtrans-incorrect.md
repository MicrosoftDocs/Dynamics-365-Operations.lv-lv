---
title: Nepareiza lauka vērtība kolonnā TaxTrans
description: Šajā tēmā sniegta informācija par nepareizu lauka vērtību novēršanu kolonnā TaxTrans.
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 488ff54f1dd99208db940024a2fe8b2d25861f44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020167"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="2ccea-103">Nepareiza lauka vērtība kolonnā TaxTrans</span><span class="sxs-lookup"><span data-stu-id="2ccea-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ccea-104">Ja lauka vērtība kolonnā **TaxTrans** nav pareiza, izmantojiet informāciju šajā tēmā, lai mēģinātu atrisināt šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="2ccea-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="2ccea-105">Vērtību apskats</span><span class="sxs-lookup"><span data-stu-id="2ccea-105">Overview of values</span></span>
<span data-ttu-id="2ccea-106">Šajā sarakstā ir parādīts, kā **TaxTrans**, **TaxUncommitted** un **TmpTaxWorkTrans** ir līdzīgas datu kopas, bet darbojas citādi.</span><span class="sxs-lookup"><span data-stu-id="2ccea-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="2ccea-107">**TaxTrans** ir pēdējais grāmatoto nodokļu transakciju rezultāts, kas saglabājas datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="2ccea-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="2ccea-108">**TaxUncommitted** ir vidējais aprēķinātais nodokļu rezultāts, kas saglabājas datu bāzē (ja piemērojams), kas vēlāk tiks izmantota grāmatojot.</span><span class="sxs-lookup"><span data-stu-id="2ccea-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="2ccea-109">**TmpTaxWorkTrans** ir pagaidu aprēķinātais nodokļu rezultāts atmiņā esošajā tabulā (Tabulas tips = Atmiņā).</span><span class="sxs-lookup"><span data-stu-id="2ccea-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="2ccea-110">Ja konstatējat nepareizu kolonnu **TaxTrans** ir atrasts arī pamatcēlonis nepareizai kolonnai **TaxUncommitted** vai **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="2ccea-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="2ccea-111">Tas ir tāpēc, ka trīs kolonnas tiek kopētas viena no otras.</span><span class="sxs-lookup"><span data-stu-id="2ccea-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="2ccea-112">Parasti nodokļu aprēķina laikā tiek ģenerēts **TmpTaxWorkTrans** un pēc tam, ja piemērojams, tiek ģenerēts **TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="2ccea-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="2ccea-113">Nodokļu grāmatošanas laikā tiek ģenerēts **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="2ccea-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="2ccea-114">Pievienot pārtraukumpunktus</span><span class="sxs-lookup"><span data-stu-id="2ccea-114">Add breakpoints</span></span>
<span data-ttu-id="2ccea-115">Lai pievienotu pārtraukumpunktus, veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="2ccea-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="2ccea-116">Paplašinājumu un pārtraukumpunktu pievienošana paplašinājumos *ievietot()* un *atjaunināt()*.</span><span class="sxs-lookup"><span data-stu-id="2ccea-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="2ccea-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="2ccea-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="2ccea-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="2ccea-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="2ccea-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="2ccea-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="2ccea-120">Alternatīvi pārtraukumpunktus var pievienot tieši, ja **TaxUncommitted** nav iekļauts.</span><span class="sxs-lookup"><span data-stu-id="2ccea-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="2ccea-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="2ccea-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="2ccea-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="2ccea-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="2ccea-123">Pavairot un atkļūdot</span><span class="sxs-lookup"><span data-stu-id="2ccea-123">Reproduce and debug</span></span>

<span data-ttu-id="2ccea-124">Kad pārtraukumpunkti ir iestatīti, atkļūdošanas laikā tiek redzamas visas datu saglabātās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="2ccea-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="2ccea-125">Lai atrastu nepareizas **TaxTrans**, **TaxUncommitted** vai **TmpTaxWorkTrans** kolonnas pamatcēloni, pārskatiet un atzīmējiet šādus elementus:</span><span class="sxs-lookup"><span data-stu-id="2ccea-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="2ccea-126">Pēdējais pārtraukumpunkts, kur kolonna ir pareiza.</span><span class="sxs-lookup"><span data-stu-id="2ccea-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="2ccea-127">Pirmais pārtraukumpunkts, kur kolonna ir nepareiza.</span><span class="sxs-lookup"><span data-stu-id="2ccea-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="2ccea-128">Kas notiek starp šiem diviem punktiem.</span><span class="sxs-lookup"><span data-stu-id="2ccea-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="2ccea-129">Noteikt, vai pielāgojums pastāv</span><span class="sxs-lookup"><span data-stu-id="2ccea-129">Determine whether customization exists</span></span>
<span data-ttu-id="2ccea-130">Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet problēmas nav iespējams atrisināt, nosakiet, vai pielāgošana eksistē.</span><span class="sxs-lookup"><span data-stu-id="2ccea-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="2ccea-131">Ja pielāgošana nepastāv, sazinieties ar Microsoft atbalsta dienestu, lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="2ccea-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
