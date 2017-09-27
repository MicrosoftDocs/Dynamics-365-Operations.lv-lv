--- 
title: "Iekasēšanas informācijas pārskatīšana"
description: "Šajā procedūrā parādīts, kā pārskatīt iekasēšanas informāciju, kā arī aprakstītas dažādas iestatīšanas opcijas un iekasēšanas transakcijas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b28d41d5ecf63b22cb84aff0c12a36cb0d728945
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="review-collections-information"></a>Iekasēšanas informācijas pārskatīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā pārskatīt iekasēšanas informāciju, kā arī aprakstītas dažādas iestatīšanas opcijas un iekasēšanas transakcijas. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="create-customer-pools"></a>Debitoru kopu izveide
1. Dodieties uz Kredīts un iekasēšana > Iestatīšana > Debitoru kopas.
    * Izmantojiet šo lapu, lai iestatītu debitoru kopas, kas ir vaicājumi, kuri definē debitoru kontu grupu, ko var parādīt un pārvaldīt iekasēšanas un vecumstruktūras procesiem. Izmantojiet debitoru kopas, lai filtrētu informāciju lapā Iekasēšanu saraksts un saistītajās sarakstu lapās. Debitoru kopas var arī izmantot, lai filtrētu debitoru kontus, kas tiek iekļauti vecumstruktūras momentuzņēmumu izveidošanas laikā.  
    * Debitoru kopas var izmantot, lai filtrētu debitoru kontus, kas tiek iekļauti vecumstruktūras momentuzņēmumu izveidošanas laikā.  
2. Noklikšķiniet uz Jauns.
3. Laukā Kopas ID ierakstiet vērtību.
4. Laukā Kopas apraksts ierakstiet vērtību.
5. Noklikšķiniet uz Atlasīt kopas kritērijus.
6. Laukā Kritēriji ierakstiet kādu vērtību.
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz Priekšskatīt debitoru kopu.

## <a name="create-collections-agents"></a>Iekasēšanas aģentu izveide
1. Dodieties uz Kredīts un iekasēšana > Iestatīšana > Iekasēšanas aģenti.
    * Izmantojiet šo lapu, lai iestatītu darbiniekus kā iekasēšanas aģentus un pēc izvēles tiem piešķirtu debitoru kopas. Iekasēšanas aģents ir persona, kas strādā ar debitoriem, lai nodrošinātu, ka maksājumi tiek saņemti savlaicīgi.  
    * Iekasēšanas aģenti, kas ir iestatīti šajā lapā, tiek automātiski pievienoti iekasēšanas grupai. Ja grupa tika atlasīta lapas Debitoru moduļa parametri laukā Grupa, iekasēšanas aģenti tiek pievienoti šai grupai. Ja grupa netika atlasīta, automātiski tiek izveidota jauna grupa ar nosaukumu Iekasēšana, un iekasēšanas aģenti tiek pievienoti šai grupai.  
2. Noklikšķiniet uz Jauns.
3. Noklikšķiniet uz Pievienot.
4. Noklikšķiniet uz Aizvērt.
5. Noklikšķiniet uz Pievienot.
6. Sarakstā atzīmējiet atlasīto rindu.
7. Laukā Kopas ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
9. Atzīmējiet izvēles rūtiņu Noklusējuma kopa vai noņemiet tās atzīmi.
    * Atzīmējiet šo opciju, lai atlasītajam iekasēšanas aģentam filtru sarakstos iekļautu visas debitoru kopas. Ja šī opcija nav atzīmēta, tad filtru sarakstos ir pieejamas tikai tās debitoru kopas, kas ir piešķirtas šim iekasēšanas aģentam.  

## <a name="create-aging-period-definition"></a>Vecumstruktūras perioda definīcijas izveide
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Vecumstruktūras perioda definīcijas.
    * Vecumstruktūras definīcijas varat izmantot, lai analizētu debitora un kreditora kontu kavējumus, kas pamatoti uz viņu ievadīto datumu. Katrs novecošanas periods, ko iestatāt novecošanas perioda definīcijai, atbilst kolonnai saraksta lapā vai formā vai pārskatam, kad tiek veikta analīze.  
