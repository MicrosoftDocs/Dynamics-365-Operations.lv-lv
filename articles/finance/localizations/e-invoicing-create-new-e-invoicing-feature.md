---
title: Elektronisko rēķinu izrakstīšanas funkcijas izveidošana
description: Šajā tēmā skaidrots, kā izveidot jaunu elektronisko rēķinu izrakstīšanas līdzekli, ja jūsu valstij vai reģionam ārpus lodziņa nav pieejams konfigurējams līdzeklis.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744939"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Elektronisko rēķinu izrakstīšanas funkcijas izveidošana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā izveidot jaunu elektronisko rēķinu izrakstīšanas līdzekli, ja jūsu valstij vai reģionam ārpus lodziņa nav pieejams konfigurējams līdzeklis.

Veiciet šīs darbības, lai izveidotu jaunu elektronisko rēķinu izrakstīšanas līdzekli:

1. Izveidojiet jaunu faila formāta konfigurāciju, izmantojot nodrošināto rēķina modeļa konfigurāciju un izmantojot esoša rēķina kartēšanas priekšrocības līdzeklim, kuru vēlaties izveidot.
2. Pievienojiet faila formāta elektronisko rēķinu izrakstīšanas līdzekļa konfigurācijām.
3. Elektronisko rēķinu izrakstīšanas funkcijas iestatījumu izveidošana.
4. Pabeidziet jauno elektronisko rēķinu izrakstīšanas līdzekli un publicējiet to jūsu organizācijas globālajā repozitorijā.
5. Elektroniskās rēķinu izrakstīšanas līdzekļa izvietošana pakalpojuma vidē.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Izveidot jaunas failu formātu konfigurācijas, kas iegūtas no esošā rēķina modeļa

Šajā procedūrā izveidosit faila formāta konfigurācijas, kas nepieciešamas jaunajam elektronisko rēķinu izrakstīšanas līdzeklim, ko vēlaties izveidot. Varat izveidot elektroniskā rēķina faila formāta konfigurāciju un jebkuras citas failu formāta konfigurācijas, kuras var būt nepieciešamas jūsu jaunajai elektronisko rēķinu izrakstīšanas funkcijai.

Pirms sākat šo procedūru, piesakieties savā Regulatory Configuration Service (RCS) kontā.

1. Microsoft Dynamics 365 Finance darbvietā **Elektroniskie pārskati** atlasiet **Repozitoriji** **Microsoft** konfigurācijas nodrošinātājam.
2. Atlasiet **Globāli**, atlasiet **Atvērt** un pēc tam kreisajā rūtī atlasiet **Rēķina modeļa** konfigurāciju.

    > [!IMPORTANT]
    > Brazīlijai tā vietā atlasiet **Finanšu dokumentu** modeļa konfigurāciju.

3. Cilnē **Konfigurācijas** atlasiet **Importēt**.
4. Aizvērt lapu.
5. Aizvērt lapu.
6. Atlasiet elementu **Pārskatu konfigurācijas** un pēc tam atlasiet importēto rēķina modeli.
7. Atlasiet **Izveidot konfigurāciju** un pēc tam atlasiet **Formāts, pamatojoties uz rēķina konteksta modeli**.
8. Ievadiet pakotnes nosaukumu un aprakstu formāta konfigurācijai.
9. Laukā **Formāta tips** atlasiet datu paplašinājuma tipu.
10. Atlasiet **Izveidot konfigurāciju**, tad atlasiet izveidoto konfigurācijas formātu.
11. Atlasiet **Veidotājs** un izmantojiet rīku Formātu veidotājs, lai konfigurētu faila izkārtojumu tā, lai tas atbilstu faila formāta specifikācijām.
12. Aizvērt lapu.
13. Cilnē **Versijas** atlasiet **Mainīt statusu** \> **Gatavs**.
14. Atlasiet **Mainīt statusu** \> **Kopīgot**, lai publicētu formāta konfigurāciju globālajā repozitorijā.

