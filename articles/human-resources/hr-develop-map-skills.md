---
title: Kartēt prasmes
description: Lai atrastu kvalificētu personu, varat izveidot prasmju kartēšanas meklēšanu programmā Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076603"
---
# <a name="map-skills"></a><span data-ttu-id="10c25-103">Kartēt prasmes</span><span class="sxs-lookup"><span data-stu-id="10c25-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="10c25-104">Lai atrastu kvalificētu personu, varat izveidot prasmju kartēšanas meklēšanu programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="10c25-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="10c25-105">Prasmju kartēšana meklē atgriešanas rezultātus kritērijiem, ko ievadāt, izmantojot šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="10c25-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="10c25-106">Prasmes</span><span class="sxs-lookup"><span data-stu-id="10c25-106">Skills</span></span>
- <span data-ttu-id="10c25-107">Izglītība</span><span class="sxs-lookup"><span data-stu-id="10c25-107">Education</span></span>
- <span data-ttu-id="10c25-108">Sertifikāti</span><span class="sxs-lookup"><span data-stu-id="10c25-108">Certificates</span></span>
- <span data-ttu-id="10c25-109">Amati</span><span class="sxs-lookup"><span data-stu-id="10c25-109">Positions</span></span>
- <span data-ttu-id="10c25-110">Projektu pieredze</span><span class="sxs-lookup"><span data-stu-id="10c25-110">Project experience</span></span>

<span data-ttu-id="10c25-111">Piemēram, varat atrast cilvēkus savā organizācijā, kas ir ieguvuši savu CPA.</span><span class="sxs-lookup"><span data-stu-id="10c25-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="10c25-112">Prasmju kartēšanas profili ļauj atrast pašreizējos darbiniekus vai kandidātus ar kvalifikāciju, kas tieši atbilst uzņēmuma vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="10c25-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="10c25-113">Prasmju kartēšanas rezultātu sarakstā tiks parādīti vai prasmju profilā tiks iekļauti tikai darbinieki, kandidāti un kontaktpersonas, kas ir izvēlēti iekļaušanai prasmju kartēšanas meklējumos.</span><span class="sxs-lookup"><span data-stu-id="10c25-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="10c25-114">Lai prasmju kartēšanas rezultātos iekļautu personu, iestatiet opciju **Iekļaut prasmju kartēšanā** uz **Jā** šādās lapās.</span><span class="sxs-lookup"><span data-stu-id="10c25-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="10c25-115">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="10c25-115">Worker</span></span><br>
> - <span data-ttu-id="10c25-116">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="10c25-116">Employee</span></span><br>
> - <span data-ttu-id="10c25-117">Kandidāts</span><span class="sxs-lookup"><span data-stu-id="10c25-117">Applicant</span></span><br>
> - <span data-ttu-id="10c25-118">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="10c25-118">Contacts</span></span><br>

<span data-ttu-id="10c25-119">Lai izveidotu prasmju kartēšanu, dodieties uz sadaļu **Darbinieku attīstība > Saites > Prasmju kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="10c25-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="10c25-120">Lai izveidotu prasmju kartēšanas profilu, dodieties uz sadaļu **Darbinieku attīstība > Saites > Prasmju kartēšanas profili**.</span><span class="sxs-lookup"><span data-stu-id="10c25-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="10c25-121">Prasmju atšķirības analīze un prasmju profila analīze</span><span class="sxs-lookup"><span data-stu-id="10c25-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="10c25-122">Lai apskatītu personas zināšanu sarakstu, varat izveidot prasmju profila analīzi.</span><span class="sxs-lookup"><span data-stu-id="10c25-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="10c25-123">Varat izveidot prasmju atbilstību analīzi, lai personas prasmes salīdzinātu ar darbam nepieciešamajām prasmēm.</span><span class="sxs-lookup"><span data-stu-id="10c25-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="10c25-124">Lai izveidotu atbilstību analīzi, dodieties uz **Darbinieku attīstība > Saites > Prasmju atbilstību analīzes darbs – persona**.</span><span class="sxs-lookup"><span data-stu-id="10c25-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="10c25-125">Lai izveidotu prasmju profila analīzi, dodieties uz sadaļu **Darbinieku attīstība > Saites > Prasmju profila analīze**.</span><span class="sxs-lookup"><span data-stu-id="10c25-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="10c25-126">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="10c25-126">See also</span></span>

[<span data-ttu-id="10c25-127">Konfigurēt prasmes</span><span class="sxs-lookup"><span data-stu-id="10c25-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="10c25-128">Ievadīt prasmes</span><span class="sxs-lookup"><span data-stu-id="10c25-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]