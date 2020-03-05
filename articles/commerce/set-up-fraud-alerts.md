---
title: Zvanu centra pārkāpumu brīdinājumu iestatīšana un darbs ar tiem
description: Šajā tēmā izskaidrots, kā iestatīt kārtulas, lai brīdinātu klientu apkalpošanas pārstāvjus par potenciāli krāpniecisku informāciju, kad tiek apstrādāti pasūtījumi. Var definēt īpašus kodus, kas tiek izmantoti, lai automātiski vai manuāli aizturētu aizdomīgus pasūtījumus.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b4ee6b128e473d0999885f1cb1b4dbb015026c4e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023304"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a><span data-ttu-id="c9b6b-104">Zvanu centra pārkāpumu brīdinājumu iestatīšana un darbs ar tiem</span><span class="sxs-lookup"><span data-stu-id="c9b6b-104">Set up and work with call center fraud alerts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c9b6b-105">Šajā tēmā ir paskaidrots, kā iestatīt kritērijus un kārtulas, lai aizturētu potenciāli krāpnieciskus pārdošanas pasūtījumus turpmākai pārskatīšanai.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-105">This topic explains how to set up criteria and rules to put potentially fraudulent sales orders on hold for further review.</span></span> <span data-ttu-id="c9b6b-106">Pārkāpumu pārbaudes līdzeklis tiek izmantots, lai noteiktu pārdošanas pasūtījumā ietvertās informācijas derīgumu.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-106">The fraud check feature is used to determine the validity of the information in a sales order.</span></span> <span data-ttu-id="c9b6b-107">Ja, pamatojoties uz organizācijas pārkāpumu kritērijiem un kārtulām, pārdošanas pasūtījumā ietvertā informācija tiek atzīta par apšaubāmu, pasūtījumu var aizturēt turpmākai pārskatīšanai.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-107">If the information in the sales order appears to be questionable, based on an organization's fraud criteria and rules, the order can be put on hold for further review.</span></span> <span data-ttu-id="c9b6b-108">Šajā gadījumā pasūtījumu nevar nosūtīt uz noliktavu turpmākai apstrādei, līdz aizturēšana ir dzēsta.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-108">In this case, the order can't be released to the warehouse for further processing until the hold has been cleared.</span></span>

> [!NOTE]
> <span data-ttu-id="c9b6b-109">Šo līdzekli var lietot tikai ar pārdošanas pasūtījumu apstrādi Commerce zvanu centra kanālam.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-109">This feature can be used only with sales order processing for the Commerce call center channel.</span></span>

## <a name="turning-on-the-fraud-check-feature"></a><span data-ttu-id="c9b6b-110">Pārkāpumu pārbaudes līdzekļa ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="c9b6b-110">Turning on the fraud check feature</span></span>

<span data-ttu-id="c9b6b-111">Lai izmantotu pārkāpumu pārbaudes līdzekli, kanāla opcijai **Iespējot pasūtījuma pabeigšanu** ir jāiestata vienums **Jā**, kad zvanu centra kanāls ir [definēts](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options).</span><span class="sxs-lookup"><span data-stu-id="c9b6b-111">To use the fraud check feature, you must set the **Enable order completion** option on the channel to **Yes** when the call center channel is [defined](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options).</span></span> <span data-ttu-id="c9b6b-112">Kad ir ieslēgta pasūtījuma pabeigšana, zvanu centra lietotājiem ir jāatlasa vienums **Pabeigt** pārdošanas pasūtījumu lapā visiem izveidotajiem pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-112">When order completion is turned on, call center users must select **Complete** on the sales order page for all sales orders that are created.</span></span> <span data-ttu-id="c9b6b-113">Pabeigšanas darbība atver lapu **Pārdošanas pasūtījumu kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-113">The Complete action causes the **Sales order summary** page to open.</span></span> <span data-ttu-id="c9b6b-114">Pēc tam, kad lietotāji ievada nepieciešamos maksājuma datus lapā **Pārdošanas pasūtījumu kopsavilkums**, viņi atlasa vienumu **Iesniegt**, lai pabeigtu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-114">After users enter the required payment data on the **Sales order summary** page, they select **Submit** to finalize the order.</span></span> <span data-ttu-id="c9b6b-115">Kad pasūtījums ir iesniegts, tiek aktivizēts pārkāpumu pārbaudes līdzeklis, un tiek automātiski pārbaudītas visas sistēmas aktīvās kārtulas.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-115">When the order is submitted, the fraud check feature is triggered, and any rules that are active in the system are automatically validated.</span></span>

