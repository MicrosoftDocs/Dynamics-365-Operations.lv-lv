---
title: Pasūtījumu paziņojumu parādīšana pārdošanas punktā (POS)
description: Šajā tēmā ir aprakstīts, kā pārdošanas punktā iespējot pasūtījumu paziņojumu rādīšanu, un aprakstīta paziņojumu struktūra
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: e663a5dca76d570217b7e02444689a2e2d312c41
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975175"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Pasūtījumu paziņojumu parādīšana pārdošanas punktā (POS)

[!include [banner](includes/banner.md)]

Modernajā mazumtirdzniecības vidē veikala darbiniekiem tiek piešķirti dažādi uzdevumi, piemēram, palīdzēšana klientiem, transakciju ievadīšana, krājumu uzskaites veikšana un pasūtījumu pieņemšana veikalā. Pārdošanas punkta (POS) klients nodrošina vienu programmu, kur veikala darbinieki vat izpildīt visus šos un vēl daudzus citus uzdevumus. Tā kā dienas laikā ir jāizpilda dažādi uzdevumi, veikala darbinieki, iespējams, ir jāinformē par lietām, kurām šiem darbiniekiem būtu jāpievērš uzmanība. Paziņojumu struktūra programmā POS atrisina šo problēmu, ļaujot mazumtirgotājiem konfigurēt paziņojumus atkarībā no lomām. Programmā Dynamics 365 for Retail ar 5. lietojumprogrammas atjauninājumu šos paziņojumus var konfigurēt tikai POS operācijām.


Pašlaik sistēma var parādīt paziņojumus tikai par pasūtījuma izpildes operācijām. Tomēr struktūra ir veidota paplašināma, tādēļ izstrādātāji galu galā varēs rakstīt paziņojumu apdarinātāju jebkādai operācijai un parādīt paziņojumus par šīm operācijām POS.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Paziņojumu iespējošana pasūtījumu izpildes operācijām

Lai iespējotu paziņojumus par pasūtījumu izpildes operācijām, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Retail un Commerce** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Operācijas**.
2. Meklējiet operāciju **Pasūtījuma izpilde** un atzīmējiet tās izvēles rūtiņu **Iespējot paziņojumus**, lai norādītu, ka paziņojumu struktūrai jāņem vērā šīs operācijas apdarinātājs. Ja apdarinātājs ir ieviests, šīs operācijas paziņojumi tiks rādīti POS.
3. Dodieties uz **Retail un Commerce** &gt; **Darbinieki** &gt; **Nodarbinātie** &gt; cilnē Commerce atveriet POS atļaujas, kas saistītas ar nodarbināto. Izvērsiet kopsavilkuma cilni **Paziņojumi**, pievienojiet operāciju **Pasūtījuma izpilde** un iestatiet laukam **Rādīt pasūtījumu** vērtību **1**. Ja ir konfigurēti vairāki paziņojumi, šis lauks tiek izmantots, lai kārtotu paziņojumus. Paziņojumi, kuriem ir zemākā vērtība **Rādīt pasūtījumu** tiek rādīti pirms paziņojumiem, kam ir lielāka vērtība. Paziņojumi, kam **Rādīt pasūtījumu** vērtība ir **1**, tiek rādīti augšā.

    Paziņojumi tiek rādīti tikai operācijām, kas tiek pievienotas kopsavilkuma cilnē **Paziņojumi**, un operācijas var pievienot tikai tad, ja šīm operācijām ir atzīmēta izvēles rūtiņa **Iespējot paziņojumus** lapā **POS operācijas**. Turklāt paziņojumi par šo operāciju tiek rādīti darbiniekiem tikai tad, ja operācija tiek pievienota šo darbinieku POS atļaujām.

    > [!NOTE]
    > Paziņojumus var ignorēt lietotāja līmenī. Atveriet darbinieka ierakstu, atlasiet **POS atļaujas** un pēc tam rediģējiet lietotāja paziņojumu abonementu.

4. Dodieties uz sadaļu **Retail un Commerce** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Funkcionalitātes profili**. Laukā **Paziņošanas intervāls** norādiet, cik bieži paziņojumi jārāda. Dažiem paziņojumiem sistēmai POS ir jāveic reāllaika izsaukums grāmatvedības programmai. Šie zvani patērē grāmatvedības programmai nepieciešamo datora noslodzi. Tādēļ, iestatot paziņošanas intervālu, jāņem vērā gan uzņēmuma prasības, gan reāllaika izsaukumu grāmatvedības programmai ietekme. Vērtība **0** (nulle) izslēdz paziņojumus.
5. Pārejiet uz **Retail un Commerce** &gt; **Retail un Commerce IT** &gt; **Sadales grafiks**. Atlasiet grafiku **1060** (**Personāls**), lai sinhronizētu paziņojumu abonementa iestatījumus, un pēc tam atlasiet **Izpildīt tūlīt**. Tālāk sinhronizējiet atļaujas intervālu, atlasot **1070** (**Kanāla konfigurācija**), un pēc tam atlasiet **Izpildīt tūlīt**.

