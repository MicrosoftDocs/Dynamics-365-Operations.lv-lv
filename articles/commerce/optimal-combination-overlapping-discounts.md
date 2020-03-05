---
title: Optimālās pārklāto atlaižu kombinācijas noteikšana
description: Ja atlaides pārklājas, ir jānosaka pārklāto atlaižu kombinācija, kas rada vismazāko transakcijas kopsummu vai lielāko kopējo atlaidi. Ja atlaides summa mainās atbilstoši nopirkto preču cenai, piemēram, parastās mazumtirdzniecības atlaides “pērc 1, saņem 1 X procentu atlaidi” (BOGO) gadījumā, šim procesam ir jāveic kombināciju optimizēšana.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount,
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 565722da65cbb711acedb5acf7de4edfbd615314
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023347"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a><span data-ttu-id="8ae1b-104">Optimālās pārklāto atlaižu kombinācijas noteikšana</span><span class="sxs-lookup"><span data-stu-id="8ae1b-104">Determine the optimal combination of overlapping discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ae1b-105">Ja atlaides pārklājas, ir jānosaka pārklāto atlaižu kombinācija, kas rada vismazāko transakcijas kopsummu vai lielāko kopējo atlaidi.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-105">When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</span></span> <span data-ttu-id="8ae1b-106">Ja atlaides summa mainās atbilstoši nopirkto preču cenai, piemēram, parastās mazumtirdzniecības atlaides “pērc 1, saņem 1 X procentu atlaidi” (BOGO) gadījumā, šim procesam ir jāveic kombināciju optimizēšana.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-106">When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</span></span>

<span data-ttu-id="8ae1b-107">Šis raksts attiecas uz programmu Microsoft Dynamics AX 2012 R3 ar KB 3105973 (2015. gada 2. novembra laidiens) vai jaunāku tās versiju un programmu Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-107">This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Dynamics 365 Commerce.</span></span> <span data-ttu-id="8ae1b-108">Lai noteiktu kombinācijas atlaides, kas pārklājas, un tās laicīgi piemērotu, esam ieviesuši metodi, kā lietot atlaides, kas pārklājas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-108">To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</span></span> <span data-ttu-id="8ae1b-109">Šī metode tiek dēvēta par **robežvērtības ranžēšanu**.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-109">We call this new method **marginal value ranking**.</span></span> <span data-ttu-id="8ae1b-110">Robežvērtības ranžēšana tiek izmantota, ja iespējamo pārklāto atlaižu kombināciju novērtēšanai nepieciešamais laiks pārsniedz sliekšņvērtību, ko var konfigurēt lapā **Commerce parametri**.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-110">Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the **Commerce parameters** page.</span></span> <span data-ttu-id="8ae1b-111">Robežvērtības ranžēšanas metodes ietvaros tiek aprēķināta katras pārklātās atlaides vērtība, izmantojot kopīgo preču atlaides vērtību.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-111">In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</span></span> <span data-ttu-id="8ae1b-112">Pēc tam pārklātās atlaides tiek lietotas secībā no lielākās relatīvās vērtības līdz mazākajai relatīvajai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-112">The overlapped discounts are then applied from the highest relative value to the lowest relative value.</span></span> <span data-ttu-id="8ae1b-113">Detalizētu informāciju par jauno metodi skatiet sadaļā “Robežvērtība” šī raksta turpinājumā.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-113">For details about the new method, see the "Marginal value" section, later in this article.</span></span> <span data-ttu-id="8ae1b-114">Robežvērtības ranžēšana netiek lietota, ja citas transakcijā ietvertās preces neietekmē preces atlaides summas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-114">Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</span></span> <span data-ttu-id="8ae1b-115">Piemēram, šī metode netiek lietota divām parastajām atlaidēm vai parastajai atlaidei un vienas preces daudzuma atlaidei.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-115">For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</span></span>

## <a name="discount-examples"></a><span data-ttu-id="8ae1b-116">Atlaižu piemēri</span><span class="sxs-lookup"><span data-stu-id="8ae1b-116">Discount examples</span></span>

