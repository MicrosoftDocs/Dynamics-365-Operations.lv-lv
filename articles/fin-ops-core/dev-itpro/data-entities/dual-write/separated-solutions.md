---
title: Atdalīta dubultās rakstīšanas programmas instrumentācijas pakotne
description: Dubultās rakstīšanas programmas instrumentācijas pakotne vairs nav viena pakotne, bet ir sadalīta mazākās pakotnēs. Šajā rakstā ir skaidroti risinājumi un kartes, kas satur katru pakotni, un tās atkarība no citām pakotnēm.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 28c321ee2815b2886c07bfb0996870e536458145
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111666"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Atdalīta dubultās rakstīšanas programmas instrumentācijas pakotne

[!include [banner](../../includes/banner.md)]



Iepriekš dubultās rakstīšanas programmas instrumentācijas pakotne bija viena pakotne, kurā bija šādi risinājumi:

- Dynamics 365 piezīmes
- Dynamics 365 finanšu un operāciju kopējais enkurss
- Dynamics 365 finanšu un operāciju dubultās rakstīšanas elementu kartes
- Dynamics 365 līdzekļu pārvaldības programma
- Dynamics 365 līdzekļu pārvaldība
- Kopējais HCM
- Dynamics 365 piegādes ķēde paplašināta
- Dynamics 365 Finance Extended
- Dynamics 365 finanses un operācijas Kopējās
- Dynamics 365 uzņēmums
- Valūtas maiņas kursi
- Lauku pakalpojuma kopīgais

Tā kā tā bija viena pakotne, šī pakotne debitoriem izveidoja situāciju "visi vai nekas". Tomēr korporācija Microsoft tagad ir nodalījusi to mazākās pakotnēs. Tādēļ debitori var atlasīt tikai tiem nepieciešamajiem risinājumiem iepakojumus. Piemēram, ja esat Microsoft Dynamics 365 Supply Chain Management Dynamics 365 Human Resources klients un nav nepieciešama integrācija ar, piezīmēm un līdzekļu pārvaldību, varat izslēgt šos risinājumus no instalētajiem risinājumiem. Tā kā pamatā esošie risinājumu nosaukumi, izdevējs un kartes versijas paliek nemainīgas, šīs izmaiņas netiek pārkāptas. Esošajām instalācijām jābūt jauninātām.

![Atdalīts iepakojums.](media/separated-package-1.png)

Šajā rakstā ir skaidroti risinājumi un kartes, kas satur katru pakotni, un tās atkarība no citām pakotnēm.

## <a name="dual-write-application-core"></a>Dubultās rakstīšanas programmas kodols

Dubultās rakstīšanas programmas pamata pakotne ļauj lietotājiem instalēt un konfigurēt dubulto rakstiet bez jebkādas debitora piesaistes programmas. Tajā ir šādi pieci risinājumi.

| Unikāls nosaukums                           | Parādāmais nosaukums                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 uzņēmums                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finanšu un operāciju kopējā versija |
| CurrencyExchangeRates                 | Valūtas maiņas kursi                    |
| msdyn_DualWriteAppCoreMaps            | Dubultās rakstīšanas programmu pamatelementa kartes   |
| msdyn_DualWriteAppCoreAnchor          | Duālās rakstīšanas programmu pamatenkurss        |

Šajā pakotnē ir pieejamas šādas kartes.

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

Dubultās rakstīšanas programmas pamata pakotnei nav atkarības no citiem iepakojumiem.

## <a name="dual-write-human-resources"></a>Dubultās rakstīšanas cilvēkresursi

Duālā ierakstā cilvēkresursu pakotnē ir ietverti risinājumi un kartes, kas ir nepieciešamas personāla vadības datu sinhronizēšanai. Tajā ir trīs turpmākie risinājumi.

| Unikāls nosaukums                | Parādāmais nosaukums                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | Kopējais HCM                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources elementu kartes |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources enkurs      |

Šajā pakotnē ir pieejamas šādas kartes.

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
| Veterāna statuss              | cdm_veteranstatuses              |
| Darbinieks                      | cdm_workers                      |
| Nodarbinātība pēc uzņēmuma      | cdm_employments                  |

**Informācija par atkarību**

Duālās rakstīšanas personāla vadības iepakojums ir atkarīgs no duālās rakstīšanas programmas pamata iepakojuma. Tāpēc jums jāinstalē Dubultās rakstīšanas programmas kodola pakotne, pirms instalējat Divdiponentu cilvēkresursu pakotni.

## <a name="dual-write-supply-chain"></a>Dubultās rakstīšanas piegādes ķēde

