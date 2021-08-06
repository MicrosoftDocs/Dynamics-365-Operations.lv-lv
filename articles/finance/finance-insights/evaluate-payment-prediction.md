---
title: Sākotnējā debitora maksājuma prognozēšanas modeļa izvērtēšana (priekšskatījums)
description: Šajā tēmā aprakstītas darbības, ko varat veikt, lai izprastu debitoru maksājumu prognozēšanas modeli un novērtētu tā efektivitāti.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 97228a68d9eaa02388675238d5a196b4af30daa5
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638564"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Sākotnējā debitora maksājuma prognozēšanas modeļa izvērtēšana (priekšskatījums)

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā novērtēt prognozēšanas modeli pēc finanšu ieskatu ieslēgšanas un pēc tam ģenerēt un apmācīt savu pirmo modeli. Šī tēma pievēršas modeļiem, kas paredzēti debitoru maksājumu prognozēšanai. Tajā aprakstītas darbības, ko varat veikt, lai izprastu debitoru maksājumu prognozēšanas modeli un novērtētu tā efektivitāti.

## <a name="getting-details-about-the-model"></a>Informācijas iegūšana par modeli

Lapā **Finanšu ieskatu parametri** pakalpojumā Microsoft Dynamics 365 Finance blakus precizitātes rezultātam ir redzama saite **Modeļa precizitātes uzlabošana**.

[![Modeļa precizitātes uzlabošanas saite.](./media/prediction-model.png)](./media/prediction-model.png)

Šī saite aizved jūs uz AI Builder, kur varat uzzināt vairāk par pašreizējo modeli, kā arī veikt darbības, lai to uzlabotu. Tālāk atrodamajā attēlā ir redzams atvērta lapa.

[![AI Builder.](./media/what-to-predict.png)](./media/what-to-predict.png)

Atvērtajā lapā ir redzama tālāk minētā informācija.

- Sadaļā **Veiktspēja** modeļa veiktspējas pakāpe sniedz skatījumu uz modeļa kvalitāti. Plašāku informāciju par šo pakāpi skatiet sadaļā [Prognozēšanas modeļa veiktspēja](/ai-builder/prediction-performance), kas atrodama AI Builder dokumentācijā.
- Sadaļā **Visietekmīgākie dati** parādīts, cik svarīgi jūsu modelim bija dažādi datu ievades tipi. Varat novērtēt šo sarakstu un atbilstošos procentus, lai noteiktu, vai informācija atbilst tam, ko zināt par savu uzņēmumu un tirgu.

    [![Prognozēšanas modeļa sadaļas Veiktspēja un Visietekmīgākie dati.](./media/models.png)](./media/models.png)

