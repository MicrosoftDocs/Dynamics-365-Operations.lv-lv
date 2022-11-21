---
title: Juridiskās personas piekļuves ierobežošana darbiniekiem
description: Šajā rakstā ir paskaidrots, kā iestatīt nodarbinātā piekļuvi juridiskajai personai.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780301"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Juridiskās personas piekļuves ierobežošana darbiniekiem

Šajā rakstā ir paskaidrots, kā iestatīt nodarbinātā piekļuvi juridiskajai personai.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Darbinieki tiek nodarbināti juridiskās personās. Daži piemēri:

- Ārons Kons ir nodarbināts USSI juridiskajā personā.
- Ahmeds Barnets ir nodarbināts USMF juridiskajā personā.
- Alicia Thornber ir nodarbināta GLSI un USMF juridiskajās personās.

Atkarībā no lietotāja lomas uzņēmumā viņam var būt nepieciešama piekļuve, lai skatītu visus darbiniekus visās juridiskajās personās. Vai arī lietotājam var būt jābūt ierobežotam, lai viņš varētu skatīt tikai tās juridiskās personas darbiniekus, kurai viņam ir piekļuve. Lai kontrolētu, kurus darbiniekus lietotājs var skatīt, atlasiet **parametru** Ierobežot piekļuvi informācijai par darbiniekiem **lapā Personāla vadības koplietojamie parametri**.

Piemēram, lietotājam ir piekļuve lapai Darbinieks **,** un viņam ir piekļuve tikai USMF juridiskajai personai. Šādā gadījumā lietotājs var skatīt šādu informāciju par darbiniekiem iepriekšējā sarakstā:

- Ja līdzeklis, kas ierobežo piekļuvi darbinieku informācijai, nav iespējots, lietotājs var skatīt informāciju par Āronu, Ahmedu un Alīsiju.
- Ja šis līdzeklis ir iespējots, lietotājs var skatīt informāciju tikai par Alicia un Ahmed, jo viņi ir nodarbināti arī USMF juridiskajā personā.

Parādītā informācija atšķiras atkarībā no izmantotās lietojumprogrammas.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources savrups

Ja ir iespējots līdzeklis piekļuves ierobežošanai darbinieku informācijai, lietotājs redzēs tukšu vērtību dažos sarakstos, kuros ir darbinieka vārds.

Piemēram, lietotājs, kuram ir piekļuve tikai USMF juridiskajai personai, saskarsies ar šādu rīcību:

- **Sarakstā** Aktīvās pozīcijas **kolonna Darbinieks** būs tukša Ārona amatam, jo lietotājam nav piekļuves USSI juridiskās personas darbiniekiem.
- Ja lietotājs detalizē darbinieka vārdu, tiks parādīta tukša **lapa Darbinieks**.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources par finanšu infrastruktūru

Ja ir iespējots līdzeklis piekļuves ierobežošanai darbinieku informācijai, ierobežotā lietotāja vārds būs redzams dažos sarakstos.

Piemēram, lietotājs, kuram ir piekļuve tikai USMF juridiskajai personai, saskarsies ar šādu rīcību:

- **Sarakstā** Aktīvās pozīcijas **kolonnā Darbinieks** tiks rādīts Ārona vārds. Ja lietotājs novieto kursoru virs darbinieka vārda, tiks parādīts tikai vārds un amats.
- Ja lietotājs detalizē darbinieka vārdu, tiks parādīta tukša **lapa Darbinieks**.

> [!TIP]
> Ja izmantojat Dynamics 365 Human resources on Finance infrastruktūra un vēlaties, lai lietotāji ar ierobežotiem resursiem redzētu tukšas vērtības darbinieku vārdiem, varat pievienot **drošības atļauju Ierobežot piekļuvi darbiniekiem** lietotāju lomām **lapā Drošības konfigurācija**.

Pēc līdzekļa iespējošanas jums ir jāveic dažas papildu darbības, lai iestatītu atļaujas katram lietotājam, kura skats ir jāierobežo.

1. Lapā **Lietotāji** atlasiet lietotāju.
2. Izvēlieties lietotājam lomu. Opcija **Piešķirt organizācijas** kļūst pieejama.
3. Atlasiet **Piešķirt organizācijas**.
4. Jaunajā lapā atlasiet **Atsevišķi piešķirt piekļuvi noteiktām organizācijām** un pēc tam atlasiet organizācijas, kurām lietotājam būs piekļuve.
5. Atkārtojiet 2. līdz 4. darbību visām citām lietotāja lomām, ieskaitot sistēmas lietotāja lomu.

> [!NOTE]
> Juridiskajām personām, kurām lietotājs var piekļūt, ir jāatbilst visām lietotāja lomām.
