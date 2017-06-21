---
title: "Jaunumi un izmaiņas Dynamics AX programmas versijā 7.0.1 (2016. gada maijs)"
description: "Šajā rakstā ir aprakstītas funkcijas, kas Microsoft Dynamics AX programmas versijā 7.0.1 ir jaunas vai ir mainītas. Šī versija tika izlaista 2016. gada maijā, un tās būvējuma numurs ir 7.0.1265.23014."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8b58cb4f9de393b3f381dbe0aa4330d5ebd62795
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Jaunumi un izmaiņas Dynamics AX programmas versijā 7.0.1 (2016. gada maijs)

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstītas funkcijas, kas Microsoft Dynamics AX programmas versijā 7.0.1 ir jaunas vai ir mainītas. Šī versija tika izlaista 2016. gada maijā, un tās būvējuma numurs ir 7.0.1265.23014.

<a name="electronic-reporting-er"></a>Elektronisko atskaišu veidošana (ER)
-------------------------

|                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                                                                                                                                   | **Kāpēc tas ir svarīgi?**                                                                                                                                                                                                                                                                                                                             |
| Konfigurējiet izpildlaika dialoglodziņu elektronisko atskaišu veidošanas (Electronic reporting —ER) atskaišu noformēšanai, lai lietotāji varētu izvēlēties vēlamās finanšu dimensijas.                                     | Izpildlaikā ER atskaites izpildes dialoglodziņā lietotāji var atlasīt vairākas finanšu dimensijas. Atlasīto finanšu dimensiju detalizētā informācija tiek rādīta elektroniskajā dokumentā, kas tiek ģenerēts.                                                                                                                              |
| Konfigurēt piekļuvi vairākām finanšu dimensijām ER atskaites veidošanas laikā, izmantojot vienu kartēšanu uz nepieciešamo datu avotu.                                                  | To pašu ER atskaites konfigurāciju var izmantot, lai veidotu elektroniskus dokumentus, kuros transakciju dati ir norādīti kopā ar informāciju par finanšu dimensijām, neatkarīgi no lietotāja atlasīto vai pašreizējai juridiskajai personai vai instancei konfigurēto finanšu dimensiju skaita.                                             |
| Konfigurējiet ER atskaiti, lai ievadītu datus dinamiski ģenerētās elektroniska dokumenta kolonnās, kurš tiek veidots OPENXML darblapas formātā.                                           | ER atskaite var ievadīt datus OPENXML darblapā, kas tiek ģenerēta, horizontāli replicējot kolonnas. Līdz ar to tādu pašu ER atskaites konfigurāciju var izmantot atkārtoti, lai ģenerētu elektroniskus dokumentus, kuros ir atšķirīgs dinamiski ģenerēto kolonnu skaits.                                                                                 |
| Konfigurējiet ER galamērķus, lai formāta izvades rezultāts būtu vērsts uz konkrētu galamērķi: failu, e-pasta ziņojumu vai arhīvu (Microsoft SharePoint mapes vai Microsoft Azure krātuve). | Iepriekš, kad izpildījāt ER konfigurēšanu, tika parādīts ziņojuma lodziņš, kas lietotājam pieprasīja kaut ko darīt, lai failu saglabātu vai atvērtu. Tagad varat jau iepriekš konfigurēt adresātu katrai formāta konfigurācijai un katram izvades komponentam (mapei vai failam) atsevišķi. Lietotāji, kuriem ir atbilstošas piekļuves tiesības, mērķa iestatījumus var modificēt arī izpildlaikā. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS — Microsoft Dynamics AX Retail
|                                |                                                                                                                                                                                         |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**           | **Kāpēc tas ir svarīgi?**                                                                                                                                                              |
| Izmantojiet pārlūku Google Chrome. | Mākoņa POS mazumtirgotāji tagad var palaist no pārlūka Chrome un var baudīt visu funkcionalitāti, kas ir pieejami Microsoft Edge un Internet Explorer mākoņa POS versijā. |

## <a name="financial-reporting"></a>Finanšu pārskati
|                                                                     |                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                | **Kāpēc tas ir svarīgi?**                                                                                                                                                                                                                                                                                         |
| Atkārtoti izveidojiet finanšu atskaišu veidošanas datuvi.                          | Ja Dynamics AX datu bāze tiek pārvietota uz citu vidi vai tiek veiktas citas būtiskas vides izmaiņas, iespējams, ir atkārtoti jāizveido finanšu pārskatu datu bāze. Tagad ir pieejams Windows PowerShell skripts, kas nodrošina datu bāzes atkārtotu izveidi.                                                                |
| Vairs nevarat atlasīt atskaišu veidotāja opcijas, kas nav derīgas. | Vairākas atskaišu veidotāja opcijas, kas tika izmantotas tirgū pieejamajās Management Reporter versijās, netiek izmantotas šajā Dynamics AX versijā. Šīs opcijas bija saistītas ar finanšu pārskatu izstrādi, izvadi un saistīšanu. Šīs opcijas ir noņemtas no finanšu pārskatu veidotāja, lai nepieļautu lietotāja kļūdas. |

