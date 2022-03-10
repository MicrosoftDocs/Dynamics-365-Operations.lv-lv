---
title: Manuāla bāzlīnijas prognozes korekciju veikšana
description: Šajā tēmā ir paskaidrots, kā var manuāli veikt bāzlīnijas prognozes korekcijas un skatīt detalizētu informāciju par prognozi.
author: ChristianRytt
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d00061efa551c9fe2ad9d0e441bba44e70b071c
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103767"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Manuāla bāzlīnijas prognozes korekciju veikšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā var manuāli veikt bāzlīnijas prognozes korekcijas un skatīt detalizētu informāciju par prognozi. 

Pirms manuālu korekciju veikšanas ir jāizprot daži dažādu lapu principi.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Lapas Koriģēta pieprasījuma apjoma prognoze režģis
Lapā **Koriģēta pieprasījuma apjoma prognoze** ir iekļauts režģis, kam ir tālāk norādītā struktūra.

-   Pirmajā kolonnā ir redzami krājumi, krājumu sadalījuma principi, uzņēmumi un citi elementi, par kuriem ir ģenerēta prognoze. Lapas apakšvirsraksts norāda pašreizējo prognozes dimensiju, kas redzamas režģī, aprakstu. Piemēram, ja lapas apakšvirsraksts ir **Uzņēmums/Vieta/Krājumu sadalījuma princips** un kāda no rindu galvenēm režģī ir **USMF/1/\_Alloc**, šajā rindā ir redzama prognoze, kas attiecas uz uzņēmumu USMF, vietu Nr. 1 un krājumu sadalījuma principu **D\_Alloc**.
-   Nākamās kolonnas attiecas uz prognožu intervāliem, kuriem prognoze ir ģenerēta. Katras kolonnas galvene ir pirmais prognozes intervāla datums, kas ir redzams kolonnā.
-   Vērtības šūnās norāda viena krājuma, krājumu sadalījuma principa un citu šī konkrētā prognozes intervāla elementu prognozi.

## <a name="forecast-aggregation-and-de-aggregation"></a>Prognozes apkopošana un apkopojuma sadalīšana
Lapas apakšvirsraksts norāda prognozes apkopojuma līmenī. 

Piemēram, ja lapas apakšvirsraksts ir **Uzņēmums / Vieta / Sadalījuma princips / Krājuma kods / Krāsa / Izmērs / Konfigurācija / Stils**, nav veikta prognozes apkopošana, un prognoze tiek parādīta krājuma un tā dimensiju līmenī. Lai mainītu apkopošanas iestatījumu, izmantojiet lapu **Mainīt prognozes dimensijas**, kuru var atvērt lietojumprogrammas izvēlnē. 

Lai mainītu prognozi, noklikšķiniet uz jebkuras pieejamās šūnas un ierakstiet koriģētās prognozes vērtību. Rediģētā šūna nekavējoties tiek parādīta treknrakstā, norādot, ka tajā redzamā prognoze nav prognoze, kas ir izveidota, izmantojot pieprasījuma prognozēšanas pakalpojumu, bet ir manuāli koriģēta. 

Ja apkopojums tiek mainīts, lai lapā parādītu vairāk apkopotos datus, var izmantot lapu **Pieprasījuma apjoma prognozes rindas**, lai skatītu atsevišķas prognozes rindas, kuras veido apkopoto prognozi. 

Piemēram, prognoze ir ģenerēta krājuma līmenī, bet ir zināms, ka reklamēšanas vai citu līdzīgu notikumu dēļ šī krājuma pieprasījums palielinās visās vietās. Šajā gadījumā var iestatīt apkopošanu dimensijām **Uzņēmums / Krājuma sadalījuma parametrs / Krājums** lapā **Mainīt prognozes dimensijas**. Var koriģēt vispārējo visās vietās pieejamo krājumu prognozi režģī **Koriģētā pieprasījuma apjoma prognoze**. Lai redzētu veikto izmaiņu ietekmi visās vietās, atveriet lapu **Pieprasījuma apjoma prognozes rindas**. Šajā lapā var redzēt vienu rindu katras vietas krājumam, koriģētās prognozes daudzumu un sākotnēji prognozēto daudzumu. 

