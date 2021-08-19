---
title: Krājumu žurnāla apstiprināšanas darbplūsmas
description: Šajā tēmā ir aprakstīts, kā uzstādīt un izmantot krājumu žurnālu apstiprināšanas darbplūsmas dažādu veidu fizisko krājumu transakcijām. Krājumu žurnāla darbplūsmas palīdz nodrošināt, ka transakcijām var grāmatot tikai apstiprinātos krājumu žurnālus.
author: sherry-zheng
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7906ac95a2421c9a974bb7f3c46ee5ee157a0b28d6e0327a139fc980cf6e9f19
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766102"
---
# <a name="inventory-journal-approval-workflows"></a>Krājumu žurnāla apstiprināšanas darbplūsmas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā uzstādīt un izmantot krājumu žurnālu apstiprināšanas darbplūsmas dažādu veidu fizisko krājumu transakcijām, piemēram, izejas un ieejas plūsmu grāmatošanu, krājumu kustības, materiālu komplektu (MK) izveidošanu un fizisko krājumu saskaņošanu. Krājumu žurnāla darbplūsmas palīdz nodrošināt, ka transakcijām var grāmatot tikai apstiprinātos krājumu žurnālus.

> [!NOTE]
> Krājumu žurnāla apstiprināšanas darbplūsmas attiecas tikai uz transakcijām, kas ierakstītas, izmantojot Krājumu vadības moduli. Tās nestrādā ar krājumu žurnāliem, kas tiek izraisīti no Noliktavas pārvaldības moduļa.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Krājumu žurnāla apstiprināšanas darbplūsmas līdzekļa iespējošana

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Inventāra un noliktavas pārvaldība*
- **Funkcionalitātes nosaukums:** *Inventāra žurnāla apstiprināšanas darbplūsma*

## <a name="create-your-inventory-journal-approval-workflows"></a>Izveidojiet jūsu krājumu žurnāla apstiprināšanas darbplūsmas

Lai iestatītu šo līdzekli, ir jāizveido darbplūsma katram krājumu žurnālu tipam, ko vēlaties kontrolēt. Tā kā dažādiem krājumu žurnālu tipiem var būt dažādas apstiprināšanas hierarhijas un darbplūsmas soļi, varat konfigurēt atsevišķas darbplūsmas katram krājumu žurnāla tipam.

Darbplūsmas atbalsta versijas kontroli, un katrai darbplūsmai ir darbplūsmas ID un aktīva versija. Varat izvēlēties aktivizēt katru jauno darbplūsmas versiju uzreiz pēc izveides vai paturēt to neaktīvu. Ja vienam žurnāla tipam nepieciešamas dažādas darbplūsmas, pēc tam izveidojiet vairākas darbplūsmas šim žurnāla tipam un pēc tam katru no tām piešķiriet citam žurnāla nosaukumam, kas izmanto šo tipu.

Lai izveidotu jūsu krājumu žurnāla apstiprināšanas darbplūsmas:

1. Dodieties uz **Krājumu vadība \> Iestatīšana\> Krājumu pārvaldības darbplūsmas**.
1. Atlasiet **Jauns** darbību rūtī.
1. Izvēlieties krājumu žurnāla tipu, kuram vēlaties iestatīt darbplūsmu:
    - **Krājumu etiķešu inventarizācijas žurnāls**
    - **Krājumu īpašumtiesību izmaiņu žurnāls**
    - **Krājumu kustības žurnāls**
    - **Krājuma pārsūtīšanas žurnāls**
    - **Krājumu skaitīšanas žurnāls**
    - **Krājumu MK žurnāls**
    - **Krājuma korekciju žurnāls**

    ![Dialoglodziņš Izveidot darbplūsmu.](media/journal-workflow-create-workflow.png "Dialoglodziņš Izveidot darbplūsmu")

