---
title: Bīstamo materiālu iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt datus, kas ir nepieciešami, lai klasificētu krājumus kā bīstamus materiālus. Kad izveidojat pārdošanas pasūtījumu, kas ietver krājumu, kas ir klasificēts kā bīstams materiāls, sistēma ģenerē bīstamo materiālu dokumentāciju šim pārdošanas pasūtījumam, kad tas tiek nosūtīts.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b049559b64045e80a40afd99bac30a9cfe1d0580
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432963"
---
# <a name="set-up-hazardous-materials"></a>Bīstamo materiālu iestatīšana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Lai izmantotu bīstamo materiālu funkcionalitāti, vispirms ir jāiestata dati, kas ir nepieciešami, lai klasificētu krājumus kā bīstamus materiālus. Pēc tam, kad izveidojat pārdošanas pasūtījumu, kas ietver krājumu, kas ir klasificēts kā bīstams materiāls, sistēma ģenerē bīstamo materiālu dokumentāciju šim pārdošanas pasūtījumam, kad tas tiek nosūtīts.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Ieslēgt bīstamo materiālu līdzekli jūsu sistēmai

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Preču informācijas pārvaldība*
- **Līdzekļa nosaukums:** *Bīstamo materiālu preču informācija un nosūtīšanas dokumentācija*

## <a name="hazardous-material-regulations"></a>Bīstamo materiālu noteikumi

Lai izmantotu bīstamo materiālu procesus, vispirms ir jāizveido regula. Noteikumi nosaka, kā drukātais nosūtīšanas teksts tiek izveidots krājumam. Tie arī nosaka saistītos piegādes veidus.

Piedāvājam dažus kopējus noteikumus:

- **ADR** – regulas, kas saistītas ar starptautiskajiem bīstamo kravu autopārvadājumiem
- **KM 49** – Amerikas Savienoto Valstu preču pārvadāšanas noteikumi bīstamo kravu pārvadāšanai
- **IMDG** – SStarptautisko jūras bīstamo kravu kodekss (IMDG) kodekss
- **IATA** – Starptautiskās gaisa transporta asociācijas (IATA) noteikumi par bīstamajām kravām

Šīs regulas palīdz noteikt, kāda informācija jānorāda, drukājot krājuma nosūtīšanas tekstu. Varat definēt tik daudz noteikumu, cik nepieciešams.

> [!IMPORTANT]
> Funkcionalitāte, lai iestatītu informācijas kodus, kas ir saistīti ar bīstamiem materiāliem, nepadara jūsu uzņēmumu atbilstošu noteikumiem. Tas ir tikai rīks, kas palīdz veidot jūsu uzņēmuma procesus.

Parasti regula ir pieejama konkrētam transporta veidam, piemēram, jūras transports, autotransports vai gaisa transports. Tāpēc varat saistīt katru noteikumu ar piegādes veidu. Piegādes veids tiks izmantots, ja konkrēti dokumenti tiek drukāti Noliktavas pārvaldībā. Noliktavas vadībā katrs sūtījums ir saistīts ar pārvadāšanas pārvadātāju un pārvadātāja pakalpojumu, kas iestatīts **Transportēšanas** modulī. Piegādes veids ir saistīts arī ar nosūtīšanas pārvadātāju un pārvadātāja servisu. Palaižot pārskatu, piegādes veids tiek izmantots, lai atrastu nosūtīšanas drukas tekstu, kas ir saistīts ar izlaisto krājumu.

Šie iestatījumu dati nav specifiski katrai juridiskajai personai (uzņēmums). Tāpēc var būt kopīgs bīstamo materiālu informācijas kopums, kas tiek koplietots starp visām juridiskajām personām.

Katrai regulai varat definēt materiālu sarakstu un izmantot to kā veidņu sarakstu, kas ir saistīts ar izlaistajiem krājumiem. Katrai regulai varat arī definēt drukas iestatījumu. Drukāšanas iestatījumi ļauj definēt, kā tiek veidots krājuma nosūtīšanas teksts. Drukāšanas iestatījumi tiek izmantoti, lai veidotu nodotajam krājumam nosūtījuma drukas tekstu.

