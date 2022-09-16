---
title: Piegādes atlaide
description: Šajā rakstā ir aprakstītas nosūtīšanas atlaides Microsoft Dynamics 365 Commerce iespējas un iestatījumi, kas ir nepieciešami to lietošanai.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: 74cfe5246ad72cbdedd0ed4e3b3394bf7277919e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473855"
---
# <a name="shipping-discount"></a>Piegādes atlaide

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstītas nosūtīšanas atlaides Microsoft Dynamics 365 Commerce iespējas un iestatījumi, kas ir nepieciešami to lietošanai.

Brīva piegāde ar atlaidi ir viens no faktoriem, kas ietekmē debitoru tiešsaistes pirkšanas lēmumus. Lai palielinātu ieņēmumus par vienu darbību, daudzi mazumtirgotāji izmanto bezmaksas nosūtīšanas atvieglojumus, lai motivāciju debitoriem palielinātu savu groza lielumu.

Commerce atbalsta nosūtīšanas atlaides iespēju, kas ļauj mazumtirgotājiem konfigurēt atlaides procentuālo vērtību noteiktas piegādes metodes piegādes maksās, ja kvalificēto krājumu pārdošanas kopsumma darbībā atbilst noteiktiem kritērijiem. Scenārija piemērs, kas izmanto piegādes atlaides iespēju, ir "Tēriņu $50 vai vairāk, lai bez maksas saņemtu piegādi pa nakti."

## <a name="prerequisites"></a>Priekšnosacījumi

Piegādes atlaides iespēju atbalsta Commerce pārdošanas kanāla papildu [automātiskās maksas](/dynamics365/unified-operations/retail/omni-auto-charges) funkcijas. Lai varētu izmantot piegādes atlaižu iespēju, **·** **·** **commerce headquarters lapas Commerce parameters** cilnē Debitoru pasūtījumi ir jāiespējo izmantot papildu automātiskās maksas konfigurāciju. Mazumtirgotāji var izmantot papildu automātisko maksu funkciju, lai iestatītu dažādus maksu veidus, piemēram, apstrādi, instalēšanu un norakstīšanas.

Piegādes atlaide tiek piemērota tikai piegādes maksām. Tāpēc mazumtirgotājam ir jānorāda, kuras maksas ir piegādes maksas. Lai programmā Commerce headquarters norādītu piegādes maksas, pārejiet **\>\>** **·** **uz** sadaļu Kanāla iestatījuma maksu kods un iestatiet opciju Piegādes maksa uz Jā nepieciešamajiem maksājumiem.

![Maksas norādīšana kā piegādes maksa.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Konfigurācija

Piegādes atlaides iespēja ir balstīta uz pakāpēm un atbalsta tikai aprēķina tipu **Procentuālā** atlaide. Lai iestatītu nosūtīšanas atlaidi, programmā Commerce headquarters dodieties uz atlaidi **cenas noteikšanai un atlaidēm Nosūtīšanas \> sliekšņa atlaide.** Pēc tam varat norādīt piegādes veidu, uz kuru attiecas atlaide, definēt vienu vai vairākus summu sliekšņus un iestatīt katras sliekšņa atlaides procentus. Varat arī konfigurēt kategoriju vai preču sarakstu kā kvalificētus krājumus. Šādā veidā tikai pārdošanas summa attiecībā pret šiem krājumiem darbībā tiek skaitīta, kad cenu noteikšanas programma novērtē, vai darbības kopsumma atbilst slieksnim.

> [!NOTE]
> Atšķirībā no citiem atlaižu veidiem piegādes atlaide neveidojiet atlaides rindas. Tā vietā tā tieši rediģē nosūtīšanas maksu un pievieno atlaides nosaukumu maksas aprakstam.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
