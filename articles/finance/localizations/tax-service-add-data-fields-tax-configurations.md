---
title: Pievienot datu laukus nodokļu konfigurācijās
description: Šajā tēmā skaidrots, kā pielāgot nodokļu konfigurācijas, pievienojot datu laukus.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ebb186a4cb9ca61399909625233b579acd2c0ec5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022791"
---
# <a name="add-data-fields-in-tax-configurations"></a>Pievienot datu laukus nodokļu konfigurācijās

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā pielāgot nodokļu konfigurācijas, izmantojot [datu laukus, kas pievienoti nodokļu integrācijai](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Nodoku datu modeļa pielāgošana

1. Pakalpojumā Microsoft Dynamics 365 Finance dodieties uz **Elektroniskie pārskati** \> **Nodokļu konfigurācijas**.
2. Konfigurācijas kokā atlasiet **Nodokļu datu modelis - Eiropa**. Pēc tam darbību rūtī atlasiet **Izveidot konfigurāciju**.
3. Nolaižamajā dialoglodziņā atlasiet opciju **Ar nodokli apliekamais dokumenta modelis, kas atvasināts no nosaukuma: nodokļu datu modelis - Eiropa, Microsoft**, ievadiet jaunā nodokļu datu modeļa nosaukumu un pēc tam atlasiet **Izveidot konfigurāciju**.
4. Atlasiet tikko izveidoto nodokļu datu modeli un pēc tam darbību rūtī atlasiet **Veidotājs**.
5. Izvērsiet datu modeļa koku, atlasiet **Rindas** un pēc tam atlasiet **Jauns**.
6. Dialoglodziņā **Mezgla izveide** ievadiet nosaukumu, norādiet krājuma tipu un pēc tam atlasiet **Pievienot**.
7. Pievienojiet vajadzīgās kolonnas.
8. Darbības rūtī atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt**.
9. Aizveriet lapu un skatiet nodokļu datu modeļa pabeigto versiju.

## <a name="customize-the-tax-configuration"></a>Nodokļa pielāgošanas konfigurācija

1. Pakalpojumā Finance dodieties uz **Elektroniskie pārskati** \> **Nodokļu konfigurācijas**.
2. Konfigurācijas kokā atlasiet **Nodokļu configurācija - Eiropa**. Pēc tam darbību rūtī atlasiet **Izveidot konfigurāciju**.
3. Nolaižamajā dialoglodziņā atlasiet opciju **Nodokļu pakalpojuma konfigurācija, kas atvasināta no nosaukuma: nodokļu konfigurācija - Eiropa, Microsoft**, ievadiet jaunā nodokļu konfigurācijas nosaukumu un pēc tam atlasiet **Izveidot konfigurāciju**.
4. Atlasiet tikko izveidoto nodokļu konfigurāciju un pēc tam darbību rūtī atlasiet **Veidotājs**.
5. Sadaļā **Rekvizīti**, laukā **Datu modelis** atlasiet iepriekš izveidoto pielāgoto nodokļu datu modeli.
6. Laukā **Datu modeļa versijas** atlasiet nodokļu datu modeļa pabeigto versiju.
7. Atlasiet **Pievienot** un pievienojiet nepieciešamos nodokļu pasākumus.
8. Darbības rūtī atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt**.
9. Aizveriet lapu un skatiet nodokļu konfigurācijas pabeigto versiju.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Pielāgotajā nodokļu konfigurācijā ieviest nodokļu līdzekļus

1. Pakalpojumā Regulatory Configuration Service (RCS) atvēriet **Globalizācijas līdzekļi** \> **Nodoklis**.
2. Atlasiet **Pievienot**, ievadiet informāciju par jauno līdzekli un pēc tam atlasiet **Izveidot līdzekli**.
3. Cilnē **Versijas** atlasiet līdzekli un pēc tam atlasiet **Rediģēt**.
4. Cilnē **Vispārīgi**, laukā **Konfigurācijas versija** atlasiet pielāgoto nodokļu konfigurāciju un versiju.
5. Dialoglodziņā **Pārvaldīt kolonnas** atlasiet virsrakstu un rindu kolonnas, kuras vēlaties iekļaut pielāgotajā nodokļu pasākumā, un pēc tam atlasiet labo bultiņas pogu, lai tos pievienotu sarakstam **Atlasītās kolonnas**.
