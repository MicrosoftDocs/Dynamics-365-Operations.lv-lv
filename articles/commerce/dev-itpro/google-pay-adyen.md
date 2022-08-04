---
title: Konfigurēt džimu apmaksu ar Adžienu
description: Šajā rakstā ir aprakstīts, kā konfigurēt Patēršu apmaksu ar Ahaenu Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115015"
---
# <a name="configure-google-pay-with-adyen"></a>Konfigurēt džimu apmaksu ar Adžienu

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt Patēršu apmaksu ar Ahaenu Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce programma <a0/&piedāvā neapmaksāti integrāciju piedāvājumu piedāvājumu apmaksai, ja tiek lietots Amaksājot maksājumu vārtejas pakalpojums. Maks. ir digitāla apmaksas metode, kas izmanto Pārlūka maksājuma tirgotāja kontu un Amacen maksājumu pakalpojumu. Ja tā ir konfigurēta, poga Manuālie maksājumi ir pieejama kā atlasāma maksāšanas metode tiešsaistes pasūtījuma paņemšanu. Kad lietotāji izvēlas **Atlas Saņemšanas apmaksu** atbalstītā pārlūkprogrammā vai ierīcē, viņi tiek novirzīti uz to, lai pabeigtu maksājumu tieši ar Līgumu Pay Service. Pēc tam viņi tiek atgriezti tiešsaistes storefront, lai pabeigtu pasūtījumu.

Kad Konta apmaksa tiek izmantota ar express checkout moduli Commerce, lietotāja maksājumu konta informācija automātiski tiek ievadīta norēķināšanas formā, lai palīdzētu lietotājam ātrāk iziet pa norēķinājuma procesu. Commerce ietver maksājuma ekspresmoduli, kas iespējo ekspresmaksājuma darbību. Maksājuma ekspresmoduli var izmantot fragmentā, kas ir iekļauts norēķinu vai groza lapā. Dynamics 365 maksājumu savienotājs atsaucei Uz apmaksas savienotāju tiek izmantots papildus Dynamics 365 maksājumu savienotājam, kas paredzēts Apārtraucen, lai, konfigurējot PayPal, iespējotu gan maksājuma steidzamas, gan regulāras norēķināšanas opcijas. Pirkšanas apmaksu var konfigurēt arī ar Ahaen maksājumu termināļiem un pārdošanas punktā Commerce Point (POS), kas tiek lietots veikalā.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | Apraksts |
|---|---|
| Darba apmaksa | To sauc arī par pogu Saņemšanas maksājums, Armēdijas maksājums ir neapmaksāts maksājuma piedāvājums, kas tiek atbalstīts, izmantojot Aradien savienotāju. Tas iespējo klienta pieredzi un integrāciju, ko atbalsta Dynamics Debitora maksājuma savienotājs. |
| Maka | Maksājuma veids, kas neietver tradicionālas maksājuma raksturīgās iezīmes, piemēram, bankas identifikācijas numura (BIN) diapazonu un beigu datumu, ko izmanto, lai atšķirtu kredītkaršu un debetkaršu veidus. |
| Maksājuma ekspresmodulis | Modulis Dynamics 365 Commerce, kas atbalsta ātrākas paņemšanas darbību ar atbalstītām maksāšanas metodēm. |

## <a name="prerequisites"></a>Priekšnosacījumi

