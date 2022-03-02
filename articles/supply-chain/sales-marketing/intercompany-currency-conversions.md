---
title: Starpuzņēmuma valūtas konvertēšana
description: Šajā tēmā skaidrota valūtu konvertācija starpuzņēmumu darījumiem
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548410"
---
# <a name="intercompany-currency-conversions"></a>Starpuzņēmuma valūtas konvertēšana

[!include [banner](../../includes/banner.md)]

Ja valūtas kods oriģinālajā pārdošanas pasūtījumā un starpuzņēmumu pirkšanas pasūtījumā atšķiras, tad, aktivizējot sinhronizāciju, valūtas konvertēšana notiek šādos laukos:

- **Vienības cena**
- **Pārdošanas izmaksas** vai **Pirkšanas papildmaksas**
- **Atlaide**
- **Daudzrindu atlaide**

Tad šie lauki tiek sinhronizēti uz starpuzņēmumu pārdošanas pasūtījuma rindu.

Tomēr tādēļ, ka valūta starpuzņēmumu pirkšanas pasūtījumā un starpuzņēmumu pārdošanas pasūtījumā tiek vienmēr sinhronizēta, tad sekojošie lauki tiek sinhronizēti bez valūtas konvertācijas:

- **Vienības cena**
- **Pārdošanas izmaksas** vai **Pirkšanas papildmaksas**
- **Atlaide**
- **Atlaides procents**
- **Daudzrindu atlaide**
- **Daudzrindu atlaide procentos**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]