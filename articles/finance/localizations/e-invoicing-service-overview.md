---
title: Pārskats par elektronisko rēķinu izrakstīšanas pievienojumprogrammu
description: Šajā tēmā ir sniegta informācija par elektronisko rēķinu izrakstīšanas pievienojumprogrammu programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffd48e173b66cc6d2571e666d5452a5eff05176c
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/19/2020
ms.locfileid: "4445766"
---
# <a name="electronic-invoicing-add-on-overview"></a>Pārskats par elektronisko rēķinu izrakstīšanas pievienojumprogrammu

[!include [banner](../includes/banner.md)]

Elektroniskā rēķinu pievienojumprogramma programmām Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management ir hipermērogojams vairāku nomnieku pakalpojums, kas iespējo elektronisko rēķinu dokumentu un konfigurējamas dokumentu apmaiņas konfigurējamu apstrādi. Apstrādes un integrācijas noteikumi ir pilnībā konfigurējami, un šī loģika darbojas ārpus programmām Finance un Supply Chain Management. Pakalpojums galvenokārt ir paredzēts e-rēķinu apstrādei biznesa-valdības scenārijos, bet to var pielāgot citiem nolūkiem.

Elektronisko rēķinu izrakstīšanas pievienojumprogramma var palīdzēt sasniegt šādus mērķus:

- Valstu/reģionu specifisko prasību ātra un vienkārša pieņemšana
- Elektronisko rēķinu izrakstīšanas pievienojumprogrammas risinājuma standartizēta implementēšana
- Dokumenta vēstures uzlabota izsekojamība
- Īsāks ieviešanas cikls
- Samazinātas kopējās īpašumtiesību izmaksas (total cost of ownership - TCO)
- Viegli pielāgojamas konfigurācijas, kam nav nepieciešamas koda izmaiņas
- Vienkāršots konfigurācijas iepakojums
- Iebūvēta eksportēšana, importēšana un integrēšana, un vienkārša paplašināšana, apstrādājot e-rēķinu dokumentus
- Vienkārša vienādu eksportēšanas, importēšanas un integrēšanas konfigurāciju izmantošana uzņēmumos

