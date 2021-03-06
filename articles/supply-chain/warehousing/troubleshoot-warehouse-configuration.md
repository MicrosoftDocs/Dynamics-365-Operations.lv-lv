---
title: Ar noliktavas konfigurāciju saistīto problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, konfigurējot Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814396"
---
# <a name="troubleshoot-warehouse-configuration"></a>Ar noliktavas konfigurāciju saistīto problēmu novēršana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, konfigurējot Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Tiek parādīts šāds kļūdas ziņojums: "Numura zīme vai novietojums nav derīgs."

### <a name="issue-description"></a>Problēmas apraksts

Šis kļūdas ziņojums tiek parādīts, skenējot numura zīmes ID vai novietojumu.

### <a name="issue-resolution"></a>Problēmas risinājums

Pārliecinieties, ka numura zīmes ID nav rezervējis kas cits. Šī problēma parasti radās, kad vērtība, ko lietotājs skenēja Warehouse Management mobile lietotnē, bija gan derīga atrašanās vieta, gan derīgs numura zīmes ID. Tomēr šī problēma tika atrisināta versijā 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Tiek parādīts šāds kļūdas ziņojums: "Šai numura zīmei ir jābūt norādītai šajā novietojumā."

### <a name="issue-description"></a>Problēmas apraksts

Šis kļūdas ziņojums tiek parādīts, ja izveidojat pārsūtīšanas pasūtījumu, izmantojot noliktavu, kas ir aktivizēta papildu noliktavas pārvaldībai (WMS), un pēc tam, kad darbs ir pabeigts, jūs mēģināt apstiprināt kravu.

### <a name="issue-resolution"></a>Problēmas risinājums

**Noklusējuma kvīts novietojuma** lauks ir tukšs noliktavas "no" tranzīta noliktavai. Lai labotu šo problēmu, norādiet noklusēto ieejas plūsmas vietu tranzīta noliktavā. Pārliecinieties, vai šī atrašanās vieta ir numura zīmes kontrolēta.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Tiek parādīts šāds kļūdas ziņojums: "Nevar izveidot darba veidnes rindu krājumu statusa maiņai, jo darba veids nav derīgs. Atlasiet citu darba veidu."

### <a name="issue-description"></a>Problēmas apraksts

Darba veidnei nevar atlasīt *Krājumu statusa izmaiņas* kolonnas **Darba veids** sadaļā **Darba veidnes informācija**.

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku. *Krājumu statusa maiņas* darba veidu izmanto tikai sistēmas procesi. To nevar konfigurēt. Tā kā darba veidu saraksts ir fiksēts kā uzskaitījums, papildu ievades nevar filtrēt no **Darba veida** nolaižamās izvēlnes.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Tiek parādīts šāds kļūdas ziņojums: "Daudzums nav derīgs 1% vienībai."

### <a name="issue-description"></a>Problēmas apraksts

Daudzums nav derīgs *ea* vienībai, ja ir izdošanas darbs, kuram vienā vietā ir vairākas numura zīmes.

### <a name="issue-resolution"></a>Problēmas risinājums

Pārbaudiet, vai lauki **Vienības secības grupas ID** un **Vienības konvertēšana** izlaistajā precē vai preces variantā tiek iestatīti pareizi.

