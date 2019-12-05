---
title: Klienta maksājumu ieskati (priekšskatījums)
description: Šī tēma apraksta maksājumu ieskatu iespēju, kas palīdz uzlabot izpratni par atsevišķu debitoru parasto maksājumu praksi un var noteikt apstākļus, kas attaisno to, ka savākšanas procesi tiek sākti agrāk, nekā citkārt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774002"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="758f8-103">Klienta maksājumu ieskati (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="758f8-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="758f8-104">Šī tēma apraksta maksājumu ieskatu iespēju, kas palīdz uzlabot izpratni par atsevišķu debitoru parasto maksājumu praksi un var noteikt apstākļus, kas attaisno to, ka savākšanas procesi tiek sākti agrāk, nekā citkārt.</span><span class="sxs-lookup"><span data-stu-id="758f8-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="758f8-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="758f8-105">Overview</span></span>

<span data-ttu-id="758f8-106">Organizācijām bieži ir grūti noteikt, kad debitori apmaksās rēķinus.</span><span class="sxs-lookup"><span data-stu-id="758f8-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="758f8-107">Šis informācijas trūkums noved pie ne tik precīzām naudas plūsmas prognozēm, iekasēšanas procesiem, kas sākas ar novēlošanos, un pasūtījumiem, kas tiek nodoti debitoriem, kuri var neizpildīt savus maksājumus.</span><span class="sxs-lookup"><span data-stu-id="758f8-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="758f8-108">Debitoru maksājumu ieskati (priekšskatījums) palīdz organizācijām prognozēt, kad debitora rēķins tiks apmaksāts, un palīdz organizācijām izveidot iekasēšanas stratēģijas, kas palielina savlaicīgas apmaksas iespējamību.</span><span class="sxs-lookup"><span data-stu-id="758f8-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="758f8-109">Prognozes</span><span class="sxs-lookup"><span data-stu-id="758f8-109">Predictions</span></span>

<span data-ttu-id="758f8-110">Maksājumu prognozes dos iespēju uzņēmumiem uzlabot savus biznesa procesus, palīdzot tiem viegli identificēt rēķinus, kas varētu tikt apmaksāti ar novēlošanos, un veikt piemērotus pasākumus, kas uzlabo viņu iespējas saņemt atalgojumu laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="758f8-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="758f8-111">Izmantojot mašīnu mācīšanās modeli, kas palīdz veikt vēsturiskos rēķinus, maksājumus un debitora datus, debitoru maksājumu ieskatus (priekšskatījums) precīzāk prognozē, kad debitors maksās nenomaksātu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="758f8-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="758f8-112">Katram neapmaksātajam rēķinam līdzeklis Debitoru maksājumu ieskati (priekšskatījums) prognozē trīs maksājumu iespējamības:</span><span class="sxs-lookup"><span data-stu-id="758f8-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="758f8-113">Iespējamība, ka maksājums tiek veikts laikā</span><span class="sxs-lookup"><span data-stu-id="758f8-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="758f8-114">Iespējamība, ka maksājums tiek veikts novēloti</span><span class="sxs-lookup"><span data-stu-id="758f8-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="758f8-115">Iespējamība, ka maksājums tiek veikts ļoti novēloti</span><span class="sxs-lookup"><span data-stu-id="758f8-115">Probability of payment being made very late</span></span>

