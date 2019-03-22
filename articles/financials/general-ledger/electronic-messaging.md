---
title: Elektr. ziņojumapm.
description: Šajā tēmā ir sniegts apskats par elektronisko ziņojumapmaiņu un tās iestatīšanai nepieciešamo informāciju programmā Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5326642553c7efcebc6c6af953e2dafe9e62e9ec
ms.sourcegitcommit: f6fc90585632918d9357a384b27028f2aebe9b5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/11/2019
ms.locfileid: "832199"
---
# <a name="electronic-messaging"></a>Elektroniskā ziņojumapmaiņa

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts apskats par elektronisko ziņojumapmaiņu un tās iestatīšanai nepieciešamo informāciju programmā Microsoft Dynamics 365 for Finance and Operations.

Nesen valdības un likumdošanas iestādes dažādās valstīs un reģionos visā pasaulē ieviesa pārskatu veidošanas prasības uzņēmumiem, kas reģistrēti attiecīgajās valstīs vai reģionos. Prasību mērķis ir nodrošināt iespēju iegūt datus no minētajiem uzņēmumiem elektroniskā formātā tieši no sistēmām, kurās tika veikta to uzskaite, uzglabāšana un apstrāde.

Elektronisko ziņojumu funkcionalitāte programmā Finance and Operations atbalsta dažādus procesus elektroniskajai sadarbspējai starp Finance and Operations un sistēmām, kuras valdības un likumdošanas iestādes nodrošina oficiālās informācijas ziņošanai, iesniegšanai un saņemšanai.

