---
title: Ieteikumu “pirkt līdzīga apraksta preces” iespējošana
description: Šajā tēmā aprakstīts, kā iespējot "pirkt līdzīga apraksta preces" preču ieteikumus programmā Microsoft Dynamics 365 Commerce.
author: bsokolov
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ce7f249d496a8cf57ad60ac33506fba3cc3dcce40cd89a0cc663ead5263e441a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755858"
---
# <a name="enable-shop-similar-description-recommendations"></a>Ieteikumu “pirkt līdzīgus aprakstus” iespējošana

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā iespējot "pirkt līdzīga apraksta preces" preču ieteikumus programmā Microsoft Dynamics 365 Commerce.

"Pirkt līdzīga apraksta preces" ieteikumu līdzeklis Dynamics 365 Commerce izmanto mākslīgā intelekta un mašīnu mācīšanās spēku (AI-ML), lai sniegtu rekomendācijas par precēm, kuru apraksts ir līdzīgs klienta meklētajām precēm. Veidojot "pirkt līdzīga apraksta preces" ieteikumus pieejamus visiem mazumtirdzniecības kanāliem Commerce, mazumtirgotāji var palielināt klientu apmierinātību, palīdzot klientiem viegli atrast to, ko viņi vēlas.

"Pirkt līdzīga apraksta preces" rekomendācijas izmanto sēklu preču variantu preču nosaukumu un aprakstu, lai atrastu un ieteiktu vizuāli līdzīgas preces mazumtirdzniecības preču katalogā.

"Pirkt līdzīga apraksta preces" ieteikumi ir pieejami gan pārdošanas punktā (POS), gan e-komercijas notikumos.

## <a name="example-scenarios"></a>Piemēra situācijas

Turpmākie piemēru scenāriji parāda rekomendāciju veidus, ko var nodrošināt funkcionalitāte "līdzīga apraksta prece":

- Klients apskata retro stila raga briļļu pāri un saņem ieteikumu komplektu citām brillēm, kam ir līdzīgs dizains, mazumtirgotāja industrijas kontekstā.
- Klients izmanto “pirkt līdzīga apraksta preces” ieteikumus, lai atklātu kafijas aromātus, kas ir līdzīgi aromatizētājam, ko tas iepriekš iegādājies no mazumtirgotāja.

## <a name="set-up-shop-similar-description-recommendations"></a>Ieteikumu “pirkt līdzīga apraksta preces” iestatīšana

Preču ieteikumi tiek atbalstīti tikai tiem Commerce lietotājiem, kuri ir migrējuši savu krātuvi uz 2. paaudzes Azure Data Lake Storage.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms “pirkt līdzīga apraksta preces” ieteikumus var parādīt klientiem, jāizpilda šādi priekšnosacījumi:

- [Iespējot preču ieteikumus](enable-product-recommendations.md) programmā Commerce Headquarters.
- Apstipriniet, ka multivides serveris atbalsta HTTPS izsaukumus.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Līdzekļa “pirkt līdzīga apraksta preces” ieslēgšana

Lai ieslēgtu "pirkt līdzīga apraksta preces" ieteikumus programmā Commerce Headquarters, veiciet šīs darbības.

1. Darbvietā **Līdzekļu pārvaldība** pieejamo līdzekļu sarakstā meklējiet un atlasiet **Pirkt līdzīga apraksta preces**.
1. Labās puses rūtī atlasiet **Iespējot**.

> [!NOTE]
> Ieslēdzot šo līdzekli, sistēma sāk ģenerēt preču ieteikumu sarakstus. Var paiet laiks līdz vienai dienai, pirms šie saraksti kļūst pieejami un redzami tiešsaistē un POS termināļos.
>
> Ja izslēdzat šo līdzekli, netiek ietekmēti citi preču ieteikumu veidi. Lai iegūtu vairāk informācijas par preču ieteikumiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Pogas Pirkt līdzīga apraksta preces pievienošana preču informācijas lapām

Pēc tam, kad ieslēdzat "pirkt līdzīga apraksta preces" ieteikumu līdzekli programmā Commerce Headquarters, varat pievienot pogu **pirkt līdzīga apraksta preces** pirkšanas kastē jebkuras preču informācijas lapā (PDP). Klients, kurš atlasa šo pogu, tiek novirzīts uz īpašu lapu **Pirkt līdzīga apraksta preces**, kas parāda vizuāli līdzīgas preces. Tad klients var izmantot atlasītājus, lai turpinātu filtrēt preces.

Lai pievienotu pogu **Pirkt līdzīga apraksta preces** PDP, izmantojot Commerce Site Builder, izpildiet tālāk norādītās darbības.

1. Atveriet esošu vietnes noformētāja lapu, kas satur pirkšanas kastes moduli.
1. Navigācijas rūtī kreisajā pusē atlasiet pirkšanas kastes moduli.
1. Labās puses rūtī atlasiet izvēles rūtiņu **Iespējot Pirkt līdzīga apraksta preces saiti**.
1. Atlasiet **Saglabāt**.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to. Kad lapa ir publicēta, PDP ietvers **Pirkt līdzīga apraksta preces** pogu.

Sekojošajā attēlā ir parādīta izvēles rūtiņa **Iespējot Pirkt līdzīga apraksta preces saiti** un poga **Pirkt līdzīga apraksta preces** piemēra PDP vietnes veidotājā.

![Pirkt līdzīga apraksta preces saites izvēles rūtiņas un Pirkt līdzīga apraksta preces pogas iespējošana PDP vietnes veidotājā.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Ieteikumu “pirkt līdzīgus modeļus” iespējošana](shop-similar-looks.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]