---
title: Pamatlīdzekļu iestatīšana
description: Šajā rakstā ir sniegts apskats par moduļa Pamatlīdzekļi iestatīšanu.
author: moaamer
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3baa842dadddd0f763f803528d322b9561b3141e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910147"
---
# <a name="set-up-fixed-assets"></a>Pamatlīdzekļu iestatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegts pārskats par Pamatlīdzekļu **moduļa iestatīšanu**. 

Parametri kontrolē pamatlīdzekļu vispārīgo darbību. Pamatlīdzekļu grupas jums ļauj grupēt savus līdzekļus un norādīt noklusējuma atribūtus katram grupai piešķirtajam līdzeklim. Pamatlīdzekļu grupām tiek piešķirtas grāmatas. Grāmatas seko līdzi pamatlīdzekļa finansiālajai vērtība laika gaitā, izmantojot nolietojuma tabulā definēto nolietojuma konfigurāciju.

Kad tiek izveidoti pamatlīdzekļi, tie tiek piešķirti kādai grupai. Pēc noklusējuma grāmatas, kuras ir piešķirtas pamatlīdzekļu grupai, pēc tam tiek piešķirtas pamatlīdzeklim. Grāmatas, kuras ir konfigurētas grāmatošanai virsgrāmatā, ir saistītas ar grāmatošanas metodi. Virsgrāmatas konti tiek definēti katrai grāmatai grāmatošanas metodē un tiek izmantoti, kad tiek grāmatotas pamatlīdzekļu transakcijas.

