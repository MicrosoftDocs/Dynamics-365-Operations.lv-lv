---
title: "Preces variantu numuru no nosaukumu nomenklatūra"
description: "Šajā tēmā ir aprakstīts, kā iestatīt preču numuru nomenklatūru, lai aizstātu fiksēto formātu [preces šablona numurs-konfigurācija-izmērs-krāsa-stils]. Jaunajai nomenklatūrai ir mērķim pielāgots formāts, kurā ir ietverts preces šablona numurs, aktīvās preces dimensijas un jūsu izvēles teksta atdalītāji. Varat arī izveidot preču nosaukumu nomenklatūru. Varat arī izveidot nomenklatūru, lai norādītu konfigurācijas, kas ir izveidotas, izmantojot ierobežojumiem atbilstošo preču konfiguratoru. Šajās nomenklatūrās var būt jūsu izvēlētie atribūti."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 4ebebc1d287908dbe8ac7557c34fc6693c88bfae
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Preces variantu numuru no nosaukumu nomenklatūra

Šajā tēmā ir aprakstīts, kā iestatīt preču numuru nomenklatūru, lai aizstātu fiksēto formātu [preces šablona numurs-konfigurācija-izmērs-krāsa-stils]. Jaunajai nomenklatūrai ir mērķim pielāgots formāts, kurā ir ietverts preces šablona numurs, aktīvās preces dimensijas un jūsu izvēles teksta atdalītāji. Varat arī izveidot preču nosaukumu nomenklatūru. Varat arī izveidot nomenklatūru, lai norādītu konfigurācijas, kas ir izveidotas, izmantojot ierobežojumiem atbilstošo preču konfiguratoru. Šajās nomenklatūrās var būt jūsu izvēlētie atribūti.

Jaunās preces variantu numuru un preces variantu nosaukumu nomenklatūras sniedz iespēju iekļaut segmentus preces variantu identifikatoros. Šajos segmentos var būt ietverts preces šablona numurs un nosaukums, preces dimensijas ID un nosaukums, numuru sērijas, teksta konstantes un atribūti. Šī funkcija sniedz iespēju ātri atrast noteiktu preces variantu, kad veidojat pārdošanas pasūtījumu vai pirkšanas pasūtījumu. Gan preces variantu numuru, gan preces variantu nosaukumu nomenklatūras varat izveidot, izmantojot lapu **Preču nomenklatūra**. Lai atvērtu šo lapu, noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Iestatījumi**.

## <a name="nomenclature-of-predefined-product-variants"></a>Iepriekš definētu preces variantu nomenklatūra
Preces varianti tiek ģenerēti preces šabloniem saskaņā ar vienu no trim konfigurācijas tehnoloģijām:

-   Iepriekš definēti varianti
-   Atbilstoši ierobežojumam
-   Atbilstoši dimensijai

Katram preces variantam ir numurs un nosaukums, un preces variantu identifikācijas nomenklatūras sniedz iespēju atlasīt segmentus, kas ir jāiekļauj katrā preces varianta numurā vai nosaukumā. Lapā **Preču nomenklatūra** varat atlasīt tālāk norādīto segmentus.

-   Preces šablona numurs
-   Preces šablona nosaukums
-   Numuru sērijas vērtība
-   Teksta konstante
-   Preces dimensijas
    -   Konfigurācijas ID vai nosaukums
    -   Krāsas ID vai nosaukums
    -   Izmēra ID vai nosaukums
    -   Stila ID vai nosaukums

Pēc preces variantu identifikācijas numuru nomenklatūras definēšanas varat to saistīt ar preces dimensiju grupu. Pēc tam visiem preču šabloniem, kuros ir ietvertas atsauces uz šo preces dimensiju grupu, tiek piešķirti preces variantu numuri atbilstoši šai nomenklatūrai. Taču preces variantu nosaukumu nomenklatūras nevar saistīt ar preces dimensiju grupām. Preces variantu identifikācijas nomenklatūru var arī tiešā veidā saistīt ar preces šablonu. Šādā gadījumā ar preces šablonu saistītajiem preces variantiem tiek piešķirti preces variantu numuri un nosaukumi atbilstoši nomenklatūrām.

### <a name="example"></a>Paraugs

