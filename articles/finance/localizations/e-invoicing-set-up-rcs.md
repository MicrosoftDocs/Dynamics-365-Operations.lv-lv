---
title: Iestatīt regulēšanas konfigurācijas pakalpojumu (RCS)
description: Šajā rakstā skaidrots, kā iestatīt regulēšanas konfigurācijas pakalpojumu (RCS).
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 63a4f77d6e80133947dff678cef3885167ec55be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285793"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Iestatīt regulēšanas konfigurācijas pakalpojumu (RCS)

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt regulēšanas konfigurācijas pakalpojumu (RCS).

## <a name="turn-on-globalization-features"></a>Ieslēgt globalizācijas līdzekļus

1. Piesakieties savā RCS kontā.
2. Atlasiet elementu **Funkciju pārvaldība**.
3. Darbvietā **Līdzekļu pārvaldība** sarakstā atlasiet **Globalizācijas līdzekļi** un pēc tam atlasiet **Iespējot tūlīt**.

Globalizācijas līdzekļu darbvietas **elementam** tagad ir jābūt redzamam galvenajā RCS informācijas panelī.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Iestatiet RCS integrācijas parametrus ar elektronisko rēķinu izrakstīšanu

1. **Globalizācijas līdzekļu** darbtelpas sadaļā **Saistītie iestatījumi** atlasiet **Elektroniskās ziņošanas parametri**.
2. Cilnē Elektroniskā **rēķina izrakstīšana**, kas atrodas **laukā Pakalpojuma galapunkta URI**, Microsoft Azure ievadiet savam ģeogrāfijai atbilstošo pakalpojuma galapunktu, kā parādīts šajā tabulā.

    | Datacenter Azure ģeogrāfija | Pakalpojuma galapunkta URI |
    |----------------------------|----------------------|
    | Amerikas Savienotās Valstis              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Eiropa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Apvienotā Karaliste             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Āzija                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japāna                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Šveice                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brazīlija                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Apvienotie Arābu Emirāti       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Austrālija                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanāda                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Francija                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Indija                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Pārbaudiet, vai lauks **Lietojumprogrammas ID** ir iestatīts uz **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Šī vērtība ir fiksēta vērtība. Pārliecinieties, vai ir ievadīts tikai globāli unikāls identifikators (GUID) un vai vērtībā nav ietverti citi simboli, piemēram, atstarpes, komati, periodi vai pēdiņas.
4. Laukā **LCS vides ID** ievadiet jūsu Lifecycle Services (LCS) vides ID Microsoft Dynamics. Šī vērtība ir atsauce uz Finanšu vai piegādes ķēžu pārvaldības vidi, ko izmantosiet ar Elektronisko rēķinu izrakstīšanas pakalpojumu. Lai saņemtu ID, [piesakieties LCS](https://lcs.dynamics.com/), **·** **·** **atveriet projektu un pēc tam cilnes Pārvaldīt vidi sadaļā Vides informācija meklējiet laukā Vides ID.**

    > [!IMPORTANT]
    > Ja Elektroniskā rēķinu izrakstīšanas pievienojumprogramma ir instalēta vairākās LCS finanšu vai piegādes ķēžu pārvaldības vidēs, vienmēr izmantojiet pēdējās instalētās vides ID. Ja izlemjat instalēt pievienojumprogrammu jaunā vidē pēc elektronisko rēķinu funkcionalitātes iestatīšanas un darba ar to, **atjauniniet LCS vides ID** lauku RCS uz jaunāko vērtību.

5. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="configuration-providers"></a>Konfigurācijas nodrošinātāji

Jūs varat izmantot konfigurācijas nodrošinātājus, lai atšķirtu elektronisko pārskatu (ER) konfigurāciju īpašniekus, kas tiek izmantoti elektronisko rēķinu izrakstīšanas procesos un īpašnieku globalizācijas funkcionalitātēs. Visiem globalizācijas līdzekļiem, ko nodrošina Microsoft un kas tiek publicēti globālajā repozitorijā, konfigurācijas nodrošinātājs tiek iestatīts uz **Microsoft** (`http://microsoft.com`).

Var regulēt tikai ER konfigurācijas un globalizācijas līdzekļus, kas pieder aktīvam konfigurācijas nodrošinātājam. Šīs konfigurācijas un funkcijas var izmantot kā veidnes, lai izveidotu konfigurācijas un līdzekļus, kas pieder aktīvam konfigurācijas nodrošinātājam, tādējādi jūs variet tās pielāgot.

Vispirms izveidojiet konfigurācijas nodrošinātājus. Pēc tam iestatiet vienu no tām kā aktīvu. Microsoft konfigurācijas nodrošinātāju nevar **iestatīt** kā aktīvu.

### <a name="create-a-configuration-provider"></a>Konfigurācijas nodrošinātāja izveide

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
2. Atlasiet **Jauna**.
3. Laukā **Nosaukums** ievadiet unikālu konfigurācijas nodrošinātāja nosaukumu.
4. Interneta adreses **laukā** ievadiet konfigurācijas nodrošinātāja unikālo URL.
5. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

### <a name="select-a-configuration-provider-as-active"></a>Atlasīt konfigurācijas nodrošinātāju kā aktīvu

1. Konfigurācijas nodrošinātāju sarakstā atlasiet konfigurācijas nodrošinātāju, kuru vēlaties iestatīt kā aktīvu.
2. Atlasiet **Iestatīt kā aktīvu**.

## <a name="import-er-configurations-from-the-global-repository"></a>Importēt ER konfigurācijas no globālā repozitorija

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
2. Konfigurācijas nodrošinātāju sarakstā atlasiet Microsoft **un** pēc tam atlasiet **Repositories**.
3. Atlasiet **Globāls**, pēc tam Darbību rūtī atlasiet **Atvērt**.
4. Importēt šādus ER modeļus:

    - **Debitora rēķina konteksta modelis**
    - **Rēķina modelis**
    - **Finanšu dokumenti** (Brazīlijas scenārijiem, ja nepieciešams)
    - **Atbildes ziņojuma modelis**

5. Ja **rēķina modeļa kartēšana** netika automātiski importēta, importējiet to.
6. Aizvērt lapu.
