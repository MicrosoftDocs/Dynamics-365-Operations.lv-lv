---
title: Maiņu un naudas kastes pārvaldība
description: Šajā tēmā ir paskaidrots, kā iestatīt un izmantot Commerce pārdošanas punkta (point of sale — POS) maiņas.
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 711f4f5549a478768f7f86a7001ac8a6cf9f4db6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985683"
---
# <a name="shift-and-cash-drawer-management"></a>Maiņu un naudas kastes pārvaldība

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt un izmantot Commerce pārdošanas punkta (point of sale — POS) maiņas.

Programmā Dynamics 365 Commerce termins *maiņa* attiecas uz POS transakciju datiem un darbībām, kas tiek veiktas noteiktā laika intervālā. Katrai maiņai paredzētā naudas summa tiek salīdzināta ar summu, kas tika aprēķināta un deklarēta.

Parasti maiņas tiek atvērtas darba dienas sākumā. Šajā brīdī lietotājs deklarē sākuma summu, kas ir pieejama naudas kastē. Pēc tam pārdošanas darbības tiek veiktas visas dienas garumā. Visbeidzot, dienas beigās naudas kastē esošā nauda tiek skaitīta un tiek deklarētas slēgšanas summas. Maiņa tiek slēgta un tiek ģenerēts Z pārskats. Z pārskatā norāda, vai ir izveidojies pārpalikums vai iztrūkums.

## <a name="typical-shift-scenarios"></a>Parastas maiņas scenāriji

Commerce nodrošina vairākas konfigurācijas opcijas un POS operācijas, lai atbalstītu dažādus dienas beigu POS biznesa procesus. Šajā sadaļā ir aprakstīti daži standarta maiņu scenāriji.

### <a name="fixed-till"></a>Fiksēts kases aparāts

Šis scenārijs tiek izmantots visbiežāk. To joprojām plaši izmanto. Maiņa “Fiksēts kases aparāts” — maiņa un kases aparāts ir saistīti ar noteiktu kases sistēmu. Tie netiek pārvietoti no vienas kases sistēmas uz citu. Maiņu “Fiksēts kases aparāts” var izmantot viens lietotājs vai koplietot vairāki lietotāji. Maiņām “Fiksēts kases aparāts” nav nepieciešama īpaša konfigurācija.

### <a name="floating-till"></a>Mainīgs kases aparāts

Maiņa “Mainīgs kases aparāts” — maiņu un naudas kasti var pārvietot no vienas kases sistēmas uz citu. Lai gan katrai kases sistēmas naudas kastei var būt tikai viena aktīva maiņa, maiņas var aizturēt un pēc tam vēlāk atsākt no citas kases sistēmas.

Piemēram, veikalam ir divas kases sistēmas. Katra kases sistēma tiek atvērta dienas sākumā, kad kasieris atver jaunu maiņu un norāda sākuma summu. Kad viens kasieris ir gatavs ņemt pārtraukumu, šis kasieris aptur savu maiņu un izņem naudas kasti no kases aparāta. Tagad šī kases sistēma ir pieejama citiem kasieriem. Cits kasieris var pierakstīties kases sistēmā un atvērt savu maiņu. Kad pirmā kasiera pārtraukums ir beidzies, šis kasieris var atsākt savu maiņu, kad kāda no citām kases sistēmām kļūst pieejama. Maiņām “Fiksēts kases aparāts” nav nepieciešama īpaša konfigurācija vai atļaujas.

### <a name="single-user"></a>Viens lietotājs

Daudzi mazumtirgotāji vienā maiņā pieļauj tikai tikai vienu lietotāju, lai nodrošinātu visaugstākā līmeņa atbildību par naudas kastē esošo skaidro naudu. Ja tikai vienam lietotājam ir atļauts izmantot kases aparātu, kas ir piesaistīts maiņai, šis lietotājs var būt vienpusēji atbildīgs par jebkādu iztrūkumu. Ja maiņu izmanto vairāki lietotāji, ir grūti noteikt, kurš no tiem pieļāva kļūdu vai kurš no tiem varētu mēģināt nozagt naudu no kases aparāta.

