---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources 2021. gada 19. aprīlis
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 19. aprīli.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8968c9cb849901288d75cd5e539a57faf0045337
ms.sourcegitcommit: e24e335811727c4b12152323b2bcb25495c08c5b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2021
ms.locfileid: "5934896"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources 2021. gada 19. aprīlis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4113.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Platformas atjauninājums 10.0.17 (41) | -- | [Platformas atjauninājumi programmu Finance and Operations versijai 10.0.17 (2021. gada aprīlis)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Pielāgoto lauku atbalsts atvieglojumu pārvaldības veidlapās | [Pielāgotā lauka atbalsts atvieglojumu pārvaldībai](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Atvieglojumu pārvaldības pārskats](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Izsniegt |  Apraksts |
| --- | --- | --- |
| 552164 | **Saglabāts skats** nedarbojas **Aarbinieku pašapkalpošanās > Atvērtie kursi** kursiem, kas ietver darba kārtību | Ja atvērtos kursos (ESS) ir izmantots saglabāts skats, un vienam no kursiem ir pievienota darba kārtība, šis skats vairs nerādīs vairākas rindas šim kursam |
| 560614 | **Atvieglojumi > Dzīves notikumu opcijas** rāda neatbilstības rīka padoma dokumentācijā un kodu uzvedībā. | Atjauninātie rīku padomi **Dzīves notikumu opcijās**, lai parādītu pareizu uzvedību. |
| 560616 | **Atvieglojumi > Dzīves notikumu opcijas** ir rediģējamas darbinieka atvieglojumu plānā, bet izmaiņas netiek ietekmētas. | Dzīves notikumu opcijas atjauninātā funkcionalitāte pārslēdzas uz iespējošanu vai deaktivizēšanu, pamatojoties uz atkarīgām opcijām, pēc rīka padoma dokumentācijas. |
| 565054 | Ja ir **Papildu piekļuve**, nevar skatīt saraksta saturu **Darbiniekus bez nodarbinātības**. | Šis laidiens risina problēmu, kad **Papildu piekļuve** tika ieslēgta, tikai sistēmas administratori var skatīt saraksta **Darbinieki bez nodarbinātības** saturu. Tā kā šis labojums ir drošības izmaiņas, to ir jāizvēlas līdzekļu pārvaldībā. Tiklīdz līdzeklis ir ieslēgts, tās lomas, kurām ir piekļuve veidlapai, redzēs saturu, pat ja ir paplašināta piekļuve. Plašāku informāciju skatiet [Darbinieki bez nodarbinātības](hr-personnel-workers-without-employment.md). |
| 570586 | Atstājiet pieprasījuma apstiprināšanu neveiksmīgu, ja nodarbinātība beidzas pirms pēdējās šī darbinieka transakcijas visos atvaļinājumu plānos. | Pēc tam, kad nodarbinātība ir beidzies, atvaļinājuma pieprasījuma pārbaude, pamatojoties uz darbinieka atvaļinājuma darījumiem, neizbeidzas.|
| 570783 | Starpuzņēmumu atvaļinājuma iespējošana un deaktivizēšana Human Resources kopīgotos parametros maina, ko atvaļinājuma pieprasījumā redz darbinieki, kas nodarbināti vienā uzņēmumā. | Ja parametrs ir iespējots vai deaktivizēts, darbinieki, kas nodarbināti vienā uzņēmumā, neredz izmaiņas brīvā laika pieprasīšanai. |
| 572343 | Nepieciešamais iemesla kods netiek rādīts, ja līdzeklis ir iespējots starpuzņēmumu atvaļinājumu skata. | Kad starpuzņēmumu atvaļinājumu līdzeklis ir iespējots, iemesla kods tagad tiek rādīts kā paredzēts. |
| 573676 | Nevar pievienot **Periodu** cilnei **atvieglojumu pārvaldības > Saites > Atvieglojumu plāni**. | Fiksētās kļūdas, kuru **Periodu** nevarēja pievienot vai atjaunināt esošajā veidlapā **Atvieglojumu plāns**. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Atvaļinājuma un kavējumu darbplūsmas pieredzes uzlabojumi | [Atvaļinājuma un kavējumu darbplūsmas pieredzes uzlabojumi](https://go.microsoft.com/fwlink/?linkid=2147528) | [Pieprasīt brīvo laiku](hr-employee-self-service-request-time-off.md)|
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detalizētā informācija |
| --- | --- |
| Vadītāja ievadītās prasmes saviem darbiniekiem var automātiski apstiprināt ar darbplūsmu | Drīzumā. |
| Platformas atjauninājums 10.0.18 (42) | Ir ieplānots, ka platformas atjaunināšana 10.0.18 sāks izriti ar pakalpojuma laidienu 2021. gada 17. maijā. Papildinformāciju skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.18 (2021. gada maijs)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Pielāgotā lauka atbalsts atvieglojumu pārvaldības atbilstības noteikumos  | [Pielāgots lauka atbalsts atbilstības apstrādei](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
