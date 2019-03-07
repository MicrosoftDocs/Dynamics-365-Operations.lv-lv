---
title: Budžeta plānošanas pārskats
description: Šajā rakstā tiek iepazīstināts ar budžeta plānošanu, un tajā ir ietverta informācija, kas jums palīdz konfigurēt budžeta plānošanu un iestatīt budžeta plānošanas procesus.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a262b5200c8071bec78ff6d3ed7976d4b2057ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "329923"
---
# <a name="budget-planning-overview"></a>Budžeta plānošanas pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā tiek iepazīstināts ar budžeta plānošanu, un tajā ir ietverta informācija, kas jums palīdz konfigurēt budžeta plānošanu un iestatīt budžeta plānošanas procesus.

<a name="overview-of-budget-planning"></a>Budžeta plānošanas pārskats
---------------------------

Budžeta plānošana tiek veikta, kad sagatavojat budžetus, kurus ieviesīs organizācija. Organizācija var konfigurēt budžeta plānošanu un pēc tam iestatīt budžeta plānošanas procesus atbilstoši savai politikai, procedūrām un budžeta sagatavošanas prasībām. 

Kad sapratīsit programmā Microsoft Dynamics 365 for Finance and Operations izmantotos jēdzienus un terminoloģiju, varēsit vieglāk ieviest budžeta plānošanu savā organizācijā.

### <a name="key-terms"></a>Galvenie termini

-   **Budžeta plānošanas procesi** — nosaka budžeta plānu atjaunināšanas, maršrutēšanas, pārskatīšanas un apstiprināšanas veidu budžeta veidošanas organizācijas hierarhijā. Budžeta plānošanas process ir saistīts ar budžeta ciklu un organizāciju, izmantojot juridisku personu.
-   **Budžeta plāni** — satur budžeta datus, kas tiek izmantoti budžeta ciklam. Jums var būt vairāki budžeta plāni, kas tiek izmantoti dažādiem nolūkiem. Piemēram, budžeta plānus var izmantot, lai izveidotu budžeta summas dažādām organizācijas vienībām vai lai veiktu salīdzinājumus un pamatotus lēmumus.
-   **Budžeta plāna scenāriji** — definē datu kategorijas budžeta plānos. Definējiet budžeta plāna scenārijus, lai atbalstītu monetāro un citas mērvienību klases vienības, piemēram, daudzumu. Monetārā budžeta plāna scenāriju paraugi ir arī nodaļas iepriekšējā gada scenārijs un nodaļu pieprasījumu scenārijs. Budžeta plāna scenāriju piemēri, kuri izmanto daudzumus, ietver arī Iepriekšējā gada atbalsta zvani un Pilna laika ekvivalentu (PLE) skaits.
-   **Budžeta plānošanas stadijas** — definē posmus, kuriem iziet budžeta plāns no tā uzsākšanas līdz galīgās apstiprināšanas brīdim. Budžeta plānošanas stadijas ir sakārtotas budžeta plānošanas darbplūsmās.
-   **Budžeta plānošanas darbplūsmas** — sastāv no budžeta plānošanas stadijām un definē tās. Budžeta plānošanas darbplūsmas ir saistītas ar budžeta veidošanas darbplūsmām. Budžeta veidošanas darbplūsmas ir automatizēti un manuāli procesi, kas pārvieto budžeta plānus no vienas budžeta plānošanas stadijas uz citu.

