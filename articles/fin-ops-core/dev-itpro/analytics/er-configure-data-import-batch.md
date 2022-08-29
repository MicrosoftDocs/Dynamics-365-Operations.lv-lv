---
title: Datu importēšana no manuāli atlasītiem failiem pakešveida režīmā
description: Šajā rakstā ir aprakstīts, kā importēt datus no manuāli atlasītiem failiem pakešveida režīmā.
author: kfend
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
ms.openlocfilehash: 21a2ab5f0eb07dda92baf9cc04ee36caeff8b4ec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288234"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Datu importēšana no manuāli atlasītiem failiem pakešveida režīmā

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Lai lietotu elektronisko [pārskatu (ER)](general-electronic-reporting.md) struktūru, lai importētu datus no manuāli atlasītiem ienākošajiem failiem pakešveida režīmā, konfigurējiet ER [formātu](er-overview-components.md#format-component), kas atbalsta importu. Pēc tam palaidiet [mērķa tipa](er-overview-components.md#model-mapping-component) Uz modeļa **kartējumu**, kas izmanto šo formātu kā datu avotu. Lai importētu datus, pārlūkojiet failu, kuru vēlaties importēt, un manuāli atlasiet to. 

Jauna ER iespēja, kas atbalsta datu importu pakešveida režīmā, ļauj šo procesu konfigurēt kā neapstrādātu. ER konfigurācijas var izmantot datu importēšanai, plānojot jaunu pakešuzdevumu no ER lietotāja interfeisa (UI).

Šajā rakstā ir aprakstīts, kā pabeigt datu importēšanu no manuāli atlasīta faila pakešveida režīmā. Piemēros kā biznesa dati tiek izmantotas kreditoru transakcijas. Šo piemēru soļus var izpildīt **USMF** uzņēmumā. Kodēšana nav nepieciešama.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai pabeigtu piemērus šajā rakstā, jums ir jābūt šādai piekļuvei:

- Viena no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- ER formāts un modeļa konfigurācijas 1099 maksājumiem

### <a name="create-the-required-er-configurations"></a>Izveidot nepieciešamās ER konfigurācijas

Lai izveidotu nepieciešamās ER konfigurācijas un iegūtu citus priekšnosacījumus, veiciet vienu no šīm darbībām:

- Noskatieties uzdevumu ceļvežus **ER: datu importēšana no Microsoft Excel faila**, kas ir ietverti biznesa procesā **7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**. Šie uzdevumu ceļveži skaidro jums ER konfigurāciju izstrādāšanas un lietošanas procesu, kas interaktīvi importē kreditora darījumus no Microsoft Excel failiem. Plašāku informāciju skatiet tēmā [Ienākošo dokumentu parsēšana programmā Excel formātā](parse-incoming-documents-excel.md).
- Pabeidziet piemērus, konfigurējot [datu importēšanu no SharePoint](er-configure-data-import-sharepoint.md). Šie piemēri skaidro jums tādu ER konfigurāciju izstrādāšanas un lietošanas procesu, kas interaktīvi importē kreditoru darbības no Programmas Excel failiem, kas tiek uzglabāti SharePoint mapē.

### <a name="download-the-required-er-configurations"></a>Lejupielādēt nepieciešamās ER konfigurācijas

1. Lejupielādējiet šādas ER konfigurācijas un saglabājiet tās lokāli.

    | Satura apraksts | Fails |
    |---------------------|------|
    | **1099 maksājumu modeļa** ER datu modeļa konfigurācija | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Kreditoru darbību importēšanai (Excel)** ER formāta konfigurācija | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Izmantojiet opciju [Ielādēt no XML](er-defer-sequence-element.md#import-the-sample-er-configurations) faila ER, lai importētu lejupielādētās ER konfigurācijas jūsu Dynamics 365 Finanšu instancē šādā secībā:

    1. ER datu modeļa konfigurācija
    2. ER formāta konfigurācija

### <a name="download-the-required-excel-files"></a>Lejupielādēt nepieciešamos Excel failus

- Lejupielādējiet šo parauga datu kopu un saglabājiet to lokāli.

    | Satura apraksts | Fails |
    |---------------------|------|
    | Ienākošais **1099import-data.xlsx** fails, kas satur importa parauga datus | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Pārskatīt priekšnosacījumus

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā Konfigurācijas **pārskatiet** sagatavoto ER risinājumu datu importēšanai pakešveida režīmā.
3. Pārskatiet **kreditoru darbību importēšanas (Excel)** formāta konfigurāciju.

    - Šīs konfigurācijas formāta komponents ir paredzēts ienākošo Excel faila parsam.
    - Šīs konfigurācijas modeļa kartēšanas komponents tiek izmantots, lai aizpildītu pamatdatu modeli, izmantojot datus no parsētā Excel faila.

    ![ER formāta konfigurācija datu importēšanai pakešuzdevuma režīmā no ER UI.](./media/er-configure-data-import-batch-configurations-1.png)

4. Pārskatiet **1099 maksājumu modeļa** datu modeļa konfigurāciju.

    - Šīs konfigurācijas modeļa komponents atspoguļo tā datu modeļa struktūru, kas tiek lietots, lai padotu datus starp ER komponentiem, kas darbojas.
    - Šīs konfigurācijas modeļa kartēšanas komponents tiek izmantots, lai vilktu datus no izpildītā formāta komponenta un pēc tam atjauninātu programmas tabulas.

    ![ER datu modeļa konfigurācija datu importēšanai pakešuzdevuma režīmā no ER UI.](./media/er-configure-data-import-batch-configurations-2.png)

5. **Atveriet 1099import-data.xlsx** failu programmā Excel.

    ![Paraugs: Excel fails ar datiem importēšanai pakešveida režīmā.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Iespējot partijas datu importēšanu ER no UI

1. Dodieties uz **Sistēmas administrēšana** \> **Darbvietas** \> **Līdzekļu pārvaldība**.
2. Līdzekļu pārvaldības **darbvietā** atlasiet manuāli **augšupielādēto dokumentu importēšanas darbību ER** pakešuzdevumā un pēc tam atlasiet Iespējot **tūlīt**.

## <a name="import-data-from-manually-selected-excel-files"></a>Importēt datus no manuāli atlasītajiem Excel failiem

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā Konfigurācijas **atlasiet** **1099 maksājumu modeļa datu** modeļa konfigurāciju.
3. Kopsavilkuma cilnē **Konfigurācijas komponenti** atlasiet saiti Manuālas **darbības 1099.**
4. Lapā Modelis **uz datu avotu kartēšana** ir iepriekš atlasīta **opcija 1099 manuālo** darbību importēšanas modeļa kartēšanai. Atlasiet **Izpildīt**.
5. Cilnē Parametri **atlasiet Pārlūkot** **.** Atrodiet un atlasiet **1099import-data.xlsx** failu un pēc tam atlasiet **Labi**.
6. Laukā **Ievadīt dokumenta ID** ievadiet **V-00001**.
7. Cilnes Fona **cilnē Palaist iestatiet** opciju Pakešapstrāde **uz** **Jā**.

    Ievērojiet, ka **·** **uzdevuma apraksta laukam ir iestatīta modeļu kartēšanas palaišana '1099 manuālo darbību importam', konfigurācijai '1099 Maksājumu modelis'**. Šī vērtība norāda, ka atlasītā modeļa kartēšanas izpilde tiks plānota kā jauns pakešuzdevums.

    ![Norādot datu importa detaļas pakešveida režīmā dialoglodziņā Elektronisko pārskatu parametri.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Atlasiet **Labi**. Ziņojums ziņo, ka ir ieplānots jauns pakešuzdevums.

    ![Ziņojums par jaunu ieplānotu pakešuzdevumu modeļa datu avota kartēšanas lapā.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Pārskatīt datu importēšanas rezultātus lapā Pakešuzdevums

1. Dodieties uz **Vispārīgi** \> **Pieprasījumi** \> **Pakešuzdevumi** \> **Mani pakešuzdevumi**.
2. Lapā Pakešuzdevums **filtrējiet** pakešuzdevumu sarakstu, lai atrastu ieplānoto pakešuzdevumu, un pēc tam atlasiet to.
3. Atlasiet darba **ID saiti,** lai pārskatītu darba papildinformāciju.
4. Kopsavilkuma cilnē **Pakešuzdevumi** atlasiet **Žurnāls**.

    ![Poga Žurnāls lapā Pakešuzdevums.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Pārskatiet detalizētu informāciju par izpildi.

    ![Ieplānotā pakešuzdevuma izpildes žurnāls pakešuzdevumu lapā.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Mainīt datu importēšanas parametrus

Kad pakete ir ieplānota un kamēr tā vēl nav palaista, ir iespējams mainīt plānotā datu importa parametrus.

1. Dodieties uz **Vispārīgi** \> **Pieprasījumi** \> **Pakešuzdevumi** \> **Mani pakešuzdevumi**.
2. Lapā Pakešuzdevums **filtrējiet** pakešuzdevumu sarakstu, lai atrastu ieplānoto pakešuzdevumu, un pēc tam atlasiet to.
3. Atlasiet **Mainīt statusu**.
4. Dialoglodziņā Atlasīt **jaunu statusu** atlasiet Aizturēt **un** pēc tam atlasiet **Labi**.
5. Atlasiet darba **ID saiti,** lai piekļūtu darba informācijai.
6. Kopsavilkuma cilnē **Pakešuzdevumi** atlasiet **Parametri**.
7. Dialoglodziņā Elektroniskā **pārskata parametri** sekojiet šiem soļiem:

    1. Atlasiet **Pārlūkot,** lai atlasītu alternatīvo failu datu importēšanai.
    2. Atlasiet **ievadiet dokumenta ID**, lai mainītu kreditora darbību importēšanas dokumenta numuru.

        ![Datu importēšanas parametru maiņa plānotajam pakešuzdevumam dialoglodziņā Elektronisko pārskatu parametri.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Atlasiet **Labi**.

8. Pārliecinieties, ka pakete joprojām ir atlasīta, un pēc tam vēlreiz **atlasiet Mainīt** statusu.
9. Dialoglodziņā Atlasīt **jaunu statusu** atlasiet Gaida un **pēc** tam atlasiet **Labi**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Pārskatīt datu importēšanas rezultātus ER avota lapā

1. Dodieties uz **organizācijas administrēšanas** \> **elektronisko pārskatu** \> **elektronisko pārskatu avotu.**
2. Atlasiet kreditoru **darbību importēšanas (Excel)** ierakstu, kas tika izveidots automātiski datu importēšanas laikā.

    ![Ieraksts kreditoru darbību importēšanas (Excel) konfigurācijai elektronisko pārskatu avota lapā.](./media/er-configure-data-import-batch-files-source-1.png)

3. Atlasiet **Avotu failu statusi**.
4. Kopsavilkuma cilnēs **Faili** **un Avota žurnāli par importa** formātu pārskatiet informāciju par importēšanu.
5. **Kopsavilkuma cilnē** Faili atlasiet ierakstu. Ievērojiet, ka importētais fails ir pievienots šim ierakstam.

    ![Importētais fails, kas pievienots ierakstam faila lapā Avotu nosaka.](./media/er-configure-data-import-batch-files-source-2.png)

6. Atlasiet **pielikumus,** lai pārskatītu importēto failu.

    ![Importētais fails dokumentu skata lapā.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Lai saglabātu šos pielikumus, ER [...](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)**struktūra izmanto dokumenta tipu, kas pašreizējam uzņēmumam ir iestatīts** ER parametru laukā Citi.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Pārskatīt datu importēšanas rezultātus kreditoru nodokļa 1099 lapas nosegšanai

1. Dodieties uz **sadaļu** \> **Kreditoru periodiskie** \> **uzdevumi nodokļa 1099 kreditora** \> **nodokļa 1099 nosegšanai.**
2. Laukā No **datuma ievadiet** **2017. gada 12. decembrī (2017** . gada 31. decembris).
3. Atlasiet **manuālas 1099 darbības**.

    ![Importētās kreditora darbības nodokļa 1099 darbību lapā.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
