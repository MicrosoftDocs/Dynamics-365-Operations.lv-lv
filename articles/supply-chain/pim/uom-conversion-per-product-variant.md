---
title: Mērvienību konvertēšana katram preces variantam
description: Šajā tēmā ir paskaidrots, kā iestatīt mērvienību pārveidošanu preču variantiem. Tajā ir ietverts iestatīšanas piemērs.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ddb6c614ede98e46e46ff284a1a16669bbaaaf66
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258051"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Mērvienību konvertēšana katram preces variantam

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt mērvienību pārveidošanu dažādiem preču variantiem.

Tā vietā, lai izveidotu vairākus atsevišķus produktus, kas jāsaglabā, varat izmantot preces variantus, lai izveidotu viena produkta variantus. Piemēram, preces variants varētu būt konkrēta izmēra un krāsas T-krekls.

Iepriekš mērvienību pārveidošanu varēja iestatīt tikai preču šablonā. Tādēļ visiem preces variantiem bija vienādi vienību pārveidošanas noteikumi. Tomēr, ja ir ieslēgta *Preces variantu mērvienību pārveidošana* funkcija, ja T-krekli tiek pārdoti kastēs un to T-kreklu skaits, ko var iepakot kastē, ir atkarīgs no T-kreklu izmēra, tagad varat iestatīt mērvienību pārveidošanu starp dažādiem krekla izmēriem un kastēm, kas tiek izmantoti iepakošanai.

## <a name="turn-on-the-feature-in-your-system"></a>Līdzekļa ieslēgšana sistēmā

Ja jūsu sistēmā šis līdzeklis nav redzams, dodieties uz [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet līdzekli *Preces variantu mērvienību pārveidošana* funkcijai.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Iestatīt preci mērvienību pārveidošanai katram variantam

Preces variantus var izveidot tikai precēm, kuras ir preču šabloni. Papildinformāciju skatiet sadaļā [Preces šablona izveide](tasks/create-product-master.md). Līdzeklis *Preces variantu mērvienību pārveidošana* nav pieejama precēm, kas iestatītas noslodzes procesiem.

Lai konfigurētu preces šablonu, lai atbalstītu mērvienību pārveidošanu katram variantam, rīkojieties šādi.

1. Dodieties uz **Preču informācijas pārvaldība \> Produkts \> Preces šabloni**.
1. Izveidojiet vai atveriet preces šablonu, lai dotos uz tā **Produkta informācijas** lapu.
1. Iestatiet opciju **Iespējot mērvienību pārveidošanu** uz *Jā*.
1. Darbību rūtī cilnē **Prece** grupā **Iestatīt**, atlasiet **Mērvienību pārveidošana**.
1. Tiek atvērta lapa **Mērvienību pārveidošana**. Atlasiet vienu no šīm cilnēm:

    - **Starpklases reklāmguvumi** – Atlasiet šo cilni, lai konvertētu no vienībām, kas pieder vienai mērvienību kategorijai.
    - **Starpklases reklāmguvumi** – atlasiet šo cilni, lai konvertētu starp vienībām, kas pieder dažādām mērvienību kategorijām.

1. Lai pievienotu jaunu pārveidi, atlasiet **Jauns**.
1. Iestatiet **Izveidot konvertēšanu šim** uz lauku uz vienu no šīm vērtībām:

    - **Prece** – atlasot šo vērtību, varat iestatīt mērvienību pārveidošanu preces šablonam. Šī mērvienību pārveidošana tiks izmantota kā atkāpšanās metode visiem preču variantiem, kam nav definēta neviena vienības pārvēršana.
    - **Preces variants** – atlasot šo vērtību, varat iestatīt mērvienību pārveidošanu konkrētam preces šablonam. Izmantojiet lauku **Preces variants**, lai atlasītu variantu.

    ![Jaunas pārveides pievienošana](media/uom-new-conversion.png "Jaunas pārveides pievienošana")

1. Izmantojiet citus laukus, kas tiek sniegti, lai iestatītu mērvienību pārveidošanu.
1. Atlasiet **Labi**, lai saglabātu jauno mērvienību pārveidošanu.

> [!TIP]
> Varat atvērt lapu **Mērvienību pārveidošana** produktam vai preces variantam no jebkuras no šīm lapām:
> 
> - Detalizēta informācija par preci
> - Informācija par izlaistajām precēm
> - Izlaistie preces varianti

## <a name="example-scenario"></a>Piemēra situācija

Šajā scenārijā uzņēmums pārdod T-kreklus šādos izmēros: mazs, vidējs, liels un īpaši liels. T-krekls ir definēts kā prece, un dažādi izmēri ir definēti kā šīs preces varianti. Krekli ir iepakoti kastēs. Izmēram mazs, vidējs un liels, katrā kastē var būt pieci krekli. Tomēr īpaši lielajam izmēram ir vieta tikai četriem krekliem katrā kastē.

Uzņēmums vēlas izsekot dažādiem T-kreklu variantiem, izmantojot mērvienību *Gabali*, bet pārdod tos, izmantojot mērvienību *Kastes*. Mazu, vidēju un lielu izmēru krājumu vienības un pārdošanas vienības pārveidošana ir 1 kaste = 5 gabali. Īpaši lielajam izmēram, pārveidošana ir 1 kaste = 4 gabali.

1. Vispirms atveriet lapu **Mērvienību pārveidošana** no lapas **Izlaistās preces detalizēta informācija** attiecīgajam **T-kreklam**.
1. Lapā **Mērvienību pārveidošana** iestatiet mērvienības pārveidošanu šādam izlaistajam preces variantam: **īpaši liels**.

    | Lauks                 | Iestatījums                 |
    |-----------------------|-------------------------|
    | Izveidot konvertēšanu šim: | Preces variants         |
    | Preces variants       | T-krekls : : Īpaši liels : : |
    | No vienības             | Kastes                   |
    | Koeficients                | 4.                       |
    | Uz vienību               | Gabali                  |

1. Izlaistajiem preces variantiem **Mazs**, **Vidējs** un **Liels** ir tāda pati mērvienību pārveidošana starp vienību *Kaste* un *Gabali*, līdz ar to šiem preces variantiem var definēt šādu mērvienību pārveidošanu preces šablonā.

    | Lauks                 | Iestatījums |
    |-----------------------|---------|
    | Izveidot konvertēšanu šim: | Prece |
    | Prece               | T-krekls |
    | No vienības             | Kastes   |
    | Koeficients                | 5.       |
    | Uz vienību               | Gabali  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Programmas Excel izmantošana, lai atjauninātu mērvienību pārveidošanu

Ja precei ir daudz preču variantu, kam ir dažādas mērvienību pārveidošanas, ir ieteicams eksportēt mērvienību pārveidošanu uz Microsoft Excel darbgrāmatu, atjaunināt tās un pēc tam tās publicēt Dynamics 365 Supply Chain Management.

Lai eksportētu mērvienību pārveidošanu uz Excel, lapā **Mērvienību pārveidošana**, kas atrodas darbību rūtī, atlasiet **Atvērt objektā Microsoft Office**.

## <a name="additional-resources"></a>Papildu resursi

[Mērvienības pārvaldība](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]