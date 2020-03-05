---
title: Pārdošanas punkta (POS) programma un lietotāja valodas iestatījumi
description: Šajā tēmā ir aprakstīts, kā mainīt valodas iestatījumus programmās Modern POS (MPOS) un Cloud POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49bfcaa4c05ea8e6cc6bf0a8f855f2474cea35bc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023343"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="1daba-103">Pārdošanas punkta (POS) programma un lietotāja valodas iestatījumi</span><span class="sxs-lookup"><span data-stu-id="1daba-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1daba-104">Šajā tēmā ir aprakstīts, kā mainīt valodas iestatījumus programmās Modern POS (MPOS) un Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="1daba-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="1daba-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="1daba-105">Overview</span></span>
<span data-ttu-id="1daba-106">Programmas Modern POS (MPOS) un Cloud POS atbalsta vides, kurās veikala un lietotāja iestatījumos var atšķirties valodas iestatījumi un tulkojumi.</span><span class="sxs-lookup"><span data-stu-id="1daba-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="1daba-107">Piemēram, veikals var atrasties reģionā, kur vairums debitoru runā angļu valodā, taču daži nodarbinātie vēlas izmantot lietojumprogrammu ar tulkojumiem franču valodā.</span><span class="sxs-lookup"><span data-stu-id="1daba-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="1daba-108">Datu valoda</span><span class="sxs-lookup"><span data-stu-id="1daba-108">Data language</span></span>

<span data-ttu-id="1daba-109">Neatkarīgi no lietotāja iestatījumiem programmās MPOS un Cloud POS vienmēr tiek izmantoti veikala valodas iestatījumi, lai noteiktu datiem lietotos tulkojumus.</span><span class="sxs-lookup"><span data-stu-id="1daba-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="1daba-110">Tādējādi tiek nodrošināts, ka visiem lietotājiem un debitoriem ir pieejamas vienādas iespējas.</span><span class="sxs-lookup"><span data-stu-id="1daba-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="1daba-111">Tālāk ir norādīti datu piemēri.</span><span class="sxs-lookup"><span data-stu-id="1daba-111">Examples of data include:</span></span>

- <span data-ttu-id="1daba-112">Preces</span><span class="sxs-lookup"><span data-stu-id="1daba-112">Products</span></span>
- <span data-ttu-id="1daba-113">Atribūti un vērtības</span><span class="sxs-lookup"><span data-stu-id="1daba-113">Attributes and values</span></span>
- <span data-ttu-id="1daba-114">Kategoriju nosaukumi</span><span class="sxs-lookup"><span data-stu-id="1daba-114">Category names</span></span>
- <span data-ttu-id="1daba-115">Drukātas vai e-pastā sūtītas transakciju kvītis</span><span class="sxs-lookup"><span data-stu-id="1daba-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="1daba-116">Maksāšanas metožu nosaukumi</span><span class="sxs-lookup"><span data-stu-id="1daba-116">Payment method names</span></span>
- <span data-ttu-id="1daba-117">Rindu displeja ziņojumi</span><span class="sxs-lookup"><span data-stu-id="1daba-117">Line display messages</span></span>

<span data-ttu-id="1daba-118">Veikala valoda tiek lietota arī galvenajā POS pieteikšanās ekrānā, jo pirms pieteikšanās nav zināms, kurš lietotājs izmanto POS.</span><span class="sxs-lookup"><span data-stu-id="1daba-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="1daba-119">Ja nav pieejams tulkojums veikala valodā, POS tiek pārslēgts atpakaļ uzņēmuma valodā.</span><span class="sxs-lookup"><span data-stu-id="1daba-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="1daba-120">Veikala valodas iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="1daba-120">Configuring the store's language setting</span></span>

