---
title: IoT informācijas scenārija iestatīšana
description: Šajā tēmā ir izskaidrots, kā konfigurēt IoT informāciju programmā Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1deaa2130b63272da39a42315c6a1bc4b7ccb8a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433028"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="eba98-103">IoT informācijas scenārija iestatīšana</span><span class="sxs-lookup"><span data-stu-id="eba98-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eba98-104">Šajā tēmā ir izskaidrots, kā konfigurēt IoT informāciju programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eba98-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="eba98-105">Pirms scenāriju iestatīšanas vispirms ir [jāiestata Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="eba98-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="eba98-106">Šajā tēmā jūs konfigurēsit scenāriju **Aprīkojuma dīkstāve**, lai tiktu izveidots paziņojumu Supply Chain Management, kad iekārta netiek izmantota.</span><span class="sxs-lookup"><span data-stu-id="eba98-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="eba98-107">Tēmā ir arī parādīts, kā konfigurēt scenāriju **Preču kvalitāte**, lai paziņojums tiktu ģenerēts, ja vienuma atribūts atrodas ārpus norādītā diapazona, un kā konfigurēt scenāriju **Ražošanas aizkave**, lai tiktu ģenerēts paziņojums, ja ražošanas caurlaidspēja ir zemāka par sliekšņa vērtību.</span><span class="sxs-lookup"><span data-stu-id="eba98-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="eba98-108">Konfigurēt scenāriju Aprīkojuma dīkstāve Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="eba98-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="eba98-109">Scenārijs **Aprīkojuma dīkstāve** kartē iekārtas brīdinājuma sliekšņa **PartOut** signālu.</span><span class="sxs-lookup"><span data-stu-id="eba98-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="eba98-110">Iekārta tiek uzraudzīta tikai tad, ja tā ir izvēlēta scenārijam un, kad tā ir iestatīta kā **Darbībā esoša** risinājumā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eba98-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="eba98-111">Ja laiks, kas pagājis kopš pēdējā saņemtā **PartOut** signāla no iekārtas pārsniedz brīdinājuma robežvērtību, tiek parādīts paziņojums **Iekārta dīkstāvē**.</span><span class="sxs-lookup"><span data-stu-id="eba98-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="eba98-112">Ja iekārta joprojām darbojas, tiek parādīts paziņojums **Iekārta darbojas**, kad tiek saņemts nākamais **PartOut** signāls.</span><span class="sxs-lookup"><span data-stu-id="eba98-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="eba98-113">Ja iekārta pārstāj darboties uz 30 minutēm, tiek parādīts jauns paziņojums **Iekārta dīkstāvē**.</span><span class="sxs-lookup"><span data-stu-id="eba98-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="eba98-114">Scenārijam **Aprīkojuma dīkstāve** ir šādas atkarības:</span><span class="sxs-lookup"><span data-stu-id="eba98-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="eba98-115">Brīdinājums var tikt parādīts tikai tad, ja ražošanas pasūtījums darbojas kartētā iekārtā.</span><span class="sxs-lookup"><span data-stu-id="eba98-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="eba98-116">Signāls, kas apzīmē kartētu iekārtas **PartOut** signālu ir jānosūta uz IoT centrmezglu un ir jāiekļauj unikāls rekvizīta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="eba98-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="eba98-117">UNIX rekvizīts **laikspiedols**, kur vērtība ir izteikta milisekundēs (ms), ir jāatrodas Azure IoT Hub ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="eba98-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="eba98-118">Lai konfigurētu scenāriju, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="eba98-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="eba98-119">Pierakstieties Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eba98-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="eba98-120">Iespējojiet IoT informācijas līdzekļa karodziņu.</span><span class="sxs-lookup"><span data-stu-id="eba98-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="eba98-121">Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="eba98-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="eba98-122">Konfigurējiet rādītājus.</span><span class="sxs-lookup"><span data-stu-id="eba98-122">Configure the metrics.</span></span> <span data-ttu-id="eba98-123">Papildinformāciju skatiet [Rādītāju konfigurēšana](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="eba98-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="eba98-124">Dodieties uz **Ražošanas kontrole \> Iestatījumi \> IoT informācija \> Scenāriju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="eba98-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="eba98-125">Lai atvērtu konfigurācijas vedni, elementā **Aprīkojuma dīkstāve** atlasiet **Konfigurēt**.</span><span class="sxs-lookup"><span data-stu-id="eba98-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="eba98-126">Pirmā lapa vednī ir lapa **Aprīkojuma sensora shēmas definīcija**.</span><span class="sxs-lookup"><span data-stu-id="eba98-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="eba98-127">Šajā lapā jūsu mērķis ir iestatīt shēmu risinājumā Supply Chain Management, lai tā atbilstu IoT Hub ziņojuma JavaScript Object Notation (JSON) formātam.</span><span class="sxs-lookup"><span data-stu-id="eba98-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="eba98-128">Var tikt definētas vairākas ziņojumu shēmas.</span><span class="sxs-lookup"><span data-stu-id="eba98-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="eba98-129">Papildinformāciju skatiet [Shēmas formāti IoT Hub ziņojumiem](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="eba98-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="eba98-130">Šajā piemērā ziņojuma lietderīgā slodze satur ziņojumu paketi ar šādu formātu.</span><span class="sxs-lookup"><span data-stu-id="eba98-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

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

7. <span data-ttu-id="eba98-131">Pievienojiet rindu tabulai un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eba98-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="eba98-132">Iestatiet lauku **Shēmas nosaukums** uz **ID**.</span><span class="sxs-lookup"><span data-stu-id="eba98-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="eba98-133">Iestatiet lauku **Shēmas ceļš** uz **/payload\[\*\]/id**.</span><span class="sxs-lookup"><span data-stu-id="eba98-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="eba98-134">Iestatiet lauku **Apraksts** uz **Ziņojuma ID**.</span><span class="sxs-lookup"><span data-stu-id="eba98-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="eba98-135">Pievienojiet vēl vienu rindu tabulai un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eba98-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="eba98-136">Iestatiet lauku **Shēmas nosaukums** uz **Laikspiedols**.</span><span class="sxs-lookup"><span data-stu-id="eba98-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="eba98-137">Iestatiet lauku **Shēmas ceļš** uz **/payload\[\*\]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="eba98-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="eba98-138">Iestatiet lauku **Apraksts** uz **Ziņojuma laikspiedols**.</span><span class="sxs-lookup"><span data-stu-id="eba98-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="eba98-139">Pievienojiet vēl vienu rindu tabulai un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eba98-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="eba98-140">Iestatiet lauku **Shēmas nosaukums** uz **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="eba98-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="eba98-141">Iestatiet lauku **Shēmas ceļš** uz **/payload\[\*\]/value**.</span><span class="sxs-lookup"><span data-stu-id="eba98-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="eba98-142">Iestatiet lauku **Apraksts** uz **Ziņojuma vērtība**.</span><span class="sxs-lookup"><span data-stu-id="eba98-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eba98-143">Nav jādefinē visi ziņojuma rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="eba98-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="eba98-144">Nosakiet tikai tos rekvizītus, kas ir nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="eba98-144">Define only the properties that you require.</span></span> <span data-ttu-id="eba98-145">Iepriekšējās darbībās neesat izveidojis rindu **Saknes laikspiedols**.</span><span class="sxs-lookup"><span data-stu-id="eba98-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="eba98-146">Ceļš laukam **Saknes laikspiedols** būtu **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="eba98-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="eba98-147">Atlasiet **Tālāk**, lai dotos uz lapu **Aprīkojuma sensora shēmas karte**.</span><span class="sxs-lookup"><span data-stu-id="eba98-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="eba98-148">Rindā **Aprīkojuma resursa ID** laukā **Shēmas nosaukums** atlasiet **ID**.</span><span class="sxs-lookup"><span data-stu-id="eba98-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="eba98-149">Rindā **UTC laiks** laukā **Shēmas nosaukums** atlasiet **Laikspiedols**.</span><span class="sxs-lookup"><span data-stu-id="eba98-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="eba98-150">Rindā **Daļējas izgatavošanas signāls** laukā **Shēmas nosaukums** atlasiet **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="eba98-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="eba98-151">Atlasiet **Tālāk**, lai dotos uz lapu **Aprīkojuma resursa ID konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="eba98-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="eba98-152">Veiciet tālāk norādītās darbības, lai kartētu vērtības IoT Hub ziņojumā uz Supply Chain Management resursiem.</span><span class="sxs-lookup"><span data-stu-id="eba98-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="eba98-153">Tabulā **Signāla datu vērtības** pievienojiet jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="eba98-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="eba98-154">Laukā **Vērtība** ievadiet **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="eba98-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="eba98-155">Šī vērtība tiek iegūta no IoT Hub ziņojuma JSON **id** rekvizīta.</span><span class="sxs-lookup"><span data-stu-id="eba98-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="eba98-156">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eba98-156">Select **Save**.</span></span>
    3. <span data-ttu-id="eba98-157">Tabulā **Biznesa ieraksta kartēšana** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eba98-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="eba98-158">Noklusējuma vērtība laukam **Biznesa ieraksta veids** tiek automātiski aizpildīta, un jums nav nepieciešams to mainīt.</span><span class="sxs-lookup"><span data-stu-id="eba98-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="eba98-159">Laukā **Biznesa ieraksts** atlasiet Supply Chain Management iekārtas resursu, no kura tiek sūtīta šī signāla vērtība.</span><span class="sxs-lookup"><span data-stu-id="eba98-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="eba98-160">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eba98-160">Select **Save**.</span></span>
    6. <span data-ttu-id="eba98-161">Atkārtojiet šīs darbības, lai pievienotu jaunu biznesa ieraksta kartējumu **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="eba98-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="eba98-162">Varat kartēt vairāku signālu datu vērtības vienam Supply Chain Management ierakstam.</span><span class="sxs-lookup"><span data-stu-id="eba98-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="eba98-163">Izmantojiet kolonnu **Atlasīts**, lai atlasītu iekārtas, ko vēlaties apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="eba98-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="eba98-164">Nav jādefinē visas signāla vērtības, un nav jāatlasa visas iekārtas.</span><span class="sxs-lookup"><span data-stu-id="eba98-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="eba98-165">Atlasiet **Tālāk**, lai dotos uz lapu **Daļu ražošanas signāla konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="eba98-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="eba98-166">Tabulā **Signāla datu vērtības** pievienojiet rindu un iestatiet lauku **Vērtība** uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="eba98-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="eba98-167">Šī vērtība tiek iegūta no IoT Hub ziņojuma JSON **vertība** rekvizīta.</span><span class="sxs-lookup"><span data-stu-id="eba98-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="eba98-168">Scenārijam var pievienot tik daudz vērtību, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="eba98-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="eba98-169">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eba98-169">Select **Save**.</span></span>
20. <span data-ttu-id="eba98-170">Atlasiet **Tālāk**, lai dotos uz lapu **Aprīkojuma dīkstāves slieksnis**.</span><span class="sxs-lookup"><span data-stu-id="eba98-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="eba98-171">Norādītās iekārtas ir iekārtas, kas iepriekš tika kartētas uz signāla vērtībām.</span><span class="sxs-lookup"><span data-stu-id="eba98-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="eba98-172">Šajā lapā definējiet slieksni, lai noteiktu, vai iekārta darbojas.</span><span class="sxs-lookup"><span data-stu-id="eba98-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="eba98-173">Piemēram, ja iestatāt slieksni uz **10**, Supply Chain Management ģenerēs paziņojumu, ja 10 minūtes no iekārtas netiek saņemts neviens **PartOut** signāls.</span><span class="sxs-lookup"><span data-stu-id="eba98-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="eba98-174">Atlasiet **Tālāk**, lai dotos uz lapu **Iespējot scenāriju**.</span><span class="sxs-lookup"><span data-stu-id="eba98-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="eba98-175">Iestatiet opciju, lai iespējotu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="eba98-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="eba98-176">Atl. **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="eba98-176">Select **Finish**.</span></span>

<span data-ttu-id="eba98-177">Scenāriju iestatīšana tagad ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="eba98-177">The scenario setup is now completed.</span></span> <span data-ttu-id="eba98-178">IoT informācija automātiski sāks apstrādāt IoT centrmezgla ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="eba98-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="eba98-179">Konfigurēt scenāriju Preces kvalitāte Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="eba98-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="eba98-180">**Preces kvalitātes** scenārijs ģenerē paziņojumu, ja vienuma atribūts atrodas ārpus norādītā diapazona.</span><span class="sxs-lookup"><span data-stu-id="eba98-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="eba98-181">Piemēram, sensors katra vienuma svaru nosūta uz IoT centrmezglu.</span><span class="sxs-lookup"><span data-stu-id="eba98-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="eba98-182">Ja vienums ir pārāk smags vai pārāk viegls, tiek ģenerēts paziņojums risinājumā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eba98-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="eba98-183">Scenārijam **Preču kvalitāte** ir šādas atkarības:</span><span class="sxs-lookup"><span data-stu-id="eba98-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="eba98-184">Brīdinājums var tikt parādīts tikai tad, ja ražošanas pasūtījums darbojas kartētā iekārtā un ražo preci ar kartētu partijas atribūtu.</span><span class="sxs-lookup"><span data-stu-id="eba98-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="eba98-185">Signāls, kas apzīmē partijas atribūtu, ir jānosūta uz IoT Hub, un ir jāiekļauj unikāls rekvizīta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="eba98-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="eba98-186">UNIX rekvizīts **laikspiedols**, kur vērtība ir izteikta ms, ir jāatrodas IoT Hub ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="eba98-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="eba98-187">Konfigurēt scenāriju Ražošanas aizkaves Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="eba98-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="eba98-188">**Ražošanas aizkaves** scenārijs ģenerē paziņojumu, ja ražošanas caurlaidspēja ir zemāka par sliekšņa vērtību.</span><span class="sxs-lookup"><span data-stu-id="eba98-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="eba98-189">Šādā gadījumā **PartOut** signāls tiek nosūtīts uz IoT Hub katrai ražotajai precei.</span><span class="sxs-lookup"><span data-stu-id="eba98-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="eba98-190">Risinājumā Supply Chain Management pasūtījuma aizkave tiek aprēķināta, ņemot vērā laiku, kad ražošanas pasūtījums tiek plānots izpildei, krājumu skaitu, kas jāsagatavo, laiku, kad darbs ir palaists, un **PartOut** saņemto signālu skaitu.</span><span class="sxs-lookup"><span data-stu-id="eba98-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="eba98-191">Aizkavēšanas paziņojums tiek ģenerēts, ja **PartOut** signālu skaits darbam nokrītas zem sliekšņa vērtības.</span><span class="sxs-lookup"><span data-stu-id="eba98-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="eba98-192">Scenārijam **Ražošanas kavējumi** ir šādas atkarības:</span><span class="sxs-lookup"><span data-stu-id="eba98-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="eba98-193">Brīdinājums var tikt parādīts tikai tad, ja ražošanas pasūtījums darbojas kartētā iekārtā.</span><span class="sxs-lookup"><span data-stu-id="eba98-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="eba98-194">Signāls, kas apzīmē kartētu iekārtas **PartOut** signālu ir jānosūta uz Azure IoT centrmezglu un ir jāiekļauj unikāls rekvizīta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="eba98-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="eba98-195">UNIX rekvizīts **laikspiedols**, kur vērtība ir izteikta ms, ir jāatrodas IoT Hub ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="eba98-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="eba98-196">Scenārija atspējošana</span><span class="sxs-lookup"><span data-stu-id="eba98-196">Disable a scenario</span></span>

<span data-ttu-id="eba98-197">Lai atspējotu scenāriju, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="eba98-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="eba98-198">Risinājumā Supply Chain Management dodieties uz **Ražošanas kontrole \> Iestatīšana \> IoT informācija \> Scenārija pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="eba98-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="eba98-199">Scenārija elementā atlasiet **Konfigurēt**.</span><span class="sxs-lookup"><span data-stu-id="eba98-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="eba98-200">Atlasiet **Tālāk**, lai dotos uz pēdējo vedņa lapu.</span><span class="sxs-lookup"><span data-stu-id="eba98-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="eba98-201">Iestatiet opciju, lai atspējotu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="eba98-201">Set the option to disable the scenario.</span></span>
