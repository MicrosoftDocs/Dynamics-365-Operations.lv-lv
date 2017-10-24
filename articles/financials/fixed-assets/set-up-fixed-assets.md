---
title: "Pamatlīdzekļu iestatīšana"
description: "Šajā tēmā ir sniegts pārskats par modeļa Pamatlīdzekļi iestatīšanu."
author: twheeloc
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d16c9ca5740c27528d74800957f9b47984c135cd
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fixed-assets"></a>Pamatlīdzekļu iestatīšana

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegts pārskats par modeļa Pamatlīdzekļi iestatīšanu.

<a name="overview"></a>Pārskats
--------
Parametri kontrolē pamatlīdzekļu vispārīgo darbību.

Pamatlīdzekļu grupas jums ļauj grupēt savus līdzekļus un norādīt noklusējuma atribūtus katram grupai piešķirtajam līdzeklim. Pamatlīdzekļu grupām tiek piešķirtas grāmatas. Grāmatas seko līdzi pamatlīdzekļa finansiālajai vērtība laika gaitā, izmantojot nolietojuma tabulā definēto nolietojuma konfigurāciju.

Kad tiek izveidoti pamatlīdzekļi, tie tiek piešķirti kādai grupai. Pēc noklusējuma grāmatas, kuras ir piešķirtas pamatlīdzekļu grupai, pēc tam tiek piešķirtas pamatlīdzeklim. Grāmatas, kuras ir konfigurētas grāmatošanai virsgrāmatā, ir saistītas ar grāmatošanas metodi. Virsgrāmatas konti tiek definēti katrai grāmatai grāmatošanas metodē un tiek izmantoti, kad tiek grāmatotas pamatlīdzekļu transakcijas. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Nolietojuma tabulas
Vispirms jums ir jāiestata nolietojuma tabulas. Nolietojuma tabulā jūs konfigurējat veidu, kādā pamatlīdzekļa vērtība mazinās laika gaitā. Jums ir nepieciešams definēt nolietojuma metodi, nolietojuma aprēķina gadu (kalendāro gadu vai finanšu gadu) un nolietojuma biežumu. Papildinformāciju skatiet šeit: [Nolietojuma profilu iestatīšana un izveide](tasks/set-up-depreciation-profiles.md)

## <a name="books"></a>Grāmatas
Kad ir iestatītas nolietojuma tabulas, jums saviem līdzekļiem ir jāizveido nepieciešamās grāmatas. Katra grāmata seko līdzi neatkarīgam līdzekļa finansiālajam dzīves ciklam. Grāmatas var konfigurēt saistīto transakciju grāmatošanai virsgrāmatā. Šī konfigurācija ir noklusējuma iestatījums, jo tā parasti tiek izmantota uzņēmuma finanšu pārskatu veidošanai. Grāmatas, kas negrāmato virsgrāmatā, grāmato vienīgi pamatlīdzekļu apakšgrāmatā un parasti tiek izmantotas nodokļu pārskatu veidošanai.

Katrai grāmatai tiek piešķirta primārā nolietojuma tabula. Grāmatām ir arī alternatīvā vai pārslēgšanas nolietojuma tabula, ja šāds tabulas tips ir piemērojams. Lai pamatlīdzekļu grāmatu automātiski iekļautu nolietojuma izpildēs, jums ir jāiespējo opcija Aprēķināt nolietojumu. Ja kādam līdzeklim šī opcija nav atlasīta, tad nolietojuma priekšlikums šo līdzekli izlaiž.

Varat iestatīt arī atvasinātās grāmatas. Norādītās atvasinātās transakcijas tiek grāmatotas kā primāro transakciju precīza kopija pret atvasinātajām grāmatām. Tādēļ atvasinātās transakcijas parasti tiek iestatītas iegādēm un norakstīšanām, nevis nolietojuma transakcijām.
Plašāku informāciju skatiet šeit: [Iestatīt grāmatas](tasks/set-up-value-models.md).

## <a name="fixed-asset-posting-profiles"></a>Pamatlīdzekļu grāmatošanas metodes
Kad esat iestatījis grāmatas, varat izveidot grāmatošanas metodi. Grāmatošanas metodei ir jābūt definētai pēc grāmatas, bet to var definēt arī detalizētākā līmenī. Piemēram, grāmatošanas metodi varat definēt grāmatas un pamatlīdzekļu grupas kombinācijai vai pat atsevišķai pamatlīdzekļu grāmatai. Pēc noklusējuma definētie virsgrāmatas konti tiek lietoti jūsu pamatlīdzekļu transakcijām.

