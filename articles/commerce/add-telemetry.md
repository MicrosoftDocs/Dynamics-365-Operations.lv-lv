---
title: Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju
description: Šajā rakstā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas kolekciju.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a0a5103d239c7f93ad6888a2eaf56d1cac32bd58
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282277"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas kolekciju.

Tīmekļa analīze ir svarīgs rīks, lai izprastu, kā jūsu klienti mijiedarbojas ar jūsu vietni, un pieņemtu lēmumus, kas palīdzēs optimizēt maksimālo pārveidošanas pieredzi. Daudzas tīmekļa analīzes pakotnes ir pieejamas šo mērķu sasniegšanai, piemēram, Google Analytics, Clicker, Moz Analytics un KISSMetrics. Lielākajai daļai tīmekļa analīzes pakotņu ir nepieciešams pievienot klienta puses skripta kodu HTML **\<head\>** elementā visām jūsu vietnes lapām.

> [!NOTE]
> Šajā rakstā sniegtās instrukcijas attiecas arī uz citām pielāgotām klienta Microsoft Dynamics 365 Commerce puses funkcionalitāti, kas neieklīst vietējā piedāvājumā.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Atkārtoti izmantojama fragmenta izveide jūsu skripta kodam

Fragments ļauj atkārtoti izmantot iekļautos vai ārējos skripta kodus visās jūsu vietnes lapās neatkarīgi no veidnes, ko tās izmanto.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Atkārtoti izmantojama fragmenta izveide jūsu iekļautā skripta kodam

Lai izveidotu atkārtoti izmantojamu fragmentu jūsu iekļautajam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.
1. Dialoglodziņā **Jauns fragments** atlasiet **Iekļauts skripts**.
1. Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma iekļautais skripts**.
1. Rekvizītu rūtī labajā pusē zem **iekļautā skripta** ievadiet savu klienta puses skriptu. Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Atkārtoti izmantojama fragmenta izveide jūsu ārējā skripta kodam

Lai izveidotu atkārtoti izmantojamu fragmentu jūsu ārējam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.
1. Dialoglodziņā **Jauns fragments** atlasiet **Ārējs skripts**.
1. Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma ārējais skripts**.
1. Rekvizītu rūtī labajā pusē zem **skripta avots** pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam. Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

> [!NOTE]
> Ja jūsu vietnei ir iespējota satura drošības politika (CSP), pārliecinieties, vai visi ārējie vietrāži URL ir pievienoti **script-src** CSP direktīvai Commerce vietņu veidotājā. Papildinformāciju skatiet [Pārvaldīt satura drošības politiku (CSP)](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Pievienot veidnei fragmentu, kas ietver skripta kodu

Lai veidnei vietnes veidotājā pievienotu fragmentu, kas ietver skripta kodu, izpildiet tālāk norādītās darbības.

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
1. Rekvizītu rūtī labajā pusē zem **iekļautā skripta** ievadiet savu klienta puses skriptu. Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

### <a name="add-an-external-script-directly-to-a-template"></a>Pievienot ārēju skriptu tieši veidnei

Lai pievienotu ārējo skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.
1. Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.
1. **HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet **Ārējs skripts**.
1. Rekvizītu rūtī labajā pusē zem **skripta avots** pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam. Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Izlases ikonas pievienošana](add-favicon.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
