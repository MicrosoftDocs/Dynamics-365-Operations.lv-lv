---
title: Noliktavas darba problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas darbu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3015ec777953cedb5a5d8eea873ed1043cac04cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970243"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="d9b2b-103">Noliktavas darba problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="d9b2b-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9b2b-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas darbu programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="d9b2b-105">Nevar pārvietot numura zīmes, kurām ir sērijas numura krājumi, ja izsekošanas dimensiju grupā ir atļautas tukšas izejas un ieejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d9b2b-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="d9b2b-106">Issue description</span></span>

<span data-ttu-id="d9b2b-107">Numura zīmi nevar pārvietot, izmantojot **Kustības** izvēlnes elementu, ja sērijas numuram ir atļauti *Tukši izejas plūsmas* un *Tukši ieejas plūsmas* iestatījumi izsekošanas dimensiju grupā, un, ja vienā un tajā pašā vietā ir vairākas numura zīmes, dažām, no kurām ir sērijas numuri, un dažām, no kurām nav.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d9b2b-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="d9b2b-108">Issue resolution</span></span>

<span data-ttu-id="d9b2b-109">Šī problēma tiks labota ar izmaiņām, kas izvietotas [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="d9b2b-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="d9b2b-110">Šīs izmaiņas padarīs **Sērijas numura** lauku neobligātu, ja ir atļautas tukšas ieejas plūsmas un tukšas izejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="d9b2b-111">Kad es apstrādāju kustības, es saņemu šādu kļūdas ziņojumu: "noliktavas īpašnieks %1 nav atļauts šajā procesā."</span><span class="sxs-lookup"><span data-stu-id="d9b2b-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d9b2b-112">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="d9b2b-112">Issue description</span></span>

<span data-ttu-id="d9b2b-113">Kad tiek izmantota noliktavas programma, lai veiktu kustības, trūkst **Īpašnieka** izsekošanas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="d9b2b-114">Regulārs krājumu pārsūtīšanas žurnāls no Supply Chain Management klienta tiek rādīts, lai darbotos, kā paredzēts, un to var grāmatot tikai tad, ja ir ievadīta **Īpašnieka** dimensija.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d9b2b-115">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="d9b2b-115">Issue resolution</span></span>

<span data-ttu-id="d9b2b-116">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="d9b2b-117">Pašlaik noliktavas pārvaldības procesi atbalsta tikai tos krājumus, kas pieder juridiskai personai.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
