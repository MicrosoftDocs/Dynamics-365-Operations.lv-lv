---
title: Konfigurācijas noteikumi
description: Šajā rakstā ir sniegta vispārīga informācija par konfigurācijas kārtulām. Konfigurācijas kārtulas nosaka attiecības starp krājumiem materiālu komplektos (MK), kas attiecas uz precēm, kurām tiek izmantota konfigurācijas atbilstoši dimensijām tehnoloģija.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac3515837df45b65121ebec72a32ac98d740796a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221875"
---
# <a name="configuration-rules"></a>Konfigurācijas noteikumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta vispārīga informācija par konfigurācijas kārtulām. Konfigurācijas kārtulas nosaka attiecības starp krājumiem materiālu komplektos (MK), kas attiecas uz precēm, kurām tiek izmantota konfigurācijas atbilstoši dimensijām tehnoloģija.

Konfigurācijas noteikumi ir pieejami, kad definējat dimensijām atbilstošas konfigurācijas modeļus. Konfigurācijas noteikumi tiek izmantoti, lai ieviestu vai aizliegto noteiktas krājumu kombinācijas materiālu komplektā (MK). Pēc tam, kad ir izveidots MK un atbilstošie krājumi ir piešķirti attiecīgajām konfigurācijas grupām, var definēt vienu vai vairākus konfigurācijas noteikumus. Ja divi krājumi ir jālieto kopā, tiek izmantots operators **Atlasīt**, lai nodrošinātu ietveršanu. Ja divi krājumi viens otru izslēdz, tiek izmantots operators **Atcelt atlasi**, lai nodrošinātu izslēgšanu.  

**Piezīme.** Šī informācija attiecas tikai uz preču šabloniem, kas izmanto dimensijām atbilstošas konfigurācijas tehnoloģiju.  

Izmaiņas konfigurācijas noteikumos neietekmē esošās konfigurācijas. Taču ir svarīgi iestatīt noteikumus pirms jaunas konfigurācijas definēšanas un pārbaudīt noteikumus, ja uzskatāt, ka tie ir mainīti.  

**Piezīme.** ja tiek izmantota metode **Atlasīt**, tiek automātiski atlasīta atvasinātā konfigurācijas grupa, krājuma kods un konfigurācija. Ja tiek izmantota metode **Atcelt atlasi**, nevar atlasīt atvasināto konfigurāciju, krājuma kodu un konfigurāciju.

<a name="additional-resources"></a>Papildu resursi
--------

[Uz dimensijām balstītas preču konfigurācijas pārskats](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]