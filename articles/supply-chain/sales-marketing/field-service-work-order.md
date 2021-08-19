---
title: Sinhronizējiet darba pasūtījumus risinājumā Field Service ar pārdošanas pasūtījumiem risinājumā Supply Chain Management
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti risinājumā Field Service ietverto darba pasūtījumu sinhronizēšanai ar pārdošanas pasūtījumiem risinājumā Supply Chain Management.
author: ChristianRytt
ms.date: 04/09/2018
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
ms.openlocfilehash: 7d7688e757a3ab9746ae0307a7c15f0624c1d8aceeb0dc935b0da32d3ab2994b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752686"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>Sinhronizējiet darba pasūtījumus risinājumā Field Service ar pārdošanas pasūtījumiem risinājumā Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto darba pasūtījumu sinhronizēšanai ar pārdošanas pasūtījumiem programmā Dynamics 365 Supply Chain Management.

[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Tālāk minētās veidnes un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Field Service ietverto darba pasūtījumu sinhronizēšanu ar pārdošanas pasūtījumiem risinājumā Supply Chain Management.

### <a name="names-of-the-templates-in-data-integration"></a>Veidņu nosaukumi līdzeklī Datu integrācija

Sinhronizēšanai tiek izmantota veidne **Darba pasūtījumi ar pārdošanas pasūtījumiem (no Field Service uz Supply Chain Management)**.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Uzdevumu nosaukumi datu integrācijas projektā

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Lai varētu veikt pārdošanas pasūtījumu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.

- Field Service preces (no Supply Chain Management uz Field Service)
- Konti (no Sales uz Supply Chain Management) – Tiešā

## <a name="entity-set"></a>Elementu kopa

| **Field Service** | **Supply Chain Management** |
|-------------------------|-------------------------|
| msdyn_workorders        | Dataverse Pārdošanas pasūtījumu galvenes |
| msdyn_workorderservices | Dataverse pārdošanas pasūtījumu rindas   |
| msdyn_workorderproducts | Dataverse pārdošanas pasūtījumu rindas   |

## <a name="entity-flow"></a>Elementu plūsma

Darba pasūtījumi tiek izveidoti pakalpojumā Field Service. Ja darba pasūtījumos ir iekļautas tikai ārēji uzturētas preces un ja vērtība **Darba pasūtījuma statuss** atšķiras no vērtības **Atvērts - Neieplānots** un **Slēgts - Atcelts**, darba pasūtījumus var sinhronizēt ar risinājumu Supply Chain Management, izmantojot Microsoft Dataverse datu integrācijas projektu. Darba pasūtījumu atjauninājumi tiks sinhronizēti kā pārdošanas pasūtījumi risinājumā Supply Chain Management. Šie atjauninājumi ietver informāciju par izcelsmes veidu un statusu.

## <a name="estimated-versus-used"></a>Vienumu Novērtēts un Izmantots salīdzinājums

Risinājumā Field Service darba pasūtījumos ietverto preču un pakalpojumu daudzumiem un summām ir gan vērtības **Novērtēts**, gan vērtības **Izmantots**. Tomēr risinājumā Supply Chain Management pārdošanas pasūtījumiem netiek izmantota tāda pati vērtību **Novērtēts** un **Izmantots** koncepcija. Lai atbalstītu ražošanas sadalījumu, kas izmanto paredzamo daudzumu pārdošanas pasūtījumā risinājumā Supply Chain Management, bet saglabātu izmantoto daudzumu, kas būtu jāpatērē un jāiekļauj rēķinā, divas uzdevumu kopas sinhronizē preces un pakalpojumus darba pasūtījumā. Viena uzdevumu kopa ir paredzēta vērtībām **Novērtēts**, un otra uzdevumus kopa — vērtībām **Izmantots**.

Šāda darbība iespējo scenārijus, kur novērtētās vērtības tiek izmantotas sadalījumam vai rezervācijai risinājumā Supply Chain Management, savukārt izmantotās vērtības tiek lietotas patēriņam un rēķinu izrakstīšanai.

### <a name="estimated"></a>Novērtēts

Preču rindu sinhronizācijai vērtības **Novērtēts** tiek izmantotas, ja vienuma **Rindas statuss** vērtība ir **Novērtēts**, opcijai **Sadalīts** ir iestatīts vienums **Jā** un vienuma **Sistēmas statuss** vērtība nav **Slēgts - Iegrāmatots**.

Pakalpojumu rindu sinhronizācijai vērtības **Novērtēts** tiek izmantotas, ja vienuma **Rindas statuss** vērtība ir **Novērtēts** un vienuma **Sistēmas statuss** vērtība nav **Slēgts - Iegrāmatots**.

### <a name="used"></a>Izmantots

Vērtības **Izmantots** tiek izmantotas patēriņam un rēķinu izrakstīšanai. Šajos gadījumos tiek sinhronizētas vērtības **Izmantots**.

Tabulā ir sniegts pārskats par dažādām preču rindu kombinācijām.

| Sistēmas statuss <br>(Field Service) | Rindas statuss <br>(Field Service) | Sadalīts <br>(Field Service) |Sinhronizētā vērtība <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| Atvērts - Ieplānots   | Novērtēts   | Jā       | Novērtēts                       |
| Atvērts - Ieplānots   | Novērtēts   | Nē        | Izmantots                            |
| Atvērts - Ieplānots   | Izmantots        | Jā       | Izmantots                            |
| Atvērts - Ieplānots   | Izmantots        | Nē        | Izmantots                            |
| Atvērts - Notiek izpilde | Novērtēts   | Jā       | Novērtēts                       |
| Atvērts - Notiek izpilde | Novērtēts   | Nē        | Izmantots                            |
| Atvērts - Notiek izpilde | Izmantots        | Jā       | Izmantots                            |
| Atvērts - Notiek izpilde | Izmantots        | Nē        | Izmantots                            |
| Atvērts - Pabeigts   | Novērtēts   | Jā       | Novērtēts                       |
| Atvērts - Pabeigts   | Novērtēts   | Nē        | Izmantots                            |
| Atvērts - Pabeigts   | Izmantots        | Jā       | Izmantots                            |
| Atvērts - Pabeigts   | Izmantots        | Nē        | Izmantots                            |
| Slēgts - Iegrāmatots    | Novērtēts   | Jā       | Izmantots                            |
| Slēgts - Iegrāmatots    | Novērtēts   | Nē        | Izmantots                            |
| Slēgts - Iegrāmatots    | Izmantots        | Jā       | Izmantots                            |
| Slēgts - Iegrāmatots    | Izmantots        | Nē        | Izmantots                            |

Tabulā ir sniegts pārskats par dažādām pakalpojumu rindu kombinācijām.

| Sistēmas statuss <br>(Field Service) | Rindas statuss <br>(Field Service) | Sinhronizētā vērtība <br>(Supply Chain Management) |
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

### <a name="example"></a>Piemērs

1. Darba pasūtījums ir izveidots un plānots risinājumā Field Service.

    Vienuma **Sistēmas statuss** vērtība ir **Atvērts - Ieplānots**.

    - **Preces rinda:** Novērtētais daudzums = 5 gab., Izmantotais daudzums = 0 gab., Rindas statuss = Novērtēts, Sadalīts = Nē
    - **Pakalpojuma rinda:** Novērtētais daudzums = 2 h, Izmantotais daudzums = 0 h, Rindas statuss = Novērtēts

    Šajā piemērā risinājumā Supply Chain Management tiek sinhronizēta preces vienuma **Izmantotais daudzums** vērtība **0** (nulle) un pakalpojuma vienuma **Novērtētais daudzums** vērtība **2 h**.

2. Preces tiek sadalītas risinājumā Field Service.

    Vienuma **Sistēmas statuss** vērtība ir **Atvērts - Ieplānots**.

    - **Preces rinda:** Novērtētais daudzums = 5 gab., Izmantotais daudzums = 0 gab., Rindas statuss = Novērtēts, Sadalīts = Jā
    - **Pakalpojuma rinda:** Novērtētais daudzums = 2 h, Izmantotais daudzums = 0 h, Rindas statuss = Novērtēts

    Šajā piemērā risinājumā Supply Chain Management tiek sinhronizēta preces vienuma **Novērtētais daudzums** vērtība **5ea** un pakalpojuma vienuma **Novērtētais daudzums** vērtība **2 h**.

3. Servisa tehniķis sāk darbu pie darba pasūtījuma un reģistrē izlietotā materiāla vērtību 6.

    Vienuma **Sistēmas statuss** vērtība ir **Atvērts - Notiek izpilde**.

    - **Preces rinda:** Novērtētais daudzums = 5 gab., Izmantotais daudzums = 6 gab., Rindas statuss = Izmantots, Sadalīts = Jā
    - **Pakalpojuma rinda:** Novērtētais daudzums = 2 h, Izmantotais daudzums = 0 h, Rindas statuss = Novērtēts

    Šajā piemērā risinājumā Supply Chain Management tiek sinhronizēta preces vienuma **Izmantotais daudzums** vērtība **6** un pakalpojuma vienuma **Novērtētais daudzums** vērtība **2 h**.

4. Servisa tehniķis pabeidz darba pasūtījumu un reģistrē izmantoto laiku 1,5 stundas.

    Vienuma **Sistēmas statuss** vērtība ir **Atvērts - Pabeigts**.

    - **Preces rinda:** Novērtētais daudzums = 5 gab., Izmantotais daudzums = 6 gab., Rindas statuss = Izmantots, Sadalīts = Jā
    - **Pakalpojuma rinda:** Novērtētais daudzums = 2 h, Izmantotais daudzums = 1,5 h, Rindas statuss = Izmantots

    Šajā piemērā programmā Supply Chain Management tiek sinhronizēta preces vienuma **Izmantotais daudzums** vērtība **6** un pakalpojuma vienuma **Izmantotais daudzums** vērtība **1,5 h**.

## <a name="sales-order-origin-and-status"></a>Pārdošanas pasūtījuma izcelsme un statuss

### <a name="sales-origin"></a>Pasūtījuma izcelsme

Lai sekotu tādiem pārdošanas pasūtījumiem, kuri izveidoti no darba pasūtījumiem, var izveidot pārdošanas izcelsmi, kurai opcijai **Izcelsmes veida piešķire** ir iestatīts vienums **Jā** un laukā **Pārdošanas izcelsmes tips** ir iestatīta vērtība **Darba pasūtījuma integrācija**.

Pēc noklusējuma kartējums atlasa pārdošanas izcelsmi pārdošanas izcelsmes tipam **Darba pasūtījuma integrācija** visiem pārdošanas pasūtījumiem, kas izveidoti no darba pasūtījumiem. Šī darbība var būt noderīga, strādājot ar pārdošanas pasūtījumiem risinājumā Supply Chain Management. Jums jāpārliecinās, ka pārdošanas pasūtījumi, kas izveidoti no darba pasūtījumiem, netiek sinhronizēti atpakaļ ar risinājumu Field Service kā darba pasūtījumi.

Papildinformāciju par to, kā izveidot pareizu pārdošanas izcelsmes iestatījumu risinājumā Supply Chain Management, skatiet šīs tēmas sadaļā “Priekšnosacījumi un kartējuma iestatījums”.

### <a name="status"></a>Statuss

Ja pārdošanas pasūtījums izveidots no darba pasūtījuma, pārdošanas pasūtījuma galvenes cilnē **Iestatījums** tiek parādīts lauks **Ārējā darba pasūtījuma statuss**. Šajā laukā ir norādīts sistēmas statuss no darba pasūtījuma risinājumā Field Service, lai palīdzētu izsekot pārdošanas pasūtījumu sinhronizēto darba pasūtījumu statusam risinājumā Supply Chain Management. Šis lauks arī var palīdzēt lietotājiem noteikt, kad pārdošanas pasūtījums jānosūta vai jāizraksta rēķins.

Laukā **Ārējā darba pasūtījuma statuss** var būt šādas vērtības:

- Atvērts - Ieplānots
- Atvērts - Notiek izpilde
- Atvērts - Pabeigts
- Slēgts - Iegrāmatots

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM

Lai atbalstītu integrāciju starp risinājumiem Field Service un Supply Chain Management ir nepieciešama papildu funkcionalitāte no pakalpojuma Field Service CRM. Risinājumā ir ietvertas šādas izmaiņas.

### <a name="work-order-entity"></a>Entītija Darba pasūtījums

Entītijai **Darba pasūtījums** ir pievienots lauks **Tikai ārēji uzturētas preces**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu, vai darba pasūtījumā ir ietvertas tikai ārēji uzturētas preces. Darba pasūtījumā ir ietvertas tikai ārēji uzturētas preces, ja visas saistītās preces tiek uzturētas risinājumā Supply Chain Management. Šis lauks palīdz nodrošināt to, ka lietotāji nesinhronizē darba pasūtījumus, kuros ietvertās preces nav zināmas.

### <a name="work-order-product-entity"></a>Entītija Darba pasūtījuma prece

- Entītijai **Darba pasūtījuma prece** ir pievienots lauks **Pasūtījumā ir tikai ārēji uzturētas preces**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu, vai darba pasūtījuma prece tiek uzturēta risinājumā Supply Chain Management. Šis lauks palīdz nodrošināt to, ka lietotāji nesinhronizē darba pasūtījumu preces, kuras nav zināmas risinājumā Supply Chain Management.
- Entītijai **Darba pasūtījuma prece** ir pievienots lauks **Galvenes sistēmas statuss**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu darba pasūtījuma sistēmas statusu un palīdzētu nodrošināt pareizu filtrēšanu, sinhronizējot darba pasūtījumu preces ar risinājumu Supply Chain Management. Iestatot filtrus integrācijas uzdevumos, lauka **Galvenes sistēmas statuss** informācija tiek izmantota arī, lai noteiktu, vai jāsinhronizē novērtētās vai izmantotās vērtības.
- Laukā **Rēķinā iekļautā vienības summa** ir norādīta summa, kas iekļauta rēķinā par faktiski izmantoto vienību. Vērtību aprēķina, dalot vērtību **Kopsumma** ar vērtību **Faktiskais daudzums**. Lauks tiek izmantots integrācijai sistēmās, kuras neatbalsta dažādas vērtības attiecībā uz izmantoto daudzumu un rēķinā iekļauto daudzumu. Šis lauks netiek parādīts lietotāja interfeisā (user interface — UI). 
- Lauks **Rēķinā iekļautā atlaides summa** tiek aprēķināts, pie vērtības **Atlaides summa** pieskaitot vērtības **Rēķinā iekļautā vienības summa** aprēķināšanas noapaļošanas vērtību. Šis lauks tiek izmantots integrācijai un neparādās UI.
- Laukā **Decimālais daudzums** tiek glabāta vērtība no lauka **Daudzums** kā decimālskaitlis. Šis lauks tiek izmantots integrācijai un neparādās UI. 
- Vērtība laukos **Izmantots** tiek atiestatīta uz **0** (nulli), ja darba pasūtījuma preces vienuma **Rindas statuss** vērtība tiek mainīta no **Izmantots** uz **Novērtēts**. Šīs izmaiņas palīdz novērst situācijas, kad kļūdaini ievadīts izmantotais daudzums tiek izmantots sinhronizācijai, ja vienuma **Rindas statuss** vērtība ir **Novērtēts** un vienumam **Sadalīts** ir iestatīta opcija **Nē**.

### <a name="work-order-service-entity"></a>Entītija Darba pasūtījuma pakalpojums

- Entītijai **Darba pasūtījuma pakalpojums** ir pievienots lauks **Pasūtījumā ir tikai ārēji uzturētas preces**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu, vai darba pasūtījuma serviss tiek uzturēta risinājumā Supply Chain Management. Šis lauks palīdz nodrošināt to, ka lietotāji nesinhronizē darba pasūtījumu servisi, kuras nav zināmas risinājumā Supply Chain Management.
- Entītijai **Darba pasūtījuma pakalpojums** ir pievienots lauks **Galvenes sistēmas statuss**, un tas tiek parādīts lapā. Tas tiek izmantots, lai pastāvīgi izsekotu darba pasūtījuma sistēmas statusu un palīdzētu nodrošināt pareizu filtrēšanu, sinhronizējot darba pasūtījumu servisi ar risinājumu Supply Chain Management. Iestatot filtrus integrācijas uzdevumos, lauka **Galvenes sistēmas statuss** informācija tiek izmantota arī, lai noteiktu, vai jāsinhronizē novērtētās vai izmantotās vērtības.
- Laukā **Ilgums stundās** tiek glabāta vērtība no lauka **Ilgums** pēc tam, kad attiecīgā vērtība ir pārveidota no minūtēm stundās. Šis lauks tiek izmantots integrācijai un neparādās UI.
- Laukā **Novērtētais ilgums stundās** tiek glabāta vērtība no lauka **Novērtētais ilgums** pēc tam, kad attiecīgā vērtība ir pārveidota no minūtēm stundās. Šis lauks tiek izmantots integrācijai un neparādās UI.
- Laukā **Rēķinā iekļautā vienības summa** tiek glabāta summa, kas iekļauta rēķinā par faktiski izmantoto vienību. Vērtību aprēķina, dalot vērtību **Kopsumma** ar vērtību **Faktiskais daudzums**. Šis lauks tiek izmantots integrācijai sistēmās, kuras neatbalsta dažādas vērtības attiecībā uz izmantoto daudzumu un rēķinā iekļauto daudzumu. Lauks netiek parādīts UI.
- Lauks **Rēķinā iekļautā atlaides summa** tiek aprēķināts, pie vērtības **Atlaides summa** pieskaitot vērtības **Rēķinā iekļautā vienības summa** aprēķināšanas noapaļošanas vērtību. Šis lauks tiek izmantots integrācijai un neparādās UI.
- Laukā **Ārējās rindas pasūtījums** ir aprēķināts negatīvais rindas pasūtījuma numurs, ko var izmantot ārējās sistēmās, kurās ir apvienotas darba pasūtījumu preču un pakalpojumu rindas. Šis lauks ļauj ievietotajām darba pasūtījuma precēm izmantot pozitīvus rindas numurus un darba pasūtījuma pakalpojumiem izmantot negatīvus rindas numurus. Šī lauka vērtība tiek aprēķināta, reizinot vērtību **Rindas pasūtījums** ar -1. Šis lauks netiek parādīts UI.
- Vērtība laukos **Izmantots** tiek atiestatīta uz **0** (nulli), ja darba pasūtījuma pakalpojuma vienuma **Rindas statuss** vērtība kaut kāda iemesla dēļ tiek mainīta no **Izmantots** uz **Novērtēts**. Šīs izmaiņas palīdz novērst situācijas, kad kļūdaini ievadīts izmantotais daudzums tiek izmantots sinhronizācijai, ja vienuma **Rindas statuss** vērtība ir **Novērtēts** un vienuma **Galvenes sistēmas statuss** vērtība ir **Slēgts - Iegrāmatots**.

## <a name="preconditions-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms darba pasūtījumu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.

### <a name="setup-in-field-service"></a>Iestatīšana risinājumā Field Service

- Pārliecinieties, ka numuru sērija, ko izmanto darba pasūtījumiem risinājumā Field Service, nepārklājas ar numuru sēriju, kas izmantota pārdošanas pasūtījumiem risinājumā Supply Chain Management. Pretējā gadījumā esošie pārdošanas pasūtījumi var tikt nepareizi atjaunināti risinājumā Field Service vai Supply Chain Management.
- Laukā **Darba pasūtījuma rēķina izveide** jābūt iestatītai vērtībai **Nekad**, jo rēķini tiks izrakstīti risinājumā Supply Chain Management. Atveriet sadaļu **Field Service** \> **Iestatījumi** \> **Administrēšana** \> **Field Service iestatījumi** un pārliecinieties, ka laukā **Darba pasūtījuma rēķina izveide** ir iestatīta vērtība **Nekad**.

### <a name="setup-in-supply-chain-management"></a>Supply Chain Management iestatīšana

Darba pasūtījumu integrācijai nepieciešams iestatīt pārdošanas izcelsmi. Pārdošanas izcelsme tiek izmantota, lai atšķirtu tādus pārdošanas pasūtījumus risinājumā Supply Chain Management, kuri izveidoti no darba pasūtījumiem risinājumā Field Service. Ja pārdošanas pasūtījuma pārdošanas izcelsmes tips ir **Darba pasūtījuma integrācija**, pārdošanas pasūtījuma galvenē tiek parādīts lauks **Ārējā darba pasūtījuma statuss**. Turklāt pārdošanas izcelsme palīdz nodrošināt, ka pārdošanas pasūtījumi, kas izveidoti no darba pasūtījumiem risinājumā Field Service, tiek filtrēti, sinhronizējot risinājumā Supply Chain Management esošos pārdošanas pasūtījumus ar risinājumu Field Service.

1. Atveriet sadaļu **Pārdošana un mārketings** \> **Iestatīšana** \> **Pārdošanas pasūtījumi** \> **Pārdošanas izcelsme**.
2. Atlasiet **Jauns**, lai izveidotu jaunu pārdošanas izcelsmi.
3. Laukā **Pārdošanas izcelsme** ievadiet pārdošanas izcelsmes nosaukumu, piemēram, **WorkOrder**.
4. Laukā **Apraksts** ievadiet aprakstu, piemēram, **Field Service darba pasūtījums**.
5. Atzīmējiet izvēles rūtiņu **Izcelsmes tipa piešķire**.
6. Laukā **Pārdošanas izcelsmes tips** iestatiet vērtību **Darba pasūtījuma integrācija**.
7. Atlasiet **Saglabāt**.


### <a name="setup-in-data-integration"></a>Datu integrācijas iestatīšana

Pārliecinieties, ka pastāv **Integrācijas atslēga** entītijai **msdyn_workorders**
1. Atveriet sadaļu Datu integrācija
2. Atlasiet cilni **Savienojumu kopa**
3. Atlasiet savienojumu kopu, kas tiek izmantota darba pasūtījumu sinhronizācijai.
4. Atlasiet cilni **Integrācijas atslēga**
5. Atrodiet msdyn_workorders un pārbaudiet, vai atslēga **msdyn_name (darba pasūtījuma numurs)** ir pievienota. Ja tā nav redzama, pievienojiet to, noklikšķinot uz **Pievienot atslēgu**, un noklikšķiniet uz **Saglabāt** lapas augšpusē

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>No darba pasūtījumiem uz pārdošanas pasūtījumiem (no Field Service uz Supply Chain Management): DarbaPasūtījumaGalvene

Filtrs: (msdyn_systemstatus ne 690970005) un (msdyn_systemstatus ne 690970000), un (msdynce_hasexternallymaintainedproductsonly eq true)

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>No darba pasūtījumiem uz pārdošanas pasūtījumiem (no Field Service uz Supply Chain Management): DarbaPasūtījumaServisaRindasNovērtējums

Filtrs: (msdynce_headersystemstatus ne 690970005) un (msdynce_headersystemstatus ne 690970000), un (msdynce_orderhasexternalmaintainedproductsonly eq true), un (msdyn_linestatus eq 690970000), un (msdynce_headersystemstatus ne 690970004)

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>No darba pasūtījumiem uz pārdošanas pasūtījumiem (no Field Service uz Supply Chain Management): DarbaPasūtījumaServisaIzmantotaRinda

Filtrs: (msdynce_headersystemstatus ne 690970005) un (msdynce_headersystemstatus ne 690970000), un (msdynce_orderhasexternalmaintainedproductsonly eq true), un ((msdyn_linestatus eq 690970001), vai (msdynce_headersystemstatus eq 690970004))

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>No darba pasūtījumiem uz pārdošanas pasūtījumiem (no Field Service uz Supply Chain Management): DarbaPasūtījumaProduktaRindasNovērtējums

Filtrs: (msdynce_headersystemstatus ne 690970005) un (msdynce_headersystemstatus ne 690970000), un (msdynce_orderhasexternalmaintainedproductsonly eq true), un (msdyn_linestatus eq 690970000), un (msdynce_headersystemstatus ne 690970004), un (msdyn_allocated eq true)

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>No darba pasūtījumiem uz pārdošanas pasūtījumiem (no Field Service uz Supply Chain Management): DarbaPasūtījumaProduktaIzmantotaRinda

Filtrs: (msdynce_headersystemstatus ne 690970005) un (msdynce_headersystemstatus ne 690970000), un (msdynce_orderhasexternalmaintainedproductsonly eq true), un ((msdyn_linestatus eq 690970001), vai (msdynce_headersystemstatus eq 690970004), vai (msdyn_allocated ne true))

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]