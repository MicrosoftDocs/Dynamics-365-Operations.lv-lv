---
title: Iespējot nokavētā nodokļa aprēķinu žurnālā
description: Šajā tēmā ir skaidrots, kā izmantot **Iespējot aizkavētā nodokļa aprēķinu žurnālā** līdzekli. lai uzlabotu nodokļu aprēķina veiktspēju, ja žurnāla rindu apjoms ir milzīgs.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178806"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="a40c4-103">Iespējot nokavētā nodokļa aprēķinu žurnālā</span><span class="sxs-lookup"><span data-stu-id="a40c4-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a40c4-104">Šajā tēmā ir skaidrots, kā izmantot **Iespējot aizkavētā nodokļa aprēķinu žurnālā** līdzekli. lai uzlabotu nodokļu aprēķina veiktspēju, ja žurnāla rindu apjoms ir milzīgs.</span><span class="sxs-lookup"><span data-stu-id="a40c4-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="a40c4-105">Pašreizējā PVN aprēķina režīms žurnālā ir aktivizēts reāllaikā, kad lietotājs atjaunina ar nodokļiem saistītos laukus, piemēram, PVN grupu/krājumu PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="a40c4-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="a40c4-106">Jebkurš atjauninājums žurnāla rindas līmenī atkārtoti aprēķinās nodokļu summu visās žurnāla rindās.</span><span class="sxs-lookup"><span data-stu-id="a40c4-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="a40c4-107">Tas palīdz lietotājam redzēt reāllaikā aprēķināto nodokļa summu, bet tas var arī izraisīt veiktspējas problēmas, ja žurnāla rindu apjoms ir milzīgs.</span><span class="sxs-lookup"><span data-stu-id="a40c4-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="a40c4-108">Šis līdzeklis sniedz iespēju atlikt nodokļu aprēķinu, lai atrisinātu veiktspējas problēmu.</span><span class="sxs-lookup"><span data-stu-id="a40c4-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="a40c4-109">Ja šī funkcija ir ieslēgta, nodokļa summa tiek aprēķināta tikai tad, kad lietotājs noklikšķina uz komandas "PVN", vai iegrāmato žurnālu.</span><span class="sxs-lookup"><span data-stu-id="a40c4-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="a40c4-110">Lietotājs var ieslēgt/izslēgt parametru trīs līmeņos:</span><span class="sxs-lookup"><span data-stu-id="a40c4-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="a40c4-111">Pēc juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="a40c4-111">By legal entity</span></span>
- <span data-ttu-id="a40c4-112">Pēc žurnāla nosaukuma</span><span class="sxs-lookup"><span data-stu-id="a40c4-112">By journal name</span></span>
- <span data-ttu-id="a40c4-113">Pēc žurnāla virsraksta</span><span class="sxs-lookup"><span data-stu-id="a40c4-113">By journal header</span></span>

<span data-ttu-id="a40c4-114">Sistēma izmantos parametra vērtību žurnāla virsrakstā kā galīgo variantu.</span><span class="sxs-lookup"><span data-stu-id="a40c4-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="a40c4-115">Parametra vērtība žurnāla virsrakstā būs iestatīta uz noklusējumu no žurnāla nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="a40c4-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="a40c4-116">Kad tiek izveidots žurnāla nosaukums, žurnāla nosaukuma parametra vērtība tiks iestatīta uz noklusējumu no virsgrāmatas parametra.</span><span class="sxs-lookup"><span data-stu-id="a40c4-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="a40c4-117">Lauki "Faktiskā PVN summa" un "Aprēķinātā PVN summa" žurnālā būs paslēpti, ja šis parametrs ir ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="a40c4-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="a40c4-118">Šis nolūks nav maldināt lietotāju, jo šo divu lauku vērtība vienmēr rādīs 0, pirms lietotājs aktivizēs nodokļa aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="a40c4-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="a40c4-119">Iespējot nokavētā nodokļa aprēķinu pēc juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="a40c4-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="a40c4-120">Dodieties uz **Virsgrāmata > Virsgrāmatas iestatīšana > Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="a40c4-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="a40c4-121">Noklikšķiniet uz **PVN** cilni</span><span class="sxs-lookup"><span data-stu-id="a40c4-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="a40c4-122">Zem ātrās cilnes **Vispārīgi** , atradiet parametru **Aizkavēta nodokļa aprēķins**, ieslēdziet/izslēdziet to</span><span class="sxs-lookup"><span data-stu-id="a40c4-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="a40c4-123">Iespējot nokavētā nodokļa aprēķinu pēc žurnāla nosaukuma</span><span class="sxs-lookup"><span data-stu-id="a40c4-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="a40c4-124">Pārejiet uz sadaļu **Virsgrāmata >Žurnāla iestatīšana > Žurnālu nosaukumi**.</span><span class="sxs-lookup"><span data-stu-id="a40c4-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="a40c4-125">Zem ātrās cilnes **Vispārīgi** , atradiet parametru **Aizkavēta nodokļa aprēķins**, ieslēdziet/izslēdziet to</span><span class="sxs-lookup"><span data-stu-id="a40c4-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="a40c4-126">Iespējot nokavētā nodokļa aprēķinu pēc žurnāla</span><span class="sxs-lookup"><span data-stu-id="a40c4-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="a40c4-127">Dodieties uz **Virsgrāmata > Žurnāla ieraksti > Vispārējie žurnāli**</span><span class="sxs-lookup"><span data-stu-id="a40c4-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="a40c4-128">Klikšķiniet **Jauns**</span><span class="sxs-lookup"><span data-stu-id="a40c4-128">Click **New**</span></span>
3. <span data-ttu-id="a40c4-129">Atlasiet žurnāla nosaukumu</span><span class="sxs-lookup"><span data-stu-id="a40c4-129">Select a journal name</span></span>
4. <span data-ttu-id="a40c4-130">Noklišķiniet uz **Iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="a40c4-130">Click **Setup**</span></span>
5. <span data-ttu-id="a40c4-131">Atradiet parametru **Aizkavēta nodokļa aprēķins**, ieslēdziet/izslēdziet to</span><span class="sxs-lookup"><span data-stu-id="a40c4-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
