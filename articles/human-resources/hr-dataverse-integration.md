---
title: ตั้งค่าคอนฟิกการรวมกับตาราง Dataverse
description: บทความนี้อธิบายการรวมระหว่าง Microsoft Dynamics 365 Human Resources และ Dataverse
author: anschmidt
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63c25020b7026a76ecc6e2c3563f8299627ec8a8
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838634"
---
# <a name="configure-integration-with-dataverse-tables"></a>ตั้งค่าคอนฟิกการรวมกับตาราง Dataverse

>[!Important]
>ขณะนี้ฟังก์ชันที่ระบบไม่แสดงในบทความนี้จะสามารถใช้งานได้กับลูกค้าบน Dynamics 365 Human Resources ในโครงสร้างพื้นฐานของการเงินและการดำเนินงาน 


หากต้องการรวม Microsoft Dynamics 365 Human Resources กับ Dataverse คุณสามารถใช้ [ตัวรวมข้อมูล](/powerapps/administrator/data-integrator) ได้ เทมเพลต Human Resources–to–Dataverse จะเปิดใช้งานข้อมูลงาน ตําแหน่ง ผู้ปฏิบัติงาน และอื่นๆ ที่จะไหลจากทรัพยากรบุคคลเข้ามายัง Dataverse และจาก Dataverse เข้าสู่ Human Resources การสร้างงานเขียนในทั้งสองระบบ

## <a name="system-requirements-for-human-resources"></a>ความต้องการของระบบสำหรับทรัพยากรบุคคล

โซลูชันการรวมจำเป็นต้องใช้ Human Resources และ Dynamics 365 Finance รุ่นต่อไปนี้: 

- Dynamics 365 Finance รุ่น 7.2 และที่ใหม่กว่า
- Dynamics CRM สภาพแวดล้อมที่มีการสร้างฐานข้อมูลและอนุญาตแอป Dynamics 365

## <a name="template-and-tasks"></a>เทมเพลตและงาน

ให้ปฏิบัติตามขั้นตอนเหล่านี้ เพื่อเข้าถึงเทมเพลต Human Resources–to–Finance

