---
title: E-komercijas digitālās dāvanu kartes
description: Šajā tēmā aprakstīts, kā digitālās dāvanu kartes darbojas Microsoft Dynamics 365 Commerce e-komercijas ieviešanā. Tajā sniegts arī apskats par svarīgiem konfigurācijas soļiem.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e0cbab05cfd9dcde8ec5caf802d13cd10bc9123716b46307616b0e3e66f0f061
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727561"
---
# <a name="e-commerce-digital-gift-cards"></a>E-komercijas digitālās dāvanu kartes

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā aprakstīts, kā digitālās dāvanu kartes darbojas Microsoft Dynamics 365 Commerce e-komercijas ieviešanā. Tajā sniegts arī apskats par svarīgiem konfigurācijas soļiem.

Programmā Dynamics 365 Commerce digitālo dāvanu karšu pirkšana notiek tāpat kā citu produktu pirkšanas sistēmā. Nav nepieciešams konfigurēt papildu moduļus. Ja grozam tiek pievienotas vairākas dāvanu kartes, dāvanu karšu krājumi netiek apkopoti vienā pārdošanas rindā. Šī darbība ir nepieciešama, jo katra pārdošanas rinda ir iekļauta rēķinā, izmantojot atsevišķu dāvanu kartes numuru.

Digitālo dāvanu karšu pirkšana ir atbalstīta Dynamics 365 Commerce 10.0.16. laidienā un jaunākās versijās.

Šajā ilustrācijā parādīts preču informācijas lapas (PDP) piemērs digitālai dāvanu kartei Fabrikam e-komercijas vietnē.

