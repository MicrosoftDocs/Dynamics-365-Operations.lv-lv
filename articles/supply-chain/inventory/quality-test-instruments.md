---
title: Kvalitātes pārvaldības testa instrumenti
description: Šajā tēmā ir aprakstīts, kā izveidot testa instrumentus, ko var izmantot kvalitātes pārbaudes pasūtījumu testēšanai Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956745"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="6d5ba-103">Kvalitātes pārvaldības testa instrumenti</span><span class="sxs-lookup"><span data-stu-id="6d5ba-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d5ba-104">Šajā tēmā ir aprakstīts, kā izveidot testa instrumentus, ko var izmantot kvalitātes pārbaudes pasūtījumu testēšanai Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="6d5ba-105">Jūs izmantojat lapu **Testa instrumenti**, lai definētu un skatītu detalizētu informāciju par ierīcēm, kas tiek izmantotas testu veikšanai kvalitātes pārbaudes pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="6d5ba-106">Testa instrumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-106">Test instruments are optional.</span></span> <span data-ttu-id="6d5ba-107">Tomēr tie var palīdzēt kvalitātes darbiniekiem zināt, kuru ierīci vai rīku viņiem būtu jāizmanto, lai veiktu noteiktu testu.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="6d5ba-108">Piemērs par testa instrumentu</span><span class="sxs-lookup"><span data-stu-id="6d5ba-108">Test instrument example</span></span>

<span data-ttu-id="6d5ba-109">Jūs veicat dažādus testus elektriskajiem komponentiem.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="6d5ba-110">Daži testi attiecas uz sastāvdaļu spriegumu, viens tests – uz to temperatūru, un vēl viens – uz to svaru.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="6d5ba-111">Katra testa veikšanai tiek izmantoti dažādi rīki, ierīces vai aprīkojums.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="6d5ba-112">Piemēram, sprieguma mērītājs tiek izmantots, lai mērītu spriegumu, termometrs tiek izmantots temperatūras mērīšanai, un skalas izmanto, lai mērītu svaru.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="6d5ba-113">Jūs varat konfigurēt katru no šīm ierīcēm kā testa instrumentu un norādīt mērvienību, kurā jāieraksta testa rezultāti.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="6d5ba-114">Piemēram, rezultāti no sprieguma tiek ierakstīti voltos, rezultāti no termometra tiek ierakstīti Fārenheita grādos vai Celsija grādos, un skalas rezultāti tiek ierakstīti mārciņās vai kilogramos.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="6d5ba-115">Testa instrumenta izveide</span><span class="sxs-lookup"><span data-stu-id="6d5ba-115">Create a test instrument</span></span>

1. <span data-ttu-id="6d5ba-116">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Testa instrumenti**.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="6d5ba-117">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6d5ba-118">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="6d5ba-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6d5ba-119">**Testa instrumenti** – ievadiet unikālu ID vai nosaukumu testa instrumentam.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="6d5ba-120">**Apraksts** — ievadiet testa instrumenta detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="6d5ba-121">**Vienība** – atlasiet vienību, pēc kuras notiek instrumenta mērīšana.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="6d5ba-122">Lauks **Precizitāte** tiek iestatīts automātiski, pamatojoties uz jūsu atlasītu vienību.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="6d5ba-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6d5ba-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d5ba-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6d5ba-124">Additional resources</span></span>

- [<span data-ttu-id="6d5ba-125">Kvalitātes pārvaldības tests</span><span class="sxs-lookup"><span data-stu-id="6d5ba-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="6d5ba-126">Kvalitātes pārvaldības testa grupas</span><span class="sxs-lookup"><span data-stu-id="6d5ba-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
