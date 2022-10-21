---
title: Rēķina tveršanas risinājuma kartēšanas kārtulas
description: Šajā rakstā ir sniegta informācija par kartēšanas kārtulu iestatīšanu rēķina ieguves risinājumā.
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
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691010"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Rēķina tveršanas risinājuma kartēšanas kārtulas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kartēšanas kārtulās ir pamatdati Microsoft Dynamics no 365 finanšu vai uzņēmuma resursu plānošanas (ERP) sistēmas. Pēc kartēšanas kārtulu iestatīšanas, informācija, kas nepieciešama kreditora rēķinu veidojiet finanses, ir atvasināta. Izmantojot kartēšanas kārtulas, kreditoriem (AP) darbinieks pārbauda statusu, nevis manuāli aizpildīt visas trūkstošās lauka vērtības.

Ir četri kartēšanas kārtulu tipi:

- Juridiska persona
- Kreditora konts
- Krājums
- Izdevumu tips

## <a name="manage-mapping-rules-by-using-the-app"></a>Pārvaldīt kartēšanas kārtulas, izmantojot programmu

Lai pārvaldītu kartēšanas kārtulas, izmantojot programmu, atlasiet **Iestatījumi**. Cilne **Kartēšanas kārtulas iestatīšana** nodrošina četras opcijas:

- Juridiska persona 
- Kreditora konts 
- Krājuma kartēšana 
- Izdevumu tips

Piemēram, jūs atlasāt juridiskas **personas kartēšanas noteikumu** opciju. Juridiskās personas kods tiks identificēts, izmantojot uzņēmuma nosaukumu, adresi un nodokļa reģistrācijas numuru. Ja uzņēmuma nosaukumā ir **teksts "Contoso Contoso ContosoIcs USA"**, noteikums ar nosaukumu LE-USPM **būs USPM**.

Lapa rāda visus aktīvos kartēšanas nosacījumus. Ja vēlaties skatīt neaktīvās kartēšanas kārtulas, atlasiet Aktīvas **kartēšanas juridiskās personas kārtulas un pēc** tam atlasiet Neaktīvs kartējuma **juridiskās personas nosacījumi**.

Kartēšanas kārtulām ir pieejamas šādas darbības.

### <a name="create-a-mapping-rule"></a>Kartēšanas kārtulas izveide

Varat lietot divas metodes, lai izveidotu kartēšanas kārtulu:

- Atlasiet **Jauns,** lai izveidotu jaunu kartēšanas kārtulu. Pēc tam ievadiet kartēšanas kārtulas informāciju. Kārtulu **nosaukuma** vērtībai ir jābūt unikālai katram kartēšanas kārtulas tipam.
- Ja atlasāt esošu kartēšanas kārtulu, **poga Kopēt** kļūst pieejama. Atlasiet to un pēc tam **dialoglodziņā**, kas tiek parādīts, atlasiet Labi. Kartēšanas kārtula tiek izveidota, pārklājot atlasīto kārtulu.

### <a name="edit-a-mapping-rule"></a>Rediģēt kartēšanas kārtulu

Lai rediģētu kartēšanas kārtulu, atlasiet lauku un mainiet vērtību.

### <a name="activatedeactivate-mapping-rules"></a>Aktivizēt/deaktivizēt kartēšanas kārtulas

Lai deaktivizētu vienu vai vairākas kartēšanas kārtulas, atlasiet tās lapā **Aktīvas kartēšanas kārtulas** un pēc tam atlasiet **Deaktivizēt**. Kārtulas tiek pārvietotas no lapas **Aktīvi kartēšanas kārtulas** uz lapu Neaktīvās **kartēšanas** kārtulas.

Tāpat, lai aktivizētu kartēšanas noteikumus, atlasiet tos lapā Neaktīvās **kartēšanas kārtulas** un pēc tam atlasiet **Aktivizēt**.

### <a name="remove-mapping-rules"></a>Noņemt kartēšanas kārtulas

Lai noņemtu kartēšanas kārtulas, atlasiet tās un pēc tam atlasiet **Dzēst**.

### <a name="check-for-conflicts"></a>Meklēt konfliktus

Ja divām **kartēšanas** **kārtulām** ir vienādas juridiskās personas un kreditora konta vērtības, **bet** atšķirīgas krājuma nosaukuma vērtības, tiks noteikts konflikts un kartējuma kārtula netiks izveidota vai atjaunināta.

## <a name="importexport-mapping-rules-from-excel"></a>Importēt/eksportēt kartēšanas kārtulas no programmas Excel

Excel pievienojumprogrammu var izmantot, lai pārvaldītu partijas kārtulas. Pieejamas šādas opcijas:

- Lejupielādējiet Excel veidni.
- Eksportējiet uz Excel.
- Importēt no Excel faila.

### <a name="download-an-excel-template"></a>Excel veidnes lejupielāde

Lai lejupielādētu Excel veidni, atlasiet **Lejupielādēt veidni**. Pēc tam atlasiet laukus, lai iekļautu veidnē.

### <a name="export-to-excel"></a>Eksportēt programmā Excel

Variet eksportēt divējādi:

- Atlasiet **Atvērt programmā Excel Online**, lai atvērtu failu programmā Excel. Pēc tam failu var rediģēt tiešsaistē. Pēc pabeigšanas atlasiet **Saglabāt**. Visas izmaiņas tiks saglabātas lapā Kartēšanas **kārtula**.
- Atlasiet **Lejupielādēt darblapu**, lai lejupielādētu Excel failu, kurā ir kartēšanas noteikumi. Pēc tam šo failu var labot. Kad esat beidzis, atlasiet Importēt **no Excel**, lai augšupielādētu atjaunināto darblapu.

### <a name="import-from-excel"></a>Importēt no Excel

1. Atlasiet **Importēt no Excel**, lai importētu datus no XLSX faila. Varat arī importēt no komatatdalīto vērtību (CSV) vai XML failiem. Pirms importēšanas jāizlemj, vai kopijas ir atļautas.
2. Atlasiet **Pārskatīt kartējumu**, lai pārskatītu atribūtu kartēšanu un noteiktu, vai tie ir pareizi. Jūs varat modificēt kartēšanas attiecības.
3. Kad esat beidzis, atlasiet Pabeigt **importēšanu**, lai sāktu importu.
4. Varat atlasīt Sekošana **procesam**, lai atsekotu importa procesa gaitu.

    Importēšanas statuss tiek atjaunināts no **Pabeigt** **uz Parsing**, pēc tam **uz Transformācija**, bet beigās – **Pabeigts**.

Kad importēšanas process ir pabeigts, tiek parādīta statistika par veiksmīgiem procesiem, daļējām kļūdām, kļūdām un kopējo apstrādāto daudzumu.
