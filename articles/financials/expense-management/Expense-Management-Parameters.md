---
title: "Izmaksu pārvaldības parametri"
description: "Tālāk norādītie parametri kontrolē darbvietas Izdevumu pārvaldība darbību."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 92a52646063c145d733b9d2960253004e8eab80a
ms.openlocfilehash: 2b3a384a3b9be686b10ce1f181664b0b9bbe9969
ms.contentlocale: lv-lv
ms.lasthandoff: 03/05/2018

---

# <a name="expense-management-parameters"></a>Izmaksu pārvaldības parametri

[!include[banner](../includes/banner.md)]

-----------------------------

Šie parametri kontrolē vispārīgo darbvietas Izdevumu pārvaldība darbību.

### <a name="general"></a>Vispārējs

| **Lauks**                                                | **Apraksts**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Nobraukuma standarta norma**                             | Ievadiet atmaksāšanas likmi nobraukuma izdevumiem. Šī likme tiks reizināta ar izdevumos ievadīto nobraukuma vērtību, lai aprēķinātu par brauciena izdevumiem atmaksāto summu.                       |
|**Personīgos izdevumus apmaksā**                             | Atlasiet, kurš ir atbildīgs par jebkuru to kredītkartes transakciju summu apmaksu, kas kategorizētas kā personīgas.                                                                                                     |
|**Rādīt visu izdevumu pārskatu par atgriešanu**               | Atlasiet šo opciju, lai rādītu visus izdevumu pārskata izdevumus, kad skatāt detalizētu informāciju par sākotnējo dokumentu konkrētam dokumentam, kas tika ģenerēts, grāmatojot izdevumu pārskatu.              |
|**Iepriekšēja komandējuma atļauja ir obligāta**                 | Atlasiet šo opciju, lai noteiktu, ka darbiniekam pirms izdevumu pārskata iesniegšanas ir jāiesniedz un jāsaņem apstiprinājums komandējuma pieprasījumam.                                                                    |
|**Pirms grāmatošanas ļaut sadales rediģēšanu**            | Atlasiet, vai izdevumu pārskata sadales var rediģēt pirms grāmatošanas.                                                                                                                 |
|**Novērtēt izmaksu pārvaldības politikas**                     | Atlasiet, kad izdevumi tiek novērtēti, lai noteiktu, vai izdevumu politika ir pārkāpta. Izdevumus var pārbaudīt attiecībā uz pārkāpumiem, kad izdevumu ieraksts ir ievadīts un saglabāts vai izdevumi ir iesniegti apstiprināšanai. Nepieciešamie ierobežojuma nosacījumi kvītīm tiks pārbaudīti, saglabājot izdevumu rindu.                   |
|**Atļaut starpuzņēmumu izdevumu rindas**                         | Atlasiet, vai atļaut izdevumu ierakstus citām juridiskajām personām izdevumu pārskatā.                                                                                                          |
|**Atļaut rediģēt maiņas kursu kredītkartes izdevumiem** | Atlasiet šo opciju, lai ļautu lietotājam rediģēt importēto kredītkartes izdevumu maiņas kursu.                                                                        |
|**Vairāklīmeņu hierarhijas lauki, kas jāparāda**                  | Atlasiet, kurus apstiprinātāja laukus rādīt, kad izdevumu pārskata darbplūsmas piešķires tips ir iestatīts kā hierarhija un hierarhijas atlase ir iestatīta izmantot izdevumu vairāklīmeņu apstiprināšanas hierarhiju. Ja darbplūsmai tiek izmantota vairāklīmeņu apstiprināšanas hierarhija, atlasītie lauki tiks parādīti un būs rediģējami izdevumu pārskatā. |
|**Ievadīt darbinieka kredītkartes numuru (2017. gada jūlija atjauninājums)**     | Atlasiet, vai darbiniekam lapas **Kredītkartes** laukā **Kartes ID** var ievadīt un saglabāt 15 vai 16 rakstzīmju numuru.                                                                          |

### <a name="financial"></a>Finanšu

