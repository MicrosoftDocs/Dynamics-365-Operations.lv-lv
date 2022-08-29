---
title: Pārdošanas punkta (POS) programma un lietotāja valodas iestatījumi
description: Šajā rakstā ir aprakstīts, kā mainīt valodas iestatījumus sistēmā Modern POS (MPOS) un Cloud POS.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.industry: Retail
ms.search.form: HcmWorker, RetailStoreTable
ms.openlocfilehash: 663e9a3558bd4d0556644fe5ad6f7f832a18ded5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288384"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Pārdošanas punkta (POS) programma un lietotāja valodas iestatījumi

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā mainīt valodas iestatījumus sistēmā Modern POS (MPOS) un Cloud POS.

## <a name="overview"></a>Pārskats
Programmas Modern POS (MPOS) un Cloud POS atbalsta vides, kurās veikala un lietotāja iestatījumos var atšķirties valodas iestatījumi un tulkojumi. Piemēram, veikals var atrasties reģionā, kur vairums debitoru runā angļu valodā, taču daži nodarbinātie vēlas izmantot lietojumprogrammu ar tulkojumiem franču valodā.

## <a name="data-language"></a>Datu valoda

Neatkarīgi no lietotāja iestatījumiem programmās MPOS un Cloud POS vienmēr tiek izmantoti veikala valodas iestatījumi, lai noteiktu datiem lietotos tulkojumus. Tādējādi tiek nodrošināts, ka visiem lietotājiem un debitoriem ir pieejamas vienādas iespējas. Tālāk ir norādīti datu piemēri.

- Preces
- Atribūti un vērtības
- Kategoriju nosaukumi
- Drukātas vai e-pastā sūtītas transakciju kvītis
- Maksāšanas metožu nosaukumi
- Rindu displeja ziņojumi

Veikala valoda tiek lietota arī galvenajā POS pieteikšanās ekrānā, jo pirms pieteikšanās nav zināms, kurš lietotājs izmanto POS. Ja nav pieejams tulkojums veikala valodā, POS tiek pārslēgts atpakaļ uzņēmuma valodā.

### <a name="configuring-the-stores-language-setting"></a>Veikala valodas iestatījumu konfigurēšana

Veikala valodas iestatījumu var norādīt, lapas **Veikals** sadaļā **Visi veikali** noklikšķinot uz **Vispārīgi &gt; Reģionālie iestatījumi &gt; Valoda**. Izmantojiet nolaižamo izvēlni, lai izvēlētos katra veikala valodu.

## <a name="user-interface-language"></a>Lietotāja interfeisa valoda

POS lietotāja valodas iestatījums nosaka tulkojumus, kas tiek izmantoti programmas lietotāja interfeisā. Tas attiecas uz visām etiķetēm, izvēlnēm un sarakstiem, kas netiek uzskatīti par datiem. Vienīgais izņēmums ir teksts, kas tiek rādīts POS pogu režģos. Pogu režģi neatbalsta tulkojumus, tāpēc tajos teksts vienmēr tiek rādīts tā, kā tas ir definēts uz pogas. Lai nodrošinātu pogu tulkojumus, ir jākopē un jāuztur atsevišķi pogu režģi un tie ir jāpiešķir atbilstošajiem lietotājiem.

### <a name="configuring-the-users-language-setting"></a>Lietotāja valodas iestatījumu konfigurēšana

POS lietotāja valodas iestatījums tiek iestatīts, lapas **Darbinieks** sadaļā **Visi darbinieki** atlasot **Retail un Commerce &gt; Valoda**. Tas netiek iestatīts galvenajā cilnē Profils. Šo iestatījumu neizmanto POS. Ja lietotāja valoda nav iestatīta vai tā ir iestatīta uz valodu, kurā tulkojumi nav pieejami, POS atiestatīs veikala valodu.

| &nbsp;      | UI valoda                | Datu valoda (preces, kvīšu formāti, rindu displejs utt.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Uzņēmums** | Noklusējums                    | Noklusējums                                                       |
| **Veikals**   | Ignorē uzņēmumu          | Ignorē uzņēmumu                                             |
| **Lietotājs**    | Ignorē veikalu vai uzņēmumu | Nekad                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
