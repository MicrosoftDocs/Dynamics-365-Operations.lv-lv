---
title: "Noklusējuma pasūtījuma iestatījumi dimensijām un preču variantiem"
description: "Pasūtījuma noklusējuma iestatījumi definē vietu un noliktavu, kur krājumi tiks iegūti vai glabāti, minimālos, maksimālos, vairākkārtējos un standarta daudzumus, kas tiks izmantoti tirdzniecībai vai krājumu pārvaldībai, izpildes laikus, apturēšanas karodziņus un pasūtījumu solīšanas metodes. Pasūtījuma noklusējuma iestatījumi tiek izmantoti, veidojot pirkšanas pasūtījumus, pārdošanas pasūtījumus, pārsūtīšanas pasūtījumus, krājumu žurnālus un veicot vispārējo plānošanu plānoto pasūtījumu ģenerēšanai. Pasūtījuma noklusējuma iestatījumi var būt atkarīgi no preces, atkarīgi no vietas, atkarīgi no preces varianta vai atkarīgi no preces dimensijas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 26ad7fb0e9371b8e1d45d61f2348241c6aca16b9
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Noklusējuma pasūtījuma iestatījumi dimensijām un preču variantiem

[!include[banner](../includes/banner.md)]


Pasūtījuma noklusējuma iestatījumi definē vietu un noliktavu, kur krājumi tiks iegūti vai glabāti, minimālos, maksimālos, vairākkārtējos un standarta daudzumus, kas tiks izmantoti tirdzniecībai vai krājumu pārvaldībai, izpildes laikus, apturēšanas karodziņus un pasūtījumu solīšanas metodes. Pasūtījuma noklusējuma iestatījumi tiek izmantoti, veidojot pirkšanas pasūtījumus, pārdošanas pasūtījumus, pārsūtīšanas pasūtījumus, krājumu žurnālus un veicot vispārējo plānošanu plānoto pasūtījumu ģenerēšanai. Pasūtījuma noklusējuma iestatījumi var būt atkarīgi no preces, atkarīgi no vietas, atkarīgi no preces varianta vai atkarīgi no preces dimensijas.

Pasūtījuma noklusējuma iestatījumus varat definēt lapā **Pasūtījuma noklusējuma iestatījumi**. Lai atvērtu šo lapu, dodieties uz **Preču informācijas pārvaldība** &gt; **Preces** &gt; **Izlaistās preces** &gt; atlasiet kādu izlaisto preci &gt; darbību rūtī **Plāns** vai ****Pārvaldīt krājumus**** &gt; **Pasūtījuma iestatījumi** &gt; **Pasūtījuma noklusējuma iestatījumi**.

## <a name="default-order-settings"></a>Pasūtījuma noklusējuma iestatījumi
Pastāv trīs veidu pasūtījuma noklusējuma iestatījumi pirkšanai, pārdošanai un krājumiem. Pasūtījuma noklusējuma iestatījumi pirkšanai tiek izmantoti, kad izveidojat tālāk uzskaitītos elementus.

-   Pirkšanas pasūtījuma rindas
-   Pirkšanas līguma rindas
-   Piedāvājuma pieprasījuma rindas
-   Pirkšanas pieprasījumu rindas
-   Sūtījuma papildināšanas rindas
-   Plānotie pirkšanas pasūtījumi

Pasūtījuma noklusējuma iestatījumi pārdošanai tiek izmantoti, kad izveidojat tālāk uzskaitītos elementus.

-   Pārdošanas pasūtījuma rindas
-   Pārdošanas līguma rindas
-   Pārdošanas piedāvājuma rindas
-   Atgriešanas pasūtījuma rindas un krājumu aizstāšanas rindas
-   Pieprasījuma apjoma prognozes rindas

Pārdošanas pasūtījuma noklusējuma iestatījumi tiek izmantoti arī tad, kad izveidojat tālāk uzskaitītos elementus.

-   Projekta krājumu prasības
-   Pakalpojumu pasūtījumu krājumu vajadzības

Pasūtījuma noklusējuma iestatījumi krājumiem tiek izmantoti, kad izveidojat tālāk uzskaitītos elementus.

