---
title: "Iestatītu pamatlīdzekļus"
description: "Šajā tēmā ir sniegts pārskats par modeļa Pamatlīdzekļi iestatīšanu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: dde8053df96d03c8c8e52fa6d2fdf7f74e95ec92
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fixed-assets"></a>Iestatītu pamatlīdzekļus

Šajā tēmā ir sniegts pārskats par modeļa Pamatlīdzekļi iestatīšanu.

<a name="overview"></a>Pārskats
--------
Parametri kontrolē pamatlīdzekļu vispārīgo darbību.

Pamatlīdzekļu grupas jums ļauj grupēt savus līdzekļus un norādīt noklusējuma atribūtus katram grupai piešķirtajam līdzeklim. Pamatlīdzekļu grupām tiek piešķirtas grāmatas. Grāmatas seko līdzi pamatlīdzekļa finansiālajai vērtība laika gaitā, izmantojot nolietojuma tabulā definēto nolietojuma konfigurāciju.

Kad tiek izveidoti pamatlīdzekļi, tie tiek piešķirti kādai grupai. Pēc noklusējuma grāmatas, kuras ir piešķirtas pamatlīdzekļu grupai, pēc tam tiek piešķirtas pamatlīdzeklim. Grāmatas, kuras ir konfigurētas grāmatošanai virsgrāmatā, ir saistītas ar grāmatošanas metodi. Virsgrāmatas konti tiek definēti katrai grāmatai grāmatošanas metodē un tiek izmantoti, kad tiek grāmatotas pamatlīdzekļu transakcijas. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Nolietojuma tabulas
Vispirms jums ir jāiestata nolietojuma tabulas. Nolietojuma tabulā jūs konfigurējat veidu, kādā pamatlīdzekļa vērtība mazinās laika gaitā. Jums ir nepieciešams definēt nolietojuma metodi, nolietojuma aprēķina gadu (kalendāro gadu vai finanšu gadu) un nolietojuma biežumu.

## <a name="books"></a>Grāmatas
Kad ir iestatītas nolietojuma tabulas, jums saviem līdzekļiem ir jāizveido nepieciešamās grāmatas. Katra grāmata seko līdzi neatkarīgam līdzekļa finansiālajam dzīves ciklam. Grāmatas var konfigurēt saistīto transakciju grāmatošanai virsgrāmatā. Šī konfigurācija ir noklusējuma iestatījums, jo tā parasti tiek izmantota uzņēmuma finanšu pārskatiem. Grāmatas, kas nav jāgrāmato Virsgrāmatā grāmatot pamatlīdzekļu subledger un parasti tiek izmantotas nodokļu pārskatiem.

Katrai grāmatai tiek piešķirta primārā nolietojuma tabula. Grāmatām ir arī alternatīvā vai pārslēgšanas nolietojuma tabula, ja šāds tabulas tips ir piemērojams. Lai pamatlīdzekļu grāmatu automātiski iekļautu nolietojuma izpildēs, jums ir jāiespējo opcija Aprēķināt nolietojumu. Ja šī opcija nav atlasīta, aktīvam, nolietojuma priekšlikums pāriet aktīva.

Varat iestatīt arī atvasinātās grāmatas. Norādītās atvasinātās transakcijas tiek grāmatotas kā primāro transakciju precīza kopija pret atvasinātajām grāmatām. Tādēļ atvasinātās transakcijas parasti tiek iestatītas iegādēm un norakstīšanām, nevis nolietojuma transakcijām.

## <a name="fixed-asset-posting-profiles"></a>Pamatlīdzekļu grāmatošanas metodes
Kad esat iestatījis grāmatas, varat izveidot grāmatošanas metodi. Grāmatošanas metodei ir jābūt definētai pēc grāmatas, bet to var definēt arī detalizētākā līmenī. Piemēram, grāmatošanas metodi varat definēt grāmatas un pamatlīdzekļu grupas kombinācijai vai pat atsevišķai pamatlīdzekļu grāmatai. Pēc noklusējuma definētie virsgrāmatas konti tiek lietoti jūsu pamatlīdzekļu transakcijām.

