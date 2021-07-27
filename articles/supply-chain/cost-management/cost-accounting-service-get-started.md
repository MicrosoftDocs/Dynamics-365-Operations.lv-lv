---
title: Darba sākšana ar izmaksu uzskaites pakalpojumu (privāts priekšskatījums)
description: Šajā tēmā ir sniegta informācija par licencēšanu un izmaksu uzskaites pakalpojuma instalēšanas instrukcijām.
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 207c9dfe9e49b845d2c98040c1571099e01b43f7
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337700"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Darba sākšana ar izmaksu uzskaites pakalpojumu (privāts priekšskatījums)

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Šajā tēmā minētā funkcionalitāte ir pieejama kā daļa no privātā priekšskatījuma laidiena. Šīs tēmas saturs un tās aprakstītā funkcionalitāte var tikt mainīti. Papildinformāciju par priekšskatījuma laidieniem skatiet sadaļā [Bieži uzdotie jautājumi par vienas versijas pakalpojuma atjauninājumiem](../../fin-ops-core/fin-ops/get-started/one-version.md).

Izmaksu uzskaites pakalpojums ļauj veikt vairāku krājumu uzskaiti izmaksu uzskaites virsgrāmatās, kas iestatītas. Katru izmaksu uzskaites virsgrāmatu saistiet ar *konvenciju*. Konvencija ir šādu uzskaites ierobežojumu tipu apkopojums:

- Izmaksu objekts
- Ievades mērījumu bāze
- Izmaksu plūsmas pieņēmums
- Izmaksu elements

> [!NOTE]
> Pat pēc tam, kad esat ieslēdzis izmaksu uzskaites pakalpojumu, jūs joprojām varat veikt krājumu uzskaiti programmā Microsoft Dynamics 365 Supply Chain Management, kā parasti.

Izmaksu uzskaites pakalpojums ir pievienojumprogramma. Lai padarītu šīs funkcijas pieejamas, tās ir jāinstalē no Microsoft Dynamics Lifecycle Services (LCS). Tāpēc varat izvēlēties to novērtēt testa vidē pirms tā ieslēgšanas ražošanas vidē.

Izmaksu uzskaites pakalpojums pašlaik neatbalsta visus izmaksu pārvaldības līdzekļus, kas ir iebūvēti Dynamics 365 Supply Chain Management. Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama, atbilst jūsu prasībām.

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Kā sākt darbu ar izmaksu uzskaites pakalpojumu (privātais priekšskats)

> [!IMPORTANT]
> Lai izmantotu izmaksu uzskaites pakalpojumu, ir jābūt ar LCS iespējotai augstas pieejamības videi (ne OneBox videi), un jums ir jāpalaiž Dynamics 365 Supply Chain Management versija 10.0.11 vai jaunāka.

Lai pieteiktos izmaksu uzskaites pakalpojuma privātajam priekšskatījumam, lūdzu, nosūtiet jūsu LCS vides ID pa e-pastu uz [Izmaksu uzskaites pakalpojumu (privāts priekšskatījums)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29). Apstiprinot jūs programmā, mēs jums nosūtīsim sekojuma e-pasta ziņojumu, kurā būs ietverta izmaksu uzskaites pakalpojuma beta atslēga. Saņemot beta atslēgu, varat turpināt, [instalējot pievienojumprogrammu](#install).

## <a name="licensing"></a>Licencēšana

Izmaksu uzskaites pakalpojums ir licencēts kopā ar krājumu uzskaites standarta funkcijām, kas ir pieejamas Supply Chain Management. Jums nav jāiegādājas papildu licence, lai izmantotu izmaksu uzskaites pakalpojumu.

## <a name="install-the-add-in"></a><a name="install"></a>Pievienojumprogrammas instalēšana

Lai izmantotu izmaksu uzskaites pakalpojumu, instalējiet izmaksu uzskaites pakalpojumu pievienojumprogrammu Supply Chain Management, kā aprakstīts šajā procedūrā.

1. [Pierakstieties](#sign-up) izmaksu uzskaites pakalpojumam (privāts priekšskatījums).

1. Pierakstieties LCS.

1. Dodieties uz **Priekšskatīt līdzekļu pārvaldību**.

1. Atlasiet plus zīmi (**+**).

1. Laukā **Kods** ievadiet savu papildinājuma beta atslēgu izmaksu uzskaites pakalpojumam. (Jums vajadzētu saņemt jūsu atslēgu pa e-pastu.)

1. Atlasiet **Atbloķēt**.

1. Atveriet LCS vidi, kurā vēlaties pievienot pakalpojumu.

1. Doties **Pilna detalizēta informācija**.

1. Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.

1. Atlasiet **Instalēt jaunu pievienojumprogrammu**.

1. Atlasiet **Izmaksu uzskaites pakalpojums**.

1. Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.

1. Atlasiet **Instalēt**.

1. Kopsavilkuma cilnē **Vides pievienojumprogramma** jūs redzēsiet, ka tiek instalēts izmaksu uzskaites pakalpojums. Pēc dažām minūtēm statusam jāmainās no **Instalē** uz **Instalēts**. (Iespējams, ka ir jāatsvaidzina lapa, lai skatītu šīs izmaiņas.) Šajā brīdī izmaksu uzskaites pakalpojums ir gatavs lietošanai.

## <a name="set-up-the-integration"></a>Iestatiet integrēšanu

Lai iestatītu integrēšanu starp izmaksu uzskaites pakalpojumu un Dynamics 365 Supply Chain Management:

1. Dodieties uz **Sistēmas administrēšana > Līdzekļu pārvaldība**.

1. Atlasiet **Pārbaudīt atjauninājumus**.

1. Atveriet cilni **Visi** un meklējiet līdzekli ar nosaukumu *Izmaksu uzskaites pakalpojums*.

1. Atlasiet **Iespējot tagad**.

1. Dodieties uz **Izmaksu pārvaldība > Izmaksu uzskaites pakalpojums > Iestatīšana > Izmaksu uzskaites pakalpojuma parametri > Integrēšanas parametri**.

1. Laukā **Programmas ID** ievadiet šādu kodu:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. Laukā **Datu pakalpojuma galapunkts** ievadiet šādu vietrādi URL:<br>https://operationsdataservice.operations365.dynamics.com/

1. Laukā **Izmaksu uzskaites pakalpojuma galapunkts** ievadiet šādu vietrādi URL:<br>https://costaccountingservice.operations365.dynamics.com/

1. Izmaksu uzskaites pakalpojums tagad ir gatavs lietošanai.

## <a name="related-resources"></a>Saistītie resursi

[Izmaksu uzskaites pakalpojuma sākumlapa](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]