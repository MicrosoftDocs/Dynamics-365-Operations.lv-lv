---
title: Data mart atiestatīšanas BUJ
description: Šajā rakstā ir sniegtas atbildes uz dažiem bieži uzdotiem jautājumiem par datu martu atiestatījumiem.
author: jinniew
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d2b20ec7af9f0c6b7899617c2b8fdbf0992d7397
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892397"
---
# <a name="data-mart-resets-faq"></a>Data mart atiestatīšanas BUJ

Šajā rakstā ir sniegtas atbildes uz dažiem bieži uzdotiem jautājumiem par datu martu atiestatījumiem. Data mart atiestatīšana var būt laikietilpīgs process un atkarībā no apstākļiem var nebūt nepieciešamais risinājums. Tāpēc šis raksts ietver informāciju par apstākļiem, kuros datu martu atiestatīšana var palīdzēt, un arī apstākļus, kad maz ticams, ka palīdz.

## <a name="what-is-a-data-mart-reset"></a>Kas ir data mart atiestatīšana?

Data marta atiestatīšana atspējos integrācijas uzdevumus, izdzēsis visus data mart datus un tad atkārtoti aktivizēs integrāciju.

Lai nodrošinātu, ka vecie dati netiek ievietoti, data mart atiestatīšanu var sākt tikai pēc esošo uzdevumu pabeigšanas. Ja mēģināsit atiestatīt data mart pirms visu uzdevumu pabeigšanas, iespējams, saņemsit ziņojumu, tādu kā "Data mart atiestatīšanu nevarēja apstrādāt aktīva uzdevuma dēļ. Lūdzu, vēlāk mēģiniet vēlreiz.”

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Kad jāveic data mart atiestatīšana?

Ja uz jūsu situāciju attiecas viens vai vairāki no šiem priekšrakstiem, jūsu organizācija var gūt labumu no data mart atiestatīšanas:

- **Programmas datu bāze ir atjaunota**
- **Jūs atvērāt atbalsta biļeti** - atbalsta inženieris instruēja jums atiestatīt datu martu kā daļu no problēmu novēršanas soļa.
- **Liels novecojušu ierakstu procentuālais** daudzums — novecojuši ieraksti paši par sevi ne vienmēr var attaisnot datu martu atiestatīšanu. Novecojušu datu augstā procentuālā vērtība var mazināt vispārējā pārskata izveides un integrācijas veiktspēju un izraisīt papildu datu bāzes vietas izmantošanu. Ieteicams pabeigt datamart atiestatīšanu, lai noņemtu novecojušus datus, ja datu martā ir vairāk par 80% novecojuši dati.
 
> [!NOTE]
> Datu apstrādes atiestatīšanas procesu ietekmē virsgrāmatas un budžeta darbību skaits jūsu datu bāzē. Atkarībā no jūsu sistēmā veikto darbību skaita datu apstrādes atiestatīšanu var veikt ilgt no 15 minūtēm līdz pat četrām stundām. Tomēr, ja atiestatīšanas process ilgst vairāk nekā četras stundas, ieteicams sazināties ar atbalsta dienestu.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Kad data mart atiestatīšana nav piemērota?

Tālāk ir norādīti daži apstākļi, kad nav ieteicams atiestatīt data mart:

- Jūs pašlaik saskaraties ar datu integrācijas veiktspējas jautājumiem.
- Jūsu finanšu pārskataētāja integrācija nav iespējota. 

    - Tas nozīmē, ka Virsgrāmatas dati vairs netiek sinhronizēti ar finanšu pārskata datummāru. Iespējams, jūsu finanšu pārskata uzstādītājs nesaņem datuma numurus jūsu finanšu pārskatos. Tas parasti notiek, ja finanšu pārskatu izveidotājs netiek lietots ilgstoši.
    - Jums tiks piedāvāts iespējot integrāciju, no jauna atiestatot datu martu. Varat turpināt, atlasot **Jā**. Varat arī izvēlēties vēlāk atiestatīt datu martu. Pēc integrācijas iespējošanas virsgrāmatas dati tiek sinhronizēti finanšu pārskatuētājā vēlreiz. 
- Jums ir periodiska atiestatīšanas shēma šādu iemeslu dēļ:

    - **Pārskatā trūkst datu vai tas ir** negaidīts – ja ievērojat, ka trūkst datu, atveriet atbalsta biļeti ar Microsoft, lai pārskatītu jūsu pārskata formātu un iespējamās datu sinhronizācijas problēmas.
    - **Pielīmēšanas** integrācijas stāvoklis - Ja ievērojat, ka integrācijas statuss darbībā tiek pielīmēts, tas var būt tādēļ, ka sistēmā ir liels darbību apjoms. Šis stāvoklis tiks atrisināts pats. Tomēr, ja vairāk nekā četras stundas ievērojat ierašanās statusu, atveriet atbalsta biļeti sistēmai Microsoft. 
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Ja atiestatīšu datu mart, vai zaudēšu pārskatus, ko es jau esmu izveidojis?

Nē. Jūsu pārskati tiek glabāti SQL tabulās, kuras neietekmē data mart atiestatīšana. Ja jums ir bažas par savu izstrādāto ziņojumu zaudēšanu, varat dublēt noformējumus, kurus nevēlaties zaudēt. Lai tos dublētu veidotājus, atveriet Pārskatu veidotāju un dodieties uz **Uzņēmums \> Uzņēmumi \> Veidošanas bloki \> Eksports**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Vai visiem lietotājiem ir jāiziet no sistēmas, pirms var atiestatīt data mart?

Nē. Lietotāji var turpināt darbu sistēmā data mart atiestatīšanas laikā. Tomēr, kamēr atiestatīšana nav pabeigta, lietotāji nevarēs piekļūt nevienam pārskatam, kas tika izveidoti, izmantojot finanšu pārskatu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
