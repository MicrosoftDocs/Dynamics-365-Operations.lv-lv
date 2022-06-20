---
title: Mazumtirdzniecības kanāla iestatīšana
description: Šajā rakstā ir aprakstīts, kā izveidot jaunu mazumtirdzniecības kanālu sistēmā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eccbbff33ddf967b000940a8ea9910c34232431f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847736"
---
# <a name="set-up-a-retail-channel"></a>Mazumtirdzniecības kanāla iestatīšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot jaunu mazumtirdzniecības kanālu sistēmā Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce atbalsta vairākus mazumtirdzniecības kanālus. Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali). Katram mazumtirdzniecības veikala kanālam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls. Pirms varat izveidot mazumtirdzniecības veikala kanālu, jums tam ir jāiestata visi šie elementi. 

Pirms mazumtirdzniecības kanāla izveidošanas pārliecinieties, ka esat ievērojis [kanāla priekšnosacījumus](channels-prerequisites.md).

## <a name="create-and-configure-a-new-retail-channel"></a>Jauna mazumtirdzniecības kanāla izveide un konfigurācija

1. Navigācijas rūtī atveriet **Moduļi \> Kanāli \> Veikali \> Visi veikali**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.
1. Laukā **Veikala numurs** ievadiet unikālu veikala nosaukumu. Numurs var būt burtciparu ar maksimums 10 rakstzīmēm.
1. Nolaižamajā sarakstā **Juridiskā persona** ievadiet atbilstošo juridisko personu.
1. Nolaižamajā sarakstā **Noliktava** ievadiet atbilstošo noliktavu.
1. Laukā **Veikala laika josla** atlasiet atbilstošo laika joslu.
1. Nolaižamajā sarakstā **PVN grupa** atlasiet atbilstošu veikala PVN grupu.
1. Laukā **Valūta** atlasiet atbilstošo valūtu.
1. Laukā **Debitora adrešu grāmata** norādiet derīgu adrešu grāmatu.
1. Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.
1. Laukā **Funkcionalitātes profils** atlasiet funkcionalitātes profilu, ja piemērojams.
1. Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīta jauna mazumtirdzniecības kanāla izveide.

![Jauns mazumtirdzniecības kanāls.](media/channel-setup-retail-1.png)

Tālāk redzamajā attēlā ir parādīts mazumtirdzniecības kanāla piemērs.

