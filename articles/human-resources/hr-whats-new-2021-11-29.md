---
title: Jaunumi vai izmaiņas Dynamics 365 Human Resources 2021. gada 19. novembrī
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir jauni vai mainīti savrupajā Microsoft Dynamics 365 Human Resources 2021. gada 19. novembrī.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 618d90f95637002f444b334e16d3fef466dda65e
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087478"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Jaunumi vai izmaiņas Dynamics 365 Human Resources 2021. gada 19. novembrī

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Microsoft Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunām funkcijām un to paredzamajiem vispārējās pieejamības datumiem skatiet [Dynamics 365 Human Resources 2021. gada 2. laidiena vilnī](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ir iekļauti šādi kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4591.

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varētu atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
|---|---|---|
| 626178 | Pārvaldnieka pašapkalpošanās darbinieka elementos **trūkst navigācijas** | Šī problēma tagad ir labota. Navigācija ir pieejama, lai skatītu detalizētu informāciju par pārskatu pārvaldnieka pašapkalpošanās **sistēmā**. |
| 632573 | Saglabājot kursu, nav validācijas **kļūdas** | Šī problēma tagad ir labota. Veidojot kursu ar minimālo dalībnieku **skaitu, kas** lielāks par 0, joprojām tika atļauts saglabāt pat tad, **ja maksimālais dalībnieku** skaits ir 0. |
| 615955 | Veidojot jaunu personāla atlases pieprasījuma atrašanās vietu, radās kļūda " **Lauka mērķis** ir jāaizpilda". | Veidojot adresi jaunai personāla atlases pieprasījuma atrašanās vietai, tiek parādīts kļūdas ziņojums: "Ir jāaizpilda lauks "Mērķis"." Tomēr **lauks Mērķis** lapā nav pieejams. |
| 620797 | Tukša **dzimuma lauka** kļūda ir maldinoša | Ja personisku kontaktu nav ievadīts dzimums, atskaitē tiek parādīts "Noklikšķiniet vai pieskarieties šeit, lai ievadītu tekstu" — tas ir maldinoši, jo laukā neko nevar ievadīt. |
| 620800 | Atvieglojumu pārskata saite ir paslēpta | Atvieglojumu pārskats pēc noklusējuma nav skatāms darbinieka pašapkalpošanās.**·**  Sadaļā Saites **darbinieka pašapkalpošanās** **labajai** pusei tika pievienota saite |
| 629778 | Veiktspējas problēma ar CDS integrāciju. | Ar autorizāciju saistītais pieprasījums izraisīja veiktspējas problēmu. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Lai iegūtu papildinformāciju par to, kā ieslēgt priekšskatījuma līdzekļus, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
|---|---|---|
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Drīzumā
Pilnu plānoto līdzekļu un to plānoto laidienu sarakstu skatiet [Dynamics 365 un nozares mākoņos: 2021. gada 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/). laidiena vilnis.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
