---
title: Vienotā preču pieredze
description: Šajā tēmā ir aprakstīta produkta datu integrācija starp Finance and Operations lietotājprogrammām un Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9dc26e0e50c0b77555d09e4a50b846c80b1d5760
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249332"
---
# <a name="unified-product-experience"></a>Vienotā preču pieredze

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Ja biznesa ekosistēma ir izveidota no Dynamics 365 lietojumprogrammām, piemēram, Finance, Supply Chain Management un Sales, ir dabiski, ka klienti lieto šīs programmas, lai iegūtu produktu datus. Tas ir tāpēc, ka šīs programmas nodrošina stabilu preču infrastruktūru, kas papildināta ar sarežģītākām cenu noteikšanas koncepcijām un precīziem rīcībā esošajiem krājumu datiem. Klienti, kuri izmanto ārējo Product Lifecycle Management (PLM) sistēmu, lai iegūtu produktu datus, var novirzīt produktus no Finance and Operations lietojumprogrammām uz citām Dynamics 365 lietojumprogrammām. Vienotā preču pieredze nodrošina integrētu preču datu modeli uz Common Data Service, lai visi programmas lietotāji, ieskaitot Power Platform lietotājus, var izmantot bagātīgo preču datu priekšrocības, ko sniedz Finance and Operations lietojumprogrammas.

Lūk, preču datu modelis no Sales.

![Preču pārdošanas datu modelis](media/dual-write-product-4.jpg)

Šeit ir preču datu modelis no Finance and Operations lietojumprogrammas.

![Preču datu modelis Finance and Operations.](media/dual-write-products-5.jpg)

Šie divi preču datu modeļi ir integrēti Common Data Service, kā parādīts zemāk.

![Preču datu modelis Dynamics 365 lietojumprogrammās.](media/dual-write-products-6.jpg)

Dubultās rakstīšanas elementa kartes, kas paredzētas produktiem, ir izveidotas, lai virzītu datus tikai vienā virzienā, un tā ir reāla laika pieredze no Finance and Operations lietojumprogrammas līdz Common Data Service. Tomēr, ja nepieciešams, preču infrastruktūra ir atvērta, lai to izveidotu kā divvirzienu. Klienti to var pielāgot, bet paši uzņemoties atbildību, jo korporācija Microsoft šo pieeju neiesaka.

## <a name="templates"></a>Veidnes

Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas. Kā redzams šajā tabulā, tiek izveidota elementa karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.

Finance and Operations | Citas Dynamics 365 programmas
-----------------------|--------------------------------
Izlaistās preces V2 | msdyn\_sharedproductdetails
CDS izlaistās atšķirīgās preces | Prece
Produkta numura identifikācijas svītrkods | msdyn\_productbarcodes
Pasūtījuma noklusējuma iestatījumi | msdyn\_productdefaultordersettings
Īpaši preču noklusējuma pasūtījuma iestatījumi | msdyn_productspecificdefaultordersettings
Preces dimensiju grupas | msdyn\_productdimensiongroups
Noliktavas dimensiju grupas | msdyn\_productstoragedimensiongroups
Izsekošanas dimensiju grupas | msdyn\_productstoragedimensiongroups
Krāsas | msdyn\_productcolors
Izmēri | msdyn\_productsizes
Stili | msdyn\_productsytles
Konfigurācijas | msdyn\_productconfigurations
Preces šablona krāsas | msdyn_sharedproductcolors
Preces šablona izmēri | msdyn_sharedproductsizes
Preces šablona stili | msdyn_sharedproductstyles
Preces šablona konfigurācijas | msdyn_sharedproductconfigurations
Visas preces | msdyn_globalproducts
Vienība | uoms
Mērvienību pārveidošana | msdyn_ unitofmeasureconversions
Īpaša preces mērvienības konversija | msdyn_productspecificunitofmeasureconversion
Atrašanās vietas | msdyn\_operationalsites
Noliktavas | msdyn\_inventwarehouses

[!include [symbols](../includes/dual-write-symbols.md)]

## <a name="integration-of-products"></a>Preču integrēšana

