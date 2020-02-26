---
title: Personāla atlases datu izmaiņu izsekošana
description: Procesa audita funkcija ļauj izsekot, kad notiek kandidātu, vakanču vai darba pieteikumu izmaiņas pārskatu veidošanas vai atbilstības nolūkā.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: c009f82e69bff0e4ea540514de8f9e60eca1e466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006360"
---
# <a name="track-changes-in-recruiting-data"></a>Personāla atlases datu izmaiņu izsekošana

[!include [banner](includes/banner.md)]

Varat izsekot izmaiņām, kas veiktas attiecībā uz kandidātiem, vakancēm un darba pieteikumiem, izmantojot audita apstrādi. Tas ir noderīgi pārskatu veidošanas vai atbilstības nolūkā.

Varat skatīt izsekotos datus pakalpojumā Power BI, izmantojot OData savienotāju. Papildinformāciju skatiet sadaļā [Savienojuma izveide ar OData plūsmām pakalpojumā Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Izsekot izmaiņas
Lai iestatītu izsekošanas izmaiņas personāla atlases datos, veiciet tālāk minētās darbības.

1. [Power Apps](https://web.powerapps.com) atlasiet atbilstošo vidi.

2. Atlasiet **Iestatījumi** (zobrata ikona), izvēlieties **Papildu pielāgojumi** un pēc tam atlasiet **Resursi** sadaļā **Izstrādātāja resursi**. 

3. Lapā **Izstrādātāja resursi** nokopējiet vērtību laukā **Instances tīmekļa API vērtība**. Piemēram, vērtība varētu izskatīties šādi: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Pēc tam varat izpildīt datu vaicājumu no kāda tālāk minēta elementa.
  - Vakanču vēsture (msdyn_jobopeninghistories)
  - Darba pieteikumu vēsture (msdyn_jobapplicationhistories) 
  - Kandidātu vēsture (msdyn_candidatehistories)

## <a name="data-reported"></a>Pārskatā iekļautie dati

Veicot procesa auditu, ir pieejami tālāk minētie dati.

| Pārskatā iekļautie dati | Apraksts |
| --- | --- |
| Mainīja (msdyn_ChangedbyId) | Atsauce uz lietotāju |
| Izveidots (createdon) |  Izmaiņu datums un laiks (UTC) |
| Izmaiņu tips (msdyn_changetype) | Notikušās izmaiņas |
| Kopīgās vērtības kandidātiem, vakancēm <br></br>un darba pieteikumiem | Izveidota<br></br>Ierāmatots |
| Darba pieteikumu vēsture | Pievienots artefakts <br></br>Noņemts artefakts |
| Vakanču vēsture | TODO: pievienots grāmatojums <br></br>TODO: noņemts grāmatojums <br></br>TODO: atjaunināts grāmatojums <br></br>TODO: pievienots dalībnieks <br></br>TODO: noņemts dalībnieks |
| Kandidātu vēsture | Pievienots artefakts <br></br>Noņemts artefakts <br></br>Pievienota darba pieredze <br></br>Noņemta darba pieredze <br></br>Pievienota izglītība <br></br>Noņemta izglītība <br></br>Pievienota prasme <br></br>Noņemta prasme <br></br>Pievienota etiķete <br></br>Noņemta etiķete <br></br>Pievienots sociālais tīkls <br></br>Noņemts sociālais tīkls <br></br>Pievienoti personas dati <br></br>Atjaunināti personas dati<br></br> |
| Mainītie lauki (msdyn_changedfields) | JSON objekts, kurā uzskaitīti mainītie lauki; iespējams, nesaglabā vērtības visiem laukiem.<br></br><br></br>Tipa "Izveidots" un "Atjaunināts" izmaiņām tas uzskaita laukus izveidotajā vai modificētajā ierakstā.<br></br><br></br>Izmaiņu tipam "Pievienots" tiks uzskaitīti lauki, kas atrodas atvasinātajā ierakstā.<br></br><br></br>**Piemērs:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|Darba pieteikumu vēsture | Darba pieteikums (msdyn_JobapplicatonId)<br></br>Statuss (msdyn_status) <br></br>Statusa iemesls (msdyn_statusreason) <br></br>Noraidīšanas iemesls (msdyn_rejectionreason) |
| Vakanču vēsture | Vakance (msdyn_JobopeningId) <br></br>Statuss (msdyn_jobopeningstatus) <br></br>Statusa iemesls (msdyn_jobopeningstatusreason) |
| Kandidātu vēsture | Kandidāts (msdyn_CandidateId) |
