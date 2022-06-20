---
title: Kvalitātes pasūtījumi
description: Šajā rakstā ir aprakstīts, kā manuāli vai automātiski izveidot kvalitātes pasūtījumus un kā strādāt ar tiem, lai veiktu pārbaudes un ierakstītu pārbaužu rezultātus sistēmā Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb7ab1de0fb4d93ed18f1862630c1af7af7f3095
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857784"
---
# <a name="quality-orders"></a>Kvalitātes pasūtījumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā manuāli vai automātiski izveidot kvalitātes pasūtījumus un kā strādāt ar tiem, lai veiktu pārbaudes un ierakstītu pārbaužu rezultātus sistēmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="automatically-created-quality-orders"></a>Automātiski izveidoti kvalitātes pārbaudes pasūtījumi

Sistēmu var konfigurēt tā, lai tā automātiski izveido kvalitātes pārbaudes pasūtījumus, pamatojoties uz krājumu paraugu ņemšanas noteikumiem. Papildinformāciju skatiet [Kvalitātes pārvaldības krājumu iztveršana](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Manuāla kvalitātes pārbaudes pasūtījumu izveide

Lai manuāli izveidotu kvalitātes pārbaudes pasūtījumu, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.
1. Atlasiet **Jauns**.
1. Dialoglodziņā **Kvalitātes pārbaudes pasūtījumi** laukā **Atsauces tips** atlasiet krājuma atsauci, ar ko būs saistīts jūsu kvalitātes pārbaudes pasūtījums. Atlasīšanai pieejamo atsauču tipu aprakstu skatiet tālāk šī raksta [sadaļā Kvalitātes](#ref-types) pasūtījuma atsauces tipi.

    > [!NOTE]
    > Krājumiem, kas saistīti ar atlasīto atsauci, jābūt pieejamiem. Ja atsauču tipa, daudzuma un krājumu dimensiju kombinācijai, ko atlasāt, nav pieejami krājumi, saņemsit kļūdas ziņojumu.

1. Izpildiet vienu no tālāk aprakstītajām darbībām, ņemot vērā laukā **Atsauces tips** atlasīto vērtību.

    - Ja atlasījāt **Krājums**, papildu informācija par atsauci nav nepieciešama.
    - Ja atlasījāt **Pārdošana** vai **Pirkšana**, norādiet šādu informāciju:

        - **Konta atlase** – atsauce uz debitora vai kreditora numuru.
        - **Atsauces numurs** – atsauce uz pārdošanas pasūtījuma vai pirkšanas pasūtījuma numuru.
        - **Atsauces laidiens** – atsauce uz noteiktu pārdošanas pasūtījuma rindu vai pirkšanas pasūtījuma rindu.

    - Ja laukā **Atsauces numurs** atlasījāt **Ražošana**, **Karantīna** vai **Līdzprodukta ražošana**, atsauce būs uz ražošanas pasūtījumu, partijas pasūtījumu vai karantīnas pasūtījuma numuru.
    - Ja atlasījāt **Maršruta operācija**, norādiet šādu informāciju:

        - **Atsauces numurs** – atsauce uz ražošanas pasūtījuma vai partijas pasūtījuma numuru.
        - **Operācija Nr.** – Atsauce uz noteiktu maršruta operācijas numuru.
        - **Operācija** – Atsauce uz noteiktu maršruta operāciju.
        - **Resurss** – atsauce uz konkrētu resursu, kas jāizmanto ar maršruta operāciju.

1. Laukā **Testa grupa** atlasiet veicamo testu grupu.
1. Laukā **Daudzums** ievadiet testējamo krājumu daudzumu.
1. Sadaļā **Krājumu dimensijas** ievadiet jebkuras papildu krājumu dimensijas, kas nepieciešamas atlasītajam krājumam.
1. Atlasiet **Labi**.

Kad kvalitātes pārbaudes pasūtījums ir izveidots, var sākt pārbaudīt krājumu un reģistrēt pārbaužu rezultātus. Papildinformāciju par to, kā reģistrēt un apstiprināt testa rezultātus, skatiet sadaļā [Preču kvalitātes pārbaude](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Kvalitātes pārbaudes pasūtījuma atsauču tipi

Kvalitātes pārbaudes pasūtījumi tiek izmantoti, lai izsekotu detalizētu informāciju par pārbaužu un testa rezultātiem konkrētam krājumam jūsu noliktavā. Kvalitātes pārbaudes pasūtījumā jābūt iekļautai atsaucei, kas parāda testējamā krājuma avotu. Kvalitātes pārbaudes pasūtījumi var būt saistīti ar sekojošo atsauces tipu:

- **Krājumi** – šis atsauces tips norāda, ka pārbaudīsiet rīcībā esošos krājumus. Šī tipa pārbaudes parasti ir nejaušas vai neplānotas un tiek veiktas, kad noliktavas darbinieks konstatē problēmu.
- **Pārdošana** – šis atsauces tips norāda, ka tiek pārbaudīti krājumi, kas attiecas uz noteiktu pārdošanas pasūtījumu. Šāda veida pārbaudes parasti ir saistītas ar klienta specifikācijām vai analīzes sertifikāta (CoA - certificate of analysis) izveidi, kas ir jāiesniedz klientam kā sūtījuma daļa. (Dažreiz CoA ir saukts arī par atbilstības sertifikātu \[CoC - certificate of compliance\].)
- **Pirkšana** – šis atsauces tips norāda, ka tiek pārbaudīti krājumi, kas attiecas uz noteiktu pirkšanas pasūtījumu. Šāda veida pārbaudes bieži tiek izmantotas, lai pārbaudītu ienākošos preču krājumus, pirms tās tiek nodotas noliktavā vai patērētas ražošanas procesos.
- **Ražošana** – šis atsauces tips norāda, ka tiek pārbaudīti krājumi, kas attiecas uz noteiktu ražošanas pasūtījumu. Šāda veida pārbaudes bieži tiek izmantotas, lai pārbaudītu pabeigto preču krājumus, pirms tās tiek nodotas noliktavā.
- **Karantīns** – šis atsauces tips norāda, ka tiek pārbaudīti krājumi, kas attiecas uz noteiktu karantīnas pasūtījumu. Karantīnas pasūtījumi ir speciāls pasūtījuma tips, kas izseko krājumus savā noliktavā, vai arī atsekotā apgabalā jūsu noliktavā. Šāda veida pārbaudes bieži tiek izmantotas, lai pārbaudītu preces, kuras debitors ir atgriezis vai kas ir novietotas karantīnā turpmākai analīzei. Karantīnas pasūtījumus var veidot no kvalitātes pārbaudes pasūtījumiem. Alternatīvi tos var izveidot no citiem avotiem, un pēc tam kvalitātes pārbaudes pasūtījumi var saistīties ar karantīnas pasūtījumiem.
- **Maršruta operācija** – šis atsauces tips norāda, ka tiek pārbaudīti krājumi, kas attiecas uz noteiktu maršruta darbību ražošanas pasūtījumam. Šī tipa pārbaudes parasti tiek izmantotas, lai analizētu produkta nepabeigto darbu (NP) pirms tas pāriet uz nākamo ražošanas procesa darbību.
- **Līdzprodukta ražošana** – šis atsauces tips norāda, ka tiek pārbaudīti krājumi, kas attiecas uz ražošanas pasūtījuma līdzproduktu. Šāda veida pārbaudes parasti tiek izmantotas, lai pārbaudītu partijas pasūtījuma līdzproduktu pirms līdzprodukta pievienošanas krājumiem.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Skatīt un izveidot kvalitātes pārbaudes pasūtījumus no dažādām sistēmas daļām

Kvalitātes pārbaudes pasūtījumus var izveidot manuāli. Alternatīvi tos var izveidot automātiski, balstoties uz jūsu definētām kvalitātes saistībām. Plašāku informāciju par to, kā izveidot un pārvaldīt automātisku kvalitātes pārbaudes pasūtījumu izveidi, skatiet [Kvalitātes saistības](quality-associations.md).

Varat izmantot kvalitātes pārbaudes pasūtījuma lapu, lai manuāli izveidotu jaunu kvalitātes pārbaudes pasūtījumu vai skatītu kvalitātes pārbaudes pasūtījuma statusu, kas attiecas uz citu ierakstu. Ir vairāki veidi, kā piekļūt kvalitātes pārbaudes pasūtījuma lapai.

### <a name="from-the-quality-orders-page"></a>No kvalitātes pārbaudes pasūtījumu lapas

Lai manuāli izveidotu kvalitātes pārbaudes pasūtījumus un skatītu visus esošos kvalitātes pārbaudes pasūtījumus, dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pasūtījumi**. Šajā rakstā pārējās sadaļās ir sniegta papildinformācija par to, kā strādāt ar Kvalitātes **pasūtījumu** lapu.

### <a name="from-sales-orders"></a>No pārdošanas pasūtījumiem

Lai strādātu ar kvalitātes pārbaudes pasūtījumiem, kas ir saistīti ar jūsu pārdošanas pasūtījumiem, dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi** un pēc tam izpildiet jebkuru no tālāk minētajām darbībām.

- Atveriet pārdošanas pasūtījumu vai atlasiet to režģī. Pēc tam darbību rūtī cilnē **Izdot un iepakot**, grupā **Kvalitātes pārvaldība** atlasiet **Kvalitātes pārbaudes pasūtījumi**, lai atvērtu lapu **Kvalitātes pārbaudes pasūtījumi**. Tur ir iespējams apskatīt, izveidot vai atjaunināt ar pārdošanas pasūtījumu saistītos kvalitātes pārbaudes pasūtījumus.
- Atveriet pārdošanas pasūtījumu un pēc tam cilnē **Virsraksts** atlasiet kopsavilkuma cilni **Vispārīgi**. Lauks **Kvalitātes pārbaudes pasūtījuma statuss** rāda visu ar pārdošanas pasūtījumu saistīto kvalitātes pārbaudes pasūtījumu vispārējo statusu.
- Atveriet pārdošanas pasūtījumu un pēc tam cilnē **Rindas** atlasiet kopsavilkuma cilni **Pārdošanas pasūtījuma rindas**. Kolonna **Kvalitātes pārbaudes pasūtījuma statuss** rāda katras pārdošanas pasūtījuma rindas statusu.

### <a name="from-purchase-orders"></a>No pirkšanas pasūtījumiem

Lai strādātu ar kvalitātes pārbaudes pasūtījumiem, kas ir saistīti ar jūsu pirkšanas pasūtījumiem, dodieties uz **Iepirkums un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi** un pēc tam izpildiet jebkuru no tālāk minētajām darbībām.

- Atveriet pirkšanas pasūtījumu vai atlasiet to režģī. Pēc tam darbību rūtī cilnē **Saņemt**, grupā **Kvalitātes pārvaldība** atlasiet **Kvalitātes pārbaudes pasūtījumi**, lai atvērtu lapu **Kvalitātes pārbaudes pasūtījumi**. Tur ir iespējams apskatīt, izveidot vai atjaunināt ar pirkšanas pasūtījumu saistītos kvalitātes pārbaudes pasūtījumus.
- Atveriet pirkšanas pasūtījumu un pēc tam cilnē **Virsraksts** atlasiet kopsavilkuma cilni **Vispārīgi**. Lauks **Kvalitātes pārbaudes pasūtījuma statuss** rāda visu ar pirkšanas pasūtījumu saistīto kvalitātes pārbaudes pasūtījumu vispārējo statusu.
- Atveriet pirkšanas pasūtījumu un pēc tam cilnē **Rindas** atlasiet kopsavilkuma cilni **Pirkšanas pasūtījuma rindas**. Kolonna **Kvalitātes pārbaudes pasūtījuma statuss** rāda katras pirkšanas pasūtījuma rindas statusu.

### <a name="from-production-orders"></a>No ražošanas pasūtījumiem

Lai strādātu ar kvalitātes pārbaudes pasūtījumiem, kas ir saistīti ar jūsu ražošanas pasūtījumiem, dodieties uz **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi** un pēc tam izpildiet jebkuru no tālāk minētajām darbībām.

- Atveriet ražošanas pasūtījumu vai atlasiet to režģī. Pēc tam darbību rūtī cilnē **Skatīt**, grupā **Pārvaldīt kvalitāti** atlasiet **Kvalitātes pārbaudes pasūtījumi**, lai atvērtu lapu **Kvalitātes pārbaudes pasūtījumi**. Tur ir iespējams apskatīt, izveidot vai atjaunināt ar ražošanas pasūtījumu saistītos kvalitātes pārbaudes pasūtījumus.
- Atveriet ražošanas pasūtījumu vai atlasiet to režģī. Pēc tam, darbību rūtī cilnes **Ražošanas pasūtījums** grupā **Ražošanas detalizētā informācija** atlasiet **Maršruts** un atveriet lapu **Ražošanas maršruts**. Lai skatītu ar maršruta operāciju saistītos kvalitātes pārbaudes pasūtījumus, veiciet vienu no šīm darbībam:

    - Atlasiet mērķa maršruta operāciju režģī. Pēc tam darbību rūtī atlasiet **Uzziņas \> Kvalitātes pārbaudes pasūtījumi**.
    - Atlasiet vērtību **Operācija Nr.** auks mērķa maršruta operācijai, lai atvērtu detalizētas informācijas lapu **Ražošanas maršruts**. Kopsavilkuma cilnē **Vispārīgi** laukā **Kvalitātes pārbaudes pasūtījuma statuss** ir norādīts ar maršruta operāciju saistīto kvalitātes pasūtījumu statuss.

- Atveriet ražošanas pasūtījumu un atlasiet kopsavilkuma cilni **Vispārīgi**. Lauks **Kvalitātes pārbaudes pasūtījuma statuss** rāda ar ražošanas pasūtījumu saistīto kvalitātes pārbaudes pasūtījumu statusu.

### <a name="from-quarantine-orders"></a>No karantīnas pasūtījumiem

Lai strādātu ar kvalitātes pārbaudes pasūtījumiem, kas ir saistīti ar jūsu karantīnas pasūtījumiem, dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Karantīnas pasūtījumi** un pēc tam izpildiet jebkuru no tālāk minētajām darbībām.

- Pārskatiet vērtības kolonnā **Kvalitātes pārbaudes pasūtījuma statuss**. Šādā veidā varat uzzināt visu kvalitātes pārbaudes pasūtījumu vispārējo statusu, kas režģī ir saistīti ar katru karantīnas pasūtījumu.
- Atlasiet karantīnas pasūtījumu režģī un pēc tam darbības rūtī atlasiet **Kvalitātes pārbaudes pasūtījumi**, lai skatītu, izveidotu vai atjauninātu ar karantīnas pasūtījumu saistītos kvalitātes pārbaudes pasūtījumus.

## <a name="advanced-actions-for-quality-orders"></a>Papildu darbības kvalitātes pārbaudes pasūtījumiem

Var veikt vairākas darbības ar kvalitātes pārbaudes pasūtījumiem, lai pārvaldītu statusu, izveidotu dokumentus un ievāktu informāciju par papildu detaļām.

### <a name="reopen-a-quality-order"></a>Atkārtoti atveriet kvalitātes pārbaudes pasūtījumu

Pēc noklusējuma jūs vairs nevarat rediģēt vai atjaunināt pārbaudes kvalitātes pasūtījumu pēc tam, kad tas ir apstiprināts un testi ir izturēti. Tomēr dažos gadījumos ir no jauna jāatver kvalitātes pārbaudes pasūtījums pēc tā pabeigšanas.

Lai atkārtoti atvērtu kvalitātes pārbaudes pasūtījumu, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.
1. Atveriet apstiprināto kvalitātes pārbaudes pasūtījumu vai atlasiet to režģī.
1. Darbību rūtī atlasiet **Atkārtoti atvērt kvalitātes pārbaudes pasūtījumu**.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Izveidot analīzes sertifikātu kvalitātes pārbaudes pasūtījumam

CoA ir pārskats, ko ģenerē organizācijas kvalitātes nodrošināšanas grupa. Tā apstiprina, ka prece atbilst noteiktiem noteikumiem vai prasībām. Jūsu klientiem vai uzraudzības iestādēm jūsu ģeogrāfiskā vietā var būt nepieciešamas CoA. Tās var būt pieprasītas, balstoties uz jūsu nozari un produktu tipu, ko apstrādāt, pirkt, ražot vai pārdot.

Supply Chain Management ļauj jums izveidot CoA no kvalitātes pārbaudes pasūtījuma. Pārskatā tiks iekļauti visi pārbaužu rezultāti kvalitātes pārbaudes pasūtījumam, kur opcija **Analīzes sertifikāta pārskats** ir iestatīta uz *Jā*. Šo opciju var iestatīt pēc noklusējuma, pamatojoties uz testu, kas tiek definēts lapā **Testi**. Tomēr varat ignorēt iestatījumu specifiskiem testiem specifiskiem kvalitātes pārbaudes pasūtījumiem.

Lai izveidotu CoA kvalitātes pārbaudes pasūtījumam, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.
1. Atlasiet kvalitātes pārbaudes pasūtījumu, kuram vēlaties izveidot CoA.
1. Darbību rūtī atlasiet **Uzziņas \> Analīzes sertifikāts**.
1. Lapā **Analīzes sertifikāts** darbību rūtī atlasiet **Jauns**.
1. Nav obligāti: laukā **Kontaktpersona** atlasiet kontaktpersonu, kurai jāadresē sertifikāts.
1. Darbību rūtī atlasiet **Drukāt**.
1. Dialoglodziņā **Analīzes sertifikāts** definējiet, kā pārskats jādrukā. Pēc tam atlasiet **Labi**, lai pārskatu drukātu uz printera, uz ekrāna, failā vai e-pasta ziņojumā.
1. Aizveriet lapas.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Bloķēt vai atbloķēt krājumus kvalitātes pārbaudes pasūtījumam

Kad kvalitātes pārbaudes pasūtījums ir automātiski izveidots no kvalitātes saistības, kvalitātes saistībai piešķirto krājumu paraugu ņemšanu var konfigurēt, lai bloķētu pilnu krājuma daudzumu atsaucei, kas tiek testēta. Papildinformāciju par krājuma paraugu ņemšanu skatiet [Kvalitātes pārvaldības krājumu iztveršana](quality-item-sampling.md).

Ja neizmantojat pilnu bloķēšanu vai izveidojat kvalitātes pārbaudes pasūtījumu manuāli, sistēma automātiski izveido krājumu bloķēšanas ierakstu krājuma daudzumam, kas tiek testēts kvalitātes pārbaudes pasūtījumā. Ierakstā, kas tiek izveidots lapā **Krājumu bloķēšana**, lauks **Krājuma bloķēšanas tips** tiek iestatīts uz *Kvalitātes pārbaudes pasūtījums*.

Lai skatītu un rediģētu krājuma bloķēšanu kvalitātes pārbaudes pasūtījumam, kas ir atlasīts lapā **Krājumu bloķēšana**, atlasiet **Uzziņas \> Krājuma bloķēšana** darbības rūtī. Papildinformāciju skatiet [Krājumu bloķēšana](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Uzziņas par kvalitātes pārbaudes pasūtījuma detaļām

Izmantojiet šādas pogas lapas **Kvalitātes pārbaudes pasūtījumu** darbību rūtī, lai skatītu papildu informāciju par kvalitātes pārbaudes pasūtījumu vai saistībā ar to:

- **Uzziņas \> Darba detāļas** — atveriet lapu, kurā varat skatīt ar kvalitātes pārbaudes pasūtījumu saistīto noliktavas darbu.
- **Uzziņas \> Neatbilstības** – atveriet lapu, kur varat apskatīt jebkuras ar kvalitātes pārbaudes pasūtījumu saistītas neatbilstības.
- **Krājumi** – komandas šajā izvēlnē ir kopējas visās krājumu darījumi. Tās var izmantot, lai skatītu vai atjauninātu tādu detalizētu informāciju kā darījumi, rīcībā esošie krājumi, rezervācijas un iezīmēšana.

### <a name="create-cases-related-to-quality-orders"></a>Izveidot gadījumus, kas saistīti ar kvalitātes pārbaudes pasūtījumiem

Jūs varat izveidot gadījumus, kas ir saistīti ar kvalitātes pārbaudes pasūtījumiem. Šādā veidā varat sekot detalizētai informācijai par problēmām un strādāt pie risinājuma. Pēc tam varat lietot gadījumu pārvaldības darbplūsmas līdzekļus, lai maršrutu gadījumā caur iepriekš definētu biznesa procesu iegūtu papildu apstiprinājumus vai iegūtu papildu informāciju par konkrētu problēmu. Ir arī iespējams izmantot zināšanu dokumentu līdzekli, lai izveidotu zināšanu bāzi kopīgiem jautājumiem.

## <a name="case-management-examples-for-quality-management"></a>Gadījumu pārvaldības piemēri kvalitātes pārvaldībai

### <a name="example-1"></a>1. piemērs

Jūs strādājat ražošanas uzņēmumā, kam jāatbilst stingriem noteikumiem, kas attiecas uz saistīto produktu, piemēram, pārtikas, ražošanu. Kvalitātes pārbaudes pasūtījumi tiek izmantoti, lai ierakstītu un atsekotu detaļas par krājumu kvalitāti visā ražošanas procesā. Ja kvalitātes pārbaudes pasūtījums neiztur noteiktus testus, iespējams, problēma ir ar aprīkojumu. Gadījumus izmanto, lai sekotu biznesa procesam un aktualizētu problēmu pareizajiem inženieriem, lai varētu noteikt pamatcēloni. Lai padarītu biznesa procesus vieglāk lietojamus, uzņēmums uztur zināšanas par vispārējiem jautājumiem, kas saistīti ar kvalitātes pārbaudes pasūtījumiem un aprīkojuma problēmām.

### <a name="example-2"></a>2. piemērs

Jūs strādājat izplatīšanas uzņēmumā, kas nosūta produktus, kurus var pielāgot dažādām valstīm un reģioniem. Dažiem debitoriem ir stingras specifikācijas, kas jāievēro. Pretējā gadījumā var rasties maksas un atgriešanas vai atmaksas. Jūs izmantojat kvalitātes pārbaudes pasūtījumus, lai izsekotu detalizētu informāciju par katru testu un rezultātiem, kas atbilst debitora prasībām. Gadījumus izmanto, lai pārskatītu un apstiprinātu CoA detaļas, pirms dokuments tiek ģenerēts un pievienots kopā ar citiem nosūtīšanas dokumentiem.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības procesi](quality-management-processes.md)
- [Kvalitātes tests](quality-tests.md)
- [Kvalitātes testa grupas](quality-test-groups.md)
- [Kvalitātes piesaistes](quality-associations.md)
- [Kvalitātes pārvaldības procesi](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
