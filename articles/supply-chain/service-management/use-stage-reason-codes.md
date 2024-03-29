---
title: Stadiju iemeslu kodu izmantošana
description: Jāizmanto iemesla kods, lai norādītu, kādēļ pakalpojuma līmeņa līgums (SLA) ir atcelts vai kādēļ pakalpojuma pasūtījums ir pārsniedzis laika ierobežojumu, kas ir definēts SLA.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06c2b6a2b338dbfdbecdeb75e12fa1c20af8e56d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669521"
---
# <a name="use-stage-reason-codes"></a>Stadiju iemeslu kodu izmantošana 

[!include [banner](../includes/banner.md)]


Jāizmanto iemesla kods, lai norādītu, kādēļ pakalpojuma līmeņa līgums (SLA) ir atcelts vai kādēļ pakalpojuma pasūtījums ir pārsniedzis laika ierobežojumu, kas ir definēts SLA.

Varat arī norādīt, ka iemesla kods ir nepieciešams, ja SLA tiek atcelts vai ja laika ierobežojums pārsniedz laiku, kas pakalpojuma pasūtījumam norādīts SLA.

Ja ir norādīts, ka iemesla kods ir nepieciešams, iemesla kods ir jāievada tālāk minētajās situācijās:

  - Ja pakalpojuma pasūtījums tiek pārvietots uz stadiju, kur tiek apturēta laika ierakstīšana attiecībā uz pakalpojuma pasūtījuma SLA.

  - Kad pakalpojuma pasūtījums ir parakstīts.

  - Kad laika ierakstīšana tiek apturēta manuāli.

## <a name="set-up-reason-codes"></a>Iestatiet cēloņa kodus

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu pasūtījumi** \> **Posmu pamatojuma kodi**.

2.  Formā **Stadiju iemeslu kodi** noklikšķiniet uz **Jauns**, lai izveidotu jaunu iemesla kodu.

3.  Laukā **Stadijas iemesla kods** ievadiet unikālu stadijas iemesla kodu.

4.  Laukā **Apraksts** ievadiet stadijas iemesla koda aprakstu.

5.  Aizveriet formu, lai saglabātu izmaiņas.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Pieprasiet cēloņa kodus, ja pakalpojuma līmeņa juridiskais līgums ir atcelts.

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu pārvaldības parametri**.

2.  Formā **Pakalpojumu pārvaldības parametri** noklikšķiniet uz saites **Vispārīgi** un pēc tam atzīmējiet izvēles rūtiņu **Atcelšanas iemesla kods**.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Pieprasiet iemeslu kodus, ja pakalpojuma līmeņa līgumam iestatītais laika ierobežojums tiek pārsniegts

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu pārvaldības parametri**.

2.  Formā **Pakalpojumu pārvaldības parametri** noklikšķiniet uz saites **Vispārīgi** un pēc tam atzīmējiet izvēles rūtiņu **Laika pārsniegšanas iemesla kods**.

## <a name="see-also"></a>Skatiet arī

[Laika ierakstīšanas sākšana un apturēšana pakalpojuma pasūtījumam](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]