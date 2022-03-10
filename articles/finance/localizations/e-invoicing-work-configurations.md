---
title: Darbs ar konfigurācijām
description: Šajā tēmā ir sniegts pārskats par galveno scenāriju darbam ar elektronisko pārskatu (ER) konfigurācijām no globalizācijas līdzekļu darbvietas.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4318399ee58ed54b29f8d360345b8930238ea9f2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371965"
---
# <a name="work-with-configurations"></a>Darbs ar konfigurācijām

[!include [banner](../includes/banner.md)]

Elektroniskās ziņošanas (ER) konfigurācijas ir viena no galvenajām elektronisko rēķinu sagatavošanas funkciju sastāvdaļām. ER konfigurācija ietver faila struktūras iestatījumus un transformācijas kārtulu kopu datu pārveidošanai divos veidos:

- **Eksportēt ER formāta konfigurāciju** – šī konfigurācija pārveido datus no vienotās iekšējās struktūras (ER modeļa) uz elektroniskā faila formātu.
- **Importēt ER formāta konfigurāciju** – šī konfigurācija pārveido datus no elektroniskā faila formāta uz vienoto iekšējo struktūru (ER modeli).

Papildus izejošo elektronisko failu ģenerēšanai iepriekš definētā formātā ER konfigurācijas tiek plaši izmantotas, lai parsētu ienākošos ziņojumus no ārējiem tīmekļa pakalpojumiem kā atbildes. Šī funkcionalitāte palīdz veidot konfigurējamu loģiku, lai iegūtu rezultātus saziņai ar ārējiem kanāliem, pārvērstu šos rezultātus (kodus, ziņojumus un žurnālus) uz lietotāja lasāmu struktūru un pēc tam nodotu šo informāciju klienta lietojumprogrammai.

Lai elektronisko rēķinu izrakstīšanas funkcijā sāktu izmantot ER konfigurācijas, tās ir jāsaista ar līdzekli un jāpadara pieejamas **pašreizējās līdzekļa versijas cilnē Konfigurācijas**. Varat strādāt ar saistītu ER konfigurāciju, atlasot **Pievienot**, **Dzēst**, **Rediģēt** vai **Skatīt**.

Lai varētu pievienot saiti uz ER konfigurāciju, konfigurācijai ir jābūt jūsu regulatīvās konfigurācijas pakalpojuma (RCS) repozitorijā. Lai pārskatītu ER konfigurācijas, kas ir pieejamas jūsu RCS repozitorijā, rīkojieties šādi.

1. Piesakieties savā RCS kontā.
2. Darbvietas **Elektroniskie pārskati** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.

Informāciju par to, kā izveidot jaunu ER konfigurāciju vai importēt esošu ER konfigurāciju no globālā repozitorija, skatiet rakstā [Elektroniskā ziņošana](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Lai pielāgotu saistīto ER konfigurāciju, pašreizējā elektronisko rēķinu izrakstīšanas līdzekļa cilnē Konfigurācijas atlasiet **Rediģēt** **.** Sistēma automātiski izveido ER konfigurācijas versiju. Ja aktīvo konfigurācijas nodrošinātājs nav izveidojis pašreizējo versiju, sistēma izveido atvasinātu versiju, kas izmanto konfigurācijas nodrošinātāju. Ja pašreizējo versiju izveidoja aktīvais konfigurācijas nodrošinātājs, sistēma izveido jaunu versiju. Abos gadījumos varat modificēt izveidoto versiju un pēc tam automātiski veikt visus nepieciešamos atjauninājumus.
