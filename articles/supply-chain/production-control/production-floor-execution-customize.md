---
title: Ražošanas izpildes interfeisa pielāgošana
description: Šajā tēmā skaidrots, kā paplašināt pašreizējās formas vai izveidot jaunas formas un pogas ražošanas izpildes interfeisam.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ad5037442f27a5068b38613655591f1298808eac
ms.sourcegitcommit: 28537b32dbcdefb1359a90adc6781b73a2fd195e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712948"
---
# <a name="customize-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa pielāgošana

[!include [banner](../includes/banner.md)]

Izstrādātāji var paplašināt pašreizējās formas vai izveidot savas formas un pogas ražošanas izpildes interfeisam. Pēc šo jauno elementu koda pievienošanas administratori vai ražotnes vadītāji var viegli pievienot tos interfeisam, izmantojot standarta konfigurācijas kontroles.

Piemēram, šeit ir daži no iespējamajiem risinājumiem, ja galvenajā formā nepieciešamas jaunas kolonnas:

- Paplašināt formu `JmgProductionFloorExecutionMainGrid` un pievienot vēlamos laukus.
- Izveidojiet jaunu formu un pievienojiet to kā jaunu galveno skatu (cilne).

## <a name="add-a-new-button-action"></a>Pievienot jaunu pogu (darbība)

Lai pievienotu jaunu pogu (darbību), sekojiet šiem soļiem, lai izveidotu klasi, kas ievieš pielāgoto darbību.

1. Izveidojiet jaunu klasi ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, kur:

    - `<ExtensionPrefix>` unikāli identificē risinājumu, parasti izmantojot uzņēmuma nosaukumu.
    - `<ActionName>` ir unikāls klases nosaukums. Parasti tas identificē darbības veidu.

1. Jaunajai klasei jāpaplašina `JmgProductionFloorExecutionAction` klase.
1. Ignorē visas nepieciešamās metodes.

Piemēram, aplūkojiet kodu šādām klasēm:

- `JmgProductionFloorExecutionBreakAction`– klase vienkāršai darbībai, kurā nav nepieciešami ieraksti.
- `JmgProductionFloorExecutionReportFeedbackAction`– klase, kas nodrošina sarežģītāku funkcionalitāti.

