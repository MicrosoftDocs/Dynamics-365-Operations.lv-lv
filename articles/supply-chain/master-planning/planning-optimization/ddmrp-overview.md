---
title: Pieprasījumam noteiktu materiālu prasību plānošanas (DDMRP) pārskats
description: Šajā rakstā ir sniegta informācija par uz pieprasījumu orientētu materiālu prasību plānošanu (DDMRP), plānošanas metodoloģija, kas ir balstīta uz piedāvājuma un pieprasījuma dekompozīcijas.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 31b45fdb92cf8a590ff77104f0c8015fb4d329d5
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689493"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Pieprasījumam noteiktu materiālu prasību plānošanas (DDMRP) pārskats

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Gados uzņēmumi ir izmantojis materiālu prasību plānošanu (MRP) kā sistēmu materiālu un komponentu aprēķināšanai, kas nepieciešami preces ražošanai. Tomēr piegādes ķēdes tagad ir mainījušās. Daļām ir garāki izpildes laiki, jo tās ir no aizjūras valstīm iegūtās reizes. Tāpēc daudzi uzņēmumi ir ziņojuši, ka pārāk bieži ir iztjuši krājumi vai krājumi, jo nav zināms, cik daudz krājumu ir noliktavā. Pastāv arī vairākas tirgus svārstības (dažreiz neprecīzi prognozi), un debitori pieprasa preces īsu izpildes laiku. Tādēļ visā pasaulē ir piegādes ķēdes iztrūkums. Turklāt MRP rīki parasti nozīmē, ka plānotāji veic tūkstošiem darbību. Tāpēc ir grūti zināt, uz ko fokuss ir jāfokusē. Bieži daudzu šo jautājumu risinājums ir pārslēgties uz uz pieprasījumu orientētu materiālu prasību plānošanu (DDMRP).

DDMRP ir plānošanas metodoloģija, kas ir balstīta uz piedāvājuma un pieprasījuma atšifrēšanu. Šo atšifrēšanu var sasniegt, iestatot dekompozīcijas punktu elementus. Šiem krājumiem buferi tiek uzturēti, lai nodrošinātu pareizu krājumu daudzumu. Piedāvājuma un pieprasījuma atšifrēšana palīdz novērst "piegādes ietekmi", jo novirzes nav pagājusi ķēdē. *(neapstrādātā ietekme* attiecas uz to, kā neliela pieprasījuma svārstības mazumtirdzniecības līmenī var radīt progresīvi lielākas pieprasījuma svārstības vairumtirdzniecības, izplatītāja, ražotāja un izejmateriālu piegādātāju līmeņos.) Katrs buferis ir paredzēts, lai nosegtu daļas vidējo izmantojumu, un to var arī pielāgot, lai nosegtu pieprasījuma steks.

DDMRP ir bijis vērtīgs plānošanas metodoloģija mainīgajām vidēm, kurās debitoru tolerances laiki ir īsāki par kopīgo izpildes laiku.

## <a name="the-five-components-of-ddmrp"></a>Pieci DDMRP komponenti

DDMRP ir pieci secīgi komponenti (soļi). Pirmie trīs komponenti pamatā nosaka pieprasījumam paredzētas materiālu prasību plānošanas modeļa sākotnējo un sarežģīto konfigurāciju. Pēdējie divi komponenti nosaka metodoloģijas ikdienas darbību.

1. **[Stratēģisko krājumu pozicionēšana](ddmrp-inventory-positioning.md)** – identificējiet dekompozīcijas punktus piegādes ķēdes tīklā. Atšifrēšanas punkti ir noteikti jūsu piegādes ķēdes punkti, kur jūs ievietosiet krājumu buferi, ko pārraudzīsiet un papildināsiet.
2. **[Bufera profili](ddmrp-buffer-profile-and-levels.md)** un līmeņi – katram dekompozīcijas punktam identificējiet bufera izmērus (minimālo daudzumu, maksimālo daudzumu un pārkārtošanas punktu) un atkārtota pasūtījuma daudzumu.
3. **[Dinamiskā bufera](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** korekcijas - pielāgojiet bufera līmeņus, pamatojoties uz dažādiem darbības parametriem vai plānotiem nākotnes notikumiem.
4. **[Uz pieprasījumu balstīta plānošana](ddmrp-planning.md)** - izveidojiet piedāvājuma pasūtījumus pēc pieprasījuma. Šie piegādes pasūtījumi ietver ražošanas pasūtījumus, pirkšanas pasūtījumus un krājumu pārsūtīšanas pasūtījumus
5. **[Ļoti laba un redzama izpilde](ddmrp-visual-and-collaborative-execution.md)** – izpildiet piegādes pasūtījumus ar vizualizēšanas palīdzību.

Parasti DDMRP izmanto ražotāji, kuriem ir vairāklīmeņu materiālu komplekts (MK). Tomēr to var lietot arī izplatīšanas un mazumtirdzniecības tīkliem.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP šādā vietā: Dynamics 365 Supply Chain Management

DDMRP ir iekļauts Microsoft, Dynamics 365 Supply Chain Management un tam nav nepieciešamas papildu licences maksas. Piegādes ķēdes pārvaldībā DDMRP funkcionalitāte ir pievienota esošajam vispārējās plānošanas **modulim**. Tomēr ir nepieciešams, lai jūs lietotu plānošanas optimizācijas pievienojumprogrammu. 

DDMRP ir integrēts ar esošajiem plānošanas iestatījumiem Piegādes ķēžu pārvaldībā un tiek izmantots kopā ar šiem iestatījumiem, lai iegūtu pareizu plānošanas konfigurāciju jūsu biznesam. To kontrolē jauns vajadzību kods, kas pilnīgi atšķiras no perioda, min/maks., vajadzības utt. Tas nav jauns modulis, un tas neaizstāj esošo plānošanas funkcionalitāti. Tomēr tas sniedz vairāk funkcionalitātes lietošanai.
