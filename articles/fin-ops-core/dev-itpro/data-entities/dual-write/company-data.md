---
title: Uzņēmuma koncepts Dataverse
description: Šajā tēmā aprakstīta uzņēmuma datu integrācija starp programmām Finance and Operations un Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 189d1b8a68f8457d32d656fefeb6cc2a332a3b22
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560253"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="500b5-103">Uzņēmuma koncepts Dataverse</span><span class="sxs-lookup"><span data-stu-id="500b5-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="500b5-104">Programmā Finance and Operations koncepts *uzņēmums* ir gan juridiska konstrukcija, gan biznesa konstrukcija.</span><span class="sxs-lookup"><span data-stu-id="500b5-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="500b5-105">Tā ir arī datu drošības un redzamības robeža.</span><span class="sxs-lookup"><span data-stu-id="500b5-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="500b5-106">Lietotāji vienmēr strādā viena uzņēmuma kontekstā, un lielāko daļu datu izslēdz uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="500b5-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="500b5-107">Dataverse nav līdzvērtīga koncepta.</span><span class="sxs-lookup"><span data-stu-id="500b5-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="500b5-108">Tuvākais koncepts ir *biznesa vienība*, kas galvenokārt ir lietotāja datu drošības un redzamības robeža.</span><span class="sxs-lookup"><span data-stu-id="500b5-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="500b5-109">Šim konceptam nav tādas pašas juridiskās vai biznesa ietekmes kā uzņēmuma konceptam.</span><span class="sxs-lookup"><span data-stu-id="500b5-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="500b5-110">Tā kā biznesa vienība un uzņēmums nav līdzvērtīgi koncepti, nav iespējams piespiest vienu pret vienu (1:1) kartēšanu starp tiem Dataverse integrācijas nolūkā.</span><span class="sxs-lookup"><span data-stu-id="500b5-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="500b5-111">Tomēr, tā kā lietotājiem pēc noklusējuma ir jābūt iespējai skatīt tās pašas rindas programmā un Dataverse, Microsoft ir ieviesis jaunu tabulu Dataverse ar nosaukumu cdm\_Uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="500b5-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="500b5-112">Šī tabula ir līdzvērtīga uzņēmuma tabulai programmā.</span><span class="sxs-lookup"><span data-stu-id="500b5-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="500b5-113">Lai palīdzētu garantēt, ka rindu redzamība ir līdzvērtīga starp programmu un Dataverse standarta komplektācijā, mēs iesakām šādu iestatīšanu datiem Dataverse:</span><span class="sxs-lookup"><span data-stu-id="500b5-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="500b5-114">Katrai Finance and Operations uzņēmuma rindai, kas ir iespējota duālajam ierakstam, tiek izveidota saistīta cmd\_uzņēmums rinda.</span><span class="sxs-lookup"><span data-stu-id="500b5-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="500b5-115">Kad CDM\_Uzņēmums rinda ir izveidota un ir iespējota duālajam ierakstam, tiek izveidota noklusējuma biznesa vienība ar tādu pašu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="500b5-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="500b5-116">Lai gan noklusējuma grupa šim biznesa vienībai tiek izveidota automātiski, biznesa vienība netiek izmantota.</span><span class="sxs-lookup"><span data-stu-id="500b5-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="500b5-117">Tiek izveidota atsevišķa īpašnieka grupa ar tādu pašu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="500b5-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="500b5-118">Arī tā ir saistīta ar biznesa vienību.</span><span class="sxs-lookup"><span data-stu-id="500b5-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="500b5-119">Pēc noklusējuma jebkuras rindas, kas tiek izveidota un duāli ierakstīta Dataverse, īpašnieks tiek iestatīts uz grupu "DW Owner", kas ir saistīta ar attiecīgo biznesa vienību.</span><span class="sxs-lookup"><span data-stu-id="500b5-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="500b5-120">Nākamajos attēlos ir parādīts šīs datu iestatīšanas piemērs Dataverse.</span><span class="sxs-lookup"><span data-stu-id="500b5-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Datu iestatīšana Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="500b5-122">Šīs konfigurācijas dēļ jebkura ar USMF uzņēmumu saistītā rinda pieder grupai, kas ir piesaistīta USMF biznesa vienībai Dataverse.</span><span class="sxs-lookup"><span data-stu-id="500b5-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="500b5-123">Tādēļ jebkurš lietotājs, kuram ir piekļuve šai biznesa vienībai, izmantojot drošības lomu, kas ir iestatīta uz biznesa vienības līmeņa redzamību, tagad var redzēt šīs rindas.</span><span class="sxs-lookup"><span data-stu-id="500b5-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="500b5-124">Nākamajā piemērā parādīts, kā grupas var tikt izmantotas, lai nodrošinātu pareizo piekļuvi šīm rindām.</span><span class="sxs-lookup"><span data-stu-id="500b5-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="500b5-125">"Pārdošanas vadītāja" loma ir piešķirta "USMF pārdošanas" grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="500b5-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="500b5-126">Lietotāji, kuriem ir "Pārdošanas vadītāja" loma, var piekļūt visām konta rindām, kas ir tās pašas biznesa vienības dalībnieki, kuras dalībnieki ir šie lietotāji.</span><span class="sxs-lookup"><span data-stu-id="500b5-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="500b5-127">"USMF pārdošanas" grupa ir saistīta ar iepriekš minēto USMF biznesa vienību.</span><span class="sxs-lookup"><span data-stu-id="500b5-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="500b5-128">Tādēļ "USMF pārdošanas" grupas dalībnieki var redzēt jebkuru kontu, kas pieder "USMF DW" lietotājam, kurš nācis no USMF uzņēmuma tabulas programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="500b5-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![Kā grupas var tikt izmantotas](media/dual-write-company-2.png)

