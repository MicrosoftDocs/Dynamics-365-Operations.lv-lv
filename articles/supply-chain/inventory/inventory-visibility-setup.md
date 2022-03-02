---
title: Instalēt krājumu uztveramības pievienojumprogrammu
description: Šajā tēmā ir aprakstīts, kā instalēt Krājumu redzamības pievienojumprogrammu programmā Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a49f35211f30cdb76104cc5be78f5b114320a228
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062654"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility instalēšana un iestatīšana

[!include [banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā instalēt Krājumu redzamības pievienojumprogrammu programmā Microsoft Dynamics 365 Supply Chain Management.

Lai instalētu Krājumu uztveramības pievienojumprogrammu, izmantojot Microsoft Dynamics Lifecycle Services (LCS). LCS ir sadarbības portāls, kas nodrošina vides un regulāri atjauninātu pakalpojumu kopu, kas palīdz pārvaldīt jūsu Finance and Operations programmu dzīves ciklu.

Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Krājumu redzamības priekšnosacījumi

Pirms instalējat Krājumu redzamību, jums ir jārīkojas šādi:

- Iegūt LCS ieviešanas projektu, kurā ir izvietota vismaz viena vide.
- Pārliecinieties, ka pievienojumprogrammu iestatīšanas priekšnoteikumi ir pabeigti. Plašāku informāciju par šiem priekšnosacījumiem skatiet [Pievienojumprogrammu pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Krājumu redzamībai nav nepieciešama dubultās rakstīšanas saistīšana.

> [!NOTE]
> Pašlaik atbalstītas valstis un reģioni: Kanāda (CCA, ECA), ASV (WUS, EUS), Eiropas Savienība (NEU, WEU), Apvienotā Karaliste (SUK, WUK), Austrālija (EAU, SEAU), Japāna (EJP, WJP) un Brazīlija (SBR, SCUS).

Ja jums ir kādi jautājumi par šiem priekšnosacījumiem, lūdzu, sazinieties ar Krājumu redzamības preču darba grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Instalēt krājumu uztveramības pievienojumprogrammu

Pirms pievienojumprogrammas instalēšanas reģistrējiet programmu un pievienojiet klienta slepeno informāciju Azure Active Directory (Azure AD) jūsu Azure abonementā. Norādījumus skatiet sadaļā [Pieteikuma reģistrēšana](/azure/active-directory/develop/quickstart-register-app) un [Klienta slepenās informācijas pievienošana](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Noteikti atzīmējiet **Programmas (klienta) ID**, **Klienta slepeno informāciju** un **Nomnieka ID** vērtības, jo jums tās būs nepieciešamas vēlāk.

Pēc pieteikuma reģistrēšanas un klienta noslēpuma pievienošanas Azure AD izpildiet šīs darbības, lai instalētu Krājumu redzamības pievienojumprogrammu.

1. Pierakstieties [LCS](https://lcs.dynamics.com/Logon/Index).
1. Sākumlapā atlasiet projektu, kurā tiek izvietota jūsu vide.
1. Projekta lapā atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.
1. Vides lapā ritiniet uz leju, līdz redzat sadaļu **Vides pievienojumprogrammas** sadaļā **Power Platform integrācija**. Tad varat atrast Dataverse vides nosaukumu. Apstipriniet, ka Dataverse vides nosaukums ir tas, ko vēlaties izmantot Krājumu redzamībai.

    > [!NOTE]
    > Pašlaik tiek atbalstītas tikai Dataverse vides, kas izveidotas, izmantojot LCS. Ja jūsu Dataverse vide tika izveidota citādi (piemēram, izmantojot Power Apps administrēšanas centru) un ja tā ir saistīta ar Supply Chain Management vidi, vispirms ir jāsazinās ar Krājumu redzamības produktu grupu, lai novērstu kartēšanas problēmu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Tad instalējiet Krājumu uztveramības pievienojumprogrammu.

1. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.

    ![Vides lapa portālā LCS](media/inventory-visibility-environment.png "Vides lapa portālā LCS")

1. Atlasiet saiti **Instalēt jaunu pievienojumprogrammu**. Tiek atvērts pieejamo pievienojumprogrammu saraksts.
1. Atlasiet no saraksta **Krājuma redzamība**.
1. Iestatiet savā vidē šādus laukus:

    - **AAD pieteikuma (klienta) ID** — ievadiet iepriekš izveidoto Azure AD pieteikuma klienta ID, kuru atzīmējāt.
    - **AAD nomnieka ID**: Ievadiet nomnieka ID, kuru iepriekš atzīmējāt.

    ![Pievienojumprogrammas iestatīšana lapā](media/inventory-visibility-setup.png "Pievienojumprogrammas iestatīšanas lapa")

1. Piekrist noteikumiem un nosacījumam, atlasot izvēles rūtiņu **Noteikumi un nosacījumi**.
1. Atlasiet **Instalēt**. Pievienojumprogrammas statuss tiks rādīts kā **Instalē**. Pēc tam, kad instalēšana ir pabeigta, atsvaidziniet lapu. Statusam ir jāmainās uz **Instalēts**.
1. Programmas Dataverse kreisās navigācijas rūtī izvēlieties sadaļu **Programmas** un pārbaudiet, vai **Krājumu redzamība** ir veiksmīgi instalēta Power Apps. Ja nav sadaļas **Programmas**, sazinieties ar Krājumu redzamības preču grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!TIP]
> Mēs iesakām pievienoties krājumu redzamības pievienojumprogrammas lietotāju grupai, kurā varat atrast noderīgas rokasgrāmatas, saņemt mūsu jaunākos atjauninājumus un publicēt visus jautājumus par krājumu redzamības izmantošanu. Lai pievienotos, lūdzu, nosūtiet e-pasta ziņojumu krājumu redzamības produktu komandai uz e-pastu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) un iekļaujiet savu Supply Chain Management vides ID.

> [!IMPORTANT]
> Ja jums ir vairāk nekā viena LCS vide, izveidojiet katrai videi atšķirīgu Azure AD lietojumprogrammu. Ja lietojat vienu lietojumprogrammas ID un nomnieka ID, lai instalētu Inventory Visibility lietojumprogrammu atšķirīgām vidēm, vecākām vidēm tiks rādīta marķiera problēma. Tikai pēdējā instalētā vide būs derīga.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Atinstalēt Krājumu redzamības pievienojumprogrammu

Lai atinstalētu Krājumu redzamības pievienojumprogrammu, atlasiet LCS lapā **Atinstalēt**. Atinstalēšanas process pārtrauc Krājumu redzamības pievienojumprogrammu, noņem pievienojumprogrammas reģistrāciju no LCS un dzēš visus pagaidu datus, kas ir saglabāti Krājumu redzamības pievienojumprogrammas datu kešatmiņā. Tomēr jūsu Dataverse abonementā saglabātie primārie krājumu dati netiek dzēsti.

Lai atinstalētu krājumu datus, kas ir saglabāti Dataverse abonementā, atveriet [Power Apps](https://make.powerapps.com), atlasiet navigācijas joslā **Vide** un atlasiet vidi, kas ir piesaistīta jūsu Dataverse LCS videi. Pēc tam dodieties uz **Risinājumi** un izdzēsiet šos piecus risinājumus:

1. Noenkurošanas risinājums Krājumu redzamības Dynamics 365 risinājumā
1. Dynamics 365 FNO SCM Krājumu redzamības Applications risinājums
1. Krājumu pakalpojuma konfigurēšana
1. Krājumu redzamības savrupā programma
1. Dynamics 365 FNO SCM Krājumu redzamības pamata risinājums

Pēc šo risinājumu dzēšanas arī tabulās saglabātie dati arī tiks dzēsti.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Inventory Visibility iestatīšana pakalpojumā Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Izvietot Krājumu redzamības integrācijas pakotni

Ja jūs palaidāt Supply Chain Management versiju 10.0.17 vai agrāk, sazinieties ar Krājumu redzamības standarta atbalsta komandu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu iepakojuma failu. Pēc tam izvietojiet pakotni LCS.

> [!NOTE]
> Ja izvietošanas laikā rodas versiju neatbilstības kļūda, X++ projekts ir jāimportē manuāli izstrādes vidē. Pēc tam izveidojiet izvietojamu pakotni savā izstrādes vidē un izvietojiet to ražošanas vidē.
>
> Kods ir iekļauts Supply Chain Management versijā 10.0.18. Ja izmantojat šo versiju vai jaunāku, izvietošana nav nepieciešama.

Pārliecinieties, ka jūsu Supply Chain Management vidē ir ieslēgtas šādas funkcijas. (Pēc noklusējuma tās ir iespējotas.)

| Līdzekļa apraksts | Koda versija | Pārslēgt klasi |
|---|---|---|
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSum tabulā      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSumDelta tabulā | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Pievienojumprogrammas Krājumu redzamība integrācijas iestatīšana

Kolīdz esat instalējuši pievienojumprogrammu, sagatavojiet Supply Chain Management sistēmu darbam ar to, izpildot tālāk norādītās darbības.

1. Pakalpojumā Supply Chain Management atveriet darbvietu **[Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** un iespējojiet šādus līdzekļus:
    - *Inventory Visibility integrācija* — obligāti.
    - *Inventory Visibility integrācija ar rezervāciju nobīdi* — ieteicama, bet ne obligāta. Vajadzīga 10.0.22. vai jaunāka versija. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Inventory Visibility integrācijas parametri**.
1. Atveriet cilni **Vispārīgi** un veiciet tālāk norādītos iestatījumus.
    - **Inventory Visibility gala punkts** — Ievadiet URL videi, kurā palaižat Inventory Visibility. Papildinformāciju skatiet rakstā [Atrast pakalpojuma galamērķi](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maksimālais ierakstu skaits vienā pieprasījumā** — Iestatīts uz maksimālo ierakstu skaitu, kuru ietvert vienā pieprasījumā. Ir jāievada pozitīvs veselais skaitlis, kas ir mazāks vai vienāds ar 1000. Noklusējuma vērtība ir 512. Stingri iesakām paturēt noklusējuma vērtību, ja vien neesat saņēmuši ieteikumi no Microsoft Support vai citu iemeslu dēļ neesat droši, ka tā ir jāmaina.

1. Ja iespējojāt neobligāto līdzekli *Inventory Visibility integrācija ar rezervāciju nobīdi*, atveriet cilni **Rezervāciju nobīde** un veiciet šādus iestatījumus:
    - **Iespējot rezervāciju nobīdi** — Iestatiet uz *Jā*, lai iespējotu šo funkcionalitāti.
    - **Rezervāciju nobīdes pārveidotājs** — Atlasiet krājuma transakcijas statusu, kas nobīdīs Inventory Visibility veiktās rezervācijas. Šis iestatījums nosaka pasūtījuma apstrādes posmu, kurš aktivizē nobīdes. Statusu izseko pasūtījuma krājumu darbības statuss. Izvēlieties vienu no šīm:
        - *Pasūtījumā* – statusam *On transaction* pasūtījums pēc izveidošanas nosūta korespondējošo pieprasījumu. Nobīžu daudzums būs izveidotā pasūtījuma daudzums.
        - *Rezervēšana* – Pasūtījuma statuss *Rezervēt pasūtītajā pasūtījumā* pēc tā rezervētā, izdotā, pavadzīmes grāmatošanas vai rēķina izrakstīšanas pasūtījums nosūta korespondējošo pieprasījumu. Pieprasījums tiks parādīts tikai vienu reizi, pirmajam solim, kad notiks iepriekš minētais process. Novīdes daudzums būs daudzums, kurā krājuma transakcijas statuss atbilstoŠajā pasūtījuma rindā tiek mainīts no *Pasūtījumā* uz *Rezervēts pasūtījums* (vai uz vēlāku statusu).

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie \> Krājumu redzamības integrāciju** un iespējojiet darbu. Visi krājumu izmaiņu notikumi no Supply Chain Management tagad tiks grāmatoti Krājumu redzamībai.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]