1. Jūsu ierīcē tiek palaista darbplūsmas redaktora programma. (Iespējams, tiks prasīts apstiprināt šo darbību.) Izmantojiet to, lai pēc nepieciešamības izstrādātu savu darbplūsmu. Detalizētu informāciju par to, kā izmantot darbplūsmas redaktoru, skatiet [Darbplūsmas sistēmas pārskats](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Pēc darbplūsmas redaktora programmas saglabāšanas un aizvēršanas ir jāizvēlas, vai aktivizēt šo darbplūsmas versiju vai paturēt to kā deaktivizētu.

> [!NOTE]
> Darbplūsmas nodrošina versiju kontroli, kas nozīmē, ka varat skatīt izveidoto versiju sarakstu un izvēlēties, kura no tām ir aktīva. Lai skatītu pieejamo versiju sarakstu un izvēlētos, kuru aktivizēt, izvēlieties darbplūsmu, kas norādīta lapā **Krājumu pārvaldības darbplūsmas**. Darbības rūtī atveriet cilni **Darbplūsma** un atlasiet **Versijas**. Katrai darbplūsmas ID vienlaicīgi var būt aktīva tikai viena versija.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Piešķiriet apstiprinājuma darbplūsmas krājumu žurnālu nosaukumiem

Nākamā darbība ir krājumu žurnāla darbplūsmas piešķiršana katram krājumu žurnāla nosaukumam. Katram krājumu žurnāla tipam var iestatīt vairākus krājumu žurnālu nosaukumus.

Lai saistītu krājumu žurnālu darbplūsmu ar krājumu žurnāla nosaukumu:

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Žurnālu nosaukumi \> Krājumi**.
1. Atlasiet žurnāla nosaukumu no saraksta kolonnas, lai atvērtu tās iestatījumu lapu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet **Apstiprinājuma darbplūsma** uz **Jā**. Atlasiet **Jā**, ja jums tiek piedāvāts apstiprināt transakciju.

    ![Piešķirt darbplūsmu žurnāla nosaukumam.](media/journal-workflow-journal-name.png "Piešķirt darbplūsmu žurnāla nosaukumam")

1. Atveriet **Darbplūsmas** nolaižamo sarakstu un atlasiet atbilstošo darbplūsmu. Sarakstā ir parādīta katra aktīvā darbplūsma, ko esat izveidojis, lietojot darbplūsmas redaktora programmu.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Izveidojiet krājumu žurnālu un nosūtiet to apstiprināšanai

Pēc tam, kad jūs saistāt krājumu žurnāla nosaukumu ar tā atbilstošo krājumu žurnāla apstiprināšanas darbplūsmu, varēsit izveidot jaunus krājumu žurnālus, kas izmanto šo nosaukumu, un pēc tam nosūtīt šos žurnālus apstiprināšanai, izmantojot šo darbplūsmu. Jūs nevarēsit grāmatot krājumu žurnālu, kamēr to nebūs apstiprinājuši darbplūsmā konfigurētie Apstiprinātāji.

1. Navigācijas rūtī izvērsiet **Krājumu pārvaldība \> Žurnāla ieraksti \> Vienumi** un pēc tam atlasiet krājumu žurnāla tipu.
1. Atlasiet **Jauns**, lai izveidotu jaunu žurnālu atlasītajam tipam.
1. Atveras dialoglodziņš **Izveidot krājumu žurnālu**. Aizpildiet veidlapu pēc nepieciešamības un pēc tam atlasiet **Labi**, lai saglabātu žurnālu.
1. Pēc nepieciešamības aizpildiet žurnālu.
1. Kad izveidojat vai atverat krājumu žurnālu ar apstiprinājuma darbplūsmu, kas saistīta ar to, darbības rūtī būs aktīva **Darbplūsmas** poga. Kad esat gatavs iesniegt žurnālu apstiprināšanai, atlasiet pogu **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu un pēc tam atlasiet **Iesniegt**. Apstiprinājuma pieprasījums tiks maršrutēts attiecīgajam apstiprinātājam, kas tiks brīdināts, izmantojot darbplūsmā konfigurēto paziņošanas metodi.

    ![Iesniegt žurnālu apstiprināšanai.](media/journal-workflow-inventory-journal.png "Iesniegt žurnālu apstiprināšanai")

Lai atsauktu apstiprinājuma pieprasījumu, atveriet atbilstošo žurnālu, atlasiet pogu **Darbplūsma** un pēc tam atlasiet **Atsaukt**. Tādējādi darbplūsma tiks atiestatīta.

Kad žurnāls ir apstiprināts, varēsit to grāmatot. Lai grāmatotu žurnālu, Darbību rūtī atlasiet **Grāmatot**. Ja poga **Grāmatot** nav aktīva, žurnāls vēl nav apstiprināts.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Atbildēt uz krājumu žurnāla apstiprināšanas pieprasījumu

Ja esat apstiprinātājs, jums jāsaņem ziņojums ikreiz, kad ir nepieciešams apstiprinājums (kā konfigurēts atbilstošajā darbplūsmā). Pēc tam varat apstiprināt vai noraidīt žurnāla apstiprinājuma pieprasījumu, rīkojoties šādi:

1. Navigācijas rūtī izvērsiet **Krājumu pārvaldība \> Žurnāla ieraksti \> Vienumi** un pēc tam atlasiet krājumu žurnāla tipu.
1. Atveriet atbilstošo žurnālu un pārskatiet to.
1. Darbību rūtī atlasiet pogu **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu. Atlasiet vienu no norādītajiem saraksta elementiem:
    - **Apstiprināt** - lai apstiprinātu pieprasījumu.
    - **Noraidīt** – lai noraidītu pieprasījumu.
    - **Vairāk \> Pieprasījuma maiņa** — lai nosūtītu ziņojumu prasītājam, lūdzot mainīt kaut ko īpašu un pēc tam atkārtoti iesniegt.
    - **Vairāk \> Deleģēt** — lai deleģētu apstiprinājumu citam lietotājam.
    - **Vairāk \> Atsaukt** — lai atsauktu apstiprinājuma pieprasījumu (atiestata darbplūsmu).
    - **Vairāk \> Darbplūsmas vēsture** — lai skatītu šīs apstiprināšanas darbplūsmas vēsturi.

## <a name="review-the-approval-history"></a>Pārskatīt apstiprināšanas vēsturi

Tāpat kā citu tipu darbplūsmās, varat izmantot lapu **Darbplūsmas vēsture**, lai skatītu apstiprinājuma darbplūsmas vēsturi jebkuram žurnālam.

Lai pārskatītu žurnāla darbplūsmas vēsturi:

1. Navigācijas rūtī izvērsiet **Krājumu pārvaldība \> Žurnāla ieraksti \> Vienumi** un pēc tam atlasiet krājumu žurnāla tipu.
1. Atveriet attiecīgo žurnālu.
1. Darbību rūtī atlasiet pogu **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu. Atlasiet **Darbplūsmas vēsture**. Papildinformācijai skatiet [Skatīt darbplūsmas vēsturi](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]