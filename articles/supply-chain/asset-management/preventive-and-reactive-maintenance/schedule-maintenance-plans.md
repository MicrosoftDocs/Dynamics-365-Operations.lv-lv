---
title: Plānot uzturēšanas plānus
description: Šajā tēmā ir aprakstīts, kā ieplānot uzturēšanas plānus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bd5192f727c83c017148405fb1b3ee587c118542450d46b5822d86cd1676d8fd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731323"
---
# <a name="schedule-maintenance-plans"></a>Plānot uzturēšanas plānus

[!include [banner](../../includes/banner.md)]

 

Profilaktiskās uzturēšanas plānošana ģenerē kalendāra ierakstus līdzekļiem, pamatojoties uz uzturēšanas plāniem, kas iestatīti līdzekļiem. Varat ieplānot kalendāra ierakstus, pamatojoties uz atlasītajiem uzturēšanas plāniem, līdzekļu tipiem un līdzekļiem.

1. Noklikšķiniet **Līdzekļu pārvaldība** > **Periodiskās darbības** > **Profilaktiskā uzturēšana** > **ieplānot uzturēšanas plānus**.

2. Varat atlasīt laika intervālu laukos **Periods** un **Perioda biežums**.

>[!NOTE]
>Lauki **Periods** un **Perioda biežums** norāda, cik tālu uz priekšu vēlaties izveidot uzturēšanas grafika rindas, pamatojoties uz jūsu izveidotajiem uzturēšanas plāniem (laika vai skaitītāja ziņā). Tālāk sniegtajā attēlā ir izveidotas uzturēšanas grafika rindas (= darba pasūtījuma priekšlikumi) no pašreizējā datuma un trīs mēnešus uz priekšu.

3. Pārslēgšanas pogā **Izveidot automātiski, ja tas ir norādīts rindā** atlasiet vērtību “Jā”, ja darba pasūtījumi ir jāizveido automātiski atbilstoši uzturēšanas plāna rindai.

>[!NOTE]
>Ja šī pārslēgšanas poga ir iestatīta uz “Jā” *un* ir atlasīta arī izvēles rūtiņa **Izveidot automātiski** uzturēšanas plānu rindās **Uzturēšanas plāni**, darba pasūtījumi tiek izveidoti, pamatojoties uz uzturēšanas plāna rindām, un tiek izveidotas arī uzturēšanas grafika rindas ar statusu “Darba pasūtījums izveidots”. Ja ir atlasīta tikai viena opcija (pārslēgšanas poga **Izveidot automātiski, ja tas ir norādīts rindā** šajā dialoglodziņā vai izvēles rūtiņa **Izveidot automātiski** veidlapā **Uzturēšanas plāni** ), tiek izveidotas tikai uzturēšanas grafika rindas ar statusu “Izveidots”. Tāda gadījumā darba pasūtījumi netiek izveidoti.

4. Ir iespējams ģenerēt kalendāra ierakstus, pamatojoties uz uzturēšanas plāniem (laiku vai skaitītāju), līdzekļiem, līdzekļu tipiem, funkcionālajiem novietojumiem un funkcionālo novietojumu tipiem. Ja nepieciešams, noklikšķiniet uz pogas **Filtrēt** un veiciet atlasi.

- Kas attiecas uz uzturēšanas plānu ieplānošanu funkcionālajiem novietojumiem: ja atjaunināt līdzekļu veidu, ražotāju un modeļu iestatīšanu uzturēšanas plānos kopsavilkuma cilnē **Visi funkcionālie novietojumi** > **Uzturēšanas plāni** pēc tam, kad esat ieplānojis uzturēšanas plānus, esošie ar šo funkcionālo novietojumu saistītie uzturēšanas grafika ieraksti tiek automātiski dzēsti. Lai izveidotu jaunus kalendāra ierakstus, kas atbilst atjauninātajam uzturēšanas plāna iestatījumam funkcionālajā novietojumā, ir jāpalaiž jauns uzturēšanas plāna grafiks minētajam funkcionālajam novietojumam. Vairāk informācijas par līdzekļu tipu, ražotāju un modeļu iestatīšanu funkcionālajos novietojumos lasiet sadaļā [Funkcionālo novietojumu izveide](../functional-locations/create-functional-locations.md).

