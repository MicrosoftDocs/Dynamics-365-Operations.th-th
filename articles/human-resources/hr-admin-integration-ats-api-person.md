---
title: บุคคล
description: หัวข้อนี้อธิบายเอนทิตี้ส่วนบุคคลสำหรับ Dynamics 365 Human Resources
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e61b768c5194b52178853d48c50dbf072eebbdcd
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125460"
---
# <a name="person"></a>บุคคล

หัวข้อนี้อธิบายเอนทิตี้ส่วนบุคคลสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_dirpersonentity

### <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะให้ข้อมูลส่วนบุคคลสำหรับบุคคลที่เป็นผู้สมัคร

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ส่วนบุคคล**<br>mshr_dirpersonentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดเอนทิตี้ |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ตัวระบุเฉพาะที่ระบบสร้างขึ้นและผู้ใช้สามารถอ่านได้สำหรับบุคคล  |
| **ชื่อ**<br>mshr_name<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ค่าฟิลด์คือการเรียงต่อกันของชื่อ ชื่อกลาง คำเสริมหน้านามสกุล และนามสกุล ในลำดับที่กําหนดในฟิลด์ **แสดงลำดับชื่อเป็น** |
| **นามแฝงของชื่อ**<br>mshr_namealias<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | นามแฝงของชื่อที่สามารถให้ไว้ของบุคคล |
| **เรียกว่า**<br>mshr_knownas<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ชื่อที่สามารถใช้กับบุคคลได้ถ้าโดยทั่วไปเรียกอีกชื่อหนึ่ง |
| **รหัสภาษา**<br>mshr_languageid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัสภาษาของภาษาหลักของบุคคลตามที่กําหนดในรูปแบบ ISO 639-1 |
| **สมุดที่อยู่**<br>mshr_addressbooks<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | สมุดที่อยู่ที่บุคคลอาจจะถูกกำหนด สมุดที่อยู่ที่ตั้งค่าไว้ให้กับองค์กรจะแสดงรายการอยู่ในเอนทิตี้ mshr_diraddressbooksentity |
| **วันครบรอบปี**<br>mshr_anniversaryday<br>*Int* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันของวันที่ครบรอบปีของบุคคล |
| **เดือนที่ครบรอบปี**<br>mshr_anniversarymonth<br>*การกำหนดตัวเลือก mshr_monthsofyear* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เดือนของวันที่ครบรอบปีของบุคคล |
| **ปีที่ครบรอบ**<br>mshr_anniversaryyear<br>*Int* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ปีของวันที่ครบรอบปีของบุคคล |
| **วันเกิด**<br>mshr_birthday<br>*Int* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันของวันเกิดของบุคคล |
| **เดือนเกิด**<br>mshr_birthmonth<br>*การกำหนดตัวเลือก mshr_monthsofyear* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เดือนของวันเกิดของบุคคล |
| **ปีเกิด**<br>mshr_birthyear<br>*Int* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ปีของวันเกิดของบุคคล |
| **ชื่อบุตร**<br>mshr_childrennames<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | สตริงสำหรับชื่อของบุตรของบุคคล ไม่มีการกำหนดเขตที่จำเป็น |
| **เพศ**<br>mshr_gender<br>*การกำหนดตัวเลือก mshr_hcmpersongender* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เพศของบุคคล |
| **งานอดิเรก**<br>mshr_hobbies<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | งานอดิเรกของบุคคล |
| **ชื่อย่อ**<br>mshr_initials<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำนำหน้าของชื่อของบุคคล |
| **สถานภาพการสมรส**<br>mshr_maritalstatus<br>*การกำหนดตัวเลือก mshr_hcmpersonmaritalstatus* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | สถานภาพการสมรสของบุคคล |
| **ชื่อตามสัทศาสตร์**<br>mshr_phoneticfirstname<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | การออกเสียงตามสัทศาสตร์ของชื่อบุคคล |
| **นามสกุลตามสัทศาสตร์**<br>mshr_phoneticlastname<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | การออกเสียงตามสัทศาสตร์ของนามสกุลบุคคล |
| **ชื่อกลางตามสัทศาสตร์**<br>mshr_phoneticmiddlename<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | การออกเสียงตามสัทศาสตร์ของนามสกุลบุคคล |
| **คำต่อท้ายบุคคล**<br>mshr_personalsuffix<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ชื่อต่อท้ายบุคคลของบุคคล ค่าที่มีผลบังคับใช้ในเอนทิตี้ mshr_dirnameaffixentity ที่ mshr_type เป็นคำต่อท้าย (200000001) |
| **คำนำหน้าชื่อของบุคคล**<br>mshr_personaltitle<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำนำหน้าชื่อของบุคคลสำหรับบุคคล ค่าที่มีผลบังคับใช้ในเอนทิตี้ mshr_dirnameaffixentity ที่ mshr_type เป็นคำนำหน้า (200000000)
| **คำต่อท้ายวิชาชีพ**<br>mshr_professionalsuffix<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำต่อท้ายวิชาชีพ |
| **คำนำหน้าวิชาชีพ**<br>mshr_professionaltitle<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำนำหน้าวิชาชีพ |
| **ที่อยู่หลักเต็มรูปแบบ**<br>mshr_fullprimaryaddress<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ที่อยู่หลักเต็มรูปแบบของบุคคล การเรียงต่อกันของฟิลด์ที่อยู่หลัก |
| **เมืองในที่อยู่**<br>mshr_addresscity<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เมืองของที่อยู่หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticsaddresscityentity |
| **ที่อยู่ ประเทศ ภูมิภาค**<br>mshr_addresscountryregionid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ประเทศ/ภูมิภาคของที่อยู่หลักของบุคคล ค่าที่มีผลบังคับใช้ในเอนทิตี้ mshr_logisticsaddresscountryregionentity |
| **รหัส ISO ที่อยู่ ประเทศ ภูมิภาค**<br>mshr_addresscountryregionisocode<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัส ISO ของประเทศของที่อยู่หลักของบุคคล |
| **ที่อยู่ ประเทศ**<br>mshr_addresscounty<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ประเทศของที่อยู่หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticsaddresscountyentity |
| **ที่อยู่ เขต ชื่อ**<br>mshr_addressdistrictname<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เขตของที่อยู่หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticsaddressdistrictentity |
| **ที่อยู๋ ละติจูด**<br>mshr_addresslatitude<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ละติจูดของที่อยู่หลักของบุคคล |
| **ที่อยู่ สถานที่ รหัส**<br>mshr_addresslocationid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ตัวระบุเฉพาะของสถานที่ของที่อยู่หลักของบุคคล ค่าที่มีผลบังคับใช้ในเอนทิตี้ mshr_logisticspostaladdresslocationcdsentity |
| **ที่อยู่ สถานที่ บทบาท**<br>mshr_addresslocationroles<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | บทบาทสถานที่ของที่อยู่หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticspostaladdresslocationcdsentity |
| **ที่อยู่ ลองติจูด**<br>mshr_addresslongitude<br>*สตริง* |  อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ลองติจูดของที่อยู่หลักของบุคคล |
| **ที่อยู่ สถานะ**<br>mshr_addressstate<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | สถานะของที่อยู่หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticsaddressstateentity |
| **ที่อยู่ ถนน**<br>mshr_addressstreet<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ที่อยู่ถนนของที่อยู่หลักของบุคคล |
| **ที่อยู่มีผลตั้งแต่**<br>mshr_addressvalidfrom<br>*วัน เดือน* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่อยู่หลักของบุคคลเริ่มต้นการมีผลบังคับใช้ |
| **ที่อยู่มีผลบังคับใช้ไปยัง**<br>mshr_addressvalidto<br>*วัน เดือน* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่อยู่หลักของบุคคลเริ่มต้นการมีผลบังคับใช้ |
| **ที่อยู่ รหัสไปรษณีย์**<br>mshr_addresszipcode<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัสไปรษณีย์ของที่อยู่หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticsaddresspostalcodeentity |
| **ที่อยู่เป็นแบบส่วนตัว**<br>mshr_addressisprivate<br>*ตัวเลือกการตั้งค่า mshr_noyes* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | กำหนดว่าที่อยู่หลักของบุคคลใช้ร่วมกันกับที่อยู่อื่นๆในองค์กรหรือไม่ |
| **คำอธิบายที่อยู่**<br>mshr_addressdescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายสำหรับที่อยู่หลักของบุคคล |
| **อีเมลผู้ติดต่อหลัก**<br>mshr_primarycontactemail<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ที่อยู่อีเมลหลักของบุคคล |
| **คำอธิบายอีเมลผู้ติดต่อหลัก**<br>mshr_primarycontactemaildescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายที่ระบุให้กับที่อยู่อีเมลหลัก |
| **อีเมลผู้ติดต่อหลักเป็น IM**<br>mshr_primarycontactemailisim<br>*ตัวเลือกการตั้งค่า mshr_noyes* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | กำหนดว่าที่อยู่อีเมลหลักจะพร้อมใช้งานในข้อความโต้ตอบแบบทันทีหรือไม่ |
| **จุดประสงค์อีเมลผู้ติดต่อหลัก**<br>mshr_primarycontactemailpurpose<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดประสงค์สำหรับที่อยู่อีเมลหลัก ตั้งค่าในเอนทิตี้ mshr_logisticslocationroleentity |
| **โทรสารผู้ติดต่อหลัก**<br>mshr_primarycontactfax<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขโทรสารหลัก |
| **คำอธิบายโทรสารผู้ติดต่อหลัก**<br>mshr_primarycontactfaxdescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายที่ระบุให้กับหมายเลขโทรสารหลัก |
| **เบอร์ต่อโทรสารผู้ติดต่อหลัก**<br>mshr_primarycontactfaxextension<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เบอร์ต่อของหมายเลขโทรสารหลัก |
| **จุดประสงค์โทรสารผู้ติดต่อหลัก**<br>mshr_primarycontactfaxpurpose<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดประสงค์สำหรับหมายเลขโทรสารหลัก ตั้งค่าในเอนทิตี้ mshr_logisticslocationroleentity
| **โทรศัพท์ผู้ติดต่อหลัก**<br>mshr_primarycontactphone<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขโทรศัพท์หลัก |
| **คำอธิบายโทรศัพท์ผู้ติดต่อหลัก**<br>mshr_primarycontactphonedescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายที่ระบุให้กับหมายเลขโทรศัพท์หลัก |
| **เบอร์ต่อโทรศัพท์ผู้ติดต่อหลัก**<br>mshr_primarycontactphoneextension<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เบอร์ต่อของหมายเลขโทรศัพท์หลัก |
| **โทรศัพท์ผู้ติดต่อหลักเป็นอุปกรณ์เคลื่อนที่**<br>mshr_primarycontactphoneismobile<br>*ตัวเลือกการตั้งค่า mshr_noyes* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | กำหนดว่าหมายเลขโทรศัพท์หลักเป็นอุปกรณ์เคลื่อนที่หรือไม่ |
| **จุดประสงค์โทรศัพท์ผู้ติดต่อหลัก**<br>mshr_primarycontactphonepurpose<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดประสงค์สำหรับหมายเลขโทรศัพท์หลัก ตั้งค่าในเอนทิตี้ mshr_logisticslocationroleentity |
| **เทเล็กซ์ผู้ติดต่อหลัก**<br>mshr_primarycontacttelex<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขเทเล็กซ์หลัก |
| **คำอธิบายเทเล็กซ์ผู้ติดต่อหลัก**<br>mshr_primarycontacttelexdescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายที่ระบุให้กับหมายเลขเทเล็กซ์หลักของบุคคล |
| **จุดประสงค์เทเล็กซ์ผู้ติดต่อหลัก**<br>mshr_primarycontacttelexpurpose<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดประสงค์ของหมายเลขเทเล็กซ์หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticslocationroleentity |
| **URL ผู้ติดต่อหลัก**<br>mshr_primarycontacturl<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | URL หลัก |
| **คำอธิบาย URL ผู้ติดต่อหลัก**<br>mshr_primarycontacturldescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายที่ให้สำหรับ URL หลักของบุคคล |
| **จุดประสงค์ URL ผู้ติดต่อหลัก**<br>mshr_primarycontacturldescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดประสงค์สำหรับ URL หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticslocationroleentity |
| **ผู้ต่อติดหลัก Facebook**<br>mshr_primarycontactfacebook<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | บัญชี Facebook หลัก ระบุโดยรหัสผู้ใช้ |
| **ผู้ติดต่อหลัก Facebook คำอธิบาย**<br>mshr_primarycontactfacebookdescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายที่ให้บัญชี Facebook หลักของบุคคล |
| **Facebook ผู้ติดต่อหลักเป็นแบบส่วนตัว**<br>mshr_primarycontactfacebookisprivate<br>*ตัวเลือกการตั้งค่า mshr_noyes* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | กำหนดว่าบัญชี Facebook หลักจะมองเห็นได้โดยผู้ใช้อื่นๆหรือไม่ |
| **จุดประสงค์ Facebook ผู้ติดต่อหลัก**<br>mshr_primarycontactfacebookpurpose<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดประสงค์สำหรับบัญชี Facebook หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticslocationroleentity |
| **LinkedIn ผู้ติดต่อหลัก**<br>mshr_primarycontactlinkedin<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | บัญชี LinkedIn หลัก ระบุโดยชื่อผู้ใช้ |
| **คำอธิบาย LinkedIn ผู้ติดต่อหลัก**<br>mshr_primarycontactlinkedindescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายที่ให้สำหรับบัญชี LinkedIn หลักของบุคคล |
| **LinkedIn ผู้ติดต่อหลักเป็นแบบส่วนตัว** <br>mshr_primarycontactlinkedinisprivate<br>*ตัวเลือกการตั้งค่า mshr_noyes* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | กำหนดว่าข้อมูลบัญชีหลัก LinkedIn หลักของบุคคลใช้ร่วมกันกับบัญชีอื่นๆในองค์กรหรือไม่ |
| **จุดประสงค์ LinkedIn ผู้ติดต่อหลัก**<br>mshr_primarycontactlinkedinpurpose<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดประสงค์สำหรับบัญชี LinkedIn หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticslocationroleentity |
| **Twitter ผู้ติดต่อหลัก**<br>mshr_primarycontacttwitter<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | บัญชี Twitter หลักของบุคคล ระบุโดย @username |
| **คำอธิบาย Twitter ผู้ติดต่อหลัก**<br>mshr_primarycontacttwitterdescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายที่ให้สำหรับบัญชี Twitter หลักของบุคคล |
| **Twitter ผู้ติดต่อหลักเป็นแบบส่วนตัว** <br>mshr_primarycontacttwitterisprivate<br>*ตัวเลือกการตั้งค่า mshr_noyes* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | กำหนดว่าข้อมูลบัญชี Twitter หลักของบุคคลใช้ร่วมกันกับบัญชีอื่นๆในองค์กรหรือไม่ |
| **จุดประสงค์ Twitter ผู้ติดต่อหลัก**<br>mshr_primarycontacttwitterpurpose<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดประสงค์สำหรับบัญชี Twitter หลักของบุคคล ตั้งค่าในเอนทิตี้ mshr_logisticslocationroleentity |
| **ชนิดฝ่าย**<br>mshr_partytype<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ชนิดฝ่ายของบุคคล จะเป็น **บุคคล** เสมอสำหรับผู้สมัคร |
| **แสดงผลลำดับชื่อเป็น**<br>mshr_namesequencedisplayas<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ลำดับที่คุณสมบัติชื่อของบุคคลรวมอยู่จากค่าคุณสมบัติชื่อ (mshr_name) |
| **ชื่อ**<br>mshr_firstname<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ชื่อของบุคคล |
| **ชื่อกลาง**<br>mshr_middlename<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ชื่อกลางของบุคคล |
| **คำนำหน้านามสกุล**<br>mshr_lastnameprefix<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำนําหน้านามสกุลของบุคคล |
| **นามสกุล**<br>mshr_lastname<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | นามสกุลของบุคคล |
| **รหัสที่ตั้งทางอิเล็กทรอนิกส์**<br>mshr_electroniclocationid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัสของที่ตั้งทางอิเล็กทรอนิกส์ของบุคคล |
| **โซนเวลาที่อยู่**<br>mshr_addresstimezone<br>*Int* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | โซนเวลาของที่อยู่หลักของบุคคล |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

