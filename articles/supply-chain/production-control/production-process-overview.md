---
title: Pārskats par ražošanas procesu
description: Šajā tēmā ir sniegts pārskats par ražošanas procesiem. Tajā ir aprakstīti dažādie ražošanas pasūtījumu, partijas pasūtījumu un Kanban darbu stāvokļi no pasūtījuma izveides līdz finanšu perioda slēgšanai.
author: cvocph
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, OpResLifecycleManagementWorkspace, ProdParmCostEstimation, ProdParmRelease, ProdSchedule, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a376510e76bdc9687f7fa9af5921ae7c50d1fc59
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998931"
---
# <a name="production-process-overview"></a>Pārskats par ražošanas procesu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par ražošanas procesiem. Tajā ir aprakstīti dažādie ražošanas pasūtījumu, partijas pasūtījumu un Kanban darbu stāvokļi no pasūtījuma izveides līdz finanšu perioda slēgšanai. 

Preču ražošanas process dažreiz tiek saukts arī par ražošanas dzīves ciklu, un tā ietvaros tiek veiktas konkrētas darbības, kas ir nepieciešamas, lai pabeigtu krājuma ražošanu. Dzīves cikls sākas ar ražošanas pasūtījuma, partijas pasūtījuma vai Kanban izveidi. Tas beidzas ar pabeigtu saražoto krājumu, ko var nodot debitoram vai citai ražošanas fāzei. Lai pabeigtu visu procesu, katrai dzīves cikla darbībai ir nepieciešama atšķirīga informācija. Pēc katras darbības pabeigšanas ražošanas pasūtījumā, partijas pasūtījumā vai Kanban tiek atspoguļotas ražošanas statusa izmaiņas. Dažāda veida precēm ir nepieciešami dažādi ražošanas procesi.  

Modulis **Ražošanas kontrole** ir saistīts ar citiem moduļiem, piemēram, **Preču informācijas pārvaldība**, **Krājumu vadība**, **Virsgrāmata**, **Noliktavas pārvaldība**, **Projektu uzskaite** un **Organizācijas administrēšana**. Šī integrācija atbalsta informācijas plūsmu, kas ir nepieciešama pabeigtā krājuma ražošanas pabeigšanai.  

Ražošanas procesu parasti ietekmē izmaksu uzskaites un krājumu novērtēšanas metodes, kas ir izvēlas konkrētam ražošanas procesam. Programmatūra Supply Chain Management atbalsta gan faktisko izmaksu (pirmie iekšā, pirmie ārā \[FIFO\]; pēdējie iekšā, pirmie ārā \[LIFO\]; slīdošais vidējais; periodiskais svērtais vidējais) un standarta izmaksu metodes. Lean manufacturing ražošana tiek ieviesta, pamatojoties uz atgriezeniskās izmaksu aprēķināšanas principu.  

Izmaksu mērīšanas metožu izvēle nosaka arī prasības attiecībā uz ziņošanu par materiālu un resursu patēriņu ražošanas procesa laikā. Parasti faktisko izmaksu metodēm ir nepieciešama precīza ziņošana darba līmenī, taču periodisko izmaksu noteikšanas metodēm ir nepieciešama mazāk detalizēta ziņošana par materiālu un resursu patēriņu.

## <a name="mixed-mode-manufacturing"></a>Jauktā režīma ražošana
Dažādām precēm un preču topoloģijām ir nepieciešams lietot dažādus pasūtījumu veidus. Supply Chain Management var lietot dažādos pasūtījumu veidus jauktā režīmā. Citiem vārdiem sakot, visa vienas saražotās preces ražošanas procesa laikā var veikt visu veidu pasūtījumus.

-   **Ražošanas pasūtījums** — tas ir standarta pasūtījuma veids, kas tiek izmantots, lai noteiktā datumā saražotu noteiktu konkrētas preces vai preces varianta daudzumu. Ražošanas pasūtījumi tiek veidoti, pamatojoties uz materiālu komplektiem (MK) un maršrutiem.
-   **Partijas pasūtījums** — šis pasūtījuma veids tiek izmantots ražošanas nozarēs un atsevišķos procesos, kur ražošanas pārveidošanas pamatā ir formula vai kur līdzprodukti un blakusprodukti var būt galaprodukti, kas papildina vai aizstāj pamatpreci. Partijas pasūtījumiem tiek izmantoti MK un maršruti, kuru tips ir **Formula**.
-   **Kanban** — Kanban tiek izmantoti, lai norādītu uz atkārtotiem lean manufacturing procesiem, kuru pamatā ir ražošanas plūsmas, Kanban nosacījumi un MK.
-   **Projekts** — ražošanas projektā ir apvienotas preces un pakalpojumi ar noteiktu grafiku un budžetu. Projekta ražošanas daļu var nodrošināt, izmantojot jebkuru citu pasūtījuma veidu.

