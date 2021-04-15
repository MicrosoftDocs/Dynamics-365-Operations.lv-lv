---
title: Kravas plānošanas rīks
description: Šajā tēmā ir aprakstīts, kā strādāt ar kravas plānošanas rīku.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8633adbab43c95366d42cf409f5e508771c906
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809042"
---
# <a name="load-building-workbench"></a>Kravas plānošanas rīks

Kravas plānošanas rīks ļauj izmantot kravas plānošanas stratēģijas, kad veidojat kravas.

## <a name="create-a-load-building-strategy"></a>Kravas plānošanas stratēģijas izveidošana

Varat izmantot kravas plānošanas stratēģijas, lai automātiski izveidotu kravas. Šī iespēja var būt noderīga šādās situācijās:

- Ja regulāri nosūtat noteiktu preču komplektu, kravas stratēģijas palīdz ietaupīt laiku, jo jums nav jāveido tāda pati krava katru reizi.
- Ja vēlaties izvairīties no daļēji pilnas kravas, lai palielinātu efektivitāti, kravas stratēģijas var palīdzēt piepildīt katru kravu, cik vien iespējams.

Kravas veidošanas stratēģijas klase, ko sauc `TMSLoadBuildingVolumeStrategy`, nodrošina kravas plānošanas stratēģiju, ko sauc *Lielapjoma kravas plānošanas stratēģija*. Šī stratēģija ļauj izmantot maksimālās vērtības, kuras ir norādītas garumam un svaram kravas veidnē, vai arī iestatījumus var ignorēt, ievadot jaunas vērtības. Šī stratēģija ir vienīgā stratēģija, kas tiek iekļauta ārpus lodziņa. (Tomēr, iespējams, ir dažas pielāgotas stratēģijas.)

Lai izmantotu *Uz apjomu balstītu kravas plānošanas stratēģiju*, atlasiet to laukā **Kravas plānošanas stratēģija** lapā **Kravas plānošanas rīks** (**Transportēšanas pārvaldības &gt; Plānošana &gt; Kravas plānošanas rīks**).

Lai izveidotu kravas plānošanas stratēģiju, veiciet šādas darbības.

1. Doties uz **Transportēšanas pārvaldība &gt; Uzstādīšana &gt; Kravas plānošana &gt; Kravas plānošanas stratēģija**.
1. Darbības rūtī atlasiet **Ģenerēt klašu sarakstu**, lai pārliecinātos, ka jums ir jaunākās visu pieejamo klašu versijas.
1. Darbību rūtī atlasiet **Jauns**.
1. Ievadiet unikālu stratēģijas nosaukumu, atlasiet tai kravas plānošanas stratēģijas klasi un ievadiet aprakstu.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Parametri**.
1. Lapā **Kravas plānošanas stratēģijas parametri** atlasiet **Kravas noslodze** sarakstā un pēc tam laukā **Vērtība** ievadiet procentuālo daļu no kravas kopējā tilpuma kravas, kas jāpiemēro jaunajai kravas plānošanas stratēģijai.
1. Atlasiet **Svara noslodze** sarakstā un pēc tam laukā **Vērtība** ievadiet procentuālo daļu no kravas kopējā svara noslodzes, kas jāpiemēro jaunajai kravas plānošanas stratēģijai.
1. Aizveriet lapu **Kravas plānošanas stratēģijas parametri**.
1. Aizveriet lapu **Kravas plānošanas stratēģijas**.

Tagad varat piešķirt kravas plānošanas stratēģiju kravas plānošanas veidnei. Vai arī to var izmantot tieši kravas plānošanas rīkā.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Izmantot kravas plānošanas stratēģiju kravas plānošanas rīkā

1. Dodieties uz **Transportēšanas pārvaldība &gt; Plānošana &gt; Kravas plānošanas rīks**.
1. Izpildiet kādu no norādītajām transakcijām.

    - Atlasiet stratēģiju laukā **Kravas plānošanas stratēģija**.
    - Ja esat noteicis kravas plānošanas veidni un piešķīris tai kravas plānošanas stratēģiju, darbības rūtī cilnē **Pārvaldīt veidnes** atlasiet **Lietot veidni**. Pēc tam nolaižamajā dialoglodziņā **Pielietot kravas plānošanas veidni** atlasiet veidni, kas atrodas laukā **Kravas plānošanas veidnes nosaukums**.

1. Kopsavilkuma cilnē **Kravas veidņu secība** atlasiet vienu vai vairākas [kravas veidnes](load-template.md). Šis rīks mēģinās ievietot kravu šajos konteineru tipos šeit noteiktajā secībā. Parasti mazākie konteineri ir jānovieto saraksta sākumā, lai nodrošinātu, ka vispirms tiek atlasīts vismazākais iespējamais konteiners.
1. Darbību rūtī atlasiet **Piedāvāt kravas**.
1. Pārskatiet piedāvātās kravas un piedāvātās kravas rindas.
1. Darbības rūtī atlasiet **Izveidot kravu**, lai izveidotu kravas, kas pamatotas uz pirmdokumenta rindām kopsavilkuma cilnē **Piedāvātās kravas rindas**.
1. Aizveriet lapu **Kravas plānošanas rīks**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]