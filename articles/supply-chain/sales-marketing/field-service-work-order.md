---
title: "Risinājumā Field Service ietverto darba pasūtījumu sinhronizācija ar pārdošanas pasūtījumiem risinājumā Finance and Operations"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti risinājumā Field Service ietverto darba pasūtījumu sinhronizēšanai ar pārdošanas pasūtījumiem risinājumā Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 854240bef9d6193c8f0f608687b68e6842fe272c
ms.contentlocale: lv-lv
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>Risinājumā Field Service ietverto darba pasūtījumu sinhronizācija ar pārdošanas pasūtījumiem risinājumā Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti risinājumā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar pārdošanas pasūtījumiem risinājumā Microsoft Dynamics 365 for Finance and Operations.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti risinājumā Field Service ietverto darba pasūtījumu sinhronizēšanai ar pārdošanas pasūtījumiem risinājumā Finance and Operations.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Tālāk minētās veidnes un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Field Service ietverto darba pasūtījumu sinhronizēšanu ar pārdošanas pasūtījumiem risinājumā Finance and Operations.

### <a name="names-of-the-templates-in-data-integration"></a>Veidņu nosaukumi līdzeklī Datu integrācija

Sinhronizēšanai tiek izmantota veidne **Darba pasūtījumi ar pārdošanas pasūtījumiem (no Field Service uz Fin and Ops)**.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Uzdevumu nosaukumi datu integrācijas projektā

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Lai varētu veikt pārdošanas pasūtījumu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.

- Field Service preces (no Fin and Ops uz Field Service)
- Konti (no Sales uz Fin and Ops) — tieši

## <a name="entity-set"></a>Elementu kopa

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS pārdošanas pasūtījumu virsraksti |
| msdyn_workorderservices | CDS pārdošanas pasūtījumu rindas   |
| msdyn_workorderproducts | CDS pārdošanas pasūtījumu rindas   |

## <a name="entity-flow"></a>Elementu plūsma

Darba pasūtījumi tiek izveidoti pakalpojumā Field Service. Ja darba pasūtījumos ir iekļautas tikai ārēji uzturētas preces un ja vērtība **Darba pasūtījuma statuss** atšķiras no vērtības **Atvērts - Neieplānots** un **Slēgts - Atcelts**, darba pasūtījumus var sinhronizēt ar risinājumu Finance and Operations, izmantojot CDS datu integrācijas projektu. Darba pasūtījumu atjauninājumi tiks sinhronizēti kā pārdošanas pasūtījumi risinājumā Finance and Operations. Šie atjauninājumi ietver informāciju par izcelsmes veidu un statusu.

## <a name="estimated-versus-used"></a>Vienumu Novērtēts un Izmantots salīdzinājums

Risinājumā Field Service darba pasūtījumos ietverto preču un pakalpojumu daudzumiem un summām ir gan vērtības **Novērtēts**, gan vērtības **Izmantots**. Tomēr risinājumā Finance and Operations pārdošanas pasūtījumiem netiek izmantota tāda pati vērtību **Novērtēts** un **Izmantots** koncepcija. Lai atbalstītu ražošanas sadalījumu, kas izmanto paredzamo daudzumu pārdošanas pasūtījumā risinājumā Finance and Operations, bet saglabātu izmantoto daudzumu, kas būtu jāpatērē un jāiekļauj rēķinā, divas uzdevumu kopas sinhronizē preces un pakalpojumus darba pasūtījumā. Viena uzdevumu kopa ir paredzēta vērtībām **Novērtēts**, un otra uzdevumus kopa — vērtībām **Izmantots**.

Šāda darbība iespējo scenārijus, kur novērtētās vērtības tiek izmantotas sadalījumam vai rezervācijai risinājumā Finance and Operations, savukārt izmantotās vērtības tiek lietotas patēriņam un rēķinu izrakstīšanai.

### <a name="estimated"></a>Novērtēts

Preču rindu sinhronizācijai vērtības **Novērtēts** tiek izmantotas, ja vienuma **Rindas statuss** vērtība ir **Novērtēts**, opcijai **Sadalīts** ir iestatīts vienums **Jā** un vienuma **Sistēmas statuss** vērtība nav **Slēgts - Iegrāmatots**.

Pakalpojumu rindu sinhronizācijai vērtības **Novērtēts** tiek izmantotas, ja vienuma **Rindas statuss** vērtība ir **Novērtēts** un vienuma **Sistēmas statuss** vērtība nav **Slēgts - Iegrāmatots**.

### <a name="used"></a>Izmantots

