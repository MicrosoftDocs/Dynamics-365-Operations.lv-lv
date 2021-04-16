---
title: Puse un globālā adrešu grāmata
description: Šajā tēmā ir aprakstīta dubultās rakstīšanas Puses un globālās adrešu grāmatas funkcionalitāte.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750792"
---
# <a name="party-and-global-address-book"></a>Puse un globālā adrešu grāmata

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Puse un globālā adrešu grāmata ir jēdzieni Finance and Operations lietojumprogrammās. Puse var būt organizācija vai persona. Ir ērti globāli glabāt un pārvaldīt **Puses** rekvizītus, piemēram, nosaukumu, valodu, kontaktpersonas un adreses. Ja īpašuma vērtība mainās vienā vietā, tā atspoguļojas visās vietās, kur **Puse** ir iesaistīta.

## <a name="party"></a>Puse

Jēdziens *Puse* nozīme uzņēmumā iesaistīta persona vai organizācija. Izmantojot Puses koncepciju, personai vai organizācijai uzņēmumā var būt vairāk nekā viena loma (darbinieks, klients, piegādātājs vai kontaktpersona). Lomas pamatā ir konteksts un mērķis. Lūk, daži piemēri no diviem fiktīviem uzņēmumiem – Contoso un Fabrikam.

+ **Nodarbinātais**: darbinieks. Piemēram, Contoso darbinieks.
+ **Kreditors**: piegādātāju organizācija vai vienīgais īpašnieks, kas piegādā preces vai sniedz pakalpojumus uzņēmumam. Piemēram, ja Fabrikam pārdod krājumus Contoso, tad Fabrikam ir kreditora lomā.
+ **Kontaktpersona** : persona, ar kuru jāsazinās. Piemēram, ja Contoso pērk krājumus no Fabrikam, Contoso darbinieks sazināsies ar kontaktpersonu Fabrikam.
+ **Debitors**: klients ir persona vai uzņēmums, kas pērk lietas no uzņēmuma. Piemēram, ja Contoso pērk krājumus no Fabrikam, tad Contoso ir Fabrikam debitors.

Puses modelis bieži tiek izmantots, lai pārstāvētu vidējas un sarežģītas attiecības starp organizācijām un cilvēkiem, jo īpaši, ja pusei ir vairāk nekā viena loma. Tālāk ir sniegti daži izplatīti piemēri.

+ Puse var būt gan debitors, gan kreditors. Piemēram, Ziemeļamerikā Fabrikam pārdod elektriskos vadus Contoso un iepērk samontētus skaļruņus no Contoso. Eiropā Fabrikam pārdod detaļas Contoso, bet neko nepērk no Contoso.
+ Puse var būt gan darbinieks, gan debitors. Piemēram, Contoso darbinieks pērk elektroniku no Contoso personiskai lietošanai.
+ Starp personu un organizāciju var būt attiecības daudzi pret daudziem. Piemēram, Fabrikam sniedz pakalpojumu speciālistus un nodarbina prakses koordinatoru. Koordinators atbilst servisa speciālistiem par vairāku Fabrikam klientu darba pieprasījumiem. Contoso ir viens no klientu kontiem. Kad Contoso ir nepieciešams speciālists, Contoso sazinās ar koordinatoru, kurš pēc tam atvieglo pieprasījumu. Koordinators apstrādā pieprasījumus visiem klientiem, izveidojot relāciju daudzi pret daudziem.

Šajā attēlā redzams Puses datu modelis:

![Puses datu modelis](media/party-gab-image1.png)

> [!Tip]
> Mēģinot izveidot jaunu konta ierakstu, izmantojiet lauku "Puse", lai meklētu ierakstu pēc nosaukuma. Gadījumā, ja atrodat ierakstu, jums vienkārši jāatlasa ieraksts. Sistēma automātiski aizpilda visus datus no puses. Nav manuāli jāievada visi nepieciešamie lauki. Šo darbību var atrast konta, kontaktpersonu un kreditoru izsūtāmajās veidlapās.

