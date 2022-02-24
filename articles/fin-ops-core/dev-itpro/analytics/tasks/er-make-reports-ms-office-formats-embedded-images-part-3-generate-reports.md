---
title: Pārskatu ģenerēšana Office formātā, kurā ir iegultie attēli
description: Tālāk ir paskaidrots, kā lietotājs ar lomu 'Sistēmas administrators' vai 'Elektronisko atskaišu izstrādātājs' var izveidot elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas, lai veidotu elektroniskos dokumentus ar iegultiem attēliem MS Office formātos (Excel un Word).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78dcdbd83dc717104d437662f7f451c9ecb714cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684383"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a>Pārskatu ģenerēšana Office formātā, kurā ir iegultie attēli

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu 'Sistēmas administrators' vai 'Elektronisko atskaišu izstrādātājs' var izveidot elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas, lai veidotu elektroniskos dokumentus ar iegultiem attēliem MS Office formātos (Excel un Word).

Šajā piemērā jūs izmantosit parauga uzņēmumam 'Litware, Inc.' izveidotās ER konfigurācijas.  Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī "ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (2. daļa: pārskatīt konfigurācijas)". Šīs darbības var veikt uzņēmumā 'USMF'.


## <a name="run-format-with-initial-model-mapping"></a>Formāta palaišana ar sākotnējo modeļa kartējumu
1. Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.
2. Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.
3. Darbību rūtī noklikšķiniet uz Iestatīt.
4. Noklikšķiniet uz Pārbaudīt.
5. Noklikšķiniet uz Drukāt paraugu.
    * Palaidiet formātu testēšanas nolūkā.  
6. Laukā Maksājumu čeka formāts atlasiet Jā.
7. Noklikšķiniet uz Labi.
    * Pārskatiet izveidoto izvadi. Pārskatā ir iekļauts gan uzņēmuma logotips, gan pilnvarotās personas paraksts. Paraksta attēls tiek ņemts no čeka izkārtojuma ieraksta lauka ar datu tipu “Konteiners”, kas ir saistīts ar atlasīto bankas kontu.  
8. Izvērsiet sadaļu Kopijas.
9. Noklikšķiniet uz Rediģēt.
10. Laukā Ūdenszīme ievadiet “Drukāt ūdenszīmi kā Anulēts”.
    * Mainiet ūdenszīmes izkārtojuma iestatījumu, lai parādītu ūdenszīmes tekstu, ģenerējot dokumentu Excel formas elementā.  
11. Noklikšķiniet uz Drukāt paraugu.
12. Noklikšķiniet uz Labi.
    * Pārskatiet izveidoto izvadi. Ūdenszīme izveidotajā pārskatā tiek rādīta atbilstoši atlasītajai opcijai.  
13. Aizvērt lapu.
14. Darbību rūtī noklikšķiniet uz Pārvaldīt maksājumus.
15. Noklikšķiniet uz Čeki.
16. Noklikšķiniet uz Rādīt filtrus.
17. Lietojiet šādus filtrus: laukā “Čeka numurs” ievadiet filtra vērtību “381”,“385”,“389”, izmantojot filtra operatoru “ir viens no”.
18. Sarakstā atzīmējiet visas rindas.
19. Noklikšķiniet uz Drukāt čeka kopiju.
    * Palaidiet formātu, lai atkārtoti drukātu atlasītos čekus.  
    * Pārskatiet izveidoto izvadi. Atlasītie čeki ir izdrukāti atkārtoti. Uzņēmuma logotips un etiķetes netiek drukātas, jo tās jau ir redzamas iepriekš izdrukātajā veidlapā.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Importētā datu modeļa kartējuma modificēšana
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
4. Koka struktūrā atlasiet “Čeku modelis”.
5. Noklikšķiniet uz Veidotājs.
6. Noklikšķiniet uz Kartēšanas modelis datu avotam.
7. Noklikšķiniet uz Veidotājs.
    * Mēs mainīsim datu modeļa paraksta vienuma saistījumu, lai iegūtu paraksta attēlu no faila, kas pievienots čeku izkārtojuma ierakstam, kurš ir saistīts ar atlasīto bankas kontu.  
8. Izslēdziet opciju Rādīt detalizēti.
9. Kokā izvērsiet elementu “izkārtojums”.
10. Kokā izvērsiet 'layout\signature'.
11. Kokā atlasiet 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.
12. Kokā izvērsiet sadaļu “chequesaccount”.
13. Kokā izvērsiet 'chequesaccount\<Relations'.
14. Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout'.
15. Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout\<Relations'.
16. Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.
17. Kokā atlasiet 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.
18. Noklikšķiniet uz Saistīt.
19. Noklikšķiniet uz Saglabāt.
20. Aizvērt lapu.
21. Aizvērt lapu.
22. Aizvērt lapu.
23. Aizvērt lapu.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Formāta palaišana, izmantojot pielāgoto modeļa kartējumu
1. Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Bankas konts vērtības “USMF OPER”.
3. Darbību rūtī noklikšķiniet uz Iestatīt.
4. Noklikšķiniet uz Pārbaudīt.
5. Noklikšķiniet uz Drukāt paraugu.
6. Noklikšķiniet uz Labi.
    * Pārskatiet izveidoto izvadi. Attēls no dokumentu pārvaldības pielikuma tiek izmantots kā pilnvarotas personas paraksts.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>Izmantot MS Word dokumentu kā veidni importētajā formātā
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
4. Koka struktūrā izvērsiet “Čeku modelis”.
5. Kokā atlasiet 'Model for cheques\Cheques printing format'.
6. Noklikšķiniet uz Veidotājs.
7. Noklikšķiniet uz Pielikumi.
8. Noklikšķiniet uz Dzēst.
9. Noklikšķiniet uz Jā.
10. Noklikšķiniet uz Jauns.
11. Noklikšķiniet uz Fails.
    * Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu 'Čeku veidne Word.docx'.  
12. Aizvērt lapu.
13. Ievadiet vai atlasiet kādu vērtību laukā Veidne.
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.
16. Noklikšķiniet uz Rediģēt.
17. Laukā Palaist melnrakstu atlasiet Jā.
18. Aizvērt lapu.
19. Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.
20. Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.
21. Noklikšķiniet uz Pārbaudīt.
22. Noklikšķiniet uz Drukāt paraugu.
23. Noklikšķiniet uz Labi.
    * Pārskatiet izveidoto izvadi. Izvade ir izveidota kā Word dokuments ar iegultiem attēliem, kuros redzams uzņēmuma logotips, pilnvarotas personas paraksts un atlasītais ūdenszīmes teksts.  

