---
title: "No potenciālā klienta līdz skaidrai naudai"
description: "Šajā tēmā ir sniegts apskats par risinājumu No potenciālā klienta līdz skaidrai naudai programmās Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, un Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2017
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
ms.sourcegitcommit: f169b0ee20a7ca0c8d05c8bdcf2c04d411722f01
ms.openlocfilehash: ff166f89d13acbc3aefcbdb39f485881c81cb42c
ms.contentlocale: lv-lv
ms.lasthandoff: 12/21/2017

---

# <a name="prospect-to-cash"></a>No potenciālā klienta līdz skaidrai naudai

[!include[banner](../includes/banner.md)]

Risinājums “No potenciālā klienta līdz skaidrai naudai” nodrošina tiešu sinhronizēšanu starp programmu Dynamics 365 for Finance and Operations, Enterprise Edition, un programmu Dynamics 365 for Sales. Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales. Kamēr notiek datu plūsma starp Finance and Operations un Sales, programmā Sales varat veikt pārdošanas un mārketinga aktivitātes, un varat tikt galā ar pasūtījuma izpildi, izmantojot krājumu vadību programmā Finance and Operations.

Pašreizējā versijā risinājums No potenciālā klienta līdz skaidrai naudai nodrošina tālāk aprakstītos tiešās sinhronizācijas tipus.

- [Kontu uzturēšana programmā Sales un to tieša sinhronizēšana ar programmu Finance and Operations](accounts-template-mapping-direct.md)
- [Preču uzturēšana programmā Finance and Operations un to tieša sinhronizēšana ar programmu Sales](products-template-mapping-direct.md)
- [Kontaktpersonu uzturēšana programmā Sales un to tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations](contacts-template-mapping-direct.md)
- [Pārdošanas piedāvājuma tieša sinhronizēšana no programmas Sales uz programmu Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Pārdošanas pasūtījumu tieša sinhronizēšana no programmas Finance and Operations uz programmu Sales](sales-order-template-mapping-direct.md)
- [Pārdošanas pasūtījumu tieša sinhronizēšana no programmas Finance and Operations uz programmu Sales un otrādi](sales-order-template-mapping-direct-two-ways.md)
- [Pārdošanas rēķinu tiešā sinhronizēšana no Finance and Operations uz Sales](sales-invoice-template-mapping-direct.md)

Agrākās versijās risinājums No potenciālā klienta līdz skaidrai naudai nodrošina tālāk aprakstītos netiešās sinhronizācijas tipus.

- [Kontu uzturēšana programmā Sales un to sinhronizēšana ar Finance and Operations](accounts-template-mapping.md)
- [Kontaktpersonu uzturēšana programmā Sales un to sinhronizēšana ar programmu Finance and Operations](contacts-template-mapping.md)
- [Preču uzturēšana programmā Finance and Operations un to tieša sinhronizēšana ar programmu Sales](products-template-mapping.md)
- [Pārdošanas piedāvājumu izveidošana programmā Sales un to sinhronizēšana ar Finance and Operations](sales-quotation-template-mapping.md)
- [Pārdošanas pasūtījumu izveidošana programmā Finance and Operations un to sinhronizēšana ar programmu Sales](sales-order-template-mapping.md)
- [Pārdošanas rēķinu izveidošana programmā Finance and Operations un to sinhronizēšana ar Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Sistēmas prasības programmai Finance and Operations

Lai lietotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir jābūt instalētiem tālāk uzskaitītajiem komponentiem.

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs)

- Dynamics 365 for Finance and Operations, Enterprise Edition (2017. jūlijs) ar platformas 8. atjauninājumu (programmas būvējums 7.2.11792.56024 ar platformas būvējumu 7.0.4565.16212)
- Ir nepieciešami tālāk minētie labojumfaili.

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** — šis labojumfails ļauj veikt pārdošanas pasūtījumu sinhronizēšanu no Sales uz Finance and Operations, izmantojot līdzekli Datu integrācija. Tas nodrošina arī vairākus citus uzlabojumus.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — šis labojumfails ļauj veikt pārdošanas pasūtījumu rindu sinhronizēšanu no Finance and Operations uz Sales, izmantojot līdzekli Datu integrācija.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — šis labojumfails ļauj veikt pārdošanas pasūtījumu sinhronizēšanu no Finance and Operations uz Sales, izmantojot līdzekli Datu integrācija.

    > [!NOTE]
    > Ir nepieciešams instalēt tikai labojumfailu KB4045570, jo tā instalācijā ir ietvertas citos labojumfailos ietvertās izmaiņas. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations, versija 1611 (2016. gada novembris) 

