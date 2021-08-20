---
title: Jaunumi un izmaiņas programmatūrā Dynamics 365 Human Resources 2021. gada 22. jūnijs
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 22. jūniju.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 897c25df96017c5be1ae789027d178ca6b3ccc0410b4f65c7d2557b39e840134
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735355"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Jaunumi un izmaiņas programmatūrā Dynamics 365 Human Resources 2021. gada 22. jūnijs

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4258.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Informējiet darbiniekus bez nodarbinātības līdzekļa - Kad ir ieslēgta papildu piekļuve un līdzekļu pārvaldībā ir atspējots līdzeklis **Skatīt visus darbiniekus bez nodarbinātības**, veidlapā darbiniekiem bez nodarbinātības tiek parādīts reklāmkarogs. Reklāmkarogs liks lietotājam ieslēgt līdzekli **Skatīt visus darbiniekus bez nodarbinātības**. | Nav attiecināms| [Nodarbinātie bez nodarbinātības](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Pielāgotā lauka atbalsts atvieglojumu pārvaldības atbilstības noteikumiem | [Pielāgots lauka atbalsts atbilstības apstrādei](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Atbilstības noteikumu konfigurēšana](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Atvaļinājuma uzkrājumu darījumu auditēšana | Nav attiecināms | [Atvaļinājuma uzkrājumu darījumu auditēšana](hr-leave-and-absence-accrue.md)|
| Atvaļinājuma un kavējumu darbplūsmas pieredzes uzlabojumi | [Atvaļinājuma un kavējumu darbplūsmas pieredzes uzlabojumi](https://go.microsoft.com/fwlink/?linkid=2147528) | [Pieprasīt brīvo laiku](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma |  Apraksts |
| --- | --- | --- |
| 583052 | Lietotājs, kas saņem atsauksmes, var rediģēt saņemtās atsauksmes | Kad darbinieks saņemot atsauksmi veiktspējas žurnālā atlasa **Pievienot ārējo saiti**, veidlapa kļūst rediģējama, ļaujot darbiniekam rediģēt saņemtos veiktspējas datus. |
| 522281 | Darbinieku skaita atlasīšana kompensācijas struktūrā kompensācijas pārvaldībā izraisa nepareizus rezultātus| Skatoties detalizēto darbinieku skaitu kompensāciju plānos no kompensāciju darbvietas, tagad tiek rādīts pareizais darbinieku skaits. |
| 580683 | Lietotājiem, kuriem ir piešķirtas darbinieka un vadītāja lomas, nevar pievienot piezīmes vai atjaunināt veiktspējas žurnālu | Lietotājiem, kuriem ir piešķirtas darbinieka un vadītāja lomas, nevar pievienot piezīmes vai atjaunināt veiktspējas žurnālu. Lietotājs saņem kļūdu "Nevar izveidot ierakstu veiktspējas žurnāla ierakstā (HcmPerfJournal). Drošības politikas atļauja ir liegta." |
| 583077 | Darbinieka dzimšanas datums atvaļinājumu un kavējumu uzņēmuma kalendārā rāda nepareizu datumu | Lietotāji varēs apskatīt pareizo darbinieku dzimšanas datumu atvaļinājumu un kavējumu uzņēmuma kalendārā. |
| 586996 | Ja piekļuve ir ierobežota vienam uzņēmumam, starpuzņēmumu atvaļinājuma skata lidzeklis izraisa to, ka atlikumi ir tukši | Lietotāji var pareizi skatīt darbinieka atvaļinājuma atlikumus, ja ir iespējots starpuzņēmumu atvaļinājumu skats. |
| 581014 | Starpuzņēmumu atvaļinājumu un kavējumu skata iespējošana rada kļūdu, skatot nākotnes atlikumus | Kļūdas ir novērstas, kad lietotāji skata nākotnes atvaļinājumu atlikumus ar iespējotu starpuzņēmumu atvaļinājumu skatu. |
| 509404 | Nodaļas darbinieku skaita analīze, kas neietekmē darbinieku kustību starp nodaļām. | Ja darbinieks migrē no vienas nodaļas uz citu, nodaļas darbinieku skaita dati neatspoguļo veco nodaļu, no kuras mirgēja darbinieks, ja pašreizējā gadā ir beidzies pozīcijas detalizētās informācijas derīguma termiņš. |
| 584851 | Atvieglojuma kredīta prorācijas kārtula "Nav" nekad nenodrošina kredītu |Brīvā režīma kredīta prorācijas kārtulas "Nav" rezultātā darbinieki saņem nulle kredītu atvieglojumu periodam, neatkarīgi no tā, kad tie nolīgti darbā. Tas ir fiksēts tā, ka darbiniekam būtu jāsaņem pilnīgus brīvā režīma kredītus, ja tie tika pieņemti darbā pirms atvieglojumu perioda sākuma, un nevienu, ja tie tiek pieņemts darbā pēc perioda sākuma. |
| 584897 | Pienakuma 'Lietot pamata ārējo funkcionalitāti' duplicēšana rada kļūdu | Mēģinot dublēt pienākumu 'Lietot pamata ārējo funkcionalitāti', lietotājs saņēma kļūdu, "Nevarēja atrast objektu ar identifikatoru UserDefinedAppHostDialogView." |
| 575692 | Uzkrāšanas atvaļinājums un prombūtne nav pieejamas gaidošajiem darbiniekiem | Atvaļinājumu un kavējumu uzkrāšanu var palaist turpmākajos nolīgšanās darbā, kad tiek aktivizēts **Racionalizēts darbinieka ieraksts**. |
| 580110 | Uzņēmuma pievienošana algu integrācijai atiestata integrāciju, lai izmantotu visas entītijas pat tad, ja opcija ir iestatīta uz neatsvaidzināt projektu | Ja debitors ir noņēmis entītijas vai mainījis datu projektu algu integrācijai, un ir iestatīta opcija, lai novērstu automātisku projekta atsvaidzināšanu, jauna uzņēmuma pievienošana integrācijai ignorē šo iestatījumu un atsvaidzina projektu.  |
| 584518 |Reģistrēt atvieglojumu apstrādes veiktspējas problēmu | Šajā labojumā ir apskatītas veiktspējas problēmas mantojuma atvieglojumu reģistrācijas procesā. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detalizētā informācija |
| --- | --- |
| Platformas atjauninājums 10.0.19 (43) | Ir ieplānots, ka platformas atjaunināšana 10.0.19 sāks izriti ar pakalpojuma laidienu 2021. gada 28. jūnijā. Papildinformāciju skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.19 (2021. gada jūnijs)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Pakalpojumu rādīšanas gadu pārslēgšanās | Šī iespēja sniedz iespēju izmantot dažādus datumus, lai aprēķinātu pakalpojuma gadus, kas attēloti vaidlapā **Racionalizēta darbinieka ieraksts** un veidlapā **Cilvēki**.  Tas būs pieejams Human Resources parametros. |
|  Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu | [Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Pilnvarojuma pielikumi īpašiem atvaļinājumu tipiem | Šis līdzeklis ļauj administratoriem pievienot pielikumus, iesniedzot atvaļinājuma pieprasījumus noteiktiem atvaļinājuma veidiem. |
|  Konfigurēt atvaļinājuma vienības pa atvaļinājuma daļām | Šis līdzeklis ļauj administratoriem konfigurēt atvaļinājumu vienības (stundas vai dienas) katram atvaļinājuma tipam.  |
| Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai | [Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
