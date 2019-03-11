---
title: Lauku aprakstu skatīšana un eksportēšana
description: Šajā rakstā ir paskaidrots, ka skatīt lauku aprakstus un kā lietot lapu Lauku apraksti, lai eksportētu aprakstus.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7be1495fc42b5f19884a7d9df747f6bec9b64680
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "359340"
---
# <a name="view-and-export-field-descriptions"></a>Lauku aprakstu skatīšana un eksportēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, ka skatīt lauku aprakstus un kā lietot lapu Lauku apraksti, lai eksportētu aprakstus.

Programmatūrā Microsoft Dynamics 365 for Finance and Operations tiek nodrošināti apraksti par dažiem sarežģītākajiem laukiem. Šie apraksti tiek parādīti, kad novietojat peles kursoru uz lauka. Aprakstus varat skatīt un eksportēt lapā **Lauku apraksti**.

Ne visām lapām ir lauku apraksti. Mēs vēlamies sniegt aprakstus tikai sarežģītākajiem laukiem, nevis tiem, kuru lietojums ir acīmredzams. Tādēļ dažās lapās nav neviena lauka apraksta, dažās lapās ir daži apraksti, bet dažās no sarežģītākajām lapām, piemēram, daudzās parametru lapās, ir daudz aprakstu.

