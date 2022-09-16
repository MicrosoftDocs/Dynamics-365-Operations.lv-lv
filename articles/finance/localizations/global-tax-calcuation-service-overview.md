---
title: Nodokļu aprēķina pārskats
description: Šis raksts skaidro nodokļu aprēķināšanas iespējas vispārējo tvērumu un funkcijas.
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: a193db82b2b079c1e10fbfb6bfde7aa43b18bc4a
ms.sourcegitcommit: dbb997f252377b8884674edd95e66caf8d817816
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/10/2022
ms.locfileid: "9465171"
---
# <a name="tax-calculation-overview"></a>Nodokļu aprēķina pārskats

[!include [banner](../includes/banner.md)]

Nodokļu aprēķins ir hipermērogojams daudznomnieku pakalpojums, kas ļauj Global Tax Engine automatizēt un vienkāršot nodokļu noteikšanas un aprēķināšanas procesu. Nodokļu programma ir pilnībā konfigurējama. Elementi, kurus var konfigurēt, ietver, bet ne tikai, apliekamo datu modeli, nodokļu kodu, nodokļu piemērošanas matricu un nodokļu aprēķina formulu. Nodokļu programma darbojas pamata pakalpojumu platformā un piedāvā modernu tehnoloģiju un Microsoft Azure eksponenciālu mērogošanu.

Nodokļu aprēķins ir integrēts ar Dynamics 365 Finansēm un Dynamics 365 Supply Chain Management. Visbeidzot tas integrēs arī ar Dynamics 365 Project Operations, Dynamics 365 Commerce un citām pirmās puses un trešās puses programmām.

