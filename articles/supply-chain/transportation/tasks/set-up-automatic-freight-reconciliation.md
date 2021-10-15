---
title: Automātiskās kravas saskaņošanas iestatīšana
description: Šajā procedūrā parādīts kā iestatīt datus automātiskai kravas saskaņošanai.
author: Henrikan
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1dbe3c683d869f86bc7231c68839f431cc61d6b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574837"
---
# <a name="set-up-automatic-freight-reconciliation"></a>Automātiskās kravas saskaņošanas iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts kā iestatīt datus automātiskai kravas saskaņošanai. To parasti veic noliktavas pārvaldnieks. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.


## <a name="set-up-the-freight-bill-type"></a>Kravas pavadzīmes veida iestatīšana
1. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Kravas saskaņošana > Kravas pavadzīmes veids.
    * Kravas pavadzīmes tips nosaka kā jāsaskaņo kravas pavadzīmes un pārvadātāja rēķinus.  
2. Noklikšķiniet uz Jauns.
3. Laukā Kravas pavadzīmes veids ievadiet vērtību.
4. Laukā Programmas komplektācija ierakstiet “Microsoft.Dynamics.Ax.Tms.dll”.
    * Tā ir standarta Transportēšanas pārvaldības atbilstoša programmas koda bibliotēka.  
5. Laukā Programmas klase ierakstiet “Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer”.
    * Tā ir standarta Transportēšanas pārvaldības atbilstoša programmas koda klase.  
6. Noklikšķiniet uz Jauns.
7. Laukā Apraksts atlasiet vērtību, kas atbilst kravas pavadzīmei un pārvadātāja rēķinam.  
8. Laukā Nepieciešama saskaņošana atlasiet Jā.
    * Ja iestatāt šajā laukā Jā, tas nozīmē, ka vērtībai, kas ir atlasīta laukā Apraksts ir jāatbilst gan kravas pavadzīmei, gan pārvadātāja rēķinam. Ja iestatāt Nē, lauks var būt tukšs vienā no tiem.  
9. Noklikšķiniet uz Saglabāt.

## <a name="set-up-the-freight-bill-type-assignment"></a>Kravas pavadzīmes veida piešķires iestatīšana
1. Aizvērt lapu.
2. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Kravas saskaņošana > Kravas pavadzīmes veida piešķires.
    * Kravas pavadzīmes veida piešķire tiek izmantota, lai norādītu, kuras kravas pavadzīmes veids tiek izmantots noteiktam pārvadātājam.   
3. Noklikšķiniet uz Jauns.
4. Laukā Režīms ievadiet vai atlasiet vērtību.
5. Laukā Sūtījumu pārvadātājs ievadiet vai atlasiet kādu vērtību.
6. Laukā Kravas pavadzīmes veids atlasiet kravas pavadzīmes veidu, ko izveidojāt agrāk.
7. Aizvērt lapu.

## <a name="set-up-the-audit-master"></a>Audita šablona iestatīšana
1. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Kravas saskaņošana > Audita šablons.
    * Audita šablons nosaka tolerances ierobežojumus automātiskai kravas saskaņošanai. Tas norāda par cik daudz var atšķirties naudas summas kravas pavadzīmē un pārvadātāja rēķinā, un joprojām pieļaut saskaņošanu. Tas arī nosaka kā apstrādāt neatbilstības.  
2. Noklikšķiniet uz Jauns.
3. Laukā Audita šablona ID ierakstiet vērtību.
4. Laukā Sūtījumu pārvadātājs atlasiet to pašu sūtījumu pārvadātāju, kā to darījāt iepriekš.
5. Laukā Kravas pavadzīmes veids atlasiet kravas pavadzīmes veidu, ko izveidojāt agrāk.
6. Izvērsiet sadaļu Tolerance.
7. Laukā Minimālais tolerances līmenis ievadiet kādu skaitli.
8. Laukā Maksimālās tolerances līmenis ievadiet kādu skaitli.
9. Izvērsiet sadaļu Rezultāts.
10. Laukā Pārmaksas iemesla kods ievadiet vai atlasiet kādu vērtību.
    * Ja naudas summas atšķiras no kravas pavadzīmes un pārvadātāja rēķina, pārmaksas un nepilnas samaksas iemesla kodi norāda kontus, kuros nepieciešams reģistrēt starpību, ja vien starpība nepārsniedz tolerances līmeņus.  
11. Laukā Nepilnas samaksas iemesla kods ievadiet vai atlasiet kādu vērtību.
12. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]