Ja apkopotā līmenī tiek veikta prognozētā daudzuma korekcija, sistēmā tiek izmantots svērtais sadalījums, lai nodotu izmaiņas uz rindām, kas veido apkopojumu. 

Korekcijas var veikt arī manuāli lapā **Pieprasījuma apjoma prognozes rindas**, mainot vai nu vienuma **Kopējais daudzums** vērtību, vai vienuma **Daudzums** šūnas apkopošanas noņemšanas režģī.

## <a name="viewing-details-of-the-forecast"></a>Detalizētu prognozes datu skatīšana
Lai skatītu sīkāku informāciju par prognozi, var atvērt lapu **Detalizēti pieprasījuma apjoma prognozes dati**. 

Lapā **Detalizēti pieprasījuma apjoma prognozes dati** grafiskā un tabulas formātā tiek parādīta tālāk norādītā informācija.

-   Vēsturiskais pieprasījums, kas ir prognozes datu pamatā.
-   Pašreizējā prognoze, kas tiek izmantota vispārējā plānošanā.
-   Jaunas pieprasījumu apjoma prognozes vērtības un summas, kurām tās ir manuāli koriģētas.
-   Prognozēto vērtību ticamības intervāls.
-   Prognozes ģenerēšanai izmantotais prognozes modelis. Ja tiek skatīti apkopotie dati, ir redzams visu to metožu saraksts, kuras tika izmantotas visām apkopotajām laika sērijām.
-   Iekšējā modeļa precizitāte (MAPE). Lai iegūtu sīkāku informāciju par prognozes precizitāti, skatiet sadaļu [Prognozes precizitātes pārraudzīšana](monitor-forecast-accuracy.md).

**Piezīmes.**

- Izmantojot *līdzekli Budžeta modelis, kas atlasīts* detalizētas informācijas par pieprasījuma apjoma prognozēm, tiek pievienotas **iestatījumi** lapā Pieprasījuma apjoma prognozes informācija, kas ļauj atlasīt iekļaujamus budžeta modeļus. No Piegādes ķēdes pārvaldības versijas 10.0.21 šī funkcija ir ieslēgta pēc noklusējuma. Tāpat kā Piegādes ķēdes pārvaldībai 10.0.25 šī funkcija ir obligāta un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.25, administratori šo funkcionalitāti var ieslēgt vai izslēgt, *·*[meklējot prognozes modeļa atlasi pieprasījuma apjoma prognozes informācijas līdzeklim līdzekļu pārvaldības darbvietā.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)
- Ticamības intervāls, kas ir redzams lapas sadaļā **Prognoze**, norāda starpību starp ticamības intervāla augšējo robežu un ticamības intervāla apakšējā robežu. Lai redzētu augšējās un apakšējās robežas vērtības, novietojiet kursoru virs diagrammas sadaļā **Grafisks vēsturiskā pieprasījuma un prognozes attēlojums**.
- Ja lietojat Microsoft Azure mašīnmācīšanās pakalpojumu pieprasījuma apjoma prognozei, varat norādīt ģenerētās prognozes ticamības līmeni procentos. Ticamības intervālu veido vairākas vērtības, kas darbojas kā labs pieprasījuma apjoma prognozes aprēķins. Ticamības līmenis 95 % norāda, ka pastāv 5 % risks, ka pieprasījuma apjoma prognoze nav ticamības intervāla diapazonā.

Lapā **Detalizēti pieprasījuma apjoma prognozes dati** var veikt arī manuālas korekcijas, mainot vērtības rindā **Prognoze** sadaļā **Prognoze**.

## <a name="additional-resources"></a>Papildu resursi

[Prognozes precizitātes pārraudzība](monitor-forecast-accuracy.md)

[Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]