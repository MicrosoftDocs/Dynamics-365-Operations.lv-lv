---
title: Izveidot tiešsaistes funkcionalitātes profilu
description: Šajā tēmā aprakstīts, kā izveidot tiešsaistes funkcionalitātes profilu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414172"
---
# <a name="create-an-online-functionality-profile"></a>Izveidot tiešsaistes funkcionalitātes profilu


[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par tiešsaistes funkcionalitātes profila iestatīšanu programmai Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Tiešsaistes funkcionalitātes profilā ir sniegti dažādi tiešsaistes kanāliem izmantotie iestatījumi. Katram tiešsaistes kanālam jānorāda tiešsaistes funkcionalitātes profils.

## <a name="create-an-online-functionality-profile"></a>Izveidot tiešsaistes funkcionalitātes profilu

Šī procedūra izskaidro, kā izveidot tiešsaistes funkcionalitātes profilu programmā Commerce Headquarters.

1. Navigācijas rūtī atveriet **Moduļi \> Kanāla iestatīšana \> Tiešsaistes veikala iestatīšana \> Funkcionalitātes profili**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Profils** ievadiet profila ID.
1. Laukā **Apraksts** ievadiet vērtību ("Adventure Works profilu" piemērā zemāk esošajā attēlā).
1. Sadaļā **Funkcijas** pēc nepieciešamības modificējiet iestatījumus **GROZS**, **MAZUMTIRDZNIECĪBAS KLIENTI** vai **IZRAKSTĪŠANĀS**.
1. Darbību rūtī atlasiet **Saglabāt**.

Šajā attēlā ir parādīts tiešsaistes funkcionalitātes piemērs.
  
![Tiešsaistes funkcionalitātes profila piemērs](media/online-functionality-profile.png)

## <a name="functions"></a>Funkcijas

- **Apkopot preces**: Ja aktivizēta, šī funkcija ļauj grozam atjaunināt daudzumu, kad viens un tas pats krājums tiek pievienots vairākkārt.
- **Atļaut izrakstīšanos bez maksājumiem**: Ja aktivizēta, šī funkcija apstrādā scenāriju, kad grozam pievienotajām precēm ir cena $0.00.
- **Izveidot debitoru async režīmā**: Šis ir mantojuma iestatījums, kas piemērojams trešās puses e-komercijas kanāliem, un tas neattiecas uz Dynamics 365 e-commerce vietni.

## <a name="additional-resources"></a>Papildu resursi

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Tiešsaistes veikala iestatīšana](channel-setup-online.md)

[Mazumtirdzniecības kanāla iestatīšana](channel-setup-retail.md)

[Zvanu centra kanāla iestatīšana](channel-setup-callcenter.md)
