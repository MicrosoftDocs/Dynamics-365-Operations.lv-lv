---
title: Pārskats par pieprasījuma prognozēšanu
description: Pieprasījuma prognozēšanas tiek izmantota, lai prognozētu debitoru pasūtījumu neatkarīgu pieprasījumu pēc pārdošanas pasūtījumiem un atkarīgos pieprasījums jebkurā atsaistīšanas punktā. Uzlabotās pieprasījuma apjoma prognozes samazināšanas kārtulas nodrošina lielisku lielapjoma pielāgošanas risinājumu.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b71fde2d1b56b237dec2a08d3bd27e8ba6c35fef
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595550"
---
# <a name="demand-forecasting-overview"></a>Pārskats par pieprasījuma prognozēšanu

[!include [banner](../includes/banner.md)]

Pieprasījuma prognozēšanas tiek izmantota, lai prognozētu debitoru pasūtījumu neatkarīgu pieprasījumu pēc pārdošanas pasūtījumiem un atkarīgos pieprasījums jebkurā atsaistīšanas punktā. Uzlabotās pieprasījuma apjoma prognozes samazināšanas kārtulas nodrošina lielisku lielapjoma pielāgošanas risinājumu.

Lai ģenerētu bāzlīnijas prognozi, uz pakalpojumā Azure viesoto Microsoft Azure algoritmiskās mācīšanās pakalpojumu tiek nosūtīts kopsavilkums par vēsturiskajām transakcijām. Tā kā šis pakalpojums netiek kopīgots starp lietotājiem, to var ērti pielāgot, lai tas atbilstu konkrētas nozares prasībām. Programmatūru Finance and Operations varat izmantot, lai vizualizētu un pielāgotu prognozi un skatītu prognozes precizitātes izpildes pamatrādītājus (KPI).

## <a name="key-features-of-demand-forecasting"></a>Pieprasījuma prognozēšanas galvenās funkcijas
Tālāk ir norādītas dažas pieprasījuma prognozēšanas galvenās funkcijas.

-   Ģenerējiet statistiskās bāzlīnijas prognozi, kura ir balstīta vēsturiskajos datos.
-   Izmantojiet dinamisko prognozes dimensiju kopu.
-   Vizualizējiet prognozes pieprasījuma tendences, ticamības intervālus un korekcijas.
-   Autorizējiet koriģēto prognozi, kas jāizmanto plānošanas procesos.
-   Noņemiet netipiskās vērtības.
-   Izveidojiet prognozes precizitātes mērījumus.

## <a name="major-themes-in-demand-forecasting"></a>Pieprasījuma prognozēšanas galvenās tēmas
Pieprasījuma prognozēšanā ir ieviestas trīs tālāk norādītās galvenās tēmas.

