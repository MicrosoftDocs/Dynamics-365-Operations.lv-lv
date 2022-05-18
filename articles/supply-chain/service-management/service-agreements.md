---
title: Izstrādes un veidošanas pakalpojumu līgumu pārskats
description: Izmantojot pakalpojumu līgumus, varat definēt resursus, ko izmantot tipiskā pakalpojumu vizītē, un veidu, kā šie resursi tiek iekļauti klienta rēķinos.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 559f4571a60ea8ec048b291e3b6a0a93e8bc9d44
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677707"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Izstrādes un veidošanas pakalpojumu līgumu pārskats

[!include [banner](../includes/banner.md)]

Izmantojot pakalpojumu līgumus, varat definēt resursus, ko izmantot tipiskā pakalpojumu vizītē, un veidu, kā šie resursi tiek iekļauti klienta rēķinos.

Katrs pakalpojumu līgums ir piesaistīts projektam, tādējādi darbības tiek iegrāmatotas un par tām izrakstīti rēķini. Tomēr varat pakalpojuma pasūtījumu rēķinos iekļaut arī tieši caur projektu, vispirms nesavienojot pakalpojuma pasūtījumu ar pakalpojumu līgumu. Varat izlemt tā rīkoties, ja pakalpojuma pasūtījums ir tikai vienreizēja pakalpojumu vizīte un nepieciešamība apstrādāt šīs pakalpojumu darbības ātri atsver nepieciešamību uzturēt detalizētu pakalpojumu līguma informāciju par attiecīgo klientu laika periodā.

## <a name="service-agreement"></a>Pakalpojumu līgums

Katrā pakalpojumu līgumā jānorāda projekts, pakalpojumu līguma ID un pakalpojumu līgumu grupa. Pakalpojumu līgumu grupu var izmantot, lai šķirotu un sakārtotu pakalpojumu līgumus.

Pakalpojumu līguma galvene satur iestatījumus, kas attiecas uz visām pievienotajām līguma rindām:

-  Vai pakalpojumu līgums ir aizturēts. Ja pakalpojumu līgums ir aizturēts, no šī pakalpojumu līguma nevar ģenerēt pakalpojuma pasūtījumus.
-  Pakalpojumu līguma ilgums.
-  Veids, kādā pakalpojuma pasūtījuma rindas jākombinē pakalpojuma pasūtījumos.
-  Vai pakalpojumu līgums ir veidne.

Pakalpojumu līguma galvenē iestatāt arī visus pakalpojumu objektus un pakalpojumu uzdevumus, ko var izmantot ar šo pakalpojumu līgumu, ievadot konkrētos pakalpojumu uzdevumus vai pakalpojumu objektus, kas tiks pievienoti dažādām līguma rindām.

No pakalpojumu līguma galvenes varat arī pašreizējā pakalpojumu līgumā kopēt pakalpojumu līguma rindas vai pakalpojuma veidnes rindas.

Jūs varat aizturēt pakalpojumu līgumus un apturēt individuālas pakalpojumu līguma rindas.

Ja atzīmējat izvēles rūtiņu **Aizturēts** pakalpojumu līguma rindā, jūs nevarat:

-    manuāli vai automātiski izveidot pakalpojuma pasūtījumus no pakalpojumu līguma rindas.

Ja atzīmējat izvēles rūtiņu **Apturēts** pakalpojumu līguma rindā, jūs nevarat:

-    manuāli vai automātiski izveidot pakalpojuma pasūtījumus no pakalpojumu līguma;
-    Kopējiet pakalpojumu līguma rindu citā pakalpojumu līgumā vai pakalpojuma pasūtījumā.


> [!NOTE]
> Ja pakalpojumu līgums ir aizturēts, visas pievienotās rindas arī ir apturētas neatkarīgi no to individuālā statusa.

## <a name="service-agreement-lines"></a>Pakalpojumu līguma rindas

Katrā pakalpojumu līguma rindā ir detalizēti aprakstīts piedāvātā pakalpojumu darba saturs. Šīs rindas satur šādus iestatījumus:

-  Darbības tips un darbības tipa apraksts.
-  Darbinieks, kas veic šo pakalpojumu darbu.
-  Objekti, kam saskaņā ar šo pakalpojumu līgumu pakalpojums jāveic.
-  Tiek reģistrēts biežums, kādā tiek veikts šis darbs, un saistītās krājuma, izmaksu un apmaksas darbības.
-  Laika logs, kur pakalpojuma pasūtījuma rindas var grupēt pakalpojuma pasūtījumā.
-  Pakalpojumu uzdevumi, kas tiek izmantoti līguma rindu kopu grupēšanai kopā darba uzdevumos un kopsavilkuma izveidei pakalpojumu tehniķiem un klientiem par to, kādi pakalpojumu uzdevumi tiek sniegti.
-  Norāda, vai rinda ir apturēta. Ja rinda ir apturēta, nevarat šai atsevišķajai rindai izveidot pakalpojuma pasūtījumus.
-  Projekta iestatījumi, tādi kā kategorija un rindas statuss.

## <a name="related-topics"></a>Saistītās tēmas

[Pakalpojumu līgumu izveide](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]