---
title: Autentifikācijas starp pakalpojumiem konfigurēšana
description: Šajā rakstā ir aprakstīts, kā konfigurēt pakalpojumu-pakalpojumu autentifikāciju Microsoft Dynamics 365 Commerce, lai droši izsauktu pakalpojuma API vērtēšanai un pārskatīšanai.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: acb3a6220d146d32bbeb5bd8169033bc897ec3fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871611"
---
# <a name="configure-service-to-service-authentication"></a>Autentifikācijas starp pakalpojumiem konfigurēšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt pakalpojumu-pakalpojumam (S2S) Microsoft Dynamics 365 Commerce autentifikāciju, lai droši izsauktu pakalpojuma programmas programmēšanas interfeisus (API) vērtēšanai un pārskatīšanai.

Dynamics 365 Commerce piedāvā [vērtējumus un pārskatus](ratings-reviews-overview.md) kā par channel risinājumu. Šis risinājums iespējo piekļuvi pakalpojumu API no ārpus Commerce, lai varētu tikt veikti dažādi uzdevumi. Šie uzdevumi ietver novērtējumu un pārskatīšanas importēšanu no jūsu ārējās sistēmas komercijai un vērtējumu un pārskatīšanas no Commerce eksportēšanas. Lai dotu iespēju Commerce droši izsaukt novērtējumus un pārskata pakalpojuma API, jums vispirms ir jākonfigurē S2S autentifikācija, izpildot šajā rakstā sniegtās procedūras.

## <a name="add-a-new-app-registration"></a>Pievienot jaunu programmas reģistrāciju

Pirms jaunas programmas reģistrācijas pievienošanas ir jāizveido programma, izmantojot [Azure portālu](https://portal.azure.com). Lai reģistrētu programmu () Azure Active Directory un Azure AD iespējotu autentifikāciju, izpildiet darbības, kas sadaļā [Izmantot Azure Active Directory ar pielāgotu savienotāju sadaļā Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Apkopojiet tālāk norādītos lietojumprogrammas WINDOWS Azure portālā. Šie umi būs vajadzīgi soļos, kas seko.

- Klienta lietojumprogrammas ID
- Klienta direktorija (nomnieka) ID

Lai pievienotu jaunu programmas reģistrāciju Commerce Site Builder, veiciet šos soļus.

1. Dodieties uz **Sākumlapa \> Atsauksmes \> Iestatījumi**.
1. Sadaļā **Pakalpojums-pakalpojumam (S2S) autentifikācija** atlasiet **Pārvaldīt**.

    ![Pārvaldīt pogu Commerce Site Builder sadaļā Pakalpojums-pakalpojumam (S2S) Autentifikācija.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. **S2S programmas ierakstu rūtī**, kas tiek parādīta labajā pusē, atlasiet **Pievienot jaunu S2S programmas reģistrāciju**.
1. **Dialoglodziņā Pievienot S2S programmas ievadni** ievadiet tālāk norādīto nepieciešamo informāciju. Izmantojiet Azure programmas reģistrācijas vērtības.

    - **Nosaukums** – ievadiet programmas nosaukumu (piemēram, **Fabrikam App**).
    - **Klienta programmas ID** - ievadiet programmas ID (piemēram **00000000-0000-0000-0000-000000000000**).
    - **Direktorija (nomnieka) ID** – ievadiet direktorija ID (piemēram, **00000000-0000-0000-0000-000000000000**).

    ![Pievienojiet S2S programmas ieraksta dialoglodziņu programmas Commerce Site Builder.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Atlasiet **Iesniegt**. Programmas nosaukumam ir jābūt redzamam S2S **programmas ierakstu rūts** sarakstā.
1. **Aizveriet S2S programmas ierakstu rūti**.
1. Atlasiet **Saglabāt**.

## <a name="edit-an-existing-app-registration"></a>Rediģēt esošu programmas reģistrāciju

Lai rediģētu esošo programmas reģistrāciju Commerce Site Builder, veiciet šos soļus.

1. Dodieties uz **Sākumlapa \> Atsauksmes \> Iestatījumi**.
1. Sadaļā **Pakalpojums-pakalpojumam (S2S) autentifikācija** atlasiet **Pārvaldīt**.
1. **S2S programmas ievadņu** rūtī atlasiet blakus ievadnei, ko vēlaties rediģēt, blakus S2S programmas ierakstiem.
1. Pēc vajadzības atjauniniet **vērtības** laukos **Nosaukums, Klienta programmas** ID **un Direktorija (Nomnieks**).
1. Atlasiet **Iesniegt**.
1. **Aizveriet S2S programmas ierakstu rūti**.
1. Atlasiet **Saglabāt**.

## <a name="remove-an-existing-app-registration"></a>Noņemt esošu programmas reģistrāciju

Lai noņemtu esošu programmas reģistrāciju Commerce Site Builder, veiciet šos soļus.

1. Dodieties uz **Sākumlapa \> Atsauksmes \> Iestatījumi**.
1. Sadaļā **Pakalpojums-pakalpojumam (S2S) autentifikācija** atlasiet **Pārvaldīt**.
1. **S2S lietojumprogrammas ierakstu** rūtī atlasiet ieejas, kuru vēlaties noņemt, blakus ierakstam. Ieraksts ir noņemts no saraksta.
1. **Aizveriet S2S programmas ierakstu rūti**.
1. Atlasiet **Saglabāt**.

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Piekrišana izmantot vērtējumus un atsauksmes](opt-in-ratings-reviews.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Vērtējumu un atsauksmju konfigurēšana](configure-ratings-reviews.md)

[Preču vērtējumu sinhronizācija](sync-product-ratings.md)

[Iespējojiet moderatora manuālo vērtējumu un atsauksmju publicēšanu](manual-publish-rating-reviews.md)

[Novērtējumu un pārskatu importēšana un eksportēšana](import-export-reviews.md)

[BUJ par vērtējumiem un atsauksmēm](ratings-reviews-faq.md) 