<span data-ttu-id="c9b6b-116">Zvanu centra lietotāji var arī manuāli aizturēt pārdošanas pasūtījumus pārkāpumu pārskatīšanai, pirms viņi atlasa vienumu **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-116">Call center users can also manually put sales orders on hold for fraud review before they select **Submit**.</span></span> <span data-ttu-id="c9b6b-117">Lai manuāli aizturētu pārdošanas pasūtījumu, lapā **Pārdošanas pasūtījumu kopsavilkums** atlasiet **Aizturēt** \> **Pārkāpuma dēļ manuāli veiktā aizturēšana**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-117">To manually put a sales order on hold, on the **Sales order summary** page, select **Hold** \> **Manual fraud hold**.</span></span> <span data-ttu-id="c9b6b-118">Pēc tam tiek piedāvāts ievadīt komentāru, lai paskaidrotu pasūtījuma aizturēšanas iemeslu.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-118">You're then prompted to enter a comment to explain your reason for putting the order on hold.</span></span> <span data-ttu-id="c9b6b-119">Šis komentārs parādīsies rīkā [Pasūtījumu aizturēšana](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), lai sniegtu kontekstu lietotājam, kurš pārskata aizturētos pasūtījumus, lai noteiktu, vai pasūtījumu var izlaist.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-119">This comment will appear in the [order holds](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) workbench to provide context to the user who reviews orders that are on hold to determine whether the order should be released.</span></span>

<span data-ttu-id="c9b6b-120">Papildus tam, ka konfigurējat kanāla opciju **Iespējot pasūtījuma pabeigšanu**, ir jākonfigurē pārkāpumu pārbaudes līdzeklis sadaļā Zvanu centra parametri.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-120">In addition to configuring the **Enable order completion** option on the channel, you must configure the fraud check feature in the Call center parameters.</span></span> <span data-ttu-id="c9b6b-121">Dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Zvanu centra parametri**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-121">Go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Call center parameters**.</span></span> <span data-ttu-id="c9b6b-122">Lapas **Zvanu centra parametri** cilnē **Aiztures** iestatiet opcijai **Pārkāpumu pārbaude** vienumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-122">On the **Call center parameters** page, on the **Holds** tab, set the **Fraud check** option to **Yes**.</span></span>

<span data-ttu-id="c9b6b-123">Cilnē **Aiztures** arī jādefinē [aizturēšanas kodi](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), kuri tiks lietoti pasūtījumam, kas tiek manuāli vai automātiski aizturēts pārkāpuma pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-123">On the **Holds** tab, you should also define the [hold codes](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) that will be applied to an order that is either manually or automatically put on hold for fraud review.</span></span> <span data-ttu-id="c9b6b-124">Iestatiet aizturēšanas kodus laukos **Pārkāpuma dēļ manuāli veiktās aizturēšanas kods** un **Pārkāpuma dēļ veiktās aizturēšanas kods**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-124">Set the hold codes in the **Manual fraud hold code** and **Fraud hold code** fields.</span></span> <span data-ttu-id="c9b6b-125">Var būt noderīgi izveidot divus unikālus aizturēšanas kodus, lai lietotāji, kuri strādā ar aizturēšanas rīku, varētu viegli filtrēt un atšķirt automātiskās aiztures no manuālajām aizturēm.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-125">You might find it helpful to create two unique hold codes, so that users who work in the holds workbench can easily filter and distinguish automatic holds from manual holds.</span></span>

