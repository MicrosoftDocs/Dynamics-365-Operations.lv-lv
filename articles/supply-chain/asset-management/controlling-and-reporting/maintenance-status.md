---
title: Uzturēšanas statuss
description: Šajā rakstā skaidrots, kā aprēķināt uzturēšanas statusu Pamatlīdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6999b6db3053eea1147ed3fc8e56bda787e22a65
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891268"
---
# <a name="maintenance-status"></a>Uzturēšanas statuss

[!include [banner](../../includes/banner.md)]

 

Līdzekļu pārvaldībā jūs varat veikt pārskatu aprēķinus konkrētā periodā jauniem, aktīviem un pabeigtiem uzturēšanas pieprasījumiem, darba pasūtījumiem un dīkstāves uzturēšanas dēļ darbībām. Jūs varat arī redzēt pabeigto nosacījuma izvērtējumu skaitu šim pašam periodam. Izmantojiet šo aprēķinu, lai iegūtu pārskatu par ienākošo un pabeigto uzturēšanas pieprasījumu un darba pasūtījumu darba slodzi.

## <a name="make-a-maintenance-status-calculation"></a>Veiciet uzturēšanas stāvokļa aprēķinus

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Uzturēšanas stāvoklis**.

2. Dialoglodziņā **Aprēķināt stāvokli** atlasiet laika diapazonu, kuram vēlaties veikt aprēķinu, laukos **Datums no** un **Datums līdz**.

3. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties uzturēšanas rindas attiecībā uz funkcionālo novietojumu. 

  Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stāvoklis rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. 
  
  Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

4. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

5. Noklikšķiniet uz pogas **Grupēt pēc**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Atlasītās **Grupēt pēc** pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

6. Neaizmirstiet noklikšķināt uz pogas **Atjaunināt**, lai atjauninātu aprēķinus katru reizi, kad veicat izmaiņas, aktivizējot vai deaktivizējot pogas **Grupēt pēc** vai veicot aprēķinu jaunam periodam.

7. Noklikšķiniet uz **Stāvoklis**, ja vēlaties izveidot jaunu uzturēšanas statusa aprēķinu.

>[!NOTE]
>Rezultāti, kas parādās laukā **Uzturēšanas stāvoklis** ietver vienīgi uzturēšanas pieprasījumus un darba pasūtījumus, kuriem ir reāls sākuma datums un laiks. Beigu datuma un laika lauki var būt tukši.

## <a name="example-1"></a>1. piemērs

Zemāk esošajā ekrānuzņēmumā ir aktivizētas pogas **Gads** un **Mēnesis**. Atlasot šīs **Grupēt pēc** opcijas, jūs saņemat vispārīgu ikmēneša pārskatu par darba slodzi un caurlaidspēju attiecībā uz uzturēšanas pieprasījumiem un darba pasūtījumiem. 

![Mēneša darba slodzes piemērs.](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>2. piemērs

Zemāk esošajā ekrānuzņēmumā ir pievienota informācija par funkcionālo novietojumu. Tagad ir iespējams salīdzināt darba slodzi un caurlaidspēju dažādos funkcionālajos novietojumos, kas var reprezentēt ģeogrāfisko novietojumu, ražotnes vai darba zonas. 

![Mēneša darba slodzes piemērs ar funkcionālajiem novietojumiem.](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]