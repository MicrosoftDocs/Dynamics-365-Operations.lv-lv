---
title: Atjaunināt pārnesto budžetu pēc pirkšanas pasūtījumu un rēķinu samazināšanas
description: Šajā rakstā ir aprakstīts, kā kontrolēt, kas notiek ar pārnesto budžetu, kad pirkšanas pasūtījumi tiek atcelti vai samazināti un kad rēķini tiek samazināti.
author: TaylorVH
ms.date: ''
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: Version 1611
ms.search.form: LedgerFund
ms.openlocfilehash: 790f1e770fd77d5209436c1c89e0f6125aac150f
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573051"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Atjaunināt pārnesto budžetu pēc pirkšanas pasūtījumu un rēķinu samazināšanas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā rakstā ir aprakstīts, kā kontrolēt, kas notiek ar pārnesto budžetu, kad pirkšanas pasūtījumi tiek atcelti vai samazināti un kad rēķini tiek samazināti.

Papildinformāciju par to, kā pirkšanas pasūtījumi tiek apstrādāti gada beigās, skatiet [sadaļā Pirkšanas pasūtījumu apstrāde gada beigās](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Ieslēgt vai izslēgt pārnesto budžeta samazinājumu rēķinu noviržu gadījumā

Sistēma vienmēr var atjaunināt pārnesto budžetu, kad pirkšanas pasūtījums tiek atcelts vai samazināts. Tomēr, ja vēlaties atjaunināt pārnesto budžetu, kad rēķins ir samazināts, ir jāieslēdz budžeta pārnešana, *ja rēķins pret pirkšanas pasūtījumu tiek samazināts ar novirzes* iespēju. Administratori var ieslēgt vai izslēgt šo līdzekli, meklējot to līdzekļu pārvaldības **[darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**.

## <a name="purchase-order-reductions-and-cancellations"></a>Pirkšanas pasūtījumu samazināšana un atcelšana

Neatkarīgi no *tā*, vai Samazināt pārnesto budžetu, ja rēķins pret pirkšanas pasūtījumu ir samazināts ar novirzes funkciju ir ieslēgts, pārnestais budžets tiks atjaunināts, kad kvalificēšanas pirkšanas pasūtījums tiek atcelts vai samazināts. Varat iestatīt katru virsgrāmatas fondu, lai atbildētu vienā no šiem veidiem:

- Saglabāt pārnesto budžetu, kā tas tika izveidots.
- Automātiski koriģējiet pārnesto budžetu, lai noņemtu atcelto vai samazināto summu.

Automātiskai budžeta korekcijai ir pieejamas tikai tās pirkšanas pasūtījumu rindas, kurās ir sadales, kurās ir ietverti līdzekļu sadalīumi. Automātiskā budžeta korekcija tiek veikta, kad tiek pabeigts pirkšanas pasūtījums vai tiek apstiprināts pirkšanas pasūtījuma samazinājums.

## <a name="invoice-reductions"></a>Rēķinu samazināšana

*Ja* samazināt pārnesto budžetu, ja rēķins pret pirkšanas pasūtījumu ir samazināts ar novirzes līdzekli ir ieslēgts, varat norādīt, vai katram fondam jāsamazina pārnestais budžets, kad rēķins tiek samazināts papildus pirkšanas pasūtījuma samazināšanai vai atcelšanai. Rēķinam jābūt pirkšanas pasūtījumam, kam ir pārnests budžets. Atlaides ietver cenas novirzes, maksas novirzes un nodokļu novirzes. Kad pārnešanas pirkšanas pasūtījums rēķina izrakstīšanas laikā tiek samazināts, tiek izveidota novirze. Kad rēķins ir iegrāmatots, pirkšanas pasūtījuma apgrūtinājums tiks samazināts par novirzes summu. Šī funkcija izveidos arī automātisku budžeta korekciju novirzes summai.

Ja opcija *Samazināt* pārnesto budžetu, ja rēķins pret pirkšanas pasūtījumu ir samazināts ar novirzes līdzekli, šajā scenārijā pārnestais budžets netiek samazināts. Tāpēc atlikušais pārnestais budžets novirzes summai ir atlicis.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Konfigurēt pārnestā budžeta opcijas katram fondam

Izpildiet šīs darbības katram virsgrāmatas fondam, kam vajadzētu būt iespējai samazināt pārnesto budžetu, ja tiek samazināts pirkšanas pasūtījums vai rēķins.

1. Dodieties uz **Virsgrāmatas \> kontu plāna \> fondu \>.**
1. Atlasiet līdzekļus, kurus vēlaties iestatīt.
1. Pirkšanas **pasūtījuma gada beigu procesā pārliecinieties**, ka opcija **Ignorēt atlasīto gada beigu opciju** ir iestatīta uz *Jā*.
1. Lai **atceltu vai samazinātu lauku** atbilstoši pieprasījumam, **iestatiet** budžeta atjaunošanu, ja ir atcelts vai samazināts pārnestā budžeta statuss. Iestatījumiem ir nedaudz atšķirīgi efekti atkarībā no tā, vai sistēmā ir ieslēgta novirzes funkcionalitāte samazināts atkarībā no tā, vai samazināt pārnesto budžetu, *ja* pirkšanas pasūtījuma rēķins ir samazināts.

    - Ja šī funkcija ir izslēgta, sistēma reaģē tikai uz atceltiem vai samazinātiem pirkšanas pasūtījumiem. Opciju iestatījumi darbojas šādā veidā:

        - *Nē* – sistēma izveido budžeta reģistra ierakstu pirkšanas pasūtījumu bilances atlikumu, kas ir atcelti vai samazināti.
        - *Jā* — sistēma ļauj pirkšanas pasūtījumus atcelt vai samazināt, bet nevar izveidot budžeta reģistra ierakstu. Pārnestais budžets paliek pieejams patēriņam citos dokumentos.

    - Ja šī funkcija ir ieslēgta, sistēma reaģē gan uz rēķinu noviržu, gan uz atceltiem vai samazinātiem pirkšanas pasūtījumiem. Opciju iestatījumi darbojas šādā veidā:

        - *Nē* - rēķina noviržu gadījumā sistēma izveido budžeta reģistra ierakstu attiecībā pret pirkšanas pasūtījumu novirzes samazinājuma summai. Atceltiem vai samazinātiem pirkšanas pasūtījumiem šim iestatījumam ir tāda pati ietekme, kā tam, ja šī funkcija ir izslēgta.
        - *Jā* — rēķinu noviržu gadījumā sistēma ļauj samazināt rēķinu, bet nevar izveidot budžeta reģistra ierakstu. Pārnestais budžets paliek pieejams patēriņam citos dokumentos. Atceltiem vai samazinātiem pirkšanas pasūtījumiem šim iestatījumam ir tāda pati ietekme, kā tam, ja šī funkcija ir izslēgta.

## <a name="additional-resources"></a>Papildu resursi

- [Apstrādāt pirkšanas pasūtījumus gada beigās](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Uzturēt vispārīgās budžeta rezervācijas](general-budget-reservation-tasks.md)
- [Līdzekļi publiskajā sektorā](funds-public-sector.md)
- [Publiskā sektora līdzekļa iestatīšana](tasks/set-up-fund-public-sector.md)