-   Krājumu žurnāli
-   Pārsūtīšanas pasūtījumi
-   Plānotie pārsūtīšanas pasūtījumi

Krājumu pasūtījuma noklusējuma iestatījumi tiek izmantoti arī tad, kad izveidojat tālāk uzskaitītos elementus.

-   Karantīnas pasūtījumi
-   Kvalitātes pasūtījumi
-   Ražošanas pasūtījumi
-   MK rindas
-   Plānotie ražošanas pasūtījumi

## <a name="full-definition-of-a-released-product"></a>Pilna izlaistās preces definīcija
Kad veidojat kādu transakciju, rindā ir jānorāda pilnā izlaistās preces definīcija, pirms Dynamics 365 for Operations mēģina identificēt pasūtījuma noklusējuma iestatījumus. Pilna izlaistās preces definīcija nozīmē, ka transakcijā ir norādīts krājuma kods un visas aktīvās preces dimensijas, piemēram, konfigurācija, izmērs, stils un krāsa. Piemēram, ja manuāli veidojat pirkšanas pasūtījuma rindu izlaistam preces variantam, ir jānorāda visas nepieciešamās preces dimensijas, pirms pasūtījuma rindā tiek parādīta noklusējuma vieta, noliktava, daudzumi un izpildes laiks. 

Ne visi pasūtījuma noklusējuma iestatījumu parametri tiek lietoti, kad veidojat pasūtījumu vai žurnāla rindas. Daudzumi un izpildes laiki pēc noklusējuma tiek rādīti tikai tad, ja piemērojams. Piemēram, veicot aprēķinus žurnāla rindā, izveidojot rindu, pēc noklusējuma tiek rādīta tikai vieta un noliktava. Skaidrs, ka netiek veikta nekāda daudzuma noklusējuma iestatīšana vai pārbaudes par vairākkārtējiem un minimālajiem daudzumiem, kad veidojot rindu vai grāmatojat žurnālu. 

Veidojot pasūtījumu vai žurnāla rindu, sistēma vienmēr mēģina atrast noklusējuma vietu un noliktavu. Ne vienmēr vieta pēc noklusējuma tiek rādīta no pasūtījuma iestatījumiem. Piemēram, kad veidojat pārdošanas pasūtījumu vai pirkšanas pasūtījumu, pasūtījuma rindās automātiski tiek lietota vieta no pasūtījuma virsraksta. Veidojot MK rindu, tiek lietota vieta no MK virsraksta. Kad vieta ir noteikta, tā tiek izmantota, lai atrastu visus no vietas atkarīgos pasūtījuma iestatījumus, kurus pēc tam var izmantot kā noliktavas noklusējumu. 

Pasūtījuma noklusējuma tipu, pirkšanu un krājumu izpildes laikus var pārlabot ar krājumu seguma kārtulām lapā **Krājumu segums**. Lai gan pasūtījuma noklusējuma iestatījumi neļauj nodalīt ražošanas un pārsūtīšanas izpildes laiku, krājumu seguma kārtulas to atļauj. Taču krājuma seguma iestatījumus MRP izmantos tikai, lai veidotu plānotu ražošanu un plānotus pārsūtīšanas pasūtījumus, un šie iestatījumi netiks lietoti, kad ražošanas un pārsūtīšanas pasūtījumus veidojat manuāli. 

## <a name="default-order-settings-rules"></a>Pasūtījuma noklusējuma iestatījumu kārtulas
Varat definēt vispārējus pasūtījuma noklusējuma iestatījumus un neierobežotu skaitu pasūtījuma noklusējuma iestatījumu kārtulu, kuras attiecas tikai uz konkrētiem nosacījumiem, piemēram, uz kādu vietu vai konkrētu preces dimensiju, vai preces dimensiju kombināciju. Nevar definēt no noliktavas atkarīgus pasūtījumu iestatījumus.

### <a name="rank-in-default-order-settings"></a>Pasūtījuma noklusējuma iestatījumu rangs

