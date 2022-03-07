---
title: Jaunumi un izmaiņas Dynamics AX programmas versijā 7.0.1 (2016. gada maijs)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti Microsoft Dynamics AX programmas versijā 7.0.1. Šī versija tika izlaista 2016. gada maijā, un tās būvējuma numurs ir 7.0.1265.23014.
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 9a455ffbc4396ea4bf0e3df12e7acdcbfeaa5f5269dbe772848341ac0d22a5e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748268"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Jaunumi un izmaiņas Dynamics AX programmas versijā 7.0.1 (2016. gada maijs)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti Microsoft Dynamics AX programmas versijā 7.0.1. Šī versija tika izlaista 2016. gada maijā, un tās būvējuma numurs ir 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Elektronisko atskaišu veidošana (ER)

| Ko iespējams izdarīt? | Kāpēc tas ir svarīgi? |
|------------------|------------------------|
| Konfigurējiet izpildlaika dialoglodziņu elektronisko atskaišu veidošanas (Electronic reporting —ER) atskaišu noformēšanai, lai lietotāji varētu izvēlēties vēlamās finanšu dimensijas. | Izpildlaikā ER atskaites izpildes dialoglodziņā lietotāji var atlasīt vairākas finanšu dimensijas. Atlasīto finanšu dimensiju detalizētā informācija tiek rādīta elektroniskajā dokumentā, kas tiek ģenerēts. |
| Konfigurēt piekļuvi vairākām finanšu dimensijām ER atskaites veidošanas laikā, izmantojot vienu kartēšanu uz nepieciešamo datu avotu. | To pašu ER atskaites konfigurāciju var izmantot, lai veidotu elektroniskus dokumentus, kuros transakciju dati ir norādīti kopā ar informāciju par finanšu dimensijām, neatkarīgi no lietotāja atlasīto vai pašreizējai juridiskajai personai vai instancei konfigurēto finanšu dimensiju skaita. |
| Konfigurējiet ER atskaiti, lai ievadītu datus dinamiski ģenerētās elektroniska dokumenta kolonnās, kurš tiek veidots OPENXML darblapas formātā. | ER atskaite var ievadīt datus OPENXML darblapā, kas tiek ģenerēta, horizontāli replicējot kolonnas. Līdz ar to tādu pašu ER atskaites konfigurāciju var izmantot atkārtoti, lai ģenerētu elektroniskus dokumentus, kuros ir atšķirīgs dinamiski ģenerēto kolonnu skaits. |
| Konfigurējiet ER galamērķus, lai formāta izvades rezultāts būtu vērsts uz konkrētu galamērķi: failu, e-pasta ziņojumu vai arhīvu (Microsoft SharePoint mape vai Microsoft Azure krātuve). | Iepriekš, kad izpildījāt ER konfigurēšanu, tika parādīts ziņojuma lodziņš, kas lietotājam pieprasīja kaut ko darīt, lai failu saglabātu vai atvērtu. Tagad varat jau iepriekš konfigurēt adresātu katrai formāta konfigurācijai un katram izvades komponentam (mapei vai failam) atsevišķi. Lietotāji, kuriem ir atbilstošas piekļuves tiesības, mērķa iestatījumus var modificēt arī izpildlaikā. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX Retail

| Ko iespējams izdarīt? | Kāpēc tas ir svarīgi? |
|------------------|------------------------|
| Izmantojiet pārlūku Google Chrome. | Mazumtirgotāji tagad var palaist Cloud POS no pārlūkprogrammas Chrome un var baudīt visu funkcionalitāti, kas ir pieejama Cloud POS Microsoft Edge un Internet Explorer versijā. |

## <a name="financial-reporting"></a>Finanšu pārskati

| Ko iespējams izdarīt? | Kāpēc tas ir svarīgi? |
|------------------|------------------------|
| Atkārtoti izveidojiet finanšu atskaišu veidošanas datuvi. | Ja Dynamics AX datu bāze tiek pārvietota uz citu vidi vai tiek veiktas citas būtiskas vides izmaiņas, iespējams, ir atkārtoti jāizveido finanšu pārskatu datu bāze. Tagad ir pieejams Windows PowerShell skripts, kas nodrošina datu bāzes atkārtotu izveidi. |
| Vairs nevarat atlasīt atskaišu veidotāja opcijas, kas nav derīgas. | Vairākas atskaišu veidotāja opcijas, kas tika izmantotas tirgū pieejamajās Management Reporter versijās, netiek izmantotas šajā Dynamics AX versijā. Šīs opcijas bija saistītas ar finanšu pārskatu izstrādi, izvadi un saistīšanu. Šīs opcijas ir noņemtas no finanšu pārskatu veidotāja, lai nepieļautu lietotāja kļūdas. |

