---
title: Jaunumi un izmaiņas programmatūrā Dynamics 365 Human Resources (2020. gada 25. jūnijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 23. jūniju.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9787df5f36c1f08ade40e3e8fc5d5189e3bd5b0
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711944"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Jaunumi un izmaiņas programmatūrā Dynamics 365 Human Resources (2020. gada 23. jūnijs)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3347. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Beidzoties reģistrācijai, darbinieka atvaļinājuma veids, bilance un summa tiek dzēsti Atvaļinājuma reģistrācijas formā (444867)

Tagad, veicot šo atlasi, **Atvaļinājuma veids**, **Bilance** un **Summa** vērtības tiek uzturētas, nevis dzēstas.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Prognozētā bilance nav pareiza, ja ir iespējots jauns līdzeklis (Atvaļinājuma uzkrājums vienam uzņēmumam vai vienam plānam) (456553)

Pareizā prognozētā bilance tagad tiek parādīta, kad ir iespējots viena uzņēmuma vai viena plāna atvaļinājuma uzkrājums.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>EntītIjas ar relācijām, kuru rezultātā tiek dublēti navigācijas rekvizīti (456486)

Šis laidiens novērš problēmu ar vairāku entītiju navigācijas rekvizītiem (relācija). Tiek noteiktas dublikātu relācijas. Šie scenāriji ir izlaboti.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Starpuzņēmuma komentāri par Veiktspējas pārskatu (455536)

Starpuzņēmumu komentāri tagad ir redzami veiktspējas pārskatos ar šo labojumu. Šī izmaiņa labo pārskatītāja komentāru skatu, kas tika ievadīti dažādos uzņēmumos vienam veiktspējas pārskatam.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Nekonsekvence, parādot atlīdzības pārvaldības datus (432562)

Saskaņots atlīdzības datu skats tagad tiek uzturēts Vadītāja pašapkalpošanās pakalpojumā. Atkarībā no tā, kā pārvietojaties uz darbinieka **Atlīdzības informāciju**, atlīdzības dati tagad pastāvīgi tiek parādīti vadītājiem.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Fiksētās atlīdzības plāna spēkā stāšanās datums pēc noklusējuma ir šodienas datums (411994)

Atlīdzības sākuma datums tagad ir balstīts uz darbiniekam piešķirtā amata sākuma datumu.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Atvaļinājuma un kavējuma forma iespējot pusi dienas definīciju tiek atspējota, atverot formu (452607)

Ar šīm izmaiņām **Iespējot pusi dienas definīciju** tiks aktivizēta, līdz jaunam atvaļinājuma darījumam. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Nevar publicēt programmā HcmDiscussionEntity, izmantojot Excel; TotalRatingScore lauka kļūda (453899)

Tagad varat atjaunināt lauku **TotalRatingScore**, izmantojot **HCMDiscussionEntity** Excel darbgrāmatas veidotājā.

## <a name="in-preview"></a>Priekšskatījumā

## <a name="database-logging"></a>Datu bāzes reģistrēšana

Datu bāzes reģistrācija ļauj noteikt, kuras tabulas un laukus ir pārraudzīt. Tas arī ļauj noteikt notikumus, kam jāizraisa izmaiņu izsekošana. Jūs izmantojat datu bāzes reģistrācijas iespējas, lai skatītu šīs izmaiņas laika gaitā. Papildinformāciju skatiet [Datu bāzes reģistrācijas konfigurēšana un pārvaldība](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>Obligātie lauki 

Tagad ir iespējams padarīt laukus obligātus, izmantojot Personāla vadības personalizēšanas iespējas. Šim līdzeklim nepieciešami **Saglabātie skati**.

## <a name="human-resources-application-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai
 
Tiek izlaisti atvieglojumu pārvaldības elementi. DMF elementi ļauj jums importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību. Lai pārvietotu datus, būs pieejama atvieglojumu pārvaldības veidne. Veidne eksportē un importē datus secīgi, lai ievērotu datu atkarības.

## <a name="buy-and-sell-leave"></a>Atvaļinājuma iegāde un pārdošana 

Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu. Šo procesu bieži pārvalda manuāli. Šis līdzeklis automatizē personāla vadības departamenta politikas un pieprasījumu pārvaldību. Tas vienkāršo atvaļinājumu pārvaldības procesu un palīdz likvidēt kļūdas. Plašāku informāciju skatiet:

- [Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atvaļinājuma iegāde un pārdošana](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Atstāt uzkrājumu vienam uzņēmumam vai atsevišķam plānam

Debitori var apstrādāt uzkrājumus vienam uzņēmumam vai atsevišķam atvaļinājumu un prombūtnes plānam. Šī spēja nodrošina skaidrību uzkrāšanas procesā debitoriem ar dažādiem atvaļinājumu gadiem vai atvaļinājuma uzkrāšanas politikām. Lai iegūtu papildu informāciju, skatiet [Uzkrāt atvaļinājumu pēc uzņēmuma vai atvaļinājuma plāna](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Pievienojiet pielikumus brīvā laika pieprasījumiem

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

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurēt Darbinieku pašapkalpošanās nosaukumu

**Personāla vadības parametros** būs pieejama jauna opcija, lai atjauninātu Darbinieku pašapkalpošanās darbvietas nosaukumu uz Pašapkalpošanās.

## <a name="checklist-entities-included-in-common-data-service"></a>Kontrolsaraksta entītijas iekļautas Common Data Service

Kontrolsaraksta entītijas Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejamas Common Data Service.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)