### <a name="multiple-users"></a>Vairāki lietotāji

Daži mazumtirgotāji ir gatavi upurēt atbildību, ko nodrošina viena lietotāja maiņas līmenis, un atļauj izmantot maiņu vairākiem lietotājiem. Šāda pieeja visbiežāk tiek izmantota, ja lietotāju ir vairāk nekā pieejamo kases sistēmu un nepieciešamais elastīgums un ātrums atsver iespējamos zaudējumus. Parasti veikala vadītājiem nav savas maiņas. Kad tas ir nepieciešams, viņi var izmantot jebkuru no kasieru maiņām. Lai pierakstītos un izmantotu maiņu, ko atvērta cits lietotājs, šim lietotājam ir jābūt POS atļaujai **Atļaut pieteikšanos vairākās maiņās**.

### <a name="shared-shift"></a>Koplietota maiņa

Maiņas "Koplietota maiņa" konfigurācija ļauj mazumtirgotājiem koplietot vienu maiņu vairākās kases sistēmās vai naudas kastēs un starp vairākiem lietotājiem. Koplietotai maiņai ir viena sākuma summa un beigu summa, kurā tiek apkopotas visu naudas kastu summas. Koplietotas maiņas ir īpaši piemērotas, ja tiek izmantotas mobilās ierīces. Šajā scenārijā atsevišķa naudas kaste nav rezervēta visām kases sistēmām. Tā vietā, visas kases sistēmas var koplietot vienu naudas kasti.

Lai veikalā izmantotu koplietotas maiņas, sadaļā **Retail un Commerce \> Kanāla iestatījumi \> POS iestatījumi \> POS profili \> Aparatūras profili \> Naudas kaste** naudas kastei jābūt konfigurētai kā “Koplietotas maiņas naudas kaste”. Turklāt lietotājiem ir jābūt vienai vai abām koplietojamas maiņas atļaujām (Atļaut pārvaldīt koplietoto maiņu un Atļaut lietot koplietoto maiņu).

> [!NOTE]
> Katrā veikalā vienlaicīgi var būt atvērta tikai viena koplietotā maiņa. Vienā veikala var lietot gan koplietotās maiņas, gan savrupās maiņas.

## <a name="shift-and-drawer-operations"></a>Naudas kastu un maiņu darbības

Var veikt dažādas darbības, lai mainītu maiņas stāvokli vai palielinātu vai samazinātu naudas kastē esošo naudas summu. Šajā sadaļā ir aprakstītas šīs maiņas darbības programmās Modern POS un Cloud POS.

### <a name="open-shift"></a>Atvērt maiņu

POS ir prasība, ka lietotājiem ir jābūt aktīvai, atvērtai maiņai, lai varētu veikt jebkādas darbības, kas var izraisīt finanšu transakciju, piemēram, pārdošanu, atgriešanu vai debitora pasūtījumu.

Kad lietotājs pierakstās POS, sistēma vispirms pārbauda, vai pašreizējā kases sistēmā šim lietotājam ir pieejama aktīva maiņa. Ja aktīva maiņa nav pieejama, lietotājs var izvēlēties atvērt jaunu maiņu, turpināt esošu maiņu vai pierakstīties naudas kastes neizmantošanas režīmā atkarībā no sistēmas konfigurācijas un lietotāja atļaujām.

### <a name="declare-start-amount"></a>Deklarēt sākuma summu

Šī darbība bieži vien ir pirmā, kas tiek veikta tikko atvērtā maiņā. Lai veiktu šo darbību, lietotāji norāda maiņas sākuma skaidras naudas summu naudas kastē. Šī darbība ir svarīga, jo šī sākuma summa tiek ņemta vērā pārpalikuma/iztrūkuma aprēķinā, kas tiek veikts maiņas slēgšanas procesā.

### <a name="float-entry"></a>Mainīgais ieraksts

