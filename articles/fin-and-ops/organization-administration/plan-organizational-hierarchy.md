---
title: "Organizācijas hierarhijas plānošana"
description: "Pirms iestatāt organizācijas un organizāciju hierarhijas, ir jāpārliecinās, vai saprotat, kā vislabāk modelēt savu uzņēmumu."
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d669defa13e8f32cd29463324e580a6d738c3e2a
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="plan-your-organizational-hierarchy"></a>Organizācijas hierarhijas plānošana

[!include[banner](../includes/banner.md)]


Pirms organizāciju un organizācijas hierarhiju iestatīšanas programmatūrā Microsoft Dynamics 365 for Finance and Operations noteikti plānojiet sava uzņēmuma modelēšanas veidu. Organizācijas modelis būtiski ietekmē Finance and Operations ieviešanu un biznesa procesus. 

Organizācijas hierarhijas atspoguļo attiecības starp organizācijām, kas veido uzņēmumu. Tāpēc vissvarīgākais apsvērums, modelējot organizācijas, ir jūsu uzņēmuma struktūra. Mēs iesakām definēt organizācijas struktūras, pamatojoties uz atsauksmēm no vadošajiem darbiniekiem un funkcionālo jomu, piemēram, finanšu un uzskaites, cilvēkresursu, operāciju, sagādes un pārdošanas un mārketinga, augstākā līmeņa vadītājiem. 

Plānojot hierarhijas, ir svarīgi arī ņemt vērā attiecības starp organizācijas hierarhiju un finanšu dimensijām. Skatus jūsu uzņēmumam var iestatīt vairākas organizācijas hierarhijas. Izmantojot finanšu dimensijas, var izveidot ziņojumus, pamatojoties uz šiem skatiem. Sadarbojieties ar savu Microsoft Dynamics 365 for Finance and Operations partneri, lai izveidotu hierarhijas, kas atbilst gan organizācijas, gan likumā noteiktās pārskatu izveides vajadzības. 

> [!Note]
> Lai gan finanšu dimensijas varat izmantot, lai apzīmētu juridiskās personas, bez nepieciešamības šīs juridiskās personas izveidot programmatūrā Finance and Operations, finanšu dimensijas nav paredzētas juridisko personu operāciju vai uzņēmējdarbības vajadzību nodrošināšanai. Programmatūras Finance and Operations starpvienību uzskaites funkcionalitāte ir paredzēta darbam tikai ar katras transakcijas ietvaros izveidotajiem uzskaites ierakstiem. 

> [!Caution]
> Jums nevajadzētu izlemt par veidu, kā modelēt organizācijas, pamatojoties tikai uz šajā rakstā sniegto informāciju. Šī dokumentācija ir ceļvedis. Lai saņemtu papildu norādes, varat sadarboties ar savu Finance and Operations partneri. Jūsu Finance and Operations partneris ir guvis pieredzi, strādājot dažādās nozarēs un ar dažādiem klientiem.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Izlemiet, vai modelēt iekšējās organizācijas kā juridiskās personas vai pārvaldības struktūrvienības

Ir jābūt vismaz vienai juridiskajai personai, kas pārstāv jūsu uzņēmumu programmatūrā Finance and Operations. Juridiskā persona var noslēgt juridiskus līgumus, un tām ir nepieciešams sagatavot finanšu pārskatus, ziņojot par savu veiktspēju. 

Programmatūrā Finance and Operations juridiskās personas var izmantot transakciju uzņēmējdarbības vai konsolidācijas vajadzībām. Tas nozīmē, ka juridiskā persona programmatūrā Finance and Operations ne vienmēr atspoguļo reālu jūsu biznesa elementu. Piemēram, uzņēmumam, kas piedalās transakcijās, var piederēt meitas juridiskās personas. Šādā gadījumā transakcijām ir nepieciešama juridiskā persona un meitas juridisko personu rezultātu un bilanču konsolidēšanai ir nepieciešama virtuāla juridiskā persona. 

Jūsu biznesa iekšējās organizācijas, piemēram, reģionālos birojus, var atspoguļot ka papildu juridiskās vienības vai ka galvenās juridiskās personas pārvaldības struktūrvienības. Pārvaldības struktūrvienībai nav obligāti jābūt juridiski definētai organizācijai. Pārvaldības struktūrvienības tiek izmantotas ekonomisko resursu un biznesa darba procesu kontrolei. Piemēram, nodaļas un izmaksu centri ir pārvaldības struktūrvienības. 