2. Noklikšķiniet uz Jauns.
3. Laukā Vecumstruktūras periods definīcija ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
    * Norādiet perioda nosaukumu, vienību un intervālu katram vecumstruktūras periodam, kas jāiekļauj vecumstruktūras perioda definīcijā. Rinda, kuras vērtība laukā Vienība ir 0 (nulle), ir datums, kad tika veikta analīze. Rindās pirms nulles būs ievadīts –1, savukārt rindās aiz nulles — lauka Vieniba noklusējuma ieraksts būs 1, bet to varēs mainīt.  Noklikšķiniet uz pogas ar augšup vai lejupvērsto bultiņu, lai pārkārtotu rindas. Rindu 0 (nulle) nevar pārvietot.  
    * Novietojiet rādītāju vietā, kur vēlaties ievietot jaunu rindu un nospiediet Pievienot.  
    * Atlasiet rādītāju, lai vecumstruktūras periodu atspoguļotu formā Iekasēšana un saraksta lapā. Piemēram, varat atlasīt zaļu indikatoru pašreizējam periodam, dzeltenu indikatoru — 30 dienu pagājušajam periodam, sarkanu indikatoru — 90 dienu pagājušajam periodam.  
    * Izvēlieties vecumstruktūras perioda definīcijas drukas virzienu. Šī atlase nosaka kārtību, kādā kolonnas parādās debitoru vecumstruktūras pārskatā vai kreditoru vecumstruktūras pārskatā.  Uz priekšu — drukā kolonnas tādā secībā, kādā virsraksti parādās tabulā, sākot ar augšējo rindu.  Atpakaļejoši — drukā kolonnas tādā secībā, kas ir pretēja tai, kādā virsraksti parādās tabulā, sākot ar apakšējo rindu.    

## <a name="setup-collections-parameters"></a>Iekasēšanas parametru iestatīšana
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru parametri.
2. Noklikšķiniet uz cilnes Iekasēšana.
3. Izvērsiet vai sakļaujiet sadaļu Iekasēšanas noklusējumi.
    * Atlasiet vecumstruktūras perioda definīciju noklusējuma vecumstruktūras momentuzņēmumam, kas tiks izmantota formā Iekasēšana.  
    * Atlasiet grupu, kuras iekasēšanas aģenti tiek piešķirti formā Iekasēšanas aģents. Sarakstā tiek parādītas tikai grupas, kuru grupas veids ir Iekasēšana.  
4. Izvērsiet vai sakļaujiet sadaļu Norakstīšana.
    * Atlasiet žurnāla nosaukumu, kurš ir iestatīts ikdienas Virsgrāmatas žurnāliem, lai to izmantotu, kad transakcija tiek norakstīta, lietojot formu Iekasēšana vai saistītās saraksta lapas.  
    * Atlasiet noklusējuma iemesla kodu, ko izmantot, kad tiek veidotas norakstīšanas transakcijas, izmantojot formu Iekasēšana vai saistītās saraksta lapas.  
    * Atlasiet šo opciju, lai izveidotu atsevišķu žurnālu rindu PVN summām, kad tiek veidotas norakstīšanas transakcijas, izmantojot iekasēšanu lapu vai saistītās saraksta lapas. Ja atlasāt šo opciju, varat vienkāršāk sekot līdzi PVN summām, kas ir iesaistītas norakstīšanas transakcijās. Varat izsekot PVN summām atsevišķi, lai palīdzētu ērtāk pielāgot nodokļu parādu par ietekmēto periodu.  