<span data-ttu-id="c9b6b-126">Lai pārkāpumu pārbaudes līdzeklis darbotos efektīvi, ir jāiestata arī lauks **Minimālais rezultāts**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-126">For the fraud check feature to work effectively, you must also set the **Minimum score** field.</span></span> <span data-ttu-id="c9b6b-127">Katram pārkāpuma kritērijam un kārtulai, kas ir definēti sistēmā, ir noteikts vērtējums.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-127">Every fraud criterion and rule that is defined in the system has a score.</span></span> <span data-ttu-id="c9b6b-128">Veicot pārdošanas pasūtījuma pārkāpumu pārbaudi, ja tiek konstatēta viena vai vairāku pārkāpumu atbilstība, vērtējumi tiek saskaitīti, iegūstot pasūtījuma kopējo pārkāpumu rezultātu.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-128">When a sales order is checked for fraud matches, if one or more matches are found, the scores are added together to give the order a total fraud score.</span></span> <span data-ttu-id="c9b6b-129">Ja pasūtījuma kopējais pārkāpumu rezultāts pārsniedz vērtību laukā **Minimālais rezultāts**, pasūtījums tiek automātiski aizturēts.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-129">If the total fraud score for an order exceeds the value of the **Minimum score** field, the order is automatically put on hold.</span></span> <span data-ttu-id="c9b6b-130">Pēc izvēles varat lietot citus ar rezultātu saistītos laukus cilnē **Aiztures**, lai definētu e-pasta rezultātu, tālruņa rezultātu, pasta indeksa rezultātu un paplašinātā pasta indeksa rezultātu.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-130">You can optionally use the other score-related fields on the **Holds** tab to define the email score, phone score, ZIP/postal code score, and extended ZIP/postal code score.</span></span> <span data-ttu-id="c9b6b-131">Ja nenorādīsit vērtējumu nevienam no minētajiem statiskajiem pārkāpumu kritērijiem, definējot tos lapā **Statiski pārkāpumu dati**, sistēma tos novērtēs, izmantojot noklusējuma vērtējumu, kuru norādāt lapas **Zvanu centra parametri** cilnē **Aiztures**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-131">If you don't specify a score for any of these static fraud criteria when you define them on the **Static fraud data** page, the system will score them by using the default scores that you specify on the **Holds** tab of the **Call center parameters** page.</span></span>

<span data-ttu-id="c9b6b-132">Visbeidzot, izmantojiet lauku **Pārkāpuma komentāra veids**, lai norādītu dokumenta veidu, kas ir jāizmanto, kad lietotāji ievada komentārus, manuāli aizturot pasūtījumu pārkāpumu pārskatīšanai.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-132">Finally, use the **Fraud comment type** field to specify the document type that should be used when users enter comments when they manually put an order on hold for fraud review.</span></span> <span data-ttu-id="c9b6b-133">Visbiežāk šajā laukā ir iestatīta vērtība **Piezīme**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-133">Most often, this field is set to **Note**.</span></span>

## <a name="defining-fraud-criteria-and-rules"></a><span data-ttu-id="c9b6b-134">Pārkāpumu kritēriju un kārtulu definēšana</span><span class="sxs-lookup"><span data-stu-id="c9b6b-134">Defining fraud criteria and rules</span></span>

<span data-ttu-id="c9b6b-135">Sistēma izmanto divu veidu pārkāpuma kritērijus, lai noteiktu, vai pasūtījums ir jāaiztur pārkāpuma pārskatīšanai.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-135">The system references two types of fraud criteria to determine whether an order should be put on hold for fraud review:</span></span>