Dažas funkcijas programmatūrā Finance and Operations darbojas atšķirīgi atkarībā no tā, vai organizācija ir juridiska persona vai pārvaldības struktūrvienība. Pieņemot lēmumu, rūpīgi apsveriet tālāk aprakstīto funkcionalitāti. 


### <a name="master-data"></a>Pamatdati
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona      
Daži pamatdati, piemēram, klienti, maksājumu noteikumi, nodokļu iestādes un konkrētas vietas krājumu pasūtīšana, katrai juridiskajai personai ir jāveido atsevišķi. Daži pamatdati, piemēram, lietotāji, produkti un lielākā daļa cilvēkresursu datu, ir kopīgi visām juridiskajām personām. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Pamatdati ir kopīgi pārvaldības struktūrvienībām. 

### <a name="module-parameters"></a>Moduļa parametri
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona    
Katrai juridiskajai personai ir jāiestata moduļu parametri, piemēram, parametri sadaļās Debitoru moduļa parametri, Kreditoru parādu parametri un Kases un bankas vadības parametri. Tā kā moduļu iestatīšana juridiskajām personām notiek atsevišķi, katrs meitas uzņēmums var ievērot vietējās likumā noteiktās prasības un biznesa praksi. Piemēram, juridiskai personai - profesionālam pakalpojumu sniedzējam un juridiskajai personai - ražotājam var būt dažādi moduļu parametri, lai arī tās ir pakļautas vienam un tam pašam mātes uzņēmumam. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Moduļa parametri ir kopīgi pārvaldības struktūrvienībām. 

### <a name="data-security"></a>Datu drošība
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona    
Lielākā daļa datu tiek automātiski aizsargāta ar uzņēmuma ID. Uzņēmuma ID ir unikāls identifikators datiem, kas ir saistīti ar juridisko personu. Uzņēmums var būt saistīts ar tikai vienu juridisko personu, un juridiskā persona var būt saistīta ar tikai vienu uzņēmumu. Lietotāji var piekļūt tikai datiem par uzņēmumiem, kuriem viņiem ir piekļuve. Programmatūra Finance and Operations nav jāpielāgo, lai nodrošinātu datu aizsardzību ar uzņēmuma ID. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Datus var nodrošināt pa pārvaldības struktūrvienībām, izveidojot pielāgotas datu drošības politikas. Datu drošības politikas tiek izmantotas, lai ierobežotu piekļuvi datiem. Piemēram, pieņemsim, ka lietotājs drīkst izveidot pirkšanas pasūtījumus tikai konkrētai pārvaldības struktūrvienībai. Datu drošības politikas var izveidot tā, lai lietotājam neļautu piekļūt pirkšanas pasūtījuma datiem no citas pārvaldības struktūrvienības. Transakciju apjoms un drošības politiku skaits var ietekmēt veiktspēju. Veidojot drošības politikas, paturiet prātā veiktspēju. 

### <a name="ledgers"></a>Virsgrāmatas
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona    
Katrai juridiskajai personai nepieciešama virsgrāmata, kas nodrošina kontu plānu, uzskaites valūtu, pārskata valūtu un finanšu kalendāru. Bilanci var izveidot tikai juridiskai personai. Galvenie konti, dimensijas, kontu struktūras, kontu diagrammas un uzskaites nosacījumus var izmantot vairākas juridiskās personas.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Pārvaldības struktūrvienībai nevar būt sava virsgrāmatas informācija. Ja jūsu iekšējām organizācijām nav nepieciešami unikāla virsgrāmata, jūs varat tas modelēt kā pārvaldības struktūrvienības. Virsgrāmatas informācija tiks iestatīta hierarhijā mātes juridiskajai personai. Ienākumu pārskatus var izveidot pārvaldības struktūrvienībām juridiskās personas ietvaros vai mātes juridiskajai personai. 

### <a name="fiscal-calendars"></a>Finanšu kalendāri 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona    
Katrai juridiskajai personai ir savs finanšu kalendārs. Ja jūsu iekšējās organizācijas izmanto dažādus finanšu gadus un finanšu kalendārus, organizācijas jāmodelē kā juridiskās personas. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Pārvaldības struktūrvienībām ir jābūt kopīgam finanšu kalendāram. Ja jūsu iekšējās organizācijas var izmantot vienādus finanšu gadus un finanšu kalendārus, organizācijas var modelēt kā pārvaldības struktūrvienības. 

### <a name="consolidation"></a>Konsolidācija
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona    
Lai sagatavotu finanšu pārskatus, reģionālo biroju finanšu rezultāti ir jākonsolidē viena, konsolidētā uzņēmumā. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Konsolidācija nav nepieciešama, jo pārvaldības struktūrvienību dati jau ir kopīgi. 