Ne visas Finance and Operations programmu pušu lomas tiek atbalstītas ar dubultu raksti. Pilnu pušu lomu sarakstu skatiet rakstā [Globālās adrešu grāmatas pārskats](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Globālā adrešu grāmata

Globālā adrešu grāmata ir to organizāciju un privātpersonu pasta un elektronisko adrešu katalogs, kas piedalās uzņēmumā.

Globālajā adrešu grāmatā tiek glabāts un apstrādāts tik daudz pasta adrešu un elektronisko adrešu, cik nepieciešams. Piemēram, pieņemsim, ka Fabrikam ir gāzes stacijas 50 vietās. Katrai atrašanās vietai ir atšķirīga pasta adrese, e-pasts un tālruņa numurs. Par visiem biznesa pirkumiem tiek izrakstīts rēķins uz galveno gāzes staciju, bet pirkumi tiek nosūtīti tieši uz konkrēto gāzes staciju, kas pieprasīja pirkumu. Globālajā adrešu grāmatā galvenā gāzes stacija tiek glabāta kā rēķina adrese un katra gāzes stacija kā Fabrikam piegādes adrese. Adreses var saglabāt vienu reizi un pēc vajadzības izgūt piedāvājumiem un pasūtījumiem.

Personai vai organizācijai var būt vairākas lomas, pamatojoties uz biznesa kontekstu. To darot, viņu pasta adreses un elektroniskās adreses var būt vienādas. Šajā gadījumā adreses maiņai vienā lomā jāparādās otrā lomā un otrādi. Globālā adrešu grāmata saglabā un apstrādā adreses visā pasaulē.

![Globālās adrešu grāmatas datu modelis](media/party-gab-image2.png)

## <a name="contacts"></a>Kontaktpersonas

Customer Engagement programmās *Kontaktpersona* ir persona. Tomēr tabula **Kontaktpersona** ir pārslogota, lai pārstāvētu personu, portāla lietotāju, B2C klientu vai kreditoru. Pārstāvība ir netieša, un jūs nevarat noteikt atšķirību, neizmeklējot saistītos darījumus. Tabulai **Kontaktpersona** ir ierobežota attiecība 1:1 ar tabulu **Konts**. Puses un globālās adrešu grāmatas modeļa daļu, dubultā rakstīšana ievieš skaidrus klasifikācijas rekvizītus, un dubultā rakstīšana pieļauj N:N attiecības starp **Kontaktpersonu** un organizāciju (uzņēmuma entītiju vai kreditora entītiju).

Ir divu veidu **Kontaktpersonas** rindas:

+ Svītrota kontaktpersona — kontaktpersonas rinda ar obligātu vērtību laukā **Uzņēmums**.
+ Nesaskaņota kontaktpersona — kontaktpersonas rinda ar tukšu lauku **Uzņēmums**.

Tabulā **Kontaktpersona** var saglabāt šāda veida rindas:

Rindas tips | Apraksts
---|---
Persona, kas ir klients, piemēram, pārdodama kontaktpersona vai B2C klients. | Svītrots kontaktpersonas ieraksts, kurā lauks **Uzņēmums** nav tukšs un lauks **Ir klients** ir iestatīts uz **Jā**.
Persona, kas ir kreditors, piemēram, individuālais īpašnieks, piemēram, kreditors. | Svītrots kontaktpersonas ieraksts, kurā lauks **Uzņēmums** nav tukšs un lauks **Ir kreditors** ir iestatīts uz **Jā**.
Persona, kas ir gan debitors, gan kreditors. | Svītrots kontaktpersonas ieraksts, kurā lauks **Uzņēmums** nav tukšs, lauks **Ir klients** ir iestatīts uz **Jā** un lauks **Ir kreditors** ir iestatīts uz **Jā**. Perosona var būt gan viena produkta ražotājs, gan cita produkta patērētājs. Gan Finance and Operations programmas, gan duālā rakstīšana atbalsta šīs attiecības.
Persona, kas ir organizācijas kontaktpersona, bet nav ne klients, ne kreditors. | Nesvītrots kontaktpersonas ieraksts, kurā lauks **Uzņēmums** ir tukšs, lauks **Ir klients** ir iestatīts uz **Nē** un lauks **Ir kreditors** ir iestatīts uz **Nē**.

## <a name="contact-for-party"></a>Puses kontaktpersona

**Puses kontaktpersona** glābā un apstrādā N:N attiecības starp **Konta** rindām un **Kontaktpersonu** rindām. Tas var filtrēt svītrotās **Kontaktpersonu** rindas no nesvītrotām rindām un saistīt tikai nesvītrotās **Kontaktpersonu** rindas ar **Konta** vai **Kreditora** rindām.

Piemēram, Nataša Džonsa un Migels Reiss ir veterinārārsti, kas rūpējas par saimniecībām savās teritorijās. Nataša apkalpo Sietlas rajonu, un Migels apkalpo Kentas rajonu. Customer Engagement lietotnē saimniecības ir pārstāvētas kā klienti un veterinārārsti ir kontaktpersonas. Viens **Kontaktpersonas** ieraksts Natašai ir saistīts ar visām saimniecībām, ar kurām Nataša strādā. Līdzīgi, viens **Kontaktpersonas** ieraksts Migelam ir saistīts ar visām saimniecībām, ar kurām Migels strādā.

Šīs attiecības tiek glabātas tabulā **Puses kontaktpersona**. Informāciju var atrast ārpus saraksta veidlapās:

+ Veidlapā **Konts** ir cilne **Saistītās kontaktpersonas**. Izmantojiet šo cilni, lai saistītu vienu vai vairākas kontaktpersonas ar rindu **Konts**. Šajā veidlapā jūs piešķirat kontaktpersonu organizācijai. Pēc kontaktpersonu piešķiršanas, vienu var izvēlēties kā šī uzņēmuma primāro kontaktpersonu. Izmantojot veidlapu **Ātrā izveide**, var izvēlēties tikai kontaktpersonu. Darbība ir tāda pati, ja izmantojat veidlapu **Kreditors** un ieraksta tips ir **Organizācija**.
+ Atrodoties veidlapā **Kontaktpersona**, un rinda ir klients vai kreditors, vai abi (svītrota kontaktpersona), tur ir cilne **Saistītās kontaktpersonas**. Izmantojiet šo cilni, lai saistītu vienu vai vairākas kontaktpersonas. Šajā veidlapā jūs piešķirat kontaktpersonu B2C klientam vai kreditoram. Pēc kontaktpersonu piešķiršanas, vienu var izvēlēties kā primāro kontaktpersonu. Izmantojot veidlapu **Ātrā izveide**, var izvēlēties tikai kontaktpersonu.
+ Atrodoties veidlapā **Kontaktpersona**, un rinda ir kontaktpersona (nesvītrota kontaktpersona), tur ir cilne **Saistītās organizācijas**. Izmantojiet šo cilni, lai saistītu vienu vai vairākus klientus vai kreditorus. Šajā veidlapā jūs piešķirat klientu vai kreditoru pamatā esošajai kontaktpersonai. Debitors vai kreditors var būt organizācija, persona vai abi. No četriem laukiem noteiktā laikā var izvēlēties tikai vienu vērtību.

    ![Cilne Saistītās organizācijas](media/party-gab-image3.png)

    + Ja izvēlaties **Puses ID**, pamatā esošā kontaktpersona tiek piešķirta visām izvēlētās puses lomām.
    + Ja izvēlaties **Saistītā kontaktpersona**, tiek atlasīta svītrotā kontaktpersona, kuras tips ir persona.
    + Ja izvēlaties **Saistītais konts** vai **Kreditors**, jūs atlasāt organizāciju.

    Neatkarīgi no jūsu izvēles asociācija tiek izveidota puses līmenī un piemērojama visām puses lomām un saglabāta vienībā "Puses kontaktpersona".

> [!Note]
> Customer Engagement programmas tabulas **Puses kontaktpersona** parādāmais nosaukums ir **Debitora/Kreditora kontaktpersona**.

Atverot rindu **Kontaktpersona**, kurā **Ir Debitors** ir iestatīts uz **Nē** un **Ir Kreditors** uz **Nē**, ir redzama **Saistītās organizācijas** cilne. Izmantojiet šo cilni, lai saistītu kontaktpersonu ar vienu vai vairākām debitoru vai kreditoru organizācijām.

Atverot rindu **Kontaktpersona**, kurā **Ir Debitors** ir iestatīts uz **Jā** vai **Ir Kreditors** uz **Jā**, ir redzama **Saistītās kontaktpersonas** cilne. Izmantojiet šo cilni, lai saistītu vienu vai vairākas kontaktpersonas.

## <a name="postal-address"></a>Pasta adrese

Veidlapās **Konts**, **Kontaktpersona** un **Kreditors** ir ieviesta jauna cilne ar nosaukumu **Adreses**. Kā parādīts šajā attēlā, **Adreses** atbalsta N adreses, izmantojot režģi:

![Pasta adreses režģis](media/party-gab-image4.png)

+ Kolonnā **Pasta adrešu lomas** ir uzskaitīti adrešu nolūki.
+ Kolonna **Ir primārā** uzskaita primārās adreses.
+ Kolonnas **Adreses numurs** uzskaita adrešu secību.
+ Poga **+ Jauna adrese** ļauj izveidot jaunu adresi. Adrešu skaits nav ierobežots.

Lauki **1. adrese** un **2. adrese** veidlapas **Konts** cilnē **Kopsavilkums** atbilst attiecīgi **Piegādes** un **Rēķina** adresēm.

![Kopsavilkuma cilne pasta adresei](media/party-gab-image5.png)

Lauki **1. adrese**, **2. adrese** un **3. adrese** veidlapas **Konts** cilnē **Kopsavilkums** atbilst attiecīgi **Biznesa**, **Piegādes** un **Rēķina** adresēm.

## <a name="electronic-address"></a>Elektroniskā adrese

Veidlapās **Konts**, **Kontaktpersona** un **Kreditors** ir ieviesta jauna cilne ar nosaukumu **Elektroniskās adreses**. Kā parādīts šajā attēlā, **Adreses** atbalsta N adreses, izmantojot režģi:

![Elektroniskās adreses režģis](media/party-gab-image6.png)

+ Kolonna **Veids** uzskaita adreses veidu.
+ Kolonna **Ir primārā** uzskaita primārās adreses.
+ Kolonnā **Nolūks** ir uzskaitīti elektronisko adrešu nolūki.
+ Poga **+ Jauna elektroniskā adrese** ļauj izveidot jaunu adresi. Adrešu skaits nav ierobežots.

Elektroniskās adreses ir pieejamas tikai šajā režģī. Turpmākajos laidienos visi elektronisko un pasta adrešu lauki tiks noņemti no citām cilnēm, piemēram, cilnēm **Kopsavilkums** un **Detalizēta informācija**.

## <a name="setup-instructions"></a>Iestatīšanas instrukcijas

Ja jūs esat esošs duālās rakstīšanas debitors, tad ir nepieciešamas šādas iestatīšanas instrukcijas. Pretējā gadījumā varat izlaist šo sadaļu.

1. Apturiet tālāk norādītās kartes, jo tās vairs nav obligātas. Tā vietā palaidiet kontaktpersonu V2 (msdyn_contactforparties) karti.

    + CDS kontaktpersonas V2 un kontaktpersonas (attiecas uz debitoru kontaktpersonām)
    + CDS kontaktpersonas V2 un kontaktpersonas (attiecas uz kreditoru kontaktpersonām)

2. Tālāk minētie elementu kartējumi ir atjaunināti puses funkcionalitātei, tāpēc tiem ir jālieto jaunākā versija.

Atbilstību karte | Atjaunināt līdz šai versijai | Izmaiņas
---|---|---
Debitori V3 (konti) | 1.0.0.5 |Noņēma PusesNumurs un citus ar pusi saistītos laukus, piemēram, vārdu, personas datus, pasta adrešu laukus, elektroniskās kontaktinformācijas laukus u.c.
Debitoru V3 (kontaktpersonas) | 1.0.0.5 | Noņēma PusesNumurs un citus ar pusi saistītos laukus, piemēram, vārdu, personas datus, pasta adrešu laukus, elektroniskās kontaktinformācijas laukus u.c.
Kreditori V2 (msdyn_vendors) | 1.0.0.6 | Noņēma PusesNumurs un citus ar pusi saistītos laukus, piemēram, vārdu, personas datus, pasta adrešu laukus, elektroniskās kontaktinformācijas laukus u.c.
CDS pārdošanas piedāvājuma virsraksti (piedāvājumi) | 1.0.0.6 | Kontaktpersona aizstāta ar ContactforParty atsauci.
Pārdošanas rēķinu galvenes V2 (rēķini) | 1.0.0.4 | Kontaktpersona aizstāta ar ContactforParty atsauci.
CDS pārdošanas pasūtījumu virsraksti (pārdošanas pasūtījumi) | 1.0.0.5 | Kontaktpersona aizstāta ar ContactforParty atsauci.
Kontakti V2 (msdyn_contactforparties) | 1.0.0.2 | Šī ir jauna karte. Ja jums ir iepriekšējā puses risinājuma versija, noteikti atjauniniet šo karti līdz pēdējai versijai, kā norādīts.
CDS puses pasta adrešu atrašanās vietas (msdyn_partypostaladdresses) | 1.0.0.1  | Šī ir jauna karte, kas ir pievienota kā daļa no iepriekšējās puses priekšskatījuma laidiena.
CDS pasta adreses vēsture V2 (msdyn_postaladdresses) | | Šī ir jauna karte, kas ir pievienota kā daļa no iepriekšējās puses priekšskatījuma laidiena.
CDS puses pasta adrešu atrašanās vietas (msdyn_postaladdresscollections) | | Šī ir jauna karte, kas ir pievienota kā daļa no iepriekšējās puses priekšskatījuma laidiena.
Puses kontaktpersonas V3 (msdyn_partyelectronicaddresses) | | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.

## <a name="templates"></a>Veidnes

Tabulas karšu vākšana darbojas kopā puses un globālās adrešu grāmatas mijiedarbībai, kā redzams nākamajā tabulā.

Finance and Operations programma | Customer engagement programma     | Apraksts
----------------------------|-----------------------------|------------
[Kontaktpersonu amati](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Debitori V3](mapping-reference.md#101) | konti |
[Debitori V3](mapping-reference.md#116) | kontaktpersonas |
[CDS puses](mapping-reference.md#220) | msdyn_parties |
[CDS puses pasta adreses vietas](mapping-reference.md#233) | msdyn_partypostaladdresses |
[CDS pasta adreses vēsture V2](mapping-reference.md#235) | msdyn_postaladdresses |
[CDS pasta adreses vietas](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS pārdošanas piedāvājuma virsraksts](mapping-reference.md#215) | piedāvājumi |
[CDS pārdošanas pasūtījumu virsraksti](mapping-reference.md#217) | salesorders |
[Noslēguma frāzes](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Kontaktpersonas V2](mapping-reference.md#221) | msdyn_contactforparties |
[Lēmumu pieņemšanas lomas](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Nodarbinātības darbu funkcijas](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Lojalitātes programmu līmeņi](mapping-reference.md#226) | msdyn_loyaltylevels |
[Puses kontaktpersonas V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Personas rakstura veidi](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Pārdošanas rēķinu galvenes V2](mapping-reference.md#118) | rēķini |
[Uzrunas](mapping-reference.md#228) | msdyn_salutations |
[Kreditori V2](mapping-reference.md#202) | msdyn_vendors |

Papildinformāciju skatiet sadaļā [Dubultā ieraksta kartēšanas atsauce](mapping-reference.md).
