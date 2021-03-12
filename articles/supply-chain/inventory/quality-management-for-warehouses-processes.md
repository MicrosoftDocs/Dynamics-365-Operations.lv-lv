---
title: Noliktavas procesu kvalitātes pārvaldība
description: Šajā tēmā ir sniegta informācija par Noliktavas procesu kvalitātes pārvaldību iespēju. Šis līdzeklis paplašina kvalitātes pārvaldības iespējas un ļauj lietotājiem integrēt krājumu iztveršanas kontroli ar noliktavas saņemšanas procesu, izmantojot papildu noliktavas pārvaldību.
author: Henrikan
manager: tfehr
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: fd6b4b0c30a8a4cb36955e9b131c937c4db80772
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983729"
---
# <a name="quality-management-for-warehouse-processes"></a>Noliktavas procesu kvalitātes pārvaldība

Šis _Noliktavas procesu kvalitātes pārvaldības_ līdzeklis ļauj jums integrēt krājumu iztveršanas kontroli ar noliktavas saņemšanas procesu, izmantojot papildu noliktavas pārvaldību. Noliktavas darbu var izveidot automātiski, lai pārvietotu krājumus uz kvalitātes kontroles novietojumu, pamatojoties uz procentuālu vai fiksētu daudzumu, vai pamatojoties uz katru *"n"* noliktavas vienību. Kad kvalitātes pārbaudes pasūtījums ir pabeigts, ir iespējams automātiski ģenerēt darbu, lai pārvietotu krājumus uz nākamo vietu procesa laikā atkarībā no kvalitātes rezultāta.

_Noliktavas procesu kvalitātes pārvaldības_ līdzeklis paplašina pamata kvalitātes pārvaldības līdzekļa iespējas. Tas sniedz iespēju izveidot kvalitātes pārbaudes pasūtījumus krājumiem, kas tiek nosūtīti uz kvalitātes kontroles vietu, lai gan kvalitātes pārbaudes pasūtījumi ne vienmēr tiek pieprasīti. Tāpēc tas ļauj izveidot vieglu kvalitātes kontroles procesu, kura pamatā ir noliktavas darbs.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Ieslēdziet Noliktavas procesu kvalitātes pārvaldības līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Noliktavas procesu kvalitātes pārvaldība*

## <a name="key-benefits"></a>Galvenie ieguvumi

Līdzeklis _Noliktavas procesu kvalitātes pārvaldība_ automātiski ģenerē darbu kā daļu no saņemšanas procesa, lai pārvietotu krājumu daudzumu, kas nepieciešams kvalitātes kontrolei kvalitātes kontroles novietojumā. Ja saņemtais daudzums pārsniedz kvalitātes kontrolei nepieciešamo daudzumu (saskaņā ar krājuma paraugu ņemšanas iestatījumiem), pārsniegtais daudzums tiek pārvietots uz saņemšanas vietu, kas definēta novietojuma direktīvas iestatījumos. Kad kvalitātes pārbaudes pasūtījums ir apstiprināts, tiek automātiski ģenerēts darbs, lai pārvietotu daudzumu kvalitātes pasūtījumam uz jaunu ienākošo vai atgriešanas vietu, pamatojoties uz apstiprināšanas rezultātu un novietojuma direktīvas iestatījumiem. Automātiski izveidots darbs, kam ir tikai daudzums, kas jāpārvieto uz un no kvalitātes kontroles, nodrošina integrētu procesu pieredzi.

> [!NOTE]
> Kad līdzeklis _Noliktavas procesu kvalitātes pārvaldība_ ir ieslēgts, jūs joprojām varat izmantot manuālo procesu. Manuālajā procesā krājumu kustība un kustība pēc veidnes tiek izmantota, lai noliktavas darbinieks iedarbinātu noliktavas darba izveidi, lai pārvietotu krājumus no kvalitātes kontroles vietas uz jaunu atrašanās vietu. Jūs varat arī iestatīt ienākošo vietu direktīvu, kas pilnībā pārvieto krājumus no saņemšanas vietas uz kvalitātes kontroles atrašanās vietu, neņemot vērā krājuma paraugu ņemšanas iestatījumus.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Kvalitātes pārvaldība un Noliktavas procesu kvalitātes pārvaldības līdzeklis

Kad līdzeklis _Noliktavas procesu kvalitātes pārvaldība_ ir ieslēgts, tiek mainīti galvenās noliktavas pārvaldības un kvalitātes pārvaldības elementu iestatījumi. Sekojošajā ilustrācijā sniegts pārskats par entītijām, kas iespējo kvalitātes pārbaudes pasūtījumus noliktavas procesiem. Teksts iekavās norāda ieteiktās darbības, kad kvalitātes pārvaldība tiek lietota, pirms _Noliktavas procesu pārvaldības kvalitātes pārvaldības_ līdzeklis ir ieslēgts.

![Kvalitātes pārvaldības entītijas](media/quality-management-entity-diagram.png "Kvalitātes pārvaldības elementi")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Veicinātāji: Kvalitātes krājumu paraugu ņemšanas un kvalitātes pārbaudes pasūtījuma darba pasūtījumu veidi

_Noliktavas procesu kvalitātes pārvaldības_ līdzeklis iepazīstina ar diviem darba pasūtījumu veidiem, kas aktivizē darba izveides procesu:

- **Kvalitātes krājumu paraugu izsniegšana** — šis darba pasūtījuma veids tiek izmantots, lai izveidotu darbu, kas veic reģistrēto krājumu pārvietošanu uz kvalitātes kontroli.
- **Kvalitātes pasūtījums** — šis darba pasūtījuma veids tiek izmantots, lai izveidotu darbu, kas krājumu pārvieto no kvalitātes kontroles uz jaunu atrašanās vietu, pamatojoties uz novietojuma direktīvas iestatījumiem.

### <a name="work-classes-location-directives-and-work-templates"></a>Darba klases, novietojuma direktīvas un darba veidnes

_Kvalitātes krājumu paraugu izsniegšana_ un _Kvalitātes pārbaudes pasūtījums_ darba pasūtījumu veidi tiek izmantoti novietojuma direktīvās, darba klasēs un darba veidnēs.

Pirms noliktavas darbu var ģenerēt automātiski, ir jāveic šādas darbības, lai pārvietotu krājumus uz kvalitātes kontroli sistēmas iestatīšanai.

1. Izveidojiet atsevišķas darba klases _Kvalitātes krājumu paraugu izsniegšana_ un _Kvalitātes pārbaudes pasūtījums_ darba pasūtījumu veidiem. Šādā veidā tiek nodrošināta iespēja automātiski izveidot atbilstošu darbu, pamatojoties uz diviem darba pasūtījumu veidiem, un ka šo darbu var veikt, izmantojot noliktavas programmu.
1. Iestatiet darba veidni katram darba pasūtījuma veidam:

    - Iestatiet darba veidni, kas izmanto _Kvalitātes krājumu paraugu izsniegšana_ darba pasūtījuma veidu, lai automātiski pārvietotu reģistrētos krājumus uz kvalitātes kontroles vietu.
    - Iestatiet darba veidni, kas izmanto _kvalitātes pārbaudes pasūtījuma_ darba pasūtījuma veidu, lai pārvietotu krājumus no kvalitātes kontroles vietas pēc tam, kad kvalitātes kontrole ir pabeigta.

1. Katram darba pasūtījuma veidam iestatiet novietojuma direktīvas, kas piemēro pareizās kvalitātes kontroles vietas, uz kurām jāpārvieto krājumi. Kad kvalitātes kontrole ir pabeigta, novietojuma direktīva _Kvalitātes pasūtījuma_ darba pasūtījuma veids nodrošina jauna mērķa novietojuma atlasi, lai krājumu varētu pārvietot no kvalitātes kontroles vietas.
1. Iestatiet atbilstošos mobilās ierīces izvēlnes elementus, lai atbalstītu saņemto krājumu pārvietošanu uz kvalitātes kontroles vietu, un krājumu apriti, kas iztur vai neiztur kvalitātes kontroli no kvalitātes kontroles vietas uz jaunu atrašanās vietu.