Jums ir nepieciešams definēt virsgrāmatas kontus, kas tiek izmantoti norakstīšanas procesu laikā — gan norakstīšanas pārdošanām, gan brāķiem. Norakstīšanas laikā iepriekš iegrāmatotās pamatlīdzekļu transakcijas tiek anulētas no sākotnējiem kontiem un neto summas tiek pārvietotas uz atbilstošo kontu peļņai un zaudējumiem no līdzekļu norakstīšanas. Lai palīdzētu nodrošināt, ka transakcijas tiek anulētas pareizi, jums ir jāiestata konti katram transakcijas tipam, kas tiek izmantots jūsu uzņēmumā. Par galveno kontu ir jānorāda sākotnējais konts, kuru attiecīgajai grāmatošanas metodei iestatījāt šim transakcijas tipam, un par korespondējošo kontu ir jānorāda jūsu peļņas un zaudējumu konts norakstīšanai. Izņēmums ir atlikusī vērtība. Šajā gadījumā gan galvenais konts, gan korespondējošais konts ir jāiestata uz peļņas un zaudējumu kontu norakstīšanai.

## <a name="fixed-asset-groups"></a>Pamatlīdzekļu grupas
Pamatlīdzekļu grupa ir vienīgais obligātais lauks, kad veidojat pamatlīdzekli. Šī lauka vērtība līdzeklim nosaka vairāku informatīvo lauku noklusējuma vērtību. Grāmatas tiek iestatītas tā, lai katram līdzeklim grupā būtu piešķirta noklusējuma grāmata. Pēc tam grāmatām varat iestatīt atribūtus, kas ir raksturīgas kādai līdzekļu grupai, piemēram, Lietošanas ilgums un Nolietojuma aprēķināšanas metode.

Varat arī definēt speciālā nolietojuma atskaitījumus vai papildnolietojumu konkrētai pamatlīdzekļu grupas un grāmatas kombinācijai. Speciālā nolietojuma atskaitījumiem ir jāpiešķir prioritāte, lai norādītu secību, kādā atskaitījumi tiek aprēķināti, kad grāmatai ir piešķirti vairāki atskaitījumi.

## <a name="fixed-asset-parameters"></a>Pamatlīdzekļu parametri
Pēdējā šīs procedūras darbība ir atjaunināt pamatlīdzekļu parametrus.

Lauks Kapitalizācijas slieksnis nosaka, kuriem pamatlīdzekļiem tiek rēķināts nolietojums. Ja iepirkuma rinda ir atzīmēta kā pamatlīdzeklis, taču tā neatbilst norādīto reģistru slieksni, pamatlīdzekļa joprojām ir izveidojis vai atjauninājis, bet iespēja aprēķināt nolietojumu ir iestatīts uz Nē. Tādēļ aktīva netiks automātiski nolietojumu, kas ir daļa no nolietojuma priekšlikumus.

Svarīga opcija ir Automātiski izveidot nolietojuma korekcijas summas ar norakstīšanu. Ja šo opciju iestatāt uz Jā, tad līdzekļa nolietojums tiek pielāgots automātiski, pamatojoties uz nolietojuma uzstādījumiem līdzekļa norakstīšanas laikā. Cita opcija jums ļauj termiņatlaides atņemt no iegādes summas, kad iegādājaties pamatlīdzekļus, izmantojot kreditora rēķinu.

Kopsavilkuma cilnē Pirkšanas pasūtījumi varat konfigurēt veidu, kādā līdzekļi tiek izveidoti kā daļa no pirkšanas procesa. Pirmā opcija ir Atļaut līdzekļu iegādi no pirkšanas. Ja šo opciju iestatāt uz Jā, tad līdzekļa iegāde notiek laikā, kad tiek grāmatots rēķins. Ja iestatāt šo opciju Nē, joprojām varat ievietot pamatlīdzekļa pirkšanas pasūtījumu (PP) un rēķina, bet netiks iegrāmatota iegāde. Grāmatošana ir jāveic kā atsevišķa darbība no pamatlīdzekļu žurnāla. Izveidot aktīvu laikā preces saņemšanas vai rēķina grāmatošanas opcijas ļauj izveidot jaunā pamatlīdzekļa "uz fly" grāmatošanas laikā tāpēc, ka tai nav jāiestata kā pamatlīdzekļa pirms darījuma. Pēdējā opcija, Pārbaudīt pamatlīdzekļu izveidošanu rindas ieraksta laikā, attiecas tikai uz pirkšanas pieprasījumiem.

Varat konfigurēt iemesla kodus, lai tie tiktu pieprasīti pamatlīdzekļu izmaiņām vai konkrētam pamatlīdzekļu transakcijām.

Visbeidzot cilnē Numuru sērijas jūs definējat pamatlīdzekļu numuru sērijas. Pamatlīdzekļu numuru sēriju var pārrakstīt ar pamatlīdzekļu grupu numuru sēriju, ja tāda ir norādīta.


