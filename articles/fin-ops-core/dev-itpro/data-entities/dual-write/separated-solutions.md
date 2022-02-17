---
title: Atsevišķa Dual-Write Application Orchestration pakotne
description: Dual-Write Application Orchestration pakotne vairs nav viena pakotne, bet ir sadalīta mazākās pakotnēs. Šajā tēmā ir izskaidroti katras pakotnes risinājumi un kartes, kā arī to atkarība no citām pakotnēm.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: e2f870368dc662032a3e7ca7ddca902feb23a713
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063266"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Atsevišķa Dual-Write Application Orchestration pakotne

[!include [banner](../../includes/banner.md)]



Iepriekš Dual-Write Application Orchestration pakotne bija viena pakotne, kurā bija šādi risinājumi:

- Dynamics 365 piezīmes
- Dynamics 365 Finance un Operations Common Enchor
- Dynamics 365 Finance un operācijas Dual Write entītiju kartes
- Programma Dynamics 365 Asset Management
- Dynamics 365 Asset Management
- Kopējais HCM
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance un Operations Common
- Uzņēmums Dynamics 365
- Valūtas maiņas kursi
- Field Service Common

Tā kā tā bija viena pakete, šī pakete radīja klientiem situāciju "visu vai neko". Tomēr Microsoft tagad to ir sadalījis mazākās paketēs. Līdz ar to klients var izvēlēties tieši viņam nepieciešamo risinājumu komplektus. Piemēram, ja esat Microsoft Dynamics 365 Supply Chain Management klientam, un nav nepieciešama integrācija ar Dynamics 365 Human Resources, piezīmes un līdzekļu pārvaldību, varat izslēgt šos risinājumus no instalētajiem risinājumiem. Tā kā pamatā esošo risinājumu nosaukumi, izdevējs un kartes versijas paliek nemainīgas, šīs izmaiņas ir nemainīgas. Esošās instalācijas tiks atjauninātas.

![Atsevišķs iepakojums.](media/separated-package-1.png)

Šajā tēmā ir izskaidroti katras pakotnes risinājumi un kartes, kā arī to atkarība no citām pakotnēm.

## <a name="dual-write-application-core"></a>Divkāršās rakstīšanas lietojumprogrammas kodols

Dual-write Application Core pakotne ļauj lietotājiem instalēt un konfigurēt duālo rakstīšanu bez klientu iesaistīšanas lietotnes. Tas satur šādus piecus risinājumus.

| Unikāls nosaukums                           | Rādīt nosaukumu                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Uzņēmums Dynamics 365                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance un Operations Common |
| CurrencyExchangeRates                 | Valūtas maiņas kursi                    |
| msdyn_DualWriteAppCoreMaps            | Divkāršās rakstīšanas lietojumprogrammu pamata entītiju kartes   |
| msdyn_DualWriteAppCoreAnchor          | Divkāršās rakstīšanas lietojumprogrammu kodola enkurs        |

Šajā iepakojumā ir pieejamas šādas kartes.

| Finance and Operations programmas     | Customer engagement programmas                    |
|---------------------------------|---------------------------------------------|
| Pārvaldības struktūrvienība                  | msdyn_internalorganizations                 |
| Organizācijas hierarhija          | msdyn_internalorganizationhierarchies       |
| Juridiskas personas                  | msdyn_internalorganizations                 |
| Juridiskas personas                  | cdm_companies                               |
| Organizācijas hierarhijas nolūki | msdyn_internalorganizationhierarchypurposes |
| Maiņas kursa valūtu pāris     | msdyn_currencyexchangeratepairs             |
| Nosaukuma afiksi                    | msdyn_nameaffixes                           |
| Maiņas kursa veids              | msdyn_exchangeratetypes                     |
| CDS maiņas kursi              | msdyn_currencyexchangerates                 |
| Organizācijas hierarhijas tips     | msdyn_internalorganizationhierarchytypes    |
| Valūtas                      | transactioncurrencies                       |
| Jauktās realitātes ceļvežu entītija     | msmrw_guides                                |

**Informācija par atkarību**

Dual-write Application Core pakotne nav atkarīga no citām pakotnēm.

## <a name="dual-write-human-resources"></a>Divkāršās rakstīšanas cilvēkresursi

Divkāršās rakstīšanas cilvēkresursu pakotne satur risinājumus un kartes, kas nepieciešami cilvēkresursu datu sinhronizēšanai. Tajā ir šādi trīs risinājumi.

| Unikāls nosaukums                | Rādīt nosaukumu                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | Kopējais HCM                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources entītiju kartes |
| msdyn_Dynamics365HCMAchor | Dynamics 365 Human Resources enkurs      |

