---
title: Piemērotības kārtulu un opciju konfigurēšana
description: Šajā rakstā ir aprakstīts, kā iestatīt piemērotības nosacījumus un opcijas Microsoft atvieglojumu pārvaldībā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 916a9955327aef67ac768d4505bdb343862058a1
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644089"
---
# <a name="configure-eligibility-rules-and-options"></a>Piemērotības kārtulu un opciju konfigurēšana 

Pēc nepieciešamo parametrus konfigurēšanas atvieglojumu pārvaldībā varat izveidot piemērotības noteikumus, komplektus, periodus un programmas, ko saistīsiet ar saviem atvieglojumu plāniem.

Piemērotības nosacījumus izmanto, lai noteiktu, vai darbinieki ir piemēroti plānam. Darbiniekiem ir jāatbilst vismaz vienas kārtulas nosacījumam, lai to uzskatītu par atbilstošu atvieglojumam. Piemēram, plānā ir divas kārtulas. Pirmā kārtula (1. rinda) norāda, ka darbinieka tipam jābūt **Darbinieks**. Otrā kārtula (2. rinda) norāda, ka darbinieka jābūt darbiniekam jābūt nodarbinātam uz pilnu slodzi. Tāpēc darbinieki, kuri atbilst 1. kārtulai, ir piemēroti pat tad, ja tie ir nodarbināti tikai nepilna laika.

Tomēr varat iestatīt vienu noteikumu, kuram ir vairāki nosacījumi. Šajā gadījumā darbiniekiem jāatbilst visiem kārtulas nosacījumiem, lai viņus uzskatītu par tiesīgiem uz atvieglojumu. Piemēram, ir noteikums ar nosaukumu **Darbinieks pilna laika**. Šis noteikums norāda, ka darbinieka tipam jābūt **Darbinieks** *un* darbiniekam jābūt nodarbinātam uz pilnu slodzi. Tādējādi, lai darbinieki varētu būt piemēroti, darbiniekiem ir jāatbilst abiem noteikuma nosacījumiem.

> [!IMPORTANT]
> Vismaz vienam piemērotības nosacījumam jābūt saistītam ar katru atvieglojumu plānu. Varat saistīt vairākus noteikumus ar atvieglojumu.

## <a name="create-an-eligibility-rule"></a>Piemērotības kārtulas izveide

Piemērotības kārtula nosaka, kuri darbinieki var reģistrēties katrā atvieglojumu plānā. Pēc piemērotības kārtulu definēšanas, piešķiriet tās atvieglojumu plāniem. Pēc tam varat apstrādāt reģistrācijas piemērotību, lai skatītu, kuri darbinieki ir piemēroti katram plānam. 

Atvērtās reģistrācijas laikā darbinieki var atlasīt atvieglojumu plānus. Ja viņi kļūst nepiemēroti atvieglojumu plānam, pamatojoties uz piemērotības kārtulām, pēc tam, kad jau ir reģistrēti, viņi netiek automātiski atsaistīti. Parasti, kad iestājas dzīves notikums, kas ietekmē piemērotību plānam, darbiniekam tiek uzsākts reģistrācijas periods, lai atlasītu plānus, kam viņš ir piemērots. 

1. Darbvietā **Atvieglojumu pārvaldība** sadaļā **Iestatīt** atlasiet **Piemērotības kārtulas un opcijas**.

