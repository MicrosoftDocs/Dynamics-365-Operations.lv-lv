---
title: Izvēlieties starp Store Commerce un Cloud POS
description: Šajā tēmā skaidrotas galvenās atšķirības starp Store Commerce un Cloud POS un apraksta dažādus faktorus Dynamics 365 Commerce, kurus mazumtirgotājiem ir jāapsver, lai palīdzētu tiem izvēlēties pēc savas vajadzības.
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b62e1737bc9e3b9d9e25a7a88e693a9aece80776
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629294"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Izvēlieties starp Store Commerce un Cloud POS

[!include [banner](includes/banner.md)]

Šajā tēmā skaidrotas galvenās atšķirības starp Store Commerce un Cloud POS un apraksta dažādus faktorus Dynamics 365 Commerce, kurus mazumtirgotājiem ir jāapsver, lai palīdzētu tiem izvēlēties pēc savas vajadzības. Tā arī sniedz lietotājam papildu fonu, padomus un ieteikumus par faktoriem, kurus tie ir jāņem vērā, veicot izvietošanu Dynamics 365 Commerce. Pārskatot un izvietošanas procesā ievērojot šis norādījumus, ieviesēji var izvairīties no problēmām, kuras varētu ietekmēt lietotāju apmierinātību vai veiktspēju.

## <a name="insights"></a>Ieskati

Programmatūra Commerce sniedz plašu izvietošanas un topoloģijas opciju klāstu. Tāpēc mazumtirgotāji var izvēlēties komponentus un konfigurācijas, kas vislabāk atbilst viņu biznesa un tehnoloģiju prasībām. Viens ieviešanas aspekts, kas ir uzmanīgi jāpārdomā, ir platformas un formas faktora izvēle pārdošanas punkta (point of sale — POS) komponentam.

### <a name="pos-platform-and-form-factor-considerations"></a>POS platformas un formas faktora apsvērumi

Commerce atbalsta tālāk norādītās POS opcijas.

- Store Commerce priekš Microsoft Windows
- Store Commerce, kas paredzēts iOS un Android
- Cloud POS (CPOS), kas atbalsta un Microsoft Edge Procesora hroma pārlūkprogrammu
- Modern POS (MPOS) priekš Microsoft Windows (MPOS tiks nolietots 2023. gada oktobris.) 

Visos gadījumos POS (Store Commerce un CPOS) koplieto vienu un to pašu pamata programmas kodu. Tas ir svarīgi tālāk norādīto iemeslu dēļ.

- Lietotāja interfeiss (user interface — UI) ir saskaņots neatkarīgi no platformas vai formas faktora.
- Vairums funkcionālo iespēju ir vienādas neatkarīgi no platformas vai formas faktora. Taču pastāv dažas svarīgas atšķirības. Šīs atšķirības ir norādītas šajā tēmā.
- Katrā veikalā POS variācijas var apvienot un tās var darbināt vienlaicīgi. Piemēram, tā galvenajām kases sistēmās mazumtirgotājs var izmantot Store Commerce datoros, kuros darbojas operētājsistēma Windows. Taču mazumtirgotājs šos reģistrus var papildināt ar termināļiem, kas ir balstīti uz pārlūkprogrammu, vai mobilajām ierīcēm.
- Pielāgojumus un paplašinājumus var ērti izmantot dažādās platformās un formu faktoros. Tā kā pamata programmas kods tiek koplietots, vairums pielāgojumu var ieviest vienlaikus, nevis dažādos laikos.

### <a name="store-commerce-vs-cpos"></a>Store Commerce pret CPOS

Lai arī store Commerce un CPOS ir viens un tas pats, ir dažas svarīgas atšķirības, kas jums ir jāsaprot.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce ir darbvirsmas programma, kas ir instalēta un apkalpota ierīcē.

