---
title: Vajadzības periods
description: Šajā tēmā ir aprakstīts, kā iestatīt vajadzību periodus, kad izmantojat plānošanas optimizāciju. Vajadzības periods norāda plānošanas diapazonu un ierobežojumu.
author: ChristianRytt
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f32c3fd523c3272665b4b45b6d3e136591d12cda191766970ebfaf74b81f0558
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726864"
---
# <a name="coverage-time-fences"></a>Vajadzības periods

Šajā tēmā ir aprakstīts, kā iestatīt *vajadzību periodus*, kad izmantojat plānošanas optimizāciju. Plānotāji var noteikt plānošanas diapazonu (vajadzības periodu dienās), kā arī izslēgt piedāvājumu un pieprasījumu, kas pārsniedz šo diapazonu. Tāpēc vajadzības laika periodi palīdz novērst "troksni", ko rada piedāvājuma ieteikumi, kas nav jā no valsts uz mēnešiem. Piemēri ietver nākamā gada prognozi un debitoru pasūtījumus, kas novietoti ārpus parastā izpildes laika.

Vajadzības periods ir dienu skaits pēc šodienas datuma (vai precīzāk, datums, kad izpildāt plānošanu), kurā piegāde un pieprasījums tiek izslēgts. Lai palīdzētu izvairīties no kavēšanās, jums jānodrošina, ka vajadzības periods ir garāks par kopējo izpildes laiku. Sistēmas noklusējuma vērtība ir 100 dienas.

Vajadzību periodu var norādīt katrā no šiem līmeņiem:

- **Vajadzības grupa** – jūs varat iestatīt noklusēto vajadzību periodu katrai vajadzību grupai.
- **Krājuma segums** – jūs varat ignorēt vajadzības periodu, kas ir mantots no nodrošinājuma grupas, kas ir piešķirta krājumam.
- **Galvenais plāns** – jūs varat ignorēt vajadzības periodu, kas ir mantots no nodrošinājuma grupas, kas ir piešķirta krājumam.

Šajās sadaļās izskaidrots, kā katrā līmenī norādīt vajadzību grupu.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Vajadzības perioda iestatīšana vajadzību grupai

Norādot vajadzības periodu vajadzību grupai, iestatījums attiecas uz visiem krājumiem (precēm), kas pieder šai grupai. Tomēr varat ignorēt iestatījumu specifiskiem krājumiem vai specifiskiem vispārējai plānam.

Lai norādītu vajadzību periodu vajadzību grupai, veiciet šīs darbības.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Segums \> Saguma grupas**.
1. Atlasiet esošo vajadzības grupu vai izveidojiet jaunu grupu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet **Vajadzību periodu (dienas)** uz dienu skaitu, kas jālieto kā vajadzības periods vajadzību grupā.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Vajadzības perioda iestatīšana noteiktam krājumam

Katrs krājums (prece) pieder vajadzību grupai. Ja neviena vajadzību grupa nav skaidri piešķirta krājumam, tiek lietota noklusētā vajadzības grupa. Katrs krājums manto vajadzības periodu no tā vajadzības grupas. Tomēr šo laika periodu var ignorēt noteiktiem krājumiem pēc vajadzības.

Lai norādītu vajadzību periodu vajadzību grupai, veiciet šīs darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Režģī atlasiet preci.
1. Darbību rūts cilnē **Plāns** grupā **Vajadzība** atlasiet **Krājumu segums**.
1. Lapas **Krājumu segums** cilnē **Pārskats** atlasiet vai izveidojiet rindu vietai, kurā vēlaties iestatīt vajadzību periodu.
1. Atlasiet cilni **Vispārīgi**, lai atvērtu atlasītās vietnes iestatījumus.
1. Atzīmējiet izvēles rūtiņu iestatījumu **Ignorēt vajadzības grupu** virsrakstā.
1. Iestatiet lauku **Vajadzību periodu (dienas)** uz dienu skaitu, kas jālieto kā vajadzības periods vajadzību grupā.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Vajadzības perioda iestatīšana noteiktam galvenajam plānam

Vajadzību periodu var norādīt galvenā plāna līmenī: Šādā veidā var norādīt dienu skaitu, ko vispārējā plāna aprēķins aptver vispārējai plānam. Šis iestatījums ignorē jebkurus vajadzības laika iestatījumus, kas ir definēti katram atbilstošam krājumam un vajadzības grupai.

Lai norādītu vajadzību periodu vajadzību grupai, veiciet šīs darbības.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet sarakstā esošu vispārējo plānu vai izveidojiet jaunu galveno plānu.
1. Kopsavilkuma cilnē **Periods dienās** iestatiet opciju **Vajadzība** uz *Jā*. Laukā zem šīs opcijas ievadiet dienu skaitu, ko vēlaties izmantot kā vajadzības periodu galvenajā plānā.

## <a name="considerations-for-coverage-time-fences"></a>Vajadzības periodu apsvērumi

Iestatot vajadzības periodus, apsveriet šādus punktus:

- Vajadzības periodi ietekmē tikai vispārējās plānošanas ievades datus. Ja rodas aizkave, rezultātā iegūtajiem plānotajiem pasūtījumiem var būt datums, kas ir pēc šodienas datuma plus vajadzības periods.
- Vajadzības periodi ir norādīti kalendāra dienās. Kalendāri, kas izmanto darbdienas, neietekmē laika perioda aprēķinu. Piemēram, nedēļa vienmēr tiek uzskatīta par septiņām dienām, pat ja nedēļas nogales darba laika kalendārā ir iestatītas kā slēgtas dienas.
- Pieprasījumu darbības netiks ģenerētas nevienam piedāvājumam un pieprasījumam, kas iekrīt ārpus vajadzību perioda.
- Ja kāds apstiprināts piedāvājums un pieprasījums iekrīt ārpus vajadzību perioda, tas netiks ielādēts programmā. Tādēļ tā aktivizēs papildināšanu un netiks aprēķināti kavējumi. Tomēr šo piedāvājumu un pieprasījumu nedrīkst np no sistēmas.
- Drošības krājumu daudzumu variācijas (no minimuma atslēgām) tiks ignorētas, ja tās pārsniedz vajadzību periodu.
- Starpuzņēmumu pieprasījums tiks ignorēts, ja aprēķinātais nosūtīšanas datums nav vajadzības periodā. Ievērojiet, ka iebūvētajā vispārējā plānošanā starpuzņēmumu pieprasījumu ierobežo vajadzību periods.
- Pieprasījuma apjoma prognozes tiks ignorētas, ja budžeta datums nav norādīts vajadzību periodā. Ievērojiet, ka iebūvētajā vispārējā plānošanā starpuzņēmumu pieprasījumu ierobežo vajadzību periods.
- Optimizācijas plānošana ir laika josla - zināms. Tas apsver laika joslu piegādes un pieprasījumu vietās un plānošanas izpildes laiku. Piemēram, galvenā plānošana tiek izraisīta 11.00 no Dānijas vietas (GMT+1 laika josla) 15. oktobrī, un tiek izmantots desmit dienu vajadzības periods. Šajā gadījumā piegāde un pieprasījums no vietas Sietlā (GMT-8 laika josla) ir iekļauts līdz 02.00 25. oktobrī (= desmit 24 stundu dienas pēc vispārējās plānošanas aktivizēšanas mīnus deviņas stundas laika joslas starpība). Ievērojiet, ka iebūvētā vispārējās plānošanas programma ņem vērā tikai laika perioda datumu. Tāpēc rezultāts var atšķirties.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]