---
title: "Kravu pārvadāšanas maršrutu ar vairākām pieturām plānošana"
description: "Šajā raksta ir izklāstīti dažādie elementi, ko izmantojat, lai plānotu transportēšanas maršrutus programmatūrā Microsoft Dynamics AX."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a59667014b7f6a8cfbd27463c33cefd5460ecfbc
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Kravu pārvadāšanas maršrutu ar vairākām pieturām plānošana

[!include[banner](../includes/banner.md)]


Šajā raksta ir izklāstīti dažādie elementi, ko izmantojat, lai plānotu transportēšanas maršrutus programmatūrā Microsoft Dynamics AX.

Kompleksiem transportēšanas maršrutiem, kuros ir vairākas pieturvietas, varat izmantot maršrutu plānus un maršrutu ceļvežus. Ja viens un tas pats maršruts tiks izmantots regulāri, varat iestatīt plānotu maršrutu.

## <a name="route-plans"></a>Maršruta plāni
Maršruta plāns ietver maršruta segmentus, kas sniedz informāciju par pieturām, kuras tiek apmeklētas pa ceļam, un par pārvadātājiem, kuri tiek izmantoti katram segmentam. Šī maršruta pieturas jums ir jādefinē kā pārkraušanas punkti. Pārkraušanas punkts var būt kreditors, noliktava, debitors vai pat vienkārši pārkraušanas vieta, kur maināt pārvadātājus. Katram segmentam varat definēt “vietu likmes” dažādām maksām. Daži piemēri:

-   Maksas par braukšanu uz attiecīgajiem segmentiem
-   Maksas par preču saņemšanu
-   Maksa par preču nodošanu

Katram maršruta plānam ir jābūt saistītam ar kādu maršruta ceļvedi.

## <a name="route-guides"></a>Maršruta ceļveži
Maršruta ceļvedis definē kritērijus kravas saskaņošanai ar konkrētu maršruta plānu. Piemēram, varat norādīt izcelsmes pārkraušanas punktu un mērķa pārkraušanas punktu, konteinera tilpuma vai svara ierobežojumus, kā arī sūtījumu pārvadātāju, pakalpojumu vai grupu. Maršrutu ceļveži ir pieejami lapā **Likmju un maršrutu rīks**, kur kravas var manuāli vai automātiski saskaņot ar maršrutiem. Ja maršruta ceļvedis ir paredzēts plānotam maršrutam, tas ir pieejams arī lapā **Kravas plānošanas rīks**.

## <a name="scheduled-routes"></a>Plānoti maršruti
Plānots maršruts ir iepriekš noteikts maršruta plāns, kam ir nosūtīšanas datumu grafiks. Plānoti maršruti no neplānotiem maršrutiem atšķiras ar veidu, kādā tiem tiek piešķirtas kravas. Ja piešķirat neplānotu maršrutu, izmantojot likmju un maršrutu rīku, tad tiek validēti tikai krava un maršruta ceļvedis. Ja piešķirat plānotu maršrutu, tiek ņemti vērā arī datumi un adreses no pasūtījumiem un pārkraušanas punktiem, kā arī datumi maršruta plānā. Jums nav jāizmanto likmju un maršrutu rīka lapa, lai kravas manuāli piešķirtu plānotam maršrutam. Tā vietā varat izmantot kravas plānošanas rīku, lai ierosinātu, ka kravas ir jāveido, pamatojoties uz debitoru adresēm un piegādes datumiem no pārdošanas pasūtījumiem attiecīgajam plānotajam maršrutam. Plānotajiem maršrutiem maršruta plānam būs fiksēti izcelsmes un galamērķa pārkraušanas punkti. Sūtījumu pārvadātājs un pakalpojums parasti būs vienādi visiem segmentiem, bet tie var atšķirties. Galamērķa pārkraušanas punkti tiek izveidoti, izmantojot pa ceļam apmeklēto debitoru pasta indeksus. Vienam maršruta plānam var definēt vairākus maršrutu grafikus. Šim maršruta plānam ir jābūt saistītam ar kādu maršruta ceļvedi. Taču plānotajiem maršrutiem šis plāns var būt saistīts tikai ar vienu maršruta ceļvedi. Maršruta grafiks tiek izmantots tikai tam, lai izveidotu faktiskos maršrutus lapā **Maršruta grafiks**. Kad kravas plānošanas rīkā ierosināt kravas, varat izmantot noklusējuma kravas veidni.

## <a name="load-building-workbench"></a>Noslodzes plānošanas rīks
Lai ierosinātu kravu, Kravas plānošanas rīks izmanto debitoru adreses un piegādes datumus no pārdošanas pasūtījumiem, un pieejamos plānotos maršrutus. Pēc noklusējuma vērtības no maršruta tiek ievadītas rīkā. Taču varat norādīt datumu “no”, kas ir agrāks par maršrutā esošo datumu “no”. Kad krava tiek ierosināta, tiek pārbaudīta piegādes adrese un piegādes datums visiem atvērtajiem pārdošanas pasūtījumiem. Ja piegādes adreses pasta indekss atbilst maršruta plānā esoša pārkraušanas punkta pasta indeksam un ja piegādes datums ir kritērijos atlasītajā diapazonā, tad šai kravai tiek ierosināts pārdošanas pasūtījums. Tiek ņemta vērā arī kravas veidnes noslodze. Vienlaikus tiek ierosināta tikai viena krava. Ja jums ir pārdošanas pasūtījums, kas nav iekļauts, iespējams, jums ir jāizmanto cita kravas veidne (piemēram, kravas veidne lielākai kravas automašīnai vai konteineram) vai jāplāno papildu piegāde.



