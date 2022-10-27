---
title: Brīva teksta rēķina labošana
description: Šajā rakstā ir paskaidrots, kā labot brīva teksta rēķinu, kas jau ir iegrāmatots, un kā to vēlreiz izsniegt kā labotu rēķinu.
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c83ac47bc5e7f7ed223c772591cf8a7c1e63a40
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715502"
---
# <a name="correct-a-free-text-invoice"></a>Brīva teksta rēķina labošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā labot brīva teksta rēķinu, kas jau ir iegrāmatots, un kā to vēlreiz izsniegt kā labotu rēķinu.

Lai labotu brīva teksta rēķinu, kas jau ir grāmatots, atveriet iegrāmatoto brīva teksta rēķinu. Lapā **Rēķins** atlasiet vienumu **Atcelt** un pēc tam — **Labot rēķinu**. Atlasiet iemesla kodu, pievienojiet komentārus un atlasiet datumu jaunajam labotajam rēķinam. Varat modificēt laboto rēķinu un to grāmatot. 

Kad grāmatojat laboto rēķinu, tiek izveidots atcelšanas rēķins par kredīta summu, kas ir vienāda ar sākotnējā rēķina summu. Līdz ar to sākotnējā rēķina un atcelšanas rēķina apvienotā bilance ir 0 (nulle). Atcelšanas rēķins tiek segts pret sākotnējo rēķinu. 

Pēc labotā rēķina grāmatošanas jums ir trīs rēķini:

-   **Sākotnējais rēķins** — rēķins, kas ietver informāciju, kuru jūs labojat.
-   **Atcelšanas rēķins** — sistēmas ģenerēts kredītrēķins, kas tika izveidots, lai atceltu pēdējo laboto rēķinu.
-   **Labotais rēķins** — rēķins, kas ietver labotā rēķina informāciju.

Atcelšanas un labošanas rēķinus varat identificēti divējādi:

-   Lapā **Visi brīva teksta rēķini** ietver kolonnu **Labojums**, kur varat redzēt, kuri rēķini ir atcelšanas rēķini un labotie rēķini.
-   Brīva teksta rēķina virsrakstā ir redzams statuss **Atcelšanas rēķins '\[rēķina numurs\]'** vai **Labotais rēķins '\[rēķina numurs\]'**.

> [!NOTE]
> Šis līdzeklis ir pieejams tikai tad, ja ir atlasīta konfigurācijas atslēga **Brīva teksta rēķina labojums**. Papildinformāciju par konfigurācijas atslēgu iespējošanu skatiet sadaļas Iespējot (vai deaktivizēt) konfigurācijas atslēgas rakstā [Uzturēšanas](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) režīms. 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
