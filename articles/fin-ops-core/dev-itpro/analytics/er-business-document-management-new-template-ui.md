---
title: Microsoft Office-stila lietotāja interfeiss biznesa dokumentu pārvaldībā
description: Šajā tēmā ir paskaidrots, kā izmantot jauno lietotāja interfeisu (UI) elektroniskā pārskata (ER) struktūras biznesa dokumentu pārvaldības līdzeklī.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881040"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office-stila lietotāja interfeiss biznesa dokumentu pārvaldībā

[!include [banner](../includes/banner.md)]

Biznesa dokumentu pārvaldība ļauj biznesa lietotājiem rediģēt biznesa dokumentu veidnes, izmantojot pakalpojumu Microsoft 365 vai atbilstošu Microsoft Office darbvirsmas lietojumprogrammu. Rediģējumi var ietvert dizaina izmaiņas vai jaunas izvietošanas, vai arī lietotāji var pievienot vietturus, lai iekļautu papildu datus, nemainot pirmkodu. Papildinformāciju par to, kā strādāt ar biznesa dokumentu pārvaldību, skatiet [Biznesa dokumentu pārvaldības pārskatā](er-business-document-management.md).

Jaunais lietotāja interfeiss (UI) ir saprotamāks un ērtāk lietojams. **Biznesa dokumenta** apgabals parāda tikai tās veidnes, kas ir pieejamas pašreizējam nodrošinātājam. Iepriekšējā UI cilnē **Veidne** ir uzskaitītas visas veidnes, kas bija pieejamas visiem nodrošinātājiem. Tas arī parāda visas veidnes, ko izveidoja un laboja jebkurš lietotājs, kuram bija vienāda loma.

Var izmantot pogu **Jauns dokuments**, lai izveidotu un rediģētu veidni elektroniskā pārskata (ER) formāta konfigurācijā, kas pieder citam nodrošinātājam. Šīs tēmas piemērā nodrošinātājs ir Microsoft. Alternatīvi veidni var izveidot, augšupielādējot savu veidni Excel formātā.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

