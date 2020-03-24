---
title: Preču ieteikumu apskats
description: Šajā tēmā ir sniegta vispārīga informācija par preču ieteikumiem. Preču ieteikumi ļauj klientiem viegli un ātri atrast preces, ko viņi vēlas, un pat tādas preces, kuras viņi sākotnēji neplānoja nopirkt.
author: Moonma
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: abeeb3c35c21f6d7a6ec24a84522033f9a5367f3
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127863"
---
# <a name="product-recommendations-overview"></a>Preču ieteikumu apskats

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce var izmantot, lai parādītu preces ieteikumus e-tirdzniecības vietnē un pārdošanas punkta (POS) ierīcē. Preces ieteikumi ir preces, kas varētu interesēt klientu. Ieteikumi ir balstīti uz citu klientu pirkšanas tendencēm citiem klientiem tiešsaistes un parastajos veikalos.

Preces ieteikumi ļauj klientiem viegli un ātri atrast preces, ko viņi vēlas, gūstot noderīgu pieredzi. Papildu preču pārdošana un citu preču pārdošana var pat tikt izmantota, lai palīdzētu klientiem atrast papildu preces, ko viņi sākotnēji nebija iecerējuši pirkt. Kad ieteikumi tiek izmantoti, lai uzlabotu preču atklāšanu, tie var izveidot vairāk pārvēršanas iespēju, palīdzēt palielināt pārdošanas ieņēmumus un pat palīdzēt uzlabot klientu apmierinātību un lojalitāti.

E-Commerce preces ieteikumi darbojas, plašā mērogā izmantojot Microsoft Recommendations mašīnmācības tehnoloģijas.

## <a name="recommendation-service"></a>Recommendation pakalpojums

Preču ieteikumu pakalpojums izmanto mākslīgās izlūkošanas un mašīnu mācīšanās (AI-ML) tehnoloģijas, kas ir sekojošā veidā:

- No Commerce operacionālās datu bāzes tiek izgūti Recommendation pakalpojumam nepieciešamā formāta dati, un šie dati tiek nosūtīti Azure data lake storage (ADLS) vai Entītiju krātuvei.
- Ieteikumu pakalpojums izmanto saglabātos datus, lai apmācītu ieteikumu modeļus sarakstiem **Pircējiem patīk arī**, **Bieži iegādāts kopā**, **Jauns**, **Vispirktākais** un **Populārs**.

## <a name="scenarios"></a>Scenāriji

Preču ieteikumi ir pieejami tālāk minētajiem POS scenārijiem.

- **Jebkurā veikala lapā, kas paredzēta pārlūkošanai vai kā mērķlapa e-tirdzniecībā:** ja klienti vai veikala partneri apmeklē veikala lapu, ieteikumu programma var ieteikt preces sarakstos **Jauns**, **Vispirktākais** un **Populārs**.
- **Preces detalizētas informācijas lapā:** ja klienti vai veikala partneri apmeklē lapu **Preces detalizēta informācija**, ieteikumu programma iesaka papildu preces, kas arī iespējams tiks iegādātas. Šīs preces parādās sarakstā **Pircējiem patīk arī**.
- **Transakciju lapā vai izrakstīšanas lapā:** ieteikumu programma piedāvā preces, balstoties uz visu grozā esošo preču sarakstu. Šie krājumi parādās sarakstā **Bieži iegādāts kopā**.
- **Personalizētie ieteikumi:** Tirgotāji var nodrošināt pieteiktajiem klientiem personalizētu **ieteikumu** sarakstu līdztekus jaunajai funkcionalitātei, kas ļauj esošajiem saraksta scenārijiem tikt personalizētiem, pamatojoties uz šo klientu. Lai uzzinātu vairāk, skatiet [Personalizētu ieteikumu iespējošana](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Preču ieteikumu veidi

Sekojošajā tabulā ir aprakstīti dažādi automatizēto preču ieteikumu veidi, kas pieejami mazumtirgotājiem risinājumā Dynamics 365 Commerce, lai to varētu ieviest, izmantojot [preču kolekcijas moduli](product-collection-module-overview.md). Mazumtirgotāji var parādīt lietotāja, kas ir pierakstījies, personalizētus rezultātus, ja vietnes autors izvēlas šo opciju.

| Preču kolekcijas modulis  | tips | apraksts |
|----------------------------|------|-------------|
| Jauna                        | Algoritmisks | Šis modulis rāda sarakstu ar jaunākajām precēm, kas ir nesen sašķirotas kanālos un katalogos. |
| Vispirktākais               | Algoritmisks | Šis modulis rāda preču sarakstu, kas ir sarindotas pēc lielākā pārdošanas apjoma. |
| Populāri                   | Algoritmisks | Šis preču kolekcijas moduļa veids parāda preču ar augstāku veiktspēju sarakstu noteiktā periodā, sarindota pēc lielākā pārdošanas skaita.  |
| Bieži iegādāti kopā | AI-ML | Šis modulis rekomendē sarakstu ar ieteiktajiem produktiem, kuri parasti tiek iegādāti kopā ar patērētāja pašreizējā groza saturu. |
| Cilvēkiem patīk arī           | AI-ML | Šis modulis iesaka preces noteiktam sēklas produktam, pamatojoties uz patēriņa pirkšanas modeļiem. |
| Ieteikumi              | AI-ML | Šis modulis rekomendē personificētu preču sarakstu, pamatojoties uz pierakstītā lietotāja pirkšanas modeļiem. Lietotājam-viesim šis saraksts tiks sakļauts. |

## <a name="additional-resources"></a>Papildu resursi

[ADLS iespējošana Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Preču ieteikumu sarakstu pievienošana e-komercijas vietnei](add-reco-list-to-page.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)