Vērtības **Izmantots** tiek izmantotas patēriņam un rēķinu izrakstīšanai. Šajos gadījumos tiek sinhronizētas vērtības **Izmantots**.

Tabulā ir sniegts pārskats par dažādām preču rindu kombinācijām.

| Sistēmas statuss <br>(Field Service) | Rindas statuss <br>(Field Service) | Sadalīts <br>(Field Service) |Sinhronizētā vērtība <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| Atvērts - Ieplānots   | Novērtēts   | Jā       | Novērtēts                       |
| Atvērts - Ieplānots   | Novērtēts   | Nav        | Izmantots                            |
| Atvērts - Ieplānots   | Izmantots        | Jā       | Izmantots                            |
| Atvērts - Ieplānots   | Izmantots        | Nav        | Izmantots                            |
| Atvērts - Notiek izpilde | Novērtēts   | Jā       | Novērtēts                       |
| Atvērts - Notiek izpilde | Novērtēts   | Nav        | Izmantots                            |
| Atvērts - Notiek izpilde | Izmantots        | Jā       | Izmantots                            |
| Atvērts - Notiek izpilde | Izmantots        | Nav        | Izmantots                            |
| Atvērts - Pabeigts   | Novērtēts   | Jā       | Novērtēts                       |
| Atvērts - Pabeigts   | Novērtēts   | Nav        | Izmantots                            |
| Atvērts - Pabeigts   | Izmantots        | Jā       | Izmantots                            |
| Atvērts - Pabeigts   | Izmantots        | Nav        | Izmantots                            |
| Slēgts - Iegrāmatots    | Novērtēts   | Jā       | Izmantots                            |
| Slēgts - Iegrāmatots    | Novērtēts   | Nav        | Izmantots                            |
| Slēgts - Iegrāmatots    | Izmantots        | Jā       | Izmantots                            |
| Slēgts - Iegrāmatots    | Izmantots        | Nav        | Izmantots                            |

Tabulā ir sniegts pārskats par dažādām pakalpojumu rindu kombinācijām.

| Sistēmas statuss <br>(Field Service) | Rindas statuss <br>(Field Service) | Sinhronizētā vērtība <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| Atvērts - Ieplānots   | Novērtēts   | Novērtēts |
| Atvērts - Ieplānots   | Izmantots        | Izmantots      |
| Atvērts - Notiek izpilde | Novērtēts   | Novērtēts |
| Atvērts - Notiek izpilde | Izmantots        | Izmantots      |
| Atvērts - Pabeigts   | Novērtēts   | Novērtēts |
| Atvērts - Pabeigts   | Izmantots        | Izmantots      |
| Slēgts - Iegrāmatots    | Novērtēts   | Izmantots      |
| Slēgts - Iegrāmatots    | Izmantots        | Izmantots      |

Vērtību **Novērtēts** sinhronizācija salīdzinājumā ar vērtībām **Izmantots** tiek pārvaldīta, izmantojot divas uzdevumu kopas preču rindām un pakalpojumu rindām. Iepriekš definēti filtri aktivizē pareizo uzdevumu, un pamata kartēšana palīdz nodrošināt, ka tiek sinhronizētas pareizās vērtības **Paredzēts** vai **Izmantots**.

### <a name="example"></a>Paraugs

1. Darba pasūtījums ir izveidots un plānots risinājumā Field Service.

    Vienuma **Sistēmas statuss** vērtība ir **Atvērts - Ieplānots**.

    - **Preces rinda:** Novērtētais daudzums = 5 gab., Izmantotais daudzums = 0 gab., Rindas statuss = Novērtēts, Sadalīts = Nē
    - **Pakalpojuma rinda:** Novērtētais daudzums = 2 h, Izmantotais daudzums = 0 h, Rindas statuss = Novērtēts

    Šajā piemērā risinājumā Finance and Operations tiek sinhronizēta preces vienuma **Izmantotais daudzums** vērtība **0** (nulle) un pakalpojuma vienuma **Novērtētais daudzums** vērtība **2 h**.

2. Preces tiek sadalītas risinājumā Field Service.

    Vienuma **Sistēmas statuss** vērtība ir **Atvērts - Ieplānots**.

    - **Preces rinda:** Novērtētais daudzums = 5 gab., Izmantotais daudzums = 0 gab., Rindas statuss = Novērtēts, Sadalīts = Jā
    - **Pakalpojuma rinda:** Novērtētais daudzums = 2 h, Izmantotais daudzums = 0 h, Rindas statuss = Novērtēts

    Šajā piemērā risinājumā Finance and Operations tiek sinhronizēta preces vienuma **Novērtētais daudzums** vērtība **0 gab.** un pakalpojuma vienuma **Novērtētais daudzums** vērtība **2 h**.

