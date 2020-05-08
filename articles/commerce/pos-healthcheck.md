---
title: Veselības pārbaude POS perifērijas ierīcēm un pakalpojumiem
description: Šajā tēmā sniegts pārskats par veselības pārbaudes darbību pārdošanas punktā (POS).
author: rubendel
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2c7e481b37a304188ab672308d915c714547d6f3
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265553"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Veselības pārbaude POS perifērijas ierīcēm un pakalpojumiem

[!include [banner](includes/banner.md)]

Šī tēma apraksta veselības pārbaudes darbību pārdošanas punktā (POS).

## <a name="overview"></a>Pārskats

Mazumtirdzniecības veikali var būt sarežģīti vidē, kur tiek izmantotas daudzas lietojumprogrammas un ierīces. Pieaugot operācijām, var būt sarežģīti nodrošināt, ka darbības vienmēr norit raiti, piemēram, atkarībā no perifērijas ierīcēm, kas var pārtraukt vai netīši kļūt atvienotas dienas gaitā. Problēmu novēršana, kas saistīta ar ierīcēm un pakalpojumiem, var būt dārga lielākam komersantam un tikpat apgrūtinoša mazākām darbībām.

Microsoft Dynamics 365 Commerce versijas 10.0.10 un jaunākas ietver veselības pārbaudes operāciju, kas var palīdzēt novērst daļu no šīm izmaksām un aiztaupīt satraukumu. Šī operācija nodrošina metodi ierīču testēšanai tieši no POS papildu parastajām operācijām. Tādēļ tas var palīdzēt mazumtirgotājiem noteikt problēmas pirms to rašanās.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | apraksts |
|---|---|
| Perifērās ierīces | Jebkura ierīce, kuru izmanto POS programma, lai atvieglotu darbības un citas operācijas veikalā. Piemēri ietver naudas kastes, svītrkodu skenerus un maksājumu termināļus. |
| Pakalpojumi | Šajā tēmā pakalpojums ir papildu programma, no kā POS lietojumprogramma ir atkarīga, lai veiktu darījumus un ikdienas darbības. Piemēram, ir programmas, kas palīdz veikt nodokļu vai sūtīšanas aprēķinus. |

## <a name="health-check-operation"></a>Veselības pārbaudes darbība

Veselības pārbaudes darbība ir darbība 717, kas atrodas **POS darbības** lapā Commerce Headquarters. To var izmantot, kamēr POS ir nesagatavotā režīmā. Tomēr aparatūras stacijai ir jābūt aktīvai.

Pēc noklusējuma veselības pārbaudes testus pārbauda tikai tās ierīces, kas ir konfigurētas aparatūras profilam aparatūras stacijai, kas pašlaik ir aktīva reģistram. Ja reģistrs izmanto vairākas aparatūras stacijas dienas gaitā, lai veiktu veselības pārbaudes, tai vienlaikus ir jāizveido savienojumu ar vienu aparatūras staciju. Nav veikala līmeņa veselības pārbaudes. Tomēr ir iespējams, ka šāda veida pārbaudi var veikt, izmantojot Commerce Server paplašinājumu.

### <a name="out-of-box-health-checks"></a>Veselības pārbaudes, kas veiktas pēc izvēles

| tips | Savienojums | Detalizēta |
|---|---|---|
| Printeris | OPOS | Šis tests pārbauda pamata objektu saistīšanu un iegulšanu POS (OPOS) funkcijām. Daži piemēri:<ul><li>Atvērt: **Atvērt** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Aizvērt: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Aizvērt**</li></ul> |
| Rindu displejs | OPOS | Šis tests pārbauda pamata OPOS funkcijas. Daži piemēri:<ul><li>Atvērt: **Atvērt** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Aizvērt: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Aizvērt**</li></ul> |
| Duālais displejs | Windows | Šis tests nodrošina, ka operētājsistēma nosaka otru Windows displeju. | 
| MJL (magnētiskās joslas lasītājs) | OPOS | Šis tests pārbauda pamata OPOS funkcijas. Daži piemēri:<ul><li>Atvērt: **Atvērt** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Aizvērt: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Aizvērt**</li></ul> |
| Naudas kaste | OPOS | Šis tests pārbauda pamata OPOS funkcijas. Daži piemēri:<ul><li>Atvērt: **Atvērt** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Aizvērt: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Aizvērt**</li></ul> | 
| Skeneris | OPOS | Šis tests pārbauda pamata OPOS funkcijas. Daži piemēri:<ul><li>Atvērt: **Atvērt** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Aizvērt: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Aizvērt**</li></ul> | 
| Mērogs | OPOS | Šis tests pārbauda pamata OPOS funkcijas. Daži piemēri:<ul><li>Atvērt: **Atvērt** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Aizvērt: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Aizvērt**</li></ul> |
| PIN bloks | OPOS | Šis tests pārbauda pamata OPOS funkcijas. Daži piemēri:<ul><li>Atvērt: **Atvērt** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Aizvērt: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Aizvērt**</li></ul> |
| Maksājumu terminālis | Maksājumu SDK | Šis tests pārbauda pamata maksājumu termināļa funkcijas, ko nodrošina Maksājumu SDK. <ul><li>Bloķēt</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Tuva</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Izmantojot veselības pārbaudes darbību POS sistēmā

Kad tiek uzsākta veselības pārbaudes darbība sistēmā POS, rūtī pa labi ir konfigurēto ierīču saraksts un tiek parādīts katras ierīces statuss. Lai veiktu vienas ierīces veselības pārbaudi, atlasiet ierīci un atlasiet **Pārbaudīt atlasīto**. Lai veiktu veselības pārbaudi visām ierīcēm, izvēlieties **Pārbaudīt visu**. Funkcija **Pārbaudīt vidu** pārbauda visas ierīces, pa vienai vienlaicīgi, un atjaunina katras ierīces statusu kolonnā **Statuss**.

**Pēdējā pārbaudes** kolonna rāda, kad veselības pārbaude tika veikta katrai ierīcei pēdējo reizi.

Ja ierīces veselības pārbaude (tas ir, ja kļūdas nav konstatētas), ierīces statuss būs **Labi**. Ja veselības pārbaude neizdodas, statuss parāda, ka radusies kļūda. Šajā gadījumā rūts labajā pusē sniedz detalizētu informāciju, kas saistīta ar kļūdu, vai arī uzdod lietotājam sazināties ar sistēmas administratoru.

Dažām ierīcēm, piemēram, OPOS taustiņslēgam, nav ¨out-of-box¨ veselības pārbaudes testu. Ja veselības pārbaudes tests netiek noteikts nevienai ierīcei, kas tiek lietota, statuss būs **Netiek atbalstīts**.

### <a name="extending-health-checks"></a>Veselības pārbaužu paplašināšana

"Out-of-box" veselības pārbaudes testi ir konfigurēti tā, lai sniegtu lietotājam draudzīgus ziņojumus par tipiskām kļūdām. Tomēr ne visi scenāriji ir ietverti. Izmantojot paplašināšanu, tirgotāji var kartēt lietotājam draudzīgus ziņojumus par kļūdām, kas varētu būt raksturīgas viņu videi.

Pielāgotas veselības pārbaudes var izveidot arī, lai testētu ierīces, kas nav atbalstītas ¨out-of-the-box¨, vai lai pārbaudītu visus pakalpojumus, uz ko balstās sistēma POS.

## <a name="related-articles"></a>Saistītie raksti

[Modern POS (MPOS) un Cloud POS trigera paplašināmība](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/modern-pos-trigger-extensibility)
