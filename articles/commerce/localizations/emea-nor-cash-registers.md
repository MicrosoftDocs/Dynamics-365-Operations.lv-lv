---
title: Kases sistēmas funkcionalitāte Norvēģijai
description: Šajā tēmā sniegts pārskats par kases sistēmas funkcionalitāti, kas pieejama Norvēģijai, un Microsoft Dynamics 365 Commerce sniedz vadlīnijas par funkcionalitātes iestatīšanu.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: bb87b3a7405ef3d8435748813fa66db74b8f0971
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944944"
---
# <a name="cash-register-functionality-for-norway"></a>Kases sistēmas funkcionalitāte Norvēģijai

[!include[banner](../includes/banner.md)]

Šajā tēmā sniegts pārskats par kases sistēmas funkcionalitāti, kas pieejama Norvēģijai Dynamics 365 Commerce. Tajā sniegti arī norādījumi par funkcionalitātes iestatīšanu. Funkcionalitāte sastāv no šādām daļām:

- Parastās pārdošanas punkta (POS) funkcijas, kas pieejamas debitoriem visās valstīs vai reģionos. Piemēri ietver opciju, kas ļauj izvairīties no vairākas kvīts kopijas drukāšanas.
- Norvēģijai raksturīgās funkcijas, piemēram, ciparparaksti pārdošanas darījumiem.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Norvēģijas kases sistēmas funkcionalitātes pārskats

### <a name="common-pos-features"></a>Parastās POS funkcijas

Lai uzzinātu par POS līdzekļiem, kas ir pieejami klientiem visās valstīs vai reģionos, skatiet [palīdzības resursus Dynamics 365 Retail](../index.md).

Turpmāk minētās POS lokalizācijas funkcijas, kas iepriekš tika ieviestas un padarītas pieejamas debitoriem visās valstīs vai reģionos, tagad var tikt izmantotas īpaši Norvēģijai:

- **Drukājiet teksta laukus kvītī lielā fontu izmērā.** Varat izmantot fonta lieluma parametru kvīts formāta veidotājā, lai norādītu, ka kvīts formāta laukam jāizmanto **liels** fonta lielums. (Liels fonta lielums aptuveni dubulto parasto fontu lielumu.) Piemēram, šo parametru var izmantot, lai drukātu indikatora "Kopēt" kopiju lielās rakstzīmēs.
- **Reģistrējiet kvīšu kopiju drukāšanu POS audita notikumu žurnālā.** Varat izmantot AUDITa parametru POS funkcionalitātes profilā, lai iespējotu drukājamu kvīšu kopijas un citus **POS** audita notikumus, kas jāreģistrē. Audita notikumi ir reģistrēti kanāla datu bāzē un programmā Headquarters. Audita notikumus var skatīt **audita notikumu** lapā.
- **Neļaut kvīts kopijas izdruku vairāk nekā vienu reizi.** Kad POS funkcionalitātes profila audita parametrs ir iespējots, atļaut kvīts kopiju POS atļaujas drukāšanu kontrolē, vai var **izdrukāt** **kvīšu** kopijas. Pastāv arī opcija, kas ļauj izvairīties no vairākas kvīts kopijas drukāšanas.

Turklāt tālāk redzamais POS līdzeklis tika ieviests Norvēģijai, taču tika padarīts pieejams debitoriem visās valstīs vai reģionos:

- **Reģistrējiet papildu notikumus POS audita notikumu žurnālā.** Ja **POS** funkcionalitātes profilā ir iespējots audita parametrs, POS audita notikumu žurnālā ir reģistrēti šādi notikumi:

    - Cenu pārbaudes
    - Nodokļu ignorēšana
    - Labojumi rindu daudzumos
    - Notiek transakciju dzēšana no kanāla datu bāzes

### <a name="norway-specific-pos-features"></a>Norvēģijai raksturīgi POS līdzekļi

Ja POS funkcionalitātes profila ISO koda parametrs ir iestatīts uz Nē, tiek iespējoti šādi Norvēģijai raksturīgi **POS** **līdzekļi**.

#### <a name="digital-signing-of-sales-transactions"></a>Pārdošanas darbību ciparparaksts

Katrai pārdošanas darbībai ir pievienots ciparparaksts. Paraksts tiek izveidots un ierakstīts POS darbību žurnālā vienlaicīgi ar darbības pabeigtību. Paraksts ir pieejams arī žurnālā, kas tiek eksportēts audita nolūkos.

