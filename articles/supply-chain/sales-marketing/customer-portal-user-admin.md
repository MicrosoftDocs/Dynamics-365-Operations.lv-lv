---
title: Debitoru portāla lietotāju izveide un pārvaldība
description: Šajā tēmā ir izskaidrots, kā izveidot Debitoru portāla lietotāju kontus un iestatīt tiem atļaujas.
author: Henrikan
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 448f315b888b63eba74dcb8b47a9b238e371bb2b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573493"
---
# <a name="create-and-manage-customer-portal-users"></a>Debitoru portāla lietotāju izveide un pārvaldība

[!include [banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Standarta ieviešanas gadījumā lietotājiem nav iespēju pašiem reģistrēties tīmekļa vietnēm, kas izveidotas, izmantojot Debitoru portālu. Lai pierakstītos tīmekļa vietnē un to izmantotu, administratoram lietotāji ir jāuzaicina. Korporācija Microsoft ar nolūku ir bloķējusi lietotāju pašu reģistrācijas iespēju.

Pirms lietotājs var izmantot tīmekļa vietni, šim lietotājam jāizveido kontakta ieraksts. Šis ieraksts norāda, kuram Debitoru kontam un juridiskai personai lietotājs pieder. Šī informācija ir svarīga, lai nodrošinātu, ka lietotājs var izveidot un skatīt pārdošanas pasūtījumus.

Kad lietotāji pašreģistrējas, kontaktpersonu ieraksti tiek izveidoti automātiski. Tāpēc nevar nodrošināt, ka lietotājs atlasa pareizo Debitoru kontu un juridisko personu. No otras puses, uzaicinājuma process ļauj administratoram piešķirt pareizo Debitoru kontu un juridisko personu kontaktpersonas ierakstam, pirms tiek nosūtīts uzaicinājums. Ja domājat par risinājuma pielāgošanu, lai lietotāji paši varētu veikt reģistrāciju, noteikti apsveriet iespējamās sekas.

## <a name="video"></a>Video
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

Video (parādīts iepriekš) [Aicināt klientus reģistrēties un izmantot jūsu klientu portālu](https://youtu.be/drGUYHX9QIQ) ir iekļauts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas ir pieejams vietnē YouTube.

## <a name="prerequisite-setup"></a>Priekšnoteikumu iestatīšana

Kontakti Power Apps portālos tiek saglabāti kā ieraksti tabulā **Kontaktpersonas** pakalpojumā Microsoft Dataverse. Pēc tam duālais ieraksts pēc vajadzības sinhronizē šos ierakstus ar Microsoft Dynamics 365 Supply Chain Management.

![Sistēmas diagramma Debitoru portāla kontaktpersonām.](media/customer-portal-contacts.png "Sistēmas diagramma Debitoru portāla kontaktpersonām")

Pirms sākat uzaicināt jaunus debitorus, pārliecinieties, ka esat iespējojis tabulas **Kontaktpersonas** kartēšanu duālajā ierakstā.

## <a name="the-invitation-process"></a>Uzaicinājuma process

Lai uzaicinātu esošo kontaktpersonu Debitoru portālā, izpildiet norādījumus sadaļā [Uzaicināt kontaktpersonas savos portālos](/powerapps/maker/portals/configure/invite-contacts) Power Apps portālu dokumentācijā.

Pirmsuzaicināt debitoru pievienoties Debitoru portālam, pārliecinieties, ka debitora [kontaktinformācijas ieraksts](/powerapps/maker/portals/configure/configure-contacts) ir pieejams un ir iestatīts, kā norādīts zemāk.

1. Iestatiet lauku **Uzņēmums** uz to juridisko personu, kurai vēlaties pievienot debitoru programmatūrā Supply Chain Management.
2. Iestatiet lauku **Kontu skaits** uz to debitora kontu skaitu, kādu vēlaties lietotājam programmatūrā Supply Chain Management.

Kad kontaktpersona ir izveidota, jūs varat to redzēt Supply Chain Management.

Plašāku informāciju skatiet [Konfigurēt kontaktpersonu izmantošanai portālā](/powerapps/maker/portals/configure/configure-contacts) Power Apps portālu dokumentācijā.

## <a name="out-of-box-web-roles-and-table-permissions"></a>Standarta tīmekļa lapu lomas un tabulu atļaujas

Lietotāja lomas Power Apps portālos nosaka [tīmekļa lapas lomas](/powerapps/maker/portals/configure/create-web-roles) un [elementu atļaujas](/powerapps/maker/portals/configure/assign-entity-permissions). Dažas lomas ir definētas Debitora portālam standarta variantā. Varat izveidot jaunas lomas, un jūs varat modificēt vai noņemt esošās lomas.

### <a name="out-of-box-web-roles"></a>Standarta tīmekļa lapu lomas

Šajā sadaļā ir aprakstītas tīmekļa lomas, kas tiek piegādātas ar Debitoru portālu.

Plašāku informāciju par to, kā modificēt standarta lietotāja lomas skatiet sadaļā [Tīmekļa lomu izveide portāliem](/powerapps/maker/portals/configure/create-web-roles) un [Uz ierakstu balstītas drošības pievienošana, izmantojot elementa atļaujas portāliem](/powerapps/maker/portals/configure/assign-entity-permissions) Power Apps portālu dokumentācijā.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]