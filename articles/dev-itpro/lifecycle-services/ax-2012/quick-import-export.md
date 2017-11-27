---
title: "Ātrās importēšanas/eksportēšanas lietošana"
description: "Ātrās importēšanas un eksportēšanas mērķis ir ļaut jums veikt importēšanu un eksportēšanu tikai ar dažām darbībām."
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 14b4a56a229a2e1eb15c29eb7a89a89ac31e58db
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a><span data-ttu-id="f3937-103">Palaidiet Dynamics AX (AX 2012) paredzēto testēšanas datu pārsūtīšanas rīku (beta versiju)</span><span class="sxs-lookup"><span data-stu-id="f3937-103">Run the Test Data Transfer Tool (beta) for Dynamics AX (AX 2012)</span></span>

[!include[banner](../../includes/banner.md)]


<span data-ttu-id="f3937-104">Ātrās importēšanas un eksportēšanas mērķis ir ļaut jums veikt importēšanu un eksportēšanu tikai ar dažām darbībām.</span><span class="sxs-lookup"><span data-stu-id="f3937-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="f3937-105">Esam pievienojuši līdzekli Ātrā importēšana un eksportēšana, lai lietotājiem ļautu importēt vai eksportēt vienkāršus darbus, kurus lietotāji vēlas ātri izpildīt.</span><span class="sxs-lookup"><span data-stu-id="f3937-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="f3937-106">Ideālā gadījumā šis līdzeklis tiek lietots scenārijos, kur fails automātiski kartē uz sistēmu un lietotājam nav nepieciešams veikt detalizētu kartēšanu vai izveidot atkārtotus importēšanas vai eksportēšanas darbus.</span><span class="sxs-lookup"><span data-stu-id="f3937-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

-   <span data-ttu-id="f3937-107">Šis līdzeklis atbalsta strādāšanu gan ar standarta, gan ar pielāgotajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="f3937-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
-   <span data-ttu-id="f3937-108">Varat importēt no failiem un — ja izmantojat ODBC datu avotu — varat atlasīt kādu vaicājumu, ko izmantot sava importa definēšanai.</span><span class="sxs-lookup"><span data-stu-id="f3937-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
-   <span data-ttu-id="f3937-109">Jums ir nepieciešami jau iepriekš definēti avota datu formāti elementiem AX vai Fails, un jums ir jāzina, kur tie atrodas.</span><span class="sxs-lookup"><span data-stu-id="f3937-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
-   <span data-ttu-id="f3937-110">Lai izmantotu ātro importēšanu/eksportēšanu, jums nav nepieciešams izveidot apstrādes grupu — sistēma tādu izveidos automātiski, kad izpildīs importēšanas vai eksportēšanas darbu.</span><span class="sxs-lookup"><span data-stu-id="f3937-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="f3937-111">Tāpat varat arī norādīt, lai tiktu saglabāta ar ātro importēšanu/eksportēšanu importēto datu vēsture.</span><span class="sxs-lookup"><span data-stu-id="f3937-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="f3937-112">Ņemiet vērā, ka ātrā importēšana un eksportēšana pieņem, ka jūs pārzināt DIXF jēdzienus.</span><span class="sxs-lookup"><span data-stu-id="f3937-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>




