---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 23. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 66419d9093cff68aa6109b22ab57bcb46ac6c718
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772900"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 23. oktobris)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract
Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard
Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2569. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Finance and Operations Platform update 30 lietojumprogramma

Plašāku informāciju skatiet [Kas jauns vai mainīts Platform update 30 for Finance and Operations lietotnēs (November 2019)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Noņemt priekšrocības atvērtās reģistrācijas priekšskatījuma funkciju

Saistībā ar mūsu sludinājumu [Stratēģiskās investīcijas Core HR Drive Operational Excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blogā, korporācija Microsoft noņem atvieglojumus, kas atvērti reģistrācijai no publiskās priekšskatīšanas 2019. gada 18. oktobrī. Tā vietā nākotnē tiks izlaista jauna funkcionalitāte. Atbalsta atvērtās reģistrācijas funkcija, kas pašlaik atrodas publiskajā priekšskatījumā, netiks atbalstīta.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Kļūda, atlasot valsti/reģionu darbinieku formā otro reizi (350294)

Ar šīs nedēļas laidienu problēma tika izlabota, atlasot valsti/reģionu **Darbinieku** formā.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Finanšu dimensijas vērtības noklusējums kombinācijas rādīšanas laukam, kad opcija Neatļaut manuālu ievadi, ir iestatīts kā patiess (340097)

Veicot šīs izmaiņas, pēc finanšu dimensijas iestatīšanas un opciju izmantošanas, lai neatļautu manuālu ievadi, sistēma pareizi norādīs dimensiju vērtību **Kombinācijas displeja** laukā.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Jaunu attiecību tipi ir jāpievieno Attiecību meklēšanā personīgo kontaktu formā (347691)

Šajā laidienā ir iekļautas jaunas iespējas, lai pievienotu jaunu attiecību tipus **Attiecību tipi** tabulā un atspoguļotu šīs izmaiņas personisko kontaktpersonu attiecību meklēšanā.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Papildu saraksta vērtības pielāgotajos laukos netiek atspoguļotas Common Data Service (379599)

Izmantojot šīs nedēļas laidienu, jaunas saraksta vērtības pievienošana esošam pielāgotam laukam, kas jau ir sinhronizēts ar Common Data Service, jaunās izdošanas saraksta vērtības tagad tiks rādītas pēc izmaiņu veikšanas elementā.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>Nodarbinātības noteikumu lapā visu darbinieku nodarbinātības noteikumi parādās pēc Excel programmas atvēršanas (348073)

Ar šo laidienu programmā Excel atvērsies tikai atlasītie darbinieku nodarbinātības noteikumi. Tiek turēta cieņā ar visa uzņēmuma drošība.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>Common Data Service nav saistības starp Darba kalendāra brīvdienu elementu un darba kalendāra elementu (324178)

Šīs attiecības tika pievienotas kopā ar laidienu. Šīs izmaiņas aktivizēs darbinieka darba dienas, kas tiks rādītas PowerApps. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Kļūda, izmantojot darbinieku pašapkalpošanās darbplūsmas ar konfigurējamām hierarhijām (370132)

Šajā laidienā ir pieejams labāks ziņojumapmaiņas veids, kā konfigurēt darbplūsmas, izmantojot konfigurējamas hierarhijas. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Sistēma ļauj izveidot jaunas pozīcijas, kur Pieejamais piešķiršanas datums ir agrāks par Aktivizēšanas datumu (340103)

Veicot šīs izmaiņas, tiks parādīts brīdinājums, kad pozīcijas **Pieejams norīkojumam** datums ir pirms **Aktivizēšanas** pozīcijas datuma.

## <a name="coming-soon"></a>Drīzumā

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Aplūkojiet [Drukāšanas veiktspējas pārskati](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.

### <a name="feature-management-workspace"></a>Līdzekļu pārvaldības darbvieta

Katrā laidienā tiek pievienoti un atjaunināti līdzekļi. Līdzekļu pārvaldības pieredze nodrošina darbvietu, kur varat skatīt katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju.

Lai iegūtu plašāku informāciju par izmaiņām, kas tiek veiktas ar funkciju pārvaldību, skatīt [Funkciju pārvaldības pārskatu](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
