---
title: Datu integrācijas projekta izveide
description: Šajā tēmā skaidrots, kā izveidot datu integrācijas projektu.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: 7841f8b31e0ac1a40dce9acaac747f5f378236e0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752668"
---
# <a name="create-a-data-integration-project"></a>Datu integrācijas projekta izveide

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā skaidrots, kā izveidot datu integrācijas projektu.

1. Pierakstieties programmā Microsoft Dynamics 365 Finance.
2. Dodieties uz **Darbvietas \> Datu pārvaldība** un atlasiet **Datu entītijas**. Pirms pārejat pie nākamās darbības, uzgaidiet, līdz visas datu entītijas ir atsvaidzinātas.
3. Atveriet [Power Apps portālu](https://make.powerapps.com/) un veiciet tālāk norādītās darbības.

    1. Atlasiet atbilstošo vidi.
    2. Navigācijas kreisajā rūtī atlasiet **Dataverse\> Savienojumi**.
    3. Izveidojiet savienojumu ar tālāk norādīto vienumu atbilstošajām instancēm.

        - Dynamics 365
        - Dynamics 365 finansēm un operācijām

4. Atveriet [Power Apps vides](https://admin.powerapps.com/environments) un veiciet tālāk norādītās darbības.

    1. Izvēlieties **Datu integrāciju**.
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

        - Debitoru maksājumu ieskatu rezultāts (CDS uz Fin un Ops 10.0.17+)
        - Skaidras naudas plūsmas laika sērijas rezultāti (CDS uz Fin and Ops)
        - Budžeta laika sērijas rezultāti (CDS uz Fin and Ops)

    2. Katram projektam iestatiet atbilstošo grafiku.

> [!NOTE]
> Ja CDS neredzat obligātās entītijas, lūdzu, dodieties uz **Kredīti un iekasēšana > Iestatījumi > Finanšu ieskati > Finanšu ieskatu parametri**, iespējojiet debitoru maksājumu prognožu līdzekli un noklikšķiniet uz pogas **Izveidot prognozēšanas modeli**. Kad mākslīgā intelekta modeļa izvietošana ir pabeigta (veiksmīgi vai neveiksmīgi), CDS entītijas, kas nepieciešamas integrācijas izveidei, tiks izvietotas CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
