# Code lists

**Purpose**: Verify that code lists extensions can be accessed.

**Prerequisites**

**Test method**

* Verify that any code list extensions are publicly accessible via HTTP, i.e. inspect extensible code list values property elements. If a reference (@xlink:href) has a value that does not start with http://inspire.ec.europa.eu/codelist/, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following empty code lists:

* [OtherHorizonNotationTypeValue](#OtherHorizonNotationTypeValue): http://inspire.ec.europa.eu/codelist/OtherHorizonNotationTypeValue
* [OtherSoilNameTypeValue](#OtherSoilNameTypeValue): http://inspire.ec.europa.eu/codelist/OtherSoilNameTypeValue


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS SU](./README.md#ref_TG_DS_SU) Annex C

**Test type**: Automated

**Notes**

The [Technical Guidelines](./README.md#ref_TG_DS_SU) defines recommended values, available in the INSPIRE Registry, that may be used by data providers and. Before creating new terms, please check if one of them can be used.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression      |Multiplicity   |Voidable
---------------------------------------------------------- | -----------------------|---------------|---------------------------------
OtherHorizonNotationTypeValue <a name="OtherHorizonNotationTypeValue"></a> | //schema-element(so:SoilHorizon)/so:otherHorizonNotation/so:OtherHorizonNotationType/so:horizonNotation/@xlink:href | 1 (0..\* for the parent) | No
OtherSoilNameTypeValue <a name="OtherSoilNameTypeValue"></a> | //schema-element(so:ObservedSoilProfile)/so:otherSoilName/so:OtherSoilNameType/so:soilName/@xlink:href <br> //schema-element(so:DerivedSoilProfile)/so:otherSoilName/so:OtherSoilNameType/so:soilName/@xlink:href | 1 (0..\* for the parent) | No