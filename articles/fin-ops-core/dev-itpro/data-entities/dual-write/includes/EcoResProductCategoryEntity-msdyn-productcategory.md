## <a name="product-categories-to-msdyn_productcategories"></a>Preču kategorijas uz msdyn_productcategories

Šī veidne sinhronizē datus starp Finance and Operations programmām un Common Data Service.

Finance and Operations lauks | Kartes veids | Cits Dynamics 365 lauks | Noklusējuma vērtība
---|---|---|---
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_hierarchy.msdyn_name | 
ISCATEGORYINHERITINGPARENTPRODUCTATTRIBUTES | >< | msdyn_isinheritingparentproductattributes | 
PROJECTCATEGORYNAME | = | msdyn_projectcategoryname | 
ISTANGIBLEPRODUCT | >< | msdyn_istangibleproduct | 
ISCATEGORYINHERITINGPARENTCATEGORYATTRIBUTES | >< | msdyn_isinheritingparentcategoryattributes | 
CATEGORYCODE | = | msdyn_code | 
CATEGORYDESCRIPTION | = | msdyn_description | 
CATEGORYKEYWORDS | = | msdyn_keywords | 
CATEGORYNAME | = | msdyn_name | 
FRIENDLYCATEGORYNAME | = | msdyn_friendlycategoryname | 
PARENTPRODUCTCATEGORYNAME | = | msdyn_parentproductcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | >> | msdyn_parentproductcategory.msdyn_hierarchy.msdyn_name | 