Pasūtījuma noklusējuma iestatījumu kārtulām ir rangi. Jo augstāks rangs, jo svarīgāka kārtula — tas nozīmē, ka tai būs augstāka prioritāte un tā tiks izmantota pirms kārtulām ar zemāku rangu. Vispārējiem pasūtījuma noklusējuma iestatījumiem rangs ir nulle, un to nevar modificēt. Tikai vienai kārtulai rangs var būt nulle. Kārtulām var būt vienāds rangs, bet ar nosacījumu, ka tās attiecas uz dažādām dimensijām. Tas ir noderīgi no vietas atkarīgu pasūtījuma iestatījumu modelēšanai. Kad tiek izveidota jauna pasūtījuma noklusējuma iestatījumu kārtula, tad pasūtījuma vērtību vērtības, apturēšanas karodziņi un citi vienumi tiek pārmantoti no kārtulas ar nulles rangu, bet šīs vērtības var pārrakstīt.

### <a name="default-order-settings-for-released-products"></a>Pasūtījuma noklusējuma iestatījumi izlaistām precēm

Atšķirīgām izlaistajām precēm varat definēt vispārējos pasūtījuma iestatījumus vai no vietas atkarīgus pasūtījuma iestatījumus. Vispārīgajiem pasūtījuma iestatījumiem rangs vienmēr ir nulle. Ja vienlaicīgi kopā iestatāt jaunus pārdošanas, pirkšanas un krājumu pasūtījuma iestatījumus, ieteicams lietot skatu **Detalizētas informācijas skats** lapā **Pasūtījuma noklusējuma iestatījumi**. Lai pārslēgtu uz detalizētas informācijas skatu, dodieties uz darbību rūti **Opcijas** &gt; **Lapas opcijas** &gt; **Mainīt skatu** &gt; **Detalizētas informācijas skats**.

### <a name="site-specific-order-settings"></a>Atrašanās vietai raksturīgie pasūtījuma iestatījumi

Lai izveidotu no vietas atkarīgus pasūtījuma iestatījumus, noklikšķiniet uz **Jauns**. Skatā **Detalizētas informācijas skats** aizpildiet vietu laukā **Iestatījumi, kas piemērojami šeit:** &gt; **Vieta**. Skatā **Režģa skats** aizpildiet vietas vērtību kolonnā **Vieta**. Jaunā kārtula automātiski iegūs jaunu ranga vērtību, kas ir lielāka par nulli. Varat izveidot neierobežotu skaitu no vietas atkarīgo kārtulu, un visām no vietas atkarīgajām kārtulām varat piešķirt vienādu rangu, lai norādītu, ka tās ir vienlīdz svarīgas. 

Ja esat atvēris skatu **Detalizētas informācijas skats**, nevar iegūt pārskatu par krājumam izveidotajām kārtulām. Pārslēdziet pogu **Rādīt/slēpt sarakstu**, lai redzētu pārskata informāciju. Kad tiek izveidota jebkāda tipa pasūtījuma rinda un tai nav norādīta neviena vieta, tad Dynamics 365 for Operations meklē kārtulu, kurai nav norādīta neviena vieta. Tas var palīdzēt pasūtījuma rindai noteikt noklusējuma vietu. Pēc tam šī vieta tiek izmantota no vietas atkarīgas kārtulas meklēšanai, kur var būt iestatīta noklusējuma noliktava. Šī noliktava tiek lietota pasūtījuma rindā.

### <a name="specific-order-settings-for-product-dimension"></a>Īpaši pasūtījuma iestatījumi preces dimensijai

Pasūtījuma iestatījumu kārtulas varat definēt jebkurai aktīvai preces dimensijai vai aktīvu preces dimensiju kombinācijai. Ja preces dimensijas lauks tiek atstāts tukšs, tad šī kārtula attiecas uz visām preces dimensijas vērtībām. 

Aplūkosim nākamo preces piemēru.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Preces nosaukums**                                    | Fotoelektriskais sensors                    |
| **Krājuma kods**                                     | XW56                                    |
| **Konfigurācija** (izmantota gaismas tipa modelēšanai) | C1-redzamā sarkanā gaisma, C2-infrasarkanā gaisma |
| **Stils** (izmantots tehniskā izdevuma modelēšanai)  | R1, R2, R3                              |

