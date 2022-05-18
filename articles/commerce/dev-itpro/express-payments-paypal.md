---
title: Konfigurēt tiešos maksājumus par PayPal
description: Šajā tēmā ir aprakstīts, kā konfigurēt tiešos maksājumus PayPal, lai iespējotu ātrākas paņemšanu iespējas Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5fff17959e7ed9299df169c68b2ed07f6b7c7d2c
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743602"
---
# <a name="configure-express-payments-for-paypal"></a>Konfigurēt tiešos maksājumus par PayPal

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt tiešos maksājumus PayPal, lai iespējotu ātrākas paņemšanu iespējas Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | Apraksts |
|---|---|
| PayPal Ar kuru | Klienta pieredze un integrācija, ko atbalsta PayPal savienotājs. Tas ir pazīstams arī kā PayPal poga. |
| Maka | Maksājuma veids, kas neietver tradicionālas maksājuma īpašības, piemēram, Bankas identifikācijas numura (BIN) diapazons un beigu datums, kas tiek izmantoti, lai diferencētu kredītkaršu un debetkaršu tipus. |
| Maksājuma steidzamais | Commerce modulis, kas atbalsta ātrāku norēķinu darbību, ja tiek izmantotas atbalstītās maksājuma metodes. Šī tēma ietver maksājuma ekspresmoduļa izmantošanu ar PayPal. |

Dynamics 365 Commerce piedāvā "PayPal Rīcībā" integrāciju". Konfigurējot Dynamics 365 maksājumu savienotāju klientam PayPal, poga PayPal tiek parādīta kā atlasāma maksājuma metode tiešsaistes pasūtījuma norēķināšanas laikā. Kad lietotāji izvēlas PayPal, tie tiek novirzīti uz to, lai aizpildītu savu maksājumu tieši caur PayPal, un tad tiek atgriezti tiešsaistes StoreFront, lai pabeigtu savu pasūtījumu. PayPal grozu norēķināšana ļauj klientiem izmantot savu maksājumu konta informāciju, lai uzpildītu norēķināšanas formu, lai viņi varētu ātrāk pabeigt norēķināšanas procesu.

Commerce ir pievienojis maksājuma ekspresmoduli, lai atvieglotu ekspres-norēķinus. Maksājuma ekspresmoduli var izmantot fragmentā, ko var ietvert norēķinu vai groza lapā. Kad PayPal ir konfigurēts, tas pats Dynamics 365 maksājumu savienotājs PayPal savienotāja atsaucei tiek izmantots gan maksājuma ekspresieka opcijai, gan parastas norēķināšanas opcijai.

## <a name="paypal-checkout-in-commerce"></a>PayPal norēķinājāies Commerce

### <a name="prerequisites"></a>Priekšnosacījumi

Iestatiet PayPalMac jūsu videi atbilstoši aprakstam [Dynamics 365 Maksājumu savienotājā priekš PayPal](../paypal.md).

