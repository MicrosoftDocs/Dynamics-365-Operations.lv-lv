---
title: Laika un apmeklētības reģistrācijas pārskats
description: Laika reģistrācijas darbinieki var ievadīt dažādus laika reģistrācijas veidus, piemēram, ierašanās laiku, aiziešanas laiku, netiešu aktivitāšu un kavējumu reģistrāciju. Šajā tēmā ir aprakstīta reģistrācija, tās aprēķināšana, apstiprināšana un darbplūsmas izmantošana, lai pievienotu struktūru un automātisko apstiprināšanu darba laika uzskaites tabulu apstiprināšanas procesam.
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr, JmgRegistrationSetup, JmgStampTrans, JmgStampJournalTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "53351"
- intro-internal
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0755a22365a2fdcbc6ed06c7e85c47d86808912e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567971"
---
# <a name="time-and-attendance-registration-overview"></a>Laika un apmeklētības reģistrācijas pārskats

[!include [banner](../includes/banner.md)]

Laika reģistrācijas darbinieki var ievadīt dažādus laika reģistrācijas veidus, piemēram, ierašanās laiku, aiziešanas laiku, netiešu aktivitāšu un kavējumu reģistrāciju. Šajā tēmā ir aprakstīta reģistrācija, tās aprēķināšana, apstiprināšana un darbplūsmas izmantošana, lai pievienotu struktūru un automātisko apstiprināšanu darba laika uzskaites tabulu apstiprināšanas procesam.

## <a name="registrations"></a>Reģistrācijas

Uzņēmumos, kuros ir laika un apmeklētības reģistrācija, darbiniekiem ir jāreģistrē laiks, ko viņi pavada darbā, kā arī apmeklējums. Dažos uzņēmumos darbiniekiem jāreģistrē tikai laiks, ierodoties darbā un dodoties mājās. Citos uzņēmumos darbiniekiem var tikt pieprasīts reģistrētu arī laiku par faktiski veiktajām darbībām, kā arī pārtraukumu laiku. Laika un apmeklētības reģistrācijas lietotāji ir:

- Darbinieki, kuriem regulāri jāreģistrē laiks un apmeklējums, to darot katru dienu, ik nedēļu vai katru otro nedēļu.
- Supervizori, vadītāji un algu daļas darbinieki, kuri aprēķina, apstiprina un pārsūta darbinieka reģistrācijas tālākai apstrādei.

| **Piezīme.**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja veicat laika un apmeklētības reģistrāciju kopā ar ražošanas izpildi, visas reģistrācijas par projektiem, projektu aktivitātēm, netiešām aktivitātēm, kavējumu kodiem, virsstundām un brīvā režīma laiku tiks veiktas algas aprēķināšanai abos moduļos. |

## <a name="time-registrations-workers"></a>Darbinieku laika reģistrācija

Lai reģistrētu laiku un kavējumu, darbinieki jāiestata kā uzņēmumā nodarbināti darbinieki ar laika reģistrāciju.

Pēc iestatīšanas darbinieku datus var ievadīt dažādu veidu reģistrācijās.

- Ierašanās darbā un aiziešanas no darba reģistrēšana.
- Laika un krājumu patēriņš ražošanas darbos.
- Laiks, kas izmantots, strādājot pie ražotnes iekārtas, ja iekārta ir definēta kā resurss.

| **Piezīme.**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darbiniekam var tik automātiski piešķirta laika reģistrācija, kas veikta par konkrētu darbu pie ražotnes iekārtas, ja darbinieks izvēlas strādāt kā asistents iekārtai, sākot ar ražošanas darbu. |

- Laika reģistrācija par projektiem un projektu aktivitātēm.
- Projekta izmaksu un krājumu patēriņa reģistrēšana, izmantojot attiecīgo projektu maksas žurnālus un projekta krājumu žurnālu.
- Plānotā prombūtne.
- Kavējums, ierodoties vēlu vai dodoties no darba agrāk, nekā plānots.
- Darba pārtraukumi, kas reģistrēti manuāli vai sistēmas automātiski aprēķināti.
- Netiešās aktivitātes, kas ir ārpus ražošanas cikla, un kuras darbinieks var veikt dienas laikā. Šo darbību piemēri ietver sapulces vai darbvietas uzkopšanu.
- Virsstundas, ko var reģistrēt kā papildstundas, brīvā režīma laiku vai virsstundas.

