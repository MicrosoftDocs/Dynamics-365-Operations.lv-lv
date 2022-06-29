---
title: Kases vides Dynamics 365 Commerce nodrošināšana
description: Šajā rakstā skaidrots, kā nodrošināt kastu Microsoft Dynamics 365 Commerce vidi demonstrācijas vai kastes lietošanai ar iebūvētiem demonstrācijas datiem.
author: psimolin
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3ada30fc9d86d236b71d018ef77f2ae8573f2285
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013140"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Kases vides Dynamics 365 Commerce nodrošināšana

[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā nodrošināt kastu Microsoft Dynamics 365 Commerce vidi demonstrācijas lietošanai ar iebūvētiem demonstrācijas datiem. Ražošanas vides iestatīšanas process ir līdzīgs, bet plašāks, jo daudzi no kastu vides priekšnosacījumi jau ir sniegti demonstrācijas datos.

Pirms sākat, ir ieteicams ātri skenēt šo rakstu, lai iegūtu procesam vajadzīgo priekšstatu.

Lai veiksmīgi nodrošinātu Commerce vadīklu vidi, ir jānorāda daži vides un Commerce Scale Unit (CSU) parametri, kas tiks izmantoti, kad nodrošināt Commerce vēlāk. Šajā rakstā sniegtās instrukcijas apraksta visus soļus, kas ir nepieciešami nodrošinājuma pabeigšanai, kā arī parametrus, kas jums ir jāizmanto.

Pēc veiksmīgas komercijas nodrošināšana ir jāveic daži pēc nodrošinājuma soļi, lai sagatavotu to izmantošanai. Daži soļi ir izvēles atkarībā no sistēmas aspektiem, kurus vēlaties izmantot. Pēc izvēles veicamās darbības vienmēr varat pabeigt vēlāk.

Papildinformāciju par to, kā konfigurēt Commerce vidi pēc tās uzkrājuma, skatiet sadaļā [Commerce kases vides konfigurēšana](cpe-post-provisioning.md). Papildinformāciju par to, kā konfigurēt commerce (Commerce) vides neobligātos līdzekļus, skatiet šeit: [Izvēles līdzekļu konfigurēšana Commerce kases vides vidē](cpe-optional-features.md).

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu nodrošināt commerce vidi, jābūt šādiem priekšnosacījumi:

- Jums ir piekļuve Microsoft Dynamics Lifecycle Services (LCS) portālam.
- Jūs esat esošs Microsoft Dynamics 365 partneris vai debitors un jums jau ir izveidots ieviešanas projekts, un tas ir pieejams izmantošanai LCS.  
- Esat izveidojis Azure Active Directory (-Azure AD usi) drošības grupu, kuru var lietot kā Commerce sistēmas administratoru grupu, un jums ir pieejams tās ID.
- Ir izveidota drošības grupa Azure AD, kuru var izmantot kā vērtējumus un pārskata regulētāja grupu, un jums ir pieejams tās ID. (Šī drošības grupa var būt tāda pati kā Commerce sistēmas administratoru grupa.)
- Jūs esat izvietojis galvenā biroja instanci LCS. Papildinformāciju skatiet sadaļā [Jaunas vides izvietošana](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Ņemiet vērā, ka šis saraksts nav pilnīgs. Ja rodas kādas problēmas, sazinieties ar Microsoft partnera kontaktpersonu, lai saņemtu palīdzību.

## <a name="provision-your-commerce-environment"></a>Nodrošināt jūsu Commerce vidi

Tālākās procedūras skaidro veidu, kā nodrošināt Commerce vidi. Kad darbības būs veiksmīgi pabeigtas, commerce vide būs gatava konfigurācijai. Visas tālāk aprakstītās darbības jāveic LCS portālā.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Unit (mākoņa) inicializēšana

Lai inicializētu CSU, veiciet tālāk norādītās darbības.

1. LCS sarakstā atlasiet vidi.
1. Labajā pusē **vides** skatā atlasiet Pilnu **informāciju**. Parādīsies detalizēts vides informācijas skats.
1. Sadaļā Pārvaldīt **vidi zem** VIDES LĪDZEKĻI **atlasiet** Pārvaldīt **·**.
1. **Cilnē Commerce Scale Units** atlasiet **Inicializēt**. Tiek **parādīts skats Pievienot mēroga** vienību.
1. Laukā **REĢIONS** atlasiet reģionu, kas ir tas pats vai tuvu reģionam, kam izvietojāt vidi.
1. **Nolaižamajā sarakstā** Versija atlasiet jaunāko pieejamo versiju.
1. Atlasiet **Inicializēt**.
1. Brīdinājuma dialoglodziņā, kurā tiek lūgts apstiprināt Commerce Scale Unit inicializāciju, atlasiet **Jā**. CSU tagad ir rindots nodrošinājumam.
1. Pirms turpināt, pārliecinieties, ka jūsu CSU statuss ir **veiksmīgs**. Inicializācija ilgst aptuveni divas līdz piecas stundas.

Ja nevarat atrast saiti **Pārvaldība** vides informācijas skatā, sazinieties ar Microsoft kontaktpersonu, lai saņemtu palīdzību.

### <a name="initialize-e-commerce"></a>E-tirdzniecības inicializēšana

Lai inicializētu Commerce, sekojiet šiem soļiem.

1. Cilnē **E-tirdzniecība** atlasiet **Iestatīt**.
1. Laukā **E-tirdzniecības novērtējuma nosaukums** ievadiet nosaukumu. Ņemiet vērā, ka šis nosaukums parādīsies dažos URL vietrāžos, kas norāda uz jūsu e-tirdzniecības instanci.
1. Laukā **Commerce Scale Unit nosaukums** atlasiet savu CSU. (Sarakstā jābūt tikai vienai opcijai.)

    Lauks **E-tirdzniecības ģeogrāfija** tiek iestatīts automātiski.

1. Lai turpinātu, atlasiet **Tālāk**.
1. Laukā **Atbalstītie resursdatora nosaukumi** ievadiet jebkuru derīgu domēnu, piemēram, `www.fabrikam.com`.
1. Laukā **Sistēmas administratora AAD drošības grupa** ievadiet tās drošības grupas nosaukuma pirmos dažus burtus, ko vēlaties izmantot, un pēc tam atlasiet lupas simbolu, lai skatītu meklēšanas rezultātus. Sarakstā atlasiet pareizo drošības grupu.
1.  Laukā **Vērtējumu un pārskatu moderatora AAD drošības grupa** ievadiet tās drošības grupas nosaukuma pirmos dažus burtus, ko vēlaties izmantot, un pēc tam atlasiet lupas simbolu, lai skatītu meklēšanas rezultātus. Sarakstā atlasiet pareizo drošības grupu.
1. Atstājiet opciju **Iespējot vērtējumu un pārskatu pakalpojumu** iestatītu uz **Jā**.
1. Atlasiet **Inicializēt**. **Commerce pārvaldības** skats tie atkal parādīts tur, kur ir atlasīt cilne **e-komercija**. Ir uzsākta e-tirdzniecības inicializēšana.
1. Pirms turpināt, uzgaidiet, līdz Commerce inicializācijas statuss ir INICIALIZĒŠANA **SEKMĪGA**.
1. Apakšā pa labi no **Saites** norakstiet URL tālāk noradītajām saitēm.

    * **E-tirdzniecības vietne** — saite uz jūsu e-tirdzniecības vietnes sakni.
    * **Commerce vietņu veidotājs** – saite uz vietnes pārvaldības rīku.

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu Commerce vides nodrošinājuma un konfigurēšanas procesu, [skatiet Sadaļu Commerce kases vides konfigurēšana](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Papildu resursi

[Konfigurēt kases Dynamics 365 Commerce vides](cpe-post-provisioning.md)

[Konfigurēt BTOPS kastēs Dynamics 365 Commerce](cpe-bopis.md)

[Konfigurēt kases vides neobligātos Dynamics 365 Commerce līdzekļus](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (mākonis)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portāls](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
