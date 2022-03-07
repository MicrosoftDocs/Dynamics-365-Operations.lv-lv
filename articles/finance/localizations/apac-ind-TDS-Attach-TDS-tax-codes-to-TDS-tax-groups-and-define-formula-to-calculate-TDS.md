---
title: Pievienojiet TDS nodokļu kodus TDS nodokļu grupām un definējiet TDS aprēķināšanas formulu
description: Šajā tēmā ir paskaidrots, kā iestatīt No kopējo ienākumu summas atskaitītā (TDS) nodokļu grupas un pievienot TDS nodokļu kodus TDS nodokļu grupām. Lai aprēķinātu TDS nodokļu grupai, jums ir jādefinē formula TDS nodokļu kodiem, kas tam piesaistīti.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 98d6ceb794716f39c6ae47b300bdb7618a8e688b
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345232"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>Pievienojiet TDS nodokļu kodus TDS nodokļu grupām un definējiet TDS aprēķināšanas formulu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt No kopējo ienākumu summas atskaitītā (TDS) nodokļu grupas un pievienot TDS nodokļu kodus TDS nodokļu grupām. Lai aprēķinātu TDS nodokļu grupai, jums ir jādefinē formula TDS nodokļu kodiem, kas tam piesaistīti.

Sekojiet šiem soļiem, lai iestatītu TDS nodokļu grupu, tai pievienotus TDS nodokļu kodus un definētu formulu TDS aprēķināšanai.

1. Pārejiet uz sadaļu **Nodokļi \> Netiešie nodokļi \> Ieturētais nodoklis \> Ieturētā nodokļa grupas**.

    [![Ieturēto nodokļu grupas lapa.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Darbību rūtī atlasiet **Jauns**, lai izveidotu ieturētā nodokļa grupu TDS, un ievadiet nepieciešamo informāciju.
3. Laukā **Nodokļa veids** atlasiet **TDS**.
4. Kopsavilkuma cilnē **Iestatīšana** atlasiet **Pievienot**, lai izveidotu rindu.
5. Laukā **Ieturētā nodokļa kods** atlasiet ieturētā TDS nodokļa kodu TDS nodokļu grupai. Laukā **Ieturētā nodokļa nosaukums** tiek rādīts TDS nodokļa koda nosaukums, un lauks **Vērtība** rāda vērtību.
6. Lai ignorētu TDS nodokļu komponentam definēto sliekšņa ierobežojumu un izņēmuma sliekšņa ierobežojumu TDS nodokļu kodam TDS darījumos, atzīmējiet izvēles rūtiņu **Neievērot slieksni**.
7. Atlasiet **Atbrīvot** izvēles rūtiņu, lai novērstu nodokļu grupas aprēķināšanu darījumos.
8. Darbību rūtī atlasiet **Veidotājs**, lai atvērtu formulas noformētāju, tādējādi varat definēt formulu TDS aprēķināšanai TDS nodokļu grupai. Lapā **Veidotājs** cilne **Nodokļi** rāda TDS nodokļu kodus, kas ir atlasīti TDS nodokļu grupai.

    [![Veidotāja lapa.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Cilnē **Aprēķins** atlasiet **Alt+N**, lai izveidotu rindu. **ID** lauks parāda automātiski ģenerēto prioritātes ID TDS aprēķinam.
10. Laukā **Nodokļa kods** atlasiet ieturētā TDS nodokļa kodu, kam definēt formulu. Visi TDS nodokļu kodi, kas atlasīti TDS nodokļu grupai, ir pieejami atlasei šajā laukā.
11. Laukā **Apliekamās bāzes** izvēlieties pamatu TDS aprēķināšanai:

    - **Bruto summa** – aprēķina TDS, pamatojoties uz bruto darbību summu (t.i., rēķina summu), izmantojot aprēķina izteiksmi, kas definēta nodokļa kodam.
    - **Bez bruto summas** – aprēķiniet TDS, pamatojoties uz nodokļu kodam definēto aprēķina izteiksmi.

    > [!NOTE]
    > Lauku **Apliekamās bāzes** nevar iestatīt uz **Bez bruto summas** TDS nodokļa kodam, kam ir prioritātes ID **1**.

12. TDS aprēķina pamatā ir formula, kas laukā **Aprēķina izteiksme** noteikta katram nodokļu kodam, kas ir piesaistīts TDS nodokļu grupai. Atlasiet pluszīmi (+), mīnuszīmi (-), reizināšanai zīmi (\*) vai dalīšanas zīmi (/) lai ievadītu aprēķina izteiksmi atlasītam TDS nodokļa kodam laukā **Aprēķina izteiksme**.

    > [!NOTE]
    > TDS nodokļa kodam, kura prioritātes ID ir **1**, nevar definēt aprēķina izteiksmi.

13. Lai definētu aprēķina izteiksmi TDS nodokļu kodam **Aprēķina izteiksmes** laukā, pievienojiet TDS nodokļu kodus, kas ir pieejami cilnē **Nodokļi**. Lai pievienotu TDS nodokļu kodus laukā **Aprēķina izteiksme**, varat izmantot jebkuru no šīm metodēm:

    - Velciet nepieciešamo nodokļa kodu no cilnes **Nodokļi** uz lauku **Aprēķina izteiksme**.
    - Veiciet dubultklikšķi uz nepieciešamā nodokļu koda cilnē **Nodokļi**.
    - Atlasiet un turiet (vai veiciet labo klikšķi) pieprasīto nodokļu kodu cilnē **Nodokļi** un pēc tam atlasiet **Pievienot nodokļa kodu**.

    > [!NOTE]
    > Pirms katra TDS nodokļa koda ievietojiet aprēķina izteiksmi. Aprēķina izteiksmei pievienotie TDS nodokļu kodi ir redzami iekavās (\[...\]).

14. Lai notīrītu aprēķina izteiksmi, kas noteikta nodokļu kodam laukā **Aprēķina izteiksme**, atlasiet **C** pogu.
15. Lai dzēstu ierakstu cilnē **Aprēķins**, atlasiet **Dzēst**.
16. Aizvērt lapu.
