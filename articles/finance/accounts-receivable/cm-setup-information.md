---
title: Kredīta pārvaldības iestatīšana
description: Šajā tēmā aprakstīta iestatīšana, kas nepieciešams kredīta pārvaldībai.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 640d81920dad391a77b58942972660b01f11b003
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830644"
---
# <a name="credit-management-setup"></a>Kredīta pārvaldības iestatīšana 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Kredītu pārvaldības darbplūsmas

Dodieties uz **Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldības darbplūsmas**, lai definētu darbplūsmas, kas tiek izmantotas kredīta limita pārrēķinu pārvaldībai.

- Varat izveidot darbplūsmu, kas ļauj apstiprināt kredīta limitu pārrēķinu partiju ar vienu apstiprinājumu.
- Rindas līmenī varat pievienot darbplūsmu, lai kredīta limita korekcijas varētu apstiprināt atsevišķi.
- Varat izveidot palaišanas darbplūsmu, kas automātiski maršrutē aizturēšanas uz darbplūsmas procesu.

## <a name="blocking-rules"></a>Aizturēšanas kārtulas

### <a name="ranking-payment-terms"></a>Apmaksas nosacījumu kārtošana pēc ranga

Varat aizturēt pārdošanas pasūtījumu, ja pasūtījumā norādītie apmaksas nosacījumi neatbilst debitora noklusējuma apmaksas nosacījumiem. Tomēr dažreiz apmaksas nosacījumi atšķiras, bet ir pietiekami līdzīgi, ka nevēlaties aizturēt pasūtījumu. Varat kārtot apmaksas nosacījumus tā, ka dažiem no tiem ir viens rangs, bet citiem ir augstāks vai zemāks rangs.

Ja apmaksas nosacījumu rangs ir aktīvs un pasūtījuma maksājuma nosacījumiem ir augstāks rangs nekā noklusējuma maksājuma nosacījumiem, pārdošanas pasūtījums tiks aizturēts.

Lai iestatītu maksājuma nosacījumu rangus, dodieties uz lapu **Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldības iestatīšana \>Kārtot apmaksas nosacījumus**  

### <a name="ranking-settlement-discounts"></a>Norēķinu atlaižu kārtošanas pēc ranga

Varat aizturēt pārdošanas pasūtījumu, ja pasūtījumā norādītās norēķinu atlaides neatbilst debitora noklusējuma norēķinu atlaidēm. Tomēr dažreiz norēķinu atlaides atšķiras, bet ir pietiekami līdzīgas, ka nevēlaties aizturēt pasūtījumu. Varat kārtot norēķinu atlaides tā, ka dažām no tām ir viens rangs, bet citām ir augstāks vai zemāks rangs.

Ja norēķinu atlaižu rangs ir aktīvs un ja norēķinu atlaidēm pasūtījumā ir augstāks rangs nekā debitora noklusējuma norēķinu atlaidēm, pārdošanas pasūtījums tiks aizturēts.

Lai iestatītu maksājuma nosacījumu rangus, dodieties uz lapu **Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldības iestatīšana \>Kārtot apmaksas nosacījumus**  

## <a name="reasons"></a>Iemesli

Kredīta pārvaldībā tiek izmantoti vairāki iemeslu tipi.

- Aizturēšanas iemesli norāda, kāpēc pārdošanas pasūtījums ir aizturēts.
- Palaišanas iemesli tiek piešķirti pasūtījumam, kad tas tiek palaists no aizturēšanas.
- Statusa iemesli norāda, kāpēc konta statuss tika piešķirts debitoram.

Varat iestatīt iemeslus lapā **Kredīta pārvaldības iemesli** (**Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldība \> Kredīta pārvaldības iestatīšana**).

1. Laukā **Iemesla veids** atlasiet iemesla veidu: **Aizturēšana**, **Palaišana** vai **Statuss**.
2. Laukā **iemesls** ievadiet iemesla nosaukumu.
3. Laukā **Apraksts** ievadiet iemesla koda aprakstu.

## <a name="credit-management-groups"></a>Kredīta pārvaldības grupas

Kredīta pārvaldības grupas tiek izmantotas, lai identificētu debitorus vai debitoru grupas, kurām ir tie paši kredīta pārvaldības rekvizīti. Piemēram, kredītu pārvaldības grupas var izmantot, lai noteiktu aizturēšanas un izslēgšanas kredīta pārvaldības kārtulas debitoriem.

Varat izveidot kredīta pārvaldības grupas lapā **Kredīta pārvaldības grupas** (**Kredīts un iekasēšana \> Iestatījumi> Kredīta pārvaldības iestatīšana \> Kredīta pārvaldības grupas**).

