---
title: Uzturēšanas cikls
description: Šajā tēmā ir uzturēšanas cikli programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 63cb2614b2037fac1129c7d2f82a26dac41a3490
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889965"
---
# <a name="maintenance-rounds"></a>Uzturēšanas cikls

[!include [banner](../../includes/banner.md)]

 

Programmā **Asset Management** jūs varat izveidot uzturēšanas ciklus dažādiem līdzekļiem, kuriem jums ir regulāros intervālos jāveic līdzīgs uzdevums. Piemēram, ieeļļošanas darbus vai drošības pārbaudes darbus, kuri ir jāveic vairākām iekārtām vienādos intervālos. Pirmā darbībā ir uzturēšanas cikla izveide, ieskaitot līdzekļus, kuriem ir nepieciešams viena un tāda paša veida uzturēšanas darbs. Pēc tam jūs ieplānojat uzturēšanas ciklus. Kad esat aizpildījis uzturēšanas ciklu grafiku, jūs varat redzēt visus darba ierakstus, kas saistīti ar raundu sadaļās **Visi uzturēšanas grafiki** un **Atvērt uzturēšanas saraksta rindas**.

>[!NOTE]
>Uzturēšanas ciklus var arī uzstādīt funkcionālajam novietojumam, kurš ir jāpabeidz līdzekļos, kuri instalēti funkcionālajā novietojumā ciklā bāzēta darba pasūtījuma izveidošanas laikā. Skatiet [Izveidot funkcionālo novietojumu](../functional-locations/create-functional-locations.md), lai iegūtu vairāk informācijas par uzturēšanas ciklu uzstādīšanu funkcionālajā novietojumā.

## <a name="set-up-a-maintenance-round"></a>Uzturēšanas cikla uzstādīšana

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādīšana** > **Preventīvā uzturēšana** > **Uzturēšanas cikli**.

2. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu uzturēšanas ciklu.

3. Laukā **Uzturēšanas cikls** ievadiet ID un laukā **Nosaukums** ievadiet uzturēšanas cikla nosaukumu.

4. Laukā **Sākuma datums** atlasiet cikla sākuma datumu.

5. Laukos **Pabeigt dienu laikā** un **Pabeigt stundu laikā** jūs varat ievadīt sagaidāmo beigu datumu dienās vai stundās. Paredzamais beigu datums tiek aprēķināts relatīvi iepretim sākuma datumam, kurš tiek aprēķināts uzturēšanas grafika rindu izveides laikā. Piemēram, jūs varat ievadīt "7" laukā **Pabeigt dienu laikā**, lai norādītu, ka attiecīgo darbu vajadzētu pabeigt nedēļas laikā kopš sākuma datuma.

6. Pārslēgšanas pogā **Automātiskā izveide** atlasiet "Jā", ja darba pasūtījumus vajadzētu automātiski izveidot no uzturēšanas grafika līnijām, kuras ir izveidotas no šī uzturēšanas cikla.

7. Laukā **Darba pasūtījuma tips** atlasiet darba pasūtījuma tipu, kuru jāizmanto darba pasūtījumiem, kuri izveidoti no šī uzturēšanas cikla.

8. Laukā **Servisa līmenis** atlasiet darba pasūtījuma servisa līmeni, kuru jāizmanto darba pasūtījumiem, kuri izveidoti no šī uzturēšanas cikla.

9. Kopsavilkuma cilnē **Līdzekļu rindas** noklikšķiniet **Pievienot**, lai uzturēšanas ciklam pievienotu līdzekli.

10. Rindas numurs tiek automātiski ievadīts laukā **Rindas numurs**, lai norādītu uzturēšanas cikla līdzekļu secību.

11. Laukā **Līdzeklis** atlasiet līdzekli.

12. Laukā **Uzturēšanas darba tips** atlasiet līdzekļa uzturēšanas darba tipu.

13. Ja nepieciešams, atlasiet **Uzturēšanas darba tipa variantu** un **Amatu**, kas saistīts ar uzturēšanas darba tipu.

14. Laukā **Perioda tips** atlasiet atkārtošanos (dienu, nedēļu u.c.).

15. Laukā **Perioda biežums** ievadiet uzturēšanas cikla atkārtošanos skaitu. Piemērs: Ja jūs esat laukā **Perioda tips** atlasījuši "Diena" un jūs ievadāt šajā laukā ciparu "7", jaunas uzturēšanas cikla rindas tiek izveidotas preventīvas uzturēšanas plānošanas laikā reizi nedēļā.

16. Laukā **Sākuma datums** atlasiet sākuma datumu līdzeklim, kuru iekļausit uzturēšanas ciklā. Šis datums var atšķirties no sākuma datuma, kas ir uzstādīts uzturēšanas ciklā.

17. Lai uzturēšanas ciklam pievienotu vairāk līdzekļu, atkārtojiet 9. līdz 16. darbību.

18. Kopsavilkuma cilnē **Funkcionālā novietojuma rindas** noklikšķiniet **Pievienot**, lai uzturēšanas ciklam pievienotu funkcionālo novietojumu. Augstāk skatiet attiecīgo lauku aprakstu. Ir pieejami tie paši lauki, kuri līdzekļa rindas izveidošanai, taču, ja nepieciešams, jūs varat arī funkcionālajam novietojumam atlasīt **Ražotāju** un **Modeli**. Ja jūs rindā atlasāt vienīgi funkcionālo novietojumu, taču neatlasāt neko opcijās **Līdzekļa tips**, **Ražotājs**, **Modelis**, **Uzturēšanas darba tips**, **Uzturēšanas darba tipa variants** un **Amats**, visi līdzekļi, kas ir saistīti ar šo funkcionālo novietojumu uzturēšanas plānošanas laikā tiks iekļauti uzturēšanas ciklā.

