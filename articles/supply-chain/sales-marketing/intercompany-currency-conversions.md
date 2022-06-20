---
title: Starpuzņēmuma valūtas konvertēšana
description: Šajā rakstā ir paskaidrotas valūtas konvertēšanas starpuzņēmumu darījumiem
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851483"
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
