---
title: Zvanu centra pārkāpumu brīdinājumu iestatīšana un darbs ar tiem
description: Šajā tēmā izskaidrots, kā iestatīt kārtulas, lai brīdinātu klientu apkalpošanas pārstāvjus par potenciāli krāpniecisku informāciju, kad tiek apstrādāti pasūtījumi. Var definēt īpašus kodus, kas tiek izmantoti, lai automātiski vai manuāli aizturētu aizdomīgus pasūtījumus.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 13b6a18750e79a17c7f6034780922c64b12390e2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "361502"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Zvanu centra pārkāpumu brīdinājumu iestatīšana un darbs ar tiem

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt kritērijus un kārtulas, lai aizturētu potenciāli krāpnieciskus pārdošanas pasūtījumus turpmākai pārskatīšanai. Pārkāpumu pārbaudes līdzeklis tiek izmantots, lai noteiktu pārdošanas pasūtījumā ietvertās informācijas derīgumu. Ja, pamatojoties uz organizācijas pārkāpumu kritērijiem un kārtulām, pārdošanas pasūtījumā ietvertā informācija tiek atzīta par apšaubāmu, pasūtījumu var aizturēt turpmākai pārskatīšanai. Šajā gadījumā pasūtījumu nevar nosūtīt uz noliktavu turpmākai apstrādei, līdz aizturēšana ir dzēsta.

> [!NOTE]
> Šo līdzekli var lietot tikai ar pārdošanas pasūtījumu apstrādi Retail zvanu centra kanālam.

## <a name="turning-on-the-fraud-check-feature"></a>Pārkāpumu pārbaudes līdzekļa ieslēgšana

Lai izmantotu pārkāpumu pārbaudes līdzekli, kanāla opcijai **Iespējot pasūtījuma pabeigšanu** ir jāiestata vienums **Jā**, kad zvanu centra kanāls ir [definēts](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options). Kad ir ieslēgta pasūtījuma pabeigšana, zvanu centra lietotājiem ir jāatlasa vienums **Pabeigt** pārdošanas pasūtījumu lapā visiem izveidotajiem pārdošanas pasūtījumiem. Pabeigšanas darbība atver lapu **Pārdošanas pasūtījumu kopsavilkums**. Pēc tam, kad lietotāji ievada nepieciešamos maksājuma datus lapā **Pārdošanas pasūtījumu kopsavilkums**, viņi atlasa vienumu **Iesniegt**, lai pabeigtu pasūtījumu. Kad pasūtījums ir iesniegts, tiek aktivizēts pārkāpumu pārbaudes līdzeklis, un tiek automātiski pārbaudītas visas sistēmas aktīvās kārtulas.

Zvanu centra lietotāji var arī manuāli aizturēt pārdošanas pasūtījumus pārkāpumu pārskatīšanai, pirms viņi atlasa vienumu **Iesniegt**. Lai manuāli aizturētu pārdošanas pasūtījumu, lapā **Pārdošanas pasūtījumu kopsavilkums** atlasiet **Aizturēt** \> **Pārkāpuma dēļ manuāli veiktā aizturēšana**. Pēc tam tiek piedāvāts ievadīt komentāru, lai paskaidrotu pasūtījuma aizturēšanas iemeslu. Šis komentārs parādīsies rīkā [Pasūtījumu aizturēšana](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), lai sniegtu kontekstu lietotājam, kurš pārskata aizturētos pasūtījumus, lai noteiktu, vai pasūtījumu var izlaist.

Papildus tam, ka konfigurējat kanāla opciju **Iespējot pasūtījuma pabeigšanu**, ir jākonfigurē pārkāpumu pārbaudes līdzeklis sadaļā Zvanu centra parametri. Dodieties uz **Mazumtirdzniecība** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Zvanu centra parametri**. Lapas **Zvanu centra parametri** cilnē **Aiztures** iestatiet opcijai **Pārkāpumu pārbaude** vienumu **Jā**.

Cilnē **Aiztures** arī jādefinē [aizturēšanas kodi](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), kuri tiks lietoti pasūtījumam, kas tiek manuāli vai automātiski aizturēts pārkāpuma pārbaudei. Iestatiet aizturēšanas kodus laukos **Pārkāpuma dēļ manuāli veiktās aizturēšanas kods** un **Pārkāpuma dēļ veiktās aizturēšanas kods**. Var būt noderīgi izveidot divus unikālus aizturēšanas kodus, lai lietotāji, kuri strādā ar aizturēšanas rīku, varētu viegli filtrēt un atšķirt automātiskās aiztures no manuālajām aizturēm.

