---
title: Izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu
description: Šajā tēmā ir paskaidrots, kā izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d076aa5230437d1ef90f6b46d49ee4dea526db24
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104233"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="4008e-103">Izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu</span><span class="sxs-lookup"><span data-stu-id="4008e-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="4008e-104">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="4008e-104">Prerequisites</span></span>

<span data-ttu-id="4008e-105">Lai varētu izpildīt šajā tēmā aprakstītās darbības, ir jāpārliecinās, ka tālāk norādītie uzdevumi tika izpildīti.</span><span class="sxs-lookup"><span data-stu-id="4008e-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="4008e-106">Galvenās akreditācijas datu glabātavas resursa veidošana risinājumā Azure.</span><span class="sxs-lookup"><span data-stu-id="4008e-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="4008e-107">Plašāku informāciju skatiet sadaļā [Par Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="4008e-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="4008e-108">Izveidot Azure krātuves kontu (BLOB Storage).</span><span class="sxs-lookup"><span data-stu-id="4008e-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="4008e-109">Papildinformāciju skatiet šeit: [Azure krātuves konta uzturēšana](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="4008e-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="4008e-110">Pārskats</span><span class="sxs-lookup"><span data-stu-id="4008e-110">Overview</span></span>

<span data-ttu-id="4008e-111">Šajā tēmā jūs veiksiet divas galvenās darbības:</span><span class="sxs-lookup"><span data-stu-id="4008e-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="4008e-112">Iestatiet Azure krātuves kontu, lai iegūtu krātuves konta URI.</span><span class="sxs-lookup"><span data-stu-id="4008e-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="4008e-113">Iestatiet galveno akreditācijas datu glabātavu, lai saglabātu krātuves konta URI.</span><span class="sxs-lookup"><span data-stu-id="4008e-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="4008e-114">Iestatiet Azure krātuves kontu, lai iegūtu krātuves konta URI</span><span class="sxs-lookup"><span data-stu-id="4008e-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="4008e-115">Atveriet krātuves kontu, ko plānojat izmantot kopā ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="4008e-115">Open the storage account that you plan to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="4008e-116">Dodieties uz **BLOB pakalpojums** \> **Konteineri** un izveidojiet jaunu konteineru.</span><span class="sxs-lookup"><span data-stu-id="4008e-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="4008e-117">Ievadiet konteinera nosaukumu un iestatiet lauku **Publiskās piekļuves līmenis** uz **Privāts (nav anonīmas piekļuves)**.</span><span class="sxs-lookup"><span data-stu-id="4008e-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="4008e-118">Atveriet konteineru un dodieties uz **Iestatījumi \> Piekļuves politika**.</span><span class="sxs-lookup"><span data-stu-id="4008e-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="4008e-119">Atlasiet **Pievienot politiku**, lai pievienotu saglabāto piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="4008e-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="4008e-120">Pēc nepieciešamības iestatiet laukus **Identifikators** un **Atļaujas**.</span><span class="sxs-lookup"><span data-stu-id="4008e-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="4008e-121">Laukā **Atļaujas** jāatlasa visas atļaujas.</span><span class="sxs-lookup"><span data-stu-id="4008e-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![BLOB krātuves atļaujas piešķiršana](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="4008e-123">Ievadiet sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="4008e-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="4008e-124">Beigu datumam ir jābūt nākotnē.</span><span class="sxs-lookup"><span data-stu-id="4008e-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="4008e-125">Atlasiet **Labi**, lai saglabātu politiku, un pēc tam saglabājiet izmaiņas konteinerā.</span><span class="sxs-lookup"><span data-stu-id="4008e-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="4008e-126">Atgriezieties krātuves kontā un atveriet **Storage Explorer (priekšskatījums)**.</span><span class="sxs-lookup"><span data-stu-id="4008e-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="4008e-127">Ar peles labo pogu noklikšķiniet uz konteinera un pēc tam atlasiet **Iegūt koplietojamās piekļuves parakstu**.</span><span class="sxs-lookup"><span data-stu-id="4008e-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="4008e-128">Dialoglodziņā **Koplietotas piekļuves paraksts** kopējiet un saglabājiet vērtību laukā **URI**.</span><span class="sxs-lookup"><span data-stu-id="4008e-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="4008e-129">Šī vērtība tiks izmantota nākamajā procedūrā, un tā tiks saukta par *koplietojamās piekļuves paraksta URI*.</span><span class="sxs-lookup"><span data-stu-id="4008e-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![Atlasīt un kopēt URI vērtību](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="4008e-131">Iestatiet galveno akreditācijas datu glabātavu, lai saglabātu krātuves konta URI</span><span class="sxs-lookup"><span data-stu-id="4008e-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="4008e-132">Atveriet galveno akreditācijas datu glabātavu, ko plānojat izmantot kopā ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="4008e-132">Open the key vault that you intend to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="4008e-133">Dodieties uz **Iestatījumi** \> **Noslēpumi** un pēc tam atlasiet **Ģenerēt/Importēt**, lai izveidotu jaunu noslēpumu.</span><span class="sxs-lookup"><span data-stu-id="4008e-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="4008e-134">Lapā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāls**.</span><span class="sxs-lookup"><span data-stu-id="4008e-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="4008e-135">Ievadiet noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="4008e-135">Enter the name of the secret.</span></span> <span data-ttu-id="4008e-136">Šis nosaukums tiks izmantots, iestatot pakalpojumu regulatīvās konfigurācijas pakalpojumā (Regulatory Configuration Service - RCS), un tas tiks saukts par *galvenās akreditācijas datu glabātavas nosaukums*.</span><span class="sxs-lookup"><span data-stu-id="4008e-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="4008e-137">Laukā **Vērtība** atlasiet **Koplietojamās piekļuves paraksta URI** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="4008e-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="4008e-138">Iestatiet piekļuves politiku, lai elektronisko rēķinu izrakstīšanas pievienojumprogrammai piešķirtu pareizu drošas piekļuves līmeni jūsu izveidotajam noslēpumam.</span><span class="sxs-lookup"><span data-stu-id="4008e-138">Set up the access policy to grant the Electronic invoicing add-on the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="4008e-139">Dodieties uz **Iestatījumi \> Piekļuves politika** un atlasiet **Pievienot piekļuves politiku**.</span><span class="sxs-lookup"><span data-stu-id="4008e-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="4008e-140">Iestatiet noslēpuma atļaujas operācijām **Iegūt** un **Uzskaitīt**.</span><span class="sxs-lookup"><span data-stu-id="4008e-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Pakalpojumu piekļuves piešķiršana](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="4008e-142">Iestatiet sertifikāta atļaujas operācijām **Iegūt** un **Uzskaitīt**.</span><span class="sxs-lookup"><span data-stu-id="4008e-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Sertifikāta atļaujas piešķiršana](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="4008e-144">Dialoglodziņā **Galvēnais** atlasiet galvēno, pievienojot **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.</span><span class="sxs-lookup"><span data-stu-id="4008e-144">In the **Principal** dialog box, select the principal by adding **Electronic invoicing add-on**.</span></span>
10. <span data-ttu-id="4008e-145">Atlasiet **Pievienot** un pēc tam atlasiet **Saglabāt Key Vault izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="4008e-145">Select **Add**, and then select **Save Key Vault changes**.</span></span>
11. <span data-ttu-id="4008e-146">Lapā **Pārskats** nokopējiet vērtību **DNS nosaukums** galvenajai akreditācijas datu glabātavai.</span><span class="sxs-lookup"><span data-stu-id="4008e-146">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="4008e-147">Šī vērtība tiks izmantota pakalpojuma iestatīšanas laikā ar RCS un tiks saukta par *galveno galvenajās akreditācijas datu glabātavas URI*.</span><span class="sxs-lookup"><span data-stu-id="4008e-147">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>
