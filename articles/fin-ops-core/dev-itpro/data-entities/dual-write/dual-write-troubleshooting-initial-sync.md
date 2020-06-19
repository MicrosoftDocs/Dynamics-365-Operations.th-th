---
title: แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410092"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น

[!include [banner](../../includes/banner.md)]

หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>ตรวจสอบข้อผิดพลาดของการซิงโครไนส์เริ่มต้นในแอป Finance and Operations

หลังจากที่คุณเปิดใช้งานเท็มเพลตการแม็ป สถานะของแผนที่ควรเป็น **กำลังรัน** ถ้าสถานะ **ไม่ได้รันอยู่** ข้อผิดพลาดเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น เมื่อต้องการดูข้อผิดพลาด ให้เลือกแท็บ **รายละเอียดการซิงค์เริ่มต้น** บนหน้า **การรวมแบบสองทิศทาง**

![แท็บรายละเอียดการซิงค์เริ่มต้น](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>คุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้: 400 คำขอไม่ถูกต้อง

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามรันการแม็ปและการซิงโครไนส์เริ่มต้น:

*เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (400) คำขอไม่ถูกต้อง) AX การส่งออกพบข้อผิดพลาด*

นี่เป็นตัวอย่างของข้อความแสดงข้อผิดพลาดทั้งหมด

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

ถ้าเกิดข้อผิดพลาดนี้อย่างสม่ำเสมอ และคุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้ ให้ทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหานี้

1. ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations
2. เปิด Microsoft Management Console
3. ในบานหน้าต่าง **บริการ** ตรวจสอบให้แน่ใจว่ามีการเรียกใช้บริการกรอบงานการนำเข้าการส่งออกข้อมูล Microsoft Dynamics 365 เริ่มต้นใหม่ ถ้าถูกหยุดเนื่องจากการซิงโครไนส์เริ่มต้นต้องการ

## <a name="initial-synchronization-error-403-forbidden"></a>ข้อผิดพลาดการซิงโครไนส์เริ่มต้น: 403 ไม่ได้รับอนุญาต

คุณอาจได้รับข้อความแสดงข้อผิดพลาดในระหว่างการซิงโครไนส์เริ่มต้น:

*(\[ไม่ได้รับอนุญาต\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต) AX การส่งออกพบข้อผิดพลาด*

เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้แอป Finance and Operations
2. บนหน้า **แอพลิเคชัน Azure Active Directory** ให้ลบไคลเอนต์ **DtAppID** และจากนั้น เพิ่มใหม่อีกครั้ง

![รายการของแอพลิเคชัน Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>ความล้มเหลวในการอ้างอิงตนเองหรือการอ้างอิงหมุนเวียนในระหว่างการซิงโครไนส์เริ่มต้น

คุณอาจได้รับข้อความแสดงข้อผิดพลาด ถ้าการแม็ปใดๆ ของคุณมีการอ้างอิงตนเองหรือการอ้างอิงหมุนเวียน ข้อผิดพลาดจะอยู่ในประเภทเหล่านี้:

- [ผู้จัดจำหน่าย V2 สำหรับการแม็ปเอนทิตี msdyn_vendors](#error-vendor-map)
- [ลูกค้า V3 สำหรับการแม็ปเอนทิตีบัญชี](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>แก้ไขข้อผิดพลาดในผู้จัดจำหน่าย V2 สำหรับการแม็ปเอนทิตี msdyn_vendors

คุณอาจพบข้อผิดพลาดในการซิงค์เริ่มต้นต่อไปนี้ใน **ผู้จัดจำหน่าย V2** สำหรับการแม็ป **msdyn_vendors** ถ้าเอนทิตีมีเรกคอร์ดที่มีอยู่ซึ่งมีค่าในฟิลด์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber** การทำเช่นนี้เนื่องจาก **InvoiceVendorAccountNumber** เป็นฟิลด์ที่อ้างอิงถึงตนเอง และ **PrimaryContactPersonId** เป็นการอ้างอิงหมุนเวียนในการแม็ปผู้จัดจำหน่าย

*ไม่สามารถแก้ไข guid สำหรับฟิลด์: <field> ไม่พบการค้นหา: <value> ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

นี่คือตัวอย่างสองรายการ:

- *ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn_vendorprimarycontactperson msdyn_contactpersonid ไม่พบการค้นหา: 000056 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber ไม่พบการค้นหา: V24-1 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

ถ้าคุณมีเรกคอร์ดที่มีค่าในฟิลด์เหล่านี้ในเอนทิตีของผู้จัดจำหน่าย ให้ทำตามขั้นตอนในส่วนด้านล่างเพื่อทำการซิงค์เริ่มต้นให้เสร็จเรียบร้อย

1. ในแอป Finance and Operations ให้ลบฟิลด์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber** จากการแม็ป และบันทึกการเปลี่ยนแปลง

    1. นำทางไปยังหน้าการแม็ปการรวมแบบสองทิศทางสำหรับ **ผู้จัดจำหน่าย V2 (msdyn_vendors)** และเลือกแท็บ **การแม็ปเอนทิตี** ในตัวกรองด้านซ้าย ให้เลือก **แอป Finance and Operations ผู้จัดจำหน่าย V2** ในตัวกรองสิทธิ์ เลือก **Sales.Vendor**

    2. ค้นหา **primarycontactperson** เพื่อค้นหาฟิลด์ต้นทาง **PrimaryContactPersonId**
    
    3. คลิกปุ่ม **การดำเนินการ** แล้วเลือก **ลบ**
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 3](media/vend_selfref3.png)
    
    4. ทำซ้ำเพื่อลบฟิลด์ **InvoiceVendorAccountNumber**
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 4](media/vend-selfref4.png)
    
    5. บันทึกการเปลี่ยนแปลงการแม็ป

2. ปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับเอนทิตี **ผู้จัดจำหน่าย V2**

    1. นำทางไปยัง **การจัดการข้อมูล \> เอนทิตีข้อมูล**
    
    2. เลือกเอนทิตี **ผู้จัดจำหน่าย V2**
    
    3. คลิก **ตัวเลือก** จากแถบเมนู แล้วจากนั้น **เปลี่ยนแปลงการติดตาม**
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 5](media/selfref_options.png)
    
    4. คลิก **ปิดใช้งานเปลี่ยนแปลงการติดตาม**
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 6](media/selfref_tracking.png)

3. รันการซิงค์เริ่มต้นของการแม็ป **ผู้จัดจำหน่าย V2 (msdyn_vendors)** การซิงค์เริ่มต้นควรรันเสร็จเรียบร้อยโดยไม่มีข้อผิดพลาดใดๆ

4. รันการซิงค์เริ่มต้นสำหรับการแม็ป **ผู้ติดต่อของ CDS V2 (ผู้ติดต่อ)** คุณต้องซิงค์การแม็ปนี้ ถ้าคุณต้องการซิงค์ฟิลด์ผู้ติดต่อหลักบนเอนทิตีของผู้จัดจำหน่าย เนื่องจากเรกคอร์ดผู้ติดต่อยังต้องมีการซิงค์เริ่มต้นด้วย

5. เพิ่มฟิลด์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber** กลับไปยังการแม็ป **ผู้จัดจำหน่าย V2 (msdyn_vendors)** และบันทึกการแม็ป

6. รันการซิงค์เริ่มต้นอีกครั้งสำหรับการแม็ป **ผู้จัดจำหน่าย V2 (msdyn_vendors)** เรกคอร์ดทั้งหมดจะถูกซิงค์ เนื่องจากมีการปิดใช้งานการติดตามการเปลี่ยนแปลง

7. เปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับเอนทิตี **ผู้จัดจำหน่าย V2**

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>แก้ไขข้อผิดพลาดในลูกค้า V3 สำหรับการแม็ปเอนทิตีบัญชี

คุณอาจพบข้อผิดพลาดในการซิงค์เริ่มต้นต่อไปนี้ใน **ลูกค้า V3** สำหรับการแม็ป **บัญชี** ถ้าเอนทิตีมีเรกคอร์ดที่มีอยู่ซึ่งมีค่าในฟิลด์ **ContactPersonID** และ **InvoiceAccount** การทำเช่นนี้เนื่องจาก **InvoiceAccount** เป็นฟิลด์ที่อ้างอิงตนเอง และ **ContactPersonID** เป็นการอ้างอิงหมุนเวียนในการแม็ปผู้จัดจำหน่าย

*ไม่สามารถแก้ไข guid สำหรับฟิลด์: <field> ไม่พบการค้นหา: <value> ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *ไม่สามารถแก้ไข guid สำหรับฟิลด์: primarycontactid.msdyn_contactpersonid ไม่พบการค้นหา: 000056 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn_billingaccount.accountnumber ไม่พบการค้นหา: 1206-1 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

ถ้าคุณมีเรกคอร์ดที่มีค่าในฟิลด์เหล่านี้ในเอนทิตีของลูกค้า ให้ทำตามขั้นตอนในส่วนด้านล่างเพื่อทำการซิงค์เริ่มต้นให้เสร็จเรียบร้อย คุณสามารถใช้วิธีการนี้สำหรับเอนทิตีแบบสำเร็จรูปใดๆ เช่น ลูกค้าองค์กร และผู้ติดต่อ

1. ในแอป Finance and Operations เพิ่มฟิลด์ **ContactPersonID** และ **InvoiceAccount** จากการแม็ป **ลูกค้า V3 (บัญชี)** และบันทึกการแม็ป

    1. นำทางไปยังหน้าการแม็ปการรวมแบบสองทิศทางสำหรับ **ลูกค้า V3 (บัญชี)** และเลือกแท็บ **การแม็ปเอนทิตี** ในตัวกรองด้านซ้าย ให้เลือก **Finance and Operations app.Customers V3** ในตัวกรองสิทธิ์ เลือก **Common Data Service.Account**

    2. ค้นหา **contactperson** เพื่อค้นหาฟิลด์ต้นทาง **ContactPersonID**
    
    3. คลิกปุ่ม **การดำเนินการ** แล้วเลือก **ลบ**
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 3](media/cust_selfref3.png)
    
    4. ทำซ้ำเพื่อลบฟิลด์ **InvoiceAccount**
    
        ![การอ้างอิงตนเองหรือหมุนเวียน](media/cust_selfref4.png)
    
    5. บันทึกการเปลี่ยนแปลงการแม็ป

2. ปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับเอนทิตี **ลูกค้า V3**

    1. นำทางไปยัง **การจัดการข้อมูล \> เอนทิตีข้อมูล**
    
    2. เลือกเอนทิตี **ลูกค้า V3**
    
    3. คลิก **ตัวเลือก** จากแถบเมนู แล้วจากนั้น **เปลี่ยนแปลงการติดตาม**
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 5](media/selfref_options.png)
    
    4. คลิก **ปิดใช้งานเปลี่ยนแปลงการติดตาม**
    
        ![การอ้างอิงตนเองหรือหมุนเวียน 6](media/selfref_tracking.png)

3. รันการซิงค์เริ่มต้นสำหรับการแม็ป **ลูกค้า V3 (บัญชี)** การซิงค์เริ่มต้นควรรันเสร็จเรียบร้อยโดยไม่มีข้อผิดพลาดใดๆ

