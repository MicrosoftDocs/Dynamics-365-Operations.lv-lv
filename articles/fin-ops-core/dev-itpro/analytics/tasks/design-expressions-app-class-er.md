---
title: ER izteiksmju noformēšana programmas klases metožu izsaukšanai
description: Šajā tēmā sniegta informācija par to, kā atkārtoti izmantot esošo programmas loģiku elektronisko pārskatu veidošanas (ER) konfigurācijās, izsaucot nepieciešamās programmas klašu metodes ER izteiksmēs.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2de6464aaceadd60a82a70f428f42cd4f864eb8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092089"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>ER izteiksmju noformēšana programmas klases metožu izsaukšanai

[!include [banner](../../includes/banner.md)]

Šajos norādījumos sniegta informācija par to, kā atkārtoti izmantot esošo programmas loģiku elektronisko pārskatu veidošanas (ER) konfigurācijās, izsaucot nepieciešamās programmas klašu metodes ER izteiksmēs. Izsaukšanas klašu argumentu vērtības var definēt dinamiski izpildlaikā: piemēram, pamatojoties uz informāciju parsēšanas dokumentā, lai nodrošinātu tās pareizību. Šajā rokasgrāmatā jūs izveidosiet nepieciešamās ER konfigurācijas parauga uzņēmumam “Litware, Inc.”. Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. 

Šīs darbības var veikt, izmantojot jebkuru datu kopu. Ir jāveic arī tālāk norādītā faila lokāla lejupielāde un saglabāšana: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Lai izpildītu tālāk norādītās darbības, vispirms ir jāizpilda darbības, kas aprakstītas procedūrā "ER Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, ka konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".   
    * Jūs veidojat procesu ienākošo bankas izrakstu parsēšanai pieteikumu datu atjaunināšanai. Jūs saņemsit ienākošos bankas izrakstus kā TXT failus, kas satur IBAN kodus. Bankas izrakstu importēšanas procesa ietvaros ir jāpārbauda šo IBAN kodu pareizība, izmantojot loģiku, kas jau ir pieejama.   

## <a name="import-a-new-er-model-configuration"></a>Importēt jaunu ER modeļa konfigurāciju
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet elementu Microsoft nodrošinātājs.  
2. Noklikšķiniet uz Repozitoriji.
3. Noklikšķiniet uz Rādīt filtrus.
4. Pievienojiet filtra lauku 'Veida nosaukums'. Laukā Nosaukums ievadiet vērtību "resursi", atlasiet filtra operatoru "satur" un pēc tam noklikšķiniet uz Lietot.
5. Noklikšķiniet uz Atvērt.
6. Koka struktūrā atlasiet “Maksājuma modelis”.
    * Ja poga Importēt kopsavilkuma cilnē Versijas nav iespējota, ER konfigurācijas 'Maksājuma modelis' 1. versija jau ir importēta. Pārējās šī apakšuzdevuma darbības var izlaist.   
7. Noklikšķiniet uz Importēt.
8. Noklikšķiniet uz Jā.
9. Aizvērt lapu.
10. Aizvērt lapu.

## <a name="add-a-new-er-format-configuration"></a>Jaunas ER formāta konfigurācijas pievienošana
1. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
    * Pievienojiet jaunu ER formātu, lai parsētu ienākošos bankas izrakstus TXT formātā.  
2. Koka struktūrā atlasiet “Maksājuma modelis”.
3. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu dialoglodziņa izvēlni.
4. Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli PaymentModel".
5. Laukā Nosaukums ierakstiet “Bankas izraksta importa formāts (paraugs)”.
    * Bankas izraksta importa formāts (paraugs)  
6. Laukā Atbalsta datu importēšanu atlasiet vērtību Jā.
7. Klikšķiniet Izveidot konfigurāciju.

## <a name="design-the-er-format-configuration---format"></a>Noformēt ER formāta konfigurāciju — formāts
1. Noklikšķiniet uz Veidotājs.
    * Izveidotais formāts pārstāv paredzamo ārējā faila struktūru TXT formātā.  
