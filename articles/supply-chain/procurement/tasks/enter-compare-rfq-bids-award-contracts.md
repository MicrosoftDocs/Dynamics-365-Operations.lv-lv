---
title: PP piedāvājumu ievade un salīdzināšana un līgumu piešķiršana
description: Šajā tēmā ir paskaidrots, kā ievadīt atbildes uz piedāvājuma pieprasījumu (PP), noteikt punktu skaitu un salīdzināt piedāvājumus, un kā pēc tam piešķirt līgumu vienam no kreditoriem.
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable, PurchTablePart, PurchRFQCompareLinePrices, PurchRFQCompareRFQ
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f14b95a71397bf5879c97654620e1d4c22a1149
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016682"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>PP piedāvājumu ievade un salīdzināšana un līgumu piešķiršana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā ievadīt atbildes uz piedāvājuma pieprasījumu (PP), noteikt punktu skaitu un salīdzināt piedāvājumus, un kā pēc tam piešķirt līgumu vienam no kreditoriem. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu **USMF**.

Pirms šīs procedūras sākšanas jums ir nepieciešams PP ar divām rindām, kas ir nosūtīts vismaz diviem kreditoriem. Lai izveidotu šo PP, pabeidziet procedūru [Piedāvājuma pieprasījuma izveide](create-request-quotation.md). Lai varētu pabeigt šo procedūru, ir nepieciešams iestatīt arī punktu skaitīšanas kritērijus.

