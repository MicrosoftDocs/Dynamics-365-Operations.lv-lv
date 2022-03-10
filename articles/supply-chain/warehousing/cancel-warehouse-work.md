---
title: Atcelt noliktavas darbu izņēmumu apstrādei
description: Šajā tēmā ir aprakstīta funkcionalitāte Atcelt darbu, kas ļauj noliktavas uzraudzītājiem apstrādāt bloķētu darbu.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: af0c147eefbfe22cb6b6d531f514e6f293d66689
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572413"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Atcelt noliktavas darbu izņēmumu apstrādei

[!include [banner](../includes/banner.md)]

Funkcija Atcelt darbu sistēmā Microsoft Dynamics 365 Supply Chain Management ļauj administratoram lietotājam atcelt konkrētu pašlaik notiekošu noliktavas darbu, kuru sistēma ir bloķējusi vai to nevar pabeigt ārkārtēju apstākļu dēļ. Šī funkcionalitāte ir pievilcīga un droša alternatīva SQL labojošajiem skriptiem, kas labo nekonsekventus datus. Tomēr, tā kā šie skripti parasti tiek pieprasīti no IT profesionāļiem, funkcionalitāti Atcelt darbu var izmantot tie lietotāji uzņēmumā, kam ir administratora tiesības.

Varat piekļūt funkcionalitātei Atcelt darbu sadaļā **Noliktavas pārvaldība** \> **Periodiskie uzdevumis** \> **Iztīrīt \> Atcelt darbu**. Dialoglodziņā **Atcelt darbu** norādiet darba ID darbam, kas jāatceļ, un pēc tam atlasiet **Labi**.

## <a name="warehouse-work-that-can-be-canceled"></a>Noliktavas darbs, kuru var atcelt

Veicot noliktavas izdošanas darbības, darbinieks var saskarties ar situācijām, kad tiem ir reģistrēti daudzumi kā izdoti no glabāšanas vietas uz to lietotāja atrašanās vietu, taču tad tie nevar reģistrēt izvietošanas darbību. Nekonsekventi noliktavas dati bieži, bet ne vienmēr, ir iemesls, kāpēc darbs tiek bloķēts.

Atšķirībā no parastās atcelšanas funkcionalitātes, kam var piekļūt, izmantojot pogu **Atcelt** darba virsrakstā, funkcionalitātei Atcelt darbu nav nepieciešams, lai pēdējā pabeigtā darba rinda būtu **izvietošanas** veida darba rinda. Citiem vārdiem sakot, funkcionalitātei Atcelt darbu atcelšanas loģiku var palaist pat tad, ja krājuma daudzums darba rindā ir lietotāja atrašanās vietā.

> [!NOTE]
> Darbam, kas jāatceļ operatīvu iemeslu dēļ, noliktavas lietotājiem ir jāturpina izmantot parasto atcelšanas funkcionalitāti darba lapā.

Izmantojot funkcionalitāti Atcelt darbu, var atcelt tikai **Pārdošanas**, **Izsniegšanas pārsūtīšanai**, **Izejmateriālu izdošanas** vai **Papildināšanas** veida darbu. Atcelšanas loģika netiks palaista iesaldētam izejmateriālu izdošanas darbam vai darbam, ko var atcelt, lietojot parasto atcelšanas funkcionalitāti (sk. iepriekšējo piezīmi).

Lai atbloķētu darbu, sistēma atceļ visas atlikušās darba rindas un labo noliktavas datus, kas ir saistīti ar lietotāja norādīto darba ID. Pēc tam var atsākt visas parastās noliktavas apstrādes darbības, kas ietver ietekmēto vienību daudzumu.

Lai ietekmēto vienību izvietotu noteiktā vietā pēc darba atcelšanas, lietotājam jāizmanto krājumu kustība vai daudzuma korekcijas operācija mobilajā ierīcē.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]