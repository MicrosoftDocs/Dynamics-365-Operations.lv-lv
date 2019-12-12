---
title: Funkcionālie novietojumi un līdzekļi
description: Šajā tēmā aprakstīti funkcionālie novietojumi un līdzekļi Līdzekļu pārvaldībā. Līdzekļu pārvaldība ir uzlabots modulis līdzekļu un uzturēšanas darbu pārvaldībai programmā Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3a42d36fd137aa780886276a4235f1b8f3a3680
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653351"
---
# <a name="functional-locations-and-assets"></a>Funkcionālie novietojumi un līdzekļi

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā aprakstīti funkcionālie novietojumi un līdzekļi Līdzekļu pārvaldībā. Līdzekļu pārvaldība ir uzlabots modulis līdzekļu un uzturēšanas darbu pārvaldībai programmā Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Kopsavilkums

Līdzekļu pārvaldība ir cieši integrēta ar vairākiem moduļiem ar citām Finance and Operations programmām. Nākamajā attēlā ir parādīti interfeisi ar citiem moduļiem.

![Shēmā ir parādīts, kā Līdzekļu pārvaldība mijiedarbojas ar citiem moduļiem](media/01-overview-image.png)

Līdzekļu pārvaldība ļauj efektīvi pārvaldīt un izpildīt visus uzdevumus, kas saistīti ar dažāda veida iekārtu pārvaldīšanu un apkopi uzņēmumā. Šajā aprīkojumā ietilpst mašīnas, ražošanas iekārtas un transportlīdzekļi. Līdzekļu pārvaldība arī atbalsta risinājumus daudzās nozarēs.

Nākamajā attēlā ir parādīts pārskats par galveno funkcionalitāti, ko ietver Līdzekļu pārvaldība.

![Shēmā ir parādīta galvenā funkcionalitāte Līdzekļu pārvaldībā](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Funkcionālie novietojumi un līdzekļi

Funkcionālie novietojumi tiek izmantoti, lai pārvaldītu līdzekļus to atrašanās vietās. Šī pārvaldība ietver līdzekļu izmaksu izsekošanu funkcionālajos novietojumos. Funkcionālie novietojumi tiek strukturēti hierarhiski, un atrašanās vietām var būt apakšvietas. Funkcionālo novietojumu struktūra ir statiska. Citiem vārdiem sakot, atrašanās vietas nevar mainīt vietu. Līdzekļus var uzstādīt funkcionālajos novietojumos un pēc vajadzības vēlāk tos var uzstādīt citos funkcionālajos novietojumos.

Līdzekļa izmaksās vienmēr tiek ievērota līdzekļa atrašanās vieta. Citiem vārdiem sakot, ja uzstādāt līdzekli jaunā funkcionālajā novietojumā, līdzeklis automātiski izmanto finanšu dimensijas, kas ir saistītas ar jauno funkcionālo novietojumu. Tāpēc līdzekļa izmaksas vienmēr ir saistītas ar funkcionālo novietojumu, kurā līdzeklis attiecīgajā brīdī ir uzstādīts. Šī automātiskā finanšu dimensiju apstrāde palīdz garantēt izmaksu pilnīgu izsekošanu, ja jūsu uzņēmums veic projektu kontroli un ziņošanu par funkcionālajiem novietojumiem.

Tas, kā veidojat savu funkcionālo novietojumu hierarhiju, ir atkarīgs no uzņēmuma vajadzībām attiecībā uz iekšējo iekārtu vai klientu apkalpošanas aprīkojuma uzturēšanu. Nākamajā attēlā ir parādīts tādu funkcionālo novietojumu piemērs, kuru pamatā ir ģeogrāfiskās atrašanās vietas.

![Shēmā ir parādītie funkcionālie novietojumi, pamatojoties uz ģeogrāfiskajām atrašanās vietām](media/03-overview-image.png)

Nākamajā attēlā ir parādīts tādu funkcionālo novietojumu piemērs, kuru pamatā ir debitori.

![Shēmā ir parādītie funkcionālie novietojumi, pamatojoties uz klientiem](media/04-overview-image.png)