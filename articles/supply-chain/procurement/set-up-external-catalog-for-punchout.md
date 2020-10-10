---
title: Ārēja kataloga iestatīšana elektroniskai atzīmēšanas sagādei
description: Šajā tēmā ir aprakstīta ārējā vai atzīmēšanas kataloga izmantošana piedāvājuma informācijas iegūšanai no kreditora un pievienošanai pieprasījumam.
author: mkirknel
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7aecc2c4786a1912bf5ae44f3949428c778f1df9
ms.sourcegitcommit: b281ac04157f6ccbd159fc89f58910b430a3b6a9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826832"
---
# <a name="set-up-an-external-catalog-for-punchout-e-procurement"></a>Ārēja kataloga iestatīšana elektroniskai atzīmēšanas sagādei

[!include [banner](../includes/banner.md)]

Izmantojot ārējo katalogu, varat nodrošināt, ka vēlāk sadaļā Supply Chain Management apstrādātā informācija par preci un cenu ir pareiza un aktuāla. Pieprasījumu pēc tam var apstiprināt un pārveidot par pirkuma pasūtījumu un pasūtījumu var izvietot kreditoram.

Kad tiek iestatīts ārējais katalogs un darbinieks gatavo pieprasījumu, būs pieejama opcija novirzīt uz ārējo vietu, ārējo katalogu un atgriezt iepirkumu grozā, kas tika izveidota ārējā vietā. Šis paziņojums ir balstīts uz cXML protokolu un tas ir jāiestata starp pirkšanas sistēmām un pārdošanas organizāciju.

Lai iestatītu paziņojumu, jūsu kreditoram ir jāiesniedz jums informācija, ko izmantot ārējā kataloga konfigurācijai, piemēram, identitāte, pircēju uzņēmuma domēns, piemēram, “DUNS” un “DUNS numurs”, akreditācijas dati un URL, lai piekļūtu piegādātāju katalogiem.

## <a name="setting-up-an-external-catalog"></a>Ārējā kataloga iestatīšana

Ārējā katalogā jāiespējo darbinieks, kurš ievada pirkšanas pieprasījumu, kas jānovirza uz ārējo vietu, lai atlasītu preces. Preces, ko darbinieks atlasa ārējā katalogā, tiek atgrieztas ar jaunāko cenu informāciju, un pēc tam tās var pievienot pirkšanas pieprasījumam. Nolūks ir neatļaut darbiniekiem veikt pasūtījumu ārējā vietā. Iestatot ārējo katalogu, ir jānodrošina, ka vietas, kurai var piekļūt no ārējā kataloga, mērķis ir piedāvājuma informācijas apkopošana, nevis reāla pasūtījuma veikšana.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Lai iestatītu ārējo piegādātāju katalogu, jāizpilda šādi uzdevumi.

