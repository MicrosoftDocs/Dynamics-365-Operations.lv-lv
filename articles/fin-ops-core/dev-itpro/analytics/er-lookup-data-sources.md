---
title: Uzmeklēšanas datu avotu konfigurēšana, lai izmantotu elektronisko pārskatu programmai raksturīgos parametrus
description: Šajā rakstā skaidrots, kā var konfigurēt Uzmeklēšanas datu avotus Elektronisko pārskatu (ER) formātos, lai izmantotu ER programmai raksturīgos parametrus.
author: kfend
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
ms.openlocfilehash: f3ce5837b1d20860588848a1b518b3d801a05db4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285127"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Uzmeklēšanas datu avotu konfigurēšana, lai izmantotu elektronisko pārskatu programmai raksturīgos parametrus 

[!include[banner](../includes/banner.md)]

Programmai raksturīgo parametru līdzeklis [Elektronisko pārskatu veidošana (ER)](general-electronic-reporting.md) ļauj konfigurēt datu filtrēšanu ER formātā, lai tā būtu balstīta uz abstraktu kārtulu kopu. Šo kārtulu kopu var konfigurēt, lai izmantotu **Uzmeklēšanas** veida informācijas avotu, kas ir pieejams ER formātā. Pēc tam var noteikt reālās kārtulas ārpus ER komponentu izstrādātājiem, izmantojot lietotāja interfeisu (UI), kas tiek ģenerēts automātiski, pamatojoties uz atbilstošā ER formāta **Uzmeklēšanas** datu avota iestatījumiem un pašreizējo juridisko personu datiem. Visbeidzot norādītajām kātulām piekļus ER formāta **Uzmeklēšanas** datu avots, kad tiks izpildīts šis ER formāts.

> [!NOTE]
> Izmantojiet rediģējama ER formāta konfigurētos datu avotus, lai norādītu, kādi programmas dati tiek izmantoti, lai konfigurētu reālās kārtulas.

Izmantojiet [ER operāciju veidotāju](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base), lai **Uzmeklēšanas** veida datu avotu novietotu savā ER formātā. Datu avotam jābūt konfigurētam tā, lai aprakstītu jūsu abstrakto kārtulu izskatu, tostarp:

   - Noteikta datu veida parametru kopa, kuras vērtība ir norādīta, lai norādītu vienu kārtulu.
   - Noteikta datu veida vērtības vaids, ko atgriež viena kārtula, ja šī kārtula citu starpā tiek uzskatīta par piemērotāko.

Jūs varat konfigurēt sekojošos **Uzmeklēšanas** datu avotu veidus atkarībā no vērtības veida, ko atgrieza jebkura konfigurētā kārtula:

   - Izmantojiet **Datu modeļa\Uzmeklēšanas** veidu, ja ir jāatgriež modeļa uzskaitījuma vērtība.
   - Izmantojiet **Dynamics 365 operāciju\uzmeklēšanas** veidu, ja ir jāatgriež programmas uzskaitījuma vērtība vai programmas [paplašinātā datu veida](../extensibility/extensible-edts.md) vērtība.
   - Izmantojiet **Formatēt skaitīšanas\Uzmeklēšanas** veidu, ja ir jāatgriež formata uzskaitījuma vērtība.

Šajā attēlā parādīts, kā formāta uzskaitījumu var konfigurēt ER parauga formātā.

   ![Formāta uzskaitījuma rādīšana kā konfigurētā uzmeklēšanas datu avota pamats.](./media/er-lookup-data-sources-img1.gif)

Šajā attēlā parādīti formāta komponenti, kas ir konfigurēti, lai ziņotu par dažādiem nodokļu veidiem citā ģenerētā pārskata sadaļā.

   ![Parāda formāta sadaļas, lai atsevišķi ziņotu dažādus nodokļu veidus.](./media/er-lookup-data-sources-img2.png)

Šajā attēlā parādīts, kā ER operāciju veidotājs atļauj pievienot **Formāta uzskaitījuma\Uzmeklēšanas** veida datu avotu.  Pievienotais datu avots tiek konfigurēts kā atgrieza vērtību no `List of taxation levels` formāta uzskaitījuma.

   ![Pievienot ER datu avotu formātu uzskaitījuma\uzmeklēšanas veidam.](./media/er-lookup-data-sources-img3.gif)

Šajā attēlā parādīts, kā pievienotais datu avots ir konfigurēts, lai izmantotu datu avota **Modelis** ierakstu saraksta **Modelis.Dati.Nodoklis** lauku **Kods** kā parametru, kas jānorāda katrai konfigurētajai kārtulai.

![Notiek formāta uzskaitījuma\uzmeklēšanas veida pievienoto datu avota parametru konfigurēšana.](./media/er-lookup-data-sources-img4.gif)

Pievienotais `Model.Data.Tax` datu avots ir konfigurēts, lai norādītu nodokļu kodu katram konfigurētai kārtulai, piekļūstot pieteikuma tabulas **NodokļuTabula** ierakstiem.

   ![Formāta uzskaitījuma\uzmeklēšanas vaida viena uzņēmuma uzmeklēšanas datu avota pārskatīšana.](./media/er-lookup-data-sources-img5.gif)

Varat iestatīt meklēšanas kārtulas atlasītajam ER formātam, izmantojot UI, kas ir automātiski saskaņots ar konfigurētā datu avota struktūru. Pašreiz šim UI ir nepieciešams, lai katrai kārtulai norādītu atgriezto vērtību kā `List of taxation levels` formāta uzskaitījuma vērtību, kā arī nodokļu kodu kā parametru.

   ![Iestatīt konfigurētā datu avota kārtulas.](./media/er-lookup-data-sources-img6.gif)

