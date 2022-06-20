---
title: Asinhronā debitora izveides režīms
description: Šajā rakstā ir aprakstīts asinhronais debitoru izveides režīms Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 4ca63fe06a804035e976a3432454078c1cca0020
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880144"
---
# <a name="asynchronous-customer-creation-mode"></a>Asinhronā debitora izveides režīms

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts asinhronais debitoru izveides režīms Microsoft Dynamics 365 Commerce.

Komercijas programmā ir divi debitoru izveides veidi: sinhroni (vai sinhroni) un asinhroni (vai async). Klienti pēc noklusējuma tiek izveidoti sinhroni. Citiem vārdiem sakot, tos izveido Commerce galvenajā pārvaldē reāllaikā. Sinhronizācijas debitora izveides režīms ir no jauna, jo jaunie debitori nekavējoties var meklēt kanālos. Taču šim režīmam ir arī trūkums. Tā kā tas uz Commerce galveno pārvaldi ģenerē zvanus [Commerce Data Exchange: Reāllaika pakalpojums](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service), var tikt ietekmēts sniegums, ja secīgi tiek veikti vairāki klientu izveides zvani.

Ja opcija **Izveidot klientu asinhronajā režīmā** ir iestatīta uz **Jā** veikala funkcionalitātes profilā (**Retail un Commerce\>Kanāla iestatīšana\>Tiešsaistes veikala iestatīšana\>Funkcionalitātes profili**), reāllaika pakalpojuma zvani netiek izmantoti klientu ierakstu izveidei kanāla datu bāzē. Async debitora izveides režīms neietekmē commerce headquarters veiktspēju. Pagaidu globāli unikāls identifikators (GUID) tiek piešķirts katram jaunam async debitora ierakstam un tiek izmantots kā debitora konta ID. Šis GUID netiek rādīts pārdošanas punkta (POS) lietotājiem. Tā vietā šie lietotāji kā klienta konta ID redzēs **Gaida sinhronizāciju**.

> [!IMPORTANT]
> Ja POS darbojas bezsaistē, sistēma automātiski izveido debitorus asinhroni, pat ja async debitora izveides režīms ir atspējots. Tāpēc neatkarīgi no veiktās atlases starp sinhronizācijas un async debitoru izveidi Commerce headquarters **administratoriem ir jāizveido un jāplāno periodisks pakešuzdevums P darbam**, **Sinhronizējiet debitorus un biznesa partnerus no async** režīma darba (**iepriekš saukts par Sinhronizēt debitorus un biznesa partnerus no async** režīma), **un 1010** darbu, tādējādi visi async debitori tiek konvertēti sinhronizācijā ar debitoriem programmā Commerce Headquarters.

## <a name="async-customer-limitations"></a>Asinhrono klientu ierobežojumi

Async debitora funkcionalitātei pašlaik ir šādi ierobežojumi:

- Asinhrono klientu ierakstus nevar rediģēt, ja vien Commerce galvenajā pārvalde nav izveidots klients un jaunais klienta konta ID nav sinhronizēts atpakaļ kanālā.
- Lojalitātes programmas kartes nevar izsniegt async debitoriem, ja jaunais debitora konta ID nav sinhronizēts atpakaļ kanālā.

## <a name="async-customer-enhancements"></a>Async debitora uzlabojumi

Attiecībā uz Commerce versijas 10.0.24 laidienu, **varat iespējot iespējot uzlabotās async** **debitoru izveides līdzekli līdzekļu pārvaldības darbvietā**. Šis līdzeklis nodrošina atšķirību starp async un sync debitoru izveides režīmiem POS un e-komercijas sistēmā, izmantojot tālāk norādītos veidus.

- Piederības var saistīt ar async debitoriem.
- Nosaukumus var pievienot async debitoriem.
- Async debitoriem var fiksēt sekundārās e-pasta adreses un tālruņa numurus.

Attiecībā uz Commerce versijas 10.0.22 izlaidi, **jūs varat iespējot asinhronu** **klientu adrešu funkcijas izveidi Līdzekļu pārvaldības darbvietā**. Šis līdzeklis iespējo jaunizveidotās debitoru adreses asinhroni saglabāt gan sinhronizētajiem debitoriem, gan async debitoriem.

**Pēc iepriekš minēto līdzekļu iespējošanas ir jāplāno periodisks pakešuzdevums P darbam**, **sinhronizēt debitorus un biznesa partnerus no async** **režīma darba un 1010** darbu, lai visi async debitori tiktu pārvērsti sinhronizācijā ar debitoriem programmā Commerce Headquarters.

### <a name="customer-creation-in-pos-offline-mode"></a>Klientu izveide POS bezsaistes režīmā

Kā tika norādīts iepriekš, vienmēr, kad POS darbojas bezsaistē, sistēma automātiski izveido debitorus asinhroni, pat ja async debitora izveides režīms ir atspējots. Tāpēc Commerce Headquarters **administratoriem ir jāizveido un jāplāno periodisks pakešuzdevums P** darbam, **sinhronizēt debitorus un biznesa partnerus no async** režīma darba un **1010** darbu, lai visi async debitori tiktu pārvērsti sinhronizācijā ar debitoriem programmā Commerce Headquarters.

> [!NOTE]
> Ja opcija **Filtra kopīgotās klientu datu tabulas** ir iestatīta uz **Jā** lapā **Commerce kanālu shēma** (**Retail un Commerce\>Galvenās pārvaldes iestatīšana\>Commerce plānotājs\>Kanālu datu bāzes grupa**), klienta ieraksti netiek izveidoti POS bezsaistes režīmā. Papildinformāciju skatiet tēmā [Datu izņemšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Papildu resursi

[Klientu pārvaldība veikalos](customer-mgmt-stores.md)

[Asinhrono debitoru pārvēršana par sinhroniem debitoriem](convert-async-to-sync.md)

[Debitora atribūti](dev-itpro/customer-attributes.md)

[Datu izslēgšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
