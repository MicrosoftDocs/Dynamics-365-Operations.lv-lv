---
title: Instalēt krājumu uztveramības pievienojumprogrammu
description: Šajā rakstā ir aprakstīts, kā instalēt krājumu redzamības pievienojumprogrammu korporācijai Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c08568b14d7f5c79a1d3609107a88f905498ce2b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762786"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility instalēšana un iestatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā instalēt krājumu redzamības pievienojumprogrammu korporācijai Microsoft Dynamics 365 Supply Chain Management.

Jums ir jāizmanto [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/v2), lai instalētu krājumu redzamības pievienojumprogrammu. Lifecycle Services ir sadarbības portāls, kas nodrošina vidi un regulāri atjauninātu pakalpojumu kopu, kas palīdz pārvaldīt jūsu finanšu un operāciju programmu lietojumprogrammu dzīves ciklu. Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Ieteicams pievienoties krājumu redzamības pievienojumprogrammas lietotāju grupai, kur varat atrast noderīgus ceļvežus, saņemt jaunākos atjauninājumus un publicēt visus iespējamos jautājumus par krājumu pārskatāmības izmantošanu. Lai pievienotos, lūdzu, nosūtiet e-pastu krājumu redzamības produktu komandai vietnē [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) un iekļaujiet savu Supply Chain Management vides ID.

## <a name="inventory-visibility-prerequisites"></a>Krājumu redzamības priekšnosacījumi

Pirms instalējat Krājumu redzamību, jums ir jārīkojas šādi:

- Iegūstiet Lifecycle Services ieviešanas projektu, kurā ir izvietota vismaz viena vide.
- Pārliecinieties, ka pievienojumprogrammu iestatīšanas priekšnoteikumi ir pabeigti. Plašāku informāciju par šiem priekšnosacījumiem skatiet [Pievienojumprogrammu pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Krājumu redzamībai nav nepieciešama dubultās rakstīšanas saistīšana.

> [!NOTE]
> Pašlaik atbalstītas valstis un reģioni: Kanāda (CCA, ECA), ASV (WUS, EUS), Eiropas Savienība (NEU, WEU), Apvienotā Karaliste (SUK, WUK), Austrālija (EAU, SEAU), Japāna (EJP, WJP) un Brazīlija (SBR, SCUS).

Ja jums ir kādi jautājumi par šiem priekšnosacījumiem, lūdzu, sazinieties ar Krājumu redzamības preču darba grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Instalēt krājumu uztveramības pievienojumprogrammu

Pirms pievienojumprogrammas instalēšanas reģistrējiet programmu un pievienojiet klienta slepeno informāciju Azure Active Directory (Azure AD) jūsu Azure abonementā. Norādījumus skatiet sadaļā [Pieteikuma reģistrēšana](/azure/active-directory/develop/quickstart-register-app) un [Klienta slepenās informācijas pievienošana](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Pierakstiet **lietojumprogrammas (klienta) ID, Klienta slepenā** klienta ID un **nomnieka ID** **vērtības**, jo tās būs nepieciešamas vēlāk.

> [!IMPORTANT]
> Ja jums ir vairākas Lifecycle Services vides, izveidojiet atšķirīgu Azure AD lietojumprogrammu katrai no tām. Ja izmantojat vienu un to pašu lietojumprogrammas ID un nomnieka ID, lai instalētu krājumu redzamības pievienojumprogrammu dažādām vidēm, vecākām vidēm radīsies marķiera problēma. Tā rezultātā būs derīga tikai pēdējā instalācija.

Pēc pieteikuma reģistrēšanas un klienta noslēpuma pievienošanas Azure AD izpildiet šīs darbības, lai instalētu Krājumu redzamības pievienojumprogrammu.

1. Piesakieties Lifecycle [Services](https://lcs.dynamics.com/Logon/Index).
1. Sākumlapā atlasiet projektu, kurā tiek izvietota jūsu vide.
1. Projekta lapā atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.
1. Vides lapā ritiniet uz leju, līdz redzat sadaļu **Vides pievienojumprogrammas** sadaļā **Power Platform integrācija**. Tad varat atrast Dataverse vides nosaukumu. Apstipriniet, ka Dataverse vides nosaukums ir tas, ko vēlaties izmantot Krājumu redzamībai.

    > [!NOTE]
    > Pašlaik tiek atbalstītas tikai Dataverse tās vides, kas izveidotas, izmantojot Lifecycle Services. Ja jūsu Dataverse vide tika izveidota kādā citā veidā (piemēram, izmantojot administrēšanas PowerApps centru) un ja tā ir saistīta ar jūsu Supply Chain Management vidi, pirms krājumu redzamības pievienojumprogrammas instalēšanas vispirms ir jānovērš kartēšanas problēma.
    >
    > Iespējams, ka jūsu duālās rakstīšanas vide ir saistīta ar instanci, Dataverse bet Lifecycle Services nav iestatīta integrācijai Power Platform. Šī saistīšanas neatbilstība var izraisīt negaidītu rīcību. Ieteicams dzīves cikla pakalpojumu vides detalizētai informācijai atbilst tam, ar ko esat izveidojis savienojumu, izmantojot dubulto rakstīšanu, lai vienu un to pašu savienojumu varētu izmantot biznesa notikumi, virtuālās tabulas un pievienojumprogrammas. Informāciju par kartēšanas problēmas novēršanu skatiet rakstā [Neatbilstības](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch) saistīšana. Kad kartēšanas problēma ir novērsta, varat turpināt instalēt krājumu redzamību.

1. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.

    ![Vides lapa sadaļā Lifecycle Services](media/inventory-visibility-environment.png "Vides lapa sadaļā Lifecycle Services")

1. Atlasiet saiti **Instalēt jaunu pievienojumprogrammu**. Tiek atvērts pieejamo pievienojumprogrammu saraksts.
1. Atlasiet no saraksta **Krājuma redzamība**.
1. Iestatiet savā vidē šādus laukus:

    - **AAD pieteikuma (klienta) ID** — ievadiet iepriekš izveidoto Azure AD pieteikuma klienta ID, kuru atzīmējāt.
    - **AAD nomnieka ID**: Ievadiet nomnieka ID, kuru iepriekš atzīmējāt.

    ![Pievienojumprogrammas iestatīšana lapā](media/inventory-visibility-setup.png "Pievienojumprogrammas iestatīšanas lapa")

1. Piekrist noteikumiem un nosacījumam, atlasot izvēles rūtiņu **Noteikumi un nosacījumi**.
1. Atlasiet **Instalēt**. Pievienojumprogrammas statuss tiks rādīts kā **Instalē**. Pēc tam, kad instalēšana ir pabeigta, atsvaidziniet lapu. Statusam ir jāmainās uz **Instalēts**.
1. Programmas Dataverse kreisās navigācijas rūtī izvēlieties sadaļu **Programmas** un pārbaudiet, vai **Krājumu redzamība** ir veiksmīgi instalēta Power Apps. Ja nav sadaļas **Programmas**, sazinieties ar Krājumu redzamības preču grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Ja sistēma brīdina, ka jums nav atļaujas instalēt krājumu redzamību Lifecycle Services, jums ir jāsazinās ar administratoru, lai modificētu savu atļauju.
>
> Ja instalēšana no dzīves cikla pakalpojumu lapas aizņem vairāk nekā stundu, iespējams, jūsu lietotāja kontam nav atļaujas instalēt risinājumus Dataverse vidē. Lai novērstu problēmu, veiciet tālāk norādītās darbības.
>
> 1. Atceliet krājumu redzamības pievienojumprogrammas instalēšanas procesu no dzīves cikla pakalpojumu lapas.
> 1. Piesakieties administrēšanas [Microsoft 365 centrā](https://admin.microsoft.com) un pārliecinieties, vai lietotāja kontam, kuru vēlaties izmantot pievienojumprogrammas instalēšanai, ir piešķirta licence "Plāns"Dynamics 365 Unified Operations. Ja nepieciešams, piešķiriet licenci.
> 1. Piesakieties administrēšanas centrā [Power Platform,](https://admin.powerplatform.microsoft.com) izmantojot attiecīgo lietotāja kontu. Pēc tam instalējiet krājumu redzamības pievienojumprogrammu, veicot šādas darbības:
>     1. Atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.
>     1. Atlasiet **Dynamics 365 programmas**.
>     1. Atlasiet **Instalēt lietotni**.
>     1. Atlasiet **Krājumu redzamība**
>
> 1. Kad instalēšana ir pabeigta, dodieties atpakaļ uz dzīves cikla pakalpojumu lapu un mēģiniet atkārtoti instalēt **krājumu redzamības** pievienojumprogrammu.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Inventory Visibility iestatīšana pakalpojumā Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Izvietot Krājumu redzamības integrācijas pakotni

Ja jūs palaidāt Supply Chain Management versiju 10.0.17 vai agrāk, sazinieties ar Krājumu redzamības standarta atbalsta komandu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu iepakojuma failu. Pēc tam izvietojiet pakotni Lifecycle Services.

> [!NOTE]
> Ja izvietošanas laikā rodas versiju neatbilstības kļūda, X++ projekts ir jāimportē manuāli izstrādes vidē. Pēc tam izveidojiet izvietojamu pakotni savā izstrādes vidē un izvietojiet to ražošanas vidē.
>
> Kods ir iekļauts Supply Chain Management versijā 10.0.18. Ja izmantojat šo versiju vai jaunāku, izvietošana nav nepieciešama.

Pārliecinieties, ka jūsu Supply Chain Management vidē ir ieslēgtas šādas funkcijas. (Pēc noklusējuma tie ir ieslēgti.)

| Līdzekļa apraksts | Koda versija | Pārslēgt klasi |
|---|---|---|
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSum tabulā      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSumDelta tabulā | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Pievienojumprogrammas Krājumu redzamība integrācijas iestatīšana

Kad pievienojumprogramma ir instalēta, sagatavojiet Supply Chain Management sistēmu darbam ar to, veicot tālāk norādītās darbības.

1. Pakalpojumā Supply Chain Management atveriet darbvietu **[Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** un iespējojiet šādus līdzekļus:
    - *Inventory Visibility integrācija* — obligāti.
    - *Inventory Visibility integrācija ar rezervāciju nobīdi* — ieteicama, bet ne obligāta. Vajadzīga 10.0.22. vai jaunāka versija. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Inventory Visibility integrācijas parametri**.
1. Atveriet cilni **Vispārīgi** un veiciet tālāk norādītos iestatījumus.
    - **Inventory Visibility gala punkts** — Ievadiet URL videi, kurā palaižat Inventory Visibility. Papildinformāciju skatiet rakstā [Atrast pakalpojuma galamērķi](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maksimālais ierakstu skaits vienā pieprasījumā** — Iestatīts uz maksimālo ierakstu skaitu, kuru ietvert vienā pieprasījumā. Ir jāievada pozitīvs veselais skaitlis, kas ir mazāks vai vienāds ar 1000. Noklusējuma vērtība ir 512. Stingri iesakām paturēt noklusējuma vērtību, ja vien neesat saņēmuši ieteikumi no Microsoft Support vai citu iemeslu dēļ neesat droši, ka tā ir jāmaina.

1. Ja iespējojāt neobligāto līdzekli *Inventory Visibility integrācija ar rezervāciju nobīdi*, atveriet cilni **Rezervāciju nobīde** un veiciet šādus iestatījumus:
    - **Iespējot rezervāciju nobīdi** — Iestatiet uz *Jā*, lai iespējotu šo funkcionalitāti.
    - **Rezervāciju nobīdes pārveidotājs** — Atlasiet krājuma transakcijas statusu, kas nobīdīs Inventory Visibility veiktās rezervācijas. Šis iestatījums nosaka pasūtījuma apstrādes posmu, kurš aktivizē nobīdes. Statusu izseko pasūtījuma krājumu darbības statuss. Izvēlieties kādu no šīm opcijām:
        - *Pasūtījumā* – statusam *On transaction* pasūtījums pēc izveidošanas nosūta korespondējošo pieprasījumu. Nobīžu daudzums būs izveidotā pasūtījuma daudzums.
        - *Rezervēšana* – Pasūtījuma statuss *Rezervēt pasūtītajā pasūtījumā* pēc tā rezervētā, izdotā, pavadzīmes grāmatošanas vai rēķina izrakstīšanas pasūtījums nosūta korespondējošo pieprasījumu. Pieprasījums tiks parādīts tikai vienu reizi, pirmajam solim, kad notiks iepriekš minētais process. Novīdes daudzums būs daudzums, kurā krājuma transakcijas statuss atbilstoŠajā pasūtījuma rindā tiek mainīts no *Pasūtījumā* uz *Rezervēts pasūtījums* (vai uz vēlāku statusu).

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie \> Krājumu redzamības integrāciju** un iespējojiet darbu. Visi krājumu izmaiņu notikumi no Supply Chain Management tagad tiks grāmatoti Krājumu redzamībai.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Atinstalēt Krājumu redzamības pievienojumprogrammu

Lai atinstalētu krājumu redzamības pievienojumprogrammu, rīkojieties šādi:

1. Pierakstieties Supply Chain Management.
1. Dodieties uz sadaļu **Krājumu pārvaldības \> periodiskās \> krājumu redzamības integrācija** un atspējojiet darbu.
1. Dodieties uz Lifecycle Services un atveriet tās vides lapu, kurā vēlaties atinstalēt pievienojumprogrammu (skatiet arī [Krājumu redzamības pievienojumprogrammas](#install-add-in) instalēšana).
1. Atlasiet **Atinstalēt**.
1. Atinstalēšanas process tagad pārtrauc krājumu redzamības pievienojumprogrammas darbību, atceļ pievienojumprogrammas reģistrāciju no Lifecycle Services un izdzēš visus pagaidu datus, kas tiek glabāti krājumu redzamības pievienojumprogrammas datu kešatmiņā. Tomēr primārie krājumu dati, kas tika sinhronizēti ar jūsu Dataverse abonementu, joprojām tiek glabāti tur. Lai izdzēstu šos datus, veiciet pārējo procedūru.
1. Atveriet [Power Apps](https://make.powerapps.com).
1. Navigācijas joslā atlasiet **Vide**.
1. Atlasiet vidi, Dataverse kas ir saistīta ar jūsu Lifecycle Services vidi.
1. Pārejiet uz Risinājumi **un** izdzēsiet tālāk norādītos risinājumus šādā secībā.
    1. Dynamics 365 krājumu redzamība — enkurs
    1. Dynamics 365 krājumu redzamība — spraudņi
    1. Dynamics 365 krājumu redzamība — lietojumprogramma
    1. Dynamics 365 krājumu redzamība — vadīklas
    1. Dynamics 365 krājumu redzamība — bāze 

    Pēc šo risinājumu dzēšanas arī tabulās saglabātie dati arī tiks dzēsti.

> [!NOTE]
> Ja pēc krājumu redzamības pievienojumprogrammas atinstalēšanas atjaunojat Supply Chain Management datu bāzi un pēc tam vēlaties atkārtoti instalēt pievienojumprogrammu, pirms pievienojumprogrammas atkārtotas instalēšanas pārliecinieties, vai esat izdzēsis vecos krājumu redzamības datus, kas ir saglabāti jūsu Dataverse abonementā (kā aprakstīts iepriekšējā procedūrā). Tas novērsīs datu neatbilstības problēmas, kas citādi varētu rasties.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a> Notīriet krājumu redzamības datus Dataverse pirms Supply Chain Management datu bāzes atjaunošanas

Ja esat izmantojis krājumu redzamību un pēc tam atjaunojis savu Supply Chain Management datu bāzi, atjaunotajā datu bāzē var būt dati, kas vairs neatbilst datiem, kurus krājumu redzamība iepriekš sinhronizēja ar Dataverse. Šī datu neatbilstība var izraisīt sistēmas kļūdas un citas problēmas. Tāpēc ir svarīgi, lai pirms Supply Chain Management datu bāzes atjaunošanas vienmēr notīrītu Dataverse visus krājumu redzamības datus.

Ja nepieciešams atjaunot Supply Chain Management datu bāzi, rīkojieties šādi:

1. Atinstalējiet krājumu redzamības pievienojumprogrammu un noņemiet visus saistītos datus Dataverse, kā aprakstīts sadaļā [Krājumu redzamības pievienojumprogrammas atinstalēšana](#uninstall-add-in)
1. Atjaunojiet savu Supply Chain Management datu bāzi, piemēram, kā aprakstīts sadaļā [Datu bāzes punkta atjaunošana (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) vai [Ražošanas datu bāzes punkta atjaunošana smilškastes vidē](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Ja joprojām vēlaties to izmantot, atkārtoti instalējiet un iestatiet krājumu redzamības pievienojumprogrammu, kā aprakstīts rakstā [Krājumu redzamības pievienojumprogrammas](#install-add-in) instalēšana un [Krājumu redzamības integrācijas iestatīšana](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