<span data-ttu-id="8ae1b-117">Vienai preču kopai varat izveidot neierobežotu skaitu atlaižu.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-117">You can create an unlimited number of discounts on a common set of products.</span></span> <span data-ttu-id="8ae1b-118">Taču, tā kā nepastāv nekāds ierobežojums, mēģinot aprēķināt dažādām precēm lietojamās atlaides, var rasties veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-118">However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</span></span> <span data-ttu-id="8ae1b-119">Tālāk sniegtajā piemērā ir detalizētāk atainota šī problēma.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-119">The following examples illustrate this issue in more detail.</span></span> <span data-ttu-id="8ae1b-120">1. piemēra ietvaros tiek apstrādātas divas preces un divas pārklātas atlaides.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-120">In example 1, we start with two products and two overlapping discounts.</span></span> <span data-ttu-id="8ae1b-121">2. piemērā ir atainots, kā problēma attīstās, ja tiek pievienotas papildu preces.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-121">Then, in example 2, we show how the issue evolves as more products are added.</span></span>

### <a name="example-1-two-products-and-two-discounts"></a><span data-ttu-id="8ae1b-122">1. piemērs: divas preces un divas atlaides</span><span class="sxs-lookup"><span data-stu-id="8ae1b-122">Example 1: Two products and two discounts</span></span>

<span data-ttu-id="8ae1b-123">Šī piemēra ietvaros, lai varētu saņemt katru atlaidi, ir nepieciešamas divas preces, un atlaides nevar kombinēt.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-123">In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</span></span> <span data-ttu-id="8ae1b-124">Piemēra ietvaros izmantoto atlaižu veids ir **Labākā cena**.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-124">The discounts in this example are **Best price** discounts.</span></span> <span data-ttu-id="8ae1b-125">Abas preces ir piemērotas abām atlaidēm.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-125">Both products qualify for both discounts.</span></span> <span data-ttu-id="8ae1b-126">Tālāk ir norādītas abas atlaides.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-126">Here are the two discounts.</span></span>

![Divu labāko cenas atlaižu piemērs](./media/overlapping-discount-combo-01.jpg)

<span data-ttu-id="8ae1b-128">Jebkurām divām precēm labākā no šīm divām atlaidēm ir atkarīga no abu preču cenas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-128">For any two products, the better of these two discounts depends on the prices of the two products.</span></span> <span data-ttu-id="8ae1b-129">Ja abu preču cenas ir vienādas vai gandrīz vienādas, 1. atlaide ir labāka.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-129">When the price of both products is equal or almost equal, discount 1 is better.</span></span> <span data-ttu-id="8ae1b-130">Ja vienas preces cena ir daudz mazāka par otras preces cenu, 2. atlaide ir labāka.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-130">When the price of one product is significantly less than the price of the other product, discount 2 is better.</span></span> <span data-ttu-id="8ae1b-131">Lūk, matemātiskā kārtula šo divu atlaižu savstarpējai novērtēšanai.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-131">Here is the mathematical rule for evaluating these two discounts against each other.</span></span>

