---
title: Pieļaujamā svara preču apstrāde noliktavas pārvaldības ietvaros
description: Šajā tēmā ir aprakstīts, kā izmantot darba veidnes un vietas direktīvas, lai noteiktu noliktavā veikta darba veidu un vietu.
author: perlynne
manager: tfehr
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy, TMSLoadBuildWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 710446db7746ed3cd3fb9754caeaa15fd2f76641
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433139"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Pieļaujamā svara preču apstrāde noliktavas pārvaldības ietvaros

[!include [banner](../includes/banner.md)]


## <a name="feature-exposure"></a>Līdzekļa pieejamība

Lai izmantotu noliktavas pārvaldības procesus pieļaujamā svara preču apstrādei, šī funkcionalitāte ir jāieslēdz, izmantojot licences konfigurācijas atslēgu. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**. Pēc tam cilnē **Konfigurācijas atslēgas** izvērsiet sadaļu **Tirdzniecība \> Noliktavas un transportēšanas pārvaldība** un atzīmējiet izvēles rūtiņu **Pieļaujamais svars noliktavā**.

> [!NOTE]
> Ir jāieslēdz arī licences konfigurācijas atslēgas **Noliktavas un transportēšanas pārvaldība** un **Procesa sadale \> Pieļaujamais svars**. Lai iestatītu konfigurācijas atslēgas pieļaujamajam svaram, ir jāieslēdz arī līdzeklis, izmantojot darbvietu **Funkciju pārvaldība**. Galvenais līdzeklis, kas ir jāieslēdz, ir **Pieļaujamā preces svara apstrāde ar noliktavas pārvaldību**. Divas saistītas, bet neobligātās funkcijas, kuras varētu vēlēties ieslēgt, ir **Krājumu statusa izmaiņas pieļaujamā svara precēm** un **Izmantot esošās pieļaujamā svara birkas, ziņojot atskaitoties par ražošanas pasūtījumiem kā pabeigtiem**.

Pēc licences konfigurācijas atslēgas ieslēgšanas, kad izveidojat izlaistu preci, varat atlasīt vienumu **Pieļaujamais svars**. Varat arī saistīt izlaisto preci ar noliktavas dimensiju grupu, kam ir atlasīts parametrs **Izmantot noliktavas vadības procesus**.

Lai preci varētu izmantot noliktavas pārvaldības procesos, vispirms ir jāveic daži precei raksturīgi pieļaujamā svara iestatījumi.

- Vienību konvertēšanas definīcijas ietvaros definējiet nominālā svara konvertēšanu pieļaujamā svara vienībai (kaste) un krājumu vienībai (kilograms \[kg\]).
- Pieļaujamā svara iestatīšanas ietvaros definējiet minimālo un maksimālo svara pielaidi.
- Iestatiet vienību secību grupu, kurā pieļaujamā svara vienība ir definēta kā mazākā noliktavas vienība (SKU).
- Iestatiet pieļaujamā svara krājumu apstrādes politiku.

