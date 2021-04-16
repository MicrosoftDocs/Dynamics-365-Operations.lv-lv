---
title: Elektronisko pārskatu konfigurāciju pielāgošana, lai izveidotu elektronisku dokumentu
description: Šajā tēmā ir paskaidrots, kā pielāgot Microsoft nodrošināto elektronisko pārskatu (ER) konfigurācijas, ko izmanto, lai ģenerētu pielāgotu elektronisko dokumentu.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46b232da404fe2106ce4b5455ea4d682a08aaa53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743633"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Elektronisko pārskatu konfigurāciju pielāgošana, lai izveidotu elektronisku dokumentu

[!include[banner](../includes/banner.md)]

[Elektroniskā pārskata (ER) struktūra](general-electronic-reporting.md) ļauj augšupielādēt ER [konfigurācijas](general-electronic-reporting.md#Configuration), ko Microsoft nodrošina jūsu Microsoft Dynamics 365 Finance instancē. Tādējādi Microsoft nodrošinātās konfigurācijas var kalpot kā ER risinājums, kas tiek izmantots, lai ģenerētu elektroniskos debitoru rēķinus (e-rēķinus). Varat izmantot šo ER risinājumu sava pielāgotā ER risinājuma konfigurēšanai, lai piekļūtu jūsu pielāgotās datu bāzes laukiem un ģenerētu e-rēķinus, kas atbilst jūsu īpašajām prasībām, bez nepieciešamības rediģēt pirmkodu.

## <a name="overview"></a>Pārskats

Šīs tēmas piemērā ir jānorāda federālā nodokļa identifikācijas kods kā jauns pielāgots atribūts katram debitoram, kuram tiek elektroniski izrakstīts rēķins. Tāpēc ir jāpielāgo pašreiz izmantotā rēķina struktūra, pievienojot jaunu krājumu, kas jāaizpilda ar nodokļa kodu katrā ģenerētajā e-rēķinā.

Šīs tēmas procedūrās ir paskaidrots, kā lietotājs sistēmas administratora, elektronisko pārskatu izstrādātāja vai elektronisko pārskatu funkcionālā konsultanta lomā var veikt tālāk minētos uzdevumus jūsu Finance instancē:

- [Konfigurējiet minimālo ER parametru kopu, kas ir nepieciešama, lai sāktu izmantot ER struktūru](#ConfigureER).
- [Importējiet standarta ER konfigurāciju sākotnējās versijas, kas tiek nodrošinātas, lai ģenerētu e-rēķinus](#ImportERConfigurations1).
- [Konfigurēt debitoru parametrus, lai sāktu izmantot standarta ER konfigurācijas](#ConfigureAR1).
- [Konfigurēt juridisku personu parametrus rēķina debitoriem](#ConfigureLE).
- [Sagatavot debitora ierakstu elektroniskajai rēķinu izrakstīšanai](#ConfigureCustomer1).
- [Pievienot, grāmatot un sūtīt debitora rēķinu, izmantojot standarta ER konfigurācijas](#ProcessInvoice1).
- [Pievienot pielāgotu datu bāzes lauku, lai pārvaldītu federālā nodokļa identifikācijas kodu debitoriem](#AddCustomField).
- [Atsvaidzināt ER metadatus, lai iespējotu datu bāzu izmaiņas ER modeļu kartēšanas noformētājā](#RefreshERMetadata).
- [Noformēt pielāgotās ER konfigurācijas, lai ģenerētu e-rēķinus, kuros ir jaunais nodokļu kods](#DesignCustomERConfigurations).
- [Konfigurēt debitoru parametrus, lai sāktu izmantot paielāšgotas ER konfigurācijas](#ConfigureAR2).
- [Atjaunināt debitora ierakstu elektroniskajai rēķinu izrakstīšanai](#ConfigureCustomer2).
- [Pievienot, grāmatot un sūtīt debitora rēķinu, izmantojot pielāgotas ER konfigurācijas](#ProcessInvoice2).
- [Importēt standarta ER konfigurāciju jaunās versijas, kas tiek nodrošinātas, lai ģenerētu e-rēķinus](#ImportERConfigurations2).
- [Pieņemt izmaiņas standarta ER konfigurāciju jaunajās versijās jūsu pielāgotajās ER konfigurācijās](#RebaseCustomERConfigurations).
- [Pievienot, grāmatot un sūtīt debitora rēķinu, izmantojot pielāgoto ER konfigurāciju jaunās versijas](#ProcessInvoice3).

Visas šīs procedūras var veikt uzņēmumā **DEMF**.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>ER struktūras konfigurēšana

Kā lietotājam elektronisko pārskatu funkcionālā konsultanta vai elektronisko pārskatu izstrādātāja lomā jums ir jākonfigurē minimālais ER parametru kopums. Pēc tam varat sākt izmantot ER struktūru, lai izstrādātu ER risinājuma standarta konfigurāciju pielāgotas versijas, ko izmanto e-rēķinu ģenerēšanai.

### <a name="configure-er-parameters"></a>Konfigurējiet ER parametrus

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.
3. Lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi** iestatiet opciju **Iespējot noformēšanas režīmu** uz **Jā**.
4. Cilnes **Pielikumi** laukā **Konfigurācijas** atlasiet **Fails**.
5. Laukos **Darbu arhīvs**, **Pagaidu**, **Bāzlīnija** un **Citi** atlasiet veidu **Fails**.

Papildinformāciju par ER parametriem skatiet sadaļā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>ER konfigurācijas nodrošinātāja aktivizēšana

Katra pievienotā ER konfigurācija tiek atzīmēta kā piederoša ER konfigurācijas nodrošinātājam. Šim nolūkam tiek izmantots ER konfigurācijas nodrošinātājs, kas ir aktivizēts **Elektroniskie pārskati** darbvietā. Tāpēc, pirms sākat pievienot vai rediģēt ER konfigurācijas, jums ir jāaktivizē ER konfigurācijas nodrošinātājs **Elektroniskie pārskati** darbvietā.

> [!NOTE]
> Tikai ER konfigurācijas īpašnieks var to rediģēt. Tāpēc, pirms ER konfigurācija var tikt rediģēta, darbvietā **Elektroniskie pārskati** ir jāaktivizē atbilstošais ER konfigurācijas nodrošinātājs.

#### <a name="review-the-list-of-er-configuration-providers"></a>ER konfigurācijas nodrošinātāju saraksta pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
3. Lapā **Konfigurācijas nodrošinātāju tabula** katram nodrošinātāja ierakstam ir unikāls nosaukums un URL. Pārskatiet šīs lapas saturu. Ja ieraksts **Litware, Inc.** (`https://www.litware.com`) jau pastāv, izlaidiet nākamo procedūru, [Jauna ER konfigurācijas nodrošinātāja pievienošana](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Jauna ER konfigurācijas nodrošinātāja pievienošana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
3. Lapā **Konfigurācijas nodrošinātāji** atlasiet **Jauns**.
4. Laukā **Nosaukums** ievadiet **Litware, Inc.**
5. Laukā **Interneta adrese** ievadiet `https://www.litware.com`.
6. Atlasiet **Saglabāt**.

#### <a name="activate-an-er-configuration-provider"></a>ER konfigurācijas nodrošinātāja aktivizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.** un pēc tam atlasiet **Iestatīt kā aktīvu**.

Papildinformāciju par ER konfigurācijas nodrošinātājiem skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Sākotnējās standarta ER konfigurācijas versijas importēšana

Lai pievienotu standarta ER konfigurācijas savai pašreizējai Finance instancei, jums tās ir jāimportē no ER [repozitorija](general-electronic-reporting.md#Repository), kas konfigurēts šai instancei.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft** un pēc tam atlasiet **Repozitoriji**, lai skatītu Microsoft nodrošinātāja repozitoriju sarakstu.
3. Lapā **Konfigurācijas repozitoriji** atlasiet repozitoriju ar veidu **Globāls** un pēc tam atlasiet **Atvērt**. Ja tiek pieprasīta autorizācija savienojumam ar Regulatory Configuration Service, izpildiet autorizācijas norādījumus.
4. Lapā **Konfigurācijas repozitorijs** konfigurācijas koka skata kreisajā rūtī atlasiet **Peppol pārdošanas rēķina** formāta konfigurāciju.
5. Kopsavilkuma cilnē **Versijas** atlasiet versiju **11.2.2**.
6. Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija.

![Konfigurācijas repozitorijas lapa.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Ja rodas problēmas ar piekļuvi [globālajam repozitorijam](er-download-configurations-global-repo.md), tā vietā varat [lejupielādēt konfigurācijas](download-electronic-reporting-configuration-lcs.md) no Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a>Importēto ER konfigurāciju pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Lapā **Konfigurācijas** izvērsiet kopsavilkuma cilni **Konfigurācijas komponenti**.
4. Konfigurācijas koka kreisajā rūtī izvērsiet **Rēķina modelis** un pēc tam izvērsiet **UBL pārdošanas rēķins**.

Ņemiet vērā, ka papildus atlasītajam **Peppol pārdošanas rēķina** ER formātam tika importētas arī citas nepieciešamās ER konfigurācijas. Tā kā jaunās ER konfigurācijas versijas tiek pastāvīgi publicētas globālajā repozitorijā un LCS, lai saglabātu atbilstošos risinājumus, kas atbilst jaunajām prasībām, tika importētas nepieciešamās [datu modeļa](general-electronic-reporting.md#data-model-and-model-mapping-components) konfigurācijas jaunākās versijas un [modeļa kartēšanas](general-electronic-reporting.md#data-model-and-model-mapping-components) konfigurācijas.

![Lapa Konfigurācijas](./media/er-quick-start3-imported-solution1a.png)

Lai simulētu stāvokli, kādā būtu ER konfigurācijas pašreizējā Finance instancē, ja jūs iepriekš būtu importējis **Peppol pārdošanas rēķina** versiju **11.2.2** (piemēram, 2019. gada 7. augustā), izpildiet tālāk norādītās darbības.

- Darbības rūtī atlasiet **Dzēst**, lai dzēstu visas ER konfigurācijas, kas tika publicētas pēc 2019. gada 7. augusta. Ir jāatstāj vienīgi konfigurācijas **Rēķina modelis**, **Rēķina modeļa kartēšana** (sākotnēji nosaukta par **Debitora rēķina modeļa kartēšanu**), **UBL pārdošanas rēķins** un **Peppol pārdošanas rēķins**.
- Pārējām ER konfigurācijām kopsavilkuma cilnē **Versijas** atlasiet **Dzēst**, lai dzēstu visas ER konfigurāciju versijas, kas tika publicētas pēc 2019. gada 7. augusta.

Pēc tam pārliecinieties, vai konfigurācijas kokā ir pieejamas tālāk minētās konfigurācijas.

- **Rēķina modeļa** ER datu modeļa konfigurācija (sākotnēji nosaukta par **Debitora rēķina modeli**):

    - Versijā 11 iekļauta [datu modeļa](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponenta 10 versija , kas atspoguļo rēķinu izrakstīšanas biznesa domēna datu struktūru. Šī ER konfigurācija ir importēta kā **Peppol pārdošanas rēķina** ER formāta, kas tika atlasīts importēšanai, priekštece.
    - Versijā 50 ir ietverta datu modeļa ER komponenta versija 31. Šī ER konfigurācija ir importēta kā 2019. gada 7. augusta **Rēķina modeļa kartēšanas** ER modeļa kartēšanas konfigurācijas versija.

    ![Rēķina modeļa ER datu modeļa konfigurācija lapā Konfigurācijas](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Ja neredzat šī datu modeļa versiju 50, atveriet globālo repozitoriju un importējiet ER konfigurācijas **Rēķina modeļa kartēšana** versiju 50.19.

- **Rēķina modeļa kartēšana** ER datu modeļa kartēšanas konfigurācija (sākotnēji nosaukta par **Debitora rēķina modeļa kartēšanu**):

    - Versija 50.19 ir importēta kā pēdējā **Rēķina modeļa** ER datu modeļa konfigurācijas ieviešanas versija 50. Tajā ir divi [modeļu kartēšanas](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponenti, kas apraksta, kā datu modelis ir aizpildīts ar programmas datiem izpildlaikā.

    ![Rēķina modeļa kartēšanas ER datu modeļa kartēšanas konfigurācija lapā Konfigurācijas](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Ja neredzat šīs datu modeļa kartēšanas versiju 50.19, atveriet globālo repozitoriju un importējiet ER konfigurācijas **Rēķina modeļa kartēšana** versiju 50.19.

- **UBL pārdošanas rēķina** ER formāta konfigurācija:

    - Versija 11.2 ietver [formātu](general-electronic-reporting.md#FormatComponentOutbound) un formāta kartēšanas ER komponentus. Formāta komponents norāda atskaites izkārtojumu. Formāta kartēšanas komponents satur modeļa datu avotu un norāda, kā šis datu avots tiek izmantots, lai aizpildītu atskaites izkārtojumu izpildlaikā. Šis ER formāts tika konfigurēts, lai ģenerētu e-rēķinus universālās biznesa valodas (UBL) formātā. Tā tikaimportēta kā **Peppol pārdošanas rēķina** ER formāta, kas tika atlasīts importēšanai, vecākelements.

- **Peppol pārdošanas rēķina** ER formāta konfigurācija:

    - Versijā 11.2.2 ir ietverti formāta un formāta kartēšanas ER elementi, kas tika konfigurēti, lai ģenerētu e-rēķinus Viseiropas publisko iepirkumu tiešsaistes (PEPPOL) formātā.

    ![Peppol pārdošanas rēķina ER formāta konfigurācija lapā Konfigurācijas](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Debitoru parametru konfigurēšana

1. Dodieties uz **Debitori** \> **Iestatīšana** \> **Debitoru parametri**.
2. Cilnes **Elektroniskie dokumenti** kopsavilkuma cilnē **Elektroniskie pārskati** laukā **Pārdošanas un brīvā teksta rēķins** atlasiet **Peppol pārdošanas rēķins**.
3. Atlasiet **Saglabāt**.

![Elektronisko dokumentu cilne lapā Debitoru parametri](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Juridisko personu parametru konfigurēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Organizācijas** \> **Juridiskās personas**.
2. Atlasītajam uzņēmumam **DEMF** kopsavilkuma cilnes **Bankas konta informācija** laukā **Maršrutēšanas numurs** ievadiet **1234**.
3. Atlasiet **Saglabāt**.
4. Aizveriet lapu **Juridiskās personas**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Debitora ieraksa sagatavošana

1. Dodieties uz sadaļu **Debitori** \> **Klienti** \> **Visi klienti**.
2. Lapā **Visi klienti** atlasiet klienta konta saiti **DE-014**.

### <a name="add-a-customer-contact"></a>Klienta kontaktpersonas pievienošana

1. Dodieties uz sadaļu **Debitori** \> **Klienti** \> **Visi klienti**.
2. Darbību rūts cilnē **Klienti** grupā **Konti** atlasiet **Kontaktpersonas**.
3. Atlasiet **Pievienot kontaktpersonas**.
4. Lapā **Kontaktpersonas**, kas atrodas laukā **Vārds**, atveriet uzmeklēšanu, atlasiet **Adam Carter** un pēc tam atlasiet **Atlasīt**, lai aizvērtu uzmeklēšanu.
5. Atlasiet **Saglabāt**.
6. Aizveriet lapu **Kontaktpersonas**.

### <a name="define-a-primary-contact"></a>Primārās kontaktpersonas definēšana

1. Dodieties uz sadaļu **Debitori** \> **Klienti** \> **Visi klienti**.
2. Kopsavilkuma cilnes **Pārdošanas demogrāfija** laukā **Primārās kontaktpersonas** atlasiet **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>E-rēķina opcijas iestatīšana

1. Dodieties uz sadaļu **Debitori** \> **Klienti** \> **Visi klienti**.
2. Kopsavilkuma cilnē **Rēķins un piegāde** iestatiet opciju **eInvoice** uz **Jā**.
3. Atlasiet **Saglabāt**.
4. Aizveriet lapu **Visi debitori**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Apstrādāt debitora rēķinu, izmantojot standarta ER konfigurācijas

Tagad varat izmantot standarta ER konfigurācijas, kas tika importētas, lai elektroniski nosūtītu debitoram brīva teksta rēķinu.

### <a name="add-a-new-invoice"></a>Pievienojiet jaunu rēķinu

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Lapā **Brīvā teksts** atlasiet **Jauns**.
3. Kopsavilkuma cilnes **LBrīva teksta rēķina galvene** laukā **Debitora konts** atlasiet **DE-014**.
4. Kopsavilkuma cilnē **Rēķina rindas** tiek automātiski atjauninātas pievienotās rēķina rindas. Iestatiet šādas vērtības šiem laukiem:

    - Laukā **Apraksts** ievadiet **Piezīmjgrāmata**.
    - Laukā **Mans konts** atlasiet **401100**.
    - Laukā **Vienības cena** ievadiet **1000**.

5. Atlasiet **Saglabāt**.

![Brīva teksta rēķinu lapa](./media/er-quick-start3-add-invoice.png)

Plašāku informāciju skatiet sadaļā [Brība teksta rēķinu izveide](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Jauna rēķina grāmatošana

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Lapā **Brīvā teksta rēķins** darbību rūtī atlasiet **Grāmatot**.
3. Dialoglodziņā **Grāmatot brīva teksta rēķinu** atlasiet **Labi**.

![Detalizētas informācijas lapa par brīva teksta rēķinu](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Nosūtīt iegrāmatotu rēķinu

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Lapas **Brīvā teksta rēķins** darbību rūts grupā **Dokumenti** atlasiet **Sūtīt** \> **Oriģināls**.

    ![Oriģinālā rēķina priekšskatījums](./media/er-quick-start3-send-invoice.png)

3. Aizveriet lapu **Brīva teksta rēķins**.

### <a name="analyze-a-generated-e-invoice"></a>Ģenerētā e-rēķina analizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu veidošanas darbi**.
2. Lapā **Elektronisko pārskatu sniegšanas darbi** atlasiet sākotnējo ierakstu, kam ir uzdevuma apraksts **Sūtīt e-pasta XML**.
3. Atlasiet **Rādīt failus**, lai piekļūtu ģenerēto failu sarakstam.

    ![Elektronisko pārskatu darbu lapa](./media/er-quick-start3-jobs-list.png)

4. Atlasiet **Atvērt**, lai lejupielādētu elektronisko rēķinu XML failu, kas tiek ģenerēts.
5. Analizējiet e-rēķina XML failu. Ņemiet vērā, ka debitoru nodokļu shēma pašlaik tiek rādīta ar **schemeID** un **schemeAgencyID** XML atribūtiem. Ņemiet arī vērā, ka **CBC: CustomizationID** XML elementā pašlaik ir šāds teksts: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Ģenerētā e-rēķina XML faila priekšskatījums](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Pievienot pielāgotu datu bāzes lauku

Varat lietot [pielāgotu lauku](../../fin-ops/get-started/user-defined-fields.md), lai veiktu tālāk minēto pielāgošanu pašreizējā Finance instancē.

- Pielāgojiet datu bāzes struktūru, pievienojot jaunu pielāgotu datu bāzes lauku, kurā tiek glabāti katra debitora federālā nodokļa identifikācijas kods.
- Pielāgojiet lapu **Klienti**, pievienojot jaunu datu ievades lauku, ko var izmantot, lai ievadītu nodokļa koda vērtību laukā Jauna pielāgota datu bāze.

Izpildiet tālāk norādītās darbības, lai veiktu pielāgošanu.

1. Dodieties uz **Debitori** \> **Klienti** \> **Visi klienti**.
2. Lapā **Visi klienti** atlasiet klienta konta saiti **DE-014**.
3. Kopsavilkuma cilnē **Vispārīgi** ar peles labo pogu noklikšķiniet jebkurā tukšā apgabalā zem lauka **Valoda** un pēc tam atlasiet **Personalizēt: UpperGroup**.

    Kopsavilkuma cilnea **Vispārīgi** saturs tiek iezīmēta un tiek parādīta izvēlne **Personalizēt**.

4. Izvēlnē **Personalizēt** atlasiet **Pievienot lauku**.
5. Dialoglodziņā **Pievienot kolonnas** atlasiet **Izveidot jaunu lauku**.
6. Dialoglodziņa **Izveidot jaunu lauku** laukā **Tabulas nosaukums** atlasiet **Debitori**.
7. Laukā **Nosaukuma prefikss** ievadiet **FederalTaxID**.

    > [!NOTE]
    > Viss lauka nosaukums tiek automātiski definēts kā **FederalTaxID\_Pielāgots**.

8. Laukā **Etiķet** ievadiet **Federal Tax ID**.
9. Laukā **Veids** atlasiet **Teksts**.
10. Laukā **Garums** ievadiet **20**.
11. Atlasiet **Saglabāt**.
12. Parādītajā ziņojuma lodziņā atlasiet **Jā**, lai apstiprinātu, ka vēlaties izveidot jaunu **FederalTaxID** lauka ierakstu tabulai **Debitori**.
13. Atlasiet **Ievietot**, lai <a name="insert_custom_field"></a>pievienotu lauku **FederalTaxID\_Pielāgots** pašreizējai lapai.

    ![Lapa Visi debitori](./media/er-quick-start3-create-new-field.gif)

14. Aizveriet lapu **Visi debitori**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>Atsvaidzināt ER metadatus

Jums ir jāatsvaidzina ER metadati, lai izveidotu pielāgoto lauku, ko pievienojat [redzams](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) ER modeļu kartēšanas veidotājā.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Pārveidot tabulas atsauces**.
2. Dialoglodziņā **Atjaunināt datu modeli** atlasiet **Labi**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Pelāgoto ER konfigurāciju izstrāde

Varat izmantot Microsoft nodrošinātās ER konfigurācijas, lai prizsttrādātu jūsu pielāgotās ER konfigurācijas, veidojot e-rēķinus, kas ietver jauno nodokļu kodu.

### <a name="customize-the-data-model-configuration"></a>Datu modeļa konfigurācijas pielāgošana

Kā lietotājs elektronisko pārskatu funkcionālā konsultanta lomā jūs varat izveidot savu pielāgoto ER datu modeli.

#### <a name="add-a-custom-data-model-configuration"></a>Pievienot pielāgotu ER datu modeļa konfigurāciju

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī atlasiet **Debitora rēķina modelis**.
3. Darbību rūtī atlasiet **Izveidot konfigurāciju**.
4. Nolaižamā dialoglodziņa laukā **Jauns** atlasiet **Atvasināts no nosaukuma: debitora rēķina modelis, Microsoft**, lai norādītu, ka jūsu jaunajai muitas datu modeļa konfigurācijai ir jābalstās uz ER datu modeļa konfigurāciju.
5. Laukā **Nosaukums** ievadiet **Rēķina modelis (Litware)**.
6. Atlasiet **Izveidot konfigurāciju**, lai pievienotu jaunu ER konfigurāciju.

Varat izmantot ER datu modeļa izstrādātāju, lai rediģētu **Rēķina modeļa (Litware)** versijas 50.1 ER konfigurāciju **Melnrakstā** [statuss](general-electronic-reporting.md#component-versioning).

![ER konfigurācijas versija 50.1 Konfigurāciju lapā](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Pielāgota datu modeļa konfigurēšana

Lai pievienotu jaunu federālā nodokļa identifikācijas koda vērtību, ir jāmodificē pielāgots datu modelis, pievienojot jaunu lauku. Šis kods ir daļa no klienta datiem katram ER formātam, kas izmantos šo datu modeli kā datu avotu.

1. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī atlasiet **Rēķina modelis (Litware)**.
2. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER **50.1** formāta konfigurāciju sadaļā **Melnraksts**.
3. Darbību rūtī atlasiet **Izstrādātājs** atlasītajai konfigurācijas versijai.
4. Lapā **Datu modeļa izstrādātājs** datumodeļa kokā atlasiet **Debitora informācija (debitors)**.
5. Atlasiet **Jauns**.
6. Nolaižamajā dialoglodziņā laukā **Jauns mezgls kā** akceptējiet noklusējuma vērtību, **Aktīvā zara apakšelements**.
7. Laukā **Nosaukums** ievadiet **FederalTaxID\_Litware**.
8. Laukā **Preces veids** akceptējiet noklusējuma vērtību **Virkne**.
9. Atlasiet **Pievienot** un pēc tam atlasiet **Saglabāt**.

    ![ER datu modeļa veidotāja lapa](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > Laukos **Etiķete** un **Apraksts** tiek aprakstīts jaunā lauka nolūks. Šos laukus varat aizpildīt vairākās valodās. Papildinformāciju skatiet tēmā [Izstrādāt daudzvalodu atskaites ektronisko pārskatu veidošanā](er-design-multilingual-reports.md).

10. Aizveriet lapu **Datu modeļa noformētājs**.

#### <a name="complete-a-custom-data-model-configuration"></a>Pabiegt pielāgotu ER datu modeļa konfigurāciju

Jums ir [jāpabeidz](general-electronic-reporting.md#component-versioning) darbs ar jūsu pielāgotās ER datu modeļa konfigurācijas versiju 50.1, lai to padarītu pieejamu, lai varētu pievienot citas pielāgotus ER konfigurācijas.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modelis** un pēc tam atlasiet **Rēķina modelis (Litware)**.
3. Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** \> **Pabeigts** un pēc tam atlasiet **Labi**.

Versijas 50.1 statuss tiek mainīts no **Melnraksts** uz **Pabeigts** un versija kļūst tikai lasāma. Ir pievienota jauna rediģējama versija, 50.2, un tās statuss ir **Melnraksts**. Varat izmantot šo versiju, lai veiktu turpmākās izmaiņas pielāgotajā ER datu modeļa konfigurācijā.

![Versija 50.1 pabeigta lapā Konfigurācijas](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Kartēšanas modeļa konfigurācijas pielāgošana

Kā lietotājs elektronisko pārskatu izstrādāja lomā jūs varat izveidot savu pielāgoto ER modeļa kartēšanu.

#### <a name="add-a-custom-model-mapping-configuration"></a>Pievienot pielāgotumodeļa kartējuma konfigurāciju

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī izvērsiet **Debitora rēķina modelis** un pēc tam atlasiet **Debitora rēķina modeļa kartēšana**.
3. Darbību rūtī atlasiet **Izveidot konfigurāciju**.
4. Nolaižamā dialoglodziņa laukā **Jauns** atlasiet **Atvasināts no nosaukuma: debitora rēķina modeļa kartēšana, Microsoft**, lai norādītu, ka jūsu jaunajai muitas datu modeļa konfigurācijai ir jābalstās uz ER datu modeļa kartēšanas konfigurāciju.
5. Laukā **Nosaukums** ievadiet **Rēķina modeļa kartēšana (Litware)**.
6. Laukā **Mērķa modelis** atlasiet **Rēķina modelis (Litware)**.

    > [!IMPORTANT]
    > Šī darbība ir ļoti svarīga. Ja to izlaižat, jūs nevarēsit izmantot savu pielāgoto datu modeli konfigurētajā modeļu kartēšanā.

7. Atlasiet **Izveidot konfigurāciju**, lai pievienotu jaunu ER konfigurāciju.

![Pielāgotas modeļa kartēšanas pievienošana konfigurācija lapā Konfigurācijas](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Konfigurēt pielāgotu modeļa kartējumu

Jums ir jāmodificē pielāgotā modeļa kartēšana un jādefinē, kā pielāgotajam laukam **FederalTaxID\_Litware** jābūt aizpildītam ar programmas datiem izpildlaikā.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī izvērsiet **Debitora rēķina modelis** \> **CDebitora rēķina modeļa kartēšana** un atlasiet **Rēķina modeļa kartēšana (Litware)**.
3. Darbību rūtī atlasiet **Noformētājs**.
4. Lapā **Avota kartējuma modelis** atlasiet **Debitora rēķins**.

    ![Datu avota kartējuma modeļa lapa](./media/er-quick-start3-select-customer-mapping.png)

5. Atlasiet **Noformētājs**.
6. Lapā **Modeļa kartēšanas izstrādātājs** rūtī **Datu avoti** izvērsiet datu avotu **CustInvoiceJou**, kas pārstāv **CustInvoiceJour** pieteikumu tabulu.
7. Elementā **CustInvoiceJour** izvērsiet **Attiecības**, lai pārskatītu relāciju sarakstu no daudziem uz vienu (N:1) veidu tabulai **CustInvoiceJour**.
8. Sadaļā **CustInvoiceJour** \> **Attiecības** izvērsiet **Debitori (CustTable)**, lai piekļūtu laukiem un attiecībām tabulā **Debitori (CustTable)**.
9. Atlasiet datu avota lauku **FederalTaxID\_Custom**, ko esat ieviesis [iepriekš](#insert_custom_field).
10. Rūtī **Datu modelis** izvērsiet **Debitora informācija (Debitors)** un atlasiet datu modeļa lauku **FederalTaxID\_Litware**.
11. Atlasiet **Saistīt**.

    ![Modeļu kartēšanas veidotāja lapa](./media/er-quick-start3-customize-model-mapping.gif)

12. Atlasiet **Saglabāt**.
13. Aizveriet lapu **Modeļa kartējuma noformētājs**.
14. Aizveriet lapu **Datu avota kartējuma modelis**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Pabiegt pielāgotu ER modeļa kartēšanas konfigurāciju

Jums ir [jāpabeidz](general-electronic-reporting.md#component-versioning) darbs ar jūsu pielāgotās ER modeļa kartēšanas konfigurācijas versiju 50.19.1, lai to padarītu pieejamu lietošanai.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī izvērsiet **Debitora rēķina modelis** \> **CDebitora rēķina modeļa kartēšana** un atlasiet **Rēķina modeļa kartēšana (Litware)**.
3. Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** \> **Pabeigts** un pēc tam atlasiet **Labi**.

Versijas 50.19.1 statuss tiek mainīts no **Melnraksts** uz **Pabeigts** un versija kļūst tikai lasāma. Ir pievienota jauna rediģējama versija, 50.19.2, un tās statuss ir **Melnraksts**. Varat izmantot šo versiju, lai veiktu turpmākās izmaiņas pielāgotajā ER modeļa kartēšanas konfigurācijā.

![Versija 50.19.1 pabeigta lapā Konfigurācijas](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Atbalstītais konfigurācijas [dzīves cikls](general-electronic-reporting-manage-configuration-lifecycle.md) nesedz datu bāzes izmaiņu dzīves ciklu. Ja eksportējat **Rēķina modeļa kartēšanas (Litware)** konfigurācijas versiju 50.19.1 no pašreizējās Finance instances un mēģināt importēt to citā instancē, kurā nav ietverts pielāgots lauks **FederalTaxID\_Custom**, tabulā **CustTable** radīsies izņēmums. Izņēmums norāda, ka importētā ER konfigurācija nav saderīga ar mērķa Finance instances metadatiem.

### <a name="customize-the-format-configuration"></a>Formāta pielāgošanas konfigurācija

Kā lietotājs elektronisko pārskatu funkcionālā konsultanta lomā jūs varat izveidot savu pielāgoto ER formātu.

#### <a name="add-a-custom-format-configuration"></a>Pielāgotas formāta konfigurācijas pievienošana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī izvērsiet **Debitora rēķina modelis** \> **UBL pārdošanas rēķins** un atlasiet **Peppol pārdošanas rēķins**.
3. Darbību rūtī atlasiet **Izveidot konfigurāciju**.
4. Nolaižamā dialoglodziņa laukā **Jauns** atlasiet **Atvasināts no nosaukuma: Peppol pārdošanas rēķins, Microsoft**, lai norādītu, ka jūsu jaunajai muitas datu modeļa konfigurācijai ir jābalstās uz ER formāta konfigurāciju.
5. Laukā **Nosaukums** ievadiet **Peppol pārdošanas rēķins (Litware)**.
6. Laukā **Datu modelis** atlasiet **Rēķina modelis (Litware)**, lai izmantotu jūsu pielāgoto datu modeli un modeļa kartēšanas komponentus.

    > [!NOTE]
    > Šī darbība ir ļoti svarīga. Ja to izlaižat, jūs nevarēsit izmantot savu pielāgoto datu modeli konfigurētajā formātā.

7. Laukā **Datu modeļlis** atlasiet saknes definīciju **InvoiceCustomer**.
8. Atlasiet **Izveidot konfigurāciju**, lai pievienotu jaunu ER konfigurāciju.

![Pielāgota formāta pievienošana konfigurācija lapā Konfigurācijas](./media/er-quick-start3-adding-custom-format.png)

Tagad varat izmantot ER operācijua izstrādātāju, lai rediģētu **Peppol pārdošanas rēķinu (Litware)** versijas 11.2.2.1 ER konfigurāciju **Melnrakstā** [statuss](general-electronic-reporting.md#component-versioning).

![ER konfigurācijas versija 11.2.2.1 Konfigurāciju lapā](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Pielāgota formāta konfigurēšana

Jums ir jāmodificē pielāgotais formāts, pievienojot jaunu formāta elementu, lai aizpildītu rēķinā iekļaujamā debitora federālā nodokļa identifikācijas koda vērtību.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī izvērsiet **Debitora rēķina modelis** \> **UBL pārdošanas rēķins** \> **Peppol pārdošanas rēķins** un atlasiet **Peppol pārdošanas rēķins (Litware)**.
3. Darbību rūtī atlasiet **Noformētājs**.
4. Formāta kokā izvērsiet **XMLHeader** \> **Rēķins** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** un atlasiet **cbc:ID**.
5. Atlasiet **Pievienot** un pēc tam atlasiet **XML** \> **Atribūts**.
6. Dialoglodziņā **Komponenta rekvizīts** laukā **Nosaukums** ievadiet **FederalTaxID**.
7. Atlasiet **Labi**, lai pievienotu jauna formāta elementu, lai izveidotu jaunu **FederalTaxID** XML atribūtu ģenerētajā XML failā.
8. Formāta kokā zem **XMLHeader** \> **Rēķins** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** atlasiet **FederalTaxID**.
9. Atlasiet **Pārvietot uz augšu**.

![Jauna formāta elements lapā Formāta veidotājs](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Konfigurēt pielāgotu formāta kartējumu

1. Lapas **Formāta veidotājs** cilnē **Kartēšana** izvērsiet veida **Modelis** datu avotu **Rēķins**.
2. Sadaļā **Rēķins** izvērsiet **Debitora informācija (debitors)** un atlasiet **FederalTaxID\_litware**.
3. Atlasiet **Saistīt**.

    ![Formāta veidotāja lapa](./media/er-quick-start3-customized-format-mapping.png)

4. Atlasiet veida **Modelis** datu avotu **Rēķins** un pēc tam atlasiet **Rediģēt**.
5. Laukā **Versija** atlasiet pielāgotā datu modeļa versiju **1** un pēc tam atlasiet **Labi**.
6. Atlasiet **Saglabāt**.
7. Aizveriet lapu **Formāta veidotājs**.

#### <a name="complete-a-custom-format-configuration"></a>Pielāgotas formāta konfigurācijas pabeigšana

Jums ir [jāpabeidz](general-electronic-reporting.md#component-versioning) darbs ar jūsu pielāgotās ER formāta konfigurācijas versiju 11.2.2.1, lai to padarītu pieejamu lietošanai.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī izvērsiet **Debitora rēķina modelis** \> **UBL pārdošanas rēķins** \> **Peppol pārdošanas rēķins** un atlasiet **Peppol pārdošanas rēķins (Litware)**.
3. Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** \> **Pabeigts** un pēc tam atlasiet **Labi**.

Versijas 11.2.2.1 statuss tiek mainīts no **Melnraksts** uz **Pabeigts** un versija kļūst tikai lasāma. Ir pievienota jauna rediģējama versija, 11.2.2.2, un tās statuss ir **Melnraksts**. Varat izmantot šo versiju, lai veiktu turpmākās izmaiņas pielāgotajā ER formāta konfigurācijā.

![Versija 11.2.2.1 pabeigta lapā Konfigurācijas](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Konfigurēt debitoru parametrus, lai sāktu izmantot pielāgotas ER konfigurācijas

1. Dodieties uz **Debitori** \> **Iestatīšana** \> **Debitoru parametri**.
2. Cilnes **Elektroniskie dokumenti** kopsavilkuma cilnē **Elektroniskie pārskati** laukā **Pārdošanas un brīvā teksta rēķins** atlasiet **Peppol pārdošanas rēķins (Litware)**.
3. Atlasiet **Saglabāt**.

![Lapa Debitoru parametri, Elektronisko dokumentu cilne, kopsavilkuma cilne Elektroniskie pārskati](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Atjaunināt debitora ierakstu, pievienojot federālā nodokļa identifikācijas kodu

1. Dodieties uz sadaļu **Debitori** \> **Klienti** \> **Visi klienti**.
2. Lapā **Visi klienti** atlasiet klienta konta saiti **DE-014**.
3. Kopsavilkuma cilnē **Vispārīgi** laukā **Federālā nodokļa ID** ievadiet **LITWARE-6789**.
4. Atlasiet **Saglabāt**.

    ![Lapa Detalizēta informācija par DE-014 debitoru](./media/er-quick-start3-added-tax-id-value.png)

5. Aizveriet lapu **Visi debitori**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Apstrādāt debitora rēķinu, izmantojot pielāgotas ER konfigurācijas

### <a name="select-and-send-a-posted-invoice"></a>Atlasiet un nosūtiet iegrāmatotu rēķinu

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Lapā **Brīvā teksta rēķins** atlasiet rēķinu, ko iepriekš pievienojāt un iegrāmatojāt.
3. Darbības rūtī, kas atrodas grupā **Dokumenti** atlasiet **Sūtīt** \> **Oriģināls**.
4. Aizveriet lapu **Brīva teksta rēķins**.

### <a name="analyze-a-generated-e-invoice"></a>Ģenerētā e-rēķina analizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu veidošanas darbi**.
2. Lapā **Elektronisko pārskatu sniegšanas darbi** atlasiet pēdējo ierakstu, kam ir uzdevuma apraksts **Sūtīt e-pasta XML**.
3. Atlasiet **Rādīt failus**, lai piekļūtu ģenerēto failu sarakstam.
4. Atlasiet **Atvērt**, lai lejupielādētu elektronisko rēķinu XML failu, kas tiek ģenerēts.
5. Analizējiet e-rēķina XML failu. Ņemiet vērā, ka atbilstoši jūsu pielāgošanai debitora nodokļu shēma ietver pielāgoto **FederalTaxID** XML atribūtu papildus **schemeID** un **schemeAgencyID** XML atribūtiem. Šī jaunā XML atribūta vērtība ir norādīta ar **LITWARE-6789** federālā nodokļa ID, kas tika ievadīts rēķinā iekļautajam debitoram.

    ![Ģenerētā e-rēķina XML faila priekšskatījums ar jūsu pielāgojumiem](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Jaunākās standarta ER konfigurācijas versijas importēšana

Lai saglabātu standarta ER konfigurāciju kopumu jūsu finanšu instancē [atjauninātu](general-electronic-reporting-manage-configuration-lifecycle.md), jums jāimportē jaunas versijas, kad tās ir pieejamas ER [repozitorijā](general-electronic-reporting.md#Repository), kurš tika konfigurēta šai instancei.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft** un pēc tam atlasiet **Repozitoriji**, lai skatītu Microsoft nodrošinātāja repozitoriju sarakstu.
3. Lapā **Konfigurācijas repozitoriji** atlasiet repozitoriju ar veidu **Globāls** un pēc tam atlasiet **Atvērt**. Ja tiek pieprasīta autorizācija savienojumam ar Regulatory Configuration Service, izpildiet autorizācijas norādījumus.
4. Lapā **Konfigurācijas repozitorijs** konfigurācijas koka skata kreisajā rūtī atlasiet **Peppol pārdošanas rēķina** formāta konfigurāciju.
5. Kopsavilkuma cilnē **Versijas** atlasiet atlasītās er formāta konfigurācijas versiju **32.6.7**, kas tika izlaista, lai atbalstītu debitoru elektroniskos rēķinus PEPPOL BIS 3 formātā. Lai iegūtu papildinformāciju, skatiet [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija uz pašreizējo Finance instanci.

![Versija 32.6.7, kas atlasīta lapā Konfigurāciju repozitorijs](./media/er-quick-start3-import-solution2.png)

Lai iegūtu informāciju par to, kā šo procesu var automatizēt, skatiet sadaļu [Atjaunināto ER konfigurāciju versiju importēšana](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Importēto ER konfigurāciju pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Izvērsiet kopsavilkuma cilni **Konfigurācijas komponenti**.
4. Konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modelis**. Ņemiet vērā, ka **Debitora rēķina modeļa** nosaukums ir mainīts uz **Rēķina modelis** vienā no importētajām ER datu modeļu konfigurācijām.
5. Konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modeļa kartēšana**. Ņemiet vērā, ka **Debitora rēķina modeļa kartēšanas** nosaukums ir mainīts uz **Rēķina modeļa kartēšana** vienā no importētajām ER datu modeļa kartēšanas konfigurācijām.
6. Izvērsiet **UBL pārdošanas rēķins** \> **Peppol pārdošanas rēķins**.

Ņemiet vērā, ka papildus atlasītajam **Peppol pārdošanas rēķina** ER formātam tika importētas arī citas nepieciešamās ER konfigurācijas jaunākās versijas. Tā kā jaunās ER konfigurācijas versijas tiek pastāvīgi publicētas globālajā repozitorijā un LCS, lai saglabātu atbilstošos ER risinājumus, kas atbilst jaunajām prasībām, tika importētas nepieciešamās datu modeļa konfigurācijas jaunākās versijas un modeļa kartēšanas konfigurācijas.

Pārliecinieties, vai konfigurācijas kokā ir galīgi pieejamas šādas ER konfigurācijas:

- **Rēķina modeļa** ER datu modeļa konfigurācija:

    - Versijā 206 (vai jaunākā) iekļauta datu modeļa ER komponenta 24 versija (vai jaunāka), kas atspoguļo rēķinu izrakstīšanas biznesa domēna datu struktūru. Šī ER konfigurācija ir importēta kā jaunākās pieejamās **Rēķina modeļa kartēšanas** ER modeļa kartēšanas konfigurācijas versijas priekštece.

    ![Versija 206 lapā Konfigurācijas](./media/er-quick-start3-imported-solution2b1.png)

- **Rēķina modeļa kartēšanas** ER datu modeļa kartēšanas konfigurācija:

    - Versija 206.132 (vai jaunāka) ir importēta kā pēdējā **Rēķina modeļa** ER datu modeļa konfigurācijas ieviešanas versija 206. Tajā ir vairāki modeļu kartēšanas ER komponenti, kas apraksta, kā datu modelis ir aizpildīts ar programmas datiem izpildlaikā.

    ![Versija 206.132 lapā Konfigurācijas](./media/er-quick-start3-imported-solution2b2.png)

- **UBL pārdošanas rēķina** ER formāta konfigurācija:

    - Versija 32.6 ietver formātu un formāta kartēšanas ER komponentus. Formāta komponents norāda atskaites izkārtojumu. Formāta kartēšanas komponents satur modeļa datu avotu un norāda, kā šis datu avots tiek izmantots, lai aizpildītu atskaites izkārtojumu izpildlaikā. Šis ER formāts tika konfigurēts, lai ģenerētu e-rēķinus UBL formātā. Tā tikaimportēta kā **Peppol pārdošanas rēķina** ER formāta, kas tika atlasīts importēšanai, vecākelements.

- **Peppol pārdošanas rēķina** ER formāta konfigurācija:

    - Versijā 32.6.7 ir ietverti formāta un formāta kartēšanas ER elementi, kas tika konfigurēti, lai ģenerētu e-rēķinus PEPPOL formātā.

    ![Versija 32.6.7 lapā Konfigurācijas](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Pieņemt izmaiņas standarta ER konfigurāciju jaunajās versijās jūsu pielāgotajās ER konfigurācijās

### <a name="adopt-your-custom-er-data-model"></a>Jūsu pielāgotā ER datu modeļa pieņemšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modelis** un pēc tam atlasiet **Rēķina modelis (Litware)**.
3. Kopsavilkuma cilnē **Versijas** atlasītās datu modeļa konfigurācijas melnraksta versijai **50.2** atlasiet **Pārveidot**.
4. Laukā **Mērķa versija** apstipriniet pamata ER datu modeļa konfigurācijas versijas **206** atlasi un pēc tam atlasiet **Labi**.

    Jūsu pielāgotās ER datu modeļa konfigurācijas melnraksta versija tiek pārnumurēta no **50.2** uz **206.2**, lai norādītu, ka tagad tā ietver jūsu pielāgojumu, kas tika sapludināts ar izmaiņām pamata ER datu modeļa konfigurācijas jaunākajā versijā (206).

    > [!NOTE]
    > Pārveides darbība ir atgriezeniska. Lai atceltu pārveidi, atlasiet modeļa **Rēķina modelis (Litware)** versiju **50.1** kopsavilkuma cilnē **Versijas** un pēc tam atlasiet **Iegūt šo versiju**. Versija 206.2 tiks pārnumurēta atpakaļ uz **50.2** un melnraksta versijas 50.2 saturs atbildīs versijas 50.1 saturam.

5. Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** \> **Pabeigts** un pēc tam atlasiet **Labi**.

Versijas 206.2 statuss tiek mainīts no **Melnraksts** uz **Pabeigts** un versija kļūst tikai lasāma. Ir pievienota jauna rediģējama versija, 206.3, un tās statuss ir **Melnraksts**. Varat izmantot šo versiju, lai veiktu turpmākās izmaiņas pielāgotajā ER datu modeļa konfigurācijā.

![Versija 206.2 pabeigta lapā Konfigurācijas](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Jūsu pielāgotā ER modeļa kartēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modelis** \> **Rēķina modeļa kartēšana** un atlasiet **Rēķina modeļa kartēšana (Litware)**.
3. Kopsavilkuma cilnē **Versijas** atlasītās modeļa kartēšanas konfigurācijas melnraksta versijai **50.19.2** atlasiet **Pārveidot**.
4. Laukā **Mērķa versija** apstipriniet pamata ER modeļa kartēšanas konfigurācijas versijas **206.132** atlasi un pēc tam atlasiet **Labi**.

    Jūsu pielāgotās ER modeļa kartēšanas konfigurācijas melnraksta versija tiek pārnumurēta no **50.19.2** uz **206.132.2**, lai norādītu, ka tagad tā ietver jūsu pielāgojumu, kas tika sapludināts ar izmaiņām pamata ER modeļa kartēšanas konfigurācijas jaunākajā versijā (206.132).

    Ņemiet vērā, ka tika atklāti daži pārveides konflikti. Tagad jums ir manuāli jāatrisina šie konflikti.

    ![Konflikta ziņojuma pārveide lapā Konfigurācijas](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Darbības rūtī atlasiet **Veidotājs** un pēc tam kartēšanu sarakstā atlasiet **Debitora rēķins**.
6. Katram pārveides konfliktam atlasiet **Saglabāt savu vērtību**, jo jums ir jāpatur sava pielāgotā datu modeļa versijas numurs katram komponentam, kas ir minēts.

    ![Pārveidot konfliktus Modeļu kartēšanas veidotāja lapā](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Atlasiet **Saglabāt** un pēc tam aizvēriet lapu **Modeļa kartēšanas veidotājs**.
8. Kartēšanas sarakstā atlasiet **Projekta rēķins**.
9. Katram pārveides konfliktam atlasiet **Saglabāt savu vērtību**, jo jums ir jāpatur sava pielāgotā datu modeļa versijas numurs katram komponentam, kas ir minēts.
10. Atlasiet **Saglabāt** un pēc tam aizvēriet lapu **Modeļa kartēšanas**.

    > [!NOTE]
    > Pārveides darbība ir atgriezeniska. Lai atceltu pārveidi, atlasiet modeļa **Rēķina modeļa kartēšana (Litware)** versiju **50.19.1** modeļa kartēšanas kopsavilkuma cilnē **Versijas** un pēc tam atlasiet **Iegūt šo versiju**. Versija 206.132.2 tiks pārnumurēta atpakaļ uz **50.19.2** un melnraksta versijas 50.19.2 saturs atbildīs versijas 50.19.1 saturam.

11. Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** \> **Pabeigts** un pēc tam atlasiet **Labi**.

Versijas 206.132.2 statuss tiek mainīts no **Melnraksts** uz **Pabeigts** un versija kļūst tikai lasāma. Ir pievienota jauna rediģējama versija, 206.132.3, un tās statuss ir **Melnraksts**. Varat izmantot šo versiju, lai veiktu turpmākās izmaiņas pielāgotajā ER modeļa kartēšanas konfigurācijā.

![Versija 206.132.2 pabeigta lapā Konfigurācijas](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Pieņemt jūsu pielāgoto ER formātu

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modelis** \> **UBL pārdošanas rēķins** \> **Peppol pārdošanas rēķins** un atlasiet **Peppol pārdošanas rēķins (Litware)**.
3. Kopsavilkuma cilnē **Versijas** atlasītās formāta konfigurācijas melnraksta versijai **11.2.2.2** atlasiet **Pārveidot**.
4. Versijas laukā **Mērķis** apstipriniet pamata ER formāta konfigurācijas versijas **32.6.7** atlasi un pēc tam atlasiet **Labi**.

    Jūsu pielāgotās ER formāta konfigurācijas melnraksta versija tiek pārnumurēta no **11.2.2.2** uz **32.6.7.2**, lai norādītu, ka tagad tā ietver jūsu pielāgojumu, kas tika sapludināts ar izmaiņām pamata ER formāta konfigurācijas jaunākajā versijā (32.6.7).

    Ņemiet vērā, ka tika atklāti daži pārveides konflikti. Tagad jums ir manuāli jāatrisina šie konflikti.

5. Darbību rūtī atlasiet **Noformētājs**.
6. Katram pārveides konfliktam atlasiet **Saglabāt savu vērtību**, jo jums ir jāpatur sava pielāgotā datu modeļa versijas numurs katram komponentam, kas ir minēts.
7. Atlasiet **Saglabāt**.
8. Cilnē **Kartēšana** atlasiet veida **Modelis** datu avotu **Rēķins** un pēc tam atlasiet **Rediģēt**.
9. Laukā **Versija** atlasiet pielāgotā datu modeļa versiju **2** un pēc tam atlasiet **Labi**.
10. Atlasiet **Saglabāt**.

    > [!NOTE]
    > Pārveides darbība ir atgriezeniska. Lai atceltu pārveidi, atlasiet modeļa **Peppol pārdošanas rēķins (Litware)** formāta versiju **11.2.2.1** kopsavilkuma cilnē **Versijas** un pēc tam atlasiet **Iegūt šo versiju**. Versija 32.6.7.2 tiks pārnumurēta atpakaļ uz **11.2.2.2** un melnraksta versijas 11.2.2.2 saturs atbildīs versijas 11.2.2.1 saturam.

11. Aizveriet lapu **Formāta veidotājs**.
12. Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** \> **Pabeigts** un pēc tam atlasiet **Labi**.

Versijas 32.6.7.2 statuss tiek mainīts no **Melnraksts** uz **Pabeigts** un versija kļūst tikai lasāma. Ir pievienota jauna rediģējama versija, 32.6.7.3, un tās statuss ir **Melnraksts**. Varat izmantot šo versiju, lai veiktu turpmākās izmaiņas pielāgotajā ER formāta konfigurācijā.

![Versija 32.6.7.2 pabeigta lapā Konfigurācijas](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Apstrādāt debitora rēķinu, izmantojot pielāgoto ER konfigurāciju jaunās versijas

### <a name="select-and-send-a-posted-invoice"></a>Atlasiet un nosūtiet iegrāmatotu rēķinu

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Lapā **Brīvā teksta rēķins** atlasiet rēķinu, ko iepriekš pievienojāt un iegrāmatojāt.
3. Darbības rūtī, kas atrodas grupā **Dokumenti** atlasiet **Sūtīt** \> **Oriģināls**.

    > [!NOTE] 
    > Tā kā jums tagad ir divas **Peppol pārdošanas rēķina (litware)** ER formāta konfigurācijas versijas un nevienai versijai nav [spēkā esošā datuma](general-electronic-reporting.md#component-date-effectivity) vērtības, e-rēķina ģenerēšanai tiek izmantota jaunākā versija.

4. Aizveriet lapu **Brīva teksta rēķins**.

### <a name="analyze-a-generated-e-invoice"></a>Ģenerētā e-rēķina analizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu veidošanas darbi**.
2. Lapā **Elektronisko pārskatu sniegšanas darbi** atlasiet jaunāko ierakstu, kam ir uzdevuma apraksts **Sūtīt e-pasta XML**.
3. Atlasiet **Rādīt failus**, lai piekļūtu ģenerēto failu sarakstam.
4. Atlasiet **Atvērt**, lai lejupielādētu elektronisko rēķinu XML failu, kas tiek ģenerēts.
5. Analizējiet e-rēķina XML failu. Ņemiet vērā, ka atbilstoši jūsu pielāgošanai debitora nodokļu shēma joprojām ietver pielāgoto **FederalTaxID** XML atribūtu papildus **schemeID** un **schemeAgencyID** XML atribūtiem. Turklāt, tā kā izmaiņas jaunajā bāzes **UBL pārdošanas rēķins** formāta versijā tika sapludinātas ar jūsu pielāgojumu, **CBC: CustomizationID** XML elementa teksts ir mainīts no `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` uz `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Ģenerētā e-rēķina XML faila priekšskatījums ar pielāgojumiem](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [ER konfigurāciju lejupielāde no Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [ER konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](er-download-configurations-global-repo.md)
- [Izveidot brīva teksta rēķinu](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new)
- [Pielāgotu lauku izveide un darbs ar tiem](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]