# Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

* Constraints of the spatial object type ProfileElement (SoilHorizon or SoilLayer):
	* To fill the featureOfInterest property of the profile element observations of a ProfileElement object, that same ProfileElement object shall be used (FoI of profile element observations).
	* The observedProperty of the profile element observation shall be specified using a value from the ProfileElementParameterNameValue code list.
	* The result of the profile element observation shall be of one of the following types: Number; RangeType; CharacterString.

* Constraints of the spatial object type SoilDerivedObject:
	* To fill the featureOfInterest property of the soil derived object observation, the same SoilDerivedObject object shall be used.
	* The observedProperty of the soil derived object observation shall be specified using a value from the SoilDerivedObjectParameterNameValue code list.
	* The result of the soil derived object observation shall be of one of the following types: Number; RangeType; CharacterString.

* Constraints of the spatial object type SoilLayer:
	* The attributes layerGenesisProcess, layerGenesisEnvironment, layerGenesisProcessState and layerRockType shall only be provided where the layerType is of the value “geogenic” (geogenicConstraint).

* Constraints of the spatial object type SoilProfile:
	* To fill the featureOfInterest property of the soil profile observations of a SoilProfile object, that same SoilProfile object shall be used.
	* The observedProperty of the soil profile observation shall be specified using a value from the SoilProfileParameterNameValue code list.
	* The result of the soil profile observation shall be of one of the following types: Number; RangeType; CharacterString.

* Constraints of the spatial object type SoilSite:
	* To fill the featureOfInterest property of the soil site observations of a SoilSite object, that same SoilSite object shall be used.
	* The observedProperty of the soil site observation shall be specified using a value from the SoilSiteParameterNameValue code list.
	* The result of the soil site observation shall be of one of the following types: Number; RangeType; CharacterString.
	* The result of the soil site observation shall be of type SoilObservationResult.

* Constraints of the spatial object type SoilThemeCoverage:
	* The rangeSet values shall be of one of the following types: Number; RangeType; CharacterString (rangeSetValuesConstraint).

* Constraints of the spatial object type SoilThemeDescriptiveCoverage:
	* The rangeSet values shall be of one of the following types: Number; RangeType; CharacterString (rangeSetValuesConstraint).

* Constraints of the data type RangeType:
	* At least one of the values shall not be empty (intervalConstraint).
	

**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset:

