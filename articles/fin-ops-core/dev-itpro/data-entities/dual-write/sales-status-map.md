---
title: Kartējuma iestatīšana pārdošanas pasūtījuma statusa kolonnām
description: Šajā tēmā ir paskaidrots, kā iestatīt pārdošanas pasūtījuma statusa kolonnas duālajam ierakstam.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: damadipa
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 53d824ca2fb1eadf34e62bf9c08b837db3efaf42
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782288"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Kartējuma iestatīšana pārdošanas pasūtījuma statusa kolonnām

[!include [banner](../../includes/banner.md)]

Kolonnām, kas norāda pārdošanas pasūtījuma statusu, ir dažādas numerācijas vērtības programmā Microsoft Dynamics 365 Supply Chain Management un Dynamics 365 Sales. Lai kartētu šīs kolonnas duālajam ierakstam, ir nepieciešams papildu iestatījumi.

## <a name="columns-in-supply-chain-management"></a>kolonnas programmā Supply Chain Management

Programmā Supply Chain Management pārdošanas pasūtījuma statusu ataino divas kolonnas. Kartējamas kolonnas ir **Statuss** un **Dokumentu statuss**.

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

## <a name="columns-in-sales"></a>Pārdošanas kolonnas

Programmā Sales pasūtījuma statusu norāda divas kolonnas. Kartējamās kolonnas ir **Statuss** un **Apstrādes statuss**.

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

    ![Organizationid meklēšana.](media/sales-map-orgid.png)

3. Sadaļā Sales atveriet pārlūka konsoli un izpildiet šādu skriptu. Izmantojiet **organizationid** vērtību no 2. darbības.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript kods pārlūka konsolē.](media/sales-map-script.png)

4. Pārbaudiet, vai **IsSOPIntegrationEnabled** ir iestatīts uz **true**. Izmantojiet URL no 1. darbības, lai pārbaudītu vērtību.

    ![IsSOPIntegrationEnabled ir iestatīts uz true.](media/sales-map-integration-enabled.png)

Lai iespējotu **isIntegrationUser** atribūtu, veiciet tālāk norādītās darbības.

1. Sadaļā Sales, dodieties uz **Iestatījumi \> Pielāgošana \> Pielāgot sistēmu**, atlasiet **Lietotāja tabulu** un pēc tam atveriet **Veidlapa \> Lietotājs**.

    ![Lietotāja veidlapas atvēršana.](media/sales-map-user.png)

2. Lauku pārlūkā meklējiet **Integrēšanas lietotāja režīms** un veiciet dubultklikšķi uz tā, lai to pievienotu veidlapai. Saglabājiet izmaiņas.

    ![Integrēšanas lietotāja režīma kolonnas pievienošana veidlapai.](media/sales-map-field-explorer.png)

3. Sadaļā Sales dodieties uz **Iestatījums \> Drošība \> Lietotāji** un mainiet skatu no **Iespējotie lietotāji** uz **Programmas lietotāji**.

    ![Skata mainīšana no Iespējotajiem lietotājiem uz Programmas lietotājiem.](media/sales-map-enabled-users.png)

4. Atlasiet divus ierakstu atribūtus **DualWrite IntegrationUser**.

    ![Programmas lietotāju saraksts.](media/sales-map-user-mode.png)

5. Mainiet kolonnas **Integrēšanas lietotāja režīms** vērtību uz **Jā**.

    ![Kolonna Integrēšanas lietotāja režīms vērtības maiņa.](media/sales-map-user-mode-yes.png)

Jūsu pārdošanas pasūtījumi tagad ir kartēti.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]