- <span data-ttu-id="c9b6b-136">**Statiski pārkāpumu dati** izmanto noteiktu vērtību, piemēram, tālruņa numuru, kas ir iekļauts bloķēto numuru sarakstā, vai e-pasta adresi, kas ir atzīmēta, jo ir zināms, ka tā iepriekš izmantota krāpnieciskām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-136">**Static fraud data** uses a specific value, such as a phone number that has been put on a list of blocked numbers or an email address that has been flagged because it's known to have been used for previous fraudulent transactions.</span></span> <span data-ttu-id="c9b6b-137">Lai iestatītu statiskus pārkāpumu datus, dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Pārkāpums** \> **Statiski pārkāpumu dati**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-137">To set up static fraud data, go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Fraud** \> **Static fraud data**.</span></span> <span data-ttu-id="c9b6b-138">Lapā **Statiski pārkāpumu dati** varat pievienot pārkāpumu kritērijus manuāli vai izmantojot datu importēšanu.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-138">On the **Static fraud data** page, you can add fraud criteria manually or through data import.</span></span> <span data-ttu-id="c9b6b-139">Krāpnieciskajai informācijai ir pievienoti vērtējumi.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-139">Scores are attached to the fraudulent information.</span></span> <span data-ttu-id="c9b6b-140">Ja ir ieslēgts pārkāpumu pārbaudes līdzeklis, katrs ievadītais pārdošanas pasūtījums tiek salīdzināts ar statiskajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-140">If the fraud check feature is turned on, every sales order that is entered is compared to the static data.</span></span> <span data-ttu-id="c9b6b-141">Ja šie dati tiek atrasti debitora norēķinu adresē vai piegādes adresē, kas ir saistīta ar pasūtījuma virsrakstu, vai ja šie dati tiek atrasti piegādes adresēs, kuras ir saistītas ar kādu no pārdošanas pasūtījuma rindām, visu unikālo atbilstību vērtējumi tiek summēti un salīdzināti ar vērtību **Minimālais rezultāts**, lai noteiktu, vai pasūtījums ir jāaiztur.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-141">If the data is found in either the customer's billing address or the delivery address that is linked to the order header, or if the data is found in the delivery addresses that are linked to any of the lines on that sales order, the scores of all unique matches are added together and compared to the **Minimum score** value to determine whether the order should be put on hold.</span></span>
- <span data-ttu-id="c9b6b-142">**Pārkāpumu kārtulas** sastāv no lietotāja definētiem mainīgajiem un nosacījumiem, kuri ir definēti attiecīgajiem mainīgajiem.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-142">**Fraud rules** consist of user-defined variables and the conditions that are defined for those variables.</span></span> <span data-ttu-id="c9b6b-143">Lai izveidotu kārtulas, dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Pārkāpums** \> **Kārtulas**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-143">To create rules, go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Fraud** \> **Rules**.</span></span> <span data-ttu-id="c9b6b-144">Pārkāpumu kārtulas ļauj uzņēmumam konfigurēt sarežģītāku kārtulu kopu, kas var ietvert priekšrakstus **AND** vai **OR**, lai novērtētu vairākus nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-144">Fraud rules let a company configure a more complex rule set that can include **AND** or **OR** statements to evaluate multiple conditions.</span></span> <span data-ttu-id="c9b6b-145">Piemēram, lietotājs vēlas, lai pārkāpumu pārbaudes veikšanai tiktu aizturēti visi pasūtījumi no debitoriem, kuri ietilpst noteiktā debitoru grupā un kuri pasūtījuši noteiktu preci.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-145">For example, a user wants all orders for customers who belong to a specific customer group and who ordered a specific product to be put on hold for fraud review.</span></span> <span data-ttu-id="c9b6b-146">Šajā gadījumā, lapā **Kārtulas** tiek definēti klienta un preces pārbaudes nosacījumi un tiek izmantots nosacījums AND.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-146">In this case, conditions to validate the customer and products are defined on the **Rules** page, and an AND condition is used.</span></span> <span data-ttu-id="c9b6b-147">Pasūtījums tiek aizturēts tikai tad, ja ir spēkā abi nosacījumi un ja attiecīgajai kārtulai piešķirtā rezultāta vērtības ietekmē, pieskaitot citu tādu kārtulu rezultāta vērtību, kurai atbilst pasūtījums, pasūtījuma kopējais pārkāpumu rezultāts pārsniedz vērtību **Minimālais rezultāts**, kas ir definēta lapā **Zvanu centra parametri**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-147">An order is then put on hold only if both conditions are true, and if the score value that is assigned to this rule, plus the score value of any other rules that the order matches, causes the order's total fraud score to exceed the **Minimum score** value that is defined on the **Call center parameters** page.</span></span>