![Pamatlīdzekļu komponenti.](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Nolietojuma tabulas

Vispirms ir jāiestata nolietojuma profili. Nolietojuma tabulā jūs konfigurējat veidu, kādā pamatlīdzekļa vērtība mazinās laika gaitā. Jums ir nepieciešams definēt nolietojuma metodi, nolietojuma aprēķina gadu (kalendāro gadu vai finanšu gadu) un nolietojuma biežumu. Papildinformāciju skatiet tēmā [Nolietojuma profilu iestatīšana un izveide](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Grāmatas

Kad ir iestatītas nolietojuma tabulas, jums saviem līdzekļiem ir jāizveido nepieciešamās grāmatas. Katra grāmata seko līdzi neatkarīgam līdzekļa finansiālajam dzīves ciklam. Grāmatas var konfigurēt saistīto transakciju grāmatošanai virsgrāmatā. Šī konfigurācija ir noklusējuma iestatījums, jo tā parasti tiek izmantota uzņēmuma finanšu pārskatu veidošanai. Grāmatas, kas negrāmato virsgrāmatā, grāmato vienīgi pamatlīdzekļu apakšgrāmatā un parasti tiek izmantotas nodokļu pārskatu veidošanai.

Katrai grāmatai tiek piešķirta primārā nolietojuma tabula. Grāmatām ir arī alternatīvā vai pārslēgšanas nolietojuma tabula, ja šāds tabulas tips ir piemērojams. Lai pamatlīdzekļu grāmatu automātiski iekļautu nolietojuma izpildēs, jums ir jāiespējo opcija **Aprēķināt nolietojumu**. Ja kādam līdzeklim šī opcija nav iespējota, nolietojuma priekšlikums šo līdzekli izlaiž.

Varat iestatīt arī atvasinātās grāmatas. Norādītās atvasinātās transakcijas tiek grāmatotas pret atvasinātajām grāmatām kā primāro transakciju precīza kopija. Tādēļ atvasinātās transakcijas parasti tiek iestatītas iegādēm un norakstīšanām, nevis nolietojuma transakcijām. Plašāku informāciju skatiet [Vērtību modeļu iestatīšana](tasks/set-up-value-models.md).

Lapā **Pamatlīdzekļu parametri** ir pieejama opcija, kas ļauj ieslēgt vai izslēgt bloķēšanas funkcionalitāti. Šis līdzeklis ir iespējots **Līdzekļu pārvaldības darbvietā**.

## <a name="fixed-asset-posting-profiles"></a>Pamatlīdzekļu grāmatošanas metodes

Kad esat iestatījis grāmatas, varat izveidot grāmatošanas metodi. Grāmatošanas metodei ir jābūt definētai pēc grāmatas, bet to var definēt arī detalizētākā līmenī. Piemēram, grāmatošanas metodi varat definēt grāmatas un pamatlīdzekļu grupas kombinācijai vai pat atsevišķai pamatlīdzekļu grāmatai. Pēc noklusējuma definētie virsgrāmatas konti tiek lietoti jūsu pamatlīdzekļu transakcijām.

Jums ir nepieciešams definēt virsgrāmatas kontus, kas tiek izmantoti norakstīšanas procesu laikā — gan norakstīšanas pārdošanām, gan brāķiem. Izslēgšanas laikā iepriekš iegrāmatotās pamatlīdzekļu transakcijas tiek anulētas no sākotnējiem kontiem. Neto summas tiek pārvietotas uz atbilstošo kontu peļņai un zaudējumiem no līdzekļu izslēgšanas. Lai palīdzētu nodrošināt, ka transakcijas tiek anulētas pareizi, jums ir jāiestata konti katram transakcijas tipam, kas tiek izmantots jūsu uzņēmumā. Par galveno kontu ir jānorāda sākotnējais konts, kuru attiecīgajai grāmatošanas metodei iestatījāt šim transakcijas tipam, un par korespondējošo kontu ir jānorāda jūsu peļņas un zaudējumu konts norakstīšanai. Izņēmums ir atlikusī vērtība. Šajā gadījumā gan galvenais konts, gan korespondējošais konts ir jāiestata uz peļņas un zaudējumu kontu norakstīšanai. Papildinformāciju skatiet tēmā [Pamatlīdzekļa grāmatošanas metožu iestatīšana](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Pamatlīdzekļu grupas

Lauks **Pamatlīdzekļu grupa** ir vienīgais obligātais lauks, kad veidojat pamatlīdzekli. Šī lauka vērtība līdzeklim nosaka vairāku informatīvo lauku noklusējuma vērtību. Grāmatas tiek iestatītas tā, lai katram līdzeklim grupā būtu piešķirta noklusējuma grāmata. Šādi grāmatām iestatītie atribūti var attiekties uz līdzekļu grupu. Šie atribūti ietver lietošanas ilguma un nolietojuma aprēķināšanas metodi.

Varat arī definēt speciālā nolietojuma atskaitījumus vai papildnolietojumu konkrētai pamatlīdzekļu grupas un grāmatas kombinācijai. Speciālā nolietojuma atskaitījumiem ir jāpiešķir prioritāte, lai norādītu secību, kādā atskaitījumi tiek aprēķināti, kad grāmatai ir piešķirti vairāki atskaitījumi. Papildinformāciju skatiet tēmā [Pamatlīdzekļu grupu iestatīšana](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Žurnālu nosaukumi

Lapā **Žurnālu nosaukumi** jums jāizveido žurnālu nosaukumi, kas jāizmanto pamatlīdzekļu žurnālam. Lauks **Žurnāla tips** jāiestata uz **Pamatlīdzekļu grāmatošana**. Iestatiet lauku **Dokumentu sērija** tā, lai žurnālu nosaukumi tiktu izmantoti pamatlīdzekļu žurnālam. Pamatlīdzekļu žurnāli nedrīkst izmantot iestatījumu **Tikai 1 dokumenta numurs**, jo vairākiem automatizētajiem procesiem, piemēram, pārsūtījumiem un sadalījumiem, ir nepieciešams unikāls dokumenta numurs.

## <a name="fixed-asset-parameters"></a>Pamatlīdzekļu parametri

Pēdējā šīs procedūras darbība ir atjaunināt pamatlīdzekļu parametrus.

Lauks **Kapitalizācijas slieksnis** nosaka, kuriem pamatlīdzekļiem tiek rēķināts nolietojums. Ja pirkuma rinda ir atzīmēta kā pamatlīdzeklis, bet tā neatbilst norādītajam kapitalizācijas slieksnim, tad pamatlīdzeklis joprojām tiek izveidots vai atjaunināts, bet opcija **Aprēķināt nolietojumu** ir iestatīta uz **Nē**. Tādēļ šim līdzeklim nolietojums netiks automātiski rēķināts kā daļa no nolietojuma priekšlikumiem.

Svarīga opcija ir **Automātiski izveidot nolietojuma korekcijas summas ar izslēgšanu**. Ja šo opciju iestatāt uz **Jā**, līdzekļa nolietojums tiek automātiski koriģēts, pamatojoties uz nolietojuma iestatījumiem līdzekļa izslēgšanas laikā. Cita opcija jums ļauj termiņatlaides atņemt no iegādes summas, kad iegādājaties pamatlīdzekļus, izmantojot kreditora rēķinu.

Parametrs **Bloķēt līdzekļu grāmatas nolietojuma žurnālā** lauj bloķēt līdzekļu grāmatas nolietojuma žurnālā. Kad nolietojuma transakcijas tiek iegrāmatotas, sistēma pārbauda, vai viena un tā pati līdzekļu grāmata nav pievienota vairāk nekā vienam nolietojuma žurnālam. Ja tā ir, tad šī līdzekļu grāmata tiks bloķēta un iegrāmatošana tiks apturēta. Ja līdzekļu grāmatas ID ir bloķētā žurnālā, tas tiks automātiski atbloķēts, kad iegrāmatošana sākotnējā žurnālā tiks pabeigta. Žurnālu var atbloķēt arī manuāli. 

Kopsavilkuma cilnē **Pirkšanas pasūtījumi** varat konfigurēt veidu, kādā līdzekļi tiek izveidoti kā daļa no pirkšanas procesa. Pirmā opcija ir **Atļaut līdzekļu iegādi no pirkšanas**. Ja šo opciju iestatāt uz **Jā**, tad līdzekļa iegāde notiek laikā, kad tiek grāmatots rēķins. Ja šo opciju iestatāt uz **Nē**, pamatlīdzekli joprojām varat norādīt pirkšanas pasūtījumā (PP) un rēķinā, bet iegāde netiek grāmatota. Grāmatošana ir jāveic kā atsevišķa darbība no pamatlīdzekļu žurnāla. Izmantojot opciju **Izveidot līdzekli produktu ieejas plūsmas vai rēķina grāmatošanas laikā**, varat izveidot jaunu līdzekli grāmatošanas laikā. Tādējādi līdzeklis nav jāiestata kā pamatlīdzeklis vēl pirms transakcijas. Pēdējā opcija, **Pārbaudīt pamatlīdzekļu izveidošanu rindas ieraksta laikā**, attiecas tikai uz pirkšanas pieprasījumiem.

Varat konfigurēt iemesla kodus, lai tie tiktu pieprasīti pamatlīdzekļu izmaiņām vai konkrētam pamatlīdzekļu transakcijām.

Visbeidzot — cilnē **Numuru sērijas** jūs definējat pamatlīdzekļu numuru sērijas. **Pamatlīdzekļu** numuru sēriju var pārrakstīt ar **Pamatlīdzekļu grupu** numuru sēriju, ja tāda ir norādīta.

Papildinformāciju skatiet tēmā [Pamatlīdzekļa izveide](tasks/create-fixed-asset.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