Lai iestatītu bīstamo materiālu noteikumus, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu regula**. Lapā **Bīstamo materiālu regula** varat izveidot jebkādu noteikumu skaitu un konfigurēt katru, lietojot laukus, kas aprakstīti šādās apakšsadaļās.

### <a name="hazardous-material-regulation-header"></a>Bīstamo materiālu noteikumu galvene

Katrai regulai ir kods un apraksts. Tālāk esošajā tabulā ir aprakstīti galvenē pieejamie lauki.

| Lauks | Apraksts |
|---|---|
| Noteikumu kods | Ievadiet kodu, lai identificētu bīstamo materiālu regulas ierakstu. |
| Apraksts | Ievadiet bīstamo materiāla regulas aprakstu. |

### <a name="print-setup-fasttab"></a>Drukāšanas uzstādīšanas kopsavilkuma cilne

Katrai regulai var būt jebkāds drukas iestatījumu skaits. Jūs nosakāt Drukāšanas iestatījumus **Drukāšanas iestatījumu** kopsavilkuma cilnē. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram drukāšanas iestatījumam.

| Lauks | Apraksts |
|---|---|
| Sērija | Norādiet kārtību, kādā lauki tiks pieminēti nosūtīšanas tekstā. |
| Drukāt lauku | Atlasiet lauku, ko iekļaut nosūtīšanas tekstā. Ne visi bīstamā materiāla lauki būs pieejami drukāšanai. Būs pieejami tikai kopējie lauki, kas tiek izmantoti, lai definētu nosūtīšanas tekstu dažādos noteikumos. Pirmais drukas lauks ir jādefinē kā lauku atdalītājs ar **Sērijas** vērtību *0* (nulle), lai to varētu izmantot kā atdalītāju starp citiem laukiem. Nepieciešama tikai viena atsauce uz lauku atdalītāju.<p>Ir pieejamas šādas vērtības:</p><ul></li><li>**Lauku atdalītājs** — Šis lauks tiek lietots kā teksta lauku atdalītājs. Nepieciešams tikai viens lauku atdalītājs secībā. Parasti šim drukas laukam ir jāiestata **Secības** vērtība uz *0* (nulle). Sistēma meklē lauka atdalītāju un izmanto pirmo, ko tas atrod sarakstā. Teksta vērtība, kas tiek izmantota virknē, nāks no lauka **Drukāt pēc**.</li><li>**Identifikācija** — Šis drukāšanas lauks ievieto [identifikācijas kodu un/vai aprakstu](#identification) drukātajā tekstā.</li><li>**Klase** — Šis drukāšanas lauks ievieto [klases kodu un/vai aprakstu](#classes) drukātajā tekstā.</li><li>**Nodaļa** — Šis drukāšanas lauks ievieto [nodaļas kodu un/vai aprakstu](#divisions) drukātajā tekstā.</li><li>**Iepakojuma grupa** — Šis drukāšanas lauks ievieto [iepakojuma grupas kodu un/vai aprakstu](#packing-group) drukātajā tekstā.</li><li>**Tuneļa kods un/vai apraksts** – Šis drukāšanas lauks ievieto [tuneļa kodu un/vai aprakstu](#tunnel) drukātajā tekstā.</li><li>**Piemērots nosūtīšanas nosaukums** — Šis drukāšanas lauks ievieto [atbilstošu piegādes nosaukumu](hazmat-items.md#hazmat-description) drukātajā tekstā.</li><li>**Tehniskais nosaukums** — Šis drukāšanas lauks ievieto [tehniskā nosaukuma kodu un/vai aprakstu](#technical-name) drukātajā tekstā.</li><li>**Transportēšanas kategorija** – Šis drukāšanas lauks ievieto [transportēšanas kategorijas kodu un/vai aprakstu](#transport-category) drukātajā tekstā.</li><li>**Uzglabāšana** — Šis drukāšanas lauks ievieto [uzglabāšanas kodu un/vai aprakstu](#stowage) drukātajā tekstā.</li><li>**Fiksēts teksts** — Šis drukāšanas lauks ievada tekstu, kas ir definēts šīs rindas **Fiksētā teksta** laukā.</li><li>**Etiķetes kods un/vai apraksts** – Šis drukāšanas lauks ievieto [etiķetes kodu un/vai aprakstu](#label) drukātajā tekstā.</li><li>**Lidmašīnu iepakojums** — Šis drukāšanas lauks ievieto [lidmašīnu iepakojuma instrukciju kodu un/vai aprakstu](#packing-instruction) drukātā tekstā.</li><li>**Ierobežots daudzums** — Šis drukas lauks pārbauda, vai krājums ir atzīmēts kā [ierobežota daudzuma vienība](hazmat-items.md#material-management) un, ja tā, ievada tekstu, kas ir definēts šīs rindas **Fiksētā teksta** laukā.</li><li>**Iepakojuma apraksts** — Šis drukāšanas lauks ievieto [iepakojuma aprakstu](#packing-description) drukātajā tekstā.</li></ul> |
| Drukāt pirms | Ievadiet tekstu, kas jādrukā pirms satura, ko definē **Drukāšanas lauka** iestatījums. |
| Drukāt pēc | Ievadiet tekstu, kas jādrukā pēc satura, ko definē **Drukāšanas lauka** iestatījums. |
| Drukāt ar iepriekšējo | Atzīmējiet šo izvēles rūtiņu, lai novērstu to, ka lauku atdalītājs tiek drukāts starp iepriekšējo lauku un šo lauku. Izmantojiet šo izvēles rūtiņu, lai drukātu laukus, kas ir vai nu neobligāti, vai iekļauti citā drukāšanas laukā. |
| Fiksēts teksts | Ja lauku **Drukāšanas lauks** iestatāt uz **Fiksētu teksts** vai **Ierobežots daudzums**, ievadiet tekstu, kas jādrukā. |
| Iekļaut izdrukā | Atlasiet, kuru vērtību vai vērtības no atlasītā drukāšanas lauka vajadzētu drukāt šai rindai. Varat izdrukāt kodu, aprakstu vai abus - kodu un aprakstu. |

### <a name="mode-of-delivery-fasttab"></a>Piegādes veida kopsavilkuma cilne

Regula ir koplietojama tabula, un tā nav raksturīga katrai juridiskajai personai. Tomēr piegādes veidi ir juridiskām personām specifiski. Tāpēc, iestatot piegādes veidu, jāatlasa attiecības starp regulu, juridisko personu un piegādes veidu.

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Piegādes veids** kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Uzņēmums | Atlasiet juridisko personu, ko saistīt ar šo regulu. |
| Piegādes veids | Balstoties uz jūsu izvēlēto juridisko personu, atlasiet piegādes veidu, kas ir jāsaista ar šo regulu. |

### <a name="country-fasttab"></a>Valsts kopsavilkuma cilne

Atsauces nolūkiem varat uzskaitīt tās valstis vai reģionus, uz kuriem attiecas regula. Tomēr, kad tiek izpildīti sūtījumu pārskati, lai noteiktu regulu, tiek izmantots tikai piegādes veids. Pārskatot noliktavas sūtījumu, nav tiešas saites ar piegādes veidu. Sūtījums var tikt saistīts arī ar nosūtīšanas pārvadātāju un pārvadātāja servisu. Definējot pārvadātāja pakalpojumu, tas ir jāsaista ar piegādes veidu. Šīs attiecības tiks izmantotas sūtījumu pārskatos, piemēram, preču transporta pavadzīmē, lai atrastu sūtījuma drukas tekstu krājumam.

Tālāk esošajā tabula apraksta lauku, kas ir pieejams **Valsts** kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Valsts/reģions | Atlasiet valsti/reģionu, ko saistīt ar regulu. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Materiāla kodi

Materiālu kodi izveido iestatījumus, kas saistīti ar noteiktu bīstamo komponentu, kas var tikt iekļauti izlaistajā produktā. Katrs materiālu kods attiecas uz specifisku bīstamo materiālu regulu, un tās definīcijai ir jāatbilst šai regulai. Kad tiek lietots materiālu kods izlaistam produktam, izmantojot **Materiālu koda** lauku, visi materiālu koda bīstamo materiālu iestatījumi tiek automātiski piemēroti šai precei. Tāpēc izlaisto preču iestatīšanas process ir ātrāks un mazāk tendēts uz kļūdu.

Lai pārvaldītu jūsu bīstamo materiālu definīcijas, veiciet tālāk norādītās darbības.

1. Dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu regula**.
2. Atlasiet regulu, lai iestatītu bīstamo materiālu definīciju.
3. Darbību rūts cilnē **Iestatījumi** atlasiet **Bīstamie materiāli**.
4. Laukā **Materiāla kods** ievadiet bīstamā materiāla definīcijas materiāla kodu. Jūs atlasīsiet šo vērtību, lietojot materiāla kodu izlaistajai precei.

    **Regulas koda** lauks ir tikai lasāms, un tas rāda regulu, kuru atlasījāt 2. solī.

5. Izmantojiet atlikušos šīs lapas laukus, lai izveidotu un iestatītu katru bīstamo materiālu, kas attiecas uz jūsu izvēlēto regulu. Pieejamie lauki ir bīstamo materiālu lauku apakškopa, kas ir pieejama atsevišķām izlaistām precēm. Papildinformāciju skatiet [Bīstamie materiāli precēs, pasūtījumos, sūtījumos un kravās](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Bīstamo materiālu klasifikācijas grupas

Katra bīstamo materiālu klasifikācijas grupa nosaka lauku vērtību grupu, kas izveido veidni. Šo veidni var izmantot vēlāk, kad izlaistajam krājumam tiek iestatīta bīstama materiālu informācija.

Kad izlaistam krājumam tiek piešķirts bīstamo materiālu klasifikācijas grupas kods, ar šo klasifikācijas grupu saistītā informācija tiks kopēta atbilstošajos krājuma laukos. Tāpēc varat vienkāršot uzstādīšanas procesus, izveidojot saistītu lauku vērtību kopu, ko bieži izmantojat kopā.

Šie iestatījumu dati nav specifiski katrai juridiskajai personai. Tāpēc var būt kopīgs bīstamo materiālu informācijas kopums, kas tiek koplietots starp visām juridiskajām personām.

Lai iestatītu bīstamo materiālu klasifikācijas grupas, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu klasifikācijas grupas**. Lapā **Bīstamo materiālu klasifikācijas grupa** varat izveidot jebkādu grupu skaitu un konfigurēt katru, lietojot laukus, kas aprakstīti šādās apakšsadaļās.

| Lauks | Apraksts |
|---|---|
| Grupas kods | Ievadiet kodu, lai noteiktu grupu. |
| Apraksts | Ievadiet grupas aprakstu. |
| Klases kods | Saistiet bīstamo materiālu [klases kodu](#classes) ar grupu. |
| Dalījuma kods | Saistiet bīstamo materiālu [nodaļas kodu](#divisions) ar grupu. |
| Iesaiņošanas grupas kods | Saistiet [iepakojuma grupas kodu](#packing-group) ar grupu. |
| Transportēšanas kategorijas kods | Saistiet [transportēšanas kategorijas kodu](#transport-category) ar grupu. |
| Reizinātājs | Ievadiet bīstamo materiālu reizinātāju, kas attiecas uz izvēlēto bīstamo materiālu klasi un dalījumu saskaņā ar piemērojamo regulu. Šis reizinātājs tiek izmantots kā daļa no formulas, kas aprēķina kopējos *bīstamos materiāla punktus*, kas ir ietverti noslodzē vai sūtījumā. Lai iegūtu vairāk informācijas par bīstamo materiālu punktiem un šo reizinātāju, skatiet [Materiālu pārvaldības kopsavilkuma cilne](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Bīstamo materiālu klases

Bīstamo materiālu klase parasti tiek kartēta ar to klašu sarakstu, kas ir nodrošinātas regulā, kurai atbilstat. Piemēram, ASV Regula CFR 49 norāda "3. klasi" kā viegli uzliesmojošu un uzliesmojošu šķidrumu. Varat iestatīt klases, kas atbilst klasificēšanai paredzētajiem materiāliem.

Katra klase tiks piešķirta materiālu iestatījumam materiālu sarakstā, kas ir saistīts ar šo regulu. Katram izlaistajam krājumam pēc nepieciešamības tiks piešķirta klase, lai aprakstītu preces bīstamību.

Šie iestatījumu dati nav specifiski katrai juridiskajai personai. Tāpēc var būt kopīgs bīstamo materiālu informācijas kopums, kas tiek koplietots starp visām juridiskajām personām.

Bīstamo materiālu klases darbojas kopā ar struktūrvienībām, grupām un saderības grupām šādos veidos:

- Kad izdotajam krājumam piešķirat bīstamu materiālu klasi, jums ir arī jāpiešķir [bīstams materiālu dalījums](#divisions).
- Varat lietot bīstamas materiālu klases kopā ar [bīstamo materiālu klasifikācijas grupām](#classification-groups), lai izveidotu krājumu iestatīšanas kodu veidni.
- Varat izmantot [bīstamo materiālu saderības grupas](#compatibility-groups), lai noteiktu, kuras bīstamās materiālu klases un dalījumus var nosūtīt kopā.

Lai iestatītu bīstamo materiālu klases, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu klase**. Lapā **Bīstamo materiālu klase** varat izveidot jebkādu klašu skaitu un konfigurēt katru, lietojot laukus, kas aprakstīti šādās apakšsadaļās.

| Lauks | Apraksts |
|---|---|
| Klases kods | Ievadiet kodu, lai noteiktu šo klasi. Šis kods tiek definēts krājumam. Tad tas tiks izmantots uzmeklēšanas sarakstos, kad izdotajam krājumam tiek piešķirta bīstama materiālu klase. |
| Apraksts | Ievadiet klases aprakstu. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Bīstamo materiālu dalījumi

Bīstamo materiālu dalījums ir bīstamo materiālu klases apakškopa. Katrai precei, kurā ir bīstami materiāli, ir jāpiešķir gan dalījums, gan klase.

Klasēm, kurām nav nevienas nodaļas, izveidojiet dalījumu, kur kods ir *0*. Piemēram, IATA regulā, 7. klases radioaktīvajiem materiāliem nav apakšnodaļu. Šādā gadījumā jūs izveidosiet *0* dalījumu, ko varat saistīt ar izlaisto preci, kad piešķirat klasi.

Šie iestatījumu dati nav specifiski katrai juridiskajai personai. Tāpēc var būt kopīgs bīstamo materiālu informācijas kopums, kas tiek koplietots starp visām juridiskajām personām.

Bīstamo materiālu dalījumi darbojas kopā ar klasēm, grupām un saderības grupām šādos veidos:

- Kad izdotajam krājumam piešķirat bīstamu materiālu dalījumu, jums ir arī jāpiešķir [bīstams materiālu klase](#classes).
- Varat lietot bīstamas materiālu dalījumus kopā ar [bīstamo materiālu klasifikācijas grupām](#classification-groups), lai izveidotu krājumu iestatīšanas kodu veidni.
- Varat izmantot [bīstamo materiālu saderības grupas](#compatibility-groups), lai noteiktu, kuras bīstamās materiālu klases un dalījumus var nosūtīt kopā.

Lai iestatītu bīstamo materiālu dalījumus, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu dalījums**. Lapā **Bīstamo materiālu dalījums** varat izveidot jebkādu dalījumu skaitu un konfigurēt katru, lietojot laukus, kas aprakstīti šādās apakšsadaļās.

| Lauks | Apraksts |
|---|---|
| Nodaļa | Ievadiet kodu, ko izmantot kā dalījuma atsauces numuru. |
| Apraksts | Ievadiet dalījuma aprakstu. |
| Klase | Sameklējiet un piešķiriet klasi, kurai pieder dalījums. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Bīstamo materiālu saderības grupas

Bīstamo materiālu saderības grupas nosaka, kuras bīstamās materiālu klases un dalījumus var nosūtīt kopā. Kad operatori izveido noliktavas noslodzes vai sūtījumus, tie var veikt saderības pārbaudi, kas izdos brīdinājumu, ja noslodze vai sūtījums ietver krājumus, kas visi nepieder vienai saderības grupai.

Šie iestatījumu dati nav specifiski katrai juridiskajai personai. Tāpēc var būt kopīgs bīstamo materiālu informācijas kopums, kas tiek koplietots starp visām juridiskajām personām.

Lai iestatītu bīstamo materiālu saderības grupas, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu saderības grupas**. Lapā **Bīstamo materiālu saderības grupa** varat izveidot jebkādu saderības grupu skaitu un konfigurēt katru, lietojot laukus, kas aprakstīti šādās apakšsadaļās.

### <a name="hazardous-material-compatibility-group-header"></a>Bīstamo materiālu saderības grupas galvene

Katrai saderības grupai ir kods un apraksts. Tālāk esošajā tabulā ir aprakstīti galvenē pieejamie lauki.

| Lauks | Apraksts |
|---|---|
| Saderības grupa | Ievadiet kodu, lai noteiktu saderības grupu |
| Apraksts | Ievadiet saderības grupas aprakstu. |

### <a name="compatibility-group-details"></a>Saderības grupas informācija

Katra saderības grupa nosaka sarakstu ar bīstamo materiālu klašu sadalījumiem un bīstamos materiālus, kurus var nosūtīt kopā.

| Lauks | Apraksts |
|---|---|
| Klase | Atlasiet bīstamo materiālu klasi, kas ir savietojama ar visām pārējām grupas klasēm. |
| Nodaļa | Atlasiet bīstamo materiālu dalījumu, kas pieder atlasītajai klasei. |

## <a name="hazardous-material-specification-values"></a>Bīstamo materiālu specifikācijas vērtības

Microsoft Dynamics 365 Supply Chain Management nodrošina vairākus bīstamo materiālu specifikāciju tipus. Katram tipam ir jāizveido centralizēta vērtību kopa katram attiecīgajam laukam. Lietotāji var atlasīt kādu no šīm vērtībām, kad tās konfigurē bīstamo materiālu definīcijas vai izlaistās preces. Supply Chain Management nodrošina lapu apkopojumu, kur var noteikt vērtības. Katra lapa ir paredzēta vienam specifikācijas tipam. Lai skatītu katras pieejamās specifikācijas aprakstu un informāciju par to, kā noteikt, kādas vērtības ir pieejamas, skatiet sekojošās apakšsadaļas.

Viens bīstamo materiālu specifikācijas piemērs ir _uzglabāšanas kods_, kas norāda, kā norādītos materiālus var uzglabāt transportēšanas laikā. Izmantojot šajā sadaļā sniegto informāciju, tiks izveidota centralizēta iekraušanas kodu kolekcija. Pēc tam šī kolekcija tiks parādīta nolaižamajā sarakstā lietotājiem, kad tie iestata izlaistā produkta iekraušanas kodu.

Šīs bīstamā materiāla specifikācijas vērtības nav raksturīgas katrai juridiskajai personai, tāpēc var būt kopīgo vērtību kopa, kas tiek koplietota starp visām juridiskajām personām.

Jūs izmantosiet [materiālu kodus](#hazmat-codes), lai izveidotu kopējas iestatījumu kopas katrai specifikācijai, kā tas attiecas uz doto regulu. Pēc tam varat izmantot atbilstošo kodu katrai izlaistajai precei pēc nepieciešamības. Lai iegūtu informāciju par to, kā piemērot bīstamo materiālu kodu noteiktai izlaistai precei un kā konfigurēt atsevišķus šīs preces iestatījumus šeit aprakstītajā specifikācijā, skatiet [Bīstamie materiāli precēs, pasūtījumos, sūtījumos un noslodzēs](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Bīstamo materiālu ārkārtas reaģēšana

*Bīstamo materiālu ārkārtas reaģēšanas* specifikācija norāda, ko darīt, ja rodas problēma, kad tiek transportēta prece, kas satur norādīto bīstamo materiālu.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu ārkārtas reaģēšana**. Lapā **Bīstamo materiālu ārkārtas reaģēšana** varat izveidot jebkādu vērtību skaitu un konfigurēt katru ar klasifikācijas kodu un īsu aprakstu.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Bīstamo materiālu identifikācija

*Bīstamo materiālu identifikācijas* specifikācija identificē bīstamā materiāla klasi vai būtību. Šī vērtība parasti ir kods, kas ir balstīts uz Apvienoto Nāciju organizācijas (ANO) standartu. Katra klase tiek identificēta ar kodu un aprakstu, un tā var noteikt ierobežojumus transportēšanas metodēm. Piemēram, lai identificētu uzliesmojošu krājumu vai materiālu, izveidojiet bīstamo materiālu klasi, kas izmanto kodu *FL* un aprakstu *uzliesmojošs*. Jūs arī nosakāt, ka klasi nedrīkst transportēt pa gaisu.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu identifikācija**. Lapā **Bīstamo materiālu identifikācija** varat izveidot jebkādu vērtību skaitu un konfigurēt katru, lietojot laukus, kas aprakstīti šādās apakšsadaļās.

| Lauks | Apraksts |
|---|---|
| Identifikācija | Ievadiet kodu, ko izmantot kā atsauces numuru, kas identificē šo bīstamā materiāla klasi. |
| Apraksts | Ievadiet šīs klases aprakstu. |
| Ierobežot transportēšanu pa gaisu | Atzīmējiet šo izvēles rūtiņu, lai norādītu, ka šo bīstamo materiālu klasi nedrīkst transportēt pa gaisu. |
| Ierobežot transportēšanu pa jūru | Atzīmējiet šo izvēles rūtiņu, lai norādītu, ka šo bīstamo materiālu klasi nedrīkst transportēt pa jūru. |

### <a name="hazardous-material-label"></a><a name="label"></a>Bīstamo materiālu etiķete

*Bīstamo materiālu etiķetes* specifikācija identificē bīstamo preču etiķeti, kas jālieto attiecīgajām izlaistajām precēm. Pašas etiķetes aprakstīs, kā prece jāapstrādā. Piemēram, jums ir prece, kas satur indīgu gāzi. Šādā gadījumā iestatiet etiķetes kodu, kas apzīmē indīgo gāzes etiķeti. Jūs arī veidojat savu biznesa procesu, lai tas uzmeklē šo vērtību, kad jūs piegādājat preces.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu etiķete**. Lapā **Bīstamo materiālu etiķete** varat izveidot jebkādu etiķešu skaitu un konfigurēt katru ar identifikācijas kodu un īsu aprakstu.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Bīstamo materiālu iesaiņošanas apraksti

*Bīstamo materiālu iepakojuma aprakstu* specifikācija norāda, kā bīstams krājums ir jāiepako. Piemēram, tas var būt iepakots noteiktā tērauda cilindra vai cita veida īpašā iepakojumā.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu iepakojuma apraksti**. Lapā **Bīstamo materiālu iepakojuma apraksti** varat izveidot jebkādu iepakojuma aprakstu skaitu un konfigurēt katru ar identifikācijas kodu un īsu aprakstu.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Bīstamo materiālu iesaiņošanas grupa

*Bīstamo materiālu iepakojuma grupas* specifikācija identificē bīstama krājumu iepakojuma grupu. Iepakojuma grupa ļauj definēt kodu un aprakstu, lai norādītu, kā bīstamie materiālu krājumi ir jāiepako transportēšanas vai nosūtīšanas laikā. Iepakojuma grupa ir piešķirta krājumam, izmantojot lapu **Preces bīstamības materiāli**.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu iepakojuma grupa**. Lapā **Bīstamo materiālu iepakojuma grupa** varat izveidot jebkādu iepakojuma grupu skaitu un konfigurēt katru ar identifikācijas kodu un īsu aprakstu.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Bīstamo materiālu iesaiņošanas instrukcija

*Bīstamo materiālu iepakošanas norādījumu* specifikācijā ir norādītas iepakošanas instrukcijas, kas jāievēro, kad attiecīgais bīstamais krājums ir sagatavots transportēšanai pa gaisu.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu iepakojuma norādījumi**. Lapā **Bīstamo materiālu iepakojuma norādījumi** varat izveidot jebkādu iepakojuma norādījumu identifikatoru skaitu un konfigurēt katru ar identifikācijas kodu un īsu aprakstu.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Bīstamo materiālu glabātuve

*Bīstamā materiāla uzglabāšanas* specifikācija norāda, kā produkts jāuzglabā uz kuģa, kad to transportē ar jūras transportu.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu uzglabāšana**. Lapā **Bīstamo materiālu uzglabāšana** varat izveidot jebkādu uzglabāšanas identifikatoru skaitu un konfigurēt katru ar identifikācijas kodu un īsu aprakstu.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Bīstamo materiālu transportēšanas kategorija

*Bīstamo materiālu transportēšanas kategorijas* specifikācijas parasti lieto, lai grupētu līdzīgas bīstamas preces pārskatos. Piemēram, transportēšanas kategorijas tiek izmantotas **Sūtījuma kopsavilkuma** pārskatā, kuru var drukāt no noliktavas sūtījuma ieraksta.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu transportēšanas kategorija**. Lapā **Bīstamo materiālu transportēšanas kategorija** varat izveidot jebkādu transportēšanas kategoriju skaitu un konfigurēt katru ar parādāmo nosaukumu un īsu aprakstu.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Bīstamo materiālu tehniskais nosaukums

*Bīstamo materiālu tehniskā nosaukuma* specifikāciju var izmantot, lai nodrošinātu bieži izmantojamu vai iekšēju uzņēmuma nosaukumu, kas apraksta katru materiālu.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu tehniskais nosaukums**. Lapā **Bīstamo materiālu tehniskais nosaukums** varat izveidot jebkādu tehnisko nosaukumu skaitu un konfigurēt katru ar parādāmo nosaukumu un īsu aprakstu.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Bīstamo materiālu tunelis

*Bīstamo materiālu tuneļa* specifikācija ierobežo tuneļu tipus, caur kuriem var transportēt bīstamos materiālus, identificējot izmantojamo tuneļu tipus. Tuneļu kategorijas ir izveidotas ar piemērojamiem noteikumiem par bīstamo materiālu transportu. Šī specifikācija parasti attiecas tikai uz ceļu transportu.

Lai iestatītu vērtības šai specifikācijai, dodieties uz **Preces informācijas pārvaldība \> Iestatījumi \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu tunelis**. Lapā **Bīstamo materiālu tunelis** varat izveidot jebkādu tuneļu identifikatoru skaitu un konfigurēt katru ar identifikācijas kodu un īsu aprakstu.
