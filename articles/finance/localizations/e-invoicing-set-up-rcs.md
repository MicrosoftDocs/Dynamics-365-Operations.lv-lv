---
title: Iestatīt regulatīvo konfigurācijas pakalpojumu (RCS)
description: Šajā tēmā ir paskaidrots, kā iestatīt regulatīvo konfigurācijas pakalpojumu (RCS).
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 33aab6f0a482ce3d90a7e9828015a8e7bebb7827
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371968"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Iestatīt regulatīvo konfigurācijas pakalpojumu (RCS)

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt regulatīvo konfigurācijas pakalpojumu (RCS).

## <a name="turn-on-globalization-features"></a>Globalizācijas līdzekļu ieslēgšana

1. Piesakieties savā RCS kontā.
2. Atlasiet elementu **Funkciju pārvaldība**.
3. Darbvietā **Līdzekļu pārvaldība** sarakstā atlasiet **Globalizācijas līdzekļi** un pēc tam atlasiet **Iespējot tūlīt**.

Globalizācijas līdzekļu **darbvietas elementam** tagad jāparādās galvenajā RCS informācijas panelī.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Iestatiet RCS integrācijas parametrus ar elektronisko rēķinu izrakstīšanu

1. **Globalizācijas līdzekļu** darbtelpas sadaļā **Saistītie iestatījumi** atlasiet **Elektroniskās ziņošanas parametri**.
2. **Cilnes** Elektroniskie rēķini **laukā Servisa galapunkts URI** ievadiet ģeogrāfijai atbilstošo servisa galapunktu Microsoft Azure, kā parādīts nākamajā tabulā.

    | Datacenter Azure ģeogrāfija | Pakalpojuma galapunkta URI |
    |----------------------------|----------------------|
    | Amerikas Savienotās Valstis              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Eiropa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Apvienotā Karaliste             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Āzija                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japāna                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Pārbaudiet, vai lauks **Lietojumprogrammas ID** ir iestatīts uz **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Šī vērtība ir fiksēta vērtība. Pārliecinieties, vai ir ievadīts tikai globāli unikāls identifikators (GLOBALLY UNIQUE IDENTIFIER — GUID) un vai vērtībā nav iekļauti citi simboli, piemēram, atstarpes, komati, punkti vai pēdiņas.
4. Laukā **LCS vides ID** ievadiet savas Microsoft Dynamics dzīves cikla pakalpojumu (LCS) vides ID. Šī vērtība ir atsauce uz finanšu vai piegādes ķēdes pārvaldības vidi, ko izmantosit ar elektronisko rēķinu pakalpojumu. Lai iegūtu savu ID, piesakieties [LKS](https://lcs.dynamics.com/), atveriet projektu un pēc tam cilnes **Vides** pārvaldība sadaļā Detalizēta informācija par **vidi** skatiet **laukā Vides ID**.

    > [!IMPORTANT]
    > Ja pievienojumprogramma Elektroniskie rēķini ir instalēta vairākās LCS finanšu vai piegādes ķēdes pārvaldības vidēs, vienmēr izmantojiet jaunākās instalētās vides ID. Ja nolemjat instalēt pievienojumprogrammu jaunā vidē Pēc elektronisko rēķinu funkcionalitātes iestatīšanas un darba ar to, atjauniniet **LCS vides ID** lauku RCS līdz jaunākajai vērtībai.

5. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="configuration-providers"></a>Konfigurācijas nodrošinātāji

Konfigurācijas nodrošinātājus var izmantot, lai atšķirtu elektronisko pārskatu (ER) konfigurāciju īpašniekus, kas tiek izmantoti elektronisko rēķinu izrakstīšanas procesos, un īpašnieku globalizācijas līdzekļus. Visiem globalizācijas līdzekļiem, ko nodrošina Korporācija Microsoft un kas publicēti globālajā repozitorijā, konfigurācijas nodrošinātājs ir iestatīts uz **Microsoft** (`http://microsoft.com`).

Var pielāgot tikai ER konfigurācijas un globalizācijas līdzekļus, kas pieder aktīvajam konfigurācijas nodrošinātājam. Šīs konfigurācijas un līdzekļus var izmantot kā veidnes, lai izveidotu konfigurācijas un līdzekļus, kas pieder aktīvajam konfigurācijas nodrošinātājam, lai tos varētu pielāgot.

Pirmkārt, izveidojiet konfigurācijas nodrošinātājus. Pēc tam iestatiet vienu no tiem kā aktīvu. Microsoft **konfigurācijas nodrošinātāju** nevar iestatīt kā aktīvu.

### <a name="create-a-configuration-provider"></a>Konfigurācijas nodrošinātāja izveide

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
2. Atlasiet **Jauna**.
3. Laukā **Nosaukums** ievadiet unikālu konfigurācijas nodrošinātāja nosaukumu.
4. Laukā **Interneta adrese** ievadiet konfigurācijas nodrošinātāja unikālo URL.
5. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

### <a name="select-a-configuration-provider-as-active"></a>Atlasiet konfigurācijas nodrošinātāju kā aktīvu

1. Konfigurācijas nodrošinātāju sarakstā atlasiet konfigurācijas nodrošinātāju, kuru vēlaties iestatīt kā aktīvu.
2. Atlasiet **Iestatīt kā aktīvu**.

## <a name="import-er-configurations-from-the-global-repository"></a>Er konfigurāciju importēšana no globālā repozitorija

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
2. Konfigurācijas nodrošinātāju sarakstā atlasiet **Microsoft** un pēc tam atlasiet **Repozitoriji**.
3. Atlasiet **Globāls** un pēc tam darbību rūtī atlasiet **Atvērt**.
4. Importējiet šādus ER modeļus:

    - **Debitora rēķina konteksta modelis**
    - **Rēķina modelis**
    - **Fiskālie dokumenti** (ja nepieciešams, Brazīlijas scenārijiem)
    - **Atbildes ziņojuma modelis**

5. Ja **rēķinu modeļa kartējums** netika importēts automātiski, importējiet to.
6. Aizvērt lapu.
