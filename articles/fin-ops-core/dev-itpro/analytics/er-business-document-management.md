---
title: Pārskats par biznesa dokumentu pārvaldību
description: Šajā tēmā ir sniegta informācija par to, kā izmantot biznesa dokumentu pārvaldības līdzekli elektroniskā pārskata struktūrā.
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a2fa6a7f6efef05862a3727a80122c22d591487
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824524"
---
# <a name="business-document-management-overview"></a>Biznesa dokumentu pārvaldības pārskats

Biznesa lietotāji izmanto [Elektronisko paziņojumu (EP) pārskatu struktūru](general-electronic-reporting.md), lai konfigurētu izejošo dokumentu formātus saskaņā ar dažādu valstu/reģionu juridiskajām prasībām. Lietotāji var arī definēt datu plūsmu, lai norādītu, kādus lietojumprogrammas datus ievietot ģenerētajos dokumentos. EP struktūra ģenerē izejošos dokumentus Microsoft Office formātos (Excel darbgrāmatas vai Word dokumentus), izmantojot iepriekš definētas veidnes. Veidnes tiek aizpildītas ar nepieciešamajiem datiem saskaņā ar konfigurēto datu plūsmu, kamēr tiek ģenerēti nepieciešamie dokumenti. Katru konfigurētu formātu var publicēt kā EP risinājuma daļu noteiktu izejošo dokumentu ģenerēšanai. To pārstāv EP formāta konfigurācija, kas var ietvert veidnes, ko var izmantot dažādu izejošo dokumentu ģenerēšanai. Biznesa lietotāji var izmantot šo struktūru, lai pārvaldītu nepieciešamos biznesa dokumentus.

**Biznesa dokumentu pārvaldība** ir izveidota uz ER struktūras un ļauj biznesa lietotājiem rediģēt biznesa dokumentu veidnes, izmantojot pakalpojumu Microsoft Office 365 vai atbilstošu datora lietojumprogrammu Microsoft Office. Dokumentu rediģējumiem ir jāietver biznesa dokumentu noformējumu izmaiņas un vietturu pievienošanu papildu datiem bez avota koda izmaiņām un jaunām izvietošanām. Lai atjauninātu biznesa dokumentu veidnes, nav nepieciešamas nekādas zināšanas par ER struktūru.

> [!NOTE]
> Biznesa dokumentu pārvaldība ļauj jums modificēt veidnes, kas tiek izmantotas tādu biznesa dokumentu izveidei kā pasūtījumi, rēķini utt. Kamēr veidne tika modificēta un tika publicēta tās jauna versija, šo versiju izmanto nepieciešamo biznesa dokumentu ģenerēšanai. Biznesa dokumentu pārvaldību nevar izmantot, lai modificētu jau ģenerētos biznesa dokumentus.

## <a name="supported-deployments"></a>Atbalstītie izvietojumi

