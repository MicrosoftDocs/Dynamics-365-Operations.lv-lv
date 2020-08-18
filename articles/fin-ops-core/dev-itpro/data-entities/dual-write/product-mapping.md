---
title: Vienotā preču pieredze
description: Šajā tēmā ir aprakstīta preču datu integrācija starp programmām Finance and Operations un Common Data Service
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 3b9a1485d37da614eea2427735e0e1323897682d
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621332"
---
# <a name="unified-product-experience"></a>Vienotā preču pieredze

[!include [banner](../../includes/banner.md)]



Ja biznesa ekosistēma ir izveidota no Dynamics 365 lietojumprogrammām, piemēram, Finance, Supply Chain Management un Sales, uzņēmumi bieži lieto šīs programmas, lai iegūtu preču datus. Tas ir tāpēc, ka šīs programmas nodrošina stabilu preču infrastruktūru, kas papildināta ar sarežģītākām cenu noteikšanas koncepcijām un precīziem rīcībā esošajiem krājumu datiem. Uzņēmumi, kuri izmanto ārējo Product Lifecycle Management (PLM) sistēmu, lai iegūtu produktu datus, var novirzīt produktus no Finance and Operations programmām uz citām Dynamics 365 programmām. Vienotā preču pieredze nodrošina integrētu preču datu modeli Common Data Service , lai visi programmas lietotāji, ieskaitot Power Platform lietotājus, var izmantot bagātīgo preču datu priekšrocības, ko sniedz Finance and Operations programmas.

Lūk, preču datu modelis no Sales.

![Preču datu modelis CE](media/dual-write-product-4.jpg)

Šeit it preču datu modelis no Finance and Operations programmām.

![Preču datu modelis pakalpojumā Finance and Operations](media/dual-write-products-5.jpg)

Šie divi preču datu modeļi ir integrēti Common Data Service, kā parādīts zemāk.

![Preču datu modelis Dynamics 365 lietojumprogrammās.](media/dual-write-products-6.jpg)

Duālā ieraksta elementa kartes precēm ir izveidotas, lai virzītu datus tikai vienā virzienā tuvu reāllaikam no Finance and Operations programmām uz Common Data Service. Tomēr, ja nepieciešams, preču infrastruktūra ir atvērta, lai to izveidotu kā divvirzienu. Kaut arī varat to pielāgot, jums pašiem jāuzņemas atbildība, jo korporācija Microsoft šo pieeju neiesaka.

## <a name="templates"></a>Veidnes

Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas. Kā redzams šajā tabulā, tiek izveidota elementa karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.

