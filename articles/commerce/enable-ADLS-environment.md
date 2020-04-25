---
title: ADLS iespējošana Dynamics 365 Commerce vidē
description: Šajā tēmā paskaidrots, kā iespējot un pārbaudīt Azure Data Lake Storage (ADLS) Dynamics 365 Commerce videi, kas ir priekšnosacījums preču ieteikumu iespējošanai.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba428765babb9ca7566da7a457368959b1c29083
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259752"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>ADLS iespējošana Dynamics 365 Commerce vidē

[!include [banner](includes/banner.md)]

Šajā tēmā paskaidrots, kā iespējot un pārbaudīt Azure Data Lake Storage (ADLS) Dynamics 365 Commerce videi, kas ir priekšnosacījums preču ieteikumu iespējošanai.

## <a name="overview"></a>Pārskats

Risinājumā Dynamics 365 Commerce visa informācija par preci un transakciju tiek izsekota vides elementu krātuvē. Lai šos datus padarītu pieejamus citiem Dynamics 365 pakalpojumiem, piemēram, datu analīzei, biznesa informācijai un personalizētiem ieteikumiem, šī vide jāsavieno ar debitoram piederošu Azure Data Lake Storage Gen 2 (ADLS) risinājumu.

Tā kā ADLS ir konfigurēta vidē, visi nepieciešamie dati tiek atspoguļoti no elementu krātuves, tomēr tie joprojām tiek aizsargāti un atrodas klienta kontrolē.

Ja arī preču ieteikumi vai personalizētie ieteikumi vidē ir iespējoti, preču ieteikumu stekam tiks piešķirta piekļuve īpašajai ADLS mapei, lai izgūtu debitora datus un apstrādātu ieteikumus, pamatojoties uz to.

## <a name="prerequisites"></a>Priekšnosacījumi

Debitoriem piederošajā Azure abonementā jābūt konfigurētai ADLS. Šī tēma neattiecas uz Azure abonementa iegādi vai ADLS iespējota krātuves konta iestatīšanu.

Papildinformāciju par ADLS skatiet [ADLS oficiālajos dokumentos](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurācijas darbības

Šajā sadaļā ir aprakstītas konfigurācijas darbības, kas nepieciešamas, lai nodrošinātu ADLS vidē, kas saistīta ar preces ieteikumiem.
Lai iegūtu padziļinātu pārskatu par darbībām, kas nepieciešamas ADLS iespējošanai, skatiet [Elementu krātuves pārvēršana par Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-adls-in-the-environment"></a>ADLS iespējošana vidē

1. Piesakieties vides iekšējās uzskaites daļas portālam.
1. Sameklējiet **Sistēmas parametri** un dodieties uz cilni **Datu savienojumi**. 
1. Iestatiet **Iespējot Data Lake integrāciju** uz **Jā**.
1. Iestatiet **Pakāpeniski atjaunināt Data Lake** uz **Jā**.
1. Pēc tam ievadiet tālāk norādīto informāciju.
    1. **Pieteikuma ID** // **Pieteikuma noslēpums** // **DNS nosaukums** — nepieciešams, lai izveidotu savienojumu ar KeyVault, kur tiek glabāts ADLS noslēpums.
    1. **Slepenais nosaukums** — slepenais nosaukums, kas tiek glabāts KeyVault un tiek izmantots, lai veiktu autentifikāciju ar ADLS.
1. Saglabājiet izmaiņas lapas augšējā kreisajā stūrī.

Tālāk redzamajā attēlā ir parādīts ADLS konfigurācijas piemērs.

![ADLS konfigurācijas piemērs](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>ADLS savienojuma pārbaude

1. Pārbaudiet savienojumu ar KeyVault, izmantojot saiti **Pābaudīt Azure Key Vault**.
1. Pārbaudiet savienojumu ar ADLS, izmantojot saiti **Pābaudīt Azure krātuvi**.

> [!NOTE]
> Ja pārbaudes nav veiksmīgs, vēlreiz pārbaudiet, vai visa iepriekš pievienotā KeyVault informācija ir pareiza, un pēc tam mēģiniet vēlreiz.

Kad savienojuma pārbaudes ir veiksmīgas, jāiespējo automātiska elementu krātuves atsvaidzināšana.

Lai iespējotu automātisku elementu krātuves atsvaidzināšanu, veiciet tālāk aprakstītās darbības.

1. Sameklējiet **Elementu krātuvi**.
1. Kreisajā pusē esošajā sarakstā dodieties uz ierakstu **RetailSales** un atlasiet **Rediģēt**.
1. Pārliecinieties, ka opcija **Iespējota automātiskā atsvaidzināšana** ir iestatīta **Jā**, atlasiet **Atsvaidzināt** un pēc tam atlasiet **Saglabāt**.

Tālak redzamaja attēlā parādīts elementu veikala ar iespējotu automātisku atsvaidzināšanu piemērs.

![Elementu krātuves ar iespējotu automātisku atsvaidzināšanu piemērs](./media/exampleADLSConfig2.png)

Tagad ADLS ir konfigurēta videi. 

Ja tas vēl nav pabeigts, sekojiet norādījumiem par [preču ieteikumu iespējošanu un personalizāciju](enable-product-recommendations.md) videi.

## <a name="additional-resources"></a>Papildu resursi

[Elementu krātuves pārvēršana par Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)
