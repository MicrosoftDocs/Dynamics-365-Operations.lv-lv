---
title: Tiešsaistes un bezsaistes pārdošanas punkta (POS) operācijas
description: Šajā tēmā ir sniegta detalizēta informācija par pārdošanas punkta (POS) operācijām programmā Dynamics 365 Commerce. Tajā ir norādīts, kurās programmas vietās var izsaukt operācijas, un tas, vai šīs operācijas ir pieejamas bezsaistes režīmā.
author: jblucher
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6b02f94bb2217729f35f0593fe99807273608811
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027652"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Tiešsaistes un bezsaistes pārdošanas punkta (POS) operācijas

[!include [banner](includes/banner.md)]

Vairums darbību, ko lietotājs veic pārdošanas punktā (POS), tiek uzskatītas par operācijām. Operācijas tiek konfigurēts un pārvaldītas Dynamics 365 Commerce operāciju uzskaites daļā. Daudzas operācijas var pievienot pogām, kas ir ietvertas POS pogu režģī. Pēc tam lietotāji var atlasīt pogas, lai izsauktu attiecīgās operācijas un veiktu ar tām saistītās funkcijas. Citas operācijas ir ietvertas galvenajā POS programmā, un tās var izsaukt, izmantojot ekrānā redzamās pogas vai arī citu darbplūsmu vai procesu ietvaros.

Tālāk esošajā tabulā ir sniegta detalizēta informācija par operācijām, kas ir pieejamas programmās Modern POS un Cloud POS. Tabulā ir arī norādīts, kurās programmas vietās var izsaukt operācijas, un tas, vai šīs operācijas ir pieejamas bezsaistes režīmā.

Dažas operācijas pašlaik nav pieejamas programmā Modern POS vai Cloud POS. Dažas no šīm operācijām ir lokalizācijai raksturīgas operācijas, kam ir nepieciešami papildu paplašinājumi un konfigurācija. Citas ir Microsoft Dynamics AX 2012 līdzekļi, kas pašlaik netiek atbalstīti.

Tālāk norādītajās kolonnās ir norādītas vietas, kur var izsaukt operācijas.

- **Pogu režģis** — operāciju var piešķirt pogām, kas ir ietvertas POS pogu režģos, kuri ir daļa no POS ekrāna izkārtojuma.
- **Transakciju ekrāns** — operācijas var izsaukt, izmantojot POS pogu režģus, kas ir konfigurēti POS transakciju ekrānā.
- **Sveiciena ekrāns** — operācijas var izsaukt, izmantojot POS pogu režģus, kas ir konfigurēti POS sveiciena ekrānā.

> [!NOTE]
> Tālāk norādītās operācijas attiecas uz jaunāko Commerce versiju. Dažas darbības var atšķirties vai nebūt pieejamas iepriekšējās versijās.

