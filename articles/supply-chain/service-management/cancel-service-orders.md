---
title: Pakalpojumu pasūtījumu atcelšana
description: Pakalpojuma pasūtījumu vai pakalpojuma pasūtījuma rindu ir iespējams dzēst no paša pakalpojuma pasūtījuma vai arī atcelt vairākus pakalpojumu pasūtījumus veicot periodisko uzdevumu.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e75ed6e30ece1f4807ff036d831c269774d941a7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670977"
---
# <a name="cancel-service-orders"></a>Pakalpojumu pasūtījumu atcelšana   

[!include [banner](../includes/banner.md)]


Pakalpojuma pasūtījumu vai pakalpojuma pasūtījuma rindu ir iespējams dzēst no paša pakalpojuma pasūtījuma vai arī atcelt vairākus pakalpojumu pasūtījumus veicot periodisko uzdevumu.


> [!NOTE]
> <P>Pakalpojumu pasūtījumus nav iespējams atcelt, ja pakalpojuma pasūtījuma posms neļauj atcelšanu, ja pakalpojuma pasūtījumam ir krājuma vajadzības, vai arī ja pakalpojuma pasūtījums jau ir ticis iegrāmatots.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Pakalpojuma pasūtījuma atcelšana formā Pakalpojumu pasūtījumi

1.  Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**. Atlasiet pakalpojuma pasūtījumu un pēc tam noklikšķiniet uz **Atcelt pasūtījumu** darbību rūtī.

## <a name="cancel-a-service-order-line"></a>Pakalpojuma pasūtījuma rindas atcelšana

1.  Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**. Veiciet dubultklikšķi uz pakalpojuma pasūtījumu, kas satur rindu, kuru vēlaties atcelt.

2.  Atlasiet pakalpojuma pasūtījuma rindu, kuru vēlaties atcelt, un pēc tam noklikšķiniet uz **Atcelt pasūtījuma rindu**, lai mainītu rindas statusu uz **Atcelta**.


> [!TIP]
> <P>Lai atsauktu pakalpojuma pasūtījuma rindas atcelšanu un mainītu statusu atpakaļ uz <STRONG>Izveidota</STRONG>, noklikšķiniet uz <STRONG>Atsaukt atcelšanu</STRONG>.</P>


## <a name="cancel-multiple-service-orders"></a>Vairāku pakalpojuma pasūtījumu atcelšana

1.  Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Periodiskie** \> **Pakalpojuma pasūtījumi** \> **Atcelt pakalpojuma pasūtījumus**.

2.  Noklikšķiniet uz pogas **Atlasīt**.

3.  Veidlapā **Pieprasījums** slejā **Kritēriji** atlasiet pakalpojumu pasūtījumus, kurus vēlaties atcelt.

4.  Klikšķiniet **Labi**, lai aizvērtu veidlapu **Pieprasījums**.

5.  Atlasiet izvēles rūtiņu **Rādīt informācijas žurnālu**, lai izveidotu informācijas žurnālu, kas parāda atceltos pakalpojuma pasūtījumus.

6.  Atlasiet izvēles rūtiņu **Atsaukt atcelšanu**, ja pakalpojuma pasūtījumu vēlaties atkal statusā **Atcelts**.

7.  Noklikšķiniet uz **Labi**.

Atlasītie pakalpojumu pasūtījumi tiek atcelti vai arī to progresa statuss tiek mainīts atpakaļ no **Atcelts** uz **Procesā**.


> [!NOTE]
> <P>Ja ir tikusi atlasīta izvēles rūtiņa <STRONG>Atsaukt atcelšanu</STRONG>, pakalpojuma pasūtījumi ar progresa statusu <STRONG>Atcelts</STRONG> tiek mainīti atpakaļ un nenotiek pakalpojuma pasūtījumu atcelšana ar progresa statusu <STRONG>Procesā</STRONG>.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]