---
title: Konfigurēt uzņēmuma informāciju programmā Attract
description: Šajā tēmā ir paskaidrots, kā konfigurēt uzņēmuma informāciju un zīmolu Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: db3ec965f3a52810d5f310697b9ed830c3abe681
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461933"
---
# <a name="configure-company-information-in-attract"></a>Konfigurēt uzņēmuma informāciju programmā Attract

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract administrēšanas centrā ir ietverti lietojumprogrammas Attract konfigurēšanas iestatījumi, integrēšanas opcijas un iestatīšanas opcijas.

## <a name="company-information"></a>Uzņēmuma informācija

Ievadiet uzņēmuma parādāmo nosaukumu un pievienojiet uzņēmuma logotipu. Pēc tam parādāmo nosaukumu un logotipu var izmantot darba sludinājumos un pievienošanās procesa laikā.

## <a name="linkedin-integration"></a>LinkedIn integrācija

Iestatiet integrāciju ar LinkedIn Recruiter System Connect (RSC). Kad esat izveidojis savienojumi ar LinkedIn, izmantojot savus LinkedIn akreditācijas datus, varat sinhronizēt kandidāta LinkedIn profilu, pieteikumus, interviju atsauksmes un darbā pieņemšanas grupas piezīmes. Ir nepieciešama pilna LinkedIn Recruiter licence. Papildinformāciju par LinkedIn Recruiter skatiet tēmā [Recruiter System Connect (RSC) — bieži uzdotie jautājumi](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Lietotāju atļaujas

Piešķiriet lomas lietotājiem savā organizācijā. Ir pieejamas šādas lomas: **Administrators**, **Personāla atlases darbinieks**, **Par pieņemšanu darbā atbildīgais vadītājs** un **Tikai lasāms**. Papildinformāciju par lietotāju atļaujām skatiet tēmā [Drošība un lomu pārvaldība programmā Attract](./security-attract.md).

## <a name="feature-management"></a>Līdzekļu pārvaldība

Kad tiek pievienoti jauni līdzekļi, tie var tikt izlaisti publiskā priekšskatījuma režīmā. Publiskā priekšskatījuma līdzekļi neatbilst visām pakalpojuma prasībām. Saņemot tos, jūs piekrītat kopīgot savus datus ar ārējām sistēmām. Iespējams, ka jūsu organizācijai nav nepieciešami visi izlaistie jaunie līdzekļi. Varat izslēgt un ieslēgt publiskā priekšskatījuma līdzekļus atkarībā no savas organizācijas vajadzībām.

## <a name="template-management"></a>Veidņu pārvaldība

Procesa veidnē ir ietvertas visas aktivitātes, kas ir jāietver noteiktas vakances darbā pieņemšanas procesā. Organizācija var atļaut izveidot darbā pieņemšanas procesa veidnes visiem darba grupas dalībniekiem vai tikai administratoriem. Lai atļautu darba grupas dalībniekiem izveidot savas darbā pieņemšanas procesa veidnes, ieslēdziet veidņu pārvaldības funkciju. Papildinformāciju par procesa veidnēm skatiet tēmā [Procesa veidnes izveide programmā Attract](./process-templates-attract.md).

## <a name="email-template-settings"></a>E-pasta veidņu iestatījumi

Organizācijas var izveidot e-pasta ziņojumu veidnes dažādiem gadījumiem. Varat atlasīt galvenes attēlu, kas ir jāietver e-pasta ziņojumu veidnēs. Pēc tam atlasītā galvene ir redzama visās e-pasta ziņojumu veidnēs. Veidnes kājenē varat pievienot saiti uz savas organizācijas paziņojumu par konfidencialitāti un saziņas lietošanas noteikumiem. Papildu informāciju par veidni skatiet [E-pasta veidnes](./email-templates.md).

## <a name="offer-process"></a>Piedāvājuma process

Varat konfigurēt darba piedāvājumu apstiprināšanas procesu. Piemēram, varat norādīt, vai piedāvājums ir jāapstiprina pirms nosūtīšanas kandidātam. Varat arī pieprasīt, lai apstiprinātāji pievienotu komentāru savam lēmumam par piedāvājumu.

Ir pieejamas divas apstiprināšanas darbplūsmas: **Līdzteku** un **Secīgi**.

- **Līdzteku** — apstiprinājumi tiek vienlaikus nosūtīti visiem apstiprinātājiem.
- **Secīgi** — apstiprinājumi tiek sūtīti apstiprinātājiem noteiktā secībā.

Varat arī konfigurēt ar kandidātu pieredzi saistītās opcijas. Piemēram, viena opcija sniedz jums iespēju norādīt, vai kandidāti var noraidīt piedāvājumu bez papildu pārrunām. Ja iestatāt opcijas **Atļaut kandidātiem noraidīt piedāvājumu bez papildu diskusijas** vērtību **Nē**, kandidātiem ir pieejama poga **Noraidīt piedāvājumu**. Ja iestatāt šīs opcijas vērtību **Jā**, kandidāti var noraidīt piedāvājumu, atlasot iemeslu un pēc tam atlasot pogu **Noraidīt piedāvājumu**.

Varat arī iestatīt piedāvājumu beigu datumu un pieprasīt tā ievērošanu. Ja iestatāt opcijas **Pieprasīt beigu datumu visiem piedāvājumiem** vērtību **Jā**, piedāvājumu derīgums beidzas, kad ir pagājis jūsu norādītais stundu vai dienu skaits.

Papildinformāciju par piedāvājumu pārvaldību skatiet tēmā [Piedāvājumu pārvaldības iestatīšana](./offer-setup.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]