5. Izvērsiet vai sakļaujiet sadaļu E-pasta veidne.
    * Atlasiet e-pasta veidni, kuru vēlaties izmantot, kad sūtāt e-pasta ziņojumu, izmantojot darbību E-pasts > Transakcijas ar kontaktpersonu formā Iekasēšana.  
    * Atlasiet e-pasta veidni, kuru vēlaties izmantot, kad sūtāt debitora pārskatu kā pielikumu e-pasta ziņojumam, izmantojot darbību E-pasts > Pārskati kontaktpersonai formā Iekasēšana.  
    * Atlasiet e-pasta veidni, kuru vēlaties izmantot, kad sūtāt e-pasta ziņojumu, izmantojot darbību E-pasts >Transakcijas ar pārdevēju formā Iekasēšana.  

## <a name="age-customer-balance"></a>Debitora bilances vecuma noteikšana
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Periodiskie uzdevumi > Vecas debitoru bilances.
    * Atlasiet vecumstruktūras perioda definīciju. Vecumstruktūras momentuzņēmums apstrādā vecuma transakcijas atbilstoši vecumstruktūras periodiem, kas ir definēti atlasītajā vecumstruktūras perioda definīcijā.  
    * Atlasiet debitoru kopu vai atstājiet šo lauku tukšu, lai izveidotu vecumstruktūras momentuzņēmumu visiem debitoriem. Ja ir atlasīta kāda debitoru kopa, tad vecumstruktūras momentuzņēmums apstrādā tikai tos debitoru kontus, kas ir daļa no attiecīgās debitoru kopas. Atlasītās debitoru kopas tipam ir jābūt Vecumstruktūras momentuzņēmums.  
    * Atlasiet datuma tipu, uz kā balstīt vecumstruktūras momentuzņēmumu.    Transakcijas datums — katras transakcijas vecums tiek noteikts, pamatojoties uz tās datumu.    Izpildes datums — katras transakcijas vecums tiek noteikts, pamatojoties uz tās izpildes datumu.    Dokumenta datums — katras transakcijas vecums tiek noteikts, pamatojoties uz tās dokumentēšanas datumu.  
    * Atlasiet datumu, ko izmantot kā vecumstruktūras momentuzņēmuma pašreizējo datumu. Vecumstruktūras periodi tiek aprēķināti, pamatojoties uz šo datumu.    Šodienas datums — izmanto sistēmas datumu. Izmantojiet šo opciju, ja apstrāde ir iestatīta izpildīšanai periodiskā pakešuzdevumā. Ja izmantojat šo datumu, tad periodisku pakešuzdevumu var palaist periodiski un tiek izmantots sistēmas datums attiecīgajā laikā.    Atlasītais datums — izmanto jūsu norādīto datumu. Ja atlasāt šo opciju, ievadiet vecuma datumu.  
2. Noklikšķiniet uz OK.

## <a name="view-aged-customer-balances"></a>Veco debitoru bilanču skatīšana
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iekasēšana > Vecas bilances.
    * Izmantojiet šo saraksta lapu, lai skatītu debitoru bilances un novecojušas summas pēc vecumstruktūras perioda. Šī informācija tiek uzglabāta vecumstruktūras momentuzņēmumā. Vecumstruktūras periodus nosaka vecumstruktūras perioda definīcija, kas tiek lietota. Vecumstruktūras perioda definīcija ir aizgūta no debitoru kopas, ja tāda ir norādīta kopas vaicājumam. Ja debitoru kopai nav vecumstruktūras perioda definīcijas, tiek lietota noklusējuma vecumstruktūras perioda definīcija, kas ir norādīta formā Debitoru parādu parametri.  
2. Izvērsiet papildinformācijas logu Kontaktpersona.
    * Debitora kontaktpersona iekasēšanas jautājumos.  
    * Debitora noklusējuma pārdevējs.  
3. Izvērsiet papildinformācijas logu Kredīta limits.
    * Lietojiet logu Informācija par kredītu papildinformācija, lai skatītu debitora kredīta limitu un pašreizējo bilances informāciju.  

