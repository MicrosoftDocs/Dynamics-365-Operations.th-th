---
title: ตั้งค่าคอนฟิกการรวมกับ Finance
description: บทความนี้อธิบายการรวมระหว่าง Dynamics 365 Human Resources กับ Dynamics 365 Finance
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8be7cbf92c11036d334516116f0895c426380954
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875871"
---
# <a name="configure-integration-with-finance"></a>ตั้งค่าคอนฟิกการรวมกับ Finance


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



เมื่อต้องการรวม Dynamics 365 Human Resources กับ Dynamics 365 Finance คุณสามารถใช้เทมเพลต Human Resources กับ Finance ใน [ตัวรวมข้อมูล](/powerapps/administrator/data-integrator) เทมเพลต Human Resources ไปยัง Finance จะเปิดใช้งานโฟลว์ของข้อมูลสำหรับงาน ตำแหน่งงาน และผู้ปฏิบัติงาน เทมเพลตจะช่วยให้สามารถส่งโฟลว์ของข้อมูลจาก Human Resources ไปยัง Finance แต่ไม่อนุญาตให้มีการส่งโฟลว์ของข้อมูลจาก Finance ไปยัง Human Resources

![ทรัพยากรบุคคลไปยังโฟลว์การรวมทางการเงิน](./media/hr-admin-integration-finance-flow.png)

โซลูชัน Human Resources ไปยัง Finance มีชนิดของการซิงโครไนส์ข้อมูลต่อไปนี้:

- รักษางานใน Human Resources และซิงค์จาก Human Resources ไปยัง Finance
- รักษาตำแหน่งงานและการมอบหมายตำแหน่งงานใน Human Resources และซิงค์จาก Human Resources ไปยัง Finance
- รักษาการจ้างงานใน Human Resources และซิงค์จาก Human Resources ไปยัง Finance
- รักษาผู้ปฏิบัติงานและที่อยู่ผู้ปฏิบัติงานใน Human Resources และซิงค์จาก Human Resources ไปยัง Finance

## <a name="system-requirements-for-human-resources"></a>ความต้องการของระบบสำหรับทรัพยากรบุคคล

โซลูชันการรวมจำเป็นต้องใช้ทรัพยากรบุคคลและการเงินรุ่นต่อไปนี้: 

- Dynamics 365 Human Resources ใน Dataverse
- Dynamics 365 Finance รุ่น 7.2 และที่ใหม่กว่า

## <a name="template-and-tasks"></a>เทมเพลตและงาน

เพื่อเข้าถึงเทมเพลต Human Resources ไปยัง Finance

