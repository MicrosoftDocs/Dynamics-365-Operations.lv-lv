---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 29. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529688"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 29. oktobris)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2586. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Dzēst puses bez lomām ir jāiestata pēc noklusējuma (371233)

Kad jūs nodrošināt jaunu vidi programmā Talent, funkcija **Dzēst puses, ja nav lomu** ir ieslēgta pēc noklusējuma. Dzēšot darbinieku, ar darbinieku saistītā puse netiek noņemta, ja vien šis iestatījums nav iestatīts. Šīs izmaiņas ierobežo ierakstu dublikātus globālajā adrešu grāmatā, kad nepieciešams importēt, mainīt vai atkārtoti importēt darbiniekus.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Melnraksta un atcelto atvaļinājumu pieprasījumi ir jāatļauj dzēst programmā Common Data Service (376999)

Ar šīm izmaiņām tagad varat dzēst atvaļinājumu pieprasījumus ar statusu **Melnraksts** vai **Atcelts** Common Data Service.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Papildu saraksta vērtības pielāgotos laukos netiek parādītas Common Data Service pēc noklikšķināšanas uz Pielietot Pielāgoto lauku formā (379599).

Kad pievienojat jaunas saraksta vērtības esošam pielāgotam laukam, kas jau ir sinhronizēts ar Common Data Service, tās tagad ir pieejamas Common Data Service pēc izmaiņu piemērošanas formā **Pielāgoti lauki**.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Piemērot pārbaudes kontrolsarakstus visās juridiskajās personās, ja pastāv vairāk nekā viens darbs (371270)

Šīs nedēļas laidienā varat pielietot kontrolsarakstus darbiniekiem ar vairāk nekā vienu darbu **Darbinieku forma > Kontrolsaraksti**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Priekšrocības atvērtās reģistrācijas priekšskatījuma funkcija ir noņemta

Saistībā ar mūsu paziņojumu [Stratēģiskās investīcijas Core HR Drive Operational Excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blogā, korporācija Microsoft noņem atvieglojumus, kas atvērti reģistrācijai no publiskās priekšskatīšanas. Nākotnē tiks izlaista jauna funkcionalitāte. Ražošanas priekšrocību atvērta reģistrēšanās funkcija netiek atbalstīta.

## <a name="coming-soon"></a>Drīzumā

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Aplūkojiet [Drukāšanas veiktspējas pārskati](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.

### <a name="feature-management-workspace"></a>Līdzekļu pārvaldības darbvieta

Katrā laidienā tiek pievienoti un atjaunināti līdzekļi. Līdzekļu pārvaldības pieredze nodrošina darbvietu, kur varat skatīt katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju.

Lai iegūtu plašāku informāciju par izmaiņām, kas tiek veiktas ar funkciju pārvaldību, skatīt [Funkciju pārvaldības pārskatu](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]