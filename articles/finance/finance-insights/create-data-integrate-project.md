---
title: Datu integrētāja projekta izveide (priekšskatījums)
description: Šajā tēmā paskaidrots, kā izveidot datu integrētāja projektu.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: bea1fe3df255bd07a205f90cff8c546cee422fa3
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638660"
---
# <a name="create-a-data-integrator-project-preview"></a>Datu integrētāja projekta izveide (priekšskatījums)

[!include [banner](../includes/banner.md)]

Šajā tēmā paskaidrots, kā izveidot datu integrētāja projektu.

1. Pierakstieties programmā Microsoft Dynamics 365 Finance.
2. Dodieties uz **Darbvietas \> Datu pārvaldība** un atlasiet **Datu entītijas**. Pirms pārejat pie nākamās darbības, uzgaidiet, līdz visas datu entītijas ir atsvaidzinātas.
3. Atveriet [Power Apps portālu](https://make.powerapps.com/) un veiciet tālāk norādītās darbības.

    1. Atlasiet atbilstošo vidi.
    2. Kreisās puses navigācijas rūtī atlasiet **Dati \> Savienojumi**.
    3. Izveidojiet savienojumu ar tālāk norādīto vienumu atbilstošajām instancēm.

        - Dynamics 365
        - Dynamics 365 finansēm un operācijām

4. Atveriet [Power Apps vides](https://admin.powerapps.com/environments) un veiciet tālāk norādītās darbības.

    1. Atlasiet **Datu integrētājs**.
    2. Atlasiet **Savienojumu kopas**.
    3. Atlasiet **Jauna savienojumu kopa**.
    4. Ievadiet savienojuma nosaukumu.
    5. Atlasiet atbilstošos savienojumus tālāk norādītajiem vienumiem.

        - Dynamics 365
        - Dynamics 365 finansēm un operācijām

    6. Atlasiet atbilstošo organizācijas kartējumu.
    7. Atlasiet **Izveidot**.

5. Atveriet [Power Apps vides](https://admin.powerapps.com/environments) un veiciet tālāk norādītās darbības.  

    1. Izveidojiet datu integrācijas projektus tālāk norādītajām veidnēm, izmantojot savienojuma kopu, ko tikko izveidojāt.

        - Debitora maksājumu ieskatu rezultāti (CDS uz Fin and Ops)
            - Ja izmantojat versiju 10.0.17 vai jaunāku versiju, ir jāizmanto veidne ar nosaukumu Debitoru maksājumu ieskatu rezultāts (CDS uz Fin un Ops 10.0.17+).
        - Skaidras naudas plūsmas laika sērijas rezultāti (CDS uz Fin and Ops)
        - Budžeta laika sērijas rezultāti (CDS uz Fin and Ops)

    2. Katram projektam iestatiet atbilstošo grafiku.

> [!NOTE]
> Ja CDS neredzat obligātās entītijas, lūdzu, dodieties uz **Kredīti un iekasēšana > Iestatījumi > Finanšu ieskati > Finanšu ieskatu parametri**, iespējojiet debitoru maksājumu prognožu līdzekli un noklikšķiniet uz pogas **Izveidot prognozēšanas modeli**. Kad mākslīgā intelekta modeļa izvietošana ir pabeigta (veiksmīgi vai neveiksmīgi), CDS entītijas, kas nepieciešamas integrācijas izveidei, tiks izvietotas CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
