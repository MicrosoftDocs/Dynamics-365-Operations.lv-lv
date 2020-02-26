---
title: Iestatīt atvieglojumu pārvaldības parametrus
description: Konfigurējiet parametrus atvieglojumu pārvaldībai risinājumā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009815"
---
# <a name="set-benefits-management-parameters"></a>Iestatīt atvieglojumu pārvaldības parametrus

[!include [banner](includes/preview-feature.md)]

Pirms varat iestatīt atvaļinājumu plānus risinājumā Microsoft Dynamics 365 Human Resources, ir jākonfigurē atvieglojumu pārvaldības parametri. Šie parametri iestata noklusējuma vērtības, pamatojuma kodus un citas opcijas.

## <a name="configure-general-parameters"></a>Vispārējo parametru konfigurēšana

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Parametri**.

2. Cilnē **Vispārīgi** norādiet vērtības šiem laukiem:

   | Lauks | Apraksts |
   | --- | --- |
   | **Valsts/reģions** | Lauks **Valsts/reģions** nosaka pasta kodu/štatu rādīšanas secību. Nolaižamajā sarakstā pirmā tiek parādīta atlasītā valsts. |
   | **Reģistrācijas iemesla kods** | Atlasiet noklusēto pamatojuma kodu, ko izmantot, kad tiek izveidoti nodarbināto plāni atvērtās reģistrācijas apstrādes laikā. |
   | **Atcelšanas iemesla kods** | Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atcelšanas laikā. Atcelšanas laikā tas rāda dialoglodziņu. Ja nepieciešams, lietotāji var mainīt **Atcelšanas pamatojuma kodu**. |
   | **Atkārtotas atvēršanas iemesla kods** | Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atkārtotas atvēršanas laikā. Atcelšanas laikā tas rāda dialoglodziņu. Ja nepieciešams, lietotāji var mainīt **Atkārtotas atvēršanas pamatojuma kodu**. | 
   | **Dzīves notikuma iemesla kods** | Pamatojuma kods, ko izmantot, kad notiek dzīves notikums. |
   | **Likmju maiņas iemesla kods** | Pamatojuma kods, ko izmantot, atceļot un atkārtoti atverot nodarbinātā atvieglojumu plānu likmes izmaiņu atjaunināšanas procesa laikā. Tas norāda, kuri ieraksti tika mainīti pēc likmes izmaiņu atjaunināšanas procesa. |
   | **Piemērots jaunai pieņemšanai darbā** | Norāda vai ir iespējams veikt jaunu pieņemšanu darbā. |
   | **Jauns pieņemšanas darbā reģistrācijas periods** | Laika periods, kurā atļauta jauna pieņemšanas darbā reģistrācija.</br></br>**Piezīme**: Šis iestatījums labo jebkuru jaunas darbā pieņemšanas reģistrācijas periodu, kuru iestatāt plāna piemērojamības kārtulai. | 
   | **Gada algas uzlabojums** | Norāda, vai automātiski aprēķināt **Gada atvieglojumu algas** summu **Nodarbinātības atvieglojumu informācijā**. Tas ir balstīts uz nodarbinātā **Fiksētās atlīdzības algas likmi**,**Vidējo laiku** un **Maksājuma biežumu**.</br></br>**Vidējais laiks** x **Fiksētās algas likme** x **Maksājuma biežums** (# no apmaksas periodiem) = **Gada atvieglojumu alga** </br></br>Ja kāda no vērtībām laukos **Vidējais laiks**, **Fiksētās atlīdzības izmaksas likme** vai **Maksājumu biežums** lauki mainās, sistēma automātiski pārrēķinās nodarbinātā **Gada atvieglojumu algas** summu, pamatojoties uz mainītajām vērtībām. Sistēma izveido ierakstu **Spēkā stāšanās datums**, lai noteiktu precīzu datumu un laiku, kad izmaiņas notikušas. Ja nepieciešams, varat manuāli rediģēt **Gada atvieglojumu algas** summu. |
   | **Dzīves notikumi iespējoti** | Iespējo dzīves notikumus. |
   | **Paslēpt mantoto atvieglojumu veidlapas** | Ļauj slēpt mantotās atvieglojumu veidlapas. |

3. Atlasiet **Saglabāt**.

## <a name="configure-employee-self-service-parameters"></a>Konfigurēt nodarbinātā patstāvīgi izmantojamo pakalpojumu parametrus

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Parametri**.

2. Cilnē **Nodarbinātā patstāvīgi izmantojamie pakalpojumi** norādiet vērtības šiem laukiem:

   | Lauks | Apraksts |
   | --- | --- |
   | **Atvieglojuma pārbaude** | Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā. |
   | **Automātiski atlasīt saņēmējus** | Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām. |

3. Atlasiet **Saglabāt**.
