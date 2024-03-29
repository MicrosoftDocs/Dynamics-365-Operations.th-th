---
title: แก้ไขปัญหาจากการอัปเกรดแอปการเงินและการดำเนินงาน
description: บทความนี้จะให้ข้อมูลเกี่ยวกับการแก้ไขปัญหาซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการปรับรุ่นแอปการเงินและการดำเนินงาน
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7ab75c3a7b6c53982a32658f376a9fd148c023e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289558"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>แก้ไขปัญหาจากการอัปเกรดแอปการเงินและการดำเนินงาน

[!include [banner](../../includes/banner.md)]





บทความนี้แสดงข้อมูลการแก้ไขปัญหาสำหรับการรวมข้อมูลด้วยการรวมแบบสองทิศทางระหว่างแอปการเงินและการดำเนินงานกับ Dataverse กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการปรับรุ่นแอปการเงินและการดำเนินงาน

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของบทความนี้ อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="database-synchronization-errors"></a>ข้อผิดพลาดในการซิงโครไนส์ฐานข้อมูล

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้ เมื่อคุณพยายามใช้ตาราง **DualWriteProjectConfiguration** เพื่ออัปเดตแอปการเงินและการดำเนินงานเป็นการอัปเดตแพลตฟอร์ม 30

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอปการเงินและการดำเนินงาน
2. เปิด Visual Studio ในฐานะผู้ดูแลระบบ และเปิด Application Object Tree (AOT)
3. ค้นหา **DualWriteProjectConfiguration**
4. ใน AOT ให้คลิกขวาที่ **DualWriteProjectConfiguration** แล้วเลือก **เพิ่มไปยังโครงการใหม่** เลือก **ตกลง** เพื่อสร้างโครงการใหม่ที่ใช้ตัวเลือกเริ่มต้น
5. ใน Solution Explorer คลิกขวาที่ **คุณสมบัติโครงการ** และตั้งค่า **ซิงโครไนส์ฐานข้อมูลในการสร้าง** เป็น **จริง**
6. สร้างโครงการ และยืนยันว่าการสร้างเสร็จเรียบร้อยแล้ว
7. บนเมนู **Dynamics 365** เลือก **ซิงโครไนส์ฐานข้อมูล**
8. เลือก **ซิงโครไนส์** เพื่อทำการซิงโครไนส์ฐานข้อมูลแบบเต็ม
9. หลังจากการซิงโครไนส์ฐานข้อมูลทั้งหมดเสร็จเรียบร้อยแล้ว เรียกใช้ขั้นตอนการซิงโครไนส์ฐานข้อมูลอีกครั้งใน Microsoft Dynamics Lifecycle Services (LCS) และใช้สคริปต์การอัพเกรดด้วยตนเองตามความเหมาะสม เพื่อให้คุณสามารถดำเนินการปรับปรุงต่อไปได้

## <a name="missing-table-columns-issue-on-maps"></a>ปัญหาคอลัมน์ตารางที่ขาดหายไปในแผนผัง

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

บนหน้า **การรวมแบบสองทิศทาง** คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:

*ฟิลด์แหล่งข้อมูลที่ขาดหายไป \<field name\> ในเค้าร่าง*

![ตัวอย่างของข้อความแสดงข้อผิดพลาดของคอลัมน์ต้นทางที่ขาดหายไป](media/error_missing_field.png)

เมื่อต้องการแก้ไขปัญหานี้ อันดับแรกให้ทำตามขั้นตอนเหล่านี้เพื่อตรวจสอบให้แน่ใจว่าคอลัมน์อยู่ในตาราง

1. ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอปการเงินและการดำเนินงาน
2. ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** เลือกไทล์ **พารามิเตอร์กรอบงาน** และจากนั้น บนแท็บ **การตั้งค่าตาราง** เลือก **รีเฟรชรายการตาราง** เพื่อรีเฟรชตาราง
3. ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** เลือกแท็บ **ตารางข้อมูล** และตรวจสอบให้แน่ใจว่ามีการแสดงรายการตาราง ถ้าไม่มีการแสดงรายการตาราง ให้ลงชื่อเข้าใช้ใน VM สำหรับแอปการเงินและการดำเนินงานและตรวจสอบให้แน่ใจว่าตารางพร้อมใช้งาน
4. เปิดหน้า **การแมปตาราง** จากหน้า **การรวมแบบสองทิศทาง** ในแอปการเงินและการดำเนินงาน
5. เลือก **รีเฟรชรายการตาราง** เพื่อเติมข้อมูลคอลัมน์โดยอัตโนมัติในการแมปตาราง

ถ้ายังไม่มีการแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้

> [!IMPORTANT]
> ขั้นตอนเหล่านี้จะให้คำแนะนำเกี่ยวกับกระบวนการลบตาราง แล้วจากนั้น เพิ่มอีกครั้ง เมื่อต้องการหลีกเลี่ยงปัญหา ให้ตรวจสอบให้แน่ใจว่าได้ปฏิบัติตามขั้นตอนต่างๆ อย่างแม่นยำ

1. ในแอปการเงินและการดำเนินงาน ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **ตารางข้อมูล**
2. ค้นหาตารางที่ขาดแอตทริบิวต์ คลิก **ปรับเปลี่ยนการแมปเป้าหมาย** ในแถบเครื่องมือ
3. บนบานหน้าต่าง **แมปการแบ่งระยะไปยังเป้าหมาย** คลิก **สร้างการแมป**
4. เปิดหน้า **การแมปตาราง** จากหน้า **การรวมแบบสองทิศทาง** ในแอปการเงินและการดำเนินงาน
5. ถ้าแอตทริบิวต์ไม่ถูกเติมข้อมูลโดยอัตโนมัติบนแผนที่ ให้เพิ่มด้วยตนเองโดยการคลิกปุ่ม **เพิ่มแอตทริบิวต์** แล้วคลิก **บันทึก** 
6. เลือกแผนที่ และคลิก **เรียกใช้**


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