2. Cilnē **Piemērotības kārtulas** atlasiet **Jauns**, lai izveidotu piemērotības kārtulu. Lai skatītu plānus, kas ir saistīti ar piemērotības kārtulu, atlasiet **Pievienotie plāni**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Piemērojamības kārtula** | Piemērotības kārtulas unikālais identifikators. |
   | **Apraksts** | Piemērojamības kārtulas apraksts. |
   | **Derīguma sākuma datums un laiks** | Piemērotības kārtulas sākuma datums. | 
   | **Derīguma beigu datums un laiks** | Piemērotības kārtulas beigu datums. |
   | **Lietotāja darbinieka veids** | Norāda, vai atvieglojumu piemērotības kārtulā izmantot darbinieka veidu. |
   | **Nodarbinātā veids** | Nodarbinātā veids, ja **Izmantot darbinieka veidu** ir pārslēgts uz **Jā**. |
   | **Izmantot darbinieka statusu** | Norāda, vai atvieglojumu piemērotības kārtulā izmantot darbinieka nodarbinātības statusu. |
   | **Statuss** | Darbinieka statuss, ja **Izmantot darbinieka statusu** ir pārslēgts uz **Jā**. Ja **Izmantot darbinieka statusu** ir pārslēgts uz **Nē**, lauks netiek izmantots. |
   | **Izmantot nodarbinātības kategoriju** | Norāda, vai izmantot darbinieka vērtību **Nodarbinātības kategorija** kā daļu no atvieglojumu piemērotības kārtulas. | 
   | **Nodarbinātības kategorija** | Darbinieka nodarbinātības kategorija, ja **Izmantot nodarbinātības kategoriju** ir pārslēgts uz **Jā**. |
   | **Izmantot jauno pieņemšanas darbā kārtulu** | Norāda, vai izmantot jauna darba pieņemtā jauno darbā pieņemšanas perioda vērtību kā daļu no atvieglojumu piemērotības kārtulas. |
   | **Reģistrācijas periods** | Laika periods, kurā atļauta jauna darba pieņemtā reģistrācija. Ja to iestatīsiet arī parametros, parametru iestatījumam būs prioritāte pār šo. |
   | **Izmantot iepriekšējo nodarbinātības statusu** | Norāda, vai izmantot darbinieka iepriekšējo nodarbinātības statusu kā daļu no atvieglojumu piemērojamības kārtulas. Piemēram, varat norādīt piemērojamības kārtulu, kas atsakās no seguma gaidīšanas perioda visiem darbiniekiem, kas ir pārnesti no statusa **Atlaists** uz statusu **Nodarbināts** 90 dienu laikā no viņa iepriekšējās nodarbinātības. |

4. Sadaļā **Papildu kritēriji** atlasiet tālāk minētās opcijas un pievienojiet informāciju pēc nepieciešamības.

   | Opcija | Apraksts |
   | --- | --- |
   | **Piemērotais vecums** | Norāda vecuma diapazonu vai diapazonus, kas nepieciešami, lai izpildītu piemērotības kārtulu. |
   | **Piemērotā nodaļa** | Norāda nodaļu vai nodaļas, kurās darbiniekam jābūt, lai izpildītu piemērotības kārtulu. |
   | **Piemērots nodarbinātības veids** | Norāda nodarbinātības veidu vai veidus, kurās darbinieks jāiedala, lai izpildītu piemērotības kārtulu. Piemēram, pilna laika vai nepilna laika. |
   | **Piemērotais darbs** | Norāda darbu vai darbus, lai izpildītu piemērotības kārtulu. Darbi ir saistīti ar amatiem, un amatus ieņem darbinieki. |
   | **Piemērotā darba funkcija** | Norāda darba funkciju vai funkcijas, lai izpildītu piemērotības kārtulu. Piemēram, nodarbinātie pārdošanā vai tehniķi. |
   | **Piemērotā darba veids** | Norāda darba veidu vai veidus, lai izpildītu piemērotības kārtulu. Piemēram, kancelejas darbinieki vai vadītāji. |
   | **Piemērota juridiska persona** | Norāda juridisko personu vai juridiskās personas, kas kvalificējas piemērotības kārtulai. Piemēram, Contoso Entertainment System USA. |
   | **Piemērojamais atlīdzības reģions** | Norāda darbinieka atrašanās vietu, lai izpildītu piemērotības kārtulu. Piemēram, centrālā ASV. |
   | **Piemērotais amats** | Norāda amatu vai amatus, lai izpildītu piemērotības kārtulu. Piemēram, personāla vadības asistents vai personāla vadības vadītājs. |
   | **Piemērots amata veids** | Norāda amata veidu vai veidus, lai izpildītu piemērotības kārtulu. Piemēram, pilna laika. |
   | **Piemērotais stāvoklis** | Norāda administratīvās teritorijas, lai izpildītu piemērotības kārtulu. Piemēram, Ziemeļdakota, ASV vai Britu Kolumbija, Kanāda. |
   | **Piemēroti nodarbinātības noteikumi** | Norāda nodarbinātības noteikumus, lai izpildītu piemērotības kārtulu. Piemēram, brīvs līgums vai koplīgums. |
   | **Piemērotā arodbiedrība** | Norāda dalību arodbiedrībā, lai izpildītu piemērotības kārtulu. Piemēram, Amerikas autoiekrāvēju vadītāji.</br></br>Izmantojot uz arodbiedrību balstītu piemērotības kārtulu, nodarbinātā arodbiedrības ierakstam jāaizpilda beigu datums. To nevar atstāt tukšu. |
   | **Piemērojamais pasta indekss** | Norāda pasta indeksus, lai izpildītu piemērotības kārtulu. Piemēram, 58104. |

