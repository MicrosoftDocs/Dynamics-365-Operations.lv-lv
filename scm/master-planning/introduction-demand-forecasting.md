---
title: "Pārskats par pieprasījuma prognozēšanu"
description: "Pieprasījuma prognozēšanas tiek izmantota, lai prognozētu debitoru pasūtījumu neatkarīgu pieprasījumu pēc pārdošanas pasūtījumiem un atkarīgos pieprasījums jebkurā atsaistīšanas punktā. Uzlabotās pieprasījuma apjoma prognozes samazināšanas kārtulas nodrošina lielisku lielapjoma pielāgošanas risinājumu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9d74c1d1219eb39f2a76c0009adb21dd0c8c7b7c
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="demand-forecasting-overview"></a>Pārskats par pieprasījuma prognozēšanu

[!include[banner](../includes/banner.md)]


Pieprasījuma prognozēšanas tiek izmantota, lai prognozētu debitoru pasūtījumu neatkarīgu pieprasījumu pēc pārdošanas pasūtījumiem un atkarīgos pieprasījums jebkurā atsaistīšanas punktā. Uzlabotās pieprasījuma apjoma prognozes samazināšanas kārtulas nodrošina lielisku lielapjoma pielāgošanas risinājumu.

Lai ģenerētu bāzlīnijas prognozi, vēsturisko transakciju apkopojums tiek nosūtīts uz Microsoft Azure Machine pakalpojumu, ko vieso Azure. Tā kā šis pakalpojums netiek kopīgots starp lietotājiem, to var ērti pielāgot, lai tas atbilstu konkrētas nozares prasībām. Varat izmantot programmatūru Dynamics 365 for Operations, lai vizualizētu un pielāgotu prognozi un skatītu prognozes precizitātes izpildes pamatrādītājus (KPI).

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
-   **Atkārtota Microsoft steka izmantošana** — korporācija Microsoft izlaida algoritmiskās mācīšanās platformu 2015. gada februārī. Algoritmiskā mācīšanās, kas tagad ir daļa no platformas Microsoft Cortana Analytics Suite, sniedz iespēju ātri vienkārši izvietot prognozējošas analīzes eksperimentus, piemēram, pieprasījuma novērtēšanas eksperimentus, izmantojot R algoritmus vai Python programmēšanas valodas un vienkāršu vilkšanas un nomešanas interfeisu.
    -   Varat lejupielādēt Dynamics 365 for Operations pieprasījuma prognozēšanas eksperimentus, mainīt tos atbilstoši jūsu uzņēmuma prasībām, publicēt tos kā tīmekļa pakalpojumu Azure vietnē un izmantot tos, lai ģenerētu pieprasījuma apjoma prognozes. Eksperimentus var lejupielādēt, ja esat nopircis Dynamics 365 for Operations ražošanas plānotāja abonementu kā uzņēmuma līmeņa lietotājs.
    -   Visi pašlaik pieejamie pieprasījuma apjoma prognozes eksperimenti ir pieejami lejupielādei sadaļā [Cortana Analytics galerija](https://gallery.cortanaanalytics.com/). Lai gan Dynamics 365 for Operations pieprasījuma prognozēšanas eksperimenti tiek automātiski integrēti programmatūrā Dynamics 365 for Operations, debitoriem un partneriem ir jāveic to eksperimentu integrācija, kas ir lejupielādēti no [Cortana Analytics galerijas](https://gallery.cortanaanalytics.com/). Tāpēc no [Cortana Analytics galerijas](https://gallery.cortanaanalytics.com/) lejupielādēto eksperimentu lietošana ir sarežģītāka nekā Dynamics 365 for Operations pieprasījuma prognozēšanas eksperimentu lietošana. Ir nepieciešams modificēt eksperimentu kodu tā, lai eksperimentiem tiktu izmantots Dynamics 365 for Operations lietojumprogrammas interfeiss (API).
    -   Pakalpojumā Microsoft Azure Machine Learning Studio var izveidot savus eksperimentus, publicēt tos kā Azure pakalpojumus un izmantot tos, lai ģenerētu pieprasījuma apjoma prognozes.
    -   Ja nav nepieciešama augsta veiktspēja vai ja nav jāapstrādā liels datu apjoms, var izmantot pakalpojuma Machine Learning bezmaksas līmeni. Mēs iesakām sākt darbu, izmantojot šo līmeni īpaši ieviešanas un testēšanas fāzes laikā. Ja ir nepieciešama augstāka veiktspēja un papildu krātuves vieta, var izmantot pakalpojuma Machine Learning standarta līmeni. Lai varētu izmantot šo līmeni, ir nepieciešams Azure abonements un jārēķinās ar papildu izmaksām. Lai iegūtu papildu informāciju par pakalpojuma Machine Learning izmaksām, skatiet vietni <http://aka.ms/machine-learning-price-info>.
-   **Budžeta samazinājums jebkurā atsaistīšanas punktā** — Dynamics 365 for Operations pieprasījuma prognozēšanas pamatā ir šī funkcija, kas sniedz iespēju prognozēt gan atkarīgo, gan neatkarīgo pieprasījumu jebkurā atsaistīšanas punktā.

## <a name="basic-flow-in-demand-forecasting"></a>Pieprasījuma prognozēšanas pamata plūsmas
Šajā diagramma ir redzama pieprasījuma prognozēšanas pamata plūsma. 

[![Pieprasījuma prognozēšanas ievada shēma](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Pieprasījuma apjoma prognozes ģenerēšana sākas programmatūrā Dynamics 365 for Operations. Tiek apkopoti Dynamics 365 for Operations transakciju datu bāzē pieejamie vēsturiskie transakciju dati, un ar tiem tiek aizpildīta izstrādāšanas tabula. Vēlāk izstrādāšanas tabula tiek nodota algoritmiskās mācīšanās pakalpojumam. Veicot nelielus pielāgojumus, varat pievienot izveidošanas tabulai dažādus datu avotus. Kā datu avotus varat izmantot Microsoft Excel failus, komatatdalīto vērtību (CSV) failus un Microsoft Dynamics AX 2009 un Microsoft Dynamics AX 2012 datus. Tāpēc varat ģenerēt pieprasījuma apjoma prognozes, izmantojot vairākās sistēmās glabātos vēsturiskos datus. Tomēr pamatdatiem, piemēram, krājumu nosaukumiem un mērvienībām, ir jābūt vienādiem visos dažādajos datu avotos.

Ja izmantojat Dynamics 365 for Operations pieprasījuma prognozēšanas algoritmiskās mācīšanās eksperimentus, bāzlīnijas prognozes aprēķināšanai tiek meklēta atbilstošākā no piecām laika sērijas prognozēšanas metodēm. Šo prognozēšanas metožu parametrus var pārvaldīt programmatūrā Dynamics 365 for Operations. 

Pēc tam prognozes, vēsturiskie dati un jebkādas iepriekšējo iterāciju pieprasījuma apjoma prognožu izmaiņas ir pieejamas programmatūrā Dynamics 365 for Operations. 

Varat izmantot programmatūru Dynamics 365 for Operations, lai vizualizētu un modificētu bāzlīnijas prognozes. Pirms prognožu izmantošanas plānošanai manuālās korekcijas ir jāapstiprina.

## <a name="limitations"></a>Ierobežojumi
Pieprasījuma prognozēšana programmatūrā Dynamics 365 for Operations ir rīks, kas palīdz ražošanas nozares debitoriem izveidot prognozēšanas procesus. Šis rīks nodrošina galvenās pieprasījuma prognozēšanas risinājuma funkcijas un ir izstrādāts tā, lai to varētu viegli paplašināt. Iespējams, ka pieprasījuma prognozēšana nav pilnībā piemērota debitoriem, piemēram, mazumtirdzniecības, vairumtirdzniecības, noliktavu, transportēšanas vai citu profesionālo pakalpojumu nozarēs.

<a name="see-also"></a>Skatiet arī
--------

[Pieprasījuma prognozēšanas iestatīšana](demand-forecasting-setup.md)

[Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)

[Manuālu bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)

[Koriģētās prognozes autorizēšana](authorize-adjusted-forecast.md)

[Prognozes precizitātes pārraudzība](monitor-forecast-accuracy.md)

[Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi](remove-historical-outliers-calculating-demand-forecast.md)




