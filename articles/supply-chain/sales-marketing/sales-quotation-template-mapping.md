---
title: "Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no Sales ar Finance and Operations"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Sales ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no Sales ar Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration). 

Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Sales (Sales) ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (Finance and Operations). 

## <a name="template-and-tasks"></a>Veidne un uzdevumi

Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Sales ar Finance and Operations tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.

- **Veidnes nosaukums:** Pārdošanas piedāvājumi (Sales ar Fin and Ops)
- **Projekta uzdevumu nosaukumi**

    - QuoteHeader
    - QuoteLine

Pirms pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanas ir jāveic tālāk norādītie sinhronizācijas uzdevumi.

- Preces (no Fin and Ops uz Sales)
- Konti (no Sales uz Fin and Ops) (ja izmantoti)
- Kontaktpersonas uz debitoriem (no Sales uz Fin un Ops) (ja tiek izmantotas)

## <a name="entity-set"></a>Elementu kopa

| Pārdošana        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Citāti       | Piedāvājums     | Pārdošanas piedāvājumu virsraksti   |
| QuoteDetails | QuotationLine | CDS pārdošanas piedāvājuma rindas |

## <a name="entity-flow"></a>Elementu plūsma

Pārdošanas piedāvājumi tiek izveidoti programmā Sales un sinhronizēti ar Finance and Operations.

Pārdošanas piedāvājumi no Sales tiek sinhronizēti tikai tad, ja ir izpildīti tālāk norādītie nosacījumi.

- Visas preces pārdošanas piedāvājuma rindās ir ārēji uzturētas.
- Pārdošanas piedāvājums ir aktīvs vai aktivizēts.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Elementam Piedāvājums ir pievienots lauks **Ir tikai ārēji uzturētas preces**, lai konsekventi izsekotu, vai pārdošanas piedāvājumā ir ietvertas tikai ārēji uzturētas preces. Ja pārdošanas piedāvājumā ir tikai ārēji uzturētas preces, tās tiek uzturētas programmā Finance and Operations. Šī izturēšanās palīdz nodrošināt, ka nemēģināsit sinhronizēt pārdošanas piedāvājuma rindas ar precēm, kas programmā Finance and Operations ir nezināmas.

Visas preces un rindas piedāvājumā tiek atjauninātas ar lauka **Ir tikai ārēji uzturētas preces** informāciju no piedāvājuma virsraksta. Šī informācija ir atrodama elementa Piedāvājuma rinda laukā **Piedāvājumam ir tikai ārēji uzturētas preces**.

Laukus **Atlaide**, **Maksas** un **Nodokļi** kontrolē kompleksi iestatījumi programmā Finance and Operations. Šie iestatījumi pašlaik neatbalsta integrācijas kartēšanu. Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** pārvalda un apstrādā programma Finance and Operations.

Programmā Sales risinājums tālāk norādītos laukus pārveido par tikai lasāmiem, jo attiecīgās vērtības netiek sinhronizētas ar programmu Finance and Operations.

- **Tikai lasāmi lauki pārdošanas piedāvājuma virsrakstā:** Atlaide %, Atlaide, Vedmaksa
- **Tikai lasāmi lauki pārdošanas piedāvājuma rindās:** Nodokļi

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms pārdošanas pasūtījumu sinhronizēšanas ir svarīgi sistēmas atjaunināt ar tālāk norādīto iestatījumu.

### <a name="setup-in-sales"></a>Iestatīšana programmā Sales

- Dodieties uz **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Sales** un pārliecinieties, vai lauks **Atlaides aprēķināšanas metode** ir iestatīts uz **Vienībai**. Šis iestatījums palīdz garantēt programmā Sales esošās rindas krājuma atlaides atbilstību iestatījumam programmā Finance and Operations. Pretējā gadījumā atlaide programmā Finance and Operations nebūs pareiza, jo programmā Finance and Operations atlaide tiks nolasīta kā atlaide par vienību pat tad, ja programmā Sales tā bija atlaide par rindu.

### <a name="setup-in-finance-and-operations"></a>Iestatīšana programmā Finance and Operations

- Dodieties uz **Debitoru parādi** &gt; **Iestatījumi** &gt; **Debitoru parādu parametri**. Cilnē **Numuru sērija** atlasiet numuru sēriju pārdošanas piedāvājumiem un pēc tam noklikšķiniet uz **Skatīt detalizētu informāciju**. Pēc tam sadaļā **Vispārīgie iestatījumi** lauku **Manuāli** iestatiet uz **Jā**.
- Dodieties uz **Debitoru parādi** &gt; **Iestatījumi** &gt; **Debitoru parādu parametri**. Pēc tam cilnē **Sūtījumi** lauku **Piegādes datuma kontrole** iestatiet uz **Nav**. Šis iestatījums palīdz novērst sinhronizācijas neizdošanos pārdošanas piedāvājumiem.

