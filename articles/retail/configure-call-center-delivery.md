---
title: Zvanu centra piegādes veidu un maksu konfigurēšana
description: Šajā tēmā ir aprakstīts, kā iestatīt zvanu centrā veikta pasūtījuma piegādes veidus un maksas programmā Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b67a1d91e41e1a4c21e0e877c06812dededbe731
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019489"
---
# <a name="configure-call-center-delivery-modes-and-charges"></a>Zvanu centra piegādes veidu un maksu konfigurēšana

[!INCLUDE [banner](includes/banner.md)]

Kad programmā Dynamics 365 Retail tiek veikts pārdošanas pasūtījums, ja persona, kas ir ievadījusi šo pārdošanas pasūtījumu, ir saistīta ar zvanu centra kanālu, tiek izmantota loģika un kārtulas, lai validētu šī pasūtījuma piegādes veidu un aprēķinātu maksas par to.

Kad veidojat pārdošanas pasūtījumu, piegādes veidu varat atlasīt pārdošanas pasūtījuma virsrakstā un pārdošanas pasūtījuma rindās. Virsrakstā atlasītais piegādes veids pēc noklusējuma tiek izmantots visām pārdošanas pasūtījuma rindām. Taču atsevišķās pārdošanas rindās šo noklusējuma piegādes veidu varat ignorēt, ja nepieciešams. Piegādes veidu varat definēt arī debitora ierakstā. Pēc tam šis piegādes veids pēc noklusējuma tiek izmantots pārdošanas pasūtījuma virsrakstā, kad šim debitoram tiek veidoti pasūtījumi.

Programmai Retail ir iespējas, kas ļauj lietotājiem ierobežot piegādes veidus, kurus var izmantot kāds kanāls, piegādes veidus, kurus var izmantot kādai precei, un piegādes veidus, kuri ir derīgi noteiktiem sūtīšanas galamērķiem. Var definēt arī maksas, lai debitora pasūtījumam tiktu pieskaitītas papildu maksas, pamatojoties uz attiecīgajam pārdošanas pasūtījumam atlasītajiem piegādes veidiem un uz kopējo pasūtījuma vērtību.

## <a name="define-delivery-modes"></a>Piegādes veidu definēšana

Lai varētu norādīt, kurus piegādes veidus var izmantot zvanu centra pasūtījumiem, un lai definētu saistītās kārtulas un maksas, ir jādefinē piegādes veidi. Dodieties uz **Pārdošana un mārketings \> Iestatīšana \> Sadale \> Piegādes veidi** Atlasiet **Jauns**, lai izveidotu jaunu piegādes veidu. Vai arī sarakstā atlasiet esošu piegādes veidu un pēc tam atlasiet **Rediģēt**, lai veiktu izmaiņas.

Laukā **Piegādes veids** varat ievadīt jebkādu burtu un ciparu kombināciju, pamatojoties uz sava uzņēmuma prasībām. Pēc tam varat izmantot lauku **Apraksts**, lai norādītu papildu kontekstu. Lauki **Maksu grupa** un **Paātrināt izpildi** ir neobligāti, un tie tiks plašāk paskaidroti tālāk šajā tēmā.

Kopsavilkuma cilnē **Mazumtirdzniecības kanāli** pievienojiet visus mazumtirdzniecības kanālus, kuriem vēlaties atļaut izmantot šo piegādes veidu, kad attiecīgajā kanālā tiek izveidotas pārdošanas transakcijas.

Kopsavilkuma cilnē **Preces** varat norādīt, kurām precēm un/vai preču kategorijām var un nevar izmantot šo piegādes veidu. Piemēram, ja kādu preci nevar nosūtīt gaisu, jo uz to attiecas bīstamu materiālu (HAZMAT) ierobežojumi, šī prece vai preču kategorija noteikti ir jāizslēdz no visiem piegādes veidiem, kas ietver transportēšanu pa gaisu.

Kopsavilkuma cilnē **Adreses** varat norādīt, kurām valstīm vai reģioniem, vai novadiem var un nevar izmantot šo piegādes veidu. Piemēram, pasūtījumiem, kas tiek sūtīti uz Havaju salām vai Aļasku, nevar izmantot piegādes pa zemi. Tādēļ šīs valstis ir jāizslēdz no visiem piegādes veidiem, kas ir saistīti ar piegādi pa zemi, bet ir jāietver visos piegādes veidos, kas ir saistīti ar piegādi pa gaisu.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Piegādes veidu validēšana zvanu centra pasūtījumam