Papildinformāciju skatiet rakstā [Pieļaujamā svara krājumu iestatīšana un uzturēšana](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Transakciju korekcijas

Tā kā krājumu svars brīdī, kad tie tiek saņemti noliktavā, var atšķirties no krājumu svara brīdī, kad tie tiek izdoti no noliktavas, pieļaujamā svara preču apstrādei ir jānodrošina krājumu regulēšana.

> [!NOTE]
> Mobilās ierīces darbība izraisīs transakcijas korekcijas tikai tad, ja preces pieļaujamā svara izejošā svara novirzes metode, kas saistīta ar apstrādes politiku ir **Atļauta svara novirze**.

**1. piemērs**

Ražošanas procesa **Reģistrēt pabeigšanu** laikā tiek noteikts, ka tādas ienākošās plūsmas noliktavas vienības svars, kas satur astoņas pieļaujamā svara preces kastes, ir 80,1 kg. Pēc tam noliktavas vienība tiek noglabāta pabeigto preču zonā, un uzglabāšanas perioda laikā tiek zaudēta daļa svara.

Vēlāk, pārdošanas pasūtījuma izdošanas procesa laikā tiek noteikts, ka tās pašas noliktavas vienības svars ir 79,8 kg. Tāpēc tagad sistēmā fizisko dimensiju kopas ietvaros pastāv svara starpība.

Šādā gadījumā sistēma automātiski koriģē starpību, grāmatojot transakciju par trūkstošajiem 0,3 kg.

**2. piemērs**

Preces definīcijā ir iestatīta pieļaujamā svara vienības **Kaste** minimālā svara tolerances vērtība 8 kg un maksimālā svara tolerances vērtība 12 kg.

Jums ir divas šīs preces kastes, un to reģistrētais svars ir 16 kg. Ja noliktavas darbinieks izdod un nosver vienu no kastēm un noteiktais svars ir 9 kg, atlikušās kastes svars ir 7 kg. Taču, tā kā 7 kg ir mazāk nekā minimālais svars, sistēma veic automātisku korekciju, lai palielinātu rīcībā esošo krājumu svaru par 1 kg.

Lai iestatītu kontus, kuros tiek grāmatotas šīs korekcijas, pārejiet uz sadaļu **Izmaksu pārvaldība \> Virsgrāmatas integrācijas politiku iestatīšana \> Grāmatošana**. Pēc tam cilnē **Krājumi** definējiet tālāk norādītos kontus.

- Pieļaujamā svara zaudējumu konts
- Pieļaujamā svara peļņas konts

## <a name="catch-weight-item-handling-policy"></a>Pieļaujamā svara preču pārvietošanas politika

Pieļaujamā svara krājumu apstrādes politikā ir definētas divas galvenās krājumu noliktavas pārvaldības plūsmas: kad tiek noteikts krājumu svars un kā tas tiek noteikts.

Varat definēt, kad tiek noteikts svars pārdošanas un pārsūtīšanas pasūtījumu apstrādes laikā. Svaru var noteikt tālāk norādīto procesu laikā.

- **Izdošana** — svars tiek noteikts pasūtījuma darba sākotnējās izdošanas darba rindu apstrādes laikā.
- **Iepakošana** — svars tiek noteikts manuālās iepakošanas laikā. (Krājumi ir jānosūta uz iepakošanas staciju.)

Ja faktiskais svars tiek noteikts iepakošanas stacijā konteinera iepakošanas procesu laikā, noliktavas darbiniekiem netiek prasīts noteikt svaru izdošanas darba laikā. Tā vietā kā uz iepakošanas zonu nosūtītā izdotā krājuma svars tiks izmantots fizisko krājumu vidējais svars. Šī koncepcija attiecas arī uz pieļaujamā svara precēm, kas tiek izsekotas ar etiķetēm. Etiķešu izsekotajām precēm šie parametri nosaka, kad etiķete tiek fiksēta. Šo etiķeti var fiksēt vai nu paņemšanas laikā, izmantojot mobilo ierīci, vai manuālās iepakošanas laikā.

> [!NOTE]
> Tā kā opcija **Iepakošana** izraisa krājumu atjaunināšanu ar vidējo izvēlēto svaru, tas var izraisīt neatbilstību, kas var izraisīt pieļaujamā svara peļņas/zaudējumu korekciju un/vai starpību starp rīcībā esošo krājumu svaru un pieļaujamā svara etiķetes svaru.

Iekšējiem noliktavas pārvaldības procesiem, piemēram, inventarizācijai un korekciju labojumiem, jūs varat definēt to, vai ir vai nav jānosaka svars. Ja svars netiek noteikts, tiek izmantots nominālais svars. Citas opcijas ļauj fiksēt svaru pēc pieļaujamā svara vienības un pēc uzskaites daudzuma.

Varat arī definēt to, kā tiek noteikts svars. Vienā no divām galvenajām plūsmām tiek izsekotas pieļaujamā svara etiķetes un tās tiek izmantotas svara noteikšanai. Otrā plūsmā pieļaujamā svara etiķetes netiek izsekotas.

- **Jā** — krājumam tiek izmantotas pieļaujamā svara etiķetes. Katram etiķetes numuram atbilst viena pieļaujamā svara vienība (kaste), un ar etiķeti ir saistīts svars un cita informācija. Izejošajās plūsmas procesiem tiek izmantots ar etiķeti saistītais svars.
- **Nē** — krājumam netiek neizmantotas pieļaujamā svara etiķetes. Ienākošās un izejošās plūsmas svēršanas procesiem tiek izmantots faktiskais svars, kas tiek noteikts katra procesa laikā.

Krājumiem, kuru svars nemainīsies uzglabāšanas perioda laikā, var izmantot pieļaujamā svara etiķešu izsekošanas procesu. Svars tiks noteikts tikai ienākošās plūsmas noliktavas procesa laikā. Izejošās plūsmas procesa laikā tiks tikai skenētas pieļaujamā svara etiķetes un izejošās plūsmas transakciju apstrādei tiks izmantots ar etiķetēm saistītais svars.

Vēl viens svarīgs parametrs, kas saistīts ar pieļaujamā svara etiķešu apstrādi, ir **Pieļaujamā svara etiķetes izmēru izsekošanas metode**. Etiķetes var būt daļēji izsekotas vai pilnībā izsekotas. Ja etiķete tiek daļēji izsekota, tā izseko preces dimensijas, izsekošanas dimensijas un krājumu statusu. Ja etiķete tiek pilnībā izsekota, tā izseko preces dimensijas, izsekošanas dimensijas un **visas** noliktavas dimensijas.

Turklāt, ja prece tiek izsekota ar etiķeti, pastāv parametrs **Izejošo etiķešu fiksēšanas metode**. Varat iestatīt šo parametru, lai jūs vienmēr saņemtu uzvedni par etiķeti izejošajām transakcijām no mobilās ierīces. Alternatīvi varat iestatīt parametru, lai jūs saņemtu uzvedni par etiķetēm tikai tad, kad tās ir nepieciešamas. Piemēram, dotajai numura zīmei krājumā ir piecas pieļaujamā svara etiķetes un jūs esat norādījis, ka vēlaties paņemt visas piecas etiķetes no numura zīmes. Šajā gadījumā, ja parametrs **Izejošo etiķešu fiksēšanas metode** ir iestatīts uz **Pieprasīt etiķeti tikai tad, kad tā ir nepieciešama**, piecas etiķetes tiek atlasītas automātiski. Nav nepieciešams skenēt katru etiķeti. Ja parametrs ir iestatīts uz **Vienmēr pieprasīt etiķeti**, ir jāpārbauda katra etiķete, pat ja visas piecas etiķetes tiek atlasītas.

> [!NOTE]
> Kā likums, etiķetes tiek fiksētas un atjauninātas tikai no mobilās ierīces izvēlnes vienumiem. Tomēr ir daži scenāriji, kuros etiķetes tiek fiksētas citur (piemēram, no manuālās iepakošanas stacijas). Tomēr parasti mobilās ierīces izvēlnes vienumi ir jāizmanto visām noliktavas darbībām, ja tiek izmantotas etiķetes.

### <a name="how-to-capture-catch-weight"></a>Pieļaujamā svara noteikšana

**Ja tiek izmantota pieļaujamā svara etiķetes izsekošanas metode**, katrai saņemtajai pieļaujamā svara vienībai vienmēr ir jāizveido etiķete un katrai etiķetei vienmēr ir jābūt saistītai ar svaru.

Piemēram, tiek izmantota pieļaujamā svara vienība **Kaste** un jūs saņemat vienu paleti ar astoņām kastēm. Šādā gadījumā ir jāizveido astoņas unikālas pieļaujamā svara etiķetes un ar katru etiķeti ir jāsaista svars. Atkarībā no ienākošās plūsmas pieļaujamā svara etiķetes var noteikt visu astoņu kastu svaru un pēc tam ar katru kasti saistīt vidējo svaru vai arī katrai kastei var noteikt unikālu svaru.
Lietojot līdzekli **Izmantot esošās pieļaujamā svara birkas, atskaitoties par ražošanas pasūtījumiem kā pabeigtiem**, ar procesu, kas iespējots, izmantojot mobilās ierīces izvēlnes elementu, krājumi tiek atjaunināti, pamatojoties uz esošo pieļaujamā svara birkas informāciju. Tāpēc noliktavas programma neprasa, lai tiktu tvertas pieļaujamā svara etiķetes kā daļa no ražošanas pārskata kā pabeigtas darbības.

**Ja netiek izmantota pieļaujamā svara etiķešu izsekošanas metode**, var noteikt katras dimensiju kopas (piemēram, katras noliktavas vienības un izsekošanas dimensijas) svaru. Svaru var arī noteikt apkopotajā līmenī, piemēram, piecām noliktavas vienībām (paletēm).

Metodēm, kas fiksē izejošo svaru, opcija **Pēc katras pieļaujamā svara vienības** ļauj norādīt, ka svēršana jāveic katrai pieļaujamā svara vienībai (piemēram, par katru kasti). Opcija **Pēc paņemšanas vienības** ļauj norādīt, ka svars ir jāuztver, pamatojoties uz daudzumu, kas tiks paņemts (piemēram, trīs kastes). Ņemiet vērā, ka gadījumā, ja tiek izmantota opcija **Nav noteikts**, ražošanas rindas izdošanas un iekšējās kustības procesiem tiek izmantots vidējais svars.

Vairākas svara fiksēšanas metodes ir definētas pieļaujamā svara preces apstrādes politikā. Katru svara fiksēšanas metodes parametru izmanto dažādas transakcijas. Tālāk esošajā tabulā ir apkopots, kurus parametrus izmanto katra transakcija.

| Metode                                     | Darījums                                |
|--------------------------------------------|--------------------------------------------|
| Izejošo sūtījumu svara fiksēšanas metode           | Pārdošanas izdošana, pārsūtīšanas izdošana            |
| Ražošanas izdošanas svara fiksēšanas metode | Ražošanas izdošana, ražošanas patēriņš |
| Kustības svara fiksēšanas metode           | Kustība                                   |
| Kad fiksēt svara labošanu       | Korekcijas, uzskaite                      |
| Uzskaites svara fiksēšanas metode           | Inventarizācija                                   |
| Noliktavas pārsūtīšanas svara fiksēšanas metode | Starpnoliktavu pārsūtīšana                         |

Lai neļautu noliktavas pārvaldības izdošanas procesiem fiksēt svaru, kas var izraisīt pieļaujamā svara peļņas/zaudējumu korekcijas, jūs varat izmantot izejošā svara novirzes metodi. Izejošā svara novirzes metode ir spēkā šādos mobilās ierīces procesos: pārdošanas izdošana, pārsūtīšanas izdošana, ražošanas izdošana, kustības, uzskaite un noliktavas pārsūtījumi. Varat izmantot opciju **Ierobežot svara novirzes**, ja pieļaujamā svara vienības svars nemainās noliktavas glabāšanas laikā un ja nav nepieciešamas pieļaujamā svara peļņas/zaudējumu korekcijas. Varat izmantot opciju **Atļaut svara novirzes**, ja svars var svārstīties un ja tiek pieprasītas pieļaujamā svara peļņas/zaudējumu korekcijas, kad tiek ierakstīta svara svārstība.

## <a name="unsupported-scenarios"></a>Neatbalstītie scenāriji

Dažas darbplūsmas neatbalsta pieļaujamā svara preču apstrādi noliktavas pārvaldības ietvaros. Pašlaik pastāv tālāk norādītie ierobežojumi. Tās attiecas uz visām pieļaujamā svara precēm neatkarīgi no tā, vai tās ir ar etiķetēm.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Pieļaujamā svara preču konfigurēšana noliktavas pārvaldības procesiem

- Pieļaujamā svara precēm tiek atbalstīta tikai formulas apstrāde (nevis materiālu komplekts).
- Pieļaujamā svara preces nevar saistīt ar izsekošanas dimensiju grupu, izmantojot dimensiju Īpašnieks.
- Pieļaujamā svara preces nevar izmantot kā pakalpojumus.
- Pieļaujamā svara preces krājumu modeļu grupā var izmantot tikai kā uzkrātās preces.
- Pieļaujamā svara preces nevar izmantot kopā ar izsekošanas funkcionalitāti Aktīvs pārdošanas procesā.
- Pieļaujamā svara preces nevar izmantot kopā ar sērijas numuru noteikšanas funkcionalitāti. Tāpēc izdošanas/iepakošanas procesa ietvaros preču tukšo vērtību nevar aizstāt ar sērijas numuru.
- Pieļaujamā svara preces nevar izmantot kopā ar sērijas numuru reģistrēšanas pirms patēriņa funkcionalitāti.
- Pieļaujamā svara preces, kam ir iespējoti varianti, nevar izmantot kopā ar variantu mērvienību pārveidošanas funkcionalitāti.
- Pieļaujamā svara preces nevar atzīmēt kā komercijas preču komplektu.
- Pieļaujamā svara preces var izmantot tikai kopā ar vienību secību grupu, kurā ir ietvertas pieļaujamā svara apstrādes vienības un pieļaujamā svara vienībai ir zemākajā pozīcijā sērijā.
- Pieļaujamā svara precēm pārveidošanu no krājumu vienībām uz pieļaujamā svara vienībām var veikt tikai tad, ja pārveidošanas rezultāts ir nominālais daudzums, kas ir lielāks nekā 1.
- Pieļaujamā svara preču svītrkodu iestatīšanas laikā netiek neatbalsta mainīga svara iestatīšana.

### <a name="order-processing"></a>Pasūtījuma apstrādāšana

- Iepriekšēja paziņojuma par nosūtīšanu (IPPN/iepakošanas struktūras) izveides laikā netiek atbalstīta informācija par svaru.
- Pasūtījuma daudzums ir jāuztur, pamatojoties uz pieļaujamā svara vienību.

### <a name="inbound-warehouse-processing"></a>Ienākošās plūsmas apstrāde noliktavā

- Saņemot noliktavas vienības, reģistrācijas laikā ir jāpiešķir svars, jo iepriekšējā paziņojumā par nosūtīšanu nav ietverta informācija par svaru. Ja tiek izmantoti pieļaujamā svara etiķešu procesi, katrai pieļaujamā svara vienībai ir manuāli jāpiešķir etiķete.
- Ienākošo preču kvalitātes pārbaudes darbs netiek atbalstīts pieļaujamā svara precēm. Ja konfigurēts, kvalitātes pārbaudes darbs tiks izlaists.

### <a name="inventory-and-warehouse-operations"></a>Krājumu un noliktavas darbības

- Pieļaujamā svara precēm netiek atbalstīta manuāla karantīnas pasūtījumu izveide.
- Pieļaujamā svara precēm netiek atbalstīta ar atvērto darbu saistīta manuāla krājumu pārvietošana.
- Pieļaujamā svara precēm netiek atbalstīta noliktavas vienības ielāde, lai inicializētu noliktavas krājumus.
- Pieļaujamā svara precēm netiek atbalstīti partijas līdzsvarošanas procesi.
- Pieļaujamā svara precēm netiek atbalstīta negatīva fizisko krājumu daudzuma apstrāde.
- Pieļaujamā svara precēm nevar izmantot krājumu iezīmēšanu.

### <a name="outbound-warehouse-processing"></a>Izejošās plūsmas apstrāde noliktavā

- Pieļaujamā svara precēm netiek atbalstīta klastera izdošanas funkcionalitāte.
- Pieļaujamā svara precēm netiek atbalstīta izdošanas un iepakošanas apstrāde noliktavā.
- Pieļaujamā svara precēm nevar automātiski izpildīt darbu, kas ir definēts darba veidnē.
- Pieļaujama svara precēm sistēma neatbalsta manuālu iepakošanas staciju apstrādi, ja pēc konteineru aizvēršanas tiek radīts iepakotu konteineru izdošanas darbs.
- Pieļaujamā svara precēm netiek atbalstīta atsevišķu vienību skenēšanas funkcionalitāte.

### <a name="production-processing"></a>Apstrāde ražošanas ietvaros

- Pieļaujamā svara precēm tiek atbalstīti tikai formulas preču partijas pasūtījumi.
- Pieļaujamā svara precēm netiek atbalstīta Kanban funkcionalitāte.
- Pieļaujamā svara precēm pirms patēriņa nevar reģistrēt sērijas numurus.
- Pieļaujamā svara precēm netiek atbalstīta numura zīmju nomaiņa no ražošanas funkcionalitātes.
- Pieļaujamā svara precēm pabeigšanu nevar reģistrēt pēc sērijas numura.

### <a name="transportation-management-processing"></a>Apstrāde transportēšanas pārvaldības ietvaros

- Pieļaujamā svara precēm netiek atbalstīta apstrāde, izmantojot noslodzes plānošanas rīku.
- Pieļaujamā svara precēm netiek atbalstītas transporta pieprasījuma rindas.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Citi ierobežojumi un darbības saistībā ar pieļaujamā svara preču apstrādi noliktavas pārvaldības ietvaros

- Tādu izdošanas procesu laikā, kuru ietvaros lietotājam netiek prasīts norādīt izsekošanas dimensijas, svara piešķiršana tiek veikta, pamatojoties uz vidējo svaru. Šī darbība notiek tad, ja, piemēram, vienā vietā tiek izmantotas vairākas izsekošanas dimensijas un pēc tam, kad lietotājs ir apstrādājis izdošanu, šajā vietā ir palikusi tikai viena izsekošanas dimensijas vērtība.
- Ja tiek rezervēti tādas pieļaujamā svara preces krājumi, kas ir konfigurēta noliktavas pārvaldības procesiem, rezervēšana tiek veikta, pamatojoties uz definēto minimālo svaru pat tad, ja šis daudzums ir vienāds ar pēdējo rīcībā esošo krājumu apstrādājamo daudzumu. Šī darbība atšķiras no darbības, kas tiek izmantota krājumiem, kuri nav konfigurēti noliktavas pārvaldības procesiem. Šim ierobežojumam ir viens izņēmums. Ražošanas izdošanai, kad pēdējais izdotais pieļaujamā svara preču daudzums, kuru kontrolē sērijas numurs, tiek izmantots faktiskais svars.
- Procesiem, kuru ietvaros noslodzes aprēķinam tiek izmantots svars (kopuma sliekšņiem, maksimālajiem darba pārtraukumiem, konteinera maksimālajām vērtībām, vietu noslodzei utt.), netiek izmantots faktiskais krājumu svars. Tā vietā, procesi tiek veikti, pamatojoties uz precei definēto fiziskās apstrādes svaru.
- Kopumā pieļaujamā svara precēm netiek atbalstīta komercijas funkcionalitāte.
- Pieļaujamā svara precēm krājumu statusu nevar atjaunināt no **Noliktavas statusa izmaiņām**.

### <a name="catch-weight-tags"></a>Pieļaujamā svara etiķetes

Pieļaujamā svara etiķeti var izveidot, izmantojot noliktavas programmas procesu, to var manuāli izveidot veidlapā vai izveidot, izmantojot datu elementa procesu. Ja pieļaujamā svara etiķete tiek saistīta ar ienākošā pirmdokumenta rindu, piemēram, pirkšanas pasūtījuma rindu, etiķete tiek reģistrēta. Ja rinda tiek izmantota izejošai apstrādei, etiķete tiks atjaunināta, kad būs nosūtīta.

Papildu ierobežojumiem, kas pašlaik attiecas uz pieļaujamā svara precēm, pieļaujamā svara precēm, kas ir ar etiķetēm, ir citi ierobežojumi, kas pašlaik tiek piemēroti.

- Visi krājumu manuālie atjauninājumi (t. i., atjauninājumi, kas nav veikti, izmantojot mobilo ierīci), ir jāiekļauj atbilstošos manuālos atjauninājumus piesaistītajām pieļaujamā svara etiķetēm, jo šie atjauninājumi netiek automātiski veikti. Piemēram, manuālo korekciju žurnāli atjauninās krājumus, bet ne saistītās pieļaujamā svara etiķetes.
- Lai atspoguļotu papildināšanas darba kustības, ir manuāli jāatjaunina pieļaujamā svara etiķetes. Tas ir tāpēc, ka sistēma nevar fiksēt svaru, kamēr tiek apstrādāti papildināšanas darbi, tāpēc tā vietā ieraksta vidējo svaru.
- Jauktu noliktavas vienību saņemšana netiek atbalstīta pieļaujamā svara precēm ar etiķetēm.
- Pārdošanas atgriešanas pasūtījuma saņemšanas apstrāde var ierakstīt pieļaujamā svara etiķetes. Tomēr process neatspēko, ka atgrieztā etiķete ir tā pati etiķete, kas sākotnēji tika nosūtīta pārdošanas pasūtījumam.
- Mobilās ierīces izvēlnes vienums, kam ir aktivitātes kods **Reģistrēt materiālu patēriņu**, pašlaik neatbalsta pieļaujamā svara etiķešu ierakstīšanu.
- Kaut arī uzskaites procesi ir atbalstīti pieļaujamā svara precēm ar etiķetēm, tie ir ierobežoti. Piemēram, varat izmantot mobilās ierīces opcijas, lai skaitītu pieļaujamā svara preces ar etiķetēm, un tiek izmantots vidējais svars. Tomēr pieļaujamā svara etiķetes netiek automātiski atjauninātas pēc uzskaites transakcijas. Kad uzskaites transakcija ir pabeigta, pieļaujamā svara etiķetes ir manuāli jāatjaunina, lai tās atspoguļotu krājumus. Ja preces, kas sākotnēji nebija vietā, tiek ieskaitītas šajā vietā, tiek izmantots nominālais svars.
- Numura zīmes konsolidācija pašlaik neatbalsta pieļaujamā svara preces ar etiķetēm.
- Atsaukšanas darba funkcionalitāte netiek atbalstīta pieļaujamā svara precēm, kuras tiek izsekotas ar etiķetes numuru.

> [!NOTE]
> Iepriekš sniegtā informācija par pieļaujamā svara etiķetēm ir derīga tikai tad, ja pieļaujamā svara precei ir pieļaujamā svara etiķetes dimensiju izsekošanas metode, kas ir pilnībā izsekota (tas ir, ja parametrs **Pieļaujamā svara etiķetes dimensiju izsekošanas metode** pieļaujamā svara preces apstrādes politikā ir iestatīts uz **Preces dimensijas, izsekošanas dimensijas un visas noliktavas dimensijas**). Ja pieļaujamā svara vienība ir tikai daļēji izsekota (tas ir, ja parametrs **Pieļaujamā svara etiķetes dimensiju izsekošanas metode** pieļaujamā svara vienuma apstrādes politikā iestatīts uz **Preces dimensijas, izsekošanas dimensijas un krājumu statusu**), ir spēkā papildu ierobežojumi. Tāpēc, ka redzamība šajā gadījumā tiek zaudēta starp etiķeti un noliktavu, daži papildu scenāriji netiek atbalstīti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]