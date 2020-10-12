---
title: Kartēšanas iestatīšana pārdošanas pasūtījuma statusa laukiem
description: Šajā tēmā ir paskaidrots, kā iestatīt pārdošanas pasūtījuma statusa laukus duālajam ierakstam.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829289"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a>Kartēšanas iestatīšana pārdošanas pasūtījuma statusa laukiem

[!include [banner](../../includes/banner.md)]

Laukiem, kas norāda pārdošanas pasūtījuma statusu, ir dažādas numerācijas vērtības programmā Microsoft Dynamics 365 Supply Chain Management un Dynamics 365 Sales. Lai kartētu šos laukus duālajam ierakstam, ir nepieciešams papildu iestatījums.

## <a name="fields-in-supply-chain-management"></a>Supply Chain Management lauki

Programmā Supply Chain Management pārdošanas pasūtījuma statusu ataino divi lauki. Kartējamie lauki ir **Statuss** un **Dokumentu statuss**.

**Statusa** uzskaitījums norāda pasūtījuma vispārējo statusu. Šis statuss tiek norādīts pasūtījuma galvenē.

**Statusa** uzskaitījums piedāvā šādas vērtības:

- Atvērts pasūtījums
- Piegādāts
- Izveidots rēķins
- Atcelta

**Dokumentu statusa** uzskaitījums norāda visjaunāko dokumentu, kas ģenerēts pasūtījumam. Piemēram, ja pasūtījums ir apstiprināts, šis dokuments ir pārdošanas pasūtījuma apstiprinājums. Ja pārdošanas pasūtījums ir daļēji iekļauts rēķinā un pēc tam tiek apstiprināta atlikusī rinda, dokumenta statuss paliek **Rēķins**, jo rēķins tiek ģenerēts vēlāk procesā.

**Dokumentu statusa** uzskaitījums piedāvā šādas vērtības:

- Apstiprināšana
- Izdošanas saraksts
- Pavadzīme
- Rēķins

## <a name="fields-in-sales"></a>Pārdošanas lauki

Programmā Sales pasūtījuma statusu norāda divi lauki. Kartējamie lauki ir **Statuss** un **Apstrādes statuss**.

**Statusa** uzskaitījums norāda pasūtījuma vispārējo statusu. Tam ir tālāk minētās vērtības:

- Aktīvs
- Iesniegts
- Izpildīts
- Izveidots rēķins
- Atcelts

Tika ieviests **Apstrādes statusa** uzskaitījums, lai statusu varētu precīzāk kartēt ar Supply Chain Management.

Tabulā ir parādīta **Apstrādes statusa** kartēšana programmā Supply Chain Management.

| Apstrādes statuss   | Supply Chain Management statuss | Supply Chain Management dokumentu statuss |
|---------------------|-----------------------------------|--------------------------------------------|
| Aktīvie              | Atvērts pasūtījums                        | None                                       |
| Apstiprināts           | Atvērts pasūtījums                        | Apstiprināšana                               |
| Izdots              | Atvērts pasūtījums                        | Izdošanas saraksts                               |
| Daļēji piegādāts | Atvērts pasūtījums                        | Pavadzīme                               |
| Piegādāts           | Piegādāts                         | Pavadzīme                               |
| Daļēji iekļauts rēķinā  | Piegādāts                         | Rēķins                                    |
| Izveidots rēķins            | Izveidots rēķins                          | Rēķins                                    |
| Atcelta           | Atcelta                         | Nav attiecināms                             |

Tabulā ir parādīta **Apstrādes statusa** kartēšana starp programmām Sales un Supply Chain Management.

| Apstrādes statuss   | Sales statuss | Supply Chain Management statuss |
|---------------------|-----------------|-----------------------------------|
| Aktīvie              | Aktīvie          | Atvērts pasūtījums                        |
| Apstiprināts           | Iesniegti       | Atvērts pasūtījums                        |
| Izdots              | Iesniegti       | Atvērts pasūtījums                        |
| Daļēji piegādāts | Aktīvie          | Atvērts pasūtījums                        |
| Daļēji iekļauts rēķinā  | Aktīvie          | Atvērts pasūtījums                        |
| Daļēji iekļauts rēķinā  | Izpildīts       | Piegādāts                         |
| Izveidots rēķins            | Izveidots rēķins        | Izveidots rēķins                          |
| Atcelta           | Atcelta       | Atcelta                         |

## <a name="setup"></a>Iestatīt

Lai iestatītu pārdošanas pasūtījuma statusa lauku kartēšanu, ir jāiespējo **IsSOPIntegrationEnabled** un **isIntegrationUser** atribūti.

Lai iespējotu **IsSOPIntegrationEnabled** atribūtu, veiciet tālāk norādītās darbības.

1. Pārlūkā dodieties uz vietni `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Aizstājiet **\<test-name\>** ar uzņēmuma saiti uz Sales.
2. Atvērtajā lapā meklējiet **organizationid** un pierakstiet vērtību.

    ![Organizationid meklēšana](media/sales-map-orgid.png)

3. Sadaļā Sales atveriet pārlūka konsoli un izpildiet šādu skriptu. Izmantojiet **organizationid** vērtību no 2. darbības.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript kods pārlūka konsolē](media/sales-map-script.png)

4. Pārbaudiet, vai **IsSOPIntegrationEnabled** ir iestatīts uz **true**. Izmantojiet URL no 1. darbības, lai pārbaudītu vērtību.

    ![IsSOPIntegrationEnabled ir iestatīts uz true](media/sales-map-integration-enabled.png)

Lai iespējotu **isIntegrationUser** atribūtu, veiciet tālāk norādītās darbības.

1. Sadaļā Sales, dodieties uz **Iestatījumi \> Pielāgošana \> Pielāgot sistēmu**, atlasiet **Lietotāja elementu** un pēc tam atveriet **Veidlapa \> Lietotājs**.

    ![Lietotāja veidlapas atvēršana](media/sales-map-user.png)

2. Lauku pārlūkā meklējiet **Integrēšanas lietotāja režīms** un veiciet dubultklikšķi uz tā, lai to pievienotu veidlapai. Saglabājiet izmaiņas.

    ![Integrēšanas lietotāja režīma lauka pievienošana veidlapai](media/sales-map-field-explorer.png)

3. Sadaļā Sales dodieties uz **Iestatījums \> Drošība \> Lietotāji** un mainiet skatu no **Iespējotie lietotāji** uz **Programmas lietotāji**.

    ![Skata mainīšana no Iespējotajiem lietotājiem uz Programmas lietotājiem](media/sales-map-enabled-users.png)

4. Atlasiet divus ierakstu atribūtus **DualWrite IntegrationUser**.

    ![Programmas lietotāju saraksts](media/sales-map-user-mode.png)

5. Mainiet lauka **Integrēšanas lietotāja režīms** vērtību uz **Jā**.

    ![Lauka Integrēšanas lietotāja režīms vērtības maiņa](media/sales-map-user-mode-yes.png)

Jūsu pārdošanas pasūtījumi tagad ir kartēti.
