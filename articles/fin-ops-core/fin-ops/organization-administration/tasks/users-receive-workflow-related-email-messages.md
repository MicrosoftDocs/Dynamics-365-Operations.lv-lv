---
title: Ļaut lietotājiem saņemt ar darbplūsmu saistītus e-pasta ziņojumus
description: Sistēmu varat konfigurēt tā, lai lietotājiem sūtītu e-pasta ziņojumus, kad notiek ar darbplūsmu saistīti notikumi.
author: jasongre
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 368fe2fbf1f8a1adcabe37ced5ed942f9fb86fc8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070429"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Ļaut lietotājiem saņemt ar darbplūsmu saistītus e-pasta ziņojumus

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Sistēmu varat konfigurēt tā, lai lietotājiem sūtītu e-pasta ziņojumus, kad notiek ar darbplūsmu saistīti notikumi. Piemēram, e-pasta ziņojumus var nosūtīt lietotājiem, ja to apstiprināšanai ir piešķirti dokumenti. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.

1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Lietotāji > Lietotāji**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. **Darbību rūtī** noklikšķiniet uz **Lietotāja opcijas**.
4. Noklikšķiniet uz cilnes **Darbplūsma**. Pārliecinieties, ka sadaļa **Paziņojumi** ir izvērsta. Sadaļā **Paziņojumi** varat norādīt, kā paziņot lietotājam par notikumiem, kas ir saistīti ar darbplūsmu.  
5. Laukā **Rindas vienuma darbplūsmas paziņojuma veids** atlasiet kādu opciju.
    - Grupēti — paziņojumi par rindas krājumiem tiek grupēti vienā e-pasta ziņojumā.
    - Atsevišķi — e-pasta ziņojums tiek nosūtīts katram rindas krājumam.  
    - Ja vēlaties, lai lietotājs saņem paziņojumus klientā, tad atzīmējiet izvēles rūtiņu **Sūtīt paziņojumus ar e-pasta ziņojumu**.  
6. Noklikšķiniet uz **Saglabāt**.
7. Aizvērt lapu.

> [!NOTE]
> Darbplūsmas e-pasta veidnes tiks iegūtas no sistēmas e-pasta veidnēm vai organizācijas e-pasta veidnēm atkarībā no tā, vai darbplūsma ir sistēmas līmeņa (nav specifiska uzņēmumam) vai organizācijas līmeņa (specifiska uzņēmumam) darbplūsma.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]