---
title: Darbs ar līdzekļu iestatījumiem
description: Šajā rakstā ir izskaidrots, kā iestatīt elektronisko rēķinu izrakstīšanas līdzekļus.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 23466a53bb8ba597503aaa12d41395fc82b9f14e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904330"
---
# <a name="work-with-feature-setups"></a>Darbs ar līdzekļu iestatījumiem

[!include [banner](../includes/banner.md)]

Lai iestatītu elektronisko failu ģenerēšanu un citus apstrādes soļus (piemēram, digitāli parakstīšanas failus, iesniedziet tos valsts tīmekļa pakalpojumam un saņem atbildi vai glabājiet tos), iestatiet apstrādes konveijeru, piemērojamības noteikumus un mainīgos elektronisko rēķinu izrakstīšanas funkcijām.

Iestatīšanas informācija ir apvienota līdzekļa *iestatīšanas koncepcijā*, un to var izveidot, dzēst, koriģēt. Elektronisko rēķinu izrakstīšanas funkciju pabeigtām versijām ir iespējams apskatīt arī informāciju.

Varat izveidot tik daudz funkciju iestatījumu krājumu, cik nepieciešams, lai definētu dažādus scenārijus elektronisko failu ģenerēšana, apstrādei un saņemšanai. Kaut arī šiem līdzekļu iestatīšanas krājumiem ir neatkarīga apstrādes darbības un izpildes nosacījumi, tie tiek izveidoti kā daļa no viena elektronisko rēķinu izrakstīšanas funkcijas un pārmantot tās dzīves cikla un izvietošanas procesu.

## <a name="add-a-feature-setup"></a>Pievienot līdzekļu iestatījumus

1. Piesakieties savā Regulēšanas konfigurācijas pakalpojuma (RCS) kontā.
2. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Elektronisko rēķinu **izrakstīšanas funkciju** lapā atlasiet elektronisko rēķinu izrakstīšanas līdzekļa versiju, kuras statuss ir **Melnraksts**.
4. **Cilnē Iestatījumi** atlasiet **Pievienot**.
5. **Nolaižamajā dialogā Izveidot** līdzekļu iestatījumus lauku grupā **Jauns** atlasiet vienu no šīm opcijām:
 
    - **Pielāgoti** iestatījumi – izveidojiet jaunu funkcionalitātes iestatījumu, kurā ir tukši kanāli, tukšs apstrādes konveijera saraksts, tukša sadaļa piemērojamības noteikumiem un mainīgo noklusējuma kopa atkarībā no iestatīšanas tipa.
    - **No funkciju iestatījumiem** – izveidojiet citas funkcionalitātes iestatījumu kopiju pašreizējā elektronisko rēķinu izrakstīšanas līdzekļa tvērumā.

6. Ja pēdējā solī **atlasījāt** opciju Pielāgots iestatījums, ievadiet līdzekļa iestatījuma krājuma nosaukumu un aprakstu un **pēc** tam lauku grupā Iestatījums atlasiet vienu no šīm opcijām:

    - **Konveijera** apstrāde – izvēlieties šo opciju, lai izveidotu un apstrādātu izejošos elektroniskos dokumentus. Šim iestatījuma tipam sistēma izveido tukšu konveijera saraksta apstrādi, tukšu sadaļu piemērojamības noteikumiem un mainīgo noklusēto kopu. Nevarēsit strādāt ar kanāliem ienākošajiem elektroniskajiem dokumentiem.
    - **Datu kanāls** – Microsoft Dynamics atlasiet šo opciju, lai iestatītu saņemšanas ienākošo elektronisko dokumentu saņemšanas procesu no viena no definētajiem kanāliem un pārietu tieši uz 365 Finansēm Dynamics 365 Supply Chain Management vai bez papildu darbībām. Šim iestatījuma tipam sistēma izveido iepriekš definētu parametru sarakstu datu kanāliem, tukšu sadaļu piemērojamības noteikumiem un noklusēto mainīgo kopu. Apstrādes konveijerā nevarēsit pievienot nekādas darbības.
    - **Datu kanāls un apstrādes konveijers** – šis iestatījuma tips ir līdzīgs datu **kanāla iestatīšanas** tipam. Tomēr pirms ienākošā elektroniskā dokumenta nosūtīšanas finanšu vai piegādes ķēžu pārvaldībai, varat iestatīt papildu darbības apstrādes konveijerā.

