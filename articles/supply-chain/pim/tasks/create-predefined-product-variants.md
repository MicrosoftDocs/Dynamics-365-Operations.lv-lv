---
title: Iepriekš definētu preces variantu izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d3a4ae8efd438e01c263af1c0a1746d9484e491
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103102"
---
# <a name="predefined-product-variants"></a>Iepriekš definēts preces variants

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Piemērs: Iepriekš definētu preces variantu izveide

Šajā piemērā parādīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Lai sekotu šim scenārijam, izmantojot šeit ieteiktās vērtības, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa *USMF* juridiskā persona.

### <a name="step-1-create-a-product-master"></a>1. darbība: Preces šablona izveide

Lai izveidotu preces šablonu:

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība > Preces > Preces šabloni**.
1. Atlasiet **Jauns**.
1. Ja laukā **Preces numurs** nav norādīts skaitlis, tad ievadiet vērtību. Tas ir nepieciešams, ja šim laukam nav iestatīta numuru sērija.
1. Ievadiet nosaukumu laukā **Preces nosaukums**.
1. Laukā **Preces dimensijas grupa** atlasiet preces dimensiju grupu *SizeCol* (Izmērs un Krāsa).
1. Atlasiet **Labi**, lai izveidotu un atvērtu jauno preces šablonu.

### <a name="step-2-add-product-dimensions"></a>2. darbība: Pievienot preces dimensijas

Šajā piemērā parādīts, kā manuāli ievadīt preču dimensijas. Jūs varat arī atlasīt izmēru, krāsu un stilu grupu, kurā ietilpst preces dimensiju vērtības, ko vēlaties izmantot.

Lai pievienotu preces dimensijas:

1. Kad jaunais preces šablons joprojām ir atvērts, darbību rūtī atlasiet **Preces dimensijas**.
1. Atveriet cilni **Izmērs** un rīkjoslā atlasiet **Jauns**, lai režģim pievienotu rindu. Jaunajai rindai veiciet šādus iestatījumus:
    - **Izmērs:** atlasiet lieluma vērtību.
    - **Nosaukums:** ievadiet elementa izmēru.
1. Rīkjoslā atlasiet **Jauns** un pievienojiet režģim otru izmēru ar jaunu **Izmēru** un **Nosaukumu**.
1. Atveriet cilni **Krāsas** un rīkjoslā atlasiet **Jauns**, lai režģim pievienotu rindu. Jaunajai rindai veiciet šādus iestatījumus:
    - **Krāsa:** atlasiet krāsas vērtību.
    - **Nosaukums:** ievadiet elementa krāsu.
1. Rīkjoslā atlasiet **Jauns** un pievienojiet režģim otru krāsu ar jaunu **Krāsu** un **Nosaukumu**.
1. Atlasiet **Saglabāt**.
1. Aizveriet lapu, lai atgrieztos pie jaunā preces šablona.

### <a name="step-3-generate-product-variants"></a>3. darbība: Ģenerēt preces variantus

> [!NOTE]
> Šajā sadaļā ir aprakstīts, kā ģenerēt preču variantus, ja nav iespējots līdzeklis *Variantu ieteikumu lapas uzlabojumi*. Skatiet nākošo sadaļu, lai iegūtu detalizētu informāciju par to, kā izveidot preču variantus, kad šis līdzeklis ir pieejama.

Lai ģenerētu preces variantus:

1. Kad jaunais preces šablons joprojām ir atvērts, darbību rūtī atlasiet **Preču vavianti**.
1. Darbību rūtī atlasiet **Variantu ieteikumi**.
1. Sistēma izveido sarakstu ar visām iespējamām produkta lielumu un krāsu kombinācijām. Atlasiet **Atlasīt visu** rīkjoslā.
    - Šajā piemērā atlasiet visus iespējamos variantus. Ja vēlaties izmantot tikai iespējamo preces dimensiju kombināciju apakškopu, atzīmējiet tikai nepieciešamās izvēles rūtiņas pēc nepieciešamības.  
1. Atlasiet **Izveidot**.
1. Atlasiet **Saglabāt**.

## <a name="improved-variant-suggestions"></a>Uzlaboti variantu ieteikumi

Līdzeklis *Variantu ieteikumu lapas uzlabojumi* uzlabo lapu **Variantu ieteikumi**, lai novērstu veiktspējas un lietojamības problēmas uzņēmumiem, kuriem ir liels preču dimensiju kombināciju skaits. Uzlabotais produktu dimensiju vērtību atlases process, kuram ģenerēt varianta ieteikumus, ļauj ātrāk un vieglāk identificēt un atbrīvot attiecīgos produkta variantus.

Šim līdzeklim ir pievienoti šādi uzlabojumi:

- **Variantu ieteikumu atliktā ģenerēšana:** atverot lapu **Variantu ieteikumi**, tajā vairs netiek rādīti ieteikumi. Tā vietā ir skaidri jāizvēlas, kuras vērtības būs nepieciešamas, un pēc tam jāatlasa poga **Ieteikt**, lai ģenerētu kombinācijas. Tas padara procesu redzamu un interaktīvu.
- **Dimensiju vērtību atlase:** Ja jums ir daudz dimensiju vērtību, jūs parasti interesējaties par variantu ieteikumu ģenerēšanu, kas ietver tikai dažas no tām (piemēram, ieviešot jaunu krāsu vai stilu kopu). Ar uzlaboto dizainu varat atlasīt dimensiju vērtības, kurām vēlaties ģenerēt preču variantu ieteikumus. Tas lielā veidā palielina ieteikto variantu atbilstību un uzlabo gan sistēmas veiktspēju, gan lietotāja produktivitāti.

### <a name="turn-the-variant-suggestions-page-improvements-feature-on-or-off"></a>Ieslēgt vai izslēgt variantu ieteikumu lapu uzlabojumu līdzekli

No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma. Administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot variantu ieteikumu *lapas uzlabojumu līdzekli* līdzekļu pārvaldības [darbvietā](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="work-with-the-improved-variant-suggestions"></a>Darbs ar uzlabotajiem variantu ieteikumiem

Lai ģenerētu preču variantu ieteikumus, ja ir iespējots līdzeklis *Variantu ieteikumu lapas uzlabojumi*:

1. Atveriet vai izveidojiet preces šablonu un pievienojiet tam nepieciešamās preču dimensijas, kā aprakstīts iepriekšējā sadaļā.
1. Kad preces šablons ir atvērts, darbību rūtī atlasiet **Preču vavianti**.
1. Darbību rūtī atlasiet **Variantu ieteikumi**.
1. Atlasiet vērtības, kuras vēlaties lietot katrai dimensijai.
1. Augšējā rīkjoslā atlasiet **Ieteikt**.
1. Sistēma izveido sarakstu ar visām iespējamām atlasīto izmēru un krāsu kombinācijām. Kopsavilkuma cilnē **Ieteiktie varianti** atzīmējiet izvēles rūtiņu katrai preces dimensijas kombinācijai, ko vēlaties izmantot, vai rīkjoslā atlasiet **Atlasīt visu**, lai atlasītu visus no tiem.  
1. Atlasiet **Izveidot**, lai pašreizējam preces šablonam pievienotu variantus.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
