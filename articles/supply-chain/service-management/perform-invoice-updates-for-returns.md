---
title: Rēķinu atjauninājumu veikšana atgrieztajiem krājumiem
description: Šī funkcionalitāte atbalsta uzņēmējdarbības procesus daudzās organizācijās, kas izvēlas vienlaicīgu rēķinu izrakstīšanu atgriešanas pasūtījumiem un pārdošanas pasūtījumiem, un to veic viens darbinieks.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32a108694c11a2ebd922a71d5c82691584bbb397
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014754"
---
# <a name="perform-invoice-updates-for-returns"></a>Rēķinu atjauninājumu veikšana atgrieztajiem krājumiem 

[!include [banner](../includes/banner.md)]


Atgriešanas pasūtījums ir pārdošanas pasūtījuma veids, kas ir atzīmēts kā atgriešanas pasūtījums. Tādēļ atgriešanas pasūtījumu rēķinu ģenerēšanai tiek izmantota saraksta lapa **Visi pārdošanas pasūtījumi**, nevis veidlapa **Atgriešanas pasūtījumi**. Šī funkcionalitāte atbalsta uzņēmējdarbības procesus daudzās organizācijās, kas izvēlas vienlaicīgu rēķinu izrakstīšanu atgriešanas pasūtījumiem un pārdošanas pasūtījumiem, un to veic viens darbinieks.

Tā kā atgriezta krājuma rēķinā ir negatīva summu, to sauc par kredīta notu.

Kad tiek iestatīta rēķina atjaunināšana pakešuzdevumu apstrādei, pārdošanas pasūtījumam, kura tips ir **Atgriešanas pasūtījums**, ir jāatgriež statuss **Saņemts**, kas norāda, ka pasūtījuma pavadzīme tikusi atjaunināta.

## <a name="post-an-invoice-for-a-return-order"></a>Rēķina par atgriešanas pasūtījumu grāmatošana

1.  Klikšķiniet **Debitoru parādu** \> **pasūtījumus** \> **visiem pārdošanas pasūtījumiem**.

2.  Atlasiet pārdošanas pasūtījumu, kuram laukā **Pasūtījuma tips** tiek rādīts vienums **Atgriešanas pasūtījums**.

3.  Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** noklikšķiniet uz **Rēķins**.

4.  Cilnē **Parametri** atzīmējiet izvēles rūtiņu **Grāmatošana**.

5.  Pārskatiet informāciju veidlapā un veiciet nepieciešamās izmaiņas.

6.  Noklikšķiniet uz **Labi**. Kredīta nota ir grāmatota.

## <a name="see-also"></a>Skatiet arī

[Pavadzīmju atjauninājumi atgrieztajiem krājumiem](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]