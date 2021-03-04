---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 27. novembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d6b5f5f7b62c400679df5eb014dee05f02e11d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461855"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-27-2018"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 27. novembris)

**8.1.2064 būvējums**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.


## <a name="changes"></a>Izmaiņas

### <a name="unable-to-create-a-note-in-case-management"></a>Nevar izveidot piezīmi pieteik. pārvaldībā

Ir veiktas izm. attiecībā uz problēmu, mēģinot rediģēt vai izveidot piezīmi pieteik. pārvald. pieteik. žurnālā.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Kļūdains vārds atlīdzības darbvietas cilnē Analīze 

Ir veiktas izmaiņas, lai labotu teksta “Etniskā izcelsme” pareizrakstību atlīdzības darbvietas atlīdzības analīzes diagrammā.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Darbinieku pašapkalp. darbv. netiek rādīta, ja lietotājs nav piešķirts nodarbinātajam 

Ir veiktas izm. gadījumos, kad darbv. **Darbinieku pašapkalpošanās** ir atlasīta kā pirmā lapa, sākot darbu, lietotājam, kas nav piešķirts nodarbinātajam. Šādā gadījumā tiks parādīts noklusējuma inform. panelis.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Vienumu Atvaļin. un Kavēj. kļūda: obj. atsauce nav iestatīta uz obj. instanci

Veiktas izm. vienumam Atvaļin. un Kavēj., lai labotu šo kļūdu pēc atvaļin. un kavēj. ierakstu apstipr. sarakstā **Darba vien., kas saistīti ar mani**.

### <a name="unable-to-recall-an-image-workflow"></a>Nevar atsaukt attēlu darbplūsmu

Pēc attēlu darbplūsmas atsaukšanas darbplūsma tiks iestatīta uz “atcelts” un esošo pieprasījumu var dzēst darbinieku pašapkalpošanās darbvietā.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Atkārt. pieņemti darb./līgumd. parādās vair. reizes pēc darba att. beigām 

Ar šo atjaun. atlaistie darb., kas pieņemti atkārt., parādās aizgājušo darb. sarakstā tikai 1 reizi. 

## <a name="known-issue"></a>Zināma problēma

- **Problēma**: kad nodarbinātajam tiek pievienots jauns pielikums, poga **Jauns** un **Rediģēt** ir pelēkotas. 
- **Risinājums:** pirms pielikuma lapas atvēršanas ir jāpārliecinās, vai papildinformācijas lodziņi lapā **Nodarbinātais** ir aizvērti. Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas. (Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]