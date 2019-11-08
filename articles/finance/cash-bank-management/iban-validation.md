---
title: Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana
description: Šajā tēmā ir izskaidrots, kā pārvaldīt starptautiskā bankas konta numura (IBAN) kontu pārbaudi.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2aaccd7c09d6daf8a237a433cc22ac1bfc3c1541
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551263"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="581eb-103">Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="581eb-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="581eb-104">Starptautiskā bankas konta numura (IBAN) validēšana palielina apjomu validēšanai, kas tiek veikta, kad bankas kontam pievienojat IBAN.</span><span class="sxs-lookup"><span data-stu-id="581eb-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="581eb-105">Programmā Microsoft Dynamics 365 Finance tiek glabāta informācija par IBAN struktūru.</span><span class="sxs-lookup"><span data-stu-id="581eb-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="581eb-106">Šī informācija tiek automātiski ielādēta, kad šo IBAN bankas kontiem lietojat pirmo reizi.</span><span class="sxs-lookup"><span data-stu-id="581eb-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="581eb-107">Šī informācija ietver IBAN garumu, bankas konta numura un maršrutēšanas numura sākuma pozīcijas, kā arī bankas konta numura un maršrutēšanas numura garumu.</span><span class="sxs-lookup"><span data-stu-id="581eb-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="581eb-108">IBAN struktūru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="581eb-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="581eb-109">Dodieties uz **Kases un bankas vadība \> Iestatīšana \> IBAN struktūras**.</span><span class="sxs-lookup"><span data-stu-id="581eb-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="581eb-110">Ņemiet vērā, ka IBAN struktūras katrai valstij vai reģionam ir iestatītas automātiski.</span><span class="sxs-lookup"><span data-stu-id="581eb-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="581eb-111">Ja vēlaties pielāgot struktūras kādai noteiktai valstij vai reģionam, varat tās rediģēt.</span><span class="sxs-lookup"><span data-stu-id="581eb-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="581eb-112">Struktūras definīcijas būs katra jauna laidiena daļa.</span><span class="sxs-lookup"><span data-stu-id="581eb-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="581eb-113">Var izmantot izvēlni **Atiestatīt struktūras**, lai ielādētu jaunākās definīcijas pēc katra jauninājuma.</span><span class="sxs-lookup"><span data-stu-id="581eb-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="581eb-114">Bankas konta IBAN struktūras validēšana</span><span class="sxs-lookup"><span data-stu-id="581eb-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="581eb-115">Atveriet sadaļu **Kases un bankas vadība \> Banku konti \> Banku konti**.</span><span class="sxs-lookup"><span data-stu-id="581eb-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="581eb-116">Izveidojiet bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="581eb-116">Create a bank account.</span></span>
3. <span data-ttu-id="581eb-117">Kopsavilkuma cilnē **Papildinformācija** ievadiet IBAN numuru.</span><span class="sxs-lookup"><span data-stu-id="581eb-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="581eb-118">Ja IBAN garums neatbilst garumam, kas ir definēts katrai valstij vai reģionam, jūs saņemat brīdinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="581eb-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="581eb-119">Nevar turpināt, ja IBAN garums neatbilst IBAN struktūrā noteiktajam garumam.</span><span class="sxs-lookup"><span data-stu-id="581eb-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="581eb-120">Validācijā arī tiek pārbaudīts, vai bankas konta numurs atbilst bankas konta numuru pārstāvošajai IBAN numura daļai.</span><span class="sxs-lookup"><span data-stu-id="581eb-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="581eb-121">Ja bankas konta numurs neatbilst, jūs saņemat brīdinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="581eb-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="581eb-122">Šis ziņojums ir tikai brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="581eb-122">This message is only a warning.</span></span> <span data-ttu-id="581eb-123">Jūs varat turpināt arī tādā gadījumā, ja bankas konta numurs neatbilst.</span><span class="sxs-lookup"><span data-stu-id="581eb-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="581eb-124">Validācijā tiek arī pārbaudīts, vai bankas maršrutēšanas numurs atbilst bankas maršrutēšanas numuru pārstāvošajai IBAN daļai.</span><span class="sxs-lookup"><span data-stu-id="581eb-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="581eb-125">Maršrutēšanas numurā ir bankas numurs un bieži arī papildu bankas filiāle.</span><span class="sxs-lookup"><span data-stu-id="581eb-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="581eb-126">Ja bankas maršrutēšanas numurs neatbilst, jūs saņemat brīdinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="581eb-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="581eb-127">Šis ziņojums ir tikai brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="581eb-127">This message is only a warning.</span></span> <span data-ttu-id="581eb-128">Jūs varat turpināt arī tādā gadījumā, ja bankas maršrutēšanas numurs neatbilst.</span><span class="sxs-lookup"><span data-stu-id="581eb-128">You can continue even if the bank routing number doesn't match.</span></span>