- Dynamics 365 for Finance and Operations, versija 1611 (2016. gada novembris) ar platformas 8. atjauninājumu vai jaunāku

- Ir nepieciešami tālāk minētie labojumfaili.

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** — ļauj veikt pārdošanas pasūtījumu sinhronizēšanu programmā Finance and Operations un programmā Sales, izmantojot datu integrētāju. 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** — ļauj veikt pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanu programmā Finance and Operations un programmā Sales, izmantojot datu integrētāju.
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** — ir nepieciešams atbalsts risinājuma “No potenciālā klienta līdz skaidrai naudai” integrēšanai datu elementos.
    
    > [!NOTE]
    > Pēc labojumfailu instalēšanas jums ir nepieciešams aktivizēt tālāk norādīto pakešuzdevumu no formas **SalesPopulateProspectToCash**. Šī forma ir slēpta, jo jums tā ir nepieciešama tikai vienreiz. Lai piekļūtu šai formai, piesakieties vidē un savā pārlūkprogrammas adresē pievienojiet šādu vietrādi URL: &mi=action:SalesPopulateProspectToCash, piemēram, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash. Kad forma tiek atvērta, noklikšķiniet uz Labi. Šādi tiek aizpildīts jauns lauks **LineCreationSequnceNumber** tabulās **SalesLine**, **SalesQuotationLine** un **CustInvoiceTrans**, izmantojot unikālas vērtības, un tiek atsvaidzināts preču saraksts. Lai darbotos risinājuma “No potenciālā klienta līdz skaidrai naudai” integrēšana, šī procedūra ir jāizpilda obligāti.


## <a name="system-requirements-for-sales"></a>Sistēmas prasības programmai Sales

Lai lietotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir jābūt instalētiem tālāk uzskaitītajiem komponentiem.

- Dynamics 365 for Sales versija 1612 (8.2.1.207) (DB 8.2.1.207), tiešsaistes versija
- Risinājums “No potenciālā klienta līdz skaidrai naudai” programmai Dynamics 365 for Sales, versija 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > Veidnes ar versiju 1.0.0.0 un 1.0.0.1 tiek atbalstītas risinājumā “No potenciālā klienta līdz skaidrai naudai” programmai Dynamics 365 for Sales, versija 1.14.1.0
   >
   > Veidnes ar versiju 2.0.0.0 un 2.1.0.0 tiek atbalstītas risinājumā “No potenciālā klienta līdz skaidrai naudai” programmai Dynamics 365 for Sales, versija 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Instalēt risinājumu No potenciālā klienta līdz skaidrai naudai programmai Sales

1. Lejupielādējiet [Risinājuma No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales pakotnes zip failu](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) no vietnes CustomerSource.
2. Pārliecinieties, vai .zip fails ir atbloķēts. Pretējā gadījumā, kad mēģināt instalēt risinājuma pakotni, var tikt parādīts šāds kļūdas ziņojums: “Importēšanas pakotnes nav atrastas.” Lai atbloķētu zip failu, noklikšķiniet uz tā ar peles labo pogu un atlasiet **Rekvizīti**. Atlasiet **Atbloķēt**.
3. Izgūstiet no zip arhīva un palaidiet failu **PackageDeployer.exe**.
4. Tālāk aprakstītajā veidā instalējiet risinājumu No potenciālā klienta līdz skaidrai naudai savā Sales instancē.

    1. Kā izvietojuma tipu atlasiet **Office 365**.
    2. Atlasiet **Rādīt papildu**.
    3. Lai veiktu ātru instalēšanu, atlasiet kādu reģionu. Ja atlasāt **Nezinu**, sistēma meklē visus reģionus un instalēšana aizņem vairāk laika.
    4. Ievadiet lietotājvārdu un paroli lietotājam ar administratora tiesībām, kuram ir tiesības veikt instalēšanu.