Šajā iepakojumā ir pieejamas šādas kartes.

| Finance and Operations programmas | Customer engagement programmas         |
|-----------------------------|----------------------------------|
| Etniskās izcelsmes              | cdm_ethnicorigins                |
| Atlīdzības darbu funkcija   | cdm_jobfunctions                 |
| Pozīcijas V2                | cdm_jobpositions                 |
| Darbi                        | cdm_jobs                         |
| Atlīdzības darba tips       | cdm_jobtypes                     |
| Valodu kodi              | cdm_languages                    |
| Amata tips               | cdm_positiontypes                |
| Pozīcijas nodarbinātā uzdevumi | cdm_positionworkerassignmentmaps |
| Veterāna statuss              | cdm_veteranstatus              |
| Darbinieks                      | cdm_workers                      |
| Nodarbinātība pēc uzņēmuma      | cdm_employments                  |

**Informācija par atkarību**

Divkāršās rakstīšanas cilvēkresursu pakotne ir atkarīga no Dual-Write Application Core pakotnes. Tāpēc pirms divkāršās rakstīšanas cilvēkresursu pakotnes instalēšanas ir jāinstalē Dual-write Application Core pakotne.

## <a name="dual-write-supply-chain"></a>Divkāršās rakstīšanas piegādes ķēde

Divkāršās rakstīšanas piegādes ķēdes pakotne satur risinājumus un kartes, kas nepieciešami piegādes ķēdes pārvaldības datu sinhronizēšanai. Tajā ir šādi trīs risinājumi.

| Unikāls nosaukums                                | Rādīt nosaukumu                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management paplašinātās entītiju kartes |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management pagarināts enkurs      |

Šajā iepakojumā ir pieejamas šādas kartes.

| Finance and Operations programmas                 | Customer engagement programmas                      |
|---------------------------------------------|-----------------------------------------------|
| Vienības                                       | uoms                                          |
| CDS pārdošanas pasūtījumu virsraksti                     | salesorders                                   |
| CDS pārdošanas pasūtījumu rindas                       | salesorderdetails                             |
| CDS pārdošanas piedāvājuma virsraksts                  | piedāvājumi                                        |
| CDS pārdošanas piedāvājuma rindas                   | quotedetails                                  |
| CDS izlaistās atšķirīgās preces              | produkti                                      |
| Noliktavas zonas                             | msdyn_warehousezones                          |
| Noliktavas zonu grupas                       | msdyn_warehousezonegroups                     |
| Noliktavas darba rindas                        | msdyn_warehouseworklines                      |
| Noliktavas darba galvenes                      | msdyn_warehouseworkheaders                    |
| Noliktavas                                  | msdyn_warehouses                              |
| Krājumu aile                             | msdyn_warehouseaisles                         |
| Mērvienību pārveidošana                            | msdyn_unitofmeasureconversions                |
| Piegādes nosacījumi                           | msdyn_termsofdeliveries                       |
| Piegādes veidi                           | msdyn_shipvias                                |
| Preces šablona stili                       | msdyn_sharedproductstyles                     |
| Pārdošanas rēķinu rindas V2                      | invoicedetails                                |
| Pārdošanas rēķinu galvenes V2                    | rēķini                                      |
| Preces šablona izmēri                        | msdyn_sharedproductsizes                      |
| Izlaistās preces V2                        | msdyn_sharedproductdetails                    |
| Preces šablona konfigurācijas               | msdyn_sharedproductconfigurations             |
| Preces šablona krāsas                       | msdyn_sharedproductcolors                     |
| Pārdošanas pasūtījumu izcelsmes kodi                    | msdyn_salesorderorigins                       |
| Preces saņemšanas galvene                      | msdyn_purchaseorderreceipts                   |
| Preces saņemšanas rinda                        | msdyn_purchaseorderreceiptproducts            |
| Pirkšanas pasūtījumu virsraksti V2                   | msdyn_purchaseorders                          |
| CDS pirkšanas pasūtījuma rindas nepilni izdzēstais elements | msdyn_purchaseorderproducts                   |
| CDS pirkšanas pasūtījuma rindas elements              | msdyn_purchaseorderproducts                   |
| Izsekošanas dimensiju grupas                   | msdyn_producttrackingdimensiongroups          |
| Stili                                      | msdyn_productstyles                           |
| Noliktavas dimensiju grupas                    | msdyn_productstoragedimensiongroups           |
| Precei specifisku mērvienību pārveidošana           | msdyn_productspecificunitofmeasureconversions |
| Preču noklusējuma pasūtījuma iestatījumi V2           | msdyn_productspecificdefaultordersettings     |
| Izmēri                                       | msdyn_productsizes                            |
| Preces dimensiju grupas                    | msdyn_productdimensiongroups                  |
| Pasūtījuma noklusējuma iestatījumi                      | msdyn_productdefaultordersettings             |
| Konfigurācijas                              | msdyn_productconfigurations                   |
| Visas preces                                | msdyn_globalproducts                          |
| Krāsas                                      | msdyn_productcolors                           |
| Preču kategoriju hierarhijas lomas            | msdyn_productcategoryhierarchyroles           |
| Preču kategoriju hierarhijas                | msdyn_productcategoryhierarchies              |
| Preču kategoriju piešķires                | msdyn_productcategoryassignments              |
| Preces kategorijas                          | msdyn_productcategories                       |
| Noliktavas novietojumi                         | msdyn_inventorylocations                      |
| CDS inventārs ieslēgts                            | msdyn_inventoryonhandentries                  |
| Preces kategorijas                          | msdyn_productcategories                       |
| CDS inventārs ieslēgts                            | msdyn_inventoryonhandrequests                 |
| Produkta numura identifikācijas svītrkods           | msdyn_product svītrkodi                         |
| Lojalitātes programmas karte                                | msdyn_loyaltycards                            |
| Lojalitātes programmas atlīdzības punkti                       | msdyn_loyaltyrewardpoints                     |
| Cenu debitoru grupas                       | msdyn_pricecustomergroups                     |
| Vietnes                                       | msdyn_operationalsites                        |
| CDS pārdošanas piedāvājuma rindas                   | quotedetails                                  |
| CDS pārdošanas pasūtījumu rindas                       | salesorderdetails                             |

