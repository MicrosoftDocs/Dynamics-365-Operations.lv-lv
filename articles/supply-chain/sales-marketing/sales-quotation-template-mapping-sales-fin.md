---
title: Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Supply Chain Management
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto pārdošanas piedāvājumu galvu un rindu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
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
ms.openlocfilehash: 848464cbc62623502b9b87b9b41dcc17150e85ba
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839009"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto pārdošanas piedāvājumu galvu un rindu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.

> [!NOTE]
> Pirms risinājuma No potenciāla klienta līdz skaidrai naudai lietošanas izlasiet rakstu [Datu integrēšana pakalpojumā Microsoft Dataverse programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs. Risinājuma ´No potenciālā klienta līdz skaidrai naudai´ veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales. Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.

[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Veidne un uzdevumi

Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu sinhronizēšanai ar programmu Supply Chain Management tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas piedāvājumi (no Sales uz Supply Chain Management) — tieši
- **Uzdevumu nosaukumi datu integrācijas projektā**

    - QuoteHeader
    - QuoteLine

Pirms pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanas ir jāveic tālāk norādītie sinhronizācijas uzdevumi.

- Preces (no Supply Chain Management uz Sales) – Tiešā
- Konti (no Sales uz Supply Chain Management) - Tiešā (ja izmantots)
- Kontaktpersonas Klientiem (no Sales uz Supply Chain Management) — Tiešā (ja izmantots)

## <a name="entity-set"></a>Elementu kopa

| Pārdošana        | Supply Chain Management     |
|--------------|----------------------------|
| Citāti       | Dataverse Pārdošanas piedāvājuma virsraksts |
| QuoteDetails | Dataverse Pārdošanas piedāvājuma rindas  |

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas piedāvājumi tiek izveidoti programmā Sales un sinhronizēti ar Supply Chain Management.

Pārdošanas piedāvājumi no Sales tiek sinhronizēti tikai tad, ja ir izpildīti tālāk norādītie nosacījumi.

- Visas pārdošanas piedāvājumā ietvertās piedāvātās preces ir ārēji uzturētas.
- Pēc noklikšķināšanas uz **Aktivizēt piedāvājumu** pārdošanas piedāvājums ir aktīvs.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Elementam **Piedāvājums** ir pievienots lauks **Ir tikai ārēji uzturētas preces**, lai pastāvīgi izsekotu to, vai pārdošanas piedāvājumā ir ietvertas tikai ārēji uzturētas preces. Ja pārdošanas piedāvājumā ir tikai ārēji uzturētas preces, tās tiek uzturētas programmā Supply Chain Management. Šī darbība palīdz nodrošināt to, ka nemēģināt sinhronizēt pārdošanas piedāvājuma rindas, kurās ietvertās preces nav zināmas programmā Supply Chain Management.

Visas pārdošanas piedāvājumā ietvertās piedāvātās preces tiek atjauninātas, izmantojot lauka **Ir tikai ārēji uzturētas preces** informāciju no pārdošanas piedāvājuma galvenes. Šī informācija ir ietverta elementa **QuoteDetails** laukā **Piedāvājumā ir tikai ārēji uzturētas preces**.

Piedāvātajai precei var pievieno atlaidi, kas tiek sinhronizēta ar programmu Supply Chain Management. Galvenes lauki **Atlaide**, **Maksas** un **Nodokļi** tiek kontrolēti, izmantojot iestatījumus programmā Supply Chain Management. Pašlaik šie iestatījumi neatbalsta integrācijas kartēšanu. Pašlaik lauki **Cena**, **Atlaide**, **Maksa** un **Nodokļi** tiek uzturēti un apstrādāti programmā Supply Chain Management.

Programmā Sales risinājums tālāk norādītos laukus pārveido par tikai lasāmiem, jo attiecīgās vērtības netiek sinhronizētas ar programmu Supply Chain Management.

- Tikai lasāmie lauki pārdošanas piedāvājuma galvenē: **Atlaide %**, **Atlaide** un **Vedmaksa**
- Tikai lasāmie piedāvāto produktu lauki: **Nodoklis**

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms pārdošanas piedāvājuma sinhronizēšanas ir svarīgi atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

- Pārliecinieties, ka darba grupai, kurai ir piešķirts ar Sales savienojumu kopu saistītais lietotājs, ir iestatītas vajadzīgās atļaujas. Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuves atļauja, bet darba grupai nav administratora piekļuves atļaujas. Ja darba grupai nav administratora piekļuves atļaujas, palaižot projektu līdzeklī Datu integrācija, saņemat kļūdas ziņojumu par to, ka trūkst galvenās darba grupas.

    Lai iestatītu darba grupas atļaujas, pārejiet uz sadaļu **Iestatījumi** &gt; **Drošība** &gt; **Darba grupas** un atlasiet attiecīgo darba grupu. Atlasiet **Pārvaldīt lomas** un pēc tam atlasiet lomu, kurai ir piešķirtas vajadzīgās atļaujas, piemēram, **Sistēmas administrators**.

- Pārejiet uz sadaļu **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.

    - Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.
    - Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.

### <a name="setup-in-the-data-integration-project"></a>Iestatīšana datu integrācijas projektā

#### <a name="quoteheader"></a>QuoteHeader

- Pārliecinieties, ka pastāv nepieciešamais kartējums no **Shipto\_country** uz **DeliveryAddressCountryRegionISOCode**. Vērtību kartē varat definēt noklusējuma vērtību, kas tiek izmantota, ja ir atstāta tukša vērtība. Vienkārši atstājiet kreiso pusi tukšu un labajā pusē iestatiet vajadzīgo valsti vai reģionu. Tādējādi jums nav jāievada valsts vai reģions iekšzemes pasūtījumos.

    Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni un kur tukšai vērtībai atbilst vērtība **ASV**.

#### <a name="quoteline"></a>QuoteLine

- Pārliecinieties, ka nepieciešamā vienuma **SalesUnitSymbol** vērtību karte ir programmā Supply Chain Management.
- Pārliecinieties, ka programmā Sales ir definētas nepieciešamās vienības.

    Kartējumam no **oumid.name** uz **SalesUnitSymbol** ir definēta veidnes vērtība ar vērtību karti.

- Pēc izvēles varat pievienot tālāk norādītos kartējumus, lai palīdzētu nodrošināt pārdošanas piedāvājuma rindu importēšanu programmā Supply Chain Management gadījumos, ja nav pieejama debitora vai preces noklusējuma informācija.

    - **SiteId**— vieta ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas. Laukam **SiteId** nav noklusējuma veidnes vērtības.
    - **WarehouseId**— noliktava ir jānorāda, lai programmā Supply Chain Management apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas. Laukam **WarehouseId** nav noklusējuma veidnes vērtības.

## <a name="template-mapping-in-data-integrator"></a>Veidnes kartēšana datu integrētājā

> [!NOTE]
> - Lauki **Atlaide**, **Maksas** un **Nodokļi** tiek kontrolēti, izmantojot saliktus iestatījumus programmā Supply Chain Management. Pašlaik šie iestatījumi neatbalsta integrācijas kartēšanu. Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** apstrādā programma Supply Chain Management.
> - Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.

### <a name="quoteheader"></a>QuoteHeader

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Saistītās tēmas

[No potenciālā klienta līdz skaidrai naudai](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]