Šajā piemērā tiek pieņemts, ka prece tiek sagādāta, nevis ražota. Tiek arī pieņemts, ka konfigurācija C1 tiek lietota biežāk, tāpēc tai ir īsāki izpildes laiki. 

Lai modelētu šo scenāriju, izveidojiet tālāk norādītos pasūtījuma noklusējuma iestatījumus.

| Rangs | Atrašanās vieta | Konfigurācija | Stils | Iegādāšanās — ignorēt noklusējuma iestatījumus | Pirkšanas izpildes laiks | Iegādāšanās — apturēta | Pārdošana — ignorēt noklusējuma iestatījumus | Pārdošana — apturēta |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10.   |      | C1            |       | Jā                                  | 2.                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5.                  |                    |                                   |                 |

Kad precei XW56, konfigurācijai C1 tiek izveidota pirkšanas pasūtījuma rinda vai plānotais pirkšanas pasūtījums, tad neatkarīgi no izdevuma vai vietas, kur šī rinda atrodas, izpildes laiks tiek uzskatīts par 2. Pieņemam, ka ir apturēti visi izdevumi, izņemot R3.

Varat izveidot tālāk norādītās pasūtījuma noklusējuma iestatījumu kārtulas.

| Rangs | Atrašanās vieta | Konfigurācija | Stils | Iegādāšanās — ignorēt noklusējuma iestatījumus | Pirkšanas izpildes laiks | Iegādāšanās — apturēta | Pārdošana — ignorēt noklusējuma iestatījumus | Pārdošana — apturēta |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20.   |      |               | R2    | Jā                                  |                    | Jā                | Jā                               | Jā             |
| 20.   |      |               | R1    | Jā                                  |                    | Jā                | Jā                               | Jā             |
| 10.   |      | C1            |       | Jā                                  | 2.                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5.                  |                    |                                   |                 |

Abām veco izdevumu apturēšanas kārtulām ir vienāds rangs, tas nozīmē, ka tās ir vienlīdz svarīgas. Abām šīm kārtulām ir augstāks rangs nekā kārtulai, kas attiecas uz konfigurāciju C1 — tas nozīmē, ka tām ir virsroka pār konfigurācijas C1 kārtulu. 

Šajā piemērā ir paskaidrota ranga nepieciešamība. Ja pirkšanas pasūtījums tiek izveidots konfigurācijai C1 un izdevumam R2, tad gadījumā, ja ranga nav, abas R2 un C1 definētās kārtulas būtu neskaidras. Lai novērstu šo neskaidrību, Dynamics 365 for Operations kārtulas meklēs dilstošā secībā pēc ranga, un lietos pirmo piemērojamo kārtulu. Pašreizējā piemērā, kad pirkšanas pasūtījuma rinda tiek izveidota konfigurācijai C1 un izdevumam R2, lietotājs saņem brīdinājuma ziņojumu, ka krājums ir aizturēts un ka to ir izraisījusi izdevuma vērtība. Ja konfigurācijas kārtulas rangs būtu augstāks par izdevuma kārtulas rangu, tad šī pirkšanas pasūtījuma rindas izveidošana konfigurācijai C1 un izdevumam R2 būtu izpildīta sekmīgi, un lietotājam netiktu rādīts ziņojums “krājums ir aizturēts”. 

Apsveriet tālāk norādītās pasūtījuma noklusējuma iestatījumu kārtulas.

| Rangs | Atrašanās vieta | Konfigurācija | Stils | Noklusējuma atrašanās vieta | Noklusējuma noliktava | Pirkšana — ignorēt noklusējuma noliktavas dimensijas | Pirkšanas noliktava |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20.   | 2.    |               |       |              |                   | Jā                                            | 22                 |
| 10.   |      | C1            |  R2   |  2.           |  21               |                                                |                    |
| 0    |      |               |       | 1.            | 11.                |                                                |                    |