**Informācija par atkarību**

Dual-Write Supply Chain pakotne ir atkarīga no tālāk norādītajām trim pakotnēm. Tādēļ šīs pakotnes ir jāinstalē, pirms instalējat divkāršās rakstīšanas piegādes ķēdes pakotni.

- Dual-Write Application Core pakotne
- Divkāršās rakstīšanas finanšu pakete
- Divkāršās rakstīšanas cilvēkresursu pakotne

## <a name="dual-write-finance"></a>Divkāršās rakstīšanas finanses

Dual-write Finance pakotnē ir sinhronizēšanai nepieciešamie risinājumi un kartes Dynamics 365 Finance datus. Tajā ir šādi četri risinājumi.

| Unikāls nosaukums                            | Rādīt nosaukumu                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance paplašinātās entītiju kartes |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance pagarināts enkurs      |

Šajā iepakojumā ir pieejamas šādas kartes.

| Finance and Operations programmas             | Customer engagement programmas        |
|-----------------------------------------|---------------------------------|
| Ieturamo nodokļu grupas                  | msdyn_withholdingtaxgroups      |
| CDS Contacts V2 (klients)              | kontaktpersonas                        |
| CDS kontaktpersonas V2 (piegādātājs)                | kontaktpersonas                        |
| Debitori V3                            | kontaktpersonas                        |
| Ieturamo nodokļu kodi                   | msdyn_withholdingtaxcodes       |
| Kreditori V2                              | msdyn_vendors                   |
| Piegādātāja maksāšanas metode                   | msdyn_vendorpaymentmethods      |
| Kreditoru grupas                           | msdyn_vendorgroups              |
| Kontu plāns                       | msdyn_chartofaccountses         |
| PVN virsgrāmatas grāmatošanas grupas V2      | msdyn_taxpostinggroups          |
| Krājumu PVN grupa                    | msdyn_taxitemgroups             |
| PVN grupas                        | msdyn_taxgroups                 |
| PVN reģistrācijas koda elements CDS        | msdyn_taxexemptcodes            |
| Debitoru grupas                         | msdyn_customergroups            |
| Debitora maksāšanas metode                 | msdyn_customerpaymentmethods    |
| Finanšu dimensijas                    | msdyn_dimensionattributes       |
| Nodokļu iestādes                   | msdyn_taxauthorities            |
| Finanšu dimensijas formāts              | msdyn_financialdimensionformats |
| Finanšu kalendāra periods                  | msdyn_fiscalcalendarperiods     |
| Elements Finanšu kalendāra integrācija      | msdyn_fiscalcalendars           |
| Elements Finanšu kalendāra gada integrācija | msdyn_fiscalcalendaryears       |
| Apmaksas nosacījumi                        | msdyn_paymentterms              |
| Maksājumu grafiks                        | msdyn_paymentschedules          |
| Maksājumu grafika rindas                  | msdyn_paymentschedulelines      |
| Maksāšanas dienas CDS                        | msdyn_paymentdays               |
| Maksāšanas dienu rindas CDS V2                | msdyn_paymentdaylines           |
| Galvenais konts                            | msdyn_mainaccounts              |
| Galvenā konta kategorijas                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Debitori V3                            | konti                        |

