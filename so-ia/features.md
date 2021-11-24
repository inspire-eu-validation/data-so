# Feature references

**Purpose**: Verify that referenced features can be retrieved.

**Prerequisites**

**Test method**

* Verify that any feature reference in an association role is publicly accessible via HTTP, i.e. inspect all relevant properties. If a reference (@xlink:href) has a value that starts with "#", verify that an element with a `gml:id` attribute with the referenced identifier exists in the same document. If the reference starts with "http", verify that a HTTP GET request to the URI retrieves an XML document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following association role:

* [DerivedSoilProfile.isDerivedFrom](#isDerivedFrom): ObservedSoilProfile
* [ObservedSoilProfile.location](#location): SoilPlot
* [ProfileElement.isPartOf](#isPartOf): SoilProfile
* [ProfileElement.profileElementObservation](#profileElementObservation): OM_Observation 
* [SoilBody.isDescribedBy](#isDescribedBySB): DerivedSoilProfile
* [SoilDerivedObject.isBasedOnSoilDerivedObject](#isBasedOnSoilDerivedObject): SoilDerivedObject
* [SoilDerivedObject.isBasedOnObservedSoilProfile](#isBasedOnObservedSoilProfile): ObservedSoilProfile
* [SoilDerivedObject.isBasedOnSoilBody](#isBasedOnSoilBody): SoilBody
* [SoilDerivedObject.soilDerivedObjectObservation](#soilDerivedObjectObservation): OM_Observation
* [SoilPlot.locatedOn](#locatedOn): SoilSite
* [SoilPlot.observedProfile](#observedProfile): ObservedSoilProfile
* [SoilProfile.isDescribedBy](#isDescribedBySP): ProfileElement
* [SoilProfile.soilProfileObservation](#soilProfileObservation): OM_Observation
* [SoilSite.isObservedOnLocation](#isObservedOnLocation): SoilPlot
* [SoilSite.soilSiteObservation](#soilSiteObservation): OM_Observation
* [SoilThemeCoverage.isDescribedBy](#isDescribedBySTC): SoilThemeDescriptiveCoverage
* [SoilThemeDescriptiveCoverage.isDescribing](#isDescribing): SoilThemeCoverage


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

**Notes**

ProfileElement and SoilProfile feature types are abstract.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                         |  XPath expression    | Multiplicity    | Voidable
------------------------------------ | ---------------------|-----------------|------------
DerivedSoilProfile.isDerivedFrom <a name ="isDerivedFrom"></a> | //schema-element(so:DerivedSoilProfile)/so:isDerivedFrom/@xlink:href | 0..\* | Yes
ObservedSoilProfile.location <a name ="location"></a> | //schema-element(so:ObservedSoilProfile)/so:location/@xlink:href | 1 | No
ProfileElement.isPartOf <a name ="isPartOf"></a> | //schema-element(so:SoilHorizon)/so:isPartOf/@xlink:href <br> //schema-element(so:SoilLayer)/so:isPartOf/@xlink:href | 1 | No
ProfileElement.profileElementObservation <a name ="profileElementObservation"></a> | //schema-element(so:SoilHorizon)/so:profileElementObservation/@xlink:href <br> //schema-element(so:SoilLayer)/so:profileElementObservation/@xlink:href | 0..\* | Yes
SoilBody.isDescribedBy <a name ="isDescribedBySB"></a> | //schema-element(so:SoilBody)/so:isDescribedBy/@xlink:href <br> //schema-element(so:SoilBody)/so:isDescribedBy/so:DerivedProfilePresenceInSoilBody/so:isDescribedBy/@xlink:href | 1..\* | Yes
SoilDerivedObject.isBasedOnSoilDerivedObject <a name ="isBasedOnSoilDerivedObject"></a> | //schema-element(so:SoilDerivedObject)/so:isBasedOnSoilDerivedObject/@xlink:href | 0..\* | Yes
SoilDerivedObject.isBasedOnObservedSoilProfile <a name ="isBasedOnObservedSoilProfile"></a> | //schema-element(so:SoilDerivedObject)/so:isBasedOnObservedSoilProfile/@xlink:href | 0..\* | Yes
SoilDerivedObject.isBasedOnSoilBody <a name ="isBasedOnSoilBody"></a> | //schema-element(so:SoilDerivedObject)/so:isBasedOnSoilBody/@xlink:href | 0..\* | Yes
SoilDerivedObject.soilDerivedObjectObservation <a name ="soilDerivedObjectObservation"></a> | //schema-element(so:SoilDerivedObject)/so:soilDerivedObjectObservation/@xlink:href | 1..\* | Yes
SoilPlot.locatedOn <a name ="locatedOn"></a> | //schema-element(so:SoilPlot)/so:locatedOn/@xlink:href | 0..1 | Yes
SoilPlot.observedProfile <a name ="observedProfile"></a> | //schema-element(so:SoilPlot)/so:observedProfile/@xlink:href | 1 | Yes
SoilProfile.isDescribedBy <a name ="isDescribedBySP"></a> | //schema-element(so:ObservedSoilProfile)/so:isDescribedBy/@xlink:href <br> //schema-element(so:DerivedSoilProfile)/so:isDescribedBy/@xlink:href | 1..\* | Yes
SoilProfile.isDescribedBy <a name ="soilProfileObservation"></a> | //schema-element(so:ObservedSoilProfile)/so:soilProfileObservation/@xlink:href <br> //schema-element(so:DerivedSoilProfile)/so:soilProfileObservation/@xlink:href | 0..\* | Yes
SoilSite.isObservedOnLocation <a name ="isObservedOnLocation"></a> | //schema-element(so:SoilSite)/so:isObservedOnLocation/@xlink:href | 1..\* | Yes
SoilSite.soilSiteObservation <a name ="soilSiteObservation"></a> | //schema-element(so:SoilSite)/so:soilSiteObservation/@xlink:href | 0..\* | Yes
SoilThemeCoverage.isDescribedBy <a name ="isDescribedBySTC"></a> | //schema-element(so:SoilThemeCoverage)/so:isDescribedBy/@xlink:href | 0..\* | Yes
SoilThemeDescriptiveCoverage.isDescribing <a name ="isDescribing"></a> | //schema-element(so:SoilThemeDescriptiveCoverage)/so:isDescribing/@xlink:href | 1 | No
