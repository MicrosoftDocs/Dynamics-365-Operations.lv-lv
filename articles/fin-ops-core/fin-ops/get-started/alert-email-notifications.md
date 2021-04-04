---
title: Klienta brīdinājuma paziņojumi pa e-pastu
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt nosacījumus, kas nodrošina e-pasta paziņojumu nosūtīšanu iepriekš definētu notikumu gadījumā.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: fe422d645c8f2c0c564af30624090828e10ea4bf
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567256"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="a8c83-103">Klienta brīdinājumu paziņojumi pa e-pastu</span><span class="sxs-lookup"><span data-stu-id="a8c83-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8c83-104">Varat definēt pielāgotus brīdinājumu nosacījumus, kas nodrošina filtrēto datu skatu uzraudzību un e-pasta paziņojumu automātisku nosūtīšanu iepriekš definēta notikuma gadījumā.</span><span class="sxs-lookup"><span data-stu-id="a8c83-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="a8c83-105">E-pasta paziņojuma nosūtīšanas opcija ir pieejama visiem atbalstītajiem brīdinājumu veidiem, un to var ieslēgt arī esošajiem brīdinājumu nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="a8c83-105">The option to send email notifications is available for all supported alert types and you can also turn them on for existing alert rules.</span></span>

<span data-ttu-id="a8c83-106">Varat izmantot iebūvētās vadīklas, lai izveidotu brīdinājumu nosacījumus, kas nodrošina sistēmas pakešuzdevumu filtrēto skatu uzraudzību.</span><span class="sxs-lookup"><span data-stu-id="a8c83-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="a8c83-107">Uzraugot lauka **Statuss** vērtību, varat arī konfigurēt brīdinājumu nosacījumus, kas nodrošina e-pasta ziņojuma nosūtīšanu gadījumā, ja neizdodas veikt pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="a8c83-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="a8c83-108">Pēc šo brīdinājumu nosacījumu izveides jums vairs nav jāpārbauda, vai pārskatos ir veiktas biznesa datu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="a8c83-108">After you create these alert rules, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="a8c83-109">Tā vietā varat uzraudzībai izmantot intelektisko izmaiņu noteikšanas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="a8c83-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="a8c83-110">Klienta brīdinājumi ir atkarīgi no e-pasta apakšsistēmas, ko nodrošina integrācija ar Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a8c83-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="a8c83-111">Ir ieteicams izmantot vienkāršā pasta pārsūtīšanas protokola (SMTP) nodrošinātāju, lai e-pasta ziņojumu izplatīšanai nebūtu jāizmanto lokālais pasta klients.</span><span class="sxs-lookup"><span data-stu-id="a8c83-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="a8c83-112">Lai nosūtītu paziņojumus pa e-pastu, debitoriem ir jākonfigurē integrētie e-pasta pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="a8c83-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="a8c83-113">E-pasta paziņojumi tiek nosūtīti adresātiem brīdinājuma īpašnieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="a8c83-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="a8c83-114">Papildinformāciju par to, kā konfigurēt e-pasta ziņojumus, skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="a8c83-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="a8c83-115">Tālāk esošajā attēlā ir redzams dialoglodziņš **Brīdinājuma nosacījumu izveide**, kurā tagad ir ietverta opcija **Sūtīt e-pasta ziņojumu**.</span><span class="sxs-lookup"><span data-stu-id="a8c83-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="a8c83-116">[![Dialoglodziņš Brīdinājuma nosacījuma izveide, kurā ir iestatīta opcijas Sūtīt e-pasta ziņojumu vērtība Jā](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="a8c83-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a8c83-117">Kad ir iestatīta opcijas **Sūtīt e-pasta ziņojumu** vērtība **Jā**, joprojām tiek piegādāti brīdinājumu paziņojumi no darbību centra.</span><span class="sxs-lookup"><span data-stu-id="a8c83-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="a8c83-118">Brīdinājumu e-pasta paziņojumu veidnes</span><span class="sxs-lookup"><span data-stu-id="a8c83-118">Alert notification email templates</span></span>

<span data-ttu-id="a8c83-119">Pakalpojums nosūta e-pasta paziņojumus, izmantojot iepriekš definētas e-pasta ziņojumu veidnes, kas sniedz brīdinājuma paziņojuma pamatinformāciju.</span><span class="sxs-lookup"><span data-stu-id="a8c83-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="a8c83-120">Tālāk esošajā attēlā ir redzama pa e-pastu saņemto brīdinājumu paziņojumu struktūra.</span><span class="sxs-lookup"><span data-stu-id="a8c83-120">The following image shows the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="a8c83-121">[![Izmantojot veidni izveidotie brīdinājumu paziņojumi par ieraksta izveidi, lauka izmaiņām un veidnes dzēšanu](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="a8c83-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]