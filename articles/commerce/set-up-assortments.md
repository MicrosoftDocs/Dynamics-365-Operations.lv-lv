---
title: Preču klāstu iestatīšana
description: Šajā rakstā ir aprakstīts, kas ir preču klāsts, un ir paskaidrots, kā iestatīt preču klāstus programmā Dynamics 365 Commerce.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: bbe7749e6c8293ded933611d6f1084b89223302c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790986"
---
# <a name="set-up-assortments"></a>Iestatīt preču klāstus

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kas ir preču klāsts, un ir paskaidrots, kā iestatīt preču klāstus programmā Dynamics 365 Commerce.

Preču klāsts ir saistīto preču grupa, ko piešķirat komercijas kanālam, piemēram, fiziskam vai tiešsaistes veikalam. Preču klāsti tiek izmantoti, lai norādītu preces, kas ir pieejamas katrā veikalā. Preču klāstā var ietvert preču kategorijas. Tāpēc visas preces, kas ir piešķirtas noteiktai kategorijai, ir ietvertas preču klāstā. Preču klāstā var ietvert arī noteiktas preces un noteiktus preču variantus. Iestatot preču klāstu, varat saviem kanāliem vienlaikus piešķirt tūkstošiem produktu jebkādā kombinācijā, kas ir nepieciešama veikalos. Varat iestatīt tik daudz preču klāstu, cik ir nepieciešams. Katru preci var iekļaut vienā vai vairākos preču klāstos, un katru preču klāstu var piešķirt vienam vai vairākiem kanāliem. Piemēram, jūs definējat vienu preču klāstu, kas ietver preču pamata kopu. Visi veikali saņem šo preču klāstu. Pēc tam jūs definējat citu preču klāstu, kas ietver tikai lielu sporta aprīkojumu. Šo preču klāstu saņem tikai lielākie veikali. Tālāk esošajā diagrammā ir redzams, kā preces var piešķirt preču klāstiem un kā šos preču klāstus var piešķirt kanāliem.

![Preču klāsta attiecības](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu iestatīt preču klāstu un to piešķirt komercijas kanālam, vispirms ir jāizpilda tālāk norādītie uzdevumi.

| Uzdevums                              | Apraksts |
|-----------------------------------|-------------|
| Kanāla iestatīšana.          | Kanāli atbilst fiziskam veikalam, tiešsaistes veikalam vai tiešsaistes tirgum. Jums ir jāiestata vismaz viens kanāls un jākonfigurē veikala opcijas. Preču klāsti tiek piešķirti veikaliem, lai norādītu konkrētā veikalā pieejamās preces. |
| Izveidojiet organizācijas hierarhiju. | Kad esat iestatījis organizācijas komercijas kanālus, jums ir jākonfigurē mazumtirdzniecības organizācijas hierarhija, kas atbilst mazumtirdzniecības kanālu organizācijas struktūrai. Organizācijas hierarhiju var izmantot preču klāstiem, papildināšanai vai ziņošanai. Pievienojot kanālu organizācijas hierarhijai, varat piešķirt preču klāstus veikalu grupām. Jūs piešķirat preču klāstu nevis katram veikalam atsevišķi, bet gan augsta līmeņa organizācijas hierarhijas mezglam. Pēc tam ikreiz, kad augsta līmeņa organizācijas hierarhijas mezglam tiek pievienots jauns kanāls, šis kanāls automātiski pārmanto visus preču klāstus, kas ir piešķirti augstākā līmeņa organizācijas hierarhijas mezglam. Preču klāstus var piešķirt tikai kanāliem, kas ir iekļauti organizācijas hierarhijā, kam ir piešķirts nolūks **Commerce preču klāsts**. |
| Definējiet preces.                  | Lai varētu pievienot preces klāstam, tās vispirms ir jāpievieno programmā Commerce. Varat pievienot preces manuāli vai arī varat tās importēt no kreditora. Pēc preču pievienošanas tās ir jāizdod juridiskai personai. Jūsu kanālos var padarīt pieejamas tikai tās preces, kas ir izdotas juridiskai personai. Preces, kas vēl nav izdotas juridiskai personai, var pievienot preču klāstam, un preču klāstu var apstiprināt. Taču preces nevar padarīt pieejamas kanālos, kamēr šīs preces nav izdotas juridiskai personai. |
| Iestatiet kategoriju hierarhiju.      | Izveidojot komercijas preces, varat tās grupēt un kategorizēt, izmantojot kategoriju hierarhijas līdzekli. Varat izveidot vienu galveno hierarhiju, lai grupētu un kategorizētu visas preces, ko izplatāt kanālos. Varat arī izveidot atsevišķas papildu kategoriju hierarhijas, lai grupētu vai kategorizētu preces īpašiem nolūkiem, piemēram, akciju preces vai preču klāstos ietvertās preces. Izmantojot kategoriju hierarhijas, varat visas noteiktas kategorijas preces piešķirt preču klāstam. Visas preces, kas tiek pievienotas kategorijai, kas ir iekļauta preču klāstā, tiek automātiski iekļautas šajā preču klāstā. Pēc tam, nākamajā reizē, kad tiek palaists komercijas preču klāsta plānotājs, šīs preces kļūst pieejamas kanālos, kam ir piešķirts preču klāsts. |

## <a name="setting-up-an-assortment"></a>Preču klāsta iestatīšana

Pēc tam, kad esat izpildījis priekšnoteikumus, varat izveidot preču klāstu un piešķirt to saviem kanāliem. Lai iestatītu preču klāstu, ir jāizpilda tālāk norādītie uzdevumi.

1. Izveidojiet jaunu preču klāstu vai kopējiet esošu preču klāstu.
2. Atlasiet kanālus vai augsta līmeņa kanālu grupas, uz ko attiecas preču klāsts.
3. Pievienojiet preču klāstam preču kategorijas, atsevišķas preces vai preces variantus. Varat iekļaut visas noteiktas kategorijas preces vai arī varat izslēgt atlasītās preces no kategorijas, kas ir iekļauta preču klāstā.
4. Publicējiet preču klāstu. Publicējot preču klāstu, tiek automātiski palaists preču klāsta plānotājs. Izpildot šo procesu, tiek ģenerēts preču saraksts. Kad šis process ir pabeigts, preces kļūst pieejamas kanālos, kam ir piešķirts preču klāsts. Ja tiek mainīts publicēts preču klāsts vai kanāli, kam ir piešķirts šis preču klāsts, ir jāatjaunina šis preču klāsts. Lai atjauninātu preču klāstā, kad tiek veiktas izmaiņas, varat palaist preču klāsta plānotāju pakešuzdevuma režīmā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]