Elektr. ziņojumu funkcionalitāte ir integrēta modulī **Elektronisko pārskatu veidošana** (ER). Tāpēc varat iestatīt ER formātus elektroniskajiem ziņojumiem. Papildinf. sk. tēmā [Elektr. pārskatu veidošana (ER)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektroniskā ziņojumapm. balstās uz šādiem elementiem:

- **Elektroniskais ziņojums** — pārskats vai deklarācija, par ko ir jāziņo un/vai kas jānosūta iekšēji. Piemērs ir pārskats, ko nosūta nodokļu iestādei.
- **Elektroniskā ziņojuma vienumi** — ieraksti, kas jāiekļauj ziņojumā, par kuru tiek ziņots.
- **Elektroniskā ziņojumu apstrāde** — saistītu vai nesaistītu darbību ķēde, kas ir jāizpilda, lai savāktu nepieciešamos datus, ģenerētu pārskatus, uzglabātu datus Microsoft Azure Blob krātuvē, pārsūtītu pārskatus ārpus sistēmas, saņemtu atbildes no sistēmas ārpuses un atjauninātu datu bāzi, pamatojoties uz saņemto informāciju.

Šajā attēlā ir parādīta elektroniskās ziņojumapmaiņas datu plūsma.

![El. ziņojumapm. datu plūsma](media/electronic-messaging-data-flow.png)

Elektronisko ziņojumu funkcionalitāte atbalsta šādus scenārijus:

- Manuāli izveidojiet ziņojumus un ģenerējiet pārskatus, pamatojoties uz dažādu veidu saistītajiem eksportēšanas ER formātiem: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, teksts un Microsoft Word.
- Automātiski izveidojiet un apstrādājiet ziņojumus, kas balstīti uz inform., kas tika pieprasītas un iegūta no iestādes, izmantojot saistīto import. ER formātu.
- Apkopojiet un apstrādājiet inf. no datu avota (Finance and Operations tabula) kā ziņojumu vienumus.
- Glabājiet papildu inform. un novērtējiet dažādas vērtības, izsaucot īpaši definētas izpildāmās klases saistībā ar ziņojumiem vai ziņojumu krājumiem.
- Apkopojiet inform., kas apkopota ziņojumu vienumos, sadaliet šo inform. atbilstoši ziņoj. un ģenerējiet pārskatus, kas ir saistītajos eksport. ER formātos.
- Pārsūtiet ģenerētos pārskatus uz tīmekļa pakalpojumu, izmantojot drošības informāciju, kas glabājas Azure Key Vault.
- Saņemiet atbildi no tīmekļa pak., interpretējiet atbildi un atjauniniet datus Finance and Operations pēc vajadzības.
- Saglabājiet un pārskatiet visus ģenerētos pārskatus.
- Saglab. un pārsk. žurnāla inf., kas saistīta ar darb., kuras tiek izpildītas ziņojumam vai ziņojuma vienumam.
- Kontrolējiet apstrādi, izmantojot ziņoj. statusus un ziņoj. vienumu statusus.

## <a name="set-up-electronic-messaging"></a>Elektr. ziņojumapm. iestat.

Elektr. ziņojumapm. var jums palīdzēt uzturēt dažādus elektr. pārskatu veidošanas procesus dažādiem dok. tipiem. Dažos sarežģītos scenārijos elektroniskajai ziņojumapmaiņai ir iestatīta daudzu ziņojumu statusu, ziņojumu vienumu statusu, darbību, papildu lauku un izpildāmo klašu kombinācija. Šādu scenāriju gadījumā datu elementu pakotnes ir pieejamas importam. Ja izmantojat šīs datu elementu pakotnes, importējiet tās juridiskajā personā, izmantojot rīku Datu pārvaldība. Plašāku inf. par to, kā izmantot rīku Datu pārvaldība, sk. sadaļā [Datu pārvaldība](../../dev-itpro/data-entities/data-entities-data-packages.md).

Ja neimportējat datu elementu pakotni, varat manuāli iestatīt elektronisko ziņojumu funkcionalitāti. Šajā gadījumā ir jāiestata šādi elementi: 

- [Numuru sērijas](#number-sequences)
- [Ziņoj. vienumu veidi un statusi](#message-item-types-and-statuses)
- [Ziņojuma statusi](#message-statuses)
- [Papildlauki](#additional-fields)
- [Izpildāmās klases darbības](#executable-class-settings)
- [Ierakstu aizpildīšanas darbības](#populate-records-actions)
- [Tīmekļa lietojumprogrammas](#web-applications)
- [Tīmekļa pakalpojuma iestatījumi](#web-service-settings)
- [Ziņojuma apstrādes darbības](#message-processing-actions)
- [Elektroniska ziņojuma apstrāde](#electronic-message-processing)

Nākamajās sadaļās ir sniegta plašāka inform. par katru no šiem elementiem.

### <a name="number-sequences"></a>Numuru sērijas

Iestatiet numuru sērijas gan ziņojumiem, gan ziņ. vienumiem. Numuru sērijas tiek izmantotas, lai automātiski numurētu ziņojumus un ziņojumu vienumus, un piešķirtie numuri tiks izmantoti kā ziņojumu un ziņojumu vienumu unikāli identifikatori sistēmā. Numuru sērijas elektroniskajai ziņojumapmaiņai var iestatīt lapā **Virsgrāmatas parametri** (**Virsgrāmata** \> **Virsgrāmatas iestatīšana** \> **Virsgrāmatas parametri**).

### <a name="message-item-types-and-statuses"></a>Ziņoj. vienumu veidi un statusi

Ziņojumu vienumu veidi norāda ierakstu veidus, kas tiks izmantoti elektron. ziņojumos. Ziņ. vien. veidus var iestatīt lapā **Ziņ. vien. veidi** (**Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ziņojumu vienumu veidi**).

Ziņojumu krājumu statusi norāda statusus, kas attieksies uz ziņojumu vienumiem apstrādē, kuru iestatāt. Ziņ. vien. veidus var iestatīt lapā **Ziņ. vien. statusi** (**Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ziņojumu vienumu statusi**).

Ziņojuma vienuma statusa parametrs **Atļaut dzēšanu** nosaka, vai lietotājam tiks atļauts dzēst ziņojuma vienumu ar šo statusu, izmantojot formu **Elektroniskie ziņojumi**  vai formu **Elektronisko ziņojumu vienumi**. 

### <a name="message-statuses"></a>Ziņojuma statusi

Iestatiet ziņojumu statusus, kam jābūt pieejamiem ziņojumu apstrādē. Ziņojumu statusus var iestatīt lapā **Ziņojumu statusi** (**Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ziņojumu statusi**).

Lauka apraksts:

| Lauka nosaukums           | Apraksts |
|----------------------|-------------|
|Ziņojuma statuss        | Elektroniskā ziņojuma statusa unikālais nosaukums, kas raksturo ziņojuma stāvokli katrā brīdī. Šis nosaukums tiks parādīts formā Elektroniskie ziņojumi un žurnālā, kas saistīts ar elektronisko ziņojumu. |
|Apraksts           | Apraksts, kas attiecas uz elektroniskā ziņojuma statusu      |
|Atbildes tips         | Dažu darbību apstrāde var izraisīt vairāk nekā vienu atbildes tipu. Kā, piemēram, tipa **Tīmekļa pakalpojums** darbība var izraisīt vai nu atbildes tipu **Izpildīts veiksmīgi**, vai **Tehniska kļūda** atkarībā no darbības izpildes rezultāta. Šajā gadījumā jādefinē ziņojuma statuss abiem atbilžu tipiem. Skatiet tēmu [Ziņojumu apstrādes darbību tipi](#message-processing-action-types), lai iegūtu plašāku informāciju par darbību tipiem un ar tiem saistīto atbilžu tipiem. |
|Ziņojuma krājuma statuss   |Ir gadījumi, kad elektroniskā ziņojuma statuss attiecīgi ietekmē saistīto ziņojumu vienumu statusu. Saistiet šādu ziņojumu vienumu statusu šajā laukā, atlasot no meklēšanas. |
|Atļaut dzēšanu          | Elektroniskā ziņojuma statusa parametrs **Atļaut dzēšanu** nosaka, vai lietotājam tiks atļauts dzēst elektronisko ziņojumu ar šo statusu, izmantojot formu **Elektroniskie ziņojumi**.            |

### <a name="additional-fields"></a>Papildlauki

Elektronisko ziņojumu funkcionalitāte ļauj aizpildīt ierakstus no transakciju tabulas. Šādā veidā var sagatavot ierakstus pārskatiem un pēc tam ziņot par tiem. Dažreiz nav pietiekami daudz informācijas transakciju tabulā, lai ziņotu par ierakstu saskaņā ar pārskatu prasībām. Var aizpildīt visu informāciju, kas ir jāziņo par ierakstu, izveidojot papildu laukus. Papildu laukus var saistīt gan ar ziņojumiem, gan ziņojumu vienumiem. Papildu laukus var iestatīt lapā **Papildu lauki** (**Nodoklis** \> **Iestatījumi** \> **Elektroniskie ziņojumi** \> **Papildu lauki**).

Nākamajā tabulā ir aprakstīti galvenie lauki lapā **Papildu lauki**.

| Lauks                | Apraksts |
|----------------------|-------------|
| Lauka nosaukums           | Ievadiet ar procesu saistīto ziņojumu vienumu papildu atribūta nosaukumu. Šis nosaukums tiek parādīts lietotāja interfeisā, strādājot ar procesu. To var izmantot arī ER konfigurācijās, kas ir saistītas ar procesu. |
| apraksts          | Ievadiet ar procesu saistīto ziņojumu vienumu papildu atribūta aprakstu. |
| Lietotāja labojumi            | Ja lietotājam ir nepieciešams mainīt papildu lauka vērtību lietotāja interfeisā, iestatiet šo izvēles rūtiņu ar **Jā**, pretējā gadījumā ar **Nē**. |
| Skaitītājs              | Ja papildu laukam jāsatur sērijas numuru noteiktā elektroniskajā ziņojumā, atzīmējiet šo izvēles rūtiņu. Papildu lauka vērtības tiek aizpildītas automātiski darbības ar tipu “Elektroniskā pārskata veidošanas eksports” palaišanas laikā.  |
| Paslēpts               | Ja papildu laukam lietotāja interfeisā jābūt paslēptam, atzīmējiet šo izvēles rūtiņu.  |

Katra papildu lauka apstrādei var būt dažādas vērtības. Kopsavilkuma cilnē Vērtības varat definēt šādas vertības:

| Lauks                | Apraksts |
|----------------------|-------------|
| Lauka vērtība          | Ievadiet lauka vērtību, ko izmantot saistībā ar ziņojumu vai ziņojuma vienumu pārskata veidošanas laikā. |
| Lauka apraksts    | Ievadiet lauka vērtības aprakstu, ko izmantot saistībā ar ziņojumu vai ziņojuma vienumu pārskata veidošanas laikā. |
| Konta veids         | Dažas papildu lauku vērtības var lietot tikai ar noteiktiem konta tipiem. Atlasiet vienu no šīm vērtībām: **Visi**, **Debitors** vai **Kreditors**. |
| Konta kods         | Ja atlasījāt **Debitors** vai **Kreditors** laukā **Konta tips**, varat vēl vairāk ierobežot lauka vērtību izmantošanu ar noteiktu grupu vai tabulu. |
| Konta/grupas numurs | Ja atlasījāt **Debitors** vai **Kreditors** laukā **Konta tips** un ja ievadījāt grupu vai tabulu laukā **Konta kods**, šajā laukā var ievadīt noteiktu grupu vai kontrahentu. |
| Ir spēkā            | Norādiet datumu, kad vērtība ir jāsāk ņemt vērā. |
| Termiņa beigas           | Norādiet datumu, kad vērtība ir jābeidz ņemt vērā. |

Laukos **Konta/grupas numurs**, **Konta kods**, **Ir spēkā**, **Termiņa beigas** definēto kritēriju kombinācijas pēc noklusējuma neietekmē papildu lauka vērtību atlasi, bet var tikt izmantotas izpildāmā klasē, lai īstenotu kādu noteiktu papildu lauka vērtības aprēķina loģiku.

### <a name="executable-class-settings"></a>Izpildāmās klases darbības

Izpildāmā klase ir X++ metode vai klase, ko elektroniskā ziņojumu apstrāde var izsaukt saistībā ar darbību, ja procesam ir vajadzīga novērtēšana.

Izpildāmo klasi varat iestatīt manuāli lapā **Izpildāmās klases iestatījumi** (**Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Izpild. klases iestat.**). Izveidojiet rindu un iestatiet šādus laukus.

| Lauks                 | apraksts |
|-----------------------|-------------|
| Izpildāmā klase      | Ievadiet nosaukumu, kas tiks izmantots, iestatot ziņojumu apstrādes darbību, saistībā ar kuru tiek izsaukta šī klase. |
| apraksts           | Ievadiet izpildāmās klases aprakstu. |
| Izpildāmās klases nosaukums | Atlasiet X++ izpildāmo klasi. |
| Izpildes līmenis       | Šis lauks tiek iestatīts autom., jo vērtībai jābūt iepriekš definētai atlasītajai izpildāmajai klasei. Šis lauks ierobežo saistītās vērtēšanas palaišanas līmeni. |
| Klases apraksts     | Šis lauks tiek iestatīts autom., jo vērtībai jābūt iepriekš definētai atlasītajai izpildāmajai klasei. |

Dažām izpildāmām klasēm var būt obligātie parametri, kas jānosaka pirms izpildāmā klase tiek palaista pirmo reizi. Lai definētu šādus parametrus, noklikšķiniet uz pogas **Parametri** rūtī Darbības, iestatiet atbilstošās vērtības un dialoga loga laukus un noklikšķiniet uz pogas **Labi**. Ir svarīgi noklikšķināt uz pogas **Labi**, citādi pamatparametri netiks saglabāti un izpildāmā klase netiks pareizi izsaukta.

### <a name="populate-records-actions"></a>Ierakstu aizpildīšanas darbības

Ierakstu aizpild. darbības izmanto, lai iestatītu darb., kas pievieno ierakstus ziņoj. vienumu tabulā, lai tos varētu pievienot elektr. ziņojumam. Piemēram, ja elektroniskajam ziņojumam ir jāziņo par debitora rēķiniem, ir jāiestata darbība **Aizpildīt ierakstus**, kas ir saistīta tabulā **Debitoru rēķinu žurnāls** (laukā **Datu avots**). Ierakstu aizpild. darbības var iestatīt lapā **Ierakstu aizpild. darbība** (**Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ier. aizpild. darb.**). Izveidojiet jaunu ierakstu katrai darbībai, kas pievieno ierakstus tabulā, un iestatiet šādus laukus.

| Lauks       | apraksts                                                               |
|-------------|---------------------------------------------------------------------------|
| Vārds/nosaukums        | Ievadiet nosaukumu darbībai, kas aizpilda ierakstus jūsu procesā.       |
| apraksts | Ievadiet aprakstu darbībai, kas aizpilda ierakstus jūsu procesā. |

Cilnē **Datu avotu iestatīšana** pievienojiet rindu katram datu avotam, kas tiek izmantots procesā, un iestatiet šādus laukus.

| Lauks                  | apraksts |
|------------------------|-------------|
| Vārds/nosaukums                   | Ievadiet datu avota nosaukumu. |
| Ziņojuma krājuma veids      | Atlasiet ziņojumu vienuma tipu, kas jāizmanto, kad tiek izveidoti ieraksti datu avotam. |
| Konta veids           | Atlasiet konta tipu, kas ir jāsaista ar ierakstiem no datu avotu. |
| Galvenās tabulas nosaukums      | Atlasiet programmā Finance and Operations tabulu, kam jābūt datu avotam. |
| Dokumenta numura lauks  | Atlasiet lauku, no kura jāņem dokumenta numurs atlasītajā tabulā. |
| Dokumenta datuma lauks    | Atlasiet lauku, no kura jāņem dokumenta datums atlasītajā tabulā. |
| Dokumenta konta lauks | Atlasiet lauku, no kura jāņem dokumenta konts atlasītajā tabulā. |
| Lietotāja vaicājums             | Ja ir atzīmēta šī izv. rūtiņa, var iestatīt vaicājumu, atlasot **Rediģēt vaicājumu** virs režģa. Pretējā gadījumā visi ieraksti tiks aizpildīti no datu avotu. |

### <a name="web-applications"></a>Tīmekļa lietojumprogrammas

Jūs izmantojat tīmekļa programmu lapu, lai iestatītu parametrus tīmekļa programmas atbalstam atvērt standartu OAuth 2.0, kas ļauj lietotājam piešķirt “drošu deleģēto piekļuvi” programmai lietotāju vārdā, nenorādot lietotāju piekļuves akreditācijas datus. Šajā lapā varat arī izpildīt autorizēšanas procesu, iegūstot autorizācijas kodu un piekļuves marķieri. Tīmekļa programmas iestatījumus varat iestatīt lapā **Tīmekļa programmas** (**Nodoklis** \> **Iestatījumi** \> **Elektroniskie ziņojumi** \> **Tīmekļa programmas**).

Nākamajā tabulā ir aprakstīti lauki lapā **Tīmekļa programmas**.

| Lauks                         | Apraksts |
|-------------------------------|-------------|
| Lietojumprogrammas nosaukums              | Ievadiet tīmekļa programmas nosaukumu. |
| Apraksts                   | Ievadiet tīmekļa programmas aprakstu. |
| Pamata vietrādis URL                      | Ievadiet tīmekļa programmas interneta pamatadresi. |
| Autorizācijas URL ceļš        | Norādiet URL izveides ceļu autorizēšanai.  |
| Marķiera URL ceļš                | Norādiet URL izveides ceļu marķierim.  |
| Novirzīšanas vietrādis URL                  | Ievadiet novirzīšanas URL.  |
| Klienta ID                     | Ievadiet tīmekļa programmas klienta ID.  |
| Klienta noslēpums                 | Ievadiet tīmekļa programmas klienta noslēpumu.  |
| Servera marķieris                  | Ievadiet tīmekļa programmas servera marķieri.  |
| Autorizācijas formāta kartēšana  | Atlasiet elektronisko pārskatu veidošanas (ER) formātu, kas jāizmanto, lai ģenerētu autorizācijas pieprasījumu.   |
| Importēt marķieru modeļa kartēšanu    | Atlasiet ER importēšānas modeļa kartēšanu, kas jāizmanto, lai saglabātu piekļuves marķieri.  |
| Piešķirtais diapazons      Piekļuves marķiera termiņa beigas ir  | Šis lauks tiks atjauninātas automātiski. Tā vērtība parāda tīmekļa programmas pieprasījumiem piešķirto diapazonu.  |
| Pieņemt                        | Norādiet tīmekļa pieprasījuma pieņemšanas rekvizītu. Piemēram, “application/vnd.hmrc.1.0+json”.  |
| Satura veids           | Norādiet satura veidu. Piemēram, “application/json”.  |

Tālāk noradītās funkcijas autorizēšanas procesa atbalstam ir pieejamas lapā **Tīmekļa programmas**.
-   **Iegūt autorizācijas kodu** — inicializē tīmekļa programmas autorizāciju.
-   **Iegūt piekļuves marķieri** — inicializē piekļuves marķiera ieguvi.
-   **Atsvaidzināt piekļuves marķieri** — atsvaidzina piekļuves marķieri.

Kad tīmekļa programmas piekļuves marķieris ir saglabāts šifrētā formātā sistēmas datubāzē, to var izmantot tīmekļa pakalpojumu pieprasījumiem. Drošības nolūkos piekļuvi piekļuves marķierim ir jāierobežo tikai tām drošības lomām, kurām ir atļauts risināt šos pieprasījumus. Ja lietotājs ārpus drošības grupas mēģina risināt pieprasījumu, izņēmums informē lietotāju, ka viņam nav atļauts sadarboties, izmantojot atlasīto tīmekļa programmu.
Izmantojiet kopsavilkuma tabulu **Drošības lomas** lapā Nodokļi > Iestatījumi > Elektroniskie ziņojumi > Tīmekļa programmas, lai iestatītu lomas, kurām jābūt piekļuvei piekļuves marķierim. Ja drošības lomas tīmekļa programmai nav definētas, tikai sistēmas administrators var sadarboties, izmantojot šo tīmekļa programmu.

### <a name="web-service-settings"></a>Tīmekļa pakalpojuma iestatījumi

Tīm. pakalp. iestatījumus izmanto, lai iestatītu tiešo datu pārs. uz tīm. pakalp. Tīmekļa pak. iestatījumus var iestatīt lapā **Tīm. pak. iestat.** (**Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Tīm. pak. iestat.**).

Nākamajā tabulā ir aprakstīti lauki lapā **Tīmekļa pakalpojumu iestatījumi**.

| Lauks                   | apraksts |
|-------------------------|-------------|
| Tīmekļa pakalpojums             | Ievadiet tīmekļa pak. nosaukumu. |
| apraksts             | Ievadiet tīmekļa pakalpojuma aprakstu. |
| Interneta adrese        | Ievadiet tīm. pakalpojuma interneta adresi. Ja tīmekļa programma tīmekļa pakalpojumam ir norādīta un interneta adresei jābūt tādai pašai kāda ir definēta atlasītajai tīmekļa programmai, noklikšķiniet uz pogas **Kopēt pamata URL**, lai kopētu tīmekļa programmas **Pamata URL** uz tīmekļa pakalpojuma lauku **Interneta adrese**.  |
| Sertifikāts             | Atlasiet Key Vault sertifikātu, kas iestatīts iepriekš. |
| Tīmekļa lietojumprogramma         | Atlasiet Key Vault sertifikātu, kas iestatīts iepriekš. |
| Atbildes veids — XML | Iestatiet šai opcijai **Jā**, ja atbildes tips ir XML. |
| Pieprasīšanas metode          | Norādiet pieprasījuma metodi. HTTP definē pieprasījuma metožu kopu, kas norāda darbību, kura jāveic attiecīgajam resursam. Metode var būt **GET**, **POST** vai cita HTTP metode. |
| Pieprasījuma galvenes         | Norādiet piepras. galv. Pieprasījuma galvene ir HTTP galvene, ko var izmantot HTTP pieprasījumā un kas nav saistīta ar ziņojuma saturu. |
| Pieņemt                  | Norādiet tīmekļa pieprasījuma pieņemšanas rekvizītu. |
| Akceptēt kodēšanu         | Norādiet kodēš. akceptēšanu. Kodēšanas akceptēšanas pieprasījuma HTTP galvene izziņo klientam saprotamu satura kodēšanu. Šī satura kodēšana parasti ir saspiešanas algoritms. |
| Satura veids            | Norādiet satura tipu. Satura tipa elementa galvene norāda resursa plašsaziņas līdzekļu tipu. |
| Sekmīgas atbildes kods   | Norādiet HTTP statusa kodu, kas norāda, ka pieprasījums bija veiksmīgs. |
| Pieprasījuma galveņu formāta kartēšana  | Atlasiet ER formātu tīmekļa pieprasījuma galvenes ģenerēšanai. |

### <a name="message-processing-actions"></a>Ziņojuma apstrādes darbības

Ziņojumu apstr. darbības izmanto, lai izveidotu darbības jūsu procesiem un iestatītu to parametrus. Ziņojumu apstrādes darbības var iestatīt lapā **Ziņojumu apstrādes darbības** (**Nodoklis** \> **Iestatījumi** \> **Elektr. ziņojumi** \> **Ziņojumu apstr. darbības**).

Tabulā ir aprakstīti lapā **Ziņojumu apstrādes darbības** esošie lauki.

#### <a name="general-fasttab"></a>Cilne Vispārīgi

| Lauks                   | apraksts |
|-------------------------|-------------|
| Darbības veids             | Atlasiet darbības tipu. Informāciju par pieejamajām opcijām skatiet sadaļā [Ziņojumu apstrādes darbību tipi](#message-processing-action-types). |
| Formāta kartēšana          | Atlasiet ER formātu, kas jāizsauc attiecīgajai darbībai. Šis lauks ir pieejams tikai darbību tipiem **Elektr. pārsk. veidoš. eksports**, **Elektr. pārsk. veidoš. imports**, **Elektr. pārsk. veidoš. eksporta ziņojums**. |
| Formāta kartējums URL ceļam | Atlasiet ER formātu, kas jāizsauc attiecīgajai darbībai. Šis lauks ir pieejams tikai darbību tipiem **Tīmekļa pakalpojumi** un tiek izmantots, lai veidotu ceļu URL adresei, kas tiks pievienota interneta pamatadresei, kas norādīta atlasītajam tīmekļa serverim. |
| Ziņojuma krājuma veids       | Atlasiet ierakstu tipu, kuram ir jāizvērtē attiecīgā darbība. Šis lauks ir pieejams darbību tipiem **Ziņojuma vienuma izpildes līmenis**, **Elektr. pārsk. veidoš. eksports**, **Elektr. pārsk. veidoš. imports** un **Tīmekļa pakalpojumi**, kā arī dažiem citiem tipiem. Ja šis lauks ir atstāts tukšs, tiek novērtēti visi ziņojumu vienumu tipi, kas definēti ziņojumu apstrādei. |
| Izpildāmā klase        | Atlasiet iepriekš izveidotos izpildāmās klases iestatījumus. Šis lauks ir pieejams tikai darbību tipiem **Ziņojuma vienuma izpildes līmenis** un **Ziņojuma vienuma izpildes līmenis**. |
| Ierakstu aizpildīšanas darbība | Atlasiet iepriekš iestatīto ierakstu aizpildīšanas darbību. Šis lauks ir pieejams tikai darbību tipam **Aizpildīt ierakstus**. |
| Tīmekļa pakalpojums  | Atlasiet iepriekš iestatīto tīmekļa pakalpojumu. Šis lauks ir pieejams tikai darbību tipam **Tīmekļa pakalpojumi**.  |
| Faila nosaukums  | Norādiet nosaukumu failam, kas izraisīs darbību — atbildi no tīmekļa servera vai pārskata ģenerēšanu. Šis lauks ir pieejams tikai darbību tipiem **Tīmekļa pakalpojumi** un **Elektroniskā pārskata veidošanas eksporta ziņojums**.   |
| Rādīt dialoglodziņu  | Atzīmējiet šo izvēles rūtiņu, ja dialogs ir jāparāda lietotājam pirms pārskata izveidošanas. Šis lauks ir pieejams tikai darbību tipam **Elektroniskā pārskata veidošanas eksporta ziņojums**.   |

##### <a name="message-processing-action-types"></a>Ziņojumu apstrādes darbību tipi

Laukā **Darbības tips** ir pieejamas tālāk norādītās opcijas.

- **Izveidot ziņojumu** — lietojiet šo tipu, lai lietotāji manuāli izveidotu ziņojumus lapā **Elektr. ziņoj**. Šim darbības tipam nevar iestatīt sākotnējo statusu.
- **Aizpildīt ierakstus** — darbība **Aizpildīt ierakstus** jāiestata iepriekš. Saistiet to ar darbības tipu **Aizpildīt ierakstus**, lai to varētu iekļaut apstrādē. Tiek pieņemts, ka šo darbības tipu lieto vai nu pirmajai darbībai ziņojumu apstrādē (ja iepriekš nav izveidots elektroniskais ziņojums), vai kā darbību, kas pievieno ziņojumu vienumus iepriekš izveidotam ziņojumam (pēc darbības tipa **Izveidot ziņojumu**). Tādēļ šim darbības tipam var iestatīt tikai ziņojumu vienumu beigu statusu. Sākotnējo statusu var iestatīt tikai ziņojumam.
- **Ziņojuma izpildes līmenis** — lietojiet šo tipu, lai iestatītu izpildāmo klasi, kas jānovērtē ziņojuma līmenī.
- **Ziņojuma vienuma izpildes līmenis** — lietojiet šo tipu, lai iestatītu izpildāmo klasi, kas jānovērtē ziņojuma vienuma līmenī.
- **Elektr. pārskata veidošanas eksports** — lietojiet šo tipu darbībām, kuras ģenerē pārskatu, kas balstās uz eksportēšanas ER konfigurāciju ziņoj. vienuma līmenī.
- **Elektronisko pārskatu veidošanas eksporta ziņojums** — lietojiet šo tipu darbībām, kuras ģenerē pārskatu, kas balstās uz eksportēšanas ER konfigurāciju ziņojuma līmenī (piem., ja ziņojumam nav neviena ziņojuma vienuma).
- **Elektr. pārsk. veidošanas imports** — lietojiet šo tipu darbībām, kuras ģenerē pārskatu, kas balstās uz importēšanas ER konfigurāciju.
- **Ziņoj. līm. lietotāja apstrāde** — lietojiet šo tipu darbībām, kas paredz manuālas lietot. darbības. Piemēram, lietotājs var atjaunināt ziņojumu statusu.
- **Lietotāja apstrāde** — lietojiet šo tipu darbībām, kas paredz manuālu lietotāja darbību. Piemēram, lietotājs var atjaunināt ziņojumu vienumu statusu.
- **Tīm. pakalpojums** — lietojiet šo tipu darbībām, kas ģenerēto pārskatu nosūta uz tīm. pakalpojumu. Šo darbības tipu neizmanto Itālijas pirkšanas un pārdošanas rēķinu paziņojumu pārskatiem. Darbību tipam **Tīmekļa pakalpojumi** lapas **Ziņojumu apstrādes darbības** kopsavilkuma cilnē **Detalizēta papildinformācija** varat norādīt **Apstiprinājuma teksts**. Šis apstiprinājuma teksts tiks parādīts lietotājam pirms atlasītā tīmekļa pakalpojuma pieprasījuma risināšanas.
- **Pieprasīt verifikāciju** — lietojiet šo tipu, lai piepr. verif. no servera.

#### <a name="initial-statuses-fasttab"></a>Cilne Sākotnējie statusi

> [!NOTE]
> Kopsavilkuma cilne **Sākotnējie statusi** nav pieejama darbībām, kuru sākotnējais tips ir **Izveidot ziņojumu**.

| Lauks               | Apraksts                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Ziņojuma krājuma statuss | Atlasiet ziņojuma vienuma statusu, kuram ir jānovērtē atlasītā ziņojumu apstrādes darbība. |
| apraksts         | Atlasītā ziņojuma vienuma statusa apraksts.                                                  |

#### <a name="result-statuses-fasttab"></a>Cilne Beigu statusi

| Lauks               | apraksts |
|---------------------|-------------|
| Ziņojuma statuss      | Atlasiet ziņojuma statusu, kuram ir jānovērtē atlasītā ziņojumu apstrādes darbība. Šis lauks ir pieejams tikai ziņojumu apstrādes darbībām, kas tiek novērtētas ziņojuma līmenī. Piemēram, tas ir pieejams darbību tipiem **Elektr. pārsk. veidoš. eksports** un **Elektr. pārsk. veidoš. imports**. Tas nav pieejams darbību tipiem **Lietotāja apstrāde** un **Ziņojuma krājuma izpildes līmenis**. |
| apraksts         | Atlasītā ziņojuma statusa apraksts. |
| Atbildes veids       | Atlasītā ziņojuma statusa atbildes tips. |
| Ziņojuma krājuma statuss | Atlasiet beigu statusus, kuriem jābūt pieejamiem pēc atlasītās ziņojumu apstrādes darbības novērtēšanas. Šis lauks ir pieejams tikai ziņojumu apstrādes darbībām, kas tiek novērtētas ziņojuma vienuma līmenī. Piemēram, tas ir pieejams darbību tipiem **Lietotāja apstrāde** un **Ziņojuma krājuma izpildes līmenis**. Ziņojumu apstrādes darbībām, kuras tiek novērtētas ziņojuma līmenī, šis lauks rāda ziņojuma vienuma statusu, kas tika iestatīts atlasītajam ziņojuma statusam. |

Nākamajā tabulā parādīts, kādi rezultātu statusi ir jāiestata saistībā uz darbību tipiem.

| Elektroniskā ziņojuma darbības tips\ atbildes veids  | Izpildīts veiksmīgi  | Biznesa kļūda  | Tehniska kļūda  | Lietotāja definēts  | Atcelt  |
|-------------------------------------------------|--------------|---------|-------|-----|-----------------|
| Izveidot ziņojumu                                  | X            |         |       |     |                 |
| Elektroniskā pārskata veidošanas eksports                     | X            |         |       |     |                 |
| Elektroniskā pārskata veidošanas imports                     |              |         |       |     |                 |
| Tīmekļa pakalpojums                                     | X            |         | X     |     |                 |
| Lietotāja apstrāde                                 |              |         |       |     |                 |
| Ziņojuma izpildes līmenis                         |              |         |       |     |                 |
| Aizpildīt ierakstus                                |              |         |       |     |                 |
| Ziņojuma krājuma izpildes līmenis                    |              |         |       |     |                 |
| Pieprasīt verifikāciju                            | X            |  X      | X     |     |                 |
| Elektronisko pārskatu veidošanas eksporta ziņojums             | X            |         |       |     |                 |
| Ziņojuma līmeņa lietotāja apstrāde                   |              |         |       |     |                 |

### <a name="electronic-message-processing"></a>Elektroniska ziņojuma apstrāde

Elektroniska ziņojuma apstrāde ir elektronisko ziņojumu funkcionalitātes pamatkoncepts. Tā apkopo darbības, kuras jānovērtē elektroniskajam ziņojumam. Darbības var saistīt, izmantojot sākotnējo statusu un beigu statusu. Vai arī darbības, kuru tips ir **Lietotāja apstrāde**, var sākt neatkarīgi. Lapā **Elektroniskā ziņojuma apstrāde** (**Nodoklis** \> **Iestatījumi** \> **Elektroniskie ziņojumi** \> **Elektroniskā ziņojuma apstrāde**) varat arī atlasīt papildu laukus, kuri ir jāatbalsta apstrādei vai nu ziņojuma līmenī, vai ziņojuma vienumu līmenī.

Kopsav. cilne **Darbība** ļauj pievienot iepr. definētas darb. apstrādei. Var norādīt, vai darbība ir jāpalaiž atsevišķi vai arī to var sākt apstrāde. Lai definētu, vai darbību var inicializēt tikai lietotājs, atzīmējiet izvēles rūtiņu **Izpildīt atsevišķi** apstrādes darbībām. Noņemiet atzīmi parametram **Izpildīt atsevišķi**, ja vēlaties, lai darbība tiktu izpildīta apstrādē, kad ziņojumu vai ziņojumu vienumu statuss ir definēts kā sākotnējais statuss šai darbībai. Darbības tips **Lietotāja darbība** ir jāpalaiž tikai atsevišķi. 

Dažreiz var būt nepieciešams apkopot vairākas secīgas darbības, pat ja pirmā no tām ir definēta atsevišķai palaišanai. Piemēram, kad ir nepieciešams, lai pārskata ģenerēšanu inicializē lietotājs, bet pēc tam, kad pārskats ir ģenerēts, tas nekavējoties jānosūta uz tīmekļa pakalpojumu, un atbildes no tīmekļa pakalpojuma ir jāatspoguļo sistēmā. Šādam nolūkam varat izmantot parametru **Nedalāma sērija**. Lai to izdarītu, noklikšķiniet uz pogas **Nedalāma sērija** lapas **Elektronisko ziņojumu apstrāde** kopsavilkuma cilnes **Darbība** darbību rūtī, izveidojiet sēriju un atlasiet to kolonnā **Nedalāma sērija**, kur apkopotas darbības, kas ir vienmēr izpildāmas kopā. Pirmo darbību šajā gadījumā var iestatīt kā **Izpildīt atsevišķi**, bet visas pārējās nevar.

Kopsav. cilne **Ziņ. vienuma papildu lauki** ļauj pievienot iepriekš defin. papildu laukus, kas saistīti ar ziņ. vienumiem. Ir jāpievieno papildu lauki katram ziņojuma vienuma tipam, ar kuru lauki ir saistīti.

Kopsav. cilne **Ziņoj. papildu lauki** ļauj pievienot iepriekš defin. papildu laukus, kas saistīti ar ziņojumiem.

Kopsav. cilne **Drošības lomas** ļauj iestatīt drošības lomas, kas ir iepriekš definētas sistēmā noteiktai apstrādei. Lietot., kam ir noteikta loma, redz tikai apstrādi, kas definēta attiecīgajai lomai.

Kopsav. cilne **Pakete** ļauj iestatīt apstrādi darbam pakešveida režīmā.

## <a name="work-with-electronic-messages-functionality"></a>Darbs ar elektr. ziņojumu funkcionalitāti

Strādājot ziņojuma līmenī, noderīgāka ir lapa **Elektroniskie ziņojumi** (**Nodoklis** \> **Pieprasījumi un pārskati** \> **Elektroniskie ziņojumi** \> **Elektroniskie ziņojumi**). Strādājot datu vākšanas (ziņojuma vienuma) līmenī, noderīgāka ir lapa **Elektroniskā ziņojuma vienumi** (**Nodoklis** \> **Pieprasījumi un pārskati** \> **Elektroniskie ziņojumi** \> **Elektr. ziņojuma vienumi**).

### <a name="electronic-messages"></a>Elektroniskie ziņojumi

Lapa **Elektroniskie ziņojumi** norāda apstrādi, kas ir pieejama jums, pamatojoties uz jūsu lomu. Drošības lomas tiek saistītas ar apstrādi, iestatot attiecīgo apstrādi. Katrai apstrādei, kas jums ir pieejama, lapā ir redzami elektroniskie ziņojumi un ar tiem saistītā informācija.

Kopsav. cilnē **Ziņojumi** tiek rādīti atlasītās apstrādes elektron. ziņojumi. Atkarībā no atlasītā ziņojuma un iepriekš definētas apstrādes statusa dažas darbības var palaist, atlasot pogas virs režģa:

- **Jauns** — šī poga ir saistīta ar darbībām, kuru tips ir **Izveidot ziņojumu**.
- **Dzēst** — šī poga ir pieejama, ja atlasītā ziņojuma pašreizējam statusam ir atzīmēta izvēles rūtiņa **Atļaut dzēšanu**.
- **Apkopot datus** — šī poga ir saistīta ar darbības tipu **Aizpildīt ierakstus**.
- **Ģenerēt pārskatu** — šī poga ir saistīta ar darbību tipu **Elektr. pārsk. veidoš. eksporta ziņojums**.
- **Sūtīt pārskatu** — šī poga ir saistīta ar darbību tipu **Tīmekļa pakalpojums**.
- **Importēt atbildi** — šī poga ir saistīta ar darbību tipu **Elektroniskā pārskata veidošanas imports**.
- **Atjaunināt statusu** — šī poga ir saistīta ar darbību tipu **Ziņojuma līmeņa lietotāja apstrāde**.
- **Ziņojuma vienumi** — atv. lapu **Elektr. ziņoj. vienumi**.

Kopsav. cilnē **Darbību žurnāls** ir redzama inform. par visām darbībām, kas izpildītas atlasītajam ziņojumam. Ja darbība atgriež kļūdu, informācija par kļūdu būs pievienota saistītajai darbību žurnāla rindai. Atlasiet rindu un noklikšķiniet uz **saspraudes** pogas lapas augšējā labajā stūrī, lai pārskatītu informāciju par kļūdu.

Kopsavilkuma cilnē **Ziņojuma papildu lauki** ir redzami visi papildu lauki, kas definēti ziņojumiem apstrādes iestatījumos. Tajā arī redzamas šo papildu lauku vērtības.

Kopsav. cilnē **Ziņojuma vienumi** ir redzami visi ziņ. vienumi, kas saistīti ar atlasīto ziņojumu. Katram ziņojuma vienumam var izmantot kādu no tālāk noradītajām funkcijām atkarībā no attiecīgā ziņojuma vienuma statusa.

- **Dzēst** — šī poga ir pieejama, ja atlasītā ziņojuma vienuma pašreizējam statusam ir atzīmēta izvēles rūtiņa **Atļaut dzēšanu**.
- **Atjaunināt statusu** — šī poga ir saistīta ar darbību tipu **Lietotāja apstrāde**.
- **Oriģinālais dokuments** — šī poga ļauj lietotājam atvērt lapu ar atlasītā ziņojuma oriģinālo dokumentu.

Var pārskatīt visus atlasītā ziņojuma pielikumus. Šie pielikumi ir pārskati, kas jau ir ģenerēti un saņemti. Atlasiet ziņojumu, kuram pārskatīt pielikumus, un pēc tam atlasiet pogu **Pielikums** darbību rūtī.

![Poga Pielikums](media/attachment-icon.png)

Poga **Pielikums** norāda visus pielikumus, kas ir saistīti ar ziņojumu. Lai skatītu failu, atlasiet to sarakstā pa kreisi un pēc tam atlasiet **Atvērt** darbību rūtī.

![Poga Atvērt](media/open-button.png)

Lai skatītu pielikumu, kas saistīts ar noteiktu darbību, kura iepriekš izpildīta ziņojumam, atlasiet ziņojumu lapā **Elektroniskie ziņojumi**, un pēc tam kopsavilkuma cilnē **Darbību žurnāls** atlasiet darbību. Pēc tam atlasiet pogu **Pielikums** darbību rūtī.

Varat palaist arī visu apstrādi vai tikai konkrētu darbību, atlasot darbību rūtī **Palaist apstrādi**.

### <a name="electronic-message-items"></a>Elektroniskie ziņojumu krājumi

Lapā **Elektr. ziņoj. vienumi** ir norādīti visi ziņojuma vienumi un tādu darbību žurnāls, kas izpildītas katram ziņojuma vienumam. Tajā arī ir norādīti papildu lauki, kas ir definēti ziņojuma vienumiem, un šo papildu lauku vērtības.

Nākamajā tabulā ir aprakstīti lauki cilnē **Ziņojuma vienumi**.

<table>
<thead>
<tr>
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr>
<td>Apstrādā</td>
<td>Apstrādes nosaukums, kas izmantota, lai izveidotu ziņojuma vienumu.</td>
</tr>
<tr>
<td>Ziņojuma krājums</td>
<td>Ziņojuma vienuma ID. Šis ID tiek piešķirts automātiski, pamatojoties uz <strong>Ziņojuma vienuma</strong> numura sēriju, kas definēta lapā <strong>Virsgrāmatas parametri</strong>.</td>
</tr>
<tr>
<td>Ziņojuma krājuma datums</td>
<td>Ziņojuma vienuma izveidošanas datums.</td>
</tr>
<tr>
<td>Ziņojuma krājuma veids</td>
<td>Ziņojuma vienuma tips. Tai pašai apstrādei var iestatīt vairāku tipu ziņojuma vienumus (piemēram, <strong>Ienākošie rēķini</strong> un <strong>Izejošie rēķini</strong>). Šo lauku var aizpildīt automātiski tikai tad, kad rēķins tiek pievienots ziņojumu vienumu tabulā.</td>
</tr>
<tr>
<td>Ziņojuma krājuma statuss</td>
<td>Ziņojuma vienuma faktiskais statuss. Pieejamie statusi mainās atkarībā no ziņojuma vienumu tipa. Daži piemēri:
<ul>
<li><strong>Aizpildīts</strong> — ieraksts tika pievienots ziņ. vienumu tabulā.</li>
<li><strong>Novērtēts</strong> — ziņojuma vienumam tika aprēķināti papildu atribūti.</li>
<li><strong>Iekļauts pārskatā</strong> — ziņ. vienums veiksmīgi pievienots pārskatā.</li>
<li><strong>Nav iekļauts</strong> — šis statuss var būt noderīgs, ja daži ziņ. vienumi jāizslēdz no pārskata pirms tā eksportēšanas.</li>
</ul>
</td>
</tr>
<tr>
<td>Pārsūtīšanas datums</td>
<td>Apstrādei, kas automātiski pārsūta ģenerēto pārskatu ārpus sistēmas, datums, kad tika pārsūtīts ziņojuma vienums.</td>
</tr>
<tr>
<td>Dokumenta numurs</td>
<td>Šis lauks tiek aizpildīts automāt., balstoties uz ierakstu aizpildīš. darb. iestatījumu. Šo lauku var aizpildīt automātiski tikai tad, kad rēķins tiek pievienots ziņojumu vienumu tabulā.</td>
</tr>
<tr>
<td>Konta numurs</td>
<td>Debitora vai kreditora konta numurs (vai cita lauka vērtība atkarībā no lauka, kas definēts darbībai <strong>Aizpildīt ierakstus</strong>). Šo lauku var aizpildīt automātiski tikai tad, kad rēķins tiek pievienots ziņojumu vienumu tabulā.</td>
</tr>
<tr>
<td>Paziņojums</td>
<td>Ziņojuma numurs. Šis numurs tiek piešķirts automātiski, pamatojoties uz <strong>Ziņojuma</strong> numura sēriju, kas definēta lapā <strong>Virsgrāmatas parametri</strong>.</td>
</tr>
<tr>
<td>Ziņojuma statuss</td>
<td>Elektroniskā ziņojuma faktiskais statuss.</td>
</tr>
<tr>
<td>Nākamā darbība</td>
<td>Nākamās darbības, kuras var sākt ziņojuma vienuma pašreizējam statusam.</td>
</tr>
</tbody>
</table>

Cilnē **Papildu lauki** tiek rādīti papildu lauki atlasītajam ziņojuma vienumam un to vērtības.

#### <a name="run-processing"></a>Apstrādes palaišana

Darbību rūtī atlasiet **Palaist apstrādi**, lai palaistu apstrādi ziņojuma vienumiem. Lai palaistu noteiktu darbību, dialoglodziņā **Palaist apstrādi** opcijai **Atlasīt darbību** iestatiet **Jā** un tad atlasiet darbību. Lai palaistu visu apstrādi, opcijai **Atlasīt darbību** iestatiet **Nē**.

#### <a name="generate-report"></a>Ģenerēt pārskatu

Darbību rūtī atlasiet **Ģenerēt pārskatu**, lai ģenerētu pārskatu. Šī poga ir saistīta ar darbību tipu **Elektroniskā pārskata veidošanas eksports**.

#### <a name="update-status"></a>Atjaunināt statusu

Darbību rūtī atlasiet **Atjaun. statusu**, lai atjaun. viena vai vairāku ziņ. vien. statusu. Dialoglodziņā **Atjaun. statusu** lietojiet cilni **Iekļaujamie ieraksti**, lai atl. atjaunināšanai ziņ. vien. Pārliecinieties, vai ir pareizi definēti atlases kritēriji, jo ziņojuma vienumu statusi tiks atjaunināti saskaņā ar šiem kritērijiem, atlasītās darbības sākotnējo statusu un jūsu iestatīto vērtību **Jauns statuss**. Pēc statusa atjaunināšanas pabeigšanas būs grūti noteikt, kuri vienumi tikko tika atjaunināti. Tādēļ būs grūti atritināt statusa atjauninājumus.

#### <a name="electronic-messages"></a>Elektroniskie ziņojumi

Darbību rūtī atlasiet **Elektroniskais ziņojums**, lai apskatītu elektr. ziņojumu, kas saistīts ar atlasīto ziņojuma vienumu.

Var arī apskatīt visus failus, kas atbilst ziņojuma vienumam. Atlasiet ziņojuma vienuma lauku **Ziņojums** vai atlasiet **Elektroniskais ziņojums** darbību rūtī. Lapā **Elektroniskais ziņojums** atlasiet ziņojumu, kuram skatīt pārskatu, un tad atlasiet pogu **Pielikums** darbību rūtī.

![Poga Pielikums](media/attachment-icon.png)

Poga **Pielikums** norāda visus pielikumus, kas ir saistīti ar ziņojumu. Lai skatītu failu, atlasiet to sarakstā pa kreisi un pēc tam atlasiet **Atvērt** darbību rūtī.

![Poga Atvērt](media/open-button.png)

#### <a name="original-document"></a>Oriģinālais dokuments

Atlasiet **Oriģinālais dokuments** darbību rūtī, lai atvērtu sākotnējo dok. atlasītajam ziņojuma vienumam.

## <a name="example"></a>Paraugs

Pēc tam, kad ER formāts ir izveidots, kartēts uz datu avotiem un pabeigts, to var palaist, izmantojot darbvietu **Elektr. pārskatu veidošana**. Tiek ģenerēts pārskats, ko var saglabāt lokāli.

Lai kontrolētu šādus pārskatu veidošanas procesa aspektus, ir jāiestata elektr. ziņojumapmaiņas apstrāde:

- Reģistrējiet inf. par to, kas ģenerējis pārsk.
- Reģ., kad pārskats tika ģenerēts.
- Saglabājiet pārsk., kas tika ģenerēti par iepr. periodiem.

Šajā sadaļā ir sniegts piemērs, kā var iestatīt elektronisko ziņojumu funkcionalitāti, lai izveidotu pārskatu veidošanas procesu.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Izveidot un palaist apstr., lai izsauktu vienk. ER eksp. formātu Excel pārsk. ģenerēšanai

Šajā sadaļā sniegts piemērs, kā var iestatīt elektronisko ziņojumapmaiņu, lai ģenerētu pārskatu, kas balstās uz eksportēšanas ER formātu programmai Excel. Lai sekotu šim piemēram, ER Excel eksportēšanas formātam jau jābūt izveidotam, kartētam uz datu avotiem un pabeigtam. Numuru sērijai jau jābūt iestatītai elektroniskajiem ziņojumiem.

Veidojot apstrādi, ir noderīgi vispirms definēt apstrādes darbības un statusus, kas tiks iestatīti. Šajā attēlā parādīts, kā apstrāde izskatās šajā piemērā.

![Apstrādes shēma](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Ziņoj. statusu izveide

1. Dod. uz **Nodoklis \> Iestat. \> Elektr. ziņ. \> Ziņ. statusi**.
2. Izveidojiet šādus ziņojumu statusus:

    - Jauns
    - Sagatavots
    - Ģenerēts

    ![Ziņojuma statusi](media/message-statuses.png)

3. Statusa **Jauns** rindā atzīmējiet izv. rūtiņu **Atļaut dzēšanu**, lai ļautu lietotājiem dzēst ziņoj., kuriem ir šis statuss.

#### <a name="create-additional-fields"></a>Papildu lauku izveide

1. Dod. uz **Nodoklis \> Iestat. \> Elektr. ziņ. \> Papildu lauki**.
2. Pievienojiet pap. lauku un tā vērtību. Tālāk ir minēts piemērs.

    ![Papildlauki](media/additional-fields.png)

3. Opc. **Lietot. laboj.** iest. **Jā**, lai ļautu lietot. red. lauku.

#### <a name="create-message-processing-actions"></a>Ziņoj. apstrādes darbību izveide

Šajā piemērā tiks izveidotas šādas darbības:

- **Izveidot ziņojumu**
- **Atjaun. uz Sagat.**
- **Ģenerēt pārsk.**
- **Atjaun. uz sākotn. statusu** (neobl.)

1. Dod. uz **Nodoklis \> Iestat. \> Elektr. ziņ. \> Ziņ. apstrādes darbības**.
2. Izveidojiet darbību ar nosauk. **Izveidot ziņ**. Kopsav. cilnes **Vispārīgi** laukā **Darbības tips** atlasiet **Izveidot ziņoj**.
3. Izveidojiet darb. ar nosauk. **Atjaunināt uz Sagatavots** un iestatiet šādus laukus:

    - Kopsav. cilnes **Vispārīgi** laukā **Darbības tips** atlasiet **Ziņoj. līmeņa lietotāja apstrāde**.
    - Kopsav. cilnes **Sākotnējie statusi** laukā **Ziņojuma statuss** atlasiet **Jauns**.
    - Kopsav. cilnes **Beigu statusi** laukā **Ziņojuma statuss** atlasiet **Sagatavots**. Laukā **Atbildes tips** ievadiet **Izpildīts veiksmīgi**.

4. Izveidojiet darbību ar nosaukumu **Ģenerēt pārskatu** un iestatiet šādus laukus:

    - Kopsav. cilnes **Vispārīgi** laukā **Darbības tips** atl. **Elektr. pārsk. veidoš. eksports**. Laukā **Formāta kartēšana** atlasiet eksportēšanas ER formātu. Opcijas ir: **Excel**, **XML**, **JSON**, **Teksts** un **Cits**.
    - Kopsav. cilnes **Sākotnējie statusi** laukā **Ziņojuma statuss** atlasiet **Sagatavots**.
    - Kopsav. cilnes **Beigu statusi** laukā **Ziņojuma statuss** atlasiet **Ģenerēts**. Laukā **Atbildes tips** ievadiet **Izpildīts veiksmīgi**.

    ![Pārsk. darbības ģener.](media/generate-report-action.png)

5. Neobligāti: lai ļautu lietot. atkārtoti ģen. pārsk. vairākas reizes, var izveidot darb. **Atjaun. uz sākotn. statusu** un iest. šādus laukus:

    - Kopsav. cilnes **Vispārīgi** laukā **Darbības tips** atlasiet **Ziņoj. līmeņa lietotāja apstrāde**.
    - Kopsav. cilnes **Sākotnējie statusi** laukā **Ziņojuma statuss** atlasiet **Ģenerēts**.
    - Kopsav. cilnes **Beigu statusi** laukā **Ziņojuma statuss** atlasiet **Sagatavots** un/vai **Jauns**. Laukā **Atbildes tips** ievadiet **Izpildīts veiksmīgi**.

#### <a name="electronic-message-processing"></a>Elektroniska ziņojuma apstrāde

Šajā piemērā visas darbības jāiestata tā, lai tās tiktu palaistas atsevišķi. Tiek pieņemts, ka katru darbību sāks lietotājs.

1. Dod. uz **Nodoklis \> Iestat. \> Elektr. ziņ. \> Elektr. ziņojuma apstrāde**.
2. Pievienojiet ierakstu apstrādei, un pievienojiet visas iepriekš defin. darbības un papildu lauku.
3. Neobligāti: kopsav. cilnē **Drošības lomas** definējiet droš. lomas apstrādei, lai ierobežotu piekļuvi noteiktiem pārskatiem.
4. Dod. uz **Nodoklis \> Piepras. un pārsk. \> Elektr. ziņojumi \> Elektr. ziņojumi**.
5. Atl. **Jauns**, lai izveidotu ziņ. Šajā brīdī varat pievienot datumus un aprakstu. Varat arī atjaunināt papildu lauka vērtību, ja nepieciešams.

    ![Elektron. ziņojuma izveide](media/create-electronic-message.png)

Režģis kopsav. cilnē **Darbību žurnāls** tiek automātiski aizpildīts ar visu darbību žurnālu, kuras veiktas ar ziņojumu.

Tagad varat dzēst vai atjaunināt ziņojuma statusu. Lai atjaunin. ziņ. statuss, atlasiet **Atjaunināt statusu** un tad laukā **Jauns statuss** atlasiet **Sagatavots**. Tad atl. **Labi**.

![Ziņojuma statusa atjaun.](media/update-status.png)

Ziņojuma statuss tiek atjaunināts uz **Sagatavots**, un tagad var ģenerēt pārskatu, atlasot **Ģenerēt pārskatu**. Tiek ģenerēts pārskats, un ziņoj. statuss un darb. žurn. tiek atjaunināti. Lai skatītu ģenerēto pārskatu, atlasiet pogu **Pielikums** darbību rūtī.
