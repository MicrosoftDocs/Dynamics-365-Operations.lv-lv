---
title: Uzturēšanas statuss
description: Šajā tēmā ir paskaidrots, kā aprēķināt uzturēšanas stāvokli programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918353"
---
# <a name="maintenance-status"></a>Uzturēšanas statuss

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Programmā Asset Management jūs varat veikt aprēķinus, lai iegūtu pārskatu par jauniem, aktīviem un pabeigtiem uzturēšanas pieprasījumiem, darba pasūtījumiem un dīkstāves uzturēšanas dēļ darbībām konkrētā periodā. Jūs varat arī redzēt pabeigto nosacījuma izvērtējumu skaitu šim pašam periodam. Izmantojiet šo aprēķinu, lai iegūtu pārskatu par darba slodzi attiecībā uz ienākošiem un pabeigtiem uzturēšanas pieprasījumiem un darba pasūtījumiem.

## <a name="make-a-maintenance-status-calculation"></a>Veiciet uzturēšanas stāvokļa aprēķinus

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Uzturēšanas stāvoklis**.

2. Dialoglodziņā **Aprēķināt stāvokli** atlasiet periodu, kuram vēlaties veikt aprēķinu, laukos **Datums no** un **Datums līdz**.

3. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties uzturēšanas rindas attiecībā uz funkcionālo novietojumu. Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stāvoklis rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

4. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

5. Darbības rūšu grupās **Grupēt pēc...** klikšķiniet uz attiecīgās pogas, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Atlasītās darbības rūts pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

6. Neaizmirstiet noklikšķināt uz pogas **Atjaunināt**, lai atjauninātu aprēķinus katru reizi, kad veicat izmaiņas, aktivizējot vai deaktivizējot pogas **Grupēt pēc...** vai veicot aprēķinu jaunam periodam.

7. Noklikšķiniet uz **Stāvoklis**, ja vēlaties izveidot jaunu uzturēšanas statusa aprēķinu.

>[!NOTE]
>Rezultāti, kas parādās laukā **Uzturēšanas stāvoklis** ietver vienīgi uzturēšanas pieprasījumus un darba pasūtījumus, kuriem ir reāls sākuma datums un laiks. Beigu datuma un laika lauki var būt tukši.

*1. piemērs:*

Zemāk esošajā attēlā ir aktivizētas pogas **Gads** un **Mēnesis**. Šeit ir vispārīgs ikmēneša pārskats par darba slodzi un caurlaidspēju attiecībā uz uzturēšanas pieprasījumiem un darba pasūtījumiem. 

![1. attēls](media/13-controlling-and-reporting.png)

*2. piemērs:*

Zemāk esošajā attēlā ir pievienota informācija par funkcionālo novietojumu. Tagad ir iespējams salīdzināt darba slodzi un caurlaidspēju visos funkcionālajos novietojumos, kas var reprezentēt ģeogrāfisko novietojumu, ražotnes vai darba zonas. 

![2. attēls](media/14-controlling-and-reporting.png)

