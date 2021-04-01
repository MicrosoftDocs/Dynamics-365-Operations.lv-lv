---
title: Visu kanālu maksājumu apskats
description: Šajā tēmā ir sniegts apskats par visu kanālu maksājumiem programmā Dynamics 365 Commerce.
author: rubendel
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 3fe64dad3c60560363428d76566d910868b87111
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244915"
---
# <a name="omni-channel-payments-overview"></a>Visu kanālu maksājumu apskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts apskats par visu kanālu maksājumiem programmā Dynamics 365 Commerce. Tajā ir visaptverošs atbalstīto scenāriju saraksts, informācija par funkcionalitāti, iestatīšanu un problēmu novēršanu, kā arī dažu tipisko problēmu apraksti.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | Apraksts |
|---|---|
| Marķieris | Datu virkne, ko maksājuma apstrādātājs nodrošina kā atsauci. Marķieri var būt maksājumu karšu numuri, maksājumu autorizācijas un iepriekšējo maksājumu iegūšana. Marķieri ir svarīgi, jo tie palīdz uzturēt sensitīvos datus ārpus pārdošanas punkta (point of sale — POS) sistēmas. Dažreiz tos sauc arī par *atsaucēm*. |
| Kartes marķieris | Marķieris, ko maksājuma apstrādātājs nodrošina glabāšanai POS sistēmā. Kartes marķieri var izmantot tikai tirgotājs, kurš to saņem. Karšu marķierus reizēm sauc arī par *karšu atsaucēm*. |
| Autorizācijas marķieris | Unikāls ID, ko maksājuma apstrādātājs nodrošina kā daļu no atbildes, ko tas nosūta uz POS sistēmu pēc tam, kad POS sistēma veic autorizācijas pieprasījumu. Autorizācijas marķieri var izmantot vēlāk, ja apstrādātājs tiek aicināts veikt tādas darbības kā autorizācijas apgriešanu vai anulēšanu. Taču visbiežāk to izmanto, lai iegūtu līdzekļus, kad pasūtījums ir izpildīts vai transakcija ir finalizēta. Autorizācijas marķierus reizēm sauc arī par *autorizācijas atsaucēm*. |
| Iegūšanas marķieris | Atsauce, ko maksājuma apstrādātājs nodrošina POS sistēmai, kad maksājums ir finalizēts vai iegūts. Iegūšanas marķieri pēc tam var izmantot, lai atsauktos uz maksājuma iegūšanu turpmākās operācijās, piemēram, atmaksas pieprasījumos. | 
| Kartes nav | Termins, kas attiecas uz maksājumu transakcijām, kurās nav norādīta fiziska karte. Piemēram, šīs transakcijas var notikt e-komercijas vai zvanu centra scenārijos. Šīm transakcijām ar maksājumu saistītā informācija tiek manuāli ievadīta e-komercijas tīmekļa vietnē, zvanu centra plūsmā vai POS vai maksājumu terminālī. |
| Karte ir | Termins, kas attiecas uz maksājumu transakcijām, kur fiziska karte tiek norādīta un lietota maksājumu terminālī, kurš ir savienots ar Microsoft Dynamics 365 POS sistēmu. |

## <a name="overview"></a>Kopsavilkums

Parasti termins *visu kanālu maksājumi* apraksta iespēju izveidot pasūtījumu vienā kanālā un izpildīt to citā kanālā. Galvenais visu kanālu maksājumu atbalsta princips ir maksājuma informācijas saglabāšana kopā ar pārējo pasūtījuma informāciju, un pēc tam šīs maksājuma informācijas izmantošana, kad attiecīgais pasūtījums tiek atkal izsaukts vai apstrādāts citā kanālā. Klasisks piemērs ir scenārijs “Pirkt tiešsaistē, saņemt veikalā”. Šajā scenārijā maksājuma informācija tiek pievienota, kad pasūtījums tiek izveidots tiešsaistē. Pēc tam šī informācija tiek atkal izsaukta POS, lai saņemšanas laikā iekasētu no klienta maksājumu kartes. 

Visus šajā tēmā aprakstītos scenārijus var ieviest, izmantojot standarta maksājumu programmatūras izstrādes komplektu (SDK), kas ir iekļauts Commerce komplektācijā. Tēmā [Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) ir sniegta ikviena šeit aprakstītā scenārija ieviešana standarta komplektācijā. 

