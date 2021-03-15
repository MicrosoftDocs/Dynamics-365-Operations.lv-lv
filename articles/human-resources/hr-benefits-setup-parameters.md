---
title: Iestatīt Atvieglojumu pārvaldību un Darbinieku pašapkalpošanās parametrus visiem uzņēmumiem
description: Konfigurēt Atvieglojumu pārvaldības parametrus un Darbinieku pašapkalpošanos programmā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "4962444"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Iestatīt Atvieglojumu pārvaldību un Darbinieku pašapkalpošanās parametrus visiem uzņēmumiem

Pirms varat iestatīt atvieglojumu plānus risinājumā Microsoft Dynamics 365 Human Resources, ir jākonfigurē atvieglojumu pārvaldības parametri. Šie parametri iestata noklusējuma vērtības, pamatojuma kodus un citas opcijas. 

## <a name="configure-general-parameters"></a>Vispārējo parametru konfigurēšana

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Personāla vadības kopīgie parametri**.

2. Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:

   | Lauks | Apraksts |
   | --- | --- |
   | **Valsts/reģions** | Lauks **Valsts/reģions** nosaka pasta kodu/štatu rādīšanas secību. Nolaižamajā sarakstā pirmā tiek parādīta atlasītā valsts. |
   | **Reģistrācijas iemesla kods** | Atlasiet noklusēto pamatojuma kodu, ko izmantot, kad tiek izveidoti nodarbināto plāni atvērtās reģistrācijas apstrādes laikā. |
   | **Atcelšanas iemesla kods** | Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atcelšanas laikā. Atcelšanas laikā tas rāda dialoglodziņu. Ja nepieciešams, lietotāji var mainīt **Atcelšanas pamatojuma kodu**. |
   | **Atkārtotas atvēršanas iemesla kods** | Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atkārtotas atvēršanas laikā. Atcelšanas laikā tas rāda dialoglodziņu. Ja nepieciešams, lietotāji var mainīt **Atkārtotas atvēršanas pamatojuma kodu**. | 
   | **Dzīves notikuma iemesla kods** | Pamatojuma kods, ko izmantot, kad notiek dzīves notikums. |
   | **Likmju maiņas iemesla kods** | Pamatojuma kods, ko izmantot, atceļot un atkārtoti atverot nodarbinātā atvieglojumu plānu likmes izmaiņu atjaunināšanas procesa laikā. Tas norāda, kuri ieraksti tika mainīti pēc likmes izmaiņu atjaunināšanas procesa. |
   | **Atvieglojumu gada alga** | Ļauj iestatīt **Atvieglojumu gada alga** summu darbiniekam. Human Resources izmanto **Atvieglojumi gada algai** summu, nosakot vajadzību summas, nevis fiksētās atlīdzības gada summu. |
   | **Piemērots jaunai pieņemšanai darbā** | Norāda vai ir iespējams veikt jaunu pieņemšanu darbā. |
   | **Jauns pieņemšanas darbā reģistrācijas periods** | Laika periods, kurā atļauta jauna pieņemšanas darbā reģistrācija.</br></br>**Piezīme**: Šis iestatījums labo jebkuru jaunas darbā pieņemšanas reģistrācijas periodu, kuru iestatāt plāna piemērojamības kārtulai. |
   | **Noklusējuma maksājumu biežums** | Noklusējuma maksājumu biežums, kas jāizmanto, pievienojot jaunus darbiniekus. |
   | **Dzīves notikumi iespējoti** | Iespējo dzīves notikumus. |
   | **Paslēpt mantoto atvieglojumu veidlapas** | Ļauj slēpt mantotās atvieglojumu veidlapas. |
   | **Atvieglojuma pārbaude** | Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā. |
   | **Automātiski atlasīt saņēmējus** | Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām. |

3. Atlasiet **Saglabāt**.

## <a name="configure-employee-self-service-parameters"></a>Konfigurēt nodarbinātā patstāvīgi izmantojamo pakalpojumu parametrus

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.

2. Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:

   | Lauks | Apraksts |
   | --- | --- |
   | **Atvieglojuma pārbaude** | Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā. |
   | **Automātiski atlasīt saņēmējus** | Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām. |

3. Atlasiet **Saglabāt**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]