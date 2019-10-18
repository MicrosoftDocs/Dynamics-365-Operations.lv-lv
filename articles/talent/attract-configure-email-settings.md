---
title: E-pasta iestatījumu konfigurēšana programmā Microsoft Dynamics 365 Talent - Attract
description: Šajā tēmā ir paskaidrots, kā konfigurēt iestatījumus e-pasta ziņojumiem, kas tiek nosūtīti, izmantojot Microsoft Dynamcis 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008666"
---
# <a name="configure-email-settings"></a><span data-ttu-id="bd19f-103">E-pasta iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bd19f-103">Configure email settings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bd19f-104">Jūsu zīmols nosaka uzticēšanos un palīdz veidot attiecības ar kandidātiem, pirms viņi vēl ir paspējuši pieteikties jūsu izsludinātajiem amatiem.</span><span class="sxs-lookup"><span data-stu-id="bd19f-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="bd19f-105">Pozitīva zīmola uztvere piesaista labākos talantus un pastiprina esošo darbinieku lojalitāti.</span><span class="sxs-lookup"><span data-stu-id="bd19f-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="bd19f-106">Microsoft Dynamics 365 Talent: Attract ļauj konfigurēt e-pasta ziņojumus tā, lai tie atspoguļotu jūsu uzņēmuma zīmolu.</span><span class="sxs-lookup"><span data-stu-id="bd19f-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="bd19f-107">Tādējādi varat nodrošināt konsekventu pieredzi darba kandidātiem visa atlases procesa gaitā.</span><span class="sxs-lookup"><span data-stu-id="bd19f-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="bd19f-108">Izmantojot Attract, varat veikt tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="bd19f-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="bd19f-109">Konfigurējiet e-pasta iestatījumus, lai tiktu izmantots jūsu uzņēmuma Microsoft Exchange e-pasta pakalpojumu konts.</span><span class="sxs-lookup"><span data-stu-id="bd19f-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="bd19f-110">Šādā veidā kandidāti zinās, ka e-pasta ziņojumi nāk no jūsu uzņēmuma.</span><span class="sxs-lookup"><span data-stu-id="bd19f-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="bd19f-111">Piemēram, varat konfigurēt iestatījumus tā, lai kandidāti saņemtu e-pasta ziņojumus no adreses `recruiting@contoso.com`, nevis no `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="bd19f-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="bd19f-112">Nodrošiniet konsekventu zīmolradi visos e-pasta ziņojumos, iestatot globālo galveni un kājeni e-pasta veidnēm.</span><span class="sxs-lookup"><span data-stu-id="bd19f-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="bd19f-113">Lai konfigurētu programmu Attract tā, lai tā e-pasta ziņojumu sūtīšanai izmantotu jūsu uzņēmuma e-pasta pakalpojumu kontu, ir nepieciešams visaptverošais darbā pieņemšanas papildinājums.</span><span class="sxs-lookup"><span data-stu-id="bd19f-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="bd19f-114">E-pasta pakalpojumu konta pievienošana</span><span class="sxs-lookup"><span data-stu-id="bd19f-114">Connect an email service account</span></span>

