---
title: Piezīmju integrācija
description: Šajā tēmā aprakstīta piezīmju datu integrācija duālajā ierakstā.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d52ff69cfd7a81eb9f19a0ef498c6ceeea77b360
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782360"
---
# <a name="note-integration"></a>Piezīmju integrācija

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Biznesa procesu laikā Microsoft Dynamics 365 lietotāji bieži apkopo informāciju par saviem klientiem. Šī informācija tiek reģistrēta kā aktivitātes un piezīmes. Šajā tēmā aprakstīta piezīmju datu integrācija duālajā ierakstā.

Klienta informāciju var klasificēt vairākos veidos:

+ **Izmantojamā informācija, ko Dynamics 365 lietotājs apstrādā klienta vārdā** — piemēram, Contoso (Dynamics 365 lietotājs) organizē spēļu šovu. Viens no Contoso klientiem (klients) vēlas piedalīties spēļu šovā. Klients lūdz Contoso darbinieku rezervēt viņiem slotu spēļu šovā. Rezervācija notiek Contoso notikumau dalībnieka kalendārā.
+ **Izmantojamā informācija Dynamics 365 lietotājam** — piemēram, klients, kurš iegādājas vienību Surface, ievada īpašas instrukcijas, kas norāda, ka ierīcei pirms piegādes ir jābūt iesaiņotai kā dāvanai. Šīs instrukcijas ir izmantojama informācija, kas jāapstrādā Contoso darbiniekam, kurš ir atbildīgs par iepakošanu.
+ **Informācija, kas nav izmantojama** — piemēram, klients apmeklē Contoso veikalu un sarunas ar veikala darbinieku laikā pauž interesi par *Halo* spēlēm un spēļu piederumiem. Veikala darbinieks izdara piezīmi par šo informāciju. Pēc tam preču ieteikumu programma to izmanto, lai klientam varētu sniegt ieteikumus.

Parasti izmantojamā informācija tiek tverta kā *aktivitātes* programmās Finance and Operations un Customer Engagement programmās. Neizmantojamā informācija tiek tverta kā *piezīmes* programmās Finance and Operations un kā *anotācijas* Customer Engagement programmās.

> [!TIP]
> Lai arī piezīmes ir paredzētas neizmantojamajai informācijai, programmas neliegs jums tās izmantot, lai saglabātu un apstrādātu izmantojamo informāciju, ja vēlaties tās izmantot šādā veidā.

Microsoft pašlaik izlaiž funkcionalitāti piezīmju integrācijai. (Funkcionalitāte aktivitātes integrācijai tiks izlaista vēlāk.) Piezīmju integrācija ir pieejama klientiem, kreditoriem, pārdošanas pasūtījumiem un pirkšanas pasūtījumiem.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Piezīmes izveide programmā Customer Engagement

Lai izveidotu piezīmi programmā Customer Engagement un pēc tam to sinhronizētu ar Finance and Operations programmu, izpildiet tālāk minētās darbības.

1. Programmā Customer Engagement atveriet klienta konta ierakstu.
2. Rūtī **Laika skala** atlasiet plus zīmi (**+**) un pēc tam atlasiet **Piezīme**, lai izveidotu piezīmi.

    ![Piezīmes izveide programmā Customer Engagement.](media/notes-ce-1.png)

3. Ievadiet nosaukumu un aprakstu un pēc tam atlasiet **Pievienot piezīmi**.

    ![Virsraksta un apraksta ievadīšana.](media/notes-ce-2.png)

    Jaunā piezīme tiek pievienota klienta laika skalai.

    ![Jauna piezīme klienta laika skalā.](media/notes-ce-3.png)

4. Pierakstieties programmā Finance and Operations un atveriet to pašu klienta ierakstu. Ievērojiet, ka poga **Pielikumi** button (saspraudes simbols) augšējā labajā stūrī norāda, ka ierakstam ir pielikums.

    ![Paziņojums par pielikumu.](media/notes-ce-4.png)