>*Piemērs:* jūs vēlaties izveidot uzturēšanas plānu konkrētai funkcionālajai vietai, kas nozīmē, ka visi līdzekļi, kas iestatīti attiecīgajā funkcionālā novietojumā, tiks iekļauti, plānojot uzturēšanas plānu, jebkurā norādītajā laikā. Tāda gadījumā jūs izveidojat uzturēšanas plānu un atlasāt konkrētu funkcionālo novietojumu, bet uzturēšanas plānā NEPIEVIENOJAT nekādus līdzekļus. Rezultāts ir tāds, ka, plānojot šo uzturēšanas plānu, tiks izveidotas uzturēšanas grafika rindas visiem līdzekļiem, kas saistīti ar funkcionālo novietojumu tajā laikā.

- Ja veicat izmaiņas līdzekļu tipos, ražotājos vai modeļos sadaļā **Līdzekļu tipi**, šīs izmaiņas ietekmē tikai jaunos līdzekļus, kuri izmanto atjaunināto līdzekļu tipu. Vairāk informācijas par līdzekļu tipu iestatīšanu lasiet sadaļā [Līdzekļu tipi](../setup-for-objects/object-types.md).  

5. Noklikšķiniet uz **Labi** labi, lai sāktu uzturēšanas grafika ierakstu ģenerēšanu par līdzekļiem. Ģenerētie ieraksti tiks parādīti saraksta lapā **Viss uzturēšanas grafiks**. Nākamajā attēlā ir parādīts dialoglodziņa **Plānot uzturēšanas plānus** piemērs.

![1. attēls.](media/09-preventive-maintenance.png)

- Dialoglodziņā **Ieplānot uzturēšanas plānus** varat iestatīt pakešuzdevumus kopsavilkuma cilnē **Palaist fonā**, lai automātiski ģenerētu kalendāra ierakstus regulāros intervālos.  
- Plānojot profilaktisko uzturēšanu, uzturēšanas grafika rindas ar paredzēto sākuma datumu un laiku, kas agrāks par sistēmas datumu un laiku, netiks izveidotas.  

Attēlā tālāk ir sniegta grafiska ilustrācija uzturēšanas plāna aprēķināšanai pēc laika.  

![2. attēls.](media/10-preventive-maintenance.jpg)

Kas attiecas uz skaitītāja uzturēšanas plāniem: attēlos tālāk ir parādīti divi atšķirīgi skaitītāja reģistrācijas cikli. Tie balstīti uz uzturēšanas plāna iestatīšanu līdzeklim “V0001”, kuram paredzēts, ka līdzeklis (automašīna) nobrauks aptuveni 2000 km katru mēnesi.

Pirmajā piemērā paredzētie 2000 km netiek sasniegti katru mēnesi. Saskaņā ar skaitītāja uzturēšanas plānu slieksnis ir 2000 km, kas nozīmē, ka, palaižot uzturēšanas plāna ieplānošanu, uzturēšanas grafika rinda ir jāizveido katru reizi, kad tiek sasniegts 2000 kilometru slieksnis. 1. piemērā ir 4 reģistrācijas rindas, bet 2000 kilometru slieksnis ir sasniegts tikai vienu reizi. Tas nozīmē, ka, palaižot uzturēšanas plānu ieplānošanu šim līdzeklim, piemēram, 3 mēnešu periodā, tiks izveidota tikai viena uzturēšanas grafika rinda.

Tālāk norādītajā attēlā katru mēnesi tiek reģistrēti 2000 km. Tāpēc, ja ieplānojat šim līdzeklim uzturēšanas plānus 3 mēnešu periodā, tiktu izveidotas trīs uzturēšanas rindas. 

Šeit aprakstītie piemēri rāda, ka visām skaitītāja reģistrācijām, kas izveidotas līdzeklim, tiek rādīta tendence, kas apraksta līdzekļa nolietojumu un nodilumu. Šī tendence tiek izmantota par pamatu, aprēķinot apkopes plānu ieplānošanas laiku.

![3. attēls.](media/11-preventive-maintenance.png)

![4. attēls.](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]