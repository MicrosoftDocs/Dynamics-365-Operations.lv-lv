---
title: Atcelt noliktavas darbu izņēmumu apstrādei
description: Šajā rakstā ir aprakstīta atceltā darba funkcionalitāte, kas ļauj noliktavas supervizoriem veikt bloķētu darbu.
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
ms.openlocfilehash: b1e2036e4e7a8a47d6df029f285df7aca0fa74e6
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404432"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Atcelt noliktavas darbu izņēmumu apstrādei

[!include [banner](../includes/banner.md)]

Sistēmas Microsoft darba funkcionalitātes atcelšana Dynamics 365 Supply Chain Management ļauj administratoram atcelt noteiktu noliktavas darbu, kas pašreiz notiek, bet to bloķē sistēma vai to nevar pabeigt ārkārtēju apstākļu dēļ. Šī funkcionalitāte ir pievilcīga un droša alternatīva SQL labojošajiem skriptiem, kas labo nekonsekventus datus. Tomēr, tā kā šos skriptus parasti pieprasa IT profesionāļiem, atcelšanas darba funkcionalitāti var izmantot lietotāji uzņēmumā, kam ir administratora tiesības.

Varat piekļūt darba atcelšanas funkcionalitātei, kas pieejama noliktavas **pārvaldības periodisko** \> **uzdevumu tīrīšanas** \> **un \> atcelšanas darbā.** Dialoglodziņā **Atcelt darbu** norādiet darba ID darbam, kas jāatceļ, un pēc tam atlasiet **Labi**.

## <a name="warehouse-work-that-can-be-canceled"></a>Noliktavas darbs, kuru var atcelt

Veicot noliktavas izdošanas darbības, darbinieks var saskarties ar situācijām, kad tiem ir reģistrēti daudzumi kā izdoti no glabāšanas vietas uz to lietotāja atrašanās vietu, taču tad tie nevar reģistrēt izvietošanas darbību. Nekonsekventi noliktavas dati bieži, bet ne vienmēr, ir iemesls, kāpēc darbs tiek bloķēts.

Atšķirībā no **parastās** atcelšanas funkcionalitātes, kam var piekļūt, izmantojot pogu Atcelt darba galvenē, darba atcelšanas funkcionalitātei nav nepieciešams, **lai pēdējā pabeigtā darba rinda būtu izvietošanas veida darba** rinda. Citiem vārdiem sakot, darba atcelšanas funkcionalitātei atcelšanas loģiku var palaist pat tad, ja krājumu daudzums darba rindā ir lietotāja novietojumā.

> [!NOTE]
> Darba nolūkos, kas ir jāatceļ darbību iemeslu dēļ, noliktavas lietotājiem darba lapā ir jāturpina izmantot parasto atcelšanas funkcionalitāti.

Izmantojot darba funkcionalitāti **Atcelt**, **·** **var** atcelt tikai pārdošanas, pārsūtīšanas izdošanas, **izejmateriālu** izdošanas vai papildināšanas veida darbu. Atcelšanas loģika netiks palaista iesaldētu izejmateriālu izdošanas darbam vai darbam, ko var atcelt, izmantojot parasto atcelšanas funkcionalitāti (skatiet iepriekšējo piezīmi).

Lai atbloķētu darbu, sistēma atceļ visas atlikušās darba rindas un labo noliktavas datus, kas ir saistīti ar lietotāja norādīto darba ID. Pēc tam var atsākt visas parastās noliktavas apstrādes darbības, kas ietver ietekmēto vienību daudzumu.

Lai ietekmēto vienību izvietotu noteiktā vietā pēc darba atcelšanas, lietotājam jāizmanto krājumu kustība vai daudzuma korekcijas operācija mobilajā ierīcē.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]