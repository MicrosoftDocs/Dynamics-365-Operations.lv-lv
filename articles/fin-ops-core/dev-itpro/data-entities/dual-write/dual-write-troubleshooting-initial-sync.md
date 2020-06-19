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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410085"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Problēmu novēršana sākotnējās sinhronizēšanas laikā

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, tajā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Sākotnējās sinhronizācijas kļūdu pārbaude Finance and Operations programmā

Kad iespējojat kartēšanas veidnes, karšu statusam jābūt **Palaists**. Ja statuss ir **Nav palaists**, sākotnējās sinhronizācijas laikā radušās kļūdas. Lai skatītu kļūdas, lapā **Duālais ieraksts** atlasiet cilni **Sākotnējās sinhronizācijas informācija**.

![Sākotnējās sinhronizācijas detalizētas informācijas cilne](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Sākotnējo sinhronizāciju nevar pabeigt: 400 nederīgs pieprasījums

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Mēģinot palaist kartēšanu un sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:

*Attālais serveris atgrieza kļūdu: (400) nederīgs pieprasījums.), AX eksportējot radās kļūda*

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

![Azure AD pieteikumu saraksts](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Pašatsauces vai cirkulārās atsauces kļūmes sākotnējās sinhronizācijas laikā

Var tikt parādīts kļūdas ziņojums, ja kādam no kartējumiem ir pašatsauces vai cirkulārās atsauces. Kļūdas ietilpst tālāk minētajās kategorijās.

- [Kreditori V2 uz msdyn_vendors elementa kartējums](#error-vendor-map)
- [Debitoru V3 uz kontu elementu kartēšana](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Atrisiniet kļūdu kreditori V2 uz msdyn_vendors elementa kartēšanu

Jums var rasties tālāk minētās sinhronizācijas kļūdas kartēšanā **Kreditori V2** uz **msdyn_vendors**, ja elementos ir esoši ieraksti ar vērtībām laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**. Tas notiek tādēļ, ka **InvoiceVendorAccountNumber** ir pašatsauces lauks un **PrimaryContactPersonId** ir riņķveida atsauce kreditora kartēšanā.

*Nevarēja atrisināt lauka GUID: <field>. Uzmeklēšana netika atrasta: <value>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

Tākāk ir minēti daži piemēri.

- *Nevarēja atrisināt ceļvedi laukam: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Nevarēja atrisināt ceļvedi laukam: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Uzmeklēšana netika atrasta: 1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1*

Ja jums ir ieraksti ar vērtībām šajos laukos kreditora elementā, izpildiet tālāk minētās darbības, kas norādītas sadaļā zemāk, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.

1. Programmā Finance and Operations izdzēsiet laukus **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** kartējumā un saglabājiet izmaiņas.

    1. Dodieties uz duālā ieraksta kartēšanas lapu **Kreditori V2 (msdyn_vendors)** un atlasiet cilni **Elementa kartējumi**. Kreisajā filtrā atlasiet **Finance and Operations apps.Vendors V2**. Labajā filtrā atlasiet **Pārdošana. Kreditors**.

    2. Meklējiet **primarycontactperson**, lai atrastu avota lauku **PrimaryContactPersonId**.
    
    3. Noklikšķiniet uz pogas **Darbības** un atlasiet **Dzēst**.
    
        ![pašatsauce vai cinkulārā atsauce Nr. 3](media/vend_selfref3.png)
    
    4. Atkārtiet, lai dzēstu lauku **InvoiceVendorAccountNumber**.
    
        ![pašatsauce vai cinkulārā atsauce Nr. 4](media/vend-selfref4.png)
    
    5. Saglabājiet kartēšanas izmaiņas.

2. Atspējietot izmaiņu izsekošanu elementam **Kreditori V2**.

    1. Pārejiet uz **Datu pārvaldība \> datu entītijas**.
    
    2. Atlasiet entītiju **Kreditori V2**.
    
    3. Izvēļņu joslā noklikšķiniet uz **Opcijas** un pēc tam uz **Mainīt izsekošanu**.
    
        ![pašatsauce vai cinkulārā atsauce Nr. 5](media/selfref_options.png)
    
    4. Noklikšķiniet uz **Atspējot Mainīt izsekošanu**.
    
        ![pašatsauce vai cinkulārā atsauce Nr. 6](media/selfref_tracking.png)

3. Palaidiet sākotnējo **Kreditori v2 (msdyn_vendors)** kartēšanas sinhronizāciju. Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.

4. Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai. Jums ir jāsinhronizē šis kartējums, ja vēlaties sinhronizēt primāro kontaktpersonu lauku kreditoru elementā kā kontaktpersonu ierakstus, kuri arī sākotnēji ir jāsinhronizē.

5. Pievienojiet laukus **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** atpakaļ kartēšānai **Kreditori V2 (msdyn_vendors)** un saglabājiet kartējumu.

6. Palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori v2 (msdyn_vendors)**. Visi ieraksti tiks sinhronizēti, jo izmaiņu izsekošana ir atspējota.

7. Iespējietot izmaiņu izsekošanu elementam **Kreditors V2**.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Novērst kļūdu elementa Debitori V3 uz kontiem kartēšanā

Jums var rasties tālāk minētās sinhronizācijas kļūdas kartēšanā **Debitori V3** uz **Konti**, ja elementos ir esoši ieraksti ar vērtībām laukos **ContactPersonID** un **InvoiceAccount**. Tas notiek tādēļ, ka **InvoiceAccount** ir pašatsauces lauks un **ContactPersonID** ir riņķveida atsauce kreditora kartēšanā.

*Nevarēja atrisināt lauka GUID: <field>. Uzmeklēšana netika atrasta: <value>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Nevarēja atrisināt ceļvedi laukam: primarycontactid.msdyn_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Nevarēja atrisināt ceļvedi laukam: msdyn_billingaccount.accountnumber. Uzmeklēšana netika atrasta: 1206-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1*

Ja jums ir ieraksti ar vērtībām šajos laukos debitora elementā, izpildiet tālāk minētās darbības, kas norādītas sadaļā zemāk, lai sekmīgi pabeigtu sākotnējo sinhronizāciju. Varat izmantot šo pieeju jebkurām iebūvētajām entītijām, piemēram, uzņēmumiem un kontaktpersonām.

1. Programmā Finance and Operations izdzēsiet laukus **ContactPersonID** un **InvoiceAccount** no **Debitori V3 (konti)** kartēšanas un saglabājiet kartējumu.

    1. Dodieties uz duālā ieraksta kartēšanas lapu **Debitori V3 (konti)** un atlasiet cilni **Elementa kartējumi**. Kreisajā filtrā atlasiet **Finance and Operations app.Customers V3**. Labajā filtrā atlasiet **Common Data Service.konts**.

    2. Meklējiet **kontaktpersonu**, lai atrastu avota lauku **ContactPersonID**.
    
    3. Noklikšķiniet uz pogas **Darbības** un atlasiet **Dzēst**.
    
        ![pašatsauce vai cinkulārā atsauce Nr. 3](media/cust_selfref3.png)
    
    4. Atkārtojiet, lai dzēstu lauku **InvoiceAccount**.
    
        ![pašatsauce vai cinkulārā atsauce](media/cust_selfref4.png)
    
    5. Saglabājiet kartēšanas izmaiņas.

2. Atspējietot izmaiņu izsekošanu elementam **Debitori V3**.

    1. Pārejiet uz **Datu pārvaldība \> datu entītijas**.
    
    2. Atlasiet entītiju **Dabitori V3**.
    
    3. Izvēļņu joslā noklikšķiniet uz **Opcijas** un pēc tam uz **Mainīt izsekošanu**.
    
        ![pašatsauce vai cinkulārā atsauce Nr. 5](media/selfref_options.png)
    
    4. Noklikšķiniet uz **Atspējot Mainīt izsekošanu**.
    
        ![pašatsauce vai cinkulārā atsauce Nr. 6](media/selfref_tracking.png)

3. Palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai. Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.

4. Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai. Ir 2 kartes ar vienādu nosaukumu. Izvēlieties vienu ar aprakstu **Duālā ieraksta veidne sinhronizācijai starp FO.CDS kreditora V2 kontaktpersonām un CDS.Contacts. Nepieciešama jauna pakotne \[Dynamics365SupplyChainExtended\].** kartes cilnē **Detalizēta informācija**.

5. Pievienojiet laukus **InvoiceAccount** un **ContactPersonId** atpakaļ kartējumam **Debitori V3 (konti)** un saglabājiet kartējumu. Tagad abi laiki **InvoiceAccount** un **ContactPersonId** atkal ir daļa no tiešsaistes sinhronizācijas režīma. Nākamajā darbībā pabeidziet sākotnējo sinhronizāciju šiem laukiem.

6. Atkal palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai. Tā kā izmaiņu izsekošana ir atspējota, palaižot sinhronizāciju, tiks sinhronizēti dati **InvoiceAccount** un **ContactPersonId** no Finance and Operations programmas uz Common Data Service.

7. Lai sinhronizētu datus **InvoiceAccount** un **ContactPersonId** no Common Data Service uz Finance and Operations, izmantojiet datu integrācijas projektu.

    1. Sistēmā Power Apps izveidojiet datu integrācijas projektu starp **Pārdošana.Konts** un **Finance and Operations apps.Customers V3** elementiem. Datu virzienam jābūt no Common Data Service uz programmu Finance and Operations.  Tā kā **InvoiceAccount** ir jauns atribūts duālajā ierakstā, iespējams, vēlēsities izlaist sākotnējo sinhronizāciju šim atribūtam. Papildinformāciju skatiet [Datu integrēšana pakalpojumā Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Šajā attēlā ir parādīts projekts, kas atjaunina **CustomerAccount** un **ContactPersonId**.

        ![pašatsauce vai cinkulārā atsauce](media/cust_selfref6.png)

    2. Pievienojiet uzņēmuma kritērijus filtram Common Data Service pusē, jo programmā tiks atjaunināti tikai tie ieraksti, kas atbilst filtra kritērijiem programmā Finance and Operations. Lai pievienotu filtru, noklikšķiniet uz filtra ikonas. Dialoglodziņā **Rediģēt vaicājumu** varat pievienot filtra vaicājumu, piemēram, **_msdyn_company_value eq '\<guid\>'**. Ja filtra ikona nav atrodama, izveidojiet atbalsta biļeti, lai lūgtu datu integrācijas grupai iespējot filtra iespēju jūsu nomniekam. Ja neievadāt filtra vaicājumu **_msdyn_company_value**, visi ieraksti tiek sinhronizēti.

        ![pašatsauce vai cinkulārā atsauce](media/cust_selfref7.png)

        Tas pabeidz ierakstu sākotnējo sinhronizāciju.

8. Iespējojiet izmaiņu izsekošanu elementam **Debitori V3** programmā Finance and Operations.

