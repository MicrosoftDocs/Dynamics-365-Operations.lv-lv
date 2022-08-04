---
title: Iespējot pamatdatu uzmeklēšanu nodokļu aprēķina konfigurācijai
description: Šajā rakstā skaidrots, kā iestatīt un iespējot nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181130"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Iespējot pamatdatu uzmeklēšanu nodokļu aprēķina konfigurācijai 

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt un iespējot nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti. Nolaižamajā sarakstā ir iespējams atlasīt **vērtības** nodokļu aprēķina konfigurācijā tādiem laukiem kā Juridiska persona, **Kreditora** konts, **Krājuma kods** un **Piegādes termiņš**. Šīs vērtības ir no savienotās Microsoft Dynamics 365 Finanšu vides, izmantojot Microsoft Dataverse datu avotu.

> [!NOTE] 
> Nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāte ir izvēles funkcionalitāte. Ja atspējojat nodokļu pakalpojuma datu avotu atbalsta līdzekli regulēšanas **konfigurācijas Dataverse** pakalpojumā (RCS), varat izlaist tālāk norādītās darbības. Tomēr šādā gadījumā nolaižamais saraksts nebūs pieejams nodokļu aprēķina konfigurācijā.

Lai iespējotu nolaižamo sarakstu nodokļu aprēķina līdzekļu versijas konfigurācijā, veiciet šādus soļus:

