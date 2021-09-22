---
title: Pārdošanas pasūtījumu nevarēja izlaist, izmantojot nosūtīšanas noliktavas operācijas
description: Ir vairāki iemesli, kādēļ var tikt parādīts kļūdas ziņojums, ka pārdošanas pasūtījumu nevar izdot. Šajā lapā skaidrots, kāpēc un kā samazināt šo problēmu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476999"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Pārdošanas pasūtījumu nevarēja izlaist, izmantojot nosūtīšanas noliktavas operācijas

## <a name="symptoms"></a>Simptomi

Strādājot ar nosūtīšanas noliktavas operācijām, varat saņemt šādu kļūdas ziņojumu:

> Pārdošanas pasūtījumu nevarēja izlaist.

## <a name="cause"></a>Iemesls

Šī problēma var rasties vairāku iemeslu dēļ. Piemēram, pasūtījums ir kredīta pārvaldības aizturēšana, un nevienu sūtījumu nevar izveidot, kamēr nav ievadīta derīga pasta adrese visām pārdošanas rindām, kas ir saistītas ar pasūtījumu. Pretējā gadījumā ir paredzēta pasūtījuma aizturēšana, kas jāadresē, lai pasūtījumu varētu nodot izpildei noliktavā. Šis aizturējums var būt specifisks pasūtījumam, vai tas var būt klienta kontā.

## <a name="resolution"></a>Novēršana

Pievienojiet vai atjauniniet adresi pārdošanas pasūtījumā un pasūtījuma rindās un pēc tam izlaidiet pasūtījumu uz noliktavu. Pasūtījumus var izlaist noliktavā tikai tad, ja tiem ir derīga piegādes adrese (katram adreses formāta iestatījumam **Organizācijas administrēšanas** modulī).

Izmeklējiet pasūtījuma aizturēšanu un risināt šos jautājumus. Pēc tam noņemiet aizturēšanu no pasūtījuma vai klienta un izlaidiet pasūtījumu uz noliktavu.