5. Sadaļā **Papildinformācija** varat apskatīt tālāk minēto papildinformāciju.

   | Lauks | Apraksts |
   | --- | --- |
   | **Piemērotā lietotāja lauks** | Norāda papildu atbilstības kārtulas, pamatojoties uz debitoru definētiem laukiem. |
   | **Piemērojamības veids** | Norāda kritēriju kategoriju, ko atlasījāt **Papildu kritēriji**. |
   | **PIemērojamības atsauce** | Norāda vērtības, ko atlasījāt **Papildu kritēriji**. |
   | **Apraksts** | Apraksts, ko atlasījāt **Papildu kritēriji**. |

6. Atlasiet **Saglabāt**.

## <a name="using-custom-fields-in-eligibility-rules"></a>Pielāgoto lauku izmantošana piemērotības kārtulās

[Pielāgotos laukus](hr-developer-custom-fields.md) var izveidot Personāla vadībā, lai izsekotu papildinformāciju. Šos laukus var pievienot tieši lietotāja interfeisam, un kolonna tiek dinamiski pievienota pakārtotai tabulai.  

Pielāgotos laukus var izmantot piemērotības procesā. Piemērotības nosacījumi var izmantot vienu vai vairākas pielāgoto lauku vērtības, lai noteiktu darbinieka atbilstību.  Lai esošajai kārtulai pievienotu pielāgotu lauku vai izveidotu jaunu kārtulu, pārejiet uz **Atvieglojumu pārvaldība > Saites > Iestatījumi > Piemērotības kārtulas > Pielāgotā lauka piemērotība**. Šajā lapā varat izveidot kārtulu, kas izmanto vienu vai vairākus pielāgotos laukus, un varat definēt vairākas vērtības katram pielāgotajam laukam, lai noteiktu piemērotību.

Tālāk norādītās tabulas atbalsta pielāgotos laukus, kurus var izmantot piemērotības apstrādē:

- Darbinieks (HcmWorker)  
- Darbs (HcmJob)  
- Pozīcija (HcmPosition)  
- Pozīcijas detalizēta informācija (HcmPositionDetail)  
- Amatā nodarbinātā piešķire  
- Nodarbinātība (HcmEmployment)  
- EmploymentDetails (HcmEmploymentDetails)  
- Detalizēta informācija par darbu (HcmJobDetails)  

Tālāk norādītie pielāgoto lauku tipi tiek atbalstīti piemērotības apstrādē:

- Teksts  
- Salasīšanas saraksts  
- Skaits  
- Decimāldaļskaitlis  
- Izvēles rūtiņa  

Tabulā ir parādīta pielāgota lauka piemērotības formas lauka informācija.

