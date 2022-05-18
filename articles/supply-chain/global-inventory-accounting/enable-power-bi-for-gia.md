---
title: Iespējot Power BI Globālajai krājumu uzskaitei
description: Šajā tēmā ir aprakstīts, kā iespējot Microsoft Power BI Globālajai krājumu uzskaiti.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8be486409d60cc4927599816e30e1e4ab21a312a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669787"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Iespējot Power BI Globālajai krājumu uzskaitei

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

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
    1. Sadaļā **Globālās krājumu uzskaites iestatījumi** izvērsiet **Parametri** un pēc vajadzības atjauniniet visus parametrus. It īpaši pārbaudiet šādus iestatījumus:
        1. Pārrakstiet noklusējuma **Dataverse URL vērtības**, izmantojot vērtības, kas **atrodamas Power platform vides** informācijā LCS (**Power platform integrācijas sadaļā**).
        1. Pārrakstiet noklusējuma **vides ID vērtības**, izmantojot vērtības, kas atrastas **vides** papildinformācijā par LCS (sadaļā **Pārvaldīt** vidi).
        1. Atlasiet saiti **Rediģēt akreditācijas** datus blakus **CDS etiķetei** datu avota akreditācijas **datu** sadaļā. Tad piesakieties savā Dataverse kontā, izmantojot **OAuth2** autentifikācijas metodi.
    1. Pārbaudiet, vai Power BI atskaites, kas atrodamas **Mana darbvieta \> Atskaites \> Globālā krājumu uzskaite**, tagad darbojas pareizi un parāda sistēmas saturu.

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
