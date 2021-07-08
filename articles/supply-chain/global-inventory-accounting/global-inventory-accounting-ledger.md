---
title: Globālo krājumu uzskaites virsgrāmata
description: Šajā tēmā aprakstītas Globālās krājumu uzskaites Virsgrāmatas, kas definētas, izmantojot valūtas kombināciju, kalendāru, konvenciju un saistību ar juridisku personu.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273190"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="ef6ef-103">Globālo krājumu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="ef6ef-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="ef6ef-104">Globālajai krājumu uzskaitei ir sava Virsgrāmatu kopa.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="ef6ef-105">Katru reizi, kad ar krājumu saistīta transakcija tiek apstrādāta saistītai juridiskajai personai, sistēma var šo transakciju ņemt vērā jebkurā Globālās krājumu uzskaites Virsgrāmatā, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="ef6ef-106">Virsgrāmata ir debeta un kredīta pasākumu reģistrs.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="ef6ef-107">Šie pasākumi tiek klasificēti, izmantojot izmaksu elementus un apakšgrāmatas kontus.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="ef6ef-108">Globālās krājumu uzskaites Virsgrāmata, kas definēta, izmantojot valūtas kombināciju, kalendāru, konvenciju un saistību ar juridisku personu.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="ef6ef-109">Lai iestatītu Globālās krājumu uzskaites Virsgrāmatas, dodieties uz sadaļu **Globālā krājumu uzskaite \> Iestatīšana \> Virsgrāmatas**.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="ef6ef-110">Katrai Virsgrāmatai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="ef6ef-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="ef6ef-111">**Nosaukums** — ievadiet Virsgrāmatas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="ef6ef-112">**Apraksts** — ievadiet Virsgrāmatas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="ef6ef-113">**Finanšu kalendārs** – norādiet Virsgrāmatas finanšu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="ef6ef-114">**Valūta un maiņas kursa tips** – izmantojiet šīs kopsavilkuma cilnes laukus, lai izvēlētos uzskaites valūtu, ko izmanto Virsgrāmata, un maiņas kursa tipu.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="ef6ef-115">Atlasītā valūta var atšķirties no juridiskās personas lietotās valūtas.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="ef6ef-116">Globālajā krājumu uzskaitē lietotāji var definēt tik daudz Virsgrāmatas izmaksu, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="ef6ef-117">Globālā krājumu uzskaite atbalsta krājumu uzskaiti vairākās valūtās un vairākos novērtējumos.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="ef6ef-118">Iestatiet tālāk minētos laukus:</span><span class="sxs-lookup"><span data-stu-id="ef6ef-118">Set the following fields:</span></span>

    - <span data-ttu-id="ef6ef-119">**Valūta** – atlasiet izmaksu valūtu, kurā tiek uzturētas ar krājumiem saistītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="ef6ef-120">Šīs vērtības ietver krājumu vērtību, pārdoto preču izmaksas, krājumu tranzītā un visus noviržu veidus.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="ef6ef-121">**Maiņas kursa tips** — atlasiet maiņas kursu, kas sistēmai jāizmanto, lai konvertētu darbības summu darbības valūtā un krājumu standarta izmaksas izmaksu valūtā.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="ef6ef-122">**Konvencijas nosaukums** – norādiet konvenciju.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="ef6ef-123">Konvencija ir politiku apkopojums, kas nosaka, kā izmaksas šajā Virsgrāmatā tiks ņemtas vērā.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="ef6ef-124">**Juridiska persona** – Virsgrāmata grāmatos dokumentus, kas grāmatoti atlasītajai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="ef6ef-125">**Primings** - atlasiet, vai krājumu darbības, kas tika izveidotas pirms Virsgrāmatas izveidošanas, ir jāapstrādā saskaņā ar valūtu un konvenciju Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="ef6ef-126">Atlasiet vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="ef6ef-126">Select one of the following values:</span></span>

    - <span data-ttu-id="ef6ef-127">**Aktivizēts** – Virsgrāmatai jāapstrādā darbības, kas tika izveidotas pirms Virsgrāmatas izveides.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="ef6ef-128">**Deaktivizēts** – Virsgrāmatai jāapstrādā tikai tās darbības, kas ir izveidotas pēc Virsgrāmatas izveides.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ef6ef-129">Pēc jaunu dokumentu ievadīšanas **nevarēsit** atgriezties un iestatīt šo lauku.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="ef6ef-130">**Statuss** – sistēma automātiski iestata jauno izveidoto Virsgrāmatu statusu uz *Sagatavot*.</span><span class="sxs-lookup"><span data-stu-id="ef6ef-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
