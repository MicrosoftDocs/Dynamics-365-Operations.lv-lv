---
title: Kas jauns vai mainīts mobilajā programmā Warehouse Management
description: Šajā tēmā ir uzskaitīti jaunie un mainītie līdzekļi katrai Microsoft Dynamics 365 Supply Chain Management Warehouse Management mobilās programmas izlaistajai versijai.
author: ivanv-microsoft
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 43d1381e73d5659bfd6ae6c6d944b7e6918b681a4f89df7ad23abbed5b4a0d3c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720088"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Kas jauns vai mainīts mobilajā programmā Warehouse Management

[!include [banner](../includes/banner.md)]

Šajā tēmā ir uzskaitīti jaunie līdzekļi, labojumi, uzlabojumi un zināmas problēmas katrai Microsoft Dynamics 365 Supply Chain Management Warehouse Management mobilās programmas izlaistajai versijai.

## <a name="2070"></a>2.0.7.0

### <a name="new-features-fixes-and-improvements-in-version-2070"></a>Jauni līdzekļi, labojumi un uzlabojumi versijā 2.0.7.0

- Pievienota sadaļa lapai **Par**, kas pārbauda programmas jaunāko izlaisto versiju.
- Atvieglo datu pārvilkšnu un pavilkšnu starp lapām.
- Mainīta darba saraksta ikona augošā/dilstošā secībā.
- Samazinātās uzcenojumi kartē **Detaļas**, lai tie atbilstu plašākai informācijai.
- Tika piemēroti dažādi veiktspējas uzlabojumi, lai samazinātu problēmu, ka lietotne laika gaitā kļūst lēnāka.
- Ja uz ekrāna ir vairāk vadīklu, nekā nepieciešams, tā rezultātā lapošanā spinera vadīkla vairs neritina tāpat kā lapa.
- Nosaka prioritāti pēdējās skenētās vērtības rādīšanai, nevis uzdevuma nosaukuma rādīšanai, tāpēc, ja tās pārklājas, uzdevuma nosaukums tiks saīsināts.
- Ir fiksētas dažādas problēmas, kuru dēļ sistēma nereaģēja.
- Dažās valodās teksts dažādās vietās vairs netiek nogriezts.
- Programma pēc noklusējuma darbojas pilnekrāna režīmā.
- Fiksētā problēma, kas dažkārt izraisa to, ka skenējumus var ignorēt pamatlapā ar noteiktām ierīcēm.

### <a name="known-issues-in-version-2070"></a>Zināmās problēmas versijā 2.0.7.0

- Dažās ierīcēs, startējot programmu vai sākot uzdevumu, saņemsit šādu kļūdas ziņojumu: "Nevar atrast šim izmēram piemērotu skatu." Ja jebkurā no jūsu ierīcēm redzat šo kļūdas ziņojumu, jums šajā ierīcē ir pazemināt mobilā programma Warehouse Management līdz versijai 2.0.6.0 un jāgaida, līdz tiks izlaista nākamā programmas versija.

## <a name="version-2060"></a>Versija 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Jauni līdzekļi, labojumi un uzlabojumi versijā 2.0.6.0

Šajā versijā ir iekļauti šādi jauni līdzekļi, labojumi un uzlabojumi:

- Demonstrācijas režīms tagad parāda visas etiķetes ierīces valodā.
- Ir mazāk ticams, ka saņemsit šādu kļūdas ziņojumu: “Nevar atrast norādītajam izmēram piemērotu skatu.”
- Ir palielināts minimālais darba karšu augstums (ja darbu sarakstā ir konfigurēti trīs vai mazāk lauku).
- Ir uzlabotas robežas (izbalinātas) detalizētās informācijas karšu apakšdaļā.
- Nederīgi simboli XML failos, ar kuriem tiek veikta apmaiņa ar serveri, tagad tiek veiksmīgi apstrādāti. (Piemēram, nedrukājamās rakstzīmes tagad tiek veiksmīgi apstrādātas un vairs neliks programmai pārtraukt reaģēt.)
- HTTP kļūdas (piemēram, "kļūda 503"), kad servera pieprasījums tiek iesniegts, tagad tiek veiksmīgi apstrādāts.
- Parādītās kļūdas gadījumā opciju saraksts vairs netiek automātiski rādīts kombinēto lodziņu vadīklām.
- Programma vairs nepārtrauc reaģēt lietotāja iestatījumos atlasītās parādāmās orientācijas dēļ.
- Preču attēli tagad tiek rādīti pašapkalpošanās vidēs. (Šīs izmaiņas attiecas tikai uz zemas izšķirtspējas versijām. Failu pārvaldības pakalpojums neatbalsta pilna lieluma attēlus pašapkalpošanās vidēs.)
- Ir fiksēta problēma, kas saistīta ar nulles daudzuma īsu savākšanu.
- Programma vairs nepārtrauc reaģēt, ja detalizētas informācijas kartē tiek rādīti vairāki identiski lauki.

