---
title: Vērtības modeļu iestatīšana
description: Šajā procedūrā parādīts, kā izveidot jaunu pamatlīdzekļu grāmatu un sasaistīt to ar pamatlīdzekļu grupu.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be3b5578bd6509859c36f6a50ea9730e9ef1780e
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890716"
---
# <a name="set-up-value-models"></a>Vērtības modeļu iestatīšana

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Šajā procedūrā parādīts, kā izveidot jaunu pamatlīdzekļu grāmatu un sasaistīt to ar pamatlīdzekļu grupu.

## <a name="create-a-book"></a>Izveidot grāmatu
1. Dodieties **uz pamatlīdzekļu \> iestatīšanas \> grāmatām**.
2. Atlasiet **Jauna**.
3. Laukā **Grāmata** ievadiet vērtību.
4. Laukā **Apraksts** ievadiet kādu vērtību.
5. Iestatiet opciju **Aprēķināt** nolietojumu uz **Jā**.

    Ja opcija **Aprēķināt** nolietojumu ir iestatīta uz **Jā**, saistītā pamatlīdzekļu grāmata tiks iekļauta nolietojuma priekšlikumos. Ja iestatījums ir **Nē**, pamatlīdzekļu grāmatai automātiski netiks aprēķināts nolietojums.

6. Laukā **Nolietojuma** profils ievadiet vai atlasiet vērtību.

    * Alternatīva nolietojuma metode ir zināma arī kā nolietojuma pārslēgšanas metode. Nolietojuma priekšlikums pārslēgsies uz šo metodi, kad alternatīvās metodes aprēķinātā nolietojuma summa ir vienāda ar vai lielāka par noklusējuma nolietojuma metodes summu.
    * Ārkārtas nolietojuma metode tiem izmantota līdzekļa papildu nolietošanai neparastos apstākļos. Piemēram, šo opciju varat izmantot, lai reģistrētu nolietojumu, ko izraisa dabas katastrofas.
    * Ja atlasāt Izveidot nolietojuma pielāgojumus ar pamata pielāgojumiem, nolietojuma korekcijas tiks **automātiski** izveidotas, atjauninot pamatlīdzekļa vērtību. Pretējā gadījumā atjauninātā līdzekļa vērtība ietekmēs tikai turpmākos nolietojuma aprēķinus.

7. Iestatiet opciju **Izveidot nolietojuma korekcijas ar pamata** pielāgojumiem uz **Jā**.

    * Pēc noklusējuma pamatlīdzekļu grāmatas darbības tiek grāmatotas Virsgrāmatā. Tomēr varat atspējot grāmatas grāmatošanu Virsgrāmatā, iestatot opciju **Grāmatot Virsgrāmatā** kā **Nē**. Grāmatas, kas nav iegrāmatotas Virsgrāmatā, parasti tiek izmantotas nodokļu pārskatiem. Šī opcija dod lielāku elastīgumu, lai dzēstu pamatlīdzekļu grāmatas vēsturiskās darbības, jo darbības nav nodotas virsgrāmatai.
    * Pēc noklusējuma lauks Grāmatošanas līmenis tiek iestatīts uz Pašreizējais līmenis, ja grāmata ir grāmatota Virsgrāmatā un Nav, ja grāmata nav grāmatota **Virsgrāmatā**. **·** **·** Atjauniniet lauka **Grāmatošanas līmenis** vērtību, ja šīs grāmatas darbības ir jāgrāmato citā līmenī.

8. Aprēķināt pozitīvo nolietojumu.

    * Pēc noklusējuma opcija **Aprēķināt pozitīvo** nolietojumu ir iestatīta uz **Nē**. Šis iestatījums norāda, ka nolietojums kreditēs atlasīto pamatlīdzekļu grāmatu. Turklāt opcijas Atļaut atlikusī vērtība ir augstāka nekā iegādes cena un Atļaut negatīvu atlikusī vērtība ir iestatītas uz Nē, un iestatījumus **var** neatkarīgi **·** **mainīt**. 
    * Lai aprēķinātu pozitīvo nolietojumu, iestatiet opciju **Aprēķināt pozitīvo** nolietojumu uz **Jā**. Šis iestatījums norāda, ka nolietojums debetēs pamatlīdzekļu grāmatu. Ja opcija Aprēķināt pozitīvo nolietojumu ir iestatīta uz Jā, opcijas Atļaut atlikušo vērtību lielāku par iegādes cenu un Atļaut negatīvu atlikušo vērtību automātiski tiks iestatītas uz Jā, un **tās** **tiks** **·** **·** **bloķētas**. Šis bloķējums palīdz nodrošināt, ka pozitīvs nolietojums tiek attiecināts tikai uz pamatlīdzekļiem, kas ir iegūti ar negatīvu atgrāmatu vērtību (kredīts). 

10. Laukā **Kalendārs** ievadiet vai atlasiet vērtību.

    Atvasinātās grāmatas var grāmatot darbības dažādās grāmatas vienlaicīgi. Jūs varat izveidot darbības, izmantojot primāro grāmatu, un grāmatošanas laikā, precīza darbības kopija tiek grāmatota atvasinātajā grāmatā. Atvasinātās grāmatas darbībām nav nekādu pārrēķinu, tāpēc to nevajadzētu izmantot nolietojuma darbībās.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Saistīt grāmatu ar pamatlīdzekļu grupu

1. Atlasiet **Pamatlīdzekļu** grupas.
2. Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**.
3. Laukā **Lietošanas** ilgums ievadiet skaitli.

    * Ņemiet vērā, ka lauka Nolietojuma periodi vērtība tiek aprēķināta pēc vērtības Lietošanas ilgums iestatīšanas.
    * Nolietojuma aprēķināšanas metodi var iestatīt nodokļu vajadzībām, ja nepieciešams.
    * Pamatlīdzekļiem, kas ir saistīti ar nomām, lauka Lietošanas ilgums vērtība tiks ignorēta, jo mazākais no nomas termiņa pamatlīdzekļu grāmatā un pamatlīdzekļu lietošanas **laikā**. Ja nomas grāmatai īpašumtiesību pārsūtīšanas opcija ir iestatīta uz Jā, lauka Lietošanas ilgums vērtība vienmēr **būs** **·** **pamatlīdzekļa** lietošanas ilgums.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
