---
title: Nesaistīto atmaksu apstrāde Dynamics 365 Commerce Payment Connector pakalpojumā Adyen
description: Šajā tēmā ir aprakstīts, kā darbojas nesaistītās atmaksas, kad tiek izmantots Microsoft Dynamics 365 Payment Connector pakalpojumam Adyen.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c137dcf7d35031a293c88d8c4f5dc1e5f3d9e2f9
ms.sourcegitcommit: a21a664cd35b95c8600c5af0aac588a64e892902
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/11/2021
ms.locfileid: "7623925"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Nesaistīto atmaksu apstrāde Dynamics 365 Commerce Payment Connector pakalpojumā Adyen

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā darbojas nesaistītās atmaksas, kad tiek izmantots [Microsoft Dynamics 365 Payment Connector pakalpojumam Adyen](adyen-connector.md). Kā arī tiek apskatīta iespēja apstrādāt atmaksu kā jaunu maksājuma metodi pārdošanas punktā (POS) vai zvanu centrā.

Dynamics 365 Payment Connector pakalpojumam Adyen atbalsta iespēju apstrādāt atmaksas, izmantojot citu maksāšanas metodi, nevis to, kas tika izmantota sākotnējai transakcijai. Kaut arī mēs iesakām izmantot [saistītās atmaksas](linked-refunds.md), lai apstrādātu atmaksu kā jau nodrošināto sākotnējo maksājuma metodi, dažos scenārijos ir nepieciešamas citas atmaksas metodes. Piemēram, kartei, kas tika izmantota oriģinālajam maksājumam, tagad var būt beidzies derīguma termiņš, vai tā ir nozaudēta, vai arī lietotājs, iespējams, to ir atcēlis.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai Dynamics 365 Payment Connector pakalpojumā Adyen varētu apstrādāt nesaistītās atmaksas, ir jāizpilda šādi priekšnosacījumi:

- Iestatīt [maksājuma metodes](../payment-methods.md).
- Iestatīt [visu kanālu maksājumus](../omni-channel-payments.md).

## <a name="additional-configuration"></a>Papildu konfigurācija

Dynamics 365 Payment Connector pakalpojumam Adyen nodrošina ikviena nākamajā sadaļā atbalstītā atmaksas scenārija ieviešanu. Debitoriem, kuri nelieto šeit aprakstītos scenārijus Dynamics 365 Payment Connector pakalpojumam Adyen, ir jāiestata savienotājs, kas atbalsta kredītkaršu marķieru ieviešanu.

## <a name="supported-refund-scenarios"></a>Atbalstītie atmaksas scenāriji

Dynamics 365 Commerce atbalsta iepriekš apstiprinātu transakciju atmaksas. Atmaksas var būt vai nu pilnīgi atmaksātas, vai daļēji atmaksātas transakcijas. Atmaksas nevar pārsniegt sākotnēji autorizētā maksājuma pilno summu. Nesaistītas atmaksas tiek atbalstītas tikai POS un zvanu centrā.

## <a name="enable-unlinked-refunds-functionality"></a>Iespējot nesaistīto atmaksu funkcionalitāti

Lai iespējotu nesaistīto atmaksu funkcionalitāti programmā Commerce Headquarters, veiciet tālāk minētās darbības.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**.
1. Cilnē **Visu kanālu maksājumi** opcijai **Izmantot visu kanālu maksājumus** iestatiet vērtību **Jā**.

### <a name="supported-payment-method-variants"></a>Atbalstītie maksājuma veidu varianti

Tālāk minētie maksājuma veidu varianti atbalsta nesaistītās atmaksas tieši no:

- Kartes
- Maka

Ne visi maksājuma veidu varianti atbalsta nesaistītās atmaksas. Tabulā ir sniegts biežāk izmantoto maksājumu veidu saraksts un parādītas katra veida atbalsta iespējas saistītajām un nesaistītajām atmaksām.

| Maksāšanas veids        | Saistītā atmaksa | Nesaistītā atmaksa |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Jā           | Jā             |
| amexconsumer          | Jā           | Jā             |
| amexcorporate         | Jā           | Jā             |
| amexdebit             | Jā           | Jā             |
| amexprepaid           | Jā           | Jā             |
| amexprepaidreloadable | Jā           | Jā             |
| amexsmallbusiness     | Jā           | Jā             |
| discover              | Jā           | Jā             |
| maestro               | Jā           | Jā             |
| maestrouk             | Jā           | Jā             |
| mc                    | Jā           | Jā             |
| mcalphabankbonus      | Jā           | Jā             |
| mcprepaidanonymous    | Jā           | Jā             |
| visa                  | Jā           | Jā             |
| visaalphabankbonus    | Jā           | Jā             |
| visacheckout          | Jā           | Jā             |
| visadankort           | Jā           | Jā             |
| visahipotecario       | Jā           | Jā             |
| visasaraivacard       | Jā           | Jā             |
| vpay                  | Jā           | Jā             |
| givex                 | **Nē**        | Jā             |
| svs                   | **Nē**        | Jā             |
| cup                   | Jā           | Jā             |
| diners                | Jā           | Jā             |
| interac               | **Nē**        | Jā             |
| jcb                   | Jā           | Jā             |
| jcb_applepay          | Jā           | Jā             |
| unionpay              | Jā           | Jā             |

### <a name="process-an-unlinked-refund-in-pos"></a>Apstrādāt nesaistītu atmaksu POS terminālī

Debitors atgriež preci POS kasierim atļautajā atgriešanas periodā, un var uzrādīt derīgu kvīti. Atgriešanas apstrādes laikā dialoglodziņš **Atgriešanas maksājums** ietver opciju **Izvēlieties maksāšanas veidu**. Pēc tam kasieris var izvēlēties maksāšanas veidu no atbalstītajiem atmaksas veidiem (kartes un maks).

### <a name="process-an-unlinked-refund-in-call-center"></a>Apstrādāt nesaistītu atmaksu zvanu centrā

Kad nesaistīta atmaksa tiek apstrādāta ka pasūtījums zvanu centrā, zvanu centra darbinieks atlasa maksājuma veidu, kas atšķiras no sākotnējās metodes. Pēc tam darbiniekam tiek piedāvāts iegūt administratora ignorēto personas identifikācijas numuru (PIN). PIN ir nepieciešams, pirms atšķirīgu maksājuma veidu var apstrādāt atmaksai.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Administratora ignorētā PIN iestatīšana zvanu centram

Lai iestatītu administratora ignorēto PIN zvanu centram programmā Commerce Headquarters, izpildiet tālākās darbības.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Zvanu centra iestatīšana** vai meklējiet “Ignorēt atļaujas.”
1. Atlasiet lomu, kurā atļaut nesaistīto atmaksu apstrādes atļaujas.
1. Kopsavilkuma cilnē **Atgriešana** iestatiet opciju **Atļaut alternatīvu maksājumu** uz **Jā**.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Payment Connector pakalpojumam Adyen](adyen-connector.md)

[Iepriekš apstiprinātu darījumu saistītās atmaksas](linked-refunds.md)
