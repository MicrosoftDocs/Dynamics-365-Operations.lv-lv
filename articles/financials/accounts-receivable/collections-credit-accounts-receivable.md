---
title: "Debitoru parādu kredīts un iekasēšana"
description: "Debitoru parādu iekasēšanas informācija tiek pārvaldīta vienā centrālajā skatā, izmantojot programmas Microsoft Dynamics 365 for Finance and Operations lapu Iekasēšana. Kredīta un iekasēšanas vadītāji šo centrālo skatu var izmantot, lai pārvaldītu iekasēšanu. Iekasēšanas aģenti var uzsākt iekasēšanas procesu, izmantojot debitoru sarakstus, kas tiek ģenerēti, izmantojot iepriekš definētus iekasēšanas kritērijus, vai lapu Debitori."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 23fc1a160cf25255a1677ca0e501c374746b6e34
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="credit-and-collections-in-accounts-receivable"></a>Debitoru parādu kredīts un iekasēšana

[!include[banner](../includes/banner.md)]


Debitoru parādu iekasēšanas informācija tiek centralizēti pārvaldīta vienā skatā, izmantojot Dynamics 365 for Finance and Operations lapu Iekasēšana. Kreditēšanas un iekasēšanas transakciju vadītāji šo centrālo skatu var izmantot, lai pārvaldītu iekasēšanas transakcijas. Iekasēšanas aģenti var uzsākt iekasēšanas procesu, izmantojot debitoru sarakstus, kas tiek ģenerēti, izmantojot iepriekš definētus iekasēšanas kritērijus, vai lapu Debitori.

Pirms sākat iekasēšanas darbību iestatīšanu vai apstrādi, jums ir jāsaprot tālāk norādītās koncepcijas.
-   Debitora vecumstruktūru momentuzņēmumi satur vecu bilances informāciju par noteiktu laika periodu
-   Iekasēšanas debitoru kopa palīdz organizēt darbu
-   Iekasēšanas aģentiem var būt savas debitoru kopas
-   Sarakstu lapās ir sakārtoti iekasēšanas debitori, aktivitātes un gadījumi
-   Visa iekasēšanas informācija par noteiktu debitoru ir pieejama vienā lapā, un šajā lapā varat veikt darbības
-   Procentus un maksas var atcelt, atjaunot vai anulēt, veicot vienu darbību
-   Norakstīšanas transakcijas var izveidot, veicot vienu darbību
-   Nepietiekamu naudas līdzekļu (NSF) maksājumus var apstrādāt, veicot vienu darbību

Tālāk esošajās sadaļās ir aprakstīta katra koncepcija.

## <a name="customer-aging-snapshots"></a>Debitora vecumstruktūru momentuzņēmumi
Vecumstruktūras momentuzņēmums satur vecas debitora bilances par noteiktu laika periodu. Šī informācija tiek rādīta saraksta lapā Vecas bilances un lapā Iekasēšana. Pirms varat skatīt informāciju iekasēšanas sarakstu lapās, ir jāizveido vecumstruktūras momentuzņēmums. 

Katra debitora vecumstruktūras momentuzņēmums satur vecumstruktūras momentuzņēmuma virsrakstu un datu ierakstus, kas atbilst katram vecumstruktūras periodam vecumstruktūras perioda definīcijā. 

Vecumstruktūras momentuzņēmuma virsraksts satur debitora konta kopsummu apmaksai, kredīta limitu, pavadzīmes summu, pārdošanas pasūtījuma summu, apstrīdēto transakciju skaitu un apstrīdēto transakciju kopsummu. Šo summu aprēķinā tiek ietvertas visas debitora transakcijas. Kopsumma apmaksai, kredīta limits, pavadzīmes summa un pārdošanas pasūtījuma summa tiek rādīti papildinformācijas rūtī Kredīta informācija lapā Iekasēšana. 

Katram vecumstruktūras periodam vecumstruktūras perioda definīcijā tiek izveidots vecumstruktūras momentuzņēmuma datu ieraksts. Katrs vecumstruktūras momentuzņēmuma datu ieraksts satur vecumstruktūras perioda ID un to transakciju kopsummu, kuru datumi ietilpst vecumstruktūras periodā. Transakcijas tiek piešķirtas vecumstruktūras periodam, piemēram, 30 dienas pēc izpildes termiņa. Datums ir relatīvs attiecībā pret vecumstruktūru datumā, kas ir norādīts, izveidojot vecumstruktūras momentuzņēmumu. Šī informācija tiek rādīta saraksta lapā Vecas bilances un lapas Iekasēšana papildinformācijas rūtī Vecas bilances.