## <a name="view-notifications-in-the-pos"></a>Paziņojumu skatīšana programmā POS

Pēc visu darbību pabeigšanas darbinieki varēs skatīt paziņojumus programmā POS. Lai skatītu paziņojumus, POS augšējā labajā stūrī nospiediet uz paziņojuma ikonas. Tiek parādīts paziņojumu centrs un paziņojumi par pasūtījuma izpildes operāciju. Paziņojumu centrā rāda tālāk norādītās grupas, kas ietilpst pasūtījuma izpildes operācijā.

- **Izdot veikalā** — ar šo grupu tiek rādīts tādu pasūtījumu skaits, kuru piegādes metode ir **Izdošana** un kuriem izdošana ir plānota no pašreizējā veikala. Varat nospiest uz grupas numura, lai atvērtu lapu **Pasūtījuma izpilde**. Šajā gadījumā lapa tiek filtrēta tā, lai rādītu tikai aktīvos pasūtījumus, kas tika iestatīti izdošanai no pašreizējā veikala.
- **Nosūtīt no veikala** — ar šo grupu tiek rādīts tādu pasūtījumu skaits, kuru piegādes metode ir **Nosūtīšana** un kuriem nosūtīšana ir plānota no pašreizējā veikala. Varat nospiest uz grupas numura, lai atvērtu lapu **Pasūtījuma izpilde**. Šajā gadījumā lapa tiek filtrēta tā, lai rādītu tikai aktīvos pasūtījumus, kas tika iestatīti nosūtīšanai no pašreizējā veikala.

Kad veikalam izpildei tiek piešķirti jauni pasūtījumi, paziņojumu ikona mainās, lai rādītu jaunos paziņojumus, un tiek atjaunināts atbilstošo grupu skaits. Kaut gan grupas tiek atsvaidzinātas regulāri, POS lietotāji var manuāli atsvaidzināt grupas jebkurā laikā, atlasot pogu **Atsvaidzināt** blakus grupas nosaukumam. Visbeidzot, ja grupai ir jauns krājums, ko pašreizējais darbinieks nav skatījis, grupai parāda sprādziena simbols, kas norāda par jaunu saturu.

## <a name="enable-live-content-on-pos-buttons"></a>Reāllaika satura iespējošana uz POS pogas

Tagad uz POS pogas var parādīt skaitu, lai darbinieki varētu viegli noteikt, kādiem uzdevumiem nekavējoties jāpievērš uzmanība. Lai šo skaitu parādītu uz POS pogas, jāveic paziņojumu iestatīšana, kā aprakstīts iepriekš šajā tēmā (t.i., jāiespējo paziņojumi operācijai, jāiestata paziņošanas intervāls un jāatjaunina POS darbinieka atļauju grupa). Turklāt ir jāatver pogas režģa veidotājs, jāapskata pogas rekvizīti un jāatzīmē izvēles rūtiņa **Iespējot reāllaika saturu**. Laukā **Satura pielāgošana** varat atlasīt, vai skaits tiek rādīts pogas augšējā labajā stūrī (**Augšējā labajā stūrī**) vai vidū (**Vidū**).

> [!NOTE]
> Reāllaika saturu operācijām var iespējot tikai tad, ja tām ir atzīmēta izvēles rūtiņa **Iespējot paziņojumus** lapā **POS operācijas**, kā aprakstīts iepriekš šajā tēmā.

Tālāk attēlā ir parādīts reāllaika satura iestatījumi pogas režģa veidotājā.

![Tiešsaistes satura iestatījumi pogu režģa noformētājā](./media/ButtonGridDesigner.png "Tiešsaistes satura iestatījumi pogu režģa noformētājā")

Lai parādītu paziņojumu skaitu uz pogas, ir jāpārliecinās, ka tiek atjaunināts atbilstošais ekrāna izkārtojums. Lai noteiktu ekrāna izkārtojumu, ko izmanto POS, augšējā labajā stūrī atlasiet ikonu **Iestatījumi** un piefiksējiet rādītājus **Ekrāna izkārtojuma ID** un **Izkārtojuma izšķirtspēja**. Izmantojot pārlūkprogrammu Edge, dodieties uz lapu **Ekrāna izkārtojums**, atrodiet iepriekš noteiktos rādītājus **Ekrāna izkārtojuma ID** un **Izkārtojuma izšķirtspēja** un atzīmējiet izvēles rūtiņu **Iespējot tiešsaistes saturu**. Dodieties uz **Retail un Commerce\> Retail un Commerce IT \> Sadales grafiks** un palaidiet darbu 1090 (Reģistri), lai sinhronizētu izkārtojuma izmaiņas.


![Atrast POS izmantoto ekrāna izkārtojumu](./media/Choose_screen_layout.png "Atrast ekrāna izkārtojumu")

Tālāk attēlā ir parādīts rezultāts, atlasot dažāda izmēra pogu **Augšējā labajā stūrī** vai **Vidū** laukā **Satura pielāgošana**.

![Reāllaika saturs POS pogās](./media/ButtonsWithLiveContent.png "Reāllaika saturs POS pogās")
