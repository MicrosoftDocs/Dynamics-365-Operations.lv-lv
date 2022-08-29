---
title: Problēmu novēršana sākotnējās sinhronizēšanas laikā
description: Šajā rakstā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt novērst problēmas, kas var rasties sākotnējās sinhronizācijas laikā.
author: RamaKrishnamoorthy
ms.date: 06/24/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d9d74eea90cc2dfca2d5decf6e5cd1d7f52da2a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289490"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Problēmu novēršana sākotnējās sinhronizēšanas laikā

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir sniegta traucējummeklēšanas informācija par dubulto rakstīšanas integrāciju starp finanšu un operāciju programmām un Dataverse. Konkrēti, tajā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.

> [!IMPORTANT]
> Dažas no problēmām, kurām šajā rakstu adresēs var būt nepieciešama sistēmas administratora loma vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Pārbaudīt sākotnējās sinhronizācijas kļūdas finanšu un operāciju programmā

Kad iespējojat kartēšanas veidnes, karšu statusam jābūt **Palaists**. Ja statuss ir **Nav palaists**, sākotnējās sinhronizācijas laikā radušās kļūdas. Lai skatītu kļūdas, lapā **Duālais ieraksts** atlasiet cilni **Sākotnējās sinhronizācijas informācija**.

