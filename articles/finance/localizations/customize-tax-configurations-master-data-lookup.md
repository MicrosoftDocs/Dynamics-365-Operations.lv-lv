---
title: Pielāgojiet nodokļu konfigurācijas pamatdatu uzmeklēšanai
description: Šajā tēmā skaidrots, kā pielāgot nodokļu konfigurācijas, lai paplašinātu pamatdatu uzmeklēšanas funkcionalitāti.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69541316ad4c6c4bb404ea142844ce596b5502b9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689133"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Pielāgojiet nodokļu konfigurācijas pamatdatu uzmeklēšanai

[!include [banner](../includes/banner.md)]

Rīkojieties pēc instrukcijas šajā tēmā, lai pielāgotu nodokļu konfigurācijas, lai paplašinātu pamatdatu uzmeklēšanas funkcionalitāti.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Importēt Microsoft nodrošināto nodokļu konfigurāciju

1. Regulatory Configuration Service (RCS) **Elektronisko pārskatu** darbvietā atlasiet **Microsoft** konfigurācijas nodrošinātāju.
2. Atlasiet **Repozitoriji**.
3. Atlasiet **Globāls** un pēc tam atlasiet **Atvērt**.
4. Atlasiet nodokļu konfigurāciju, piemēram, **Nodokļu aprēķina konfigurāciju**, un pēc tam cilnē **Versijas** atlasiet versiju.
5. Atlasiet **Importēt**.

