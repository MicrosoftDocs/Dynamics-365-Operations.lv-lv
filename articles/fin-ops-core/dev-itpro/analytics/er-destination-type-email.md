---
title: E-pasta ziņojuma ER adresāta tips
description: Šajā tēmā ir sniegta informācija par to, kā konfigurēt e-pasta ziņojuma adresātu katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745565"
---
# <a name="email-destination"></a>E-pasta galamērķis

[!include [banner](../includes/banner.md)]

Varat konfigurēt e-pasta ziņojuma adresātu katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai. Pamatojoties uz adresāta iestatījumu, ģenerētais dokuments tiek piegādāts kā elektroniskā pasta pielikums.

Opciju **Iespējots** iestatiet uz **Jā**, lai izvades failu sūtītu pa e-pastu. Kad šī opcija ir iespējota, varat norādīt e-pasta ziņojumu adresātus, kā arī rediģēt tēmu un e-pasta ziņojuma pamattekstu. E-pasta ziņojuma tēmai un pamattekstam varat iestatīt konstantus tekstus, vai arī varat lietot ER- [formulas](er-formula-language.md), lai e-pasta tekstus izveidotu dinamiski. 

E-pasta adreses lietošanai ar ER varat konfigurēt divos veidos. Konfigurāciju var pabeigt tādā pašā veidā, kā to pabeidz drukāšanas pārvaldības līdzeklis, vai arī varat atrisināt e-pasta adresi, izmantojot tiešu atsauci uz ER konfigurāciju ar formulas palīdzību.

[![E-pasta ziņojuma galamērķa iespējošana](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>E-pasta adrešu tipi

Kad atlasāt **Rediģēt** laukos **Kam** vai **Kopija**, tiek parādīts dialoglodziņš **E-pasta ziņojuma adresāts**. Pēc tam varat atlasīt izmantojamo e-pasta adreses tipu. Pašlaik tiek atbalstīti e-pasta tipi **Konfigurācijas e-pasts** un **Drukāšanas pārvaldība**.

[![E-pasta ziņojuma tipa atlasīšana](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Drukāšanas iestatījumi

Ja atlasāt e-pasta ziņojuma tipu **Drukāšanas pārvaldība**, varat laukā **Kam** ievadīt fiksētas e-pasta adreses. 

[![Fiksēto e-pasta adresu konfigurēšana](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Lai lietotu e-pasta adreses, kas nav fiksētas, jums faila galamērķim ir jāatlasa e-pasta avota tips. Tiek atbalstītas šādas vērtības: **Debitors**, **Kreditors**, **Potenciālais klients**, **Kontaktpersona**, **Konkurents**, **Nodarbinātais**, **Kandidāts**, **Potenciālais piegādātājs** un **Neatļauts piegādātājs**. Kad e-pasta avota tips ir atlasīts, izmantojiet pogu blakus laukam **E-pasta ziņojuma avota konts**, lai atvērtu formu **Formulas veidotājs**. Varat izmantot šo formu, lai pievienotu formulu, kas atgriežas izpildlaikā, atlasītā avota tipa **puses kontu** no apstrādātā dokumenta līdz e-pasta ziņojuma adresātam.

[![E-pasta ziņojuma avota konta konfigurācija](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Formulas ir atkarīgas no ER konfigurācijas. Laukā **Formula** ievadiet dokumentam specifisko atsauci uz debitora vai kreditora puses tipu. Tā vietā, lai rakstītu, varat atrast datu avota mezglu, kas apzīmē debitora vai kreditora kontu, un pēc tam atlasīt **Pievienot datu avotu**, lai atjauninātu šo formulu. Piemēram, ja izmantojat konfigurāciju **ISO 20022 kredīta pārskaitījums**, tad kreditora kontu apzīmē mezgls `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Ja ievadāt virknes vērtību, piemēram `"DE-001"`, un saglabājat formulu, e-pasta ziņojums tiks nosūtīts kreditora kontaktpersonai **DE-001**.


[![ER formulas veidotāja lapa](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![E-pasta ziņojuma avota atribūtu konta konfigurācija](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Konfigurācijas e-pasta ziņojums

Izmantojiet šo e-pasta ziņojuma tipu, ja izmantotajā konfigurācijā ir datu avotu mezgls, kas atgriež **e-pasta adresi**. Formulu veidotājā varat izmantot datu avotus un funkcijas, lai iegūtu pareizi formatētu e-pasta adresi. Piemēram, ja izmantojat konfigurāciju **ISO 20022 kredīta pārskaitījums**, tad kreditora kontaktpersonas e-pasta adresi apzīmē mezgls `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![E-pasta adreses avota konfigurācija](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)
- [Formulas veidotājs elektronisko pārskatu veidošanā (ER)](general-electronic-reporting-formula-designer.md)
