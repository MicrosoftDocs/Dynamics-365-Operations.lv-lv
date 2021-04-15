---
title: Dokumentu drukāšanas pārskats
description: Varat drukāt dokumentus, izmantojot lokālu printeri vai tīklam pievienotu ierīci. Šajā rakstā ir sniegts apskats par to, kā tiek drukāti dokumenti.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d41e299f0076e1016e8ddae8584bfec338a73a9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749397"
---
# <a name="document-printing-overview"></a>Dokumentu drukāšanas pārskats

[!include [banner](../includes/banner.md)]

Varat drukāt dokumentus, izmantojot lokālu printeri vai tīklam pievienotu ierīci. Šajā rakstā ir sniegts apskats par to, kā tiek drukāti dokumenti.

## <a name="printing-overview"></a>Drukāšanas apskats

Programma nodrošina integrētus pakalpojumus un klienta lietojumprogrammas, kas sniedz iespēju viegli ģenerēt, glabāt un izplatīt dokumentus, kuri atbalsta biznesa aktivitāti. Varat drukāt dokumentus, izmantojot lokālu printeri vai tīklam pievienotu ierīci. Turklāt klientā varat tiešā veidā eksportēt lapas un pārskatus PDF failu vai Microsoft Office dokumentu formātā. Visbeidzot, sadalītā noslodze jums ļauj drukāt biznesa dokumentus tieši no mobilās ierīces, izmantojot tīkla resursus. Lai gan drukāšanas prasības var būt dažādas, visām nozarēm parasti ir jāizveido izdrukātās biznesa dokumentu kopijas, izmantojot programmu. Dokumentu drukāšana tīkla ierīcēs no viesotām programmām rada virkni unikālu problēmu. Daži piemēri:

- Lietotāja ierīcē var nebūt pieejami drukas draiveri.
- Lietotāja ierīce var nebūt savienota ar uzņēmuma tīklu.

Izmantojot atvēlēto resursdatoru un izpildot dažas vienkāršas procedūras, sistēmas administratori var konfigurēt izvietojumus tā, lai lietotāji tieši no biznesa programmām varētu drukāt tīkla ierīcēs.

### <a name="application-printing-scenarios"></a>Programmas drukāšanas scenāriji 

Nākamajā tabulā ir aprakstīti trīs primārie drukāšanas scenāriji.

| Scenārijs                        | Mērķis                                                      | Risinājums |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Rādītā satura drukāšana        | Izdrukāt tieši to, kas pārlūkprogrammā tiek rādīts pašlaik.             | Pārlūkprogrammai tiek ģenerēta “drukāšanai draudzīga” tīmekļa lapas versija. |
| 2. Interaktīva drukāšana         | Izdrukāt precīzu dokumentu lokāli pievienotā ierīcē. | Varat eksportēt pārskata PDF versiju un lejupielādēt to pārlūkprogrammā. |
| 3. Drukāšana tīkla ierīcē | Nosūtīt precīzu dokumentu uz domēna printera ierīci.     | Precīzais dokuments tiek nosūtīts uz klienta programmu, kas darbojas serverī, kurš tiek viesots klienta domēnā. |

Tā kā atkarībā no scenārija risinājumi ir dažādi, programmas nodrošina tālāk aprakstītos iebūvētos pakalpojumus un rīkus, lai palīdzētu lietotājiem sasniegt savus mērķus.

- **1. scenārijs** tiek atbalstīts pārlūkprogrammas HTML5 klienta renderēšanā.
- **2. scenārijs** izmanto klienta programmas un Microsoft 365 pakalpojumus.
- **3. scenārijam** ir nepieciešams pakalpojumā Microsoft Azure viesoto pakalpojumu un klienta lietojumprogrammu atbalsts.

Papildus platformai, kas tiek izvietota Azure abonementā, Finance and Operations programmas debitoriem nodrošina integrētu, pirmās puses Azure programmu, kas viņiem palīdz dokumentu drukāšanai vienkāršāk izmantot domēnā viesotas ierīces.

## <a name="service-overview"></a>Pakalpojuma apskats
Kamēr viesoto programmu izveidotie dokumenti gaida izdrukāšanu tīklam pievienotā ierīcē, šie dokumenti tiek saglabāti Azure BLOB krātuvē. [Dokumentu maršrutēšanas aģenta instalēšana, lai iespējotu tīkla printēšanu](install-document-routing-agent.md) izmanto Azure autentifikāciju, lai izveidotu drošu kanālu uz Azure pakalpojumiem.

**Izpildes secība**

1. Pakalpojumā Microsoft SQL Server Reporting Services (SSRS) tiek ģenerēts pārskats, un tas tiek saglabāts Azure BLOB krātuvē. Pievienotie printera iestatījumi tiek glabāti kopā ar dokumentu.
2. Dokumentu maršrutēšanas aģents veic vaicājumus par aktīviem darbiem Azure Service Bus rindā.
3. Dokumentu maršrutēšanas aģents šo dokumentu lejupielādē un spolē uz tīkla printeri.

No klienta atkarīgais risinājums ļauj lietotājiem pārvaldīt savu drukas vajadzību apjomu. Lietotāji, kuriem ir liela apjoma drukāšanas darbu slodzes, var instalēt daudzus Dokumentu maršrutēšanas aģentus, lai palielinātu vienlaicīgo drukāšanas operāciju skaitu. Savukārt citiem lietotājiem viņu gaidāmo drukāšanas nepieciešamību izpildei ir nepieciešamas tikai dažas Dokumentu maršrutēšanas aģentu instalācijas.

### <a name="service-components-for-network-printing"></a>Pakalpojuma komponenti drukāšanai tīklā

Nākamajā diagrammā ir redzami pamata komponenti, kas palīdz atbalstīt tīkla drukāšanas operācijas.

[![pakalpojuma-komponenti-drukāšanai-tīklā\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Ņemiet vērā, ka vienu printeri var reģistrēt vairākiem dokumentu maršrutēšanas aģentiem. Lai atrisinātu printera preferences, viesotais pakalpojums izmanto tīkla ceļu, kas unikāli identificē katru tīkla printeri. Līdz ar to pat gadījumos, kad printeris ir reģistrēts vairākiem klientiem, programmu pieejamo printeru sarakstā tas tiek rādīts kā viena atlase.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]