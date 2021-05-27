---
title: Nav ģenerēts TaxTrans ieraksts
description: Šajā tēmā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt, kad nav ģenerēts TaxTrans ieraksts.
author: qire
ms.date: 04/13/2021
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
ms.openlocfilehash: 74987506699834d86703702106e5abf87bfa45da
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018785"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="a29c3-103">Nav ģenerēts TaxTrans ieraksts</span><span class="sxs-lookup"><span data-stu-id="a29c3-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a29c3-104">Ja transakcijai atlasāt **Grāmatots PVN**, bet lapa **Grāmatots PVN** vai nu nerāda nodokļu rindas, vai arī tai trūkst nodokļu rindas, iespējams, netiks ģenerēts **TaxTrans** ieraksts.</span><span class="sxs-lookup"><span data-stu-id="a29c3-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="a29c3-105">[![Grāmatota PVN lapa, kurā nav rindas krājumu](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="a29c3-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="a29c3-106">Lai novērstu šo problēmu, ja nepieciešams, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a29c3-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="a29c3-107">Pārbaudīt PVN pirms transakcijas grāmatošanas</span><span class="sxs-lookup"><span data-stu-id="a29c3-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="a29c3-108">Pirms transakcijas grāmatošanas lapā **Rēķina grāmatošana** atlasiet **PVN**, lai pārbaudītu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="a29c3-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="a29c3-109">[![PVN poga rēķina grāmatošanas lapā](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="a29c3-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="a29c3-110">Lapā **Pagaidu PVN transakcijas** pārskatiet aprēķina rezultātus.</span><span class="sxs-lookup"><span data-stu-id="a29c3-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="a29c3-111">Ja nodoklis netiek aprēķināts, skatiet [Nodoklis nav aprēķināts vai nodokļa summa ir nulle](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="a29c3-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="a29c3-112">Atrast TaxTrans ierakstu visos grāmatotos PVN</span><span class="sxs-lookup"><span data-stu-id="a29c3-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="a29c3-113">Dodieties uz **Nodokļi** \> **Pieprasījumi un pārskati** \> **PVN pieprasījumi** > **Grāmatotais PVN**.</span><span class="sxs-lookup"><span data-stu-id="a29c3-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="a29c3-114">Kolonnas **Dokuments** virsrakstā atlasiet filtra simbolu, lai atrastu **TaxTrans** ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a29c3-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="a29c3-115">Ja meklējat PVN ierakstus, pārbaudiet datumu.</span><span class="sxs-lookup"><span data-stu-id="a29c3-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="a29c3-116">Ja datums atšķiras no žurnāla virsraksta datuma, izveidojiet Microsoft pakalpojuma pieprasījumu papildu atbalstam.</span><span class="sxs-lookup"><span data-stu-id="a29c3-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="a29c3-117">[![Grāmatota PVN lapa](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="a29c3-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="a29c3-118">Atkļūdot, lai pārbaudītu detaļas</span><span class="sxs-lookup"><span data-stu-id="a29c3-118">Debug to check details</span></span>

1. <span data-ttu-id="a29c3-119">Informāciju par to, kā atkļūdot un noteikt, vai **TmpTaxWorkTrans** un **TaxUncommitted** ir pareizi ģenerētas, skatiet [Lauku vērtība TaxTrans ir nepareiza](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="a29c3-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="a29c3-120">Ja **TaxTmpWorkTrans** vai **TaxUncommitted** ir pareizi ģenerēts, pievienojiet pārtraukumpunktu pie **TaxPost::SaveAndPost()** un **Tax::SaveAndPost**, lai atkļūdotu iemeslu, kāpēc **TaxTrans** nav ievietots.</span><span class="sxs-lookup"><span data-stu-id="a29c3-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="a29c3-121">[![Kodā pievienoti pārtraukumpunkti](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="a29c3-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="a29c3-122">[![Pievienoto pārtraukumpunktu rezultāti](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="a29c3-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="a29c3-123">Noteikt, vai pielāgojums pastāv</span><span class="sxs-lookup"><span data-stu-id="a29c3-123">Determine whether customization exists</span></span>

<span data-ttu-id="a29c3-124">Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē.</span><span class="sxs-lookup"><span data-stu-id="a29c3-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="a29c3-125">Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.</span><span class="sxs-lookup"><span data-stu-id="a29c3-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
