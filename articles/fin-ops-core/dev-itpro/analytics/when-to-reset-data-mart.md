---
title: Data mart atiestatīšanas BUJ
description: Šī tēma sniedz atbildes uz dažiem bieži uzdotiem jautājumiem par data mart atiestatīšanu.
author: jinniew
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266613"
---
# <a name="data-mart-resets-faq"></a>Data mart atiestatīšanas BUJ

Šī tēma sniedz atbildes uz dažiem bieži uzdotiem jautājumiem par data mart atiestatīšanu. Data mart atiestatīšana var būt laikietilpīgs process un atkarībā no apstākļiem var nebūt nepieciešamais risinājums. Tāpēc šī tēma ietver informāciju par apstākļiem, kuros data mart atiestatīšana var palīdzēt, kā arī gadījumos, kad tas, visticamāk, nepalīdzēs.

## <a name="what-is-a-data-mart-reset"></a>Kas ir data mart atiestatīšana?

Data marta atiestatīšana atspējos integrācijas uzdevumus, izdzēsis visus data mart datus un tad atkārtoti aktivizēs integrāciju.

Lai nodrošinātu, ka vecie dati netiek ievietoti, data mart atiestatīšanu var sākt tikai pēc esošo uzdevumu pabeigšanas. Ja mēģināsit atiestatīt data mart pirms visu uzdevumu pabeigšanas, iespējams, saņemsit ziņojumu, tādu kā "Data mart atiestatīšanu nevarēja apstrādāt aktīva uzdevuma dēļ. Lūdzu, vēlāk mēģiniet vēlreiz.”

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Kad jāveic data mart atiestatīšana?

Ja uz jūsu situāciju attiecas viens vai vairāki no šiem priekšrakstiem, jūsu organizācija var gūt labumu no data mart atiestatīšanas:

- Programmu datu bāze ir atjaunota.
- Jūs esat atvēris atbalsta biļeti, un atbalsta inženieris ir norādījis, ka jūs atiestatīt data mart kā daļu no problēmu novēršanas soļa.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Kad data mart atiestatīšana nav piemērota?

Tālāk ir norādīti daži apstākļi, kad nav ieteicams atiestatīt data mart:

- Jūs saskaraties ar datu sinhronizāciju saistītās veiktspējas problēmām.
- Jums ir periodiska atiestatīšanas shēma šādu iemeslu dēļ:

    - **Trūkst datu** – ja ievērojat, ka trūkst datu, atveriet atbalsta biļeti ar Microsoft, lai pārskatītu savu pārskata formātu un iespējamās datu sinhronizācijas problēmas.
    - **Iesprūdis integrācijas stāvoklis**
    - **Novecojuši ieraksti** – novecojuši ieraksti paši par sevi neattaisno data mart atiestatīšanu. Ja ir iestatīta liela datu kopa, atiestatīšanas process var ilgt kādu laiku, bet maz ticams, ka tas novedīs pie kaut kādiem uzlabojumiem.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Ja atiestatīšu datu mart, vai zaudēšu pārskatus, ko es jau esmu izveidojis?

Nē. Jūsu pārskati tiek glabāti SQL tabulās, kuras neietekmē data mart atiestatīšana. Ja jums ir bažas par savu izstrādāto ziņojumu zaudēšanu, varat dublēt noformējumus, kurus nevēlaties zaudēt. Lai tos dublētu veidotājus, atveriet Pārskatu veidotāju un dodieties uz **Uzņēmums \> Uzņēmumi \> Veidošanas bloki \> Eksports**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Vai visiem lietotājiem ir jāiziet no sistēmas, pirms var atiestatīt data mart?

Nē. Lietotāji var turpināt darbu sistēmā data mart atiestatīšanas laikā. Tomēr, kamēr atiestatīšana nav pabeigta, lietotāji nevarēs piekļūt nevienam pārskatam, kas tika izveidoti, izmantojot finanšu pārskatu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
