---
title: Lietojuma pārvaldības informācijas panelis
description: Šajā tēmā skaidrots, kā izmantot lietojuma pārvaldības informācijas paneli, lai pārraudzītu elektronisko rēķinu izrakstīšanas pakalpojuma lietošanu un saglabātu to atbilstību.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 35b50c8cb5c6ef72f466a4fb10c7af0e53afc3db5d1ef9e2b23d6049e24a70c3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776478"
---
# <a name="usage-management-dashboard"></a>Lietojuma pārvaldības informācijas panelis

[!include [banner](../includes/banner.md)]

**Lietojuma pārvaldības** informācijas panelis palīdz pārraudzīt elektronisko rēķinu izrakstīšanas pakalpojuma lietošanu un tādēļ palīdz uzņēmumam saglabāt atbilstību attiecībā uz tā ikmēneša lietojumu. Atbilstību nosaka, aprēķinot iesniegšanas apjomu un salīdzinot to ar iesniegšanas iegādāto apjomu, lai identificētu jebkādas iegādātā apjoma un izmantotā apjoma novirzes.

Informācijas panelis ietver šādus indikatorus:

- Viens izmaksu indikators, ko var izmantot, lai pārraudzītu patēriņu licencēšanas atbilstības nolūkiem:

    - Lietojums mēnesī (eksports)

- Trīs darbību indikatori, ko var izmantot elektronisko rēķinu izrakstīšanas pakalpojuma lietošanas pārvaldības nolūkiem:

    - Lietojums pēc līdzekļa
    - Lietojums pēc vides
    - Lietojums mēnesī (imports)

## <a name="measurement-scope"></a>Mērījuma tvērums

- Mērvienība: 

    **Lietojuma pārvaldības** informācijas panelis uzskaita biznesa dokumentu un importēto elektronisko rēķinu iesniegšanu.

- Organizācija: 

    Uzskaite tiek summēta ar jūsu uzņēmuma nomnieka ID neatkarīgi no Microsoft Dynamics 365 Finance vai Dynamics 365 Supply Chain Management instanču skaita vai juridisko personu skaita, kur elektronisko rēķinu izrakstīšanas pakalpojums ir iespējots.


## <a name="indicator-usage-per-month-export"></a>Indikators: lietojums mēnesī (eksports)

Šis indikators sniedz detalizētu informāciju par elektroniskajiem rēķiniem, ko jūsu uzņēmums izsniedz noteiktā periodā.

### <a name="scope"></a>Sfēra
- Biznesa dokumentu skaits, kas ir iesniegti no programmas Finance un Supply Chain Management elektronisko rēķinu izrakstīšanas pakalpojumam, neatkarīgi no rindu skaita, ko šie biznesa dokumenti ietver.
- Elektronisko rēķinu izrakstīšanas pakalpojumā iesniegto veiksmīgi apstrādāto biznesa dokumentu skaits. Dokuments tiek uzskatīts par veiksmīgi apstrādātu, kad tiek pabeigta līdzekļu iestatījumā definēto darbību plūsma.

> [!NOTE]
> Kad elektroniskais rēķins tiek iesniegts ārējam tīmekļa pakalpojumam, uzskaite nav atkarīga no tīmekļa pakalpojumu apstrādes rezultātiem (pieņemts, noraidīts vai shēmas validācijas kļūda). Ja tīmekļa pakalpojums saņēmis un atbildējis uz pieprasījumu no elektronisko rēķinu izrakstīšanas pakalpojuma, tad iesniegšana tiek uzskatīta par derīgu uzskaiti.

- **Izņēmums.** Biznesa dokumenti netiek uzskaitīti, ja tie no Finance un Supply Chain Management tiek atkārtoti iesniegti elektronisko rēķinu izrakstīšanas pakalpojumam, piemēram, scenārijos, kuros nepieciešams atkārtoti iesniegt vienu un to pašu biznesa dokumentu, lai mainītu elektroniskā rēķina statusu. Piemēram, Brazīlijas elektroniskā rēķina (finanšu dokumenta) izsniegšana tiek uzskaitīta kā derīga, bet nav uzskaitīts atcelšanas pieprasījums.


### <a name="calculation"></a>Aprēķins

Bilances aprēķins tiek aprēķināts šādi:

Bilance = Bezmaksas + Nopirkts – Izmantots

Kur:

