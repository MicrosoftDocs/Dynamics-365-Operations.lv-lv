---
title: Zvanu centra pasūtījumu izveide
description: Šajā rakstā ir apskatīta piemēra procedūra, kurā zvanu centra lietotājs meklē debitoru, izveido jaunu pasūtījumu, meklē preci un iekasē maksājumu no debitora Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228515"
---
# <a name="create-call-center-orders"></a>Zvanu centra pasūtījumu izveide

[!include [banner](../includes/banner.md)]

Šajā rakstā ir apskatīta piemēra procedūra, kurā zvanu centra lietotājs meklē debitoru, izveido jaunu pasūtījumu, meklē preci un iekasē maksājumu no debitora Microsoft Dynamics 365 Commerce. Procedūra izmanto USRT demonstrācijas datu uzņēmumu un ir paredzēta pārdošanas pasūtījumu darbiniekiem. 

## <a name="prerequisites"></a>Priekšnosacījumi

Lietotājam, kas veic procedūru, jābūt iestatītam kā zvanu centra lietotājam. Pēc izvēles Fabrikam pusgada katalogu var publicēt ar vismaz vienu avota kodu.

### <a name="add-yourself-as-a-call-center-user"></a>Pievienot sevi kā zvanu centra lietotāju

Lai pievienotu sevi kā zvanu centra lietotāju, veiciet šādas darbības.

1. Programmā Commerce headquarters dodieties uz sadaļu **Mazumtirdzniecības un Commerce \> kanāli \> zvanu centri \>**.
1. Laukā **Lietotāji** atlasiet Kanāla **lietotāji**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Lietotāja ID** ievadiet savu lietotāja ID.
1. Laukā **Nosaukums** ievadiet savu lietotāja vārdu. Lietotājvārds var būt tāds pats kā lietotāja ID.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Atgriezieties mazumtirdzniecības **un Commerce \> kanālu \> zvanu centros \>**.
1. Atlasiet zvanu centra mazumtirdzniecības kanāla ID.
1. Apstipriniet, ka **opcija Iespējot pasūtījuma pabeigšanu** ir iestatīta uz **Jā**. Ja opcija nav redzama, varat izlaist šo darbību.

## <a name="complete-the-example-call-center-procedure"></a>Izpildīt zvanu centra piemēra procedūru

Lai pabeigtu zvanu centra piemēra procedūru, sekojiet šiem soļiem.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Debitori \> Debitoru apkalpošana**.
1. Cilnē Debitora **meklēšana** ievadiet meklēšanas kritērijus, lai meklētu debitoru. Šajā piemērā procedūru ievadiet **Karena**.
1. Atlasiet **Meklēt**. Parādās **debitora meklēšanas** dialoglodziņš, kurā uzskaitīti meklēšanas rezultāti.
1. Atlasiet debitora ierakstu Karenai **Karenai**, kam ir debitora konta numurs **2001**, un pēc tam atlasiet **Atlasīt**.
1. Darbību rūtī atlasiet Jauns **pārdošanas pasūtījums**.
1. Labajā pusē atlasiet cilni **Virsraksts**.
1. Kopsavilkuma cilnes **Piegāde** laukā Piegādes **veids atlasiet** **99 Standarts**.

    ![Piegādes veida atlase.](../media/Select_Mode_of_Delivery.png)

1. Labajā pusē atlasiet cilni **Rindas**.
1. **Sadaļas Pārdošanas pasūtījuma** rindas jaunā rindas jaunajai pārdošanas rindai **laukā Krājuma** kods ievadiet meklējamā krājuma kodu. Šai piemēra procedūrai ievadiet **81327** un pēc tam atlasiet preci nolaižamajā sarakstā, lai pievienotu to pārdošanas pasūtījumam.
1. Laukā **Daudzums** ievadiet pārdošanas daudzumu.
1. **Laukā Avota** kods atlasiet kataloga avota kodu. Ja nav aktīvu avota kodu, varat izlaist šo darbību.
1. Darbību rūtī atlasiet Pabeigts, lai **tvertu** debitora maksājumu. Šī darbība atver pārdošanas **pasūtījuma kopsavilkuma** dialoglodziņu, kurā redzama apmaksas kopsumma. Darbība arī izraisa visu maksu aprēķinus, piemēram, nosūtīšanu un apstrādi, un parāda tās **Pārdošanas pasūtījuma kopsavilkuma** dialoglodziņā.

    ![Poga Pabeigts.](../media/Complete_button.png)

1. Lai tvertu **maksājumus**, **pārdošanas** pasūtījuma kopsavilkuma dialoglodziņā kopsavilkuma **cilnē** Maksājumi atlasiet Pievienot.

    ![Pārdošanas pasūtījumu kopsavilkuma dialoglodziņš.](../media/order_summary.png)

1. **Dialoglodziņa Debitora maksājuma informācijas** ievadīšana laukā **Maksājuma metode** atlasiet maksājuma metodi. Šajā piemērā izvēlieties Skaidra **nauda**.
1. Laukā **Maksājuma** summa ievadiet maksājuma summu. Šajā piemērā ievadiet **120,00**, **kas ir vienāds ar pasūtījuma bilanci, kas ir parādīta pārdošanas pasūtījuma kopsavilkuma** dialoglodziņā. Ievadot šo summu, varat pabeigt pasūtījumu kā pilnībā apmaksātu.
1. Atlasiet **Labi**.
1. Atlasiet **Iesniegt**.

## <a name="additional-resources"></a>Papildu resursi

[Darījumu e-pasta ziņojumu pielāgošana pēc piegādes veida](../customize-email-delivery-mode.md)

[Piegādes veida mainīšana programmā POS](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
