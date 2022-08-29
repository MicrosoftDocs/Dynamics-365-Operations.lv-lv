---
title: Izveidot tiešsaistes funkcionalitātes profilu
description: Šajā rakstā ir aprakstīts, kā izveidot tiešsaistes funkcionalitātes profilu Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5ce81900cd0648132748167d03906afc64e97f25
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276806"
---
# <a name="create-an-online-functionality-profile"></a>Izveidot tiešsaistes funkcionalitātes profilu

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskats par tiešsaistes funkcionalitātes profila iestatīšanu Microsoft Dynamics 365 Commerce.

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
  
![Tiešsaistes funkcionalitātes profila piemērs.](media/online-functionality-profile.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