## <a name="collections-customer-pools"></a>Iekasēšanas debitoru kopas
Debitoru kopas ir vaicājumi, ar ko tiek definēta debitoru ierakstu grupa, ko var skatīt un pārvaldīt iekasēšanas vai vecumstruktūru procesu ietvaros. Izmantojiet debitoru kopas, lai filtrētu informāciju sarakstu lapās Vecas bilances, Kolekciju aktivitātes un Atgādinājumu gadījumi. Varat arī izmantot debitoru kopas, lai filtrētu debitoru kontus, kas tiek iekļauti vecumstruktūru momentuzņēmumu izveides laikā.

## <a name="collections-agents"></a>Iekasēšanas aģenti
Pēc noklusējuma Microsoft Dynamics 365 for Finance and Operations lietotāji var skatīt visu debitora informāciju iekasēšanas sarakstu lapās. Varat izmantot iekasēšanas aģentu ierakstus, lai noteiktu debitoru kopas, kas ir pieejamas informācijas filtrēšanai iekasēšanas sarakstu lapās un lapā Iekasēšana. 

Iekasēšanas aģents ir persona, kas strādā ar debitoriem, lai nodrošinātu, ka maksājumi tiek saņemti savlaicīgi. Programmatūrā Dynamics 365 for Finance and Operations iekasēšanas aģenti ir darbinieki, kuri ir piešķirti lietotājiem lapā Lietotāja iestatījumi.

## <a name="collections-list-pages"></a>Iekasēšanas sarakstu lapas
Tālāk ir norādītas sarakstu lapas, kas palīdz sakārtot iekasēšanas informāciju.
-   Vecas bilances — saraksta lapas kolonnās tiek parādītas debitoru bilances un vecās summas pēc vecumstruktūras perioda. Šī informācija tiek uzglabāta vecumstruktūras momentuzņēmumā. Vecumstruktūras periodus nosaka vecumstruktūras perioda definīcija, kas tiek lietota. Vecumstruktūras perioda definīcija ir aizgūta no debitoru kopas, ja tāda ir norādīta kopas vaicājumam. Ja kopai nav vecumstruktūras perioda definīcijas, tiek izmantota noklusējuma vecumstruktūras perioda definīcija, kas ir norādīta lapā Debitoru parādu parametri. Ja nav norādīta noklusējuma vecumstruktūras perioda definīcija, tiek izmantota pirmā vecumstruktūras perioda definīcija lapā Vecumstruktūras perioda definīcijas.
-   Kolekciju aktivitātes — saraksta lapas kolonnās tiek rādītas aktivitātes, kas ir norādītas kā iekasēšanas aktivitātes. Šīs aktivitātes tiek izveidotas, izmantojot lapu Iekasēšana. Lai izsekotu darbam, ko veicat saistībā ar iekasēšanu, izmantojiet aktivitātes.
-   Atgādinājumu gadījumi — saraksta lapas kolonnās tiek rādīta informācija par gadījumiem, kuru gadījuma kategorijas gadījuma veids ir Iekasēšana.

> [!NOTE]
> Pirms varat skatīt informāciju šajās sarakstu lapās, ir jāizveido vecumstruktūras momentuzņēmums. Tiek rādīta informācija tikai par tiem debitoriem, kam ir izveidots vecumstruktūras momentuzņēmums. Saraksta lapā rādītos ierakstus var papildus filtrēt tālāk norādītajā veidā.
<li>Pēc noklusējuma Dynamics 365 for Finance and Operations lietotājs var piekļūt visiem debitoriem, kuriem ir vecumstruktūras momentuzņēmums.</li>
<li>Ja pastāv debitoru kopas, lietotājam ir jābūt iestatītam kā iekasēšanas aģentam, lai viņš varētu izmantot kopas informācijas filtrēšanai iekasēšanas sarakstu lapās. Ir pieejama informācija tikai par debitoriem, kuri ir ietverti atlasītajā debitoru kopā.</li>
<li>Ja lietotājs ir iestatīts kā iekasēšanas aģents, saraksta lapā ir pieejamas tikai tās kopas, kas ir atlasītas konkrētajam iekasēšanas aģentam. Ja iekasēšanas aģentam lapā Iekasēšanas aģents ir atlasīta slēdzis Ļaut aģentam skatīt visas debitoru kopas, šim aģentam ir pieejamas visas kopas.</li>


## <a name="collections-page"></a>Lapa Iekasēšana
Izmantojiet lapu Iekasēšana, lai skatītu, pārvaldītu un izmantoto debitora iekasēšanas informāciju, aktivitātes un gadījumus. 