Ņemiet vērā, ka kļūdas ziņojums ir uzlabots versijā 10.0.15 (skatiet [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Jaunais kļūdas ziņojums ir "Daudzums nav derīgs. Paredzamais %1 %2."

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Novietojuma direktīvās, kas attiecas uz pārdošanas pasūtījuma izvietošanas darbu, vairāku SKU opcija nenovērtē vairākas atrašanās vietas direktīvas darbības.

### <a name="issue-description"></a>Problēmas apraksts

*Pārdošanas pasūtījuma* darba pasūtījuma veida un *Izvietošanas* darba veida novietojuma direktīvas nenovērtē vairākas novietojuma direktīvas, kad ir atlasīta opcija. **Vairāki SKU**. Tiek novērtēta tikai pirmā novietojuma direktīvas darbība.

### <a name="issue-resolution"></a>Problēmas risinājums

Versijā 10.0.15 ir pievienots jauns līdzeklis *Novērtēt visas darbības vairāku SKU novietojuma direktīvām* (skatiet [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Šis līdzeklis novērtē visas darbības vairāku SKU novietojuma direktīvām. Ja jums ir nepieciešams šis līdzeklis, izmantojiet [funkciju pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai to ieslēgtu.

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a>Nevaru izmantot Warehouse Management mobile programmu, lai veiktu daļēju izdošanu.

### <a name="issue-description"></a>Problēmas apraksts

Pārdošanas un pārsūtīšanas pasūtījumiem nevar izlaist krājumus un veiktu daļēju izdošanu.

### <a name="issue-resolution"></a>Problēmas risinājums

Lapā **Mobilās ierīces izvēlnes vienumi** katram izvēlnes elementam, kas iestatīts, lai apstrādātu pārdošanas pasūtījumus vai pārsūtīšanas pasūtījumus, iestatiet opciju **Atļaut sadalīt darbu** kopsavilkuma cilnē **Vispārīgi** uz *Jā*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Kā var veikt krājumu statusa izmaiņas daļējiem daudzuma darbiem?

### <a name="issue-description"></a>Problēmas apraksts

Vēlaties veikt krājumu statusa izmaiņas daļējam paketes daudzumam.

### <a name="issue-resolution"></a>Problēmas risinājums

Lai ļautu darbiniekiem veikt šīs izmaiņas, varat izveidot izvēlnes elementu Warehouse Management mobile programmai. Izveidojiet (vai rediģējiet) izvēlnes vienumu lapā **Mobilās ierīces izvēlnes vienumi**, kam ir sekojošie iestatījumi:

- **Režīms:** *Darbs*
- **Izmantot esošo darbu:** *Nē*
- **Darba izveides process:** *Kustība*
- **Rādīt krājumu statusu:** *Jā*

Varat iestatīt citus laukus lapā pēc nepieciešamības.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Doka pārvaldības profils novietojuma profilā nepieļauj krājumu tipu sajaukšanu.

### <a name="issue-description"></a>Problēmas apraksts

Jūs izmantoja *sūtījumu konsolidācijas politikas*. *Novietojuma profilam* esat iestatījis *doka pārvaldības profilu*, taču, kad darbs ir izveidots, krājumu tipi beigu vietā tiek jaukti.

### <a name="issue-resolution"></a>Problēmas risinājums

Doka pārvaldības profiliem nepieciešams, lai darbs tiktu sadalīts iepriekš. Citiem vārdiem sakot, doka pārvaldības profils sagaida, ka darba galvenei nebūs vairāku izvietošanas vietu.

Lai doka pārvaldības profils efektīvi pārvaldītu krājumu jaukšanu, ir jāiestata darba galvenes pārtraukums.

Šajā piemērā mūsu doka pārvaldības profils tiek konfigurēts tā, ka **Krājumu veidi, kas nedrīkst būt jaukti**, tiek iestatīts *Kravas ID*, un mēs tam iestatām darba galvenes pārtraukumu:

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Atlasiet rediģējamā **Darba pasūtījuma veidu** (piemēram, *Pirkšanas pasūtījumi*).
1. Atlasiet darba veidni rediģēšanai.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Atveriet cilni **Kārtošana** un pievienojiet rindu ar šādiem iestatījumiem:
    - **Tabula** - *Pagaidu darba darbības*
    - **Atveidotā tabula** - *Pagaidu darba darbības*
    - **Lauks** - *Sūtījuma ID*
1. Atlasiet **Labi**.
1. Jūs atgriežaties lapā **Darbu veidnes**. Darbību rūtī atlasiet **Darba galvenes pārtraukumi**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Atzīmējiet izvēles rūtiņu, kas saistīta ar **lauka nosaukuma** *sūtījuma ID*.
1. Darbību rūtī atlasiet **Saglabāt**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
