---
title: Elektronisko pārskatu komponenti
description: Šajā tēmā aprakstīti Elektronisko pārskatu (ER) komponenti.
author: nselin
ms.date: 09/28/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.topic: overview
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a24aa52c805722c20045b6227ceac0103cfbe6b
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324039"
---
# <a name="electronic-reporting-components"></a>Elektronisko pārskatu komponenti

[!include [banner](../includes/banner.md)]

Elektroniskie pārskati (ER) atbalsta šādus komponentu tipus:

- Datu modelis
- Modeļa kartēšana
- Formāts
- Metadati

## <a name="data-model-component"></a>Datu modeļa komponents

Datu modeļa komponents ir abstrakts datu struktūras atainojums. Tas tiek izmantots kāda specifiska biznesa domēna apgabala aprakstīšanai pietiekami detalizēti, lai nodrošinātu šī domēna pārskatu veidošanas prasības. Datu modeļa komponents sastāv no šādām daļām:

- **Datu modelis** - domēnam raksturīgo biznesa elementu kopa, un hierarhiski strukturēta šo elementu attiecību definīcija.
- **Modeļa kartēšana** - atlasīti programmas datu avoti tiek saistīti ar atsevišķiem datu modeļa elementiem, kuri izpildes laikā norāda datu plūsmu un kārtulas biznesa datu aizpildīšanai datu modeļa komponentā.

Datu modeļa biznesa elements tiek attēlots kā konteiners vai ieraksts. Biznesa vienuma rekvizīti tiek attēloti kā datu elementi vai lauki. Katram datu vienumam ir unikāls nosaukums, etiķete, apraksts un vērtība. Katra datu vienuma vērtība var būt izveidota tā, lai tā tiktu atpazīta kā virkne, vesels skaitlis, reāls skaitlis, datums, uzskaitījums vai Būla vērtība. Turklāt datu krājums var būt cits ieraksts kādā ierakstu sarakstā.

Viens datu modeļa komponents var ietvert vairākas domēnam specifisko uzņēmējdarbības elementu hierarhijas. Tāpat tas var ietvert modeļa kartējumus, kas izpildes laikā atbalsta no pārskata atkarīgu datu plūsmu. Hierarhijas tiek atšķirtas pēc viena ieraksta, kas tika atlasīts kā modeļa kartēšanas sakne. Piemēram, maksājumu domēna apgabala datu modelis varētu atbalstīt šādus kartējumus:


- Uzņēmums \> kreditors \> parādu kreditoriem domēna maksājumu transakcijas
- Debitors \> uzņēmums \> debitoru parādu domēna maksājumu transakcijas

Biznesa entītijas, piemēram, uzņēmums un maksājumu transakcijas, tiek izveidoti vienreiz. Ja nepieciešams, dažādos kartējumus var izmantot atkārtoti.

## <a name="model-mapping-component"></a>Modeļa kartēšanas komponents

Modeļa kartēšana saista programmas datu avotus ar atsevišķiem datu modeļa elementiem, kuri izpildes laikā norāda datu plūsmu un kārtulas biznesa datu aizpildīšanai datu modeļa komponentā.

Modeļa kartējumam, kas atbalsta izejošos elektroniskos dokumentus, ir tālāk norādītās iespējas.

- Kā datu avotus kādam datu modelim tā var izmantot dažādus datu tipus. Šo datu elementu klāstā ietilpst tabulas, datu elementi, metodes un uzskaitījums.
- Tā atbalsta lietotāja ievades parametrus, kurus var definēt kā datu modeļa datu avotus, kur izpildes laikā ir jānorāda kādi dati.
- Tas atbalsta datu pārveidošanu nepieciešamajās grupās. Turklāt tas sniedz iespēju filtrēt, kārtot un summēt datus, kā arī pievienot loģiski aprēķinātos laukus, kuri ir izveidoti, izmantojot formulas, kas līdzinās Microsoft Excel formulām. Papildinformāciju skatiet tēmā [Formulas veidotājs elektronisko pārskatu (EP) veidošanā](general-electronic-reporting-formula-designer.md).

Modeļa kartējumam, kas atbalsta ienākošos elektroniskos dokumentus, ir tālāk norādītās iespējas.

- Tas var kā mērķus izmantot dažādus atjaunināmos datu elementus. Šo datu elementu klāstā ietilpst tabulas, datu elementi un skati. Datus var atjaunināt, izmantojot datus no ienākošiem elektroniskajiem dokumentiem. Vienā modeļa kartēšanā var izmantot vairākus mērķus.
- Tā atbalsta lietotāja ievades parametrus, kurus var definēt kā datu modeļa datu avotus, kur izpildes laikā ir jānorāda kādi dati.

Datu modeļa komponents ir paredzēts katram biznesa domēnam, ko izmanto kā unificētu datu avotu pārskata veidošanai. Unificētais datu avots izolētu pārskatus no datu avotu fiziskās ieviešanas. Tas pārstāv domēnam specifiskās biznesa koncepcijas un funkcionalitātes tādā formā, kas pārskata formāta sākotnējo noformējumu un turpmāko uzturēšanu padara efektīvāku.

## <a name="format-component"></a>Komponenta formāts