Kad piegādes veidi ir definēti, ir jāpalaiž pakešuzdevums **Apstrādāt piegādes veidus**. Šis darbs piegādes veidus padara pieejamus, lai mazumtirdzniecības kanāliem tos varētu izmantot pārdošanas pasūtījumu procesos. Lai palaistu darbu **Apstrādāt piegādes veidus**, dodieties uz **Retail \> Mazumtirdzniecības IT \> Apstrādāt piegādes veidus**. Šis darbs ir jāpalaiž katru reizi, kad kādam mazumtirdzniecības kanālam tiek pievienoti jauni piegādes veidi vai tiek veiktas izmaiņas esošās piegādes veida/kanāla attiecībās.

Pēc pakešuzdevuma **Apstrādāt piegādes veidus** palaišanas varat doties uz **Retail \> Kanāli \> Zvanu centri \> Visi zvanu centri**. Lapas **Visi zvanu centri** darbību rūtī, cilnē **Iestatīt** atlasiet **Piegādes veidi**. Lapā **Piegādes veidi** ir uzskaitīti visi derīgie piegādes veidi atlasītajam zvanu centra kanālam. Lai rediģētu esošos piegādes veidus vai pievienotu jaunus piegādes veidus, atlasiet **Pārvaldīt piegādes veidus**. Ņemiet vērā, ka darbs **Apstrādāt piegādes veidus** ir jāpalaiž katru reizi, kad tiek veiktas kādas izmaiņas.

## <a name="define-charges-for-delivery-services"></a>Maksu definēšana piegādes pakalpojumiem

Kad debitoriem tiek veidoti pārdošanas pasūtījumi, uzņēmums var vēlēties pievienot maksas, kas tiek automātiski aprēķinātas, pamatojoties uz pasūtījumam atlasītajiem piegādes veidiem. Šīs maksas var konfigurēt tā, lai tās būtu vienādas visiem debitoriem un piegādes veidiem. Vai arī varat norādīt, ka maksām ir jāatšķiras atkarībā no debitora un/vai piegādes veida, kas ir atlasīts attiecīgajam pārdošanas pasūtījumam.

Lai definētu maksas, dodieties uz **Retail \> Kanāla iestatīšana \> Maksas \> Automātiskās maksas**. Atlasiet **Jauns**, lai pievienotu jaunas maksas. Vai arī atlasiet esošu ierakstu un pēc tam atlasiet **Rediģēt**.

Maksas var definēt tā, lai tās tiktu aprēķinātas pasūtījuma virsraksta vai pasūtījuma rindu līmenī. Izmantojiet lauku **Līmenis**, lai atlasītu nepieciešamo līmeni.

Maksas var definēt konkrētam debitoram, debitoru grupai vai visiem debitoriem. Laukā **Konta kods** atlasiet **Tabula**, lai definētu maksas, kas tiek lietotas tikai konkrētam debitoram. Atlasiet **Grupa**, lai definētu maksas konkrētai debitoru grupai. Atlasiet **Visi**, lai maksas lietotu visiem debitoriem, kas veic pārdošanas pasūtījumu, kurā tiek izmantots saistītais piegādes veids. Ja laukā **Konta kods** atlasījāt **Tabula** vai **Grupa**, laukā **Kontu saistība** atlasiet attiecīgo debitoru vai debitoru grupu.

Maksas var konfigurēt tā, lai tās tiktu lietotas konkrētam piegādes veidam, piegādes veidu grupai vai visiem piegādes veidiem. Ja laukā **Piegādes veida kods** atlasāt **Tabula**, laukā **Piegādes veida relācija** jums ir jāatlasa konkrēts piegādes veids. Ja atlasāt **Grupa**, laukā **Piegādes veida relācija** jums ir jāatlasa piegādes veida grupa. Piegādes veidu grupas tiek definētas sadaļā **Retail \> Kanāla iestatīšana \> Maksas \> Piegādes maksu grupas**. Pēc tam tās var saistīt ar vienu vai vairākiem piegādes veidiem lapā **Piegādes veidi**. Ja atlasāt kādu grupu, kad definējat maksas, šīs maksas izmanto visi piegādes veidi, kas ir saistīti ar atlasīto piegādes grupu. Visbeidzot, ja laukā **Piegādes veida kods** atlasāt **Visi**, šīs maksas izmanto visi piegādes veidi. Tādēļ nav jāatlasa nekāda vērtību laukā **Piegādes veida relācija**.

