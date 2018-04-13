---
title: "Izvēle starp Modern POS un Cloud POS"
description: "Šajā tēmā ir izskaidrotas galvenās atšķirības starp Retail Modern POS un Cloud POS. Tajā ir aprakstīti arī dažādi faktori, kas ir jāņem vērā mazumtirgotājiem, kuri ievieš Microsoft Dynamics 365 for Retail, lai izdarītu savām prasībām visatbilstošāko izvēli."
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7eb15f9f73f4773d98160e1b0ec5ce74c159cdea
ms.contentlocale: lv-lv
ms.lasthandoff: 02/07/2018

---

# <a name="choose-between-modern-pos-and-cloud-pos"></a>Izvēle starp Modern POS un Cloud POS

[!INCLUDE [banner](includes/banner.md)]

Šajā tēma ieviesējiem tiek sniegta papildu fona informācija, padomi un norādījumi par faktoriem, kas ir jāņem vērā, izvietojot programmatūru Microsoft Dynamics 365 for Retail. Pārskatot un izvietošanas procesā ievērojot šis norādījumus, ieviesēji var izvairīties no problēmām, kuras varētu ietekmēt lietotāju apmierinātību vai veiktspēju.

## <a name="insights"></a>Insights
Programmatūra Retail sniedz plašu izvietošanas un topoloģijas opciju klāstu. Tāpēc mazumtirgotāji var izvēlēties komponentus un konfigurācijas, kas vislabāk atbilst viņu biznesa un tehnoloģiju prasībām. Viens ieviešanas aspekts, kas ir uzmanīgi jāpārdomā, ir platformas un formas faktora izvēle pārdošanas punkta (point of sale — POS) komponentam.

### <a name="pos-platform-and-form-factor-considerations"></a>POS platformas un formas faktora apsvērumi
Retail atbalsta tālāk norādītās POS opcijas.

- Retail Modern POS (MPOS) operētājsistēmai Microsoft Windows
- MPOS tālrunim Microsoft Windows Phone
- MPOS ierīcei Apple iPad vai Google Android planšetdatoram
- Cloud POS (CPOS), kas atbalsta pārlūkprogrammu Microsoft Edge, Internet Explorer, un Google Chrome

Visos gadījumos POS (MPOS un CPOS) koplieto to pašu pamata programmas kodu. Tas ir svarīgi tālāk norādīto iemeslu dēļ.

- Lietotāja interfeiss (user interface — UI) ir saskaņots neatkarīgi no platformas vai formas faktora.
- Vairums funkcionālo iespēju ir vienādas neatkarīgi no platformas vai formas faktora. Taču pastāv dažas svarīgas atšķirības. Šīs atšķirības ir norādītas šajā tēmā.
- Katrā konkrētajā veikalā POS variācijas var kombinēt un var darbināt vienlaikus. Piemēram, galvenajiem reģistriem mazumtirgotājs var izmantot MPOS datoros, kur darbojas operētājsistēma Windows. Taču mazumtirgotājs šos reģistrus var papildināt ar termināļiem, kas ir balstīti uz pārlūkprogrammu, vai mobilajām ierīcēm.
- Pielāgojumus un paplašinājumus var ērti izmantot dažādās platformās un formu faktoros. Tā kā pamata programmas kods tiek koplietots, vairums pielāgojumu var ieviest vienlaikus, nevis dažādos laikos.

### <a name="mpos-vs-cpos"></a>MPOS salīdzinājums ar CPOS
Lai gan MPOS un CPOS lielā mērā ir vienādi, pastāv dažas būtiskas atšķirības, kas jums ir jāsaprot.

#### <a name="mpos"></a>MPOS

MPOS operētājsistēmā Windows, iOS vai Android ir programma, kas tiek iepakota, instalēta un apkalpota attiecīgajā ierīcē.