1. Iestatiet sagādes kategoriju hierarhiju. Papildinformāciju skatiet sadaļā [Politikas iestatīšana sagādes kategoriju hierarhijai](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Reģistrēt kreditoru Supply Chain Management. Pirms piekļuves konfigurāciju iestatīšanas piegādātāju ārējam katalogam programmā Microsoft Dynamics 365 ir jāiestata kreditors un kreditora kontaktpersona. Ārējā kataloga kreditors ir jāpievieno arī atlasītajai sagādes kategorijai. Papildinformāciju par kreditoru reģistrāciju skatiet rakstā [Kreditoru sadarbības lietotāju pārvaldība](manage-vendor-collaboration-users.md). Informāciju par to, kā piešķirt kreditorus sagādes kategorijai, skatiet tēmā [Kreditoru apstiprināšana noteiktām sagādes kategorijām](tasks/approve-vendors-specific-procurement-categories.md).
3. Pārliecinieties, vai ir iestatītas mērvienības un valūta, ko izmanto kreditors. Informāciju par to, kā izveidot mērvienību, skatiet rakstā [Mērvienību pārvaldība](../pim/tasks/manage-unit-measure.md).
4. Konfigurējiet ārējo piegādātāju katalogu, izmantojot piegādātāju prasību ārējo kataloga vietu. Papildinformāciju par šo uzdevumu skatiet sadaļā [Ārējā piegādātāju kataloga konfigurēšana](#configure-the-external-vendor-catalog).
5. Testējiet ārējā piegādātāju kataloga konfigurācijas, lai pārbaudītu, vai iestatījumi ir derīgi un varat piekļūt ārējam piegādātāju katalogam. Izmantojiet darbību **Validēt iestatījumus**, lai validētu iestatīšanas pieprasījuma ziņojumu, ko esat definējis. Šim ziņojumam ir jāizraisa kreditoru ārējā kataloga vietnes atvēršana pārlūkprogrammas logā. Pārbaudes laikā nevar pasūtīt preces un pakalpojumus no kreditora. Lai pasūtītu preces un pakalpojumus, ir jāpiekļūst piegādātāju katalogam no pirkšanas pieprasījuma.
6. Aktivizējiet ārējo katalogu, izmantojot pogu **Aktivizēt katalogu** lapā **Ārējie katalogi**. Lai darbinieki varētu lieto ārējo katalogu, vispirms tas ir jāaktivizē. Varat deaktivizēt ārējo katalogu jebkurā laikā.


## <a name="configure-the-external-vendor-catalog"></a>Ārējā piegādātāju kataloga konfigurēšana

Šī sadaļa sniedz sīkāku informāciju par iepriekšējā sadaļā minēto 4. uzdevumu.

1. Ievadiet piegādātāja ārējā kataloga nosaukumu un aprakstu. Nosaukums, ko ievadīsit, parādīsies grozā, kas atspoguļo ārējo katalogu, kas tiek rādīts darbiniekiem, kuri izveido pieprasījumu. Darbinieki var noklikšķināt uz groza, lai atvērtu katalogu no kreditora ārējā kataloga vietnes.
2. Pievienojiet attēlu, izmantojot darbību **Ārējā kataloga attēls**. Attēls parādīsies grozā, kas atspoguļo ārējo katalogu, kas tiek rādīts darbiniekiem, kuri izveido pieprasījumu. Ņemiet vērā, ka attēla platumam un augstumam ir jābūt vienādam. Pretējā gadījumā attēls tiks parādīts nepareizi.
3. Atlasiet, vai piegādātāju ārējā kataloga tīmekļa vietne ir jāparāda jaunā pārlūkprogrammas logā vai tajā pašā logā, kurā darbinieks ir izveidojis šo pieprasījumu.
4. Atlasiet katalogu kreditoram. Sarakstā **Juridiskās personas** ir rinda katrai juridiskajai personai, kur jāiestata kreditors. Lai atļautu lietotājiem tiešā veidā pieprasīt preces no dažu juridisko personu (bet ne citu) piegādātāju kataloga, varat izmantot pogu **Neļaut piekļuvi** vai **Atļaut piekļuvi** katrai juridiskajai personai, kuras katalogam ir vai nav jābūt pieejamam.
5. Laukā **Noklusējuma derīguma termiņš (dienās)** ievadiet dienu skaitu, kad piedāvājums, kas saņemts no ārējā kataloga, ir spēkā un kad to var izmantot, lai veiktu iegādi no ārējā kreditora. Pēc piedāvājuma izveides un izguves no piegādātāja ārējās kataloga vietnes, piedāvājums ir derīgs, sākot ar pašreizējo sistēmas datumu un paliek spēkā uz to dienu skaitu, ko ievadījāt šajā laukā.
6. Noklikšķiniet uz pogas **Pievienot**, lai sāktu sagādes kategoriju kartēšanu ārējā katalogā. Pēc tam atlasiet kategoriju sarakstā Kategorijas nosaukums. Kategoriju saraksts ir paplašināts sagādes kategoriju variants, ko kreditors kartēja visām juridiskajām personām, kuras kreditors iestatīja.

    > [!NOTE]
    > Iepirkuma politikas tiek izmantotas, lai atļautu vai ierobežotu piekļuvi kategorijām juridiskajai personai, kura iegādājas, vai pārvaldības struktūrvienībai, kura saņem. Lai veiktu atzīmēšanu ārējā katalogā, ir jābūt atļautai piekļuvei vismaz vienai no sagādes kategorijām, kas ir kartētas ar katalogu.

7. Iestatiet cXML iestatījumu pieprasījuma ziņojumu, kas tiks nosūtīts kreditoram. Automātiski ģenerētā ziņojuma formāts ir minimālā veidne, kas ir nepieciešama, lai sāktu sesiju. Ievadiet etiķešu vērtības.

Varat jebkurā brīdī pārlādēt sistēmas ģenerēto ziņojuma veidni, noklikšķinot uz vienuma **Atjaunot ziņojuma formātu**. 
Ņemiet vērā, ka, atjaunojot ziņojuma formātu, pašreizējais ziņojuma formāts tiek aizstāts ar automātiski ģenerētu ziņojumu formātu, kurā ir tukšas etiķetes.

### <a name="cxml-setup-message"></a>cXML iestatījumu ziņojums
Zemāk varat atrast visu to etiķešu aprakstus, kas ir iekļautas veidnē.

| Lauks | Apraksts | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Pircēja uzņēmuma domēns.|
|< Header >< From >< Credential>< Identity >< /Identity > | Pircēja uzņēmuma identitāte.|
|< Header >< To >< Credential domain=”” > | Kreditora uzņēmuma domēns.|
|< Header >< To >< Credential>< Identity >< /Identity> | Kreditora uzņēmuma identitāte.|
|< Header >< Sender >< Credential domain=”” > | Pircēja uzņēmuma domēns.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Pircēja uzņēmuma identitāte.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Pircēja uzņēmuma koplietojamais noslēpums.|
|< Request deploymentMode=”” >|Pārbaudes vai ražošanas izvietošana.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Kreditora atzīmēšanas galapunkta URL.|

### <a name="extrinsic-elements"></a>Ārēji elementi

Ārējs elements ir papildinformācija, piemēram, lietotājvārds, kas ir atkarīga no lietotāja, kas reģistrē aiziešanu. Ārējais elements tiek iestatīts, kad tiek reģistrēta aiziešana, un to var nosūtīt iestatīšanas pieprasījuma ziņojumā.
Kreditoram var būt nepieciešama prasība, lai iestatīšanas pieprasījumā tiktu saņemts ārējais elements. Šādā gadījumā ārējais elements ir jāpievieno ārējo elementu sarakstam lapas **Ārējais katalogs** sadaļā **Ziņojuma formāts**.
Norādiet ārējā elementa nosaukumu, ko kreditors var atpazīt un kartēt vērtībā. Vērtību opcijas: Lietotājvārds, Lietotāja e-pasts vai Nejauša vērtība.
Plašāku informāciju par cXML protokolu skatiet [cXML.org tīmekļa vietnē](http://cxml.org/).

## <a name="post-back-message"></a>Ar iepriekšēju datumu grāmatots ziņojums
Ar iepriekšēju datumu grāmatots ziņojums ir ziņojums, kas tiek saņemts no kreditora, kad lietotājs reģistrē aiziešanu no ārējās vietnes un atgriežas programmatūrā Supply Chain Management. Ar iepriekšēju datumu grāmatotos ziņojumus nevar konfigurēt. Ziņojumi tiek izveidoti, pamatojoties uz cXML protokola definīciju. Tālāk ir norādīta informācija, kas var būt ietverta ar iepriekšēju datumu grāmatotā ziņojumā, kurš tiek saņemts pieprasījuma rindā.

| No kreditora saņemts ziņojums | Kopēts pieprasījuma rindā|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Daudzums|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Ārējā krājuma ID|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Valūta|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Vienības cena|
|< ItemDetail >< Description ShortName=”” >|Preces nosaukums|
|< ItemDetail >< Description >< /Description >|Iekļauts krājuma aprakstā; preces nosaukums, ja ShortName vērtība nav norādīta.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Vienība|
|< ItemDetail >< Classification >< /Classification >|Iekļauts rēķina aprakstā|
|< ItemDetail >< Classification domain=”” >|Iekļauts rēķina aprakstā|

## <a name="delete-an-external-catalog"></a>Dzēš ārējo katalogu
Dzēsiet ārējo katalogu ar lapas darbību Dzēst.

Ja tika pieprasīta preces dzēšana no ārējā piegādātāju kataloga, ārējo piegādātāju katalogu nevar dzēst. Tā vietā ārējā piegādātāju kataloga statuss tiek iestatīts uz Neaktīvs. Ja vēlaties noņemt piekļuvi ārējā piegādātāju kataloga vietnei, bet nevēlaties to dzēst, mainiet ārējā kataloga statusu uz Neaktīvs.

## <a name="additional-resources"></a>Papildu resursi

- [CXML uzlabojumu iegāde](purchasing-cxml-enhancements.md)
- [Ārējo katalogu izmantošana elektroniskai atzīmēšanas sagādei](use-external-catalogs-for-punchout.md)