---
title: Iespējot "pirkt līdzīgas preces" rekomendācijas
description: Šajā tēmā aprakstīts, kā iespējot "pirkt līdzīgas preces" preču ieteikumus programmā Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
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
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818378"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Iespējot "pirkt līdzīgas preces" rekomendācijas

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā iespējot "pirkt līdzīgas preces" preču ieteikumus programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

"Pirkt līdzīgas preces" ieteikumu līdzeklis Dynamics 365 Commerce izmanto mākslīgā intelekta un mašīnu mācīšanās spēku (AI-ML), lai sniegtu rekomendācijas par vizuāli līdzīgiem produktiem klientiem. Veidojot "pirkt līdzīgas preces" ieteikumus pieejamus visiem mazumtirdzniecības kanāliem Commerce, mazumtirgotāji var palielināt klientu apmierinātību, palīdzot klientiem viegli atrast to, ko viņi vēlas.

"Pirkt līdzīgas preces" rekomendācijas izmanto sēklu preču variantu preču attēlus, lai atrastu un ieteiktu vizuāli līdzīgas preces mazumtirdzniecības preču katalogā. 

"Pirkt līdzīgas preces" ieteikumi ir pieejami gan pārdošanas punktā (POS), gan e-komercijas notikumos.

### <a name="example-scenarios"></a>Piemēra situācijas

- Klients aplūko melnu, svītrainu džemperi un saņem rekomendāciju līdzīgam džemperim sarkanā krāsā. Klients atlasa ieteicamo preci, nevis sākotnēji skatīto preci, un pēc tam saņem ieteikumus par līdzīgiem produktiem sarkanā krāsā. 
- Klients izmanto "pirkt līdzīgas preces" ieteikumus, lai atklātu pieskaņotus auskarus gredzenam, ko klients vēlas iegādāties.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Iespējot "pirkt līdzīgas preces" ieteikumus Commerce Headquarters

Preču ieteikumi tiek atbalstīti tikai tiem Commerce lietotājiem, kuri ir migrējuši savu krātuvi uz Azure Data Lake Gen2.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms mazumtirgotāji var sākt rādīt "pirkt līdzīgas preces" ieteikumus klientiem, ir divi priekšnosacījumu soļi:

- [Iespējot preču ieteikumus](enable-product-recommendations.md) programmā Commerce Headquarters.
- Apstipriniet, ka multivides serveris atbalsta HTTPS izsaukumus.

Lai ieteikumu programma varētu piekļūt preces attēliem, mazumtirgotājiem ir jāģenerē preču URL. Lai izveidotu preču URL programmā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Preču attēli**.
1. Darbību rūtī atlasiet **Definēt multivides veidni**.
1. Rekvizītu rūtī **Definēt multivides veidni** sadaļā **Multivides URL**, atlasiet **Izveidot URL**.

> [!NOTE]
> Kad iespējojat "pirkt līdzīgas preces" ieteikumu funkciju, tiek sākts preču rekomendāciju saraksta ģenerēšanas process. Var tikt pieprasīta līdz vienai dienai, pirms šie saraksti ir pieejami un redzami tiešsaistē un POS termināļos.

Lai iespējotu "pirkt līdzīgas preces" ieteikumus programmā Commerce Headquarters, veiciet šīs darbības.

1. Dodieties uz **Līdzekļu pārvaldība**.
1. Pieejamo funkciju sarakstā meklējiet un atlasiet **pirkt līdzīgas preces**.
1. Labajā rūtī atlasiet **Iespējot**, lai ieslēgtu pakalpojumu.

Sekojošajā attēlā ir parādīts līdzeklis **pirkt līdzīgas preces** lapā **Līdzekļu pārvaldība** programmā Commerce Headquarters.

![Pirkt līdzīgas preces līdzeklis lapā Līdzekļu pārvaldība programmā Commerce Headquarters](./media/enableshopsimilarlooks.png)

Pēc tam, kad iepriekš norādītie uzdevumi ir pabeigti, POS termināļi tiek automātiski uzlaboti ar kontekstuālu **pirkt līdzīgas preces** paneli. Atlasot **Skatīt vairāk**, POS termināļa lietotājus var aizvest uz "pirkt līdzīgas preces" lapu, ko var filtrēt tālāk.

> [!NOTE]
> Izslēdzot "pirkt līdzīgas preces" ieteikumu funkciju, netiek ietekmēti nekādi citi preces ieteikumi. Lai iegūtu vairāk informācijas par preču ieteikumiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Pievienot pogu Pirkt līdzīgas preces preču detalizētas informācijas lapām, izmantojot Commerce Site Builder

Pēc tam, kad iespējojat "pirkt līdzīgas preces" ieteikumu līdzekli programmā Commerce Headquarters, opcija Commerce Site Builder ļauj mazumtirgotājiem pievienot pogu **pirkt līdzīgas preces** pirkšanas kastē jebkuras preču informācijas lapā (PDP). Klients, kurš atlasa šo pogu, tiek nogādāts uz īpašu "pirkt līdzīgas preces" lapu, kas atgriež vizuāli līdzīgas preces. Tur klients var izmantot atlasītāju, lai turpinātu filtrēt preces.

Lai pievienotu pogu **Pirkt līdzīgas preces** PDP, izmantojot Commerce Site Builder, sekojiet šiem soļiem.

1. Atveriet esošu vietnes noformētāja lapu, kas satur pirkšanas kastes moduli.
1. Navigācijas rūtī kreisajā pusē atlasiet pirkšanas kastes moduli.
1. Labajā navigācijas rūtī atlasiet izvēles rūtiņu **Iespējot Pirkt līdzīgas preces saiti**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to. Kad lapa ir publicēta, PDP ietvers **Pirkt līdzīgas preces** pogu.

Sekojošajā attēlā ir parādīta izvēles rūtiņa **Iespējot Pirkt līdzīgas preces saiti** un **Pirkt līdzīgas preces**, piemēram, PDP vietnes veidotājā.

![Iespējot Pirkt līdzīgas preces saiti un Pirkt līdzīgas preces PDP vietnes veidotājā](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)
