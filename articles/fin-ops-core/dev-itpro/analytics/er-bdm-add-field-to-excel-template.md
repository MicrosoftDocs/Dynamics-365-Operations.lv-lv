---
title: Pievienot jaunus laukus biznesa dokumenta veidnei Microsoft Excel
description: Šajā tēmā sniegta informācija par to, kā pievienot jaunus laukus biznesa dokumenta veidnei Microsoft Excel, izmantojot biznesa dokumentu pārvaldības līdzekli.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 6368d763f44c015a6e85652b1880cfd86ff5ba09
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569025"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="a05d7-103">Pievienot jaunus laukus biznesa dokumenta veidnei Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="a05d7-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a05d7-104">Jūs varat pievienot jaunus laukus veidnei, kas tiek izmantota, lai izveidotu biznesa dokumentus Microsoft Excel formātā.</span><span class="sxs-lookup"><span data-stu-id="a05d7-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="a05d7-105">Šos laukus var pievienot kā vietturus, kas tiek izmantoti, lai aizpildītu ģenerētos dokumentus ar nepieciešamo informāciju no programmas.</span><span class="sxs-lookup"><span data-stu-id="a05d7-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="a05d7-106">Katram laukam, ko pievienojat, varat arī norādīt saistījumu ar datu avotiem, lai norādītu, kādi programmas dati tiks ievadīti laukā, kad veidne tiek lietota biznesa dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="a05d7-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="a05d7-107">Lai iegūtu papildinformāciju par šo līdzekli, aizpildiet šajā tēmā sniegto piemēru.</span><span class="sxs-lookup"><span data-stu-id="a05d7-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="a05d7-108">Šajā piemērā ir parādīts, kā atjaunināt veidni, lai aizpildītu laukus brīvā teksta rēķina veidlapās, kas tiek veidotas.</span><span class="sxs-lookup"><span data-stu-id="a05d7-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="a05d7-109">Biznesa dokumentu pārvaldības konfigurēšana veidņu rediģēšanai</span><span class="sxs-lookup"><span data-stu-id="a05d7-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="a05d7-110">Tā kā biznesa dokumentu pārvaldība (BDP) ir veidota papildus [Elektronisko paziņojumu (EP) pārskatu](general-electronic-reporting.md) sistēmai, pirms varat sākt strādāt ar BDP, ir jākonfigurē obligātie EP un BDP parametri.</span><span class="sxs-lookup"><span data-stu-id="a05d7-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="a05d7-111">Piesakieties Microsoft Dynamics 365 Finance instancei kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="a05d7-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="a05d7-112">Veiciet šādas darbības no piemēra tēmā [Biznesa dokumentu pārvaldības pārskats](er-business-document-management.md):</span><span class="sxs-lookup"><span data-stu-id="a05d7-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="a05d7-113">Konfigurējiet ER parametrus.</span><span class="sxs-lookup"><span data-stu-id="a05d7-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="a05d7-114">Ieslēdziet BDP.</span><span class="sxs-lookup"><span data-stu-id="a05d7-114">Turn on BDM.</span></span>

