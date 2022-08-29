---
title: Bāzes izmaiņas ICMS-DIF nodokļa aprēķinos precēm no piegādātājiem citās valstīs
description: Šajā rakstā ir aprakstīta ICMS-DIF nodokļu tipa aprēķinu konfigurācija, kad finanšu dokuments tiek saņemts Plkst. Mk (RS) vai São Papildmaksas (SP) stāvoklī.
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218655"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Bāzes izmaiņas (dubultā bāze) ICMS-DIF nodokļa aprēķinos precēm no piegādātājiem citās valstīs

Šajā rakstā ir aprakstīta ICMS-DIF **nodokļu tipa aprēķinu konfigurācija, kad finanšu dokuments tiek saņemts** Plkst. Mk (RS) vai São Papildmaksas (SP) stāvoklī.

Atbilstoši valsts likuma definīcijai, Imposto sobre Circulação de Mercadorias e Serviços (ICMS), kas tiek apkopota, jāatbilst šim noteikumam:

*ICMS* apkopot = ([(*Operācijas* summa - *ICMS no* avota) ÷ (1 – *ICMS %* iekšējais)] × *ICMS %* iekšējais) – *ICMS summa no avota*

## <a name="example"></a>Paraugs

Brazīlijas uzņēmums RS stāvoklī saņem finanšu dokumentu pirkšanai no kreditora SP stāvoklī. Uzņēmumam jāsavāc ICMS procentuālā starpība starp RS stāvokli (18 procenti) un SP stāvokli (12 procenti). Tomēr bāze jāaprēķina saskaņā ar iepriekšējo noteikumu.

- **Operācijas summa:** 1 000,00 Brazīlijas reāls (R$ 1000,00)
- **ICMS starpstate:** R$ 120,00
- **ICMS procenti RS stāvoklī:** 18 procenti
- **ICMS apkopošanai RS stāvoklī:** (\[(1000 – 120) ÷ (1 – 0,18)\] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Novēršana

Lai aprēķinātu diferenciāālu ICMS (ICMS-DIF) saskaņā ar RS statusa nosacījumiem, PVN kodi un PVN grupa jāiestata šādā veidā:

1. Izveidojiet PVN kodu, lai saņemtu 12 procentu ICMS (citam štatam). Šis kods tiek izmantots, lai reģistrētu kreditora nodokļu saņemamo summu.
2. Izveidojiet PVN kodu, lai savāktu ICMS-DIF. Lai definētu 18 procentu un 12 procentu starpību, šim PVN kodam procentuālajai summai jābūt 18 procenti (savam štatam). Iestatiet nodokļa tipu kā **ICMS-DIF**. Šis PVN kods aprēķina parametros jādefinē šādi:

    - Laukā **Izcelsme atlasiet bruto** summas **procentus**.
    - Aprēķina bāzes **laukā** atlasiet neto **summu katrai rindai**.
    - Nosakiet taksācijas kodu tā, lai tam finanšu vērtība būtu **3**. Šādā veidā korekcijas darbība tiks automātiski izveidota, kad ir iespējots **finanšu** grāmatu modulis.
    - PVN grupas konfigurācijā atlasiet opciju **Izmantot** **nodokli ICMS-DIF** PVN kodam.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Izmantot delta nodokļa likmi, kas tiek lietota divvalūtu ICMS-DIF PVN kodu konfigurācijā

Ja tiek lietoti iepriekš aprakstītie iestatījumi, **ICMS-DIF** PVN kods tiks aprēķināts divvalūtu pamata noteikumā. Tomēr nominālā nodokļa likme kļūst par 18 procentiem, kas atšķiras no 6 procentu likmes vienkāršajā pamat noteikumā. Šī starpība izraisa neatbilstības problēmas finanšu dokumentā un nodokļu pārskatiem. Microsoft Dynamics No 365 finanšu versijas 10.0.29 varat iespējot (Brazīlija) Konfigurējiet delta nodokļu likmi ICMS-DIF **nodokļa** **kodā duālā pamata gadījuma funkcijai līdzekļu pārvaldībā,** lai noņemtu neatbilstību.

- Papildus iepriekšējā sadaļā veicamo darbību pabeigšanai PVN **laukā PVN atlasiet ICMS 12** **PVN** kodu.
- Iestatiet ICMS-DIF **PVN koda nodokļu** likmi uz 18 procentiem. **Laukā Procenti/summa** nomināla nodokļu likme tiks parādīta kā 6 procenti.

> [!NOTE]
> **ICMS-DIF** un **ICMS 12** PVN kodiem jābūt piešķirtiem tajā pašā PVN grupā.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Bāzes maiņa (dubultā bāze) ICMS-DIF nodokļu aprēķinos precēm, kas nav nodokļu maksātāji (DIFAL) citās valstīs

Iespējojiet **(Brazīlija) Dubultās bāzes aprēķinu ICMS-DIFAL** **pārdošanas** darbību funkcijai līdzekļu pārvaldībā, lai atbalstītu pamata maiņas ICMS-DIF tirdzniecību ar ne-nodokļu maksātājiem no citas valsts. Parauga ICMS-DIF PVN kods stājas spēkā pārdošanas pasūtījuma un brīvā teksta rēķina darbībās.

Iespējojiet **(Brazīlija) Dubultās bāzes aprēķinu ICMS-DIFAL IPI gadījumiem funkcijai** **Līdzekļu** pārvaldība, lai atbalstītu scenārijus, kur tirdzniecība ar neapliktajiem patērētājiem no cita valsts arī ir atbildīga par Imposto sobre Produtos Industrializados (IPI). IPI PVN koda nodokļu summa tiks atpazīta un pielietota nodokļu bāzē ICMS-DIFAL.

- Pārdošanas pasūtījuma vai brīva teksta rēķina **virsrakstā** **kopsavilkuma** cilnes Fiskālā informācija iestatījumam gala lietotāja opcijai jābūt iestatītai uz **Jā.**
- Pirkšanas pasūtījuma vai kreditora rēķina virsrakstā **kopsavilkuma** **cilnē Fiskālā informācija opcijai Izmantot un** patēriņš jābūt iestatītai uz **Jā.**
