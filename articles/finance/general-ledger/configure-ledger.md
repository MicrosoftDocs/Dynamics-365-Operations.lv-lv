---
title: Virsgrāmatas konfigurēšana
description: Šī tēma sniedz informāciju par to, kā konfigurēt Virsgrāmatu katrai juridiskajai personai. Tajā iekļauta informācija par to, kā atlasīt valūtas, fiskālos kalendārus, kontu plānu un kontu struktūras, kas jāizmanto katrai juridiskajai personai.
author: kweekley
manager: ''
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5a7fcda435fd957edbbe09d796685c0c742dc6a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975820"
---
# <a name="configure-ledgers"></a>Virsgrāmatas konfigurēšana

[!include [banner](../includes/banner.md)]

Šī tēma sniedz informāciju par to, kā konfigurēt Virsgrāmatu katrai juridiskajai personai. Tajā iekļauta informācija par to, kā atlasīt valūtas, fiskālos kalendārus, kontu plānu un kontu struktūras, kas jāizmanto katrai juridiskajai personai.

## <a name="selecting-the-chart-of-accounts"></a>Kontu plāna atlasīšana

Katrai juridiskajai personai Microsoft Dynamics 365 Finance ir jākonfigurē detalizēta informācija par Virsgrāmatu. Lapa **Virsgrāmata** ļauj atlasīt kontu plānu un konta struktūras, kas tiks izmantotas atlasītajai juridiskajai personai. Varat kopīgot savu kontu plānu un konta struktūras, konfigurējot lapu **Virsgrāmata** katrā juridiskajā personā, lai izmantotu to pašu kontu plānu un konta struktūras. Katrā juridiskajā personā varat arī kopīgot konfigurācijas daļu, un katrai juridiskajai personai var būt īpašas konfigurācijas.

Ja juridiskajām personām ir nepieciešami dažādi kontu plāni vai dažādas konta struktūras, var būt noderīgs juridiskās personas pārlabošanas līdzeklis. Lietojot vienu un to pašu kontu shēmu un konta struktūras vairākām juridiskajām personām un pēc tam pārvaldot jebkurus izņēmumus, izmantojot juridiskās personas pārlabošanu, laika gaitā varat vienkāršot uzturēšanu.

Lai konfigurētu kontu plānu juridiskajai personai, dodieties **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmata**. Lapā **Virsgrāmata** atlasiet **Kontu plāns** un pēc tam saraksta atlasiet izmantojamo kontu plānu. Ņemiet vērā, ka kontu plānu nevar mainīt pēc tam, kad ir atlasīta vērtība un juridiskajā personā grāmatoti darījumi.