## <a name="financial-management"></a>Finanšu pārvaldība

| Ko iespējams izdarīt? | Kāpēc tas ir svarīgi? |
|------------------|------------------------|
| Ģenerējiet pozitīvo maksājumu failus kreditoriem veicamajiem maksājumiem. | Pozitīvā maksājuma failus var ģenerēt, lai palīdzētu novērst krāpšanos ar čekiem. |

## <a name="warehouse-and-production"></a>Noliktava un ražošana

<table>
<thead>
<tr>
<th>Ko iespējams izdarīt?</th>
<th>Kāpēc tas ir svarīgi?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definējiet noliktavas darba politiku, kas kontrolē darba izveidošanu preču kopai konkrētos novietojumos.</td>
<td>Ne vienmēr noliktavas procesi ietver darbu. Izmantojot jauno noliktavu darba politiku, varat novērst darba izveidošanu izejmateriālu izdošanai un gatavās produkcijas izvietošanai kādai preču kopai konkrētos novietojumos.</td>
</tr>
<tr>
<td>Norādiet, ka ražošanas izlaides novietojums nav atkarīgs no numura zīmes.</td>
<td>Tagad varat norādīt, ka preces izvades novietojums nav atkarīgs no numura zīmes. Piemēram, šis līdzeklis noder, kad augšupstraumes ražošanas pasūtījums par krājumiem kā pabeigtiem ziņo tieši uz novietojumu, kas darbojas kā ražošanas ievades novietojums kādam lejupstraumes ražošanas pasūtījumam.</td>
</tr>
<tr>
<td>Atbalstiet MK, kuros ir ietverti krājumi ar tā paša krājuma atšķirīgām preces dimensijām.</td>
<td>Ja ražošanā lietojat vienu vai vairākas preces dimensijas, var rasties situācijas, kad vēlaties ražot kādu krājumu, balstoties uz citu tā paša krājuma variantu. Papildinformāciju skatiet <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">šajā emuārā</a>.</td>
</tr>
<tr>
<td>Ražošanas pasūtījumi ar cikliskajām struktūrām to MK pirmajā līmenī tiek izslēgtas no MK līmeņa aprēķina materiālo resursu plānošanai.</td>
<td>Nav iespējams piešķirt pareizus MK līmeņus preču variantiem tādos ražošanas pasūtījumos, kas MK hierarhijā izraisa cikliskumu.</td>
</tr>
<tr>
<td>Aprēķiniet atsevišķus MK līmeņus materiālo resursu plānošanai un izmaksu aprēķinam:
<ul>
<li>Materiālo resursu plānošanai MK līmeņi tiek aprēķināti jaunajā tabulā <strong>ReqItemLevel</strong>. Pabeigtie ražošanas pasūtījumi šajā aprēķinā netiek ņemti vērā.</li>
<li>Ražošanas izmaksu aprēķināšanai MK līmeņi tiek aprēķināti tabulā <strong>InventTable</strong>. Pabeigtie ražošanas pasūtījumi tiek iekļauti šajā aprēķinā.</li>
</ul>
</td>
<td>
<ul>
<li>Izpildot materiālo resursu plānošanu, piemēram, vispārējās plānošanas plāna grafika izveidošanu un izvēršanu, ir nepieciešams pārrēķināt tikai tos MK līmeņus, kas tika izmantoti materiālo resursu plānošanai. Citiem vārdiem sakot, nav nepieciešams aprēķināt ražošanas izmaksu aprēķināšanai izmantotos MK līmeņus.</li>
<li>Izpildot izmaksu aprēķināšanas operācijas, piemēram, krājumu slēgšanu, ir jāpārrēķina tikai tie MK līmeņi, kas ir izmantoti ražošanas izmaksu aprēķinam.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildu resursi

[Jaunumi un izmaiņas Finance and Operations sākumlapā](whats-new-changed.md)

[Jauni vai atjaunināti uzdevumu ceļveži (2016. gada maijs)](new-updated-task-guides-available-may-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]