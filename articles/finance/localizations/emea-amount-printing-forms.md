---
title: Atjaunināt veidu, kā summas tiek rādītas pārskatos un dokumentos
description: Šajā rakstā ir sniegta informācija, kā atjaunināt summas un kā summas tiek rādītas pārskatos un citos dokumentos Igaunijai, Latvijai, Lietuvai, Polijai, Čehijai, Ungārijai un Krievijai.
author: anasyash
ms.date: 01/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Currency
audience: Application User
ms.reviewer: kfend
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e985ffc156caa86da3a3e8c36122e4f73278ca7f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907711"
---
# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Atjaunināt veidu, kā summas tiek rādītas pārskatos un dokumentos

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija, kā atjaunināt summas un kā summas tiek rādītas pārskatos un citos dokumentos Igaunijai, Latvijai, Lietuvai, Polijai, Čehijai, Ungārijai un Krievijai.

Juridiskajām personām Igaunijā, Latvijā, Lietuvā, Polijā, Čehijā, Ungārijā un Krievijā valūtas vienībām un apakšvienībām varat iestatīt pilnos nosaukumus un īsos nosaukumus. Šos nosaukumus var izmantot, lai pārveidotu summu rādīšanu dokumentos un pārskatos. Piemēram, summa **LTL 100.20** var tikt parādīta kā **100 liti 20 centi**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Iestatīt pilnos un īsos nosaukumus valūtas vienībām un apakšvienībām
Lai kādai valodai iestatītu valūtas vienību un apakšvienību pilnos un īsos nosaukumus, izpildiet tālāk sniegtos norādījumus.

1. Atveriet lapu **Valūtas**.
2. Izvēlieties valūtu.
3. Darbību rūtī atlasiet **Novirze**.
4. Lai pievienotu valodas pilno nosaukumu un īso nosaukumu, atlasiet **Jauns** un ievadiet informāciju šādos laukos.

   |             Lauks                                                           |                        Apraksts                                                                                                                                                                                                                                                |
   |------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                       <strong>Valoda</strong>                        |                                                                                                               Atlasiet pašreizējā teksta valodu.                                                                                                                |
   |    <strong>Vienskaitļa nominatīvs (vienības nosaukumu lauku grupa)</strong>    |                                                                                       Ievadiet valūtas nosaukumu vienskaitļa formā. Piemēram, vienskaitļa forma no litiem ir “lits”.                                                                                       |
   |     <strong>Daudzskaitļa nominatīvs (vienības nosaukumu lauku grupa)</strong>     | Ievadiet valūtas nosaukumu daudzskaitļa formā. Ievadiet, piemēram, “liti”. <strong>Piezīme</strong>. Lauki <strong>Vienskaitļa ģenitīvs</strong> un <strong>Daudzskaitļa ģenitīvs</strong> ir pieejami atkarībā no valodas, kas atlasīta laukā <strong>Valoda</strong>. |
   | <strong>Vienskaitļa nominatīva lauks (daļu nosaukumu lauku grupa)</strong> |                                                                                                        Ievadiet valūtas apakšvienības nosaukumu vienskaitļa formā.                                                                                                         |
   |     <strong>Daudzskaitļa nominatīvs (daļu nosaukumu lauku grupa)</strong>     |                                                                                                         Ievadiet valūtas apakšvienības nosaukumu daudzskaitļa formā.                                                                                                          |
   |    <strong>Vienību saīsinātais nosaukums (īso nosaukumu lauku grupa)</strong>    |                                                                                         Ievadiet ISO kodu, lai identificētu attiecīgo valūtu. Piemēram, ievadiet LTL, lai identificētu litus.                                                                                         |
   |   <strong>Daļu saīsinātais nosaukums (īso nosaukumu lauku grupa)</strong>    |                                                                                               Ievadiet valūtas apakšvienības apzīmējumu. Ievadiet, piemēram, “centi”.                                                                                               |
   |       <strong>Saiklis “un” starp vienībām un daļām</strong>       |                                     Atzīmējiet šo opciju, lai starp valūtas vienībām un vienības daļām drukātu saikli “un”. Piemēram, rēķinos vai pārskatos summa LTL 100,20 tiks rādīta kā “100 liti un 20 centi”.                                      |
   |       <strong>Dzimums</strong>       |  Atlasiet **Vīrietis**, **Sieviete** vai **Neitrāls**. Šis parametrs var ietekmēt summas novirzes tekstu, kas parādīts Kases orderī vietējās valodas tekstā. Piemēram, **iestatot** valūtu EUR **valūtai EUR kā Neiteru**, summa 101 EUR *tiek rakstīta kases orderī čehu valodā kā Jedno euro 01 cents*.  |

5. Atlasiet **Saglabāt**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
