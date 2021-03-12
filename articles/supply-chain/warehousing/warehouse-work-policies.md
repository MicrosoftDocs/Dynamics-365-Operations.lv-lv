---
title: Darba politikas
description: Šajā tēmā ir izskaidrots, kā iestatīt darba politiku.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 530abffb4c80a2d2f0e58e0c5a34294f7cba0b1a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998457"
---
# <a name="work-policies"></a>Darba politikas

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt sistēmu un noliktavu programmu, lai tās atbalstītu darba politikas. Varat izmantot šo funkcionalitāti, lai ātri reģistrētu krājumus, neveidojot izvietošanas darbu, kad saņemat pirkšanas vai pārsūtīšanas pasūtījumus vai kad aizpildāt ražošanas procesus. Šajā tēmā ir sniegta vispārīga informācija. Lai iegūtu detalizētu informāciju, kas saistīta ar numura zīmes saņemšanu, skatiet [Numura zīmes saņemšana ar noliktavas programmas starpniecību](warehousing-mobile-device-app-license-plate-receiving.md).

Darba politika kontrolē, vai noliktavas darbs tiek izveidots, kad saražotais krājums ir fiziski pabeigts vai kad preces tiek saņemtas, izmantojot noliktavas programmu. Katra darba politika tiek iestatīta, definējot nosacījumus, uz kuriem tas attiecas: darba pasūtījuma tipi un procesi, krājumu novietojums un (pēc izvēles) preces. Piemēram, pirkšanas pasūtījums precei *A0001* ir jāsaņem atrašanās vietā *RECV* noliktavā *24*. Vēlāk prece tiek patērēta citā procesā atrašanās vietā *RECV*. Šādā gadījumā varat iestatīt darba politiku, lai novērstu izvietošanas darba neveidošanu, kad darbinieks ziņo preci *A0001*, kā saņemtu atrašanās vietā *RECV*.

> [!NOTE]
> - Lai darba politika būtu aktīva, ir jādefinē vismaz viena atrašanās vieta, kas atrodas kopsavilkuma cilnē **Krājumu atrašanās vietas** **Darba politikas** lapā. 
> - Vairākām darba politikām nevar norādīt vienu un to pašu atrašanās vietu.
> - Mobilās ierīces izvēlnes elementu opcija **Drukāt etiķeti** nedrukās noliktavas vienības etiķeti, ja vien darbs nav izveidots.

## <a name="activate-the-features-in-your-system"></a>Aktivizēt sistēmas līdzekļus

