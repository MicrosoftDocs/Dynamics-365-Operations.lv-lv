---
title: Sensor Data Intelligence sākumlapa
description: Šajā rakstā sniegts pārskats par Sensora datu informāciju. Organizācijas var izmantot šo iespēju, lai vadītu biznesa procesus Microsoft Dynamics 365 Supply Chain Management, balstoties uz Interneta things (IoT) signālus no mašīnām un aprīkojuma ražošanas stāvā.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ba030364056db8b0524de22aacbc6528ef77813b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689862"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensor Data Intelligence sākumlapa

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensora datu informācija, kas nepieciešama Microsoft Dynamics 365 Supply Chain Management, ļauj organizācijām vadīt biznesa procesus Piegādes ķēžu pārvaldībā, balstoties uz interneta things (IoT) signālus no mašīnām un aprīkojuma ražošanas stāvā. Tā ir atjaunināta, pārdēvēta *IoT Intelligence funkcijas versija, kas* iepriekš bija pieejama piegādes ķēžu pārvaldībai.

Sensora datu informācija ļauj veikt sekojošos uzdevumus:

- Apkopojiet informāciju no mašīnām un aprīkojuma, lai atjauninātu uzturēšanas līdzekļu skaitītāja vērtības Piegādes ķēžu pārvaldībā un vadītu prognozējošu uzturēšanu.
- Iestatiet risinājumu, izmantojot vienkāršu onboarding Microsoft Dynamics vedni, nevis manuāli instalēt un konfigurēt komponentus pakalpojumos Lifecycle Services (LCS).
- Izvietojiet komponentus savā abonementā, lai jums būtu elastīgāks pārvaldīt Azure komponentus.
- Konfigurējiet, mēriet un pagariniet risinājumu kā biznesa loģiku, kas darbojas uz Azure komponentiem. Šie komponenti tagad tiek pārvaldīti jūsu abonementā. Tāpēc tos var pielāgot, kā nepieciešams, lai atbilstu jūsu unikālajām biznesa vajadzībām.

## <a name="business-scenarios"></a>Biznesa scenāriji

Sensora datu informācija ļauj izmantot vairākus funkcionalitātes veidus, katru no kuriem sistēmā attēlo *specifisks* scenārijs. Katrs scenārijs nodrošina specializētu konfigurācijas opciju kopu sistēmā, kā norādīts šajā tabulā.

| Scenārijs | Apraksts |
|---|---|
| [Līdzekļa dīkstāve](sdi-scenario-asset-downtime.md) | Precīzi atseciet iekārtu līdzekļu efektivitāti, izmantojot sensora datus, lai izsekotu iekārtas dīkstāves laiku. |
| [Līdzekļu uzturēšana](sdi-scenario-asset-maintenance.md) | Samaziniet uzturēšanas izmaksas un paildzināt pamatlīdzekļu lietošanas ilgumu, uzlabojot uzturēšanas plānus, balstoties uz pamatlīdzekļiem kritisko kontrolpunktu sensora rādījumiem. |
| [Mašīnas statuss](sdi-scenario-equipment-downtime.md) | Nodrošiniet operāciju efektivitāti, izmantojot sensora lasījumus, lai paziņotu plānotājiem par iekārtu aiziešanu un nodrošinātu potenciālās aizkavēšanās palielināšanas opcijas. |
| [Preces kvalitāte](sdi-scenario-product-quality.md) | Nodrošiniet produktu partiju kvalitāti, salīdzinot sensora lasījumus katras produkta paketes faktiskajiem rekvizītiem, piemēram, sietu, temperatūras vai pielāgošanai noteiktus kvalitātes rādītājus. Sistēma informēs lietotājus, ja rodas novirzes. |
| [Ražošanas aizkaves](sdi-scenario-production-delays.md) | Izmantojiet sensora lasījumus, lai salīdzinātu faktisko cikla laiku ar plānoto cikla laiku, un paziņotu supervizoriem, kad ražošana nav ieplānota. Tad supervizori var veikt atbilstošus pasākumus, lai nodrošinātu maksimālās operācijas efektivitāti. |

## <a name="architecture"></a>Arhitektūra

Šī arhitektūras diagramma sniedz risinājumu un tā komponentu apskatu.

![Sensora datu inteliģences arhitektūras diagramma.](media/sdi-architecture.png "Sensora datu inteliģences arhitektūras diagramma")
