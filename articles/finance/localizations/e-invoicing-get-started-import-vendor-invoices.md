---
title: Elektronisko rēķinu izveides pakalpojuma izmantošana, lai importētu kreditoru rēķinus
description: Šajā rakstā ir sniegta informācija, kā importēt kreditora rēķinus, izmantojot Elektronisko rēķinu izrakstīšanas pakalpojumu.
author: gionoder
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: c98f33345b37a72c4099f01e37c82e27002ac687
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283151"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Elektronisko rēķinu izveides pakalpojuma izmantošana, lai importētu kreditoru rēķinus

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šajā rakstā ir sniegta informācija, kas palīdzēs sākt kreditora rēķinu importēšanu, izmantojot elektronisko rēķinu izrakstīšanas pakalpojumu. Tas jūs vadīs pa konfigurācijas soļiem regulēšanas konfigurācijas pakalpojumos (RCS), Dynamics 365 Finanses un ka jums ir jāievēro, Dynamics 365 Supply Chain Management lai saņemtu elektroniskos kreditoru rēķinus no kreditoriem.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Kreditoru rēķinu importa iestatīšana RCS
Lai iestatītu kreditora rēķina importu RCS, sekojiet šiem soļiem:

1. Skatiet [vispārīgi pieejamo elektronisko rēķinu izrakstīšanas funkciju](e-invoicing-configuration-rcs.md#generally-available-features) sarakstu.
2. Atlasiet un importējiet elektronisko rēķinu izrakstīšanas līdzekli. Papildinformācija: skatiet [Importēt Elektronisko rēķinu izrakstīšanas līdzekli no Microsoft konfigurācijas nodrošinātāja](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Izveidojiet Elektronisko rēķinu izrakstīšanas līdzekli jūsu organizācijā. Papildinformācija: skatiet [Izveidojiet Elektronisko rēķinu izrakstīšanas līdzekli jūsu organizācijas nodrošinātājā](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Konfigurēt e-pasta konta kanālu

Konfigurējiet e-pasta konta kanālu, ja jūs izveidojāt Elektronisko rēķinu izrakstīšanas līdzekli, importē elektroniskos kreditora rēķinus no pievienotajiem failiem, kas tiek saņemti ar e-pastu.

1. RCS atlasiet jūsu izveidoto elektronisko rēķinu izrakstīšanas līdzekli. Pārliecinieties, vai ir atlasīta versija ar statusu **Melnraksts**.
2. Režģa cilnē **Iestatījumi** atlasiet funkcijas iestatījumus un pēc tam atlasiet **Rediģēt**.
3. Cilnes **Datu kanāls** lauka grupā **Parametri**, laukā **Datu kanāls** ievadiet kanāla nosaukumu. Kanāla nosaukumam nevajadzētu pārsniegt 10 rakstzīmes.
4. Laukā **Servera adrese** ievadiet e-pasta konta sniedzēju. Piemēram, **https://outlook.live.com/** servera adrese ir **imap-mail.outlook.com**.
5. Laukā **Servera ports** ievadiet e-pasta konta sniedzēja izmantoto portu. Piemēram, **https://outlook.live.com/** servera ports ir **993**.
6. Laukā **Lietotājvārda slepenie dati** ievadiet atslēgu akreditācijas datu komplekta slepeno datu nosaukumu, kas satur e-pasta lietotāja kontu. Slepenos datus ir jāizveido Azure atslēgu akreditācijas datu komplektā un jāiestata servisa vidē. 
7. Laukā **Lietotājvārda slepenā parole** ievadiet atslēgu akreditācijas datu komplekta e-pasta lietotāja konta paroli.
8. Neobligāti — Ievadiet vērtības laukos **Filtrs no**, **Tēmas filtrs** un **Datuma filtrs**.
9. Ievadiet nosaukumus tām pastkastes mapēm, kurās atradīsies vēstules:

    - Importētas no: **Galvenā mape**
    - Saglabātas pēc sekmīgas apstrādes: **Arhīva mape**
    - Saglabātas pēc sekmīgas apstrādes: **Kļūdu mape** Jums nav jāizveido šīs mapes pastkastē. Mapes tiek izveidotas automātiski pēc pirmās e-rēķina importēšanas un apstrādes. 
   
10. Lauka grupā **Pielikumu filtrs** pievienojiet filtrēšanas informāciju. Tiek apstrādāti tikai tie pielikumi, kuri atbilst definētajam filtram. Piemēram, varat iestatīt "\*.xml" pielikumiem ar xml paplašinājumu. Pielikuma nosaukums tiek izmantots Dynamics 365 Finanses vai iestatīšanas Dynamics 365 Supply Chain Management laikā. 
11. Cilnē **Piemērojamības kārtulas** pārskatiet un atjauniniet kritērijus pēc vajadzības. Laukam **Kanāls** jābūt vienādam ar iepriekš norādīto lauku **Datu kanāls**. Papildinformāciju skatiet sadaļā [Piemērojamības noteikumi](e-invoicing-configuration-rcs.md#applicability-rules).
12. Atlasiet **Saglabāt** un aizveriet lapu.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Konfigurējiet Microsoft SharePoint kanālu

Konfigurējiet Microsoft SharePoint kanālu, ja elektronisko rēķinu izrakstīšanas līdzeklis importē elektroniskos kreditora rēķinus no SharePoint mapēs ievietotajiem failiem.

1. RCS atlasiet jūsu izveidoto elektronisko rēķinu izrakstīšanas līdzekli. Pārliecinieties, vai ir atlasīta **Versija** ar statusu **Melnraksts**.
2. Režģa cilnē **Iestatījumi** atlasiet funkcijas iestatījumus un pēc tam atlasiet **Rediģēt**.
3. Cilnē **Datu kanāls** lauku grupā **Parametri** atlasiet **SharePoint** adrese un ievadiet SharePoint URL.
4. Atlasiet **Servera portu** un ievadiet portu, ko izmanto e-pasta konta nodrošinātājs.
5. Atlasiet **Programmas ID** un ievadiet atslēgas noslēpuma vārdu, kas satur SharePoint lietotāja ID.
6. Atlasiet **Programmas noslēpums** un ievadiet atslēgas noslēpuma vārdu, kas satur SharePoint lietotāja paroli.
7. Atlasiet **Faila filtrs**. Pārskatiet un atjauniniet masku, lai filtrētu failus, kas ietver importējamu elektronisko kreditoru rēķinu.
8. Cilnē **Piemērojamības noteikumi** pārskatiet un atjauniniet kritērijus, ja nepieciešams. Papildinformāciju skatiet sadaļā [Piemērojamības noteikumi](e-invoicing-configuration-rcs.md#applicability-rules).
9. Atlasiet **Saglabāt** un aizveriet lapu

### <a name="deploy-an-electronic-invoicing-feature"></a>Elektronisko rēķinu izrakstīšanas funkcijas izvietošana

Lai izvietotu Elektronisko rēķinu izrakstīšanas līdzekli Pakalpojuma vidē, skatiet sadaļu [Sākt darbu ar Elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-or-supply-chain-management"></a>Piegādātāja rēķina importēšanas iestatīšana Finance vai Supply Chain Management
Lai iestatītu dažādu veidu kreditora rēķinu importu, veiciet tālāk norādītās divas sadaļās norādītās darbības.

### <a name="import-brazilian-nf-e-from-email"></a>Brazīlijas NF-e importēšana no e-pasta

1. Piesakieties Finance vai Supply Chain Management instancēs un pārbaudiet, vai esat pareizajā juridiskajā personā.
2. Dodieties uz **Organizācijas pārvaldība** > **Iestatīšana** > **Elektronisko dokumentu parametri**.
3. Cilnē **Līdzekļi** pārliecinieties, ka ir atlasīts **NF-e Federal - Brazīlijas elektroniskais rēķins**.
4. **Ārējo kanālu** cilnē **Kanālu** lauku grupā atlasiet **Pievienot**.
5. **Kanāla** laukā ievadiet **NFe** (kanāla nosaukums, kas dots datu kanāla konfigurācijā elektronisko rēķinu izrakstīšanas līdzeklim RCS).
6. Ievadiet aprakstu laukā **Apraksts**. Laukā **Uzņēmums** atlasiet juridisko personu.
7. Laukā **Dokumenta konteksts** atlasiet **Debitora rēķina konteksta modelis – Finanšu dokumenta konteksts**.
8. Lauku grupā **Avotu importēšana** atlasiet **Pievienot**.
9. **Nosaukuma** laukā ievadiet **XmlFile** (**Pievienojuma filtra** nosaukums, kas dots datu kanāla konfigurācijā elektronisko rēķinu izrakstīšanas līdzeklim RCS).
10. Laukā **Apraksts** ievadiet aprakstu un **Datu elementa nosaukuma** laukā atlasiet **Saņemtie NF-e XML dokumenti**.
11. **Modeļa kartēšanas** laukā atlasiet **NF-e-pasta importēšana — NF e-pasta importēšana (BR)** un pēc tam atlasiet **Saglabāt**.
12. Cilnes **Elektronisks dokuments** **Elektronisko pārskatu** lauku grupā atlasiet **Pievienot** un laukā **Tabulas nosaukums** atlasiet **Saņemtais NF-e XML dokuments**.
13. Laukā **Dokumenta konteksts** atlasiet **Debitora rēķina konteksts – Uzziņas par finanšu dokumenta kontekstu**.
14. Laukā **Elektronisko dokumentu modeļu kartēšana** atlasiet **Uzziņas par kartēšanu — finanšu dokumentu kartēšana**.
15. Atlasiet **Atbilžu veidi** un pēc tam atlasiet **Jauns**.
16. Laukā **Atbildes tips** ievadiet **Atbilde**. Laukā **Iesniegšanas statuss** atlasiet **Plānots**.
17. Laukā **Modeļa kartēšana** atlasiet **Atbildes ziņojuma importēšanas formāts — Modeļa kartēšana no atbildes ziņojuma**.
18. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

### <a name="import-peppol-electronic-vendor-invoices"></a>PEPPOL importa kreditoru rēķini

1. Pārejiet uz darbvietu **Elektroniskie pārskati** un atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
2. Atlasiet **Klienta rēķina konteksta modelis** un pēc tam atlasiet **Izveidot konfigurāciju**  > **Atvasināt no nosaukuma: Klienta rēķina konteksta modelis, Microsoft**, lai izveidotu atvasinātu konfigurāciju.
3. Versijā **Melnraksts** atlasiet **Noformētājs** un kokā **Datu modelis** atlasiet **Kartēt modeli datu avotos**.
4. Kokā **Definīcijas** atlasiet **DataChannel** un pēc tam atlasiet **Noformētājs**.
5. Kokā **Datu avoti** izvērsiet konteineru **$Context\_Channel**. Laukā **Vērtība** atlasiet **Rediģēt** un ievadiet datu kanāla nosaukumu. Šis ir kanāla nosaukums, kas ir elektronisko rēķinu funkcijas datu kanāla nosaukums RCS. 
7. Atlasiet **Saglabāt** un aizveriet lapu.
8. Aizvērt lapu.
9. Atlasiet atvasināto konfigurāciju, kuru izveidojāt no **Klienta rēķina konteksta modeļa** un kopsavilkuma cilnē **Versijas** atlasiet **Izmaiņu statuss**  > **Izpildīts**.
10. Dodieties uz **Organizācijas administrēšana** > **Iestatījumi** > **Elektronisko dokumentu parametri** un cilnē **Līdzekļi** pārliecinieties, ka ir atlasīti **PEPPOL globālie elektroniskie rēķini**. 
11. **Ārējo kanālu** cilnē **Kanālu** lauku grupā atlasiet **Pievienot**.
12. Laukā **Kanāls** ievadiet datu kanāa nosaukumu un laukā **Apraksts** ievadiet aprakstu.
13. Laukā **Uzņēmums** atlasiet juridisko personu. 
14. Laukā **Dokumenta konteksts** atlasiet jauno atvasināto konfigurāciju no **Klientu rēķina konteksta modeļa**. Kartējuma aprakstam vajadzētu būt **Datu kanāla konteksts**.
15. Lauku grupā **Avotu importēšana** atlasiet **Pievienot**.
16. Laukā **Nosaukums** ievadiet **Pielikumu filtra nosaukumu**, un laukā **Datu entitījas nosaukums** atlasiet **Piegādātāja rēķina galvene**.
17. Laukā **Modeļa kartēšana** atlasiet **Piegādātāja rēķina imports — Importēt piegādātāja rēķinu**.
18. Noklikšķiniet uz **Saglabāt** un tad aizveriet lapu.


## <a name="receive-electronic-invoices"></a>Elektronisko rēķinu saņemšana

Elektroniskās rēķinu izrakstīšanas pakalpojums veic divas darbības, importējot rēķinu no datu kanāliem:

1. Nodrošina piekļuvi pastkastei un e-pasta lasīšanai.
2. Veic e-pastu apstrādi. 
    
Lai izpildītu šīs divas darbības, klientam vajadzētu manuāli izsaukt servisu katrai darbībai. Taču iesakām iestatīt paketi elektronisko dokumentu saņemšanai.

Lai saņemtu elektroniskos rēķinus, veiciet šādus soļus:

1. Dodieties uz **Organizācijas administrēšana** > **Periodiskais** > **Elektroniskie dokumenti** > **Saņemt elektroniskos dokumentus**.
2. Atlasiet **Labi** un pēc tam aizveriet lapu.


## <a name="view-receive-logs-for-electronic-invoices"></a>Skatīt elektronisko rēķinu saņemšanas žurnālus

Lai skatītu elektronisko rēķinu saņemšanas žurnālus, dodieties uz **Organizācijas administrēšana** > **Periodiskais** > **Elektroniskie dokumenti** > **Elektronisko dokumentu saņemšanas žurnāls**.
Ja neredzat sekmīgi apstrādātus rēķinus, noņemiet tabulas filtru.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
