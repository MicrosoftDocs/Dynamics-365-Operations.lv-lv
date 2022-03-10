---
title: Azure Data Lake Storage iespējošana Dynamics 365 Commerce vidē
description: Šajā tēmā sniegti norādījumi, kā savienot Azure Data Lake Storage Gen 2 risinājumu ar Dynamics 365 Commerce vides entitīju veikalu. Tā ir obligāta darbība pirms produktu rekomendāciju iespējošanas.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c96c29a4d9639b02e6a60ad938b7e06f7d500c68
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466296"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Azure Data Lake Storage iespējošana Dynamics 365 Commerce vidē

[!include [banner](includes/banner.md)]

Šajā tēmā sniegti norādījumi, kā savienot Azure Data Lake Storage Gen 2 risinājumu ar Dynamics 365 Commerce vides entitīju veikalu. Tā ir obligāta darbība pirms produktu rekomendāciju iespējošanas.

Dynamics 365 Commerce risinājumā dati, kuri ir vajadzīgi, lai aprēķinātu rekomendācijas, preces un transakcijas, tiek apkopoti vides entitīju veikalā. Lai šos datus padarītu pieejamus citiem Dynamics 365 pakalpojumiem, piemēram, datu analīzei, biznesa informācijai un personalizētiem ieteikumiem, vide ir jāpieslēdz klientam piederošam Azure Data Lake Storage Gen 2 risinājumam.

Pēc tam, kad ir izpildītas visas iepriekš noteiktās darbības, visi vides entitīju veikala klientu dati tiek automātiski spoguļoti klienta Azure Data Lake Storage Gen 2 risinājumā. Kad ieteikumu līdzekļi tiek iespējoti ar Līdzekļu pārvaldības darbvietu Commerce galvenajā pārvaldē, ieteikumu kopai būs atļauja piekļūt tam pašam Azure Data Lake Storage Gen 2 risinājumam.

Visa procesa laikā klientu dati paliek aizsargāti un atrodas viņu pārvaldībā.

## <a name="prerequisites"></a>Priekšnosacījumi

Dynamics 365 Commerce vides entitīju veikalam jābūt savienotam ar Azure Data LAke Gen Storage Gen 2 kontu un pavadošajiem pakalpojumiem.

Papildinformāciju par Azure Data Lake Storage Gen 2 un to, kā to iestatīt, skatiet rakstā [Azure Data Lake Storage Gen 2 oficiālā dokumentācija](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurācijas darbības

Šajā sadaļā aprakstītas konfigurēšanas darbības, kuras jāveic, lai iespējotu Azure Data Lake Storage Gen 2 vidē, jo tā ir saistīta ar preču ieteikumiem.
Padziļinātāku pārskatu par darbībām, kuras vajadzīgas, lai iespējotu Azure Data Lake Storage Gen 2, skatiet rakstā [Padarīt entitīju veikalu pieejamu kā Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Azure Data Lake Storage iespējošana vidē

1. Piesakieties vides iekšējās uzskaites daļas portālam.
1. Sameklējiet **Sistēmas parametri** un dodieties uz cilni **Datu savienojumi**. 
1. Iestatiet **Iespējot Data Lake integrāciju** uz **Jā**.
1. Pēc tam ievadiet tālāk norādīto informāciju.
    1. **Pieteikuma ID** // **Pieteikuma noslēpums** // **DNS nosaukums** — jāizveido savienojums ar KeyVault, kur tiek glabāts Azure Data Lake Storage noslēpums.
    1. **Slepenais nosaukums** — slepenais nosaukums, kas tiek glabāts KeyVault un tiek izmantots, lai veiktu autentifikāciju ar Azure Data Lake Storage.
1. Saglabājiet izmaiņas lapas augšējā kreisajā stūrī.

Tālāk redzamajā attēlā ir parādīts Azure Data Lake Storage konfigurācijas piemērs.

![Pakalpojuma Azure Data Lake Storage konfigurācijas piemērs.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Azure Data Lake Storage savienojuma pārbaude

1. Pārbaudiet savienojumu ar KeyVault, izmantojot saiti **Pābaudīt Azure Key Vault**.
1. Pārbaudiet savienojumu ar Azure Data Lake Storage, izmantojot saiti **Pābaudīt Azure krātuvi**.

> [!NOTE]
> Ja neviena pārbaude neizdodas, apstipriniet, ka visa KeyVault informācija, kas pievienota augstāk, ir pareiza, un mēǵiniet vēlreiz.

Kad savienojuma pārbaudes ir veiksmīgas, jāiespējo automātiska elementu krātuves atsvaidzināšana.

Lai iespējotu automātisku elementu krātuves atsvaidzināšanu, veiciet tālāk aprakstītās darbības.

1. Sameklējiet **Elementu krātuvi**.
1. Kreisajā pusē esošajā sarakstā dodieties uz ierakstu **RetailSales** un atlasiet **Rediģēt**.
1. Pārliecinieties, ka opcija **Iespējota automātiskā atsvaidzināšana** ir iestatīta **Jā**, atlasiet **Atsvaidzināt** un pēc tam atlasiet **Saglabāt**.

Tālak redzamaja attēlā parādīts elementu veikala ar iespējotu automātisku atsvaidzināšanu piemērs.

![Elementu krātuves ar iespējotu automātisku atsvaidzināšanu piemērs.](./media/exampleADLSConfig2.png)

Azure Data Lake Storage tagad ir konfigurēta videi. 

Ja tas vēl nav pabeigts, sekojiet norādījumiem par [preču ieteikumu iespējošanu un personalizāciju](enable-product-recommendations.md) videi.

## <a name="additional-resources"></a>Papildu resursi

[Elementu krātuves pārvēršana par Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Preču ieteikumu pievienošana punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