7. Ja pēdējā **solī** **atlasījāt** datu kanāla vai datu kanāla un apstrādes konveijera opciju, **laukā** Datu kanāla atlase ir jāatlasa kanāls, ar kuru integrēt kanālu.
8. Atlasiet **Izveidot**.

Pēc tam, kad ir izveidots līdzekļu iestatījums, varat atlasīt Rediģēt **,** lai to konfigurētu.

## <a name="edit-a-feature-setup"></a>Rediģēt līdzekļa iestatījumus

Atkarībā no funkcionalitātes iestatījuma tipa, varat konfigurēt izejošo elektronisko failu izveides procesu un iesniegt tos ārējiem kanāliem vai saņemt ienākošos dokumentus un nodot tos programmai Finanses vai Piegādes ķēdes pārvaldība.

### <a name="data-channel"></a>Datu kanāls

Datu *kanāls paņem* elektronisko failu un vai nu to apstrādā, vai pāriet tieši uz Finanšu vai Piegādes ķēžu pārvaldību. Šī opcija nav pieejama apstrādes konveijera tipa līdzekļu **iestatījumiem**.

Lai iestatītu datu kanālu, ievadiet kanāla nosaukumu. Pēc tam definējiet parametrus, pamatojoties uz atlasīto kanāla tipu. Datu kanāla identifikatoram ir jāatbilst mainīgajam, kas ir izveidots īpaši datu kanāla identificēšanai. Tas tiks izmantots kā atsauce Finanšu vai Piegādes ķēžu pārvaldībā.

Cilnē Pielikumu **filtrs jums jādefinē** filtru kopa, lai no kanāla iegūtu noteiktus failus. Varat izveidot vairākas rindas, ja vēlaties, lai failiem būs dažādi failu nosaukumu paplašinājumi vai arī faili jāapstrādā atšķirīgi atkarībā no faila nosaukuma. Šie ir galvenie parametri:

- **Nosaukums** – ievadiet nosaukumu failam, uz kuru sistēma atsaucas apstrādes laikā. Finanšu un piegādes ķēdes pārvaldības programmās jūs varēsiet redzēt failus iesniegšanas žurnālā.
- **Filtrs** - Nosakiet filtru, lai izvēlētos failus.
- **Nav** obligāti - ja šī izvēles rūtiņa ir notīrīta, fails ir nepieciešams. Šajā gadījumā sistēma parādīs kļūdas ziņojumu, ja kanālos nav failu, kas atbilst filtram. Šis parametrs ir attiecināms uz e-pasta ziņojumiem.

Ja kanāls ir pastkastīte un ienākošais e-pasta ziņojums satur vairākus pielikumus, varat konfigurēt noteikumus, lai definētu, kā pakalpojumam vajadzētu apstrādāt pielikumus. Pakalpojums var apsvērt katru pielikumu atsevišķu elektronisko rēķinu vai arī to var uzskatīt par vienu pielikumu kā galveno rēķinu un visus citus pielikumus kā papildinājumus.

### <a name="processing-pipeline"></a>Apstrādes konveijers

Apstrādes *konveijers* ir darbību kopa *,* kas tiek secīgi palaista līdz to veiksmīgai apstrādei. Varat izmantot apstrādes konveijeru, lai iestatītu procesu elektronisko failu ģenerēšanai un citu darbību veikšanai (piemēram, digitāli parakstīšanas failus, iesniegt tos ārējiem Tīmekļa pakalpojumiem un parsēt atbildi, kā arī saņemt un apstrādāt ienākošos dokumentus).

Darbību saraksts ir iepriekš definēts. Jūs variet izmantot **pogas** Jauns **un** Dzēst, lai norādītu darbību kombināciju, kas loģiski definē nepieciešamo procesu dokumentu iesniegšanai vai saņemšanai.

Darbību secība ir svarīga. Secību var pielāgot, lietojot pogas Uz **augšu** un **Uz** leju.

Katrai darbībai ir parametru kopa, ko var konfigurēt vai koriģēt. Noteikta parametru kopa ir atkarīga no darbības tipa.

