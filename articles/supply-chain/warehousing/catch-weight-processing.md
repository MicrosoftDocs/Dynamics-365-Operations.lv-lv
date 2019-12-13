---
title: Pieļaujamā svara preču apstrāde noliktavas pārvaldības ietvaros
description: Šajā tēmā ir aprakstīts, kā izmantot darba veidnes un vietas direktīvas, lai noteiktu noliktavā veikta darba veidu un vietu.
author: perlynne
manager: AnnBe
ms.date: 11/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 5800f95de0ec773f40c506662a031887810b8c92
ms.sourcegitcommit: db222a1719d4756d9ccb73fc71e7eaf4521c23a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696643"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Pieļaujamā svara preču apstrāde noliktavas pārvaldības ietvaros

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pivate-preview-banner.md)]


## <a name="feature-exposure"></a>Līdzekļa pieejamība

Lai izmantotu noliktavas pārvaldības procesus pieļaujamā svara preču apstrādei, šī funkcionalitāte ir jāieslēdz, izmantojot licences konfigurācijas atslēgu. (Pārdejiet uz sadaļu **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**. Pēc tam cilnē **Konfigurācijas atslēgas** izvērsiet sadaļu **Tirdzniecība \> Noliktavas un transportēšanas pārvaldība** un atzīmējiet izvēles rūtiņu **Pieļaujamais svars noliktavā**).

> [!NOTE]
> Ir jāieslēdz arī licences konfigurācijas atslēgas **Noliktavas un transportēšanas pārvaldība** un **Procesa sadale \> Pieļaujamais svars**.

Pēc licences konfigurācijas atslēgas ieslēgšanas, kad izveidojat izlaistu preci, varat atlasīt vienumu **Pieļaujamais svars**. Varat arī saistīt izlaisto preci ar noliktavas dimensiju grupu, kam ir atlasīts parametrs **Izmantot noliktavas vadības procesus**.

Lai preci varētu izmantot noliktavas pārvaldības procesos, vispirms ir jāveic daži precei raksturīgi pieļaujamā svara iestatījumi.

- Vienību konvertēšanas definīcijas ietvaros definējiet nominālā svara konvertēšanu pieļaujamā svara vienībai (kaste) un krājumu vienībai (kilograms \[kg\]).
- Pieļaujamā svara iestatīšanas ietvaros definējiet minimālo un maksimālo svara pielaidi.
- Iestatiet vienību secību grupu, kurā pieļaujamā svara vienība ir definēta kā mazākā noliktavas vienība (SKU).
- Iestatiet pieļaujamā svara krājumu apstrādes politiku.

