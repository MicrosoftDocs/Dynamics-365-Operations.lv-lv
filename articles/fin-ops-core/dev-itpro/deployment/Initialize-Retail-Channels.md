---
title: Commerce Scale Unit (mākoņa) inicializēšana
description: Šajā rakstā ir izskaidrots, kā inicializēt Commerce Scale Unit (mākonī)Microsoft Dynamics 365 Commerce.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: f9d21de3e498b293394835d5cf564899338b9c18
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474020"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Commerce Scale Unit (mākoņa) inicializēšana

[!include[banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā inicializēt Commerce Scale Unit (mākonī)Microsoft Dynamics 365 Commerce.

Ja izmantojat 2. pakāpes tekstlodziņu vai ražošanas vidi, kuras programmas versija ir 8.1.2.x vai jaunāka, pirms Retail Channel Unit (mākoņa) izmantošanas varat izmantot mazumtirdzniecības kanāla funkcionalitāti vai nu pārdošanas punkta (POS) operācijām, vai e-komercijas operācijām, kas izmanto Mākonī Retail Server. Inicializācija izvietos Commerce Scale Unit (mākonī).

> [!IMPORTANT]
> Lai nodrošinātu nepārtrauktu un netraucētu atbalstu uzņēmējdarbībai, esošajiem debitoriem, kas izmanto mazumtirdzniecības kanāla funkcionalitāti mākonī, mēs pieprasām, lai jūs atjauninātu mazumtirdzniecības kanālus un lietotu Commerce Scale Unit. Jaunas vides, kas izvietotas bez Commerce Scale Unit, vairs nesaņems kvalitātes un pakalpojumu atjauninājumus mākonī viesotajiem mazumtirdzniecības kanāla komponentiem. Klientiem, kuri izmanto tikai Commerce Scale Unit (pašpiegādots), nav jāveic darbība. Ja nepieciešams paplašinājums, sazinieties ar Microsoft FastTrack risinājuma arhitektu.

## <a name="prerequisites"></a>Priekšnosacījumi

1. Izvietojiet pakāpes 2 vadīklu vai ražošanas vidi, kuras versija ir 8.1.2.x vai jaunāka.
2. Jūs varat izvietot līdz 2 Commerce Scale Units vienā vidē. Ja jums ir nepieciešamas vairāk nekā 2 Commerce Scale vienības vienā vidē, Microsoft Dynamics pakalpojumos Lifecycle Services (LCS), **izveidojiet atbalsta pieprasījumu un ievadiet papildu Commerce Scale Unit** pieprasījumu un norādiet vides ID, Commerce Scale Vienību skaitu un vēlamos datu centru reģionus. Pieprasījums tiks izpildīts piecu darba dienu laikā. Ja nav nepieciešams vairāk nekā 2 Commerce Scale Vienības vienā vidē, nav nepieciešams izveidot atbalsta pieprasījumu. 
3. Lai inicializētu Commerce Scale Unit, jums ir jābūt projekta īpašnieka atļaujām pakalpojumos Lifecycle Services.
4. Pārliecinieties, vai vidē ir iespējotas mazumtirdzniecības licences konfigurācijas atslēgas. Papildinformāciju skatiet licences kodu [un konfigurācijas atslēgu pārskatā](../sysadmin/license-codes-configuration-keys-report.md). Lai lietotu Commerce Scale Unit, ir jābūt ieslēgtām šādām atslēgām.

    - RetailBasic
    - RetaileCommerce — ja plānojat izmantot pakalpojumu E-Commerce šim:Dynamics 365 Commerce.
    - RetailGiftCard — ja plānojat izmantot dāvanu kartes.
    - RetailInvent — ja plānojat izmantot krājumus.
    - RetailModernPos — ja plānojat izmantot pārdošanas punktu (POS).
    - RetailReplenishment — ja plānojat izmantot papildināšanu.
    - RetailScheduler (tikai mazumtirdzniecības cenu)
    - RetailStores — ja plānojat izmantot POS.


## <a name="region-availability"></a>Reģiona pieejamība
Commerce Scale Unit ir pieejama izvietošanai tālākajos reģionos.

| Globālā atrašanās vieta | Reģions              | Pieejamība        | Komentāri                  |
|-----------------|---------------------|---------------------|---------------------------|
| AMERICAS        | ASV austrumi             | Vispārēji pieejams |  Nav komentāru.                         |
| AMERICAS        | ASV austrumi 2           | Vispārēji pieejams |  Nav komentāru.                          |
| AMERICAS        | ASV centrālā ziemeļu daļa    | Ierobežota noslodze    |  Nav komentāru.                            |
| AMERICAS        | ASV dienvidu centrālā daļa    | Ierobežota noslodze    |  Nav komentāru.                            |
| AMERICAS        | ASV centrālā daļa          | Vispārēji pieejams |  Nav komentāru.                            |
| AMERICAS        | ASV rietumi             | Vispārēji pieejams |  Nav komentāru.                            |
| AMERICAS        | Rietumu ASV 2           | Vispārēji pieejams |  Nav komentāru.                            |
| AMERICAS        | Kanādas Centrālā      | Ierobežota noslodze    |  Nav komentāru.                            |
| AMERICAS        | Kanādas austrumi         | Ierobežota noslodze    |   Nav komentāru.                           |
| AMERICAS        | Rietumu Centrālā ASV     | Ierobežota noslodze    |   Nav komentāru.                           |
| APAC            | Austrālijas austrumi      | Vispārēji pieejams |   Nav komentāru.                           |
| APAC            | Dienvidaustrumāzija      | Noslodze ierobežota | Izvietošana nav atļauta.    |
| APAC            | Japānas austrumi          | Vispārēji pieejams |  Nav komentāru.                            |
| APAC            | Japānas rietumi          | Vispārēji pieejams |   Nav komentāru.                           |
| APAC            | Austrālijas dienvidaustrumi | Vispārēji pieejams |   Nav komentāru.                           |
| APAC            | Austrumāzija           | Ierobežota noslodze    |   Nav komentāru.                           |
| APAC            | Indijas dienvidi         | Noslodze ierobežota | Izvietošana nav atļauta.    |
| APAC            | Indijas Centrālā       | Ierobežota noslodze    | Nepieciešams apstiprināšanas process. |
| EMEA            | Rietumeiropa         | Vispārēji pieejams    |  Nav komentāru. |
| EMEA            | Ziemeļeiropa        | Vispārēji pieejams    |  Nav komentāru. |
| EMEA            | Apvienotās Karalistes dienvidi            | Vispārēji pieejams |    Nav komentāru.                          |
| EMEA            | Lielbritānijas Rietumi             | Vispārēji pieejams |    Nav komentāru.                          |
| Aae             | Apvienoto Arābu Emirātu ziemeļi           | Ierobežota noslodze    | Nepieciešams apstiprināšanas process. |

Izvietošanas noslodze ierobežotās noslodzes reģionos ir īpaši ierobežota. Izvietošanas pieprasījumi katrā gadījumā tiek novērtēti pēc gadījuma. Ja ir nepieciešama uzņēmējdarbības vajadzība izvietošanai ierobežotās noslodzes reģionos, varat ievadīt atbalsta pieprasījumu pievienošanai gaidīšanas sarakstam. Pašlaik commerce Scale Unit izvietošanai nav atļauta noslodzes ierobežotās zonas. 

![Kartēt, parādot reģiona pieejamību.](media/Commerce-Scale-Unit-Region-Availability.png "Kartēt, parādot reģiona pieejamību")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Inicializēt Commerce Scale Unit kā daļu no jaunas vides izvietošanas

Lūdzu, pārliecinieties, ka galvenais birojs ir pieejams. Inicializācijas procesa laikā ir jāreģistrē mēroga vienība galvenajā birojā. Ja galvenā pārvalde tiek apkalpota, nav ieteicams inicializēt mēroga vienību, jo tā var nebūt pieejama apstrādes procesa laikā.

1. Pārliecinieties, vai galvenā pārvalde ir pieejama, nevis uzturēšanas [režīmā](../sysadmin/maintenance-mode.md).
2. LCS vides informācijas lapā atlasiet Vides līdzekļi **Commerce \>**.
3. Commerce iestatīšanas izvietošanas lapā atlasiet **Inicializēt**.
4. Atlasiet inicializēšanas Commerce Scale Unit versiju.
5. Atlasiet reģionu, kurā inicializēt Commerce Scale Unit.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Konfigurēt kanālus Commerce Scale Unit izmantošanai

Pēc Commerce Scale Unit izvietošanas ir jānodrošina, lai kanāli būtu konfigurēti tās datu bāzes izmantošanai. 

Lai konfigurētu kanālus Commerce Scale Unit datu bāzes izmantošanai, sekojiet šiem soļiem.

1. Programmā Commerce headquarters dodieties uz mazumtirdzniecības **un commerce \> Headquarters iestatīšanas \> Commerce Scheduler \> kanāla datu bāzi**.
1. Kreisajā rūtī atlasiet kanāla datu bāzi.
1. Kopsavilkuma cilnē **Mazumtirdzniecības** kanāls atlasiet **Pievienot** un pēc tam nolaižamajā sarakstā atlasiet mazumtirdzniecības kanālu.
1. Atlasiet **Pievienot** un pēc tam nolaižamajā sarakstā atlasiet tiešsaistes kanālu. 

Kad esat beidzis, dodieties uz **programmu Retail un Commerce \> Retail un commerce IT \> Distribution grafiku** un palaidiet darbu 9999.

> [!NOTE] 
> Darbs 9999 sinhronizē visas jaunās preces un debitorus commerce Scale Unit. Šis process var aizņemt ilgāku laiku. Ja kanālam ir jābūt pieejamam tikai e-komercijas vietnes veidotāja konfigurācijai, darba 9999 vietā varat palaist darbu 1070.

### <a name="database-refresh-and-commerce-scale-units"></a>Datu bāzes atsvaidzināšana un Commerce Scale Units

Pirms sākat, pārliecinieties, vai ir zināmi darbības [, kas jāveic pēc datu bāzes atsvaidzināšanas vidēm, kas izmanto funkcionalitāti](../database/database-refresh.md) Commerce.

Mēroga vienības kanāla datu bāzes ierakstus (kanāla datu bāzes formā) nevar pārvietot vidēs kā daļu no datu bāzes atsvaidzināšanas. Tas ir tāpēc, ka ieraksti pārstāv vidē noteiktu konfigurāciju.

Pēc datu bāzes atsvaidzināšanas, jūs varat reģenerēt mēroga vienības kanāla datu bāzes ierakstu, izsniedzot atkārtoti izvietotu mēroga vienību LCS. Jebkura izvietošanas vai apkalpošanas darbība mēroga vienībā mēģinās galvenajā birojā reģistrēt mēroga vienību, ja tiek konstatēts, ka trūkst reģistrācijas.

Mēroga vienības atkārtotu izvietošanu varat izdot, nemainot komponentus, atlasot izvietot to pašu mēroga vienības versiju, kura jau ir. To var izdarīt LCS, izpildot šādas darbības:

1. Vides detalizētās informācijas lapas LCS sadaļā atlasiet Vides līdzekļi **Mazumtirdzniecība \>**.
2. Iestatīšanas izvietošanas lapā atlasiet mēroga vienību, kuru vēlaties atkārtoti izvietot.
3. Mēroga vienības operāciju izvēlnē atlasiet **Atjaunināt**.
4. Nolaižamā izvēlnē Atlasiet versiju izvēlieties **opciju** Norādīt **versiju**.
5. Teksta lodziņā, kas atrodas sadaļā **Norādiet versiju**, ievadiet mēroga vienībai parādīto versiju, kas parādīta papildus pašreizējās **versijas etiķetei**.
6. Noklikšķiniet uz **pogas** Atjaunināt.

Atjaunināšanas paplašinājumi **nav jāatlasa, pat ja iepriekš esat piemērojis paplašinājumus**, jo pēdējā mēroga vienībai piemērotā paplašinājuma pakotne tiek automātiski paņemta, atjauninot mēroga vienību.

Ja ir vairākas mēroga vienības, ir jāveic operācija virs katras mēroga vienības. Ja vēlaties, šīs operācijas var veikt paralēli.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Izvietot papildu Commerce Scale Vienības (neobligāti)

Ja esat inicializējis Commerce Scale Unit, varat pats izvietot otru mēroga vienību, ja licences tiesības ir tās darīt. Lai izvietotu vairāk nekā divas mēroga vienības, ir jāizveido atbalsta pieprasījums. Atbalsta pieprasījumā ir norādīts nepieciešamo Commerce Scale Vienību skaits, vides nosaukums un vēlamie reģioni. Plašāku informāciju par licencēšanas informāciju skatiet [Dynamics 365 licencēšanas rokasgrāmatā](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Attiecībā uz katru izvietoto papildu Commerce Scale Unit mēs iesakām izveidot atsevišķu kanāla datu bāzes grupu, veicot šādas darbības.

1. Commerce galvenā biroja ejiet uz mazumtirdzniecības **un commerce > Retail Headquarters > mazumtirdzniecības plānotāja > kanāla datu bāzes grupas**.
2. Izveidojiet jaunu kanāla datu bāzu grupu.
3. Dodieties uz **mazumtirdzniecības un commerce > Retail Headquarters > mazumtirdzniecības plānotāja iestatījumiem >** kanāla datu bāzi un atlasiet kanāla datu bāzi, kas atbilst jaunizveidotajai Commerce Scale Unit.
4. Atlasiet **Rediģēt** un atlasiet jauno kanāla datu bāzes grupu.
5. Atlasiet **Saglabāt**.
6. Atlasiet **izpildīt pilnīgu datu sinhronizāciju** atlasītajai kanāla datu bāzei.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Papildu apsvērumi, ja esošajā vidē inicializējiet mākonī viesotos Commerce kanāla komponentus

Ja vidē jau izmantojat mākonī viesotos Commerce kanāla komponentus, Commerce Scale Unit inicializācija palīdzēs samazināt dīkstāves laiku, kad šie komponenti tiek atjaunināti. Pirms Commerce Scale Unit inicializācijas ir nepieciešama papildu plānošana.

Kad inicializēsiet pirmo Commerce Scale vienību vidē, kas izmanto mākonī viesotos Commerce kanāla komponentus, inicializēšanas process migrēs kanālus, kas ir saistīti ar mākonī viesotajiem kanāla komponentiem uz pirmo mēroga vienību. Ar veikala mēroga vienībām saistītie kanāli netiek ietekmēti.

Migrācijas process ir caurredzams kanāliem. Pēc mēroga vienības inicializācijas sākšanas automātiski tiek veiktas šādas operācijas:

1. Tiks izveidota jauna Commerce Scale Unit un saistīta ar vidi.
2. Commerce Scale Unit tiks reģistrēta kā galvenajā birojā pieejama kanāla datu bāze.
3. Visi kanāli, kas ir kartēti **galvenajā** birojā noklusējuma kanāla datu bāzē, tiks atjaunināti tā, lai tos kartētu uz jauno Commerce Scale vienību.
4. Tiks Commerce Data Exchange veikta pilna CDX (CDX) datu sinhronizācija, lai kanāla datus ievietotu jaunajā mēroga vienībā.

**Commerce Scale Unit** inicializācijas plānošana un testēšana kā vispārīgs noteikums, kad tiek inicializēta Commerce Scale Unit, veikala operācijām ir jāplāno piecu stundu dīkstāves logs, kā arī jebkuras e-komercijas kanāla operācijas, kas izmanto Retail Server vai Cloud Point of Sale.

1. Veiciet datu bāzes atsvaidzināšanu no ražošanas vides uz UAT vides kasti. 
2. Inicializējiet Commerce Scale Vienību kastē UAT vidē. 
3. Ievērojiet Commerce Scale Unit inicializēšanas laiku, kas jāpabeidz. Šis process būs salīdzināms ar laiku, kad šī operācija jāveic ražošanas vidē un kuru laikā veikala operācijas un e-komercijas operācijas nav pieejamas.

Pirms Commerce Scale Unit inicializēšanas ir jāveic tālāk norādītās papildu darbības.

- **Slēgt visas POS maiņas** — pēc migrācijas POS lietotāji nevarēs slēgt maiņas, kas migrācijas procesa laikā bija aktīvas.
- **Pārbaudiet, vai visi P darbi** ir veiksmīgi pabeigti - Ir ieteicams, lai P darbi sinhronizētu nenokārtotās darbības, kas ir pabeigtas pirms CSU inicializēšanas.
- **Izrakstīties no visas POS ierīces —** POS operācijas netiek atbalstītas migrācijas laikā.
- **Atsaukt un anulēt visas AIZTURĒTās darbības šeit: POS** - bloķētās darbības netiek saglabātas kā daļa no inicializācijas.

> [!IMPORTANT]
> Kā commerce Scale Unit inicializācijas daļa, iepriekš bloķētās darbības tiks zaudētas, un tās nevar atsaukt. 

Šeit notiek inicializācijas perioda laikā:

- Mākonī viesotie Commerce kanāli nedarbojas, ja netiek ieslēgta POS bezsaistes iespēja.
- POS ierīcēm ar ieslēgtu bezsaistes iespēju būs samazināta funkcionalitāte.
- Visi no Retail Server atkarīgie e-Commerce klienti tiks pārtraukti.
- Netiek ietekmēti kanāli, kas tiek viesoti Commerce Scale units (pašmitinātos).
- Netiek ietekmēta galvenā biroja funkcionalitāte.

Šeit notiek pēc inicializācijas pabeigšanas:

- Visu aktivizēto POS ierīču ierīces aktivizēšanas stāvoklis tiek saglabāts, tas nozīmē, ka ierīces nebūs jāaktivizē atkārtoti.
- Gaidīs aparatūras stacijas instances, turpinās darbu.
- POS kanālu puses pārskati tiks atiestatīti, un dati netiks rādīti pirms inicializācijas.
- Rādīt arī žurnāla operāciju, tiks atiestatīta, un dati netiks rādīti pirms inicializācijas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
