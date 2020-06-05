---
title: Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā
description: Šī tēma sniedz informāciju par to, kā veidot elektronisko pārskatu (ER) formātu, lai aizpildītu Excel veidni un pēc tam ģenerētu izejošos Excel formāta dokumentus.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375817"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="5ca50-103">Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā</span><span class="sxs-lookup"><span data-stu-id="5ca50-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5ca50-104">Varat izveidot [elektroniskās ziņošanas (ER)](general-electronic-reporting.md) formāta konfigurāciju, kurai ir ER [formāta komponents](general-electronic-reporting.md#FormatComponentOutbound), ko varat konfigurēt, lai izveidotu izejošo dokumentu Microsoft Excel darbgrāmatas formātā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="5ca50-105">Šim nolūkam jāizmanto īpaši ER formāta komponenti.</span><span class="sxs-lookup"><span data-stu-id="5ca50-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="5ca50-106">Lai uzzinātu vairāk par šo līdzekli, sekojiet norādījumiem tēmā [Noformēt konfigurāciju, lai veidotu pārskatus OPENXML formātā](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5ca50-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="5ca50-107">Jauna ER formāta pievienošana</span><span class="sxs-lookup"><span data-stu-id="5ca50-107">Add a new ER format</span></span>

<span data-ttu-id="5ca50-108">Kad pievienojat jaunu ER formāta konfigurāciju, lai ģenerētu izejošo dokumentu Excel darbgrāmatas formātā, ir vai nu jāatlasa **Excel** vērtība **Formāta veida** atribūtam, vai nu jāatstāj **formāta veida** atribūtu tukšu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="5ca50-109">Ja atlasāt **Excel**, jūs varat konfigurēt formātu, lai ģenerētu izejošo dokumentu tikai Excel formātā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="5ca50-110">Ja atstājat atribūtu tukšu, varat konfigurēt formātu, lai ģenerētu izejošo dokumentu jebkurā formātā, ko atbalsta ER struktūra.</span><span class="sxs-lookup"><span data-stu-id="5ca50-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="5ca50-111">Lai konfigurētu konfigurācijas ER formāta komponentu, darbību rūtī atlasiet **Veidotājs** un atveriet ER formāta komponentu rediģēšanai ER operāciju veidotājā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Lapa Konfigurācijas](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="5ca50-113">Excel faila komponents</span><span class="sxs-lookup"><span data-stu-id="5ca50-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="5ca50-114">Manuāla ievade</span><span class="sxs-lookup"><span data-stu-id="5ca50-114">Manual entry</span></span>

<span data-ttu-id="5ca50-115">Jums ir jāpievieno **Excel\\Fails** komponents konfigurētajam ER formātam, lai ģenerētu izejošo dokumentu Excel formātā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel\Faila komponents](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="5ca50-117">Lai norādītu izejošā dokumenta izkārtojumu, pievienojiet Excel darbgrāmatu, kam ir paplašinājums .xlsx, **Excel\\Faila** komponentam kā veidni izejošajiem dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="5ca50-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca50-118">Manuāli pievienojot veidni, jāizmanto [dokumenta veids](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), kas ir konfigurēts šim nolūkam [ER parametros](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="5ca50-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Pielikuma pievienošana Excel\Faila komponentam](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="5ca50-120">Lai norādītu, kā pievienotā veidne tiks aizpildīta, palaižot konfigurēto ER formātu, ir jāpievieno ligzdotas **Lapas**, **Diapazona** un **Šūnas** komponenti **Excel\\Faila** komponentam.</span><span class="sxs-lookup"><span data-stu-id="5ca50-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="5ca50-121">Katram ligzdotajam komponentam ir jābūt saistītam ar Excel nosaukto krājumu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="5ca50-122">Veidnes importēšana</span><span class="sxs-lookup"><span data-stu-id="5ca50-122">Template import</span></span>

<span data-ttu-id="5ca50-123">Varat atlasīt **Importēt no Excel** darbību rūts cilnē **Importēt**, lai importētu jaunu veidni tukšā ER formātā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="5ca50-124">Šajā piemērā **Excel\\Faila** komponents tiks izveidots automātiski, un importētā veidne tiks tai pievienota.</span><span class="sxs-lookup"><span data-stu-id="5ca50-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="5ca50-125">Visi vajadzīgie ER komponenti arī tiks izveidoti automātiski, balstoties uz Excel nosaukto vienumu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Opcijas Importēt no Excel atlasīšana](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="5ca50-127">Ja vēlaties izveidot izvēles **Lapas** elementu rediģējamajā ER formātā, iestatiet opciju **Izveidot Excel lapas formāta elementu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5ca50-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="5ca50-128">Lapas komponents</span><span class="sxs-lookup"><span data-stu-id="5ca50-128">Sheet component</span></span>

<span data-ttu-id="5ca50-129">**Lapas** komponents norāda pievienotās Excel darbgrāmatas darblapu, kas ir jāaizpilda.</span><span class="sxs-lookup"><span data-stu-id="5ca50-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="5ca50-130">Darblapas nosaukums Excel veidnē ir definēts šī komponenta **Lapas** rekvizītā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca50-131">Šis komponents nav obligāts Excel darbgrāmatām, kurās ir ietverta viena darblapa.</span><span class="sxs-lookup"><span data-stu-id="5ca50-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="5ca50-132">ER operācijas veidotāja cilnē **Kartēšana** varat konfigurēt **Iespējoto** rekvizītu **Lapas** komponentam, lai norādītu, vai komponents ir jāievieto ģenerētajā dokumentā:</span><span class="sxs-lookup"><span data-stu-id="5ca50-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="5ca50-133">Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Patiess** izpildlaikā, vai arī, ja neviena izteiksme nav konfigurēta vispār, izveidotajā dokumentā tiks ievietota atbilstoša darblapa.</span><span class="sxs-lookup"><span data-stu-id="5ca50-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="5ca50-134">Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, ģenerētajā dokumentā netiks ietverta darblapa.</span><span class="sxs-lookup"><span data-stu-id="5ca50-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Lapas komponenta piemērs](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="5ca50-136">Diapazona komponents</span><span class="sxs-lookup"><span data-stu-id="5ca50-136">Range component</span></span>

<span data-ttu-id="5ca50-137">**Diapazona** komponents norāda Excel diapazons, kas ir jākontrolē šim ER komponentam.</span><span class="sxs-lookup"><span data-stu-id="5ca50-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="5ca50-138">Diapazona nosaukums ir definēts šī komponenta **Excel diapazona** rekvizītā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="5ca50-139">**Replicēšanas virziena** rekvizīts norāda, vai un kā diapazons tiks atkārtots ģenerētajā dokumentā:</span><span class="sxs-lookup"><span data-stu-id="5ca50-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="5ca50-140">Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Bez replikācijas**, atbilstošais Excel diapazons netiks atkārtots ģenerētajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="5ca50-141">Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Vertikāls**, atbilstošais Excel diapazons tiks atkārtots ģenerētajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="5ca50-142">Katrs replicētais diapazons tiek ievietots zem sākotnējā diapazona Excel veidnē.</span><span class="sxs-lookup"><span data-stu-id="5ca50-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="5ca50-143">Atkārtojumu skaits tiek noteikts pēc ierakstu skaita **Ierakstu saraksta** tipa datu avotā, kas ir saistīts ar šo ER komponentu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="5ca50-144">Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Horizontāls**, atbilstošais Excel diapazons tiks atkārtots ģenerētajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="5ca50-145">Katrs replicētais diapazons tiek ievietots pa labi no sākotnējā diapazona Excel veidnē.</span><span class="sxs-lookup"><span data-stu-id="5ca50-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="5ca50-146">Atkārtojumu skaits tiek noteikts pēc ierakstu skaita **Ierakstu saraksta** tipa datu avotā, kas ir saistīts ar šo ER komponentu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="5ca50-147">Lai iegūtu vairāk informācijas par horizontālo replicēšanu, sekojiet soļiem sadaļā [Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas Excel pārskatos](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="5ca50-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="5ca50-148">**Diapazona** komponentā var būt citi ligzdotie ER komponenti, kas tiek izmantoti, lai ievadītu vērtības atbilstošajos Excel nosauktajos diapazonos.</span><span class="sxs-lookup"><span data-stu-id="5ca50-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="5ca50-149">Ja kāds **Teksta** grupas komponents tiek izmantots vērtību ievadīšanai, vērtība tiek ievadīta Excel diapazonā kā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="5ca50-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ca50-150">Izmantojiet šo modeli, lai formatētu ievadītās vērtības, pamatojoties uz lietojumprogrammā definēto lokalizāciju.</span><span class="sxs-lookup"><span data-stu-id="5ca50-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="5ca50-151">Ja **Excel** grupas **Šūnas** komponents tiek izmantots vērtību ievadīšanai, šī vērtība tiek ievadīta Excel diapazonā kā datu tipa vērtība, kas tiek definēta, saistot šo **Šūnas** komponentu (piemēram, **Virkne**, **Reāls** vai **Vesels skaitlis**).</span><span class="sxs-lookup"><span data-stu-id="5ca50-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ca50-152">Izmantojiet šo modeli, lai iespējotu Excel programmu, lai formatētu ievadītās vērtības, pamatojoties uz vietējā datora lokalizāciju, kas atver izejošo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="5ca50-153">ER operācijas veidotāja cilnē **Kartēšana** varat konfigurēt **Iespējoto** rekvizītu **Diapazona** komponentam, lai norādītu, vai komponents ir jāievieto ģenerētajā dokumentā:</span><span class="sxs-lookup"><span data-stu-id="5ca50-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="5ca50-154">Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Patiess** izpildlaikā, vai arī, ja neviena izteiksme nav konfigurēta vispār, izveidotajā dokumentā tiks aizpildīts diapazons.</span><span class="sxs-lookup"><span data-stu-id="5ca50-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="5ca50-155">Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, un, ja šis diapazons nepārstāv visas rindas un kolonnas, izveidotajā dokumentā diapazons netiks aizpildīts.</span><span class="sxs-lookup"><span data-stu-id="5ca50-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="5ca50-156">Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, un šis diapazons pārstāv visas rindas un kolonnas, izveidotajā dokumentā šīs rindas un kolonnas būs slēptas rindas un kolonnas.</span><span class="sxs-lookup"><span data-stu-id="5ca50-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="5ca50-157">Šūnas komponents</span><span class="sxs-lookup"><span data-stu-id="5ca50-157">Cell component</span></span>

<span data-ttu-id="5ca50-158">**Šūnas** komponents tiek izmantots, lai aizpildītu Excel nosauktās šūnas, formas un attēlus.</span><span class="sxs-lookup"><span data-stu-id="5ca50-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="5ca50-159">Lai norādītu Excel nosaukto objektu, kas jāaizpilda ar **Šūnas** ER komponentu, jums ir jānorāda šī objekta nosaukums **Šūnas** komponenta **Excel diapazona** rekvizītā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="5ca50-160">ER operācijas veidotāja cilnē **Kartēšana** varat konfigurēt **Iespējoto** rekvizītu **Šūnas** komponentam, lai norādītu, vai objekts ir jāaizpilda ģenerētajā dokumentā:</span><span class="sxs-lookup"><span data-stu-id="5ca50-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="5ca50-161">Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Patiess** izpildlaikā, vai arī, ja neviena izteiksme nav konfigurēta vispār, izveidotajā dokumentā tiks aizpildīts objekts.</span><span class="sxs-lookup"><span data-stu-id="5ca50-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="5ca50-162">Šīs **Šūnas** komponenta saistījums norāda vērtību, kas tiek ievietota atbilstošajā objektā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="5ca50-163">Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, ģenerētajā dokumentā netiks aizpildīts atbilstošais objekts.</span><span class="sxs-lookup"><span data-stu-id="5ca50-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="5ca50-164">Ja **Šūnas** komponents ir konfigurēts, lai ievadītu vērtību šūnā, tas var būt saistīts ar datu avotu, kas atgriež primitīva datu veida vērtību (piemēram, **Virkne**, **Reāls** vai **Vesels skaitlis**).</span><span class="sxs-lookup"><span data-stu-id="5ca50-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="5ca50-165">Šādā gadījumā vērtība tiek ievadīta šūnā kā tā paša datu veida vērtība.</span><span class="sxs-lookup"><span data-stu-id="5ca50-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="5ca50-166">Ja **Šūnas** komponents ir konfigurēts, lai ievadītu vērtību Excel formā, tas var būt saistīts ar datu avotu, kas atgriež primitīva datu veida vērtību (piemēram, **Virkne**, **Reāls** vai **Vesels skaitlis**).</span><span class="sxs-lookup"><span data-stu-id="5ca50-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="5ca50-167">Šādā gadījumā vērtība tiek ievadīta Excel formā kā tā pašas formas teksts.</span><span class="sxs-lookup"><span data-stu-id="5ca50-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="5ca50-168">Datu veidu vērtībām, kas nav **Virkne**, konvertēšana uz tekstu tiek veikta automātiski.</span><span class="sxs-lookup"><span data-stu-id="5ca50-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca50-169">Jūs varat konfigurēt **Šūnas** komponentu, lai aizpildītu formu tikai gadījumos, kad tiek atbalstīts formas teksta rekvizīts.</span><span class="sxs-lookup"><span data-stu-id="5ca50-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="5ca50-170">Ja **Šūnas** komponents ir konfigurēts, lai ievadītu vērtību Excel attēlā, tas var būt saistīts ar datu avotu, kas **Konteinera** datu veida vērtību, kas pārstāv attēlu binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="5ca50-171">Šādā gadījumā vērtība tiek ievadīta Excel attēlā kā attēls.</span><span class="sxs-lookup"><span data-stu-id="5ca50-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca50-172">Katrs Excel attēls un forma tiek uzskatīta par noenkurotu pie tā augšējā kreisā stūra uz noteiktu Excel šūnu vai diapazonu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="5ca50-173">Ja vēlaties replicēt Excel attēlu vai formu, ir jākonfigurē šūna vai diapazons, kas tiek noenkurots kā replicēta šūna vai diapazons.</span><span class="sxs-lookup"><span data-stu-id="5ca50-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="5ca50-174">Papildinformāciju par attēlu un formu iegulšanu skatiet sadaļā [Attēlu un formu iegulšana dokumentos, kas tiek ģenerēti, izmantojot ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="5ca50-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="5ca50-175">Lappuses pārtraukuma komponents</span><span class="sxs-lookup"><span data-stu-id="5ca50-175">Page break component</span></span>

<span data-ttu-id="5ca50-176">**Lappuses pārtraukuma** komponents liek programmai Excel sākt jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="5ca50-177">Šis komponents nav nepieciešams, ja vēlaties izmantot programmas Excel noklusējuma lapošanu, bet to vajadzētu izmantot, ja vēlaties, lai Excel seko savam ER formātam struktūras lapošanai.</span><span class="sxs-lookup"><span data-stu-id="5ca50-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="5ca50-178">Rediģēt pievienoto ER formātu</span><span class="sxs-lookup"><span data-stu-id="5ca50-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="5ca50-179">Veidnes atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5ca50-179">Update a template</span></span>

<span data-ttu-id="5ca50-180">Varat atlasīt **Atjaunināt no Excel** darbību rūts cilnē **Importēt**, lai importētu atjauninātu veidni rediģējamā ER formātā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="5ca50-181">Šī procesa laikā atlasītā **Excel\\Faila** komponenta veidne tiks aizstāta ar jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="5ca50-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="5ca50-182">Rediģējamā ER formāta saturs tiks sinhronizēts ar atjauninātās ER veidnes saturu.</span><span class="sxs-lookup"><span data-stu-id="5ca50-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="5ca50-183">Jauns ER formāta komponents tiks automātiski izveidots katram Excel nosaukumam, ja ER formāta komponents nav atrasts rediģējamā formātā.</span><span class="sxs-lookup"><span data-stu-id="5ca50-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="5ca50-184">Katrs ER formāta komponents tiks dzēsts no rediģējamā ER formāta, ja tam nav atrasts atbilstošais Excel nosaukums.</span><span class="sxs-lookup"><span data-stu-id="5ca50-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="5ca50-185">Ja vēlaties izveidot izvēles **Lapas** elementu rediģējamajā ER formātā, iestatiet opciju **Izveidot Excel lapas formāta elementu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5ca50-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="5ca50-186">Ja rediģējamais ER formāts sākotnēji ietvēra **Lapas** elementus, ieteicams iestatīt opciju **Izveidot Excel lapas formāta elementu** uz **Jā**, importējot atjauninātu veidni.</span><span class="sxs-lookup"><span data-stu-id="5ca50-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="5ca50-187">Pretējā gadījumā visi oriģinālās **Lapas** elementa ligzdotie elementi tiks izveidoti no nulles.</span><span class="sxs-lookup"><span data-stu-id="5ca50-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="5ca50-188">Tāpēc atjauninātajā ER formātā tiks zaudēti visi atkārtoti izveidoto formāta elementu saistījumi.</span><span class="sxs-lookup"><span data-stu-id="5ca50-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Izveidot Excel lapas formāta elementa opciju dialoglodziņā Atjaunināt no Excel](./media/er-excel-format-update-template.png)

<span data-ttu-id="5ca50-190">Lai uzzinātu vairāk par šo līdzekli, sekojiet soļiem sadaļā [Modificēt elektronisko pārskatu formātus, atkārtoti pielietojot Excel veidnes](modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="5ca50-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="5ca50-191">Pārbaudīt ER formātu</span><span class="sxs-lookup"><span data-stu-id="5ca50-191">Validate an ER format</span></span>

<span data-ttu-id="5ca50-192">Pārbaudot ER formātu, ko var rediģēt, tiek veikta konsekvences pārbaude, lai pārliecinātos, ka Excel nosaukums ir pašlaik izmantotajā Excel veidnē.</span><span class="sxs-lookup"><span data-stu-id="5ca50-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="5ca50-193">Jūs tiksiet informēts par jebkādām neatbilstībām.</span><span class="sxs-lookup"><span data-stu-id="5ca50-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="5ca50-194">Dažām neatbilstībām tiks piedāvāta opcija automātiski labot problēmas.</span><span class="sxs-lookup"><span data-stu-id="5ca50-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Pārbaudes kļūdu ziņojums](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="5ca50-196">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5ca50-196">Additional resources</span></span>

[<span data-ttu-id="5ca50-197">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="5ca50-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="5ca50-198">Izveidot konfigurāciju atskaišu ģenerēšanai formātā OPENXML</span><span class="sxs-lookup"><span data-stu-id="5ca50-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="5ca50-199">Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes</span><span class="sxs-lookup"><span data-stu-id="5ca50-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="5ca50-200">Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas programmas Excel pārskatos</span><span class="sxs-lookup"><span data-stu-id="5ca50-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="5ca50-201">Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER</span><span class="sxs-lookup"><span data-stu-id="5ca50-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="5ca50-202">Elektronisko pārskatu (EP) izveides konfigurēšana, lai pārsūtītu datu uz pakalpojumu Power BI</span><span class="sxs-lookup"><span data-stu-id="5ca50-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
