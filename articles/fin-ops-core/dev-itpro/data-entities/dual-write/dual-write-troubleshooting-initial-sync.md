---
title: แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9a6be5f4e08a92171892549c017c15c66b1bde2e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350823"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>ตรวจสอบข้อผิดพลาดของการซิงโครไนส์เริ่มต้นในแอป Finance and Operations

หลังจากที่คุณเปิดใช้งานเท็มเพลตการแม็ป สถานะของแผนที่ควรเป็น **กำลังรัน** ถ้าสถานะ **ไม่ได้รันอยู่** ข้อผิดพลาดเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น เมื่อต้องการดูข้อผิดพลาด ให้เลือกแท็บ **รายละเอียดการซิงค์เริ่มต้น** บนหน้า **การรวมแบบสองทิศทาง**

![ข้อผิดพลาดในแท็บรายละเอียดการซิงค์เริ่มต้น](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>คุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้: 400 คำขอไม่ถูกต้อง

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามรันการแม็ปและการซิงโครไนส์เริ่มต้น:

*(\[คำขอไม่ถูกต้อง\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (400) คำขอไม่ถูกต้อง) AX การส่งออกพบข้อผิดพลาด*

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

![ไคลเอนต์ DtAppID ในรายการของแอพลิเคชัน Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>ความล้มเหลวในการอ้างอิงตนเองหรือการอ้างอิงหมุนเวียนในระหว่างการซิงโครไนส์เริ่มต้น

คุณอาจได้รับข้อความแสดงข้อผิดพลาด ถ้าการแม็ปใดๆ ของคุณมีการอ้างอิงตนเองหรือการอ้างอิงหมุนเวียน ข้อผิดพลาดจะอยู่ในประเภทเหล่านี้:

- [ข้อผิดพลาดในผู้จัดจำหน่าย V2–สำหรับ–การแม็ปตาราง msdyn_vendors](#error-vendor-map)
- [ข้อผิดพลาดในลูกค้า V3–สำหรับ–การแม็ปตารางบัญชี](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>แก้ไขข้อผิดพลาดในผู้จัดจำหน่าย V2–สำหรับ–การแม็ปตาราง msdyn_vendors

คุณอาจพบข้อผิดพลาดในการซิงโครไนส์เริ่มต้นสำหรับการแม็ปของ **ผู้จัดจำหน่าย V2** สำหรับ **msdyn\_vendors** ถ้าตารางมีแถวที่มีอยู่ที่ซึ่งมีค่าในคอลัมน์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber** ข้อผิดพลาดเหล่านี้เกิดขึ้นเนื่องจาก **InvoiceVendorAccountNumber** เป็นคอลัมน์ที่อ้างอิงถึงตนเอง และ **PrimaryContactPersonId** เป็นการอ้างอิงหมุนเวียนในการแม็ปผู้จัดจำหน่าย

ข้อความแสดงข้อผิดพลาดที่คุณได้รับจะมีฟอร์มต่อไปนี้

*ไม่สามารถแก้ไข guid สำหรับฟิลด์: \<field\> ไม่พบการค้นหา: \<value\> ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

ยกตัวอย่างเช่น

- *ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid ไม่พบการค้นหา: 000056 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber ไม่พบการค้นหา: V24-1 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

ถ้าแถวใดๆ ในตารางของผู้จัดจำหน่ายมีค่าในคอลัมน์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber** ให้ทำตามขั้นตอนเหล่านี้เพื่อทำให้การซิงโครไนส์เริ่มต้นเสร็จสมบูรณ์

1. ในแอป Finance and Operations ให้ลบคอลัมน์ **PrimaryContactPersonId** และคอลัมน์ **InvoiceVendorAccountNumber** จากการแม็ป และจากนั้น บันทึกการแม็ป

    1. บนหน้าการแม็ปการรวมแบบสองทิศทางสำหรับ **ผู้จัดจำหน่าย V2 (msdyn\_vendors)** บนแท็บ **การแม็ปตาราง** ในตัวกรองด้านซ้าย ให้เลือก **Finance and Operations apps.Vendors V2** ในตัวกรองสิทธิ์ เลือก **Sales.Vendor**
    2. ค้นหา **primarycontactperson** เพื่อค้นหาคอลัมน์ต้นทาง **PrimaryContactPersonId**
    3. เลือก **การดำเนินการ** แล้วจากนั้น เลือก **ลบ**

        ![การลบคอลัมน์ PrimaryContactPersonId](media/vend_selfref3.png)

    4. ทำซ้ำขั้นตอนเหล่านี้เพื่อลบคอลัมน์ **InvoiceVendorAccountNumber**

        ![การลบคอลัมน์ InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. บันทึกการเปลี่ยนแปลงของคุณไปยังการแม็ป

2. ปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับตาราง **ผู้จัดจำหน่าย V2**

    1. ในพื้นที่ทำงาน **การจัดการข้อมูล** เลือกไทล์ **ตารางข้อมูล**
    2. เลือกตาราง **ผู้จัดจำหน่าย V2**
    3. ในบานหน้าต่างการดำเนินการ ให้เลือก **ตัวเลือก** แล้วจากนั้น เลือก **การติดตามการเปลี่ยนแปลง**

        ![การเลือกตัวเลือกการติดตามการเปลี่ยนแปลง](media/selfref_options.png)

    4. เลือก **ปิดใช้งานการติดตามการเปลี่ยนแปลง**

        ![การเลือกปิดใช้งานการติดตามการเปลี่ยนแปลง](media/selfref_tracking.png)

3. รันการซิงโครไนส์เริ่มต้นสำหรับการแม็ป **ผู้จัดจำหน่าย V2 (msdyn\_vendors)** การซิงโครไนส์เริ่มต้นควรรันเสร็จเรียบร้อย โดยไม่มีข้อผิดพลาดใดๆ
4. รันการซิงโครไนส์เริ่มต้นสำหรับการแม็ป **ผู้ติดต่อของ CDS V2 (ผู้ติดต่อ)** คุณต้องซิงค์การแม็ปนี้ ถ้าคุณต้องการซิงค์คอลัมน์ผู้ติดต่อหลักบนตารางของผู้จัดจำหน่าย เนื่องจากยังต้องทำการซิงโครไนส์เริ่มต้นสำหรับแถวผู้ติดต่อด้วย
5. เพิ่มคอลัมน์ **PrimaryContactPersonId** และคอลัมน์ **InvoiceVendorAccountNumber** กลับไปยังการแม็ป **ผู้จัดจำหน่าย V2 (msdyn\_vendors)** และจากนั้น บันทึกการแม็ป
6. รันการซิงโครไนส์เริ่มต้นอีกครั้งสำหรับการแม็ป **ผู้จัดจำหน่าย V2 (msdyn\_vendors)** เนื่องจากมีการปิดใช้งานการติดตามการเปลี่ยนแปลง แถวทั้งหมดจะถูกซิงค์
7. เปิดการติดตามการเปลี่ยนแปลงอีกครั้งสำหรับตาราง **ผู้จัดจำหน่าย V2**

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>แก้ไขข้อผิดพลาดในลูกค้า V3–สำหรับ–การแม็ปตารางบัญชี

คุณอาจพบข้อผิดพลาดในการซิงโครไนส์เริ่มต้นสำหรับการแม็ปของ **ลูกค้า V3** ไปยัง **บัญชี** ถ้าตารางมีแถวที่มีอยู่ที่ซึ่งมีค่าในคอลัมน์ **ContactPersonID** และคอลัมน์ **InvoiceAccount** ข้อผิดพลาดเหล่านี้เกิดขึ้นเนื่องจาก **InvoiceAccount** เป็นคอลัมน์ที่อ้างอิงตนเอง และ **ContactPersonID** เป็นการอ้างอิงหมุนเวียนในการแม็ปผู้จัดจำหน่าย

ข้อความแสดงข้อผิดพลาดที่คุณได้รับจะมีฟอร์มต่อไปนี้

*ไม่สามารถแก้ไข guid สำหรับฟิลด์: \<field\> ไม่พบการค้นหา: \<value\> ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

ยกตัวอย่างเช่น

- *ไม่สามารถแก้ไข guid สำหรับฟิลด์: primarycontactid.msdyn\_contactpersonid ไม่พบการค้นหา: 000056 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn\_billingaccount.accountnumber ไม่พบการค้นหา: 1206-1 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

ถ้าแถวใดๆ ในตารางของลูกค้ามีค่าในคอลัมน์ **ContactPersonID** และคอลัมน์ **InvoiceAccount** ให้ทำตามขั้นตอนเหล่านี้เพื่อทำให้การซิงโครไนส์เริ่มต้นเสร็จสมบูรณ์ คุณสามารถใช้วิธีการนี้สำหรับตารางแบบสำเร็จรูปใดๆ เช่น **บัญชี** และ **ผู้ติดต่อ**

1. ในแอป Finance and Operations ลบคอลัมน์ **ContactPersonID** และคอลัมน์ **InvoiceAccount** จากการแม็ป **ลูกค้า V3 (บัญชี)** และจากนั้น บันทึกการแม็ป

    1. บนหน้าการแม็ปการรวมแบบสองทิศทางสำหรับ **ลูกค้า V3 (บัญชี)** บนแท็บ **การแม็ปตาราง** ในตัวกรองด้านซ้าย ให้เลือก **Finance and Operations app.Customers V3** ในตัวกรองสิทธิ์ เลือก **Dataverse.Account**
    2. ค้นหา **contactperson** เพื่อค้นหาคอลัมน์ต้นทาง **ContactPersonID**
    3. เลือก **การดำเนินการ** แล้วจากนั้น เลือก **ลบ**

        ![การลบคอลัมน์ ContactPersonID](media/cust_selfref3.png)

    4. ทำซ้ำขั้นตอนเหล่านี้เพื่อลบคอลัมน์ **InvoiceAccount**

        ![การลบคอลัมน์ InvoiceAccount](media/cust_selfref4.png)

    5. บันทึกการเปลี่ยนแปลงของคุณไปยังการแม็ป

2. ปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับตาราง **ลูกค้า V3**

    1. ในพื้นที่ทำงาน **การจัดการข้อมูล** เลือกไทล์ **ตารางข้อมูล**
    2. เลือกตาราง **ลูกค้า V3**
    3. ในบานหน้าต่างการดำเนินการ ให้เลือก **ตัวเลือก** แล้วจากนั้น เลือก **การติดตามการเปลี่ยนแปลง**

        ![การเลือกตัวเลือกการติดตามการเปลี่ยนแปลง](media/selfref_options.png)

    4. เลือก **ปิดใช้งานการติดตามการเปลี่ยนแปลง**

        ![การเลือกปิดใช้งานการติดตามการเปลี่ยนแปลง](media/selfref_tracking.png)

3. รันการซิงโครไนส์เริ่มต้นสำหรับการแม็ป **ลูกค้า V3 (บัญชี)** การซิงโครไนส์เริ่มต้นควรรันเสร็จเรียบร้อย โดยไม่มีข้อผิดพลาดใดๆ
4. รันการซิงโครไนส์เริ่มต้นสำหรับการแม็ป **ผู้ติดต่อของ CDS V2 (ผู้ติดต่อ)**

    > [!NOTE]
    > มีแผนที่สองรายการที่มีชื่อเดียวกัน ตรวจสอบให้แน่ใจว่าได้เลือกแม็ปที่มีคำอธิบายต่อไปนี้บนแท็บ **รายละเอียด**: **แม่แบบการรวมแบบสองทิศทางสำหรับการซิงค์ระหว่าง FO.CDS Vendor Contacts V2 ไปยัง CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\]**

5. เพิ่มคอลัมน์ **InvoiceAccount** และคอลัมน์ **ContactPersonId** กลับไปยังการแม็ป **ลูกค้า V3 (บัญชี)** และจากนั้น บันทึกการแม็ป ตอนนี้ทั้งคอลัมน์ **InvoiceAccount** และคอลัมน์ **ContactPersonId** เป็นส่วนหนึ่งของโหมดการซิงโครไนส์ที่เริ่มใช้งานจริงอีกครั้ง ในขั้นตอนถัดไป คุณจะดำเนินการซิงค์เริ่มต้นสำหรับคอลัมน์เหล่านี้
6. รันการซิงโครไนส์เริ่มต้นอีกครั้งสำหรับการแม็ป **ลูกค้า V3 (บัญชี)** เนื่องจากการติดตามการเปลี่ยนแปลงถูกปิด จะมีการซิงค์ข้อมูลสำหรับ **InvoiceAccount** และ **ContactPersonId** จากแอป Finance and Operations ไปยัง Dataverse
7. เมื่อต้องการซิงค์ข้อมูลสำหรับ **InvoiceAccount** และ **ContactPersonId** จาก Dataverse ไปยังแอป Finance and Operations คุณต้องใช้โครงการการรวมข้อมูล

    1. ใน Power Apps ให้สร้างโครงการการรวมข้อมูลระหว่างตาราง **Sales.Account** และ **Finance and Operations apps.Customers V3** ทิศทางของข้อมูลต้องมาจาก Dataverse ไปยังแอป Finance and Operations เนื่องจาก **InvoiceAccount** เป็นแอททริบิวต์ใหม่ในการรวมแบบสองทิศทาง คุณอาจต้องการข้ามการซิงโครไนส์เริ่มต้นสำหรับแอททริบิวต์นี้ สำหรับข้อมูลเพิ่มเติม ดู [รวมข้อมูลลงใน Dataverse](/power-platform/admin/data-integrator)

        ภาพประกอบต่อไปนี้แสดงโครงการที่ปรับปรุง **CustomerAccount** และ **ContactPersonId**

        ![โครงการการรวมข้อมูลเพื่อปรับปรุง CustomerAccount และ ContactPersonId](media/cust_selfref6.png)

    2. เพิ่มเงื่อนไขของบริษัทในตัวกรองในฝั่ง Dataverse เพื่อให้เฉพาะแถวที่ตรงกับเงื่อนไขตัวกรองจะถูกปรับปรุงในแอป Finance and Operations เมื่อต้องการเพิ่มตัวกรอง ให้เลือกปุ่มตัวกรอง จากนั้น ในกล่องโต้ตอบ **แก้ไขการสอบถาม** คุณสามารถเพิ่มการสอบถามตัวกรอง เช่น **\_msdyn\_company\_value eq '\<guid\>'** 

        > [หมายเหตุ] ถ้าไม่มีปุ่มตัวกรองอยู่ ให้สร้างตั๋วการสนับสนุนเพื่อขอให้ทีมงานการรวมข้อมูลเปิดใช้งานความสามารถในการกรองของผู้เช่าของคุณ

        ถ้าคุณไม่ได้ป้อนการสอบถามตัวกรองสำหรับ **\_msdyn\_company\_value** แถวทั้งหมดจะถูกซิงค์

        ![การเพิ่มการสอบถามตัวกรอง](media/cust_selfref7.png)

    การซิงโครไนส์เริ่มต้นของแถวเสร็จสมบูรณ์ในขณะนี้

8. ในแอป Finance and Operations เปิดใช้งานการติดตามการเปลี่ยนแปลงอีกครั้งสำหรับตาราง **ลูกค้า V3**


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]