---
title: Nomas apstiprinājuma darbplūsmu izmantošana
description: Šajā tēmā skaidrots, kā izmantot darbplūsmas, lai apstiprinātu līdzekļu nomas, un kā izsekot darbplūsmas statusu un vēsturi.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f19cb0be14ba784cc4c3d189f4d2b5b00426e1b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249561"
---
# <a name="use-lease-approval-workflows"></a>Nomas apstiprinājuma darbplūsmu izmantošana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā izmantot darbplūsmas, lai apstiprinātu līdzekļu nomas, un kā izsekot darbplūsmas statusu un vēsturi. Darbplūsmas palīdz sakārtot nomas apstiprinājumu pārvaldību, nodrošinot standarta apstiprināšanas darbības un piešķirot noteiktus lietotājus, kas apstiprina katru procesa darbību. Apstiprinātājs var apstiprināt nomu, noraidīt to, pieprasīt izmaiņas tajā vai piešķirt to citam lietotājam apstiprināšanai. Darbplūsmas var arī radīt lielāku redzamību apstiprināšanas procesā, ļaujot izsekot to statusu un vēsturi. Var arī skatīt centralizētu darbu sarakstu, kas uzskaita uzdevumus un apstiprinājumus, kuri ir piešķirti noteiktiem apstiprinātājiem.

Pirms šīs procedūras izmantošanas pārliecinieties, ka vismaz nomas apstiprinājuma darbplūsma ir izveidota. Ja neviena darbplūsma nepastāv, izveidojiet to. Plašāku informāciju par to, kā iestatīt darbplūsmu, skatiet tēmā [Nomu apstiprināšanas darbplūsmu iestatīšana](set-up-lease-wrkflw.md).

1. Iesniedziet nomu apstiprināšanai. Lapā **Grāmatas informācija** nomai atlasiet elementu **Darbplūsma** un pēc tam atlasiet **Iesniegt**.
2. Dialoglodziņā, kas parādās, varat pievienot komentāru. Nozīmētais apstiprinātājs redzēs šo komentāru kopā ar nomu. Kad esat pabeidzis komentāra ievadi, atlasiet **Iesniegt**. Noma tiek iesniegta darbplūsmas sistēmā, un apstiprinātājs to saņem apstiprināšanai.
3. Lai skatītu nomas, kas nozīmētas apstiprināšanai, dodieties uz **Moduļi \> Vispārēji \> Darba vienumi \> Man piešķirtie darbplūsmas elementi**.
4. Lapā **Man piešķirtie darba elementi** atlasiet saiti **nomas ID** nomai, ko vēlaties skatīt. Lapa, kas tiek parādīta, ir atkarīga no nomas grāmatām un nomas detaļām, kurām jums ir piekļuve.
5. Kad ir pabeigta nomas skatīšana, atlasiet **Darbplūsma** un izlemiet, kādas darbības jāveic. Opcijas ietver **Apstiprināt**, **Noraidīt**, **Pieprasīt izmaiņas**, **Deleģēt** un **Atcelts**. Varat arī atlasīt **Skatījuma vēsture**, lai skatītu atlasītās nomas apstiprināšanas vēsturi.
6. Pēc tam, kad esat atlasījis darbību, ievadiet komentāru, lai aprakstītu darbību. Kad esat pabeidzis komentāra ievadi, sarakstā atlasiet **apstiprināto** darbību.
7. Lai skatītu apstiprināšanas darbības, atgriezieties lapā **Nomas informācija** no lapas **Nomas kopsavilkums** un pēc tam atlasiet **Darbplūsma \> Skatīt vēsturi**.

    Darbplūsmas darbības var skatīt lapā **Darbplūsmas vēsture**. Šī lapa parāda darbplūsmas darbības kas tika veiktas konkrētajā nomā. Lai apskatītu piešķirto darba elementu statusu, varat izmantot arī lauku **Darba elementi**.

8. Lai pārtrauktu darbplūsmu, lapā **Darbplūsmas vēsture** atlasiet **Atsaukt**. Parādītajā dialoglodziņā ievadiet komentāŗu un pēc tam atlasiet **Labi**.
9. Lai deaktivizētu darbplūsmu vai lai aktivizētu darbplūsmu, kas iepriekš izveidota, dodieties uz **Līdzekļu noma \> Iestatīšana \> Nomas darbplūsma**. Pēc tam lapā **Nomas darbplūsma** atlasiet **Darbplūsma \> Versijas**. Lai pašreizējo darbplūsmu padarītu neaktīvu, nomas versijas dialoglodziņā atlasiet aktīvo nomu un pēc tam atlasiet **Padarīt neaktīvu**. Lai aktivizētu esošo darbplūsmu, atlasiet darbplūsmu un pēc tam atlasiet **Padarīt aktīvu**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]