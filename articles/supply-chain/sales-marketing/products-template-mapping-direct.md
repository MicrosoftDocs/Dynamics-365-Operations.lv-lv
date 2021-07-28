---
title: Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Sales
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar programmu Dynamics 365 Sales.
author: ChristianRytt
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 613fd4bad93e28360ca6862b7b30b2e4356ca489
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353400"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Sales

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Pirms risinājuma No potenciāla klienta līdz skaidrai naudai lietošanas izlasiet rakstu [Datu integrēšana pakalpojumā Microsoft Dataverse programmām](/powerapps/administrator/data-integrator).

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču tiešai sinhronizēšanai ar programmu Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [Power Apps administrēšanas centru](https://admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti programmā Supply Chain Management ietverto preču sinhronizēšanai ar programmu Sales.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Preces (no Supply Chain Management uz Sales) — tieši
- **Uzdevuma nosaukums līdzekļa Datu integrācija projektā:** Preces

Lai varētu veikt preču sinhronizāciju, nav nepieciešams neviens sinhronizācijas uzdevums.

## <a name="entity-set"></a>Entītiju kopa

| Supply Chain Management    | Pārdošana    |
|----------------------------|----------|
| Pārdodamas izlaistās preces | Preces |

## <a name="entity-flow"></a>Entītiju plūsma

Preces tiek pārvaldītas programmā Supply Chain Management un tiek sinhronizēti ar programmu Sales. Datu elements **Pārdodamas izlaistās preces** programmā Supply Chain Management nodrošina tikai *pārdodamo* preču eksportēšanu. Pārdodamās preces ir preces, par kurām ir pieejama informācija, kas ir nepieciešama, lai tās varētu izmantot pārdošanas pasūtījumā. Tie paši noteikumi attiecas uz preces validāciju, izmantojot funkciju **Validēt** lapā **Izlaistā prece**.

Preces numurs tiek izmantots kā atslēga. Tāpēc, kad preces varianti tiek sinhronizēti ar programmu Sales, katram preces variantam ir atsevišķs preces ID.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Programmā Sales precēm ir pievienots jauns lauks **Tiek uzturēts ārēji**, lai norādītu, ka konkrētā prece tiek uzturēta ārēji. Pēc noklusējuma, veicot importēšanu programmā Sales, tiek iestatīta vērtība **Jā**. Ir pieejamas šādas vērtības:

- **Jā**— prece ir iegūta no programmas Supply Chain Management, un to nevar rediģēt programmā Sales.
- **Nē** – prece ir tieši ievadīta programmā Sales.
- **(Tukšs)** – prece bija pieejama programmā Sales pirms risinājuma No potenciālā klienta līdz skaidrai naudai iespējošanas.

Lauks **Tiek uzturēts ārēji** palīdz nodrošināt, ka ar programmu Supply Chain Management tiek sinhronizēti tikai piedāvājumi un pārdošanas pasūtījumi, kas ir saistīti ar ārēji uzturētām precēm.

Ārēji uzturētās preces tiek automātiski pievienotas pirmajam derīgajam cenrādim tajā pašā valūtā. Cenrāži ir sakārtoti alfabēta secībā pēc nosaukuma. Kā cena cenrādī tiek izmantota preces pārdošanas cena no programmas Supply Chain Management. Tāpēc programmā Sales ir jābūt cenrādim atbilstoši katrai preču pārdošanas valūtai programmā Supply Chain Management. Kā izlaisto pārdodamo preču valūta tiek iestatīta tās juridiskās personas uzskaites valūta, no kurienes šī prece ir eksportēta.

> [!NOTE]
> - Preces sinhronizācija neizdosies, ja vien nebūs pieejams cenrādis atbilstošajā valūta.
> - Varat kontrolēt izmantoto cenrādi ar integrāciju, datu integrācijas projektā kartējot elementu pricelevelid.name [noklusējuma cenrādis (nosaukums)]. Ievadē jāizmanto tikai mazie burti. Piemēram, modulī Pārdošana cenrāža ar nosaukumu “Standarta” noklusējuma vērtība būtu šāda: mērķa lauks: pricelevelid.name [Noklusējuma cenrādis (nosaukums)] un kartes veids: [ { "transformType": "Default", "defaultValue": "standarta" } ].

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

- Pirms pirmās sinhronizēšanas reizes esošajām precēm programmā Supply Chain Management ir jāaizpilda tabula Atšķirīga prece. Esošās preces netiek sinhronizētas, kamēr nav pabeigts šis darbs.

    1. Programmā Supply Chain Management izmantojiet lauku Meklēt, lai atrastu vienumu **Aizpildīt atšķirīgo preču tabulu**.
    2. Atlasiet **Aizpildīt atšķirīgu preču tabulu**, lai palaistu darbu. Šis darbs ir jāpalaiž tikai vienu reizi.

- Pārliecinieties, ka kartējumā no **SalesUnitSymbol** uz **DefaultUnit (nosaukums)** pastāv nepieciešamā pārdošanas mērenības (UOM) vērtību karte starp programmām Supply Chain Management un Sales.
- Atjauniniet vienuma **Vienību grupa** (**defaultuomscheduleid.name**) vērtību karti atbilstoši vienumam **Vienību grupas** programmā Sales.

    Noklusējuma veidnes vērtība ir **Noklusējuma vienība**.

- Pārliecinieties, ka programmā Sales pastāv visu preču pārdošanas UOM no programmas Supply Chain Management.
- Pārliecinieties, ka programmā Sales pastāv cenrāži katrā preču pārdošanas valūtā no programmas Supply Chain Management.
- Kad programmā Sales tiek izveidotas preces, to statuss var būt **Melnraksts** vai **Aktīva**. Šī darbība tiek kontrolēta programmas Sales sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana**.

    Preces, kam izveides brīdī ir statuss **Melnraksts**, ir jāaktivizē, pirms tās var pievienot piedāvājumiem vai pārdošanas pasūtījumiem.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes kartēšanai līdzeklī Datu integrācija. 

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Supply Chain Management.

![Veidnes kartēšana datu integrētājā.](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

[Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management](accounts-template-mapping-direct.md)

[Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai klientiem programmā Supply Chain Management](contacts-template-mapping-direct.md)

[Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]