Ir parakstītas tikai pārdošanas darbības skaidrā naudā. Šeit sniegti daži piemēri darbībām, kas ir izslēgtas no parakstīšanas procesa:

- Priekšapmaksas (debitora konta depozīts)
- Pārdošanas pasūtījumu priekšapmaksas (debitora pasūtījuma depozīts)
- Dāvanu kartes izsniegšana
- Darbības, kas nav pārdošanas darbības (mainīgā ievade, norēķinu noņemšana u.c.)

Parakstītie dati ir teksta virkne, kas sastāv no šādiem datu laukiem. Datu lauki ir atdalīti ar semikoliem.

1. Iepriekšējais paraksts tam pašam POS (pirmajai \[**darbībai tiek izmantota nulle 0.)**\]
2. Darījuma datums
3. Darbības laiks
4. Secīgs parakstīts darbības numurs
5. Darbības summa ar nodokļiem
6. Darbības summa bez PVN

Ciparparaksta parakstīšanas procesā tiek izmantota RSA 1024 bitu atslēga, kam ir jaukšanas SHA-1 (RSA-SHA1-1024). Parakstīšanai tiek izmantots Commerce Scale Unit instalētais sertifikāts. Sertifikāta (pēdu nospiedums) unikālais identifikators tiek ierakstīts kopā ar parakstu.

Paraksts tiek saglabāts veikala datu bāzē un galvenajā birojā (HQ) datu bāzē kopā ar darbību datiem. Varat skatīt darbību parakstu un veikala darbību lapas finanšu darbību kopsavilkuma cilnē izmantotos darbību datus, kas tika izmantoti **tā** **ģenerēšanai**.

#### <a name="receipts"></a>Ieejas plūsma

Norvēģijas ieejas plūsmās var būt ietverta papildinformācija, kas tika ieviesta, izmantojot pielāgotos laukus:

- **Kvīts** nosaukums – var pievienot lauku kvīts formāta izkārtojumam, lai identificētu kvīts veidu. Piemēram, pārdošanas kvītī tiks iekļauts teksts "Pārdošanas ieejas plūsma".
- **Parakstīts darbības secīgais numurs – secīgais parakstītās darbības numurs var parādīties kvītī, lai saistītu izdrukātu kvīti ar** ciparparakstu datu bāzē.
- **Ieejas plūsmas kopsummas** - pielāgoti lauki ieņēmumu kopsummām izslēdz ne pārdošanas summas no darbību kopsummām. Summas, kas nav pārdošanas summas, ietver šādas operācijas:

    - Priekšapmaksas (debitora konta depozīts)
    - Pārdošanas pasūtījumu priekšapmaksas (debitora pasūtījuma depozīts)
    - Dāvanu kartes izsniegšana
    - Līdzekļu pievienošana dāvanu kartei

#### <a name="x-and-z-reports"></a>X un Z pārskati

X un Z pārskatos iekļautā informācija ir balstīta uz Norvēģu prasībām. Piemēram, kopējā pārdošanas summa skaidrā naudā ietver tikai summas pārdošanas darbībām skaidrā naudā **un** izslēdziet dāvanu karšu operācijas un priekšapmaksas. Kopējās pārdošanas skaidrā naudā tiek uzskaitītas arī pa krājumu grupām un maksāšanas metodēm. Turklāt tiek uzturēta **un** izdrukāta kopējā kopsummas pārdošanas un kopējās **atgriešanas** summas.

#### <a name="saf-t-cash-register-audit-file"></a>PĀRLŪKA-T kases reģistra audita fails

IR iespējams eksportēt POS darbību žurnālu iepriekš definētajā standarta audita faila - nodokļa (EXE-T) kases reģistra formātā. Audita fails ietver informāciju par organizāciju, būtiskiem pamatdatiem (piemēram, krājumu grupām, krājumiem un nodokļa kodiem), pārdošanas darbību datiem skaidrā naudā ar šo darbību parakstiem, datiem par notikumiem, kas nav pārdošanas notikumi, kā arī beigu datuma pārskata datus.

Audita failu var eksportēt šādos scenārijos:

- Katram veikalam
- Visi veikali
- Vienam terminālim
- Visi termināļi

