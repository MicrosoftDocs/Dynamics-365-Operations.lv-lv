---
title: Commerce Scale Unit (mākoņa) inicializēšana
description: Šajā tēmā ir paskaidrots, kā inicializēt Commerce Scale Unit (mākonis) programmā Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.openlocfilehash: 84e70515accde161e7efa36755edec68d26be952
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092224"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Commerce Scale Unit (mākoņa) inicializēšana

[!include[banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā inicializēt Commerce Scale Unit (mākonis) programmā Microsoft Dynamics 365 Commerce.

Ja izmantojat 2. līmeņa smilškaste vai ražošanas vidi, kurai ir lietojumprogrammas versija 8.1.2.x vai jaunāka versija, pirms mazumtirdzniecības kanāla funkcionalitātes izmantošanas tirdzniecības vietas (POS) darbībām ir jāinicializē Commerce Scale Unit (mākonis). vai e-komercijas darbībām, kas izmanto Retail Server mākonī. Inicializēšana izvietos Commerce Scale Unit (mākonis).

> [!IMPORTANT]
> Esošajiem klientiem, kuri izmanto mazumtirdzniecības kanālu funkcionalitāti mākonī, lai nodrošinātu nepārtrauktu un nepārtrauktu jūsu uzņēmuma atbalstu, mēs pieprasām, lai jūs atjauninātu savus mazumtirdzniecības kanālus, lai izmantotu Commerce Scale Unit. Jaunās vides, kas izvietotas bez Commerce Scale Unit, vairs nesaņems mākoņa mitināto mazumtirdzniecības kanālu komponentu kvalitātes un pakalpojumu atjauninājumus. Klientiem, kuri izmanto tikai Commerce Scale Unit (pašmitināti), nav jāveic nekādas darbības. Ja nepieciešams paplašinājums, sazinieties ar savu Microsoft FastTrack risinājumu arhitektu.

## <a name="prerequisites"></a>Priekšnosacījumi

1. Izvietojiet 2. līmeņa smilškaste vai ražošanas vidi, kuras versija ir 8.1.2.x vai jaunāka.
2. Vienā vidē varat patstāvīgi izvietot līdz 2 komercijas mēroga vienībām. Ja jums ir nepieciešamas vairāk nekā 2 tirdzniecības mēroga vienības vienā vidē,Microsoft Dynamics Lifecycle Services (LCS), izveidojiet atbalsta pieprasījumu un ievadiet **Pieprasīt papildu tirdzniecības mērogu vienību** un norādiet vides ID, tirdzniecības mēroga vienību skaitu un vēlamos datu centra reģionus. Pieprasījums tiks izpildīts piecu darba dienu laikā. Ja jums nav nepieciešamas vairāk par 2 Commerce Scale Units vienā vidē, jums nav jāizveido atbalsta pieprasījums. 
3. Lai varētu inicializēt Commerce Scale Unit, jums ir jābūt projekta īpašnieka atļaujām pakalpojumā Lifecycle Services.
4. Pārliecinieties, vai jūsu vidē ir iespējotas mazumtirdzniecības licences konfigurācijas atslēgas. Papildinformāciju skatiet [Licenču kodu un konfigurācijas atslēgu pārskats](../sysadmin/license-codes-configuration-keys-report.md). Lai izmantotu Commerce Scale Unit, ir jābūt ieslēgtiem tālāk norādītajiem taustiņiem.

    - RetailBasic
    - RetaileCommerce — ja plānojat izmantot e-komerciju Dynamics 365 Commerce.
    - RetailGiftCard — ja plānojat izmantot dāvanu kartes.
    - RetailInvent — ja plānojat izmantot krājumus.
    - RetailModernPos — ja plānojat izmantot tirdzniecības vietu (POS).
    - RetailReplenishment — ja plānojat izmantot papildināšanu.
    - RetailScheduler
    - Mazumtirdzniecības veikali — ja plānojat izmantot POS.


## <a name="region-availability"></a>Reģiona pieejamība
Commerce Scale Unit ir pieejams izvietošanai tālāk norādītajos reģionos.

| Globālā atrašanās vieta | Reģions              | Pieejamība        |
|-----------------|---------------------|---------------------|
| AMERIKA        | ASV austrumi             | Vispārēji pieejams |
| AMERIKA        | ASV austrumi 2           | Vispārēji pieejams |
| AMERIKA        | ASV centrālā ziemeļu daļa    | Vispārēji pieejams |
| AMERIKA        | ASV dienvidu centrālā daļa    | Vispārēji pieejams |
| AMERIKA        | ASV centrālā daļa          | Vispārēji pieejams |
| AMERIKA        | ASV rietumi             | Vispārēji pieejams |
| AMERIKA        | ASV rietumi 2           | Vispārēji pieejams |
| AMERIKA        | Kanādas centrālā daļa      | Ierobežota jauda    |
| AMERIKA        | Kanādas austrumi         | Ierobežota jauda    |
| AMERIKA        | ASV rietumu centrālā daļa     | Ierobežota jauda    |
| APAC            | Austrālijas austrumi      | Vispārēji pieejams |
| APAC            | Dienvidaustrumāzija      | Vispārēji pieejams |
| APAC            | Japānas austrumi          | Vispārēji pieejams |
| APAC            | Japānas rietumi          | Vispārēji pieejams |
| APAC            | Austrālijas dienvidaustrumi | Ierobežota jauda    |
| APAC            | Austrumāzija           | Ierobežota jauda    |
| APAC            | Indijas dienvidi         | Ierobežota jauda    |
| APAC            | Indijas centrālā daļa       | Ierobežota jauda    |
| EMEA            | Rietumeiropa         | Vispārēji pieejams |
| EMEA            | Ziemeļeiropa        | Vispārēji pieejams |
| EMEA            | Apvienotās Karalistes dienvidi            | Ierobežota jauda    |
| EMEA            | Apvienotās Karalistes rietumi             | Ierobežota jauda    |

Izvēršanas jauda ierobežotas jaudas reģionos ir ārkārtīgi ierobežota. Izvēršanas pieprasījumi tiek izvērtēti katrā gadījumā atsevišķi. Ja jums ir pārliecinoša biznesa vajadzība pēc izvietošanas ierobežotas jaudas reģionos, varat iesniegt atbalsta pieprasījumu, lai to pievienotu gaidīšanas sarakstam.

![Karte, kurā parādīta reģiona pieejamība.](media/Commerce-Scale-Unit-Region-Availability.png "Karte, kurā redzama reģiona pieejamība")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Inicializējiet Commerce Scale Unit kā daļu no jaunas vides izvietošanas

Lūdzu, pārliecinieties, vai galvenā mītne ir pieejama. Tas ir nepieciešams, lai inicializācijas procesa laikā reģistrētu mēroga vienību galvenajā mītnē. Nav ieteicams inicializēt skalas vienību, kad galvenajā mītnē tiek veikta apkope, jo apkopes procesa laikā tā var kļūt nepieejama.

1. Pārliecinieties, vai galvenā mītnes vide ir pieejama, nevis tajā [Apkopes režīms](../sysadmin/maintenance-mode.md).
2. LCS vides informācijas lapā atlasiet **Vides īpašības \> komercija**.
3. Tirdzniecības iestatīšanas izvietošanas lapā atlasiet **Palaist**.
4. Atlasiet inicializējamo Commerce Scale Unit versiju.
5. Atlasiet reģionu, kurā inicializēt Commerce Scale Unit.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Konfigurējiet kanālus, lai izmantotu Commerce Scale Unit

Pēc Commerce Scale Unit izvietošanas jums ir jāpārliecinās, ka jūsu kanāli ir konfigurēti, lai tam izmantotu datu bāzi. 

Lai konfigurētu kanālus Commerce Scale Unit datu bāzes lietošanai, veiciet šīs darbības.

1. Tirdzniecības galvenajā mītnē dodieties uz **Mazumtirdzniecība un tirdzniecība \> Galvenās mītnes iestatīšana \> Tirdzniecības plānotājs \> Kanālu datu bāze**.
1. Kreisajā rūtī atlasiet kanālu datu bāzi.
1. Uz **Mazumtirdzniecības kanāls** FastTab, atlasiet **Pievienot** un pēc tam nolaižamajā sarakstā atlasiet savu mazumtirdzniecības kanālu.
1. Izvēlieties **Pievienot** un pēc tam nolaižamajā sarakstā atlasiet savu tiešsaistes kanālu. 

Kad esat pabeidzis, dodieties uz **Mazumtirdzniecība un tirdzniecība \> Mazumtirdzniecības un tirdzniecības IT \> Izplatīšanas grafiks**, un palaist darbu 9999.

> [!NOTE] 
> Darbs 9999 sinhronizē visus jaunos produktus un klientus ar Commerce Scale Unit. Šis process var aizņemt ilgu laiku. Ja kanālam ir jābūt pieejamam tikai e-komercijas vietņu veidotāja konfigurēšanai, varat palaist darbu 1070, nevis darbu 9999.

### <a name="database-refresh-and-commerce-scale-units"></a>Datu bāzes atsvaidzināšana un tirdzniecības mēroga vienības

Pirms sākat, pārliecinieties, vai esat iepazinies ar [Darbības, kas jāveic pēc datu bāzes atsvaidzināšanas vidēm, kurās tiek izmantota Commerce funkcionalitāte](../database/database-refresh.md).

Mēroga vienības kanālu datu bāzes ierakstus (veidlapā Kanālu datu bāze) nevar pārvietot starp vidēm datu bāzes atsvaidzināšanas ietvaros. Tas ir tāpēc, ka ieraksti atspoguļo videi specifisku konfigurāciju.

Pēc datu bāzes atsvaidzināšanas varat reģenerēt mēroga vienības kanāla datu bāzes ierakstu, izdodot mēroga vienības atkārtotu izvietošanu LCS. Jebkāda izvietošanas vai apkalpošanas darbība mēroga vienībā mēģinās reģistrēt skalas vienību galvenajā mītnē, ja tiks konstatēts, ka reģistrācija trūkst.

Varat izdot mēroga vienības atkārtotu izvietošanu, nemainot nevienu komponentu, atlasot izvietot to pašu versiju, kurā jau ir jūsu mēroga vienība. To var izdarīt LCS, veicot šādas darbības:

1. LCS vides informācijas lapā atlasiet **Vides īpašības \> Mazumtirdzniecība**.
2. Iestatīšanas izvietošanas lapā atlasiet mēroga vienību, kuru vēlaties atkārtoti izvietot.
3. Svaru vienības darbības izvēlnē atlasiet **Atjaunināt**.
4. Slīdnī, nolaižamajā izvēlnē **Izvēlieties versiju**, izvēlieties opciju **Norādiet versiju**.
5. Tekstlodziņā zem **Norādiet versiju**, ierakstiet jūsu skalas vienībai parādīto versiju, kas parādīta blakus simbolam **Pašreizējā versija** etiķete.
6. Klikšķiniet uz **Atjaunināt** pogu.

Jums nav nepieciešams atlasīt **Atjauniniet paplašinājumus**, pat ja paplašinājumus esat lietojis iepriekš, jo pēdējā skalas vienībai lietotā paplašinājumu pakotne tiek automātiski atlasīta, atjauninot skalas vienību.

Ja jums ir vairākas skalas vienības, katrai skalas vienībai ir jāveic iepriekš minētā darbība. Ja nepieciešams, šīs darbības var veikt paralēli.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Izvietot papildu Commerce mēroga vienības (pēc izvēles)

Kad esat inicializējis Commerce Scale Unit, varat paši izvietot otru mēroga vienību, ja jūsu licence jums dod tiesības to darīt. Lai izvietotu vairāk nekā divas mēroga vienības, ir jāizveido atbalsta pieprasījums. Atbalsta pieprasījumā norādiet nepieciešamo Commerce Scale Units skaitu, vides nosaukumu un vēlamos reģionus. Papildinformāciju par licencēšanu skatiet [Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Katrai papildu izvietotajai Commerce Scale vienībai ieteicams izveidot atsevišķu kanālu datu bāzes grupu, veicot šīs darbības.

1. Sadaļā Commerce galvenais birojs dodieties uz **Mazumtirdzniecības un tirdzniecības > Retail Headquarters > Retail Scheduler iestatīšanas > kanālu datu bāzes grupu**.
2. Izveidojiet jaunu kanāla datu bāzu grupu.
3. Dodieties uz **mazumtirdzniecības un tirdzniecības > Retail Headquarters > mazumtirdzniecības plānotāja iestatīšanas > kanāla datu bāzi** un atlasiet kanālu datu bāzi, kas atbilst jaunizveidotajai Commerce Scale Unit.
4. Atlasiet **Rediģēt** un atlasiet jauno kanālu datu bāzes grupu.
5. Atlasiet **Saglabāt**.
6. Atlasītajai kanālu datu bāzei atlasiet **Palaist pilnu datu** sinhronizāciju.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Papildu apsvērumi, ja inicializējat mākonī viesotus Commerce kanāla komponentus esošā vidē

Ja vidē jau izmantojat mākonī viesotus Commerce kanāla komponentus, Commerce Scale Unit inicializācija palīdzēs samazināt dīkstāvi, atjauninot šos komponentus. Pirms Commerce Scale Unit inicializēšanas ir nepieciešama papildu plānošana.

Inicializējot savu pirmo Commerce mēroga vienību vidē, kas izmanto mākoņa viesotus Commerce kanāla komponentus, inicializācijas process migrēs jūsu kanālus, kas saistīti ar mākoņa viesotajiem kanāla komponentiem, uz pirmā mēroga vienību. Kanāli, kas saistīti ar store scale vienībām, netiek ietekmēti.

Migrācijas process kanāliem ir pārredzams. Pēc mēroga vienības inicializācijas sākuma automātiski tiek veiktas šādas darbības:

1. Tiks izveidota jauna Commerce Scale Unit, kas tiks saistīta ar vidi.
2. Commerce Scale Unit tiks reģistrēta kā pieejama kanālu datu bāze galvenajā mītnē.
3. Visi kanāli, kas kartēti uz **noklusējuma** kanālu datu bāzi galvenajā mītnē, tiks atjaunināti, lai kartētu uz jauno Commerce Scale Vienību.
4. Tiks Commerce Data Exchange veikta (CDX) pilna datu sinhronizācija, lai kanāla dati iesēdinātu jaunajā mēroga vienībā.

**Plānošana un testēšana Commerce Scale Unit inicializācijai** Parasti, inicializējot Commerce Scale Unit, ir jāplāno piecu stundu dīkstāves logs veikala operācijām, kā arī visām e-komercijas kanāla operācijām, kas izmanto Retail Server vai Cloud Point of Sale.

1. Veiciet datu bāzes atsvaidzināšanu no ražošanas vides uz smilškastes UAT vidi. 
2. Inicializēt Commerce Scale Unit smilškastes UAT vidē. 
3. Ņemiet vērā Commerce Scale Unit inicializācijas laiku. Tas būs salīdzināms ar laiku, ko šī operācija aizņem jūsu ražošanas vidē, kuras laikā veikala darbība un e-komercijas darbības nebūs pieejamas.

Pirms Commerce Scale Unit inicializēšanas ir jāveic šādas papildu darbības.

- **Aizveriet visas POS maiņas** — pēc migrēšanas POS lietotāji nevarēs aizvērt nekādas maiņas, kas bija aktīvas migrācijas procesa laikā.
- **Pārbaudiet, vai visi P darbi ir veiksmīgi pabeigti** – ieteicams, lai P darbi, lai sinhronizētu gaidošās darbības, ir pabeigti pirms CSU inicializēšanas.
- **Izrakstieties no visām POS ierīcēm** - POS operācijas migrācijas laikā netiek atbalstītas.
- **Atsaukt un anulēt visas POS** apturētās darbības – apturētās darbības netiek saglabātas kā daļa no inicializācijas.

> [!IMPORTANT]
> Kā daļa no Commerce Scale Unit inicializācijas iepriekšējie apturētie darījumi tiks zaudēti, un tos nevar atsaukt. 

Lūk, kas notiek inicializācijas periodā:

- Mākonī viesoti Commerce kanāli nedarbosies, ja vien neieslēgsit POS bezsaistes iespēju.
- POS ierīcēm, kurās ir ieslēgtas bezsaistes iespējas, būs samazināta funkcionalitāte.
- Visi e-komercijas klienti, kas ir atkarīgi no Retail Server, tiks pārtraukti.
- Kanāli, kas tiek viesoti commerce scale units (pašvadīti), netiks ietekmēti.
- Galvenā biroja funkcionalitāte netiek ietekmēta.

Lūk, kas notiek pēc inicializācijas pabeigšanas:

- Tiek saglabāts visu aktivizēto POS ierīču aktivizācijas stāvoklis, kas nozīmē, ka ierīces nebūs jāaktivizē no jauna.
- Savrupas aparatūras staciju instances turpinās darboties.
- POS kanāla puses atskaites tiks atiestatītas un nerādīs datus pirms inicializēšanas.
- Rādīt žurnāla operāciju arī tiks atiestatīta un nerādīs datus no pirms inicializēšanas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
