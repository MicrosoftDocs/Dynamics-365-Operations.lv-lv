---
title: Pakalpojuma līmenis un apraksts
description: Šajā tēmā ir paskaidrots pakalpojuma līmenis un tā apraksts Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 32e6dd6ba7291e8ea1cb78eeed2d8e2fcec0f6dd3cbd039336be0169730101ba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758692"
---
# <a name="service-level-and-description"></a>Pakalpojuma līmenis un apraksts

[!include [banner](../../includes/banner.md)]

 

Kad izveidojat darba pasūtījumu, iespējams, vēlaties tam definēt pakalpojumu līmeņus un pievienot vispārīgu aprakstu. Varat izveidot darba pasūtījuma pakalpojumu līmeņus lapā **Darba pasūtījuma pakalpojumu līmeņi** un aprakstus lapā **Darba pasūtījuma apraksts**.

## <a name="create-a-service-level"></a>Pakalpojuma līmeņa izveide

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Pakalpojuma līmenis**.
2. Atlasiet **Jauns**.
3. Laukā **Pakalpojuma līmenis** ievadiet pakalpojuma līmeni (piemēram, numuru).
4. Laukā **Nosaukums** ievadiet nosaukumu.

    Kopsavilkuma cilnē **Darba pasūtījumi** varat definēt paredzamo sākuma un beigu datumu un laiku. Šīs kopsavilkuma cilnes lauki definē periodu, kad darba pasūtījumi ir jāsāk un kad tiem ir jābeidzas. Tie tiek izmantoti manuāli izveidotiem darba pasūtījumiem un darba pasūtījumiem, kas tiek izveidoti, pamatojoties uz uzturēšanas pieprasījumiem. 

5. Laukā **Sākuma diena** ievadiet dienu skaitu, lai definētu periodu, kurā jāsākas darba pasūtījumam. Dienu skaits tiek aprēķināts no darba pasūtījuma izveides datuma. Piemēram, ja darba pasūtījums jāsāk uzreiz pēc tā izveides, ievadiet **0**. Ja darba pasūtījums jāsāk vienas nedēļas laikā pēc tā izveides, ievadiet **7**.
6. Lai darba pasūtījumam iestatītu sākuma laiku, papildus sākuma datumam iestatiet opciju **Iestatīt sākuma laiku** uz **Jā**. Pēc tam laukā **Sākuma laiks** ievadiet sākuma laiku. Ja opcija ir iestatīta uz **Nē**, tiek izmantots pašreizējās dienas laiks.
7. Laukā **Beigu diena** ievadiet dienu skaitu, lai definētu periodu, kurā jāpabeidz darba pasūtījums. Dienu skaits tiek aprēķināts no darba pasūtījuma sākšanas datuma. Piemēram, ja darba pasūtījums ir jāpabeidz vienas nedēļas laikā kopš tā sākuma datuma, ievadiet **7**.
8. Lai darba pasūtījumam iestatītu beigu, laiku papildus beigu datumam iestatiet opciju **Iestatīt beigu laiku** uz **Jā**. Pēc tam laukā **Beigu laiks** ievadiet beigu laiku. Ja opcija ir iestatīta uz **Nē**, tiek izmantots pašreizējās dienas laiks.
9. Atlasiet **Saglabāt**.

![Darba pasūtījumu pakalpojuma līmeņa lapa.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Izveidot aprakstu

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Apraksti**.
2. Atlasiet **Jauns**.
3. Laukā **Apraksts** ievadiet aprakstu.
4. Atlasiet **Saglabāt**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]