Varat arī nosūtīt pārskatu no vienas juridiskās personas citas juridiskas personas vārdā. Šajā gadījumā jums ir jāpalaiž eksports no juridiskās personas, kas darbojas, un jānorāda atskaišu juridiskā persona kā pārskata sūtītājs.

DATU BĀZES-T kases sistēmas formāts ir ieviests galvenajā birojā, izmantojot [elektroniskos](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) pārskatus. 

## <a name="setting-up-commerce-for-norway"></a>Commerce for Norway iestatīšana

Šajā sadaļā aprakstīti iestatījumi, kas ir specifiski un ieteicami Norvēģijai. Papildinformāciju skatiet [sadaļā Palīdzības resursi Dynamics 365 Retail](../index.md).

Lai lietotu Norvēģijai raksturīgo funkcionalitāti, pabeidziet šos uzdevumus:

- Iestatiet lauku **Valsts/reģions** uz **NOR** (Norvēģija) juridiskas personas primārajā adresē.
- Iestatiet **ISO koda lauku NO (Norvēģija) katra norvēģijas veikala** POS **funkcionalitātes** profilā.

Norvēģijai ir jānorāda arī šādi iestatījumi.

### <a name="set-up-the-legal-entity"></a>Iestatīt juridisko personu

Pārliecinieties, vai ir norādīts juridiskās personas nosaukums. Šis nosaukums tiks drukāts X un Z pārskatos.

Turklāt kopsavilkuma cilnē **Bankas konta** informācija laukā **Maršrutēšanas** numurs norādiet organizācijas numuru.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Pvn (PVN) iestatīšana norvēģu prasībām


Veidojiet PVN kodus, PVN grupas un krājumu PVN grupas. Ir jāiestata arī PVN informācija par produktiem un pakalpojumiem. Papildinformāciju par TO, kā iestatīt un izmantot PVN, skatiet [PVN](../../finance/general-ledger/indirect-taxes-overview.md) pārskatā.

Ir arī jānorāda PVN grupas un jāiespējo opcija Cenās ir **iekļauta PVN opcija** veikaliem, kas atrodas Norvēģijā.

### <a name="set-up-functionality-profiles"></a>Funkcionalitātes profilu iestatīšana

Ir jāiespējo auditēšana un jāiestata kvīšu numerācija.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Atjaunināt veikala darbinieku POS atļauju grupas un individuālos atļauju iestatījumus

Piešķiriet **tiesības Atļaut drukāt** kvīts kopiju uz atbilstošu vērtību:

- **Atļaut vienmēr** – operators var drukāt kvīts kopiju vairākas reizes.
- **Atļaut tikai** vienu reizi – operators var drukāt kvīts kopiju tikai vienu reizi.
- **Atļaut tikai vienu reizi un tikai tad, ja ir pieejams HQ DB – operators var drukāt kvīts kopiju tikai vienu reizi un tikai tad, ja HQ datu bāze ir pieejama,** izmantojot: Real-time Service, tādējādi sistēma var pārbaudīt, vai kvīts kopijas iepriekš nav izdrukātas jebkurā Commerce Data Exchange veikalā.
- **Nekad** – operators nevar drukāt kvīts kopiju.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotos laukus, lai tos varētu izmantot pārdošanas ieejas plūsmu saņemšanas formātiem

Lapā **Valodas teksts** pievienojiet šādus ierakstus kvīts izkārtojumiem pielāgoto lauku etiķetēm. **Ievērojiet, ka tabulā** **parādītās valodas ID, teksta ID un teksta vērtības ir tikai** **piemēri**. Jūs varat mainīt tos tā, lai tie atbilstu jūsu prasībām.

| Valodas kods | Teksts                   | Teksta ID |
|-------------|------------------------|---------|
| en-ASV       | Kvīts nosaukums          | 900011  |
| en-ASV       | Ir dāvanu karte           | 900012  |
| en-ASV       | Kopā (pārdošana)          | 900013  |
| en-ASV       | Nodoklis kopā (PVN)      | 900014  |
| en-ASV       | Kopsumma ar nodokli (pārdošana) | 900015  |
| en-ASV       | Nodokļa summa (pārdošana)     | 900016  |
| en-ASV       | Skaidras naudas darījuma ID    | 900017  |

Pielāgoto **lauku lapā pievienojiet šiem ierakstiem kvīts izkārtojumu** pielāgotajiem laukiem. **Ievērojiet, ka** uzraksta teksta ID vērtībām ir jāatbilst teksta **ID** vērtībām, kas norādītas **teksta lapā** Valoda.

