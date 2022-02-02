---
title: Pārskats par biznesa dokumentu pārvaldību
description: Šajā tēmā ir sniegta informācija par to, kā izmantot biznesa dokumentu pārvaldības līdzekli elektroniskā pārskata struktūrā.
author: NickSelin
ms.date: 04/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: faea9d4d9b3fc8f3f1474b6bb2a8dc31cdc22511
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986255"
---
# <a name="business-document-management-overview"></a>Pārskats par biznesa dokumentu pārvaldību

[!include [banner](../includes/banner.md)]

Biznesa lietotāji izmanto [Elektronisko pārskatu (EP)](general-electronic-reporting.md) struktūru, lai konfigurētu izejošo dokumentu formātus saskaņā ar dažādu valstu/reģionu juridiskajām prasībām. Lietotāji var arī definēt datu plūsmu, lai norādītu, kādus lietojumprogrammas datus ievietot ģenerētajos dokumentos. EP struktūra ģenerē izejošos dokumentus Microsoft Office formātos (Excel darbgrāmatas vai Word dokumentus), izmantojot iepriekš definētas veidnes. Veidnes tiek aizpildītas ar nepieciešamajiem datiem saskaņā ar konfigurēto datu plūsmu, kamēr tiek ģenerēti nepieciešamie dokumenti. Katru konfigurētu formātu var publicēt kā EP risinājuma daļu noteiktu izejošo dokumentu ģenerēšanai. To pārstāv EP formāta konfigurācija, kas var ietvert veidnes, ko var izmantot dažādu izejošo dokumentu ģenerēšanai. Biznesa lietotāji var izmantot šo struktūru, lai pārvaldītu nepieciešamos biznesa dokumentus.

**Biznesa dokumentu pārvaldība** ir izveidota uz ER struktūras un ļauj biznesa lietotājiem rediģēt biznesa dokumentu veidnes, izmantojot pakalpojumu Microsoft 365 vai atbilstošu datora lietojumprogrammu Microsoft Office. Dokumentu rediģējumiem ir jāietver biznesa dokumentu noformējumu izmaiņas un vietturu pievienošanu papildu datiem bez avota koda izmaiņām un jaunām izvietošanām. Lai atjauninātu biznesa dokumentu veidnes, nav nepieciešamas nekādas zināšanas par ER struktūru.

> [!NOTE]
> Biznesa dokumentu pārvaldība ļauj jums modificēt veidnes, kas tiek izmantotas tādu biznesa dokumentu izveidei kā pasūtījumi, rēķini utt. Kamēr veidne tika modificēta un tika publicēta tās jauna versija, šo versiju izmanto nepieciešamo biznesa dokumentu ģenerēšanai. Biznesa dokumentu pārvaldību nevar izmantot, lai modificētu jau ģenerētos biznesa dokumentus.

## <a name="supported-deployments"></a>Atbalstītie izvietojumi

