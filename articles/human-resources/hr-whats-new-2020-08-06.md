---
title: Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 06. augusts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources.
author: darinkramer
manager: AnnBe
ms.date: 8/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0903be5ead66e09a3e571b523ad4bc20bf92eeb
ms.sourcegitcommit: 6cb0fb3f6fcffa872b855cffa11105f8e3ce074b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698582"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 06. augusts)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3444. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="platform-update-1001236-is-now-available"></a>Platform update 10.0.12(36) tagad ir pieejams

Papildinformāciju skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.12 (2020. gada augusts)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai
 
Tiek izlaisti atvieglojumu pārvaldības elementi. DMF elementi ļauj jums importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību. Lai pārvietotu datus, būs pieejama atvieglojumu pārvaldības veidne. Veidne eksportē un importē datus secīgi, lai ievērotu datu atkarības. Plašāku informāciju skatiet:

- [DMF elementa atbalsts](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) Dynamics 365 2020. gada izlaiduma 1. laidiena plānā
- [Datu pārvaldības pārskats](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Klēra izveido darbplūsmu pirkšanas un pārdošanas atvaļinājumu pieprasījumiem (446557)

Plašāku informāciju skatiet:

- [Atļaut darbiniekiem pirkt un pārdot atvaļinājumu](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) Dynamics 365 2020. gada izlaiduma 2. laidiena plānā
- [Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Atvaļinājuma iegāde un pārdošana](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Darbinieka pasta adreses v2 elementam ir piekļuve starp juridiskām personām ar ierobežotām piekļuves tiesībām (459126)

Ar šīm izmaiņām **Darbinieka pasta adreses V2** elements tiks ierobežots atkarībā no lietotājam piešķirtās juridiskās personas piekļuves.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Darbplūsmas e-pasta hipersaite neatver atbilstošos pārskatus (437398)

Kad izmantojat vietturi, lai pārskata darbplūsmā atvērtu veiktspējas pārskatu, e-pasta ziņojumā ģenerētā hipersaite tagad atver atlasīto ierakstu.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Jaunas vienības atvaļinājuma pirkšanai un pārdošanai (473180)

Datu pārvaldības struktūras elementi tagad ir pieejami atvaļinājumu pirkšanai un pārdošanai. Papildinformāciju skatiet [Datu pārvaldības pārskatā](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Apskatot ieraksta informāciju un izmantojot papildu filtrus, lietotājs var piekļūt citu darbinieku ierakstiem (472490)

Ar šīm izmaiņām darbinieku pašapkalpošanās lietotāji var piekļūt tikai paši saviem ierakstiem, lietojot darbinieku pašapkalpošanās pakalpojumu. Informācijas skatīšana, mainot filtrēšanas opciju, vairs neatklāj papildu datus.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Personāla vadības analīze iekļauj izejošos darbinieku ierakstus (382893)

Ar šo laidienu personāla vadības analīze tagad iekļauj tikai aktīvos darbiniekus. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Nevar apstrādāt nopelnu palielināšanu darbiniekam (473125)

Šīs izmaiņas ļauj ievadīt nopelnu palielinājumu, mainot spēkā stāšanās datumu jaunajam nopelnu palielinājumam.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Pārskata darbplūsmu var sākt vairāk nekā vienu reizi (467541)

Veicot šīs izmaiņas, varat sākt veiktspējas pārskata darbplūsmu tikai vienu reizi. Vadītāja statuss vairs nerāda opciju, lai sāktu pārskatu.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Atvaļinājuma pieprasījuma darba plūsma beidzas ar kļūdu, atceļot apstiprinātu atvaļinājuma pieprasījumu (472063)

Šajā laidienā, kad atceļat apstiprinātu atvaļinājuma pieprasījumu, pieprasījuma stāvoklis vairs nepaliek apstiprināts, un darbplūsma turpināsies.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Sistēma piedāvā izejošos darbiniekus, izveidojot jaunu pārskatu no veidnes (460624)

Ar šīm izmaiņām aizejošie darbinieki ir ilgāk pieejami, veidojot jaunus pārskatus no veidnes. Nevar izveidot pārskatus par darbiniekiem, kas ir ārpus nodarbinātības datumiem.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Pozīciju hierarhijas riņķveida atsauču noteikšana (415879)

Ar šo izmaiņu pozīcijas hierarhijas riņķveida atsauces noteikšana ir tikai viens laika punkts. Varat palaist riņķveida atsauču noteikšanu dažādiem datumiem, lai verificētu, ka pārskata struktūrai nav nevienas riņķveida atsauces.

## <a name="buy-and-sell-leave"></a>Atvaļinājuma iegāde un pārdošana 

Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu. Šo procesu bieži pārvalda manuāli. Šis līdzeklis automatizē personāla vadības departamenta politikas un pieprasījumu pārvaldību. Tas vienkāršo atvaļinājumu pārvaldības procesu un palīdz likvidēt kļūdas. Plašāku informāciju skatiet:

- [Atļaut darbiniekiem pirkt un pārdot atvaļinājumu](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) Dynamics 365 2020. gada izlaiduma 2. laidiena plānā
- [Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Atvaļinājuma iegāde un pārdošana](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Atstāt uzkrājumu vienam uzņēmumam vai atsevišķam plānam

Debitori var apstrādāt uzkrājumus vienam uzņēmumam vai atsevišķam atvaļinājumu un prombūtnes plānam. Šī iespēja nodrošina skaidrību uzkrāšanas procesā debitoriem ar dažādiem atvaļinājumu gadiem vai atvaļinājumu uzkrāšanas politikām. Lai iegūtu papildu informāciju, skatiet [Uzkrāt atvaļinājumu pēc uzņēmuma vai atvaļinājuma plāna](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

## <a name="add-attachments-to-time-off-requests"></a>Pielikumu pievienošana brīvā laika pieprasījumiem

Iespēja pievienot pielikumus apstiprinātajiem atvaļinājumu pieprasījumiem ir kritiski nepieciešama pašreizējā COVID-19 vidē. Tagad darbinieki var pievienot šos pielikumus. Tām ir arī vairāk izpratnes par to, kā tiek atjaunināti atvaļinājumu pieprasījumi. Lai iegūtu papildu informāciju, skatiet [Pielikumu pievienošana esošam pieprasījumam](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Pievienot uzkrājumu atlikšanas iemesla kodu 

Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.

## <a name="carry-forward-rules"></a>Pārnešanas kārtulas 

Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas. Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem

Jūs varat izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam. Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt. Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="mandatory-fields"></a>Obligātie lauki

Ir iespējams padarīt laukus obligātus, izmantojot Personāla vadības personalizēšanas iespējas. Šim līdzeklim nepieciešami **Saglabātie skati**. Papildinformāciju par saglabātajiem skatiem skatiet sadaļā:

- [Saglabātie skati — vispārīga pieejamība](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020. gada izlaiduma 2. laidiena plāns
- [Būvējuma formas, kas pilnībā izmanto saglabātos skatus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Plašāku informāciju skatiet:

- [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 1. laidiena plānā
- [Programma Human Resources programmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF elements ir pieejams uzkrājumu atlikšanai

DMF elements tagad ir pieejams uzkrājumu atlikšanai.

## <a name="coming-soon"></a>Drīzumā

## <a name="checklist-entities-included-in-common-data-service"></a>Kontrolsaraksta entītijas iekļautas Common Data Service

Kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami Common Data Service.

## <a name="known-issues"></a>Zināmās problēmas

**Funkciju pārvaldības** darbvietā var tikt parādīti līdzekļi, kas ir atspējoti kā priekšskatījuma līdzekļi, kad tie parasti ir pieejami. Zemāk ir saraksts ar vispārēji pieejamiem līdzekļiem, kas rāda nepareizu statusu. 

1.  Atvieglojumu pārvaldība
2.  Pieteikumu pārvaldība
3.  Datu bāzes reģistrēšana (audits)
4.  Atvaļinājumu uzkrājums vienam uzņēmumam vai vienam plānam
5.  Uzkrājumu veidošanas apturēšana atvaļinājumiem un kavējumiem
6.  Bilances korekcijas iemesla kods un komentārs
7.  Atvaļinājuma iegāde un pārdošana
8.  Atvaļinājumu un prombūtnes kalendārs
9.  Atvaļinājuma pārnešanas kārtulas
10. Atvaļinājuma uzkrājumu auditēšana
11. Atvaļinājuma uzkrājumu dzēšana
12. Atvaļinājuma uzkrājumu noapaļošana
13. Konfigurēt vairākus atvaļinājuma veidus vienā atvaļinājumu plānā
14. Brīvā laika uzlabojumu atjaunināšana
15. Uzkrājumiem izmantot darbinieka FTE
16. Starpuzņēmumu kompensācijas skats
17. Veiktspējas pārskatu drukāšana
18. Atvaļinājuma uzkrājumu korekcija, ņemot vērā brīvdienas

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)
