---
title: Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022
description: Šajā procedūrā ir parādīts, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18c7d0b6c5c6a7f598f4b94f4dcf02df498d74cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822709"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="2dc34-103">Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022</span><span class="sxs-lookup"><span data-stu-id="2dc34-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2dc34-104">Šajā tēmā ir paskaidrots, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru.</span><span class="sxs-lookup"><span data-stu-id="2dc34-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="2dc34-105">Šī ir piektā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="2dc34-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="2dc34-106">Lai izpildītu šo piemēru, izmantojiet DEMF demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="2dc34-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="2dc34-107">Paraugs</span><span class="sxs-lookup"><span data-stu-id="2dc34-107">Example</span></span>

1.    <span data-ttu-id="2dc34-108">Pārejiet uz sadaļu **Kreditori > Maksājumi > Maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.    <span data-ttu-id="2dc34-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-109">Click **New**.</span></span>
3.    <span data-ttu-id="2dc34-110">Ievadiet vai atlasiet vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-110">In the **Name** field, enter or select a value.</span></span>
4.    <span data-ttu-id="2dc34-111">Noklikšķiniet uz **Rindas >Maksājuma priekšlikums > Izveidot maksājuma priekšlikumu**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.    <span data-ttu-id="2dc34-112">Izvērsiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-112">Expand the **Records to include** section.</span></span>
6.    <span data-ttu-id="2dc34-113">Noklikšķiniet uz **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-113">Click **Filter**.</span></span>
7.    <span data-ttu-id="2dc34-114">Sarakstā atlasiet vienumam **Kreditoru tabula** un **Kreditora konta lauks** atbilstošo rindu.</span><span class="sxs-lookup"><span data-stu-id="2dc34-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.    <span data-ttu-id="2dc34-115">Ievadiet vai atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="2dc34-116">Apmaksājamo kreditoru transakciju atlasei varat izmantot jebkuru kritēriju, šī piemēra ietvaros izmantojiet kreditora kontu DE-001.</span><span class="sxs-lookup"><span data-stu-id="2dc34-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12.    <span data-ttu-id="2dc34-117">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-117">Click **OK**.</span></span>
13.    <span data-ttu-id="2dc34-118">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-118">Click **OK**.</span></span>
14.    <span data-ttu-id="2dc34-119">Noklikšķiniet uz **Izveidot maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="2dc34-120">Ģenerējiet ISO20022 maksājuma failu.</span><span class="sxs-lookup"><span data-stu-id="2dc34-120">Generate an ISO20022 payment file.</span></span>
    1.    <span data-ttu-id="2dc34-121">Noklikšķiniet uz **Ģenerēt maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-121">Click **Generate payments**.</span></span>
    2.    <span data-ttu-id="2dc34-122">Ievadiet vai atlasiet vērtību laukā **Maksājuma metode**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.    <span data-ttu-id="2dc34-123">Ievadiet vērtību laukā **Faila nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="2dc34-124">Šī piemēra ietvaros ģenerētas fails būs saderīgs ar SEPA, jo maksājuma valūta ir EUR.</span><span class="sxs-lookup"><span data-stu-id="2dc34-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="2dc34-125">Lai ģenerētu maksājumus citās valūtās, var izmantot arī ISO20022 kredīta pārskaitījumu, kā arī citus kreditora maksājumu formātus</span><span class="sxs-lookup"><span data-stu-id="2dc34-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.    <span data-ttu-id="2dc34-126">Ievadiet vai atlasiet vērtību laukā **Bankas konts**.</span><span class="sxs-lookup"><span data-stu-id="2dc34-126">In the **Bank account** field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]