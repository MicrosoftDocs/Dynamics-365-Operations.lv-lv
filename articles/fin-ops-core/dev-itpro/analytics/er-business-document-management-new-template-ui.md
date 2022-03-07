---
title: Microsoft Office-stila lietotāja interfeiss biznesa dokumentu pārvaldībā (satur video)
description: Šajā tēmā ir paskaidrots, kā izmantot jauno lietotāja interfeisu (UI) elektroniskā pārskata (ER) struktūras biznesa dokumentu pārvaldības līdzeklī.
author: v-anamir
ms.date: 01/05/2022
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
ms.openlocfilehash: e33830e2147d92ad5ee53ad11da55a50613b8ef9
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074745"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office-stila lietotāja interfeiss biznesa dokumentu pārvaldībā

[!include [banner](../includes/banner.md)]

Biznesa dokumentu pārvaldība ļauj iznesa lietotājiem rediģēt biznesa dokumentu veidnes, izmantojot pakalpojumu Microsoft Office 365 vai atbilstošu Microsoft Office darbvirsmas lietojumprogrammu. Rediģējumi var ietvert dizaina izmaiņas vai jaunas izvietošanas, vai arī lietotāji var pievienot vietturus, lai iekļautu papildu datus, nemainot pirmkodu. Papildinformāciju par to, kā strādāt ar biznesa dokumentu pārvaldību, skatiet [Biznesa dokumentu pārvaldības pārskatā](er-business-document-management.md).

