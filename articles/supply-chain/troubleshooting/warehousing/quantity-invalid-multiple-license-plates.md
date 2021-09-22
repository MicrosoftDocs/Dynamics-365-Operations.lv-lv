---
title: Daudzums nav derīgs izpildes darbam ar vairākām noliktavas vienībām
description: Kad vienā atrašanās vietā ir izdošanas darbs ar vairākām numuru zīmēm, daudzums nav derīgs vienības ea. Pārbaudiet, vai tālāk minētie lauki ir pareizi.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476943"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Daudzums nav derīgs, ja vienā atrašanās vietā ir izdošanas darbs ar vairākām noliktavas vienībām

## <a name="symptoms"></a>Simptomi

Kad vienā atrašanās vietā ir izdošanas darbs ar vairākām numuru zīmēm, daudzums nav derīgs vienības *ea* un jūs saņemsit šādu kļūdas ziņojumu:

> Daudzums nav derīgs vienībai 1%.

## <a name="resolution"></a>Novēršana

Pārbaudiet, vai lauki **Vienības secības grupas ID** un **Vienības konvertēšana** izlaistajā precē vai preces variantā tiek iestatīti pareizi.

Ņemiet vērā, ka kļūdas ziņojums ir uzlabots 10.0.15. versijā, lai parādītu paredzamo daudzumu (sk. [KV 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Jaunais kļūdas ziņojums:

> Daudzuma vērtība nav derīga. Paredzamais %1 %2.
