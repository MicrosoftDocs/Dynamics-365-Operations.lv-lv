---
title: Pabeigt, publicēt un izvietot globalizācijas līdzekli
description: Šajā tēmā ir sniegta informācija par globalizācijas līdzekļu dzīves ciklu.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a842a3ba31c0a8e0d80ad1856d9d6d861a8514ea
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371941"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Pabeigt, publicēt un izvietot globalizācijas līdzekli

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Elektronisko rēķinu izrakstīšanas funkcionalitātes versijas

Elektronisko rēķinu izrakstīšanas funkcijas ir pieejamas versijās. Veidojot jaunu versiju, versijas numurs tiek automātiski palielināts.

Elektronisko rēķinu izrakstīšanas līdzekļa versijas seko dzīves ciklam, kam var būt trīs statusi:

- **Melnraksts** – kad funkcionalitātes versijai ir šis statuss, ir iespējams rediģēt tās konfigurācijas atribūtus un artefaktus (piemēram, faila formāta konfigurācijas).
- **Pabeigts** — šis statuss norāda, ka līdzekļa versijas rediģēšana pabeigta un tai vairs nevēlaties veikt atjauninājumus. Ja funkcijas versijai ir šis statuss, jūs vairs nevarat to vai nevienu no tās komponentiem rediģēt.
- **Publicēts** - šis statuss norāda, ka funkcijas versija ir publicēta globālajā repozitorijā, kas ir saistīts ar jūsu organizāciju. Ja funkcijas versijai ir šis statuss, jūs vairs nevarat to vai nevienu no tās komponentiem rediģēt.

Jūs variet norādīt **Spēkā stāšanās** datumu jaunai elektronisko rēķinu izrakstīšanas līdzekļa versijai. Šādā veidā varat definēt noklusējuma versiju, ko var izmantot vai ko var pārrakstīt, kad funkcija tiek izvietota pakalpojumu vidē.

Lai mainītu elektronisko rēķinu izrakstīšanas līdzekļa versijas statusu, sekojiet šiem soļiem.

1. Piesakieties savā Regulēšanas konfigurācijas pakalpojuma (RCS) kontā.
2. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Elektronisko rēķinu izrakstīšanas funkciju **lapas kreisajā pusē** izvēlieties elektronisko rēķinu izrakstīšanas līdzekli.
4. **Lapas labajā** pusē cilnē Versijas atlasiet versiju.
5. Atlasiet **Mainīt statusu un** pēc tam atlasiet **Pabeigt**(ja pašreizējais statuss ir **Melnraksts**) vai **Publicēts** (ja pašreizējais statuss ir **Pabeigts**).
6. Ziņojuma lodziņā atlasiet Jā **, lai** apstiprinātu pieprasījumu.

Manuālas izmaiņas no Pilna **statusa** uz Publicēts **statuss** nav obligātas. Elektronisko rēķinu izrakstīšanas līdzekļu versijas automātiski tiek atjauninātas **uz Publicēto** statusu, kad tās tiek izvietotas pakalpojumu vidē.

Cilnes Versijas kolonnā Līdzekļa **versijas statusu var** izsekot **·**.

## <a name="deploy-feature-versions"></a>Izvietot līdzekļu versijas

RcS izmantojiet komandu **Izvietot**, lai publicētu elektronisko rēķinu izrakstīšanas līdzekļa versiju mērķa pakalpojuma vidē vai pievienotajā programmā.

1. Elektronisko rēķinu izrakstīšanas funkciju **lapas kreisajā pusē** izvēlieties elektronisko rēķinu izrakstīšanas līdzekli.
2. **Cilnes Versijas** lapas labajā pusē atlasiet elektronisko rēķinu izrakstīšanas funkcijas versiju, ko vēlaties izvietot pakalpojumu vidē vai pievienotajā programmā. Atlasītās versijas statusam ir jābūt Pabeigts **vai** **Publicēts**.
3. Atlasiet **Izvietot** un pēc tam atlasiet vienu vai abas no šīm opcijām, lai definētu izvietošanas mērķi:

    - **Savienotā** programma - konfigurācija, ko nodrošina programmas iestatījumi, ir rakstīta Microsoft Dynamics 365 Finance Dynamics 365 Supply Chain Management instancē vai iepriekš saistīta ar to.
    - **Pakalpojumu vide** – elektronisko rēķinu izrakstīšanas funkcijas versija tiek izvietota pakalpojumu vidē. Elektronisko rēķinu izrakstīšana ir gatava saņemt un apstrādāt elektroniskos dokumentus, ko sūta Finanšu vai piegādes ķēžu pārvaldība.

> [!NOTE]
> Parasti jūs mainīsiet elektroniskā pārskata (ER) funkcijas parametrus, kas jāizvieto pakalpojumu vidē. Saistītās programmas izmaiņas būs retas. Jaunās versijas ir jāizvieto pievienotajā programmā tikai tad, ja maināt atbilstošos programmas parametrus.

Lai noteiktu, vai noteikta elektronisko rēķinu izrakstīšanas līdzekļa versija ir izvietota specifiskā vidē, pārskatiet informāciju **cilnē** Vides.

## <a name="remove-feature-versions"></a>Noņemt līdzekļu versijas

RcS varat atlasīt Atcelt, lai **noņemtu** noteiktu elektronisko rēķinu izrakstīšanas līdzekļa versiju no pakalpojumu vides, ja tā tika izvietota tur.

> [!IMPORTANT]
> Poga **Atcelt** darbojas tikai pakalpojumu vidēs. Viss nav noņemts no pievienotās lietojumprogrammas pašreizējai elektronisko rēķinu izrakstīšanas funkcijai.

## <a name="rebase-electronic-invoicing-features"></a>Elektronisko rēķinu izrakstīšanas funkciju pārsāšana

Kad viens elektroniskais rēķinu izrakstīšanas līdzeklis ir atvasināts no cita, varat atlasīt Rebase **,** lai atjauninātu atvasināto līdzekli ar izmaiņām, kas veiktas sākotnējā (pamata) funkcionalitātē.

Lai izgūtu izgūtu izveidotā līdzekļa versiju, sekojiet šiem soļiem.

1. Iegūstiet pēdējo funkcijas versiju, importējot to no globālā repozitorija. Papildinformāciju skatiet sadaļā "Importēt līdzekli [no globālā repozitorija"](e-invoicing-import-feature-global-repository.md).
2. Līdzekļu sarakstā atlasiet līdzekli, kas jāpārskata.
3. Lai izveidotu **melnraksta** versiju **·**, cilnē Versijas atlasiet Jauns.
4. Atlasiet **Pārskatīt**.
5. Dialoglodziņā Atkārtota **bāze** atlasiet līdzekli, uz kuru veikt atkārtotu bāzes datu bāzi.
6. Atlasiet **Labi**.
7. Pārskatiet līdzekļa komponentus un veiciet nepieciešamās izmaiņas.
8. Atlasiet **Mainīt statusu**, lai pabeigtu pārskatīto līdzekli. Kad pārskatīšana ir pabeigta, varat veikt papildu darbības.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Iegūstiet noteiktu elektronisko rēķinu izrakstīšanas funkciju versiju

Veidojot jaunu elektronisko rēķinu izrakstīšanas funkcijas versiju, sistēma izveido pēdējās funkcionalitātes versijas kopiju. Lai izmantotu agrāku funkcijas versiju kā pamatu jaunai versijai, atlasiet versiju un pēc tam atlasiet Iegūt **šo versijas komandu**. Tiek izveidota jauna līdzekļa melnraksta versija, kas ir atlasītās versijas kopija.
