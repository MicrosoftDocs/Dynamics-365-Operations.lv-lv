---
title: SharePoint savienojuma konfigurēšana
description: Šajā rakstā ir izskaidrots, kā konfigurēt savienojumu, lai elektronisko rēķinu izrakstīšana varētu piekļūt Microsoft SharePoint vietnei.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: a2762178686d1f29c457b6de2a9b052fd048484b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283993"
---
# <a name="configure-a-sharepoint-connection"></a>SharePoint savienojuma konfigurēšana

[!include [banner](../includes/banner.md)]

Elektronisko rēķinu izrakstīšanas pakalpojums var lasīt failus no Microsoft SharePoint mapēm un augšupielādēt failus SharePoint. Lai nodrošinātu, ka elektronisko rēķinu izrakstīšana var piekļūt noteiktai SharePoint vietai, jums jānodrošina vietas akreditācijas dati elektronisko rēķinu izrakstīšanas pakalpojumam. Turklāt, lai nodrošinātu akreditācijas datu drošu glabāšanu, tie netiek nodrošināti tieši. Tā vietā glabājiet tos Azure atslēgas krātuvē un norādiet Azure atslēgas noslēpumu.

## <a name="grant-access-to-a-sharepoint-folder"></a>Piešķirt piekļuvi mapei SharePoint

1. Izveidojiet programmas reģistrāciju nomniekā, kur ir instalēts regulēšanas konfigurācijas pakalpojums (RCS).

    1. Pierakstieties [Azure portālā](https://portal.azure.com/).
    2. Pārejiet uz **programmu reģistrācijām**.
    3. Atlasiet **Jauna reģistrācija**.
    4. Ievadiet nosaukumu, piemēram, **SharePoint Programmu elektroniskajai rēķinu izrakstīšanai**, un pabeidziet reģistrēšanu
    5. Atlasiet jaunās programmas reģistrāciju.
    6. Cilnē Autentifikācija **iespējojiet** opciju Atļaut **publiskās klientu plūsmas**.
    4. Cilnē Sertifikāti **&noslēpumi atlasiet Jauns klienta noslēpums** **·**, lai izveidotu klienta noslēpumu.
    5. Kopēt izveidotā noslēpuma vērtību.

    Izpildiet šīs vadlīnijas:

    - Dažādiem pakalpojumiem neizmantojiet vienu un to pašu programmas reģistrāciju.
    - Izpildiet paroles [politikas ieteikumus](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Iestatīt paroļu maiņa. Rotācijas laikā izveidojiet jaunu klienta noslēpumu programmas reģistrācijai, atjauniniet atslēgas karti un pēc tam izdzēsiet veco slepeno.

2. Saglabājiet **Programmas reģistrācijas noslēpuma** **un lietojumprogrammas (klienta) ID** vērtības kā divus jaunus noslēpumus atslēgas rēķina vides iestatījumos.
3. Pievienojiet jūsu izveidotos noslēpumus atslēgas parametros Jūsu elektroniskās rēķinu izrakstīšanas vides iestatīšanai RCS.
4. Azure portālā piešķiriet piekļuvi SharePoint. Šo darbību būtu jāveic nomnieka administratoram.

    1. Atlasiet izveidoto programmas reģistrāciju.
    2. **API atļauju cilnē** atlasiet **Pievienot atļauju**.
    3. Atlasīt **Microsoft grafika (lietojumprogrammas atļaujas)** \> **vietnes. Atlasīts.**
    4. Atlasiet **Dotācijas administratora atļauju \<user&nbsp;name\>**.
    5. Pārskatiet lauku **Statuss**, lai pārliecinātos, ka atļaujas ir piešķirtas.

        ![Api atļauju cilnē piešķirtās atļaujas.](media/configured-permissions.jpg)

    6. Atveriet [Graph Explorer - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) un piesakieties.
    7. Kreisās puses rūts cilnes **Parauga vaicājumi** sadaļā **SharePoint** Vietas atlasiet Iegūt vietni, **SharePoint pamatojoties uz relatīvo vietas ceļu**.
    8. Ievadiet resursdatora **\{nosaukumu un\}** servera **\{relatīvos-ceļa parametrus \}**. Piemēram, norādiet hostdatora nosaukumu un server-relatīvo `<domain>.sharepoint.com` ceļu **\{.\}**`sites/<siteName>`**\{\}**

        > [!NOTE]
        > Noklusējuma vietnei atstājiet servera **\{relatīvo-ceļa parametru\}** tukšu.

    9. Atlasiet **Izpildīt vaicājumu** un saglabājiet rezultātu.
    10. Konfigurējiet šo vaicājumu.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        Šajā vaicājumā **\{vietas ID\}** ir iepriekšējās vaicājuma atbildes **ID** zara vērtība.

        Šeit ir pieprasījuma pamatteksts.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        Šajā pieprasījuma pamattekstā **\{programmas ID\}** ir lietojumprogrammas **(klienta) ID** vērtība, **\{un programmas nosaukums\}** ir **programmas nosaukuma** vērtība.

        ![GRĀMATOT vaicājumu.](media/app-id-query.jpg)

    11. Cilnē Mainīt **atļaujas atlasiet** Atļauju paneli **un pēc** tam atlasiet **Sites.FullControl.Visas** \> **atļaujas.** \> **·**
    12. Atlasiet **Izpildīt vaicājumu**.

Elektronisko rēķinu izrakstīšanas pakalpojumam tagad ir piekļuve jūsu vietnei SharePoint.