2. Noklikšķiniet uz Pievienot sakni, lai atvērtu dialoglodziņa izvēlni.
3. Koka struktūrā atlasiet 'Text\Sequence'.
4. Laukā Nosaukums ierakstiet 'Sakne'.
    * Sakne  
5. Laukā Īpašas rakstzīmes atlasiet 'New line - Windows (CR LF)'.
    * Laukā 'Īpašas rakstzīmes' ir atlasīta opcija 'Jauna rinda — Windows (CR LF)'. Pamatojoties uz šo iestatījumu, katra rinda parsēšanas failā tiek uzskatīta par atsevišķu ierakstu.  
6. Noklikšķiniet uz OK.
7. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
8. Koka struktūrā atlasiet 'Text\Sequence'.
9. Laukā Nosaukums ierakstiet “Rindas”.
    * Rindas  
10. Laukā Daudzkārtīgums atlasiet "One many".
    * Laukā 'Daudzkārtīgums' ir atlasīta opcija 'Viens — daudzi'. Pamatojoties uz šo iestatījumu, ir paredzams, ka parsēšanas failā būs norādīta vismaz viena rinda.  
11. Noklikšķiniet uz OK.
12. Kokā atlasiet “Sakne\Rindas”.
13. Noklikšķiniet uz Pievienot secību.
14. Laukā Nosaukums ierakstiet “Lauki”.
    * Lauki  
15. Laukā Daudzkārtīgums atlasiet "Exactly one".
16. Noklikšķiniet uz OK.
17. Kokā atlasiet “Sakne\Rindas\Lauki”.
18. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
19. Kokā atlasiet elementu “Teksts\Virkne”.
20. Laukā Nosaukums ierakstiet "IBAN".
    * IBAN  
21. Noklikšķiniet uz OK.
    * Tas ir konfigurēts, lai katra rinda parsēšanas failā saturētu vienīgo IBAN kodu.  
22. Noklikšķiniet uz Saglabāt.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>Noformēt ER formāta konfigurāciju — kartēšana uz datu modeli
1. Noklikšķiniet uz Kartēt formātu uz modeli.
2. Noklikšķiniet uz Jauns.
3. Laukā Definīcija ierakstiet “BankToCustomerDebitCreditNotificationInitiation”.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges vienumam Definīcija.
5. Laukā Nosaukums ierakstiet “Kartēšana uz datu modeli”.
    * Kartēšana uz datu modeli  
6. Noklikšķiniet uz Saglabāt.
7. Noklikšķiniet uz Veidotājs.
8. Koka struktūrā atlasiet Dynamics 365 for Operations\Klase.
9. Noklikšķiniet uz Pievienot sakni.
    * Pievienojiet jaunu datu avotu, lai izsauktu esošo programmas loģiku IBAN kodu pārbaudei.  
10. Laukā Nosaukums ierakstiet “check_codes”.
    * check_codes  
11. Laukā Klase ierakstiet “ISO7064”.
    * ISO7064  