1. เปิด [Power Apps ศูนย์การจัดการ](https://admin.powerapps.com/) 

2. เลือก **โครงการ** แล้วเลือก **โครงการใหม่** ในมุมด้านขวาบน สร้างโครงการใหม่สำหรับนิติบุคคลแต่ละรายที่คุณต้องการรวมเข้าไปใน Finance

3. เลือก **Human Resources (Human Resources Dataverse ไปยัง Finance**) เพื่อซิงโครไนส์เรกคอร์ดจาก Human Resources ไปยัง Finance

เทมเพลตใช้งานพื้นฐานต่อไปนี้ในการซิงโครไนส์เรกคอร์ดจาก Human Resources ไปยัง Finance:

- **ฟังก์ชันงานสำหรับฟังก์ชันงานค่าตอบแทน**
- **แผนกไปยังหน่วยปฏิบัติงาน**
- **ชนิดงานไปยังชนิดงานค่าตอบแทน**
- **งานไปยังงาน**
- **งานไปยังรายละเอียดงาน**
- **ชนิดของตำแหน่งไปยังชนิดของตำแหน่ง**
- **ตำแหน่งงานไปยังตำแหน่งฐาน**
- **ตำแหน่งงานไปยังรายละเอียดตำแหน่ง**
- **ตำแหน่งงานไปยังช่วงเวลาของตำแหน่ง**
- **ตำแหน่งงานไปยังลำดับชั้นของตำแหน่ง**
- **ผู้ปฏิบัติงานไปยังผู้ปฏิบัติงาน**
- **การจ้างงานไปยังการจ้างงาน**
- **การจ้างงานไปยังรายละเอียดการจ้างงาน**
- **การมอบหมายผู้ปฏิบัติงานของตำแหน่งไปยังการมอบหมายผู้ปฏิบัติงานของตำแหน่ง**
- **ที่อยู่ของผู้ปฏิบัติงานไปยังที่อยู่ทางไปรษณีย์ของผู้ปฏิบัติงาน V2**

## <a name="template-mappings"></a>การแมปเทมเพลต

ในตารางการแมปเทมเพลตต่อไปนี้ ชื่อของงานจะมีเอนทิตี้ที่ใช้ในแอปพลิเคชันแต่ละรายการ ต้นทาง (Human Resources) อยู่ทางด้านซ้าย และปลายทาง (Finance) อยู่ทางด้านขวา

### <a name="job-functions-to-compensation-job-function"></a>ฟังก์ชันงานสำหรับฟังก์ชันงานค่าตอบแทน

| ตาราง Dataverse (แหล่งที่มา) | เอนทิตี้ Finance (ปลายทาง) |
|-------------------------------------|---------------------------------------------|
| cdm_name (ชื่อฟังก์ชัน cdm_Job)  | JOBFUNCTIONID (JOBFUNCTIONID)            |
| cdm_description (cdm_description) | คำอธิบาย (คำอธิบาย)                 |

### <a name="departments-to-operating-unit"></a>แผนกไปยังหน่วยปฏิบัติงาน

| ตาราง Dataverse (แหล่งที่มา)           | เอนทิตี้ Finance (ปลายทาง) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | ชื่อ (ชื่อ)                                 |
| cdm_departmentnumber (cdm_departmentnumber) | OPERATINGUNITNUMBER (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE (OPERATINGUNITTYPE)     |
| cdm_description (cdm_description)           | NAMEALIAS (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>ชนิดงานไปยังชนิดงานค่าตอบแทน

| ตาราง Dataverse (แหล่งที่มา)   | เอนทิตี้ Finance (ปลายทาง) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID (JOBTYPEID)                     |
| cdm_description (cdm_description)   | คำอธิบาย (คำอธิบาย)                 |
| cdm_exemptstatus (cdm_exemptstatus) | EXEMPTSTATUS (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>งานไปยังงาน

| ตาราง Dataverse (แหล่งที่มา)                           | เอนทิตี้ Finance (ปลายทาง)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description (cdm_description)                           | คำอธิบาย (คำอธิบาย)                           |
| cdm_jobdescription (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>งานไปยังรายละเอียดงาน

| ตาราง Dataverse (แหล่งที่มา)                             | เอนทิตี้ Finance (ปลายทาง) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid cdm_name (ชนิดงาน (ชื่อชนิดงาน))             | JOBTYPEID (JOBTYPEID)                     |
| cdm_jobfunctionid cdm_name (ฟังก์ชันงาน (ชื่องานของฟังก์ชันงาน)) | FUNCTIONID (FUCNTIONID)                   |
| cdm_validfrom (มีผลบังคับใช้ตั้งแต่)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (มีผลบังคับใช้ถึง)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent (จำนวนเทียบเท่าเต็มเวลาเริ่มต้น)   | FULLTIMEEQUIVALENT (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>ชนิดของตำแหน่งไปยังชนิดของตำแหน่ง

| ตาราง Dataverse (แหล่งที่มา)       | เอนทิตี้ Finance (ปลายทาง) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID (POSITIONTYPEID)           |
| cdm_description (cdm_description)       | คำอธิบาย (คำอธิบาย)                 |
| cdm_classification (cdm_classification) | CLASSIFICATION (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>ตำแหน่งงานไปยังตำแหน่งฐาน

| ตาราง Dataverse (แหล่งที่มา)           | เอนทิตี้ Finance (ปลายทาง) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>ตำแหน่งงานไปยังรายละเอียดตำแหน่ง

| ตาราง Dataverse (แหล่งที่มา)              | เอนทิตี้ Finance (ปลายทาง)       |
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

| ตาราง Dataverse (แหล่งที่มา)             | เอนทิตี้ Finance (ปลายทาง) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน)   | POSITIONID (POSITIONID)                      |
| การเรียกใช้ที่คำนวณได้ (การเรียกใช้ที่คำนวณได้) | VALIDFROM (VALIDFROM)                        |
| การเกษียณอายุที่คำนวณได้ (การเกษียณอายุที่คำนวณได้) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>ตำแหน่งงานไปยังลำดับชั้นของตำแหน่ง

| ตาราง Dataverse (แหล่งที่มา)        | เอนทิตี้ Finance (ปลายทาง) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน)                                                 | POSITIONID (POSITIONID)                      |
| cdm_parentjobpositionid cdmjobpositionnumber (cdm_parentjobpositionid cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom (มีผลบังคับใช้ตั้งแต่)                                                                  | VALIDFROM (VALIDFROM)                     |
| cdm_validto (มีผลบังคับใช้ถึง)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>ผู้ปฏิบัติงานไปยังผู้ปฏิบัติงาน
| ตาราง Dataverse (แหล่งที่มา)           | เอนทิตี้ Finance (ปลายทาง)       |
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

| ตาราง Dataverse (แหล่งที่มา)                             | เอนทิตี้ Finance (ปลายทาง) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE (EMPLOYMENTSTARTDATE) |
| cdm_employmentstartdate (cdm_employmentstartdate)                 | EMPLOYMENTENDDATE (EMPLOYMENTENDDATE)     |
| cdm_workertype (cdm_workertype)                               | WORKERTYPE (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode (cdm_companyid.cdm_companycode) | LEGALENTITYID (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>การจ้างงานไปยังรายละเอียดการจ้างงาน

| ตาราง Dataverse (แหล่งที่มา)                             | เอนทิตี้ Finance (ปลายทาง)   |
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

| ตาราง Dataverse (แหล่งที่มา)                             | เอนทิตี้ Finance (ปลายทาง)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER (PERSONNELNUMBER)           |
| cdm_jobpositionnumber (หมายเลขตำแหน่งงาน)                   | POSITIONID (POSITIONID)                        |
| cdm_validfrom (มีผลบังคับใช้ตั้งแต่)                                    | VALIDFROM (VALIDFROM)                       |
| cdm_validto (มีผลบังคับใช้ถึง)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>ที่อยู่ของผู้ปฏิบัติงานไปยังที่อยู่ทางไปรษณีย์ของผู้ปฏิบัติงาน V2

| ตาราง Dataverse (แหล่งที่มา)                             | เอนทิตี้ Finance (ปลายทาง)   |
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

การรวมจาก Human Resources ไปยัง Finance จะพยายามจับคู่เรกคอร์ดตามรหัส ถ้าเรกคอร์ดตรงกัน ตัวรวมข้อมูลจะบันทึกทับข้อมูลใน Finance ด้วยค่าใน Human Resources อย่างไรก็ตาม อาจมีปัญหาเกิดขึ้นถ้าตรรกะเหล่านี้เป็นเรกคอร์ดที่แตกต่างกันและมีการสร้างรหัสเดียวกันในทรัพยากรบุคคลหรือการเงินตามลำดับหมายเลขที่เกี่ยวข้องอย่างใดอย่างหนึ่ง

ปัญหานี้อาจเกิดขึ้นได้กับ **ผู้ปฏิบัติงาน** ซึ่งจะใช้ **หมายเลขบุคลากร** เพื่อทำการจับคู่ และ **ตำแหน่งงาน** งานไม่ได้ใช้ลำดับหมายเลข ด้วยเหตุนี้ ถ้ารหัสงานเดียวกันมีอยู่ในทั้ง Human Resources และ Finance ข้อมูล Human Resources จะเขียนทับข้อมูล Dynamics 365 Finance 

เมื่อต้องการป้องกันไม่ให้เกิดปัญหากับรหัสที่ซ้ำกัน คุณสามารถเพิ่มคำนำหน้าบน [ลำดับหมายเลข](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) หรือตั้งค่าหมายเลขเริ่มต้นบนลำดับหมายเลขที่อยู่นอกช่วงของระบบอื่นได้ 

รหัสที่ตั้งที่ใช้สำหรับที่อยู่ของผู้ปฏิบัติงานไม่ได้เป็นส่วนหนึ่งของลำดับหมายเลข เมื่อรวมที่อยู่ของผู้ปฏิบัติงานจากทรัพยากรบุคคลไปยังการเงิน ถ้าที่อยู่ของผู้ปฏิบัติงานมีอยู่แล้วในการเงินคุณ อาจมีการสร้างเรกคอร์ดที่อยู่ที่ซ้ำกัน 

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแมปเทมเพลตในตัวรวมข้อมูล 

![การแมปเทมเพลต](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
