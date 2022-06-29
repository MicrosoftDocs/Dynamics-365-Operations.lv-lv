---
title: Budžeta noteikta pirkšanas pasūtījuma izveide
description: Izmantojiet šo procedūru, lai izveidotu pirkšanas pasūtījumu, kurā ir pārbaudīts pieejamais budžets.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016193"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Budžeta noteikta pirkšanas pasūtījuma izveide

[!include [banner](../../includes/banner.md)]

Izmantojiet šo procedūru, lai izveidotu pirkšanas pasūtījumu, kurā ir pārbaudīts pieejamais budžets.

## <a name="review-the-budget-control-configuration"></a>Budžeta kontroles konfigurācijas pārskatīšana

1. Pārejiet **uz budžeta > budžeta > kontroles > kontroles konfigurāciju**.
1. Atlasiet cilni **Pieejamie budžeta** līdzekļi.
1. Atlasiet cilni **Dokumenti un** žurnāli.
1. Atlasiet cilni **Definēt budžeta kontroles** nosacījumus.
1. Atlasiet cilni **Definēt budžeta** grupas.
1. Aizvērt lapu.

## <a name="create-a-purchase-order"></a>Pirkuma pasūtījuma izveide

1. Dodieties uz **Sagādes un avotu > pirkšanas pasūtījumi > visiem pirkšanas pasūtījumiem**.
1. Atlasiet **Jauna**.
1. Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.
1. Izvērsiet kopsavilkuma cilni **Vispārīgi**.
1. Laukā **Uzskaites** datums iestatiet datumu.
1. Atlasiet **Labi,** lai aizvērtu dialogu un atvērtu jauno pirkšanas pasūtījumu.
1. Kopsavilkuma cilnē **Pirkšanas** pasūtījuma rindas no rīkjoslas atlasiet Pievienot rindu, lai pievienotu jaunu rindu, un pēc tam, kad nepieciešams, aizpildiet rindu, **lai** pievienotu pasūtījumam krājumu.
1. Kopsavilkuma cilnes **Pirkšanas pasūtījuma** rindas rīkjoslā atlasiet Finanšu **sadales \> summas**.
1. Laukā **Virsgrāmatas** konts norādiet kontu.
1. Aizvērt lapu.

## <a name="perform-budget-checking"></a>Veikt budžeta pārbaudi

1. Turpiniet darbu ar pirkšanas pasūtījumu, tam tikko pievienojat rindu.
1. Kopsavilkuma cilnes **Pirkšanas pasūtījuma** rindas rīkjoslā atlasiet Finanšu **darbību \> budžeta pārbaude**.
1. Kopsavilkuma cilnes **Pirkšanas pasūtījuma** rindas rīkjoslā atlasiet Finanšu **budžeta \> pārbaudes kļūdas vai brīdinājumus**.
1. Tiek **atvērts budžeta pārbaudes kļūdu vai brīdinājumu** dialoglodziņš. Pārbaudiet pārbaudes rezultātus un pēc tam atlasiet Aizvērt, **lai** aizvērtu dialogu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]