- **Darbība** – atlasiet darbības tipu.
- **Darbības** nosaukums – ievadiet darbības nosaukumu. Šis nosaukums tiks parādīts iesniegšanas žurnālos un ziņojumos Finanšu un piegādes ķēžu pārvaldības programmās.
- **Apraksts** – sniedziet sīkāku informāciju par procesa darbības mērķi.
- **Aktivizējiet atkārtotu** mēģinājumu - Ja jūs atzīmējiet šo izvēles rūtiņu, **·** **jūs variet izvēlēties darbību laukā Atkārtot darbību un konfigurēt papildu parametrus cilnē Atkārtot parametrus.**

    Atkārtotā funkcionalitāte ļauj jums konfigurēt pakalpojuma darbību, ja noteiktu darbību nevar palaist. Piemēram, ja ārējais Web pakalpojums, ar kuru mēģināt pievienoties, nereaģē, var norādīt, cik reizes sistēmai ir atkārtoti jāveic savienojuma mēģinājums, kādā intervālā un kādā veidā darbība apstrādes konveijerā.

- **Eksporta rezultāti** – šo izvēles rūtiņu var atzīmēt vienai darbībai *apstrādes* konveijerā. Elektronisko failu, ko darbība rada Finanšu vai Piegādes ķēžu pārvaldības programmā, pēc tam var eksportēt no Elektronisko **dokumentu iesniegšanas žurnāla** lapas.

### <a name="applicability-rules"></a>Lietojamības kārtulas

*Piemērojamības* kārtulas ir konfigurējamas klauzulas, kas nodrošina kontekstu elektronisko rēķinu izrakstīšanas funkciju izpildīšanai, izmantojot iespēju Iestatīt Elektronisko rēķinu izrakstīšanu.
Biznesa dokumentos, kas ir iesniegti no finanšu vai piegādes ķēžu pārvaldības elektronisko rēķinu izrakstīšanai, nav īpašas atsauces, kas ļauj iestatīt elektronisko rēķinu izrakstīšanas iespēju, lai izsauktu noteiktu elektronisko rēķinu izrakstīšanas funkcijas versiju un noteiktu funkcionalitātes iestatīšanas elementu, lai apstrādātu iesniegšanu. Tomēr, kad biznesa dokuments ir pareizi konfigurēts, tas ietver nepieciešamos elementus, kas aktivizēs elektronisko rēķinu izrakstīšanu, lai noteiktu, kura elektronisko rēķinu izrakstīšanas funkcijas versija un apstrādes konveijers jāatlasa un jāpalaiž.

Piemērojamības noteikumi ļauj Elektronisko rēķinu izrakstīšanas pakalpojumam atrast precīzus elektronisko rēķinu izrakstīšanas līdzekļus, kas jāizmanto iesniegšanas iesniegšanai. Lai atrastu pareizās funkcijas, konteksta **lauki** no iesniegtā biznesa dokumenta tiek saskaņoti ar piemērojamības kārtulu klauzulām.

Varat strādāt ar piemērojamības kārtulām šādos veidos:

- Atlasiet **Jauns**, lai pievienotu jaunu klauzulu piemērojamības kārtulu kopai.
- Atlasiet **Dzēst,** lai dzēstu klauzulu.
- Atlasiet vairākus ierakstus un lietojiet pogu Grupa **vai** Atkopšana **·**, lai izveidotu krājumu vai loģisko priekšrakstu kombināciju. Piemēram, atlasiet rindas, kuras vēlaties grupēt, un pēc tam atlasiet klauzulu **Grupa**. Kad klauzulas tiek grupētas, režģim tiek pievienota jauna kolonna. Šī kolonna norāda grupētās klauzulas loģisko operatoru. Tiek atbalstīti šādi operatoru tipi:

    - Equal
    - Not equal
    - Lielāks par/mazāks par
    - Lielāks par vai vienāds/mazāks par vai vienāds
    - Contains
    - Sākt ar

    > [!NOTE]
    > Atgrupējot klauzulu, vienmēr sāciet no iekšējā grupēšanas līmeņa.

### <a name="variables"></a>Mainīgie

*Mainīgie* dod jums lielāku elastīgumu, iestatot apstrādes konveijeru un datu plūsmu starp darbībām. Varat atsaukties uz mainīgo dažos darbības parametros, lai īslaicīgi saglabātu datus vai elektroniskos failus. Daži mainīgie tiek lietoti, lai padotu datus starp Finanšu vai piegādes ķēdes pārvaldības programmām un Elektronisko rēķinu izrakstīšanas pakalpojumu.

