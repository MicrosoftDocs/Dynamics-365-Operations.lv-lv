---
title: Preces dimensijas
description: "Pastāv četras preču dimensijas: Krāsa, Konfigurācija, Izmērs un Stils. Preču dimensijas var apvienot dimensiju grupās, un dimensiju grupas var piešķirt preču šabloniem. Preču dimensiju kombinācijas nosaka, kā tiek definēti preču varianti."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 9cb4bded4b8d841c6d164e6b8ded2cb3fb4d0978
ms.contentlocale: lv-lv
ms.lasthandoff: 02/07/2018

---

# <a name="product-dimensions"></a>Preces dimensijas

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

Pastāv četras preču dimensijas: Krāsa, Konfigurācija, Izmērs un Stils. Preču dimensijas var apvienot dimensiju grupās, un dimensiju grupas var piešķirt preču šabloniem. Preču dimensiju kombinācijas nosaka, kā tiek definēti preču varianti.

Preču dimensijas ir īpašības, ko izmanto, lai identificētu preces variantu. Preču variantu definēšanai vai izmantot preču dimensiju kombinācijas. Lai izveidotu preces variantu, ir jādefinē vismaz viena preces dimensija preces šablonam.
Preces varianti
----------------

Preču varianti tiek saukti arī par krājumiem. Krājums ir materiāla prece, kas nav tāds pats kā pakalpojums. Var arī definēt preces šablonu, kura veids ir Pakalpojums. Izmantojot tipu Pakalpojums, varat norādīt preču variantus, kas ietver pakalpojumus. Piemēram, var norādīt preces šablonu konsultāciju darbam un preču variantus darbam, ko veic vecākie konsultanti un jaunākie konsultanti.

## <a name="product-dimensions"></a>Preces dimensijas
Ir pieejamas šādas preču dimensijas: Konfigurācija, Krāsa, Izmērs un Stils. Pamatojoties uz preces dimensijas vērtībām, var ģenerēt preces variantu.

Tādu preču dimensiju kā Izmērs, Krāsa un Stils vērtības var izveidot lapās **Izmērs**, **Krāsa** un **Stils**, kam var piekļūt šajās vietās: **Preču informācijas pārvaldība** &gt; **Iestatījumi** &gt; **Dimensiju un variantu grupas** &gt; **Izmēri/Krāsas/Stili**. Preces dimensijas Konfigurācija vērtības parasti tiek izveidotas, izmantojot preču konfiguratoru vai dimensiju konfiguratoru. Preces dimensijas var izveidot un uzturēt arī lapā **Preces dimensijas**, kam var piekļūt tālāk norādītajās vietās.
-   Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Preces** &gt; **Preču šabloni**. **Darbību rūtī** noklikšķiniet uz **Preču dimensijas**.
-   Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Preces** &gt; **Visas preces un preču šabloni**. Atlasiet preces šablonu. **Darbību rūtī** noklikšķiniet uz **Preču dimensijas**.
-   Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Izlaistās preces**. Atlasiet preces šablonu. **Darbību rūtī** noklikšķiniet uz**Prece**. Grupā **Preces šablons** noklikšķiniet uz **Preces dimensijas**.

Krājumam izveidojamo variantu skaitu ierobežo iespējamo preču dimensiju kombināciju skaits.

| **Padoms**                                                                                                                                              |
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






