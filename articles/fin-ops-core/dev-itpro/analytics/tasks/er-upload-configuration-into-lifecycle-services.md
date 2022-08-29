---
title: Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services
description: Šajā rakstā ir izskaidrots, kā izveidot jaunu elektronisko pārskatu (ER) konfigurāciju un augšupielādēt to pakalpojumā Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
ms.openlocfilehash: 28ad20956b4b621abdb74332187d8601c10ac164
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290070"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots [, kā lietotājs sistēmas administratora vai elektronisko pārskatu izstrādātāja lomā var izveidot jaunu elektronisko pārskatu (ER)](../general-electronic-reporting.md#Configuration)[...](../../lifecycle-services/asset-library.md)Microsoft Dynamics konfigurāciju un augšupielādēt to projekta līmeņa līdzekļu bibliotēkā pakalpojumā Lifecycle Services (LCS).

> [!IMPORTANT]
> LCS kā ER konfigurāciju glabāšanas repozitorija izmantošana ir [novecojusi](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Papildinformāciju skatiet [Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves nolietojums](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

Šajā piemērā jūs izveidosiet konfigurācijas un augšupielādēsiet to pakalpojumos LCS parauga uzņēmumam ar nosaukumu Litware, Inc. Šīs darbības var pabeigt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem. Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md). Ir nepieciešama arī piekļuve LCS.

1. Pierakstieties programmā, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Atlasiet vienumu **Litware, Inc.** un atzīmējiet to kā **Aktīvs**.
4. Atlasiet **Konfigurācijas**.

<a name="accessconditions"></a>
> [!NOTE]
> Pārliecinieties, vai pašreizējais Dynamics 365 finanšu lietotājs ir LCS [projekta](../../lifecycle-services/asset-library.md#asset-library-support) dalībnieks, kas satur līdzekļu bibliotēku, kas tiek izmantota ER konfigurāciju importēšanai.
>
> Jūs nevarat piekļūt LCS projektam no ER repozitorija, kas pārstāv citu domēnu, nevis to domēnu, kas tiek izmantots programmā Finance. Ja jūs mēģināt, tiks rādīts tukšs LCS projektu saraksts, un jūs nevarēsiet importēt ER konfigurācijas no projekta līmeņa līdzekļu bibliotēkas uz LCS. Lai piekļūtu projekta līmeņa līdzekļu bibliotēkām no ER repozitorija, kas tiek izmantots, lai importētu ER konfigurācijas, piesakieties programmai Finance, izmantojot lietotāja akreditācijas datus, kas pieder nomniekam (domēns), kam ir nodrošināta pašreizējā Finance instance.

## <a name="create-a-new-data-model-configuration"></a>Jaunas datu modeļa konfigurācijas izveide

1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
2. Lapā **Konfigurācijas** atlasiet **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.

    Šajā piemērā jūs izveidosiet konfigurāciju, kas satur parauga datu modeli elektroniskajiem dokumentiem. Šī datu modeļa konfigurācija vēlāk tiks augšupielādēta pakalpojumos LCS.

3. Laukā **Nosaukums** ievādiet **Parauga modeļa konfigurācija**.
4. Laukā **Apraksts** ievādiet **Parauga modeļa konfigurācija**.
5. Atlasiet **Izveidot konfigurāciju**.
6. Atlasiet **Modeļa veidotājs**.
7. Atlasiet **Jauns**.
8. Laukā **Nosaukums** ievadiet **Ieejas punkts**.
9. Atlasiet **Pievienot**.
10. Atlasiet **Saglabāt**.
11. Aizvērt lapu.
12. Atlasiet **Mainīt statusu**.
13. Atlasiet **Pabeigt**.
14. Atlasiet **Labi**.
15. Aizvērt lapu.

## <a name="register-a-new-repository"></a>Reģistrēt jaunu repozitoriju

1. Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.

2. Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.**.

3. Elementā **Litware, Inc.** atlasiet **Repozitoriji**.

    Tagad var atvērt sarakstu ar repozitorijiem, kas paredzēti Litware, Inc. konfigurācijas nodrošinātājam.

4. Atlasiet **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.

    Tagad varat pievienot jaunu repozitoriju.

5. Laukā **Konfigurācijas repozitorija ievade** atlasiet **LCS**.
6. Atlasiet **Izveidot repozitoriju**.
7. Laukā **Projekts** ievadiet vai atlasiet kādu vērtību.

    Šim piemēram atlasiet vēlāmo LCS projektu. Jums ir nepieciešama [piekļuve](#accessconditions) šim projektam.

8. Atlasiet **Labi**.

    Pabeidziet jauna repozitorija ierakstu.

9. Sarakstā atzīmējiet atlasīto rindu.

    Šajā piemērā atlasiet **LCS** repozitorija ierakstu.

    Ievērojiet, ka reģistrēto repozitoriju ir iezīmējis pašreizējais nodrošinātājs. Citiem vārdiem, tikai konfigurācijas, kas pieder šim nodrošinātājam, var tikt ievietotas šajā repozitorijā un tāpēc augšupielādētas atlasītajā LCS projektā.

10. Atlasiet **Atvērt**.

    Atverat repozitoriju, lai skatītu sarakstu ar ER konfigurācijām. Ja atlasītais projekts vēl nav lietots ER konfigurāciju koplietošanai, saraksts būs tukšs.

11. Aizvērt lapu.
12. Aizvērt lapu.

## <a name="upload-a-configuration-into-lcs"></a>Konfigurācijas augšupielāde pakalpojumā LCS

1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Modeļa konfigurācijas paraugs**.

    Ir jāatlasa izveidota konfigurācija, kas jau ir pabeigta.

3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

    Šajā piemērā atlasiet atlasītās konfigurācijas versiju, kuras statuss ir **Pabaigts**.

4. Atlasiet **Mainīt statusu**.
5. Atlasiet **Koplietot**.

    Konfigurācijas statuss tiek mainīts no **Pabeigts** uz **Koplietots** , kad konfigurācija tiek publicēta LCS.

6. Atlasiet **Labi**.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

    Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Koplietots**.

    Ņemiet vērā, ka atlasītās versijas statuss no **Pabeigts** ir mainīts uz **Koplietots**.

8. Aizvērt lapu.
9. Atlasiet **Repozitoriji**.

    Tagad var atvērt sarakstu ar repozitorijiem, kas paredzēti Litware, Inc. konfigurācijas nodrošinātājam.

10. Atlasiet **Atvērt**.

    Šajā piemērā atlasiet **LCS** repozitoriju un atveriet to.

    Ievērojiet, ka atlasītā konfigurācija tiek rādīta kā atlasītā LCS projekta līdzeklis.

11. Atvēriet LCS, pārejot uz <https://lcs.dynamics.com>.
12. Atvēriet projektu, kas iepriekš tika izmantots repozitorija reģistrācijai.
13. Atveriet projekta līdzekļu bibliotēku.
14. Atlasiet **GER konfigurācija** līdzekļa veidu.

    Ir jāuzskaita jūsu augšupielādētā ER konfigurācija.

    Ņemiet vērā, ka augšupielādēto LCS konfigurāciju var importēt citā instancē, ja nodrošinātājiem ir piekļuve šim LCS projektam.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