Lai noteiktu vietu un noliktavu, sistēma divreiz šķērso kārtulu kopu. Kad pirkšanas pasūtījuma rinda tiek izveidota konfigurācijai C1, stilam R2, tad vieta tiek noteikta, balstoties uz kārtulu ar rangu 10. Pēc tam sistēma meklē kārtulu vietai 2, lai noteiktu noliktavu. Kārtula 20 tiek atrasta, un — tā kā tās rangs ir augstāks — noliktava pirkšanas pasūtījuma rindā būs 22, nevis 21. 

Parasti konkrētas kārtulas un dimensiju kārtulas, kuras ir svarīgākas par citām dimensijām, saņem augstāku rangu, bet vispārīgākām kārtulām tiek piešķirti zemāki rangi. 

Kārtula ar nulles rangu kalpo par drošības tīklu. Ja nav piemērota neviena cita kārtula, tad tiks izmantoti pasūtījuma noklusējuma iestatījumi no nulles kārtulas. 

Tā kā ranga skaitlis ir tik svarīgs, darbību rūtī **Pasūtījuma noklusējuma iestatījumi** pastāv funkcijas kārtulu pārbīdīšanai uz augšu vai uz leju un kārtulu pārnumurēšanai, lai tās vienmēr būtu uzskaitītas ar soļiem pa 10. 

Izlaistajām precēm var būt daudz izveidoto kārtulu. Lai gūtu labāku priekšstatu par to, ko katra kārtula pārraksta un kāpēc tā ir nepieciešama, iesakām lietot skatu **Režģa skats** lapā **Pasūtījuma noklusējuma iestatījumi**. Režģa skatu varat iespējot, dodoties uz darbību rūti **Opcijas** &gt; **Lapas opcijas** &gt; **Mainīt skatu** &gt; **Režģa skats**. Režģī rādīto kolonnu skaits varētu būt diezgan būtisks, it īpaši attiecībā uz pārdošanas un krājumu cilnēm. Lai ierobežotu režģī rādīto kolonnu skaitu, kolonnu grupas ir iespējams slēpt vai rādīt, izmantojot pogas izvēlnē **Pasūtījuma noklusējuma iestatījumi** &gt; **Kolonnas attēlojums**.

### <a name="specific-order-settings-for-released-product-variant"></a>Īpaši pasūtījuma iestatījumi izlaistās preces variantam

Ja kārtulu sistēma pasūtījuma noklusējuma iestatījumiem ir pārāk apgrūtinoša, pastāv iespēja vienkārši definēt noklusējuma pasūtījuma uzstādījumus katram preces variantam. Nākamajos piemēros ir parādīts, kā tas izskatītos precei un iepriekš aprakstītajos gadījumos.

| Rangs | Atrašanās vieta | Konfigurācija | Stils | Iegādāšanās — ignorēt noklusējuma iestatījumus | Pirkšanas izpildes laiks | Iegādāšanās — apturēta | Pārdošana — ignorēt noklusējuma iestatījumus | Pārdošana — apturēta |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10.   |      | C2            | R3    | Jā                                  | 5.                  |                    |                                   |                 |
| 10.   |      | C2            | R2    | Jā                                  | 5.                  | Jā                | Jā                               | Jā             |
| 10.   |      | C2            | R1    | Jā                                  | 5.                  | Jā                | Jā                               | Jā             |
| 10.   |      | C1            | R3    | Jā                                  | 2.                  |                    |                                   |                 |
| 10.   |      | C1            | R2    | Jā                                  | 2.                  | Jā                | Jā                               | Jā             |
| 10.   |      | C1            | R1    | Jā                                  | 2.                  | Jā                | Jā                               | Jā             |
| 0    |      |               |       |                                      | 5.                  |                    |                                   |                 |

Šajā gadījumā rangs nav īsti svarīgs, tāpēc varat izvēlēties to slēpt. Šis risinājums potenciāli izraisa uzturēšanas problēmu. Taču varat apsvērt iespēju izmantot šo iestatījumu, ja plānojat integrēšanu ar Preces dzīves cikla pārvaldības (Product Lifecycle Management — PLM) sistēmām.




