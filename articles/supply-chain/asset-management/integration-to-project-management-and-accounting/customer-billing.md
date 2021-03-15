---
title: Rēķins par uzturēšanu debitora īpašumā aktīviem
description: Šajā tēmā skaidrots, kā izveidot, apstrādāt un izrakstīt rēķinu uzturēšanas darbu, kas tiek veikts jūsu debitoriem piederošām pamatlīdzekļiem.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131845"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Rēķins par uzturēšanu debitora īpašumā aktīviem

[!include [banner](../../includes/banner.md)]

*Darba pasūtījuma rēķinu izrakstīšanas* funkcija ļauj izveidot, apstrādāt un izrakstīt rēķinu uzturēšanas darbu, kas tiek veikts jūsu debitoriem piederošām pamatlīdzekļiem. Šī funkcija ļauj veikt šādus uzdevumus:

- Saistiet debitorus ar tiem piederošajiem pamatlīdzekļiem.
- Atlasiet debitoru un skatiet līdzekļus, kas debitoram pieder, veidojot darba pasūtījumu.
- Iestatiet pamatprojektu katram debitoram.
- Reģistrējiet darba pasūtījumam stundas, krājumus, izdevumus un komisijas maksas un pēc tam vēlāk izveidojiet debitoram rēķina priekšlikumu.

Turklāt šī funkcija nodrošina sekojošo funkcionalitāti:

- Projekta līgums no debitora pamatprojekta tiek automātiski kopēts uz atbilstošo darba pasūtījuma projektu.
- Tagad līdzekļu vadība var izmantot *maksas* projekta darbības tipu gan darba pasūtījumu prognozēs, gan darba pasūtījumu žurnālos.

## <a name="turn-on-the-customer-billing-feature"></a>Ieslēdziet debitora maksājumu ieskatu līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Projektu pārvaldība un uzskaite*
- **Funkcionalitātes nosaukums:** *Darba pasūtījuma norēķini*

## <a name="example-scenario"></a>Piemērs

Lai uzzinātu, kā šī funkcija darbojas, aplukojiet nākamo situācijas paraugu.

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Pirms sākat, jāatlasa **USMF** juridiskā persona.

Varat arī izmantot šo scenāriju kā norādījumus, lai līdzekli lietotu darbā ar ražošanas sistēmu. Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>1. darbība: jauna projekta līguma izveide debitoram

1. Dodieties uz **Projektu vadība un uzskaite \> Projekti \> Projekta līgumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Jauns projekta līgums** iestatiet sekojošas vērtības:

    - **Nosaukums:** *Pelican vairumtirdzniecība*
    - **Finansējuma tips:** *Debitors*
    - **Finansējuma avots:** *US-013* (*Pelican vairumtirdzniecība*)

1. Atlasiet **Labi**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>2. darbība: jauna projekta līguma izveide debitoram

Šeit izveidotais pamatprojekts tiks izmantots, veidojot debitora darba pasūtījumus.

1. Dodieties uz **Projektu vadība un uzskaite \> Projekti \> Visi projekti**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Jauns produkts** iestatiet sekojošas vērtības:

    - **Projekta veids:** *Laiks un materiāls*
    - **Projekta nosaukums:** *Pelican vairumtirdzniecības darba pasūtījumi*
    - **Projektu grupa:** *TM*
    - **Projekta līguma ID:** *Pelican vairumtirdzniecība* (iepriekš izveidotais līgums)
    - **Sākuma datums:** atlasiet šodienas datumu.

1. Atlasiet **Izveidot projektu**.
1. Jaunais projekts ir atvērts. Pierakstiet **Projekta ID** vērtību. Tā būs jāievada vēlāk.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>3. darbība: jauna darba pasūtījuma tipa izveide Līdzekļu pārvaldībā

1. Atlasiet **Līdzekļu pārvaldība \> Iestatīšana \> Darba pasūtījumi \> Darba pasūtījumu veidi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Sarakstam tiek pievienota jauna rinda. Iestatiet rindai šādas vērtības:

    - **Darba pasūtījuma veids:** *Pakalpojums*
    - **Nosaukums:** *Pakalpojuma darba pasūtījumi*
    - **Darba pasūtījuma dzīves cikla statuss:** *Standarts*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>4. darbība: debitora konta saistīšana ar pamatprojektu

Tagad debitora konts ir jāsaista ar pamatprojektu Līdzekļu pārvaldības projektu iestatījumos.

1. Dodieties uz **Līdzekļu pārvaldība \> Iestatīšana \> Darba pasūtījumi \> Projekta iestatīšana**.
1. Cilnē **Pamatprojekts** atlasiet **Pievienot**, lai pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Debitora konts:** *US-013* (*Pelican vairumtirdzniecība*)
    - **Projekta ID:** Ievadiet projekta ID, kuru iepriekš atzīmējāt.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>5. solis: projektu grupas un tipa saistīšana ar darba pasūtījuma projektu

