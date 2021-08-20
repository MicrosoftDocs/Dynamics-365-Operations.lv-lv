---
title: Iespējot Power BI Globālajai krājumu uzskaitei
description: Šajā tēmā ir aprakstīts, kā iespējot Microsoft Power BI Globālajai krājumu uzskaiti.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 562b56a85ad2f40cb673f8f2101bf92c39853d1f1a087d0498b6f7d19d1cca01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773349"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Iespējot Power BI Globālajai krājumu uzskaitei

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Varat piespraust jūsu uzņēmuma [PowerBI.com](https://powerbi.com/) informācijas paneļus un pārskatus savai Microsoft Dynamics 365 lietojumprogrammas darbvietai.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms Power BI pārskatu iespējošanas jābūt šādiem priekšnosacījumiem:

- Jums ir jābūt sistēmas administratoram Dynamics 365 programmā.
- Jums jābūt [PowerBI.com](https://powerbi.com/) kontam.
- Jūsu Power BI kontā ir jābūt vismaz vienam informācijas panelim un vienam pārskatam.
- Jums jābūt sava Azure Active Directory (Azure AD) konta administratoram.
- Domēnam Azure AD jābūt tam pašam domēnam, ko izmantojāt savam [PowerBI.com](https://powerbi.com/) kontam.

## <a name="setup"></a>Iestatīt

Lai iestatītu Power BI integrāciju, veiciet tālāk norādītās darbības.

1. Pierakstieties portālā [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Dodieties uz **Koplietojamo līdzekļu bibliotēku**, atlasiet **Power BI pārskata modeli** kā līdzekļu tipu un lejupielādējiet pakotni **Globālā krājumu uzskaite**. 
1. Piesakieties [PowerBI.com](https://app.powerbi.com/) un augšupielādējiet **Globālās krājumu uzskaites** Power BI pārskata failu, veicot šādas darbības:

    1. Atlasiet **Jauns**.
    1. Atlasiet **Augšupielādēt failu**.
    1. Atlasiet **Globālās krājumu uzskaites** Power BI pārskata failu.

1. Konfigurējiet **Globālās krājumu uzskaites** Power BI pārskatu, izpildot šādas darbības:

    1. Dodieties uz **Manu darbvietu**, atrodiet Globālās krājumu uzskaites datu kopu un pēc tam izvēlnē **Opcijas** atlasiet **Iestatījumi**.
    1. Sadaļā **Globālās krājumu uzskaites iestatījumi** izvērsiet **Parametri** un pēc vajadzības atjauniniet visus parametrus.

1. Reģistrējiet programmu atbilstoši aprakstam sadaļā [Konfigurēt PowerBI.com integrāciju](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Integrējiet **Globālās krājumu uzskaites** Power BI pārskata failu programmā Dynamics 365 Supply Chain Management, izpildot šādas darbības:

    1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> PowerBI.com konfigurācija**.
    1. Atlasiet **Rediģēt**.
    1. Atlasiet **Aktivizēt PowerBI.Com integrāciju**.
    1. Laukā **Programmas ID** ievadiet pieteikuma ID.
    1. Laukā **Pieteikuma atslēga** ievadiet pieteikuma atslēgu.
    1. Atlasiet **Saglabāt**.

1. Atsvaidziniet lapu, lai parādās Power BI pierakstīšanās dialoglodziņš.
1. Cilnē **Opcijas** atlasiet **Atvērt pārskatu katalogu** un pēc tam atlasiet agrāk augšupielādēto **Globālās krājuma uzskaites** Power BI pārskata failu.
1. Atsvaidziniet lapu. Jums vajadzētu redzēt, ka jūsu pārskats ir pievienots.
1. Sadaļā **Power BI pārskati** atlasiet saiti **Globālā krājumu uzskaite**.

Papildinformāciju skatiet tēmā [PowerBI.com integrācijas konfigurēšana](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
