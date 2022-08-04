---
title: Konteinera darbību elements
description: Šajā rakstā ir sniegta informācija par konteinera aktivitātēm, kas tiek izmantotas, lai atsekotu pārvadāšanas konteineru progresu.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6a518003f8624ef05ac86be1b963c3f916420278
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167579"
---
# <a name="container-activities-entity"></a>Konteinera darbību elements

[!include [banner](../includes/banner.md)]

Konteinera darbības tiek izmantotas, lai atsekotu pārvadāšanas konteineru progresu. Ieraksts tiek izveidots katrai kājai, kas piešķirta ceļojuma veidnei, kas atlasīta pārvadāšanas konteinera izveides laikā. Ieraksti tiek izveidoti arī tad, kad nosūtīšanas konteiners tiek izveidots, izmantojot datu elementu.

Informācija par tranzīta pārvadāšanas konteinera progresu bieži tiek saņemta no ārēja avota. Konteinera darbību entītija iespējo ārēju avotu, piemēram, kravas ekspediatoru, lai tieši atjauninātu ierakstu. Tāpēc datu manuāla atjaunināšana nav nepieciešama.

## <a name="container-activities-itmcontaineractivityentity"></a>Konteinera aktivitātes (ITMContainerActivityEntity)

Varat izmantot konteinera aktivitāšu elementu (`ITMContainerActivityEntity`), lai izveidotu papildu aktivitāšu ierakstus. Alternatīvi kravas ekspediators var veikt atjauninājumus apstiprinātai **faktiskajai beigu datuma vērtībai**.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Faktiskais pabeigšanas datums | ITMContainerActivityTable.ActualEndDate | Datetime | Nē | Nē |
| Piegādes veids | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Nē | Nē |
| Plānotais beigu datums | ITMContainerActivityTable.ArtimatedDate | Datetime | Nē | Nē |
| Rindas numurs | ITMContainerActivityTable.LineNum | Skaitlis (32, 16) | **Jā** | Nē |
| Piezīmes | ITMContainerActivityTable.Piezīmes | Nvarchar (MAX) | Nē | Nē |
| Aktivitāte | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Nē | **Jā** |
| Nosūtīšanas konteiners | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Jā** | **Jā** |
| Reiss | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Jā** | **Jā** |
| Fāze | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Nē | **Jā** |
| Pakalpojuma sniedzējs | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Nē | Nē |
| Temperatūra | ITMContainerActivityTable.ShipTempermaksājots | Skaitlis (32, 6) | Nē | Nē |
| Kuģis | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Nē | Nē |
| Sākuma datums | ITMContainerActivityTable.StartDate | Datetime | Nē | Nē |

## <a name="tracking-control"></a>Izsekošanas kontrole

Izsekošanas kontroles centrs iespējo norādītā avota lauka atjaunināšanu, kas tiks izraisīts, atjauninot norādīto mērķa lauku. Ja avota lauka un mērķa lauka vērtības tiek atjauninātas, izmantojot konteinera aktivitāšu elementu, mērķa laukā tiks parādīta elementa vērtība. Šī uzvedība ir saistīta ar izsekošanas kontroles ierakstiem, kuriem **ir izpildes laika Tipa** Izveidot *tipa vērtību*.

Izmaksu apgabaliem, **kuru statusa** *·* *atjauninājuma* tipa vērtība ir Izveidot vai Tukšs (kas ir lietotāja definēta vērtība), sistēma atjauninās reisa statusu vai mērķa lauku atbilstoši izsekošanas kontroles konfigurācijai.

## <a name="calculated-fields"></a>Aprēķinātie lauki

Tālāk norādīto lauku vērtības konteinera darbības ierakstā tiek aprēķinātas, pamatojoties uz citu lauku vērtībām. Lai arī šie aprēķinātie lauki nav ietverti datu elements, tie tiks iestatīti, ja ir nodrošināti lauki, uz kuriem balstīti aprēķini.

- **Plānotais dienu** = **plānotais beigu datums** — **sākuma datums**
- **Faktiskās** = **dienas faktiskais beigu datums** – **sākuma datums**
