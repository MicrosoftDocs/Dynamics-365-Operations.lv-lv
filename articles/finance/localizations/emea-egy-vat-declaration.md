---
title: PVN deklarācija Ēģiptei
description: Šajā tēmā paskaidrots, kā konfigurēt un ģenerēt PVN atgriešanas formu Ēģiptei.
author: sndray
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3ebb78f3fa481cc63376b7d6428cf4944bbf6f4c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839820"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>PVN deklarācija Ēģiptei (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

Šajā tēmā paskaidrots, kā iestatīt un ģenerēt PVN atgriešanas veidlapu un pārdošanas un pirkšanas grāmatas juridiskām personām Ēģiptē.

Ēģiptes PVN atgriešanas veidlapa ir oficiālais dokuments, kas apkopo kopējo izvades PVN nodokļa summu, kopējo atgūstamo ievades PVN nodokļa summu un saistītās PVN nodokļa summas saistības. Šī veidlapa tiek izmantota visu veidu nodokļu maksātājiem un tā jāaizpilda manuāli, izmantojot nodokļu iestādes portālu. PVN atgriešanas veidlapa parasti tiek saukta par PVN nodokļu deklarāciju.

PVN atgriešanas veidlapa programmā Dynamics 365 Finance iekļauj tālāk minētos pārskatus.

- PVN atgriešanas veidlapa Nr. 10, kas sniedz summu sadalījumu, korekcijas un PVN summu katrai rindas precei PVN atgriešanas veidlapā, kā tas ir aprakstīts tiesību aktos.
- Pārdošanas darbību grāmata
- Pirkšanas darījumu grāmata

## <a name="prerequisites"></a>Priekšnosacījumi
Juridiskās personas primārajai adresei ir jāatrodas Ēģiptē.
Darbvietā **Līdzekļu pārvaldība** iespējojiet tālāk norādīto līdzekli.

   - (Ēģipte) Kategoriju hierarhija pārdošanas un pirkšanas nodokļa pārskatam.

