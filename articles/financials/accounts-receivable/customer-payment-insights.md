---
title: Debitoru maksājumu ieskati (priekšskatījums)
description: Šajā tēmā ir aprakstīts, kā līdzeklis Debitoru maksājumu ieskati var palīdzēt prognozēt, kad rēķins tiks apmaksāts, un kā tas palīdz organizācijām izveidot optimizācijas stratēģijas, kas palielina savlaicīgas apmaksas iespējamību.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "344666"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="a43ff-103">Debitoru maksājumu ieskati (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="a43ff-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="a43ff-104">Šis līdzeklis ir ietverts noteiktas mērķauditorijas laidienā un ir pieejams tikai tiem lietotājiem, kuri ir izvēlējušies privāto priekšskatījumu.</span><span class="sxs-lookup"><span data-stu-id="a43ff-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="a43ff-105">Šis līdzeklis tiks ietverts turpmākā vispārējās pieejamības laidienā.</span><span class="sxs-lookup"><span data-stu-id="a43ff-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="a43ff-106">Pārskats</span><span class="sxs-lookup"><span data-stu-id="a43ff-106">Overview</span></span>

<span data-ttu-id="a43ff-107">Organizācijām bieži ir grūti noteikt, kad debitors apmaksās rēķinus.</span><span class="sxs-lookup"><span data-stu-id="a43ff-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="a43ff-108">Šīs informācijas trūkuma dēļ var tikt izveidotas neprecīzas naudas plūsmas prognozes, neefektīvi iekasēšanas procesi, kā arī pasūtījumi var tikt izdoti debitoriem, kuri var radīt kredītrisku.</span><span class="sxs-lookup"><span data-stu-id="a43ff-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="a43ff-109">Līdzeklis Debitoru maksājumu ieskati (priekšskatījums) rēķina apmaksas prognozei izmanto mašīnmācīšanos.</span><span class="sxs-lookup"><span data-stu-id="a43ff-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="a43ff-110">Šis līdzeklis nodrošina arī optimizācijas stratēģijas, kuras var pielāgot tā, lai maksimāli palielinātu iespēju, ka debitori rēķinus apmaksās savlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="a43ff-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="a43ff-111">Prognozes</span><span class="sxs-lookup"><span data-stu-id="a43ff-111">Predictions</span></span>

<span data-ttu-id="a43ff-112">Maksājumu prognozes ļauj organizācijām uzlabot biznesa procesus, sniedzot iespēju:</span><span class="sxs-lookup"><span data-stu-id="a43ff-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="a43ff-113">viegli identificēt rēķinus, kam tiek prognozēta kavēta apmaksa;</span><span class="sxs-lookup"><span data-stu-id="a43ff-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="a43ff-114">veikt atbilstošus pasākumus, kas palielina iespēju savlaicīgi saņemt samaksu.</span><span class="sxs-lookup"><span data-stu-id="a43ff-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="a43ff-115">Līdzeklis Debitoru maksājumu ieskati (priekšskatījums) rēķina apmaksas prognozei izmanto mašīnmācīšanos.</span><span class="sxs-lookup"><span data-stu-id="a43ff-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="a43ff-116">Šis līdzeklis izmanto vēsturiskos rēķinu, maksājumu un debitoru datus, lai izveidotu mašīnmācīšanās modeli un izmantotu to rēķinu apmaksas prognozēm.</span><span class="sxs-lookup"><span data-stu-id="a43ff-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="a43ff-117">Katram neapmaksātajam rēķinam līdzeklis Debitoru maksājumu ieskati (priekšskatījums) prognozē trīs maksājumu iespējamības:</span><span class="sxs-lookup"><span data-stu-id="a43ff-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="a43ff-118">savlaicīgas maksājuma izpildes iespējamība (nepārsniedzot rēķina apmaksas termiņu);</span><span class="sxs-lookup"><span data-stu-id="a43ff-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="a43ff-119">iespējamība, ka maksājums tiks veikts 30 dienu laikā pēc rēķina apmaksas termiņa;</span><span class="sxs-lookup"><span data-stu-id="a43ff-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="a43ff-120">iespējamība, ka maksājums tiks veikts vēlāk nekā 30 dienu laikā pēc rēķina apmaksas termiņa.</span><span class="sxs-lookup"><span data-stu-id="a43ff-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="a43ff-121">Maksājumu iespējamību var redzēt prognožu sadaļā.</span><span class="sxs-lookup"><span data-stu-id="a43ff-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="a43ff-122">[![Maksājumu prognozes](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="a43ff-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="a43ff-123">Katram rēķinam tiek piešķirta arī ticamākā maksājuma iespējamība, izmantojot kādu no trīs iepriekš definētajām prognozētajām maksājuma iespējamībām.</span><span class="sxs-lookup"><span data-stu-id="a43ff-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="a43ff-124">Scenārijs ar lielāko maksājuma iespējamību ir ticamākais scenārijs.</span><span class="sxs-lookup"><span data-stu-id="a43ff-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="a43ff-125">Pieņemsim, ka rēķinam ir prognoze ar 71 procenta iespējamību savlaicīgai rēķina apmaksai, 13 procentu iespējamība rēķina apmaksai 30 dienu laikā pēc apmaksas termiņa un 16 procentu iespējamība rēķina apmaksai vēlāk nekā 30 dienu laikā pēc apmaksas termiņa.</span><span class="sxs-lookup"><span data-stu-id="a43ff-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="a43ff-126">Saskaņā ar lielāko iespējamību rēķinam ir savlaicīgas apmaksas scenārijs, tādēļ rēķinam tiks atzīmēta savlaicīgas apmaksas iespējamība.</span><span class="sxs-lookup"><span data-stu-id="a43ff-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="a43ff-127">[![Maksājumu prognozes](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="a43ff-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="a43ff-128">Optimizācijas stratēģijas</span><span class="sxs-lookup"><span data-stu-id="a43ff-128">Optimization strategies</span></span>

<span data-ttu-id="a43ff-129">Papildus maksājumu prognozēm līdzeklis Debitoru maksājumu ieskati (priekšskatījums) savlaicīgas apmaksas iespēju palielināšanai var izmantot optimizācijas stratēģijas.</span><span class="sxs-lookup"><span data-stu-id="a43ff-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="a43ff-130">Tās organizācijām sniedz iespēju veikt “Kā būtu, ja” analīzi, lai pielāgotu rēķinu un debitoru parametrus un pēc tam salīdzinātu attiecīgo iespaidu, kas atstāts uz savlaicīgas rēķinu apmaksas iespējamību.</span><span class="sxs-lookup"><span data-stu-id="a43ff-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="a43ff-131">Piemēram, organizācija var vēlēties novērtēt, kādu iespaidu uz savlaicīgu maksājuma izpildi atstāj rēķinu termiņatlaides atjaunināšana.</span><span class="sxs-lookup"><span data-stu-id="a43ff-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="a43ff-132">Kad rēķini ir optimizēti jaunās atlaides izmantošanai, lietotāji var apskatīt atstāto iespaidu, lietojot šo atlaidi attiecīgo rēķinu savlaicīgas apmaksas iespējamībai.</span><span class="sxs-lookup"><span data-stu-id="a43ff-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="a43ff-133">Ja šīs atlaides lietošanas izmaksas ir minimālas, salīdzinot ar savlaicīgas maksājuma saņemšanas priekšrocībām, organizācija var izvēlēties atlasīto atlaidi lietot visiem turpmākajiem neapmaksātajiem pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="a43ff-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="a43ff-134">Pašlaik vienīgā līdzeklī Debitoru maksājumu ieskati (priekšskatījums) pieejamā optimizācijas stratēģija ir atlaide.</span><span class="sxs-lookup"><span data-stu-id="a43ff-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="a43ff-135">[![Optimizētās prognozes](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="a43ff-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="a43ff-136">Kā iegūt līdzekli Debitoru maksājumu ieskati (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="a43ff-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="a43ff-137">Ja vēlaties izmēģināt līdzekli Debitoru maksājumu ieskati (priekšskatījums), sūtiet e-pasta ziņojumu [finanšu ieskatu priekšskatījumu grupai](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a43ff-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="a43ff-138">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="a43ff-138">Privacy Statement</span></span>

<span data-ttu-id="a43ff-139">Priekšskatījumos Amerikas Savienotajās Valstīs tiek glabāti debitoru dati.</span><span class="sxs-lookup"><span data-stu-id="a43ff-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="a43ff-140">Turklāt priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 for Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="a43ff-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