> [!NOTE]
> Pēc noklusējuma tiek importēta Dataverse modeļa kartēšana . Ja konfigurācijas importēšanas procesa laikā saņemat brīdinājuma ziņojumus, iespējojiet virtuālos Dataverse elementus. Plašāku informāciju skatiet sadaļā [Virtuālo Dataverse elementu iespējošana](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Pielāgotas datu modeļa konfigurācijas izveide

1. **Elektronisko pārskatu** darbvietā atlasiet **Nodokļu konfigurācijas** un pēc tam atlasiet datu modeļa konfigurāciju, kas jāpaplašina. Piemēram, izvēlieties **Nodokļu aprēķina datu modeli**.
2. Atlasiet **Izveidot konfigurāciju**.
3. Atlasiet **Ar nodokli apliekamā dokumenta modelis, kas atvasināts no nosaukuma: Nodokļu aprēķina datu modelis, Microsoft**.
4. Laukā **Nosaukums** ievadiet **Datu modeļa pielāgošana**.
5. Atlasiet **Izveidot konfigurāciju**.

## <a name="create-customized-reference-models"></a>Pielāgoto atsauču modeļu izveide

1. Lapā **Nodokļu konfigurācijas** atlasiet **Pielāgošanas datu modelis** un pēc tam atlasiet **Noformētājs**.
2. Atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet skatu **Atsauces modelis**.

    [![Atsauces modelis.](./media/pic2.png)](./media/pic2.png)

3. Pielāgoto atsauču modeļu izveide. Pielāgotais modelis ir saknes modelis. Pielāgotā entītija ir ieraksta saraksts. Pielāgotais lauks ir virknes lauks, ko vēlaties izmantot uzmeklēšanā. Ja nepieciešams, varat pievienot vairāk lauku.
4. Atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet skatu **Ar nodokli apliekamais dokuments**.
5. Atlasiet atribūtu, kas jāsaista ar pielāgoto atsauces modeli. Piemēram, atlasiet **Pielāgotu atribūtu** un pēc tam veiciet šādas darbības:

    1. Atlasiet **Atlasīt atsauces modeli**.
    2. Atlasiet **Pielāgots modelis** un pēc tam atlasiet **Labi**. Atsauces modeļa nosaukums tiek atjaunināts līdz lauka **Fiziskās atslēgas** vērtībai.

        [![Atlasiet atsauces modeļa dialoglodziņu.](./media/pic5.png)](./media/pic5.png)

    3. Atlasiet **Saglabāt** un pēc tam **Pabeigt**.

## <a name="create-a-customized-model-mapping-configuration"></a>Pielāgotas modeļa kartējuma konfigurācijas izveide

1. **Elektronisko pārskatu** darbvietā atlasiet **Nodokļu konfigurācijas** un pēc tam atlasiet **Dataverse modeļa kartējuma** konfigurāciju.
2. Laukā **Modeļu kartējuma noklusējums** atlasiet vērtību **Nē**.
3. Atlasiet **Izveidot konfigurāciju**.
4. Atlasiet **Ar nodokli apliekamā dokumenta modeļa kartējums, kas atvasināts no nosaukuma: Dataverse modeļa kartējums, Microsoft**.
5. Laukā **Nosaukums** ievadiet **Modeļa kartējuma pielāgošana**.
6. Laukā **Mērķa modelis** atlasiet datu modeli **Pielāgošanas datu modelis**.
7. Atlasiet **Izveidot konfigurāciju**.

    [![Izveidot konfigurācijas nolaižamo dialoglodziņu.](./media/pic6.png)](./media/pic6.png)

8. Atlasiet **Pielāgošanas modeļa kartējumu** un iestatiet **Saistītās programmas** lauku savienojumam, kas tika izveidots 8. darbībā: [Pamatdatu uzmeklēšanas vides iestatīšana](tax-service-set-up-environment-master-data-lookup.md).
9. Iestatiet lauku **Modeļu kartējuma noklusējums** kā **Jā**.

## <a name="create-customized-model-mappings"></a>Pielāgoto modeļa kartējumu izveide

1. Lapā **Nodokļu konfigurācijas** atlasiet **Pielāgošanas modeļa kartējums**.
2. Atlasiet **Noformētājs** un pēc tam atlasiet **Pielāgošanas modelis**.

    [![Pielāgošanas modelis.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Modeļa kartējuma kartēšana uz Dataverse entītiju

1. Lapā **Modeļu kartējuma noformētājs** atlasiet **Pielāgošanas modelis** un pēc tam atlasiet **Noformētājs**.
2. Kokā **Datu avota tipi** atlasiet **Dataverse Tabula**.
3. Atlasiet **Pievienot sakni** cilnē **Datu avoti**.
4. Laukā **Nosaukums** ievadiet **Pielāgots Dataverse**.
5. Otrā laukā **Nosaukums** atlasiet entītiju.
6. Atlasiet **Labi**.

    [![Dialoglodziņš Tabulas datu avota rekvizīti.](./media/pic9.png)](./media/pic9.png)

7. Atlasiet **Pielāgots Dataverse** un **Pielāgota entītija** un pēc tam atlasiet **Saistīt**.

    [![Pielāgota Dataverse un Pielāgotas entītijas saistīšana.](./media/pic10.png)](./media/pic10.png)

8. Sadaļā **Pielāgots Dataverse** un **Pielāgots lauks** atlasiet lauku, un pēc tam atlasiet **Saistīt**.

    [![Pielāgota Dataverse un Pielāgota lauka saistīšana.](./media/pic11.png)](./media/pic11.png)

9. Atlasiet **Saglabāt** un pēc tam **Pabeigt**.

## <a name="create-a-customized-tax-configuration"></a>Pielāgotas nodokļu konfigurācijas izveide

1. **Elektronisko pārskatu** darbvietā atlasiet **Nodokļu konfigurācijas** un pēc tam atlasiet **Nodokļu aprēķina konfigurācija**.
2. Atlasiet **Izveidot konfigurāciju**.
3. Atlasiet **Nodokļu pakalpojuma konfigurācija, kas atvasināta no nosaukuma: Nodokļu aprēķina konfigurācija, Microsoft**.
4. Laukā **Nosaukums** ievadiet **Pielāgojuma konfigurācija**.
5. Atlasiet **Izveidot konfigurāciju**.
6. Atlasiet **Pielāgošanas konfigurācija** un pēc tam atlasiet **Noformētājs**.
7. Laukā **Datu modelis** atlasiet **Pielāgošanas datu modelis**.
8. Laukā **Datu modeļa versija** atlasiet attiecīgo datu modeļa versiju.

    [![Rekvizītu sadaļa.](./media/pic13.png)](./media/pic13.png)

9. Atlasiet **Pabeigt**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
