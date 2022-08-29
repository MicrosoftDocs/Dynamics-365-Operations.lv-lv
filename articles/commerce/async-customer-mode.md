---
title: Asinhronā debitora izveides režīms
description: Šajā rakstā ir aprakstīts asinhronais debitoru izveides režīms Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 1ac1bc842d5d12ece8951ffed18157e6f9b50d14
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228728"
---
# <a name="asynchronous-customer-creation-mode"></a>Asinhronā debitora izveides režīms

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā rakstā ir aprakstīts asinhronais debitoru izveides režīms Microsoft Dynamics 365 Commerce.

Komercijas programmā ir divi debitoru izveides veidi: sinhroni (vai sinhroni) un asinhroni (vai async). Klienti pēc noklusējuma tiek izveidoti sinhroni. Citiem vārdiem sakot, tie ir izveidoti Commerce Headquarters reāllaikā. Sinhronizācijas debitora izveides režīms ir no jauna, jo jaunie debitori nekavējoties var meklēt kanālos. Taču šim režīmam ir arī trūkums. Tā kā tas uz Commerce galveno pārvaldi ģenerē zvanus [Commerce Data Exchange: Reāllaika pakalpojums](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service), var tikt ietekmēts sniegums, ja secīgi tiek veikti vairāki klientu izveides zvani.

Ja opcija **Izveidot klientu asinhronajā režīmā** ir iestatīta uz **Jā** veikala funkcionalitātes profilā (**Retail un Commerce\>Kanāla iestatīšana\>Tiešsaistes veikala iestatīšana\>Funkcionalitātes profili**), reāllaika pakalpojuma zvani netiek izmantoti klientu ierakstu izveidei kanāla datu bāzē. Async debitora izveides režīms neietekmē commerce headquarters veiktspēju. Pagaidu globāli unikāls identifikators (GUID) tiek piešķirts katram jaunam async debitora ierakstam un tiek izmantots kā debitora konta ID. Šis GUID netiek rādīts pārdošanas punkta (POS) lietotājiem. Tā vietā šie lietotāji kā klienta konta ID redzēs **Gaida sinhronizāciju**.

> [!IMPORTANT]
> Ja POS darbojas bezsaistē, sistēma automātiski izveido debitorus asinhroni, pat ja async debitora izveides režīms ir atspējots. Tāpēc neatkarīgi no veiktās atlases starp sinhronizācijas un async debitoru izveidi Commerce Headquarters **administratoriem ir jāizveido un jāplāno periodisks pakešuzdevums P-darbam**, **sinhronizēt debitorus un biznesa partnerus no async** **režīma darba un 1010 darbu, lai visi async debitori** tiktu pārvērsti par sinhronizētiem debitoriem programmā Commerce Headquarters.

## <a name="async-customer-limitations"></a>Asinhrono klientu ierobežojumi

Async debitora funkcionalitātei pašlaik ir šāds ierobežojums:

- Lojalitātes programmas kartes nevar izsniegt async debitoriem, ja jaunais debitora konta ID nav sinhronizēts atpakaļ kanālā.

## <a name="async-customer-enhancements"></a>Async debitora uzlabojumi

Lai palīdzētu organizācijām izmantot async debitoru izveides režīmu, lai pārvaldītu debitorus un palīdzētu samazināt reāllaika sakarus ar programmu Commerce Headquarters, ir izcelti šādi uzlabojumi, lai kanālos izveidotu pārību starp sinhronizācijas un async režīmiem. 

| Līdzekļa uzlabojumi | Commerce versija | Līdzekļa detalizētā informācija |
|---|---|---|
| Veiktspējas uzlabojumi, kad debitora informācija tiek izgūta no kanāla datu bāzes | 10.0.20 vai jaunāka versija | Lai uzlabotu veiktspēju, debitora elements tiek sadalīts mazākās entītijās. Tad sistēma izgūst tikai nepieciešamo informāciju no kanāla datu bāzes. |
| Iespēja izveidot adresi asinhroni pārbaudes laikā | 10.0.22 vai jaunāka versija | <p>Funkcionalitātes pārslēgšana: **asinhronas izveidošanas iespējošana debitora adresēm**</p><p>Detalizēta informācija par līdzekli:</p><ul><li>Iespēja pievienot adreses, neveicot reāllaika pakalpojumu izsaukumus programmā Commerce Headquarters</li><li>Iespēja unikāli identificēt adreses kanāla datu bāzē, neizmantojot ieraksta ID (**RecId** vērtība)</li><li>Izsekošanas laikspiedolus adreses izveidošanai</li><li>Adrešu sinhronizācija programmā Commerce Headquarters</li></ul><p>Šis līdzeklis ietekmē gan sinhronizētos debitorus, gan async debitorus. Lai rediģētu adreses asinhroni papildus to asinhronai veidošanai, **jums ir jāiespējo Rediģēšanas debitoru asinhronā režīmā** funkcija.</p> |
| Iespējojiet sinhrono un asinhrono debitora izveidi. | 10.0.24 vai jaunāka versija | <p>Līdzekļu pārslēgšanās: **iespējojiet uzlabotu async debitoru izveidi**</p><p>Līdzekļa detaļas: spēja iegūt papildinformāciju, piemēram, nosaukumu, piederības no noklusējuma debitora, un sekundāro kontaktinformāciju (tālruņa numuru un e-pasta adresi), kamēr izveidojat debitorus asinhroni</p> |
| Lietotājam draudzīgs kļūdu ziņojums | 10.0.28 vai jaunāka versija | Šie uzlabojumi palīdz uzlabot lietotājam draudzīgās kļūdu ziņojumus, ja lietotājs nevar nekavējoties rediģēt informāciju sinhronizācijas laikā. Jūs iespējosiet šos uzlabojumus **, izmantojot Atļaut noteiktus UI elementus atmodīt, izmantojot async** **\> debitora iestatījumu Vietnes iestatījumos Paplašinājumi** Commerce Site Builder. |
| Iespēja rediģēt debitora informāciju asinhroni | 10.0.29 vai jaunāka versija | <p>Līdzekļu pārslēgšana: **iespējojiet debitoru rediģēšanu asinhronajā režīmā**</p><p>Detalizēta informācija par līdzekli: spēja rediģēt debitora datus asinhroni</p><p>Atbildes uz bieži uzdotiem jautājumiem par jautājumiem, kas ir saistīti ar debitora informācijas rediģēšanu asinhroni, [skatiet asinhronā debitora izveides režīma FAQ](async-customer-mode-faq.md).</p> |

### <a name="feature-switch-hierarchy"></a>Līdzekļu pārslēgšanās hierarhija

Sakarā ar līdzekļu pārslēgšanās hierarhiju, pirms iespējojat **iespējot debitoru rediģēšanu asinhronā** režīmā, ir jāiespējo šādas funkcijas: 

- **Debitoru pasūtījumu un debitoru darbību veiktspējas** uzlabojumi — šī funkcija ir obligāta kopš Commerce versijas 10.0.28 laidiena. 
- **Iespējot uzlabotu Async debitoru izveidi**
- **Iespējot klientu adrešu asinhrono izveidi**

Atbildes uz bieži uzdotiem traucējummeklēšanas jautājumiem [skatiet asinhronajā debitora izveides režīmā FAQ](async-customer-mode-faq.md). 

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