Šajā modelī preci attēlo divu Common Data Serviceelementu kombinācija: **preces** un **msdyn\_sharedproductdetails**. Tā kā pirmais elements satur preces definīciju (preces unikālais identifikators, preces nosaukums un apraksts), otrais elements ietver laukus, kas tiek glabāti preču līmenī. Šo divu elementu kombinācija tiek izmantota, lai definētu preci atbilstoši krājumu uzskaites vienības (SKU) koncepcijai. Katrai izlaistajai precei būs sava informācija minētajos elementos (Prece un Koplietojamā informācija par preci). Lai izsekotu visām precēm (izlaistas un nav izlaistas), tiek izmantota**Globālā preču** vienība. 

Tā kā produkts tiek attēlots kā SKU, atšķirīgu preču, preču šablonu un preču variantu koncepcijas var uztvert Common Data Servicešādi:

- **Preces ar apakštipa preci** ir preces, kas definētas pašas. Tām nav jādefinē dimensijas. Piemērs ir noteikta grāmata. Šīm precēm viens ieraksts tiek izveidots**Preces** elementā, un viens ieraksts tiek izveidots **msdyn\_sharedproductdetails** elementā. Nav izveidots neviens preču saimes ieraksts.
- **Preču šabloni** tiek izmantoti kā ģenēriskas preces, kas satur definīciju un nosacījumus, kas nosaka biznesa procesu darbību. Balstoties uz šīm definīcijām, var tikt ģenerētas atšķirīgas preces, kas zināmas kā preces varianti. Piemēram, T-krekls ir preces šablons, un tam var būt Krāsa un Izmērs dimensiju veidā. Var izlaist variantus, kuriem ir dažādas šo dimensiju kombinācijas, piemēram, mazs zils T-krekls vai vidēji zaļš T-krekls. Integrācijā katram variantam preču tabulā tiek izveidots viens ieraksts. Šis ieraksts satur ar variantu saistītu informāciju, piemēram, dažādas dimensijas. Vispārīgā informācija par preci tiek uzglabāta **msdyn\_sharedproductdetails** elementā. (Šī vispārīgā informācija tiek turēta preču šablonā.) Papildus tiek izveidots viens produktu saimes ieraksts katram preces šablonam. Preces pamatinformācija tiek sinhronizēta Common Data Service, tiklīdz tiek izveidots izlaistais preces šablons (bet pirms tiek izlaisti varianti).
- **Atšķirīgas preces** attiecas uz visām produktu apakštipa precēm un visiem preces variantiem. 

![Preču datu modelis](media/dual-write-product.png)

Ar iespējotu duālās rakstīšanas funkcionalitāti Finance and Operations lietojumprogrammas tiks sinhronizētas citās Dynamics 365 lietojumprogrammās **Melnraksta** stāvoklī. Tās tiek pievienotas pirmajam cenrādim ar nemainīgu valūtu. Citiem vārdiem, tie ir pievienoti pirmajam cenrādim Dynamics 365 lietojumprogrammā, kas atbilst jūsu juridiskās personas valūtai, kur prece tiek izdota Finance and Operations lietojumprogrammā. 

Lai sinhronizētu preci ar statusu **Aktīvs**, lai varētu to tieši izmantot pārdošanas pasūtījuma piedāvājumos, ir jāizvēlas, piemēram, šāds iestatījums: zem **Sistēma > Administrēšana > Sistēmas administrēšana > Sistēmas iestatījumi > Pārdošana** atlasiet opciju **Izveidot preces aktīvā stāvoklī = Jā**. 

### <a name="cds-released-distinct-products-to-product"></a>CDS izlaistās atšķirīgās preces sadaļā Prece

**Preces** elements satur laukus, kas definē preci. Tā ietver atsevišķas preces (preces ar apakštipa preci) un preces variantus. Tālāk esošajā tabulā parādīta kartēšana.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
PRODUCTNUMBER | >> | productnumber
PRODUCTNAME | >> | name
PRODUCTDESCRIPTION | >> | apraksts
ITEMNUMBER | >> | msdyn_itemnumber
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol
SALESPRICE | >> | vērt.
UNITCOST | >> | currentcost
PRODUCTTYPE | >> | producttypecode
SALESUNITDECIMALPRECISION | >> | quantitydecimal
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTCOLORID | >> | Preces konfigurācija
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle

### <a name="released-products-v2-to-msdyn_sharedproductdetails"></a>V2 izlaistās preces sadaļā msdyn\_sharedproductdetails

