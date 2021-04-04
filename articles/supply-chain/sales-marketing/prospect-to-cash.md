---
title: No potenciālā klienta līdz skaidrai naudai
description: Šajā tēmā ir sniegts apskats par risinājumu No potenciālā klienta līdz skaidrai naudai, kas darbojas programmās Dynamics 365 Supply Chain Management un Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 70ea2638408296df283a030dedce03b22cb57d81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248743"
---
# <a name="prospect-to-cash"></a>No potenciālā klienta līdz skaidrai naudai

[!include [banner](../includes/banner.md)]

Risinājums No potenciālā klienta līdz skaidrai naudai nodrošina tiešu sinhronizāciju programmās Dynamics 365 Supply Chain Management un Dynamics 365 Sales. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu. Kamēr notiek datu plūsma, programmā Sales varat veikt pārdošanas un mārketinga aktivitātes, un varat tikt galā ar pasūtījuma izpildi, izmantojot krājumu vadību programmā Supply Chain Management. 

Lai iegūtu papildinformāciju par risinājuma No potenciālā klienta līdz skaidrai naudai integrāciju, noskatieties īso YouTube video [Risinājuma No potenciālā klienta līdz skaidrai naudai integrācija](https://www.youtube.com/watch?v=AVV9x5x-XCg).

Pašreizējā versijā risinājums No potenciālā klienta līdz skaidrai naudai nodrošina tālāk aprakstītos tiešās sinhronizācijas tipus.

- [Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management](accounts-template-mapping-direct.md)
- [Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Sales](products-template-mapping-direct.md)
- [Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai klientiem programmā Supply Chain Management](contacts-template-mapping-direct.md)
- [Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Supply Chain Management](sales-quotation-template-mapping-sales-fin.md)
- [Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)
- [Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Management sistēmas prasības
Integrācija No potenciālā klienta līdz skaidrai naudai tiek atbalstīta tālāk norādītajās versijās.

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 (2017. gada decembris)

- Dynamics 365 for Finance and Operations Enterprise Edition (2017. gada decembris) — lietojumprogrammas būvējums 7.3.11971.56116 ar 12. platformas atjauninājumu (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations Enterprise Edition (2017. gada jūlijs)

- Dynamics 365 for Finance and Operations Enterprise Edition (2017. gada jūlijs) — ar 8. platformas atjauninājumu (lietojumprogrammas būvējums 7.2.11792.56024 ar platformas būvējumu 7.0.4565.16212).
- Ir nepieciešami tālāk minētie labojumfaili.

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)**— šis labojumfails ļauj veikt pārdošanas pasūtījumu sinhronizēšanu no Sales uz Supply Chain Management, izmantojot līdzekli Datu integrācija. Tas nodrošina arī vairākus citus uzlabojumus.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**— šis labojumfails ļauj veikt pārdošanas pasūtījumu rindas sinhronizēšanu no Supply Chain Management uz Sales, izmantojot līdzekli Datu integrācija.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**— šis labojumfails ļauj veikt pārdošanas pasūtījumu sinhronizēšanu no Supply Chain Management uz Sales, izmantojot līdzekli Datu integrācija.

    > [!NOTE]
    > Ir nepieciešams instalēt tikai labojumfailu KB4045570, jo tā instalācijā ir ietvertas citos labojumfailos ietvertās izmaiņas. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations versija 1611 (2016. gada novembris)

- Dynamics 365 for Finance and Operations versija 1611 (2016. gada novembris) ar 8. platformas atjauninājumu vai jaunāka versija

- Ir nepieciešami tālāk minētie labojumfaili.

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)**— ļauj veikt pārdošanas pasūtījumu sinhronizēšanu programmā Supply Chain Management un programmā Sales, izmantojot datu integrētāju. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)**— ļauj veikt pārdošanas pasūtījumu galvēņu un rindu sinhronizēšanu programmā Supply Chain Management un programmā Sales, izmantojot datu integrētāju.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – ir nepieciešams atbalsts risinājuma “No potenciālā klienta līdz skaidrai naudai” integrēšanai datu elementos.
    
    > [!NOTE]
    > Pēc labojumfailu instalēšanas jums ir nepieciešams aktivizēt tālāk norādīto pakešuzdevumu no formas **SalesPopulateProspectToCash**. Šī forma ir slēpta, jo jums tā ir nepieciešama tikai vienreiz. Lai piekļūtu šai veidlapai, piesakieties vidē un savā pārlūkprogrammas adresē pievienojiet šādu vietrādi URL: *&mi=action:SalesPopulateProspectToCash*, piemēram, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Kad forma tiek atvērta, noklikšķiniet uz Labi. Šādi tiek aizpildīts jauns lauks **LineCreationSequnceNumber** tabulās **SalesLine**, **SalesQuotationLine** un **CustInvoiceTrans**, izmantojot unikālas vērtības, un tiek atsvaidzināts preču saraksts. Lai darbotos risinājuma “No potenciālā klienta līdz skaidrai naudai” integrēšana, šī procedūra ir jāizpilda obligāti.


## <a name="system-requirements-for-sales"></a>Sistēmas prasības programmai Sales

Lai lietotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir jābūt instalētiem tālāk uzskaitītajiem komponentiem.

- Dynamics 365 Sales versija 1612 (8.2.1.207) (DB 8.2.1.207) tiešsaistes versija vai jaunāka versija.
- Risinājums skaidrai naudai programmai Dynamics 365 Sales, versija 1.15.0.0 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma AppSource. [Lejupielādēt Dynamics 365, No potenciālā klienta līdz skaidrai naudai](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]