3. Servisa tehniķis sāk darbu pie darba pasūtījuma un reģistrē izlietotā materiāla vērtību 6.

    Vienuma **Sistēmas statuss** vērtība ir **Atvērts - Notiek izpilde**.

    - **Preces rinda:** Novērtētais daudzums = 5 gab., Izmantotais daudzums = 6 gab., Rindas statuss = Izmantots, Sadalīts = Jā
    - **Pakalpojuma rinda:** Novērtētais daudzums = 2 h, Izmantotais daudzums = 0 h, Rindas statuss = Novērtēts

    Šajā piemērā risinājumā Finance and Operations tiek sinhronizēta preces vienuma **Izmantotais daudzums** vērtība **6** un pakalpojuma vienuma **Novērtētais daudzums** vērtība **2 h**.

4. Servisa tehniķis pabeidz darba pasūtījumu un reģistrē izmantoto laiku 1,5 stundas.

    Vienuma **Sistēmas statuss** vērtība ir **Atvērts - Pabeigts**.

    - **Preces rinda:** Novērtētais daudzums = 5 gab., Izmantotais daudzums = 6 gab., Rindas statuss = Izmantots, Sadalīts = Jā
    - **Pakalpojuma rinda:** Novērtētais daudzums = 2 h, Izmantotais daudzums = 1,5 h, Rindas statuss = Izmantots

    Šajā piemērā risinājumā Finance and Operations tiek sinhronizēta preces vienuma **Izmantotais daudzums** vērtība **6** un pakalpojuma vienuma **Novērtētais daudzums** vērtība **1,5 h**.

## <a name="sales-order-origin-and-status"></a>Pārdošanas pasūtījuma izcelsme un statuss

### <a name="sales-origin"></a>Pasūtījuma izcelsme

Lai sekotu tādiem pārdošanas pasūtījumiem risinājumā Finance and Operations, kuri izveidoti no darba pasūtījumiem, var izveidot pārdošanas izcelsmi, kurai opcijai **Izcelsmes veida piešķire** ir iestatīts vienums **Jā** un laukā **Pārdošanas izcelsmes tips** ir iestatīta vērtība **Darba pasūtījuma integrācija**.

Pēc noklusējuma kartējums atlasa pārdošanas izcelsmi pārdošanas izcelsmes tipam **Darba pasūtījuma integrācija** visiem pārdošanas pasūtījumiem, kas izveidoti no darba pasūtījumiem. Šī darbība var būt noderīga, strādājot ar pārdošanas pasūtījumiem risinājumā Finance and Operations. Jums jāpārliecinās, ka pārdošanas pasūtījumi, kas izveidoti no darba pasūtījumiem, netiek sinhronizēti atpakaļ ar risinājumu Field Service kā darba pasūtījumi.

Papildinformāciju par to, kā izveidot pareizu pārdošanas izcelsmes iestatījumu risinājumā Finance and Operations, skatiet šīs tēmas sadaļā “Priekšnosacījumi un kartējuma iestatījums”.

### <a name="status"></a>Statuss

Ja pārdošanas pasūtījums izveidots no darba pasūtījuma, pārdošanas pasūtījuma galvenes cilnē **Iestatījums** tiek parādīts lauks **Ārējā darba pasūtījuma statuss**. Šajā laukā ir norādīts sistēmas statuss no darba pasūtījuma risinājumā Field Service, lai palīdzētu izsekot pārdošanas pasūtījumu sinhronizēto darba pasūtījumu statusam risinājumā Finance and Operations. Šis lauks arī var palīdzēt risinājuma Finance and Operations lietotājiem noteikt, kad pārdošanas pasūtījums jānosūta vai jāizraksta rēķins.

Laukā **Ārējā darba pasūtījuma statuss** var būt šādas vērtības:

- Atvērts - Ieplānots
- Atvērts - Notiek izpilde
- Atvērts - Pabeigts
- Slēgts - Iegrāmatots

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM

Lai atbalstītu integrāciju starp risinājumiem Field Service un Finance and Operations ir nepieciešama papildu funkcionalitāte no pakalpojuma Field Service CRM. Risinājumā ir ietvertas šādas izmaiņas.

### <a name="work-order-entity"></a>Entītija Darba pasūtījums