### <a name="centralized-payments"></a>Centralizēti maksājumi
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona 
Ir jāizveido centralizēti maksājumi, lai visu meitas juridisko personu rēķinus varētu maksāt vienai mātes juridiskajai personai vai tos maksātu viena mātes juridiskā persona. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Centralizētie maksājumi nav nepieciešami, jo visi rēķini tiek reģistrēti vienai juridiskai personai.

### <a name="intercompany-transactions"></a>Starpuzņēmumu transakcijas
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona 
Starpuzņēmumu pārdošanas pasūtījumus, pirkšanas pasūtījumus, maksājumus vai kvītis var lietot savstarpēji. Jums nav nepieciešams izmantot žurnāla dokumentus. Jūs varat skatīt starpuzņēmumu transakcijas pakārtotās virsgrāmatas līmenī (debitori, kreditori). Tālāk ir paskaidrots, kā tiek apstrādātas starpuzņēmumu transakcijas. 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>1. piemērs. Galvenā pārvalde sniedz pakalpojumus reģionālajiem birojiem, un tai no reģionālajiem birojiem ir jāietur maksa par šiem pakalpojumiem
Ja reģionālo biroju jūs modelējat kā juridisku personu, jums ir tālāk norādītās iespējas. 
- Galvenā pārvalde izveido žurnāla ierakstu, lai maksu par izdevumiem savstarpēji ieturētu no reģionālā biroja. Transakcijām nevar noteikt vecumu.
- Galvenā pārvalde reģionālajam birojam nosūta pirkšanas pasūtījumu par pakalpojumiem. Juridiskajā personā tiek automātiski izveidots pārdošanas pasūtījums reģionālajam birojam ar pakārtotās virsgrāmatas transakcijām. 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>2. piemērs. Galvenā pārvalde iegādājas pakalpojumu un maksā par pakalpojumu, kas tiek piegādāts reģionālajam birojam
Ja reģionālo biroju jūs modelējat kā juridisku personu, jums ir tālāk norādītās iespējas. 
- Rēķinam un maksājumam tiek ievērotas galvenās pārvaldes normatīvās prasības. Galvenā pārvalde var izveidot žurnāla ierakstu, lai savstarpēji ieturētu no reģionālā biroja maksu par izdevumiem. Transakcijām nevar noteikt vecumu. 
- Rēķinam un maksājumam tiek ievērotas galvenās pārvaldes normatīvās prasības. Galvenā pārvalde var izveidot starpuzņēmumu pakārtotās virsgrāmatas transakciju.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Starpuzņēmumu transakcijas starp pārvaldības struktūrvienībām tiek atbalstītas tikai caur žurnāla dokumentiem. Pārvaldības struktūrvienība nevar izdot vai saņemt pirkšanas pasūtījumu, pārdošanas pasūtījumu vai rēķinu no cita pārvaldības struktūrvienības vienas un tās pašas juridiskās personas ietvaros. Jūs nevarat skatīt starpuzņēmumu transakcijas pakārtotās virsgrāmatas līmenī (debitori, kreditori). Tālāk ir paskaidrots, kā tiek apstrādātas starpuzņēmumu transakcijas. 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>1. piemērs. Galvenā pārvalde sniedz pakalpojumus reģionālajiem birojiem, un tai no reģionālajiem birojiem ir jāietur maksa par šiem pakalpojumiem
Ja jūs modelējat reģionālo biroju kā pārvaldības struktūrvienību, galvenā pārvalde ievada izdevumu transakciju un kodē to reģionālajam birojam. 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>2. piemērs: Galvenā pārvalde iegādājas un maksā par pakalpojumu, kas tiek piegādāts reģionālajam birojam.
Ja jūs modelējat reģionālo biroju kā pārvaldības struktūrvienību, rēķinam un maksājumam tiek ievērotas galvenās pārvaldes ar likumu noteiktās prasības. Rēķins var tikt kodēts reģionālajam birojam. Lai ziņotu reģionālā biroja izmaksas, peļņas vai zaudējumu pārskatā izmantojiet līdzsvarojošo finanšu dimensiju.

