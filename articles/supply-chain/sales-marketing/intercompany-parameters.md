---
title: Starpuzņēmumu parametri
description: Šajā tēmā skaidroti starpuzņēmumu parametri
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 78186d466d88f876629ceb81ec99b94c8818c560
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678608"
---
# <a name="intercompany-parameters"></a>Starpuzņēmumu parametri

[!include [banner](../../includes/banner.md)]

Starpuzņēmumu organizācijā var iestatīt parametrus, kas nosaka tirdzniecības veidu starp dažādiem uzņēmumiem. Šos parametrus nosaka atlasītie lauki. Varat atlasīt dažādas kombinācijas, lai atspoguļotu dažādus tirdzniecības scenārijus.

Nākamie divi piemēri parāda vienu starpuzņēmumu organizāciju ar diviem līmeņiem un vienu ar trim līmeņiem.

## <a name="example-1-two-level-intercompany-chain"></a>1. piemērs. Divu līmeņu starpuzņēmumu ķēde

Starpuzņēmumu organizācija ietver šādas juridiskas personas:

- Juridiska persona A – pārdod ārējiem debitoriem, bet nav rezerves. Šī juridiskā persona pērk no juridiskās personas B.
- Juridiska persona B – pārdod tikai juridiskai personai A.

Abas juridiskās personas var pārdot un pirkt viens no otra.

Šajā piemērā cenu noteikšana oriģinālajā pārdošanas pasūtījumā, kurš ir virzīts uz ārējo debitoru, vienmēr tiek pamatota ar pārdošanas cenu. Cenu noteikšanu starpuzņēmumu pārdošanas pasūtījumā un starpuzņēmumu pirkšanas pasūtījumā kontrolē iekšējā pārdošanas/pārsūtīšanas cenu noteikšana starpuzņēmumu pārdošanas pasūtījumā iekšējā pārdošanas uzņēmumā (B).

Pasūtījuma virsraksta informācija tiek kontrolēta no oriģinālā pārdošanas pasūtījuma līdz ārējam debitoram. Nekādas izmaiņas starpuzņēmumu pārdošanas pasūtījumā netiek sinhronizētas ar oriģinālo pārdošanas pasūtījumu.

Juridiskās personas A lapā **Starpuzņēmumu** kreditoriem atlasiet **Pirkšanas pasūtījumu politikas**. Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums (tiešā piegāde)**:

- **Drukāt pavadzīmi automātiski**
- **Grāmatot rēķinu automātiski**
- **Drukāt rēķinu automātiski**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums (tiešā piegāde)**:

- **Grāmatot rēķinu automātiski**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums <-> Starpuzņēmumu pirkšanas pasūtījums**:

- **Informācija par debitoru**
- **RMA numurs**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums <-> Starpuzņēmumu pirkšanas pasūtījums**:

- **Informācija par debitoru**
- **RMA numurs**
- **Paketes numurs**
- **Sērijas numurs**

Juridiskās personas B lapā **Starpuzņēmumu** debitoriem atlasiet **Pārdošanas pasūtījumu politikas**. Atlasiet šādus laukus lauku grupā **Starpuzņēmumu pārdošanas pasūtījuma izveide**:

- **Pārdošanas pasūtījumu numerācija**: **Uzņēmums + oriģinālais numurs**
- **Atļaut dokumentu kopsavilkuma atjauninājumu oriģinālajam debitoram**

Atlasiet šādus laukus lauku grupā **Starpuzņēmumu pārdošanas pasūtījuma cenas**:

- **Cenas un atlaides meklēšana**
- **Ļaut labot cenu**
- **Ļaut labot atlaidi**

Atlasiet šādus laukus lauku grupā **Starpuzņēmumu pārdošanas pasūtījums \> Starpuzņēmumu pirkšanas pasūtījums**:

- **Paketes numurs**
- **Sērijas numurs**

## <a name="example-2-three-level-intercompany-chain"></a>2. piemērs. Trīs līmeņu starpuzņēmumu ķēde

Starpuzņēmumu organizācija ietver šādas juridiskas personas:

- Juridiska persona A – pārdošanas juridiska persona, kas pārdod ārējiem debitoriem un pērk no juridiskās personas B.
- Juridiska persona B – ražošanas vai izplatīšanas juridiska persona, kas nevar piegādāt preces un pērk no juridiskās personas C.
- Juridiska persona B – ražošanas vai izplatīšanas juridiska persona, kas nevar piegādāt preces un pērk no juridiskās personas C.