- Sadaļā **Veiktspēja** atlasiet **Skatīt papildinformāciju,**, lai uzzinātu vairāk par pakāpi un citiem apsvērumiem. Šajā attēlā informācija rāda, ka modelis izmanto mazāk informācijas nekā ieteicams. Tāpēc sistēma ir ģenerējusi brīdinājuma ziņojumu.

    [![Brīdinājumi par modeļa veiktspēju.](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Detalizētāka izpēte

Kaut arī precizitāte ir labs sākumpunkts, lai novērtētu modeli, un veiktspējas pakāpe nodrošina perspektīvu, AI Builder nodrošina detalizētāku metriku, ko varat izmantot novērtējumam. Lai lejupielādētu detalizētu informāciju, sadaļā **Veiktspēja** atlasiet daudzpunktes pogu (**...**) blakus pogai **Izmantot modeli** un pēc tam atlasiet **Lejupielādēt detalizētu metriku**.

[![Komanda Lejupielādēt detalizētu metriku.](./media/performance.png)](./media/performance.png)

Tālāk atrodamajā attēlā redzams formāts, kādā varat lejupielādēt datus.

[![Lejupielādēto datu formāts.](./media/data-format.png)](./media/data-format.png)

Lai iegūtu detalizētāku rezultātu analīzi, ir labs sākumpunkts, lai pārskatītu metriku Neskaidrību matrica. Piemēram, šeit ir dati, kas tiek rādīti šim rādītājam iepriekšējā attēlā.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Šos datus var izvērst, kā norādīts tālāk.

| &nbsp;                   | Prognozēts laikā | Prognozēts vēlu | Prognozēts ļoti vēlu |
|--------------------------|-------------------|----------------|---------------------|
| Faktiskais laiks maksājumam   | **71**            | 0              | 21                  |
| Faktiskais nokavētais maksājums      | 5                 | **0**          | 27                  |
| Faktiskais ļoti nokavētais maksājums | 2                 | 0              | **45**              |

Neskaidrību matrica parāda no mācību procesa nejauši izvēlēta testa datu komplekta rezultātus. Tā kā šie slēgtie rēķini netika izmantoti modeļa apmācīšanai, tie ir labi testa gadījumi modelim. Tā kā ir zināms rēķina faktiskais stāvoklis, var redzēt arī modeļa veiktspēju.

Vispirms ir jāmeklē visizplatītākā faktiskā vērtība. Kaut arī šī vērtība var nebūt precīzi saskaņota ar vispārējo datu kopu, tas ir saprātīgs aptuvens skaitlis. Šādā gadījumā **Faktiskais laika maksājums** notiek par 92 no 171 rēķiniem, un tā ir visizplatītākā faktiskā vērtība. Tāpēc tas ir labs pamats jūsu modelim. Ja jūs minējāt, ka visi rēķini būtu savlaicīgi, jums būtu taisnība 92 no 171 reizēm (proti, 54 procenti).

Jums ir svarīgi saprast, cik sabalansēta ir datu kopa. Šajā gadījumā 92 rēķini 171 tika apmaksāti savlaicīgi, 32 tika apmaksāti novēloti, un 47 tika apmaksāti ļoti novēloti. Šīs vērtības norāda samērā līdzsvarotu datu kopu, jo katrā klasifikācijā ir netriviāli rezultāti. Situācija, kad vienai no valstīm ir ļoti maz rezultātu, algoritmiskās mācīšanās modelim var būt sarežģīta.

Modeļa precizitāti norāda testa datu kopas pareizo prognožu skaits. Šīs pareizās prognozes ir vērtības, kas iepriekšējā piemērā redzamas treknrakstā. Šādā gadījumā vērtības veido aprēķināto precizitāti 67,8 procenti (= \[71 + 0 + 45\] ÷ 171). Šī vērtība parāda 14 procentu uzlabojumu virs bāzlīnijas minējuma (54 procenti) un ir viens no modeļa kvalitātes rādītājiem.

Ja jūs rūpīgāk aplūkosiet neskaidrību matricu, jūs ievērosiet, ka modelis spēj labi prognozēt laicīgus un ļoti novēlotus rēķinu maksājumus. Tomēr tas nepareizi prognozēja visus 32 rēķinus, kas faktiski apmaksāti ar novēlošanos (bet ne ar lielu novēlošanos). Šis rezultāts liecina, ka modelim nepieciešama papildu izpēte un uzlabošana.

Skaitlis, kas attēlo modeļa veiktspēju labāk nekā precizitāti, ir F1 makro rezultāts. Šis rezultāts ņem vērā visu klasifikācijas stāvokļu (laicīgs, novēlots un ļoti novēlots) rezultātus. Piemēram, šeit ir dati, kas tiek rādīti rādītājam F1 makro iepriekšējā attēlā.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

Šādā gadījumā F1 makro rezultāts ir aptuveni 49,3 procenti, kas norāda, ka modelis nenodrošina efektīvas prognozes visiem stāvokļiem, neskatoties uz vispārējo precizitātes rādītāju, kas šķiet samērā augsts.

## <a name="improving-the-model"></a>Modeļa uzlabošana

Kad esat izpratis pirmā modeļa rezultātus, iespējams, vēlēsities uzlabot modeli, pievienojot vai noņemot funkciju kolonnas, vai filtrējot jebkuru datu kopas daļu, kas neatbalsta precīzas prognozes. Aizveriet AI Builder un tad izmantojiet saiti **Modeļa uzlabošana** pakalpojumā Dynamics 365 Finance, lai restartētu AI Builder procesu. Varat eksperimentēt ar dažādiem raksturlielumiem, neietekmējot publicēto modeli. Publicētais modelis tiek ietekmēts tikai tad, kad atlasāt **Publicēt**. Atcerieties, ka jūsu Dynamics 365 Finance instancei tiek izmantots viens modelis. Tāpēc rūpīgi pārskatiet jebkuru jauno modeli, pirms to publicējat.

## <a name="for-more-information"></a>Plašāka informācija

Papildinformāciju par to, kā izvērtēt prognozēšanas modeļus skatiet sadaļā [Algoritmiskās mācīšanās modeļu rezultāti](/confusion-matrix.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
