---
title: Maksājuma rēķinu izveide
description: Šajā tēmā izskaidrots, kā izveidot ikmēneša nomas rēķinus. Varat izveidot rēķinus atsevišķām nomām, vai arī varat izmantot partijas procesu, lai izveidotu tos vairākām nomām.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bc87c329f6f5dd9532b1319f8d88fbc41dcd4d14
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344324"
---
# <a name="create-payment-invoices"></a>Maksājuma rēķinu izveide

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Varat izveidot ikmēneša rēķinus atsevišķām nomām, vai arī varat izmantot partijas procesu, lai izveidotu tos vairākām nomām. Tālāk minētajā procedūrā ir parādīts, kā izveidot atsevišķu nomas maksājuma ierakstu, ja ir ieslēgts parametrs **Maksāt kreditoram** lapā **Nomas grāmatas iestatīšana**.

1. Lapā **Nomas kopsavilkums** atlasiet nomu un pēc tam atlasiet **Grāmatas \> Maksājumu grafiks**.
2. Atlasiet maksājumu, kas ir jāveic, un pēc tam atlasiet **Izveidot žurnālu**. Tiek parādīts ziņojums, ka žurnāls tika izveidots atbilstoši atlasītajam maksājumam.
3. Atlasiet **Rēķinu žurnāli** un pēc tam atlasiet rēķinu, kas ir jāsamaksā.
4. Cilnē **Rindas** pārskatiet žurnāla ierakstu, pirms to grāmatot Virsgrāmatā.

    > [!NOTE]
    > Pēc noklusējuma izveidotās kreditora rēķina rindas izmanto kreditoru grāmatošanas profilu no lapas **Kreditora parādu parametri**.

5. Atlasiet pareizo žurnālu un pēc tam atlasiet rēķinu, kas ir jāsamaksā.

    Šajā piemērā nomas grāmatas parametrs **Maksāt kreditoram** ir ieslēgts. Tāpēc rēķins būs rēķinu žurnālā. Sadaļā **Pārskats** tiek parādīts žurnāla ieraksta kopsavilkums, un sadaļā **Rindas** tiek parādīta detalizēta informācija par faktiskajām žurnāla rindām.
    
   Sistēma bloķē noteiktus finanšu laukus, lai novērstu novirzes starp darbībām un grafikiem. Dažos bloķētos laukos ir iekļauts: **Konts**, **Summa**, **Finanšu dimensijas**, **Valūta** un **Darbības tips**. Turklāt nevarēsit pievienot vai dzēst žurnāla ierakstu rindas jebkurās Pamatlīdzekļu izlaižot žurnāla ierakstos, jo tas var izraisīt novirzes starp grafikiem un darbībām.

    > [!NOTE]
    > Ja parametrs **Maksāt kreditoram** ir izslēgts, maksājumu žurnāla ieraksti tiks uzskaitīti nomas grāmatas lapā **Līdzekļa noma**, un sistēma izveidos līdzekļa nomas ierakstu, nevis rēķinu. Nomas maksājuma ieraksts tiks grāmatots žurnālā ar nosaukumu, kas norādīts laukā **Ikmēneša nomas žurnāls**.

6. Kad darījums ir iegrāmatots, varat skatīt informāciju par darījumu un nomas saistību uzskaites vērtību, nomas grāmatā atlasot **Saistību darījumi**.

    Maksājumu grafikā būs atlasīta izvēles rūtiņa **Žurnāls grāmatots**, un rindā tiks parādīts rēķinu žurnāla numurs. Pēc tam, kad ir izveidots maksājumu žurnāls un ieraksts šim žurnālam, ieraksts ir jāanulē, pirms to var izveidot atkārtoti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
