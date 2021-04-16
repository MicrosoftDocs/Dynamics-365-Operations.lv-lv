---
title: Biznesa dokumenta veidnes struktūras atjaunināšana
description: Šajā tēmā paskaidrots, kā atjaunināt biznesa dokumenta veidnes struktūru, izmantojot biznesa dokumentu pārvaldības līdzekli.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 203c9f0990051c1618660959dad0e184add68ffa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750488"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Biznesa dokumenta veidnes struktūras atjaunināšana 

[!include[banner](../includes/banner.md)]

Rūtī **Veidnes struktūra**, kas atrodas veidnes redaktorā [Biznesa dokumentu pārvaldība](er-business-document-management.md), varat modificēt biznesa dokumenta veidni, [pievienojot jaunus laukus](er-bdm-add-field-to-excel-template.md) veidnei Microsoft Excel. Tad veidnes struktūra tiek automātiski atjaunināta Dynamics 365 Finance, lai tā atspoguļotu izmaiņas, ko veicāt rūtī **Veidnes struktūra**.

Varat arī modificēt veidni, izmantojot Office 365 tiešsaistes funkcionalitāti. Piemēram, rediģējamajā darblapā varat pievienot jaunu nosauktu krājumu, piemēram, attēlu vai formu. Šādā gadījumā veidnes struktūra netiek automātiski atjaunināta Finance, un pievienotais krājums netiek parādīts rūtī **Veidnes struktūra**. Manuāli atjauniniet veidnes struktūru Finance, veidnes redaktora lapā atlasot **Atjaunināt struktūru**.

Lai iegūtu vairāk informācijas par šo līdzekli, izpildiet tālāk minēto piemēru.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Piemērs: biznesa dokumenta veidnes struktūras atjaunināšana

Šis piemērs parāda, kā sistēmas administrators var atjaunināt biznesa dokumenta veidnes struktūru Finance pēc veidnes modificēšanas Office Online. Turpmākajās sadaļās ir izskaidrotas tam nepieciešamās darbības.

### <a name="prepare-a-business-document-template-for-editing"></a>Biznesa dokumenta veidnes sagatavošana rediģēšanai

Veiciet procedūras, kas norādītas [Biznesa dokumentu pārvaldības pārskatā](er-business-document-management.md).

1. [Konfigurējiet ER parametrus](er-business-document-management.md#configure-er-parameters)
2. [ER risinājumu importēšana](er-business-document-management.md#import-er-solutions)
3. [Biznesa dokumentu pārvaldības iespējošana](er-business-document-management.md#enable-business-document-management)
4. [Konfigurēt parametrus](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Biznesa dokumenta veidnes rediģēšana

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.
2. Lapā **Izveidot jaunu veidni** atlasiet veidni **Brīva teksta rēķins (ER paraugs)(Excel)**.
3. Atlasiet **Izveidot dokumentu**.
4. Laukā **Nosaukums** ievadiet **FTI paraugs Litware**.
5. Atlasiet **Labi**, lai izveidotu jaunu veidni.

    > [!NOTE]
    > Ja vēl neesat pierakstījies Office Online, jūs tiekat [novirzīts uz Office 365 pierakstīšanās lapu](er-business-document-management.md#frequently-asked-questions). Lai atgrieztos savā Finance vidē, pārlūkprogrammā atlasiet pogu **Atpakaļ**.

    Jaunā veidne tiek atvērta rediģēšanai Excel Online iegultajā vadīklā veidnes redaktora lapā.

[![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai sāktu biznesa dokumenta veidnes rediģēšanu](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Pašreizējās rediģējamās veidnes struktūras pārskatīšana

1. Excel Online lentē, kas atrodas cilnē **Skats**, grupā **Rādīt** atlasiet **Režģlīnijas**.
2. Rediģējamajā veidnē atlasiet taisnstūri virs veidnes virsraksta. Šis taisnstūris ir attēls, kura nosaukums ir **rptHeaderCompLogo**.
3. Ja rūts **Veidnes struktūra** ir paslēpta, atlasiet **Rādīt struktūru**.
4. Rūtī **Veidnes struktūra** izvērsiet **Pārskats \> Rēķins \> rptHeader \> rptHeaderPart1**.
5. Ņemiet vērā, ka Finance veidnes struktūrā krājums **rptHeaderCompLogo** tiek parādīts kā pakārtotais krājums **Pārskats \> Rēķins \> rptHeader \> rptHeaderPart1**.

[![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai pārskatītu rediģējamas veidnes pašreizējo struktūru](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Biznesa dokumenta veidnes struktūras atjaunināšana, dzēšot attēlu

1. Excel Online rediģējamajā veidnē atlasiet attēlu **rptHeaderCompLogo**.
2. Izpildiet vienu no norādītajām darbībām, lai dzēstu atlasīto attēlu no rediģējamās veidnes.

    - Atlasiet taustiņu **Dzēst** uz tastatūras.
    - Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) attēlu, un pēc tam atlasiet **Izgriezt**.

    > [!NOTE]
    > Krājums **rptHeaderCompLogo** pašlaik joprojām atrodas Finance veidnes struktūrā, pat ja attēls vairs nav iekļauts Excel veidnē.

3. Atlasiet **Atjaunināt struktūru**, lai sinhronizētu rediģējamās veidnes struktūru Excel un Finance.
4. Rūtī **Veidnes struktūra** izvērsiet **Pārskats \> Rēķins \> rptHeader \> rptHeaderPart1**.
5. Ņemiet vērā, ka krājums **rptHeaderCompLogo** vairs nav iekļauts Finance veidnes struktūrā.

[![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai dzēstu attēlu no biznesa dokumenta veidnes](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Biznesa dokumenta veidnes struktūras atjaunināšana, pievienojot attēlu

1. Excel Online lentē, kas atrodas cilnē **Ievietot**, grupā **Ilustrācijas** atlasiet **Attēls**.
2. Atlasiet **Izvēlēties failu**, atrodiet attēlu, ko vēlaties pievienot, atlasiet to un pēc tam atlasiet **Labi**.
3. Atlasiet **Ievietot**.
4. Pārvietojiet jauno attēlu, līdz tas ir pareizajā vietā. Pēc noklusējuma Excel piešķir nosaukumu attēlam. Piemēram, tas var piešķirt attēlam nosaukumu **Attēls 2**.
5. Atlasiet **Atjaunināt struktūru**, lai sinhronizētu rediģējamās veidnes struktūru Excel un Finance.
6. Rūtī **Veidnes struktūra** izvērsiet **Pārskats \> Rēķins \> rptHeader \> rptHeaderPart1**.
7. Ņemiet vērā, ka jaunais attēls tagad ir iekļauts Finance veidnes struktūrā kā krājums.

[![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai pievienotu attēlu biznesa dokumenta veidnei](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Saistītās saites

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Biznesa dokumentu pārvaldības pārskats](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]