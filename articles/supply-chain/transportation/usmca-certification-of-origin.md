---
title: USMCA izcelsmes sertificēšana
description: Šis līdzeklis ļauj izdrukāt izcelsmes dokumentu sertifikāciju, kā paredzēts Amerikas Savienoto Valstu, Meksikas un Kanādas līgumā (USMCA).
author: Henrikan
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 4d34c1778802baaa0de0506d3dd4bc7efeb13f27
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573061"
---
# <a name="usmca-certification-of-origin"></a>USMCA izcelsmes sertificēšana

[!include [banner](../includes/banner.md)]

Šis līdzeklis ļauj izdrukāt izcelsmes dokumentu sertifikāciju, kā paredzēts Amerikas Savienoto Valstu, Meksikas un Kanādas līgumā (USMCA).

*USMCA izcelsmes dokumenta sertifikācija* ietver minimālos datu elementus, kas nepieciešami deklarēšanai. Dažus datu elementus var iepriekš aizpildīt pirms drukāšanas, bet citiem ir jābūt aizpildītiem manuāli pēc drukāšanas. Lai iegūtu preferenciālu tarifa režīmu, dokuments ir jāaizpilda un tam jābūt importētāja valdījumā laikā, kad tiek veikta deklarācija. Dokumentu var aizpildīt importētājs, eksportētājs vai ražotājs.

Dokumentu var drukāt vienam sūtījumam no saraksta lapas **Visi sūtījumi** vai no lapas **Informācija par sūtījumu**.

Dokuments ir pieejams tikai tad, ja valsts primārajā adresē ir juridiskās personas adrese Amerikas Savienotajās Valstīs.

Atkarībā no dokumenta drukāšanas atlases dokumentu var iepriekš aizpildīt ar datiem no jūsu sistēmas. Drukātajam dokumentam ir iespējams mainīt vai pievienot datus, eksportējot drukāto dokumentu rediģējamā formātā, piemēram, Microsoft Word. Pēc eksportēšanas varat lietot visas nepieciešamās izmaiņas pirms deklarācijas izveides.

## <a name="turn-on-the-usmca-feature"></a>Līdzekļa USMCA ieslēgšana

Lai varētu izmantot USMCA līdzekli, tas vispirms ir jāieslēdz jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Transportēšanas pārvaldība*
- **Līdzekļa nosaukums:** *USMCA izcelsmes dokumenta sertificēšana*

## <a name="document-content"></a>Dokumenta saturs

Izcelsmes dokumenta USMCA sertificēšana ietver tālāk minētos datu elementus.

- Adrešu elementi
- Sertificējošās puses loma
- Viens sūtījums
- Rēķini
- Tukšs periods
- Detalizēta informācija par krājumu
- Sertificētāja paraksts
- Lapu skaits

Plašāku informāciju par katru no šiem elementiem un to, kā tiek atrastas to vērtības, skatiet šīs tēmas pārējās sadaļās.

## <a name="print-a-usmca-certification-of-origin-document"></a>Izcelsmes dokumenta USMCA sertifikācijas izdrukāšana

Lai sūtījumam izdrukātu izcelsmes dokumenta USMC sertifikāciju, rīkojieties šādi:

1. Veiciet vienu no tālāk norādītajām darbībām.
    - Doties uz **Transportēšanas pārvaldība > Sūtījumi > Visi sūtījumi** un atlasiet sūtījumu, kuram vēlaties drukāt dokumentu.
    - Atveriet lapu **Informācija par sūtījumu** sūtījumam, kuram vēlaties izdrukāt dokumentu (ir vairāki veidi, kā šeit nokļūt, tostarp no lapas **Visi sūtījumi**).
1. Darbību rūtī atveriet cilni **Sūtījumi** un grupā **Drukāt** atlasiet **USMCA izcelsmes sertifikāts**.
1. Tiek atvērts dialoglodziņš **Sertifikāts vai izcelsme**. Veiciet iestatījumus, kas aprakstīti turpmākajās apakšsadaļās, un pēc tam atlasiet **Labi**, lai ģenerētu dokumentu.
1. Tiek atvērts dokumenta priekšskatījums. Izmantojiet Darbību rūtī sniegtās komandas, lai izdrukātu vai eksportētu dokumentu pēc nepieciešamības.

### <a name="certifying-party"></a>Sertificētāja puse

Izmantojiet nolaižamo sarakstu **Sertificētāja puse**, lai identificētu puses veidu, kura izdrukā dokumentu. Norādiet, vai sertifikācijas puse ir *Eksportētājs*, *Eksportētājs un ražotājs*, *Ražotājs* vai *Importētājs* ; vai atstājiet to tukšu, ja sertificētāja puse nav neviena no minētā. Atlasītā opcija nosaka, kas tiek izdrukāts dokumenta adreses sadaļās.