| Lauks  | Apraksts |
|--------|-------------|
| Nosaukums/vārds, uzvārds | Izveidotā kritērija nosaukums. |
| Tabulas nosaukums | Tabulas nosaukums, kas satur pielāgoto lauku, kas tiek izmantots piemērotības nosacījumam. |
| Lauka nosaukums | Lauks, kas tiks izmantots piemērotības kārtulai. |
| Operatora tips | Parāda operatoru, kas tiek izmantots pielāgotā lauka piemērotības konfigurācijā. |
| Vērtība | Parāda vērtību, kas tiek izmantota pielāgotā lauka piemērotības konfigurācijā. |

## <a name="eligibility-logic"></a>Piemērotības loģika

Šajās sadaļās aprakstīts, kā tiek apstrādāta atvieglojumu atbilstība.

### <a name="rules-assigned-to-a-plan"></a>Plānam piešķirtās kārtulas 
Kad atvieglojumu plānam ir piešķirti vairāki piemērotības nosacījumi, darbiniekam jāatbilst vismaz vienai kārtulai, lai būtu piemērots reģistrācijai atvieglojumu plānā.  Tālākajā piemērā darbiniekam ir jāatbilst vai nu kārtulas **Darba tips**, vai arī kārtulas **Aktīvie darbinieki** prasībām.

