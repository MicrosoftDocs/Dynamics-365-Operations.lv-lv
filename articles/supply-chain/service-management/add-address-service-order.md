---
title: Adreses pievienošana pakalpojuma pasūtījumam
description: Šajā rakstā ir aprakstīts, kā pievienot debitora adresi pakalpojuma pasūtījumam.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015730"
---
# <a name="add-an-address-to-a-service-order"></a>Adreses pievienošana pakalpojuma pasūtījumam

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pievienot debitora adresi pakalpojuma pasūtījumam. Kad tiek veidots pakalpojuma pasūtījums, adresāta informācija tiek pārsūtīta no projekta, kuram šis pakalpojuma pasūtījums ir piesaistīts. Taču jūs varat atlasīt citu atrašanās vietu, izvēloties kādu no adresēm, kas jau ir ievadītas programmā Microsoft Dynamics AX debitoriem, kreditoriem, vietām, noliktavām, pakalpojumu pasūtījumiem un projektiem.

Varat arī izveidot jaunu adresi. Pēc noklusējuma jaunā adrese tiek pārsūtīta uz projektu. Tomēr var norādīt, ka jaunā adrese ir derīga tikai šai pakalpojuma instancei. Šajā gadījumā jaunā adrese netiek pārsūtīta uz projektu.

## <a name="create-a-customer-address-for-a-service-order"></a>Debitora adreses izveidošana pakalpojuma pasūtījumam

Lai pievienotu adresi pakalpojuma pasūtījumam, rīkojieties šādi:

1. Dodieties uz **Pakalpojumu pārvaldības** \> **Pakalpojumu pasūtījumi** \> **Pakalpojumu pasūtījumi**.

1. Atveriet pakalpojuma pasūtījumu, kuram vēlaties izveidot adresi.

1. Atveriet cilni **Virsraksts**.

1. Izvērsiet kopsavilkuma **cilni** Adrese un pēc tam FastTab **rīkjoslā** atlasiet Pievienot adresi.

1. Dialogā **Jauna adrese** ievadiet unikālu adreses nosaukumu un aizpildiet atlikušos laukus. 

    > [!WARNING]
    > Ja ievadāt tādu pašu nosaukumu kā esošai adresei, atlikušajos laukos ievadītā informācija pārrakstīs esošās adreses informāciju.

1. Atlasiet **Labi,** lai kopētu jauno adresi uz jūsu pakalpojuma pasūtījumu.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Alternatīvās adreses noteikšana pakalpojuma pasūtījumā

Lai pievienotu alternatīvu adresi pakalpojuma pasūtījumam, rīkojieties šādi:

1. Dodieties uz **Pakalpojumu pārvaldības** \> **Pakalpojumu pasūtījumi** \> **Pakalpojumu pasūtījumi**.

1. Atveriet pakalpojuma pasūtījumu, kuram vēlaties ievadīt alternatīvo adresi.

1. Atveriet cilni **Virsraksts**.

1. Izvērsiet kopsavilkuma **cilni** Adrese un pēc tam Kopsavilkuma **cilnē Kopsavilkuma cilnē** atlasiet Cita adrese.

1. **Adreses atlases** dialogā **atlasiet Pakalpojumu pasūtījumi** nolaižamajā sarakstā virs atzīmētā.

1. Atlasiet adresi un pēc tam atlasiet Labi, **lai** kopētu to uz pakalpojuma pasūtījumu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]