---
title: Izveidot globalizācijas līdzekli
description: Šajā rakstā skaidrots, kā izveidot globalizācijas līdzekli.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5432de8f8a70a4e6a0facd546083b37fd8690556
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283181"
---
# <a name="create-a-globalization-feature"></a>Izveidot globalizācijas līdzekli

[!include [banner](../includes/banner.md)]

Jūs varat izveidot elektronisko rēķinu izrakstīšanas līdzekli no jauna vai arī varat balstīt to uz esošo funkciju. Ja veidojat funkciju no jauna, manuāli jāpievieno elektronisko pārskatu (ER) konfigurācijas un citi komponenti, piemēram, līdzekļu iestatīšanas un programmas iestatīšanas detaļas. Veidojot līdzekli, kas ir balstīts uz esošu līdzekli, jaunā funkcija manto visas pamata funkcionalitātes konfigurācijas un parametrus. Varat pārskatīt, kas ir kopēts no pamatlīdzekļa jaunajā līdzeklī.

## <a name="create-a-feature-from-scratch"></a>Līdzekļu izveide no jauna

Šajā sadaļā skaidrots, kā izveidot elektronisko rēķinu izrakstīšanas līdzekli, ja jūsu biznesa scenārijos globālajā repozitorijā nav pieejama neviena globalizācijas funkcija.

Lai izveidotu elektronisko rēķinu izrakstīšanas līdzekli, veiciet šos soļus.

1. Piesakieties savā Regulēšanas konfigurācijas pakalpojuma (RCS) kontā.
2. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. **Atlasiet** Pievienot un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Jauna** funkcija.
4. Ievadiet nosaukumu un aprakstu elektronisko rēķinu izrakstīšanas līdzeklim.
5. Atlasiet **Izveidot līdzekli**. Pirmā jaunās funkcijas versija parādās lapas labajā pusē un tai ir statuss **Melnraksts**.

    Pēc tam ir jāpievieno ER konfigurācijas un līdzekļu iestatījumi. Pirms pievienojat jaunas vai esošas ER formāta konfigurācijas, pārliecinieties, ka tās ir vietējā RCS repozitorijā.

6. Atlasiet elektronisko rēķinu izrakstīšanas līdzekli, pie kura strādājat.
7. Cilnē **Konfigurācijas** atlasiet **Pievienot**.
8. **Konfigurāciju režģī pārlūkojiet un atlasiet formātu konfigurācijas, kas nepieciešamas** konveijera apstrādei (piemēram, lai izveidotu elektronisko rēķinu failus vai apstrādātu atbildes no ārējiem tīmekļa pakalpojumiem).
9. Atlasiet **Labi**. Konfigurācijas tagad var izmantot apstrādes konveijera darbībās. Papildinformāciju skatiet sadaļā [Darbs ar konfigurācijām](e-invoicing-work-configurations.md).
10. Lai pievienotu elektronisko rēķinu izrakstīšanas funkcijas iestatījumu, izveidojiet to **cilnes** Iestatījumi lapā **Jauna** funkcija. Papildinformāciju skatiet sadaļā [Darbs ar līdzekļu iestatījumiem](e-invoicing-feature-setup.md).
11. Pabeidziet iestatīšanu un izvietojiet elektronisko rēķinu izrakstīšanas līdzekli pakalpojumu vidē. Papildinformāciju skatiet šeit: [Pabeigt, publicēt un izvietot globalizācijas līdzekli](e-invoicing-complete-publish-deploy-globalization-feature.md).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Izveidot failu formātu konfigurācijas, kas ir atvasinātas no esošā rēķina modeļa

Šo sadaļu varat izlaist, ja nav jāveido ER konfigurācijas, bet esošās versijas var izmantot atkārtoti kā pamatu.

Šī procedūra parāda, kā izveidot faila formāta konfigurācijas, kas nepieciešamas jaunajam elektronisko rēķinu izrakstīšanas līdzeklim, ko vēlaties izveidot. Izveidojiet elektroniskā rēķina faila formāta konfigurāciju un jebkuras citas failu formāta konfigurācijas, kas nepieciešamas jūsu jaunajam elektroniskā rēķina izrakstīšanas līdzeklim.

