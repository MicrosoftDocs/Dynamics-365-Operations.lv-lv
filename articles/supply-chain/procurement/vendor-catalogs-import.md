---
title: Piegādātāju katalogu importēšana
description: Šajā tēmā ir aprakstīts piegādātāju katalogu datu importēšanas process.
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: cf81823de46da9a834f0214896b9e634989cac0e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "362031"
---
# <a name="import-vendor-catalogs"></a>Importēt piegādātāju katalogus
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Piegādātāju katalogu importēšana

Programmā Microsoft Dynamics 365 for Finance and Operations iepirkumu speciālisti var izveidot un uzturēt katalogus, ko uzņēmuma darbinieki var izmantot, pasūtot krājumus un pakalpojumus iekšējai lietošanai. Lai izveidotu sagādes katalogu, varat pievienot krājumus un pakalpojumus, kurus vēlaties padarīt pieejamus darbiniekiem, Tas ir izdarāms, vai nu importējot preču kataloga datus, vai manuāli pievienojot preču kataloga datus preces šablonam. 

Kreditora iesniegtos kataloga datus varat augšupielādēt Microsoft Dynamics 365 klientā.

Preces datiem, ko piegādātājs jums iesniedz kataloga uzturēšanas pieprasījuma (Catalog Maintenance Request — CMR) faila formā, ir jābūt XML faila formātā. CMR failā ir jābūt informācijai par precēm, ko šis piegādātājs piegādā jūsu uzņēmumam.

## <a name="import-vendor-catalog-data"></a>Piegādātāja kataloga datu importēšana

Lai importētu piegādātāja kataloga datus, jums ir jāizpilda tālāk minētie uzdevumi.

1.  Iestatiet projektu tajā datu pārvaldības darbvietā, kur ir definētas jūsu datu kartēšanas kārtulas. Atlasiet **Datu pārvaldība** un pēc tam atlasiet **Iestatīt lomas datu projektiem**. 

2.  Iestatiet sagādes kategoriju hierarhiju un savus piegādātājus piešķirt sagādes kategorijām. Ja izmantojat preču kodus, šie preču kodi ir jāpievieno sagādes kategorijām. Informāciju par sagādes kategoriju hierarhijas iestatīšanu skatiet rakstā [Sagādes kategoriju hierarhijas iestatīšana](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3.  Konfigurējiet piegādātāju kataloga importēšanai. Atlasiet piegādātāju un pēc tam atlasiet **Sagāde** > **Iestatīt** > **Konfigurēt piegādātāju kataloga importēšanai**.

4.  Konfigurējiet darbplūsmu katalogu importēšanai. Izveidojiet CMR faila veidni un kopīgojiet to ar piegādāju.

5.  Lai izveidotu piegādātāja katalogu, atlasiet **Sagāde un avoti** \> **Vispārīgi** \> **Katalogi** \> **Piegādātāju katalogi**. Šajā katalogā tiek grupēti kataloga uzturēšanas pieprasījuma (CMR) faili, ko saņemat no sava piegādātāja. 

6.  Augšupielādējiet CMR failu.

7.  Pārskatiet, apstipriniet vai noraidiet preces šajā piegādātāju katalogā. Preces tiek automātiski kartētas uz sagādes kategorijām programmatūrā Dynamics 365 for Finance and Operations. 
    
Apstiprinātās preces tiek pievienotas preces šablonam un izlaistas atlasītajām juridiskajām personām. Sagādes katalogam var pievienot tikai apstiprinātās preces.

## <a name="generate-a-catalog-import-file-template"></a>Kataloga importēšanas faila veidnes ģenerēšana

Kataloga importēšanas faila veidne ir XSD fails, ko izmanto, lai izveidotu CMR failu piegādātāja precēm. Varat izmantot CMR failu, lai izveidotu jaunu katalogu, aizstātu esošu katalogu vai modificētu esošu katalogu.

1.  Atlasiet **Sagāde un avoti** \> **Katalogi** \> **Piegādātāju katalogi** un veiciet dubultklikšķi uz kataloga, ar kuru vēlaties strādāt.

2.  Lejupielādējiet pašreizēju kataloga importēšanas veidni (XSD fails). Lapā **Atjaunināt katalogu**, loga **Darbību rūts** cilnē **Katalogi**, grupā **Saistītā informācija** noklikšķiniet uz **Ģenerēt kataloga veidni** un atlasiet **Sagādes kategorija**.

    -   Izmantojot opciju **Sagādes kategorija**, varat ģenerēt kataloga veidni, kur ir sagādes kategorijas, kurās piegādātājs ir autorizēts nodrošināt preces.

3. Dialoglodziņā **Saglabāt kā** atlasiet atrašanās vietu, kur vēlaties saglabāt kataloga faila veidni, un saglabājiet failu.

Papildinformāciju un piemērus skatiet šajā emuāra ierakstā: [Piegādātāju katalogi sistēmā Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).
