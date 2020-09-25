---
title: Izcelsmes valsts/reģions
description: Daudzas organizācijas izsniedz sertifikātus saviem kreditoriem, lai nodrošinātu preču atbilstību noteiktiem sertifikācijas standartiem. Šie sertifikāti bieži ir atkarīgi no izcelsmes valsts/reģiona. Šajā tēmā ir sniegta informācija par izcelsmes valsts/reģiona līdzekli, kas ļauj saistīt preci ar tās izcelsmes valsti/reģionu un sekot tās preču sertifikācijai.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: d0d93a02817bab8e188818862c1bb7f84b498fc1
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802801"
---
# <a name="country-of-origin"></a>Izcelsmes valsts/reģions

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Daudzas organizācijas izsniedz sertifikātus saviem kreditoriem, lai nodrošinātu preču atbilstību noteiktiem sertifikācijas standartiem. Šie sertifikāti bieži ir atkarīgi no izcelsmes valsts/reģiona. Izcelsmes valsts/reģiona līdzeklis ļauj saistīt preci ar tās izcelsmes valsti/reģionu un sekot tās preču sertifikācijai.

## <a name="turn-on-the-country-of-origin-feature"></a>Ieslēgt izcelsmes valsts līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Preču informācijas pārvaldība*
- **Līdzekļa nosaukums:** *Izcelsmes valsts pārvaldības līdzeklis*

## <a name="configure-source-and-destination-countries"></a>Izcelsmes un galamērķa valstu/reģionu konfigurēšana

Pirms izdot preces sertifikātu, prece ir jāsaista ar tās galamērķa valsti un tās izcelsmes valsti/reģionu.

1. Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Izcelsmes valsts/reģions \> Izcelsmes valsts/reģiona noteikumi**.
2. Atlasiet rediģēšanai esošu valsts iestatījumu vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu valsts iestatījumu.
3. Atlasītajai vai jaunajai valstij iestatiet šādas vērtības.

    | Lauks | apraksts |
    |---|---|
    | Krājums | Atlasiet preces krājuma kodu. |
    | Galamērķa valsts | Atlasiet, uz kuru valsti sūtīt preci. |
    | Izcelsmes valsts | Atlasiet, no kuras valsts prece tiek sūtīta. |

Šī iestatījuma nolūks ir palīdzēt ģenerēt materiālu komplekta (MK) pārskatu, kurā var iekļaut izcelsmes valsti katrai daļai, kam ir norādītas izcelsmes un galamērķa valstis. Šis pārskats palīdzēs iegūt visaptverošu priekšstatu par to, no kurienes daļas ir un uz kurieni tās sūta.

## <a name="keep-track-of-vendor-certificates"></a>Kreditora sertifikātu pārraudzīšana

Varat izmantot lapu **Izcelsmes valsts/reģiona kreditoru sertifikāti**, lai sekotu sertifikātiem, ko izsniedzat kreditoriem.

Jums ir jāizlemj, kurus sertifikātu dokumentus jūs izsniedzat un kā par tiem paziņosit klientiem. Šis līdzeklis palīdz sekot līdzi jūsu sertifikātiem. Tas arī ļauj izvēlēties, vai attiecīgie sertifikātu numuri ir redzami rēķinos, pavadzīmēs un/vai pasūtījumu apstiprinājumos.

Lai iestatītu sertifikāta informāciju, veiciet tālāk norādītās darbības.

1. Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Izcelsmes valsts/reģions \> Izcelsmes valsts/reģiona kreditora sertifikāti**.
2. Atlasiet rediģēšanai esošu sertifikāta iestatījumu vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu sertifikāta iestatījumu.
3. Atlasītajam vai jaunajam sertifikātam iestatiet šādus iestatījumus.

    | Lauks | apraksts |
    |---|---|
    | Kreditora konts | Atlasiet kreditoru, kuram sertifikāts izsniegts. |
    | Krājums | Atlasiet krājumu, kuram sertifikāts izsniegts. |
    | Valsts/reģions | Galamērķa valsts vai reģions, kurā jāizmanto šis sertifikāts. |
    | Sertifikāta numurs | Ievadiet izsniegtā sertifikāta identifikācijas numuru. |
    | Spēkā esošs | Atlasiet pirmo datumu, kad pašreizējais sertifikāts ir derīgs.|
    | Termiņa beigas | Atlasiet pēdējo datumu, kad pašreizējais sertifikāts ir derīgs. |
    | Drukāt rēķinā | Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru rēķinos, kas norādītajā datumu diapazonā ir adresēti norādītajai valstij. |
    | Drukāt pavadzīmē | Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru pavadzīmēs, kas norādītajā datumu diapazonā ir adresētas norādītajai valstij. |
    | Drukāt pārdošanas pasūtījumā | Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru pārdošanas pasūtījumos, kas norādītajā datumu diapazonā ir adresēti norādītajai valstij. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Izcelsmes valsts/reģiona iekļaušana MK pārskatos

Ģenerējot MK pārskatu, varat iekļaut izcelsmes valsti katrai daļai, kam norādījāt izcelsmes un galamērķa valstis, lapā **Izcelsmes valsts noteikumi**.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet vai izveidojiet preci, lai atvērtu tās lapu **Izlaisto preču detalizēta informācija**.
1. Darbību rūts cilnē **Inženieris**, grupā **MK** atlasiet **Noformētājs**.
1. Parādītās lapas darbību rūtī atlasiet **MK \> Drukāt**.
1. Dialoglodziņā **Materiālu komplektu rindas** iestatiet lauku **Galamērķa valsts** uz galamērķa valsti, kuru vēlaties skatīt savā pārskatā.
1. Atlasiet **Labi**.

Tiek ģenerēts un parādīts pārskats, kas parāda informāciju par katras daļas izcelsmes valsti/reģion. Tālāk ir sniegts pārskata piemērs.

![Izcelsmes valsts/reģiona pārskats](media/country-of-origin-report.png "Izcelsmes valsts/reģiona pārskats")
