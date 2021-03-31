---
title: Ērta bezsaistes pārslēgšanās dāvanu karšu un kredītrēķinu darbībām
description: Šajā tēmā sniegts to uzlabojumu apskats, kas nodrošina ērtu bezsaistes pārslēgšanos noteiktiem maksājuma veidiem.
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ea46ae90dedcc3ad3c3b305bddeb4d98827353a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230672"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="dbcad-103">Ērta bezsaistes pārslēgšanās dāvanu karšu un kredītrēķinu darbībām</span><span class="sxs-lookup"><span data-stu-id="dbcad-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbcad-104">Ja pārdošanas punkta (POS) ierīce zaudē savu savienojumu ar kanāla datu bāzi, lielākā daļa POS darbību un transakciju, kas bija uzsāktas, var tikt turpinātas pēc tam, kad kasieris saņems brīdinājuma ziņojumu par savienojamības zudumu.</span><span class="sxs-lookup"><span data-stu-id="dbcad-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="dbcad-105">Tomēr dažos gadījumos transakcijām ir elementi, kas paļaujas uz reāllaika pakalpojumu, un šie elementi netiek atbalstīti, ja POS ir bezsaistē.</span><span class="sxs-lookup"><span data-stu-id="dbcad-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="dbcad-106">Šajā tēmā ir aprakstīta daļa funkcionalitātes, kas palīdz samazināt zaudētās savienojamības ietekmi šādos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="dbcad-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="dbcad-107">Dāvanu karšu transakciju izpilde bezsaistes režīmā</span><span class="sxs-lookup"><span data-stu-id="dbcad-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="dbcad-108">Iekšējās dāvanu kartes ir atkarīgas no reāllaika pakalpojuma, jo dāvanu karšu bilancei jābūt centralizēti uzturētai programmā Microsoft Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="dbcad-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="dbcad-109">Lai novērstu krāpšanu vai citas sinhronizēšanas problēmas, dāvanu kartes tiek bloķētas, tiklīdz tās tiek pievienotas transakcijai.</span><span class="sxs-lookup"><span data-stu-id="dbcad-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="dbcad-110">Bloķēšanas funkcija nodrošina to, ka dāvanu karti nevar izmantot vairākos termināļos vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="dbcad-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="dbcad-111">Pēc darbības pabeigšanas dāvanu karte tiek automātiski atjaunināta un atbloķēta.</span><span class="sxs-lookup"><span data-stu-id="dbcad-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="dbcad-112">Tomēr, ja POS pazaudē savienojumu pēc tam, kad dāvanu karte ir pievienota transakcijai, dāvanu karte var kļūt nelietojama.</span><span class="sxs-lookup"><span data-stu-id="dbcad-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="dbcad-113">Lai nepieļautu šo situāciju, Dynamics 365 Commerce ir parametrs, kas aktivizē transakcijas, kas ietver dāvanu kartes rindu, kas jāizpilda, kamēr POS ir bezsaistē.</span><span class="sxs-lookup"><span data-stu-id="dbcad-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="dbcad-114">Kad šis parametrs ir ieslēgts, dāvanu kartes transakcijas, kas nonāk bezsaistē, tiks saglabātas kopā ar bezsaistes transakcijām, un tās tiks sinhronizētas ar Commerce Headquarters, kad tiks sinhronizētas bezsaistes transakcijas.</span><span class="sxs-lookup"><span data-stu-id="dbcad-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="dbcad-115">Sinhronizācija arī atbloķē dāvanu karti, lai to varētu izmantot citā terminālī.</span><span class="sxs-lookup"><span data-stu-id="dbcad-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="dbcad-116">Lai iespējotu funkcionalitāti, kas ļauj noslēgt dāvanu kartes transakcijas pēc pārslēgšanās uz bezsaistes režīmu, dodieties uz cilni **Grāmatošana**, kas atrodas lapā **Commerce parametri**.</span><span class="sxs-lookup"><span data-stu-id="dbcad-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="dbcad-117">Šajā cilnē atrodiet kopsavilkuma cilni **Dāvanu karte** un iestatiet opciju **Noslēgt dāvanu karšu darbības bezsaistes režīmā** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="dbcad-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![Bezsaistes dāvanu kartes iestatīšana](../media/gift.png)

<span data-ttu-id="dbcad-119">Commerce parametri parasti tiek kešoti.</span><span class="sxs-lookup"><span data-stu-id="dbcad-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="dbcad-120">Tāpēc, lai sinhronizētu izmaiņas kanālā pēc šī parametra iestatījuma atjaunināšanas un sadales grafika sākšanas, izmaiņas var ilgt līdz pat 24 stundām.</span><span class="sxs-lookup"><span data-stu-id="dbcad-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="dbcad-121">Lai izmaiņas stātos spēkā nekavējoties, atiestatiet Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="dbcad-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="dbcad-122">Kredītrēķina transakciju izpilde bezsaistes režīmā</span><span class="sxs-lookup"><span data-stu-id="dbcad-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="dbcad-123">Līdzīgi kā iekšējās dāvanu kartes, kredītrēķini tiek centralizēti uzturēti pakalpojumā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="dbcad-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="dbcad-124">Commerce ir parametrs, kas iespējo kredītrēķinu transakciju izpildi, kamēr POS ir bezsaistē.</span><span class="sxs-lookup"><span data-stu-id="dbcad-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="dbcad-125">Šis parametrs darbojas tāpat kā dāvanu kartes parametrs, kas minēts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="dbcad-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="dbcad-126">Kad parametrs ir ieslēgts, kredītrēķina transakcijas, kas nonākušas bezsaistē, tiks sinhronizētas ar kanāla datu bāzi kopā ar citām transakcijām, kas tika veiktas, kamēr POS bija bezsaistē.</span><span class="sxs-lookup"><span data-stu-id="dbcad-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="dbcad-127">Lai iespējotu funkcionalitāti, kas ļauj noslēgt kredītrēķina transakcijas pēc pārslēgšanās uz bezsaistes režīmu, dodieties uz cilni **Grāmatošana**, kas atrodas lapā **Commerce parametri**.</span><span class="sxs-lookup"><span data-stu-id="dbcad-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="dbcad-128">Šajā cilnē atrodiet kopsavilkuma cilni **Kredītrēķins** un iestatiet opciju **Noslēgt kredītrēķinu transakcijas bezsaistes režīmā** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="dbcad-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![Bezsaistes kredītrēķina iestatīšana](../media/creditmemo.png)

<span data-ttu-id="dbcad-130">Commerce parametri parasti tiek kešoti.</span><span class="sxs-lookup"><span data-stu-id="dbcad-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="dbcad-131">Tāpēc, lai sinhronizētu izmaiņas kanālā pēc šī parametra iestatījuma atjaunināšanas un sadales grafika sākšanas, izmaiņas var ilgt līdz pat 24 stundām.</span><span class="sxs-lookup"><span data-stu-id="dbcad-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="dbcad-132">Lai izmaiņas stātos spēkā nekavējoties, atiestatiet IIS.</span><span class="sxs-lookup"><span data-stu-id="dbcad-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbcad-133">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="dbcad-133">Related topics</span></span>

- [<span data-ttu-id="dbcad-134">Pārdošanas punktu (POS) funkcionalitāte bezsaistē</span><span class="sxs-lookup"><span data-stu-id="dbcad-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="dbcad-135">Tiešsaistes un bezsaistes pārdošanas punkta (POS) operācijas</span><span class="sxs-lookup"><span data-stu-id="dbcad-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]