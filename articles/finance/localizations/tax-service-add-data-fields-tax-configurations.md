---
title: Pievienot datu laukus nodokļu konfigurācijās
description: Šajā tēmā skaidrots, kā pielāgot nodokļu konfigurācijas, pievienojot datu laukus.
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819428"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="c649f-103">Pievienot datu laukus nodokļu konfigurācijās</span><span class="sxs-lookup"><span data-stu-id="c649f-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c649f-104">Šajā tēmā skaidrots, kā pielāgot nodokļu konfigurācijas, izmantojot [datu laukus, kas pievienoti nodokļu integrācijai](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="c649f-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="c649f-105">Nodoku datu modeļa pielāgošana</span><span class="sxs-lookup"><span data-stu-id="c649f-105">Customize the tax data model</span></span>

1. <span data-ttu-id="c649f-106">Pakalpojumā Microsoft Dynamics 365 Finance dodieties uz **Elektroniskie pārskati** \> **Nodokļu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="c649f-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="c649f-107">Konfigurācijas kokā atlasiet **Nodokļu datu modelis - Eiropa**.</span><span class="sxs-lookup"><span data-stu-id="c649f-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="c649f-108">Pēc tam darbību rūtī atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="c649f-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="c649f-109">Nolaižamajā dialoglodziņā atlasiet opciju **Ar nodokli apliekamais dokumenta modelis, kas atvasināts no nosaukuma: nodokļu datu modelis - Eiropa, Microsoft**, ievadiet jaunā nodokļu datu modeļa nosaukumu un pēc tam atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="c649f-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="c649f-110">Atlasiet tikko izveidoto nodokļu datu modeli un pēc tam darbību rūtī atlasiet **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="c649f-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="c649f-111">Izvērsiet datu modeļa koku, atlasiet **Rindas** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c649f-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="c649f-112">Dialoglodziņā **Mezgla izveide** ievadiet nosaukumu, norādiet krājuma tipu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="c649f-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="c649f-113">Pievienojiet vajadzīgās kolonnas.</span><span class="sxs-lookup"><span data-stu-id="c649f-113">Add any required columns.</span></span>
8. <span data-ttu-id="c649f-114">Darbības rūtī atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="c649f-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="c649f-115">Aizveriet lapu un skatiet nodokļu datu modeļa pabeigto versiju.</span><span class="sxs-lookup"><span data-stu-id="c649f-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="c649f-116">Nodokļa pielāgošanas konfigurācija</span><span class="sxs-lookup"><span data-stu-id="c649f-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="c649f-117">Pakalpojumā Finance dodieties uz **Elektroniskie pārskati** \> **Nodokļu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="c649f-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="c649f-118">Konfigurācijas kokā atlasiet **Nodokļu configurācija - Eiropa**.</span><span class="sxs-lookup"><span data-stu-id="c649f-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="c649f-119">Pēc tam darbību rūtī atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="c649f-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="c649f-120">Nolaižamajā dialoglodziņā atlasiet opciju **Nodokļu pakalpojuma konfigurācija, kas atvasināta no nosaukuma: nodokļu konfigurācija - Eiropa, Microsoft**, ievadiet jaunā nodokļu konfigurācijas nosaukumu un pēc tam atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="c649f-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="c649f-121">Atlasiet tikko izveidoto nodokļu konfigurāciju un pēc tam darbību rūtī atlasiet **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="c649f-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="c649f-122">Sadaļā **Rekvizīti**, laukā **Datu modelis** atlasiet iepriekš izveidoto pielāgoto nodokļu datu modeli.</span><span class="sxs-lookup"><span data-stu-id="c649f-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="c649f-123">Laukā **Datu modeļa versijas** atlasiet nodokļu datu modeļa pabeigto versiju.</span><span class="sxs-lookup"><span data-stu-id="c649f-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="c649f-124">Atlasiet **Pievienot** un pievienojiet nepieciešamos nodokļu pasākumus.</span><span class="sxs-lookup"><span data-stu-id="c649f-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="c649f-125">Darbības rūtī atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="c649f-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="c649f-126">Aizveriet lapu un skatiet nodokļu konfigurācijas pabeigto versiju.</span><span class="sxs-lookup"><span data-stu-id="c649f-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="c649f-127">Pielāgotajā nodokļu konfigurācijā ieviest nodokļu līdzekļus</span><span class="sxs-lookup"><span data-stu-id="c649f-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="c649f-128">Pakalpojumā Regulatory Configuration Service (RCS) atvēriet **Globalizācijas līdzekļi** \> **Nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="c649f-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="c649f-129">Atlasiet **Pievienot**, ievadiet informāciju par jauno līdzekli un pēc tam atlasiet **Izveidot līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="c649f-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="c649f-130">Cilnē **Versijas** atlasiet līdzekli un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c649f-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="c649f-131">Cilnē **Vispārīgi**, laukā **Konfigurācijas versija** atlasiet pielāgoto nodokļu konfigurāciju un versiju.</span><span class="sxs-lookup"><span data-stu-id="c649f-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="c649f-132">Dialoglodziņā **Pārvaldīt kolonnas** atlasiet virsrakstu un rindu kolonnas, kuras vēlaties iekļaut pielāgotajā nodokļu pasākumā, un pēc tam atlasiet labo bultiņas pogu, lai tos pievienotu sarakstam **Atlasītās kolonnas**.</span><span class="sxs-lookup"><span data-stu-id="c649f-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>