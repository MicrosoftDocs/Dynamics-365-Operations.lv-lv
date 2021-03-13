---
title: Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 20. augusts)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 20. augustu.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b3654617b0e8bc4b586e969913d5dc355b60b882
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130063"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 20. augusts)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3478. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta atsauces numuriem portālā Lifecycle Services (LCS).

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Parādiet nākošo un gaidāmo prombūtnes informāciju kartītēs Cilvēku darbvietā

Gaidāmo un nākošo atvaļinājumu pieprasījumu opcijas tagad ir pieejamas atvaļinājumu un prombūtnes kartītēs **Cilvēku** darbvietā.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Privāts lauks netiek uzstādīts Jā pēc noklusējuma Darbinieka lomai darbinieku pašapkalpošanās sistēmā (477106)

Lauks **Privāts** tagad pēc noklusējuma tiek iestatīts uz **Jā**, kad darbinieki pievieno jaunus adrešu ierakstus darbinieku pašapkalpošanās sistēmā **Personas informācijas** lapā. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Kopsavilkuma cilne Kandidāti, kurus pieņemt darbā Personāla vadībā rāda nepareizu kandidātu skaitu (470110)

**Personāla vadības** lapa tagad precīzi parāda algojamo kandidātu skaitu. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Nevar ievadīt slimību, kas paredzēta darbiniekam, kad uzkrājums ir iestatīts uz nulli (446195)

Tagad atvaļinājuma darbības ir atļautas darbiniekiem, kuru darba attiecības tiek pārtrauktas nākotnē, un uzkrājums tiek iestatīts uz nulli. Atvaļinājuma darbības var ievadīt līdz pat darbinieka izbeigšanas datumam. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Pievienojot pielāgotus laukus jaunajai Darbinieka veidlapai, tiek atspējoti lauki darbības rūtī opcijai Pārvaldīt atvaļinājumu (473314)

Darbības rūts opcijas jaunajā **Darbinieka** veidlapā sadaļā **Pārvaldīt atvaļinājumu** vairs netiks atspējotas, ja jaunajai **Darbinieka** veidlapai būs pievienoti pielāgoti lauki.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Ja komentāru lauks Atvaļinājumam tiek noteikts kā obligāts, tas ļauj iesniegt atvaļinājuma pieprasījumu, ja nav ievadīts neviens komentārs (473543)

Tagad komentāru lauki var būt obligāti, un atvaļinājumu pieprasījumos tiek ievērots šis iestatījums. Obligātie lauki ir priekšskatījuma līdzeklis.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF elements ir pieejams uzkrājumu atlikšanai

DMF elements tagad ir pieejams uzkrājumu atlikšanai.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="mandatory-fields"></a>Obligātie lauki

Ir iespējams padarīt laukus obligātus, izmantojot Personāla vadības personalizēšanas iespējas. Šim līdzeklim nepieciešami **Saglabātie skati**. Papildinformāciju par saglabātajiem skatiem skatiet sadaļā:

- [Saglabātie skati — vispārīga pieejamība](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020. gada izlaiduma 2. laidiena plāns
- [Būvējuma formas, kas pilnībā izmanto saglabātos skatus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Plašāku informāciju skatiet:

- [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 1. laidiena plānā
- [Programma Human Resources programmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a>Drīzumā

### <a name="human-resources-app-in-teams-preview-features"></a>Programma Human Resources programmas Teams priekšskatījuma līdzekļos
 
-  **Paziņojumi**: iesniedzēji un pārtraukuma pieprasījumu apstiprinātāji tiek informēti par Personāla vadības lietotni programmā Teams. Apstiprinātāji varēs apstiprināt vai noraidīt pārtraukumu pieprasījumus, un iesniedzējiem tiks paziņots, ja pieprasījums tika apstiprināts vai noraidīts.
 
- **Pārvaldnieka pārtraukuma kalendārs** : vadītājiem būs iespēja redzēt apstiprināto un gaidāmo laiku to tiešajiem pārskatiem kalendāra skatā. Šis skats nodrošina vieglu izpratni par to, kad viņu grupas dalībnieki ir prom no darba.

### <a name="checklist-entities-included-in-dataverse"></a>Kontrolsaraksta entītijas iekļautas Dataverse

Kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami Dataverse.

## <a name="known-issues"></a>Zināmās problēmas

**Funkciju pārvaldības** darbvietā var tikt parādīti līdzekļi, kas ir atspējoti kā priekšskatījuma līdzekļi, kad tie parasti ir pieejami. Zemāk ir saraksts ar vispārēji pieejamiem līdzekļiem, kas rāda nepareizu statusu. 

- Atvieglojumu pārvaldība
- Pieteikumu pārvaldība
- Datu bāzes reģistrēšana (audits)
- Atvaļinājumu uzkrājums vienam uzņēmumam vai vienam plānam
- Uzkrājumu veidošanas apturēšana atvaļinājumiem un kavējumiem
- Bilances korekcijas iemesla kods un komentārs
- Atvaļinājuma iegāde un pārdošana
- Atvaļinājumu un prombūtnes kalendārs
- Atvaļinājuma pārnešanas kārtulas
- Atvaļinājuma uzkrājumu auditēšana
- Atvaļinājuma uzkrājumu dzēšana
- Atvaļinājuma uzkrājumu noapaļošana
- Konfigurēt vairākus atvaļinājuma veidus vienā atvaļinājumu plānā
- Brīvā laika uzlabojumu atjaunināšana
- Uzkrājumiem izmantot darbinieka FTE
- Starpuzņēmumu kompensācijas skats
- Veiktspējas pārskatu drukāšana
- Atvaļinājuma uzkrājumu korekcija, ņemot vērā brīvdienas

### <a name="benefit-plan-employee-entity"></a>Atvieglojumu plāna darbinieka entītija 

Nesen ir atklātas divas problēmas saistībā ar **BenefitsPlanEmployee** entītiju. Importējot darbinieku reģistrācijas, opcijas **Pārklājuma kods** un **Plāna tipa kods** tiek nepareizi iestatītas. Šī problēma izraisa darbinieku atvieglojumu plānu nekorektu attēlošanu **Darbinieku atvieglojumu plāna** veidlapā un **Atvērt reģistrāciju** veidlapā darbinieku pašapkalpošanās. Šī problēma var ietekmēt arī darbinieka spēju atlasīt plānus Darbinieku pašapkalpošanās. Pašlaik nav risinājuma. Mēs to uzskatām par augstas prioritātes labojumu, un mēs to izlaidīsim ar nākamo laidienu.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)