Uzņēmuma Kases apmaksas ar Adžienu izmantošanai ir nepieciešams Tirdzniecības tirgotāja konts. Papildinformāciju par to, kā iestatīt savu tirgotāja kontu, [skatiet Aības rēķina dokumentāciju par Siamu](https://docs.adyen.com/payment-methods/google-pay/) un Parietas integrācijas [kontrolsarakstu](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist).

Konta apmaksas metodei jābūt integrētai arī ar jūsu Alvērna kontu. Integrācijas saišu instrukcijas skatiet [Adžiens Toms(I) Apmaksā](https://www.adyen.com/payment-methods/google-pay).

Ir jāiespējo arī uzlabotā funkcionalitāte galvenajā birojā Dynamics 365 Commerce. Pārejiet uz **darbvietu \> līdzekļu pārvaldību**, meklējiet **līdzekli Uzlabots Avansa** atbalsts un maksājumu uzlabojumi, atlasiet šo līdzekli un pēc tam atlasiet **Iespējot**. Pēc funkcijas iespējošanas palaidiet **1110 sadales** grafiku, lai padarītu izmaiņas pieejamas visos kanālos.

## <a name="map-the-google-pay-payment-method"></a>Kartēt Saņemšanas/ maksājuma metodi

Maks. ir digitāla apmaksas metode. Papildinformāciju par to, kā iestatīt maksājumu kartēšanu šim: '% Maksājuma apmaksa' skatiet smaksas [maksājumu atbalsta sadaļā](../wallets.md).

Lai uz kartes norēķinu veidiem kartētu gan POS, gan tiešsaistes kanālos, sekojiet šiem soļiem.

1. Programmā Commerce headquarters dodieties uz sadaļu **Mazumtirdzniecības un Commerce \> Channel setup \> maksājumu metodes Kartes \> veidi**.
1. Atlasiet **Jauns**, lai pievienotu rindu Pasūtījuma apmaksai.
1. **ID laukā** ievadiet **SiamPay**.
1. Laukā **Elektroniskā maksājuma nosaukums** ievadiet **Saņemšanas apmaksu**.
1. Laukā **Tips** ievadiet **Sia**.
1. Laukā **Izsniedzēja** ievadiet **Sia**.
1. Darbību rūtī atlasiet Procesora kartēšana **, lai** atvērtu dialoglodziņu **Procesora maksājuma kartēšanas** metodes.
1. Nekartēto **procesoru maksājumu** metodēs ir redzams nekartēto procesoru maksājumu metožu saraksts, un katra no tām ir savienota pārī ar atbilstošo savienotāju. Lai kartētu nekartētos Algu procesora maksājuma metodes norēķinu veidiem ar karti, izpildiet tālāk aprakstītās darbības katram norēķinu veidam ar karti:

    1. Sadaļā Norēķinu **veidi ar karti** atlasiet norēķinu veidu ar karti.
    1. **Kolonnā Nekartītās** **procesora maksājuma metodes atlasiet gan Dynamics 365 maksājumu savienotāju A stabiņu** savienotājam (izmantošanai POS), **gan Dynamics 365 maksājumu savienotāju connectoru Maksājuma** apmaksai (izmantošanai tiešsaistes kanālos).
    1. Atlasiet **Pievienot**. Atlases tiek pievienotas kolonnā Kartētās **procesora maksājuma** metodes.

1. Kad maksāšanas metodes ir pabeigtas, atlasiet **Saglabāt**.
1. Lapā Karšu **veidi** atlasiet **Saglabāt**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Commerce interneta veikala konfigurēšana Konta maksājumam

Lai konfigurētu Commerce interneta veikalu, lai lietotu Algu, sekojiet šiem soļiem.

1. Programmā Commerce headquarters dodieties uz mazumtirdzniecības **un commerce \> kanālu tiešsaistes \> veikaliem**.
1. Atlasiet savas vietnes tiešsaistes veikala kanālu, atlasot kanāla Mazumtirdzniecības **kanāla ID** vērtību.
1. Kopsavilkuma cilnē **Maksājumu konti** zem savienotāja **apstipriniet**, ka **ir uzskaitīts Dynamics 365 maksājumu savienotājs A nosūtīšanai**. Ja tā nav uzskaitīta, izpildiet [dynamics 365 Payment Connector for Aradien norādījumus,](adyen-connector-setup.md) lai to pievienotu.

    > [!NOTE]
    > Vairākumā gadījumu **Dynamics 365 maksājumu savienotājs A papildmaksu** savienotājam jānorāda kā pirmais savienotājs jūsu kanālam (pirmais savienotājs tiek saukts arī par primāro savienotāju). Pēc tam ir jāseko citiem savienotājiem, kas tiks lietoti, piemēram, **Dynamics 365 Payment Connector for PayPal** un **Dynamics 365 Payment Connector for Connectors.**

1. **Pēc Tam, kad Dynamics 365 maksājumu savienotājs Amaksājot savienotājam** ir pievienots, atlasiet Pievienot, **·** **lai pievienotu Dynamics 365 maksājumu savienotāju Šim: Connector Connector.** Pēc tam iestatiet savienotājam šādus rekvizītus.

    | Lauks                  | Apraksts | Obligāti | Automātiski iestatīts | Parauga vērtība |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Komplektācijas nosaukums          | Dynamics 365 maksājumu savienotāja, kas paredzēts Connector for Connector For Connector, komplektācijas nosaukums. | Jā | Jā | *Binārais nosaukums* |
    | Pakalpojuma konta ID     | Tirgotāja rekvizītu iestatīšanas unikālais identifikators. Šis identifikators ir uzspiests maksājumu darbībās un identificē tirgotāja rekvizītus, ko vajadzētu izmantot lejupstraumes procesiem (piemēram, rēķinu izrakstīšanai). | Jā | Jā | *GUID* |
    | Tirgotāja ID     | Ievadiet Jūsu Tirgotāja kontam piešķirto Tirgotāja ID. Šis rekvizīts ir nepieciešams ražošanas vidēm, bet tas nav obligāts pārbaudes vidēm. Lai iegūtu papildu informāciju, apmeklējiet <https://pay.google.com/>. | Jā | Nē | *Skaitlisks identifikators* |
    | Tirgotāja konta ID    | Ievadiet unikālo A ne uzdācības tirgotāja identifikatoru. Šī vērtība tiek nodrošināta, kad pierakstāties ar Ahaen, kā aprakstīts [pierakstā ar Ahaen](adyen-connector-setup.md#sign-up-with-adyen). | Jā | Nē | *Tirgotāja identifikators* |
    | Mākoņa API atslēga          | Ievadiet Ahaen mākoņa API atslēgu. Lai iegūtu šo atslēgu, izpildiet norādes [Sadaļā Kā iegūt API atslēgu](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Jā | Nē | "abcdefg" |
    | Vārtejas vide    | Ahaen vārtejas vide, uz kuru kartēt. Iespējamās vērtības ir Pārbaude **un** Tiešas **·**. Šis lauks jāuzstāda uz Live **tikai** ražošanas ierīcēm un darbībām. | Jā | Jā | "Uz vietas" |
    | Atbalstītās valūtas   | Valūtas, kuras savienotājam jāapstrādā. Pašlaik lietotajos scenārijos Abayen [var](https://www.adyen.com/pos-payments/dynamic-currency-conversion) atbalstīt papildu valūtas, izmantojot dinamisko valūtas konvertēšanu pēc darbības pieprasījuma nosūtīšanas uz maksājumu termināli. Sazinieties ar Ahaen atbalstu, lai iegūtu atbalstīto valūtu sarakstu. | Jā | Jā | "USD; EUR" |
    | Atbalstītie konkursu veidi | Norēķinu veidi, kas jāapstrādā savienotājam. | Jā | Jā | "Atmaksa par smaku" |

1. Kad savienotāja rekvizītu iestatīšana pabeigta, **palaidiet 1070 (Kanāla konfigurācijas**) sadales grafika darbu.

## <a name="configure-commerce-pos-for-google-pay"></a>Konfigurēt Commerce POS for Konfigurējiet Commerce POS for Algu

POS konfigurācija izmanto aparatūras **profila EFT** pakalpojuma lauka iestatījumu Dynamics 365 maksājumu savienotājam Ahaenā. Informāciju par to, kā konfigurēt elektronisko līdzekļu pārskaitījuma (EFT) pakalpojumu Dynamics 365 Maksājumu savienotājam A nosūtīšanai programmā Commerce Headquarters, [skatiet Sadaļā Dynamics 365 POS aparatūras profila iestatīšana](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Procesora kartēšana A pārkaru savienotājam tver Pārlūka karšu tipus, ko Neapmaksāts izmanto POS terminālī.

### <a name="use-the-payment-express-module-with-google-pay"></a>Lietot maksājuma ekspresmoduli ar Maksājuma apmaksu

Commerce Payment Express modulis darbojas ar atbalsta maksājumu metodēm, lai vietas debitoriem varētu ātrāk veikt pārbaudi, izmantojot viņu maksājumu pakalpojuma konta informāciju norēķinu procesa laikā. Maksājuma ekspresmoduļam ir atsauce uz konfigurēto savienotāja pogu, un tas atgriež lietotāja atlasītā pasūtījuma detaļas (adresi, kontaktinformāciju un maksāšanas metodi), lai varētu aizpildīt paņemšanu no formas.

Ja maksājuma ekspresmodulis tiek lietots ar Maksājuma kodu, ja debitori sadaļā Maksājumu express atlasa pogu Maksājuma **steidzamais** maksājums, tiek atvērts maksājums iframe. Lietotāji var tad pieteikties savā Pamatteksta kontā, lai izmantotu savu konta piegādes adresi, rēķina adresi, e-pasta adresi un Outlook maksājuma metodi pēc izvēles maksāt par darbību.

Kad lietotāji izpildīs darbību logāRaktas apmaksa, viņi tiek novirzīti uz Commerce vietnes norēķinu lapu, kur norēķināšanas forma ir iepriekš aizpildīta ar savu Konta apmaksas informāciju. Kad lietotāji atgriežas norēķināšanas lapā no loga Pasūtījuma apmaksa, viņi redzēs šādu informāciju:

- Maksājuma ekspresplūsmā pirmā piegādes opcija, kas ir pieejama atgrieztai piegādes adresei, tiks iepriekš atlasīta debitoram.
- Ja tiek izmantota Konta apmaksa, e-pasta adrese netiek atgriezta. Viesa reģistrēšanās lietotājiem būs jāievada e-pasta adrese kases lapas kontaktinformācijas sadaļā. Pierakstīšanās lietotājiem automātiski tiks aizpildīti viņu Dynamics debitora kontā (primārā e-pasta adrese, ko tie izmantoja autentifikācijai).

Debitoriem ir iespēja pārskatīt pasūtījumus un mainīt detalizētu informāciju par pārbaudes pasūtījumu, pirms **tie izvēlas Veikt pasūtījumu**, lai pabeigtu pasūtījumu.

### <a name="configure-google-pay-in-site-builder"></a>Konfigurējiet Konta apmaksas vietu veidotājā 

Pirms konfigurējat savus fragmentus vai lapas ar Algu, jums jānodrošina, lai Commerce Site Builder tiktu iestatītas jūsu vietnes satura drošības politikas.

Lai nodrošinātu, ka jūsu satura drošības politikas ir iestatītas vietas veidotājā, sekojiet šiem soļiem.

1. Jūsu vietnē dodieties uz sadaļu **Vietnes iestatījumu \> paplašinājumi**.
1. **Cilnē** Satura drošības politika pievienojiet rindu bērnelementiem rc, `*.google.com`**savienot-src** **,** **rāmja priekštečiem**, **rāmja-src**, **img-src**, **skripta-src**, **un stila un ciļņu** direktīvas.
1. Kad esat beidzis, atlasiet Saglabāt **un publicēt**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Konfigurējiet maksājuma ekspres fragmentu ar Saņemšanas maksu vietnes veidotājā

Lai iestatītu maksājuma ekspres fragmentu ar Maksājuma, kas paredzēts tiešsaistes veikalam, sekojiet šiem soļiem.

1. Vietas veidotājā dodieties uz **Fragmenti**.
1. Atlasiet **Jauna**.
1. Dialoglodziņā Jauns **fragments** atlasiet moduli **Konteiners**, ievadiet fragmenta nosaukumu (piemēram, **Ekspres**-paņemšanu) un pēc tam atlasiet **Labi**. 
1. Atlasiet jaunā fragmenta noklusējuma konteinera **slotu**.
1. Rekvizītu rūtī labajā pusē iestatiet konteinera moduļa rekvizītus:

    - **Virsraksts** – ievadiet virsrakstu, kas tiks rādīts jūsu vietnes ekspres-pārbaudes sadaļai (piemēram, Ātrā **pārbaude**).
    - **Konteinera izkārtojums** — atlasiet **plūsmu**.
    - **Platums** — atlasiet aizpildīšanas **konteineru**.
    - **Rādītie** bērniem – **atlasiet** Trīs, lai norādītu bērnu skaitu, kas iederas norēķinu lapas ekspresmaksājuma sadaļas rindā (piemēram, teksta lodziņu, maksājumu ekspresmaksājumu PayPal un maksājuma ekspresmaksājumu Lauku maksājumam).
    - **CSS klases nosaukums** – ievadiet **soda naudas ekspresmaksājuma konteineru** (obligāti).

    > [!IMPORTANT]
    > - Lai **CSS kontrolētu konteinera** darbību pārbaudes laikā **, klases nosaukuma vērtībai** ir jābūt iestatītai uz konteineri ar mainīto maksājuma vērtību. Šī uzvedība ietver paslēpšanu, saliekšanu un citas darbības, kas attiecas uz ekspres-pārbaudes sadaļu pārbaudes plūsmas laikā. Konteineris **-express-payment-container** darbojas ar noklusējuma operācijām, kas ir izlaistas ar moduļa bibliotēkas pārbaudes moduli.
    > - Klases nosaukumam var pievienot papildu **CSS stilus**. Ja pielāgojat moduļa darbību, pārbaudiet stila kontroles, ja izmantojat to pašu moduļa bibliotēkas kodē darbību pārbaudes modulī, lai noteiktu eksprespārbaudes darbību.

1. Noklusējuma konteinera **slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet Maksājuma ekspresmoduli **un** pēc tam atlasiet **Labi**.
1. Maksājuma ekspresmoduļa **rekvizītu** rūtī iestatiet vai **iFrame** koriģējiet vērtības augstumu pikseļos (piemēram, **60**).
1. Laukā **Atbalstītie norēķinu** veidi ievadiet **Atmaksu**. Vērtībai ir jāatbilst **atbalstīto** norēķinu veidu virknei savienotājā, kas ir iestatīts kanālam ([kā aprakstīts iepriekš šajā rakstā sadaļā Commerce tiešsaistes veikala konfigurēšana Šim](#configure-a-commerce-online-store-for-google-pay) uzņēmumam).

    > [!NOTE]
    > Jūs varat atkārtot soļus no 6 līdz 9, lai pievienotu Maksājuma **ekspresmoduļi** citām maksājuma metodēm. Izlīdziniet **atbalstīto norēķinu veidu** vērtību ar papildu konfigurētiem maksājumu veidiem (piemēram, **Paypal**).

1. Nav obligāti: jūs varat pievienot teksta bloķēšanas moduli noklusējuma konteinera modulim, lai ietvertu instrukcijas vai izpaušanas informāciju. Pēc moduļa pievienošanas rekvizītu rūtī ievadiet vēlamo tekstu bagātinātā **teksta** laukā. Varat novietot tekstu virs vai zem maksājuma ekspresmoduļiem, atlasot elipsi (...)**teksta bloka slotā un pēc tam atlasot** **Pārvietot uz augšu vai** Pārvietot uz leju.**·** **·**
1. Atlasiet **Saglabāt,** lai saglabātu izmaiņas, un pēc tam atlasiet Pabeigt **rediģēšanu**.
1. Atlasiet Publicēt **,** lai publicētu fragmentu.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Pievienot maksājuma ekspres fragmentu norēķinu lapai

Lai pievienotu maksājuma ekspres fragmentu norēķinu lapai, sekojiet šiem soļiem.

1. Vietas veidotājā dodieties uz **Lapas** un tad izvēlieties jūsu vietnes pārbaudes lapu.
1. Atlasiet **Rediģēt**.
1. Galvenajā slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī labajā pusē iestatiet konteinera moduļa rekvizītus:

    - **Konteinera izkārtojums —** atlasiet stekā **sakrautus**.
    - **Platums** — atlasiet aizpildīšanas **konteineru**.
    - **·** **Bērniem** ir rādīts – atlasiet trīs, lai norādītu bērnu skaitu, kas iederas norēķinu lapas ekspresmaksājuma sadaļas rindā (piemēram, teksta lodziņš, tiešais maksājums PayPal un maksājums Arko apmaksai).

1. Konteinera moduļa **slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **fragmentu**.
1. Dialoglodziņā Atlasīt **fragmentu** atlasiet izveidoto ekspresmaksājuma fragmentu un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt,** lai saglabātu izmaiņas, un pēc tam atlasiet Pabeigt **rediģēšanu**.
1. Atlasiet **Publicēt,** lai publicētu lapu.

> [!NOTE]
> Ja norēķinu lapā jau ir ietverts konteiners, kuram ir norēķinu fragments, un vēlaties, lai maksājuma ekspresmodulis tiktu atveidots virs parastā norēķinu konteinera, varat to novietot virs esošā paņemšanu vai zem tās, atlasot galvenā slota daudzpunkti (**...**)**·** **·** **un pēc tam atlasot Pārvietot uz augšu vai Pārvietot uz leju.**

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Pievienot maksājuma ekspres fragmentu groza lapai

Lai groza lapai pievienotu maksājuma ekspres fragmentu, sekojiet šiem soļiem.

1. Vietas veidotājā dodieties uz **Sadaļu** Lapas un pēc tam atlasiet jūsu vietnes groza lapu.
2. Atlasiet **Rediģēt**.
3. Izklāsta skatā izvērsiet galveno slotu **koka** skatā un atrodiet konteineru, kas satur grozu **moduli**.
4. Modulī **Grozs** atlasiet maksājuma **ekspresatslēpu**, atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
5. Dialoglodziņā Moduļu **atlase** atlasiet Maksājuma ekspresmoduli **un** pēc tam atlasiet **Labi**.
6. Izvēlieties Maksājuma ekspresmoduļa **slotu**. Pēc tam rekvizītu rūtī, kas atrodas labajā pusē, sadaļā Atbalstītie **norēķinu veidi** ievadiet **Nemaksa**. Vērtībai ir jāatbilst **atbalstīto** norēķinu veidu virknei savienotājā, kas tika iestatīts kanālam ([kā aprakstīts iepriekš šajā rakstā sadaļā Commerce tiešsaistes veikala konfigurēšana Šim](#configure-a-commerce-online-store-for-google-pay) uzņēmumam).
1. Atlasiet **Saglabāt,** lai saglabātu izmaiņas, un pēc tam atlasiet Pabeigt **rediģēšanu**.
1. Atlasiet **Publicēt,** lai publicētu lapu.

Lietotāji var iekļaut līdz pat trīs atbalstītiem **Payment Express** moduļiem (citiem vārdiem, trīs pieejamās atbalstītās maksājumu opcijas) grozā **Payment Express slotā**.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Iestatīt Pret apmaksas sistēmu kā opciju norēķinu maksājumu sadaļā

Jūs varat iestatīt Algu kā opciju norēķinu maksājuma sadaļā tikai maksājumam, kas nav ekspresfunkcionalitāte. Lietotājs aizpildīs šo norēķināšanas formu, un Šim norēķinā apmaksas lapai tiks sagatavots tikai Siam Maksājuma paņemšanu. Lai pārrakstītu ievadīto informāciju par paņemšanu, netiks izmantota neviena Konta informācija.

> [!NOTE]
> Šī procedūra pieņem, ka jūsu vietne izmanto kontroles fragmentu, kas ir konfigurēts ar savākšanas informāciju, piegādes adresi, piegādes opcijām, kontaktinformāciju, neobligātiem nosacījumiem un pārbaudes elementu sadaļu. Noklusējuma moduļa bibliotēkas pārbaudes modulis tiek izdots, izmantojot norēķinu sadaļas konteineru, kam ir teksta bloķēts, lojalitātes programmas punkti, dāvanu karte un maksājumu moduļi. Papildinformāciju skatiet maksājumu [modulī](../payment-module.md).

Lai uzstādītu Saņemšanas apmaksu kā regulāru maksājumu opciju **norēķinu lapas** sadaļā Maksājuma metode, sekojiet šiem soļiem.

1. Vietas veidotājā dodieties uz **Fragmenti** un pēc tam atlasiet jūsu vietnes paņemšanu fragmentu.
1. Atlasiet **Rediģēt**.
1. **Izvēlnes informācijas slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet maksājumu moduli **un** pēc tam atlasiet **Labi**.
1. **Maksājumu moduļa** rekvizītu rūtī labajā pusē iestatiet rekvizītus konteinera modulim:

    - **Virsraksts** – ievadiet virsrakstu, kas tiks rādīts jūsu vietnes ekspresmaksāšanas sadaļai (piemēram, **Apmaksa par Apmaksu).**
    - **– mainiet iFrame** vērtību uz vēlamo dizaina augstumu pikseļos (piemēram, **75**). 
    - **Atbalstītie norēķinu** veidi – ievadiet **Maksājuma maksājumu**, lai atbilstu Programmas Commerce Headquarters pasūtījumu maksājumu savienotāja konfigurācijai.
    - **Ir primārais maksājums** - atstājiet izvēles rūtiņu notīrītu. (Šis rekvizīts parasti tiek iespējots Ahaen pārbaudes modulim.)
    - **Maksājuma stila ignorēšana** — šis rekvizīts netiek atbalstīts Šai Maksājuma konfigurācijai.
    - **Izmantot savienotāja ID** – šis rekvizīts ir jāatlasa, ja lapā tiek izmantoti vairāki maksājumu savienotāji.

1. Novietojiet moduli virs vai zem citiem maksājumu moduļiem, atlasot daudzpunkti (**...**)**maksājuma** slotā un pēc tam atlasot **Pārvietot** uz augšu vai **Pārvietot uz leju**.
1. Atlasiet **Saglabāt,** lai saglabātu izmaiņas, un pēc tam atlasiet Pabeigt **rediģēšanu**.
1. Atlasiet **Publicēt**.

### <a name="modes-of-delivery"></a>Piegādes veidi

Ar maksājuma ekspresmoduli, kas izmanto Debitora apmaksu, tiks iepriekš atlasīta pirmā piegādes opcija, kas tiek atgriezta attiecībā pret atlasīto piegādes adresi no Debitora maksājuma konta. Lietotājiem ir iespēja pielāgot piegādes adresi dažādām opcijām, ja vēlaties.

Pasūtījums, kurā tiek rādītas piegādes metodes maksājuma ekspresmoduļa modulī, ir konfigurēts **kanāla** piegādes lapā Commerce Headquarters. Programmā Commerce headquarters dodieties uz **mazumtirdzniecības un commerce \> kanālu \> tiešsaistes** veikaliem un atlasiet **veikala mazumtirdzniecības kanāla ID** vērtību. Darbību rūts cilnē Iestatījumi **atlasiet** Piegādes **veidi**. Uzskaitītie piegādes režīmi tiks parādīti vienā pasūtījumā maksājuma ekspresmoduļa. Atlasiet **Pārvaldīt piegādes veidus** Darbību rūtī, lai pievienotu vai noņemtu mazumtirdzniecības kanāla vai preces piegādes veidus. Papildinformāciju par to, kā iestatīt piegādes veidus [, skatiet piegādes veidu iestatīšana](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Pārbaudes modulis izmanto arī piegādes opciju moduli, ja piegādes režīmi tiek renderēti pārbaudes laikā. Papildinformāciju skatiet piegādes [opciju modulī](../delivery-options-module.md).

Piegādes veidi tiek rādīti tā, kā tie ir pievienoti **tiešsaistes veikala piegādes** sarakstam Režīmi.

## <a name="additional-resources"></a>Papildu resursi

[Bieži uzdotie jautājumi par maksājumiem](payments-retail.md)

[Norēķināšanās modulis](../add-checkout-module.md)

[Maksājumu modulis](../payment-module.md)
