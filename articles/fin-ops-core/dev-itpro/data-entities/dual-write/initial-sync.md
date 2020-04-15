---
title: Elementu atkarības ķēde (sinhronizācijas secība)
description: Šajā tēmā ir norādīta sinhronizācijas kārtība, kura ir jāievēro sākotnējo datu izveidei.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 4adb2c8d57ad8f67346b8d34212b7a4b0bd052ab
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173135"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Elementu atkarības ķēde (sinhronizācijas secība)

[!include [banner](../../includes/banner.md)]



Nākamajās astoņās tabulās entītijas ir uzskaitītas tādā secībā, kādā jums tās ir jāaktivizē. Aktivizējot karti sākotnējai sinhronizācijai, duālās rakstīšanas sistēma automātiski atpazīst citas kartes, kas ir jāaktivizē. Varat izmantot lapu **Duālā rakstīšana** programmā Finance and Operations, lai atlasītu vai atceltu entītiju atlasi sākotnējās sinhronizācijas laikā.

Jaunākajā duālajā rakstīšanas versijā var iespējot tikai dažas entītijas, un atkarības tiek apstrādātas jūsu vietā.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management entītijas

Sekojošās Supply Chain Management entītijas ir uzskaitītas tādā secībā, kādā jums tās ir jāaktivizē.

