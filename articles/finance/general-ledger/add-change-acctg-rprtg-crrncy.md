---
title: Uzskaites vai pārskata valūtas maiņa
description: Šajā tēmā ir paskaidrots, kā mainīt uzskaites vai pārskata valūtu vai pievienot pārskata valūtu virsgrāmatas iestatījumiem.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0435deb009173684c7faaf5340e8095c019ec71c
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085478"
---
# <a name="change-the-accounting-or-reporting-currency"></a><span data-ttu-id="fb647-103">Uzskaites vai pārskata valūtas maiņa</span><span class="sxs-lookup"><span data-stu-id="fb647-103">Change the accounting or reporting currency</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb647-104">Šajā tēmā ir paskaidrots, kā mainīt uzskaites vai pārskata valūtu vai pievienot pārskata valūtu virsgrāmatas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="fb647-104">This topic explains how to change the accounting or reporting currency, or add a reporting currency to the setup of a ledger.</span></span>

## <a name="symptom"></a><span data-ttu-id="fb647-105">Simptoms</span><span class="sxs-lookup"><span data-stu-id="fb647-105">Symptom</span></span>

<span data-ttu-id="fb647-106">Jūs vēlaties mainīt uzskaites vai pārskata valūtu vai pievienot pārskata valūtu virsgrāmatas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="fb647-106">You want to change the accounting or reporting currency, or add a reporting currency to the ledger setup.</span></span> <span data-ttu-id="fb647-107">Tas parasti notiek tālāk aprakstītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="fb647-107">This typically occurs in the following scenarios:</span></span>

- <span data-ttu-id="fb647-108">Iestatot juridisku personu, tika norādīta nepareiza uzskaites vai pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="fb647-108">The wrong accounting or reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="fb647-109">Tagad jūs vēlaties mainīt šo valūtu.</span><span class="sxs-lookup"><span data-stu-id="fb647-109">You now want to change that currency.</span></span>
- <span data-ttu-id="fb647-110">Iestatot juridisku personu, tika norādīta pārskata valūta, bet tagad organizācija vēlas noņemt pārskata valūtu.</span><span class="sxs-lookup"><span data-stu-id="fb647-110">A reporting currency was specified when a legal entity was set up, but the organization now wants to remove the reporting currency.</span></span>
- <span data-ttu-id="fb647-111">Organizācija jaunina vai migrē uz Microsoft Dynamics 365 Finance un vēlas mainīt uzskaites vai pārskata valūtu.</span><span class="sxs-lookup"><span data-stu-id="fb647-111">The organization is upgrading or migrating to Microsoft Dynamics 365 Finance, and wants to change the accounting or reporting currency.</span></span>

<span data-ttu-id="fb647-112">Organizācija, kas iepriekš neizmantoja divkāršās valūtas iespēju, vēlas sākt to izmantot.</span><span class="sxs-lookup"><span data-stu-id="fb647-112">An organization that didn't previously use the Dual currency capability wants to start to use it.</span></span> <span data-ttu-id="fb647-113">Šī problēma parasti notiek tālāk aprakstītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="fb647-113">This issue typically occurs in the following scenarios.</span></span>

- <span data-ttu-id="fb647-114">Iestatot juridisku personu, netika norādīta nekāda uzskaites vai pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="fb647-114">No reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="fb647-115">(Pārskata valūta nav obligāta.) Tagad vēlaties pievienot pārskata valūtu.</span><span class="sxs-lookup"><span data-stu-id="fb647-115">(A reporting currency is optional.) You now want to add a reporting currency.</span></span>

## <a name="resolution"></a><span data-ttu-id="fb647-116">Novēršana</span><span class="sxs-lookup"><span data-stu-id="fb647-116">Resolution</span></span>

