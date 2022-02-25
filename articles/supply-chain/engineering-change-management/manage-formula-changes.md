---
title: Pārvaldīt izmaiņas formulās un to sastāvdaļās
description: Šajā tēmā ir aprakstīts, kā veikt formulas pārvaldību un pārvaldīt izmaiņas ražošanas pamatdatu apstrādāšanai.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 31953fd29c471e52bd63dbb02c20f5f224c3cae2
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103048"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Pārvaldīt izmaiņas formulās un to sastāvdaļās

[!include [banner](../includes/banner.md)]

Ja izmantojat Microsoft Dynamics 365 Supply Chain Management procesa ražošanas iespējas, varat izmantot arī saistītās formulas pārvaldības iespējas, lai pārvaldītu šādas izmaiņas:

- **Formulas un plānošanas krājumi:** pārvaldīt sastāvdaļu izmaiņas formulās un to līdzproduktos un blakusproduktos.
- **Līdzprodukti un blakusprodukti:** rediģējiet formulā līdzproduktu un blakusproduktu daudzumus un citu informāciju.
- **Pieļaujamā svara krājumi:** pārvaldīt pieļaujamā svara krājumu izmaiņas.

## <a name="turn-this-feature-on-or-off"></a>Ieslēgt vai izslēgt šo līdzekli

Šajā tēmā aprakstītajai funkcionalitātei ir nepieciešams, lai *gan* *inženierzinātnes izmaiņu pārvaldība, gan pārvaldīt izmaiņas formulās un to sastāvdaļas būtu ieslēgtas* jūsu sistēmai. Papildinformāciju par to, kā ieslēgt vai izslēgt šos līdzekļus, skatiet inženierzinātnes [izmaiņu pārvaldības pārskatā](product-engineering-overview.md).

## <a name="feature-naming-conventions"></a>Līdzekļu nosaukumdošanas konvencijas

Supply Chain Management lietotāja interfeisā (Ui) un dokumentācijā izmaiņu pārvaldības funkcionalitāte parasti tiek saukta par *inženiertehnisko izmaiņu pārvaldību*, un pārvaldāmās preces parasti tiek sauktas par *inženiertehniskajām precēm*. Lai arī šī terminoloģija parasti nav saistīta ar procesa ražošanas formulu pārvaldību, jums jāpadomā par inženiertehnisko izmaiņu pārvaldību kā vienkārši izmaiņu pārvaldību, un jums jāpadomā par inženiertehniskajām precēm kā versijai izveidotu preci.

## <a name="work-with-formula-change-management-features"></a>Darbs ar formulas izmaiņu pārvaldības funkcijām

Šajā sarakstā tiek apkopots, kā inženiertehniskās izmaiņu pārvaldības funkcijas attiecas uz formulas pārvaldību. Tas arī nodrošina saites uz plašāku informāciju. Tā kā formulas izmaiņu pārvaldība izmanto inženiertehnisko izmaiņu pārvaldības līdzekļu priekšrocības, jums vajadzētu uzzināt, kā inženiertehnisko izmaiņu pārvaldība darbojas kopumā, lai to varētu izmantot, lai pārvaldītu formulas un to sastāvdaļas.

- **Centralizēta preču datu pārvaldība** – iestatiet organizāciju, kas, izmantojot pārvaldītu izlaišanas procesu, nodrošina, ka uzņēmuma lietotājiem ir pieejami precīzi un atbilstoši preces dati. Papildinformāciju skatiet šeit: [Inženiertehniskie uzņēmumi un datu īpašumtiesību kārtulas](engineering-org-data-ownership-rules.md).
- **Preču versijas** – izsekojiet preču izmaiņām, izmantojot preču versijas, un kontrolējiet preci visās piegādes ķēdes stadijās. Šādā veidā varat izsekot izmaiņām jūsu formulās. Papildinformāciju skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).
- **Preču dzīves cikla pārvaldība** – pārvaldiet preču datu redzamību organizācijā un kontrolējiet preču versiju pieejamību katrā piegādes ķēdes posmā. Jums ir detalizēta kontrole pār to, kad preču versiju var izmantot konkrētos biznesa procesos, un varat izveidot savus dzīves cikla stāvokļus, lai tie atbilstu uzņēmuma vajadzībām. Papildinformāciju skatiet šeit: [Produktu dzīves cikla stāvokļi un darījumi](product-lifecycle-state-transactions.md).
- **Formulas izmaiņu pārvaldība** – lietotāji savā organizācijā var pieprasīt izmaiņas formulās. Izmantojiet izmaiņu pasūtījumus, lai novērtētu un dokumentētu piedāvāto izmaiņu ietekmi. Pievienojiet darbplūsmas, lai pārvaldītu izmaiņu procesu un izlaistu jaunas preču versijas un to formulas. Plašāku informāciju skatiet rakstā [Pārvaldīt izmaiņas tehniskajām precēm](engineering-change-management.md).
- **Gatavības kontrole** – izmantojiet sistēmas pārbaudes un lietotāju vadlīnijas (anketas un kontrolsaraksti), lai nodrošinātu, ka visi nepieciešamie preces dati ir pilnībā ievadīti pirms preces laišanas izpildei. Papildinformāciju skatiet sadaļā [Produktu gatavība](product-readiness.md).
- **Uzlabota preču laidiena funkcionalitāte** – nodot preces pilnībā definētās versijas un to formulu no organizācijas (juridiskas personas) citām juridiskām personām. Var arī izlemt, vai preces informācija ir jāpārskata vai jālabo pirms izlaišanas. Plašāku informāciju skatiet sadaļā [Izlaist produkta struktūras](release-product-structure.md).

Ievērojiet, ka lielākā daļa tēmu, kas ir saistītas ar iepriekšējo sarakstu, sniedz piemērus, kas balstīti uz materiālu komplektiem (MK). Tomēr formulas darbojas līdzīgi. Šeit ir dažas papildu koncepcijas, kas ir noderīgas, lai uzzinātu, kad izmantojat izmaiņu pārvaldību (vai tikai formulas izmaiņu pārvaldību), lai pārvaldītu formulas un MK:

- Katrai [preču inženiertehniskajai kategorijai](engineering-versions-product-category.md) var norādīt ražošanas tipu (MK, formulu vai plānošanas krājumu). Var arī norādīt, vai precēm, kas izmanto šo kategoriju, ir nepieciešams pieļaujamā svara atbalsts.
- Līdzprodukti un blakusprodukti nav inženiertehniskās preces. Tādēļ to versija nav iestatīta. Ja tās ir jāmaina, vienkārši izveidojiet jaunu preci. Šī pieeja atvieglo uzturēšanu.
- Varat pārvaldīt gala produktus, kas ir MK un kuriem ir pakārtotās formulas krājumi. Funkcionalitāte darbosies jebkurai MK kombinācijai, kas ietver formulas un/vai formulas, kas satur MK.
