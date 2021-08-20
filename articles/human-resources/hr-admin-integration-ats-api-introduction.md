---
title: Kandidāta izsekošanas sistēmas integrācijas API ievads
description: Šajā tēmā aprakstīts Dynamics 365 Human Resources kandidāta izsekošanas sistēmas (ATS) integrācijas API.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dacca05c47f50099ca1420413ef80430b7ebf1850a799d1208328581699242d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751222"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Kandidāta izsekošanas sistēmas integrācijas API ievads

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Dynamics 365 Human Resources kandidāta izsekošanas sistēmas (ATS) integrācijas API. API nolūks ir nodrošināt racionalizētu integrāciju starp Dynamics 365 Human Resources un partnera ATS.

![AtS integrācijas plūsma.](media/hr-admin-integration-ats-api-introduction-flow.png)

Integrētā pieredze Human Resources sākas, kad darbā pieņemšanas vadītājs izveido personāla atlases pieprasījumu. Kad pieprasījums ir aktivizēts, ATS izvelk detalizētu informāciju pieprasījumam izveidot personāla atlases projektu. Pēc tam tas seko darbā pieņemšanas konveijeram, lai atlasītu un pieņemtu kandidātu šiem amatiem. Visbeidzot ATS pabeidz aprites integrāciju uz serveri, nosūtot atlasītā kandidāta ierakstu Human Resources. Pēc tam kandidāta ierakstam var veikt vairākas uzņēmuma apstiprināšanas un darbplūsmām, lai izveidotu darbinieka ierakstu.

Lai iespējotu integrāciju, Human Resources ir pievienojusi šādus komponentus:

1.  Personāla atlases pieprasījuma izveides funkcionalitāte.
2.  Izvērsts kandidāta profils un saistītās darbplūsmas.
3.  Integrācijas API, kas atver jauno funkcionalitāti programmu integrēšanai.

