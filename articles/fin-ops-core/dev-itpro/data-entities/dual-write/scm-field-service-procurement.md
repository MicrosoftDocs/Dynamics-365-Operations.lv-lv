---
title: Integrēt sagādes starp Supply Chain Management un Field Service
description: Šajā tēmā aprakstīts, kā duālā rakstīšanas integrācija atbalsta pirkšanas pasūtījuma izveidi un atjauninājumus gan no Supply Chain Management, gan Field Service.
author: RamaKrishnamoorthy
ms.date: 11/11/2020
ms.topic: article
audience: Application User
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ab251ee60bf3c831b0139beb9557c6b3faaf9f66
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783287"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Integrēt sagādes starp Supply Chain Management un Field Service

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management nodrošina robustu sagādes funkcionalitāti. Dynamics 365 Field Service piedāvā līdzīgu funkcionalitāti, kas atbalsta ar pakalpojuma procesu saistītos iepirkumu procesus. Šo divu programmu funkcionalitāte ir integrēta ar duālās rakstīšanas palīdzību, un rezultātā iegūtie krusteniskā lietojuma gadījumi tiek iespējoti caur tabulu kartēšanu, risinājumu loģiku, skatījumiem un formām.

Šī integrācija atbalsta pirkšanas pasūtījuma izveidi un vairumā gadījumu arī abu programmu atjauninājumus. Tomēr Supply Chain Management kontrolē cenu noteikšanu, adreses un preču ieejas plūsmu. Vairākas jaudīgas krusteniskās izmantošanas situācijas ir iespējotas organizācijām, kas izmanto gan Field Service, gan Supply Chain Management. Šie izmantošanas gadījumi iespējo sagādes inicializēšanu un izsekošanu abās sistēmās.

Šajā attēlā redzamas tabulas abās sistēmās un parādīts, kā tās ir kartētas viena ar otru. Pirkšanas pasūtījumi Field Service atsaucas *uz konta* rindu, bet pirkšanas pasūtījumi Supply Chain Management atsaucē ir *kreditora* rinda. Lai atrisinātu integrāciju, duālā rakstīšana izmanto atsauci, lai saistītu *kreditora* rindas ar *konta* rindām. Plašāku informāciju skatiet šeit: [Vispārīgā informācija par integrētajiem kreditoriem](vendor-mapping.md).

