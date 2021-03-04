---
title: Sagatavošanās darba ar Human Resources sākšanai
description: Šajā lapā ir sniegti norādījumi par to, kā sagatavoties darbam ar Dynamics 365 Human Resources.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: b40d6ce45aeb07724fc41d1a41923970b007fbcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/14/2020
ms.locfileid: "4419621"
---
# <a name="prepare-for-human-resources-go-live"></a>Sagatavošanās darba ar Human Resources sākšanai

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā sagatavoties doties ar projektu Dynamics 365 Human Resources, izmantojot Microsoft Dynamics Lifecycle Services (LCS). 

Šajā grafikā ir parādīti darba sākšanas procesa posmi. 

![Darba sākšanas process](./media/hr-admin-go-live-prepare-process.png)

Tabulā zemāk ir uzskaitīti visi procesa soļi, paredzamais ilgums un atbildīgais par darbību.

| Fāze | Darbība | Ilgums/kad | Kurš | Piezīmes |
| --- | --- | --- | --- |--- |
| 1 | Darba sākšanas datuma atjaunināšana LCS | Vēlākais 2-3 mēnešus iepriekš | Partneris/Klients | Atskaites punktu datumiem jābūt pastāvīgi atjauninātiem. |
| 2 | Kontrolsaraksta pabeigšana un nosūtīšana | Pēc lietotāju akceptēšanas testēšana (UAT) ir pabeigta | Partneris/Klients | Ievērojiet instrukcijas, kas sniegtas sadaļā [FastTrack darba sākšanas novērtējums](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projekta novērtējums (FastTrack) | FastTrack arhitekts* | Arhitekts sniedz novērtējumu pēc kontrolsaraksta saņemšanas un turpina pārskatīšanu, līdz tiek noskaidroti jautājumi vajadzības gadījumā tiek ieviesta problēmu mazināšana. |
| 4 | Projekta seminārs (FastTrack) | FastTrack arhitekts* | |
| 5 | Datu pakotnes importēšana | Atkarīgs no projekta | Partneris/Klients | Ievērojiet instrukcijas, kas sniegtas sadaļā [Datu pārvaldības pārskats](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).|
| 6 | Ražošana ir gatava | Pēc tam, kad visas iepriekšējās darbības ir pabeigtas | Partneris/Klients | Partneris/Klients var veikt ražošanas vides kontroli.|
| 7 | Pārslēgšanas aktivitātes | Atkarīgs no projekta | Partneris/Klients | |
| 8 | Palaišana | Atkarīgs no projekta | Debitors | |

> [!IMPORTANT]
> *3. un 4. solis ir pabeigts tikai tiem klientiem, kuri kvalificējas FastTrack.

## <a name="completing-the-lcs-methodology"></a>LCS metodoloģijas pabeigšana

Svarīgs atskaites punkts katrā īstenošanas projektā ir pārslēgšana uz ražošanas vidi. 

Lai palīdzētu nodrošināt ražošanas vides izmantošanu sākšanas operācijām, korporācija Microsoft nodrošina ražošanas instanci tikai tad, kad ieviešana tuvojas **Ekspluatācijas** fāzei — pēc tam, kad ir pabeigtas nepieciešamās aktivitātes LCS metodoloģijā. Plašāku informāciju par vidēm jūsu abonementā skatiet sadaļā  [Dynamics 365 licencēšanas rokasgrāmata](https://go.microsoft.com/fwlink/?LinkId=866544). 

Klientiem ir jāpabeidz fāzes **Analīze**, **Projektēšana un izstrāde** un **Testēšana** LCS metodoloģijā, pirms ir pieejama poga  **Konfigurēt** , kas nepieciešama ražošanas vides pieprasīšanai. Lai varētu pabeigt fāzi LCS, jums vispirms ir jāizpilda visas nepieciešamās darbības šajā fāzē. Kad visas fāzes darbības ir pabeigtas, varat pabeigt visu fāzi. Ja jāveic izmaiņas, vienmēr varat atvērt fāzi vēlāk. Papildinformāciju skatiet sadaļā  [Lifecycle Services (LCS) programmu Finance and Operations klientiem](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs). 

Darbības pabeigšanas procesam ir divas tālāk minētās daļas. 

- Paveikt faktisko darbu, piemēram, atbilstību analīzi vai lietotāju akceptēšanas testēšanu (UAT). 
- Atzīmēt atbilstošo darbību LCS metodoloģijā kā pabeigtu. 

Laba prakse ir pabeigt darbības metodoloģijā, virzoties uz priekšu ieviešanā. Negaidiet līdz pēdējai minūtei. Lai varētu iegūt ražošanas vidi, neklikšķiniet vienkārši uz visām darbībām. Klienta interesēs ir stingra ieviešana. 

## <a name="uat-for-your-solution"></a>UAT jūsu risinājumam

UAT fāzes laikā ieviešanas projektā smilškastes vidē ir jāpārbauda visi jūsu ieviestie biznesa procesi un visi veiktie pielāgojumi. Lai palīdzētu nodrošināt sekmīgu darba sākšanu, pabeidzot UAT fāzi, ņemiet vērā tālāk minēto. 

- Testa gadījumi aptver visu prasību jomu. 
- Testējiet, izmantojot migrētos datus. Šajos datos jāiekļauj pamatdati, piemēram, darbinieki, darbi un amati. Iekļaujiet arī sākuma bilances, piemēram, atvaļinājumu un prombūtnes uzkrājumus. Visbeidzot iekļaujiet atvērtās transakcijas, piemēram, pašreizējās atvieglojumu reģistrācijas. Pabeidziet testēšanu ar visiem datu veidiem pat tad, ja datu kopa nav pabeigta. 
- Testējiet, izmantojot pareizās drošības lomas (noklusējuma lomas un pielāgotās lomas), kas piešķirtas lietotājiem. 
- Pārliecinieties, vai risinājums atbilst visām uzņēmumas un nozarei specifiskām reglamentējošām prasībām. 
- Dokumentējiet visus līdzekļus un iegūstiet no klienta apstiprinājumu un parakstu. 

## <a name="fasttrack-go-live-assessment"></a>FastTrack darba sākšanas novērtējums

Klienti, kuri ir kvalificēti FastTrack un ir saistīti ar FastTrack risinājuma arhitektu, pabeigs darba sākšanas pārskatu ar Microsoft FastTrack. Papildinformāciju skatiet sadaļā  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). 

Aptuveni astoņas nedēļas pirms darba sākšanas FastTrack komanda lūgs jums aizpildīt [Darba sākšanas kontrolsarakstu](https://go.microsoft.com/fwlink/?linkid=2146013).

Projekta vadītājam vai galvenajam projekta dalībniekam ir jāaizpilda darba sākšanas kontrolsaraksts projekta pirmspalaišanas fāzē. Parasti kontrolsaraksts tiek aizpildīts četras līdz sešas nedēļas pirms ierosinātā darba sākšanas datuma, kad UAT ir pabeigta vai gandrīz pabeigta. 

Kad esat aizpildījis darba sākšanas kontrolsarakstu, nosūtiet to pa e-pastu savam FastTrack risinājuma arhitektam. Vienmēr e-pasta ziņojuma saņēmējos iekļaujiet galveno klienta ieinteresēto personu un īstenošanas partneri. 

Kad esat iesniedzis kontrolsarakstu, jūsu FastTrack risinājumu arhitekts pārskatīs projektu un sniegs novērtējumu, aprakstot iespējamos riskus, labāko praksi un ieteikumus veiksmīgai projekta palaišanai. Dažos gadījumos risinājuma arhitekts var uzsvērt riska faktorus un pieprasīt riska mazināšanas plānu. 

## <a name="see-also"></a>Skatiet arī

[Bieži uzdotie jautājumi par palaišanu](hr-admin-go-live-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]