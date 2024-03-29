---
title: Jaunas preces izveide programmā Commerce
description: Šajā rakstā ir aprakstīts, kā izveidot jaunu preci Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 654ba19b0bc96ab40c8c27106fd819faa85a4ce8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270186"
---
# <a name="create-a-new-product-in-commerce"></a>Jaunas preces izveide programmā Commerce


[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot jaunu preci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Preces galvenokārt nosaka pēc preces numura, nosaukuma un apraksta. Lai aprakstītu preci vai pakalpojumu, tomēr ir nepieciešami arī citi dati.

## <a name="create-a-new-product"></a>Jaunas preces izveide

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Preces pēc kategorijas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Nolaižamajā saraksā **Preces veids** atlasiet vai nu **Krājums**, vai **Pakalpojums**.
1. Nolaižamajā sarakstā **Preces apakštips** atlasiet vai nu **Prece** (ja precei nebūs variantu), vai **Preces šablons** (ja precei būs varianti).
1. Ja lodziņš **Preces numurs** jau nav iepriekš aizpildīts, ievadiet tajā preces numuru.
1. Lodziņā **Preces nosaukums** ievadiet preces nosaukumu.
1. Lodziņā **Saīsinātais nosaukums** ievadiet saīsināto nosaukumu.
1. Nolaižamajā sarakstā **Mazumtirdzniecības kategorija** atlasiet atbilstošu kategoriju.
1. Ja prece ir komplekts, izvēlieties **Jā** vaicājumam **Preču komplekts**.
1. Ja preces apakštips ir preces šablons, iestatiet **Preču dimensiju grupa**, lai iekļautu atbalstītos variantus. Iespējamie varianti ir **Krāsa**, **Izmērs**, **Stils** un **Konfigurācija**. Ja nepieciešams, jāizveido papildu preču dimensiju grupas.
1. Nolaižamajā sarakstā **Konfigurācijas tehnoloģija** atlasiet atbilstošu opciju.
1. Atlasiet **Labi**.

Tālāk redzamajā attēlā parādīts pievienojamās preces piemērs.

![Preces izveide.](media/create-new-product.png)

Kad prece ir pievienota, tai var iestatīt papildu datus, piemēram, **Preces apraksts**, **Variantu grupas**, **Dimensiju grupas**, **Preces īpašības** un **Saistītās preces**.

Tālāk redzamajā attēlā ir parādīta preces papildu informācija.

![Detalizēta informācija par preci.](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Izveidot preces variantus

Ja preces apakštips ir **Preces šablons**, būs jāizveido noteikti varianti. 

Lai izveidotu preču variantus, veiciet tālāk aprakstītās darbības.

1. Darbību rūtī atlasiet **Preču varianti**.
1. Ja darbības rūtī ir atlasītas variantu grupas, atlasiet **Variantu ieteikumi*.
1. Atlasiet variantus, kurus vēlaties atbalstīt šai precei.
1. Atlasiet **Izveidot**.

## <a name="release-a-product"></a>Preces izlaišana

Lai pārdotu preci, tā vispirms jānodod juridiskai personai.

1. Preču lapā atlasiet **Preču izlaišana**.

    ![Izlaist preci.](media/create-new-product-3.png)

1. Atlasiet izlaižamo preci un pēc tam atlasiet **Tālāk**.

    ![Izlaižamās preces izvēle.](media/create-new-product-4.png)

1. Atlasiet izlaižamo preču variantu komplektu un pēc tam atlasiet **Tālāk**.

    ![Izvēlēties izlaižamos variantus.](media/create-new-product-5.png)

1. Atlasiet juridisko personu un pēc tam atlasiet **Tālāk**.

    ![Izvēlieties juridisko personu.](media/create-new-product-6.png)

1. Atl. **Pabeigt**.

    ![Preces izlaišanas pabeigšana.](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Izlaistās preces konfigurēšana

Pēc preces izlaišanas tai būs nepieciešama turpmāka konfigurācija, kas ietver cenas pievienošanu precei.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Izlaistās preces pēc kategorijas**.
1. Atlasiet preces kategorijas mezglu precei, kas tika izlaista, un pēc tam preču sarakstā atlasiet preci.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Sadaļā **Pirkšana** konfigurējiet visus nepieciešamos rekvizītus, tostarp **Vienība**, **Cena** un **Daudzums**.
1. Darbības rūtī atlasiet **Pārbaudīt**, lai nodrošinātu, ka trūkstošajiem laukiem nav ziņotas kļūdas.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā ir parādīts izlaistās preces konfigurācijas piemērs.

![Izlaistās preces konfigurēšana.](media/create-new-product-8.png)

## <a name="additional-resources"></a>Papildu resursi

[Izveidot juridiskās personas](channels-legal-entities.md)

[Variantu grupas izveide](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
