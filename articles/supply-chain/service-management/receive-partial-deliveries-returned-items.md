---
title: Atgriezto krājumu daļēju piegāžu saņemšana
description: Daļējas piegādes tiek definētas atgriešanas pasūtījuma rindās, nevis atgriešanas pasūtījuma sūtījumā.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c0e27e3a5cb6be36a1d69190ce1b01ecada48a6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677119"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Atgriezto krājumu daļēju piegāžu saņemšana    

[!include [banner](../includes/banner.md)]


Daļējas piegādes tiek definētas atgriešanas pasūtījuma rindās, nevis atgriešanas pasūtījuma sūtījumā.

Tas nozīmē, ka gadījumā, ja saņemat visu daudzumu, kas ir norādīts atgriešanas pasūtījuma rindā, bet nesaņemat neko no atgriešanas pasūtījuma citām rindām, piegāde nav daļēja piegāde. Tomēr, ja atgriešanas pasūtījuma rindās norādītas attiecīgās atgriežamās preces 10 vienības, bet jūs saņemat tikai 4, tā ir daļēja piegāde.

Ja atgrieztajā sūtījumā ir mazāk nekā pilns daudzums no atgriešanas pasūtījuma rindas, jūs varat sūtījumu rezervēt un nogaidīt, līdz tiek saņemts pārējais daudzums vai arī varat reģistrēt un grāmatot daļēju daudzumu.

## <a name="register-and-post-a-partial-quantity"></a>Reģistrēt un grāmatot daļēju daudzumu

1.  Kad ir atlasīts atgriešanas pasūtījums saņemšanai, formā **Saņemšanas darbību apskats — noliktava: %1, doks: %2, žurnāla nosaukums: %3** noklikšķiniet uz **Sākt saņemšanu**, lai izveidotu saņemšanas žurnālu, un pēc tam noklikšķiniet uz vienuma **Žurnāli** \> **Rādīt saņemšanas no ieejas plūsmām**, lai atvērtu formu **Novietojumu žurnāls**.

2.  Atlasiet žurnāla rindu, ar kuru vēlaties strādāt, un pēc tam noklikšķiniet uz **Rindas**, lai atvērtu veidlapu **Žurnāla rindas, novietojumi**.

3.  Atlasiet krājuma koda rindu, kurai ir saņemts tikai daļējs daudzums un tad noklikšķiniet uz **Funkcijas** \> **Sadale**, lai atvērtu veidlapu **Sadale**.

4.  Laukā **Atdalīt daudzumu** ierakstiet kopējo saņemto krājumu daudzumu un pēc tam noklikšķiniet uz **Labi**.

5.  Veidlapā **Žurnāla rindas, novietojumi** atlasiet saņemto krājumu daudzuma rindu un pēc tam noklikšķiniet uz **Grāmatot**. Jūs varat grāmatot papildu daudzuma rindu pēc tam, kad krājumi tiek saņemti.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]