> [!NOTE]
> <span data-ttu-id="c9b6b-148">Vairāku kārtulu vai pārāk sarežģītu kārtulu izmantošana ietekmē sistēmas veiktspēju pārdošanas pasūtījumu iesniegšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-148">Multiple rules or overly complex rules will affect system performance when sales orders are submitted.</span></span> <span data-ttu-id="c9b6b-149">Pārkāpuma pārbaudes līdzeklis nav optimizēts darbam ar lielu statisko pārkāpumu datu ierakstu skaitu un daudzām aktīvajām kārtulām.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-149">The fraud check feature hasn't been optimized to handle a large volume of static fraud data entries and many active rules.</span></span> <span data-ttu-id="c9b6b-150">Atcerieties, ka katra kārtula tiek novērtēta, kad zvanu centra lietotāji atlasa vienumu **Iesniegt** pārdošanas pasūtījuma izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-150">Remember that every rule is evaluated when call center users select **Submit** during sales order entry.</span></span> <span data-ttu-id="c9b6b-151">Kārtulas tiek novērtētas, salīdzinot tās ar pārdošanas pasūtījuma galveni un visām pasūtījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-151">The rules are evaluated against the sales order header and all order lines.</span></span> <span data-ttu-id="c9b6b-152">Jo vairāk kārtulu ir jāapstrādā un jo sarežģītāki ir kārtulu priekšraksti, jo ilgāks laiks ir nepieciešams to apstrādei.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-152">The more rules there are and the more complex the rule statements are, the more time will be required for processing.</span></span> <span data-ttu-id="c9b6b-153">Ja pasūtījumā ir daudz rindu vienumu un ir daudz aktīvo kārtulu un statisko datu ierakstu, automātiskā visu datu pārskatīšana un pārbaude un pārkāpuma vērtējuma aprēķināšana var būtiski pazemināt veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-153">If there are many line items on an order, and many active rules and static data entries, the automatic process of reviewing and validating all the data and calculating a fraud score can have a severe impact on performance.</span></span> <span data-ttu-id="c9b6b-154">Organizācijām, kas lieto šo līdzekli, pirms jebkādu kārtulu vai statisko pārkāpumu kritēriju izmaiņu ieviešanas ražošanas vidē vienmēr ir jāpārbauda pasūtījumu iesniegšanas apstrādes laiks un jāpārliecinās, ka tas ir pieņemams.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-154">Organizations that use this feature should always test and confirm that the processing time for order submission is acceptable before they apply any changes to rules or static fraud criteria to the production environment.</span></span>

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a><span data-ttu-id="c9b6b-155">Pārkāpumu pārbaudes veikšanai aizturētu pasūtījumu identificēšana</span><span class="sxs-lookup"><span data-stu-id="c9b6b-155">Identifying orders that are on hold for fraud review</span></span>

<span data-ttu-id="c9b6b-156">Ja zvanu centra lietotāji iesniedz pārdošanas pasūtījumu, ja pasūtījums atbilst pārkāpumu kritērijiem vai kārtulām un ja rezultāts pārsniedz minimālo vērtību, lietotāji saņem brīdinājuma ziņojumu, kurā norādīts, ka pasūtījums ir aizturēts.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-156">When call center users submit a sales order, if the order matches the fraud criteria or rules, and if the score exceeds the minimum, the users receive a warning message that states that the order has been put on hold.</span></span> <span data-ttu-id="c9b6b-157">Lietotāji var aizvērt šo ziņojumu, jo tas ir tikai informatīvs.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-157">Users can close this message, because it's for informational purposes only.</span></span> <span data-ttu-id="c9b6b-158">Lietotāji pēc izvēles var paziņot šo informāciju debitoram.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-158">Users can optionally communicate this information to the customer.</span></span> <span data-ttu-id="c9b6b-159">Uzņēmumam ir jānosaka procedūra, kas jāievēro lietotājiem šādā situācijā.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-159">The business should determine the protocol that users follow in this situation.</span></span>

