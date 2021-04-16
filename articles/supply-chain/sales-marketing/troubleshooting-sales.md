---
title: Pārdošanas pasūtījumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas pasūtījumiem.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b5389b0d5a8ff68a3c16dedd2d8bb62f6e99af4f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824730"
---
# <a name="troubleshoot-sales-orders"></a>Pārdošanas pasūtījumu problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas pasūtījumiem.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Mainot pārdošanas pasūtījuma galvenē norādīto atrašanās vietu, nodokļu informācija netiek atjaunināta.

### <a name="issue-description"></a>Problēmas apraksts

Ja vieta, noliktava vai piegādes adrese tiek izmainīta pārdošanas pasūtījuma galvenes vai rindas līmenī, šo rindu nodokļu informācija netiek automātiski atjaunināta.

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku. Problēma rodas, ja piegādes adrese, vieta un noliktava netiek automātiski mainīta rindas līmenī. Tās ir jāatjaunina manuāli.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Ja vienam periodam vai periodiem, kas pārklājas, ir divi tirdzniecības līgumi, vienmēr tiek atlasīta viena un tā pati līguma rinda.

### <a name="issue-description"></a>Problēmas apraksts

Ja divi tirdzniecības līgumi ir definēti vienam periodam vai periodiem, kas pārklājas, viens un tas pats tirdzniecības līgums tiek atlasīts katru reizi, kad izveidojat pārdošanas pasūtījuma rindas, kurās ir ietverti šie vienumi.

### <a name="issue-resolution"></a>Problēmas risinājums

Ja noteiktam datumam ir vairāk nekā viens tirdzniecības līgums, vienmēr tiek atlasīts tirdzniecības līgums ar zemāko cenu. Lai iegūtu papildinformāciju, lejupielādējiet šādu tehnisko dokumentu: [Tirdzniecības līgumi programmā Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Vai var saistīt pirkšanas pasūtījumu ar pārdošanas pasūtījumu, lai izpildītu pieprasījumu?

Pirkšanas pasūtījumu varat izveidot no pārdošanas pasūtījuma. Papildinformāciju skatiet sadaļā [Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Nevar atcelt vai dzēst atgriešanas pasūtījumu vai pārdošanas pasūtījumu.

Varat atcelt tikai tos pārdošanas pasūtījumus un atgriešanas pasūtījumus, kas ir ar statusu *Izveidots*. Papildinformāciju skatiet sadaļā [Atgriešanas pasūtījuma atcelšana](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Mēģinot atcelt pārdošanas pasūtījumu, tiek atgriezta kļūda “Rezervācijas nevar noņemt, jo ir izveidots darbs, kas balstās uz rezervāciju”.

Kļūdas kods: WAX4661

Ja darbs ir saistīts ar pārdošanas pasūtījumu, jūs nevarat atcelt pārdošanas pasūtījumu, kamēr nav atcelts un atsaukts darbs. Šī prasība ir spēkā pat tad, ja ar pārdošanas pasūtījumu saistītais darbs ir slēgts.

Lai novērstu šo problēmu, izpildiet sekojošās darbības.

1. Atceliet darbu un ievietojiet krājumu atpakaļ vēlamajā novietojumā. Dodieties uz atbilstošo pārdošanas pasūtījuma noslodzi un atlasiet **Samazināt izdoto daudzumu** kravas rindā vai **Atsaukt darbu** darbību rūtī.

    Darbs tagad ir ar statusu *Atcelts* un jauns krājumu pārvietošanas darbs tiek automātiski izveidots un apstrādāts, lai ievietotu krājumus atpakaļ novietojumā, kas tika aprakstīts atsaukšanas laikā.

2. Dzēsiet noslodzi. Tiek dzēsts arī sūtījums.
3. Tagad varēsit doties uz pārdošanas pasūtījumu un to atcelt.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Nevar atcelt starpuzņēmumu pirkšanas pasūtījumu, kas ir saistīts ar pārdošanas pasūtījumu.

### <a name="issue-description"></a>Problēmas apraksts

Mēģinot atcelt starpuzņēmumu pirkšanas pasūtījumu, kas ir saistīts ar pārdošanas pasūtījumu, var tikt parādīts šāds kļūdas ziņojums: “Daudzumu nevar samazināt, jo atlikušais atjaunināšanas daudzums maina zīmi.”

### <a name="issue-resolution"></a>Problēmas risinājums

Šī problēma tika novērsta Microsoft Dynamics 365 Supply Chain Management versijā 10.0.13. Šajā un jaunākās versijās tagad varat atcelt starpuzņēmumu pirkšanas pasūtījumu, kas ir saistīts ar pārdošanas pasūtījumu.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Vai var atjaunot rēķinā iekļauto pārdošanas pasūtījumu, kas tika dzēsts?

### <a name="issue-description"></a>Problēmas apraksts

Rēķinā iekļautais pārdošanas pasūtījums tika dzēsts kļūdas dēļ, un jūs vēlaties to atjaunot vai skatīt tā detalizētu informāciju.

### <a name="issue-resolution"></a>Problēmas risinājums

Ja dzēstais pārdošanas pasūtījums jau ir iekļauts rēķinā, dodieties uz **Debitora konts \> Transakcijas \> Oriģinālais dokuments \> Skatīt detalizētu informāciju**. Atrodiet meklēto rēķinu un atlasiet to, lai skatītu tā detalizētu informāciju. Šīs informācija ietver pārdošanas pasūtījuma atsauci. Pārdošanas pasūtījuma informācijai var piekļūt arī no šīs lapas.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Pārdošanas pasūtījuma izpildes termiņa galveni nevar atrast SalesOrderHeaderV2Entity datu elementā.

Elementā *SalesOrderHeaderV2Entity* nav izpildes termiņa lauka.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Nepieciešams dzēst nošķirtos pārdošanas pasūtījumu ierakstus.

Lai notīrītu nošķirtos pārdošanas pasūtījumu ierakstus, palaidiet periodisko uzdevumu *Pārdošanas pasūtījumu dzēšana*, dodoties uz vienu no šīm vietām:

- Pārdošana un mārketings \> Periodiskie uzdevumi \> Tīrīt \> Dzēst pārdošanas pasūtījumus
- Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Tīrīt \> Dzēst pārdošanas pasūtījumus

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Vai ir iespējams aprēķināt komisijas maksu rēķiniem, kas jau ir iegrāmatoti?

Supply Chain Management pašlaik neatbalsta komisijas maksu aprēķināšanu iegrāmatotajiem rēķiniem.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Komplekta krājums netiek atbalstīts starpuzņēmumu procesā.

Komplekta krājums nav pieejams pirkšanas pasūtījumam, jo, pārbaudot komplekta krājuma pārdošanas pasūtījuma rindas, jūs ievērosit, ka daudzums ir *0* (nulle) un statuss ir *Atcelts*. Tas tiek darīts ar nolūku. Pārdošanas pasūtījums iegādājas tikai komplekta krājuma komponentus. Tas nepērk pašu komplekta krājumu.

Ja ir nepieciešams iegādāties komplektu, apsveriet, vai ir nepieciešams to atzīmēt kā komplekta krājumu, jo šī funkcionalitāte faktiski ir paredzēta ieņēmumu atzīšanas scenārijiem. Papildinformāciju par komplektu krājumiem, skatiet sadaļā [Komplekti](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]