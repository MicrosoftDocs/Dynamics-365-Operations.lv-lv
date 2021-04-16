---
title: Pievienot datu laukus nodokļu integrācijai, izmantojot paplašinājumus
description: Šajā tēmā skaidrots, kā izmantot X++ paplašinājumus datu lauku pievienošanai nodokļu integrācijā.
author: qire
ms.date: 03/26/2021
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
ms.openlocfilehash: fdf112bbdd5245d19ab1d07cfcf94c58bf8208c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830344"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="7556e-103">Pievienot datu laukus nodokļu integrācijai, izmantojot paplašinājumu</span><span class="sxs-lookup"><span data-stu-id="7556e-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7556e-104">Šajā tēmā skaidrots, kā izmantot X++ paplašinājumus datu lauku pievienošanai nodokļu integrācijā.</span><span class="sxs-lookup"><span data-stu-id="7556e-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="7556e-105">Šos laukus var paplašināt līdz nodokļu pakalpojuma nodokļu datu modelim un izmantot nodokļu kodu noteikšanai.</span><span class="sxs-lookup"><span data-stu-id="7556e-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="7556e-106">Papildinformāciju skatiet [Datu lauku pievienošana nodokļu konfigurācijās](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7556e-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="7556e-107">Datu modelis</span><span class="sxs-lookup"><span data-stu-id="7556e-107">Data model</span></span>

