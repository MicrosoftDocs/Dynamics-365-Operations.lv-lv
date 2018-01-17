---
title: "Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma ar Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 405a6cf9f3e6cc52925ff7d9f10836196343c36b
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration). 

Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma ar Microsoft Dynamics 365 for Sales.

## <a name="template-and-task"></a>Veidne un uzdevums

Preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma (Finance and Operations) ar Microsoft Dynamics 365 for Sales (Sales) tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.

-   Veidnes nosaukums: Preces (Fin and Ops ar Sales)

-   Projekta uzdevuma nosaukums: Preces

Nepieciešamie sinhronizēšanas uzdevumi pirms preču sinhronizācijas: nav

## <a name="entity-set"></a>Elementu kopa

| **Finance and Operations** | **CDS** | **pārdošana;**  |
|----------------------------|---------|------------|
| Pārdodamas izlaistās preces | Prece | Preces   |

## <a name="entity-flow"></a>Elementu plūsma

Preces tiek pārvaldītas programmā Finance and Operations un sinhronizētas ar programmu Sales. Datu elements **Pārdodamas izlaistās preces** programmā Finance and Operations eksportē tikai pārdodamas preces, un tas nozīmē, ka precēm ir nepieciešamā informācija, kas jāizmanto pārdošanas pasūtījumā. Tie paši noteikumi ir spēkā, kad prece tiek validēta, izmantojot funkciju **Validēt** lapā **Izlaistā prece**.

**Preces numurs** tiek izmantots kā atslēga, proti, preču varianti tiek sinhronizēti pakalpojumā CDS un programmā Sales ar atsevišķiem **Preču ID** katram vienumam **Preces variants**.

## <a name="prospect-to-cash-solution-for-sales"></a>Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales

Programmā Sales precēm tiek pievienots jauns lauks **Tiek ārēji uzturēts**, lai norādītu, ka konkrētā prece tiek uzturēta ārēji. Importēšanas laikā uz programmu Sales vērtība pēc noklusējuma tiek iestatīta uz **Jā**.

-   **Tiek ārēji uzturēts = Jā**: prece ir no Finance and Operations un nebūs rediģējama programmā Sales.

-   **Tiek ārēji uzturēts = Nē**: prece ir ievadīta tieši programmā Sales.

-   **Tiek ārēji uzturēts = Tukšs**: prece pastāv programmā Sales pirms risinājuma No potenciālā klienta līdz skaidrai naudai iespējošanas.

Lauka **Tiek ārēji uzturēts** informācija tiek izmantota, lai nodrošinātu, ka ar Finance and Operations tiek sinhronizēti tikai **Piedāvājumi** un **Pārdošanas pasūtījumi**, kuros preces ir **Ārēji uzturētas preces**.

**Ārēji uzturētas preces** tiek automātiski pievienotas pirmajam derīgajam vienumam **Cenrādis** ar to pašu valūtu. Ņemiet vērā, ka saraksts tiek kārtots alfabētiskā secībā pēc vienuma **Nosaukums**. Preces pārdošanas cena no Finance and Operations tiek izmantota kā cena vienumā **Cenrādis**. Tas nozīmē, ka programmā Sales ir nepieciešams vienums **Cenrādis** katram vienumam **Preces pārdošanas valūta** programmā Finance and Operations. Izlaisto pārdodamo preču valūta tiek iestatīta uz uzskaites valūtu juridiskajā personā, no kurienes šī prece ir eksportēta.

> [!NOTE]
> Preču sinhronizācija neizdosies bez vienuma **Cenrādis** ar atbilstošu valūtu.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

-   Pirms veicat pirmo sinhronizāciju, esošajām precēm programmā Finance and Operations ir jaaizpilda **Atšķirīgo preču tabula**. Esošās preces netiks sinhronizētas, kamēr nebūs pabeigts šis darbs.

    -   Programmā Finance and Operations izmantojiet lauku Meklēt, lai atrastu vienumu **Aizpildīt atšķirīgo preču tabulu**.

    -   Noklikšķiniet uz **Aizpildīt atšķirīgo preču tabulu**, lai palaistu darbu. Šis darbs ir jāizpilda vienu reizi.

-   Pārliecinieties, vai sadaļā **Avots -\> CDS kartējuma SalesUnitSymbol/DefaultSellingUnitOfMeasure** pārdošanas vienumam **Mērvienība** (UOM) programmā Finance and Operations ir norādīta nepieciešamā **ValueMap** informācija.

-   Atjauniniet **CDS organizācijas ID Organization_OrganizationId** sadaļā **Avots -\> CDS**.

    -   Veidnes vērtība tiek iestatīta uz noklusējuma vērtību ORG001.

-   Atjauniniet vienuma **Vienību grupa** (**defaultuomscheduleid.name**) **ValueMap** sadaļā **CDS -\> Adresāts** tā, lai tas atbilstu vienumam **Vienību grupas** programmā Sales.

    -   Veidnes vērtība tiek iestatīta uz **Noklusējuma mērvienība**.

-   Pārliecinieties, vai visu preču pārdošanas mērvienības no Finance and Operations pastāv programmā Sales ar vienuma **CDS izdošanas saraksti** vērtību.

-   Pārliecinieties, vai programmā Sales pastāv **Cenrāži** katrai preču pārdošanas valūtai programmā Finance and Operations.

-   Preces programmā Sales var izveidot ar statusu **Melnraksts** vai **Aktīvs**. Tas tiek kontrolēts programmas Sales sadaļas **Pārdošana** esošajā sadaļā **Sistēmas iestatījumi**.

    -   Preces, kas izveidotas ar melnraksta statusu, ir jāaktivizē pirms tos pievienošanas sadaļā **Piedāvājums** vai **Pārdošanas pasūtījums**.

## <a name="template-mapping-in-data-integrator"></a>Veidnes kartēšana datu integrētājā

Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.

![Veidnes kartēšana datu integrētājā](./media/products-template-mapping-data-integrator-1.png)

![Veidnes kartēšana precēm datu integrētājā](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Saistītās tēmas

[Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations](accounts-template-mapping.md)

[Kontaktpersonu sinhronizēšana no programmas Sales uz kontaktpersonām vai klientiem programmā Finance and Operations](contacts-template-mapping.md)

[Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations](sales-quotation-template-mapping.md)

[Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales](sales-order-template-mapping.md)

[Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales](sales-invoice-template-mapping.md)


