---
title: Ārējo datu izmantošana naudas plūsmas prognozēs (priekšskatījums)
description: Šajā tēmā ir aprakstītas iestatīšanas darbības, kas jāveic, lai ārējos datus varētu ievadīt vai importēt naudas plūsmas prognozēs.
author: rcarlson
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7d5768a6cb2b3623333fab93a42ac5840e87ec68
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818623"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="cfe92-103">Ārējo datu izmantošana naudas plūsmas prognozēs (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="cfe92-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cfe92-104">Ārējos datus var ievadīt vai importēt naudas plūsmas prognozēs.</span><span class="sxs-lookup"><span data-stu-id="cfe92-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="cfe92-105">Šajā tēmā ir aprakstītas iestatīšanas darbības, kas ir raksturīgas ārējo datu izmantošanai un kas ļauj ārējos datus iekļaut naudas plūsmas prognozē.</span><span class="sxs-lookup"><span data-stu-id="cfe92-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="cfe92-106">Ārējo datu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cfe92-106">External data setup</span></span>

<span data-ttu-id="cfe92-107">Lietojiet cilni **Ārējais avots** lapā **Skaidras naudas plūsmas prognozes iestatījumi** (**Skaidras naudas un bankas pārvaldība \> Skaidras naudas plūsmas prognozēšana**), lai ievadītu iestatījumus, kas atbalsta ārējo datu izmantošanu naudas plūsmas prognozēs.</span><span class="sxs-lookup"><span data-stu-id="cfe92-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="cfe92-108">Papildinformāciju par skaitītāju iestatīšanu skatiet sadaļā [Skaidras naudas plūsmas prognozēšana](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="cfe92-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="cfe92-109">Lai ievadītu ārējos datus naudas plūsmas prognozēm, varat izmantot Atvēršanas Excel programmā pieredzi, lai ievadītu mainītu ārējos datus.</span><span class="sxs-lookup"><span data-stu-id="cfe92-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="cfe92-110">Atlasiet pogu **Ārējie dati** un pēc tam atlasiet opciju **Pievienot ārējos datus** vai **Rediģēt esošos ārējos datus**.</span><span class="sxs-lookup"><span data-stu-id="cfe92-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="cfe92-111">Kad Microsoft Excel fails tiek atvērts, varat ievadīt informāciju šādos laukos:</span><span class="sxs-lookup"><span data-stu-id="cfe92-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="cfe92-112">**Ieraksta ID**</span><span class="sxs-lookup"><span data-stu-id="cfe92-112">**Entry ID**</span></span>
- <span data-ttu-id="cfe92-113">**Apraksts** (nav obligāts)</span><span class="sxs-lookup"><span data-stu-id="cfe92-113">**Description** (optional)</span></span>
- <span data-ttu-id="cfe92-114">**Ārējais avota nosaukums** — atlasiet vienu no vērtībām sarakstā, kuru definējāt, iestatot finanšu ieskatus.</span><span class="sxs-lookup"><span data-stu-id="cfe92-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="cfe92-115">**Juridiska persona**</span><span class="sxs-lookup"><span data-stu-id="cfe92-115">**Legal Entity**</span></span>
- <span data-ttu-id="cfe92-116">**Datums**</span><span class="sxs-lookup"><span data-stu-id="cfe92-116">**Date**</span></span>
- <span data-ttu-id="cfe92-117">**Summa darījuma valūtā**</span><span class="sxs-lookup"><span data-stu-id="cfe92-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="cfe92-118">**Valūtas kods**</span><span class="sxs-lookup"><span data-stu-id="cfe92-118">**Currency Code**</span></span>
- <span data-ttu-id="cfe92-119">**Noklusējuma dimensija** (nav obligāts)</span><span class="sxs-lookup"><span data-stu-id="cfe92-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="cfe92-120">**Dokumenta numurs** (nav obligāts)</span><span class="sxs-lookup"><span data-stu-id="cfe92-120">**Document number** (optional)</span></span>
- <span data-ttu-id="cfe92-121">**Konta numurs** (nav obligāts)</span><span class="sxs-lookup"><span data-stu-id="cfe92-121">**Account number** (optional)</span></span>
- <span data-ttu-id="cfe92-122">**Konta nosaukums** (nav obligāts)</span><span class="sxs-lookup"><span data-stu-id="cfe92-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="cfe92-123">Ārējo datu importēšana, izmantojot datu pārvaldības struktūru</span><span class="sxs-lookup"><span data-stu-id="cfe92-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="cfe92-124">Varat importēt ārējos datus naudas plūsmas prognozēm, izmantojot **datu pārvaldības** darbvietu un elementu, kam ir nosaukums **Naudas plūsmas prognozes ārējā avota ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="cfe92-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="cfe92-125">Ja ir jāpārvieto iestatījumu dati no vienas vides uz citu, ir pieejamas šādas elementu apgabalam nepieciešamās iestatījumu tabulas:</span><span class="sxs-lookup"><span data-stu-id="cfe92-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="cfe92-126">Skaidras naudas plūsmas prognozes ārējā avota iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cfe92-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="cfe92-127">Skaidras naudas plūsmas prognozes ārējā avota juridiskās personas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cfe92-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="cfe92-128">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="cfe92-128">Privacy notice</span></span>
<span data-ttu-id="cfe92-129">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="cfe92-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]