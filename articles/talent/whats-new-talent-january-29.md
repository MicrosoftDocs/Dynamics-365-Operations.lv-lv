---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 31. janvāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
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
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d4504cebb7702c7163c94badeeb06d9af0e5467e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518520"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a><span data-ttu-id="f809a-103">Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 31. janvāris)</span><span class="sxs-lookup"><span data-stu-id="f809a-103">What's new or changed in Dynamics 365 for Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f809a-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="f809a-104">This topic describes features that are either new or changed in Dynamics 365 for Talent</span></span>

<span data-ttu-id="f809a-105">**8.1.2128 būvējums**</span><span class="sxs-lookup"><span data-stu-id="f809a-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="f809a-106">Core HR izmaiņas</span><span class="sxs-lookup"><span data-stu-id="f809a-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="f809a-107">Paņemtajā brīvajā laikā personas kartītē Atvaļinājums netiek ņemti vērā atvaļinājumu plāna datumi</span><span class="sxs-lookup"><span data-stu-id="f809a-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="f809a-108">Gadījumā, ja atvaļinājumu plāni netiek izpildīti kalendārā gada ietvaros, kartītē **Paņemts** tagad ir norādīts brīvais laiks, kas ir paņemts plānā noteiktajā atvaļinājuma gadā.</span><span class="sxs-lookup"><span data-stu-id="f809a-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="f809a-109">Piemēram, ja organizācijas atvaļinājuma gads ir no 1. jūnija līdz 30. maijam un darbinieks ir izmantojis 3 atvaļinājuma dienas decembrī, kartītē **Paņemts** 15. janvārī tiks rādītas 3 dienas.</span><span class="sxs-lookup"><span data-stu-id="f809a-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="f809a-110">Uzkrātais daudzums neatbilst pakāpju datuma bāzei</span><span class="sxs-lookup"><span data-stu-id="f809a-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="f809a-111">Atvaļinājumiem un kavējumiem ir pievienotas jaunas opcijas (parametri **Personāla vadība**), lai klienti varētu noteikt, kad ir spēkā darbinieku nodarbinātības mēnešu datums.</span><span class="sxs-lookup"><span data-stu-id="f809a-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="f809a-112">Dažām organizācijām datums ir mēneša beigās, bet citām tas var būt nākamā mēneša sākumā.</span><span class="sxs-lookup"><span data-stu-id="f809a-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="f809a-113">Piemēram, viena organizācija var piešķirt prombūtnes laiku 31. decembrī, savukārt cita var piešķirt prombūtnes laiku 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="f809a-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="f809a-114">Šī opcija ļauj izvēlēties, kad jāveic piešķiršana.</span><span class="sxs-lookup"><span data-stu-id="f809a-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="f809a-115">Nodarbināto darbā pieņemšanas darbības ir iestrēgušas statusā “Darbplūsma izpildīta“</span><span class="sxs-lookup"><span data-stu-id="f809a-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="f809a-116">Ir veiktas izmaiņas, lai labotu problēmu, kad neliels skaits darbplūsmu tika pabeigts ar statusu “Darbplūsma izpildīta”.</span><span class="sxs-lookup"><span data-stu-id="f809a-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="f809a-117">Tagad jaunajām darbplūsmām statusam būtu jāmainās uz “Pabeigts”, kad darbplūsma tiek pabeigta.</span><span class="sxs-lookup"><span data-stu-id="f809a-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="f809a-118">Visām darbplūsmām, kuru statuss ir “Darbplūsma izpildīta”, tas tiks mainīts uz kļūdas statusu, lai to atjauninātu vai noņemtu nepieciešamības gadījumā.</span><span class="sxs-lookup"><span data-stu-id="f809a-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
