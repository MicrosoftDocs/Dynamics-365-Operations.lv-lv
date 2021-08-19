---
title: Līdzekļi un darba pasūtījumi
description: Šajā tēmā aprakstīti līdzekļi un darba pasūtījumi Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2872dc84ec11ae7fad9fd5b225b9207f13280db334cc0d010a3d6749a591ee2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718111"
---
# <a name="assets-and-work-orders"></a>Līdzekļi un darba pasūtījumi

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā aprakstīti līdzekļi un darba pasūtījumi Līdzekļu pārvaldībā. Līdzekļi un darba pasūtījumi ir Līdzekļu pārvaldības centrālās daļas. *Līdzeklis* ir mašīna vai mašīnas daļa, kam nepieciešama nepārtraukta uzturēšana un apkope. Līdzekļus var izveidot hierarhiskā struktūrā, un tie var būt saistīti ar funkcionālajiem novietojumiem. Uzturēšanas darbus līdzekļu struktūrā var plānot visos līmeņos.

Katram līdzeklim tiek iestatīti dažādi dati, piemēram, informācija par preci un līdzekļa specifikācija, un nepieciešamie uzturēšanas plāni. Nākamajā attēlā ir redzams pārskats par līdzekļu datiem un līdzekļu piederību darba veidiem. Sarkanaiss teksts tiek izmantots piemēriem, kas parāda pārmantošanu un atkarības.

![Shēmā ir parādīti līdzekļu dati saistībā ar darbu veidiem.](media/05-overview-image.png)

Katram darba pasūtījumam ir darba pasūtījuma veids, šāda profilaktiska uzturēšana, koriģējoša uzturēšana vai pārbaude. Darba pasūtījumā ir viens vai vairāki darba pasūtījuma darbi. Katrs darba pasūtījuma darbs definē darbu, kas jāveic līdzeklim, un saistīto darba veidu. Saistīto darba veidu piemēri ietver 10 000 km, 50 000 km, 1 gada kapitālremontu un drošības pārbaudi. Viens darba pasūtījums var būt saistīts ar vairākiem līdzekļiem.

Nākamajā attēlā ir parādīts pārskats par galvenajiem datiem darba pasūtījumā.

![Shēmā ir redzami darba pasūtījuma galvenie dati.](media/06-overview-image.png)

Darba pasūtījums var būt saistīts ar citu darba pasūtījumu, un darba veidos var ietilpt secīgi darbi, kas veido darba pasūtījumu. Parasti starp darba pasūtījumiem nav atkarību. Tāpēc tie var mainīt savu darba pasūtījuma dzīves cikla stāvokli, un tos var ieplānot neatkarīgi vienu no otra.

Darba pasūtījumus var veidot dažādos veidos, kas ir saistīti ar koriģējošu, preventīvu vai reaktīvu uzturēšanu. Darba pasūtījumus var izveidot arī manuāli. Nākamajā attēlā ir parādīts apskats par procesu automātiskai vai manuālai darba pasūtījumu izveidei.

![Shēmā ir parādīta automātiska vai manuāla darba pasūtījumu izveide.](media/07-overview-image.png)

Ja vēlaties plānot un izpildīt uzturēšanas darbu darba pasūtījumā, ir jāizpilda vairākas darbības. Nākamajā attēlā ir parādīts pārskats par darba pasūtījum apstrādi.

![Shēmā ir parādīts darba pasūtījuma apstrādes pārskats.](media/08-overview-image.png)

> [!NOTE]
> Parasti, strādājot programmā Dynamics 365 Supply Chain Management un modulī **Līdzekļu pārvaldība**, jūs atlasāt **Jauns**, lai izveidotu jaunu ierakstu, atlasāt **RediģētEdit**, lai atjauninātu esošu ierakstu, un atlasāt **Saglabāt**, lai saglabātu jaunus vai rediģētus datus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]