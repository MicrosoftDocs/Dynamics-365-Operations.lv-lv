---
title: NF‑e pielāgoto sertifikātu validācija
description: Šajā rakstā ir sniegta informācija par NF-e pielāgotā sertifikāta iespējošanu un izmantošana.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288550"
---
# <a name="nf-e-custom-certificate-validation"></a>NF‑e pielāgoto sertifikātu validācija

[!include [banner](../includes/banner.md)]

**Servera autentifikācijas nolūka** rekvizīts no Brazīlijas saknes sertifikāta iestādes izsniegtajiem sertifikātiem pēc noklusējuma ir izslēgts un ir jāiespējo manuāli. Dažos gadījumos automātiskais sertifikāta atjauninājums var pārslēgt šo rekvizītu uz kā vairs neiespējojamu. Ja tā notiek, TLS savienojums tiek ietekmēts, un tas vairs nav uzticams. Ir ietekmēta arī spēja izdot Brazīlijas elektronisko finanšu dokumenta modeli 55 (NF-e) ražošanas vidēs Minasžeraisas (MG) un Paranas (PR) štatos.

Lai iespējotu labojumu **NF-e-pielāgoto sertifikātu validēšanai**, pārejiet uz sadaļu **Līdzekļu pārvaldība**. Šī funkcija ļauj alternatīvu risinājumu V5 un V10 sertifikāta validācijām un ļauj izveidot uzticamu savienojumu ar tīmekļa pakalpojumiem, kas ir nepieciešams NF-e drošai pārsūtīšanai un autorizācijas saņemšanai no SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
