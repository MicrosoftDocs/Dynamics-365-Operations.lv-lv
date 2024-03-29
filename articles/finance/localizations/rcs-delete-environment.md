---
title: Regulatory Configuration Service (RCS) — RCS vides dzēšana
description: Šajā rakstā skaidrots, kā regulēšanas konfigurācijas pakalpojuma (RCS) sistēmas administrators var dzēst RCS vidi un saistītos datus.
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277246"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) — RCS vides dzēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā regulēšanas konfigurācijas pakalpojuma (RCS) sistēmas administrators var dzēst RCS vidi un saistītos datus.

Pirms varat veikt procedūru šajā rakstā, jābūt izpildītiem šādiem priekšnosacījumi:

- RCS videi ir jābūt piešķirtai lomai **Sistēmas administrators**.
- Lomai **Sistēmas administrators** ir jābūt piešķirtai lomai **RCSDeleteEnvironmentDuty**.

## <a name="delete-an-rcs-environment"></a>RCS vides dzēšana

1. Atvēriet RCS un atlasiet darbvietas elementu **Elektronisko pārskatu veidošana**.
2. Sadaļā **Saistītās saites** atlasiet **Dzēst RCS vidi**.

    ![Dzēst RCS vides saiti sadaļā Saistītās saites.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Dialoglodziņā, kas tiek parādīts, pārskatiet ziņojumus par vides dzēšanas tvērumu.

    ![Ziņojumi RCS vides dzēšanas dialoglodziņā.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > RCS vides dzēšanu nevar atcelt.
    >
    > Ar šo darbību tiek dzēsta atlasītā RCS vide un jebkuri saistītie dati, tostarp līdzekļi un konfigurācijas, kas tiek glabātas Globālajā repozitorijā. Līdzekļi un konfigurācijas, kas tiek koplietotas ar citām organizācijām, netiks kopīgotas un tiks dzēstas, ja tām nav atkarību. Līdzekļi un konfigurācijas, kurām ir atkarības, tiks atzīmētas kā pārtrauktas.

4. Sniegtajā laukā ievadiet RCS vides vispārēji unikālo identifikatoru (GUID), lai apstiprinātu, ka vēlaties to dzēst. Vides GUID ir ietverts dzēšanas ziņojumā.
5. Atlasiet **Dzēst vidi**.
    
Jūsu RCS vide un jebkuri saistītie dati tagad tiek dzēsti.

> [!IMPORTANT]
> Pēc RCS vides dzēšanas datus nevar atkopt. Jaunu RCS vidi var izveidot jebkurā pieejamā RCS reģionā.