## <a name="view-customer-collections-details"></a>Debitoru iekasēšanas datu skatīšana
1. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
2. Izvērsiet papildinformācijas sadaļu Adrese.
3. Izvērsiet papildinformācijas logu Kontaktpersona.
4. Izvērsiet papildinformācijas logu Vecumstruktūras.
5. Izvērsiet papildinformācijas logu Kredīta limits.
6. Darbību rūtī noklikšķiniet uz Iekasēt.
    * Atjauniniet debitora vecumstruktūras momentuzņēmumu, izmantojot pašreizējo datumu ka vecumstruktūras datumu, ar kuru tiek salīdzināti transakcijas datumi. Ja vecumstruktūras momentuzņēmums satur informāciju par vairākām juridiskām personām, atjauninātajā vecumstruktūras momentuzņēmumā tiks ietverta informācija par vienu un to pašu juridisko personu kopu. Summas tiek saglabātas tās juridiskās personas uzskaites valūtā, kuras kontā pieteicāties, kad atjauninājāt vecumstruktūras momentuzņēmumu.  
    * Atlasiet vecumstruktūras perioda definīciju. Pēc noklusējuma tiek rādīta tā vecumstruktūras perioda definīcija, kas ir saistīta ar parādītā debitora vecumstruktūras momentuzņēmumu. Vecumstruktūras perioda definīcija kontrolē vecumstruktūras periodus un summas, kas tiek rādītas papildinformācijas logā Vecas bilances un Kredīta informācija.  
    * Atveriet izvēlni, kas satur šādus elementus: Uzņēmums — parāda summas juridiskās personas uzskaites valūtā papildinformācijas logā Vecas bilances un Kredīta informācija.    Debitors — parāda summas debitora uzskaites valūtā papildinformācijas logā Vecas bilances un Kredīta informācija  
    * Debitora vecumstruktūras momentuzņēmumā atlasiet vienu vai vairākas juridiskās personas, kuru informāciju vēlaties skatīt. Juridiskās personas, kas tiek parādītas sarakstā, tika atlasītas vecumstruktūras momentuzņēmuma izveides laikā.  
    * Skatiet debitora pārskatu Microsoft Excel formātā. Var atlasīt, lai pārskatā iekļautu transakciju diapazons sākuma datumu un izlemt, vai ietvert tikai atvērtās transakcijas vai gan atvērtās, gan segtās transakcijas. Ja vecumstruktūras momentuzņēmumā ir iekļauta vairāku juridisko personu informācija, tiek iekļautas visu juridisko personu transakcijas.  
    * Atveriet formu Dokumenti, kurā var izveidot vai rediģēt dokumentus vai piezīmes.  