| Kartēšanas nosaukums duālajā rakstīšanas lapā | Entītijas metadatu nosaukums Supply Chain Management | Entītijas metadatu nosaukums Common Data Service | Piezīmes |
|---|---|---|---|
| Vienības ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Mērvienību pārveidošana ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Visas preces ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Preces dimensiju grupas ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Noliktavas dimensiju grupas ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Izsekošanas dimensiju grupas ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Krāsas ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Izmēri ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Stili ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Konfigurācijas ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| V2 izlaistās preces ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service izlaistās atšķirīgās preces ... preču sadaļu                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | prece                                      | |
| Preces numura identifikācijas svītrkods ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Noklusējuma pasūtījuma iestatījumi ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Preču noklusējuma pasūtījuma iestatījumi V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Precei specifisku mērvienību pārveidošana ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Vietnes ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Noliktavas ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Skatīt [1. piezīmi](#scm-notes). |
| Preces šablona krāsas ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Preces šablona izmēri ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Preces šablona stili ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Preces šablona konfigurācijas ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Preču kategorijas ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Skatīt [2. piezīmi](#scm-notes). |
| Preču kategoriju piešķires ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Preču kategoriju hierarhijas ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Preču kategoriju hierarhijas lomas ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Krājumu aile ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Noliktavas zonas ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Noliktavas zonu grupas ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Noliktavas atrašanās vietas... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Skatīt [3. piezīmi](#scm-notes). |
| Noliktavas darbu virsraksti... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Noliktavas darba rindas... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Skatīt [4. piezīmi](#scm-notes). |
| Piegādes veidi ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Saņemšanas nosacījumi ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Pārdošanas pasūtījuma izcelsmes kodi ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service pārdošanas pasūtījumu virsraksti ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Common Data Service pārdošanas pasūtījuma rindas ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Common Data Service pārdošanas piedāvājuma virsraksts ... piedāvājumi                               | SalesQuotationHeaderCommon Data ServiceEntity          | piedāvāt.                                        | |
| Common Data Service pārdošanas piedāvājuma rindas ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Pārdošanas rēķinu galvenes V2 ... rēķini                                               | SalesInvoiceHeaderV2Entity                             | rēķins                                      | |
| Pārdošanas rēķinu rindas V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Īpašas kartēšanas piezīmes

1. Pašatkarības dēļ sākotnējā sinhronizācija jums var būt jāveic divas reizes.
2. Pēc noklusējuma sākotnējā sinhronizācija ir izslēgta vecāku un atvašu attiecību dēļ (platforma neveic “smart” pasūtīšanu). Tāpēc esošās preču kategorijas ir jāsinhronizē manuāli (piemēram, atjauninot kategorijas aprakstu) pareizā secībā (vispirms pamata kategorija, pēc tam atvases un pēc tam atvašu atvases). Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana  \> Kategorijas un atribūti  \> Kategoriju hierarhijas**. Lapā **Kategoriju hierarhija** varat atlasīt katru hierarhiju un aplūkot preču kategorijas tajā.
3. Tukšo **ItemNumberInLocation** uzmeklēšanas lauku un pirmās, otrās un trešās papildu noliktavas zonu kartēšana izraisīs sākotnējās sinhronizācijas kļūmi. Tāpēc šie kartējumi pagaidām tiek noņemti.
4. Tukšā **CaptureWeight** lauka kartēšana izraisīs sākotnējās sinhronizācijas kļūmi. Tāpēc šis kartējums pagaidām tiek noņemts.

### <a name="setup-related-information"></a>Ar iestatīšanu saistītā informācija

+ Kad ieraksti pirmo reizi tiek veidoti entītijā **Preces** ar modeli vadītās programmās Dynamics 365, tiem ir **Melnraksta** statuss. Lai mainītu statusu uz **Aktīvs**, dodieties uz **Iestatījumi \>Administrēšana \>Sistēmas iestatījumi \>Pārdošana** ar modeli vadītā programmā un iestatiet opciju **Izveidot preces aktīvā stāvoklī** uz **Jā**.
+ Ja jūs izveidojat ierakstus entītijā **Preces** ar modeli vadītās programmās Dynamics 365 vai Common Data Service pirms duālās rakstīšanas iespējošanas, šie ieraksti tiks atjaunināti tikai tad, ja visa atslēga, ieskaitot **Uzņēmums**, atbilst datiem Finance and Operations programmā.
+ **Preču** entītijas sinhronizācija ir vienvirziena no Finance and Operations programmām uz Common Data Service. Ja kartēšanas lauks **Preču** entītijā, kas ir ar modeli vadītās programmās Dynamics 365, tiek atjaunināts, atjaunināšana tiks pārrakstīta nākamās sinhronizācijas laikā no Finance and Operations programmas.

### <a name="known-issues"></a>Zināmās problēmas

- Kļūda rodas, ja vienība tiek dzēsta programmā Finance and Operations. Kad mērvienības tiek sinhronizētas no Finance and Operations programmas uz Common Data Service, pirmā konkrētās klases vienība tiks izveidota kā primārā vienība un novērsīs dzēšanu.

    **Mazināšana:** vispirms izdzēsiet vienību Common Data Service. Pēc tam to var dzēst Finance and Operations programmā.

- Kļūda rodas, ja darbības vietne tiek dzēsta programmā Common Data Service. Kļūdas ziņojums norāda: "Informācijas žurnāls - Brīdinājums: primāro adresi nevar dzēst; Brīdinājums: entītijas ierakstu nevarēja dzēst, jo neizdevās šāds datu avots: InventSiteLogisticsLocation (InventSiteLogisticsLocation)." Šo kļūdu rada problēma, kas saistīta ar datu entītiju Finance and Operations programmā.

    **Mazināšana:** varat dzēst vietni programmā Finance and Operations. Pēc tam vietne tiks dzēsta Common Data Service, ja tiek palaista atbilstošā duālā ieraksta karte.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance entītijas

Sekojošās entītijas Dynamics 365 Finance ir uzskaitītas tādā secībā, kādā jums tās ir jāaktivizē.

| Kartēšanas nosaukums duālajā rakstīšanas lapā | Entītijas metadatu nosaukums programmā Finance | Entītijas metadatu nosaukums Common Data Service | Piezīmes |
|---|---|---|---|
| Valūtas ... transactioncurrencies                                            | CurrencyEntity                              | Valūta                                   | |
| Maiņas kursa tips ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Maiņas kursa valūtu pāris ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service maiņas kursi ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Skatīt [1. piezīmi](#fin-notes). |
| Finanšu kalendāra integrācijas entītija ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Finanšu kalendāra gada integrācijas entītija ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Finanšu kalendāra periods ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Organizācijas hierarhijas tipi ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Skatīt [1. piezīmi](#fin-notes). |
| Organizācijas hierarhijas nolūki ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Skatīt [1. piezīmi](#fin-notes). |
| Juridiskas personas ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Skatīt [1. piezīmi](#fin-notes). |
| Juridiskās personas ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Pārvaldības struktūrvienība ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Skatīt [1. piezīmi](#fin-notes). |
| Organizācijas hierarhija — publicēta ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Skatīt [1. piezīmi](#fin-notes). |
| Nosaukuma afiksi ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Maksāšanas dienas Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Maksāšanas dienu rindas Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Maksājumu grafiks ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Maksājumu grafika rindas ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Apmaksas nosacījumi ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Debitora maksāšanas metode ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Kreditora maksājuma metode ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Debitoru grupas ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Kreditoru grupas ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| PVN grupas ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Krājumu PVN grupas ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| PVN virsgrāmatas grāmatošanas grupas V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| PVN reģistrācijas koda entītijas Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| PVN iestādes ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| PVN kods ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Skatīt [1. piezīmi](#fin-notes). |
| Finanšu dimensijas formāts ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Finanšu dimensijas ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Ieturēto nodokļu grupas ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Ieturēto nodokļu kodi ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Kontu plāns ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Virsgrāmata ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Skatīt [1. piezīmi](#fin-notes). |
| Galvenā konta kategorijas ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Galvenais konts ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Debitori V3 ... kontiem                                                       | CustCustomerV3Entity                        | konts                                    | Skatīt [2. piezīmi](#fin-notes). |
| Debitori V3 ... kontaktpersonām                                                       | CustCustomerV3Entity                        | kontaktēties                                    | Skatīt [3. piezīmi](#fin-notes). |
| Kreditori V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Skatīt [2. piezīmi](#fin-notes). |
| Common Data Service kontaktpersonas V2 ... kontaktpersonām                                    | smmContactPersonCommon Data ServiceV2Entity | kontaktēties                                    | Skatīt [4. piezīmi](#fin-notes). |
| Common Data Service kontaktpersonas V2 ... kontaktpersonām                                    | smmContactPersonCommon Data ServiceV2Entity | kontaktēties                                    | Skatīt [5. piezīmi](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Īpašas kartēšanas piezīmes

1. Tiek veikta vienvirziena sinhronizācija no Finance and Operations programmām uz Common Data Service.
2. Pašatkarības dēļ sākotnējā sinhronizācija jums var būt jāveic vairāk kā vienu reizi. Kad veidojat kontu, noteikti atlasiet **Klients** kā relācijas tipu, izmantojot lapu **Konti** programmā Common Data Service. Ja sākotnējās sinhronizācijas laikā rodas problēmas ar **Primāro kontaktpersonu**  lauku, izņemiet šo lauku no kartējuma un pēc tam vēlreiz palaidiet sākotnējo sinhronizāciju. Pēc tam, kad sākotnējā sinhronizācija ir sekmīgi pabeigta, apturiet kartēšanu un vēlreiz pievienojiet **Primāro kontaktpersonu** lauku. Pēc tam sāciet kartēšanu, bet izlaidiet sākotnējo sinhronizāciju. **Primārās kontaktpersonas** lauka vērtība netiks iekļauta sākotnējā sinhronizācijā, un jums ir manuāli jāmigrē vērtības.
3. Pārliecinieties, ka opcija **Pārdodams** ir iestatīta uz **Jā** lapā **Kontakti** programmā Common Data Service, kad mēģināt izveidot **Personas** tipa klientu.
4. Šai kartēšanai ir filtrs abās pusēs, lai saistītu klienta kontaktpersonas. Atveriet kartēšanas datus, atlasiet filtra pogu (piltuves simbols) blakus **Sales.Contact** entītijas nosaukumam un pārliecinieties, ka faila kritēriji satur **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Šai kartēšanai ir filtrs abās pusēs, lai saistītu kreditora kontaktpersonas. Atveriet kartēšanas datus, atlasiet filtra pogu (piltuves simbols) blakus **Sales.Contact** entītijas nosaukumam un pārliecinieties, ka filtra kritēriji satur **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources entītijas

Sekojošās entītijas Dynamics 365 Human Resources ir uzskaitītas tādā secībā, kādā jums tās ir jāaktivizē.

| Kartēšanas nosaukums duālajā rakstīšanas lapā | Entītijas metadatu nosaukums programmā Human Resources | Entītijas metadatu nosaukums Common Data Service | Piezīmes |
|---|---|---|---|
| cdm_jobfunction – Darba funkcija                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes- Darba tipi                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs — Darbi                                               |                                   | cdm_jobs                         | |
| cdm_jobs — Detalizēta informācija par darbu                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Pamata amats                              | HcmPositionBaseEntity             | cdm_jobposition                  | Skatīt [1. piezīmi](#hr-notes). |
| cdm_jobposition - Detalizēta informācija par amatu                            | HcmPositionDetailEntity           | cdm_jobposition                  | Skatīt [1. piezīmi](#hr-notes). |
| cdm_jobposition - Amata ilgums                           | HcmPositionDurationEntity         | cdm_jobposition                  | Skatīt [1. piezīmi](#hr-notes). |
| cdm_jobposition - Amata hierarhijas                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Skatīt [1. piezīmi](#hr-notes). |
| cdm_veteranstatus - Veterāna statuss                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin — Etniskā izcelsme                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - Valodas kods                              |                                   | cdm_languagecode                 | |
| cdm_worker — Darbinieks                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - Nodarbinātība                                 |                                   | cdm_employments                  | |
| cdm_employments - Detalizēta informācija par nodarbinātību                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Amatā nodarbināto piešķire | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Skatīt [2. piezīmi](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Īpašas kartēšanas piezīmes

1. Viena Common Data Service entītija ir kartēta ar vairākām Finance and Operations programmas entītijām.
2. Šai kartēšanai ir pašatsauce.

## <a name="asset-management-entities"></a>Līdzekļu pārvaldības entītijas

Sekojošās Līdzekļu pārvaldības entītijas, kas paredzētas Dynamics 365 Supply Chain Management, ir uzskaitītas tādā secībā, kādā jums tās ir jāaktivizē.

| Kartēšanas nosaukums duālajā rakstīšanas lapā | Entītijas metadatu nosaukums Līdzekļu pārvaldībā | Entītijas metadatu nosaukums Common Data Service | Piezīmes |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Līdzekļu pārvaldība līdzeklis dzīves cikla stāvokļi               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Līdzekļu pārvaldība līdzeklis dzīves cikla modeļi               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Līdzekļu pārvaldība funkcionālie novietojumi dzīves cikla modeļi | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Līdzekļu pārvaldība funkcionālais novietojums dzīves cikla stāvokļi | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Līdzekļu pārvaldība līdzekļu veidi                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Līdzekļu pārvaldība funkcionālie novietojumu veidi            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Līdzekļu pārvaldība funkcionālie novietojumi                 | msdyn_functionallocations                | Skatiet [piezīmi](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Līdzekļu pārvaldības līdzekļi                               | msdyn_customerassets                     | Skatiet [piezīmi](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Līdzekļu pārvaldība ražotāji                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Līdzekļu pārvaldības modeļi                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Līdzekļu pārvaldības garantija                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Īpašas kartēšanas piezīmes

- Pašatkarības dēļ sākotnējā sinhronizācija jums var būt jāveic vairāk kā vienu reizi.
