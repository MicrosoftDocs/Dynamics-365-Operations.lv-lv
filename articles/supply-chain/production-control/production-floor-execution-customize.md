---
title: Ražošanas izpildes interfeisa pielāgošana
description: Šajā tēmā ir paskaidrots, kā paplašināt pašreizējās veidlapas vai izveidot jaunas veidlapas un pogas ražošanas grīdas izpildes interfeisam.
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
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790982"
---
# <a name="customize-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa pielāgošana

[!include [banner](../includes/banner.md)]

Izstrādātāji var paplašināt pašreizējās veidlapas vai izveidot savas formas un pogas ražošanas grīdas izpildes saskarnei. Pēc šo jauno elementu koda pievienošanas administratori vai ražotnes vadītāji tos var viegli pievienot interfeisam, izmantojot standarta konfigurācijas vadīklas.

Piemēram, šeit ir daži no iespējamiem risinājumiem, ja galvenajā formā ir nepieciešamas jaunas kolonnas:

- Paplašiniet `JmgProductionFloorExecutionMainGrid` veidlapu un pievienojiet vēlamos laukus.
- Izveidojiet jaunu veidlapu un pievienojiet to kā jaunu galveno skatu (cilni).

## <a name="add-a-new-button-action"></a>Pievienot jaunu pogu (darbība)

Lai pievienotu jaunu pogu (darbību), veiciet tālāk norādītās darbības, lai izveidotu klasi, kas īsteno jūsu pielāgoto darbību.

1. Izveidojiet jaunu klasi ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, kur:

    - `<ExtensionPrefix>` unikāli identificē jūsu risinājumu, parasti izmantojot uzņēmuma nosaukumu.
    - `<ActionName>` ir unikāls klases nosaukums. Tas parasti identificē darbības veidu.

1. Jaunajai klasei jāpaplašina `JmgProductionFloorExecutionAction` klase.
1. Ignorēt visas nepieciešamās metodes.

Piemēram, skatiet kodu šādām klasēm:

- `JmgProductionFloorExecutionBreakAction`– Klase vienkāršai darbībai, kurai nav nepieciešami nekādi ieraksti.
- `JmgProductionFloorExecutionReportFeedbackAction`– Klase, kas nodrošina sarežģītāku funkcionalitāti.

Kad esat pabeidzis, jaunā poga (darbība) tiks automātiski norādīta **·** Microsoft cilnēs Noformējums. Dynamics 365 Supply Chain Management Tur jūs (vai administrators vai grīdas pārvaldnieks) varat to viegli pievienot primārajai vai sekundārajai rīkjoslai, tāpat kā varat pievienot standarta pogas. Norādījumus skatiet [Design the production floor execution interface](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Jauna galvenā skata pievienošana

1. Izveidojiet jaunu formu, kurā ir vēlamie elementi un funkcionalitāte. Ņemiet vērā, ka šī veidlapa ir jauna veidlapa, nevis paplašinājums. Piešķiriet veidlapai nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, kur:

    - `<ExtensionPrefix>` unikāli identificē jūsu risinājumu, parasti izmantojot uzņēmuma nosaukumu.
    - `<FormName>` ir unikāls veidlapas nosaukums.

1. Izveidojiet izvēlnes elementu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Izveidojiet paplašinājumu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kur metode tiek `getMainMenuItemsList` paplašināta, sarakstam pievienojot jauno izvēlnes elementu. Šajā kodā ir parādīts piemērs.

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

Kad esat pabeidzis, jaunais galvenais skats tiks automātiski norādīts **piegādes ķēdes pārvaldības cilnes lapas** Noformējums galvenajā skata kombinētajā **·** lodziņā. Tur jūs (vai administrators vai grīdas pārvaldnieks) varat to viegli pievienot jaunām vai esošām cilnēm, tāpat kā varat pievienot standarta galvenos skatus. Norādījumus skatiet [Design the production floor execution interface](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Detalizētas informācijas skata pievienošana

1. Izveidojiet jaunu formu, kurā ir vēlamie elementi un funkcionalitāte. Ņemiet vērā, ka šī veidlapa ir jauna, nevis paplašinājums. Piešķiriet veidlapai nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, kur: 

    - `<ExtensionPrefix>` unikāli identificē jūsu risinājumu, parasti izmantojot uzņēmuma nosaukumu.
    - `<FormName>` ir unikāls veidlapas nosaukums.

1. Izveidojiet izvēlnes elementu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Izveidojiet paplašinājumu ar nosaukumu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kur metode tiek `getDetailsMenuItemList` paplašināta, sarakstam pievienojot jauno izvēlnes elementu.

Kad esat pabeidzis, jaunais detalizētas informācijas skats tiks automātiski norādīts **piegādes ķēdes pārvaldības cilnes lapas Cilnes** Noformējums kombinētā lodziņā Detalizēta **·** informācija. Tur jūs (vai administrators vai grīdas pārvaldnieks) varat to viegli pievienot jaunām vai esošām cilnēm, tāpat kā varat pievienot standarta informācijas skatus. Norādījumus skatiet [Design the production floor execution interface](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Ciparu tastatūras pievienošana formai vai dialogam

Šajā piemērā parādīts, kā veidlapai pievienot ciparu tastatūras.

1. Katrā formā esošo ciparu tastatūras kontrolleru skaitam ir jābūt vienādam ar ciparu tastatūru skaitu šajā formā.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Iestatiet katra ciparu tastatūras kontrollera darbību un savienojiet katru ciparu tastatūras kontrolleri ar ciparu tastatūru.

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

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Ciparu tastatūras izmantošana uznirstošajā dialogā

Šajā piemērā ir parādīts viens veids, kā uznirstošajam dialogam iestatīt ciparu tastatūras kontrolleri.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Šajā piemērā ir parādīts viens veids, kā izsaukt cipartastatūras uznirstošo dialogu.

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