Pašreiz biznesa dokumentu pārvaldības līdzeklis ir ieviests tikai mākoņa izvietojumiem. Ja šis līdzeklis ir kritisks jūsu lokālajam izvietojumam, ziņojiet mums, sniedzot atsauksmes vietnē [Idejas](https://experience.dynamics.com/ideas/).

## <a name="supported-microsoft-office-applications"></a>Atbalstītās Microsoft Office programmas

Lai izmantotu Biznesa dokumentu pārvaldību veidņu rediģēšanai Excel vai Word formātos, izmantojot Microsoft Office datora lietojumprogrammas, jums ir jābūt instalētai programmai Microsoft Office 2010 vai jaunākajai versijai. Tā tiek atbalstīta mākonī un lokālajā izvietojumā.

Lai izmantotu biznesa dokumentu pārvaldību veidņu rediģēšanai Excel vai Word formātos, izmantojot programmas, jums Microsoft 365 jābūt Office tīmekļa Microsoft 365 abonementam. Tas tiek atbalstīts mākoņa izvietošanā.

## <a name="business-document-availability"></a>Biznesa dokumentu pieejamība

Pilns saraksts ar visiem pārskatiem, kas ieplānoti 2019. gada oktobra laidienam, ir atrodams rakstā [Konfigurējamas biznesa dokumentu atskaites Word un Excel formātā](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

Pilns saraksts ar visiem pārskatiem, kas ieplānoti 2020. gada oktobra laidienā, ir atrodams rakstā [Konfigurējamas biznesa dokumentu veidnes Word formātā](/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Papildu pārskati kļūs pieejami turpmākajos laidienos. Īpaši paziņojumi par papildu pārskatiem tiks nosūtīti atsevišķi. Lai uzzinātu, kā pārskatīt pašlaik pieejamo pārskatu sarakstu, skatiet tālāk sadaļu [ER konfigurāciju saraksts, kas izlaistas finansēs, lai atbalstītu tālāk norādītos konfigurējamus biznesa dokumentus](#list-of-configurations-cbd).

Lai iegūtu papildinformāciju par šo līdzekli, aizpildiet šajā tēmā sniegto piemēru.

## <a name="configure-er-parameters"></a>Konfigurējiet ER parametrus

Tā kā Biznesa dokumentu pārvaldība ir izveidota, balstoties uz ER struktūru, jums ir jākonfigurē ER parametri, lai sāktu darbu ar Biznesa dokumentu pārvaldību. Lai to paveiktu, ir nepieciešams iestatīt EP parametrus, kā aprakstīts rakstā [Elektronisko paziņojumu (EP) struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md). Ir nepieciešams pievienot jaunu konfigurācijas sniedzēju, kā aprakstīts rakstā [Konfigurācijas sniedzēju izveide un to atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER darbvieta.](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>ER risinājumu importēšana

Šīs procedūras piemērā tiek izmantoti parauga EP konfigurācijas. Jums ir jāimportē jūsu pašreizējā Dynamics 365 Finance instancē tās EP konfigurācijas, kas ietver biznesa dokumentu veidnes, kuras var rediģēt, izmantojot biznesa dokumentu pārvaldību. Lejupielādējiet un pēc tam lokāli saglabājiet tālāk norādītos failus šīs procedūras pabeigšanai.

**ER debitoru rēķinu risinājuma paraugs**

| Fails                                      | Saturs |
|-------------------------------------------|---------|
| Customer invoicing model.version.2.xml    | [ER datu modeļa konfigurācija](https://download.microsoft.com/download/b/f/a/bfa5cb52-e6e2-42bc-a4c0-77014a4c54e6/Customerinvoicingmodel.version.2.xml) |
| Customer FTI report (GER).version.2.3.xml | [Brīva teksta rēķina ER formāta konfigurācija](https://download.microsoft.com/download/3/c/2/3c2e58f2-6e56-43d9-85ea-4c97252a108d/CustomerFTIreportGER.version.2.3.xml) |

**ER maksājumu čeku risinājuma paraugs**

| Fails                                     | Saturs |
|------------------------------------------|---------|
| Model for cheques.version.10.xml         | [ER datu modeļa konfigurācija](https://download.microsoft.com/download/3/7/6/376cb0f6-181a-4895-a432-390ffca64162/Modelforcheques.version.10.xml) |
| Cheques printing format.version.10.9.xml | [Maksājuma čeka ER formāta konfigurācija](https://download.microsoft.com/download/6/d/6/6d61bfff-3d89-4377-9e34-2e3ee6d6df91/Chequesprintingformat.version.10.9.xml) |

**ER ārējās tirdzniecības risinājuma paraugs**

| Fails                             | Saturs |
|----------------------------------|---------|
| Intrastat model.version.1.xml    | [ER datu modeļa konfigurācija](https://download.microsoft.com/download/2/0/0/200d6ed1-eff8-48ec-ab75-175a4acf9714/Intrastatmodel.version.1.xml) |
| Intrastat report.version.1.9.xml | [Intrastat kontroles pārskata ER formāta konfigurācija](https://download.microsoft.com/download/7/a/2/7a2a27c3-a8a5-42a1-9d04-f0a8e1ec1707/Intrastatreport.version.1.9.xml) |

Izmantojiet šādu procedūru katra faila importēšanai. Importējiet katra ER risinājuma ER *datu modeļa* konfigurāciju iepriekš minētajās tabulās, pirms atbilstošās ER *formāta* konfigurācijas importēšanas.

1. Atveriet sadaļu **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> lapu **Konfigurācijas**.
2. Lapas augšdaļā atlasiet **Maiņa**.
3. Atlasiet **Ielādēt no XML faila**.
4. Atlasiet **Pārlūkot**, lai ielādētu nepieciešamo XML failu.
5. Atlasiet **Labi**, lai apstiprinātu konfigurācijas importēšanu.

![Konfigurāciju lapā importētās ER konfigurācijas.](./media/BDM-Overview-ERSolutions.png)

Jūs varat arī importēt oficiāli publicētās EP formāta konfigurācijas no Microsoft Dynamics Lifecycle Service (LCS). Piemēram, lai pabeigtu šo procedūru, varat importēt **Brīvā teksta rēķina (Excel)** EP formāta konfigurācijas jaunāko versiju. Atbilstošais EP datu modelis un EP modeļu kartēšanas konfigurācijas tiks importētas automātiski.

![LCS koplietojamo līdzekļu bibliotēkas satura lapa.](./media/BDM-Overview-SharedAssetLibrary.png)

Lai iegūtu papildinformāciju par ER konfigurāciju importēšanu, skatiet [ER konfigurācijas dzīves cikla pārvaldība](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Biznesa dokumentu pārvaldības iespējošana

Lai sāktu Biznesa dokumentu pārvaldību, ir jāatver darbvieta **Funkcionalitātes pārvaldība** un jāiespējo funkcionalitāte **Biznesa dokumentu pārvaldība**.

Izmantojiet šādu procedūru, lai iespējotu Biznesa dokumentu pārvaldības funkcionalitāti visām juridiskām personām.

1. Atveriet darbvietu **Funkcionalitātes pārvaldība**.
2. Cilnē **Jauns** sarakstā atlasiet funkcionalitāti **Biznesa dokumentu pārvaldība**.
3. Atlasiet **Iespējot tūlīt**, lai ieslēgtu atlasīto funkcionalitāti.
4. Atsvaidziniet lapu, lai piekļūtu jaunajam līdzeklim.

> [!NOTE]
> Lai iegūtu plašāku informāciju par jaunā dokumenta lietotāja interfeisa izmantošanu biznesa dokumentu pārvaldībā, skatiet [Jauno dokumentu lietotāja interfeisu biznesa dokumentu pārvaldībā](er-business-document-management-new-template-ui.md).

![Līdzekļu pārvaldības darbvieta.](./media/BDM-Overview-FMEnabling.png)

Papildinformāciju par jaunu līdzekļu aktivizēšanu skatiet rakstā [Pārskats par līdzekļu pārvaldību](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Konfigurēt parametrus

Izmantojiet tālāk norādītajās sadaļās redzamo informāciju, lai iestatītu pamatparametrus Biznesa dokumentu pārvaldībai.

### <a name="prerequisites-for-parameter-setup"></a>Parametru iestatīšanas priekšnosacījumi

Pirms Biznesa dokumentu pārvaldības iestatīšanas, ir jāiestata nepieciešamais dokumenta tips Dokumentu pārvaldības struktūrā. Šo dokumenta tipu lieto, lai norādītu dokumentu pagaidu glabāšanu Office formātos (Excel un Word), kas izmantoti kā veidnes ER pārskatiem. Pagaidu glabāšanas veidni var rediģēt, izmantojot Office datora lietojumprogrammas.

Šim dokumenta tipam ir jāatlasa šādas atribūtu vērtības.

| Atribūta nosaukums | Atribūta vērtība |
|----------------|-----------------|
| Klase          | Pievienot failu     |
| Grupa          | Fails            |
| Vieta       | SharePoint      |

Lai iegūtu papildu informāciju, kā iestatīt nepieciešamos dokumentu pārvaldības parametrus un dokumentu tipus, skatiet [Dokumentu pārvaldības konfigurācija](../../fin-ops/organization-administration/configure-document-management.md).

![Iestatiet Dokumentu pārvaldības dokumentu tipu.](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Iestatīšanas parametri

Pamata Biznesa dokumentu pārvaldības parametrus var iestatīt lapā **Biznesa dokumentu parametri**. Lapai var piekļūt tikai noteikti lietotāji. Tā ietver:

- Lietotāji, kuriem piešķirta **Sistēmas administratora** loma.
- Lietotāji, kuriem ir piešķirta jebkāda loma, kas ir konfigurēta pienākuma izpildei **Uzturēt Biznesa dokumentu pārvaldības parametrus** (lietojumprogrammas objektu koka (AOT) nosaukums **ERBDMaintainParameters**).

Izmantojiet šādu procedūru pamata parametru iestatīšanai visām juridiskām personām.

1. Pierakstieties kā lietotājs ar piekļuvi lapai **Biznesa dokumentu parametri**.
2. Pārejiet uz sadaļu **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Biznesa dokumentu pārvaldība** \> **Biznesa dokumentu parametri**.
3. Lapā **Biznesa dokumentu parametri** cilnē **Pielikumi**, laukā **SharePoint document tips** definējiet dokumenta tipu, ko izmantot veidņu pagaidu glabāšanai Office formātos, kamēr tiek rediģēti, izmantojot Office datora lietojumprogrammas. 

> [!NOTE]
> Šim parametram ir pieejami tikai dokumentu tipi, kas konfigurēti, izmantojot SharePoint atrašanās vietu.

![Biznesa dokumentu pārvaldības parametru iestatīšana.](./media/BDM-Overview-BDMSetting.png)

Izvēlētais dokumenta tips ir raksturīgs uzņēmumam un tiks izmantots, kad lietotājs strādā ar Biznesa dokumentu pārvaldību uzņēmumā, kuram atlasītais dokumenta veids ir konfigurēts. Ja lietotājs strādā ar Biznesa dokumentu pārvaldību citā uzņēmumā, tiks izmantots tāds pats atlasītais dokumenta tips, ja šim uzņēmumam tāds netika konfigurēts. Ja dokumenta tips tika konfigurēts, tas tiks izmantots laukā **SharePoint dokumenta tips** atlasītā dokumenta tipa vietā.

> [!NOTE]
> **SharePoint dokumentu tipa** parametrs definē SharePoint mapi kā pagaidu krātuvi veidnēm, kas rediģējamas, izmantojot vai nu Microsoft Excel, vai Word. Šis parametrs jāiestata, ja veidņu rediģēšanai plānojat lietot šīs Office datora lietojumprogrammas. Papildinformāciju skatiet [Veidnes rediģēšana Office datora lietojumprogrammā](#EditInOfficeDesktopApp). Šo parametru varat atstāt tukšu, ja plānojat modificēt veidni, tikai izmantojot funkcionalitāti šeit: <a0/&Microsoft 365. Papildu informāciju par veidni skatiet [Rediģēt veidni Microsoft 365](#EditInOffice365).

## <a name="configure-access-permissions"></a>Piekļuves atļauju konfigurēšana

Pēc noklusējuma, ja Biznesa dokumentu pārvaldības atļaujas nav iespējotas, katrs lietotājs, kuram ir piekļuve Biznesa dokumentu pārvaldības darbvietai, redzēs visas ER risinājuma veidnes, kas ir pieejamas. Biznesa dokumentu pārvaldības darbvietā būs parādīti tikai tās veidnes, kuras atrodamas ER formāta konfigurācijās un kuras atzīmētas kā **Biznesa dokumentu tips**.

![ER konfigurāciju lapa ar biznesa dokumenta tipa vietturi.](./media/BDM-Overview-ERFormatTags.png)

Veidņu sarakstu, kas pieejams Biznesa dokumentu pārvaldības darbvietā, var ierobežot, konfigurējot piekļuves atļaujas. Tas var būt svarīgi, kad dažādas veidnes tiek izmantotas biznesa dokumentu izveidei dažādiem biznesa domēniem (funkcionālajiem apgabaliem) un jūs vēlaties atļaut noteiktiem lietotājiem piekļūt dažādām veidnēm rediģēšanai Biznesa dokumentu pārvaldības darbvietā.

Biznesa dokumentu pārvaldības piekļuves atļaujas var iestatīt sadaļā **Piekļuves parametru konfigurētājs**. Lapai var piekļūt tikai šādi lietotāji:

- Lietotāji, kuriem piešķirta **Sistēmas administratora** loma.
- Lietotāji, kuriem ir piešķirta jebkāda cita loma, kas ir konfigurēta pienākuma izpildei **Konfigurēt atļaujas, lai piekļūtu Biznesa dokumentu veidnēm rediģēšanas veikšanai** (lietojumprogrammas objektu koka (AOT) nosaukums **ERBDTemplatesSecurity**).

Izmantojiet šādu procedūru, lai iestatītu Biznesa dokumentu pārvaldības atļaujas visām juridiskām personām.

1. Pierakstieties kā lietotājs ar piekļuvi lapai **Biznesa dokumentu parametri**.
2. Pārejiet uz sadaļu **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Biznesa dokumentu pārvaldība** \> **Pārvaldīt piekļuves atļaujas**.

    Pievērsiet uzmanību informatīvajam paziņojumam par to, ka piekļuves atļauju izmantošana Biznesa dokumentu pārvaldībai pašlaik nav iespējota.

    ![Biznesa dokumentu pārvaldības piekļuves lapas konfigurētājs.](./media/BDM-Overview-TemplatesAccess1.png)

    Izmantojot šo iestatījumu, katrs lietotājs, kam piešķirta jebkāda drošības loma, konfigurēta pienākuma **Pārvaldīt Biznesa dokumentu veidnes** (AOT nosaukums **ERBDManageTemplates**) veikšanai, spēj atvērt Biznesa dokumentu pārvaldības darbvietu un var rediģēt jebkādu veidni, kas ir pieejama.

    Tālāk redzamā grafika parāda, kas ir pieejams Biznesa dokumentu pārvaldības darbvietā lietotājiem, kam piešķirta loma **Debitoru parādu darbinieks**. Ar pašreizējo piekļuves atļauju iestatījumu lietotājs var rediģēt biznesa dokumentu veidnes no dažādām funkcionālajām jomām, tostarp rēķinu izrakstīšanu, regulēšanas pārskatu veidošanu un maksājumus.

    ![Biznesa dokumentu pārvaldības darbvietas lapa Debitoru parādu darbinieks.](./media/BDM-Overview-TemplatesForAlice1.png)

3. Lapā **Piekļuves atļauju konfigurētājs** atlasiet **Piekļuves atļauju iestatījums**.
4. Dialoglodziņā **Piekļuves atļauju iestatījumi veidņu rediģēšanai** iespējojiet opciju **Piemērot konfigurētās piekļuves atļaujas**.
5. Atlasiet **Labi**, lai apstiprinātu, ka Biznesa dokumentu pārvaldības piekļuves atļaujas tika iespējotas.

    ![Biznesa dokumentu pārvaldības piekļuves atļauju apstiprināšana.](./media/BDM-Overview-TemplatesAccess2.png)

6. Atlasiet **Pievienot**, lai ievadītu jaunu biznesa lomu, kurai ir jākonfigurē atļaujas, lai piekļūtu Biznesa dokumentu pārvaldības veidnēm.
7. Dialoglodziņā **Drošības lomas** atlasiet lomu **Debitoru parādu darbinieks** un pēc tam atlasiet **Labi**, lai apstiprinātu lomas atlasi.
8. Cilnē **Piekļuves atļaujas konfigurāciju atzīmēm** atlasiet **Jauns**.
9. Laukā **Atzīmes tips** atlasiet **Funkcionālais apgabals** un laukā **ID** atlasiet **Rēķinu izrakstīšana**.
10. Atlasiet **Saglabāt** konfigurēto piekļuves atļauju glabāšanai atlasītajai lomai.

    Pašreizējais iestatījums nozīmē, ka jebkuram lietotājam, kuram piešķirta loma **Debitoru parādu darbinieks** un pienākuma **Pārvaldīt Biznesa dokumentu veidnes** (AOT nosaukums **ERBDManageTemplates**) izpilde, ER formāta konfigurācijas veidnes ar vērtību **Rēķina izrakstīšana** atzīmei **Funkcionālais apgabals** būs pieejamas rediģēšanai Biznesa dokumentu pārvaldības darbvietā.

11. Pašreizējās lapas labajā pusē pārslēdziet rūti **Saistītā informācija**. Rūts **Saistītā informācija** parāda, kā tiks piemērotas konfigurētās piekļuves atļaujas, tostarp kādas ER konfigurācijas veidnes būs pieejamas lietotājiem, kuriem piešķirta loma **Debitoru parādu darbinieks**.

    ![Saistītā informācijas rūts piekļuves tiesību lapas konfigurētājā.](./media/BDM-Overview-TemplatesAccess3.png)

12. Cilnē **Piekļuves atļaujas konfigurācijām** atlasiet opciju **Pievienot**.
13. Dialoglodziņā **Atlasīt konfigurāciju** atzīmējiet ER formāta konfigurāciju **Intrastat pārskats**.
14. Atlasiet **Labi**, lai apstiprinātu atlasīto konfigurāciju ierakstu, un pēc tam atlasiet **Saglabāt**, lai saglabātu konfigurētās piekļuves atļaujas atlasītajai lomai.

Pašreizējais iestatījums nozīmē, ka jebkuram lietotājam, kuram piešķirta loma **Debitoru parādu darbinieks** un pienākuma **Pārvaldīt Biznesa dokumentu veidnes** (AOT nosaukums **ERBDManageTemplates**) izpilde, būs pieejamas tālāk norādītās veidnes rediģēšanai Biznesa dokumentu pārvaldības darbvietā:

- Veidnes ar vērtību **Rēķina izrakstīšana** atzīmei **Funkcionālais apgabals**.
- Veidnes no ER formāta konfigurācijām ir uzskaitītas cilnē **Piekļuves atļaujas konfigurācijām** (šajā piemērā veidnes no **Intrastat pārskata** formāta konfigurācijas domēnā **Likumā noteiktie pārskati** ).

![Piekļūstiet atļaujām kopsavilkuma cilnē Konfigurētāja atļauju piekļuves lapā.](./media/BDM-Overview-TemplatesAccess4.png)

Tālāk redzamā grafika parāda, kas ir pieejams Biznesa dokumentu pārvaldības darbvietā lietotājam, kam piešķirta loma **Debitoru parādu darbinieks**. Ar pašreizējo Biznesa dokumentu pārvaldības piekļuves atļauju iestatījumu lietotājs var rediģēt biznesa dokumentu veidnes no domēna **Rēķina izrakstīšana** un ER formāta konfigurācijas **Intrastat pārskats**. Veidnes no domēna **Maksājumi** nav pieejamas lomai **Debitoru parādu darbinieks**.

![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai sāktu biznesa dokumenta veidnes rediģēšanu.](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> Kārtulas **Piekļuves atļaujas konfigurācijām** tiek glabātas, izmantojot ER formāta konfigurācijas unikālo identifikācijas ID. Tas nozīmē, ka šīs kārtulas netiks dzēstas, izdzēšot uz tām attiecināmo ER konfigurāciju. Importējot dzēstas konfigurācijas atpakaļ uz šo instanci, šīs kārtulas atkal tiks uz tiem attiecinātas. Nav nepieciešams iestatīt kārtulas vēlreiz pēc tam, kad izdzēstas konfigurācijas tiek vēlreiz importētas.

## <a name="use-business-document-management-to-edit-templates"></a>Biznesa dokumentu pārvaldības izmantošana veidņu rediģēšanai

Biznesa lietotāji var piekļūt biznesa dokumentu veidnēm rediģēšanai Biznesa dokumentu pārvaldības darbvietā. Tikai šādi lietotāji var piekļūt Biznesa dokumentu pārvaldības darbvietai:

- Lietotāji, kuriem piešķirta loma **Sistēmas administrators**.
- Lietotāji, kuriem ir piešķirta jebkāda loma, kas ir konfigurēta pienākuma izpildei **Uzturēt Biznesa dokumentu pārvaldības parametrus** (AOT nosaukums **ERBDManageTemplates**).

Izmantojiet šādu procedūru, lai rediģētu brīva teksta rēķinu veidnes Biznesa dokumentu pārvaldības darbvietā. Pirms pabeigt šo procedūru, jums ir jāpabeidz visas iepriekšējās procedūras šajā tēmā.

1. Pierakstieties kā lietotājs ar piekļuvi Biznesa dokumentu pārvaldības darbvietai.
2. Atveriet Biznesa dokumentu pārvaldības darbvietu

Ja **Office līdzīga interfeisa pieredze biznesa dokumentu pārvaldības** līdzeklis ir izslēgts **Funkciju pārvaldības** darbvietā, galvenais režģis **Biznesa dokumentu pārvaldības** darbvietā rāda šādas veidnes:

- Veidnes, kas pieder jūsu ER konfigurācijas nodrošinātājam (t.i., sniedzējam, kas pašlaik ir atzīmēts kā aktīvs **Elektroniskā pārskata** darbvietā). Kad esat atlasījis vienu no šīm veidnēm, varat atlasīt **Rediģēt veidni**, lai sāktu vai turpinātu tās rediģēšanu.
- Citu ER konfigurācijas nodrošinātājiem piederošas veidnes. Pēc tam, kad esat atlasījis vienu no šīm veidnēm, jūs varat atlasīt **Jaunu dokumentu**, lai izveidotu tā kopiju, kas pieder jūsu ER konfigurācijas nodrošinātājam, un tad sākt rediģēt kopiju.

![Veidņu saraksti biznesa dokumentu pārvaldības darbvietā.](./media/BDM-Overview-EditingTemplate1.png)

Cilnē **Veidne** redzams atlasītās veidnes saturs. Atlasiet cilni **Detalizēti**, lai pārskatītu atlasītās veidnes papildinformāciju, kā arī papildinformāciju ER formāta konfigurācijai, kurā šī veidne atrodas. Ievērojiet, ka visām veidnēm ir statuss **Publicēts** un tajās nav papildinformācijas kolonnā **Pārskatījums**. Tas nozīmē, ka šīs veidnes šobrīd netiek rediģētas.

Ja **Office līdzīga lietotāja interfeisa pieredze biznesa dokumentu pārvaldības** līdzeklim ir ieslēgts **Funkciju pārvaldības** darbvietā, galvenais režģis **Biznesa dokumentu pārvaldības** darbvietā parāda veidnes, kas pieder jūsu ER konfigurācijas nodrošinātājam (tas ir, nodrošinātājs, kas pašlaik ir atzīmēts kā aktīvs **Elektroniskā pārskata** darbvietā). Kad esat atlasījis vienu no šīm veidnēm, varat atlasīt **Rediģēt veidni**, lai sāktu vai turpinātu tās rediģēšanu.

Lai strādātu ar veidnēm, kas pieder citiem ER konfigurācijas nodrošinātājiem, atlasiet **Jauns dokuments**, lai izveidotu veidnes kopiju, kas pieder jūsu ER nodrošinātājam. Pēc tam varat sākt rediģēt kopiju. Papildinformācijai skatiet [Jauna dokumenta lietotāja interfeiss Biznesa dokumentu pārvaldībā](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Sāciet rediģēt veidnes, kas pieder jūsu konfigurācijas sniedzējam

1. Biznesa dokumentu pārvaldības darbvietā no saraksta atlasiet veidni **Čeku drukāšanas formāts**.
2. Atlasiet cilni **Detalizēti**.

![Biznesa dokumentu pārvaldības darbvietas lapa, cilne Detalizēta informācija.](./media/BDM-Overview-EditingTemplate2.png)

Atlasītajai veidnei ir pieejama opcija **Rediģēt veidni**. Šī opcija vienmēr ir pieejama veidnei ER formāta konfigurācijā, kas pieder aktīvajam ER konfigurācijas sniedzējam (šajā piemērā **Litware, Inc.** ). Kad ir atlasīta opcija **Rediģēt veidni**, esošā veidne no pamatā esošās ER formāta konfigurācijas melnraksta versijas būs pieejama rediģēšanai.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Sāciet rediģēt veidnes, kas pieder citiem nodrošinātājiem

1. Biznesa dokumentu pārvaldības darbvietā atlasiet dokumentu, kuru vēlaties izmantot kā veidni.

    ![Darbvietas lapā Biznesa dokumentu pārvaldība atlasiet dokumentu.](./media/BDM-Overview-EditingTemplate3.png)

2. Atlasiet **Jauns dokuments**, un laukā **Nosaukums** izmainiet rediģējamās veidnes nosaukumu, ja nepieciešams. Teksts tiks izmantots automātiski izveidotās ER formāta konfigurācijas nosaukumam. Ievērojiet, ka šīs konfigurācijas (**Klientu FTI pārskats (GER) Kopija**) melnraksta versija, kas ietvers rediģēto veidni, automātiski tiks atzīmēta šī ER formāta izmantošanai pašreizējam lietotājam. Tajā pašā laikā nemainītā sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai jebkādam citam lietotājam.
3. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
4. Laukā **Komentārs** nomainiet komentāru nosaukumu rediģējamās veidnes automātiski izveidotajai pārskatīšanai.
5. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

![Apstipriniet rediģēšanas procesa sākumu, lai izveidotu jaunu veidni.](./media/BDM-Overview-EditingTemplate4.png)

Ja nav neviena nodrošinātāja, to piedāvās izveidot. Ja nav aktīva nodrošinātāja, tiek piedāvāts to izvēlēties aktivizēšanai.

Lai izveidotu nodrošinātāju, mainiet nodrošinātāja nosaukumu laukā **Nosaukums**, atjauniniet jaunā nodrošinātāja interneta adresi laukā **Interneta adrese** un atlasiet **Labi**, lai apstiprinātu.

   ![Izveidot jaunu nodrošinātāju BDM.](./media/bdm_create_provider.png)

Lai aktivizētu esošu nodrošinātāju, izvēlieties nodrošinātāja nosaukumu laukā **Konfigurācijas nodrošinātājs** un atlasiet **Labi**, lai iestatītu nodrošinātāju kā aktīvu.

   ![Aktivizēt nodrošinātāju BDM.](./media/bdm_choose_provider.png)

> [!NOTE]
> Katra BDM veidne atsaucas uz nodrošinātāju kā konfigurācijas autoru. Tāpēc veidnei ir nepieciešams aktīvs nodrošinātājs.


Opcija **Jauns dokuments** vienmēr ir pieejama veidnei ER formāta konfigurācijā, kas pieder pašreizējam un citam nodrošinātājam (šajā piemērā Microsoft) un kurai nav pārskatījuma. Rediģētā veidne būs saglabāta jaunā ER formāta konfigurācijā, kas ģenerēta automātiski.



### <a name="start-editing-a-template"></a>Sāciet veidnes rediģēšanu

1. Atlasītajā veidnē atlasiet **Rediģēt dokumentu**.
2. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
3. Laukā **Komentārs** nomainiet piezīmi nosaukumu rediģējamās veidnes automātiski izveidotajai pārskatīšanai.

    ![Veidņu saraksti biznesa dokumentu pārvaldības darbvietā.](./media/BDM-Overview-EditingTemplate5.png)

4. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

**BDM veidnes redaktors** lapa atversies. Atlasītā veidne būs pieejama rediģēšanai tiešsaistē, izmantojot programmu Microsoft 365.

![Biznesa dokumentu pārvaldības veidņu rediģēšanas lapa.](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Rediģēt veidni programmā Microsoft 365

Veidni iespējams modificēt, izmantojot Microsoft 365. Piemēram, programmā Office online izmaniet lauku uzvedņu fontu veidnes virsrakstā no **Parasts** uz **Treknraksts**. Šīs izmaiņas tiek automātiski saglabātas rediģējamajā veidnē, kas tiek glabāta primārajā veidnes krātuvē (pēc noklusējuma Azure BLOB krātuvē). Tas ir konfigurēts ER struktūrai.

![Maina fontu uz treknrakstu veidnes virsrakstā biznesa dokumentu pārvaldības veidnes redaktora lapā.](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Rediģējiet veidni datora lietojumprogrammā Office

> [!NOTE]
> Šī funkcija ir pieejama tikai tad, ja parametrs **SharePoint dokumenta tips** ir pareizi konfigurēts. Papildinformāciju skatiet sadaļā [Parametru konfigurēšana](#SetupBdmParameters).

1. Atlasiet opciju **Atvērt datora lietojumprogrammu**, lai modificētu veidni, izmantojot datora lietojumprogrammas Office (šajā piemērā Excel) funkcionalitāti. Rediģējamā veidne tiek kopēta no pastāvīgās krātuves uz pagaidu krātuvi, kas Biznesa dokumentu pārvaldības parametros ir konfigurēta kā SharePoint mape.
2. Apstipriniet, ka vēlaties atvērt veidni no pagaidu failu krātuves Office datora lietojumprogrammā Excel.

    ![Veidne atvērta darbvirsmas Excel programmā.](./media/BDM-Overview-EditingLayout3.png)

3. Modificējiet veidni. Piemēram, izmaniet lauku uzvedņu fontu veidnes virsrakstā no **Melnās** uz **Zilo** krāsu.

    ![Fonta krāsas modificēšana veidnes galvenē, izmantojot darbvirsmas Excel programmu.](./media/BDM-Overview-EditingLayout4.png)

4. Atlasiet **Saglabāt** datora lietojumprogrammā Excel, lai saglabātu veidņu izmaiņas pagaidu krātuvē.

    ![Saglabāt izmaiņas biznesa dokumentu pārvaldības veidnes redaktora lapā, izmantojot darbvirsmas Excel programmu.](./media/BDM-Overview-EditingLayout5.png)

5. Aizveriet datora lietojumprogrammu Excel.
6. Atlasiet **Sinhronizētu saglabāto kopiju**, lai sinhronizētu pagaidu veidņu krātuvi ar pastāvīgu veidņu krātuvi.

> [!NOTE]
> Rediģējamās veidnes kopija pagaidu failu krātuvē tiek glabāta tikai veidņu rediģēšanas pašreizējai sesijai. Kad pabeidzat šo sesiju, aizverot lapu **BDM veidņu redaktors**, šī kopija tiks dzēsta. Ja pielāgojāt veidni pagaidu failu krātuvē un neesat atlasījis **Sinhronizēto saglabāto kopiju**, mēģinot aizvērt lapu **BDM veidņu redaktors**, parādīsies ziņojums ar jautājumu, vai vēlaties saglabāt ieviestās izmaiņas. Atlasiet **Jā**, ja vēlaties saglabāt izmaiņas veidnē pastāvīgā faila atrašanās vietā.

### <a name="validate-a-template"></a>Validējiet veidni

1. Lapā **BDM veidņu redaktors** atlasiet **Problēmu meklēšana**, lai validētu modificētu veidni attiecībā pret pamatā esošo ER formāta konfigurāciju. Izpildiet ieteikumus (ja ir), lai pielāgotu veidni formāta struktūrai no pamata ER formāta konfigurācijas.
2. Atlasiet **Rādīt formātu**, lai skatītu formāta pašreizējo struktūru no pamata ER formāta konfigurācijas, kas jāpielāgo rediģējamajai veidnei. 
3. Atlasiet **Slēpt formātu**, lai aizvērtu rūti.

    ![BDM BDM veidnes redaktora lapa.](./media/BDM-Overview-EditingTemplate6.png)

4. Aizveriet lapu **BDM veidnes redaktors**.

Atjauninātā veidne tiek rādīta cilnē **Veidne**. Ievērojiet, ka rediģētās veidnes statuss tagad ir **Melnraksts** un pašreizējā pārskatīšana vairs nav tukša. Tas nozīmē, ka ir sācies šīs veidnes rediģēšanas process.

![Skatiet atjauninātās veidnes Biznesa dokumentu pārvaldības darbvietas lapā.](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Modificētās veidnes testēšana 

1. Programmā, mainiet uz uzņēmumu, **USMF**.
2. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
3. Atlasiet rēķinu **FTI-00000002** un pēc tam atlasiet **Drukāšanas pārvaldība**.
4. Atlasiet **Modulis — debitori** \> **Dokumenti** \> **Brīva teksta rēķins** \> līmeni **Sākotnējais dokuments**, lai norādītu rēķinu tvērumu apstrādei.
5. Laukā **Pārskata formāts** atlasiet ER formātu **Klientu FTI pārskats (GER) Kopija** norādītā dokumenta līmenim.

    ![Drukāšanas pārvaldības iestatījumu lapa.](./media/BDM-Overview-TestRun1.png)

6. Nospiediet taustiņu **Escape**, lai aizvērtu pašreizējo lapu.
7. Atlasiet **Drukāt** un pēc tam nospiediet uz **Atlasīts**.
8. Lejupielādējiet dokumentu un atveriet to, izmantojot datora lietojumprogrammu Excel.

![Brīva teksta rēķinu lapa.](./media/BDM-Overview-TestRun2.png)

Modificētā veidne tiek izmantota, lai ģenerētu brīva teksta rēķina pārskatu atlasītajam vienumam. Lai analizētu, kā šo pārskatu ietekmēja jūsu ieviestās izmaiņas veidnē, varat palaist šo pārskatu vienā lietojumprogrammas sesijā uzreiz pēc tam, kad esat modificējis veidni citā lietojumprogrammas sesijā.

### <a name="create-an-alternative-template-revision"></a>Alternatīvās veidnes pārskatīšanas izveide

1. Atveriet lapu **BDM veidnes redaktors** un atlasiet veidni **Klientu FTI pārskats (GER) Kopija**.
2. Cilnē **Pārskatīšanas** atlasiet **Jauns**.
3. Ja nepieciešams, laukā **Nosaukums** nomainiet nosaukumu otrai pārskatīšanai un balstiet to uz pašreiz aktīvu pirmo pārskatīšanu.
4. Ja nepieciešams, laukā **Komentārs** nomainiet piezīmi rediģējamās veidnes automātiski izveidotajai pārskatīšanai.

    ![Izveidojiet veidņu pārskatījumu Biznesa dokumentu pārvaldības darbvietas lapā.](./media/BDM-Overview-AddRevision.png)

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

![Noraidiet veidnes izmaiņas pārskatījumu Biznesa dokumentu pārvaldības darbvietas lapā.](./media/BDM-Overview-RevokeChanges.png)

1. Lapā **BDM veidnes redaktors** atlasiet cilni **Veidne**.
2. Atlasiet **Atsaukt**.
3. Izvēloties **Labi** veidnē veikto izmaiņu atcelšanai, modificētā veidne tiks aizstāta ar sākotnējo veidni un visas izmaiņas tiks noņemtas. Kad atsaucat izmaiņas veidnē, varēsiet dzēst veidni. Atlasiet **Atcelt** citu opciju izpētei.

### <a name="publish-a-modified-template"></a>Modificētās veidnes publicēšana

1. Lapā **BDM veidnes redaktors** cilnē **Veidne** atlasiet **Publicēt**.
2. Izvēloties **Labi** publicēšanas apstiprināšanai, atvasinātā ER formāta **Customer FTI report (GER) Copy** melnraksta versija, kas satur modificēto veidni, tiks atzīmēta kā pabeigta. Modificētā veidne kļūst pieejama citiem programmas lietotājiem. ER formāta pabeigtās versijas saglabās tikai jūsu veidnes pēdējo aktīvo pārskatīšanu. Citas pārskatīšanas tiks dzēstas. Atlasiet **Atcelt** citu opciju izpētei.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Es atlasīju Rediģēt dokumentu, bet tā vietā, lai atvērtu BDM veidnes redaktora lapu Finansēs, es tiku nosūtīts uz tīmekļa Microsoft 365 lapu.

Šis jautājums ir zināms, kas ietver Microsoft 365 virzienmaiņu. Tas notiek, ja Microsoft 365 parakstāties pirmo reizi. Lai novērstu šo problēmu, atlasiet **Atpakaļ** pārlūkprogrammā, lai atgrieztos iepriekšējā lapā.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>Es saprotu, kā rediģēt veidni, izmantojot pirmo programmas sesiju, un kā izmantot veidni otrajā programmas sesijā un pielāgot veidni, lai redzētu, kā manas izmaiņas ietekmē Microsoft 365 ģenerēto biznesa dokumentu. Vai es varu izmantot Office datora lietojumprogrammu tādā pašā veidā?

Jā, varat. Pirmajā piemērošanas sesijā atlasiet **Atvērt datora lietojumprogrammu**. Jūsu veidne tiks saglabāta pagaidu failu krātuvē un atvērta datora lietojumprogrammā Office. Tālāk, pabeidziet šādas darbības, lai priekšskatītu savas veidnes izmaiņas ģenerētajā biznesa dokumentā:

1. Veiciet izmaiņas veidnē, izmantojot datora lietojumprogrammu Office.
2. Datora lietojumprogrammā Office atlasiet **Saglabāt**.
3. Pirmās pielietošanas sesijas lapā **BDM veidnes redaktors** atlasiet **Sinhronizētā saglabātā kopija**.
4. Izpildiet šo veidnes ER formātu otrās pielietošanās sesijā.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Atlasot Atvērt programmā Darbvirsma, tiek parādīts šāds kļūdas ziņojums: "Vērtība nevar būt null. Parametra nosaukums: externalId." Kā atrisināt šo problēmu?

Visticamāk, esat pierakstījies pašreizējai Azure AD domēna lietojumprogrammas instancei, kas atšķiras no Azure AD domēna, kas tika izmantots šīs instances izvietošanai. Tā kā pakalpojums SharePoint, kas tiek izmantots veidņu glabāšanai, lai padarītu tās pieejamas rediģēšanai, izmantojot datora lietojumprogrammas Office, pieder pie tā paša domēna, mums nav atļauju piekļūt pakalpojumam SharePoint. Lai atrisinātu šo problēmu, pierakstieties pašreizējai instancei, izmantojot lietotāja ar pareizu Azure AD domēnu akreditācijas datus.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko ziņojumu (ER) pārskats](general-electronic-reporting.md)

[ER Izveidot konfigurāciju pārskatu ģenerēšanai formātā OPENXML (2016. gada maijs)](tasks/er-design-reports-openxml-2016-11.md)

[ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā](tasks/er-design-configuration-word-2016-11.md)

[Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md)

[Elektronisko atskaišu (ER) konfigurēšana, lai nogādātu datus uz Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>Saraksts ar ER konfigurācijām, kas izlaistas programmā Finance, lai atbalstītu konfigurējamus biznesa dokumentus

ER [konfigurāciju saraksts](general-electronic-reporting.md#list-of-configurations) programmai Finance tiek pastāvīgi atjaunināts. Atveriet [Globālo repozitoriju](er-download-configurations-global-repo.md), lai pārskatītu pašreiz atbalstīto ER konfigurāciju sarakstu. Varat filtrēt [Globālo repozitoriju](../../../finance/localizations/enhanced-filtering-global-repo.md), lai pārskatītu to ER konfigurāciju sarakstu, ko izmanto konfigurējamu biznesa dokumentu atbalstam.

![Globālā repozitorija satura filtrēšana Konfigurācijas repozitorija lapā.](./media/bdm-overview-filterglobalrepo.gif)

Tabulā ir parādīts ER konfigurāciju saraksts, kas atbalsta konfigurējamus biznesa dokumentus un kas ir izlaistas programmā Finance līdz 2020. gada decembrim.

| Datu modeļa konfigurācija    | Formāta konfigurācija                           |
|-----------------------------|-------------------------------------------------|
| Preču transporta pavadzīmes modelis        | Preču transporta pavadzīme (Excel)                          |
|                             | Preču transporta pavadzīme (Word)                           |
| Izcelsmes sertifikāta modelis | Izcelsmes sertifikāta modelis (Excel)                   |
|                             | Izcelsmes sertifikāta modelis (Word)                    |
| Rēķina modelis               | Debitora debeta un kredīta piezīmes (Excel)          |
|                             | Debitora debeta un kredīta piezīmes (Word)           |
|                             | Brīva teksta rēķins (Excel)                       |
|                             | Brīva teksta rēķins (Excel) (BH)                  |
|                             | Brīva teksta rēķins (FR) (Excel)                  |
|                             | Brīva teksta rēķins (LT) (Excel)                  |
|                             | Brīva teksta rēķins (LV) (Excel)                  |
|                             | Brīva teksta rēķins (PL) (Excel)                  |
|                             | Brīva teksta rēķins (CZ) (Excel)                  |
|                             | Brīva teksta rēķins (EE) (Excel)                  |
|                             | Brīva teksta rēķins (HU) (Excel)                  |
|                             | Brīva teksta rēķins (TH) (Excel)                  |
|                             | Brīva teksta rēķinS (Word)                        |
|                             | Projekta līguma rindas vienumi (Excel)             |
|                             | Projekta līguma rindas vienumi (CZ) (Excel)        |
|                             | Projekta līguma rindas vienumi (Excel) (BH)        |
|                             | Projekta līguma rindas vienumi (HU) (Excel)        |
|                             | Projekta līguma rindas vienumi (LT) (Excel)        |
|                             | Projekta līguma rindas vienumi (PL) (Excel)        |
|                             | Projekta līguma rindas vienumi (Word)              |
|                             | Projekta debitora ieturējumu izlaišana (Excel)      |
|                             | Projekta debitora ieturējumu izlaišana (CZ) (Excel) |
|                             | Projekta debitora ieturējumu izlaišana (HU) (Excel) |
|                             | Projekta debitora ieturējumu izlaišana (LT) (Excel) |
|                             | Projekta debitora ieturējumu izlaišana (PL) (Excel) |
|                             | Projekta debitora ieturējumu izlaišana (TH) (Excel) |
|                             | Projekta debitora ieturējumu izlaišana (Word)       |
|                             | Projekta rēķins (Excel)                         |
|                             | Projekta rēķins (Word)                          |
|                             | Projekta rēķins (AE) (Excel)                    |
|                             | Projekta rēķins (CZ) (Excel)                    |
|                             | Projekta rēķins (Excel) (BH)                    |
|                             | Projekta rēķins (HU) (Excel)                    |
|                             | Projekta rēķins (JP) (Excel)                    |
|                             | Projekta rēķins (LT) (Excel)                    |
|                             | Projekta rēķins (PL) (Excel)                    |
|                             | Projekta rēķins (TH) (Excel)                    |
|                             | Pilns projekta rēķins (MY) (Excel)               |
|                             | Vienkāršs projekta rēķins (MY) (Excel)             |
|                             | Projekta rēķina pārvaldīšana (Excel)                  |
|                             | Projekta rēķina pārvaldīšana (CZ) (Excel)             |
|                             | Projekta rēķina pārvaldīšana (Excel) (BH)             |
|                             | Projekta rēķina pārvaldīšana (HU) (Excel)             |
|                             | Projekta rēķina pārvaldīšana (JP) (Excel)             |
|                             | Projekta rēķina pārvaldīšana (LT) (Excel)             |
|                             | Projekta rēķina pārvaldīšana (PL) (Excel)             |
|                             | Projekta rēķina pārvaldīšana (Word)                   |
|                             | Pirkšanas avansa rēķins (Excel)                |
|                             | Pirkšanas avansa rēķins (Word)                 |
|                             | Pārdošanas avansa rēķins (Excel)                   |
|                             | Pārdošanas avansa rēķins (Word)                    |
|                             | Pārdošanas avansa rēķins (PL) (Excel)              |
|                             | Pārdošanas rēķins (Excel)                           |
|                             | Pārdošanas rēķins (Excel) (BH)                      |
|                             | Pārdošanas rēķins (Excel) (CZ)                      |
|                             | Pārdošanas rēķins (Excel) (EE)                      |
|                             | Pārdošanas rēķins (Excel) (FR)                      |
|                             | Pārdošanas rēķins (Excel) (HU)                      |
|                             | Pārdošanas rēķins (Excel) (IN)                      |
|                             | Pārdošanas rēķins (Excel) (LT)                      |
|                             | Pārdošanas rēķins (Excel) (LV)                      |
|                             | Pārdošanas rēķins (Excel) (PL)                      |
|                             | Pārdošanas rēķins (Excel) (TH)                      |
|                             | Pārdošanas rēķins (Word)                            |
|                             | TMS Tirdzniecības rēķins (Excel)                  |
|                             | TMS Tirdzniecības rēķins (Word)                   |
|                             | Kreditora rēķina dokuments (Excel)                 |
|                             | Kreditora rēķina dokuments (CZ) (Excel)            |
|                             | Kreditora rēķina dokuments (HU) (Excel)            |
|                             | Kreditora rēķina dokuments (IN) (Excel)            |
|                             | Kreditora rēķina dokuments (LT) (Excel)            |
|                             | Kreditora rēķina dokuments (LV) (Excel)            |
|                             | Kreditora rēķina dokuments (MY) (Excel)            |
|                             | Kreditora rēķina dokuments (Word)                  |
| Pasūtījuma modelis                 | Līguma apstiprināšana (Excel)                  |
|                             | Līguma apstiprināšana (Word)                   |
|                             | Pirkšanas līguma apstiprināšana (Excel)         |
|                             | Pirkšanas līguma apstiprināšana (Word)          |
|                             | Pirkšanas pasūtījums (Excel)                          |
|                             | Pirkšanas pasūtījums (CZ) (Excel)                     |
|                             | Pirkšanas pasūtījuma pieprasījums (CZ) (Excel)             |
|                             | Pirkšanas pasūtījums (HU) (Excel)                     |
|                             | Pirkšanas pasūtījuma pieprasījums (HU) (Excel)             |
|                             | Pirkšanas pasūtījums (Word)                           |
|                             | Pirkšanas pasūtījuma pieprasījums (Excel)                  |
|                             | Pirkšanas pasūtījuma pieprasījums (Word)                   |
|                             | Pārdošanas pasūtījuma apstiprinājums (Excel)                |
|                             | Pārdošanas pasūtījuma apstiprinājums (CZ) (Excel)           |
|                             | Pārdošanas pasūtījuma apstiprinājums (HU) (Excel)           |
|                             | Pārdošanas pasūtījuma apstiprinājums (Word)                 |
| Iepakojumu saraksta modelis          | Konteinera saturs (Excel)                      |
|                             | Konteinera saturs (Word)                       |
|                             | Kravu saraksts (Excel)                               |
|                             | Kravu saraksts (Word)                                |
|                             | Izdošanas saraksts (Excel)                            |
|                             | Izdošanas saraksts (CZ) (Excel)                       |
|                             | Izdošanas saraksts (Word)                             |
|                             | Ražošanas izdošanas saraksts (Excel)                    |
|                             | Ražošanas izdošanas saraksts (Word)                     |
|                             | Kravas piegādes izdošanas saraksts (Excel)             |
|                             | Kravas piegādes izdošanas saraksts (Word)              |
|                             | Kravas piegādes izdošanas saraksts (Excel)         |
|                             | Kravas piegādes izdošanas saraksts (Word)          |
|                             | Kravas piegādesk izdošanas saraksta kopums (Excel)             |
|                             | Kravas piegādes izdošanas saraksta kopums (Word)              |
| Maksājuma modelis               | Debitora maksājuma paziņojums (Excel)                 |
|                             | Debitora maksājuma paziņojums (Word)                  |
|                             | Kreditora maksājuma pievienošana (Excel)                   |
|                             | Kreditora maksājuma pievienošana (Word)                    |
| Piedāvājuma modelis             | Projekta piedāvājums (Excel)                       |
|                             | Projekta piedāvājums (Word)                        |
|                             | Piedāvājuma pieprasījums (Excel)                   |
|                             | Piedāvājuma pieprasījums (Pieņemt) (Excel)          |
|                             | Piedāvājuma pieprasījums (Pieņemt) (Word)           |
|                             | Piedāvājuma pieprasījums (Noraidīt) (Excel)          |
|                             | Piedāvājuma pieprasījums (Noraidīt) (Word)           |
|                             | Piedāvājuma pieprasījums (Atgriezt) (Excel)          |
|                             | Piedāvājuma pieprasījums (Atgriezt) (Word)           |
|                             | Piedāvājumu pieprasījums (Word)                    |
|                             | Pārdošanas piedāvājums (Excel)                         |
|                             | Pārdošanas piedāvājums (CZ) (Excel)                    |
|                             | Pārdošanas piedāvājums (HU) (Excel)                    |
|                             | Pārdošanas piedāvājums (Word)                          |
|                             | Pārdošanas pasūtījuma apstiprinājums (Excel)            |
|                             | Pārdošanas pasūtījuma apstiprinājums (Word)             |
| Saskaņošanas modelis        | Cust konta pārskats, Ext (Excel)             |
|                             | Cust konta pārskats, Ext (CN) (Excel)        |
|                             | Cust konta pārskats, Ext (Word)              |
|                             | Cust konta pārskats, Ext, Francija (Excel)          |
| Atgādinājuma modelis              | Atgādinājuma vēstules piezīmes (Excel)                  |
|                             | Atgādinājuma vēstules piezīmes (CN) (Excel)             |
|                             | Atgādinājuma vēstules piezīmes (Word)                   |
|                             | Debitora procentu piezīmes (Excel)                  |
|                             | Debitora procentu piezīmes (Word)                   |
| Ceļazīmes modelis               | Kravas norēķini (Excel)                             |
|                             | Kravas norēķini (Word)                              |
|                             | Pirkšanas pasūtījuma pavadzīme (Excel)             |
|                             | Pirkšanas pasūtījuma pavadzīme (CZ) (Excel)        |
|                             | Pirkšanas pasūtījuma pavadzīme (Word)              |
|                             | Maršruts (Excel)                                   |
|                             | Maršruts (Word)                                    |
|                             | Pārdošanas pasūtījuma pavadzīme (Excel)                |
|                             | Pārdošanas pasūtījuma pavadzīme (CZ) (Excel)           |
|                             | Pārdošanas pasūtījuma pavadzīme (LT) (Excel)           |
|                             | Pārdošanas pasūtījuma pavadzīme (PL) (Excel)           |
|                             | Pārdošanas pasūtījuma pavadzīme (Word)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
