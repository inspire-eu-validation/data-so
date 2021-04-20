# Statistical Units theme-specific requirements

**Purpose**: Verify that the following specific requirements are meet:

* (1) The values of the first level hierarchical code lists ProfileElementParameterNameValue, SoilDerivedObjectParameterNameValue, SoilProfileParameterNameValue, SoilSiteParameterNameValue (chemicalParameter, biologicalParameter, physicalParameter) serve only the purpose of structuring; only the lower-level values shall be used.
* (2) When an additional descriptive parameter for the soil derived object is needed, the parameter attribute of the OM_Observation spatial object type shall be used.
* (3) Only one Other Horizon Notation Type classification shall be used for a dataset.
* (4) Only one Other Soil Name Type classification shall be used for a dataset.


**Prerequisites**

**Test method**

The following check is performed for every feature in the dataset.

* Check that <ins>only</ins> the lower-level values of the hierarchical code lists [ProfileElementParameterNameValue](http://inspire.ec.europa.eu/codelist/ProfileElementParameterNameValue), [SoilDerivedObjectParameterNameValue](http://inspire.ec.europa.eu/codelist/SoilDerivedObjectParameterNameValue), [SoilProfileParameterNameValue](http://inspire.ec.europa.eu/codelist/SoilProfileParameterNameValue), [SoilSiteParameterNameValue](http://inspire.ec.europa.eu/codelist/SoilSiteParameterNameValue) are used (the values of the first level: chemicalParameter, biologicalParameter, physicalParameter serve <ins>only</ins> the purpose of structuring).


The following check shall be manually performed for every feature in the dataset:

* Check that when an additional descriptive parameter for the soil derived object is needed, the parameter attribute of the OM_Observation spatial object type is used.

* Check that only one Other Horizon Notation Type classification is used for a dataset.
* Check that only one Other Soil Name Type classification is used for a dataset.


**Reference(s)**: 

* [TG DS-SO](./README.md#ref_TG_DS_SO) 5.3.1.1.
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex IV, Section 3.4

**Test type**: Automatic + Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
