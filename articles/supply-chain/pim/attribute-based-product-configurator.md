---
title: Atribūtiem atbilstošas pārdošanas cenas ierobežojumiem atbilstošām preču konfigurācijām
description: Šajā tēmā ir aprakstīts, kā veidot pārdošanas cenu modeļus ar pārdošanas cenām, pamatojoties uz komponentiem un atribūtiem, nevis uz fizisko materiālu komplektu un maršrutu.
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: cba4b1eac33ae53e214297728c1cdf2710ebd9d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007920"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Atribūtiem atbilstošas pārdošanas cenas ierobežojumiem atbilstošām preču konfigurācijām

Šajā tēmā ir aprakstīts, kā veidot pārdošanas cenu modeļus ar pārdošanas cenām, pamatojoties uz komponentiem un atribūtiem, nevis uz fizisko materiālu komplektu un maršrutu. Katram preces konfigurācijas modelim var izveidot vairākus pārdošanas cenu modeļus.

## <a name="set-relevant-product-information-management-parameters"></a>Atbilstošo preču informācijas pārvaldības parametru iestatīšana

Pirms sākat veidot cenu modeļus, ir jādefinē noklusējuma valūta, kas tiek izmantota, veidojot pārdošanas cenu modeļus. Varat arī izvēlēties, vai pievienot Microsoft Excel failu ar cenu sadalījumu visām pasūtījuma vai piedāvājuma rindām. Cenu sadalījums ļauj koplietot informāciju ar klientiem par to, kā ieguvāt konfigurētās preces noteikto pārdošanas cenu.

Lai iestatītu noklusējuma valūtu:

1. Dodieties uz  **Preču informācijas pārvaldība \> Iestatīšana \> Preču informācijas pārvaldības parametri**.
1. Atveriet cilni **Ierobežojumam atbilstošie preces konfigurācijas modeļi**.
1. Atveriet **Noklusējuma valūta** nolaižamo sarakstu un atlasiet valūtu.

    ![Noklusējuma valūtas iestatīšana ierobežojumam atbilstošai preces konfigurācijai](media/prod-config-currency.png "Noklusējuma valūtas iestatīšana ierobežojumam atbilstošai preces konfigurācijai")

1. Ja vēlaties pievienot Excel failu ar cenu sadalījumu visām pasūtījuma vai piedāvājuma rindām, tad sadaļā **Cenas modelis** iestatiet **Pievienot** uz *Jā*.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Pārdošanas cenu modeļu izveide

Lai izveidotu pārdošanas cenu modeli:

1. Dodieties uz  **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
1. Atlasiet mērķa preces konfigurācijas modeli.
1. Darbību rūtī atveriet cilni **Modelis** un grupā **Iestatīšana** atlasiet **Cenu modeļi**.
1. Tiek atvērta lapa **Cenu modeļi**.
1. Atlasiet cenas modeli vai pievienojiet režģim jaunu.
1. Atlasiet **Rediģēt**, lai atvērtu atlasītā modeļa rediģēšanas lapu, kas nodrošina šādus līdzekļus:
    - Formas galvenē tiek parādīta noklusējuma valūta un cenas iestatījumam var pievienot jaunas valūtas.
    - Kreisajā rūtī tiek parādi visi komponenti un lietotāju prasības attiecībā uz preces modeli. Katram zaram preces modeļa kokā var būt viena pamatcenas izteiksme un neobligāts izteiksmes kārtulu skaits. Izteiksmes kārtula sastāv no nosacījuma un izteiksmes, un katra izteiksmes kārtula attiecas uz vienu preces opciju, kas palīdz kontrolēt preces cenu.
    - Veidojot nosacījumus un izteiksmes, jums ir pieejami tie paši operatori, kas ir pieejami kā aprēķini preces modelī. Izteiksmju redaktors atbalsta arī nosacījumus un izteiksmes.
1. Kreisajā kolonnā atlasiet zaru un pēc tam izmantojiet iepriekšējā darbībā aprakstītos līdzekļus, lai tam izveidotu cenu noteikšanas kārtulas (skatiet arī piemēru, kas sniegts pēc šīs procedūras). Atkārtojiet šo darbību katram zaram pēc nepieciešamības.

Tālāk esošajā piemērā ir parādīta fiksēta skaita pamatcena 899,95 EUR, ko var modificēt ar vienu vai vairākām tālāk norādītajām piecām izteiksmes kārtulām, atkarībā no klienta izvēlētās konfigurācijas:

- Baltā korpusa apdare, atņemt 59,95 EUR.
- Stūru aizsardzība, pievienot 35,95 EUR.
- Metāla priekšējais režģis, pievienot 89,95 EUR.
- Rožkoka korpusa apdare, pievienot 119,95 EUR.
- Pievienot 12,95 EUR par katru skaļruņa augstuma vienību.