**Informācija par atkarību**

Dual-write Finance pakotne ir atkarīga no Dual-write Application Core pakotnes. Tāpēc pirms Dual-write Finance pakotnes instalēšanas jāinstalē Dual-write Application Core pakotne.

## <a name="dual-write-notes"></a>Divkāršās rakstīšanas piezīmes

Divkāršās rakstīšanas piezīmju pakotne satur risinājumus un kartes, kas nepieciešami piezīmju vai anotāciju datu sinhronizēšanai. Tajā ir šādi četri risinājumi.

| Unikāls nosaukums                  | Rādīt nosaukumu                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 piezīmes             |
| Dynamics365NotesExtended     | Dynamics 365 piezīmes pagarinātas    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 piezīmju entītiju kartes |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 piezīmju enkurs      |

Šajā iepakojumā ir pieejamas šādas kartes.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Pārdošanas pasūtījuma galvenes dokumenta pielikumi    | anotācijas         |
| Debitora pielikumi                       | anotācijas         |
| Kreditora dokumentu pielikumi                | anotācijas         |
| Pirkšanas pasūtījuma galvenes dokumenta pielikumi | anotācijas         |

**Informācija par atkarību**

Dual-write Notes pakotne ir atkarīga no tālāk norādītajām divām pakotnēm. Tādēļ šīs pakotnes ir jāinstalē pirms Dual-write Notes pakotnes instalēšanas.

- Dual-Write Application Core pakotne
- Divkāršās rakstīšanas finanšu pakete

## <a name="dual-write-asset-management"></a>Divkāršās rakstīšanas līdzekļu pārvaldība

Divkāršās rakstīšanas līdzekļu pārvaldības pakotnē ir iekļauti risinājumi un kartes, kas nepieciešami, lai sinhronizētu līdzekļu datus no piegādes ķēdes pārvaldības vai Dynamics 365 Field Service. Tajā ir šādi četri risinājumi.

| Unikāls nosaukums                          | Rādīt nosaukumu                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 Asset Management             |
| Dynamics365AssetManagementApp        | Programma Dynamics365 Asset Management          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 Asset Management entītiju kartes |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 Asset Management enkurs      |

Šajā iepakojumā ir pieejamas šādas kartes.

| Finance and Operations programmas                           | Customer engagement programmas                |
|-------------------------------------------------------|-----------------------------------------|
| Līdzekļu pārvaldības garantija                             | msdyn_warranties                        |
| Līdzekļu pārvaldības modeļi                               | msdyn_models                            |
| Līdzekļu pārvaldība ražotāji                        | msdyn_manufacturers                     |
| Līdzekļu pārvaldība funkcionālie novietojumu veidi            | msdyn_functionallocationtypes           |
| Līdzekļu pārvaldība funkcionālie novietojumi                 | msdyn_functionallocations               |
| Līdzekļu pārvaldība funkcionālais novietojums dzīves cikla stāvokļi | msdyn_functionallocationlifecyclestates |
| Līdzekļu pārvaldība funkcionālie novietojumi dzīves cikla modeļi | msdyn_functionallocationlifecyclemodels |
| Līdzekļu pārvaldības līdzekļi                               | msdyn_customerassets                    |
| Līdzekļu pārvaldība līdzekļu veidi                          | msdyn_customerassetcategories           |
| Līdzekļu pārvaldība līdzeklis dzīves cikla stāvokļi               | msdyn_assetlifecyclestates              |
| Līdzekļu pārvaldība līdzeklis dzīves cikla modeļi               | msdyn_assetlifecyclemodels              |

**Informācija par atkarību**

Divkāršās rakstīšanas līdzekļu pārvaldības pakotne ir atkarīga no Dual-Write Application Core pakotnes. Tāpēc pirms divkāršās rakstīšanas līdzekļu pārvaldības pakotnes instalēšanas jāinstalē Dual-Write Application Core pakotne.

## <a name="packages-required-for-project-operations"></a>Projekta darbībām nepieciešamās paketes
Projekta darbības ir atkarīgas no tālāk norādītajām pakotnēm. Tādēļ šīs pakotnes jāinstalē pirms Project Operations instalēšanas.

- Dual-Write Application Core pakotne
- Divkāršās rakstīšanas finanšu pakete
- Divkāršās rakstīšanas piegādes ķēdes iepakojums
- Divkāršās rakstīšanas līdzekļu pārvaldības pakotne
- Divkāršās rakstīšanas cilvēkresursu pakotne
