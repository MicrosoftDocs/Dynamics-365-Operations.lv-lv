---
title: Ieturētais nodoklis pārdošanas darījumos
description: Šajā rakstā ir norādītas darbības, kas jāveic, lai atlasītajiem debitoriem nepieļautu ieturamā nodokļa aprēķinu. Debitoriem, kuri savos maksājumos norāda ieturamo nodokli, varat piešķirt noklusēto ieturētā nodokļa grupu.
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 75a7fc62c1d493007f3aa88a723465828c557df7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910089"
---
# <a name="withholding-tax-in-sales-transactions"></a>Ieturētais nodoklis pārdošanas darījumos

Šajā rakstā ir norādītas darbības, kas jāveic, lai atlasītajiem debitoriem nepieļautu ieturamā nodokļa aprēķinu. Klientiem, kuri savos maksājumos norāda ieturamo nodokli, varat piešķirt noklusēto **Ieturētā nodokļa grupu** lapā **Klienti**. 

1. Dodieties uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Klienti > Visi klienti**.

2. Noklikšķiniet uz attiecīgā klienta konta, noklikšķiniet uz **Rediģēt**.

3. Cilnē **Rēķins un piegāde** iestatiet lauku **Aprēķināt ieturēto nodokli** uz **Jā**.

   > [!NOTE] 
   > Ieturētais nodoklis netiks aprēķināts, ja pamatdatos šim klientam nav ieslēgts **Aprēķināt ieturēto nodokli**.

4. Atlasiet ieturētā nodokļa grupu **Ieturētā nodokļa grupa**.

5. Noklikšķiniet uz **Saglabāt**.

Krājumiem/pakalpojumiem, kas ir apliekami ar ieturēto nodokli, varat piešķirt noklusējuma **Krājuma ieturētā nodokļa grupu** sadaļā **Izlaistās preces**.

1. Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.

2. Noklikšķiniet uz attiecīgā vienuma numura, noklikšķiniet uz **Rediģēt**.

3. Cilnē **Pārdošana** noklikšķiniet uz **Aprēķināt ieturēto nodokli**.

   > [!NOTE] 
   > Ieturētais nodoklis netiks aprēķināts, ja **Aprēķināt ieturēto nodokli** nav iestatīts uz **Jā** šim krājumam cilnē **Pārdot** lapā **Izlaistās preces**.

4. Atlasiet krājuma ieturētā nodokļa grupu sarakstā **Krājuma ieturētā nodokļa grupa**.

5. Noklikšķiniet uz **Saglabāt**.

Ieturētā nodokļa grupas un krājuma ieturētā nodokļa grupas var piešķirt, izmantojot lapu **Pārdošanas pasūtījums**. 

Noklusējuma ieturētā nodokļa grupa un krājuma ieturētā nodokļa grupa tiks izmantota kā noklusējuma ieraksti pārdošanas pasūtījuma rindās, veidojot jaunu pārdošanas pasūtījumu.

Ieturētais nodoklis tiek aprēķināts un grāmatots **Klientu maksājumu žurnālā**. Varat manuāli koriģēt piemērojamo ieturētā nodokļa kodu, kā arī faktisko ieturētā nodokļa summu cilnē **Ieturētais nodoklis** lapā **Transakciju kārtošana**.

Aprēķinātā ieturētā nodokļa summa tiks atskaitīta no klienta maksājuma un grāmatota kontā **Ieturētā nodokļa korespondējošais konts** saistītā dokumentā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
