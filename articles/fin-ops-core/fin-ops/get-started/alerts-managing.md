---
title: Brīdinājumu pakešveida apstrāde
description: Šajā rakstā ir sniegta informācija par brīdinājumu pakešveida apstrādi.
author: RichdiMSFT
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: ba17ebe1bdd95b8780b99b8f82b566bf527aca89
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860073"
---
# <a name="batch-processing-of-alerts"></a>Brīdinājumu pakešveida apstrāde

[!include [banner](../includes/banner.md)]

Brīdinājumu apstrādei tiek izmantota pakešveida apstrādes funkcionalitāte. Pirms procesa un piegādes brīdinājumiem ir jāiestata pakešveida apstrāde.

Pakešapstrādes funkcionalitāte atbalsta divus notikumu tipus:

- Notikumi, kurus izraisa ar izmaiņām saistīti notikumi. Šos notikumus dēvē arī par izveidošanas/dzēšanas un atjaunināšanas notikumiem.
- Termiņu izraisītie notikumi.

Pakešveida apstrādi var iestatīt abiem notikumu veidiem.

## <a name="batch-processing-for-change-based-events"></a>Ar izmaiņām saistītu notikumu pakešveida apstrāde

Sistēma nolasa visus ar izmaiņām saistītos notikumus, kas ir radušies pēc pēdējās izpildītās pakešveida apstrādes. Uz izmaiņām balstītie notikumi iekļauj lauku, ierakstu dzēšanas un ierakstu veidošanas atjauninājumus. Šie notikumi tiek salīdzināti ar brīdinājuma kārtulās iestatītajiem nosacījumiem. Ja notikums atbilst kārtulas nosacījumiem, pakešveida apstrāde ģenerē brīdinājumu.

### <a name="frequency-for-change-based-events"></a>Ar izmaiņām saistīto notikumu biežums

Notikumiem, kas pamatoti uz izmaiņām, var iestatīt pakešuzdevumu, kas izraisa notikuma apstrādi drīz pēc tam, kad sistēma ir pieteikusi notikumu. Ja pakešuzdevuma iestatījums nosaka tā biežāku atkārtošanu, lietotāji saņem brīdinājumus ātrāk, ja tiek veiktas izmaiņas. Tomēr bieža pakešveida apstrādes veikšana var negatīvi ietekmēt sistēmas veiktspēju.

No otras puses, pakešuzdevums, kas tiek izpildīts retāk un kura izpilde ir ieplānota, kad sistēmas noslodze ir zema, var palīdzēt uzlabot sistēmas veiktspēju. Tomēr reti izpildīta pakešveida apstrāde var neatbilst lietotāju prasībām par savlaicīgu brīdinājumu saņemšanu.

Tāpēc, iestatot ar izmaiņām saistīto notikumu pakešveida apstrādes izpildes biežumu, ir jāsaglabā līdzsvars starp brīdinājumu parādīšanas savlaicīgumu un visas sistēmas veiktspēju. Šiem ieteikumiem ir lielāka nozīme, ja palielinās to lietotāju skaits, kuri veido brīdinājuma kārtulas. Biežums neietekmē apstrādājamo notikumu skaitu. Tomēr, ja lielāks skaits lietotāju izveido kārtulas, jāveic vairāk pārbaužu. Šis datu apmaiņas veids var ietekmēt sistēmas veiktspēju.

#### <a name="the-risks-of-low-batch-frequency"></a>Zema pakešuzdevumu biežuma risks

Ja tiek iestatīts ar notikumiem saistītā pakešveida apstrādes zems izpildes biežums, ar brīdinājuma kārtulu nosacījumiem saistītie dati var tikt izmainīti pirms pakešuzdevums ir apstrādāts. Tāpēc brīdinājumi var tikt zaudēti.

Piemēram, brīdinājuma kārtula ir iestatīta aktivizēt brīdinājumu, ja notikums ir **debitora kontaktinformācijas izmaiņas** un nosacījums ir **debitors = BB**. Citiem vārdiem sakot, ja debitora BB kontaktinformācija tiek mainīta, tiek reģistrēts notikums. Tomēr pakešveida apstrādes sistēma tiek iestatīta tā, ka pakešveida apstrāde notiek retāk nekā datu ievade. Ja debitora nosaukums tiek mainīts no **BB** uz **AA**, pirms notikums ir apstrādāts, dati datu bāzē vairs neatbilst kārtulas nosacījumam, kur **debitors = BB**. Tādēļ, veicot galīgo notikuma apstrādāti, brīdinājums netiek ģenerēts.

### <a name="set-up-processing-for-change-based-alerts"></a>Uz izmaiņām pamatoto brīdinājumu apstrādes iestatīšana

