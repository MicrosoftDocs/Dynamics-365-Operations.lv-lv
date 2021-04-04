---
title: Koriģēt ER formātu pielāgota elektroniskā dokumenta ģenerēšanai
description: Šajā tēmā ir paskaidrots, kā koriģēt Microsoft nodrošināto elektronisko pārskatu (ER) formātu, lai tas ģenerētu pielāgotu elektronisko dokumentu.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
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
ms.openlocfilehash: 3c643c913d9bc9233c891709593dff995284e2e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569001"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Koriģēt ER formātu pielāgota elektroniskā dokumenta ģenerēšanai

[!include[banner](../includes/banner.md)]

Šīs tēmas procedūrās ir paskaidrots, kā lietotājs sistēmas administratora vai elektronisko pārskatu funkcionālā konsultanta lomā var veikt šos uzdevumus:

- Konfigurēt parametrus [Elektronisko pārskatu (ER) veidošanas struktūrai](general-electronic-reporting.md).
- Importēt Microsoft nodrošinātās ER konfigurācijas un izmantot, lai ģenerētu maksājuma failu, kamēr [kreditora maksājums](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) tiek apstrādāts.
- Izveidot Microsoft nodrošinātās standarta ER formāta konfigurācijas pielāgotu versiju.
- Modificēt pielāgoto ER formāta konfigurāciju, lai tā ģenerētu maksājuma failus, kas atbilst noteiktas bankas prasībām.
- Pieņemt standarta ER formāta konfigurācijā veiktās izmaiņas pielāgotajā ER formāta konfigurācijā.

Visas tālāk norādītās procedūras var veikt uzņēmumā **GBSI**. Kodēšana nav nepieciešama.