Finance and Operations programmas | Citas Dynamics 365 programmas | apraksts
-----------------------|--------------------------------|---
Izlaistās preces V2 | msdyn\_sharedproductdetails | **msdyn\_sharedproductdetails** elements satur laukus no Finance and Operations lietojumprogrammām, kas nosaka preci, un kurās ir ietverta preces finanšu un pārvaldības informācija. 
Common Data Service izlaistās atšķirīgās preces | Prece | **Preces** elements satur laukus, kas definē preci. Tā ietver atsevišķas preces (preces ar apakštipa preci) un preces variantus. Tālāk esošajā tabulā parādīta kartēšana.
Produkta numura identifikācijas svītrkods | msdyn\_productbarcodes | Preču svītrkodi tiek izmantoti, lai unikāli identificētu preces.
Pasūtījuma noklusējuma iestatījumi | msdyn\_productdefaultordersettings
Īpaši preču noklusējuma pasūtījuma iestatījumi | msdyn_productdefaultordersettings
Preces dimensiju grupas | msdyn\_productdimensiongroups | Preču dimensiju grupa definē, kuras preces dimensijas definē preci. 
Noliktavas dimensiju grupas | msdyn\_productstoragedimensiongroups | Produktu noliktavas dimensiju grupa atbilst metodei, kas tiek izmantota, lai definētu preces novietojumu noliktavā.
Izsekošanas dimensiju grupas | msdyn\_productstoragedimensiongroups | Preču izsekošanas dimensiju grupa parāda metodi, kas tiek izmantota, lai izsekotu preci krājumos.
Krāsas | msdyn\_productcolors
Izmēri | msdyn\_productsizes
Stili | msdyn\_productsytles
Konfigurācijas | msdyn\_productconfigurations
Preces šablona krāsas | msdyn_sharedproductcolors | **Koplietojamās preces krāsas** elements norāda krāsas, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Common Data Service, lai saglabātu datus saskaņotus.
Preces šablona izmēri | msdyn_sharedproductsizes | Elements **Koplietojamās preces izmērs** norāda izmērus, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Common Data Service, lai saglabātu datus saskaņotus.
Preces šablona stili | msdyn_sharedproductstyles | **Koplietojamās preces stila** elements norāda stilus, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Common Data Service, lai saglabātu datus saskaņotus.
Preces šablona konfigurācijas | msdyn_sharedproductconfigurations | **Koplietojamo preču konfigurācijas** elements norāda konfigurācijas, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Common Data Service, lai saglabātu datus saskaņotus.
Visas preces | msdyn_globalproducts | Visu preču elements satur visas preces, kas pieejamas Finance and Operations lietojumprogrammās, gan izlaistām, gan neizlaistām precēm.
Vienība | uoms
Mērvienību pārveidošana | msdyn_ unitofmeasureconversions
Īpaša preces mērvienības konversija | msdyn_productspecificunitofmeasureconversion
Preces kategorijas | msdyn_productcategories | Katra no preču kategorijām un informācija par tās struktūru un raksturlielumiem ir ietverta preču kategorijas elementā. 
Preču kategoriju hierarhijas | msdyn_productcategoryhierarhies | Varat izmantot preču hierarhijas, lai dalītu preces kategorijās vai grupās. Kategoriju hierarhijas ir pieejamas pakalpojumā Common Data Service, izmantojot preču kategoriju hierarhijas elementu. 
Preču kategoriju hierarhijas lomas | msdyn_productcategoryhierarchies | Preču hierarhijas var izmantot atšķirīgām lomām D365 Finance and Operations. Tās norāda, kura kategorija tiek izmantota katrai lomai, kurā preču kategorijas lomas elements tiek lietots. 
Preču kategoriju piešķires | msdyn_productcategoryassignments | Lai piešķirtu preci kategorijai, var izmantot preču kategorijas piešķires elementu.

## <a name="integration-of-products"></a>Preču integrēšana

Šajā modelī preci attēlo divu Common Data Serviceelementu kombinācija: **preces** un **msdyn\_sharedproductdetails**. Tā kā pirmais elements satur preces definīciju (preces unikālais identifikators, preces nosaukums un apraksts), otrais elements ietver laukus, kas tiek glabāti preču līmenī. Šo divu elementu kombinācija tiek izmantota, lai definētu preci atbilstoši krājumu uzskaites vienības (SKU) koncepcijai. Katrai izlaistajai precei būs sava informācija minētajos elementos (Prece un Koplietojamā informācija par preci). Lai izsekotu visām precēm (izlaistas un nav izlaistas), tiek izmantots elements **Globālās preces**. 

Tā kā produkts tiek attēlots kā SKU, atšķirīgu preču, preču šablonu un preču variantu koncepcijas var uztvert Common Data Servicešādi:

- **Preces ar apakštipa preci** ir preces, kas definētas pašas. Dimensijas nav jādefinē. Piemērs ir noteikta grāmata. Šīm precēm viens ieraksts tiek izveidots**Preces** elementā, un viens ieraksts tiek izveidots **msdyn\_sharedproductdetails** elementā. Nav izveidots neviens preču saimes ieraksts.
- **Preču šabloni** tiek izmantoti kā ģenēriskas preces, kas satur definīciju un nosacījumus, kas nosaka biznesa procesu darbību. Balstoties uz šīm definīcijām, var tikt ģenerētas atšķirīgas preces, kas zināmas kā preces varianti. Piemēram, T-krekls ir preces šablons, un tam var būt Krāsa un Izmērs dimensiju veidā. Var izlaist variantus, kuriem ir dažādas šo dimensiju kombinācijas, piemēram, mazs zils T-krekls vai vidēji zaļš T-krekls. Integrācijā katram variantam preču tabulā tiek izveidots viens ieraksts. Šis ieraksts satur ar variantu saistītu informāciju, piemēram, dažādas dimensijas. Vispārīgā informācija par preci tiek uzglabāta **msdyn\_sharedproductdetails** elementā. (Šī ir vispārīga informācija tiek turēta preces pamatinformācijā.) Preces pamatinformācija tiek sinhronizēta Common Data Service, tiklīdz tiek izveidots izlaistais preces šablons (bet pirms tiek izlaisti varianti).
- **Atšķirīgas preces** attiecas uz visām produktu apakštipa precēm un visiem preces variantiem. 

