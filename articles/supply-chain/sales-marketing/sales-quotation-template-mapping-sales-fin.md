---
title: "Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Finance and Operations"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales pieejamo pārdošanas piedāvājumu galveņu un rindu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.contentlocale: lv-lv
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Finance and Operations

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales pieejamo pārdošanas piedāvājumu galveņu un rindu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Lai varētu lietot risinājumu No potenciāla klienta līdz skaidrai naudai, vispirms izlasiet rakstu [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Veidne un uzdevumi

Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas piedāvājumi (no Sales uz Fin and Ops) — tieši
- **Uzdevumu nosaukumi datu integrācijas projektā**

    - QuoteHeader
    - QuoteLine

Pirms pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanas ir jāveic tālāk norādītie sinhronizācijas uzdevumi.

- Preces (no Fin and Ops uz Sales) — tieši
- Konti (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)
- Kontaktpersonas kā debitori (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)

## <a name="entity-set"></a>Elementu kopa

| Pārdošana        | Finance and Operations     |
|--------------|----------------------------|
| Citāti       | CDS pārdošanas piedāvājuma galvene |
| QuoteDetails | CDS pārdošanas piedāvājuma rindas  |

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas piedāvājumi tiek izveidoti programmā Sales un sinhronizēti ar Finance and Operations.

Pārdošanas piedāvājumi no Sales tiek sinhronizēti tikai tad, ja ir izpildīti tālāk norādītie nosacījumi.

- Visas pārdošanas piedāvājumā ietvertās piedāvātās preces ir ārēji uzturētas.
- Pēc noklikšķināšanas uz **Aktivizēt piedāvājumu** pārdošanas piedāvājums ir aktīvs.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Elementam **Piedāvājums** ir pievienots lauks **Ir tikai ārēji uzturētas preces**, lai pastāvīgi izsekotu to, vai pārdošanas piedāvājumā ir ietvertas tikai ārēji uzturētas preces. Ja pārdošanas piedāvājumā ir tikai ārēji uzturētas preces, tās tiek uzturētas programmā Finance and Operations. Šī darbība palīdz nodrošināt to, ka nemēģināt sinhronizēt pārdošanas piedāvājuma rindas, kurās ietvertās preces nav zināmas programmā Finance and Operations.

Visas pārdošanas piedāvājumā ietvertās piedāvātās preces tiek atjauninātas, izmantojot lauka**Ir tikai ārēji uzturētas preces** informāciju no pārdošanas piedāvājuma galvenes. Šī informācija ir ietverta elementa **QuoteDetails** laukā **Piedāvājumā ir tikai ārēji uzturētas preces**.

Piedāvātajai precei var pievieno atlaidi, kas tiek sinhronizēta ar programmu Finance and Operations. Galvenes lauki **Atlaide**, **Maksas** un **Nodokļi** tiek kontrolēti, izmantojot iestatījumus programmā Finance and Operations. Pašlaik šie iestatījumi neatbalsta integrācijas kartēšanu. Pašlaik lauki **Cena**, **Atlaide**, **Maksa** un **Nodokļi** tiek uzturēti un apstrādāti programmā Finance and Operations.

Programmā Sales risinājums tālāk norādītos laukus pārveido par tikai lasāmiem, jo attiecīgās vērtības netiek sinhronizētas ar programmu Finance and Operations.

- Tikai lasāmie lauki pārdošanas piedāvājuma galvenē: **Atlaide %**, **Atlaide** un **Vedmaksa**
- Tikai lasāmie piedāvāto produktu lauki: **Nodoklis**

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms pārdošanas piedāvājuma sinhronizēšanas ir svarīgi atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

- Pārliecinieties, ka darba grupai, kurai ir piešķirts ar Sales savienojumu kopu saistītais lietotājs, ir iestatītas vajadzīgās atļaujas. Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuves atļauja, bet darba grupai nav administratora piekļuves atļaujas. Ja darba grupai nav administratora piekļuves atļaujas, palaižot projektu līdzeklī Datu integrācija, saņemat kļūdas ziņojumu par to, ka trūkst galvenās darba grupas.

    Lai iestatītu darba grupas atļaujas, pārejiet uz sadaļu **Iestatījumi** &gt; **Drošība** &gt; **Darba grupas** un atlasiet attiecīgo darba grupu. Atlasiet **Pārvaldīt lomas** un pēc tam atlasiet lomu, kurai ir piešķirtas vajadzīgās atļaujas, piemēram, **Sistēmas administrators**.

- Pārejiet uz sadaļu **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.

    - Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.
    - Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

### <a name="setup-in-the-data-integration-project"></a>Iestatīšana datu integrācijas projektā

#### <a name="quoteheader"></a>QuoteHeader

- Pārliecinieties, ka pastāv nepieciešamais kartējums no **Shipto\_country** uz **DeliveryAddressCountryRegionISOCode**. Vērtību kartē varat definēt noklusējuma vērtību, kas tiek izmantota, ja ir atstāta tukša vērtība. Vienkārši atstājiet kreiso pusi tukšu un labajā pusē iestatiet vajadzīgo valsti vai reģionu. Tādējādi jums nav jāievada valsts vai reģions iekšzemes pasūtījumos.

    Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni un kur tukšai vērtībai atbilst vērtība **ASV**.

#### <a name="quoteline"></a>QuoteLine

- Pārliecinieties, ka programmā Finance and Operations pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.
- Pārliecinieties, ka programmā Sales ir definētas nepieciešamās vienības.

    Kartējumam no **oumid.name** uz **SalesUnitSymbol** ir definēta veidnes vērtība ar vērtību karti.

- Pēc izvēles varat pievienot tālāk norādītos kartējumus, lai palīdzētu nodrošināt pārdošanas piedāvājuma rindu importēšanu programmā Finance and Operations gadījumos, ja nav pieejama debitora vai preces noklusējuma informācija.

    - **SiteId** — vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas. Laukam **SiteId** nav noklusējuma veidnes vērtības.
    - **WarehouseId** — noliktava ir jānorāda, lai programmā Finance and Operations apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas. Laukam **WarehouseId** nav noklusējuma veidnes vērtības.

## <a name="template-mapping-in-data-integrator"></a>Veidnes kartēšana datu integrētājā

> [!NOTE]
> - Laukus **Atlaide**, **Maksas** un **Nodokļi** kontrolē kompleksi iestatījumi programmā Finance and Operations. Pašlaik šie iestatījumi neatbalsta integrācijas kartēšanu. Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** apstrādā programma Finance and Operations.
> - Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.

### <a name="quoteheader"></a>QuoteHeader

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)