Papildinformāciju par personāla atlases pieprasījumu un kandidātu funkcionalitātes iestatīšanu un lietošanu skatiet sadaļā [Darba kandidātu pieņemšana darbā](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Šis API ir veidots Microsoft Dataverse (iepriekš Common Data Service). Visa RESTful mijiedarbība ar šo API tiek veikta, izmantojot Microsoft Dataverse Web API, kas izmanto OData. Šis API ir Dataverse Web API apakškopa. Dataverse Web API nosaka tādus raksturlielumus kā autentifikācija, SLA, pakete, vienlaicīguma kontrole un kļūdu apstrāde.

Vispārīgāku informāciju par Microsoft Dataverse Web API skatiet šeit:

- [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Izmantot Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse izstrādātāja rokasgrāmata](/powerapps/developer/data-platform)

Iepriekš minētajā dokumentācijā ir ietvertas detalizētas un izstrādātāja norādes par Dataverse Web API izmantošanu, piemēram, [autentifikācijas pārvaldību](/powerapps/developer/data-platform/webapi/authenticate-web-api), [darbību veikšanu](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postman izmantošanu ar API](/powerapps/developer/data-platform/webapi/use-postman-web-api) un [izmaiņu izsekošanas vai delta marķieru izmantošanu](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) ar API.

### <a name="option-sets"></a>Opciju kopas

Šajā dokumentā aprakstītais ATS integrācijas API datu modelis ietver opciju kopas, kas nodrošina ar elementa rekvizītiem saistītas uzskaitījuma vērtības. Papildinformāciju par darbu ar opciju kopām Dataverse Web API skatiet sadaļā [Opciju kopu izveide un atjaunināšana, izmantojot Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets). Opciju kopas tiek definētas katrai Dataverse videi.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuālie tabulas Human Resources programmā Dataverse

Galapunkti ATS integrācijai API izmanto Microsoft Dataverse virtuālās tabulas platformas iespējas. Pēc noklusējuma virtuālās tabulas un to saistītie API galapunkti nav izvietoti Human Resources vidēs, iespējojot organizācijas, lai noteiktu, kuri OData galapunkti būs redzami vidē. Lai izmantotu API, videi ir jāizveido Human Resources elementu virtuālās tabulas. 

Informāciju par API virtuālo tabulu ģenerēšanu skatiet [Konfigurēt Dataverse virtuālās tabulas](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Datu modelis

Datu modelis ir centrēts ap diviem galvenajiem elementiem:

- **RecruitingRequest** pārstāv pieprasījumu ATS pieņemt darbā vienu vai vairākus atvērtus amatus. Vaicājuma piemēru skatiet sadaļā [Vaicājuma piemērs personāla atlases pieprasījumam](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** parāda informāciju par kandidātu, kurš pieņēmis amata piedāvājumu. **Persona** parāda personu, kas ir kandidāts. Personai uzņēmumā var būt vairākas lomas, piemēram, kandidāts, darbinieks, nodarbinātais vai darbuzņēmējs. Vaicājuma piemēru skatiet sadaļā [Vaicājuma piemērs kandidāta pieņemšanai darbā](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Sekojošā diagramma attēlo attiecības API. Vairākiem veidiem ir ārējās atslēgas citām, iepriekš esošām Human Resources entītijām, kas šeit nav attēlotas. Šajā dokumentā ir sniegta informācija par elementiem, kas ir specifiski darbā pieņemšanas integrācijas scenārijiem. Tomēr Web API ir daudzi citi elementi Dataverse Web API programmai Dynamics 365 Human Resources, kas var būt atbilstīgi jūsu integrācijai. Piemēram, jums var būt nepieciešama detalizēta informācija par darbiniekiem, darbiem, amatiem vai citiem šeit nedefinētiem elementiem. Daudziem no šiem elementiem ir atsauces ārējās atslēgas attiecībās vai navigācijas rekvizītos.

![ATS integrācijas API datu modelis.](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Darbā pieņemšanas pieprasījums un saistītie elementi un opciju kopas

Piemēra vaicājums: 

- [Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Elementi:

- [Pieņemšanas darbā pieprasījums](hr-admin-integration-ats-api-recruiting-request.md)
- [Darbā pieņemšanas pieprasījuma amats](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Personāla atlases pieprasījuma prasmes](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Personāla atlases pieprasījuma izglītība](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Darbā pieņemšanas pieprasījuma atrašanās vieta](hr-admin-integration-ats-api-recruiting-request-location.md)

Opciju kopas:

- [Darba nodokļu atvieglojumu statuss](hr-admin-integration-ats-api-job-exempt-status.md)
- [Personāla atlases pieprasījuma pozīcijas statuss](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Personāla atlases pieprasījuma statuss](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Normatīvā darba kategorija](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Kandidāts, kuru pieņemt darbā un saistīties elementi un opciju kopas

Piemēra vaicājums:

- [Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Elementi:

- [Kandidāts pieņemšanai darbā](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Persona](hr-admin-integration-ats-api-person.md)
- [Personas izglītība](hr-admin-integration-ats-api-person-education.md)
- [Personas profesionālā pieredze](hr-admin-integration-ats-api-person-professional-experience.md)
- [Personas adrese](hr-admin-integration-ats-api-person-address.md)
- [Puses kontaktpersona](hr-admin-integration-ats-api-party-contact.md)
- [Personas prasme](hr-admin-integration-ats-api-person-skill.md)
- [Novērtējuma līmenis](hr-admin-integration-ats-api-rating-level.md)
- [Personas sertifikāts](hr-admin-integration-ats-api-person-certificate.md)
- [Sertifikāta veids](hr-admin-integration-ats-api-certificate-type.md)
- [Personas izvērtēšana](hr-admin-integration-ats-api-person-screening.md)
- [Izvērtēšanas tipi](hr-admin-integration-ats-api-screening-types.md)
- [Personas identifikācijas numurs](hr-admin-integration-ats-api-person-identification-number.md)

Opciju kopas:

- [Kandidātu integrācijas rezultāts](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Tukšs Jā Nē](hr-admin-integration-ats-api-blank-yes-no.md)
- [Izpildes statuss](hr-admin-integration-ats-api-completion-status.md)
- [Kontaktpersonas tips](hr-admin-integration-ats-api-contact-type.md)
- [Izglītības kredīta bāze](hr-admin-integration-ats-api-education-credit-basis.md)
- [Dzimums](hr-admin-integration-ats-api-gender.md)
- [Ģimenes stāvoklis](hr-admin-integration-ats-api-marital-status.md)
- [Gada mēneši](hr-admin-integration-ats-api-months-of-year.md)
- [Nē Jā](hr-admin-integration-ats-api-no-yes.md)
- [Perioda vienība](hr-admin-integration-ats-api-period-unit.md)
- [Izvērtēšanas biežums](hr-admin-integration-ats-api-screening-frequency.md)
- [Izvērtēšanas biežums ǵenerāts no](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Prasmju līmeņa veids](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Skatiet arī

[Kandidātu pieņemšana darbā](hr-personnel-recruit.md)<br>
[Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Izmantot Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>
[Opciju kopu izveide un atjaunināšana, izmantojot Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]