- **Windows** — programmā Store Commerce for Windows ir ietverts viss programmas kods Commerce Runtime () un aparatūras CRT stacija (HWS).
- **iOS/Android** — šajās platformās lietojumprogramma darbojas kā CPOS lietojumprogrammas koda resursdators. Citiem vārdiem sakot, programmas kods tiek nāk no CPOS servera, kas tiek viesots Commerce Scale Unit. Papildinformāciju skatiet šeit: [Commerce Store Scale Unit pārskats](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Tā kā CPOS darbojas pārlūkprogrammā, programma nav instalēta ierīcē. Tā vietā pārlūkprogramma piekļūst programmas kodam no CPOS servera. Tādēļ CPOS nevar tieši piekļūt POS aparatūrai vai strādāt bezsaistes stāvoklī.

### <a name="store-deployment-considerations"></a>Veikala izvietošanas apsvērumi

Papildus platformai un formas faktoram mazumtirgotājiem ir jāizvēlas arī izvietošanas opcija veikalā. Nākamajā tabulā ir parādītas katrai POS opcijai pieejamās konfigurācijas.

| POS programma            | Commerce Scale Unit | Pieejama bezsaistē | Lokālais HWS atbalsts |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce operētājsistēmai Windows | Mākonis vai RSSU       | Jā               | Jā               |
| Store Commerce priekš Android | Mākonis vai RSSU       | Nē                | Jā               |
| Store Commerce, kas paredzēts iOS     | Mākonis vai RSSU       | Nē                | Nē                |
| Cloud POS                  | Mākonis vai RSSU       | Nē                | Nē                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit ir komponents, kas vieso CRT. CRT satur visu POS izmantoto biznesa loģiku, un tas nodrošina piekļuvi kanāla datu bāzei. Atrodoties tiešsaistē, visi POS klienti veikalā izmanto Commerce Scale Unit. Commerce Scale Unit var izvietot mākoni vai veikalā.

#### <a name="offline-mode"></a>Bezsaistes režīms

Veikals Commerce for Windows atbalsta bezsaistes režīmu. Bezsaistes režīmā POS var turpināt apstrādāt pārdošanu pat tad, ja tas ir atvienots no Commerce Scale Unit. Kad savienojums ir atjaunots, to var sinhronizēt ar kanāla datu bāzi. Store Commerce izmanto pati savu iegulto datu avota CRT instanci un īslaicīgi lieto savu lokālo datu avotu (bezsaistes SQL Server datu bāze). Papildinformāciju par bezsaistes funkcionalitāti skatiet šeit: [POS bezsaistes funkcionalitāte](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>POS perifērijas/aparatūras apsvērumi

Mazumtirgotājiem ir jāņem vērā arī veids, kā POS piekļūs ierīcēm un perifērijas ierīcēm, piemēram, printeriem, kases aparātiem un maksājumu termināļiem. Aparatūras stacijas var būt speciālas viena POS reģistra stacijas vai veikala reģistru koplietotas stacijas.

| POS programma            | Vietējais HWS OPOS | Tīkla perifērās ierīces | Koplietots HWS atbalsts |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce operētājsistēmai Windows | Jā            | Jā                 | Jā                |
| Store Commerce priekš Android | Nē             | Jā                 | Jā                |
| Store Commerce, kas paredzēts iOS     | Nē             | Nē                  | Jā                |
| Cloud POS                  | Nē             | Nē                  | Jā                |

Papildinformāciju par aparatūras stacijām skatiet šeit: [Retail aparatūras stacijas konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Ieviešanas apsvērumi

Plānojot POS implementēšanu savos veikalos, ir jāapsver tālāk norādītā informācija.

- **Funkcionālās prasības** — pamata biznesa procesi un iespējas ir vienādi neatkarīgi no platformas, formu faktora vai izvietošanas topoloģijas. Tādēļ vairumam mazumtirgotāju nav jāņem vērā funkcionālās prasības, kad viņi plāno savu ieviešanu.
- **Savienojamība** — tīkla pieejamība (plaša apgabala tīkls (wide area network — \[WAN\]) un lokālais tīkls (local area network — \[LAN\])) ir būtisks faktors, un tas ir rūpīgi jāapsver. Visas priekšrocības, ko nulles patēriņa, mākonī viesots risinājums rada attiecībā uz izmaksām un vienkāršību, tiek zaudētas, ja sistēma nav pieejama komercdarbībai svarīgu procesu izpildei.

    Izņemot gadījumus, kad attiecīgās ierīces savienojamība ir ļoti uzticama un noturīga, vai gadījumus, kad mazumtirgotājam ir pieļaujama zināma dīkstāve, iesakām vienu no tālāk norādītajām opcijām.

    - Lietojiet programmu Store Commerce operētājsistēmā Windows un iespējojiet bezsaistes režīmu.
    - Izvietojiet lokālo Commerce Scale Unit.

    Abas šīs opcijas nav savstarpēji izslēdzošas. Lai iegūtu visuzticamāko topoloģiju, mazumtirgotāji var izvietot lokālu RSSU, mazinot atkarību no interneta savienojamības vai Azure pieejamības, un viņi var izvietot arī POS reģistrus, kur ir iespējots bezsaistes režīms, ja rodas problēma ar lokālo serveri vai tīklu.

- **Aparatūras ierīces/perifērijas ierīces** — svarīgs Retail POS sistēmas aspekts ir tā pieejamība POS perifērijas ierīču lietošanai, piemēram, printeriem, kases aparātiem un maksājumu termināļiem. Lai gan visas pieejamās POS opcijas var izmantot perifērijas ierīces, tikai store Commerce for Windows atbalsta tās tieši. Visām pārējām programmām ir nepieciešama viena aparatūras stacija vai vairākas. Lai gan šī pieeja sniedz papildu elastību, ir nepieciešams izvietot, konfigurēt un apkalpot papildu komponentus.
- **Sistēmas prasības** — dažādām POS programmām ir atšķirīgas sistēmas prasības. Pirms izvēles pieņemšanas noteikti pārbaudiet visjaunāko informāciju. Piemēram, tā kā CPOS darbojas pārlūkprogrammā, tas atbalsta plašāku operētājsistēmu klāstu. Papildinformāciju par sistēmas prasībām skatiet šeit: [Sistēmas prasības mākoņa izvietojumiem](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Izvietošana un apkalpošana** — izvietošanas sarežģītība un apkalpošanas prasības var atšķirties atkarībā no programmas un izvietošanas izvēlēm. Piemēram, mākonī viesotam CPOS izvietojumam nav nepieciešams veikt instalēšanu un atjaunināšanu katru ierīcē. Tāpēc šī pieeja ievērojami samazina sarežģītību un izmaksas. Tomēr, ja izvietojat Store Commerce katrā kases sistēmā un iespējojat bezsaistes režīmu, kā arī izvietojat koplietotas aparatūras stacijas, ir ļoti jāpalielina pārvaldāmo galapunktu skaits.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
