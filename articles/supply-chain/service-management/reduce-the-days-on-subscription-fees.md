---
title: Abonementa apmaksas dienu samazināšana
description: Lai samazinātu esošas abonementa maksas dienu skaitu, varat izveidot jaunu darījumu, kurā tiek noņemts laika periods, kas vairs nebūs abonementa maksas intervāla daļa.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370722d5c2f66e316d7c37f711cdd086bc53f6a8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014827"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Abonementa apmaksas dienu samazināšana 

[!include [banner](../includes/banner.md)]


Lai samazinātu esošas abonementa maksas dienu skaitu, varat izveidot jaunu darījumu, kurā tiek noņemts laika periods, kas vairs nebūs abonementa maksas intervāla daļa.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Samazināt dienu skaitu abonementa maksā

1.  Noklikšķiniet **uz Pakalpojumu** \> **pārvaldības pakalpojumu abonementi** \> **visi pakalpojumu abonementi**. Atlasiet pakalpojuma abonementu un darbību rūtī noklikšķiniet uz **Abonēšanas maksas**.

2.  Laukā **Abonementa tips** atlasiet **Dienu skaita samazināšana**.

3.  Izmantojiet lauku **Sākuma datums** un lauku **Beigu datums**, lai definētu abonementa maksas datumu intervālu, ko vēlaties noņemt no abonementa maksas perioda, pēc tam noklikšķiniet uz **Labi**.

Lai apskatītu izveidoto darbību, veidlapā **Abonements** noklikšķiniet uz **Apmaksas darbības**.

## <a name="example"></a>Paraugs

Ja abonementa darbību periods ir no 1. janvāra līdz 31. janvārim un vēlaties samazināt periodu par 10 dienām, izveidojiet jaunu darbību, kurā samazināšanas periods ir no 1. līdz 10. janvārim. (Samazināšanas periods varētu būt arī no 5. līdz 15. janvārim vai jebkurš cits desmit dienu periods).

Turklāt, ja samazinājuma periodā **Sākuma datums** ir 21. janvāris (31 mīnus 10), varat iestatīt **Beigu datumu** jebkurā datumā pēc 31. janvāra un 10 dienas tik un tā tiks atņemtas no apmaksas darbības perioda.

## <a name="see-also"></a>Skatiet arī

[Piemērs dienu skaita samazināšanai](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]