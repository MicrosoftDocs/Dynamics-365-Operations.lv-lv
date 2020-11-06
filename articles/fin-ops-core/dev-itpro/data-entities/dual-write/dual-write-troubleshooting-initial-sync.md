---
title: Problēmu novēršana sākotnējās sinhronizēšanas laikā
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 4d0ca1fb4b7a4964194516544686b6bb7d26e76c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997330"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Problēmu novēršana sākotnējās sinhronizēšanas laikā

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, tajā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Sākotnējās sinhronizācijas kļūdu pārbaude Finance and Operations programmā

Kad iespējojat kartēšanas veidnes, karšu statusam jābūt **Palaists**. Ja statuss ir **Nav palaists** , sākotnējās sinhronizācijas laikā radušās kļūdas. Lai skatītu kļūdas, lapā **Duālais ieraksts** atlasiet cilni **Sākotnējās sinhronizācijas informācija**.

![Kļūda cilnē Sākotnējā sinhronizācijas informācija](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Sākotnējo sinhronizāciju nevar pabeigt: 400 nederīgs pieprasījums

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Mēģinot palaist kartēšanu un sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:

*(\[Nederīgs pieprasījums\], Attālais serveris atgrieza kļūdu: (400) nederīgs pieprasījums.), AX eksportējot radās kļūda*

Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma piemērs.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Ja šī kļūda rodas konsekventi un nevar pabeigt sākotnējo sinhronizāciju, veiciet tālāk norādītās darbības, lai novērstu šo problēmu.

1. Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).
2. Atveriet Microsoft pārvaldības konsoli.
3. Rūtī **Pakalpojumi** pārbaudiet, vai ir palaists Microsoft Dynamics 365 datu importēšanas eksporta struktūras pakalpojums. Ja tas ir apturēts, restartējiet to, jo tas tas ir nepieciešams sākotnējai sinhronizēšanai.

## <a name="initial-synchronization-error-403-forbidden"></a>Sākotnējās sinhronizācijas kļūda: 403 aizliegts

Sākotnējās sinhronizācijas laikā, iespējams, saņemsit šādu kļūdas ziņojumu:

*(\[Aizliegts\], Attālinātais serveris atgrieza kļūdu: (403) Aizliegts.), AX eksportējot radās kļūda*

Lai novērstu problēmu, izpildiet šīs darbības.

1. Piesakieties Finance and Operations programmā.
2. Lapā **Azure Active Directory programma** izdzēsiet klientu **DtAppID** un pēc tam pievienojiet to vēlreiz.