7. Darbību rūtī noklikšķiniet uz Sazināties.
    * Atveriet programmu Outlook, no kuras var nosūtīt e-pasta ziņojumu kontaktpersonai, kas tika norādīta laukā Kontaktpersona. Ja iekasēšanas kontaktpersona nav norādīta, tiek izmantota debitora konta primārā adrese. Ja nav norādīta primārā kontaktpersona, e-pasta ziņojumi tiks nosūtīti uz pirmo adresi, kas norādīta formā Kontaktpersonas. Atlasītas transakcijas tiek iekļautas kā pielikums. Pielikums ir Excel formātā un satur trīs darblapas. E-pasta ziņojumu veidni debitora kontaktpersonām var norādīt formā Debitoru parādu parametri.  
    * Šī poga nav pieejama, ja kontaktpersonai, kas atlasīta šajā formā, nav iestatīta e-pasta adrese.  
    * Sagatavojiet pārskatu un atveriet programmu Outlook, no kuras varat nosūtīt e-pasta ziņojumu ar pievienotu pārskats uz adresi, kas norādīta laukā Kontaktpersona. Ja iekasēšanas kontaktpersona nav norādīta, tiek izmantota debitora konta primārā adrese. Ja nav norādīta primārā kontaktpersona, e-pasta ziņojumi tiks nosūtīti uz pirmo adresi, kas norādīta formā Kontaktpersonas.  
    * Šī poga nav pieejama, ja kontaktpersonai, kas atlasīta šajā formā, nav iestatīta e-pasta adrese.  
    * Atveriet programmu Outlook, no kuras var nosūtīt e-pasta ziņojumu darbiniekam, kurš ir norādīts kā debitoram piešķirtās pārdošanas grupas tirdzniecības pārstāvis. Ja transakcijas ir atlasītas, tās tiek iekļautas kā pielikums. Pielikums ir Excel formātā un satur divas darblapas. E-pasta ziņojumu veidni pārdevējiem var norādīt formā Debitoru parādu parametri.  
    * Šī poga nav pieejama, ja pārdevējam, kas tiek rādīts šajā formā, nav iestatīta e-pasta adrese.  
    * Skatiet un izpildiet darbības ar debitoru transakcijām. Ja izmantojat centralizētus norēķinus, tiek iekļauta informācija par visām juridiskajām personām, kas ir iekļautas debitora vecumstruktūras momentuzņēmumā. Varat ierobežot informāciju par juridisko personu, izmantojot darbību rūts grupā Atlasīt esošo pogu Uzņēmums.  
    * Mainiet atlasīto transakciju iekasēšanas statusu.    Nav apstrīdēts — saistībā ar darījumu nav notikusi neviena iekasēšanas transakcija.    Apstrīdēts — debitors jums ir paziņojis, ka ar darījumu ir saistīta problēma.    Solīts apmaksāt — debitors ir piekritis apmaksāt darījumu.    Atrisināts — visas ar darījumu saistītās problēmas ir atrisinātas un nav nepieciešamas nekādas papildu iekasēšanas transakcijas.  
    * Atveriet izvēlni un atlasiet vienu no šiem elementiem, lai norādītu, kuras transakcijas ir jāparāda šajā formā: Atvērt — parāda tikai tās transakcijas, kas nav pabeigtas.    Atvērtas un slēgtas — parāda visas transakcijas, t.i., gan izpildītās, neizpildītās.  
    * Apstrādājiet atlasīto maksājumu kā tādu, kurā nepietiek naudas līdzekļu (NSF).    Šī poga ir pieejama tikai tad, ja atlasītā transakcija ir maksājums (kredīta bilance bez rēķina), kas ievadīts maksājumu žurnālā, transakcijai ir piešķirts bankas konts un maksājums iepriekš nav atcelts.  
    * Norakstiet atlasītās transakcijas.  
    * Atzīmējiet atlasītās transakcijas savstarpējai izpildei.  
    * Atveriet formu Oriģinālais dokuments, kurā var skatīt un drukāt atlasītās transakcijas dokumentu.  
    * Atveriet izvēlni, kas satur šādus elementus: Iekasēšana — parāda tikai tās darbības, kas tika izveidotas formā Iekasēšana.    Visas — parāda visas debitora darbības neatkarīgi no tā, kur tās tika izveidotas.  
    * Atveriet izvēlni, kas satur šādus elementus: Atvērtas — parāda tikai tās darbības, kas nav slēgtas.    Atvērtas un slēgtas — parāda visas darbības neatkarīgi no to statusa.  
    * Atlasiet iekasēšanas gadījumu, kas ir saistīts ar debitoru, vai atstājiet šo lauku tukšu. Ja gadījums ir atlasīts, šajā formā tiek parādītas tikai tās transakcijas un darbības, kas ir saistītas ar šo gadījumu.  
8. Noklikšķiniet uz Rādīt sarakstu.
    * Atlasiet debitora kontu vai akceptējiet noklusējuma ierakstu. Pēc noklusējuma saraksta lapā vai formā, no kuras atvērāt šo formu, tiek atlasīts šis debitora konts. Ja formu atvērāt no saraksta lapas, sarakstā ietvertie debitori ir tie, kuri ir ietverti iekasēšanas kopā, kas tiek izmantota saraksta lapā.  

