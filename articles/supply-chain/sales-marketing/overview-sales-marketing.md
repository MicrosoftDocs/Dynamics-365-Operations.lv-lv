---
title: "Pārdošana un mārketings"
description: "Moduli Pārdošana un mārketings varat izmantot, lai iegūtu, uzglabātu un izmantotu dažādu tipu datus pārdošanas plūsmā. Šie dati ietver sākotnējo pārdošanas iniciatīvu, turpmāko darbību un papildu pārdošanu."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 4de2ac36ec13f95c7603d097a0800b317014bbd0
ms.contentlocale: lv-lv
ms.lasthandoff: 05/22/2018

---

# <a name="sales-and-marketing"></a>Pārdošana un mārketings

[!include [banner](../includes/banner.md)]

Moduli Pārdošana un mārketings varat izmantot, lai iegūtu, uzglabātu un izmantotu dažādu tipu datus pārdošanas plūsmā. Šie dati ietver sākotnējo pārdošanas iniciatīvu, turpmāko darbību un papildu pārdošanu.

<a name="marketing"></a>Mārketings
---------

Mārketinga kampaņas un aktivitātes jūs izmantojat, lai atrastu un veidotu attiecības ar potenciālajiem klientiem un sākotnējās mijiedarbības varētu pārtapt par tirdzniecības attiecībām. Nākamajā procesa plūsmā ir parādīts biznesa process mārketingam. [![Mārketinga biznesa process](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Attiecības

Pārdošanā un mārketingā sākotnējās mijiedarbības, kas jums notiek ar potenciālajiem klientiem, var rasties dažādās situācijās. Piemēram, potenciālu klientu varat atrast, kamēr apmeklējat tirdzniecības izstādi, vai jums varētu būt potenciāla sadarbība ar klientu pēc tam, kad jūsu organizācija realizē lielapjoma pasta sūtīšanas kampaņu. Ir ļoti svarīgi izprast personas elementa plūsmu, pirms šī persona kļūst par klientu. Nākamajā attēlā ir parādīta elementu attiecību plūsma, potenciālajam klientam kļūstot par faktisku debitoru. [![SalesandMarketing01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampaņas

Kampaņa ir vērsta uz kontaktpersonām potenciālajiem klientiem, interesentiem, iespējām un debitoriem, kas ir atlasīti dalībai šajā kampaņā. Programmatūrā Microsoft Dynamics 365 for Finance and Operations varat izveidot vairāku tipu kampaņas, piemēram, telemārketinga, pasta sūtījumu un e-pasta kampaņas, lai maksimāli izmantotu debitoru potenciālu. Kad kampaņas gaitā saņemt pozitīvas atbildes, varat sākt pārdošanas procesu tiem adresātiem, kuri uz kampaņu ir atbildējuši pozitīvi.

## <a name="sales"></a>Pārdošana
Pārdošanas funkcionalitāti varat izmantot, lai izveidotu piedāvājumus, papildu pārdošanu un šķērspārdošanu jauniem un esošajiem klientiem, izveidot pārdošanas pasūtījumus un izveidot pārdošanas rēķinus debitoriem. Nākamajā procesa plūsmā ir parādīts biznesa process pārdošanai. [![Pārdošanas biznesa process](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Pārdošanas piedāvājumi

Jūs izveidojat pārdošanas piedāvājumus, lai debitoriem piedāvātu jūsu nodrošinātās preces vai pakalpojumus. Debitors var pieprasīt piedāvājumu, vai jūs varat izveidot piedāvājumu, atbildot uz potenciāla vai esoša debitora pieprasījumu. Kad debitors apstiprina pārdošanas piedāvājumu, jūs varat to pārveidot par pārdošanas pasūtījumu.

### <a name="up-sellcross-sell"></a>Papildu pārdošana/šķērspārdošana

Papildu pārdošana un šķērspārdošana ir preču pārdošanas metodes, kad debitoram ir ievadīts pasūtījums. Papildu pārdošanā tiek piedāvāta cita prece, nevis pašreizējā. Šķērspārdošanā prece tiek piedāvāta papildus pašreizējai precei. Kad iestatāt preču sarakstus, varat izveidot noteiktas kārtulas, lai norādītu, kad prece ir jāpiedāvā kā šķērspārdošanas vai papildu pārdošanas prece.

### <a name="sales-orders"></a>Pārdošanas pasūtījumi

Kad veidojat jaunu pārdošanas pasūtījumu, jums ir jāatlasa izveidojamā pārdošanas pasūtījuma tips. Pastāv piecas iespējas. **Piezīme.** Pēc pārdošanas pasūtījuma izveidošanas var mainīt jebkuru pasūtījuma tipu, izņemot tipu **Krājumu prasības**, ja pārdošanas pasūtījuma statuss ir **Piegādāts**.

| Pārdošanas pasūtījuma veids  | Apraksts                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Žurnāls           | Izmantojiet šo tipu kā melnrakstu pārdošanas pasūtījumam. Šis tips neietekmē rezervju daudzumu un neveido krājumu transakcijas.                                                                                                                                                                    |
| Abonements      | Izmantojiet šo tipu periodiskiem pasūtījumiem. Kad pasūtījums ir iekļauts rēķinā, pasūtījuma statuss tiek automātiski iestatīts uz atvērtu pasūtījumu. Piegādātais daudzums, kas bija iekļauts rēķinā, un atlikušās piegādes daudzumi tiek atjaunināti. Šo pārdošanas pasūtījuma tipu nevar izmantot, ja lietojat noliktavas vadības funkcionalitāti. |
| Pārdošanas pasūtījums       | Izmantojiet šo tipu, kad debitors ir veicis vai ratificējis pasūtījumu.                                                                                                                                                                                                                                        |
| Atgrieztais pasūtījums    | Izmantojiet šo tipu, kad debitors atgriež kādu krājumu. Atgrieztā krājuma kods (AKA kods) tiek piešķirts automātiski.                                                                                                                                                                                            |
| Krājumu pieprasījumi | Šis tips tiek izveidots automātiski, kad veidojat krājumu pārdošanu, izmantojot projektu.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Pārdošanas līgumi

Pārdošanas līgums ir līgums, ar kuru debitors piekrīt laika gaitā iegādāties noteiktu daudzumu preces vai iegādāties preci par noteiktu summu apmaiņā pret īpašām cenām un atlaidēm. Pārdošanas līguma cenām un atlaidēm ir prioritāte pār jebkādām cenām un atlaidēm, kas ir norādītas jebkādos jau pastāvošajos tirdzniecības līgumos. Pārdošanas līgums ir derīgs uz noteiktu laiku. Pieprasītajam nosūtīšanas datumam, kas pārdošanai ir norādīts lapā **Pārdošanas pasūtījums**, ir jāietilpst šajā derīgajā periodā. Pēc noklusējuma pārdošanas līgums ir aizturēts. No pārdošanas līguma varat pasūtīt tikai tad, ja tas ir iestatīts kā **Spēkā esošs**.

### <a name="backorders"></a>Neizpildītie pasūtījumi

Kad ievadāt un validējat pasūtījumus, iespējams, ir nepieciešams pārvaldīt neizpildītos pasūtījumus un izņēmumus, pirms pārdošanu ir iespējams pabeigt. Neizpildītie pasūtījumi ir pirkšanas pasūtījumi, kas vēl nav piegādāti no kreditora, vai pārdošanas pasūtījumi, kas nav vēl piegādāti debitoram. Ir svarīgi sekot līdzi neizpildītajiem pasūtījumiem. Piemēram, ja preces no kreditora kavējas, iespējams, jums ir jāmaina datums, kad prece tiek piegādāta debitoram, un pēc tam ir jāinformē debitors par kavēšanos. Neizpildītos pasūtījumus varat skatīt pēc krājuma, debitora vai kreditora.

#### <a name="viewing-backorders-by-item"></a>Neizpildīto pasūtījumu skatīšana pēc krājuma

Kad neizpildītos pasūtījumus skatāt pēc krājuma, varat izsekot paredzamajai aizkavēšanās transakciju plūsmai attiecībā uz šo krājumu. Piemēram, varat pārbaudīt šādu informāciju:

-   Krājumam veikto pārdošanas pasūtījumu skaits
-   Vai joprojām trūkst krājumu piegādes no kreditoriem
-   Vai ir jāpasūta vairāk krājumu, lai varētu laicīgi piegādāt visus pārdošanas pasūtījumus

Veicot šo pārbaudi, varat atbildēt uz debitoru vaicājumiem par preču piegādes laiku. Turklāt varat noteikt prioritāti pārdošanas neizpildītajiem pasūtījumiem un sadalīt rīcībā esošos krājumus starp pasūtījumiem.

#### <a name="viewing-backorders-by-customer"></a>Neizpildīto pasūtījumu skatīšana pēc debitora

Kad neizpildītos pasūtījumus skatāt pēc debitora, varat skatīt debitora atlikušo pasūtījumu statusu. Šī pārbaude noder, kad jums ir jāatbild debitoriem, kuri gaida krājumus, kuru piegāde aizkavējas.

#### <a name="viewing-backorders-by-vendor"></a>Neizpildīto pasūtījumu skatīšana pēc kreditoriem

Kad neizpildītos pasūtījumus skatāt pēc kreditora, varat sekot līdzi trūkstošajām piegādēm un paredzamajiem piegādes datumiem. Šī pārbaude jums palīdz arī noteikt prioritāti neizpildītajiem pasūtījumiem, kad preces tiek piegādātas no kreditoriem un ir jāizdod pārdošanas pasūtījumi piegādei.

### <a name="invoices"></a>Rēķini

Pārdošanas procesa laikā varat izveidot trīs tipu rēķinus:

-   Debitora rēķins
-   Brīva teksta rēķins
-   Pro forma rēķins

#### <a name="customer-invoice"></a>Debitora rēķins

Debitora rēķins ir rēķins, kuru organizācija izsniedz debitoram saistībā ar pārdošanu. Šāda veida debitora rēķinu jūs veidojat, pamatojoties uz pārdošanas pasūtījumu, kurā ir iekļauts virsraksts un viena vai vairākas krājumu vai pakalpojumu rindas. Debitora rēķins pabeidz pārdošanas pasūtījuma, pavadzīmes un pārdošanas rēķina ciklu.  

Varat grāmatot un drukāt atsevišķu debitora rēķinu, pamatojoties uz pārdošanas pasūtījumu vai pavadzīmi un datumu. Varat arī grāmatot un drukāt vairākus debitoru rēķinus kopā, pamatojoties uz pavadzīmēm un datumiem. Kad grāmatojat atsevišķu debitora rēķinu, izmantojot pārdošanas pasūtījumu, katra krājuma daudzums **Rēķinā iekļautais atlikums** tiek atjaunināts ar kopējiem rēķinā iekļautajiem daudzumiem no atlasītā pārdošanas pasūtījuma.  

Ja gan daudzums **Rēķinā iekļautais atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pārdošanas pasūtījumā ir 0 (nulle), tad pārdošanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**. Ja jebkura lauka daudzums nav 0, tad pārdošanas pasūtījuma statuss nemainās un jūs varat ievadīt papildu rēķinus. Ja gatavojaties grāmatot un drukāt vienu vai vairākus debitoru rēķinus, pamatojoties uz pavadzīmēm, jums ir jābūt iegrāmatotai vismaz vienai pavadzīmei par katru pārdošanas pasūtījumu. Debitora rēķins tiek pamatots ar pavadzīmēm un atspoguļo uzskaitītos daudzumus.  

Varat izveidot debitora rēķinu, kas ir balstīts uz pavadzīme rindas krājumiem, kuri ir piegādāti līdz šim datumam — arī tad, ja krājumi konkrētam pārdošanas pasūtījumam vēl nav nosūtīti. To varat izdarīt, piemēram, ja jūsu juridiskā persona izsniedz vienu rēķinu katram debitoram mēnesī, lai segtu visas piegādes, kuras attiecīgā mēneša laikā piegādājat. Katra pavadzīme ataino daļēju vai pilnīgu krājumu piegādi pēc pārdošanas pasūtījuma.  

Kad grāmatojat rēķinu, daudzums **Rēķina atlikums** katram krājumam tiek atjaunināts ar kopīgo piegādāto daudzumu no atlasītajām pavadzīmēm. Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pārdošanas pasūtījumā ir 0 (nulle), tad pārdošanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**. Ja šis daudzums nav 0, tad pārdošanas pasūtījuma statuss nemainās un jūs varat ievadīt papildu rēķinus. Krājumu transakcijas tiek atjauninātas ar rēķina numuru, un statuss pārdošanas pasūtījuma rindā mainās uz **Iekļauts rēķinā**.

#### <a name="free-text-invoice"></a>Brīva teksta rēķins

Brīva teksta rēķins ir rēķins, kas nav saistīts ar pārdošanas pasūtījumu. Tajā ir pasūtījuma rindas, kurās ir iekļauti virsgrāmatas konti, brīvā teksta apraksti un pārdošanas summas. Šāda veida rēķinā nevar ievadīt krājuma kodu, un jums ir jāievada atbilstošā pārdošanas nodokļa informācija. Galvenais konts pārdošanai ir norādīts katrā rēķinu rindā. Debitora bilance tiek grāmatota kopsavilkuma kontā no grāmatošanas metodes, kas tiek izmantota brīva teksta rēķinam.

#### <a name="pro-forma-invoice"></a>Pro forma rēķins

Pro forma rēķins ir rēķins, kas tiek sagatavots kā faktiskās rēķina summas novērtējums pirms rēķina grāmatošanas. Pro forma rēķinu var drukāt debitora rēķinam vai brīva teksta rēķinam.

### <a name="additional-resources"></a>Papildu resursi

#### <a name="blogs"></a>Emuāri

Apskats par pārdošanas procesu ir atrodams ziņā [Kā darbojas pārdošana programmā Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/05/15/how-sales-work-in-dynamics-365-for-finance-and-operations).