19. Kopsavilkuma cilnē **Kopas** noklikšķiniet uz **Pievienot**, lai atlasītu darba pasūtījumu kopu, kuru ietvert uzturēšanas ciklā. Vienam uzturēšanas ciklam var pievienot vairākas darba pasūtījumu kopas.

20. Saglabājiet savu uzstādījumu.

>[!NOTE]
>Lauki **Līdzekļi** un **Rindas**, kas atrodas ātrās cilnes **Galvene** grupā **Detalizēta informācija** uzrāda kopējo līdzekļu un rindu skaitu, kuras ir saistītas ar atlasīto uzturēšanas ciklu.

Nākamajā ilustrācijā ir redzams piemērs uzturēšanas ciklam, kurā ietilpst trīs līdzekļi.

![1. attēls](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Plānot uzturēšanas ciklus

Kad esat uzstādījis uzturēšanas ciklu, jūs palaižat grafika darbu, lai ieplānotu visus darbus, kas ir saistīti ar uzturēšanas ciklu.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Periodiski** > **Preventīvā uzturēšana** > **Ieplānot uzturēšanas ciklus** vai **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas grafiks** > **Visas uzturēšanas grafiks** vai **Atvērt uzturēšanas grafika rindas** vai **Atvērt uzturēšanas grafiku kopas** > atlasiet uzturēšanas grafika rindu sarakstā > pogas **Uzturēšanas cikli**.

2. Laukā **Periods** atlasiet perioda tipu, kuru izmantot plānošanas darbam.

3. Laukā **Perioda biežums** ievadiet periodu skaitu, kurus iekļaut plānošanas darbā. Plānošanas sākums ir esošais datums.

4. Pārslēgšanas pogā **Automātiskā izveide** atlasiet "Jā", ja darba pasūtījumu vajadzētu automātiski izveidot no uzturēšanas grafika līnijām, kuras ir izveidotas no šī uzturēšanas cikla.

>[!NOTE]
>Ja šī pārslēgšanas poga ir iestatīta uz "Jā" un pārslēgšanas poga **Automātiskā izveide** arī ir iestatīta uz "Jā" uzturēšanas ciklā veidlapā **Uzturēšanas cikli**, darba pasūtījumi tiek izveidoti, pamatojoties uz uzturēšanas cikla rindām, un tiek izveidotas arī uzturēšanas grafika rindas ar statusu "Darba pasūtījums izveidots". Ja tikai viena pārslēgšanas poga **Automātiskā izveide** arī ir iestatīta uz "Jā" šajā nolaižamajā sarakstā vai veidlapā **Uzturēšanas cikli**, tiek izveidotas uzturēšanas grafika rindas ar statusu "Izveidota". Tāda gadījumā darba pasūtījumi netiek izveidoti.

5. Nepieciešamības gadījumā jūs varat atlasīt konkrētus ciklus vai citu plānota darba sākuma datumu. Noklikšķiniet uz **Filtrēt** un pievienojiet iekļaujamos ciklus.

6. Noklikšķiniet uz **Labi**.

7. Tagad jūs varat redzēt uzturēšanas ciklu darbus opcijā **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas grafiks** > **Visi uzturēšanas grafiki** vai **Atvērt uzturēšanas grafika rindas**. Ja ieplānotie cikli ir saistīti ar darba pasūtījumu kopu, jūs arī redzēsit uzturēšanas saraksta rindas opcijā **Atvērt uzturēšanas grafika kopas**. Uzturēšanas grafika rindām, kuras izveidotas no cikla, ir atsauces tips "Uzturēšanas cikli".

Divās nākamajās ilustrācijās ir parādīts darba grafiks dialoglodziņā **Plānot uzturēšanas ciklus** un uzturēšanas grafika rindas, kas izveidotas **Visos uzturēšanas grafikos**, pamatojoties uz šo plānoto darbu.

![2. attēls](media/14-preventive-maintenance.png)

![3. attēls](media/15-preventive-maintenance.png)

- Kad darba pasūtījums tiek manuāli izveidots līdzekļiem, uz kuriem attiecas piegādātāja garantija, tiek parādīts dialoglodziņš, lai informētu lietotāju par garantiju. Pēc tam darba pasūtījuma izveidi var atcelt. Garantijas saistības pārbaude tiek izlaista tiem darba pasūtījumiem, kuri ir izveidoti automātiski.  
- Ātrajā cilnē **Palaist fonā** jūs uzstādīt pakešuzdevumu, lai ieplānotu ciklus regulāros intervālos.  
- Ja cikls ir ietvers vairākās darba pasūtījumu kopās (skatīt [Darba pasūtījumu kopas](../work-orders/work-order-pools.md)), katrai kopai tiek uzrādīts viens ieraksts opcijā **Atvērt uzturēšanas grafiku kopas**. Tas tiek darīts, lai optimizētu filtrēšanas opcijas darba pasūtījumu kopām.

