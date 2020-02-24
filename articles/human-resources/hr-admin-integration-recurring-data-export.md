---
title: Periodiskas datu eksportēšanas programmas izveide
description: Šajā rakstā parādīts, kā izveidot Microsoft Azure loģikas programmu, kas eksportē datus no Microsoft Dynamics 365 Human Resources uz periodisku grafiku.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edd4b999624a845fc145ed9ff348ae9cba782719
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009764"
---
# <a name="create-a-recurring-data-export-app"></a>Periodiskas datu eksportēšanas programmas izveide

Šajā rakstā parādīts, kā izveidot Microsoft Azure loģikas programmu, kas eksportē datus no Microsoft Dynamics 365 Human Resources uz periodisku grafiku. Lai eksportētu datus, apmācība izmanto Human Resources DMF pakotnes REST programmas programmēšanas interfeisa (API) sniegtās priekšrocības. Kad dati ir eksportēti, loģikas programma saglabā eksportēto datu pakotni Microsoft OneDrive biznesam mapē.

## <a name="business-scenario"></a>Biznesa scenārijs

Vienā tipiskā biznesa scenārijā Microsoft Dynamics 365 integrācijām, dati periodiskā grafikā ir jāeksportē uz pakārtoto sistēmu. Šajā apmācībā parādīts, kā eksportēt visus nodarbinātā ierakstus no Microsoft Dynamics 365 Human Resources un saglabāt nodarbināto sarakstu OneDrive biznesam mapē.

> [!TIP]
> Konkrētie dati, kas tiek eksportēti šajā apmācībā, un eksportēto datu galamērķis ir tikai piemēri. Tos var viegli mainīt, lai atbilstu jūsu biznesa vajadzībām.

## <a name="technologies-used"></a>Izmantotās tehnoloģijas

