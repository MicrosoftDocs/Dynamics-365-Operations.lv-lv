---
title: "Risinājumā Field Service ietverto līguma rēķinu sinhronizēšana ar brīva teksta rēķiniem risinājumā Finance and Operations"
description: "Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti risinājumā Microsoft Dynamics 365 for Field Service ietverto līguma rēķinu sinhronizēšanai ar brīvā teksta rēķiniem risinājumā Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: lv-lv
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Risinājumā Field Service ietverto līguma rēķinu sinhronizēšana ar brīva teksta rēķiniem risinājumā Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti risinājumā Microsoft Dynamics 365 for Field Service ietverto līguma rēķinu sinhronizēšanai ar brīvā teksta rēķiniem risinājumā Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Field Service ietverto līguma rēķinu sinhronizēšanu ar brīvā teksta rēķiniem risinājumā Finance and Operations.

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Līguma rēķini (no Field Service uz Fin and Ops)

**Uzdevumu nosaukumi datu integrācijas projektā**

- Rēķinu virsraksti
- Rēķina rindas

Lai varētu veikt līguma rēķinu sinhronizāciju, ir nepieciešama tālāk norādītā sinhronizācija.

- Konti (no Sales uz Fin and Ops) — tieši

## <a name="entity-set"></a>Elementu kopa

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| rēķini       | CDS debitora brīva teksta rēķinu virsraksti |
| invoicedetails | CDS debitora brīva teksta rēķinu rindas   |

## <a name="entity-flow"></a>Elementu plūsma

Rēķinus, kas izveidoti no līguma risinājumā Field Service, var sinhronizēt ar risinājumu Finance and Operations, izmantojot Common Data Service (CDS) datu integrācijas projektu. Šo rēķinu atjauninājumi tiks sinhronizēti ar brīvā teksta rēķiniem risinājumā Finance and Operations, ja brīvā teksta rēķinu uzskaites statuss ir **Apstrāde**. Pēc brīvā teksta rēķinu grāmatošanas risinājumā Finance and Operations un pēc uzskaites statusa atjaunināšanas uz **Pabeigts** vairs nav iespējams sinhronizēt atjauninājumus no Field Service.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM

Entītijai **Rēķins** ir pievienots lauks **Ir rindas ar līguma izcelsmi**. Šis lauks palīdz nodrošināt, ka tiek sinhronizēti tikai tie rēķini, kas izveidoti no līguma. Vērtība ir **patiess**, ja rēķinā ir vismaz viena rēķina rinda, kas izveidota no līguma.

Entītijai **Rēķina rinda** ir pievienots lauks **Ir līguma izcelsme**. Šis lauks palīdz nodrošināt, ka tiek sinhronizētas tikai tās rēķina rindas, kas izveidotas no līguma. Vērtība ir **patiess**, ja rēķina rinda izveidota no līguma.

**Rēķina datums** ir obligāts lauks risinājumā Finance and Operations. Tādēļ laukā ir jābūt vērtībai risinājumā Field Service, pirms tiek veikta sinhronizēšana. Lai izpildītu šo prasību, tiek pievienota šāda loģika.

- Ja entītijas **Rēķins** lauks **Rēķina datums** ir tukšs (proti, ja tajā nav vērtības), tajā tiek iestatīts pašreizējais datums, kad tiek pievienota rēķina rinda, kas izveidota no līguma.
- Lietotājs var mainīt lauku **Rēķina datums**. Tomēr, kad lietotājs mēģina saglabāt rēķinu, kas izveidots no līguma, tiek parādīta biznesa procesa kļūda, ja rēķinā ir tukšs lauks **Rēķina datums**.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="in-finance-and-operations"></a>Programmā Finance and Operations

Integrēšanas veikšanai ir jāiestata rēķina izcelsme, lai atšķirtu tādus brīva teksta rēķinus risinājumā Finance and Operations, kuri izveidoti no līguma rēķiniem risinājumā Field Service. Ja rēķina izcelsmes tips ir **Līguma rēķina integrācija**, lauks **Ārējais rēķina numurs** tiek rādīts **Pārdošanas rēķina** virsrakstā.

Papildus parādīšanai rēķina virsrakstā, informāciju **Ārējais rēķina numurs** var izmantot, lai palīdzētu nodrošināt, ka rēķini, kas izveidoti no Field Service līguma rēķiniem, tiek filtrēti, kad risinājumā Finance and Operations ietvertie rēķini tiek sinhronizēti ar Field Service.

1. Atveriet sadaļu **Debitoru parādi** \> **Iestatīšana** \> **Rēķinu izcelsmes kodi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu rēķina izcelsmi.
3. Laukā **Rēķina izcelsme** ievadiet rēķina izcelsmes nosaukumu, piemēram, **FS**.
4. Laukā **Apraksts** ievadiet aprakstu, piemēram, **Field Service līguma rēķins**.
5. Atzīmējiet izvēles rūtiņu **Izcelsmes tipa piešķire**.
6. Laukā **Rēķina izcelsmes tips** iestatiet vērtību **Līguma rēķina integrācija**.
7. Atlasiet **Saglabāt**.

### <a name="in-the-data-integration-project"></a>Datu integrācijas projektā

Uzdevums: **Rēķina rindas**  

Pārliecinieties, ka noklusējuma vērtība Finance and Operations laukā **Galvenā konta parādāmā vērtība** ir atjaunināta atbilstoši vēlamajai vērtībai.

Noklusējuma veidnes vērtība ir **401100**.