## <a name="manufacturing-principles"></a>Ražošanas principi
Lai atlasītu ražošanas principu, kas ir vislabāk piemērots konkrētai precei un saistītajam tirgum, ir jāņem vērā ražošanas un loģistikas prasības, kā arī debitoru prasības attiecībā uz piegādes izpildes laiku.

-   **Ražot krājumiem** — šis ir standarta ražošanas princips, kura ietvaros preces tiek ražotas krājumiem, pamatojoties uz prognozi vai minimālo krājumu papildinājumu (pēdējais parasti tiek aprēķināts, pamatojoties uz prognozi vai vēsturisko patēriņu).
-   **Ražot pēc pasūtījuma** — standarta preces tiek ražotas pēc pasūtījuma vai pabeigtas pēc pasūtījuma. Lai gan preces var saražot iepriekš, izmantojot principu Ražot krājumiem, pārdošanas pasūtījums vai pārsūtīšanas pasūtījums aktivizē dārgas vērtības ķēdes darbības vai variantu izgatavošanas darbības.
-   **Konfigurēt pēc pasūtījuma** — vērtības ķēdes beigu operācijas tiek veiktas pēc pasūtījuma tāpat kā principam Ražot pēc pasūtījuma. Faktiskais saražotais preces variants nav iepriekš definēts, bet tiek izgatavots pasūtījuma ievades laikā, pamatojoties uz pārdotās preces konfigurācijas modeli. Principam Konfigurēt pēc pasūtījuma ir nepieciešama noteikta līmeņa procesa unificēšana attiecīgajai preču līnijai.
-   **Izstrādāt pēc pasūtījuma** — principa Izstrādāt pēc pasūtījuma procesi parasti ir saistīti ar projektu un parasti sākas ar izstrādes fāzi. Izstrādes fāzes laikā tiek izstrādātas un aprakstītas faktiskās preces, kas ir nepieciešamas, lai izpildītu pasūtījumu. Pēc tam var izveidot ražošanas pasūtījumus, partijas pasūtījumus vai Kanban, lai saražotu preces.

## <a name="overview-of-the-production-life-cycle"></a>Ražošanas dzīves cikla pārskats
Tālāk norādītās ražošanas dzīves cikla darbības var tikt veiktas visiem jauktas ražošanas pasūtījumu veidiem. Taču dažas no tām netiek norādītas ar īpašu pasūtījuma statusu.

1.  **Izveidots** — varat manuāli izveidot ražošanas pasūtījumu, partijas pasūtījumu vai Kanban vai arī varat konfigurēt sistēmu tā, lai tie tiktu ģenerēti, pamatojoties uz dažādiem pieprasījuma signāliem. Vispārējā plānošana nodrošina ražošanas pasūtījumu, partijas pasūtījumu vai Kanban izveidi, apstiprinot plānotos pasūtījumus. Citi pieprasījuma signāli ir pārdošanas pasūtījumi vai piesaistītas piegādes signāli no citiem ražošanas pasūtījumiem vai Kanban. Fiksēta daudzuma Kanban gadījumā pieprasījuma signāli tiek ģenerēti, kad Kanban tiek reģistrēti kā tukši.
2.  **Novērtēts** — varat aprēķināt materiālu vai resursu patēriņa novērtēto apjomu. Veicot novērtējumu, tiek ģenerētas krājumu transakcijas izejmateriāliem, kuru statuss ir **Pasūtīts**. Kad tiek novērtēti ražošanas pasūtījumi vai partijas pasūtījumi, tiek ģenerētas pamatpreču, līdzproduktu un blakusproduktu ieejas plūsmas. Ja MK ir rindas, kuru veids ir **Pieprasīta piegāde**, tiek ģenerēti materiālu vai apakšuzņēmēja operāciju pakalpojumu pirkšanas pasūtījumi, kas tiek piesaistīti ražošanas pasūtījumam vai partijas pasūtījumam. Krājumi vai pasūtījumi tiek rezervēti atbilstoši ražošanas pasūtījuma rezervēšanas stratēģijai, un saražoto preču cena tiek aprēķināta, pamatojoties uz parametru iestatījumiem.
3.  **Ieplānots** — varat plānot ražošanu, pamatojoties uz operācijām, atsevišķiem darbiem vai abiem šiem faktoriem.
    -   **Operāciju plānošana** — šī plānošanas metode nodrošina aptuvenu ilgtermiņa plānu. Izmantojot šo metodi, ražošanas pasūtījumiem varat piešķirt sākuma un beigu datumus. Ja ražošanas pasūtījumi tiek piesaistīti maršruta operācijām, varat tos piešķirt izmaksu centru grupām.
    -   **Darbu plānošana** — šī plānošanas metode nodrošina detalizētu plānu. Katra operācija tiek sadalīta atsevišķos darbos, kam ir noteikti datumi, laiki un piešķirtie operācijas resursi. Ja tiek izmantota ierobežota noslodze, darbi tiek piešķirti operācijas resursiem atkarībā no pieejamības. Plānu var skatīt un mainīt Ganta shēmā.
    -   **Kanban grafiks** — Kanban darbi tiek plānoti, izmantojot Kanban grafika dēli, vai tiek automātiski plānoti, pamatojoties uz Kanban nosacījumu automātiskās plānošanas konfigurāciju.