![Kārtula atlaižu novērtēšanai](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> <span data-ttu-id="8ae1b-133">Kad 1. preces cena ir vienāda ar divām trešdaļām no 2. preces cenas, tad abas atlaides ir vienādas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-133">When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</span></span> <span data-ttu-id="8ae1b-134">Šī piemēra ietvaros 1. atlaides faktiskā procentuālā vērtība mainās diapazonā no dažiem procentiem (ja abu preču cenas ļoti atšķiras) līdz 25 procentiem (ja abu preču cenas ir vienādas).</span><span class="sxs-lookup"><span data-stu-id="8ae1b-134">In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</span></span> <span data-ttu-id="8ae1b-135">2. atlaides faktiskā procentuālā vērtība ir nemainīga.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-135">The effective discount percentage for discount 2 is fixed.</span></span> <span data-ttu-id="8ae1b-136">Tā vienmēr ir 20 procenti.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-136">It's always 20 percent.</span></span> <span data-ttu-id="8ae1b-137">Tā kā 1. atlaides faktiskā procentuālā vērtība var būt lielāka vai mazāka nekā 2. atlaide, tas, labākā atlaide ir atkarīga no abu preču cenas pirms atlaides lietošanas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-137">Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</span></span> <span data-ttu-id="8ae1b-138">Šī piemēra ietvaros aprēķinu var veikt ātri, jo tiek lietotas tikai divas atlaides un tikai divām precēm.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-138">In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</span></span> <span data-ttu-id="8ae1b-139">Pastāv tikai divas iespējamās kombinācijas: viens 1. atlaides lietojums vai viens 2. atlaides lietojums.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-139">There are only two possible combinations: one application of discount 1 or one application of discount 2.</span></span> <span data-ttu-id="8ae1b-140">Nav jāaprēķina nekādas permutācijas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-140">There are no permutations to calculate.</span></span> <span data-ttu-id="8ae1b-141">Katras atlaides vērtība tiek aprēķināta, izmantojot abas preces, un tiek lietota labākā atlaide.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-141">The value of each discount is calculated by using both products, and the best discount is used.</span></span>

### <a name="example-2-four-products-and-two-discounts"></a><span data-ttu-id="8ae1b-142">2. piemērs: četras preces un divas atlaides</span><span class="sxs-lookup"><span data-stu-id="8ae1b-142">Example 2: Four products and two discounts</span></span>

<span data-ttu-id="8ae1b-143">Turpinājumā tiek lietotas četras preces un tās pašas divas atlaides.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-143">Next, we will use four products and the same two discounts.</span></span> <span data-ttu-id="8ae1b-144">Visas četras preces ir piemērotas abām atlaidēm.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-144">All four products qualify for both discounts.</span></span> <span data-ttu-id="8ae1b-145">Pastāv divpadsmit iespējamās kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-145">There are twelve possible combinations.</span></span> <span data-ttu-id="8ae1b-146">Piemēra beigās transakcijai tiek lietotas divas atlaides vienā no trim kombinācijām: divi 1. atlaides lietojumi, divi 2. atlaides lietojumi vai viens 1. atlaides un viens 2. atlaides lietojums.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-146">In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</span></span> <span data-ttu-id="8ae1b-147">Lai atainotu iespējamās kombinācijas, tiek aplūkotas divas dažādas četru preču kopas ar dažādām cenām.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-147">To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</span></span>

- <span data-ttu-id="8ae1b-148">Visām četrām precēm ir viena cena $ 15,00.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-148">All four products have the same price, $15.00.</span></span> <span data-ttu-id="8ae1b-149">Šādā gadījumā labākā atlaižu kombinācija ir divi 1. atlaides lietojumi.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-149">In this case, the best discount combination is two applications of discount 1.</span></span> <span data-ttu-id="8ae1b-150">Divām precēm ir pilna cena, un divām ir 50 procentu atlaide.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-150">Two products will be full price, and two will be 50 percent off.</span></span> <span data-ttu-id="8ae1b-151">Transakcijas kopsumma ar atlaidi ir $ 45 (15 + 15 + 7,50 + 7,50), kas ir par $ 15 (25 procentiem) mazāka nekā kopsumma bez atlaides $ 60.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-151">The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</span></span> <span data-ttu-id="8ae1b-152">2. atlaide ir tikai $ 12 (20 procenti).</span><span class="sxs-lookup"><span data-stu-id="8ae1b-152">Discount 2 is only $12 (20 percent).</span></span>
- <span data-ttu-id="8ae1b-153">Divas preces maksā $ 20 katra, viena prece maksā $ 15 un viena prece maksā $ 5.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-153">Two products are $20 each, one product is $15, and one product is $5.</span></span> <span data-ttu-id="8ae1b-154">Šādā gadījumā labākā atlaižu kombinācija ir viens 2. atlaides lietojums un viens 1. atlaides lietojums.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-154">In this case, the best discount combination is one application of discount 2 and one application of discount 1.</span></span> <span data-ttu-id="8ae1b-155">Tālāk esošajās tabulās ir norādītas atlaides.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-155">The following tables illustrates the discounts.</span></span>

<span data-ttu-id="8ae1b-156">Lai nolasītu tabulās sniegto informāciju, izmantojiet vienu preci no rindas un vienu preci no kolonnas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-156">To read the tables, use one product from a row and one product from a column.</span></span> <span data-ttu-id="8ae1b-157">Piemēram, 1. atlaides tabulā, kombinējot divas preces ar cenu $ 20, iegūstat atlaidi $ 10.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-157">For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</span></span> <span data-ttu-id="8ae1b-158">2. atlaides tabulā, kombinējot preci ar cenu $ 15 un preci ar cenu $ 5, iegūstat atlaidi $ 4.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-158">In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</span></span>

![Piemērs, kur ir izmantotas četras preces tām pašam divām atlaidēm](./media/overlapping-discount-combo-03.jpg)

<span data-ttu-id="8ae1b-160">Vispirms ir jānosaka vislielākā atlaide, ko var iegūt jebkurām divām precēm, lietojot jebkuru atlaidi.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-160">First, we find the largest discount that is available from any two products by using either discount.</span></span> <span data-ttu-id="8ae1b-161">Divās tabulās ir norādītas atlaides summas visām divi preču kombinācijām.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-161">The two tables show the discount amount for all combinations of the two products.</span></span> <span data-ttu-id="8ae1b-162">Tabulu kopējās daļas atbilst gadījumiem, kad prece tiek kombinēta pati ar sevi, kas nav iespējams, vai divu preču apgrieztajai kombinēšanai, kas rada tādu pašu atlaides summu un ko var ignorēt.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-162">The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</span></span> <span data-ttu-id="8ae1b-163">Aplūkojot tabulas, varat konstatēt, ka 1. atlaide divām precēm ar cenu $ 20 ir lielākā atlaide, kas ir pieejama, lietojot jebkuru atlaidi visām četrām precēm.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-163">By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</span></span> <span data-ttu-id="8ae1b-164">(Šī atlaide pirmajā tabulā ir iezīmēta zaļā krāsā.) Tādējādi atliek tikai prece ar cenu $ 15 un prece ar cenu $ 5.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-164">(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</span></span> <span data-ttu-id="8ae1b-165">Vēlreiz aplūkojot abas tabulas, varat konstatēt, ka, šīm divām precēm lietojot 1. atlaidi, tiek iegūta atlaide $ 2,50, bet, tām lietojot 2. atlaidi, tiek iegūta atlaide $ 4.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-165">By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</span></span> <span data-ttu-id="8ae1b-166">Tāpēc tiek izvēlēta 2. atlaide.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-166">Therefore, we select discount 2.</span></span> <span data-ttu-id="8ae1b-167">Kopējā atlaide ir $ 14.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-167">The total discount is $14.</span></span> <span data-ttu-id="8ae1b-168">Lai atvieglotu šī piemēra vizualizēšanu, tālāk ir sniegtas divas papildu tabulas, kurās ir redzamas visu iespējamo divu preču kombināciju faktiskās atlaides procentuālās vērtības gan 1., gan 2. atlaidei.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-168">To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</span></span> <span data-ttu-id="8ae1b-169">Ir ietverta tikai puse no kombināciju saraksta, jo šīm divām atlaidēm nav svarīgi, kādā secībā abām precēm tiek lietota atlaide.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-169">Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</span></span> <span data-ttu-id="8ae1b-170">Lielākā faktiskā atlaide (25 procenti) ir iezīmēta zaļā krāsā, un mazākā faktiskā atlaide (10 procenti) ir iezīmēta sarkanā krāsā.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-170">The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</span></span>

![Faktiskās atlaides procentuālais daudzums visām divu preču kombinācijām abām atlaidēm](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> <span data-ttu-id="8ae1b-172">Ja cenas atšķiras un ir jāsalīdzina divas atlaides vai vairāk, vienīgais veids, kā garantēt vislabākās atlaižu kombinācijas izvēli, ir novērtēt abas atlaides un tās salīdzināt.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-172">When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</span></span>

## <a name="total-possible-combinations"></a><span data-ttu-id="8ae1b-173">Visas iespējamās kombinācijas</span><span class="sxs-lookup"><span data-stu-id="8ae1b-173">Total possible combinations</span></span>

<span data-ttu-id="8ae1b-174">Šajā sadaļā tiek turpināts iepriekšējā sadaļā apskatītais piemērs.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-174">This section continues the example from the previous section.</span></span> <span data-ttu-id="8ae1b-175">Tiek pievienotas papildu preces un vēl viena atlaide un noteikts, cik daudz kombināciju ir jāaprēķina un jāsalīdzina.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-175">We will add more products and another discount, and see how many combinations must be calculated and compared.</span></span> <span data-ttu-id="8ae1b-176">Tālāk esošajā tabulā ir norādīts iespējamo atlaižu kombināciju skaits atbilstoši preču daudzuma palielinājumam.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-176">The following table shows the number of possible discount combinations as the product quantity increases.</span></span> <span data-ttu-id="8ae1b-177">Tabulā ir atainots divu pārklātu atlaižu gadījums, kā tas ir aprakstīts iepriekšējā piemērā, fan trīs pārklātu atlaižu gadījums.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-177">The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</span></span> <span data-ttu-id="8ae1b-178">Novērtējamo iespējamo atlaižu kombināciju skaits drīz vien kļūst tik liels, ka pat ātrdarbīgs dators nespēj veikt aprēķinu un salīdzinājumu tik ātri, cik ir vajadzīgs, strādājot ar mazumtirdzniecības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-178">The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</span></span>

![Iespējamo atlaižu kombināciju skaits, palielinoties preču daudzumam](./media/overlapping-discount-combo-05.jpg)

<span data-ttu-id="8ae1b-180">Ja tiek lietots vēl lielāks daudzums vai vēl vairāk pārklāto atlaižu, tad kopējais iespējamo atlaižu kombināciju skaits drīz vien sasniedz miljonus, un kombināciju novērtēšanai un vislabākās iespējamās kombinācijas izvēlei drīz vien ir vajadzīgs daudz ilgāks laiks.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-180">When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</span></span> <span data-ttu-id="8ae1b-181">Cenas noteikšanas programmā ir veiktas dažas optimizācijas, lai samazinātu novērtējamo kombināciju skaitu.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-181">Some optimizations have been done in the price engine to reduce the total number of combinations that must be evaluated.</span></span> <span data-ttu-id="8ae1b-182">Taču, tā kā pārklāto atlaižu skaits un transakcijās ietvertais daudzums nav ierobežots, vienmēr, kad pastāv pārklātās atlaides, ir jānovērtē ļoti daudz kombināciju.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-182">However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</span></span> <span data-ttu-id="8ae1b-183">Šo problēmu palīdz novērst robežvērtības ranžēšanas metode.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-183">This issue is the issue that the marginal value ranking method addresses.</span></span>

## <a name="marginal-value-method"></a><span data-ttu-id="8ae1b-184">Robežvērtības metode</span><span class="sxs-lookup"><span data-stu-id="8ae1b-184">Marginal value method</span></span>

<span data-ttu-id="8ae1b-185">Lai novērstu eksponenciāli pieaugošā novērtējamo kombināciju daudzuma problēmu, ir pieejama optimizācijas metode, kas nodrošina katras atlaides vērtības aprēķināšanu katrai kopīgajai precei preču kopā, kurai var lietot divas atlaides vai vairāk.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-185">To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</span></span> <span data-ttu-id="8ae1b-186">Šī vērtība tiek dēvēta par kopīgo preču atlaides **robežvērtību**.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-186">We refer to this value as the **marginal value** of the discount for the shared products.</span></span> <span data-ttu-id="8ae1b-187">Robežvērtība ir vidējais kopējās atlaides summas palielinājums katrai precei, lietojot kopīgajām precēm katru atlaidi.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-187">The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</span></span> <span data-ttu-id="8ae1b-188">Robežvērtība tiek aprēķināta, aprēķinot kopējo atlaides summu (DTotal), atņemot atlaides summu bez kopīgajām precēm (DMinus\\ Shared) un dalot iegūto starpību ar kopīgo preču skaitu (ProductsShared).</span><span class="sxs-lookup"><span data-stu-id="8ae1b-188">The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus\\ Shared), and dividing that difference by the number of shared products (ProductsShared).</span></span>

![Formula robežvērtības aprēķināšanai](./media/overlapping-discount-combo-06.jpg)

<span data-ttu-id="8ae1b-190">Kad ir aprēķināta katras atlaides robežvērtība kopīgo preču kopā, tad kopīgajām precēm tiek lietotas visas atlaides secībā no lielākās robežvērtības līdz mazākajai robežvērtībai.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-190">After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</span></span> <span data-ttu-id="8ae1b-191">Šīs metodes ietvaros ikreiz pēc atsevišķas atlaides instances lietošanas netiek salīdzinātas visas atlikušās atlaižu iespējas.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-191">For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</span></span> <span data-ttu-id="8ae1b-192">Tā vietā tiek vienu reizi salīdzinātas pārklātās atlaides, kas pēc tam tiek lietotas noteiktajā secībā.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-192">Instead, the overlapping discounts are compared one time and then applied in order.</span></span> <span data-ttu-id="8ae1b-193">Netiek veikta papildu salīdzināšana.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-193">No additional comparisons are done.</span></span> <span data-ttu-id="8ae1b-194">Sliekšņvērtību programmatūras pārslēgšanai uz robežvērtības metodi varat konfigurēt lapas **Commerce parametri** cilnē **Atlaide**.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-194">You can configure the threshold to switch to the marginal value method on the **Discount** tab of the **Commerce parameters** page.</span></span> <span data-ttu-id="8ae1b-195">Pieņemamais kopējās atlaides parēķina laiks atšķirtas dažādās mazumtirdzniecības nozarēs.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-195">The acceptable time to calculate the total discount varies across retail industries.</span></span> <span data-ttu-id="8ae1b-196">Taču parasti šis laiks ir no dažiem desmitiem milisekunžu līdz vienai sekundei.</span><span class="sxs-lookup"><span data-stu-id="8ae1b-196">However, this time generally falls in the range of tens of milliseconds to one second.</span></span>