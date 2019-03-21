---
title: Klienta brīdinājuma paziņojumi pa e-pastu
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt nosacījumus, kas nodrošina e-pasta paziņojumu nosūtīšanu iepriekš definētu notikumu gadījumā.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9545731af20a96c322b4e92c17f3a46b7077295b
ms.sourcegitcommit: a13f44549ab402cfd04b600f6097ba179915f233
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/05/2019
ms.locfileid: "775068"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="c0619-103">Klienta brīdinājuma paziņojumi pa e-pastu</span><span class="sxs-lookup"><span data-stu-id="c0619-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c0619-104">Programmā Microsoft Dynamics 365 for Finance and Operations varat definēt pielāgotus brīdinājumu nosacījumus, kas nodrošina filtrēto datu skatu uzraudzību un e-pasta paziņojumu automātisku nosūtīšanu iepriekš definēta notikuma gadījumā.</span><span class="sxs-lookup"><span data-stu-id="c0619-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="c0619-105">E-pasta paziņojuma nosūtīšanas opcija ir pieejama visiem atbalstītajiem brīdinājumu veidiem, un to var ieslēgt arī esošajiem brīdinājumu nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="c0619-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="c0619-106">Varat izmantot iebūvētās vadīklas, lai izveidotu brīdinājumu nosacījumus, kas nodrošina sistēmas pakešuzdevumu filtrēto skatu uzraudzību.</span><span class="sxs-lookup"><span data-stu-id="c0619-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="c0619-107">Uzraugot lauka **Statuss** vērtību, varat arī konfigurēt brīdinājumu nosacījumus, kas nodrošina e-pasta ziņojuma nosūtīšanu gadījumā, ja neizdodas veikt pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="c0619-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="c0619-108">Pēc šo brīdinājumu nosacījumu izveides jums vairs nav jāpārbauda, vai pārskatos ir veiktas biznesa datu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="c0619-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="c0619-109">Tā vietā varat uzraudzībai izmantot Finance and Operations intelektisko izmaiņu noteikšanas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="c0619-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="c0619-110">Klienta brīdinājumi ir atkarīgi no e-pasta apakšsistēmas, ko nodrošina integrācija ar Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="c0619-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="c0619-111">Ir ieteicams izmantot vienkāršā pasta pārsūtīšanas protokola (SMTP) nodrošinātāju, lai e-pasta ziņojumu izplatīšanai nebūtu jāizmanto lokālais pasta klients.</span><span class="sxs-lookup"><span data-stu-id="c0619-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="c0619-112">Lai nosūtītu paziņojumus pa e-pastu, debitoriem ir jākonfigurē integrētie e-pasta pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="c0619-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="c0619-113">E-pasta paziņojumi tiek nosūtīti adresātiem brīdinājuma īpašnieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="c0619-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="c0619-114">Papildinformāciju par to, kā konfigurēt e-pasta ziņojumus programmā Finance and Operations, skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="c0619-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="c0619-115">Tālāk esošajā attēlā ir redzams dialoglodziņš **Brīdinājuma nosacījumu izveide**, kurā tagad ir ietverta opcija **Sūtīt e-pasta ziņojumu**.</span><span class="sxs-lookup"><span data-stu-id="c0619-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="c0619-116">[![Dialoglodziņš Brīdinājuma nosacījuma izveide, kurā ir iestatīta opcijas Sūtīt e-pasta ziņojumu vērtība Jā](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="c0619-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c0619-117">Kad ir iestatīta opcijas **Sūtīt e-pasta ziņojumu** vērtība **Jā**, joprojām tiek piegādāti brīdinājumu paziņojumi no darbību centra.</span><span class="sxs-lookup"><span data-stu-id="c0619-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="c0619-118">Brīdinājumu e-pasta paziņojumu veidnes</span><span class="sxs-lookup"><span data-stu-id="c0619-118">Alert notification email templates</span></span>

<span data-ttu-id="c0619-119">Pakalpojums nosūta e-pasta paziņojumus, izmantojot iepriekš definētas e-pasta ziņojumu veidnes, kas sniedz brīdinājuma paziņojuma pamatinformāciju.</span><span class="sxs-lookup"><span data-stu-id="c0619-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="c0619-120">Tālāk esošajā attēlā ir redzama pa e-pastu saņemto brīdinājumu paziņojumu struktūra.</span><span class="sxs-lookup"><span data-stu-id="c0619-120">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="c0619-121">[![Izmantojot veidni izveidotie brīdinājumu paziņojumi par ieraksta izveidi, lauka izmaiņām un veidnes dzēšanu](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="c0619-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