<span data-ttu-id="1daba-121">Veikala valodas iestatījumu var norādīt, lapas **Veikals** sadaļā **Visi veikali** noklikšķinot uz **Vispārīgi &gt; Reģionālie iestatījumi &gt; Valoda**.</span><span class="sxs-lookup"><span data-stu-id="1daba-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="1daba-122">Izmantojiet nolaižamo izvēlni, lai izvēlētos katra veikala valodu.</span><span class="sxs-lookup"><span data-stu-id="1daba-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="1daba-123">Lietotāja interfeisa valoda</span><span class="sxs-lookup"><span data-stu-id="1daba-123">User interface language</span></span>

<span data-ttu-id="1daba-124">POS lietotāja valodas iestatījums nosaka tulkojumus, kas tiek izmantoti programmas lietotāja interfeisā.</span><span class="sxs-lookup"><span data-stu-id="1daba-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="1daba-125">Tas attiecas uz visām etiķetēm, izvēlnēm un sarakstiem, kas netiek uzskatīti par datiem.</span><span class="sxs-lookup"><span data-stu-id="1daba-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="1daba-126">Vienīgais izņēmums ir teksts, kas tiek rādīts POS pogu režģos.</span><span class="sxs-lookup"><span data-stu-id="1daba-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="1daba-127">Pogu režģi neatbalsta tulkojumus, tāpēc tajos teksts vienmēr tiek rādīts tā, kā tas ir definēts uz pogas.</span><span class="sxs-lookup"><span data-stu-id="1daba-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="1daba-128">Lai nodrošinātu pogu tulkojumus, ir jākopē un jāuztur atsevišķi pogu režģi un tie ir jāpiešķir atbilstošajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="1daba-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="1daba-129">Lietotāja valodas iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="1daba-129">Configuring the user's language setting</span></span>

<span data-ttu-id="1daba-130">POS lietotāja valodas iestatījums tiek iestatīts, lapas **Darbinieks** sadaļā **Visi darbinieki** atlasot **Retail un Commerce &gt; Valoda**.</span><span class="sxs-lookup"><span data-stu-id="1daba-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="1daba-131">Tas netiek iestatīts galvenajā cilnē Profils. Šo iestatījumu neizmanto POS.</span><span class="sxs-lookup"><span data-stu-id="1daba-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="1daba-132">Ja lietotāja valoda nav iestatīta vai tā ir iestatīta uz valodu, kurā tulkojumi nav pieejami, POS atiestatīs veikala valodu.</span><span class="sxs-lookup"><span data-stu-id="1daba-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="1daba-133">UI  valoda   </span><span class="sxs-lookup"><span data-stu-id="1daba-133">UI language</span></span>                | <span data-ttu-id="1daba-134">Datu valoda (preces, kvīšu formāti, rindu displejs utt.)</span><span class="sxs-lookup"><span data-stu-id="1daba-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1daba-135">**Uzņēmums**</span><span class="sxs-lookup"><span data-stu-id="1daba-135">**Company**</span></span> | <span data-ttu-id="1daba-136">Noklusējums</span><span class="sxs-lookup"><span data-stu-id="1daba-136">Default</span></span>                    | <span data-ttu-id="1daba-137">Noklusējums</span><span class="sxs-lookup"><span data-stu-id="1daba-137">Default</span></span>                                                       |
| <span data-ttu-id="1daba-138">**Veikals**</span><span class="sxs-lookup"><span data-stu-id="1daba-138">**Store**</span></span>   | <span data-ttu-id="1daba-139">Ignorē uzņēmumu</span><span class="sxs-lookup"><span data-stu-id="1daba-139">Overrides company</span></span>          | <span data-ttu-id="1daba-140">Ignorē uzņēmumu</span><span class="sxs-lookup"><span data-stu-id="1daba-140">Overrides company</span></span>                                             |
| <span data-ttu-id="1daba-141">**Lietotājs**</span><span class="sxs-lookup"><span data-stu-id="1daba-141">**User**</span></span>    | <span data-ttu-id="1daba-142">Ignorē veikalu vai uzņēmumu</span><span class="sxs-lookup"><span data-stu-id="1daba-142">Overrides store or company</span></span> | <span data-ttu-id="1daba-143">Nekad</span><span class="sxs-lookup"><span data-stu-id="1daba-143">Never</span></span>                                                         |