---
title: Tūlītēja papildināšana
description: Šajā tēmā ir aprakstīts, kā var izmantot tūlītēju papildināšanu, lai papildinātu krājumu, kad atrašanās vietas direktīvai neizdodas piešķirt krājumu.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c69a9c9fd595280ba4f05a11409a3e672e4b1691
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017511"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="55af7-103">Tūlītēja papildināšana</span><span class="sxs-lookup"><span data-stu-id="55af7-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55af7-104">Tūlītēja papildināšana ļauj papildināt krājumu tūlīt pēc tam, kad atrašanās vietas direktīvas rindai neizdodas piešķirt krājumu.</span><span class="sxs-lookup"><span data-stu-id="55af7-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="55af7-105">Papildināšanas pamatā ir atsevišķa rinda atrašanās vietas direktīvas iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="55af7-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="55af7-106">Ja krājumi nav pieejami mērvienībās, kas ir norādītas attiecīgajā rindā, nekavējoties tiek veikta attiecīgās mērvienības papildināšana.</span><span class="sxs-lookup"><span data-stu-id="55af7-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="55af7-107">Tūlītēja papildināšana nodrošina alternatīvu tādai metodi, saskaņā ar kuru krājumu sadalījums balstās uz vairākām rindām atrašanās vietas direktīvā un pieprasījums tiek summēts sadalījuma beigās un papildināts, izmantojot mērvienības, kas norādītas atrašanās vietas direktīvas pēdējā rindā.</span><span class="sxs-lookup"><span data-stu-id="55af7-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="55af7-108">Tūlītējas papildināšanas priekšrocības ir tās, ka papildināšanu var ierobežot, izmantojot noteiktas vienības, un daudzumu var novirzīt uz noteiktām vietām.</span><span class="sxs-lookup"><span data-stu-id="55af7-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="55af7-109">Biznesa scenārijs</span><span class="sxs-lookup"><span data-stu-id="55af7-109">Business scenario</span></span>

<span data-ttu-id="55af7-110">Piemēram, jums ir noliktava, kurā ir atsevišķas izdošanas zonas mērvienībām “kārba" un “gabals”.</span><span class="sxs-lookup"><span data-stu-id="55af7-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="55af7-111">Jūs vēlaties optimizēt izdošanas procesu, izdodot pēc iespējas vairāk kārbu un pēc tam izdodot atlikušo daudzumu, kas ir mazāks par vienu kārbu, no zonas “gabali”.</span><span class="sxs-lookup"><span data-stu-id="55af7-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="55af7-112">Šajā gadījumā, var izmantot tūlītēju papildināšanu.</span><span class="sxs-lookup"><span data-stu-id="55af7-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="55af7-113">Atrašanās vietas direktīvā var iestatīt tūlītēju papildināšanu kārbām, lai pieprasījuma papildināšana tiktu izmantota, tiklīdz trūkst kārbu, kuras izdot pieprasītajam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="55af7-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="55af7-114">Šādā veidā tiek optimizēts izdošanas process, lai izdošanā tiktu ietvertas pēc iespējas vairāk kārbas.</span><span class="sxs-lookup"><span data-stu-id="55af7-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="55af7-115">Tūlītējā papildināšanas ģenerēs kārbu papildināšanu, un pieprasījums netiks nodots, lai izdotu daudzumus, izmantojot mērvienības "gabals".</span><span class="sxs-lookup"><span data-stu-id="55af7-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="55af7-116">Citiem vārdiem sakot, no zonas “gabals” tiks izdoti tikai daudzumi, kas ir jāizdod, izmantojot mērvienību “gabals” (t. i., daudzumi, kas ir mazāki nekā “kārba”).</span><span class="sxs-lookup"><span data-stu-id="55af7-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="55af7-117">Ja zonā “kārba” ir nepietiekams daudzums, varat izdot maksimāli iespējamo kārbu daudzumu no kopējā pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="55af7-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="55af7-118">Pēc tam atlikušie daudzumi tiks izdoti no zonas “gabali”.</span><span class="sxs-lookup"><span data-stu-id="55af7-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="55af7-119">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="55af7-119">Where it applies</span></span>

<span data-ttu-id="55af7-120">Tūlītēja papildināšana tiek izmantota kopuma izpildes laikā, ja notiek nesekmīgs sadalījums kādai atrašanās vietas direktīvas rindai, kurai ir iestatīta papildinājuma veidne.</span><span class="sxs-lookup"><span data-stu-id="55af7-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="55af7-121">Tūlītējas papildināšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="55af7-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="55af7-122">Atveriet sadaļu **Noliktavas pārvaldība** \> **Iestatīšana** \> **Atrašanās vietas direktīvas** un pēc tam cilnes **Rindas** sarakstā **Tūlītējas papildināšanas veidne** atlasiet papildināšanas veidni kopuma pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="55af7-122">Go to **Warehouse management** \> **Setup** \> **Location directives** , and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="55af7-123">Papildināšanas veidne tiek lietota, ja atrašanās vietas direktīvas rindai neizdodas sadalīt atvēlēto mērvienību.</span><span class="sxs-lookup"><span data-stu-id="55af7-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="55af7-124">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="55af7-124">Troubleshooting</span></span>

<span data-ttu-id="55af7-125">Ja atrašanās vietas direktīvas rindai ir atlasīta tūlītēja papildināšana, bet netiek ģenerēts papildināšanas darbs, kad izmantojat pieprasījuma papildināšanas veidnes attiecīgajai atrašanās vietas direktīvas rindai, ir jāpārbauda divi galvenie iemesli.</span><span class="sxs-lookup"><span data-stu-id="55af7-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="55af7-126">Pārliecinieties, ka lietotā pieprasījuma papildināšanas veidne ir iestatīta tā, lai izmantotu pareizās atrašanās vietas veidnes un darba veidnes, kuru tips ir **Papildināšana**.</span><span class="sxs-lookup"><span data-stu-id="55af7-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="55af7-127">Pārliecinieties, ka ir pietiekami daudz pieejamu krājumu atrašanās vietās, kurās pieprasījuma papildināšanas veidne meklē pieejamus krājumus papildināšanai.</span><span class="sxs-lookup"><span data-stu-id="55af7-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>