12. Noklikšķiniet uz OK.
13. Kokā izvērsiet "format".
14. Kokā izvērsiet “formāts\Sakne: Secība(Sakne)”.
15. Kokā atlasiet “formāts\Sakne: Secība(Sakne)\Rindas: Secība 1..* (Rindas)”.
16. Noklikšķiniet uz Saistīt.
17. Kokā izvērsiet “formāts\Sakne: Secība(Sakne)\Rindas: Secība 1..* (Rindas)”.
18. Kokā izvērsiet “formāts\Sakne: Secība(Sakne)\Rindas: Secība 1..* (Rindas)\Lauki: Secība 1..1 (Lauki)”.
19. Kokā atlasiet “formāts\Sakne: Secība(Sakne)\Rindas: Secība 1..* (Rindas)\Lauki: Secība 1..1 (Lauki)\IBAN: String(IBAN)”.
20. Kokā izvērsiet “Maksājumi = format.Root.Rows”.
21. Kokā izvērsiet “Maksājumi = format.Root.Rows\Kreditora konts(CreditorAccount)“.
22. Kokā izvērsiet “Maksājumi = format.Root.Rows\Kreditora konts(CreditorAccount)\Identifikācija“.
23. Kokā atlasiet “Maksājumi = format.Root.Rows\Kreditora konts(CreditorAccount)\Identifikācija\IBAN“.
24. Noklikšķiniet uz Saistīt.
25. Noklikšķiniet uz cilnes Validācijas.
26. Noklikšķiniet uz Jauns.
    * Pievienot jaunu pārbaudes kārtulu, kas parāda kļūdu jebkurai parsēšanas faila rindai, kurā ir nederīgs IBAN kods.  
27. Noklikšķiniet uz Rediģēt nosacījumu.
28. Kokā izvērsiet "check_codes".
29. Kokā atlasiet “check_codes\verifyMOD1271_36”.
30. Noklikšķiniet uz Pievienot datu avotu.
31. Laukā Formula ievadiet “check_codes.verifyMOD1271_36(”.
    * check_codes.verifyMOD1271_36(  
32. Kokā izvērsiet "format".
33. Kokā izvērsiet “formāts\Sakne: Secība(Sakne)”.
34. Kokā izvērsiet “formāts\Sakne: Secība(Sakne)\Rindas: Secība 1..* (Rindas)”.
35. Kokā izvērsiet “formāts\Sakne: Secība(Sakne)\Rindas: Secība 1..* (Rindas)\Lauki: Secība 1..1 (Lauki)”.
36. Kokā atlasiet “formāts\Sakne: Secība(Sakne)\Rindas: Secība 1..* (Rindas)\Lauki: Secība 1..1 (Lauki)\IBAN: String(IBAN)”.
37. Noklikšķiniet uz Pievienot datu avotu.
38. Laukā Formula ievadiet “check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)”.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Noklikšķiniet uz Saglabāt.
40. Aizvērt lapu.
    * Pārbaudes nosacījums ir konfigurēts, lai atgrieztu vērtību FALSE jebkuram nederīgam IBAN kodam, izsaucot programmas klases 'ISO7064' esošo metodi 'verifyMOD1271_36'. Ņemiet vērā, ka IBAN koda vērtība tiek definēta dinamiski izpildlaikā kā izsaukšanas metodes arguments, pamatojoties uz parsēšanas TXT faila saturu.   
41. Noklikšķiniet uz Rediģēt ziņojumu.
42. Laukā Formula ievadiet “CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)”.
    * CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)”.  
43. Noklikšķiniet uz Saglabāt.
44. Aizvērt lapu.
45. Noklikšķiniet uz Saglabāt.
46. Aizvērt lapu.

## <a name="run-the-format-mapping"></a>Formāta kartēšanas palaišana
Testēšanas nolūkos izpildiet formāta kartēšanu, izmantojot lejupielādēto failu SampleIncomingMessage.txt. Ģenerētajā izvadē ir ietverti dati, kuri tiks importēti no atlasītā TXT faila un reālās importēšanas laikā aizpildīti pielāgotajā datu modelī.   
1. Noklikšķiniet uz Palaist.
    * Noklikšķiniet uz Pārlūkot un dodieties uz iepriekš lejupielādēto failu SampleIncomingMessage.txt.  
2. Noklikšķiniet uz OK.
    * Pārskatiet izvadi XML formātā, kas parāda no atlasītā faila importētos un uz datu modeli pārnestos datus. Ņemiet vērā, ka tika apstrādātas tikai 3 importētā TXT faila rindas. IBAN kods 4. rindā, kas nav derīgs, tika izlaists, un informācijas žurnālā ir reģistrēts kļūdas ziņojums.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]