Jaunais lietotāja interfeiss (UI) ir saprotamāks un ērtāk lietojams. Biznesa **dokumentu** apgabalā tiek rādītas tikai tās veidnes, kas pieder pašreizējam [aktīvajam](tasks/er-configuration-provider-mark-it-active-2016-11.md)[nodrošinātājam](general-electronic-reporting.md#Provider) un atrodas pašreizējā programmas instancē Dynamics 365 Finance. Iepriekšējā lietotāja interfeisā **cilnē Veidne** bija uzskaitītas visas veidnes, kas bija pieejamas jebkuram pakalpojumu sniedzējam. Tas arī parāda visas veidnes, ko izveidoja un laboja jebkurš lietotājs, kuram bija vienāda loma.

Biznesa dokumentu pārvaldības **darbvietas** pogu Jauns dokuments **var izmantot**, lai izveidotu un rediģētu [veidni elektroniskās pārskatu (ER)](general-electronic-reporting.md) formāta [konfigurācijā](general-electronic-reporting.md#Configuration), ko nodrošina cits pakalpojumu sniedzējs un kas atrodas pašreizējā Finance instancē, vai lai augšupielādētu jaunu veidni no Excel darbgrāmatas. Turklāt versijā 10.0.25 un jaunākās versijās varat izmantot **pogu Jauns dokuments**, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, kas tiek glabāta [globālajā repozitorijā](general-electronic-reporting.md#Repository).

Šīs tēmas piemēros aktīvais pakalpojumu sniedzējs ir Contoso, un to izmanto, lai izveidotu veidni, kuras pamatā ir Microsoft nodrošināta veidne. Alternatīvi veidni var izveidot, augšupielādējot savu veidni Excel formātā.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Jauna [biznesa dokumenta izveide, izmantojot biznesa dokumentu pārvaldības](https://youtu.be/gAIYl-mM_pw) video (parādīts iepriekš) ir iekļauta programmā pieejamajā [atskaņošanas](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sarakstā YouTube Finanses un operācijas.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Nodrošināt jauno dokumentu lietotāja interfeisa pieejamību biznesa dokumentu pārvaldībā

Lai biznesa dokumentu pārvaldībā sāktu izmantot jauno dokumentu lietotāja interfeisu, jāieslēdz līdzeklis **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai** darbvietā **Līdzekļu pārvaldība**.

Lai ieslēgtu šo līdzekli visām juridiskajām personām, veiciet tālak norādītās darbības.

1. Darbvietas **Lïdzekĺu pārvaldība** cilnē **Viss** atlasiet sarakstā līdzekli **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai**.
2. Atlasiet **Iespējot tūlīt**, lai ieslēgtu atlasīto funkcionalitāti.
3. Atsvaidziniet lapu, lai piekļūtu jaunajam līdzeklim.

## <a name="add-or-activate-a-provider"></a>Pakalpojumu sniedzēja pievienošana vai aktivizēšana

Katra biznesa dokumenta veidne tiek glabāta ER formāta konfigurācijā, kas ir atzīmēta kā noteikta konfigurācijas nodrošinātāja īpašumā. Veidojot jaunu veidni, tiek izveidota jauna ER formāta konfigurācija tās turēšanai. Tāpēc šai konfigurācijai ir jāidentificē pakalpojumu sniedzējs. Šim nolūkam tiek izmantots aktīvs ER sistēmas nodrošinātājs. Ja ER nav pakalpojumu sniedzēja, varat to izveidot. Ja nav *aktīva* pakalpojumu sniedzēja, varat aktivizēt kādu no esošajiem pakalpojumu sniedzējiem. Kad tas ir nepieciešams, tiek atvērts dialoglodziņš pakalpojumu sniedzēja pievienošanai vai aktivizēšanai, kamēr sākat pievienot jaunu veidni.

### <a name="add-a-new-provider"></a>Pievienot jaunu nodrošinātāju

Lai izveidotu jaunu pakalpojumu sniedzēju, dialoglodziņā Konfigurācijas nodrošinātājs **rīkojieties** šādi:

1.  Cilnes **Konfigurācijas** nodrošinātāja **izvēle laukā Nosaukums** ievadiet jaunā nodrošinātāja nosaukumu.
2.  Laukā **Interneta adrese** ievadiet jaunā pakalpojumu sniedzēja interneta adresi (URL). 
3.  Atlasiet **Labi**.

    ![Jauna nodrošinātāja izveide biznesa dokumentu pārvaldībā.](./media/bdm_create_provider.png)

Pievienotais nodrošinātājs tiks automātiski aktivizēts.

### <a name="activate-a-provider"></a>Pakalpojumu sniedzēja aktivizēšana

Lai aktivizētu pakalpojumu sniedzēju, dialoglodziņā Konfigurācijas nodrošinātājs **rīkojieties** šādi:

1.  Cilnes Konfigurācijas **nodrošinātāja** izvēle laukā Konfigurācijas **nodrošinātājs** atlasiet nodrošinātāju.
2.  Atlasiet **Labi**.

    ![Nodrošinātāja aktivizēšana biznesa dokumentu pārvaldībā.](./media/bdm_choose_provider.png)

Atlasītais nodrošinātājs tiks aktivizēts.

> [!NOTE]
> Katra biznesa dokumentu pārvaldības veidne atrodas ER formāta konfigurācijā, kas pakalpojumu sniedzēju dēvē par konfigurācijas autoru. Tāpēc katrai veidnei ir nepieciešams aktīvs nodrošinātājs.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Rediģēt veidni, kas pieder citam pakalpojumu sniedzējam

Šajā piemērā parādīts, kā izmantot **pogu Jauns dokuments** biznesa dokumentu pārvaldības **darbvietā**, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, ko nodrošina cits pakalpojumu sniedzējs un kas atrodas pašreizējā Finance instancē. Šajā piemērā aktīvais pakalpojumu sniedzējs ir Contoso, kas izmanto Microsoft nodrošināto ER formāta konfigurāciju. Kad esat atlasījis **Jauns dokuments**, **lapas Jaunas veidnes** izveide cilnē **Atlasīt** tiek rādītas visas pašreizējās finanšu instances veidnes, kas pieder pašreizējam nodrošinātājam un citiem pakalpojumu sniedzējiem. Atlasiet veidni, lai to atvērtu. Pēc tam varat izveidot jaunu rediģējamu veidnes kopiju. Rediģētā veidne tiek glabāta jaunā ER formāta konfigurācijā, kas tiek ģenerēta automātiski.

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.

    ![Biznesa dokumentu pārvaldības darbvieta.](./media/BDM_overview_new_template1.png)

2. **Lapas** Jaunas veidnes **izveide cilnē Atlase** atlasiet dokumentu, ko izmantot kā veidni, un pēc tam atlasiet **Izveidot dokumentu**.

    ![Dialoglodziņš biznesa dokumenti.](./media/BDM_overview_new_template2.png)

3. Jaunā dialoglodziņa laukā **Nosaukums** mainiet nosaukumu, kā nepieciešams. Nosaukuma teksts tiek izmantots jaunajam automātiski izveidotās ER formāta konfigurācijas nosaukumam. Šīs konfigurācijas (**Klientu FTI pārskats (GER) Kopija**) melnraksta versija ietvers rediģēto veidni un tiks izmantota šī ER formāta izmantošanai pašreizējam lietotājam. Sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai ikvienam citam lietotājam.
4. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
5. Laukā **Komentārs** atjauniniet piezīmes rediģējamās veidnes, kas tiks izveidota automātiski, pārskatīšanai.
6. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

    ![Dialoglodziņš Dokumenta izveide.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Tādas veidnes augšupielāde, kas izmanto esošu Excel darbgrāmatu

Šajā piemērā parādīts, kā izmantot **pogu Jauns dokuments** biznesa dokumentu pārvaldības **darbvietā**, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, pamatojoties uz pieejamo Excel darbgrāmatu. Šajā piemērā aktīvais nodrošinātājs ir Contoso, un jūs izmantojat Microsoft nodrošināto ER [datu modeli](er-overview-components.md#data-model-component) un ER [modeļu kartēšanas](er-overview-components.md#model-mapping-component) konfigurācijas. Kad esat atlasījis **Jauns dokuments**, lapā Jaunas veidnes **izveide atlasiet** cilni **Augšupielādēt**. Tur varat norādīt excel darbgrāmatas augšupielādes detaļas. Pēc Excel darbgrāmatas augšupielādes tā tiek pārveidota par biznesa dokumentu veidni, kas tiek atvērta rediģēšanai. Rediģētā veidne tiks saglabāta jaunā ER formāta konfigurācijā, kas tiek ģenerēta automātiski.

Izpildiet šīs darbības, lai pirms veidnes augšupielādes sniegtu nepieciešamo informāciju.

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.
2. Lapā **Izveidot jaunu veidni**, cilnē **Augšupielādēt**, cilnē **Veidne** atlasiet **Pārlūkot**, lai atrastu un atlasītu Excel failu, kuru vēlaties izmantot kā veidni. Sadaļā **Veidne** automātiski tiek aizpildīti lauki **Nosaukums** un **Apraksts**. Tie nosaka automātiski izveidotās jaunā ER formāta konfigurācijas nosaukumu un aprakstu. Ja nepieciešams, jūs varat rediģēt šos laukus.
3. Sadaļas **Dokumenta tips** laukā **Nosaukums** norādiet biznesa dokumenta tipu. Šī vērtība tiks izmantota, lai meklētu pareizo datu avotu (t.i., ER modeļa konfigurāciju).

    ![Lapas Jaunas veidnes izveide cilnes Veidnes cilne Augšupielāde.](./media/BDM_overview_new_UI_import_21.jpg)

4. Cilnē **Datu avots** kopsavilkuma cilnē **Filtrs** atlasiet **Lietot filtru**. Sadaļā **Datu avots** lauks **Nosaukums** tiek aizpildīts automātiski vai varat atlasīt vērtību manuāli. Filtru var izmantot, lai meklētu atbilstošu datu avota nosaukumu pēc nosaukuma, apraksta, valsts/reģiona koda un biznesa dokumenta tipa.

    ![Lapas Jaunas veidnes izveide cilnes Augšupielādēt cilne Datu avots.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Kopsavilkuma cilne **Filtrs** tiek izmantota, lai meklētu pareizo datu avotu (t.i., ER modeļa konfigurāciju). Jūs varat rediģēt visus filtra laukus, lai atrastu vispiemērotāko datu avotu dokumentam, ko augšupielādējat.
    > 
    > Kopsavilkuma cilnē **Filtrs** nosacījumi tiek izmantoti kā **VAI** nosacījumi.

5. Cilnē **Kartēšana** atlasiet **Automātiski noteikt**. Lauks **Saknes definīcija** tiek aizpildīts automātiski vai varat atlasīt vērtību manuāli. Šajā cilnē ir redzama elementu beigu kartēšana no veidnes un modeļa.

    ![Lapas Jaunas veidnes izveide cilnes Augšupielāde cilne Kartēšana.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Kartēšanai sadaļā **Veidņu struktūra** izmanto pilnu etiķešu vai aprakstu atbilstību datu avotā lietotāja valodā un šūnas nosaukumā veidnē.

6. Atlasiet **Izveidot dokumentu**, lai apstiprinātu, ka vēlaties izveidot veidni un sākt rediģēšanas procesu.

Plašāku informāciju skatiet [Biznesa dokumentu pārvaldības apskatā](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Veidnes augšupielāde no globālā repozitorija

Šajā piemērā parādīts, kā izmantot **pogu Jauns dokuments** biznesa dokumentu pārvaldības **darbvietā**, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, ko nodrošina korporācija Microsoft un kas atrodas globālajā repozitorijā. Šajā piemērā aktīvais pakalpojumu sniedzējs ir Contoso, kas izmanto Microsoft nodrošināto ER formāta konfigurāciju. Pēc jauna dokumenta **atlasīšanas** **lapas Jaunas veidnes** izveide cilnē **Importēt no globālā repozitorija** tiek rādītas visas biznesa dokumentu veidnes, kas tiek glabātas globālajā repozitorijā, bet trūkst pašreizējā Finance instancē. Pēc veidnes atlasīšanas tā tiek importēta no globālā repozitorija pašreizējā Finance instancē, lai izveidotu jaunu rediģējamu kopiju. Rediģētā veidne tiek glabāta jaunā ER formāta konfigurācijā, kas tiek ģenerēta automātiski.

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.
2. **Lapas** Jaunas veidnes **izveide cilnē Importēt no globālā repozitorija** atlasiet dokumentu, ko izmantot kā veidni, un pēc tam atlasiet **Izveidot dokumentu**.

    ![Importēt no globālā repozitorija lapas Izveidot jaunu veidni cilnes.](./media/BDM_overview_new_template22.png)

3. Ziņojuma lodziņā atlasiet **Jā**, lai apstiprinātu, ka vēlaties importēt atlasīto dokumentu no globālā repozitorija pašreizējā Finance instancē. Ja tiek prasīts autorizēt, izpildiet ekrānā redzamos norādījumus.
4. Jaunā dialoglodziņa laukā **Nosaukums** mainiet nosaukumu, kā nepieciešams. Nosaukuma teksts tiek izmantots jaunajam automātiski izveidotās ER formāta konfigurācijas nosaukumam. Šīs konfigurācijas melnraksta versija (**Atgādinājuma vēstules piezīmes (Excel) Kopija**) saturēs rediģēto veidni un tiks izmantota, lai palaistu šo ER formātu pašreizējam lietotājam. Sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai ikvienam citam lietotājam.
5. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
6. Laukā **Komentārs** atjauniniet piezīmes rediģējamās veidnes, kas tiks izveidota automātiski, pārskatīšanai.
7. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