- [ER struktūras konfigurēšana](#ConfigureFramework)

    - [Konfigurējiet ER parametrus](#ConfigureParameters)
    - [ER konfigurācijas nodrošinātāja aktivizēšana](#ActivateProvider)

        - [ER konfigurācijas nodrošinātāju saraksta pārskatīšana](#ReviewProvidersList)
        - [Jauna ER konfigurācijas nodrošinātāja pievienošana](#ActivateProvider)
        - [ER konfigurācijas nodrošinātāja aktivizēšana](#ActivateAddedProvider)

- [Standarta ER formāta konfigurāciju importēšana](#ImportERSolution1)

    - [Standarta ER konfigurāciju importēšana](#ImportERFormat1)
    - [Importēto ER konfigurāciju pārskatīšana](#ReviewImportedERSolution)

- [Kreditora maksājuma sagatavošana apstrādei](#PrepareVendorPayment)

    - [Bankas informācijas pievienošana kreditora kontam](#AddBankAccount)
    - [Kreditora maksājuma ievadīšana](#EnterVendorPayment)

- [Kreditora maksājuma apstrādāšana, izmantojot standarta ER formātu](#ProcessVendorPayment1)

    - [Elektroniskā maksājuma metodes iestatīšana](#ConfigureMethodOfPayment1)
    - [Kreditora maksājuma apstrādāšana](#ProcessPayment1)

- [Standarta ER formāta pielāgošana](#CustomizeProvidedFormat)

    - [Pielāgota formāta izveidošana](#DeriveProvidedFormat)
    - [Pielāgota formāta rediģēšana](#ConfigureDerivedFormat)
    - [Pielāgota formāta atzīmēšana kā izpildāms](#MarkFormatRunnable)

- [Kreditora maksājuma apstrādāšana, izmantojot pielāgotu ER formātu](#ProcessVendorPayment2)

    - [Elektroniskā maksājuma metodes iestatīšana](#ConfigureMethodOfPayment2)
    - [Kreditora maksājuma apstrādāšana](#ProcessPayment2)

- [Jaunas standarta ER formāta konfigurācijas versijas importēšana](#ImportERSolution2)

    - [Jaunas standarta ER konfigurācijas versijas importēšana](#ImportERFormat2)
    - [Importētās ER formāta konfigurācijas pārskatīšana](#ReviewImportedERFormat)

- [Importētā formāta jaunās versijas izmaiņu pieņemšana pielāgotajā formātā](#AdoptNewBaseVersion)

    - [Pielāgotā formāta pašreizējās melnraksta versijas pabeigšana](#CompleteDerivedFormat)
    - [Pielāgotā formāta pārvietošana uz jaunu bāzes versiju](#RebaseDerivedFormat)
    - [Kreditora maksājuma apstrādāšana, izmantojot pārveidotu ER formātu](#ProcessPayment3)

- [Papildu resursi](#References)

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
> Tikai ER konfigurācijas īpašnieks var to rediģēt. Tāpēc, pirms ER konfigurācija var tikt rediģēta, darbvietā **Elektroniskie pārskati** ir jāaktivizē atbilstošais ER konfigurācijas nodrošinātājs.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER konfigurācijas nodrošinātāju saraksta pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
3. Lapā **Konfigurācijas nodrošinātāju tabula** katram nodrošinātāja ierakstam ir unikāls nosaukums un URL. Pārskatiet šīs lapas saturu. Ja ieraksts **Litware, Inc.** (`https://www.litware.com`) jau pastāv, izlaidiet nākamo procedūru, [Jauna ER konfigurācijas nodrošinātāja pievienošana](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Jauna ER konfigurācijas nodrošinātāja pievienošana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
3. Lapā **Konfigurācijas nodrošinātāji** atlasiet **Jauns**.
4. Laukā **Nosaukums** ievadiet **Litware, Inc.**
5. Laukā **Interneta adrese** ievadiet `https://www.litware.com`.
6. Atlasiet **Saglabāt**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>ER konfigurācijas nodrošinātāja aktivizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.** un pēc tam atlasiet **Iestatīt kā aktīvu**.

Papildinformāciju par ER konfigurācijas nodrošinātājiem skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Standarta ER formāta konfigurāciju importēšana

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Standarta ER konfigurāciju importēšana

Lai pievienotu standarta ER konfigurācijas savai pašreizējai Microsoft Dynamics 365 Finance instancei, jums tās ir jāimportē no šai instancei konfigurētā ER [repozitorija](general-electronic-reporting.md#Repository).

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft** un pēc tam atlasiet **Repozitoriji**, lai skatītu Microsoft nodrošinātāja repozitoriju sarakstu.
3. Lapā **Konfigurācijas repozitoriji** atlasiet repozitoriju ar veidu **Globāls** un pēc tam atlasiet **Atvērt**. Ja tiek pieprasīta autorizācija savienojumam ar Regulatory Configuration Service, izpildiet autorizācijas norādījumus.
4. Lapā **Konfigurācijas repozitorijs** konfigurācijas koka skata kreisajā rūtī atlasiet **BACS (UK)** formāta konfigurāciju.
5. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER formāta konfigurācijas **1.1** versiju.
6. Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija uz pašreizējo Finance instanci.

![Konfigurācijas repozitorijas lapa.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Ja rodas problēmas ar piekļuvi [globālajam repozitorijam](er-download-configurations-global-repo.md), tā vietā varat [lejupielādēt konfigurācijas](download-electronic-reporting-configuration-lcs.md) no Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Importēto ER konfigurāciju pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis**.
4. Ņemiet vērā, ka papildus atlasītajam **BACS (UK)** ER formātam tika importētas arī citas nepieciešamās ER konfigurācijas. Pārliecinieties, vai konfigurācijas kokā ir pieejamas šādas ER konfigurācijas:

    - **Maksājuma modelis** — šajā konfigurācijā ir norādīts [datu modeļa](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponents, kas parāda maksājuma biznesa domēna datu struktūru.
    - **Maksājuma modeļa kartēšana 1611** — šajā konfigurācijā ir norādīta [modeļa kartēšana](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponentam, kas apraksta, kā datu modelis tiek aizpildīts ar programmas datiem izpildlaikā.
    - **BACS (UK)** — šajā konfigurācijā ir norādīts [formāts](general-electronic-reporting.md#FormatComponentOutbound) un formāta kartēšanas ER komponenti. Formāta komponents norāda atskaites izkārtojumu. Formāta kartēšanas komponents satur modeļa datu avotu un norāda, kā atskaites izkārtojums tiek aizpildīts, izmantojot šo datu avotu izpildlaikā.

![Lapa Konfigurācijas](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Kreditora maksājuma sagatavošana apstrādei

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Bankas informācijas pievienošana kreditora kontam

Kreditora kontam ir jāpievieno bankas informācija, kas vēlāk tiks norādīta reģistrētā maksājumā.

1. Dodieties uz **Kreditori** \> **Kreditori** \> **Visi kreditori**.
2. Lapā **Visi kreditori** atlasiet kreditora kontu **GB_SI_000001** un pēc tam darbību rūts cilnē **Kreditors** grupā **Iestatīt** atlasiet **Banku konti**.
3. Lapā **Kreditora banku konti** atlasiet **Jauns** un pēc tam ievadiet tālāk norādīto informāciju:

    1. Laukā **Bankas konts** ievadiet **GBP OPER**.
    2. Laukā **Bankas grupas** atlasiet **BankGBP**.
    3. Laukā **Bankas konta numurs** ievadiet **202015**.
    4. Laukā **SWIFT kods** ievadiet <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.
    5. Laukā **IBAN** ievadiet **GB33BUKB20201555555555**.
    6. Laukā **Reģistrācijas numurs** saglabājiet noklusējuma vērtību <a id="DefineRoutingNumber"></a>**123456**.

    ![Lapa Kreditora banku konti](./media/er-quick-start2-bank-account.png)

4. Atlasiet **Saglabāt**.
5. Aizvērt lapu.
6. Lapā **Visi kreditori** atveriet kreditora kontu **GB_SI_000001**.
7. Ja nepieciešams, lapā informācija par kreditoru atlasiet **Rediģēt**, lai lapu varētu rediģēt.
8. Kopsavilkuma cilnē **Maksājums**, laukā **Bankas konts** atlasiet **GBP OPER**.

    ![Lapa Informācija par kreditoru](./media/er-quick-start2-bank-account-reference.png)

9. Atlasiet **Saglabāt**.
10. Aizvērt lapu.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Kreditora maksājuma ievadīšana

Ir nepieciešams ievadīt jaunu kreditora maksājumu, izmantojot [maksājuma priekšlikumu](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).

1. Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.
2. Lapā **Kreditora maksājumu žurnāls** atlasiet **Jauns**.
3. Laukā **Nosaukums** atlasiet **VendPay**.
4. Atlasiet **Rindas**.
5. Atlasiet **Maksājuma priekšlikums** \> **Izveidot maksājuma priekšlikumu**.
6. Dialoglodziņā **Kreditora maksājuma priekšlikums** konfigurējiet nosacījumus, lai filtrētu tikai **GB_SI_000001** kreditora konta ierakstus, un pēc tam atlasiet **Labi**.
7. Atlasiet rindu rēķinam **00000007_Inv** un pēc tam atlasiet **Izveidot maksājumu**.

    ![Kreditora maksājuma priekšlikuma dialoglodziņš](./media/er-quick-start2-payment-proposal.png)

8. Pārbaudiet, vai ievadītais maksājums ir konfigurēts, lai izmantotu **elektroniska** maksājuma metodi.

    ![Kreditora maksājumu lapa](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Kreditora maksājuma apstrādāšana, izmantojot standarta ER formātu

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Elektroniskā maksājuma metodes iestatīšana

Elektroniskā maksājuma metode ir jākonfigurē, lai tā izmantotu importēto ER formāta konfigurāciju.

1. Dodieties uz **Kreditori** \> **Maksājuma iestatīšana** \> **Maksājuma metodes**.
2. Lapā **Maksājuma metodes – kreditori**, kreisajā rūtī atlasiet maksājuma metodi **Elektronisks**.
3. Atlasiet **Rediģēt**.
4. Kopsavilkuma cilnē **Faila formāti** iestatiet opciju **Vispārīgs elektroniskās eksportēšanas formāts** uz **Jā**.
5. Laukā **Eksporta formāta konfigurācija** atlasiet **BACS (UK)** formāta konfigurāciju.

    ![Lapa Maksājuma metodes – kreditori](./media/er-quick-start2-method-of-payment1.png)

6. Atlasiet **Saglabāt**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Kreditora maksājuma apstrādāšana

1. Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.
2. Lapā **Kreditora maksājumu žurnāls** atlasiet iepriekš pievienoto maksājumu žurnālu un pēc tam atlasiet **Rindas**.
3. Lapā **Kreditora maksājumi** atlasiet **Ģenerēt maksājumus**.
4. Dialoglodziņā **Ģenerēt maksājumus** ievadiet tālāk norādīto informāciju:

    - Laukā **Maksājuma metode** atlasiet **Elektronisks**.
    - Laukā **Bankas konts** atlasiet **GBSI OPER**.

5. Atlasiet **Labi**.
6. Dialoglodziņā **Elektronisko pārskatu parametri** iestatiet opciju **Drukāt kontroles pārskatu** uz **Jā** un pēc tam atlasiet **Labi**.

    ![Elektronisko pārskatu parametru dialoga lapa](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Papildus maksājuma failam tagad varat ģenerēt arī kontroles pārskatu.

7. Lejupielādējiet zip failu un pēc tam no tā izvelciet tālāk norādītos failus:

    - Kontroles pārskats Excel formātā
    - Maksājuma fails TXT formāta

        Ņemiet vērā, ka saskaņā ar sniegtā ER formāta [struktūru](#PositionRoutingNumber) maksājuma rinda ģenerētajā failā sākas ar reģistrācijas numuru, kas [definēts](#DefineRoutingNumber) konfigurētajam bankas kontam.

        ![Maksājuma fails TXT formāta](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Standarta ER formāta pielāgošana

Šajā sadaļā sniegtā piemēra ietvaros, jūs vēlaties izmantot korporācijas Microsoft nodrošinātās ER konfigurācijas, lai ģenerētu kreditora maksājumu failus BACS formātā, bet ir jāpievieno pielāgojums, lai atbalstītu noteiktas bankas prasības. Jūs vēlaties arī varēt jaunināt savu pielāgoto formātu, kad būs pieejamas jaunas ER konfigurāciju versijas. Tomēr jūs vēlaties veikt jaunināšanu ar pēc iespējas zemākām izmaksām.

Šādā gadījumā, kā Litware, Inc. pārstāvim, jums ir jāizveido (jāatvasina) jauna ER formāta konfigurācija, izmantojot Microsoft nodrošināto **BACS (UK)** konfigurāciju kā bāzi.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Pielāgota formāta izveidošana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **BACS (UK)**. Litware, Inc. izmantos šīs ER formāta konfigurācijas versiju 1.1 kā pielāgotās versijas bāzi.
3. Atlasiet **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu. Varat izmantot šo dialoglodziņu, lai izveidotu jaunu konfigurāciju pielāgotam maksājuma formātam.
4. Lauka grupā **Jauns** atlasiet opciju **Atvasināt no nosaukuma: BACS (UK), Microsoft**.
5. Laukā **Nosaukums** ievadiet **BACS (UK pielāgots)**.

    ![Izveidot konfigurācijas nolaižamo dialoglodziņu](./media/er-quick-start2-add-derived-format.png)

6. Atlasiet **Izveidot konfigurāciju**.

ER formāta konfigurācijas **BACS (UK pielāgots)** versija 1.1.1 ir izveidota. Šīs versijas [statuss](general-electronic-reporting.md#component-versioning) ir **Melnraksts** un to var rediģēt. Pielāgotā ER formāta pašreizējais saturs atbilst Microsoft nodrošinātā formāta saturam.

![Lapa Konfigurācijas](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Pielāgota formāta rediģēšana

Jums ir jākonfigurē pielāgotais formāts, lai tas atbilstu bankas noteiktajām prasībām. Piemēram, banka var pieprasīt, lai ģenerētie maksājumu faili ietver Vispasaules Starpbanku finanšu telekomunikāciju sabiedrības (SWIFT) kodu bankai, kurai tiek piešķirta aģenta loma apstrādātā kreditora maksājumā. SWIFT kodi ir starptautiski bankas kodi, kas identificē noteiktas bankas visā pasaulē. Tos sauc arī par banku identifikācijas kodiem (BIC). SWIFT kodam jābūt 11 rakstzīmes garam un tas ir jāievada ģenerētā maksājuma faila katras maksājuma rindas sākumā.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **BACS (UK pielāgots)**.
3. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās konfigurācijas **1.1.1** versiju.
4. Atlasiet **Noformētājs**.
5. Lapā **Formāta veidotājs** atlasiet **Rādīt detalizēti**, lai skatītu papildinformāciju par formāta elementiem.
6. Izvērsiet un pārskatiet šādus elementus:

    - Veids **Mape**, elements **BACSReportsFolder**. Šis elements tiek izmantots, lai ģenerētu izvadi ZIP formātā.
    - Veids **Fails**, elements **fails**. Šis elements tiek izmantots, lai ģenerētu maksājuma failu TXT formātā.
    - Veids **Secība**, elements **transakcijas**. Šis elements tiek izmantots, lai maksājuma failā ģenerētu vienu maksājuma rindu.
    - Veids **Secība**, elements **transakcija**. Šis elements tiek izmantots, lai viena maksājuma rindai ģenerētu atsevišķus laukus.

7. Atlasiet elementu **transakcija**.

    ![Transakcijas elements ER operāciju veidotājā](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Nodrošinātais pārskats ir konfigurēts, lai <a id="PositionRoutingNumber"></a>katra maksājuma rinda sākas ar bankas reģistrācijas numuru. Šim nolūkam tiek izmantots **vendBankRouteNum** formāta elements. 

8. Atlasiet **Pievienot** un pēc tam atlasiet **Teksts\\Virkne** formāta elementa veidu, kuru pievienojat:

    1. Laukā **Nosaukums** ievadiet **vendBankSWIFT**.
    2. Laukā **Minimālais garums** ievadiet **11**.
    3. Laukā **Maksimālais garums** ievadiet **11**.
    4. Atlasiet **Labi**.

    > [!NOTE]
    > Elements **vendBankSWIFT** tiks izmantots, lai ģenerētajos failos ievadītu kreditora bankas SWIFT kodu.

9. Formāta struktūras kokā atlasiet **vendBankSWIFT**.
10. Atlasiet **Pārvietot uz augšu**, lai pārvietotu atlasīto formāta elementu par vienu līmeni uz augšu. Atkārtojiet šo darbību, līdz **vendBankSWIFT** elements ir <a id="PositionSWIFTCode"></a>pirmais elements zem pamatelementa **transakcija**.

    ![VendBankSWIFT kā pirmais elements zem transakcijas ER operāciju veidotājā](./media/er-quick-start2-derived-format1.png)

11. Kamēr formāta struktūras kokā joprojām ir atlasīts **vendBankSWIFT**, atlasiet cilni **Kartēšana** un pēc tam izvērsiet **modeļa** datu avotu.
12. Izvērsiet **model.Payment** \> **model.Payment.CreditorAgent** un atlasiet datu avota lauku **model.Payment.CreditorAgent.BICFI**. Šis datu avota lauks atklāj tā kreditora bankas SWIFT kodu, kam tiek piešķirta aģenta loma apstrādātā kreditora maksājumā.
13. Atlasiet **Saistīt**. Formāta elements **vendBankSWIFT** tagad ir saistīts ar datu avota lauku **model.Payment.CreditorAgent.BICFI**, lai SWIFT kodi tiktu ievadīti ģenerētajos maksājuma failos.

    ![Formāta elements vendBankSWIFT saistīts ar datu avota lauku model.Payment.CreditorAgent.BICFI ER operāciju veidotājā](./media/er-quick-start2-derived-format2.png)

14. Atlasiet **Saglabāt**.
15. Aizveriet veidotāja lapu.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Pielāgota formāta atzīmēšana kā izpildāms

Tagad, kad ir izveidota pielāgotā formāta pirmā versija un tai ir statuss **Melnraksts**, varat to palaist testēšanas nolūkos. Lai palaistu pārskatu, kreditora maksājums ir jāapstrādā, izmantojot maksāšanas metodi, kas attiecas uz pielāgoto ER formātu. Pēc noklusējuma, izsaucot ER formātu no programmas, tiek [ņemtas vērā](general-electronic-reporting.md#component-versioning) tikai tās versijas, kuru statuss ir **Pabeigts** vai **Koplietots**. Šī darbība neļauj izmantot ER formātus, kuri nav pabeigti. Tomēr testējot, programmai var likt izmantot ER formāta versiju ar statusu **Melnraksts**. Šādā veidā var pielāgot pašreizējo formāta versiju, ja ir nepieciešamas kādas modifikācijas. Papildinformāciju skatiet sadaļā [Piemērojamība](electronic-reporting-destinations.md#applicability).

Lai izmantotu ER formāta melnraksta versiju, jums jāatzīmē ER formāts.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Palaist iestatījumus** uz **Jā** un pēc tam atlasiet **Labi**.
4. Atlasiet **Rediģēt**, lai pašreizējo lapu varētu rediģēt pēc nepieciešamības.
5. Konfigurācijas koka skata kreisajā rūtī atlasiet **BACS (UK pielāgots)**.
6. Iestatiet opciju **Palaist melnrakstu** uz **Jā**.

    ![Melnraksta opcijas palaišana lapā konfigurācijas](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Kreditora maksājuma apstrādāšana, izmantojot pielāgotu ER formātu

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Elektroniskā maksājuma metodes iestatīšana

Elektroniskā maksājuma metode ir jākonfigurē, lai pielāgotais ER formāts tiktu izmantots kreditora maksājumu apstrādei.

1. Dodieties uz **Kreditori** \> **Maksājuma iestatīšana** \> **Maksājuma metodes**.
2. Lapā **Maksājuma metodes – kreditori**, kreisajā rūtī atlasiet maksājuma metodi **Elektronisks**.
3. Atlasiet **Rediģēt**.
4. Kopsavilkuma cilnē **Faila formāts** iestatiet opciju **Vispārīgs elektroniskās eksportēšanas formāts** uz **Jā**.
5. Laukā **Eksporta formāta konfigurācija** atlasiet **BACS (UK pielāgots)** formāta konfigurāciju.

    ![Lapa Maksājuma metodes – kreditori](./media/er-quick-start2-method-of-payment2.png)

6. Atlasiet **Saglabāt**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Kreditora maksājuma apstrādāšana

1. Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.
2. Lapā **Kreditora maksājumu žurnāls** atlasiet iepriekš izveidoto maksājumu žurnālu.
3. Atlasiet **Rindas**.
4. Lapā **Kreditora maksājumi** virs režģa atlasiet **Maksājuma statuss** \> **Nav**.
5. Atlasiet **Ģenerēt maksājumu**.
6. Dialoglodziņā **Ģenerēt maksājumus** ievadiet tālāk norādīto informāciju:

    - Laukā **Maksājuma metode** atlasiet **Elektronisks**.
    - Laukā **Bankas konts** atlasiet **GBSI OPER**.

7. Atlasiet **Labi**.
8. Dialoglodziņā **Elektronisko pārskatu parametri** iestatiet opciju **Drukāt kontroles pārskatu** uz **Jā** un pēc tam atlasiet **Labi**.

    > [!NOTE]
    > Papildus maksājuma failam varat ģenerēt tikai kontroles pārskatu.

9. Lejupielādējiet zip failu un pēc tam no tā izvelciet tālāk norādītos failus:

    - Kontroles pārskats Excel formātā
    - Maksājuma fails TXT formāta

        Ņemiet vērā, ka saskaņā ar pielāgotā ER formāta struktūru, maksājuma rinda ģenerētajā failā tagad [sākas](#PositionSWIFTCode) ar SWIFT kodu, kas tika [ievadīts](#DefineSWIFTCode) kreditora bankas kontam, kura maksājums ir apstrādāts.

        ![Maksājuma fails TXT formāta](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Jaunas standarta ER formāta konfigurācijas versijas importēšana

Šajā sadaļā sniegtā piemēra ietvaros, jūs saņemat ziņojumu par zināšanu bāzes rakstu [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). Šis paziņojums informē par Microsoft publicētu jaunu **BACS (UK)** ER formāta versiju. Papildus kontroles pārskatam, šī jaunā versija ļauj lietotājiem ģenerēt maksājuma izziņas pārskatu un dalības piezīmes pārskatu, kamēr kreditora maksājums tiek apstrādāts. Noteikti izmēģiniet šo funkcionalitāti.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Jaunas standarta ER konfigurācijas versijas importēšana

Lai ER konfigurācijas jaunās versijas pievienotu pašreizējai Finance instancei, jums tās ir jāimportē no konfigurētā ER [repozitorija](general-electronic-reporting.md#Repository).

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft** un pēc tam atlasiet **Repozitoriji**, lai skatītu Microsoft nodrošinātāja repozitoriju sarakstu.
3. Lapā **Konfigurācijas repozitoriji** atlasiet repozitoriju ar veidu **Globāls** un pēc tam atlasiet **Atvērt**. Ja tiek pieprasīta autorizācija savienojumam ar Regulatory Configuration Service, izpildiet autorizācijas norādījumus.
4. Lapā **Konfigurācijas repozitorijs** konfigurācijas koka skata kreisajā rūtī atlasiet **BACS (UK)** formāta konfigurāciju.
5. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER formāta konfigurācijas **3.3** versiju.
6. Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija uz pašreizējo Finance instanci.

![Konfigurācijas repozitorijas lapa.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Ja rodas problēmas ar piekļuvi [globālajam repozitorijam](er-download-configurations-global-repo.md), tā vietā varat [lejupielādēt konfigurācijas](download-electronic-reporting-configuration-lcs.md) no LCS.

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Importētās ER formāta konfigurācijas pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **BACS (UK)**.
4. Kopsavilkuma cilnē **Versijas** atlasiet versiju **3.3**.
5. Atlasiet **Noformētājs**.
6. Lapā **Formāta veidotājs** izvērsiet formāta elementu **BACSReportsFolder**.
7.  Ņemiet vērā, ka versija 3.3 ietver formāta elementu **PaymentAdviceReport**, kas tiek izmantots, lai ģenerētu maksājuma izziņas pārskatu, apstrādājot kreditora maksājumu.

    ![PaymentAdviceReport formāta elements ER operāciju veidotājā](./media/er-quick-start2-imported-solution2.png)

8. Aizveriet veidotāja lapu.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Importētā formāta jaunās versijas izmaiņu pieņemšana pielāgotajā formātā

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Pielāgotā formāta pašreizējās melnraksta versijas pabeigšana

Ja vēlaties saglabāt pašreizējo pielāgotā formāta stāvokli, pabeidziet melnraksta versiju 1.1.1, mainot statusu no **Melnraksts** uz **Pabeigts**.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis**, izvērsiet **BACS (UK)** un pēc tam atlasiet **BACS (UK pielāgots)**.
4. Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** \> **Pabeigts** un pēc tam atlasiet **Labi**.

Versijas 1.1.1 statuss tiek mainīts no **Melnraksts** uz **Pabeigts** un versija kļūst tikai lasāma. Ir pievienota jauna rediģējama versija, 1.1.2, un tās statuss ir **Melnraksts**. Varat izmantot šo versiju, lai veiktu turpmākās izmaiņas pielāgotajā ER formātā.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Pielāgotā formāta pārvietošana uz jaunu bāzes versiju

Lai pielāgojumam sāktu izmantot jauno versijas 3.3 formāta funkcionalitāti **BACS (UK)**, ir jāmaina pielāgotās konfigurācijas **BACS (UK pielāgots)** bāzes konfigurācijas versija. Šis process tiek saukts par [pārbāzēšanu](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase). 1.1 **BACS (UK)** versijas vietā, izmantojiet 3.3 versiju.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **BACS (UK pielāgots)**.
3. Kopsavilkuma cilnē **Versijas** atlasiet versiju **1.1.2** un pēc tam atlasiet **Pārveidot**.
4. Dialoglodziņā **Pārveidošana** laukā **Mērķa versija** atlasiet bāzes konfigurācijas versiju **3.3**, lai to lietotu kā jauno bāzi, un izmantotu, lai atjauninātu konfigurāciju.

    ![Dialoglodziņš Pārskatīt](./media/er-quick-start2-rebase1.png)

5. Atlasiet **Labi**.
6. Ņemiet vērā, ka melnraksta versijas numurs ir mainīts no **1.1.2** uz **3.3.2**, lai atspoguļotu izmaiņas bāzes versijā.

    Sapludinot pielāgotu versiju un jaunu bāzes versiju, var tikt konstatēti konflikti formāta izmaiņu dēļ, ko nevar sapludināt automātiski.

    ![Pārveidota konfigurācija ar konfliktiem lapā Konfigurācijas](./media/er-quick-start2-rebase2.png)

    Ja tiek konstatēti konflikti, tie ir manuāli jāatrisina formāta veidotājā.

7. Kopsavilkuma cilnē **Versijas** atlasiet versiju **3.3.2**.
8. Atlasiet **Noformētājs**.
9. Lapā **Formāta veidotājs** kopsavilkuma cilnē **Detalizēti** atlasiet pārveides konflikta ierakstu un pēc tam atlasiet **Lietot bāzes vērtību**.

    ![Pārveides konflikta ieraksts ER operāciju veidotājā](./media/er-quick-start2-rebase3.png)

10. Atlasiet **Saglabāt**.

    Pārveides konflikta ierakstam vairs nevajadzētu parādīties kopsavilkuma cilnē **Detalizēti**.

    ![Konflikts atrisināts ER operāciju veidotājā](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Konflikts tika atrisināts, apstiprinot, ka bāzes modeļa 3. versija ir jālieto šajā ER formātā.

11. Izvērsiet **BACSReportsFolder** \> **fails** \> **transakcijas** \> **transakcija**.
12. Ņemiet vērā, ka cilnē **Kartēšana** jūsu pielāgotā ER formāta versija 3.3.2 ietver gan pielāgojumu (formāta elementu **vendBankSWIFT** un tā saistījumu), gan bāzes ER formāta versijas 3.3 jauno funkcionalitāti, ko nodrošina Microsoft (formāta elementu **PaymentAdviceReport** kopā ar tā ligzdotajiem elementiem un konfigurētajiem saistījumiem). Veicot dažus peles klikšķus, esat pieņēmis jaunas bāzes versijas modifikācijas, sapludinot tās ar pielāgojumu.

    ![Sapludināts formāts ER operāciju veidotājā](./media/er-quick-start2-rebase5.png)

13. Aizveriet veidotāja lapu.

> [!NOTE]
> Pārveides darbība ir atgriezeniska. Lai atceltu pārveidi, atlasiet formāta **BACS (UK pielāgots)** versiju **1.1.1** kopsavilkuma cilnē **Versijas** un pēc tam atlasiet **Iegūt šo versiju**. Versija 3.3.2 tiks pārnumurēta par 1.1.2 un melnraksta versijas 1.1.2 saturs atbildīs versijas 1.1.1 saturam.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Kreditora maksājuma apstrādāšana, izmantojot pārveidotu ER formātu

1. Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.
2. Lapā **Kreditora maksājumu žurnāls** atlasiet iepriekš izveidoto maksājumu žurnālu.
3. Atlasiet **Rindas**.
4. Lapā **Kreditora maksājumi** virs režģa atlasiet **Maksājuma statuss** \> **Nav**.
5. Atlasiet **Ģenerēt maksājumu**.
6. Dialoglodziņā **Ģenerēt maksājumus** ievadiet tālāk norādīto informāciju:

    - Laukā **Maksājuma metode** atlasiet **Elektronisks**.
    - Laukā **Bankas konts** atlasiet **GBSI OPER**.

7. Atlasiet **Labi**.
8. Dialoglodziņā **Elektronisko pārskatu parametri** ievadiet tālāk norādīto informāciju:

    - Iestatiet opciju **Drukāt kontroles pārskatu** uz **Jā**.
    - Iestatiet opciju **Drukāt maksājuma izziņu** uz **Jā**.

    ![Dialoglodziņš Elektronisko pārskatu parametri](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Papildus maksājuma failam tagad varat ģenerēt gan kontroles pārskatu, gan maksājuma izziņas pārskatu.

9. Atlasiet **Labi**.
10. Lejupielādējiet zip failu un pēc tam no tā izvelciet tālāk norādītos failus:

    - Kontroles pārskats Excel formātā
    - Maksājuma izziņas pārskats Excel formātā

        ![Maksājuma izziņas pārskats Excel formātā](./media/er-quick-start2-payment-advice-report.png)

    - Maksājuma fails TXT formāta

        Ņemiet vērā, ka maksājuma rinda ģenerētajā failā sākas ar SWIFT kodu, kas tika ievadīts kreditora bankas kontam, kura maksājums ir apstrādāts.

        ![Maksājuma fails TXT formāta](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [ER konfigurāciju lejupielāde no Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [ER konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]