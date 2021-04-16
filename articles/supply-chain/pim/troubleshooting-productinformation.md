---
title: Problēmu novēršana saistībā ar preču informāciju
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar preču informāciju.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a05e9957363ef6a659e25ceba84a168507cd641a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841531"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="382c0-103">Problēmu novēršana saistībā ar preču informāciju</span><span class="sxs-lookup"><span data-stu-id="382c0-103">Troubleshoot product information</span></span>

<span data-ttu-id="382c0-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar preču informāciju.</span><span class="sxs-lookup"><span data-stu-id="382c0-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="382c0-105">Nevar izdzēst izlaisto preci.</span><span class="sxs-lookup"><span data-stu-id="382c0-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="382c0-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="382c0-106">Issue description</span></span>

<span data-ttu-id="382c0-107">Izlaisto preci un visus tā variantus var dzēst tikai tad, ja izlaistajai precei nav nevienas saistītās darbības.</span><span class="sxs-lookup"><span data-stu-id="382c0-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="382c0-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="382c0-108">Issue resolution</span></span>

<span data-ttu-id="382c0-109">Sekojiet šiem soļiem, lai dzēstu izlaisto preci vai preču šablonu.</span><span class="sxs-lookup"><span data-stu-id="382c0-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="382c0-110">Aizveriet visas atvērtās krājumu darbības.</span><span class="sxs-lookup"><span data-stu-id="382c0-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="382c0-111">Samaziniet krājumu uz 0 (nulli).</span><span class="sxs-lookup"><span data-stu-id="382c0-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="382c0-112">Veiciet krājumu slēgšanu.</span><span class="sxs-lookup"><span data-stu-id="382c0-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="382c0-113">Dzēsiet visus preču šablona preces variantiem, kurus vēlaties dzēst.</span><span class="sxs-lookup"><span data-stu-id="382c0-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="382c0-114">Vai var mainīt izlaistās preces krājuma kodu?</span><span class="sxs-lookup"><span data-stu-id="382c0-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="382c0-115">Vairumā gadījumu nevar rediģēt izlaisto preču numurus, jo šīs izmaiņas rezultātā dati kļūs bojāti.</span><span class="sxs-lookup"><span data-stu-id="382c0-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="382c0-116">Krājuma kodu var rediģēt tikai tad, ja ir jālabo datu bojājums, ko izraisījusi šīs izlaistās preces iepriekšējā pārdēvēšana, kā norādīts [noņemto vai novecojušo funkciju Finance and Operations 10.0.0 ar platformas atjauninājumu 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24) sarakstā.</span><span class="sxs-lookup"><span data-stu-id="382c0-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="382c0-117">Ja vēlaties rediģēt izlaisto preču krājumu numurus, [nobalsojiet par šo ideju Ideju portālā](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="382c0-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="382c0-118">Noklusējuma norakstīšanas princips no preces netiek ievadīts materiālu komplekta rindā.</span><span class="sxs-lookup"><span data-stu-id="382c0-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="382c0-119">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="382c0-119">Issue description</span></span>

<span data-ttu-id="382c0-120">Kad pievienojat krājumu materiālu komplekta (MK) rindai, sistēma neizmanto noklusējuma norakstīšanas principa informāciju, kas ir iestatīta krājumam.</span><span class="sxs-lookup"><span data-stu-id="382c0-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="382c0-121">Citiem vārdiem, norakstīšanas princips no krājuma netiek parādīts **MK rindas** lapā.</span><span class="sxs-lookup"><span data-stu-id="382c0-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="382c0-122">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="382c0-122">Issue resolution</span></span>

<span data-ttu-id="382c0-123">Ja MK rindā tiek norādīts norakstīšanas princips, tas tiek lietots šai MK rindai.</span><span class="sxs-lookup"><span data-stu-id="382c0-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="382c0-124">Tomēr, ja norakstīšanas princips ir tukšs vai arī tas nav iestatīts MK rindā, tad krājumam iestatītais norakstīšanas princips joprojām būs spēkā šai MK rindai, pat ja tas nav redzams MK rindā.</span><span class="sxs-lookup"><span data-stu-id="382c0-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="382c0-125">Noklusējuma loģika citos Microsoft Dynamics 365 Supply Chain Management līdzekļos parasti nedarbojas šādā veidā.</span><span class="sxs-lookup"><span data-stu-id="382c0-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="382c0-126">Tomēr pašreizējo darbību nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="382c0-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="382c0-127">Pretējā gadījumā var tikt bojāti daži esošie pielāgojumi, kas ir atkarīgi no tā.</span><span class="sxs-lookup"><span data-stu-id="382c0-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="382c0-128">Sistēma ļauj man saglabāt dublētus svītrkodus dažādiem krājumiem vai vienam krājumam ar atšķirīgām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="382c0-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="382c0-129">Sistēma pašlaik neievieš unikālus svītrkodus, un šī ierobežojuma pievienošana ir pārrāvuma izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="382c0-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="382c0-130">Patiesībā korporācija Microsoft ir apliecinājusi, ka ar šīm izmaiņām tiks bojātas dažas esošās klientu instalācijas.</span><span class="sxs-lookup"><span data-stu-id="382c0-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="382c0-131">Tomēr tiks apsvērta plašāka dizaina maiņa, lai nākotnē iespējotu šo funkciju.</span><span class="sxs-lookup"><span data-stu-id="382c0-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="382c0-132">Rediģējot krājumu ierakstu veidnes, tiek parādīts šāds kļūdas ziņojums: "Noliktavas novietojumu nevar izveidot, jo krājums nav uzkrāts.</span><span class="sxs-lookup"><span data-stu-id="382c0-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="382c0-133">Lai uzkrātu krājumus, ir jāatlasa Uzkrātā produkta opcija, kas atrodas saistītajā krājumu modeļu grupā."</span><span class="sxs-lookup"><span data-stu-id="382c0-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="382c0-134">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="382c0-134">Issue description</span></span>

<span data-ttu-id="382c0-135">Šī problēma rodas, ja ievērojat šos soļus, lai mēģinātu izveidot veidni krājumam, kas nav uzkrāts.</span><span class="sxs-lookup"><span data-stu-id="382c0-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="382c0-136">Atveriet izlaisto preci, kas nav uzkrāta.</span><span class="sxs-lookup"><span data-stu-id="382c0-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="382c0-137">Darbību rūts cilnē **Opcijas** atlasiet **Ieraksta informācija**.</span><span class="sxs-lookup"><span data-stu-id="382c0-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="382c0-138">Dialoglodziņā **Ieraksta informācija** atlasiet **Uzņēmuma kontu veidne**.</span><span class="sxs-lookup"><span data-stu-id="382c0-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="382c0-139">Šajā gadījumā, jūs saņemsit sekojošo kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="382c0-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="382c0-140">Noliktavas novietojumu nevar izveidot, jo krājums nav uzkrāts.</span><span class="sxs-lookup"><span data-stu-id="382c0-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="382c0-141">Lai uzkrātu krājumus, ir jāatlasa Uzkrātā produkta opcija, kas atrodas saistītajā krājumu modeļu grupā.</span><span class="sxs-lookup"><span data-stu-id="382c0-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="382c0-142">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="382c0-142">Issue resolution</span></span>

<span data-ttu-id="382c0-143">Preču veidņu izveidošanas procesam ir nepieciešama īpašas preces loģika.</span><span class="sxs-lookup"><span data-stu-id="382c0-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="382c0-144">Tāpēc šim nolūkam nevar izmantot vispārējo **Uzņēmuma kontu veidnes** pogu.</span><span class="sxs-lookup"><span data-stu-id="382c0-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="382c0-145">Tā vietā rīkojieties sekojoši.</span><span class="sxs-lookup"><span data-stu-id="382c0-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="382c0-146">Atveriet izlaisto preci.</span><span class="sxs-lookup"><span data-stu-id="382c0-146">Open a released product.</span></span>
1. <span data-ttu-id="382c0-147">Darbību rūts grupas **Jauns** cilnē **Prece** atlasiet **Veidne \> Izveidot kopīgotu veidni**.</span><span class="sxs-lookup"><span data-stu-id="382c0-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="382c0-148">Noklusējuma palīdzības teksts, kas tiek pievienots preču atribūtos, netiek ievadīts izlaistajā precē.</span><span class="sxs-lookup"><span data-stu-id="382c0-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="382c0-149">Apraksts un palīdzības teksts, kas tiek pievienots preču atribūtos, nav redzams vai ievadīts izlaistajās precēs pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="382c0-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="382c0-150">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="382c0-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="382c0-151">Ievadītais noklusētais daudzums atšķiras no tā, vai tas ir reģistrēts no MK, un kad tas ir reģistrēts no MK versijas.</span><span class="sxs-lookup"><span data-stu-id="382c0-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="382c0-152">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="382c0-152">Issue description</span></span>

<span data-ttu-id="382c0-153">Pēc noklusējuma, kad pievienojat krājumu MK, daudzums tiek iestatīts uz 1, nevis daudzums, kas ir definēts laukā **Minimālais pasūtījuma daudzums** lapā **Noklusējuma pasūtījuma iestatījumi** atlasītajai precei.</span><span class="sxs-lookup"><span data-stu-id="382c0-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="382c0-154">Tomēr, kad jūs pievienojat krājumu no MK versijas un ir atlasīts krājums un variants, pēc noklusējuma ievadītais daudzums ņem vērā minimālo daudzumu, kas tiek iestatīts noklusējuma pasūtījuma iestatījumos noteiktām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="382c0-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="382c0-155">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="382c0-155">Issue resolution</span></span>

<span data-ttu-id="382c0-156">Šāda darbība ir paredzama.</span><span class="sxs-lookup"><span data-stu-id="382c0-156">This behavior is expected.</span></span> <span data-ttu-id="382c0-157">Tomēr fakts, ka loģika atšķiras MK un MK versijā, ir zināma problēma.</span><span class="sxs-lookup"><span data-stu-id="382c0-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="382c0-158">Tomēr šī uzvedība netiks mainīta, jo izmaiņas var ietekmēt daudzus dažādus klientu scenārijus.</span><span class="sxs-lookup"><span data-stu-id="382c0-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="382c0-159">Izlaistajā preces informācijā nevar mainīt pievienotos attēlus, kas tika augšupielādēti no produkta dokumentu pielikumu datu elementa.</span><span class="sxs-lookup"><span data-stu-id="382c0-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="382c0-160">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="382c0-160">Issue description</span></span>

<span data-ttu-id="382c0-161">Šī problēma var rasties, pievienojot attēlu krājumam, izmantojot *Preces dokumentu pielikumu* datu elementu.</span><span class="sxs-lookup"><span data-stu-id="382c0-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="382c0-162">Šādā gadījumā krājuma attēls tiek uzrādīts krājumam.</span><span class="sxs-lookup"><span data-stu-id="382c0-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="382c0-163">Tomēr, atlasot **Mainīt attēlu**, nekas netiek norādīts augšupielādēto attēlu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="382c0-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="382c0-164">Turklāt krājumam netiek parādīti pielikumi.</span><span class="sxs-lookup"><span data-stu-id="382c0-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="382c0-165">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="382c0-165">Issue resolution</span></span>

<span data-ttu-id="382c0-166">*EcoResProductDocumentAttachmentEntity* elements (*Preču dokumentu pielikumi*) importē dokumentu pielikumus *precēm*, bet ne *izlaistām precēm*.</span><span class="sxs-lookup"><span data-stu-id="382c0-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="382c0-167">(Izlaistās preces sauc arī par *krājumiem*.) Lai apskatītu preces pielikumus, kas atrodas **Izlaistajā preces informācijas** lapā, jāizmanto *EcoResReleasedProductDocumentAttachmentEntity* elements (*Izlaistās preces dokumentu pielikumi*).</span><span class="sxs-lookup"><span data-stu-id="382c0-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="382c0-168">Microsoft Flow savienotājs rāda šādu kļūdas ziņojumu: "Atjaunināšana nav atļauta laukam 'ProductNumber'."</span><span class="sxs-lookup"><span data-stu-id="382c0-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="382c0-169">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="382c0-169">Issue description</span></span>

<span data-ttu-id="382c0-170">Šī problēma rodas, ja mēģināt atjaunināt **Preces numura** lauku, izmantojot *Izlaisto preču* elementu v2 un Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="382c0-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="382c0-171">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="382c0-171">Issue resolution</span></span>

<span data-ttu-id="382c0-172">Šāda darbība ir paredzama.</span><span class="sxs-lookup"><span data-stu-id="382c0-172">This behavior is expected.</span></span> <span data-ttu-id="382c0-173">Spēja rediģēt izlaistā produkta numuru tika noņemta Dynamics 365 Finance and Operations 10.0.0 ar platformas atjauninājumu 24, lai palīdzētu novērst datu bojājumus.</span><span class="sxs-lookup"><span data-stu-id="382c0-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="382c0-174">Izņēmumos, kad ir nepieciešams labot datu bojājumus, ko radījusi iepriekšēja izlaistās preces primārā atslēga, lūdzu, varat lūgt Microsoft atbalsta personālu, lai pieprasītu šī ierobežojuma pagaidu noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="382c0-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="382c0-175">Nevar izveidot izlaistu preces variantu citā juridiskā personā.</span><span class="sxs-lookup"><span data-stu-id="382c0-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="382c0-176">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="382c0-176">Issue description</span></span>

<span data-ttu-id="382c0-177">Ja mēģināsit izlaist preces šablonu bez variantiem un pēc tam izveidot variantus katrai juridiskajai personai (uzņēmums), kā tas ir nepieciešams, variantus nevar izlaist, izmantojot variantu ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="382c0-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="382c0-178">Jūs arī nevarēsit manuāli izveidot variantus.</span><span class="sxs-lookup"><span data-stu-id="382c0-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="382c0-179">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="382c0-179">Issue resolution</span></span>

<span data-ttu-id="382c0-180">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="382c0-180">This behavior is by design.</span></span> <span data-ttu-id="382c0-181">Preces šablona un dimensiju attiecības, kuras šablons var veikt, tiek turētas koplietojamā līmenī.</span><span class="sxs-lookup"><span data-stu-id="382c0-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="382c0-182">Tāpēc nevar izveidot pieejamās dimensijas koplietojamam preces šablonam konkrētajā juridiskajā personā, kur šīs dimensijas tiek izlaistas, un tad atkārtot procesu katrā juridiska persona, kurai ir nepieciešamas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="382c0-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="382c0-183">Tā vietā ir jāmaina izlaišanas process, lai pielāgotos izstrādātajam procesam.</span><span class="sxs-lookup"><span data-stu-id="382c0-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="382c0-184">Šeit ir process, lai izlaistu preces.</span><span class="sxs-lookup"><span data-stu-id="382c0-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="382c0-185">Izveidojiet koplietojamu preču šablonu un dimensijas, ko var nodot juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="382c0-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="382c0-186">Izlaist preces juridiskām personām vai nu izmantojot variantu ierosinājumus, vai manuāli pievienojot kombinācijas, kas ir jāatbrīvo.</span><span class="sxs-lookup"><span data-stu-id="382c0-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="382c0-187">Varat arī tieši izveidot izlaisto preci.</span><span class="sxs-lookup"><span data-stu-id="382c0-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="382c0-188">Izlaižot variantu citā uzņēmumā, tiek parādīts šāds kļūdas ziņojums: "Preces variants ar norādītajām dimensijām jau ir izveidots."</span><span class="sxs-lookup"><span data-stu-id="382c0-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="382c0-189">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="382c0-189">Issue description</span></span>

<span data-ttu-id="382c0-190">Ja preces variants jau ir izlaists uzņēmumā A, un jūs mēģināt to izlaist uzņēmumā B, izmantojot pogu **Jauns** lapā **Izlaistie preces varianti**, tiks parādīts šāds kļūdas ziņojums:</span><span class="sxs-lookup"><span data-stu-id="382c0-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="382c0-191">Preces variants ar norādītajām dimensijām jau ir izveidots.</span><span class="sxs-lookup"><span data-stu-id="382c0-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="382c0-192">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="382c0-192">Issue resolution</span></span>

<span data-ttu-id="382c0-193">Poga **Jauns** lapā **Izlaistās preces varianti** izveido variantu un izlaiž to uzņēmuma kontekstā.</span><span class="sxs-lookup"><span data-stu-id="382c0-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="382c0-194">Ja variants jau ir izveidots, nevar izmantot pogu **Jauns**, lai to izlaistu citā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="382c0-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="382c0-195">Lai labotu problēmu, atveriet lapu **Preču šablons** un atlasiet **Izlaistā prece**, lai izlaistu esošo variantu vēlamajā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="382c0-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]