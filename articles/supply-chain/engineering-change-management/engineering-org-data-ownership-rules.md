---
title: Inženiertehniskie uzņēmumi un datu īpašumtiesību noteikumi
description: Šajā tēmā skaidrots, kā var izmantot vienu vai vairākus inženiertehniskus uzņēmumus, lai nodrošinātu, ka produktu pamatdati ir centralizēti izveidoti un uzturēti. Inženiertehniskais uzņēmums ir uzņēmums, kam pieder tehniskie produkti un ar inženieriju saistītie dati.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5cab02600e13a1a539b5ae0cd3ff66960430e826
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433226"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Inženiertehniskie uzņēmumi un datu īpašumtiesību noteikumi

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Inženiertehniskie uzņēmumi un operacionālie uzņēmumi

Lai nodrošinātu produktu pamatdatu centrālu izveidi un uzturēšanu, var izmantot vienu vai vairākus *inženiertehniskos uzņēmumus*. Inženiertehniskajam uzņēmumam pieder tehniskie produkti un ar inženieriju saistītie dati. Vienmēr ir izveidots savienojums ar (pamatojoties uz) esošu *juridisku personu*, kas arī ir uzņēmums. Izmantojot šo savienojumu, sistēma izveido centrālo ieejas punktu visiem ar inženieriju sastītiem datiem, kas attiecas uz tehniskiem produktiem inženiertehniskajā uzņēmumā. Šajā centrālajā ieejas punktā tiek veidoti tehniskie produkti, un tiek uzturēti tehniskie dati. No tā tehniskie produkti un ar inženieriju saistītie dati tiks nodoti *operacionālie uzņēmumiem*, kas ir citas juridiskas personas. (Plašāku informāciju par laidiena pārvaldību skatiet sadaļā [Izlaist produktu struktūras](release-product-structure.md).) Šie operacionālie uzņēmumi izmantos tehnisko informāciju, kā to projektējis inženiertehniskais uzņēmums. Visus loģistikas datus lokāli uztur katrs inženiertehniskais uzņēmums un operacionāls uzņēmums.

Lai izveidotu inženiertehnisko uzņēmumu, dodieties uz **Tehnisko izrmaiņu pārvaldība \> Iestatījumi \> Inženiertehniskās organizācijas**. Atlasiet **Jauns**, ievadiet inženiertehniskā uzņēmuma nosaukumu un atlasiet esošo uzņēmumu (juridiska persona), kas ir tā pamatā.

Ja integrējat ar ārējo produktu dzīves cikla pārvaldības (product lifecycle management - PLM) sistēmām, jums jāizveido biznesa vienība (uzņēmuma veids), kas kļūs par ārēju uzņēmumu.

## <a name="engineering-product-categories-and-engineering-companies"></a>Tehnisko produktu kategorijas un inženiertehniskie uzņēmumi

*Tehnisko produktu kategorijas* palīdz nodrošināt, ka tehniskie produkti tiek veidoti atbilstoši jūsu uzņēmuma biznesa noteikumiem un darbojas pēc nepieciešamības. Papildinformāciju par produktu kategorijām skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).

Katra tehnisko produktu kategorija pieder noteiktam inženiertehniskām uzņēmumam un var veidot tikai produktus, kas pieder šim uzņēmumam. Līdzīgi arī tiesības uzturēt tehniskos produktus pieder uzņēmumam, kas ir saistīts ar ša produkta tehnisko produktu kategoriju.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Dati, kas pieder inženiertehniskajam uzņēmumam

Tā kā inženiertehniskajam uzņēmumam pieder tehniskie dati, tas kontrolē šādus procesus:

