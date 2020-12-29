---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 5. novembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4068cf81782d2f9559179b91da31e049c006059
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527124"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 5. novembris)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2598. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Kopēt Core HR instanci

Šīs nedēļas laidienā varat izmantot Microsoft Dynamics Lifecycle Services (LCS), lai kopētu Microsoft Dynamics 365 Talent: Core HR datu bāzi sandbox vidē. Ja jums ir cita smilškastes vide, varat arī kopēt datu bāzi no šīs vides uz mērķtiecīgu smilškastes vidi. Plašāku informāciju skatiet:

- [Plašāka vides pārvaldība](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) Dynamics 365: 2019. gada izlaiduma kopuma 2. plāns

- [Kopēt Core HR instanci](hr-copy-instance.md) programmas Talent dokumentācijā

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service integrēšanas pakešuzdevumi netiek veidoti, kad ir iespējota Common Data Service integrācija (388030)

Šīs izmaiņas izveidos pakešuzdevumus Common Data Service integrācijai, kad tā būs iespējota.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity nemaina personas attēla izmēru augšupielādējot (369469)

Šīs nedēļas laidiens izmaina, kā attēli tiek pārveidoti, lai uzlabotu veiktspēju, kad tos importē, izmantojot datu pārvaldību.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Amats, kas ir pieejams piešķiršanai datumam, var būt pirms aktivizēšanas datuma (340103)

Ar šīm izmaiņām tiks parādīts brīdinājums, ja atlasīsiet **Pieejamo piešķiršanas datumu**, kas ir agrāks par pozīcijas **Aktivizēšanas datumu**.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Nevar izveidot atlīdzības izmaiņu pieprasījumu darbinieku pašapkalpošanās servisā. lai iegūtu pakāpeniskos plānus (376872)

Šis laidiens izlabo problēmu, pieprasot kompensāciju izmaiņas, izmantojot darbinieka pašapkalpošanos, lai iegūtu pakāpeniskos plānus. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Iemesla kods netiek sinhronizēts uz Common Data Service, ja apraksts ir garāks par 30 rakstzīmēm, Core HR atļauj 60 rakstzīmes (352682)

Ar šīm izmaiņām iemesla kodi ar vairāk nekā 30 rakstzīmēm tiks atjaunināti sadaļā Common Data Service. Veiktās izmaiņas Common Data Service tiks atspoguļotas arī Talent.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Adrešu integrēšana no Talent uz Finance and Operations (351961)

Šis laidiens atrisina problēmu, kur programmā Talent atjauninātās adreses netika atjauninātas programmā Finance and Operations. Izmaiņas adrešu blokiem tagad tiks atjauninātas.

## <a name="coming-soon"></a>Drīzumā

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Aplūkojiet [Drukāšanas veiktspējas pārskati](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.

### <a name="feature-management-workspace"></a>Līdzekļu pārvaldības darbvieta

Katrā laidienā tiek pievienoti un atjaunināti līdzekļi. Līdzekļu pārvaldības pieredze nodrošina darbvietu, kur varat skatīt katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju.

Lai iegūtu plašāku informāciju par izmaiņām, kas tiek veiktas ar funkciju pārvaldību, skatīt [Funkciju pārvaldības pārskatu](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