<span data-ttu-id="fb647-117">Svarīgākais apsvērums ir tas, vai virsgrāmatas iestatījumos juridiskajai personai ir iegrāmatotas jebkādas transakcijas (faktiskas vai budžeta).</span><span class="sxs-lookup"><span data-stu-id="fb647-117">The most important consideration is whether any transactions (actual or budget) have been posted in the legal entity for the ledger setup.</span></span> <span data-ttu-id="fb647-118">**Ja par juridisko personu ir iegrāmatotas jebkādas transakcijas (faktiskas vai budžeta), nav iespējams mainīt uzskaites vai pārskata valūtu vai pievienot pārskata valūtu.**</span><span class="sxs-lookup"><span data-stu-id="fb647-118">**You can't change the accounting or reporting currency, or add a reporting currency, if any transactions (actual or budget) have been posted in the legal entity.**</span></span> <span data-ttu-id="fb647-119">Atkarībā no tā, vai transakcijas ir iegrāmatotas, veiciet kādā no tālāk norādītajām sadaļām aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fb647-119">Follow the steps in one of the following sections, depending on whether transactions have been posted.</span></span>

### <a name="no-transactions-have-been-posted"></a><span data-ttu-id="fb647-120">Nav iegrāmatota neviena transakcija</span><span class="sxs-lookup"><span data-stu-id="fb647-120">No transactions have been posted</span></span>

1. <span data-ttu-id="fb647-121">Tās juridiskās personas sadaļā, kurai atjaunināt valūtas, dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="fb647-121">In the legal entity that you're updating currencies for, go to **General ledger \> Ledger setup \> Ledger**.</span></span>
2. <span data-ttu-id="fb647-122">Lapā **Virsgrāmata** atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="fb647-122">On the **Ledger** page, select **Edit**.</span></span>
3. <span data-ttu-id="fb647-123">Kopsavilkuma cilnē **Valūta** atlasiet juridiskajai personai izmantojamo uzskaites valūtu un pārskata valūtu.</span><span class="sxs-lookup"><span data-stu-id="fb647-123">On the **Currency** FastTab, select the accounting currency and reporting currency to use for the legal entity.</span></span>
4. <span data-ttu-id="fb647-124">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="fb647-124">Select **Save**.</span></span>

<span data-ttu-id="fb647-125">Ja lapā **Virsgrāmata** nav pieejami uzskaites valūtas un pārskata valūtas lauki, par juridisko personu ir iegrāmatota viena vai vairākas transakcijas (faktiskas vai budžeta).</span><span class="sxs-lookup"><span data-stu-id="fb647-125">If the fields for the accounting currency and the reporting currency aren't available on the **Ledger** page, one or more transactions (actual or budget) have been posted in the legal entity.</span></span> <span data-ttu-id="fb647-126">Tādēļ valūtas nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="fb647-126">Therefore, the currencies can't be changed.</span></span> <span data-ttu-id="fb647-127">Šādā gadījumā veiciet nākamajā sadaļā norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fb647-127">In this case, follow the steps in the next section.</span></span>

### <a name="transactions-have-been-posted"></a><span data-ttu-id="fb647-128">Ir iegrāmatotas transakcijas</span><span class="sxs-lookup"><span data-stu-id="fb647-128">Transactions have been posted</span></span>

<span data-ttu-id="fb647-129">**Ja juridiskajai personai ir iegrāmatotas transakcijas, tad vienīgais veids, kā mainīt vai pievienot uzskaites un pārskata valūtas, ir izveidot jaunu juridisko personu ar pareizajām valūtām.**</span><span class="sxs-lookup"><span data-stu-id="fb647-129">**If transactions have been posted in the legal entity, the only way to change or add accounting and reporting currencies is to create a new legal entity that has the correct currencies.**</span></span> <span data-ttu-id="fb647-130">Lai palīdzētu padarīt šo procesu ērtāku, datu pārvaldības opcija sistēmā sniedz iespēju kopēt iestatīšanas ierakstus un pamata ierakstus no pašreizējās juridiskās personas uz jaunu juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="fb647-130">To help make this process easier, Data management in the system lets you copy setup records and master records from the current legal entity to a new legal entity.</span></span>