[![Budžeta plānošanas terminoloģija](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Vispārīgie uzdevumi

Budžeta plānošanu var izmantot tālāk norādīto uzdevumu izpildei.

-   Izveidojiet budžeta plānus, lai noteiktu paredzamos ieņēmumus un izdevumus budžeta ciklā.
-   Analizējiet un atjauniniet budžeta plānus vairākiem scenārijiem.
-   Automātiski maršrutējiet budžeta plānus kopā ar darblapām, pamatojuma dokumentiem un citiem pielikumiem turpmākai pārskatīšanai un apstiprināšanai.
-   Konsolidējiet vairākus budžeta plānus no zemāka organizācijas līmeņa vienā pamata budžeta plānā augstākā organizācijas līmenī. Varat arī izstrādāt vienu budžeta plānu augstākā organizācijas līmenī un piešķirt budžetu zemākiem organizācijas līmeņiem.

Budžeta plānošana ir integrēta citos Microsoft Dynamics 365 for Finance and Operations moduļos. Tāpēc varat ietvert informāciju no iepriekšējiem budžetiem, faktiskajiem izdevumiem, pamatlīdzekļiem un cilvēkresursiem. Tā kā budžeta plānošana ir integrēta arī programmās Microsoft Excel un Microsoft Word, varat izmantot šīs programmas, lai strādātu ar budžeta plānošanas datiem. Piemēram, budžeta pārvaldnieks var eksportēt nodaļas budžeta pieprasījumu no budžeta plāna scenārija uz Excel darblapu. Datus var analizēt, atjaunināt un veido diagrammas darblapās un pēc tam publicēt budžeta plāna rindās.

## <a name="configuring-budget-planning"></a>Budžeta plānošanas konfigurēšana
Lapā **Budžeta plānošanas konfigurācija** ir lielākā iestatījumu daļa, kas jums nepieciešama, lai iestatītu budžeta plānošanu. Turpmākajās sadaļās aprakstīti galvenie faktori, kas jāņem vērā, kad konfigurējat budžeta plānošanu. Kad esat pabeidzis konfigurēšanu, uzstādiet budžeta plānošanas procesus.

### <a name="create-a-budget-planning-schema"></a>Budžeta plānošanas shēmas izveide

Neobligāts, bet ieteicams pirmais solis ir izveidot shēmu, kas parāda jūsu organizācijas budžeta formulēšanas procedūru. Šīs shēmas izveidei varat izmantot jebkuru metodi, kuru vēlaties. Šajā attēlā parādīts vispārīgs piemērs, kurā dažādiem organizācijas līmeņiem ir izveidotas atsevišķas budžeta plānošanas darbplūsmas. Katrā darbplūsmā tiek noteiktas stadijas, un katrai stadijai tiek piešķirti noteikti scenāriji, kas satur budžeta datus. Uzdevumi tiek veikti, lai pārvietotu datus no vienas stadijas uz nākamo. Piemēram, summas var tikt piesaistītas vai apkopotas dažādos kontos, apstiprinājumos vai citos pārskatos. Šajā piemērā teksts kursīvā apzīmē scenāriju, kas šajā stadijā nav rediģējams, vai datus, kas ir vēsturiski vai ir apstiprināti agrākā stadijā un tādēļ nav jāmaina. 

[![Budžeta plānošanas vispārīgā shēma](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Nākamajā piemērā galvenā pārvalde prognozē sākotnējās budžetā bāzlīnijas summas un izplata tās pārdošanas nodaļām. Pārdošanas nodaļas novērtē un iesniedz savas prognozes atpakaļ galvenajai pārvaldei, kur budžeta pārvaldnieks prognozi apkopo un pielāgo. Visbeidzot, budžeta pārvaldnieks nosūta koriģētās budžeta summas pārskatīšanai, galīgajiem pielāgojumiem un apstiprināšanai CFO. 

[![Budžeta plānošanas shēmas piemērs](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Organizācijas hierarhija budžeta plānošanai

Lapā **Organizācijas hierarhija** varat norādīt organizācijas hierarhiju par budžeta plānošanas hierarhiju katrā budžeta plānošanas procesā. Budžeta plānošanas hierarhijai nav jāatbilst standarta organizācijas hierarhijai, kas tiek izmantota citiem mērķiem. Tā kā šī hierarhija tiek izmantota, lai apkopotu un izplatītu datus, varat izvēlēties atšķirīgu struktūru. Piemēra shēmā pārdošanas nodaļas pakļaujas galvenās pārvaldes līmenim, kurā ir budžeta un finanšu nodaļas. Šī struktūra, iespējams, atšķiras no struktūras, kas tiek izmantota, lai pārvaldītu operācijas pārdošanas nodaļās. Katram budžeta plānošanas procesam var piešķirt tikai vienu organizācijas hierarhiju. 

Papildinformāciju skatiet rakstā [Organizācijas un organizāciju hierarhijas](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Lietotāja drošība

Budžeta plānošanai varat izmantot vienu no diviem drošības modeļiem, kas definē lietotāju atļaujas. Lai norādītu drošības modeli, iestatiet budžeta plānošanas parametru lapā **Budžeta plānošanas konfigurācija**.

### <a name="budget-planning-workflows-stages"></a>Budžeta plānošanas darbplūsmu stadijas

Lai pārvaldītu budžeta plānu izveidi un attīstību, tiek izmantotas budžeta plānošanas darbplūsmas un budžeta veidošanas darbplūsmas.

Budžeta plānošanas darbplūsmu sastāv no sakārtota posmu kopuma, pa kuru pārvietojas budžeta plāns. Katra budžeta plānošanas darbplūsma ir saistīta ar budžeta veidošanas darbplūsmu. Budžeta veidošanas darbplūsmas ir viens no programmatūrā Dynamics 365 for Finance and Operations izmantotajiem darbplūsmu veidiem. Budžeta veidošanas darbplūsmas maršrutē budžeta plānus kopā ar darblapām, pamatojumiem un pielikumiem organizācijas ietvaros to pārskatīšanai un apstiprināšanai. 

Budžeta plānošanas darbplūsmu iespējams izveidot lapas **Budžeta plānošanas konfigurācija** sadaļā **Darbplūsmas stadijas**. Tur varat atlasīt izmantojamās stadijas un budžeta veidošanas darbplūsmas, kā arī konfigurēt papildu iestatījumus. 

Laba prakse ir izveidot budžeta plānošanas darbplūsmu katrā budžeta veidošanas hierarhijas līmenī. Pēc tam piešķiriet budžeta veidošanas darbplūsmu, kas satur elementus, kuri atbilst budžeta plānošanas darbplūsmas stadijām. Piemēra shēmā, kas parādīta iepriekš šajā rakstā, viena budžeta plānošanas darbplūsma tiktu izveidota pārdošanas nodaļām un cita tiktu izveidota galvenajai pārvaldei. Budžeta veidošanas darbplūsmas pārvieto budžeta plānus no vienas stadijas uz citu. 

Budžeta veidošanas darbplūsmu budžeta plānošanai varat izveidot lapā **Budžeta veidošanas darbplūsmas**. Šis process līdzinās citu darbplūsmu izveidei programmatūrā Dynamics 365 for Finance and Operations. Šajā attēlā parādīts galvenās pārvaldes darbplūsmas piemērs. 

[![Budžeta veidošanas darbplūsma budžeta plānošanai](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Šī darbplūsma ietver elementus sadalīšanai uz pārdošanas nodaļām un to sniegtās informācijas apkopošanai, budžeta vadītāja veiktai pārskatīšanai, CFO veiktai apstiprināšanai un stadiju pārejām starp katru stadiju. 

Budžeta veidošanas darbplūsma tiek piešķirta katrai budžeta plānošanas darbplūsmai lapas **Budžeta plānošanas konfigurācija** sadaļā **Darbplūsmas stadijas**.

### <a name="parameters-scenarios-and-stages"></a>Parametri, scenāriji un stadijas

Sākotnējie iestatījumi lapā **Budžeta plānošanas konfigurācija** ļauj izveidot dažus veidošanas blokus vēlākām konfigurēšanas darbībām.

-   **Parametri** — definē drošības kārtulas, kuras vēlaties lietot budžeta plāniem un noklusējuma finanšu dimensijas, kas ir jāizmanto, kad lietotāji detalizē budžeta plānu scenāriju summas.
-   **Scenāriji** — ietver datu kategorijas, kuras vēlaties izmantot budžeta plānos. Definējiet budžeta plāna scenārijus, lai atbalstītu monetāro un citas mērvienību klases vienības, piemēram, daudzumu. Budžeta plānā scenāriji atspoguļo vienu budžeta plānošanas datu versiju. Monetārā budžeta plāna scenāriju paraugi ir arī Iepriekšējā gada pārdošana un Noslēgtie līgumi. Piemēri scenārijiem, kas izmanto daudzumus, ir arī Pārdošanas zvanu skaits un Pilna laika ekvivalents (PLE).
-   **Stadijas** — definē darbības, kurām seko budžeta plāns no sākuma līdz galīgajai apstiprināšanai. Budžeta plānošanas stadijas piemēri ir HQ apkopojums, CFO pārskatīšana un Gala.

### <a name="allocation-schedules"></a>Sadalījuma grafiki

Budžeta plānošanā varat sadalīt budžeta plāna rindu summas vai daudzumus no viena scenārija citā scenārijā, vai pat tajā pašā scenārijā. Piemēram, varat sadalīt tajā pašā scenārijā, ja vēlaties veikt izmaiņas finanšu dimensijās vai summu datumos šajā scenārijā. Sadalīšanu varat veikt budžeta plāna ietvaros vai no viena budžeta plāna uz citu. 

Sadalījuma grafiki automātiski sadala budžeta plāna rindas darbplūsmas apstrādes laikā. Varat veikt sadalījumu, izmantojot kādu no metodēm sarakstā **Sadalījuma metode**.

- <strong>Sadalīt pa periodiem</strong> — lai budžeta plāna rindas no avota budžeta plāna scenārija sadalītu mērķa scenārija periodos, izmantojiet periodu sadalījuma principu. <strong>Piezīme.</strong> Lai varētu sadalīt dažādos periodos, lapā *<strong><em>Perioda sadalījuma kategorijas</em></strong>* ir jāiestata periodu sadalījuma principi.
- <strong>Sadalīšana dimensijās</strong> — budžeta plāna rindas tiek sadalītas no avota budžeta plāna scenārija visās mērķa scenārija finanšu dimensijās. <strong>Piezīme.</strong> Lai varētu sadalīt dimensijās, lapā *<strong><em>Budžeta sadalījuma noteikumi</em></strong>* ir jāiestata budžeta sadalījuma noteikumi.
- **Apkopot** — budžeta plāna rindas tiek apkopotas no avota budžeta plāna scenārija saistītajos budžeta plānos uz mērķa scenāriju pamata budžeta plānā.
- **Sadalīt** — budžeta plāna rindas ir sadalītas no avota budžeta plāna scenārija pamata budžeta plānā uz mērķa scenāriju saistītajos budžeta plānos.
- **Izmantot Virsgrāmatas sadalījuma kārtulas** — budžeta plāna rindas tiek sadalītas no avota budžeta plāna scenārija uz mērķa scenāriju saskaņā ar atlasīto Virsgrāmatas sadalījuma kārtulu.
- **Kopēt no budžeta plāna** — varat atlasīt citu budžeta plānu, kas tiks izmantots par sadalījuma avotu.

### <a name="stage-allocations"></a>Stadijas sadalījumi

Stadijas sadalījumi tiek izmantoti, lai automātiski sadalītu budžeta plāna rindas darbplūsmas apstrādes laikā. Ja tiek izmantots stadijas sadalījums, budžeta plāna rindas mērķa scenārijā var veidot un izmainīt bez budžeta plāna sagatavotāja vai recenzenta iesaistīšanās.

Iestatot posmu sadalījumu, saistiet budžeta plānošanas darbplūsma un posmu ar sadalījuma grafiks. Budžeta plānošanas darbplūsmai ir jābūt saistītai ar budžeta plānošanas darbplūsmu, kas izmanto automatizēto darbplūsmas uzdevumu *<strong><em>Budžeta plānošanas stadiju sadalījums</em></strong>*. Kad darbplūsma sasniedz norādīto stadiju, sadalīšana notiek automātiski. Automatizētu uzdevumu var izmantot, lai izveidotu budžeta plāna rindas jaunā scenārijā. 

Piemēra shēmā, kas parādīta iepriekš šajā rakstā, sadalījums tiek veikts, lai pārsūtītu summas no budžeta plāna un scenārijiem galvenās pārvaldes bāzlīnijas stadijā uz citu budžeta plānu un scenārijiem pārdošanas nodaļas novērtēšanas stadijā. Šajā attēlā parādīta piemēra shēmas attiecīgā daļa.

[![Stadiju sadalījums](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Turklāt piemēra shēmā apkopojums tiek veikts no budžeta plāniem un scenārijiem pārdošanas nodaļas stadijā Iesniegts uz pamatplānu stadijā HQ apkopojums. Šajā attēlā parādīta piemēra shēmas attiecīgā daļa.

[![Apkopojums](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioritātes

Budžeta plāna prioritātes varat izmantot pēc izvēles, lai definētu kategorijas un mērķus izveidotajiem budžeta plāniem. Prioritātes varat arī izmantot, lai organizētu, klasificētu un novērtētu vairākus budžeta plānus. Piemēram, varat izveidot budžeta plānošanas prioritāti veselībai un drošībai un pēc tam novērtēt budžeta plānus, kas ir piešķirti šai prioritātei. Varat arī piešķirt skaitli, lai sarindotu visus budžeta plānus.

### <a name="columns-and-layouts"></a>Kolonnas un izkārtojums

Budžeta vērtības tiek attēlotas budžeta plāna rindās un kolonnās. Vispirms jādefinē kolonnas un pēc tam varat izveidot izkārtojumu, lai definētu kolonnu attēlojumu. 

Lai definētu kolonnu, atlasiet budžeta plāna scenāriju. Rindas summas no šī scenārija tiek rādītas budžeta plānā. Varat atlasīt periodu, lai filtrētu summu, un varat arī izmantot filtrus, kuru pamatā ir Virsgrāmatas konts. 

Definējot izkārtojumu, atlasiet Virsgrāmatas dimensiju kopu, lai izveidotu budžeta plāna rindas, kuras vēlaties parādīt, un atlasiet kolonnas kā izkārtojuma elementus. Varat izveidot vairākus izkārtojumus, lai budžeta plānā tiek parādīti dati, kurus vēlaties redzēt dažādās budžeta plānošanas procesa stadijās. 

Papildus budžeta summu kolonnām varat definēt kolonnas budžeta plāna laukiem par projektu, piedāvāto projektu, līdzekļiem un piedāvātajiem līdzekļiem. Varat arī definēt kolonnu paredzētajām budžeta pozīcijām. Šī opcija ir ļoti noderīga, ja ir nepieciešams analizēt personāla budžetu. 

Piemēra shēmā jūs varētu vēlēties izveidot kolonnas pārdošanai, līgumiem un prognožu scenārijiem (šajā attēlā parādīta attiecīgā shēmas daļa). Pēc tam varat sadalīt visus vai vienu no šiem scenārijiem atsevišķās kolonnās katram finanšu gada ceturksnim, lai pārdošanas nodaļas vadītājs var precīzi ievadīt katra perioda prognozētās summas.

[![Kolonnas](./media/columns.png)](./media/columns.png) 

Varat arī norādīt, vai katru izkārtojuma elementu (kolonnu) ir atļauts rediģēt un vai tas ir pieejams jebkurā darblapas veidnē, kas ir izveidota šim izkārtojumam. Piemēra shēmas izkārtojumā, kas tiek izmantots novērtēšanas stadijā, prognožu kolonnas ir rediģējamas, bet kolonnas pārdošana un līgumi ir tikai lasāmas.

### <a name="templates"></a>Veidnes

Lapas **Budžeta plānošanas konfigurācija** sadaļā **Izkārtojumus** varat arī izveidot, apskatīt vai augšupielādēt Excel veidnes. Šīs veidnes ir darbgrāmatas, kuras ir saistītas ar katru budžeta plānu, lai sniegtu papildu analīzi, diagrammas un datu ievades iespējas. 

Varat izveidot, skatīt vai augšupielādēt veidni katram izkārtojumam. Ģenerējot veidni, izkārtojums tiek bloķēts, un to nevar rediģēt. Šī bloķēšana sniedz garantiju, ka veidnes formāts atbilst budžeta plāna izkārtojumam un ietver tādus pašus datus. Pēc veidnes ģenerēšanas, to var apskatīt un rediģēt. Piemēram, varat veidnei pievienot diagrammas vai turpmāk pielāgot tās izskatu.

> [!NOTE] 
> Veidne ir jāsaglabā vietā, kurai lietotājam ir piekļuve, tādējādi pēc rediģēšanas pabeigšanas to var augšupielādēt izkārtojumā. Šādi veidne tiks izmantota budžeta plāniem, kuri lieto šo izkārtojumu.

### <a name="descriptions"></a>Apraksti

Apraksti, kurus varat piešķirt sadaļā **Izkārtojumi** tiek izmantoti, lai attēlotu nosaukumu finanšu dimensijai, kas ir iekļauta izkārtojumā. Piemēram, organizācija budžeta plānā blakus galvenā konta skaitlim var vēlēties parādīt galvenā konta nosaukumu, bet varētu vēlēties izlaist citu finanšu dimensiju nosaukumus, lai izvairītos no ekrāna pārblīvēšanas.

## <a name="setting-up-budget-planning-processes"></a>Budžeta plānošanas procesu iestatīšana

Kad esat pabeidzis konfigurēt budžeta plānošanu, varat iestatīt budžeta plānošanas procesus lapā **Budžeta plānošanas process**. Budžeta plānošanas procesi ir kārtulu kopas, kas nosaka budžeta plānu atjaunināšanas, maršrutēšanas, pārskatīšanas un apstiprināšanas veidu budžeta veidošanas organizācijas hierarhijā. 

Katram budžeta plānošanas procesam sākumā atlasiet budžeta ciklu un Virsgrāmatu. Katrs budžeta plānošanas process ir saistīts tikai ar vienu budžeta ciklu un vienu Virsgrāmatu. Tad atlasiet budžeta organizācijas hierarhiju kopsavilkuma cilnē **Budžeta plānošanas procesa administrācija** un piešķiriet budžeta plānošanas darbplūsmu visiem organizācijas atbildības centriem, kas parādās režģī. 

Lai budžeta plānošanas darbplūsmu piešķirtu vai izmainītu līdzīgiem atbildības centriem, noklikšķiniet uz **Piešķirt darbplūsmu** un pēc tam atlasiet vēlamo organizācijas veidu un izmantojamo budžeta plānošanas darbplūsmu. Budžeta veidošanas darbplūsmas ID, kas ir saistīts ar katru budžeta plānošanas darbplūsmu, tiek pievienots režģim automātiski. 

Nosakot stadijas noteikumus un veidnes kopsavilkuma cilnē **Budžeta plānošanas stadijas noteikumi un izkārtojumi**, varat noteikt citu noteikumu un noklusējuma izkārtojumu kopumu katrai budžeta plānošanas stadijai. Piemēram, pārdošanas nodaļas novērtējuma stadijā var ļaut lietotājiem modificēt budžeta plāna rindas, bet neļaut lietotājiem rindas pievienot. Iesniegšanas stadijā varat ļaut lietotājiem skatīt rindas, bet neļaut tās pievienot vai modificēt, jo šajā stadijā darbs ir pabeigts un ir jānovērš budžeta plānu izmaiņas. Lai atlasītu izkārtojumus, kas ir pieejami budžeta plāniem, noklikšķiniet uz **Alternatīvie izkārtojumi**. 

Ja vēlaties, varat atlasīt budžeta plānošanas prioritātes kopsavilkuma cilnē **Budžeta plāna prioritāšu ierobežojumi**. Prioritātes varat atlasīt budžeta plāniem. 

Pēdējais solis ir aktivizēt budžeta plānošanas procesu, izmantojot izvēlni **Darbības**. Budžeta plānošanas procesu nevar izmantot, līdz tas tiek aktivizēts. 

Izvēlnē **Darbības** varat arī izveidot jaunu procesu, kopējot jau esošu procesu. Šī iespēja ir noderīga organizācijām, kurās katrā budžeta ciklā tiek izpildīts viens un tas pats process, un tiek veikts maz izmaiņu vai izmaiņas netiek veiktas. 

Cita noderīga komanda izvēlnē **Darbības** ir **Skatīt budžeta procesa statusu**. Šī komanda grafiski parāda budžeta plānus procesā, kā arī attiecīgos datus, piemēram, plānu darbplūsmu statusu, kopsavilkumus pēc summas un vienības, kā arī satur viena klikšķa navigācijas iespēju uz pašiem budžeta plāniem.

[![Budžeta plānošanas procesa statuss](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)