Lai izmantotu elektronisko rēķinu izrakstīšanas pievienojumprogrammu, tas ir jāinstalē no jūsu projekta programmā Microsoft Dynamics Lifecycle Services (LCS). Pēc tam sekojiet iestatīšanas procedūrai, lai ieslēgtu integrāciju ar programmu Finance vai Supply Chain Management. Papildinformāciju skatiet sadaļā [Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="availability"></a>Pieejamība

Sākotnēji elektronisko rēķinu izrakstīšanas pievienojumprogramma ir pieejama atlasītajiem debitoriem, izmantojot priekšskatījuma programmu. Vēlāk priekšskatījums tiks atvērts plašākam debitoru lokam. Visbeidzot pakalpojums kļūs vispārīgi pieejams. Tā kā funkcionalitāte, kas attiecas uz valsts/reģiona specifiskām prasībām, var būt ierobežota dažādās laidiena fāzēs, vienmēr pārbaudiet visjaunāko dokumentāciju, kas izceļ atbalstīto valsts/reģiona specifisko risinājumu segumu un darbības jomu.

Elektronisko rēķinu izrakstīšanas pievienojumprogramma ir izvietota šādās Azure ģeogrāfijās:

- ASV
- Eiropa

> [!NOTE]
> Elektronisko rēķinu izrakstīšanas pievienojumprogramma neatbalsta lokālas izvietošanas.

## <a name="extended-configurability"></a>Paplašinātā konfigurēšana

Elektronisko rēķinu izrakstīšanas pievienojumprogrammu var izmantot scenārijos, kur jāizveido un jānosūta elektronisks dokuments izraudzītajām pusēm. Tā ir īpaši izstrādāta konfigurējamu apstrādes darbību plūsmas vadīšanai, pamatojoties uz saņemtajiem datiem. Finance un Supply Chain Management pieejamās konfigurēšanas opcijas ir ierobežotas ar dokumentu transformāciju. Pakalpojums paplašina šīs opcijas, pievienojot tajā pieejamās konfigurējamas integrācijas. Turklāt visas elektronisko rēķinu funkcionalitātes, kas iepriekš bija pieejamas, piemēram, Brazīlijas Nota fiscal eletrônica (NF-e), Meksikas Comprobante Fiscal Digital por Internet (CFDI) vai citas Rietumeiropas universālās biznesa valodas (Universal Business Language - UBL)/Pan-European Public Procurement OnLine (PEPPOL) funkcionalitātes, izmantos konfigurācijas eksportēšanai un importēšanai, kā arī iespējos integrāciju ar ārējiem tīmekļa pakalpojumiem.

## <a name="feature-highlights"></a>Līdzekļu iezīmēšana

- Out-of-box integrācija ar Finance un Supply Chain management
- Saskaņota lietotāja pieredze, lai varētu konfigurēt un pārraudzīt e-rēķinu procesu visās valstīs vai reģionos
- Ātrāka, vieglāka un lētāka Elektronisko rēķinu izrakstīšanas pievienojumprogrammas risinājuma pieņemšana jaunajās valstīs vai reģionos
- Pakalpojuma konfigurācija, izmantojot regulatīvo konfigurācijas pakalpojumu (Regulatory Configuration Service - RCS) un globalizācijas līdzekļa iestatījumu
- Biznesa datu pārveide vairākos e-rēķinu formātos (XML, JavaScript Object Notation \[JSON\], TXT un ar komatu atdalītas vērtības \[CSV\]), izmantojot konfigurācijas, kas definētas RCS:

    - Elektronisko pārskatu formāti, kas ir pieejami valstīm vai reģioniem, kur nav pieejamas konfigurēšana e-rēķina pārveidei

- Konfigurējama e-rēķinu iesniegšana ārējiem tīmekļa pakalpojumiem, ieskaitot sertifikāciju, izmantojot elektroniskos parakstus:

    - Iebūvēta, viegli pagarināma un konfigurējama integrācija ar papildu saturu vairākām valstīm

    > [!NOTE]
    > Pašlaik tiek atbalstīts ierobežots tiešo iesniegumu skaits. Papildinformāciju skatiet sadaļā [Pieejamība](#availability) iepriekš šajā tēmā. Nākotnē atbalsts tiks paplašināts.

- Atbilžu apstrāde no tīmekļa pakalpojumiem, ieskaitot konfigurējamu izņēmuma ziņojumu apstrādi
- Elektronisko parakstu atbalsts (piemēram, izmantojot XMLDSig parakstīšanas algoritmu)
- E-rēķina ziņojumu pakešveida apstrāde

## <a name="architecture-and-data-flow"></a>Arhitektūra un datu plūsma

Kad elektronisko rēķinu izrakstīšanas pievienojumprogramma ir instalēta no LCS un pieprasītā iestatīšana ir pabeigta visās nepieciešamajās lietojumprogrammās, tiek izveidots drošs savienojums. Pakalpojums šobrīd atrodas datu centros Amerikas Savienotajās Valstīs un Eiropā. Tāpēc pakalpojuma atrašanās vieta var atšķirties no saistīto Finance vai Supply Chain Management instances atrašanās vietas. Pēc elektronisko rēķinu izrakstīšanas pievienojumprogrammas iestatīšanas un integrācijas ieslēgšanas, kad elektroniskais rēķins tiek nosūtīts, pamatdati un transakciju dati, kas ir saistīti ar noteiktu dokumentu, tiek nosūtīti elektronisko rēķinu izrakstīšanas pievienojumprogrammai.

> [!NOTE]
> Ja elektroniskajā rēķinā vai citos dokumentos ir ietverti personiskie dati, pārbaudiet, vai šīs funkcijas izmantošana atbilst vispārīgajai datu aizsardzības regulai (General Data Protection Regulation - GDPR) un citiem noteikumiem, kas ir saistīti ar personisko datu pārsūtīšanu.

### <a name="high-level-description-of-the-data-flow"></a>Datu plūsmas augsta līmeņa apraksts

1. Klients nosūta uzņēmumam kanonisko biznesa dokumentu.
2. Balstoties uz konteksta informāciju, kas tiek saņemta no klienta, pakalpojums atlasa piemērojamo apstrādes plūsmu.
3. Pakalpojums izpilda apstrādes darbības. Šīs darbības var ietvert biznesa dokumenta pārveidošanu elektroniskā rēķinā, elektroniskā paraksta piemērošanu un dokumenta iesniegšanu ārējam tīmekļa pakalpojumam.
4. Visi saņemtie un apstrādātie dokumenti tiek glabāti klienta Azure BLOB krātuvē.
5. Visi nomnieka noslēpumi un sertifikāti, kas tika izmantoti apstrādei, tiek saglabāti klienta Azure galvēnajā glabātuvē.
6. Pakalpojums pēc pieprasījuma sniedz klientam informāciju par nosūtītā biznesa dokumenta apstrādes statusu.
7. Klients saņem informāciju par pabeigto apstrādes izpildi un padara visu žurnāla informāciju pieejamu. Tas arī padara pieejamu dokumentu, kas tika izveidots vai saņemts plūsmas apstrādes laikā.

Sekojošajā attēlā ir parādīts, kā dati plūst no elektronisko rēķinu izrakstīšanas pievienojumprogrammas un uz to.

![Elektronisko rēķinu izrakstīšanas pievienojumprogrammas datu plūsma](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti
Iespējojot un izmantojot elektronisko rēķinu izrakstīšanu, var būt nepieciešams nosūtīt ierobežotus datus, kas ietver organizācijas nodokļa reģistrācijas ID. Tas tiks nosūtīts trešo personu aģentūrām, ko pilnvarojusi nodokļu iestādes, lai nosūtītu elektroniskos rēķinus šai nodokļu iestādei iepriekš noteiktos formātos, kas nepieciešams integrācijai ar valdības tīmekļa pakalpojumiem. No šīm ārējām sistēmām importētie dati šajā Dynamics 365 tiešsaistes pakalpojumā ir pakļauti mūsu [paziņojumam par privātumu](https://go.microsoft.com/fwlink/?LinkId=512132). Lai iegūtu plašāku informāciju, skatiet sadaļas Konfidencialitātes paziņojums valstij raksturīgā līdzekļa dokumentācijā.

## <a name="additional-resources"></a>Papildu resursi

- [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md)
- [Sākt ar elektronisko rēķinu pievienojumu Brazīlijai](e-invoicing-bra-get-started.md)
- [Sākt ar elektronisko rēķinu pievienojumu Meksikai](e-invoicing-mex-get-started.md)
- [Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai](e-invoicing-ita-get-started.md)
- [Elektronisko rēķinu izrakstīšanas pievienojumprogrammas iestatīšana](e-invoicing-setup.md)