| **Lauks**                                                            | **Apraksts**     |
|----------------------------------------------------------------------|------------------------------------|
|**Virsgrāmatas ikdienas žurnāla nosaukums**                                         | Atlasiet tā virsgrāmatas žurnāla nosaukumu, kurā ir grāmatoti apstiprinātie izdevumu pārskati.            |
|**Iespējot nodokļu atgūšanu no izdevumiem**                                  | Atlasiet šo opciju, lai iespējotu izdevumu nodokļu atgūšanu atbilstošajiem izdevumiem. Šo opciju nevar iespējot, ja ir iespējoti ASV PVN un importa nodokļa nosacījumi.      |
|**Skaidras naudas avansus grāmatot nekavējoties**                                     | Atlasiet šo opciju, lai grāmatotu apstiprināto skaidras naudas avansu, kad ir pabeigts apmaksas un pārsūtīšanas process. Ja šī opcija nav atlasīta, apmaksas un pārsūtīšanas process ģenerēs neiegrāmatotu virsgrāmatas žurnālu. |
|**Labot uzskaites datumu grāmatošanas laikā**                             | Atlasiet šo opciju, lai atjauninātu uzskaites datumu, grāmatojot izdevumus, ja pašreizējais periods ir aizturēts vai slēgts. Uzskaites datums tiks iestatīts uz nākamo atvērto periodu.   |
|**Atļaut transakciju grupēšanu, ņemot vērā maksāšanas metodē norādīto korespondējošo kontu**      | Atlasiet šo opciju, lai apkopotu izdevumu pārskata izdevumu transakcijas, pamatojoties uz korespondējošo kontu, kas norādīts izdevumu maksāšanas metodē.   
|**Iekļautie nodokļi**                                                   | Atlasiet šo opciju, lai pēc noklusējuma izdevumu summā iekļautu PVN.             |
|**Noņemt apgrūtinājumus, slēdzot komandējuma pieprasījumus**            | Atlasiet šo opciju, lai noņemtu apgrūtinātos līdzekļus, kad tiek slēgts apstiprinātais komandējuma pieprasījums.                                                                                   |
|**Atļaut iesniegt komandējuma pieprasījumu ar budžeta pārtēriņu attiecībā pret budžeta reģistru un projekta budžetu** | Atlasiet šo opciju, lai ļautu darbiniekiem iesniegt apstiprināšanai komandējumu pieprasījumus, kas pārsniedz budžeta reģistrā iestatīto atļauto budžetu vai projektam atļauto budžetu.            |
|**Atļaut iesniegt izdevumu pārskatu ar budžeta pārtēriņu attiecībā pret budžeta reģistru un projekta budžetu**    | Atlasiet šo opciju, lai ļautu darbiniekiem iesniegt apstiprināšanai izdevumu pārskatus, kas pārsniedz budžeta reģistrā iestatīto atļauto budžetu vai projektam atļauto budžetu.                |
|**Atļaut apstiprināt izdevumu pārskatu ar budžeta pārtēriņu tikai budžeta reģistram**                | Atlasiet šo opciju, lai apstiprinātājiem ļautu apstiprināt izdevumu pārskatus, kas pārsniedz budžeta reģistrā iestatīto atļauto budžetu.                                                                       |

### <a name="per-diem"></a>Dienasnauda