![DtAppID klients Azure AD programmu sarakstā](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Pašatsauces vai cirkulārās atsauces kļūmes sākotnējās sinhronizācijas laikā

Var tikt parādīts kļūdas ziņojums, ja kādam no kartējumiem ir pašatsauces vai cirkulārās atsauces. Kļūdas ietilpst tālāk minētajās kategorijās.

- [Kļūdas Kreditori V2-uz-msdyn_vendors elementa kartēšanā](#error-vendor-map)
- [Kļūdas Debitori V3-uz-kontiem elementa kartēšanā](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Atrisināt kļūdas Kreditori V2-uz-msdyn_vendors elementa kartēšanā

Jums var rasties sinhronizācijas kļūdas kartēšanā **Kreditori V2** uz **msdyn\_vendors** , ja elementos ir esoši ieraksti ar vērtībām laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**. Šīs kļūdas notiek tādēļ, ka **InvoiceVendorAccountNumber** ir pašatsauces lauks un **PrimaryContactPersonId** ir riņķveida atsauce kreditora kartēšanā.

Saņemtajiem kļūdu ziņojumiem būs šāda forma.

*Nevarēja atrisināt lauka GUID: \<field\>. Uzmeklēšana netika atrasta: \<value\>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Daži piemēri:

- *Nevarēja atrisināt lauka GUID: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Nevarēja atrisināt lauka GUID: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Uzmeklēšana netika atrasta: V24-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Ja jums ir jebkādi ieraksti kreditoru entītijā ar vērtībām laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** , izpildiet tālāk minētās darbības, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.

1. Programmā Finance and Operations izdzēsiet laukus **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** kartējumā un tad saglabājiet kartējumu.

    1. Duālā ieraksta kartēšanas lapā **Kreditori V2 (msdyn\_vendors)** cilnē **Elementa kartējumi** , kreisajā filtrā atlasiet **Finance and Operations apps.Vendors V2**. Labajā filtrā atlasiet **Pārdošana. Kreditors**.
    2. Meklējiet **primarycontactperson** , lai atrastu avota lauku **PrimaryContactPersonId**.
    3. Atlasiet **Darbības** un pēc tam atlasiet **Dzēst**.

        ![PrimaryContactPersonId lauka dzēšana](media/vend_selfref3.png)

    4. Atkārtojiet šos soļus, lai dzēstu lauku **InvoiceVendorAccountNumber**.

        ![InvoiceVendorAccountNumber lauka dzēšana](media/vend-selfref4.png)

    5. Saglabājiet jūsu izmaiņas kartējumā.

2. Izslēdziet izmaiņu izsekošanu elementam **Kreditors V2**.

    1. Darbvietā **Datu pārvaldība** atlasiet elementu **Datu elementi**.
    2. Atlasiet entītiju **Kreditori V2**.
    3. Darbību rūtī atlasiet **Opcijas** un pēc tam atlasiet **Mainīt izsekošanu**.

        ![Izmaiņu izsekošanas opcijas atlasīšana](media/selfref_options.png)

    4. Atlasiet **Atspējot izmaiņu izsekošanu**.

        ![Atspējot izmaiņu izsekošanu atlasīšana](media/selfref_tracking.png)

3. Palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori V2 (msdyn\_vendors)**. Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.
4. Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai. Jums ir jāsinhronizē šis kartējums, ja vēlaties sinhronizēt primāro kontaktpersonu lauku kreditoru elementā, tāpēc ka sākotnējā sinhronizācija jāveic arī kontaktu ierakstiem.
5. Pievienojiet **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** laukus atpakaļ kartēšanai **Kreditori V2 (msdyn\_vendors)** un tad saglabājiet kartējumu.
6. Vēlreiz palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori V2 (msdyn\_vendors)**. Visi ieraksti tiks sinhronizēti, jo izmaiņu izsekošana ir atspējota.
7. Vēlreiz ieslēdziet izmaiņu izsekošanu elementam **Kreditors V2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a>Novērst kļūdas elementa Debitori V3-uz-kontiem kartēšanā

Jums var rasties sinhronizācijas kļūdas kartēšanā **Debitori V3** uz **Konti** , ja elementos ir esoši ieraksti ar vērtībām laukos **ContactPersonID** un **InvoiceAccount**. Šīs kļūdas notiek tādēļ, ka **InvoiceAccount** ir pašatsauces lauks un **ContactPersonID** ir riņķveida atsauce kreditora kartēšanā.

Saņemtajiem kļūdu ziņojumiem būs šāda forma.

*Nevarēja atrisināt lauka GUID: \<field\>. Uzmeklēšana netika atrasta: \<value\>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Daži piemēri:

- *Nevarēja atrisināt lauka GUID: primarycontactid.msdyn\_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Nevarēja atrisināt lauka GUID: msdyn\_billingaccount.accountnumber. Uzmeklēšana netika atrasta: 1206-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Ja jums ir jebkādi ieraksti debitoru entītijā ar vērtībām laukos **ContactPersonID** un **InvoiceAccount** , izpildiet tālāk minētās darbības, lai sekmīgi pabeigtu sākotnējo sinhronizāciju. Varat izmantot šo pieeju jebkurām iebūvētajām entītijām, piemēram, **Uzņēmumiem** un **Kontaktpersonām**.

1. Programmā Finance and Operations izdzēsiet laukus **ContactPersonID** un **InvoiceAccount** no **Debitori V3 (konti)** kartēšanas un tad saglabājiet kartējumu.

    1. Duālā ieraksta kartēšanas lapā **Debitori V3 (konti)** , cilnē **Elementa kartējumi** , kreisajā filtrā atlasiet **Finance and Operations app.Customers V3**. Labajā filtrā atlasiet **Common Data Service.konts**.
    2. Meklējiet **kontaktpersonu** , lai atrastu avota lauku **ContactPersonID**.
    3. Atlasiet **Darbības** un pēc tam atlasiet **Dzēst**.

        ![ContactPersonID lauka dzēšana](media/cust_selfref3.png)

    4. Atkārtojiet šos soļus, lai dzēstu lauku **InvoiceAccount**.

        ![InvoiceAccount lauka dzēšana](media/cust_selfref4.png)

    5. Saglabājiet jūsu izmaiņas kartējumā.

2. Izslēdziet izmaiņu izsekošanu elementam **Debitori V3**.

    1. Darbvietā **Datu pārvaldība** atlasiet elementu **Datu elementi**.
    2. Atlasiet entītiju **Dabitori V3**.
    3. Darbību rūtī atlasiet **Opcijas** un pēc tam atlasiet **Mainīt izsekošanu**.

        ![Izmaiņu izsekošanas opcijas atlasīšana](media/selfref_options.png)

    4. Atlasiet **Atspējot izmaiņu izsekošanu**.

        ![Atspējot izmaiņu izsekošanu atlasīšana](media/selfref_tracking.png)

3. Palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai. Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.
4. Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai.

    > [!NOTE]
    > Ir divas kartes, kurām ir vienāds nosaukums. Pārliecinieties, ka izvēlaties karti ar sekojošu aprakstu cilnē **Detaļas** : **Duālā ieraksta veidne sinhronizācijai starp FO.CDS kreditora V2 kontaktpersonām un CDS.Contacts. Nepieciešama jauna pakotne \[Dynamics365SupplyChainExtended\].**

5. Pievienojiet laukus **InvoiceAccount** un **ContactPersonId** atpakaļ kartējumam **Debitori V3 (konti)** un tad saglabājiet kartējumu. Abi lauki **InvoiceAccount** un **ContactPersonId** atkal ir daļa no tiešsaistes sinhronizācijas režīma. Nākamajā darbībā veiciet sākotnējo sinhronizāciju šiem laukiem.
6. Vēlreiz palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai. Tā kā izmaiņu izsekošana ir izslēgta, tiks sinhronizēti dati **InvoiceAccount** un **ContactPersonId** no Finance and Operations programmas uz Common Data Service.
7. Lai sinhronizētu datus **InvoiceAccount** un **ContactPersonId** no Common Data Service uz Finance and Operations programmu, izmantojiet datu integrācijas projektu.

    1. Sistēmā Power Apps izveidojiet datu integrācijas projektu starp **Pārdošana.Konts** un **Finance and Operations apps.Customers V3** elementiem. Datu virzienam jābūt no Common Data Service uz programmu Finance and Operations. Tā kā **InvoiceAccount** ir jauns atribūts duālajā ierakstā, iespējams, vēlēsities izlaist sākotnējo sinhronizāciju tam. Papildinformāciju skatiet [Datu integrēšana pakalpojumā Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Šajā attēlā ir parādīts projekts, kas atjaunina **CustomerAccount** un **ContactPersonId**.

        ![Datu integrācijas projekts, lai atjauninātu CustomerAccount un ContactPersonId](media/cust_selfref6.png)

    2. Pievienojiet uzņēmuma kritērijus filtram Common Data Service pusē, lai tiktu atjaunināti tikai tie ieraksti, kas atbilst filtra kritērijiem programmā Finance and Operations. Lai pievienotu filtru, atlasiet filtra pogu. Tad dialoglodziņā **Rediģēt vaicājumu** varat pievienot filtra vaicājumu, piemēram, **\_msdyn\_company\_value eq '\<guid\>'**. 

        > [PIEZĪME] Ja filtra poga nav atrodama, izveidojiet atbalsta biļeti, lai lūgtu datu integrācijas grupai iespējot filtra iespēju jūsu nomniekam.

        Ja neievadāt filtra vaicājumu **\_msdyn\_company\_value** , visi ieraksti tiks sinhronizēti.

        ![Filtra vaicājuma pievienošana](media/cust_selfref7.png)

    Ierakstu sākotnējā sinhronizācija tagad ir pabeigta.

8. Programmā Finance and Operations vēlreiz iespējojiet izmaiņu izsekošanu elementā **Debitori V3**.
