---
title: Kas jauns vai mainīts mobilajā programmā Warehouse Management
description: Šajā tēmā ir uzskaitīti jaunie un mainītie līdzekļi katrai Microsoft Dynamics 365 Supply Chain Management Warehouse Management mobilās programmas izlaistajai versijai.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261788"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="2c2e7-103">Kas jauns vai mainīts mobilajā programmā Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="2c2e7-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c2e7-104">Šajā tēmā ir uzskaitīti jaunie līdzekļi, labojumi, uzlabojumi un zināmas problēmas katrai Microsoft Dynamics 365 Supply Chain Management Warehouse Management mobilās programmas izlaistajai versijai.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="2c2e7-105">Versija 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="2c2e7-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="2c2e7-106">Jauni līdzekļi, labojumi un uzlabojumi versijā 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="2c2e7-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="2c2e7-107">Šajā versijā ir iekļauti šādi jauni līdzekļi, labojumi un uzlabojumi:</span><span class="sxs-lookup"><span data-stu-id="2c2e7-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="2c2e7-108">Demonstrācijas režīms tagad parāda visas etiķetes ierīces valodā.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="2c2e7-109">Ir mazāk ticams, ka saņemsit šādu kļūdas ziņojumu: “Nevar atrast norādītajam izmēram piemērotu skatu.”</span><span class="sxs-lookup"><span data-stu-id="2c2e7-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="2c2e7-110">Ir palielināts minimālais darba karšu augstums (ja darbu sarakstā ir konfigurēti trīs vai mazāk lauku).</span><span class="sxs-lookup"><span data-stu-id="2c2e7-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="2c2e7-111">Ir uzlabotas robežas (izbalinātas) detalizētās informācijas karšu apakšdaļā.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="2c2e7-112">Nederīgi simboli XML failos, ar kuriem tiek veikta apmaiņa ar serveri, tagad tiek veiksmīgi apstrādāti.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="2c2e7-113">(Piemēram, nedrukājamās rakstzīmes tagad tiek veiksmīgi apstrādātas un vairs neliks programmai pārtraukt reaģēt.)</span><span class="sxs-lookup"><span data-stu-id="2c2e7-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="2c2e7-114">HTTP kļūdas (piemēram, "kļūda 503"), kad servera pieprasījums tiek iesniegts, tagad tiek veiksmīgi apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="2c2e7-115">Parādītās kļūdas gadījumā opciju saraksts vairs netiek automātiski rādīts kombinēto lodziņu vadīklām.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="2c2e7-116">Programma vairs nepārtrauc reaģēt lietotāja iestatījumos atlasītās parādāmās orientācijas dēļ.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="2c2e7-117">Preču attēli tagad tiek rādīti pašapkalpošanās vidēs.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="2c2e7-118">(Šīs izmaiņas attiecas tikai uz zemas izšķirtspējas versijām.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="2c2e7-119">Failu pārvaldības pakalpojums neatbalsta pilna lieluma attēlus pašapkalpošanās vidēs.)</span><span class="sxs-lookup"><span data-stu-id="2c2e7-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="2c2e7-120">Ir fiksēta problēma, kas saistīta ar nulles daudzuma īsu savākšanu.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="2c2e7-121">Programma vairs nepārtrauc reaģēt, ja detalizētas informācijas kartē tiek rādīti vairāki identiski lauki.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="2c2e7-122">Zināmās problēmas versijā 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="2c2e7-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="2c2e7-123">Šajā versijā pastāv šādas zināmās problēmas:</span><span class="sxs-lookup"><span data-stu-id="2c2e7-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="2c2e7-124">Programma (it īpaši darbu saraksts) laika gaitā kļūst lēnāka.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="2c2e7-125">**Windows versija:** Ja USB pistoli izmanto skenēšanai sistēmā Windows, nekonsekventi rezultāti izraisa skenēto simbolu sajaukšanu.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="2c2e7-126">Versija 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="2c2e7-126">Version 2.0.5.0</span></span>