1. Atlasiet **Jauns**, lai izveidotu rindu.
2. Ievadiet grupas ID. ID var ietvert līdz 10 rakstzīmēm.
3. Laukā **Apraksts** ievadiet grupas nosaukumu. Nosaukums var ietvert līdz 60 rakstzīmēm.

Kredītu pārvaldības grupa ir piešķirta debitoram kopsavilkuma cilnē **Kredīts un iekasēšana** lapā **Visi debitori** (**Debitoru parādi \> Debitori \> Visi debitori**).

## <a name="account-statuses"></a>Kontu statusi

Varat izveidot konta statusus, lai identificētu debitora konta kredīta stāvokli. Varat noteikt statusu un tā ietekmi uz rēķinu izrakstīšanas un nosūtīšanas aizturēšanas procesiem. Konta statusus var izmantot arī, lai noteiktu debitora aizturēšanas kārtulas.

Jūs varat izveidot konta statusus lapā **Konta statusi** (**Kredīts un iekasēšana \> Iestatījumi> Kredīta pārvaldības iestatījumi \> Konta statusi**).

1. Pievienojiet konta statusu un ievadiet aprakstu, kas atspoguļo debitora kredīta stāvokli. Piemēram, izmantojiet **Parasts**, lai norādītu, ka debitors ir uzticams un atvērtajos pasūtījumos tiek piemērota standarta kredīta pārvaldības apstrāde.
2. Laukos **Rēķinu izrakstīšana** un **Nodošana aizturēšanai** atlasiet aizturēšanas tipu, kas jāizpilda debitoriem, kuriem ir šis konta statuss. Varat aizturēt visu apstrādi, aizturēt tikai rēķina apstrādi vai aizturēt apstrādi, kad tiek piemērotas kredīta limita kārtulas.

## <a name="scoring-groups"></a>Vērtēšanas grupas

Varat iestatīt punktu skaitīšanas grupas, lai definētu riska faktorus un kritērijus, kas tiek izmantoti to novērtēšanai. Kad informācija par debitoru tiek piemērota punktu skaitīšanas grupai, katram riska faktoram tiek aprēķināts rezultāts, un tas tiek izmantots, lai debitors tiktu pakļauts riska grupai. Riska grupu var izmantot, lai identificētu kredītspēju un automātiski aprēķinātu kredīta limitus.

Punktu skaitīšanas grupas varat izveidot lapā **Punktu skaitīšanas grupas** (**Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldības iestatījumi \> Risks \> Punktu skaitīšanas grupas**).

1. Izveidojiet punktu skaitīšanas grupu un piešķiriet tai nosaukumu.
2. Ievadiet aprakstu, lai aprakstītu punktu skaitīšanas grupu.
3. Atlasiet grupas veidu. Ir astoņi iepriekš definēti veidi. Varat arī atlasīt **Lietotāja definēts**, lai definētu grupas veidu, kas ir labāk piemērots jūsu organizācijai.
4. Atlasiet punktu skaitīšanas veidu, lai definētu, kā punktu skaitīšanas grupa aprēķina riska punktu skaitu. Pieejamas šādas opcijas

    - **Diapazons** — Izmantojiet šo opciju, lai definētu vērtību diapazonu, kas jāizmanto punktu aprēķināšanai.
    - **Lietotāja definēts** — izmantojiet šo opciju, lai manuāli definētu vērtību sarakstu, kas jāizmanto rezultātam.

5. Ja atlasījāt **Diapazons** kā rezultāta veidu, pievienojiet rindas, lai definētu vērtību diapazonu un atbilstošos punktus.

    1. Laukā **Vērtība No** norādiet zemāko vērtību diapazonā.
    2. Laukā **Vērtība Līdz** norādiet augstāko vērtību diapazonā.
    3. Laukā **Rezultāts** ievadiet punktu skaitu, kas jāpiešķir, ja vērtība, kas tiek sniegta, ir “No”/“Līdz” diapazonā.

    Ja atlasījāt **Lietotāja definēts** kā rezultāta veidu, pievienojiet rindas, lai definētu lietotāja definētās vērtības un atbilstošos punktus.

    1. Laukā **Vērtība** ievadiet lietotāja definēto vērtību, kas jāsniedz no debitora informācijas.
    2. Laukā **Rezultāts** ievadiet punktu skaitu, kas jāpiešķir, ja vērtība, kas tiek sniegta, ir “No”/“Līdz” diapazonā.

## <a name="risk-classification"></a>Risku klasifikācija