Lai iegūtu vairāk informācijas par to, kā plānot un konfigurēt kontu plānu un galvenos kontus, skatiet [Kontu plāna ieplānošana](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Konta struktūru atlasīšana

Katru juridisko personu Dynamics 365 Finance var konfigurēt, lai izmantotu vienu vai vairākas konta struktūras. Katra konta struktūra definē finanšu dimensijas un galveno kontu un finanšu dimensiju kombinācijas, kas tiks atļautas, grāmatojot darījumus. Varat izmantot vienas un tās pašas konta struktūras vairāk kā vienā juridiskajā personā.

Ņemiet vērā, ja jums ir vairākas konta struktūras, varat atlasīt tikai tās konta struktūras, kurām nepārklājas galveno kontu un finanšu dimensiju kombinācijas. Piemēram, viena no jūsu konta struktūrām ir konfigurēta, lai pievienotu biznesa vienību galvenajiem kontiem starp 1000 un 1999. Citā konta struktūrā jūs esat pievienojis nodaļas finanšu dimensiju galvenajiem kontiem, kas sākas ar 1. Šādā gadījumā vienai un tai pašai juridiskajai personai var pievienot tikai vienu no konta struktūrām.

Lai konfigurētu konta struktūras savai Virsgrāmatai, lapā **Virsgrāmata** kopsavilkuma cilnē **Konta struktūras** atlasiet **Pievienot**, sarakstā atlasiet konta struktūru un pēc tam atlasiet **Atlasīt**. Var paiet dažas minūtes, kamēr konta struktūras tiks pievienotas un saglabātas. Ņemiet vērā, ka jūsu atlasītajām konta struktūrām jābūt aktīvām. Pretējā gadījumā konta struktūru detalizētā informācija nebūs spēkā juridiskajās personās, kur tā ir saistītas.

Lai noņemtu konta struktūru, lapā **Virsgrāmata** kopsavilkuma cilnē **Konta struktūras** atlasiet **Noņemt**. Ņemiet vērā, ka, noņemot konta struktūru no Virsgrāmatas, netiek noņemti darījumi, kas tika grāmatotas, izmantojot konta struktūras konfigurāciju.

Vairāk informācijas par to, kā iestatīt konta struktūras, skatiet [Konta struktūru konfigurēšana](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Kalendāru konfigurēšana Virsgrāmatai

Cits Virsgrāmatas komponents ir fiskālais kalendārs. Fiskālais kalendārs ir jāatlasa katrai juridiskajai personai. Varat izmantot vienu un to pašu fiskālo kalendāru vairāk kā vienā juridiskajā personā. Atlasot Virsgrāmatas fiskālo kalendāru, tiek izveidota kopija. Šī kopija tiek saukta par Virsgrāmatas kalendāru. Virsgrāmatas kalendārs ļauj atlasīt periodu un moduļu statusu katrā periodā.

Lai piekļūtu atlasītās juridiskās personas kalendāram un atjauninātu to, lapā **Virsgrāmata** darbību rūtī atlasiet **Virsgrāmatas kalendārs**.

Lai atlasītu kalendāru, atlasiet **Fiskālie kalendāri** un pēc tam sarakstā atlasiet kalendāru. Ja maināt fiskālo kalendāru pēc darījumu grāmatošanas juridiskajā personā, jāatlasa **Pārrēķināt Virsgrāmatas periodus**. Pēc tam dialoglodziņā, kas tiek parādīts, varat atjaunināt Virsgrāmatas bilances periodiem kalendārā. Ieteicams palaist procesu **Pārrēķināt Virsgrāmatas periodus** režīmā **Partijas**, un to palaist, kad sistēmā nenotiek būtiski procesi. Atkarībā no darījumu un finanšu dimensiju kombināciju skaita šis process var aizņemt kādu laiku.

Ja juridiskajai personai nav atlasīts fiskālais kalendārs, tiks parādīts kļūdas ziņojums, mēģinot grāmatot darījumu šajā juridiskajā personā.

Papildinformāciju skatiet rakstā [Finanšu kalendāri, finanšu gadi un periodi](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Līdzsvarošanas finanšu dimensijas izmantošana

Pēc kontu plāna atlasīšanas un vienas vai vairāku konta struktūru pievienošanas, pēc izvēles varat atlasīt vienu finanšu dimensiju, ko izmantot kā līdzsvarošanas finanšu dimensiju. Atlasītajai dimensijai ir jāpastāv visās konta struktūrās. Tas arī jābūt līdzsvarotai visos uzskaites ierakstos. Citiem vārdiem, debetam un kredītam ir jābūt vienādiem galvenajā kontā un līdzsvarošanas finanšu dimensijā. Sistēma automātiski izveido darījumus, lai sabalansētu ierakstus, pamatojoties uz galvenajiem kontiem, kas ir norādīti laukos **Starpvienības — kredīts** un **Starpvienības — debets** lapā **Automātisko darījumu konti**.

Lai iegūtu papildu informāciju par līdzsvarošanas ierakstiem, skatiet [Starpvienību uzskaites līdzsvarotie žurnāli](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Valūtu konfigurēšana Virsgrāmatai

Lapa **Virsgrāmata** lapa tiek izmantota arī, lai kontrolētu un definētu valūtas, kas tiks izmantotas, kad darījumi tiek grāmatoti Virsgrāmatā. Ir jānorāda uzskaites valūta, kas ir valūta, kāda tiek izmantota visos dokumentos Virsgrāmatas kolonnā **Virsgrāmatas valūta**. Turklāt kolonnā **Pārskata valūta** varat pēc izvēles atlasīt otru valūtu. Ja atlasāt pārskata valūtu, visi darījumi tiks ierakstīti šajā valūtā visos dokumentos Virsgrāmatas kolonnā **Pārskata valūta**.

Ja darījumi ir grāmatotas citā valūtā, sistēma automātiski konvertē darījuma summu no darījuma valūtas uzskaites valūtā un dokumenta pārskata valūtā. Lapas **Virsgrāmata** laukā **Uzskaites valūtas maiņas kursa veids** atlasiet valūtas maiņas kursa veidu, kas konfigurēts maiņas kursiem, kas jāizmanto, konvertējot vērtības no darījuma valūtas uz dokumenta uzskaites valūtu. Ja atlasījāt pārskata valūtu, ir jāiestata arī lauks **Pārskata valūtas maiņas kursa veids**, lai norādītu valūtas maiņas kursu, kas jāizmanto, konvertējot vērtības no darījuma valūtas uz dokumenta pārskata valūtu.

Ja izmantojat budžeta veidošanas funkcionalitāti, varat arī iestatīt lauku **Budžeta maiņas kursa veids**, lai norādītu maiņas kursu, kas jāizmanto budžeta darījumu konvertēšanai no vienas valūtas citā.

Ja izmantojat divas valūtas vai izmantojat vienu valūtu, bet darījumi tiek grāmatoti citā valūtā, jākonfigurē kopsavilkuma cilne **Konti valūtas pārvērtēšanai** lapā **Virsgrāmata**. Šajā kopsavilkuma cilnē tiek definēti noklusējuma realizētās un nerealizētās peļņas un zaudējumu konti, kas tiks lietoti pēc noklusējuma, grāmatojot darījumus, ja lapā **Valūtas pārvērtēšanas konti** nav norādīts neviens konts. (Lapas **Valūtas pārvērtēšanas konti** tiek izmantota, lai katrai valūtai konfigurētu dažādus kontus realizētai un nerealizētai peļņai un zaudējumiem.)

Realizētā peļņa un zaudējumi ir peļņa un zaudējumi, kas gūti no pabeigtiem darījumiem. Tie tiek ierakstīti peļņas un zaudējumu aprēķinā. Nerealizētā peļņa un zaudējumi ir peļņa un zaudējumi, kas ir radušies, bet darījums nav pabeigts. Citiem vārdiem, esat, piemēram, grāmatojis rēķinu, bet tas vēl nav nosegts un apmaksāts. Nerealizētā peļņa un zaudējumi tiek ierakstīti bilancē.

Lai iegūtu vairāk informācijas par to, kā izmantot divas valūtas, skatiet [Divas valūtas](dual-currency.md).