Dubultās rakstīšanas piegādes ķēdes pakotnē ir ietverti risinājumi un kartes, kas ir nepieciešamas Piegādes ķēdes pārvaldības datu sinhronizēšanai. Tajā ir trīs turpmākie risinājumi.

| Unikāls nosaukums                                | Parādāmais nosaukums                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 piegādes ķēde paplašināta                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management paplašināto elementu kartes |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management paplašināts enkurss      |

Šajā pakotnē ir pieejamas šādas kartes.

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
| CDS krājumi                            | msdyn_inventoryonhandentries                  |
| Preces kategorijas                          | msdyn_productcategories                       |
| CDS krājumi                            | msdyn_inventoryonhandrequests                 |
| Produkta numura identifikācijas svītrkods           | msdyn_productbarcodes                         |
| Lojalitātes programmas karte                                | msdyn_loyaltycards                            |
| Lojalitātes programmas atlīdzības punkti                       | msdyn_loyaltyrewardpoints                     |
| Cenu debitoru grupas                       | msdyn_pricecustomergroups                     |
| Vietnes                                       | msdyn_operationalsites                        |
| CDS pārdošanas piedāvājuma rindas                   | quotedetails                                  |
| CDS pārdošanas pasūtījumu rindas                       | salesorderdetails                             |

**Informācija par atkarību**

Dubultās rakstīšanas piegādes ķēdes iepakojums ir atkarīgs no tālāk minētajiem trim iepakojumiem. Tāpēc jums ir jāinstalē šīs pakotnes pirms duālās rakstīšanas piegādes ķēdes pakotnes instalēšanas.

- Duālās rakstīšanas programmas pamata pakotne
- Dubultās rakstīšanas finanšu pakotne
- Duālā ieraksta cilvēkresursu pakotne

## <a name="dual-write-finance"></a>Dubultās rakstīšanas finanses

Dubultās rakstīšanas finanšu pakotnē ir ietverti risinājumi un kartes, kas ir nepieciešamas Dynamics 365 finanšu datu sinhronizēšanai. Tajā ir šādi četri risinājumi.

| Unikāls nosaukums                            | Parādāmais nosaukums                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 finanšu paplašināto elementu kartes |
| FieldServiceCommon                     | Lauku pakalpojuma kopīgais                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 finanšu paplašinātais enkurss      |

Šajā pakotnē ir pieejamas šādas kartes.

| Finance and Operations programmas             | Customer engagement programmas        |
|-----------------------------------------|---------------------------------|
| Ieturēto nodokļu grupas                  | msdyn_withholdingtaxgroups      |
| CDS kontaktpersonas V2 (Debitors)              | kontaktpersonas                        |
| CDS kontaktpersonas V2 (kreditors)                | kontaktpersonas                        |
| Debitori V3                            | kontaktpersonas                        |
| Ieturēto nodokļu kodi                   | msdyn_withholdingtaxcodes       |
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
| Virsgrāmata                                  | msdyn_ledgers                   |
| Debitori V3                            | konti                        |

**Informācija par atkarību**

Dubultās rakstīšanas finanšu pakotne ir atkarīga no dubultās rakstīšanas programmas pamata pakotnes. Tāpēc jums jāinstalē Dual-write application Core pakotne pirms dubultās rakstīšanas finanšu pakotnes instalēšanas.

## <a name="dual-write-notes"></a>Duālās rakstīšanas piezīmes

Duālās rakstīšanas piezīmju pakotnē ir ietverti risinājumi un kartes, kas ir nepieciešamas piezīmju vai anotāciju datu sinhronizācijai. Tajā ir šādi četri risinājumi.

| Unikāls nosaukums                  | Parādāmais nosaukums                   |
|------------------------------|--------------------------------|
| Dynamics365notes             | Dynamics 365 piezīmes             |
| Dynamics365NotesExtended     | Paplašinātas Dynamics 365 piezīmes    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 piezīmju elementu kartes |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 piezīmju enkurss      |

Šajā pakotnē ir pieejamas šādas kartes.

| Finanses un operācijas                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Pārdošanas pasūtījuma galvenes dokumenta pielikumi    | Anotācijas         |
| Debitora pielikumi                       | Anotācijas         |
| Kreditora dokumentu pielikumi                | Anotācijas         |
| Pirkšanas pasūtījuma galvenes dokumenta pielikumi | Anotācijas         |

**Informācija par atkarību**

Duālās rakstīšanas piezīmju iepakojums ir atkarīgs no tālāk minētajiem diviem iepakojumiem. Tāpēc pirms Duālās rakstīšanas piezīmju pakotnes instalēšanas ir jāinstalē šīs pakotnes.

- Duālās rakstīšanas programmas pamata pakotne
- Dubultās rakstīšanas finanšu pakotne

