# ConfigurableProductSplitter

Splits all configurable products in product list by color while trying to keep product order. When opening a product page, color variant clicked will be preselected. This was implemented by modifying product collection after it has loaded in observer event which gets fired from product list block in frontend.

## Known issues 

* Because of modifying collection items after it has loaded, the collection count will be invalid, and this may cause issues elsewhere. 
* Also product ids in the collection will be invalid since configurable items' ids gets replaced by simple products' ids. 
* If the collection will be loaded again elsewhere, configurable products do not get splitted. 
* Products per page limiter does not work anymore. 
* Products count on product list is invalid. 
* 3rd party search modules such as Klevu might not work 
* Other 3rd party modules may have issues with the implementation. 
* Product stock data, reviews etc. are broken on product list (although is probably easy to fix in frontend). 
* Not sure if implementation will work without url rewrites (should be easy to fix though).
