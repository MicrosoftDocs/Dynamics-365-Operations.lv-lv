---
title: Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 20. augusts)
description: Šajā rakstā aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Human Resources 2020. gada 20. augustā.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c71a742022afba36c417092d5a9b75c78600357
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902174"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 20. augusts)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3478. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta atsauces numuriem portālā Lifecycle Services (LCS).

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

- [Saglabātie skati — vispārīga pieejamība](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020. gada izlaiduma 2. laidiena plāns
- [Būvējuma formas, kas pilnībā izmanto saglabātos skatus](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Plašāku informāciju skatiet:

- [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 1. laidiena plānā
- [Programma Human Resources programmā Teams](./hr-admin-teams-leave-app.md)

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
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]