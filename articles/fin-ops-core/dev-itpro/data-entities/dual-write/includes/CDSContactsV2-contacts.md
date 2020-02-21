## <a name="cds-contacts-v2-to-contacts"></a>ผู้ติดต่อของ CDS V2 สำหรับผู้ติดต่อ

เท็มเพลตนี้ซิงโครไนส์ข้อมูลระหว่างแอป Finance and Operations และ Common Data Service

ตัวกรองต้นทาง: (AssociatedContactType = 1)

ตัวกรองต้นทางแบบย้อนกลับ: msdyn_contactforvendor eq true และ msdyn_sellable eq false และ msdyn_contactpersonid ne ''

ฟิลด์ Finance and Operations | ชนิดของการแม็ป | ฟิลด์ Dynamics 365 อื่นๆ | ค่าเริ่มต้น
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | none | ผู้จัดจำหน่าย
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | fax | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | department | 
NOTES | = | description | 
GENDER | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
none | >> | msdyn_contactforvendor | True
CONTACTPERSONID | = | msdyn_contactpersonid | 
