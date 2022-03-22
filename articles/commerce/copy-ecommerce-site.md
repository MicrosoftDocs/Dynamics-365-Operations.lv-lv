---
title: Kopēt e-komercijas vietni
description: Šajā tēmā ir aprakstīts, kā kopēt esošo e-komercijas vietni starp e-komercijas vidēm vietu Microsoft Dynamics 365 Commerce veidotājā.
author: psimolin
ms.date: 03/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 284a33099fecc5a8e8d5d5d31612abab51735773
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2022
ms.locfileid: "8386913"
---
# <a name="copy-an-e-commerce-site"></a>Kopēt e-komercijas vietni

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir aprakstīts, kā kopēt esošo e-komercijas vietni starp e-komercijas vidēm vietu Microsoft Dynamics 365 Commerce veidotājā.

Dynamics 365 Commerce atbalsta vietņu kopēšanu vai labošanu kā pašapkalpošanās darbību Commerce Site Builder. Vietas var kopēt vienā e-komercijas vidē vai divās e-komercijas vidēs. Lietotājam, kas uzsāk vietnes kopēšanas operāciju, jābūt nomnieka administratoram gan avota, gan mērķa e-komercijas vidēs.

Vietnes kopēšanas operācija kopē visu avota vietnes e-komercijas saturu. Šajā saturā ir lapas, fragmenti, veidnes, vietrāži URL un līdzekļi. Pirms jaunas vietas lietošanas tā jāinicializē, izmantojot pirmo izpildes pieredzes (FRE) procesu. Kanālus var kartēt un pārvaldīt vietņu veidotājā vietnes iestatījumu **kanālos \>**.

Vietas kopēšanas operācijas ilgums galvenokārt ir atkarīgs no līdzekļu skaita avota vietā. Ļoti lielām vietām ieteicams izmantot vides kopēšanas operāciju. (Šī operācija ir pazīstama arī kā datu pārnesamības darbība).

> [!NOTE]
> - Avota vieta būs tikai lasāma vietnes kopēšanas operācijas veikšanai.
> - Tiek kopētas tikai publicētās dokumentu versijas. Ja versijas nav publicētas, tad tiek kopētas tikai jaunākās versijas.
> - Versiju vēsture par saturu nebūs pieejama mērķa vietnē.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Vietas kopēšana e-komercijas vidē

Lai kopētu vietu e-komercijas vidē, sekojiet šiem soļiem.

1. Piesakieties vietas veidotājā videi, kur vēlaties veikt kopēšanas darbību.
1. Atveriet vietņu saraksta skatu, augšējā labajā **stūrī atlasot** Vietas pārslēgšana un pēc tam atlasot **Pārvaldīt vietnes**.
1. Atrodiet vietni, ko vēlaties kopēt vai saglabāt mapē, un atlasiet to, atzīmējot izvēles rūtiņu blakus vietnes nosaukumam.
1. Darbību rūtī atlasiet Kopēt **vietni**.
1. **Dialoglodziņa Kopēt vietni** laukā Jaunas **vietas nosaukums** ievadiet jaunās vietas nosaukumu. E-komercijas vidē jaunajam vietas nosaukumam ir jābūt unikālam. Avota **nomnieka un** Avota **vietas** lauki tiek automātiski iestatīti uz informāciju par pašreizējo nomnieku un atlasīto vietu.
1. Atlasiet **Izveidot kopiju**.

