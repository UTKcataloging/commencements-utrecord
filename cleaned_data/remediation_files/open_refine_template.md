# Open Refine Commencement Programs within the UT Record


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["identifier"].value}}</identifier>
{{if(isBlank(cells['title_supplied'].value), '', '<titleInfo supplied="yes"><title>' + cells["title_supplied"].value + '</title></titleInfo>')}} 
{{if(isBlank(cells['title_alternative'].value), '', '<titleInfo type="alternative"><title>' + cells['title_alternative'].value + '</title></titleInfo>')}} 
<abstract>{{cells["abstract"].value}}</abstract>
{{if(isBlank(cells['dateCreated_year'].value), '', '<originInfo><dateCreated>' + cells['dateCreated_year'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes">' + cells['Season'].value + '</dateCreated><dateIssued encoding="edtf">' + cells['date_edtf'].value + '</dateIssued></originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells["extent"].value}}</extent></physicalDescription>
{{if(isBlank(cells['subject1'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject1_URI'].value + '"><topic>' + cells['subject1'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_URI'].value + '"><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
<language>
<languageTerm type="text" authority="iso639-2b">English</languageTerm>
</language>
<typeOfResource>text</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_project'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```