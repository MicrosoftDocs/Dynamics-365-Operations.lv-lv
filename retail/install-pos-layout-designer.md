---
title: "Instalēt Retail POS izkārtojuma veidotāju"
description: "Viena klikšķa veidotāju varat izmantot, lai veikaliem, reģistriem, kasieriem un vadītājiem veidotu dažādus pārdošanas punktu Retail Modern POS (MPOS) un mākoņa POS izkārtojumus gan ainavorientācijas, gan portretorientācijas režīmā."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b33cbf67c00b6baea4393e82d19300085781af29
ms.lasthandoff: 03/31/2017


---

# <a name="install-the-retail-pos-layout-designer"></a>Instalēt Retail POS izkārtojuma veidotāju

Viena klikšķa veidotāju varat izmantot, lai veikaliem, reģistriem, kasieriem un vadītājiem veidotu dažādus pārdošanas punktu Retail Modern POS (MPOS) un mākoņa POS izkārtojumus gan ainavorientācijas, gan portretorientācijas režīmā.

Pārdošanas punkta MPOS vai mākoņa POS grafiskā dizaina interfeisu nosaka kases aparāta izkārtojums. Izkārtojums kontrolē dažādu objektu pozīcijas. Piemēri tostarp ir kopējais izkārtojums, krājumu režģa izkārtojums, debitoru izkārtojums, maksājumu izkārtojums un dažādu izvēlnes pogu izkārtojums. Izkārtojumi ietver arī vispārējo pārdošanas interfeisa izskatu, kas tiek rādīts nodarbinātajiem.

## <a name="install-the-oneclick-designer"></a>Viena klikšķa veidotāja instalēšana
1.  Programmatūrā Microsoft Dynamics 365 for Operations izmantojiet augšējā kreisajā stūrī esošo izvēlni, lai pārietu uz sadaļu **Mazumtirdzniecība** **un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.
2.  Atlasiet jebkuru izkārtojumu, kura programmas tips ir **Modern POS operētājsistēmai Windows** vai **Mākoņa POS**, un pēc tam noklikšķiniet uz **Izkārtojuma veidotājs**.
3.  Lai instalētu viena klikšķa veidotāju, pārlūkprogrammas Internet Explorer loga apakšā parādītajā paziņojumu joslā noklikšķiniet uz **Atvērt**. (Citās pārlūkprogrammās šī paziņojumu josla var tikt parādīta citā vietā.)
4.  Lai instalētu Mazumtirdzniecības veidotāja resursdatoru, parādītajā ziņojuma lodziņā **Programmas palaišana - Drošības brīdinājums** noklikšķiniet uz **Palaist**. Norises indikators rāda instalēšanas norises gaitu.
5.  Kad instalēšana ir pabeigta, lapā **Pierakstīties** ievadiet savu Microsoft Dynamics 365 for Operations lietotājvārdu un paroli, un pēc tam noklikšķiniet uz **Pierakstīties**, lai palaistu šo veidotāju.
6.  Kad jūsu akreditācijas dati ir apstiprināti un veidotājs ir palaists, varat noformēt pats savu izkārtojumu vai mainīt esošo izkārtojumu. [![Izkārtojums viena klikšķa veidotājā](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Novērst izkārtojuma veidotāja instalēšanas problēmas
-   Kad noklikšķināt uz **Veidotājs**, netiek parādīta uzvedne lejupielādēt (vai palaist) instalētāju vai pašreizējie drošības iestatījumi neļauj lejupielādēt failu. **Risinājumi.**
    -   Pārlūkprogrammā Internet Explorer pārliecinieties, ka šai vietnei ir atspējots uznirstošo logu bloķētājs. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Konfidencialitāte** &gt; **Atrast uznirstošo elementu bloķētāju** un mainiet iestatījumu, ja tas ir nepieciešams.
    -   Pārlūkprogrammā Internet Explorer programmas Dynamics 365 for Operations vietrādi URL pievienojiet savām uzticamajām vietnēm. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Drošība** &gt; **Uzticamās vietnes** &gt; **Vietnes** &gt; **Pievienot**.
-   Programma nestartējas un jums liek sazinieties ar kreditoru. **Risinājums.** Pārlūkprogrammā Internet Explorer programmas Dynamics 365 for Operations vietrādi URL pievienojiet savām uzticamajām vietnēm. Noklikšķiniet uz **Iestatījumi** &gt; **Opcijas** &gt; **Drošība** &gt; **Uzticamās vietnes** &gt; **Vietnes** &gt; **Pievienot**.

**Zināma problēma.** Veidotājs nedarbojas pareizi pārlūkprogrammās Google Chrome un Mozilla Firefox. Mēs strādājam, lai šo problēmu novērstu.

<a name="see-also"></a>Skatiet arī
--------

[Konfigurēt, lejupielādēt, instalēt un aktivizēt pārdošanas punktu Retail Modern POS](retail-modern-pos-device-activation.md)


