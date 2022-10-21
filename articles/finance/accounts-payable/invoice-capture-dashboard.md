---
title: Rēķina ieguves risinājumu informācijas panelis
description: Šajā rakstā ir aprakstīts rēķina ieguves risinājuma informācijas panelis.
author: sunfzam
ms.date: 10/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690151"
---
# <a name="invoice-capture-solution-dashboard"></a>Rēķina ieguves risinājumu informācijas panelis

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Rēķina tveršanas informācijas panelī ir ietvertas diagrammas, kas nodrošina importēto rēķinu pārskatu. Šīs diagrammas palīdz parādu kreditoriem (AP) pārvaldniekam analizēt rēķinu ģenerēšanas procesa veiktspēju. Kreditora vadītājs var skatīt rēķina ģenerēšanas procesa statusu un, lietojot dažādus filtrus, var skatīt arī detalizētu informāciju.

## <a name="available-charts"></a>Pieejamās diagrammas

Informācijas panelī ir pieejamas šādas diagrammas:

- **Visi fiksētie rēķini pēc statusa** – šajā diagrammā ir redzami šādi notvertā rēķina statusi. Atlasot statusu, lietotāji var filtrēt detalizētā sarakstā saglabātos rēķinus.

    - Notverti
    - Izpildīt
    - Pārskatīšanā
    - Novecojis

- **Kopējais notvertais rēķina apjoms** - šī diagramma parāda notverto rēķinu skaitu pēc perioda. Lietotāji var mainīt periodu, izmantojot nolaižamo sarakstu.
- **Notverts rēķins no visaugstākajiem** kreditoriem – šajā diagrammā ir redzams rēķinu kopskaits katram kreditoram. Augšējā daļā ir redzami kreditori, kuriem ir visvairāk rēķinu.
- **Dienas, cik ilgi jāpabeidz rēķins ar** izņēmumiem – šajā diagrammā norādīts vidējais dienu skaits, kas nepieciešams viena rēķina tveršanai. Šī informācija var palīdzēt AP pārvaldniekam analizēt laiku rēķina apstrādāšanai, ja nepieciešama manuāla iejaukšanās. Ja ir tendences uz augšu, lietotāji var pārskatīt procesa detaļas un pielāgot iestatījumus, lai palīdzētu samazināt nepieciešamo dienu skaitu.
- **Nepilnīgi rēķini līdz** neizlemtam laikam — šajā diagrammā ir norādīts, cik dienas uzņēmuma resursu plānošanas (ERP) sistēmā nav ģenerēts notvertais rēķins. Jo lielāks gaidošo dienu skaits, jo ilgāks rēķina ģenerēšanas process. KREDITORU vadītājs var detalizēti apskatīt detalizētus tvertos rēķinus un ģenerēt rēķinus ERP sistēmā.
