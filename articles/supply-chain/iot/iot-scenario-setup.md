---
title: IoT informācijas scenārija iestatīšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt IoT informācijas Supply Chain Management scenāriju.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386538"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="34a51-103">IoT informācijas scenārija iestatīšana</span><span class="sxs-lookup"><span data-stu-id="34a51-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34a51-104">Šajā tēmā ir aprakstīts, kā konfigurēt IoT informācijas Supply Chain Management scenāriju.</span><span class="sxs-lookup"><span data-stu-id="34a51-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="34a51-105">Pirms scenāriju iestatīšanas ir [jāiestata LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="34a51-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="34a51-106">Šajā tēmā jūs konfigurēsit scenāriju **Aprīkojuma dīkstāve**, lai izveidotu paziņojumu Supply Chain Management, kad iekārta netiek izmantota.</span><span class="sxs-lookup"><span data-stu-id="34a51-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="34a51-107">Konfigurēt scenāriju **Aprīkojuma dīkstāve** Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="34a51-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="34a51-108">Scenārijs **Aprīkojuma dīkstāve** kartē iekārtas brīdinājuma sliekšņa izslēgšanas signālu.</span><span class="sxs-lookup"><span data-stu-id="34a51-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="34a51-109">Iekārta tiek uzraudzīta tikai tad, ja iekārta ir izvēlēta scenārijam un ir iestatīta Supply Chain Management darbam.</span><span class="sxs-lookup"><span data-stu-id="34a51-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="34a51-110">Ja laiks, kas pagājis kopš iekārtas pēdējā saņemtā izslēgšanas signāla ir lielāks nekā brīdinājuma robežvērtība, tiek parādīts paziņojums **Iekārta dīkstāvē**.</span><span class="sxs-lookup"><span data-stu-id="34a51-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="34a51-111">Ja iekārta joprojām darbojas, kad tiek saņemts nākamais **PartOut** signāls, tiek parādīts paziņojums **Iekārta darbojas**.</span><span class="sxs-lookup"><span data-stu-id="34a51-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="34a51-112">Ja iekārta pārstāj darboties uz 30 min., tiek parādīts jauns paziņojums **Iekārta dīkstāvē**.</span><span class="sxs-lookup"><span data-stu-id="34a51-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="34a51-113">Scenārijam **Aprīkojuma dīkstāve** ir šādas atkarības:</span><span class="sxs-lookup"><span data-stu-id="34a51-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="34a51-114">Lai brīdinājums tiktu parādīts, ražošanas pasūtījumam ir jādarbojas kartētā iekārtā.</span><span class="sxs-lookup"><span data-stu-id="34a51-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="34a51-115">Uz IoT centrmezglu ar unikālu rekvizīta nosaukumu jānosūta signāls, kas apzīmē kartētās iekārtas izslēgšanas signālu.</span><span class="sxs-lookup"><span data-stu-id="34a51-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="34a51-116">IoT centrmezgla ziņojumā jābūt Unix milisekundes laikspiedola rekvizītam.</span><span class="sxs-lookup"><span data-stu-id="34a51-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="34a51-117">Lai konfigurētu scenāriju, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="34a51-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="34a51-118">Piesakieties Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="34a51-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="34a51-119">Iespējojiet IoT informācijas līdzekļa karodziņu.</span><span class="sxs-lookup"><span data-stu-id="34a51-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="34a51-120">Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="34a51-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="34a51-121">Konfigurējiet rādītājus.</span><span class="sxs-lookup"><span data-stu-id="34a51-121">Configure the metrics.</span></span> <span data-ttu-id="34a51-122">Papildinformāciju skatiet [Rādītāju konfigurēšana](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="34a51-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="34a51-123">Pārejiet uz **Ražošanas kontrole**.</span><span class="sxs-lookup"><span data-stu-id="34a51-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="34a51-124">Pārejiet uz **Iestatījumi \> IoT informācija \> Scenārija pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="34a51-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="34a51-125">Noklikšķiniet uz **Konfigurēt**, kas atrodas **Aprīkojuma dīkstāve** elementā.</span><span class="sxs-lookup"><span data-stu-id="34a51-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="34a51-126">Konfigurācijas vednis sākas ar lapu **Aprīkojuma sensora shēmas definīcija**.</span><span class="sxs-lookup"><span data-stu-id="34a51-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="34a51-127">Mērķis ir iestatīt shēmu Supply Chain Management, lai tā atbilstu IoT ziņojumu JSON formātam.</span><span class="sxs-lookup"><span data-stu-id="34a51-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="34a51-128">Var tikt definētas vairākas ziņojumu shēmas.</span><span class="sxs-lookup"><span data-stu-id="34a51-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="34a51-129">Papildinformāciju skatiet [Ziņojumu shēmas formāti IoT centrmezglam](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="34a51-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="34a51-130">Šajā piemērā ziņojuma lietderīgā slodze satur ziņojumu paketi ar šādu formātu:</span><span class="sxs-lookup"><span data-stu-id="34a51-130">In this example, the message payload contains a batch of messages with this format:</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="34a51-131">Pievienojiet tabulai rindu.</span><span class="sxs-lookup"><span data-stu-id="34a51-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="34a51-132">Iestatiet **Shēmas nosaukumu** uz **ID**.</span><span class="sxs-lookup"><span data-stu-id="34a51-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="34a51-133">Iestatiet **Shēmas ceļu** uz **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="34a51-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="34a51-134">Iestatiet **Aprakstu** uz **Ziņojuma ID**.</span><span class="sxs-lookup"><span data-stu-id="34a51-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="34a51-135">Pievienojiet tabulai rindu.</span><span class="sxs-lookup"><span data-stu-id="34a51-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="34a51-136">Iestatiet **Shēmas nosaukumu** uz **Laikspiedols**.</span><span class="sxs-lookup"><span data-stu-id="34a51-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="34a51-137">Iestatiet **Shēmas ceļu** uz **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="34a51-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="34a51-138">Iestatiet **Aprakstu** uz **Ziņojuma laikspiedols**.</span><span class="sxs-lookup"><span data-stu-id="34a51-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="34a51-139">Pievienojiet tabulai rindu.</span><span class="sxs-lookup"><span data-stu-id="34a51-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="34a51-140">Iestatiet **Shēmas nosaukumu** uz **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="34a51-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="34a51-141">Iestatiet **Shēmas ceļu** uz **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="34a51-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="34a51-142">Iestatiet **Aprakstu** uz **Ziņojuma vērtība**.</span><span class="sxs-lookup"><span data-stu-id="34a51-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="34a51-143">Nav nepieciešams definēt visus ziņojuma rekvizītus, tikai tos, kas nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="34a51-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="34a51-144">Šajā piemērā netika veidota rinda **Saknes laikspiedols**.</span><span class="sxs-lookup"><span data-stu-id="34a51-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="34a51-145">**Saknes laikspiedola** ceļš būtu **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="34a51-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="34a51-146">Noklikšķiniet uz **Tālāk**, lai dotos uz lapu **Aprīkojuma sensora shēmas karte**.</span><span class="sxs-lookup"><span data-stu-id="34a51-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="34a51-147">Rindā **Aprīkojuma resursa ID** iestatiet **Shēmas nosaukumu** uz **ID**.</span><span class="sxs-lookup"><span data-stu-id="34a51-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="34a51-148">Derīgās vērtības tiek rādītas nolaižamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="34a51-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="34a51-149">Rindā **UTC laiks** iestatiet **Shēmas nosaukumu** uz **Laikspiedols**.</span><span class="sxs-lookup"><span data-stu-id="34a51-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="34a51-150">Derīgās vērtības tiek rādītas nolaižamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="34a51-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="34a51-151">Rindā **Daļējas izgatavošanas signāls** iestatiet **Shēmas nosaukumu** uz **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="34a51-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="34a51-152">Derīgās vērtības tiek rādītas nolaižamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="34a51-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="34a51-153">Noklikšķiniet uz **Tālāk**, lai nonāktu lapā **Aprīkojuma resursa ID konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="34a51-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="34a51-154">Šajā darbībā kartējiet IoT centrmezgla ziņojuma vērtības uz Supply Chain Management resursiem.</span><span class="sxs-lookup"><span data-stu-id="34a51-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="34a51-155">Tabulā **Signāla datu vērtības** pievienojiet jaunu rindu un ievadiet **IoTInt.Machine1225.PartOut** kolonnā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="34a51-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="34a51-156">Vērtība **IoTInt.Machine1225.PartOut** tiek iegūta no IoT centrmezgla ziņojuma JSON **id** rekvizīta.</span><span class="sxs-lookup"><span data-stu-id="34a51-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="34a51-157">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="34a51-157">Click **Save**.</span></span>
    3. <span data-ttu-id="34a51-158">Tabulā **Biznesa ieraksta kartēšana** klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="34a51-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="34a51-159">Noklusējuma vērtība **Biznesa ieraksta veidam** tiek automātiski aizpildīta, un jums nav nepieciešams to mainīt.</span><span class="sxs-lookup"><span data-stu-id="34a51-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="34a51-160">Kolonnā **Biznesa ieraksts** atlasiet Supply Chain Management iekārtas resursu, no kura tiek sūtīta šī signāla vērtība.</span><span class="sxs-lookup"><span data-stu-id="34a51-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="34a51-161">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="34a51-161">Click **Save**.</span></span>
    6. <span data-ttu-id="34a51-162">Atkārtojiet šīs darbības, pievienojot jaunu biznesa ieraksta kartējumu **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="34a51-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="34a51-163">Varat kartēt vairāku signālu datu vērtības vienam Supply Chain Management ierakstam.</span><span class="sxs-lookup"><span data-stu-id="34a51-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="34a51-164">Izmantojiet kolonnu **Atlasīts**, lai izvēlētos iekārtas, ko vēlaties apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="34a51-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="34a51-165">Nav jādefinē visas signāla vērtības un nav jāatlasa visas iekārtas.</span><span class="sxs-lookup"><span data-stu-id="34a51-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="34a51-166">Noklikšķiniet **Tālāk**, lai dotos uz lapu **Daļu ražošanas signāla konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="34a51-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="34a51-167">Tabulā **Signāla datu vērtības** pievienojiet rindu un iestatiet **Vērtību** uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="34a51-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="34a51-168">Vērtība **Patiess** tiek iegūta no IoT centrmezgla ziņojuma JSON **vērtības** rekvizīta.</span><span class="sxs-lookup"><span data-stu-id="34a51-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="34a51-169">Scenārijam var pievienot tik daudz vērtību, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="34a51-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="34a51-170">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="34a51-170">Click **Save**.</span></span>
20. <span data-ttu-id="34a51-171">Noklikšķiniet **Tālāk**, lai dotos uz lapu **Aprīkojuma dīkstāves slieksnis**.</span><span class="sxs-lookup"><span data-stu-id="34a51-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="34a51-172">Norādītās iekārtas ir iepriekš uz signālu vērtībām kartētās iekārtas.</span><span class="sxs-lookup"><span data-stu-id="34a51-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="34a51-173">Šajā darbībā definējiet slieksni, lai noteiktu, vai iekārta darbojas.</span><span class="sxs-lookup"><span data-stu-id="34a51-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="34a51-174">Piemēram, ja iestatāt slieksni uz 10, Supply Chain Management ģenerē paziņojumu, ja 10 minūtes no iekārtas netiek izvadīts neviens ziņojums.</span><span class="sxs-lookup"><span data-stu-id="34a51-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="34a51-175">Noklikšķiniet **Tālāk**, lai dotos uz lapu **Iespējot scenāriju**.</span><span class="sxs-lookup"><span data-stu-id="34a51-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="34a51-176">Pārslēdziet slīdni, lai iespējotu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="34a51-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="34a51-177">Noklikšķiniet uz **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="34a51-177">Click **Finish**.</span></span>

<span data-ttu-id="34a51-178">Scenāriju iestatīšana ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="34a51-178">The scenario setup is complete.</span></span> <span data-ttu-id="34a51-179">IoT informācija automātiski sāks apstrādāt IoT centrmezgla ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="34a51-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="34a51-180">Konfigurēt scenāriju **Preces kvalitāte** Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="34a51-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="34a51-181">**Preces kvalitātes** scenārijs ģenerē paziņojumu, ja vienuma atribūts atrodas ārpus norādītā diapazona.</span><span class="sxs-lookup"><span data-stu-id="34a51-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="34a51-182">Piemēram, sensors katra vienuma svaru varētu nosūtīt uz IoT centrmezglu.</span><span class="sxs-lookup"><span data-stu-id="34a51-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="34a51-183">Paziņojums Supply Chain Management tiks ģenerēts, ja vienums būs pārāk smags vai pārāk viegls.</span><span class="sxs-lookup"><span data-stu-id="34a51-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="34a51-184">Scenārijam ir šādas atkarības:</span><span class="sxs-lookup"><span data-stu-id="34a51-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="34a51-185">Ražošanas pasūtījumam ir jādarbojas kartētā iekārtā un jāražo prece ar kartētu partijas atribūtu, lai tiktu parādīts brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="34a51-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="34a51-186">Uz IoT centrmezglu ar unikālu rekvizīta nosaukumu jānosūta signāls, kas apzīmē partijas atribūtu.</span><span class="sxs-lookup"><span data-stu-id="34a51-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="34a51-187">IoT centrmezgla ziņojumā jābūt Unix milisekundes laikspiedola rekvizītam.</span><span class="sxs-lookup"><span data-stu-id="34a51-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="34a51-188">Konfigurēt scenāriju **Ražošanas aizkaves** Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="34a51-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="34a51-189">**Ražošanas aizkaves** scenārijs ģenerē paziņojumu, ja ražošanas caurlaidspēja ir zemāka par sliekšņa vērtību.</span><span class="sxs-lookup"><span data-stu-id="34a51-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="34a51-190">Šādā gadījumā **PartOut** signāls tiek nosūtīts uz IoT centrmezglu katram saražotajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="34a51-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="34a51-191">Supply Chain Management pasūtījuma aizkave tiek aprēķināta, pamatojoties uz to, cik ilgā laikā paredzēts izpildīt ražošanas pasūtījumu, cik krājumu ir jāražo, cik ilgi darbs tiek veikts un cik **PartOut** signālu tiek saņemts.</span><span class="sxs-lookup"><span data-stu-id="34a51-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="34a51-192">Aizkavēšanas paziņojums tiks ģenerēts, ja **PartOut** signālu skaits darbam nokrītas zem paredzētās sliekšņa vērtības.</span><span class="sxs-lookup"><span data-stu-id="34a51-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="34a51-193">Scenārijam ir šādas atkarības:</span><span class="sxs-lookup"><span data-stu-id="34a51-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="34a51-194">Lai brīdinājums tiktu parādīts, ražošanas pasūtījumam ir jādarbojas kartētā iekārtā.</span><span class="sxs-lookup"><span data-stu-id="34a51-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="34a51-195">Uz IoT centrmezglu ar unikālu rekvizīta nosaukumu jānosūta signāls, kas apzīmē kartētās iekārtas izslēgšanas signālu.</span><span class="sxs-lookup"><span data-stu-id="34a51-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="34a51-196">IoT centrmezgla ziņojumā jābūt Unix milisekundes laikspiedola rekvizītam.</span><span class="sxs-lookup"><span data-stu-id="34a51-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="34a51-197">Scenārija atspējošana</span><span class="sxs-lookup"><span data-stu-id="34a51-197">How to disable a scenario</span></span>

<span data-ttu-id="34a51-198">Lai atspējotu scenāriju, izpildiet tālāk aprakstītās darbības:</span><span class="sxs-lookup"><span data-stu-id="34a51-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="34a51-199">Supply Chain Management pārejiet uz **Ražošanas kontrole \> Iestatīšana \> IoT informācija \> Scenārija pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="34a51-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="34a51-200">Scenārijā noklikšķiniet uz **Konfigurēt**.</span><span class="sxs-lookup"><span data-stu-id="34a51-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="34a51-201">Noklikšķiniet **Tālāk**, lai nokļūtu pēdējā vedņa cilnē.</span><span class="sxs-lookup"><span data-stu-id="34a51-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="34a51-202">Pārslēdziet slīdni, lai atspējotu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="34a51-202">Toggle the slider to disable the scenario.</span></span>