![Kļūda cilnē Sākotnējā sinhronizācijas informācija.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Sākotnējo sinhronizāciju nevar pabeigt: 400 nederīgs pieprasījums

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Mēģinot palaist kartēšanu un sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:

*(\[Nederīgs pieprasījums\], attālais serveris atgrieza kļūdu: (400) nederīgs pieprasījums.), AX eksportējot radās kļūda.*

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

1. Piesakieties virtuālajā mašīnā (VM) finanšu un operāciju programmai.
2. Atveriet Microsoft pārvaldības konsoli.
3. Rūtī **Pakalpojumi** pārbaudiet, vai ir palaists Microsoft Dynamics 365 datu importēšanas eksporta struktūras pakalpojums. Ja tas ir apturēts, restartējiet to, jo tas tas ir nepieciešams sākotnējai sinhronizēšanai.

## <a name="initial-synchronization-error-403-forbidden"></a>Sākotnējās sinhronizācijas kļūda: 403 aizliegts

Sākotnējās sinhronizācijas laikā, iespējams, saņemsit šādu kļūdas ziņojumu:

*(\[Aizliegts\], Attālinātais serveris atgrieza kļūdu: (403) Aizliegts.), AX eksportējot radās kļūda*

Lai novērstu problēmu, izpildiet šīs darbības.

1. Pieteikties finanšu un operāciju programmā.
2. Lapā **Azure Active Directory programma** izdzēsiet klientu **DtAppID** un pēc tam pievienojiet to vēlreiz.

![DtAppID klients Azure AD programmu sarakstā.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Pašatsauces vai cirkulārās atsauces kļūmes sākotnējās sinhronizācijas laikā

Var tikt parādīts kļūdas ziņojums, ja kādam no kartējumiem ir pašatsauces vai cirkulārās atsauces. Kļūdas ietilpst tālāk minētajās kategorijās.

- [Kļūdas Kreditori V2-uz-msdyn_vendors tabulas kartēšanā](#error-vendor-map)
- [Kļūdas Debitori V3-uz-kontiem tabulas kartēšanā](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Atrisināt kļūdas Kreditori V2-uz-msdyn_vendors tabulas kartēšanā

Jums var rasties sinhronizācijas kļūdas kartēšanā **Kreditori V2** uz **msdyn\_vendors**, ja tabulās ir esošas rindas ar vērtībām laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**. Šīs kļūdas notiek tādēļ, ka **InvoiceVendorAccountNumber** ir pašatsauces kolonna un **PrimaryContactPersonId** ir riņķveida atsauce kreditora kartēšanā.

Saņemtajiem kļūdu ziņojumiem būs šāda forma.

*Nevarēja atrisināt lauka GUID: \<field\>. Uzmeklēšana netika atrasta: \<value\>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Daži piemēri:

- *Nevarēja atrisināt lauka GUID: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Nevarēja atrisināt lauka GUID: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Uzmeklēšana netika atrasta: V24-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Ja jebkādām rindām kreditora elementā ir vērtības kolonnās **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**, izpildiet tālāk minētās darbības, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.

1. Finanšu un operāciju programmā no kartēšanas izdzēsiet **PrimaryContactPersonId** **un InvoiceVendorAccountNumber** kolonnas un pēc tam saglabājiet kartējumu.

    1. Dubultās rakstīšanas **kartēšanas lapā kreditoriem V2 (msdpapīrs\_, kreditori)** **·** **cilnes Tabulu kartēšana kreisajā filtrā atlasiet finanšu un operāciju programmas. Kreditori V2**. Labajā filtrā atlasiet **Pārdošana. Kreditors**.
    2. Meklējiet **primarycontactperson**, lai atrastu avota kolonnu **PrimaryContactPersonId**.
    3. Atlasiet **Darbības** un pēc tam atlasiet **Dzēst**.

        ![PrimaryContactPersonId kolonnas dzēšana.](media/vend_selfref3.png)

    4. Atkārtojiet šos soļus, lai dzēstu kolonnu **InvoiceVendorAccountNumber**.

        ![InvoiceVendorAccountNumber kolonnas dzēšana.](media/vend-selfref4.png)

    5. Saglabājiet jūsu izmaiņas kartējumā.

2. Izslēdziet izmaiņu izsekošanu tabulai **Kreditors V2**.

    1. Darbvietā **Datu pārvaldība** atlasiet elementu **Datu tabulas**.
    2. Atlasiet tabulu **Kreditori V2**.
    3. Darbību rūtī atlasiet **Opcijas** un pēc tam atlasiet **Mainīt izsekošanu**.

        ![Izmaiņu izsekošanas opcijas atlasīšana.](media/selfref_options.png)

    4. Atlasiet **Atspējot izmaiņu izsekošanu**.

        ![Atspējot izmaiņu izsekošanu atlasīšana.](media/selfref_tracking.png)

3. Palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori V2 (msdyn\_vendors)**. Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.
4. Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai. Jums ir jāsinhronizē šis kartējums, ja vēlaties sinhronizēt primāro kontaktpersonu kolonnu kreditoru tabulā, tāpēc ka sākotnējā sinhronizācija jāveic arī kontaktu rindām.
5. Pievienojiet **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** kolonnas atpakaļ kartēšanai **Kreditori V2 (msdyn\_vendors)** un tad saglabājiet kartējumu.
6. Vēlreiz palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori V2 (msdyn\_vendors)**. Visas rindas tiks sinhronizētas, jo izmaiņu izsekošana ir atspējota.
7. Vēlreiz ieslēdziet izmaiņu izsekošanu tabulai **Kreditors V2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Novērst kļūdas rindas Debitori V3-uz-kontiem kartēšanā

Jums var rasties sinhronizācijas kļūdas kartēšanā **Debitori V3** uz **Konti**, ja tabulās ir esošas rindas ar vērtībām kolonnās **ContactPersonID** un **InvoiceAccount**. Šīs kļūdas notiek tādēļ, ka **InvoiceAccount** ir pašatsauces kolonna un **ContactPersonID** ir riņķveida atsauce kreditora kartēšanā.

Saņemtajiem kļūdu ziņojumiem būs šāda forma.

*Nevarēja atrisināt lauka GUID: \<field\>. Uzmeklēšana netika atrasta: \<value\>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Daži piemēri:

- *Nevarēja atrisināt lauka GUID: primarycontactid.msdyn\_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Nevarēja atrisināt lauka GUID: msdyn\_billingaccount.accountnumber. Uzmeklēšana netika atrasta: 1206-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Ja jebkādām rindām debitora tabulā ir vērtības kolonnās **ContactPersonID** un **InvoiceAccount**, izpildiet tālāk minētās darbības, lai sekmīgi pabeigtu sākotnējo sinhronizāciju. Varat izmantot šo pieeju jebkurām iebūvētajām tabulām, piemēram, **Uzņēmumi** un **Kontaktpersonas**.

1. Finanšu un operāciju programmā izdzēsiet **kolonnas ContactPersonID** **un InvoiceAccount** **no kartēšanas Debitori V3 (konti)** un pēc tam saglabājiet kartējumu.

    1. **Klientu V3 (kontu)** **dubultās rakstīšanas** kartēšanas lapas cilnes Tabulu kartēšana kreisajā filtrā atlasiet finanšu **un operāciju programmu. Debitori V3**. Labajā filtrā atlasiet **Dataverse.konts**.
    2. Meklējiet **kontaktpersonu**, lai atrastu avota kolonnu **ContactPersonID**.
    3. Atlasiet **Darbības** un pēc tam atlasiet **Dzēst**.

        ![ContactPersonID kolonnas dzēšana.](media/cust_selfref3.png)

    4. Atkārtojiet šos soļus, lai dzēstu kolonnu **InvoiceAccount**.

        ![InvoiceAccount kolonnas dzēšana.](media/cust_selfref4.png)

    5. Saglabājiet jūsu izmaiņas kartējumā.

2. Izslēdziet izmaiņu izsekošanu tabulai **Debitori V3**.

    1. Darbvietā **Datu pārvaldība** atlasiet elementu **Datu tabulas**.
    2. Atlasiet tabulu **Dabitori V3**.
    3. Darbību rūtī atlasiet **Opcijas** un pēc tam atlasiet **Mainīt izsekošanu**.

        ![Izmaiņu izsekošanas opcijas atlasīšana.](media/selfref_options.png)

    4. Atlasiet **Atspējot izmaiņu izsekošanu**.

        ![Atspējot izmaiņu izsekošanu atlasīšana.](media/selfref_tracking.png)

3. Palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai. Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.
4. Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai.

    > [!NOTE]
    > Ir divas kartes, kurām ir vienāds nosaukums. Pārliecinieties, ka izvēlaties karti ar sekojošu aprakstu cilnē **Detaļas**: **Duālā ieraksta veidne sinhronizācijai starp FO.CDS kreditora V2 kontaktpersonām un CDS.Contacts. Nepieciešama jauna pakotne \[Dynamics365SupplyChainExtended\].**

5. Pievienojiet kolonnas **InvoiceAccount** un **ContactPersonId** atpakaļ kartējumam **Debitori V3 (konti)** un tad saglabājiet kartējumu. Abas kolonnas **InvoiceAccount** un **ContactPersonId** atkal ir daļa no tiešsaistes sinhronizācijas režīma. Nākamajā darbībā veiciet sākotnējo sinhronizāciju šīm kolonnām.
6. Vēlreiz palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai. Tā kā izmaiņu izsekošana ir izslēgta, data for **InvoiceAccount** **un ContactPersonId** tiks sinhronizēti no finanšu un operāciju programmas uz Dataverse.
7. Lai sinhronizētu **InvoiceAccount un** **ContactPersonId** Dataverse datus no finanšu un operāciju programmas, jāizmanto datu integrācijas projekts.

    1. Power Apps Veidojiet datu integrācijas projektu starp Sales.Account **un** finanšu un **operāciju programmām. Debitoru V3 tabulas**. Datu virzienam jābūt no finanšu Dataverse un operāciju programmas. Tā kā **InvoiceAccount** ir jauns atribūts duālajā ierakstā, iespējams, vēlēsities izlaist sākotnējo sinhronizāciju tam. Papildinformāciju skatiet [Datu integrēšana pakalpojumā Dataverse](/power-platform/admin/data-integrator).

        Šajā attēlā ir parādīts projekts, kas atjaunina **CustomerAccount** un **ContactPersonId**.

        ![Datu integrācijas projekts, lai atjauninātu CustomerAccount un ContactPersonId.](media/cust_selfref6.png)

    2. Pievienojiet filtram uzņēmuma kritērijus, lai Dataverse finanšu un operāciju programmā tiktu atjauninātas tikai tās rindas, kas atbilst filtra kritērijiem. Lai pievienotu filtru, atlasiet filtra pogu. Tad dialoglodziņā **Rediģēt vaicājumu** varat pievienot filtra vaicājumu, piemēram, **\_msdyn\_company\_value eq '\<guid\>'**.

        > [PIEZĪME] Ja filtra poga nav atrodama, izveidojiet atbalsta biļeti, lai lūgtu datu integrācijas grupai iespējot filtra iespēju jūsu nomniekam.

        Ja neievadāt filtra vaicājumu **\_msdyn\_company\_value**, visas rindas tiks sinhronizētas.

        ![Filtra vaicājuma pievienošana.](media/cust_selfref7.png)

    Rindu sākotnējā sinhronizācija tagad ir pabeigta.

8. Finanšu un operāciju programmā mainiet debitoru V3 tabulas izmaiņu **izsekošanu** atpakaļ.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Sākotnējās sinhronizācijas kļūmes kartēs ar vairāk nekā 10 uzmeklēšanas laukiem

Varat saņemt šādu kļūdas ziņojumu, mēģinot palaist sākotnējās sinhronizācijas kļūmes **Debitori V3 (konti)**, **Pirkšanas pasūtījumi** kartēšanā vai jebkurā kartēšanā ar vairāk nekā 10 uzmeklēšanas laukiem:

*CRMExport: pakotnes izpilde pabeigta. Kļūdas apraksts: 5 nesekmīgi mēģinājumi iegūt datus no https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc.*

Tā kā vaicājumā ir norādīti uzmeklēšanas ierobežojumi, sākotnējā sinhronizācija neizdodas, ja elementa kartēšanā ir vairāk par 10 uzmeklējumiem. Papildinformāciju skatiet rakstā [Saistīto tabulas ierakstu izgūšana ar vaicājumu](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Lai novērstu šo problēmu, veiciet tālāk minētās darbības.

1. Noņemiet izvēles uzmeklēšanas laukus no dubultā ieraksta elementu kartes, lai uzmeklēšanas skaits būtu 10 vai mazāk.
2. Saglabājiet karti un veiciet sākotnējo sinhronizāciju.
3. Kad pirmā soļa sākotnējā sinhronizācija ir veiksmīga, pievienojiet atlikušos uzmeklēšanas laukus un noņemiet uzmeklēšanas laukus, kas ir sinhronizēti pirmajā darbībā. Pārliecinieties, ka uzmeklēšanas lauku skaits ir 10 vai mazāk. Saglabājiet karti un veiciet sākotnējo sinhronizāciju.
4. Atkārtojiet šīs darbības, līdz visi uzmeklēšanas lauki tiek sinhronizēti.
5. Pievienojiet kartē visus uzmeklēšanas laukus, saglabājiet karti un palaidiet karti ar **Izlaist sākotnējo sinhronizāciju**.

Šis process iespējo karti tiešsaistes sinhronizācijas režīmam.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Zināmā problēma puses pasta adrešu un puses elektronisko adrešu sākotnējās sinhronizēšanas laikā

Mēģinot palaist puses pasta adrešu un puses elektronisko adrešu sākotnējo kodu, iespējams, saņemsit šādu kļūdas ziņojumu:

*Puses numurs nav atrasts pakalpojumā Dataverse.*

Finanšu un operāciju programmās **DirPartyCDSEntity** ir iestatīts diapazons, kas filtrē personas un **organizācijas tipa** **puses**. Tāpēc sākotnējā sinhronizācija **CDS puses – msdyn_parties** kartēšanā nesinhronizēs citu veidu puses, tostarp **Juridiska persona** un **Pārvaldības struktūrvienība**. Ja sākotnējā sinhronizācija tiek palaista **CDS pušu pasta adresēm (msdyn_partypostaladdresses)** vai **pušu kontaktinformācijai V3 (msdyn_partyelectronicaddresses)**, iespējams, tiks saņemts kļūdas ziņojums.

Mēs strādājam pie labojuma, lai noņemtu pušu tipu diapazonu finanšu un operāciju entītijā, lai puses ar visiem tipiem varētu veiksmīgi sinhronizēt Dataverse.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Vai, izpildot sākotnējo sinhronizāciju debitoriem vai kontaktpersonu datiem, ir veiktspējas problēmas?

Ja veicāt sākotnējo sinhronizāciju **debitoru** datiem un veicāt **klientu** kartēšanu, kā arī pēc tam veicāt sākotnējo sinhronizāciju **kontaktpersonu** datiem, ievietošanas un atjaunināšanas laikā var būt veiktspējas problēmas ar **LogisticsPostalAddress** un **LogisticsElectronicAddress** tabulām **kontakpersonu** adresēm. Tādas pašas globālās pasta adreses un elektronisko adrešu tabulas tiek izsekotas **CustCustomerV3Entity** un **VendVendorV2Entity** un duālā ieraksta mēģinājumiem, lai veidotu vairāk vaicājumu, lai rakstītu datus citā pusē. Ja jau esat izpildījis sākotnējo sinhronizāciju **debitoram**, apturiet atbilstošo karti, kad tiek izpildīta **kontaktpersonu** datu sākotnējā sinhronizācija. Veiciet to pašu ar **kreditoru** datiem. Kad sākotnējā sinhronizācija ir pabeigta, jūs varat palaist visas kartes, izlaižot sākotnējo sinhronizāciju.

## <a name="float-data-type-that-has-a-zero-value-cant-be-synchronized"></a>Nevar sinhronizēt peldošo datu tipu, kam ir nulles vērtība

Sākotnējā sinhronizācija var neizdoties ierakstiem, kuru cenas lauka vērtība ir nulle, piemēram, **fiksēta maksājuma** summa **vai** Summa darbības valūtā. Šajā gadījumā saņemsit kļūdas ziņojumu, kas līdzīgs šim piemēram:

*Radās kļūda, validējot ievades parametrus: Microsoft.OData.ODataException: nevar pārveidot literāļa '000000' paredzēto tipu 'Edm. Decimāldaļskaitļu,...*

Problēma ir ar valodas lokalizācijas **vērtību** avota datu **formātos** datu **pārvaldības modulī**. Mainiet lauka Valodas atrašanās **vietas vērtību** uz **En-Us**, un pēc tam mēģiniet vēlreiz.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

