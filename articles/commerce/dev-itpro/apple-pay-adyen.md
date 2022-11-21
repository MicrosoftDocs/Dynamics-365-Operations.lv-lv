---
title: Apple Pay iestatīšana pakalpojumā Adyen Dynamics 365 Commerce
description: Šajā rakstā ir aprakstīts, kā iestatīt pakalpojumu Apple Pay ar Adyen pakalpojumā Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 0949b9d7a4b181605d43956932b4fc095940bd64
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780207"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Apple Pay iestatīšana pakalpojumā Adyen Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt pakalpojumu Apple Pay ar Adyen pakalpojumā Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | Apraksts |
|---|---|
| Apple Pay | Apple Pay, kas pazīstams arī kā Apple Pay "poga", ir maka maksājumu piedāvājums, kas tiek atbalstīts, izmantojot Adyen savienotāju. Tas nodrošina klientu pieredzi un integrāciju, ko atbalsta 365 Apple Pay savienotājs Microsoft Dynamics. |
| Maka | Maksājuma veids, kas neietver tradicionālos maksājumu raksturlielumus, piemēram, bankas identifikācijas numura (BIN) diapazonu un derīguma termiņu, ko izmanto, lai atšķirtu kredītkaršu un debetkaršu veidus. |

Dynamics 365 Commerce piedāvā gatavu integrāciju pakalpojumam Apple Pay, kad tiek izmantots Adyen maksājumu vārtejas pakalpojums. Apple Pay ir digitālā maka maksājuma veids, kas izmanto Apple Pay tirgotāja kontu sadarbībā ar Adyen maksājumu pakalpojumu. Kad tas ir konfigurēts, Apple Pay poga ir atlasāms maksājuma veids, kas ir daļa no tiešsaistes veikala pasūtījuma izrakstīšanās lapas. Poga Apple Pay tiek parādīta kā maksāšanas iespēja tikai atbalstītajām Apple Pay ierīcēm. Kad lietotāji atbalsta pārlūkprogrammā vai ierīcē atlasa **pakalpojumu Apple Pay**, viņi tiek novirzīti uz pakalpojumu Apple Pay, lai tieši pabeigtu maksājumu. Pēc tam tie tiek atgriezti tiešsaistes veikalā pasūtījuma pabeigšanai.

