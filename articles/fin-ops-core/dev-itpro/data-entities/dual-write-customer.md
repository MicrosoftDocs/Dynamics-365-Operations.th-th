---
title: ข้อมูลหลักของลูกค้าแบบรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลของลูกค้าระหว่าง Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a66beb6338ea593247c79a11feb7f301d56f32a9
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572529"
---
# <a name="integrated-customer-master"></a>ข้อมูลหลักของลูกค้าแบบรวม

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

เป็นเรื่องปกติสำหรับเรกคอร์ดลูกค้าที่จะมีความเชี่ยวชาญในแอพลิเคชันมากกว่าหนึ่งรายการ ตัวอย่างเช่น กิจกรรมการขายสามารถนำเรกคอร์ดลูกค้าเชิงพาณิชย์เข้ามาผ่านแอพลิเคชันทางการขายและ e-Commerce หรือการขายปลีกสามารถนำเรกคอร์ดลูกค้าเข้ามาผ่านแอพลิเคชัน Finance and Operations โดยไม่คำนึงถึงจุดกำเนิดของเรกคอร์ดลูกค้า จะมีการรวมอยู่เบื้องหลังในขอบเขตของแอพลิเคชันและความแตกต่างของโครงสร้างพื้นฐาน การพัฒนาความเชี่ยวชาญของลูกค้าแบบรวมช่วยจัดการสถานการณ์จำลองการพัฒนาความเชี่ยวชาญที่หลากหลาย และให้มุมมองที่ครอบคลุมของลูกค้าไปยังชุดแอพลิเคชัน Dynamics 365

## <a name="customer-data-flow"></a>โฟลว์ข้อมูลของลูกค้า

*ลูกค้า*เป็นแนวคิดที่กำหนดไว้อย่างดีในแอปพลิเคชัน ดังนั้น การรวมของข้อมูลลูกค้าก็เกี่ยวข้องกับความสอดคล้องแนวคิดของลูกค้าระหว่างสองแอพลิเคชัน ภาพประกอบต่อไปนี้แสดงโฟลว์ข้อมูลของลูกค้า

![โฟลว์ข้อมูลของลูกค้า](media/dual-write-customer-data-flow.png)

ลูกค้าสามารถแบ่งออกย่างกว้างๆ ได้เป็นสองประเภท: ลูกค้าเชิงพาณิชย์/เชิงองค์กร และผู้บริโภค/ผู้ใช้ ลูกค้าสองประเภทนี้จะถูกจัดเก็บและได้รับจัดการโดยแตกต่างกันใน Finance and Operations และ Common Data Service

ใน Finance and Operations ทั้งลูกค้าเชิงพาณิชย์/เชิงองค์กร และผู้บริโภค/ผู้ใช้ จะมีความเชี่ยวชาญในตารางเดียวที่ชื่อว่า **CustTable** (CustomerCustomerV3Entity) และจะถูกจำแนกประเภทตามแอททริบิวต์ **ชนิด** (ถ้า **ชนิด** ถูกตั้งค่าเป็น **องค์กร** ลูกค้าเป็นลูกค้าเชิงพาณิชย์/เชิงองค์กร และถ้ามีการตั้งค่า **ชนิด** เป็น **บุคคล** ลูกค้าเป็นผู้บริโภค/ผู้ใช้) ข้อมูลผู้ติดต่อหลักจะได้รับการจัดการผ่านเอนทิตี SMMContactPersonEntity

ใน Common Data Service ลูกค้าเชิงพาณิชย์/เชิงองค์กรมีความเชี่ยวชาญในเอนทิตีบัญชี และถูกระบุเป็นลูกค้า เมื่อมีการตั้งค่าแอททริบิวต์ **RelationshipType** เป็น **ลูกค้า** ทั้งผู้บริโภค/ผู้ใช้และผู้ติดต่อจะถูกแสดงโดยเอนทิตีผู้ติดต่อ เพื่อให้การแยกที่ชัดเจนระหว่างผู้บริโภค/ผู้ใช้ และผู้ติดต่อ เอนทิตี **ผู้ติดต่อ** มีแฟล็กบูลีนที่มีชื่อว่า **Sellable** เมื่อ **Sellable** เป็น **จริง** ผู้ติดต่อเป็นผู้บริโภค/ผู้ใช้ และสามารถสร้างใบเสนอราคาและใบสั่งสำหรับผู้ติดต่อนั้นได้ เมื่อ **Sellable** เป็น **เท็จ** ผู้ติดต่อเป็นเพียงผู้ติดต่อหลักของลูกค้า

เมื่อผู้ติดต่อที่ไม่ใช่ Sellable มีส่วนร่วมในกระบวนการใบเสนอราคาหรือใบสั่ง **Sellable** ถูกตั้งค่าเป็น **จริง** เพื่อแฟล็กผู้ติดต่อเป็นผู้ติดต่อ Sellable ผู้ติดต่อที่กลายเป็นผู้ติดต่อที่สามารถขายได้ยังคงเป็นผู้ติดต่อ Sellable

## <a name="templates"></a>เท็มเพลต

ข้อมูลลูกค้ารวมถึงข้อมูลทั้งหมดเกี่ยวกับลูกค้า เช่น กลุ่มลูกค้า ที่อยู่ ข้อมูลผู้ติดต่อ โพรไฟล์การชำระเงิน และสถานะบัตรสมาชิก ชุดของแผนผังเอนทิตีทำงานร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

