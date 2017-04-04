---
title: "Konfigurācijas noteikumi"
description: "Šajā rakstā ir sniegta vispārīga informācija par konfigurācijas kārtulām. Konfigurācijas kārtulas nosaka attiecības starp krājumiem materiālu komplektos (MK), kas attiecas uz precēm, kurām tiek izmantota konfigurācijas atbilstoši dimensijām tehnoloģija."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 271a780eec291455b433c0767246d79cb965ce02
ms.lasthandoff: 03/31/2017


---

# <a name="configuration-rules"></a>Konfigurācijas noteikumi

Šajā rakstā ir sniegta vispārīga informācija par konfigurācijas kārtulām. Konfigurācijas kārtulas nosaka attiecības starp krājumiem materiālu komplektos (MK), kas attiecas uz precēm, kurām tiek izmantota konfigurācijas atbilstoši dimensijām tehnoloģija.

Konfigurācijas noteikumi ir pieejami, kad definējat dimensijām atbilstošas konfigurācijas modeļus. Konfigurācijas noteikumi tiek izmantoti, lai ieviestu vai aizliegto noteiktas krājumu kombinācijas materiālu komplektā (MK). Pēc tam, kad ir izveidots MK un atbilstošie krājumi ir piešķirti attiecīgajām konfigurācijas grupām, var definēt vienu vai vairākus konfigurācijas noteikumus. Ja divi krājumi ir jālieto kopā, tiek izmantots operators **Atlasīt**, lai nodrošinātu ietveršanu. Ja divi krājumi viens otru izslēdz, tiek izmantots operators **Atcelt atlasi**, lai nodrošinātu izslēgšanu.  

**Piezīme.** Šī informācija attiecas tikai uz preču šabloniem, kas izmanto dimensijām atbilstošas konfigurācijas tehnoloģiju.  

Izmaiņas konfigurācijas noteikumos neietekmē esošās konfigurācijas. Taču ir svarīgi iestatīt noteikumus pirms jaunas konfigurācijas definēšanas un pārbaudīt noteikumus, ja uzskatāt, ka tie ir mainīti.  

**Piezīme.** ja tiek izmantota metode **Atlasīt**, tiek automātiski atlasīta atvasinātā konfigurācijas grupa, krājuma kods un konfigurācija. Ja tiek izmantota metode **Atcelt atlasi**, nevar atlasīt atvasināto konfigurāciju, krājuma kodu un konfigurāciju.

<a name="see-also"></a>Skatiet arī
--------

[Preces konfigurācija atbilstoši dimensijām](dimension-based-product-configuration.md)


