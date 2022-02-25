---
title: Datu integrācijas projekta izveide
description: Šajā tēmā skaidrots, kā izveidot datu integrācijas projektu.
author: ShivamPandey-msft
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 50f435f9d461667a1908baa529d73766085c183a
ms.sourcegitcommit: 6526acd0300d9c5800d3d7675d54e23090d031df
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2022
ms.locfileid: "8107291"
---
# <a name="create-a-data-integration-project"></a>Datu integrācijas projekta izveide

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā izveidot datu integrācijas projektu.

1. Pierakstieties programmā Microsoft Dynamics 365 Finance.
2. Dodieties uz **Darbvietas \> Datu pārvaldība** un atlasiet **Datu entītijas**. Pirms pārejat pie nākamās darbības, uzgaidiet, līdz visas datu entītijas ir atsvaidzinātas.
3. Atveriet [Power Apps portālu](https://make.powerapps.com/) un veiciet tālāk norādītās darbības.

    1. Atlasiet atbilstošo vidi.
    2. Navigācijas kreisajā rūtī atlasiet Savienojumi **Dataverse\>**.
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
> Ja sadaļā Nepieciešamie elementi Dataverse nav redzams, **pārejiet uz sadaļu Kredīts** > **·** > **un kolekcijasSetupFinanceSetupFinancesFinancesfinances** > **·** **parametros**, iespējojiet līdzekli, **debitora maksājumu prognozes un pēc tam atlasiet Izveidot prognozēšanas modeli.** Kad AI modeļa izvietošana ir pabeigta, tiks Dataverse izvietoti elementi, kas nepieciešami integrācijas integrācijai.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
