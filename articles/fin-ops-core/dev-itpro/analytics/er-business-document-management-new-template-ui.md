---
title: Microsoft Office- stila lietotāja interfeiss biznesa dokumentu pārvaldībā (satur video)
description: Šajā rakstā skaidrots, kā izmantot jauno lietotāja interfeisu Elektronisko pārskatu (ER) struktūras biznesa dokumentu pārvaldības funkcijai.
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
ms.openlocfilehash: bcc464a17e27393c5904c59b8439de6ca000d57a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892230"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office-stila lietotāja interfeiss biznesa dokumentu pārvaldībā

[!include [banner](../includes/banner.md)]

Biznesa dokumentu pārvaldība ļauj iznesa lietotājiem rediģēt biznesa dokumentu veidnes, izmantojot pakalpojumu Microsoft Office 365 vai atbilstošu Microsoft Office darbvirsmas lietojumprogrammu. Rediģējumi var ietvert dizaina izmaiņas vai jaunas izvietošanas, vai arī lietotāji var pievienot vietturus, lai iekļautu papildu datus, nemainot pirmkodu. Papildinformāciju par to, kā strādāt ar biznesa dokumentu pārvaldību, skatiet [Biznesa dokumentu pārvaldības pārskatā](er-business-document-management.md).

Jaunais lietotāja interfeiss (UI) ir saprotamāks un ērtāk lietojams. Biznesa **dokumentu apgabals** parāda [tikai](tasks/er-configuration-provider-mark-it-active-2016-11.md)[veidnes](general-electronic-reporting.md#Provider), kas pieder pašreizējam aktīvajam nodrošinātājam un atrodas pašreizējā Dynamics 365 Finanšu instancē. Iepriekšējā UI cilnē Veidne ir **uzskaitītas** visas veidnes, kas bija pieejamas jebkuram nodrošinātājam. Tas arī parāda visas veidnes, ko izveidoja un laboja jebkurš lietotājs, kuram bija vienāda loma.

**·** **·**[Varat izmantot pogu Jauns dokuments biznesa dokumentu pārvaldības darbvietā, lai izveidotu un rediģētu veidni elektronisko pārskatu (ER)](general-electronic-reporting.md)[formāta](general-electronic-reporting.md#Configuration) konfigurācijā, ko nodrošina cits nodrošinātājs un kas atrodas pašreizējā Finanšu instancē, vai lai augšupielādētu jaunu veidni no Excel darbgrāmatas. Turklāt versijā 10.0.25 un jaunākā versijā varat lietot pogu Jauns dokuments, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, **kas** saglabāta Globālajā repozitorijā [.](general-electronic-reporting.md#Repository)

Šī raksta piemēros aktīvais nodrošinātājs ir Contoso, un jūs to izmantojat, lai izveidotu veidni, kas ir balstīta uz Microsoft nodrošināto veidni. Alternatīvi veidni var izveidot, augšupielādējot savu veidni Excel formātā.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Jaunais [biznesa dokuments, lietojot biznesa dokumentu](https://youtu.be/gAIYl-mM_pw) pārvaldības video (parādīts iepriekš) ir iekļauts [Finanšu un operāciju par](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) pieejamajiem YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Nodrošināt jauno dokumentu lietotāja interfeisa pieejamību biznesa dokumentu pārvaldībā

Lai biznesa dokumentu pārvaldībā sāktu izmantot jauno dokumentu lietotāja interfeisu, jāieslēdz līdzeklis **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai** darbvietā **Līdzekļu pārvaldība**.

Lai ieslēgtu šo līdzekli visām juridiskajām personām, veiciet tālak norādītās darbības.

1. Darbvietas **Lïdzekĺu pārvaldība** cilnē **Viss** atlasiet sarakstā līdzekli **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai**.
2. Atlasiet **Iespējot tūlīt**, lai ieslēgtu atlasīto funkcionalitāti.
3. Atsvaidziniet lapu, lai piekļūtu jaunajam līdzeklim.

## <a name="add-or-activate-a-provider"></a>Nodrošinātāja pievienošana vai aktivizēšana

Katra biznesa dokumenta veidne tiek glabāta ER formāta konfigurācijā, kas atzīmēta kā pieder noteiktam konfigurācijas nodrošinātājam. Veidojot jaunu veidni, tiek izveidota jauna ER formāta konfigurācija, lai to aizturētu. Tādēļ ir jābūt identificētam šīs konfigurācijas nodrošinātājam. Šim nolūkam tiek izmantots ER struktūras aktīvais nodrošinātājs. Ja ER nav nodrošinātāja, to var izveidot. Ja nav aktīva *nodrošinātāja*, var aktivizēt vienu no esošajiem nodrošinātājiem. Ja nepieciešams, tiek atvērts dialogs nodrošinātāja pievienošanai vai aktivizēšanai, jāsāk jaunas veidnes pievienošana.

### <a name="add-a-new-provider"></a>Pievienot jaunu nodrošinātāju

Lai izveidotu jaunu nodrošinātāju, konfigurācijas nodrošinātāja dialogā **veiciet tālāk aprakstītās** darbības.

1.  Cilnes Izvēlēties **konfigurācijas nodrošinātāju** laukā **Nosaukums** ievadiet jaunā nodrošinātāja nosaukumu.
2.  Interneta adreses **laukā** ievadiet jaunā nodrošinātāja interneta adresi (URL). 
3.  Atlasiet **Labi**.

    ![Tiek veidots jauns nodrošinātājs biznesa dokumentu pārvaldībā.](./media/bdm_create_provider.png)

Pievienotais nodrošinātājs tiks automātiski aktivizēts.

### <a name="activate-a-provider"></a>Nodrošinātāja aktivizēšana

Lai aktivizētu nodrošinātāju, konfigurācijas nodrošinātāja dialogā **veiciet šādas** darbības:

1.  Cilnes Izvēlēties **konfigurācijas nodrošinātāju** laukā **Konfigurācijas nodrošinātājs** atlasiet nodrošinātāju.
2.  Atlasiet **Labi**.

    ![Nodrošinātāja aktivizēšana biznesa dokumentu pārvaldībā;](./media/bdm_choose_provider.png)

Atlasītais nodrošinātājs tiks aktivizēts.

> [!NOTE]
> Katra biznesa dokumentu pārvaldības veidne atrodas ER formāta konfigurācijā, kas attiecas uz nodrošinātāju kā konfigurācijas autoru. Tāpēc katrai veidnei ir nepieciešams aktīvs nodrošinātājs.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Rediģēt veidni, kas pieder citam nodrošinātājam

Šajā piemērā **parādīts** **·**, kā izmantot pogu Jauns dokuments biznesa dokumentu pārvaldības darbvietā, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, ko nodrošina cits nodrošinātājs un kas atrodas pašreizējā Finanšu instancē. Šajā piemērā aktīvais pakalpojumu sniedzējs ir Contoso, kas izmanto ER formāta konfigurāciju, ko nodrošina Microsoft. Pēc jauna dokumenta atlases **cilnes Atlasīt lapā Izveidot jaunu veidni ir redzamas visas pašreizējā finanšu instances veidnes,** **·** **kas pieder pašreizējam nodrošinātājam un citiem nodrošinātājiem.** Atlasiet veidni, lai to atvērtu. Pēc tam var izveidot jaunu rediģējamu veidnes kopiju. Rediģētā veidne tiek saglabāta automātiski ģenerētā jaunā ER formāta konfigurācijā.

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.

    ![Biznesa dokumentu pārvaldības darbvieta.](./media/BDM_overview_new_template1.png)

2. **Cilnes Atlasīt lapā Izveidot** jaunu **veidni atlasiet dokumentu**, ko izmantot kā veidni, un pēc tam atlasiet **Izveidot dokumentu**.

    ![Dialoglodziņš biznesa dokumenti.](./media/BDM_overview_new_template2.png)

3. Jaunā dialoglodziņa laukā **Nosaukums** mainiet nosaukumu, kā nepieciešams. Nosaukuma teksts tiek izmantots jaunajam automātiski izveidotās ER formāta konfigurācijas nosaukumam. Šīs konfigurācijas (**Klientu FTI pārskats (GER) Kopija**) melnraksta versija ietvers rediģēto veidni un tiks izmantota šī ER formāta izmantošanai pašreizējam lietotājam. Sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai ikvienam citam lietotājam.
4. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
5. Laukā **Komentārs** atjauniniet piezīmes rediģējamās veidnes, kas tiks izveidota automātiski, pārskatīšanai.
6. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

    ![Dialoglodziņš Dokumenta izveide.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Augšupielādēt veidni, kas izmanto esošu Excel darbgrāmatu

Šajā piemērā parādīts, **kā izmantot pogu** **Jauns** dokuments biznesa dokumentu pārvaldības darbvietā, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, pamatojoties uz pieejamo Excel darbgrāmatu. Šajā piemērā aktīvais nodrošinātājs ir Contoso, un jūs izmantojat ER datu [modeli un ER](er-overview-components.md#data-model-component)[modeļa](er-overview-components.md#model-mapping-component) kartēšanas konfigurācijas, ko nodrošina Microsoft. Kad esat izveidojis **jaunu** dokumentu **·**, atlasiet cilni Augšupielādēt lapā **Izveidot jaunu veidni**. Tur varat norādīt excel darbgrāmatas augšupielādes detaļas. Pēc Excel darbgrāmatas augšupielādes tā ir pārvērsta biznesa dokumenta veidnē, kas ir atvērta rediģēšanai. Rediģētā veidne tiks saglabāta jaunā ER formāta konfigurācijā, kas ir automātiski ģenerēta.

Izpildiet šīs darbības, lai pirms veidnes augšupielādes sniegtu nepieciešamo informāciju.

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.
2. Lapā **Izveidot jaunu veidni**, cilnē **Augšupielādēt**, cilnē **Veidne** atlasiet **Pārlūkot**, lai atrastu un atlasītu Excel failu, kuru vēlaties izmantot kā veidni. Sadaļā **Veidne** automātiski tiek aizpildīti lauki **Nosaukums** un **Apraksts**. Tie nosaka automātiski izveidotās jaunā ER formāta konfigurācijas nosaukumu un aprakstu. Ja nepieciešams, jūs varat rediģēt šos laukus.
3. Sadaļas **Dokumenta tips** laukā **Nosaukums** norādiet biznesa dokumenta tipu. Šī vērtība tiks izmantota, lai meklētu pareizo datu avotu (t.i., ER modeļa konfigurāciju).

    ![Cilnes Augšupielādēt veidne lapā Izveidot jaunu veidni.](./media/BDM_overview_new_UI_import_21.jpg)

4. Cilnē **Datu avots** kopsavilkuma cilnē **Filtrs** atlasiet **Lietot filtru**. Sadaļā **Datu avots** lauks **Nosaukums** tiek aizpildīts automātiski vai varat atlasīt vērtību manuāli. Filtru var izmantot, lai meklētu atbilstošu datu avota nosaukumu pēc nosaukuma, apraksta, valsts/reģiona koda un biznesa dokumenta tipa.

    ![Datu avota cilne cilnes Augšupielāde lapā Izveidot jaunu veidni.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Kopsavilkuma cilne **Filtrs** tiek izmantota, lai meklētu pareizo datu avotu (t.i., ER modeļa konfigurāciju). Jūs varat rediģēt visus filtra laukus, lai atrastu vispiemērotāko datu avotu dokumentam, ko augšupielādējat.
    > 
    > Kopsavilkuma cilnē **Filtrs** nosacījumi tiek izmantoti kā **VAI** nosacījumi.

5. Cilnē **Kartēšana** atlasiet **Automātiski noteikt**. Lauks **Saknes definīcija** tiek aizpildīts automātiski vai varat atlasīt vērtību manuāli. Šajā cilnē ir redzama elementu beigu kartēšana no veidnes un modeļa.

    ![Cilnes Augšupielāde cilnē Izveidot jaunu veidni kartēšana.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Kartēšanai sadaļā **Veidņu struktūra** izmanto pilnu etiķešu vai aprakstu atbilstību datu avotā lietotāja valodā un šūnas nosaukumā veidnē.

6. Atlasiet **Izveidot dokumentu**, lai apstiprinātu, ka vēlaties izveidot veidni un sākt rediģēšanas procesu.

Plašāku informāciju skatiet [Biznesa dokumentu pārvaldības apskatā](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Augšupielādēt veidni no globālā repozitorija

Šis piemērs parāda, **·** **kā** izmantot pogu Jauns dokuments biznesa dokumentu pārvaldības darbvietā, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, ko nodrošina Microsoft un kas atrodas Globālajā repozitorijā. Šajā piemērā aktīvais pakalpojumu sniedzējs ir Contoso, kas izmanto ER formāta konfigurāciju, ko nodrošina Microsoft. Pēc jauna **dokumenta atlases cilnes Importēt no globālā repozitorija lapā Izveidot jaunu veidni tiks rādītas visas biznesa dokumentu veidnes,** **·** **kas tiek glabātas Globālajā repozitorijā, bet nav norādītas pašreizējā finanšu instancē.** Pēc veidnes atlases tas ir importēts no globālā repozitorija pašreizējā finanšu instancē, lai izveidotu jaunu rediģējamu kopiju. Rediģētā veidne tiek saglabāta automātiski ģenerētā jaunā ER formāta konfigurācijā.

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.
2. Lapā Izveidot **jaunu veidni cilnē** Importēt no **globālā repozitorija** atlasiet dokumentu, ko izmantot kā veidni, un pēc tam atlasiet **Izveidot dokumentu**.

    ![Importēt no globālā repozitorija cilnes, kas atrodas lapā Izveidot jaunu veidni.](./media/BDM_overview_new_template22.png)

3. Ziņojuma lodziņā atlasiet Jā, lai **apstiprinātu**, ka vēlaties importēt atlasīto dokumentu no globālā repozitorija pašreizējā Finanšu instancē. Ja tiek prasīta autorizācija, izpildiet ekrānā redzamos norādījumus.
4. Jaunā dialoglodziņa laukā **Nosaukums** mainiet nosaukumu, kā nepieciešams. Nosaukuma teksts tiek izmantots jaunajam automātiski izveidotās ER formāta konfigurācijas nosaukumam. Šīs konfigurācijas melnraksta versija (**Atgādinājuma vēstules (Excel) kopija)** saturēs rediģēto veidni un tiks izmantota, lai palaistu šo ER formātu pašreizējam lietotājam. Sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai ikvienam citam lietotājam.
5. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
6. Laukā **Komentārs** atjauniniet piezīmes rediģējamās veidnes, kas tiks izveidota automātiski, pārskatīšanai.
7. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
