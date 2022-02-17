---
title: Ražošanas izpildes interfeisa pielāgošana
description: Šajā tēmā ir paskaidrots, kā paplašināt pašreizējās veidlapas vai izveidot jaunas veidlapas un pogas ražošanas grīdas izpildes saskarnei.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 67fb381cbef6f1673afcaa834666b4a859bdf4e6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066550"
---
# <a name="customize-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa pielāgošana

[!include [banner](../includes/banner.md)]

Izstrādātāji var paplašināt pašreizējās veidlapas vai izveidot savas veidlapas un pogas ražošanas grīdas izpildes saskarnei. Kad esat pievienojis šo jauno elementu kodu, administratori vai veikalu vadītāji var tos viegli pievienot saskarnei, izmantojot standarta konfigurācijas vadīklas.

Piemēram, šeit ir daži no iespējamiem risinājumiem, ja ir nepieciešamas jaunas kolonnas galvenajā formā:

- Pagariniet`JmgProductionFloorExecutionMainGrid` veidlapu un pievienojiet vajadzīgos laukus.
- Izveidojiet jaunu veidlapu un pievienojiet to kā jaunu galveno skatu (cilni).

## <a name="add-a-new-button-action"></a>Pievienot jaunu pogu (darbība)

Lai pievienotu jaunu pogu (darbību), veiciet šīs darbības, lai izveidotu klasi, kas ievieš jūsu pielāgoto darbību.

1. Izveidojiet jaunu klasi ar nosaukumu`<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, kur:

    - `<ExtensionPrefix>` unikāli identificē jūsu risinājumu, parasti izmantojot jūsu uzņēmuma nosaukumu.
    - `<ActionName>` ir unikāls klases nosaukums. Tas parasti norāda darbības veidu.

1. Jaunajai klasei ir jāpaplašina`JmgProductionFloorExecutionAction` klasē.
1. Ignorēt visas nepieciešamās metodes.

Lai iegūtu piemērus, skatiet tālāk norādīto klašu kodu:

- `JmgProductionFloorExecutionBreakAction`– Klase vienkāršai darbībai, kurai nav nepieciešami nekādi ieraksti.
- `JmgProductionFloorExecutionReportFeedbackAction`– Klase, kas nodrošina sarežģītāku funkcionalitāti.

Kad esat pabeidzis, jaunā poga (darbība) automātiski tiks parādīta sarakstā **Dizaina cilnes** lapa Microsoft Dynamics 365 Supply Chain Management. Tur jūs (vai administrators vai grīdas pārvaldnieks) varat to viegli pievienot primārajai vai sekundārajai rīkjoslai, tāpat kā varat pievienot standarta pogas. Norādījumus sk [Izstrādājiet ražošanas grīdas izpildes saskarni](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Pievienojiet jaunu galveno skatu

1. Izveidojiet jaunu veidlapu, kurai ir vēlamie elementi un funkcionalitāte. Ņemiet vērā, ka šī veidlapa ir jauna veidlapa, nevis paplašinājums. Nosauciet formu`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, kur:

    - `<ExtensionPrefix>` unikāli identificē jūsu risinājumu, parasti izmantojot jūsu uzņēmuma nosaukumu.
    - `<FormName>` ir unikāls veidlapas nosaukums.

1. Izveidojiet izvēlnes vienumu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Izveidojiet paplašinājumu ar nosaukumu`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kur`getMainMenuItemsList` metode tiek paplašināta, sarakstam pievienojot jaunu izvēlnes vienumu. Šis kods parāda piemēru.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Kad esat pabeidzis, jaunais galvenais skats automātiski tiks parādīts sarakstā **Galvenais skats** kombinētais lodziņš uz **Dizaina cilnes** lapu piegādes ķēdes pārvaldībā. Tur jūs (vai administrators vai grīdas pārvaldnieks) varat to viegli pievienot jaunām vai esošām cilnēm, tāpat kā varat pievienot standarta galvenos skatus. Norādījumus sk [Izstrādājiet ražošanas grīdas izpildes saskarni](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Pievienojiet detalizētas informācijas skatu

1. Izveidojiet jaunu veidlapu, kurai ir vēlamie elementi un funkcionalitāte. Ņemiet vērā, ka šī veidlapa ir jauna, nevis paplašinājums. Nosauciet formu`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, kur: 

    - `<ExtensionPrefix>` unikāli identificē jūsu risinājumu, parasti izmantojot jūsu uzņēmuma nosaukumu.
    - `<FormName>` ir unikāls veidlapas nosaukums.

1. Izveidojiet izvēlnes vienumu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Izveidojiet paplašinājumu ar nosaukumu`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kur`getDetailsMenuItemList` metode tiek paplašināta, sarakstam pievienojot jaunu izvēlnes vienumu.

Kad esat pabeidzis, jaunais detalizētās informācijas skats automātiski tiks parādīts sarakstā **Detaļas skats** kombinētais lodziņš uz **Dizaina cilnes** lapu piegādes ķēdes pārvaldībā. Tur jūs (vai administrators vai stāva pārvaldnieks) varat to viegli pievienot jaunām vai esošām cilnēm, tāpat kā varat pievienot standarta detalizētās informācijas skatus. Norādījumus sk [Izstrādājiet ražošanas grīdas izpildes saskarni](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Pievienojiet veidlapai vai dialogam ciparu tastatūru

Nākamajā piemērā ir parādīts, kā veidlapai pievienot ciparu tastatūras.

1. Katrā veidlapā ietverto ciparu tastatūras kontrolleru skaitam ir jābūt vienādam ar ciparu tastatūru skaitu šajā veidlapā.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Iestatiet katra ciparu tastatūras kontrollera darbību un savienojiet katru ciparu tastatūras kontrolleri ar ciparu tastatūras formas daļu.

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

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Izmantojiet ciparu tastatūru kā uznirstošo dialoglodziņu

Nākamajā piemērā ir parādīts viens veids, kā iestatīt ciparu tastatūras kontrolleri uznirstošajam dialogam.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Nākamajā piemērā parādīts viens veids, kā izsaukt ciparu tastatūras uznirstošo dialoglodziņu.

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

## <a name="additional-resources"></a>Papildu resursi

- [Ražošanas izpildes interfeisa stils](production-floor-execution-styles.md)
- [Ražošanas izpildes interfeisa noformēšana](production-floor-execution-tabs.md)