![Piemēra cenu modelis](media/prod-config-rules-example.png "Piemēra cenu modelis")

## <a name="add-support-for-multiple-currencies"></a>Atbalsta pievienošana vairākām valūtām

Pārdodot konfigurējamu preci, sistēma pārbauda, vai cenas ir iestatītas tieši klienta valūtā. Ja tā ir, tiek izmantotas precīzas vērtības. Ja tā nav, sistēma izmanto pārdošanas uzņēmumam izveidotos valūtas maiņas kursus, lai konvertētu noklusējuma valūtas vērtību klienta valūtā.

Lai pievienotu precīzas cenas papildu valūtā:

1. Atveriet cenas modeļa rediģēšanas lapu, kā aprakstīts sadaļā [Pārdošanas cenu modeļu izveide](#build-price-model).
1. Atlasiet pogu **Pievienot** cenas modeļa galvenē, lai atvērtu **Valūtas** nolaižamo dialoglodziņu, kurā uzskaitītas pieejamās valūtas.
1. Atlasiet valūtu, kuru vēlaties pievienot, **Valūtas** nolaižamajā dialoglodziņā un pēc tam atlasiet **Labi**.
1. Nolaižamajā sarakstā **Pašreizējā valūta** tagad ir iekļauta tikko pievienotā valūta, kā arī citas valūtas, kas tika pievienotas iepriekš. Atlasiet savu jauno valūtu un ievērojiet, ka režģa sadaļā **Izteiksmes kārtulas** tagad ir ietverti divi izteiksmes lauki:
    - **Izteiksme** – parāda izteiksmi (vai nemainīgu vērtību) cenas atrašanai, izmantojot pašreizējo valūtu, kas atlasīta **Pašreizējā valūta**.
    - **Noklusējuma izteiksmes** – parāda izteiksmi (vai nemainīgu vērtību) cenas atrašanai, izmantojot pašreizējo noklusējumu (parādīts **Noklusējuma valūta** laukā).

    > [!NOTE]
    > Izteiksmes kārtulu lauks **Nosacījums** ir “piederošs” noklusējuma valūtai, kas nozīmē, ka nav iespējams modificēt citu valūtu nosacījumu. Kā arī nav iespējams pievienot jaunas izteiksmes kārtulas, kamēr valūta, kas nav noklusējuma valūta, ir atlasīta kā **Pašreizējā valūta**.
1. Rediģējiet vērtības kolonnā **Izteiksme**, kā nepieciešams pašreizējai valūtai.

Tālāk esošajā piemērā _EUR_ ir noklusējuma valūta un _USD_ ir pievienota kā papildu valūta.

![Modeļa piemērs ar vairākām valūtām](media/prod-config-rules-currency-example.png "Modeļa piemērs ar vairākām valūtām")

> [!NOTE]
> Nav iespējams pievienot izteiksmes kārtulas, kas ir unikālas valūtai, kas nav noklusējuma valūta. Lai izveidotu izteiksmes kārtulas, kas būtu piemērotas tikai valūtai, kas nav noklusējuma valūta, iestatiet noklusējuma valūtas cenas izteiksmi uz nulli. Pēc tam valūtai, kas nav noklusējuma valūta, iestatiet atbilstošu izteiksmi.

## <a name="test-your-price-model"></a>Pārbaudīt cenas modeli

Lai pārbaudītu, kā konfigurācijas sesijā darbojas pārdošanas cenas, atveriet jūsu cenas modeļa rediģēšanas lapu, kā aprakstīts sadaļā [Pārdošanas cenu modeļu izveide](#build-price-model) un pēc tam darbību rūtī atlasiet  **Pārbaudīt**. Tiek atvērts dialoglodziņš **Pārbaudīt preces modeli**, kurā var rīkoties šādi:

- Izmantojiet šeit piedāvātos konfigurācijas iestatījumus, lai atlasītu preces opcijas un pēc tam skatītu, kā tās ietekmē **Cena un nosūtīšanas datums** parādīto vērtību.
- Atlasiet **Skatīt cenu sadalījumu**, lai lejupielādētu Excel dokumentu, kas parāda pilnīgu informāciju par cenas aprēķināšanu.

![Preces modeļa pārbaudīšana](media/prod-config-test.png "Preces modeļa pārbaudīšana")

Lejupielādētajā izklājlapā tiek parādīta gan aktīvā cenas elementa absolūtā vērtība, gan segums procentos. Ja lapā **Preču informācijas pārvaldības parametri** esat iestatījis opciju **Pievienot** cenu modeli, tad Excel lapa tiek pievienota pasūtījuma vai piedāvājuma rindai.

![Excel izklājlapa, kurā parādīts cenu sadalījums](media/prod-config-excel-example.png "Excel izklājlapa, kurā parādīts cenu sadalījums")

## <a name="set-up-selection-criteria-for-price-models"></a>Cenu modeļu atlases kritēriju iestatīšana

Kad cenu modeļi ir ieviesti, jums ir jāizveido vismaz viens atlases kritērijs, lai, konfigurējot piedāvājumu vai pasūtījumu, tiktu iekļauts arī cenas modelis. To var izdarīt, iestatot vienu vai vairākus vaicājumus. Kombinācijā ar atbilstošiem pārdošanas cenu modeļiem vaicājumi nodrošina lielu elastību, nosakot pārdošanas cenas konkrētiem klientiem, reģioniem, periodiem un citiem kritērijiem.

Lai iestatītu cenu modeļu atlases kritērijus:

1. Dodieties uz  **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
1. Atlasiet mērķa preces konfigurācijas modeli.
1. Darbību rūtī atveriet cilni **Modelis** un grupā **Iestatīšana** atlasiet **Cenas modeļa kritēriji**. Tiek atvērta lapa **Cenas modeļa kritēriji**.
1. Ja nepieciešamā vaicājuma rinda vēl nepastāv, darbību rūtī atlasiet **Jauns**, lai režģim pievienotu jaunu rindu, un veiktu šādus iestatījumus:
    - **Nosaukums** – ievadiet šīs rindas nosaukumu.
    - **Apraksts** – īsi aprakstiet vaicājumu un kam tas paredzēts.
    - **Cenas modelis** – atlasiet [cenas modeli](#build-price-model) (no pašreizējā konfigurācijas modeļa), ko vaicājums lietos, kad tiks aktivizēts.
    - **Pasūtījuma veids** – atlasiet pasūtījuma veidu, kurā tiks lietots vaicājums.
    - **Derīgs no** – norādiet pirmo dienu, kad vaicājums tiks lietots.
    - **Beidzas pēc** – norādiet pēdējo datumu, vaicājums tiks lietots.

    ![Cenas modeļa kritēriji](media/prod-config-price-model-criteria.png "Cenas modeļa kritēriji")

1. Atlasiet, kuru vaicājuma rindu vēlaties definēt, un pēc tam atlasiet **Rediģēt** **Darbību rūtī**. Tiek atvērts vaicājuma noformētāja dialoglodziņš. Tas darbojas tāpat kā vairums vaicājumu noformētāji programmā Supply Chain Management. Izmantojiet to, lai definētu nosacījumus, ar kuriem jālieto atlasītās rindas cenas modelis.

1. Atkārtojiet 4.–5. darbību katram nepieciešamajam vaicājumam.
    > [!TIP]
    > Jūs varat ietaupīt laiku, nokopējot jau esošu rindu, kas ir līdzīga jaunajai rindai, kuru nepieciešams pievienot. Lai to izdarītu, atlasiet mērķa rindu un pēc tam darbību rūtī atlasiet **Dublēt**.

1. Kad esat pabeidzis iestatīt kritērijus, sakārtojiet tos atbilstošā secībā **Cenas modeļa kritēriji** sarakstā. Lai pārvietotu rindu, atlasiet rindu un pēc tam darbību rūtī atlasiet **Uz augšu** vai **Uz leju**.

    > [!IMPORTANT]
    > Konfigurēšanas laikā sistēma sāk meklēšanu no saraksta sākuma un izmanto pirmo vaicājumu, kas atbilst datiem piedāvājumā vai pasūtījuma rindā. Tāpēc visprecīzākie vaicājumi ir jāievada saraksta sākumā. Ja vispārīgu vaicājumu novietosit saraksta sākumā, tad tiks izmantots šis vaicājums neatkarīgi no tā, ka sarakstā, iespējams, ir vaicājums, kas ir vērsts tieši uz klientu vai potenciālo konfigurāciju.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Atribūtiem atbilstošu pārdošanas cenu iestatīšana preču modeļa versijā

Pēdējā darbība ir atribūtiem atbilstošu pārdošanas cenu norādīšana preču modeļa versijā. Lai izpildītu šo darbību:

1. Dodieties uz  **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
1. Atlasiet mērķa preces konfigurācijas modeli.
1. Darbību rūtī atveriet cilni **Modelis** un grupā **Produkta modeļa informācija** atlasiet **Versijas**.
1. Tiek atvērta lapa **Versijas**. Pārliecinieties, vai **Cenu noteikšanas metode** ir iestatīta uz **Atribūtam atbilstošs**.
    ![Cenu noteikšanas metodes iestatīšana uz atribūtam atbilstošs](media/prod-config-versions.png "Cenu noteikšanas metodes iestatīšana uz atribūtam atbilstošs")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]