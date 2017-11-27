---
title: "Iestatīt ārējo katalogus elektroniskai atzīmēšanas sagādei"
description: "Šajā tēmā ir aprakstīta ārējā vai atzīmēšanas kataloga izmantošana piedāvājuma informācijas iegūšanai no kreditora un pievienošanai pieprasījumam."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a20bb97e451ac59ba23c7f767b5feb336278dcd1
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>Iestatīt ārējo katalogus elektroniskai atzīmēšanas sagādei

Izmantojot ārējo katalogu, var nodrošināt, lai preces un cenas informācija, kas vēlāk tiek apstrādāta Dynamics 365 for Finance and Operations izdevuma Enterprise 2017. jūlija laidienā, būtu precīza un aktuāla. Pieprasījumu pēc tam var apstiprināt un pārveidot par pirkuma pasūtījumu un pasūtījumu var izvietot kreditoram.

Kad tiek iestatīts ārējais katalogs un darbinieks gatavo pieprasījumu, būs pieejama opcija novirzīt uz ārējo vietu, ārējo katalogu un atgriezt iepirkumu grozā, kad tika izveidota ārējā vietā. Šis paziņojums ir balstīts uz cXML protokolu un tas ir jāiestata starp pirkšanas sistēmām un pārdošanas organizāciju.

Lai iestatītu savienojumu, jūsu kreditoram ir jāiesniedz jums informācija, ko izmantot ārējā kataloga konfigurācijai, piemēram, identitāte, pircēju uzņēmuma domēns, piemēram, “DUNS” un “DUNS numurs”, akreditācijas dati un URL, lai piekļūtu kreditoru katalogiem.

## <a name="setting-up-an-external-catalog"></a>Ārējā kataloga iestatīšana

Ārējā katalogā jāiespējo darbinieks, kurš ievada pirkšanas pieprasījumu, kas jānovirza uz ārējo vietu, lai atlasītu preces. Preces, ko darbinieks atlasa no ārējā kataloga, tiek atgrieztas programmatūrā Dynamics 365 for Finance and Operations ar jaunāko cenu informāciju, un no šejienes tās var pievienot pirkšanas pieprasījumam. Nolūks nav atļaut darbiniekiem veikt pasūtījumu ārējā vietā. Iestatot ārējo katalogu, ir jānodrošina, ka vietas, kurai var piekļūt no ārējā kataloga, mērķis ir piedāvājuma informācijas apkopošana, nevis reāla pasūtījuma veikšana.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Lai iestatītu ārējo piegādātāju katalogu, jāizpilda šādi uzdevumi.