Papildinformāciju par līdzekļu iespējošanu skatiet rakstā [Pārskats par līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Darbvietā **Elektronisko pārskatu sniegšana** no repozitorija importējiet elektronisko pārskatu formātu:

- PVN deklarācija Excel (EG)

> [!NOTE]
> Iepriekš minētais formāts ir balstīts uz **Nodokļu deklarēšanas modeli** un tas izmanto **Nodokļu deklarācijas modeļa kartējumu**. Papildu konfigurācijas tiks importētas automātiski.

Papildinformāciju par elektronisko pārskatu konfigurāciju importēšanu skatiet sadaļā [Elektronisko pārskatu konfigurāciju lejupielāde no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektronisko atskaišu veidošanas konfigurāciju lejupielāde

PVN atgriešana no Ēģiptes īstenošana ir balstīta uz elektronisko pārskatu (ER) konfigurācijām. Papildinformāciju par konfigurējamām pārskata iespējām un koncepcijām skatiet sadaļā [Elektronisko pārskatu sniegšana](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Informāciju par ražošanas un lietotāju pieņemšanas testēšanas (UAT) vidēm skatiet sadaļā [Elektronisko pārskatu konfigurāciju lejupielāde no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Lai izveidotu PVN atgriešanas veidlapu un saistītos pārskatus Ēģiptes juridiskajā personā, augšupielādējiet tālāk minētās konfigurācijas.

- Nodokļu deklarācijas model.version.70.xml vai jaunāka versija
- Nodokļu deklarācijas modeļa mapping.version.70.120.xml vai jaunāka versija
- PVN deklarācijas Excel (EG).version.70.32 vai jaunāka versija

Pēc ER konfigurāciju lejupielādes no Lifecycle Services (LCS) vai globālā repozitorija, veiciet tālāk minētās darbības.

1. Pārejiet uz darbvietu **Elektroniskie pārskati** un atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
1. Lapas **Konfigurācijas** darbību rūtī atlasiet **Valūta** > **Ielādēt no XML faila**.
1. Augšupielādējiet failus augstāk minētajā secībā. Kad visas konfigurācijas ir augšupielādētas, konfigurācijas kokam ir jābūt redzamam programmā Finance.

## <a name="set-up-application-specific-parameters"></a>Programmai raksturīgu parametru iestatīšana

Programmai specifiskie parametri ļauj izveidot kritērijus tam, kā nodokļu darbības tiek klasificētas un aprēķinātas katrā rindā, ģenerējot pārskatu. Noteikšana ir pamatota uz krājumu PVN grupas, PVN grupas, PVN koda un citiem kritērijiem, kas noteikti uzmeklēšanas definīcijā.

Ēģiptes pārdošanas un pirkšanas grāmatas pārskatos ir ietverta kolonnu kopa, kas atbilst noteiktai darbību klasifikācijai kā operāciju, preču un dokumentu tipi, kas ir specifiski Ēģiptei. Tā vietā, lai šīs jaunās klasifikācijas iekļautu kā jaunus ierakstu datus, grāmatojot darbības, klasifikācijas tiks noteiktas, pamatojoties uz dažādām uzmeklēšanām, kas ieviestas **Konfigurācijas** > **Programmai specifisku parametru iestatīšana** > **Iestatīšana**, lai izpildītu PVN pārskatu prasības Ēģiptei. 

![Programmai specifisku parametru lapa](media/egypt-vat-declaration-setup1.png)

Šīs uzmeklēšanas konfigurācijas tiek izmantotas, lai klasificētu darbības pirkšanas un pārdošanas PVN grāmatu pārskatos:

- **PurchaseItemTypeLookup** > O kolonna: krājuma veids
- **VATRateTypeLookup** > B kolonna: nodokļa veids
- **VATRateTypeLookup** > C kolonna: tabulas krājuma veids
- **PurchaseOperationTypeLookup** > A kolonna: dokumenta veids
- **SalesOperationTypeLookup** > N kolonna: operācijas veids
- **SalesItemTypeLookup** > O kolonna: krājuma veids

Veiciet tālāk norādītās darbības, lai iestatītu dažādās uzmeklēšanas, kas tiek izmantotas PVN deklarācijas un saistīto grāmatu pārskatu ģenerēšanai. 

1. Darbvietā **Elektronisko pārskatu sniegšana** atlasirt **Konfigurācijas** > **Iestatījumi**, lai iestatītu noteikumus nodokļu darījumu identificēšanai PVN atgriešanas veidlapas saistītajā rūtiņā.
2. Atlasiet pašreizējo versiju un kopsavilkuma cilnē **Uzmeklēšanas** atlasiet uzmeklēšanas nosaukumu. Piemēram, **SalesItemTypeLookup**. Šī uzmeklēšana identificē klasifikāciju sarakstu pārdošanas PVN grāmatā, ko pieprasa nodokļu iestāde.
3. Kopsavilkuma cilnē **Nosacījumi** atlasiet **Pievienot** un jaunajā rindā kolonnā **Uzmeklēšanas rezultāti** atlasiet saistīto rindu, kas apzīmē klasifikāciju **O kolonnā**.
4. Kolonnā **PVN grupa** atlasiet PVN grupu, kas tiek izmantota klasifikācijas identificēšanai. Piemēram, **Iekšzemes pārdošanas rēķins**. Varat izmantot arī krājumu PVN grupu, nodokļu kodu vai koka atribūtu kombināciju, ja konfigurācija ir definēta citādi. 
5. Kolonnā **Nosaukums** atlasiet nodokļu darbības klasifikāciju.
6. Atkārtojiet 3.-5. darbību visām pieejamajām uzmeklēšanām.
7. Atlasiet **Pievienot**, lai ietvertu galīgo ieraksta rindu, un kolonnā **Uzmeklēšanas rezultāti** atlasiet **Nav piemērojams**. 
8. Atlikušajās kolonnās atlasiet **Nav tukšs**. 

> [!NOTE]
> Kad pievienojat pēdējo ierakstu — **Nav piemērojams** —, jūs definējat šādu kārtulu: kad PVN grupa, krājuma PVN grupa, nodokļa kods un nosaukums, kas tiek nodots kā arguments, neatbilst nevienam no iepriekšējiem noteikumiem, darījumi netiek iekļauti pārdošanas PVN grāmatā. Lai gan šī kārtula netiek lietota, ģenerējot pārskatu, kārtula palīdz izvairīties no kļūdām pārskatu ģenerēšanā, ja trūkst kārtulas konfigurācijas.

Tabulās zemāk ir parādīts ieteiktās konfigurācijas piemērs aprakstītajām uzmeklēšanas konfigurācijām. 

**SalesItemTypeLookup**

| Uzmeklēšanas rezultāts         | Līnija | PVN grupa    | Krājumu PVN grupa    | Nodokļa kods (kods) | Nosaukums/vārds, uzvārds                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Iekšzemes              | 1    | VAT_LOCAL          | *Nav tukšs*             | *Nav tukšs*     | Pārdošana                 |
| Iekšzemes              | 2    | VAT_LOCAL          | *Nav tukšs*             | *Nav tukšs*     | SalesCreditNote       |
| Iekšzemes              | 3    | VAT_FINALC         | *Nav tukšs*             | *Nav tukšs*     | Pārdošana                 |
| Iekšzemes              | 4    | VAT_FINALC         | *Nav tukšs*             | *Nav tukšs*     | SalesCreditNote       |
| Iekšzemes              | 5    | VAT_PUBLIO         | *Nav tukšs*             | *Nav tukšs*     | Pārdošana                 |
| Iekšzemes              | 6    | VAT_PUBLIO         | *Nav tukšs*             | *Nav tukšs*     | SalesCreditNote       |
| Eksports                | 7    | VAT_EXPORT         | *Nav tukšs*             | *Nav tukšs*     | Pārdošana                 |
| Eksports                | 8    | VAT_EXPORT         | *Nav tukšs*             | *Nav tukšs*     | SalesCreditNote       |
| Mašīna un aprīkojums | 9    | *Nav tukšs*        | VAT_M&E                 | *Nav tukšs*     | Pārdošana                 |
| Mašīna un aprīkojums | 10.   | *Nav tukšs*        | VAT_M&E                 | *Nav tukšs*     | SalesCreditNote       |
| Mašīnu daļas        | 11.   | *Nav tukšs*        | VAT_PARTS               | *Nav tukšs*     | Pārdošana                 |
| Mašīnu daļas        | 12.   | *Nav tukšs*        | VAT_PARTS               | *Nav tukšs*     | SalesCreditNote       |
| Atbrīvojumi            | 13   | VAT_EXE            | *Nav tukšs*           | *Nav tukšs*     | SaleExempt            |
| Atbrīvojumi            | 14.   | VAT_EXE            | *Nav tukšs*           | *Nav tukšs*     | SalesExemptCreditNote |
| Nav attiecināms        | 15   | *Tukšs*            | *Tukšs*                 | VAT_ADJ         | *Nav tukšs*           |
| Nav attiecināms        | 16   | *Nav tukšs*        | *Nav tukšs*             | *Nav tukšs*     | *Nav tukšs*           |

 **SalesOperationTypeLookup**

| Uzmeklēšanas rezultāts  | Līnija | Krājumu PVN grupa    | Nodokļa kods    | Nosaukums/vārds, uzvārds                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Preces          | 1    | VAT_GOODS               | *Nav tukšs* | Pārdošana                 |
| Preces          | 2    | VAT_GOODS               | *Nav tukšs* | SalesCreditNote       |
| Preces          | 3    | VAT_GOODS               | *Nav tukšs* | SaleExempt            |
| Preces          | 4    | VAT_GOODS               | *Nav tukšs* | SalesExemptCreditNote |
| Pakalpojumi       | 5    | VAT_SERV                | *Nav tukšs* | Pārdošana                 |
| Pakalpojumi       | 6    | VAT_SERV                | *Nav tukšs* | SalesCreditNote       |
| Pakalpojumi       | 7    | VAT_SERV                | *Nav tukšs* | SaleExempt            |
| Pakalpojumi       | 8    | VAT_SERV                | *Nav tukšs* | SalesExemptCreditNote |
| Korekcijas    | 9    | *Tukšs*                 | VAT_ADJ     | Pārdošana                 |
| Korekcijas    | 10.   | *Tukšs*                 | VAT_ADJ     | Pirkšana              |
| Nav attiecināms | 11.   | *Nav tukšs*             | *Nav tukšs* | *Nav tukšs*           |

**PurchaseItemTypeLookup**

| Uzmeklēšanas rezultāts          | Līnija | Krājumu PVN grupa    | Nodokļa kods    | Nosaukums/vārds, uzvārds                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Preces                  | 1    | VAT_GOODS               | *Nav tukšs* | Pirkšana                 |
| Preces                  | 2    | VAT_GOODS               | *Nav tukšs* | PurchaseCreditNote       |
| Pakalpojumi               | 3    | VAT_SERV                | *Nav tukšs* | Pirkšana                 |
| Pakalpojumi               | 4    | VAT_SERV                | *Nav tukšs*  | PurchaseCreditNote       |
| Mašīna un aprīkojums  | 5    | VAT_M&E                 | *Nav tukšs* | Pirkšana                 |
| Mašīna un aprīkojums  | 6    | VAT_M&E                 | *Nav tukšs* | PurchaseCreditNote       |
| Mašīnu daļas         | 7    | VAT_PARTS               | *Nav tukšs* | Pirkšana                 |
| Mašīnu daļas         | 8    | VAT_PARTS               | *Nav tukšs* | PurchaseCreditNote       |
| Atbrīvojumi             | 9    | VAT_EXE                 | *Nav tukšs*  | PurchaseExempt           |
| Atbrīvojumi             | 10.   | VAT_EXE                 | *Nav tukšs* | PurchaseExemptCreditNote |
| Nav attiecināms         | 11.   | *Tukšs*                 | VAT_ADJ     | *Nav tukšs*              |
| Nav attiecināms         | 12.   | *Nav tukšs*             | *Nav tukšs* | *Nav tukšs*              |
| Nav attiecināms         | 13   | *Tukšs*                 | *Nav tukšs* | *Nav tukšs*              |

**PurchaseOperationTypeLookup**

| Uzmeklēšanas rezultāts  | Līnija | PVN grupa  | Nodokļa kods    | Nosaukums/vārds, uzvārds                     |
|----------------|------|------------------|-------------|--------------------------|
| Iekšzemes       | 1    | VAT_LOCAL        | *Nav tukšs* | Pirkšana                 |
| Iekšzemes       | 2    | VAT_LOCAL        | *Nav tukšs* | PurchaseCreditNote       |
| Iekšzemes       | 3    | VAT_LOCAL        | *Nav tukšs* | PurchaseExempt           |
| Iekšzemes       | 4    | VAT_LOCAL        | *Nav tukšs* | PurchaseExemptCreditNote |
| Importēts       | 5    | VAT_IMPORT       | *Nav tukšs* | Pirkšana                 |
| Importēts       | 6    | VAT_IMPORT       | *Nav tukšs* | PurchaseCreditNote       |
| Importēts       | 7    | VAT_IMPORT       | *Nav tukšs* | PurchaseExempt           |
| Importēts       | 8    | VAT_IMPORT       | *Nav tukšs* | PurchaseExemptCreditNote |
| Korekcijas    | 9    | *Tukšs*          | VAT_ADJ     | PurchaseCreditNote       |
| Korekcijas    | 10.   | *Tukšs*          | VAT_ADJ     | Pirkšana                 |
| Nav attiecināms | 11.   | *Nav tukšs*      | *Nav tukšs* | *Nav tukšs*              |

**VATRateTypeLookup**

| Uzmeklēšanas rezultāts  | Līnija | Nodokļa kods (kods) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Nav tukšs*     |
| SecondTable    | 4    | *Nav tukšs*     |
| Nav attiecināms | 5    | *Nav tukšs*     |


## <a name="set-up-general-ledger-parameters"></a>Virsgrāmatas parametru iestatīšana

Lai izveidotu PVN atgriešanas veidlapu Microsoft Excel formātā, definējiet ER formātu lapā **Virsgrāmatas parametri**.

1. Atveriet **Nodoklis** > **Iestatīšana** > **Virsgrāmatas parametri**.
2. Cilnes **PVN** sadaļā **Nodokļu opcijas** laukā **PVN deklarācijas formāta kartēšana** atlasiet **PVN deklarācija Excel (EG)**. Ja šo lauku atstājat tukšu, standarta PVN pārskats tiks ģenerēts SSRS formātā.
3. Atlasiet **Kategoriju hierarhija**. Šī kategorija iespējo preču kodu Ārējās tirdzniecības cilnes darbībās, lai ļautu lietotājiem atlasīt un klasificēt preces un pakalpojumus. Šīs klasifikācijas apraksts ir detalizēts pārdošanas un pirkšanas darījumu pārskatos. Šī konfigurācija nav obligāta.

![Deklarācijas veidlapa](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>Ģenerēt PVN atgriešanas pārskatu
Process, kurā tiek sagatavots un iesniegts PVN atgriešanas pārskats par periodu, ir balstīts uz PVN maksājumu darījumiem, kas tika grāmatoti PVN iegrāmatošanas darba laikā. Plašāku informāciju par PVN iegrāmatošanu un pārskatiem skatiet sadaļā [PVN pārskats](../general-ledger/indirect-taxes-overview.md).

Lai ģenerētu nodokļu deklarācijas pārskatu, veiciet tālāk norādītās darbības.

1. Atveriet **Nodoklis** > **Deklarācijas** > **PVN** > **Sniegt PVN pārskatu par apmaksas periodu** vai **Nosegt un grāmatot PVN**.
2. Atlasiet **Apmaksas periods**.
3. Atlasiet sākuma datumu un pēc tam atlasiet PVN maksājuma versiju.
5. Atlasiet **Labi**. 
6. Ievadiet kredīta summu no iepriekšējā perioda, ja tas ir attiecināms, vai atstājiet summu kā nulli.
7. Laukā **Atskaišu informācija** atlasiet kādu no šādām pieejamām opcijām. 
   - **Pirkšanas PVN grāmata**: ģenerēt detalizētu informāciju par pirkšanas nodokļa darījumu pārskatu.
   - **Pārdošanas PVN grāmata**: ģenerēt detalizētu informāciju par pārdošanas nodokļa darījumu pārskatu.
   - **PVN deklarācija**: ģenerēt tikai PVN deklarācijas atgriešanas veidlapu.
8. Ievadiet tās personas vārdu, kura ir reģistrēta, lai piešķirtu veidlapu.
9. Atlasiet valodu. Visi pārskati tiek tulkoti **en-us** un **ar-eg**.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


