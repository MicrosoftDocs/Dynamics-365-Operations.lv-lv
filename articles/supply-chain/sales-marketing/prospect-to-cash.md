---
title: No potenciālā klienta līdz skaidrai naudai
description: Šajā tēmā ir sniegts apskats par risinājumu No potenciālā klienta līdz skaidrai naudai, kas darbojas programmās Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b46ece384a28f8e78989253fcf467fbf3feaf1b7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554625"
---
# <a name="prospect-to-cash"></a>No potenciālā klienta līdz skaidrai naudai

[!include [banner](../includes/banner.md)]

Risinājums No potenciālā klienta līdz skaidrai naudai nodrošina tiešu sinhronizāciju programmās Dynamics 365 for Finance and Operations un Dynamics 365 for Sales. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales. Kamēr notiek datu plūsma starp Finance and Operations un Sales, programmā Sales varat veikt pārdošanas un mārketinga aktivitātes, un varat tikt galā ar pasūtījuma izpildi, izmantojot krājumu vadību programmā Finance and Operations. 

Lai iegūtu papildinformāciju par risinājuma No potenciālā klienta līdz skaidrai naudai integrāciju, noskatieties īso YouTube video [Risinājuma No potenciālā klienta līdz skaidrai naudai integrācija](https://www.youtube.com/watch?v=AVV9x5x-XCg).

Pašreizējā versijā risinājums No potenciālā klienta līdz skaidrai naudai nodrošina tālāk aprakstītos tiešās sinhronizācijas tipus.

- [Kontu uzturēšana programmā Sales un to tieša sinhronizēšana ar programmu Finance and Operations](accounts-template-mapping-direct.md)
- [Preču uzturēšana programmā Finance and Operations un to tieša sinhronizēšana ar programmu Sales](products-template-mapping-direct.md)
- [Kontaktpersonu uzturēšana programmā Sales un to tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations](contacts-template-mapping-direct.md)
- [Pārdošanas piedāvājuma tieša sinhronizēšana no programmas Sales uz programmu Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Pārdošanas pasūtījumu tieša sinhronizēšana no programmas Finance and Operations uz programmu Sales un otrādi](sales-order-template-mapping-direct-two-ways.md)
- [Pārdošanas rēķina tieša sinhronizēšana no programmas Finance and Operations uz programmu Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>Sistēmas prasības programmai Finance and Operations
Integrācija No potenciālā klienta līdz skaidrai naudai tiek atbalstīta tālāk norādītajās versijās.

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 (2017. gada decembris)

- Dynamics 365 for Finance and Operations Enterprise Edition (2017. gada decembris) — lietojumprogrammas būvējums 7.3.11971.56116 ar 12. platformas atjauninājumu (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations Enterprise Edition (2017. gada jūlijs)

- Dynamics 365 for Finance and Operations Enterprise Edition (2017. gada jūlijs) — ar 8. platformas atjauninājumu (lietojumprogrammas būvējums 7.2.11792.56024 ar platformas būvējumu 7.0.4565.16212).
- Ir nepieciešami tālāk minētie labojumfaili.

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)**  — šis labojumfails ļauj veikt pārdošanas pasūtījumu sinhronizēšanu no Sales uz Finance and Operations, izmantojot līdzekli Datu integrācija. Tas nodrošina arī vairākus citus uzlabojumus.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**  — šis labojumfails ļauj veikt pārdošanas pasūtījumu rindu sinhronizēšanu no Finance and Operations uz Sales, izmantojot līdzekli Datu integrācija.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**  — šis labojumfails ļauj veikt pārdošanas pasūtījumu sinhronizēšanu no Finance and Operations uz Sales, izmantojot līdzekli Datu integrācija.

    > [!NOTE]
    > Ir nepieciešams instalēt tikai labojumfailu KB4045570, jo tā instalācijā ir ietvertas citos labojumfailos ietvertās izmaiņas. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations versija 1611 (2016. gada novembris)

- Dynamics 365 for Finance and Operations versija 1611 (2016. gada novembris) ar 8. platformas atjauninājumu vai jaunāka versija

- Ir nepieciešami tālāk minētie labojumfaili.

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)**  — ļauj veikt pārdošanas pasūtījumu sinhronizēšanu programmā Finance and Operations un programmā Sales, izmantojot datu integrētāju. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)**  — ļauj veikt pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanu programmā Finance and Operations un programmā Sales, izmantojot datu integrētāju.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)**  — ir nepieciešams atbalsts risinājuma “No potenciālā klienta līdz skaidrai naudai” integrēšanai datu elementos.
    
    > [!NOTE]
    > Pēc labojumfailu instalēšanas jums ir nepieciešams aktivizēt tālāk norādīto pakešuzdevumu no formas **SalesPopulateProspectToCash**. Šī forma ir slēpta, jo jums tā ir nepieciešama tikai vienreiz. Lai piekļūtu šai veidlapai, piesakieties vidē un savā pārlūkprogrammas adresē pievienojiet šādu vietrādi URL: *&mi=action:SalesPopulateProspectToCash*, piemēram, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Kad forma tiek atvērta, noklikšķiniet uz Labi. Šādi tiek aizpildīts jauns lauks **LineCreationSequnceNumber** tabulās **SalesLine**, **SalesQuotationLine** un **CustInvoiceTrans**, izmantojot unikālas vērtības, un tiek atsvaidzināts preču saraksts. Lai darbotos risinājuma “No potenciālā klienta līdz skaidrai naudai” integrēšana, šī procedūra ir jāizpilda obligāti.


## <a name="system-requirements-for-sales"></a>Sistēmas prasības programmai Sales

Lai lietotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir jābūt instalētiem tālāk uzskaitītajiem komponentiem.

- Dynamics 365 for Sales versija 1612 (8.2.1.207) (DB 8.2.1.207) (tiešsaistes versija) vai jaunāka versija
- Risinājuma No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales versija 1.15.0.0 vai jaunāka versija. Risinājumu var lejupielādēt no pakalpojuma AppSource. [Lejupielādēt Dynamics 365, No potenciālā klienta līdz skaidrai naudai](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
