---
title: Nomas apstiprinājuma darbplūsmu izmantošana
description: Šajā rakstā ir izskaidrots, kā izmantot darbplūsmas līdzekļu nomas apstiprināšanai un kā sekot darbplūsmu statusam un vēsturei.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4205b83919f0b3c30a4b5d8e3290af230f538f39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906447"
---
# <a name="use-lease-approval-workflows"></a>Nomas apstiprinājuma darbplūsmu izmantošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā izmantot darbplūsmas līdzekļu nomas apstiprināšanai un kā sekot darbplūsmu statusam un vēsturei. Darbplūsmas palīdz sakārtot nomas apstiprinājumu pārvaldību, nodrošinot standarta apstiprināšanas darbības un piešķirot noteiktus lietotājus, kas apstiprina katru procesa darbību. Apstiprinātājs var apstiprināt nomu, noraidīt to, pieprasīt izmaiņas tajā vai piešķirt to citam lietotājam apstiprināšanai. Darbplūsmas var arī radīt lielāku redzamību apstiprināšanas procesā, ļaujot izsekot to statusu un vēsturi. Var arī skatīt centralizētu darbu sarakstu, kas uzskaita uzdevumus un apstiprinājumus, kuri ir piešķirti noteiktiem apstiprinātājiem.

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
