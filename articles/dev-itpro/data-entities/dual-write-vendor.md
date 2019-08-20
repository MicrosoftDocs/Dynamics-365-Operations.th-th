---
title: ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม
description: หัวข้อนี้อธิบายการรวมข้อมูลของผู้จัดจำหน่ายระหว่าง Finance and Operations และ Common Data Service
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
ms.openlocfilehash: 45808bc35aba04df6fcaf6b1cbfcc2461b0b65cb
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789250"
---
## <a name="integrated-vendor-master"></a>ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

คำว่า *ผู้จัดจำหน่าย* หมายถึงองค์กรของซัพพลายเออร์หรือเจ้าของแต่ละรายที่เป็นส่วนหนึ่งของกระบวนการห่วงโซ่อุปทาน และที่จัดหาสินค้าสำหรับธุรกิจ แม้ว่า *ผู้จัดจำหน่าย* เป็นแนวคิดที่สร้างขึ้นใน Microsoft Dynamics 365 for Finance and Operations แนวคิดของผู้จัดจำหน่ายไม่มีอยู่ใน Dynamics 365 for Customer Engagement แต่บางธุรกิจจะโอเวอร์โหลดเอนทิตีบัญชีเพื่อจัดเก็บทั้งข้อมูลลูกค้าและข้อมูลผู้จัดจำหน่าย ธุรกิจอื่นๆ ใช้แนวคิดของผู้จัดจำหน่ายที่กำหนดเอง การรวม Common Data Service สนับสนุนการออกแบบเหล่านี้ทั้งสองรายการ ดังนั้น คุณจึงสามารถเปิดใช้งานการออกแบบแบบใดแบบหนึ่ง โดยขึ้นอยู่กับสถานการณ์จำลองทางธุรกิจของคุณ

การรวมของข้อมูลผู้จัดจำหน่ายระหว่าง Finance and Operations และ Customer Engagement จะช่วยให้คุณสามารถมีข้อมูลหลักหลายรายการ โดยไม่คำนึงถึงจุดกำเนิดของข้อมูลของผู้จัดจำหน่าย จะมีการรวมอยู่เบื้องหลังในขอบเขตของแอพลิเคชันและความแตกต่างของโครงสร้างพื้นฐาน 

### <a name="vendor-data-flow"></a>โฟลว์ข้อมูลของผู้จัดจำหน่าย

ถ้าคุณต้องการใช้ Customer Engagement สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการแยกข้อมูลผู้จัดจำหน่ายออกจากข้อมูลลูกค้า คุณสามารถใช้การออกแบบผู้จัดจำหน่ายใหม่ได้

![โฟลว์ข้อมูลของผู้จัดจำหน่าย](media/dual-write-vendor-data-flow.png)

ถ้าคุณต้องการใช้ Customer Engagement สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการใช้เอนทิตีบัญชีต่อเพื่อจัดเก็บข้อมูลผู้จัดจำหน่าย คุณสามารถใช้การออกแบบผู้จัดจำหน่ายแบบขยายใหม่ได้ ในการออกแบบนี้ ข้อมูลผู้จัดจำหน่ายแบบขยาย เช่น กลุ่มผู้จัดจำหน่าย และโพรไฟล์การลงบัญชีผู้จัดจำหน่าย จะถูกเก็บไว้ในรายละเอียดผู้จัดจำหน่าย

![โฟลว์ข้อมูลของผู้จัดจำหน่ายแบบขยาย](media/dual-write-vendor-detail.jpg)

ข้อมูลการติดต่อของผู้จัดจำหน่ายคล้ายกับข้อมูลการติดต่อของลูกค้า ในเบื้องหลัง ข้อมูลของผู้ติดต่อจะถูกเก็บและถูกดึงมาจากเอนทิตีเดียวกัน

## <a name="templates"></a>เท็มเพลต

ข้อมูลผู้จัดจำหน่ายรวมถึงข้อมูลทั้งหมดเกี่ยวกับผู้จัดจำหน่าย เช่น กลุ่มผู้จัดจำหน่าย ที่อยู่ ข้อมูลผู้ติดต่อ โพรไฟล์การชำระเงิน และโพรไฟล์ใบแจ้งหนี้ ชุดของแผนผังเอนทิตีทำงานร่วมกันในระหว่างการโต้ตอบข้อมูลผู้จัดจำหน่าย ดังที่แสดงในตารางต่อไปนี้

Finance and Operations  | แอพลิเคชัน Customer Engagement
------------------------|---------------------------------
ผู้จัดจำหน่าย V2               | บัญชี
ผู้จัดจำหน่าย V2               | Msdyn\_vendors
ผู้ติดต่อ CDS V2         | ผู้ติดต่อ
กลุ่มผู้จัดจำหน่าย           | Msdyn\_vendorgroups
วิธีการชำระเงินของผู้จัดจำหน่าย   | Msdyn\_vendorpaymentmethods
กำหนดการชำระเงิน        | Msdyn\_paymentschedules
กำหนดการชำระเงิน        | Msdyn\_paymentschedulelines
CDS วันที่ชำระเงิน         | Msdyn\_paymentdays
CDS รายการแสดงวันที่ชำระเงิน   | Msdyn\_paymentdaylines
เงื่อนไขการชำระเงิน        | Msdyn\_paymentterms
ส่วนเพิ่มของชื่อ            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>ผู้จัดจำหน่าย V2 และบัญชี 

ธุรกิจที่ใช้เอนทิตีบัญชีเพื่อจัดเก็บข้อมูลผู้จัดจำหน่ายสามารถใช้ต่อไปได้ในลักษณะเดียวกัน นอกจากนี้ ยังสามารถใช้ประโยชน์จากฟังก์ชันของผู้จัดจำหน่ายที่ชัดเจนซึ่งกำลังจะมา เนื่องจากการรวมของ Finance and Operations

## <a name="vendor-v2-and-msdyn_vendors"></a>ผู้จัดจำหน่าย V2 และ Msdyn\_vendors

ธุรกิจที่ใช้โซลูชันแบบกำหนดเองสำหรับผู้จัดจำหน่ายสามารถใช้ประโยชน์จากแนวคิดผู้จัดจำหน่ายแบบสำเร็จรูปที่ถูกนำมาใช้ใน Common Data Service เนื่องจากการรวมของ Finance and Operations 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>ผู้ติดต่อ

เท็มเพลตนี้จะซิงโครไนส์ข้อมูลการติดต่อหลัก รอง และลำดับสามทั้งหมด สำหรับทั้งลูกค้าและผู้จัดจำหน่าย ระหว่าง Finance and Operations และ Customer Engagement สำหรับรายละเอียดของแผนผังเอนทิตี ให้ดูที่ [รายการหลักของลูกค้าแบบรวม](dual-write-customer.md#contacts)

## <a name="vendor-groups"></a>กลุ่มผู้จัดจำหน่าย

เท็มเพลตนี้ซิงโครไนส์ข้อมูลกลุ่มผู้จัดจำหน่ายระหว่าง Finance and Operations และ Customer Engagement

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
คำอธิบาย | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>วิธีการชำระเงินของผู้จัดจำหน่าย

เท็มเพลตนี้ซิงโครไนส์ข้อมูลวิธีชำระเงินของผู้จัดจำหน่ายระหว่าง Finance and Operations และ Customer Engagement

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
ชื่อ | = | msdyn\_name
คำอธิบาย | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

