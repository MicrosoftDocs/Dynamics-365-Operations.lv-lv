---
title: "Produkta numurs nomenklatūrā"
description: "Šajā tēmā aprakstīts, kā iestatīt numuru produktu nomenklatūra nomainīt fiksētā formātā [produkta kapteinis numuru - konfigurācija - Size - Color - stilu], ar mērķtiecīgu formātu, ko ietver produkta galveno numuru, aktīvā izstrādājuma izmēri un teksta norobežotājus, kas savu izvēli. Varat arī izveidot nomenklatūru, lai identificētu konfigurācijas, kuras izveidojis ierobežojumiem atbilstošais preču konfigurators. Šajās nomenklatūrās var būt jūsu izvēlētie atribūti."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Produkta numurs nomenklatūrā

Šajā tēmā aprakstīts, kā iestatīt numuru produktu nomenklatūra nomainīt fiksētā formātā [produkta kapteinis numuru - konfigurācija - Size - Color - stilu], ar mērķtiecīgu formātu, ko ietver produkta galveno numuru, aktīvā izstrādājuma izmēri un teksta norobežotājus, kas savu izvēli. Varat arī izveidot nomenklatūru, lai identificētu konfigurācijas, kuras izveidojis ierobežojumiem atbilstošais preču konfigurators. Šajās nomenklatūrās var būt jūsu izvēlētie atribūti.

Jaunā produkta varianta numuru nomenklatūra ļauj iekļaut segmentus produkta varianta identifikatoros. Šie segmenti var būt preces šablona numurs, preces dimensijas, numuru sērijas, teksta konstantes un atribūti. Šī funkcija ļauj ātri atrast noteiktu produkta variantu, veidojot pārdošanas pasūtījumu vai pirkšanas pasūtījumu.

## <a name="nomenclature-of-predefined-product-variants"></a>Iepriekš definētu preces variantu nomenklatūra
Preces varianti tiek ģenerēti preces šabloniem saskaņā ar vienu no trim konfigurācijas tehnoloģijām:

-   Iepriekš definēti varianti
-   Atbilstoši ierobežojumam
-   Atbilstoši dimensijai

Katram preces variantam ir numurs, un preces variantu identifikācijas nomenklatūra ļauj atlasīt segmentus, kas tiks iekļauti katrā preces varianta numurā. Var atlasīt šādus segmentus lapā **Preču nomenklatūra**.

-   Preces šablona numurs
-   Numuru sērijas vērtība
-   Teksta konstante
-   Preces dimensijas
    -   Konfigurācija
    -   krāsa
    -   izmērs
    -   Stils

Pēc tam, kad ir definēta preces variantu identifikācijas nomenklatūra, to var saistīt ar preces dimensiju grupu. Tādējādi visiem preces šabloniem, kuros ir atsauce uz šo preces dimensiju grupu, tiks piešķirti preces varianta numuri saskaņā ar nomenklatūru. Iespējams arī piešķirt preces variantu identifikācijas nomenklatūru tieši preces šablonam; šādā gadījumā preces variantiem, kuri pieder šim šablonam, tiks piešķirti preces varianta numuri atbilstoši nomenklatūrai.

### <a name="example"></a>Paraugs

T-krekli (TS1234) tiek ražoti 3 dažādos izmēros (S, M, L), 4 dažādās krāsās (sarkana, zaļa, zila, dzeltena) un 2 stilos (polo, ar V-veida kakla izgriezumu), līdz ar to kopā ir iespējami 24 preces varianti. Preces variantu identifikācijas nomenklatūra tiek veidota ar šādiem segmentiem:

1.  Preces šablona numurs
2.  Teksta konstante: '-'
3.  krāsa
4.  Teksta konstante: '-'
5.  izmērs
6.  Teksta konstante: '-'
7.  Stils

Preces varianta numurs sarkanam, maza izmēra polo kreklam ir: TS1234 Sarkans-Mazs-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Nomenklatūru, constraintbased sastāvi
Ierobežojuma pamatā konfigurācijām, speciāla nomenklatūras var būvēt par konfigurācijas dimensija produkts. Var atlasīt šādus segmentus lapā **Preču nomenklatūra**.

-   Numuru sērijas vērtība
-   Teksta konstante
-   Atribūta vērtība 

Katram komponentam preču konfigurācijas modelī var būt sava konfigurāciju nomenklatūra. Var izmantot tikai komponentam piederošos atribūtus. Atribūti no apakškomponentiem vai lietotāju prasībām nav pieejami.

### <a name="example"></a>Paraugs

Preces konfigurācijas modelim ir saknes komponents ar diviem atribūtiem.

-   Materiāls (plastmasa, koks, tērauds)
-   Garums (10...100)

Konfigurāciju nomenklatūra tiek definēta, izmantojot šādus segmentus:

1.  Atribūta vērtība: Materiāls
2.  Teksta konstante: 'AAA'
3.  Atribūta vērtība: Garums

Piemēram, koksnes materiālam ar garumu 78 tiks izveidots šāds konfigurācijas ID: KoksAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Nomenklatūru, dimensionbased sastāvi
Konfigurācijas dimensiju, pamatojoties speciāla nomenklatūras var būvēt par konfigurācijas dimensija produkts. Var atlasīt šādus segmentus lapā **Preču nomenklatūra**.

-   Numuru sērijas vērtība
-   Teksta konstante
-   Konfigurācijas grupas krājums

Konfigurāciju nomenklatūru var definēt materiālu komplektam (MK).

### <a name="example"></a>Paraugs

Materiālu komplektam ir 4 MK rindas, kas sadalītas 2 konfigurācijas grupās.

