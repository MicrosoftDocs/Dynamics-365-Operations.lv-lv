---
title: Debitora sertifikāti un noslēpumi
description: Šajā rakstā skaidrots, kā iestatīt debitora sertifikātus un slepus Elektronisko rēķinu izrakstīšanai.
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
ms.openlocfilehash: a4d33135bf352a4c4a245e597e0c3c7467317864
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880665"
---
# <a name="customer-certificates-and-secrets"></a>Debitora sertifikāti un noslēpumi

[!include [banner](../includes/banner.md)]

Ja atsauce Key Microsoft Azure Papildmaksas jau ir regulēšanas konfigurācijas pakalpojumā (RCS), ir iespējams izveidot atsauces uz atslēgas lauvām un noslēpumiem. Ja vēl nav atslēgas [Atsauču To ir, skatiet pakalpojumu](e-invoicing-service-environments.md) vides, lai iegūtu informāciju par to, kā to izveidot.

## <a name="create-certificates-and-secrets"></a>Izveidot sertifikātus un noslēpumus

Lai izveidotu un iestatītu sertifikātus un noslēpumus, sekojiet šiem soļiem.

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. **Lapas Vides iestatījums** darbību rūtī atlasiet Pakalpojuma **vides**.
4. **Lapas Pakalpojumu vides darbību** rūtī atlasiet Atslēgas Pasūtījuma **parametri**.
5. Lapā Atslēgas **Laika parametri** atlasiet atslēgu Atsauču atsauču un pēc tam sadaļā **Sertifikāti** atlasiet **Pievienot**.
6. Laukā **Nosaukums** ievadiet atslēgas pasūtījuma sertifikāta vai noslēpuma nosaukumu. Papildinformāciju skatiet [Azure glabāšanas konta izveidošana Azure portālā](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Ievadiet aprakstu laukā **Apraksts**.
8. Laukā **Tips** atlasiet **Sertifikātu**, ja atsaucaties uz sertifikātu, kas tiek saglabāts atslēgā. Atlasiet **Noslēpums**, ja atsaucaties uz noslēpumu, kas ir saglabāts atslēgas līdzās.
9. Atlasiet **Saglabāt**.

> [!NOTE]
> Dažos scenārijos ir jāizmanto publiskie sertifikāti ar .cer faila nosaukuma paplašinājumu. Tomēr atslēgas Uzrēja neatbalsta šī tipa sertifikātu importēšanu un uzglabāšanu kā Atslēgas saknes sertifikātus. Šajos scenārijos .cer fails ir jāsaglabā kā bāzes 64 šifrēts X.509 (. CER) virkne. Pēc tam Atslēgas noslēpumā saglabājiet **virkni, kas parādās starp sākuma** sertifikāta rindu un **BEIGU** SERTIFIKĀTA rindu failā. Pakalpojumu vidē joprojām ir jāizveido atsauce uz atslēgas Pasūtījuma ierakstu un jāiestata tipa **lauks** uz **Sertifikāts**.

## <a name="create-a-chain-of-certificates"></a>Izveidot sertifikātu ķēdi

Ja jūsu valstij/reģionam specifiskiem rēķiniem nepieciešama sertifikātu ķēde, lai pielietotu ciparparakstus vai izveidotu drošu (Secure Sockets Layer \[SSL\]) savienojumu ar ārējiem tīmekļa pakalpojumiem, izveidojiet sertifikātu ķēdi, kur sertifikāti ir šādā secībā:

1. Saknes sertifikāti
2. Vidējie sertifikāti
3. Lietotāju sertifikāti

Saknes sertifikātu iestādes (CAs) ir uzticams sertifikātu avots. Vidējie CA sertifikāti ir pagaidu sertifikāti, kas saista lietotāja sertifikātus ar saknes CA sertifikātiem.

Lai izveidotu un iestatītu sertifikātu ķēdi, sekojiet šiem soļiem.

1. **Cilnes Ķēžu** parametru lapas darbību rūtī atlasiet **Sertifikātu ķēde**.
2. Atlasiet **Jauns**, lai izveidotu sertifikātu ķēdi.
3. **Laukā** Nosaukums ievadiet sertifikātu ķēdes nosaukumu.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Sadaļā **Sertifikāti** atlasiet **Pievienot**, lai pievienotu ķēdei sertifikātu.
6. Izmantojiet pogu **Augšā** vai **Lejā**, lai mainītu sertifikāta pozīciju ķēdē. Paturiet CA saknes sertifikātu saraksta augšpusē un gala lietotāja sertifikātu apakšpusē.
7. Atlasiet **Saglabāt**.

Varat izveidot tik daudz galvenās Atsauču RCS, cik vēlaties. Atcerieties, ka glabāšanas koplietojamās piekļuves paraksta (SAS) marķiera noslēpums tiek izmantots, lai saistītu šo pakalpojuma vidi ar atsauci KeyHar. Varat atsaukties uz Atslēgas Atsauču sertifikātiem un noslēpumiem, kas ir saglabāti atslēgas noliktavā, kas arī satur glabāšanas SAS pilnvaras, ko izmantojat, iestatot pakalpojumu vidi.
