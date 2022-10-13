---
title: Izvietot IoT risinājumu pakalpojumā Azure
description: Sensora datu informācija izmanto datus no sensoriem, kas ir pievienoti Microsoft Azure. Šajā rakstā ir izskaidrots, kā izvietot interneta lietas (IoT) risinājumu jūsu Azure abonementā.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5026f234f1b2f38e7041098421d0261fd468db96
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643724"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Izvietot IoT risinājumu pakalpojumā Azure

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensora datu informācija izmanto datus no sensoriem, kas ir pievienoti Microsoft Azure. Lai iespējotu Azure datus izgūt no sensoriem un koplietotu tos Dynamics 365 Supply Chain Management ar, Azure abonementā ir jāizvieto interneta interneta (IoT) risinājums. Šī arhitektūras diagramma sniedz risinājumu un tā komponentu apskatu.

![Sensora datu inteliģences arhitektūras diagramma.](media/sdi-architecture.png "Sensora datu inteliģences arhitektūras diagramma")

## <a name="video-instructions"></a>Video instrukcijas

Šajā video ir parādīts, kā [ieslēgt sensora datu informācijas līdzekli un](sdi-enable-feature.md) izvietot nepieciešamos Azure resursus. Šī raksta cita sadaļa sniedz tās pašas instrukcijas uz tekstu balstītā formātā.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>Procedūra

Izpildiet šīs darbības, lai vietnē Azure izvietotu nepieciešamos resursus.

1. Piesakieties Piegādes ķēžu pārvaldībā kā administrators.
1. Dodieties uz **sistēmas administrēšanas \> iestatīšanas \> sensora datu \> informācijas izvietošanu un pievienojiet Azure resursus**, lai atvērtu izvietošanas vedni.
1. Sveiciena **lapā** izlasiet informāciju un pēc tam atlasiet **Tālāk**.
1. **Lapā Izvietot parauga IoT risinājumu Azure** lapā izlasiet informāciju un pēc tam sadaļā **Instrukcijas** atlasiet **Izvietot**.
1. Tiek atvērta jauna pārlūka cilne, kas tiek atvērta azure portālā, lai varētu izvietot Azure resursus. Ja saņemat uzaicinājumu, piesakieties, izmantojot Azure abonementa akreditācijas datus.
1. **Pielāgotas izvietošanas lapas** laukā Abonements **atlasiet** savu abonementu.
1. Laukā **Resursu grupa** atlasiet Izveidot **jaunu**, lai izveidotu resursu grupu Azure komponentiem, ko izvietojsit.
1. Nolaižamā dialoglodziņa, kas **parādās** laukā Nosaukums, ievadiet jaunās resursu grupas nosaukumu (piemēram, *IoT-demo*). Pēc tam atlasiet **Labi**.
1. Iestatiet tālāk norādītos laukus.

    - **Resursu grupa** — atlasiet tikko izveidoto resursu grupu.
    - **Reģions** – izvēlieties reģionu, ideālā gadījumā arī reģionu, kurā izvieto piegādes ķēžu pārvaldības vidi. Ņemiet vērā, ka Azure reģioniem ir atšķirīga cenu noteikšana. Jūs varat skatīt novērtētās izmaksas savam reģionam, izmantojot [Sensora datu informācijas cenas kalkulatoru](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **Piegādes ķēdes pārvaldības vides URL** – ievadiet url jūsu Piegādes ķēdes pārvaldības videi.
    - **Atkārtoti izmantot esošo Azure Iot hub** — atstājiet šo izvēles rūtiņu notīrītu.

1. Atlasiet **Tālāk: Pārskatīt + Izveidot**.
1. Pielāgotās **izvietošanas lapā** pārbaudiet, vai pārbaude ir veiksmīga, un pēc tam atlasiet **Izveidot**.
1. Lapa **Izvietošana ir progresā**, atsecē jūsu izvietošanas progresu. Izvietošanas process var ilgt līdz 30 minūtēm. Kad lapa **Izvietošana notiek**, norāda, ka izvietošana ir pabeigta, atlasiet saiti uz resursu grupas nosaukumu, lai atvērtu lapu, kurā parādīts grupā izvietoto resursu saraksts.
1. Resursu sarakstā atrodiet ierakstu, kur tipa lauks ir **iestatīts** uz Pārvaldīto *identitāti*. Kolonnā Nosaukums **atlasiet** nosaukumu, lai atvērtu detalizētas informācijas lapu resursam.
1. Kopējiet vērtību laukā **Klienta ID** (piemēram, atlasot pogu **Kopēt starpliktuvē**).
1. Atgriezieties pārlūka cilnē, kurā darbojas Piegādes ķēžu pārvaldība, *taču Neizslēdziet Azure portāla cilni*. Joprojām **ir jāatver Azure vedņa** lapā izvietot parauga IoT risinājumu. 
1. Atlasiet **Nākamais**.
1. **Lapā Savienot Azure resursus** laukā **Azure AD Programmas klienta ID** ielīmējiet **kopēto klienta ID** vērtību.
1. Atgriezieties pārlūka cilnē, kurā ir atvērts Azure portāls, *taču neaizveriet piegādes ķēžu pārvaldības cilni*. Resursa detalizētas informācijas lapai joprojām jābūt atvērtai.
1. Atlasiet pārlūka pogu **Atpakaļ**, lai atgrieztos jaunās resursu grupas resursu sarakstā.
1. Resursu sarakstā atrodiet ierakstu, kur tipa lauks **ir iestatīts** uz Azure kešatmiņa *redis*. Kolonnā Nosaukums **atlasiet** nosaukumu, lai atvērtu detalizētas informācijas lapu resursam.
1. Kreisās puses navigācijas rūtī atlasiet Piekļuves **atslēgas**.
1. Piekļuves atslēgu **lapā kopējiet** vērtību, **kas tiek rādīta primārā savienojuma virknei (StackExchange.Redis)** (piemēram, **atlasot pogu Kopēt starpliktuvē**).
1. Atgriezieties pārlūka cilnē, kur darbojas Piegādes ķēžu pārvaldība. Joprojām **ir jābūt atvērtai** lapai Savienot Azure resursus.
1. **Redis metriskajā veikala savienojuma virknes** **laukā ielīmējiet kopēto primārā savienojuma virkni (StackExchange.Redis**).
1. Atl. **Pabeigt**.

Azure resursi, kas ir pieejami Sensor Data Intelligence, tagad tiek izvietoti jūsu Azure abonementā.

> [!NOTE]
> Jebkurā laikā varat skatīt vai rediģēt savienojuma informāciju, kas ir saglabāta Piegādes ķēžu pārvaldībā, atverot **sensora datu informācijas parametru** lapu. Plašāku informāciju skatiet sensora [datu inteliģences parametros](sdi-parameters.md).
