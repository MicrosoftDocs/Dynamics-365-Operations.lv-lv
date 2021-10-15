---
title: Izmaksu aprēķina līmenis
description: Šajā tēmā aprakstīts materiālu komplekta (MK) līmenis, kura nosaukums ir Izmaksu aprēķina līmenis. Šis MK līmenis tā aprēķinos neietver ražošanas un partijas pasūtījumus.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e08d11c8e9d98e56c5ef076cbab7bb68bedea62a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7581036"
---
# <a name="cost-calculation-level"></a>Izmaksu aprēķina līmenis

[!include [banner](../includes/banner.md)]

Materiālu komplekta (MK) līmenis ar nosaukumu **Izmaksu aprēķina līmenis** tā aprēķinos neietver ražošanas pasūtījumus un partijas pasūtījumus. Sistēma izmanto šo līmeni, kad tā veic izmaksu aprēķinus izmaksu aprēķināšanas versijās. Tādos procesos kā pārrēķins un krājumu slēgšana, sistēma to vietā izmanto **Izmaksu līmeņa** MK līmeni.

Tālāk minētajā vienkāršajā scenārijā ir parādītas atšķirības starp **Izmaksu aprēķina līmeņa** MK līmeni un **Izmaksu aprēķināšanas līmeņa** MK līmeni.

Jums ir trīs preces: A, B un C. Prece C ir preces B komponents, un prece B ir preces A komponents.

- **Izmaksu aprēķināšanas līmenis** piešķir šādus MK līmeņus:

    - **Prece A:** 0
    - **Prece B:** 1
    - **Prece C:** 2

- **Izmaksu aprēķina** piešķir šādus MK līmeņus:

    - **Prece A:** 0
    - **Prece B:** 1
    - **Prece C:** 2

Pēc tam tiek izveidots ražošanas pasūtījuma precei C, un prece A tiek pievienota ražošanas pasūtījuma MK. Pēc tam, kad pasūtījums tiek aplēsts, MK līmeņi tiek atjaunināti šādi:

- **Izmaksu aprēķināšanas līmenis** piešķir šādus MK līmeņus:

    - **Prece B:** 1
    - **Prece C:** 2
    - **Prece A:** 3

- **Izmaksu aprēķina** piešķir šādus MK līmeņus:

    - **Prece A:** 0
    - **Prece B:** 1
    - **Prece C:** 2

Šī uzvedība nodrošina, ka ražošanas pasūtījuma MK izmaiņas neietekmē turpmākos izmaksu aprēķinus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]