---
title: Kreditoru katalogu importēšana
description: Šajā rakstā ir aprakstīts kreditora kataloga datu importēšanas process.
author: GalynaFedorova
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gfedorova
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 923715893b9f1c4b87d7bbb67e200f8cb8f92e6b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015560"
---
# <a name="import-vendor-catalogs"></a>Kreditoru katalogu importēšana

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Piegādātāju katalogu importēšana

Programmā Dynamics 365 Supply Chain Management iepirkumu speciālisti var izveidot un uzturēt katalogus, ko uzņēmuma darbinieki var izmantot, pasūtot krājumus un pakalpojumus iekšējai lietošanai. Lai izveidotu sagādes katalogu, varat pievienot krājumus un pakalpojumus, kurus vēlaties padarīt pieejamus darbiniekiem, Tas ir izdarāms, vai nu importējot preču kataloga datus, vai manuāli pievienojot preču kataloga datus preces šablonam. 

Kreditora iesniegtos kataloga datus varat augšupielādēt Microsoft Dynamics 365 klientā.

Preces datiem, ko piegādātājs jums iesniedz kataloga uzturēšanas pieprasījuma (Catalog Maintenance Request — CMR) faila formā, ir jābūt XML faila formātā. CMR failā ir jābūt informācijai par precēm, ko šis piegādātājs piegādā jūsu uzņēmumam.

## <a name="import-vendor-catalog-data"></a>Piegādātāja kataloga datu importēšana

Lai importētu piegādātāja kataloga datus, jums ir jāizpilda tālāk minētie uzdevumi.

1. Iestatiet projektu tajā datu pārvaldības darbvietā, kur ir definētas jūsu datu kartēšanas kārtulas. Atlasiet **Datu pārvaldība** un pēc tam atlasiet **Iestatīt lomas datu projektiem**.

2. Iestatiet sagādes kategoriju hierarhiju un savus piegādātājus piešķirt sagādes kategorijām. Ja izmantojat preču kodus, šie preču kodi ir jāpievieno sagādes kategorijām. Informāciju par sagādes kategoriju hierarhijas iestatīšanu skatiet rakstā [Sagādes kategoriju hierarhijas iestatīšana](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3. Konfigurējiet piegādātāju kataloga importēšanai. Atlasiet piegādātāju un pēc tam atlasiet **Sagāde** > **Iestatīt** > **Konfigurēt piegādātāju kataloga importēšanai**.

4. Konfigurējiet darbplūsmu katalogu importēšanai. Izveidojiet CMR faila veidni un kopīgojiet to ar piegādāju.

5. Atlasiet **sagādes un avotu katalogu** \> **piegādātāju** \> **katalogus**, lai izveidotu piegādātāju katalogu. Šajā katalogā tiek grupēti kataloga uzturēšanas pieprasījuma (CMR) faili, ko saņemat no sava piegādātāja.

6. Augšupielādējiet CMR failu.

7. Pārskatiet, apstipriniet vai noraidiet preces šajā piegādātāju katalogā. Preces tiek automātiski kartētas uz sagādes kategorijām. 

Apstiprinātās preces tiek pievienotas preces šablonam un izlaistas atlasītajām juridiskajām personām. Sagādes katalogam var pievienot tikai apstiprinātās preces.

## <a name="generate-a-catalog-import-file-template"></a>Kataloga importēšanas faila veidnes ģenerēšana

Kataloga importēšanas faila veidne ir XSD fails, ko izmanto, lai izveidotu CMR failu piegādātāja precēm. Varat izmantot CMR failu, lai izveidotu jaunu katalogu, aizstātu esošu katalogu vai modificētu esošu katalogu.

1. Atlasiet **Sagāde un avoti** \> **Katalogi** \> **Piegādātāju katalogi** un veiciet dubultklikšķi uz kataloga, ar kuru vēlaties strādāt.

2. Lejupielādējiet pašreizēju kataloga importēšanas veidni (XSD fails). Lapā **Atjaunināt katalogu**, loga **Darbību rūts** cilnē **Katalogi**, grupā **Saistītā informācija** noklikšķiniet uz **Ģenerēt kataloga veidni** un atlasiet **Sagādes kategorija**.

    - Izmantojot opciju **Sagādes kategorija**, varat ģenerēt kataloga veidni, kur ir sagādes kategorijas, kurās piegādātājs ir autorizēts nodrošināt preces.

3. Dialoglodziņā **Saglabāt kā** atlasiet atrašanās vietu, kur vēlaties saglabāt kataloga faila veidni, un saglabājiet failu.

Papildinformāciju un piemērus skatiet šajā emuāra ierakstā: [Piegādātāju katalogi sistēmā Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]