---
title: Debitora maksājumu prognožu iespējošana (priekšskatījums)
description: Šajā tēmā paskaidrots, kā ieslēgt un konfigurēt debitora maksājumu prognozēšanas līdzekli Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0b945111f360838dfa35cddb916c4fb34a41f55bdd8f3095bd97c906b7dd3dd7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768895"
---
# <a name="enable-customer-payment-predictions-preview"></a>Debitora maksājumu prognožu iespējošana (priekšskatījums)

[!include [banner](../includes/banner.md)]

Šajā tēmā paskaidrots, kā ieslēgt un konfigurēt debitora maksājumu prognozēšanas līdzekli Finanšu ieskatos. Ieslēdziet līdzekli darbvietā **Līdzekļu pārvaldība** un ievadiet konfigurācijas iestatījumus lapā **Finanšu ieskatu parametri**. Šajā tēmā iekļauta arī informācija, kas var palīdzēt efektīvi izmantot līdzekli.

> [!NOTE]
> Pirms veicat tālāk norādītās darbības, pārliecinieties, vai ir paveiktas priekšnosacījumu darbības tēmā [Finanšu ieskatu konfigurēšana](configure-for-fin-insites.md).

1. Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi. Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi. (Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > Izlaidiet šo darbību, ja izmantojat versiju 10.0.20 vai jaunāku versiju, vai, ja izmantojat Service Fabric izvietojumu. Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli. Ja neredzat līdzekli darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot to ieslēgt, sazinieties ar <fiap@microsoft.com>. 

2. Ieslēdziet debitora maksājumu ieskatu līdzekli:

    1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
    2. Atrodiet līdzekli, kura nosaukums ir **Debitora maksājumu ieskati (priekšskatījums)**.
    3. Atlasiet **Iespējot tagad**.

    Debitora maksājumu ieskatu līdzeklis tagad ir ieslēgts un gatavs konfigurēšanai.

3. Konfigurējiet debitora maksājumu ieskatu līdzekli:

    1. Doties uz **Kredīti un iekasēšana \> Iestatījumi \> Finanšu ieskati \> Finanšu ieskatu parametri**.

        [![Finanšu ieskatu parametru lapa pirms līdzekļa konfigurēšanas.](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Lapā **Finanšu ieskatu parametri**, kas atrodas cilnē **Debitora maksājumu ieskati** atlasiet saiti **Skatīt datu laukus, kas izmantoti prognozēšanas modelī**, lai atvērtu lapu **Datu lauki prognozēšanas modelim**. Tur varat apskatīt noklusējuma sarakstu ar laukiem, kas tiek izmantoti, lai izveidotu mākslīgā intelekta prognozēšanas modeli debitora maksājumu prognozēm.

        Lai izmantotu noklusējuma lauku sarakstu un izveidotu prognozēšanas modeli, aizveriet lapu **Datu lauki prognozēšanas modelim** un pēc tam lapā **Finanšu ieskatu parametri** iestatiet opciju **Iespējot līdzekli** uz **Jā**.

    3. Nosakiet darījumu periodu "ļoti novēloti", lai definētu, ko jūsu biznesam nozīmē prognozēšanas grozs **Ļoti novēloti**.

        Katram atvērtajam rēķinam sistēma prognozē maksājuma iespējamību trīs grozos: **Savlaicīgi**, **Novēloti** un **Ļoti novēloti**.

        - **Savlaicīgi** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti darījuma termiņā vai pirms tā.
        - **Novēloti** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti pēc darījuma termiņa beigām, bet pirms darījuma perioda "ļoti novēloti" sākuma.
        - **Ļoti novēloti** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti pēc darījuma perioda "ļoti novēloti" sākuma.

        > [!NOTE]
        > Ja maināt darījumu periodu "ļoti novēloti" un atlasāt **Mainīt novēlošanas slieksni** pēc tam, kad ir izveidots mākslīgā intelekta modelis debitora maksājumiem, esošais prognozēšanas modelis tiek dzēsts, un tiek izveidots jauns modelis. Jaunais prognozēšanas modelis pārvietos darījumus uz periodu "ļoti novēloti", pamatojoties uz iestatījumiem, kas tika ievadīti, to definējot.

    4. Pēc tam, kad esat pabeidzis definēt darījumu periodu "ļoti novēloti", atlasiet **Izveidot prognozēšanas modeli**, lai izveidotu prognozēšanas modeli. Sadaļa **Prognozēšanas modelis** lapā **Finanšu ieskatu parametri** parāda prognozēšanas modeļa statusu.

        > [!NOTE]
        > Jebkurā laikā, kamēr tiek veidots prognozēšanas modelis, varat atlasīt **Atiestatīt modeļa izveidi**, lai atiestatītu procesu.

    Līdzeklis tagad ir konfigurēts un ir gatavs lietošanai.

Pēc tam, kad līdzeklis ir ieslēgts un konfigurēts, un prognozēšanas modelis ir izveidots un darbojas, sadaļā **Prognozēšanas modelis** lapā **Finanšu ieskatu parametri** redzama modeļa precizitāte, kā parādīts tālāk redzamajā attēlā.

[![Prognozēšanas modeļa precizitāte finanšu ieskatu parametru lapā.](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Informācija par izlaišanu

Finanšu ieskatu publiskais priekšskatījums izmēģinājuma izvietošanai ir pieejams Amerikas Savienotajās Valstīs, Eiropā un Apvienotajā Karalistē. Korporācija Microsoft pakāpeniski pievieno atbalstu citiem reģioniem.

Publiskā priekšskatījuma līdzekļus var un vajadzētu ieslēgt tikai 2. līmeņa smilškastes vidēs. Iestatīšanas un mākslīgā intelekta modeļus, kas izveidoti smilškastes vidē, nevar migrēt uz ražošanas vidi. Lai iegūtu papildu informāciju, skatiet rakstu [Pakalpojuma Microsoft Dynamics 365 Previews lietošanas papildu nosacījumi](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
