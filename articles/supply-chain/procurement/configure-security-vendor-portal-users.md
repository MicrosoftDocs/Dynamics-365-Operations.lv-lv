---
title: Kreditoru portāla lietotāja drošība
description: Šajā rakstā ir paskaidrots, kā veikt drošības iestatīšanu ārējiem kreditoriem, kuri lieto kreditoru portālu. Šī informācija attiecas tikai uz 2016. februāra un 2016. gada &amp; maija Dynamics AXversijām.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72f353448f3b5d1f816bb240a230e26529c9cec3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433063"
---
# <a name="vendor-portal-user-security"></a>Kreditoru portāla lietotāju drošība

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā veikt drošības iestatīšanu ārējiem kreditoriem, kuri lieto kreditoru portālu. Šī informācija attiecas tikai uz 2016. februāra un 2016. gada &amp; maija Dynamics AXversijām.

Dynamics 365 for Operations versijā 1611 kreditoru portāla funkcionalitāte ir aizstāta ar paplašināto kreditoru sadarbības funkcionalitāti. Papildinformāciju par drošības iestatīšanu kreditoru sadarbībai skatiet rakstā [Iestatīt un uzturēt kreditoru sadarbību](set-up-maintain-vendor-collaboration.md). Kreditoru portālā ārējiem kreditoriem ir pieejama ierobežota informācija par pirkšanas pasūtījumiem (PP). Ir svarīgi programmā Microsoft Dynamics AX pareizi iestatīt lietotāja atļaujas kreditoru portālā, lai kreditoriem netīšām nepiešķirtu tiesības piekļūt papildinformācijai jūsu Dynamics AX vidē. **Svarīgi:** atšķirībā no citiem lietotājiem, ārējiem kreditoriem nedrīkst būt loma **SystemUser**. Loma **SystemUser** piešķir piekļuvi privilēģiju kopai, kas nav piemērota ārējiem lietotājiem.

## <a name="setting-up-a-vendor-portal-user"></a>Kreditoru portāla lietotāja iestatīšana
Pirms kādam kreditoru portāla lietotājam izveidot lietotāja kontu, jāiestata kreditors, lai atļautu kreditoru portāla sadarbību. Izmantojiet lauku **Pirkšanas pasūtījuma sadarbība** cilnē **Vispārējā** lapā **Kreditori**. Ārējiem kreditoriem, kuri lieto kreditoru portālu, jābūt šādiem iestatījumiem:

-   Kreditoram programmas Dynamics AXlapā **Lietotāji** ir jābūt reģistrētam Microsoft Azure Active Directory (AAD) lietotāja kontam.
-   Kreditoram ir jābūt drošības lomai **Kreditors (ārējs)**, nevis lomai **SystemUser**. **Piezīme.** Kad izveidojat jaunu lietotāja kontu programmā Dynamics AX, tiek automātiski piešķirta loma **SystemUser**. Tāpēc šī loma ir jānoņem un jāapstiprina saņemtais brīdinājuma ziņojums.
-   Kreditora lietotājam nevajadzētu piešķirt atļauju pievienot papildu laukus no PP tabulām PP skatā. Cilnē **Personalizēšana**, cilnē **Lietotāji** iestatiet lietotājam opciju **Atļaut skaidri izteiktu personalizēšanu** uz **Nē**.
-   Lietotāja kontam ir jābūt saistītam ar reģistrētu kontaktpersonu. Lapā **Lietotāji** izvēlieties kontaktpersonu laukā **Nosaukums**. Personai, kuru atlasījāt, jābūt lomai **Kontaktpersona** attiecīgajam kreditoram.

Ja viena un tā pati persona pieprasa piekļuvi vairākiem kreditoru kontiem kreditoru portālā (iespējams, dažādām juridiskajām personām), katram šīs personas lietotāja kontam ir jābūt saistītām ar to pašu reģistrēto kontaktpersonu. Loma **Kreditors (ārējs)** ietver pamata iespējas, kas ir nepieciešamas, lai varētu izmantot funkcionalitāti, kas ir pieejamas kreditoru portālā. Šis iestatījums palīdz garantēt, ka lietotāja interfeiss, ko ārējais lietotājs redz, ir vērsts tikai uz paredzēto scenāriju.

<a name="additional-resources"></a>Papildu resursi
--------

[Sadarbība ar kreditoriem, izmantojot kreditoru portālu](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]