### <a name="local-tax-requirements"></a>Vietējās nodokļu prasības
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona
Juridiskā persona ir pakļauta juridiskās personas reģistrācijas valsts/reģiona nodokļu iestādes nodokļu likumiem. Piemēram, juridiskā persona, kas ir reģistrēta Dānijā, ir pakļauta Dānijas nodokļu likumiem un noteikumiem. Programmatūrā Finance and Operations juridiskā persona var tikt reģistrēta tikai vienā valstī/reģionā. Valsts/reģions, ko atlasāt juridiskās personas primārajai adresei, nosaka valstij/reģionam specifiskos līdzekļus, kas ir pieejami šai juridiskajai personai. Piemēram, ja juridiskās personas primārā adrese ir Dānijā, ir pieejami līdzekļi, kas ir saistīti ar Dānijas nodokļu likumiem un noteikumiem. Tāpēc, ja jūsu organizācijai atrodas dažādās valstīs/reģionos un tām nepieciešamas dažādas vietējās nodokļu iespējas, jums jāiestata organizācijas kā atsevišķas juridiskas personas.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Pārvaldības struktūrvienības izmanto mātes juridiskās personas valsts kontekstu. Pārvaldības struktūrvienībām vienā juridiskajā personā nevar būt dažādas valstij/reģionam specifiskas prasības. Ja jūsu organizācijas atrodas vienā valstī/reģionā un izmanto vienas un tās pašas nodokļu iespējas, varat tās iestatīt kā pārvaldības struktūrvienības.


### <a name="statutory-reporting-for-a-countryregion"></a>Likumā noteiktie pārskati valstij/reģionam 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona
Valstīm/reģioniem, kas tiek atbalstīti programmatūrā Finance and Operations, var izveidot lielāko daļu likumā noteikto pārskatu. Informāciju par to, kuri pārskati ir pieejami katrai valstij/reģionam, skatiet portāla [Microsoft Dynamics Localization Portal](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC) sadaļā par Finance and Operations. (Nepieciešama CustomerSource pieteikšanās.) 

> [!Note]
> Programmatūrā Finance and Operations grāmatošanas līmenis virsgrāmatā jums ļauj veidot pielāgošanas ierakstus mātes uzņēmumā, kas izmanto citādu uzskaites standartu nekā meitas uzņēmums. Piemēram, uzņēmumam, kas izmanto Apvienotās Karalistes vispārpieņemtos grāmatvedības principus (UK GAAP), varat veikt pielāgošanas ierakstus grāmatošanas līmeni. Šos ierakstus var konsolidēt mātes uzņēmumā, kas izmanto Amerikas Savienoto Valstu vispārpieņemtos grāmatvedības principus (GAAP). Pielāgošanas ieraksti neietekmē UK GAAP pārskatu.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Ar likumu noteiktie pārskati ir jāveido, izmantojot citu programmu. Ir jānodrošina, ka programmatūrā Finance and Operations tiek reģistrēti dati, kas atbilst katras pārvaldības struktūrvienības prasībām, ja tās atšķiras no galvenās pārvaldes prasībām. 

### <a name="currency"></a>Valūta
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona
Ja jūsu iekšējām organizācijām jāizmanto dažādas funkcionālās valūtas, organizācijas jāmodelē kā juridiskās personas. Funkcionālās valūtas tiek iestatītas pa juridiskajām personām. Tomēr jūs varat ievadīt transakcijas vairākās valūtās. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Ja jūsu organizācijas var izmantot vienu funkcionālo valūtu, varat modelēt organizācijas kā pārvaldības struktūrvienības. Pārvaldības struktūrvienībām ir jābūt kopīgai funkcionālajai valūtai. Tomēr jūs varat ievadīt transakcijas un izveidot pārskatus vairākās valūtās. 


### <a name="year-end-closing"></a>Gada beigu slēgšana
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona
Ja pastāv atšķirības starp likumiem un uzskaites praksēm valstīs/reģionos, kur atrodas jūsu organizācijas, katrai organizācijai var būt nepieciešamas dažādas gada beigu procedūras. Tas nozīmē, ka organizācijas ir jāmodelē kā juridiskas personas. Katrai juridiskajai personai ir savas gada beigu procedūras. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Ja likumi un uzskaites prakses valstīs/reģionos, kur atrodas jūsu organizācijas, ir vienādas, varat izmantot vienu gada beigu procedūru kopu. Tas nozīmē, ka varat modelēt organizācijas ka pārvaldības struktūrvienības. Visām pārvaldības struktūrvienībām ir jāizmanto vienu un tā pati gada beigu slēgšanas procedūra. 
   
### <a name="number-sequences"></a>Numuru sērijas
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona
Numuru rindas dažām atsaucēm var iestatīt pēc juridiskās personas. Dažas numuru rindas var koplietot. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Numuru rindas dažām atsaucēm var iestatīt pēc pārvaldības struktūrvienības. Dažas numuru rindas var koplietot.

