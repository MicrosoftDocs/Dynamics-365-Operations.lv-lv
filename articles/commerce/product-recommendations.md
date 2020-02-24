---
title: Preču ieteikumu apskats
description: Šajā tēmā ir sniegta vispārīga informācija par preču ieteikumiem. Preču ieteikumi ļauj klientiem viegli un ātri atrast preces, ko viņi vēlas, un pat tādas preces, kuras viņi sākotnēji neplānoja nopirkt.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024983"
---
# <a name="product-recommendations-overview"></a>Preču ieteikumu apskats

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce var izmantot, lai parādītu preces ieteikumus e-tirdzniecības vietnē un pārdošanas punkta (POS) ierīcē. Preces ieteikumi ir preces, kas varētu interesēt klientu. Ieteikumi ir balstīti uz citu klientu pirkšanas tendencēm citiem klientiem tiešsaistes un parastajos veikalos.

Preces ieteikumi ļauj klientiem viegli un ātri atrast preces, ko viņi vēlas, gūstot noderīgu pieredzi. Papildus preču pārdošana un citu preču pārdošana var pat tikt izmantota, lai palīdzētu klientiem atrast papildu preces, ko viņi sākotnēji nebija iecerējuši pirkt. Kad ieteikumi tiek izmantoti, lai palīdzētu atklāt preces, tie var izveidot vairāk pārvēršanas iespēju, palīdzēt palielināt pārdošanas ieņēmumus un pat palīdzēt uzlabot klientu apmierinātību un lojalitāti.

Commerce preces ieteikumi darbojas, plašā mērogā izmantojot Microsoft Recommendations mašīnmācības tehnoloģijas.


## <a name="scenarios"></a>Scenāriji

Preču ieteikumi ir pieejami tālāk minētajiem POS scenārijiem.

- **Jebkurā veikala lapā, kas paredzēta pārlūkošanai vai kā mērķlapa e-tirdzniecībā:** ja klienti vai veikala partneri apmeklē veikala lapu, ieteikumu programma var ieteikt preces sarakstos **Jauns**, **Vispirktākais** un **Populārs**.
- **Preces detalizētas informācijas lapā:** ja klienti vai veikala partneri apmeklē lapu **Preces detalizēta informācija**, ieteikumu programma iesaka papildu preces, kas arī iespējams tiks iegādātas. Šīs preces parādās sarakstā **Pircējiem patīk arī**.
- **Transakciju lapā vai izrakstīšanas lapā:** ieteikumu programma piedāvā preces, balstoties uz visu grozā esošo preču sarakstu. Šie krājumi parādās sarakstā **Bieži iegādāts kopā**.
- **Personalizētie ieteikumi:** Tirgotāji var nodrošināt pieteiktajiem klientiem personalizētu **ieteikumu** sarakstu līdztekus jaunajai funkcionalitātei, kas ļauj esošajiem saraksta scenārijiem tikt personalizētiem, pamatojoties uz šo klientu. Lai iegūtu papildinformāciju, lūdzu, skatiet līdzekļu dokumentu: [personalizētu ieteikumu iespējošana.](personalized-recommendations.md)

## <a name="recommendation-service"></a>Recommendation pakalpojums

Preces ieteikumi izmanto Recommendations mašīnmācības tehnoloģijas tālāk minētajā veidā.

- No Commerce operacionālās datu bāzes tiek izgūti Recommendation pakalpojumam nepieciešamā formāta dati, un šie dati tiek nosūtīti Entity krātuvei.
- Recommendation pakalpojums izmanto datus, lai apmācīt ieteikumu modeļus sarakstiem **Pircējiem patīk arī**, **Bieži iegādāts kopā**, **Jauns**, **Vispirktākais** un **Populārs**.

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu iespējošana](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Preču kolekcijas moduļa apskats](product-collection-module-overview.md)

[Pārraudzītu preču ieteikumu sarakstu izveide](create-editorial-recommendation-lists.md)

[Uz AI-ML balstītu preču ieteikumu rezultātu pārvaldība](modify-product-recommendation-results.md)

[Preču ieteikumu sarakstu pievienošana lapām](add-reco-list-to-page.md)