Kad esat beidzis, jaunā poga (darbība) automātiski tiks uzskaitīta **Microsoft cilnes** lapā Dizains Dynamics 365 Supply Chain Management. Tur jūs (vai administrators vai stāva pārvaldnieks) varat viegli pievienot to primārajai vai sekundārajai rīkjoslai, tāpat kā jūs varat pievienot standarta pogas. Norādījumus skatiet sadaļā Ražošanas [izpildes interfeisa dizains](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Pievienot jaunu galveno skatu

1. Izveidojiet jaunu formu, kurā ir vēlamais elements un funkcionalitāte. Ievērojiet, ka šī forma ir jauna forma, nevis paplašinājums. Nosaukiet formu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, kur:

    - `<ExtensionPrefix>` unikāli identificē risinājumu, parasti izmantojot uzņēmuma nosaukumu.
    - `<FormName>` ir unikāls formas nosaukums.

1. Izveidojiet izvēlnes elementu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Izveidojiet paplašinājumu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kur metode `getMainMenuItemsList` tiek paplašināta, pievienojot sarakstam jaunu izvēlnes elementu. Šajā kodā parādīts piemērs.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Pēc pabeigšanas jaunais **galvenais** **skatījums automātiski tiks uzskaitīts** Galvenā skata kombinētajā lodziņā Cilnes Dizains lapā Piegādes ķēžu pārvaldība. Tur varat (vai arī administratora vai stāva pārvaldnieks) viegli pievienot to jaunām vai esošajām cilnēm, tāpat kā jūs varat pievienot standarta galvenos skatus. Norādījumus skatiet sadaļā Ražošanas [izpildes interfeisa dizains](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Pievienot detalizētu skatu

1. Izveidojiet jaunu formu, kurā ir vēlamais elements un funkcionalitāte. Ievērojiet, ka šī forma ir jauna, nevis paplašinājums. Nosaukiet formu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, kur: 

    - `<ExtensionPrefix>` unikāli identificē risinājumu, parasti izmantojot uzņēmuma nosaukumu.
    - `<FormName>` ir unikāls formas nosaukums.

1. Izveidojiet izvēlnes elementu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Izveidojiet paplašinājumu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kur metode `getDetailsMenuItemList` tiek paplašināta, pievienojot sarakstam jaunu izvēlnes elementu.

Pēc pabeigšanas jaunās informācijas **skats** **automātiski tiks uzskaitīts Piegādes ķēdes pārvaldības cilnes lapas Detalizētas** informācijas skata kombinētajā lodziņā. Tur varat (vai arī administratora vai stāva pārvaldnieks) viegli pievienot to jaunām vai esošajām cilnēm, tāpat kā jūs varat pievienot standarta detalizētas informācijas skatus. Norādījumus skatiet sadaļā Ražošanas [izpildes interfeisa dizains](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Pievienot formai vai dialogam skaitlisku iestatījumu

Šajā piemērā parādīts, kā formai pievienot ciparus.

1. Skaitlisko kontrolleru skaitam, kas ir katrai formai, ir jābūt vienādam ar šīs formas skaitlisko vērtību skaitu.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Iestatiet katra skaitliskā kontrollera darbību un savienojiet katru skaitlisko cipara kontrolleri ar skaitlisko cipara formas daļu.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Izmantot ciparu dialogu ar uznirstošo logu

Šajā piemērā parādīts viens veids, kā uznirstošam dialogam iestatīt skaitlisku kontrolleri.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Šajā piemērā parādīts viens veids, kā izsaukt skaitlisko uznirstošo dialogu.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Datuma un laika kontroļu pievienošana formai vai dialogam

Šajā sadaļā ir parādīts, kā formai vai dialogam pievienot datuma un laika kontroles. Skārienejošais datums un laiks kontrolē, lai darbinieki varētu norādīt datumus un laikus. Šajā ekrānuzņēmumā ir parādīts, kā vadīklas parasti tiek parādītas lapā. Laika kontrole nodrošina gan 12 stundu, gan 24 stundu versijas; Parādītā versija sekos lietotāja konta preferenču kopai, zem kuras interfeiss darbojas.

![Datuma kontroles piemērs.](media/pfe-customize-date-control.png "Datuma kontroles piemērs")

![Laika kontroles piemērs ar 12 stundu pulksteni.](media/pfe-customize-time-control-12h.png "Laika kontroles piemērs ar 12 stundu pulksteni")

![Laika kontroles piemērs ar 24 stundu ierašanos.](media/pfe-customize-time-control-24h.png "Laika kontroles piemērs ar 24 stundu pulksteni")

Šajā procedūrā parādīts piemērs, kā formai pievienot datuma un laika kontroles.

1. Pievienojiet formai kontrolleri katrai datuma un laika kontrolei, ko formai vajadzētu ietvert. (Kontrolleru skaitam formā jābūt vienādam ar datuma un laika kontroļu skaitu.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Norādiet nepieciešamos mainīgos (ar tipu `utcdatetime`).

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Izveidojiet metodes, kuru datetime atjaunina datuma un laika kontrolleri. Šajā piemērā parādīta viena šāda metode.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Iestatiet katra datuma un laika kontrollera darbību un savienojiet katru kontrolleri ar formas daļu. Šajā piemērā parādīts, kā iestatīt datus kontrolkontrolēm Datums-no un Laiks no. Varat pievienot līdzīgu kodu kontrolei "no datuma līdz" un "no laika uz" (netiek rādīts).

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Ja nepieciešama datuma kontrole, varat izlaist laika kontroles iestatīšanu un tā vietā iestatīt datuma kontroli tā, kā parādīts šajā piemērā:

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Papildu resursi

- [Ražošanas izpildes interfeisa stils](production-floor-execution-styles.md)
- [Ražošanas izpildes interfeisa noformēšana](production-floor-execution-tabs.md)