![Preču datu modelis](media/dual-write-product.png)

Ar iespējotu duālās rakstīšanas funkcionalitāti Finance and Operations lietojumprogrammas tiks sinhronizētas citās Dynamics 365 lietojumprogrammās **Melnraksta** stāvoklī. Tās tiek pievienotas pirmajam cenrādim ar nemainīgu valūtu. Citiem vārdiem, tie ir pievienoti pirmajam cenrādim Dynamics 365 lietojumprogrammā, kas atbilst jūsu juridiskās personas valūtai, kur prece tiek izdota Finance and Operations programmā. 

Pēc noklusējuma preces no Finance and Operations programmām tiek sinhronizētas ar citām Dynamics 365 programmām statusā **Melnraksts**. Lai sinhronizētu preci ar statusu **Aktīvs**, lai varētu to tieši izmantot pārdošanas pasūtījuma piedāvājumos, ir jāizvēlas, piemēram, šāds iestatījums: cilnē **Sistēma > Administrēšana > Sistēmas administrēšana > Sistēmas iestatījumi > Pārdošana** atlasiet opciju **Izveidot preces aktīvā stāvoklī = Jā**. 

Ņemiet vērā, ka preču sinhronizācija notiek no Finance and Operations programmām uz Common Data Service. Tas nozīmē, ka preču elementa lauku vērtības var mainīt pakalpojumā Common Data Service, taču, kad sinhronizācija tiks uzsākta (kad preces lauks tiek modificēts programmā Finance and Operations ), to vērtības tiks pārrakstītas pakalpojumā Common Data Service. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Preces dimensijas 

Preču dimensijas ir īpašības, ko izmanto, lai identificētu preces variantu. Četras preces dimensijas (krāsa, lielums, stils un konfigurācija) ir arī kartētas Common Data Service, lai definētu preces variantus. Sekojošajā attēlā ir parādītas preces dimensijas krāsas datu modelis. Tas pats modelis ir piemērots izmēriem, stiliem un konfigurācijām. 