![Digitāla dāvanu kartes PDP piemērs Fabrikam e-komercijas vietnē.](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Ieslēgt digitālās dāvanu kartes funkciju programmā Commerce Headquarters

Lai digitālo dāvanu karšu pirkšanas plūsma darbotos programmā Dynamics 365 Commerce, sadaļā Commerce Headquarters ir jābūt ieslēgtai līdzeklim **Dāvanu kartes pirkšana e-komercijas līdzeklī**. Sekojošajā attēlā atradīsiet līdzekli darbvietā **Līdzekļu pārvaldība** sadaļā Commerce headquarters.

![Līdzekļu pārvaldības darbvieta programmā Commerce Headquarters.](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Konfigurēt digitālo dāvanu karti programmā Commerce Headquarters

Digitālās dāvanu kartes precēm jābūt konfigurētām programmā Commerce Headquarters. Process līdzinās citu preču procesam. Tomēr tālāk minētās svarīgās darbības ir raksturīgas dāvanu karšu pirkuma konfigurācijai. Plašāku informāciju par preču izveidošanu un konfigurēšanu skatiet šeit: [Jaunas preces izveide programmā Commerce](create-new-product-commerce.md).

- Konfigurējot digitālo dāvanu karšu preces dialoglodziņā **Jauna prece**, iestatiet **Preces tips** lauku uz **Pakalpojums**. (Lai atvērtu dialoglodziņu, dodieties uz **Mazumtirdzniecības un komercija \> Preces un kategorijas \> Preces pēc kategorijas**  un atlasiet **Jauns**.) Preces ar **Pakalpojuma** tipu nav atzīmētas pieejamiem krājumiem, pirms tiek veikts pasūtījums. Papildinformāciju skatiet sadaļā [Jaunas preces izveide](create-new-product-commerce.md#create-a-new-product).
- Lapas **Komercijas parametri** cilnē **Grāmatošana** laukam **Dāvanu kartes prece** ir jābūt iestatītam uz **Digitālā dāvanu karte**, kā parādīts ilustrācijā. Ja prece ir ārējā dāvanu karte, plašāku informāciju skatiet sadaļā [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md).

    ![Dāvanu kartes preces lauks programmā Commerce Headquarters.](./media/PostGiftcard.png)

- Ja dāvanu kartei ir jāatbalsta vairākas iepriekš definētas summas (piemēram, $25, $50 un $100), šo iepriekš definēto summu iestatīšanai jāizmanto **Izmēra** dimensija. Katra iepriekš definētā summa būs variants. Papildinformāciju skatiet sadaļā [Preču dimensijas](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json).
- Ja klientiem ir jāprecizē pielāgotā summa dāvanu kartei, vispirms iestatiet variantu, kas ļauj izmantot pielāgotu summu. Pēc tam atveriet preci no lapas **Izlaistās preces pēc kategorijas** un pēc tam kopsavilkuma cilnē **Komercija** iestatiet lauku **Ievadīt cenu** vērtību uz **Jāievada jauna cena**, kā parādīts šajā ilustrācijā. Šis iestatījums nodrošina, ka klienti var ievadīt cenu, pārlūkojot preci PDP.

    ![Lauks Ievadīt cenu pakalpojumā Commerce Headquarters.](./media/KeyInPrice.png)

- Digitālās dāvanu kartes piegādes režīmam ir jābūt iestatītam uz **Elektronisks**. Lapā **Piegādes veidi** (**Mazumtirdzniecība un komercija \> Kanālu iestatīšana \> Piegādes veidi**), atlasiet piegādes veidu **Elektroniski** saraksta rūtī un tad pievienojiet digitālās dāvanu kartes preci režģim kopsavilkuma cilnē **Preces**, kā parādīts sekojošajā ilustrācijā. Plašāku informāciju skatiet [Piegādes veidu iestatīšana](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Digitālās dāvanu kartes preces Commerce Headquarters piegādes veidu lapā.](./media/ElectronicMode.PNG)

- Pārliecinieties, ka ir izveidots tiešsaistes funkcionalitātes profils un saistīts ar jūsu tiešsaistes veikalu programmā Commerce Headquarters. Funkcionalitātes profilā iestatiet opciju **Apkopot preces** uz **Jā**. Šis iestatījums nodrošina, ka tiek apkopotas visas preces, izņemot dāvanu kartes. Papildinformāciju skatiet [Tiešsaistes funkcionalitātes profila izveidošana](online-functionality-profile.md).
- Lai nodrošinātu, ka klienti saņem e-pasta ziņojumu pēc tam, kad ir izrakstīts rēķins par dāvanu karti, izveidojiet jaunu e-pasta paziņojuma veidu **E-pasta paziņojuma profilu** lapā un iestatiet **E-pasta paziņojuma veida** lauku uz **Izsniegt dāvanu karti**. Papildinformāciju skatiet šeit: [E-pasta paziņojuma profilu iestatīšana](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Pievienojiet preču attēlus Commerce vietnes veidotāja multimediju bibliotēkā

Jums jāpievieno preces attēli digitālās dāvanu kartes precēm Commerce vietnes veidotāja multimediju bibliotēkā. Pārliecinieties, vai failu nosaukumi dāvanu karšu attēlu failiem seko jūsu vietnes nosaukumu piešķiršanas nosacījumiem preču attēliem. Plašāku informāciju skatiet sadaļā [Attēlu augšuplāde](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Konfigurēt pielāgotu summu digitālai dāvanu kartei Commerce vietnes veidotājā

Ja digitālā dāvanu karte ir konfigurēta, lai atļautu pielāgotu summu, šai darbībai ir jābūt iespējotai arī [pirkšanas lodziņa modulī](add-buy-box.md), kas tiek izmantots jūsu vietnes PDP. Pirkšanas lodziņa modulis atbalsta moduļa konfigurāciju, lai atļautu pielāgotās summas. Varat arī noteikt minimālos un maksimālos apjomus, kas atļauti pielāgotajām summām.

Lai konfigurētu pielāgotu summu digitālai dāvanu kartei Commerce vietnes veidotājā, sekojiet šiem soļiem.

1. Dodieties uz pirkšanas lodziņa moduli, kas tiek izmantots jūsu vietnes PDP. Šis pirkšanas lodziņa modulis var būt implementēts fragmentā, veidnē vai lapā.
1. Atlasiet **Rediģēt**.
1. Rekvizītu rūtī labajā pusē atzīmējiet izvēles rūtiņu **Atļaut pielāgotu cenu**.
1. Nav obligāti: lai definētu minimālo un maksimālo daudzumu pielāgotajām summām, ievadiet summas zem **Minimālās cenas** un **Maksimālās cenas**.
1. Atlasiet **Beigt rediģēšanu** un pēc tam atlasiet **Publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Groza modulis](add-cart-module.md)

[Jaunas preces izveide programmā Commerce](create-new-product-commerce.md)

[Iestatiet piegādes veidus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Preces dimensijas](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json)

[E-pasta paziņojumu profila iestatīšana](email-notification-profiles.md)

[Izveidot tiešsaistes funkcionalitātes profilu](online-functionality-profile.md)

[Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]