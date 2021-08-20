---
title: Preces konfigurācijas modeļa aprēķini
description: Šajā tēmā aprakstīts, kā izveidot preces konfigurācijas modeļa atribūtu aprēķinus
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 349fed3ca75b94db2f421a1ff3c3553c96c202c37d59857a3d973f3de8f995ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755255"
---
# <a name="product-configuration-model-calculations"></a>Preces konfigurācijas modeļa aprēķini

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot preces konfigurācijas modeļa atribūtu aprēķinus.

## <a name="prerequisites"></a>Priekšnosacījumi

Aprēķinus preces konfigurēšanas modelī var izmantot, lai aprēķinātu preces konfigurācijas vērtības. Pirms varat sākt iestatīt aprēķinus, ir jāpastāv saistītajam preču konfigurācijas modelim. Konfigurācijas modeļu iestatīšanas procesa apskatu un saistītos uzdevumus skatiet sadaļā [Preču konfigurācijas modeļa iestatīšana](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Aprēķina izveide

Aprēķinu veido izteiksme un mērķa atribūts. Papildinformāciju par preču konfigurācijas modeļiem skatiet tēmā [BUJ par preces konfigurācijas modeļu aprēķiniem](calculate-product-configuration-models.md).

Lai izveidotu aprēķinu esošam preču modelim, rīkojieties šādi.

1. Dodieties uz **Preču informācijas pārvaldība \> Vispārīgi \> Preču konfigurācijas modeļi**.
1. Atlasiet preces konfigurācijas modeli un pēc tam atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Aprēķini** atlasiet **Pievienot**, lai pievienotu aprēķinu, un iestatiet šādus laukus:

    - **Nosaukums** – ievadiet aprēķina nosaukumu.
    - **Apraksts** — ievadiet aprēķina aprakstu.
    - **Mērķa atribūts** — atlasiet atribūtu, kam tiek veidots aprēķins.

1. Atlasiet **Rediģēt izteiksmi**.
1. Dialoglodziņā **Ievadīt aprēķinu** pievienojiet izteiksmei nepieciešamos atribūtus, operatorus un vērtības. Plašāku informāciju par darbībām ar šiem elementiem skatiet rakstā [Izteiksmes ierobežojumi un tabulas ierobežojumi preču konfigurācijas modeļos](expression-constraints-table-constraints-product-configuration-models.md).
1. Kad izteiksme ir gatava, atlasiet **Labi**.

## <a name="calculation-examples"></a>Aprēķina piemēri

Šajā sadaļā sniegti daži piemēri, kas parāda, kā aprēķini darbojas.

### <a name="example-1"></a>1. piemērs

Nākamajā piemērā mērķa atribūts ir Būla tipa, un aprēķinā tiek izmantota nosacījuma izteiksme:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Šī izteiksme mērķa atribūtam atgriež vērtību *Patiess*, ja vērtība `decimalAttribute2` ir lielāka par vai vienāda ar vērtību `decimalAttribute1`. Pretējā gadījumā tā atgriež Būla vērtību *Aplams*.

### <a name="example-2"></a>2. piemērs

Šajā piemērā teksta atribūts `textFixedList` tiek izmantots kā mērķa atribūts. Šis atribūts ietver šādu fiksēto sarakstu.

| Vērtība | Risinātāja vērtība |
|---|---|
| A | 1a |
| mljrd. | 2b |
| K | 2c |

Šajā ekrānuzņēmumā parādīts, kā šī atribūta iestatījumi var izskatīties jūsu sistēmā.

![Atribūta tipa iestatījumi 2. piemēram.](media/model-calculations-example2.png "Atribūta tipa iestatījumi 2. piemēram")

Atribūts tiek lietots šādā nosacījuma priekšrakstā:

`If[integerAttribute < 150, 0, 2]`

Ja `integerAttribute` ir mazāks par 150, šis priekšraksts atgriež pirmā ieraksta teksta vērtību fiksētā sarakstā *A*. Pretējā gadījumā tiek atgriezta trešā ieraksta teksta vērtība fiksētā sarakstā *C*.

> [!NOTE]
> Fiksētais saraksts ir nulles bāzes uzskaitījuma (uzskaitījuma) ekvivalents, un tā vērtībām piekļūst no atbilstošā vesela skaitļa vērtības. Tāpēc pirmā fiksētā saraksta vērtība (*A*) tiek saskaņota ar *0*, otrā vērtība (*B*) tiek saskaņota ar *1*, un trešā vērtība (*C*) tiek saskaņota ar *2*.

### <a name="example-3"></a>3. piemērs

Šajā piemērā teksta atribūts `textFixedList` tiek izmantots kā mērķa atribūts no iepriekšējā piemēra. Tas izmanto arī citu teksta `textAttribute` atribūtu, kas satur šādu fiksēto sarakstu.

| Vērtība | Risinātāja vērtība |
|---|---|
| AA | 1aa |
| BB | 2bb |

Šajā ekrānuzņēmumā parādīts, kā šī atribūta iestatījumi var izskatīties jūsu sistēmā.

![Atribūta tipa iestatījumi 3. piemēram.](media/model-calculations-example3.png "Atribūta tipa iestatījumi 3. piemēram")

Atribūta `textFixedList` vērtība tiek aprēķināta, izmantojot šādu nosacījuma priekšrakstu:

`If[textAttribute == "1aa", 0, 2]`

Ja `textAttribute` vērtība ir vienāda ar *1aa*, šī izteiksme atgriež pirmā ieraksta teksta vērtību fiksētā sarakstā `textFixedList` *A*. Pretējā gadījumā tiek atgriezta trešā ieraksta teksta vērtība fiksētā sarakstā `textFixedList` *C*.

> [!NOTE]
> - Nosacījuma priekšrakstam ir jāizmanto atribūta risinātāja vērtība.
> - Aprēķinos var lietot tikai fiksētā saraksta teksta atribūtus.

## <a name="see-also"></a>Skatiet arī

- [Biežāk uzdotie jautājumi par preču konfigurācijas modeļu aprēķiniem](calculate-product-configuration-models.md)
- [Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim](tasks/add-expression-constraint-product-configuration-model.md)
- [Pārskats par preču konfigurācijas modeļiem](product-configuration-models.md)
