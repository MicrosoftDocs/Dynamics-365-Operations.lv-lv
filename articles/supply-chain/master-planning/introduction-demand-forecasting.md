---
title: Pārskats par pieprasījuma prognozēšanu
description: Pieprasījuma prognozēšanas tiek izmantota, lai prognozētu debitoru pasūtījumu neatkarīgu pieprasījumu pēc pārdošanas pasūtījumiem un atkarīgos pieprasījums jebkurā atsaistīšanas punktā. Uzlabotās pieprasījuma apjoma prognozes samazināšanas kārtulas nodrošina lielisku lielapjoma pielāgošanas risinājumu.
author: roxanadiaconu
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1033432d0d820516d8c9b2f58f27241351e7c64b
ms.sourcegitcommit: 2e7454c07adfc05164121307050f6f24303d36d2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/10/2020
ms.locfileid: "3550044"
---
# <a name="demand-forecasting-overview"></a>Pārskats par pieprasījuma prognozēšanu

[!include [banner](../includes/banner.md)]

Pieprasījuma prognozēšanas tiek izmantota, lai prognozētu debitoru pasūtījumu neatkarīgu pieprasījumu pēc pārdošanas pasūtījumiem un atkarīgos pieprasījums jebkurā atsaistīšanas punktā. Uzlabotās pieprasījuma apjoma prognozes samazināšanas kārtulas nodrošina lielisku lielapjoma pielāgošanas risinājumu.

Lai ģenerētu bāzlīnijas prognozi, uz pakalpojumā Azure mitināto Microsoft Azure mašīnmācīšanās pakalpojumu tiek nosūtīts kopsavilkums par vēsturiskajām transakcijām. Tā kā šis pakalpojums netiek kopīgots starp lietotājiem, to var ērti pielāgot, lai tas atbilstu konkrētas nozares prasībām. Programmatūru Supply Chain Management varat izmantot, lai vizualizētu un pielāgotu prognozi un skatītu prognozes precizitātes izpildes pamatrādītājus (KPI).

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