## <a name="dual-write-asset-management"></a>Duālā norakstīšanas līdzekļu pārvaldība

Dubultās rakstīšanas līdzekļu pārvaldības pakotnē ir ietverti risinājumi un kartes, kas ir nepieciešamas līdzekļu datu sinhronizēšanai no Supply Chain Management vai Dynamics 365 Field Service. Tajā ir šādi četri risinājumi.

| Unikāls nosaukums                          | Parādāmais nosaukums                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 līdzekļu pārvaldība             |
| Dynamics365AssetManagementApp        | Dynamics365 līdzekļu pārvaldības programma          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 Līdzekļu pārvaldības elementu kartes |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 līdzekļu pārvaldības enkurss      |

Šajā pakotnē ir pieejamas šādas kartes.

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

Duālās rakstīšanas līdzekļu pārvaldības pakotne ir atkarīga no duālās rakstīšanas programmas pamata iepakojuma. Tāpēc jums jāinstalē Dubultās rakstīšanas programmas kodola pakotne pirms duālās rakstīšanas aktīvu pārvaldības pakotnes instalēšanas.

## <a name="packages-required-for-project-operations"></a>Projekta operācijām nepieciešamās pakotnes
Projekta operācijas ir atkarīgas no tālāk minētajiem iepakojumiem. Tādēļ jums ir jāinstalē šīs pakotnes pirms projekta operāciju instalēšanas.

- Duālās rakstīšanas programmas pamata pakotne
- Dubultās rakstīšanas finanšu pakotne
- Duālās rakstīšanas piegādes ķēdes iepakojums
- Duālās rakstīšanas līdzekļu pārvaldības pakotne
- Duālā ieraksta cilvēkresursu pakotne

## <a name="dual-write-party-and-global-address-book-solutions"></a>Duālās rakstīšanas puses un globālās adrešu grāmatas risinājumi

Dubultās rakstīšanas puses un globālās adrešu grāmatas pakotnē ir iekļauti šādi risinājumi un kartes, kas ir nepieciešamas, lai sinhronizētu pušu un globālās adrešu grāmatas datus. 

| Unikāls nosaukums                       | Parādāmais nosaukums                            |
|-----------------------------------|-----------------------------------------|
| Puse                             | Puse                                   |
| Dynamics365GABExtended            | Dynamics 365 GAB paplašinātā               |
| Dynamics365GABDualWriteEntityMaps | Dynamics 365 GAB dubultās rakstīšanas elementu kartes |
| Dynamics365GABParty_Anchor        | Dynamics 365 GAI un puse              |

Šajā pakotnē ir pieejamas šādas kartes.

| Finance and Operations programmas | Customer engagement programmas | 
|-----------------------------|--------------------------|
| CDS puses | msdyn_parties | 
| CDS pasta adreses vietas | msdyn_postaladdresscollections | 
| CDS pasta adreses vēsture V2 | msdyn_postaladdresses | 
| CDS puses pasta adreses vietas | msdyn_partypostaladdresses | 
| Puses kontaktpersonas V3 | msdyn_partyelectronicaddresses | 
| Debitori V3 | konti | 
| Debitori V3 | kontaktpersonas | 
| Kreditori V2 | msdyn_vendors | 
| Kontaktpersonu amati | msdyn_salescontactpersontitles | 
| Noslēguma frāzes | msdyn_complimentaryclosings | 
| Uzrunas | msdyn_salutations | 
| Lēmumu pieņemšanas lomas | msdyn_decisionmakingroles | 
| Nodarbinātības darbu funkcijas | msdyn_employmentjobfunctions | 
| Lojalitātes programmu līmeņi | msdyn_loyaltylevels | 
| Personas rakstura veidi | msdyn_personalcharactertypes | 
| Kontaktpersonas V2 | msdyn_contactforparties | 
| CDS pārdošanas piedāvājuma virsraksts | piedāvājumi | 
| CDS pārdošanas pasūtījumu virsraksti | salesorders | 
| Pārdošanas rēķinu galvenes V2 | rēķini | 
| CDS adrešu lomas | msdyn_addressroles |

**Informācija par atkarību**

Duālās rakstīšanas puses un globālās adrešu grāmatas risinājumi ir atkarīgi no trīs tālāk minētajiem iepakojumiem. Tāpēc jums ir jāinstalē šīs pakotnes pirms duālās rakstīšanas puses un globālās adrešu grāmatas risinājumu pakotnes instalēšanas.

- Duālās rakstīšanas programmas pamata pakotne
- Dubultās rakstīšanas finanšu pakotne
- Duālās rakstīšanas piegādes ķēdes iepakojums

