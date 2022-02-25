---
title: Abonementa rēķinu apskats
description: Šajā tēmā aprakstīti Abonementa norēķini ar Microsoft Dynamics 365 Finance.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b94ac36e49d55ad42909877d77903cd40cb22cbe
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182713"
---
# <a name="subscription-billing-overview"></a>Abonementa rēķinu apskats

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Abonementa norēķini ļauj organizācijām pārvaldīt abonementa ieņēmumu iespējas un periodiskus norēķinus, izmantojot rēķinu grafikus. Kompleksas cenu noteikšanas un norēķinu modeļi un ieņēmumu sadalījums ir viegli pārvaldāms un tiek izrakstīts rēķins un atpazīts rindu līmenī. Vairāku elementu ieņēmumu sadalījums ļauj ieņēmumu sadali veikt saskaņā ar starptautiskajiem grāmatvedības standartiem (Starptautiskais finanšu pārskatu standarts 15 \[IFRS 15\]) un vispārpieņemtiem grāmatvedības principiem (US GAAP) standartiem (Grāmatvedības standartu 606 \[. tēma ASC 606\]).

Risinājumam ir trīs moduļi, ko var izmantot neatkarīgi. Alternatīvi visus trīs moduļus var izmantot kopā.

- **Periodiskie līguma norēķini** - šis modulis iespējo periodiskus norēķinus un cenu pārvaldību, lai nodrošinātu kontroli pār cenu noteikšanas un norēķinu parametriem, līgumu atjaunošanu un konsolidēto rēķinu izrakstīšanu.
- **Ieņēmumu un izdevumu atliktie ieņēmumi – šis modulis likvidē manuālos procesus un atkarību no ārējām sistēmām, pārvaldot ieņēmumus** un aktivizējot reāllaika ieskatu ikmēneša periodiskos ieņēmumos.
- **Vairāku elementu ieņēmumu sadalījums** – šis modulis palīdz ar ieņēmumu atbilstību, apstrādājot cenu noteikšanu un ieņēmumu sadalījumu starp vairākiem krājumiem.

Abonementa rēķini ir iespējoti, **izmantojot funkciju pārvaldību**. Tomēr to nevar izmantot ar ieņēmumu **atzīšanas** līdzekli. Tāpēc pirms abonementa rēķinu iespējošanas šī funkcija ir jāatspējo.

1. Līdzekļu pārvaldības **darbvietā** cilnē Visi **ievadiet** **filtrā ieņēmumu atzīšanu** un pēc tam atlasiet līdzekļa nosaukumu kā filtru.
2. Atlasiet iespēju **Ieņēmumu atzīšana** un pēc tam atlasiet **Deaktivizēt**.
3. Līdzekļu **nosaukuma filtrā** ievadiet abonementa **rēķinus** un pēc tam atlasiet moduļa filtru.
4. Atlasiet līdzekli **Abonementa norēķini** un pēc tam atlasiet **Iespējot**.
5. Atlasiet vienu no trim moduļiem no iepriekšējā saraksta un pēc tam atlasiet **Iespējot**. Atkārtojiet šo soli katram no diviem pārējiem moduļiem.

    > [!IMPORTANT]
    > Lai **varētu aktivizēt jebkuru** no trim moduļiem, ir jābūt iespējotai abonementu rēķinu izrakstīšanas funkcijai.