4. รันการซิงค์เริ่มต้นสำหรับการแม็ป **ผู้ติดต่อของ CDS V2 (ผู้ติดต่อ)** มี 2 แผนที่ที่มีชื่อเดียวกัน เลือกหนึ่งรายการที่มีคำอธิบาย **แม่แบบการรวมแบบสองทิศทางสำหรับการซิงค์ระหว่าง FO.CDS Vendor Contacts V2 ไปยัง CDS.Contacts ต้องมีแพคเกจใหม่ \[Dynamics365SupplyChainExtended\]** บนแท็บ **รายละเอียด** ของแผนที่

5. เพิ่มฟิลด์ **InvoiceAccount** และ **ContactPersonId** กลับไปยังการแม็ป **ลูกค้า V3 (บัญชี)** และบันทึกการแม็ป ตอนนี้ทั้งฟิลด์ **InvoiceAccount** และฟิลด์ **ContactPersonId** เป็นส่วนหนึ่งของโหมดการซิงค์ที่เริ่มใช้งานจริงอีกครั้ง ในขั้นตอนถัดไป คุณดำเนินการซิงค์เริ่มต้นสำหรับฟิลด์เหล่านี้ให้เสร็จสมบูรณ์

6. รันการซิงค์เริ่มต้นอีกครั้งสำหรับการแม็ป **ลูกค้า V3 (บัญชี)** เนื่องจากการติดตามการเปลี่ยนแปลงถูกปิดใช้งาน การรันการซิงค์จะซิงค์ข้อมูลสำหรับ **InvoiceAccount** และ **ContactPersonId** จากแอป Finance and Operations ไปยัง Common Data Service

7. เมื่อต้องการซิงค์ข้อมูลสำหรับ **InvoiceAccount** และ **ContactPersonId** จาก Common Data Service ไปยัง Finance and Operations คุณใช้โครงการการรวมข้อมูล

    1. ใน Power Apps ให้สร้างโครงการการรวมข้อมูลระหว่างเอนทิตี **Sales.Account** และ **Finance and Operations apps.Customers V3** ทิศทางของข้อมูลต้องมาจาก Common Data Service ไปยังแอป Finance and Operations  เนื่องจาก **InvoiceAccount** เป็นแอททริบิวต์ใหม่ในการรวมแบบสองทิศทาง คุณอาจต้องการข้ามการซิงค์เริ่มต้นสำหรับแอททริบิวต์นี้ สำหรับข้อมูลเพิ่มเติม ดู [รวมข้อมูลลงใน Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator)

        รูปภาพต่อไปนี้แสดงโครงการที่ปรับปรุง **CustomerAccount** และ **ContactPersonId**

        ![การอ้างอิงตนเองหรือหมุนเวียน](media/cust_selfref6.png)

    2. เพิ่มเงื่อนไขของบริษัทในตัวกรองในฝั่ง Common Data Service เนื่องจากมีการปรับปรุงเฉพาะเรกคอร์ดที่ตรงกับเงื่อนไขตัวกรองในแอป Finance and Operations เมื่อต้องการเพิ่มตัวกรอง ให้คลิกไอคอนตัวกรอง ในกล่องโต้ตอบ **แก้ไขการสอบถาม** คุณสามารถเพิ่มการสอบถามตัวกรอง เช่น **_msdyn_company_value eq '\<guid\>'** ถ้าไม่มีไอคอนตัวกรองอยู่ ให้สร้างตั๋วสนับสนุนเพื่อขอทีมงานการรวมข้อมูลเพื่อเปิดใช้งานความสามารถในการกรองของผู้เช่าของคุณ ถ้าคุณไม่ได้ป้อนการสอบถามตัวกรองสำหรับ **_msdyn_company_value** เรกคอร์ดทั้งหมดจะถูกซิงค์

        ![การอ้างอิงตนเองหรือหมุนเวียน](media/cust_selfref7.png)

        การดำเนินการนี้จะทำให้การซิงค์เริ่มต้นของเรกคอร์ดเสร็จสิ้น

8. เปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับเอนทิตี **ลูกค้า V3** ในแอป Finance and Operations

