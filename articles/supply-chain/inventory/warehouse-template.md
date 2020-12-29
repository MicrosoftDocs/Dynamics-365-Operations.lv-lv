---
title: Noliktavas iestatīšana, izmantojot noliktavas konfigurācijas veidni
description: Šajā tēmā ir aprakstīts, kā iestatīt noliktavu, izmantojot noliktavas konfigurācijas veidni.
author: perlynne
manager: tfehr
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 66fdc26b0b967a04a3c6a6e3444e00b1372dc504
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433030"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Noliktavas iestatīšana, izmantojot noliktavas konfigurācijas veidni

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt noliktavu, izmantojot noliktavas konfigurācijas veidni. Varat izmantot vairākas iepriekš definētas konfigurācijas veidnes. Papildinformāciju par šo veidņu lietošanu skatiet šeit: [Konfigurācijas datu veidnes](../../dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Scenāriji, kur konfigurācijas veidnes varētu noderēt

Konfigurācijas veidnes var noderēt dažādos scenārijos. Daži piemēri:

- Esat pabeidzis konfigurācijas iestatījumus un pārbaudījis tos testēšanas vidē, un tagad šos iestatījumus vēlaties kopēt uz ražošanas vidi.
- Noliktavas iestatījumus vēlaties paplašināt uz vairākām juridiskajām personām vai vēlaties izveidot jaunu noliktavu tajā pašā juridiskajā personā.
- Vēlaties ātri sagatavoties noliktavas funkcionalitātes demonstrācijai.
- Vēlaties, lai esošie krājumi un noliktavas izmantotu noliktavas pārvaldības funkcionalitāti, nevis krājumu pārvaldības funkcionalitāti.

Šajā tēmā galvenā uzmanība ir vērsta uz pirmo no šiem scenārijiem. Tajā ir parādīts, kā varat izmantot konfigurācijas veidni, lai konfigurācijas iestatījumus no testa vides kopētu uz ražošanas vidi.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Konfigurācijas iestatījumu kopēšana no testa vides uz ražošanas vidi

Šim scenārijam konfigurācijas iestatījumi noliktavai un dažiem transakciju procesiem testēšanas vidē jau pastāv. Tagad šos konfigurācijas iestatījumus noliktavai vēlaties kopēt no testa vides uz ražošanas vidi.

> [!NOTE]
> Kad kopējat konfigurācijas iestatījumus, ir svarīgi iekļaut citus saistītos iestatījumu datus. Piemēram, vēlaties iestatīt preces, kopējot iestatījumus no testēšanas vides. Taču precei nevar iestatīt fiksētu izdošanas vietu, kamēr šī prece vēl nav izveidota. Lai gan atsevišķas konfigurācijas veidnes neatbalsta šāda veida atkarību, ir noklusējuma datu veidnes, kas to atbalsta. Konfigurācijas procesā varat vienkārši ietvert šīs noklusējuma datu veidnes.

### <a name="export-a-default-warehouse-template"></a>Noklusējuma noliktavas darba veidnes eksportēšana 

1. Atveriet darbvietu **Datu pārvaldība**.

    > [!NOTE]
    > Ja šo darbvietu lietojat pirmo reizi, pirms turpināšanas ir jāielādē visi datu elementi.

2. Atlasiet elementu **Veidnes** un pēc tam atlasiet **Ielādēt noklusējuma veidnes**, lai ielādētu noklusējuma veidnes.

    > [!NOTE]
    > Vienums **Ielādēt noklusējuma veidnes** ir pieejams tikai skatā **Paplašināts**. Atlasiet **Struktūras parametri** un pēc tam laukā **Skatīt noklusējuma vērtības** atlasiet **Paplašināts skats**.

3. Kad noklusējuma veidnes ir ielādētas, varat šīs veidnes mainīt, lai tās atbilstu jūsu uzņēmuma prasībām.

    > [!NOTE]
    > Lai ielādētu noklusējuma veidnes un importētu veidnes, jums ir nepieciešama administratora piekļuve sistēmai. Šī prasība palīdz nodrošināt, ka visi elementi veidnē tiek ielādēti pareizi.

4. Pārliecinieties, vai atrodaties juridiskajā personā, no kuras vēlaties eksportēt uzņēmumam raksturīgos datus.
5. Darbvietā atlasiet **Eksportēt**.
6. Izveidojiet jaunu eksporta projektu.
7. Atlasiet **+ Pievienot veidni** un atrodiet noklusējuma noliktavas veidni **400 - NPS**. Šī veidne pievieno datu elementus noliktavas konfigurācijai.

    > [!NOTE]
    > Ja datus, ko vēlaties eksportēt, ir nepieciešams filtrēt (piemēram, vēlaties eksportēt tikai tos datus, kas attiecas uz konkrētu noliktavu), jums ir jānovērtē katrs datu elements un jāpievieno filtrēšana, izmantojot vaicājumu. Varat arī eksportēt visus datus un pēc tam dzēst tos ierakstus, kas nav nepieciešami mērķa failos.

8. Atlasiet **Eksportēt**. Tiek eksportēti dati, kas ir saistīti ar visiem datu elementiem projektā.

Varat lejupielādēt zip failu šai datu pakotnei. Šajā failā ir visi dati atlasītajā formātā (piemēram, Excel formātā). Kā jau minēts, dažus ierakstus datu pakotnes failos, iespējams, ir nepieciešams atjaunināt, lai tos varētu importēt ražošanas vidē. Ja atjaunināt kādu ierakstu, pārliecinieties, vai netiek mainīts šī faila nosaukums.

### <a name="import-a-warehouse-configuration-setup"></a>Noliktavas konfigurācijas iestatījumu importēšana

1. Mērķa vidē pārliecinieties, vai atrodaties uzņēmumā, kurā vēlaties importēt noliktavas datus.

    > [!NOTE]
    > Pirms importēšanas ir jānosaka visas datu atkarības. Piemēram, veidnē **Noliktavas pārvaldība** ir datu elements ar nosaukumu **Noliktavas atgriešanas metodes kodi**. Šajā elementā ir dati, kas ir saistīti ar iestatījumu lapu **Atgriešanas metodes kodi** (**Noliktavas pārvaldība** > **Iestatīšana** > **Mobilā ierīce** > **Atgriešanas metodes kodi**). Ja esošie iestatījumi jau apstrādā atgriešanas procesu pārdošanas pasūtījumiem, laukā **Atgriešanas metodes kods** ir kāda vērtība. Atgriešanas metodes kods šajā laukā ir saistīts ar datu elementu **Atgriešanas metodes kods**, kas ir daļa no veidnes **Pārdošana un mārketings**. Ja dati no datu elementa **Atgriešanas metodes kods** netiek importēti pirms datiem no lauka **Noliktavas atgriešanas metodes kodi**, importēšana būs nesekmīga.

2. Darbvietā **Datu pārvaldība** atlasiet **Importēt**.
3. Izveidojiet jaunu importēšanas projektu.
4. Atlasiet **+ Pievienot failu** un augšupielādējiet zip failu šai datu pakotnei.
5. Atlasiet **Importēt**. Skatā **Paplašināts** varat lietot opciju **Filtrēt**, lai ātri iegūtu pārskatu par problēmām, kas varētu rasties importēšanas laikā.

Žurnālā **Skatīt izpildi** ir sniegta detalizēta informācija par katru importēto datu elementu. Varat izmantot sagatavošanas posmu datu skatu, lai ātri nokļūtu pie mērķa datiem. Šādi varat redzēt, kā importētie dati izskatās saistītajās programmas lapās. Kad lietojat noklusējuma datu veidnes, importēšanas secība katram datu elementam darbojas iepriekš definētā veidā, lai palīdzētu nodrošināt, ka visi atkarīgie dati tiek importēti vispirms. Ja daļu no projekta veido pielāgotie datu elementi, jums ir jāpārliecinās, vai ir definēta pareizā secība. Papildinformāciju skatiet šeit: [Konfigurācijas datu veidnes](../../dev-itpro/data-entities/configuration-data-templates.md).

Lai uzzinātu vairāk par to, kā izmantot noliktavas veidni noliktavu konfigurācijas kopēšanai no viena uzņēmuma uz jaunu uzņēmumu vienas instances ietvaros, noskatieties šo 3 minūšu video pakalpojumā YouTube par: [Noliktavas veidnes izmantošana, lai kopētu konfigurāciju, programmā Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-topic"></a>Saistītā tēma

[Konfigurācijas datu veidnes](../../dev-itpro/data-entities/configuration-data-templates.md)
