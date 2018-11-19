---
title: "Inteliģentie ieteikumi"
description: "Šajā tēmā ir paskaidrots, kā var izmantot algoritmisko mācīšanos, lai sniegtu ieteikumus darbiem un darba kandidātiem."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/12/2018

---

# <a name="intelligent-recommendations"></a><span data-ttu-id="46ca7-103">Inteliģentie ieteikumi</span><span class="sxs-lookup"><span data-stu-id="46ca7-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="46ca7-104">Algoritmiskā mācīšanās var noderēt personāla atlases darbiniekiem un darbā pieņemšanas vadītājiem, lai ātri atpazītu amatiem piemērotākos kandidātus.</span><span class="sxs-lookup"><span data-stu-id="46ca7-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="46ca7-105">Tā var noderēt arī potenciālajiem darba ņēmējiem, lai atrasto savam profilam un interesēm vispiemērotāko amatu.</span><span class="sxs-lookup"><span data-stu-id="46ca7-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="46ca7-106">Izmantojot šos līdzekļus un sniedzot atsauksmes, laika gaitā ieteikumi uzlabojas.</span><span class="sxs-lookup"><span data-stu-id="46ca7-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="46ca7-107">Inteliģento ieteikumu līdzekļi ir pieejami tikai kopā ar visaptverošās darbā pieņemšanas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="46ca7-107">The intelligent recommendation features are available only with the Comprehensive hiring add-on.</span></span>
> - <span data-ttu-id="46ca7-108">Lai iespējotu kandidāta un darba ieteikumu līdzekļus, administratoram ir jāieslēdz to priekšskatījuma opcijas.</span><span class="sxs-lookup"><span data-stu-id="46ca7-108">To enable the candidate and job recommendation features, an admin must turn on the preview options for them.</span></span> <span data-ttu-id="46ca7-109">Administrēšanas centra cilnē **Līdzekļu pārvaldība** pārliecinieties, vai opcija **Priekšskatījuma līdzekļi** ir iestatīta uz **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="46ca7-109">In the Admin center, on the **Feature management** tab, make sure that the **Preview features** option is set to **On**.</span></span> <span data-ttu-id="46ca7-110">Pēc tam pārliecinieties, vai atsevišķā opcija **Kandidāta ieteikums** un opcija **Darba ieteikums** ir iestatīta uz **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="46ca7-110">Then make sure that the individual **Candidate recommendation** and **Job recommendation** options are set to **On**.</span></span>

## <a name="candidate-recommendations"></a><span data-ttu-id="46ca7-111">Kandidātu ieteikumi</span><span class="sxs-lookup"><span data-stu-id="46ca7-111">Candidate recommendations</span></span>

<span data-ttu-id="46ca7-112">Tā kā darba piedāvājumi var piesaistīt simtiem kandidātu, personāla atlases darbiniekiem un darbā pieņemšanas vadītājiem varētu būt sarežģīti atrast kandidātus, kuru prasmes un līdzšinējā darba pieredze vislabāk atbilst nepieciešamajiem amatiem.</span><span class="sxs-lookup"><span data-stu-id="46ca7-112">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="46ca7-113">Analizējot korelāciju starp darba pienākumu aprakstu un prasībām un datiem no kandidātu CV un profiliem, var izmantot algoritmisko mācīšanos, lai veidotu kandidātu ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="46ca7-113">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="46ca7-114">Kandidātu ieteikumi var noderēt personāla atlases darbiniekiem un darbā pieņemšanas vadītājiem, lai atpazītu labākos talantus un ātrāk pārceltu tos uz interviju posmu.</span><span class="sxs-lookup"><span data-stu-id="46ca7-114">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="46ca7-115">Ikvienam darbam, kuram pastāv vairāk nekā desmit kandidātu vai potenciālo darba ņēmēju, kam ir CV vai aizpildīti profili, kandidāti vai potenciālie darba ņēmēji, kas darba prasībām atbilst vislabāk, tiek rādīti lapas **Darbs** sadaļā **Apsveramie kandidāti**.</span><span class="sxs-lookup"><span data-stu-id="46ca7-115">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="46ca7-116">Ikvienam ieteiktajam kandidātam kandidāta kartītē varat atlasīt **Skatīt kandidātu**, lai pārskatītu šī kandidāta profilu un rīkotos saistībā ar šo pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="46ca7-116">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="46ca7-117">Varat izmantot daudzpunktes pogu (**...**), lai kandidāta profilu atvērtu jaunā cilnē. Šo daudzpunktes pogu varat arī izmantot, lai sniegtu atsauksmes par attiecīgo ieteikumu.</span><span class="sxs-lookup"><span data-stu-id="46ca7-117">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="46ca7-118">Šādi jūs palīdzat pielāgot ieteikumu programmu un uzlabot turpmākos ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="46ca7-118">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="46ca7-119">Visi ieteikumi, kas jums nepatīk, tiek izņemti no sadaļas **Apsveramie kandidāti**, kad atsvaidzināt lapu **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="46ca7-119">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="46ca7-120">Atsauksmju kartīti varat izmantot, lai norādītu, kādēļ attiecīgais ieteikums nebija noderīgs.</span><span class="sxs-lookup"><span data-stu-id="46ca7-120">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="46ca7-121">Darbu ieteikumi</span><span class="sxs-lookup"><span data-stu-id="46ca7-121">Job recommendations</span></span> 

<span data-ttu-id="46ca7-122">Kad potenciālais darbinieks izmanto karjeras vietni, lai pieteiktos kādam darbam, tiek ieteikti citi attiecīgajā organizācijā pieejamie amati.</span><span class="sxs-lookup"><span data-stu-id="46ca7-122">When a prospective employee uses the career site to apply to a job, other open positions at the organization are recommended.</span></span> <span data-ttu-id="46ca7-123">Šie ieteikumi ir balstīti uz potenciālā darba ņēmēja iepriekšējiem pieteikumiem un CV vai kandidāta profilu.</span><span class="sxs-lookup"><span data-stu-id="46ca7-123">These recommendations are based on the prospect's past applications, and on his or her resume or candidate profile.</span></span> <span data-ttu-id="46ca7-124">Tādēļ darbu ieteikumi palīdz potenciālajiem darba ņēmējiem ātri atpazīt sev vispiemērotākos darbus.</span><span class="sxs-lookup"><span data-stu-id="46ca7-124">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="46ca7-125">Darbu ieteikumi potenciālajiem darba ņēmējiem tiek piedāvāti, ja karjeras vietnē ir publicēti vairāk nekā desmit darbi.</span><span class="sxs-lookup"><span data-stu-id="46ca7-125">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="46ca7-126">Potenciālie darba ņēmēji no ieteikuma kartītes var atvērt detalizētu informāciju par attiecīgo darba sludinājumu.</span><span class="sxs-lookup"><span data-stu-id="46ca7-126">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="46ca7-127">Viņi var arī sniegt atsauksmes par ieteikumiem, lai palīdzētu uzlabot turpmākos ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="46ca7-127">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>

