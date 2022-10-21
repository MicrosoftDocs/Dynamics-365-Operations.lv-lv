---
title: Rēķina tveršanas risinājuma darbvieta
description: Šajā rakstā ir sniegta informācija par rēķina ieguves risinājuma darbvietu.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690986"
---
# <a name="invoice-capture-solution-workspace"></a>Rēķina tveršanas risinājuma darbvieta

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Rēķinu tveršanas risinājuma līdzāsparādīšanas skatītājs

Rēķinu ievadīšana sistēmā parasti ir laikietilpīgs process, kam ir33 pret kļūdām, jo clerks ir jāpāriet uz vairākiem pielikumu failiem un logiem, lai apkopotu pareizo informācijas daļu. Dokumentu skatītājs līdzāsparādīs jūsu pieredzi rēķinu pielabošanas laikā, atvieglojot procesu, efektīvāku un precīzāku.

Līdzāsparādīšana dokumentu skatītājam ļauj lietotājiem vienā logā būt oriģinālajam dokumentam un rēķinam, kas ir atvērts līdzās. Rēķina lapa tiek aizpildīta ar informāciju, kas nāk no oriģinālā rēķina dokumenta. Skatītājs izveido savienojumu starp rēķina lapas laukiem un oriģinālo rēķina dokumentu. Skatītājs palīdz lietotājiem arī atrast rēķina lapā parādītās kļūdas.

### <a name="open-the-side-by-side-viewer"></a>Atvērt skatītāju līdzās

Microsoft Dynamics 365 Finansēs varat atvērt skatītāju līdzās no kopsavilkuma lapas saraksta vai rēķinu saraksta lapas. To var atvērt arī, divreiz noklikšķinot uz ieraksta vai atlasot rēķina numuru.

### <a name="using-the-side-by-side-viewer"></a>Līdzāsparādītas skatītāja lietošana

#### <a name="manually-review-an-invoice"></a>Manuāli pārskatīt rēķinu

Importētam rēķina dokumentam var būt nepieciešama manuāla pārskatīšana, jo radušās kļūdas vai brīdinājumi. Līdzās skatītājā dokumenta **virsrakstā tiks rādīts importēto** datu statuss, un pašreizējā versija būs **oriģinālā versija**.

Lai sāktu pārskatīt rēķinu, atlasiet Sākt **pārskatīšanu**. Visi lauki kļūst rediģējami. Lauks **Statuss** ir atjaunināts uz Tiek **pārskatīts**, un lauks **Pašreizējā versija ir** atjaunināts uz Modificēts **versija**.

#### <a name="view-and-work-with-messages"></a>Skatīt ziņojumus un strādāt ar to

Lietotājiem pārskata process ir jāsāk no ziņojumu rūts. Kļūdu ziņojumi ir norādīti ar sarkanu X, brīdinājuma ziņojumi ir norādīti ar trīsstūri, un informaīvs ziņojums ir norādīts ar apli. Ar pārliecību saistītie ziņojumi var tikt klasificēti kā brīdinājumi vai kļūdas atkarībā no konfigurācijas grupas iestatītā sliekšņa. Papildinformāciju skatiet rēķina tveršanas [risinājuma konfigurācijas grupās](invoice-capture-config-group.md).

Ziņojumu rūtī, rēķina galvenē vai rēķina rindās var ignorēt brīdinājumu un kļūdu ziņojumus. Kad ziņojums tiek ignorēts, tas vairs netiek parādīts kā kļūda vai brīdinājums un rēķina apstiprināšana neizdosies.

- Lai ignorētu ziņojumus ziņojumu rūtī, atlasiet **Ignorēt**. Lai atiestatītu ziņojumu, kas ir ignorēts, atlasiet **Ignorēt** vēlreiz. Pēc tam tā veids tiek mainīts no kļūdas vai brīdinājuma uz informāciju.
- Lai ignorētu ziņojumus no rēķina virsraksta vai rēķina rindas, atlasiet **Ignorēt** laukā. Ziņojuma simbols pazūd. Tomēr, ja ziņojums ir atiestatīts no ziņojumu rūts, tas tiks parādīts atkārtoti.

Ziņojumiem, kas saistīti ar rēķina galvenes laukiem, kad ziņojumu rūtī atlasāt, kursors tiek pārvietots uz atbilstošo lauku galvenes sadaļā.

#### <a name="proofread-and-edit-fields"></a>Korektīve un rediģēšanas lauki

Ja lauka vērtība ir nolasīta no sākotnējā rēķina, izmantojot optisko rakstzīmju atpazīšanu (OCR), laukā tiek parādīts simbols. Ja izvēlaties simbolu, dokumentu skatītājs pietuvināsies un izceļ vietu, kur lauka vērtība ir nolasīta, lai palīdzētu pārbaudīt rēķina datus.

Lai atiestatītu dokumentu skatītāju uz tā sākotnējo palielinājumu, veiciet vienu no tālāk minētajām darbībām:

- Atlasiet to pašu simbolu, kas iepriekš atlasīts.
- Atlasiet pogu dokumentu skatītāja augšējā labajā stūrī.