Ja izmantojat PayPal kā opciju regulārā norēķinu plūsmā (kur lietotāji manuāli ievada savu konta informāciju, neizmantojot maksājumu eksprespildes darbības), [izpildiet iestatīšanas norādījumus Maksājumu modulī](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Maksājuma ekspresmodulis ar PayPal

Maksājuma ekspresmodulis strādā ar atbalsta maksājumu metodēm, lai vietas debitoriem piedāvātu iespēju ātrāk veikt pārbaudi, iepriekš aizpildot savu maksājumu pakalpojuma konta informāciju iztēruma procesa laikā. Maksājuma ekspresmodulis izmanto konfigurēto maksājumu savienotāju, lai uzpildītu norēķinu formu ar lietotāja konta informāciju, piemēram, adresi, kontaktinformāciju un atlasīto maksāšanas metodi.

Ja tiek izmantota PayPal ekspres-norēķināšana, un lietotājs atlasa pogu PayPal norēķinu lapas maksājuma ekspresmaksājuma sadaļā, tiek atvērts PayPal maksājuma iFrame logs. Lietotājs tad pierakstās savā PayPal kontā, lai izmantotu savu konta piegādes adresi, rēķina adresi, e-pasta adresi un PayPal maksājuma metodi pēc izvēles maksāt par darbību.

Kad lietotājs pabeidz darbību PayPal logā, tie tiek novirzīti atpakaļ uz Commerce vietnes norēķināšanas lapu, kur norēķināšanas forma tiek iepriekš aizpildīta ar viņu atlasīto informāciju. Maksājuma ekspresplūsmā pirmā piegādes opcija, kas ir pieejama atgrieztā piegādes adresei, tiks iepriekš aizpildīta lietotājam. Tad lietotājam ir opcija pārskatīt pasūtījumu un mainīt detalizētu informāciju par pārbaudes pasūtījumu, pirms **lietotājs izvēlas Veikt** pasūtījumu, lai pabeigtu pasūtījumu.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>Pievienojiet maksājuma ekspresmoduli payPal fragmentam

Lai pievienotu maksājuma ekspresmoduli ar PayPal fragmentam Commerce Site Builder, sekojiet šiem soļiem.

1. Dodieties uz vietni.
1. Kreisajā navigācijas rūtī atlasiet Fragmenti **un** pēc tam atlasiet **Jauns**.
1. Dialoglodziņā Jauns **fragments** atrodiet **·** **un atlasiet maksājuma ekspresmoduli un pēc tam sadaļā Fragmenta** nosaukums ievadiet fragmenta nosaukumu (piemēram, Ekspresņemiet). **·**
1. Atlasiet **Labi,** lai izveidotu fragmentu.
1. Izklāsta skatā atlasiet izveidotā maksājuma ekspresmoduļa slotu.
1. Rekvizītu rūtī atlasiet **Virsraksts**.
1. Dialoglodziņa **Virsraksts** **laukā** Virsraksta teksts ievadiet virsraksta tekstu, ko vēlaties rādīt steidzamai paņemšanu sadaļai jūsu vietnē (piemēram, **tieša** pārbaude).
1. Sadaļā **Virsraksta līmenis** atlasiet virsraksta līmeni (piemēram, **H2**).
1. Atlasiet **Labi**.
1. Rekvizītu rūtī laukā **Augstums ievadiet iFrame** vai koriģējiet elementa iFrame augstumu (piemēram, **60**).
1. Laukā **Atbalstītie norēķinu** veidi ievadiet **PayPal**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Pievienot maksājuma ekspres fragmentu norēķinu lapai

Lai vietas veidotājā pievienotu maksājuma ekspres fragmentu izdrukas lapai, sekojiet šiem soļiem.

1. Dodieties uz vietni.
1. Navigācijas kreisajā rūtī atlasiet Lapas **un** pēc tam atlasiet jūsu vietnes paņemšanu.
1. Izvēlieties **Rediģēt,** lai rediģētu lapu.
1. Galvenajā slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.

    > [!NOTE]
    > Ja konteinera modulis, kas satur norēķinu fragmentu, jau pastāv, pārvietojiet maksājuma ekspres sadaļu tā, **lai tas parādītos virs esošā norēķinu konteinera galvenajā slotā**. Maksājuma ekspressa sadaļa tiks atveidota virs parastā norēķinu konteinera. Lai pārvietotu konteinera moduli uz augšu vai uz leju, atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pārvietot uz **augšu** vai **Pārvietot uz leju**.

1. **Konteinera rekvizītu** rūtī ir ieteicams konfigurēt rekvizītu iestatījumus šādā veidā:

    - **Konteinera izkārtojums —** atlasiet stekā **sakrautus**.
    - **Platums** — atlasiet aizpildīšanas **konteineru**.
    - **Parādītās bērnu kategorijas** – atlasiet **trīs**.

1. Konteinera slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **fragmentu**.
1. Dialoglodziņā Atlasīt **fragmentu** atrodiet un atlasiet izveidoto ekspresmaksājuma fragmentu un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Pievienot maksājuma ekspres fragmentu groza lapai

Lai vietas veidotājā groza lapai pievienotu maksājuma ekspres fragmentu, sekojiet šiem soļiem.

1. Dodieties uz vietni.
1. Kreisajā navigācijas rūtī atlasiet Lapas **un** pēc tam atlasiet jūsu vietnes groza lapu.
1. Izvēlieties **Rediģēt,** lai rediģētu lapu.
1. Galvenajā slotā **atrodiet** konteineru, kas satur groza **moduli**. Grozs **modulī** būs maksājuma eksprespreso **slots**.
1. Atlasiet Maksājuma **ekspres** slotu, atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet Maksājuma ekspresmoduli **un** pēc tam atlasiet **Labi**.
1. Rekvizītu rūts laukā Atbalstītie **norēķinu veidi** ievadiet vērtību **Paypal**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

### <a name="modes-of-delivery"></a>Piegādes veidi

Kad maksājuma ekspresmodulis ir konfigurēts izmantot PayPal, tiks iepriekš aizpildīta pirmā piegādes opcija, kas tiek atgriezta piegādes adresei, kas tika atlasīta PayPal kontam. Lietotāji, ja vēlaties, var mainīt piegādes adresi.

Piegādes veida pasūtījums ir konfigurēts Commerce **Headquarters** kanāla piegādes sadaļā Režīmi. Plašāku informāciju skatiet [Piegādes veidu iestatīšana](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Pārbaudes modulis izmantos arī piegādes opciju moduli, kad piegādes režīmi tiek atveidoti pārbaudes laikā. Papildinformāciju skatiet piegādes [opciju modulī](../delivery-options-module.md).

Piegādes veidi tiek pievienoti sarakstam ar tiešsaistes veikalu programmā Commerce Headquarters. Dodieties uz **mazumtirdzniecības \> un \> commerce kanālu** interneta veikaliem un atlasiet veikala kanāla ID. Pēc tam atlasiet **Iestatiet \> piegādes veidus**. Piegādes moduļa režīmi, kas tiek rādīti konfigurācijā, tiks parādīti līdzīgi vietai. Lai pievienotu vai noņemtu mazumtirdzniecības kanāla vai preces piegādes režīmus **, darbību rūtī atlasiet** Pārvaldīt piegādes veidus.

## <a name="additional-resources"></a>Papildu resursi

[Bieži uzdotie jautājumi par maksājumiem](payments-retail.md)

[Norēķināšanās modulis](../add-checkout-module.md)

[Maksājumu modulis](../payment-module.md)

[Iestatiet piegādes veidus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Piegādes opciju modulis](../delivery-options-module.md)