| **Lauks**                             | **Apraksts**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Stundu minimums dienasnaudai**           | Ievadiet noklusējuma minimālo stundu skaitu, kas darbiniekam ir jānostrādā vienā dienā, lai viņš būtu tiesīgs saņemt dienasnaudu par izdevumiem, kas saistīti ar komandējumu.  Šī vērtība kā noklusējuma vērtība tiek izmantota tikai laukam Stundu minimums dienasnaudas likmju pakāpēs.                                                                                      |
|**Maltītes atlaides procenti**                          | Ievadiet maltītēm noklusējuma procentus no dienasnaudas, kas tiek izmantoti ar komandējumu saistīto izdevumu pirmajā un pēdējā dienā, ja lauks **Aprēķināt ēdināšanas izdevumu samazināšanu par** ir iestatīts uz **Maltītes veids dienā** vai **Maltīšu skaits dienā**. Darba diena pirmajā un pēdējā dienā var būt īsāka par standarta darba dienu. Tāpēc dienasnaudas summa šajās dienās var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz 0, pirmās un pēdējās dienas atlaide būs 0,00. |
|**Viesnīcas atlaides procenti**                        | Ievadiet viesnīcām noklusējuma procentus no dienasnaudas, kas tiek izmantoti ar komandējumu saistīto izdevumu pirmajā un pēdējā dienā. Darba diena pirmajā un pēdējā dienā var būt īsāka par standarta darba dienu. Tāpēc dienasnaudas summa šajās dienās var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz 0, pirmās un pēdējās dienas atlaide būs 0,00.                                              |
|**Citi atlaides procenti**                        | Ievadiet dažādiem izdevumiem noklusējuma procentus no dienasnaudas, kas tiek izmantoti ar komandējumu saistīto izdevumu pirmajā un pēdējā dienā. Darba diena pirmajā un pēdējā dienā var būt īsāka par standarta darba dienu. Tāpēc dienasnaudas summa šajās dienās var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz 0, pirmās un pēdējās dienas atlaide būs 0,00.                                                                                                     |
|**Procentuālais samazinājums brokastīm** | Ievadiet summu, par kādu dienasnauda tiek samazināta brokastīm. Piemēram, ja darbinieks saņem bezmaksas brokastis, varat izvēlēties samazināt dienasnaudas summu par 10 procentiem.                               |
|**Procentuālais samazinājums pusdienām**    | Ievadiet summu, par kādu dienasnauda tiek samazināta pusdienām. Piemēram, ja darbinieks saņem bezmaksas pusdienas, varat izvēlēties samazināt dienasnaudas summu par 15 procentiem.                                       |
|**Procentuālais samazinājums vakariņām**   | Ievadiet summu, par kādu dienasnauda tiek samazināta vakariņām. Piemēram, ja darbinieks saņem bezmaksas vakariņas, varat izvēlēties samazināt dienasnaudas summu par 25 procentiem.                                     |
|**Aprēķināt ēdināšanas izdevumu samazināšanu par**         | Atlasiet, kā sistēmai jāaprēķina dienasnaudas ēdināšanas izdevumu samazinājums, atlasot, vai samazinājums ir balstīts uz maltītes veidu komandējumā vai dienā vai arī samazinājuma pamatā ir dienā atļauto maltīšu skaits.|
|**Dienasnaudas noapaļošana**                  | Atlasiet noapaļošanas veidu, kas tiek izmantots dienasnaudas izmaksām. Atlasot parasto noapaļošanu, visi dienasnaudas izdevumi, kuru summa ir 0,50, tiek noapaļoti līdz 1,00 un visi dienasnaudas izdevumi, kuru summa mazāka par 0,50, tiek noapaļoti uz 0,00.                                                                                              |
|**Dienasnaudas aprēķins balstīts uz**         | Atlasiet, vai dienasnaudas summas pamatā ir kalendārā diena vai 24 stundu periods.       |

### <a name="fax-cover-pages"></a>Faksa titullapas

| **Lauks**                      | **Apraksts**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instrukcijas**                   | Ievadiet instrukcijas, kuras darbiniekiem jāievēro, veidojot titullapu faksam, kas tiek izmantots, lai sūtītu ar izdevumu pārskatu saistītās kvītis. Noklikšķiniet uz pogas **Tulkojumi**, lai ievadītu valodai specifisku tekstu, kas tiks parādīts atbilstoši lietotāja valodai. |
|**Lietotāja ID (svītrkoda informācija)** | Atlasiet šo opciju, lai saglabātu darbinieka unikālo identifikatoru svītrkodā, kas tiek lietots faksa titullapā.                 |
|**Svītrkods**;                      | Atlasiet svītrkodu, kas tiek lietots faksa titullapā. Izmaksu pārvaldībai tiek atbalstīti svītrkodi 39 un 128.               |

### <a name="anti-corruption"></a>Korupcijas novēršana

| **Lauks**                             | **Apraksts**      |
|---------------------------------------|------------------------------------------------------------------------|
|**Rādīt korupcijas novēršanas pārbaudi**   | Atlasiet šo opciju, lai rādītu korupcijas novēršanas tekstu, veidojot jaunu izdevumu pārskatu. Pēc tam var iespējot noteiktas izdevumu kategorijas, kas prasīs izdevumu pārskatā atlasīt korupcijas novēršanas pārbaudi. Piemēram, dāvanu kategorija, kas saistīta ar valsts amatpersonas izdevumiem, var prasīt darbiniekam apstiprināt, ka izdevumi atbilst uzņēmuma politikai attiecībā uz valsts amatpersonām. |
|**Ziņojums iesniedzējam saistībā ar korupcijas novēršanu** | Ievadiet tekstu, kas tiks parādīts darbiniekam, kad viņš veidos jaunu izdevumu pārskatu. Noklikšķiniet uz pogas **Tulkojumi**, lai ievadītu valodai specifisku tekstu, kas tiks parādīts atbilstoši lietotāja valodai.         |
|**Ziņojums apstiprinātājam saistībā ar korupcijas novēršanu**  | Ievadiet tekstu, kas tiks parādīts apstiprinātājam, kad viņš veidos jaunu izdevumu pārskatu. Noklikšķiniet uz pogas **Tulkojumi**, lai ievadītu valodai specifisku tekstu, kas tiks parādīts atbilstoši lietotāja valodai.        |

