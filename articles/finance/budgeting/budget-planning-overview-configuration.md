---
title: Budžeta plānošanas pārskats
description: Šajā tēmā aprakstīta budžeta plānošana. Tā satur informāciju, kas var palīdzēt jums sagatavoties budžeta plānošanas konfigurēšanai un iestatītu budžeta plānošanas procesus.
author: panolte
ms.date: 01/11/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "17251"
- intro-internal
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d69d3d1620616bd7a136645d6f28f638e8bcf199
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711748"
---
# <a name="budget-planning-overview"></a>Budžeta plānošanas pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīta budžeta plānošana. Tā satur informāciju, kas var palīdzēt jums sagatavoties budžeta plānošanas konfigurēšanai un iestatītu budžeta plānošanas procesus.

## <a name="overview-of-budget-planning"></a>Budžeta plānošanas pārskats

Organizācija var konfigurēt budžeta plānošanu un pēc tam iestatīt budžeta plānošanas procesus atbilstoši savai politikai, procedūrām un budžeta sagatavošanas prasībām. Izprotot koncepcijas un terminoloģija Microsoft Dynamics, kas tiek izmantota 365 Finansēs, ir iespējams daudz vieglāk un efektīvāk īstenot budžeta plānošanu savā organizācijā.

### <a name="key-terms"></a>Galvenie termini

- **Budžeta plānošanas procesi** — nosaka budžeta plānu atjaunināšanas, maršrutēšanas, pārskatīšanas un apstiprināšanas veidu budžeta veidošanas organizācijas hierarhijā. Budžeta plānošanas process ir saistīts ar budžeta ciklu un organizāciju, izmantojot juridisku personu.
- **Budžeta plāni** — satur budžeta datus, kas tiek izmantoti budžeta ciklam. Jums var būt vairāki budžeta plāni, kas tiek izmantoti dažādiem nolūkiem. Piemēram, varat izmantot budžeta plānus, lai izveidotu budžeta summas atšķirīgām organizācijas vienībām. Varat arī tos izmantot, lai veiktu salīdzinājumus un pieņemtu informētus lēmumus.
- **Budžeta plāna scenāriji** — definē datu kategorijas budžeta plānos. Definējiet budžeta plāna scenārijus, lai atbalstītu monetāro un citas mērvienību klases vienības, piemēram, daudzumus. Monetārā budžeta plāna scenāriju paraugi ir arī "Nodaļas iepriekšējā gads" un "Nodaļu pieprasījumi". Budžeta plāna scenāriju piemēri, kuri izmanto daudzumus, ietver arī "Iepriekšējā gada atbalsta zvani" un "Pilna laika ekvivalentu (PLE) skaits."
- **Budžeta plānošanas stadijas** — definē posmus, kurus iziet budžeta plāns no tā uzsākšanas līdz galīgās apstiprināšanas brīdim. Budžeta plānošanas stadijas ir sakārtotas budžeta plānošanas darbplūsmās.
- **Budžeta plānošanas darbplūsmas** — sastāv no budžeta plānošanas stadijām un definē tās. Budžeta plānošanas darbplūsmas ir saistītas ar budžeta veidošanas darbplūsmām. Budžeta veidošanas darbplūsmas ir automatizēti un manuāli procesi, kas pārvieto budžeta plānus no vienas budžeta plānošanas stadijas uz citu.