<span data-ttu-id="bd19f-115">Pievienojot uzņēmuma e-pasta pakalpojumu kontu, varat izveidot zīmolam pielāgotus e-pasta ziņojumus sarakstei ar darba kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="bd19f-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="bd19f-116">Ja nepievienojat sava uzņēmuma kontu, programma Attract izmanto noklusējuma Microsoft zīmola e-pasta pakalpojumu kontu.</span><span class="sxs-lookup"><span data-stu-id="bd19f-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="bd19f-117">Atlasiet **Iestatījumi** (zobrata simbols augšējā labajā stūrī) un pēc tam atlasiet **Administrēšanas centrs**.</span><span class="sxs-lookup"><span data-stu-id="bd19f-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="bd19f-118">Cilnes **E-pasta iestatījumi** sadaļā **E-pasta pakalpojumu konti** atlasiet **Pievienot uzņēmuma kontu**.</span><span class="sxs-lookup"><span data-stu-id="bd19f-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Uzņēmuma e-pasta pakalpojumu konta pievienošana programmā Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="bd19f-120">Plašāku informāciju par to, kā izveidot kopīgotu e-pasta kontu, skatiet tēmā [Koplietojamās pastkastes pakalpojumā Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="bd19f-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="bd19f-121">Microsoft pierakstīšanās logā pierakstieties, izmantojot uzņēmuma akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="bd19f-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="bd19f-122">Ja vēl neesat iestatījis e-pasta pakalpojumu kontu vai vēlaties pievienot jaunu, atlasiet **Pievienot jaunu pakalpojumu kontu** un pēc tam ievadiet e-pasta informāciju.</span><span class="sxs-lookup"><span data-stu-id="bd19f-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="bd19f-123">Ja esat jau iestatījis e-pasta pakalpojumu kontu, ko vēlaties izmantot, atlasiet to.</span><span class="sxs-lookup"><span data-stu-id="bd19f-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="bd19f-124">Kad jūsu e-pasta pakalpojumu konts ir veiksmīgi konfigurēts, tas tiek rādīts sadaļā **E-pasta pakalpojumu konti**.</span><span class="sxs-lookup"><span data-stu-id="bd19f-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="bd19f-125">E-pasta pakalpojumu konta atvienošana</span><span class="sxs-lookup"><span data-stu-id="bd19f-125">Disconnect an email service account</span></span>

<span data-ttu-id="bd19f-126">Ja vēlaties pārtraukt sava uzņēmuma domēna izmantošanu e-pasta sarakstē programmā Attract, varat atvienot e-pasta pakalpojumu kontu.</span><span class="sxs-lookup"><span data-stu-id="bd19f-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="bd19f-127">Atlasiet **Iestatījumi** (zobrata simbols augšējā labajā stūrī) un pēc tam atlasiet **Administrēšanas centrs**.</span><span class="sxs-lookup"><span data-stu-id="bd19f-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="bd19f-128">Cilnes **E-pasta iestatījumi** sadaļā **E-pasta pakalpojumu konti** atlasiet pogu **Vairāk** (trīs vertikālie punkti) blakus e-pasta pakalpojumu kontam, ko vēlaties atvienot.</span><span class="sxs-lookup"><span data-stu-id="bd19f-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="bd19f-129">Atlasiet **Atvienot e-pasta kontu**.</span><span class="sxs-lookup"><span data-stu-id="bd19f-129">Select **Disconnect email account**.</span></span>

    ![Uzņēmuma e-pasta pakalpojumu konta atvienošana](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="bd19f-131">Kad tiek parādīta uzvedne ar aicinājumu apstiprināt operāciju, atlasiet **Atvienot**.</span><span class="sxs-lookup"><span data-stu-id="bd19f-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Uzņēmuma e-pasta pakalpojumu konta atvienošanas apstiprināšana](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="bd19f-133">Ja nepievienojat citu e-pasta pakalpojumu kontu, e-pasta ziņojumu sūtīšanai no programmas Attract tiek izmantots noklusējuma Microsoft zīmola e-pasta pakalpojumu konts.</span><span class="sxs-lookup"><span data-stu-id="bd19f-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="bd19f-134">E-pasta veidnes iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bd19f-134">Configure email template settings</span></span>

<span data-ttu-id="bd19f-135">Varat augšupielādēt sava uzņēmuma logotipa attēlu vai citu informāciju kā zīmola galveni uzņēmuma e-pasta ziņojumiem.</span><span class="sxs-lookup"><span data-stu-id="bd19f-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="bd19f-136">E-pasta kājenē varat arī norādīt saites uz konfidencialitātes politiku un lietošanas nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="bd19f-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="bd19f-137">Jums ir jāievēro visi piemērojamie jūsu valsts vai reģiona tiesību akti, kā arī e-pasta adresātam piemērojamie valsts vai reģiona tiesību akti.</span><span class="sxs-lookup"><span data-stu-id="bd19f-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="bd19f-138">Tostarp jāievēro arī surogātpasta ierobežošanas noteikumi.</span><span class="sxs-lookup"><span data-stu-id="bd19f-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="bd19f-139">Atlasiet **Iestatījumi** (zobrata simbols augšējā labajā stūrī) un pēc tam atlasiet **Administrēšanas centrs**.</span><span class="sxs-lookup"><span data-stu-id="bd19f-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="bd19f-140">Cilnes **E-pasta iestatījumi** sadaļā **E-pasta veidnes iestatījumi** ievelciet attēlu, kuru vēlaties izmantot kā e-pasta galveni, attēlu lodziņā vai noklikšķiniet uz attēlu lodziņa, lai pārlūkotu failu.</span><span class="sxs-lookup"><span data-stu-id="bd19f-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="bd19f-141">Lai aizstātu jau esošu attēlu, vispirms atlasiet opciju **Noņemt** blakus attēlam.</span><span class="sxs-lookup"><span data-stu-id="bd19f-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="bd19f-142">Attēlam ir jābūt JPEG, JPG, PNG vai SVG failam.</span><span class="sxs-lookup"><span data-stu-id="bd19f-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="bd19f-143">Ieteicamais attēlu lielums ir no 25 līdz 800 pikseļiem platumā un no 25 līdz 150 pikseļiem augstumā.</span><span class="sxs-lookup"><span data-stu-id="bd19f-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="bd19f-144">Maksimālais galvenes faila lielums ir 1 megabaits (MB).</span><span class="sxs-lookup"><span data-stu-id="bd19f-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Uzņēmuma e-pasta galvenes attēla pievienošana](./media/attract-admin-email-header.png)

3. <span data-ttu-id="bd19f-146">Sadaļā **Jūsu konfidencialitātes politika saziņai** norādiet saiti uz jūsu uzņēmuma konfidencialitātes politiku.</span><span class="sxs-lookup"><span data-stu-id="bd19f-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="bd19f-147">Sadaļā **Jūsu noteikumi un nosacījumi komunikācijai** norādiet saiti uz jūsu uzņēmuma lietošanas nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="bd19f-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Saišu pievienošana uz uzņēmuma konfidencialitātes politiku un lietošanas nosacījumiem izmantošanai e-pasta kājenē](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="bd19f-149">Atlasiet **Saglabāt**, lai saglabātu e-pasta veidnes iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="bd19f-149">Select **Save** to save your email template settings.</span></span>