Šajā attēlā parādīts, kā **Aprēķinātā lauka** veida `Model.Data.Summary.LevelByLookup` datu avotu var konfigurēt, lai izsauktu konfigurēto **Uzmeklēšanas** datu avotu, kas sniedz nepieciešamos parametrus. Lai apstrādātu šo izsaukumu izpildlaikā, ER iziet cauri konfigurēto kārtulu sarakstam definētajā secībā, lai atrastu pirmo kārtulu, kas atbilst norādītajiem nosacījumiem. Šajā piemērā tā ir kārtula, kas satur nodokļu kodu, kas atbilst norādītajam. Rezultātā tiek atrasta vispiemērotākā kārtula un šis datu avots atgriež atrastajai kārtulai konfigurēto uzskaitījuma vērtību.

> [!NOTE]
> Ja nav atrasta neviena piemērojamā kārtula, rodas izņēmums. Lai novērstu šos izņēmumus, kārtulu saraksta beigās konfigurējiet papildu kārtulas, lai apstrādātu gadījumus, kad ir norādīta nekonfigurēta vērtība vai arī vērtība nav sniegta. Izmantojiet atbilstīgi opcijas **\*Nav tukšs**\* un **\*Tukšs**\*.  
>
> ![Pievienot datu avotu, lai izsauktu konfigurēto uzmeklēšanas datu avotu.](./media/er-lookup-data-sources-img7.png)

Iestatot opciju **Starpuzņēmums** kā **Jā** rediģējamam uzmeklēšanas datu avotam, šai datu avota parametru kopai tiek pievienots jauns nepieciešamais parametrs **Uzņēmums**. Parametra **Uzņēmums** vērtība ir jānorāda izpildlaikā, kad tiek izsaukts uzmeklēšanas datu avots. Ja uzņēmuma kods ir norādīts izpildlaikā, šim uzņēmumam konfigurētās kārtulas tiek izmantotas, lai atrastu piemērotāko kārtulu, un atbilstošā vērtība tiek atgriezta. Šajā attēlā parādīts, kā to var izdarīt un kā tiek mainīta rediģējama datu avota parametru kopa.

   ![Formāta uzskaitījuma\uzmeklēšanas veida starpuzņēmuma uzmeklēšanas datu avota pārskatīšana.](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Atlasiet katru uzņēmumu atsevišķi, lai konfigurētu kārtulu kopu šim uzmeklēšanas datu avotam rediģējamā ER formātā. Izpildlaikā rodas izņēmums, ja starpuzņēmuma uzmeklēšana tiek izsaukta ar tā uzņēmuma kodu, kura uzmeklēšanas iestatījums netika pabeigts.
>
> Pārliecinieties, ka jūs piešķirat atļaujas lietotājam, kurš darbina ER formātu ar starpuzņēmuma **Uzmeklēšanas** datu avotu, lai piekļūtu katra uzņēmuma datiem, kas ir šī datu avota tvērumā. Pretējā gadījumā izpildlaikā tiek izmests izņēmums.

Sākot ar versiju 10.0.19, ir pieejamas **Uzmeklēšanas** datu avotu paplašinātās iespējas. Kad rediģējamajam uzmeklēšanas datu avotam iestatāt opciju **Paplašināts** uz **Jā**, konfigurētais uzmeklēšanas datu avots tiek pārvērsts par strukturēto datu avotu, kas piedāvā papildu iespējas analizēt konfigurēto kārtulu kopu. Šajā attēlā parādīta šī transformācija.

   ![Formāta uzskaitījuma\uzmeklēšanas veida strukturētā uzmeklēšanas datu avota pārskatīšana.](./media/er-lookup-data-sources-img9.gif)

- Apakškrājums **Uzmeklēšana** ir veidots kā funkcija, kas atrod atbilstošāko kārtulu no konfigurējamo kārtulu kopas, pamatojoties uz sniegto parametru kopu.
- Apakškrājums **IrUzmeklēšanasRezultātuKopa** ir veidota kā funkcija, lai pieņemtu pamata uzskaitījuma datu avota sniegto vērtību un atgrieztu *Būla* vērtību **Patiess**, kad kārtulu kopa satur vismaz vienu kārtulu, kurai sniegtā uzskaitījuma vērtība tika konfigurēta kā atgriezta vērtība. Šī funkcija atgriež *Būla* vērtību **Aplams**, ja nav nevienas kārtulas, kas konfigurēta, lai atgrieztu šo uzskaitījuma vērtību.
- Apakškrājums **Iestatījums** ir veidots kā funkcija, kas atgriež konfigurēto kārtulu kopu kā ierakstu saraksta ierakstus. Konfigurēto kārtulu atgrieztās vērtības un parametru kopa ir uzrādīta katrā atgrieztajā ierakstā kā attiecīgo datu vaidu lauki:

    - Atgrieztā vērtība tiek uzrādīta kā lauks **Uzmeklēšanas rezultāts**.
    - Konfigurētie parametri ir norādīti kā lauki ar parametru nosaukumiem (**Kods** lauks šajā piemērā).

Papildinformāciju par to, kā konfigurēt **Uzmeklēšanas** datu avotu, skatiet sadaļā [ER formātu konfigurēšana parametru izmantošanai, kas norādīti katrai juridiskajai personai](er-app-specific-parameters-configure-format.md). Lai uzzinātu, kā iestatīt Uzmeklēšanas kārtulas, skatiet sadaļu [ER formāta parametru iestatīšana juridiskajai personai](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu formātu konfigurēšana, lai izmantotu parametrus, kas ir norādīti par juridisko personu](er-app-specific-parameters-configure-format.md)

[Elektronisko pārskatu formāta parametru iestatīšana juridiskai personai](er-app-specific-parameters-set-up.md)
