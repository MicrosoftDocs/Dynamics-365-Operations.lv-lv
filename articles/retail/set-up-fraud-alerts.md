---
title: "Pārkāpumu brīdinājumu iestatīšana"
description: "Šajā tēmā izskaidrots, kā iestatīt kārtulas, lai brīdinātu klientu apkalpošanas pārstāvjus par potenciāli krāpniecisku informāciju, kad tiek apstrādāti pasūtījumi. Var definēt īpašus izmantošanai paredzētus kodus, lai automātiski vai manuāli aizturētu aizdomīgus pasūtījumus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Iestatīt pārkāpumu brīdinājumus

[!INCLUDE [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt kritērijus un kārtulas, lai aizturētu potenciāli krāpnieciskus pārdošanas pasūtījumus turpmākai pārskatīšanai. Pārkāpuma pārskatīšanas funkcionalitāte tiek izmantota, lai noteiktu pārdošanas pasūtījumā ietvertās informācijas derīgumu. Ja, pamatojoties uz organizācijas pārkāpuma kritērijiem un kārtulām, pārdošanas pasūtījumā ietvertā informācija tiek atzīta par apšaubāmu, pasūtījumu var aizturēt turpmākai pārskatīšanai, ko veic administrators.

> [!NOTE]
> Šo līdzekli var lietot tikai tad, ja tiek izmantota mazumtirdzniecības zvanu centra kanāla pārdošanas pasūtījumu apstrāde. 

Pēc zvanu centra kanāla definēšanas ir jāiestata opcijas **Iespējot pasūtījuma pabeigšanu** vērtība **Jā**. Kad ir iespējota pasūtījuma pabeigšana, lietotāji var skatīt pasūtījuma kopsavilkumu un noklikšķināt uz **Iesniegt**, lai pabeigtu pasūtījumu. Lietotājiem ir pieejamas arī iespējas manuāli aizturēt pārdošanas pasūtījumu pārkāpuma pārskatīšanai. Zvanu centra lietotāja ievadītie pārdošanas pasūtījumi iesniegšanas laikā tiek apstrādāti, izmantojot pārkāpuma pārbaudes kārtulas un kritērijus.

Lai pārbaudītu, vai pasūtījums ir jāaiztur pārkāpuma pārskatīšanai, sistēmā tiek izmantoti divu veidu pārkāpuma kritēriji.

-   **Statiskās kārtulas** izmanto noteiktu vērtību, piemēram, tālruņa numuru, kas ir pievienots bloķēto sarakstam, vai e-pasta adresi, kas ir atzīmēta kā iepriekš izmantota krāpnieciskām transakcijām. Lapā **Statiski pārkāpumu dati** var manuāli ievadīt vai importēt informāciju par pārkāpumiem, kam ir pievienoti vērtējumi. Ja ir ieslēgta pārkāpuma pārbaude, katrs ievadītais pārdošanas pasūtījums tiek salīdzināts ar statiskajiem datiem. Ja šie dati tiek atrasti debitora norēķinu vai piegādes adresē vai pārdošanas rindā norādītajā piegādes adresē, tiek summēti visu unikālo atbilstību vērtējumi.  
-   **Dinamiskās kārtulas** ir veidotas no mainīgajiem un nosacījumiem, kas ir definēti šiem mainīgajiem. Izmantojot dinamiskās kārtulas, var pārbaudīt citus kritērijus, kas nav definēti statiskajās kārtulās. Izmantojot sarežģītākus priekšrakstus UN/VAI, var lietot vairākus nosacījumus, lai noteiktu, vai iesniegtais pārdošanas pasūtījums atbilst kārtulas kritērijam. Piemēram, ja lietotājs vēlas pārkāpuma pārskatīšanai aizturēt visus pasūtījumus no debitoriem, kas ir saistīti ar noteiktu debitoru grupas vērtību un kas ir pasūtījuši noteiktu preci, lapā **Kārtulas** ir jādefinē debitora pārbaudes un preces pārbaudes nosacījumi ar priekšrakstu UN. Pasūtījums tiek aizturēts pārkāpuma pārskatīšanai tikai tad, ja abi nosacījumi ir patiesi un pēc kārtulai piešķirtā vērtējuma vērtības pieskaitīšanas pasūtījuma kopējā pārkāpuma vērtība pārsniedz minimālo pārkāpuma vērtību, kas ir definēta zvanu centra parametros.

Zvanu centra lietotājs var arī manuāli ievieto pasūtījumu pārkāpuma dēļ veiktas aizturēšanas rindā. Ja pasūtījumu ievadījušais lietotājs uzskata, ka pasūtījumu veikušais debitors, iespējams, ir aizdomīgs, un vēlas, lai kāds cits pārskatītu pasūtījuma derīgumu pirms tā apstrādes, pasūtījumu ievadījušais lietotājs var arī izvēlēties opciju **Pārkāpuma dēļ manuāli veiktā aizturēšana**, kas ir pieejama lapas **Pārdošanas pasūtījuma kopsavilkums** nolaižamajā izvēlnē **Aiztures** (šī opcija tiek parādīta pēc pasūtījuma funkcijas **Pabeigt** izsaukšanas). Lietotājam tiek prasīts ievadīt piezīmi, lai plašāk paskaidrotu, kāpēc viņam šķiet, ka pasūtījums varētu būt krāpniecisks, lai sniegtu pārskatītājam papildu kontekstu.

Visi pasūtījumi, kas ir aizturēti, veicot manuālu aizturēšanu pārkāpuma dēļ vai sistēmā aprēķinot pārkāpuma vērtējumus, tiek rādīti lapā **Pasūtījumu aizturēšana**, kur pasūtījumu var pārskatīt un pēc tam atcelt vai nodot apstrādei.

> [!NOTE]
> Vairāku kārtulu vai pārāk sarežģītu kārtulu lietošana izraisa zemu sistēmas veiktspēju pārdošanas pasūtījumu iesniegšanas laikā. Pārkāpuma brīdinājuma līdzeklis nav optimizēts darbam ar lielu statisko pārkāpumu datu ierakstu skaitu un daudzām aktīvajām kārtulām. Ir svarīgi ņemt vērā, ka, iesniedzot zvanu centra pārdošanas pasūtījuma ierakstu, tiek novērtēta katra kārtula. Kārtulas tiek novērtētas, salīdzinot tās ar pārdošanas pasūtījuma galveni un visām pasūtījuma rindām. Jo vairāk kārtulu ir jāapstrādā un jo sarežģītāki ir kārtulu priekšraksti, jo ilgāks laiks ir nepieciešams apstrādei. Ja pasūtījumā ir daudz rindu vienumu un ir definēts daudz aktīvo kārtulu un statisko datu ierakstu, šī sistemātiskā visu datu pārskatīšana un pārbaude un pārkāpuma vērtējuma aprēķināšana var būtiski pazemināt veiktspēju.  Organizācijām, kas lieto šo līdzekli, pirms jebkādu kārtulu vai statisko pārkāpumu kritēriju izmaiņu ieviešanas ražošanas vidē vienmēr ir jāpārbauda pasūtījumu iesniegšanas apstrādes laiks un jāpārliecinās, ka tas ir pieņemams.