### <a name="known-issues-in-version-2060"></a>Zināmās problēmas versijā 2.0.6.0

Šajā versijā pastāv šādas zināmās problēmas:

- Programma (it īpaši darbu saraksts) laika gaitā kļūst lēnāka.
- **Windows versija:** Ja USB pistoli izmanto skenēšanai sistēmā Windows, nekonsekventi rezultāti izraisa skenēto simbolu sajaukšanu.

## <a name="version-2050"></a>Versija 2.0.5.0

Šajā versijā ir iekļauti šādi jauni līdzekļi, labojumi un uzlabojumi:

- Klienta noslēpums vairs nav paslēpts savienojuma iestatījumu uzstādījumos.
- Tagad var īlgi nospiest visu tekstu, lai to skatītu pilnībā.
- Kļūdas ziņojums, kad trūkst glabāšanas atļauju, ir uzlabots.
- Dažām plūsmām pievienotas jaunas kontroles secības.
- Iesniegšanas poga vairs nav pieejama nepareizi loga izmēra dēļ.
- Tagad, kad tiek izmantoti lielāki pogu izmēri, slīdņi var pāriet uz mazākiem ekrāniem.
- Četru pogu pārklājums vairs nav nogriezts.
- Tagad tastatūra atbalsta dzēšanas pogu.
- Ir novērsta spilgtuma problēma, kas var rasties, nospiežot tastatūru.
- Dažādas demonstrācijas datu problēmas ir fiksētas.
- Problēma, kas ietekmēja skaitliskos laukus detalizētās informācijas lapā, ir novērsta.
- Dažās ierīcēs ekrāna tastatūra vairs nepazūd.
- Dažādas lietotāja interfeisa (UI) kļūdas ir novērstas, piemēram, kļūdas, kas ietekmēja fona krāsu un novietojumu.
- Krievijas valodas UI ir uzlabota.
- Ir fiksētas dažādas problēmas, kuru dēļ sistēma nereaģēja.
- Problēma, kas saistīta ar kalkulatora atkārtotu atvēršanu, ir novērsta.
- **Android versija:** problēma, kuras dēļ Android 4.4 pārstāja reaģēt startēšanas laikā, ir novērsta.
- **Android versija:** minimālā mērogošana ir samazināta līdz 50 procentiem.

## <a name="version-2040"></a>Versija 2.0.4.0

Versija 2.0.4.0 bija Warehouse Management mobilās lietotnes pirmais vispārpieejamais laidiens.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Jauni līdzekļi, labojumi un uzlabojumi versijā 2.0.4.0

Šī versija iepazīstina ar tālāk minētajiem jaunajiem līdzekļiem, labojumiem un uzlabojumiem, kas priekšskatījuma versijā nebija pieejami:

- Ja detalizētas informācijas kartē ir iekļautas divas etiķetes ar identiskiem datiem, viena no etiķetēm tiek paslēpta.
- Pēc noklusējuma tiek parādītas īpašās rakstzīmes, un iespēja tās slēpt ir noņemta no lietotāja iestatījumiem.
- Atspējotās iesniegšanas pogas kompaktā rokas skatā tagad tiek rādītas kā nepieejamas.
- Vadības ierīču secības loģikas maiņa nodrošina vienmērīgāku mērogošanu starp ierīcēm. Tāpēc mazāk nepieciešams pielāgot fontu vai pogu mērogošanu.
- Noklusējuma krāsas tēma ir mainīta uz *Tumša*.
- Lentes skatā ir pievienota atspējotās iesniegšanas pogas trūkstošā ikona.
- Taimauta izņēmumi tagad aizved jūs uz savienojuma lapu, nevis parāda rindā esošu kļūdu.
- Ja iesniegšanas darbības nav pieejama (piemēram, **Labi**, **Jā**, **Akceptēt**, **Gatavs** vai **Pabeigts**) iesniegšanas poga tiek deaktivizēta.
- Programmas stabilitātes uzlabojumi.
- Drošības ievainojamībai ir labojums [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Windows versija:** ir fiksēta problēma operētājsistēmā Windows, kur izvēlnes nebija responsīvas pēc loga lieluma maiņas.

### <a name="known-issue-in-version-2040"></a>Zināmā problēma versijā 2.0.4.0

Šajā versijā pastāv šāda zināmā problēma:

- Šai versijai ir problēma ar ierīcēm, kas izmanto Android 4.4. Izmantojot programmu šajā Android versijā, var rasties problēmas.