## <a name="financial-management"></a>Finanšu pārvaldība
|                                                            |                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                       | **Kāpēc tas ir svarīgi?**                                       |
| Ģenerējiet pozitīvo maksājumu failus kreditoriem veicamajiem maksājumiem. | Pozitīvā maksājuma failus var ģenerēt, lai palīdzētu novērst krāpšanos ar čekiem. |

## <a name="warehouse-and-production"></a>Noliktava un ražošana
|                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                                                                                                                                                                                                                                                                                                                                    | **Kāpēc tas ir svarīgi?**                                                                                                                                                                                                                                                                                                                                                                                                              |
| Definējiet noliktavas darba politiku, kas kontrolē darba izveidošanu preču kopai konkrētos novietojumos.                                                                                                                                                                                                                                                                          | Ne vienmēr noliktavas procesi ietver darbu. Izmantojot jauno noliktavu darba politiku, varat novērst darba izveidošanu izejmateriālu izdošanai un gatavās produkcijas izvietošanai kādai preču kopai konkrētos novietojumos.                                                                                                                                                                                                     |
| Norādiet, ka ražošanas izlaides novietojums nav atkarīgs no numura zīmes.                                                                                                                                                                                                                                                                                                               | Tagad varat norādīt, ka preces izvades novietojums nav atkarīgs no numura zīmes. Piemēram, šis līdzeklis noder, kad augšupstraumes ražošanas pasūtījums par krājumiem kā pabeigtiem ziņo tieši uz novietojumu, kas darbojas kā ražošanas ievades novietojums kādam lejupstraumes ražošanas pasūtījumam.                                                                                                                                                     |
| Atbalstiet MK, kuros ir ietverti krājumi ar tā paša krājuma atšķirīgām preces dimensijām.                                                                                                                                                                                                                                                                                                     | Ja ražošanā lietojat vienu vai vairākas preces dimensijas, var rasties situācijas, kad vēlaties ražot kādu krājumu, balstoties uz citu tā paša krājuma variantu. Papildinformāciju skatiet [šajā emuārā](https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/).                                                                  |
| Ražošanas pasūtījumi ar cikliskajām struktūrām to MK pirmajā līmenī tiek izslēgtas no MK līmeņa aprēķina materiālo resursu plānošanai.                                                                                                                                                                                                                                     | Nav iespējams piešķirt pareizus MK līmeņus preču variantiem tādos ražošanas pasūtījumos, kas MK hierarhijā izraisa cikliskumu.                                                                                                                                                                                                                                                                                                  |
| Aprēķināt atsevišķus MK līmeņus materiālu resursu plānošanai un izmaksu aprēķinam. • Materiālu resursu plānošanas MK līmeņi tiek aprēķināti jaunajā tabulā **ReqItemLevel**. Pabeigtie ražošanas pasūtījumi šajā aprēķinā netiek ņemti vērā. • Ražošanas izmaksu aprēķināšanai MK līmeņi tiek aprēķināti tabulā **InventTable**. Pabeigtie ražošanas pasūtījumi tiek iekļauti šajā aprēķinā. | • Izpildot materiālo resursu plānošanu, piemēram, vispārējās plānošanas plāna grafika izveidošanu un izvēršanu, ir nepieciešams pārrēķināt tikai tos MK līmeņus, kas tika izmantoti materiālo resursu plānošanai. Citiem vārdiem sakot, nav nepieciešams aprēķināt ražošanas izmaksu aprēķināšanai izmantotos MK līmeņus. • Izpildot izmaksu aprēķināšanas operācijas, piemēram, krājumu slēgšanu, ir nepieciešams pārrēķināt tikai MK līmeņus, kas tika izmantoti ražošanas izmaksu aprēķinā. |

 

<a name="see-also"></a>Skatiet arī
--------

[Jaunumi un izmaiņas](whats-new-changed.md)

[Jauni vai atjaunināti uzdevumu ceļveži (2016. gada maijs)](new-updated-task-guides-available-may-2016.md)




