---
title: ER formāta izveide, lai ģenerētu pārskatu Excel formātā ar iegultiem attēliem lapas galvenēs vai kājenēs
description: Šajā rakstā skaidrots, kā izmantot elektroniskos pārskatus (ER), lai ģenerētu biznesa dokumentus, kuriem ir attēli un formas iegulti lapas galvenēs un kājenēs.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1cfde60459e440c851edb97276321216b1654e40
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854848"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>ER formāta izveide, lai ģenerētu pārskatu Excel formātā ar iegultiem attēliem lapas galvenēs vai kājenēs

[!include[banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā lietotājs sistēmas administratora vai elektroniskā pārskata funkcionālā konsultanta lomā var veikt šos uzdevumus:

- Konfigurēt parametrus [Elektronisko pārskatu (ER)](general-electronic-reporting.md) veidošanas struktūrai.
- Importēt ER [konfigurācijas](general-electronic-reporting.md#Configuration), ko [nodrošina](general-electronic-reporting.md#Provider) Microsoft un ko izmanto, lai ģenerētu [brīvā teksta rēķinus](../../../finance/accounts-receivable/create-free-text-invoice-new.md), pamatojoties uz [veidnes](er-fillable-excel.md#excel-file-component) formātā Microsoft Excel.
- Izveidot Microsoft nodrošinātās standarta ER formāta konfigurācijas [pielāgotu (atvasinātu)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) versiju.
- Modificēt pielāgoto ER formāta konfigurāciju, lai tā ģenerētu brīvā teksta rēķina pārskatu, kam kājenē ir uzņēmuma logotipa attēls.

Šajā rakstā šīs procedūras var izpildīt **USMF** uzņēmumā. Kodēšana nav nepieciešama. Pirms sākšanas, lejupielādējiet un saglabājiet tālāk norādīto failu:

| Apraksts        | Faila nosaukums |
|--------------------|-----------|
| Uzņēmuma logo attēls | [Uzņēmuma logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Saturs

- [Juridiskās personas konfigurācija](#ConfigureLegalEntity)
- [ER struktūras konfigurēšana](#ConfigureFramework)

    - [Konfigurējiet ER parametrus](#ConfigureParameters)
    - [ER konfigurācijas nodrošinātāja aktivizēšana](#ActivateProvider)

        - [ER konfigurācijas nodrošinātāju saraksta pārskatīšana](#ReviewProvidersList)
        - [Jauna ER konfigurācijas nodrošinātāja pievienošana](#AddProvider)
        - [Jaunā ER konfigurācijas nodrošinātāja aktivizēšana](#ActivateAddedProvider)

- [Standarta ER formāta konfigurāciju importēšana](#ImportERSolution1)

    - [Standarta ER konfigurāciju importēšana](#ImportERFormat)
    - [Importēto ER konfigurāciju pārskatīšana](#ReviewImportedERSolution)

- [Drukāt brīva teksta rēķinu, izmantojot standarta ER formātu](#PrintInvoice1)

    - [Drukas pārvaldības iestatīšana](#ConfigurePrintManagement1)
    - [Drukāt brīva teksta rēķinu](#ProcessInvoice1)

- [Standarta ER formāta pielāgošana](#CustomizeProvidedFormat)

    - [Pielāgota formāta izveidošana](#DeriveProvidedFormat)
    - [Pielāgotā formāta rediģēšana](#ConfigureDerivedFormat)
    - [Pielāgota formāta atzīmēšana kā izpildāms](#MarkFormatRunnable)

- [Drukāt brīva teksta rēķinu, izmantojot pielagoto ER formātu](#PrintInvoice2)

    - [Drukas pārvaldības iestatīšana](#ConfigurePrintManagement2)
    - [Drukāt brīva teksta rēķinu](#ProcessInvoice2)

- [Papildu resursi](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Juridiskās personas konfigurācija

1. Dodieties uz **Organizācijas administrēšana** \> **Organizācijas** \> **Juridiskās personas**.
2. Lapā **Juridiskās personas** kopsavilkuma cilnē **Pārskata uzņēmuma logotipa attēls** atlasiet **Mainīt**.
3. Dialoglodziņā **Atlasīt augšupielādējamā attēla failu** atlasiet **Pārlūkot** un atlasiet failu **Uzņēmuma logotips.png**, kuru lejupielādējāt agrāk.
4. Atlasiet **Saglabāt** un pēc tam aizvēriet lapu **Juridiskās personas**.

![Uzņēmuma logotipa attēls, kas atlasīts juridisko personu lapā.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>ER struktūras konfigurēšana

Kā lietotājam elektronisko pārskatu funkcionālā konsultanta lomā, jums ir jākonfigurē minimāls ER parametru kopums, pirms varat sākt izmantot ER struktūru, lai veidotu standarta ER formāta pielāgotu versiju.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurējiet ER parametrus

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.
3. Lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi** iestatiet opciju **Iespējot noformēšanas režīmu** uz **Jā**.
4. Cilnē **Pielikumi** iestatiet šādus parametrus:

    - Laukā **Konfigurācijas** atlasiet veidu **Fails** uzņēmumam **USMF**.
    - Laukos **Darbu arhīvs**, **Pagaidu**, **Bāzlīnija** un **Citi** atlasiet veidu **Fails**.

Papildinformāciju par ER parametriem skatiet sadaļā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER konfigurācijas nodrošinātāja aktivizēšana

Katra pievienotā ER konfigurācija tiek atzīmēta kā piederoša ER konfigurācijas nodrošinātājam. Šim nolūkam tiek izmantots ER konfigurācijas nodrošinātājs, kas ir aktivizēts **Elektroniskie pārskati** darbvietā. Tāpēc, pirms sākat pievienot vai rediģēt ER konfigurācijas, jums ir jāaktivizē ER konfigurācijas nodrošinātājs **Elektroniskie pārskati** darbvietā.

> [!NOTE]
> ER konfigurāciju var rediģēt tikai konfigurācijas īpašnieks. Pirms ER konfigurācija var tikt rediģēta, darbvietā **Elektroniskie pārskati** ir jāaktivizē atbilstošais ER konfigurācijas nodrošinātājs.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER konfigurācijas nodrošinātāju saraksta pārskatīšana

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

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Jaunā ER konfigurācijas nodrošinātāja aktivizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.** un pēc tam atlasiet **Iestatīt kā aktīvu**.

Papildinformāciju par ER konfigurācijas nodrošinātājiem skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Standarta ER formāta konfigurāciju importēšana

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Standarta ER konfigurāciju importēšana

Lai pievienotu standarta ER konfigurācijas pašreizējai Dynamics 365 Finanšu instancei, jums tās jāimportē no ER [repozitorija](general-electronic-reporting.md#Repository), kas tika konfigurēts šim gadījumam.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft** un pēc tam atlasiet **Repozitoriji**, lai skatītu **Microsoft** nodrošinātāja repozitoriju sarakstu.
3. Lapā **Konfigurācijas repozitoriji** atlasiet repozitoriju ar veidu **Globāls** un pēc tam atlasiet **Atvērt**. Ja tiek pieprasīta autorizācija savienojumam ar [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md), izpildiet autorizācijas norādījumus.
4. Lapā **Konfigurācijas repozitorijs** konfigurācijas koka skata kreisajā rūtī atlasiet **Brīva teksta rēķins (Excel)** formāta konfigurāciju.
5. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER formāta konfigurācijas jaunāko versiju (piemēram, **240.112**).
6. Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija uz pašreizējo Finance instanci.

![Standarta ER konfigurāciju importēšana lapā Konfigurācijas krātuve.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Ja rodas problēmas ar piekļuvi [globālajam repozitorijam](er-download-configurations-global-repo.md), tā vietā varat [lejupielādēt konfigurācijas](download-electronic-reporting-configuration-lcs.md) no Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Importēto ER konfigurāciju pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis**.
4. Papildus atlasītajam **Brīva teksta rēķins (Excel)** ER formātam tika importētas arī citas nepieciešamās ER konfigurācijas. Pārliecinieties, vai konfigurācijas kokā ir pieejamas šādas ER konfigurācijas:

    - **Rēķina modelis** - šī konfigurācija satur datu modeļa ER komponentu, kas parāda rēķinu izrakstīšanas biznesa domēna datu struktūru.
    - **Rēķina modeļa kartēšana** - šī konfigurācija ietver modeļa kartēšanas ER komponentu, kas apraksta, kā izpildlaikā datu modelis tiek aizpildīts ar programmas datiem.
    - **Brīva teksta rēķins (Excel)** – šī konfigurācija satur formātu un formātu kartēšanas ER komponentus. Formāta komponents nosaka pārskata formātu, pamatojoties uz veidni Excel formātā. Formāta kartēšanas komponents satur modeļa datu avotu un norāda, kā šis datu avots tiek izmantots, lai aizpildītu atskaites izkārtojumu izpildlaikā.

![Konfigurāciju lapā importētās ER konfigurācijas.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Drukāt brīva teksta rēķinu, izmantojot standarta ER formātu

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Drukas pārvaldības iestatīšana

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Lapā **Brīva teksta rēķins** atlasiet **FTI-00000002** rēķinu un pēc tam Darbību rūtī cilnē **Rēķins** grupā **Drukas pārvaldība** atlasiet **Drukas pārvaldība**.
3. Lapas **Drukas pārvaldības iestatījums** kreisajā pusē koka struktūrā izvērsiet **Modulis - debitoru parādi \> Dokumenti \> Brīvā teksta rēķins** un pēc tam atlasiet krājumu **Sākotnējais \<Default\>**.
4. Laukā **Pārskata formāts** atlasiet **Brīva teksta rēķins (Excel)**.
5. Atlasiet taustiņu **Esc**, lai atstātu lapu **Drukas pārvaldības iestatījums** un atgrieztos lapā **Brīva teksta rēķins**.

![Drukas pārvaldības iestatījumi brīva teksta rēķinam standarta ER formātā drukas pārvaldības iestatījuma lapā.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Drukāt brīva teksta rēķinu

1. Lapā **Brīva teksta rēķins** pārliecinieties, ka ir atlasīts rēķins **FTI-00000002** un pēc tam Darbību rūtī cilnē **Rēķins** grupā **Dokuments** atlasiet **Drukat** \> **Atlasīts**.
2. Lejupielādējiet ģenerēto rēķinu Excel formātā un atveriet to priekšskatījumā.
3. Ņemiet vērā, ka saskaņā ar Excel veidnes struktūru, kas paredzēta ER formātam, ģenerētā rēķina lapas kājenē ir informācija par pašreizējo lapas numuru un kopējo lapu skaitu pārskatā.

![Ģenerēts brīva teksta rēķins.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Standarta ER formāta pielāgošana

Piemēram šajā sadaļā varat izmantot ER konfigurācijas, ko nodrošina Microsoft, lai izveidotu brīva teksta rēķinu Excel formātā. Tomēr pielāgošana ir jāpievieno, lai ģenerēto rēķinu lapas kājenē ievietotu uzņēmuma logotipa attēlu.

Šādā gadījumā, kā Litware, Inc. pārstāvim, jums ir jāizveido (jāatvasina) jauna ER formāta konfigurācija, kas balstīta uz Microsoft nodrošināto **Brīva teksta rēķins (Excel)** konfigurāciju.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Pielāgota formāta izveidošana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modelis** un pēc tam atlasiet **Brīva teksta rēķins (Excel)**. Litware, Inc. izmantos šīs ER formāta konfigurācijas importēto versiju (piemēram, **240.112**) kā pielāgotās versijas bāzi.
3. Atlasiet **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu. Izmantojiet šo dialoglodziņu, lai izveidotu jaunu konfigurāciju pielāgotam maksājuma formātam.
4. Lauka grupā **Jauns** atlasiet opciju **Atvasināt no nosaukuma: Brīva teksta rēķins (Excel), Microsoft**.
5. Laukā **Nosaukums** ievadiet **Brīva teksta rēķina (Excel) pielāgošana**.
6. Atlasiet **Izveidot konfigurāciju**.

![Izveidojiet konfigurāciju pielāgotā maksājuma formātam nolaižamajā dialoglodziņā Izveidot konfigurāciju.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Tiek 240.112.1 **Brīvā teksta rēķina (Excel) pielāgošana** ER formāta konfigurācijas versija. Šīs versijas [statuss](general-electronic-reporting.md#component-versioning) ir **Melnraksts** un to var rediģēt. Pielāgotā ER formāta pašreizējais saturs atbilst Microsoft nodrošinātā formāta saturam.

![ER formāta konfigurācijas jauna versija izveidota Konfigurāciju lapā.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Pielāgotā formāta rediģēšana

Konfigurējiet savu pielāgoto formātu tā, lai uzņēmuma logotipa attēls būtu ievietots pārskata katras lapas kājenē.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **Brīva teksta rēķina (Excel) pielagošana**.
3. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās konfigurācijas **240.112.1** versiju.
4. Atlasiet **Noformētājs**.
5. Lapā **Formāta veidotājs** atlasiet **Rādīt detalizēti**, lai skatītu papildinformāciju par formāta elementiem.
6. Izvērsiet un pārskatiet šādus elementus:

    - Elements **Brīva teksta rēķins** **Excel** tipa. Šis elements tiek izmantots, lai izveidotu rēķinu Excel darbgrāmatas formātā.
    - Elements **Brīva teksta rēķins \\ Rēķins** **Lapa** tipa. Šis elements tiek izmantots, lai ģenerētu ģenerētās Excel darbgrāmatas darblapu.
    - Elements **Brīva teksta rēķins \\ Rēķins \\ Kājiene** **Kājiene** tipa. Šis elements tiek izmantots, lai aizpildītu rēķina kājeni.

7. Atlasiet elementu **Brīvā teksta rēķins \\ Rēķins \\ Kājene**.

    ![Kājienes elements ER operāciju veidotājā.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Katra ģenerētā rēķina lappuses kājene ietver informāciju par pašreizējo lappuses numuru un kopējo lapu skaitu pārskatā. Kā redzams, elementā **Brīvā teksta rēķins \\ Rēķins \\ Kājene** nav apakšelementu. Tāpēc izmantotais Excel veidne tiek konfigurēta tā, lai parādītu lapošanas detaļas katra pārskata kājenē.

8. Atlasiet **Pievienot** un pēc tam atlasiet **Excel \\ Attēls** formāta elementa veidu, kuru pievienojat:

    1. Laukā **Līdzinājums** atlasiet **Pa labi**.
    2. Laukā **Mērogot augstumu** atlasiet **Relatīvais**.
    3. Laukā **Svari procentos** ievadiet **70**.
    4. Atlasiet **Labi**.

        > [!NOTE]
        > Elements **Excel \\ Attēls** tiek izmantots, lai pievienotu uzņēmuma logotipa attēlu un līdzinātu to lapas kājenes labajā pusē.

    ![Attēla elementa rekvizīti dialoglodziņā Komponentu rekvizīti.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Formāta struktūras kokā kreisajā pusē atlasiet tikko pievienoto elementu **Attēls** un pēc tam cilnē **Kartēšana** izvērsiet datu avotu **modelis**.
10. Izvērst **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo** un pēc tam atlasiet **model.InvoiceBase.CompanyInfo.Logo** datu avota lauku. Datu avota lauks [Konteinera](er-formula-supported-data-types-composite.md#container) veida pakļauj uzņēmuma logotipa attēlu kā plašsaziņas līdzekļu saturu.
11. Atlasiet **Saistīt**. Tagad formāta elements **Attēls** ir piesaistīts datu avota laukam **model.InvoiceBase.CompanyInfo.Logo**. Tāpēc izpildlaikā uzņēmuma logotipa attēls tiks ievietots ģenerēto rēķinu kājenē.

    ![Formāta elements Attēls ir piesaistīts datu avota laukam model.InvoiceBase.CompanyInfo.Logo ER operāciju veidotājā.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Atlasiet **Saglabāt** un pēc tam aizvēriet lapu **Veidotājs**.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Pielāgota formāta atzīmēšana kā izpildāms

Tāpēc ka ir izveidota pielāgotā formāta pirmā versija un tai ir statuss **Melnraksts**, varat palaist formātu testēšanas nolūkos. Lai palaistu pārskatu, apstrādājiet kreditora maksājumu, izmantojot maksāšanas metodi, kas attiecas uz pielāgoto ER formātu. Pēc noklusējuma, izsaucot ER formātu no programmas, tiek [ņemtas vērā](general-electronic-reporting.md#component-versioning) tikai tās versijas, kuru statuss ir **Pabeigts** vai **Koplietots**. Šī darbība neļauj izmantot ER formātus, kuri nav pabeigti. Tomēr testējot, programmai var likt izmantot ER formāta versiju ar statusu **Melnraksts**. Šādā veidā var pielāgot pašreizējo formāta versiju, ja ir nepieciešamas kādas modifikācijas. Papildinformāciju skatiet sadaļā [Piemērojamība](electronic-reporting-destinations.md#applicability).

Lai izmantotu ER formāta melnraksta versiju, jums jāatzīmē ER formāts.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Palaist iestatījumus** uz **Jā** un pēc tam atlasiet **Labi**.
4. Atlasiet **Rediģēt**, lai pašreizējā lapa būtu rediģējama, un pēc tam konfigurācijas koka skata kreisajā rūtī atlasiet **Brīva teksta rēķina (Excel) pielagošana**.
5. Iestatiet opciju **Palaist melnrakstu** uz **Jā**.

![Pielāgotā formāta atzīmēšana kā izpildāma konfigurāciju lapā.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Drukāt brīva teksta rēķinu, izmantojot pielagoto ER formātu

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Drukas pārvaldības iestatīšana

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Lapā **Brīva teksta rēķins** atlasiet **FTI-00000002** rēķinu un pēc tam Darbību rūtī cilnē **Rēķins** grupā **Drukas pārvaldība** atlasiet **Drukas pārvaldība**.
3. Lapas **Drukas pārvaldības iestatījums** kreisajā pusē koka struktūrā izvērsiet **Modulis - debitoru parādi** \> **Dokumenti** \> **Brīvā teksta rēķins** un pēc tam atlasiet krājumu **Sākotnējais** **\<Default\>**.
4. Laukā **Pārskata formāts** atlasiet **Brīva teksta rēķina (Excel) pielagošana**.
5. Atlasiet **Esc**, lai atstātu lapu **Drukas pārvaldības iestatījums** un atgrieztos lapā **Brīva teksta rēķins**.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Drukāt brīva teksta rēķinu

1. Lapā **Brīva teksta rēķins** pārliecinieties, ka ir atlasīts rēķins **FTI-00000002** un pēc tam Darbību rūtī cilnē **Rēķins** grupā **Dokuments** atlasiet **Drukat** \> **Atlasīts**.
2. Lejupielādējiet ģenerēto rēķinu Excel formātā un atveriet to priekšskatījumā.
3. Ņemiet vērā, ka saskaņā ar pielāgotā ER formāta struktūru ģenerētā rēķina lapas kājenē papildus informācijai par pārskata lapošanu ir uzņēmuma logotipa attēls.

![Ģenerēts brīva teksta rēķins ar uzņēmuma logotipa attēlu lapas kājenē.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Papildu resursi

- [Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā](er-fillable-excel.md)
- [Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md)
