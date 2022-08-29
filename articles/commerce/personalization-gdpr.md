---
title: Atteikšanās no personalizētiem ieteikumiem
description: Šajā rakstā skaidrots, kā ļaut debitoriem izvēlēties saņemt personalizētus ieteikumus Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 5d75f1ae4ec8fbccd00635d3c245a5ae7c1e1dff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283673"
---
# <a name="opt-out-of-personalized-recommendations"></a>Atteikšanās no personalizētiem ieteikumiem

[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā ļaut debitoriem izvēlēties saņemt personalizētus ieteikumus Microsoft Dynamics 365 Commerce.

Konta izveides laikā tiek automātiski iestatīts, ka jauni debitori saņems personalizētus ieteikumus. Tomēr Dynamics 365 Commerce piedāvā dažādus veidus, kā mazumtirgotāji ļauj lietotājiem izvēlēties nesaņemt šos ieteikumus un ierobežot savu personas datu apstrādi. Autentificēti lietotāji, kas atsakās saņemt personalizētus ieteikumus, nekavējoties beigs redzēt personalizētos sarakstus. Turklāt visi personiskie dati, kas tiek vākti personalizēšanai, tiks noņemti no personalizēto ieteikumu modeļiem.

Papildinformāciju par preču personalizēto ieteikumu saņemšanu skatiet sadaļā [Personalizēto ieteikumu iespējošana](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Veidi, kā mazumtirgotājiem ieviest atteikšanās iespēju

Mazumtirgotājiem ir trīs veidi, kādos ieviest atteikšanās iespēju.

### <a name="opting-out-on-behalf-of-users"></a>Atteikšanās lietotāju vārdā

Kontu pārvaldībā Commerce atbalsta birojā tirgotāji var atteikties lietotāju vārdā.

1. Vadības sākumlapā meklējiet **visus debitorus**.
1. Meklējiet un atlasiet debitoru un pēc tam atlasiet **mazumtirdzniecības** kopsavilkuma cilni.

    ![Mazumtirdzniecības kopsavilkuma cilnes.](./media/Disablepersonalizationpart1.png)

1. Sadaļā **Konfidencialitāte** iestatiet opciju **Atspējot personalizāciju** uz **Jā**.

    ![Konfidencialitātes iestatījumi.](./media/Disablepersonalizationpart2.png)

1. Atlasiet **Saglabāt** un aizveriet lapu.

### <a name="module-based-opt-out-experience"></a>Modulī balstīta atteikšanās iespēja

Mazumtirgotāji var ļaut autentificētiem lietotājiem pašiem atteikties no personalizētajiem ieteikumiem. Lai nodrošinātu šo atteikšanās iespēju, pievienojiet lietotāja atteikšanās moduli klienta konta profila lapām.

### <a name="custom-extensions"></a>Pielāgoti paplašinājumi

Mazumtirgotāji var izveidot savus paplašinājumus, lai pārvaldītu lietotāju atteikšanās pieredzi. Papildinformāciju skatiet šeit [Retail Server API izsaukšana](e-commerce-extensibility/call-retail-server-apis.md) un [Tiešsaistes kanāla paplašināšana](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Iegūstiet personalizēto ieteikumu datu digitālo kopiju autentificēta lietotāja vārdā

Klienti var vēlēties iegūt savu personas datu digitālo kopiju un arī skatīt eksportētus ieteikumu rezultātus. Ja debitors pieprasa šo informāciju, mazumtirgotājam ir jāizveido pielāgots paplašinājums, kas izsauc Retail Server pieteikuma programmēšanas interfeisu (API) un veic vaicājumus par visiem rezultātiem no **Ieteikumu** saraksta, pamatojoties uz klienta ID. Pēc tam rezultātus var eksportēt ar komatu atdalītu vērtību (CSV) formātā un koplietot ar debitoru.

Šajā piemērā parādīts, kā mazumtirgotājs var izpildīt šo uzdevumu.

1. Mazumtirgotājs izveido pielāgotu paplašinājumu, lai izvilktu personisku ieteikumu datus lietotāja vārdā. Lai iegūtu informāciju par to, kā izveidot moduļus, klonēt esošos moduļus, izsaukt Retail Server API un izsaukt datu darbības, skatiet [Tiešsaistes kanāla paplašināmība](e-commerce-extensibility/overview.md).
2. Pielāgotais paplašinājums veic zvanu **get-recommendations** pamatdatu darbībai, un nodod tai nepieciešamo informāciju, pamatojoties uz saraksta prasībām. **Ieteikumu** saraksts gadījumā paplašinājumam ir jānodod pareizais saraksta nosaukums un klienta ID datu darbībai.

    Viens no veidiem, kā izveidot pielāgotu paplašinājumu, ir klonēt esošo preču ievākšanas moduli, kas tiek izmantots ieteikumu rezultātu atgriešanai. Klonējot šo esošo moduli, mazumtirgotājs var modificēt esošo kodu un pievienot jaunu pogu, kas eksportē ieteikumu rezultātus CSV failā. Papildinformāciju skatiet [Moduļu bibliotēkas moduļa klonēšana](e-commerce-extensibility/clone-starter-module.md) un [Preču kolekcijas moduļi](product-collection-module-overview.md).

    Lai pilnībā skatītu Retail Server API bibliotēku, skatiet sadaļu [Retail Server klientu un patērētāju API](dev-itpro/retail-server-customer-consumer-api.md).

3. Pēc tam, kad ir izveidots pielāgots paplašinājums, tirgotājs var eksportēt CSV failu no visiem ieteikumu rezultātiem, balstoties uz autentificētā lietotāja unikālo klienta ID.
4. Mazumtirgotājs var koplietot eksportēto CSV failu, kurā ir ietverts pilns ieteikto preču saraksts ar autentificēto lietotāju.

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Preču ieteikumu pievienošana punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