*Mainīgās ievades* ir ar pārdošanu nesaistītas transakcijas, kas tiek veiktas aktīvas maiņas laikā un palielina naudas kastē esošo summu. Izplatīts mainīgās ievades piemērs ir papildu sīknaudas ievietošana naudas kastē, kad trūkst sīknaudas.

### <a name="tender-removal"></a>Norēķinu noņemšana

*Norēķinu noņemšanas* ir ar pārdošanu nesaistītas transakcijas, kas tiek veiktas aktīvas maiņas laikā, lai samazinātu naudas kastē esošo summu. Tās visbiežāk tiek lietotas kopā ar mainīgās ievades darbību citā maiņā. Piemēram, 1. kases sistēmā trūkst sīknaudas, tāpēc 2. kases sistēmas lietotājs veic norēķinu noņemšanu, lai samazinātu naudas kastē esošo summu. 1. kases sistēmas lietotājs veic mainīgo ievadi, lai palielinātu summu savā naudas kastē.

### <a name="suspend-shift"></a>Maiņas pārtraukšana

Lietotāji var pārtraukt savu aktīvo maiņu, lai atbrīvotu pašreizējo kases sistēmu citam lietotājam vai pārvietotu savu maiņu uz citu kases sistēmu (tādā gadījumā bieži šo procedūru dēvē par maiņu ar mainīgu kases aparātu).

Pēc maiņas pārtraukšanas nevar veikt nekādas jaunas transakcijas vai izmaiņas, līdz maiņa tiek atsākta.

### <a name="resume-shift"></a>Atsākt maiņu

Šī darbība sniedz lietotājam iespēju atsākt iepriekš apturētu maiņu kases sistēmā, kurā vēl nav aktīvas maiņas.

### <a name="tender-declaration"></a>Norēķinu uzskaite

Šī darbība tiek veikta, lai norādītu kopējo naudas summu, kas pašlaik ir pieejama naudas kastē. Lietotāji šo darbību parasti veic pirms savas maiņas slēgšanas. Norādītā summa tiek salīdzināta ar paredzēto summu maiņas beigās, lai aprēķinātu pārpalikuma/iztrūkuma summu.

### <a name="safe-drop"></a>Noguldījums seifā

Noguldījumus seifā var veikt jebkurā brīdī aktīvas maiņas laikā. Veicot šo darbību, nauda tiek izņemta no naudas kastes un pārvietota uz drošāku vietu, piemēram, uz seifu dibenistabā. Kopējā reģistrētā seifā noguldītā summa tiek ietverta maiņas kopsummā, taču nav jāietver norēķinu uzskaitē.

### <a name="bank-drop"></a>Noguldījums bankā

Tāpat kā noguldījumi seifā, arī noguldījumi bankā tiek veikti aktīvu maiņu laikā. Veicot šo darbību, no maiņas summas tiek noņemta nauda, lai to sagatavotu noguldīšanai bankā.

### <a name="blind-close-shift"></a>Diskrēti slēgt maiņu

*Diskrēti slēgtās maiņas* vairs nav aktīvas, bet vēl nav pilnībā slēgtas. Atšķirībā no pārtrauktām maiņām, diskrēti slēgtās maiņas nevar atsākt. Tomēr tādas darbības kā Deklarēt sākuma summu un Norēķinu uzskaite var veikt vēlāk, arī vai no citas kases sistēmas.

Diskrēti slēgtās maiņas bieži tiek izmantotas, lai atbrīvotu kases sistēmu jaunam lietotājam vai maiņai, iepriekš neveicot šīs maiņas pilnīgu uzskaiti, saskaņošanu un slēgšanu.

### <a name="close-shift"></a>Maiņas slēgšana

Veicot šo darbību, tiek aprēķinātas maiņas kopsummas un pārpalikuma/iztrūkuma summas un pēc tam tiek pabeigta aktīva vai diskrēti slēgta maiņa. Atkarībā no lietotāja atļaujas, Z pārskats tiek drukāts arī maiņai. Slēgtās maiņas nevar atsākt vai izmainīt.

### <a name="print-x"></a>Drukāt X