**Msdyn\_sharedproductdetails** elements satur laukus no Finance and Operations lietojumprogrammām, kas nosaka preci, un kurās ir ietverta preces finanšu un pārvaldības informācija. Tālāk esošajā tabulā parādīta kartēšana.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
PRODUCTNUMBER | > | msdyn_globalproduct.msdyn_productnumber
INTRASTATCHARGEPERCENTAGE | > | msdyn_intrastatchargepercentage
ITEMNUMBER | >> | msdyn_itemnumber
APPROXIMATESALESTAXPERCENTAGE | > | msdyn_approximatesalestaxpercentage
BESTBEFOREPERIODDAYS | > | msdyn_bestbeforeperioddays
CARRYINGCOSTABCCODE | >> | msdyn_carryingcostabccode
CONSTANTSCRAPQUANTITY | > | msdyn_constantscrapquantity
COSTCHARGESQUANTITY | > | msdyn_costchargesquantity
DEFAULTRECEIVINGQUANTITY | > | msdyn_defaultreceivingquantity
FIXEDPURCHASEPRICECHARGES | > | msdyn_fixedpurchasepricecharges
FIXEDSALESPRICECHARGES | > | msdyn_fixedsalespricecharges
GROSSDEPTH | > | msdyn_grossdepth
GROSSPRODUCTHEIGHT | > | msdyn_grossproductheight
GROSSPRODUCTWIDTH | > | msdyn_grossproductwidth
INVENTORYUNITSYMBOL | > | msdyn_inventoryunitsymbol.msdyn_symbol
ISDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_isdiscountposregistrationprohibited
ISEXEMPTFROMAUTOMATICNOTIFICATIONANDCANCELLATION | >> | msdyn_exemptautomaticnotificationcancel
ISINSTALLMENTELIGIBLE | >> | msdyn_isinstallmenteligible
ISINTERCOMPANYPURCHASEUSAGEBLOCKED | >> | msdyn_isintercompanypurchaseusageblocked
ISINTERCOMPANYSALESUSAGEBLOCKED | >> | msdyn_isintercompanysalesusageblocked
ISMANUALDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_ismanualdiscposregistrationprohibited
ISPHANTOM | >> | msdyn_isphantom
ISPOSREGISTRATIONBLOCKED | >> | msdyn_isposregistrationblocked
ISPOSREGISTRATIONQUANTITYNEGATIVE | >> | msdyn_isposregistrationquantitynegative
ISPURCHASEPRICEAUTOMATICALLYUPDATED | >> | msdyn_ispurchasepriceautomaticallyupdated
ISPURCHASEPRICEINCLUDINGCHARGES | >> | msdyn_ispurchasepriceincludingcharges
ISSALESWITHHOLDINGTAXCALCULATED | >> | msdyn_issaleswithholdingtaxcalculated
ISRESTRICTEDFORCOUPONS | >> | msdyn_isrestrictedforcoupons
ISSALESPRICEADJUSTMENTALLOWED | >> | msdyn_issalespriceadjustmentallowed
ISSALESPRICEINCLUDINGCHARGES | >> | msdyn_issalespriceincludingcharges
ISSCALEPRODUCT | >> | msdyn_isscaleproduct
ISSHIPALONEENABLED | >> | msdyn_isshipaloneenabled
ISUNITCOSTPRODUCTVARIANTSPECIFIC | >> | msdyn_isunitcostproductvariantspecific
ISVARIANTSHELFLABELSPRINTINGENABLED | >> | msdyn_isvariantshelflabelsprintingenabled
ISZEROPRICEPOSREGISTRATIONALLOWED | >> | msdyn_iszeropriceposregistrationallowed
KEYINPRICEREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinpricerequirementsatposregister
KEYINQUANTITYREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinquantityrequirementsatposregister
MARGINABCCODE | >> | msdyn_marginabccode
MAXIMUMPICKQUANTITY | > | msdyn_maximumpickquantity
MUSTKEYINCOMMENTATPOSREGISTER | >> | msdyn_mustkeyincommentatposregister
NECESSARYPRODUCTIONWORKINGTIMESCHEDULINGPROPERTYID | > | msdyn_necessaryproductionworkingtimeschedulingp
NETPRODUCTWEIGHT | > | msdyn_netproductweight
PACKINGDUTYQUANTITY | > | msdyn_packingdutyquantity
POSREGISTRATIONACTIVATIONDATE | > | msdyn_posregistrationactivationdate
POSREGISTRATIONBLOCKEDDATE | > | msdyn_posregistrationblockeddate
POSREGISTRATIONPLANNEDBLOCKEDDATE | > | msdyn_posregistrationplannedblockeddate
POTENCYBASEATTIBUTETARGETVALUE | > | msdyn_potencybaseattibutetargetvalue
POTENCYBASEATTRIBUTEVALUEENTRYEVENT | >> | msdyn_potencybaseattributevalueentryevent
PRODUCTTYPE | >> | msdyn_producttype
PRODUCTIONCONSUMPTIONDENSITYCONVERSIONFACTOR | > | msdyn_productionconsumptiondensityconversion
PRODUCTIONCONSUMPTIONDEPTHCONVERSIONFACTOR | > | msdyn_productionconsumptiondepthconversion
PRODUCTIONCONSUMPTIONHEIGHTCONVERSIONFACTOR | > | msdyn_productionconsumptionheightconversion
PRODUCTIONCONSUMPTIONWIDTHCONVERSIONFACTOR | > | msdyn_productionconsumptionwidthconversion
PRODUCTVOLUME | > | msdyn_productvolume
PURCHASECHARGESQUANTITY | > | msdyn_purchasechargesquantity
PURCHASEOVERDELIVERYPERCENTAGE | > | msdyn_purchaseoverdeliverypercentage
PURCHASEPRICE | > | msdyn_purchaseprice
PURCHASEPRICEDATE | > | msdyn_purchasepricedate
PURCHASEPRICINGPRECISION | > | msdyn_purchasepricingprecision
PURCHASEUNDERDELIVERYPERCENTAGE | > | msdyn_purchaseunderdeliverypercentage
RAWMATERIALPICKINGPRINCIPLE | >> | msdyn_rawmaterialpickingprinciple
SALESCHARGESQUANTITY | > | msdyn_saleschargesquantity
SALESOVERDELIVERYPERCENTAGE | > | msdyn_salesoverdeliverypercentage
SALESPRICE | > | msdyn_salesprice
SALESPRICECALCULATIONCHARGESPERCENTAGE | > | msdyn_salespricecalculationchargespercentage
SALESPRICECALCULATIONCONTRIBUTIONRATIO | > | msdyn_salespricecalculationcontributionratio
SALESPRICECALCULATIONMODEL | >> | msdyn_salespricecalculationmodel
SALESPRICEDATE | > | msdyn_salespricedate
SALESPRICINGPRECISION | > | msdyn_salespricingprecision
SALESUNDERDELIVERYPERCENTAGE | > | msdyn_salesunderdeliverypercentage
SALESUNITSYMBOL | > | msdyn_salesunitsymbol.msdyn_symbol
SCALEINDICATOR | >> | msdyn_scaleindicator
SELLSTARTDATE | > | msdyn_sellstartdate
SHELFADVICEPERIODDAYS | > | msdyn_shelfadviceperioddays
SHELFLIFEPERIODDAYS | > | msdyn_shelflifeperioddays
SHIPSTARTDATE | > | msdyn_shipstartdate
TAREPRODUCTWEIGHT | > | msdyn_tareproductweight
TRANSFERORDEROVERDELIVERYPERCENTAGE | > | msdyn_transferorderoverdeliverypercentage
TRANSFERORDERUNDERDELIVERYPERCENTAGE | > | msdyn_transferorderunderdeliverypercentage
UNITCOST | > | msdyn_unitcost
UNITCOSTDATE | > | msdyn_unitcostdate
UNITCOSTQUANTITY | > | msdyn_unitcostquantity
VARIABLESCRAPPERCENTAGE | > | msdyn_variablescrappercentage
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE1 | > | msdyn_warehousemobiledevicedescriptionline1
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE2 | > | msdyn_warehousemobiledevicedescriptionline2
WILLINVENTORYISSUEAUTOMATICALLYREPORTASFINISHED | >> | msdyn_willinventoryissueautoreportasfinished
WILLINVENTORYRECEIPTIGNOREFLUSHINGPRINCIPLE | >> | msdyn_willinventoryreceiptignoreflushing
WILLPICKINGWORKBENCHAPPLYBOXINGLOGIC | >> | msdyn_willpickingworkbenchapplyboxinglogic
WILLTOTALPURCHASEDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalpurchdiscountcalcincludeproduct
WILLTOTALSALESDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalsalesdiscountcalcincludeproduct
WILLWORKCENTERPICKINGALLOWNEGATIVEINVENTORY | >> | msdyn_willworkcenterpickingallownegativeinvent
YIELDPERCENTAGE | > | msdyn_yieldpercentage
ISUNITCOSTAUTOMATICALLYUPDATED | >> | msdyn_isunitcostautomaticallyupdated
PURCHASEUNITSYMBOL | > | msdyn_purchaseunitsymbol.msdyn_symbol
PURCHASEPRICEQUANTITY | > | msdyn_purchasepricequantity
ISUNITCOSTINCLUDINGCHARGES | >> | msdyn_isunitcostincludingcharges
FIXEDCOSTCHARGES | >> | msdyn_fixedcostcharges
MINIMUMCATCHWEIGHTQUANTITY | >> | msdyn_minimumcatchweightquantity
MAXIMUMCATCHWEIGHTQUANTITY | >> | msdyn_maximumcatchweightquantity
ALTERNATIVEITEMNUMBER | >> | msdyn_alternativeitemnumber.msdyn_itemnumber
BOMUNITSYMBOL | >> | msdyn_bomunitsymbol.msdyn_symbol
CATCHWEIGHTUNITSYMBOL | >> | msdyn_catchweightunitsymbol.msdyn_symbol
COMPARISONPRICEBASEUNITSYMBOL | >> | msdyn_comparisonpricebaseunitsymbol.msdyn_symbol
PRIMARYVENDORACCOUNTNUMBER | >> | msdyn_vendorid.msdyn_vendoraccountnumber
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTDIMENSIONGROUPNAME | >> | msdyn_productdimensiongroupid.msdyn_groupname

