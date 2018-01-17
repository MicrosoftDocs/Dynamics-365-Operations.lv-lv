---
title: "Paziņojumu rādīšanas secība programmā Point of Sale"
description: "Šajā tēmā ir aprakstīts, kā programmā Point of Sale iespējot paziņojumu rādīšanu noteiktā secībā, un aprakstīta paziņojumu struktūra, kuru var paplašināt arī uz citām operācijām."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Paziņojumu rādīšana programmā Point of Sale

Mūsdienu modernajā mazumtirdzniecības vidē veikala darbiniekiem tiek piešķirti dažādi uzdevumi, piemēram, palīdzēšana klientiem, transakciju ievadīšana, krājumu uzskaites veikšana un pasūtījumu pieņemšana veikalā. Klients Point of Sale (POS) darbiniekiem sniedz iespējas izpildīt šos uzdevumus un vēl daudz ko citu, un to visu var paveikt no vienas programmas. Tā kā dienas laikā ir jāizpilda dažādi uzdevumi, veikala darbinieki, iespējams, ir jāinformē par lietām, kurām šiem darbiniekiem būtu jāpievērš uzmanība. Paziņojumu struktūra programmā POS atrisina šo problēmu, ļaujot mazumtirgotājiem konfigurēt paziņojumus atkarībā no lomām. Izmantojot Dynamics 365 for Retail programmas 5. atjauninājumu, šos paziņojumus var konfigurēt tikai POS operācijām.

Pašlaik sistēma nodrošina iespēju rādīt paziņojumus par pasūtījumu izpildes operācijām, taču paziņojumu struktūra ir izveidota tā, lai to varētu paplašināt, tādēļ nākotnē izstrādātāji varēs uzrakstīt paziņojumu apdarinātāju jebkādām operācijām un rādīt šos paziņojumus programmā POS.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Paziņojumu iespējošana pasūtījumu izpildes operācijām

Lai iespējotu paziņojumus par pasūtījumu izpildes operācijām, skatiet tālāk aprakstītās darbības.

 - Dodieties uz lapu **Operācijas** (**Retail** > **Kanāla iestatīšana** > **POS iestatīšana** > **POS** > **Operācijas**).
 - Atrodiet attiecīgo pasūtījuma izpildes operāciju un atzīmējiet šīs operācijas izvēles rūtiņu **Iespējot paziņojumus**. Šādi paziņojumu struktūrai tiek norādīts klausīties apdarinātāju saistībā ar šo pasūtījuma izpildes operāciju. Ja apdarinātājs ir ieviests, šie paziņojumi tiek rādīti programmā POS, pretējā gadījumā paziņojumi par šo operāciju netiek rādīti.
- Dodieties uz POS atļaujām, kas ir saistītas ar darbiniekiem, un kopsavilkuma cilnē **Paziņojumi** pievienojiet pasūtījuma izpildes operāciju, kurai vienums “Rādīšanas secība” ir iestatīts uz 1. Ja ir konfigurēti vairāki paziņojumi, šī rādīšanas secība tiek izmantota paziņojumu sakārtošanai no augšas uz leju, sākot no 1 pašā augšā. Var pievienot tikai tādas operācijas, kurām ir atzīmēta izvēles rūtiņa **Iespējot paziņojumus**. Turklāt šie paziņojumi tiks rādīti tikai par šeit pievienotajām operācijām un tikai tiem darbiniekiem, kuriem šīs operācijas ir pievienotas atbilstošajās POS atļaujās. 

> [!NOTE]
> Paziņojumus var pārrakstīt lietotāja līmenī, dodoties uz darbinieka ierakstu, atlasot **POS atļaujas** un pēc tam rediģējot attiecīgā lietotāja paziņojumu abonementu.

 - Dodieties uz lapu **Funkcionalitātes profils** (**Retail** > **Kanāla iestatīšana** > **POS iestatīšana** > **POS profili** > **Funkcionalitātes profili**). Atjauniniet rekvizītu **Paziņošanas intervāls**, lai iestatītu minūtēs izteiktu intervālu, pēc kāda paziņojumi ir jāizņem. Ieteicams šo vērtību iestatīt uz 10 minūtēm, lai izvairītos no liekas saziņas ar galveno biroju. Paziņošanas intervālu iestatot uz “0”, paziņojumi tiek izslēgti.  

 - Dodieties uz **Retail** > **Mazumtirdzniecības IT** > **Sadales grafiks**. Atlasiet grafiku “1060-Personāls”, lai sinhronizētu abonēšanas iestatījumus, un pēc tam noklikšķiniet uz **Izpildīt tūlīt**. Pēc tam sinhronizējiet atļaujas intervālu, atlasot “1070-Kanāla konfigurācija”, un pēc tam noklikšķiniet uz **Izpildīt tūlīt**. 

