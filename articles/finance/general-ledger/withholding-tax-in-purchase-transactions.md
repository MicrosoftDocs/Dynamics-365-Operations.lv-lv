---
title: Ieturētais nodoklis pirkšanas darījumos
description: Piegādātājiem, uz kuriem attiecas ieturamais nodoklis, varat piešķirt noklusēto **Ieturētā nodokļa grupu** lapā **Visi piegādātāji**.
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
ms.openlocfilehash: c2220159cef31bf3343bcf39325c7a0ff3e0cf47
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727207"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Ieturētais nodoklis pirkšanas darījumos

Piegādātājiem, uz kuriem attiecas ieturamais nodoklis, varat piešķirt noklusēto **Ieturētā nodokļa grupu** lapā **Visi piegādātāji**.

1. Dodieties uz **Navigācijas rūts > Moduļi > Kreditori > Piegādātāji > Visi piegādātāji**.

2. Noklikšķiniet uz attiecīgā piegādātāja konta, noklikšķiniet uz **Rediģēt**.

3. Cilnē **Rēķins un piegāde** iestatiet lauku **Aprēķināt ieturēto nodokli** uz **Jā**.

   > [!NOTE] 
   > Ieturētais nodoklis netiks aprēķināts, ja datos šim piegādātājam nav ieslēgts **Aprēķināt ieturēto nodokli**.

4. Atlasiet ieturētā nodokļa grupu **Ieturētā nodokļa grupa**.

5. Noklikšķiniet uz **Saglabāt**.

Krājumiem/pakalpojumiem, kas ir apliekami ar ieturēto nodokli, varat piešķirt noklusējuma **Krājuma ieturētā nodokļa grupu** sadaļā **Izlaistās preces**.

1. Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.

2. Noklikšķiniet uz attiecīgā vienuma numura, noklikšķiniet uz **Rediģēt**.

3. Cilnē **Pirkums** noklikšķiniet uz **Aprēķināt ieturēto nodokli**.

   > [!NOTE] 
   > Ieturētais nodoklis netiks aprēķināts, ja **Aprēķināt ieturēto nodokli** nav iestatīts uz **Jā** šim krājumam cilnē **Pirkt** lapā **Izlaistās preces**.

4. Atlasiet krājuma ieturētā nodokļa grupu sarakstā **Krājuma ieturētā nodokļa grupa**.

5. Noklikšķiniet uz **Saglabāt**.

Ieturētā nodokļa grupas un krājuma ieturētā nodokļa grupas var piešķirt tālāk minētajās lapās. 

- **Pirkšanas pasūtījums**
- **Kreditora rēķins**
- **Rēķinu žurnāls**

Noklusējuma ieturētā nodokļa grupa un vienuma ieturētā nodokļa grupa tiks iekļauta rindās, veidojot **Pirkšanas pasūtījumus** un/vai **Neapmaksātos piegādātāja rēķinus**. **Piegādātāju rēķinu žurnālam** varat ieslēgt **Aprēķināt ieturēto nodokli** un atlasīt **Vienuma ieturētā nodokļa grupa** žurnāla cilnē **Vispārīgi**.

Ieturētā nodokļa pagaidu summa ir pieejama laukā **Koriģētais ieturētais nodoklis** cilnē **Kopsummas** lapā **Pirkšanas pasūtījums**.

![Ieturētais nodoklis ir iekļauts pirkšanas pasūtījumā.](media/withholding-tax-adjusted.png)

Ieturētais nodoklis tiek aprēķināts **Piegādātāja maksājumu žurnālā**. Varat manuāli koriģēt piemērojamos ieturētā nodokļa kodus, kā arī faktiskās ieturētā nodokļa summas cilnē **Ieturētais nodoklis** lapā **Transakciju kārtošana**.

![Ieturēto summu var manuāli koriģēt lapā Transakciju izpilde.](media/withholding-tax-vendor-payment-tab.png)

Atvasinātā ieturētā nodokļa summa tiks atskaitīta no piegādātāja maksājuma un grāmatota **Ieturētā nodokļa korespondējošais konts** saistītā dokumentā.

![Ieturētā nodokļa konts, kas rāda saistīto dokumentu.](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
