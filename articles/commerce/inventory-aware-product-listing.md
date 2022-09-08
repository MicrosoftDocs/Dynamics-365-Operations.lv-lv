---
title: Krājuma informācija par preču sarakstu
description: Šajā rakstā ir aprakstīts, kā organizācijas var konfigurēt preču sarakstu lapas savā Microsoft Dynamics 365 Commerce e-komercijas vietnē, lai tās būtu informēti par krājumiem.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: e33a4dd8650ee2e371c51c5a19e955f2d2bdade2
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405519"
---
# <a name="inventory-aware-product-listing"></a>Krājuma informācija par preču sarakstu

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā rakstā ir aprakstīts, kā organizācijas var konfigurēt preču sarakstu lapas savā Microsoft Dynamics 365 Commerce e-komercijas vietnē, lai tās būtu informēti par krājumiem. Preču saraksta lapas ietver kategoriju papildu lapas un meklēšanas rezultātu lapas.

Iepirktājos parasti paredzams, ka e-komercijas vietnē preču atklājumi tiks atzīti par krājumiem, tādējādi tie var izlemt, ko darīt, ja prece nav krājumā. Commerce [moduļu bibliotēkas](starter-kit-overview.md) kategoriju un meklēšanas rezultātu moduļus var konfigurēt, lai ietvertu krājumu datus. Šādā veidā viņi var sniegt sekojošo pieredzi:

- Rādīt krājumu līmeņa etiķetes līdzās precēm.
- Paslēpt preču sarakstā preces, kas atrodas ārpus noliktavas.
- Pārvietojiet preces, kas atrodas ārpus noliktavas, uz preču saraksta lapu apakšdaļu.
- Atbalstīt krājumu preču filtrēšanu.

Lai iespējotu šo pieredzi, vispirms programmā **Commerce headquarters iespējojiet uzlaboto e-commerce** preču noteikšanu, lai būtu krājumos izprotams līdzeklis.

> [!NOTE]
> Commerce versijā 10.0.29 vai jaunākā versijā uzlabotās e-commerce **preces noteikšana, lai būtu krājumu informācijas funkcija,** kas ir aktivizēta pēc noklusējuma, ir iespējota.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Iestatīt preces īpašību krājumu pieejamībai

Krājuma izprotamā preču saraksts izmanto preču īpašību struktūru. Lai tvertu krājumu pieejamības datus, ir jāizveido atvēlētais preces atribūts.

Lai iestatītu preces īpašību krājumu pieejamībai programmā Commerce Headquarters, sekojiet šiem soļiem.

1. Pārejiet uz **sadaļu \> Mazumtirdzniecība un Commerce Retail un Commerce IT \> preces un krājumi \>.**
1. Dialoglodziņā Aizpildīt **preces īpašības** ar krājuma līmeņa dialoglodziņu, laukā Preces īpašības un tipa nosaukums ievadiet pielāgotu nosaukumu atvēlētajai preces īpašībai, kas tiks izveidota, **lai** tvertu krājumu datus.
1. Laukā Krājumu **pieejamība, pamatojoties uz** lauku, atlasiet daudzuma tipu, uz kura krājumu līmeņa aprēķinam jābūt balstītam: Pieejamais **fiziskais vai** Kopējais **pieejamais**.
1. Iestatiet opciju **Pakešapstrāde** uz **Jā**.
1. Atlasiet **Labi**.

> [!NOTE]
> Lai veiktu konsekventu krājumu līmeņa aprēķinu jūsu e-komercijas vietnes **lapās** **, nodrošiniet,** **lai** jums būtu viens un tas pats daudzuma tips gan krājumu pieejamība, gan laukā Aizpildīt preču īpašības ar krājumu līmeņa darbu, gan krājumu līmeni, pamatojoties uz iestatījumu Commerce Site Builder.

Kad atvēlētā preces īpašība ir izveidota, nākamais solis ir konfigurēt atribūtu tiešsaistes kanālam.

Lai konfigurētu atribūtu tiešsaistes kanālam programmā Commerce Headquarters, sekojiet šiem soļiem.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preču īpašības**.
1. Atlasiet tiešsaistes kanālu, lai iespējotu krājumam zināma preču saraksta pieredzi.
1. Atlasiet un atveriet saistīto atribūtu grupu un pēc tam pievienojiet tai jaunu preces īpašību.
1. Dodieties uz **grafiku Mazumtirdzniecība un Commerce Retail un Commerce IT \> sadale \> un palaidiet** 1150 **(** kataloga **)** darbu. Mēs iesakām jums plānot šo darbu kā pakešuzdevumu, **kas darbojas tik bieži kā krājumu līmeņa darbs aizpildīt preces** īpašības.

> [!NOTE]
> Commerce versijā 10.0.26 un agrāk pēc **krājumu pieejamības preces īpašību pievienošanas atribūtu grupai ir jāatlasa arī iestatījuma atribūtu metadati** un **pēc** tam pēc tam jāslēdz atribūts Rādīt kanālā, **Izgūstams**, var tikt precizēts **un** **var** būt vaicājumā pieejamas opcijas jaunajam preces atribūtam.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Konfigurēt displeju precēm, kas atrodas ārpus rezervēm preču saraksta lapās

Kad visi iepriekšējie konfigurācijas soļi ir pabeigti, kategorijas un meklēšanas rezultātu lapu uzlabotājiem būs uz krājumiem balstīta filtra opcija. Krājuma līmeņa etiķete tiks parādīta katram preces elementam, kas parādās lapā.

Kategorijas un meklēšanas rezultātu lapā ir parādītas preces galvenajā līmenī, nevis preces varianta līmenī. Krājumu līmenis, kas ir parādīts līdzās katrai precei, ir apkopots krājumu līmenis, ko nosaka visu preču variantu krājumu līmenis. Varianta krājumu līmenis tiek aprēķināts, balstoties uz šī varianta rīcībā ajiem krājumiem programmas Commerce Headquarters tiešsaistes kanāla noklusējuma noliktavā. Šablona preces krājumu līmenim ir divas iespējamās vērtības, kas norāda noliktavā esošos un noliktavā esošos krājumus. Ja visi tās varianti ir krājumos, šablona prece netiek uzskatīta par krājumiem. Pretējā gadījumā prece tiek uzskatīta krājumos. Vērtības iezīme tiek izgūta no krājuma [līmeņa definīcijas](inventory-buffers-levels.md). Ja krājuma līmenis nav noteikts, noklusējuma etiķetes (angļu valodā) ir pieejamas **un** **ir ārpus noliktavas**.

Varat konfigurēt krājumu iestatījumus **preču** saraksta lapu iestatījumam Commerce Site Builder, lai kontrolētu to, kā kategoriju un meklēšanas rezultātu lapā tiks rādītas preces, kas atrodas ārpus noliktavas. Papildinformāciju skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