<span data-ttu-id="500b5-130">Kā redzams iepriekšējā attēlā, šī 1:1 kartēšana starp biznesa vienību, uzņēmumu un grupu ir tikai sākumpunkts.</span><span class="sxs-lookup"><span data-stu-id="500b5-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="500b5-131">Šajā piemērā jaunā "Eiropas" biznesa vienība tiek izveidota manuāli Dataverse kā DEMF un ESMF vecākelements.</span><span class="sxs-lookup"><span data-stu-id="500b5-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="500b5-132">Šī jaunā saknes biznesa vienība nav saistīta ar duālo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="500b5-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="500b5-133">Taču to var izmantot, lai grupas "EUR Sales" dalībniekiem piešķirtu piekļuvi konta datiem gan DEMF, gan ESMF, saistītajā drošības lomā iestatot datu redzamību uz **Vecākelementa/Pakārtotā elementa BU**.</span><span class="sxs-lookup"><span data-stu-id="500b5-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="500b5-134">Pēdējā tēma, kas jāapspriež, ir tas, kā duālais ieraksts nosaka, kurai īpašnieka grupai būtu jāpiešķir rindas.</span><span class="sxs-lookup"><span data-stu-id="500b5-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="500b5-135">Šo uzvedību kontrolē kolonna **Noklusējuma atbildīgā darba grupa** CDM\_Uzņēmums rindā.</span><span class="sxs-lookup"><span data-stu-id="500b5-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="500b5-136">Kad cdm\_Uzņēmums rinda ir iespējota duālam ierakstam, spraudnis automātiski izveido saistīto biznesa vienību un īpašnieka grupu (ja tādas vēl nav) un iestata kolonnu **Noklusējuma atbildīgā darba grupa**.</span><span class="sxs-lookup"><span data-stu-id="500b5-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="500b5-137">Administrators var mainīt šo kolonnu uz citu vērtību.</span><span class="sxs-lookup"><span data-stu-id="500b5-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="500b5-138">Tomēr administrators nevar notīrīt kolonnu, kamēr tabula ir iespējota duālajam ierakstam.</span><span class="sxs-lookup"><span data-stu-id="500b5-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="500b5-139">![Noklusējuma atbildīgās darba grupas kolonna](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="500b5-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="500b5-140">Uzņēmuma svītrošana un sāknēšana</span><span class="sxs-lookup"><span data-stu-id="500b5-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="500b5-141">Dataverse integrācija rada uzņēmuma paritāti, izmantojot uzņēmuma identifikatoru datu svītrošanai.</span><span class="sxs-lookup"><span data-stu-id="500b5-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="500b5-142">Kā redzams nākamajā attēlā, visas uzņēmumam specifiskās tabulas tiek izvērstas tā, lai tām būtu relācija daudzi pret vienu (N:1) ar cdm\_Uzņēmuma tabulu.</span><span class="sxs-lookup"><span data-stu-id="500b5-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="500b5-143">![N:1 relācija starp uzņēmumam specifisko tabulu un cdm_Uzņēmuma tabula](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="500b5-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="500b5-144">Pēc tam, kad uzņēmums ir pievienots un saglabāts, rindu vērtība kļūst tikai lasāma.</span><span class="sxs-lookup"><span data-stu-id="500b5-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="500b5-145">Tādēļ lietotājiem jāpārliecinās, ka tie atlasa pareizo uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="500b5-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="500b5-146">Tikai rindas, kurās ir uzņēmuma dati, ir piemērotas duālajiem ierakstiem starp programmu un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="500b5-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="500b5-147">Esošajiem Dataverse datiem drīzumā būs pieejama administratora vadītas sāknēšanas pieredze.</span><span class="sxs-lookup"><span data-stu-id="500b5-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="500b5-148">Automātiski pievienot uzņēmuma nosaukumu klientu iesaistīšanās lietojumprogrammās</span><span class="sxs-lookup"><span data-stu-id="500b5-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="500b5-149">Ir vairāki veidi, kā automātiski aizpildīt uzņēmuma nosaukumu klientu iesaistīšanās lietojumprogrammās.</span><span class="sxs-lookup"><span data-stu-id="500b5-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="500b5-150">Ja esat sistēmas administrators, varat iestatīt noklusējuma uzņēmumu, pārvietojoties uz **Papildu iestatījumi > Sistēma > Drošība > Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="500b5-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="500b5-151">Atveriet **Lietotāja** veidlapu un sadaļā **Organizācijas informācija** iestatiet vērtību **Uzņēmuma noklusējums veidlapās**.</span><span class="sxs-lookup"><span data-stu-id="500b5-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Iestatiet noklusējuma uzņēmumu Organizācijas informācijas sadaļā.":::

