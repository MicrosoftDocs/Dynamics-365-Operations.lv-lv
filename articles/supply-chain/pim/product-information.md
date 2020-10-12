---
title: Preču informācijas pārskats
description: Šajā tēmā ir sniegta informācija par preču informācijas pārvaldību. Preču informācijas pārvaldība darbojas ar kopīgoto preču definīciju, kategoriju un identifikatoriem visās juridiskajās personās, kā arī ar noteiktām preču konfigurācijām, lai ietilptu biznesa procesos.
author: benebotg
manager: tfehr
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace, EcoResProductVariantPerCompanyImagePart, EcoResProductRelationType,EcoResProductAvailabilityPart,  EcoResProductReleasedSelect, EcoResProductLookup, EcoResProductVariantsPendingReleaseFormPart, EcoResProductSearchLookup, EcoResProductNumberRename, EcoResDimensionBasedConfigWorkspace, EcoResProductVariantImagePart, EcoResProductImagePart, EcoResProductVariantsPerCompanyPart, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleaseSessions, EcoResProductVariantMaintainWorkspaceConfiguration, EcoResProductProcessManufacturingWorkspaceConfiguration, EcoResProductMasterVariantsPart, EcoResProductDiscreteManufacturingWorkspaceConfiguration, EcoResProductVariantAvailabilityPart, EcoResProductInformationFactBox, EcoResProductLookupTest, EcoResProductImageTest, EcoResProductReleasedRecentlyCreatedFormPart, EcoResPhysicalProductDimensions, PdsMRCRegulatedListItem, EcoResProductAvailabilityPart, PdsMRCRestrictionList, InventItemIdLookupAllocationId, EcoResProductAvailability, EcoResProductEntityAttributeTableFieldAssociation, EcoResProductImagePart, EcoResProductRelation, EcoResProductReleaseAddProduct, EcoResProductPerCompanyListPage, EcoResProductParameters, PdsMRCRestrictedItemByCountryState, EngChgCasePreview, InventTablePreview, PdsMRCItemDetails, EngChgCaseAssociate, PdsMRCCustomerHistory, PdsMRCVendorHistory, PdsMRCRestrictedCountryStateByItem, InventItemIdGroupLookup, InventLocationLookup, PdsMRCValidityIntervalbyCountry, PdsMRCValidityIntervalbyCountry, PdsMRCEventTracker, PdsMRCReportingCountry, PdsMRCDocument, PdsMRCReportingList, PdsMRCItemCAS, GraphicsTestForm, EngChgPicklist
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e5983fa7272a89d28699eb10bb9c5e0d79490ae
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895576"
---
# <a name="product-information-overview"></a>Preču informācijas pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par preču informācijas pārvaldību. Preču informācijas pārvaldība darbojas ar kopīgoto preču definīciju, kategoriju un identifikatoriem visās juridiskajās personās, kā arī ar noteiktām preču konfigurācijām, lai ietilptu biznesa procesos. 

Preču informācija ir piegādes ķēžu un komercijas programmu pamats visās nozarēs. Tas attiecas uz procesiem un tehnoloģijām, kas fokusējas uz centralizētu preču informācijas pārvaldību (piemēram, piegādes ķēdēs). Ir svarīgi izmantot kopīgotas preču definīcijas, dokumentāciju, atribūtus un identifikatorus. Dažādos biznesa risinājumu moduļos preču informācija un konfigurācija ir vajadzīga, lai pārvaldītu biznesa procesus, kas ir saistīti ar īpašām precēm, preču saimēm vai kategorijām.

## <a name="product-definition"></a>Preču definīcija

Preces galvenokārt nosaka pēc preces numura, nosaukuma un apraksta. Lai aprakstītu preci vai pakalpojumu, tomēr ir nepieciešami arī citi dati.

- Preces veids: krājums vai pakalpojums
- Preces apakšveids: atšķirīgas preces vai preču šabloni
- Preces varianta modeļa definīcija

     - Preču dimensijas un dimensiju grupas
     - Preču nomenklatūra
     - Preču konfigurācijas modeļi

- Preces saistība ar vienu vai vairākām kategorijām
- Preces un kategorijas atribūtu definīcija
- Preces attēli
- Pielikumi
- Mērvienības un saistītās pārveides
- Visu nosaukumu un aprakstu tulkojumi

## <a name="distribution-export-and-import-of-product-data"></a>Preces datu izplatīšana, imports un eksports

Preces definīciju var izveidot programmatūrā Supply Chain Management. Tas var arī importēt no šādām sistēmām: preces dzīves cikla pārvaldība (PLM), preču datu pārvaldība (PDM) vai preces informācijas pārvaldība (PIM). Ja tiek izmantotas vairākas Supply Chain Management instances, viena instance parasti tiek izmantota kā visu pārējo instanču preču datu šablons. Šo pieeju atbalsta liela datu elementu kopa, kas ļauj eksportēt un importēt preču definīcijas datus no vienas instances uz citu.

Lai atbalstītu preces datu izplatīšanu daudzās instancēs, programma Supply Chain Management sniedz iespēju izmantot pakalpojumu Common Data Service. Preču definīcijas var eksportēt no Supply Chain Management instances uz pakalpojumu Common Data Service. Pēc tam preču definīcijas var izmantot, lai nodrošinātu preces datus citām biznesa programmām, piemēram, Dynamics 365 Sales.

Ņemiet vērā, ka dinamiskās un elastīgās organizācijās, preču informācijas dati mainās katru dienu. Tādēļ precīzu un aktuālu preču datu uzturēšana ir būtisks biznesa process.

## <a name="product-masters-and-product-variants"></a>Preču šabloni un varianti

