---
title: Darbs ar konfigurācijām
description: Šajā rakstā ir sniegts galvenā scenārija apskats darbam ar elektronisko pārskatu (ER) konfigurācijām no globalizācijas līdzekļu darbvietas.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: d87559405d2490c314eb2c8b88268af0dc0dfaca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283061"
---
# <a name="work-with-configurations"></a>Darbs ar konfigurācijām

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu (ER) konfigurācijas ir viena no galvenajām elektronisko rēķinu izrakstīšanas funkciju sastāvdaļu kopām. ER konfigurācija satur faila struktūras iestatījumu un pārvēršanas noteikumu kopu datu pārvēršanai divos veidos:

- **Eksportēt ER formāta konfigurāciju** – šī konfigurācija pārveido datus no vienotās iekšējās struktūras (ER modeļa) uz elektroniskā faila formātu.
- **Importēt ER formāta konfigurāciju** – šī konfigurācija pārveido datus no elektroniskā faila formāta uz unificēto iekšējo struktūru (ER modelis).

Papildus izejošo elektronisko failu ģenerēšanai iepriekš definētajā formātā ER konfigurācijas ir plaši izmantotas, lai parsētu ienākošos ziņojumus no ārējiem Web pakalpojumiem kā atbildes. Šī funkcionalitāte palīdz veidot konfigurējamu loģiku, lai iegūtu saziņas rezultātus ar ārējiem kanāliem, pārvērstu šos rezultātus (kodus, ziņojumus un žurnālus) uz lietotāja lasāmo struktūru un pēc tam nodotu šo informāciju klienta programmai.

Lai sāktu izmantot ER konfigurācijas elektroniskajā rēķinu izrakstīšanas funkcionalitātē, **tās ir jāsaista ar funkciju un jāpadar tās pieejamas pašreizējās funkcionalitātes** versijas cilnē Konfigurācijas. Varat strādāt ar saistīto ER konfigurāciju, atlasot **Pievienot**, **Dzēst**, **Rediģēt** vai **Skatīt**.

Pirms varat pievienot saiti ER konfigurācijai, konfigurācijai ir jāpastāv jūsu regulēšanas konfigurācijas pakalpojuma (RCS) repozitorijā. Lai pārskatītu ER konfigurācijas, kas ir pieejamas jūsu RCS repozitorijā, sekojiet šiem soļiem.

1. Piesakieties savā RCS kontā.
2. Darbvietas **Elektroniskie pārskati** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.

Informāciju par to, kā izveidot jaunu ER konfigurāciju vai importēt esošu ER konfigurāciju no globālā repozitorija, skatiet elektroniskos [pārskatus](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Lai pielāgotu saistīto ER konfigurāciju, pašreizējā **elektronisko** rēķinu izrakstīšanas **līdzekļa** cilnē Konfigurācijas atlasiet Rediģēt. Sistēma automātiski izveido ER konfigurācijas versiju. Ja aktīvo konfigurācijas nodrošinātāju pašreizējo versiju nav izveidojis, sistēma izveido atvasinātu versiju, kas izmanto konfigurācijas nodrošinātāju. Ja pašreizējo versiju ir izveidojis aktīvais konfigurācijas nodrošinātājs, sistēma izveido jaunu versiju. Abos gadījumos var modificēt izveidoto versiju un pēc tam automātiski veikt visus nepieciešamos atjauninājumus.