Jūsu izvēlētā **Sertificētāja puse** tiks iekļauta izdrukātajā dokumentā.

Dokumentu var izdrukāt gan ienākošajiem, gan izejošajiem sūtījumiem. Atlasiet *Importētājs* kā **Sertificētāja pusi** tikai ienākošajiem sūtījumiem.

Tabulā zemāk ir aprakstīti informācijas veidi, kas ir iekļauti dokumentā, pamatojoties uz jūsu izvēlēto **Sertificētāja pusi**.

| Sertificētāja&nbsp;puse | Apraksts |
|---|---|
| *\[Tukšs\]* | Dokumentam tiek pievienota tālāk minētā informācija.<ul><li>**Informācija par sertificētāju**: izmanto piegādes noliktavas adreses informāciju, ja tāda ir pieejama; pretējā gadījumā tā izmanto piegādes vietas adresi, ja tāda ir pieejama; pretējā gadījumā tā izmanto juridiskās personas (uzņēmuma) adresi, kas atlasīta Supply Chain Management.</li><li>**Informācija par eksportētāju**: tukšs</li><li>**Informācija par ražotāju**: tukšs</li><li>**Informācija par importētāju**: tukšs</li><ul>|
| *Eksportētājs* | Dokumentam tiek pievienota tālāk minētā informācija.<ul><li>**Informācija par sertificētāju**: izmanto piegādes noliktavas adreses informāciju, ja tāda ir pieejama; pretējā gadījumā tā izmanto piegādes vietas adresi, ja tāda ir pieejama; pretējā gadījumā tā izmanto juridiskās personas (uzņēmuma) adresi, kas atlasīta Supply Chain Management.</li><li>**Informācija par eksportētāju**: izmanto juridiskās personas adreses informāciju.</li><li>**Informācija par ražotāju**: tukšs</li><li>**Informācija par importētāju**: izmanto saistītā pārdošanas pasūtījuma rēķina kontu.</li><ul>|
| *Eksportētājs un ražotājs* | Dokumentam tiek pievienota tālāk minētā informācija.<ul><li>**Informācija par sertificētāju**: izmanto piegādes noliktavas adreses informāciju, ja tāda ir pieejama; pretējā gadījumā tā izmanto piegādes vietas adresi, ja tāda ir pieejama; pretējā gadījumā tā izmanto juridiskās personas (uzņēmuma) adresi, kas atlasīta Supply Chain Management.</li><li>**Informācija par eksportētāju**: izmanto juridiskās personas adreses informāciju.</li><li>**Informācija par ražotāju**: izmanto juridiskās personas adreses informāciju.</li><li>**Informācija par importētāju**: izmanto saistītā pārdošanas pasūtījuma rēķina kontu.</li><ul>|
| *Importētājs* | Dokumentam tiek pievienota tālāk minētā informācija.<ul><li>**Informācija par sertificētāju**: izmanto piegādes noliktavas adreses informāciju, ja tāda ir pieejama; pretējā gadījumā tā izmanto piegādes vietas adresi, ja tāda ir pieejama; pretējā gadījumā tā izmanto juridiskās personas (uzņēmuma) adresi, kas atlasīta Supply Chain Management.</li><li>**Informācija par eksportētāju**: tukšs</li><li>**Informācija par ražotāju**: tukšs</li><li>**Informācija par importētāju**: izmanto juridiskās personas adreses informāciju.</li><ul>|
| *Ražotājs* | Dokumentam tiek pievienota tālāk minētā informācija.<ul><li>**Informācija par sertificētāju**: izmanto piegādes noliktavas adreses informāciju, ja tāda ir pieejama; pretējā gadījumā tā izmanto piegādes vietas adresi, ja tāda ir pieejama; pretējā gadījumā tā izmanto juridiskās personas adresi, kas atlasīta Supply Chain Management.</li><li>**Informācija par eksportētāju**: tukšs</li><li>**Informācija par ražotāju**: izmanto juridiskās personas adreses informāciju.</li><li>**Informācija par importētāju**: tukšs</li><ul>|

### <a name="has-various-producers"></a>Ir dažādi ražotāji

Nolaižamais saraksts **Sertificētāja puse** kontrolē tekstu, kas tiks izmantots informācijai par ražotāju dokumentā. Izvēlieties vienu no šīm:

- *Dažādi ražotāji* – izdrukā tekstu "Dažādi" informācijā par ražotāju.
- *Pieejams pēc pieprasījuma* – izdrukā tekstu "Pieejams pēc importētāju iestāžu pieprasījuma" informācijā par ražotāju.

