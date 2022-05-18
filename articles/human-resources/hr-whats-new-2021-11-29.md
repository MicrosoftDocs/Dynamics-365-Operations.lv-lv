---
title: Jaunumi vai izmaiņas Dynamics 365 Human Resources 2021. gada 19. novembrī
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir jauni vai mainīti atsevišķajā Microsoft Dynamics 365 Human Resources 2021. gada 19. novembrī.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f28057c370b27dbdad4bfe1104e9289f7df65621
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691951"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Jaunumi vai izmaiņas Dynamics 365 Human Resources 2021. gada 19. novembrī

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Microsoft Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzamajiem vispārējās pieejamības datumiem skatiet [Dynamics 365 Human Resources 2021. laidiena 2. laidienā](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ir ietverti tālāk minētās kļūdas labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4591.

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varētu atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
|---|---|---|
| 626178 | Nav norādīta navigācija no darbinieka, kurš atrodas pārvaldnieka **pašapkalpošanās programmā** | Šī problēma tagad ir labota. Navigācija ir pieejama, lai redzētu pārskata detaļas pārvaldnieka **pašapkalpošanās sadaļā**. |
| 632573 | Saglabājot kursu, nav validācijas **kļūdas** | Šī problēma tagad ir labota. Veidojot kursus ar minimālo **dalībnieku skaitu**, kas lielāks par **0**, joprojām tika atļauts saglabāt pat tad, ja maksimālais dalībnieku skaits ir 0. |
| 615955 | Veidojot jaunu personāla **atlases** pieprasījuma vietu, ir jāaizpilda kļūda "Jāaizpilda lauka mērķis". | Veidojot adresi jaunai personāla atlases pieprasījuma atrašanās vietai, tiek parādīts kļūdas ziņojums: "Ir jāaizpilda lauks "Mērķis". Tomēr lauks **Nolūks** nav pieejams lapā. |
| 620797 | Tukša dzimtes **lauka** kļūda ir maldinoša. | Ja personiskām kontaktpersonām nav ievadīts dzimums, pārskatā tiek parādīts "Noklikšķiniet vai nospiediet šeit, lai ievadītu tekstu" – tas ir maldinošs, jo laukā nevar ievadīt datus. |
| 620800 | Atvieglojumu pārskata saite ir paslēpta | Atvieglojumu pārskats pēc noklusējuma nav skatāms darbinieku **patstāvīgi lietotajā pakalpojumā**.  Saite tika pievienota darbinieku pašapkalpošanās labajā **pusē zem** saites **sadaļas** |
| 629778 | Veiktspējas problēma saistībā ar CDS integrāciju. | Ar autorizāciju saistīts pieprasījums izraisīja veiktspējas problēmu. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Lai iegūtu papildinformāciju par to, kā ieslēgt priekšskatījuma līdzekļus, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
|---|---|---|
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Drīzumā
Pilnu plānoto līdzekļu un to [plānoto laidienu sarakstu skatiet dynamics 365 un nozares mākonos: 2021. gada 2. laidienā](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
