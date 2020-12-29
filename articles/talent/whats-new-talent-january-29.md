---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 31. janvāris)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690056"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="b65bc-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 31. janvāris)</span><span class="sxs-lookup"><span data-stu-id="b65bc-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="b65bc-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="b65bc-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="b65bc-105">**8.1.2128 būvējums**</span><span class="sxs-lookup"><span data-stu-id="b65bc-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="b65bc-106">Core HR izmaiņas</span><span class="sxs-lookup"><span data-stu-id="b65bc-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="b65bc-107">Paņemtajā brīvajā laikā personas kartītē Atvaļinājums netiek ņemti vērā atvaļinājumu plāna datumi</span><span class="sxs-lookup"><span data-stu-id="b65bc-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="b65bc-108">Atvaļinājumu plāni, kas netiek izpildīti kalendārā gada ietvaros, kartītē **Paņemts** tagad ir norādīts brīvais laiks, kas ir paņemts plānā noteiktajā atvaļinājuma gadā.</span><span class="sxs-lookup"><span data-stu-id="b65bc-108">For leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="b65bc-109">Piemēram, ja organizācijas atvaļinājuma gads ir no 1. jūnija līdz 30. maijam un darbinieks ir izmantojis trīs atvaļinājuma dienas decembrī, kartītē **Paņemts** 15. janvārī tiks rādītas 3 dienas.</span><span class="sxs-lookup"><span data-stu-id="b65bc-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken three days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="b65bc-110">Uzkrātais daudzums neatbilst pakāpju datuma bāzei</span><span class="sxs-lookup"><span data-stu-id="b65bc-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="b65bc-111">Atvaļinājumiem un kavējumiem ir pievienotas jaunas opcijas (parametri **Personāla vadība**), lai klienti varētu noteikt, kad ir spēkā darbinieku nodarbinātības mēnešu datums.</span><span class="sxs-lookup"><span data-stu-id="b65bc-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="b65bc-112">Dažām organizācijām datums ir mēneša beigās, bet citām tas var būt nākamā mēneša sākumā.</span><span class="sxs-lookup"><span data-stu-id="b65bc-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="b65bc-113">Piemēram, viena organizācija var piešķirt prombūtnes laiku 31. decembrī, savukārt cita var piešķirt prombūtnes laiku 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="b65bc-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="b65bc-114">Šī opcija ļauj izvēlēties, kad jāveic piešķiršana.</span><span class="sxs-lookup"><span data-stu-id="b65bc-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="b65bc-115">Nodarbināto darbā pieņemšanas darbības ir iestrēgušas statusā “Darbplūsma izpildīta“</span><span class="sxs-lookup"><span data-stu-id="b65bc-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="b65bc-116">Ir veiktas izmaiņas, lai labotu problēmu, kad neliels skaits darbplūsmu tika pabeigts ar statusu “Darbplūsma izpildīta”.</span><span class="sxs-lookup"><span data-stu-id="b65bc-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="b65bc-117">Tagad jaunajām darbplūsmām statusam būtu jāmainās uz “Pabeigts”, kad darbplūsma tiek pabeigta.</span><span class="sxs-lookup"><span data-stu-id="b65bc-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="b65bc-118">Visām darbplūsmām, kuru statuss ir “Darbplūsma izpildīta”, tas tiks mainīts uz kļūdas statusu, lai to atjauninātu vai noņemtu nepieciešamības gadījumā.</span><span class="sxs-lookup"><span data-stu-id="b65bc-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