## <a name="adding-clock-out-registrations"></a>Aiziešanas no darba reģistrācijas pievienošana

Ja darbinieks aizmirst reģistrēt aiziešanu no darba darbdienas beigās, trūkstošo reģistrāciju var pievienot izpildot pakešuzdevumu. Sistēma salīdzinās ierašanās un aiziešanas reģistrācijas laiku saskaņā ar saistīto darbinieka profilu un automātiski ievietos trūkstošo aiziešanas no darba reģistrāciju atbilstoši profila beigu laikam. Ierašanās un aiziešanas no darba reģistrācija ir ļoti svarīga nākamajam reģistrāciju laika aprēķinam un apstiprināšanai pirms reģistrāciju pārsūtīšanas uz algu daļu.

## <a name="calculating-registrations"></a>Reģistrāciju aprēķināšana

Kad reģistrēšanas darbinieks tiek piešķirts aprēķinu grupai, kas parasti attiecas uz konkrētu komandu, maiņu vai darba grupu. Grupas vadītājs vai supervizors parasti validē darbinieku veiktās reģistrācijas, tāpēc viņš ir atbildīgs arī par attiecīgo aprēķina grupu ikdienas aprēķina veikšanu. Kā daļu no aprēķina procesa grupas vadītājs vai supervizors var:

- Labot kļūdainu reģistrāciju. Piemēram, mainīt pārslēgšanās kodus un pielāgot atsauksmes par ražošanas darbiem.
- Pievienot trūkstošās reģistrācijas. Piemēram, izveidojiet aiziešanas no darba reģistrācijas un kavējumu darbības.
- Dzēst nepareizas reģistrācijas.

Tā kā reģistrētais laiks jāpakārto darbinieka laika profilam pirms reģistrāciju aprēķināšanas, jums jāignorē darba laika profils jebkuram darbiniekam, kurš neatbilst standarta darba laika profilam. Gadījumā, ja darbinieka profils ir dienas maiņa, un darbinieks ir piekritis strādāt nakts maiņā bez virsstundu apmaksas, grupas vadītājam vai supervizoram, lai aprēķinātu darba laiku atbilstoši standarta nakts likmei, nevis kā virsstundas, ir jāignorē noklusējuma darbinieka profils. Ja kavējuma reģistrācija iztrūkst, aprēķinā tiks arī parādīta kļūda. Tā jāpievieno pirms aprēķina pabeigšanas.

## <a name="approving-registrations"></a>Reģistrāciju apstiprināšana

Tāpat kā piešķīrāt reģistrācijas darbiniekam aprēķina grupu, jums jāpiešķir arī apstiprinājuma grupas. Grupa parasti attiecas uz komandu, maiņu vai darba grupu. Ir jāapstiprina pareizi aprēķinātās laika reģistrācijas — tas nozīmē, ka aprēķins jāveic bez kļūdām — pirms var ģenerēt apmaksas elementus, ko pēc tam varēs pārsūtīt uz algu sistēmu. Algu administrators parasti apstiprina reģistrācijas, un pirms apstiprināšanas viņš var:

- Ignorēt atsevišķu darbinieku apmaksas līgumus.
- Manuāli pievienot prēmijas.
- Ievadīt papildinformāciju par kavējuma reģistrācijām.

| **Piezīme.**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja konkrētiem darbiniekiem ir aprēķinātas virsstundas, tās var piešķirt par konkrētiem dienas laika darbiem. Tas jādara, ja darba izmaksas tiek aprēķinātas, pamatojoties uz darbinieka apmaksu. |

## <a name="approving-registrations-using-workflow"></a>Reģistrāciju apstiprināšana, izmantojot darbplūsmu