Jums ir nepieciešams definēt virsgrāmatas kontus, kas tiek izmantoti norakstīšanas procesu laikā — gan norakstīšanas pārdošanām, gan brāķiem. Norakstīšanas laikā iepriekš iegrāmatotās pamatlīdzekļu transakcijas tiek anulētas no sākotnējiem kontiem un neto summas tiek pārvietotas uz atbilstošo kontu peļņai un zaudējumiem no līdzekļu norakstīšanas. Lai palīdzētu nodrošināt, ka transakcijas tiek anulētas pareizi, jums ir jāiestata konti katram transakcijas tipam, kas tiek izmantots jūsu uzņēmumā. Par galveno kontu ir jānorāda sākotnējais konts, kuru attiecīgajai grāmatošanas metodei iestatījāt šim transakcijas tipam, un par korespondējošo kontu ir jānorāda jūsu peļņas un zaudējumu konts norakstīšanai. Izņēmums ir atlikusī vērtība. Šajā gadījumā gan galvenais konts, gan korespondējošais konts ir jāiestata uz peļņas un zaudējumu kontu norakstīšanai. Plašāku informāciju skatiet šeit: [Pamatlīdzekļa grāmatošanas profilu iestatīšana](tasks/set-up-fixed-asset-posting-profiles.md)

## <a name="fixed-asset-groups"></a>Pamatlīdzekļu grupas
Pamatlīdzekļu grupa ir vienīgais obligātais lauks, kad veidojat pamatlīdzekli. Šī lauka vērtība līdzeklim nosaka vairāku informatīvo lauku noklusējuma vērtību. Grāmatas tiek iestatītas tā, lai katram līdzeklim grupā būtu piešķirta noklusējuma grāmata. Pēc tam grāmatām varat iestatīt atribūtus, kas ir raksturīgas kādai līdzekļu grupai, piemēram, Lietošanas ilgums un Nolietojuma aprēķināšanas metode.

Varat arī definēt speciālā nolietojuma atskaitījumus vai papildnolietojumu konkrētai pamatlīdzekļu grupas un grāmatas kombinācijai. Speciālā nolietojuma atskaitījumiem ir jāpiešķir prioritāte, lai norādītu secību, kādā atskaitījumi tiek aprēķināti, kad grāmatai ir piešķirti vairāki atskaitījumi. Plašāku informāciju skatiet šeit: [Iestatīt pamatlīdzekļu grupas](tasks/set-up-fixed-asset-groups.md)

## <a name="fixed-asset-parameters"></a>Pamatlīdzekļu parametri
Pēdējā šīs procedūras darbība ir atjaunināt pamatlīdzekļu parametrus.

Lauks **Kapitalizācijas slieksnis** nosaka, kuriem pamatlīdzekļiem tiek rēķināts nolietojums. Ja pirkuma rinda ir atzīmēta kā pamatlīdzeklis, bet tā neatbilst norādītajam kapitalizācijas slieksnim, tad pamatlīdzeklis joprojām tiek izveidots vai atjaunināts, bet opcija Aprēķināt nolietojumu ir iestatīta uz Nē. Tādēļ šim līdzeklim nolietojums netiks automātiski rēķināts kā daļa no nolietojuma priekšlikumiem.

Svarīga opcija ir **Automātiski izveidot nolietojuma korekcijas summas ar norakstīšanu**. Ja šo opciju iestatāt uz **Jā**, tad līdzekļa nolietojums tiek pielāgots automātiski, pamatojoties uz nolietojuma uzstādījumiem līdzekļa norakstīšanas laikā. Cita opcija jums ļauj termiņatlaides atņemt no iegādes summas, kad iegādājaties pamatlīdzekļus, izmantojot kreditora rēķinu.

Kopsavilkuma cilnē Pirkšanas pasūtījumi varat konfigurēt veidu, kādā līdzekļi tiek izveidoti kā daļa no pirkšanas procesa. Pirmā opcija ir Atļaut līdzekļu iegādi no pirkšanas. Ja šo opciju iestatāt uz Jā, tad līdzekļa iegāde notiek laikā, kad tiek grāmatots rēķins. Ja šo opciju iestatāt uz Nē, pamatlīdzekli joprojām varat norādīt pirkšanas pasūtījumā (PP) un rēķinā, bet iegāde netiek grāmatota. Grāmatošana ir jāveic kā atsevišķa darbība no pamatlīdzekļu žurnāla. Opcija Izveidot līdzekli produktu ieejas plūsmas vai rēķina grāmatošanas laikā jums ļauj izveidot jaunu līdzekli grāmatošanas laikā, lai tas nebūtu jāiestata kā pamatlīdzeklis vēl pirms transakcijas. Pēdējā opcija, Pārbaudīt pamatlīdzekļu izveidošanu rindas ieraksta laikā, attiecas tikai uz pirkšanas pieprasījumiem.

Varat konfigurēt iemesla kodus, lai tie tiktu pieprasīti pamatlīdzekļu izmaiņām vai konkrētam pamatlīdzekļu transakcijām.

Visbeidzot cilnē Numuru sērijas jūs definējat pamatlīdzekļu numuru sērijas. Pamatlīdzekļu numuru sēriju var pārrakstīt ar pamatlīdzekļu grupu numuru sēriju, ja tāda ir norādīta.

Plašāku informāciju skatiet rakstā [Pamatlīdzekļu izveide](tasks/create-fixed-asset.md).


