---
title: Iestatīt pakalpojuma pasūtījumu posmus
description: Iestatiet pakalpojuma pasūtījuma stadijas.
author: ShylaThompson
ms.date: 05/07/2018
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
ms.openlocfilehash: 4b6e245b351b66724eedf8e0d1a0ebf0202df857
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824418"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="637af-103">Iestatīt pakalpojuma pasūtījumu posmus</span><span class="sxs-lookup"><span data-stu-id="637af-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="637af-104">Dodieties uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu pasūtījumi** \> **Pakalpojumu stadijas**.</span><span class="sxs-lookup"><span data-stu-id="637af-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="637af-105">Atlasiet **Jauns**, lai izveidotu jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="637af-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="637af-106">Laukā **Pakalpojuma stadija** un **Apraksts** norādiet pakalpojuma stadijas ID un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="637af-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="637af-107">Atlasiet attiecīgajai stadijai atbilstošos parametrus.</span><span class="sxs-lookup"><span data-stu-id="637af-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="637af-108">Atlasiet pašreizējās stadijas pamata stadiju vai atstājiet lauku **Vecākelements** tukšu, ja stadiju iestatījumā šī stadija ir sākotnējā stadija.</span><span class="sxs-lookup"><span data-stu-id="637af-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="637af-109">Pēc stadijas saglabāšanas lauku <STRONG>Vecākelements</STRONG> vairs nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="637af-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="637af-110">Tā vietā varat dzēst šo ierakstu un izveidot to vēlreiz, norādot citu atlasi laukā <STRONG>Vecākelements</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="637af-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="637af-111">Turklāt lauks <STRONG>Vecākelements</STRONG> var būt tukšs tikai vienai stadijai.</span><span class="sxs-lookup"><span data-stu-id="637af-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="637af-112">Tas nozīmē, ka ir atļauta tikai viena sākotnējā stadija.</span><span class="sxs-lookup"><span data-stu-id="637af-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]