| ID | Operācija | apraksts | Pogu režģis | Transakciju ekrāns | Sveiciena ekrāns | Pieejama bezsaistē | Lokalizācijai raksturīga |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktivizēt ierīci | Aktivizēt pašreizējo ierīci, atļaujot autentificētam lietotājam ievadīt savienojuma informāciju un piešķirt ierīces un kases sistēmas ID. | Nē | Nē | Nē | Nē | Nē |
| 134 | Pievienot piederību | Pievienojiet darījumam iepriekš atlasītu piederību. Atlasiet piederību lapā **Pogas rekvizīti**. | Jā | Jā | Nē | Jā | Nē |
| 135 | Pievienot piederību no saraksta | Pievienot transakcijai piederību, atlasot to sarakstā. | Jā | Jā | Jā | Jā | Nē |
| 137 | Piederības pievienošana klientam | Pievienot piederību klientam lapā **detalizēta informācija par klientu**. | Nē | Nē | Nē | Jā | Nē |
| 138 | Piederības noņemšana klientam | Noņemt piederību lapā **detalizēta informācija par klientu**. | Nē | Nē | Nē | Jā | Nē |
| 643 | Pievienot kupona kodu | Pievienot kuponu, ievadot tā kodu POS sistēmā. | Jā | Jā | Nē | Jā | Nē |
| 141 | Pievienot virsrakstu maksas | Pievienojiet papildmaksu pasūtījuma galvenei. | Jā | Jā | Nē | Nē| Nē |
| 141 | Pievienot rindu maksas | Pievienojiet papildmaksu atlasītajai pārdošanas rindai. | Jā | Jā | Nē | Nē| Nē |
| 117 | Pievienot lojalitātes karti | Aicināt lietotāju ievadīt lojalitātes kartes numuru, kas tiks pievienots pašreizējai transakcijai. | Jā | Jā | Nē | Jā | Nē |
| 136 | Pievienot sērijas numuru | Šī operācija sniedz lietotājam iespēju norādīt pašlaik atlasītās preces sērijas numuru. | Jā | Jā | Nē | Jā | Nē |
| 1214 | Pievienot piegādes adresi | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 519 | Pievienot dāvanu kartei | Pievienojiet naudas līdzekļus norādītajai dāvanu kartei. | Jā | Jā | Nē | Nē | Nē |
| 6000 | Atļaut izlaist fiskālo reģistrāciju | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 1212 | Noguldījums bankā | Ierakstiet naudas summu, kas tiek nosūtīta uz banku, kā arī citu informāciju, piemēram, bankas inkasācijas somas numuru. | Jā | Jā | Jā | Jā | Nē |
| 923 | Bankas kopsummas pārbaude | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 915 | Tukša operācija | Šī operācija nodrošina pielāgojamu pogu, ko programmatūras izstrādātājs var programmiski piesaistīt jebkurai specializētai operācijai, kas ir nepieciešama uzņēmumam. | Jā | Jā | Jā | Jā | Nē |
| 1053 | Diskrēti slēgt maiņu | Iestatīt pašreizējo maiņu kā diskrēti slēgtu un izrakstiet lietotāju. Diskrēti slēgta maiņa ir slēgta papildu transakcijām, taču joprojām ir atvērta naudas kastes operācijām, piemēram, norēķinu noņemšanai un norēķinu uzskaitei. | Jā | Jā | Jā | Nē | Nē |
| 310 | Aprēķināt kopsummu | Ja ir atlikts atlaides aprēķins, šī operācija sniedz iespēju uzsākt aprēķinu pašreizējai transakcijai. | Jā | Jā | Nē | Jā | Nē |
| 642 | Iznest visas preces | Iestatīt visām rindām piegādes veidu **Iznešana**. | Jā | Jā | Nē | Jā\* | Nē |
| 641 | Iznest atlasītas preces | Iestatīt atlasītajām rindām piegādes veidu **Iznešana**. | Jā | Jā | Nē | Jā\* | Nē |
| 647 | Mainīt piegādes veidu | Mainiet iepriekš konfigurēto nosūtīšanas pārdošanas rindu piegādes veidu. | Jā | Jā | Nē | Nē| Nē |
| 1215 | Mainīt paroli | Šī operācija sniedz POS lietotājam iespēju mainīt savu paroli. | Jā | Jā | Jā | Nr. | Nr. |
| 123 | Mainīt mērvienību | Mainīt atlasītā rindas vienuma mērvienību. | Jā | Jā | Nē | Jā | Nē |
| 639 | Notīrīt noklusējuma darījuma pārdošanas pārstāvi | Noņemt no transakcijas komisijas pārdošanas grupu (pārdošanas pārst.). | Jā | Jā | Nē | Jā | Nē |
| 106 | Nodzēst daudzumu | Atiestatīt pašlaik atlasītās rindas daudzumu uz **1**. | Jā | Jā | Nē | Jā | Nē |
| 640 | Notīrīt rindā norādīto tirdzniecības pārstāvi | Noņemt no pašlaik atlasītās rindas komisijas pārdošanas grupu (pārdošanas pārst.). | Jā | Jā | Nē | Jā | Nē |
| 121 | Dzēst pārdevēju | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 1055 | Maiņas slēgšana | Slēgt pašreizējo maiņu, drukāt Z pārskatu un izrakstīt lietotāju no sistēmas. | Jā | Jā | Jā | Nē | Nē |
| 139 | Noslēgt transakciju | Lietotājam parāda uzvedni, lai atlasītu maksājuma metodi | Jā | Jā | Nē | Jā | Nē |
| 620 | Izveidot debitora pasūtījumu | Pārveidot POS transakciju par debitora pasūtījumu. | Jā | Jā | Nē | Jā\* | Nē |
| 925 | Kopēt bankas čeku | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 620 | Izveidot debitora pasūtījumu | Pārveidot POS transakciju par debitora pasūtījumu. | Jā | Jā | Nē | Jā\* | Nē |
| 621 | Izveidot piedāvājumu | Pārveidot POS transakciju par pārdošanas piedāvājumu. | Jā | Jā | Nē | Jā\* | Nē |
| 636 | Izveidot mazumtirdzniecības transakciju | Šī operācija sniedz lietotājam iespēju izveidot standarta pārdošanas transakciju gadījumā, kad noklusējuma POS darbība ir debitora pasūtījumu izveide. | Jā | Jā | Nē | Jā | Nē |
| 600 | Debitors | Pievienot transakcijai norādīto debitoru. | Nē | Nē | Nē | Jā | Nē |
| 1100 | Debitora konta depozīts | Veiciet maksājumu debitora kontā. | Jā | Jā | Jā | Jā | Jā |
| 612 | Debitora pievienošana | Šī operācija sniedz lietotājam iespēju izveidot jaunu debitora ierakstu. | Jā | Jā | Jā | Jā† | Nē |
| 603 | Debitora dzēšana | Noņemt debitoru no pašreizējās transakcijas. | Jā | Jā | Nē | Jā | Nē |
| 602 | Debitora meklēšana | Šī operācija sniedz lietotājam iespēju meklēt debitora ierakstu, pārlūkojot debitoru meklēšanas lapu POS sistēmā. | Jā | Jā | Jā | Jā | Nē |
| 609 | Debitora darbības | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 917 | Datu bāzes savienojuma statuss | Šī operācija sniedz lietotājam iespēju skatīt pašreizējā savienojuma iestatījumus un pārslēgt tiešsaistes un bezsaistes režīmu. | Jā | Jā | Jā | Jā | Nē |
| 1200 | Deklarēt sākuma summu | Norādiet summu, kas ir naudas kastē, sākot dienu vai maiņu. | Jā | Jā | Jā | Jā | Nē |
| 132 | Depozīta ignorēšana | Ignorējiet debitoru pasūtījumiem noklusējuma depozītu. | Jā | Jā | Nē | Jā\* | Nē |
| 913 | Dizaina režīma atspējošana | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 912 | Dizaina režīma iespējošana | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 1217 | Izjaukt komplektus | Izjauciet komplektu tā komponentu precēs. | Jā | Jā | Jā | Jā | Nē |
| 624 | Rādīt atmaksas summas | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 513 | Rādīt kopsummu | Parādīt transakcijas bilanci debitora displejā. | Jā | Jā | Jā | Jā | Nē |
| 623 | Labot debitoru | Rediģēt pašreizējā debitora datus. | Jā | Jā | Nē | Nē | Nē |
| 614 | Rediģēt debitora pasūtījumu | Atsaukt atlasīto pasūtījumu, lai to varētu izmainīt POS sistēmā. | Nē | Nē | Nē | Nē | Nē |
| 615 | Rediģēt piedāvājumu | Atsaukt atlasīto piedāvājumu, lai to varētu izmainīt POS sistēmā. | Nē | Nē | Nē | Nē | Nē |
| 518 | Izdevumu konti | Reģistrējiet naudas summu, kas tiek izņemta no naudas kastes neparedzētu izdevumu segšanai. | Jā | Jā | Jā | Jā | Nē |
| 919 | Paplašinātā pieteikšanās | Piešķirt vai noņemt atļauju pierakstīties, skenējot svītrkodu vai novelkot karti. | Jā | Jā | Jā | Jā | Nē |
| 1201 | Mainīgais ieraksts | Šī operācija sniedz lietotājam iespēju pievienot papildu naudu pašreizējā naudas kastē vai maiņā. | Jā | Jā | Jā | Jā | Nē |
| 1218 | Veikt perifērijas ierīces piespiedu atbloķēšanu | Šī operācija tiek iekšēji izmantota sistēmā, lai atbloķētu POS perifērijas ierīces. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 520 | Dāvanu kartes bilance | Parādīt dāvanu kartes bilanci. | Jā | Jā | Nē | Nē | Nē |
| 708 | Deaktivizēt ierīci | Deaktivizēt pašreizējo ierīci, lai to nevarētu izmantot kā POS kases sistēmu. | Nē | Nē | Nē | Nē | Nē |
| 804 | Ienākošā operācija | Piekļūstiet ienākošā veikala krājumu pārvaldības funkcijām. | Jā | Nē | Jā | Nē| Nē |
| 517 | Ieņēmumu konti | Reģistrējiet naudu, kas tiek ievietota naudas kastē citu iemeslu dēļ, kas nav pārdošana. | Jā | Jā | Jā | Jā | Nē |
| 801 | Krājumu pārlūkošana | Uzmeklēt pieejamos, pasūtāmos un solīšanai pieejamos (ATP) daudzumus pašreizējā veikalā un citās pieejamajās vietās. | Jā | Jā | Jā | Nē | Nē |
| 122 | Rēķina komentārs | Šī operācija sniedz lietotājam iespēju ievadīt komentāru par pašreizējo transakciju. | Jā | Jā | Nē | Jā | Nē |
| 511 | Izsniegt kredītrēķinu | Izsniegt kredītrēķinu, lai atmaksas vietā izsniegtu kuponu. | Jā | Jā | Nē | Nē | Nē |
| 512 | Izsniegt dāvanu karti | Izsniegt jaunu dāvanu karti par norādīto summu. | Jā | Jā | Nē | Nē | Nē |
| 625 | Izsniegt lojalitātes programmas karti | Izsniegt debitoram lojalitātes programmas karti, lai šis debitors varētu piedalīties veikala lojalitātes programmā. | Jā | Jā | Jā | Nē | Nē |
| 300 | Rindas atlaides summa | Ievadiet darījuma dokumenta rindas atlaides summu. Šī operācija tiek lietota tikai precēm, kam var lietot atlaidi, un tikai ar noteiktiem atlaides ierobežojumiem. | Jā | Jā | Nē | Jā | Nē |
| 301 | Rindas atlaide procentos | Ievadiet darījumā izmantotās dokumenta rindas atlaidi procentos. Šī operācija tiek lietota tikai precēm, kam var lietot atlaidi, un tikai ar noteiktiem atlaides ierobežojumiem. | Jā | Jā | Nē | Jā | Nē |
| 703 | Bloķēt reģistru | Bloķēt pašreizējo kases sistēmu, lai to nevarētu izmantot, taču neizrakstīt pašreizējo lietotāju. | Nē | Nē | Nē | Jā | Nē |
| 701 | Atteikties | Izrakstīt pašreizējo lietotāju no kases sistēmas. | Jā | Jā | Jā | Jā | Nē |
| 521 | Lojalitātes programmu karšu punktu bilance | Parādīt norādītās lojalitātes programmas kartes punktu bilanci. | Jā | Jā | Nē | Nē | Nē |
| 142 | Pārvaldīt maksas | Skatiet un pārvaldiet papildmaksas, kas piemērotas transakcijai. | Jā | Jā | Nē | Nē| Nē |
| 918 | Pārvaldīt maiņas | Parādīt aktīvo, pārtraukto un diskrēti slēgto maiņu sarakstu. | Jā | Jā | Jā | Nē | Nē |
| 914 | Minimizēt POS logu | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 1000 | Atvērt naudas kasti | Veikt operāciju bez pārdošanas un atvērt pašlaik atlasīto naudas kasti. | Jā | Jā | Jā | Jā | Nē |
| 928 | Pasūtījuma izpilde | Šī operācija ļauj lietotājiem izdot, iepakot, nosūtīt un atsaukt veikalā izdotos pasūtījumus. | Jā | Jā | Jā | Nē | Nē |
| 805 | Izejošā operācija | Piekļuves līdzekļi izejošo pārsūtīšanas pasūtījumu sūtījumu pārvaldībai. | Jā | Nē | Jā | Nē| Nē |
| 129 | Ignorēt preces rindas nodokli | Pārlabot nodokli par atlasīto rindas vienumu un izmantot citu norādīto nodokli. | Jā | Jā | Nē | Jā | Nē |
| 130 | Ignorēt sarakstā esošu preces rindas nodokli | Pārlabot nodokli par atlasīto rindas vienumu un izmantot nodokli, ko lietotājs atlasa sarakstā. | Jā | Jā | Nē | Jā | Nē |
| 127 | Ignorēt darbības nodokli | Pārlabot nodokli par transakciju un izmantot citu norādīto nodokli. | Jā | Jā | Nē | Jā | Nē |
| 128 | Ignorēt sarakstā esošu darbības nodokli | Pārlabot nodokli par transakciju un izmantot nodokli, ko lietotājs atlasa sarakstā. | Jā | Jā | Nē | Jā | Nē |
| 131 | Pavadzīme | Izveidot atlasītā pasūtījuma pavadzīmi. | Nē | Nē | Nē | Nē | Nē |
| 710 | Savienot aparatūras staciju pārī | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 201 | Maksājums ar karti | Kā maksājuma veidu pieņemt karti, piemēram, kredītkarti vai debetkarti. | Jā | Jā | Nē | Jā | Nē |
| 200 | Maksājums skaidrā naudā | Kā maksājuma veidu pieņemiet skaidru naudu. | Jā | Jā | Nē | Jā | Nē |
| 206 | Ātrais maksājums skaidrā naudā | Pabeigt transakciju ar vienu pieskārienu un pieņemt maksājamo summu skaidrā naudā (bez atlikuma). | Jā | Jā | Nē | Jā | Nē |
| 204 | Maksājums ar čeku | Pieņemiet čeku kā maksājuma veidu. | Jā | Jā | Nē | Jā | Nē |
| 213 | Maksājums ar kredītrēķinu | Pieņemt veikalā izsniegtu kredītrēķinu (kuponu). | Jā | Jā | Nē | Nē | Nē |
| 203 | Maksājums valūtā | Pieņemiet maksājumu dažādās valūtās. | Jā | Jā | Nē | Jā | Nē |
| 202 | Maksājums, izmantojot debitora kontu | Ņemt maksu par transakciju no debitora konta. Šī maksāšanas metode nav derīga debitoru pasūtījumu depozītiem. | Jā | Jā | Nē | Nē | Nē |
| 214 | Maksājums ar dāvanu karti | Pieņemt veikalā izsniegtu dāvanu karti. | Jā | Jā | Nē | Nē | Nē |
| 207 | Maksāt ar lojalitātes programmas karti | Kā maksāšanas metodi pieņemt lojalitātes karti un izpirkt punktus apmaiņā pret piemērotajām precēm. | Jā | Jā | Nē | Nē | Nē |
| 634 | Maksājumu vēsture | Parādīt debitora maksājumu vēsturi par pašreizējo debitora pasūtījumu. | Jā | Jā | Nē | Nē | Nē |
| 803 | Izdošana un saņemšana | Atvērt lapu **Izdošana un saņemšana**, kur varat atlasīt pasūtījumus, kas ir jāizdod vai jāsaņem veikalā. | Jā | Jā | Jā | Nē | Nē |
| 632 | Saņemt visas preces | Iestatīt visām rindām izpildes metodi **Saņemšana veikalā**. | Jā | Jā | Nē | Jā\* | Nē |
| 631 | Saņemt atlasītās preces | Iestatīt atlasītajām rindām izpildes metodi **Saņemšana veikalā**. | Jā | Jā | Nē | Jā\* | Nē |
| 400 | Uznirstošā izvēlne | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 101 | Cenas pārbaude | Šī operācija sniedz lietotājam iespēju uzmeklēt norādītās preces cenu. | Jā | Jā | Jā | Jā | Nē |
| 104 | Cenas ignorēšana | Pārlabot preces cenu, ja šai precei ir iestatīta cenas pārlabošana. | Jā | Jā | Nē | Jā | Nē |
| 1058 | Drukāt finanšu X | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 1059 | Drukāt finanšu Z | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 927 | Drukāt krājuma etiķeti | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 926 | Drukāt plaukta etiķeti | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 1056 | Drukāt X | Drukāt X pārskatu par pašreizējo maiņu. | Jā | Jā | Jā | Nē | Nē |
| 103 | Preces piezīme | Pievienojiet komentāru darījumā atlasītajai dokumenta rindai. | Jā | Jā | Nē | Jā | Nē |
| 100 | Preces pārdošana | Pievienot transakcijai norādīto preci. | Jā | Jā | Jā | Jā | Nē |
| 108 | Preču meklēšana | Šī operācija sniedz lietotājam iespēju meklēt preci, pārlūkojot preču meklēšanas lapu POS sistēmā. | Jā | Jā | Jā | Jā | Nē |
| 633 | Piedāvājuma beigu datums | Šī operācija sniedz lietotājam iespēju skatīt vai izmainīt pārdošanas piedāvājuma beigu datumu. | Jā | Jā | Nē | Jā\* | Nē |
| 627 | Pārrēķināt | Pārrēķināt visas debitora pasūtījuma rindas un nodokļus, pamatojoties uz pašreizējo konfigurāciju. | Jā | Jā | Nē | Jā\* | Nē |
| 143 | Pārrēķināt maksas | Pārrēķiniet pasūtījumam piemērotās automātiskās maksas. | Jā | Jā | Nē | Nē| Nē |
| 515 | Atsaukt pasūtījumu | Šī operācija sniedz lietotājam iespēju meklēt un atsaukt debitoru pasūtījumus un pārdošanas piedāvājumus. | Jā | Jā | Jā | Nē | Nē |
| 504 | Atsaukt darījumu | Šī operācija sniedz lietotājam iespēju atsaukt pašreizējā veikalā iepriekš aizturētu transakciju. | Jā | Jā | Nē | Jā‡ | Nē |
| 305 | Izpirkt lojalitātes programmas punktus | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 635 | Atmaksāt piegādes izmaksas | Šī operācija sniedz lietotājam iespēju atmaksāt atcelta pasūtījuma piegādes izmaksas. | Nē | Nē | Nē | Nē | Nē |
| 644 | Noņemt kupona kodu | Aicināt lietotāju noņemt kuponus, atlasot tos ar transakciju pašlaik saistīto kuponu sarakstā. | Jā | Jā | Nē | Jā | Nē |
| 1057 | Atkārtoti drukāt Z | Atkārtoti drukāt Z pārskatu par iepriekšējo maiņu vai atlasītu maiņu. | Jā | Jā | Jā | Nē | Nē |
| 1216 | Jaunas paroles ievadīšana | Šī operācija sniedz lietotājam iespēju atiestatīt cita darbinieka paroli, izmantojot pagaidu paroli, ja šim lietotājam ir paroles atiestatīšanas atļauja. | Jā | Jā | Jā | Nē | Nē |
| 1219 | URL atvērš. POS | Šī operāc. ļauj lietotājam atvērt admin. konfigurētu URL POS. | Jā | Jā | Jā | Jā | Nē | 
| 109 | Atgriezt preci | Veiciet atsevišķu preču atgriešanu. Nākamā skenētā prece tiek parādīta kā atgriezta prece ar negatīvu daudzumu un cenu. | Jā | Jā | Nē | Jā | Nē |
| 114 | Atgriezt darījumu | Atsaukt iepriekšējo transakciju pēc tās kvīts numura, lai atgrieztu visas preces vai daļu no tām. | Jā | Jā | Jā | Jā§ | Nē |
| 1211 | Noguldījums seifā | Veiciet noguldījumu seifā, lai pārvietotu naudu no kases sistēmas uz seifu. | Jā | Jā | Jā | Jā | Nē |
| 516 | Pārdošanas rēķins | Šī operācija sniedz debitoram iespēju veikt maksājumus, lai apmaksātu atlasīto pārdošanas rēķinu. | Jā | Jā | Nē | Nē | Nē |
| 502 | Pārdevējs | Šī operācija sniedz lietotājam iespēju iestatīt debitoru pasūtījumu pārdošanas pasūtījuma parametra **Pārdošanas uzņēmējs** vērtību POS sistēmā. | Jā | Jā | Nē | Jā\* | Nē |
| 2000 | Grafika pārvaldība | Šī operācija pagaidām netiek atbalstīta. | Jā | Jā | Jā | Nē | Nē |
| 2001 | Grafika pieprasījumi | Šī operācija pagaidām netiek atbalstīta. | Jā | Jā | Jā | Nē | Nē |
| 622 | Meklēšana | Šī operācija sniedz lietotājiem iespēju iepriekš konfigurēt POS pogas, lai veiktu meklēšanu pēc krājuma, debitora vai kategorijas. | Jā | Jā | Jā | Jā | Nē |
| 1213 | Meklēt piegādes adresi | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 709 | Atlasīt aparatūras staciju | Šī operācija sniedz lietotājam iespēju atlasīt aparatūras staciju pieejamo aparatūras staciju sarakstā. | Jā | Jā | Jā | Jā | Nē |
| 637 | Iestatīt noklusējuma darījuma pārdošanas pārstāvi | Šī operācija sniedz lietotājam iespēju atlasīt vienu no derīgajām komisijas pārdošanas grupām (pārdošanas pārst.) kā vēlāk pievienoto rindu noklusējuma pārdošanas pārstāvi. | Jā | Jā | Nē | Jā | Nē |
| 105 | Iestatīt daudzumu | Mainiet darījuma dokumenta rindas daudzumu. | Jā | Jā | Nē | Jā | Nē |
| 638 | Iestatīt rindas pārdošanas pārstāvi | Šī operācija sniedz lietotājam iespēju atlasīt vienu no derīgajām komisijas pārdošanas grupām (pārdošanas pārst.) pašlaik atlasītajai rindai. | Jā | Jā | Nē | Jā | Nē |
| 630 | Nosūtīt visas preces | Iestatīt visiem rindu vienumiem izpildes režīmu **Nosūtīšana**. | Jā | Jā | Nē | Jā\* | Nē |
| 629 | Nosūtīt atlasītās preces | Iestatīt atlasītajām rindām izpildes režīmu **Nosūtīšana**. | Jā | Jā | Nē | Jā\* | Nē |
| 115 | Rādīt žurnālu | Parādīt veikala žurnālu. Varat skatīt transakcijas, atkārtoti izdrukāt kvītis un dāvanu kvītis un atsaukt transakcijas atgriešanai. | Jā | Jā | Jā | Jā\*\* | Nē |
| 802 | Krājumu uzskaite | Šī operācija sniedz lietotājam iespēju izveidot vai izmainīt fizisko krājumu vai cikla inventarizācijas uzskaites žurnālus. | Jā | Jā | Jā | Nē | Nē |
| 401 | Apakšizvēlne | Šī operācija nodrošina lietotāja novirzīšanu uz citu saistīto pogu režģi. | Jā | Jā | Jā | Jā | Nē |
| 1054 | Maiņas pārtraukšana | Aizturēt pašreizējo maiņu, lai pašreizējā kases sistēmā varētu aktivizēt jaunu vai citu maiņu. | Jā | Jā | Jā | Nē | Nē |
| 503 | Darījuma aizturēšana | Aizturēt pašreizējo pārdošanas transakciju, lai to vēlāk varētu atsaukt veikalā. | Jā | Jā | Nē | Jā‡ | Nē |
| 1004 | Uzdevumu reģistrētājs | Atvērt uzdevumu reģistrētāju, lai reģistrētu procedūras darbības POS sistēmā. | Nē | Nē | Nē | Jā | Nē |
| 1052 | Norēķinu uzskaite | Šī operācija sniedz lietotājam iespēju norādīt naudas kastē esošo naudas summu atbilstoši katrai uzskaitītajai maksāšanas metodei. | Jā | Jā | Jā | Jā | Nē |
| 1210 | Norēķinu noņemšana | Šī operācija sniedz lietotājam iespēju izņemt naudu no pašreizējās naudas kastes vai maiņas. | Jā | Jā | Jā | Jā | Nē |
| 920 | Darba laika uzskaite | Šī operācija sniedz lietotājiem iespēju reģistrēt darba maiņu un pārtraukumu sākumu un beigas. | Jā | Jā | Jā | Nē | Nē |
| 302 | Kopējā atlaides summa | Ievadīt transakcijas atlaides summu. Šī operācija attiecas tikai uz tām precēm, kam var lietot atlaidi, un tikai ar noteiktiem atlaides ierobežojumiem. | Jā | Jā | Nē | Jā | Nē |
| 303 | Kopējie atlaides procenti | Ievadīt transakcijas atlaides procentus. Šī operācija attiecas tikai uz tām precēm, kam var lietot atlaidi, un tikai ar noteiktiem atlaides ierobežojumiem. | Jā | Jā | Nē | Jā | Nē |
| 501 | Darbības apraksts | Pievienot komentāru pašreizējai transakcijai. | Jā | Jā | Nē | Jā | Nē |
| 922 | Skatiet detalizētu informāciju par preci | Atvērt pašlaik atlasītā rindas vienuma lapu Detalizēta informācija par preci. | Jā | Jā | Nē | Jā | Nē |
| 1003 | Skatīt pārskatus | Parādīt pašreizējam lietotājam konfigurētos pārskatus. | Jā | Jā | Jā | Nē | Nē |
| 921 | Skatiet darba laika uzskaites ierakstus | Parādīt visu veikala darbinieku laika uzskaites ierakstus. | Jā | Jā | Jā | Nē | Nē |
| 211 | Anulēt maksājumu | Anulēt transakcijā pašlaik atlasīto maksājuma rindu. | Jā | Jā | Nē | Jā | Nē |
| 102 | Anulēt preci | Anulēt transakcijā pašlaik atlasīto rindas vienumu. | Jā | Jā | Nē | Jā | Nē |
| 500 | Anulēt darījumu | Anulēt pašreizējo transakciju. | Jā | Jā | Nē | Jā | Nē |
| 916 | Windows darbplūsmas pamats | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē |
| 924 | X pārskats bankas kartēm | Šī operācija netiek atbalstīta. | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Jā |
| 311 | Noņemt sistēmas atlaides no darījumiem | Noņemiet no darbības visas sistēmas piemērotās atlaides, ieskaitot uz kuponu balstītās atlaides. Tādējādi netiek noņemtas manuālās atlaides. | Jā | Jā | Jā | Jā | Nr. |
| 312 | Atkārtoti izmantot sistēmas atlaides | Atkārtoti izmantot sistēmas atlaides darījumam, ja tās ir noņemtas, izmantojot operāciju **Noņemt sistēmas atlaides no darījuma**. | Jā | Jā | Jā | Jā | Nr. |

\* Operācija ir pieejama bezsaistes režīmā tikai tad, ja tiek izveidots debitora pasūtījums vai pārdošanas piedāvājums un ja POS funkcionalitātes profilā ir konfigurēta debitoru rēķinu un pārdošanas piedāvājumu izveide bezsaistes režīmā. Operāciju nevar veikt, ja pasūtījumi tiek veidoti, izmantojot reāllaika pakalpojumu, vai ja pasūtījumi tiek atsaukti vai rediģēti.

† Operāciju var veikt bezsaistes režīmā tikai tad, ja POS funkcionalitātes profils ir konfigurēts tā, lai atļautu debitoru izveidi bezsaistes režīmā.

‡ Ja POS ir bezsaistē, aizturētās transakcijas var atsaukt tikai no pašreizējās kases sistēmas bezsaistes datu bāzes. Lietotāji nevar aizturēt un atsaukt transakcijas dažādās kases sistēmās.

§ Ja POS ir bezsaistē, atgriešanai var atsaukt tikai pašreizējā bezsaistes datu bāzē saglabātās transakcijas.

\*\* Ja POS ir bezsaistē, žurnālā tiek rādītas tikai pašreizējā bezsaistes kanāla datu bāzē saglabātās transakcijas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]