<span data-ttu-id="758f8-116">Lai palīdzētu uzņēmumiem izprast kopējo maksājuma summu, ko tie var sagaidīt no debitora vienā no trijiem intervāliem (Laikā, Novēloti un Ļoti novēloti), klientu maksājumu ieskati (priekšskatījums) sniedz arī apkopotu skatījumu par paredzētajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="758f8-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="758f8-117">[![Apkopots skats uz maksājuma prognozēm](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="758f8-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="758f8-118">Turklāt katram rēķinam ir piešķirta maksājuma iespējamība laikā.</span><span class="sxs-lookup"><span data-stu-id="758f8-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="758f8-119">Ja maksājuma iespējamība laikā ir mazāka par 50%, rēķini tiek atzīmēti ar sarkanu apli, lai norādītu, ka šiem rēķiniem var būt nepieciešama uzmanība iekasēšanā.</span><span class="sxs-lookup"><span data-stu-id="758f8-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="758f8-120">[![Maksājumu iespējamības saraksts](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="758f8-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="758f8-121">Debitora maksājuma ieskats (priekšskatījums) sniedz arī kontekstuālu informāciju, lai izskaidrotu prognozēšanu, piemēram, vislabākos faktorus, kas ietekmēja prognozes, pašreizējo biznesa situāciju ar debitoru un detalizētu informāciju par vēsturisko debitoru maksājumu uzvedību.</span><span class="sxs-lookup"><span data-stu-id="758f8-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="758f8-122">Daudzos uzņēmumos iekasēšanas process ir aktīva darbība; iekasēšanas process netiek sākts, līdz pienāk rēķinu apmaksas laiks.</span><span class="sxs-lookup"><span data-stu-id="758f8-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="758f8-123">Ar debitoru maksājumu ieskatu (priekšskatījums), organizācijas var būt aktīvākas iekasēšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="758f8-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="758f8-124">Vairs nav jāgaida uz transakcijām, lai sāktu iekasēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="758f8-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="758f8-125">Tā vietā tās var izmantot maksājumu prognozēšanas iespēju, lai noteiktu, vai proaktīvās iekasēšanas uzlabos iespējamību, ka tiks maksāts laikā.</span><span class="sxs-lookup"><span data-stu-id="758f8-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="758f8-126">Maksājumu prognozēšana arī sniedz uzņēmumiem informāciju, kas nepieciešama, lai attaisnotu agrāku iekasēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="758f8-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="758f8-127">Metodoloģija</span><span class="sxs-lookup"><span data-stu-id="758f8-127">Methodology</span></span>

<span data-ttu-id="758f8-128">AI risinājuma izstrāde un izvietošana ir grūta.</span><span class="sxs-lookup"><span data-stu-id="758f8-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="758f8-129">Ir nepieciešama datu zinātnieku grupa, mācību priekšmetu eksperti un inženieri, kas strādā ilgāku laika periodu, lai formulētu, attīstītu, izvietotu un uzturētu izmantojamu AI risinājumu.</span><span class="sxs-lookup"><span data-stu-id="758f8-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="758f8-130">Mēs atvieglojam AI risinājumu izvietošanu un izmantošanu programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="758f8-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="758f8-131">Mēs esam ievietojuši AI risinājumus programmā Finance, kas ir iebūvēti papildus Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="758f8-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="758f8-132">Gala lietotājs ar vienu pogas klikšķi var izvietot AI risinājumu un sākt izmantot inteliģento prognožu iespējas.</span><span class="sxs-lookup"><span data-stu-id="758f8-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="758f8-133">Ja organizācija nav apmierināta ar prognožu precizitāti, prasmīgs lietotājs, atkal izmantojot vienu klikšķi, var ievadīt AI builder paplašināšanas pieredzi un pēc tam atlasīt vai noņemt laukus, ko izmanto prognožu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="758f8-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="758f8-134">Kad tas ir sagatavots, tie var apmācīt un publicēt izmaiņas, un jaunais modelis tiks automātiski ievākts prognozēm programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="758f8-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="758f8-135">Kā iegūt debitoru maksājumu ieskatus (priekšskatījums)?</span><span class="sxs-lookup"><span data-stu-id="758f8-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="758f8-136">Lūdzu nosūtiet e-pasta ziņojumu uz [Debitoru maksājumu ieskati (priekšskatījums)](mailto:fiap@microsoft.com), ja vēlaties izmēģināt Debitoru maksājumu ieskatus (priekšskatījums).</span><span class="sxs-lookup"><span data-stu-id="758f8-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="758f8-137">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="758f8-137">Privacy Notice</span></span>

<span data-ttu-id="758f8-138">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="758f8-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


