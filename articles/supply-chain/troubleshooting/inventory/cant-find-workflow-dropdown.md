---
title: Nevar atrast krājumu žurnālu nolaižamo dialoglodziņu "Darbplūsma"
description: Nevar atrast nolaižamo dialoglodziņu "Darbplūsma" žurnāla lapā vai saistītās darbplūsmas darbības nav pieejamas
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476966"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Nevar atrast krājumu žurnālu nolaižamo dialoglodziņu "Darbplūsma"

## <a name="symptoms"></a>Simptomi

Žurnāla lapā nevar atrast **Darbplūsmas** nolaižamo dialoglodziņu, vai arī saistītās darbplūsmas operācijas nav pieejamas.

Šī problēma var rasties trīs iemeslu dēļ, kā aprakstīts sadaļās tālāk.

## <a name="resolution-1"></a>1. risinājums

Ja problēma attiecas uz visiem lietotājiem, var rasties, jo apstiprināšanas darbplūsma nav piešķirta žurnāla nosaukumam. Lai novērstu problēmu, izpildiet šīs darbības.

1. Dodieties uz **Krājumu pārvaldība &gt; Iestatīšana &gt; Žurnālu nosaukumi &gt; Krājumi**.
1. Atlasiet žurnāla nosaukumu no saraksta kolonnas, lai atvērtu tās iestatījumu lapu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Darbplūsmas apstiprināšana** uz *Jā*. Atlasiet **Jā**, ja jums tiek piedāvāts apstiprināt izmaiņās.
1. Laukā **Darbplūsma** atlasiet izdevumu pārskatītāju konfigurāciju, kuru vēlaties izmantot šim atlasītajam žurnāla nosaukumam.

## <a name="resolution-2"></a>2. risinājums

Ja darbplūsma izmanto pielāgotu kodu, pēc sistēmas jaunināšanas var rasties problēmas. Piemēram, žurnāla darbplūsmā poga **Iesniegt** var būt pelēkota, tāpēc jūs nevarat to atlasīt, lai apstiprinātu iesniegšanu.

Ja poga **Iesniegt** ir iepelēkota, iespējams, ka darbplūsma ir pielāgota, kas nozīmē darbplūsmas metodi, sadaļā `canSubmitToWorkflow()` ir `FormDataUtil`paplašināta. Lai novērstu šo problēmu, mainiet veidu, kā paplašināt metodes `canSubmitToWorkflow()` struktūras izmantošanai šajā piemērā.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>3. risinājums

Ja problēma attiecas tikai uz dažiem specifiskiem lietotājiem, iespējams, šiem lietotājiem nav drošības privilēģiju, kas nepieciešamas darbplūsmas operāciju palaišanai krājumu žurnālos. Pārbaudiet, vai katram ietekmētam lietotājam ir drošības privilēģija *Uzturēt krājumu žurnāla darbplūsmu*. Pēc noklusējuma šī privilēģija tiek piešķirta pienākumam ar tādu pašu nosaukumu un šis pienākums tiek attiecināts uz lomām *Noliktavas darbinieks* un *Noliktavas vadītājs*.