Tiek ražoti trīs izmēru (S, M, L), četru krāsu (sarkans, zaļš, zils, dzeltens) un divu stilu (polo, V) t-krekli (TS1234). Tāpēc ir iespējami 24 preces varianti (= 3 × 4 × 2). Jūs izveidojat preces variantu numuru nomenklatūru ar tālāk norādītajiem segmentiem.

1.  Preces šablona numurs
2.  Teksta konstante: “-”
3.  krāsa
4.  Teksta konstante: “-”
5.  izmērs
6.  Teksta konstante: “-”
7.  Stils

Šādā gadījumā sarkana, maza, polo stila t-krekla preces varianta numurs ir TS1234-sarkans-mazs-polo

## <a name="nomenclature-of-constraintbased-configurations"></a>Ierobežojumiem atbilstošu konfigurāciju nomenklatūra
Ierobežojumiem atbilstošu konfigurāciju gadījumā varat izvedot īpašu nomenklatūru, kas ir paredzēta konfigurācijas preces dimensijai. Lapā **Preču nomenklatūra** varat atlasīt tālāk norādīto segmentus.

-   Numuru sērijas vērtība
-   Teksta konstante
-   Atribūta vērtība

Katram komponentam preču konfigurācijas modelī var būt sava konfigurāciju nomenklatūra. Var izmantot tikai komponenta atribūtus. Apakškomponentu vai lietotāju prasību atribūtus nevar izmantot.

### <a name="example"></a>Paraugs

Preces konfigurācijas modelim ir saknes komponents ar diviem tālāk norādītajiem atribūtiem.

-   Materiāls (plastmasa, koks, tērauds)
-   Garums (10...100)

Jūs izveidojat konfigurāciju nomenklatūru ar tālāk norādītajiem segmentiem.

1.  Atribūta vērtība: Materiāls
2.  Teksta konstante: “AAA”
3.  Atribūta vērtība: Garums

Šādā gadījumā koka materiāla, kura garums ir 78, konfigurācijas ID ir WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Dimensijām atbilstošu konfigurāciju nomenklatūra
Dimensijām atbilstošu konfigurāciju gadījumā varat izvedot īpašu nomenklatūru, kas ir paredzēta konfigurācijas preces dimensijai. Lapā **Preču nomenklatūra** varat atlasīt tālāk norādīto segmentus.

-   Numuru sērijas vērtība
-   Teksta konstante
-   Konfigurācijas grupas krājums

Varat definēt materiālu komplekta (MK) konfigurāciju nomenklatūru.

### <a name="example"></a>Paraugs

MK ir iekļautas četras MK rindas, kas ir sadalītas divās konfigurāciju grupās.

-   MK rinda: M0007, Standarta korpuss
    -   Konfigurācijas grupa: Korpuss
-   MK rinda: M0008, Augstas kvalitātes korpuss
    -   Konfigurācijas grupa: Korpuss
-   MK rinda: M0021, Auduma priekšējais režģis
    -   Konfigurācijas grupa: Priekšējais režģis
-   MK rinda: M0022, Metāla priekšējais režģis
    -   Konfigurācijas grupa: Priekšējais režģis

Jūs izveidojat konfigurāciju nomenklatūru ar tālāk norādītajiem segmentiem.

1.  Konfigurācijas grupa: Korpuss
2.  Teksta konstante: “&”
3.  Konfigurācijas grupa: Priekšējais režģis

Šādā gadījumā ar auduma priekšējo režģi aprīkota standarta korpusa konfigurācijas ID ir M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Preces variantu un konfigurāciju kombinācijas nomenklatūra
Ja preces šablona preces variantu konfigurēšanai izmantojat ierobežojumiem vai dimensijām atbilstošās konfigurācijas tehnoloģiju, preces variantu numuros var tikt ietverta konfigurācijas dimensijas nomenklatūra. Lai konfigurētu variantus, veiciet tālāk norādītās darbības.

1.  Lapā **Preču nomenklatūra** definējiet preces variantu numuru nomenklatūru, kurā ir ietverta konfigurācijas dimensija.
2.  Piešķiriet nomenklatūru preces dimensiju grupai, kurā ir ietverta konfigurācijas dimensija.
3.  Definējiet konfigurāciju nomenklatūru komponentiem vai MK, kas tiks izmantoti preces variantu konfigurēšanai.

Varat arī izveidot preču nosaukumu nomenklatūras. Preces variantu nosaukumus var konfigurēt tā, lai tajos tiktu ietverts konfigurācijas ID vai nosaukums.

