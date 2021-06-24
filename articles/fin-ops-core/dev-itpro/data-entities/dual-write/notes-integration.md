---
title: Piezīmju integrācija
description: Šajā tēmā aprakstīta piezīmju datu integrācija duālajā ierakstā.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186790"
---
# <a name="note-integration"></a><span data-ttu-id="67194-103">Piezīmju integrācija</span><span class="sxs-lookup"><span data-stu-id="67194-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="67194-104">Biznesa procesu laikā Microsoft Dynamics 365 lietotāji bieži apkopo informāciju par saviem klientiem.</span><span class="sxs-lookup"><span data-stu-id="67194-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="67194-105">Šī informācija tiek reģistrēta kā aktivitātes un piezīmes.</span><span class="sxs-lookup"><span data-stu-id="67194-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="67194-106">Šajā tēmā aprakstīta piezīmju datu integrācija duālajā ierakstā.</span><span class="sxs-lookup"><span data-stu-id="67194-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="67194-107">Klienta informāciju var klasificēt vairākos veidos:</span><span class="sxs-lookup"><span data-stu-id="67194-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="67194-108">**Izmantojamā informācija, ko Dynamics 365 lietotājs apstrādā klienta vārdā** — piemēram, Contoso (Dynamics 365 lietotājs) organizē spēļu šovu.</span><span class="sxs-lookup"><span data-stu-id="67194-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="67194-109">Viens no Contoso klientiem (klients) vēlas piedalīties spēļu šovā.</span><span class="sxs-lookup"><span data-stu-id="67194-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="67194-110">Klients lūdz Contoso darbinieku rezervēt viņiem slotu spēļu šovā.</span><span class="sxs-lookup"><span data-stu-id="67194-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="67194-111">Rezervācija notiek Contoso notikuma dalībnieka kalendārā.</span><span class="sxs-lookup"><span data-stu-id="67194-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="67194-112">**Izmantojamā informācija Dynamics 365 lietotājam** — piemēram, klients, kurš iegādājas vienību Surface, ievada īpašas instrukcijas, kas norāda, ka ierīcei pirms piegādes ir jābūt iesaiņotai kā dāvanai.</span><span class="sxs-lookup"><span data-stu-id="67194-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="67194-113">Šīs instrukcijas ir izmantojama informācija, kas jāapstrādā Contoso darbiniekam, kurš ir atbildīgs par iepakošanu.</span><span class="sxs-lookup"><span data-stu-id="67194-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="67194-114">**Informācija, kas nav izmantojama** — piemēram, klients apmeklē Contoso veikalu un sarunas ar veikala darbinieku laikā pauž interesi par *Halo* spēlēm un spēļu piederumiem.</span><span class="sxs-lookup"><span data-stu-id="67194-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="67194-115">Veikala darbinieks izdara piezīmi par šo informāciju.</span><span class="sxs-lookup"><span data-stu-id="67194-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="67194-116">Pēc tam preču ieteikumu programma to izmanto, lai klientam varētu sniegt ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="67194-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="67194-117">Parasti izmantojamā informācija tiek tverta kā *aktivitātes* programmās Finance and Operations un Customer Engagement programmās.</span><span class="sxs-lookup"><span data-stu-id="67194-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="67194-118">Neizmantojamā informācija tiek tverta kā *piezīmes* programmās Finance and Operations un kā *anotācijas* Customer Engagement programmās.</span><span class="sxs-lookup"><span data-stu-id="67194-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="67194-119">Lai arī piezīmes ir paredzētas neizmantojamajai informācijai, programmas neliegs jums tās izmantot, lai saglabātu un apstrādātu izmantojamo informāciju, ja vēlaties tās izmantot šādā veidā.</span><span class="sxs-lookup"><span data-stu-id="67194-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="67194-120">Microsoft pašlaik izlaiž funkcionalitāti piezīmju integrācijai.</span><span class="sxs-lookup"><span data-stu-id="67194-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="67194-121">(Funkcionalitāte aktivitātes integrācijai tiks izlaista vēlāk.) Piezīmju integrācija ir pieejama klientiem, kreditoriem, pārdošanas pasūtījumiem un pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="67194-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="67194-122">Piezīmes izveide programmā Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="67194-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="67194-123">Lai izveidotu piezīmi programmā Customer Engagement un pēc tam to sinhronizētu ar Finance and Operations programmu, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="67194-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="67194-124">Programmā Customer Engagement atveriet klienta konta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="67194-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="67194-125">Rūtī **Laika skala** atlasiet plus zīmi (**+**) un pēc tam atlasiet **Piezīme**, lai izveidotu piezīmi.</span><span class="sxs-lookup"><span data-stu-id="67194-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Piezīmes izveide programmā Customer Engagement](media/notes-ce-1.png)

