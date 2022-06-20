---
title: Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo krājumu segumu
description: Šajā rakstā ir aprakstīts, kā izmantot drošības rezerves žurnālu, lai atjauninātu krājumu drošības rezervju daudzumu, aprēķinot minimālo vajadzību priekšlikumus, pamatojoties uz vēsturiskiem darījumiem.
author: t-benebo
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 385144738b83fcf6873eae5204b4784d6ecd5b80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851774"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo krājumu segumu

[!include [banner](../../includes/banner.md)]

Drošības rezerve norāda krājuma papildu daudzumu, kas tiek glabāts noliktavā, lai samazinātu risku, ka krājums iziet no krājumiem. Drošības rezerve tiek izmantota kā buferis gadījumā, ja tiek ievadīti pārdošanas pasūtījumi, bet piegādātājs nevar atbilst debitora pieprasītajam nosūtīšanas datumam.

Šajā rakstā ir aprakstīts, kā izmantot drošības rezerves žurnālu minimālo vajadzību priekšlikumu jāaprēķina, pamatojoties uz vēsturiskām darbībām, un pēc tam krājumu vajadzību atjaunināt ar priekšlikumiem.

## <a name="overview-of-minimum-coverage-usage"></a>Minimālās vajadzības izmantošanas apskats

Drošības rezerve ir iestatīta katra **krājuma krājumu** vajadzības lapā. Dažādi papildināšanas veidi tiek attēloti ar dažādiem seguma kodiem. (Plašāku informāciju skatiet [Krājumu drošības rezerve](safety-stock-replenishment.md).) Tomēr visi vajadzību kodi izmanto vērtību, kas ir iestatīta **laukā** Minimums lapā **Krājumu vajadzība** katram krājumam. Ir divas galvenās pieejas lauka Minimums **lietošana**:

- **Minimālais daudzums min/maks. nolūkiem** – šai pieejai tiek izmantots minimālais daudzums kopā ar min/maks. loģiku. Tas ir spēkā, ja **vajadzības koda** lauks ir iestatīts uz *Min/Max* atbilstošam krājumam vai vajadzības grupai. Minimālais **daudzums** norāda vidējo dienas lietojumu, kas reizināts ar krājuma izpildes laiku.
- **Minimālais daudzums krājumu plāna nolūkiem** – šī pieeja izmanto minimālo daudzumu, lai attēlotu krājumu plānu kombinācijā ar pieprasījuma apjoma prognozēm. Tas ir spēkā, ja **vajadzības** koda lauks ir iestatīts uz *Periods* *vai* Vajadzība atbilstošam krājumam vai vajadzības grupai. Minimālais **daudzums** ir krājumu plāns, kas atspoguļo vēlamo debitora pakalpojumu līmeni, lai palīdzētu samazināt krājumu izmaksas, daļējo piegādi un piegādes izpildes laikus. Minimālais daudzums atspoguļo prognozes precizitātes procentu likmi dotajam krājumam. Tā neatbilst vajadzīgajai krājuma pozīcijai.

**Minimālo** vērtību var iestatīt trīs veidos:

- Manuāli lapā **Krājumu vajadzība**
- Pēc Datu pārvaldības struktūras (krājumu *vajadzību* datu elementi)
- Drošības krājumu aprēķins, ko veic drošības krājumu žurnāli

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Aprēķināt minimālo vajadzību, pamatojoties uz vēsturisko lietojumu

Drošības rezervju žurnāli tiek izmantoti, lai aprēķinātu piedāvāto minimālo daudzumu, pamatojoties uz krājuma vēsturisko izmantojumu min./maks. nolūkiem vai krājumu plāna nolūkiem. Vēsturiskā izmantošana parāda visas izdošanas darbības norādītajā periodā. Šīs izdošanas darbības ietver pārdošanas pasūtījuma darbības un krājumu pielāgojumus. Aprēķini identificē arī piedāvātā minimālā daudzuma ietekmi uz krājumu vērtību un krājumu vērtības izmaiņas, salīdzinot ar pašreizējiem minimālajiem daudzumiem.

Katra drošības krājumu žurnāla rinda ataino krājumu un tā vajadzības dimensijas. Šīs žurnāla rindas tiek izveidotas un parādītas drošības **rezervju žurnāla rindu** lapā (**Vispārējās plānošanas vispārējās plānošanas \> izpildes \> drošības \> krājumu aprēķins**). Biznesa process drošības rezerves žurnālu izmantošanai, lai aprēķinātu piedāvātos minimālos daudzumus, ir aprakstīts tālāk šajā rakstā.