### <a name="example-for-constraint-based-configurations"></a>Ierobežojumiem atbilstošu konfigurāciju piemērs

Šī piemēra ietvaros tiek izmantota preces variantu numuru nomenklatūra, kas sastāv no tālāk norādītajiem segmentiem.

1.  Preces šablona numurs
2.  Teksta konstante: “\_”
3.  Konfigurācija

Konfigurāciju nomenklatūra sastāv no tālāk norādītajiem segmentiem.

1.  Atribūta vērtība: Materiāls
2.  Teksta konstante: “AAA”
3.  Atribūta vērtība: Garums

Jūs ievadāt šādas segmentu vērtības.

-   Preces šablona numurs = **M0099**
-   Materiāls = **Plastmasa**
-   Garums = **12**

Šādā gadījumā preces varianta numurs ir M0099\_PlastmasaAAA12.

### <a name="example-for-dimension-based-configurations"></a>Dimensijām atbilstošu konfigurāciju piemērs

Šī piemēra ietvaros tiek izmantota preces variantu numuru nomenklatūra, kas sastāv no tālāk norādītajiem segmentiem.

1.  Preces šablona numurs
2.  Teksta konstante: “//”
3.  Konfigurācija

Konfigurāciju nomenklatūra sastāv no tālāk norādītajiem segmentiem.

1.  Konfigurācijas grupa: Korpuss
2.  Teksta konstante: “&”
3.  Konfigurācijas grupa: Priekšējais režģis

Jūs ievadāt šādas segmentu vērtības.

-   Preces šablona numurs = **D0123**
-   Korpuss = **M0008**
-   Priekšējais režģis = **M0022**

Šādā gadījumā preces varianta numurs ir D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numerācijas konflikti
Dažos gadījumos iestatītā preces variantu numuru nomenklatūra var nenodrošināt unikālus preces variantu numurus. Piemēram, preces variantu numuri nav unikāli, ja preces šablonam tiek izmantota iepriekš definēta variantu konfigurēšanas tehnoloģija un šī šablona nomenklatūrā nav ietverta viena aktīva preces dimensija. Konfliktu novēršanas veids ir atkarīgs no konfigurēšanas tehnoloģijas.

### <a name="predefined-variants"></a>Iepriekš definēti varianti

Ja mēģināt manuāli izveidot vai automātiski ģenerēt preces variantus un vairākiem preces variantiem tiek piešķirts viens un tas pats preces varianta numurs, rodas kļūda. Lai to nepieļautu, ir jāizmanto visas preces dimensijas grupā ietvertās aktīvās preces dimensijas. Varat arī ietvert numuru sēriju, lai palīdzētu nodrošināt, ka preces variantu numuri ir unikāli.

### <a name="constraint-based-configurations"></a>Konfigurācijas atbilstoši ierobežojumam

Atkarībā no nomenklatūras sistēma var tikt mēģināts piešķirt konfigurācijai preces varianta numuru, kas nav unikāls. Šajā gadījumā sistēmā preces varianta numura vietā tiek izmantota konfigurācijas dimensijas numuru sērija un tiek parādīts brīdinājums. Lai to nepieļautu, nomenklatūrā ir jāietver pietiekami daudz atribūtu, kas nodrošina, ka preces variantu numuri ir unikāli. Ir arī jāpārliecinās, ka komponentam ir ieslēgta opcija **Atkārtoti izmantot**.

### <a name="dimension-based-configurations"></a>Konfigurācijas atbilstoši dimensijām

Vienas konfigurācijas procesa darbības laikā sistēmā tiek ieteikta konfigurācijas vērtību atbilstoši nomenklatūrai. Šajā darbībā varat manuāli mainīt konfigurācijas vērtību. Saglabājot konfigurāciju, sistēmā tiek pārbaudīts, vai konfigurācijas vērtība ir unikāla. Ja ievadītā vērtība nav unikāla, tiek parādīts kļūdas ziņojums. Lai saglabātu konfigurāciju, ir jāievada unikāla konfigurācijas vērtība.

<a name="see-also"></a>Skatiet arī
--------

[Preces variantu nomenklatūras izveide iepriekš definētiem preces variantiem](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Preces variantu nomenklatūras izveide konfigurētiem preces variantiem](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