Varat definēt riska novērtējumus, kurus var piešķirt debitoriem, pamatojoties uz to riska punktu skaitu. Riska punktu skaits tiek aprēķināts, salīdzinot debitoru informāciju katrai punktu skaitīšanas grupai. Punktu skaits tiek summēts, un kopējais rezultāts tiek salīdzināts ar vērtībām riska grupas iestatījumos, lai identificētu riska grupu, kurai pieder debitors. Tad riska grupas punktu skaits tiek izmantots, lai klientam definētu kredīta pārvaldības aizturēšanas un izslēgšanas kārtulas.

Jūs varat iestatīt riska grupas lapā **Riska novērtējumu** (**Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldības iestatījumi \> Risks \> Risku klasifikācija**).

1. Ievadiet riska grupas ID.
2. Ievadiet aprakstu, lai sīkāk paskaidrotu riska grupu.
3. Ievadiet rezultātu diapazonu, kas tiek izmantots, lai noteiktu, kuri debitori pieder riska grupai.
4. Atlasiet riska grupas indikatoru, lai norādītu simbolu, kas attēlo riska grupu.

## <a name="guaranteeinsurance-types"></a>Garantijas/apdrošināšanas veidi

Varat iestatīt garantijas/apdrošināšanas veidus lapā **Garantijas/apdrošināšanas veidi** (**Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldības iestatījumi \> Apdrošināšana un garantijas \> Apdrošināšanas un garantiju veidi**).

1. Ievadiet garantijas vai apdrošināšanas veidu, kas identificē garantētāja vai apdrošināšanas starpnieka nosaukumu.
2. Ievadiet aprakstu, lai aprakstītu garantētāja/apdrošināšanas starpnieku.

## <a name="coverage-types"></a>Seguma tipi

Vajadzību veidus var izmantot, lai klasificētu apdrošināšanas polises. Tās nevar izmantot kopā ar garantijām.

Varat pievienot vajadzību veidus lapā **Vajadzību veidi** (**Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldības iestatījumi \> Apdrošināšana un garantijas \> Vajadzību veidi**).

1. Ievadiet vajadzības veidu, lai identificētu vajadzības veidu, kas jāpievieno kā apdrošināšana vai garantija.
2. Ievadiet aprakstu, lai aprakstītu vajadzības veidu.

## <a name="automatic-credit-limits"></a>Automātiski kredītlimiti

Varat izveidot kritērijus, lai automātiski noteiktu kredīta limitus, lapā **Automātiski kredīta limiti** (**Kredīts un iekasēšana \> Iestatījumi \> Kredīta pārvaldības iestatījumi \> Risks \> Automātiski kredīta limiti**).

1. Atlasiet riska grupu, kurai piešķirt automātisko kredīta limitu.
2. Atlasiet valūtu automātiskajam kredīta limitam. Vienai riska grupai var izveidot vairākus automātiskus kredīta limitus dažādās valūtās.
3. Ievadiet ieņēmumu summu, kas attēlo maksimālo uzņēmuma ieņēmumu, ko var izmantot šim automātiskajam kredīta limitam. Kad tiek veidoti kredīta limiti, ieņēmumu summa tiek salīdzināta ar ieņēmumu vērtību, kas ir atrodama lapā **Finanses** (**Debitoru parādi \> Visi debitori \> Atlasīt debitoru \> Vispārīgi \> Statistikas \> Finanses**). Sistēma izmanto jaunāko vērtību sadaļā **Pārskats**.

Izpildiet šīs darbības, lai pievienotu rindas, kas norāda kredīta limitu, kas tiks ģenerēts, pamatojoties uz atlasītajiem kritērijiem.

1. Atlasiet punktu skaitīšanas grupu, kas nosaka debitora informāciju, kas jāizmanto kredīta limita aprēķināšanai.
2. Atlasiet salīdzinājuma operatoru, kas nosaka, kā jānovērtē punktu skaitīšanas grupas informācija.
3. Ievadiet vērtību, kas jāsalīdzina ar vērtību, kas norādīta punktu skaitīšanas grupai.
4. Ievadiet kredīta limitu, kas jāpiešķir, ja debitora informācija atbilst vērtībai, kas norādīta punktu skaitīšanas grupai. Piemēram, jūs izveidojat automātisku kredīta limitu punktu skaitīšanas grupai **Zema**. Ja uzņēmuma darbības gadi ir viena no punktu skaitīšanas grupām, varat definēt vienu rindu, kas piešķir kredīta limitu 100 000, ja debitors ir bijis aktīvs uzņēmējdarbības veicējs piecus gadus, un citu rindu, kas piešķir kredīta limitu 200 000, ja debitors ir bijis aktīvs uzņēmējdarbības veicējs 10 gadus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]