> [!IMPORTANT]
> Iespējojot nodokļu aprēķinu, atsevišķas operācijas ar saistītajiem datiem var tikt veiktas datu centrā, kurš neuztur jūsu pakalpojuma datus. Pirms nodokļu aprēķina iespējošanas pārskatiet sadaļu [Noteikumi un nosacījumi](https://go.microsoft.com/fwlink/?linkid=2156043). Mums ir svarīga jūsu konfidencialitāte. Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=521839).

Nodokļu aprēķins ir uz mikropakalpojumiem balstīta nodokļu programma, kas piedāvā eksponenciālu mērogojamību un var palīdzēt veikt tālāk minētos uzdevumus.

- Izmantojot uzlabotu noteikšanas mehānismu, automātiski nosaka pareizo PVN grupu, krājumu PVN grupu un nodokļu kodus.
- Atbalsta vairākus nodokļa reģistrācijas numurus vienai juridiskajai personai un automātiski nosaka pareizo nodokļa reģistrācijas numuru ar nodokli apliekamām transakcijām.
- Atbalsta nodokļu noteikšanu, aprēķinu, grāmatošanu un norēķinus pārsūtīšanas pasūtījumiem.
- Definē konfigurējamas nodokļu aprēķina formulas un nosacījumus specifiskām uzņēmējdarbības prasībām.
- Kopīgo nodokļu noteikšanas un aprēķina risinājumu visām juridiskajām personām, lai samazinātu uzturēšanas darba apjomu un izvairītos no kļūdām.
- Atbalsta debitoru un kreditoru nodokļa reģistrācijas numuru noteikšanu.
- Atbalsta saraksta koda noteikšanu.
- Atbalsta nodokļu aprēķina parametrus nodokļu jurisdikcijas līmenī.

Lai izmantotu nodokļu aprēķinu, instalējiet nodokļu aprēķina pievienojumprogrammu savam projektam pakalpojumā Microsoft Dynamics Lifecycle Services (LCS). Pēc tam pabeidziet iestatīšanu pakalpojumā [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) un iespējojiet nodokļu aprēķinu pakalpojumā Finance un Supply Chain Management. Papildinformāciju skatiet sadaļā [Sākt darbu ar nodokļu pakalpojumu](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Pieejamība

Nodokļu aprēķins parasti ir pieejams ražošanas vidē visiem debitoriem, sākot no versijas 10.0.21.

Jaunas funkcijas tiks ieviestas arī turpmāk. Regulāri skatiet visjaunāko izlaišanas plānu, lai uzzinātu par atbalstīto funkciju segumu un darbības jomu.

Nodokļu aprēķins ir izvietots tālāk redzamajās Azure ģeogrāfiskās lapās. Atbilstoši debitoru vajadzībām tiks pievienotas vairākas Azure ģeogrāfiskās vietas.

- Āzijas Klusā okeāna daļa
- Austrālija
- Brazīlija
- Kanāda
- Eiropa
- Francija
- Indija
- Japāna
- Dienvidāfrikas Republika
- Šveice
- Apvienotie Arābu Emirāti
- Apvienotā Karaliste
- Amerikas Savienotās Valstis

> [!NOTE]
> Nodokļu aprēķins neatbalsta agrāku Dynamics 365 versiju, piemēram, Dynamics AX 2012 vai Dynamics 365 lokālu izvietošanu.

## <a name="versions"></a>Versijas
Mēs iesakām jums importēt un iestatīt nodokļu aprēķina konfigurāciju ar versiju, kas atbilst finanšu vai piegādes ķēdes pārvaldības versijai.

| Finanšu vai piegādes ķēdes pārvaldības versija | Nodokļu konfigurācijas versija               |
| --------------- | --------------------------------------- |
| 10.0.30         | Nodokļu aprēķina konfigurācija 40.55.239 |
| 10.0.29         | Nodokļu aprēķina konfigurācija 40.55.236 |
| 10.0.28         | Nodokļu aprēķina konfigurācija 40.54.234 |
| 10.0.27         | Nodokļu aprēķina konfigurācija 40.54.234 |


## <a name="data-flow"></a>Datu plūsmas

Šeit ir datu plūsmas procesa ieskicēšana nodokļu aprēķināšanai. 

1. RCS skatiet un importējiet ar nodokli apliekamā dokumenta modeļa konfigurācijas un modeļa kartēšanas konfigurācijas. Ja paplašināta scenārija gadījumā konfigurācijas ir jāpaplašina, skatiet sadaļu [Datu lauku pievienošana nodokļu konfigurācijās](tax-service-add-data-fields-tax-configurations.md).
2. RCS izveidojiet vai uzturiet nodokļu līdzekļus. Lai uzturētu nodokļu likmes un nodokļu piemērojamības noteikumus, varat izmantot nodokļu līdzekļus.
3. Kad nodokļu līdzekļu iestatīšana ir pabeigta, publicējiet nodokļu konfigurācijas un nodokļu līdzekļus no RCS globālajā repozitorijā.
4. Risinājumā Finance atlasiet, kuru nodokļu līdzekļu iestatīšanas versiju lietot noteiktai juridiskajai personai.
5. Risinājumā Finance un Supply Chain Management veiciet transakcijas kā parasti. Kad nepieciešams nodokļu aprēķins, klients apkopos informāciju no transakcijas, piemēram, pārdošanas pasūtījumu vai pirkšanas pasūtījumu, un iepakos šo informāciju kā vērtumu. Pēc tam tiks nosūtīts pieprasījums nodokļu aprēķinam.
6. Nodokļu aprēķina pieprasījums tiek saņemts no klienta, un aprēķins tiek pabeigts. Pēc tam nodokļu rezultāts tiek nosūtīts atpakaļ klientam.
7. Dynamics 365 klients saņem nodokļu rezultātu un norāda nodokļu aprēķina rezultātu PVN lapā.

## <a name="supported-transactions"></a>Atbalstītie darījumi

Nodokļu aprēķinu var iespējot pēc transakcijām. 

Šajā tabulā uzskaitītas darbības, kas tiek atbalstītas atbilstošajā versijā.

| Versija | Transakcijas |
|---------|--------------|
| 10.0.29 | Periodiskie žurnāli |
| 10.0.28 | Kreditoru maksājumu žurnāls<br> Debitora maksājumu žurnāls | 
| 10.0.26 | Virsgrāmatas žurnāli<br> Kreditoru rēķinu žurnāls |
| 10.0.23 | Brīva teksta rēķins |
| 10.0.21| Pārdošana<br><ul><li>Pārdošanas piedāvājums</li><li>Pārdošanas pasūtījums</li><li>Apstiprināšana</li><li>Izdošanas saraksts</li><li>Pavadzīme</li><li>Pārdošanas rēķins</li><li>Kredīta piezīme</li><li>Atgriešanas pasūtījums</li><li>Virsraksta papildmaksa</li><li>Rindas papildmaksas pieprasījums</li></ul>Pirkšana<br><ul><li>Pirkšanas pasūtījums</li><li>Apstiprināšana</li><li>Saņemšanas saraksts</li><li>Produktu saņemšana</li><li>Pirkšanas rēķins</li><li>Virsraksta papildmaksas pieprasījums</li><li>Rindas papildmaksas pieprasījums</li><li>Kredīta piezīme</li><li>Atgriešanas pasūtījums</li><li>Pirkšanas pieprasījums</li><li>Pirkšanas pieprasījuma rindas papildmaksas pieprasījums</li><li>Piedāvājuma pieprasījums</li><li>Piedāvājuma pieprasījuma virsraksta papildmaksas pieprasījums</li><li>Piedāvājuma pieprasījuma rindas papildmaksas pieprasījums</li></ul>Krājums<ul><li>Pārvietošanas pasūtījums – nosūtīšana</li><li>Pārsūtīšanas pasūtījums – saņemšana</li></ul>|

## <a name="supported-countriesregions"></a>Atbalstītās valstis/reģioni

Nodokļu aprēķinu var palaist ar atbalstītām lokalizācijas funkcijām. Šajā tabulā uzskaitītas valstis/reģioni, kas attiecas uz juridiskas personas primāro adresi.

| Versija | Valsts/reģions |
|---------|----------------|
| 10.0.26 | — Ķīnāā <br>- Čehijas Republika<br>- Spānija |
| 10.0.24 | Meksika |
| 10.0.23 | - Taizeme <br>- Japāna <br>- Malaizija <br>- Singapūra |
| 10.0.22 | - Austrālija<br>- Bahreina <br>- Kanāda<br>- Ēģipte <br>– Honkongas īpašās pārvaldes apgabals (SAR) <br>- Kuveita <br>— Jaunzēlande <br>- Omāna <br>- Katara <br>- Saūda Arābu <br>- Dienvidāfrika <br>- Apvienotie Arābu Emirāti |
| 10.0.21 | - Austrija <br>- Beļģija <br>- Dānija <br>- Igaunija <br>- Somija <br>- Francija <br>- Vācija <br>- Ungārija <br>- Islande <br>- Īrija <br>- Itālija <br>- Latvija <br>- Lietuva <br>- Nīderlande <br>- Norvēģija <br>- Polija <br>- Zviedrija <br>- Šveice <br>- Apvienotā Karaliste <br>- ASV |

Jebkurai valstij/reģionam, ko nav lokalizēts korporācija Microsoft, nodokļu aprēķinu var iespējot un palaist arī ar citiem globāliem līdzekļiem.

## <a name="related-resources"></a>Saistītie resursi

[Darba sākšana ar nodokļu pakalpojumu](./global-get-started-with-tax-calculation-service.md)

[Vairāki PVN reģistrācijas numuri](./emea-multiple-vat-registration-numbers.md)

[Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumam](./tasks/tax-feature-support-for-transfer-order.md)

[Kā veidot paplašinājumu nodokļu pakalpojumā](./tax-service-add-data-fields-tax-integration-by-extension.md)