แอพ Finance and Operations    | แอปพลิเคชันอื่น ๆ ของ Dynamics 365
--------------------------|---------------------------------
V3 ของลูกค้า               | บัญชี
V3 ของลูกค้า               | ผู้ติดต่อ
ผู้ติดต่อ CDS V2           | ผู้ติดต่อ
กลุ่มลูกค้า           | Msdyn\_customergroups
วิธีการชำระเงินของลูกค้า   | Msdyn\_customerpaymentmethods
บัตรสมาชิก              | Msdyn\_loyaltycards
กำหนดการชำระเงิน          | Msdyn\_paymentschedules
กำหนดการชำระเงิน          | Msdyn\_paymentschedulelines
CDS วันที่ชำระเงิน           | Msdyn\_paymentdays
CDS รายการแสดงวันที่ชำระเงิน     | Msdyn\_paymentdaylines
เงื่อนไขการชำระเงิน          | Msdyn\_paymentterms
ส่วนเพิ่มของชื่อ              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>ลูกค้า V3 สำหรับบัญชี

เท็มเพลตนี้จะซิงโครไนส์ข้อมูลหลักของลูกค้าสำหรับลูกค้าเชิงพาณิชย์และเชิงองค์กรระหว่างแอพลิเคชัน Finance and Operations และ Common Data Service

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | name
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | คำอธิบาย
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid. msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | ไม่มี
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
ไม่มี | \>\> | address1\_addresstypecode
ไม่มี | \>\> | customertypecode
PARTYTYPE | \<\< | ไม่มี
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>ลูกค้า V3 ไปยังผู้ติดต่อ

เท็มเพลตนี้ซิงโครไนส์ข้อมูลหลักของลูกค้าสำหรับผู้บริโภคและผู้ใช้ระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
ไม่มี | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | ไม่มี
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid. msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | ไม่มี
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | ไม่มี
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
ไม่มี | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
ไม่มี | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
ไม่มี | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | โทรศัพท์ 1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | คำอธิบาย

## <a name="contacts"></a>ผู้ติดต่อ

เท็มเพลตนี้จะซิงโครไนส์ข้อมูลการติดต่อหลัก รอง และลำดับสามทั้งหมด สำหรับทั้งลูกค้าและผู้จัดจำหน่าย ระหว่าง Finance and Operations และแอปพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-contacts.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | ไม่มี
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | แผนก
บันทึกย่อ | = | คำอธิบาย
เพศ | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
ไม่มี | \>\> | msdyn\_contactforvendor
ไม่มี | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>กลุ่มลูกค้า

เท็มเพลตนี้ซิงโครไนส์ข้อมูลกลุ่มลูกค้าระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-customer-groups.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
คำอธิบาย | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>วิธีการชำระเงินของลูกค้า

เท็มเพลตนี้ซิงโครไนส์ข้อมูลการชำระเงินของลูกค้าระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-customer-payment-methods.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
ชื่อ | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
คำอธิบาย | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>บัตรสมาชิก

เท็มเพลตนี้ซิงโครไนส์ข้อมูลบัตรสมาชิกของลูกค้าระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-loyalty-cards.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>กำหนดการชำระเงิน

เท็มเพลตนี้ซิงโครไนส์ข้อมูลอ้างอิงกำหนดการชำระเงิน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย ระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-payment-schedules.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
ชื่อ | = | msdyn\_name
คำอธิบาย | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
บันทึกย่อ | = | msdyn\_note

## <a name="payment-schedule-lines"></a>รายการกำหนดการชำระเงิน

ซิงโครไนส์รายการข้อมูลอ้างอิงกำหนดการชำระเงิน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย ระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>จำนวนวันการชำระเงิน

เท็มเพลตนี้ซิงโครไนส์ข้อมูลอ้างอิงวันที่การชำระเงิน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย ระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-payment-days.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
ชื่อ | = | msdyn\_name
คำอธิบาย | = | msdyn\_description

## <a name="payment-day-lines"></a>รายการแสดงวันที่ชำระเงิน

เท็มเพลตนี้ซิงโครไนส์ข้อมูลอ้างอิงวันที่ชำระเงิน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย ระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-payment-day-lines.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
ความถี่ | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
ชื่อ | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>เงื่อนไขการชำระเงิน

เท็มเพลตนี้ซิงโครไนส์ข้อมูลอ้างอิงเงื่อนไขการชำระเงิน (เงื่อนไขของการชำระเงิน) สำหรับทั้งลูกค้าและผู้จัดจำหน่าย ระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-payment-terms.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
คำอธิบาย | = | msdyn\_description
ชื่อ | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>ส่วนเพิ่มของชื่อ

เท็มเพลตนี้ซิงโครไนส์ข้อมูลอ้างอิงส่วนเพิ่มเติมของชื่อ สำหรับทั้งลูกค้าและผู้จัดจำหน่าย ระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![](media/dual-write-name-affixes.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
ส่วนผนวก | = | msdyn\_affix
ชนิด | \>\< | msdyn\_affixtype
คำอธิบาย | = | msdyn\_description
