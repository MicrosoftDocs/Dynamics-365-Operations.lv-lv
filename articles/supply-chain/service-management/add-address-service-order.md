---
title: Adreses pievienošana pakalpojuma pasūtījumam
description: Šajā tēmā aprakstīts, kā pievienot debitora adresi pakalpojuma pasūtījumam.
author: ShylaThompson
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a54ec439fc88dc9688bbb3d6b833b5d80482f024
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824658"
---
# <a name="add-an-address-to-a-service-order"></a>Adreses pievienošana pakalpojuma pasūtījumam    

[!include [banner](../includes/banner.md)]


Šajā tēmā aprakstīts, kā pievienot debitora adresi pakalpojuma pasūtījumam. Kad tiek veidots pakalpojuma pasūtījums, adresāta informācija tiek pārsūtīta no projekta, kuram šis pakalpojuma pasūtījums ir piesaistīts. Taču jūs varat atlasīt citu atrašanās vietu, izvēloties kādu no adresēm, kas jau ir ievadītas programmā Microsoft Dynamics AX debitoriem, kreditoriem, vietām, noliktavām, pakalpojumu pasūtījumiem un projektiem.

Varat arī izveidot jaunu adresi. Pēc noklusējuma jaunā adrese tiek pārsūtīta uz projektu. Tomēr var norādīt, ka jaunā adrese ir derīga tikai šai pakalpojuma instancei. Šajā gadījumā jaunā adrese netiek pārsūtīta uz projektu.

## <a name="create-a-customer-address-for-a-service-order"></a>Debitora adreses izveidošana pakalpojuma pasūtījumam

Lai pievienotu adresi pakalpojuma pasūtījumam, rīkojieties šādi:

1.  Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.

2.  Atveriet pakalpojuma pasūtījumu, kuram vēlaties izveidot adresi.

3.  **Darbību rūtī** noklikšķiniet uz **Rediģēt** un pēc tam noklikšķiniet uz **Virsraksta skatījums**.

4.  Kopsavilkuma cilnē **Adrese** noklikšķiniet uz **Pievienot adresi**.

5.  Veidlapā **Jauna adrese** ievadiet unikālu adreses nosaukumu un aizpildiet atlikušos laukus. 
    

    > [!WARNING]
    > <P>Ja ievadāt tādu pašu nosaukumu kā esošai adresei, atlikušajos laukos ievadītā informācija pārrakstīs esošās adreses informāciju.</P>


6.  Noklikšķiniet uz **Labi**, lai kopētu jaunu adresi uz pakalpojuma pasūtījumu.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Alternatīvās adreses noteikšana pakalpojuma pasūtījumā

Lai pievienotu alternatīvu adresi pakalpojuma pasūtījumam, rīkojieties šādi:

1.  Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.

2.  Atveriet pakalpojuma pasūtījumu, kuram vēlaties ievadīt alternatīvo adresi.

3.  **Darbību rūtī** noklikšķiniet uz **Rediģēt** un pēc tam noklikšķiniet uz **Virsraksta skatījums**.

4.  Kopsavilkuma cilnē **Adrese** noklikšķiniet uz **Cita adrese**.

5.  Veidlapā **Adreses atlase** laukā **Ieraksta tips** atlasiet **Pakalpojuma pasūtījumi**.

6.  Atlasiet adresi un pēc tam noklikšķiniet uz **Labi**, lai to kopētu uz pakalpojuma pasūtījumu.


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]