[![Budžeta plānošanas terminoloģija.](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Parastie uzdevumi

Budžeta plānošanu var izmantot tālāk norādīto uzdevumu izpildei.

- Izveidojiet budžeta plānus, lai noteiktu paredzamos ieņēmumus un izdevumus budžeta ciklā.
- Analizējiet un atjauniniet budžeta plānus vairākiem scenārijiem.
- Automātiski maršrutējiet budžeta plānus kopā ar darblapām, pamatojuma dokumentiem un citiem pielikumiem turpmākai pārskatīšanai un apstiprināšanai.
- Konsolidējiet vairākus budžeta plānus no zemāka organizācijas līmeņa vienā pamata budžeta plānā augstākā līmenī. Varat arī izstrādāt vienu budžeta plānu augstākā organizācijas līmenī un piešķirt budžetu zemākiem līmeņiem.

Budžeta plānošana ir integrēta ar citiem moduļiem. Tāpēc varat ietvert informāciju no iepriekšējiem budžetiem, faktiskajiem izdevumiem, pamatlīdzekļiem un cilvēkresursiem. Tā kā budžeta plānošana ir integrēta arī programmās Microsoft Excel un Microsoft Word, varat izmantot šīs programmas, lai strādātu ar budžeta plānošanas datiem. Piemēram, budžeta pārvaldnieks var eksportēt nodaļas budžeta pieprasījumu no budžeta plāna scenārija uz Excel darblapu. Datus var pēc tam analizēt, atjaunināt un veido diagrammas darblapās un pēc tam publicēt budžeta plāna rindās.

## <a name="configuring-budget-planning"></a>Budžeta plānošanas konfigurēšana

Funkcionalitāte, kas ieviesta Dynamics 365 finanšu versijā 10.0.9 (2020. gada aprīlī) **ietver** līdzekli, kas palīdz uzlabot veiktspēju, kad izmantojat pogu Publicēt, lai atjauninātu esošos ierakstus programmā Excel un pēc tam tos publicētu atpakaļ klientā. Šis līdzeklis paātrina atjaunināšanas procesu un palīdz arī samazināt iespējamību, ka atjauninājums tiks bloķēts, kad vienlaicīgi atjaunināt daudzus ierakstus. Lai šo funkcionalitāti padarītu pieejamu, pārejiet uz darbvietu **Līdzekļu pārvaldība** un ieslēdziet līdzekli **Budžeta plānošanas vaicājumu optimizācija veiktspējai**, kas atrodas sadaļā **Budžeta veidošana**. Iesakām ieslēgt šo līdzekli.

Lapā **Budžeta plānošanas konfigurācija** ir lielākā iestatījumu to daļa, kas jums nepieciešami, lai iestatītu budžeta plānošanu. Turpmākajās sadaļās aprakstīti daži faktori, kas jāņem vērā, kad konfigurējat budžeta plānošanu. Kad esat pabeidzis konfigurēšanu, varat iestatīt budžeta plānošanas procesus.

### <a name="budget-planning-schema-optional"></a>Budžeta plānošanas shēma (neobligāta)

Neobligāta, bet ieteicama pirmā darbība ir izveidot shēmu, kas parāda jūsu organizācijas budžeta formulēšanas procedūru. Šīs shēmas izveidei varat izmantot jebkuru metodi, kuru vēlaties.

Šajā attēlā parādīts vispārīgs piemērs, kurā dažādiem organizācijas līmeņiem ir izveidotas atsevišķas budžeta plānošanas darbplūsmas. Katrā darbplūsmā tiek noteiktas stadijas, un katrai stadijai tiek piešķirti noteikti scenāriji, kas satur budžeta datus. Uzdevumi tiek izpildīti, lai pārvietotu datus no vienas stadijas uz nākamo. Piemēram, summas var tikt piesaistītas vai apkopotas dažādos kontos, apstiprinājumos vai citos pārskatos. Šajā ilustrācijā teksts kursīvā apzīmē scenāriju, kas šajā stadijā nav rediģējams, vai datus, kas ir vēsturiski vai ir apstiprināti agrākā stadijā un tādēļ nav jāmaina.

[![Budžeta plānošanas vispārīgā shēma.](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Šajā ilustrācijā rādīts piemērs, kurā galvenā pārvalde aplēš bāzlīnijas summas sākotnējam budžetam un izplata tās pārdošanas nodaļām. Pārdošanas nodaļas novērtē un iesniedz savas prognozes atpakaļ galvenajai pārvaldei, kur budžeta pārvaldnieks prognozi apkopo un pielāgo. Visbeidzot, budžeta pārvaldnieks nosūta koriģētās budžeta summas pārskatīšanai, galīgajiem pielāgojumiem un apstiprināšanai galvenajam finanšu pārvaldniekam (CFO).

[![Budžeta plānošanas shēmas piemērs.](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Organizācijas hierarhija budžeta plānošanai

Lapā **Organizācijas hierarhija** varat konkretizēt organizācijas hierarhiju par budžeta plānošanas hierarhiju katrā budžeta plānošanas procesā. Budžeta plānošanas hierarhijai nav jāatbilst standarta organizācijas hierarhijai, kas tiek izmantota citiem mērķiem. Tā kā šī hierarhija tiek izmantota, lai apkopotu un izplatītu datus, varat izvēlēties atšķirīgu struktūru. Piemēra shēmā pārdošanas nodaļas pakļaujas galvenās pārvaldes līmenim, kurā ir budžeta un finanšu nodaļas. Šī struktūra, iespējams, atšķiras no struktūras, kas tiek izmantota, lai pārvaldītu operācijas pārdošanas nodaļās. Katram budžeta plānošanas procesam var piešķirt tikai vienu organizācijas hierarhiju.

Papildinformāciju skatiet rakstā [Organizācijas un organizāciju hierarhijas](../../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Lietotāja drošība

Budžeta plānošanai varat izmantot vienu no diviem drošības modeļiem, kas definē lietotāju atļaujas. Lai norādītu drošības modeli, iestatiet budžeta plānošanas parametru lapā **Budžeta plānošanas konfigurācija**.

### <a name="budget-planning-workflows-stages"></a>Budžeta plānošanas darbplūsmu stadijas

Lai pārvaldītu budžeta plānu izveidi un attīstību, tiek izmantotas budžeta plānošanas darbplūsmas un budžeta veidošanas darbplūsmas.

Budžeta plānošanas darbplūsmu sastāv no sakārtota posmu kopuma, pa kuru pārvietojas budžeta plāns. Katra budžeta plānošanas darbplūsma ir saistīta ar budžeta veidošanas darbplūsmu. Budžeta plānošanas darbplūsmas ir viens no darbplūsmas tipiem, kas tiek izmantoti visā Dynamics 365 finansēs. Tās maršrutē budžeta plānus kopā ar darblapām, pamatojumiem un pielikumiem organizācijas ietvaros to pārskatīšanai un apstiprināšanai.

Budžeta plānošanas darbplūsmu iespējams izveidot lapas **Budžeta plānošanas konfigurācija** sadaļā **Darbplūsmas stadijas**. Tur varat atlasīt izmantojamās stadijas un budžeta veidošanas darbplūsmas, un konfigurēt papildu iestatījumus.

Laba prakse ir izveidot budžeta plānošanas darbplūsmu katrā budžeta veidošanas hierarhijas līmenī. Pēc tam piešķiriet budžeta veidošanas darbplūsmu, kas satur elementus, kuri atbilst budžeta plānošanas darbplūsmas stadijām. Piemēra shēmā, kas parādīta iepriekš šajā tēmā, viena budžeta plānošanas darbplūsma tiks izveidota pārdošanas nodaļām un cita tiks izveidota galvenajai pārvaldei. Budžeta veidošanas darbplūsmas pārvieto budžeta plānus no vienas stadijas uz citu.

Budžeta veidošanas darbplūsmu budžeta plānošanai varat izveidot lapā **Budžeta veidošanas darbplūsmas**. Process līdzinās citu darbplūsmu veidošanas procesam. Šajā attēlā parādīts galvenās pārvaldes darbplūsmas piemērs.

[![Budžeta veidošanas darbplūsma budžeta plānošanai.](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Darbplūsma ietver šādus elementus:

- Sadalījums pārdošanas nodaļās un to iesniegumu summēšana
- Budžeta pārvaldnieka pārskats
- CFO apstiprinājums
- Sagatavošanas posmu pārejas starp katru budžeta plānošanas darbplūsmas stadiju

Budžeta veidošanas darbplūsma tiek piešķirta katrai budžeta plānošanas darbplūsmai lapas **Budžeta plānošanas konfigurācija** sadaļā **Darbplūsmas stadijas**.

### <a name="parameters-scenarios-and-stages"></a>Parametri, scenāriji un stadijas

Sākotnējie iestatījumi lapā **Budžeta plānošanas konfigurācija** ļauj izveidot dažus veidošanas blokus vēlākām konfigurēšanas darbībām.

- **Parametri** — definē drošības kārtulas, kuras vēlaties lietot budžeta plāniem un noklusējuma finanšu dimensijas, kas ir jāizmanto, kad lietotāji detalizē summas budžeta plāna scenārijos.
- **Scenāriji** — ietver datu kategorijas, kuras vēlaties izmantot budžeta plānos. Definējiet budžeta plāna scenārijus, lai atbalstītu monetāro un citas mērvienību klases vienības, piemēram, daudzumu. Budžeta plānā scenāriji atspoguļo vienu budžeta plānošanas datu versiju. Monetārā budžeta plāna scenāriju paraugi ir arī "Iepriekšējā gada pārdošana" un "Noslēgtie līgumi." Piemēri scenārijiem, kas izmanto daudzumus, ir arī "Pārdošanas zvanu skaits" un "Pilna laika ekvivalents (PLE)."
- **Stadijas** — definē darbības, kurām seko budžeta plāns no sākuma līdz galīgajai apstiprināšanai. Budžeta plānošanas stadijas piemēri ir "HQ apkopojums", "CFO pārskatīšana" un "Gala."

### <a name="allocation-schedules"></a>Sadalījuma grafiki

Budžeta plānošanā varat sadalīt budžeta plāna rindu summas vai daudzumus no viena scenārija citā scenārijā, vai pat tajā pašā scenārijā. Piemēram, varat sadalīt summas vai daudzumus tajā pašā scenārijā, ja vēlaties veikt izmaiņas finanšu dimensijās vai summu datumos šajā scenārijā. Sadalīšanu varat veikt budžeta plāna ietvaros vai no viena budžeta plāna uz citu.

Sadalījuma grafiki automātiski sadala budžeta plāna rindas darbplūsmas apstrādes laikā. Varat veikt sadalījumu, izmantojot kādu no metodēm sarakstā **Sadalījuma metode**.

- **Sadalīt pa periodiem** — lai budžeta plāna rindas no avota budžeta plāna scenārija sadalītu mērķa scenārija periodos, izmantojiet periodu sadalījuma principu.

    > [!NOTE]
    > Lai varētu sadalīt dažādos periodos, lapā **Perioda sadalījuma kategorijas** ir jāiestata periodu sadalījuma principi.

- **Sadalīšana dimensijās** — budžeta plāna rindas tiek sadalītas no avota budžeta plāna scenārija visās mērķa scenārija finanšu dimensijās.

    > [!NOTE]
    > Lai varētu sadalīt dimensijās, lapā **Budžeta sadalījuma nosacījumi** ir jāiestata budžeta sadalījuma noteikumi.

- **Apkopot** — budžeta plāna rindas tiek apkopotas no avota budžeta plāna scenārija saistītajos budžeta plānos uz mērķa scenāriju pamata budžeta plānā.
- **Sadalīt** — budžeta plāna rindas ir sadalītas no avota budžeta plāna scenārija pamata budžeta plānā uz mērķa scenāriju saistītajos budžeta plānos.
- **Izmantot Virsgrāmatas sadalījuma kārtulas** — budžeta plāna rindas tiek sadalītas no avota budžeta plāna scenārija uz mērķa scenāriju saskaņā ar atlasīto Virsgrāmatas sadalījuma kārtulu.
- **Kopēt no budžeta plāna** — varat atlasīt citu budžeta plānu, kas tiks izmantots par sadalījuma avotu.

### <a name="stage-allocations"></a>Stadijas sadalījumi

Stadijas sadalījumi tiek izmantoti, lai automātiski sadalītu budžeta plāna rindas darbplūsmas apstrādes laikā. Ja tiek izmantots stadijas sadalījums, budžeta plāna rindas mērķa scenārijā var veidot un izmainīt bez budžeta plāna sagatavotāja vai recenzenta iesaistīšanās.

Iestatot posmu sadalījumu, saistiet budžeta plānošanas darbplūsma un posmu ar sadalījuma grafiks. Budžeta plānošanas darbplūsmai ir jābūt saistītai ar budžeta plānošanas darbplūsmu, kas izmanto automatizēto darbplūsmas uzdevumu **Budžeta plānošana stadiju sadalījums**. Kad darbplūsma sasniedz norādīto stadiju, sadalīšana notiek automātiski. Automatizētu uzdevumu var izmantot, lai izveidotu budžeta plāna rindas jaunā scenārijā.

Piemēra shēmā, kas parādīta iepriekš šajā tēmā, sadalījums tiek veikts, lai pārsūtītu summas no budžeta plāna un scenārijiem galvenās pārvaldes "Bāzlīnijas" stadijā uz citu budžeta plānu un scenārijiem pārdošanas nodaļas "Novērtēšanas" stadijā. Šajā attēlā parādīta piemēra shēmas attiecīgā daļa.

[![Stadiju sadalījums.](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Stadijas sadalījums Turklāt piemēra shēmā tiek veikts apkopojums no budžeta plāniem un scenārijiem pārdošanas nodaļas "Iesniegšanas" stadijā uz pamatplānu galvenās pārvaldes "Apkopojuma" stadijā. Šajā attēlā parādīta piemēra shēmas attiecīgā daļa.

[![Apkopojums.](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioritātes

Budžeta plāna prioritātes varat izmantot pēc izvēles, lai definētu kategorijas un mērķus izveidotajiem budžeta plāniem. Prioritātes varat arī izmantot, lai organizētu, klasificētu un novērtētu vairākus budžeta plānus. Piemēram, varat izveidot budžeta plānošanas prioritāti veselībai un drošībai un pēc tam novērtēt budžeta plānus, kas ir piešķirti šai prioritātei. Varat arī budžeta plāniem piešķirt numuru, lai norādītu rangu.

### <a name="columns-and-layouts"></a>Kolonnas un izkārtojums

Budžeta vērtības tiek attēlotas budžeta plāna rindās un kolonnās. Vispirms jādefinē kolonnas un pēc tam varat izveidot izkārtojumu, lai definētu šo kolonnu attēlojumu.

Lai definētu kolonnu, atlasiet budžeta plāna scenāriju. Rindas summas no šī scenārija tiek rādītas budžeta plānā. Varat atlasīt periodu, lai filtrētu summu, un varat arī izmantot filtrus, kuru pamatā ir Virsgrāmatas konts.

Definējot izkārtojumu, atlasiet Virsgrāmatas dimensiju kopu, lai izveidotu budžeta plāna rindas, kuras vēlaties parādīt, un atlasiet kolonnas kā izkārtojuma elementus. Varat izveidot vairākus izkārtojumus, lai budžeta plānā tiek parādīti vēlamie dati dažādās budžeta plānošanas procesa stadijās.

Papildus budžeta summu kolonnām varat definēt kolonnas budžeta plāna laukiem par projektu, piedāvāto projektu, līdzekļiem un piedāvātajiem līdzekļiem. Varat arī definēt kolonnu paredzētajām budžeta pozīcijām. Šī opcija ir noderīga, ja ir nepieciešams analizēt personāla budžetu.

Piemēram shēmai, iespējams, vēlēsieties izveidot kolonnas scenārijiem "PY pārdošana," "Līgumi" un "Prognoze". (Šajā ilustrācijā parādīta shēmas atbilstošā sadaļa.) Pēc tam varat sadalīt visus vai vienu no šiem scenārijiem atsevišķās kolonnās katram finanšu gada ceturksnim, lai pārdošanas nodaļas vadītājs var precīzi ievadīt katra perioda prognozētās summas.

[![Shēmas sadaļu ilustrācija kolonnu pievienošanai.](./media/columns.png)](./media/columns.png)

Varat arī konkretizēt, vai katru izkārtojuma elementu (kolonnu) ir atļauts rediģēt un vai tas ir pieejams jebkurā darblapas veidnē, kas ir izveidota šim izkārtojumam. Piemēra shēmas izkārtojumā, kas tiek izmantots "Novērtēšanas" stadijā, "Prognožu" kolonnas ir rediģējamas, bet kolonnas "PY pārdošana" un "Līgumi" ir tikai lasāmas.

> [!NOTE]
> Pēc noklusējuma jums būs ierobežojums līdz 36 kolonnām, ja vien nepaplašināsit budžeta plānošanu ar šādām darbībām no sadaļas [Paplašināt budžetu plānošanas izkārtojumu](./extending-budget-planning-layout.md).

### <a name="templates"></a>Veidnes

Lapas **Budžeta plānošanas konfigurācija** sadaļā **Izkārtojumus** varat arī izveidot, apskatīt vai augšupielādēt Excel veidnes katram izkārtojumam. Šīs veidnes ir darbgrāmatas, kuras ir saistītas ar katru budžeta plānu, lai sniegtu papildu analīzi, diagrammas un datu ievades iespējas.

Ģenerējot veidni, izkārtojums tiek bloķēts, un to nevar rediģēt. Šī bloķēšana nodrošina, ka veidnes formāts atbilst budžeta plāna izkārtojumam un ietver tādus pašus datus. Pēc veidnes ģenerēšanas, to var apskatīt un rediģēt. Piemēram, varat veidnei pievienot diagrammas vai turpmāk pielāgot tās izskatu.

> [!NOTE]
> Veidne ir jāsaglabā vietā, kurai lietotājam ir piekļuve, tādējādi pēc rediģēšanas pabeigšanas to var augšupielādēt izkārtojumā. Šādi veidne tiks izmantota budžeta plāniem, kuri lieto šo izkārtojumu.

### <a name="descriptions"></a>Apraksti

Sadaļā **Izkārtojumi** varat piešķirt aprakstus, lai attēlotu nosaukumu finanšu dimensijai, kas ir iekļauta izkārtojumā. Piemēram, organizācija var vēlēties parādīt galvenā konta nosaukumu blakus galvenā konta numuram budžeta plānā. Tomēr var rasties nepieciešamība izlaist citu finanšu dimensiju nosaukumus, lai izvairītos no displeja pārblīvēšanas.

## <a name="setting-up-budget-planning-processes"></a>Budžeta plānošanas procesu iestatīšana

Kad esat pabeidzis konfigurēt budžeta plānošanu, varat iestatīt budžeta plānošanas procesus lapā **Budžeta plānošanas process**. Budžeta plānošanas procesi ir kārtulu kopas, kas nosaka budžeta plānu atjaunināšanas, maršrutēšanas, pārskatīšanas un apstiprināšanas veidu budžeta veidošanas organizācijas hierarhijā.

Katram budžeta plānošanas procesam sākumā atlasiet budžeta ciklu un Virsgrāmatu. Katrs budžeta plānošanas process ir saistīts tikai ar vienu budžeta ciklu un vienu Virsgrāmatu. Pēc tam atlasiet budžeta organizācijas hierarhiju kopsavilkuma cilnē **Budžeta plānošanas procesa administrācija** un piešķiriet budžeta plānošanas darbplūsmu visiem organizācijas atbildības centriem, kas parādās režģī.

Lai budžeta plānošanas darbplūsmu piešķirtu vai izmainītu līdzīgiem atbildības centriem, atlasiet **Piešķirt darbplūsmu** un pēc tam atlasiet vēlamo organizācijas veidu un izmantojamo budžeta plānošanas darbplūsmu. Budžeta veidošanas darbplūsmas ID, kas ir saistīts ar katru budžeta plānošanas darbplūsmā, tiek automātiski pievienots režģī.

Nosakot stadijas noteikumus un veidnes kopsavilkuma cilnē **Budžeta plānošanas stadijas noteikumi un izkārtojumi**, varat noteikt citu noteikumu un noklusējuma izkārtojumu kopumu katrai budžeta plānošanas stadijai. Piemēram, pārdošanas nodaļu "Novērtējuma" stadijā var ļaut lietotājiem modificēt budžeta plāna rindas, bet neļaut lietotājiem rindas pievienot. "Iesniegšanas" stadijā varat ļaut lietotājiem skatīt rindas, bet neļaut tās pievienot vai modificēt, jo šajā stadijā darbs ir pabeigts un ir jānovērš budžeta plānu izmaiņas. Lai atlasītu izkārtojumus, kas ir pieejami budžeta plāniem, atlasiet **Alternatīvie izkārtojumi**.

Ja vēlaties, varat atlasīt budžeta plānošanas prioritātes kopsavilkuma cilnē **Budžeta plāna prioritāšu ierobežojumi**. Prioritātes varat atlasīt budžeta plāniem.

Pēdējā darbība ir aktivizēt budžeta plānošanas procesu, izmantojot izvēlni **Darbības**. Budžeta plānošanas procesu nevar izmantot, kamēr tas nav aktivizēts.

Varat arī izmantot izvēlni **Darbības**, lai izveidotu jaunu procesu, kopējot jau esošu procesu. Šī iespēja ir noderīga organizācijām, kurās katrā budžeta ciklā tiek izpildīts viens un tas pats process, un tiek veikts maz izmaiņu vai izmaiņas netiek veiktas.

Cita noderīga komanda izvēlnē **Darbības** ir **Skatīt budžeta procesa statusu**. Šī komanda grafiski parāda budžeta plānus procesā, kā arī attiecīgos datus, piemēram, plānu darbplūsmu statusu, kopsavilkumus pēc summas un vienības, kā arī satur viena klikšķa navigācijas iespēju uz pašiem budžeta plāniem.

[![Budžeta plānošanas procesa statuss.](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