Entītijai **Darba pasūtījums** ir pievienots lauks **Tikai ārēji uzturētas preces**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu, vai darba pasūtījumā ir ietvertas tikai ārēji uzturētas preces. Darba pasūtījumā ir ietvertas tikai ārēji uzturētas preces, ja visas saistītās preces tiek uzturētas risinājumā Finance and Operations. Šis lauks palīdz nodrošināt to, ka lietotāji nesinhronizē darba pasūtījumus, kuros ietvertās preces nav zināmas risinājumā Finance and Operations.

### <a name="work-order-product-entity"></a>Entītija Darba pasūtījuma prece

- Entītijai **Darba pasūtījuma prece** ir pievienots lauks **Pasūtījumā ir tikai ārēji uzturētas preces**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu, vai darba pasūtījuma prece tiek uzturēta risinājumā Finance and Operations. Šis lauks palīdz nodrošināt to, ka lietotāji nesinhronizē darba pasūtījumu preces, kuras nav zināmas risinājumā Finance and Operations.
- Entītijai **Darba pasūtījuma prece** ir pievienots lauks **Galvenes sistēmas statuss**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu darba pasūtījuma sistēmas statusu un palīdzētu nodrošināt pareizu filtrēšanu, sinhronizējot darba pasūtījumu preces ar risinājumu Finance and Operations. Iestatot filtrus integrācijas uzdevumos, lauka **Galvenes sistēmas statuss** informācija tiek izmantota arī, lai noteiktu, vai jāsinhronizē novērtētās vai izmantotās vērtības.
- Laukā **Rēķinā iekļautā vienības summa** ir norādīta summa, kas iekļauta rēķinā par faktiski izmantoto vienību. Vērtību aprēķina, dalot vērtību **Kopsumma** ar vērtību **Faktiskais daudzums**. Lauks tiek izmantots integrācijai sistēmās, kuras neatbalsta dažādas vērtības attiecībā uz izmantoto daudzumu un rēķinā iekļauto daudzumu. Šis lauks netiek parādīts lietotāja interfeisā (user interface — UI). 
- Lauks **Rēķinā iekļautā atlaides summa** tiek aprēķināts, pie vērtības **Atlaides summa** pieskaitot vērtības **Rēķinā iekļautā vienības summa** aprēķināšanas noapaļošanas vērtību. Šis lauks tiek izmantots integrācijai un neparādās UI.
- Laukā **Decimālais daudzums** tiek glabāta vērtība no lauka **Daudzums** kā decimālskaitlis. Šis lauks tiek izmantots integrācijai un neparādās UI. 
- Vērtība laukos **Izmantots** tiek atiestatīta uz **0** (nulli), ja darba pasūtījuma preces vienuma **Rindas statuss** vērtība tiek mainīta no **Izmantots** uz **Novērtēts**. Šīs izmaiņas palīdz novērst situācijas, kad kļūdaini ievadīts izmantotais daudzums tiek izmantots sinhronizācijai, ja vienuma **Rindas statuss** vērtība ir **Novērtēts** un vienumam **Sadalīts** ir iestatīta opcija **Nē**.

### <a name="work-order-service-entity"></a>Entītija Darba pasūtījuma pakalpojums

