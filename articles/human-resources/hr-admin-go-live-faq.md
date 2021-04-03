---
title: Bieži uzdotie jautājumi par palaišanu
description: Šajā tēmā uzskaitīti bieži uzdotie jautājumi par to, kā sākt strādāt ar Dynamics 365 Human Resources ieviešanas projektu.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d667d94983d5c8f8e6140259922396d4299a15e3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467600"
---
# <a name="go-live-faq"></a>Bieži uzdotie jautājumi par palaišanu 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā uzskaitīti bieži uzdotie jautājumi par to, kā sākt strādāt ar Dynamics 365 Human Resources ieviešanas projektu. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Kad varu konfigurēt un pieprasīt savu ražošanas vidi? 

Parasti ražošanas vide tiek izvietota, ja ir ievērota atbilstība tālāk minētajiem kritērijiem.

- Visi pielāgojumi ir ar kodu pabeigti.
- Lietotāju akceptēšanas testēšana (UAT) ir pabeigta.
- Debitors ir parakstījis risinājumu.
- Nav bloķējošu problēmu darba sākšanai. 

Kad kvalificētie debitori ir šajā posmā, Microsoft FastTrack darba grupa strādās ar projekta grupu, lai veiktu darba sākšanas novērtējumu. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Kādi ir priekšnosacījumi ražošanas vides izvietošanai? 

Priekšnosacījumu sarakstu skatiet tēmā  [Sagatavošanās darba sākšanai](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Kas ir darba sākšanas novērtējums?  

Darba sākšanas novērtējums ir daļa no  [Microsoft FastTrack programmas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). Šīs pārskatīšanas laikā risinājuma arhitekts izvērtē, vai ieviešanas projekts ir gatavs veiksmīgai pārslēgšanai un darba sākšanai. Šī pārskatīšana ir obligāta katram ieviešanas projektam, pirms varat pieprasīt sākt darbu ražošanas vidē. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Mūsu smilškastes vides ir izvietotas centrālajā ASV datu centrā. Mēs vēlamies, lai mūsu ražošanas vides tiktu izvietotas ASV Rietumu datu centros. Vai es varu atlasīt ASV Rietumus kā datu centru savā ražošanas konfigurācijā? 

LCS neierobežo iespēju atlasīt citu datu centru, kad izvietojat Human Resources vidi, bet mēs stingri iesakām neizvēlēties citu datu centru.  

Ja vēlaties, lai jūsu ražošanas vide būtu ASV Rietumu datu centrs, vispirms atkārtoti izvietojiet savas smilšu vides ASV Rietumu datu centrā, pārbaudiet tās un izrakstieties. 

Informāciju par pareizā datu centra atlasīšanu skatiet tēmā [Tīkla prasības](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Kāda līmeņa piekļuve man ir Azure resursiem manās Human Resources vidēs?  

Piekļuve Human Resources vidēm ir ierobežota. Jūs nevarat piekļūt virtuālajai mašīnai (VM) vai Microsoft interneta informācijas pakalpojumiem (IIS). Jūs arī nevarat piekļūt datu bāzei, izmantojot Microsoft SQL Server Management Studio. 

Lai gan nevarat piekļūt saviem Azure resursiem vai Dynamics 365 Human Resources videi tieši, ir papildu līdzekļi, ko varat izmantot, lai piekļūtu saviem datiem:

- Azure SQL datu bāzi varat izvietot savā Azure nomniekā un izmantot līdzekli Savas datu bāzes izmantošana (BYOD), lai sinhronizētu datus. Plašāku informāciju skatiet tēmā [Savas datu bāzes izmantošana (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- Varat izmantot Dataverse integrāciju, lai sinhronizētu atlases elementus Dataverse datu bāzē. Papildinformāciju skatiet šeit: [Dataverse tabulas](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Cik bieži mana ražošanas datu bāze tiek dublēta? 

Datu bāzes tiek aizsargātas ar automātisko dublēšanu šādā biežumā:

| Dublējuma veids | Biežums |
| --- | --- |
| Pilna datu bāzes dublēšana | Reizi nedēļā |
| Diferenciālā datu bāzes dublēšana | Ik pēc 12-24 stundām |
| Darījumu žurnāla dublēšana | Ik pēc 5–10 minūtēm |

Microsoft saglabā pietiekamu dublēšanu, lai nodrošinātu punkta laikā atjaunošanu (PITR) pēdējo 14 dienu laikā. 

Plašāku informāciju skatiet  [Uzzināt par automātisko SQL datu bāzu dublēšanu](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Vai varu pieprasīt manas ražošanas datu bāzes dublējuma kopiju? 

Nr.p.k. Tomēr varat iesniegt datu bāzes atsvaidzināšanas pakalpojuma pieprasījumu, lai iekopētu ražošanas vidi savā smilškastes vidē. Azure SQL datu bāzi varat izvietot savā Azure nomniekā un izmantot līdzekli BYOD, lai sinhronizētu datus no savas ražošanas vides. Plašāku informāciju skatiet tēmā [Savas datu bāzes izmantošana (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Kā es varu pārvietot savu smilškastes vidi uz ražošanu darba sākšanai? 

Tā kā kopēšanas līdzeklis nav pieejams, lai pārvietotu vidi no smilškastes uz ražošanas vidi, jums jāizmanto datu pakotnes, lai pārvietotu datus uz ražošanas vidi.  

Mēs iesakām uzturēt skaidru to elementu sarakstu, kas konfigurēti jūsu smilškastē, visa projekta gaitā. Pēc tam testējiet pārslēgšanas un migrācijas procesu visām datu pakotnēm, kas nepieciešamas jūsu darba sākšanai. Jums ir manuāli jāpārvieto visas datu pakotnes ražošanas vidē, kad esat gatavs sākt darbu. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Ko darīt, ja mana ražošanas vide nedarbojas? 

Lai ziņotu par ražošanas pārtraukumu, izpildiet procesu, kas aprakstīts tēmā  [Ziņošana par ražošanas pārtraukumu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage). 

 ## <a name="see-also"></a>Skatiet arī

 [Sagatavošana publicēšanai](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]