Elastīgā pasaulē, ja preces ir ātri jāpielāgo klienta prasībām, preču definīcijas jānorāda kā preču kopa nevis atšķirīgas preces. Programmatūrā Supply Chain Management šīs vispārīgās preces tiek sauktas par *preču šabloniem*. Preču šabloni satur definīciju un kārtulas, kas norāda, kā atšķirīgas preces tiek aprakstītas un darbojas biznesa procesos. Pamatojoties uz šīm definīcijām, var tikt ģenerētas atšķirīgas preces. Šīs atšķirīgās preces tiek sauktas par *preces variantiem*.

Preces šablons tiek saistīts ar preču dimensiju grupu un konfigurācijas tehnoloģiju, lai norādītu biznesa kārtulas. Preču dimensijas (krāsa, izmēri, stils un konfigurācija) ir specifiskas atribūtu kopas, ko var izmantot visā programmā, lai definētu un izsekotu noteiktu saistīto preču izturēšanos. Šīs dimensijas arī palīdz lietotājiem meklēt un identificēt preces.

## <a name="configuration-technologies"></a>Konfigurācijas tehnoloģijas

Varat izvēlēties no trim konfigurācijas tehnoloģijām.

- Iepriekš definēti varianti tiek definēti ar iepriekš definētām preču dimensijām. Varianta definīcija ietver noteiktas derīgas dimensiju kombinācijas definīciju, piemēram, krāsu, stilu un izmēru. Katra kombinācija veido atšķirīgu preces variantu.
- Konfigurāciju atbilstoši dimensijām parasti lieto ražošanas scenārijos, un tā ļauj izmantot konfigurācijas dimensiju materiālu komplektu (MK) definīcijā. Ja noteikta konfigurācija ir atlasīta, sistēma izmanto plānošanā un ražošanā to MK rindu apakškopu, kuras ir derīgas attiecīgajai konfigurācijai. Šī koncepcija ir zināma arī kā *globālais MK*, jo viens koplietojams MK tiek izmantots visām preces konfigurācijām.
- Konfigurācijas atbilstoši ierobežojumam preces izmanto konfigurācijas modeli, lai aprakstītu visus iespējamos atribūtus un komponentus, kas nepieciešami, lai vienā modelī aprakstītu visus iespējamos preces variantus. Atribūtu kombināciju ierobežojumus var aprakstīt, izmantojot regulāras izteiksmes vai tabulas ierobežojumus. Konfigurācijas modeļi un konfigurētāji kļūst svarīgāki preču informācijas pārvaldības procesā un tiek izmantoti visās nozarēs.

Plānojot Supply Chain Management ieviešanu, ir ļoti svarīgi izvēlēties pareizu biznesa procesa konfigurācijas tehnoloģiju. Preci nevar pārveidot no viena modeļa uz citu pēc ieviešanas.

## <a name="product-variant-model-definition-workspace"></a>Preces varianta modeļa definīcijas darbvieta

**Preces varianta modeļa definīcijas** darbvieta sniedz pārskatu par preču šabloniem. Tas parāda arī šablonu un saistīto variantu izlaišanas statusu konkrētām juridiskām personām.

## <a name="released-products"></a>Izlaistās preces

Preces, kas tiek izlaistas konkrētai juridiskajai personai tiek sauktas par *izlaistajām precēm*. Preces var izlaist lielapjoma vienībās vienai juridiskajai personai vai vienlaicīgi vairākām juridiskajām personām. Juridiskajai personai var pievienot dažādus preču rekvizītus un atribūtus, tādēļ darbvieta **Izlaisto preču uzturēšana** ļauj pārraudzīt un pabeigt katrai juridiskajai personai vai juridiskās personas apakšorganizācijām nesen izlaistās preces.

### <a name="released-product-maintenance-workspace"></a>Izlaisto preču uzturēšanas darbvieta

Darbvietu **Izlaisto preču uzturēšana** varat konfigurēt no izvēlnes vienuma **Konfigurēt manu darbvietu**. Atlasiet mazumtirdzniecības kategoriju hierarhiju un kategoriju, lai filtrētu darbvietu. Lai koriģētu darbvietas preču datus, var arī norādīt, dienās, laika periodus **Pēdējās izlaistās preces** un **Preces, kuru izlaide ir pārtraukta**.

Darbvietu veido elementu un divu sarakstu kopsavilkums. Sarakstā **Atvērtie pieteikumi** tiek rādīti preču izmaiņu gadījumi, kuriem ir preces atlasītajā preču kategoriju hierarhijā, kas nav pabeigtas un slēgtas. Sarakstā **Pēdējās izlaistās** tiek rādītas preces, kas tika izlaistas laika periodā, kas tika iestatīts darbvietas konfigurācijā. Katram saraksta krājumam tiek veikta pārbaude un tiek parādīts pārbaudes statuss. Šis statuss varētu norādīt, ka juridiskajai personai nepieciešamā konfigurācija nav pabeigta. No saraksta varat tieši piekļūt lapai **Nodoto preču papildinformācija**, **Preces īpašību uzturēšana**, **Preces kategorijas uzturēšana**, **Noklusējuma pasūtījuma iestatījumi** un **Teksta tulkojumi**, lai pabeigtu nepieciešamo preču konfigurāciju.

### <a name="manually-creating-a-new-released-product"></a>Manuāla jaunas izlaistās preces izveide

Varat manuāli izveidot izlaistu preci vienā izpildē, atkarībā no organizācijas biznesa procesiem un noteikumiem par to, vai vajadzētu izmantot šo funkciju. Šī funkcija izveido jaunu preci un automātiski atbrīvo to pašreizējai juridiskajai personai. Lai izveidotu jaunu preci, noklikšķiniet uz **Izlaistās preces** darbvietā **Izlaisto preču uzturēšana** vai saraksta lapā **Izlaistā prece**.