Sadaļā **Rindas** pēc nepieciešamības varat definēt vienu vai vairākas maksas pēc valūtas. Maksām ir jābūt saistītām ar izmaksu kodu, kas attiecīgajai maksai definē finanšu grāmatošanas kārtulas. Lauks **Kategorija** tiek izmantots, lai definētu veidu, kādā maksas tiek aprēķinātas. Piemēram, ja no debitoriem ir jāiekasē fiksēta likme 9,95 USD, lai pasūtījumu nosūtītu ar konkrētu piegādes veidu, izmantojiet kategoriju **Fiksēts**. Ja uzņēmums izlemj, ka maksa no debitoriem ir jāiekasē kā procentuāls daudzums no pasūtījuma kopsummas, lai segtu piegādes maksas, izmantojiet kategoriju **Procenti**. Faktiskā no debitoriem iekasētā maksa tiek definēta laukā **Maksu vērtība**.

Mazumtirdzniecības uzņēmumi bieži vien konfigurē pa pakāpēm sadalītās maksas. Tādā gadījumā summa, kas debitoriem ir jāmaksā par piegādi, ir balstīta uz pasūtījuma vērtību. Lai konfigurētu pa pakāpēm sadalītās maksas, papildus pašas maksas definēšanai laukā **Maksu vērtība** ievadiet vērtības laukā **No summas** un **Līdz summai**. Piemēram, pasūtījumiem, kuru vērtība ir mazāka par 50 USD, mazumtirgotājs par sūtīšanu iekasē 5,95 USD. Par pasūtījumiem, kuru vērtība ir vienāda ar vai lielāka par 50 USD, bet ir mazāk par 100 USD, mazumtirgotājs iekasē 7,95 USD. Visbeidzot — pasūtījumiem, kuru vērtība ir vienāda ar vai lielāka par 100 USD, mazumtirgotājs nodrošina bezmaksas sūtīšanu. Nākamajā attēlā ir parādīta šo maksu konfigurācija.

![Piemērs ar fiksētām un pa pakāpēm sadalītām maksām](media/fixedtieredcharges.png)

Maksām varat izmantot vairāku kategoriju kombināciju, ņemot vērā sava uzņēmuma vajadzības. Piemēram, visiem pasūtījumiem, kuru vērtība ir mazāka par 100 USD, par sūtīšanu tiek iekasēta fiksēta maksa 9,95 USD. Pēc tam par pasūtījumiem, kuru vērtība ir vienāda ar vai lielāka par 100 USD, piegādes maksas tiek aprēķinātas ar likmi 5 procenti no pasūtījuma vērtības. Nākamajā attēlā ir parādīta šo maksu konfigurācija.

