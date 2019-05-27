---
title: Retail pārdošanas punkta (POS) izkārtojumu veidotāja instalēšana
description: Varat izmantot viena klikšķa veidotāju, lai veikaliem, kases sistēmām, kasieriem un vadītājiem izveidotu dažādus programmu Retail Modern POS (MPOS) un Cloud POS izkārtojumus ainavorientācijas vai portretorientācijas režīmā.
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
ms.openlocfilehash: 7fc5b48b71816b662f016f4a2d909526da0595f4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572084"
---
# <a name="install-the-retail-point-of-sale-pos-layout-designer"></a>Retail pārdošanas punkta (POS) izkārtojumu veidotāja instalēšana

[!include [banner](includes/banner.md)]

Varat izmantot viena klikšķa veidotāju, lai veikaliem, kases sistēmām, kasieriem un vadītājiem izveidotu dažādus programmu Retail Modern POS (MPOS) un Cloud POS izkārtojumus ainavorientācijas vai portretorientācijas režīmā.

Pārdošanas punkta MPOS vai mākoņa POS grafiskā dizaina interfeisu nosaka kases aparāta izkārtojums. Izkārtojums kontrolē dažādu objektu pozīcijas. Piemēri tostarp ir kopējais izkārtojums, krājumu režģa izkārtojums, debitoru izkārtojums, maksājumu izkārtojums un dažādu izvēlnes pogu izkārtojums. Izkārtojumi ietver arī vispārējo pārdošanas interfeisa izskatu, kas tiek rādīts nodarbinātajiem.

## <a name="install-the-one-click-designer"></a>Instalēt viena klikšķa veidotāju

1. Programmā Microsoft Dynamics 365 for Retail izmantojiet augšējā kreisajā pusē esošo izvēlni, lai pārietu uz sadaļu **Mazumtirdzniecība** **un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.
2. Atlasiet jebkuru izkārtojumu, kura programmas tips ir **Modern POS operētājsistēmai Windows** vai **Mākoņa POS**, un pēc tam noklikšķiniet uz **Izkārtojuma veidotājs**.
3. Internet Explorer loga apakšdaļā parādītajā paziņojumu joslā noklikšķiniet uz **Atvērt**, lai instalētu viena klikšķa veidotāju. (Citās pārlūkprogrammās šī paziņojumu josla var tikt parādīta citā vietā.)
4. Lai instalētu Mazumtirdzniecības veidotāja resursdatoru, parādītajā ziņojuma lodziņā **Programmas palaišana - Drošības brīdinājums** noklikšķiniet uz **Palaist**. Norises indikators rāda instalēšanas norises gaitu.
5. Kad instalēšana ir pabeigta, lapā **Pierakstīšanās** ievadiet savu Microsoft Dynamics 365 for Retail lietotājvārdu un paroli un pēc tam noklikšķiniet uz **Pierakstīties**, lai palaistu veidotāju.
6. Kad jūsu akreditācijas dati ir apstiprināti un veidotājs ir palaists, varat noformēt pats savu izkārtojumu vai mainīt esošo izkārtojumu.

    [![Izkārtojums viena klikšķa veidotājā](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Novērst izkārtojuma veidotāja instalēšanas problēmas

- Kad noklikšķināt uz **Veidotājs**, netiek parādīta uzvedne lejupielādēt (vai palaist) instalētāju vai pašreizējie drošības iestatījumi neļauj lejupielādēt failu. 

    **Risinājumi.**

    - Pārlūkprogrammā Internet Explorer pārliecinieties, vai šai vietnei ir atspējots uznirstošo logu bloķētājs. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Konfidencialitāte** &gt; **Atrast uznirstošo elementu bloķētāju** un mainiet iestatījumu, ja tas ir nepieciešams.
    - Pārlūkprogrammā Internet Explorer pievienojiet Dynamics 365 for Retail vietrādi URL uzticamo vietņu sarakstam. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Drošība** &gt; **Uzticamās vietnes** &gt; **Vietnes** &gt; **Pievienot**.

- Programma nestartējas un jums liek sazinieties ar kreditoru.

    **Risinājums.** Pārlūkprogrammā Internet Explorer pievienojiet Dynamics 365 for Retail vietrādi URL uzticamo vietņu sarakstam. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Drošība** &gt; **Uzticamās vietnes** &gt; **Vietnes** &gt; **Pievienot**.

**Zināma problēma.** Veidotājs nedarbojas pareizi pārlūkprogrammās Google Chrome un Mozilla Firefox. Mēs strādājam, lai šo problēmu novērstu.

## <a name="additional-resources"></a>Papildu resursi

[Retail Modern POS konfigurēšana, lejupielāde, instalēšana un aktivizēšana](retail-modern-pos-device-activation.md)