![Darbiniekam ir jāatbilst vai nu kārtulas Darba tips, vai arī kārtulas Aktīvie darbinieki prasībām.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Kritēriji piemērotības kārtulai 
Kārtulā definējiet kritērijus, kas veido kārtulu. Iepriekšminētajā piemērā **Darba tipa** kārtulas kritērijs ir tas, kur Darba tips = Vadītāji. Tādēļ darbiniekam jābūt vadītājam, lai viņš būtu piemērots darbinieks. Šī ir kārtula, kurā ir tikai viens kritērijs.

Varat definēt kārtulas, kurās ir vairāki kritēriji. Kad definējat vairākus kritērijus piemērotības kārtulā, darbiniekam ir jāatbilst visiem kārtulas kritērijiem, lai būtu piemērots atvieglojumu plānam. 

Piemēram, **Aktīvo darbinieku** kārtula tiek veidota no šādiem kritērijiem. Lai darbinieks būtu piemērots, pamatojoties uz **Aktīvo darbinieku** kārtulu, darbiniekam jābūt nodarbinātam juridiskajā amatā USMF *un* jābūt pilnas laika amata tipam.  

![Kritēriji piemērotības kārtulai.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Vairāki nosacījumi kritērijos

Kārtulas var papildus izvērst, lai vienā kritērijā izmantotu vairākus nosacījumus. Darbiniekam ir jāatbilst vismaz vienam nosacījumam, lai varētu tikt piemērots. Lai izveidotu iepriekšminētajā piemērā, **Aktīvo darbinieku** kārtulu var papildus paplašināt, lai iekļautu darbiniekus, kas arī ir nepilna laika darbinieki. Tā rezultātā darbiniekam jābūt darbiniekam USMF *un* vai nu pilnas laika, vai nepilnas laika darbiniekam.  

![Vairāki nosacījumi kritērijos.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Piemērotības nosacījumi pielāgotā lauka kritērijā 
Līdzīgi iepriekš pielāgotos laukus var izmantot, veidojot piemērotības nosacījumus un strādāt vienādā veidā. Piemēram, varat piedāvāt interneta kompensāciju Fargo vai Kopenhāgenas darbiniekiem, kas strādā no mājām, jo šajās vietās interneta izmaksas ir augstākas. Lai to izdarītu, izveidojiet divus pielāgotos laukus: **Biroja atrašanās vieta** (izdošanas veidlapa) un **Darbs no mājām** (izvēles rūtiņa). Pēc tam izveidojiet kārtulu ar nosaukumu **WFH darbinieki**. Kārtulas kritērijs ir vieta, kur **Biroja atrašanās vieta = Fargo** vai **Kopenhāgena** *un*, kur **Darbs no mājām = Jā**.

Pielāgotās piemērotības kārtulas būtu jāiestata, kā norādīts šajā attēlā. 

![Piemērotības nosacījumi pielāgotā lauka kritērijā.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Pakešu konfigurācija

Komplekti ir saistītu atvieglojumu plānu kopa. Varat izmantot atvieglojumu komplektus, lai grupētu atvieglojumu plānus, kas darbiniekam jāizvēlas, lai reģistrētos noteiktos atvieglojumu plānos, kas var būt atkarīgi no reģistrācijas citos atvieglojumu plānos. Tālāk minēti piemēri, kad, iespējams, vēlēsieties izmantot komplektu.

- Veselības plānu komplekts, kas ietver veselības apdrošināšanu ar lieliem atskaitījumiem kopā ar saistītu veselības uzkrājumu kontu (health savings account — HSA).

- Dzīvības apdrošināšanas plāns ar obligātu darbinieku dzīvības apdrošināšanas plānu, kas iekļauts komplektā ar apgādājamā dzīvības apdrošināšanas plānu. Tas nodrošinātu, ka darbinieks nevar atlasīt apgādājamā dzīvības apdrošināšanas segumu bez pierakstīšanās darbinieka segumam.

1. Darbvietā **Atvieglojumu pārvaldība** sadaļā **Iestatīt** atlasiet **Piemērotības kārtulas un opcijas**.

2. Lai izveidotu komplektu, cilnē **Komplekti** atlasiet **Jauns**. Lai skatītu plānus, kas ir saistīti ar komplektu, atlasiet **Pievienotie plāni**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Saišķis** | Komplekta unikālais identifikators. |
   | **Apraksts** | Komplekta apraksts. |
   | **Šablons** | Norāda, vai viens no komplekta plāniem ir jāatzīmē kā galvenais plāns. Galveno plānu ir jāatlasa atvērtās reģistrācijas laikā kā daļu no komplekta, pirms atvieglojumu administrators var apstiprināt darbinieka atvieglojumu izvēli. |
   | **Obligāts**| Norāda, ka plāns ir jāatlasa, lai paņemtu jebkuru citu plānu saišķī. Kā Obligāts var atzīmēt vairākus **plānus**. Tādā gadījumā visi plāni, kas atzīmēti kā **Nepieciešami**, būs jāatlasa, lai paņemtu jebkuru no plāniem saišķī.|
   | **Derīguma sākuma datums un laiks** | Datums un laiks, kad komplekts kļūst aktīvs. |
   | **Derīgs līdz** | Komplekta darbības beigu termiņš. Pēc noklusējuma tas ir 12/31/2154, kas nozīmē "nekad". |

4. Atlasiet **Saglabāt**.

## <a name="configure-periods"></a>Periodu konfigurēšana

Periodi nosaka, kad atvieglojumi stājas spēkā un kad darbiniekiem ir atļauts reģistrēties. Varat izveidot tik daudzus periodus, cik vēlaties, lai saglabātu atvērtu reģistrāciju atvieglojumiem un atvieglojumu seguma periodus. Atvieglojumu plāna gadi var sakrist vai nesakrist ar kalendāro gadu. 

1. Darbvietā **Atvieglojumu pārvaldība** sadaļā **Iestatīt** atlasiet **Piemērotības kārtulas un opcijas**.

2. Lai izveidotu periodu, cilnē **Periodi** atlasiet **Jauns**. Lai izpildītu procesu, kas atvieglojumu periodam pievieno visus derīgos aktīvos atvieglojumu plānus, atlasiet **Pievienot plānus**. Lai skatītu plānus, kas ir saistīti ar komplektu, atlasiet **Pievienotie plāni**. 

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Periods** | Unikāls perioda identifikators. |
   | **Derīguma sākuma datums un laiks** | Sākuma datums un laiks, kad atvieglojumu periods ir aktīvs. |
   | **Derīguma beigu datums un laiks** | Sākuma datums un laiks, kad atvieglojumu periods kļūst neaktīvs. |
   | **Reģistrācijas sākums** | Atvērtās reģistrācijas sākuma datums. Atvērtā reģistrācija ir, kad darbinieks var veikt atvieglojumu izvēli patstāvīgi izmantojamajos atvieglojumos. |
   | **Reģistrācijas beigas** | Atvērtās reģistrācijas beigu datums. |
   | **Atvērtās** | Norāda, vai periods ir atvērts, pamatojoties uz sistēmas datumu un spēkā esamības sākuma un beigu datumiem un laikiem. | 
   | **Iepriekšējais periods** | Norāda atvieglojumu periodu, kas ir pirms atlasītā atvieglojumu perioda. Šī informācija tiek izmantota atvieglojumu piemērotības reģistrācijas laikā, lai piešķirtu plānus, segumu opcijas un pilnvarotas personas no iepriekšējā gada. |
 
4. Atlasiet **Saglabāt**.

## <a name="use-a-flex-credit-program"></a>Brīvā režīma kredīta programmas izmantošana

Varat izmantot brīvā režīma kredīta programmas, lai reģistrētu darbiniekus atvieglojumos atbilstoši iepriekš noteiktam brīvā režīma kredītu skaitam. Darbinieki var izvēlēties, kā sadalīt savus brīvā režīma kredītus. Piemēram, ja darbinieks ir apdrošināts sava dzīvesbiedra veselības apdrošināšanas plānā, viņš var vēlēties izmantot citiem atvieglojumiem kredītus, ko citādi izmantotu veselības apdrošināšanai.

1. Darbvietā **Atvieglojumu pārvaldība** sadaļā **Iestatīt** atlasiet **Piemērotības kārtulas un opcijas**.

2. Cilnē **Periodi** atlasiet **Brīvā režīma kredīta programmas**.

3. Atlasiet piemērojamo brīvā režīma kredīta programmu. Lauki satur tālāk minēto informāciju.

   | Lauks | Apraksts |
   | --- | --- |
   | **Atvieglojumu kredīta ID** | Brīvā režīma kredīta programmas unikālais identifikators. |
   | **Apraksts** | Brīvā režīma kredīta programmas apraksts. | 
   | **No datuma** | Datums, kad brīvā režīma kredīta programma kļūst aktīva. |
   | **Līdz datumam** | Datums, kad brīvā režīma kredīta programma beidz darboties. Varat atstāt noklusēto vērtību (12/31/2154), lai norādītu, ka brīvā režīma kredīta programmai nav ieplānota beigu termiņa. |
   | **Kopējā kredīta vērtība** | Kredītpunktu skaits, kas katram darbiniekam jāizmanto saviem atvieglojumiem. |
   | **Proporcionālas sadalīšanas kārtula** | Kārtula, ko izmanto, lai proporcionāli sadalītu brīvā režīma kredītus, ja darbinieks tiek nolīgts brīvā režīma kredīta perioda vidū. </br></br><ul><li>**Nav** — darbinieks nesaņem brīvā režīma kredītus, ja tas tiek pieņemti darbā pēc brīvā režīma kredīta programmas perioda sākuma.</li><li>**Pilns kredīts** — darbinieks saņem pilnu brīvā režīma kredītu summu, neatkarīgi no tā, kad tiek pieņemts darbā.</li><li>**Proporcionāla sadale** — darbinieks saņem proporcionālu brīvā režīma kredītu summu, pamatojoties uz pieņemšanas datumu.</li></ul> |
   | **Brīvā režīma kredīta proporcionālas sadales formula** | Kārtula, ko izmanto, lai proporcionāli sadalītu brīvā režīma kredītus darbiniekiem, kuri pieņemti darbā brīvā režīma kredīta atvieglojumu perioda vidū. Šīs proporcijas pamatā ir nodarbinātības sākuma datums. Šis lauks tiek izmantots tikai tad, ja laukā **Proporcionālās sadalīšanas kārtula** atlasāt **Proporcionāli sadalīt**. </br></br><ul><li>**Katru dienu** — proporcionāli sadala brīvā režīma kredītu skaitu, ko darbinieks saņem katru dienu. Kopējais brīvā režīma kredītu skaits tiek dalīts ar dienu skaitu periodā. Piemēram, ja atvieglojumu periods ir 400 dienas, sistēma kopējo brīvā režīma kredītu skaitu izdalīs ar 400, lai aprēķinātu brīvā režīma kredītpunktu skaitu, ko darbinieki saņems katru dienu.</li><li>**Pašreizējā mēnesī** — proporcionāli sadala brīvā režīma kredītu skaitu, ko darbinieks saņem katru mēnesi, noapaļojot līdz pašreizējam mēnesim. Kopējais brīvā režīma kredītu skaits tiek dalīts ar mēnešu skaitu periodā. Piemēram, ja atvieglojumu periods ir 15 mēneši, sistēma kopējo brīvā režīma kredītu skaitu izdalīs ar 15, lai aprēķinātu brīvā režīma kredītpunktu skaitu, ko darbinieki saņems katru mēnesi.</li><li>**Nākamajā mēnesī** — proporcionāli sadala brīvā režīma kredītu skaitu, ko darbinieks saņem katru mēnesi, noapaļojot līdz nākamajam mēnesim. Kopējais brīvā režīma kredītu skaits tiek dalīts ar mēnešu skaitu periodā. Piemēram, ja atvieglojumu periods ir 15 mēneši, sistēma kopējo brīvā režīma kredītu skaitu izdala ar 15, lai aprēķinātu brīvā režīma kredītpunktu skaitu, ko darbinieki saņems katru mēnesi.</li></ul> |
   
   Pārliecinieties, ka katrs atvieglojumu plāns tiek reģistrēts tikai vienā brīvā režīma kredīta programmā katram atvieglojumu periodam. Pretējā gadījumā sistēma nezinās, kuru brīvā režīma kredīta programmu izmantot, lai piešķirtu brīvā režīma kredītus, un radīsies problēmas. 

## <a name="configure-programs"></a>Programmu konfigurēšana

Programmas ir atvieglojumu plānu kopa, kam ir kopīga piemērotības kārtulu kopa. Varat definēt piemērotības kārtulas visai programmai, nevis katram atsevišķam plānam. Piemēram, Contoso Canada FTE programma vai Contoso Europe vadības līmeņa programma. 

1. Darbvietā **Atvieglojumu pārvaldība** sadaļā **Iestatīt** atlasiet **Piemērotības kārtulas un opcijas**.

2. Lai izveidotu programmu, cilnē **Programmas** atlasiet **Jauns**. Lai izdarītu izņēmumus darbiniekiem, kuri neatbilst piemērotības kārtulas prasībām, atlasiet **Piemērotības kārtulas ignorēšana**. Lai skatītu plānus, kas ir saistīti ar programmu, atlasiet **Pievienotie plāni**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Aplikācija** | Programmas unikālais identifikators. |
   | **Apraksts** | Programmas apraksts. | 
   | **Derīguma sākuma datums un laiks** | Datums un laiks, kad programma kļūst aktīva. |
   | **Derīguma beigu datums un laiks** | Datums un laiks, kad beidzas programmas termiņš. Pēc noklusējuma tas ir 12/31/2154, kas nozīmē "nekad". |
   | **Vajadzības gaidīšanas periods** | Periods, ko darbiniekam jāgaida, pirms seguma sākuma atvieglojumu programmā. |
   | **Ieturējumu gaidīšanas periods** | Periods, ko darbinieks gaida, pirms sākas ieturējumi atvieglojumu programmai. |
   | **Piemērojamības kārtulas** | Atlasiet piemērotības kārtulas, ko piemērot atvieglojumu programmai. Nosakiet piemērotības kārtulas šīs lapas cilnē **Piemērotības kārtulas**. |
   
4. Atlasiet **Saglabāt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
