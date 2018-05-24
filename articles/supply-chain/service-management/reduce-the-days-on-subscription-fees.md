---
title: "Abonementa apmaksas dienu samazināšana"
description: "Lai samazinātu esošas abonementa maksas dienu skaitu, varat izveidot jaunu darījumu, kurā tiek noņemts laika periods, kas vairs nebūs abonementa maksas intervāla daļa."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c70e393c125eecef85e8711d1635250f5ff408d9
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a>Abonementa apmaksas dienu samazināšana 

[!include [banner](../includes/banner.md)]


Lai samazinātu esošas abonementa maksas dienu skaitu, varat izveidot jaunu darījumu, kurā tiek noņemts laika periods, kas vairs nebūs abonementa maksas intervāla daļa.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Samazināt dienu skaitu abonementa maksā

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu abonementi** \> **Visi pakalpojumu abonementi**. Atlasiet pakalpojuma abonementu un darbību rūtī noklikšķiniet uz **Abonēšanas maksas**.

2.  Laukā **Abonementa tips** atlasiet **Dienu skaita samazināšana**.

3.  Izmantojiet lauku **Sākuma datums** un lauku **Beigu datums**, lai definētu abonementa maksas datumu intervālu, ko vēlaties noņemt no abonementa maksas perioda, pēc tam noklikšķiniet uz **Labi**.

Lai apskatītu izveidoto darbību, veidlapā **Abonements** noklikšķiniet uz **Apmaksas darbības**.

## <a name="example"></a>Paraugs

Ja abonementa darbību periods ir no 1. janvāra līdz 31. janvārim un vēlaties samazināt periodu par 10 dienām, izveidojiet jaunu darbību, kurā samazināšanas periods ir no 1. līdz 10. janvārim. (Samazināšanas periods varētu būt arī no 5. līdz 15. janvārim vai jebkurš cits desmit dienu periods).

Turklāt, ja samazinājuma periodā **Sākuma datums** ir 21. janvāris (31 mīnus 10), varat iestatīt **Beigu datumu** jebkurā datumā pēc 31. janvāra un 10 dienas tik un tā tiks atņemtas no apmaksas darbības perioda.

## <a name="see-also"></a>Skatiet arī

[Piemērs dienu skaita samazināšanai](reduction-days-example.md)

  