1. [Microsoft Power Platform Aktivizējiet integrāciju un atveriet Dataverse vidi.](#enable)
2. [Instalē finanšu un operāciju virtuālās entītijas.](#install)
3. [Azure Active Directory Reģistrēt ()Azure AD pieteikumu.](#register)
4. [Piešķiriet programmas atļaujas finanšu un operāciju programmām.](#grant)
5. [Konfigurējiet virtuālā elementa datu avotu.](#configure)
6. [Iespējot Dataverse virtuālos elementus.](#virtual)
7. [Iestatiet pievienoto pieteikumu nodokļu aprēķinam.](#set-up)
8. [Importējiet un iestatiet modeļa Dataverse kartēšanas konfigurāciju.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a> Aktivizēt Microsoft Power Platform integrāciju un atvērt Dataverse vidi

Finanšu un operāciju programmu integrēšanu Microsoft Power Platform var iespējot, izveidojot jaunu finanšu un operāciju programmu Microsoft Dynamics vidi pakalpojumā Lifecycle Services (LCS). Papildinformāciju skatiet sadaļā [Microsoft Power Platform integrācija - Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Kad vides nosaukums ir pabeigts, tas Microsoft Power Platform tiks rādīts integrācijas **Power Platform** sadaļā.

1. Finanšu un operāciju vidē LCS sadaļā **Power Platform** **Integrācija** atrodiet un pierakstiet vides nosaukuma vērtību saistītajā vidē.

    [![Vides nosaukuma vērtība.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. [Power Platform Administrēšanas](https://admin.powerplatform.microsoft.com/environments) centrā **cilnē** Vides atlasiet vidi, kas atbilst vides **nosaukuma vērtībai**, par kuru piekritāt.
3. **Lapā Detalizēta informācija** atrodiet vides **URL** vērtību videi Dataverse. Atzīmējiet šo vērtību, jo jums tā būs jāveic [7. solī. Iestatiet pievienoto pieteikumu nodokļu aprēķinam](#set-up).
4. Pārliecinieties, vai varat atvērt vidi Dataverse jūsu pārlūkprogrammā, atlasot Vides **URL** vērtību.

    [![Dataverse vides lapa.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Saglabājiet Dataverse vidi atvērtu jūsu pārlūkprogrammā. Tas būs nepieciešams [5. solī. Konfigurējiet virtuālā elementa datu avotu](#configure).

Papildinformāciju skatiet sadaļā [Aktivizēt Microsoft Power Platform integrāciju](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a> Instalēt finanšu un operāciju virtuālos elementus

No Dataverse virtuālā elementa risinājuma ir jāinstalē finanšu un operāciju virtuālo Microsoft AppSource elementu risinājums.

1. Atrast AppSource Finanšu un operāciju [virtuālo elementu](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Izvēlieties **Iegūt to tūlīt**.
3. Laukā **Vides atlase** ievadiet vides **nosaukuma vērtību**, kuru iepriekš atzīmējāt.
4. Atzīmējiet izvēles rūtiņas un pēc tam atlasiet **Instalēt**.

Kad instalēšana ir pabeigta, **·**[Power Platform](https://admin.powerplatform.microsoft.com/) finanšu un operāciju virtuālās entītijas programmu varat atrast administrēšanas centrā, **sadaļā Resursu** \> **Dynamics 365 programmas.**

Papildinformāciju skatiet virtuālās [entītijas risinājuma iegūšanai](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a> Pieteikuma Azure AD reģistrēšana

Jums jāreģistrē pieteikums Azure AD tam pašam nomniekam, kas ir finanšu un operāciju programmas, lai tos varētu izsaukt Dataverse.

1. Azure portālā [atveriet sadaļu Programmu](https://portal.azure.com)**Azure Active Directory reģistrācijas \>.**
2. Atlasiet **Jauna reģistrācija** un ievadiet šādu informāciju:

    - **Nosaukums** – ievadiet unikālu nosaukumu.
    - **Konta tips** - ievadiet **direktoriju Azure AD** (viens nomnieks vai vairāk nomnieks).
    - **URI virzienmaiņa** - atstājiet šo lauku tukšu.

3. Atlasiet **Reģistrēt**.
4. Pierakstiet **Lietojumprogrammas (klienta) ID** vērtību, jo tā būs nepieciešama vēlāk.

    [![Azure AD Programmas (klienta) ID vērtība.](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Izveidojiet programmai simetrisku atslēgu.
6. Jaunajā programmā atlasiet Sertifikāti **&noslēpumus**.
7. Atlasiet **Jauns klienta noslēpums**.
8. Ievadiet aprakstu, atlasiet beigu datumu un pēc tam atlasiet **Saglabāt**. Tiks izveidota un rādīta atslēga. Kopējiet vērtību vēlākai lietošanai.

Papildinformāciju skatiet sadaļā [Pieteikuma Azure AD reģistrēšana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a> Piešķirt programmas atļaujas finanšu un operāciju programmās

Dataverse programma <a0 Azure AD /> izmanto jūsu izveidoto programmu, lai izsauktu finanšu un operāciju programmas. Tāpēc programmai jābūt uzticamai finanšu un operāciju programmām un saistītai ar lietotāja kontu, kuram ir atbilstošas tiesības. Finanšu un operāciju programmās jums ir jāizveido speciāls pakalpojuma lietotājs, kuram ir tiesības **tikai** virtuālās entītijas funkcionalitātei. Šim pakalpojuma lietotājam nav jābūt ar citām tiesībām. Pēc šīs darbības veikšanas jebkura lietojumprogramma, kas ir jūsu izveidotās lietojumprogrammas noslēpums, Azure AD varēs izsaukt finanšu un operāciju lietojumprogrammu vidi un piekļūt virtuālās entītijas funkcionalitātei.

1. Jūsu vidē dodieties uz Sistēmas **administrēšanas** \> **lietotāju** \> **lietotājiem**.
2. Atlasiet **Jauns**, lai pievienotu jaunu lietotāju, un ievadiet šādu informāciju:

    - **Lietotāja ID** - ievadiet **datu šķērssadalījumu** vai citu vērtību.
    - **Lietotājvārds** – ievadiet datu **apgriezto integrāciju** vai citu vērtību.
    - **Nodrošinātājs** - iestatiet šo lauku kā **NonAAD**.
    - **E-pasts** - ievadiet **datu šķērsošanu** vai citu vērtību. (Vērtībai nav jābūt derīgam e-pasta kontam.)

3. Piešķiriet **lietotājam CDS virtuālā** elementa programmas drošības lomu.
4. Noņemt visas pārējās lomas, tostarp **Sistēmas lietotāju**.
5. Lai reģistrētu **, pārejiet uz** \> **sadaļu** \> **Azure Active Directory Sistēmas administrēšanas** iestatīšanas programmas.Dataverse 
6. Pievienojiet rindu un pēc tam **laukā Klienta ID** **ievadiet programmas (klienta) ID** vērtību, par kuru iepriekš atzīmējāt.
7. Laukā **Nosaukums** ievadiet nosaukumu. Piemēram, ievadiet **Dataverse Integrāciju**.
8. Laukā **Lietotāja ID** ievadiet lietotāja ID, ko izveidojāt agrāk.

Papildinformāciju skatiet programmu [atļauju piešķiršana finanšu un operāciju programmās](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Virtuālo elementu datu avota konfigurēšana

Savienojumam ir Dataverse jānorāda finanšu un operāciju programmas instance.

1. Jūsu Dataverse videi joprojām jābūt atvērtai jūsu pārlūkprogrammā no [1. soļa. Microsoft Power Platform Aktivizējiet integrāciju un atveriet Dataverse vidi](#enable). Augšējā labajā stūrī atlasiet pogu Iestatījumi (ātrumkārbas simbols) un pēc tam atlasiet Papildu **iestatījumi**.

    [![Atver papildu iestatījumus Dataverse vidē.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. Izvēlnē Iestatījumi **atlasiet Administrēšana** **.**

    [![Pārvalde.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Atlasiet **virtuālā elementa datu avotus**.

    [![Virtuālā elementa datu avoti.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Atlasiet datu avotu ar nosaukumu Finanses **un operācijas**.

    [![Finanšu un operāciju datu avots.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Ievadiet šādu informāciju no iepriekšējiem soļiem:

    - **Mērķa URL** – ievadiet URL, kur varat piekļūt finanšu un operāciju programmām.
    - **OAuth URL —** ievadiet `https://login.windows.net/`.
    - **Nomnieka ID** – norādiet savu nomnieku. Šī vērtība var būt jūsu uzņēmuma e-pasta domēna nosaukums (piemēram, contoso.com).
    - **AAD programmas ID** — ievadiet iepriekš **izveidotās programmas (klienta) ID** vērtību.
    - **AAD programmas noslēpums** - ievadiet noslēpumu, kas tika ģenerēts agrāk.
    - **AAD resurss** — ievadiet **00000015-0000-0000-c000-000000000000**. Šī vērtība ir programma Azure AD, kas pārstāv finanšu un operāciju programmas. Tai vienmēr jābūt tādai pašai vērtībai.

6. Saglabājiet izmaiņas.
7. Aizveriet lapu, lai atgrieztos administrēšanas **lapā**, kur sāksiet [6. soli. Iespējot Dataverse virtuālos elementus](#virtual).

    [![Elementa slēgšana labošanai.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Papildinformāciju skatiet virtuālā [elementa datu avota konfigurēšana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a> Iespējot Dataverse virtuālos elementus

Pirms nodokļu aprēķina konfigurācijā to **patērēšanas** no finanšu un operāciju programmām virtuālo entītiju redzamībai ir jābūt iestatītai uz Jā.

> [!NOTE]
> Šo darbību var izlaist, iespējojot ar nodokļu aprēķinu saistītās virtuālās entītijas tikai ar vienu klikšķi [8. darbībā. Iestatiet pievienoto pieteikumu nodokļu aprēķinam](#import). Tomēr mēs iesakām manuāli iespējot vismaz vienu virtuālo entītiju, lai norādītu, ka savienojums starp finanšu un operāciju programmām un ir Dataverse labi izveidots.

1. Jūsu vidē Dataverse lapas Administrēšana **augšējā** labajā stūrī atlasiet filtra pogu (burtspīļa simbols).

    [![Filtra poga.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Loga Detalizētā **atrašana laukā Meklēt** atlasiet elementus **Pieejamās** finanses un **operācijas**.
3. Pievienot šādu noteikumu: Nosaukums **·** – Ietver **·** – **CompanyInfoEntity**. Pēc tam atlasiet **Rezultāti**.

    [![Detalizētās meklēšanas logs.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Meklēšanas **rezultātos atlasiet CompanyInfoEntity**, atzīmējiet izvēles **rūtiņu** Redzams un pēc tam atlasiet **Saglabāt**.

    [![Elementa redzamības iestatīšana.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Atkārtojiet iepriekšējās darbības tālāk minētajiem elementiem, kas attiecas uz nodokļu aprēķina konfigurāciju:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Tikai pirmos 5000 Dataverse elementa ierakstus var izgūt un padarīt pieejamus nodokļu aprēķina konfigurācijas nolaižamajā sarakstā.

Plašāku informāciju skatiet sadaļā [Virtuālo Microsoft Dataverse elementu iespējošana](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a> Iestatīt pievienoto pieteikumu nodokļu aprēķinam

1. RcS atveriet līdzekļu pārvaldības darbalauku **un** iespējojiet šādas funkcijas:

    - Elektronisko pārskatu izrakstīšanas Dataverse datu avotu atbalsts
    - Nodokļu pakalpojuma Dataverse datu avotu atbalsts
    - Globalizācijas līdzekļi

2. Dodieties uz **Elektronisko pārskatu** izveide un pēc tam sadaļā **Saistītās saites** atlasiet Pievienotās **programmas**.

    [![pievienotos pieteikumus;](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. Atlasiet **Jauns**, lai pievienotu ierakstu, un ievadiet šādu informāciju.

    - **Nosaukums** – ievadiet nosaukumu.
    - **Veids** – atlasīt **Dataverse**.
    - **Lietojumprogramma** - Dataverse ievadiet vides vides URL **vērtību, kuru esiet veicis**(-usi) piezīmi [1. solī. Iespējojiet Microsoft Power Platform integrāciju un atveriet Dataverse vidi](#enable).
    - **Nomnieks** – ievadiet savu nomnieku.
    - **Pielāgots URL** - ievadiet Dataverse savu URL un pievienojiet **tam /api/data/v9.1**.

4. Atlasiet **Pārbaudīt savienojumu** un pēc tam parādītajā dialoglodziņā atlasiet Noklikšķiniet šeit, lai **izveidotu savienojumu ar atlasīto attālo programmu**.

    [![Pārbauda savienojumu.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. Pārliecinieties, ka esat saņēmis "Veiksmīgs" Ziņojums, kas norāda, ka savienojums tika izveidots veiksmīgi.

    [![Veiksmes ziņojums.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a> Modeļu kartēšanas konfigurācijas importēšana Dataverse un iestatīšana

Microsoft nodrošina noklusējuma modeļa kartēšanas konfigurācijas entītijām no finanšu un operāciju programmām līdz nodokļu aprēķinam.

1. RCS dodieties uz Elektronisko **pārskatu sniegšanu**.
2. **Sadaļā Konfigurācijas nodrošinātāji** Microsoft nodrošinātāja elementā **atlasiet** Repositories **·**.

    [![Krātuvēs.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Atlasiet globālās **konfigurācijas repozitorija** ierakstu un pēc tam atlasiet **Atvērt**.
4. Sadaļā **Nodokļu datu modeļa** \> **nodokļu aprēķina datu modelis** atlasiet modeļa kartēšanas **Dataverse** konfigurāciju.
5. Kopsavilkuma cilnē **Versijas** atlasiet versiju, kas atbilst finanšu un operāciju programmu versijai, un pēc tam atlasiet **Importēt**.

    [![Tiek importēta modeļa Dataverse kartēšanas konfigurācija.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > Modeļu **Dataverse kartēšanas** konfigurācija ir spēkā tikai tai augstākajā importētajā versijā. Tādēļ jūs nedrīkstat importēt modeļa **Dataverse** kartēšanas konfigurācijas versiju, kas ir augstāka nekā nodokļu aprēķina konfigurācijas versija, ko plānojat ieviest. Piemēram, ja plānojat ieviest nodokļu 40.50.225 konfigurācijas versiju, jāimportē tikai modeļa kartēšanas konfigurācijas versija 40.50.13 **Dataverse**. Nedrīkst importēt versiju 40.54.14. Pretējā gadījumā konfigurācijā būs datu modeļu neatbilstība.

6. Atgriezieties elektronisko **pārskatu veidošanas** sadaļā un atlasiet **elementu Nodokļu** konfigurācijas.
7. Atlasiet importēto modeļa **Dataverse kartēšanas** konfigurāciju un pēc tam atlasiet **Rediģēt**.
8. Iestatiet opciju **Noklusējums modeļu kartēšanai** kā **Jā**.
9. Saistītā **programmas** laukā atlasiet pievienoto programmu, kas iestatīta [7. darbībā. Iestatiet pievienoto pieteikumu nodokļu aprēķinam](#set-up).
10. Iestatiet opciju Iestatīt **virtuālās tabulas** redzamību kā **Jā**, lai visiem ar nodokļu aprēķiniem saistītiem virtuālajiem elementiem iestatītu kā redzamus.

Tagad ir pabeigta pamatdatu uzmeklēšanas funkcionalitātes iestatīšana. Nolaižamajā sarakstā tādiem laukiem kā Juridiska persona, Kreditora konts, **·** **·** **Krājuma** kods un Piegādes termiņš no Dynamics 365 Finanses **tagad tiks iespējots Nodokļu aprēķina līdzekļa versijas iestatījumā.** **·**

[![Juridiskas personas nolaižamais saraksts.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
