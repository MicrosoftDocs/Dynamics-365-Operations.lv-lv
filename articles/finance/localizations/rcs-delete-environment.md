---
title: Regulatory Configuration Service (RCS) - dzēst RCS vidi
description: Šajā tēmā skaidrots, kā Regulatory Configuration Service (RCS) sistēmas administrators var dzēst RCS vidi un saistītos datus.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: cf82abbe5493eac9665323738441fa016205e9ef
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355011"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - dzēst RCS vidi

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā Regulatory Configuration Service (RCS) sistēmas administrators var dzēst RCS vidi un saistītos datus.

Pirms varat pabeigt šajā tēmā norādīta procedūra, jāizpilda šādi priekšnosacījumi:

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
