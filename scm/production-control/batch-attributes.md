---
title: "Partijas atribūti"
description: "Šajā rakstā ir sniegta informācija par partijas atribūtiem. Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi. Rakstā ir sniegts arī skaidrojums, kā piešķirt partijas atribūtus un kā var tos meklēt, rezervējot partijas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8225460ccb311c79db45d618e8b02233e7bab51c
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="batch-attributes"></a>Partijas atribūti

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par partijas atribūtiem. Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi. Rakstā ir sniegts arī skaidrojums, kā piešķirt partijas atribūtus un kā var tos meklēt, rezervējot partijas.

Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi. Partijas atribūti var atšķirties atkarībā no tādiem faktoriem kā vides apstākļi, partijas ražošanai izmantoto izejmateriālu kvalitāte vai saražotās preces rezultāta. Izmantoto partijas atribūtu skaits un veidi var būtiski atšķirties atkarībā no nozares. Tālāk ir sniegti divi partijas atribūtu izmantošanas piemēri.

-   Siera ražošanas nozarē pienam, kas ir viens no siera ražošanas izejmateriāliem, var būt tādi atribūti kā tauku saturs un procentuālais svars. No piena saražotajam sieram var būt citi atribūti, piemēram, mitrums un noturēšanas ilgums.
-   Tērauda ražošanas nozarē saražotajai dzelzij var būt tādi atribūti kā magnija saturs procentos, sudraba saturs procentos un cinka saturs procentos.

Lai labāk pārvaldītu atribūtu skaitu un veidus, varat izmantot partijas atribūtu grupas. Tādējādi nav jāpievieno katrs atribūts atsevišķi.

## <a name="assign-batch-attributes"></a>Partijas atribūtu piešķiršana
Varat piešķirt partijas atribūtus atsevišķām precēm, kas ir ietvertas krājumu partijās, vai precēm, kas ir saistītas ar noteiktiem debitoriem. Pirms partijas atribūta piešķiršanas debitora līmenī, tas ir jāpiešķir preces līmenī. Precei izsekošanas dimensiju grupā ir jāiestata partijas dimensijas opcija **Aktīvs**. Lai piešķirtu partijas atribūtu atsevišķai precei, izmantojiet šīs preces lapu. Ja atribūts ir raksturīgs noteiktam debitoram paredzētai precei, izmantojiet attiecīgā debitora lapu. Pievienojot precei atribūtu, jūs definējat arī citus parametrus. Daži piemēri:

-   Minimālās un maksimālās vērtības diapazons atribūtam, kura tips ir **Vesels skaitlis** vai **Daļskaitlis**.
-   Pielaides darbības atribūtam, kura tips ir **Vesels skaitlis** vai **Daļskaitlis**. Ja atribūta vērtība ir ārpus minimālās un maksimālās vērtības diapazona, tad šī darbība var būt brīdinājuma vai kļūdas ziņojuma parādīšana.
-   Atribūta mērķa vērtība. Tā ir atribūta optimālā vērtība un attiecas uz visiem atribūtu tipiem.

To preču lapām, kuras atlasāt lapā **Izlaistās preces**, varat piekļūt modulī Preču informācijas pārvaldība. Pēc partijas atribūtu piešķiršanas precei varat pievienot atribūtiem noteiktas vērtības lapā **Krājumu partijas atribūti**.

## <a name="reserve-batches"></a>Partiju rezervēšana
Varat meklēt pēc partijas atribūtiem, kad rezervējat partijas pārdošanas pasūtījumam, lai izpildītu debitora pasūtījumu, vai kad izdodat un rezervējat partijas ražošanas pasūtījumam. Meklēšana palīdz atrast krājumu partiju, kurā ir ietverta prece, kurai ir vajadzīgais partijas atribūts. Kad esat atradis partiju vai partijas, varat rezervēt preci izcelsmes noliktavas transakcijas rindā.