Plānotājs izmanto drošības rezerves žurnālu, lai aprēķinātu piedāvāto minimālo daudzumu atlasītajiem krājumiem, pamatojoties uz vēsturisko lietojumu atlasītajos periodos. Piedāvāto minimumu var manuāli ignorēt pēc vajadzības, un jūs variet pārskatīt piedāvātā minimuma ietekmi uz krājuma vērtību. Kad žurnāls ir iegrāmatots, automātiski tiek atjaunināti saistītie minimālie krājumu vajadzības daudzumi.

### <a name="create-a-new-safety-stock-journal-name"></a>Izveidot jaunu drošības krājumu žurnāla nosaukumu

Pirms šī tipa žurnāla ģenerēšanas ir jāizveido vismaz viens drošības rezerves žurnāla nosaukums. Parasti var lietot vairākus žurnālu nosaukumus, lai palīdzētu atdalīt drošības rezerves aprēķinus.

1. Dodieties uz **vispārējās plānošanas \> iestatījumiem \> drošības krājumu žurnālu nosaukumiem**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādus laukus:

    - **Nosaukums** – ievadiet īsu žurnāla nosaukumu.
    - **Apraksts** – ievadiet žurnāla aprakstu.
    - **Privāts lietotāju grupai** – lai ierobežotu pašreizējā žurnāla nosaukuma mērķauditoriju, izvēlieties lietotāju grupu.
    - **Dzēst rindas pēc grāmatošanas** — atzīmējiet šo izvēles rūtiņu, lai pēc noklusējuma tīrītu žurnāla rindas, kad tās tiek grāmatotas. Notīriet to, lai saglabātu visas grāmatotās rindas.

    Lauks **Žurnāla tips** ir tikai nolasāms un ir iestatīts drošības *rezervē*.

1. Aizvērt lapu.

### <a name="create-a-safety-stock-journal-and-lines"></a>Drošības krājumu žurnāla un rindu izveide

Šis solis izveido žurnālu un automātiski pievieno tam rindas. Katra rinda identificē krājumu, tā vajadzības dimensijas un vairākus aprēķinātos daudzumus lietošanas vēsturē. Aprēķinātie daudzumi ietver vidējās izejas plūsmas katram krājuma izpildes laikam, vidējās izejas plūsmas mēnesī un mēneša standarta novirzi.

#### <a name="automatically-generate-journal-lines"></a>Automātiski ģenerēt žurnāla rindas

Žurnāla rindas var automātiski ģenerēt tikai tad, ja pašreiz parādītajā žurnālā nav rindu.

Sekojiet šiem soļiem, lai automātiski ģenerētu žurnāla rindas.

1. Dodieties uz **vispārējās plānošanas \> vispārējās plānošanas palaistā \> drošības \> krājuma aprēķinu**.
1. Darbību rūtī atlasiet **Jauns**. Ir izveidots jauns drošības krājumu žurnāls.
1. Kopsavilkuma cilnē **Žurnāla virsraksta informācija** iestatiet šādus laukus:

    - **Nosaukums** — atlasiet drošības rezerves žurnāla nosaukumu, ko pievienot rindai.
    - **Apraksts** – noklusētā vērtība ir atlasītā žurnāla nosaukuma apraksts. Tomēr, ja nepieciešams, vērtību var labot.
    - **Dzēst rindas pēc grāmatošanas** — atzīmējiet šo izvēles rūtiņu, lai tīrītu žurnāla rindas pēc to grāmatošanas. Notīriet to, lai saglabātu visas grāmatotās rindas. Iestatījums tiek pārmantots no atlasītā žurnāla nosaukuma.

    Žurnāla **lauks** ir tikai lasāms un parāda tā žurnāla ID numuru, kuru veidojat un pievienojat rindām.

1. Kopsavilkuma cilnē **Žurnāla** rindas atlasiet **Izveidot rindas** rīkjoslā.
1. Dialoglodziņā Izveidot **žurnāla rindas piedāvātajiem minimālajiem krājumu līmeņiem** iestatiet šādus laukus:

    - **No datuma** – atlasiet perioda sākuma datumu, kam izejas plūsmas jāiekļauj aprēķinā.
    - **Līdz datumam** – atlasiet perioda, kam šajā aprēķinā jāiekļauj izejas plūsmas, beigu datumu. Starp sākuma un beigu datumiem jābūt vismaz diviem mēnešiem.
    - **Aprēķināt standarta novirzi** – iestatiet šo opciju kā Jā *,* lai aprēķinātu standarta novirzi. Šī opcija jāiestata kā Jā *,* lai izmantotu opciju **Izmantot** pakalpojumu līmeni, kad aprēķināt priekšlikumu (kā aprakstīts tālāk šajā rakstā).

