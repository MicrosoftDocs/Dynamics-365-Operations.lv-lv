---
title: E-pasta ziņojumu veidņu izveide transakciju notikumiem
description: Šajā tēmā ir aprakstīts, kā izveidot, augšupielādēt un konfigurēt e-pasta veidnes darbību notikumiem programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2da1044cd332d841a8c18f7139d0d8c09bad95f446494034060e59416b4018b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718711"
---
# <a name="create-email-templates-for-transactional-events"></a>E-pasta ziņojumu veidņu izveide transakciju notikumiem

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot, augšupielādēt un konfigurēt e-pasta veidnes darbību notikumiem programmā Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce nodrošina ārpus kastes risinājumu, kas paredzēts, lai sūtītu e-pasta ziņojumus, kas brīdina debitorus par darbību notikumiem (piemēram, kad tiek veikts pasūtījums, pasūtījums ir gatavs saņemšanai vai pasūtījums ir nosūtīts). Šajā tēmā aprakstīti soļi, kā izveidot, augšupielādēt un konfigurēt e-pasta veidnes, kas tiek izmantotas, lai nosūtītu darbības e-pasta ziņojumus.

## <a name="create-an-email-template"></a>E-pasta veidnes izveidošana

Pirms varat kartēt specifisku darbību notikumu uz e-pasta veidni, ir jāizveido veidne.

Lai izveidotu e-pasta veidni, izpildiet tālāk norādītās darbības.

1. Programmā Commerce Headquarters atveriet **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Organizācijas e-pasta veidnes** vai **Organizācijas administrēšana \> Iestatīšana \> Organizācijas e-pasta veidnes**.
1. Atlasiet **Jauns**.
1. Sadaļā **Vispārīgi** iestatiet šādus laukus:

    - **E-pasta ID** — e-pasta ID ir unikāls veidnes identifikators, un tā ir vērtība, kas tiek rādīta, atlasot veidni, ko kartēt uz notikumu.
    - **E-pasta apraksts** — jūs varat izmantot šo neobligāto lauku, lai sniegtu veidnes aprakstu. Ievadītā vērtība parādās tikai Commerce galvenajā mītnē.
    - **Sūtītāja vārds** — ievadītais vārds parādās laukā “no” vairumā e-pasta klientu.
    - **Sūtītāja e-pasts** — ievadiet e-pasta adresi, kas jālieto e-pasta ziņojumiem, kas tiek nosūtīti, izmantojot šo veidni.
    - **Noklusētais valodas kods** — šis lauks norāda pēc noklusējuma nosūtītā e-pasta ziņojuma lokalizēto versiju, ja kanāls, kas izsauc šo veidni, nesniedz nekādu valodu.

1. Sadaļā **E-pasta** ziņojuma saturs atlasiet **Jauns**.
1. Laukā **Valoda** ievadiet e-pasta veidnes valodu. Vēlāk varat pievienot vairākas valodas un lokalizētas veidnes.
1. Laukā **Tēma** ievadiet e-pasta tēmu, kam jāparādās e-pasta tēmas laukā.
1. Atlasiet **Rediģēt**, lai augšupielādētu savu e-pasta veidni.

## <a name="create-an-email-message-body-by-using-html"></a>E-pasta ziņojuma pamatteksta izveidošana, izmantojot HTML

E-pasta ziņojuma pamatteksts ir sastādīts HTML formātā. Jūs varat izmantot jebkuru izkārtojumu, stilu un zīmolu, ko HTML un iekļautās kaskadētās stila lapas (CSS) atļauj. Varat arī izmantot attēlus, ja tos uzturēsiet publiski pieejamā Web galapunktā. Lai pievienotu attēlu, ievadiet attēla vietrādi URL, kas ir norādīts **src** atribūtā HTML **&lt;img&gt;** etiķetei.

> [!NOTE]
> E-pasta klienti nosaka izkārtojuma un stila ierobežojumus, kas varētu prasīt labojumus HTML un CSS, ko izmantojat ziņojuma pamattekstam. Mēs iesakām jums iepazīties ar labāko praksi, lai izveidotu HTML, ko atbalstīs populārākie e-pasta klienti.

## <a name="add-placeholders-to-the-email-message-body"></a>Pievienot vietturus e-pasta ziņojuma pamattekstam

E-pasta ziņojumā var iekļaut vietturus, kas ir aizstāti ar debitoram specifiskām un darbībām specifiskām vērtībām laikā, kad tiek ģenerēts e-pasts. Vietturus vienmēr ietver procentu zīmes (%), un tie tiek ievietoti tieši HTML dokumentā.

Tālāk ir minēts piemērs.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Pasūtījuma vietturi (pārdošanas pasūtījuma līmenis)

Šie vietturi izgūst un rāda datus, kas ir definēti pārdošanas pasūtījuma līmenī (pretēji pārdošanas rindas līmenim).

