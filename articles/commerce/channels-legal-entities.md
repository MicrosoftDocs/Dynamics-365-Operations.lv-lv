---
title: Izveidot juridiskās personas
description: Šajā tēmā aprakstīts, kā izveidot juridisku personu risinājumā Microsoft Dynamics 365 Commerce, kas jāizveido un jākonfigurē pirms kanālu izveides.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800619"
---
# <a name="create-legal-entities"></a>Izveidot juridiskās personas

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot juridisku personu risinājumā Microsoft Dynamics 365 Commerce, kas jāizveido un jākonfigurē pirms kanālu izveides.

Juridiskā persona ir organizācija, kurai ir reģistrēta vai likumā noteikta juridiskā struktūra. Juridiskas personas var noslēgt juridiskos līgumus, un tām ir nepieciešams sagatavot pārskatus, lai ziņotu par savu veiktspēju.

Uzņēmums ir juridiskas personas veids. Pašlaik uzņēmums ir vienīgais juridiskas personas veids, ko varat izveidot, un katra juridiska persona ir saistīta ar uzņēmuma ID. Šī saistība pastāv, jo daži programmas funkcionālie apgabali izmanto uzņēmuma ID vai *DataAreaId* savos datu modeļos. Šajos funkcionālos apgabalos uzņēmumi tiek izmantoti kā datu drošības robeža. Lietotāji var piekļūt tikai tā uzņēmuma datiem, kurš ir pašlaik pieteicies sistēmā. 

Veidojot kanālu, jānorāda, kurai juridiskajai personai pieder kanāls.

## <a name="create-a-new-legal-entity"></a>Izveidot jaunu juridisko personu

Lai izveidotu jaunu juridisko personu programmā Dynamics 365 Commerce, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz  **Moduļi \> Headquarters iestatīšana \> Juridiskās personas**.
1. Darbību rūtī atlasiet **Jauns**. Labajā pusē tiek parādīta rūts **Jaunā juridiskā persona**.
1. Laukā **Nosaukums** ievadiet vērtību.
1. Laukā **Uzņēmums** ievadiet vērtību.
1. Laukā **Valsts/reģions** ievadiet vai atlasiet kādu vērtību.
1. Atlasiet **Labi**. 

   ![Juridiskās personas izveide](media/legal-entities.png)

1. Sadaļā **Vispārīgi** sniedziet šādu vispārīgo informāciju par juridisko personu: 
   1. Ievadiet meklēšanas nosaukumu, ja ir nepieciešams meklēšanas nosaukums. Meklēšanas nosaukums ir alternatīvs nosaukums, ko var lietot šīs juridiskās personas meklēšanai. 
   1. Atlasiet, vai šī juridiskā persona tiek izmantota kā konsolidēšanas uzņēmums.
   1. Atlasiet, vai šī juridiskā persona tiek izmantota kā korekcijas uzņēmums. 
   1. Atlasiet elementam **noklusējuma valodu**. 
   1. Izvēlieties **laika joslu** elementam.
1. Sadaļā **Adreses** atlasiet **Rediģēt**, lai ierakstītu informāciju par adresi, piemēram, ielas nosaukumu un numuru, pasta indeksu un pilsētu.
1. Sadaļā **Kontaktinformācija** ievadiet informāciju par komunikācijas veidiem, piemēram, e-pasta adreses, URL un tālruņa numurus.
1. Sadaļā **Likumā noteiktie pārskati** ievadiet reģistrācijas numurus, kas tiek lietoti ar likumu noteikto atskaišu veidošanai.
1. Sadaļā **Reģistrācijas numuri** ievadiet juridiskās personas prasīto informāciju.
1. Sadaļā **Bankas konta informācija** ievadiet juridiskās personas bankas kontus un reģistrācijas numurus.
1. Sadaļā **Ārējā tirdzniecība un loģistika** ievadiet juridiskās personas piegādes informāciju.
1. Sadaļā **Numuru sērijas** varat apskatīt numuru sērijas, kas ir saistītas ar šo juridisku personu. Lai sāktu, šis lauks būs tukšs.
1. Sadaļā **Informācijas paneļa attēls** skatiet vai mainiet logotipu un informācijas paneļa attēlu, kas ir saistīti ar juridisko personu.
1. Sadaļā **Nodokļa reģistrācija** ievadiet reģistrācijas numurus, kas tiek izmantoti, atskaitoties nodokļu iestādēm.
1. Sadaļā **Nodoklis 1099** ievadiet 1099 informāciju par juridisko iestādi.
1. Sadaļā **Nodokļu informācija** ievadiet nodokļu informāciju par juridisko iestādi.
1. Atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīts juridiskas personas informācijas piemērs.

![Juridiskās personas vispārīgā sadaļa](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Papildu resursi

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organizācijas hierarhijas plānošana](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organizācijas hierarhijas](channels-org-hierarchies.md)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
