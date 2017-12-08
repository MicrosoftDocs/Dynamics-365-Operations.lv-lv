---
title: "Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma ar Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6c68c4482cacf70f003669cf335e52e47425d2f7
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Lai varētu lietot risinājumu No potenciāla klienta līdz skaidrai naudai, vispirms iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition ietverto preču tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration). Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.

Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti programmā Finance and Operations ietverto preču sinhronizēšanai ar programmu Sales.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Preces (no Fin and Ops uz Sales) — tieši
- **Uzdevuma nosaukums līdzekļa Datu integrācija projektā:** Preces

Lai varētu veikt preču sinhronizāciju, nav nepieciešams neviens sinhronizācijas uzdevums.

## <a name="entity-set"></a>Elementu kopa

| Finance and Operations     | Pārdošana    |
|----------------------------|----------|
| Pārdodamas izlaistās preces | Preces |

## <a name="entity-flow"></a>Elementu plūsma

Preces tiek pārvaldītas programmā Finance and Operations un sinhronizētas ar programmu Sales. Datu elements **Pārdodamas izlaistās preces** programmā Finance and Operations nodrošina tikai *pārdodamo* preču eksportēšanu. Pārdodamās preces ir preces, par kurām ir pieejama informācija, kas ir nepieciešama, lai tās varētu izmantot pārdošanas pasūtījumā. Tie paši noteikumi attiecas uz preces validāciju, izmantojot funkciju **Validēt** lapā **Izlaistā prece**.

Preces numurs tiek izmantots kā atslēga. Tāpēc, kad preces varianti tiek sinhronizēti ar programmu Sales, katram preces variantam ir atsevišķs preces ID.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Programmā Sales precēm ir pievienots jauns lauks **Tiek uzturēts ārēji**, lai norādītu, ka konkrētā prece tiek uzturēta ārēji. Pēc noklusējuma, veicot importēšanu programmā Sales, tiek iestatīta vērtība **Jā**. Ir pieejamas šādas vērtības:

- **Jā** — prece ir iegūta no programmas Finance and Operations, un to nevar rediģēt programmā Sales.
- **Nē** — prece ir tieši ievadīta programmā Sales.
- **(Tukšs)** — prece bija pieejama programmā Sales pirms risinājuma No potenciālā klienta līdz skaidrai naudai iespējošanas.

Lauks **Tiek uzturēts ārēji** palīdz nodrošināt, ka ar programmu Finance and Operations tiek sinhronizēti tikai piedāvājumi un pārdošanas pasūtījumi, kas ir saistīti ar ārēji uzturētām precēm.

Ārēji uzturētās preces tiek automātiski pievienotas pirmajam derīgajam cenrādim tajā pašā valūtā. Cenrāži ir sakārtoti alfabēta secībā pēc nosaukuma. Kā cena cenrādī tiek izmantota preces pārdošanas cena no programmas Finance and Operations. Tāpēc programmā Sales ir jābūt cenrādim atbilstoši katrai preču pārdošanas valūtai programmā Finance and Operations. Kā izlaisto pārdodamo preču valūta tiek iestatīta tās juridiskās personas uzskaites valūta, no kurienes šī prece ir eksportēta.

> [!NOTE]
> Preces sinhronizācija neizdosies, ja vien nebūs pieejams cenrādis atbilstošajā valūta.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

- Pirms pirmās sinhronizēšanas reizes esošajām precēm programmā Finance and Operations ir jāaizpilda tabula Atšķirīga prece. Esošās preces netiek sinhronizētas, kamēr nav pabeigts šis darbs.

    1. Programmā Finance and Operations izmantojiet lauku Meklēt, lai atrastu vienumu **Aizpildīt atšķirīgo preču tabulu**.
    2. Atlasiet **Aizpildīt atšķirīgu preču tabulu**, lai palaistu darbu. Šis darbs ir jāpalaiž tikai vienu reizi.

- Pārliecinieties, ka kartējumā no **SalesUnitSymbol** uz **DefaultUnit (nosaukums)** pastāv nepieciešamā pārdošanas mērenības (UOM) vērtību karte starp programmām Finance and Operations un Sales.
- Atjauniniet vienuma**Vienību grupa** (**defaultuomscheduleid.name**) vērtību karti atbilstoši vienumam **Vienību grupas** programmā Sales.

    Noklusējuma veidnes vērtība ir **Noklusējuma vienība**.

- Pārliecinieties, ka programmā Sales pastāv visu preču pārdošanas UOM no programmas Finance and Operations.
- Pārliecinieties, ka programmā Sales pastāv cenrāži katrā preču pārdošanas valūtā no programmas Finance and Operations.
- Kad programmā Sales tiek izveidotas preces, to statuss var būt **Melnraksts** vai **Aktīva**. Šī darbība tiek kontrolēta programmas Sales sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana**.

    Preces, kam izveides brīdī ir statuss **Melnraksts**, ir jāaktivizē, pirms tās var pievienot piedāvājumiem vai pārdošanas pasūtījumiem.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes kartēšanai līdzeklī Datu integrācija. 

> [!NOTE]
> Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.

![Veidnes kartējums datu integrētājā](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)

[Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations](accounts-template-mapping-direct.md)

[Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations](contacts-template-mapping-direct.md)

[Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-order-template-mapping-direct.md)

[Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-invoice-template-mapping-direct.md)