| Viettura nosaukums     | Viettura vērtība                                            |
| -------------------- | ------------------------------------------------------------ |
| customername         | Klienta vārds, kurš veica pasūtījumu.               |
| customeraddress      | Klienta adrese.                                 |
| customeremailaddress | E-pasta adrese, kuru klients ievadīja norēķināšanās laikā.     |
| salesid              | Pasūtījuma pārdošanas ID.                                   |
| orderconfirmationid  | Starpkanālu ID, kas tika ģenerēts pasūtījuma izveides laikā. |
| channelid            | Tā mazumtirdzniecības vai tiešsaistes kanāla ID, kurā tika veikts pasūtījums. |
| deliveryname         | Konkrēts nosaukums piegādes adresei.        |
| deliveryaddress      | Piegādes adrese nosūtītajiem pasūtījumiem.                     |
| deliverydate         | Piegādes datums.                                           |
| shipdate             | Nosūtīšanas datums.                                               |
| modeofdelivery       | Pasūtījuma piegādes veids.                              |
| ordernetamount       | Pasūtījuma kopējā summa, no kuras atņem nodokļu kopsummu.         |
| atlaide             | Pasūtījuma kopējā atlaide.                            |
| maksas              | Pasūtījuma kopējās izmaksas.                             |
| nodokļi                  | Pasūtījuma kopējie nodokļi.                                 |
| kopā                | Pasūtījuma kopējā summa.                              |
| storename            | Veikala nosaukums, kur tika veikts pasūtījums.            |
| storeaddress         | Veikala adrese, kur tika veikts pasūtījums.              |
| storeopenfrom        | Veikala, kuš veica pasūtījumu, atvēršanās laiks.         |
| storeopento          | Veikala, kuš veica pasūtījumu, aizvēršanās laiks.         |
| pickupstorename      | Veikala nosaukums, kurā pasūtījums tiks paņemts.\* |
| pickupstoreaddress   | Veikala adrese, kurā pasūtījums tiks paņemts.\* |
| pickupopenstorefrom  | Veikala atvēršanās laiks, kurā pasūtījums tiks paņemts.\* |
| pickupopenstoreto    | Veikala aizvēršanās laiks, kurā pasūtījums tiks paņemts.\* |
| pickupchannelid      | Tā veikala kanāla ID, kas ir norādīts piegādes savākšanas režīmam.\* |
| packingslipid        | Tās pavadzīmes ID, kas tika ģenerēta, iepakojot pasūtījuma rindas.\* |

\* Šie vietturi atgriež datus tikai tad, kad tie tiek izmantoti **Pasūtījumam, kas ir gatavs paņemšanai** paziņojuma veidam. 

### <a name="order-line-placeholders-sales-line-level"></a>Pasūtījuma rindas vietturi (pārdošanas rindas līmenis)

Šie vietturi izgūst un parāda datus par atsevišķām precēm (rindām) pārdošanas pasūtījumā.

| Viettura nosaukums               | Viettura vērtība |
|--------------------------------|-------------------|
| productid                      | <p>Preces ID. Šis ID konts variantiem.</p><p><strong>Piezīme:</strong> Šis vietturis ir novecojis par labu **lineproductrecid**.</p> |
| lineproductrecid               | Preces ID. Šis ID konts variantiem. Tas unikāli identificē preci varianta līmenī. |
| lineitemid                     | Produkta preces līmeņa ID. (Šis ID konts nav domāts variantiem.) |
| lineproductvariantid           | Preces varianta ID. |
| lineproductname                | Preces nosaukums. |
| lineproductdescription         | Preces apraksts. |
| linequantity                   | Vienību skaits, kas pasūtīts rindai, plus mērvienība (piemēram, **katrs** vai **pāris**). |
| lineunit                       | Mērvienība rindai. |
| linequantity_withoutunit       | Vienību skaits, kas pasūtīts rindai bez mērvienības. |
| linequantitypicked             | Izvēlēto vienību skaits, kad tiek izmantots **PickOrder** notikums. Pretējā gadījumā **0** (nulle). |
| linequantitypicked_withoutunit | Izdotais vienību skaits bez mērvienības, kad tiek izmantots **PickOrder** notikums. Pretējā gadījumā **0** (nulle). |
| linequantitypacked             | Vienību skaits, kas tika iepakots, kad tiek izmantoti **PackOrder** un **Pasūtījums gatavs saņemšanai** notikumi. Pretējā gadījumā **0** (nulle). |
| linequantitypacked_withoutuom  | Vienību skaits, kas tika iepakots bez mērvienības, kad tiek izmantoti **PackOrder** un **Pasūtījums gatavs saņemšanai** notikumi. Pretējā gadījumā **0** (nulle). |
| linequantityshipped            | Vienmēr **0**, izņemot gadījumus, kad tiek izmantoti konkrēti notikumi, kā aprakstīts nākamajā rindā. |
| linequantityshipped_withoutuom | Izdotais vienību skaits bez mērvienības, kad tiek izmantots **ShipOrder** notikums. Pretējā gadījumā **0** (nulle). |
| lineprice                      | Vienas vienības cena. |
| linenetamount                  | Tiek pielietota rindas cena pēc vienību skaita un atlaides. |
| linediscount                   | Atlaide atsevišķai vienībai. |
| lineshipdate                   | Rindas nosūtīšanas datums. |
| linedeliverydate               | Rindas piegādes datums. |
| linedeliverymode               | Rindas piegādes veids. |
| linedeliveryaddress            | Rindas piegādes adrese. |
| linepickupdate                 | Debitora norādītais saņemšanas datums pasūtījumiem, kas izmanto piegādes savākšanas režīmu. |
| linepickuptimeslot             | Debitora norādītais saņemšanas datums pasūtījumiem, kas izmanto piegādes savākšanas režīmu. |
| giftcardnumber                 | Dāvanu kartes numurs dāvanu kartes veida precēm. |
| giftcardbalance                | Dāvanu kartes bilance dāvanu kartes veida precēm. |
| giftcardmessage                | Dāvanu kartes ziņojums dāvanu kartes veida precēm. |
| giftcardpin                    | Dāvanu kartes personīgais identifikācijas numurs (PIN) dāvanu kartes veida precēm. (Šis vietturis ir raksturīgs ārējām dāvanu kartēm.) |
| giftcardexpiration             | Dāvanu kartes beigu datums dāvanu kartes veida precēm. (Šis vietturis ir raksturīgs ārējām dāvanu kartēm.) |
| giftcardrecipientname          | Dāvanu kartes saņēmēja vārds dāvanu kartes veida precēm. |
| giftcardbuyername              | Dāvanu kartes pircēja vārds dāvanu kartes veida precēm. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Pasūtījuma rindu vietturu formāts e-pasta ziņojuma pamattekstā

