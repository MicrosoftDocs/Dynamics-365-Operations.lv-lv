---
title: Debitoru portāla lietotāju izveide un pārvaldība
description: Šajā tēmā ir izskaidrots, kā izveidot Debitoru portāla lietotāju kontus un iestatīt tiem atļaujas.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: c56e41b8ea5039531205083b5b42aff05e05cf66
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413987"
---
# <a name="create-and-manage-customer-portal-users"></a>Debitoru portāla lietotāju izveide un pārvaldība

Standarta ieviešanas gadījumā lietotājiem nav iespēju pašiem reģistrēties tīmekļa vietnēm, kas izveidotas, izmantojot Debitoru portālu. Lai pierakstītos tīmekļa vietnē un to izmantotu, administratoram lietotāji ir jāuzaicina. Korporācija Microsoft ar nolūku ir bloķējusi lietotāju pašu reģistrācijas iespēju.

Pirms lietotājs var izmantot tīmekļa vietni, šim lietotājam jāizveido kontakta ieraksts. Šis ieraksts norāda, kuram Debitoru kontam un juridiskai personai lietotājs pieder. Šī informācija ir svarīga, lai nodrošinātu, ka lietotājs var izveidot un skatīt pārdošanas pasūtījumus.

Kad lietotāji pašreģistrējas, kontaktpersonu ieraksti tiek izveidoti automātiski. Tāpēc nevar nodrošināt, ka lietotājs atlasa pareizo Debitoru kontu un juridisko personu. No otras puses, uzaicinājuma process ļauj administratoram piešķirt pareizo Debitoru kontu un juridisko personu kontaktpersonas ierakstam, pirms tiek nosūtīts uzaicinājums. Ja domājat par risinājuma pielāgošanu, lai lietotāji paši varētu veikt reģistrāciju, noteikti apsveriet iespējamās sekas.

## <a name="prerequisite-setup"></a>Priekšnoteikumu iestatīšana

Kontakti Power Apps portālos tiek saglabāti kā ieraksti elementā **Kontaktpersonas** pakalpojumā Common Data Service. Pēc tam duālais ieraksts pēc vajadzības sinhronizē šos ierakstus ar Microsoft Dynamics 365 Supply Chain Management.

![![Sistēmas diagramma Debitoru portāla kontaktpersonām](media/customer-portal-contacts.png "Sistēmas diagramma Debitoru portāla kontaktpersonām")](media/customer-portal-contacts.png "System diagram for Customer portal contacts")

Pirms sākat uzaicināt jaunus debitorus, pārliecinieties, ka esat iespējojis elementa **Kontaktpersonas** kartēšanu duālajā ierakstā.

## <a name="the-invitation-process"></a>Uzaicinājuma process

Lai uzaicinātu esošo kontaktpersonu Debitoru portālā, izpildiet norādījumus sadaļā [Uzaicināt kontaktpersonas savos portālos](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) Power Apps portālu dokumentācijā.

Pirmsuzaicināt debitoru pievienoties Debitoru portālam, pārliecinieties, ka debitora [kontaktinformācijas ieraksts](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) ir pieejams un ir iestatīts, kā norādīts zemāk.

1. Iestatiet lauku **Uzņēmums** uz to juridisko personu, kurai vēlaties pievienot debitoru programmatūrā Supply Chain Management.
2. Iestatiet lauku **Kontu skaits** uz to debitora kontu skaitu, kādu vēlaties lietotājam programmatūrā Supply Chain Management.

Kad kontaktpersona ir izveidota, jūs varat to redzēt Supply Chain Management.

Plašāku informāciju skatiet [Konfigurēt kontaktpersonu izmantošanai portālā](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) Power Apps portālu dokumentācijā.

## <a name="out-of-box-web-roles-and-entity-permissions"></a>Standarta tīmekļa lapu lomas un elementu atļaujas

Lietotāja lomas Power Apps portālos nosaka [tīmekļa lapas lomas](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) un [elementu atļaujas](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions). Dažas lomas ir definētas Debitora portālam standarta variantā. Varat izveidot jaunas lomas, un jūs varat modificēt vai noņemt esošās lomas.

### <a name="out-of-box-web-roles"></a>Standarta tīmekļa lapu lomas

Šajā sadaļā ir aprakstītas tīmekļa lomas, kas tiek piegādātas ar Debitoru portālu.

Plašāku informāciju par to, kā modificēt standarta lietotāja lomas skatiet sadaļā [Tīmekļa lomu izveide portāliem](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) un [Uz ierakstu balstītas drošības pievienošana, izmantojot elementa atļaujas portāliem](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)Power Apps portālu dokumentācijā.

#### <a name="administrator"></a>Administrators

Administrators pārrauga un uztur tīmekļa vietni. Šī persona nodrošinās un iestatīs Debitoru portālu. Administrators uztur portāla IT un drošības aspektus un pārliecinās, ka viss norit labi. Administrators var arī pielāgot un/vai mainīt portālu, pievienojot jaunas funkcionalitātes, izveidojot jaunas lomas un daudz ko citu.

#### <a name="customer-representative"></a>Klienta pārstāvis

Klienta pārstāvis strādā klienta uzņēmumam un ir atbildīgs par to pasūtījumu pārvaldību, kurus iesniedz uzņēmums. Klienta pārstāvis var redzēt visus pasūtījumus, kas ir iesniegti uzņēmumam un lietotājus, kuri tos ievietojuši. Turklāt klienta pārstāvis var skatīt informāciju par vispārējo kontu un to, kuras kontaktpersonas var veikt pasūtījumus šī konta vārdā.

#### <a name="authorized-users"></a>Autorizēti lietotāji

Autorizētie lietotāji var veikt pasūtījumus un skatīt to pasūtījumu statusu, kurus tie ir ievietojuši. Tomēr viņi nevar skatīt to pasūtījumu statusu, kurus ir ievietojuši citi viņu uzņēmuma lietotāji.

#### <a name="unauthorized-users"></a>Neautorizēti lietotāji

Neautorizēti lietotāji nevar skatīt nekādus datus. Viņi var skatīt tikai publisko informāciju, piemēram, noteikumus un nosacījumus, un detalizētu informāciju par uzņēmumu, kas lieto Debitoru portālu.

#### <a name="example"></a>Paraugs

Tabulā zemāk ir parādīts, kurus pārdošanas pasūtījumus lietotāji katrā tīmekļa lomā var skatīt sistēmā.

| Pārdošanas pasūtījums | Administrators | Klienta pārstāvis debitoram&nbsp;X | Autorizēts lietotājs: Jane | Autorizēts lietotājs: Sam | Neautorizēts lietotājs: May |
|---|---|---|---|---|---|
| Debitors&nbsp;X Pasūtītājs:&nbsp;Jane | Jā | Jā | Jā | Nr. | Nr. |
| Debitors&nbsp;X Pasūtītājs:&nbsp;Sam | Jā | Jā | Nr. | Jā | Nr. |
| Debitors&nbsp;Y Pasūtītājs:&nbsp;May | Jā | Nr. | Nr. | Nr. | Nr. |

> [!NOTE]
> Kaut gan Sam un Jane ir kontaktpersonas, kas strādā debitoram X, viņi var skatīt tikai tos pasūtījumus, kurus viņi paši ir ievietojuši, un neko citu. Lai gan May sistēmā ir pasūtījums, viņa nevar redzēt šo pasūtījumu Debitoru portālā, jo viņa ir neautorizēts lietotājs. (Turklāt viņa ir ievietojusi pasūtījumu, izmantojot kādu citu kanālu, nevis Debitoru portālu.)