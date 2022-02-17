---
title: Importējiet datus no manuāli atlasītajiem failiem pakešu režīmā
description: Šajā tēmā ir paskaidrots, kā importēt datus no manuāli atlasītajiem failiem pakešu režīmā.
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 8615b5a0623fd696c64f4ec03e481a2bcb16c0ac
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075748"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Importējiet datus no manuāli atlasītajiem failiem pakešu režīmā

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Lai izmantotu [Elektroniskā ziņošana (ER)](general-electronic-reporting.md) sistēmu, lai importētu datus no manuāli atlasītiem ienākošajiem failiem pakešu režīmā, konfigurējiet ER [formātā](er-overview-components.md#format-component) kas atbalsta importēšanu. Pēc tam palaidiet a [modeļu kartēšana](er-overview-components.md#model-mapping-component) no **Uz galamērķi** veids, kas izmanto šo formātu kā datu avotu. Lai importētu datus, pārlūkojiet līdz failam, kuru vēlaties importēt, un manuāli atlasiet to. 

Jaunā ER iespēja, kas atbalsta datu importēšanu pakešu režīmā, ļauj konfigurēt šo procesu kā bez uzraudzības. Varat izmantot ER konfigurācijas, lai veiktu datu importēšanu, ieplānojot jaunu pakešu darbu no ER lietotāja interfeisa (UI).

Šajā tēmā ir paskaidrots, kā pabeigt datu importēšanu no manuāli atlasīta faila pakešu režīmā. Piemēros kā biznesa dati tiek izmantotas kreditoru transakcijas. Šo piemēru darbības var pabeigt **USMF** uzņēmums. Kodēšana nav nepieciešama.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai izpildītu šajā tēmā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.

- Viena no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- ER formāta un modeļa konfigurācijas 1099 maksājumiem

### <a name="create-the-required-er-configurations"></a>Izveidojiet nepieciešamās ER konfigurācijas

Lai izveidotu nepieciešamās ER konfigurācijas un iegūtu citus priekšnoteikumus, veiciet vienu no šīm darbībām:

- Noskatieties uzdevumu ceļvežus **ER: datu importēšana no Microsoft Excel faila**, kas ir ietverti biznesa procesā **7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**. Šajās uzdevumu rokasgrāmatās ir izskaidrots ER konfigurāciju izstrādes un izmantošanas process, kas interaktīvi importē piegādātāja darījumus no Microsoft Excel failus. Plašāku informāciju skatiet tēmā [Ienākošo dokumentu parsēšana programmā Excel formātā](parse-incoming-documents-excel.md).
- Pabeidziet piemērus [Konfigurējiet datu importēšanu no SharePoint](er-configure-data-import-sharepoint.md). Šie piemēri izskaidro ER konfigurāciju izstrādes un izmantošanas procesu, kas interaktīvi importē piegādātāja transakcijas no Excel failiem, kas tiek glabāti SharePoint mapi.

### <a name="download-the-required-er-configurations"></a>Lejupielādējiet nepieciešamās ER konfigurācijas

1. Lejupielādējiet tālāk norādītās ER konfigurācijas un saglabājiet tās lokāli.

    | Satura apraksts | Fails |
    |---------------------|------|
    | **1099 Maksājumu modelis** ER datu modeļa konfigurācija | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Pārdevēju darījumu importēšanai (Excel)** ER formāta konfigurācija | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Izmantojiet [Ielādēt no XML faila](er-defer-sequence-element.md#import-the-sample-er-configurations) ER opcija, lai importētu lejupielādētās ER konfigurācijas savā instancē Dynamics 365 Finance šādā secībā:

    1. ER datu modeļa konfigurācija
    2. ER formāta konfigurācija

### <a name="download-the-required-excel-files"></a>Lejupielādējiet nepieciešamos Excel failus

- Lejupielādējiet tālāk norādīto datu kopas paraugu un saglabājiet to lokāli.

    | Satura apraksts | Fails |
    |---------------------|------|
    | Ienākošais **1099import-data.xlsx** failu, kurā ir datu paraugi importēšanai | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Pārskatiet priekšnoteikumus

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Uz **Konfigurācijas** lapā, pārskatiet sagatavoto ER risinājumu datu importēšanai pakešu režīmā.
3. Pārskatiet **Pārdevēju darījumu importēšanai (Excel)** formāta konfigurācija.

    - Šīs konfigurācijas formāta komponents ir paredzēts ienākoša Excel faila parsēšanai.
    - Šīs konfigurācijas modeļa kartēšanas komponents tiek izmantots, lai aizpildītu bāzes datu modeli, izmantojot datus no parsētā Excel faila.

    ![ER formāta konfigurācija datu importēšanai pakešu režīmā no ER lietotāja saskarnes.](./media/er-configure-data-import-batch-configurations-1.png)

4. Pārskatiet **1099 Maksājumu modelis** datu modeļa konfigurācija.

    - Šīs konfigurācijas modeļa komponents atspoguļo datu modeļa struktūru, kas tiek izmantota datu pārsūtīšanai starp darbojošiem ER komponentiem.
    - Šīs konfigurācijas modeļa kartēšanas komponents tiek izmantots, lai iegūtu datus no izpildītā formāta komponenta un pēc tam atjauninātu lietojumprogrammu tabulas.

    ![ER datu modeļa konfigurācija datu importēšanai pakešu režīmā no ER lietotāja saskarnes.](./media/er-configure-data-import-batch-configurations-2.png)

5. Atveriet **1099import-data.xlsx** failu programmā Excel.

    ![Excel faila paraugs ar datiem importēšanai pakešu režīmā.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Iespējot ER paketes datu importēšanu no lietotāja saskarnes

1. Dodieties uz **Sistēmas administrēšana** \> **Darbvietas** \> **Līdzekļu pārvaldība**.
2. Iekš **Funkciju pārvaldība** darbvieta, atlasiet **Palaidiet manuāli augšupielādēto dokumentu ER importēšanu paketē** funkciju un pēc tam atlasiet **Iespējot tūlīt**.

## <a name="import-data-from-manually-selected-excel-files"></a>Importējiet datus no manuāli atlasītajiem Excel failiem

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Uz **Konfigurācijas** lapā atlasiet **1099 Maksājumu modelis** datu modeļa konfigurācija.
3. Uz **Konfigurācijas komponenti** FastTab, atlasiet **1099 manuālo darījumu importēšanai** saite.
4. Uz **Modelis uz datu avotu kartēšanu** lapa, **1099 manuālo darījumu importēšanai** modeļa kartēšana ir iepriekš atlasīta. Atlasiet **Izpildīt**.
5. Uz **Parametri** cilni, atlasiet **Pārlūkot**. Atrodiet un atlasiet **1099import-data.xlsx** failu un pēc tam atlasiet **labi**.
6. Iekš **Ievadiet kupona ID** laukā, ievadiet **V-00001**.
7. Uz **Palaist fonā** cilnē iestatiet **Partijas apstrāde** iespēja uz **Jā**.

    Ievērojiet, ka **Uzdevuma apraksts** lauks ir iestatīts uz **Modeļa kartēšanas “1099 manuālo darījumu importēšanai”, konfigurācijas “1099 maksājumu modelis” izpilde**. Šī vērtība norāda, ka atlasītā modeļa kartēšanas izpilde tiks ieplānota kā jauns pakešdarbs.

    ![Dialoglodziņā Elektroniskās atskaites parametri tiek norādīta detalizēta informācija par datu importēšanu pakešu režīmā.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Atlasiet **Labi**. Ziņojums informē, ka ir ieplānots jauns pakešdarbs.

    ![Ziņojums par jaunu ieplānotu pakešuzdevumu lapā Modelis uz datu avotu kartēšanu.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Pārskatīt datu importēšanas rezultātus pakešuzdevuma lapā

1. Dodieties uz **Vispārīgi** \> **Pieprasījumi** \> **Pakešuzdevumi** \> **Mani pakešuzdevumi**.
2. Lapā Pakešuzdevums **filtrējiet** pakešuzdevumu sarakstu, lai atrastu plānoto paketi, un pēc tam atlasiet to.
3. Atlasiet **saiti Darba ID**, lai pārskatītu detalizētu informāciju par darbu.
4. Kopsavilkuma cilnē **Pakešuzdevums** atlasiet **Žurnāls**.

    ![Poga Reģistrēt pakešuzdevuma lapā.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Pārskatiet izpildes detaļas.

    ![Plānotā pakešuzdevuma izpildes žurnāls pakešuzdevuma lapā.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Datu importēšanas parametru maiņa

Kad pakete ir ieplānota un kamēr tā vēl nav palaista, varat mainīt plānotās datu importēšanas parametrus.

1. Dodieties uz **Vispārīgi** \> **Pieprasījumi** \> **Pakešuzdevumi** \> **Mani pakešuzdevumi**.
2. Lapā Pakešuzdevums **filtrējiet** pakešuzdevumu sarakstu, lai atrastu plānoto paketi, un pēc tam atlasiet to.
3. Atlasiet **Mainīt statusu**.
4. Dialoglodziņā **Jauna statusa** atlasīšana atlasiet **Aizturēt** un pēc tam atlasiet **Labi**.
5. Atlasiet **saiti Darba ID**, lai piekļūtu darba detaļai.
6. Kopsavilkuma cilnē **Pakešuzdevums** atlasiet **Parametri**.
7. Dialoglodziņā **Elektroniskās atskaites parametri** rīkojieties šādi:

    1. Atlasiet **Pārlūkot**, lai atlasītu alternatīvo failu datu importēšanai.
    2. Atlasiet **Ievadīt dokumenta ID**, lai mainītu kreditora darbību importēšanas dokumenta numuru.

        ![Datu importēšanas parametru mainīšana plānotajam pakešuzdevumam dialoglodziņā Elektroniskā pārskata parametri.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Atlasiet **Labi**.

8. Pārliecinieties, vai pakete joprojām ir atlasīta, un pēc tam vēlreiz atlasiet **Mainīt statusu**.
9. Dialoglodziņā **Jauna statusa** atlasīšana atlasiet **Gaida** un pēc tam atlasiet **Labi**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Datu importēšanas rezultātu pārskatīšana ER avota lapā

1. Dodieties uz **Organizācijas administrēšana** \> **Elektroniskā atskaišu elektroniskās ziņošanas** \> **avots.**
2. Atlasiet **ierakstu kreditoru darbību importēšanai (Excel),** kas tika automātiski izveidots datu importēšanas laikā.

    ![Konfigurācijas Kreditoru darbību importēšanai (Excel) ieraksts lapā Elektroniskās pārskatu avota avots.](./media/er-configure-data-import-batch-files-source-1.png)

3. Atlasiet **Avotu** failu stāvokļi.
4. **Kopsavilkuma cilnes Importēšanas formāta** žurnālos Faili **un** avots pārskatiet importa detaļas.
5. Kopsavilkuma cilnē **Faili** atlasiet ierakstu. Ievērojiet, ka importētais fails ir pievienots šim ierakstam.

    ![Importētais fails, kas pievienots ierakstam lapā Failu stāvokļi avotiem.](./media/er-configure-data-import-batch-files-source-2.png)

6. Atlasiet **Pielikumi**, lai pārskatītu importēto failu.

    ![Importētais fails dokumenta skata lapā.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Lai paturētu šos pielikumus, ER struktūra izmanto dokumenta tipu, kas pašreizējam uzņēmumam ir [iestatīts](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)**ER parametru laukā Citi**.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Pārskatīt datu importēšanas rezultātus lapā Kreditoru nosegšana 1099s

1. Dodieties uz **Parādi kreditoriem** \> **Periodiskie uzdevumi** \> **Nodoklis 1099** \> **Kreditora nosegšana 1099s.**
2. Laukā **No datuma** ievadiet **12/31/2017 (2017** . gada 31. decembris).
3. Atlasiet **Manuālas 1099 darbības**.

    ![Importētās kreditoru darbības lapā PVN 1099 darbības.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
