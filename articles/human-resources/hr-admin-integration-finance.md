---
title: ตั้งค่าคอนฟิกการรวมกับการเงิน
description: บทความนี้อธิบายถึงฟังก์ชันที่พร้อมใช้งานสำหรับการรวมจาก Dynamics 365 Human Resources และ Dynamics 365 Finance
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e7070f627654c9eb889f3e0ee27e37681db0502
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010703"
---
# <a name="configure-integration-with-finance"></a>ตั้งค่าคอนฟิกการรวมกับการเงิน

บทความนี้อธิบายถึงฟังก์ชันที่พร้อมใช้งานสำหรับการรวมจาก Dynamics 365 Human Resources และ Dynamics 365 Finance ทรัพยากรบุคคลไปยังเท็มเพลตการเงินที่พร้อมใช้งานกับ [ตัวรวมข้อมูล](https://docs.microsoft.com/powerapps/administrator/data-integrator) จะช่วยให้โฟลว์ของข้อมูลสำหรับงาน ตำแหน่งงาน และผู้ปฏิบัติงาน ใช้งานได้ โฟลว์ข้อมูลจากทรัพยากรบุคคลไปยังการเงิน เท็มเพลตไม่มีความสามารถในการทำให้ข้อมูลย้อนกลับจากการเงินไปยังทรัพยากรบุคคล 

![ทรัพยากรบุคคลไปยังโฟลว์การรวมทางการเงิน](./media/TalentFinOpsFlow.png)

ทรัพยากรบุคคลไปยังโซลูชันการเงินมีชนิดของการซิงโครไนส์ข้อมูลต่อไปนี้ 

- รักษางานในทรัพยากรบุคคลและซิงค์จากทรัพยากรบุคคลไปยังการเงิน
- รักษาตำแหน่งงานและการมอบหมายตำแหน่งงานในทรัพยากรบุคคลและซิงค์จากทรัพยากรบุคคลไปยังการเงิน
- รักษาการจ้างงานในทรัพยากรบุคคลและซิงค์จากทรัพยากรบุคคลไปยังการเงิน
- รักษาผู้ปฏิบัติงานและที่อยู่ผู้ปฏิบัติงานในทรัพยากรบุคคล และซิงค์จากทรัพยากรบุคคลไปยังการเงิน

## <a name="system-requirements-for-human-resources"></a>ความต้องการของระบบสำหรับทรัพยากรบุคคล
โซลูชันการรวมจำเป็นต้องใช้ทรัพยากรบุคคลและการเงินรุ่นต่อไปนี้: 
- Dynamics 365 Human Resources บน Common Data Service
- Dynamics 365 Finance รุ่น 7.2 และรุ่นใหม่กว่า

## <a name="template-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงเท็มเพลต ให้ดำเนินการต่อไปนี้
1. เปิด [Power Apps ศูนย์การจัดการ](https://admin.powerapps.com/) 
1. เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ โครงการใหม่จะต้องมีการสร้างขึ้นสำหรับแต่ละนิติบุคคลที่คุณต้องการรวมเข้าไปในการเงิน

เท็มเพลตต่อไปนี้จะใช้ในการซิงโครไนส์เรกคอร์ดจากทรัพยากรบุคคลไปยังการเงิน

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** ทรัพยากรบุคคล (ทรัพยากรบุคคล Common Data Service ไปยังการเงิน)

  > [!NOTE]
  > ชื่อของงานประกอบด้วยเอนทิตีที่ใช้ในแต่ละแอปพลิเคชัน ต้นทาง (ทรัพยากรบุคคล) อยู่ทางด้านซ้ายและปลายทาง (Finance and Operations) อยู่ทางด้านขวา

งานพื้นฐานต่อไปนี้จะใช้ในการซิงโครไนส์เรกคอร์ดจากทรัพยากรบุคคลไปยังการเงิน
- ฟังก์ชันงานสำหรับฟังก์ชันงานค่าตอบแทน
- แผนกไปยังหน่วยปฏิบัติงาน
- ชนิดงานไปยังชนิดงานค่าตอบแทน
- งานไปยังงาน
- งานไปยังรายละเอียดงาน
- ชนิดของตำแหน่งไปยังชนิดของตำแหน่ง
- ตำแหน่งงานไปยังตำแหน่งฐาน
- ตำแหน่งงานไปยังรายละเอียดตำแหน่ง
- ตำแหน่งงานไปยังช่วงเวลาของตำแหน่ง
- ตำแหน่งงานไปยังลำดับชั้นของตำแหน่ง
- ผู้ปฏิบัติงานไปยังผู้ปฏิบัติงาน
- การจ้างงานไปยังการจ้างงาน
- การจ้างงานไปยังรายละเอียดการจ้างงาน
- การมอบหมายผู้ปฏิบัติงานของตำแหน่งไปยังการมอบหมายผู้ปฏิบัติงานของตำแหน่ง
- ที่อยู่ของผู้ปฏิบัติงานไปยังที่อยู่ทางไปรษณีย์ของผู้ปฏิบัติงาน V2

## <a name="template-mappings"></a>การแม็ปเท็มเพลต

### <a name="job-functions-to-compensation-job-function"></a>ฟังก์ชันงานสำหรับฟังก์ชันงานค่าตอบแทน

| เอนทิตี (แหล่งที่มา) Common Data Service                 | เอนทิตี (ปลายทาง) Finance and Operations |
|-------------------------------------|---------------------------------------------|
| cdm_name (ชื่อฟังก์ชัน cdm_Job)  | JOBFUNCTIONID (JOBFUNCTIONID)            |
| cdm_description (cdm_description) | คำอธิบาย (คำอธิบาย)                 |

### <a name="departments-to-operating-unit"></a>แผนกไปยังหน่วยปฏิบัติงาน

| เอนทิตี (แหล่งที่มา) Common Data Service                           | เอนทิตี (ปลายทาง) Finance and Operations |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | ชื่อ (ชื่อ)                                 |
| cdm_departmentnumber (cdm_departmentnumber) | OPERATINGUNITNUMBER (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE (OPERATINGUNITTYPE)     |
| cdm_description (cdm_description)           | NAMEALIAS (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>ชนิดงานไปยังชนิดงานค่าตอบแทน

| เอนทิตี (แหล่งที่มา) Common Data Service                   | เอนทิตี (ปลายทาง) Finance and Operations |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID (JOBTYPEID)                     |
| cdm_description (cdm_description)   | คำอธิบาย (คำอธิบาย)                 |
| cdm_exemptstatus (cdm_exemptstatus) | EXEMPTSTATUS (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>งานไปยังงาน

| เอนทิตี (แหล่งที่มา) Common Data Service                                           | เอนทิตี (ปลายทาง) Finance and Operations           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description (cdm_description)                           | คำอธิบาย (คำอธิบาย)                           |
| cdm_jobdescription (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>งานไปยังรายละเอียดงาน

| เอนทิตี (แหล่งที่มา) Common Data Service                                             | เอนทิตี (ปลายทาง) Finance and Operations |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid cdm_name (ชนิดงาน (ชื่อชนิดงาน))             | JOBTYPEID (JOBTYPEID)                     |
| cdm_jobfunctionid cdm_name (ฟังก์ชันงาน (ชื่องานของฟังก์ชันงาน)) | FUNCTIONID (FUCNTIONID)                   |
| cdm_validfrom (มีผลบังคับใช้ตั้งแต่)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (มีผลบังคับใช้ถึง)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent (จำนวนเทียบเท่าเต็มเวลาเริ่มต้น)   | FULLTIMEEQUIVALENT (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>ชนิดของตำแหน่งไปยังชนิดของตำแหน่ง

| เอนทิตี (แหล่งที่มา) Common Data Service                       | เอนทิตี (ปลายทาง) Finance and Operations |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID (POSITIONTYPEID)           |
| cdm_description (cdm_description)       | คำอธิบาย (คำอธิบาย)                 |
| cdm_classification (cdm_classification) | CLASSIFICATION (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>ตำแหน่งงานไปยังตำแหน่งฐาน

| เอนทิตี (แหล่งที่มา) Common Data Service                           | เอนทิตี (ปลายทาง) Finance and Operations |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>ตำแหน่งงานไปยังรายละเอียดตำแหน่ง

| เอนทิตี (แหล่งที่มา) Common Data Service                                                      | เอนทิตี (ปลายทาง) Finance and Operations       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name (งาน (ชื่อ))                                        | JOBID (JOBID)                                    |
| cdm_description (cdm_description)                                        | คำอธิบาย (คำอธิบาย)                       |
| cdm_departmentid cdm_departmentnumber (แผนก (หมายเลขแผนก)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid cdm_name (ชนิดของตำแหน่ง (ชื่อ))                     | POSITIONTYPEID (POSITIONTYPEID)                 |
| cdm_avaialableforassignment (มีให้สำหรับการมอบหมาย)                 | AVAILABLEFORASSIGNMENT (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom (มีผลบังคับใช้ตั้งแต่)                                            | VALIDFROM (VALIDFROM)                           |
| cdm_validto (มีผลบังคับใช้ถึง)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent (จำนวนเทียบเท่าเต็มเวลา)                           | FULLTIMEEQUIVALENT (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>ตำแหน่งงานไปยังช่วงเวลาของตำแหน่ง

| เอนทิตี (แหล่งที่มา) Common Data Service                             | เอนทิตี (ปลายทาง) Finance and Operations |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน)   | POSITIONID (POSITIONID)                      |
| การเรียกใช้ที่คำนวณได้ (การเรียกใช้ที่คำนวณได้) | VALIDFROM (VALIDFROM)                        |
| การเกษียณอายุที่คำนวณได้ (การเกษียณอายุที่คำนวณได้) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hiearchies"></a>ตำแหน่งงานไปยังลำดับชั้นของตำแหน่ง

| เอนทิตี (แหล่งที่มา) Common Data Service                                                                           | เอนทิตี (ปลายทาง) Finance and Operations |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน)                                                 | POSITIONID (POSITIONID)                      |
| cdm_parentjobpositionid cdmjobpositionnumber (cdm_parentjobpositionid cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom (มีผลบังคับใช้ตั้งแต่)                                                                  | VALIDFROM (VALIDFROM)                     |
| cdm_validto (มีผลบังคับใช้ถึง)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>ผู้ปฏิบัติงานไปยังผู้ปฏิบัติงาน
| เอนทิตี (แหล่งที่มา) Common Data Service                           | เอนทิตี (ปลายทาง) Finance and Operations       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate (cdm_birthdate)               | BIRTHDATE (BIRTHDATE)                           |
| cdm_gender (cdm_gender)                     | เพศ (เพศ)                                   |
| cdm_primaryaddress (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone (cdm_primarytelephone) | PRIMARYCONTACTPHONE (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl (cdm_websiteurl)             | PRIMARYCONTACTURL (PRIMARYCONTACTURL)           |
| cdm_firstname (cdm_firstname)               | FIRSTNAME (FIRSTNAME)                           |
| cdm_middlename (cdm_middlename)             | MIDDLENAME (MIDDLENAME)                         |
| cdm_lastname (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber (cdm_workernumber)         | PERSONNELNUMBER (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE (WORKERTYPE)                         |
| cdm_state (cdm_state)                       | WORKSTATUS (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>การจ้างงานไปยังการจ้างงาน

| เอนทิตี (แหล่งที่มา) Common Data Service                                             | เอนทิตี (ปลายทาง) Finance and Operations |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE (EMPLOYMENTSTARTDATE) |
| cdm_employmentstartdate (cdm_employmentstartdate)                 | EMPLOYMENTENDDATE (EMPLOYMENTENDDATE)     |
| cdm_workertype (cdm_workertype)                               | WORKERTYPE (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode (cdm_companyid.cdm_companycode) | LEGALENTITYID (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>การจ้างงานไปยังรายละเอียดการจ้างงาน

| เอนทิตี (แหล่งที่มา) Common Data Service                                             | เอนทิตี (ปลายทาง) Finance and Operations   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE (EMPLOYMENTSTARTDATE)   |
| cdm_employmentstartdate (cdm_employmentstartdate)                 | EMPLOYMENTENDDATE (EMPLOYMENTENDDATE)       |
| cdm_validfrom (มีผลบังคับใช้ตั้งแต่)                                    | VALIDFROM (VALIDFROM)                       |
| cdm_validto (มีผลบังคับใช้ถึง)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate (cdm_workerstartdate)                     | WORKERSTARTDATE (WORKERSTARTDATE)           |
| cdm_lastdateworked (cdm_lastdateworked)                       | LASTDATEWORKED (LASTDATEWORKED)             |
| cdm_transitiondate (cdm_transitiondate)                       | TRANSITIONDATE (TRANSITIONDATE)             |
| cdm_employerunitofnotice (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode (cdm_companyid.cdm_companycode) | LEGALENTITYID (LEGALENTITYID)               |
| cdm_employernoticeamount (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount (cdm_workernoticeamount)              | WORKERNOTICEAMOUNT (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>การมอบหมายผู้ปฏิบัติงานของตำแหน่งไปยังการมอบหมายผู้ปฏิบัติงานของตำแหน่ง

| เอนทิตี (แหล่งที่มา) Common Data Service                                             | เอนทิตี (ปลายทาง) Finance and Operations   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER (PERSONNELNUMBER)           |
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน)                   | POSITIONID (POSITIONID)                        |
| cdm_validfrom (มีผลบังคับใช้ตั้งแต่)                                    | VALIDFROM (VALIDFROM)                       |
| cdm_validto (มีผลบังคับใช้ถึง)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>ที่อยู่ของผู้ปฏิบัติงานไปยังที่อยู่ทางไปรษณีย์ของผู้ปฏิบัติงาน V2

| เอนทิตี (แหล่งที่มา) Common Data Service                                             | เอนทิตี (ปลายทาง) Finance and Operations   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER (PERSONNELNUMBER)           |
| cdm_addresstype (cdm_addresstype)                             | ADDRESSLOCATIONROLES (ADDRESSLOCATIONROLES) |
| cdm_line1 (cdm_line1)                                         | ADDRESSSTREET (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY (ADDRESSCITY)                   |
| cdm_stateorprovince (cdm_stateorprovince)                     | ADDRESSSTATE (ADDRESSSTATE)                 |
| cdm_postalcode (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred (cdm_ispreferred)                             | ISPRIMARY (ISPRIMARY)                       |
| cdm_county (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>ข้อควรพิจารณาในการรวม
เมื่อรวมข้อมูลจากทรัพยากรบุคคลเข้ากับการเงิน การรวมจะพยายามจับคู่เรกคอร์ดตามรหัส ถ้าการจับคู่เกิดขึ้น ข้อมูลในการเงินจะถูกบันทึกทับด้วยค่าในทรัพยากรบุคคล อย่างไรก็ตาม อาจมีปัญหาเกิดขึ้นถ้าตรรกะเหล่านี้เป็นเรกคอร์ดที่แตกต่างกันและมีการสร้างรหัสเดียวกันในทรัพยากรบุคคลหรือการเงินตามลำดับหมายเลขที่เกี่ยวข้องอย่างใดอย่างหนึ่ง

พื้นที่ที่อาจเกิดขึ้นแบบนี้ได้คือผู้ปฏิบัติงาน ซึ่งจะใช้หมายเลขบุคลากรเพื่อทำการจับคู่และตำแหน่งงาน งานไม่ได้ใช้ลำดับหมายเลข ด้วยเหตุนี้ถ้ารหัสงานเดียวกันมีอยู่ในทั้งทรัพยากรบุคคลและการเงิน ข้อมูลทรัพยากรบุคคลจะเขียนทับข้อมูล Dynamics 365 Finance 

เมื่อต้องการป้องกันไม่ให้เกิดปัญหากับรหัสที่ซ้ำกัน คุณสามารถเพิ่มคำนำหน้าบน [ลำดับหมายเลข](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json) หรือตั้งค่าหมายเลขเริ่มต้นบนลำดับหมายเลขที่อยู่นอกช่วงของระบบอื่นได้ 

รหัสที่ตั้งที่ใช้สำหรับที่อยู่ของผู้ปฏิบัติงานไม่ได้เป็นส่วนหนึ่งของลำดับหมายเลข เมื่อรวมที่อยู่ของผู้ปฏิบัติงานจากทรัพยากรบุคคลไปยังการเงิน ถ้าที่อยู่ของผู้ปฏิบัติงานมีอยู่แล้วในการเงินคุณ อาจมีการสร้างเรกคอร์ดที่อยู่ที่ซ้ำกัน 

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล 

![การแม็ปเท็มเพลต](./media/IntegrationMapping.png)


