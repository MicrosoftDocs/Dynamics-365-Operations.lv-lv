---
title: Puse un globālā adrešu grāmata
description: Šajā tēmā ir aprakstīta dubultās rakstīšanas Puses un globālās adrešu grāmatas funkcionalitāte.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 1e2dcfa69308f6691e787a1ff1893f9080dcaef1
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717451"
---
# <a name="party-and-global-address-book"></a>Puse un globālā adrešu grāmata

[!include [banner](../../includes/banner.md)]



*Puse* un *globālā adrešu grāmata ir* koncepcijas finanšu un operāciju programmās. Puse var būt organizācija vai persona. Ir ērti globāli glabāt un pārvaldīt puses rekvizītus, piemēram, nosaukumu, valodu, kontaktpersonas un adreses. Tad, ja īpašuma vērtība mainās vienā vietā, izmaiņas atspoguļojas visās vietās, kur puse ir iesaistīta.

## <a name="party"></a>Puse

Puse ir persona vai organizācija, kas ir iesaistīta biznesā. Ja tiek izmantots puses jēdziens, personai vai organizācijai uzņēmumā var būt vairāk nekā viena loma (piemēram, darbinieks, klients, piegādātājs vai kontaktpersona). Lomas pamatā ir konteksts un mērķis. Šeit sniegti daži divu fiktīvu uzņēmumu — Contoso un Fabrikam lomu piemēri:

+ **Nodarbinātais** - darbinieks. Piemērs ir Contoso darbinieks.
+ **Kreditors** - piegādātāju organizācija vai vienīgais īpašnieks, kas piegādā preces vai sniedz pakalpojumus uzņēmumam. Piemēram, ja Fabrikam pārdod preces uzņēmumam Contoso, Fabrikam ir Contoso kreditors.
+ **Kontaktpersona** - persona, ar kuru jāsazinās. Piemēram, ja Contoso iegādājas piegādes no Fabrikam, contoso darbinieki sazinās ar uzņēmumu Fabrikam.
+ **Debitors** - persona vai uzņēmums, kas pērk lietas no uzņēmuma. Piemēram, ja Contoso pērk piegādes no Fabrikam, Contoso ir Fabrikam debitors.

Puses modelis bieži tiek izmantots, lai pārstāvētu vidējas un sarežģītas attiecības starp organizācijām un cilvēkiem, jo īpaši, ja pusei ir vairāk nekā viena loma. Tālāk ir sniegti daži izplatīti piemēri.

+ Puse var būt gan debitors, gan kreditors. Piemēram, Ziemeļamerikā Fabrikam pārdod elektriskos fabrikas contoso un pērk no Contoso saliktās fabrikas. Eiropā Fabrikam pārdod daļas uzņēmumam Contoso, bet neko nepērk no Contoso.
+ Puse var būt gan darbinieks, gan debitors. Piemēram, Contoso darbinieks pērk elektroniku no Contoso personiskai lietošanai.
+ Starp personu un organizāciju var būt attiecības daudzi pret daudziem (N:N). Piemēram, Fabrikam sniedz pakalpojumu speciālistus un nodarbina prakses koordinatoru. Norīkojuma koordinators atbilst servisa speciālistiem par vairāku Fabrikam klientu darba pieprasījumiem. Contoso ir viens no Fabrikam debitoriem. Ja contoso pieprasa pakalpojumu speciālistu, tas sazinās ar izvietojuma koordināti, kas pēc tam atvieglo pieprasījumu. Tā kā norīkojuma koordinators apstrādā pieprasījumus visiem debitoriem, ir iesaistītas N:N attiecības.

Šajā attēlā redzams puses datu modelis.

![Puses datu modelis.](media/party-gab-image1.png)

> [!TIP]
> Mēģinot izveidot jaunu konta ierakstu, izmantojiet lauku **Puse**, lai meklētu ierakstu pēc nosaukuma. Šādā veidā, ja atrodat ierakstu, tas ir tikai jāatlasa. Tad sistēma automātiski aizpilda visus datus no puses. Nav manuāli jāiestāta visi nepieciešamie lauki. Šo darbību var atrast ārpus saraksta lapas **Konts**, **Kontaktpersona** un **Kreditors**.

