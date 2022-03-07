---
title: Nomas apstiprinājuma darbplūsmu iestatīšana
description: Tēmā ir izskaidrots, kā iestatīt apstiprināšanas darbplūsmu, kas tiks palaista, kad tiek izveidota jauna noma.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e7280bbf60901266c81a0c89395c5183f991425
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881666"
---
# <a name="set-up-lease-approval-workflows"></a>Nomas apstiprinājuma darbplūsmu iestatīšana

[!include [banner](../includes/banner.md)]

Tēmā ir izskaidrots, kā iestatīt apstiprināšanas darbplūsmu, kas tiks palaista, kad tiek izveidota jauna noma. Plašāku informāciju par to, kā izmantot darbplūsmu, skatiet tēmā [Nomu apstiprināšanas darbplūsmu izmantošana](use-create-lease-wrkflw.md). 

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas darbplūsma**.
2. Lapā **Nomas darbplūsma** atlasiet **Jauna**.
3. Parādītā dialoglodziņa sadaļā **Darbplūsmas veids** atlasiet saiti **Nomas darbplūsma**.

    Programma ir atvērta. Kad tā ir palaista, pierakstieties Azure Active Directory (Azure AD), lai tiktu novirzīts uz darbplūsmas programmu.

4. Velciet elementu **Nomas darbplūsmas apstiprinājums** uz darbplūsmu.
5. Pievienojiet vienu mezglu no **sākuma** līdz **Nomas darbplūsmas apstiprinājumam**. Pēc tam pievienojiet **Nomas darbplūsmas apstiprinājums** elementam **Beigas**.
6. Veiciet dubultklikšķi uz **Nomas darbplūsmas apstiprinājums**.
7. Atlasiet **Rekvizīti** un pēc tam sadaļā **Pamata iestatījumi** ievadiet darbplūsmas nosaukumu.

    Šajā lapā var arī iestatīt vairāk darbplūsmas parametru. Ja ieslēdzāt elementu **Automātiskās darbības**, sistēma automātiski veiks noteiktu darbību. Paziņojumus var nosūtīt, ja tie ir norādīti cilnē **Paziņojumi**. Cilnē **Papildu iestatījumi** varat norādīt galīgo apstiprinātāju, iestatīt laika ierobežojumu un norādīt konkrētas darbības, kas ir jāpabeidz.

8. Kad esat pabeidzis iestatīt darbplūsmas parametrus, atlasiet **Aizvērt**.
9. Atlasiet **1. darbība** un pēc tam atlasiet **Rekvizīti**.
10. Sadaļā **Pamata iestatījumi** ievadiet darbības nosaukumu, izveidojiet apstiprinājuma tēmas rindu un norādiet apstiprinājuma norādījumus.
11. Lapā **Piešķire** atlasiet piešķires tipu.
12. Lai piešķirtu apstiprināšanai noteiktus lietotājus, atlasiet **Lietotājs**, atlasiet lietotājus, kas apstiprina nomas, un pēc tam atlasiet **Aizvērt**.
13. Atlasiet **Saglabāt un aizvērt**, lai izveidotu darbplūsmu. Pēc tam, kad tiek parādīta uzvedne, atlasiet **Labi**.
14. Lapā **Darbplūsma izveide** atlasiet **Aizvērt**.
14. Atlasiet jauno darbplūsmu un pēc tam atlasiet **Versijas**. Pēc tam atlasiet **Padarīt aktīvu**, lai nodrošinātu, ka darbplūsma ir aktīva.
15. Atlasiet **Aizvērt**. Tiek parādīta jauna aktīvā versija.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
