---
title: Asinhronais debitoru izveides režīms
description: Šajā tēmā ir aprakstīts asinhronais klientu izveides režīms programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 22bb4eaf3d4897904412120fa5580c42637b56e0
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913777"
---
# <a name="asynchronous-customer-creation-mode"></a>Asinhronais debitoru izveides režīms

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir aprakstīts asinhronais klientu izveides režīms programmā Microsoft Dynamics 365 Commerce.

Programmā Commerce ir divi klientu izveides režīmi: sinhrons (vai sinhronizēts) un asinhrons (vai asinhrons). Klienti pēc noklusējuma tiek izveidoti sinhroni. Citiem vārdiem sakot, tos izveido Commerce galvenajā pārvaldē reāllaikā. Sinhronizācijas klientu izveides režīms ir izdevīgs, jo jauni klienti ir nekavējoties meklējami kanālos. Taču šim režīmam ir arī trūkums. Tā kā tas uz Commerce galveno pārvaldi ģenerē zvanus [Commerce Data Exchange: Reāllaika pakalpojums](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service), var tikt ietekmēts sniegums, ja secīgi tiek veikti vairāki klientu izveides zvani.

Ja opcija **Izveidot klientu asinhronajā režīmā** ir iestatīta uz **Jā** veikala funkcionalitātes profilā (**Retail un Commerce\>Kanāla iestatīšana\>Tiešsaistes veikala iestatīšana\>Funkcionalitātes profili**), reāllaika pakalpojuma zvani netiek izmantoti klientu ierakstu izveidei kanāla datu bāzē. Asinhronais klientu izveides režīms neietekmē Commerce headquarters veiktspēju. Pagaidu globāli unikālais identifikators (GUID) tiek piešķirts katram jaunam asinhronajam debitora ierakstam un izmantots kā debitora konta ID. Šis GUID netiek rādīts tirdzniecības vietas (POS) lietotājiem. Tā vietā šie lietotāji kā klienta konta ID redzēs **Gaida sinhronizāciju**.

> [!IMPORTANT]
> Ikreiz, kad POS pāriet bezsaistē, sistēma automātiski izveido klientus asinhroni, pat ja asinhronais klienta izveides režīms ir atspējots. Tāpēc neatkarīgi no atlases starp sinhronizāciju un asinhrono klientu izveidi Commerce headquarters administratoriem ir jāizveido un jāplāno periodisks pakešuzdevums **P darbam, sinhronizēt** **klientus un biznesa partnerus no asinhronā režīma** darba (iepriekš saukts **Par Sinhronizēt klientus un biznesa partnerus no asinhronā režīma**) un **1010** darbs, lai visi asinhronie klienti tiktu konvertēti par klientu sinhronizāciju Commerce headquarters.

## <a name="async-customer-limitations"></a>Asinhrono klientu ierobežojumi

Asinhronajai klienta funkcionalitātei pašlaik ir šādi ierobežojumi:

- Asinhrono klientu ierakstus nevar rediģēt, ja vien Commerce galvenajā pārvalde nav izveidots klients un jaunais klienta konta ID nav sinhronizēts atpakaļ kanālā.
- Lojalitātes programmas kartes nevar izsniegt asinhronajiem klientiem, ja vien jaunais debitora konta ID nav sinhronizēts atpakaļ kanālā.

## <a name="async-customer-enhancements"></a>Asinhronie debitoru uzlabojumi

No Commerce versijas 10.0.24 laidiena līdzekļu pārvaldības darbvietā varat iespējot **uzlabotās asinhronās klientu izveides** **līdzekli**. Šī funkcija novērš plaisu starp asinhronās un sinhronizācijas klientu izveides režīmiem POS un e-komercijā šādos veidos:

- Piederību var saistīt ar asinhronajiem debitoriem.
- Nosaukumus var pievienot asinhronajiem debitoriem.
- Asinhronajiem klientiem var tvert sekundārās e-pasta adreses un tālruņu numurus.

No Commerce versijas 10.0.22 laidiena līdzekļu pārvaldības darbvietā var iespējot **līdzekli Iespējot asinhrono izveidi klientu** **adresēm**. Šis līdzeklis ļauj asinhroni saglabāt jaunizveidotās klientu adreses gan sinhronizācijas klientiem, gan asinhronajiem klientiem.

Pēc iepriekš minēto līdzekļu iespējošana ir jāieplāno periodisks pakešuzdevums **P darbam, sinhronizēt** **klientus un biznesa partnerus no asinhronā režīma** darba un **1010** darbam, lai visi asinhronie klienti tiktu konvertēti par klientu sinhronizāciju programmā Commerce Headquarters.

### <a name="customer-creation-in-pos-offline-mode"></a>Klientu izveide POS bezsaistes režīmā

Kā minēts iepriekš, ikreiz, kad POS pāriet bezsaistē, sistēma automātiski izveido klientus asinhroni, pat ja asinhronais klientu izveides režīms ir atspējots. Tāpēc Commerce headquarters administratoriem ir jāizveido un jāplāno periodisks pakešuzdevums **P darbam, sinhronizēt** **klientus un biznesa partnerus no asinhronā režīma** darba un **1010** darbam, lai visi asinhronie klienti tiktu konvertēti par klientu sinhronizāciju programmā Commerce Headquarters.

> [!NOTE]
> Ja opcija **Filtra kopīgotās klientu datu tabulas** ir iestatīta uz **Jā** lapā **Commerce kanālu shēma** (**Retail un Commerce\>Galvenās pārvaldes iestatīšana\>Commerce plānotājs\>Kanālu datu bāzes grupa**), klienta ieraksti netiek izveidoti POS bezsaistes režīmā. Papildinformāciju skatiet tēmā [Datu izņemšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Papildu resursi

[Klientu pārvaldība veikalos](customer-mgmt-stores.md)

[Asinhrono debitoru pārvēršana par sinhroniem debitoriem](convert-async-to-sync.md)

[Debitora atribūti](dev-itpro/customer-attributes.md)

[Datu izslēgšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