Kad informācija ir pārbaudīta, paziņojums norāda, ka ir izveidots jauns vietnes kopijas darbs. Nomnieka darbu lapas labajā rūtī [varat pārraudzīt **darba** izpildi](#monitor-the-site-copy-operation). Kad kopēšanas operācija ir veiksmīgi pabeigta, jaunā vietne parādās vietņu saraksta skatījumā.

Šajā attēlā parādīts piemērs par vietas **kopēšanas dialoglodziņu** vietas veidotājā.

![Kopējiet vietas dialoglodziņu vietas veidotājā.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Kopēt vietu starp divām e-komercijas vidēm

Lai kopētu vietu starp divām e-komercijas vidēm, sekojiet šiem soļiem.

1. Piesakieties vietas veidotājā mērķa e-komercijas videi.
1. Darbību rūtī atlasiet Kopēt **vietni**.
1. **Dialoglodziņa Kopēt vietni** laukā Jaunas **vietas nosaukums** ievadiet jaunās vietas nosaukumu. E-komercijas vidē jaunajam vietas nosaukumam ir jābūt unikālam.
1. Laukā **Avota nomnieks** atlasiet avota nomnieka nosaukumu.
1. Laukā **Avota** vieta atlasiet avota vietni.
1. Atlasiet **Izveidot kopiju**.

> [!NOTE]
> Nomnieka administratora atļaujas ir nepieciešamas gan avota, gan mērķa e-komercijas vidēm.

Kad informācija ir pārbaudīta, paziņojums norāda, ka ir izveidots jauns vietnes kopijas darbs. Nomnieka darbu lapas labajā rūtī [varat pārraudzīt **darba** izpildi](#monitor-the-site-copy-operation). Kad kopēšanas operācija ir veiksmīgi pabeigta, jaunā vietne parādās vietņu saraksta skatījumā.

## <a name="monitor-the-site-copy-operation"></a>Pārraudzīt vietnes kopēšanas operāciju

Lai pārraudzītu vietnes kopēšanas operācijas norisi, sekojiet šiem soļiem.

1. Piesakieties vietas veidotājā mērķa e-komercijas videi.
1. Kreisās puses rūtī atlasiet nomnieka **darbus**.
1. Nomnieka **darbu lapā** atrodiet un atlasiet sarakstā vietas kopijas darbu. Rūts parādās labajā pusē un parāda atlasītā darba statusu un detaļas.

Jūs varat atcelt darbu, kura statuss ir **Notiek**. Atlasiet sarakstā darbu un pēc tam darbību **rūtī** atlasiet Atcelt.

Jūs varat mēģināt vēlreiz darbu, kura statuss ir Neizdevās **vai** Pabeigts **ar kļūdām**. Atlasiet sarakstā darbu un pēc tam darbību **rūtī atlasiet** Mēģināt vēlreiz.

> [!NOTE]
> Video līdzekļu apstrāde var turpināties pēc tam, kad ir pabeigts vietnes kopēšanas darbs.

Šajā attēlā parādīts nomnieka darbu **lapas** labās rūts piemērs vietas veidotājā.

![Detalizēta informācija par darbu, kas atrodas vietas veidotāja nomnieka darbu lapas labajā rūtī.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Inicializēt jaunu vietni, izmantojot FRE procesu

Pirms jaunas vietas lietošanas tā ir jāinicializē, izmantojot FRE procesu.

Lai inicializētu jaunu vietni, izmantojot FRE procesu, sekojiet šiem soļiem.

1. Piesakieties vietas veidotājā jaunajai vietai.
1. Atveriet vietņu saraksta skatu, augšējā labajā **stūrī atlasot** Vietas pārslēgšana un pēc tam atlasot **Pārvaldīt vietnes**.
1. Atrodiet un atlasiet jaunu vietni, ko vēlaties inicializēt.
1. **Vietnes iestatīšanas** dialoglodziņā atlasiet **domēnu** laukā Atlasīt domēnu. Visi domēni, kas inicializēšanas laikā tika saistīti ar e-komercijas vidi, ir pieejami atlasei.
1. Laukā **Atlasīt noklusējuma kanāla** lauku atlasiet saistīto tiešsaistes veikala kanālu. Atlasītajā kanālā tiks nodrošināts preču klāsts un cita informācija, kas tiek glabāta programmā Commerce Headquarters.
1. Laukā **Atlasīt noklusējuma valodu** atlasiet noklusējuma autorēšanas valodu. Visas valodas, kas tika konfigurētas atlasītajam tiešsaistes veikala kanālam, ir pieejamas atlasei.
1. Laukā **Ceļš** vērtība sastāv no pamata domēna un neobligāta URL ceļa, ko varat ievadīt. Varat atstāt URL ceļu tukšu, ja kanāls tiks apkalpots no domēna saknes, vai ja vēlaties ievadīt šo informāciju vēlāk kanāla konfigurācijas skatījumā vietu veidotājā. Vietas ceļam e-komercijas vidē ir jābūt unikālam.
1. Atlasiet **Labi**. Vieta tiek inicializēta ar jūsu sniegto informāciju un jūs neesat šeit piederīgs vietas pārvaldības skatam.

Šajā attēlā parādīts piemērs par vietas **iestatīšanas** dialoglodziņu vietas veidotājā.

![Iestatiet savu vietnes dialoglodziņu vietu veidotājā.](media/site-copy_3.png)

## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Failu robots.txt pārvaldība](manage-robots-txt-files.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[B2C nomnieka iestatīšana programmā Commerce](set-up-b2c-tenant.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-b2c-tenants.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)
