---
title: POS izkārtojuma veidotāja instalēšana
description: Viena klikšķa veidotāju varat izmantot, lai veikaliem, reģistriem, kasieriem un vadītājiem veidotu dažādus pārdošanas punktu Modern POS (MPOS) un mākoņa POS izkārtojumus gan ainavorientācijas, gan portretorientācijas režīmā.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9882ae895de926e0da3579ab65a988f2b97f7be
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414039"
---
# <a name="install-the-pos-layout-designer"></a>POS izkārtojuma veidotāja instalēšana

[!include [banner](includes/banner.md)]

Viena klikšķa veidotāju varat izmantot, lai veikaliem, reģistriem, kasieriem un vadītājiem veidotu dažādus pārdošanas punktu Modern POS (MPOS) un mākoņa POS izkārtojumus gan ainavorientācijas, gan portretorientācijas režīmā.

Pārdošanas punkta MPOS vai mākoņa POS grafiskā dizaina interfeisu nosaka kases aparāta izkārtojums. Izkārtojums kontrolē dažādu objektu pozīcijas. Piemēri tostarp ir kopējais izkārtojums, krājumu režģa izkārtojums, debitoru izkārtojums, maksājumu izkārtojums un dažādu izvēlnes pogu izkārtojums. Izkārtojumi ietver arī vispārējo pārdošanas interfeisa izskatu, kas tiek rādīts nodarbinātajiem.

## <a name="install-the-one-click-designer"></a>Instalēt viena klikšķa veidotāju

1. Programmā Commerce izmantojiet augšējā kreisajā pusē esošo izvēlni, lai pārietu uz sadaļu **Retail un Commerce** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.
2. Atlasiet jebkuru izkārtojumu, kura programmas tips ir **Modern POS operētājsistēmai Windows** vai **Mākoņa POS**, un pēc tam noklikšķiniet uz **Izkārtojuma veidotājs**.
3. Internet Explorer loga apakšdaļā parādītajā paziņojumu joslā noklikšķiniet uz **Atvērt**, lai instalētu viena klikšķa veidotāju. (Citās pārlūkprogrammās šī paziņojumu josla var tikt parādīta citā vietā.)
4. Lai instalētu Mazumtirdzniecības veidotāja resursdatoru, parādītajā ziņojuma lodziņā **Programmas palaišana - Drošības brīdinājums** noklikšķiniet uz **Palaist**. Norises indikators rāda instalēšanas norises gaitu.
5. Kad instalēšana ir pabeigta, lapā **Pierakstīties** ievadiet savu Commerce lietotājvārdu un paroli un pēc tam noklikšķiniet uz **Pierakstīties**, lai palaistu veidotāju.
6. Kad jūsu akreditācijas dati ir apstiprināti un veidotājs ir palaists, varat noformēt pats savu izkārtojumu vai mainīt esošo izkārtojumu.

    [![Izkārtojums viena klikšķa veidotājā](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Novērst izkārtojuma veidotāja instalēšanas problēmas

- Kad noklikšķināt uz **Veidotājs**, netiek parādīta uzvedne lejupielādēt (vai palaist) instalētāju vai pašreizējie drošības iestatījumi neļauj lejupielādēt failu. 

    **Risinājumi.**

    - Pārlūkprogrammā Internet Explorer pārliecinieties, vai šai vietnei ir atspējots uznirstošo logu bloķētājs. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Konfidencialitāte** &gt; **Atrast uznirstošo elementu bloķētāju** un mainiet iestatījumu, ja tas ir nepieciešams.
    - Pārlūkprogrammā Internet Explorer pievienojiet Commerce vietrādi URL uzticamo vietņu sarakstam. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Drošība** &gt; **Uzticamās vietnes** &gt; **Vietnes** &gt; **Pievienot**.

- Programma nestartējas un jums liek sazinieties ar kreditoru.

    **Risinājums:** Pārlūkprogrammā Internet Explorer pievienojiet Commerce vietrādi URL uzticamo vietņu sarakstam. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Drošība** &gt; **Uzticamās vietnes** &gt; **Vietnes** &gt; **Pievienot**.

**Zināma problēma:** veidotājs nedarbojas pareizi pārlūkprogrammās Google Chrome un Mozilla Firefox. Mēs strādājam, lai šo problēmu novērstu.

## <a name="additional-resources"></a>Papildu resursi

[ Retail Modern POS (MPOS) konfigurēšana, instalēšana un aktivizēšana](retail-modern-pos-device-activation.md)