-   **Modularitāte** — pieprasījuma prognozēšanas ir modulārs un viegli konfigurējams process. Šo funkciju var ieslēgt un izslēgt, mainot konfigurācijas atslēgu sadaļā **Tirdzniecība** &gt; **Krājumu prognoze** &gt; **Pieprasījuma prognozēšana**.
-   **Atkārtota Microsoft Stack izmantošana** – algoritmiskā mācīšanās, kas ir daļa no platformas Microsoft Cortana Analytics Suite, sniedz iespēju ātri vienkārši izveidot prognozējošas analīzes eksperimentus, piemēram, pieprasījuma novērtēšanas eksperimentus, izmantojot R algoritmus vai Python programmēšanas valodas un vienkāršu vilkšanas un nomešanas interfeisu.
    -   Pieprasījuma prognozēšanas eksperimentus var lejupielādēt, tos var mainīt, lai tie atbilstu uzņēmējdarbības prasībām, publicēt kā tīmekļa pakalpojumu Azure vietnē un izmantot tos, lai ģenerētu pieprasījuma apjoma prognozes. Eksperimentus var lejupielādēt, ja Supply Chain Management ražošanas plānotāja abonementu esat iegādājies kā uzņēmuma līmeņa lietotājs.
    -   Visi pašlaik pieejamie pieprasījuma apjoma prognozes eksperimenti ir pieejami lejupielādei sadaļā [Cortana Analytics galerija](https://gallery.cortanaanalytics.com/). Lai gan Pieprasījuma prognozēšanas eksperimenti tiek automātiski integrēti programmatūrā Supply Chain Management, klientiem un partneriem ir jāveic to eksperimentu integrēšana, ko viņi lejupielādē no [Cortana Analytics galerijas](https://gallery.cortanaanalytics.com/). Līdz ar to sadaļā [Cortana analīzes galerijā](https://gallery.cortanaanalytics.com/) pieejamos eksperimentus nevar vienkārši izmantot kā Finance and Operations prognozēšanas eksperimentus. Eksperimentu kods ir jāmaina tā, lai tiek izmantots lietojumprogrammas Finance and Operations programmēšanas interfeiss (API).
    -   Varat izveidot savus eksperimentus pakalpojumā Microsoft Azure Machine Learning Studio (klasiskā), publicēt tos kā pakalpojumus platformā Azure un izmantot tos pieprasījuma apjoma prognožu ģenerēšanai.
    -   Ja nav nepieciešama augsta veiktspēja vai ja nav jāapstrādā liels datu apjoms, var izmantot pakalpojuma Machine Learning bezmaksas līmeni. Mēs iesakām sākt darbu, izmantojot šo līmeni īpaši ieviešanas un testēšanas fāzes laikā. Ja ir nepieciešama augstāka veiktspēja un papildu krātuves vieta, var izmantot pakalpojuma Machine Learning standarta līmeni. Lai varētu izmantot šo līmeni, ir nepieciešams Azure abonements un jārēķinās ar papildu izmaksām. Plašāku informāciju par algoritmiskās mācīšanās izcenojumu skatiet tēmā [Machine Learning Studio izcenojums](https://aka.ms/machine-learning-price-info).
-   **Budžeta samazinājums jebkurā atsaistīšanas punktā** — Pieprasījuma prognozēšana ir atkarīga no šīs funkcionalitātes, kas ļauj prognozēt gan atkarīgo, gan neatkarīgo pieprasījumu jebkurā atsaistīšanas punktā.

## <a name="basic-flow-in-demand-forecasting"></a>Pieprasījuma prognozēšanas pamata plūsmas
Šajā diagramma ir redzama pieprasījuma prognozēšanas pamata plūsma. 

[![Pieprasījuma prognozēšanas ievada shēma](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Pieprasījuma apjoma prognozes ģenerēšana sākas Supply Chain Management. Tiek apkopoti Supply Chain Management transakciju datu bāzē pieejamie vēsturiskie transakciju dati, un ar tiem tiek aizpildīta izstrādāšanas tabula. Vēlāk izstrādāšanas tabula tiek nodota algoritmiskās mācīšanās pakalpojumam. Veicot nelielus pielāgojumus, varat pievienot izveidošanas tabulai dažādus datu avotus. Var izmantot tādus datu avotus kā Microsoft Excel faili, komatatdalīto vērtību (CSV) faili un programmu Microsoft Dynamics AX 2009 un Microsoft Dynamics AX 2012 dati. Tāpēc varat ģenerēt pieprasījuma apjoma prognozes, izmantojot vairākās sistēmās glabātos vēsturiskos datus. Tomēr pamatdatiem, piemēram, krājumu nosaukumiem un mērvienībām, ir jābūt vienādiem visos dažādajos datu avotos.

Ja tiek izmantoti pieprasījuma prognozēšanas pakalpojuma Machine Learning eksperimenti, bāzlīnijas prognozes aprēķināšanai tiek meklēta atbilstošākā piecu laika sēriju prognozēšanas metode. Šo prognozēšanas metožu parametrus var pārvaldīt programmatūrā Supply Chain Management. 

Pēc tam prognozes, vēsturiskie dati un jebkādas iepriekšējo iterāciju pieprasījuma apjoma prognožu izmaiņas ir pieejamas programmatūrā Supply Chain Management. 

Programmatūru Supply Chain Management varat izmantot, lai vizualizētu un modificētu bāzlīnijas prognozes. Pirms prognožu izmantošanas plānošanai manuālās korekcijas ir jāapstiprina.

## <a name="limitations"></a>Ierobežojumi
Pieprasījuma prognozēšana ir rīks, kas palīdz ražošanas nozares debitoriem izveidot prognozēšanas procesus. Šis rīks nodrošina galvenās pieprasījuma prognozēšanas risinājuma funkcijas un ir izstrādāts tā, lai to varētu viegli paplašināt. Iespējams, ka pieprasījuma prognozēšana nav pilnībā piemērota debitoriem, piemēram, komercijas, vairumtirdzniecības, noliktavu, transportēšanas vai citu profesionālo pakalpojumu nozarēs.

### <a name="demand-forecast-variant-conversion-limitation"></a>Pieprasījuma apjoma prognozes varianta konversiju ierobežojumi

Ģenerējot pieprasījuma apjoma prognozi, mērvienība (UOM) katra varianta konversijai netiek pilnībā atbalstīta, ja krājumu UOM atšķiras no pieprasījuma apjoma prognozes UOM.

Prognozes ģenerēšana (**Krājumu UOM > Pieprasījuma apjoma prognozes UOM**) izmanto preču UOM konversiju. Ielādējot vēsturiskos datus pieprasījuma apjoma prognozes ģenerēšanai, preču līmeņa UOM konversija tiks izmantota vienmēr, konvertējot no krājumu UOM uz pieprasījuma apjoma prognozes UOM, pat ja konversijas ir definētas varianta līmenī.

Prognozes autorizēšanas pirmā daļa (**Pieprasījuma apjoma prognozes UOM > Krājumu UOM**) izmanto preču UOM konversiju. Prognozes autorizēšanas otrā daļa (**Krājumu UOM > Pārdošanas UOM**) izmanto variantu UOM konversiju. Kad ģenerētā pieprasījuma apjoma prognoze ir autorizēta, konvertēšana uz krājumu UOM no pieprasījuma apjoma prognozes UOM tiks veikta, izmantojot preču līmeņa UOM konversiju. Tajā pašā laikā konvertēšana starp krājumu vienībām un pārdošanas UOM ņems vērā varianta līmeņa definētās konversijas.

Ņemiet vērā, ka pieprasījuma apjoma prognozes UOM nav jābūt ar noteiktu nozīmi. To var definēt kā “Pieprasījuma apjoma prognozes vienība”. Katrai precei varat definēt konversiju, kas ir 1:1 ar krājumu UOM.

<a name="additional-resources"></a>Papildu resursi
--------

[Pieprasījuma prognozēšanas iestatīšana](demand-forecasting-setup.md)

[Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)

[Manuāla bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)

[Autorizēt koriģēto pieprasījuma apjoma prognozi](authorize-adjusted-forecast.md)

[Prognozes precizitātes pārraudzība](monitor-forecast-accuracy.md)

[Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi](remove-historical-outliers-calculating-demand-forecast.md)

[Pieprasījuma prognozēšanas funkcionalitātes paplašināšana](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



