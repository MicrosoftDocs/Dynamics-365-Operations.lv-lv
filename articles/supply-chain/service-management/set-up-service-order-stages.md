---
title: Iestatīt pakalpojuma pasūtījumu posmus
description: Iestatiet pakalpojuma pasūtījuma stadijas.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9774d5f4e97d3f768366ba552e5928929bacf508
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470933"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="6ccd8-103">Iestatīt pakalpojuma pasūtījumu posmus</span><span class="sxs-lookup"><span data-stu-id="6ccd8-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="6ccd8-104">Dodieties uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu pasūtījumi** \> **Pakalpojumu stadijas**.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="6ccd8-105">Atlasiet **Jauns**, lai izveidotu jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="6ccd8-106">Laukā **Pakalpojuma stadija** un **Apraksts** norādiet pakalpojuma stadijas ID un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="6ccd8-107">Atlasiet attiecīgajai stadijai atbilstošos parametrus.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="6ccd8-108">Atlasiet pašreizējās stadijas pamata stadiju vai atstājiet lauku **Vecākelements** tukšu, ja stadiju iestatījumā šī stadija ir sākotnējā stadija.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6ccd8-109">Pēc stadijas saglabāšanas lauku <STRONG>Vecākelements</STRONG> vairs nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="6ccd8-110">Tā vietā varat dzēst šo ierakstu un izveidot to vēlreiz, norādot citu atlasi laukā <STRONG>Vecākelements</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="6ccd8-111">Turklāt lauks <STRONG>Vecākelements</STRONG> var būt tukšs tikai vienai stadijai.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="6ccd8-112">Tas nozīmē, ka ir atļauta tikai viena sākotnējā stadija.</span><span class="sxs-lookup"><span data-stu-id="6ccd8-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]