1. Iestatiet sagādes kategoriju hierarhiju. Plašāku informāciju skatiet sadaļā [Iestatīt politikas sagādes kategoriju hierarhijai](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Reģistrējiet kreditoru programmatūrā Finance and Operations. Lai iestatītu konfigurācijas un piekļūtu ārējam kreditora katalogam, programmatūrā Microsoft Dynamics 365 jāiestata kreditors un kreditora kontaktpersonas. Ārējā kataloga kreditors arī ir jāpievieno atlasītajai sagādes kategorijai. Plašāku informāciju par kreditoru reģistrāciju programmatūrā Microsoft Dynamics 365 skatiet sadaļā [Pārvaldīt kreditoru sadarbības lietotājus](manage-vendor-collaboration-users.md). Informāciju par to, kā piešķirt kreditorus sagādes kategorijai, skatiet tēmā [Kreditoru apstiprināšana noteiktām sagādes kategorijām](tasks/approve-vendors-specific-procurement-categories.md).
3. Pārliecinieties, vai ir iestatītas mērvienības un valūta, ko izmanto kreditors. Informāciju par to, kā izveidot mērvienību, skatiet rakstā [Mērvienību pārvaldība](../pim/tasks/manage-unit-measure.md).
4. Konfigurējiet ārējo piegādātāju katalogu, izmantojot piegādātāju prasību ārējo kataloga vietni. Papildinformāciju par šo uzdevumu skatiet sadaļā [Ārējā piegādātāju kataloga konfigurēšana](#configure-the-external-vendor-catalog).
5. Testējiet ārējā piegādātāju kataloga konfigurācijas, lai pārbaudītu, vai iestatījumi ir derīgi un varat piekļūt ārējam piegādātāju katalogam. Izmantojiet darbību **Validēt iestatījumus**, lai validētu pieprasījuma iestatījumu ziņojumu, ko esat definējis. Šim ziņojumam būtu jāatver ārējā piegādātāju kataloga vietne pārlūka logā. Pārbaudes laikā nevar pasūtīt preces un pakalpojumus no kreditora. Lai pasūtītu preces un pakalpojumus, ir jāpiekļūst piegādātāju katalogam no pirkšanas pieprasījuma.
6. Aktivizējiet ārējo katalogu, izmantojot pogu **Aktivizējiet katalogu** lapā **Ārējie katalogi**. Ārējais katalogs ir jāaktivizē, lai darbinieki varētu to lietot. Varat deaktivizēt ārējo katalogu jebkurā laikā.


## <a name="configure-the-external-vendor-catalog"></a>Ārējā piegādātāju kataloga konfigurēšana

Šī sadaļa sniedz sīkāku informāciju par iepriekšējā sadaļā minēto 4. uzdevumu.

1. Ievadiet nosaukumu un aprakstu par piegādātāja ārējo katalogu. Nosaukums, ko ievadīsit, parādīsies grozā, kas atspoguļo ārējo katalogu, kas tiek rādīts darbiniekiem, kuri izveido pieprasījumu. Darbinieki var noklikšķināt uz groza, lai atvērtu katalogu no kreditora ārējā kataloga vietnes.
2. Pievienojiet attēlu, izmantojot darbību **Ārējā kataloga attēls**. Attēls parādīsies grozā, kas atspoguļo ārējo katalogu, kas tiek rādīts darbiniekiem, kuri izveido pieprasījumu. Ņemiet vērā, ka attēla platumam un augstumam ir jābūt vienādam. Pretējā gadījumā attēls tiks parādīts nepareizi.
3. Atlasiet, vai kreditora ārējā kataloga vietne ir jāparāda tajā pašā pārlūka logā, kur darbinieks ir izveidojis šo pieprasījumu, vai arī tā jāatver jaunā logā.
4. Atlasiet katalogu kreditoram. Sarakstā **Juridiskās personas** ir rinda katrai juridiskajai personai, kur jāiestata kreditors. Lai lietotāji varētu pieprasīt preces tieši no dažu juridisko personu, bet ne citu, kreditora kataloga, var izmantot pogu **Neļaut piekļuvi** vai **Atļaut piekļuvi** katrai tai juridiskajai personai, kurai katalogam ir vai nav jābūt pieejamam.
5. Laukā **Noklusējuma derīguma termiņš (dienās)** ievadiet dienu skaitu, kad piedāvājums, kas saņemts no ārējā kataloga, ir spēkā un kad to var izmantot, lai veiktu iegādi no ārējā kreditora. Pēc piedāvājuma izveides un izguves no piegādātāja ārējās kataloga vietas piedāvājums ir derīgs, sākot ar pašreizējo sistēmas datumu un paliek spēkā uz to dienu skaitu, ko ievadījāt šajā laukā.
6. Noklikšķiniet uz pogas **Pievienot**, lai sāktu sagādes kategoriju kartēšanu ārējā katalogā. Pēc tam sarakstā Kategorijas nosaukums atlasiet kategoriju. Kategoriju saraksts ir paplašināts sagādes kategoriju variants, ko kreditors kartēja visām juridiskajām personām, kuras kreditors iestatīja.
[!NOTE]
Iepirkuma politikas tiek izmantotas, lai atļautu vai ierobežotu piekļuvi kategorijām juridiskajai personai, kura iegādājas, vai pārvaldības struktūrvienībai, kura saņem. Lai veiktu atzīmēšanu ārējā katalogā, nepieciešama piekļuve vismaz vienai sagādes kategorijai, kas ir kartēta katalogā.
7. Iestatiet cXML iestatījumu pieprasījuma ziņojumu, kas tiks nosūtīts kreditoram. Automātiski ģenerētā ziņojuma formāts ir minimālā veidne, kas ir nepieciešama, lai sāktu sesiju. Ievadiet etiķešu vērtības.

Sistēmas ziņojuma veidni jebkurā laikā var pārlādēt, noklikšķinot uz **Atjaunot ziņojuma formātu**. Ņemiet vērā, ka, atjaunojot ziņojuma formātu, pašreizējais ziņojums tiks aizstāts ar automātiski ģenerētu ziņojumu formātu, kam ir tukšas etiķetes.

### <a name="cxml-setup-message"></a>cXML iestatījumu ziņojums
Zemāk varat atrast visu to etiķešu aprakstus, kas ir iekļautas veidnē.

| Lauks | Apraksts | 
|---------|---------|
|< Virsraksts >< No >< Akreditācijas datu domēns=”” >|Pircēja uzņēmuma domēns.|
|< Virsraksts >< No >< Akreditācijas dati>< Identitāte >< /Identity > | Pircēja uzņēmuma identitāte.|
|< Virsraksts >< Adresāts >< Akreditācijas datu domēns=”” > | Kreditora uzņēmuma domēns.|
|< Virsraksts >< Adresāts >< Akreditācijas dati>< Identitāte >< /Identity> | Kreditora uzņēmuma identitāte.|
|< Virsraksts >< Sūtītājs >< Akreditācijas datu domēns=”” > | Pircēja uzņēmuma domēns.|
|< Virsraksts >< Sūtītājs >< Akreditācijas dati >< Identitāte >< /Identity> | Pircēja uzņēmuma identitāte.|
|< Virsraksts >< Sūtītājs ><Akreditācijas dati >< SharedSecret >< /SharedSecret >|Pircēja uzņēmuma koplietojamais noslēpums.|
|< Pieprasījuma režīms deploymentMode=”” >|Pārbaudes vai ražošanas izvietošana.|
|< Pieprasījums >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Kreditora atzīmēšanas galapunkta URL.|

### <a name="extrinsic-elements"></a>Ārēji elementi

Ārējs elements ir papildinformācija, piemēram, lietotājvārds, kas tiek balstīta uz lietotāju, kas atzīmē aiziešanu. Ārējs elements tiek iestatīts, ja tiek atzīmēta aiziešana, un to var nosūtīt iestatīšanas pieprasījuma ziņojumā.
Kreditoram varētu būt prasība saņemšanai ārēju elementu iestatīšanas pieprasījumā. Šajā gadījumā ārējo elementu pievienojiet ārēju elementu sarakstam lapas **Ārējais katalogs** sadaļā **Ziņojuma formāts**. Norādiet ārējā elementa nosaukumu, ko kreditors var atpazīt un kartēt vērtībā. Vērtību opcijas: Lietotājvārds, Lietotāja e-pasts vai Nejauša vērtība.
Plašāku informāciju par cXML protokolu skatiet vietnē http://cxml.org/

## <a name="post-back-message"></a>Ar iepriekšēju datumu grāmatots ziņojums
Ar iepriekšēju datumu grāmatots ziņojums tiek saņemts no kreditora, kad lietotājs atzīmē aiziešanu no ārējās vietnes un atgriežas programmatūrā Finance and Operations. Ar iepriekšēju datumu grāmatotus ziņojumus nevar konfigurēt. Ziņojumi ir balstīti uz cXML protokola definīciju. Tālāk ir norādīta informācija, kas var būt daļa no ar iepriekšēju datumu grāmatota ziņojuma, kurš tiek saņemts pieprasījuma rindā.

| No kreditora saņemts ziņojums | Kopēts Finance and Operations pieprasījuma rindā|
|------------------------------|----------------------------------------------------------|
|< Krājumu daudzums=”” > |Daudzums|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Ārējā krājuma ID|
|< ItemDetail>< UnitPrice >< Naudas valūta=”” >| Valūta|
|< ItemDetail >< UnitPrice >< Nauda >< /Money >| Vienības cena|
|< ItemDetail >< Apraksta ShortName=”” >|Preces nosaukums|
|< ItemDetail >< Apraksts >< /Description >|Iekļauts krājuma aprakstā; preces nosaukums, ja ShortName vērtība nav norādīta.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Vienība|
|< ItemDetail >< Klasifikācija >< /Classification >|Iekļauts rēķina aprakstā|
|< ItemDetail >< Klasifikācijas domēns=”” >|Iekļauts rēķina aprakstā|

## <a name="delete-an-external-catalog"></a>Dzēš ārējo katalogu
Dzēsiet ārējo katalogu ar lapas darbību Dzēst.

Ja tika pieprasīta preces dzēšana no ārējā piegādātāju kataloga, ārējo piegādātāju katalogu nevar dzēst. Tā vietā ārējā piegādātāju kataloga statuss tiek iestatīts uz Neaktīvs. Ja vēlaties noņemt piekļuvi ārējā piegādātāju kataloga vietnei, bet nevēlaties to dzēst, mainiet ārējā kataloga statusu uz Neaktīvs.


