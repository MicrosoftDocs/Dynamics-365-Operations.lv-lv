---
title: "POS operācijas"
description: "Šajā tēmā ir sniegta detalizēta informācija par pārdošanas punkta (POS) operācijām programmā Microsoft Dynamics 365 for Retail. Tajā ir norādīts, kurās programmas vietās var izsaukt operācijas, un tas, vai šīs operācijas ir pieejamas bezsaistes režīmā."
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 02d777da3b97706f9e63478a1978ac9b230a591e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="pos-operations"></a>POS operācijas
Vairums darbību, ko lietotājs veic pārdošanas punktā (POS), tiek uzskatītas par operācijām. Operācijas var konfigurēt un pārvaldīt programmas Microsoft Dynamics 365 for Retail operāciju uzskaites daļā. Daudzas operācijas var pievienot pogām, kas ir ietvertas POS pogu režģī. Pēc tam lietotāji var atlasīt pogas, lai izsauktu attiecīgās operācijas un veiktu ar tām saistītās funkcijas. Citas operācijas ir ietvertas galvenajā POS programmā, un tās var izsaukt, izmantojot ekrānā redzamās pogas vai arī citu darbplūsmu vai procesu ietvaros.

Tālāk esošajā tabulā ir sniegta detalizēta informācija par Dynamics 365 for Retail paredzētajās programmās Retail Modern POS un Cloud POS pieejamajām operācijām. Tabulā ir arī norādīts, kurās programmas vietās var izsaukt operācijas, un tas, vai šīs operācijas ir pieejamas bezsaistes režīmā.

Dažas operācijas pašlaik nav pieejamas Dynamics 365 for Retail paredzētajā programmā Retail Modern POS vai Cloud POS. Dažas no šīm operācijām ir lokalizācijai raksturīgas operācijas, kam ir nepieciešami papildu paplašinājumi un konfigurācija. Dažas ir programmatūras Microsoft Dynamics AX 2012 līdzekļi, kas pašlaik netiek atbalstīti.

Tālāk norādītajās kolonnās ir norādītas vietas, kur var izsaukt operācijas.

- **Pogu režģis** — operāciju var piešķirt pogām, kas ir ietvertas POS pogu režģos, kuri ir daļa no POS ekrāna izkārtojuma.
- **Transakciju ekrāns** — operācijas var izsaukt, izmantojot POS pogu režģus, kas ir konfigurēti POS transakciju ekrānā.
- **Sveiciena ekrāns** — operācijas var izsaukt, izmantojot POS pogu režģus, kas ir konfigurēti POS sveiciena ekrānā.

