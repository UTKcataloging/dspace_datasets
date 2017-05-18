# DSPACE Dataset Metadata Migration

---

## About

This repository includes metadata for the DSPACE metadata migration.

## Metadata Mapping from DSPACE

| Dspace Mapping | MODS Mapping | Notes |
|--------|--------|-------|
| id | ```<identifier type="local" displayLabel="dspace">VALUE</identifier>``` |  |
| collection | **Dont Map** |  |
| dc.contributor.author | ```<name><namePart>VALUE</namePart><role><roleTerm authority="marcrelator" valueURI="">Creator</roleTerm</role>```| |
| dc.coverage.spatial | ```<subject><geographic>VALUE</geographic><cartographics></cartographics>``` | Concat country / city |
| dc.coverage.temporal | ```<originInfo><dateCreated encoding="edtf" keyDate="yes" point="start">VALUE1</dateCreated>><dateCreated encoding="edtf" keyDate="yes" point="end">VALUE2</dateCreated><dateCreated>BOTH VALUES</dateCreated></originInfo>``` | Split Values into individual nodes for machine actionable start / end dates in Solr.  Also, keep them together so we can display them like that to users.    |
| dc.creator | ```<name><namePart>VALUE</namePart><role><roleTerm authority="marcrelator" valueURI="">Creator</roleTerm</role>``` |  |
| dc.date.issued  | ```<originInfo><dateCaptured>VALUE</dateCaptured></originInfo>```|  |
| dc.date.issued[]  | ```<originInfo><dateCaptured>VALUE</dateCaptured></originInfo>``` | If edtf, keep.  If not, drop. |
| dc.date | ```<originInfo><dateCaptured>VALUE</dateCaptured></originInfo>``` |  |
| dc.description.abstract  | ```<abstract>VALUE</abstract>``` |  |
| dc.description.sponsorship  | ```<note displayLabel="sponsor">VALUE</note>```|  |
| dc.description  | ```<abstract>VALUE</abstract>``` |  |
| dc.identifier.citation[]  | ```<note type="citation">VALUE</note>``` |  |
| dc.identifier.citation[en_US]  | ```<note type="citation">VALUE</note>``` |  |
| dc.identifier.uri  | ```<identifier type="doi">VALUE</identifier>``` | **If DOI ONLY!!!**  |
| dc.language.iso | ```<language><languageTerm type="code" authority="iso639-2b">VALUE</languageTerm></language>``` | These all need to be cleaned. |
| dc.language | ```<language><languageTerm type="code" authority="iso639-2b">VALUE</languageTerm></language>``` | These all need to be cleaned. |
| dc.publisher  | ```<originInfo><publisher>VALUE</publisher></originInfo>``` | Only Keep PLOS.  Other values aren't publishers. |
| dc.rights  | ```<accessCondition type="use and reproduction">VALUE</accessCondition>``` |  |
| dc.subject | ```<subject><topic>VALUE</topic></subject>``` |  |
| dc.title.alternative  | Don't Map | Drop.  Not a title. |
| dc.title  | ```<titleInfo><title>VALUE</title></titleInfo>``` |  |
| dc.type  | **Don't Map** | Do not map.  Inconsistent use.  We will brute force all of this below.  |

## Additional Fields

| New MODS Field | Notes |
|------|------|
|```<relatedItem type="series"><titleInfo ><title>Faculty and Graduate Student Research and Creative Work</title></titleInfo></relatedItem>``` | |
| ```<physicalDescription><form authority="casrai" valueURI="http://dictionary.casrai.org/Data_Set">Data Set</form></physicalDescription>``` | Couldn't find an ontology with URI that represented this concept. |
| ```<typeOfResource>software, multimedia</typeOfResource>```| Appropriate for any electronic resource without a significant aspect that indicates one of the other <typeOfResource> categories. It includes: software, numeric data, computer-oriented multimedia, and online systems and services.  |

## OpenRefine Template



