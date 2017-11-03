---
title: "Analīzes pievienošana darbvietām, izmantojot Power BI Embedded"
description: "Šajā tēmā ir parādīts, kā iegult Power BI pārskatu darbvietas cilnē Analīze."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Platform
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.intro: Platform update 8
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: fc8102d945faf9ad533f57ec1a45b0e0dc344963
ms.openlocfilehash: d36abbf7c08c56d84ed83dbec1bfa33f30b47ef5
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Analīzes pievienošana darbvietām, izmantojot Power BI Embedded

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Šis līdzeklis tiek atbalstīts programmā Dynamics 365 for Finance and Operations (versija 7.2 un jaunākas versijas).

# <a name="introduction"></a>Ievads
Šajā tēmā ir parādīts, kā iegult Microsoft Power BI pārskatu darbvietas cilnē **Analīze**. Šeit sniegtā piemēra ietvaros paplašināsim darbvietu **Rezervēšanas pārvaldība** autoparka pārvaldības programmā, lai cilnē **Analīze** iegultu analītisku darbvietu.

# <a name="prerequisites"></a>Priekšnosacījumi
+ Piekļuve izstrādātāju videi, kas darbina platformas 8. atjauninājumu vai jaunāku atjauninājumu.
+ Analītisks pārskats (.pbix fails), kas tika izveidots, izmantojot programmu Microsoft Power BI Desktop, un kam ir no elementu krātuves datu bāzes iegūts datu modelis.

# <a name="overview"></a>Pārskats
Neatkarīgi no tā, vai paplašināt esošu programmas darbvietu vai ieviešat jaunu darbvietu, varat izmantot iegultos analītiskos skatus, lai nodrošinātu visaptverošus un interaktīvus biznesa datu skatus. Analītiskās darbvietas cilnes pievienošanas procesā ir četras darbības.

1. Pievienojiet .pbix failu kā Dynamics 365 resursu.
2. Definējiet analītiskās darbvietas cilni.
3. Ieguliet .pbix resursu darbvietas cilnē.
4. Neobligāti: pievienojiet paplašinājumus, lai pielāgotu skatu.

> [!NOTE]
> Papildinformāciju par to, kā izveidot analītiskus pārskatus, skatiet rakstā [Darba sākšana ar Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/). Šī lapa ir lielisks informācijas avots, kas var palīdzēt jums izveidot pārliecinošus analītisko pārskatu risinājumus.

# <a name="add-a-pbix-file-as-a-resource"></a>.pbix faila kā resursa pievienošana
Pirms sākat, izveidojiet vai iegūstiet Power BI pārskatu, ko iegulsit darbvietā. Papildinformāciju par to, kā izveidot analītiskus pārskatus, skatiet rakstā [Darba sākšana ar Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).
 
Izpildiet tālāk norādītās darbības, lai pievienotu .pbix failu kā Visual Studio projekta artefaktu.

1. Izveidojiet jaunu projektu atbilstošajā modelī.
2. Risinājumu pārlūkā atlasiet projektu, noklikšķiniet uz tā ar peles labo pogu un pēc tam atlasiet **Pievienot** > **Jauns vienums**.
3. Dialoglodziņa **Pievienot jaunu vienumu** sadaļā **Operāciju artefakti** atlasiet veidni **Resurss**.
4. Ievadiet nosaukumu, kas tiks izmantots kā atsauce uz pārskatu X++ metadatos, un pēc tam noklikšķiniet uz **Pievienot**.

    ![Dialoglodziņš Pievienot jaunu vienumu](media/analytical-workspace-add.png)

5. Atrodiet .pbix failu, kas satur analītiskā pārskata definīciju, un pēc tam noklikšķiniet uz **Atvērt**.

    ![Dialoglodziņš Atlasīt resursa failu](media/analytical-workspace-select-resource.png)
  
Tagad, kad esat pievienojis .pbix failu kā Dynamics 365 resursu, varat iegult pārskatus darbvietās un pievienot tiešās saites, izmantojot izvēlnes elementus.

# <a name="add-a-tab-control-to-an-application-workspace"></a>Cilnes vadīklas pievienošana programmas darbvietai
Šajā piemērā paplašināsim darbvietu **Rezervēšanas pārvaldība** autoparka pārvaldības modelī, pievienojot cilni **Analīze** formas **FMClerkWorkspace** definīcijai.
 
Tālāk esošajā attēlā parādīts, kā forma **FMClerkWorkspace** izskatās Microsoft Visual Studio noformētājā.

![Forma FMClerkWorkspace pirms izmaiņām](media/analytical-workspace-definition-before.png)

Veiciet tālāk norādītās darbības, lai paplašinātu formas definīciju darbvietai **Rezervēšanas pārvaldība**.

