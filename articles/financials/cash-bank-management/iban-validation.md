---
title: "Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana"
description: "Šajā tēmā ir izskaidrots, kā pārvaldīt starptautiskā bankas konta numura (IBAN) kontu pārbaudi."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: lv-lv
ms.lasthandoff: 09/22/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="79129-103">Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="79129-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79129-104">Starptautiskā bankas konta numura (IBAN) kontu pārbaude palielina pārbaudes apjomu, kas tiek veikts, kad jūs pievienojat IBAN bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="79129-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="79129-105">IBAN struktūra tiek glabāta sistēmā Microsoft Dynamics 365 for Finance and Operation un tiek automātiski ielādēta, kad pirmoreiz izmantojat IBAN bankas kontos.</span><span class="sxs-lookup"><span data-stu-id="79129-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="79129-106">Bankas konta numurs ir daļa no IBAN numura definētās struktūras.</span><span class="sxs-lookup"><span data-stu-id="79129-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="79129-107">Pamatojoties uz šo struktūru, ja IBAN izvietojums un konta numura garums neatbilst izvietojumam, kas ir definēts struktūrā katrai valstij vai reģionam, jūs saņemsiet brīdinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="79129-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="79129-108">IBAN struktūru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="79129-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="79129-109">Dodieties uz **Kases un bankas vadība \> Iestatīšana \> IBAN struktūras**.</span><span class="sxs-lookup"><span data-stu-id="79129-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="79129-110">Ņemiet vērā, ka IBAN struktūras katrai valstij vai reģionam ir iestatītas automātiski.</span><span class="sxs-lookup"><span data-stu-id="79129-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="79129-111">Ja kādai noteiktai valstij vai reģionam struktūras ir jāpielāgo, varat tās rediģēt.</span><span class="sxs-lookup"><span data-stu-id="79129-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="79129-112">Struktūras definīcijas būs katra jauna laidiena daļa.</span><span class="sxs-lookup"><span data-stu-id="79129-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="79129-113">Var izmantot izvēlni **Atiestatīt struktūras**, lai ielādētu jaunākās definīcijas pēc katra jauninājuma.</span><span class="sxs-lookup"><span data-stu-id="79129-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="79129-114">Bankas konta IBAN struktūras validēšana</span><span class="sxs-lookup"><span data-stu-id="79129-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="79129-115">Atveriet sadaļu **Kases un bankas vadība\> Banku konti \> Banku konti**.</span><span class="sxs-lookup"><span data-stu-id="79129-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="79129-116">Izveidojiet bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="79129-116">Create a bank account.</span></span>
3. <span data-ttu-id="79129-117">Kopsavilkuma cilnē **Papildinformācija** ievadiet IBAN numuru.</span><span class="sxs-lookup"><span data-stu-id="79129-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="79129-118">Ja IBAN izvietojums un konta numura garums neatbilst izvietojumam, kas ir definēts struktūrā katrai valstij vai reģionam, jūs saņemat ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="79129-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="79129-119">Nevar turpināt, ja IBAN numura garums neatbilst garumam IBAN struktūrā.</span><span class="sxs-lookup"><span data-stu-id="79129-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="79129-120">Validācijā arī tiek pārbaudīts, vai bankas konta numurs atbilst bankas konta numuru pārstāvošajai IBAN numura daļai.</span><span class="sxs-lookup"><span data-stu-id="79129-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="79129-121">Ja bankas konta numurs neatbilst, jūs saņemsiet brīdinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="79129-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="79129-122">Šis ziņojums ir tikai brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="79129-122">This message is only a warning.</span></span> <span data-ttu-id="79129-123">Jūs varat turpināt arī tādā gadījumā, ja bankas konta numurs neatbilst.</span><span class="sxs-lookup"><span data-stu-id="79129-123">You can continue even if the bank account number doesn't match.</span></span>