Šī darbība izveido un izdrukā X pārskatu par pašreizējo aktīvo maiņu.

### <a name="reprint-z"></a>Atkārtoti drukāt Z

Šī darbība atkārtoti drukā pēdējo Z pārskatu, ko sistēma ģenerēja, kad maiņa tika slēgta.

### <a name="manage-shifts"></a>Pārvaldīt maiņas

Šī darbība sniedz lietotājiem iespēju skatīt visas veikala aktīvās, apturētās un diskrēti slēgtās maiņas. Atkarībā no atļaujām lietotāji var veikt beigu slēgšanas darbības, piemēram, diskrēti slēgto maiņu norēķinu uzskaiti un maiņu slēgšanu. Šī darbība sniedz lietotājiem iesēju arī skatīt un dzēst nederīgās maiņas retos gadījumos, kad pēc bezsaistes un tiešsaistes režīmu pārslēgšanas maiņas stāvoklis ir kļuvis nederīgs. Šajās nederīgajās maiņās nav ietverta nekāda finanšu informācija vai transakciju dati, kas ir nepieciešami saskaņošanai.

## <a name="shift-and-drawer-permissions"></a>Naudas kastu un maiņu atļaujas

Tālāk minētās POS atļaujas ietekmē to, kādas darbības lietotājam ir atļautas dažādās situācijās un kādas nav atļautas.

- **Atļaut neskaidri slēgt maiņu**
- **Atļaut X pārskatu drukāšanu**
- **Atļaut Z pārskata drukāšanu**
- **Atļaut norēķinu uzskaiti**
- **Atļaut naudas plūsmas uzskaiti**
- **Atvērt naudas kasti nepārdodot**
- **Atļaut pieteikšanos vairākās maiņās** — ar šo atļauju lietotājs drīkst pierakstīties un izmantot maiņu, ko atvērta cits lietotājs. Lietotāji, kuriem nav šīs atļaujas, var pierakstīties un izmantot tikai savas atvērtās maiņas.
- **Atļaut pārvaldīt koplietoto maiņu** — lietotājiem jābūt šai atļaujai, lai atvērtu vai slēgtu koplietoto maiņu.
- **Atļaut lietot koplietoto maiņu** — lietotājiem jābūt šai atļaujai, lai pierakstītos un lietotu koplietoto maiņu.

## <a name="back-office-end-of-day-considerations"></a>Operāciju uzskaites daļas darbības dienas beigās

Veids, kā maiņu un naudas kastu dati tiek saskaņoti POS sistēmā un kā darbību dati tiek apkopoti izraksta aprēķināšanas laikā, ir atšķirīgs. Ir svarīgi izprast visas atšķirības. Atkarībā no sistēmas konfigurācijas un biznesa procesiem, POS maiņu dati (Z pārskatu) un operāciju uzskaites daļas aprēķinātā izraksta dati var atšķirties. Šī atšķirība nenozīmē, ka maiņu datus vai aprēķinātā izraksta dati nav pareizi, vai arī, ka radusies problēma ar datiem. Tas nozīmē, ka parametros, kas tika sniegti, varētu būt iekļautas vairāk vai mazāk darbības, vai arī darbības tika atšķirīgi apkopotas.

Lai gan katram mazumtirgotājam ir atšķirīgas biznesa prasības, ieteicams iestatīt sistēmu, kā aprakstīts tālāk, lai izvairītos no situācijām, kad rodas šāda veida atšķirības.

Dodieties uz **Retail un Commerce \> Kanāli \> Veikali \> Visi mazumtirdzniecības veikali \> Izraksts/slēgšana** un katram veikalam laukam **Izraksta metode** un **Slēguma metode** iestatiet **Maiņa**.

Šāds iestatījums nodrošinās, ka operāciju uzskaites daļas pārskati ietver tās pašas darbības, kas ietvertas POS maiņās, un dati tiek apkopoti pēc attiecīgās maiņas.

Plašāku informāciju par izrakstu un slēgšanas metodēm skatiet tēmā [Veikalu konfigurācijas mazumtirdzniecības izrakstiem](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).