<span data-ttu-id="a05d7-115">Tagad varat sākt izmantot BDP, lai rediģētu biznesa dokumentu veidnes.</span><span class="sxs-lookup"><span data-stu-id="a05d7-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="a05d7-116">Importēt EP risinājumus, kas satur veidni</span><span class="sxs-lookup"><span data-stu-id="a05d7-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="a05d7-117">Šīs procedūras piemērā tiek izmantots oficiāli publicētais EP risinājums.</span><span class="sxs-lookup"><span data-stu-id="a05d7-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="a05d7-118">Jums ir jāimportē šī risinājuma EP konfigurācijas jūsu pašreizējā Finance instancē.</span><span class="sxs-lookup"><span data-stu-id="a05d7-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="a05d7-119">**Brīvā teksta rēķina (Excel)** EP formāta konfigurācija šajā risinājumā ietver biznesa dokumenta veidni Excel formātā, ko var rediģēt, izmantojot BDP.</span><span class="sxs-lookup"><span data-stu-id="a05d7-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="a05d7-120">Importējiet šīs EP formāta konfigurācijas jaunāko versiju no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a05d7-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="a05d7-121">Atbilstošais EP datu modelis un EP modeļu kartēšanas konfigurācijas tiks importētas automātiski.</span><span class="sxs-lookup"><span data-stu-id="a05d7-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="a05d7-122">Lai iegūtu papildinformāciju par EP konfigurāciju importēšanu, skatiet sadaļu [EP konfigurācijas dzīves cikla pārvaldība](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="a05d7-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![LCS koplietojamo līdzekļu bibliotēkas lapa](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="a05d7-124">Rediģēt EP risinājuma veidni</span><span class="sxs-lookup"><span data-stu-id="a05d7-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="a05d7-125">Pierakstieties kā lietotājs ar piekļuvi darbvietai **Biznesa dokumentu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="a05d7-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="a05d7-126">Atveriet darbvietu **Biznesa dokumentu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="a05d7-126">Open the **Business document management** workspace.</span></span>

    ![Biznesa dokumentu pārvaldības darbvieta](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="a05d7-128">Režģī atlasiet veidni **Brīvā teksta rēķins (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="a05d7-129">Labajā rūtī atlasiet **Jauna veidne**, lai izveidotu jaunu veidni, kas ir balstīta uz atlasīto veidni.</span><span class="sxs-lookup"><span data-stu-id="a05d7-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="a05d7-130">Laukā **Nosaukums** ievadiet **Brīvā teksta rēķins (Excel) Contoso** kā jaunās veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a05d7-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="a05d7-131">Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.</span><span class="sxs-lookup"><span data-stu-id="a05d7-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="a05d7-132">Parādīsies BDP veidnes redaktora lapa.</span><span class="sxs-lookup"><span data-stu-id="a05d7-132">The BDM template editor page appears.</span></span> <span data-ttu-id="a05d7-133">Var lietot Microsoft 365, lai rediģētu atlasīto veidni tiešsaistē iegultajā vadīklā.</span><span class="sxs-lookup"><span data-stu-id="a05d7-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![BDP veidnes redaktora lapa](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="a05d7-135">Pievienot etiķeti jaunam laukam veidnē</span><span class="sxs-lookup"><span data-stu-id="a05d7-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="a05d7-136">BDP veidņu redaktora lapā, Excel lentē cilnē **Skats** atlasiet rediģējamās Excel veidnes izvēles rūtiņas **Virsraksti un režģlīnijas.**</span><span class="sxs-lookup"><span data-stu-id="a05d7-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Atzīmētas izvēles rūtiņas Virsraksti un režģlīnijas](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="a05d7-138">Atlasiet šūnas **E8: F8**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="a05d7-139">Excel lentē, cilnē **Sākums** atlasiet **Sapludināt un centrēt**, lai sapludinātu atlasītās šūnas jaunajā sapludinātā **E8: F8** šūnā.</span><span class="sxs-lookup"><span data-stu-id="a05d7-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="a05d7-140">Sapludinātajā šūnā **E8: F8** ievadiet **URL**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="a05d7-141">Atlasiet sapludināto šūnu **E7:F7**, atlasiet **Formāta kopētājs**, tad atlasiet sapludināto šūnu **E8:F8** tādā pašā veidā, kā sapludināto šūnu **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Veidnei pievienota jauna lauka etiķete](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="a05d7-143">Veidnes formatēšana, lai rezervētu vietu jaunam laukam</span><span class="sxs-lookup"><span data-stu-id="a05d7-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="a05d7-144">Lapā BDP veidnes redaktora lapā atlasiet sapludināto šūnu **G8: H8.**</span><span class="sxs-lookup"><span data-stu-id="a05d7-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="a05d7-145">Excel lentē, cilnē **Sākums** atlasiet **Sapludināt un centrēt**, lai sapludinātu atlasītās šūnas jaunajā sapludinātā **G8: H8** šūnā.</span><span class="sxs-lookup"><span data-stu-id="a05d7-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="a05d7-146">Atlasiet sapludināto šūnu **G7:H7**, atlasiet **Formāta kopētājs**, tad atlasiet sapludināto šūnu **G8:H8** tādā pašā veidā, kā sapludināto šūnu **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Jaunajam laukam rezervētā vieta](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="a05d7-148">Laukā **Nosaukums** atlasiet **CompanyInfo.**</span><span class="sxs-lookup"><span data-stu-id="a05d7-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="a05d7-149">Pašreizējās **Excel** veidnes CompanyInfo diapazons ietver visus laukus, kas tiek izmantoti, lai aizpildītu ģenerētā pārskata galveni ar detalizētu informāciju par pašreizējo uzņēmumu kā pārdevēja pusi.</span><span class="sxs-lookup"><span data-stu-id="a05d7-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![Atlasīts CompanyInfo diapazons](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="a05d7-151">Pievienot veidnei jaunu lauku</span><span class="sxs-lookup"><span data-stu-id="a05d7-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="a05d7-152">**BDP veidnes redaktora** lapā, darbības rūtī atlasiet **Rādīt formātu**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="a05d7-153">Rūtī **Veidnes struktūra** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a05d7-154">Jums ir jāpielāgo tā veidnes sadaļa, ko vēlaties izmantot kā jaunu lauku.</span><span class="sxs-lookup"><span data-stu-id="a05d7-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="a05d7-155">Jūs jau veicāt šo pielāgojumu, formatējot sapludināto šūnu **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Jauna lauka pievienošana veidnei](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="a05d7-157">Atlasiet **Excel\Cell**, lai pievienotu jaunu lauku kā šūnu veidnē.</span><span class="sxs-lookup"><span data-stu-id="a05d7-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="a05d7-158">Varat atlasīt **Excel\Range**, ja vēlaties veidnei pievienot jaunu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="a05d7-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="a05d7-159">Ievadītajā diapazonā var būt vairākas šūnas.</span><span class="sxs-lookup"><span data-stu-id="a05d7-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="a05d7-160">Šīs šūnas var pievienot vēlāk.</span><span class="sxs-lookup"><span data-stu-id="a05d7-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="a05d7-161">Ņemiet vērā, ka **CompanyInfo** veidnes komponents tiek automātiski atlasīts rūtī **Veidnes struktūras**, jo tas ir vispiemērotākais pamatelements pašreizējās veidnes struktūrā laukam, kuru pievienojat.</span><span class="sxs-lookup"><span data-stu-id="a05d7-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="a05d7-162">Laukā **Excel diapazons** ievadiet **CompanyURL_Value.**</span><span class="sxs-lookup"><span data-stu-id="a05d7-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="a05d7-163">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-163">Select **OK**.</span></span>

    ![Veidnes struktūrai pievienotais CompanyURL_Value lauks](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="a05d7-165">Rūtī **Veidnes struktūras** atlasiet daudzpunktes pogu (...) un pēc tam atlasiet **Rādīt saistījumus**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Saistījumu atlasīšana parādīta](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="a05d7-167">Tagad rūtī **Veidnes struktūra** ir redzami datu avoti, kas ir pieejami pamata EP formātā.</span><span class="sxs-lookup"><span data-stu-id="a05d7-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="a05d7-168">Atlasiet **CompanyInfo_Value** kā lauku, ko plānojat saistīt ar pamata EP formāta datu avotu.</span><span class="sxs-lookup"><span data-stu-id="a05d7-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="a05d7-169">Rūts **Veidnes struktūra** sadaļā **Datu avoti** izvērsiet **Modelis \> InvoiceBase \> CompanyInfo.**</span><span class="sxs-lookup"><span data-stu-id="a05d7-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="a05d7-170">Elementā **CompanyInfo** atlasiet vienumu **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Atlasīts vienums WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="a05d7-172">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-172">Select **Bind**.</span></span>
11. <span data-ttu-id="a05d7-173">Rūtī **Veidnes struktūra** atlasiet **Saglabāt** un pēc tam aizveriet BDP veidnes redaktora lapu.</span><span class="sxs-lookup"><span data-stu-id="a05d7-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="a05d7-174">Darbvietā **Biznesa dokumentu pārvaldība**, cilnes **Veidne** cilne labajā rūtī rāda atjaunināto veidni.</span><span class="sxs-lookup"><span data-stu-id="a05d7-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="a05d7-175">Režģī ievērojiet, ka rediģētās veidnes lauks **Statuss** ir mainīts **Melnraksts**, un lauks **Pārskatījums** vairs nav tukšs.</span><span class="sxs-lookup"><span data-stu-id="a05d7-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="a05d7-176">Šīs izmaiņas nozīmē to, ka šīs veidnes rediģēšanas process ir uzsākts.</span><span class="sxs-lookup"><span data-stu-id="a05d7-176">These changes indicate that the process of editing this template has been started.</span></span>

![Rediģētā veidne biznesa dokumentu pārvaldības darbvietā](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="a05d7-178">Uzņēmuma iestatījumu pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="a05d7-178">Review company settings</span></span>

1.  <span data-ttu-id="a05d7-179">Dodieties uz **Organizācijas administrēšanas \> Organizācijas \> Juridiskās personas**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="a05d7-180">Kopsavilkuma cilnē **Kontaktinformācija** pārbaudiet, vai ir ievadīts uzņēmuma URL.</span><span class="sxs-lookup"><span data-stu-id="a05d7-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Juridiskās personas lapā ievadītais uzņēmuma vietrādis URL](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="a05d7-182">Ģenerēt biznesa dokumentus, lai pārbaudītu atjaunināto veidni</span><span class="sxs-lookup"><span data-stu-id="a05d7-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="a05d7-183">Programmā mainiet uzņēmumu uz **USMF** un dodieties uz **Debitoru parādi \> Rēķini \> Visi brīvā teksta rēķini.**</span><span class="sxs-lookup"><span data-stu-id="a05d7-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="a05d7-184">Atlasiet rēķinu **FTI-00000002** un pēc tam atlasiet **Drukāšanas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="a05d7-185">Kreisajā rūtī izvērtiet **Modulis - debitori \> Parādu dokumenti \> Brīvā teksta rēķins**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="a05d7-186">Sadaļā **Brīvā teksta rēķins**, atlasiet līmeni **Sākotnējais dokuments**, lai norādītu rēķinu tvērumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="a05d7-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="a05d7-187">Labajā rūtī, laukā **Pārskata formāts** atlasiet veidni **Brīvā teksta rēķins (Excel) Contoso** norādītajam dokumenta līmenim.</span><span class="sxs-lookup"><span data-stu-id="a05d7-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Atlasīta bezmaksas teksta veidne (Excel) Contoso](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="a05d7-189">Nospiediet taustiņu **Esc**, lai aizvērtu pašreizējo lapu.</span><span class="sxs-lookup"><span data-stu-id="a05d7-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="a05d7-190">Atlasīt **Drukāt \> Izvēlēts**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="a05d7-191">Lejupielādējiet ģenerēto dokumentu un atveriet to programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="a05d7-191">Download the generated document, and open it in Excel.</span></span>

    ![Bezmaksas teksta rēķins programmā Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="a05d7-193">Modificētā veidne tiek izmantota, lai ģenerētu brīva teksta rēķina pārskatu atlasītajam vienumam.</span><span class="sxs-lookup"><span data-stu-id="a05d7-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="a05d7-194">Lai analizētu, kā šo pārskatu ietekmēja jūsu ieviestās izmaiņas veidnē, varat palaist šo pārskatu vienā lietojumprogrammas sesijā uzreiz pēc tam, kad esat mainījis veidni citā lietojumprogrammas sesijā.</span><span class="sxs-lookup"><span data-stu-id="a05d7-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="a05d7-195">Saistītās saites</span><span class="sxs-lookup"><span data-stu-id="a05d7-195">Related links</span></span>

[<span data-ttu-id="a05d7-196">Elektronisko ziņojumu (ER) pārskats</span><span class="sxs-lookup"><span data-stu-id="a05d7-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a05d7-197">Biznesa dokumentu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="a05d7-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="a05d7-198">Izveidot konfigurāciju atskaišu ģenerēšanai formātā OPENXML</span><span class="sxs-lookup"><span data-stu-id="a05d7-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]