5. Atlasiet pogu **Pielikumi**, lai atvērtu lapu **Pielikumi**. Jums vajadzētu atrast piezīmi, ko esat izveidojis programmā Customer Engagement.

    ![Piezīme no programmas Customer Engagement.](media/notes-ce-5.png)

Visi piezīmes atjauninājumi tiek sinhronizēti abos virzienos starp programmu Finance and Operations un programmu Customer Engagement.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Piezīmes izveide programmā Finance and Operations

Varat izveidot piezīmi arī programmā Finance and Operations, un pēc tam tā tiks sinhronizēta ar programmu Customer Engagement.

Lai izveidotu piezīmi programmā Finance and Operations un pēc tam to sinhronizētu ar programmu Customer Engagement, izpildiet tālāk minētās darbības.

1. Programmas Finance and Operations lapā **Pielikumi** atlasiet **Jauns** \> **Piezīme**.

    ![Piezīmes izveide programmā Finance and Operations.](media/notes-fo-1.png)

2. Ievadiet nosaukumu un īsu norādījumu kopu un pēc tam atlasiet **Saglabāt**.

    ![Virsraksta un instrukciju ievadīšana.](media/notes-fo-2.png)

3. Programmā Customer Engagement atjauniniet ierakstu. Jaunā piezīme atradīsies laika skalā.

    ![Jauna piezīme laika skalā programmā Customer Engagement.](media/notes-fo-3.png)

Piezīmi var klasificēt kā iekšēju vai ārēju.

- Programmas Finance and Operations lapā **Pielikumi** atveriet piezīmi un pēc tam laukā **Ierobežojums** atlasiet **Iekšēja** vai **Ārēja**.

    ![Ierobežojuma lauks.](media/notes-fo-4.png)

Var izveidot arī vietrādi URL.

1. Programmas Finance and Operations lapā **Pielikumi** atlasiet **Jauns** \> **Vietrādis URL**.
2. Ievadiet virsrakstu un vietrādi URL.
3. Laukā **Ierobežojums** atlasiet **Iekšējais** vai **Ārējais**.

    ![Vietrāža URL izveide programmā Finance and Operations.](media/notes-fo-5.png)

4. Atlasiet **Saglabāt**.

    Tā kā programmām Customer Engagement nav vietrāža URL veida, tas tiek integrēts ar dubulto ierakstu kā piezīme.

    ![Vietrāža URL parādīšana piezīmes veidā programmā Customer Engagement.](media/notes-ce-6.png)

> [!NOTE]
> Failu pielikumi netiek atbalstīti.

## <a name="templates"></a>Veidnes

Piezīmju integrācija ietver tabulas karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

| Finance and Operations programma | Customer engagement programma | Apraksts |
|----------------------------|-------------------------|-------------|
| [Debitora pielikumi](mapping-reference.md#230) | Anotācijas | Uzņēmumi, kas izmanto vienkāršu tekstu un vietrāžus URL, lai tvertu debitoram specifisko informāciju (gan organizācijām, gan personām). |
| [Kreditora dokumentu pielikumi](mapping-reference.md#231) | Anotācijas | Uzņēmumi, kas izmanto vienkāršu tekstu un vietrāžus URL, lai tvertu kreditoram specifisko informāciju (gan organizācijām, gan personām). |
| [Pārdošanas pasūtījuma galvenes dokumenta pielikumi](mapping-reference.md#229) | Anotācijas | Uzņēmumi, kas izmanto vienkāršu tekstu un vietrāžus URL, lai tvertu pārdošanas pasūtījumam specifisku informāciju. |
| [Pirkšanas pasūtījuma galvenes dokumenta pielikumi](mapping-reference.md#232) | Anotācijas | Uzņēmumi, kas izmanto vienkāršu tekstu un vietrāžus URL, lai tvertu pirkšanas pasūtījumam specifisku informāciju. |

## <a name="limitations"></a>Ierobežojumi

Kad piezīmju risinājums ir instalēts, to nevar atinstalēt. 

Papildinformāciju skatiet sadaļā [Dubultā ieraksta kartēšanas atsauce](mapping-reference.md).