Video [Izveidot jaunu biznesa dokumentu, izmantojot biznesa dokumentu pārvaldību](https://youtu.be/gAIYl-mM_pw) (parādīts iepriekš) ir iekļauts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas ir pieejams YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Nodrošināt jauno dokumentu lietotāja interfeisa pieejamību biznesa dokumentu pārvaldībā

Lai biznesa dokumentu pārvaldībā sāktu izmantot jauno dokumentu lietotāja interfeisu, jāieslēdz līdzeklis **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai** darbvietā **Līdzekļu pārvaldība**.

Lai ieslēgtu šo līdzekli visām juridiskajām personām, veiciet tālak norādītās darbības.

1. Darbvietas **Lïdzekĺu pārvaldība** cilnē **Viss** atlasiet sarakstā līdzekli **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai**.
2. Atlasiet **Iespējot tūlīt**, lai ieslēgtu atlasīto funkcionalitāti.
3. Atsvaidziniet lapu, lai piekļūtu jaunajam līdzeklim.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Citiem nodrošinātājiem piederošu veidņu rediģēšana

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.

    ![Biznesa dokumentu pārvaldības darbvieta](./media/BDM_overview_new_template1.png)

2. Cilnē **Atlasīt** atlasiet dokumentu, kas jālieto kā veidne, un pēc tam atlasiet **Izveidot dokumentu**.

    ![Dialoglodziņš biznesa dokumenti](./media/BDM_overview_new_template2.png)

3. Jaunā dialoglodziņa laukā **Nosaukums** mainiet nosaukumu, kā nepieciešams. Nosaukuma teksts tiek izmantots jaunajam automātiski izveidotās ER formāta konfigurācijas nosaukumam. Šīs konfigurācijas (**Klientu FTI pārskats (GER) Kopija**) melnraksta versija ietvers rediģēto veidni un tiks izmantota šī ER formāta izmantošanai pašreizējam lietotājam. Sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai ikvienam citam lietotājam.
4. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
5. Laukā **Komentārs** atjauniniet piezīmes rediģējamās veidnes, kas tiks izveidota automātiski, pārskatīšanai.
6. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

    ![Dialoglodziņš Dokumenta izveide](./media/BDM_overview_new_template3.png)

Pogu **Jauns dokuments** lieto, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, kas pieder citam nodrošinātājam. Šajā piemērā nodrošinātājs ir Microsoft. Atlasot **Jauns dokuments**, jūs varat rezēt visas veidnes, kas pieder pašreizējiem un citiem nodrošinātājiem. Pēc veidnes atlasīšanas tā ir atvērta rediģēšanai. Rediģētā veidne būs saglabāta jaunā ER formāta konfigurācijā, kas ģenerēta automātiski.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Augšupielādēt veidni, kas izmanto esošu Excel formātu
Izpildiet šīs darbības, lai pirms veidnes augšupielādes sniegtu nepieciešamo informāciju.

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.

    ![Biznesa dokumentu pārvaldības darbvieta](./media/BDM_overview_new_template1.png)
    
2. Lapā **Izveidot jaunu veidni**, cilnē **Augšupielādēt**, cilnē **Veidne** atlasiet **Pārlūkot**, lai atrastu un atlasītu Excel failu, kuru vēlaties izmantot kā veidni. Sadaļā **Veidne** automātiski tiek aizpildīti lauki **Nosaukums** un **Apraksts**. Tie nosaka automātiski izveidotās jaunā ER formāta konfigurācijas nosaukumu un aprakstu. Ja nepieciešams, jūs varat rediģēt šos laukus.
3. Sadaļas **Dokumenta tips** laukā **Nosaukums** norādiet biznesa dokumenta tipu. Šī vērtība tiks izmantota, lai meklētu pareizo datu avotu (t.i., ER modeļa konfigurāciju).

    ![Cilne Veidne](./media/BDM_overview_new_UI_import_21.jpg)

4. Cilnē **Datu avots** kopsavilkuma cilnē **Filtrs** atlasiet **Lietot filtru**. Sadaļā **Datu avots** lauks **Nosaukums** tiek aizpildīts automātiski vai varat atlasīt vērtību manuāli. Filtru var izmantot, lai meklētu atbilstošu datu avota nosaukumu pēc nosaukuma, apraksta, valsts/reģiona koda un biznesa dokumenta tipa.

    ![Datu avota cilne](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > Kopsavilkuma cilne **Filtrs** tiek izmantota, lai meklētu pareizo datu avotu (t.i., ER modeļa konfigurāciju). Jūs varat rediģēt visus filtra laukus, lai atrastu vispiemērotāko datu avotu dokumentam, ko augšupielādējat.
    > 
    > Kopsavilkuma cilnē **Filtrs** nosacījumi tiek izmantoti kā **VAI** nosacījumi.
    
5. Cilnē **Kartēšana** atlasiet **Automātiski noteikt**. Lauks **Saknes definīcija** tiek aizpildīts automātiski vai varat atlasīt vērtību manuāli. Šajā cilnē ir redzama elementu beigu kartēšana no veidnes un modeļa.

    ![Cilne Kartēšana](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Kartēšanai sadaļā **Veidņu struktūra** izmanto pilnu etiķešu vai aprakstu atbilstību datu avotā lietotāja valodā un šūnas nosaukumā veidnē.

6. Atlasiet **Izveidot dokumentu**, lai apstiprinātu, ka vēlaties izveidot veidni un sākt rediģēšanas procesu.

Plašāku informāciju skatiet [Biznesa dokumentu pārvaldības apskatā](er-business-document-management.md).

Ja elektronisko pārskatu nodrošinātājs nav pieejams, varat to izveidot. Ja nav aktīva nodrošinātāja, varat izvēlēties to aktivizēt.

- Lai izveidotu nodrošinātāju, mainiet nodrošinātāja nosaukumu laukā **Nosaukums**, atjauniniet jaunā nodrošinātāja interneta adresi laukā **Interneta adrese** un atlasiet **Labi**, lai apstiprinātu.

    ![Izveidot jaunu nodrošinātāju BDM](./media/bdm_create_provider.png)
    
- Lai aktivizētu esošu nodrošinātāju, izvēlieties nodrošinātāja nosaukumu laukā **Konfigurācijas nodrošinātājs** un atlasiet **Labi**, lai iestatītu nodrošinātāju kā aktīvu.

    ![Aktivizēt nodrošinātāju BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> Katra BDM veidne atsaucas uz nodrošinātāju kā konfigurācijas autoru. Tāpēc veidnei ir nepieciešams aktīvs nodrošinātājs.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
