# Code list values

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II, III and IV of the Implementing Rule. To pass this test verify that any instance of an attribute:

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.
* takes values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'open' or if a value is not one of the values listed in the code list register check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements (This last check is a manual test).

<br>

The following check is performed for every feature in the dataset, for the not extensible codelist:

* Check that all the [FAOHorizonMaster](#FAOHorizonMaster) elements have a xlink:href attribute pointing to a [valid value](#validValue1). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue1"></a> Valid values for xlink:href attribute of [FAOHorizonMaster](#FAOHorizonMaster) element are available in the INSPIRE Registry. | 
| ---- | 
| FAOHorizonMasterValue: http://inspire.ec.europa.eu/codelist/FAOHorizonMasterValue |

* Check that all the [FAOHorizonSubordinate](#FAOHorizonSubordinate) elements have a xlink:href attribute pointing to a [valid value](#validValue2). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue2"></a> Valid values for xlink:href attribute of [FAOHorizonSubordinate](#FAOHorizonSubordinate) element are available in the INSPIRE Registry. | 
| ---- | 
| FAOHorizonSubordinateValue: http://inspire.ec.europa.eu/codelist/FAOHorizonSubordinateValue |

* Check that all the [FAOPrime](#FAOPrime) elements have a xlink:href attribute pointing to a [valid value](#validValue3). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue3"></a> Valid values for xlink:href attribute of [FAOPrime](#FAOPrime) element are available in the INSPIRE Registry. | 
| ---- | 
| FAOPrimeValue: http://inspire.ec.europa.eu/codelist/FAOPrimeValue |

* Check that all the [layerGenesisProcessState](#layerGenesisProcessState) elements have a xlink:href attribute pointing to a [valid value](#validValue4). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue4"></a> Valid values for xlink:href attribute of [layerGenesisProcessState](#layerGenesisProcessState) element are available in the INSPIRE Registry. | 
| ---- | 
| LayerGenesisProcessStateValue: http://inspire.ec.europa.eu/codelist/LayerGenesisProcessStateValue |

* Check that all the [layerType](#layerType) elements have a xlink:href attribute pointing to a [valid value](#validValue5). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue5"></a> Valid values for xlink:href attribute of [layerType](#layerType) element are available in the INSPIRE Registry. | 
| ---- | 
| LayerTypeValue: http://inspire.ec.europa.eu/codelist/LayerTypeValue |

* Check that all the [soilInvestigationPurpose](#soilInvestigationPurpose) elements have a xlink:href attribute pointing to a [valid value](#validValue6). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue6"></a> Valid values for xlink:href attribute of [soilInvestigationPurpose](#soilInvestigationPurpose) element are available in the INSPIRE Registry. | 
| ---- | 
| SoilInvestigationPurposeValue: http://inspire.ec.europa.eu/codelist/SoilInvestigationPurposeValue |

* Check that all the [soilPlotType](#soilPlotType) elements have a xlink:href attribute pointing to a [valid value](#validValue7). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue7"></a> Valid values for xlink:href attribute of [soilPlotType](#soilPlotType) element are available in the INSPIRE Registry. | 
| ---- | 
| SoilPlotTypeValue: http://inspire.ec.europa.eu/codelist/SoilPlotTypeValue |

* Check that all the [qualifierPlace](#qualifierPlace) elements have a xlink:href attribute pointing to a [valid value](#validValue8). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue8"></a> Valid values for xlink:href attribute of [qualifierPlace](#qualifierPlace) element are available in the INSPIRE Registry. | 
| ---- | 
| WRBQualifierPlaceValue: http://inspire.ec.europa.eu/codelist/WRBQualifierPlaceValue |

* Check that all the [WRBqualifier](#WRBqualifier) elements have a xlink:href attribute pointing to a [valid value](#validValue9). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue9"></a> Valid values for xlink:href attribute of [WRBqualifier](#WRBqualifier) element are available in the INSPIRE Registry. | 
| ---- | 
| WRBQualifierValue: http://inspire.ec.europa.eu/codelist/WRBQualifierValue |

* Check that all the [WRBReferenceSoilGroup](#WRBReferenceSoilGroup) elements have a xlink:href attribute pointing to a [valid value](#validValue10). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue10"></a> Valid values for xlink:href attribute of [WRBReferenceSoilGroup](#WRBReferenceSoilGroup) element are available in the INSPIRE Registry. | 
| ---- | 
| WRBReferenceSoilGroupValue: http://inspire.ec.europa.eu/codelist/WRBReferenceSoilGroupValue |

* Check that all the [WRBspecifier](#WRBspecifier) elements have a xlink:href attribute pointing to a [valid value](#validValue11). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue11"></a> Valid values for xlink:href attribute of [WRBspecifier](#WRBspecifier) element are available in the INSPIRE Registry. | 
| ---- | 
| WRBSpecifierValue: http://inspire.ec.europa.eu/codelist/WRBSpecifierValue |

<br>

The following check is performed for every feature in the dataset, for the 'narrower' codelist:

* Check that all the [soilThemeParameterName](#soilThemeParameterName) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValueA). If the check fails a manual check will be required asking to review the codelist definition in order to verify that any extensions do not overlap with the codelists that are defined in Annexes II, III and IV of the Implementing Rule. In particular, for the 'narrower' codelists the extended values shall refer to a parent value defined by the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).

| <a name="preDefinedValueA"></a> Pre-defined values for xlink:href attribute of [soilThemeParameterName](#soilThemeParameterName) element are available in the INSPIRE Registry| 
| ---- | 
| SoilDerivedObjectParameterNameValue: http://inspire.ec.europa.eu/codelist/SoilDerivedObjectParameterNameValue |

<br>

The following checks are performed for every feature in the dataset, for the 'open' codelist:

* Check that all the [layerGenesisEnvironment](#layerGenesisEnvironment) elements have a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue1). If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).

| <a name="preDefinedValue1"></a> Pre-defined values for xlink:href attribute of [layerGenesisEnvironment](#layerGenesisEnvironment) element are available in the INSPIRE Registry | 
| ---- | 
| EventEnvironmentValue: http://inspire.ec.europa.eu/codelist/EventEnvironmentValue |

* Check that all the [layerGenesisProcess](#layerGenesisProcess) elements have a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue2). If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).

| <a name="preDefinedValue2"></a> Pre-defined values for xlink:href attribute of [layerGenesisProcess](#layerGenesisProcess) element are available in the INSPIRE Registry | 
| ---- | 
| EventProcessValue: http://inspire.ec.europa.eu/codelist/EventProcessValue |

* Check that all the [layerRockType](#layerRockType) elements have a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue3). If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).

| <a name="preDefinedValue3"></a> Pre-defined values for xlink:href attribute of [layerRockType](#layerRockType) element are available in the INSPIRE Registry | 
| ---- | 
| LithologyValue: http://inspire.ec.europa.eu/codelist/LithologyValue |



**Reference(s)**: 

* [TG DS AF](./README.md#ref_TG_DS_SO) 5.3.3
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated + Manual

**Notes**



## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/> | XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. Please note that the URIs of all code list values from the INSPIRE Registry shall be referenced using the http protocol.
reviewCodeListValue <a name="reviewCodeListValue"/> | XML document '{filename}', {featureType} '{gmlid}': The property '{property}' has a value '{value}' that is not one of the pre-defined values in the INSPIRE data specification. The same value is used by {count} other features in the dataset, too. Extensions to the pre-defined values are allowed, but must not overlap with one of the pre-defined values and be consistent with the specification of the property. Please review the definition of the value. Please note that the URIs of all code list values from the INSPIRE Registry shall be referenced using the http protocol.


## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression				|Multiplicity       |Voidable
---------------------------------------------------------- | -------------------------------|-------------------|---------
FAOHorizonMaster <a name="FAOHorizonMaster"></a> | //schema-element(so:SoilHorizon)/so:FAOHorizonNotation/so:FAOHorizonNotationType/so:FAOHorizonMaster/@xlink:href | 1 | No
FAOHorizonSubordinate <a name="FAOHorizonSubordinate"></a> | //schema-element(so:SoilHorizon)/so:FAOHorizonNotation/so:FAOHorizonNotationType/so:FAOHorizonSubordinate/@xlink:href | 0..\* | No
FAOPrime <a name="FAOPrime"></a> | //schema-element(so:SoilHorizon)/so:FAOHorizonNotation/so:FAOHorizonNotationType/so:FAOPrime/@xlink:href | 1 | No
layerGenesisProcessState <a name="layerGenesisProcessState"></a> | //schema-element(so:SoilLayer)/so:layerGenesisProcessState/@xlink:href | 0..1 | Yes
layerType <a name="layerType"></a> | //schema-element(so:SoilLayer)/so:layerType/@xlink:href | 1 | No
soilInvestigationPurpose <a name="soilInvestigationPurpose"></a> | //schema-element(so:SoilSite)/so:soilInvestigationPurpose/@xlink:href | 1 | No
soilPlotType <a name="soilPlotType"></a> | //schema-element(so:SoilPlot)/so:soilPlotType/@xlink:href | 1 | No
qualifierPlace <a name="qualifierPlace"></a> | //schema-element(so:ObservedSoilProfile)/so:WRBSoilName/so:WRBSoilNameType/so:WRBQualifierGroup/so:WRBQualifierGroupType/so:qualifierPlace/@xlink:href <br> //schema-element(so:DerivedSoilProfile)/so:WRBSoilName/so:WRBSoilNameType/so:WRBQualifierGroup/so:WRBQualifierGroupType/so:qualifierPlace/@xlink:href | 1 | No
WRBqualifier <a name="WRBqualifier"></a> | //schema-element(so:ObservedSoilProfile)/so:WRBSoilName/so:WRBSoilNameType/so:WRBQualifierGroup/so:WRBQualifierGroupType/so:WRBqualifier/@xlink:href <br> //schema-element(so:DerivedSoilProfile)/so:WRBSoilName/so:WRBSoilNameType/so:WRBQualifierGroup/so:WRBQualifierGroupType/so:WRBqualifier/@xlink:href | 1 | No
WRBReferenceSoilGroup <a name="WRBReferenceSoilGroup"></a> | //schema-element(so:ObservedSoilProfile)/so:WRBSoilName/so:WRBSoilNameType/so:WRBReferenceSoilGroup/@xlink:href <br> //schema-element(so:DerivedSoilProfile)/so:WRBSoilName/so:WRBSoilNameType/so:WRBReferenceSoilGroup/@xlink:href | 1 | No
WRBspecifier <a name="WRBspecifier"></a> | //schema-element(so:ObservedSoilProfile)/so:WRBSoilName/so:WRBSoilNameType/so:WRBQualifierGroup/so:WRBQualifierGroupType/so:WRBspecifier/@xlink:href <br> //schema-element(so:DerivedSoilProfile)/so:WRBSoilName/so:WRBSoilNameType/so:WRBQualifierGroup/so:WRBQualifierGroupType/so:WRBspecifier/@xlink:href | 0..2 | No
soilThemeParameterName <a name="soilThemeParameterName"></a> | //schema-element(so:SoilThemeCoverage)/so:soilThemeParameter/so:SoilThemeParameterType/so:soilThemeParameterName/@xlink:href | 1 | No
layerGenesisEnvironment <a name="layerGenesisEnvironment"></a> | //schema-element(so:SoilLayer)/so:layerGenesisEnvironment/@xlink:href | 0..1 | Yes
layerGenesisProcess <a name="layerGenesisProcess"></a> | //schema-element(so:SoilLayer)/so:layerGenesisProcess/@xlink:href | 0..1 | Yes
layerRockType <a name="layerRockType"></a> | //schema-element(so:SoilLayer)/so:layerRockType/@xlink:href | 0..\* | Yes


