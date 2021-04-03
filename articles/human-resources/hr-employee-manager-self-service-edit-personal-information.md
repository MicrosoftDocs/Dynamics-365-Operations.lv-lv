---
title: Rediģēt personisko informāciju
description: Šajā rakstā ir aprakstīts, kā rediģēt personisko informāciju darbinieku un vadītāju pašapkalpošanās darbvietā.
author: andreabichsel
manager: tfehr
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ed215c4577484269ddf5de20ad93417f8eef38d6
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/05/2021
ms.locfileid: "5502992"
---
# <a name="edit-personal-information"></a>Rediģēt personisko informāciju

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Varat rediģēt savu personisko informāciju Dynamics 365 Human Resources **Darbinieku pašapkalpošanās darbvietā.**

Personiskā informācija, ko var rediģēt, ietver:

- Adreses
- Detalizēta informācija par kontaktpersonu
- Personas kontaktinformācija
- Identifikācijas numuri
- Maksāšanas metode
- Programmā Human Resources izmantotais attēls

>[!NOTE]
>Iespējams, ka nevarēsiet rediģēt noteiktus personiskās informācijas veidus, piemēram, biznesa kontaktinformāciju. Papildinformāciju skatiet sadaļā [Personas informācijas rediģēšanas](hr-employee-self-service-restrict-editing.md)ierobežošana.

Globālajā adrešu grāmatā iestatītie parametri nosaka lomas, kuras var skatīt jūsu personisko informāciju.

1. Programmā Human Resources atlasiet **Darbinieku pašapkalpošanās**.

2. Atlasiet **Rediģēt personas informāciju**.

3. Lai mainītu savu adresi, atlasiet cilni **Adreses**. Jūsu veiktās izmaiņas parādīsies **Personāla vadības** darbvietā, lai brīdinātu personāla vadību.

    - Noklikšķiniet uz **Pievienot**, lai pievienotu jaunu adresi.
    - Lai rediģētu esošu adresi, izvēlieties adresi un pēc tam atlasiet **Rediģēt**.
    - Lai skatītu karti, atlasiet **Karte**.
    - Lai pievienotu vai noņemtu kontaktpersonu, atlasiet **Papildu opcijas** un pēc tam atlasiet **Papildu**. Sadaļā **Kontaktinformācija** atlasiet **Pievienot** vai **Noņemt** un pēc nepieciešamības rediģējiet laukus.
    - Lai iestatītu laika joslu un atrašanās vietu, atlasiet **Papildu opcijas** un pēc tam atlasiet **Papildu**. Elementā **Vispārīgi** pēc nepieciešamības rediģējiet laukus.

4. Lai mainītu savu kontaktinformāciju, izvēlieties cilni **Kontaktinformācija**. Varat nodrošināt dažādus kontaktinformācijas veidus, tostarp tālruņa, e-pasta un sociālo plašsaziņas līdzekļu saites. Varat iestatīt kontaktpersonas datus kā primāros, bet varat iestatīt tikai vienus katra veida datus kā primāros.

    - Lai pievienotu jaunu kontaktinformāciju, atlasiet **Pievienot**. Pēc nepieciešamības rediģējiet laukus.
    - Lai rediģētu esošu kontaktinformāciju, atlasiet vienumu un pēc tam atlasiet **Rediģēt**. Pēc nepieciešamības rediģējiet laukus.
    - Lai iestatītu kontaktpersonas informāciju kā privātu, atlasiet **Papildu** un pēc tam iestatiet pārslēgšanas pogu **Privāts** uz **Jā**. Atlasiet **Labi**.
      >[!NOTE]
      >**Papildus** poga nav pieejama, ja administrators ir iespējojis funkciju **(Priekšskatījums) Ierobežot darbiniekiem pievienot vai rediģēt adresi un kontaktinformāciju atlases nolūkos**. Papildinformāciju skatiet sadaļā [Personas informācijas rediģēšanas](hr-employee-self-service-restrict-editing.md)ierobežošana.
  
5. Lai mainītu savas kontakpersonas, atlasiet **Personīgās kontaktpersonas**. Varat norādīt ārkārtas kontaktpersonas, saņēmējus un pakārtotos. Kontaktpersona var būt persona vai organizācija. Līdzeklis **Atvieglojumu pārvaldība** izmanto personīgo kontaktinformāciju. Papildinformāciju skatiet rakstā [Konfigurēt personīgo kontaktu piemērotības opcijas](hr-benefits-setup-contact-eligibility-options.md).

6. Lai mainītu identifikācijas numurus, piemēram, sociālās apdrošināšanas numuru, atlasiet cilni **Identifikācijas numuri**. Izmaiņas var tikt veiktas apstiprināšanas procesā, ja jūsu organizācija ir iestatījusi apstiprināšanas darbplūsmu.

    - Lai pievienotu identifikācijas numuru, atlasiet **Jauns**. Pēc nepieciešamības aizpildiet laukus un atlasiet **Saglabāt**.
    - Lai rediģētu numuru, atlasiet **Rediģēt**. Pēc nepieciešamības rediģējiet laukus un atlasiet **Saglabāt**.

7. Lai mainītu metodes, ar kurām jums samaksā, atlasiet cilni **Mana maksājuma informācija** . Šī cilne ir pieejama tikai tad, ja maksājuma metodes ir iespējotas veidlapā **Human Resources parametri**. HR var iespējot opcijas **Bankas čeks**, **Skaidrā naudā**, **Čeks**, **Elektronisks maksājums** vai **Cits**. HR var arī deaktivizēt elektronisko maksājumu validāciju (izmanto izmaksai ASV) un bankas kontu un maršrutēšanas numura pārbaudi.

8. Lai mainītu attēlu, kas tiek parādīts Human Resources profilā, atlasiet cilni **Attēls**. Atkarībā no organizācijas iestatījumiem, iespējams, attēli tiks maršrutēti apstiprināšanai.

    - Lai augšupielādētu attēlu, atlasiet **Augšupielādēt jaunu attēlu**.
    - Lai noņemtu attēlu, atlasiet attēlu un pēc tam atlasiet **Noņemt**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]