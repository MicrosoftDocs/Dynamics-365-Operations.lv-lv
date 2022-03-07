---
title: Parametru iestatīšana starpuzņēmumu pasūtījuma grāmatošanai
description: Šajā rakstā ir paskaidrots, kā iestatīt uzņēmumam raksturīgus parametrus programmā
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
ms.openlocfilehash: c728f2f491948ae1c8550396ba4d72f76f46fe85
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548399"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Parametru iestatīšana starpuzņēmumu pasūtījuma grāmatošanai

[!include [banner](../../includes/banner.md)]

Pēc starpuzņēmuma debitora rēķina grāmatošanas to var iestatīt automātiskai grāmatošanai gan starpuzņēmumu pirkšanas pasūtījumā, gan oriģinālajā debitora rēķinā.

> [!NOTE]
> Pirms šīs procedūras izpildāt, iestatiet drukas pārvaldību savā organizācijā, lai norādiet uz pareizo rēķina printeri. Tas nodrošina, ka oriģinālā pārdošanas pasūtījuma rēķins tiek drukāts uz pareizā printera.

Parametri, kuri jāiestata:

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**. Atlasiet pārdošanas pasūtījumu, ar kuru vēlaties strādāt.
1. Pārdošanas pasūtījuma darbību rūtī atlasiet **Galvenes skatu** un pēc tam atlasiet kopsavilkuma cilni **Starpuzņēmumu iestatījumi** un atveriet to.
1. Pēc tam darbību rūtī noklikšķiniet uz cilnes **Pārdošanas pasūtījums** un atlasiet **Rediģēt**.
1. Atgriezieties kopsavilkuma cilnē **Starpuzņēmumu iestatījumi** un atlasiet **Tiešā piegāde**, lai aktivizētu tiešo piegādi visā starpuzņēmumu ķēdē (visi pasūtījumi).
1. Atlasiet **Saglabāt**, lai saglabātu pārdošanas pasūtījumu ar jauno iestatījumu. Pēc tam atlasiet **Aizvērt**, lai slēgtu pārdošanas pasūtījumu.
1. Pārejiet uz sadaļu **Sagāde un avoti \> Kreditori \> Visi kreditori**. Cilnē **Vispārīgi** atlasiet **Starpuzņēmums**.
1. **Starpuzņēmumu** lapā atlasiet **Pirkšanas pasūtījumu politikas** saiti. Lauku grupā **Starpuzņēmumu pirkšanas pasūtījums (tiešā piegāde)** atlasiet **Grāmatot rēķinu automātiski** un noņemiet izvēles rūtiņu no lauka **Drukāt rēķinu automātiski**.
1. Lauku grupā **Starpuzņēmumu pirkšanas pasūtījums (tiešā piegāde)** atlasiet **Grāmatot rēķinu automātiski** un noņemiet izvēles rūtiņu no lauka **Drukāt rēķinu automātiski**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