Lai pārkāpumu pārbaudes līdzeklis darbotos efektīvi, ir jāiestata arī lauks **Minimālais rezultāts**. Katram pārkāpuma kritērijam un kārtulai, kas ir definēti sistēmā, ir noteikts vērtējums. Veicot pārdošanas pasūtījuma pārkāpumu pārbaudi, ja tiek konstatēta viena vai vairāku pārkāpumu atbilstība, vērtējumi tiek saskaitīti, iegūstot pasūtījuma kopējo pārkāpumu rezultātu. Ja pasūtījuma kopējais pārkāpumu rezultāts pārsniedz vērtību laukā **Minimālais rezultāts**, pasūtījums tiek automātiski aizturēts. Pēc izvēles varat lietot citus ar rezultātu saistītos laukus cilnē **Aiztures**, lai definētu e-pasta rezultātu, tālruņa rezultātu, pasta indeksa rezultātu un paplašinātā pasta indeksa rezultātu. Ja nenorādīsit vērtējumu nevienam no minētajiem statiskajiem pārkāpumu kritērijiem, definējot tos lapā **Statiski pārkāpumu dati**, sistēma tos novērtēs, izmantojot noklusējuma vērtējumu, kuru norādāt lapas **Zvanu centra parametri** cilnē **Aiztures**.

Visbeidzot, izmantojiet lauku **Pārkāpuma komentāra veids**, lai norādītu dokumenta veidu, kas ir jāizmanto, kad lietotāji ievada komentārus, manuāli aizturot pasūtījumu pārkāpumu pārskatīšanai. Visbiežāk šajā laukā ir iestatīta vērtība **Piezīme**.

## <a name="defining-fraud-criteria-and-rules"></a>Pārkāpumu kritēriju un kārtulu definēšana

Sistēma izmanto divu veidu pārkāpuma kritērijus, lai noteiktu, vai pasūtījums ir jāaiztur pārkāpuma pārskatīšanai.

- **Statiski pārkāpumu dati** izmanto noteiktu vērtību, piemēram, tālruņa numuru, kas ir iekļauts bloķēto numuru sarakstā, vai e-pasta adresi, kas ir atzīmēta, jo ir zināms, ka tā iepriekš izmantota krāpnieciskām transakcijām. Lai iestatītu statiskus pārkāpumu datus, dodieties uz **Mazumtirdzniecība** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Pārkāpums** \> **Statiski pārkāpumu dati**. Lapā **Statiski pārkāpumu dati** varat pievienot pārkāpumu kritērijus manuāli vai izmantojot datu importēšanu. Krāpnieciskajai informācijai ir pievienoti vērtējumi. Ja ir ieslēgts pārkāpumu pārbaudes līdzeklis, katrs ievadītais pārdošanas pasūtījums tiek salīdzināts ar statiskajiem datiem. Ja šie dati tiek atrasti debitora norēķinu adresē vai piegādes adresē, kas ir saistīta ar pasūtījuma virsrakstu, vai ja šie dati tiek atrasti piegādes adresēs, kuras ir saistītas ar kādu no pārdošanas pasūtījuma rindām, visu unikālo atbilstību vērtējumi tiek summēti un salīdzināti ar vērtību **Minimālais rezultāts**, lai noteiktu, vai pasūtījums ir jāaiztur.
- **Pārkāpumu kārtulas** sastāv no lietotāja definētiem mainīgajiem un nosacījumiem, kuri ir definēti attiecīgajiem mainīgajiem. Lai izveidotu kārtulas, dodieties uz **Mazumtirdzniecība** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Pārkāpums** \> **Kārtulas**. Pārkāpumu kārtulas ļauj uzņēmumam konfigurēt sarežģītāku kārtulu kopu, kas var ietvert priekšrakstus **AND** vai **OR**, lai novērtētu vairākus nosacījumus. Piemēram, lietotājs vēlas, lai pārkāpumu pārbaudes veikšanai tiktu aizturēti visi pasūtījumi no debitoriem, kuri ietilpst noteiktā debitoru grupā un kuri pasūtījuši noteiktu preci. Šajā gadījumā, lapā **Kārtulas** tiek definēti klienta un preces pārbaudes nosacījumi un tiek izmantots nosacījums AND. Pasūtījums tiek aizturēts tikai tad, ja ir spēkā abi nosacījumi un ja attiecīgajai kārtulai piešķirtā rezultāta vērtības ietekmē, pieskaitot citu tādu kārtulu rezultāta vērtību, kurai atbilst pasūtījums, pasūtījuma kopējais pārkāpumu rezultāts pārsniedz vērtību **Minimālais rezultāts**, kas ir definēta lapā **Zvanu centra parametri**.

