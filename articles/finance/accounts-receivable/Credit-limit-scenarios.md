---
title: Kredīta limita scenāriji
description: Šajā rakstā ir aprakstīts, kā tiek pārbaudīts debitora kredīta limits, kad debitors pieder debitora kredīta limitu grupai.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130274"
---
# <a name="credit-limit-scenarios"></a>Kredīta limita scenāriji

Kredīta pārvaldībā kredīta limitu var piešķirt debitoriem debitora līmenī. Katru debitoru var piešķirt debitora kredīta *limitu grupai*, un katrai grupai ir kredīta limits. Tāpēc kredīta limitu grupas līmenī var piešķirt arī debitoriem. Visiem debitoriem, kas piešķirti tai pašai debitoru kredīta grupai, ir viens kredīta limits.

Grupas kredīta limiti parasti tiek pārbaudīti pirms atsevišķiem kredīta limitiem. Individuālais kredīta limits vienmēr neignorē grupas kredīta limitu.

Šajā rakstā ir aprakstīti pieci scenāriji, kas ir saistīti ar debitoru kredīta grupām un atsevišķiem kredīta limitiem.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Debitoru grupas kredīta limits ir lielāks nekā individuālais kredīta limits

Piemēram, debitoram ir atsevišķs bankas kredīta $10,000. Debitors tiek piešķirts debitora kredīta grupai, un grupas kredīta limits $15,000. Šajā gadījumā debitora "efektīvais kredīta limits" ir $10,000, jo šī summa ir mazāka nekā grupas ierobežojums. Bloķēšanas kārtulas vispirms pārbauda grupas ierobežojumu. Tad viņi pārbauda atsevišķu limitu. Jebkurš pārdošanas pasūtījums, $10,000 tiks bloķēts.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Atsevišķais kredīta limits ir lielāks nekā debitoru grupas kredīta limits

Piemēram, debitoram ir atsevišķs bankas kredīta $20,000. Debitors tiek piešķirts debitora kredīta grupai, un grupas kredīta limits $15,000. Šajā gadījumā debitora efektīvais kredīta limits ir $15,000, jo bloķēšanas noteikumi vienmēr vispirms pārbauda grupas limitu. Visi pārdošanas pasūtījumi, $15,000 tiks bloķēti.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Individuālais kredīta limits ir iestatīts uz 0,00, bet obligātais kredīta limits ir iestatīts uz Jā.

**Ja debitoram ir iestatīts atsevišķs kredīta limits 0,00** **·** **un** obligātā kredīta limita opcija ir iestatīta uz Jā, debitora efektīvais kredīta limits $0.00 pat tad, ja debitors ir piešķirts debitoru kredīta grupai. Šādā veidā klients var būt daļa no grupas, bet visi pasūtījumi tiks atvērti uz Kredīta pārvaldību.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Atsevišķais kredīta limits ir iestatīts uz 0,00, bet neierobežots kredīta limits ir iestatīts uz Jā.

Ja debitoram **ir iestatīts atsevišķs kredīta limits 0,00**, **·** **bet** opcija Neierobežots kredīta limits ir iestatīta uz Jā, debitoram ir neierobežots kredīts pat tad, ja tie ir piešķirti debitoru kredīta grupai.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Individuālais kredīta limits ir iestatīts uz 0,00, un debitors ir daļa no debitoru kredīta grupas

Piemēram, debitoram **ir atsevišķs kredīta limits, kas iestatīts kā 0,00**, **·** **opcija Neierobežots kredīts ir iestatīta uz Nē**,**un** opcija Obligātais kredīta limits ir iestatīta uz **Nē.** Debitors tiek piešķirts debitora kredīta grupai, un grupas kredīta limits $15,000. Šajā gadījumā debitora efektīvais kredīta limits ir grupas ierobežojums, un $15,000. Tāpēc visi pārdošanas pasūtījumi, kas pārsniedz šo summu, tiks bloķēti. Šī darbība iespējo kredīta limita pārvaldību debitora kredīta grupas līmenī, nevis atsevišķā debitora līmenī. Visiem debitoriem, kas piešķirti tai pašai grupai, ir viens kredīta limits.
