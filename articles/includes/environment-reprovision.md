Kopējot datu bāzi starp vidēm, jāpalaiž vides atkārtotas nodrošināšanas rīks, lai nokopētā datu bāze būtu pilnībā funkcionāla un visi Commerce komponenti būtu atjaunināti.

> [!IMPORTANT]
> Ieteicams palaist šo procedūru neatkarīgi no tā, vai izmantojat Commerce komponentus, jo Commerce funkcionalitāte ir iekļauta visās vidēs. 

Pirms turpināt, jums jāpārliecinās, vai ir izpildīti tālāk norādītie priekšnosacījumi.
1. Ja veicat jaunināšanu uz 2017. gada jūlija laidienu (zināms arī kā 7.2) 7.2.11792.56024, pirms datu jaunināšanas mērķa vidē izmantojiet tajā tālāk norādītos programmas X++ labojumfailus. Tie novērsīs dažādas kļūdas, kas rodas datu jaunināšanas laikā.

    - KB 4036156 — Retail papildversijas jauninājums — "Varianta numuru sērija nav iestatīta". Šajā labošanas pakotnē ir iekļautas arī versijas KB 4035399 un KB 4035751. Ņemiet vērā, ka šīs pakotnes izmantošanai jums ir nepieciešams vismaz atjauninājums Platform Update 9. Ja neesat pārliecināts, instalējiet jaunākos bināros failus.
    
2. Ja veicat jaunināšanu no Microsoft Dynamics AX 2012, pirms datu jaunināšanas palaišanas mērķa vidē instalējiet tālāk norādītos programmas X++ labojumus.
    - KB 4033183 — Dynamics AX 2012 R2 vai Dynamics AX 2012 R3 Pre-CU8 ar mazumtirdzniecību nesaistīta jaunināšana neizdodas ar ziņojumu Objekts nav atrasts vienumam dbo.RETAILTILLLAYOUTZONE.
    - Jaunināšana no KB 4040692 — Dynamics AX 2012 R3 uz Microsoft Dynamics 365 for Operations 7.2 neizdodas RetailSalesLine indeksa dublikātā vienumā SalesLineIdx.
    - KB 4035490 — veiktspējas problēma ar GeneralJournalAccountEntry MainAccount lauka jaunināšanas skriptu.


Veiciet šīs darbības, lai palaistu vides atkārtotas nodrošināšanas rīku.

1. Koplietojamo līdzekļu bibliotēkā atlasiet **Programmatūrā izvietojama pakotne**.
2. Lejupielādēt vides atkārtotas nodrošināšanas rīku.
3. Līdzekļu bibliotēkā jūsu projektam atlasiet **Programmatūrā izvietojama pakotne**.
4. Atlasiet **Jauns**, lai izveidotu jaunu pakotni.
5. Ievadiet pakotnes nosaukumu un aprakstu. Varat izmantot **Vides atkārtotas nodrošināšanas rīku** kā pakotnes nosaukumu.
6. Augšupielādējiet pakotni, kuru lejupielādējāt iepriekš.
7. Lapā **Informācija par vidi** jūsu mērķa videi atlasiet **Uzturēt** > **Lietot atjauninājumus.**
8. Atlasiet vides atkārtotas nodrošināšanas rīku, ko augšupielādējāt iepriekš, un pēc tam atlasiet **Lietot**, lai lietotu pakotni.
9. Pārraugiet pakotnes izvietošanas norisi. 

Papildinformāciju par to, kā lietot izvietojamu pakotni, skatiet sadaļā [Lietot izvietojamu pakotni](../deployment/create-apply-deployable-package.md). Papildinformāciju par to, kā manuāli lietot izvietojamu pakotni, skatiet sadaļā [Instalēt izvietojamu pakotni](../deployment/install-deployable-package.md).
