---
title: Klientu apliecības un noslēpumi
description: Šajā tēmā ir paskaidrots, kā iestatīt klientu sertifikātus un noslēpumus elektroniskajos rēķinos.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1325cad95e9a6dc470691f5f168439fccaaa78e1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371956"
---
# <a name="customer-certificates-and-secrets"></a>Klientu apliecības un noslēpumi

[!include [banner](../includes/banner.md)]

Ja regulatīvajā konfigurācijas pakalpojumā (RCS) jau ir Microsoft Azure atslēgas seifu atsauce, varat izveidot atsauces uz atslēgu seifu sertifikātiem un noslēpumiem. Ja jums vēl nav atslēgas [seifu atsauces, informāciju par to, kā to izveidot, skatiet](e-invoicing-service-environments.md) sadaļā Pakalpojumu vides.

## <a name="create-certificates-and-secrets"></a>Sertifikātu un noslēpumu izveide

Lai izveidotu un iestatītu sertifikātus un noslēpumus, rīkojieties šādi.

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. **Lapas Vides iestatījums** darbību rūtī atlasiet Pakalpojuma **vides**.
4. **Lapas Pakalpojumu vides darbību** rūtī atlasiet Atslēgas Pasūtījuma **parametri**.
5. **Lapā Taustiņu seifu parametri** atlasiet taustiņu seifu atsauci un pēc tam **sadaļā Sertifikāti** atlasiet **Pievienot**.
6. Laukā **Nosaukums** ievadiet Atslēgas seifu sertifikāta vai noslēpuma nosaukumu. Papildinformāciju skatiet [Azure glabāšanas konta izveidošana Azure portālā](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Ievadiet aprakstu laukā **Apraksts**.
8. Laukā **Tips** atlasiet **Sertifikāts**, ja atsaucaties uz sertifikātu, kas tiek glabāts atslēgu glabātavā. Atlasiet **Slepeni**, ja atsaucaties uz noslēpumu, kas tiek glabāts atslēgas seifā.
9. Atlasiet **Saglabāt**.

> [!NOTE]
> Dažos gadījumos ir jāizmanto publiskie sertifikāti, kuriem ir .cer faila nosaukuma paplašinājums. Tomēr Key Vault neatbalsta šāda veida sertifikātu importēšanu un glabāšanu kā Key Vault sertifikātus. Šādos gadījumos .cer fails jāsaglabā kā bāzes 64 kodēts X.509 (. CER) virkne. Pēc tam taustiņu seifā glabājiet virkni, kas failā parādās starp **rindu BEGIN CERTIFICATE** un **rindu END CERTIFICATE**. Servisa vidē joprojām ir jāizveido atsauce uz atslēgas seifu ierakstu un jāiestata **lauks Tips** uz **Sertifikāts**.

## <a name="create-a-chain-of-certificates"></a>Sertifikātu ķēdes izveide

Ja jūsu valstij/reģionam raksturīgajiem rēķiniem ir nepieciešama sertifikātu ķēde, lai lietotu ciparparakstus vai izveidotu drošu (Secure Sockets Layer \[SSL\]) savienojumu ar ārējiem tīmekļa pakalpojumiem, izveidojiet sertifikātu ķēdi, kurā sertifikāti ir šādā secībā:

1. Saknes sertifikāti
2. Starpsertifikāti
3. Galalietotāju sertifikāti

Saknes sertificēšanas iestādes (CA) ir uzticams sertifikātu avots. Starpposma CA sertifikāti ir tilti, kas saista galalietotāja sertifikātus ar saknes CA sertifikātiem.

Lai izveidotu un iestatītu sertifikātu ķēdi, rīkojieties šādi.

1. **Lapas Atslēgu seifu parametri** darbību rūtī atlasiet **Sertifikātu** ķēde.
2. Atlasiet **Jauns**, lai izveidotu sertifikātu ķēdi.
3. Laukā **Nosaukums** ievadiet sertifikātu ķēdes nosaukumu.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Sadaļā **Sertifikāti** atlasiet **Pievienot**, lai pievienotu ķēdei sertifikātu.
6. Izmantojiet pogu **Augšā** vai **Lejā**, lai mainītu sertifikāta pozīciju ķēdē. Glabājiet CA saknes sertifikātu saraksta augšdaļā un lietotāja sertifikātu apakšā.
7. Atlasiet **Saglabāt**.

Jūs varat izveidot tik daudz Key Vault atsauču RCS, cik vēlaties. Atcerieties, ka krātuves koplietojamās piekļuves paraksta (SAS) pilnvaras noslēpums tiek izmantots, lai saistītu noteiktu pakalpojuma vidi ar Key Vault atsauci. Varat atsaukties uz Key Vault sertifikātiem un noslēpumiem, kas tiek glabāti atslēgu glabātuvē, kurā ir arī krātuves SAS pilnvaru noslēpums, ko izmantojat, iestatot pakalpojuma vidi.
