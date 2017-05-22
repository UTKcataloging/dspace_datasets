# DSPACE Datasets Open Refine Template

### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

### Row Template

```
<mods xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
<titleInfo><title>{{cells['Title'].value}}</title></titleInfo>
<identifier type="local" displayLabel="dspace">{{cells['id'].value}}</identifier>
<name><namePart>{{cells['dc.contributor.author.1'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.contributor.author.2'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.contributor.author.3'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.contributor.author.4'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.creator.1'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.creator.2'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.creator.3'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.creator.4'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.creator.5'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<name><namePart>{{cells['dc.creator.6'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre.html">Creator</roleTerm></role></name>
<subject><geographic>{{cells['dc.coverage.spatial.2'].value}}</geographic></subject>
<subject><geographic>{{cells['dc.coverage.spatial.3'].value}}</geographic></subject>
<originInfo>
<dateCreated encoding="edtf" keyDate="yes" point="start">{{cells['dc.coverage.temporal.start'].value}}</dateCreated>
<dateCreated encoding="edtf" keyDate="yes" point="end">{{cells['dc.coverage.temporal.end'].value}}</dateCreated>
<dateCaptured>{{cells['dc.date.issued'].value}}</dateCaptured>
<dateCaptured>{{cells['dc.date.issued.1'].value}}</dateCaptured>
<dateCaptured>{{cells['dc.date.issued.2'].value}}</dateCaptured>
</originInfo>
<abstract>{{cells['dc.description.abstract'].value}}</abstract>
<abstract>{{cells['dc.description'].value}}</abstract>
<note displayLabel="sponsor">{{cells['dc.description.sponsorship'].value}}</note>
<note type="citation">{{cells['dc.identifier.citation'].value}}</note>
<note type="citation">{{cells['dc.identifier.citation.1'].value}}</note>
<identifier type="doi">{{cells['dc.identifier.uri.1'].value}}</identifier>
<identifier type="doi">{{cells['dc.identifier.uri.2'].value}}</identifier>
<language><languageTerm type="code" authority="iso639-2b">{{cells['dc.language.iso.1'].value}}</languageTerm></language>
<language><languageTerm type="code" authority="iso639-2b">{{cells['dc.language.iso.2'].value}}</languageTerm></language>
<language><languageTerm type="code" authority="iso639-2b">{{cells['dc.language.iso.3'].value}}</languageTerm></language>
<accessCondition type="use and reproduction">{{cells['dc.rights'].value}}</accessCondition>
<subject><topic>{{cells['dc.subject.1'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.2'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.3'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.4'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.5'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.6'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.7'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.8'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.9'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.10'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.11'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.12'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.13'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.14'].value}}</topic></subject>
<subject><topic>{{cells['dc.subject.15'].value}}</topic></subject>
<relatedItem type="series"><titleInfo ><title>Faculty and Graduate Student Research and Creative Work</title></titleInfo></relatedItem>
<physicalDescription><form authority="coar" valueURI="http://purl.org/coar/resource_type/c_ddb1">dataset</form></physicalDescription>
<typeOfResource>software, multimedia</typeOfResource>
<recordInfo><recordContentSource authority="isni" valueURI="http://www.isni.org/isni/0000000123151184">University of Tennessee (Knoxville)</recordContentSource> <languageOfCataloging><languageTerm type="code" authority="iso639-2b">eng</languageTerm></languageOfCataloging><recordOrigin>Created and edited in general conformance to MODS Guidelines (Version 3.5).</recordOrigin></recordInfo>
</mods>
```

### Row Separator

Leave this **blank**.

### Suffix

```
</modsCollection>
```