- **Tehnisko produktu izveide:** Katrs inženiertehniskais uzņēmums var radīt tikai jaunus tehniskos produktus, kas ir balstīti uz tehnisko produktu kategoriju, kas tam pieder. Dažos gadījumos operacionālie uzņēmumi uztur savus vietējos datus, kas ir saistīti ar šiem produktiem.
- **Tehnisko versiju izveide:** kad uzņēmums izveido jaunu tehnisku produktu, sistēma automātiski izveido tam sākotnējo tehnisko versiju. Tikai inženiertehniskais uzņēmums-īpašnieks varēs izveidot jaunas šī produkta versijas.
- **Tehnisko atribūtu izveide un uzturēšana:** kad uzņēmums izveido jaunu tehnisku produktu, sistēma automātiski pievieno tam tehnisko atribūtu. Tikai inženiertehniskais uzņēmums-īpašnieks varēs izveidot un uzturēt šo atribūtu vērtības. Plašāku informāciju par tehniskajiem atribūtiem skatiet sadaļā [Tehniskie atribūti un tehnisko atribūtu meklēšana](engineering-attributes-and-search.md).
- **Izveidot un uzturēt materiālu komplektus (MK), kas ir saistīti ar tehniskajām versijām:** inženiertehniskais uzņēmums-īpašnieks var tieši saistīt MK ar tehniskā produkta versiju. Kad šie MK tiek nodoti citām juridiskajām personām, MK tehnisko datu izmaiņas tiek ierobežotas šādos veidos:

    - Operacionāls uzņēmums nevar noņemt izlaistās MK rindas.
    - Tehniskie lauki MK rindās ir lasāmi tikai operacionālām uzņēmumam. Visi pārējie lauki ir loģistikas ieviešanas lauki, un tos var rediģēt operacionāls uzņēmums.
    - Operacionāls uzņēmums var pievienot MK rindas vienam un tam pašam MK. Šādā veidā tas var pievienot vietējos papildinājumus, piemēram, iepakojuma materiālus vai eļļošanas šķidrumus.
    - Darbības uzņēmums var pievienot pilnīgi jaunu, lokālu MK. Šīs izmaiņas var būt nepieciešamas gadījumos, kad, piemēram, izlaižot materiālu, nav norādīts MK. Operacionālām uzņēmumam pieder un tas uztur šos vietējos MK. Plašāku informāciju par izlaišanas pārvaldību skatiet šeit: [Produktu struktūru izlaide](release-product-structure.md).
    - Visi lokālie MK un MK rindas tiek saglabātas, kad inženiertehniskais uzņēmums atjaunina MK.

- **Izveidot un uzturēt maršrutus, kas ir saistīti ar tehniskajām versijām:** inženiertehniskais uzņēmums-īpašnieks var tieši saistīt maršrutu ar katru tehnisko versiju. Kad šie maršruti tiek nodoti citām juridiskajām personām, maršrutu datu izmaiņas tiek ierobežotas šādos veidos:

    - Citas juridiskās personas nevar noņemt tehniskos datus maršrutos.
    - Citas juridiskās personas var pievienot operācijas maršrutam. Šādā veidā viņi var pievienot vietējās maršrutu darbības.
    - Operacionālie uzņēmumi var pievienot pilnīgi jaunus, vietējos maršrutus. Šīs izmaiņas var būt nepieciešamas tad, kad, piemēram, izlaiduma laikā nav iekļauti maršruti. Operatīvajiem uzņēmumiem pieder un tie uztur šos vietējos maršrutus. Plašāku informāciju par izlaišanas pārvaldību skatiet šeit: [Produktu struktūru izlaide](release-product-structure.md).
    - Visas lokāli veiktās izmaiņas tiek saglabātas, kad no inženiertehniskā uzņēmuma atjauninājumi tiek atkal izlaisti maršrutos.

- **Tehnisko dokumentu izveide un uzturēšana:** inženiertehniskais uzņēmums var pievienot tehniskos dokumentus katrai tehniskai versijai.

    - Kad šie dokumenti tiek nodoti citām juridiskajām personām, operacionālais uzņēmums aizsargā dokumentus no to izņemšanas.
    - Citas juridiskas personas var pievienot pilnīgi jaunus, lokālus dokumentus. Operacionālām uzņēmumam pieder un tas uztur šos vietējos dukumentus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]