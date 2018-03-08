---
title: "Izmantot ārējos katalogus elektroniskai atzīmēšanas sagādei"
description: "Šajā tēmā paskaidrots, kā izmantot ārējos katalogus pieprasījumu izveidei un iesniegšanai."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c345f1f8d1aaa93dbe02f1f8c53df63bf3488a9e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a>Izmantot ārējos katalogus elektroniskai atzīmēšanas sagādei

[!include[banner](../includes/banner.md)]

Izmantojot ārējos katalogus elektroniskai atzīmēšanas sagādei, jums nav jāuztur informācija par kreditoru precēm savos pamatdatos. Tā vietā iepirkumu grozs kreditora vietnē tiek pārveidots pieprasījuma rindās, kurās ir pareizā preces informācija. 

Ieteicams neuzturēt aprakstus un cenas kreditoru precēm savos preces pamatdatos. Tā vietā izmantojiet ārējos katalogus elektroniskai atzīmēšanas sagādei. Kad darbinieki izveido pieprasījumus, viņi var pāriet uz kreditora ārējā kataloga vietni (t.i., viņi atstāj jūsu sistēmu un dodas uz kreditora vietni). Preces, kas tiek pievienotas iepirkumu grozam kreditora vietnē, var pārveidot pieprasījuma rindās. Tādējādi jūs iegūstat pareizo preces informāciju: preces ID, nosaukumu, cenu un citu informāciju.

Lai izmantotu ārējos katalogus, darbiniekam ir jāizveido pieprasījums lapā **Mani pirkšanas pieprasījumi**.

Darbinieks, kurš izveido pieprasījumu, tiek dēvēts par pieprasījuma sagatavotāju. Kā sagatavotājs varat veikt tālāk aprakstītos uzdevumus.

Izmantojiet rindas darbību **Ārējie katalogi**, lai atvērtu lapu, kurā ir visi norādītajam pieprasītājam, iepirkuma juridiskajai personai un saņemošajai pārvaldības struktūrvienībai pieejamie ārējie katalogi.

Atkarībā no jūsu atļaujām mainiet pieprasītāju, iepirkuma juridisko personu un saņemošo pārvaldības struktūrvienību. Šo vērtības izmaiņas var mainīt sarakstu ar ārējiem katalogiem, kas ir pieejami pieprasītājam. Pieejamie ārējie katalogi ir atkarīgi no pašreizējiem aktīvajiem pirkšanas ierobežojumiem iepirkuma juridiskajai personai vai saņemošajai pārvaldības struktūrvienībai. Šie ierobežojumi var atļaut vai liegt piekļuvi noteiktām sagādes kategorijām. Tādējādi var tikt ietekmēts saraksts ar ārējiem katalogiem, kas tiek kartēti uz šīm sagādes kategorijām.

Papildinformāciju par ierobežojumiem skatiet sadaļā [Pirkšanas ierobežojumi](../procurement/purchase-policies.md).

- Lai atrastu ārējos katalogus noteiktām sagādes kategorijām, ievadiet tekstu katalogu meklēšanas laukā.
- Lai pievienotu preces no kreditora ārējā kataloga kreditora vietnē, noklikšķiniet uz ārējā kataloga. Pēc tam pievienojiet preces iepirkumu grozam un paņemiet tās. Iepirkumu groza rindas tiks pārsūtītas uz Microsoft Dynamics 365.

Ja sagādes kategorijām ir vairākas opcijas, atlasiet pareizo sagādes kategoriju, pirms pievienojat rindas pieprasījumam.
Pēc tam, kad rindas ir pievienotas pieprasījumam, varat pievienot vairāk rindu, neizmantojot ārējos katalogus. Vai arī varat turpināt izmantot ārējos katalogus, lai pievienotu rindas.

Kad pieprasījums ir gatavs, izmantojiet darbību **Darbplūsma** > **Iesniegt**, lai to iesniegtu apstiprināšanai.