Pašreiz biznesa dokumentu pārvaldības līdzeklis ir ieviests tikai mākoņa izvietojumiem. Ja šis līdzeklis ir kritisks jūsu lokālajam izvietojumam, ziņojiet mums, sniedzot atsauksmes vietnē [Idejas](https://experience.dynamics.com/ideas/).

## <a name="supported-microsoft-office-applications"></a>Atbalstītās Microsoft Office programmas

Lai izmantotu Biznesa dokumentu pārvaldību veidņu rediģēšanai Excel vai Word formātos, izmantojot Microsoft Office datora lietojumprogrammas, jums ir jābūt instalētai programmai Microsoft Office 2010 vai jaunākajai versijai. Tā tiek atbalstīta makonī un lokālajā izvietojumā.

## <a name="business-document-availability"></a>Biznesa dokumentu pieejamība

Šādi pārskati, kā arī uz Excel balstītās veidnes, būs pieejami, izlaižot tos publiskai atsauksmju sniegšanai:

**Debitori** (2019. gada augusts)

- Pārdošanas avansa rēķins
- Pārdošanas pasūtījuma pavadzīme

**Kreditori** (2019. gada augusts)

- Pirkšanas avansa rēķins
- Pirkšanas pasūtījums
- Pirkšanas pasūtījuma pavadzīme

Vairāk pārskatu kļūs pieejami. Īpaši paziņojumi par papildu pārskatiem tiks nosūtīti atsevišķi. 

Pilns saraksts ar visiem pārskatiem, kas ieplānoti 2019. gada oktobra laidienam, ir atrodams rakstā [Konfigurējamas biznesa dokumentu atskaites Word un Excel formātā](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details). Lai iegūtu papildinformāciju par šo līdzekli, aizpildiet šajā tēmā sniegto piemēru.

## <a name="configure-er-parameters"></a>Konfigurējiet ER parametrus

Tā kā Biznesa dokumentu pārvaldība ir izveidota, balstoties uz ER struktūru, jums ir jākonfigurē ER parametri, lai sāktu darbu ar Biznesa dokumentu pārvaldību. Lai to paveiktu, ir nepieciešams iestatīt EP parametrus, kā aprakstīts rakstā [Elektronisko paziņojumu (EP) struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md). Ir nepieciešams pievienot jaunu konfigurācijas sniedzēju, kā aprakstīts rakstā [Konfigurācijas sniedzēju izveide un to atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER darbvieta](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>ER risinājumu importēšana

Šīs procedūras piemērā tiek izmantoti parauga EP konfigurācijas. Jums ir jāimportē jūsu pašreizējā Dynamics 365 Finance instancē tās EP konfigurācijas, kas ietver biznesa dokumentu veidnes, kuras var rediģēt, izmantojot biznesa dokumentu pārvaldību. Lejupielādējiet un pēc tam lokāli saglabājiet tālāk norādītos failus šīs procedūras pabeigšanai.

**ER debitoru rēķinu risinājuma paraugs**

| **Fails**                                  | **Saturs**                                |
|-------------------------------------------|--------------------------------------------|
| Customer invoicing model.version.2.xml    | [ER datu modeļa konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [Brīva teksta rēķina ER formāta konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**ER maksājumu čeku risinājuma paraugs**

| **Fails**                                  | **Saturs**                                |
|-------------------------------------------|--------------------------------------------|
| Model for cheques.version.10.xml          | [ER datu modeļa konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml  | [Maksājuma čeka ER formāta konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**ER ārējās tirdzniecības risinājuma paraugs**

| **Fails**                                  | **Saturs**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat model.version.1.xml             | [ER datu modeļa konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml          | [Intrastat kontroles pārskata ER formāta konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Izmantojiet šādu procedūru katra faila importēšanai. Importējiet katra ER risinājuma ER *datu modeļa* konfigurāciju iepriekš minētajās tabulās, pirms atbilstošās ER *formāta* konfigurācijas importēšanas.

1. Atveriet sadaļu **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> lapu **Konfigurācijas**.
2. Lapas augšdaļā atlasiet **Maiņa**.
3. Atlasiet **Ielādēt no XML faila**.
4. Atlasiet **Pārlūkot**, lai ielādētu nepieciešamo XML failu.
5. Atlasiet **Labi**, lai apstiprinātu konfigurācijas importēšanu.

![ER konfigurāciju lapa](./media/BDM-Overview-ERSolutions.png)


Jūs varat arī importēt oficiāli publicētās EP formāta konfigurācijas no Microsoft Dynamics Lifecycle Service (LCS). Piemēram, lai pabeigtu šo procedūru, varat importēt **Brīvā teksta rēķina (Excel)** EP formāta konfigurācijas jaunāko versiju. Atbilstošais EP datu modelis un EP modeļu kartēšanas konfigurācijas tiks importētas automātiski.

![LCS koplietojamo līdzekļu bibliotēkas satura lapa](./media/BDM-Overview-SharedAssetLibrary.png)

Lai iegūtu papildinformāciju par ER konfigurāciju importēšanu, skatiet [ER konfigurācijas dzīves cikla pārvaldība](general-electronic-reporting-manage-configuration-lifecycle.md).


## <a name="enable-business-document-management"></a>Biznesa dokumentu pārvaldības iespējošana

Lai sāktu Biznesa dokumentu pārvaldību, ir jāatver darbvieta **Funkcionalitātes pārvaldība** un jāiespējo funkcionalitāte **Biznesa dokumentu pārvaldība**.

Izmantojiet šādu procedūru, lai iespējotu Biznesa dokumentu pārvaldības funkcionalitāti visām juridiskām personām.

1. Atveriet darbvietu **Funkcionalitātes pārvaldība**.
2. Cilnē **Jauns** sarakstā atlasiet funkcionalitāti **Biznesa dokumentu pārvaldība**.
3. Atlasiet **Iespējot tūlīt**, lai ieslēgtu atlasīto funkcionalitāti.
4. Atsvaidziniet lapu, lai piekļūtu jaunajam līdzeklim.

>[!NOTE]
> Jums ir arī jāiespējo **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai**, lai varētu izmantot jaunu biznesa dokumentu pārvaldības interfeisu

![Līdzekļu pārvaldības darbvieta](./media/BDM-Overview-FMEnabling.png)

Papildinformāciju par jaunu līdzekļu aktivizēšanu skatiet rakstā [Pārskats par līdzekļu pārvaldību](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Konfigurēt parametrus

Izmantojiet tālāk norādītajās sadaļās redzamo informāciju, lai iestatītu pamatparametrus Biznesa dokumentu pārvaldībai.

### <a name="prerequisites-for-parameter-setup"></a>Parametru iestatīšanas priekšnosacījumi
Pirms Biznesa dokumentu pārvaldības iestatīšanas, ir jāiestata nepieciešamais dokumenta tips Dokumentu pārvaldības struktūrā. Šo dokumenta tipu lieto, lai norādītu dokumentu pagaidu glabāšanu Office formātos (Excel un Word), kas izmantoti kā veidnes ER pārskatiem. Pagaidu glabāšanas veidni var rediģēt, izmantojot Office datora lietojumprogrammas.

Šim dokumenta tipam ir jāatlasa šādas atribūtu vērtības.

| **Atribūta nosaukums**  | **Atribūta vērtība**   |
|---------------------|-----------------------|
| Klase               | Pievienot failu           |
| Grupa               | Fails                  |
| Vieta            | SharePoint            |

Lai iegūtu papildu informāciju, kā iestatīt nepieciešamos dokumentu pārvaldības parametrus un dokumentu tipus, skatiet [Dokumentu pārvaldības konfigurācija](../../fin-ops/organization-administration/configure-document-management.md).

![Iestatiet Dokumentu pārvaldības dokumentu tipu](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a>Iestatīšanas parametri

Pamata Biznesa dokumentu pārvaldības parametrus var iestatīt lapā **Biznesa dokumentu parametri**. Lapai var piekļūt tikai noteikti lietotāji. Tā ietver:

- Lietotāji, kuriem piešķirta **Sistēmas administratora** loma.
- Lietotāji, kuriem ir piešķirta jebkāda loma, kas ir konfigurēta pienākuma izpildei **Uzturēt Biznesa dokumentu pārvaldības parametrus** (lietojumprogrammas objektu koka (AOT) nosaukums **ERBDMaintainParameters**).

Izmantojiet šādu procedūru pamata parametru iestatīšanai visām juridiskām personām.

1. Pierakstieties kā lietotājs ar piekļuvi lapai **Biznesa dokumentu parametri**.
2. Pārejiet uz sadaļu **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Biznesa dokumentu pārvaldība** \> **Biznesa dokumentu parametri**.
3.  Lapā **Biznesa dokumentu parametri** cilnē **Pielikumi**, laukā **SharePoint document tips** definējiet dokumenta tipu, ko izmantot veidņu pagaidu glabāšanai Office formātos, kamēr tiek rediģēti, izmantojot Office datora lietojumprogrammas. 

> [!NOTE]
> Šim parametram ir pieejami tikai dokumentu tipi, kas konfigurēti, izmantojot SharePoint atrašanās vietu.

![Biznesa dokumentu pārvaldības parametru iestatīšana](./media/BDM-Overview-BDMSetting.png)

Izvēlētais dokumenta tips ir raksturīgs uzņēmumam un tiks izmantots, kad lietotājs strādā ar Biznesa dokumentu pārvaldību uzņēmumā, kuram atlasītais dokumenta veids ir konfigurēts. Ja lietotājs strādā ar Biznesa dokumentu pārvaldību citā uzņēmumā, tiks izmantots tāds pats atlasītais dokumenta tips, ja šim uzņēmumam tāds netika konfigurēts. Ja dokumenta tips tika konfigurēts, tas tiks izmantots laukā **SharePoint dokumenta tips** atlasītā dokumenta tipa vietā.

## <a name="configure-access-permissions"></a>Piekļuves atļauju konfigurēšana

Pēc noklusējuma, ja Biznesa dokumentu pārvaldības atļaujas nav iespējotas, katrs lietotājs, kuram ir piekļuve Biznesa dokumentu pārvaldības darbvietai, redzēs visas ER risinājuma veidnes, kas ir pieejamas. Biznesa dokumentu pārvaldības darbvietā būs parādīti tikai tās veidnes, kuras atrodamas ER formāta konfigurācijās un kuras atzīmētas kā **Biznesa dokumentu tips**.

![ER konfigurāciju lapa](./media/BDM-Overview-ERFormatTags.png)

Veidņu sarakstu, kas pieejams Biznesa dokumentu pārvaldības darbvietā, var ierobežot, konfigurējot piekļuves atļaujas. Tas var būt svarīgi, kad dažādas veidnes tiek izmantotas biznesa dokumentu izveidei dažādiem biznesa domēniem (funkcionālajiem apgabaliem) un jūs vēlaties atļaut noteiktiem lietotājiem piekļūt dažādām veidnēm rediģēšanai Biznesa dokumentu pārvaldības darbvietā.

Biznesa dokumentu pārvaldības piekļuves atļaujas var iestatīt sadaļā **Piekļuves parametru konfigurētājs**. Lapai var piekļūt tikai šādi lietotāji:

- Lietotāji, kuriem piešķirta **Sistēmas administratora** loma.
- Lietotāji, kuriem ir piešķirta jebkāda cita loma, kas ir konfigurēta pienākuma izpildei **Konfigurēt atļaujas, lai piekļūtu Biznesa dokumentu veidnēm rediģēšanas veikšanai** (lietojumprogrammas objektu koka (AOT) nosaukums **ERBDTemplatesSecurity**).

Izmantojiet šādu procedūru, lai iestatītu Biznesa dokumentu pārvaldības atļaujas visām juridiskām personām.

1. Pierakstieties kā lietotājs ar piekļuvi lapai **Biznesa dokumentu parametri**.
2. Pārejiet uz sadaļu **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Biznesa dokumentu pārvaldība** \> **Pārvaldīt piekļuves atļaujas**.

    Pievērsiet uzmanību informatīvajam paziņojumam par to, ka piekļuves atļauju izmantošana Biznesa dokumentu pārvaldībai pašlaik nav iespējota.

    ![Biznesa dokumentu pārvaldības piekļuves lapas konfigurētājs](./media/BDM-Overview-TemplatesAccess1.png)

    Izmantojot šo iestatījumu, katrs lietotājs, kam piešķirta jebkāda drošības loma, konfigurēta pienākuma **Pārvaldīt Biznesa dokumentu veidnes** (AOT nosaukums **ERBDManageTemplates**) veikšanai, spēj atvērt Biznesa dokumentu pārvaldības darbvietu un var rediģēt jebkādu veidni, kas ir pieejama.

    Tālāk redzamā grafika parāda, kas ir pieejams Biznesa dokumentu pārvaldības darbvietā lietotājiem, kam piešķirta loma **Debitoru parādu darbinieks**. Ar pašreizējo piekļuves atļauju iestatījumu lietotājs var rediģēt biznesa dokumentu veidnes no dažādām funkcionālajām jomām, tostarp rēķinu izrakstīšanu, regulēšanas pārskatu veidošanu un maksājumus.

    ![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-TemplatesForAlice1.png)

3. Lapā **Piekļuves atļauju konfigurētājs** atlasiet **Piekļuves atļauju iestatījums**.
4. Dialoglodziņā **Piekļuves atļauju iestatījumi veidņu rediģēšanai** iespējojiet opciju **Piemērot konfigurētās piekļuves atļaujas**.
5. Atlasiet **Labi**, lai apstiprinātu, ka Biznesa dokumentu pārvaldības piekļuves atļaujas tika iespējotas.

    ![Biznesa dokumentu pārvaldības piekļuves atļauju lapa](./media/BDM-Overview-TemplatesAccess2.png)

6. Atlasiet **Pievienot**, lai ievadītu jaunu biznesa lomu, kurai ir jākonfigurē atļaujas, lai piekļūtu Biznesa dokumentu pārvaldības veidnēm.
7. Dialoglodziņā **Drošības lomas** atlasiet lomu **Debitoru parādu darbinieks** un pēc tam atlasiet **Labi**, lai apstiprinātu lomas atlasi.
8. Cilnē **Piekļuves atļaujas konfigurāciju atzīmēm** atlasiet **Jauns**.
9. Laukā **Atzīmes tips** atlasiet **Funkcionālais apgabals** un laukā **ID** atlasiet **Rēķinu izrakstīšana**.
10. Atlasiet **Saglabāt** konfigurēto piekļuves atļauju glabāšanai atlasītajai lomai.

    Pašreizējais iestatījums nozīmē, ka jebkuram lietotājam, kuram piešķirta loma **Debitoru parādu darbinieks** un pienākuma **Pārvaldīt Biznesa dokumentu veidnes** (AOT nosaukums **ERBDManageTemplates**) izpilde, ER formāta konfigurācijas veidnes ar vērtību **Rēķina izrakstīšana** atzīmei **Funkcionālais apgabals** būs pieejamas rediģēšanai Biznesa dokumentu pārvaldības darbvietā.

11. Pašreizējās lapas labajā pusē pārslēdziet rūti **Saistītā informācija**. Rūts **Saistītā informācija** parāda, kā tiks piemērotas konfigurētās piekļuves atļaujas, tostarp kādas ER konfigurācijas veidnes būs pieejamas lietotājiem, kuriem piešķirta loma **Debitoru parādu darbinieks**.

    ![Biznesa dokumentu pārvaldības piekļuves atļauju lapa](./media/BDM-Overview-TemplatesAccess3.png)

12. Cilnē **Piekļuves atļaujas konfigurācijām** atlasiet opciju **Pievienot**.
13. Dialoglodziņā **Atlasīt konfigurāciju** atzīmējiet ER formāta konfigurāciju **Intrastat pārskats**.
14. Atlasiet **Labi**, lai apstiprinātu atlasīto konfigurāciju ierakstu, un pēc tam atlasiet **Saglabāt**, lai saglabātu konfigurētās piekļuves atļaujas atlasītajai lomai.

Pašreizējais iestatījums nozīmē, ka jebkuram lietotājam, kuram piešķirta loma **Debitoru parādu darbinieks** un pienākuma **Pārvaldīt Biznesa dokumentu veidnes** (AOT nosaukums **ERBDManageTemplates**) izpilde, būs pieejamas tālāk norādītās veidnes rediģēšanai Biznesa dokumentu pārvaldības darbvietā:

- Veidnes ar vērtību **Rēķina izrakstīšana** atzīmei **Funkcionālais apgabals**.
- Veidnes no ER formāta konfigurācijām ir uzskaitītas cilnē **Piekļuves atļaujas konfigurācijām** (šajā piemērā veidnes no **Intrastat pārskata** formāta konfigurācijas domēnā **Likumā noteiktie pārskati** ).

![Biznesa dokumentu pārvaldības piekļuves atļauju lapa](./media/BDM-Overview-TemplatesAccess4.png)

Tālāk redzamā grafika parāda, kas ir pieejams Biznesa dokumentu pārvaldības darbvietā lietotājam, kam piešķirta loma **Debitoru parādu darbinieks**. Ar pašreizējo Biznesa dokumentu pārvaldības piekļuves atļauju iestatījumu lietotājs var rediģēt biznesa dokumentu veidnes no domēna **Rēķina izrakstīšana** un ER formāta konfigurācijas **Intrastat pārskats**. Veidnes no domēna **Maksājumi** nav pieejamas lomai **Debitoru parādu darbinieks**.

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> Kārtulas **Piekļuves atļaujas konfigurācijām** tiek glabātas, izmantojot ER formāta konfigurācijas unikālo identifikācijas ID. Tas nozīmē, ka šīs kārtulas netiks dzēstas, izdzēšot uz tām attiecināmo ER konfigurāciju. Importējot dzēstas konfigurācijas atpakaļ uz šo instanci, šīs kārtulas atkal tiks uz tiem attiecinātas. Nav nepieciešams iestatīt kārtulas vēlreiz pēc tam, kad izdzēstas konfigurācijas tiek vēlreiz importētas.

## <a name="use-business-document-management-to-edit-templates"></a>Biznesa dokumentu pārvaldības izmantošana veidņu rediģēšanai

Biznesa lietotāji var piekļūt biznesa dokumentu veidnēm rediģēšanai Biznesa dokumentu pārvaldības darbvietā. Tikai šādi lietotāji var piekļūt Biznesa dokumentu pārvaldības darbvietai:

- Lietotāji, kuriem piešķirta loma **Sistēmas administrators**.
- Lietotāji, kuriem ir piešķirta jebkāda loma, kas ir konfigurēta pienākuma izpildei **Uzturēt Biznesa dokumentu pārvaldības parametrus** (AOT nosaukums **ERBDManageTemplates**).

Izmantojiet šādu procedūru, lai rediģētu brīva teksta rēķinu veidnes Biznesa dokumentu pārvaldības darbvietā. Pirms pabeigt šo procedūru, jums ir jāpabeidz visas iepriekšējās procedūras šajā tēmā.

1. Pierakstieties kā lietotājs ar piekļuvi Biznesa dokumentu pārvaldības darbvietai.
2. Atveriet Biznesa dokumentu pārvaldības darbvietu

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-EditingTemplate1.png)

Cilnē **Veidne** redzams atlasītās veidnes saturs. Atlasiet cilni **Detalizēti**, lai pārskatītu atlasītās veidnes papildinformāciju, kā arī papildinformāciju ER formāta konfigurācijai, kurā šī veidne atrodas. Ievērojiet, ka visām veidnēm ir statuss **Publicēts** un tajās nav papildinformācijas kolonnā **Pārskatījums**. Tas nozīmē, ka šīs veidnes šobrīd netiek rediģētas.

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Sāciet rediģēt veidnes, kas pieder jūsu konfigurācijas sniedzējam

1. Biznesa dokumentu pārvaldības darbvietā no saraksta atlasiet veidni **Čeku drukāšanas formāts**.
2. Atlasiet cilni **Detalizēti**.

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-EditingTemplate2.png)

Atlasītajai veidnei ir pieejama opcija **Rediģēt veidni**. Šī opcija vienmēr ir pieejama veidnei ER formāta konfigurācijā, kas pieder aktīvajam ER konfigurācijas sniedzējam (šajā piemērā **“Litware, Inc.”** ). Kad ir atlasīta opcija **Rediģēt veidni**, esošā veidne no pamatā esošās ER formāta konfigurācijas melnraksta versijas būs pieejama rediģēšanai.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Sāciet rediģēt veidnes, kas pieder citiem nodrošinātājiem

1. Biznesa dokumentu pārvaldības darbvietā atlasiet **Jauns dokuments**

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM_overview_new_template1.png)

2. Atlasiet dokumentu, kuru vēlaties izmantot kā veidni.

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM_overview_new_template2.png)

3. Noklikšķiniet uz **Izveidot dokumentu**
4. Laukā **Virsraksts** izmainiet rediģējamās veidnes virsrakstu, ja nepieciešams. Teksts tiks izmantots automātiski izveidotās ER formāta konfigurācijas nosaukumam. Ievērojiet, ka šīs konfigurācijas (**Klientu FTI pārskats (GER) Kopija**) melnraksta versija, kas ietvers rediģēto veidni, automātiski tiks atzīmēta šī ER formāta izmantošanai pašreizējam lietotājam. Tajā pašā laikā nemainītā sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai jebkādam citam lietotājam.
5. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
6. Laukā **Komentārs** nomainiet piezīmi nosaukumu rediģējamās veidnes automātiski izveidotajai pārskatīšanai.
7. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM_overview_new_template3.png)

Opcija **Jauns dokuments** vienmēr ir pieejama veidnei ER formāta konfigurācijā, kas pieder citam nodrošinātājam (šajā piemērā Microsoft). Noklikšķinot uz **Jauns dokuments** dokuments, jūs redzat visas veidnes, kas pieder pašreizējiem un citiem nodrošinātājiem. Pēc veidnes izvēlēšanās tā būs atvērta rediģēšanai. Rediģētā veidne būs saglabāta jaunā ER formāta konfigurācijā, kas ģenerēta automātiski.

### <a name="start-editing-a-template"></a>Sāciet veidnes rediģēšanu

1. Atlasītajā veidnē atlasiet **Rediģēt dokumentu**.
2. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
3. Laukā **Komentārs** nomainiet piezīmi nosaukumu rediģējamās veidnes automātiski izveidotajai pārskatīšanai.

    ![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM_overview_new_template4.png)

5. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

**BDM veidnes redaktors** lapa atversies. Atlasītā veidne būs pieejama rediģēšanai tiešsaistē, izmantojot programmu Office 365.

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a>Rediģējiet veidni programmā Office 365

Modificējiet veidni, izmantojot programmas Office 365 funkcionalitāti. Piemēram, programmā Office online izmaniet lauku uzvedņu fontu veidnes virsrakstā no **Parasts** uz **Treknraksts**. Šīs izmaiņas tiek automātiski saglabātas rediģējamajai veidnei, kas ir glabāta primārajā veidnes krātuvē (pēc noklusējuma Azure BLOB krātuvē), kas konfigurēta ER struktūrai.

![Biznesa dokumentu pārvaldības veidņu rediģēšanas lapa](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a>Rediģējiet veidni datora lietojumprogrammā Office

1. Atlasiet opciju **Atvērt datora lietojumprogrammu**, lai modificētu veidni, izmantojot datora lietojumprogrammas Office (šajā piemērā Excel) funkcionalitāti. Rediģējamā veidne tiek kopēta no pastāvīgās krātuves uz pagaidu krātuvi, kas Biznesa dokumentu pārvaldības parametros ir konfigurēta kā SharePoint mape.
2. Apstipriniet, ka vēlaties atvērt veidni no pagaidu failu krātuves Office datora lietojumprogrammā Excel.

    ![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-EditingLayout3.png)

3. Modificējiet veidni. Piemēram, izmaniet lauku uzvedņu fontu veidnes virsrakstā no **Melnās** uz **Zilo** krāsu.

    ![Biznesa dokumentu pārvaldības veidņu rediģēšanas lapa](./media/BDM-Overview-EditingLayout4.png)

4. Atlasiet **Saglabāt** datora lietojumprogrammā Excel, lai saglabātu veidņu izmaiņas pagaidu krātuvē.

    ![Biznesa dokumentu pārvaldības veidņu rediģēšanas lapa](./media/BDM-Overview-EditingLayout5.png)

5. Aizveriet datora lietojumprogrammu Excel.
6. Atlasiet **Sinhronizētu saglabāto kopiju**, lai sinhronizētu pagaidu veidņu krātuvi ar pastāvīgu veidņu krātuvi.

> [!NOTE]
> Rediģējamās veidnes kopija pagaidu failu krātuvē tiek glabāta tikai veidņu rediģēšanas pašreizējai sesijai. Kad pabeidzat šo sesiju, aizverot lapu **BDM veidņu redaktors**, šī kopija tiks dzēsta. Ja pielāgojāt veidni pagaidu failu krātuvē un neesat atlasījis **Sinhronizēto saglabāto kopiju**, mēģinot aizvērt lapu **BDM veidņu redaktors**, parādīsies ziņojums ar jautājumu, vai vēlaties saglabāt ieviestās izmaiņas. Atlasiet **Jā**, ja vēlaties saglabāt izmaiņas veidnē pastāvīgā faila atrašanās vietā.

### <a name="validate-a-template"></a>Validējiet veidni

1. Lapā **BDM veidņu redaktors** atlasiet **Problēmu meklēšana**, lai validētu modificētu veidni attiecībā pret pamatā esošo ER formāta konfigurāciju. Izpildiet ieteikumus (ja ir), lai pielāgotu veidni formāta struktūrai no pamata ER formāta konfigurācijas.
2. Atlasiet **Rādīt formātu**, lai skatītu formāta pašreizējo struktūru no pamata ER formāta konfigurācijas, kas jāpielāgo rediģējamajai veidnei. 
3. Atlasiet **Slēpt formātu**, lai aizvērtu rūti.

    ![BDM BDM veidnes redaktora lapa](./media/BDM-Overview-EditingTemplate6.png)

4. Aizveriet lapu **BDM veidnes redaktors**.

Atjauninātā veidne tiek rādīta cilnē **Veidne**. Ievērojiet, ka rediģētās veidnes statuss tagad ir **Melnraksts** un pašreizējā pārskatīšana vairs nav tukša. Tas nozīmē, ka ir sācies šīs veidnes rediģēšanas process.

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Modificētās veidnes testēšana 

1. Programmā, mainiet uz uzņēmumu, **USMF**.
2. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
3. Atlasiet rēķinu **FTI-00000002** un pēc tam atlasiet **Drukāšanas pārvaldība**.
4. Atlasiet **Modulis — debitori** \> **Dokumenti** \> **Brīva teksta rēķins** \> līmeni **Sākotnējais dokuments**, lai norādītu rēķinu tvērumu apstrādei.
5. Laukā **Pārskata formāts** atlasiet ER formātu **Klientu FTI pārskats (GER) Kopija** norādītā dokumenta līmenim.

    ![Drukāšanas pārvaldības iestatījumu lapa](./media/BDM-Overview-TestRun1.png)

6. Nospiediet taustiņu **Escape**, lai aizvērtu pašreizējo lapu.
7. Atlasiet **Drukāt** un pēc tam nospiediet uz **Atlasīts**.
8. Lejupielādējiet dokumentu un atveriet to, izmantojot datora lietojumprogrammu Excel.

![Brīva teksta rēķinu lapa](./media/BDM-Overview-TestRun2.png)

Modificētā veidne tiek izmantota, lai ģenerētu brīva teksta rēķina pārskatu atlasītajam vienumam. Lai analizētu, kā šo pārskatu ietekmēja jūsu ieviestās izmaiņas veidnē, varat palaist šo pārskatu vienā lietojumprogrammas sesijā uzreiz pēc tam, kad esat modificējis veidni citā lietojumprogrammas sesijā.

### <a name="create-an-alternative-template-revision"></a>Alternatīvās veidnes pārskatīšanas izveide

1. Atveriet lapu **BDM veidnes redaktors** un atlasiet veidni **Klientu FTI pārskats (GER) Kopija**.
2. Cilnē **Pārskatīšanas** atlasiet **Jauns**.
3. Ja nepieciešams, laukā **Nosaukums** nomainiet nosaukumu otrai pārskatīšanai un balstiet to uz pašreiz aktīvu pirmo pārskatīšanu.
4. Ja nepieciešams, laukā **Komentārs** nomainiet piezīmi rediģējamās veidnes automātiski izveidotajai pārskatīšanai.

    ![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-AddRevision.png)

    Esat izveidojis veidnes jaunu pārskatīšanu, kas tika saglabāta pastāvīgā veidnes krātuvē. Tagad varat turpināt rediģēt otrās pārskatīšanas veidni, kas pašlaik ir atlasīta kā aktīva.

5. Atlasiet pirmo pārskatīšanu un pēc tam atlasiet **Iestatīt kā aktīvu**. Varat atlasīt citu pārskatīšanu ka aktīvu, ja jebkurā laikā vēlaties atgriezties pie šīs veidnes pārskatīšanas.
6. Atlasiet otro pārskatīšanu un pēc tam atlasiet **Dzēst**.
7. Atlasiet **Labi**, lai apstiprinātu, ka vēlaties dzēst atlasīto pārskatīšanu. Varat dzēst jebkādas neaktīvas pārskatīšanas, kad tās vairāk nav nepieciešamas.

### <a name="delete-a-modified-template"></a>Modificētās veidnes dzēšana

1. Lapā **BDM veidnes redaktors** atlasiet cilni **Veidne**.
2. Atlasiet **Dzēst**.
3. Ja izvēlaties **Labi** dzēšanas apstiprināšanai, tiks dzēsta ER formāts **Klientu FTI pārskats (GER) Kopija** ar modificētu veidni. Atlasiet **Atcelt** citu opciju izpētei.

### <a name="revoke-changes-of-template"></a>Veidnes izmaiņu atsaukšana

Rediģējot ER formāta veidni, kas pieder pašreizējam aktīvajam nodrošinātājam, jums būs piedāvāta opcija atsaukt veidnē veiktās izmaiņas.

![Biznesa dokumentu pārvaldības darbvietas lapa](./media/BDM-Overview-RevokeChanges.png)

1. Lapā **BDM veidnes redaktors** atlasiet cilni **Veidne**.
2. Atlasiet **Atsaukt**.
3. Izvēloties **Labi** veidnē veikto izmaiņu atcelšanai, modificētā veidne tiks aizstāta ar sākotnējo veidni un visas izmaiņas tiks noņemtas. Kad atsaucat izmaiņas veidnē, varēsiet dzēst veidni. Atlasiet **Atcelt** citu opciju izpētei.

### <a name="publish-a-modified-template"></a>Modificētās veidnes publicēšana
1. Lapā **BDM veidnes redaktors** cilnē **Veidne** atlasiet **Publicēt**.
2. Izvēloties **Labi** publicēšanas apstiprināšanai, atvasinātā ER formāta **Customer FTI report (GER) Copy** melnraksta versija, kas satur modificēto veidni, tiks atzīmēta kā pabeigta. Modificētā veidne kļūst pieejama citiem programmas lietotājiem. ER formāta pabeigtās versijas saglabās tikai jūsu veidnes pēdējo aktīvo pārskatīšanu. Citas pārskatīšanas tiks dzēstas. Atlasiet **Atcelt** citu opciju izpētei.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

#### <a name="i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a>Esmu izvēlējies **Rediģēt dokumentu**, bet lapa **BDM veidnes redaktors** programmā Finance and Operations netika atvērta un tiku novirzīts uz Office 365 tīmekļa lapu.
Šī ir zināma problēma ar Office 365 virzienmaiņu. Tā notiek, pirmo reizi pierakstoties programmā Office 365. Lai atrisinātu šo problēmu, savā pārlūkprogrammā atlasiet pogu **Atpakaļ**, lai atgrieztos atpakaļ.

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>Es saprotu, kā rediģēt veidni, izmantojot programmu Office 365 pirmajā piemērošanas reizē un kā izmantot veidni otrajā piemērošanas reizē, pielāgojot veidni, lai redzētu, kā manas izmaiņas ietekmē ģenerēto biznesa dokumentu. Vai es varu to izdarīt, izmantojot datora lietojumprogrammā Office?
Jā, varat. Pirmajā piemērošanas sesijā atlasiet **Atvērt datora lietojumprogrammu**. Jūsu veidne tiks saglabāta pagaidu failu krātuvē un atvērta datora lietojumprogrammā Office. Tālāk, pabeidziet šādas darbības, lai priekšskatītu savas veidnes izmaiņas ģenerētajā biznesa dokumentā:

1. Veiciet izmaiņas veidnē, izmantojot datora lietojumprogrammu Office.
2. Datora lietojumprogrammā Office atlasiet **Saglabāt**.
3. Pirmās pielietošanas sesijas lapā **BDM veidnes redaktors** atlasiet **Sinhronizētā saglabātā kopija**.
4. Izpildiet šo veidnes ER formātu otrās pielietošanās sesijā.

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>Parādās kļūda “Vērtība nevar būt nulle. Parametra nosaukums: externalId”, izvēloties **Atvērt datora lietojumprogrammā**. Kā atrisināt šo problēmu? 
Visticamāk, esat pierakstījies pašreizējai Azure AD domēna lietojumprogrammas instancei, kas atšķiras no Azure AD domēna, kas tika izmantots šīs instances izvietošanai. Tā kā pakalpojums SharePoint, kas tiek izmantots veidņu glabāšanai, lai padarītu tās pieejamas rediģēšanai, izmantojot datora lietojumprogrammas Office, pieder pie tā paša domēna, mums nav atļauju piekļūt pakalpojumam SharePoint. Lai atrisinātu šo problēmu, pierakstieties pašreizējai instancei, izmantojot lietotāja ar pareizu Azure AD domēnu akreditācijas datus.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko ziņojumu (ER) pārskats](general-electronic-reporting.md)

[ER Izveidot konfigurāciju pārskatu ģenerēšanai formātā OPENXML (2016. gada maijs)](tasks/er-design-reports-openxml-2016-11.md)

[ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā](tasks/er-design-configuration-word-2016-11.md)

[Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md)

[Elektronisko pārskatu (EP) izveides konfigurēšana, lai pārsūtītu datu uz pakalpojumu Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)