Lai elektronisko rēķinu izrakstīšanas pakalpojums varētu patērēt šo konfigurāciju, jaunā faila formāta konfigurācija ir jākopīgo ar Microsoft domēnu.

1. Atlasiet formāta konfigurāciju, pie kuras strādājat. Konfigurācijas statusam ir jābūt **Koplietots**.
2. Cilnē **Versijas** atlasiet **Paplašināta kopīgošana** \> **Globālais repozitorijs**.
3. Cilnē **Kopīgots ar** atlasiet **Organizācija**.
4. Laukā **Parametri** ievadiet **Microsoft.com**, lai kopīgotu formāta konfigurāciju ar Microsoft domēnu.
5. Atlasiet **Labi**.

## <a name="create-the-new-electronic-invoicing-feature"></a>Elektronisko rēķinu izrakstīšanas funkcijas izveidošana

1. RCS darbvietā **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
2. Atlasiet **Pievienot** un pēc tam atlasiet **Jauna funkcija**.
3. Atlasiet elektronisko rēķinu izrakstīšanas līdzekļa nosaukumu un aprakstu.
4. Atlasiet **Izveidot līdzekli**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Elektronisko rēķinu izrakstīšanas līdzekļa konfigurāciju pievienošana

1. Atlasiet jūsu izveidoto elektronisko rēķinu izrakstīšanas līdzekli, ar kuru strādājat.
2. Cilnē **Konfigurācijas** atlasiet **Pievienot**.
3. Režģī **Konfigurācijas** pārlūkojiet un atlasiet faila formāta konfigurācijas, kas nepieciešamas jūsu elektronisko rēķinu izrakstīšanas funkcijai, lai izveidotu elektroniskā rēķina failu.
4. Atlasiet **Labi**.

## <a name="add-electronic-invoicing-feature-setups"></a>Elektronisko rēķinu izrakstīšanas līdzekļa iestatījumu pievienošana

1. Cilnē **Iestatījumi** atlasiet **Pievienot** un pēc tam atlasiet **Pielāgoti iestatījumi**.
2. Ievadiet līdzekļa iestatījuma nosaukumu un aprakstu.
3. Laukā **Iestatīšanas tips** atlasiet **Apstrādes konveijers**.
4. Atlasiet **Izveidot**.
5. Atlasiet iestatījumu, ar ko strādājat, un pēc tam izvēlieties **Rediģēt**.
6. Cilnē **Konveijera apstrāde** atlasiet **Jauns**, lai pievienotu konveijera darbību. Papildinformāciju par konveijeriem skatiet sadaļā [Darbības](e-invoicing-configuration-rcs.md#actions).
7. Cilnē **Piemērojamības kārtulas** atlasiet **Jauns**, lai pievienotu kārtulu noteikumus. Papildinformāciju par piemērojamības kārtulām skatiet sadaļā [Piemērojamības kārtulas](e-invoicing-configuration-rcs.md#applicability-rules).
8. Lai pievienotu mainīgos pēc vajadzības, cilnē **Mainīgie** atlasiet **Jauns**.
9. Atlasiet **Saglabāt** un pēc tam atlasiet **Pārbaudīt**, lai pārbaudītu konfigurācijas konsekvenci.
10. Aizvērt lapu.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Elektroniskās rēķinu izrakstīšanas līdzekļa izvietošana pakalpojuma vidē

Informāciju par to, kā pabeigt šo uzdevumu, skatiet [Elektronisko rēķinu izrakstīšanas līdzekļa izvietošana pakalpojumu vidē](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Elektroniskās rēķinu izrakstīšanas līdzekļa izvietošana saistītajā programmā

Informāciju par to, kā pabeigt šo uzdevumu, skatiet [Programmu iestatījumu konfigurēšana](e-invoicing-get-started.md#configure-the-application-setup) un [Elektronisko rēķinu izrakstīšanas līdzekļa izvietošana lietojumprogrammā Connected](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
