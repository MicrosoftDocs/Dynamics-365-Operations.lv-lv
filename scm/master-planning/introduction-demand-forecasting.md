---
title: "Pieprasījuma prognozēšana pārskats"
description: "Pieprasījuma prognozēšanas tiek izmantota, lai prognozētu debitoru pasūtījumu neatkarīgu pieprasījumu pēc pārdošanas pasūtījumiem un atkarīgos pieprasījums jebkurā atsaistīšanas punktā. Pastiprinātu pieprasījumu budžeta samazināšanas noteikumiem sniedz ideālu risinājumu masu pielāgošanas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Pieprasījuma prognozēšana pārskats

Pieprasījuma prognozēšanas tiek izmantota, lai prognozētu debitoru pasūtījumu neatkarīgu pieprasījumu pēc pārdošanas pasūtījumiem un atkarīgos pieprasījums jebkurā atsaistīšanas punktā. Pastiprinātu pieprasījumu budžeta samazināšanas noteikumiem sniedz ideālu risinājumu masu pielāgošanas.

Lai ģenerētu bāzlīnijas prognozi, vēsturisko transakciju apkopojums tiek nosūtīts uz Microsoft Azure Machine pakalpojumu, ko vieso Azure. Tā kā šis pakalpojums netiek kopīgots starp lietotājiem, to var ērti pielāgot, lai tas atbilstu konkrētas nozares prasībām. Dynamics 365 operācijām var izmantot, lai vizualizēt prognoze, koriģēt budžetu un apskatīt veiktspējas pamatrādītāji (KPI) par prognozes precizitāti.

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