Papildinformāciju skatiet rakstā [Pieļaujamā svara krājumu iestatīšana un uzturēšana](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Transakciju korekcijas

Tā kā krājumu svars brīdī, kad tie tiek saņemti noliktavā, var atšķirties no krājumu svara brīdī, kad tie tiek izdoti no noliktavas, pieļaujamā svara preču apstrādei ir jānodrošina krājumu regulēšana.

**1. piemērs**

Ražošanas procesa **Reģistrēt pabeigšanu** laikā tiek noteikts, ka tādas ienākošās plūsmas noliktavas vienības svars, kas satur astoņas pieļaujamā svara preces kastes, ir 80,1 kg. Pēc tam noliktavas vienība tiek noglabāta pabeigto preču zonā, un uzglabāšanas perioda laikā tiek zaudēta daļa svara.

Vēlāk, pārdošanas pasūtījuma izdošanas procesa laikā tiek noteikts, ka tās pašas noliktavas vienības svars ir 79,8 kg. Tāpēc tagad sistēmā fizisko dimensiju kopas ietvaros pastāv svara starpība.

Šādā gadījumā sistēma automātiski koriģē starpību, grāmatojot transakciju par trūkstošajiem 0,3 kg.

**2. piemērs**

Preces definīcijā ir iestatīta pieļaujamā svara vienības **Kaste** minimālā svara tolerances vērtība 8 kg un maksimālā svara tolerances vērtība 12 kg.

Jums ir divas šīs preces kastes, un to reģistrētais svars ir 16 kg. Ja noliktavas darbinieks izdod un nosver vienu no kastēm un noteiktais svars ir 9 kg, atlikušās kastes svars ir 7 kg. Taču, tā kā 7 kg ir mazāk nekā minimālais svars, sistēma veic automātisku korekciju, lai palielinātu rīcībā esošo krājumu svaru par 1 kg.

Lai iestatītu kontus, kuros tiek grāmatotas šīs korekcijas, pārejiet uz sadaļu **Izmaksu pārvaldība \> Virsgrāmatas integrācijas politiku iestatīšana \> Grāmatošana**. Pēc tam cilnē **Krājumi** definējiet tālāk norādītos kontus.

- Pieļaujamā svara zaudējumu konts
- Pieļaujamā svara peļņas konts

## <a name="catch-weight-item-handling-policy"></a>Pieļaujamā svara preču pārvietošanas politika

Pieļaujamā svara krājumu apstrādes politikā ir definētas divas galvenās krājumu noliktavas pārvaldības plūsmas: kad tiek noteikts krājumu svars un kā tas tiek noteikts.

Varat definēt, kad tiek noteikts svars pārdošanas un pārsūtīšanas pasūtījumu apstrādes laikā. Svaru var noteikt tālāk norādīto procesu laikā.

- **Izdošana** — svars tiek noteikts pasūtījuma darba sākotnējās izdošanas darba rindu apstrādes laikā.
- **Iepakošana** — svars tiek noteikts manuālās iepakošanas laikā. (Krājumi ir jānosūta uz iepakošanas staciju.)

Ja faktiskais svars tiek noteikts iepakošanas stacijā konteinera iepakošanas procesu laikā, noliktavas darbiniekiem netiek prasīts noteikt svaru izdošanas darba laikā. Tā vietā kā uz iepakošanas zonu nosūtītā izdotā krājuma svars tiek izmantots fizisko krājumu vidējais svars.

Iekšējiem noliktavas pārvaldības procesiem, piemēram, inventarizācijai un korekciju labojumiem, var definēt to, vai ir vai nav jānosaka svars. Ja svars netiek noteikts, tiek izmantots nominālais svars.

Varat arī definēt to, kā tiek noteikts svars. Vienā no divām galvenajām plūsmām tiek izsekotas pieļaujamā svara etiķetes un tās tiek izmantotas svara noteikšanai. Otrā plūsmā pieļaujamā svara etiķetes netiek izsekotas.

- **Jā** — krājumam tiek izmantotas pieļaujamā svara etiķetes. Katram etiķetes numuram atbilst viena pieļaujamā svara vienība (kaste), un ar etiķeti ir saistīts svars un cita informācija. Izejošajās plūsmas procesiem tiek izmantots ar etiķeti saistītais svars.
- **Nē** — krājumam netiek neizmantotas pieļaujamā svara etiķetes. Ienākošās un izejošās plūsmas svēršanas procesiem tiek izmantots faktiskais svars, kas tiek noteikts katra procesa laikā.

Krājumiem, kuru svars nemainīsies uzglabāšanas perioda laikā, var izmantot pieļaujamā svara etiķešu izsekošanas procesu. Svars tiks noteikts tikai ienākošās plūsmas noliktavas procesa laikā. Izejošās plūsmas procesa laikā tiks tikai skenētas pieļaujamā svara etiķetes un izejošās plūsmas transakciju apstrādei tiks izmantots ar etiķetēm saistītais svars.

### <a name="how-to-capture-catch-weight"></a>Pieļaujamā svara noteikšana

Ja tiek izmantota pieļaujamā svara etiķetes izsekošanas metode, katrai saņemtajai pieļaujamā svara vienībai vienmēr ir jāizveido etiķete un katrai etiķetei vienmēr ir jābūt saistītai ar svaru.

Piemēram, tiek izmantota pieļaujamā svara vienība **Kaste** un jūs saņemat vienu paleti ar astoņām kastēm. Šādā gadījumā ir jāizveido astoņas unikālas pieļaujamā svara etiķetes un ar katru etiķeti ir jāsaista svars. Atkarībā no ienākošās plūsmas pieļaujamā svara etiķetes var noteikt visu astoņu kastu svaru un pēc tam ar katru kasti saistīt vidējo svaru vai arī katrai kastei var noteikt unikālu svaru.

Ja netiek izmantota pieļaujamā svara etiķešu izsekošanas metode, var noteikt katras dimensiju kopas (piemēram, katras noliktavas vienības un izsekošanas dimensijas) svaru. Svaru var arī noteikt apkopotajā līmenī, piemēram, piecām noliktavas vienībām (paletēm).

Izejošās plūsmas svara noteikšanas metodēm varat definēt to, vai svēršana tiek veikta katrai pieļaujamā svara vienībai (t.i., kastei) vai svars tiek noteikts izdodamajam daudzumam (piemēram, trīs kastēm). Ņemiet vērā, ka gadījumā, ja tiek izmantota opcija **Nav noteikts**, ražošanas rindas izdošanas un iekšējās kustības procesiem tiek izmantots vidējais svars.

Lai neļautu noliktavas pārvaldības izdošanas procesiem fiksēt svaru, kas var izraisīt pieļaujamā svara peļņas/zaudējumu korekcijas, var izmantot izejošā svara novirzes metodi.

## <a name="supported-scenarios"></a>Atbalstītie scenāriji

Dažas darbplūsmas neatbalsta pieļaujamā svara preču apstrādi noliktavas pārvaldības ietvaros. Pašlaik pastāv tālāk norādītie ierobežojumi.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Pieļaujamā svara preču konfigurēšana noliktavas pārvaldības procesiem

- Pieļaujamā svara produktiem nevar mainīt krājumu noliktavas dimensiju grupu (lai tiem varētu izmantot noliktavas pārvaldības procesus).
- Pieļaujamā svara precēm tiek atbalstīta tikai formulas apstrāde (nevis materiālu komplekts).
- Pieļaujamā svara preces nevar saistīt ar izsekošanas dimensiju grupu, izmantojot dimensiju Īpašnieks.
- Pieļaujamā svara preces nevar izmantot kā pakalpojumus.
- Pieļaujamā svara preces krājumu modeļu grupā var izmantot tikai kā uzkrātās preces.
- Pieļaujamā svara preces nevar izmantot kopā ar izsekošanas funkcionalitāti Aktīvs pārdošanas procesā.
- Pieļaujamā svara preces nevar izmantot kopā ar sērijas numuru noteikšanas funkcionalitāti. Tāpēc izdošanas/iepakošanas procesa ietvaros preču tukšo vērtību nevar aizstāt ar sērijas numuru.
- Pieļaujamā svara preces nevar izmantot kopā ar sērijas numuru reģistrēšanas pirms patēriņa funkcionalitāti.
- Pieļaujamā svara preces, kam ir iespējoti varianti, nevar izmantot kopā ar variantu mērvienību pārveidošanas funkcionalitāti.
- Pieļaujamā svara preces nevar atzīmēt kā mazumtirdzniecība preču komplektu.
- Pieļaujamā svara preces var izmantot tikai kopā ar vienību secību grupu, kurā ir ietvertas pieļaujamā svara apstrādes vienības un pieļaujamā svara vienībai ir zemākajā pozīcijā sērijā.
- Pieļaujamā svara precēm pārveidošanu no krājumu vienībām uz pieļaujamā svara vienībām var veikt tikai tad, ja pārveidošanas rezultāts ir nominālais daudzums, kas ir lielāks nekā 1.
- Pieļaujamā svara preču svītrkodu iestatīšanas laikā netiek neatbalsta mainīga svara iestatīšana.
 
### <a name="order-processing"></a>Pasūtījuma apstrādāšana

- Iepriekšēja paziņojuma par nosūtīšanu (IPPN/iepakošanas struktūras) izveides laikā netiek atbalstīta informācija par svaru.
- Pasūtījuma daudzums ir jāuztur, pamatojoties uz pieļaujamā svara vienību.
 
### <a name="inbound-warehouse-processing"></a>Ienākošās plūsmas apstrāde noliktavā

- Saņemot noliktavas vienības, reģistrācijas laikā ir jāpiešķir svars, jo iepriekšējā paziņojumā par nosūtīšanu nav ietverta informācija par svaru. Ja tiek izmantoti pieļaujamā svara etiķešu procesi, katrai pieļaujamā svara vienībai ir manuāli jāpiešķir etiķete.
 
### <a name="inventory-and-warehouse-operations"></a>Krājumu un noliktavas darbības

- Pieļaujamā svara precēm netiek atbalstīta manuāla karantīnas pasūtījumu izveide.
- Pieļaujamā svara precēm netiek atbalstīta ar darbu saistīta manuāla krājumu pārvietošana.
- Pieļaujamā svara precēm netiek atbalstīta noliktavas vienības ielāde, lai inicializētu noliktavas krājumus.
- Pieļaujamā svara precēm netiek atbalstīti partijas līdzsvarošanas procesi.
- Pieļaujamā svara precēm netiek atbalstīta negatīva fizisko krājumu daudzuma apstrāde.
- Pieļaujamā svara precēm nevar izmantot krājumu iezīmēšanu.
 
### <a name="outbound-warehouse-processing"></a>Izejošās plūsmas apstrāde noliktavā

- Pieļaujamā svara precēm netiek atbalstīta klastera izdošanas funkcionalitāte.
- Pieļaujamā svara precēm netiek atbalstīta izdošanas un iepakošanas apstrāde noliktavā.
- Pieļaujamā svara precēm var automātiski izpildīt darbu, kas ir definēts darba veidnē.
- Pieļaujamā svara precēm netiek atbalstīta tāda manuāla apstrāde iepakošanas stacijā, kuras ietvaros darbs tiek izveidots pēc konteineru slēgšanas.
- Pieļaujamā svara precēm netiek atbalstīta atsevišķu vienību skenēšanas funkcionalitāte.
 
### <a name="production-processing"></a>Apstrāde ražošanas ietvaros

- Pieļaujamā svara precēm tiek atbalstīti tikai formulas preču partijas pasūtījumi.
- Pieļaujamā svara precēm netiek atbalstīta Kanban funkcionalitāte.
- Pieļaujamā svara precēm pirms patēriņa nevar reģistrēt sērijas numurus.
- Pieļaujamā svara precēm netiek atbalstīta noliktavas vienības atsaukšanas funkcionalitāte.
- Pieļaujamā svara precēm pabeigšanu nevar reģistrēt pēc sērijas numura.

### <a name="transportation-management-processing"></a>Apstrāde transportēšanas pārvaldības ietvaros

- Pieļaujamā svara precēm netiek atbalstīta apstrāde, izmantojot noslodzes plānošanas rīku.
- Pieļaujamā svara precēm netiek atbalstītas transporta pieprasījuma rindas.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Citi ierobežojumi un darbības saistībā ar pieļaujamā svara preču apstrādi noliktavas pārvaldības ietvaros

- Tādu izdošanas procesu laikā, kuru ietvaros lietotājam netiek prasīts norādīt izsekošanas dimensijas, svara piešķiršana tiek veikta, pamatojoties uz vidējo svaru. Šī darbība notiek tad, ja, piemēram, vienā vietā tiek izmantotas vairākas izsekošanas dimensijas un pēc tam, kad lietotājs ir apstrādājis izdošanu, šajā vietā ir palikusi tikai viena izsekošanas dimensijas vērtība.
- Ja tiek rezervēti tādas pieļaujamā svara preces krājumi, kas ir konfigurēta noliktavas pārvaldības procesiem, rezervēšana tiek veikta, pamatojoties uz definēto minimālo svaru pat tad, ja šis daudzums ir vienāds ar pēdējo rīcībā esošo krājumu apstrādājamo daudzumu. Šī darbība atšķiras no darbības, kas tiek izmantota krājumiem, kuri nav konfigurēti noliktavas pārvaldības procesiem.
- Procesiem, kuru ietvaros noslodzes aprēķinam tiek izmantots svars (kopuma sliekšņiem, maksimālajiem darba pārtraukumiem, konteinera maksimālajām vērtībām, vietu noslodzei utt.), netiek izmantots faktiskais krājumu svars. Tā vietā, procesi tiek veikti, pamatojoties uz precei definēto fiziskās apstrādes svaru.
- Kopumā pieļaujamā svara precēm netiek atbalstīta mazumtirdzniecības funkcionalitāte.
 
### <a name="catch-weight-tags"></a>Pieļaujamā svara etiķetes

Pašlaik pieļaujamā svara etiķešu funkcionalitāte tiek atbalstīta tikai tālāk norādīto scenāriju ietvaros.

- Kad tiek apstrādāts pirkšanas pasūtījums, izmantojot noliktavas programmu.
- Kad tiek pastrādāta kravas saņemšana, izmantojot noliktavas programmu.
- Ar pirkšanas pasūtījuma kravu saistītas noliktavas vienības saņemšanas procesa laikā tiek pieprasīta svara piešķire. Turpretim ar pārsūtīšanas pasūtījumu saistītai saņemšanai tiek izmantots pārsūtīšanas pasūtījuma sūtījuma datos ietvertais svars.
- Pārsūtīšanas pasūtījuma krājuma un rindu saņemšanai no noliktavas, kas nav saistīta ar noliktavas pārvaldības procesu.
- Ar pārdoto preču atgriešanas pasūtījumu saistītas saņemšanas apstrādes ietvaros var tikt reģistrētas pieļaujamā svara etiķetes, taču apstrāde netiek validēta, ja tās ir tās pašas etiķetes, kas tika sākotnēji nosūtītas atbilstoši noteiktai pārdošanas pasūtījuma rindai.
- Kad tiek apstrādāts krājumu statuss, kas ir izmainīts, izmantojot noliktavas programmu.
- Kad tiek veikta starpnoliktavu pārsūtīšana, izmantojot noliktavas programmu.
- Kad tiek apstrādātas ienākošās un izejošās plūsmas korekcijas, izmantojot noliktavas programmu.
- Kad tiek apstrādāts pārdošanas, pārsūtīšanas un ražošanas līniju izdošanas darbs.
- Kad izdotais daudzums tiek atskaitīts no kravas rindām neatkarīgi no tā, vai tiek izmantoti konteineri.
- Kad preces tiek iepakotas konteineros iepakošanas stacijā.
- Kad konteineri tiek atkārtoti atvērti.
- Kad tiek reģistrēta formulas preču pabeigšana, izmantojot noliktavas programmu.
- Kad tiek apstrādātas transporta kravas, izmantojot noliktavas programmu.

Pieļaujamā svara etiķeti var izveidot, izmantojot noliktavas programmas procesu, manuāli izveidot veidlapā vai izveidot, izmantojot datu elementu procesu. Ja pieļaujamā svara etiķete tiek saistīta ar ienākošā pirmdokumenta rindu, piemēram, pirkšanas pasūtījuma rindu, etiķete tiek reģistrēta. Ja rinda tiek izmantota izejošajai apstrādei. Etiķete tiek atjaunināta kā nosūtīta.