Lai soli pa solim redzētu, kā izpildīt šo iestatījumu, skatiet [piemēru scenāriju](#example-scenario) šīs tēmas beigās.

## <a name="enable-a-warehouse-for-quality-management"></a>Iespējot noliktavu kvalitātes pārvaldībai

Pirms _Noliktavas procesu kvalitātes pārvaldības_ līdzeklis tiek iespējots konkrētai noliktavai, ir jāveic šīs darbības, lai šo līdzekli padarītu pieejamu šai noliktavai.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Noliktavas**.
1. Atlasiet noliktavu, lai iespējotu to kvalitātes pārvaldībai.
1. **Noliktavas** kopsavilkuma cilnē iestatiet opciju **Iespējot kvalitātes pārbaudes pasūtījumu noliktavas procesiem** uz _Jā_. (Ņemiet vērā, ka šo opciju var iestatīt uz _Jā_ tikai noliktavām, kas izmanto noliktavu pārvaldības procesus.)

Kad opcija **Iespējot kvalitātes pārbaudes pasūtījumu noliktavas procesiem** ir iestatīta uz _Jā_, kvalitātes saistības iestatīšana kontrolē, vai _Noliktavas procesu kvalitātes pārvaldības_ funkcija tiek faktiski piemērota atlasītajai noliktavai. Jūs varat mainīt opcijas iestatījumu uz _Nē_ jebkurā laikā. Šādā gadījumā šis līdzeklis vairs netiks piemērots noliktavai neatkarīgi no kvalitātes saistības iestatījumiem.

## <a name="quality-control"></a>Kvalitātes kontrole

Līdzeklis _Noliktavas procesu kvalitātes pārvaldība_ kontrolē vairākus galvenos iestatījumus kvalitātes saistībām un krājuma paraugu izsniegšanai.

### <a name="quality-associations"></a>Kvalitātes piesaistes

Katrs [kvalitātes saistības ieraksts](enable-quality-management.md) nosaka pārbaužu kopu, pieņemamās kvalitātes līmeni (PKL) un iztveršanas plānu, kas tiek piemērots veidotajiem kvalitātes pasūtījumiem. Lai iestatītu kvalitātes saistības ierakstu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Krājumu pāŗvaldība \> Iestatījumi \> Kvalitātes kontrole \> Kvalitātes piesaistes**.
1. Izveidojiet vai atlasiet kvalitātes saistības ierakstu krājumam vai grupai, ar ko strādājat, vai visiem krājumiem.
1. Kopsavilkuma cilnē **Nosacījumi** iestatiet **Piemērojamā noliktavas veida** lauku uz vienu no šīm vērtībām:

    - **Kvalitātes pārvaldība tikai noliktavas procesiem** - aktivizējiet līdzekli _Noliktavas procesu kvalitātes pārvaldība_. Šo vērtību varat atlasīt tikai tad, ja atsauces veids ir *Pirkums* vai *Ražošana*.
    - **Visi** – deaktivizējiet _Noliktavas procesu kvalitātes pārvaldības_ līdzekli. Atlasiet šo vērtību visiem atsauču veidiem, izņemot *Pirkums* un *Ražošana*.

> [!NOTE]
> _Noliktavas procesu kvalitātes pārvaldības_ līdzeklis darbojas tikai tad, ja preces pirmdokumenta rindā tiek izmantoti papildu noliktavas pārvaldības procesi, un ja opcija **Iespējot kvalitātes pārbaudes pasūtījums noliktavas procesiem** ir iestatīta uz _Jā_ noliktavai pirmdokumenta rindā.

Kad katrs krājums ir reģistrēts (vai pabeigts), sistēma nosaka, kuras kvalitātes piesaistes uz to attiecas.

Kad līdzeklis _Noliktavas procesu kvalitātes pārvaldības_ ir ieslēgts, piemērojamais noliktavas veids tiek loģiski ievietots ceturtajā kvalitātes piesaistes meklēšanas hierarhijas meklēšanas grupā. Tabulā ir sniegti meklēšanas hierarhijas loģiskie attēlojumi.

| Meklēšanas grupa | Apraksts |
|---|---|
| 1. grupa | Katrai kvalitātes asociācijai pārbaudiet **Atsauces tipu**, **Notikuma veidu** un **Izpildes atbilstības** vērtības attiecībā pret elementu. Ja dokumenta pirmdokumenta rinda atbilst, pārejiet uz 2. grupu. |
| 2. grupa | Katrai kvalitātes asociācijai pārbaudiet **Krājuma koda** vērtību (_Tabula_, _Grupa_ vai _Visi_) attiecībā pret krājumu. _Tabula_ ir daudz konkrētāka par _Grupu_, un _Grupa_ ir konkrētāka par _Visiem_. Ja ir atbilstība _Tabulai_ (konkrētam krājumam), pārejiet uz 3. grupu. Ja _Tabulai_ nav atbilstības, meklējiet atbilstošo _Grupu_. Ja _Grupai_ nav atbilstības, tiek piemēroti _Visi_. Ja ir atbilstība, pārejiet uz 3. grupu. |
| 3. grupa | Katrai kvalitātes asociācijai pārbaudiet **Konta kodu** un **Resursa koda** vērtības attiecībā pret krājumu. Izmantotā loģika līdzinās loģikai, kas tiek lietota **Krājuma koda** vērtībai. |
| 4. grupa | Katrai kvalitātes asociācijai pārbaudiet **Piemērojamo noliktavas veida** vērtību (_Kvalitātes pārvaldība tikai noliktavas procesiem_ vai _Visi_) attiecībā pret krājumu. Ja opcija **Iespējot kvalitātes pārbaudes pasūtījums** ir iespējota uz _Jā_ noliktavai pirmdokumentā, un prece no pirmdokumenta rindas ir iestatīta uz _Izmantot noliktavas pārvaldības procesus_ abām asociācijām, kur ir atbilstība _Kvalitātes pārvaldībai tikai noliktavas procesiem_ , un asociācijas, kur ir atbilstība _visiem_, tiks piemērotas paralēli, ja tās abas pastāv. Ja opcija **Iespējot kvalitātes pārbaudes pasūtījumu noliktavas procesiem** ir iestatīta uz _Nē_ noliktavai pirmdokumentā, un krājums pirmdokumenta rindā ir iestatīts uz _Izmantot noliktavas pārvaldības procesus_, tiks piemērota tikai kvalitātes pārvaldība. |

Piemēram, jūs definējāt noliktavu, kurā opcija **Iespējot kvalitātes pārbaudes pasūtījumu noliktavas procesiem** ir iespējota uz _Jā_, un jums ir divas kvalitātes saistības, kas definētas *Pirkuma* atsauces veidam: viens visiem krājumiem un viens *Reģistrācijas* notikuma veidam. Vienīgā atšķirība starp diviem kvalitātes piesaistes veidiem ir **Piemērojams noliktavas veids** vērtība: tā ir iestatīta uz _Visi_ vienai kvalitātes saistībai un uz _Kvalitātes pārvaldība tikai noliktavas procesiem_ otrai. Šādā gadījumā abas kvalitātes saistības ir vienlīdz specifiskas, un tās abas tiks piemērotas.

Kvalitātes piesaistes **Testa grupas** lauka vērtība arī ir faktors. Šis lauks nosaka testa procedūru, kas jālieto. Ja **Testa grupas** vērtība ir vienāda abām saistībām, tiks izveidots tikai viens kvalitātes pārbaudes pasūtījums kvalitātes saistībai, kur **Piemērojama noliktavas veida** vērtība ir _Kvalitātes pārvaldība tikai noliktavas procesiem_. Ja **Testa grupas** vērtība nav vienāda abām saistībām, tiks izveidoti divi kvalitātes pārbaudes pasūtījumi. Pirmais kvalitātes pārbaudes pasūtījums tiks izveidots kvalitātes saistībai, kur **Piemērojams noliktavas veids** vērtība ir _Kvalitātes pārvaldība tikai noliktavas procesiem_. Otrais kvalitātes pārbaudes pasūtījums tiks izveidots kvalitātes saistībai, kur **Piemērojams noliktavas veids** vērtība ir _Visi_.

> [!NOTE]
> _Kvalitātes pārvaldība tikai noliktavas procesiem_ vērtība tiek uzskatīta par specifiskāku nekā _Visiem_, ja 1. un 2. grupas kvalitātes piesaistes kritēriji ir vienādi un ja testa grupa ir viena un tā pati. Divi kvalitātes pārbaudes pasūtījumi tiks izveidoti tikai tad, ja testa grupas atšķiras.

#### <a name="reference-types"></a>Atsauču tipi

Kad **Atsauces veida** vērtība ir _Pirkums_ un **Piemērotā noliktavas tipa** vērtība ir _Kvalitātes pārvaldība tikai noliktavas procesiem_, **Notikuma veida** lauks **Procesa** kopsavilkuma cilnē ir jāiestata uz _Reģistrācija_. _Reģistrācija_ ir vienīgais atbalstītais notikuma veids _Pirkuma_ atsauces veidam, kad izmantojat līdzekli _Noliktavas procesu kvalitātes pārvaldība_.

#### <a name="quality-processing-policy"></a>Kvalitātes pārbaudes apstrādes politika

Līdzeklis _Kvalitātes pārvaldība tikai noliktavas procesiem_ ļauj izveidot darbu, pamatojoties tikai uz krājumu paraugu izsniegšanu. Tāpēc tas ļauj veikt vieglu procesu. Krājums, kas tiek izveidots, ir atkarīgs no krājumu paraugu izsniegšanas, kas ir saistīta ar kvalitātes saistību. Izmantojot vieglu procesu, pēc tam, kad darbinieks nostāda daudzumu kvalitātes kontroles vietā, kvalitātes departaments var manuāli izveidot kvalitātes pārbaudes pasūtījumu, ja tāds ir nepieciešams.

**Kvalitātes apstrādes politikas** lauks kopsavilkuma cilnē **Kvalitātes pārbaudes pasūtījuma process** kontrolē, vai kvalitātes pārbaudes pasūtījums tiek izveidots arī, izveidojot darbu, lai pārvietotu krājumu uz kvalitātes kontroles vietu. Šo lauku var iestatīt, lai _Izveidotu kvalitātes pārbaudes pasūtījumu_ vai _Izveidotu tikai darbu_. Noklusējuma vērtība ir _Izveidot kvalitātes pārbaudes pasūtījumu_.

> [!NOTE]
> Neatkarīgi no tā, vai kvalitātes pārbaudes pasūtījumus veidojat manuāli vai automātiski, sistēma automātiski izveido darbu, lai pārvietotu krājumus no kvalitātes kontroles vietas, kad kvalitātes pārbaudes pasūtījums ir atzīmēts kā pārbaudīts.

Kvalitātes pārbaudes pasūtījuma darba izveide nav saistīta ar kvalitātes saistības iestatījumiem. Ja pastāv darba veidne, kurai **Darba pasūtījuma veida** vērtība ir *Kvalitātes pārbaudes pasūtījums*, un ja vaicājuma kritēriji ir izpildīti šai darba veidnei, kvalitātes pārbaudes apliecināšana izraisīs kvalitātes pārbaudes pasūtījuma darba izveidi.

#### <a name="referenced-item-sampling"></a>Atsauce uz krājumu iztveršanu

Katrai kvalitātes saistībai ir jāatsaucas uz krājumu iztveršanu. Krājumu iztveršana nosaka daudzumu, kas tiks nosūtīts kvalitātes kontrolei. Tas var tikt uzstādīts, lai attiektos tikai uz kvalitātes saistībām, kur **Piemērojamā noliktavas veida** vērtība ir _Kvalitātes pārvaldība tikai noliktavas procesiem_. Ja **Iztveršanas nolūka** vērtība krājuma paraugu izsniegšanai ir _Noslodze_ vai _Sūtīšana_, vai **Daudzuma specifikācijas** vērtība ir _Pilna noliktavas vienība_, krājumu iztveršana var būt attiecināma tikai pēc kvalitātes saistības, kur **Piemērojamā noliktavas veida** vērtība ir _Kvalitātes pārvaldība tikai noliktavas procesiem_.

Ja jūs definējat krājumu iztveršanu, kas izmanto _Kvalitātes pārvaldība tikai noliktavas procesiem_ piemērojamo noliktavas veidu, jums tiks parādīta kļūda, ja mēģināsit atsaukties uz to no kvalitātes saistības, kas neizmanto _Kvalitātes pārvaldība noliktavas procesiem_ līdzekli.

> [!NOTE]
> Krājumu iztveršana, kas izmanto pilnīgu bloķēšanu, netiek atbalstīta kvalitātes saistībām, kur **Piemērojamais noliktavas veidu** lauks ir iestatīts uz _Kvalitātes pārvaldība tikai noliktavas procesiem_.

### <a name="item-sampling"></a>Krājumu iztveršana

Krājumu iztveršana kontrolē to, cik bieži krājumi tiek nosūtīti kvalitātes kontrolei. Funkcija _Noliktavas procesu kvalitātes pārvaldība_ iepazīstina ar _krājumu iztveršanas_ konceptu. Sistēma izmanto krājumu iztveršanas nolūku, kad tiek novērtēts, vai un kā jāizveido kvalitātes pārbaudes pasūtījumi un/vai kvalitātes krājumu iztveršanas darbs un kvalitātes pārbaudes pasūtījuma darbs.

Lai iestatītu krājumu iztveršanu, dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Kvalitātes kontrole \> Krājumu iztveršana** un iestatiet **Paraugu ņemšana** lauku uz vienu no šīm vērtībām:

- **Pasūtījums** – Pirmdokumenta rinda būs pamats izvērtēšanai, vai un kā jāizveido kvalitātes pārbaudes pasūtījumi un/vai kvalitātes krājumu paraugu ņemšanas darbs un kvalitātes pārbaudes pasūtījuma darbs. Šī vērtība ir noklusējuma vērtība, un, atlasot to, sistēma darbojas tāpat, kā tā darbojas, kad _Noliktavas procesu kvalitātes pārvaldības_ līdzeklis nav ieslēgts.
- **Noslodze** – noslodzes tiks izmantotas kā pamats, lai novērtētu, vai un kā tiek izveidots kvalitātes pārbaudes pasūtījums un/vai darbs. Šī vērtība ir pieejama tikai tad, kad _Noliktavas procesu kvalitātes pārvaldības_ līdzeklis ir ieslēgts.
- **Sūtījums** – sūtījumi tiks izmantoti kā pamats, lai novērtētu, vai un kā tiek izveidots kvalitātes pārbaudes pasūtījums un/vai darbs. Šī vērtība ir pieejama tikai tad, kad _Noliktavas procesu kvalitātes pārvaldības_ līdzeklis ir ieslēgts.

> [!NOTE]
> Kad **Paraugu ņemšanas** lauks ir iestatīts uz *Noslodze* vai *Sūtījums*, noslodzes elements un sūtījuma elementi tiks izmantoti, ja tie ir pieejami. Ja tie nav pieejami, tiks izmantots pasūtījuma elements.

_Noliktavas procesu kvalitātes pārvaldības_ līdzeklis ievieš arī *Pilnu noliktavas vienības* vērtību **Daudzuma specifikācijas** laukam. Šī vērtība atbalsta kvalitātes pārbaudes pasūtījuma darbu un kvalitātes krājumu iztveršanas darbu izveidi, balstoties uz noliktavas vienībām. Atlasot šo vērtību, rodas šādas izmaiņas:

- Opcija **Sadalīt skaitu pēc krājuma** un lauks **Pēc "n" noliktavas vienības** kopsavilkuma cilnē **Process** kļūst pieejama.
- **Vērtības** lauks kopsavilkuma cilnē **Paraugu daudzums** kļūst nepieejams.
- **Pēc atjauninātā daudzuma**, **Atrašanās vieta** un **Noliktavas vienība** opcijas ir iestatītas uz *Jā*, un iestatījumus nevar mainīt.

Opcija **Sadalīt skaitu pēc krājuma** kontrolē, vai noliktavas vienību skaits tiek novērtēts pēc preces vai visiem krājumiem iztveršanas diapazonā. Preces varianti tiek uzskatīti par vienu un to pašu krājumu. Šī opcija kontrolē arī to, vai noliktavas vienību skaits ir atiestatīts katram krājumam.

**Pēc "n" noliktavas vienības** lauka vērtība kontrolē, cik bieži kvalitātes pārbaudes pasūtījumi tiek izveidoti saistībā ar reģistrēto krājumu skaitu. Piemēram, vērtība *3* nosūtīs katru trešo krājumu kvalitātes kontrolei, sākot ar pirmo krājumu. Vērtībai jābūt lielākai par 0 (nulle).

Lai gan darbinieki saņem elementus, izmantojot noliktavas programmu, sistēma pārbauda, vai kvalitātes saistība ir iestatīta katram ienākošajam elementam. Ja ir iestatīta kvalitātes saistība, sistēma izmanto krājumu iztveršanas ierakstu, kas ir konfigurēts šai kvalitātes saistībai, lai noteiktu, kā tā izveidos kvalitātes pārbaudes pasūtījumus, kvalitātes krājumu iztveršanas darbu un pirkšanas pasūtījuma darbu.

> [!NOTE]
> Kad kvīts reģistrācija ir veikta Web klientā (izmantojot mazo reģistrācijas lapu vai krājumu saņemšanas žurnālu pirkšanas pasūtījuma rindām), netiks izveidots neviens kvalitātes krājumu iztveršanas darbs vai pirkšanas pasūtījuma darbs, neatkarīga no šī iestatījuma. Tā vietā krājumiem, kas atbilst kvalitātes saistībai, tiek izmantota atsauce uz preču paraugu ņemšanu, lai kontrolētu tikai kvalitātes pārbaudes pasūtījumu izveidi.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Automātisku kvalitātes pasūtījumu izveidošanas piemēri

Nākamie piemēri parāda, kā kvalitātes saistības iestatījums un saistītā krājumu iztveršana ietekmē kvalitātes pārbaudes pasūtījumu veidošanu, kad **Piemērojamā noliktavas veida** lauks ir iestatīts uz _Kvalitātes pārvaldība tikai noliktavas procesiem_.

Kad **Kvalitātes specifikācijas** vērtība ir _Pilna noliktavas vienība_, **Pēc "n" noliktavas vienības** lauks kontrolē, kuriem noliktavas vienību kvalitātes krājumu iztveršanas darbiem tas ir izveidots. Pirmā noliktavas vienība vienmēr iet uz kvalitātes kontroli, un tad šī lauka vērtība norāda, ka ir jāpāriet arī katrai *"n"* noliktavas vienībai pēc šīs noliktavas vienības.

**Atsauču tipa** vērtība šādiem piemēriem ir _Pirkšana_, un **Notikuma veida** vērtība ir *Reģistrācija*.

| Iztveršana | Daudzuma specifikācija | Pēc atjauninātā daudzuma | Pēc noliktavas dimensijas | Sadalīt skaitu pēc krājuma | Pēc “n” noliktavas vienības | Rezultāts |
|---|---|---|---|---|---|---|
| Pasūtījums | Pilna noliktavas vienība | Jā _(slēgts/nav rediģējams)_ | <p>Novietojums: Jā</p><p>Noliktavas vienība: Jā _(slēgts/nav rediģējams)_</p> | Nr. | 3 | <p>**Pasūtījuma rindas daudzums: 100 EA**</p><ol><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP1<p>Kvalitātes krājumu iztveršanas darbs uz 20 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 20 EA</p></li><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP2<p>Pirkšanas pasūtījuma darbs uz 20 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP3<p>Pirkšanas pasūtījuma darbs uz 20 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP4<p>Kvalitātes krājumu iztveršanas darbs uz 20 EA</p></li><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP5<p>Pirkšanas pasūtījuma darbs uz 20 EA (izvietošanai)</p></li></ol> |
| Pasūtījums | Fiksēts daudzums = 1 | Jā | <p>Novietojums: Jā</p><p>Noliktavas vienība: Jā</p> | Nr. | Nav attiecināms | <p>**Pasūtījuma rindas daudzums: 100**</p><ol><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP1<p>Kvalitātes krājumu paraugu izdošanas darbs uz 1 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 1 EA</p><p>Pirkšanas pasūtījuma darbs uz 19 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP2<p>Kvalitātes krājumu paraugu izdošanas darbs uz 1 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 1 EA</p><p>Pirkšanas pasūtījuma darbs uz 19 (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP3<p>Kvalitātes krājumu paraugu izdošanas darbs uz 1 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 1 EA</p><p>Pirkšanas pasūtījuma darbs uz 19 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP4<p>Kvalitātes krājumu paraugu izdošanas darbs uz 1 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 1 EA</p><p>Pirkšanas pasūtījuma darbs uz 19 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 20 EA, LP5<p>Kvalitātes krājumu paraugu izdošanas darbs uz 1 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 1 EA</p><p>Pirkšanas pasūtījuma darbs uz 19 EA (izvietošanai)</p></li></ol> |
| Pasūtījums | Procenti = 10 | Nr. | <p>Novietojums: Nē</p><p>Noliktavas vienība: Nē</p> | Nr. | Nav attiecināms | <p>**Pasūtījuma rindas daudzums: 100 EA**</p><ol><li>Reģistrēt kvīti noliktavas programmā 50 EA, LP1<p>Kvalitātes krājumu paraugu izdošanas darbs uz 10 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 10 EA</p><p>Pirkšanas pasūtījuma darbs uz 40 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 50 EA, LP2<p>Pirkšanas pasūtījuma darbs uz 50 EA (izvietošanai)</p></li></ol> |
| Noslodze | Procenti = 5 | Jā _(slēgts/nav rediģējams)_ | <p>Novietojums: Nē</p><p>Noliktavas vienība: Nē</p> | Nr. | Nav attiecināms | <p>**Pasūtījuma rindas daudzums: 500 EA**</p><p>**Divas noslodzes: pirmā noslodze 200 EA, otrā noslodze 300 EA**</p><ol><li>Reģistrēt kvīti noliktavas programmā pirmajai noslodzei 100 EA<p>Kvalitātes krājumu paraugu izdošanas darbs uz 5 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 5 EA</p><p>Pirkšanas pasūtījuma darbs uz 95 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā pirmajai noslodzei 100 EA<p>Kvalitātes krājumu paraugu izdošanas darbs uz 5 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 5 EA</p><p>Pirkšanas pasūtījuma darbs uz 95 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā otrajai noslodzei 300 EA<p>Kvalitātes krājumu paraugu izdošanas darbs uz 15 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 15 EA</p><p>Pirkšanas pasūtījuma darbs uz 285 EA (izvietošanai)</p></li></ol> |
| Pasūtījums | Procenti = 10 | Nr. | <p>Novietojums: Jā</p><p>Noliktavas vienība: Jā</p> | Nr. | Nav attiecināms | <p>**Pasūtījuma rindas daudzums: 100**</p><ol><li>Reģistrēt kvīti noliktavas programmā 50 EA, LP1<p>Kvalitātes krājumu paraugu izdošanas darbs uz 5 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 5 EA</p><p>Pirkšanas pasūtījuma darbs uz 45 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 50 EA, LP2<p>Kvalitātes krājumu paraugu izdošanas darbs uz 5 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 5 EA</p><p>Pirkšanas pasūtījuma darbs uz 45 (izvietošanai)</p></li></ol> |
| Noslodze | Pilna noliktavas vienība | Jā _(slēgts/nav rediģējams)_ | <p>Novietojums: Jā</p><p>Noliktavas vienība: Jā _(slēgts/nav rediģējams)_</p> | Nr. | 3 | <p>**Divi krājumi:**</p><ul><li>**Pasūtījuma rindas daudzums krājumam A: 120 EA (4 paletes)**</li><li>**Pasūtījuma rindas daudzums krājumam B: 90 EA (3 paletes)**</li></ul><p>**Viena noslodze, divas noslodzes rindas ar katru pasūtījuma rindu**</p><ol><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP1<p>Kvalitātes krājumu paraugu izdošanas darbs uz 30 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 30 EA</p></li><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP2<p>Pirkšanas pasūtījuma darbs uz 30 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP3<p>Pirkšanas pasūtījuma darbs uz 30 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP4<p>Kvalitātes krājumu paraugu izdošanas darbs uz 30 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 30 EA</p></li><li>Reģistrēt kvīti noliktavas programmā elementam B, 30 EA, LP5<p>Pirkšanas pasūtījuma darbs uz 30 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā elementam B, 30 EA, LP6<p>Pirkšanas pasūtījuma darbs uz 30 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP7<p>Kvalitātes krājumu paraugu izdošanas darbs uz 30 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 30 EA</p></li></ol> |
| Noslodze | Pilna noliktavas vienība | Jā _(slēgts/nav rediģējams)_ | <p>Novietojums: Jā</p><p>Noliktavas vienība: Jā _(slēgts/nav rediģējams)_</p> | Jā | 3 | <p>**Divi krājumi:**</p><ul><li>**Pasūtījuma rindas daudzums krājumam A: 120 EA (4 paletes)**</li><li>**Pasūtījuma rindas daudzums krājumam B: 90 EA (3 paletes)**</li></ul><p>**Viena noslodze, divas noslodzes rindas ar katru pasūtījuma rindu**</p><ol><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP1<p>Kvalitātes krājumu paraugu izdošanas darbs uz 30 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 30 EA</p></li><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP2<p>Pirkšanas pasūtījuma darbs uz 30 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP3<p>Pirkšanas pasūtījuma darbs uz 30 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP4<p>Kvalitātes krājumu paraugu izdošanas darbs uz 30 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 30 EA</p></li><li>Reģistrēt kvīti noliktavas programmā elementam B, 30 EA, LP5<p>Kvalitātes krājumu paraugu izdošanas darbs uz 30 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 30 EA</p></li><li>Reģistrēt kvīti noliktavas programmā elementam B, 30 EA, LP6<p>Pirkšanas pasūtījuma darbs uz 30 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā elementam A, 30 EA, LP7<p>Pirkšanas pasūtījuma darbs uz 30 EA (izvietošanai)</p></li></ol> |
| Noslodze | Procenti = 10 | Jā _(slēgts/nav rediģējams)_ | <p>Novietojums: Nē</p><p>Noliktavas vienība: Nē</p> | Nr. | Nav attiecināms | <p>**Pasūtījuma rindas daudzums: 100 EA**</p><p>**Neviena noslodze netiek veidota. Pasūtījuma tvērums tiek pielietots.**</p><ol><li>Reģistrēt kvīti noliktavas programmā 50 EA, LP1<p>Kvalitātes krājumu paraugu izdošanas darbs uz 5 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 5 EA</p><p>Pirkšanas pasūtījuma darbs uz 45 EA (izvietošanai)</p></li><li>Reģistrēt kvīti noliktavas programmā 50 EA, LP2<p>Kvalitātes krājumu paraugu izdošanas darbs uz 5 EA</p><p>Kvalitātes pārbaudes pasūtījums 1 uz 5 EA</p><p>Pirkšanas pasūtījuma darbs uz 45 EA (izvietošanai)</p></li></ol> |

Kad darbinieks apstiprina vienu no kvalitātes pasūtījumiem, kas tiek parādīti iepriekšējā tabulā, sistēma automātiski ģenerē kvalitātes pārbaudes pasūtījuma darbu, lai pārvietotu krājumus no kvalitātes kontroles novietojuma uz vietu, kas noteikta novietojuma direktīvā _Kvalitātes pasūtījuma_ darba pasūtījuma veids. Šim nolūkam var iestatīt jebkuru atrašanās vietu, piemēram, atgriešanas vai glabāšanas vietu atkarībā no kvalitātes pārbaudes pasūtījuma testa rezultāta. Šī iestatījumu piemēru skatiet tēmā [piemēru scenārijs](#example-scenario) šīs tēmas beigās.

Jūs varat atkārtoti atvērt kvalitātes pārbaudes pasūtījumu, kas jau ir apstiprināts, ar nosacījumu, ka kvalitātes pārbaudes pasūtījuma darbam, kas ir saistīts ar krājuma pārvietošanu no kvalitātes kontroles vietas, nav **Darba statusa** vērtība *Noslēgts* vai *Nepabeigts*.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Apstrādāt priekšstatus, ja pastāv vairākas kvalitātes saistības

Vienai un tai pašai pirmdokumenta rindai var definēt un pielietot vairāk nekā vienu kvalitātes saistību, un **Piemērotais noliktavas veida** lauks var būt iestatīts uz _Kvalitātes pārvaldība tikai noliktavas procesiem_ dažām no šīm kvalitātes saistībām, bet citām saistībām uz _Visi_.

Sekojošajā piemērā **Atsauces veida** vērtība ir _Pirkšana_.

1. Pirmā kvalitātes saistība ir iestatīta šādā veidā:

    - **Atbilstošais noliktavas veids:** *Kvalitātes pārvaldība tikai noliktavu procesiem*
    - **Krājuma kods:** *A0001*
    - **Konta kods:** *Visi*
    - **Testa grupa:** *Norobežojums*
    - **Krājuma paraugu izdošana:** *5 gab.*

1. Otrā kvalitātes saistība ir iestatīta šādā veidā:

    - **Atbilstošais noliktavas veids:** *Visi*
    - **Krājuma kods:** *Visi*
    - **Konta kods:** *Visi*
    - **Testa grupa:** *Norobežojums*
    - **Krājuma paraugu izdošana:** *1 gab.*

1. Trešā kvalitātes saistība ir iestatīta šādā veidā:

    - **Atbilstošais noliktavas veids:** *Kvalitātes pārvaldība tikai noliktavu procesiem*
    - **Krājuma kods:** *Visi*
    - **Konta kods:** *104*
    - **Testa grupa:** *Pretestība*
    - **Krājuma paraugu izdošana:** *Katra otrā noliktavas vienība* (Šis iestatījums nozīmē, ka pirmā, trešā, piektā un tā tālāk, saņemtās noliktavas vienības radīs kvalitātes pārbaudes pasūtījumu.)

1. Ceturtā kvalitātes saistība ir iestatīta šādā veidā:

    - **Atbilstošais noliktavas veids:** *Visi*
    - **Krājuma kods:** *Visi*
    - **Konta kods:** *Visi*
    - **Testa grupa:** *Pretestība*
    - **Krājuma paraugu izdošana:** *5 gab.*

1. Piektā kvalitātes saistība ir iestatīta šādā veidā:

    - **Atbilstošais noliktavas veids:** *Visi*
    - **Krājuma kods:** *Visi*
    - **Konta kods:** *Visi*
    - **Testa grupa:** *Konuss*
    - **krājuma paraugu izdošana:** *10%*

Pirkšanas pasūtījums krājuma A0001 daudzumam 10 tagad ir izveidots kreditoram 104. Tad pirkšanas pasūtījuma rinda ar daudzumu 10 tiek reģistrēta kā saņemta zem vienas noliktavas vienības, izmantojot noliktavas programmu. Rezultāts ir šāds:

- Ir viens kvalitātes pārbaudes pasūtījums no pirmās kvalitātes saistības *Norobežojuma* testa grupai. Daudzums ir 5. Nav kvalitātes pasūtījuma no otrās kvalitātes saistības, jo pirmās kvalitātes saistības kritēriji ir konkrētāki attiecībā uz *Norobežojuma* testa grupu.
- Ir viens kvalitātes pārbaudes pasūtījums trešajai kvalitātes saistībai *Pretestības* testa grupai. Daudzums ir 10. Nav kvalitātes pasūtījuma no ceturtās kvalitātes saistības, jo pirmās kvalitātes saistības kritēriji ir konkrētāki attiecībā uz *Pretestības* testa grupu.
- Ir viens kvalitātes pārbaudes pasūtījums piektajai kvalitātes saistībai *Konuss* testa grupai. Daudzums ir 1.

Saistībā ar vienas kvalitātes pārbaudes pasūtījuma izveidi katrai no trim kvalitātes saistībām ir izveidots arī kvalitātes krājumu iztveršanas darbs. Reģistrētais daudzums ir tikai 10. Tomēr, ņemot vērā krājumu iztveršanas iestatījumu, to kvalitātes pārbaudes pasūtījumu daudzumu summa, kas ir izveidota *Kvalitātes pārvaldība tikai noliktavas procesiem* piemērojamajam noliktavas veidam, ir 16, kas pārsniedz fizisko reģistrēto daudzumu 10. Tādēļ darbs netiks izveidots pilnīgas kvalitātes pārbaudes pasūtījumu daudzumiem (16), jo tikai 10 ir fiziski pieejami pārvietošanai uz kvalitātes kontroles vietu. Prioritāte, kas tiek izmantota kvalitātes krājumu iztveršanas darba izveidei, ir saistīta ar kvalitātes pārbaudes pasūtījuma izveides secību:

- **Pirmais kvalitātes pārbaudes pasūtījums (daudzums = 5):** Kvalitātes krājumu iztveršanas darbs tiek izveidots daudzumam 5. Daudzums 5 (10 – 5) tagad ir paredzēts turpmākai kvalitātes krājumu iztveršanas darbu izveidei.
- **Otrais kvalitātes pārbaudes pasūtījums (daudzums = 10):** Kvalitātes krājumu iztveršanas darbs tiek izveidots daudzumam 5. Daudzums 0 (nulle) tagad ir paredzēts turpmākai kvalitātes krājumu iztveršanas darbu izveidei.
- **Trešais kvalitātes pārbaudes pasūtījums (daudzums = 1):** Netiek izveidots neviens kvalitātes krājumu iztveršanas darbs.

Kvalitātes pārbaudes pasūtījumu izveides procesa ietvaros tiek izveidots krājumu bloķēšanas daudzums 10. Šī krājumu bloķēšana ir atsauce uz katru no trim kvalitātes pārbaudes pasūtījumiem. Kvalitātes pārbaudes pasūtījuma daudzumu summa ir 16.

Kad kvalitātes pārbaudes pasūtījumi tiek pārbaudīti, sistēma mēģina izveidot kvalitātes pārbaudes pasūtījumu darbu katram pārbaudītajam kvalitātes pārbaudes pasūtījumam. Tā kā kvalitātes pārbaudes pasūtījuma daudzumu summa pārsniedz daudzumu, kas patiesībā ir bloķēts, un tāpēc tas ir pieejams darba izveidei, kvalitātes pārbaudes pasūtījuma darbu nevar izveidot pilnīgiem kvalitātes pasūtījumu daudzumiem, kā redzams šeit. (Šajā piemērā tiek turpināts iepriekšējais piemērs.)

1. **Pārbaudiet otro izveidoto kvalitātes pārbaudes pasūtījumu (daudzums = 10). Kvalitātes pārbaudes pasūtījuma darbs ir izveidots daudzumam 4.**

    Kvalitātes pārbaudes pasūtījuma darba izveide tiek uzsākta pēc krājumu bloķēšanas daudzuma maiņas. Tā kā kvalitātes pārbaudes pasūtījuma daudzumu summa bija 16, tad daudzuma 10 apstiprināšanas dēļ atlikušie kvalitātes pārbaudes pasūtījuma daudzumi tiks uzskatīti kā 6. Krājumu bloķēšanas daudzums ir samazināts no 10 uz 6. Samazinātais daudzums 4 ir piešķirts kvalitātes pārbaudes pasūtījuma darba izveidei.

2. **Pārbaudiet pirmo izveidoto kvalitātes pārbaudes pasūtījumu (daudzums = 5). Kvalitātes pārbaudes pasūtījuma darbs ir izveidots daudzumam 5.**

    Kvalitātes pārbaudes pasūtījuma darba izveide tiek uzsākta pēc krājumu bloķēšanas daudzuma maiņas. Tā kā kvalitātes pārbaudes pasūtījuma daudzumu summa bija 6, tad daudzuma 5 apstiprināšanas dēļ atlikušie kvalitātes pārbaudes pasūtījuma daudzumi tiks uzskatīti kā 1. Krājumu bloķēšanas daudzums ir samazināts no 6 uz 1. Samazinātais daudzums 5 ir piešķirts kvalitātes pārbaudes pasūtījuma darba izveidei.

3. **Pārbaudiet trešo izveidoto kvalitātes pārbaudes pasūtījumu (daudzums = 1). Kvalitātes pārbaudes pasūtījuma darbs ir izveidots daudzumam 1.**

    Kvalitātes pārbaudes pasūtījuma darba izveide tiek uzsākta pēc krājumu bloķēšanas daudzuma maiņas. Tā kā kvalitātes pārbaudes pasūtījuma daudzumu summa bija 1, tad daudzuma 1 apstiprināšanas dēļ atlikušie kvalitātes pārbaudes pasūtījuma daudzumi tiks uzskatīti kā 0 (nulle). Krājumu bloķēšana tiek noņemta (tas ir, krājumu bloķēšanas daudzums ir samazināts no 1 līdz 0). Samazinātais daudzums 1 ir piešķirts kvalitātes pārbaudes pasūtījuma darba izveidei.

> [!NOTE]
> Kvalitātes pārbaudes pasūtījumu darba izveide ir atkarīga no krājumu bloķēšanas daudzuma, kas ir saistīts ar vienu vai vairākiem kvalitātes pārbaudes pasūtījumiem. Ja kvalitātes pārbaudes pasūtījuma daudzumu summa pārsniedz norādītos krājumu bloķēšanas daudzumus, kvalitātes pārbaudes pasūtījumu apstiprināšanas secība nosaka kvalitātes pārbaudes pasūtījuma darba izveidi.

## <a name="canceling-quality-item-sampling-work"></a>Kvalitātes krājumu iztveršanas darba atteikšana

Jūs varat atcelt darbu, kas ir izveidots kvalitātes krājumu iztveršanai. Lai kontrolētu, kas tiek parādīts, kad šis darbs tiek atcelts, veiciet šādas darbības.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.
1. Cilnē **Vispārīgi**, kopsavilkuma cilnē **Darbs** iestatiet opciju **Atreģistrēt kvīti, kad darbs tiek atcelts** uz vienu no šīm vērtībām:

    - **Jā** – ja kvalitātes krājumu iztveršanas darbs ir atcelts, tiek dzēsts saistītais kvalitātes pārbaudes pasūtījums, un krājumi tiek atreģistrēti.
    - **Nē** – ja kvalitātes krājumu iztveršanas darbs ir atcelts, netiek dzēsts saistītais kvalitātes pārbaudes pasūtījums, un krājumi tiek reģistrēti.

## <a name="cross-docking"></a>Pārkraušana sadales centrā

Jums var būt kvalitātes saistības iestatīšana, kas veido krājumu iztveršanas darbu. Tomēr, ja pārkraušanas sadales centrā eksistē paralēli ar kvalitātes saistību, kas izveido kvalitātes krājumu iztveršanas darbu, ja pastāv pietiekams daudzums, lai izpildītu pārkraušanu sadales centrā, tiek izveidots tikai krājumu iztveršanas darbs. Gadījumos, kad opcija **Iespējot kvalitātes pārbaudes pasūtījumu noliktavas procesiem** ir iestatīta uz _Jā_ saņemšanas noliktavai, un **Piemērojamais noliktavas veida** lauks ir iestatīts uz _Kvalitātes pārvaldība tikai noliktavas procesiem_ kvalitātes saistībai, kvalitātes krājumu iztveršanas darba izveide ir prioritāra attiecībā uz pārkraušanu sadales centrā izveidi. Ja daudzums pārsniedz pieprasījumu pārkraušanai sadales centrā, sistēma joprojām izveido tikai krājumu iztveršanas darbu.

## <a name="destructive-testing"></a>Destruktīva testēšana

Jūs varat definēt testa grupu, kas veic destruktīvo testēšanu. Destruktīvas pārbaudes gadījumā pieņēmums ir tāds, ka neatkarīgi no testa rezultāta testējamā krājuma daudzums tiks iznīcināts kā daļa no testa. Veids, kā _Kvalitātes pārvaldība noliktavu procesiem_ līdzeklis atbalsta destruktīvo testēšanu, līdzinās kvalitātes pārvaldības atbalsta veidam, kad līdzeklis nav ieslēgts. Lai varētu pārbaudīt kvalitātes pārbaudes pasūtījumu, kvalitātes kontrolierim ir jānorāda iznīcinātā daudzuma izdošanas vieta. Jūs varat reģistrēt izdošanu no kvalitātes pārbaudes pasūtījuma lapas, darbības rūtī atlasot **Krājums \> Izdošana**. Pēc tam, kad izdošana par kvalitātes pārbaudes pasūtījuma daudzumu ir reģistrēta, apstiprināšanu var pabeigt.

## <a name="example-scenario"></a>Piemēra situācija

### <a name="prepare-the-scenario"></a>Scenārija sagatavošana

Lai strādātu ar šo scenāriju, jums jāsagatavo sistēma sekojoši:

- Pārliecinieties, ka sistēmā ir instalēti demonstrācijas dati, un atlasiet **USMF** juridisko personu.
- Ieslēdziet _Noliktavas procesu kvalitātes pārvaldības_ līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigurējiet noliktavu 51, lai izmantotu _Noliktavas procesu kvalitātes pārvaldības_ līdzekli, veicot šīs darbības:

    1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Noliktavas**.
    1. Atlasiet noliktavu 51.
    1. Kopsavilkuma cilnē **Noliktavas** iestatiet opciju **Iespējot kvalitātes pārbaudes pasūtījumu noliktavas procesiem** uz *Jā*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Ievadītā kvalitāte iestatījumos — pāriet uz kvalitātes kontroles vietu

Tagad jums ir jāsagatavo pamata iestatījums, kas ļaus jūsu sistēmai atbalstīt līdzekli _Noliktavas procesu kvalitātes pārvaldība_ noliktavai 51. (Demonstrācijas dati definē kvalitātes pārvaldības atrašanās vietu, kuras nosaukums ir *KPS*. Šajā scenārijā uz šo atrašanās vietu ir atsauces vairākas reizes.) Jūs sagatavosiet tālāk norādītos elementus, kā aprakstīts šīs sadaļas apakšnodaļās:

- Darba klase
- Darba veidne
- Novietojuma direktīva
- Krājumu iztveršana
- Kvalitātes saistība
- Mobilās ierīces izvēlnes vienumi

#### <a name="work-class-for-quality-in"></a>Darba klase ievadītajai kvalitātei

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.
1. Izveidojiet darba klasi un iestatiet šādas vērtības:

    - **Darba klases ID:** _QualityIn_
    - **Apraksts:** _Kvalitātes krājumu iztveršana_
    - **Darba pasūtījuma veids:** _Kvalitātes krājumu iztveršana_

#### <a name="work-template"></a>Darba veidne

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Laukā **Darba pasūtījuma veids** iestatiet vērtību _Kvalitātes krājuma paraugu izdošana_.
1. Izveidojiet darba veidni un iestatiet šādas vērtības:

    - **Darba veidne:** _51 kvalitāte_
    - **Darba veidnes apraksts:** _51 kvalitāte_

1. Pievienojiet rindu darba veidnei un iestatiet šādas vērtības:

    - **Darba veids:** _Izdošana_
    - **Darba klases ID:** _QualityIn_

1. Pievienojiet otru rindu darba veidnei un iestatiet šādas vērtības:

    - **Darba veids:** _Izvietošana_
    - **Darba klases ID:** _QualityIn_

#### <a name="location-directive"></a>Novietojuma direktīva

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Laukā **Darba pasūtījuma veids** iestatiet vērtību _Kvalitātes krājumu iztveršana_.
1. Izveidojiet novietojuma direktīvu un iestatiet šādas vērtības:

    - **Nosaukums:** _51 uz kvalitāti_
    - **Darba veids:** _Izvietošana_
    - **Vieta:** 5
    - **Noliktava:** _51_

1. Pievienojiet rindu novietojuma direktīvai un iestatiet šādas vērtības:

    - **No daudzuma:** _1_
    - **Līdz daudzumam:** _1 000 000_

1. Izveidojiet novietojuma direktīvas darbību un iestatiet šādu vērtību:

    - **Nosaukums:** _Kvalitāte_

1. Jaunās atrašanās vietas direktīvas darbībai atlasiet **Rediģēt vaicājumu** un norādiet **Diapazona** ierakstu, kam ir šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Lauks:** _Atrašanās vietas profila ID_
    - **Kritēriji:** *KPS*

1. Atlasiet **Labi**, lai saglabātu vaicājumu, un saglabājiet jauno atrašanās vietas direktīvu.

Pēc tam jums ir jānomaina esošo pirkšanas pasūtījuma novietojuma direktīvu secība noliktavai 51. Demonstrācijas dati iekļauj divas novietojuma direktīvas, kurām ir **Darba pasūtījuma veida** vērtība uz _Pirkšana_: pirmā ar nosaukumu _51 KPS_, un otra ar nosaukumu _51 PO Direct_. Lai nodrošinātu, ka *Noliktavas procesu kvalitātes pārvaldības* līdzeklis tiek lietots noliktavai 51, ir jāpārliecinās, ka netiek pielietota _51 KPS_ atrašanās vietas direktīva. Tomēr, tā vietā, lai dzēstu šo atrašanās vietas direktīvu (jo, iespējams, vēlēsieties izmantot to nākotnē), varat vienkārši mainīt secību.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Iestatiet lauku **Darba pasūtījuma veids** uz _Pirkšanas pasūtījums_.
1. Secības sarakstā atlasiet sērijas numuru 5 _51 PO Direct_ atrašanās vietas direktīvai.
1. Pārvietojiet atlasīto secību uz sērijas numuru 4.
1. Pārbaudiet, vai _51 KPS_ atrašanās vietas secības numurs tagad ir vismaz 5.

#### <a name="item-sampling"></a>Krājumu iztveršana

Līdzeklis _Noliktavas procesu kvalitātes pārvaldība_ pievieno jaunas krājumu iztveršanas iespējas. **Iztveršanas** vērtība tagad var būt _Pasūtījums_, _Sūtījums_ vai _Noslodze_, un **Iztveršanas daudzuma** vērtība tagad var būt _Pilna noliktavas vienība_.

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Kvalitātes kontrole \> Krājumu iztveršana**.
1. Izveidojiet krājumu iztveršanas ierakstu un iestatiet šādas vērtības:

    - **Krājumu iztveršana:** _3. LP_
    - **Apraksts:** _Katrai trešajai noliktavas vienībai_
    - **Iztveršana:** _Pasūtījums_

1. Kopsavilkuma cilnē **Iztveršanas daudzums** iestatiet **Daudzuma specifikācijas** lauku uz _Pilna noliktavas vienība_.
1. **Procesa** kopsavilkuma cilnē iestatiet lauku **Pēc "n" noliktavas vienības** uz _3_.
1. Sadaļā **Pēc noliktavas dimensijas** iespējojiet gan **Noliktavu**, gan **Krājuma statusu**.

#### <a name="quality-associations"></a>Kvalitātes piesaistes

Izveidot kvalitātes saistību, kas izmantos jauno krājumu iztveršanu.

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Kvalitātes kontrole \> Kvalitātes piesaistes**.
1. Izveidojiet kvalitātes saistības ierakstu un iestatiet šādas vērtības:

    - **Atsauces veids:** _Pirkšana_
    - **Krājuma kods:** _Tabula_
    - **Krājums:** _M9201_
    - **Vieta:** _5_

1. Kopsavilkuma cilnē **Process** iestatiet lauku **Notikuma veids** uz *Reģistrācija*.
1. Kopsavilkuma cilnē **Nosacījumi** iestatiet lauku **Piemērojamais noliktavas veids** uz *Kvalitātes pārvaldība tikai noliktavu procesiem*.
1. Kopsavilkuma cilnē **Kvalitātes pārbaudes pasūtījums process** iestatiet lauku **Kvalitātes apstrādes politika** uz _Izveidot kvalitātes pārbaudes pasūtījumu_.
1. Kopsavilkuma cilnē **Specifikācijas** ar peles labo pogu noklikšķiniet laukā **Testu grupa** un pēc tam atlasiet **Skatīt detalizētu informāciju**, lai atvērtu lapu **Testa grupas**.
1. Lapā **Testa grupas** augšējā režģa cilnē **Pārskats** izveidojiet testa grupu un iestatiet šādas vērtības:

    - **Testa grupa:** _KPS_
    - **Apraksts:** _KPS tests_
    - **Pieņemamais daudzums:** _100_
    - **Krājumu iztveršana:** _3. LP_ (atlasīt)

1. Apakšējās režģa cilnē **Pārskats** pievienojiet viena testa ierakstu un iestatiet šādas vērtības:

    - **Secība:** *1*
    - **Tests:** *Norobežojuma mērīšana*

1. Apakšējā režģa cilnē **Tests** iestatiet šādas vērtības:

    - **Testa mainīgie:** *Nokārtots/Nav nokārtots*
    - **Noklusējuma iznākums:** *Nokārtots*

1. Saglabājiet jauno testa grupu un aizveriet lapu **Testa grupas**.
1. Atgriežoties lapā **Kvalitātes saistības** laukā **Testa grupas** atlasiet **KPS**.
1. Saglabājiet ierakstu.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Mobilās ierīces izvēlnes krājumi ievadītajai kvalitātei

Lai pabeigtu iestatīšanu preču pārvietošanai uz kvalitātes kontroles atrašanās vietu, ir jāizveido kvalitātes krājumu iztveršanas darbs pieejams no mobilās ierīces izvēlnes krājuma.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Atlasiet **Pirkšanas izvietošana** mobilās ierīces izvēlnes krājumu.
1. Kopsavilkuma cilnē **Darba klases** pievienojiet *QualityIn* darba klases ID.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Kopsavilkums: jūsu iestatījumi preču pārvietošanai uz kvalitātes kontroli

Tagad esat noteicis kvalitātes saistību, kas izmanto *Noliktavas procesu kvalitātes pārvaldības* līdzekli, lai aktivizētu kvalitātes pasūtījuma izveidošanu. Jūs esat iestatījis darba un atrašanās vietas datus noliktavai 51, lai nodrošinātu, ka tiek izveidots konkrēts darbs, kad pirkšanas reģistrācija tiek veikta krājumam M9201. Šis iestatījums nodrošina, ka katra reģistrētā trešā noliktavas vienība tiks pārvietota uz kvalitātes atrašanās vietu (_KPS_) un kvalitātes pārbaudes pasūtījums tiks izveidots noliktavas vienības daudzumam. Viss pārējais tiks pārvietots izvietošanai, nevis uz kvalitātes kontroles atrašanās vietu.

### <a name="process-quality-management-work"></a>Procesa kvalitātes pārvaldības darbs

1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Izveidojiet pirkšanas pasūtījumu un iestatiet šādas vērtības:

    - **Norādīt kreditora konts:** *104*
    - **Noliktava:** *51*

1. Pievienojiet pirkšanas pasūtījumu rindu un iestatiet šādas vērtības:

    - **Krājums:** *M9201*
    - **Daudzums:** *20*
    - **UoM:** *ea*
    - **Noliktava:** *51*

1. Pierakstiet pirkšanas pasūtījuma numuru, lai varētu to izmantot vēlāk.
1. Dodieties uz mobilo ierīci vai emulatoru, kas darbina noliktavas programmu, un piesakieties noliktavā 51, izmantojot *51* kā lietotāja ID un *1* kā paroli.
1. Dodieties uz **Ienākošie \> Pirkumu saņemšana** un ievadiet šādas vērtības:

    - **PONum:** Pirkšanas pasūtījuma numurs, ko tikko esat izveidojis
    - **Daudz.:** *5*
    - **Vienība:** *ea*

1. Turpināt saņemt pret rindu *5 ea* vienlaicīgi, līdz rinda tiek pilnībā saņemta. (Kopā tiks izveidotas četras noliktavas vienības.)
1. Izrakstieties no noliktavas programmas.
1. Atpakaļ tīmekļa klientā dodieties uz **Sagāde un avoti \> Pirkšanas pieprasījumi \> Visi pirkšanas pieprasījumi**.
1. Meklēt un atvērt jūsu pirkšanas pasūtījumu.
1. Sadaļā **Pirkšanas pasūtījuma rindas** atlasiet rindu krājuma numuram *M9201* un pēc tam atlasiet **Pirkšanas pasūtījuma rindas \> Darba detalizēta informācija**.
1. Ņemiet vērā, ka izveidotās otrās un trešās darba galvenes ir regulārs izvietošanas darbs, turpretī pirmā un ceturtā darba galvene ir kvalitātes krājuma paraugu izdošanas darbs. Šis rezultāts atbilst krājumu iztveršanas iestatījumam, kas ir konfigurēts katras trešās noliktavas vienības paraugam.

#### <a name="move-to-the-quality-control-location"></a>Pārvietot uz kvalitātes kontroles vietu

Tagad jūs pārvietosiet noliktavas vienības uz to norādītajām vietām. Pirmās un ceturtās noliktavas vienības atgriezīsies kvalitātes kontroles vietā, turpretī otrā un trešā noliktavas vienība dosies tieši uz glabātavu.

1. Dodieties uz mobilo ierīci vai emulatoru, kas darbina noliktavas programmu, un piesakieties noliktavā 51, izmantojot *51* kā lietotāja ID un *1* kā paroli.
1. Dodieties uz **Ienākošie \> Pirkšanas izvietošana** un izlieciet katru noliktavas vienību no iepriekšējās procedūras, līdz esat aizvēris visus darbus.

#### <a name="summary-process-quality-management-work"></a>Kopsavilkums: Procesa kvalitātes pārvaldības darbs

Jūs tagad esat veicis kvalitātes krājumu iztveršanu pirmajai un ceturtajai noliktavas vienībai, pārvietojot tās uz kvalitātes kontroles vietu. Jūs esat izvietojis arī otro un trešo noliktavas vienību. Nākamais solis ir veikt kvalitātes pārbaudes pasūtījumu testu un kontroli.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Izvadītās kvalitātes iestatījumi: pāreja no kvalitātes kontroles vietas uz glabātavu vai atgriešanu

Kad darbinieki pārskata kvalitātes pārbaudes pasūtījuma rezultātus, sistēma automātiski izveido darbu.

Tagad jūs turpināsiet ar nepieciešamo darba klases pamata iestatījumu, darba veidni un novietojuma direktīvu, lai iespējotu noliktavas procesu kvalitātes pārvaldību, lai varētu izveidot nepieciešamo darbu kvalitātes pārbaudes pasūtījuma daudzuma pārvietošanai no kvalitātes kontroles vietas uz norādīto noliktavu atrašanās vietu.

#### <a name="work-class-for-quality-out"></a>Darba klase izvadītajai kvalitātei

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.
1. Izveidojiet darba klasi un iestatiet šādas vērtības:

    - **Darba klases ID:** *QualityOut*
    - **Apraksts:** *Izvadītā kvalitāte*
    - **Darba pasūtījuma veids:** *Kvalitātes pārbaudes pasūtījums*

#### <a name="work-templates"></a>Darba veidnes

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Mainiet **Darba pasūtījuma veida** vērtību uz *Kvalitātes pārbaudes pasūtījums*.
1. Izveidojiet darba veidni un iestatiet šādas vērtības:

    - **Darba veidne:** *51 izvadītā kvalitāte*
    - **Darba veidnes apraksts:** *51 izvadītā kvalitāte*

1. Pievienojiet rindu un iestatiet šādas vērtības:

    - **Darba veids:** *Izdošana*
    - **Darba klases ID:** **QualityOut**

1. Pievienojiet otro rindu un iestatiet šādas vērtības:

    - **Darba veids:** *Izvietošana*
    - **Darba klases ID:** *QualityOut*

#### <a name="location-directives"></a>Vietas direktīvas

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Mainiet **Darba pasūtījuma veida** vērtību uz *Kvalitātes pārbaudes pasūtījums*.
1. Izveidojiet novietojuma direktīvu un iestatiet šādas vērtības:

    - **Nosaukums:** *51 nokārtots*
    - **Darba veids:** *Izvietošana*
    - **Vieta:** *5*
    - **Noliktava:** *51*

1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājuma redaktora dialoglodziņu.
1. Cilnē **Diapazons** iestatiet šādas vērtības:

    - **Tabula:** *Kvalitātes pārbaudes pasūtījumi*
    - **Lauks:** *Statuss*
    - **Kritēriji:** *Nokārtots*

1. Atlasiet **Labi**, lai saglabātu vaicājumu un aizvērtu dialoglodziņu.
1. Kopsavilkuma cilnē **Rindas** pievienojiet rindu un iestatiet šādas vērtības:

    - **No daudzuma:** *1*
    - **Līdz daudzumam:** *1 000 000*

1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** pievienojiet rindu un iestatiet šādu vērtību:

    - **Nosaukums:** *Nokārtots*

1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājuma redaktora dialoglodziņu.
1. Cilnē **Diapazons** iestatiet šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Lauks:** *Zonas ID*
    - **Kritēriji:** *Lielapjoma*

1. Atlasiet **Labi**, lai saglabātu vaicājumu un aizvērtu dialoglodziņu.
1. Darbības rūtī atlasiet **Saglabāt**, lai saglabātu jauno atrašanās vietas direktīvu.
1. Izveidojiet otro novietojuma direktīvu un iestatiet šādas vērtības:

    - **Nosaukums:** *51 nenokārtots*
    - **Darba veids:** *Izvietošana*
    - **Vieta:** *5*
    - **Noliktava:** *51*

1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājuma redaktora dialoglodziņu.
1. Cilnē **Diapazons** iestatiet šādas vērtības:

    - **Tabula:** *Kvalitātes pārbaudes pasūtījumi*
    - **Lauks:** *Statuss*
    - **Kritēriji:** *Nenokārtots*

1. Atlasiet **Labi**, lai saglabātu vaicājumu un aizvērtu dialoglodziņu.
1. Kopsavilkuma cilnē **Rindas** pievienojiet rindu un iestatiet šādas vērtības:

    - **No daudzuma:** *1*
    - **Līdz daudzumam:** *1 000 000*

1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** pievienojiet rindu un iestatiet šādu vērtību:

    - **Nosaukums:** *Nenokārtots*

1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājuma redaktora dialoglodziņu.
1. Cilnē **Diapazons** iestatiet šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Lauks:** *Zonas ID*
    - **Kritēriji:** *Atgriešana*

1. Atlasiet **Labi**, lai saglabātu vaicājumu un aizvērtu dialoglodziņu.
1. Darbības rūtī atlasiet **Saglabāt**, lai saglabātu jauno atrašanās vietas direktīvu.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Mobilās ierīces izvēlnes krājumi izvadītajai kvalitātei

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Atlasiet **KPS izvietošana** mobilās ierīces izvēlnes krājumu.
1. Kopsavilkuma cilnē **Darba klases** pievienojiet *QualityOut* darba klases ID.

Tagad noliktavas darbinieki varēs izvēlēties kvalitātes pārbaudes pasūtījumu darbu, izmantojot **KPS izvietošanas** izvēlnes krājumu. Preces, kuras nenokārtoja kvalitātes kontroli, var novietot atpakaļ atgriešanas vietā, bet preces, kuras nokārtoja kvalitātes kontroli, var novietot lielapjoms-001 vietā.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Kopsavilkums: jūsu iestatījumi preču pārvietošanai no kvalitātes kontroles

Jūs esat iestatījis darba un atrašanās vietas datus noliktavai 51, lai nodrošinātu, ka automātiski tiek izveidots konkrēts darbs, kad kvalitātes pārbaudes pasūtījumi ir pabeigti. Šis iestatījums nodrošina, ka katra kvalitātes kontrolētā noliktavas vienība tiek pārvietota uz lielapjoma atrašanās vietu vai atgriešanas vietu.

### <a name="process-quality-management-work"></a>Procesa kvalitātes pārvaldības darbs

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.
1. Atlasiet pirmo kvalitātes pārbaudes pasūtījumu reģistrētajiem daudzumiem.
1. Atlasiet **Pārbaudīt**. Testa statuss tiek atjaunināts uz *Nenokārtots*.
1. Dodieties uz **Noliktavas paŗvaldība \> Visi darbi**.
1. Atveriet tikko izveidoto darbu un ievērojiet, ka **Darba pasūtījuma veida** vērtība ir *Kvalitātes pārbaudes pasūtījums*. Darbs ietver rindu, kur izvietošanas vieta ir *Atgriezt* un statuss ir *Nenokārtots*. (Ja kvalitātes pārbaudes pasūtījuma statuss bija *Nokārtots*, izvietošanas vieta būs *Lielapjoms* .)
1. Dodieties atpakaļ uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.
1. Atlasiet otro kvalitātes pārbaudes pasūtījumu reģistrētajiem krājumiem.
1. Atlasiet **Rezultāti** virs apakšējā režģa. Atjauniniet **Rezultāta daudzuma** vērtību uz *5* un pārbaudiet, vai **Testa rezultāta** vērtība tiek mainīta uz atzīmi.
1. Atlasiet **Pārbaudīt** un aizveriet lapu.
1. Atgriežoties lapā **Kvalitātes pārbaudes pasūtījumi**, atlasiet **Pārbaudīt** un veiciet pārbaudi. Statuss tiek atjaunināts uz *Nokārtots*.

    > [!NOTE]
    > Pārbaudes notikums aktivizē kvalitātes pārbaudes pasūtījuma darba izveidi, lai pārvietotu daudzumu no kvalitātes kontroles vietas uz jaunu atrašanās vietu.

1. Dodieties uz **Noliktavas pārvaldība \> Visi darbi**.
1. Atlasiet tikko izveidoto darbu un ievērojiet, ka ir izveidots otrs kvalitātes pārbaudes pasūtījuma darba virsraksts, kur izvietošanas vieta ir *LIELAPJOMS-001*.
1. Dodieties uz mobilo ierīci vai emulatoru, kas darbina noliktavas programmu, un piesakieties noliktavā 51, izmantojot *51* kā lietotāja ID un *1* kā paroli.
1. Dodieties uz **Kvalitāte \> Izvietots no KPS**, un apstrādājiet abas noliktavas vienības, kas ir saistītas ar abām darbu vienībām, lai viss darbs tiktu slēgts.

> [!NOTE]
> Apsveriet iespēju pievienot izvadīto kvalitāti uz mobilās ierīces izvēlnes krājumu, kur aktivitātes kods ir *Parādīt atvērto darbu sarakstu*. Piemēram, demonstrācijas datos skatiet mobilās ierīces izvēlnes krājumu ar nosaukumu **Darbu saraksts**. Vispirms pievienojiet *Kvalitātes pārbaudes pasūtījuma* darba klasi uz lietotāja vērstu izvēlnes krājumu, jo šī darba klase ir nepieciešama darbam, kam jāparādās darbu sarakstā. Pēc tam pievienojiet *Kvalitātes pārbaudes pasūtījuma* darba klasi izvēlnes vienumam **Darbu saraksts**. Lietotāji, kuriem ir piekļuve darba sarakstam, pēc tam varēs izvietot un apstrādāt darbu, ko automātiski izveido kvalitātes pārbaudes pasūtījuma apstiprināšana.