Iekšējā transfertcena noteikšana starp juridiskām personām B un C ir pēc izmaksām no pārdošanas juridiskās personas ķēdes sākumā. Tā ir arī par cenu juridiskai personai A, kas pārdod ārējiem debitoriem. Tomēr cenu noteikšana oriģinālajā pārdošanas pasūtījumā ārējam debitoram vienmēr pamatojas uz pārdošanas cenu.

Cenu noteikšana visos starpuzņēmumu pārdošanas pasūtījumos un starpuzņēmumu pirkšanas pasūtījumos tiek kontrolēta starpuzņēmumu pārdošanas pasūtījumā. To kontrolē ķēdes sākumā. Tāpēc juridiskā persona C, kas pārdod juridiskai personai B, kontrolē cenu. Starpuzņēmumu pārdošanas pasūtījuma cenu noteikšana tiek pamatota uz iekšējo pārdošanas vai pārsūtījuma cenu noteikšanu, kas tiek saglabāta iekšējā pārdošanas uzņēmumā C.

Pasūtījuma virsraksta informācija tiek kontrolēta no oriģinālā pārdošanas pasūtījuma līdz ārējam debitoram. Nekādas izmaiņas starpuzņēmumu pasūtījumos netiek sinhronizētas ar oriģinālo pārdošanas pasūtījumu.

Vajadzētu atlasīt šādus parametrus:

Juridiskās personas A lapā **Starpuzņēmumu** kreditoriem atlasiet **Pirkšanas pasūtījumu politikas**. Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums (tiešā piegāde)**:

- **Drukāt pavadzīmi automātiski**
- **Grāmatot rēķinu automātiski**
- **Drukāt rēķinu automātiski**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums (tiešā piegāde)**:

- **Grāmatot rēķinu automātiski**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums <-> Starpuzņēmumu pirkšanas pasūtījums**:

- **Informācija par debitoru**
- **RMA numurs**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums <-> Starpuzņēmumu pirkšanas pasūtījums**:

- **Informācija par debitoru**
- **RMA numurs**
- **Paketes numurs**
- **Sērijas numurs**

Juridiskās personas B lapā **Starpuzņēmumu** debitoriem atlasiet **Pārdošanas pasūtījumu politikas**. Atlasiet šādus laukus lauku grupā **Starpuzņēmumu pārdošanas pasūtījuma izveide**:

- **Pārdošanas pasūtījumu numerācija**: **Uzņēmums + oriģinālais numurs**
- **Atļaut dokumentu kopsavilkuma atjauninājumu oriģinālajam debitoram**

Atlasiet šādus laukus lauku grupā **Starpuzņēmumu pārdošanas pasūtījums \> Starpuzņēmumu pirkšanas pasūtījums**:

- **Paketes numurs**
- **Sērijas numurs**

Atlasiet šādus laukus lauku grupā **Starpuzņēmumu debitoru rēķinu grāmatošana**:

- **Vienības cena ir vienāda ar izmaksu cenu**
- **Sākt sākotnējā debitora rēķina grāmatošanu**

Juridiskās personas B lapā **Starpuzņēmums** kreditoriem atlasiet **Pirkšanas pasūtījumu politikas**. Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums (tiešā piegāde)**:

- **Drukāt pavadzīmi automātiski**
- **Grāmatot rēķinu automātiski**
- **Drukāt rēķinu automātiski**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums (tiešā piegāde)**:

- **Grāmatot rēķinu automātiski**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums <-> Starpuzņēmumu pirkšanas pasūtījums**:

- **Informācija par debitoru**
- **RMA numurs**
- **Cena un atlaide**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums <-> Starpuzņēmumu pirkšanas pasūtījums**:

- **Informācija par debitoru**
- **RMA numurs**
- **Paketes numurs**
- **Sērijas numurs**

Juridiskās personas C lapā **Starpuzņēmumu** debitoriem atlasiet **Pārdošanas pasūtījumu politikas**. Atlasiet šādus laukus lauku grupā **Starpuzņēmumu pārdošanas pasūtījuma izveide**:

- **Pārdošanas pasūtījumu** numerācija: **numuru sērijas kods**
- **Atļaut dokumentu kopsavilkuma atjauninājumu oriģinālajam debitoram**

Atlasiet šādus laukus lauku grupā **Starpuzņēmumu pārdošanas pasūtījuma cenas**:

- **Cenas un atlaides meklēšana**

Atlasiet šādus laukus lauku grupā **Starpuzņēmumu debitoru rēķinu grāmatošana**:

- **Vienības cena ir vienāda ar izmaksu cenu**
- **Sākt sākotnējā debitora rēķina grāmatošanu**

Atlasiet šādus laukus lauku grupā **Oriģinālais pārdošanas pasūtījums <-> Starpuzņēmumu pirkšanas pasūtījums**:

- **Paketes numurs**
- **Sērijas numurs**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
