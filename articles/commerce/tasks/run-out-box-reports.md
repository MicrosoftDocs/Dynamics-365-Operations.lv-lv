---
title: Ārpus zonu pārskatu ģenerēšana un palaišana
description: Izmantojiet šo uzdevumu ceļvedi, lai palaistu ārpus zonu pārskatus Headquarters no dažādām darbvietām un vaicājumiem, un pārdošanas pārskatiem, kas atrodas sadaļā Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d148fa36a116860af8c44043d90759b8a2d76fb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414081"
---
# <a name="generate-and-run-out-of-box-reports"></a>Ārpus zonu pārskatu ģenerēšana un palaišana

[!include [banner](../includes/banner.md)]

Izmantojiet šo uzdevumu ceļvedi, lai palaistu ārpus zonu pārskatus Headquarters no dažādām darbvietām un vaicājumiem, un pārdošanas pārskatiem, kas atrodas sadaļā Commerce.

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo ierakstu, ir USRT. Šis ieraksts ir paredzēts lietotajiem ar sistēmas administratora lomu.

## <a name="launch-reports-from-workspaces"></a>Pārskaitu palaišana no darbvietām
1. Dodieties uz Retail un Commerce > Preces un kategorijas > Kategorijas un preču pārvaldība.
2. Noklikšķiniet uz šīs bultiņas, lai izvērstu vai sakļautu sadaļu Pārskati.
3. Noklikšķiniet uz Labāko preču pārskats.
4. Ievadiet datumu laukā No datuma.
5. Laukā Līdz datumam ievadiet datumu.
6. Laukā Kanāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
7. Koka struktūrā atlasiet Contoso mazumtirdzniecība\Contoso mazumtirdzniecība ASV\Centrāli\Houston.
    * Tiek parādīta noklusējuma Commerce organizācijas hierarhija, kas tiks lietota mazumtirdzniecības pārskatiem.   Dodieties uz Organizācijas administrēšana > Organizācijas > Organizācijas hierarhijas nolūki un izvēlēties Commerce pārskati, savukārt sadaļā Piešķirtās hierarhijas pārbaudiet hierarhijas nosaukumu, kurai ir atzīmēta noklusējuma kolonna. Kā daļu no demonstrācijas datiem (izmantoti šī uzdevuma ierakstā) jūs ievērojāt, ka noklusējuma organizācijas hierarhija pārskatiem ir Veikali pēc reģiona.     
8. Noklikšķiniet uz Labi.
9. Laukā Skats atlasiet opciju.
10. Laukā Pēc atlasiet opciju.
11. Noklikšķiniet uz Labi.

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a>Palaist pārskatus no vaicājumiem un pārdošanas pārskatiem
1. Dodieties uz Retail un Commerce > Pieprasījumi un pārskati > Pārdošanas pārskati > Kategorijas pārdošanas pārskats.
2. Ievadiet datumu laukā No datuma.
3. Laukā Līdz datumam ievadiet datumu.
4. Laukā Kanāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
5. Koka struktūrā atlasiet Contoso mazumtirdzniecība\Contoso mazumtirdzniecība ASV\Rietumi\Sietla.
    * Tiek parādīta noklusējuma Commerce organizācijas hierarhija, kas tiks lietota mazumtirdzniecības pārskatiem. Dodieties uz Organizācijas administrēšana > Organizācijas > Organizācijas hierarhijas nolūki un izvēlēties Commerce pārskati, savukārt sadaļā Piešķirtās hierarhijas pārbaudiet hierarhijas nosaukumu, kurai ir atzīmēta noklusējuma kolonna. Kā daļu no demonstrācijas datiem (izmantoti šī uzdevuma ierakstā) jūs ievērojāt, ka noklusējuma organizācijas hierarhija pārskatiem ir Veikali pēc reģiona.     
6. Noklikšķiniet uz Labi.
7. Noklikšķiniet uz Labi.

## <a name="export-an-hq-reports"></a>HQ pārskatu eksportēšana
1. Dodieties uz Retail un Commerce > Pieprasījumi un pārskati > Pārdošanas pārskati > Organizācijas pārdošanas pārskats.
2. Ievadiet datumu laukā No datuma.
3. Laukā Līdz datumam ievadiet datumu.
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Eksportēt.
6. Noklikšķiniet uz PDF.

