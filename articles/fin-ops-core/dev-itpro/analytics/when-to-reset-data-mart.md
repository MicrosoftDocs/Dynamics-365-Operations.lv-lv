---
title: Kad atiestatīt data mart
description: Šajā tēmā uzskaitīti apstākļi, kas, iespējams, var tikt uzlaboti, no jauna atiestatot data mart, kas, maz ticams, ka palīdzēs.
author: jinniew
ms.date: 05/06/2021
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
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988996"
---
# <a name="when-to-reset-a-data-mart"></a>Kad atiestatīt data mart

Data mart atiestatīšana var būt laikietilpīga. Atkarībā no apstākļiem šī darbība var nebūt nepieciešamais risinājums. Šajā tēmā uzskaitīti apstākļi, kas, iespējams, var tikt uzlaboti, no jauna atiestatot data mart, kas, maz ticams, ka palīdzēs.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Kad nepieciešams veikt data mart atiestatīšanu?
Pirms data mart atiestatīšanas aplūkosim šādus jautājumus. Atbildot "jā" uz vienu vai vairākiem jautājumiem, var norādīt, ka jūsu organizācija var gūt labumu, atiestata data mart.

- Vai programmu datu bāze ir atjaunota?
- Ja esat atvēris atbalsta incidentu, un atbalsta inženieris ir norādījis, ka jūs atiestatīt data mart kā daļu no problēmu novēršanas soļa.
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Kad nav atbilstoši atiestatīt data mart?
Ir daži apstākļi, kad nav ieteicams atiestatīt data mart. Tie ietver. 

- Jūs saskaraties ar datu sinhronizāciju saistītās veiktspējas problēmām. 
- Ja periodisks atiestatīšanas modelis ir nepieciešams kāda no šo iemeslu dēļ: 
  - **Trūkst datu** 
  - **Iesprūdis integrācijas stāvoklis** 
  - **Novecojuši ieraksti** - novecojuši ieraksti paši par sevi neattaisno data mart atiestatīšanu. Ja ir iestatīta liela datu kopa, atiestatīšanas process var ilgt kādu laiku, bet maz ticams, ka tā rezultāts būs uzlabojums.
 
## <a name="what-is-a-data-mart-reset"></a>Kas ir data mart atiestatīšana?
- Atiestatīšana sāksies tikai tad, kad esošie uzdevumi būs pabeigti. Tas nodrošina, ka vecie dati netiek ievietoti. Šajā brīdī varat redzēt ziņojumu, piemēram, "Data mart atiestatīšanu nevarēja apstrādāt aktīva uzdevuma dēļ. Lūdzu, vēlāk mēģiniet vēlreiz."
- Atiestatīšana atspējos integrācijas uzdevumus un izdzēsīs visus data mart datus. Integrācijas atkārtota iespējošana.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Ja atiestatīšu datu mart, vai zaudēšu pārskatus, ko es jau esmu izveidojis? 
Nē, jūsu pārskati tiek glabāti SQL tabulās, kuras neietekmē data mart atiestatīšana. Ja jums ir bažas par savu izstrādāto ziņojumu zaudēšanu, varat dublēt noformējumus, kurus nevēlaties zaudēt. Lai tos dublētu, atveriet Pārskatu veidotāju un dodieties uz **Uzņēmums > Uzņēmumi > Veidošanas bloki > Eksports**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Vai visiem lietotājiem ir jāiziet no sistēmas, lai atiestatītu data mart?
Nē, lietotāji var turpināt darbu sistēmā data mart atiestatīšanas laikā. Tomēr viņi nevarēs piekļūt nevienam pārskatam, kas tika izveidoti finanšu pārskatā līdz atiestatīšanas pabeigšanai. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
