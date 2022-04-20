---
title: Globalizācijas līdzekļa izveide
description: Šajā tēmā ir paskaidrots, kā izveidot globalizācijas līdzekli.
author: dkalyuzh
ms.date: 02/14/2022
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
ms.openlocfilehash: 94038b0eb412632c348081bbf467f44310d9e955
ms.sourcegitcommit: 6109fc2fe5f407363bb6f240d64b7214657f5914
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/15/2022
ms.locfileid: "8603030"
---
# <a name="create-a-globalization-feature"></a>Globalizācijas līdzekļa izveide

[!include [banner](../includes/banner.md)]

Elektronisko rēķinu izrakstīšanas funkciju var izveidot no nulles vai arī to var balstīt uz esošu līdzekli. Veidojot līdzekli no nulles, manuāli jāpievieno elektronisko pārskatu (ER) konfigurācijas un citi komponenti, piemēram, līdzekļu iestatīšana un detalizēta informācija par lietojumprogrammas iestatīšanu. Veidojot līdzekli, kura pamatā ir esošs līdzeklis, jaunais līdzeklis pārmanto visas bāzes līdzekļa konfigurācijas un parametrus. Varat pārskatīt, kas tiek kopēts no bāzes līdzekļa uz jauno līdzekli.

## <a name="create-a-feature-from-scratch"></a>Līdzekļa izveide no nulles

Šajā sadaļā ir paskaidrots, kā izveidot elektronisko rēķinu izrakstīšanas līdzekli, ja globālajā repozitorijā nav pieejams neviens globalizācijas līdzeklis jūsu biznesa scenārijiem ārpus lodziņa.

Lai izveidotu elektronisko rēķinu izrakstīšanas līdzekli, rīkojieties šādi.

1. Piesakieties savā Regulēšanas konfigurācijas pakalpojuma (RCS) kontā.
2. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Atlasiet **Pievienot** un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Jauns līdzeklis**.
4. Ievadiet elektronisko rēķinu izrakstīšanas līdzekļa nosaukumu un aprakstu.
5. Atlasiet **Izveidot līdzekli**. Jaunā līdzekļa pirmā versija tiek parādīta lapas labajā pusē, un tās statuss **ir Melnraksts**.

    Pēc tam jāpievieno ER konfigurācijas un līdzekļu iestatījumi. Pirms pievienojat jaunas vai esošas ER formāta konfigurācijas, pārliecinieties, vai tās pastāv jūsu lokālajā RCS repozitorijā.

6. Atlasiet elektronisko rēķinu izrakstīšanas līdzekli, ar kuru strādājat.
7. Cilnē **Konfigurācijas** atlasiet **Pievienot**.
8. **Režģī Konfigurācijas atrodiet un atlasiet formāta konfigurācijas, kas nepieciešamas apstrādes konveijeram (piemēram, lai ģenerētu elektroniskos rēķinu failus** vai apstrādātu atbildes no ārējiem tīmekļa pakalpojumiem).
9. Atlasiet **Labi**. Tagad konfigurācijas var izmantot apstrādes konveijera darbībās. Plašāku informāciju skatiet [Work with configurations](e-invoicing-work-configurations.md).
10. Lai pievienotu elektronisko rēķinu izrakstīšanas līdzekļu iestatījumus, izveidojiet to **lapas Jauns līdzekļu** lapas cilnē **Uzstādījumi**. Papildinformāciju skatiet rakstā [Darbs ar līdzekļu iestatījumiem](e-invoicing-feature-setup.md).
11. Pabeidziet iestatīšanu un ievietojiet elektronisko rēķinu izrakstīšanas līdzekli pakalpojuma vidē. Papildinformāciju skatiet rakstā [Globalizācijas līdzekļa](e-invoicing-complete-publish-deploy-globalization-feature.md) pabeigšana, publicēšana un izvietošana.

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Izveidot faila formāta konfigurācijas, kas atvasinātas no esošā rēķinu modeļa

Šo sadaļu var izlaist, ja nav jāizveido ER konfigurācijas, bet kā pamatu var atkārtoti izmantot esošās versijas.