| ID | Operācija | apraksts | Pogu režģis | Transakciju ekrāns | Sveiciena ekrāns | Pieejama bezsaistē | Lokalizācijai raksturīga |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktivizēt ierīci | Aktivizēt pašreizējo ierīci, atļaujot autentificētam lietotājam ievadīt savienojuma informāciju un piešķirt ierīces un kases sistēmas ID. | Nav | Nav | Nav | Nav | Nav |
| 134 | Pievienot piederību | Pievienojiet darījumam iepriekš atlasītu piederību. Atlasiet piederību lapā **Pogas rekvizīti**. | Jā | Jā | Nav | Jā | Nav |
| 135 | Pievienot piederību no saraksta | Pievienot transakcijai piederību, atlasot to sarakstā. | Jā | Jā | Jā | Jā | Nav |
| 643 | Pievienot kupona kodu | Pievienot kuponu, ievadot tā kodu POS sistēmā. | Jā | Jā | Nav | Jā | Nav |
| 117 | Pievienot lojalitātes karti | Aicināt lietotāju ievadīt lojalitātes kartes numuru, kas tiks pievienots pašreizējai transakcijai. | Jā | Jā | Nav | Jā | Nav |
| 136 | Pievienot sērijas numuru | Šī operācija sniedz lietotājam iespēju norādīt pašlaik atlasītās preces sērijas numuru. | Jā | Jā | Nav | Jā | Nav |
| 1214 | Pievienot piegādes adresi | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 519 | Pievienot dāvanu kartei | Pievienojiet naudas līdzekļus norādītajai dāvanu kartei. | Jā | Jā | Nav | Nav | Nav |
| 6000 | Atļaut izlaist fiskālo reģistrāciju | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 1212 | Noguldījums bankā | Ierakstiet naudas summu, kas tiek nosūtīta uz banku, kā arī citu informāciju, piemēram, bankas inkasācijas somas numuru. | Jā | Jā | Jā | Jā | Nav |
| 923 | Bankas kopsummas pārbaude | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 915 | Tukša operācija | Šī operācija nodrošina pielāgojamu pogu, ko programmatūras izstrādātājs var programmiski piesaistīt jebkurai specializētai operācijai, kas ir nepieciešama uzņēmumam. | Jā | Jā | Jā | Jā | Nav |
| 1053 | Diskrēti slēgt maiņu | Iestatīt pašreizējo maiņu kā diskrēti slēgtu un izrakstiet lietotāju. Diskrēti slēgta maiņa ir slēgta papildu transakcijām, taču joprojām ir atvērta naudas kastes operācijām, piemēram, norēķinu noņemšanai un norēķinu uzskaitei. | Jā | Jā | Jā | Nav | Nav |
| 310 | Aprēķināt kopsummu | Ja ir atlikts atlaides aprēķins, šī operācija sniedz iespēju uzsākt aprēķinu pašreizējai transakcijai. | Jā | Jā | Nav | Jā | Nav |
| 642 | Iznest visas preces | Iestatīt visām rindām piegādes veidu **Iznešana**. | Jā | Jā | Nav | Jā\* | Nav |
| 641 | Iznest atlasītas preces | Iestatīt atlasītajām rindām piegādes veidu **Iznešana**. | Jā | Jā | Nav | Jā\* | Nav |
| 1215 | Mainīt paroli | Šī operācija sniedz POS lietotājam iespēju mainīt savu paroli. | Jā | Jā | Jā | Nav | Nav |
| 123 | Mainīt mērvienību | Mainīt atlasītā rindas vienuma mērvienību. | Jā | Jā | Nav | Jā | Nav |
| 639 | Notīrīt noklusējuma darījuma pārdošanas pārstāvi | Noņemt no transakcijas komisijas pārdošanas grupu (pārdošanas pārst.). | Jā | Jā | Nav | Jā | Nav |
| 106 | Nodzēst daudzumu | Atiestatīt pašlaik atlasītās rindas daudzumu uz **1**. | Jā | Jā | Nav | Jā | Nav |
| 640 | Notīrīt rindā norādīto tirdzniecības pārstāvi | Noņemt no pašlaik atlasītās rindas komisijas pārdošanas grupu (pārdošanas pārst.). | Jā | Jā | Nav | Jā | Nav |
| 121 | Dzēst pārdevēju | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 1055 | Maiņas slēgšana | Slēgt pašreizējo maiņu, drukāt Z pārskatu un izrakstīt lietotāju no sistēmas. | Jā | Jā | Jā | Nav | Nav |
| 925 | Kopēt bankas čeku | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 620 | Izveidot debitora pasūtījumu | Pārveidot POS transakciju par debitora pasūtījumu. | Jā | Jā | Nav | Jā\* | Nav |
| 621 | Izveidot piedāvājumu | Pārveidot POS transakciju par pārdošanas piedāvājumu. | Jā | Jā | Nav | Jā\* | Nav |
| 636 | Izveidot mazumtirdzniecības transakciju | Šī operācija sniedz lietotājam iespēju izveidot standarta pārdošanas transakciju gadījumā, kad noklusējuma POS darbība ir debitora pasūtījumu izveide. | Jā | Jā | Nav | Jā | Nav |
| 600 | Debitors | Pievienot transakcijai norādīto debitoru. | Nav | Nav | Nav | Jā | Nav |
| 1100 | Debitora konta depozīts | Veiciet maksājumu debitora kontā. | Jā | Jā | Jā | Jā | Jā |
| 612 | Debitora pievienošana | Šī operācija sniedz lietotājam iespēju izveidot jaunu debitora ierakstu. | Jā | Jā | Jā | Jā† | Nav |
| 603 | Debitora dzēšana | Noņemt debitoru no pašreizējās transakcijas. | Jā | Jā | Nav | Jā | Nav |
| 602 | Debitora meklēšana | Šī operācija sniedz lietotājam iespēju meklēt debitora ierakstu, pārlūkojot debitoru meklēšanas lapu POS sistēmā. | Jā | Jā | Jā | Jā | Nav |
| 609 | Debitora darbības | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 917 | Datu bāzes savienojuma statuss | Šī operācija sniedz lietotājam iespēju skatīt pašreizējā savienojuma iestatījumus un pārslēgt tiešsaistes un bezsaistes režīmu. | Jā | Jā | Jā | Jā | Nav |
| 1200 | Deklarēt sākuma summu | Norādiet summu, kas ir naudas kastē, sākot dienu vai maiņu. | Jā | Jā | Jā | Jā | Nav |
| 132 | Depozīta ignorēšana | Ignorējiet debitoru pasūtījumiem noklusējuma depozītu. | Jā | Jā | Nav | Jā\* | Nav |
| 913 | Dizaina režīma atspējošana | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 912 | Dizaina režīma iespējošana | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 1217 | Izjaukt komplektus | Izjauciet komplektu tā komponentu precēs. | Jā | Jā | Jā | Jā | Nav |
| 624 | Rādīt atmaksas summas | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 513 | Rādīt kopsummu | Parādīt transakcijas bilanci debitora displejā. | Jā | Jā | Jā | Jā | Nav |
| 623 | Labot debitoru | Rediģēt pašreizējā debitora datus. | Jā | Jā | Nav | Nav | Nav |
| 614 | Rediģēt debitora pasūtījumu | Atsaukt atlasīto pasūtījumu, lai to varētu izmainīt POS sistēmā. | Nav | Nav | Nav | Nav | Nav |
| 615 | Rediģēt piedāvājumu | Atsaukt atlasīto piedāvājumu, lai to varētu izmainīt POS sistēmā. | Nav | Nav | Nav | Nav | Nav |
| 518 | Izdevumu konti | Reģistrējiet naudas summu, kas tiek izņemta no naudas kastes neparedzētu izdevumu segšanai. | Jā | Jā | Jā | Jā | Nav |
| 919 | Paplašinātā pieteikšanās | Piešķirt vai noņemt atļauju pierakstīties, skenējot svītrkodu vai novelkot karti. | Jā | Jā | Jā | Nav | Nav |
| 1201 | Mainīgais ieraksts | Šī operācija sniedz lietotājam iespēju pievienot papildu naudu pašreizējā naudas kastē vai maiņā. | Jā | Jā | Jā | Jā | Nav |
| 1218 | Veikt perifērijas ierīces piespiedu atbloķēšanu | Šī operācija tiek iekšēji izmantota sistēmā, lai atbloķētu POS perifērijas ierīces. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 520 | Dāvanu kartes bilance | Parādīt dāvanu kartes bilanci. | Jā | Jā | Nav | Nav | Nav |
| 708 | Deaktivizēt ierīci | Deaktivizēt pašreizējo ierīci, lai to nevarētu izmantot kā POS kases sistēmu. | Nav | Nav | Nav | Nav | Nav |
| 517 | Ieņēmumu konti | Reģistrējiet naudu, kas tiek ievietota naudas kastē citu iemeslu dēļ, kas nav pārdošana. | Jā | Jā | Jā | Jā | Nav |
| 801 | Krājumu pārlūkošana | Uzmeklēt pieejamos, pasūtāmos un solīšanai pieejamos (ATP) daudzumus pašreizējā veikalā un citās pieejamajās vietās. | Jā | Jā | Jā | Nav | Nav |
| 122 | Rēķina komentārs | Šī operācija sniedz lietotājam iespēju ievadīt komentāru par pašreizējo transakciju. | Jā | Jā | Nav | Jā | Nav |
| 511 | Izsniegt kredītrēķinu | Izsniegt kredītrēķinu, lai atmaksas vietā izsniegtu kuponu. | Jā | Jā | Nav | Nav | Nav |
| 512 | Izsniegt dāvanu karti | Izsniegt jaunu dāvanu karti par norādīto summu. | Jā | Jā | Nav | Nav | Nav |
| 625 | Izsniegt lojalitātes programmas karti | Izsniegt debitoram lojalitātes programmas karti, lai šis debitors varētu piedalīties veikala lojalitātes programmā. | Jā | Jā | Jā | Nav | Nav |
| 300 | Rindas atlaides summa | Ievadiet darījuma dokumenta rindas atlaides summu. Šī operācija tiek lietota tikai precēm, kam var lietot atlaidi, un tikai ar noteiktiem atlaides ierobežojumiem. | Jā | Jā | Nav | Jā | Nav |
| 301 | Rindas atlaide procentos | Ievadiet darījumā izmantotās dokumenta rindas atlaidi procentos. Šī operācija tiek lietota tikai precēm, kam var lietot atlaidi, un tikai ar noteiktiem atlaides ierobežojumiem. | Jā | Jā | Nav | Jā | Nav |
| 703 | Bloķēt reģistru | Bloķēt pašreizējo kases sistēmu, lai to nevarētu izmantot, taču neizrakstīt pašreizējo lietotāju. | Nav | Nav | Nav | Jā | Nav |
| 701 | Atteikties | Izrakstīt pašreizējo lietotāju no kases sistēmas. | Jā | Jā | Jā | Jā | Nav |
| 521 | Lojalitātes programmu karšu punktu bilance | Parādīt norādītās lojalitātes programmas kartes punktu bilanci. | Jā | Jā | Nav | Nav | Nav |
| 914 | Minimizēt POS logu | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 1000 | Atvērt naudas kasti | Veikt operāciju bez pārdošanas un atvērt pašlaik atlasīto naudas kasti. | Jā | Jā | Jā | Jā | Nav |
| 129 | Ignorēt preces rindas nodokli | Pārlabot nodokli par atlasīto rindas vienumu un izmantot citu norādīto nodokli. | Jā | Jā | Nav | Jā | Nav |
| 130 | Ignorēt sarakstā esošu preces rindas nodokli | Pārlabot nodokli par atlasīto rindas vienumu un izmantot nodokli, ko lietotājs atlasa sarakstā. | Jā | Jā | Nav | Jā | Nav |
| 127 | Ignorēt darbības nodokli | Pārlabot nodokli par transakciju un izmantot citu norādīto nodokli. | Jā | Jā | Nav | Jā | Nav |
| 128 | Ignorēt sarakstā esošu darbības nodokli | Pārlabot nodokli par transakciju un izmantot nodokli, ko lietotājs atlasa sarakstā. | Jā | Jā | Nav | Jā | Nav |
| 131 | Pavadzīme | Izveidot atlasītā pasūtījuma pavadzīmi. | Nav | Nav | Nav | Nav | Nav |
| 710 | Savienot aparatūras staciju pārī | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 201 | Maksājums ar karti | Kā maksājuma veidu pieņemt karti, piemēram, kredītkarti vai debetkarti. | Jā | Jā | Nav | Jā | Nav |
| 200 | Maksājums skaidrā naudā | Kā maksājuma veidu pieņemiet skaidru naudu. | Jā | Jā | Nav | Jā | Nav |
| 206 | Ātrais maksājums skaidrā naudā | Pabeigt transakciju ar vienu pieskārienu un pieņemt maksājamo summu skaidrā naudā (bez atlikuma). | Jā | Jā | Nav | Jā | Nav |
| 204 | Maksājums ar čeku | Pieņemiet čeku kā maksājuma veidu. | Jā | Jā | Nav | Jā | Nav |
| 213 | Maksājums ar kredītrēķinu | Pieņemt veikalā izsniegtu kredītrēķinu (kuponu). | Jā | Jā | Nav | Nav | Nav |
| 203 | Maksājums valūtā | Pieņemiet maksājumu dažādās valūtās. | Jā | Jā | Nav | Jā | Nav |
| 202 | Maksājums, izmantojot debitora kontu | Ņemt maksu par transakciju no debitora konta. Šī maksāšanas metode nav derīga debitoru pasūtījumu depozītiem. | Jā | Jā | Nav | Nav | Nav |
| 214 | Maksājums ar dāvanu karti | Pieņemt veikalā izsniegtu dāvanu karti. | Jā | Jā | Nav | Nav | Nav |
| 207 | Maksāt ar lojalitātes programmas karti | Kā maksāšanas metodi pieņemt lojalitātes karti un izpirkt punktus apmaiņā pret piemērotajām precēm. | Jā | Jā | Nav | Nav | Nav |
| 634 | Maksājumu vēsture | Parādīt debitora maksājumu vēsturi par pašreizējo debitora pasūtījumu. | Jā | Jā | Nav | Nav | Nav |
| 803 | Izdošana un saņemšana | Atvērt lapu **Izdošana un saņemšana**, kur varat atlasīt pasūtījumus, kas ir jāizdod vai jāsaņem veikalā. | Jā | Jā | Jā | Nav | Nav |
| 632 | Saņemt visas preces | Iestatīt visām rindām izpildes metodi **Saņemšana veikalā**. | Jā | Jā | Nav | Jā\* | Nav |
| 631 | Saņemt atlasītās preces | Iestatīt atlasītajām rindām izpildes metodi **Saņemšana veikalā**. | Jā | Jā | Nav | Jā\* | Nav |
| 400 | Uznirstošā izvēlne | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 101 | Cenas pārbaude | Šī operācija sniedz lietotājam iespēju uzmeklēt norādītās preces cenu. | Jā | Jā | Jā | Jā | Nav |
| 104 | Cenas ignorēšana | Pārlabot preces cenu, ja šai precei ir iestatīta cenas pārlabošana. | Jā | Jā | Nav | Jā | Nav |
| 1058 | Drukāt finanšu X | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 1059 | Drukāt finanšu Z | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 927 | Drukāt krājuma etiķeti | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 926 | Drukāt plaukta etiķeti | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 1056 | Drukāt X | Drukāt X pārskatu par pašreizējo maiņu. | Jā | Jā | Jā | Nav | Nav |
| 103 | Preces piezīme | Pievienojiet komentāru darījumā atlasītajai dokumenta rindai. | Jā | Jā | Nav | Jā | Nav |
| 100 | Preces pārdošana | Pievienot transakcijai norādīto preci. | Jā | Jā | Jā | Jā | Nav |
| 108 | Preču meklēšana | Šī operācija sniedz lietotājam iespēju meklēt preci, pārlūkojot preču meklēšanas lapu POS sistēmā. | Jā | Jā | Jā | Jā | Nav |
| 633 | Piedāvājuma beigu datums | Šī operācija sniedz lietotājam iespēju skatīt vai izmainīt pārdošanas piedāvājuma beigu datumu. | Jā | Jā | Nav | Jā\* | Nav |
| 627 | Pārrēķināt | Pārrēķināt visas debitora pasūtījuma rindas un nodokļus, pamatojoties uz pašreizējo konfigurāciju. | Jā | Jā | Nav | Jā\* | Nav |
| 515 | Atsaukt pasūtījumu | Šī operācija sniedz lietotājam iespēju meklēt un atsaukt debitoru pasūtījumus un pārdošanas piedāvājumus. | Jā | Jā | Jā | Nav | Nav |
| 504 | Atsaukt darījumu | Šī operācija sniedz lietotājam iespēju atsaukt pašreizējā veikalā iepriekš aizturētu transakciju. | Jā | Jā | Nav | Jā‡ | Nav |
| 305 | Izpirkt lojalitātes programmas punktus | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 635 | Atmaksāt piegādes izmaksas | Šī operācija sniedz lietotājam iespēju atmaksāt atcelta pasūtījuma piegādes izmaksas. | Nav | Nav | Nav | Nav | Nav |
| 644 | Noņemt kupona kodu | Aicināt lietotāju noņemt kuponus, atlasot tos ar transakciju pašlaik saistīto kuponu sarakstā. | Jā | Jā | Nav | Jā | Nav |
| 1057 | Atkārtoti drukāt Z | Atkārtoti drukāt Z pārskatu par iepriekšējo maiņu vai atlasītu maiņu. | Jā | Jā | Jā | Nav | Nav |
| 1216 | Jaunas paroles ievadīšana | Šī operācija sniedz lietotājam iespēju atiestatīt cita darbinieka paroli, izmantojot pagaidu paroli, ja šim lietotājam ir paroles atiestatīšanas atļauja. | Jā | Jā | Jā | Nav | Nav |
| 109 | Atgriezt preci | Veiciet atsevišķu preču atgriešanu. Nākamā skenētā prece tiek parādīta kā atgriezta prece ar negatīvu daudzumu un cenu. | Jā | Jā | Nav | Jā | Nav |
| 114 | Atgriezt darījumu | Atsaukt iepriekšējo transakciju pēc tās kvīts numura, lai atgrieztu visas preces vai daļu no tām. | Jā | Jā | Jā | Jā§ | Nav |
| 1211 | Noguldījums seifā | Veiciet noguldījumu seifā, lai pārvietotu naudu no kases sistēmas uz seifu. | Jā | Jā | Jā | Jā | Nav |
| 516 | Pārdošanas rēķins | Šī operācija sniedz debitoram iespēju veikt maksājumus, lai apmaksātu atlasīto pārdošanas rēķinu. | Jā | Jā | Nav | Nav | Nav |
| 502 | Pārdevējs | Šī operācija sniedz lietotājam iespēju iestatīt debitoru pasūtījumu pārdošanas pasūtījuma parametra **Pārdošanas uzņēmējs** vērtību POS sistēmā. | Jā | Jā | Nav | Jā\* | Nav |
| 2000 | Grafika pārvaldība | Šī operācija sniedz lietotājam iespēju izveidot, izmainīt vai skatīt darbinieku grafikus. | Jā | Jā | Jā | Nav | Nav |
| 2001 | Grafika pieprasījumi | Šī operācija sniedz lietotājam iespēju pieprasīt brīvo laiku, apmainīt maiņas vai piedāvāt maiņas citiem darbiniekiem. | Jā | Jā | Jā | Nav | Nav |
| 622 | Meklēšana | Šī operācija sniedz lietotājiem iespēju iepriekš konfigurēt POS pogas, lai veiktu meklēšanu pēc krājuma, debitora vai kategorijas. | Jā | Jā | Jā | Jā | Nav |
| 1213 | Meklēt piegādes adresi | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 709 | Atlasīt aparatūras staciju | Šī operācija sniedz lietotājam iespēju atlasīt aparatūras staciju pieejamo aparatūras staciju sarakstā. | Jā | Jā | Jā | Jā | Nav |
| 637 | Iestatīt noklusējuma darījuma pārdošanas pārstāvi | Šī operācija sniedz lietotājam iespēju atlasīt vienu no derīgajām komisijas pārdošanas grupām (pārdošanas pārst.) kā vēlāk pievienoto rindu noklusējuma pārdošanas pārstāvi. | Jā | Jā | Nav | Jā | Nav |
| 105 | Iestatīt daudzumu | Mainiet darījuma dokumenta rindas daudzumu. | Jā | Jā | Nav | Jā | Nav |
| 638 | Iestatīt rindas pārdošanas pārstāvi | Šī operācija sniedz lietotājam iespēju atlasīt vienu no derīgajām komisijas pārdošanas grupām (pārdošanas pārst.) pašlaik atlasītajai rindai. | Jā | Jā | Nav | Jā | Nav |
| 630 | Nosūtīt visas preces | Iestatīt visiem rindu vienumiem izpildes režīmu **Nosūtīšana**. | Jā | Jā | Nav | Jā\* | Nav |
| 629 | Nosūtīt atlasītās preces | Iestatīt atlasītajām rindām izpildes režīmu **Nosūtīšana**. | Jā | Jā | Nav | Jā\* | Nav |
| 918 | Rādīt neskaidri slēgtās maiņas | Parādīt visu diskrēti slēgto maiņu sarakstu. | Jā | Jā | Jā | Nav | Nav |
| 115 | Rādīt žurnālu | Parādīt veikala žurnālu. Varat skatīt transakcijas, atkārtoti izdrukāt kvītis un dāvanu kvītis un atsaukt transakcijas atgriešanai. | Jā | Jā | Jā | Jā\*\* | Nav |
| 802 | Krājumu uzskaite | Šī operācija sniedz lietotājam iespēju izveidot vai izmainīt fizisko krājumu vai cikla inventarizācijas uzskaites žurnālus. | Jā | Jā | Jā | Nav | Nav |
| 401 | Apakšizvēlne | Šī operācija nodrošina lietotāja novirzīšanu uz citu saistīto pogu režģi. | Jā | Jā | Jā | Jā | Nav |
| 1054 | Maiņas pārtraukšana | Aizturēt pašreizējo maiņu, lai pašreizējā kases sistēmā varētu aktivizēt jaunu vai citu maiņu. | Jā | Jā | Jā | Nav | Nav |
| 503 | Darījuma aizturēšana | Aizturēt pašreizējo pārdošanas transakciju, lai to vēlāk varētu atsaukt veikalā. | Jā | Jā | Nav | Jā‡ | Nav |
| 1004 | Uzdevumu reģistrētājs | Atvērt uzdevumu reģistrētāju, lai reģistrētu procedūras darbības POS sistēmā. | Nav | Nav | Nav | Jā | Nav |
| 1052 | Norēķinu uzskaite | Šī operācija sniedz lietotājam iespēju norādīt naudas kastē esošo naudas summu atbilstoši katrai uzskaitītajai maksāšanas metodei. | Jā | Jā | Jā | Jā | Nav |
| 1210 | Norēķinu noņemšana | Šī operācija sniedz lietotājam iespēju izņemt naudu no pašreizējās naudas kastes vai maiņas. | Jā | Jā | Jā | Jā | Nav |
| 920 | Darba laika uzskaite | Šī operācija sniedz lietotājiem iespēju reģistrēt darba maiņu un pārtraukumu sākumu un beigas. | Jā | Jā | Jā | Nav | Nav |
| 302 | Kopējā atlaides summa | Ievadīt transakcijas atlaides summu. Šī operācija attiecas tikai uz tām precēm, kam var lietot atlaidi, un tikai ar noteiktiem atlaides ierobežojumiem. | Jā | Jā | Nav | Jā | Nav |
| 303 | Kopējie atlaides procenti | Ievadīt transakcijas atlaides procentus. Šī operācija attiecas tikai uz tām precēm, kam var lietot atlaidi, un tikai ar noteiktiem atlaides ierobežojumiem. | Jā | Jā | Nav | Jā | Nav |
| 501 | Darbības apraksts | Pievienot komentāru pašreizējai transakcijai. | Jā | Jā | Nav | Jā | Nav |
| 922 | Skatiet detalizētu informāciju par preci | Atvērt pašlaik atlasītā rindas vienuma lapu Detalizēta informācija par preci. | Jā | Jā | Nav | Jā | Nav |
| 1003 | Skatīt pārskatus | Parādīt pašreizējam lietotājam konfigurētos pārskatus. | Jā | Jā | Jā | Nav | Nav |
| 921 | Skatiet darba laika uzskaites ierakstus | Parādīt visu veikala darbinieku laika uzskaites ierakstus. | Jā | Jā | Jā | Nav | Nav |
| 211 | Anulēt maksājumu | Anulēt transakcijā pašlaik atlasīto maksājuma rindu. | Jā | Jā | Nav | Jā | Nav |
| 102 | Anulēt preci | Anulēt transakcijā pašlaik atlasīto rindas vienumu. | Jā | Jā | Nav | Jā | Nav |
| 500 | Anulēt darījumu | Anulēt pašreizējo transakciju. | Jā | Jā | Nav | Jā | Nav |
| 916 | Windows darbplūsmas pamats | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav |
| 924 | X pārskats bankas kartēm | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |

\* Operācija ir pieejama bezsaistes režīmā tikai tad, ja tiek izveidots debitora pasūtījums vai pārdošanas piedāvājums un ja POS funkcionalitātes profilā ir konfigurēta debitoru rēķinu un pārdošanas piedāvājumu izveide bezsaistes režīmā. Operāciju nevar veikt, ja pasūtījumi tiek veidoti, izmantojot reāllaika pakalpojumu, vai ja pasūtījumi tiek atsaukti vai rediģēti.

† Operāciju var veikt bezsaistes režīmā tikai tad, ja POS funkcionalitātes profils ir konfigurēts tā, lai atļautu debitoru izveidi bezsaistes režīmā.

‡ Ja POS ir bezsaistē, aizturētās transakcijas var atsaukt tikai no pašreizējās kases sistēmas bezsaistes datu bāzes. Lietotāji nevar aizturēt un atsaukt transakcijas dažādās kases sistēmās.

§ Ja POS ir bezsaistē, atgriešanai var atsaukt tikai pašreizējā bezsaistes datu bāzē saglabātās transakcijas.

\*\* Ja POS ir bezsaistē, žurnālā tiek rādītas tikai pašreizējā bezsaistes kanāla datu bāzē saglabātās transakcijas.