3. <span data-ttu-id="67194-127">Ievadiet nosaukumu un aprakstu un pēc tam atlasiet **Pievienot piezīmi**.</span><span class="sxs-lookup"><span data-stu-id="67194-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Virsraksta un apraksta ievadīšana](media/notes-ce-2.png)

    <span data-ttu-id="67194-129">Jaunā piezīme tiek pievienota klienta laika skalai.</span><span class="sxs-lookup"><span data-stu-id="67194-129">The new note is added to the customer timeline.</span></span>

    ![Jauna piezīme klienta laika skalā](media/notes-ce-3.png)

4. <span data-ttu-id="67194-131">Pierakstieties programmā Finance and Operations un atveriet to pašu klienta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="67194-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="67194-132">Ievērojiet, ka poga **Pielikumi** button (saspraudes simbols) augšējā labajā stūrī norāda, ka ierakstam ir pielikums.</span><span class="sxs-lookup"><span data-stu-id="67194-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Paziņojums par pielikumu](media/notes-ce-4.png)

5. <span data-ttu-id="67194-134">Atlasiet pogu **Pielikumi**, lai atvērtu lapu **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="67194-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="67194-135">Jums vajadzētu atrast piezīmi, ko esat izveidojis programmā Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="67194-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Piezīme no programmas Customer Engagement](media/notes-ce-5.png)

<span data-ttu-id="67194-137">Visi piezīmes atjauninājumi tiek sinhronizēti abos virzienos starp programmu Finance and Operations un programmu Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="67194-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="67194-138">Piezīmes izveide programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="67194-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="67194-139">Varat izveidot piezīmi arī programmā Finance and Operations, un pēc tam tā tiks sinhronizēta ar programmu Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="67194-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="67194-140">Lai izveidotu piezīmi programmā Finance and Operations un pēc tam to sinhronizētu ar programmu Customer Engagement, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="67194-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="67194-141">Programmas Finance and Operations lapā **Pielikumi** atlasiet **Jauns** \> **Piezīme**.</span><span class="sxs-lookup"><span data-stu-id="67194-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Piezīmes izveide programmā Finance and Operations](media/notes-fo-1.png)

2. <span data-ttu-id="67194-143">Ievadiet nosaukumu un īsu norādījumu kopu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="67194-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Virsraksta un instrukciju ievadīšana](media/notes-fo-2.png)

3. <span data-ttu-id="67194-145">Programmā Customer Engagement atjauniniet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="67194-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="67194-146">Jaunā piezīme atradīsies laika skalā.</span><span class="sxs-lookup"><span data-stu-id="67194-146">You should find the new note on the timeline.</span></span>

    ![Jauna piezīme laika skalā programmā Customer Engagement](media/notes-fo-3.png)

<span data-ttu-id="67194-148">Piezīmi var klasificēt kā iekšēju vai ārēju.</span><span class="sxs-lookup"><span data-stu-id="67194-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="67194-149">Programmas Finance and Operations lapā **Pielikumi** atveriet piezīmi un pēc tam laukā **Ierobežojums** atlasiet **Iekšēja** vai **Ārēja**.</span><span class="sxs-lookup"><span data-stu-id="67194-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Ierobežojuma lauks](media/notes-fo-4.png)

<span data-ttu-id="67194-151">Var izveidot arī vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="67194-151">You can also create a URL.</span></span>

