---
title: Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju
description: Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914543"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.

## <a name="overview"></a>Pārskats

Tīmekļa analīze ir svarīgs rīks, lai izprastu, kā jūsu klienti mijiedarbojas ar jūsu vietni, un pieņemtu lēmumus, kas palīdzēs optimizēt maksimālo pārveidošanas pieredzi. Daudzas tīmekļa analīzes pakotnes ir pieejamas šo mērķu sasniegšanai, piemēram, Google Analytics, Clicker, Moz Analytics un KISSMetrics. Lielākajai daļai tīmekļa analīzes pakotņu ir nepieciešams pievienot klienta puses skripta kodu HTML **\<galvenajā\>** elementā visām jūsu vietnes lapām.

> [!NOTE]
> Šajā tēmā instrukcijas attiecas arī uz citu pielāgotu klienta puses funkcionalitāti, ko programma Microsoft Dynamics 365 Commerce vispārēji nepiedāvā.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Atkārtoti izmantojama fragmenta izveide jūsu skripta kodam

Pēc tam, kad esat izveidojis fragmentu savam skripta kodam, to var atkārtoti izmantot visās vietnes lapās.

1. Dodieties uz **Fragmenti \>Jaunas lapas fragments**.
2. Atlasiet **Ārējais skripts**, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
3. Fragmentu hierarhijā atlasiet **skripta ievadītājs**, kas ir jūsu tikko izveidotā fragmenta moduļa apakšelements.
4. Labajā pusē rekvizītu rūtī pievienojiet jūsu klienta puses skriptu un iestatiet citas konfigurācijas opcijas pēc nepieciešamības.

## <a name="add-the-fragment-to-templates"></a>Fragmenta pievienošana veidnēm

1. Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.
2. Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.
3. Atlasiet daudzpunktes pogu (**...**) **HTML galvenajam** slotam un pēc tam atlasiet **Pievienot moduli**.
4. Atlasiet fragmentu, ko izveidojāt savam skripta kodam.
5. Saglabājiet veidni un pārbaudiet to.

> [!NOTE]
> Pēc pabeigšanas jums ir jāpublicē fragments un pamata veidne. 

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Izlases ikonas pievienošana](add-favicon.md)

[Sveiciena ziņojuma pievienošana](add-welcome-message.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