![Mazumtirdzniecības kanāla piemērs.](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Citi iestatījumi

Pastāv vairāki citi neobligāti iestatījumi, ko var iestatīt sadaļās **Izraksts/slēgšana** un **Dažādi** , pamatojoties uz mazumtirdzniecības veikala vajadzībām.

Turklāt skatiet sadaļu [Pārdošanas punkta (POS) ekrāna izkārtojumi](pos-screen-layouts.md), lai iegūtu informāciju par noklusētā ekrāna izkārtojuma iestatīšanu sadaļā **Ekrāna izkārtojums**, un sadaļu [Retail Hardware Station konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md), lai iegūtu informāciju par sadaļu **Aparatūras stacijas**.

Tālāk redzamajā attēlā ir parādīts mazumtirdzniecības kanāla iestatījumu konfigurācijas piemērs.

![Mazumtirdzniecības kanāla konfigurācijas piemērs.](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Papildu kanāla iestatīšana

Ir papildu vienumi, kas ir jāiestata kanālam, ko var atrast darbības rūtī sadaļā **Iestatīt**.

Papildu uzdevumi, kas nepieciešami tiešsaistes kanāla iestatīšanai, ietver maksājuma metožu iestatīšanu, skaidras naudas deklarēšanu, piegādes veidus, ienākumu/izdevumu kontu, sadaļas, izpildes grupas piešķiršanu un seifus.

Tālāk esošajā attēlā ir parādītas dažādas papildu mazumtirdzniecības kanāla iestatīšanas opcijas cilnē **Iestatīšana**.

![Kanāla iestatīšana.](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Iestatīt maksājuma metodes

Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.

1. Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Maksājumu metodes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Navigācijas rūtī atlasiet vēlamo maksājuma metodi.
1. Sadaļā **Vispārīgi** norādiet **Operācijas nosaukumu** un konfigurējiet citus vēlamos iestatījumus.
1. Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.

![Maksājumu metožu piemērs.](media/channel-setup-retail-5.png)

Šajā attēlā parādīts skaidras naudas maksāšanas metodes piemērs un cilnes **Summa** konfigurācija.

![Piemērs maksāšanas metodes iestatīšanai summām.](media/payment-methods-recount.png)

> [!NOTE]
> Cilnes Summa **vērtības** tiek kešotas mazumtirdzniecības serverī un stāsies spēkā tikai pēc sadales grafika darbu palaišanas. Iespējams, būs jārestartē mākoņa mēroga vienība, lai nekavējoties piemērotu šīs vērtības testēšanas laikā.

### <a name="set-up-cash-declaration"></a>Skaidrās naudas deklarācijas iestatīšana

1. Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Skaidras naudas deklarēšana**.
1. Darbības rūtī atlasiet **Jauns** un pēc tam izveidojiet visas **Monētu** un **Banknošu** piemērojamās denominācijas.

Tālāk esošajā attēlā ir parādīts skaidras naudas deklarācijas piemērs.

![Skaidrās naudas deklarācijas iestatīšana.](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Iestatiet piegādes veidus

Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas darbības rūtī.  

Lai mainītu vai pievienotu piegādes veidu, rīkojieties, kā norādīts tālāk.

1. Navigācijas rūtī atveriet **Moduļi \> krājumu pārvaldība \> Piegādes režīmi**.
1. Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.
1. Sadaļā **Mazumtirdzniecības kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu. Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.

Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.

![Iestatiet piegādes veidus.](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Ienākumu/izdevumu konta iestatīšana

Lai iestatītu ienākumu/izdevumu kontu, veiciet tālāk norādītās darbības.

1. Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **ienākumu/izdevumu konts**.
1. Darbību rūtī atlasiet **Jauns**.
1. Sadaļa **nosaukums** ievadiet nosaukumu.
1. Sadaļā **Saīsinātais nosaukums** ievadiet saīsināto nosaukumu.
1. Sadaļā **Konta veids** ievadiet konta veidu.
1. Ievadiet tekstu sadaļās **1. ziņojuma rinda**, **2. ziņojuma rinda**, **1. kvīts teksts** un **2. kvīts teksts**, kā tas ir nepieciešams.
1. Sadaļā **Grāmatošana** ievadiet grāmatošanas informāciju.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk esošajā attēlā parādīts ieņēmumu/izdevumu konta piemērs.

![Ienākumu/izdevumu kontu iestatīšana.](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Sadaļu iestatīšana

Lai iestatītu sadaļas, rīkojieties, kā norādīts tālāk.

1. Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam noklikšķiniet uz **Sadaļas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Sadaļā **Sadaļas numurs** ievadiet sadaļas numuru.
1. Sadaļā **Apraksts** ievadiet aprakstu.
1. Sadaļā **Sadaļas izmērs** ievadiet sadaļas izmēru.
1. Konfigurējiet papildu iestatījumus sadaļām **Vispārīgi** un **Pārdošanas statistika**, kā tas ir nepieciešams.
1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="set-up-a-fulfillment-group-assignment"></a>Izpildes grupas piešķires iestatīšana

Lai iestatītu izpildes grupas piešķiri, veiciet tālāk norādītās darbības.

1. Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Izpilde/grupas piešķire**.
1. Darbību rūtī atlasiet **Jauns**.
1. Nolaižamajā sarakstā **Izpildes grupa** atlasiet izpildes grupu.
1. Nolaižamajā sarakstā **Apraksts** ievadiet aprakstu.
1. Darbību rūtī atlasiet **Saglabāt**

Tālāk redzamajā attēlā parādīts izpildes grupas piešķires piemērs.

![Izpildes grupas piešķires iestatīšana.](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Seifu iestatīšana

Lai iestatītu seifus, rīkojieties, kā norādīts tālāk.

1. Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam noklikšķiniet uz **Seifi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Ievadiet seifa nosaukumu.
1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="ensure-unique-transaction-ids"></a>Nodrošināt unikālus transakciju ID

Attiecībā uz Commerce versiju 10.0.18 pārdošanas punktam (POS) ģenerētie transakciju ID ir secīgi un ietver šādas daļas:

- Fiksēta daļa, kas ir veikala ID un termināļa ID konkatenācija. 
- Secīga daļa, kas ir numuru sērija. 

It īpaši formāts ir *{store}-{terminal}-{numbersequence}*. 

Tā kā transakciju ID var ģenerēt bezsaistes un tiešsaistes režīmā, ir gadījumi, kad tiek ģenerēti dublēti transakciju ID. Lai noņemtu transakciju ID dublikātus, ir nepieciešama manuāla datu labošana. 

Ar Commerce versiju 10.0.19 transakciju ID formāts ir atjaunināts, lai noņemtu secīgu daļu, un tā vietā tiek izmantots 13 ciparu numurs, kas ģenerēts, aprēķinot laiku milisekundēs kopš 1970. gada. Ar šo izmaiņu jaunais transakciju ID formāts ir *{store}-{terminal}-{millisecondsSince1970}*. Šis atjauninājums padara transakciju ID nesecīgo un nodrošina, ka transakciju ID vienmēr ir unikāli. 

> [!NOTE]
> Transakciju ID ir paredzēti tikai iekšējai sistēmai, tāpēc tiem nav jābūt secīgiem. Tomēr daudzas valstis pieprasa, lai saņemšanas ID būtu secīgi.

Jauno transakciju ID formāta līdzekli var iespējot no darbvietas **Līdzekļu pārvaldība**. 

Lai aktivizētu jaunu transakciju ID izmantošanu, rīkojieties šādi:

1. Programmā Commerce Headquarters dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
1. Filtrs modulim "mazumtirdzniecība un komercija".
1. Meklējiet līdzekļa nosaukumu **Aktivizēt jaunu transakciju ID, lai izvairītos no dublētiem transakciju ID**.
1. Atlasiet līdzekli un pēc tam labajā rūtī atlasiet **Iespējot tūlīt**.  
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Palaidiet darbus **1070 kanāla konfigurācija** un **1170 POS uzdevumu ierakstītājs**, lai sinhronizētu iespējoto līdzekli ar veikaliem.
1. Lai lietotu jauno transakciju ID formātu, kad uz veikaliem ir nosūtītas izmaiņas, POS termināļi ir jāaizver un atkārtoti jāatver. 

> [!NOTE]
> Kad jaunais transakciju ID formāta līdzeklis ir aktivizēts, šo līdzekli nevarēs deaktivizēt. Ja tas ir jāatspējo, lūdzu, sazinieties ar Commerce Support.

## <a name="additional-resources"></a>Papildu resursi

[Kanālu apskats](channels-overview.md)

[Kanāla iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Tiešsaistes veikala iestatīšana](channel-setup-online.md)

[Zvanu centra kanāla iestatīšana](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
