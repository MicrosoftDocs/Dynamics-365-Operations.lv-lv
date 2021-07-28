---
title: Pasūtījumu paziņojumu parādīšana pārdošanas punktā (POS)
description: Šajā tēmā ir aprakstīts, kā pārdošanas punktā iespējot pasūtījumu paziņojumu rādīšanu, un aprakstīta paziņojumu struktūra
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57f5d23533c2fd17593648a15745fa770fc01dc4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345212"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Pasūtījumu paziņojumu parādīšana pārdošanas punktā (POS)

[!include [banner](includes/banner.md)]

Veikala darbiniekiem var tikt piešķirti dažādi uzdevumi veikalā, piemēram, pasūtījumu aizpildīšana vai krājumu saņemšana vai krājumu uzskaites veikšana. Pārdošanas punkta (POS) klients nodrošina vienu programmu, kur veikala darbinieki vat tikt informēti par šiem uzdevumiem. Paziņojumu struktūra programmā POS atrisina šo problēmu, ļaujot mazumtirgotājiem konfigurēt paziņojumus atkarībā no lomām. Sākot ar programmas Dynamics 365 Retail 5. atjauninājumu šos paziņojumus var konfigurēt POS operācijām.

Sistēma var rādīt paziņojumus par operāciju *pasūtījuma izpilde*, un sākot ar Commerce versiju 10.0.18 paziņojumi var tikt rādīti arī operācijai *atsaukt pasūtījumu*. Tomēr struktūra ir veidota paplašināma, tādēļ izstrādātāji var [rakstīt paziņojumu apdarinātāju](dev-itpro/extend-pos-notification.md) jebkādai operācijai un parādīt paziņojumus par šīm operācijām POS.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Paziņojumu iespējošana pasūtījumu izpildes vai pasūtījuma atcelšanas operācijām

Lai iespējotu paziņojumus par pasūtījumu izpildes vai pasūtījuma atcelšanas operācijām, izpildiet tālāk aprakstītās darbības.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS \> Operācijas**.
1. Meklējiet operāciju **Pasūtījuma izpilde** vai **Atsaukt pasūtījumu** un pēc tam atlasiet **Iespējot paziņojumus**, lai norādītu, ka paziņojumu struktūrai jāņem vērā šīs operācijas apdarinātājs. Ja apdarinātājs ir ieviests, šīs operācijas paziņojumi tiks rādīti POS.
1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Darbinieki \> Darbinieki**.
1. Atlasiet cilni **Commerce**, atlasiet darbinieka rindu un pēc tam atlasiet **POS atļaujas**. Atlasiet kopsavilkuma cilni **Paziņojumi**, lai to izvērstu, un pēc tam pievienojiet operācijas, kurām iespējoti paziņojumi. Ja konfigurējot vienu paziņojumu darbiniekam, nodrošiniet, lai vērtība **Rādīšanas secība** būtu iestatīta uz **1**. Ja konfigurējot vairāk nekā vienu operāciju, iestatiet vērtības **Rādīšanas secība**, lai norādītu secību, kādā paziņojumi jāparāda. 

      Paziņojumi tiek rādīti tikai operācijām, kas ir pievienotas kopsavilkuma cilnē **Paziņojumi**. Operācijas varat pievienot tikai tad, ja lapā **POS operācijas** šīm operācijām ir atzīmēta izvēles rūtiņa **Iespējot operācijas**. Turklāt paziņojumi par šo operāciju tiek rādīti darbiniekiem tikai tad, ja operācija tiek pievienota šo darbinieku POS atļaujām.

    > [!NOTE]
    > Paziņojumus var ignorēt lietotāja līmenī. Lai to paveiktu, atveriet darbinieka ierakstu, atlasiet **POS atļaujas** un pēc tam rediģējiet lietotāja paziņojumu abonementu.

1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Laukā **Paziņošanas intervāls** norādiet, cik bieži paziņojumi jārāda. Dažiem paziņojumiem sistēmai POS ir jāveic reāllaika izsaukums grāmatvedības programmai. Šie zvani patērē grāmatvedības programmai nepieciešamo datora noslodzi. Tādēļ, iestatot paziņošanas intervālu, jāņem vērā gan uzņēmuma prasības, gan reāllaika izsaukumu grāmatvedības programmai ietekme. Vērtība **0** (nulle) izslēdz paziņojumus.
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**. Atlasiet grafiku **1060** (**Personāls**), lai sinhronizētu paziņojumu abonementa iestatījumus, un pēc tam atlasiet **Izpildīt tūlīt**. Tālāk sinhronizējiet atļaujas intervālu, atlasot **1070** (**Kanāla konfigurācija**), un pēc tam atlasiet **Izpildīt tūlīt**.

## <a name="view-notifications-in-the-pos"></a>Paziņojumu skatīšana programmā POS

Pēc visu darbību pabeigšanas darbinieki varēs skatīt paziņojumus programmā POS. Lai skatītu paziņojumus, POS augšējā labajā stūrī atlasiet paziņojuma ikonu. Tiek parādīts paziņojumu panelis, kas rāda paziņojumus par darbiniekam konfigurētajām operācijām. 

Operācijai **pasūtījuma izpilde** paziņojumu panelis parādīs tālāk minētās grupas.

- **Saņemšana veikalā** — šī grupa rāda to atsevišķo pasūtījumu rindu skaitu, kurus ir plānots saņemt pašreizējā veikalā. Varat atlasīt skaitu grupai, lai atvērtu operāciju **Pasūtījuma izpilde** ar filtru tā, ka tiek rādītas tikai aktīvo pasūtījumu rindas, kas ir iestatīti saņemšanai no pašreizējā veikala.
- **Nosūtīt no veikala** — šajā grupā ir norādīts to individuālo pasūtījumu rindu skaits, kas ir konfigurēti nosūtīšanai no lietotāja pašreizējā veikala. Varat atlasīt skaitu grupai, lai atvērtu operāciju **Pasūtījuma izpilde** ar filtrētu skatu tā, ka tiek rādītas tikai aktīvo pasūtījumu rindas, kas ir iestatīti nosūtīšanai no pašreizējā veikala.