<span data-ttu-id="c9b6b-160">Pasūtījums tiek saglabāts, tas tiek atzīmēts ar karodziņu **Neapstrādāt**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-160">The order is saved, but the **Do not process** flag is set on it.</span></span> <span data-ttu-id="c9b6b-161">Šis karodziņš palīdz nodrošināt, ka pasūtījumu nevar nosūtīt uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-161">This flag helps guarantee that the order can't be released to the warehouse.</span></span> <span data-ttu-id="c9b6b-162">Lietotāji jebkurā laikā var apskatīt karodziņa **Neapstrādāt** iestatījumu jebkuram pārdošanas pasūtījumam lapā **Detalizēts statuss**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-162">At any time, users can view the setting of the **Do not process** flag for any sales order on the **Detailed status** page.</span></span> <span data-ttu-id="c9b6b-163">Šo lapu var atvērt no lapām **Visi pārdošanas pasūtījumi** un **Klientu apkalpošana**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-163">This page can be opened from the **All sales order** and **Customer service** pages.</span></span> <span data-ttu-id="c9b6b-164">Sistēma arī atjaunina pasūtījumam vērtību laukā **Detalizēts statuss** iestatot vienumu **Aizturēšanu pārkāpuma dēļ**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-164">The system also updates the value of the **Detailed status** field for the order to **Fraud hold**.</span></span>

<span data-ttu-id="c9b6b-165">Lai skatītu un pārvaldītu pasūtījumus, kas ir aizturēti pārkāpuma pārskatīšanai, dodieties uz **Retail un Commerce** \> **Debitori** \> **Pasūtījumu aizturēšana**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-165">To view and manage the orders that are on hold for fraud review, go to **Retail and Commerce** \> **Customers** \> **Order holds**.</span></span> <span data-ttu-id="c9b6b-166">Lapā **Pasūtījumu aizturēšana** atlasiet ierakstu sarakstā un pēc tam noklikšķiniet uz **Pasūtījuma aizturēšana**, lai atvērtu detalizētāku skatu, kurā ietverta informācija par aizturēšanas iemeslu.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-166">On the **Order holds** page, select an entry in the list, and then click **Order hold** to see a more detailed view that includes information about the reason for the hold.</span></span> <span data-ttu-id="c9b6b-167">Kopsavilkuma cilnē **Detalizēta informācija par pārkāpumu** varat skatīt sistemātiskos pārkāpumu kritērijus, kuriem tika noteikta atbilstība attiecīgā pasūtījuma gadījumā, un izmantotos vērtējumus.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-167">On the **Fraud details** FastTab, you can view the systematic fraud criteria that were found to be a match for the order and the scores that were applied.</span></span> <span data-ttu-id="c9b6b-168">Ja pasūtījums tika aizturēts manuāli, varat pārskatīt visus komentārus, kurus ievadīja lietotājs, kas aizturēja pasūtījumu, apskatot kopsavilkuma cilnes **Piezīmes** sadaļu **Pārkāpuma piezīmes**.</span><span class="sxs-lookup"><span data-stu-id="c9b6b-168">If the order was put on manual hold, you can review any comments that were entered by the user who put the order on hold by looking at the **Fraud notes** section on the **Notes** FastTab.</span></span>

<span data-ttu-id="c9b6b-169">Lai iegūtu vairāk informācijas par to, kā darboties ar pasūtījumu aizturēšanu, skatiet sadaļu [Pasūtījumu aizturēšana](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).</span><span class="sxs-lookup"><span data-stu-id="c9b6b-169">For more information about how to work with hold orders, see [Order holds](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).</span></span>