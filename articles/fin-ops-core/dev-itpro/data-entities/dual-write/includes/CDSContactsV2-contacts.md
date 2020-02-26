## <a name="cds-contacts-v2-to-contacts"></a>CDS kontaktpersonas V2 uz kontaktpersonām

Šī veidne sinhronizē datus starp Finance and Operations programmām un Common Data Service.

Avota filtrs: (AssociatedContactType = 1)

Pretējais avota filtrs: msdyn_contactforvendor eq true un msdyn_sellable eq false un msdyn_contactpersonid ne ''

Finance and Operations lauks | Kartes veids | Cits Dynamics 365 lauks | Noklusējuma vērtība
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | nav | Kreditors
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | fakss | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | nodaļa | 
PIEZĪMES | = | apraksts | 
DZIMUMS | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
nav | >> | msdyn_contactforvendor | Patiess
CONTACTPERSONID | = | msdyn_contactpersonid | 
