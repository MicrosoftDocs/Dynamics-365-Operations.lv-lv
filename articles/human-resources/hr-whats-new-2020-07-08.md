---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 08. jūlijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 8. jūliju.
author: andreabichsel
ms.date: 07/08/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b277333ea37c2b6157ae9befc9d94f0e35ff97be
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891893"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 8. jūlijs)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3382. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="database-logging"></a>Datu bāzes reģistrēšana

Datu bāzes reģistrācija ļauj noteikt, kuras tabulas un laukus ir pārraudzīt. Tas arī ļauj noteikt notikumus, kam jāizraisa izmaiņu izsekošana. Jūs izmantojat datu bāzes reģistrācijas iespējas, lai skatītu šīs izmaiņas laika gaitā. Papildinformāciju skatiet [Datu bāzes reģistrācijas konfigurēšana un pārvaldība](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurēt Darbinieku patstāvīgi izmantojamais pakalpojums nosaukumu

Tagad **Personāla vadības parametri** var mainīt darbvietas nosaukumu **Darbinieku patstāvīgi izmantojamais pakalpojums** uz **Patstāvīgi izmantojamais pakalpojums**. Papildinformāciju skatiet sadaļā [Darbinieku patstāvīgi izmantojamā pakalpojuma darbvietas nosaukuma maiņa](hr-employee-self-service-workspace-name.md).

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Atvieglojumu pārvaldība atklātās reģistrācijas pieejai ārpus perioda

Šis laidiens izlabo kļūdu, kur darbinieki var piekļūt atklātās reģistrācijas atvieglojumiem ārpus reģistrācijas perioda vai bez dzīves notikuma. Tā rezultātā, ja ir nepieciešama atklātās reģistrācijas demonstrācija Darbinieku patstāvīgi izmantojamajā pakalpojumā, jums ir jāpielāgo atklātās reģistrācijas datumi šodienai (vai agrāk), lai to padarītu pieejamu. Varat mainīt šo iestatījumu, izmantojot **Atvieglojumu pārvaldība > Kārtulas un opciju periodi**.

## <a name="email-employee-enrollment-confirmation"></a>Darbinieka e-pasta reģistrācijas apstiprinājums

Tagad varat nosūtīt e-pasta ziņojumus darbiniekiem pēc tam, kad tie pabeidz savu atvieglojumu atlasi. Varat nosūtīt noklusējuma ziņojumu vai izmantot organizācija e-pasta veidni. Šie iestatījumi atrodas **Personāla vadības parametri > Atvieglojumu pārvaldība**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Atceltais atvaļinājums joprojām tiek rādīts darbvietas Personas gaidāmajā brīvajā laika (441358)

Atceltais atvaļinājums vairs netiks rādīts kā gaidāmais brīvais laiks atvaļinājumu kartītēs darbvietā **Personas**.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Nevar izmantot nodaļas elementa rekvizītu elementā PositionV2 (456486)

Tagad varat pievienot nodaļu, neveidojot dublikāta relāciju.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity jāizmanto tikai aprēķinātā lauka pensiju plāniem (459779)

Eksportējot **PayrollWorkerEnrolledBenefitDetailEntity** elementu, eksportēšana nosaka, vai tam jāizmanto aprēķinātais lauks, pamatojoties uz likmes tabulu, vai jāizmanto lauks **ContributionAmountCur**, kas atrodas dublēšanas tabulā. Datu elementa izmantotā loģika izmantos likmes tabulu situācijās, kurās parasti nav pieteikuma. Šī loģika izraisa elementa eksportēšanu, lai atgrieztu nulles vērtību šai kolonnai, jo nav aprēķina likmes tabulas un prece neļauj klientam to norādīt.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Neskaidri tulkojumi čehu valodā Personāla pārvaldībā un Darbinieku patstāvīgi izmantojamajā pakalpojumā (400276)

Šajā laidienā ir izlaboti tulkojumi **Uzņēmuma direktorijs**, **Nākamais reģistrētais kurss**, **Darbs** un **Amats**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>Tabulā WorkCalendarEmployment nav iespējoti izveidotie un modificētie sistēmas lauki (460171)

Izveidotie un modificētie sistēmas lauki tagad ir iespējoti Human Resources tabulā **WorkCalendarEmployment**.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Nulles atsauces izņēmums Jauna darbinieka pieņemšanai darbā un informācijas pievienošanai (455475)

Šis laidiens izlabo kļūdu (nulles atsauce) racionalizētā darbinieka ierakstā, kad, pieņemot darbā darbinieku, izmantojat opciju **Pieņemt darbā un pievienot informāciju**.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Dataverse darbinieka elementā veiktās izmaiņas netiek atspoguļotas Human Resources (455652)

Izmaiņas, kas veiktas šādos laukos Dataverse elementā **Darbinieks**, tagad tiks parādītas Human Resources:

- **Strādā no mājām**
- **Darba stāža datums**
- **Gadadienas datums**
- **Sākotnējais darbā pieņemšanas datums**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Pamatojoties uz amatam piešķirto darbu, pareizais atlīdzības līmenis netiek noklusēts (394136)

Ar šīm izmaiņām pareizais atlīdzības līmenis tiek noklusēts pamatojoties uz **Spēkā stāšanās datuma** ierakstiem **Amata informācija** un **Sākuma datums**, **Atlīdzības plāna piešķirē**.

## <a name="in-preview"></a>Priekšskatījumā

## <a name="mandatory-fields"></a>Obligātie lauki 

Tagad ir iespējams padarīt laukus obligātus, izmantojot Personāla vadības personalizēšanas iespējas. Šim līdzeklim nepieciešami **Saglabātie skati**.

## <a name="human-resources-application-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai
 
Tiek izlaisti atvieglojumu pārvaldības elementi. DMF elementi ļauj jums importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību. Lai pārvietotu datus, būs pieejama atvieglojumu pārvaldības veidne. Veidne eksportē un importē datus secīgi, lai ievērotu datu atkarības.

## <a name="buy-and-sell-leave"></a>Atvaļinājuma iegāde un pārdošana 

Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu. Šo procesu bieži pārvalda manuāli. Šis līdzeklis automatizē personāla vadības departamenta politikas un pieprasījumu pārvaldību. Tas vienkāršo atvaļinājumu pārvaldības procesu un palīdz likvidēt kļūdas. Plašāku informāciju skatiet:

- [Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atvaļinājuma iegāde un pārdošana](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Atstāt uzkrājumu vienam uzņēmumam vai atsevišķam plānam

Debitori var apstrādāt uzkrājumus vienam uzņēmumam vai atsevišķam atvaļinājumu un prombūtnes plānam. Šī iespēja nodrošina skaidrību uzkrāšanas procesā debitoriem ar dažādiem atvaļinājumu gadiem vai atvaļinājuma uzkrāšanas politikām. Lai iegūtu papildu informāciju, skatiet [Uzkrāt atvaļinājumu pēc uzņēmuma vai atvaļinājuma plāna](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Pielikumu pievienošana brīvā laika pieprasījumiem

Iespēja pievienot pielikumus apstiprinātajiem atvaļinājumu pieprasījumiem ir kritiski nepieciešama pašreizējā COVID-19 vidē. Tagad darbinieki var pievienot šos pielikumus. Tām ir arī vairāk izpratnes par to, kā tiek atjaunināti atvaļinājumu pieprasījumi. Lai iegūtu papildu informāciju, skatiet [Pielikumu pievienošana esošam pieprasījumam](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Pievienot uzkrājumu atlikšanas iemesla kodu 

Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.

## <a name="carry-forward-rules"></a>Pārnešanas kārtulas 

Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas. Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem

Jūs varat izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam. Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt. Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF elements ir pieejams uzkrājumu atlikšanai 

DMF elements tagad ir pieejams uzkrājumu atlikšanai.

## <a name="coming-soon"></a>Drīzumā

## <a name="checklist-entities-included-in-dataverse"></a>Kontrolsaraksta entītijas iekļautas Dataverse

Kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami Dataverse.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]