1. Atveriet formu noformētāju, lai paplašinātu noformējuma definīciju.
2. Noformējuma definīcijā atlasiet augšējo elementu, kas ir apzīmēts kā **Noformējums|modelis: operatīvā darbvieta**.
3. Noklikšķiniet ar peles labo pogu un atlasiet **Jauns** > **Cilne**, lai pievienotu jaunu vadīklu ar nosaukumu **FormTabControl1**.
4. Formu noformētājā atlasiet vienumu **FormTabControl1**.
5. Noklikšķiniet ar peles labo pogu un atlasiet vienumu **Jauna cilnes lapa**, lai pievienotu jaunu cilnes lapu.
6. Pārdēvējiet cilnes lapu uz kaut ko atpazīstamu, piemēram, **Darbvieta**.
7. Formu noformētājā atlasiet vienumu **FormTabControl1**.
8. Noklikšķiniet ar peles labo pogu un atlasiet vienumu **Jauna cilnes lapa**.
9. Pārdēvējiet cilnes lapu uz kaut ko atpazīstamu, piemēram, **Analīze**.
10. Formu noformētājā atlasiet vienumu **Analīze (cilnes lapa)**.
11. Rekvizītu **Paraksts** iestatiet uz **Analīze**.
12. Noklikšķiniet ar peles labo pogu uz vadīklas un atlasiet **Jauns** > **Grupa**, lai pievienoju jaunu formu grupas vadīklu.
13. Pārdēvējiet formu grupu uz kaut ko atpazīstamu, piemēram, **powerBIReportGroup**.
14. Formu noformētājā atlasiet vienumu **PanoramaBody (cilne)** un pēc tam velciet vadīklu uz cilni **Darbvieta**.
15. Noformējuma definīcijā atlasiet augšējo elementu, kas ir apzīmēts kā **Noformējums|modelis: operatīvā darbvieta**.
16. Noklikšķiniet ar peles labo pogu un atlasiet vienumu **Noņemt modeli**.
17. Vēlreiz noklikšķiniet ar peles labo pogu un atlasiet **Pievienot modeli** > **Darbvieta ar cilnēm**.
18. Veiciet būvējumu, lai pārbaudītu veiktās izmaiņas.
 
Tālāk esošajā attēlā parādīts, kā noformējums izskatās pēc šo izmaiņu lietošanas.

![FMClerkWorkspace pēc izmaiņām](media/analytical-workspace-definition-after.png)

Tagad, kad esat pievienojis formu vadīklas, kas tiks izmantotas darbvietas pārskata iegulšanai, jums ir jādefinē vecākobjekta vadīklas lielums tā, lai varētu izvietot izkārtojumu. Pēc noklusējuma pārskatā būs redzama gan lapa **Filtru rūts**, gan lapa **Cilne**. Tomēr šo vadīklu redzamību var mainīt pēc nepieciešamības pārskata mērķa patērētājam.
 
> [!NOTE]
> Iegultajām darbvietām ieteicams izmantot paplašinājumus, lai konsekvences nolūkā paslēptu gan lapu **Filtru rūts**, gan lapu **Cilne**.
 
Esat pabeidzis programmas formas definīcijas paplašināšanas uzdevumu. Papildinformāciju par to, kā izmantot paplašinājumus pielāgojumu veikšanai, skatiet rakstā [Pielāgošana: pārklāšanās un paplašinājumi](../extensibility/customization-overlayering-extensions.md).

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a>X++ biznesa loģikas pievienošana skatītāja vadīklas iegulšanai
Izpildiet tālāk norādītās darbības, lai pievienotu biznesa loģiku, kas inicializē pārskatu skatītāja vadīklu, kas ir iegulta darbvietā **Rezervēšanas pārvaldība**.

1. Atveriet formu noformētāju **FMClerkWorkspace**, lai paplašinātu noformējuma definīciju.
2. Nospiediet taustiņu F7, lai piekļūtu koda definīcijas kodam.
3. Pievienojiet tālāk norādīto X++ kodu.

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Veiciet būvējumu, lai pārbaudītu veiktās izmaiņas.

Esat pabeidzis uzdevumu ar biznesa loģikas pievienošanu, kas inicializē iegulto pārskatu skatītāja vadīklu. Tālāk esošajā attēlā parādīts, kā darbvieta izskatās pēc šo izmaiņu lietošanas.

![Pārskats iegults darbvietā](media/analytical-workspace-final.png)

> [!NOTE]
> Esošajam darbības skatam varat piekļūt, izmantojot darbvietas cilnes zem lapas virsraksta.

# <a name="reference"></a>Atsauce

## <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl metode
Šajā sadaļā sniegta informācija par palīga klasi, kas tiek izmantota, lai Power BI pārskatu (.pbix resursu) iegultu formu grupas vadīklā.

### <a name="syntax"></a>Sintakse
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a>Parametri

| Nosaukums | Apraksts |
|---|---|
| resourceName | .pbix resoursa nosaukums. |
| formGroupControl | Formu grupas vadīkla, kam jālieto Power BI pārskatu vadīkla. |
| defaultPageName | Noklusējuma lapas nosaukums. |
| showFilterPane | Būla vērtība, kas norāda, vai filtra rūts jārāda (**Patiess**) vai jāpaslēpj (**Aplams**). |
| showNavPane | Būla vērtība, kas norāda, vai navigācijas rūts jārāda (**Patiess**) vai jāpaslēpj (**Aplams**). |
| defaultFilters | Noklusējuma filtri Power BI pārskatam. |

