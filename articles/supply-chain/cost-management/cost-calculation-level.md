---
title: Izmaksu aprēķina līmenis
description: Šajā tēmā aprakstīts materiālu komplekta (MK) līmenis, kura nosaukums ir Izmaksu aprēķina līmenis. Šis MK līmenis tā aprēķinos neietver ražošanas un partijas pasūtījumus.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967736"
---
# <a name="cost-calculation-level"></a>Izmaksu aprēķina līmenis

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
