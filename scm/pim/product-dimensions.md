---
title: Preces dimensijas
description: "Pastāv četri izstrādājuma izmēri - krāsu, konfigurācija, lielums un stils. Preču dimensijas var apvienot dimensiju grupās, un dimensiju grupas var piešķirt preču šabloniem. Preču dimensiju kombinācijas nosaka, kā tiek definēti preču varianti."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8854ab94a71cc363bcd073d2df47bc01a243b6cd
ms.lasthandoff: 03/31/2017


---

# <a name="product-dimensions"></a>Preces dimensijas

Pastāv četri izstrādājuma izmēri - krāsu, konfigurācija, lielums un stils. Preču dimensijas var apvienot dimensiju grupās, un dimensiju grupas var piešķirt preču šabloniem. Preču dimensiju kombinācijas nosaka, kā tiek definēti preču varianti.

Preču dimensijas ir īpašības, ko izmanto, lai identificētu preces variantu. Preču variantu definēšanai vai izmantot preču dimensiju kombinācijas. Lai izveidotu preces variantu, ir jādefinē vismaz viena preces dimensija preces šablonam.
Preces varianti
----------------

Preču varianti tiek saukti arī par krājumiem. Krājums ir materiāla prece, kas nav tāds pats kā pakalpojums. Ir iespējams noteikt produkta pamata ar pakalpojuma veidu. Izmantojot tipu Pakalpojums, varat norādīt preču variantus, kas ietver pakalpojumus. Piemēram, var norādīt preces šablonu konsultāciju darbam un preču variantus darbam, ko veic vecākie konsultanti un jaunākie konsultanti.

## <a name="product-dimensions"></a>Preces dimensijas
Ir pieejamas šādas preču dimensijas: konfigurācijas, krāsu, lielumu un stilu. Izstrādājuma variantu var ģenerēts, pamatojoties uz preču dimensijas vērtības.

Preču dimensijas vērtības, piemēram, lielumu, krāsu un stilu var izveidot **izmērs**, **krāsu** un **stila** lapas, kuram var piekļūt no šādām vietām: **produkta informācijas pārvaldības**&gt;**Setup**&gt;**dimensiju un variant grupas**&gt;**izmēri/krāsas/stili**. Preces dimensijas Konfigurācija vērtības parasti tiek izveidotas, izmantojot preču konfiguratoru vai dimensiju konfiguratoru. Preces dimensijas var izveidot un uzturēt arī lapā **Preces dimensijas**, kam var piekļūt tālāk norādītajās vietās.
-   Noklikšķiniet uz **produkta informācijas pārvaldības**&gt;**produkti**&gt;**produkta meistari**. Par **darbību rūti**, noklikšķiniet uz **izstrādājuma izmēri**.
-   Noklikšķiniet uz **produkta informācijas pārvaldības**&gt;**produkti**&gt;**visiem produktiem un produktu meistari**. Atlasiet preces šablonu. Par **darbību rūti**, noklikšķiniet uz **izstrādājuma izmēri**.
-   Noklikšķiniet uz **produkta informācijas pārvaldības**&gt;**atbrīvo produktus**. Atlasiet preces šablonu. Par **darbību rūti**, noklikšķiniet uz **produkta**. Grupā **Preces šablons** noklikšķiniet uz **Preces dimensijas**.

Krājumam izveidojamo variantu skaitu ierobežo iespējamo preču dimensiju kombināciju skaits.
| **Padoms **                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja izmantojat preci, piemēram, pasūtījuma rindā, izvēlieties preču dimensijas, lai norādītu preces variantu, ar ko vēlaties strādāt. |

## <a name="example"></a>Paraugs
Uzņēmums pārdod džinsus. Krājumam Džinsi tiek izmantotas preces dimensijas Krāsa un Izmērs. Džinsi tiek pārdoti trīs dažādās krāsas un sešos dažādos izmēros. Krāsas: zila, melna, brūna. Izmēri: XS, S, M, L, XL, XXL. Noteikti izmēti nav pieejami visās trīs krāsās. Ja būtu pieejamas visas kombinācijas, tā rezultātā būtu 18 dažādi džinsu veidi. Šajā piemērā tiek iegūtas tikai šādas deviņās preču variantu kombinācijas.

| Krāsa | Izmēri |
|-------|------|
| Zila  | XS   |
| Zila  | S    |
| Zila  | P    |
| melna | P    |
| melna | L    |
| melna | XL   |
| brūna | L    |
| brūna | XL   |
| brūna | XXL  |




