---
title: Transportēšanas pārvaldības papildmaksas
description: Šajā tēmā ir paskaidrots, kā transportēšanas izveidotajām maksām jābūt saistītām ar maksas kodu.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 4f58db216176832d61bdafbe43831ededd3dd6dc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233419"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="2830e-103">Transportēšanas pārvaldības papildmaksas</span><span class="sxs-lookup"><span data-stu-id="2830e-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2830e-104">Kas attiecas uz visām papildizmaksām, transportēšanas izveidotajām maksām jābūt saistītām ar maksas kodu.</span><span class="sxs-lookup"><span data-stu-id="2830e-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="2830e-105">Pretējā gadījumā tās netiks pievienotas pasūtījumam kā papildmaksa.</span><span class="sxs-lookup"><span data-stu-id="2830e-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="2830e-106">**Izmaksu kods** nosaka, kā maksa tiek uzskaitīta saistībā ar pasūtījumu un pasūtījuma rindu, kur tā ir pievienota.</span><span class="sxs-lookup"><span data-stu-id="2830e-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="2830e-107">Dodieties uz **Transportēšanas pārvaldība > Iestatījumi > Novērtējums > Papildmaksas**, lai definētu kvalifikācijas kritērijus, kas nosaka, kad noteikts **Izmaksu kods** tiek piemērots maksai.</span><span class="sxs-lookup"><span data-stu-id="2830e-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="2830e-108">Katram attiecīgajam **Izmaksu moduļa** iestatījumam ir jābūt vismaz vienam iestatījumam (*Klients* un *Kreditors*), kur **Papildmaksu veids** ir iestatīts uz *Nav*.</span><span class="sxs-lookup"><span data-stu-id="2830e-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="2830e-109">Ja tā nav, papildmaksa *netiks* pievienota pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="2830e-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]