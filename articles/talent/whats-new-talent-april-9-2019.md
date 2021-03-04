---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Talent (2019. gada 9. aprīlis)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a4d4de6cf28e24d1265395d6440df85edf71a0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461931"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Jaunumi vai izmaiņas risinājumā Dynamics 365 Talent (2019. gada 9. aprīlis)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) integrācija ar līdzekli Ziņot par problēmu
Programmā Attract un Onboard problēmas, kuras lietotāji ir reģistrējuši, izmantojot līdzekli Ziņot par problēmu, tagad automātiski izveido atbalsta problēmas klienta LCS projektā. Administratori varat izskatīt šīs problēmas un iesniegt tās korporācijai Microsoft, ja nepieciešams. Tas atbilst veidam, kā Core HR apstrādā lietotāju atbalsta problēmas.

### <a name="relevance-search"></a>Atbilstības meklēšana
No kandidātu kopām tagad visā savā kandidātu datu bāzē varat meklēt noteiktas prasmes, nosaukumus vai iegūto izglītību. Jums vairs nav jānorāda, kurā kandidātu profilu sadaļā vēlaties meklēt. Attract meklē visā profilā un izceļ visas atrastās atbilstības. Attract meklē arī visos dokumentos, kas ir pieejami par kādu kandidātu, un viedi sakārto meklēšanas rezultātus. Turklāt rezultātus varat filtrēt pēc avota vai pēc tā, vai tie ir saņēmuši sudraba medaļu. Plašāku informāciju skatiet rakstā [Kandidātu profilu meklēšana un skatīšana](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Potenciālo kandidātu ieteikumi
Attract var palīdzēt, uzsākot avotu meklēšanu kādam darbam, līdzko jūs to aktivizējat, sniedzot viedus kandidātu ieteikumus no jūsu organizācijas kandidātu datu bāzes. Šajos ieteikumos ir ietverta informācija par prasmēm un izglītību, kuru norādījāt, meklējot saistītus potenciālos kandidātus. Šie ieteikumi ir redzami attiecīgā darba sadaļas cilnē **Potenciālie kandidāti**, ja šim darbam to iespējojāt darbā pieņemšanas procesa laikā. Plašāku informāciju skatiet tēmā [Potenciālo kandidātu ieteikumi](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Intervētāja pieejamības statusi
Interviju plānotāji drīz varēs redzēt intervētāju statusus **Ārpus biroja, strādā citur**, lai palīdzētu ieplānot intervētājiem vispiemērotākos laikus.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Kandidātu interviju pieredze: kalendāra aicinājumu saglabāšana
Tagad kandidāti var lejupielādēt un saglabāt interviju notikumus savos personiskajos kalendāros, izmantojot kandidātam atsūtītajam intervijas kopsavilkuma e-pasta ziņojumam pievienoto .ics failu.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) integrācija ar ziņošanu par problēmu
Programmā Attract un Onboard problēmas, kuras lietotāji ir reģistrējuši, izmantojot līdzekli Ziņot par problēmu, tagad automātiski izveido atbalsta problēmas klienta LCS projektā. Administratori varat izskatīt šīs problēmas un iesniegt tās korporācijai Microsoft, ja nepieciešams. Tas atbilst veidam, kā Core HR apstrādā lietotāju atbalsta problēmas.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR
Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Procenti no pamata mainīgajiem plāniem ielādē nepareizu summu
Šīs nedēļas izlaidums labo problēmu, kad tiek ielādētas mainīgo atlīdzību piemaksas, izmantojot procentus no pamata plāniem.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Datuma atlasītājs pēdējai darbadienai nedarbojas pareizi
Ar šo izmaiņu tiek izlabota problēma:, kad lietotāji rediģē vērtību **Nodarbinātības beigu datums** un atlasa datumu, lietojot kalendāra vadīklu, atlasei tiek pievienota kāda diena.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Personāla darbības tipu ierobežošana ar veikto darbību
Šī izmaiņa ierobežo darbību tipus, kas tiek rādīti, veicot noteiktas darbības. Piemēram, kad tiek pieprasīts jaunu amats, atlasāmo darbību sarakstā ir redzamas tikai jaunā amata darbības. Iepriekš tika rādītas gan jaunās, gan rediģētās darbības. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Darbinieka ar atlīdzību pārsūtīšana uz otru juridisko personu
Šajā laidienā ir iespējams atlīdzību pabeigt otrā juridiskajā personā, ja pārsūtīšana tiek veikta starpuzņēmumu pārsūtīšanai.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Pārsūtīšanas laikā nevar atlasīt atlīdzību turpmākai nodarbinātībai
Kad pārsūtāt darbinieku uz jaunu juridisko personu, tagad pārsūtīšanas procesa laikā varat iestatīt atlīdzību jaunajai juridiskajai personai.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Amata piešķires laikā lietotājs nevar piešķirt atlīdzību
Pievienojot jaunu amata piešķiri, tagad ir iespējams iestatīt fiksētās atlīdzības ierakstus. 

## <a name="in-preview"></a>Priekšskatījumā

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Atļaušana norādīt iemeslu kodus atvaļinājumu tipiem
Organizācijām, iespējams, ir nepieciešama papildinformācija par brīvā laika pieprasījumiem. Tagad atvaļinājumu tipiem varat norādīt iemeslu kodus un ļaut darbiniekiem savos brīvā laika pieprasījumos atlasīt iemesla kodu.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Iemeslu kodu pieprasīšana noteiktiem atvaļinājumu tipiem brīvā laika pieprasījumos
Organizācijām var būt nepieciešami iemeslu kodi noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Tas varētu būt saistīts ar uzņēmuma politiku vai normatīvajām prasībām. Tagad varat norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods, un varat pieprasīt, lai darbinieki savos brīvā laika pieprasījumos atvaļinājuma tipam norādītu iemesla kodu.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Atvaļinājumu un kavējumu transakciju sarakstu nodrošināšana personāla vadībai
Darbinieku brīvā laika izsekošana un saprašana, kā tiek aprēķināts brīvais laiks, ne tikai palīdz personāla vadībai atbildēt uz darbinieku jautājumiem, bet arī nodrošina darbiniekiem precīzas brīvā laika piemaksas. Personāla vadībai tagad ir jauns skats uz transakcijām (dotācijām, uzkrājumiem, korekcijām un pieprasījumiem), lai redzētu bilanču aprēķinu ietekmējošos faktorus. 

## <a name="coming-soon"></a>Drīzumā

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Lietotāja interfeisa uzlabojumi dublētu darbinieku pārbaudei
Līdz ar šīs izmaiņas ieviešanu dublikāti tiek noteikti, kad aizpildāt vārda/uzvārda/nosaukuma laukus, un statuss parāda atrasto dublikātu skaitu. Varat atlasīt norādīto saiti, lai atvērtu jaunu lapu, kur novērtēt, vai atrastā atbilstība ir jāizmanto. Lai izvairītos no datu ievades pārtraukšanas, dublikātu forma netiek atvērta automātiski.

###  <a name="email-support-for-alerts"></a>E-pasta atbalsts brīdinājumiem
Līdz ar platformas atjauninājumu 25 Finance and Operations ieviešanu lietotāji var izveidot brīdinājumu kārtulas, kas automātiski sūta e-pasta paziņojumus kontaktpersonām, ja kāds notikums tās aktivizē. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]