![Sagādes kartējumi.](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Priekšnosacījumi

Lai integrētu Supply Chain Management ar Field Service, jums jāinstalē šādi komponenti:

- Field Service versija 8.8.31.60 vai jaunāka, vispārējā pirkšanas pasūtījuma integrācijai
- Supply Chain Management versija 10.0.14 (vai jaunāka)
- Duālā rakstīšana, lai palaistu OneFSSCM risinājumu

## <a name="installation-guidelines"></a>Instalēšanas vadlīnijas

### <a name="prerequisites"></a>Priekšnosacījumi

- **Duālā rakstīšana** - Papildinformāciju skatiet [Duālās rakstīšanas mājas](dual-write-home-page.md#dual-write-setup) lapā.
- **Dynamics 365 Field Service** – Papildinformāciju skatiet sadaļā [Kā instalēt Dynamics 365 Field Service](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Kad tie ir iespējoti Microsoft Dataverse, duālajā ierakstā un Field Service ir ieviesti vairāki risinājumu līmeņi, kas paplašinās vidi ar jauniemmetadatiem, formām, skatiem un loģiku. Šos risinājumus var iespējot jebkurā secībā, tomēr parasti jūs tos instalējiet šādā secībā:

1. **Field Service Common** – Field Service Common tiek instalēts, kad vidē ir instalēts Field Service.
2. **Field Service (Anchor)** – Field Service (Anchor) tiek instalēts, kad vidē ir instalēts Field Service. 
3. **Paplašināts Supply Chain Management** – Supply Chain Management paplašinātā versija tiek automātiski instalēta, kad vidē ir aktivizēts duālais ieraksts. 
4. **OneFSSCM risinājums** - OneFSSCM tiek automātiski instalēts atkarībā no tā, kurš risinājums (Field Service vai Supply Chain Management) ir instalēts pēdējais.

    - Ja vidē jau ir instalēts Field Service un tiek aktivizēts duālais ieraksts, kas instalē Supply Chain Management paplašināto versiju, tiek instalēts OneFSSCM.
    - Ja vidē jau ir instalēts Field Service un tiek aktivizēts duālais ieraksts, kas instalē Supply Chain Management paplašināto versiju, tiek instalēts OneFSSCM.

## <a name="initial-synchronization"></a>Sākotnējā sinhronizācija

Lai izveidotu jaunus pirkšanas pasūtījumus un strādātu ar esošajiem pirkšanas pasūtījumiem, jāsinhronizē atsauces dati starp Supply Chain Management un Dataverse. Jūs izmantojat sākotnējo rakstīšanas funkcionalitāti, lai noteiktu tabulas attiecības un atrastu tabulas, kuras jāiespējo dotai kartei.

Jāsinhronizē šādas tabulas:

- Preču veidnes

    Palaižot sākotnējo ierakstu, iegūstiet pilnu nepieciešamo tabulu sarakstu. Tālāk ir sniegti daži šo veidņu piemēri:

    - Visas preces
    - Izlaistās preces V2
    - Dataverse izlaistās atšķirīgās preces

- Vietnes
- Noliktavas
- Sagādes kategorijas veidnes

    Tālāk ir sniegti daži šo veidņu piemēri:

    - Sagādes kategorijas
    - pro
    - Preču kategoriju hierarhija
    - Preču kategoriju piešķires

- Kreditoru veidnes, piemēram, Kreditors V2
- Kontaktpersonu veidnes, piemēram, Dataverse Kontaktpersonas V2
- Darbinieku veidnes, piemēram, Darbinieks

Tabulu sinhronizācija nodrošina, ka visi Supply Chain Management dokumenti (pirkšanas pasūtījumi un produktu ieejas plūsmas) ir pieejami Dataverse.

### <a name="account-and-vendor-tables"></a>Konta un kreditoru tabulas

Pirkšanas pasūtījumi Field Service attiecas uz Konta tabulu, lai izsekotu kreditorus. Tāpēc pirkšanas pasūtījumu Dataverse tabulas izmanto kontus, lai atsekotu kreditorus. Lai pielāgotu šo galveno atšķirību, jāaktivizē šādas četras darbplūsmas, lai konti un kreditori būtu sinhronizēti: 

- Kreditoru izveide Kontu tabulā
- Kreditoru izveide Kreditoru tabulā
- Kreditoru atjaunināšana Kontu tabulā
- Kreditoru atjaunināšana Kreditoru tabulā

Ja ir instalēts OneFSSCM, jo ir instalēts gan Field Service, gan paplašinātais Supply Chain Management, šīs darbplūsmas tiek automātiski aktivizētas. Ja Field Service nav instalēts, bet jūs vēlaties integrēt pirkšanas pasūtījuma tabulas ar Dataverse, jums ir jāaktivizē šīs darbplūsmas. Abos gadījumos, ja vien netiek sākts no jauna, var nākties nodrošināt, ka visi kreditori pirms pirkšanas pasūtījumu izveidošanas Dataverse tiek izveidoti kā konti. Pretējā gadījumā radīsies kļūdas.

### <a name="initial-synchronization"></a>Sākotnējā sinhronizācija

Ja vēlaties, lai abās sistēmās būtu pieejami visi priekšnosacījumi, ja vēlaties, lai esošie pirkšanas pasūtījumi un produktu ieejas plūsmas būtu pieejamas abās sistēmās, jāveic šādu veidņu sākotnējā sinhronizācija:

- Pirkšanas pasūtījuma galvene V2
- CDS Pirkšanas pasūtījuma rinda
- CDS Pirkšanas pasūtījuma rindas vieglā dzēšana
- Pirkšanas pasūtījuma ieejas plūsma
- Pirkšanas pasūtījuma saņemtās preces

## <a name="mappings-with-logic"></a>Kartēšana ar loģiku

Sagādes integrācija paplašina preču kartēšanu ar šādu loģiku, lai nodrošinātu, ka kolonna **Field Service preces tips** ir pareizi iestatīta preču tabulā Dataverse:

- Ja **Preces tips** ir iestatīts uz *Prece* un **Krājumu modeļu grupa, uzkrātā prece** ir iestatīta uz *Patiess*, lauka **Field Service preces veids tiek** iestatīts uz *Krājumi*.
- Ja **Preces tips** ir iestatīts uz *Prece* un **Krājumu modeļu grupa, uzkrātā prece** ir iestatīta uz *Aplams*, **Field Service preces veids tiek** iestatīts uz *Nav krājums*.
- Ja **Preces veids** ir iestatīts uz *Pakalpojums*, **Field Service preces veids** ir iestatīts uz *Pakalpojums*.

Turklāt Dataverse ietver loģiku, kas kartē kreditorus ar to saistītajiem kontiem. Šī loģika iestata noklusējuma rēķina kreditora kontu. Izveidojot servera puses spraudņa loģiku iestata noklusējuma rēķina kreditora kontu no kreditora, kas ir saistīts ar kontu. Kreditoram ir atsauce uz rēķina kontu, kas tiek izmantots šīs vērtības iestatīšanai.

## <a name="supported-scenarios"></a>Atbalstītie scenāriji

- Pirkšanas pasūtījumus var izveidot un atjaunināt Dataverse lietotāji. Tomēr procesu un datus kontrolē Supply Chain Management. Supply Chain Management pirkšanas pasūtījumu kolonnu atjauninājumi tiek piemēroti, kad atjauninājumi ir no Field Service. Piemēram, jūs nevarat atjaunināt pirkšanas pasūtījumu, ja tas ir pabeigts. 
- Ja pirkšanas pasūtījumu kontrolē izmaiņu pārvaldība Supply Chain Management, Field Service lietotājs var atjaunināt pirkšanas pasūtījumu tikai tad, ja Supply Chain Management apstiprinājuma statuss ir *Melnraksts*.
- Vairākas kolonnas pārvalda tikai Supply Chain Management, un tās nevar atjaunināt Field Service. Lai uzzinātu, kuras kolonnas nevar atjaunināt, pārskatiet produkta kartēšanas tabulas. Parasti lielākā daļa šo kolonnu tiek iestatītas kā tikai lasāmas Dataverse lapās. 

    Piemēram, cenu informācijas kolonnas pārvalda Supply Chain Management. Supply Chain Management ir tirdzniecības līgumi, no kuriem Field Service var gūt labumu. Kolonnas, piemēram, **Cena par vienību**, **Atlaide**  un **Neto summa** ir tikai no Supply Chain Management. Lai pārliecinātos par cenas sinhronizāciju ar Field Service, jāizmanto **Sinhronizācijas** līdzeklis lapās **Pirkšanas pasūtījums** un **Pirkšanas pasūtījuma prece** Dataverse, ievadot pirkšanas pasūtījuma datus. Papildinformāciju skatiet sadaļā [Sinhronizācija ar Dynamics 365 Supply Chain Management sagādes datiem pēc pieprasījuma](#sync-procurement).

- **Kopsummas** kolonna ir pieejama tikai Field Service, jo Supply Chain Management nav atjauninātas pirkšanas pasūtījuma kopsummas. Supply Chain Management kopsummas tiek aprēķinātas, pamatojoties uz vairākiem parametriem, kas nav pieejami Field Service.
- Pirkšanas pasūtījuma rindas, kurās ir norādīta tikai sagādes kategorija vai kur norādītā prece ir *Pakalpojuma* preces tipa vai Field Service preces tipa krājums, var tikt iniciēta tikai Supply Chain Management. Pēc tam rindas tiek sinhronizētas ar Dataverse un ir redzamas sadaļā Field Service.
- Ja ir instalēts tikai Field Service, nevis Supply Chain Management, kolonna **Noliktava** ir obligāta pirkšanas pasūtījumā. Tomēr, ja piegādes ķēdes pārvaldība ir instalēta, šī prasība ir atcelta, jo Supply Chain Management pieļauj pirkšanas pasūtījuma rindas, kur noteiktos gadījumos nav norādīta noliktava.
- Produktu ieejas plūsmas (pirkšanas pasūtījumu ieejas plūsmas Dataverse) pārvalda Supply Chain Management, un tās nevar izveidot Dataverse, ja ir instalēta Supply Chain Management. Produktu ieejas plūsmas no Supply Chain Management tiek sinhronizētas no Supply Chain Management uz Dataverse.
- Supply Chain Management ir atļauts veikt nesniegšanu. OneFSSCM risinājums pievieno loģiku, tādējādi, kad tiek izveidota vai atjaunināta produktu ieejas plūsmas rinda (vai pirkšanas pasūtījuma ieejas plūsmas prece Dataverse), tiek izveidota Dataverse krājumu žurnāla rinda, lai koriģētu atlikušo daudzumu, kas ir pasūtīts neproduktīgiem piegādes scenārijiem.

## <a name="unsupported-scenarios"></a>Neatbalstītie scenāriji

- Field Service neļauj rindas pievienot atceltam pirkšanas pasūtījumam Supply Chain Management. Kā risinājumu varat mainīt pirkšanas pasūtījuma sistēmas statusu Field Service un pēc tam pievienot jauno rindu sadaļā Field Service vai Supply Chain Management.
- Lai gan sagādes rindas ietekmē krājumu līmeņus abās sistēmās, šī integrācija nesniedz krājumu līdzinājumu Supply Chain Management un Field Service. Gan Field Service, gan Supply Chain Management ir citi procesi, kas atjaunina krājumu līmeņus. Šie procesi ir ārpus sagādes sfēras.

## <a name="status-management"></a>Statusa pārvaldība

Pirkšanas pasūtījumu statusi Field Service atšķiras no Supply Chain Management statusiem.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Field Service pirkšanas pasūtījuma un pirkšanas pasūtījuma preču statusi

| Galvene — sistēmas statuss | Galvene - Apstiprināšanas statuss | Krājuma statuss |
|---|---|---|
| <ul><li>Melnraksts</li><li>Iesniegti</li><li>Atcelta</li><li>Preces ieejas plūsma</li><li>Rēķins izrakstīts</li></ul> | <ul><li>Null</li><li>Apstiprināts</li><li>Noraidījis</li></ul> | <ul><li>Gaida</li><li>Saņemts</li><li>Atcelta</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Supply Chain Management pirkšanas pasūtījuma un pirkšanas pasūtījuma rindu statusi

Rindu apstiprināšanas statusi ir aktīvi tikai tad, ja ir rindas darbplūsma.

| Virsraksts — dokumentu statuss | Galvene - Apstiprināšanas statuss | Rindas statuss | Rindas apstiprināšanas statuss |
|---|---|---|---|
| <ul><li>Atvērts pasūtījums (neizpildīts pasūtījums)</li><li>Saņemts</li><li>Izveidots rēķins</li><li>Atcelta</li></ul> | <ul><li>Melnraksts</li><li>Pārskatīšanā</li><li>Apstiprināts</li><li>Noraidīts</li><li>Tiek pārskatīts ārēji</li><li>Apstiprināts</li><li>Pabeigtie</li></ul> | <ul><li>Atvērts pasūtījums (neizpildīts pasūtījums)</li><li>Saņemts</li><li>Izveidots rēķins</li><li>Atcelta</li></ul> | <ul><li>Nav iesniegts</li><li>Pārskatīšanā</li><li>Apstiprināts</li><li>Noraidījis</li></ul> |

Statusa kolonnām tiek pielietotas šādas kārtulas:

- Supply Chain Management statusu nevar atjaunināt no Field Service. Tomēr dažos gadījumos Field Service statuss tiks atjaunināts, mainoties pirkšanas pasūtījuma statusam Supply Chain Management.
- Ja Pirkšanas pasūtījums Supply Chain Management tiek mainīts un tiek apstrādātas izmaiņas, apstiprinājuma statuss ir *Melnraksts* vai *Tiek pārskatīts*. Šajā gadījumā Field Service apstiprinājuma statuss tiks iestatīts uz *Null*.
- Ja pirkšanas pasūtījuma apstiprinājuma statuss Supply Chain Management ir iestatīts uz *Apstiprināts*, *Ārēji pārskatīt*, *Apstiprināts* vai *Pabeigts*, Field Service pirkšanas pasūtījuma apstiprinājuma statuss tiks iestatīts uz *Apstiprināts*.
- Ja pirkšanas pasūtījuma apstiprinājuma statuss Supply Chain Management ir iestatīts uz *Noraidīts*, Field Service pirkšanas pasūtījuma apstiprinājuma statuss tiks iestatīts uz *Noraidīts*.
- Ja dokumenta virsraksta statuss Supply Chain Management ir mainīts uz *Atvērts pasūtījums (neizpildīts pasūtījums)* un Field Service pirkšanas pasūtījuma statuss ir *Melnraksts* vai *Atcelts*, Field Service pirkšanas pasūtījuma statuss tiks mainīts uz *Iesniegts*.
- Ja dokumentu virsraksta statuss Supply Chain Management tiek mainīts uz *Atcelts* un neviena pirkšanas pasūtījuma ieejas plūsmas preces Field Service nav saistītas ar pirkšanas pasūtījumu (izmantojot pirkšanas pasūtījuma preces), Field Service sistēmas statuss tiek iestatīts uz *Atcelts*.
- Ja pirkšanas pasūtījuma rindas statuss Supply Chain Management ir *Atcelts*, pirkšanas pasūtījuma preces statuss Field Service tiek iestatīts uz *Atcelts*. Turklāt, ja pirkšanas pasūtījuma rindas statuss Supply Chain Management ir mainīts no *Atcelts* uz *Neizpildīts pasūtījums*, pirkšanas pasūtījuma preces krājuma statuss Field Service tiek iestatīts uz *Gaida*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a> Sinhronizēt ar Supply Chain Management sagādes datiem pēc pieprasījuma

Supply Chain Management ietver sagādes datus, kas apstrādā tirdzniecības līgumus, atlaides un citus scenārijus, kas ir atkarīgi no Supply Chain Management sekundārajiem procesiem. Sagādes programma izmanto kompleksas kārtulas, lai noteiktu labāko cenu dotajam pirkšanas pasūtījumam. Ja izmantojat dubultās rakstīšanas, dati vienmēr netiek saglabāti sinhroni divās vidēs, it īpaši scenārijos, kuros rinda tika izveidota vai atjaunināta no Dataverse un var izraisīt sekojuma procesus Supply Chain Management.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Sinhronizēt sagādes datus ar Supply Chain Management

1. Dataverse dodieties uz **Krājumi \> Pirkšanas pasūtījums**.
2. Atlasiet **Jauns**, lai izveidotu jaunu pirkuma pasūtījumu vai atlasītu rindu esošam pirkuma pasūtījumam.
3. No pirkšanas pasūtījuma vai pirkšanas pasūtījuma rindas.
4. Darbību rūtī atlasiet **Sinhronizēt**.

Visas kolonnas no Dataverse un Field Service, ko koplieto Supply Chain Management, ir sinhronizētas.

Šeit ir situācijas, kurās var izmantot **Sinhronizēšanas** funkciju:

- Ja vienā rindā veicat vairākas secīgas Dataverse izmaiņas, izpildiet **Sinhronizēšanas** funkciju.
- Ja neesat pārliecināts, vai izmaiņa var būt otrā veiksmīgā izmaiņa Dataverse vidē, var būt nozīme palaist **Sync** funkciju.
- Ja saņemat kļūdas ziņojumu par vērtības atjaunināšanu no Supply Chain Management, palaidiet **Sinhronizēšanas** funkciju un pēc tam vēlreiz mēģiniet atjaunināt Dataverse vidē.

## <a name="cancelling-the-posting-process"></a>Grāmatošanas procesa atcelšana

Ja produktu ieejas plūsmas grāmatošanas process apstrādes laikā ir atcelts, duālā rakstīšana var izveidot produktu ieejas plūsmas rindu Dataverse vidē, taču ne izveidot produktu ieejas plūsmas rindu Supply Chain Management. Šāda situācija notiek, jo duālais ieraksts neatbalsta sadalītās darbības.

## <a name="templates"></a>Veidnes

Ar sagādes dokumentiem saistīto dokumentu integrāciju ir pieejamas šādas veidnes.

| Supply Chain Management | Field Service | Apraksts |
|---|---|---|
| [Pirkšanas pasūtījuma galvene V2](mapping-reference.md#183) | msdyn\_ Purchaseorders | Šajā tabulā ir kolonnas, kas atspoguļo pirkšanas pasūtījuma galveni. |
| [Pirkšanas pasūtījuma rindas elements](mapping-reference.md#181) | msdyn\_ PurchaseOrderProducts | Šajā tabulā ir rindas, kas atspoguļo pirkšanas pasūtījuma rindas. Preces numurs tiek izmantots sinhronizācijai. Tas identificē preci kā noliktavas vienību (NV), tostarp preces dimensijas. Informāciju par produktu integrāciju Dataverse vidē, skatiet sadaļā [Unificētā preču pieredze](product-mapping.md). |
| [Preces saņemšanas galvene](mapping-reference.md#185) | msdyn\_ purchaseorderreceipts | Šajā tabulā ir ietvertas produktu ieejas plūsmas galvenes kas tika izveidotas, kad produktu ieejas plūsma tiek grāmatota Supply Chain Management. |
| [Preces saņemšanas rinda](mapping-reference.md#184) | msdyn\_ purchaseorderreceiptproducts | Šajā tabulā ir ietverti produktu ieejas plūsmas rindas, kas tika izveidoti, kad produktu ieejas plūsma tiek grāmatota Supply Chain Management. |
| [Pirkšanas pasūtījuma rindas viegli dzēstā entītijā](mapping-reference.md#182) | msdyn\_ purchaseorderproducts | Šajā tabulā ir informācija par pirkšanas pasūtījuma rindām, kas ir viegli dzēstas. Pirkšanas pasūtījuma rindu Supply Chain Management var viegli dzēst tikai tad, kad pirkšanas pasūtījums ir apstiprināts vai apstiprināts, ja izmaiņu pārvaldība ir ieslēgta. Rinda pastāv Supply Chain Management datu bāzē un ir atzīmēta kā **IsDeleted**. Tā kā Dataverse videi nav vieglās dzēšanas koncepcijas, ir svarīgi, lai šī informācija tiktu sinhronizēta ar Dataverse. Šādā veidā rindas, kas ir viegli dzēstas Supply Chain Management, var automātiski izdzēst no Dataverse. Šajā gadījumā loģika rindas dzēšanai Dataverse vidē atrodas paplašinātajā Supply Chain Management versijā. |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
