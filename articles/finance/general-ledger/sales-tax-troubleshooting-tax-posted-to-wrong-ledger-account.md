---
title: Nodoklis ir grāmatots nepareizam virsgrāmatas kontam dokumentā
description: Šajā tēmā sniegta traucējummeklēšanas informācija, kas var palīdzēt, grāmatojot nodokļus nepareizam Virsgrāmatas kontam dokumentā.
author: qire
ms.date: 04/12/2021
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
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020095"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="f55b2-103">Nodoklis ir grāmatots nepareizam virsgrāmatas kontam dokumentā</span><span class="sxs-lookup"><span data-stu-id="f55b2-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f55b2-104">Grāmatošanas laikā nodoklis varētu būt grāmatots nepareizam virsgrāmatas kontam dokumentā.</span><span class="sxs-lookup"><span data-stu-id="f55b2-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="f55b2-105">Lai novērstu šo problēmu, ja nepieciešams, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f55b2-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="f55b2-106">Piemēri šajā tēmā izmanto pārdošanas pasūtījumu kā biznesa dokumentu.</span><span class="sxs-lookup"><span data-stu-id="f55b2-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="f55b2-107">Atrast nepareizi grāmatotās nodokļu transakcijas nodokļu kodu</span><span class="sxs-lookup"><span data-stu-id="f55b2-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="f55b2-108">Lapā **Dokumentu transakcijas** atlasiet transakciju, ar kuru vēlaties strādāt, un pēc tam atlasiet **Grāmatotais PVN**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="f55b2-109">[![Grāmatotā PVN poga dokumentu transakciju lapā](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="f55b2-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="f55b2-110">Pārskatiet vērtību laukā **PVN kods**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="f55b2-111">Šajā piemērā tas ir **PVN 19**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="f55b2-112">[![PVN koda lauks lapā Grāmatotais PVN](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="f55b2-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="f55b2-113">Pārbaudīt PVN koda Virsgrāmatas grāmatošanas grupu</span><span class="sxs-lookup"><span data-stu-id="f55b2-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="f55b2-114">Dodieties uz **Nodoklis** \> **Netiešie nodokļi** \> **PVN** \> **PVN kodi**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="f55b2-115">Atrodiet un atlasiet nodokļa kodu un pēc tam pārskatiet vērtību laukā **Virsgrāmatas grāmatošanas grupa**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="f55b2-116">Šajā piemērā tas ir **PVN**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="f55b2-117">[![Virsgrāmatas grāmatošanas grupas lauks lapā PVN kodi](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="f55b2-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="f55b2-118">Lauka **Virsgrāmatas grāmatošanas grupas** vērtība ir saite.</span><span class="sxs-lookup"><span data-stu-id="f55b2-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="f55b2-119">Lai apskatītu grupas konfigurācijas detaļas, izvēlieties saiti.</span><span class="sxs-lookup"><span data-stu-id="f55b2-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="f55b2-120">Pēc izvēles atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) laukā un pēc tam atlasiet **Skatīt detalizētu informāciju**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="f55b2-121">[![Komanda Skatīt informāciju](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="f55b2-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="f55b2-122">Laukā **Maksājamais PVN** pārbaudiet, vai konta numurs ir pareizs atbilstoši transakciju tipam.</span><span class="sxs-lookup"><span data-stu-id="f55b2-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="f55b2-123">Ja tā nav, atlasiet pareizo kontu, ar kuru grāmatot.</span><span class="sxs-lookup"><span data-stu-id="f55b2-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="f55b2-124">Šajā piemērā pārdošanas pasūtījuma PVN ir jāgrāmato maksājamā PVN kontā 222200.</span><span class="sxs-lookup"><span data-stu-id="f55b2-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="f55b2-125">[![Lauks Maksājamais pārdošanas nodoklis lapā Virsgrāmatas grāmatošanas grupas](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="f55b2-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="f55b2-126">Šajā tabulā sniegta informācija par katru lauku **Virsgrāmatas grāmatošanas grupu** lapā.</span><span class="sxs-lookup"><span data-stu-id="f55b2-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="f55b2-127">Lauks</span><span class="sxs-lookup"><span data-stu-id="f55b2-127">Field</span></span>                  | <span data-ttu-id="f55b2-128">Apraksts</span><span class="sxs-lookup"><span data-stu-id="f55b2-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="f55b2-129">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="f55b2-129">Sales tax payable</span></span>      | <span data-ttu-id="f55b2-130">Galvēnais konts izejošiem PVN, kas jāmaksā PVN iestādei.</span><span class="sxs-lookup"><span data-stu-id="f55b2-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="f55b2-131">Saņemtais PVN</span><span class="sxs-lookup"><span data-stu-id="f55b2-131">Sales tax receivable</span></span>   | <span data-ttu-id="f55b2-132">Galvēnais konts ienākošajiem nodokļiem, kas saņemti no PVN iestādes.</span><span class="sxs-lookup"><span data-stu-id="f55b2-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="f55b2-133">Importa nodokļa izdevumi</span><span class="sxs-lookup"><span data-stu-id="f55b2-133">Use tax expense</span></span>        | <span data-ttu-id="f55b2-134">Galvenais konts, kas tiek izmantots, lai iegrāmatotu atskaitāmos lietošanas nodokļus, kurus kreditori nepieprasa vai neiesniedz nodokļu administrācijai kā daļu no Eiropas Savienības (ES) apgrieztās maksāšanas preču un pakalpojumu nodokļa (PPN)/saskaņotā PVN (Harmonized Sales Tax - HST).</span><span class="sxs-lookup"><span data-stu-id="f55b2-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="f55b2-135">Opcijai **Izmantošanas nodoklis** ir jābūt atlasītai PVN kodam PVN grupā, kas tiek izmantota transakcijā.</span><span class="sxs-lookup"><span data-stu-id="f55b2-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="f55b2-136">Šis lauks nav pieejams, ja lapā **Virsgrāmatas parametri** ir atlasīts **Piemērot PVN nodokļu sistēmas kārtulas**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="f55b2-137">Maksājamais importa nodoklis</span><span class="sxs-lookup"><span data-stu-id="f55b2-137">Use tax payable</span></span>        | <span data-ttu-id="f55b2-138">Galvenais konts, ko lieto, lai grāmatotu ienākošos importa nodokļus, kas jāmaksā nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="f55b2-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="f55b2-139">Maksājumu konts</span><span class="sxs-lookup"><span data-stu-id="f55b2-139">Settlement account</span></span>     | <span data-ttu-id="f55b2-140">Galvenais konts tiek izmantots, lai grāmatotu neto bilanci no Virsgrāmatas kontiem, kas norādīti laukos **Maksājamais importa nodoklis** un **Saņemamais PVN**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="f55b2-141">Kreditora termiņatlaide</span><span class="sxs-lookup"><span data-stu-id="f55b2-141">Vendor cash discount</span></span>   | <span data-ttu-id="f55b2-142">Galvenais konts, ko izmanto, lai grāmatotu termiņatlaidi PVN kodiem, kas saistīti ar šo Virsgrāmatas grāmatošanas grupu.</span><span class="sxs-lookup"><span data-stu-id="f55b2-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="f55b2-143">Debitora gadījuma atlaide</span><span class="sxs-lookup"><span data-stu-id="f55b2-143">Customer case discount</span></span> | <span data-ttu-id="f55b2-144">Galvenais konts, ko izmanto, lai grāmatotu termiņatlaidi PVN kodiem, kas saistīti ar šo Virsgrāmatas grāmatošanas grupu.</span><span class="sxs-lookup"><span data-stu-id="f55b2-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="f55b2-145">Papildinformācijai skatiet [Virsgrāmatas PVN grāmatošanas grupu iestatīšana](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="f55b2-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="f55b2-146">Atkļūdošanas kods Virsgrāmatas dimensiju pārbaudei</span><span class="sxs-lookup"><span data-stu-id="f55b2-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="f55b2-147">Kodā grāmatošanas kontu nosaka Virsgrāmatas dimensija.</span><span class="sxs-lookup"><span data-stu-id="f55b2-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="f55b2-148">Virsgrāmatas dimensija saglabā konta ieraksta ID datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="f55b2-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="f55b2-149">Pārdošanas pasūtījumam pievienojiet pārtraukumpunktu metodēs **Tax::saveAndPost()** un **Tax::post()**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="f55b2-150">Jāpievērš uzmanība vērtībai **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="f55b2-151">[![Pārdošanas pasūtījuma koda paraugs, kam ir pārtraukumpunkts](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="f55b2-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="f55b2-152">Pirkšanas pasūtījumam pievienojiet pārtraukumpunktu metodes **TaxPost::saveAndPost()** un **TaxPost::postToTaxTrans()**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="f55b2-153">Jāpievērš uzmanība vērtībai **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="f55b2-154">[![Pirkšanas pasūtījuma koda paraugs, kam ir pārtraukumpunkts](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="f55b2-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="f55b2-155">Palaidiet šādu SQL vaicājumu, lai atrastu konta parādāmo vērtību datu bāzē, balstoties uz ieraksta ID, kas saglabāts ar Virsgrāmatas dimensiju.</span><span class="sxs-lookup"><span data-stu-id="f55b2-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="f55b2-156">[![Rādīt ieraksta ID vērtību](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="f55b2-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="f55b2-157">Pārbaudiet izsaukumus, lai atrastu, kur **_ledgerDimension** ir piešķirts.</span><span class="sxs-lookup"><span data-stu-id="f55b2-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="f55b2-158">Parasti vērtība ir no **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="f55b2-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="f55b2-159">Šajā gadījumā ir jāpievieno pārtraukumpunkts pie **TmpTaxWorkTrans::insert()** un **TmpTaxWorkTrans::update()**, lai atrastu piešķirto vērtību.</span><span class="sxs-lookup"><span data-stu-id="f55b2-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="f55b2-160">Noteikt, vai pielāgojums pastāv</span><span class="sxs-lookup"><span data-stu-id="f55b2-160">Determine whether customization exists</span></span>

<span data-ttu-id="f55b2-161">Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē.</span><span class="sxs-lookup"><span data-stu-id="f55b2-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="f55b2-162">Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.</span><span class="sxs-lookup"><span data-stu-id="f55b2-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