Varat ievadīt piedāvājumu vai nu kā kreditors, vai kā sagādes speciālists. Papildinformāciju skatiet šeit: [Kreditoru sadarbības iestatīšana un uzturēšana](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Atbildes ievadīšana kreditora lomā

1. Informācijas panelī atlasiet **Piegādātāja piedāvājuma izteikšana**.
2. Sarakstā **Jauni aicinājumi izteikt piedāvājumus** atrodiet nupat nosūtīto PP. Atlasiet PP, lai pārskatītu pieprasīto informāciju.
3. Atlasiet **PP pielikumi**, lai pārskatītu pievienotos pielikumus.
4. Atlasiet **Piedāvājums**, lai laukus padarītu rediģējamus. Ņemiet vērā, ka laukā **Piedāvājuma norise** ir iestatīta vērtība **Kreditors atjaunina**.
5. Virsrakstā un rindās ievadiet vērtības no piedāvājuma atbildes.
6. Ja piedāvājumam jāpievieno kāds pielikums, izvēlieties **Piedāvājuma pielikumi**.
7. Atlasiet kopsavilkuma cilni **Solīšanas norādījumu krājumi**, lai noskaidrotu, vai ir nepieciešami dokumenti.
8. Atlasiet kopsavilkuma cilni **Grozījumi**, lai noskaidrotu, vai PP ir grozīts.
9. Kopsavilkuma cilnē atlasiet vienumu **Anketa**. Uz visām šeit parādītajām anketām ir jāatbild.
10. Atlasiet kopsavilkuma cilni **Detalizēta informācija par rindu**, lai skatītu paplašinātu informāciju par rindu.
11. Atlasiet **Atiestatīt no PP** tikai tad, ja ir jāatiestata ievadītās vērtības uz sākotnējām PP vērtībām.
12. Varat saglabāt piedāvājumu jebkurā laikā un veikt papildu apstrādi vēlāk, ja nav pagājis derīguma beigu datums un laiks. Šādā gadījumā varat meklēt piedāvājumu sarakstā **Notiekošie piedāvājumi** darbvietā **Piegādātāja piedāvājuma izteikšana**.
13. Kad piedāvājums ir gatavs nosūtīšanai, atlasiet **Iesniegt.** Atlasiet **Noraidīt**, ja nevēlaties izteikt piedāvājumu. Iesniegtie piedāvājumi ir pieejami sarakstā **Iesniegtie piedāvājumi** darbvietā **Piegādātāja piedāvājuma izteikšana**.  
14. Kad piedāvājums ir iesniegts, to var atsaukt jebkurā laikā pirms beigu datuma un laika. Ņemiet vērā, ka, atsaucot piedāvājumu, tas netiek uzskatīts par iesniegtu. Kad sagādes nodaļa ir piedāvājumu ir akceptējusi vai noraidījusi,, tas tiek rādīts sarakstā **Piešķirtie piedāvājumi** vai **Zaudētie piedāvājumi** darbvietā **Piegādātāja piedāvājuma izteikšana**.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Kreditora atbildes ievadīšana sagādes speciālista lomā

1. Pārliecinieties, vai ir iestatīta atļauja rediģēt kreditoru piedāvājumus. Dodieties uz **Sagāde un avoti \> Iestatīšana \> Sagādes un avotu parametri**. Cilnē **Piedāvājumu pieprasījumi** opcijai **Pircējs var rediģēt piegādātāju piedāvājumu** iestatiet vērtību **Jā**.
2. Dodieties uz **Sagāde un avoti \> Piedāvājumu pieprasījumi \> Visi piedāvājuma pieprasījumi**.
3. Atlasiet PP, kura statuss ir **Nosūtīts**, un atlasiet saiti laukā **Piedāvājuma pieprasījuma gadījums**.
4. Atlasiet **Pārvaldīt atbildes**. Parādītajā lapā ir redzams katra kreditora PP, kuram tika nosūtīts uzaicinājums izteikt piedāvājumu.
5. Atlasiet PP, uz kuru nav atbildēts. ( Laukam **Atbildes norise** laukam jābūt iestatītam kā **Nav sākts**.)
6. Atlasiet **Rediģēt \> Rediģēt PP atbildi**. Tiek atvērta lapa **PP atbilde**. Kā sagādes speciālists tagad varat ievadīt atbildi kreditora vārdā. Ņemiet vērā, ka laukā **Piedāvājuma norise** ir iestatīta vērtība **Pircējs atjaunina**.  
7. Ievadiet piedāvājuma datus. Pēc pabeigšanas atlasiet **Iesniegt**.

## <a name="score-the-bids"></a>Piedāvājumu punktu skaitīšana

1. Lapā **Visi piedāvājuma pieprasījumi** atlasiet PP gadījumu, kura atbilžu punktus vēlaties skaitīt.
2. Atlasiet **Pārvaldīt atbildes**.
3. Atlasiet atbildi, kurai skaitīt punktus.
4. Atlasiet **Virsraksts**, lai varētu skatīt piedāvājuma punktu skaitu.
5. Kopsavilkuma cilnes **Piedāvājuma punktu skaitīšana** laukā **Punktu skaits** ievadiet numuru vienam no punktu skaitīšanas kritērijiem. Ja peles kursoru novietojat virs punktu skaitīšanas kritērija, rīka padomā tiek parādīts nepieciešamo punktu diapazons. Šajā demonstrācijā jebkuram punktu skaitīšanas kritērijam varat pievienot skaitli no 1 līdz 5.  
6. Atkārtojiet 5. darbību citam punktu skaitīšanas kritērijam.
7. Ja PP gadījumam ir anketa, kas tika nosūtīta kreditoriem, tad kopsavilkuma cilnē **Anketas** varat ievadīt kreditoru atbildes.
8. Aizvērt lapu.
9. Atkārtojiet 1. līdz 8. darbību visiem citiem piedāvājumiem.

## <a name="compare-the-replies"></a>Salīdzināt atbildes

1. Darbību rūts cilnē **Vispārīgi** atlasiet **Salīdzināt atbildes**.
2. Laukā **Rangs** ievadiet kādu numuru.  
    - Šajā lapā tiek rādīti piedāvājumi ar virsrakstu un rindu informāciju, kā arī kopējo punktu skaitu virsraksta līmenī. Rindas varat salīdzināt, kārtojot režģi, lai salīdzināmās rindas atrastos līdzās. Ir iekļauta arī tālāk norādītā informācija.
    - **Daudzums** — kreditora piedāvātais daudzums. Šis daudzums var nebūt vienāds ar daudzumu, kas norādīts PP.
    - **Neto summa** — kreditora piedāvātā cena pēc visu atlaižu atņemšanas rindā norādītajiem krājumiem.
    - **Novirze** — dienu skaits, par kādu piedāvājuma virsrakstā vai rindā norādītais piegādes datums atšķiras no PP virsrakstā vai rindā pieprasītā piegādes datuma. Katram piedāvājumam varat ievadīt rangu.  
3. Atlasiet virsraksta rindu otram piedāvājumam, kuram vēlaties noteikt rangu.
4. Laukā **Rangs** ievadiet kādu numuru.
5. Atlasiet **Saglabāt**.

## <a name="reject-a-bid"></a>Noraidīt piedāvājumu

1. Atlasiet virsraksta rindu piedāvājumam, kuru vēlaties noraidīt. Vienlaicīgi varat pieņemt, noraidīt vai atgriezt tikai vienu piedāvājumu vai viena piedāvājuma rindas.
2. Atzīmējiet izvēles rūtiņu **Atzīmēt**.  
    - Ja piedāvājuma virsrakstā atzīmējat izvēles rūtiņu **Atzīmēt**, tad tiek atzīmētas arī visas rindas. Lai noraidītu vai pieņemtu tikai dažas no piedāvājuma rindām, varat iezīmēt tikai šīs rindas. Turklāt varat pieņemt viena kreditora priekšlikumu dažās PP rindās, bet pārējās PP rindas piešķirt citam kreditoram. Tomēr ir jāapstrādā viens piedāvājums vienlaikus.  
    - Ja pastāv citas rindas, varat pieņemt sākotnējo piedāvājuma rindu vai tās alternatīvu, bet ne abas.  
3. Atlasiet **Noraidīt**.
4. Atlasiet **Parametri** un pēc tam laukā **Noraidīšanas pamatojums** ievadiet vai atlasiet pamatojumu piedāvājuma noraidīšanai. Pamatojums tiek saglabāts atbildē.  
5. Atlasiet **Labi**.
6. Atlasiet **Labi**.

## <a name="accept-a-bid"></a>Pieņemt piedāvājumu

1. Atlasiet piedāvājumu, kuru vēlaties pieņemt, un pēc tam atlasiet saiti laukā **Piedāvājuma pieprasījums**. Ja atrodaties lapā **Salīdzināt piedāvājuma pieprasījumu atbildes**, izceltais piedāvājums, kam ir fokuss, ir piedāvājums, ko sistēma apsvērs pieņemšanas darbības laikā. Varat pieņemt rindas tikai no viena piedāvājuma vienlaikus.  
2. Darbību rūtī atlasiet **Atbilde**.
3. Atlasiet **Pieņemt**. Ja esat atzīmējis tikai noteiktas rindas, pieņemšanas darbība iekļaus tikai šīs rindas. Ja vēlaties pieņemt visas piedāvājuma rindas, tad rindas nav jāatzīmē.  
4. Atlasiet **Parametri** un pēc tam laukā **Pieņemšanas pamatojums** ievadiet vai atlasiet pamatojumu piedāvājuma pieņemšanai. Pamatojums tiek saglabāts piedāvājumā.  
5. Atlasiet **Labi**.
6. Atlasiet **Labi**. Kad atlasāt **Labi**, tiek izveidots pirkšanas pasūtījums, pamatojoties uz PP pieņemšanā iekļautajām rindām. Ja pastāv citi piedāvājumi, kas nav apstrādāti (pieņemti, noraidīti vai atgriezti), tad sistēma jums piedāvā noraidīt tos.  

## <a name="view-the-purchase-order-that-is-generated"></a>Skatīt ģenerēto pirkšanas pasūtījumu

Darbību rūts cilnē **Vispārīgi** atlasiet **Pirkšanas pasūtījums**. Lapā, kas tiek parādīta, ir pirkšanas pasūtījums, kas tika ģenerēts, kad pieņēmāt piedāvājumu.