### <a name="prerequisites"></a>Priekšnosacījumi

Katram šajā tēmā aprakstītajam scenārijam ir nepieciešams maksājumu savienotājs, kas atbalsta visu kanālu maksājumus. Var izmantot arī standarta komplektācijā ietverto Adyen savienotāju, jo tas atbalsta scenārijus, kuri ir padarīti pieejami, izmantojot maksājumu SDK. Lai uzzinātu papildinformāciju par to, kā ieviest maksājumu savienotājus, un par Retail SDK vispār, apmeklējiet [mājas lapu Retail IT speciālistiem un izstrādātājiem](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Atbalstītās versijas

Šajā tēmā aprakstītās visu kanālu maksājumu iespējas tika izlaistas kā daļa no Microsoft Dynamics 365 for Retail versijas 8.1.3. 

#### <a name="card-present-and-card-not-present-connectors"></a>Savienotāji “karte ir” un “kartes nav”

Maksājumu SDK paļaujas uz divām maksājumiem paredzētu lietojumprogrammu programmēšanas interfeisu (application programming interface — API) kopām. Pirmās API kopas nosaukums ir **iPaymentProcessor**. Tā tiek izmantota, lai ieviestu maksājumu savienotājus “kartes nav”, kurus var izmantot visos zvanu centros un ar Microsoft Dynamics e-komercijas platformu. Plašāku informāciju par interfeisu **iPaymentProcessor** skatiet tehniskajā dokumentā [Maksājumu savienotāja un maksājumu ierīces ieviešana](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf), kurā ir aprakstīti maksājumi. 

Otrās API kopas nosaukums ir **iNamedRequestHandler**. Tā atbalsta maksājumu “karte ir” ieviešanu, kas izmanto maksājumu termināli. Plašāku informāciju par interfeisu **iNamedRequestHandler** skatiet tēmā [Maksājumu integrācijas izveidošana maksājumu terminālim](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Ir nepieciešami tālāk norādītie komponenti un iestatīšanas soļi.

- **E-komercijas integrācija:** ir nepieciešama integrācija ar Commerce lai atbalstītu scenārijus, kur pasūtījuma izcelsme ir tiešsaistes vitrīna. Plašāku informāciju par Retail e-komercijas SDK skatiet tēmā [E-komercijas platformas programmatūras izstrādes komplekts (SDK)](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). Demonstrācijas vidē atsauces vitrīna atbalsta visu kanālu maksājumu scenārijus. 
- **Tiešsaistes maksājumu konfigurācija:** tiešsaistes kanāla iestatīšanai ir jāietver maksājumu savienotājs, kas ir atjaunināts, lai atbalstītu visu kanālu maksājumus. Var arī izmantot standarta komplektācijā ietverto maksājumu savienotāju. Informāciju par to, ka konfigurēt Adyen maksājumu savienotāju tiešsaistes veikaliem, skatiet tēmā [Adyen maksājumu savienotājs](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce). Papildus šajā tēmā aprakstītajai e-komercijas iestatīšanai, Adyen savienotāja iestatījumos parametra **Ļaut maksājumu informācijas saglabāšanu e-komercijā** vērtība ir jāiestata uz **True**. 
- **Visu kanālu maksājumu konfigurācija:** iekšējās uzskaites daļā dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Commerce koplietojamie parametri**. Pēc tam cilnē **Visu kanālu maksājumi** opcijai **Izmantot visu kanālu maksājumus** iestatiet vērtību **Jā**. Commerce versijās 10.0.12 un jaunākās versijās šis iestatījums ir **Funkciju pārvaldības** darbvietā. Atlasiet **Universālā kanāla maksājumu** funkciju un noklikšķiniet uz **Iespējot tūlīt**. 
- **Maksājumu pakalpojumi:** lai apstrādātu maksājumus, zvanu centrs izmanto noklusējuma maksājumu savienotāju lapā **Maksājumu pakalpojumi**. Lai atbalstītu tādus scenārijus kā, piemēram, “Pirkt zvanu centrā, saņemt veikalā”, šim noklusējuma maksājumu savienotājam ir jābūt Adyen maksājumu savienotājam vai maksājumu savienotājam, kas atbilst visu kanālu maksājumu ieviešanas prasībām.
- **EFT pakalpojums:** maksājumiem caur maksājumu termināli ir jābūt iestatītiem aparatūras profila kopsavilkuma cilnē **EFT pakalpojums**. Adyen savienotājs atbalsta standarta komplektācijā ietvertos visu kanālu maksājumu scenārijus. Var izmantot arī citus maksājumu savienotājus, kas atbalsta interfeisu **iNamedRequestHandler**, ja tie atbalsta visu kanālu maksājumus.
- **Maksājumu savienotāja pieejamība:** kad tiek atkal izsaukts kāds pasūtījums, maksājuma norēķina rindas, kas tiek atkal izsauktas kopā ar šo pasūtījumu, ietver tā maksājumu savienotāja nosaukumu, kurš tika izmantots ar šo pasūtījumu saistīto autorizāciju izveidošanai. Kad pasūtījums ir izpildīts, maksājumu SDK mēģina izmantot to pašu savienotāju, kas tika izmantots sākotnējās autorizācijas izveidošanai. Tādēļ maksājumu savienotājam, kuram ir tādi paši tirgotāja rekvizīti, ir jābūt pieejamam tveršanai. 
- **Karšu tipi:** lai visu kanālu scenāriji darbotos pareizi, katram kanālam ir nepieciešams tāds pats norēķinu tipu iestatījums, kādu var izmantot visiem kanāliem. Šis iestatījums ietver maksāšanas metodes ID un kartes tipa ID. Piemēram, ja norēķinu tipam **Kartes** tiešsaistes veikala iestatījumā identifikators (ID) ir **2**, arī mazumtirdzniecības veikala iestatījumā šim tipam ir nepieciešams tāds pats ID. Tādas pašas prasības attiecas arī uz kartes tipa ID. Ja tiešsaistes veikalā kartes numurs **12** ir iestatīts kā **VISA**, arī mazumtirdzniecības veikalā tam ir jāiestata tāds pats ID. 
- Retail Modern POS operētājsistēmai Windows ar Android ar iebūvētu aparatūras staciju -vai-
- Modern POS operētājsistēmai iOS vai Cloud POS ar savienotu koplietojamo aparatūras staciju. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Visu kanālu maksājumu atbalsta pamatprincips

Maksājumu savienojumi un maksājumu apstrādātāji izmanto marķierus jeb atsauces, lai atsauktos uz mijiedarbībām, kas ir saistītas ar karšu maksājumiem. Piemēram, kad tiek pieprasīta maksājuma autorizācija, tiek norādīta atsauce uz šo autorizāciju. Tādēļ uz autorizāciju var atsaukties vēlāk, kad izpildīšanas laikā tiek iegūti līdzekļi. Tirgotājam, maksājumu savienotājam un apstrādātājam šī autorizācija ir unikāla. 

Ja tiešsaistē izveidots pasūtījums tiek saņemts veikalā, šim pasūtījumam ir atkal jāizsauc un jālieto tā pati maksājuma informācija. Kad sākotnējā informācija tiek sniegta kā daļa no pieprasījuma iegūt maksājumu pret sākotnējo autorizāciju, maksājuma apstrādātājs var apstrādāt pieprasījumu un iegūt maksājumu. 

Lai pareizi atsauktos uz tiešsaistes pasūtījumu, ir jābūt pieejamam arī maksājumu savienotājam “kartes nav”, kas atbalsta to pašu apstrādātāju. Šādi POS sistēmai var būt viens apstrādātājs maksājumiem “karte ir”, bet tam var būt piekļuve arī citiem maksājumu savienotājiem, lai tas varētu izpildīt citos kanālos izveidotus pasūtījumus, izmantojot dažādus maksājumu apstrādātājus. 

## <a name="supported-scenarios"></a>Atbalstītie scenāriji

Tiek atbalstīti tālāk norādītie visu kanālu maksājumu scenāriji.

- Pirkt tiešsaistē, saņemt veikalā
- Pirkt zvanu centrā, saņemt veikalā
- Pirkt veikalā A, saņemt veikalā B
- Pirkt veikalā A, nosūtīt klientam

    > [!NOTE]
    > Zvanu centrā veiktie maksājumi, kas kartēti ar norēķinu funkciju “Parasts”, ir jāatzīmē kā **Priekšapmaksa** = **Jā**, lai tie tiktu atspoguļoti maksājamajā summā, atsaucot pasūtījumu POS. Maksājumi, kas nav priekšapmaksas, ar tipu “Parasts” netiek atpazīti, kad pasūtījums tiek atsaukts POS. 

Tiek atbalstītas arī šo scenāriju variācijas. Piemēram, tiešsaistes pasūtījumā var būt ietvertas gan rindas, kas tiks nosūtītas klientam, gan rindas, kas tiks saņemtas veikalā. Visas pasūtījumu izpildes opcijas tiek atbalstītas, izmantojot visu kanālu maksājumus. 

Nākamajās sadaļās ir aprakstītas darbības katram scenārijam un parādīts, kā palaist scenāriju, izmantojot demonstrācijas datus. 

### <a name="buy-online-pick-up-in-store"></a>Pirkt tiešsaistē, saņemt veikalā

Pirms sākat, jums ir jāpārliecinās, vai ir izpildīti tālāk norādītie priekšnosacījumi.

- Jums ir atsauces vitrīna, kur ir konfigurēts Adyen savienotājs.
- Opcija **Visu kanālu maksājumi** lapā **Commerce koplietojamie parametri** ir iestatīta uz **True**. Jaunākās versijās šis iestatījums tiek pārvietots uz **Funkciju pārvaldības** darbvietu, kur varat izvēlēties **Universālā kanāla maksājumu** funkciju un noklikšķiniet uz **Iespējot tūlīt**. 
- Adyen maksājumu savienotājs ir konfigurēts Hjūstonas POS reģistram.
- Retail Modern POS operētājsistēmai Windows ar Android ar iebūvētu aparatūras staciju -vai-
- Modern POS operētājsistēmai iOS vai Cloud POS ar savienotu koplietojamo aparatūras staciju. 

Lai palaistu šo scenāriju, izpildiet tālāk aprakstītās darbības.

1. Atsauces vitrīnā izveidojiet pasūtījumu saņemšanai veikalā. Noteikti atlasiet veikalu **Hjūstona**. 
2. Izpildiet norēķināšanās procedūru un samaksājiet, izmantojot testa kredītkartes numuru. Testa kredītkaršu numuri ir atrodami [Adyen testa karšu numuru lapā](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. Programmā Commerce izmantojiet pakešuzdevumu **Sinhronizēt pasūtījumus** un sadales grafiku **P-001**, lai izveidotu pasūtījumus iekšējās uzskaites daļā.
4. Pārdošanas punkta (POS) sveiciena lapā atlasiet operāciju **Saņemamie pasūtījumi**, lai redzētu pasūtījumus, kurus ir paredzēts saņemt veikalā. 
5. Atlasiet vienu vai vairākas rindas no pasūtījuma, kurš tika izveidots atsauces vitrīnā, un pēc tam atlasiet **Saņemt**.

    Pasūtījums tiek izgūts no iekšējās uzskaites daļas. 

6. Kad pasūtījuma rindas informācija ir izgūta no iekšējās uzskaites daļas un tiek konstatēts kartes maksājums, ko var izmantot visiem kanāliem, jūs tiekat informēts, ka ir pieejama maksāšanas metode.
7. Atlasiet **Izmantot pieejamu maksāšanas metodi**, lai pabeigtu transakciju, izmantojot atsauces vitrīnā ievadīto kartes informāciju.

    Pasūtījuma rindas tiek ielādētas transakcijas lapā, un apmaksājamā bilance ir 0 (nulle). 

8. Atlasiet cilni **Maksājumi**, lai skatītu norēķinu rindu, kas tika izgūta no tiešsaistes pasūtījuma. 
9. Atlasiet jebkuru maksāšanas metodi, lai pabeigtu šo transakciju. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Pirkt zvanu centrā, saņemt veikalā

1. Programmas Commerce lapas **Klientu apkalpošana** meklēšanas lodziņā ievadiet **Zane Siliņa** un pēc tam atlasiet **Meklēt**. 
3. Meklēšanas rezultātos atlasiet **Zane Siliņa**.
4. Kad Zane ir ielādēta lapā **Klientu apkalpošana**, atlasiet **Jauns pārdošanas pasūtījums**.
5. Jaunā pārdošanas pasūtījuma lapā atlasiet **Virsraksts**, lai apskatītu pasūtījuma virsrakstu. 
6. Lapā **Pasūtījuma virsraksts** iestatiet vietu uz **Centrāle** un noliktavu uz **Hjūstona**.
7. Cilnē **Piegādāt** lauku **Piegādes veids** iestatiet uz **60** izsniegšanai klientiem.
8. Atlasiet **Rindas** un pēc tam pievienojiet pasūtījumam vienu vai vairākas rindas. 
9. Atlasiet **Pabeigt**, lai pasūtījumu ievadītu pabeigšanas plūsmā.
10. Ritiniet uz leju līdz maksājumu sadaļai, atlasiet **Pievienot** un pēc tam atlasiet rindu, kur maksāšanas metodes tips ir iestatīts uz **Kartes**. 
11. Atlasiet plus zīmi (**+**), lai pievienotu kartes maksājumu. 
12. Ievadiet informāciju par testa kredītkartes numuru, kuru atradāt [Adyen testa karšu numuru lapā](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description), un pēc tam atlasiet **Labi**.

    > [!NOTE]
    > Ja jūsu ievadītā kartes numura zīmols atšķiras no zīmola, kas tika atlasīts maksājuma uzsākšanas laikā, maksājums tik un tā tiks apstrādāts. Taču tas tiks grāmatots kontiem, kas ir kartēti uz karšu zīmolu, kuru atlasījāt 10. darbībā.

12. Vēlreiz atlasiet **Labi**, lai aizvērtu dialoglodziņu **Pasūtījuma pabeigšanas maksājumi**.
13. Lapā **Pārdošanas pasūtījuma kopsavilkums** atlasiet **Iesniegt**.
14. Pārdošanas punkta (POS) sveiciena lapā atlasiet operāciju **Saņemamie pasūtījumi**, lai redzētu pasūtījumus, kurus ir paredzēts saņemt veikalā. 
15. Atlasiet vienu vai vairākas rindas no pasūtījuma, kurš tika izveidots atsauces vitrīnā, un pēc tam atlasiet **Saņemt**.

    Pasūtījums tiek izgūts no iekšējās uzskaites daļas. 

16. Kad pasūtījuma rindas informācija ir izgūta no iekšējās uzskaites daļas un tiek konstatēts kartes maksājums, ko var izmantot visiem kanāliem, jūs tiekat informēts, ka ir pieejama maksāšanas metode.
17. Atlasiet **Izmantot pieejamu maksāšanas metodi**, lai pabeigtu transakciju, izmantojot atsauces vitrīnā ievadīto kartes informāciju.

    Pasūtījuma rindas tiek ielādētas transakcijas lapā, un apmaksājamā bilance ir 0 (nulle).

18. Atlasiet cilni **Maksājumi**, lai skatītu norēķinu rindu, kas tika izgūta no tiešsaistes pasūtījuma. 
19. Atlasiet jebkuru maksāšanas metodi, lai pabeigtu šo transakciju. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Pirkt veikalā A, saņemt veikalā B

1. Palaidiet pārdošanas punktu (POS) Hjūstonas veikalam.
2. Lapā **Transakcija** pievienojiet transakcijai Zani Siliņu, ar ciparu tastatūru ievadot **2001**.
3. Pievienot transakcijai vienu vai vairākas rindas.
4. Atlasiet **Pasūtījumi**, lai skatītu pasūtījuma opcijas.
5. Atlasiet **Saņemt visu** un pēc tam, kad tiek parādīta uzvedne, atlasiet **Klienta pasūtījums**.
6. Meklēšanas joslā ievadiet **Sietla** un pēc tam saņemšanai atlasiet veikalu **Sietla**. 
7. Atlasiet **Labi**, lai kā saņemšanas datumu apstiprinātu pašreizējo datumu.
9. Atlasiet **Maksājums ar karti**, lai uzsāktu maksājumu.
10. Norēķinieties ar kartes maksājumu par depozītam paredzēto summu. 
11. Pabeidziet šo depozīta maksājumu maksājumu terminālī. 
12. Kad depozīts ir apmaksāts, atlasiet šo opciju, lai to pašu karti izmantotu izpildīšanai, un gaidiet pasūtījuma pabeigšanu. 
13. Palaidiet pārdošanas punktu (POS) Sietlas veikalam.
14. Pārdošanas punkta (POS) sveiciena lapā atlasiet operāciju **Saņemamie pasūtījumi**, lai redzētu pasūtījumus, kurus ir paredzēts saņemt veikalā. 
15. Atlasiet vienu vai vairākas rindas no pasūtījuma, kurš tika izveidots atsauces vitrīnā, un pēc tam atlasiet **Saņemt**.

    Pasūtījums tiek izgūts no iekšējās uzskaites daļas. 

16. Kad pasūtījuma rindas informācija ir izgūta no iekšējās uzskaites daļas un tiek konstatēts kartes maksājums, ko var izmantot visiem kanāliem, jūs tiekat informēts, ka ir pieejama maksāšanas metode.
17. Atlasiet **Izmantot pieejamu maksāšanas metodi**, lai pabeigtu transakciju, izmantojot atsauces vitrīnā ievadīto kartes informāciju.

    Pasūtījuma rindas tiek ielādētas transakcijas lapā, un apmaksājamā bilance ir 0 (nulle).

18. Atlasiet cilni **Maksājumi**, lai skatītu norēķinu rindu, kas tika izgūta no tiešsaistes pasūtījuma. 
19. Atlasiet jebkuru maksāšanas metodi, lai pabeigtu šo transakciju. 

### <a name="buy-in-store-a-ship-to-customer"></a>Pirkt veikalā A, nosūtīt klientam

1. Palaidiet pārdošanas punktu (POS) Hjūstonas veikalam.
2. Lapā **Transakcija** pievienojiet transakcijai Zani Siliņu, ar ciparu tastatūru ievadot **2001**.
3. Pievienot transakcijai vienu vai vairākas rindas.
4. Atlasiet **Pasūtījumi**, lai skatītu pasūtījuma opcijas.
5. Atlasiet **Nosūtīt visu** un pēc tam, kad tiek parādīta uzvedne, atlasiet **Klienta pasūtījums**.
6. Lapā nosūtīšanas metode atlasiet **Standarta piegāde pa nakti** un pēc tam atlasiet **Labi**, lai pieņemtu šodienas datumu kā nosūtīšanas datumu. 
7. Atlasiet **Labi**, lai kā saņemšanas datumu apstiprinātu pašreizējo datumu.
8. Atlasiet **Maksājums ar karti**, lai uzsāktu maksājumu.
9. Norēķinieties ar kartes maksājumu par depozītam paredzēto summu. 
10. Pabeidziet šo depozīta maksājumu maksājumu terminālī. 
11. Kad depozīts ir apmaksāts, atlasiet šo opciju, lai to pašu karti izmantotu izpildīšanai, un gaidiet pasūtījuma pabeigšanu.

Kad pasūtījums ir saņemts, iepakots un par to ir izrakstīts rēķins iekšējā uzskaites daļā, pārdošanas punktā (POS) norādītā maksājuma informācija tiek izmantota, lai iegūtu līdzekļus par klientam nosūtītajām precēm. 

## <a name="scenario-details"></a>Detalizēta informācija par scenāriju

Papildus tikko aprakstītajiem pamata scenārijiem maksājumu SDK ir veikti vairāki uzlabojumi, lai atbalstītu visu kanālu maksājumus. 

### <a name="pos"></a>POS

#### <a name="single-swipedip-for-customer-orders"></a>Viena kartes novilkšana/ievietošana klientu pasūtījumiem

Pirms visu kanālu maksāšanas līdzekļa ieviešanas, kad pārdošanas punktā (POS) tika izveidoti klientu pasūtījumi, kuros bija depozīti, klientiem bija nepieciešams novilkt (vai ievietot) savas kartes divreiz: vienu reizi, lai samaksātu depozītu, un vēl vienu reizi, lai kartei piešķirtu marķieri turpmākai pasūtījumu izpildīšanai. Kad ir ieslēgts visu kanālu marķieru piešķiršanas līdzeklis, klientiem savas kartes ir jānovelk tikai vienreiz, lai gan samaksātu depozītu, gan autorizētu par precēm maksājamo summu, kura tiks izpildīta vēlāk. Izpildes laikā tiek iegūti autorizētie līdzekļi. Pirms visu kanālu marķieru piešķiršanas līdzekļa ieviešanas turpmākai pasūtījumu izpildīšanai tika izveidots tikai periodisks kartes marķieris. Tādēļ līdzekļi gaidošajai izpildīšanai netika autorizēti un — tā kā šie līdzekļi netika aizturēti šim konkrētajam pirkumam — pastāvēja mazāka iespējamība, ka tos varētu iegūt vēlāk.

> [!NOTE]
> Viena kartes novilkšana netiek atbalstīta Retail versijā 8.1.3. Klientu pasūtījumi versijā 8.1.3 izmanto tādu pašu plūsmu, kāda tika izmantota pirms visu kanālu marķieru piešķiršanas līdzekļa ieviešanas. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Kartes, kas nevar izsniegt periodiskus karšu marķierus

Dažas kartes nevar izmantot visu kanālu maksājumiem, jo tās neatbalsta periodisku karšu marķieru izsniegšanu. Kad pārdošanas punktā (POS) tiek izveidots kāds pasūtījums, kurā depozīts ir samaksāts, izmantojot karti, kas neatbalsta periodiskus karšu marķierus, tiek izmantota iepriekšējā karšu marķieru piešķiršanas plūsma. Tādēļ klientam, kurš vēlas veikt maksājumu, kas tiks izmantots turpmākai pasūtījuma izpildīšanai, ir jānorāda otra karte. Ja otrā karte neatbalsta periodiskos karšu marķierus, marķieru piešķiršanas darbība tiek noraidīta un kasieris tiek aicināts lūgt klientam uzrādīt citu karti. 

### <a name="using-a-different-card"></a>Citas kartes lietošana

Klientam, kurš ierodas veikalā pasūtījuma saņemšanai, ir iespēja izmantot citu karti. Kad pasūtījuma saņemšanas laikā kasierim tiek parādīta uzvedne **Izmantot pieejamu maksāšanas metodi**, kasieris var pavaicāt, vai klients vēlas izmantot to pašu karti. Ja klients ir pazaudējis karti, kura tika izmantota pasūtījuma izveidošanai, un vēlas maksāt par pasūtījumu, izmantojot citu karti, kasieris var atlasīt **Izmantot citu maksāšanas metodi**. Ja klients vēlāk atgriežas, lai saņemtu citus vienumus tam pašam pasūtījumam, un ja sākotnējā kartes autorizācija joprojām ir derīga, kasieris atkal var vaicāt, vai klients vēlas izmantot šo karti.

### <a name="invalid-authorizations"></a>Nederīgas autorizācijas

Ja pasūtījuma izveidošanai izmantotā karte vairs nav derīga, kad preces tiek atlasītas saņemšanai, maksājuma iegūšanas pieprasījums ir nesekmīgs. Tādā gadījumā POS maksājumu savienotājs mēģina izveidot jaunu autorizāciju un iegūšanu, izmantojot to pašu kartes informāciju. Ja jaunā autorizācija vai iegūšana ir nesekmīga, kasieris tiek informēts, ka maksājumu nevarēja apstrādāt. Tādā gadījumā kasierim no klienta ir jāiegūst jauns maksājums. 

### <a name="multiple-available-payments"></a>Vairāki pieejamie maksājumi

Kad tiek saņemts pasūtījums ar vairākiem norēķiniem un vairākām rindām, kasierim vispirms tiek parādīta uzvedne **Izmantot pieejamu maksāšanas metodi**. Ja pastāv vairākas kartes, kad kasieris atlasa **Izmantot pieejamu maksāšanas metodi**, tiek iegūtas esošās karšu norēķinu rindas, līdz bilance par pašlaik saņemtajām precēm ir izpildīta. Kasierim nav iespējas atlasīt karti, kas ir jāizmanto precēm, kuras tiek saņemtas. 

## <a name="related-topics"></a>Saistītās tēmas

- [Bieži uzdotie jautājumi par maksājumiem](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi](https://docs.microsoft.com/dynamics365/commerce/cpe-bopis)



[!INCLUDE[footer-include](../includes/footer-banner.md)]