- Bezmaksas:
  
    Biznesa dokumentu bezmaksas apjoms, ko debitors var iesniegt katru mēnesi. Tajā ir ietverta pakete ar 100 biznesa dokumentiem, ko var iesniegt elektronisko rēķinu izrakstīšanas pakalpojumā. Bezmaksas apjoms nav kumulatīvs, un neviena atlikusī bilance netiek pārnesta uz nākamo periodu.
  
- Nopirkts:
  
    Pakete ar 1 000 biznesa dokumentiem, ko var iesniegt elektronisko rēķinu izrakstīšanas pakalpojumā. Šī pakete jūsu uzņēmumam ir jāiegādājas katru mēnesi. Nopirktais apjoms nav kumulatīvs, un neviena atlikusī bilance netiek pārnesta uz nākamo periodu.
  
- Izmantots: 

    Biznesa dokumentu iesniegumu skaits elektroniskajā rēķinu izrakstīšanas pakalpojumā atbilstoši noteiktiem kritērijiem.
   
> [!IMPORTANT]
> Ja jūsu uzņēmums plāno pārsniegt 100 bezmaksas iesniegumu ikmēneša apjomu, iegādājieties maksimālo apjomu, lai nodrošinātu atbilstību Microsoft licencēšanas politikai attiecībā uz elektronisko rēķinu izrakstīšanas pakalpojumu.
>
> Pašlaik nopirktais apjoms ir jāievada manuāli atbilstoši iegādes datumam kā vairākas paketes ar 1000 iesniegumiem.

## <a name="indicator-usage-by-feature"></a>Indikators: lietojums pēc līdzekļa

Šis indikators rāda elektroniskā rēķina izrakstīšanas līdzekļa izmantošanu elektronisko rēķinu izsniegšanai noteiktā periodā.

- Aprēķins:
  
    Izmantots = skaits, cik reizes tika izmantots katrs elektronisko rēķinu izrakstīšanas līdzeklis, iesniedzot biznesa dokumentus elektronisko rēķinu izrakstīšanas pakalpojumam.

## <a name="indicator-usage-by-environment"></a>Indikators: lietojums pēc vides

Šis indikators rāda elektronisko rēķinu izrakstīšanas pakalpojumu vides izmantošanu noteiktā periodā.

- Aprēķins:
    
    Izmantots = skaits, cik reizes tika izmantota katra elektronisko rēķinu izrakstīšanas pakalpojuma vide, iesniedzot biznesa dokumentus elektronisko rēķinu izrakstīšanas pakalpojumam.

## <a name="indicator-usage-per-month-import"></a>Indikators: lietojums mēnesī (imports)

Šis indikators rāda elektronisko rēķinu importēšanas apjomu programmā Finance un Supply Chain Management noteiktā periodā, izmantojot elektronisko rēķinu izrakstīšanas pakalpojumu.

- Tvērums:

    Elektroniskie rēķini, kas importēti programmā Finance un Supply Chain Management, neņemot vērā rindu skaitu, ko ietver šie elektroniskie rēķini.

- Aprēķins:

    Saņemts = importēto elektronisko rēķinu skaits programmā Finance un Supply Chain Management.

## <a name="functions"></a>Funkcijas
### <a name="purchase"></a>Pirkšana

Cilnē **Lietojums mēnesī (eksports)** atlasiet **Pirkums**, lai manuāli reģistrētu iegādāto iesniegumu summu.

Norādītajam datumam atlasiet **Jauns** un ievadiet šaja datumā iegādāto **Pakešu** skaitu.

**Daudzumu** aprēķina šādi:

Daudzums = Paketes * 1,000

Aprēķinātais **Daudzums** tiek atainots dialoglodziņā **Pirkums** no indikatora **Lietojums mēnesī (eksports)**.

### <a name="update"></a>Grāmatot

Darbību rūtī atlasiet **Atjaunināt**, lai atsvaidzinātu aprēķinu un atjauninātu lapā un diagrammā parādītos datus.

### <a name="reset-history-data"></a>Atiestatīt vēstures datus

Darbību rūtī atlasiet **Atiestatīt vēstures datus**, lai atsvaidzinātu datu bāzi, no kuras tiek aprēķināti indikatori.




> [!NOTE]
> **Lietojuma pārvaldības** informācijas panelī netiek rādītas naudas summas. Tā vietā tiek parādītas tikai uzskaitītās iesniegšanas un importēto dokumentu apjoms.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
