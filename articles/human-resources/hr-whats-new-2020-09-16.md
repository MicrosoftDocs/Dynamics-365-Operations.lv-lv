---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 16. septembris)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 16. septembri.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b07bfb27bbe5e546dac9d72666b3225cc202670
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890703"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 16. septembris)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3557. Iekavās esošie skaitļi blakus dažiem līdzekļiem attiecas uz atbalsta atsauces numuriem portālā Lifecycle Services (LCS).

## <a name="included-in-this-release"></a>Šajā laidienā iekļauts

-  [Saglabātie skati — vispārīga pieejamība](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Papildinformāciju skatiet sadaļā [Saglabātie skati](../fin-ops-core/fin-ops/get-started/saved-views.md). 

- Veidlapā **Amata darbības** ir atjaunināts dimensiju režģis un jauns dialogs (469495).

- Iestatot **Ierobežot piekļuvi nodarbinātā informācijai** uz Jā, ja ir **Papildu piekļuve** programmas **Human Resources koplietojamajiem parametriem**, atvieglojumu veidlapās tiks rādīti tikai atbilstošie nodarbinātie (393384).

- Jaunas kalendāra ģenerēšanas opcijas **WorkCalendar** elementā (477055):<br>- Noklusējuma beigu laiks<br>- Noklusējuma sākuma laiks<br>- Piektdiena kā darba diena<br>- Pirmdiena kā darba diena<br>- Sestdiena kā darba diena<br>- Svētdiena kā darba diena<br>- Ceturtdiena kā darba diena<br>- Otrdiena kā darba diena<br>- Trešdiena kā darba diena<br>- Brīvdienas ID darba kalendārā

- Entītija **LeaveBankTransactionV1** tagad ietver iemesla kodu (477823).

- Tagad varat saglabāt uzdevumu ierakstus (492923).

- Tagad dati tiek veiksmīgi publicēti no **HCMWorkerContactEntity** (427620).

- Kopsavilkuma cilne **Atlīdzība** tagad tiek rādīta nodarbinātā veida līgumdarbinieka veidlapā **Nodarbināto darbības** (482494).

- Lauki **Līmenis** un **Plāns** tagad ir obligāti, ja iestatāt **Fiksētā atlīdzība**. Šos laukus atstājot tukšus, tiek parādīts kļūdas ziņojums (482497).

- Lauka **Plāna veids** **Atvieglojumi** tagad ir nolaižamā saraksta veidā (488768).

- Sistēmas administratori tagad saņem paziņojumu, ja pielāgots lauks tiek dzēsts no programmas Human Resources (481408).

- Darbinieka darba attiecību pārtraukšanas laikā Human Resources darbojas kā paredzēts un nemaina atlasīto uzņēmumu pēc tam, kad tiek parādīta bloķēšana (479877). 

- Vadītāji vairs nevar pievienot ciparu kolonnu, izmantojot personalizāciju (485317).

- Vadītāji vairs nevar noņemt datu diapazona filtru no identifikācijas numuriem, kuriem beidzas derīgums (485321).

- Kad lauks **Pakļautība** ir tukšs, amata informācija joprojām tiek rādīta, novietojot kursoru virs amata (433328).

- Tagad darbinieki var skatīt atvieglojumu plāna informāciju pakalpojumā Darbinieka pašapkalpošanās (481676).

- Tagad darbinieki var redzēt visus reģistrētos kursus (429048).

- Tagad varat ierobežot lapas **Profesionālie sertifikāti** skatīšanas opcijas. Varat ierobežot skatīšanas opcijas pašreizējām juridiskajām personām, pēc nodarbinātā statusa un pēc nodarbinātā veida (451501). 


## <a name="in-preview"></a>Priekšskatījumā

### <a name="human-resources-app-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Plašāku informāciju skatiet:

- [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 1. laidiena plānā
- [Programma Human Resources risinājumā Teams](./hr-admin-teams-leave-app.md) Human Resources dokumentācijā

### <a name="human-resources-app-in-teams-preview-features"></a>Programma Human Resources programmas Teams priekšskatījuma līdzekļos
 
-  **Paziņojumi**: iesniedzēji un pārtraukuma pieprasījumu apstiprinātāji tiek informēti par Personāla vadības lietotni programmā Teams. Apstiprinātāji var apstiprināt vai noraidīt brīvā laika pieprasījumus. Iesniedzēji tiks informēti, ja pieprasījums tika apstiprināts vai noraidīts. Plašāku informāciju skatiet:
   - [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 2. laidiena plānā
   - [Iespējot paziņojumus programmai Human Resources risinājumā Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) Human Resources dokumentācijā
   - [Ieslēgt vai izslēgt Teams paziņojumus atsevišķiem lietotājiem](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) Human Resources dokumentācijā
   - [Teams paziņojumi](./hr-teams-leave-app.md#respond-to-teams-notifications) Human Resources dokumentācijā
   - [Skatīt jūsu grupas atvaļinājumu kalendāru](./hr-teams-leave-app.md#view-your-teams-leave-calendar) Human Resources dokumentācijā
 
- **Vadītāja brīvā laika kalendārs**: vadītāji var redzēt apstiprinātās un gaidāmās prombūtnes to tiešajiem pārskatiem kalendāra skatā. Šis skats nodrošina vieglu izpratni par to, kad viņu grupas dalībnieki ir prom no darba. Plašāku informāciju skatiet:
   - [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 2. laidiena plānā
   - [Skatīt jūsu grupas atvaļinājumu kalendāru](./hr-teams-leave-app.md#view-your-teams-leave-calendar) Human Resources dokumentācijā

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi (477004)

Tagad ir pieejama jauna opcija, lai pozicionētu sarakstu **Man piešķirtie darbplūsmas elementi** informācijas paneļa labajā kolonnā. Ar šīm izmaiņām visi darba elementi un uzdevumu saraksti tiek rādīti tajā pašā apgabalā. Iespējojiet šo funkcionalitāti, ieslēdzot **Priekšskatījums - darbplūsmas ērtību uzlabojumi** līdzekļu pārvaldībā. Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu ieslēgšanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

Šis līdzeklis arī veicina darbplūsmas opcijas, kas parādās personāla darbību veidlapās. Darbplūsmas opcijas parādās arī virs darbību kopsavilkuma cilnes, lai tām varētu ātri piekļūt. Plašāku informāciju skatiet: 

- [Organizācijas un personāla vadības darbplūsmas ērtības uzlabojumi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) risinājuma Dynamics 365 2020. gada laidiena 2. kopuma plānā

![Darba vienumi, kas saistīti ar mani](./media/hr-workflow-work-items-assigned-to-me.png)

![Ātrā piekļuve arbplūsmas elementiem](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Atvaļinājumu un prombūtnes kalendārs

Šajā laidienā ir ietvertas kalendāra papildu opcijas atvaļinājuma un prombūtnes kalendāriem. Papildinformāciju skatiet šeit [: grupas un uzņēmuma kalendāru](./hr-employee-self-service-calendar.md)skatīšana.

## <a name="coming-soon"></a>Drīzumā

### <a name="checklist-entities-included-in-dataverse"></a>Kontrolsaraksta entītijas iekļautas Dataverse

Kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami Dataverse.

### <a name="benefits-management-reason-codes"></a>Priekšrocību pārvaldības pamatojuma kodi

Priekšrocību pārvaldības pamatojuma kodi drīz tiks apvienoti ar esošajiem pamatojuma kodiem programmā Human Resources. Ja izveidojāt pamatojuma kodus Priekšrocību pārvaldībā, kas ir garāki par 15 rakstzīmēm, ir jāmaina pamatojuma koda nosaukums Priekšrocību pārvaldībā veidlapā **Pamatojuma kodi** uz tādu, kas ir 15 rakstzīmes vai mazāk. Pēc nosaukuma atjaunināšanas pamatojuma kods būs redzams Personāla vadības sadaļā esošajā pamatojuma koda veidlapā. Šīs izmaiņas būs pieejamas nākotnē un tās neietekmēs jau esošo funkcionalitāti.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
