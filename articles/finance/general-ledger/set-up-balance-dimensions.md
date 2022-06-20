---
title: Kā var iestatīt līdzsvarošanas finanšu dimensijas?
description: Šajā rakstā aprakstītas opcijas līdzsvarošanas finanšu dimensijas funkcijas iestatīšanai un izmantošanai.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: dd859629b0eb9f14fa4907699613382f3897d21d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878017"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Kā var iestatīt līdzsvarošanas finanšu dimensijas?

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstītas opcijas līdzsvarošanas finanšu dimensijas funkcijas iestatīšanai un izmantošanai.

## <a name="symptom"></a>Simptoms

Ir divas opcijas līdzsvarošanas finanšu dimensiju iestatīšanai. Pirmā opcija ir izmantot lauku **Līdzsvarošanas finanšu dimensija** iestatījuma lapā **Virsgrāmata** (**Virsgrāmata \> Virsgrāmatas iestatījums \> Virsgrāmata**). Otra opcija ir izmantot lauku **Pieprasīt, lai dimensija būtu līdzsvarota** lapā **Finanšu dimensijas** (**Virsgrāmata > Kontu plāns \> Dimensijas \> Finanšu dimensijas**). Šis raksts skaidro atšķirību starp šīm divām opcijām.

## <a name="resolution"></a>Novēršana

Organizācijas parasti izmanto līdzsvarošanas dimensijas, lai ģenerētu bilanci, kas ir līdzsvarota finanšu dimensijas līmenī. Iespējojot jebkuru līdzekli, iegrāmatotās, nelīdzsvarotās dimensijas netiks līdzsvarotas. Vispirms ir manuāli jāievada pielāgošanas ieraksti, lai bilance būtu līdzsvarota pirms kāda no līdzekļu iespējošanas.

Abas opcijas ir savstarpēji izslēdzošas. Opcijai, kuru izmanto jūsu organizācija, jābūt pamatotai ar jūsu uzņēmuma prasībām. Bieži dzirdam par debitoriem, kas definē līdzsvarošanas dimensiju gan Virsgrāmatas iestatījumos, gan finanšu dimensijas iestatījumos, un pēc tam pabeidz dažus vai visus nepieciešamos papildu iestatījumus. Tomēr tie joprojām nevar grāmatot, jo finanšu dimensijas līmenī pastāv nelīdzsvarotība.

Šajās sadaļās aprakstītas divas opcijas un skaidrots, kā tās iestatīt.

### <a name="ledger--balancing-financial-dimension"></a>Virsgrāmata – Līdzsvarošanas finanšu dimensija

Līdzsvarošanas dimensija iestatīšanas lapā **Virsgrāmata** tiek izmantota, lai iespējotu starpvienību uzskaiti. Lai ieslēgtu funkcionalitāti, rīkojieties šādi.

1. Nosakiet, kura finanšu dimensija būs līdzsvarošanas dimensija.

    - Šī funkcionalitāte ļauj izvēlēties tikai vienu finanšu dimensiju kā līdzsvarošanas dimensiju.
    - Neatlasiet vēl dimensiju iestatījumu lapā **Virsgrāmata**.
    - Pārliecinieties, vai bilance atlasītajai finanšu dimensijai jau ir līdzsvarota.

2. Atjauniniet konta struktūru līdzsvarošanas finanšu dimensijai.

    - Līdzsvarošanas finanšu dimensija ir jāiekļauj visās virsgrāmatai piešķirtajās kontu struktūrās.
    - Finanšu dimensija nedrīkst atļaut tukšas vērtības konta struktūrā. Šis ierobežojums nodrošina, ka katrs Virsgrāmatā iegrāmatotais uzskaites ieraksts satur finanšu dimensijas vērtību. Ja tiek izmantotas līdzsvarošanas dimensijas, tukša dimensija nav derīga.

3. Lapā **Konti utomātiskām darbībām** (**Virsgrāmata \> Grāmatošanas iestatījums \> Konti automātiskām darbībām**) definējiet starpvienumu debeta un kredīta galvenos kontus.
4. Iestatījuma lapā **Virsgrāmata** (**Virsgrāmata \> Virsgrāmatas iestatījums \> Virsgrāmata**), laukā **Līdzsvarošanas finanšu dimensija** atlasiet finanšu dimensiju, ko izmantot līdzsvarošanai.

Ja atlasītā finanšu dimensija netiek līdzsvarota, kad darbības tiek ievadītas un grāmatotas, sistēma automātiski pievienos debeta vai kredīta ierakstus, kas ir nepieciešami grāmatvedības ierakstu līdzsvarošanai grāmatošanas laikā. Starpvienumu darbības debeta un kredīta virsgrāmatas konti tiek parādīti virsgrāmatā grāmatotajā dokumentā. Tomēr tās netiks rādītas žurnālos vai pirmdokumentos, kam tika grāmatoti uzskaites ieraksti.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Finanšu dimensijas – pieprasīt, lai dimensija tiktu līdzsvarota

