---
title: Finanšu saskaņošana mazumtirdzniecības veikalos
description: Šajā tēmā ir aprakstīta finanšu saskaņošana mazumtirdzniecības veikalos POS programmatūrai Microsoft Dynamics 365 Commerce.
author: anpurush
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2afe967248136e9b658e1ee18053a54ab3f0d325c088a5eb2e522fac335c01f0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752463"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Finanšu saskaņošana mazumtirdzniecības veikalos

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce versijā 10.0.10 un vecākās versijās funkcionalitāte, ko pārdošanas punkta (POS) klients nodrošina darbadienas beigu procesiem mazumtirdzniecības veikalos, ļauj veikalu darbiniekiem un veikalu vadītājiem veiktu darbadienas beigu operācijas. Piemēram, veikt norēķinu uzskaites, diskrētas slēgšanas maiņas, maiņu transakciju saskaņošanu un maiņu slēgšanu. Tomēr POS nav iespēja pabeigt finanšu informāciju maiņām, lai to varētu izmantot, iegrāmatojot finanses Commerce Headquarters. Parasti veikala vadītāji ir atbildīgi par šī uzdevuma pabeigšanu. Pirms izrakstīties no maiņas, ir jāpārskata informācija, jāveic visi nepieciešamie labojumi un jāpabeidz šīs maiņas kopsummas. Pēc tam kopsummas grāmato finanšu moduļos Commerce Headquarters.

Turklāt Commerce versija 10.0.10 un vecākās versijās veikala vadītāji var pārskatīt un veikt dažas korekcijas Commerce Headquarters pārskata rindās. Tomēr iespēja ir ierobežota, un veikala vadītājiem reti ir piekļuve Commerce Headquarters klientam. Turklāt finanšu mazumtirdzniecības pārskata pārskatīšanu un korekciju var veikt tikai tad, ja pārskati ir izveidoti Commerce Headquarters. Tomēr šis process parasti ir nakts process. Tāpēc veikala vadītājiem ir jāgaida maiņas izrakstīšanās, kad finanšu mazumtirdzniecības pārskati tiek veidoti programmā Commerce Headquarters.

Commerce versija 10.0.11 un jaunākās veikala vadītāji var pārskatīt, pielāgot un pabeigt savas maiņas POS klientā. Pēc tam šos datus izmanto finanšu mazumtirdzniecības pārskatu izveidei un grāmatošanai Commerce Headquarters.

> [!NOTE]
> Ar finanšu saskaņošanu mazumtirdzniecības veikalos saistītā funkcionalitāte darbojas tikai tad, ja ir ieslēgta pakāpeniskas plūsmas pasūtījuma izveide. Papildinformāciju skatiet sadaļā [Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Iestatīt finanšu saskaņošanu

Lai izmantotu finanšu saskaņošanas funkcionalitāti, rīkojieties šādi.

1. Darbvietā **Līdzekļu pārvaldība** ieslēdziet līdzekli **Mazumtirdzniecības pārskati - pakāpeniska plūsma**.
1. Attiecīgā veikala POS funkcionalitātes profilā iestatiet opciju **Iespējot finanšu saskaņošanu veikalā** uz **Jā**.

## <a name="more-information-about-financial-reconciliation"></a>Papildinformācija par finanšu saskaņošanu

Kad ir ieslēgta finanšu saskaņošanas funkcionalitāte, daži parametri, kas ir definēti Commerce headquarters lapas **Mazumtirdzniecības veikali** kopsavilkuma cilnē **Izraksts/slēgšana** tiek sinhronizēti ar kanāla datu bāzi. Tiek izpildīts tas pats aprēķina kritēriju kopums un summas robežvērtības, kas tiek izmantotas mazumtirdzniecības pārskatos.

Kad ir izsaukta operācija **Maiņas slēgšana**, sistēma validē, vai sistēmas aprēķinātās summas un deklarētās summas atbilst. Ja tās atšķiras un atšķirība pārsniedz definētos sliekšņus, lietotājam tiek piedāvāts veikt nepieciešamās korekcijas.

Korekcijas var veikt katram piedāvājumam. Kad ir atlasīts norēķins, lietotājs var apskatīt dažādu transakciju veidu kopsummas un rediģēt noteikta transakciju veida kopsummas. Rediģēšanas laikā sistēma parāda sākotnējo aprēķināto summu un šī transakcijas veida ignorēto summu. Lietotājs var tvert arī piezīmes kā rediģēšanas procesa daļu. Piezīmes var izmantot auditēšanas nolūkiem.

Lietotāji var ignorēt validēšanas uzvednes un ziņojumus, un var turpināt, lai aizvērtu maiņu. Tomēr, ja lietotājs ignorē validācijas uzvednes, tās pašas problēmas saglabāsies un būs jālabo, kad maiņas grāmato finanšu pārskatus Commerce Headquarters.

POS operācija **Slēgt maiņu** validē, ka visas transakcijas bezsaistes datu bāzē tiek sinhronizētas ar kanāla datu bāzi. Ja kādas transakcijas netiek sinhronizētas, lietotājs saņem brīdinājuma ziņojumu, jo šī situācija var izraisīt sistēmas summu kļūdainu aprēķināšanu. Šādā gadījumā lietotājs var beigt operāciju **Slēgt maiņu** un mēģināt sinhronizēt bezsaistes transakcijas ar kanāla datu bāzi. Vai arī lietotājs var manuāli koriģēt sistēmas aprēķinātās summas, lai uzskaitītu transakcijas, kas nav sinhronizētas, lai tiktu pabeigta un grāmatota pareizā finanšu numuru kopa. 

Kad tiek izmantota pakāpeniskās plūsmas pārskata grāmatošana, lai transakciju grāmatošana tiktu nodalīta no finanšu grāmatošanas, varat izvēlēties koriģēt sistēmas aprēķinātās summas trūkstošajām bezsaistes transakcijām. Šādā veidā tiek nodrošināts, ka finanses vienmēr tiek pareizi ieskaitītas un grāmatotas, neatkarīgi no trūkstošajām transakcijām. Bezsaistes transakcijas var sinhronizēt ar kanāla datu bāzi un Commerce Headquarters un grāmatot vēlāk, atsevišķi no finanšu grāmatojumiem.

Detalizēta informācija par finanšu saskaņošanu maiņā tiek sinhronizēta ar Commerce Headquarters, izmantojot P–darbu.

Finanšu mazumtirdzniecības pārskati Commerce Headquarters neaprēķina kopsummas, lai parādītu informāciju par pārskata rindām. Tā vietā POS klienta faktiskie apjomi tiek izmantoti finanšu mazumtirdzniecības pārskatu izveidei un grāmatošanai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]