### <a name="products"></a>Preces 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona
Preču definīcijas ir kopīgas, un tas ir jānodod individuālajam juridiskajām personām, pirms tās var iekļaut transakcijās. Katrai juridiskajai personai ir sava nodoto preču kopa, ko var iekļaut transakcijas dokumentos. Ja jūsu iekšējām organizācijām jāizmanto dažādas preču kopas, organizācijas jāmodelē kā juridiskās personas. 

> [!Note]
> Lai arī preču definīcijas ir kopīgas, katrai juridiskajai personai, kurai ir nodota prece, var norādīt dažādus pārdošanas, pirkšanas un krājumu parametrus precei katrā krājumu vietā. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Visas pārvaldības struktūrvienības koplieto vienu un to pašu produktu kopu. Ja jūsu iekšējās organizācijas var koplietot vienu un to pašu preču kopu, organizācijas var modelēt kā pārvaldības struktūrvienības. 

### <a name="inquiry-and-reporting"></a>Pieprasījumi un pārskati  
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ja organizācija ir modelēta kā juridiska persona
Lai ievadītu transakcijas un veiktu pieprasījumus vairākās juridiskajās personās, uzņēmumi ir jānomaina manuāli. Datu drošības robežu dēļ konsolidēti pieprasījumi un pārskati var patērēt daudz resursu un laika. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ja organizācija ir modelēta kā pārvaldības struktūrvienība 
Lai piekļūtu datiem no vairākām pārvaldības struktūrvienībām, uzņēmumi nav jāmaina. Konsolidēti pieprasījumi un pārskati un individuāli reģionāli pieprasījumi ir vieglāki un ātrāki.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Organizāciju un hierarhiju modelēšanas labākā prakse
Ieviešot organizācijas hierarhiju, ņemiet vērā šādu labāko praksi:
-   Izveidojiet nodaļu, lai modelētu krustošanos starp juridisko personu un biznesa vienību. Tad varat apvienot datus no nodaļas uz juridisko personu ar likumu noteikto pārskatu vajadzībām un no nodaļas uz biznesa vienību iekšējo pārskatu vajadzībām. Nodaļas var kalpot kā peļņas centri. Ja izmantojat nodaļas, nav jāizmanto juridiskās personas un biznesa vienības kā dimensijas konta struktūrā. Varat izmantot tikai nodaļas kā dimensiju. Tomēr ir jāizmanto gan izmaksu centri, gan nodaļas kā dimensijas konta struktūrā, ja izmaksu centri tiek izmantoti tikai kā izmaksu uzkrājēji un nodaļas tiek izmantotas ieņēmumu atzīšanai.
-   Modelējiet vairākas hierarhijas pārvaldības struktūrvienībām, ja jums ir sarežģītas prasības peļņas un zaudējumu pārskatam.
-   Nemodelējiet vairākas hierarhijas vienas juridiskās personas ietvaros vienam un tam pašam hierarhijas nolūkam.
-   Neveidojiet hierarhiju katram nolūkam. Parasti varat izmantot vienu hierarhiju vairākiem nolūkiem. Piemēram, vienu pārvaldības struktūrvienību hierarhiju var piešķirt visiem ar politiku saistītajiem nolūkiem.
-   Veidojiet līdzsvarotas hierarhijas. Visi hierarhijas zari, kas ir vienādā attālumā no saknes zara, tiek definēti ka līmenis. Līdzsvarotā hierarhijā katrā līmenī var būt tikai viens pārvaldības struktūrvienības veids, un attālums no saknes zara līdz katram līmenim ir nemainīgs. Ja starp nodaļu un juridisko personu vai biznesa vienību ir starpposma līmeņi, līdzsvarotas hierarhijas izveidei var būt nepieciešamas viettura organizācijas.
-   Nemodelējiet atsevišķu pārvaldības struktūrvienību hierarhiju, ja juridisko personu struktūra ir arī jūsu darba struktūra. Jaukta juridisko personu un pārvaldības struktūrvienību hierarhija var kalpot abiem nolūkiem.
-   Pirms modelējat nopietnus restrukturizācijas scenārijus, izmantojiet hierarhijas derīguma datumus, lai veiktu ietekmes analīzi un apstiprināšanas pārbaudi.
-   Izmantojiet melnraksta režīmu, lai mainītu hierarhiju, pirms publicējat jaunu versiju ražošanas vidē.
-   Ierobežojiet cilvēku skaitu, kam ir atļaujas pievienot vai noņemt organizācijas no hierarhijas ražošanas vidē. Mazāks skaits samazina iespēju, ka var rasties dārgas kļūdas un ir jāveic labojumi.