1. เปิด [ศูนย์การจัดการ Power Apps](https://admin.powerapps.com/) 
2. ภายใต้สภาพแวดล้อมของคุณให้เลือก **แอป Dynamics 365** แล้วเลือก **แหล่งที่มาของแอป** บนแถบเครื่องมือ
3. เมื่อต้องการติดตั้งเทมเพลต ให้ค้นหา "Human Resources ของการรวมแบบสองทิศทาง" หรือไปที่ที่อยู่ต่อไปนี้โดยตรง <https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite>
3. หลังจากการติดตั้งเสร็จสมบูรณ์ ให้เปิด Dynamics 365 Finance
4. เปิดพื้นที่ทำงาน **การจัดการข้อมูล** 
5. เลือก **การรวมแบบสองทิศทาง** 
6. ปฏิบัติตามกระบวนการในการเชื่อมโยงสภาพแวดล้อมของคุณกับบริษัทอย่างน้อยหนึ่งบริษัทในองค์กรของคุณ 
7. เมื่อคุณตั้งค่าลิงค์ไปยังสภาพแวดล้อม Dataverse ของคุณเสร็จสิ้นแล้ว ให้เลือก **ใช้โซลูชัน** มีการใช้โซลูชันนี้ และมีการติดตั้งการแม็ปไว้ในแอปตัวรวม

## <a name="template-mappings"></a>การแมปเทมเพลต

ในตารางการแมปเทมเพลตต่อไปนี้ ชื่อของงานจะบ่งชี้เอนทิตี้ที่ใช้ในแอปพลิเคชันแต่ละรายการ การเงินอยู่ทางด้านซ้าย และ Dataverse อยู่ทางด้านขวา

### <a name="bank-account-disbursements-dual-write-to-bank-account-disbursement"></a>การเบิกจ่ายเงินผ่านบัญชีธนาคาร (การรวมแบบสองทิศทาง) ไปยังการเบิกจ่ายเงินผ่านบัญชีธนาคาร

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATIONID        | cdm\_bankaccountid.cdm\_accountidentification        |
| ยอดเงิน                         | cdm\_amount                                         |
| PRIORITY                       | cdm\_disbursementpriority                           |
| PERSONNELNUMBER                | cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber    |
| REMAINDER                      | cdm\_isremainder                                    |

### <a name="benefit-calculation-rate-detail-dual-write-to-benefit-calculation-rate-detail"></a>รายละเอียดอัตราการคำนวณสวัสดิการ (การรวมแบบสองทิศทาง) ไปยังรายละเอียดอัตราการคำนวณสวัสดิการ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CONTRIBUTIONMETHOD             | cdm\_contributionmethod                             |
| EFFECTIVE                      | cdm\_effective                                      |
| EMPLOYERCONTRIBUTION           | cdm\_employercontribution                           |
| EXPIRATION                     | cdm\_expiration                                     |
| WORKERDEDUCTION                | cdm\_workerdeduction                                |
| ชื่อ                           | cdm\_calculationrateid.cdm\_name                     |

### <a name="benefit-calculation-rate-header-to-benefit-calculation-rate"></a>ส่วนหัวของอัตราการคำนวณสวัสดิการไปยังอัตราการคำนวณสวัสดิการ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| ชื่อ                           | cdm\_name                                           |
| TIERTYPE                       | cdm\_tiertype                                       |

### <a name="benefit-option-to-benefit-option"></a>ตัวเลือกสวัสดิการไปยังตัวเลือกสวัสดิการ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ALLOWBENEFICIARYDESIGNATIONS   | cdm\_allowbeneficiarydesignations                   |
| ALLOWDEPENDENTCOVERAGE         | cdm\_allowdependentcoverage                         |
| BENEFITOPTIONID                | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| ISWAIVE                        | cdm\_iswaived                                       |

### <a name="benefit-type-to-benefit-type"></a>ชนิดของสวัสดิการให้กับชนิดของสวัสดิการ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| BENEFITTYPEID                  | cdm\_name                                           |
| CONCURRENTENROLLMENT           | cdm\_concurrentenrollment                           |
| คำอธิบาย                    | cdm\_description                                    |
| PAYROLLCATEGORY                | cdm\_payrollcategory                                |

### <a name="business-calendar-to-business-process-calendar"></a>ปฏิทินทางธุรกิจให้กับปฏิทินกระบวนการทางธุรกิจ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| ชื่อ                           | cdm\_calendarname                                   |
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| ISOPENMONDAY                   | cdm\_ismondayopen                                   |
| ISOPENTUESDAY                  | cdm\_istuesdayopen                                  |
| ISOPENWEDNESDAY                | cdm\_iswednesdayopen                                |
| ISOPENTHURSDAY                 | cdm\_isthursdayopen                                 |
| ISOPENFRIDAY                   | cdm\_isfridayopen                                   |
| ISOPENSATURDAY                 | cdm\_issaturdayopen                                 |
| ISOPENSUNDAY                   | cdm\_issundayopen                                   |

### <a name="business-process-to-business-process-header"></a>กระบวนการทางธุรกิจให้กับส่วนหัวของกระบวนการทางธุรกิจ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processid                                      |
| PROCESSTYPE                    | cdm\_processtype                                    |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| ชื่อ                           | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| สถานะ                         | cdm\_status                                         |
| TARGETDATE                     | cdm\_targetdate                                     |
| STARTDATETIME                  | cdm\_startdatetime                                  |
| ENDDATETIME                    | cdm\_enddatetime                                    |
| RESOLVEDBYPERSONNELNUMBER      | cdm\_resolvedbyid.cdm\_workernumber                  |
| PROCESSOWNERPERSONNELNUMBER    | cdm\_processownerid.cdm\_workernumber                |
| SOURCETEMPLATSNAME             | cdm\_sourcetemplateid.cdm\_name                      |
| SOURCETEMPLATSPROCESSTYPE      | cdm\_sourcetemplataid.cdm\_businessprocesstype       |
| SOURCETEMPLATEGENERICSUBTYPE   | cdm\_sourcetemplateid.cdm\_genericsubtype            |

### <a name="business-process-library-task-group-to-business-process-library-task-group"></a>กลุ่มงานไลบรารีกระบวนการทางธุรกิจให้กับกลุ่มงานไลบรารีกระบวนการทางธุรกิจ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_processtype                                    |
| ชื่อ                           | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |

### <a name="business-process-stage-to-business-process-stage"></a>ขั้นตอนกระบวนการทางธุรกิจให้กับขั้นตอนกระบวนการทางธุรกิจ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| ชื่อ                           | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| .SEQUENCENUMBER                 | cdm\_sequencenumber                                 |

### <a name="business-process-task-to-business-process-task"></a>งานกระบวนการทางธุรกิจให้กับงานกระบวนการทางธุรกิจ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| DUEDATE                        | cdm\_duedate                                        |
| TASKID                         | cdm\_taskid                                         |
| INSTRUCTIONS                   | cdm\_instructions                                   |
| COMPLETIONDATETIME             | cdm\_completiondatetime                             |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| ชื่อ                           | cdm\_name                                           |
| สถานะ                         | cdm\_status                                         |
| RESOLVEDBY\_PERSONNELNUMBER     | cdm\_resolvedbyid.cdm\_workernumber                  |
| TEMPLATETASKID                 | cdm\_templatetaskid.cdm\_taskid                      |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedposition.cdm\_jobpositionnumber         |

### <a name="business-process-template-to-checklist-template-header"></a>เทมเพลตกระบวนการทางธุรกิจให้กับส่วนหัวของเทมเพลตรายการตรวจสอบ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| ชื่อ                           | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| CALENDARID                     | cdm\_businessprocesscalendarid.cdm\_name             |
| PERSONNELNUMBER                | cdm\_processownerid.cdm\_workernumber                |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="business-process-template-task-to-checklist-template-task"></a>งานเทมเพลตกระบวนการทางธุรกิจให้กับงานเทมเพลตรายการตรวจสอบ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| TASKID                         | cdm\_taskid                                         |
| ชื่อ                           | cdm\_name                                           |
| TEMPLATEHEADER\_PROCESSTYPE     | cdm\_businessprocesstemplateheaderid.cdm\_businessprocesstype |
| TEMPLATEHEADER\_GENERICSUBTYPE  | cdm\_businessprocesstemplateheaderid.cdm\_genericsubtype |
| TEMPLATEHEADER\_NAME            | cdm\_businessprocesstemplateheaderid.cdm\_name       |
| คำอธิบาย                    | cdm\_description                                    |
| DUEDATEOFFSETDAYS              | cdm\_duedateoffsetdays                              |
| MENUITEMTYPE                   | cdm\_tasklinktype                                   |
| MENUITEM                       | cdm\_tasklink                                       |
| CONTACTPERSON\_PERSONNELNUMBER  | cdm\_contactpersonid.cdm\_workernumber               |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedpositionid.cdm\_jobpositionnumber       |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| INSTRUCTIONS                   | cdm\_instructions                                   |

### <a name="calculation-frequency-to-benefit-calculation-frequency"></a>ความถี่ในการคํานวณให้กับความถี่ในการคํานวณสวัสดิการ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| ความถี่                      | cdm\_name                                           |
| FREQUENCYCONTROL               | cdm\_frequencycontrol                               |
| ISIMMUTABLE                    | cdm\_isimmutable                                    |

### <a name="calculation-frequency-pay-period-to-benefit-calculation-frequency-pay-period"></a>รอบระยะเวลาการชำระค่าจ้างตามความถี่ในการคำนวณให้กับรอบระยะเวลาการชำระค่าจ้างตามความถี่ในการคำนวณสวัสดิการ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALCULATIONFREQUENCYID         | cdm\_benefitcalculationfrequencyid.cdm\_name         |
| PERIODSTARTDATE                | cdm\_payperiodid.cdm\_periodstartdate                |
| PAYCYCLEID                     | cdm\_payperiodid.cdm\_paycycleid.cdm\_name            |

### <a name="calendar-to-work-calendar"></a>ปฏิทินให้กับปฏิทินการทำงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| CALENDARNAME                   | cdm\_description                                    |
| WORKCALENDARHOLIDAYID          | cdm\_workcalendarholidayid.cdm\_name                 |

### <a name="compensation-fixed-action-table-to-fixed-compensation-event"></a>ตารางการดำเนินการเกี่ยวกับค่าตอบแทนคงที่ให้กับเหตุการณ์ค่าตอบแทนคงที่

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACTION                         | cdm\_name                                           |
| ACTIVE                         | cdm\_isactive                                       |
| คำอธิบาย                    | cdm\_description                                    |
| ชนิด                           | cdm\_eventtype                                      |

### <a name="compensation-fixed-plan-to-compensation-fixed-plan"></a>แผนค่าตอบแทนคงที่ให้กับแผนค่าตอบแทนคงที่

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PLAN                           | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| ชนิด                           | cdm\_type                                           |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| สกุลเงิน                       | cdm\_transactioncurrencyid.isocurrencycode          |
| PAYFREQUENCY                   | cdm\_payfrequency.cdm\_name                          |
| HIRERULE                       | cdm\_hirerule                                       |
| OUTOFRANGETOLERANCE            | cdm\_outofrangetolerance                            |
| RECOMMENDATIONALLOWED          | cdm\_recommendationallowed                          |
| COMPENSATIONSTRUCTURE          | cdm\_compensationgrid.cdm\_name                      |
| REFPOINTSETUPID                | cdm\_referencepointsetupline.cdm\_referencepointsetupid.cdm\_name |
| CONTROLPOINT                   | cdm\_referencepointsetupline.cdm\_name               |

### <a name="compensation-grids-to-compensation-grid"></a>กริดค่าตอบแทนไปยังกริดค่าตอบแทน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| GRIDID                         | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| REFERENCESETUP                 | cdm\_referencepointsetupid.cdm\_name                 |
| ชนิด                           | cdm\_type                                           |
| สกุลเงิน                       | cdm\_transactioncurrencyid.isocurrencycode          |

### <a name="compensation-job-function-to-job-function"></a>ฟังก์ชันงานค่าตอบแทนให้กับฟังก์ชันงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBFUNCTIONID                  | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |

### <a name="compensation-job-type-to-job-type"></a>ชนิดงานค่าตอบแทนให้กับชนิดงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBTYPEID                      | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| EXEMPTSTATUS                   | cdm\_exemptstatus                                   |

### <a name="compensation-pay-frequency-to-compensation-pay-frequency"></a>ความถี่ในการจ่ายค่าตอบแทนให้กับความถี่ในการจ่ายค่าตอบแทน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYRATECONVERSION              | cdm\_name                                           |
| PERIOD                         | cdm\_period                                         |
| คำอธิบาย                    | cdm\_description                                    |
| ANNUALCONVERSIONFACTOR         | cdm\_annualconversionfactor                         |
| HOURLYCONVERSIONFACTOR         | cdm\_hourlyconversionfactor                         |
| MONTHLYCONVERSIONFACTOR        | cdm\_monthlyconversionfactor                        |
| WEEKLYCONVERSIONFACTOR         | cdm\_weeklyconversionfactor                         |

### <a name="compensation-regions-to-compensation-region"></a>ภูมิภาคของค่าตอบแทนไปยังภูมิภาคของค่าตอบแทน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| ที่ตั้ง                       | cdm\_name                                           |

### <a name="compensation-variable-plan-v2-to-compensation-variable-plan"></a>แผนค่าตอบแทนผันแปร V2 ให้กับแผนค่าตอบแทนผันแปร

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| VARIABLEAWARDBASIS             | cdm\_awardbasis                                     |
| AWARDBASISCALCULATION          | cdm\_awardbasiscalculation                          |
| CALCULATIONTYPE                | cdm\_calculationtype                                |
| คำอธิบาย                    | cdm\_description                                    |
| ENABLEENROLLMENT               | cdm\_enableenrollment                               |
| ENABLELEVELS                   | cdm\_enablelevels                                   |
| ENABLERECOMMENDATION           | cdm\_enablerecommendation                           |
| HIRERULE                       | cdm\_hirerule                                       |
| LEVERAGE100PERCENT             | cdm\_leverage100percent                             |
| LEVERAGEMAXIMUM                | cdm\_leveragemaximum                                |
| LEVERAGEMINIMUM                | cdm\_leverageminimum                                |
| LEVERAGEOVEROBJECTIVE          | cdm\_leverageoverobjective                          |
| LEVERAGEUNDEROBJECTIVE         | cdm\_leverageunderobjective                         |
| PERCENTOFBASIS                 | cdm\_percentofbasis                                 |
| PLANID                         | cdm\_name                                           |
| VARIABLECOMPENSATIONTYPE       | cdm\_variablecompensationtypeid.cdm\_name            |
| UNITCURRENCYCODE               | transactioncurrencyid.isocurrencycode              |
| UNITRELATIONSHIP               | cdm\_unitrelationship                               |
| UNITVALUE                      | cdm\_unitvalue                                      |
| NUMBEROFUNITSREAL              | cdm\_numberofunits                                  |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VESTINGRULE                    | cdm\_vestingruleid.cdm\_name                         |
| LEVERAGETOLERANCEMAX           | cdm\_leveragetolerancemax                           |
| LEVERAGETOLERANCEMIN           | cdm\_leveragetolerancemin                           |

### <a name="compensation-variable-type-to-compensation-variable-plan-type"></a>ชนิดแผนค่าตอบแทนผันแปรให้กับชนิดแผนค่าตอบแทนผันแปร

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| ชนิด                           | cdm\_awardtype                                      |
| VARIABLECOMPENSATIONTYPE       | cdm\_name                                           |

### <a name="compensation-vesting-rules-to-vesting-rule"></a>กฎสิทธิ์พึงได้ค่าตอบแทนให้กับกฎสิทธิ์พึงได้

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| บันทึกย่อ                           | cdm\_notes                                          |
| VESTINGRULE                    | cdm\_name                                           |

### <a name="department-v2-to-department"></a>แผนก V2 ให้กับแผนก

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| OPERATINGUNITNUMBER            | cdm\_departmentnumber                               |
| ชื่อ                           | cdm\_name                                           |
| SEARCHNAME                     | cdm\_description                                    |
| PARTYTYPE                      | cdm\_partytype                                      |

### <a name="dual-write-tax-region-to-tax-region"></a>ภูมิภาคภาษีการรวมแบบสองทิศทางให้กับภูมิภาคภาษี

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CITY                           | cdm\_city                                           |
| COUNTRYORREGION                | cdm\_countryorregion                                |
| COUNTY                         | cdm\_county                                         |
| STATE                          | cdm\_stateorprovince                                |
| TAXREGIONNAME                  | cdm\_name                                           |

### <a name="dual-write-worker-identification-to-worker-person-identification-number"></a>การระบุรหัสประจำตัวผู้ปฏิบัติงานในการรวมแบบสองทิศทางให้กับหมายเลขรหัสประจำตัวของบุคคลของผู้ปฏิบัติงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| ENTRYTYPE                      | cdm\_entrytype                                      |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| IDENTIFICATIONNUMBER           | cdm\_identificationnumber                           |
| IDENTIFICATIONTYPEID           | cdm\_identificationtypeid.cdm\_name                  |
| ISPRIMARY                      | cdm\_isprimary                                      |
| ISSUEDATE                      | cdm\_issuedate                                      |
| ISSUINGAGENCYID                | cdm\_issuingagencyid.cdm\_name                       |
| WORKERNUMBER                   | cdm\_workerid.cdm\_workernumber                      |

### <a name="compensation-structure-to-compensation-structure"></a>โครงสร้างค่าตอบแทนให้กับโครงสร้างค่าตอบแทน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ยอดเงิน                         | cdm\_amount                                         |
| GRID                           | cdm\_compensationgridid.cdm\_name                    |
| LEVELID                        | cdm\_compensationlevelid.cdm\_name                   |
| REFERENCEPOINTLINENUMBER       | cdm\_referencepointid.cdm\_linenumber                |
| REFERENCESETUP                 | cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name |
| REFERENCEPOINT                 | cdm\_referencepointid.cdm\_name                      |

### <a name="earning-code-to-payroll-earning-code"></a>รหัสรายได้ให้กับรหัสรายได้ค่าจ้าง

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| EARNINGCODE                    | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| INCLUDEINPAYMENTTYPE           | cdm\_includeinpaymenttype                           |
| QUANTITYUNIT                   | cdm\_quantityunit                                   |
| TRACKFMLAHOURS                 | cdm\_trackfmlahours                                 |
| ISPRODUCTIVE                   | cdm\_isproductive                                   |

### <a name="employee-fixed-compensation-to-worker-fixed-compensation"></a>ค่าตอบแทนคงที่ของพนักงานให้กับค่าตอบแทนคงที่ของผู้ปฏิบัติงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| ชนิด                           | cdm\_compensationtype                               |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| LINENUMBER                     | cdm\_linenumber                                     |
| PAYFREQUENCY                   | cdm\_payfrequencyid.cdm\_name                        |
| PAYRATE                        | cdm\_payrate                                        |
| PLAN                           | cdm\_planid.cdm\_name                                |
| POSITIONID                     | cdm\_positionid.cdm\_jobpositionnumber               |
| PROCESSTYPE                    | cdm\_processtype                                    |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| ACTION                         | cdm\_eventid.cdm\_name                               |
| STEP                           | cdm\_referencepointsetuplineid.cdm\_name             |
| REFPOINTSETUPID                | cdm\_referencepointsetuplineid.cdm\_referencepointsetupid.cdm\_name |

### <a name="employment-per-company-to-employment"></a>การจ้างงานต่อบริษัทให้กับการจ้างงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| EMPLOYMENTENDDATE              | cdm\_employmentenddate                              |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| EMPLOYMENTSTARTDATE            | cdm\_employmentstartdate                            |
| WORKERTYPE                     | cdm\_workertype                                     |
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| ADJUSTEDWORKERSTARTDATE        | cdm\_adjustedworkerstartdate                        |
| EMPLOYERNOTICEAMOUNT           | cdm\_employernoticeamount                           |
| EMPLOYERUNITOFNOTICE           | cdm\_employerunitofnotice                           |
| WORKERUNITOFNOTICE             | cdm\_workerunitofnotice                             |
| WORKERNOTICEAMOUNT             | cdm\_workernoticeamount                             |
| LASTDATEWORKED                 | cdm\_lastdateworked                                 |
| PROBATIONENDDATE               | cdm\_probationenddate                               |
| TRANSITIONDATE                 | cdm\_transitiondate                                 |
| TRANSITIONREASONCODENAME       | cdm\_transitionreasoncode.cdm\_name                  |
| WORKERSTARTDATE                | cdm\_workerstartdate                                |
| VALIDTO                        | cdm\_validto                                        |
| VALIDFROM                      | cdm\_validfrom                                      |

### <a name="ethnic-origins-to-ethnic-origin"></a>เชื้อชาติให้กับเชื้อชาติ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ETHNICORIGINID                 | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |

### <a name="group-assignment-to-business-process-group-assignment"></a>การกำหนดกลุ่มให้กับการกำหนดกลุ่มกระบวนการทางธุรกิจ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ชื่อ                           | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="identification-type-to-worker-person-identification-type"></a>ชนิดการระบุรหัสประจำตัวให้กับชนิดการระบุรหัสประจำตัวของบุคคลของผู้ปฏิบัติงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| IDENTIFICATIONTYPEID           | cdm\_name                                           |
| ALLOWEDVALUES                  | cdm\_allowedvalues                                  |
| FIXEDLENGTH                    | cdm\_fixedlength                                    |
| IDENTIFICATIONNUMBERFORMAT     | cdm\_identificationnumberformat                     |

### <a name="issuing-agency-to-person-identification-issuing-agency"></a>หน่วยงานที่ออกให้กับหน่วยงานที่ออกรหัสประจำตัวของบุคคล

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| อีเมล                          | cdm\_email                                          |
| EXTENSION                      | cdm\_extension                                      |
| FAX                            | cdm\_fax                                            |
| ISSUINGAGENCY                  | cdm\_name                                           |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| ชื่อ                           | cdm\_description                                    |
| PAGER                          | cdm\_pager                                          |
| SMS                            | cdm\_sms                                            |
| TELEPHONE                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telex                                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |

### <a name="job-positions-dual-write-to-job-position"></a>การรวมแบบสองทิศทางของตำแหน่งงานให้กับตําแหน่งงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONID                     | cdm\_jobpositionnumber                              |
| ACTIVATION                     | cdm\_activation                                     |
| AVAILABLEFORASSIGNMENT         | cdm\_availableforassignment                         |
| COMPENSATIONREGIONID           | cdm\_compensationregionid.cdm\_name                  |
| DEPARTMENTID                   | cdm\_departmentid.cdm\_departmentnumber              |
| คำอธิบาย                    | cdm\_description                                    |
| FULLTIMEEQUIVALENT             | cdm\_fulltimeequivalent                             |
| JOBID                          | cdm\_jobid.cdm\_name                                 |
| PARENTPOSITIONID               | cdm\_parentjobpositionid.cdm\_jobpositionnumber      |
| POSITIONTYPEID                 | cdm\_positiontypeid.cdm\_name                        |
| การปลดเกษียณ                     | cdm\_retirement                                     |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |

### <a name="jobs-dual-write-to-job"></a>การรวมแบบสองทิศทางของงานไปยังงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBID                          | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| JOBDESCRIPTION                 | cdm\_jobdescription                                 |
| ALLOWUNLIMITEDPOSITIONS        | cdm\_allowunlimitedpositions                        |
| MAXIMUMNUMBEROFPOSITIONS       | cdm\_maximumnumberofpositions                       |
| JOBFUNCTIONID                  | cdm\_jobfunctionid.cdm\_name                         |
| JOBTYPEID                      | cdm\_jobtypeid.cdm\_name                             |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| DEFAULTFULLTIMEEQUIVALENCY     | cdm\_defaultfulltimeequivalent                      |

### <a name="language-codes-to-language"></a>รหัสภาษาให้กับภาษา

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| LANGUAGECODEID                 | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |

### <a name="leave-and-absence-bank-transaction-v2-to-leave-bank-transaction"></a>ธุรกรรมธนาคารการลางานและการขาดงาน V2 ให้กับธุรกรรมธนาคารการลา

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ยอดเงิน                         | cdm\_amount                                         |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TRANSACTIONDATE                | cdm\_transactiondate                                |
| TRANSACTIONNUMBER              | cdm\_transactionnumber                              |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| TRANSACTIONTYPE                | cdm\_transactiontype                                |

### <a name="leave-and-absence-enrollment-v2-to-leave-enrollment"></a>การลงทะเบียนการลางานและการขาดงาน V2 ให้กับการลงทะเบียนการลางาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| CUSTOMDATE                     | cdm\_customdate                                     |
| ACCRUALSTARTDATE               | cdm\_accrualstartdate                               |
| ACCRUALDATEBASIS               | cdm\_accrualdatebasis                               |
| ISACCRUALSUSPENDED             | cdm\_isaccrualsuspended                             |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TIERBASIS                      | cdm\_tierbasis                                      |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="leave-and-absence-plan-v2-to-leave-plan"></a>แผนการลางานและการขาดงาน V2 ให้กับแผนการลางาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCRUALFREQUENCY               | cdm\_accrualfrequency                               |
| ชื่อ                           | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| STARTDATE                      | cdm\_startdate                                      |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-and-absence-type-to-leave-type"></a>ชนิดการลางานและการขาดงานให้กับชนิดการลางาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| ชนิด                           | cdm\_type                                           |
| EARNINGCODEID                  | cdm\_earningcodeid.cdm\_name                         |

### <a name="leave-and-absence-type-reason-code-to-leave-type-reason-code"></a>รหัสเหตุผลของชนิดการลางานและการขาดงานให้กับรหัสเหตุผลของชนิดการลางาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| LEAVETYPE                      | cdm\_typeid.cdm\_type                                |
| REASONCODEID                   | cdm\_reasoncodeid.cdm\_name                          |

### <a name="leave-time-off-request-detail-to-leave-request-detail"></a>รายละเอียดคำขอลาหยุดงานให้กับรายละเอียดคำขอลางาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ยอดเงิน                         | cdm\_amount                                         |
| LEAVEDATE                      | cdm\_leavedate                                      |
| REQUESTID                      | cdm\_leaverequestid.cdm\_leaverequestnumber          |
| ชนิด                           | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-time-off-request-header-to-leave-request"></a>ส่วนหัวคำขอลาหยุดงานให้กับคำขอลางาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REQUESTID                      | cdm\_leaverequestnumber                             |
| REQUESTDATE                    | cdm\_requestdate                                    |
| สถานะ                         | cdm\_status                                         |
| COMMENT                        | cdm\_comment                                        |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="levels-to-compensation-level"></a>ระดับให้กับระดับค่าตอบแทน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ชนิด                           | cdm\_type                                           |
| คำอธิบาย                    | cdm\_description                                    |
| LEVEL                          | cdm\_name                                           |

### <a name="onboarding-process-header-to-onboard-process-header"></a>ส่วนหัวของกระบวนการเตรียมความพร้อมให้กับส่วนหัวของกระบวนการเตรียมความพร้อม

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ONBOARDEDEMPLOYEEPERSONNELNUMBER | cdm\_onboardedemployeeid.cdm\_workernumber           |
| EMPLOYMENTPERSONNELNUMBER      | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| LEGALENTITYID                  | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |
| EMPLOYMENTSTARTDATE            | cdm\_employmentid.cdm\_employmentstartdate           |

### <a name="pay-cycle-to-pay-cycle"></a>รอบการชำระค่าจ้างไปยังรอบการชำระค่าจ้าง

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| PAYCYCLEFREQUENCY              | cdm\_frequency                                      |

### <a name="pay-period-to-pay-period"></a>รอบระยะเวลาการชำระค่าจ้างไปยังรอบระยะเวลาการชำระค่าจ้าง

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| COMMENTS                       | cdm\_description                                    |
| DEFAULTPAYMENTDATE             | cdm\_defaultpaymentdate                             |
| PAYCYCLEID                     | cdm\_paycycleid.cdm\_name                            |
| PERIODENDDATE                  | cdm\_periodenddate                                  |
| PERIODSTARTDATE                | cdm\_periodstartdate                                |
| สถานะ                         | cdm\_status                                         |

### <a name="payroll-details-for-positions-to-payroll-position-detail"></a>รายละเอียดค่าจ้างสำหรับตำแหน่งให้กับรายละเอียดตำแหน่งดูแลค่าจ้าง

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_paycycle.cdm\_name                              |
| POSITIONID                     | cdm\_position.cdm\_jobpositionnumber                 |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| ANNUALREGULARHOURS             | cdm\_annualregularhours                             |
| PAIDBYLEGALENTITY              | cdm\_paidby.cdm\_companycode                         |

### <a name="position-default-dimensions-dual-write-to-job-position-dimension"></a>การรวมแบบสองทิศทางของมิติเริ่มต้นของตำแหน่งให้กับมิติตำแหน่งงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |

### <a name="position-type-to-position-type"></a>ชนิดของตำแหน่งไปยังชนิดของตำแหน่ง

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONTYPEID                 | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| CLASSIFICATION                 | cdm\_classification                                 |

### <a name="position-worker-assignments-v2-to-position-worker-assignment"></a>การมอบหมายผู้ปฏิบัติงานให้กับตำแหน่งงาน V2 ให้กับการมอบหมายผู้ปฏิบัติงานให้กับตำแหน่งงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| IsPrimaryPosition              | cdm\_isprimaryposition                              |

### <a name="reason-codes-to-reason-code"></a>รหัสเหตุผลให้กับรหัสเหตุผล

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REASONCODEID                   | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| ISABSENCEAPPLICABLE            | cdm\_isabsenceapplicable                            |
| ISAPPLICATIONAPPLICABLE        | cdm\_isapplicationapplicable                        |
| ISCOMPENSATIONAPPLICABLE       | cdm\_iscompensationapplicable                       |
| ISCREATENEWPOSITIONAPPLICABLE  | cdm\_iscreatenewpositionapplicable                  |
| ISEDITPOSITIONAPPLICABLE       | cdm\_iseditpositionapplicable                       |
| ISHIREAPPLICABLE               | cdm\_ishireapplicable                               |
| ISSKILLMAPPINGAPPLICABLE       | cdm\_isskillmappingapplicable                       |
| ISTERMINATIONAPPLICABLE        | cdm\_isterminationapplicable                        |
| ISTRANSFERAPPLICABLE           | cdm\_istransferapplicable                           |

### <a name="reference-point-setup-line-dual-write-to-compensation-reference-point-setup-line"></a>รายการการตั้งค่าจุดอ้างอิง (การรวมแบบสองทิศทาง) ไปยังรายการการตั้งค่าจุดอ้างอิงค่าตอบแทน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| คำอธิบาย                    | cdm\_description                                    |
| LINENUM                        | cdm\_linenumber                                     |
| REFPOINTID                     | cdm\_name                                           |
| REFPOINTSETUPID                | cdm\_referencepointsetupid.cdm\_name                 |

### <a name="reference-point-setups-to-compensation-reference-point-setup"></a>การตั้งค่าจุดอ้างอิงให้กับการตั้งค่าจุดอ้างอิงค่าตอบแทน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REFERENCESETUP                 | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| ชนิด                           | cdm\_compensationtype                               |

### <a name="skill-types-to-skill-type"></a>ชนิดของทักษะให้กับชนิดของทักษะ

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| SKILLTYPE                      | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |

### <a name="titles-to-title"></a>ตำแหน่งให้กับตำแหน่ง

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| TITLEID                        | cdm\_name                                           |

### <a name="variable-compensation-level-v2-to-compensation-variable-plan-level"></a>ระดับค่าตอบแทนผันแปร V2 ให้กับระดับแผนค่าตอบแทนผันแปร

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| AWARDAMOUNT                    | cdm\_awardamount                                    |
| AWARDPERCENT                   | cdm\_awardpercent                                   |
| AWARDUNITSREAL                 | cdm\_awardunits                                     |
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| PLANID                         | cdm\_compensationvariableplanid.cdm\_name            |

### <a name="veteran-status-to-veteran-status"></a>สถานะทหารผ่านศึกให้กับสถานะทหารผ่านศึก

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| VETERANSTATUSID                | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |
| ISPROTECTEDVETERAN             | cdm\_isprotectedveteran                             |

### <a name="work-calendar-enrollments-to-work-calendar-enrollment"></a>การลงทะเบียนในปฏิทินการทำงานให้กับการลงทะเบียนในปฏิทินการทำงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_employmentid.cdm\_employmentstartdate           |
| PERSONNELNUMBER                | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| CALENDARID                     | cdm\_workcalendarid.cdm\_name                        |
| COMPANYID                      | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |

### <a name="work-calendar-holiday-to-work-calendar-holiday"></a>วันหยุดในปฏิทินการทำงานให้กับวันหยุดในปฏิทินการทำงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| รหัส                             | cdm\_name                                           |
| คำอธิบาย                    | cdm\_description                                    |

### <a name="work-calendar-holiday-line-to-work-calendar-holiday-line"></a>รายการวันหยุดในปฏิทินการทำงานให้กับรายการวันหยุดในปฏิทินการทำงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| HOLIDAYID                      | cdm\_workcalendarholidayid.cdm\_name                 |
| ชื่อ                           | cdm\_name                                           |
| HOLIDAYDATE                    | cdm\_holidaydate                                    |

### <a name="worker-to-worker"></a>ผู้ปฏิบัติงานไปยังผู้ปฏิบัติงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workernumber                                   |
| FIRSTNAME                      | cdm\_firstname                                      |
| MIDDLENAME                     | cdm\_middlename                                     |
| LASTNAME                       | cdm\_lastname                                       |
| WORKERTYPE                     | cdm\_type                                           |
| WORKERSTATUS                   | cdm\_status                                         |
| PRIMARYCONTACTEMAIL            | cdm\_primaryemailaddress                            |
| PRIMARYCONTACTPHONE            | cdm\_primarytelephone                               |
| PRIMARYCONTACTFACEBOOK         | cdm\_facebookidentity                               |
| PRIMARYCONTACTTWITTER          | cdm\_twitteridentity                                |
| PRIMARYCONTACTLINKEDIN         | cdm\_linkedinidentity                               |
| PRIMARYCONTACTURL              | cdm\_websiteurl                                     |
| เพศ                         | cdm\_gender                                         |
| BIRTHDATE                      | cdm\_birthdate                                      |
| ชื่อ                           | cdm\_fullname                                       |

### <a name="worker-bank-accounts-to-worker-bank-account"></a>บัญชีธนาคารของผู้ปฏิบัติงานให้กับบัญชีธนาคารของผู้ปฏิบัติงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATION          | cdm\_accountidentification                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONID         | cdm\_countryorregion                                |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSDISTRICTNAME            | cdm\_districtname                                   |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| BANKACCOUNTNUMBER              | cdm\_bankaccountnumber                              |
| BANKACCOUNTTYPE                | cdm\_bankaccounttype                                |
| อีเมล                          | cdm\_email                                          |
| EXTENSION                      | cdm\_extension                                      |
| FAX                            | cdm\_fax                                            |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| ROUTINGNUMBER                  | cdm\_routingnumber                                  |
| TELEPHONE                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telexnumber                                    |
| BANKIBAN                       | cdm\_iban                                           |
| SWIFTNO                        | cdm\_swiftcode                                      |
| BANKLOCATIONCODE               | cdm\_banklocationcode                               |
| BRANCHNAME                     | cdm\_branchname                                     |
| BRANCHNUMBER                   | cdm\_branchnumber                                   |
| ROUTINGNUMBERTYPE              | cdm\_routingnumbertype                              |
| ACCOUNTHOLDER                  | cdm\_accountholder                                  |
| NAMEOFPERSON                   | cdm\_nameofperson                                   |
| ชื่อ                           | cdm\_description                                    |
| ADDRESSSTREET                  | cdm\_line1                                          |
| ADDRESSSTREETNUMBER            | cdm\_line2                                          |

### <a name="worker-personal-details-to-worker-personal-detail"></a>รายละเอียดส่วนตัวของผู้ปฏิบัติงานให้กับรายละเอียดส่วนตัวของผู้ปฏิบัติงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| BIRTHDATE                      | cdm\_birthdate                                      |
| PERSONBIRTHCITY                | cdm\_birthcity                                      |
| เพศ                         | cdm\_gender                                         |
| EXPATRIATEENDDATE              | cdm\_expatriateenddate                              |
| EXPATRIATESTARTDATE            | cdm\_expatriatestartdate                            |
| DISABLEDVETERAN                | cdm\_isdisabledveteran                              |
| DECEASEDDATE                   | cdm\_deceaseddate                                   |
| DISABLEDVERIFICATIONDATE       | cdm\_disabledveteranverificationdate                |
| EDUCATION                      | cdm\_education                                      |
| ETHNICORIGINID                 | cdm\_ethnicoriginid.cdm\_name                        |
| ISDISABLED                     | cdm\_isdisabled                                     |
| ISFULLTIMESTUDENT              | cdm\_isfulltimestudent                              |
| ISEXPATRIATERULINGAPPLICABLE   | cdm\_isexpatriaterulingapplicable                   |
| MARITALSTATUS                  | cdm\_maritalstatus                                  |
| MILITARYSERVICESTARTDATE       | cdm\_militaryservicestartdate                       |
| MILITARYSERVICEENDDATE         | cdm\_militaryserviceenddate                         |
| NUMBEROFDEPENDENTS             | cdm\_numberofdependents                             |
| NATIVELANGUAGEID               | cdm\_nativelanguageidid.cdm\_name                    |
| NATIONALITYCOUNTRYREGION       | cdm\_nationalitycountryregion                       |
| PERSONBIRTHCOUNTRYREGION       | cdm\_birthcountryregion                             |
| FATHERBIRTHCOUNTRYREGION       | cdm\_fatherbirthcountryregion                       |
| MOTHERBIRTHCOUNTRYREGION       | cdm\_motherbirthcountryregion                       |
| CITIZENSHIPCOUNTRYREGION       | cdm\_citizenshipcountryregion                       |
| VETERANSTATUSID                | cdm\_veteranstatusid.cdm\_name                       |

### <a name="worker-postal-addresses-dual-write-to-worker-address"></a>การรวมแบบสองทิศทางของที่อยู่ไปรษณีย์ของผู้ปฏิบัติงานไปยังที่อยู่ของผู้ปฏิบัติงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| ADDRESSLOCATIONID              | cdm\_addressnumber                                  |
| ADDRESSLOCATIONROLES           | cdm\_addresstype                                    |
| EFFECTIVE                      | cdm\_effectivedate                                  |
| EXPIRATION                     | cdm\_expirationdate                                 |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSSTREETNUMBER            | cdm\_streetnumber                                   |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSCOUNTYID                | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_description                                    |
| ADDRESSLATITUDE                | cdm\_latitude                                       |
| ADDRESSLONGITUDE               | cdm\_longitude                                      |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ISPRIMARY                      | cdm\_ispreferred                                    |

### <a name="working-time-to-work-calendar-time-interval"></a>เวลาการทำงานให้กับช่วงเวลาในปฏิทินการทำงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ENDTIME                        | cdm\_endtime                                        |
| STARTTIME                      | cdm\_starttime                                      |
| WORKCALENDARDATE               | cdm\_workcalendardayid.cdm\_calendardate             |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKCALENDARID                 | cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name  |

### <a name="working-times-to-work-calendar-day"></a>เวลาการงานไปยังวันในปฏิทินงาน

| เอนทิตี้การเงิน                 | ตาราง Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARDATE                   | cdm\_calendardate                                   |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKINGDAYDEFINITION           | cdm\_status                                         |

## <a name="integration-considerations"></a>ข้อควรพิจารณาในการรวม

- การเปลี่ยนแปลงทั้งหมดที่ได้กับข้อมูลในระบบใดระบบหนึ่งจะต้องได้รับการตรวจสอบความถูกต้องโดยระบบอื่น ถ้าเกิดความล้มเหลวเกิดขึ้น ข้อมูลจะไม่เขียนในระบบใดระบบหนึ่ง 
- การเขียนทั้งหมดจะขึ้นอยู่กับการตั้งค่าเริ่มต้นของข้อมูล (ถ้าตรรกะที่กำหนดเองเกิดขึ้นในการเงิน)
- แอปพลิเคชันตัวรวมการรวมแบบสองทิศทางใช้คีย์การรวมเพื่อแมประหว่างสองระบบ บางครั้ง การเลือกคีย์การรวมที่ถูกต้องเป็นเรื่องยาก โดยเฉพาะอย่างยิ่งถ้าคีย์การรวมหลายคีย์ตอบสนองความต้องการ เพื่อช่วยในการเลือกนี้ ตารางต่อไปนี้จะแสดงรายการคีย์การรวมที่แนะนำสำหรับการแมปของคุณ

| ตาราง Dataverse                          | คีย์การรวม |
|------------------------------------------|------------------|
| การเบิกจ่ายเงินของบัญชีธนาคาร                | cdm\_bankaccountid.cdm\_accountidentification, cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| ความถี่ในการคำนวณสวัสดิการ            | cdm\_name |
| รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ | cdm\_payperiodid.cdm\_periodstartdate, cdm\_payperiodid.cdm\_paycycleid.cdm\_name, cdm\_benefitcalculationfrequencyid.cdm\_name |
| อัตราการคำนวณสวัสดิการ                 | cdm\_name |
| รายละเอียดอัตราการคำนวณสวัสดิการ          | cdm\_workerdeduction, cdm\_effective, cdm\_calculationrateid.cdm\_name |
| ตัวเลือกสวัสดิการ                           | cdm\_name |
| ชนิดของสวัสดิการ                             | cdm\_name |
| ปฏิทินกระบวนการทางธุรกิจ                | cdm\_name |
| การกำหนดกลุ่มกระบวนการทางธุรกิจ        | cdm\_name |
| ส่วนหัวของกระบวนการทางธุรกิจ                  | cdm\_processid |
| กลุ่มงานไลบรารีกระบวนการทางธุรกิจ      | cdm\_processtype, cdm\_name |
| ระยะของกระบวนการทางธุรกิจ                   | cdm\_name, cdm\_businessprocesstype, cdm\_companyid.cdm\_companycode |
| งานของกระบวนการทางธุรกิจ                    | cdm\_taskid |
| หน่วยธุรกิจ                            | |
| ส่วนหัวเทมเพลตรายการตรวจสอบ                | cdm\_businessprocesstype, cdm\_name, cdm\_genericsubtype |
| งานเทมเพลตรายการตรวจสอบ                  | cdm\_taskid |
| บริษัท                                  | cdm\_companycode |
| แผนค่าตอบแทนคงที่                  | cdm\_name, cdm\_company.cdm\_companycode |
| กริดค่าตอบแทน                        | cdm\_name, cdm\_companyid.cdm\_companycode |
| ระดับค่าตอบแทน                       | cdm\_name |
| ความถี่ในการจ่ายค่าตอบแทน               | cdm\_name, cdm\_companyid.cdm\_companycode |
| การตั้งค่าจุดอ้างอิงค่าตอบแทน       | cdm\_name, cdm\_companyid.cdm\_companycode |
| รายการการตั้งค่าจุดอ้างอิงค่าตอบแทน  | cdm\_name, cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode |
| ภูมิภาคของค่าตอบแทน                      | cdm\_name |
| โครงสร้างค่าตอบแทน                   | cdm\_compensationlevelid.cdm\_name, cdm\_referencepointid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_compensationgridid.cdm\_name, cdm\_compensationgridid.cdm\_companyid.cdm\_companycode |
| แผนค่าตอบแทนผันแปร               | cdm\_name, cdm\_companyid.cdm\_companycode |
| ระดับแผนค่าตอบแทนผันแปร         | cdm\_companyid.cdm\_companycode, cdm\_compensationvariableplanid.cdm\_name, cdm\_compensationvariableplanid.cdm\_companyid.cdm\_companycode, cdm\_compensationlevelid.cdm\_name |
| ชนิดแผนค่าตอบแทนผันแปร          | cdm\_name, cdm\_companyid.cdm\_companycode |
| สกุลเงิน                                 | isocurrencycode |
| แผนก                               | cdm\_departmentnumber |
| การจ้างงาน                               | cdm\_employmentstartdate, cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| เชื้อชาติ                            | cdm\_name |
| เหตุการณ์ค่าตอบแทนคงที่                 | cdm\_name, cdm\_companyid.cdm\_companycode |
| หน้าที่                                      | cdm\_name |
| ฟังก์ชันงาน                             | cdm\_name |
| ตำแหน่งงาน                             | cdm\_jobpositionnumber |
| มิติตำแหน่งงาน                   | cdm\_jobpositionid.cdm\_jobpositionnumber, cdm\_companyid.cdm\_companycode |
| ชนิดงาน                                 | cdm\_name |
| ภาษา                                 | cdm\_name |
| ธุรกรรมธนาคารวันลา                   | cdm\_transactiondate, cdm\_transactiontype, cdm\_transactionnumber, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| การลงทะเบียนการลาหยุด                         | cdm\_startdate, cdm\_leaveplanid.cdm\_name, cdm\_leaveplanid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| แผนการลาหยุด                               | cdm\_name, cdm\_companyid.cdm\_companycode |
| การขอลา                            | cdm\_leaverequestnumber, cdm\_companyid.cdm\_companycode |
| รายละเอียดคำขอการลางาน                     | cdm\_leavedate, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_leaverequestid.cdm\_leaverequestnumber, cdm\_leaverequestid.cdm\_companyid.cdm\_companycode |
| ชนิดการลา                               | cdm\_type, cdm\_companyid.cdm\_companycode |
| รหัสเหตุผลชนิดการลา                   | cdm\_reasoncodeid.cdm\_name, cdm\_typeid.cdm\_type, cdm\_typeid.cdm\_companyid.cdm\_companycode |
| ส่วนหัวของกระบวนการเตรียมความพร้อม                   | cdm\_processheaderid.cdm\_processid |
| องค์กร                             | |
| รอบการชำระค่าจ้าง                                | cdm\_name |
| รอบระยะเวลาการชำระค่าจ้าง                               | cdm\_periodstartdate, cdm\_paycycleid.cdm\_name, cdm\_periodenddate |
| รหัสรายได้ค่าจ้าง                     | cdm\_name |
| รายละเอียดตำแหน่งดูแลค่าจ้าง                  | cdm\_validfrom, cdm\_validto, cdm\_position.cdm\_jobpositionnumber |
| หน่วยงานที่ออกรหัสประจำตัวของบุคคล     | cdm\_name |
| ชนิดตำแหน่ง                            | cdm\_name |
| การกำหนดตำแหน่งของผู้ปฏิบัติงาน               | cdm\_validfrom, cdm\_jobpositionid.cdm\_jobpositionnumber |
| รหัสเหตุผล                              | cdm\_name |
| ชนิดทักษะ                               | cdm\_name |
| ภูมิภาคการเก็บภาษี                               | cdm\_stateorprovince, cdm\_name, cdm\_countryorregion, cdm\_county, cdm\_city |
| ทีมงาน                                     | azureactivedirectoryobjectid, membershiptype |
| ตำแหน่ง                                    | cdm\_name |
| ผู้ใช้                                     | azureactivedirectoryobjectid |
| กฎสิทธิ์พึงได้                             | cdm\_name, cdm\_companyid.cdm\_companycode |
| สถานะทหารผ่านศึก                           | cdm\_name |
| ปฏิทินการทำงาน                            | cdm\_name, cdm\_companyid.cdm\_companycode |
| วันในปฏิทินงาน                        | cdm\_calendardate, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| การลงทะเบียนในปฏิทินการทำงาน                 | cdm\_employmentid.cdm\_employmentstartdate, cdm\_employmentid.cdm\_workerid.cdm\_workernumber, cdm\_employmentid.cdm\_companyid.cdm\_companycode |
| วันหยุดในปฏิทินการทำงาน                    | cdm\_name |
| รายการวันหยุดในปฏิทินงาน               | cdm\_holidaydate, cdm\_workcalendarholidayid.cdm\_name |
| ช่วงเวลาในปฏิทินงาน              | cdm\_starttime, cdm\_workcalendardayid.cdm\_calendardate, cdm\_workcalendardayid.cdm\_companyid.cdm\_companycode, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| ผู้ปฏิบัติงาน                                   | cdm\_workernumber |
| ที่อยู่ของผู้ปฏิบัติงาน                           | cdm\_addressnumber, cdm\_addresstype, cdm\_workerid.cdm\_workernumber |
| บัญชีธนาคารของผู้ปฏิบัติงาน                      | cdm\_accountidentification, cdm\_workerid.cdm\_workernumber |
| ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน                | cdm\_linenumber, cdm\_effectivedate, cdm\_companyid.cdm\_companycode, cdm\_positionid.cdm\_jobpositionnumber, cdm\_workerid.cdm\_workernumber, cdm\_eventid.cdm\_name, cdm\_eventid.cdm\_companyid.cdm\_companycode, cdm\_planid.cdm\_name, cdm\_planid.cdm\_company.cdm\_companycode |
| หมายเลขรหัสของผู้ปฏิบัติงาน      | cdm\_identificationnumber, cdm\_workerid.cdm\_workernumber, cdm\_identificationtypeid.cdm\_name |
| ชนิดรหัสของผู้ปฏิบัติงาน        | cdm\_name |
| รายละเอียดส่วนตัวของผู้ปฏิบัติงาน                   | cdm\_workerid.cdm\_workernumber |
