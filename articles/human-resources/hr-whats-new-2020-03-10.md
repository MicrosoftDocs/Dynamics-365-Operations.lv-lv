---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 10. marts)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1843095c41428d377341154c9f2140085831e770
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555262"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 10. marts)

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.2985. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Nevar piekļūt prasmju atbilstības analīzes pārskatam (394460)

Šis pārskats netiek atbalstīts programmā Dynamics 365 Human Resources. Ir noņemts izvēlnes elements, lai izdrukātu SSRS pārskatu.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Nepareizs ziņojums, piekļūstot Darba sākšana lapai (417950)

Izmantojot šīs izmaiņas, drošība paslēpj šo izvēlnes elementu, ja jums nav pieejas veidlapai.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Racionalizēta uzdevumu uzturēšana darbiniekiem (380538)

Nodarbināmā uzdevuma uzturēšanas veidlapa uzskaita visus darbinieka uzdevumus, kas saistīti ar ievadīšanu, izvadīšanu, pārejām un biznesa procesiem. Tagad varat dzēst, piešķirt no jauna vai atjaunināt uzdevuma statusu.

Piemērs: Bendžamins Martins ir pabalstu administrators. Darbinieka ievadīšanas laikā ir izveidoti uzdevumi, lai Bendžamins pārskatītu jaunā darbinieka pabalstu atlasi. Bendžaminam ir pagātnes uzdevumi, ko viņš ir pabeidzis, un nākotnes uzdevumi, kas viņam ir jāpabeidz. Bendžamins nolemj atstāt uzņēmumu, tāpēc viņa uzdevumiem jābūt vai nu atkārtoti piešķirtiem vai noņemtiem. Uzdevumu uzturēšanas veidlapa (**Nodarbinātā** veidlapas darbības rūtī) ļauj visiem Bendžamina uzdevumiem tikt atkārtoti piešķirtiem citam darbiniekam vai noņemtiem.  

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service risinājums tagad ir pieejams ar šādām izmaiņām:

| apraksts | Labot |
| --- | --- |
| **Darba/amata** elementa izmaiņas | <ul><li>**Kompensācijas reģions** pievienots</li>|
| **Darba amata dimensijas** pievienotais elements | <ul><li>**Finanšu dimensijas** pievienotas</li>
| **Darbinieka** elementa izmaiņas | <ul><li>**Vārdu secība** pievienota</li><li>**Darbi no mājām** pievienoti</li><li>**Valoda** pievienota</li><li>**Darba stāža datums** pievienots</li><li>**Gadadienas datums** pievienots</li><li>**Sākotnējais darbā pieņemšanas datums** pievienots</li></ul> |
| **Nodarbinātības** elementa izmaiņas | <ul><li>**Finanšu dimensijas** pievienotas</li><li>**Darba attiecību pārtraukšanas pamatojums** pievienots</li><li>**Beigu datums** pārdēvēts no **Pārejas datuma**</li><li>**Probācijas datums** pievienots</li></ul> |
| **Darbinieka adreses** elementa izmaiņas | <ul><li>**Adrese** pievienota</li><li>**1. adreses rinda**, **2. adreses rinda** un **3. adreses rinda** atzīmēta norakstīšanai</li></ul> |
| Jaunas mainīgās atlīdzības iestatījuma entitījas | <ul><li>**Atlīdzības mainīgā plāna tips**</li><li>**Atlīdzības mainīgā sistēma**</li><li>**Izmaksas noteikumi**</li><li>**Atlīdzības mainīgā plāna līmenis**</li></ul> |
| Jauna **Darbinieka kalendāra nodarbinātības** entitīja | <ul><li>**Darba kalendāra elements** pievienots</li></ul> |
| Jauna **Algas pozīcijas detalizētas informācijas** entitīja | <ul><li>**Algas pozīcijas detalizēta informācija** pievienota</li></ul> |
| Jauna **Nosaukuma** entitīja | <ul><li>**Nosaukums** pievienots</li></ul> Jaunā **Nosaukuma** entītija ir iekļauta Common Data Service, bet šajā laikā nav atsauces no **Darba amata** vai **Darba** vienībām. |

> [!NOTE]
> Finanšu dimensijas abām pozīcijām un nodarbinātībai nodrošina viena virziena integrēšanu personāla vadības resursu atjauninājumiem Common Data Service. Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Common Data Service uz personāla vadības resursiem.

Nākamo dažu nedēļu laikā šīs elementa izmaiņas būs pieejamas visās vidēs. Lai manuāli instalētu jaunāko Common Data Service risinājumu Personāla vadībai:

1.  Dodieties uz [Power Platform Administrēšanas centru](https://admin.powerplatform.microsoft.com).

2.  Atlasiet **Vides**.

3.  Sameklējiet vidi, ko vēlaties atjaunināt. Apkārtējai videi ir jāatbilst **Vides nosaukumam** **Common Data Service informācijas** sadaļā, kas atrodas sadaļā **Par** personāla vadības veidlapā.

4.  Atlasiet vidi, lai skatītu vides informāciju.

5.  Darbību joslas augšdaļā atlasiet pogu **Pārvaldīt risinājumus**. Tiks atvērts jauns pārlūkprogrammas logs un navigēs uz **Dynamics 365 administrēšanas centru** vides kontekstā.

6.  **Risinājumu** sarakstā atlasiet **Dynamics 365 Human Resources enkurs**.

7.  Atlasiet **Atjaunināt**, lai izmantotu jaunāko risinājumu.

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie priekšskatījuma līdzekļi ir pieejami 2020. gada 3. februārī:

- **Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi** – Papildu informāciju skatiet [Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Atvieglojumu pārvaldības priekšskatījums** — plašāku informāciju, ieskaitot zināmās problēmas, skatiet [Atvieglojumu pārvaldības apskatā](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Drīzumā

### <a name="platform-update-33"></a>Platformas update 33

- Pilnas lapas lietojumprogrammas (priekšskatījums) - Šī priekšskatījuma funkcija, kas paredz saglabāto skatu funkcijas iespējošanu, ļauj Power Apps un trešo pušu programmas pievienot kā pilnas lapas programmas, izmantojot informācijas paneli. 

- Saglabātie skati (priekšskatījums) — Šis priekšskatījuma līdzeklis iespējo saglabātos skatījumus, kas ir nozīmīgs personalizēšanas apakšsistēmas papildinājums. Šis līdzeklis ļauj lietotājiem iegūt vairākas nosauktas personalizācijas kopas uz lapu. Varat arī publicēt skatus uz drošības lomām.

- Optimizēta ¨ir viens no¨ filtrēšanas iespēja - Šī funkcija ļauj optimizētu "ir viens no" filtrēšanas iespēju, kas atvieglo vairāku filtru vērtību ievadīšanu. Tai ir vienkāršāks individuālo vai visu filtru vērtību noņemšanas mehānisms, kā arī filtra vērtību vizualizācija ir kompaktāka un intuitīvāka. 

- Ieteicamie lauki — Lietotājiem bieži ir jāpievieno lauki režģim vai lapai. Tas var būt sarežģīti ar tik daudziem pieejamiem laukiem. Tā vietā, lai meklētu pēc liela saraksta, šis līdzeklis ļauj sistēmai pāriet pāri ieteicamo lauku kopai, pamatojoties uz to, ko citi lietotāji visbiežāk pievieno līdzīgos scenārijos.

- Sticky noklusējuma darbības režģos - Šī funkcija nodrošina, ka noklusējuma darbība režģī tiek sasaistīta ar konkrētu kolonnu režģī neatkarīgi no tā, vai šī kolonna tiek pārvietota vai paslēpta.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)