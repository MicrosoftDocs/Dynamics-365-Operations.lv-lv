---
title: Partijas atribūti
description: Šajā tēmā ir sniegta informācija par partijas atribūtiem. Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi. Tēmā ir arī paskaidrots, kā piešķirt partijas atribūtus un kā tos izmantot meklēšanai, rezervējot partijas.
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 744c8d65d8f1b28dc8197f3f8dd1803f916958b5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246481"
---
# <a name="batch-attributes"></a>Partijas atribūti

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par partijas atribūtiem. Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi. Tēmā ir arī paskaidrots, kā piešķirt partijas atribūtus un kā tos izmantot meklēšanai, rezervējot partijas.

Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi. Partijas atribūti var atšķirties atkarībā no tādiem faktoriem kā vides apstākļi, partijas ražošanai izmantoto izejmateriālu kvalitāte vai saražotās preces rezultāta. Izmantoto partijas atribūtu skaits un veidi var būtiski atšķirties atkarībā no nozares. Tālāk ir sniegti divi partijas atribūtu izmantošanas piemēri:

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
Rezervējat partijas pārdošanas pasūtījumam, lai izpildītu debitora pasūtījumu, vai kad izdodot un rezervējot partijas ražošanas pasūtījumam, varat meklēt partijas pēc partijas atribūtiem. Meklēšana palīdz atrast krājumu partiju, kurā ir ietverta prece, kurai ir vajadzīgais partijas atribūts. Kad esat atradis partiju vai partijas, varat rezervēt preci izcelsmes noliktavas transakcijas rindā.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]