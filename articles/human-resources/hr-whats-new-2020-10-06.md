---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 6. oktobris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Human Resources 2020. gada 6. oktobris.
author: jcart1106
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4eb3e893c3243d3b2c169cb5a47001d4e0771a20
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887723"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 6. oktobris)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā Dynamics 365 Human Resources. Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.3636.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētais līdzeklis parasti ir pieejams ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Papildu ieskats atvaļinājumu kalendāros | [Papildu ieskata atvaļinājumu kalendāru skatos nodrošināšana](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Grupas un uzņēmuma kalendāra skatīšana](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

>[!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Iespējams, šim rakstam ir pieejami atjauninājumi, lai iekļautu kļūdu labojumus, kas to izlaboja būvējuma laikā pēc šī raksta sākotnējā publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
| --- | --- | --- |
| 448806 | **Noklusējuma identifikācijas veids** tiek eksportēts kā **RecID** HCM parametros | Šīs izmaiņas personāla vadības parametru elementā pievieno papildu kolonnu, kas rāda **Noklusējuma identifikācijas veidu**. |
| 492923 | Uzdevuma ieraksti netiek saglabāti Lifecycle Services (LCS) | Uzdevumu ierakstus tagad var saglabāt LCS. |
| 429950 | Fiksēta kompensācija nebeidzas pareizi, mainot amatu | Mainot darbinieka amatu lapā **Pārsūtīt darbinieku**, beigu atlīdzības datums tika iestatīts vienu dienu pirms amata beigām. Tagad atlīdzības beigu datums ir tāds pats kā amata beigu datums. |
| 467214 | **Izmaksāto algu analīze** tiek parādīta tikai tad, ja opcija **Apmaksas likmes pārvēršanas nosaukums** ir iestatīts uz **Ikgadējs** | Algu izmaksas likmes ar nosaukumu, kas nav **Ikgadējs**, netiek rādītas Atlīdzības analīzē. Ar šo atjauninājumu Atlīdzības analīze tagad izmanto visas apmaksas likmes konvertēšanas. Palaižot pārskatus pēc **Stundas** vai **Alga**, jebkura apmaksas likmes konvertēšana tagad izmanto periodu, kas nav stundas, kurš ir iekļauts filtrā **Alga**. **Stundu** filtrā tiek iekļautas tikai apmaksas likmes ar periodu **Stundas**. |
| 482464 | Skatot **Pārskatus**, skats **Detalizēta informācija** nemainās uz režģa skatu pēc filtra piemērošanas | Pēc filtra piemērošanas pārskata režģis tiek parādīts, kā paredzēts. |
| 483184 | Human Resources neģenerē atvaļinājumu uzkrājumus, atlasot **Pakāpes pamatu** kā **Koriģēto sākuma datumu** ierakstā **Atvaļinājuma reģistrācija** |**Pielāgoto sākuma datumu** aizpilda un izmanto, ģenerējot atvaļinājumu uzkrājumus.  |
| 509731 | Prombūtnes pieprasījums turpmākai darbinieka atbrīvošanai rada problēmas, ja tas attiecas uz prombūtni pēc atbrīvošanas datuma | Tagad prombūtnes pieprasījumus var iesniegt darbiniekiem ar turpmāku atbrīvošanas datuma, ciktāl pieprasījums ir iesniegts pirms atbrīvošanas datuma. |
| 510716 | Atlīdzības analīze ietver gan vīriešu, gan sieviešu dzimtes darbiniekus **Vīriešu vidējā stundas algā** | Atlīdzības analīzē **Vīriešu vidējā stundas alga** par **Atlīdzības demogrāfiskā analīze** ietver sieviešu vidējo algu. Tagad tā ietver tikai vīriešus. |
| 511348 | Atvieglojumu pašapkalpošanās sistēmai ir jāparāda tikai atvieglojumu plāni, kas ir spēkā no šodienas līdz atvieglojumu perioda beigām | Atvieglojumu plāni, kuru derīgums bija beidzies, tika parādīti darbiniekiem lapā **Atvieglojumu reģistrācija**. Šis labojums noņem šos plānus. |
| 512706 | Iestatiet tālāk norādītos laukus kā tikai lasāmus.<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Pogas **Pievienot** un **Noņemt** dimensiju informācijai tika nepareizi iespējotas pēc darbības pabeigšanas. Šis atjauninājums lapai **Amata darbības informācija** padara laukus nerediģējamus, kad darbība ir pabeigta. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Programma Human Resources programmā Microsoft Teams | [Darbinieka atvaļinājuma un prombūtnes pieredze programmā Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Programma Human Resources programmā Teams](./hr-admin-teams-leave-app.md)<br>[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md) |
| Uzlaboti darbplūsmas pieprasījumi un apstiprinājumi | [Organizācijas un personāla vadības darbplūsmas pieredzes uzlabojumi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuālie elementi Dataverse programmai Human Resources | [Pakalpojuma Dynamics 365 Human Resources pamatdatu izvēršana programmā Dataverse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Pakalpojuma Dataverse virtuālo elementu konfigurēšana](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Drīzumā

Nākamajiem laidieniem ir plānoti tālāk norādītie jaunie līdzekļi.

- **Kontrolsaraksta elementi, kas iekļauti Dataverse**: kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami pakalpojumā Dataverse.

- **Atvieglojumu pārvaldības pamatojuma kodi**: atvieglojumu pārvaldības pamatojuma kodi drīz tiks apvienoti ar esošajiem pamatojuma kodiem programmā Human Resources. Ja izveidojāt pamatojuma kodus Priekšrocību pārvaldībā, kas ir garāki par 15 rakstzīmēm, ir jāmaina pamatojuma koda nosaukums Priekšrocību pārvaldībā veidlapā **Pamatojuma kodi** uz tādu, kas ir 15 rakstzīmes vai mazāk. Pēc nosaukuma atjaunināšanas pamatojuma kods būs redzams Personāla vadības sadaļā esošajā pamatojuma koda veidlapā. Šīs izmaiņas būs pieejamas nākotnē un tās neietekmēs jau esošo funkcionalitāti.

- **Pielāgotas saites pārvaldnieka pašapkalpošanās sistēmā**: lai atbalstītu vadītājus, mēs paplašinām iespējas pakalpojumā Vadītāja pašapkalpošanās. Mēs pievienojam iespēju pievienot pielāgotas saites cilnē **Mana grupa**. Šis līdzeklis ir līdzīgs pielāgoto saišu līdzeklim, kas atrodas Darbinieku pašapkalpošanās **Manas informācijas cilne**. Papildinformāciju skatiet sadaļā [Pielāgotas saites pakalpojumā Vadītāja pašapkalpošanās](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2019 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Papildu resursi

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2020. gada laidiena 2. kopumu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]