## <a name="all-product-to-msdyn_global-products"></a>Visas preces msdyn_global produktiem

Visu preču elements satur visas preces, kas pieejamas Finance and Operations lietojumprogrammās, gan izlaistām, gan neizlaistām precēm. Šie produkti ir pieejamas programmā Common Data Service, izmantojot šādus kartējumus:

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
PRODUCTNAME | >> | msdyn_productname
PRODUCTNUMBER | >> | msdyn_productnumber

## <a name="product-dimensions"></a>Preces dimensijas 

Preču dimensijas ir īpašības, ko izmanto, lai identificētu preces variantu. Četras preces dimensijas (krāsa, lielums, stils un konfigurācija) ir arī kartētas Common Data Service, lai definētu preces variantus. Sekojošajā attēlā ir parādītas preces dimensijas krāsas datu modelis. Tas pats modelis ir piemērots izmēriem, stiliem un konfigurācijām. 

![Preču datu modelis](media/dual-write-product-2.PNG)

### <a name="colors"></a>Krāsas

Iespējamās krāsas ir pieejamas Common Data Service, izmantojot tālāk norādītos kartējumus.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
COLORID | \>\> | msdyn\_productcolorname

### <a name="sizes"></a>Izmēri

Iespējamie izmēri ir pieejami Common Data Service, izmantojot tālāk norādītos kartējumus.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
SIZEID | \>\> | msdyn\_productsize