Dubultā rakstīšana neatbalsta visas pušu finanšu un operāciju programmu lomas. Pilnu pušu lomu sarakstu skatiet rakstā [Globālās adrešu grāmatas pārskats](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Globālā adrešu grāmata

Globālā adrešu grāmata ir to organizāciju un privātpersonu pasta un elektronisko adrešu katalogs, kas piedalās uzņēmumā.

Globālajā adrešu grāmatā tiek glabāts un apstrādāts tik daudz pasta adrešu un elektronisko adrešu, cik nepieciešams. Piemēram, Fabrikam ir gāzes stacijas 50 vietās. Katrai atrašanās vietai ir atšķirīga pasta adrese, e-pasta adrese un tālruņa numurs. Par visiem biznesa pirkumiem tiek izrakstīts rēķins uz galveno gāzes staciju, bet tie tiek nosūtīti tieši uz konkrēto gāzes staciju, kas pieprasīja pirkumu. Globālajā adrešu grāmatā galvenā gāzes stacija tiek glabāta kā Fabrikam rēķina adrese un glabā katru gāzes staciju kā piegādes adresi. Adreses var saglabāt vienu reizi un pēc tam tās izgūt, kā tas nepieciešams piedāvājumiem un pasūtījumiem.

Atkarībā no biznesa konteksta personai vai organizācijai var būt vairāk nekā viena loma, un visām lomām var izmantot vienādu pasta adresi un elektronisko adresi. Šajā gadījumā adreses maiņai vienā lomā jāparādās visās pārējās lomās. Globālā adrešu grāmata saglabā un apstrādā adreses visā pasaulē.

Sekojošajā attēlā ir parādītas globālās adrešu grāmatas datu modelis.

![Globālās adrešu grāmatas datu modelis.](media/party-gab-image2.png)

## <a name="contact"></a>Saziņa

Customer Engagement programmās kontaktpersona ir persona. Tomēr tabula **Kontaktpersona** ir pārslogota, lai pārstāvētu personu, portāla lietotāju, uzņēmums-patērētājs (B2C) klientu vai kreditoru. Pārstāvība ir netieša, un jūs nevarat noteikt atšķirību, neizmeklējot saistītos darījumus. Tabulai **Kontaktpersona** ir ierobežota attiecība viens pret vienu (1:1) ar tabulu **Konts**. Kā puses un globālās adrešu grāmatas modeļa daļa dubultā rakstīšana ievieš precīzus klasifikācijas rekvizītus un pieļauj N:N attiecības starp kontaktpersonu, kas ir persona un organizācija (**Konts** vai **Kreditors** entītijas).

Ir divu veidu **Kontaktpersonas** rindas:

+ **Svītrota kontaktpersona** — rinda **Kontaktpersona**, kur laukam **Uzņēmums** ir obligāta vērtība.
+ **Nesaskaņota kontaktpersona** — Rinda **Kontaktpersona**, kur lauks **Uzņēmums** ir tukšs.

Tabulā **Kontaktpersona** tabulā var saglabāt šādu veidu rindas.

| Rindas tips | Apraksts |
|----------|-------------|
| Persona, kas ir klients (piemēram, pārdodama kontaktpersona vai B2C klients) | Svītrots kontaktpersonas ieraksts, kurā lauks **Uzņēmums** nav tukšs un lauks **Ir klients** ir iestatīts uz **Jā**. |
| Persona, kas ir kreditors (piemēram, individuālais īpašnieks, tāds kā kreditors) | Svītrots kontaktpersonas ieraksts, kurā lauks **Uzņēmums** nav tukšs un lauks **Ir kreditors** ir iestatīts uz **Jā**. |
| Persona, kas ir gan debitors, gan kreditors | Svītrots kontaktpersonas ieraksts, kurā lauks **Uzņēmums** nav tukšs, lauks **Ir klients** ir iestatīts uz **Jā** un lauks **Ir kreditors** ir iestatīts uz **Jā**. Perosona var būt gan viena produkta ražotājs, gan cita produkta patērētājs. Šīs attiecības atbalsta gan finanšu, gan operāciju programmas, kā arī dubultās rakstīšanas programmas. |
| Persona, kas ir organizācijas kontaktpersona, bet nav klients vai kreditors | Nesvītrots kontaktpersonas ieraksts, kurā lauks **Uzņēmums** ir tukšs, lauks **Ir klients** ir iestatīts uz **Nē** un lauks **Ir kreditors** ir iestatīts uz **Nē**. |

## <a name="contact-for-party-table"></a>Puses kontaktpersonas tabula

Tabula **Puses kontaktpersona** glābā un apstrādā N:N attiecības starp **Konta** rindām un **Kontaktpersonu** rindām. Tas var filtrēt svītrotās **Kontaktpersonu** rindas no nesvītrotām rindām un saistīt tikai nesvītrotās **Kontaktpersonu** rindas ar **Konta** vai **Kreditora** rindām.

Piemēram, Nataša Džonsa un Migels Reiss ir veterinārārsti, kas rūpējas par saimniecībām savās teritorijās. Nataša apkalpo Sietlas rajonu, un Migels apkalpo Kentas rajonu. Customer Engagement lietotnē saimniecības ir pārstāvētas kā klienti un veterinārārsti ir pārstāvēti kā kontaktpersonas. Viens **Kontaktpersonas** ieraksts Natašai ir saistīts ar visām saimniecībām, ar kurām Nataša strādā. Līdzīgi, viens **Kontaktpersonas** ieraksts Migelam ir saistīts ar visām saimniecībām, ar kurām Migels strādā.

Šīs attiecības tiek glabātas tabulā **Puses kontaktpersona**. Informāciju par ārpus saraksta lapām var atrast **Konts**, **Kontaktpersona** un **Kreditors**:

+ Lapā **Konts** varat lietot cilni **Saistītās kontaktpersonas**, lai vienu vai vairākas kontaktpersonas saistītu ar rindu **Konts**. Šādā veidā uzņēmumam tiek piešķirtas kontaktpersonas. Pēc tam varat izvēlēties vienu kontaktpersonu kā konta primāro kontaktpersonu. Ja izmantojat lapu **Ātrā izveide**, varat atlasīt tikai kontaktpersonu. Darbība ir tāda pati, ja izmantojat lapu **Kreditors** un ieraksta tips ir **Organizācija**.
+ Lapā **Kontaktpersona**, kad rinda ir debitors, kreditors vai abi (svītrota kontaktpersona), varat izmantot cilni **Saistītās kontaktpersonas**, lai saistītu vienu vai vairākas kontaktpersonas. Šādā veidā B2C klientam vai kreditoram tiek piešķirtas kontaktpersonas. Pēc tam varat izvēlēties vienu kontaktpersonu kā primāro kontaktpersonu. Ja izmantojat lapu **Ātrā izveide**, varat atlasīt tikai kontaktpersonu.
+ Lapā **Kontaktpersona**, kad rinda ir contaktpersona (nesvītrota kontaktpersona), varat izmantot cilni **Saistītās organizācijas**, lai saistītu vienu vai vairākus debitorus vai kreditorus. Šādā veidā var piešķirt klientus vai kreditorus pamatā esošajai kontaktpersonai. Debitors vai kreditors var būt organizācija, persona vai abi. Vērtību var atlasīt tikai vienā no četriem laukiem:

    + Ja izvēlaties vērtību laukā **Puses ID**, pamatā esošā kontaktpersona tiek piešķirta visām atlasitām puses lomām.
    + Ja izvēlaties vērtību laukā **Saistītā kontaktpersona**, tiek atlasīta svītrotā kontaktpersona, kuras tips ir **Persona**.
    + Ja atlasāt vērtību laukā **Saistītais konts** vai **Saistītais kreditors**, jūs atlasāt organizāciju.

    ![Cilne Saistītās organizācijas lapā Kontaktpersona.](media/party-gab-image3.png)

    Neatkarīgi no jūsu izvēles asociācija tiek izveidota puses līmenī, taa attiecas uz visām puses lomām, un glabājas elementā **Puses kontaktpersona**.

> [!NOTE]
> Customer Engagement programmu tabulas **Puses kontaktpersona** parādāmais nosaukums ir **Debitora/Kreditora kontaktpersona**.

Kad tiek atvērta rinda **Kontaktpersona**, kur gan lauks **Ir debitors**, gan **Ir kreditors** ir iestatīts uz **Nē** tiek parādīta cilne **Saistītās organizācijas**. Izmantojiet šo cilni, lai saistītu vienu vai vairākas debitoru vai kreditoru organizācijas ar kontaktpersonu.

Kad tiek atvērta rinda **Kontaktpersona**, kur vai nu lauks **Ir debitors**, vai nu lauks **Ir kreditors** ir iestatīts uz **Jā** tiek parādīta cilne **Saistītās kontaktpersonas**. Izmantojiet šo cilni, lai saistītu vienu vai vairākas kontaktpersonas.

## <a name="postal-addresses"></a>Pasta adreses

Lapās **Konts**, **Kontaktpersona** un **Kreditors** ir ieviesta jauna cilne **Adreses**. Šī cilne atbalsta vairākas pasta adreses, izmantojot režģi, kā parādīts šajā ilustrācijā.

![Pasta adrešu režģis.](media/party-gab-image4.png)

Režģī ir iekļautas tālāk minētās kolonnas.

+ **Pasta adrešu lomas** - Pasta adrešu nolūki.
+ **Ir primārā** – vērtība, kas norāda, vai adrese ir primārā adrese;
+ **Adreses numurs** – adreses pasūtījums.

Varat izmantot pogu **Jauna adrese** virs režģa, lai izveidotu pēc izvēles tik daudz pasta adrešu, cik vēlaties.

Lauki **1. adrese** un **2. adrese** lapas **Konts** cilnē **Kopsavilkums** atbilst attiecīgi **Piegādes** un **Rēķina** adresēm.

![Kopsavilkuma cilne pasta adresēm.](media/party-gab-image5.png)

Lauki **1. adrese**, **2. adrese** un **3. adrese** lapas **Konts** cilnē **Kopsavilkums** atbilst attiecīgi **Biznesa**, **Piegādes** un **Rēķina** adresēm.

## <a name="electronic-addresses"></a>Elektroniskās adreses

Lapās **Konts**, **Kontaktpersona** un **Kreditors** ir ieviesta jauna cilne **Elektroniskās adreses**. Šī cilne atbalsta vairākas elektroniskās adreses, izmantojot režģi, kā parādīts šajā ilustrācijā.

![Elektronisko adrešu režģis.](media/party-gab-image6.png)

Režģī ir iekļautas tālāk minētās kolonnas.

+ **Veids** – elektroniskās adreses veids.
+ **Ir primārā** vērtība, kas norāda, vai adrese ir primārā adrese;
+ **Mērķis** – elektroniskās adreses nolūks.

Varat izmantot pogu **Jauna elektroniskā adrese** virs režģa, lai izveidotu pēc izvēles tik daudz adrešu, cik vēlaties.

Potenciālā klienta kvalifikācijas procesa laikā varat norādīt gan biznesa tālruņa numuru, gan mobilā tālruņa numuru. Biznesa tālruņa numurs tiek uzskatīts **par primāro tālruņa numuru, ja IsMobile=Nē**, **un mobilā tālruņa numurs tiek uzskatīts par sekundāro tālruņa numuru, ja IsMobile=Jā**.

> [!TIP]
> Lai pārvaldītu pasta un elektroniskās adreses, lietojiet **Konta** un **Kontaktu** veidlapas **Adreses** **Elektroniskās adreses** . Tas nodrošina, ka adrešu dati tiek sinhronizēti ar finanšu un operāciju programmām.

## <a name="setup"></a>Iestatīt

1. Atveriet savu Customer Engagement programmas vidi.

2. Instalējiet visus priekšnosacījumu risinājumus, kā aprakstīts Atsevišķā [duālās rakstīšanas programmas instrumentācijas pakotnē](separated-solutions.md).

3. Instalējiet [Dubultās rakstīšanas puses un globālās adrešu grāmatas risinājumus](https://aka.ms/dual-write-gab).

4. Atveriet Finance and Operations programmu. Pārejiet uz datu pārvaldības moduli un atlasiet cilni Duālais ieraksts. Tiks atvērta duālā ieraksta administrēšanas lapa.

5. Pielietojiet 2. un 3. darbībā instalētos risinājumus, izmantojot funkciju [Pielietot risinājumu](link-your-environment.md).

6. Apturiet tālāk norādītās kartes, jo tās vairs nav obligātas. Tā vietā palaidiet `Contacts V2 (msdyn_contactforparties)` karti.

    + CDS kontaktpersonas V2 un kontaktpersonas (attiecas uz debitoru kontaktpersonām)
    + CDS kontaktpersonas V2 un kontaktpersonas (attiecas uz kreditoru kontaktpersonām)

7. Tālāk minētie elementu kartējumi ir atjaunināti puses funkcionalitātei, tāpēc tiem ir jālieto jaunākā versija.

    Atbilstību karte | Atjaunināt līdz šai versijai | Izmaiņas
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.2 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.6 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Customers V3 (accounts)` | 1.0.0.5 |Noņēma `PartyNumber` un citus ar pusi saistītos laukus, piemēram, vārdu, personas datus, pasta adrešu laukus un elektroniskās kontaktpersonu adreses.
    `Customer V3 (contacts)` | 1.0.0.5 | Noņēma `PartyNumber` un citus ar pusi saistītos laukus, piemēram, vārdu, personas datus, pasta adrešu laukus un elektroniskās kontaktpersonu adreses.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Noņēma `PartyNumber` un citus ar pusi saistītos laukus, piemēram, vārdu, personas datus, pasta adrešu laukus un elektroniskās kontaktpersonu adreses.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Kontaktpersona aizstāta ar `ContactforParty` atsauci.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Kontaktpersona aizstāta ar `ContactforParty` atsauci.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Kontaktpersona aizstāta ar `ContactforParty` atsauci.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.2 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Complimentary Closings (msdyn_compliemntaryclosings)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.
    `CDS Address roles (msdyn_addressroles)` | 1.0.0.0 | Šī ir jauna karte, kas ir pievienota kā daļa no ša laidiena.

8. Pirms iepriekš minēto karšu lietošanas integrācijas atslēgas jāatjaunina manuāli, kā aprakstīts šādās darbībās. Pēc tam atlasiet **Saglabāt**.

    | Atbilstību karte | Atslēgas |
    |-----|------|
    | Konts |  accountnumber [Konta numurs]<br>msdyn_company.cdm_companycode [Uzņēmums (Uzņēmuma kods)] |
    | Kontaktpersona | msdyn_contactpersonid [Konta numurs/Kontaktpersonas ID]<br>msdyn_company.cdm_companycode [Uzņēmums (Uzņēmuma kods)] |
    | Debitora/kreditora kontaktpersona | msdyn_contactforpartynumber [Kontaktpersona puses numuram]<br>msdyn_associatedcompanyid.cdm_companycode [Saistits uzņēmums (Uzņēmuma kods)] |
    | Kreditors | msdyn_vendoraccountnumber [Kreditora konta numurs]<br>msdyn_company.cdm_companycode [Uzņēmums (Uzņēmuma kods)]|

9. Pakalpojumā Dataverse dublikātu noteikšanas kārtulu rakstzīmju ierobežojumi ir pieauguši no 450 līdz 700 rakstzīmēm. Šis ierobežojums ļauj pievienot vienu vai vairākas atslēgas dublikātu noteikšanas kārtulām. Izvērsiet dublikātu noteikšanas kārtulu tabulai **Konts**, iestatot sekojošos laukus.

    | Lauks | Vērtība |
    |-------|-------|
    | Nosaukums/vārds, uzvārds | Konti ar vienādu konta nosaukumu. |
    | Apraksts | Nosaka konta ierakstus, kuriem konta nosaukuma atribūtā ir vienāda vērtība. |
    | Pamatieraksta tips | Konts |
    | Atbilstošais ieraksta tips | Konts |
    | Konta nosaukums (lauks) | Precīza atbilstība |
    | Uzņēmums (lauks) | Precīza atbilstība |
    | Attiecību tips (lauks) | Precīza atbilstība |
    | Puses ID (lauks) | Precīza atbilstība |
    | Atlasiet (lauku) | (tukšs) |

    ![Dublēt kontu kārtulu.](media/duplicate-rule-1.PNG)

10. Izvērsiet dublikātu noteikšanas kārtulu tabulai **Kontaktpersonas**, iestatot sekojošos laukus.

    | Lauks | Vērtība |
    |-------|-------|
    | Nosaukums/vārds, uzvārds | Kontaktpersonas ar tādu pašu vārdu un uzvārdu. |
    | Apraksts | Nosaka kontaktpersonu ierakstus, kuriem laukos Vārds un Uzvārds ir tādas pašas vērtības. |
    | Pamatieraksta tips | Kontaktpersona |
    | Atbilstošais ieraksta tips | Kontaktpersona |
    | Vārds (lauks) | Precīza atbilstība |
    | Uzvārds (lauks) | Precīza atbilstība |
    | Uzņēmums (lauks) | Precīza atbilstība |
    | Puses ID (lauks) | Precīza atbilstība |
    | Atlasiet (lauku) | (tukšs) |

    ![Dublēt kontaktpersonu kārtulu.](media/duplicate-rule-2.PNG)

11. Ja jūs esat esošs duālās rakstīšanas lietotājs, izpildiet norādes sadaļā [Jaunināšana uz pušu un globālo adrešu grāmatas modeli](upgrade-party-gab.md) un jauniniet savus datus. **Ne turpiniet ar 12. soli, neizpabeidzot šo darbību.** Ja esat jauns duālās rakstīšanas lietotājs, turpiniet ar 12. soli.

12. Ja jūs esat esošs duālās rakstīšanas lietotājs, izpildiet 11. soli un pēc tam varēsiet palaist kartes šādā secībā. Ja esat jauns dubultās rakstīšanas debitors, jūs varat turpināt tieši. Ja tiek parādīts kļūdas ziņojums, kas norāda, ka projekta apstiprināšana neizdevās. Trūkst mērķa lauka...", atveriet karti un atlasiet Atsvaidzināt **tabulas** un pēc tam palaidiet karti.

    Finanšu un operāciju programma | Customer engagement programma  
    ----------------------------|------------------------
    [CDS puses](mapping-reference.md#220) | msdyn_parties
    [CDS pasta adreses vietas](mapping-reference.md#234) | msdyn_postaladdresscollections
    [CDS pasta adreses vēsture V2](mapping-reference.md#235) | msdyn_postaladdresses
    [CDS puses pasta adreses vietas](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Puses kontaktpersonas V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Debitori V3](mapping-reference.md#101) | konti
    [Debitori V3](mapping-reference.md#116) | kontaktpersonas
    [Kreditori V2](mapping-reference.md#202) | msdyn_vendors
    [Kontaktpersonu amati](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Noslēguma frāzes](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Uzrunas](mapping-reference.md#228) | msdyn_salutations
    [Lēmumu pieņemšanas lomas](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Nodarbinātības darbu funkcijas](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Lojalitātes programmu līmeņi](mapping-reference.md#226) | msdyn_loyaltylevels
    [Personas rakstura veidi](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Kontaktpersonas V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS pārdošanas piedāvājuma virsraksts](mapping-reference.md#215) | piedāvājumi
    [CDS pārdošanas pasūtījumu virsraksti](mapping-reference.md#217) | salesorders
    [Pārdošanas rēķinu galvenes V2](mapping-reference.md#118) | rēķini
    [CDS adrešu lomas](mapping-reference.md#301) | msdyn_addressroles

> [!NOTE]
> Karte `CDS Contacts V2 (contacts)` ir karte, kas tika apturēta 1. darbībā. Mēģinot palaist citas kartes, šīs 2 kartes var parādīties pakārtoto sarakstā. Neizmantojiet šīs kartes.
>
> Ja ir instalēts puses un globālās adrešu grāmatas risinājums, disable the party and global address book solution `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead`. Atinstalējot pusi un globālo adrešu grāmatas risinājumu, spraudnis ir jāiespējo no jauna.
>
> Lauku `msdyn_*partynumber` (vienas rindas teksta lauku), kas iekļauts tabulās **Konts**, **Kontaktpersona** un **Kreditors** nedrīkst izmantot turpmāk. Iezīmes nosaukumam ir prefikss **(Novecojis)** skaidrības labad. Tā vietā izmantojiet **msdyn_partyid** lauku. Lauks ir pārlūks **msdyn_party** tabulai.
>
> Tabulas nosaukums | Vecais lauks | Jauns lauks
> --------|-------|--------
> Konts | `msdyn_partynumber` | `msdyn_partyid`
> Kontaktpersona | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Veidnes

Tabulas karšu vākšana darbojas kopā puses un globālās adrešu grāmatas mijiedarbībai, kā redzams nākamajā tabulā.

| Finanšu un operāciju programma | Customer engagement programma | Apraksts |
|----------------------------|-------------------------|-------------|
| [Kontaktpersonu amati](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Debitori V3](mapping-reference.md#101) | konti |
| [Debitori V3](mapping-reference.md#116) | kontaktpersonas |
| [CDS puses](mapping-reference.md#220) | msdyn\_parties |
| [CDS puses pasta adreses vietas](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [CDS pasta adreses vēsture V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [CDS pasta adreses vietas](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS pārdošanas piedāvājuma virsraksts](mapping-reference.md#215) | piedāvājumi |
| [CDS pārdošanas pasūtījumu virsraksti](mapping-reference.md#217) | salesorders |
| [Noslēguma frāzes](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Kontaktpersonas V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Lēmumu pieņemšanas lomas](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Nodarbinātības darbu funkcijas](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Lojalitātes programmu līmeņi](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Puses kontaktpersonas V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Personas rakstura veidi](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Pārdošanas rēķinu galvenes V2](mapping-reference.md#118) | rēķini |
| [Uzrunas](mapping-reference.md#228) | msdyn\_salutations |
| [Kreditori V2](mapping-reference.md#202) | msdyn\_vendors |
| [CDS adrešu lomas](mapping-reference.md#301) |msdaddressroles\_|

Papildinformāciju skatiet sadaļā [Dubultā ieraksta kartēšanas atsauce](mapping-reference.md).

## <a name="address-roles-as-a-multi-select-drop-down-list"></a>Adrešu lomas kā nolaižamais saraksts ar vairākiem sarakstiem
Pasta adrese vai elektroniskā adrese var kalpot vairākiem nolūkiem. Piemēram, pasta adrese var kalpot kā rēķina adrese un piegādes adrese. Šādos gadījumos lietotājs nolaižamajā sarakstā var **atlasīt** **rēķinu** un piegādi, kā parādīts šajā ilustrācijā. 

![Nolaižamajā sarakstā nolūks/loma.](media/purpose.png)

## <a name="known-issues-and-limitations"></a>Zināmās problēmas un ierobežojumi

+ Finanšu un operāciju programmās, kad izveidojat debitoru kopā ar adresi un to saglabājat, adrese var nesinhronizēt uz **adrešu** tabulu. Tas ir tāpēc, ka pastāv dubultrakstīšanas platformu secības problēma. Vispirms izveidojiet debitoru un saglabājiet to. Pēc tam pievienojiet adresi.
+ Finanšu un operāciju programmās, kad debitora ierakstam ir primārā adrese un jūs šim debitoram izveidojat jaunu kontaktpersonu, tad kontaktpersonas ieraksts pārmanto primāro adresi no saistītā debitora ieraksta. Tas notiek arī attiecībā uz kreditora kontaktpersonu. Dataverse neatbalsta šo uzvedību. Ja ir aktivizēta duālā rakstīšana, debitoru kontaktpersonas, kas pārmantotas ar primāro adresi no finanšu un operāciju programmas Dataverse, tiek sinhronizētas kopā ar tās adresi.
+ Finanšu un operāciju programmās varat izveidot kontaktpersonas ierakstu no formas **Pievienot** kontaktpersonu. Ja mēģināt izveidot jaunu kontaktpersonu no veidlapas **Skatīt kontaktpersonu**, darbība neizdodas. Šī ir zināma problēma.

    ![Zināmā problēma ar Pievienot kontaktpersonu.](media/party-gab-contact-issue.png)

+ **Sākotnējā sinhronizācija** neatbalsta laika laukus **Pieejams no** un **Pieejams līdz** cilnē **ContactForParty**, jo DIXF pārvērš vērtību virknē vesela skaitļa vietā. Pārvēršana izraisa kļūdu `Cannot convert the literal '<say 08:00:00>' to the expected type edm.int32`.
+ Nevar ievadīt uz priekšu datētu pasta adresi, izmantojot finanšu un operāciju programmu ar dubulto rakstiet, jo Dataverse tā neatbalsta spēkā stāšanās datumu. Ja ievadāt nākotnes datētu pasta adresi, izmantojot finanšu un operāciju programmu, Dataverse tā pilnībā tiek sinhronizēta un adrese tiks skatīta lietotāja interfeisā nekavējoties. Jebkura šī ieraksta atjaunināšanas rezultātā rodas kļūda, jo tā ir nākotnes datēta un nav pašlaik finanšu un operāciju programmā.