Lai veiktu visu šajā tēmā aprakstīto funkcionalitāti, kas ir pieejama jūsu sistēmā, ieslēdziet šādus divus līdzekļus [Līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Numura zīmes saņemšanas uzlabojumi
- Darba politikas uzlabojumi ienākošajam darbam

## <a name="the-work-policies-page"></a>Darba politikas lapa

Lai iestatītu darba politikas, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbs \> Darba politikas**. Pēc tam katrā kopsavilkuma cilnē iestatiet laukus, kā aprakstīts sekojošās apakšsadaļās.

### <a name="the-work-order-types-fasttab"></a>Darba pasūtījumu tipu kopsavilkuma cilne

**Darba pasūtījuma tipu** kopsavilkuma cilnē pievienojiet visus darba pasūtījumu tipus un saistītos darba procesus, uz kuriem attiecas darba politika. Tālāk norādītie darba pasūtījumu tipi un saistītie darba procesi tiek atbalstīti darba politikām.

| Darba pasūtījuma veids | Darba process |
|---|---|
| Izejmateriālu izdošana| Visi saistītie procesi |
| Līdzproduktu un blakusproduktu izvietošana | Visi saistītie procesi |
| Pabeigto preču izvietošana | Visi saistītie procesi |
| Pārsūtīšanas saņemšanas p/z | Numura zīmes saņemšana (un izvietošana) |
| Pirkšanas pasūtījumi | <ul><li>Numura zīmes saņemšana (un izvietošana)</li><li>Kravas krājuma saņemšana (un izvietošana)</li><li>Pirkšanas pasūtījuma rindas saņemšana (un izvietošana)</li><li>Pirkšanas pasūtījuma krājuma saņemšana (un izvietošana)</li></ul> |

Lai iestatītu darba politiku tā, lai tā attiektos uz vairākiem viena un tā paša darba pasūtījuma tipa darba procesiem, pievienojiet tīklam atsevišķu rindu katram darba procesam.

Katrai režģa rindai iestatiet **Darba izveides metodes** lauku uz vienu no šīm vērtībām:

- **Nekad** – darba politika atlasītajam darba pasūtījuma veidam un saistītajam darba procesam neļaus izveidot noliktavas darbu.
- **Pārkraušana sadales centrā** — darba politika veic pārkraušanu sadales centrā, izmantojot politiku, ko atlasāt laukā **Pārkraušana sadales centrā politikas nosaukums**.

### <a name="the-inventory-locations-fasttab"></a>Krājumu atrašanās vietas kopsavilkuma cilne

Kopsavilkuma cilnē **Krājumu atrašanās vietas** pievienojiet visas vietas, kur jāpiemēro šī darba politika. Ja darba politikai nav piesaistīts neviens novietojums, tad šī darba politika netiks lietota nevienam procesam.

Vairākām darba politikām nevar norādīt vienu un to pašu atrašanās vietu.

Jūs varat izmantot noliktavas atrašanās vietu, kas piešķirta atrašanās vietas profilam, kur opcija **Izmantot noliktavas vienības izsekošanu** ir izslēgta. Šādā gadījumā darbinieki tieši reģistrē rīcībā esošos krājumus.

### <a name="the-products-fasttab"></a>Preču kopsavilkuma cilne

Cilnē **Preces** iestatiet **preces atlases** lauku, lai kontrolētu, kuras preces šai politikai jāpiemēro:

- **Visi** – politika ir jāpiemēro visām precēm.
- **Atlasīts** – politika jāattiecina tikai uz precēm, kas ir uzskaitītas režģī. Izmantojiet rīkjoslu kopsavilkuma cilnē **Preces**, lai pievienotu režģim preces vai noņemtu tās no režģa.

## <a name="default-and-custom-to-locations"></a>Noklusējums un pielāgots "uz" vietām

> [!NOTE]
> Lai padarītu funkcionalitāti, kas aprakstīta šajā sadaļā, pieejamu jūsu sistēmā, jums jāieslēdz funkcijas *Numura zīmes saņemšanas uzlabojumi* un *Darba politikas uzlabojumi ienākošajam darbam* [Funkciju pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Iepriekš sistēma atbalstīja saņemšanu tikai noklusētajā atrašanās vietā, kas definēta katrai noliktavai. Tomēr mobilās ierīces izvēlnes vienumi, kas izmanto šādus darba izveides procesus, tagad sniedz opciju **Izmantot noklusējuma datus**. Šī opcija ļauj piešķirt pielāgotu "uz" atrašanās vietu vienam vai vairākiem izvēlnes elementiem. (Šī opcija jau bija pieejama dažiem citiem izvēlnes elementu veidiem.)

- Numura zīmes saņemšana (un izvietošana)
- Kravas krājuma saņemšana (un izvietošana)
- Pirkšanas pasūtījuma rindas saņemšana (un izvietošana)
- Pirkšanas pasūtījuma krājuma saņemšana (un izvietošana)

Izvēlnes elementa iestatījums **Uz atrašanās vietu** pārspēj noklusējuma saņemšanas vietu noliktavā visiem pasūtījumiem, kas tiek apstrādāti, izmantojot šo izvēlnes vienumu.

Lai iestatītu mobilās ierīces izvēlnes elementu, lai atbalstītu saņemšanu pielāgotā vietā, sekojiet šiem soļiem.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Atlasiet vai izveidojiet izvēlnes elementu, kas izmanto vienu no darba izveides procesiem, kas uzskaitīti iepriekš šajā sadaļā.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Izmantot noklusējuma datus** uz **Jā**.
1. Darbību rūtī atlasiet **Noklusējuma dati**.
1. Lapā **Noklusējuma dati** iestatiet šādas vērtības:

    - **Noklusējuma datu lauks:** iestatiet šo lauku uz *Uz atrašanās vietu*.
    - **Noliktava:** atlasiet mērķa noliktavu, ko izmantot ar šo izvēlnes elementu.
    - **Atrašanās vieta:** šajā laukā ir uzskaitīti visi novietojuma ID, kas ir pieejami atlasītajai noliktavai. Tomēr šī lauka iestatījumam faktiski nav nekāda efekta. Tādēļ to var atstāt tukšu. Tomēr jūs varat izmantot šo sarakstu, lai apstiprinātu ID, kas ir jāievada laukā **Stingri kodētā vērtība**.
    - **Stingri kodētā vērtība:** ievadiet atrašanās vietas ID, kas attiecas uz šo izvēlnes elementu.

> [!TIP]
> Darba politiku var lietot tikai tad, ja visas saņemšanas vietas ir uzskaitītas atbilstošajā darba ierobežojuma iestatījumā. Šī prasība ir piemērojama neatkarīgi no tā, vai izmantojat noklusējuma noliktavas saņemšanas vietu vai pielāgotu "uz" atrašanās vietu.

## <a name="example-scenario-warehouse-receiving"></a>Piemēra scenārijs: noliktavas saņemšana

Visas preces, ko saņem *Pirkšanas pasūtījuma krājuma saņemšanas (un nosūtīšanas)* process, jābūt reģistrētam atrašanās vietā *FL-001*, un tiem jābūt pieejamiem *24.* noliktavā. Tomēr darbu nedrīkst izveidot. Preces, kas tiek saņemtas, izmantojot citus procesus (tas ir, lietojot citas mobilās ierīces izvēlnes vienības), jāreģistrē noklusējuma noliktavas saņemšanas vietā (*RECV*), un darbs ir jāizveido kā parasti. (Šajā scenārijā netiek rādīts noklusējuma saņemšanas iestatījums.)

Šim scenārijam nepieciešami šādi elementi:

- Darba politika *Pirkšanas pasūtījuma krājuma saņemšanas (un nosūtīšana)* procesam novietojumā *FL-001* visiem produktiem
- Mobilās ierīces izvēlnes elements, kam ir noklusētie dati, un kas iestata lauku **Uz atrašanās vietu** uz *FL-001*

### <a name="prerequisites"></a>Priekšnosacījumi

Lai padarītu funkcionalitāti, kas aprakstīta šajā scenārijā, pieejamu jūsu sistēmā, jums jāieslēdz funkcijas *Numura zīmes saņemšanas uzlabojumi* un *Darba politikas uzlabojumi ienākošajam darbam* [Funkciju pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Šajā scenārijā tiek izmantoti standarta demonstrācijas dati. Tādēļ, ja jūs vēlaties strādāt ar to, izmantojot šeit piedāvātās vērtības, ir jāstrādā ar sistēmu, kurā ir instalēti demonstrācijas dati. Turklāt ir jāatlasa **USMF** juridiskā persona.

### <a name="set-up-a-work-policy"></a>Iestatīt darba politiku

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba politikas**.
1. Atlasiet **Jauns**.
1. Laukā **Darba politikas nosaukums** ievadiet *Pirkšanas preces izvietošanas darbs nav veikts*.
1. Atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Darba pasūtījuma tipi** atlasiet **Pievienot**, lai pievienotu rindu režģim, un pēc tam iestatiet šādas vērtības jaunajai rindai:

    - **Darba pasūtījuma tips:** *Pirkšanas pasūtījumi*
    - **Darba process:** *Pirkšanas pasūtījuma krājuma saņemšana (nosūtīšana)*
    - **Darba izveides metode:** *Nekad*
    - **Pārkraušana sadales centrā politikas nosaukums:** atstājiet šo lauku tukšu.

1. Kopsavilkuma cilnē **Krājumu atrašanās vietas** atlasiet **Pievienot**, lai pievienotu rindu režģim, un pēc tam iestatiet šādas vērtības jaunajai rindai:

    - **Noliktava:** *24*
    - **Atrašanās vieta:** *FL-001*

1. Kopsavilkuma cilnē **Preces** iestatiet **Preces atlases** lauku uz *Visi*.
1. Atlasiet **Saglabāt**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Mobilās ierīces izvēlnes vienuma iestatīšana, lai mainītu saņemto atrašanās vietu

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Kreisajā rūtī atlasiet esošo **Pirkšanas saņemšanas** izvēlnes elementu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Izmantot noklusējuma datus** uz *Jā*.
1. Atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Noklusējuma dati**.
1. Lapā **Noklusējuma dati** darbības rūtī atlasiet **Jauns**, lai pievienotu rindu režģim, un pēc tam iestatiet šādas vērtības jaunajai rindai:

    - **Noklusējuma datu lauks:** *Uz atrašanās vietu*
    - **Noliktava:** *24*
    - **Atrašanās vieta:** atstājiet šo lauku tukšu.
    - **Stingri kodētā vērtība:** *FL-001*

1. Atlasiet **Saglabāt**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Saņemt pirkšanas pasūtījumu, neveidojot darbu

Šajā sadaļā ir parādīts, kā saņemt pirkšanas pasūtījuma krājumu, bet neveidojot darbu, vietā, kas atšķiras no noklusējuma saņemšanas vietas, kas iestatīta noliktavai. Šajā piemērā tiek izmantota darba politika un mobilās ierīces krājums, ko izveidojāt iepriekš šajā scenārijā.

#### <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide

1. Dodieties uz **Sagāde un avoti \> Pirkuma pasūtījumi \> Visi pirkuma pasūtījumi**.
1. Atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:

    - **Tirgotāja konts:** *US-101*
    - **Vieta:** *2*
    - **Noliktava:** *24*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu un atvērtu jaunu pirkšanas pasūtījumu.
1. Kopsavilkuma cilnē **Pirkšanas pasūtījuma rindas** iestatiet šādas vērtības tukšai rindai:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *1*

1. Atlasiet **Saglabāt**.
1. Pierakstiet pirkuma pasūtījuma numuru.

#### <a name="receive-a-purchase-order"></a>Pirkšanas pasūtījuma saņemšana

1. Mobilajā ierīcē pierakstieties *24.* noliktavā, izmantojot *24* kā lietotāja ID un *1* kā paroli.
1. Atlasiet **Ienākošais**.
1. Atlasiet **Pirkšanas saņemšana**. Laukam **Atrašanās vieta** jābūt iestatītam uz *FL-001*.
1. Ievadiet pirkšanas pasūtījuma numuru pirkšanas pasūtījumam, ko izveidojāt iepriekšējā procedūrā.
1. Laukā **Krājuma kods** ievadiet *A0001*.
1. Atlasiet **Labi**.
1. Laukā **Daudzums** ievadiet *1*.
1. Atlasiet **Labi**.

Pirkšanas pasūtījums tagad ir saņemts, bet ar to nav saistīts neviens darbs. Rīcībā esošie krājumi ir atjaunināti, un daudzums *1* krājumam *A0001* tagad ir pieejams atrašanās vietā *FL-001*.

## <a name="example-scenario-manufacturing"></a>Piemēra scenārijs: ražošana

Nākamajā piemērā ir divi ražošanas pasūtījumi, *PRD-001* un *PRD-002*. Ražošanas pasūtījumā *PRD-001* ir operācija ar nosaukumu *Montāža*, kur prece *SC1* tiek ziņota kā pabeigta uz novietojumu *001*. Ražošanas pasūtījumā *PRD-002* ir operācija ar nosaukumu *Krāsošana*, un tas patērē preci *SC1* no novietojuma *001*. Ražošanas pasūtījums *PRD-002* patērē arī izejmateriālu *RM1* no novietojuma *001*. Izejmateriāls *RM1* tiek glabāts noliktavas novietojumā *BULK-001* un ar noliktavas darbu izejmateriālu izdošanai tiks izdots uz novietojumu *001*. Izdošanas darbs tiek ģenerēts, kad tiek izlaista ražošana *PRD-002*.

[![Noliktavas darba politikas](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Kad plānojat konfigurēt noliktavas darba politiku šim scenārijam, ir jāņem vērā tālāk norādītā informācija:

- Noliktavas darbs gatavo preču izvietošanai nav nepieciešams, kad preci *SC1* ziņojat kā pabeigtu no ražošanas pasūtījuma *PRD-001* uz novietojumu *001*. Tas ir tādēļ, ka operācija *Krāsošana* ražošanas pasūtījumam *PRD-002* preci *SC1* patērē tajā pašā novietojumā.
- Noliktavas darbs izejmateriālu izdošanai ir nepieciešams, lai izejmateriālu *RM1* no noliktavas novietojumā *BULK-001* pārvietotu uz novietojumu *001*.

Šeit ir sniegts darba politikas piemērs, kuru varat iestatīt, pamatojoties uz šiem apsvērumiem:

- **Darba politikas nosaukums:** *Nav izvietošanas darba*
- **Darba pasūtījumu veidi:** *Pabeigtās preces izvietošana* un *Līdzprodukta un blakusproduktu izvietošana*
- **Noliktavas atrašanās vietas:** Noliktava *51* un atrašanās vieta *001*
- **Preces:** *SC1*

Nākamais piemēra scenārijs nodrošina detalizētas instrukcijas par noliktavas darba politiku iestatīšanu šim scenārijam.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Piemēra scenārijs: ziņot ražošanas pasūtījumu kā pabeigtu uz novietojumu, kas nav atkarīgs no noliktavas vienības

Šajā scenārijā ir parādīts piemērs, kad ražošanas pasūtījums tiek paziņots kā pabeigts vietā, kura netiek kontrolēta ar numura zīmi.

Šajā scenārijā tiek izmantoti standarta demonstrācijas dati. Tādēļ, ja jūs vēlaties strādāt ar to, izmantojot šeit piedāvātās vērtības, ir jāstrādā ar sistēmu, kurā ir instalēti demonstrācijas dati. Turklāt ir jāatlasa **USMF** juridiskā persona.

### <a name="set-up-a-warehouse-work-policy"></a>Iestatīt noliktavas darba politiku

Ne vienmēr noliktavas procesi ietver noliktavas darbu. Definējot darba politiku, jūs varat novērst darba izveidošanu izejmateriālu izdošanai un gatavās produkcijas izvietošanai preču kopai konkrētos novietojumos.

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba politikas**.
1. Atlasiet **Jauns**.
1. Laukā **Darba politikas nosaukums** ievadiet *Izvietošanas darbs nav veikts*.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Darba pasūtījuma tipi** atlasiet **Pievienot**, lai pievienotu rindu režģim, un pēc tam iestatiet šādas vērtības jaunajai rindai:

    - **Darba pasūtījuma veids:** *Pabeigto preču izvietošana*
    - **Darba process:** *Visi saistītie darba procesi*
    - **Darba izveides metode:** *Nekad*
    - **Pārkraušana sadales centrā politikas nosaukums:** atstājiet šo lauku tukšu.

1. Vēlreiz atlasiet **Pievienot**, lai pievienotu otru rindu režģim, un pēc tam iestatiet šādas vērtības jaunajai rindai:

    - **Darba pasūtījuma veids** *Līdzproduktu un blakusproduktu izvietošana*
    - **Darba process:** *Visi saistītie darba procesi*
    - **Darba izveides metode:** *Nekad*
    - **Pārkraušana sadales centrā politikas nosaukums:** atstājiet šo lauku tukšu.

1. Kopsavilkuma cilnē **Krājumu atrašanās vietas** atlasiet **Pievienot**, lai pievienotu rindu režģim, un pēc tam iestatiet šādas vērtības jaunajai rindai:

    - **Noliktava:** *51*
    - **Atrašanās vieta:** *001*

1. Kopsavilkuma cilnē **Preces** iestatiet **Preces atlases** lauku uz *Atlasītie*.
1. Kopsavilkuma cilnē **Preces** atlasiet **Pievienot**, lai režģim pievienotu rindu.
1. Jaunā rindā iestatiet **Krājuma numura** lauku uz *L0101*.
1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="set-up-an-output-location"></a>Iestatīt izvades novietojumu

1. Dodieties uz **Organizācijas administrēšana \> Resursi \> Resursu grupas**.
1. Kreisajā rūtī atlasiet resursu grupu **5102**.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Ražojumu noliktava:** *51*
    - **Ražojuma atrašanās vieta:** *001*

1. Darbību rūtī atlasiet **Saglabāt**.

> [!NOTE]
> Novietojums *001* nav no numura zīmes atkarīgs novietojums. Izvades vietu, kas netiek kontrolēta ar numura zīmi, var iestatīt tikai tad, ja šai atrašanās vietai ir piemērojama darba politika.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Izveidot ražošanas pasūtījumu un norādīt to kā pabeigtu

1. Doties uz **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns ražošanas pasūtījums**.
1. Dialoglodziņā **Ražošanas pasūtījuma izveide** iestatiet **Krājuma numura** lauku uz *L0101*.
1. Atlasiet **Izveidot**, lai izveidotu pasūtījumu un aizvērtu dialoglodziņu.

    Jauns ražošanas pasūtījums tiek pievienots režģim lapā **Visi ražošanas pasūtījumi**.

    Saglabāt jauno, atlasīto ražošanas pasūtījumu.

1. Darbību rūts cilnē **Ražošanas pasūtījums**, grupā **Process** atlasiet **Aplēst**.
1. Dialoglodziņā **Aplēst** izlasiet aplēsi un pēc tam atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Darbību rūts cilnē **Ražošanas pasūtījums**, grupā **Process** atlasiet **Sākt**.
1. Dialoglodziņā **Sākt** cilnē **Vispārīgi** iestatiet **Automātiskās MK patēriņa** lauku uz *Nekad*.
1. Atlasiet **Labi**, lai iestatījumu saglabātu un aizvērtu dialoglodziņu.
1. Darbību rūts cilnē **Ražošanas pasūtījums**, grupā **Process** atlasiet **Ziņot kā pabeigtu**.
1. Dialoglodziņā **Ziņot kā pabeigts**, cilnē **Vispārīgi** iestatiet opciju **Pieņemt kļūdu** uz *Jā*.
1. Atlasiet **Labi**, lai iestatījumu saglabātu un aizvērtu dialoglodziņu.
1. Darbību rūtī cilnē **Noliktavas** grupā **Vispārīgi** atlasiet **Detalizēta informācija par darbu**.

Kad ražošanas pasūtījums tiek norādīts kā pabeigts, netika ģenerēts darbs izvietošanai. Šī uzvedība notiek tāpēc, ka ir definēta darba politika, kas neļauj ģenerēt darbu, kad produkts *L0101* tiek norādīts kā pabeigts novietojumā *001*.

## <a name="more-information"></a>Papildinformācija

Papildinformāciju par mobilās ierīces izvēlnes elementiem skatiet [Mobilo ierīču iestatīšana noliktavas darbam](configure-mobile-devices-warehouse.md).

Lai iegūtu detalizētu informāciju, kas saistīta ar numura zīmes saņemšanu un darba politikām, skatiet [Numura zīmes saņemšana ar noliktavas programmas starpniecību](warehousing-mobile-device-app-license-plate-receiving.md).

Papildinformāciju par saņemšanas noslodzes pārvaldību skatiet [Ienākošo noslodžu noliktavas apstrāde pirkšanas pasūtījumu veikšanai](inbound-load-handling.md).