4.  **Izlaists** — varat izlaist ražošanas pasūtījumu vai partijas pasūtījumu, kad grafiks ir izpildīts un materiāls ir pieejama izdošanai vai sagatavošanai. Materiālu pieejamības pārbaude palīdz ražotnes vadītājam novērtēt materiāla pieejamību ražošanas pasūtījumu vai partijas pasūtījumu izpildei. Varat arī izdrukāt ražošanas pasūtījuma dokumentus, piemēram, izdošanas sarakstus, darbu karti, maršruta karti un maršruta darbu. Kad ražošanas pasūtījums ir izlaists, pasūtījuma statuss tiek mainīts, norādot, ka ražošanu var sākt. Ja tiek izmantota noliktavas pārvaldība, izlaižot ražošanas pasūtījumu vai partijas pasūtījumu, ražošanas MK rindas tiek izlaistas noliktavas pārvaldībai. Pēc tam tiek ģenerēti noliktavas kopumi un noliktavas darbi atbilstoši noliktavas iestatījumiem.
5.  **Sagatavots**/**izdots** — kad ražošanas vietā ir nodrošināti visi materiāli un resursi, ražošanas MK rindu vai Kanban rindu statuss tiek mainīts uz **Izdots**. Šajā posmā parasti tiek pabeigti pieprasītās piegādes pasūtījumi un saistītie noliktavas darbi. Ir jāpiešķir un jāizdrukā Kanban kartes vai darbu kartes, kas ir nepieciešamas ziņošanai par ražošanas norisi.
6.  **Sākts** — kad tiek sākts ražošanas pasūtījums, partijas pasūtījums vai Kanban, varat ziņot par materiālu un resursu patēriņu atbilstoši pasūtījumam. Sistēmu var konfigurēt tā, lai automātiski grāmatotu to materiālu un resursu patēriņu, kas tiek piešķirti pasūtījumam tā sākšanas laikā. Šī piešķiršana tiek saukta par sākotnējo norakstīšanu, iepriekšēju norakstīšanu vai automātisko patēriņu. Varat manuāli piešķirt materiālus ražošanas pasūtījumiem vai partijas pasūtījumiem, izveidojot papildu izdošanas sarakstu žurnālus. Varat pasūtījumam manuāli piešķirt arī darbaspēka un citas maršruta izmaksas. Ja izmantojat operāciju plānošanu, varat piešķirt šīs izmaksas, izveidojot maršruta karšu žurnālu. Ja izmantojat darbu plānošanu, varat piešķirt izmaksas, izveidojot darbu karšu žurnālu. Ražošanas pasūtījumus vai partijas pasūtījumus var sākt pieprasītajam beigu daudzumam atbilstošās partijās. Ražošanas pasūtījumā, partijas pasūtījumā vai Kanban izveidotos darbus var sākt un reģistrēt atsevišķi, izmantojot žurnālus, ražošanas izpildes termināli (MES termināli) vai Kanban dēļus.
7.  Ziņot par norisi/**pabeigt** darbus — izmantojiet MES termināli, ražošanas žurnālus, Kanban dēļus vai mobilās skenēšanas iespējas, lai ziņotu par ražošanas norisi pēc darba vai resursa. Tiek grāmatots materiālu un resursu patēriņš, un saistīto Kanban, ražošanas pasūtījumu un partijas pasūtījumu statuss var tikt atjaunināts uz **Saņemts** vai **Ziņots kā pabeigts**. Var tikt izveidots izvietošanas noliktavas darbs atkarībā no noliktavas konfigurācijas.
8.  **Ziņots kā pabeigts** (produktu ieejas plūsma) — kad tiek ziņots par ražošanas pasūtījuma vai partijas pasūtījuma pabeigšanu, krājumos tiek atjaunināts pabeigto saražoto preču daudzums. Šis daudzums ietver saistīto līdzproduktu un blakusproduktu daudzumu. Ja izmantojat nepabeigtās ražošanas (NP) uzskaiti, tiek ģenerēts virsgrāmatas žurnāls, lai samazinātu NP kontu skaitu un palielinātu saražoto preču krājumu skaitu. Kad ir aprēķinātas ražošanas pasūtījuma izmaksas, tiek iegrāmatotas ražošanas faktiskās izmaksas. Ja ar ražošanu saistītās materiālu un darbaspēka izmaksas vēl nav piešķirtas žurnālā vai ar iepriekšēju norakstīšanu, tās var automātiski piešķirt, izmantojot atgriezenisko norakstīšanu. Piešķiršana, izmantojot atgriezenisko norakstīšanu, ietver krājumu transakciju procesu vēlāku samazināšanu. Ja ražošanas pasūtījums ir pabeigts, atzīmējiet izvēles rūtiņu **Pēdējais darbs**, lai mainītu atlikušo statusu uz **Pabeigts**. Pretējā gadījumā atstājiet šo lauku tukšu, lai varētu ziņot par papildu saražoto daudzumu.
9.  **Kvalitātes novērtēšana** — produktu ieejas plūsma var izraisīt kvalitātes pārbaudes pasūtījumu izveidi atkarībā no pārbaudes procesiem un kvalitātes nosacījumiem, kas ir noteikti konkrētajām precēm. Tā kā kvalitātes pārbaudes pasūtījums var izraisīt pārbaudīto preču krājumu statusa vai partijas atribūtu atjaunināšanu, daudzās nozarēs kvalitātes novērtēšana ir obligāts process.
10. **Izvietot** un **Nosūtīt pēc pasūtījuma** — pēc produktu ieejas plūsmas saņemšanas un kvalitātes novērtēšanas pēc izvēles veicamais izvietošanas darbs novirza saņemtās preces uz nākamo patēriņa punktu, saražoto preču noliktavu vai nosūtīšanas zonu, ja pastāv prasības nosūtīšanai pēc pasūtījuma.
11. **Pabeigts** — pirms ražošanas beigšanas tiek aprēķinātas saražotā daudzuma faktiskās izmaksas. Visas novērtētās materiālu, darbu un papildu atbalsta izmaksas tiek apgrieztas un aizstātas ar faktiskajām izmaksām. Ja, veicot izmaksu aprēķināšanu, atzīmējat izvēles rūtiņu **Pēdējais darbs**, ražošanas pasūtījuma statuss tiek mainīts uz **Pabeigts**.. Šis statuss neļauj pabeigtā ražošanas pasūtījumā grāmatot papildu izmaksas.
12. **Perioda slēgšana** — dažiem izmaksu uzskaites principiem, piemēram, periodiskā vidējā, atgriezeniskās norakstīšanas, FIFO vai LIFO principam, ir nepieciešamas periodiskas krājumu vai finanšu perioda slēgšanas aktivitātes. Parasti pirms periodu slēgšanas sistēmā tiek mēģināts ziņot par visu materiālu un resursu patēriņu, kā arī krājumu un brāķu labojumiem. Šī ziņošana parasti tiek veikta, izmantojot krājumu kustības žurnālus vai korekciju žurnālus. Mērķis ir novērtēt pārvaldības struktūrvienības ekonomisko sniegumu konkrētā periodā. Dažos gadījumos, kad tiek izmantoti ilgstoši ražošanas pasūtījumi, kas aptver vairākus finanšu pārskata periodus, par ražošanas norisi un resursu patēriņu līdz perioda beigām tiek ziņots, izmantojot ražošanas žurnālus.


<a name="additional-resources"></a>Papildu resursi
--------

[Ražošanas atsauksmes](production-feedback.md)

[Pārskats par preču konfigurācijas modeļiem](../pim/product-configuration-models.md)

[Lean manufacturing apskats](lean-manufacturing-overview.md)