![Piemērs ar jauktām un pa pakāpēm sadalītām maksām](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Piegādes veidu lietošana zvanu centrā pasūtījuma izveidošanas laikā

Kad tiek veidots jauns pārdošanas pasūtījums, ir jānorāda vērtība laukā **Piegādes veids**, kurš atrodas pārdošanas pasūtījuma virsraksta kopsavilkuma cilnē **Piegāde**. Šis lauks var tikt aizpildīts automātiski, pamatojoties uz noklusējuma vērtībām no debitora ieraksta.

Veidojot pārdošanas pasūtījuma rindas, tajās tiek automātiski kopēts pasūtījuma virsrakstā definētais piegādes veids. Taču varat mainīt piegādes veida iestatījumus konkrētam rindas vienumam pārdošanas pasūtījuma izveidošanas lapas sadaļā **Detalizēta informācija par rindu**, cilnē **Piegāde**.

Ja atlasītais piegādes veids nav derīgs attiecīgajai precei vai piegādes adresei, kas ir definēta šim pasūtījumam vai pasūtījuma rindai, tiek parādīts kļūdas ziņojums. Pēc tam jums ir jāatlasa piegādes veids, kas ir definēts šīs preces vai adreses konfigurācijas atbalstam.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Piegādes maksu aprēķināšana pasūtījuma izveides laikā

Ja jūsu zvanu centra kanālam ir ieslēgts iestatījums **Iespējot pasūtījuma pabeigšanu**, sūtīšanas maksas pārdošanas pasūtījumiem tiek automātiski aprēķinātas, kad lietotāji atlasa **Pabeigts**. Lapā **Pārdošanas pasūtījumu kopsavilkums** tiek parādīts šāds ziņojums: “Pa pakāpēm sadalītās maksas ir aprēķinātas.” Aprēķinātās maksas tiek pieskaitītas lauka **Pārdošanas kopsumma** vērtībai. Kopsavilkuma cilnes **Summa** laukā **Maksas** tiek radīta visam šim pasūtījumam un rindām aprēķināto maksu kopsumma. Lai redzētu detalizētāku maksu sadalījumu, atlasiet **Pasūtījums** lapā **Pārdošanas pasūtījumu kopsavilkums**, un pēc tam atlasiet opciju **Maksas**, lai apskatītu, pievienotu vai rediģētu maksas. Ņemiet vērā, ka piegādes maksu aprēķināšana pasūtījuma virsrakstam ir balstīta uz piegādes veidu, kas ir saistīts ar šo virsrakstu. Rindas līmeņa piegādes maksas tiek aprēķinātas, pamatojoties uz piegādes veidu, kas ir konfigurēts pārdošanas rindai. Ja dažādās rindās tiek izmantoti vairāki piegādes veidi, var tikt piemērotas un saskaitītas vairākas maksas. Pēc tam kopsumma tiek rādīta lapas **Pārdošanas pasūtījuma kopsavilkums** laukā **Maksas**.

Ja iestatījums **Iespējot pasūtījuma pabeigšanu** ir izslēgts, maksu aprēķināšana lietotājiem ir jāaktivizē manuāli. Lapas **Pārdošanas pasūtījums** darbību rūtī, cilnē **Pārdot**, grupā **Aprēķināt** atlasiet **Pa pakāpēm sadalītās maksas**. Tiek parādīts ziņojums “Pa pakāpēm sadalītās maksas ir aprēķinātas”. Pēc tam varat atlasīt opciju **Maksas** cilnē **Pārdot**, lai skatītu, rediģētu vai dzēstu aprēķinātās maksas.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Paātrinātās izpildes piegādes veidu lietošana zvanu centra pasūtījumiem

Jebkuram jūsu konfigurētajam piegādes veidam pēc izvēles varat piesaistīt paātrinātās izpildes kodu. Šis kods tiek izmantots kā prioritātes noteikšanas rīks kārtošanai un pārskatu izveidei. Pašlaik tas nerada pasūtījumam piemērojamas papildu maksas. Lai iestatītu paātrinātas izpildes kodus, dodieties uz **Pārdošana un mārketings \> Iestatīšana \> Sadale \> Paātrinātās izpildes kodi**.

Piemēram, pasūtījumiem, kas nākamajā dienā tiks nosūtīti pa gaisu, izdošana noliktavā katru dienu ir jāpaveic līdz 13.00. Tādā gadījumā var izveidot paātrinātās izpildes kodu, un šo kodu var saistīt ar visiem nākamās dienas piegādes veidiem, kas sistēmā ir konfigurēti. Kad noliktava izveido savu izdošanas kopumu, kā filtru var izmantot atbilstošo paātrinātas izpildes kodu laukā **Paātrināt izpildi**, lai izdošana tiktu palaista tikai pasūtījumiem, kuru piegādes veidi ir saistīti ar šo kodu.

Turklāt, kad tiek izveidots zvanu centra pasūtījums, paātrinātās izpildes kodu var manuāli lietot pārdošanas pasūtījuma virsrakstam vai atsevišķai pārdošanas pasūtījuma rindai. Un atkal šo kodu var izmantot kārtošanai vai pārskatu veidošanai. Reizēm pasūtījums ir jāapstrādā uzmanīgi, jo ir radusies klientu apkalpošanas problēma. Tādā gadījumā pasūtījuma virsrakstam vai rindām var lietot noteiktu paātrinātās izpildes kodu, lai palīdzētu identificēt šo pasūtījumu un piešķirt tam prioritāti izpildes procesa laikā.
