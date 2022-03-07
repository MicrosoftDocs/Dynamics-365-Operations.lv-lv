---
title: NF‑e pielāgoto sertifikātu validācija
description: Šajā tēmā sniegta informācija par NF-e pielāgota sertifikāta iespējošanu un izmantošanu.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755595"
---
# <a name="nf-e-custom-certificate-validation"></a>NF‑e pielāgoto sertifikātu validācija

[!include [banner](../includes/banner.md)]

**Servera autentifikācijas nolūka** rekvizīts no Brazīlijas saknes sertifikāta iestādes izsniegtajiem sertifikātiem pēc noklusējuma ir izslēgts un ir jāiespējo manuāli. Dažos gadījumos automātiskais sertifikāta atjauninājums var pārslēgt šo rekvizītu uz kā vairs neiespējojamu. Ja tā notiek, TLS savienojums tiek ietekmēts, un tas vairs nav uzticams. Ir ietekmēta arī spēja izdot Brazīlijas elektronisko finanšu dokumenta modeli 55 (NF-e) ražošanas vidēs Minasžeraisas (MG) un Paranas (PR) štatos.

Lai iespējotu labojumu **NF-e-pielāgoto sertifikātu validēšanai**, pārejiet uz sadaļu **Līdzekļu pārvaldība**. Šī funkcija ļauj alternatīvu risinājumu V5 un V10 sertifikāta validācijām un ļauj izveidot uzticamu savienojumu ar tīmekļa pakalpojumiem, kas ir nepieciešams NF-e drošai pārsūtīšanai un autorizācijas saņemšanai no SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