1. Kopsavilkuma cilnē **Ieraksti var** iestatīt filtrus un ierobežojumus, lai noteiktu iekļautos krājumus. (Piemēram, var filtrēt pēc **Vajadzības grupas** vērtība.) Atlasiet **Opciju Filtrs**, lai atvērtu standarta vaicājumu redaktora dialoglodziņu, kurā varat definēt atlases kritērijus, kārtošanas kritērijus un savienojumus. Šie lauki darbojas tāpat, kā citi Microsoft vaicājumu veidi Dynamics 365 Supply Chain Management.
1. Kopsavilkuma cilnē **Izpildīt fonā** atlasiet, vai uzdevumu palaist pakešuzdevumu režīmā un/vai iestatīt periodisku grafiku. Lauki darbojas tāpat, kā citi [fona darbu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.
1. Atlasiet **Labi**. Rindas tiek izveidotas dimensijām, kurām ir krājumu darbības.

#### <a name="manually-add-or-remove-journal-lines"></a>Pievienot vai noņemt žurnāla rindas manuāli

Jūs varat manuāli pievienot un/vai noņemt žurnāla rindas jebkurā laikā (vai nu pēc vai tā vietā, lai automātiski ģenerētu rindas). Izmantojiet šādas pogas kopsavilkuma cilnes Žurnāla rindu **rīkjoslā**:

- **Jauna** – pievienot jaunu rindu. Pēc tam ievadiet vērtību katrā kolonnā, lai definētu preci, kuru aprēķināt un piemērot jaunu minimumu. Tā kā piedāvātie minimālie aprēķini nav pieejami manuāli pievienotajām rindām, tām netiek **rādītas** jaunas aprēķinātā minimālā daudzuma vērtības. Tāpēc jums manuāli jāievada Jaunas minimālā **daudzuma** vērtības. Tomēr joprojām var skatīt jaunās minimālā daudzuma vērtības **potenciālo** ietekmi uz krājumu vērtību un potenciālās izmaiņas krājumos, salīdzinot ar pašlaik norādīto minimumu.
- **Dzēst** — dzēsiet atlasīto rindu.
- **Dzēst žurnāla rindas** — dzēsiet visas žurnāla rindas.

### <a name="calculate-a-proposal"></a>Priekšlikuma aprēķināšana

Šajā solī tiek aprēķināts piedāvātais minimums katrai žurnāla rindai un rindas potenciālā ietekme uz krājumu vērtību. (Piedāvātais minimums tiek parādīts kā **Aprēķinātā minimālā** daudzuma vērtība.) Aprēķinu var veikt vairākas reizes, kā nepieciešams. Aprēķins atjaunina aprēķināto **minimālā daudzuma vērtību**, kas tiek rādīta visām žurnāla rindām.

Parādītie aprēķini neietekmēs katras preces faktisko minimālo daudzumu **vērtības**, kamēr darbību rūtī nav atlasīts Grāmatot. Tajā laikā katrai precei **tiks** piemērotas jaunas minimālās daudzuma vērtības.

1. Dodieties uz **vispārējās plānošanas \> vispārējās plānošanas palaistā \> drošības \> krājuma aprēķinu**.
1. Atveriet žurnālu, lai aprēķinātu priekšlikumu. Vai arī izveidojiet jaunu žurnālu tā, kā aprakstīts iepriekš šajā rakstā.
1. Kopsavilkuma cilnē **Žurnāla** rindas atlasiet Aprēķināt **priekšlikumu** rīkjoslā. (Nav jāatlasa neviena rindas.)
1. **Dialoglodziņā Aprēķināt priekšlikumu krājumu minimuma līmenim** iestatiet šādus laukus:

    - **Izmantojiet vidējo izejas plūsma izpildes laikā** - Izvēlieties šo opciju **, lai izveidotu Aprēķinātās minimālā daudzuma** vērtības, pamatojoties uz vidējo izejas plūsmas norādītajā periodā. Pēc tam laukā **Reizināšanas koeficients** ievadiet vērtību, lai pēc vajadzības koriģētu rezultātu. Piemēram, ievadiet *1,0* *, lai izmantotu precīzu aprēķināto vidējo vai 1,1*, lai pievienotu papildu buferi ar 10 procentiem.
    - **Lietojiet pakalpojumu** līmeni – atlasiet šo opciju, lai aprēķinātu piedāvāto minimumu, pamatojoties uz vēlamo pakalpojuma līmeni. Pēc tam **laukā Pakalpojumu** līmenis atlasiet vēlamo pakalpojuma līmeni.
    - **Izpildes laika rezerve** – ievadiet vērtību, lai pagarinātu parasto izpildes laiku par (piemēram, lai atļautu administrēšanu).
    - **Izmantojiet aprēķināto minimālo** daudzumu kā jaunu minimālo daudzumu —*·* **·** **iestatiet** šo opciju uz Jā, lai automātiski kopētu vērtības no kolonnas Aprēķinātais minimālais daudzums uz kolonnu Jaunais minimālais daudzums visām rindām pēc aprēķina pabeigšanas. Iestatot šo opciju kā *Nē*, **pašreizējā minimālā daudzuma** vērtība visām **rindām tiks kopēta** kolonnā Jauns minimālais daudzums. Pēc tam jums būs manuāli jārediģē jaunas **minimālā daudzuma vērtības**, kā nepieciešams.

1. Kopsavilkuma cilnē **Izpildīt fonā** atlasiet, vai uzdevumu palaist pakešuzdevumu režīmā un/vai iestatīt periodisku grafiku. Lauki darbojas tāpat, kā citi [fona darbu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.
1. Atlasiet **Labi**. Aprēķinu rezultāti tiek rādīti kopsavilkuma cilnes **Žurnāla** rindu kolonnā Aprēķinātais **minimālais** daudzums. Pašlaik vērtības ir tikai piedāvātās vērtības, kas vēl nav lietotas jūsu precēm.

### <a name="update-minimum-quantity"></a>Atjaunināt minimālo daudzumu

Drošības krājumu žurnālā var atlasīt jebkuru rindu un manuāli ignorēt lauka Jauns minimālais **daudzums** vērtību.

1. Dodieties uz **vispārējās plānošanas \> vispārējās plānošanas palaistā \> drošības \> krājuma aprēķinu**.
1. Atveriet žurnālu rediģēšanai. Vai arī izveidojiet jaunu žurnālu tā, kā aprakstīts iepriekš.
1. Kopsavilkuma cilnē **Žurnāla rindas** atrodiet koriģējamo rindu un pēc tam rediģējiet vērtību kolonnā **Jauns minimālais** daudzums. Piemēram, varat iestatīt jaunā minimālā daudzuma **vērtību**, lai tā atbilstu aprēķinātajai minimālā **daudzuma vērtībai**. Ja aprēķinātā **minimālā daudzuma** vērtība ir *0* (nulle), varat ievadīt vēlamo nākotnes vērtību.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Grāmatot jauno minimālo daudzumu un validēt rezultātu

Ievērojiet šos soļus, lai grāmatotu jauno minimālo daudzumu un pārbaudītu rezultātu.

1. Dodieties uz **vispārējās plānošanas \> vispārējās plānošanas palaistā \> drošības \> krājuma aprēķinu**.
1. Atveriet žurnālu, lai grāmatotu jaunus minimālos daudzumus. Vai arī izveidojiet jaunu žurnālu tā, kā aprakstīts iepriekš.
1. Darbību rūtī atlasiet **Grāmatot**.
1. Dialoglodziņā Grāmatot **žurnālu iestatiet** lauku Visas grāmatošanas **kļūdas pārsūtīt uz jaunu žurnāla lauku pēc** vajadzības. Pēc tam atlasiet **Labi**, lai grāmatotu žurnālu.
1. Ja jūs mainījuiet **Jaunā** **minimālā** daudzuma vērtību rindai kopsavilkuma cilnē Žurnāla rindas, jūs varat apstiprināt izmaiņu, tas jāveic šādi:

    1. Rediģētai rindai atlasiet saiti krājuma numura **kolonnā**.
    1. Dialoglodziņā Informācija **par preci** atlasiet saiti laukā Krājuma numurs **, lai** atvērtu saistīto izlaisto preces ierakstu.
    1. Darbību rūts cilnē **Plāns** grupā **Vajadzība** atlasiet **Krājumu segums**.
    1. Ievērojiet, **ka** tagad atrašanās vietas un noliktavas minimālā vērtība, ko koriģējusi, izmantojot grāmatoto drošības krājumu žurnālu, ir atjaunināta, lai atbilstu jūsu rediģēšanai.

## <a name="additional-resources"></a>Papildu resursi

- [Krājumu drošības rezerves izpilde](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
