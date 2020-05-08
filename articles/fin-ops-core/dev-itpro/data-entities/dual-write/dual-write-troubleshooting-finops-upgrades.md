---
title: แก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงแอป Finance and Operations
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการแก้ไขปัญหาซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงแอป Finance and Operations
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
ms.openlocfilehash: 53df00de82b101aa02160d865a9c3bbebcfcae15
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275475"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>แก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงแอป Finance and Operations

[!include [banner](../../includes/banner.md)]



หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงของแอป Finance and Operations

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="database-synchronization-errors"></a>ข้อผิดพลาดในการซิงโครไนส์ฐานข้อมูล

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้ เมื่อคุณพยายามใช้เอนทิตี้ **DualWriteProjectConfiguration** เพื่อปรับปรุงแอป Finance and Operations เป็น Platform update 30

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations
2. เปิด Visual Studio ในฐานะผู้ดูแลระบบ และเปิด Application Object Tree (AOT)
3. ค้นหา **DualWriteProjectConfiguration**
4. ใน AOT ให้คลิกขวาที่ **DualWriteProjectConfiguration** แล้วเลือก **เพิ่มไปยังโครงการใหม่** เลือก **ตกลง** เพื่อสร้างโครงการใหม่ที่ใช้ตัวเลือกเริ่มต้น
5. ใน Solution Explorer คลิกขวาที่ **คุณสมบัติโครงการ** และตั้งค่า **ซิงโครไนส์ฐานข้อมูลในการสร้าง** เป็น **จริง**
6. สร้างโครงการ และยืนยันว่าการสร้างเสร็จเรียบร้อยแล้ว
7. บนเมนู **Dynamics 365** เลือก **ซิงโครไนส์ฐานข้อมูล**
8. เลือก **ซิงโครไนส์** เพื่อทำการซิงโครไนส์ฐานข้อมูลแบบเต็ม
9. หลังจากการซิงโครไนส์ฐานข้อมูลทั้งหมดเสร็จเรียบร้อยแล้ว รันขั้นตอนการซิงโครไนส์ฐานข้อมูลอีกครั้งใน Microsoft Dynamics Lifecycle Services (LCS) และใช้สคริปต์การอัพเกรดด้วยตนเองตามความเหมาะสม เพื่อให้คุณสามารถดำเนินการปรับปรุงต่อไปได้

## <a name="missing-entity-fields-issue-on-maps"></a>ปัญหาฟิลด์เอนทิตี้ที่หายไปบนแผนที่

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

บนหน้า **การรวมแบบสองทิศทาง** คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:

*ฟิลด์แหล่งข้อมูลที่ขาดหายไป \<ชื่อฟิลด์\> ในเค้าร่าง*

![ตัวอย่างของข้อความแสดงข้อผิดพลาดของฟิลด์ต้นทางที่ขาดหายไป](media/error_missing_field.png)

เมื่อต้องการแก้ไขปัญหานี้ อันดับแรกให้ทำตามขั้นตอนเหล่านี้เพื่อตรวจสอบให้แน่ใจว่าฟิลด์อยู่ในเอนทิตี้

1. ลงชื่อเข้าใช้ใน VM สำหรับแอป Finance and Operations
2. ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** เลือกไทล์ **พารามิเตอร์กรอบงาน** และจากนั้น บนแท็บ **การตั้งค่าเอนทิตี้** เลือก **รีเฟรชรายการเอนทิตี้** เพื่อรีเฟรชเอนทิตี้
3. ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** เลือกแท็บ **เอนทิตี้ข้อมูล** และตรวจสอบให้แน่ใจว่ามีการแสดงรายการเอนทิตี้ ถ้าไม่มีการแสดงรายการเอนทิตี้ ให้ลงชื่อเข้าใช้ใน VM สำหรับแอป Finance and Operations และตรวจสอบให้แน่ใจว่าเอนทิตี้พร้อมใช้งาน
4. เปิดหน้า **การแม็ปเอนทิตี้** จากหน้า **การรวมแบบสองทิศทาง** ในแอป Finance and Operations
5. เลือก **รีเฟรชรายการเอนทิตี้** เพื่อเติมข้อมูลในฟิลด์โดยอัตโนมัติในการแม็ปเอนทิตี้

ถ้ายังไม่มีการแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้

> [!IMPORTANT]
> ขั้นตอนเหล่านี้จะให้คำแนะนำเกี่ยวกับกระบวนการลบเอนทิตี้ แล้วเพิ่มอีกครั้ง เมื่อต้องการหลีกเลี่ยงปัญหา ให้ตรวจสอบให้แน่ใจว่าได้ปฏิบัติตามขั้นตอนต่างๆ อย่างแม่นยำ

1. ในแอป Finance and Operations ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **เอนทิตี้ข้อมูล**
2. ค้นหาเอนทิตี้ที่ขาดแอททริบิวต์ คลิก **ปรับเปลี่ยนการแม็ปเป้าหมาย** ในแถบเครื่องมือ
3. บนบานหน้าต่าง **แม็ปการแบ่งระยะไปยังเป้าหมาย** คลิก **สร้างการแม็ป**
4. เปิดหน้า **การแม็ปเอนทิตี้** จากหน้า **การรวมแบบสองทิศทาง** ในแอป Finance and Operations
5. ถ้าแอททริบิวต์ไม่ถูกเติมข้อมูลโดยอัตโนมัติบนแผนที่ ให้เพิ่มด้วยตนเองโดยการคลิกปุ่ม **เพิ่มแอททริบิวต์** แล้วคลิก **บันทึก** 
6. เลือกแผนที่ และคลิก **รัน**
