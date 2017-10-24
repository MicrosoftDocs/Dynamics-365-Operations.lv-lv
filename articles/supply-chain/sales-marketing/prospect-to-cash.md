---
title: "No potenciālā klienta līdz skaidrai naudai"
description: "Šajā tēmā ir sniegts apskats par risinājumu No potenciālā klienta līdz skaidrai naudai programmās Dynamics 365 for Finance and Operations, Enterprise Edition un Dynamics 365 for Sales."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>No potenciālā klienta līdz skaidrai naudai  

[!include[banner](../includes/banner.md)]

Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantota [Datu integrācija](/common-data-service/entity-reference/dynamics-365-integration), lai sinhronizētu datus starp Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition un Dynamics 365 for Sales instancēm, izmantojot Common Data Service (CDS). Līdzeklī Datu integrācija pieejamās risinājuma No potenciālā klienta līdz skaidrai naudai veidnes ļauj izmantot kontu, kontaktpersonu, preču, pārdošanas piedāvājumu, pārdošanas pasūtījumu un pārdošanas rēķinu datu plūsmu starp Finance and Operations un Sales. Kamēr notiek datu plūsma starp Finance and Operations un Sales, programmā Sales varat veikt pārdošanas un mārketinga aktivitātes, savukārt programmā Finance and Operations varat veikt pasūtījuma izpildi ar krājumu vadību. 

Šis risinājums nodrošina integrāciju tālāk norādītajās jomās. 

-   [Kontu uzturēšana programmā Sales un to sinhronizēšana ar Finance and Operations](accounts-template-mapping.md)
-   [Kontaktpersonu uzturēšana programmā Sales un to sinhronizēšana ar Finance and Operations](contacts-template-mapping.md)
-   [Preču uzturēšana programmā Finance and Operations un to sinhronizēšana ar Sales](products-template-mapping.md)
-   [Pārdošanas piedāvājumu izveidošana programmā Sales un to sinhronizēšana ar Finance and Operations](sales-quotation-template-mapping.md)
-   [Pārdošanas pasūtījumu izveidošana programmā Finance and Operations un to sinhronizēšana ar Sales](sales-order-template-mapping.md)
-   [Pārdošanas rēķinu izveidošana programmā Finance and Operations un to sinhronizēšana ar Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Sistēmas prasības programmai Dynamics 365 for Finance and Operations, Enterprise Edition

Lai izmantotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir nepieciešams instalēt tālāk uzskaitītos elementus.

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. jūlijs) ar platformas 8. atjauninājumu (programma 7.2.11792.56024 ar platformu 7.0.4565.16212)

- Divi labojumfaili programmatūrai Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs).

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — šis labojumfails ļauj veikt pārdošanas pasūtījuma rindas sinhronizēšanu ar līdzekli Datu integrācija no programmas Finance and Operations uz programmu Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — šis labojumfails ļauj veikt pārdošanas pasūtījuma sinhronizēšanu ar līdzekli Datu integrācija no programmas Finance and Operations uz programmu Sales.
    
**Piezīme**. Labojumfails KB4036524 ir jāinstalē tikai tāpēc, ka instalācijā ir ietvertas izmaiņas no KB4036461.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Sistēmas prasības programmai Dynamics 365 for Sales

Lai izmantotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir nepieciešams instalēt tālāk uzskaitītos elementus.

- Dynamics 365 for Sales versija 1612 (8.2.1.207) (DB 8.2.1.207) tiešsaistes versija vai jaunāka.
- Risinājums No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales, versija 1.14.0.0 (v14) vai jaunāka.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Instalēt risinājumu No potenciālā klienta līdz skaidrai naudai programmai Sales

- Lejupielādējiet [Risinājuma No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales pakotnes zip failu](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) vietnē CustomerSource.

- Pārliecinieties, vai zip fails ir atbloķēts, lai risinājuma pakotnes instalēšanas laikā jums nerādītu kļūdas ziņojumu “Importēšanas pakotnes nav atrastas”. Lai failu atbloķētu, izpildiet tālāk aprakstītos norādījumus.

    -  Noklikšķiniet uz zip faila ar peles labo pogu.
    -  Atlasiet **Rekvizīti** un pēc tam atlasiet **Atbloķēt**. 

- Izgūstiet no ZIP arhīva un palaidiet failu PackageDeployer.exe.

- Instalējiet risinājumu No potenciālā klienta līdz skaidrai naudai savai Sales instancei.

    - Atlasiet izvietošanas tipu **Office 365**.
    - Atlasiet **Rādīt papildu**.
    - Lai veiktu ātru instalēšanu, atlasiet kādu vērtību vienumam **Reģions**. Ja atlasāt **Nezinu**, tad sistēma meklē visus reģionus un instalēšanai var būt nepieciešams ilgāks laiks.
    - Ievadiet vērtības laukiem **Lietotājvārds** un **Parole** lietotājam–administratoram, kuram ir lietotāja tiesības veikt instalēšanu.

