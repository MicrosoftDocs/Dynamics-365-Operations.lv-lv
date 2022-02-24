---
title: Pārvaldīt kreditoru sadarbības lietotājus
description: Šajā tēmā ir aprakstīts, kā varat pieprasīt jaunu kreditoru sadarbības lietotāju nodrošināšanu un kā pievienot jaunas kreditoru sadarbības kontaktpersonas.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6356c1d11ba507c0eaa42087bdebe982ef091dbd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019938"
---
# <a name="manage-vendor-collaboration-users"></a>Pārvaldīt kreditoru sadarbības lietotājus

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā varat pieprasīt jaunu kreditoru sadarbības lietotāju nodrošināšanu un kā pievienot jaunas kreditoru sadarbības kontaktpersonas. 

Kreditoru sadarbības interfeiss programmā Dynamics 365 Supply Chain Management sniedz informāciju par ārējo kreditoru pirkšanas pasūtījumiem, rēķiniem un sūtījumu krājumiem. Varat izveidot jaunas kreditoru sadarbības kontaktpersonas un pieprasīt, lai tiktu nodrošināti jauni lietotāji, ja strādājat kā ārējs kreditors ar drošības lomu **Kreditora administrators (ārējs)** vai līdzīgām atļaujām. Šos uzdevumus varat arī veikt, ja strādājat kā sagādes speciālists. Šajā tēmā šī loma atsaucas uz sagādes speciālistu, kurš strādā uzņēmumā, kam pieder Supply Chain Management instance. Papildinformāciju par to, kā ārējais kreditors var izmantot moduli Kreditoru sadarbība, skatiet tēmā [Kreditoru sadarbība ar debitoriem](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Papildinformāciju par to, kā sagādes speciālists var izmantot moduli Kreditoru sadarbība, skatiet tēmā [Kreditoru sadarbība ar ārējiem kreditoriem](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Pievienot jaunas kreditoru sadarbības kontaktpersonas
Ja vēlaties, lai kāda persona varētu piekļūt kreditoru sadarbībai, tad šī persona vispirms ir jāpievieno kā kreditoru sadarbības kontaktpersona. Iespējams, vēlaties arī pievienot kontaktpersonas tādiem darbiniekiem savā uzņēmumā, kas neizmantos kreditoru sadarbību. Piemēram, viņi varētu būt kontaktpunkts citādai sagādes informācijai. Jaunas kontaktpersonas var pievienot lapā **Visas kontaktpersonas**, kam var piekļūt izvēlnē **Kreditoru sadarbība** &gt; **Kontaktpersonas**. Lai pievienotu jaunu kontaktpersonu, rīkojieties tālāk aprakstītajā veidā.

1.  Noklikšķiniet uz **Jauns.**
2.  Ievadiet informāciju par šo kontaktpersonu.
3.  Izvēlēties, kuru juridisko personu viņi pārstāv jūsu uzņēmumā un ar kuru juridisko personu viņi sadarbojas tajā uzņēmumā, ar kuru viņi sadarbojas. To var izdarīt, atlasot vienumu pāri **Juridiskā persona manā uzņēmumā**/**Juridiskā persona debitora uzņēmumā**.
4.  Noklikšķiniet uz **Izveidot.**

Ja vēlaties dzēst kādu kontaktpersonu, varat dzēst tikai tās kontaktpersonas, ko izveidojāt jūs.

## <a name="vendor-collaboration-user-requests"></a>Kreditoru sadarbības lietotāja pieprasījumi
Kreditoru sadarbības lietotāju pieprasījumus var paaugstināt sagādes speciālists vai ārēja kreditora administrators.

-   Ja esat ārējs kreditors, pieprasījumus varat iesniegt moduļa **Kreditoru sadarbība** lapā **Visas kontaktpersonas**.
-   Ja esat sagādes speciālists, jums jāiesniedz pieprasījumi no lapas **Skatīt kontaktpersonas**. Lai to izdarītu, kreditora ieraksta darbību rūts sadaļā **Iestatījumi** atlasiet vienumu **Kontaktpersonas** &gt; **Skatīt kontaktpersonas**.

Varat iesniegt pieprasījumu nodrošināt kādu lietotāju, deaktivizēt kādu lietotāju vai modificēt drošības lomas. Ja esat ārēja kreditora administrators, jums ir jābūt reģistrētam kā kontaktpersonai attiecībā uz šī kreditora kontiem, par kuriem vēlaties iesniegt lietotāja pieprasījumus, un jums ir nepieciešama piekļuve šo kreditoru kontu kreditoru sadarbības interfeisam.  

Kad tiek iesniegts pieprasījums, tas tiek pievienots sarakstam **Kreditoru sadarbības lietotāja pieprasījumi** modulī **Kreditoru sadarbība** un sarakstam **Kreditoru sadarbības lietotāja pieprasījums** modulī **Sagāde un avoti** (modulis Sagāde un avoti nav pieejams ārējiem lietotājiem).

### <a name="provision-a-user"></a>Lietotāja nodrošināšana

Lai varētu pieprasīt, ka tiek nodrošināts jauns lietotājs, šī persona ir jāiestata kā kontaktpersona vienam vai vairākiem kreditoru kontiem. Lai izveidotu jauna kreditoru sadarbības lietotāja pieprasījumu, rīkojieties tālāk aprakstītajā veidā.

1. Lapā **Visas kontaktpersonas** noklikšķiniet uz **Nodrošināt piegādātāja lietotāju**.
2. Ievadiet šī lietotāja e-pasta adresi. Šī adrese tiks izmantota lietotājam, lai pieteiktos Supply Chain Management. Ja e-pasta adreses domēns ir reģistrēts kā nomnieks pakalpojumā Microsoft Azure, tad, lai nodrošināšanas process tiktu izpildīts sekmīgi, šai e-pasta adresei ir jābūt saistītai ar esošu Azure Active Directory (AAD) kontu. Ja e-pasta adreses domēns nav reģistrēts pakalpojumā Microsoft Azure, nodrošināšanas procesa ietvaros tiek izveidots AAD konts un jaunais lietotājs saņem uzaicinājuma pasta ziņojumu. Lietotāja reģistrācijai nevar izmantot debitoru e-pasta adreses ar tādiem domēniem kā @hotmail.com, @gmail.com vai @comcast.net.
3. Opciju **Kreditoru sadarbības piekļuve ir atļauta** iestatiet uz **Jā** visām juridiskajām personām, kurām šim lietotājam ir nepieciešama piekļuve.
4. Sadaļā **Piešķirt lietotāju lomas** atzīmējiet izvēles rūtiņu **Piešķirt** tām drošības lomām, kuras jaunajam lietotājam ir nepieciešamas.
5. Noklikšķiniet uz **Iesniegt**.

Kad tiek iesniegts kreditora lietotāja pieprasījums, atlasītajam kreditora kontam tiek iestatīta lauka **Debitoru sadarbības piekļuve ir atļauta** vērtība **Jā** un tiek sākta lietotāja pieprasījuma darbplūsma. Kā daļa no šīs darbplūsmas tiek izveidots jauns lietotājs un tiek piešķirtas drošības lomas. Turklāt tiek aktivizēts Azure B2B pakalpojums, kas iniciē mijiedarbību ar Azure portālu un jaunu vai pastāvošu AAD kontu saista ar Supply Chain Management lietotāja kontu. Papildinformāciju skatiet rakstā [Kas ir Azure AD B2B sadarbība?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Deaktivizēt lietotāju

Pastāv divi veidi, kā lietotājam atņemt piekļuvi kreditoru sadarbībai.

-   Lapā **Kontaktpersonas** attiecībā uz kreditoru opciju **Kreditoru sadarbības piekļuve ir atļauta** šai kontaktpersonai iestatiet uz **Nē**. To var atsevišķi izdarīt katrai juridiskajai personai, kurai šī persona ir kontaktpersona. Šo opciju var lietot tikai sagādes speciālisti.
-   Deaktivizējiet visu lietotāja kontu, iesniedzot pieprasījumu **Deaktivizēt kreditora lietotāju**.

Lai pieprasītu lietotāja deaktivizēšanu, veiciet tālāk norādītās darbības.

1.  Lapā **Visas kontaktpersonas** noklikšķiniet uz **Deaktivizēt** **kreditora lietotāju**.
2.  Ierakstiet komentāru laukā **Biznesa pamatojums**.
3.  Noklikšķiniet uz **Iesniegt**.

### <a name="modify-security-roles"></a>Modificēt drošības lomas

Lapa **Uzturēt piegādātāja lietotāja lomas** ir tāda pati kā lapa **Nodrošināt piegādātāja lietotāju**, izņemot to, ka var rediģēt drošības lomu sarakstu.  

Lai pieprasītu lietotāja drošības lomu modificēšanu, veiciet tālāk norādītās darbības.

1.  Lapā **Visi konti** noklikšķiniet uz **Uzturēt** **kreditora lietotāja lomas**.
2.  Ierakstiet komentāru laukā **Biznesa pamatojums**.
3.  Sadaļā **Uzturēt lietotāja lomas** atzīmējiet drošības lomas, kuras vēlaties piešķirt, vai noņemiet atzīmi tām lomām, kuras vēlaties noņemt.
4.  Noklikšķiniet uz **Iesniegt**.