Dynamics 365 Payment Connector for Apple Pay savienotāja atsauce tiek izmantota papildus Dynamics 365 Payment Connector pakalpojumam Adyen, lai vietnē iespējotu maksājumus pakalpojumā Apple Pay un kredītkaršu maksājumus. Pakalpojumu Apple Pay var konfigurēt lietošanai arī veikalos, kuros ir Adyen maksājumu termināļi, kas izmanto Dynamics 365 Payment Connector for Adyen ar commerce point of sale (POS). Šajā gadījumā Dynamics 365 Payment Connector for Adyen apstrādā Apple Payment ierīci, kas pieskaras caur termināli.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai izmantotu pakalpojumu Apple Pay ar Adyen programmatūrā Commerce, ir nepieciešams Apple tirgotāja konts. Informāciju par to, kā iestatīt pakalpojumu Apple Pay klientu testa zonā, skatiet sadaļā [Pakalpojuma Apple Pay nodošanas integrācija](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Informāciju par to, kā rīkoties, kad esat gatavs sākt darbību savā ražošanas vidē, skatiet sadaļā [Tiešraide](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Apple Pay maksājuma veidam ir jābūt integrētam arī jūsu Adyen kontā. Adyen var palīdzēt iestatīt maksājuma veidu, kā arī nodrošināt, ka domēni, kuriem izmantosit sertifikātu, tiek piešķirti lietošanai kopā ar sertifikātu.

Lai iespējotu uzlabotā maka līdzekļa karodziņu Commerce galvenajā mītnē, dodieties uz sadaļu **Darbvietu līdzekļu \> pārvaldība** un meklējiet **funkciju Uzlabots maka atbalsts un maksājumu uzlabojumi**. Atlasiet līdzekli un pēc tam atlasiet **Iespējot**. Kad līdzeklis ir iespējots, palaidiet **1110** izplatīšanas grafiku, lai izmaiņas būtu pieejamas visos kanālos.

## <a name="map-the-apple-pay-payment-method"></a>Apple Pay maksājuma veida kartēšana

Apple Pay ir digitālā maka maksājuma veids. Informāciju par to, kā iestatīt maksājumu kartēšanu pakalpojumam Apple Pay, skatiet sadaļā [Maka maksājumu atbalsts](../wallets.md).

Lai kartētu Apple Pay maksājuma veidu Commerce galvenajā mītnē, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Mazumtirdzniecības un komercijas \> kanālu iestatīšana \> Maksājumu veidi Karšu veidi \>**.
1. Atlasiet **Jauns**, lai pievienotu rindu pakalpojumam Apple Pay, un iestatiet tālāk norādītās vērtības.

    - **ID:** ApplePay
    - **Elektroniskā maksājuma nosaukums:** Apple Pay
    - **Veids:** Maks
    - **Izdevējs:** Apple

1. Atlasiet **Procesora kartēšana**, lai atvērtu dialoglodziņu Procesora **maksājumu kartēšanas metodes**. Kolonnā **Unmapped Processor Payment Methods (Nemappped Processor Payment Methods**) ir uzskaitītas atbalstītās maksājumu metodes katram pieejamajam savienotājam (Adyen, PayPal un Apple).
1. Kartējiet atbalstītās maksāšanas metodes, kuras vēlaties izmantot gan Dynamics 365 Payment Connector for Adyen **Connector (izmantošanai POS), gan** **Dynamics 365 Payment Connector for Apple Pay** savienotājam (tiešsaistes kanālam).
1. Katrai kartēšanas rindai **kolonnā Nekartētie procesora maksājumu veidi** atlasiet atbalstāmo rindu un pēc tam atlasiet **Pievienot**, lai pārvietotu atlasi uz **kolonnu Kartētā procesora maksājumu metodes**.
1. Atlasiet **Labi** un pēc tam **lapā Karšu tipi** atlasiet **Saglabāt**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Apple Pay sertifikāta iestatīšana vietnei

Katrai vietnei ir jāaugšupielādē domēna asociācijas fails (pazīstams arī kā Apple Pay sertifikāts), kā aprakstīts [Adyen Apple Pay dokumentācijā](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). Varat izmantot Commerce vietņu veidotāju, lai augšupielādētu domēnu piesaistes failu savas vietnes multivides bibliotēkā.

Lai vietnes veidotājā iestatītu Apple Pay sertifikātu, veiciet tālāk norādītās darbības.

1. Lejupielādējiet sertifikātu (domēna asociācijas failu) no [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Pievienojiet .txt paplašinājumu domēna piesaistes failam.
1. Vietnes veidotājā [augšupielādējiet](../upload-serve-static-files.md) domēnu piesaistes failu savas vietnes multivides bibliotēkā.
1. Dodieties uz **vietrāžiem URL**.
1. Atlasiet **Jauns \> Jauns URL**.
1. Dialoglodziņā **Jauns URL** atlasiet **Multivides bibliotēkas līdzeklis**.
1. **Laukā URL ceļš** ievadiet URL ceļu (ja tas vēl nav ievadīts). Pēc domēna bāzes URL ievadiet šādu Apple virkni:`<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Atlasiet **Nākamais**. Multivides bibliotēkā tiek rādīti visi augšupielādētie dokumenta **(.txt) tipa multivides līdzekļi**.
1. Atlasiet domēnu piesaistes failu, kas ir jāpiegādā pieprasījumiem uz iepriekš definēto vietrādi URL.
1. Atlasiet **Izveidot**.

Šajā brīdī vietrādis URL, kuru izveidojāt, ir melnraksta statusā. Publicējiet vietrādi URL, lai pabeigtu procesu. Fails, uz kuru URL norāda, netiks atgriezts, līdz publicēsit vietrādi URL.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Commerce tiešsaistes veikala konfigurēšana pakalpojumam Apple Pay

Lai konfigurētu Commerce tiešsaistes veikalu pakalpojumam Apple Pay, veiciet tālāk norādītās darbības.

1. Galvenajā mītnē Commerce dodieties uz **mazumtirdzniecības un komercijas \> kanālu \> tiešsaistes veikaliem**.
1. **Atlasiet savas vietnes tiešsaistes veikala kanāla mazumtirdzniecības kanāla ID** vērtību.
1. Kopsavilkuma **cilnē Maksājumu konti** pievienojiet **Dynamics 365 Payment Connector for Adyen Connector, ja tas vēl nav iestatīts, izpildot norādījumus sadaļā** Dynamics 365 Payment Connector iestatīšana pakalpojumam [Adyen](adyen-connector-setup.md).
1. Kad Adyen savienotājs ir konfigurēts, atlasiet **Pievienot**, lai pievienotu Dynamics 365 Payment Connector for Apple Pay **savienotāju**.
1. Ievadiet savienotāja tirgotāja rekvizītu vērtības.

    | Rekvizīts               | Apraksts | Obligāti | Automātiska iestatīšana | Parauga vērtība |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Komplektācijas nosaukums          | Dynamics 365 Payment Connector pakalpojumam Apple Pay montāžas nosaukums. | Jā | Jā | Binārais vārds |
    | Pakalpojuma konta ID     | Tirgotāja rekvizītu iestatīšanas unikālais identifikators. Šis identifikators tiek apzīmogots maksājumu transakcijām un identificē tirgotāja rekvizītus, kas jāizmanto pakārtotajos procesos (piemēram, rēķinu izrakstīšanā). | Jā | Jā | Guid |
    | Tirgotāja konta ID    | Ievadiet unikālo Adyen tirgotāja identifikatoru. Šī vērtība tiek nodrošināta, reģistrējoties ar Adyen, kā aprakstīts sadaļā [Reģistrēšanās ar Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Jā | Nē | Tirgotāja identifikators |
    | Mākoņa API atslēga          | Ievadiet Adyen mākoņa API atslēgu. Šo atslēgu var iegūt, izpildot sadaļā Kā iegūt API atslēgu [sniegtos](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key) norādījumus. | Jā | Nē | ABCDEFG |
    | Vārtejas vide    | Ievadiet Adyen vārtejas vidi, uz kuru kartēt. Iespējamās vērtības ir **Test** un **Live**. Šis lauks ir jāiestata uz **Dzīvot** tikai ražošanas ierīcēm un transakcijām. | Jā | Jā | Reāllaika |
    | Atbalstītās valūtas   | Ievadiet valūtas, kuras savienotājam vajadzētu apstrādāt. Kartes pašreizējos scenārijos Adyen var atbalstīt papildu valūtas, izmantojot [dinamisku valūtas konvertēšanu](https://www.adyen.com/pos-payments/dynamic-currency-conversion) pēc darījuma pieprasījuma nosūtīšanas uz maksājumu termināli. Sazinieties ar Adyen atbalsta dienestu, lai iegūtu atbalstīto valūtu sarakstu. | Jā | Jā | USD; EUR |
    | Atbalstītie konkursu veidi | Ievadiet savienotājam apstrādājamos izsoles veidus. | Jā | Jā | ApplePay |

1. Kad tirgotāja informācija ir ievadīta, palaidiet **1070** kanāla konfigurācijas izplatīšanas grafika uzdevumu.

## <a name="configure-commerce-pos-for-apple-pay"></a>Commerce POS konfigurēšana pakalpojumam Apple Pay

POS konfigurācija izmanto aparatūras profila **EFT pakalpojuma** lauka konfigurāciju Dynamics 365 Payment Connector for Adyen. Programmas Commerce galvenajā mītnē konfigurējiet EFT pakalpojumu programmai Dynamics 365 Payment Connector for Adyen, kā aprakstīts sadaļā [Dynamics](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile) 365 POS aparatūras profila iestatīšana.

Noteikti pievienojiet **ApplePay** piedāvājumu veidu sarakstam laukā Atbalstītie **konkursu veidi**. Izmantojiet semikolus (;) lai sarakstā nodalītu piedāvājumu veidus.

Adyen savienotāja procesora kartēšana tvers maka karšu veidus, ko izmanto Apple Pay POS terminālī.

### <a name="configure-content-security-policies-in-site-builder"></a>Satura drošības politiku konfigurēšana vietnes veidotājā

Pirms konfigurējat fragmentus vai lapas, lai izmantotu pakalpojumu Apple Pay, jums ir jāpārliecinās, vai jūsu satura drošības politikas (CSP) ir konfigurētas jūsu vietnes Commerce vietņu veidotājā.

Lai konfigurētu satura drošības politikas vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.
1. Cilnē Satura drošības politika atlasiet Pievienot **, lai pievienotu rindu, kas ir pakārtotajām** **sadaļām src, connect-src, frame-src, img-src,**`https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js`**script**-src un **style-src.** **·** **·** **·** **·**
1. Kad esat pabeidzis, atlasiet **Saglabāt un publicēt**, lai veiktu izmaiņas.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Apple Pay kā norēķināšanās iespējas iestatīšana

Lai iestatītu pakalpojumu Apple Pay kā norēķinu maksāšanas iespēju savas vietnes (bezekspress) norēķināšanās lapā, veiciet tālāk norādītās darbības.

1. Vietnes veidotājā dodieties uz Fragmenti **un** atlasiet vietnes norēķināšanās fragmentu.
1. Atlasiet **Rediģēt**.
1. Konteinera **slotā Checkout atlasiet daudzpunkti (**...)**un pēc tam atlasiet** Pievienot moduli **.**
1. Dialoglodziņā **Moduļu** atlase atlasiet moduli **Apple Pay** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Apple Pay moduļa **iestatījumi ir iebūvēti modulī un savienojas ar konfigurēto Dynamics 365 Payment Connector for Apple Pay** savienotāju, kas ir iestatīts tiešsaistes kanālam Commerce galvenajā mītnē.

### <a name="apple-pay-payment-behavior"></a>Apple Pay maksājumu darbība

Maksājuma **poga Apple Pay tiek rādīta tikai atbalstītajās Apple Pay ierīcēs (iPhone, iPad un Safari pārlūkprogrammās, kas atbalsta pakalpojumu Apple Pay**). Ja lietotājs neizmanto kādu no šīm ierīcēm, Apple Pay **maksājuma poga tiek paslēpta** no skata.

Kad lietotājs atlasa **maksājuma pogu Apple Pay**, tiek parādīts dialoglodziņš **Apple Pay**. Tur lietotājs var autentificēties, izmantojot savu Apple Pay ierīci vai pārlūkprogrammu. Dialoglodziņā **Apple Pay** tiek parādīts kopsavilkums par pasūtījuma summu un maksājuma veidu, ko lietotājs ir konfigurējis savam Apple Wallet. Lietotājs var pārskatīt šo informāciju un pēc tam atlasīt **Maksāt**, lai pabeigtu maksājumu. Kad maksājums ir pabeigts, lietotājs tiek novirzīts uz **pasūtījuma pabeigšanas** vietnes lapu, kurā tiek parādīts detalizēts pasūtījuma kopsavilkums par pabeigto darījumu.

## <a name="additional-resources"></a>Papildu resursi

[Bieži uzdotie jautājumi par maksājumiem](payments-retail.md)

[Norēķināšanās modulis](../add-checkout-module.md)

[Maksājumu modulis](../payment-module.md)