+ <span data-ttu-id="500b5-153">Ja jums ir **Rakstīšanas** piekļuve **SystemUser** vienībai **Biznesa struktūrvienības** līmenī, varat mainīt noklusējuma uzņēmumu jebkurā veidlapā, atlasot uzņēmumu no **Uzņēmumu** nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="500b5-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Uzņēmuma nosaukuma maiņa jaunā kontā.":::

+ <span data-ttu-id="500b5-155">Ja jums ir **Rakstīšanas** piekļuve datiem vairāk nekā vienā uzņēmumā, varat mainīt noklusējuma uzņēmumu, izvēloties rindu, kas pieder citam uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="500b5-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Izvēloties rindu, mainās noklusējuma uzņēmums.":::

+ <span data-ttu-id="500b5-157">Ja esat sistēmas konfigurētājs vai administrators un vēlaties automātiski aizpildīt uzņēmuma datus pielāgotā veidlapā, varat izmantot [veidlapas notikumus](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="500b5-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="500b5-158">Pievienojiet JavaScript atsauci **msdyn_/DefaultCompany.js** un izmantojiet tālāk norādītos notikumus.</span><span class="sxs-lookup"><span data-stu-id="500b5-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="500b5-159">Jūs varat izmantot jebkuru veidlapu, piemēram, **Konta** veidlapu.</span><span class="sxs-lookup"><span data-stu-id="500b5-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="500b5-160">**OnLoad** notikumu veidlapai: iestatiet kolonnu **defaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="500b5-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="500b5-161">**OnChange** notikums **Uzņēmuma** kolonnā: iestatiet kolonnu **updateDefaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="500b5-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="500b5-162">Lietot filtrēšanu, pamatojoties uz uzņēmuma kontekstu</span><span class="sxs-lookup"><span data-stu-id="500b5-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="500b5-163">Lai lietotu filtrēšanu, pamatojoties uz uzņēmuma kontekstu pielāgotās veidlapās vai pielāgotajos uzmeklēšanas laukos, kas pievienoti standarta veidlapām, atveriet veidlapu un izmantojiet **Saistīto ierakstu filtrēšanas** sadaļu, lai pielietotu uzņēmuma filtru.</span><span class="sxs-lookup"><span data-stu-id="500b5-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="500b5-164">Tas ir jāiestata katram uzmeklēšanas laukam, kam ir nepieciešama filtrēšana, pamatojoties uz norādītajam uzņēmumam atbilstošo rindu.</span><span class="sxs-lookup"><span data-stu-id="500b5-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="500b5-165">Šis iestatījums tiek parādīts **Kontam** sekojošajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="500b5-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Lietot uzņēmuma kontekstu":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]