-   **Modularitāte** — pieprasījuma prognozēšanas ir modulārs un viegli konfigurējams process. Šo funkciju var ieslēgt un izslēgt, mainot konfigurācijas atslēgu sadaļā **Tirdzniecība** &gt; **Krājumu prognoze** &gt; **Pieprasījuma prognozēšana**.
-   **Atkārtota Microsoft steka izmantošana** — korporācija Microsoft izlaida algoritmiskās mācīšanās platformu 2015. gada februārī. Algoritmiskā mācīšanās, kas tagad ir daļa no platformas Microsoft Cortana Analytics Suite, sniedz iespēju ātri vienkārši izvietot prognozējošas analīzes eksperimentus, piemēram, pieprasījuma novērtēšanas eksperimentus, izmantojot R algoritmus vai Python programmēšanas valodas un vienkāršu vilkšanas un nomešanas interfeisu.
    -   Varat lejupielādēt Finance and Operations pieprasījuma prognozēšanas eksperimentus, mainīt tos atbilstoši jūsu uzņēmuma prasībām, publicēt tos kā tīmekļa pakalpojumu Azure vietnē un izmantot tos, lai ģenerētu pieprasījuma apjoma prognozes. Eksperimentus var lejupielādēt, ja Finance and Operations ražošanas plānotāja abonementu esat iegādājies kā uzņēmuma līmeņa lietotājs.
    -   Visi pašlaik pieejamie pieprasījuma apjoma prognozes eksperimenti ir pieejami lejupielādei sadaļā [Cortana Analytics galerija](https://gallery.cortanaanalytics.com/). Lai gan Finance and Operations pieprasījuma prognozēšanas eksperimenti tiek automātiski integrēti programmatūrā Finance and Operations, debitoriem un partneriem ir jāveic to eksperimentu integrēšana, ko viņi lejupielādē no [Cortana Analytics galerijas](https://gallery.cortanaanalytics.com/). Tāpēc no [Cortana Analytics galerijas](https://gallery.cortanaanalytics.com/) lejupielādēto eksperimentu lietošana ir sarežģītāka nekā Finance and Operations pieprasījuma prognozēšanas eksperimentu lietošana. Eksperimentu kodu ir nepieciešams modificēt tā, lai eksperimentiem tiktu izmantots Finance and Operations programmēšanas interfeiss (API).
    -   Varat izveidot savus eksperimentus pakalpojumā Microsoft Azure Machine Learning Studio, publicēt tos kā pakalpojumus platformā Azure un izmantot tos pieprasījuma apjoma prognožu ģenerēšanai.
    -   Ja nav nepieciešama augsta veiktspēja vai ja nav jāapstrādā liels datu apjoms, var izmantot pakalpojuma Machine Learning bezmaksas līmeni. Mēs iesakām sākt darbu, izmantojot šo līmeni īpaši ieviešanas un testēšanas fāzes laikā. Ja ir nepieciešama augstāka veiktspēja un papildu krātuves vieta, var izmantot pakalpojuma Machine Learning standarta līmeni. Lai varētu izmantot šo līmeni, ir nepieciešams Azure abonements un jārēķinās ar papildu izmaksām. Plašāku informāciju par algoritmiskās mācīšanās izcenojumu skatiet tēmā [Machine Learning Studio izcenojums](https://aka.ms/machine-learning-price-info).
-   **Budžeta samazinājums jebkurā atsaistīšanas punktā** — programmatūras Finance and Operations pieprasījuma prognozēšanas pamatā ir šī funkcionalitāte, kas jums sniedz iespēju prognozēt gan atkarīgo, gan neatkarīgo pieprasījumu jebkurā atsaistīšanas punktā.

## <a name="basic-flow-in-demand-forecasting"></a>Pieprasījuma prognozēšanas pamata plūsmas
Šajā diagramma ir redzama pieprasījuma prognozēšanas pamata plūsma. 

[![Pieprasījuma prognozēšanas ievada shēma](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Pieprasījuma apjoma prognozes ģenerēšana sākas programmatūrā Finance and Operations. Tiek apkopoti Finance and Operations transakciju datu bāzē pieejamie vēsturiskie transakciju dati, un ar tiem tiek aizpildīta izstrādāšanas tabula. Vēlāk izstrādāšanas tabula tiek nodota algoritmiskās mācīšanās pakalpojumam. Veicot nelielus pielāgojumus, varat pievienot izveidošanas tabulai dažādus datu avotus. Var izmantot tādus datu avotus kā Microsoft Excel faili, komatatdalīto vērtību (CSV) faili un programmu Microsoft Dynamics AX 2009 un Microsoft Dynamics AX 2012 dati. Tāpēc varat ģenerēt pieprasījuma apjoma prognozes, izmantojot vairākās sistēmās glabātos vēsturiskos datus. Tomēr pamatdatiem, piemēram, krājumu nosaukumiem un mērvienībām, ir jābūt vienādiem visos dažādajos datu avotos.

Ja izmantojat Finance and Operations pieprasījuma prognozēšanas algoritmiskās mācīšanās eksperimentus, bāzlīnijas prognozes aprēķināšanai tiek meklēta atbilstošākā no piecām laika sērijas prognozēšanas metodēm. Šo prognozēšanas metožu parametrus var pārvaldīt programmatūrā Finance and Operations. 

Pēc tam prognozes, vēsturiskie dati un jebkādas iepriekšējo iterāciju pieprasījuma apjoma prognožu izmaiņas ir pieejamas programmatūrā Finance and Operations. 

Programmatūru Finance and Operations varat izmantot, lai vizualizētu un modificētu bāzlīnijas prognozes. Pirms prognožu izmantošanas plānošanai manuālās korekcijas ir jāapstiprina.

## <a name="limitations"></a>Ierobežojumi
Pieprasījuma prognozēšana programmatūrā Finance and Operations ir rīks, kas ražošanas nozares debitoriem palīdz izveidot prognozēšanas procesus. Šis rīks nodrošina galvenās pieprasījuma prognozēšanas risinājuma funkcijas un ir izstrādāts tā, lai to varētu viegli paplašināt. Iespējams, ka pieprasījuma prognozēšana nav pilnībā piemērota debitoriem, piemēram, mazumtirdzniecības, vairumtirdzniecības, noliktavu, transportēšanas vai citu profesionālo pakalpojumu nozarēs.

<a name="additional-resources"></a>Papildu resursi
--------

[Pieprasījuma prognozēšanas iestatīšana](demand-forecasting-setup.md)

[Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)

[Manuālu bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)

[Koriģētās prognozes autorizēšana](authorize-adjusted-forecast.md)

[Prognozes precizitātes pārraudzība](monitor-forecast-accuracy.md)

[Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi](remove-historical-outliers-calculating-demand-forecast.md)

[Pieprasījuma prognozēšanas funkcionalitātes paplašināšana](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



