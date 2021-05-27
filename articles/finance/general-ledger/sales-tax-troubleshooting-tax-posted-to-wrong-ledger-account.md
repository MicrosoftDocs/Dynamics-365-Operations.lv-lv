---
title: Nodoklis ir grāmatots nepareizam virsgrāmatas kontam dokumentā
description: Šajā tēmā sniegta traucējummeklēšanas informācija, kas var palīdzēt, grāmatojot nodokļus nepareizam Virsgrāmatas kontam dokumentā.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020095"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Nodoklis ir grāmatots nepareizam virsgrāmatas kontam dokumentā

[!include [banner](../includes/banner.md)]

Grāmatošanas laikā nodoklis varētu būt grāmatots nepareizam virsgrāmatas kontam dokumentā. Lai novērstu šo problēmu, ja nepieciešams, veiciet tālāk norādītās darbības. Piemēri šajā tēmā izmanto pārdošanas pasūtījumu kā biznesa dokumentu.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Atrast nepareizi grāmatotās nodokļu transakcijas nodokļu kodu

1. Lapā **Dokumentu transakcijas** atlasiet transakciju, ar kuru vēlaties strādāt, un pēc tam atlasiet **Grāmatotais PVN**.

    [![Grāmatotā PVN poga dokumentu transakciju lapā](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Pārskatiet vērtību laukā **PVN kods**. Šajā piemērā tas ir **PVN 19**.

    [![PVN koda lauks lapā Grāmatotais PVN](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Pārbaudīt PVN koda Virsgrāmatas grāmatošanas grupu

1. Dodieties uz **Nodoklis** \> **Netiešie nodokļi** \> **PVN** \> **PVN kodi**.
2. Atrodiet un atlasiet nodokļa kodu un pēc tam pārskatiet vērtību laukā **Virsgrāmatas grāmatošanas grupa**. Šajā piemērā tas ir **PVN**.

    [![Virsgrāmatas grāmatošanas grupas lauks lapā PVN kodi](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. Lauka **Virsgrāmatas grāmatošanas grupas** vērtība ir saite. Lai apskatītu grupas konfigurācijas detaļas, izvēlieties saiti. Pēc izvēles atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) laukā un pēc tam atlasiet **Skatīt detalizētu informāciju**.

    [![Komanda Skatīt informāciju](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. Laukā **Maksājamais PVN** pārbaudiet, vai konta numurs ir pareizs atbilstoši transakciju tipam. Ja tā nav, atlasiet pareizo kontu, ar kuru grāmatot. Šajā piemērā pārdošanas pasūtījuma PVN ir jāgrāmato maksājamā PVN kontā 222200.

    [![Lauks Maksājamais pārdošanas nodoklis lapā Virsgrāmatas grāmatošanas grupas](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Šajā tabulā sniegta informācija par katru lauku **Virsgrāmatas grāmatošanas grupu** lapā.

    | Lauks                  | Apraksts |
    |------------------------|-------------|
    | Maksājamais PVN      | Galvēnais konts izejošiem PVN, kas jāmaksā PVN iestādei. |
    | Saņemtais PVN   | Galvēnais konts ienākošajiem nodokļiem, kas saņemti no PVN iestādes. |
    | Importa nodokļa izdevumi        | Galvenais konts, kas tiek izmantots, lai iegrāmatotu atskaitāmos lietošanas nodokļus, kurus kreditori nepieprasa vai neiesniedz nodokļu administrācijai kā daļu no Eiropas Savienības (ES) apgrieztās maksāšanas preču un pakalpojumu nodokļa (PPN)/saskaņotā PVN (Harmonized Sales Tax - HST). Opcijai **Izmantošanas nodoklis** ir jābūt atlasītai PVN kodam PVN grupā, kas tiek izmantota transakcijā. Šis lauks nav pieejams, ja lapā **Virsgrāmatas parametri** ir atlasīts **Piemērot PVN nodokļu sistēmas kārtulas**. |
    | Maksājamais importa nodoklis        | Galvenais konts, ko lieto, lai grāmatotu ienākošos importa nodokļus, kas jāmaksā nodokļu iestādēm. |
    | Maksājumu konts     | Galvenais konts tiek izmantots, lai grāmatotu neto bilanci no Virsgrāmatas kontiem, kas norādīti laukos **Maksājamais importa nodoklis** un **Saņemamais PVN**. |
    | Kreditora termiņatlaide   | Galvenais konts, ko izmanto, lai grāmatotu termiņatlaidi PVN kodiem, kas saistīti ar šo Virsgrāmatas grāmatošanas grupu. |
    | Debitora gadījuma atlaide | Galvenais konts, ko izmanto, lai grāmatotu termiņatlaidi PVN kodiem, kas saistīti ar šo Virsgrāmatas grāmatošanas grupu. |

    Papildinformācijai skatiet [Virsgrāmatas PVN grāmatošanas grupu iestatīšana](tasks/set-up-ledger-posting-groups-sales-tax.md)

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Atkļūdošanas kods Virsgrāmatas dimensiju pārbaudei

Kodā grāmatošanas kontu nosaka Virsgrāmatas dimensija. Virsgrāmatas dimensija saglabā konta ieraksta ID datu bāzē.

1. Pārdošanas pasūtījumam pievienojiet pārtraukumpunktu metodēs **Tax::saveAndPost()** un **Tax::post()**. Jāpievērš uzmanība vērtībai **\_ledgerDimension**.

    [![Pārdošanas pasūtījuma koda paraugs, kam ir pārtraukumpunkts](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Pirkšanas pasūtījumam pievienojiet pārtraukumpunktu metodes **TaxPost::saveAndPost()** un **TaxPost::postToTaxTrans()**. Jāpievērš uzmanība vērtībai **\_ledgerDimension**.

    [![Pirkšanas pasūtījuma koda paraugs, kam ir pārtraukumpunkts](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Palaidiet šādu SQL vaicājumu, lai atrastu konta parādāmo vērtību datu bāzē, balstoties uz ieraksta ID, kas saglabāts ar Virsgrāmatas dimensiju.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Rādīt ieraksta ID vērtību](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Pārbaudiet izsaukumus, lai atrastu, kur **_ledgerDimension** ir piešķirts. Parasti vērtība ir no **TmpTaxWorkTrans**. Šajā gadījumā ir jāpievieno pārtraukumpunkts pie **TmpTaxWorkTrans::insert()** un **TmpTaxWorkTrans::update()**, lai atrastu piešķirto vērtību.

## <a name="determine-whether-customization-exists"></a>Noteikt, vai pielāgojums pastāv

Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē. Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