Operācijai **atsaukt pasūtījumu** paziņojumu panelis parādīs tālāk minētās grupas.

- **Pasūtījumi izpildei** — šajā grupā ir parādīts to pasūtījumu skaits, kas ir konfigurēti vai nu saņemšanas vai nosūtīšanas izpildei lietotāja pašreizējam veikalam. Varat atlasīt skaitu grupā, lai atvērtu operāciju **Atsaukt pasūtījumu** ar filtrētu skatu, kas rāda tikai atvērtos pasūtījumus, kas lietotāja pašreizējam veikalam ir jāizpilda vai nu scenārijā saņemšana noliktavā, vai scenārijā nosūtīšana no veikala.
- **Pasūtījumi saņemšanai** — šī grupa rāda to pasūtījumu skaitu, kurus ir plānots saņemt pašreizējā veikalā. Varat atlasīt skaitu grupā, lai atvērtu operāciju **Atsaukt pasūtījumu** ar filtrētu skatu, kas rāda tikai atvērtos pasūtījumus, kas lietotāja pašreizējam veikalam ir jāizpilda, lai klients tos saņemtu no lietotāja pašreizējā veikala.
- **Pasūtījumi nosūtīšanai** — šajā grupā ir norādīts no lietotāja pašreizējā veikala nosūtāmo pasūtījumu skaits. Varat atlasīt skaitu grupā, lai atvērtu operāciju **Atsaukt pasūtījumu** ar filtrētu skatu, kas rāda tikai atvērtos pasūtījumus, kas lietotāja pašreizējam veikalam ir jāizpilda, lai tie tiktu nosūtīti no lietotāja pašreizējā veikala.

Gan pasūtījuma izpildes, gan pasūtījuma atsaukšanas paziņojumiem, kad process saņem jaunus pasūtījumus, paziņojumu ikona mainās, lai rādītu jaunos paziņojumus, un tiek atjaunināts atbilstošo grupu skaits. Kaut gan grupas tiek atsvaidzinātas regulāri, POS lietotāji var manuāli atsvaidzināt grupas jebkurā laikā, atlasot **Atsvaidzināt** blakus grupas nosaukumam. Visbeidzot, ja grupai ir jauns krājums, ko pašreizējais darbinieks nav skatījis, grupai parāda sprādziena simbols, kas norāda par jaunu saturu.

## <a name="enable-live-content-on-pos-buttons"></a>Reāllaika satura iespējošana uz POS pogas

Tagad uz POS pogas var parādīt skaitu, lai darbinieki varētu viegli noteikt, kādiem uzdevumiem nekavējoties jāpievērš uzmanība. Lai šo skaitu parādītu uz POS pogas, jāveic paziņojumu iestatīšana, kā aprakstīts iepriekš šajā tēmā (t.i., jāiespējo paziņojumi operācijai, jāiestata paziņošanas intervāls un jāatjaunina POS darbinieka atļauju grupa). Turklāt ir jāatver pogas režģa veidotājs, jāapskata pogas rekvizīti un jāatzīmē izvēles rūtiņa **Iespējot reāllaika saturu**. Laukā **Satura pielāgošana** varat atlasīt, vai skaits tiek rādīts pogas augšējā labajā stūrī (**Augšējā labajā stūrī**) vai vidū (**Vidū**).

> [!NOTE]
> Reāllaika saturu operācijām var iespējot tikai tad, ja tām ir atzīmēta izvēles rūtiņa **Iespējot paziņojumus** lapā **POS operācijas**, kā aprakstīts iepriekš šajā tēmā.

Tālāk attēlā ir parādīts reāllaika satura iestatījumi pogas režģa veidotājā.

![Tiešsaistes satura iestatījumi pogu režģa noformētājā.](./media/ButtonGridDesigner.png "Tiešsaistes satura iestatījumi pogu režģa noformētājā")

Lai parādītu paziņojumu skaitu uz pogas, ir jāpārliecinās, ka tiek atjaunināts atbilstošais ekrāna izkārtojums. Lai noteiktu ekrāna izkārtojumu, ko izmanto POS, augšējā labajā stūrī atlasiet ikonu **Iestatījumi** un piefiksējiet rādītājus **Ekrāna izkārtojuma ID** un **Izkārtojuma izšķirtspēja**. Izmantojot pārlūkprogrammu Edge, dodieties uz lapu **Ekrāna izkārtojums**, atrodiet iepriekš noteiktos rādītājus **Ekrāna izkārtojuma ID** un **Izkārtojuma izšķirtspēja** un atzīmējiet izvēles rūtiņu **Iespējot tiešsaistes saturu**. Dodieties uz **Retail un Commerce \> Retail un Commerce IT \> Sadales grafiks** un palaidiet darbu 1090 (Reģistri), lai sinhronizētu izkārtojuma izmaiņas.

![Atrast POS izmantoto ekrāna izkārtojumu.](./media/Choose_screen_layout.png "Atrast ekrāna izkārtojumu")

Tālāk attēlā ir parādīts rezultāts, atlasot dažāda izmēra pogu **Augšējā labajā stūrī** vai **Vidū** laukā **Satura pielāgošana**.

![Reāllaika saturs POS pogās.](./media/ButtonsWithLiveContent.png "Reāllaika saturs POS pogās")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