<span data-ttu-id="2c2e7-127">Šajā versijā ir iekļauti šādi jauni līdzekļi, labojumi un uzlabojumi:</span><span class="sxs-lookup"><span data-stu-id="2c2e7-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="2c2e7-128">Klienta noslēpums vairs nav paslēpts savienojuma iestatījumu uzstādījumos.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="2c2e7-129">Tagad var īlgi nospiest visu tekstu, lai to skatītu pilnībā.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="2c2e7-130">Kļūdas ziņojums, kad trūkst glabāšanas atļauju, ir uzlabots.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="2c2e7-131">Dažām plūsmām pievienotas jaunas kontroles secības.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="2c2e7-132">Iesniegšanas poga vairs nav pieejama nepareizi loga izmēra dēļ.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="2c2e7-133">Tagad, kad tiek izmantoti lielāki pogu izmēri, slīdņi var pāriet uz mazākiem ekrāniem.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="2c2e7-134">Četru pogu pārklājums vairs nav nogriezts.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="2c2e7-135">Tagad tastatūra atbalsta dzēšanas pogu.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="2c2e7-136">Ir novērsta spilgtuma problēma, kas var rasties, nospiežot tastatūru.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="2c2e7-137">Dažādas demonstrācijas datu problēmas ir fiksētas.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="2c2e7-138">Problēma, kas ietekmēja skaitliskos laukus detalizētās informācijas lapā, ir novērsta.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="2c2e7-139">Dažās ierīcēs ekrāna tastatūra vairs nepazūd.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="2c2e7-140">Dažādas lietotāja interfeisa (UI) kļūdas ir novērstas, piemēram, kļūdas, kas ietekmēja fona krāsu un novietojumu.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="2c2e7-141">Krievijas valodas UI ir uzlabota.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="2c2e7-142">Ir fiksētas dažādas problēmas, kuru dēļ sistēma nereaģēja.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="2c2e7-143">Problēma, kas saistīta ar kalkulatora atkārtotu atvēršanu, ir novērsta.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="2c2e7-144">**Android versija:** problēma, kuras dēļ Android 4.4 pārstāja reaģēt startēšanas laikā, ir novērsta.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="2c2e7-145">**Android versija:** minimālā mērogošana ir samazināta līdz 50 procentiem.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="2c2e7-146">Versija 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="2c2e7-146">Version 2.0.4.0</span></span>

<span data-ttu-id="2c2e7-147">Versija 2.0.4.0 bija Warehouse Management mobilās lietotnes pirmais vispārpieejamais laidiens.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="2c2e7-148">Jauni līdzekļi, labojumi un uzlabojumi versijā 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="2c2e7-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="2c2e7-149">Šī versija iepazīstina ar tālāk minētajiem jaunajiem līdzekļiem, labojumiem un uzlabojumiem, kas priekšskatījuma versijā nebija pieejami:</span><span class="sxs-lookup"><span data-stu-id="2c2e7-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="2c2e7-150">Ja detalizētas informācijas kartē ir iekļautas divas etiķetes ar identiskiem datiem, viena no etiķetēm tiek paslēpta.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="2c2e7-151">Pēc noklusējuma tiek parādītas īpašās rakstzīmes, un iespēja tās slēpt ir noņemta no lietotāja iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="2c2e7-152">Atspējotās iesniegšanas pogas kompaktā rokas skatā tagad tiek rādītas kā nepieejamas.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="2c2e7-153">Vadības ierīču secības loģikas maiņa nodrošina vienmērīgāku mērogošanu starp ierīcēm.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="2c2e7-154">Tāpēc mazāk nepieciešams pielāgot fontu vai pogu mērogošanu.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="2c2e7-155">Noklusējuma krāsas tēma ir mainīta uz *Tumša*.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="2c2e7-156">Lentes skatā ir pievienota atspējotās iesniegšanas pogas trūkstošā ikona.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="2c2e7-157">Taimauta izņēmumi tagad aizved jūs uz savienojuma lapu, nevis parāda rindā esošu kļūdu.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="2c2e7-158">Ja iesniegšanas darbības nav pieejama (piemēram, **Labi**, **Jā**, **Akceptēt**, **Gatavs** vai **Pabeigts**) iesniegšanas poga tiek deaktivizēta.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="2c2e7-159">Programmas stabilitātes uzlabojumi.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-159">App stability has been improved.</span></span>
- <span data-ttu-id="2c2e7-160">Drošības ievainojamībai ir labojums [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="2c2e7-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="2c2e7-161">**Windows versija:** ir fiksēta problēma operētājsistēmā Windows, kur izvēlnes nebija responsīvas pēc loga lieluma maiņas.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="2c2e7-162">Zināmā problēma versijā 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="2c2e7-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="2c2e7-163">Šajā versijā pastāv šāda zināmā problēma:</span><span class="sxs-lookup"><span data-stu-id="2c2e7-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="2c2e7-164">Šai versijai ir problēma ar ierīcēm, kas izmanto Android 4.4.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="2c2e7-165">Izmantojot programmu šajā Android versijā, var rasties problēmas.</span><span class="sxs-lookup"><span data-stu-id="2c2e7-165">You might experience issues when you use the app on this Android version.</span></span>