Kad **Sertificētāja puse** ir iestatīta uz *Eksportētājs un ražotājs* vai *Ražotājs*, tad ir noraidīts iestatījums **Ir vairāki ražotāji**, un ražotāja adreses informācija būs tāda pati kā sertificētājam.

### <a name="blanket-period"></a>Tukšs periods

Lietojiet iestatījumus **Virspasūtījuma periods no** un **Virspasūtījuma periods līdz**, lai izveidotu virspasūtījuma periodu, kura laikā dokuments attieksies uz vairākiem identisku preču sūtījumiem, pat ja dokuments ir izdrukāts tikai vienam sūtījumam. Varat iestatīt virspasūtījuma perioda datumus bez ierobežojumiem, un tas tiks pievienots dokumentam. Šos iestatījumus var arī atstāt tukšus vai iestatīt tos pagātnē.

### <a name="is-single-shipment"></a>Ir viens sūtījums

Dialoglodziņā **Izcelsmes sertifikāts** iestatiet **Ir viens sūtījums** uz vienu no tālāk minētā.

- *Jā* - pievieno "Viens sūtījums: Jā" blakus rēķina numuram.
- *Nē* – nekas netiek pievienots.

## <a name="other-information-included-in-the-document"></a>Cita dokumentā iekļautā informācija

Papildus neobligātajiem elementiem, kurus jūs atlasāt, izmantojot dialoglodziņu **Sertifikāts vai izcelsme**, USMC sertifikācijas vai izcelsmes dokumentā tiks iekļauta informācija un pielāgoti lauki, kas apkopoti turpmākajās apakšsadaļās. Daļa no šīs informācijas ir jāievada manuāli pēc dokumenta ģenerēšanas.

### <a name="invoice-number"></a>Rēķina numurs

Ar sūtījumiem saistīto pārdošanas rēķinu ID tiek izdrukāti dokumentā neatkarīgi no virspasūtījuma perioda. Rēķinu numuri tiek izdrukāti neatkarīgi no tā atlases **Ir viens sūtījums**.

### <a name="item-details"></a>Detalizēta informācija par krājumu

Dokumentā ir iekļautas vairākas sadaļas ar detalizētu informāciju par krājumu, kas ir:

- **SKU numurs**: izdrukā izlaistās preces krājuma numuru.

- **Apraksts**: izdrukā izlaistās preces aprakstu vai nosaukumu. Ja pastāv apraksts lietotāja valodā, tas tiek drukāts. Ja šāda apraksta nav, tiek izdrukāts nosaukums lietotāja valodā. Ja šāda nosaukuma nav, tiek izdrukāts krājuma nosaukums.

- **Saskaņotās sistēmas (HS) tarifu klasifikācija**: izdrukā saskaņoto tarifu grafiku, kas saistīts ar preci. Varat iestatīt šos grafikus, pārejot uz **Transportēšanas pārvaldība \> Iestatījumi \> Transportēšanas standarts \> Saskaņoto tarifu grafiki**.

- **Izcelsmes kritērijs:** šajā sadaļā pirmo reizi izlaižot dokumentu, dati ir jāievada manuāli.

- **Izcelsmes valsts:** izdrukā izcelsmes valsti, ko jūs piemērojat, dodoties uz **Informācijas par preci pārvaldība \> Iestatījumi \> Preces atbilstība \> Izcelsmes valsts** (skatīt arī [Izcelsmes valsts](../pim/country-of-origin.md)). Izcelsmes valsts ISO kods tiek izdrukāts, pamatojoties uz adresāta valsti/reģionu sūtījuma piegādes adresē un krājumā. Ja nav iestatīti dati par izcelsmes valsti, šī vērtība tiek atgriezta atpakaļ uz iestatījumu, kas atrodams sadaļā **Izlaistā prece \> Ārējā tirdzniecība \> Izcelsme**. Ja joprojām netiek atrasti izcelsmes valsts dati, pēc dokumenta ģenerēšanas ir manuāli jāievada izcelsmes valsts.

### <a name="certifier-signature-and-date"></a>Sertificētāja paraksts un datums

Tas ir jāievada manuāli pēc dokumenta ģenerēšanas.

### <a name="consists-of-number-of-pages"></a>Sastāv no lappušu skaita

Lietotājam, kas paraksta sertifikāciju, ir manuāli jāievada lappušu skaits (verifikācijai) pēc dokumenta ģenerēšanas.

### <a name="page-numbers"></a>Lappušu numuri

Pašreizējā lappuse un izdrukāto lappušu skaits dokumenta apakšpusē.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]