| Nosaukums                            | Veids    | Uzraksta teksta ID |
|---------------------------------|---------|-----------------|
| Kvīts datums                    | Saņemšana | 900011          |
| IsGiftCard                      | Saņemšana | 900012          |
| SalesTotalExt (pārdošanas pasūtījums)                   | Saņemšana | 900013          |
| TaxTotalExt                     | Saņemšana | 900014          |
| TotalWithTaxExt                 | Saņemšana | 900015          |
| AmountPerTaxExt summa                 | Saņemšana | 900016          |
| Kods CashTransactionSequentialNumber | Saņemšana | 900017          |

> [!NOTE]
> Ir svarīgi norādīt pareizus pielāgotos lauku nosaukumus, kā norādīts augstāk esošajā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs ieejas plūsmās trūkstošo datu.

### <a name="configure-receipt-formats"></a>Konfigurēt ieejas plūsmas formātus

Visiem nepieciešamajiem kvīšu formātiem mainiet lauka Drukāt vērtību uz Vienmēr **drukāt** **kvīts** formātam.

Pievienojiet atbilstošajām saņemšanas sadaļām šādus pielāgotos laukus kvīts formāta veidotājā. Ievērojiet, ka lauku nosaukumi atbilst valodas tekstiem, kas definēti iepriekšējā sadaļā.

1. Galvenes:

    - **Kvīts** nosaukums – šis lauks identificē kvīts tipu.
    - **Kases darbības ID** – šajā laukā tiek drukāts secīgais kases darbības numurs.

2. Rindas:

    - **ir dāvanu karte** — šajā laukā saņemšanas rinda tiek ievietota kā saistīta ar dāvanu kartes izdošanu vai pievienošanas dāvanu kartes operācijai.

3. Kājenes:

    - **Kopsumma (pārdošana)** — šajā laukā tiek drukāta kvīts kopējā skaidras naudas pārdošanas summa. Summa neietver nodokli. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.
    - **Nodokļu kopsumma (pārdošana)** – šis lauks drukā ieņēmumu kopējo nodokļu summu par pārdošanu skaidrā naudā. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.
    - **Kopsumma ar nodokli (pārdošana)** – šajā laukā tiek drukāta kvīts kopējā skaidras naudas pārdošanas summa. Summa ietver nodokļus. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.
    - **Nodokļa summa (pārdošana)** – šajā laukā tiek drukāta kvīts nodokļu summa par katru PVN kodu. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, [skatiet sadaļā Kvīšu formātu iestatīšana un](../receipt-templates-printing.md) noformēšana.

### <a name="configure-the-saf-t-cash-register-export-format"></a>Konfigurējiet HTML-T kases sistēmas eksporta formātu

KONFIGURĀCIJA CL-T cash Register ir pieejama lejupielādei no Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet elektronisko [pārskatu konfigurāciju](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md) importēšana. Jums jālejupielādē šādas konfigurācijas:

- **Mazumtirdzniecības kanāla data.version.1** – datu modeļa konfigurācija.
- **DMM Retail kanāla data.version.1.14** — datu modeļa kartēšanas konfigurācija.
- **NAV IERAKSTU KONTA T Kases reģistra.versija.1.20** – formāta konfigurācija.

Pēc konfigurāciju importēšanas commerce parametru lapas cilnē Elektroniskie dokumenti, laukā **·** **·** **PIETEIKUMU-T kases sistēmas eksporta formāts atlasiet importētās formāta konfigurācijas** nosaukumu.

Nepieciešamajiem pamatdatiem jābūt kartētiem arī uz iepriekš definētiemIET-T standarta kodiem. Lai iegūtu vairāk informācijas, skatiet SAŅEMŠANAS-T kases sistēmas dokumentāciju, ko nodrošina Norvēģijas nodokļu pārvalde. Lai izveidotu kartēšanu, šajās lapās ir **jāiestata jauns lauks HTML-T** kases sistēmas kods:

- Krājumu grupas
- Maksājuma metodes
- PVN kodi

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

Lai iespējotu Norvēģijai raksturīgo funkcionalitāti, ir jākonfigurē kanāla komponenti. Plašāku informāciju skatiet izvietošanas [vadlīnijās](emea-nor-fi-deployment.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
