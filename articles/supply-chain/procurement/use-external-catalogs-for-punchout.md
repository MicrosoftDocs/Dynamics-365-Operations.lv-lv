---
title: Ārējo katalogu izmantošana elektroniskai atzīmēšanas sagādei
description: Šajā rakstā skaidrots, kā var izmantot ārējos katalogus, lai izveidotu un iesniegtu pieprasījumus.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3ef0a144cd1a893f08c73c3b00fa3cf6ae8f7bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851686"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a>Ārējo katalogu izmantošana elektroniskai atzīmēšanas sagādei

[!include [banner](../includes/banner.md)]

Izmantojot ārējos katalogus elektroniskai atzīmēšanas sagādei, jums nav jāuztur informācija par kreditoru precēm savos pamatdatos. Tā vietā iepirkumu grozs kreditora vietnē tiek pārveidots pieprasījuma rindās, kurās ir pareizā preces informācija. 

Ieteicams neuzturēt aprakstus un cenas kreditoru precēm savos preces pamatdatos. Tā vietā izmantojiet ārējos katalogus elektroniskai atzīmēšanas sagādei. Kad darbinieki izveido pieprasījumus, viņi var pāriet uz kreditora ārējā kataloga vietni (t.i., viņi atstāj jūsu sistēmu un dodas uz kreditora vietni). Preces, kas tiek pievienotas iepirkumu grozam kreditora vietnē, var pārveidot pieprasījuma rindās. Tādējādi jūs iegūstat pareizo preces informāciju: preces ID, nosaukumu, cenu un citu informāciju.

Lai izmantotu ārējos katalogus, darbiniekam ir jāizveido pieprasījums lapā **Mani pirkšanas pieprasījumi**.

Darbinieks, kurš izveido pieprasījumu, tiek dēvēts par pieprasījuma sagatavotāju. Kā sagatavotājs varat veikt tālāk aprakstītos uzdevumus.

Izmantojiet rindas darbību **Ārējie katalogi**, lai atvērtu lapu, kurā ir visi norādītajam pieprasītājam, iepirkuma juridiskajai personai un saņemošajai pārvaldības struktūrvienībai pieejamie ārējie katalogi.

Atkarībā no jūsu atļaujām mainiet pieprasītāju, iepirkuma juridisko personu un saņemošo pārvaldības struktūrvienību. Šo vērtības izmaiņas var mainīt sarakstu ar ārējiem katalogiem, kas ir pieejami pieprasītājam. Pieejamie ārējie katalogi ir atkarīgi no pašreizējiem aktīvajiem pirkšanas ierobežojumiem iepirkuma juridiskajai personai vai saņemošajai pārvaldības struktūrvienībai. Šie ierobežojumi var atļaut vai liegt piekļuvi noteiktām sagādes kategorijām. Tādējādi var tikt ietekmēts saraksts ar ārējiem katalogiem, kas tiek kartēti uz šīm sagādes kategorijām.

Papildinformāciju par ierobežojumiem skatiet sadaļā [Pirkšanas ierobežojumu pārskats](../procurement/purchase-policies.md).

- Lai atrastu ārējos katalogus noteiktām sagādes kategorijām, ievadiet tekstu katalogu meklēšanas laukā.
- Lai pievienotu preces no kreditora ārējā kataloga kreditora vietnē, noklikšķiniet uz ārējā kataloga. Pēc tam pievienojiet preces iepirkumu grozam un paņemiet tās. Iepirkumu groza rindas tiks pārsūtītas uz Microsoft Dynamics 365.

Ja sagādes kategorijām ir vairākas opcijas, atlasiet pareizo sagādes kategoriju, pirms pievienojat rindas pieprasījumam.
Pēc tam, kad rindas ir pievienotas pieprasījumam, varat pievienot vairāk rindu, neizmantojot ārējos katalogus. Vai arī varat turpināt izmantot ārējos katalogus, lai pievienotu rindas.

Kad pieprasījums ir gatavs, izmantojiet darbību **Darbplūsma** > **Iesniegt**, lai to iesniegtu apstiprināšanai.

### <a name="additional-resources"></a>Papildu resursi

- [Ārēja kataloga iestatīšana elektroniskai atzīmēšanas sagādei](set-up-external-catalog-for-punchout.md)
- [CXML uzlabojumu iegāde](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]