Ir iespējama iestatīt darbplūsmas apstiprināšanas procesu, kas automātiski apstiprinās reģistrācijas atbilstoši darbplūsmas kārtulām, atstājot tikai manuāli apstrādājamas atkāpes. Ja ir aktivizēta darbplūsmas apstiprināšana, grupas vadītājs vai supervizors iesniedz aprēķinātās reģistrācijas apstiprināšanai. Darbplūsmas process ģenerēs atbilstošus apstiprinājumus un uzdevumus, un pēc tam piešķirs tos attiecīgiem lietotājiem un lomām, kā tas norādīts darbplūsmā. Uz laika un apmeklējuma reģistrāciju attiecas divi darbplūsmas apstiprinājuma veidi.

| Darbplūsma                                  | Mērķis                                                                                                   | Reģistrācijas veids                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kopējais laika un apmeklētības dienu daudzums            | Darbplūsma var validēt reģistrācijas atbilstoši paredzamajam dienas darba stundu skaitam. |                                                                                                                                                                                                                                                       |
| Laika un apmeklētības žurnāla reģistrācija. | Darbplūsma validē katru reģistrācijas tipu atbilstoši reģistrācijas datumam.                           | Laiks un apmeklētība • Ierašanās • Aiziešana • Kavējumi • Pārtraukums • Pārslēgšanās kods • Projekts • Projekta aktivitāte • Netiešās aktivitātes ražošanas darbi • Gaidīšana pirms • Iestatīšana • Process • Pārklāšanās • Transportēšana • Gaidīšana pēc • Sākt palīdzību • Apturēt palīdzību |

## <a name="transferring-approved-registrations"></a>Apstiprināto reģistrāciju pārsūtīšana

Pēc reģistrāciju apstiprināšanas tās var pārsūtīt uz periodisko algas darbu. Pārsūtītā reģistrācija tiek grāmatota aktivitātē vai darbā, kas tas saistīts ar, piemēram, ražošanas pasūtījumu vai projektu. Pamatojoties uz reģistrācijām, katram darbiniekam tiek ģenerētas algas transakcijas.  

## <a name="reversing-transferred-registrations"></a>Pārsūtīto reģistrāciju atcelšana

Atcelto darbību uzdevumu — darbību anulēšanu — var veikt līdz laikam, kad izpildei ir jāpalaiž algas perioda apmaksas pārsūtīšana. Tas nozīmē, ka algu dati ir pārsūtīti uz ārēju failu. Pēc atcelšanas visas reģistrācijas tiek izņemtas un visas darbības, kas grāmatotas konkrētos ražošanas pasūtījumos vai projektos, tiek nobīdītas un neitralizētas.

| **Piezīme.**                                                 |
|----------------------------------------------------------|
| Ārējo failu var importēt uz algu sistēmu. |

## <a name="registrations-in-electronic-timecards"></a>Reģistrācija elektroniskās darba laika uzskaites kartēs

Darbinieki ar darba uzdevumiem, kuriem nav nepieciešamas tūlītējas atsauksmes, kā gadījumā ar ražošanas darbiem, bet, kas strādā pie projekta aktivitātēm, var gūt labumu no elektronisko darba laika uzskaites karšu lietošanas. Elektroniskās darba laika uzskaites kartes ļauj ievadīt reģistrāciju jebkurā laikā un atbilstoši jūsu biznesa grafikam — katru dienu, katru nedēļu vai kad darbinieks atkal ierodas birojā. Lai izmantotu darba laika uzskaites kartes vai šos darbiniekus, jums jānorāda darba laika uzskaites kartes lietošana informācijā par darbinieku. Elektroniskās darba laika uzskaites kartes ļauj darbiniekam reģistrēt turpmāk norādīto.

- Datums
- Reģistrācijas veids
- Darba atsauce, piemēram, projekts, netieša aktivitāte vai ražošanas pasūtījums
- Darba kods
- laika patēriņš.
- Projekta papildmaksa
- Projekta krājumi

[!INCLUDE[footer-include](../../includes/footer-banner.md)]