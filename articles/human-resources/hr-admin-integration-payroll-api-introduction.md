---
title: Payroll integrācijas API ieviešana
description: Šajā rakstā ir aprakstīts Dynamics 365 Human Resources algu integrācijas API.
author: twheeloc
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33c17dd25477b2c34470fe16ce2927c1781ae147
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846396"
---
# <a name="payroll-integration-api-introduction"></a>Payroll integrācijas API ieviešana


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā dokumentā aprakstīts Dynamics 365 Human Resources Payroll integrācijas API. API iespējo racionalizētu “no gala līdz galam” integrēšanu starp Human Resources un partnerattiecībām algu sistēmā. Pakalpojumā Human Resources sākas integrētā pieredze ar darbinieka profilu, algu, ieturējumu un ieguldījumu informāciju. Nolīgjot darbinieku un ievadot nepieciešamo profilu un apmaksas informāciju sistēmā Human Resources, algu sistēma izvelk šo informāciju, lai to izmantotu algas apstrādes laikā. Visi darbiniekam veiktie atjauninājumi vai maksājuma informācija arī tiek izvilkti izmantošanai vēlākās algas izpildes.

[![Payroll integrācijas plūsma.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Lai iespējotu integrāciju, Human Resources satur šādus komponentus:

- [Funkcionalitāte, lai atzīmētu darbinieku kā gatavu apmaksai.](hr-compensation-payroll.md)
- Integrācijas API, kas atver jauno funkcionalitāti programmu integrēšanai.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Šis API ir veidots Microsoft Dataverse (iepriekš Common Data Service). Visa RESTful mijiedarbība ar šo API tiek veikta, izmantojot Microsoft Dataverse Web API, kas izmanto OData. Šis API ir Dataverse Web API apakškopa. Dataverse Web API nosaka tādus raksturlielumus kā autentifikācija, SLA, pakete, vienlaicīguma kontrole un kļūdu apstrāde.

Vispārīgāku informāciju par Microsoft Dataverse Web API skatiet šeit:

- [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Izmantot Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse izstrādātāja rokasgrāmata](/powerapps/developer/data-platform)

Šajā dokumentācijā ir ietverta detalizēta informācija un izstrādātāja norādījumi par Dataverse Web API izmantošanu, ietverot šādas tēmas:

- [Autentificēties pakalpojumā Microsoft Dataverse ar Web API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Veikt operācijas, izmantojot Web API](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Izmantot Postman ar Web API](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Izmantot izmaiņu izsekošanu, lai sinhronizētu datus ar ārējām sistēmām](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuālie tabulas Human Resources programmā Dataverse

Galapunkti Payroll integrācijai API izmanto Microsoft Dataverse virtuālās tabulas platformas iespējas. Pēc noklusējuma virtuālās tabulas un to saistītie API galapunkti nav izvietoti Human Resources vidēs, iespējojot organizācijas, lai noteiktu, kuri OData galapunkti būs redzami vidē. Lai izmantotu API, videi ir jāizveido Human Resources elementu virtuālās tabulas.

Informāciju par API virtuālo tabulu ģenerēšanu skatiet [Konfigurēt Dataverse virtuālās tabulas](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Datu modelis

Sekojošā diagramma attēlo attiecības API. Vairākiem veidiem ir ārējās atslēgas citām, iepriekš esošām Human Resources entītijām, kas šeit nav attēlotas. Šajā dokumentā ir sniegta informācija par elementiem, kas ir specifiski darbā algas integrācijas scenārijiem. Tomēr Web API ir daudzi citi elementi Dataverse Web API programmai Human Resources, kas var būt atbilstīgi jūsu integrācijai. Dažiem no šiem elementiem ir atsauces ārējās atslēgas attiecībās vai navigācijas rekvizītos.

[![Payroll integrācijas API datu modelis.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Payroll darbinieks un saistītie elementi

Elementi:

- [Algots darbinieks](hr-admin-integration-payroll-api-payroll-employee.md)
- [Algas nodarbinātā adrese](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Algu aprēķina fiksētās atlīdzības plāns](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Algu aprēķina mainīgās atlīdzības plāns](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Algas pozīcijas darbs](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Algas pozīcija](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Skatiet arī

[Algu aprēķina elementu ģenerēšana un pārskatīšana](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Konfigurēt Human Resources parametrus](hr-setup-parameters.md)<br>
[Konfigurēt Human Resources koplietotos parametrus](hr-setup-shared-parameters.md)<br>
[Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Izmantot Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