1. Piesakieties savā RCS kontā.
2. Darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Atlasiet rēķina **modeli vai** Brazīlijas scenārijiem atlasiet finanšu **modeli**.
4. Atlasiet **Konfigurāciju un** pēc tam nolaižamajā dialoglodziņā atlasiet opciju Formāts, **pamatojoties uz datu modeļa rēķinu**.
5. Ievadiet pakotnes nosaukumu un aprakstu formāta konfigurācijai.
6. Laukā **Formāta tips** atlasiet datu paplašinājuma tipu.
7. Laukā **Datu modeļa** definīcija atlasiet saknes struktūru, uz kuru kartēt formātu. Piemēram, **InvoiceCustomer** tiek izmantots debitora rēķina formātiem.
8. Atlasiet **Izveidot konfigurāciju**.
9. Izvēlieties jaunu formāta konfigurāciju.
10. Atlasiet **Veidotājs** un izmantojiet rīku Formātu veidotājs, lai konfigurētu faila izkārtojumu tā, lai tas atbilstu faila formāta specifikācijām.
11. Aizvērt lapu.
12. Cilnē **Versijas** atlasiet **Mainīt statusu** \> **Gatavs**.
13. Atlasiet **Mainīt statusu** \> **Kopīgot**, lai publicētu formāta konfigurāciju globālajā repozitorijā.

Pirms elektronisko rēķinu izrakstīšanas pakalpojums tās var lietot, jaunās failu formāta konfigurācijas ir jā koplietotas ar Microsoft domēnu.

1. Atlasiet formāta konfigurāciju, pie kuras strādājat. Konfigurācijas statusam ir jābūt **Koplietots**.
2. Cilnē **Versijas** atlasiet **Paplašināta kopīgošana** \> **Globālais repozitorijs**.
3. Cilnē **Kopīgots ar** atlasiet **Organizācija**.
4. Laukā **Parametri** ievadiet vērtību **microsoft.com** lai kopīgotu formāta konfigurāciju ar Microsoft domēnu.
5. Atlasiet **Labi**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Izveidot līdzekli, kas ir balstīts uz esošu līdzekli

1. Piesakieties savā RCS kontā.
2. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Laukā **Konfigurācijas nodrošinātājs** pārliecinieties, vai ir atlasīts aktīvs konfigurācijas nodrošinātājs. Šādā veidā jaunais elektronisko rēķinu izrakstīšanas līdzeklis tiks parādīts sarakstā pēc tās izveides. Ja nav atlasīts aktīvais konfigurācijas nodrošinātājs, jaunā funkcija tiks filtrēta ārpus saraksta.
4. Atlasiet **Pievienot** un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Pamatojoties uz esošu versiju**.
5. Ievadiet līdzekļa nosaukumu un aprakstu.
6. Laukā **Bāzes** funkcija atlasiet funkcijas pamat versiju.
7. Atlasiet **Izveidot līdzekli**. Šī funkcija ir izveidota un tai ir statuss **Melnraksts**.
8. Pārskatiet līdzekļa komponentus, lai noteiktu, vai ir nepieciešami atjauninājumi.

    - Pārskatiet konfigurācijas gadījumā, ja ir jāpielāgo ER formāti un to saistīšana ar funkcionalitātes versijas formāta kartēšanu.
    - Pārskatiet iestatījumu, ja līdzekļa versijai **ir** **jāpielāgo** cilne Darbības, Cilne **Piemērojamības noteikumi** vai Mainīgie.

9. Pabeidziet iestatīšanu un izvietojiet elektronisko rēķinu izrakstīšanas līdzekli pakalpojumu vidē. Papildinformāciju skatiet šeit: [Pabeigt, publicēt un izvietot globalizācijas līdzekli](e-invoicing-complete-publish-deploy-globalization-feature.md).