1. Dodieties uz sadaļu **Sistēmas administrēšana** &gt; **Periodiskie uzdevumi** &gt; **Brīdinājumi** &gt; **Mainīt saistītos brīdinājumus**.
2. Dialoglodziņā **Mainīt saistītos brīdinājumus** ievadiet attiecīgo informāciju.

## <a name="batch-processing-for-due-date-events"></a>Ar izpildes datumu saistītu notikumu pakešveida apstrāde

Sistēma nosaka visus notikumus, kuru aktivizēšana saistīta ar izpildes datumiem, un šie notikumi tiek salīdzināti ar brīdinājumu kārtulās iestatītajiem nosacījumiem. Pakešveida apstrāde ģenerē brīdinājumu, ja notikums atbilst kārtulas nosacījumiem.

### <a name="frequency-for-due-date-events"></a>Ar izpildes datumu saistītu notikumu biežums

Ar izpildes datumu saistītiem notikumiem, iespējams, jāiestata pakešuzdevumi, kas tiek izpildīti pa nakti vai īpašā dienas laikā, lai līdzsvarotu sistēmas noslodzi. Mēs iesakām iestatīt pakešuzdevumu tā, lai tas tiek izpildīts vismaz vienu reizi dienā. Ja brīdinājumi ir jānosūta iespējami ātrāk, iestatiet pakešveida apstrādi tā, lai tā tiek nekavējoties izpildīta, tiklīdz tiek mainīti sistēmas dati. Ja vēlaties ģenerēt brīdinājumus par ar izpildes datumu saistītiem notikumiem, kuri notiek pēc tam, kad pakešuzdevums jau ir apstrādājis brīdinājumus, pakešuzdevumu var izpildīt vēlreiz tajā pašā dienā.

Piemēram, pakešuzdevums jau ir izpildīts konkrētā dienā. Pēc tam var izveidot pirkšanas pasūtījumu, kura izpildes datumam ir jāaktivizē brīdinājums tajā pašā dienā. Lai saņemtu brīdinājumu šajā dienā, pakešuzdevums ir jāizpilda vēlreiz, kad pirkšanas pasūtījums ir izveidots. Tomēr, ja pakešuzdevums netiek izpildīts šajā dienā vēlreiz, nākamās dienas pakešuzdevums nosaka ar izpildes datumu saistītus notikumus, kas nav apstrādāti iepriekšējās dienās.

> [!NOTE]
> Arī tad, ja pakešveida apstrāde tiek izpildīta biežāk nekā vienu reizi dienā, brīdinājumi vienam ar izpildes datumu saistītam notikumam un tiem pašiem nosacījumiem netiek ģenerēti divas reizes. Brīdinājumi tiek ģenerēti tikai tiem datumiem, kuri ir kļuvuši par izpildes datumiem to izmaiņu dēļ, kuras notikušas sistēmā pēc pēdējā pakešuzdevuma izpildes.

### <a name="batch-processing-window"></a>Pakešveida apstrādes logs

Brīdinājuma kārtulu apstrādi uzņēmumā var apturēta vairāku iemeslu dēļ. Šie iemesli ir, piemēram, brīvdienas, sistēmas kļūdas vai citi gadījumi, kas ierobežo pakešuzdevumu izpildi uz kādu laiku.

Lai novērstu ar izpildes datumu saistīto brīdinājumu novecošanu tāpēc, ka pakešuzdevums nav izpildīts vairākas dienas, var iestatīt pakešveida apstrādes logu. Pakešveida apstrādes logu var izmantot, lai novērstu pakešuzdevuma izpildi noteiktu dienu skaitu.

Ja tiek iestatīts pakešveida apstrādes logs, apstrādājot brīdinājuma kārtulu, tiek nosūtīts brīdinājums arī tad, ja brīdinājums pārsniedz laika ierobežojumu, kas ir definēts izpildes datuma kritērijos. Brīdinājums tiek sūtīts tik ilgi, līdz tiek pārsniegts šī laika ierobežojuma un pakešveida apstrādes logā noteiktais periods. Kad laika ierobežojuma un pakešveida apstrādes logā noteiktais periods ir pārsniegts, brīdinājums vairs netiek sūtīts.

### <a name="set-up-processing-for-due-date-alerts"></a>Apmaksas datuma brīdinājumu apstrādes iestatīšana

1. Dodieties uz sadaļu **Sistēmas administrēšana** &gt; **Periodiskie uzdevumi** &gt; **Brīdinājumi** &gt; **Ar izpildes datumu saistīti brīdinājumi**.
2. Dialoglodziņā **Ar izpildes datumu saistīti brīdinājumi** ievadiet attiecīgo informāciju.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
