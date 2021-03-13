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
ms.openlocfilehash: b4196532be8ad40bacb8d614c6b0c86215b00bdb
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113365"
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

Svarīgs atskaites punkts katrā īstenošanas projektā ir pārslēgšana uz ražošanas vidi. Darbības pabeigšanas procesam ir divas tālāk minētās daļas. 

- Paveikt faktisko darbu, piemēram, atbilstību analīzi vai lietotāju akceptēšanas testēšanu (UAT). 
- Atzīmēt atbilstošo darbību LCS metodoloģijā kā pabeigtu. 

Laba prakse ir pabeigt darbības metodoloģijā, virzoties uz priekšu ieviešanā. Negaidiet līdz pēdējai minūtei. Klienta interesēs ir stingra ieviešana. 

## <a name="uat-for-your-solution"></a>UAT jūsu risinājumam

UAT fāzes laikā ieviešanas projektā smilškastes vidē ir jāpārbauda visi jūsu ieviestie biznesa procesi un visi veiktie pielāgojumi. Lai palīdzētu nodrošināt sekmīgu darba sākšanu, pabeidzot UAT fāzi, ņemiet vērā tālāk minēto. 

- Iesakām, lai jūsu UAT process sāktos ar iztīrītu un jaunu vidi, kur dati no jūsu GOLD konfigurācijas tiek kopēti vidē pirms UAT procesa sākšanas. Iesakām izmantot ražošanas vidi kā jūsu GOLD vidi līdz brīdim, kad vide kļūst par ražošanas vidi.
- Testa gadījumi aptver visu prasību jomu. 
- Testējiet, izmantojot migrētos datus. Šajos datos jāiekļauj pamatdati, piemēram, darbinieki, darbi un amati. Iekļaujiet arī sākuma bilances, piemēram, atvaļinājumu un prombūtnes uzkrājumus. Visbeidzot iekļaujiet atvērtās transakcijas, piemēram, pašreizējās atvieglojumu reģistrācijas. Pabeidziet testēšanu ar visiem datu veidiem pat tad, ja datu kopa nav pabeigta. 
- Testējiet, izmantojot pareizās drošības lomas (noklusējuma lomas un pielāgotās lomas), kas piešķirtas lietotājiem. 
- Pārliecinieties, vai risinājums atbilst visām uzņēmumas un nozarei specifiskām reglamentējošām prasībām. 
- Dokumentējiet visus līdzekļus un iegūstiet no klienta apstiprinājumu un parakstu. 

## <a name="mock-go-live"></a>Pārbaudes objekta darba sākšana

Pirms darbības veikšanas ir jāveic pārbaudes objekta darba sākšana, lai pārbaudītu darbības, kas jāveic pārslēgšanai no mantojuma sistēmām uz jauno sistēmu. Veiciet savu pārbaudes objekta darba sākšana smilškastes vidē un ietveriet visas darbības pārslēgšanas plānā.

- Iesakām izmantot ražošanas vidi kā GOLD konfigurācijas vidi līdz pat darba sākšanai.
- Nodrošiniet, ka ir ieviests spēcīgs pārvaldības procesā, lai aizsargātu ražošanas vidi no nejaušām darbībām vai atjauninājumiem pirms darba sākšanas.
- Kad esat gatavs veikt UAT vai sākt pārbaudāmā objekta darbu, atsvaidziniet smilškastes vidi no ražošanas vides. Papildinformāciju skatiet sadaļā [Instances kopēšana](hr-admin-setup-copy-instance.md).
- Pārbaudiet katru pārslēgšanas plāna darbību smilškastes vidē un pēc tam pārbaudiet smilškastes vidi, veicot vietas pārbaudes vai veicot pārbaudes no UAT skriptiem vidē.
  - Testos jāietver visa datu migrācija, tostarp transformācijas, kas nepieciešamas darba sākšanai.
  - Šajā procesā ir jāietver kādā no mantojuma sistēmām veiktās prakses samazināšana.
  - Noteikti ietveriet visas integrācijas pārslēgšanas darbības vai ārējās sistēmas darbības jūsu pārbaudāmā objekta pārslēgšanā.
- Ja rodas problēmas pārbaudāmā objekta pārslēgšanas laikā, var būt nepieciešama otra pārbaudāmā objekta pārslēgšana. Tāpēc ir ieteicams savā projekta plānā plānot divas pārbaudāmā objekta pārslēgšanas.

## <a name="fasttrack-go-live-assessment"></a>FastTrack darba sākšanas novērtējums

Klienti, kuri ir kvalificēti FastTrack un ir saistīti ar FastTrack risinājuma arhitektu, pabeigs darba sākšanas pārskatu ar Microsoft FastTrack. Papildinformāciju skatiet sadaļā  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). 

Aptuveni astoņas nedēļas pirms darba sākšanas FastTrack komanda lūgs jums aizpildīt [Darba sākšanas kontrolsarakstu](https://go.microsoft.com/fwlink/?linkid=2146013).

Projekta vadītājam vai galvenajam projekta dalībniekam ir jāaizpilda darba sākšanas kontrolsaraksts projekta pirmspalaišanas fāzē. Parasti kontrolsaraksts tiek aizpildīts četras līdz sešas nedēļas pirms ierosinātā darba sākšanas datuma, kad UAT ir pabeigta vai gandrīz pabeigta. 

Kad esat aizpildījis darba sākšanas kontrolsarakstu, nosūtiet to pa e-pastu savam FastTrack risinājuma arhitektam. Vienmēr e-pasta ziņojuma saņēmējos iekļaujiet galveno klienta ieinteresēto personu un īstenošanas partneri. 

Kad esat iesniedzis kontrolsarakstu, jūsu FastTrack risinājumu arhitekts pārskatīs projektu un sniegs novērtējumu, aprakstot iespējamos riskus, labāko praksi un ieteikumus veiksmīgai projekta palaišanai. Dažos gadījumos risinājuma arhitekts var uzsvērt riska faktorus un pieprasīt riska mazināšanas plānu. 

## <a name="see-also"></a>Skatiet arī

[Bieži uzdotie jautājumi par palaišanu](hr-admin-go-live-faq.md)