Pēc vajadzības labojiet laukus. Labojumi tiek automātiski saglabāti, kad kursors atstāj lauku. Simbols lauka labajā pusē norāda, ka lauks ir atjaunināts manuāli. Kad lapa tiek atsvaidzināta, simbols tiks noņemts.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Pārbaudiet rēķinu, lai saņemtus ziņojumus

Labojot lauku, lauka vērtība tiek atjaunināta, bet jauni apstiprināšanas ziņojumi netiek ģenerēti. Lai saņemtu atjauninātas apstiprināšanas ziņojumus, atlasiet **Pārbaudīt**. Ziņojumi ziņojumu rūtī, rēķina galvenē un rēķina rindās tiek atjaunināti.

#### <a name="complete-the-review"></a>Pabeigt pārskatu

Lai pabeigtu pārskatu, atlasiet Pabeigt **pārskatīšanu**. Rēķini ir pārbaudīti. Ja tiek atrastas kļūdas, dokumenta statuss tiek pārskatīts **un** tiek parādīta ziņojumu josla. Visi ziņojumi ziņojumu rūtī un rēķina virsrakstā un rindās tiek automātiski atjaunināti, lai sniegtu informāciju par neveiksmīgās pārbaudes iemesliem.

Pēc visu bloķēšanas kļūdu labošanas, pārskatīšanu var pabeigt. Dokumenta statuss tiek atjaunināts **uz Pārskatīts**, un laukus vairs nevar rediģēt. Varat restartēt pārskatu, vēlreiz atlasot **Sākt pārskatīšanu**.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Ģenerēt neizlemtu kreditora rēķinu finansēs

Lai rēķina dokumentu nosūtītu uz pievienoto Finanšu vidi, atlasiet **Ģenerēt**. Ja rēķina ģenerēšana neizdodas, ziņojumu joslā tiek parādīts kļūdas ziņojums.

#### <a name="void-an-invoice"></a>Rēķina anulēšana

Lai anulētu rēķinu, atlasiet **Anulēt**. Anulētos rēķinus nevar pārskatīt, un rēķinos nav norādīts, ka **tos pārskatīt manuāli**.

### <a name="validation-logic"></a>Apstiprināšanas loģika

Daži atslēgas lauki līdzāsparādīšanas skatītājā nepastāv rēķina sagatavošanas datos, bet tie ir nepieciešami, lai izveidotu neizlemtus rēķinus Finanses. Šie lauki tiek atvasināti no pašreizējā rēķina sagatavošanas datu un finanšu pamatdatu kombinācijas.

Lauki, kas ir jāievasina, ir **juridiska persona**, **kreditora konts** un **krājuma kods**. Tos jāievasina šādā secībā. Ja lauka atvasināšana neizdodas, process tiek apturēts.

1. **Juridiska persona** – pirmā juridiskā persona ir atvasināta. Ja juridiskajai personai ir atrasta aktīva kartēšanas kārtula, juridiskā persona tiek atvasināta, pamatojoties uz uzņēmuma nosaukumu un uzņēmuma adresi.
2. **Kreditora konts** – nākamais- kreditora konts tiek atvasināts, balstoties uz aktīvu kartēšanas noteikumu un atvasinātās juridiskās personas un kreditora adreses kombināciju.
3. **Krājuma numurs** – visbeidzot, krājuma nosaukums tiek iegūts no sagatavošanas, pamatojoties uz šādiem trim informācijas tipiem:

    - Konfigurēta kartēšanas kārtula
    - Atvasinātā juridiskā persona
    - Atvasinātā kreditora konts

Lai izpildītu pārbaudi, atlasiet **Pārbaudīt** līdzās skatītājā. Šobrīd apstiprināšana veic šādas pārbaudes:

- **Obligātā pārbaude** - šī pārbaude apstiprina obligātos laukus līdzās skatītājam. Lietotāji var izvēlēties, kuri lauki konfigurācijas iestatījuma lapā ir **obligāti**.
- **Pārliecības rezultāts** – Lietotāji var iestatīt brīdinājuma slieksni un kļūdas slieksni uzticamības punktu kopumam. Šī pārbaude fokusējas uz pārliecību no OCR, kas ir zem šiem sliekšņiem. Kļūdas vai brīdinājuma ziņojumi tiks rādīti, pamatojoties uz apstiprināšanas rezultātu.
- **Juridiska persona** - šī pārbaude apstiprina, ka juridiska persona atrodas Finanses. Ja juridiskā persona finanšu vidē nepastāv, apstiprināšana neizdodas.

Kad līdzāsparādīšana tiek izmantota pirmo reizi un **lietotājs atlasa Pārbaudi**, tiek palaisti atvasināšanas un apstiprināšanas procesi. Ja rēķini ir precīzi, apstiprināšanas process tiek palaists, kad lietotājs atlasa Pilnu **pārskatīšanu**. Tā tiek palaista arī tad, ja lietotājs atlasa Ģenerēt **kreditora rēķinu**.

Atvasināšanas process notiek pirms apstiprināšanas procesa, un visi brīdinājumi vai kļūdas tiek nāk no apstiprināšanas procesa. Brīdinājumi un kļūdas tiks reģistrētas Finansēs.