### <a name="setup-in-the-data-integration-project"></a>Iestatīšana datu integrācijas projektā

#### <a name="quoteheader"></a>QuoteHeader

- Programmā Finance and Operations ir obligāti jāaizpilda lauks **Pieprasītais piegādes datums**; atstājot to tukšu, sinhronizācija neizdosies. Lai novērstu šo problēmu tukša lauka gadījumā, no sadaļas **Avots &gt;CDS** tiek paņemts noklusējuma datums. Šis datums ir jāatjaunina uz vajadzīgo vērtību. Pašlaik nevarat ievadīt tādu vērtību kā **Šodien**, lai norādītu šodienas datumu. Ir jāievada konkrēts datums. Lauka **Pieprasītais piegādes datums** noklusējuma veidnes vērtība ir **01.01.2020.**.
- Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts. Lai palīdzētu novērst sinhronizācijas kļūdas, varat norādīt noklusējuma vērtību, ko izmantot gadījumos, ja lauks programmā Sales ir atstāts tukšs. Šī noklusējuma vērtība ir noderīga arī tādēļ, ka jums nav manuāli jāievada vērtība laukā **Valsts reģions** vietējām adresēm. Laukam **DeliveryAddressCountryRegionISOCode** nav noklusējuma veidnes vērtības.
- Atjauniniet lauka **CDS organizācijas ID** kartējumu sadaļā **Avots &gt; CDS** tā, lai tas atbilstu lauka **CDS organizācija** vērtībai elementā Organizācija.

    - Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.
    - Lauka **Account_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.
    - Lauka **InvoiceAccount_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.

#### <a name="quoteline"></a>QuoteLine

- Atjauniniet lauka **CDS organizācijas ID** kartējumu sadaļā **Avots &gt; CDS** tā, lai tas atbilstu lauka **CDS organizācija** vērtībai elementā Organizācija.

    - Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.
    - Lauka **Product_Organization_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.
    - Lauka **Quotation_Organization_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.

- Programmā Finance and Operations ir obligāti jāaizpilda lauks **Pieprasītais piegādes datums**; atstājot to tukšu, sinhronizācija neizdosies. Lai novērstu šo problēmu tukša lauka gadījumā, no sadaļas **Avots &gt;CDS** tiek paņemts noklusējuma datums. Šis datums ir jāatjaunina uz vajadzīgo vērtību. Pašlaik nevarat ievadīt tādu vērtību kā **Šodien**, lai norādītu šodienas datumu. Ir jāievada konkrēts datums. Lauka **Pieprasītais piegādes datums** noklusējuma veidnes vērtība ir **01.01.2020.**.
- Varat pievienot tālāk norādītos kartējumus no sadaļas **CDS &gt; Adresāts**, lai palīdzētu nodrošināt piedāvājuma rindu importēšanu programmā Finance and Operations gadījumos, ja nav noklusējuma informācijas no debitora vai preces.

    - **SiteId** — vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas. Laukam **SiteId** nav noklusējuma veidnes vērtības.
    - **WarehouseId** — noliktava ir jānorāda, lai programmā Finance and Operations apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas. Laukam **WarehouseId** nav noklusējuma veidnes vērtības.

- Pārliecinieties, vai programmā Finance and Operations pārdošanas mērvienībai (UOM) obligātā vērtības karte ir norādīta lauka **Quantity_UOM** kartējumā **CDS &gt; Adresāts** vienumam **SALESUNITSYMBOL**.

## <a name="template-mapping-in-data-integrator"></a>Veidnes kartēšana datu integrētājā

> [!NOTE]
> - Laukus **Atlaide**, **Maksas** un **Nodokļi** kontrolē kompleksi iestatījumi programmā Finance and Operations. Šie iestatījumi pašlaik neatbalsta integrācijas kartēšanu. Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** apstrādā programma Finance and Operations.
> - Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**. Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.

Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.

### <a name="quoteheader"></a>QuoteHeader

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Saistītās tēmas

[Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales](products-template-mapping.md)

[Kontu sinhronizēšana no programmas Sales uz klientiem programmā Finance and Operations](accounts-template-mapping.md)

[Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations](contacts-template-mapping.md)