Jums joprojām jābūt lapā **Projekta iestatījumi** (**Līdzekļu pārvaldība \>Iestatījumi \> Darba pasūtījumi \> Projekta iestatījumi**).

1. Cilnē **Projekta grupa** atlasiet **Pievienot**, lai pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Darba pasūtījuma tips:** *Pakalpojums* (iepriekš izveidotais darba pasūtījuma tips)
    - **Projektu grupa:** *TM*

> [!NOTE]
> Projekta līgums darba pasūtījuma projektā vienmēr ir pārmantots no pamatprojekta.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>6. darbība: līdzekļa saistīšana ar debitora ID

1. Dodieties uz **Līdzekļu pārvaldība \> Līdzekļi \> Aktīvie līdzekļi**.
1. Laukā **Filtrs** ievadiet *VE-102 un* atlasiet, lai filtrētu pēc **Līdzekļiem**.
1. Atlasiet līdzekli, lai atvērtu tā iestatījumus.
1. Kopsavilkuma cilnē **Klients** iestatiet lauku **Klienta konts** uz *US-013* (*Pelican vairumtirdzniecība*).

    Lauks **Nosaukums** tiek automātiski atjaunināts uz *Pelican vairumtirdzniecība*.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>7. darbība: jauna darba pasūtījuma tipa izveide līdzeklim

1. Dodieties uz **Līdzekļu pārvaldība \> Darba pasūtījumi \> Aktīvie darba pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Darba pasūtījuma veids:** *Pakalpojums*
    - **Apraksts:** *Kravas automašīnas remonts*
    - **Debitora konts:** *US-013* (*Pelican vairumtirdzniecība*)
    - **Pamatlīdzeklis:** *VE-102*

        > [!NOTE]
        > Uzmeklēšana parāda tikai līdzekļus, kas ir saistīti ar atlasīto debitora kontu.

    - **Uzturēšanas darba veids:** *Labošana*
    - **Tirdzniecība:** *Mehānika*
    - **Pakalpojumu līmenis:** *4*

1. Atlasiet **Labi**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>8. darbība: darba pasūtījuma pārskatīšana un darba sākšana ar to

Šajā sadaļā jūs strādāsiet pie darba pasūtījuma, ko izveidojāt iepriekšējā sadaļā.

1. Izpildiet šīs darbības, lai pārbaudītu, vai pamatprojekts ir *Pelican vairumtirdzniecības darba pasūtījuma* projekts:

    1. Sadaļā **Darba pasūtījuma uzturēšanas darbi** atlasiet rindu.
    1. Pārbaudiet **Projekta ID** vērtību kopsavilkuma cilnē **Detalizēta informācija par rindu**. Veidlapā jābūt numuram ar defisi *\<Parent-Project-ID\>-\<Project-ID\>*. Šī vērtība ir saite.
    1. Izvēlieties projekta ID saiti, lai atvērtu lapu, kur jūs variet skatīt projektu pamatprojektu un projektu nosaukumus.

1. Darbību rūts cilnē **Darba pasūtījums** grupā **Dzīves cikla statuss** atlasiet **Atjaunināt darba pasūtījuma statusu**.
1. Dialoglodziņa **Atjaunināt darba pasūtījuma stāvokli** kolonnā **Atlasīt** atzīmējiet izvēles rūtiņu rindai, kurā lauks **Dzīves cikla stāvoklis** ir iestatīts uz *Notiek*.
1. Atlasiet **Labi**.
1. Dialoglodziņā **Dzīves cikla stāvoklis: Notiek** atlasiet **Labi**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>9. darbība: darba pasūtījumam veltīto stundu grāmatošana un jauna rēķina priekšlikuma izveide

Šajā sadaļā jūs strādāsiet pie darba pasūtījuma, ko izveidojāt iepriekšējā sadaļā.

1. Darbību rūts cilnē **Darba pasūtījumi**, grupā **Projekti**, atlasiet **Žurnāli**.

    Tiek parādīta lapa **Darba pasūtījumu žurnāli**. Šeit var reģistrēt laiku, kas pavadīts darba pasūtījumā.

1. Kopsavilkuma cilnē **Stundas** atlasiet **Pievienot rindu**.
1. Jaunajā rindā iestatiet laukam **Stundas** vērtību *4*.
1. Darbību rūtī atlasiet **Publicēt žurnālus**.
1. Aizveriet lapu **Darba pasūtījumu žurnāli**, lai atgrieztos darba pasūtījumā.
1. Darbību rūts cilnē **Rēķini** atlasiet **Jauna rēķina piedāvājums**.
1. Dialoglodziņa **Izveidot rēķina priekšlikumu** sadaļā **Projekta darbības** atzīmējiet **Izvēles** rūtiņu katrai rindai, ko vēlaties iekļaut rēķinā.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu un skatītu jaunu rēķina piedāvājumu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]