## <a name="view-notifications-in-pos"></a>Paziņojumu skatīšana programmā POS

Pēc iepriekš aprakstīto darbību izpildīšanas darbinieki, kuram ir iestatīti paziņojumi, šos paziņojumus var skatīt programmā POS. Lai skatītu šos paziņojumus, noklikšķiniet uz paziņojuma ikonas POS virsrakstjoslā. Šādi tiek parādīts paziņojumu centrs ar paziņojumiem par pasūtījuma izpildes operāciju. Paziņojumu centrā būtu jārāda tālāk noradītās grupas, kas ietilpst pasūtījuma izpildes operācijā. 

- **Gaidošie pasūtījumi** — šajā grupā tiek rādīts to pasūtījumu skaits, kuriem ir gaidošs stāvoklis, piemēram, pasūtījumi, kas ir jāpieņem kādam POS darbiniekam, kuram ir veikala izpildes nepieciešanās atļaujas. Noklikšķinot uz grupas skaita, tiek atvērta lapa **Pasūtījuma izpilde**, kura ir filtrēta tā, lai rādītu tikai gaidošos pasūtījumus, kas veikalam ir piešķirti izpildīšanai. Ja veikalam pasūtījumi tiek pieņemti automātiski, šai grupai skaits ir nulle.

- **Izdot veikalā** — ar šo grupu tiek rādīts tādu pasūtījumu skaits, kuru piegādes metode ir **Izdošana** un kuriem izdošana ir plānota no pašreizējā veikala. Noklikšķinot uz grupas skaita, tiek atvērta lapa **Pasūtījuma izpilde**, kura ir filtrēta tā, lai rādītu aktīvos pasūtījumus, kas ir iestatīti izdošanai no pašreizējā veikala.

- **Nosūtīt no veikala** — ar šo grupu tiek rādīts tādu pasūtījumu skaits, kuru piegādes metode ir **Nosūtīšana** un kuriem nosūtīšana ir plānota no pašreizējā veikala. Noklikšķinot uz grupas skaita, tiek atvērta lapa **Pasūtījuma izpilde**, kura ir filtrēta tā, lai rādītu aktīvos pasūtījumus, kas ir iestatīti nosūtīšanai no pašreizējā veikala.

Kad veikalam izpildei tiek piešķirti jauni pasūtījumi, paziņojumu ikona mainās, lai rādītu jaunos paziņojumus, un tiek atjaunināts atbilstošo grupu skaits. Lietotājs var arī noklikšķināt uz atsvaidzināšanas ikonas blakus operācijas nosaukumam, lai nekavējoties atjauninātu grupu skaitu. Skaits tiek atjaunināts arī ik pēc iepriekš definētā intervāla. Kad kādai grupai rodas jauns vienums, kuru pašreizējais darbinieks vēl nav redzējis, tiek rādīta sprāgšanas ikona, tā norādot, ka šai grupai ir jauns vienums. Paziņojumos noklikšķinot uz elementiem, tiek atvērta konkrētā operācija, kurai šis paziņojums ir konfigurēts. Iepriekš aprakstītajos scenārijos noklikšķinot uz paziņojumiem, tiek atvērta lapa **Pasūtījuma izpilde** un nodoti atbilstošie parametri: gaidošie pasūtījumi, izdošana veikalā un nosūtīšana no veikala. 

> [!NOTE]
> Gaidošo pasūtījumu paziņojumi tiks iespējoti turpmākā programmas Dynamics 365 for Retail atjauninājumā. 


