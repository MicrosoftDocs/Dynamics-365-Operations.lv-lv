---
title: Finanšu kalendāri, finanšu gadi un periodi
description: Šajā rakstā ir aprakstīti finanšu kalendāri, finanšu gadi un periodi, kā arī to lietošana juridiskajām personām, pamatlīdzekļiem un budžeta veidošanai.
author: aprilolson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: roschlom
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 795c884cf429b2a212d6c874b3b7634d6cd10c71
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210171"
---
# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Finanšu kalendāri, finanšu gadi un periodi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti finanšu kalendāri, finanšu gadi un periodi, kā arī to lietošana juridiskajām personām, pamatlīdzekļiem un budžeta veidošanai.

Finanšu kalendāri nodrošina struktūru organizācijas finanšu aktivitātei. Katrs finanšu kalendārs satur vienu vai vairākus finanšu gadus, un katrs finanšu gads satur vairākus periodus. Finanšu kalendāri var būt balstīti uz kalendāra gadu no 1. janvāra līdz 31. decembrim vai jebkādiem jūsu izvēlētiem datumiem. Piemēram, dažas organizācijas izvēlas finanšu kalendāru, kas sākas viena gada 1. jūlijā un beidzas nākamā gada 30. jūnijā. 

Finanšu kalendāru skaits, ko varat izveidot, nav ierobežots, un finanšu gadu skaits, ko var izveidot finanšu kalendāram, arī nav ierobežots. Katram finanšu kalendārs ir neatkarīgs no jūsu organizācijai, un to var izmantot vairākas juridiskās personas organizācijā. Piemēram, organizācijai ir astoņas nodaļas un katra nodaļa ir atsevišķa juridiska persona. Piecas no tām koplieto vienu finanšu kalendāru, un trīs izmanto dažādus finanšu kalendārus. Jūs varat izveidot vienu finanšu kalendāru piecām juridiskajām personām, kas koplieto vienu un to pašu finanšu kalendāru, un pēc tam izveidot atsevišķus finanšu kalendārus pārējām juridiskajām personām.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Izveidot finanšu kalendārus, finanšu gadus un periodus
Finanšu kalendārus, finanšu gadus un periodus varat izveidot un dzēst lapā Finanšu kalendāri. Varat arī sadalīt esošos periodus un veidot slēgšanas periodus, ko var izmantot finanšu gada slēgšanai. 

Slēgšanas periods tiek lietots, lai dalītu Virsgrāmatas darījumus, kas tiek ģenerēti, kad finanšu gads tiek slēgts. Ja slēgšanas darījumi ir vienā finanšu periodā, ir vieglāk izveidot finanšu pārskatus, kas iekļauj vai izslēdz dažādu veidu slēgšanas ierakstus. Ja finanšu gads ir sadalīts 12 finanšu periodos, slēgšanas periods parasti ir 13. periods. Taču slēgšanas periodu var izveidot no jebkura perioda, kura statuss ir Atvērts. 

Kad veidojat slēgšanas periodu, atlasiet kādu periodu, kura statuss ir Atvērts un kuram ir datumi, ko vēlaties izmantot. Jaunais slēgšanas periods kopēs esošā perioda sākuma un beigu datumu. Sākotnējais periods turpinās pastāvēt. Piemēram, jūs atlasāt 12. periodu, kas ir pēdējais finanšu gada periods un kurā ir ietverti datumi no 1. augusta līdz 31. augustam. Jūs ievadāt slēgšanas perioda nosaukumu, piemēram “Slēgšana”. Kad esat izveidojis jaunu slēgšanas periodu, jums ir sākotnējais periods un slēgšanas periods. Abiem datumi sākas 1. augustā un beidzas 31. augustā.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Atlasīt finanšu kalendārus Virsgrāmatām, pamatlīdzekļiem un budžeta cikliem
Finanšu kalendāri tiek izmantoti ar pamatlīdzekļu nolietojumu, finanšu transakcijām un budžeta cikliem. Veidojot finanšu kalendāru, varat to izmantot vairākiem nolūkiem. Atlasīt var pamatlīdzekļu grāmatas finanšu kalendāru, lai padarītu to par pamatlīdzekļu kalendāru. Varat atlasīt finanšu kalendāru Virsgrāmatai, lai padarītu to par Virsgrāmatas kalendāru. Varat arī atlasīt finanšu kalendāru budžeta ciklam, lai padarītu to par budžeta kalendāru. Varat izmantot vienu un to pašu finanšu kalendāru visiem šiem nolūkiem.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Atlasīt finanšu kalendāru savai juridiskajai personai

Formā Virsgrāmata atlasiet finanšu kalendāru, ko vēlaties izmantot virsgrāmatai savai juridiskajai personai. Lapā Virsgrāmata finanšu kalendārs ir jāatlasa katrai juridiskajai personai. Kad finanšu kalendārs ir atlasīts, lapā Virsgrāmatas kalendārs varat iestatīt periodu statusus un atļaujas jebkuriem periodiem, kas ir daļa no finanšu gada.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Atlasīt finanšu kalendāru pamatlīdzekļiem

Atlasīt var pamatlīdzekļu grāmatas finanšu kalendāru, un šis finanšu kalendārs tiks izmantots pamatlīdzekļiem, kas lieto atlasīto grāmatu. Varat atlasīt no jebkura finanšu kalendāra, kas ir definēts lapā Finanšu kalendāri.

### <a name="define-budget-cycle-time-spans"></a>Definēt budžeta cikla laika posmus

Budžeta cikli ir laika posms, kurā tiek izmantots budžets. Budžeta cikli var saturēt daļu no finanšu gada vai vairākiem finanšu gadiem, piemēram, divgadīgs budžeta cikls ar diviem gadiem vai trīsgadīgs budžeta cikla ar trīs gadiem. Budžeta cikla laika posms nosaka budžeta ciklā iekļauto periodu skaitu. Lai norādītu budžeta cikla laika posmu, izmantojiet lapu Budžeta cikla laika posmi.

## <a name="maintain-periods-for-your-organization"></a>Uzturēt jūsu organizācijas periodus
Lapu Virsgrāmatas kalendārs varat izmantot, lai apskatītu detalizētu informāciju par savas organizācijas izmantoto finanšu kalendāru, finanšu gadiem un periodiem. Varat arī mainīt periodu statusu un atlasīt lietotājus, kuriem atļauts grāmatot uzskaites transakcijas periodos. Piemēram, jauna perioda sākumā jūs, iespējams, vēlaties, lai kāda lietotāju grupa pabeidz finanšu darījumu grāmatošanu iepriekšējā periodā, bet citas grupas strādā tikai jaunajā periodā.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]