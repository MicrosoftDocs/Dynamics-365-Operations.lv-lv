---
title: Nodokļu aprēķina pārskats
description: Šajā tēmā ir izskaidrots nodokļu aprēķina iespēju vispārējais tvērums un iezīmes.
author: wangchen
ms.date: 03/02/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a02767e4a90fa6b7414c796d66e758afe0501cf5
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388499"
---
# <a name="tax-calculation-overview"></a>Nodokļu aprēķina pārskats

[!include [banner](../includes/banner.md)]

Nodokļu aprēķins ir hipermērogojams daudznomnieku pakalpojums, kas ļauj Global Tax Engine automatizēt un vienkāršot nodokļu noteikšanas un aprēķināšanas procesu. Nodokļu programma ir pilnībā konfigurējama. Elementi, kurus var konfigurēt, ietver, bet ne tikai, apliekamo datu modeli, nodokļu kodu, nodokļu piemērošanas matricu un nodokļu aprēķina formulu. Nodokļu programma darbojas pamata pakalpojumu platformā un piedāvā modernu tehnoloģiju un Microsoft Azure eksponenciālu mērogošanu.

Nodokļu aprēķins ir integrēts ar Dynamics 365 Finance un Dynamics 365 Supply Chain Management. Visbeidzot tas integrēs arī ar Dynamics 365 Project Operations, Dynamics 365 Commerce un citām pirmās puses un trešās puses programmām.

> [!IMPORTANT]
> Iespējojot nodokļu aprēķinu, atsevišķas operācijas ar saistītajiem datiem var tikt veiktas datu centrā, kurš neuztur jūsu pakalpojuma datus. Pirms nodokļu aprēķina iespējošanas pārskatiet sadaļu [Noteikumi un nosacījumi](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md). Mums ir svarīga jūsu konfidencialitāte. Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=521839).

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
- Kanāda
- Eiropa
- Japāna
- Šveice
- Apvienotā Karaliste
- Amerikas Savienotās Valstis

> [!NOTE]
> Nodokļu aprēķins neatbalsta agrāku Dynamics 365 versiju, piemēram, Dynamics AX 2012 vai Dynamics 365 lokālu izvietošanu.

## <a name="versions"></a>Versijas
Mēs iesakām jums importēt un iestatīt nodokļu aprēķina konfigurāciju ar versiju, kas atbilst finanšu vai piegādes ķēdes pārvaldības versijai.

| Finanšu vai piegādes ķēdes pārvaldības versija | Nodokļu konfigurācijas versija               |
| --------------- | --------------------------------------- |
| 10.0.18         | Nodokļu konfigurācija — Eiropa 30.12.82     |
| 10.0.19         | Nodokļu aprēķina konfigurācija 36.38.193 |
| 10.0.20         | Nodokļu aprēķina konfigurācija 40.43.208 |
| 10.0.21         | Nodokļu aprēķina konfigurācija 40.48.215 |
| 10.0.22         | Nodokļu aprēķina konfigurācija 40.48.215 |
| 10.0.23         | Nodokļu aprēķina konfigurācija 40.50.221 |
| 10.0.24         | Nodokļu aprēķina konfigurācija 40.50.225 |
| 10.0.25         | Nodokļu aprēķina konfigurācija 40.50.225 |
| 10.0.26         | Nodokļu aprēķina konfigurācija 40.54.234 |


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

Versijā 10.0.21 tiek atbalstītas tālāk norādītās transakcijas. 

- Pārdošana

    - Pārdošanas piedāvājums
    - Pārdošanas pasūtījums
    - Apstiprināšana
    - Izdošanas saraksts
    - Pavadzīme
    - Pārdošanas rēķins
    - Kredīta piezīme
    - Atgriešanas pasūtījums
    - Virsraksta papildmaksa
    - Rindas papildmaksas pieprasījums

- Pirkšana

    - Pirkšanas pasūtījums
    - Apstiprināšana
    - Saņemšanas saraksts
    - Produktu saņemšana
    - Pirkšanas rēķins
    - Virsraksta papildmaksas pieprasījums
    - Rindas papildmaksas pieprasījums
    - Kredīta piezīme
    - Atgriešanas pasūtījums
    - Pirkšanas pieprasījums
    - Pirkšanas pieprasījuma rindas papildmaksas pieprasījums
    - Piedāvājuma pieprasījums
    - Piedāvājuma pieprasījuma virsraksta papildmaksas pieprasījums
    - Piedāvājuma pieprasījuma rindas papildmaksas pieprasījums

- Krājums

    - Pārvietošanas pasūtījums – nosūtīšana
    - Pārsūtīšanas pasūtījums – saņemšana

Versijā 10.0.23 tiek atbalstītas tālāk norādītās transakcijas. 

- Brīva teksta rēķins

Versijā 10.0.26 tiek atbalstītas tālāk norādītās transakcijas. 

- Virsgrāmatas žurnāli
- Kreditoru rēķinu žurnāls

## <a name="supported-countriesregions"></a>Atbalstītās valstis/reģioni

Nodokļu aprēķinu var iespējot pēc juridiskās personas. 

Versijā 10.0.21 tiek atbalstīti tālāk norādītās juridiskās personas primārās adreses valstis/reģioni.

- Austrija
- Beļģija
- Dānija
- Igaunija
- Somija
- Francija
- Vācija
- Ungārija
- Islande
- Itālija
- Latvija
- Lietuva
- Nīderlande
- Norvēģija
- Polija
- Zviedrija
- Šveice
- Apvienotā Karaliste
- ASV

Versijā 10.0.22 tiek atbalstīti tālāk norādītās juridiskās personas primārās adreses valstis/reģioni.

- Austrālija
- Bahreina
- Kanāda
- Ēģipte
- ĶTR īpašais administratīvais reģions Honkonga
- Kuveita
- Jaunzēlande
- Omāna
- Katara
- Saūda Arābija
- Dienvidāfrika
- Apvienotie Arābu Emirāti

Versijā 10.0.23 tiek atbalstīti tālāk norādītās juridiskās personas primārās adreses valstis/reģioni.

- Taizeme
- Japāna
- Malaizija
- Singapūra

Versijā 10.0.24 tiek atbalstīti tālāk norādītās juridiskās personas primārās adreses valstis/reģioni.

- Meksika

Versijā 10.0.26 tiek atbalstīti tālāk norādītās juridiskās personas primārās adreses valstis/reģioni.

- Ķīna
- Čehijas Republika
- Spānija

## <a name="related-resources"></a>Saistītie resursi

[Darba sākšana ar nodokļu pakalpojumu](./global-get-started-with-tax-calculation-service.md)

[Vairāki PVN reģistrācijas numuri](./emea-multiple-vat-registration-numbers.md)

[Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumam](./tasks/tax-feature-support-for-transfer-order.md)

[Kā veidot paplašinājumu nodokļu pakalpojumā](./tax-service-add-data-fields-tax-integration-by-extension.md)
