---
title: Sinhronizējiet līguma rēķinus risinājumā Field Service ar brīva teksta rēķiniem risinājumā Supply Chain Management
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto līgumu rēķinu sinhronizēšanai ar brīva teksta rēķiniem programmā Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/10/2018
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 70f1c072c3a2a1b201aac1f1d2beea9979a3b792
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060768"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Sinhronizējiet līguma rēķinus risinājumā Field Service ar brīva teksta rēķiniem risinājumā Supply Chain Management

[!include[banner](../includes/banner.md)]



Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto līgumu rēķinu sinhronizēšanai ar brīva teksta rēķiniem programmā Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Field Service ietverto līguma rēķinu sinhronizēšanu ar brīvā teksta rēķiniem risinājumā Supply Chain Management.

**Veidnes nosaukums līdzeklī Datu integrācija**

- Līguma rēķini (no Field Service uz Supply Chain Management)

**Uzdevumu nosaukumi datu integrācijas projektā**

- Rēķinu virsraksti
- Rēķina rindas

Lai varētu veikt līguma rēķinu sinhronizāciju, ir nepieciešama tālāk norādītā sinhronizācija.

- Konti (no Sales uz Supply Chain Management) – Tiešā

## <a name="entity-set"></a>Elementu kopa

| Field Service  | Supply Chain Management                 |
|----------------|----------------------------------------|
| rēķini       | Dataverse debitora brīva teksta rēķinu galvenes |
| invoicedetails | Dataverse debitora brīva teksta rēķinu rindas   |

## <a name="entity-flow"></a>Elementu plūsma

Rēķinus, kas ir izveidoti no līguma programmā Field Service, var sinhronizēt ar programmu Supply Chain Management, izmantojot Microsoft Dataverse datu integrācijas projektu. Šo rēķinu atjauninājumi tiks sinhronizēti ar brīvā teksta rēķiniem risinājumā Supply Chain Management, ja brīvā teksta rēķinu uzskaites statuss ir **Apstrāde**. Pēc brīvā teksta rēķinu grāmatošanas risinājumā Supply Chain Management un pēc uzskaites statusa atjaunināšanas uz **Pabeigts** vairs nav iespējams sinhronizēt atjauninājumus no Field Service.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM

Tabulai **Rēķins** ir pievienota kolonna **Ir rindas ar līguma izcelsmi**. Šī kolonna palīdz nodrošināt tikai to rēķinu sinhronizāciju, kas izveidoti no līguma. Vērtība ir **patiess**, ja rēķinā ir vismaz viena rēķina rinda, kas izveidota no līguma.

Tabulai **Rēķina rinda** ir pievienota kolonna **Ir līguma izcelsme**. Šī kolonna palīdz nodrošināt tikai to rēķinu rindu sinhronizāciju, kas izveidotas no līguma. Vērtība ir **patiess**, ja rēķina rinda izveidota no līguma.

**Rēķina datums** ir obligāts lauks risinājumā Supply Chain Management. Tādēļ kolonnā ir jābūt vērtībai risinājumā Field Service, pirms tiek veikta sinhronizēšana. Lai izpildītu šo prasību, tiek pievienota šāda loģika.

- Ja tabulas **Rēķins** kolonna **Rēķina datums** ir tukšs (proti, ja tajā nav vērtības), tajā tiek iestatīts pašreizējais datums, kad tiek pievienota rēķina rinda, kas izveidota no līguma.
- Lietotājs var mainīt kolonnu **Rēķina datums**. Tomēr, kad lietotājs mēģina saglabāt rēķinu, kas izveidots no līguma, tiek parādīta biznesa procesa kļūda, ja rēķinā ir tukša kolonna **Rēķina datums**.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="in-supply-chain-management"></a>Supply Chain Management

Integrēšanas veikšanai ir jāiestata rēķina izcelsme, lai atšķirtu tādus brīva teksta rēķinus risinājumā Supply Chain Management, kuri izveidoti no līguma rēķiniem risinājumā Field Service. Ja rēķina izcelsmes tips ir **Līguma rēķina integrācija**, lauks **Ārējais rēķina numurs** tiek rādīts **Pārdošanas rēķina** virsrakstā.

Papildus parādīšanai rēķina virsrakstā, informāciju **Ārējais rēķina numurs** var izmantot, lai palīdzētu nodrošināt, ka rēķini, kas izveidoti no Field Service līguma rēķiniem, tiek filtrēti, kad risinājumā Supply Chain Management ietvertie rēķini tiek sinhronizēti ar Field Service.

1. Atveriet sadaļu **Debitoru parādi** \> **Iestatīšana** \> **Rēķinu izcelsmes kodi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu rēķina izcelsmi.
3. Laukā **Rēķina izcelsme** ievadiet rēķina izcelsmes nosaukumu, piemēram, **FS**.
4. Laukā **Apraksts** ievadiet aprakstu, piemēram, **Field Service līguma rēķins**.
5. Atzīmējiet izvēles rūtiņu **Izcelsmes tipa piešķire**.
6. Laukā **Rēķina izcelsmes tips** iestatiet vērtību **Līguma rēķina integrācija**.
7. Atlasiet **Saglabāt**.

### <a name="in-the-data-integration-project"></a>Datu integrācijas projektā

Uzdevums: **Rēķina rindas**  

Pārliecinieties, ka noklusējuma vērtība Supply Chain Management laukā **Galvenā konta parādāmā vērtība** ir atjaunināta atbilstoši vēlamajai vērtībai.

Noklusējuma veidnes vērtība ir **401100**.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Līguma rēķini (no Field Service uz Supply Chain Management): Rēķinu galvenes

[![Veidņu kartēšana Rēķinu virsrakstu datu integrācijā.](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Līguma rēķini (no Field Service uz Supply Chain Management): Rēķinu rindas

[![Veidņu kartēšana Rēķinu rindu datu integrācijā.](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]