Kad jūs izveidojat HTML atsevišķu pasūtījuma rindu e-pasta ziņojuma pamattekstā, aplieciet atkārtojošos HTML un vietturu bloku rindas ar šādiem vietturiem, kas tiek ievietoti HTML komentāra tagos.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Tālāk ir minēts piemērs.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Izveidot e-pasta saņēmēju veidni

Saņemšanu var nosūtīt debitoriem, kuri veic pirkumus pārdošanas punktā (POS). Kopumā darbības e-pasta saņemšanas veidnes izveidei ir tādas paša, lai izveidotu veidnes citiem darbību notikumiem. Tomēr ir nepieciešamas šādas izmaiņas:

- Kvīts teksts tiek iesprausts e-pasta ziņojumā, izmantojot **%message%** vietturi. Lai nodrošinātu, ka kvīts struktūra ir pareizi izveidota, ietveriet **%message%** vietturi ar HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tagiem.
- Vietturi **%receiptid%** var izmantot, lai parādītu QR kodu vai svītrkodu, kas pārstāv kvīts ID. (QR kodi un svītrkodi tiek dinamiski izveidoti un apkalpoti ar trešās puses pakalpojumu.) Papildinformāciju par to, kā e-pasta kvītī parādīt QR kodu vai svītrkodu, skatiet sadaļā [QR koda vai svītrkoda pievienošana darījumu un kvīts e-pasta ziņojumiem](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>Augšupielādēt e-pasta HTML

Pēc tam, kad esat izveidojis un pārbaudījis HTML jūsu ziņojuma pamattekstam, tas ir jāaugšupielādē Commerce Headquarters. Pašlaik e-pasta HTML nevar eksportēt. Tāpēc jums ir jāsaglabā galvenā kopija jūsu HTML ārpus Commerce Headquarters.

Lai augšupielādētu jaunu vai rediģētu e-pasta veidnes HTML, veiciet šīs darbības.

1. Commerce galvenajā mītnē dodieties uz **Mazumtirdzniecība un tirdzniecība \> Galvenās mītnes iestatījumi \> Organizācijas e-pasta veidnes**.
1. Atlasiet tās valodas rindu, kurai vēlaties pievienot vai aizstāt HTML. Varat arī atlasīt **Jauns**, lai izveidotu rindu jaunai valodai.
1. Atlasiet **Rediģēt**.
1. Parādītajā dialoglodziņā atlasiet **Pārlūkot**. Pārlūkojiet HTML dokumentu, kuru vēlaties augšupielādēt, atlasiet to un pēc tam atlasiet **Atvērt**.
1. Atlasiet **Augšupielādēt**.
1. Kad e-pasta HTML tiek parādīts priekšskatījuma logā, izvēlieties **Labi**.
1. Pārliecinieties ka ir atlasīta **Ir ķermenis** izvēles rūtiņa rindai.

Ja esat jau konfigurējis Commerce Headquarters, lai sūtītu e-pastu, jaunais vai atjauninātais e-pasts tiks nosūtīts visiem debitoriem, kuri veic darbību, un tas, savukārt, izsauc notikumu, kas ir kartēts veidnē.

Papildinformāciju par to, kā konfigurēt e-pasta vēstules Dynamics 365 Commerce, skatiet sadaļā [E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Papildu resursi 

[E-pasta paziņojumu profila iestatīšana](email-notification-profiles.md)

[E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Iestatīt e-pasta saņemšanu](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[E-pasta kvīšu sūtīšana no Modern POS ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
