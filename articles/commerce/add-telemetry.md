---
title: Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju
description: Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761253"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.

## <a name="overview"></a>Pārskats

Tīmekļa analīze ir svarīgs rīks, lai izprastu, kā jūsu klienti mijiedarbojas ar jūsu vietni, un pieņemtu lēmumus, kas palīdzēs optimizēt maksimālo pārveidošanas pieredzi. Daudzas tīmekļa analīzes pakotnes ir pieejamas šo mērķu sasniegšanai, piemēram, Google Analytics, Clicker, Moz Analytics un KISSMetrics. Lielākajai daļai tīmekļa analīzes pakotņu ir nepieciešams pievienot klienta puses skripta kodu HTML **\<head\>** elementā visām jūsu vietnes lapām.

> [!NOTE]
> Šajā tēmā instrukcijas attiecas arī uz citu pielāgotu klienta puses funkcionalitāti, ko programma Microsoft Dynamics 365 Commerce vispārēji nepiedāvā.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Atkārtoti izmantojama fragmenta izveide jūsu skripta kodam

Fragments ļauj atkārtoti izmantot iekļautos vai ārējos skripta kodus visās jūsu vietnes lapās neatkarīgi no veidnes, ko tās izmanto.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Atkārtoti izmantojama fragmenta izveide jūsu iekļautā skripta kodam

Lai izveidotu atkārtoti izmantojamu fragmentu jūsu iekļautajam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.
1. Dialoglodziņā **Jauns fragments** atlasiet **Iekļauts skripts**.
1. Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma iekļautais skripts**.
1. Rekvizītu rūtī labajā pusē zem **iekļautā skripta**ievadiet savu klienta puses skriptu. Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Atkārtoti izmantojama fragmenta izveide jūsu ārējā skripta kodam

Lai izveidotu atkārtoti izmantojamu fragmentu jūsu ārējam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.
1. Dialoglodziņā **Jauns fragments** atlasiet **Ārējs skripts**.
1. Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma ārējais skripts**.
1. Rekvizītu rūtī labajā pusē zem **skripta avots**pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam. Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Pievienot veidnei fragmentu, kas ietver skripta kodu

Lai veidnei vietnes veidotājā pievienotu fragmentu, kas ietver skripta kodu, izpildiet tālāk noradītās darbības.

1. Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.
1. Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.
1. Slotā **HTML galvene** atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot fragmentu**.
1. Atlasiet fragmentu, ko izveidojāt savam skripta kodam.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Pievienot ārēju skriptu vai iekļautu skriptu tieši veidnei

Ja vēlaties ievietot iekļauto vai ārējo skriptu tieši lapu kopā, kas tiek kontrolēta ar vienu veidni, vispirms nav jāizveido fragments.

### <a name="add-an-inline-script-directly-to-a-template"></a>Pievienot iekļautu skriptu tieši veidnei

Lai pievienotu iekļauto skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.
1. Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.
1. **HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet **Iekļauts skripts**.
1. Rekvizītu rūtī labajā pusē zem **iekļautā skripta**ievadiet savu klienta puses skriptu. Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

### <a name="add-an-external-script-directly-to-a-template"></a>Pievienot ārēju skriptu tieši veidnei

Lai pievienotu ārējo skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.
1. Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.
1. **HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet **Ārējs skripts**.
1. Rekvizītu rūtī labajā pusē zem **skripta avots**pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam. Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Izlases ikonas pievienošana](add-favicon.md)

[Sveiciena ziņojuma pievienošana](add-welcome-message.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)
