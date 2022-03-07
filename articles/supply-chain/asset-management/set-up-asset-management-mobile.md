---
title: Līdzekļu pārvaldības darbvietas izmantošana
description: Šajā tēmā ir aprakstīts, kā iestatīt Microsoft Dynamics 365 Supply Chain Management un Finance and Operations (Dynamics 365) mobile programmu, lai palaistu Līdzekļu pārvaldības mobilo darbvietu, kuru darbinieki var izmantot, lai veiktu līdzekļu pārvaldības uzdevumus.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5d628f99d4fc6788ddb38590c65decb871d49f93
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572197"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Līdzekļu pārvaldības darbvietas izmantošana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt Microsoft Dynamics 365 Supply Chain Management un Finance and Operations (Dynamics 365) mobile programmu, lai palaistu **Līdzekļu pārvaldības** mobilo darbvietu, kuru darbinieki var izmantot, lai veiktu līdzekļu pārvaldības uzdevumus.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Iestatīt uzturēsanas darbinieku lietotājus Supply Chain Management

Katram lietotājam, kam ir nepieciešama piekļuve **Līdzekļu pārvaldības** mobilajai darbvietai, veiciet šīs darbības.

1. Supply Chain Management dodieties uz **Cilvēkresursi \> Darbinieki** un pārliecinieties, vai lietotājam, kuru vēlaties iestatīt,pastāv darbinieka ieraksts. Izveidojiet jaunu darbinieka ierakstu, ja nepieciešams.
1. Dodieties uz sadaļu **Līdzekļu pārvaldība \> Iestatījumi \> Darbinieki \> Darbinieki** un pārliecinieties, vai iepriekšējā darbībā identificētais (vai izveidotais) darbinieka ieraksts ir kartēts uz darbinieka uzturēšanas ierakstu. Izveidojiet jaunu darbinieka uzturēšanas ierakstu pēc vajadzības un iestatiet lauku **Darbinieks** uz darbinieka ierakstu no iepriekšējā soļa.
1. Dodieties uz sadaļu **Līdzekļu pārvaldība \> Iestatījumi \> Darbinieki \> Uzturēšanas darbinieku grupas** un pārliecinieties, vai iepriekšējā darbībā identificētais (vai izveidotais) darbinieka ieraksts pieder darbinieka uzturēšanas ierakstam.
1. Dodieties uz **Sistēmas administrēšana \> Lietotāji**.
1. Režģī atlasiet atbilstošo lietotāju.
1. Kopsavilkuma cilnē **Lietotāja informācija** iestatiet lauku **Persona** uz darbinieka kontu, kuru vēlaties saistīt ar pašreizējo lietotāja kontu. Šim darbinieka kontam jābūt darbinieka ierakstam, ko 1. solī identificējāt (vai izveidojāt) un kartēts uz darbinieka uzturēšanas ierakstu 2. solī.

> [!NOTE]
> Lietotāju atļaujas un drošības lomas attiecas uz **Līdzekļu pārvaldības** mobilās darbvietas funkcijām, tāpat kā uz Supply Chain Management lietotāja interfeisa funkcijām. Tāpēc katram lietotājam, kuru iestatāt, lai piekļūtu **Līdzekļu pārvaldības** mobilajai darbvietai, jābūt drošības lomām, kurām ir nepieciešamas veikt līdzīgas operācijas tieši Supply Chain Management.

## <a name="publish-the-asset-management-mobile-workspace"></a>Līdzekļu pārvaldības mobilās darbvietas publicēšana

Lai līdzekļu pārvaldības līdzekļi būtu pieejami mobilajā programmā Finance and Operations (Dynamics 365), publicējiet **Līdzekļu pārvaldības** mobilo darbvietu.

1. Supply Chain Management atlasiet pogu **Iestatījumi** (ātrumkārbas simbols augšējā labajā stūrī) un izvēlnē atlasiet **Mobilā programma**.
1. Dialoglodziņā **Pārvaldīt mobilo programmu** atrodiet elementu **Līdzekļu pārvaldība**. Ja tajā ir teksts "Metadatos - nav publicēti", darbalauks vēl nav publicēts. Ja tajā ir teksts "Metadatos - publicēts", darbvieta jau ir publicēta, un jūš varat izlaist šīs procedūras atlikušo daļu.

    ![Pārvaldīt mobilās programmas dialoglodziņu.](media/mobile-workspaces.png "Pārvaldīt mobilās programmas dialoglodziņu")

1. Atlasiet elementu **Līdzekļu pārvaldība** un pēc tam rīkjoslā atlasiet **Publicēt**. Pēc dažām sekundēm jums jāsaņem paziņojums par to, ka darbvietas publicēšana ir veiksmīgi pabeigta. Turklāt elementa tekstam jāmainās uz "Metadatos — publicēts."

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Instalējiet un iestatiet Finance and Operations (Dynamics 365) mobilo programmu

1. Lai mobilajā ierīcē instalētu **Microsoft Finance and Operations (Dynamics 365) programmu**, dodieties uz vienu no tālāk minētajiem programmu veikaliem:

    - [Google Android ierīcēm](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Apple iOS ierīcēm](https://go.microsoft.com/fwlink/?linkid=850663)

1. Atveriet Finance and Operations (Dynamics 365) programmu. Jāparādās pierakstīšanās lapai. **Pieteikšanās** laukā ievadiet Supply Chain Management URL vai atlasiet neseno URL sarakstā **Jaunākās vides** un pēc tam nospiediet **Savienot**.

    ![Pierakstīšanās lapa.](media/mobile-app-sign-in.png "Pierakstīšanās lapa")

1. Ja tiek piedāvāts apstiprināt savienojumu, atzīmējiet izvēles rūtiņu **Es saprotu** un pēc tam nospiediet taustiņu **Savienot**.
1. Lapā **Konta izvēle** izmantojiet Microsoft kontu, lai pieteiktos mobilajā programmā.

    Tiek atvērta lapa **Darbvietas**. Tas uzskaita katru mobilo darbvietu, ko publicējusi jūsu Supply Chain Management instance.

    ![Darbvietu saraksts.](media/mobile-app-workspaces.png "Darbvietu saraksts")

1. Ja jāmaina juridiskā persona (uzņēmums), augšējā kreisajā stūrī klikšķiniet pogu Izvēlne (dažreiz tiek saukta par hamburgera pogu) un pēc tam nospiediet **Mainīt uzņēmumu**.

    ![Juridiskās personas maiņa.](media/mobile-app-change-comp.png "Juridiskās personas maiņa")

1. Lapā **Darbvietas** atlasiet darbvietu, ar kuru vēlaties strādāt, lai to atvērtu.

    ![Līdzekļu pārvaldības mobilā darbvieta.](media/mobile-app-asset-workspace.png "Līdzekļu pārvaldības mobilā darbvieta")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Darbs ar Līdzekļu pārvaldības mobilo darbvietu

Papildinformāciju par to, kā strādāt ar **Līdzekļu pārvaldības** mobilo darbvietu, skatiet sadaļā [Līdzekļu pārvaldības mobilās darbvietas izmantošana](asset-management-mobile-workspace.md).

Papildinformāciju par Finance and Operations (Dynamics 365) mobilo programmu skatiet [mobilās programmas sākumlapā](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]