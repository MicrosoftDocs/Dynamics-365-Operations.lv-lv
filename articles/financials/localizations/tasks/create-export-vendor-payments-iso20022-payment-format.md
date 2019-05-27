---
title: Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022
description: Šajā procedūrā ir parādīts, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b589d64a4446420164175b41f435cf48daac01a9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570057"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="f8a74-103">Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022</span><span class="sxs-lookup"><span data-stu-id="f8a74-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8a74-104">Šajā tēmā ir paskaidrots, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru.</span><span class="sxs-lookup"><span data-stu-id="f8a74-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="f8a74-105">Šī ir piektā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="f8a74-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="f8a74-106">Lai izpildītu šo piemēru, izmantojiet DEMF demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="f8a74-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="f8a74-107">Paraugs</span><span class="sxs-lookup"><span data-stu-id="f8a74-107">Example</span></span>

1.  <span data-ttu-id="f8a74-108">Pārejiet uz sadaļu **Kreditori > Maksājumi > Maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="f8a74-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-109">Click **New**.</span></span>
3.  <span data-ttu-id="f8a74-110">Ievadiet vai atlasiet vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="f8a74-111">Noklikšķiniet uz **Rindas >Maksājuma priekšlikums > Izveidot maksājuma priekšlikumu**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="f8a74-112">Izvērsiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="f8a74-113">Noklikšķiniet uz **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="f8a74-114">Sarakstā atlasiet vienumam **Kreditoru tabula** un **Kreditora konta lauks** atbilstošo rindu.</span><span class="sxs-lookup"><span data-stu-id="f8a74-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="f8a74-115">Ievadiet vai atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="f8a74-116">Apmaksājamo kreditoru transakciju atlasei varat izmantot jebkuru kritēriju, šī piemēra ietvaros izmantojiet kreditora kontu DE-001.</span><span class="sxs-lookup"><span data-stu-id="f8a74-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="f8a74-117">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-117">Click **OK**.</span></span>
13. <span data-ttu-id="f8a74-118">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-118">Click **OK**.</span></span>
14. <span data-ttu-id="f8a74-119">Noklikšķiniet uz **Izveidot maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="f8a74-120">Ģenerējiet ISO20022 maksājuma failu.</span><span class="sxs-lookup"><span data-stu-id="f8a74-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="f8a74-121">Noklikšķiniet uz **Ģenerēt maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="f8a74-122">Ievadiet vai atlasiet vērtību laukā **Maksājuma metode**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="f8a74-123">Ievadiet vērtību laukā **Faila nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="f8a74-124">Šī piemēra ietvaros ģenerētas fails būs saderīgs ar SEPA, jo maksājuma valūta ir EUR.</span><span class="sxs-lookup"><span data-stu-id="f8a74-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="f8a74-125">Lai ģenerētu maksājumus citās valūtās, var izmantot arī ISO20022 kredīta pārskaitījumu, kā arī citus kreditora maksājumu formātus</span><span class="sxs-lookup"><span data-stu-id="f8a74-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="f8a74-126">Ievadiet vai atlasiet vērtību laukā **Bankas konts**.</span><span class="sxs-lookup"><span data-stu-id="f8a74-126">In the **Bank account** field, enter or select a value.</span></span>

