---
title: Ģenerēt variantus tehniskām precēm
description: Šajā rakstā ir aprakstīts, kā ģenerēt variantus tehnikas precēm
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 08feb66dedfa79f5a21a7723a22f3bef883431e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870758"
---
# <a name="generate-variants-for-engineering-products"></a>Ģenerēt variantus tehniskām precēm

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā ģenerēt variantus tehnikas precēm.

## <a name="turn-variant-generation-for-engineering-products-on-or-off"></a>Variantu ģenerēšanas izslēgšana inženierzinātnes precēm

Šajā rakstā aprakstītajai funkcionalitātei ir nepieciešams, lai *jūsu* *sistēmai ieslēgtu* gan inženierzinātnes izmaiņu pārvaldību, gan variantu ģenerēšanu inženierzinātnes preču līdzekļiem. Papildinformāciju par to, kā ieslēgt vai izslēgt šos līdzekļus, skatiet inženierzinātnes [izmaiņu pārvaldības pārskatā](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Ģenerēt vienu vai vairākus jaunus tehnikas preces variantus

Varat izveidot vienu vai vairākus jaunus preces variantus, nekopējot informāciju no esošās preces. Tas ir noderīgi, ja jāizveido vairāki preces varianti vienlaicīgi.

Šajā procedūrā sniegts piemērs par to, kā izveidot vairākus variantus, kas ietver krāsu dimensiju.

1. Atveriet lapu **Izlaistās preces** (piemēram, dodieties uz sadaļu **Tehnisko pārmaiņu pārvaldība \>— Kopējās \> Izlaistās preces**).
1. Darbību rūts atvēriet cilni **Produkts** un no grupas **Jauns** atlasiet **Tehniskais produkts**.
1. Atveras dialogs **Jauna prece**. Atlasiet atbilstošo **Tehnisko kategoriju**.
1. Ja atlasītā tehniskā kategorija ietver variantu dimensijas, tad tagad varat iestatīt to vērtības. Piemēram, ja kategorijai ir dimensija **Krāsa**, varat to iestatīt uz *Zils*.
1. Pēc nepieciešamības izveidojiet citus iestatījumus. Atlasiet **Labi**, lai izveidotu preci.
1. Tiek izveidota prece un V-1 variants, un tagad tiek atvērta jauna prece.
1. Pēc nepieciešamības pievienojiet materiālu komplektu (MK) un maršrutu šim variantam.
1. Darbību rūtī atvēriet cilni **Prece** un no grupas **Preces šablons** atlasiet **Preces dimensijas**.
1. Atveras lapa **Preces dimensijas**. Šī lapa ietver cilni katrai pieejamai dimensijai. Katrā cilnē pievienojiet rindu katrai vērtībai, kuru atbalstīsit katrai atbilstošajai dimensijai. (Šajā piemērā varat pievienot rindas cilnē **Krāsa** variantiem *Balts*, *Dzeltens* un *Zaļš*).
1. Aizveriet lapu un pēc tam atlasiet **Izlaisto preču varianti**. Tiek parādīts pirmais izveidotais variants (zils V-1).
1. Darbību rūts cilnē **Preces variants** atlasiet **Variantu ierosinājumi**.
1. Dialoglodziņā **Variantu ierosinājumi** izpildiet vienu no šīm darbībām:

    - Dialoglodziņa augšpusē ir sadaļa katrai pieejamajai dimensijai. Katrai dimensijai atlasiet aizzīmes lodziņu katrai vērtībai, kurai vēlaties ģenerēt varianta ierosinājumu, un pēc tam rīkjoslā atlasiet **Ierosināt**. Atbilstošie ierosinājumi tiek pievienoti sadaļā **Ierosinātie varianti**.
    - Rīkjoslā atlasiet **Ierosināt visu**, lai ģenerētu variantu ierosinājumus visām pieejamajām dimensiju vērtību kombinācijām. Ierosinājumi tiek pievienoti sadaļā **Ierosinātie varianti**.

1. Sadaļā **Ierosinātie varianti** atlasiet aizzīmes lodziņu katram variantam, kuru vēlaties izveidot. Pēc tam atlasiet **Izveidot**, lai ģenerētu un izlaistu atlasītos variantus uz inženiertehnisko uzņēmumu. Spēkā ir tālāk minētie nosacījumi:

    - Nevienam no izveidotiem variantiem nebūs MK vai maršruts.
    - Šo variantu atribūti pēc noklusējuma tiks kopēti no tehniskās kategorijas un netiks kopēti no iepriekšējā varianta.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Ģenerēt variantu kā cita preces varianta kopiju

Varat izveidot preces variantu, pamatojoties uz citu preces variantu. Materiālu komplekts (MK) un maršruts no avota preces varianta tiek kopēti uz jauno variantu. Tas var būt noderīgi diskrētiem ražošanas produktiem, kur var būt noderīgi izveidot MK, pamatojoties uz sākuma MK, un sekot līdzi izmaiņām no iepriekšējā varianta. Lai saglabātu izsekojamību, sistēma reģistrē, kurš variants tika kopēts, lai izveidotu jaunu kopiju.

Šajā procedūrā sniegts piemērs par to, kā izveidot jaunu variantu, kas ietver krāsu dimensiju, izveidojot esoša varianta kopiju

1. Atveriet lapu **Izlaistās preces** (piemēram, dodieties uz sadaļu **Tehnisko pārmaiņu pārvaldība \>— Kopējās \> Izlaistās preces**).
1. Darbību rūts atvēriet cilni **Produkts** un no grupas **Jauns** atlasiet **Tehniskais produkts**.
1. Atveras dialogs **Jauna prece**. Atlasiet atbilstošo **Tehnisko kategoriju**.
1. Ja atlasītā tehniskā kategorija ietver variantu dimensijas, tad tagad varat iestatīt to vērtības. Piemēram, ja kategorijai ir dimensija **Krāsa**, varat to iestatīt uz *Zils*.)
1. Pēc nepieciešamības izveidojiet citus iestatījumus. Atlasiet **Labi**, lai izveidotu preci.
1. Tiek izveidota prece un V-1 variants, un tagad tiek atvērta jauna prece.
1. Pēc nepieciešamības pievienojiet MK un maršrutu šim variantam.
1. Pēc vajadzības pievienojiet preces variantam atribūtus.
1. Pievienojiet preces variantu zils V-1 tehnisko izmaiņu pasūtījumam.
1. Iestatiet **Ietekmi** uz *Jaunu variantu*.
1. Atlasiet jauno krāsas vērtību (piemēram, *Balts*). Ņemiet vērā, ka tiks piemēroti šādi nosacījumi: 
    - Jaunajam variantam ir MK un maršruts, kas ir nokopēts no iepriekšējā varianta.
    - Jaunajam variantam ir atribūti, kas kopēti no iepriekšējā varianta.
1. Apstipriniet izmaiņu pasūtījumu.
1. Apstrādājiet izmaiņu pasūtījumu. Kad pasūtījums ir apstrādāts, jaunais V-1 variants tiks izveidots un nodots tehniskajam uzņēmumam.
