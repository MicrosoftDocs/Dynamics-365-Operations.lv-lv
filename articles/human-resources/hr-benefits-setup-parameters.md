---
title: Iestatīt atvieglojumu pārvaldības parametrus
description: Konfigurējiet parametrus atvieglojumu pārvaldībai risinājumā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429992"
---
# <a name="set-benefits-management-parameters"></a>Iestatīt priekšrocību pārvaldības parametrus

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
