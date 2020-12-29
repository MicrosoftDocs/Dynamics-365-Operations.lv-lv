---
title: Pārvaldīt līdzekļus
description: Šajā tēmā ir aprakstīts, kā administrators var iespējot priekšskatījuma līdzekļus programmā Microsoft Dynamics 365 Talent, un ir uzskaitīti līdzekļi, kas pašlaik ir iespējoti priekšskatījumam.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461927"
---
# <a name="manage-features"></a><span data-ttu-id="d6f94-103">Pārvaldīt līdzekļus</span><span class="sxs-lookup"><span data-stu-id="d6f94-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6f94-104">Programmā Microsoft Dynamics 365 Human Resources mēs pastāvīgi ieviešam jaunas cilvēkkapitāla pārvaldības (human capital management — HCM) iespējas, un vēlamies, lai klienti šos jaunos līdzekļus varētu izbaudīt pēc iespējas ātrāk.</span><span class="sxs-lookup"><span data-stu-id="d6f94-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="d6f94-105">Administratori var skatīt un izmantot priekšskatījuma līdzekļus savās vidēs.</span><span class="sxs-lookup"><span data-stu-id="d6f94-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="d6f94-106">Šie līdzekļi ir gandrīz gatavi vispārīgai pieejai un ir tikuši plaši testētas.</span><span class="sxs-lookup"><span data-stu-id="d6f94-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="d6f94-107">Mums vēl tikai ir jāpabeidz pēdējais posms — klientu atsauksmju un validāciju saņemšana —, pirms šie līdzekļi kļūst vispārēji pieejami.</span><span class="sxs-lookup"><span data-stu-id="d6f94-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="d6f94-108">Šajā tēmā ir aprakstīts, kā jūs varat iespējot priekšskatījuma līdzekļus, un ir uzskaitīti līdzekļi, kas pašlaik ir pieejami priekšskatījumam.</span><span class="sxs-lookup"><span data-stu-id="d6f94-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="d6f94-109">Šis saraksts tiks atjaunināts, laižot klajā līdzekļus vispārīgai lietošanai un laižot klajā jaunus līdzekļus priekškatīšanai.</span><span class="sxs-lookup"><span data-stu-id="d6f94-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="d6f94-110">Par jaunu līdzekļu piedāvāšanu priekšskatījumam netiek sniegts paziņojums.</span><span class="sxs-lookup"><span data-stu-id="d6f94-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="d6f94-111">Lietotāji vienkārši sāks redzēt jaunus līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="d6f94-111">Users will just start to see the features.</span></span> <span data-ttu-id="d6f94-112">Plašāku informāciju par jaunajiem līdzekļiem programmā Talent skatiet tēmā [Jaunumi un izmaiņas programmā Dynamics 365 Talent](./whats-new.md) un [Dynamics 365 un Power Platform laidiena piezīmes](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="d6f94-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="d6f94-113">Priekšskatījuma līdzekļu iespējošana vai atspējošana</span><span class="sxs-lookup"><span data-stu-id="d6f94-113">Enable or disable preview features</span></span>

<span data-ttu-id="d6f94-114">Lai piekļūtu priekšskatījuma līdzekļiem, jums vispirms tie ir jāiespējo savā vidē.</span><span class="sxs-lookup"><span data-stu-id="d6f94-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="d6f94-115">Priekšskatījuma līdzekļu iespējošana un atspējošana ir atkarīga no vides.</span><span class="sxs-lookup"><span data-stu-id="d6f94-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6f94-116">Kad ieslēdzat iestatījumu **Priekšskatījuma līdzekļi**, jūs iespējojat priekšskatījuma līdzekļus visiem lietotājiem savā organizācijā, kas atrodas attiecīgajā vidē.</span><span class="sxs-lookup"><span data-stu-id="d6f94-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="d6f94-117">Kad izslēdzat šo iestatījumu, jūs atspējojat priekšskatījuma līdzekļus un padarāt tos nepieejamus saviem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="d6f94-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="d6f94-118">Priekšskatījuma līdzekļiem ir ierobežots atbalsts pakalpojumā Talent.</span><span class="sxs-lookup"><span data-stu-id="d6f94-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="d6f94-119">Tie, iespējams, izmanto mazāk privātuma un drošības pasākumu, un tie nav ietverti Talent pakalpojumu līmeņa līgumā (Service Level Agreement — SLA).</span><span class="sxs-lookup"><span data-stu-id="d6f94-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="d6f94-120">Jūs nedrīkstat lietot priekšskatījuma līdzekļus, lai apstrādātu personas datus (t.i., jebkura informācija, kas varētu identificēt jūs) vai apstrādāt citus datus, uz ko attiecas juridiskas vai normatīvas atbilstības prasības.</span><span class="sxs-lookup"><span data-stu-id="d6f94-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="d6f94-121">Attract</span><span class="sxs-lookup"><span data-stu-id="d6f94-121">Attract</span></span>

