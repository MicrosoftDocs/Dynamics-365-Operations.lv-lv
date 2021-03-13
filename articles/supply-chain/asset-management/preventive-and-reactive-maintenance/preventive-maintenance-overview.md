---
title: Profilaktiskās uzturēšanas pārskats
description: Šajā tēmā ir paskaidrota profilaktiskā uzturēšana programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 36a70a3e60566fd8048ad404e0c391d898053a0a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016732"
---
# <a name="preventive-maintenance-overview"></a><span data-ttu-id="18e3a-103">Profilaktiskās uzturēšanas pārskats</span><span class="sxs-lookup"><span data-stu-id="18e3a-103">Preventive maintenance overview</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="18e3a-104">Šajā tēmā ir paskaidrota profilaktiskā uzturēšana programmā Asset Management.</span><span class="sxs-lookup"><span data-stu-id="18e3a-104">This topic explains preventive maintenance in Asset Management.</span></span> <span data-ttu-id="18e3a-105">Profilaktiskā uzturēšana ir disciplīna, kas ietver plānotos uzturēšanas darbus, piemēram, regulāru servisu, kalibrēšanu un pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="18e3a-105">Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections.</span></span> <span data-ttu-id="18e3a-106">Programmā **Asset Management** jūs varat izveidot uzturēšanas plānus un tos uzstādīt līdzekļiem un funkcionāliem novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="18e3a-106">In **Asset Management**, you can create maintenance plans and set them up on assets and functional locations.</span></span> <span data-ttu-id="18e3a-107">Jūs varat arī funkcionāliem novietojumiem uzstādīt uzturēšanas ciklus.</span><span class="sxs-lookup"><span data-stu-id="18e3a-107">You can also set up maintenance rounds on functional locations.</span></span> <span data-ttu-id="18e3a-108">Līdzekļu uzturēšanas plāni ir aktīvi neatkarīgi no tā, kur ir instalēts līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="18e3a-108">Maintenance plans on assets are active regardless of where the asset is installed.</span></span> <span data-ttu-id="18e3a-109">Funkcionālā novietojuma uzturēšanas plāni un uzturēšanas cikli ir aktīvi līdzekļiem, kuri ir patlaban instalēti novietojumā.</span><span class="sxs-lookup"><span data-stu-id="18e3a-109">Maintenance plans and maintenance rounds on functional location are active for the assets currently installed at the location.</span></span> <span data-ttu-id="18e3a-110">Tā vietā, lai uzstādītu uzturēšanas plānus līdzekļiem vai uzstādītu uzturēšanas ciklus funkcionāliem novietojumiem, jūs varat izveidot uzturēšanas ciklus, kuri ietver vairākus līdzekļus, kuriem jums ir jāveic saistīti uzturēšanas darbu tipi vienā un tajā pašā darba rutīnā.</span><span class="sxs-lookup"><span data-stu-id="18e3a-110">Instead of setting up maintenance plans on assets, or setting up maintenance rounds on functional locations, you can create maintenance rounds that include multiple assets on which you need to perform related types of maintenance jobs in the same work routine.</span></span> <span data-ttu-id="18e3a-111">No līdzekļiem izveidoti uzturēšanas cikli - atšķirībā no tādiem, kas izveidoti funkcionāliem novietojumiem - nozīmē to, ka jūs varat atlasīt vairākus līdzekļus vienam uzturēšanas ciklam, kurš nav instalēts vienā funkcionālajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="18e3a-111">Maintenance rounds created from assets - instead of created on functional locations - means that you can select a number of assets for one maintenance round, which are not installed on the same functional location.</span></span>

<span data-ttu-id="18e3a-112">Uzturēšanas plāni tiek izmantoti profilaktiskai un reaktīvai atsevišķu līdzekļu uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="18e3a-112">Maintenance plans are used for preventive and reactive maintenance on individual assets.</span></span> <span data-ttu-id="18e3a-113">Uzturēšanas cikli tiek izmantoti profilaktiskai un reaktīvai līdzekļu grupas vai kopas uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="18e3a-113">Maintenance rounds are used for preventive maintenance on a group or a set of assets.</span></span> <span data-ttu-id="18e3a-114">Uzturēšanas plāni un uzturēšanas cikli tiek izmantoti, lai ģenerētu darba pasūtījuma priekšlikumus.</span><span class="sxs-lookup"><span data-stu-id="18e3a-114">Maintenance plans and maintenance rounds are used for generating work order proposals.</span></span> <span data-ttu-id="18e3a-115">Darba pasūtījuma priekšlikumi tiek saglabāti kā uzturēšanas grafika rindas, kuras var saistīt un konvertēt darba pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="18e3a-115">The work order proposals are saved as maintenance schedule lines, which can be bundled and converted into work orders.</span></span>

<span data-ttu-id="18e3a-116">Nākamajā attēlā sniegts pārskats darba plūsmai no uzturēšanas plānu un uzturēšanas ciklu izveides līdz darba pasūtījumu izveidei līdzekļiem, pamatojoties uz šiem uzturēšanas plāniem un uzturēšanas cikliem.</span><span class="sxs-lookup"><span data-stu-id="18e3a-116">The following illustration provides an overview of the work flow from creating maintenance plans and maintenance rounds to creating work orders for assets, based on those maintenance plans and maintenance rounds.</span></span>

![1. attēls](media/01-preventive-maintenance.png)