Ja jums ir piekļuve Finance and Operations izstrādes videi, varat pievienot jaunus lauku aprakstus un pielāgot esošos aprakstus. Piemēram, lauka aprakstam varat pievienot uzņēmumam specifisku informāciju. Papildinformāciju skatiet rakstā [Pielāgot lauka palīdzību](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Skatīt lauku aprakstus lietotāja interfeisā

Lauku aprakstus varat apskatīt, virzot peles kursoru pār attiecīgo lauku. Ja apraksts nav pieejams, kad novietojat peles kursoru uz lauka, jūs redzat lauka nosaukumu.

> [!NOTE]
> Programmā Dynamics AX 7.0 (2016. gada februāris) lauku aprakstus var skatīt tikai lapā **Lauku apraksti**.

Nākamajā attēlā ir parādīts lauka apraksts, kas ir redzams, kad novietojat peles kursoru uz lauka **Bloķēt krājumus inventarizācijas laikā**.

[![Lauka apraksta piemērs](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Izmantot lapu Lauku apraksti, lai skatītu un eksportētu lauku palīdzību

Lapa **Lauku apraksti** jums ļauj skatīt un eksportēt lauku aprakstus. Jūs varat redzēt aprakstus, kas ir pieejami vienā lapā vienlaicīgi.

### <a name="view-the-descriptions-for-a-page"></a>Skatīt lapas aprakstus

Lai skatītu aprakstus kādai lapai, izpildiet šo darbību.

- Laukā **Atlasīt lapu** ierakstiet lapas nosaukumu. Varat arī noklikšķināt uz bultiņas, lai atvērtu lapu sarakstu, un pēc tam pārlūkot vai filtrēt šo sarakstu.

Var izmantot lapas nosaukumu, kas tiek rādīts lietotāja interfeisā (UI) (piemēram, **Debitori**), vai lapas koda nosaukumu (AOT nosaukumu), kas ir pieejams, kad ar peles labo pogu noklikšķināt uz lapas (piemēram, **CustTable**).

Informāciju par dažādajiem veidiem, kā filtrēt lapu sarakstu, skatiet vēlākā šī raksta sadaļā “Lapas meklēšana”.

Ja opciju **Iekļaut laukus bez apraksta** iestatāt uz **Jā**, tad tiek rādīti visi šajā lapā esošie lauki, pat ja tiem nav lauka apraksta.

### <a name="export-the-descriptions-for-a-page"></a>Eksportēt lapas aprakstus

Lai eksportētu aprakstus kādai lapai, izpildiet šīs darbības.

1. Laukā **Atlasīt lapu** atlasiet kādu lapu.
2. Noklikšķiniet uz pogas **Atvērt programmā Microsoft Office** augšējā labajā stūrī un pēc tam noklikšķiniet uz **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Lapas meklēšana

Pastāv vairāki veidi, kā meklēt lapu laukā **Atlasīt lapu**. Daudzos gadījumos ir jānoklikšķina uz bultiņas laukā **Atlasīt lapu**, lai atvērtu nolaižamo sarakstu, un pēc tam jāatlasa no filtrētā lapu saraksta.

- Ierakstiet daļēju nosaukumu un pēc tam atveriet nolaižamo sarakstu, lai atlasītu no filtrētā lapu saraksta.
- Atveriet nolaižamo sarakstu un pēc tam noklikšķiniet uz virsraksta **Lapas nosaukums** saraksta augšpusē vai uz virsraksta **Lapas AOT nosaukums**. Tiek parādīts dialoglodziņš, kur varat izmantot papildu filtrēšanas opcijas, piemēram, **Lapas nosaukums sākas ar**.
- Ierakstiet pilnu lapas nosaukumu. Ja izmantojat šo opciju, ieteicams atvērt nolaižamo sarakstu un apskatīt, kas vēl ir pieejams šajā sarakstā pat tad, ja tiek rādīti lauku apraksti.

    - Ja nosaukumam ir viena precīza atbilstība, tiek rādīti lauku apraksti šai lapai.
    - Ja ir vairākas precīzas atbilstības, netiek rādīts neviens apraksts. Jums ir jāatver nolaižamais saraksts un jāatlasa nepieciešamā lapa.
    - Ja ierakstītais nosaukums ir daļa no citas lapas nosaukuma, tiek rādīti apraksti jūsu lapai. Taču, ja atverat nolaižamo sarakstu, varat redzēt papildu lapas, kas ietver šo nosaukumu.

Piemēram, nekādi apraksti netiek rādīti, kad laukā **Atlasīt lapu** ierakstāt **Inventarizācija**. Jūs atverat nolaižamo sarakstu un redzat, ka pastāv divas lapas, kuru nosaukums ir **Inventarizācija**, un vairākas lapas, kuru nosaukumā ir ietverts vārds “Inventarizācija”. Ja atlasāt lapu, kuras AOT nosaukums ir **InventJournalCount**, tiek rādīti lauku nosaukumi šai lapai. Taču, ja atkal atverat nolaižamo sarakstu, jūs redzat, ka sarakstā tagad ir visas lapas, kurām kā daļa no to AOT lapas nosaukuma ir “InventJournalCount”.

## <a name="troubleshooting"></a>Problēmu novēršana

Šajā sadaļā ir sniegta informācija, lai jums palīdzētu novērst problēmas, kas varētu rasties, izmantojot lauku aprakstus.

### <a name="i-cant-find-a-field-description"></a>Nevar atrast lauka aprakstu

Mēs pievienojam aprakstus sarežģītākajiem laukiem. Ja jums ir nepieciešama palīdzība par noteiktu lauku, lūdzu, ziņojiet mums, pievienojot komentāru šai tēmai.

### <a name="the-field-description-isnt-helpful"></a>Šis lauka apraksts nav noderīgs

Ziņojiet mums, pievienojot komentāru šai tēmai. Ja varat, aprakstiet papildinformāciju, kas jums ir nepieciešama.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Nevar atrast kādu lauku lapā Lauku apraksti

Lai lapā parādītu visus laukus, opciju **Iekļaut laukus bez apraksta** iestatiet uz **Jā**. Noklikšķiniet uz lauka **Atlasīt lapu**, lai pārliecinātos, ka esat atlasījis pareizo lapu. Ja jūsu ierakstītais nosaukums ir daļa no cita lauka nosaukuma, iespējams, esat atlasījis lapu, kurai ir garāks nosaukums.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Nevar atrast kādu lapu lapā Lauku apraksti

Informāciju par dažādajiem veidiem, kā atrast lapas, skatiet agrākā šī raksta sadaļā “Lapu meklēšana”. Ja ierakstījāt precīzu lapas nosaukumu, iespējams, lauku apraksti netiek rādīti, ja šāds nosaukums ir vairākām lapām. Noklikšķiniet uz bultiņas laukā **Atlasīt lapu**, lai atvērtu filtrētu sarakstu ar pieejamajām lapām.

## <a name="additional-resources"></a>Papildu resursi

[Pielāgot lauku palīdzību](../../dev-itpro/user-interface/customize-field-help.md)
