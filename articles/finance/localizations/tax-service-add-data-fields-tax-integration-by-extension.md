---
title: Pievienot datu laukus nodokļu integrācijai, izmantojot paplašinājumus
description: Šajā tēmā skaidrots, kā izmantot X++ paplašinājumus datu lauku pievienošanai nodokļu integrācijā.
author: qire
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: acbe8070424febf24883362448ea56857d9d72d9
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323577"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Pievienot datu laukus nodokļu integrācijai, izmantojot paplašinājumu

[!include [banner](../includes/banner.md)]


Šajā tēmā skaidrots, kā izmantot X++ paplašinājumus datu lauku pievienošanai nodokļu integrācijā. Šos laukus var paplašināt līdz nodokļu pakalpojuma nodokļu datu modelim un izmantot nodokļu kodu noteikšanai. Papildinformāciju skatiet [Datu lauku pievienošana nodokļu konfigurācijās](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Datu modelis

Dati datu modelī tiek pārnesti ar objektiem un ieviesti klasēs.

Šeit ir galveno objektu saraksts:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Šajā ilustrācijā parādīts, kā šie objekti ir saistīti.

[![Datu modeļa objekta attiecības.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Objektā **Dokuments** var būt daudzi objekti **Rindas**. Katrs objekts satur nodokļu pakalpojuma metadatus.

- `TaxIntegrationDocumentObject` ir `originAddress` metadati, kas satur informāciju par avota adresi, un `includingTax` metadati, kas norāda, vai rindas summa ietver nodokli.
- `TaxIntegrationLineObject` ir `itemId`, `quantity`, un `categoryId` metadati.

> [!NOTE]
> `TaxIntegrationLineObject` ievieš arī objektus **Maksa**.

## <a name="integration-flow"></a>Integrācijas plūsma

Plūsmas datus ietekmē aktivitātes.

### <a name="key-activities"></a>Galvenās aktivitātes

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Aktivitātes tiek izpildītas šādā secībā:

1. Izgūšanas iestatīšana
2. Datu izgūšana
3. Aprēķinu pakalpojums
4. Valūtas maiņa
5. Datu caurlaidība

Piemēram, paplašināt **Datu izgūšana** pirms **Aprēķina pakalpojums**.

#### <a name="data-retrieval-activities"></a>Datu izgūšanas aktivitātes

**Datu izgūšanas** aktivitātes iegūst datus no datu bāzes. Adapteri dažādām darījumiem ir pieejami, lai izgūtu datus no dažādām darījumu tabulām:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

Šajās **Datu izgūšanas** aktivitātes dati tiek kopēti no datu bāzes uz `TaxIntegrationDocumentObject` un `TaxIntegrationLineObject`. Tā kā visas šīs aktivitātes paplašina vienu abstraktās veidnes klasi, tām ir kopīgas metodes.

#### <a name="calculation-service-activities"></a>Aprēķina pakalpojuma aktivitātes

Aktivitāte **Aprēķina pakalpojums** ir saite starp nodokļu pakalpojumiem un nodokļu integrāciju. Šī aktivitāte ir atbildīga par šādām funkcijām:

1. Pieprasījuma konstruēšana.
2. Grāmatojiet pieprasījumu nodokļu pakalpojumam.
3. Saņemt nodokļu iestādes atbildi.
4. Parsējiet atbildi.

Datu lauks, ko pievienojat pieprasījumam, tiks grāmatots kopā ar citiem metadatiem. 

## <a name="extension-implementation"></a>Paplašinājuma ieviešana

Šajā sadaļā sniegtas detalizētas darbības, kas skaidro kā ieviest paplašinājumu. Tas kā piemērus izmanto finanšu dimensijas **Izmaksu centrs** un **Projekts**.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>1. darbība. Pievienot datu mainīgo objekta klasē

Objekta klase satur datu mainīgo un datu ieguves/iestatīšanas metodes. Pievienojiet datu lauku vai nu `TaxIntegrationDocumentObject` vai `TaxIntegrationLineObject` atkarībā no lauka līmeņa. Šajā piemērā tiek izmantots rindu līmenis, bet faila nosaukums ir `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Ja datu lauks, ko pievienojat, ir dokumenta līmenī, mainiet faila nosaukumu uz `TaxIntegrationDocumentObject_Extension.xpp`.

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

**Izmaksu centrs** un **Projekts** tiek pievienoti kā privāti mainīgie. Izveidojiet ieguves un iestatīšanas metodes šiem datu laukiem, lai manipulētu ar datiem.

### <a name="step-2-retrieve-data-from-the-database"></a>2. darbība. Iegūt datus no datu bāzes

Norādiet transakciju un paplašināt atbilstošas adaptera klases, lai izgūtu datus. Piemēram, ja izmantojat transakciju **Pirkšanas pasūtījums**, jāpaplašina `TaxIntegrationPurchTableDataRetrieval` un `TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` ir pārmantots no `TaxIntegrationPurchTableDataRetrieval`. To nedrīkst mainīt, ja atšķiras `purchTable` un `purchParmTable` tabulu loģika.

Ja datu lauks jāpievieno visām transakcijām, paplašiniet visas `DataRetrieval` klases.

Tā kā visas **Datu izgūšanas** aktivitātes paplašina vienu un to pašu veidnes klasi, klases struktūras, mainīgos, un metodes ir līdzīgas.

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

Šajā piemērā parādīta pamatstruktūra, kad tiek izmantota tabula `PurchTable`.

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

Pēc metodes `CopyToDocument` izsaukšanas `this.purchTable` buferis jau pastāv. Šīs metodes mērķis ir kopēt visus nepieciešamos datus no `this.purchTable` uz objektu `document`, izmantojot iestatītāja metodi, kas izveidota `DocumentObject` klasē.

Tāpat arī buferis `this.purchLine` jau pastāv `CopyToLine` metodē. Šīs metodes mērķis ir kopēt visus nepieciešamos datus no `this.purchLine` uz objektu `_line`, izmantojot iestatītāja metodi, kas izveidota `LineObject` klasē.

Taisnākā pieeja ir paplašināt `CopyToDocument` un `CopyToLine` metodes. Tomēr ieteicams vispirms pamēģināt `copyToDocumentFromHeaderTable` un `copyToLineFromLineTable` metodes. Ja tie nedarbojas kā vajadzīgs, ieviesiet savu metodi un izsauciet to `CopyToDocument` un `CopyToLine`. Ir trīs parastās situācijas, kur šo pieeju var izmantot:

- Nepieciešamais lauks ir `PurchTable` vai `PurchLine`. Šādā gadījumā var paplašināt `copyToDocumentFromHeaderTable` un `copyToLineFromLineTable`. Šeit ir parauga kods.

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

- Nepieciešamie dati nav transakciju noklusējuma tabulā. Tomēr ar noklusējuma tabulu ir dažas apvienotas attiecības, un lauks ir nepieciešams lielākajā daļā rindu. Šādā gadījumā aizstājiet `getDocumentQueryObject` vai `getLineObject`, lai vaicātu tabulu pēc savienojuma attiecībām. Šajā piemērā lauks **Piegādāt tagad** ir integrēts ar pārdošanas pasūtījumu rindu līmenī.

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

    Šajā piemērā buferis `mcrSalesLineDropShipment` tiek deklarēts un vaicājums ir definēts `getLineQueryObject`. Vaicājums izmanto attiecības `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Kamēr šajā situācijā paplašinās, varat aizstāt `getLineQueryObject` ar savu izveidoto vaicājuma objektu. Taču ņemiet vērā šādus punktus:

    * Tā kā metodes `getLineQueryObject` atgrieztā vērtība ir `SysDaQueryObject`, šis objekts jāizveido, izmantojot SysDa pieeju.
    * Nevar noņemt pastāvošu tabulu.

- Nepieciešamie dati ir saistīti ar transakciju tabulu, izmantojot sarežģītu savienojuma relāciju, vai arī relācija nav viena ar vienu (1:1), bet gan viena ar daudziem (1:N). Šādā situācijā lietas kļūst mazliet sarežģītākas. Situācija attiecas uz finanšu dimensiju piemēru. 

    Šādā gadījumā var ieviest savu metodi, lai izgūtu datus. Šeit ir parauga kods `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` failā.

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

### <a name="step-3-add-data-to-the-request"></a>3. darbība. Pievienot datus pieprasījumam

Paplašinā `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` vai `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` metodi, lai pievienotu datus pieprasījumam. Šeit ir parauga kods `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` failā.

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

Šajā kodā `_destination` ir ievietošanas objekts, kas tiek izmantots, lai ģenerētu grāmatošanas pieprasījumu, un `_source` ir `TaxIntegrationLineObject` objekts.

> [!NOTE]
> Definējiet atslēgu, ko pieprasījuma formā izmanto kā **privātus konstantes soļus**. Virknei ir jābūt tieši tādai pašai kā tēmā pievienotais mēra nosaukums. [Pievienojiet datu laukus nodokļu konfigurācijās](tax-service-add-data-fields-tax-configurations.md).
> Iestatiet lauku metodē **copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine**, izmantojot **metodi SetField**. Otrā parametra datu tipam ir jābūt **virknei**. Ja datu tips nav virkne, **konvertējiet** to.
> Ja X++ uzskaitījuma **tips ir** paplašināts, atzīmējiet starpību starp tā vērtību, iezīmi un nosaukumu.
> 
>   - Uzskaitījuma vērtība ir vesels skaitlis.
>   - Uzskaitījuma iezīme var atšķirties dažādās izvēlētās valodās. Neizmantojiet enum2Str **,** lai pārveidotu uzskaitījuma tipu par virkni.
>   - Enum nosaukums ir ieteicams, jo tas ir fiksēts. **enum2Symbol** var lietot, lai pārvērstu uzskaitījumu tā nosaukumā. Nodokļu konfigurācijā pievienotai uzskaitījuma vērtībai jābūt tieši tādai pašai kā uzskaitījuma nosaukumam.

## <a name="model-dependency"></a>Modeļa atkarība

Lai projektu varētu sekmīgi izveidot, pievienojiet modeļa atkarībām šādus atsauces modeļus:

- Forma Application No
- Lietojumprogrammas objektu
- Nodokļu programma
- Dimensijas, ja tiek izmantota finanšu dimensija
- Citi nepieciešamie modeļi, uz ko ir atsauce

## <a name="validation"></a>Validācija

Pēc iepriekšējo darbību veikšanas jūs varat apstiprināt savas izmaiņas.

1. Finansēs dodieties uz **sadaļu Parādi kreditoriem** **un pievienojiet vietrādim &debug=vsCconfirmExit%2>** vietrādim URL. Piemēram,https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&. Galaprodukts **&** ir būtisks.
2. Atveriet pirkšanas **pasūtījuma** lapu un atlasiet Jauns, **lai** izveidotu pirkšanas pasūtījumu.
3. Iestatiet vērtību pielāgotajā laukā un pēc tam atlasiet **PVN**. Traucējummeklēšanas fails ar prefiksu **TaxServiceTroubleshootingLog tiek** lejupielādēts automātiski. Šajā failā ir ietverta darbību informācija, kas grāmatota nodokļu aprēķina pakalpojumā. 
4. Pārbaudiet, vai pielāgotais lauks ir pievienots nodokļu pakalpojuma **aprēķina ievades JSON sadaļā** un vai tā vērtība ir pareiza. Ja vērtība nav pareiza, veiciet dubultklikšķi uz soļiem šajā dokumentā.

Faila piemērs:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>Pielikums

Šajā pielikums parāda pilnīgu parauga kodu finanšu dimensiju, izmaksu **centra un** projekta **integrācijai** rindu līmenī.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

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