-   **Modularitāte** — pieprasījuma prognozēšanas ir modulārs un viegli konfigurējams process. Var ieslēgt funkcionalitāti un izslēgt, mainot konfigurācijas atslēga pie **tirdzniecības**&gt;**krājumu budžeta**&gt;**pieprasījuma prognozēšanas**.
-   **Atkārtota izmantošana Microsoft steka** – Microsoft uzsāka Machine Learning platform februārī 2015. gadā. Mašīna mācībām, kas tagad ir daļa no Microsoft Cortana Analytics Suite, ļauj ātri un viegli izveidot prognožu analīzi eksperimentus, piemēram, pieprasījuma novērtējums eksperimentus, izmantojot algoritmus R vai Python programmēšanas valodām un vienkāršu vilkšanas un nomešanas lietotāja saskarni.
    -   Jūs tās varat lejupielādēt Dynamics 365 operācijas pieprasījuma prognozēšanai eksperimentu, tās mainīt, lai apmierinātu jūsu biznesa prasības, tos publicēt kā tīmekļa pakalpojumu par debeszils un izmantot tos, lai radītu pieprasījumu prognozes. Eksperimenti ir pieejami lejupielādei, ja esat iegādājies Dynamics 365 periodiskām darbībām par ražošanas plānotājs kā uzņēmuma līmeņa lietotāja.
    -   Visi pašlaik pieejamie pieprasījuma apjoma prognozes eksperimenti ir pieejami lejupielādei sadaļā [Cortana Analytics galerija](https://gallery.cortanaanalytics.com/). Tā kā Dynamics 365 operācijas pieprasījuma prognozēšanai eksperimentu automātiski ir integrēti ar Dynamics 365 operācijām, klientiem un partneriem jāuztur eksperimenti, kas tās lejupielādēt no integrācijas [Cortana Analytics galerija](https://gallery.cortanaanalytics.com/). Tādēļ no eksperimentiem [Cortana Analytics galerija](https://gallery.cortanaanalytics.com/) nav tik vienkārša kā Dynamics 365 izmantošanai operāciju pieprasījuma prognozēšanai eksperimentu. Nedrīkst modificēt eksperimentu kodu, tā, ka tiek izmantota Dynamics 365 darbības lietojumprogrammu programmēšanas interfeisu (API).
    -   Pakalpojumā Microsoft Azure Machine Learning Studio var izveidot savus eksperimentus, publicēt tos kā Azure pakalpojumus un izmantot tos, lai ģenerētu pieprasījuma apjoma prognozes.
    -   Ja nav nepieciešama augsta veiktspēja vai ja nav jāapstrādā liels datu apjoms, var izmantot pakalpojuma Machine Learning bezmaksas līmeni. Mēs iesakām sākt darbu, izmantojot šo līmeni īpaši ieviešanas un testēšanas fāzes laikā. Ja ir nepieciešama augstāka veiktspēja un papildu krātuves vieta, var izmantot pakalpojuma Machine Learning standarta līmeni. Lai varētu izmantot šo līmeni, ir nepieciešams Azure abonements un jārēķinās ar papildu izmaksām. Lai iegūtu papildu informāciju par pakalpojuma Machine Learning izmaksām, skatiet vietni <http://aka.ms/machine-learning-price-info>.
-   **Budžeta samazināšanas spinu jebkurā** -pieprasījuma prognozēšanas Dynamics 365 par darbības balstās uz šo funkcionalitāti, kas ļauj budžeta atkarīgajiem un neatkarīgajiem pieprasījums jebkurā brīdī atdalīšanu.

## <a name="basic-flow-in-demand-forecasting"></a>Pieprasījuma prognozēšanas pamata plūsmas
Šajā diagramma ir redzama pieprasījuma prognozēšanas pamata plūsma. 

[![pieprasījuma prognozēšanas ieviešanas shēma](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Pieprasījuma prognoze, paaudze sāk Dynamics 365 operācijām. Vēsturisko transakciju datus no Dynamics 365 operāciju darījumu bāzes tiek savākti un pieturvietas tabulu aizpilda. Pieturvietas tabulā tiek piegādāta vēlāk Machine Learning pakalpojumu. Veicot minimālu pielāgošanu, pieturvietas tabulu var pievienot dažādus datu avotus. Datu avotiem var ietvert Microsoft Excel failus, komatatdalīto vērtību (CSV) failus un datus no Microsoft Dynamics AX 2009 un Microsoft Dynamics AX 2012. Tāpēc jūs varat izveidot pieprasījuma prognozes, ko uzskata par vēsturiskiem datiem, kas ir sadalīts starp vairākām sistēmām. Tomēr pamatdatiem, piemēram, krājumu nosaukumiem un mērvienībām, ir jābūt vienādiem visos dažādajos datu avotos.

Ja izmantojat Dynamics 365 operācijas pieprasījuma prognozēšanas Machine Learning eksperimentus, viņi meklē atbilstošāko starp pieciem laikrindu prognozēšanas metodes, lai aprēķinātu bāzes prognoze. Šīs prognozēšanas metodes parametriem tiek pārvaldītas Dynamics 365 operācijām. 

Prognozes, vēsturiskajiem datiem un visas izmaiņas, kas tika veiktas iepriekšējās iterācijas pieprasījuma prognozes pēc tam ir pieejami Dynamics 365 operācijām. 

Dynamics 365 operācijām var izmantot, lai vizualizētu un modificēt bāzlīnijas prognozes. Pirms prognožu izmantošanas plānošanai manuālās korekcijas ir jāapstiprina.

## <a name="limitations"></a>Ierobežojumi
Pieprasījuma prognozēšana programmā Dynamics 365 operācijām ir rīks, kas palīdz klientiem pārstrādājošās rūpniecības izveidotu prognozēšanas procesu. Tā piedāvā pieprasījuma prognozēšanas risinājumu pamata funkcionalitāti, un ir projektēts tā, ka to var viegli paplašināt. Pieprasījuma prognozēšana, varētu būt labākais piemērots klientiem rūpniecības nozarēs, piemēram, mazumtirdzniecība, vairumtirdzniecība, noliktavu, transporta vai citi profesionālie pakalpojumi.

<a name="see-also"></a>Skatiet arī
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