### <a name="format-components-for-outgoing-electronic-documents"></a>Formāta komponenti izejošiem elektroniskajiem dokumentiem

Formāta komponents ir atskaišu veidošanas izvades shēma, kas tiks ģenerēta izpildes laikā. Shēma sastāv no šādiem elementiem:

- Formāts, kas nosaka izpildes laikā ģenerētā izejošā elektroniskā dokumenta struktūru un saturu.
- Datu avoti kā lietotāja ievades parametru kopa un domēnam specifisku datu modelis, kas izmanto atlasīto modeļa kartēšanu.
- Formāta kartēšana kā formāta datu avotu saistījumu kopa, kuriem ir atsevišķi formāta elementi, kas izpildes laikā norāda datu plūsmu un kārtulas formāta izvades ģenerēšanai.
- Formāta validēšana kā konfigurējamu kārtulu kopa, kas izpildes laikā regulē pārskata ģenerēšanu atkarībā no izpildes konteksta. Var būt, piemēram, kārtula, kas aptur kreditoru maksājumu izvades ģenerēšanu un parāda izņēmumu, ja trūkst atlasītā kreditora specifisku atribūtu, piemēram, bankas konta numura.

Formāta komponents atbalsta tālāk aprakstītās funkcijas.

- Pārskatu izveides izvade, izveidojot atsevišķus dažādu formātu, piemēram, teksta, XML, Microsoft Word dokumenta vai darblapas, failus
- Vairāku failu izveidošana atsevišķi un šo failu iekapsulēšana .zip failos

Formāta komponents jums ļauj pievienot noteiktus failus, kurus var izmantot pārskatu izvadē tālāk aprakstītajos veidos.

- Excel darbgrāmatas, kas ietver darblapu, kuru var izmantot kā veidni izvadei OPENXML darblapas formātā
- Word faili, kuros ir ietverts dokumentu, kuru var izmantot kā veidni izvadei Microsoft Word dokumenta formātā
- Citi faili, kurus var iekļaut formāta izvadē kā iepriekš definētus failus

Nākamajā attēlā ir parādīts, kā šiem formātiem notiek datu plūsmas.

[![Datu plūsma ienākošo formātu komponentiem.](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Lai palaistu atsevišķu ER formāta konfigurāciju un importētu datus no ienākoša elektroniskā dokumenta, ir nepieciešams identificēt formāta konfigurācijas vēlamo kartējumu un modeļa kartējuma integrācijas punktu. Vienu un to pašu modeļa kartējumu un mērķus varat izmantot kopā ar dažādiem formātiem dažāda tipa ienākošajiem dokumentiem.

## <a name="component-versioning"></a>Komponenta versiju izveide

ER komponentiem tiek atbalstīta versiju izveide. ER komponentu izmaiņu pārvaldīšanai tiek sniegta tālāk aprakstītā darbplūsma.

1. Sākotnēji izveidotā versija tiek atzīmēta kā versija **Melnraksts**. Šo versiju var rediģēt, un tā ir pieejama testu izpildīšanai.
2. Versiju **Melnraksts** var pārveidot par versiju **Pabeigts**. Šo versiju var izmantot vietējos atskaišu procesos.
3. Versiju **Pabeigts** var pārveidot par versiju **Koplietots**. Šī versija tiek publicēta Microsoft Dynamics Lifecycle Services (LCS), un to var izmantot globālu pārskatu izveides procesos.
4. Versiju **Koplietots** var pārveidot par versiju **Pārtraukts**. Šo versiju var dzēst.

Versijas, kuru statuss ir **Pabeigts** vai **Koplietots**, ir pieejamas citai datu apmaiņai. Komponentam, kam ir šie statusi, var izpildīt tālāk norādītās darbības.

- Komponentu var serializēt XML formātā un eksportēt kā XML formāta failu.
- Komponentu var atkārtoti serializēt no XML faila un importēt programmā kā jaunu ER komponenta versiju.

## <a name="component-date-effectivity"></a>Komponenta spēkā stāšanās datums

ER komponentu versijas ir ar spēkā stāšanās datumu. ER komponentam varat iestatīt datumu "Spēkā no", lai norādītu datumu, kad šis komponents stājas spēkā pārskatu veidošanas procesiem. Lai definētu, vai komponents ir derīgs izpildei, tiek izmantots programmas sesijas datums. Ja noteiktam datumam ir derīgas vairākas versijas, tad atskaišu veidošanas procesiem tiek izmantota jaunākā versija.

## <a name="component-access"></a>Komponenta piekļuve

Piekļuve ER formāta komponentiem ir atkarīga no iestatījuma Starptautiskās standartizācijas organizācijas (ISO) valsts/reģiona kodam. Ja šis iestatījums atlasītajai formāta konfigurācijas versijai ir atstāts tukšs, formāta komponentam izpildes laikā var piekļūt no jebkura uzņēmuma. Ja šis iestatījums satur ISO valsts/reģiona kodus, formāta komponents ir pieejams tikai no uzņēmumiem, kuru primārā adrese ir definēta vienam no formāta komponenta ISO valsts/reģiona kodiem.

Datu formāta komponenta dažādām versijām var būt dažādi iestatījumi ISO valsts/reģiona kodiem.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