Šī procedūra parāda, kā izveidot faila formāta konfigurācijas, kas nepieciešamas jaunajam elektronisko rēķinu izrakstīšanas līdzeklim, kuru vēlaties izveidot. Izveidojiet elektroniskā rēķina faila formāta konfigurāciju un citas failu formāta konfigurācijas, kas nepieciešamas jaunajam elektronisko rēķinu izrakstīšanas līdzeklim.

1. Piesakieties savā RCS kontā.
2. Darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Atlasiet **rēķina modeli** vai Brazīlijas scenārijiem atlasiet **finanšu modeli**.
4. Atlasiet **Izveidot konfigurāciju** un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Formatēt, pamatojoties uz datu modeļa rēķinu**.
5. Ievadiet pakotnes nosaukumu un aprakstu formāta konfigurācijai.
6. Laukā **Formāta tips** atlasiet datu paplašinājuma tipu.
7. Laukā **Datu modeļa definīcija** atlasiet saknes struktūru, uz kuru kartēt formātu. Piemēram, **InvoiceCustomer** tiek izmantots debitoru rēķinu formātiem.
8. Atlasiet **Izveidot konfigurāciju**.
9. Atlasiet jaunā formāta konfigurāciju.
10. Atlasiet **Veidotājs** un izmantojiet rīku Formātu veidotājs, lai konfigurētu faila izkārtojumu tā, lai tas atbilstu faila formāta specifikācijām.
11. Aizvērt lapu.
12. Cilnē **Versijas** atlasiet **Mainīt statusu** \> **Gatavs**.
13. Atlasiet **Mainīt statusu** \> **Kopīgot**, lai publicētu formāta konfigurāciju globālajā repozitorijā.

Jaunās failu formāta konfigurācijas ir jākopīgo ar Microsoft domēnu, pirms tās var patērēt elektronisko rēķinu izrakstīšanas pakalpojums.

1. Atlasiet formāta konfigurāciju, pie kuras strādājat. Konfigurācijas statusam ir jābūt **Koplietots**.
2. Cilnē **Versijas** atlasiet **Paplašināta kopīgošana** \> **Globālais repozitorijs**.
3. Cilnē **Kopīgots ar** atlasiet **Organizācija**.
4. Laukā **Parametri** ievadiet **microsoft.com**, lai koplietotu formāta konfigurāciju ar Microsoft domēnu.
5. Atlasiet **Labi**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Tāda līdzekļa izveide, kura pamatā ir esošs līdzeklis

1. Piesakieties savā RCS kontā.
2. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Pārliecinieties, vai laukā **Konfigurācijas nodrošinātājs** ir atlasīts aktīvais konfigurācijas nodrošinātājs. Tādējādi jaunais elektronisko rēķinu izrakstīšanas līdzeklis tiks parādīts sarakstā pēc tā izveides. Ja jūsu aktīvais konfigurācijas nodrošinātājs nav atlasīts, jaunais līdzeklis tiks filtrēts no saraksta.
4. Atlasiet **Pievienot** un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Pamatojoties uz esošu versiju**.
5. Ievadiet līdzekļa nosaukumu un aprakstu.
6. Laukā **Bāzes līdzeklis** atlasiet līdzekļa pamatversiju.
7. Atlasiet **Izveidot līdzekli**. Līdzeklis ir izveidots, un tā statuss **ir Melnraksts**.
8. Pārskatiet līdzekļa komponentus, lai noteiktu, vai ir nepieciešami atjauninājumi.

    - Pārskatiet konfigurācijas, ja ir jāpielāgo ER formāti un to saistīšana ar līdzekļu versijas formāta kartējumiem.
    - Pārskatiet iestatījumus, ja līdzekļa versijai ir jāpielāgo **cilne Darbības**, **cilne Piemērojamības kārtulas** vai **Mainīgie**.

9. Pabeidziet iestatīšanu un ievietojiet elektronisko rēķinu izrakstīšanas līdzekli pakalpojuma vidē. Papildinformāciju skatiet rakstā [Globalizācijas līdzekļa](e-invoicing-complete-publish-deploy-globalization-feature.md) pabeigšana, publicēšana un izvietošana.
