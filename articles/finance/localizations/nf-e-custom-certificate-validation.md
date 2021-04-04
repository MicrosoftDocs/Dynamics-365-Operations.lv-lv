---
title: NF‑e pielāgoto sertifikātu validācija
description: Šajā tēmā sniegta informācija par NF-e pielāgota sertifikāta iespējošanu un izmantošanu.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240583"
---
# <a name="nf-e-custom-certificate-validation"></a>NF‑e pielāgoto sertifikātu validācija

[!include [banner](../includes/banner.md)]

Ieslēdzot NF-e pielāgoto sertifikātu verifikācijas līdzekli, pielāgota validācija ļauj izveidot savienojumu ar tīmekļa pakalpojumiem. Šis savienojums ir nepieciešams, lai pārsūtītu NF-e un saņemtu autorizāciju no SEFAZ.

Rekvizītu **Servera autentifikācijas nolūks** no V5 sertifikāta izsniedz Brazīlijas maršruta sertificēšanas iestāde. Šis rekvizīts ir izslēgts pēc noklusējuma, un tas ir jāiespējo manuāli. Dažos gadījumos automātiskais sertifikāta atjauninājums var pārslēgt šo rekvizītu uz kā vairs neiespējojamu. Ja tā notiek, TLS savienojums tiek ietekmēts, un tas vairs nav uzticams. Ir ietekmēta arī spēja izdot NF-e ražošanas vidēs Minasžeraisas (MG) un Paranas (PR) štatos.

Šis atjauninājums pieļauj alternatīvu sertifikātu validācijas risinājumu, kas nozīmē, ka ir iespējams izveidot drošus sakarus.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]