1. <span data-ttu-id="67194-152">Programmas Finance and Operations lapā **Pielikumi** atlasiet **Jauns** \> **Vietrādis URL**.</span><span class="sxs-lookup"><span data-stu-id="67194-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="67194-153">Ievadiet virsrakstu un vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="67194-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="67194-154">Laukā **Ierobežojums** atlasiet **Iekšējais** vai **Ārējais**.</span><span class="sxs-lookup"><span data-stu-id="67194-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Vietrāža URL izveide programmā Finance and Operations](media/notes-fo-5.png)

4. <span data-ttu-id="67194-156">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="67194-156">Select **Save**.</span></span>

    <span data-ttu-id="67194-157">Tā kā programmām Customer Engagement nav vietrāža URL veida, tas tiek integrēts ar dubulto ierakstu kā piezīme.</span><span class="sxs-lookup"><span data-stu-id="67194-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![Vietrāža URL parādīšana piezīmes veidā programmā Customer Engagement](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="67194-159">Failu pielikumi netiek atbalstīti.</span><span class="sxs-lookup"><span data-stu-id="67194-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="67194-160">Veidnes</span><span class="sxs-lookup"><span data-stu-id="67194-160">Templates</span></span>

<span data-ttu-id="67194-161">Piezīmju integrācija ietver tabulas karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="67194-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="67194-162">Finance and Operations programma</span><span class="sxs-lookup"><span data-stu-id="67194-162">Finance and Operations app</span></span> | <span data-ttu-id="67194-163">Customer engagement programma</span><span class="sxs-lookup"><span data-stu-id="67194-163">Customer engagement app</span></span> | <span data-ttu-id="67194-164">Apraksts</span><span class="sxs-lookup"><span data-stu-id="67194-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="67194-165">Debitora pielikumi</span><span class="sxs-lookup"><span data-stu-id="67194-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="67194-166">Anotācijas</span><span class="sxs-lookup"><span data-stu-id="67194-166">Annotations</span></span> | <span data-ttu-id="67194-167">Uzņēmumi, kas izmanto vienkāršu tekstu un vietrāžus URL, lai tvertu debitoram specifisko informāciju (gan organizācijām, gan personām).</span><span class="sxs-lookup"><span data-stu-id="67194-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="67194-168">Kreditora dokumentu pielikumi</span><span class="sxs-lookup"><span data-stu-id="67194-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="67194-169">Anotācijas</span><span class="sxs-lookup"><span data-stu-id="67194-169">Annotations</span></span> | <span data-ttu-id="67194-170">Uzņēmumi, kas izmanto vienkāršu tekstu un vietrāžus URL, lai tvertu kreditoram specifisko informāciju (gan organizācijām, gan personām).</span><span class="sxs-lookup"><span data-stu-id="67194-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="67194-171">Pārdošanas pasūtījuma galvenes dokumenta pielikumi</span><span class="sxs-lookup"><span data-stu-id="67194-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="67194-172">Anotācijas</span><span class="sxs-lookup"><span data-stu-id="67194-172">Annotations</span></span> | <span data-ttu-id="67194-173">Uzņēmumi, kas izmanto vienkāršu tekstu un vietrāžus URL, lai tvertu pārdošanas pasūtījumam specifisku informāciju.</span><span class="sxs-lookup"><span data-stu-id="67194-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="67194-174">Pirkšanas pasūtījuma galvenes dokumenta pielikumi</span><span class="sxs-lookup"><span data-stu-id="67194-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="67194-175">Anotācijas</span><span class="sxs-lookup"><span data-stu-id="67194-175">Annotations</span></span> | <span data-ttu-id="67194-176">Uzņēmumi, kas izmanto vienkāršu tekstu un vietrāžus URL, lai tvertu pirkšanas pasūtījumam specifisku informāciju.</span><span class="sxs-lookup"><span data-stu-id="67194-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

## <a name="limitations"></a><span data-ttu-id="67194-177">Ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="67194-177">Limitations</span></span>

<span data-ttu-id="67194-178">Kad piezīmju risinājums ir instalēts, to nevar atinstalēt.</span><span class="sxs-lookup"><span data-stu-id="67194-178">Once you install the notes solution, you cannot uninstall it.</span></span> 

<span data-ttu-id="67194-179">Papildinformāciju skatiet sadaļā [Dubultā ieraksta kartēšanas atsauce](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="67194-179">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