* Check that the attributes [layerGenesisProcess](layerGenesisProcess), [layerGenesisEnvironment](layerGenesisEnvironment), [layerGenesisProcessState](layerGenesisProcessState) and [layerRockType](layerRockType) are only provided where the [layerType](layerType) is of the value “[geogenic](http://inspire.ec.europa.eu/codelist/LayerTypeValue/geogenic)” (OCL: "inv: self.layerType = LayerTypeValue::geogenic implies (self.layerGenisisEnvironment.isNotEmpty() and self.layerGenisisProcess.isNotEmpty() and self.layerRockType.isNotEmpty() and layerGenesisProcessState.isNotEmpty())").

* Check that at least one of the values ([upperValue](upperValue) or [lowerValue](lowerValue)) of the RangeType dataType is not empty (OCL: "inv: self.upperValue->notEmpty() or self.lowerValue->notEmpty()").


The following checks shall be manually performed for every feature in the dataset:

* ProfileElement (SoilHorizon or SoilLayer):
	* Check that to fill the featureOfInterest property of the profile element observations of a ProfileElement object, the same ProfileElement object is used (OCL: "inv: self.profileElementObservation.featureOfInterest = self").
	* Check that the observedProperty of the profile element observation is specified using a value from the [ProfileElementParameterNameValue](http://inspire.ec.europa.eu/codelist/ProfileElementParameterNameValue) code list.
	* Check that the result of the profile element observation is of one of the following types: Number; RangeType; CharacterString.

* SoilDerivedObject:
	* Check that to fill the  featureOfInterest property of the soil derived object observation, the same SoilDerivedObject object is used.
	* Check that the observedProperty of the soil derived object observation is specified using a value from the [SoilDerivedObjectParameterNameValue](http://inspire.ec.europa.eu/codelist/SoilDerivedObjectParameterNameValue) code list.
	* Check that the result of the soil derived object observation is of one of the following types: Number; RangeType; CharacterString.

* SoilProfile (ObservedSoilProfile or DerivedSoilProfile):
	* Check that to fill the featureOfInterest property of the soil profile observations of a SoilProfile object, that same SoilProfile object is used.
	* Check that the observedProperty of the soil profile observation shall be specified using a value from the [SoilProfileParameterNameValue](http://inspire.ec.europa.eu/codelist/SoilProfileParameterNameValue) code list.
	* Check that the result of the soil profile observation is of one of the following types: Number; RangeType; CharacterString.
	
* SoilSite:
	* Check that to fill the featureOfInterest property of the soil site observations of a SoilSite object, that same SoilSite object is used.
	* Check that the observedProperty of the soil site observation shall be specified using a value from the [SoilSiteParameterNameValue](http://inspire.ec.europa.eu/codelist/SoilSiteParameterNameValue) code list.
	* Check that the result of the soil site observation is of one of the following types: Number; RangeType; CharacterString.
	* Check that the result of the soil site observation is of type SoilObservationResult.

* SoilThemeCoverage:
	* Check that the [rangeSet](rangeSetSTC) values are of one of the following types: Number; RangeType; CharacterString (OCL: "inv: rangeSet->oclIsKindOf(Number) or rangeSet->oclIsKindOf(Characterstring) or rangeSet->oclIsKindOf(RangeType)").

* SoilThemeDescriptiveCoverage:
	* Check that the [rangeSet](rangeSetSTDC) values are of one of the following types: Number; RangeType; CharacterString (OCL: "inv: rangeSet->oclIsKindOf(Number) or rangeSet->oclIsKindOf(Characterstring) or rangeSet->oclIsKindOf(RangeType)").


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-SO](./README.md#ref_TG_DS_SO) 5.3.2.1.4.; 

**Test type**: Automated + Manual

**Notes** 

* The ProfileElement feature type is abstract, it is specilized by SoilHorizon and SoilLayer feature types.
* The SoilProfile feature type is abstract, it is specilized by ObservedSoilProfile and DerivedSoilProfile feature types.


Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
layerGenesisProcess <a name="layerGenesisProcess"></a> | //schema-element(so:SoilLayer)/so:layerGenesisProcess | 0..1 | Yes
layerGenesisEnvironment <a name="layerGenesisEnvironment"></a> | //schema-element(so:SoilLayer)/so:layerGenesisEnvironment | 0..1 | Yes
layerGenesisProcessState <a name="layerGenesisProcessState"></a> | //schema-element(so:SoilLayer)/so:layerGenesisProcessState | 0..1 | Yes
layerRockType <a name="layerRockType"></a> | //schema-element(so:SoilLayer)/so:layerRockType | 0..\* | Yes
layerType <a name="layerType"></a> | //schema-element(so:SoilLayer)/so:layerType/@xlink:href="http://inspire.ec.europa.eu/codelist/LayerTypeValue/geogenic" | 1 | No
rangeSet (SoilThemeCoverage) <a name="rangeSetSTC"></a> | //schema-element(so:SoilThemeCoverage)/gml:rangeSet | 0..\* | No
rangeSet (SoilThemeDescriptiveCoverage) <a name="rangeSetSTDC"></a> | //schema-element(so:SoilThemeDescriptiveCoverage)/gml:rangeSet | 0..\* | No
upperValue <a name="upperValue"></a> | //schema-element(so:SoilLayer)/so:profileElementDepthRange/so:RangeType/so:upperValue <br> //schema-element(so:SoilHorizon)/so:profileElementDepthRange/so:RangeType/so:upperValue <br> //schema-element(so:SoilLayer)/so:particleSizeFraction/so:ParticleSizeFractionType/so:fractionParticleSizeRange/so:RangeType/so:upperValue <br> //schema-element(so:SoilHorizon)/so:particleSizeFraction/so:ParticleSizeFractionType/so:fractionParticleSizeRange/so:RangeType/so:upperValue <br> //schema-element(so:SoilBody)/so:isDescribedBy/so:DerivedProfilePresenceInSoilBody/so:derivedProfilePercentageRange/so:RangeType/so:upperValue | 0..1 | No
lowerValue <a name="lowerValue"></a> | //schema-element(so:SoilLayer)/so:profileElementDepthRange/so:RangeType/so:lowerValue <br> //schema-element(so:SoilHorizon)/so:profileElementDepthRange/so:RangeType/so:lowerValue <br> //schema-element(so:SoilLayer)/so:particleSizeFraction/so:ParticleSizeFractionType/so:fractionParticleSizeRange/so:RangeType/so:lowerValue <br> //schema-element(so:SoilHorizon)/so:particleSizeFraction/so:ParticleSizeFractionType/so:fractionParticleSizeRange/so:RangeType/so:lowerValue <br> //schema-element(so:SoilBody)/so:isDescribedBy/so:DerivedProfilePresenceInSoilBody/so:derivedProfilePercentageRange/so:RangeType/so:lowerValue | 0..1 | No