Augšējā rūtī tiek rādīti atlasītā debitora gadījumi. Vidējā rūtī tiek rādītas debitora transakcijas. Apakšējā rūtī tiek rādītas debitora aktivitātes. Varat izveidot iekasēšanas gadījumus, lai izsekotu iekasēšanas informāciju par vienu vai vairākām transakcijām un aktivitātēm. Augšējā un apakšējā rūtī redzamo informāciju var filtrēt pēc gadījuma. 

Papildinformācijas rūtī tiek rādītas atlasītā debitora vecās bilances un kredīta limita informācija. Šī informācija tiek glabāta vecumstruktūras momentuzņēmumā. Ja nepieciešams, var atjaunināt vecumstruktūras momentuzņēmumu, izmantojot pašreizējo informāciju. 

Darbību rūts satur pogas, kas ļauj skatīt saistīto informāciju par atlasīto debitoru, gadījumu, transakciju vai aktivitāti. Varat arī veikt vispārīgas darbības, piemēram, mainīt transakcijas iekasēšanas statusu, sūtīt e-pasta ziņojumus, izmantojot integrāciju ar jūsu e-pasta pakalpojumu sniedzējs, izmaksāt debitoriem kompensāciju, apstrādāt NSF maksājumus un norakstīt neiekasējamās bilances.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a>Procentu vai maksu atcelšana, atjaunošana vai anulēšana
Var atcelt, atjaunot vai anulēt veselus procentu paziņojumus vai procentu paziņojumos ietvertas maksas un transakciju procentus. Varat to izdarīt saraksta lapas Visi debitori darbību rūts cilnē Apkopot, noklikšķinot uz Procentu paziņojums, Darbību procenti vai Maksa. 

Šīs korekcijas ietekmē tikai procentu paziņojumus un tajos ietvertos procentus un maksas. Veiciet sadaļā “Norakstīšanas transakciju izveide, veicot vienu darbību” aprakstītās darbības, lai norakstītu visas maksas, kuras debitors nav apmaksājis.

Plašāku informāciju skatiet šeit: [Procentu koda ar diapazonu izveidošana](tasks/create-interest-code-range.md) un šeit: [Procentu apstrāde](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Izveidot norakstīšanas transakcijas
Varat norakstīt sliktos parādus, noklikšķinot uz Norakstīt veidlapā Iekasēšana un sarakstu lapās Vecas bilances, Debitori un Atvērtie debitoru rēķini. 

Norakstot debitora transakcijas, visas debitora transakcijas tiek automātiski iezīmētas segšanai. Norakstītā summa ir atkarīga no iezīmēto transakciju neto summas. Vispārējā žurnālā tiek izveidots norakstīšanas darījums, un tas var ietvert ne vairāk kā trīs veidu žurnāla rindas.

-   Pirmā veida žurnāla rinda satur debitora norakstīšanas ierakstu. Ja iezīmētās transakcijas satur vairākas valūtas koda, dimensijas un grāmatošanas profila kombinācijas, katrai kombinācijai tiek izveidota atsevišķa žurnāla rinda.
-   Otrā veida žurnāla rinda satur virsgrāmatas norakstīšanas ierakstu. Ja iezīmētās transakcijas satur vairākas valūtas koda, dimensijas un grāmatošanas profila kombinācijas, katrai kombinācijai tiek izveidota atsevišķa žurnāla rinda.
-   Trešā veida žurnāla rinda satur virsgrāmatas norakstīšanas informāciju par PVN. Šī žurnāla rinda tiek izveidota tikai tad, ja lapā Debitoru parādu parametri ir atlasīts slēdzis Atdalīt PVN. Ja iezīmētās transakcijas satur vairākas maksājamā PVN konta, dimensijas un PVN koda kombinācijas, katrai kombinācijai tiek izveidota atsevišķa žurnāla rinda.

Norakstīšanas transakcija tiek izveidota transakcijas valūtā.

Plašāku informāciju skatiet šeit: [Debitora norakstīšanas žurnāla izveide](tasks/create-write-off-journal-customer.md)

<a name="process-not-sufficient-funds-nsf-payments"></a>Nepietiekamu naudas līdzekļu (NSF) maksājumi 
--------------------------------------------

Varat apstrādāt NSF maksājumus, lapā Iekasēšana noklikšķinot uz NSF maksājums. Noklikšķinot uz šīs pogas, maksājums tiek atcelts. Ja debitoram ir jāmaksā NSF maksa, maksājumu žurnālā tiek izveidota maksas transakcija. Maksas summa balstās uz automātisko maksu iestatījumiem. Automātiskās maksas, kas attiecas uz NSF maksājumiem, ir atkarīgas no maksu grupas, kas ietekmētajam bankas kontam ir atlasīta lapā Bankas konti.