- **Windows** — programma MPOS for Windows ietver visu programmas kodu, kā arī iegulto Commerce Runtime (CRT). 
- **iOS/Android** — šajās platformās programma darbojas kā resursdators CPOS programmas kodam. Citiem vārdiem sakot — programmas kods tiek ņemts no CPOS servera pakalpojumā Microsoft Azure vai Retail Store Scale Unit (RSSU). Papildinformāciju skatiet šeit: [Retail Store Scale Unit pārskats](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

Tā kā CPOS darbojas pārlūkprogrammā, programma nav instalēta ierīcē. Tā vietā pārlūkprogramma piekļūst programmas kodam no CPOS servera. Tādēļ CPOS nevar tieši piekļūt POS aparatūrai vai strādāt bezsaistes stāvoklī.

### <a name="store-deployment-considerations"></a>Veikala izvietošanas apsvērumi
Papildus platformai un formas faktoram mazumtirgotājiem ir jāizvēlas arī izvietošanas opcija veikalā. Nākamajā tabulā ir parādītas katrai POS opcijai pieejamās konfigurācijas.

| POS programma         | Retail serveris | Pieejama bezsaistē |
|-------------------------|---------------|-------------------|
| MPOS for Windows        | Mākonis vai RSSU | Jā               |
| MPOS for iOS vai Android | Mākonis vai RSSU | Nē                |
| Cloud POS               | Mākonis vai RSSU | Nē                |

#### <a name="retail-server"></a>Retail serveris

Retail serveris ir komponents, kas vieso CRT. CRT satur visu POS izmantoto biznesa loģiku, un tas nodrošina piekļuvi kanāla datu bāzei. Atrodoties tiešsaistē, visi POS klienti veikalā izmanto Retail serveri. Retail serveri var izvietot mākoni vai veikalā (RSSU).

#### <a name="offline-mode"></a>Bezsaistes režīms

Programma MPOS for Windows atbalsta bezsaistes režīmu. Bezsaistes režīmā POS var turpināt apstrādāt pārdošanu pat tad, ja tas ir atvienots no Retail servera. Kad savienojums ir atjaunots, to var sinhronizēt ar kanāla datu bāzi. MPOS izmanto pats savu iegulto CRT instanci un īslaicīgi izmanto savu lokālo datu avotu (bezsaistes SQL Server datu bāzi). Papildinformāciju par bezsaistes funkcionalitāti skatiet šeit: [POS bezsaistes funkcionalitāte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-offline-functionality).

### <a name="pos-peripheralhardware-considerations"></a>POS perifērijas/aparatūras apsvērumi
Mazumtirgotājiem ir jāņem vērā arī veids, kā POS piekļūs ierīcēm un perifērijas ierīcēm, piemēram, printeriem, kases aparātiem un maksājumu termināļiem. Tikai programma MPOS for Windows atbalsta tiešu saziņu ar šīm ierīcēm. Programmai MPOS for Windows Phone, iOS vai Android, kā arī programmai Cloud POS ir nepieciešama aparatūras stacija, lai piekļūtu šīm ierīcēm. Aparatūras stacijas var būt speciālas viena POS reģistra stacijas vai veikala reģistru koplietotas stacijas. Papildinformāciju par aparatūras stacijām skatiet šeit: [Retail aparatūras stacijas konfigurēšana un instalēšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Ieviešanas apsvērumi
Plānojot POS implementēšanu savos mazumtirdzniecības veikalos, ir jāapsver tālāk norādītā informācija.

- **Funkcionālās prasības** — pamata biznesa procesi un iespējas ir vienādi neatkarīgi no platformas, formu faktora vai izvietošanas topoloģijas. Tādēļ vairumam mazumtirgotāju nav jāņem vērā funkcionālās prasības, kad viņi plāno savu ieviešanu.
- **Savienojamība** — tīkla pieejamība (plaša apgabala tīkls (wide area network — \[WAN\]) un lokālais tīkls (local area network — \[LAN\])) ir būtisks faktors, un tas ir rūpīgi jāapsver. Visas priekšrocības, ko nulles patēriņa, mākonī viesots risinājums rada attiecībā uz izmaksām un vienkāršību, tiek zaudētas, ja sistēma nav pieejama komercdarbībai svarīgu procesu izpildei.

    Izņemot gadījumus, kad attiecīgās ierīces savienojamība ir ļoti uzticama un noturīga, vai gadījumus, kad mazumtirgotājam ir pieļaujama zināma dīkstāve, iesakām vienu no tālāk norādītajām opcijām.

  - Izmantojiet MPOS operētājsistēmā Windows un iespējojiet bezsaistes režīmu.
  - Izvietojiet lokālu RSSU.

    Abas šīs opcijas nav savstarpēji izslēdzošas. Lai iegūtu visuzticamāko topoloģiju, mazumtirgotāji var izvietot lokālu RSSU, mazinot atkarību no interneta savienojamības vai Azure pieejamības, un viņi var izvietot arī POS reģistrus, kur ir iespējots bezsaistes režīms, ja rodas problēma ar lokālo serveri vai tīklu.

- **Aparatūras ierīces/perifērijas ierīces** — svarīgs Retail POS sistēmas aspekts ir tā pieejamība POS perifērijas ierīču lietošanai, piemēram, printeriem, kases aparātiem un maksājumu termināļiem. Lai gan visas pieejamās POS opcijas var izmantot perifērijas ierīces, tiešā veidā tās atbalsta tikai programma MPOS for Windows. Visām pārējām programmām ir nepieciešama viena aparatūras stacija vai vairākas. Lai gan šī pieeja sniedz papildu elastību, ir nepieciešams izvietot, konfigurēt un apkalpot papildu komponentus.
- **Sistēmas prasības** — dažādām POS programmām ir atšķirīgas sistēmas prasības. Pirms izvēles pieņemšanas noteikti pārbaudiet visjaunāko informāciju. Piemēram, tā kā CPOS darbojas pārlūkprogrammā, tas atbalsta plašāku operētājsistēmu klāstu. Papildinformāciju par sistēmas prasībām skatiet šeit: [Sistēmas prasības mākoņa izvietojumiem](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Izvietošana un apkalpošana** — izvietošanas sarežģītība un apkalpošanas prasības var atšķirties atkarībā no programmas un izvietošanas izvēlēm. Piemēram, mākonī viesotam CPOS izvietojumam nav nepieciešams veikt instalēšanu un atjaunināšanu katru ierīcē. Tāpēc šī pieeja ievērojami samazina sarežģītību un izmaksas. Taču, ja MPOS izvietojat katrā reģistrā un iespējojat bezsaistes režīmu, un izvietot arī koplietojamas aparatūras stacijas, jūs ievērojami palielināt pārvaldāmo galapunktu skaitu.