1. <span data-ttu-id="d6f94-122">Pierakstieties programmā Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="d6f94-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="d6f94-123">Augšējā labajā stūrī, izvēlnē **Iestatīšana** (zobrata simbols) atlasiet **Administrēšanas centrs**.</span><span class="sxs-lookup"><span data-stu-id="d6f94-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="d6f94-124">Cilnē **Līdzekļu pārvaldība** atlasiet opciju blakus vienumam **Priekšskatījuma līdzekļi**, lai tā kļūtu zila un rādītu uzrakstu **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="d6f94-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Priekšskatījuma līdzekļu iespējošana programmā Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="d6f94-126">Atlasiet vai atceliet atsevišķu priekšskatījuma līdzekļu atlasi.</span><span class="sxs-lookup"><span data-stu-id="d6f94-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="d6f94-127">Ja neko nemaināt, ir iespējoti visi pieejamie priekšskatījuma līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="d6f94-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="d6f94-128">Atsvaidziniet pārlūku, lai sāktu redzēt jaunos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="d6f94-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="d6f94-129">Visi lietotāji, kas jau ir pierakstījušies, redzēs šos līdzekļus nākamajā reizē, kad viņi pierakstīsies, vai viņi var atsvaidzināt savu pārlūku, lai šos līdzekļus redzētu nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="d6f94-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="d6f94-130">Dažiem priekšskatījuma līdzekļiem varētu būt nepieciešama papildu konfigurēšana.</span><span class="sxs-lookup"><span data-stu-id="d6f94-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="d6f94-131">Lai pabeigtu attiecīgo iestatīšanu, izmantojiet priekšskatījuma līdzeklim blakus esošās saites.</span><span class="sxs-lookup"><span data-stu-id="d6f94-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="d6f94-132">Dati</span><span class="sxs-lookup"><span data-stu-id="d6f94-132">Feedback</span></span>

<span data-ttu-id="d6f94-133">Vēlamies uzzināt par jūsu pieredzi saistībā ar jebkuru no šiem priekšskatījuma līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="d6f94-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="d6f94-134">Lietojot šos vai citus līdzekļus, laipni lūdzam regulāri sniegt atsauksmes tālāk norādītajās vietnēs.</span><span class="sxs-lookup"><span data-stu-id="d6f94-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="d6f94-135">[Kopiena](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) — šī vieta ir lielisks resurss, kur lietotāji var apspriest lietošanas gadījumos, uzdot jautājumus un saņemt kopienas palīdzību.</span><span class="sxs-lookup"><span data-stu-id="d6f94-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="d6f94-136">Pastāstiet mums par līdzekļiem, kurus vēlaties redzēt produktā, vai informējiet par visām izmaiņām, kuras pēc jūsu domām mums vajadzētu ieviest esošajos līdzekļos.</span><span class="sxs-lookup"><span data-stu-id="d6f94-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="d6f94-137">Iesakiet produktu idejas tālāk norādītajās vietnēs.</span><span class="sxs-lookup"><span data-stu-id="d6f94-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="d6f94-138">Attract idejas</span><span class="sxs-lookup"><span data-stu-id="d6f94-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="d6f94-139">Onboard idejas</span><span class="sxs-lookup"><span data-stu-id="d6f94-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="d6f94-140">Uzmanieties, lai iesniegtajās atsauksmēs vai produktu apskatos neiekļautu nekādus personas datus (jebkādu informāciju, kas ļautu jūs identificēt).</span><span class="sxs-lookup"><span data-stu-id="d6f94-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="d6f94-141">Ievāktā informācija varētu tikt analizēta tālāk, un tā netiek izmantota, lai atbildētu uz pieprasījumiem saskaņā ar piemērojamajiem privātuma likumiem.</span><span class="sxs-lookup"><span data-stu-id="d6f94-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="d6f94-142">Uz personas datiem, kas tiek ievākti atsevišķi saskaņā ar šīm programmām, attiecas [Microsoft privātuma paziņojums](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="d6f94-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="d6f94-143">Ielieciet šo tēmu grāmatzīmēs un atgriezieties, lai uzzinātu par jauniem pievienotiem priekšskatījuma līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="d6f94-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6f94-144">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d6f94-144">See also</span></span>

- [<span data-ttu-id="d6f94-145">Talent programmu izmēģināšana vai iegādāšanās</span><span class="sxs-lookup"><span data-stu-id="d6f94-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="d6f94-146">Jaunumi un izmaiņas Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="d6f94-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="d6f94-147">Nodošanas izpildei plāni</span><span class="sxs-lookup"><span data-stu-id="d6f94-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="d6f94-148">Atbalsta saņemšana saistībā ar Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="d6f94-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
