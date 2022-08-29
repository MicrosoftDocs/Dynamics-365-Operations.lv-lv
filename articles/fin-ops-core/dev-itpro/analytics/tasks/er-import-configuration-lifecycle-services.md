---
title: Importēt konfigurāciju no Lifecycle Services
description: Šajā rakstā ir aprakstīts, kā no Lifecycle Services (LCS) konfigurācijas importēt jaunu elektronisko pārskatu (ER) Microsoft Dynamics konfigurāciju.
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
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
ms.openlocfilehash: 92c5d010430b38cb6c11a87283a2f7d4c29484f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290370"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Importēt konfigurāciju no Lifecycle Services

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots [, kā lietotājs sistēmas administratora vai elektronisko pārskatu izstrādātāja lomā var importēt jaunu elektronisko pārskatu (ER)](../general-electronic-reporting.md#Configuration)[...](../../lifecycle-services/asset-library.md)Microsoft Dynamics konfigurācijas versiju no projekta līmeņa Līdzekļu bibliotēkas lifecycle Services (LCS).

> [!IMPORTANT]
> LCS kā ER konfigurāciju glabāšanas repozitorija izmantošana ir [novecojusi](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Papildinformāciju skatiet [Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves nolietojums](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

Šajā piemērā jūs atlasīsiet vēlamo ER konfigurācijas versiju un importēsiet to parauga uzņēmumam ar nosaukumu Litware, Inc. Šīs darbības var pabeigt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos. Lai izpildītu šīs darbības, jums vispirms ir jāizpilda procedūras [Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). Ir nepieciešama arī piekļuve LCS.

1. Pierakstieties programmā, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Atlasiet **Konfigurācijas**.

<a name="accessconditions"></a>
> [!NOTE]
> Pārliecinieties, vai pašreizējais Dynamics 365 finanšu lietotājs ir LCS [projekta](../../lifecycle-services/asset-library.md#asset-library-support) dalībnieks, kas satur līdzekļu bibliotēku, kuru lietotājs vēlas piekļūt ER konfigurāciju importēšanai.
>
> Jūs nevarat piekļūt LCS projektam no ER repozitorija, kas pārstāv citu domēnu, nevis to domēnu, kas tiek izmantots programmā Finance. Ja jūs mēģināt, tiks rādīts tukšs LCS projektu saraksts, un jūs nevarēsiet importēt ER konfigurācijas no projekta līmeņa līdzekļu bibliotēkas uz LCS. Lai piekļūtu projekta līmeņa līdzekļu bibliotēkām no ER repozitorija, kas tiek izmantots, lai importētu ER konfigurācijas, piesakieties programmai Finance, izmantojot lietotāja akreditācijas datus, kas pieder nomniekam (domēns), kam ir nodrošināta pašreizējā Finance instance.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Dzēst koplietotu datu modeļa konfigurācijas versiju

1. Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Modeļa konfigurācijas paraugs**.

    Jūs izveidojāt parauga datu modeļa konfigurācijas pirmo versiju un publicējāt to LCS, kad pabeidzāt darbības [Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). Šajā procedūrā jūs dzēsīsiet to ER konfigurācijas versiju. Pēc tam šī versija vēlāk tiks importēta no LCS šajā rakstā.

2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

    Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Koplietots**. Šis statuss norāda, ka konfigurācija ir publicēta pakalpojumos LCS.

3. Atlasiet **Mainīt statusu**.
4. Atlasiet **Pārtraukt**.

    Mainot atlasītās versijas statusu no **Koplietots** uz **Pārtraukts**, versiju padara pieejamu dzēšanai.

5. Atlasiet **Labi**.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

    Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Pārtraukts**.

7. Atlasiet **Dzēst**.
8. Atlasiet **Jā**.

    Ievērojiet, ka atlasītajai datu modeļa konfigurācijai tagad ir pieejama tikai melnraksta 2. versija.

9. Aizvērt lapu.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Importēt koplietotu datu modeļa konfigurācijas versiju no LCS

1. Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.

2. Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.**.

3. Elementā **Litware, Inc.** atlasiet **Repozitoriji**.

    Tagad var atvērt sarakstu ar repozitorijiem, kas paredzēti Litware, Inc. konfigurācijas nodrošinātājam.

4. Atlasiet **Atvērt**.

    Šajā piemērā atlasiet **LCS** repozitoriju un atveriet to. Jums ir jābūt [piekļuve](#accessconditions) LCS projektam un līdzekļu bibliotēkai, kuram var piekļūt atlasītais ER repozitorijs.

5. Sarakstā atzīmējiet atlasīto rindu.

    Šā piemēra versiju sarakstā atlasiet konfigurācijas **Parauga modeļa konfigurācija** pirmo versiju.

6. Atlasiet **Importēt**.
7. Atlasiet **Jā** , lai apstiprinātu atlasītās versijas importēšanu no LCS.

    Informatīvs ziņojums apstiprina, ka atlasītā versija tika veiksmīgi importēta.

8. Aizvērt lapu.
9. Aizvērt lapu.
10. Atlasiet **Konfigurācijas**.
11. Koka struktūrā atlasiet **Parauga modeļa konfigurācija**.
12. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

    Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Koplietots**.

    Ievērojiet, ka tagad atlasītajai datu modeļa konfigurācijai ir pieejama arī koplietotā 1. versija.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
