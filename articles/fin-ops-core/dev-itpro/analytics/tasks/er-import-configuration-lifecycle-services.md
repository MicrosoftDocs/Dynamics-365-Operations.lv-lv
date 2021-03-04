---
title: Importēt konfigurāciju no Lifecycle Services
description: Šajā tēmā ir izskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c43cdce8d073f04a3158c8beb13a5376e669a4c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684455"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Importēt konfigurāciju no Lifecycle Services

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu [Elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācija](../general-electronic-reporting.md#Configuration) versiju no [projekta līmeņa līdzekļu bibliotēka](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS).

Šajā piemērā jūs atlasīsiet vēlamo ER konfigurācijas versiju un importēsiet to parauga uzņēmumam ar nosaukumu Litware, Inc. Šīs darbības var pabeigt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos. Lai izpildītu šīs darbības, jums vispirms ir jāizpilda procedūras [Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). Ir nepieciešama arī piekļuve LCS.

1. Pierakstieties programmā, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Atlasiet **Konfigurācijas**.

<a name="accessconditions"></a>
> [!NOTE]
> Pārliecinieties, vai pašreizējais Dynamics 365 Finance lietotājs ir tāda LCS projekta biedrs, kurā ir ietverta tā līdzekļu bibliotēka, kurai lietotājs vēlas [piekļūt](../../lifecycle-services/asset-library.md#asset-library-support) , lai importētu ER konfigurācijas.
>
> Jūs nevarat piekļūt LCS projektam no ER repozitorija, kas pārstāv citu domēnu, nevis to domēnu, kas tiek izmantots programmā Finance. Ja jūs mēģināt, tiks rādīts tukšs LCS projektu saraksts, un jūs nevarēsiet importēt ER konfigurācijas no projekta līmeņa līdzekļu bibliotēkas uz LCS. Lai piekļūtu projekta līmeņa līdzekļu bibliotēkām no ER repozitorija, kas tiek izmantots, lai importētu ER konfigurācijas, piesakieties programmai Finance, izmantojot lietotāja akreditācijas datus, kas pieder nomniekam (domēns), kam ir nodrošināta pašreizējā Finance instance.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Dzēst koplietotu datu modeļa konfigurācijas versiju

1. Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Modeļa konfigurācijas paraugs**.

    Jūs izveidojāt parauga datu modeļa konfigurācijas pirmo versiju un publicējāt to LCS, kad pabeidzāt darbības [Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). Šajā procedūrā jūs dzēsīsiet to ER konfigurācijas versiju. Vēlāk šajā tēmā šo versiju importēsit no LCS.

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