![Preču datu modelis](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Ja precei ir dažādas preces dimensijas (piemēram, preces šablona izmērs un krāsa ir tādas pašas kā preces dimensijas), katra atšķirīga prece (t.i., katrs preču variants) tiek definēta kā šo preču dimensiju kombinācija. Piemēram, preču numurs B0001 ir īpaši mazs, melns T krekls, un preces numurs B0002 ir neliels melns T krekls. Šādā gadījumā tiek definētas esošās preču dimensiju kombinācijas. Piemēram, no iepriekšējā piemēra T-krekls var būt īpaši mazs un melns, mazs un melns, vidējs un melns vai liels un melns, bet tas nevar būt īpaši liels un melns. Citiem vārdiem sakot, preču dimensijas, ko var veikt preces šablons, ir norādītas, un variantus var izlaist, pamatojoties uz šīm vērtībām.

Lai sekotu preču dimensijām, ko var veikt preces šablons, katrai preces dimensijai tiek izveidoti un kartēti Common Data Service tālāk norādītie elementi. Papildinformāciju skatiet rakstā, [Preču informācija](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Noklusējuma pasūtījuma iestatījumi un preces specifiskie noklusējuma iestatījumi

Pasūtījuma noklusējuma iestatījumi definē vietu un noliktavu, kur krājumi tiks iegūti vai glabāti, minimālos, maksimālos, vairākkārtējos un standarta daudzumus, kas tiks izmantoti tirdzniecībai vai krājumu pārvaldībai, izpildes laikus, apturēšanas karodziņus un pasūtījumu solīšanas metodes. Šī informācija ir pieejama Common Data Service, izmantojot noklusētos pasūtījuma iestatījumus un preces specifiskos noklusējuma pasūtījuma iestatījumu elementu. Plašāku informāciju par funkcionalitāti varat izlasīt tēmā [Noklusējuma pasūtījuma iestatījumi](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mērvienība un mērvienību pārvēršana

Mērvienības un to atbilstošais pārveidojums ir pieejami Common Data Service sekojošajā datu modelī, kas redzams diagrammā.

![Preču datu modelis](media/dual-write-product-three.png)

Mērvienības koncepcija ir integrēta starp Finance and Operations un citām Dynamics 365 lietojumprogrammām. Katrai mērvienību klasei Finance and Operations lietojumprogrammā tiek izveidota mērvienību grupa Dynamics 365 lietojumprogrammā, kas satur mērvienības, kas pieder pie mērvienību kategorijas. Katrai vienību grupai tiek izveidota arī noklusētā pamatvienība. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>Sākotnējā atbilstošo datu vienību sinhronizēšana starp programmu Finance and Operations un Common Data Service

### <a name="initial-synchronization-of-units"></a>Sākotnējā vienību sinhronizācija

Kad duālais ieraksts ir iespējots, vienības no Finance and Operations programmām tiek sinhronizētas ar citām Dynamics 365 programmām. Vienību grupas, kas tiek sinhronizētas no Finance and Operations programmām pakalpojumā Common Data Service, ir atzīmētas ar karodziņu kopu, kas norāda, ka tās ir "Uzturētas ārēji".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Atbilstošās vienības un vienību klases/grupas dati no Finance and Operations un citām Dynamics 365 programmām

Pirmkārt, ir svarīgi atzīmēt, ka vienības integrācijas atslēga ir msdyn_symbol. Tāpēc šai vērtībai ir jābūt unikālai pakalpojumā Common Data Service vai citās Dynamics 365 programmās. Tā kā citās Dynamics 365 programmās vienības unikalitāti nosaka pāris "Vienību grupas ID" un "Nosaukums", ir jāapsver dažādi scenāriji, kā saskaņot vienību datus starp Finance and Operations programmām un Common Data Service.

Vienībām, kas atbilst/pārklājas Finance and Operations programmās un citās Dynamics 365 lietojumprogrammās:

+ **Vienība pieder vienību grupai citās Dynamics 365 programmās, kas atbilst saistītajai vienību klasei Finance and Operations programmās**. Šādā gadījumā lauks msdyn_symbol citās Dynamics 365 programmās ir jāaizpilda ar vienības simbolu no Finance and Operations programmām. Tāpēc, kad dati tiks saskaņoti, vienību grupa tiks iestatīta kā "Uzturēta ārēji" citās Dynamics 365 programmās.
+ **Vienība pieder kādai vienību grupai citās Dynamics 365 programmās, kas neatbilst saistītajai vienību klasei Finance and Operations programmās (neviena no esošajām vienību klasēm Finance and Operations programmās citās Dynamics 365 lietojumprogrammās).** Šādā gadījumā msdyn_symbol jāaizpilda ar nejaušu virkni. Ņemiet vērā, ka šai vērtībai ir jābūt unikālai citās Dynamics 365 programmās.

Vienībām un vienību klasēm Finance and Operations programmās, kas nepastāv citās Dynamics 365 programmās:

Kā daļa no duālā ieraksta vienību grupas no Finance and Operations programmām un tās atbilstošās vienības tiek izveidotas un sinhronizētas citās Dynamics 365 programmās un Common Data Service, un vienību grupa tiks iestatīta kā "Uzturēta ārēji". Nav nepieciešama papildu sāknēšana.

Vienībām citās Dynamics 365 programmās, kas nepastāv Finance and Operations programmās:

Laukam msdyn_symbol jābūt aizpildītam visām vienībām. Vienības vienmēr var izveidot Finance and Operations programmās atbilstošajā vienību klasē (ja tāda ir). Ja vienības klase nepastāv, vispirms ir jāizveido vienību klase (ņemiet vērā, ka vienības klasi nevar izveidot Finance and Operations programmās, izņemot paplašinājumu, ja paplašināt uzskaitījumu), kas atbilst pārējo Dynamics 365 programmu vienību grupai. Pēc tam varat izveidot vienību. Ņemiet vērā, ka vienības simbolam Finance and Operations programmās jābūt msdyn_symbol, kas vienībai iepriekš norādīts citās Dynamics 365 programmās.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Preces politikas: dimensija, izsekošanas un glabāšanas grupas

Preces politikas ir politiku kopas, ko izmanto preču definēšanai un to raksturlielumus krājumos. Produktu dimensiju grupa, preču izsekošanas dimensiju grupa un noliktavas dimensiju grupa ir atrodama kā produktu politikas. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Preču hierarhijas

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Preču integrācijas atslēga 

Lai unikāli identificētu preces starp Dynamics 365 for Finance and Operations un precēm pakalpojumā Common Data Service, tiek izmantotas integrācijas atslēgas. Precēm **(productnumber)** ir unikāla atslēga, kas identificē preci pakalpojumā Common Data Service. To veido šāda konkatenācija: **(uzņēmums, msdyn_productnumber)**. **Uzņēmums** norāda juridisko personu Finance and Operations, un **msdyn_productnumber** norāda preces numuru konkrētai precei Finance and Operations. 

Citu Dynamics 365 programmu lietotājiem prece tiek identificēta UI ar **msdyn_productnumber** (ņemiet vērā, ka lauka etiķete ir **Preces numurs**). Preces veidlapā tiek rādīts gan uzņēmums, gan msydn_productnumber. Tomēr lauks (productnumber) — unikālā preces atslēga — netiek rādīts. 

Ja izveidojat programmas pakalpojumā Common Data Service, ir jāpievērš uzmanība tam, kā izmantojat **productnumber** (unikālo produkta ID) kā integrācijas atslēgu. Nelietojiet **msdyn_productnumber**, jo tā nav unikāla. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>Sākotnējā preču sinhronizācija un datu migrēšana no Common Data Service uz Finance and Operations

### <a name="initial-synchronization-of-products"></a>Sākotnējā preču sinhronizācija 

Kad duālais ieraksts ir iespējots, preces no Finance and Operations programmām tiek sinhronizētas ar Common Data Service un citām modeļa vadītām programmām pakalpojumā Dynamics 365. Preces, kas izveidotas Common Data Service un citās Dynamics 365 programmās pirms duālā ieraksta palaišanas, netiks atjauninātas vai saskaņotas ar preču datiem no Finance and Operations programmām.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Atbilstošie preču dati no Finance and Operations un citām Dynamics 365 programmām

Ja vienas un tās pašas preces tiek turētas (pārklāšanās/salīdzināšana) Finance and Operations un Common Data Service, un citās Dynamics 365 programmās, iespējojot duālo ierakstu, tiks veikta preču sinhronizācija no Finance and Operations, un vienai un tai pašai precei parādīsies dublikāta ieraksti pakalpojumā Common Data Service.
Lai izvairītos no iepriekš minētās situācijas, ja citām Dynamics 365 programmām ir produkti, kas pārklājas/saskan ar Finance and Operations, tad administratoram, iespējojot duālo ierakstu, ir jāsāknē lauki **Uzņēmums** (piemērs: "USMF") and **msdyn_productnumber** (piemērs: "1234:Black:S"), pirms tiek veikta preču sinhronizēšana. Citiem vārdiem sakot, šie divi preces lauki pakalpojumā Common Data Service ir jāaizpilda ar attiecīgo uzņēmumu Finance and Operations, ar kuru prece ir jāsaskaņo, un ar preces numuru. 

Pēc tam, kad sinhronizācija ir iespējota un notiek, preces no Finance and Operations tiks sinhronizētas ar saskaņotajām precēm pakalpojumā Common Data Service un citās Dynamics 365 programmās. Tas ir attiecināms uz atšķirīgām precēm un preču variantiem. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Preču datu migrēšana no citām Dynamics 365 programmām uz Finance and Operations

Ja citās Dynamics 365 programmās ir preces, kas nav iekļautas Finance and Operations, administrators var vispirms izmantot **EcoResReleasedProductCreationV2Entity**, lai importētu šīs preces Finance and Operations. Un, otrkārt, saskaņot preču datus no Finance and Operations un citām Dynamics 365 programmām, kā aprakstīts iepriekš. 