> [!NOTE]
> Vairāku kārtulu vai pārāk sarežģītu kārtulu izmantošana ietekmē sistēmas veiktspēju pārdošanas pasūtījumu iesniegšanas laikā. Pārkāpuma pārbaudes līdzeklis nav optimizēts darbam ar lielu statisko pārkāpumu datu ierakstu skaitu un daudzām aktīvajām kārtulām. Atcerieties, ka katra kārtula tiek novērtēta, kad zvanu centra lietotāji atlasa vienumu **Iesniegt** pārdošanas pasūtījuma izveides laikā. Kārtulas tiek novērtētas, salīdzinot tās ar pārdošanas pasūtījuma galveni un visām pasūtījuma rindām. Jo vairāk kārtulu ir jāapstrādā un jo sarežģītāki ir kārtulu priekšraksti, jo ilgāks laiks ir nepieciešams to apstrādei. Ja pasūtījumā ir daudz rindu vienumu un ir daudz aktīvo kārtulu un statisko datu ierakstu, automātiskā visu datu pārskatīšana un pārbaude un pārkāpuma vērtējuma aprēķināšana var būtiski pazemināt veiktspēju. Organizācijām, kas lieto šo līdzekli, pirms jebkādu kārtulu vai statisko pārkāpumu kritēriju izmaiņu ieviešanas ražošanas vidē vienmēr ir jāpārbauda pasūtījumu iesniegšanas apstrādes laiks un jāpārliecinās, ka tas ir pieņemams.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Pārkāpumu pārbaudes veikšanai aizturētu pasūtījumu identificēšana

Ja zvanu centra lietotāji iesniedz pārdošanas pasūtījumu, ja pasūtījums atbilst pārkāpumu kritērijiem vai kārtulām un ja rezultāts pārsniedz minimālo vērtību, lietotāji saņem brīdinājuma ziņojumu, kurā norādīts, ka pasūtījums ir aizturēts. Lietotāji var aizvērt šo ziņojumu, jo tas ir tikai informatīvs. Lietotāji pēc izvēles var paziņot šo informāciju debitoram. Uzņēmumam ir jānosaka procedūra, kas jāievēro lietotājiem šādā situācijā.

Pasūtījums tiek saglabāts, tas tiek atzīmēts ar karodziņu **Neapstrādāt**. Šis karodziņš palīdz nodrošināt, ka pasūtījumu nevar nosūtīt uz noliktavu. Lietotāji jebkurā laikā var apskatīt karodziņa **Neapstrādāt** iestatījumu jebkuram pārdošanas pasūtījumam lapā **Detalizēts statuss**. Šo lapu var atvērt no lapām **Visi pārdošanas pasūtījumi** un **Klientu apkalpošana**. Sistēma arī atjaunina pasūtījumam vērtību laukā **Detalizēts statuss** iestatot vienumu **Aizturēšanu pārkāpuma dēļ**.

Lai skatītu un pārvaldītu pasūtījumus, kas ir aizturēti pārkāpuma pārskatīšanai, dodieties uz **Mazumtirdzniecība** \> **Debitori** \> **Pasūtījumu aizturēšana**. Lapā **Pasūtījumu aizturēšana** atlasiet ierakstu sarakstā un pēc tam noklikšķiniet uz **Pasūtījuma aizturēšana**, lai atvērtu detalizētāku skatu, kurā ietverta informācija par aizturēšanas iemeslu. Kopsavilkuma cilnē **Detalizēta informācija par pārkāpumu** varat skatīt sistemātiskos pārkāpumu kritērijus, kuriem tika noteikta atbilstība attiecīgā pasūtījuma gadījumā, un izmantotos vērtējumus. Ja pasūtījums tika aizturēts manuāli, varat pārskatīt visus komentārus, kurus ievadīja lietotājs, kas aizturēja pasūtījumu, apskatot kopsavilkuma cilnes **Piezīmes** sadaļu **Pārkāpuma piezīmes**.

Lai iegūtu vairāk informācijas par to, kā darboties ar pasūtījumu aizturēšanu, skatiet sadaļu [Pasūtījumu aizturēšana](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).