### <a name="styles"></a>Stili

Iespējamie stili ir pieejami Common Data Service, izmantojot tālāk norādītos kartējumus.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
STYLEID | \>\> | msdyn\_productstyle

### <a name="configurations"></a>Konfigurācijas

Iespējamās konfigurācijas ir pieejamas Common Data Service, izmantojot tālāk norādītos kartējumus.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
CONFIGURATIONID | \>\> | msdyn\_name

Ja precei ir dažādas preces dimensijas (piemēram, preces šablona izmērs un krāsa ir tādas pašas kā preces dimensijas), katra atšķirīga prece (t.i., katrs preču variants) tiek definēta kā šo preču dimensiju kombinācija. Piemēram, preču numurs B0001 ir īpaši mazs, melns T krekls, un preces numurs B0002 ir neliels melns T krekls. Šādā gadījumā tiek definētas esošās preču dimensiju kombinācijas. Piemēram, no iepriekšējā piemēra T-krekls var būt īpaši mazs un melns, mazs un melns, vidējs un melns vai liels un melns, bet tas nevar būt īpaši liels un melns. Citiem vārdiem sakot, preču dimensijas, ko var veikt preces šablons, ir norādītas, un variantus var izlaist, pamatojoties uz šīm vērtībām.

Lai sekotu preču dimensijām, ko var veikt preces šablons, katrai preces dimensijai tiek izveidoti un kartēti Common Data Service tālāk norādītie elementi. Papildinformāciju skatiet rakstā, [Preču informācija](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

### <a name="shared-product-color"></a>Koplietotā preces krāsa

**Koplietojamās preces krāsas** elements norāda krāsas, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Common Data Service, lai saglabātu datus saskaņotus. Tālāk esošajā tabulā parādīta kartēšana.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
PRODUCTCOLORID | \>\> | msdyn\_productcolorid.msdyn\_productcolorname
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_retaildisplayorder

### <a name="shared-product-size"></a>Koplietotais preces izmērs

**Koplietojamās preces izmēra** elements norāda izmērus, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Common Data Service, lai saglabātu datus saskaņotus. Tālāk esošajā tabulā parādīta kartēšana.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
PRODUCTSIZEID | \>\> | msdyn\_productsizeid.msdyn\_productsize
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-style"></a>Koplietotais preces stils

**Koplietojamās preces stila** elements norāda stilus, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Common Data Service, lai saglabātu datus saskaņotus. Tālāk esošajā tabulā parādīta kartēšana.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailsid.msdyn\_itemnumber
PRODUCTSTYLEID | \>\> | msdyn\_productstyleintegration
PRODUCTSTYLEID | \>\> | msdyn\_productstyleid.msdyn\_productstyle
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-configuration"></a>Koplietojamo preču konfigurācija

**Koplietojamo preču konfigurācijas** elements norāda konfigurācijas, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Common Data Service, lai saglabātu datus saskaņotus. Tālāk esošajā tabulā parādīta kartēšana.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
CONTAINERUNITSYMBOL | \>\> | msdyn\_containerunitsymbol
PRODUCTCONFIGURATIONID | \>\> | msdyn\_productconfigurationid.msdyn\_productconfiguration
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

## <a name="product-number-identifier-bar-codes"></a>Preces numura identifikācijas svītrkodi

Preču svītrkodi tiek izmantoti, lai unikāli identificētu preces. Sekojošie kartējumi ir izmantoti, lai padarītu preču svītrkodus pieejamas programmā Common Data Service.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
PRODUCTNUMBER | \> | msdyn\_productnumberid.productnumber
BARCODE | \> | msdyn\_name
BARCODE | \> | msdyn\_barcode
PRODUCTQUANTITY | \> | msdyn\_productquantity
PRODUCTDESCRIPTION | \> | msdyn\_productdescription
BARCODESETUPID | \> | msdyn\_barcodesetupid
PRODUCTQUANTITYUNITSYMBOL | \> | msdyn\_unitofmeasureid.name
ISDEFAULTSCANNEDBARCODE | \>\> | msdyn\_isdefaultscannedbarcode
ISDEFAULTPRINTEDBARCODE | \>\> | msdyn\_isdefaultprintedbarcode
ISDEFAULTDISPLAYEDBARCODE | \>\> | msdyn\_isdefaultdisplayedbarcode

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Noklusējuma pasūtījuma iestatījumi un preces specifiskie noklusējuma iestatījumi

Pasūtījuma noklusējuma iestatījumi definē vietu un noliktavu, kur krājumi tiks iegūti vai glabāti, minimālos, maksimālos, vairākkārtējos un standarta daudzumus, kas tiks izmantoti tirdzniecībai vai krājumu pārvaldībai, izpildes laikus, apturēšanas karodziņus un pasūtījumu solīšanas metodes. Šī informācija būs pieejama kompaktdiskos, izmantojot noklusētos pasūtījuma iestatījumus un preces specifiskos noklusējuma pasūtījuma iestatījumu elementu. Plašāku informāciju par funkcionalitāti varat izlasīt lapā [Noklusējuma pasūtījuma iestatījumu lapa](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings)noklusējuma pasūtījuma iestatījumi.

### <a name="default-order-settings"></a>Pasūtījuma noklusējuma iestatījumi

Sekojošie kartējumi ir izmantoti, lai padarītu noklusējuma pasūtījuma iestatījumus pieejamus programmā Common Data Service.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
INVENTWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory

### <a name="product-specific-default-order-settings"></a>Īpaši preču noklusējuma pasūtījuma iestatījumi

Sekojošie kartējumi ir izmantoti, lai padarītu preces specifiskos noklusējuma pasūtījuma iestatījumus pieejamus programmā Common Data Service.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
INVENTORYWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory
OPERATIONALSITEID | = | msdyn_operationalsite.msdyn_siteid
PRODUCTCOLORID | = | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | = | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | = | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | = | msdyn_productstyle.msdyn_productstyle

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mērvienība un mērvienību pārvēršana

Mērvienības un tās atbilstošie pārveidojumi būs pieejami Common Data Service dekojošajā datu modelī, kas redzams diagrammā.

![Preču datu modelis](media/dual-write-product-3.PNG)

Mērvienības koncepcija ir integrēta starp Finance and Operations un citām Dynamics 365 lietojumprogrammām. Katrai mērvienību klasei Finance and Operations lietojumprogrammā tiek izveidota mērvienību grupa Dynamics 365 lietojumprogrammā, kas satur mērvienības, kas pieder pie mērvienību kategorijas. Katrai vienību grupai tiek izveidota arī noklusētā pamatvienība. 

### <a name="unit-of-measure"></a>Mērvienība

Tālāk norādītie kartējumi tiek izmantoti, lai mērvienības Finance and Operations lietojumprogrammās būtu pieejamas Common Data Service.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
UNITSYMBOL | >> | msdyn_symbol
UNITCLASS | >> | msdyn_externalunitclassname
DECIMALPRECISION | >> | msdyn_decimalprecision
ISBASEUNIT | >> | msdyn_isbaseunit
ISSYSTEMUNIT | >> | msdyn_issystemunit
SYSTEMOFUNITS | >> | msdyn_systemofunits
UNITSYMBOL | >> | name
UNITDESCRIPTION | >> | msdyn_description

### <a name="unit-of-measure-conversions"></a>Mērvienību konvertēšana

Tālāk norādītie kartējumi tiek izmantoti, lai mērvienību konvertēšanu Finance and Operations lietojumprogrammās būtu pieejamas Common Data Service.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol

### <a name="product-specific-unit-of-measure-conversions"></a>Īpaša preces mērvienības konversija

Tālāk norādītie kartējumi tiek izmantoti, lai īpašā preces mērvienību konvertēšana Finance and Operations lietojumprogrammās būtu pieejamas Common Data Service.

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Preces politikas: dimensija, izsekošanas un glabāšanas grupas

Preces politikas ir politiku kopas, ko izmanto preču definēšanai un to raksturlielumus krājumos. Produktu dimensiju grupa, preču izsekošanas dimensiju grupa un noliktavas dimensiju grupa ir atrodama kā produktu politikas. 

### <a name="product-dimension-group"></a>Preces dimensijas grupa

Preču dimensiju grupa definē, kuras preces dimensijas definē preci. Ir pieejamas četras preču dimensiju grupas: izmērs, krāsa, stils un konfigurācija. Preču dimensiju grupas ir pieejamas programmā Common Data Service, izmantojot šādus kartējumus. 

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
WILLSALESPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willsalespricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willpurchasepricesearchuseproductsize
WILLSALESPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willsalespricesearchuseprodconfig
WILLSALESPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willsalespricesearchuseproductcolor
WILLPURCHASEPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willpurchasepricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willpurchpricesearchuseprodconfig
WILLPURCHASEPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willpurchpricesearchuseproductcolor
ISPRODUCTSTYLEACTIVE | >< | msdyn_isproductstyleactive
ISPRODUCTSIZEACTIVE | >< | msdyn_isproductsizeactive
ISPRODUCTCONFIGURATIONACTIVE | >< | msdyn_isproductconfigurationactive
ISPRODUCTCOLORACTIVE | >< | msdyn_isproductcoloractive
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
PRODUCTVARIANTNOMENCLATURENAME | = | msdyn_productvariantnomenclaturename
WILLSALESPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willsalespricesearchuseproductsize

### <a name="product-tracking-dimension-group"></a>Preces izsekošanas dimensiju grupa

Preču izsekošanas dimensiju grupa parāda metodi, kas tiek izmantota, lai izsekotu preci krājumos. Šie produkti ir pieejamas programmā Common Data Service, izmantojot šādus kartējumus. 

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
SERIALNUMBERCAPTURINGOPERATION | >< | msdyn_serialnumbercapturingoperation
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISSERIALNUMBERENABLEDFORPRODUCTIONCONSUMPTIONPROCESS | >< | msdyn_issnenabledforpcprocess
ISSERIALNUMBERCONTROLENABLED | >< | msdyn_isserialnumbercontrolenabled
ISSERIALNUMBERENABLEDFORSALESPROCESS | >< | msdyn_isserialnumberenabledforsalesprocess
ISSERIALNUMBERACTIVE | >< | msdyn_isserialnumberactive
ISSALESPRICEBYSERIALNUMBER | >< | msdyn_issalespricebyserialnumber
ISSALESPRICEBYBATCHNUMBER | >< | msdyn_issalespricebybatchnumber
ISPURCHASEPRICEBYSERIALNUMBER | >< | msdyn_ispurchasepricebyserialnumber
ISPURCHASEPRICEBYBATCHNUMBER | >< | msdyn_ispurchasepricebybatchnumber
ISPRIMARYSTOCKINGENABLEDFORSERIALNUMBER | >< | msdyn_isprimarystockingenabledforsn
ISPRIMARYSTOCKINGENABLEDFORBATCHNUMBER | >< | msdyn_isprimarystockingenabledforbn
ISPHYSICALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isphysicalinventoryenabledforsn
ISPHYSICALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isphysicalinventoryenabledforbn
ISFINANCIALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isfinancialinventoryenabledforsn
ISFINANCIALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isfinancialinventoryenabledforbn
ISCOVERAGEPLANENABLEDFORSERIALNUMBER | >< | msdyn_iscoverageplanenabledforserialnumber
ISCOVERAGEPLANENABLEDFORBATCHNUMBER | >< | msdyn_iscoverageplanenabledforbatchnumber
ISBLANKRECEIPTALLOWEDFORSERIALNUMBER | >< | msdyn_isblankreceiptallowedforserialnumber
ISBLANKRECEIPTALLOWEDFORBATCHNUMBER | >< | msdyn_isblankreceiptallowedforbatchnumber
ISBLANKISSUEALLOWEDFORSERIALNUMBER | >< | msdyn_isblankissueallowedforserialnumber
ISBLANKISSUEALLOWEDFORBATCHNUMBER | >< | msdyn_isblankissueallowedforbatchnumber
ISBATCHNUMBERACTIVE | >< | msdyn_isbatchnumberactive
ISINVENTORYOWNERACTIVE | >< | msdyn_isinventoryowneractive

### <a name="product-storage-dimension-group"></a>Preces noliktavas dimensiju grupa

Produktu noliktavas dimensiju grupa atbilst metodei, kas tiek izmantota, lai definētu preces novietojumu noliktavā. Šie produkti ir pieejamas programmā Common Data Service, izmantojot šādus kartējumus. 

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
WILLSALESPRICESEARCHUSEWAREHOUSE | >< | msdyn_willsalespricesearchusewarehouse
WILLSALESPRICESEARCHUSESITE | >< | msdyn_willsalespricesearchusesite
WILLSALESPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willsalespricesearchuseinventorystatus
WILLPURCHASEPRICESEARCHUSEWAREHOUSE | >< | msdyn_willpurchasepricesearchusewarehouse
WILLPURCHASEPRICESEARCHUSESITE | >< | msdyn_willpurchasepricesearchusesite
WILLPURCHASEPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willpurchpricesearchuseinventstatus
WILLCOVERAGEPLANNINGUSEWAREHOUSE | >< | msdyn_willcoverageplanusewarehouse
WILLCOVERAGEPLANNINGUSELOCATION | >< | msdyn_iscoverageplanenabledforlocation
WILLCOVERAGEPLANNINGUSEINVENTORYSTATUS | >< | msdyn_willcoverageplanuseinventorystatus
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >< | msdyn_areadvancedwmprocessesenabled
ISWAREHOUSEPRIMARYSTORAGEDIMENSION | >< | msdyn_iswarehouseprimarystoragedimension
ISWAREHOUSEMANDATORY | >< | msdyn_iswarehousemandatory
ISPHYSICALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isphysicalinventoryenabledforwarehouse
ISPHYSICALINVENTORYENABLEDFORLOCATION | >< | msdyn_isphysicalinventoryenabledforlocation
ISLOCATIONACTIVE | >< | msdyn_islocationactive
ISFINANCIALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isfinancialinventoryenabledforwarehouse
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISBLANKRECEIPTALLOWEDFORLOCATION | >< | msdyn_isblankreceiptallowedforlocation
ISBLANKISSUEALLOWEDFORLOCATION | >< | msdyn_isblankissueallowedforlocation