<span data-ttu-id="fb647-131">Uzskaites un pārskata valūtu izmaiņas tiek izplatītas.</span><span class="sxs-lookup"><span data-stu-id="fb647-131">Changes to the accounting and reporting currencies are pervasive.</span></span> <span data-ttu-id="fb647-132">Tās ietekmē ne tikai virsgrāmatu, bet arī visas apakšvirsgrāmatas (Debitori, Kreditori, Krājumi, Projekts un citas apakšvirsgrāmatas), visus neatkarīgo programmatūras izstrādātāju (independent software vendor — ISV) risinājumus un visus izveidotos paplašinājumus, kuros tiek glabātas summas.</span><span class="sxs-lookup"><span data-stu-id="fb647-132">They affect not only General ledger but also every subledger (Accounts receivable, Accounts payable, Inventory, Project, and so on), every independent software vendor (ISV) solutions, and any extension that you've made that stores amounts.</span></span>

<span data-ttu-id="fb647-133">Katras summas atrašanas un tulkošanas process uz citu valūtu ir pakļauts kļūdas riskam.</span><span class="sxs-lookup"><span data-stu-id="fb647-133">The process of finding and translating each amount to a different currency is subject to error.</span></span> <span data-ttu-id="fb647-134">Tādēļ inženieru grupa neapstiprinās skriptu, kas maina vai pievieno uzskaites un pārskata valūtas.</span><span class="sxs-lookup"><span data-stu-id="fb647-134">Therefore, the engineering team won't approve a script that changes or adds accounting and reporting currencies.</span></span> <span data-ttu-id="fb647-135">Turklāt, lai gan rīks, kas agrāk bija pieejams risinājumā Microsoft Dynamics AX 2012, sniedza iespēju mainīt vai pievienot uzskaites un pārskata valūtas, šis rīks tika atzīts par novecojušu risinājumam AX 2012 R3 un Finance.</span><span class="sxs-lookup"><span data-stu-id="fb647-135">Additionally, although a tool that used to be available for Microsoft Dynamics AX 2012 let you change or add accounting and reporting currencies, that tool was deprecated for both AX 2012 R3 and Finance.</span></span>

<span data-ttu-id="fb647-136">Veiciet šīs darbības, lai kopētu iestatījumu datus un pamatdatus no pašreizējās juridiskās personas uz jaunu juridisku personu.</span><span class="sxs-lookup"><span data-stu-id="fb647-136">Follow these steps to copy the setup and master data from the current legal entity to a new legal entity.</span></span>