<span data-ttu-id="7556e-108">Dati datu modelī tiek pārnesti ar objektiem un ieviesti klasēs.</span><span class="sxs-lookup"><span data-stu-id="7556e-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="7556e-109">Šeit ir galveno objektu saraksts:</span><span class="sxs-lookup"><span data-stu-id="7556e-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="7556e-110">AxClass/TaxIntegration **Dokuments** objekts</span><span class="sxs-lookup"><span data-stu-id="7556e-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="7556e-111">AxClass/TaxIntegration **Rinda** objekts</span><span class="sxs-lookup"><span data-stu-id="7556e-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="7556e-112">AxClass/TaxIntegration **TaxLine** objekts</span><span class="sxs-lookup"><span data-stu-id="7556e-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="7556e-113">Šajā ilustrācijā parādīts, kā šie objekti ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="7556e-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="7556e-114">[![Datu modeļa objekta attiecības](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="7556e-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="7556e-115">Objektā **Dokuments** var būt daudzi objekti **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="7556e-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="7556e-116">Katrs objekts satur nodokļu pakalpojuma metadatus.</span><span class="sxs-lookup"><span data-stu-id="7556e-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="7556e-117">`TaxIntegrationDocumentObject` ir `originAddress` metadati, kas satur informāciju par avota adresi, un `includingTax` metadati, kas norāda, vai rindas summa ietver nodokli.</span><span class="sxs-lookup"><span data-stu-id="7556e-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="7556e-118">`TaxIntegrationLineObject` ir `itemId`, `quantity`, un `categoryId` metadati.</span><span class="sxs-lookup"><span data-stu-id="7556e-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="7556e-119">`TaxIntegrationLineObject` ievieš arī objektus **Maksa**.</span><span class="sxs-lookup"><span data-stu-id="7556e-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="7556e-120">Integrācijas plūsma</span><span class="sxs-lookup"><span data-stu-id="7556e-120">Integration flow</span></span>

<span data-ttu-id="7556e-121">Plūsmas datus ietekmē aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="7556e-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="7556e-122">Galvenās aktivitātes</span><span class="sxs-lookup"><span data-stu-id="7556e-122">Key activities</span></span>

* <span data-ttu-id="7556e-123">AxClass/TaxIntegration **Aprēķins** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="7556e-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="7556e-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="7556e-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="7556e-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="7556e-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="7556e-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="7556e-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="7556e-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="7556e-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="7556e-128">Aktivitātes tiek izpildītas šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="7556e-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="7556e-129">Izgūšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7556e-129">Setting Retrieval</span></span>
2. <span data-ttu-id="7556e-130">Datu izgūšana</span><span class="sxs-lookup"><span data-stu-id="7556e-130">Data Retrieval</span></span>
3. <span data-ttu-id="7556e-131">Aprēķinu pakalpojums</span><span class="sxs-lookup"><span data-stu-id="7556e-131">Calculation Service</span></span>
4. <span data-ttu-id="7556e-132">Valūtas maiņa</span><span class="sxs-lookup"><span data-stu-id="7556e-132">Currency Exchange</span></span>
5. <span data-ttu-id="7556e-133">Datu caurlaidība</span><span class="sxs-lookup"><span data-stu-id="7556e-133">Data Persistence</span></span>

<span data-ttu-id="7556e-134">Piemēram, paplašināt **Datu izgūšana** pirms **Aprēķina pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="7556e-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="7556e-135">Datu izgūšanas aktivitātes</span><span class="sxs-lookup"><span data-stu-id="7556e-135">Data Retrieval activities</span></span>

<span data-ttu-id="7556e-136">**Datu izgūšanas** aktivitātes iegūst datus no datu bāzes.</span><span class="sxs-lookup"><span data-stu-id="7556e-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="7556e-137">Adapteri dažādām darījumiem ir pieejami, lai izgūtu datus no dažādām darījumu tabulām:</span><span class="sxs-lookup"><span data-stu-id="7556e-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="7556e-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="7556e-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="7556e-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="7556e-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="7556e-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="7556e-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="7556e-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="7556e-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="7556e-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="7556e-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="7556e-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="7556e-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="7556e-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="7556e-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="7556e-145">Šajās **Datu izgūšanas** aktivitātes dati tiek kopēti no datu bāzes uz `TaxIntegrationDocumentObject` un `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="7556e-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="7556e-146">Tā kā visas šīs aktivitātes paplašina vienu abstraktās veidnes klasi, tām ir kopīgas metodes.</span><span class="sxs-lookup"><span data-stu-id="7556e-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="7556e-147">Aprēķina pakalpojuma aktivitātes</span><span class="sxs-lookup"><span data-stu-id="7556e-147">Calculation Service activities</span></span>

<span data-ttu-id="7556e-148">Aktivitāte **Aprēķina pakalpojums** ir saite starp nodokļu pakalpojumiem un nodokļu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="7556e-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="7556e-149">Šī aktivitāte ir atbildīga par šādām funkcijām:</span><span class="sxs-lookup"><span data-stu-id="7556e-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="7556e-150">Pieprasījuma konstruēšana.</span><span class="sxs-lookup"><span data-stu-id="7556e-150">Construct the request.</span></span>
2. <span data-ttu-id="7556e-151">Grāmatojiet pieprasījumu nodokļu pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="7556e-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="7556e-152">Saņemt nodokļu iestādes atbildi.</span><span class="sxs-lookup"><span data-stu-id="7556e-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="7556e-153">Parsējiet atbildi.</span><span class="sxs-lookup"><span data-stu-id="7556e-153">Parse the response.</span></span>

<span data-ttu-id="7556e-154">Datu lauks, ko pievienojat pieprasījumam, tiks grāmatots kopā ar citiem metadatiem.</span><span class="sxs-lookup"><span data-stu-id="7556e-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="7556e-155">Paplašinājuma ieviešana</span><span class="sxs-lookup"><span data-stu-id="7556e-155">Extension implementation</span></span>

<span data-ttu-id="7556e-156">Šajā sadaļā sniegtas detalizētas darbības, kas skaidro kā ieviest paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="7556e-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="7556e-157">Tas kā piemērus izmanto finanšu dimensijas **Izmaksu centrs** un **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="7556e-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="7556e-158">1. darbība.</span><span class="sxs-lookup"><span data-stu-id="7556e-158">Step 1.</span></span> <span data-ttu-id="7556e-159">Pievienot datu mainīgo objekta klasē</span><span class="sxs-lookup"><span data-stu-id="7556e-159">Add the data variable in the object class</span></span>

<span data-ttu-id="7556e-160">Objekta klase satur datu mainīgo un datu ieguves/iestatīšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="7556e-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="7556e-161">Pievienojiet datu lauku vai nu `TaxIntegrationDocumentObject` vai `TaxIntegrationLineObject` atkarībā no lauka līmeņa.</span><span class="sxs-lookup"><span data-stu-id="7556e-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="7556e-162">Šajā piemērā tiek izmantots rindu līmenis, bet faila nosaukums ir `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="7556e-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="7556e-163">Ja datu lauks, ko pievienojat, ir dokumenta līmenī, mainiet faila nosaukumu uz `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="7556e-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="7556e-164">**Izmaksu centrs** un **Projekts** tiek pievienoti kā privāti mainīgie.</span><span class="sxs-lookup"><span data-stu-id="7556e-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="7556e-165">Izveidojiet ieguves un iestatīšanas metodes šiem datu laukiem, lai manipulētu ar datiem.</span><span class="sxs-lookup"><span data-stu-id="7556e-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="7556e-166">2. darbība.</span><span class="sxs-lookup"><span data-stu-id="7556e-166">Step 2.</span></span> <span data-ttu-id="7556e-167">Iegūt datus no datu bāzes</span><span class="sxs-lookup"><span data-stu-id="7556e-167">Retrieve data from the database</span></span>

<span data-ttu-id="7556e-168">Norādiet transakciju un paplašināt atbilstošas adaptera klases, lai izgūtu datus.</span><span class="sxs-lookup"><span data-stu-id="7556e-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="7556e-169">Piemēram, ja izmantojat transakciju **Pirkšanas pasūtījums**, jāpaplašina `TaxIntegrationPurchTableDataRetrieval` un `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="7556e-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="7556e-170">`TaxIntegrationPurchParmTableDataRetrieval` ir pārmantots no `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="7556e-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="7556e-171">To nedrīkst mainīt, ja atšķiras `purchTable` un `purchParmTable` tabulu loģika.</span><span class="sxs-lookup"><span data-stu-id="7556e-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="7556e-172">Ja datu lauks jāpievieno visām transakcijām, paplašiniet visas `DataRetrieval` klases.</span><span class="sxs-lookup"><span data-stu-id="7556e-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="7556e-173">Tā kā visas **Datu izgūšanas** aktivitātes paplašina vienu un to pašu veidnes klasi, klases struktūras, mainīgos, un metodes ir līdzīgas.</span><span class="sxs-lookup"><span data-stu-id="7556e-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="7556e-174">Šajā piemērā parādīta pamatstruktūra, kad tiek izmantota tabula `PurchTable`.</span><span class="sxs-lookup"><span data-stu-id="7556e-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="7556e-175">Pēc metodes `CopyToDocument` izsaukšanas `this.purchTable` buferis jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="7556e-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="7556e-176">Šīs metodes mērķis ir kopēt visus nepieciešamos datus no `this.purchTable` uz objektu `document`, izmantojot iestatītāja metodi, kas izveidota `DocumentObject` klasē.</span><span class="sxs-lookup"><span data-stu-id="7556e-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="7556e-177">Tāpat arī buferis `this.purchLine` jau pastāv `CopyToLine` metodē.</span><span class="sxs-lookup"><span data-stu-id="7556e-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="7556e-178">Šīs metodes mērķis ir kopēt visus nepieciešamos datus no `this.purchLine` uz objektu `_line`, izmantojot iestatītāja metodi, kas izveidota `LineObject` klasē.</span><span class="sxs-lookup"><span data-stu-id="7556e-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="7556e-179">Taisnākā pieeja ir paplašināt `CopyToDocument` un `CopyToLine` metodes.</span><span class="sxs-lookup"><span data-stu-id="7556e-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="7556e-180">Tomēr ieteicams vispirms pamēģināt `copyToDocumentFromHeaderTable` un `copyToLineFromLineTable` metodes.</span><span class="sxs-lookup"><span data-stu-id="7556e-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="7556e-181">Ja tie nedarbojas kā vajadzīgs, ieviesiet savu metodi un izsauciet to `CopyToDocument` un `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="7556e-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="7556e-182">Ir trīs parastās situācijas, kur šo pieeju var izmantot:</span><span class="sxs-lookup"><span data-stu-id="7556e-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="7556e-183">Nepieciešamais lauks ir `PurchTable` vai `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="7556e-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="7556e-184">Šādā gadījumā var paplašināt `copyToDocumentFromHeaderTable` un `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="7556e-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="7556e-185">Šeit ir parauga kods.</span><span class="sxs-lookup"><span data-stu-id="7556e-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="7556e-186">Nepieciešamie dati nav transakciju noklusējuma tabulā.</span><span class="sxs-lookup"><span data-stu-id="7556e-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="7556e-187">Tomēr ar noklusējuma tabulu ir dažas apvienotas attiecības, un lauks ir nepieciešams lielākajā daļā rindu.</span><span class="sxs-lookup"><span data-stu-id="7556e-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="7556e-188">Šādā gadījumā aizstājiet `getDocumentQueryObject` vai `getLineObject`, lai vaicātu tabulu pēc savienojuma attiecībām.</span><span class="sxs-lookup"><span data-stu-id="7556e-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="7556e-189">Šajā piemērā lauks **Piegādāt tagad** ir integrēts ar pārdošanas pasūtījumu rindu līmenī.</span><span class="sxs-lookup"><span data-stu-id="7556e-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="7556e-190">Šajā piemērā buferis `mcrSalesLineDropShipment` tiek deklarēts un vaicājums ir definēts `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="7556e-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="7556e-191">Vaicājums izmanto attiecības `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="7556e-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="7556e-192">Kamēr šajā situācijā paplašinās, varat aizstāt `getLineQueryObject` ar savu izveidoto vaicājuma objektu.</span><span class="sxs-lookup"><span data-stu-id="7556e-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="7556e-193">Taču ņemiet vērā šādus punktus:</span><span class="sxs-lookup"><span data-stu-id="7556e-193">However, note the following points:</span></span>

    * <span data-ttu-id="7556e-194">Tā kā metodes `getLineQueryObject` atgrieztā vērtība ir `SysDaQueryObject`, šis objekts jāizveido, izmantojot SysDa pieeju.</span><span class="sxs-lookup"><span data-stu-id="7556e-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="7556e-195">Nevar noņemt pastāvošu tabulu.</span><span class="sxs-lookup"><span data-stu-id="7556e-195">Can't remove existed table.</span></span>

- <span data-ttu-id="7556e-196">Nepieciešamie dati ir saistīti ar transakciju tabulu, izmantojot sarežģītu savienojuma relāciju, vai arī relācija nav viena ar vienu (1:1), bet gan viena ar daudziem (1:N).</span><span class="sxs-lookup"><span data-stu-id="7556e-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="7556e-197">Šādā situācijā lietas kļūst mazliet sarežģītākas.</span><span class="sxs-lookup"><span data-stu-id="7556e-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="7556e-198">Situācija attiecas uz finanšu dimensiju piemēru.</span><span class="sxs-lookup"><span data-stu-id="7556e-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="7556e-199">Šādā gadījumā var ieviest savu metodi, lai izgūtu datus.</span><span class="sxs-lookup"><span data-stu-id="7556e-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="7556e-200">Šeit ir parauga kods `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` failā.</span><span class="sxs-lookup"><span data-stu-id="7556e-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="7556e-201">3. darbība.</span><span class="sxs-lookup"><span data-stu-id="7556e-201">Step 3.</span></span> <span data-ttu-id="7556e-202">Pievienot datus pieprasījumam</span><span class="sxs-lookup"><span data-stu-id="7556e-202">Add data to the request</span></span>

<span data-ttu-id="7556e-203">Paplašinā `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` vai `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` metodi, lai pievienotu datus pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="7556e-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="7556e-204">Šeit ir parauga kods `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` failā.</span><span class="sxs-lookup"><span data-stu-id="7556e-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="7556e-205">Šajā kodā `_destination` ir ievietošanas objekts, kas tiek izmantots, lai ģenerētu grāmatošanas pieprasījumu, un `_source` ir `TaxIntegrationLineObject` objekts.</span><span class="sxs-lookup"><span data-stu-id="7556e-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="7556e-206">Definējiet atslēgu, kas pieprasījuma veidlapā tiek izmantota kā `private const str`.</span><span class="sxs-lookup"><span data-stu-id="7556e-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="7556e-207">Iestatiet metodes `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` lauku, izmantojot `SetField` metodi.</span><span class="sxs-lookup"><span data-stu-id="7556e-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="7556e-208">Otrā parametra datu tipam jābūt `string`.</span><span class="sxs-lookup"><span data-stu-id="7556e-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="7556e-209">Ja datu tips nav `string`, konvertējiet to par `string`.</span><span class="sxs-lookup"><span data-stu-id="7556e-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="7556e-210">Pielikums</span><span class="sxs-lookup"><span data-stu-id="7556e-210">Appendix</span></span>

<span data-ttu-id="7556e-211">Šajā pielikumā ir parādīts pilns parauga kods finanšu dimensiju integrēšanai (**Izmaksu centrs** un **Projekts**) rindas līmenī.</span><span class="sxs-lookup"><span data-stu-id="7556e-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="7556e-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="7556e-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="7556e-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="7556e-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="7556e-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="7556e-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