Sistēma pēc noklusējuma izveido dažus mainīgos. Piemēram, businessDocumentDataModel **mainīgais ietver biznesa datus JavaScript objekta notācijas (JSON) struktūrā,** kas tiek iekļautas izsaukumu no pievienotās lietojumprogrammas iesniegšanas procesa laikā.

Pieejami šādi mainīgo tipi:

- **Konstante** – konteiners pagaidu datu glabāšanai, kas tiek izmantots konveijera darbību apstrādē.
- **No klienta** - mainīgā saturs tiek iegūts no Dynamics 365 klienta, kad tiek palaists iesniegšanas process.
- **Klientam** - mainīgā saturs ir padarīts pieejams importēšanai dynamics 365 klientā, kad tiek palaists iesniegšanas process.
- **Datu tips** – atlasiet datu tipu informācijai, kas tiek glabāta mainīgajā.

### <a name="parameters"></a>Parametri

Opcija **Atspējot biznesa datu samazināšanu tiek** izmantota, lai optimizētu biznesa datu lietderīgās slodzes struktūru, kas tiek iegūta finanšu vai piegādes ķēdes pārvaldības programmā elektroniskā dokumenta iesniegšanas laikā. Optimizācija palīdz samazināt datus, kas ir pieejami elektronisko rēķinu izrakstīšanas pakalpojumā, lai tālāku pārvēršanu nepieciešamajā elektroniskajā failā. Noklusējuma vērtība ir **Nē**.

- **Jā** — finanšu vai piegādes ķēžu pārvaldība nosūtīs **JSON** **failu** elektronisko pārskatu modulī definētās rēķinu modeļa vai finanšu modeļa (Brazīlijai) **struktūrai**. Visi modeļa elementi ir aizpildīti ar biznesa datiem programmas pusē neatkarīgi no galīgās elektroniskā faila struktūras. Modeļos parasti ir vairāk biznesa datu nekā nepieciešama mērķa faila struktūra, un var būt nepieciešams vairāk laika, lai ģenerētu šos datus lietojumprogrammā. Šai opcijai **nepieciešama vērtība Jā** retos gadījumos, kad vēlaties ģenerēt dažādus izvades failus vienā elektroniskā rēķina izrakstīšanas funkcijai un funkcionalitātes iestatījumam. Jā vērtība ir **noderīga**, ja novērsīsit scenārijus, elektronisko failu struktūru un biznesa datu pabeigtību.
- **Nē** – Finanses un piegādes ķēžu pārvaldība veiks pirmo zvanu pakalpojumam bez uzņēmējdarbības datiem. Šī zvana mērķis ir iegūt informāciju par elektronisko pārskatu (ER) konfigurāciju, kas tiks izmantota elektronisko failu pārveidošanai apstrādes konveijerā. Šī informācija tiek atgriezta lietojumprogrammā, kas to izmanto, lai noteiktu biznesa datu apakškopu, kurai jābūt iekļautai Rēķina modeļa vai Finanšu modeļa (Brazīlijas) struktūras **JSON** **failā**. Šīs opcijas **vērtība palīdz** samazināt biznesa datu apjomu, ko lietojumprogramma iesniedz pakalpojumam, jo programma var iesniegt tikai tos biznesa datus, kas ir nepieciešami veiksmīgai elektroniskā faila ģenerēšanai.

### <a name="validate-a-feature-setup"></a>Līdzekļa iestatījumu pārbaude

Var veikt pārbaudi, lai pārbaudītu visas konfigurācijas konsekvenci. Piemēram, ja obligāts parametrs darbībai ir atstāts tukšs, apstiprināšana nosaka šo neatbilstību, un jūs saņemat brīdinājuma ziņojumu.

- Līdzekļa **versijas iestatījuma** lapā darbības rūtī atlasiet **Pārbaudīt**.

## <a name="delete-a-feature-setup"></a>Līdzekļa iestatījumu dzēšana

1. Elektronisko rēķinu **izrakstīšanas funkciju** lapā atlasiet elektronisko rēķinu izrakstīšanas līdzekļa versiju, kuras statuss ir **Melnraksts**.
2. **Cilnē Iestatījumi** atlasiet **Dzēst**.
3. Parādās ziņojuma lodziņā atlasiet Jā, lai **apstiprinātu**, ka vēlaties dzēst līdzekļu iestatījumus.