Lai gan līdzsvarošanas dimensija lapā **Finanšu dimensijas** parasti izmanto valsts sektora uzņēmumi, funkcionalitāte nav saistīta ne ar vienu valsts sektora konfigurācijas atslēgu. Tā kā sistēmā nav ierobežojumu, šo funkcionalitāti var izmantot pat tad, ja jūsu organizācija nav valsts sektora iestāde.

Šī funkcionalitāte parasti tiek izmantota valsts sektora debitoru bāzē, jo tai ir nepieciešams, lai šīs grāmatošanas definīcijas tiek izmantotas katras darbības automātiskai līdzsvarošanai. Tas neizmanto starpvienumu debeta un kredīta kontus, kas ir definēti lapā **Konti automātiskām darbībām**, lai automātiski līdzsvarotu uzskaites ierakstus. Ja uzskaites ieraksts dimensiju līmenī netiek līdzsvarots pēc grāmatošanas definīciju lietošanas, darbība netiks grāmatota, pat ja ir definēti starpvienumu debeta un kredīta konti.

Bieži dzirdam par debitoriem, kas definē korespondējošo dimensiju gan Virsgrāmatas iestatījumos, gan finanšu dimensiju iestatījumos. iestatījumā. Šajā gadījumā sistēma izmanto finanšu dimensiju funkcionalitāti. Līdzsvarošanas dimensiju iestatījumam finanšu dimensijas līmenī grāmatošanas laikā ir prioritāte. Grāmatošana neizdosies, ja grāmatošanas definīcija neveido līdzsvarotu uzskaites ierakstu finanšu dimensijas līmenī.

Veiciet šīs darbības, lai ieslēgtu līdzsvarošanas dimensijas izmantošanu finanšu dimensijas līmenī.

1. Nosakiet, kuras finanšu dimensijas būs līdzsvarošanas dimensijas.

    - Vairāk nekā vienu finanšu dimensiju var iestatīt kā līdzsvarošanas dimensiju.
    - Vēl nav iestatītas finanšu dimensijas, kas būs nepieciešamas darbības līdzsvarošanai lapā **Finanšu dimensijas**.

2. Definējiet grāmatošanas definīcijas katram žurnāla vai pirmdokumenta tipam, ko izmanto jūsu organizācija. Grāmatošanas definīcijas patērē Virsgrāmatas kontus no negrāmatota žurnāla vai pirmdokumenta kā "atbilstība kritērijiem". Pēc tam grāmatošanas definīcija atgriež "ģenerētos ierakstus", kas kļūst par uzskaites ierakstu. Ja grāmatošanas definīcija ir pareizi iestatīta, ģenerētais ieraksts ietver atbilstības kritēriju Virsgrāmatas kontus un papildu kontus, lai līdzsvarotu uzskaites ierakstu dimensiju līmenī. Papildinformāciju skatiet tēmā [Grāmatošanas definīcijas](posting-definitions.md). 
   
   Grāmatošanas definīcijas netiek atbalstītas katram darbības veidam. Piemēram, grāmatošanas definīcijas nevar definēt nevienai darbībai, kas ievadīta Virsgrāmatas žurnālā vai pamatlīdzekļu žurnālā. Ja žurnālam vai pirmdokumentam nevar definēt grāmatošanas definīciju, darbība ir manuāli jālīdzsvaro pie finanšu dimensijas vērtības. Piemēram, ja ir veikts virsgrāmatas žurnāla ieraksts un dimensija Nodaļa ir līdzsvarošanas dimensija, ir jānodrošina, lai katra nodaļas vērtība būtu līdzsvarota.  Ja dimensija netiek līdzsvarota katrai nodaļas vērtībai, dokuments netiks grāmatots, kamēr bilance netiek izlabota, manuāli pievienojot dokumentam starpvienumu debetu vai kredītu. 

    > [!IMPORTANT]
    > Ja manuāli jālīdzsvaro liels darbību skaits, **nevajadzētu** izmantot līdzsvarošanas dimensijas funkcionalitāti lapā **Finanšu dimensijas**. Tā vietā izmantojiet līdzsvarošanas dimensijas funkcionalitāti iestatījuma lapā **Virsgrāmata**.

3. Pēc tam, kad ir definētas grāmatošanas definīcijas, finanšu dimensijas var atzīmēt, kā nepieciešams līdzsvarošanai.

Ievadot un grāmatojot darbības, grāmatošanas laikā tiek izsauktas grāmatošanas definīcijas, lai noteiktu uzskaites ierakstus. Ja finanšu dimensijas ir līdzsvarotas, apstiprināšana notiek pēc uzskaites ierakstu apstiprināšanas. Ja finanšu dimensijas nav līdzsvarotas, darbība netiks grāmatota un tiks nosūtīts paziņojums, ka debeti nav vienādi ar noteiktas dimensijas kredītiem.