-   MK rinda: M0007, Standarta korpuss
    -   Konfigurācijas grupa: Korpuss
-   MK rinda: M0008, Augstas kvalitātes korpuss
    -   Konfigurācijas grupa: Korpuss
-   MK rinda: M0021, Auduma priekšējais režģis
    -   Konfigurācijas grupa: Priekšējais režģis
-   MK rinda: M0022, Metāla priekšējais režģis
    -   Konfigurācijas grupa: Priekšējais režģis

Konfigurāciju nomenklatūra tiek definēta, izmantojot šādus segmentus:

1.  Konfigurācijas grupa: Korpuss
2.  Teksta konstante: '&'
3.  Konfigurācijas grupa: Priekšējais režģis

Konfigurācijas ID standarta korpusam ar auduma priekšējo režģi būs: M0007&M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Preces variantu un konfigurāciju kombinācijas nomenklatūra
Izmantojot konfigurācijas atbilstoši ierobežojumam vai konfigurācijas atbilstoši dimensijām tehnoloģiju, lai konfigurētu preces variantus preces šablonam, produkta variantiem var piešķirt preces varianta numurus, kuros ietilpst nomenklatūra no konfigurācijas dimensijas. Veiciet šīs darbības, lai konfigurētu variantus:

1.  Definējiet preces varianta numuru nomenklatūru, kurā ietilpst konfigurācijas dimensija, lapā **Preces nomenklatūra**.
2.  Piešķiriet šo nomenklatūru preces dimensiju grupai ar konfigurācijas dimensiju.
3.  Definējiet konfigurāciju nomenklatūru komponentiem vai MK, kas tiks izmantoti produkta variantu konfigurēšanai.

### <a name="example-for-constraint-based-configurations"></a>Ierobežojumiem atbilstošu konfigurāciju piemērs

Šajā piemērā var izmantot produkta varianta numuru nomenklatūru, kas sastāv no šādiem segmentiem:

1.  Preces šablona numurs
2.  Konstantu tekstu '\_'
3.  Konfigurācija

Konfigurāciju nomenklatūra var sastāvēt no šādiem segmentiem:

1.  Atribūta vērtība: Materiāls
2.  Teksta konstante: 'AAA'
3.  Atribūta vērtība: Garums

Segmentiem var ievadīt šādas vērtības:

-   Preces šablona numurs = M0099
-   Materiāls = Plastmasa
-   Garums = 12

Preces varianta numurs kļūs: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Dimensijām atbilstošu konfigurāciju piemērs

Šajā piemērā var izmantot produkta varianta numuru nomenklatūru, kas sastāv no šādiem segmentiem:

1.  Preces šablona numurs
2.  Teksta konstante '//'
3.  Konfigurācija

Konfigurāciju nomenklatūra var sastāvēt no šādiem segmentiem:

1.  Konfigurācijas grupa: Korpuss
2.  Teksta konstante: '&'
3.  Konfigurācijas grupa: Priekšējais režģis

Segmentiem var ievadīt šādas vērtības:

-   Preces šablona numurs = D0123
-   Korpuss = M0008
-   Priekšējais režģis = M0022

Preces varianta numurs kļūs: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numerācijas konflikti
Ir iespējams iestatīt preces varianta numuru nomenklatūru, kas neizveido unikālus preces varianta numurus. Piemēram, tas var notikt, ja viena aktīva preces dimensija nav iekļauta nomenklatūrā preces šablonam, kas izmanto iepriekš definētu varianta konfigurācijas tehnoloģiju. Konflikti tiek apstrādāti dažādi atšķirīgām konfigurācijas tehnoloģijām.

### <a name="predefined-variants"></a>Iepriekš definēti varianti

Mēģinot manuāli vai automātiski ģenerēt preces variantus, ja viens vai vairāki varianti beidzas ar tādu pašu preces varianta numuru, radīsies kļūda. Lai no tā izvairītos, jāizmanto visas aktīvās preces dimensijas preces dimensiju grupā vai jāiekļauj numuru sērija, lai nodrošinātu, ka preces varianta numuri ir unikāli.

### <a name="constraint-based-configurations"></a>Konfigurācijas atbilstoši ierobežojumam

Atkarībā no nomenklatūras sistēma var mēģināt piešķirt konfigurācijai preces varianta numurus, kas nav unikāli. Šajā gadījumā sistēma izmanto numuru sērijas konfigurācijas dimensijas kā preces varianta numurs vietā. Ja tā notiek, jūs saņemsit brīdinājumu. Lai no tā izvairītos, iekļaujiet nomenklatūrā pietiekami daudz atribūtu, lai nodrošinātu unikalitāti, un pārliecinieties, ka komponentam ir ieslēgta opcija **Izmantot atkārtoti**.

### <a name="dimension-based-configurations"></a>Konfigurācijas atbilstoši dimensijām

Konfigurācijas procesā ietilpst darbība, kurā sistēma piedāvā konfigurācijas vērtību saskaņā ar nomenklatūru. Šajā darbībā varat manuāli mainīt konfigurācijas vērtību. Saglabājot konfigurāciju, sistēma pārbaudīs, vai konfigurācijas vērtība ir unikāla. Ja tā nav, tiks parādīts kļūdas ziņojums. Lai saglabātu konfigurāciju, ir jāievada unikāla konfigurācijas vērtība.



<a name="see-also"></a>Skatiet arī
--------

[Izveidot produktu numuru nomenklatūras iepriekš definēto produktu variantiem (uzdevuma norādījumi)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Izveidot produktu numuru nomenklatūras konfigurēto izstrādājuma variantu (uzdevuma norādījumi)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)


