---
title: Līdzekļu pārvaldība programmā Human Resources
description: Šajā rakstā ir aprakstīts Funkciju pārvaldības līdzeklis un tas, kā to var lietot.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5023e8b60ede1f75961abff158bec9424d1aca4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907614"
---
# <a name="manage-features-in-human-resources"></a>Līdzekļu pārvaldība programmā Human Resources


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources mēs pastāvīgi ieviešam jaunas iespējas, un vēlamies, lai klienti šos jaunos līdzekļus varētu izbaudīt pēc iespējas ātrāk. Mēs nodrošinām priekšskatījuma līdzekļus, kas ir gandrīz gatavi vispārīgai pieejamībai un ir tikuši plaši testēti. Mums vēl tikai ir jāpabeidz pēdējais posms — klientu atsauksmju un validāciju saņemšana —, pirms šie līdzekļi kļūst vispārēji pieejami.

Papildinformāciju par Human Resources jaunajiem līdzekļiem skatiet [Human Resources jaunumi](hr-admin-whats-new.md) un [Dynamics 365 un Power Platform laidiena plāns](/dynamics365/release-plans/?panel=products1#pivot=products).

**Funkciju pārvaldības** darbvieta sniedz katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju. Papildinformāciju par Līdzekļu pārvaldību skatiet [Pārskats par līdzekļu pārvaldību](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas. Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda. Tiklīdz jūs redzat jaunas iespējas **Līdzekļu pārvaldības** darbvietā, varat tās ieslēgt. Daži līdzekļi var būt ieslēgti pēc noklusējuma.

Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs. **Līdzekļu pārvaldības** darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts. Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem. Jūs nevarat izslēgt obligātos līdzekļus. Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.

## <a name="enable-or-disable-preview-features"></a>Priekšskatījuma līdzekļu iespējošana vai atspējošana

Lai piekļūtu priekšskatījuma līdzekļiem, jums vispirms tie ir jāiespējo savā vidē. Priekšskatījuma līdzekļu iespējošana un atspējošana ir atkarīga no vides.

> [!IMPORTANT]
> Priekšskatījuma līdzekļi ir pieejami tikai **Smilškastes** vidēs. Ieslēdzot priekšskatījuma līdzekli, tas tiek iespējots visiem jūsu organizācijas lietotājiem, kas atrodas attiecīgajā vidē. Izslēdzot priekšskatījuma līdzekli, tas tiek atspējots un padarīts nepieejams jūsu lietotājiem. Priekšskatījuma līdzekļiem Human Resources ir ierobežots atbalsts. Tie, iespējams, izmanto mazāk privātuma un drošības pasākumu, un tie nav ietverti Human Resources pakalpojumu līmeņa līgumā (Service Level Agreement — SLA). Jūs nedrīkstat lietot priekšskatījuma līdzekļus, lai apstrādātu personas datus (t.i., jebkura informācija, kas varētu identificēt jūs) vai apstrādāt citus datus, uz ko attiecas juridiskas vai normatīvas atbilstības prasības.

1. Human Resources atlasiet **Sistēmas administrēšana**.

2. Atlasiet elementu **Funkciju pārvaldība**.

3. Lai iespējotu priekšskatījuma līdzekli, atlasiet to no saraksta un pēc tam atlasiet **Iespējot**. Lai atspējotu priekšskatījuma līdzekli, atlasiet to no saraksta un pēc tam atlasiet **Atspējot**.

## <a name="enable-or-disable-benefits-management"></a>Atvieglojumu pārvaldības iespējošana vai atspējošana

Lai iespējotu Atvieglojumu pārvaldību, izmantojiet to pašu procedūru sadaļā [Iespējot vai atspējot priekšskatījuma līdzekļus](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Jūs nevarat atspējot Atvieglojumu pārvaldību **Ražošanas** vidē pēc tās iespējošanas. Tomēr varat atspējot Atvieglojumu pārvaldību **Smilškastes** vidē.

Papildinformāciju par atvieglojumu pārvaldības konfigurāciju un izmantošanu skatiet [Atvieglojumu pārvaldības pārskats](hr-benefits-management-overview.md).

Atvieglojumu pārvaldība aizvieto funkcionalitāti darbvietā **Atvieglojumi**. Iespējojot atvieglojumu pārvaldības priekšskatījuma līdzekli, vairs nevarēsiet piekļūt tālāk minētajām veidlapām darbvietā **Atvieglojumi**.

- **Atvieglojumi**
- **Atvieglojumu elementi**
- **Seguma aprēķina likmes**
- **Atvieglojumu reģistrācijas rezultāti**
- **Atvieglojumu termiņa un pagarinājuma beigu rezultāti**
- **Atvieglojumu piemērojamības ierobežojuma nosacījumu tipi**
- **Atvieglojumu piemērojamības politikas**
- **Piemērojamības notikumi**

Informāciju šajās lapās varat skatīt tikai lasīšanas režīmā. Ja vēlaties rediģēt informāciju, vispirms ir jāatspējo Atvieglojumu pārvaldība (piemērojams tikai **Smilškastes** vidēm).

## <a name="enable-or-disable-leave-and-absence"></a>Iespējot vai atspējot Atvaļinājumu un prombūtni

Lai iespējotu Atvaļinājumu vai prombūtni, izmantojiet to pašu procedūru sadaļā [Iespējot vai atspējot priekšskatījuma līdzekļus](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Jūs nevarat deaktivizēt **Vairāku atvaļinājumu tipu** funkciju Atvaļinājumā un prombūtnē pēc tā iespējošanas. Tas attiecas gan uz **Smilškastes**, gan **Ražošanas** vidēm.

Papildinformāciju par priekšskatījuma līdzekļiem Atvaļinājumā un prombūtnē skatiet [Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Nosūtiet mums atsauksmes

Mēs vēlamies uzzināt par jūsu pieredzi ar priekšskatījuma līdzekļiem. Lietojot šos vai citus līdzekļus, laipni lūdzam regulāri sniegt atsauksmes tālāk norādītajās vietnēs.

- [Kopiena](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) — šī vieta ir lielisks resurss, kur lietotāji var apspriest lietošanas gadījumos, uzdot jautājumus un saņemt kopienas palīdzību.
- Pastāstiet mums par līdzekļiem, kurus vēlaties redzēt produktā, vai informējiet par visām izmaiņām, kuras pēc jūsu domām mums vajadzētu ieviest esošajos līdzekļos. Iesakiet preces idejas sadaļā [Personāla vadības idejas](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Iesniegtajās atsauksmēs vai produkta apskatos, lūdzu, neiekļaujiet personas datus (jebkāda informācija, kas ļauj jūs identificēt). Ievāktā informācija varētu tikt analizēta tālāk, un tā netiek izmantota, lai atbildētu uz pieprasījumiem saskaņā ar piemērojamajiem privātuma likumiem. Uz personas datiem, kas tiek ievākti atsevišķi saskaņā ar šīm programmām, attiecas [Microsoft privātuma paziņojums](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Skatiet arī

- [Human Resources jaunumi](hr-admin-whats-new.md)
- [Dynamics 365 un Power Platform laidiena plāns](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
