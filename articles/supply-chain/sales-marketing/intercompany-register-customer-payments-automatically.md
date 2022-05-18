---
title: Starpuzņēmumu debitoru rēķinu maksājumu automātiska reģistrēšana
description: Šajā rakstā skaidrota starpuzņēmumu debitoru rēķinu maksājumu automātiska reģistrēšana
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
ms.openlocfilehash: dbd06b21d736d1e247cd087e5bb86fbe641352e6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669437"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Starpuzņēmumu debitoru rēķinu maksājumu automātiska reģistrēšana

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management izveido debitora darbību, grāmatojot starpuzņēmuma pārdošanas pasūtījuma rēķinu. Šī debitora darbība paliek atvērta līdz tās segšanai, kas nozīmē, ka tā ir apmaksāta. Ja atbilstīgais starpuzņēmumu pirkšanas pasūtījums ir atjaunināts rēķinā, tiek izveidota kreditora darbība, kas atbilst debitora darbībai. Šī kreditora darbība arī paliek atvērta līdz tās segšanai (apmaksāšanai). Lai samazinātu neatbilstību risku, debitoru maksājumu žurnālu var izveidot un grāmatot automātiski, grāmatojot kreditoru maksājumu žurnālu.

1. Dodieties uz **Pārdošana un mārketings \> Debitori \> Visi debitori**.
1. Darbību rūts cilnē **Vispārīgi** atlasiet **Starpuzņēmums**.
1. Lai iestatītu starpuzņēmumu debitoru maksājumus **Starpuzņēmumu** lapā pārdošanas pasūtījumiem, atlasiet **Pārdošanas pasūtījuma politikas** saiti.
1. Laukā **Maksājumu žurnāls** atlasiet debitoru maksājumu žurnālu, kurā jāreģistrē starpuzņēmumu kreditoru maksājumi. Darba grupu varat atlasīt lapā **Debitoru moduļa parametri**.
1. Ja vēlaties šajā žurnālā grāmatot automātiski, atzīmējiet izvēles rūtiņu **Grāmatot žurnālā automātiski**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