Šī apmācība izmanto tālāk minētās tehnoloģijas.

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** — pamatdatu avots par nodarbinātajiem, kas tiks eksportēts.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** — tehnoloģija, kas nodrošina periodiskās eksportēšanas saskaņošanu un plānošanu.

    - **[Savienotāji](https://docs.microsoft.com/azure/connectors/apis-list)** — tehnoloģija, kas tiek izmantota, lai savienotu loģikas programmu ar nepieciešamajiem galapunktiem.

        - [HTTP ar Azure AD](https://docs.microsoft.com/connectors/webcontents/) savienotāju
        - [OneDrive biznesam](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) savienotājs

- **[DMF pakotnes REST API](../dev-itpro/data-entities/data-management-api.md)** — tehnoloģija, kas tiek izmantota, lai izraisītu eksportēšanu un pārraudzītu tā norisi.
- **[OneDrive biznesam](https://onedrive.live.com/about/business/)** — eksportēto nodarbināto galamērķis.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākt vingrinājumu šajā apmācībā, nepieciešami tālāk minētie vienumi.

- Human Resources vide, kam ir administratora līmeņa atļaujas vidē
- [Azure abonements](https://azure.microsoft.com/free/), lai viesotu loģikas programmu

## <a name="the-exercise"></a>Vingrinājums

Šī vingrinājuma beigās jums būs loģikas programma, kas ir savienota ar jūsu Human Resources vidi un jūsu OneDrive biznesam kontu. Loģikas programma eksportēs datu pakotni no Human Resources, gaidiet, kamēr tiks pabeigta eksportēšana, lejupielādējiet eksportēto datu pakotni un saglabājiet to OneDrive biznesam norādītajā mapē.

Pabeigtā loģikas programma būs līdzīga tālāk redzamajam attēlam.

![Loģikas programmas pārskats](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>1. darbība: datu eksportēšanas projekta izveide Human Resources

Human Resources izveidojiet datu eksportēšanas projektu, kas eksportē nodarbinātos. Nosauciet projektu **Nodarbināto eksportēšana** un pārliecinieties, ka opcija **Ģenerēt datu pakotni** ir iestatīta uz **Jā**. Pievienojiet projektam atsevišķu elementu (**Nodarbinātais**) un atlasiet formātu tā eksportēšanai. (Šajā pamācībā tiek izmantots Microsoft Excel formāts.)

![Nodarbināto datu projekta eksportēšana](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Atcerieties datu eksportēšanas projekta nosaukumu. Tas būs nepieciešams, nākamajā darbībā veidojot loģikas programmu.

### <a name="step-2-create-the-logic-app"></a>2. darbība: loģikas programmas izveide

Vingrinājuma lielākā daļa ietver loģikas programmas izveidi.

1. Izveidojiet loģikas programmu Azure portālā.

    ![Loģikas programmas izveides lapa](media/integration-logic-app-creation-1.png)

2. Logic Apps Designer sāciet ar tukšu loģikas programmu.
3. Pievienojiet [Periodiskuma grafika trigeri](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence), lai palaistu loģikas programmu ik pēc 24 stundām (vai saskaņā ar izvēlēto grafiku).

    ![Periodiskuma dialoglodziņš](media/integration-logic-app-recurrence-step.png)

4. Izsauciet [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API, lai ieplānotu savas datu pakotnes eksportēšanu.

    1. Izmantojiet darbību **Izsaukt HTTP pieprasījumu** no HTTP ar Azure AD savienotāju.

        - **Pamatresursa URL:** jūsu Human Resources vides URL (neietver ceļa/nosaukumvietas informāciju.)
        - **Azure AD Resursa URI:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Human Resources pakalpojums vēl nenodrošina savienotāju, kas sniedz visus API, kas veido DMF pakotnes REST API, piemēram, **ExportToPackage**. Tā vietā jāizsauc API, izmantojot neapstrādātus HTTPS pieprasījumus, izmantojot HTTP ar Azure AD savienotāju. Šis savienotājs izmanto Azure Active Directory (Azure AD) autentifikācijai un autorizēšanai Human Resources.

        ![HTTP ar Azure AD savienotāju](media/integration-logic-app-http-aad-connector-step.png)

    2. Pierakstieties savā Human Resources vidē, izmantojot HTTP ar Azure AD savienotāju.
    3. Iestatiet HTTP **POST** pieprasījumu, lai izsauktu **ExportToPackage** DMF REST API.

        - **Metode:** POST
        - **Pieprasījuma URL** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Pieprasījuma pamatteksts**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![HTTP pieprasījuma darbības izsaukšana](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Iespējams, vēlēsieties pārdēvēt katru darbību, lai tai būtu nozīme salīdzinājumā ar noklusējuma nosaukumu **Izsaukt HTTP pieprasījumu**. Piemēram, varat pārdēvēt šo darbību **ExportToPackage**.

5. [Mainīga lieluma inicializācija](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable), lai glabātu **ExportToPackage** pieprasījuma izpildes statusu.

    ![Mainīgā lieluma darbības inicializācija](media/integration-logic-app-initialize-variable-step.png)

6. Uzgaidiet, līdz datu eksportēšanas izpildes statuss ir **Sekmīgs**.

    1. Pievienojiet [Līdz cilpai](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop), kas atkārtojas, līdz **ExecutionStatus** mainīgā lieluma vērtība ir **Sekmīgs**.
    2. Pievienojiet darbību **Aizkave**, kas gaida piecas sekundes, pirms aptaujā pašreizējo eksportēšanas izpildes statusu.

        ![Līdz cilpas konteiners](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Iestatiet ierobežojumu skaitu uz **15**, lai uzgaidītu ne vairāk kā 75 sekundes (15 atkārtojumi x 5 sekundes), kamēr eksportēšana tiks pabeigta. Ja eksportēšanai nepieciešams ilgāks laiks, koriģējiet ierobežojumu pēc nepieciešamības.        

    3. Pievienojiet darbību **Izsaukt HTTP pieprasījumu**, lai izsauktu [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, un iestatiet mainīgo lielumu **ExecutionStatus** uz rezultātu no **GetExecutionSummaryStatus** atbildes.

        > Šis paraugs neveic kļūdu pārbaudi. **GetExecutionSummaryStatus** API var atgriezt neveiksmīgus termināļa stāvokļus (t.i., stāvokļus, kas nav **Sekmīgs**). Papildinformāciju skatiet [API dokumentācijā](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Metode:** POST
        - **Pieprasījuma URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Pieprasījuma pamatteksts:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Iespējams, vērtība **Pieprasījuma pamatteksts** būs jāievada vai nu koda skatā, vai arī noformētāja funkciju redaktorā.

        ![HTTP pieprasījuma 2. darbības izsaukšana](media/integration-logic-app-get-execution-status-step.png)

        ![Mainīgā lieluma darbības iestatīšana](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > Darbības **Iestatīt mainīgo lielumu** vērtība (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) atšķirsies no **Izsaukt HTTP 2. pieprasījumu** pamatteksta vērtības, lai arī noformētājs parādīs vērtības vienādi.

7. Iegūstiet eksportējamās pakotnes lejupielādes URL.

    - Pievienojiet darbību **Izsaukt HTTP pieprasījumu**, lai izsauktu [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.

        - **Metode:** POST
        - **Pieprasījuma URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Pieprasījuma pamatteksts:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![Darbība GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. Lejupielādējiet eksportēto pakotni.

    - Pievienojiet HTTP pieprasījumu **GET** (iebūvēta [HTTP savienotāja darbība](https://docs.microsoft.com/azure/connectors/connectors-native-http)), lai no URL lejupielādētu pakotni, kas tika atgriezta iepriekšējā darbībā.

        - **Metode:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Iespējams, vērtība **URI** būs jāievada vai nu koda skatā, vai arī noformētāja funkciju redaktorā.

        ![Darbība HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Šim pieprasījumam nav nepieciešama papildu autentifikācija, jo URL, ko atgriež **GetExportedPackageUrl** API, ietver kopīgotas piekļuves paraksta marķieri, kas piešķir piekļuvi faila lejupielādei.

9. Saglabājiet lejupielādēto pakotni, izmantojot [OneDrive biznesam](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) savienotāju.

    - Pievienojiet OneDrive biznesam [Faila izveides](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) darbību.
    - Ja nepieciešams, pieslēdzieties savam OneDrive biznesam kontam.

        - **Mapes ceļš:** izvelētā mape
        - **Faila nosaukums:** worker\_package.zip
        - **Faila saturs:** iepriekšējās darbības pamatteksts (dinamiskais saturs)

        ![Faila darbības izveide](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>3. darbība: loģikas programmas pārbaude

Lai pārbaudītu loģikas programmu, atlasiet noformētāja pogu **Izpildīt**. Tiks uzsākta loģikas programmas darbību izpilde. Pēc 30 līdz 40 sekundēm loģikas programmai izpilde jāpabeidz, un jūsu OneDrive biznesam mapei jāietver jauns pakotnes fails, kas satur eksportētos nodarbinātos.

Ja tiek ziņots par kļūmi jebkurā darbībā, noformētājā atlasiet kļūdaino darbību un pārbaudiet tās laukus **Ievades** un **Izvades**. Atkļūdojiet un pielāgojiet darbības, kā nepieciešams kļūdu labošanai.

Tālāk redzamajā attēlā ir parādīts, kā izskatās Logic Apps Designer, kad visas loģiskās programmas darbības tiek izpildītas sekmīgi.

![Sekmīga loģikas programmas izpilde](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Kopsavilkums

Šajā apmācībā apguvāt, kā izmantot loģikas programmu, lai eksportētu datus no Human Resources un saglabātu eksportētos datus OneDrive biznesam mapē. Pēc nepieciešamības varat modificēt šīs apmācības darbības, lai pielāgotos sava biznesa vajadzībām.