1. <span data-ttu-id="fb647-137">Dodieties uz **Darbvietas \> Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="fb647-137">Go to **Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="fb647-138">Grupā **Importēšana/eksportēšana** atlasiet **Veidnes**.</span><span class="sxs-lookup"><span data-stu-id="fb647-138">Select **Templates** under the **Import/Export** group.</span></span>
3. <span data-ttu-id="fb647-139">Pārliecinieties, vai veidnes ir pieejamas.</span><span class="sxs-lookup"><span data-stu-id="fb647-139">Make sure that templates are available.</span></span> <span data-ttu-id="fb647-140">Ja veidnes nav pieejamas, atlasiet **Ielādēt noklusējuma veidnes** un uzgaidiet, līdz veidnes tiek ģenerētas.</span><span class="sxs-lookup"><span data-stu-id="fb647-140">If no templates are available, select **Load default templates**, and wait for the templates to be generated.</span></span>
4. <span data-ttu-id="fb647-141">Atgriezieties darbvietā **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="fb647-141">Return to the **Data management** workspace.</span></span>
5. <span data-ttu-id="fb647-142">Atlasiet **Kopēt juridiskajā personā**.</span><span class="sxs-lookup"><span data-stu-id="fb647-142">Select **Copy into legal entity**.</span></span>
6. <span data-ttu-id="fb647-143">Ievadiet grupas nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="fb647-143">Enter a group name and description.</span></span>
7. <span data-ttu-id="fb647-144">Laukā **Avota juridiskā persona** atlasiet juridisko personu, no kuras kopēt datus.</span><span class="sxs-lookup"><span data-stu-id="fb647-144">In the **Source legal entity** field, select the legal entity to copy data from.</span></span>
8. <span data-ttu-id="fb647-145">Kopsavilkuma cilnē **Mērķa juridiskās personas** atlasiet **Izveidot juridiskās personas**, lai izveidotu jaunu juridisko personu, kurā varat kopēt avota juridiskās personas datus.</span><span class="sxs-lookup"><span data-stu-id="fb647-145">In the **Destination legal entities** FastTab, select **Create legal entities** to create a new legal entity that you can copy the source legal entity data to.</span></span> <span data-ttu-id="fb647-146">Atlasiet **Atlasīt esošu**, lai kopētu datus esošā juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="fb647-146">Select **Select existing** to copy data to an existing legal entity.</span></span>
9. <span data-ttu-id="fb647-147">Neobligāti: laukā **Kopēt skaitļu virknes** norādiet vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="fb647-147">Optional: Set the **Copy number sequences** field to **Yes**.</span></span> <span data-ttu-id="fb647-148">(Šī darbība ir ieteicama, kopējot datus.)</span><span class="sxs-lookup"><span data-stu-id="fb647-148">(This step is recommended when you copy data.)</span></span>
10. <span data-ttu-id="fb647-149">Apgabalā **Atlasītie elementi** atlasiet **Pievienot veidni**.</span><span class="sxs-lookup"><span data-stu-id="fb647-149">In the **Selected entities** area, select **Add template**.</span></span>
11. <span data-ttu-id="fb647-150">Atlasiet veidnes, ko izmantot.</span><span class="sxs-lookup"><span data-stu-id="fb647-150">Select the templates to use.</span></span> <span data-ttu-id="fb647-151">Ieteicamās veidnes jaunai juridiskajai personai iever **025 — Virsgrāmata** un **Finanses**.</span><span class="sxs-lookup"><span data-stu-id="fb647-151">Suggested templates for a new legal entity include **025 - General Ledger** and **Financials**.</span></span> <span data-ttu-id="fb647-152">Ieteicams pārskatīt visas pārējās pieejamās veidnes, lai noteiktu, vai kāda no tām attiecas uz jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="fb647-152">We recommend that you review all the other available templates to determine whether any of them apply to your requirements.</span></span>
12. <span data-ttu-id="fb647-153">Atlasiet **Kopēt juridiskajā personā**, lai sāktu pakešveida apstrādi, kas izveidos atlasītos elementus un kopēs tos mērķa juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="fb647-153">Select **Copy into legal entity** to start a batch process that will create the selected entities and copy them into the destination legal entity.</span></span>
13. <span data-ttu-id="fb647-154">Kad process ir pabeigts, bet pirms kāda transakcija ir iegrāmatota, dodieties uz virsgrāmatu un atjauniniet uzskaites un pārskata valūtas, kā aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="fb647-154">After the process is completed, but before any transaction are posted, go to the ledger, and update the accounting and reporting currencies as described earlier in this topic.</span></span>

<span data-ttu-id="fb647-155">Ja izveidojāt jaunu juridisku personu, lai varētu mainīt uzskaites vai pārskata valūtu, pārbaudiet, vai sākuma bilances tiek pārrēķinātas no iepriekšējās juridiskās personas valūtām uz jaunajām valūtām.</span><span class="sxs-lookup"><span data-stu-id="fb647-155">If you created a new legal entity so that you can change the accounting or reporting currency, verify that the beginning balances are translated from the currencies of the old legal entity to the new currencies.</span></span>

<span data-ttu-id="fb647-156">Video, kurā parādītas iepriekšējās darbības, skatiet vietnē [Kopēšana juridiskajā personā](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span><span class="sxs-lookup"><span data-stu-id="fb647-156">For a video that shows the preceding steps, see [Copy Into Legal Entity](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span></span>