- Entītijai **Darba pasūtījuma pakalpojums** ir pievienots lauks **Pasūtījumā ir tikai ārēji uzturētas preces**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu, vai darba pasūtījuma pakalpojums tiek uzturēts risinājumā Finance and Operations. Šis lauks palīdz nodrošināt to, ka lietotāji nesinhronizē darba pasūtījumu pakalpojumus, kuri nav zināmi risinājumā Finance and Operations.
- Entītijai **Darba pasūtījuma pakalpojums** ir pievienots lauks **Galvenes sistēmas statuss**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu darba pasūtījuma sistēmas statusu un palīdzētu nodrošināt pareizu filtrēšanu, sinhronizējot darba pasūtījumu pakalpojumus ar risinājumu Finance and Operations. Iestatot filtrus integrācijas uzdevumos, lauka **Galvenes sistēmas statuss** informācija tiek izmantota arī, lai noteiktu, vai jāsinhronizē novērtētās vai izmantotās vērtības.
- Laukā **Ilgums stundās** tiek glabāta vērtība no lauka **Ilgums** pēc tam, kad attiecīgā vērtība ir pārveidota no minūtēm stundās. Šis lauks tiek izmantots integrācijai un neparādās UI.
- Laukā **Novērtētais ilgums stundās** tiek glabāta vērtība no lauka **Novērtētais ilgums** pēc tam, kad attiecīgā vērtība ir pārveidota no minūtēm stundās. Šis lauks tiek izmantots integrācijai un neparādās UI.
- Laukā **Rēķinā iekļautā vienības summa** tiek glabāta summa, kas iekļauta rēķinā par faktiski izmantoto vienību. Vērtību aprēķina, dalot vērtību **Kopsumma** ar vērtību **Faktiskais daudzums**. Šis lauks tiek izmantots integrācijai sistēmās, kuras neatbalsta dažādas vērtības attiecībā uz izmantoto daudzumu un rēķinā iekļauto daudzumu. Lauks netiek parādīts UI.
- Lauks **Rēķinā iekļautā atlaides summa** tiek aprēķināts, pie vērtības **Atlaides summa** pieskaitot vērtības **Rēķinā iekļautā vienības summa** aprēķināšanas noapaļošanas vērtību. Šis lauks tiek izmantots integrācijai un neparādās UI.
- Laukā **Ārējās rindas pasūtījums** ir aprēķināts negatīvais rindas pasūtījuma numurs, ko var izmantot ārējās sistēmās, kurās ir apvienotas darba pasūtījumu preču un pakalpojumu rindas. Šis lauks ļauj ievietotajām darba pasūtījuma precēm izmantot pozitīvus rindas numurus un darba pasūtījuma pakalpojumiem izmantot negatīvus rindas numurus. Šī lauka vērtība tiek aprēķināta, reizinot vērtību **Rindas pasūtījums** ar -1. Šis lauks netiek parādīts UI.
- Vērtība laukos **Izmantots** tiek atiestatīta uz **0** (nulli), ja darba pasūtījuma pakalpojuma vienuma **Rindas statuss** vērtība kaut kāda iemesla dēļ tiek mainīta no **Izmantots** uz **Novērtēts**. Šīs izmaiņas palīdz novērst situācijas, kad kļūdaini ievadīts izmantotais daudzums tiek izmantots sinhronizācijai, ja vienuma **Rindas statuss** vērtība ir **Novērtēts** un vienuma **Galvenes sistēmas statuss** vērtība ir **Slēgts - Iegrāmatots**.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms darba pasūtījumu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-field-service"></a>Iestatīšana risinājumā Field Service

- Pārliecinieties, ka numuru sērija, ko izmanto darba pasūtījumiem risinājumā Field Service, nepārklājas ar numuru sēriju, kas izmantota pārdošanas pasūtījumiem risinājumā Finance and Operations. Pretējā gadījumā esošie pārdošanas pasūtījumi var tikt nepareizi atjaunināti risinājumā Field Service vai Finance and Operations.
- Laukā **Darba pasūtījuma rēķina izveide** jābūt iestatītai vērtībai **Nekad**, jo rēķini tiks izrakstīti risinājumā Finance and Operations. Atveriet sadaļu **Field Service** \> **Iestatījumi** \> **Administrēšana** \> **Field Service iestatījumi** un pārliecinieties, ka laukā **Darba pasūtījuma rēķina izveide** ir iestatīta vērtība **Nekad**.

### <a name="setup-in-finance-and-operations"></a>Iestatīšana programmā Finance and Operations

Darba pasūtījumu integrācijai nepieciešams iestatīt pārdošanas izcelsmi. Pārdošanas izcelsme tiek izmantota, lai atšķirtu tādus pārdošanas pasūtījumus risinājumā Finance and Operations, kuri izveidoti no darba pasūtījumiem risinājumā Field Service. Ja pārdošanas pasūtījuma pārdošanas izcelsmes tips ir **Darba pasūtījuma integrācija**, pārdošanas pasūtījuma galvenē tiek parādīts lauks **Ārējā darba pasūtījuma statuss**. Turklāt pārdošanas izcelsme palīdz nodrošināt, ka pārdošanas pasūtījumi, kas izveidoti no darba pasūtījumiem risinājumā Field Service, tiek filtrēti, sinhronizējot risinājumā Finance and Operations esošos pārdošanas pasūtījumus ar risinājumu Field Service.

1. Atveriet sadaļu **Pārdošana un mārketings** \> **Iestatīšana** \> **Pārdošanas pasūtījumi** \> **Pārdošanas izcelsme**.
2. Atlasiet **Jauns**, lai izveidotu jaunu pārdošanas izcelsmi.
3. Laukā **Pārdošanas izcelsme** ievadiet pārdošanas izcelsmes nosaukumu, piemēram, **WorkOrder**.
4. Laukā **Apraksts** ievadiet aprakstu, piemēram, **Field Service darba pasūtījums**.
5. Atzīmējiet izvēles rūtiņu **Izcelsmes tipa piešķire**.
6. Laukā **Pārdošanas izcelsmes tips** iestatiet vērtību **Darba pasūtījuma integrācija**.
7. Atlasiet **Saglabāt**.

### <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

(Drīzumā)
