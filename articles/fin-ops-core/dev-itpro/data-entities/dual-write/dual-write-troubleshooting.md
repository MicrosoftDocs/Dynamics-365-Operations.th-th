---
title: การแก้ไขปัญหาเบื้องต้นทั่วไป
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาเบื้องต้นทั่วไปสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service
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
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172702"
---
# <a name="general-troubleshooting"></a>การแก้ไขปัญหาเบื้องต้นทั่วไป

[!include [banner](../../includes/banner.md)]



หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาเบื้องต้นทั่วไปสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>เมื่อคุณพยายามติดตั้งแพคเกจการรวมแบบสองทิศทางโดยใช้เครื่องมือ Package Deployer ไม่มีโซลูชันที่พร้อมใช้งานแสดงขึ้น

เครื่องมือ Package Deployer บางรุ่นเข้ากันไม่ได้กับแพคเกจโซลูชันการรวมแบบสองทิศทาง เมื่อติดตั้งแพคเกจเสร็จเรียบร้อยแล้ว ให้ตรวจสอบให้แน่ใจว่าได้ใช้ [รุ่น 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) หรือรุ่นที่ใหม่กว่าของเครื่องมือ Package Deployer

หลังจากที่คุณติดตั้งเครื่องมือ Package Deployer แล้ว ให้ติดตั้งแพคเกจโซลูชันโดยทำตามขั้นตอนต่อไปนี้

1. ดาวน์โหลดไฟล์แพคเกจโซลูชันล่าสุดจาก Yammer.com หลังจากดาวน์โหลดไฟล์ zip ของแพคเกจแล้ว ให้คลิกขวา และเลือก **คุณสมบัติ** เลือกกล่องกาเครื่องหมาย **ยกเลิกการบล็อค** และจากนั้น เลือก **นำไปใช้** ถ้าคุณไม่เห็นกล่องกาเครื่องหมาย **ยกเลิกการบล็อค** ไฟล์ zip ถูกยกเลิกการบล็อคเรียบร้อยแล้ว และคุณสามารถข้ามขั้นตอนนี้ได้

    ![กล่องโต้ตอบคุณสมบัติ](media/unblock_option.png)

2. แยกไฟล์ zip ของแพคเกจ และคัดลอกไฟล์ทั้งหมดในโฟลเดอร์ **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**

    ![เนื้อหาของโฟลเดอร์ Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. วางไฟล์ที่คัดลอกทั้งหมดไปยังโฟลเดอร์ **เครื่องมือ** ของเครื่องมือ Package Deployer 
4. รัน **PackageDeployer.exe** เพื่อเลือกสภาพแวดล้อม Common Data Service และติดตั้งโซลูชัน

    ![เนื้อหาของโฟลเดอร์เครื่องมือ](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>เปิดใช้งานและดูล็อกการติดตามปลั๊กอินใน Common Data Service เพื่อดูรายละเอียดข้อผิดพลาด

**บทบาทที่จำเป็นในการเปิดล็อกการติดตามและดูข้อผิดพลาด:** ผู้ดูแลระบบ

หากต้องการเปิดล็อกการติดตาม ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้แอป Finance and Operations เปิดหน้า **การตั้งค่า** และจากนั้น ภายใต้ **ระบบ** ให้เลือก **การจัดการ**
2. บนหน้า **การจัดการ** เลือก **การตั้งค่าระบบ**
3. บนแท็บ **การกำหนดค่า** ในฟิลด์ **ปลั๊กอินและการสืบค้นกลับกิจกรรมลำดับงานที่กำหนดเอง** เลือก **ทั้งหมด** เพื่อเปิดใช้งานล็อกการติดตามปลั๊กอิน ถ้าคุณต้องการบันทึกล็อกการติดตามเฉพาะเมื่อมีข้อยกเว้นเกิดขึ้น คุณสามารถเลือก **ข้อยกเว้น** แทนได้


หากต้องการดูการติดตาม ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้แอป Finance and Operations เปิดหน้า **การตั้งค่า** และจากนั้น ภายใต้ **การกำหนดค่า** ให้เลือก **ล็อกการติดตามปลั๊กอิน**
2. ค้นหาล็อกการติดตามที่ซึ่งฟิลด์ **ชื่อชนิด** ถูกตั้งค่าเป็น **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**
3. ดับเบิลคลิกที่รายการเพื่อดูล็อกทั้งหมด และจากนั้น บน FastTab **การดำเนินการ** ให้ตรวจสอบข้อความ **บล็อคข้อความ**

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>เปิดใช้งานโหมดดีบักเมื่อต้องการแก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริงในแอป Finance and Operations

**บทบาทที่จำเป็นในการดูข้อผิดพลาด:** ผู้ดูแลระบบ

ข้อผิดพลาดในการรวมแบบสองทิศทางที่เกิดขึ้นใน Common Data Service สามารถปรากฏขึ้นได้ในแอป Finance and Operations ในบางกรณี ข้อความแบบเต็มของข้อความแสดงข้อผิดพลาดจะไม่พร้อมใช้งาน เนื่องจากข้อความยาวเกินไปหรือมีข้อมูลการระบุถึงตัวบุคคล (PII) คุณสามารถเปิดใช้งานการบันทึกก verbose สำหรับข้อผิดพลาดได้โดยปฏิบัติตามขั้นตอนเหล่านี้

1. การตั้งค่าคอนฟิกโครงการทั้งหมดในแอป Finance and Operations มีคุณสมบัติ **IsDebugMode** ในเอนทิตี้ **DualWriteProjectConfiguration** เปิดเอนทิตี้ **DualWriteProjectConfiguration** โดยใช้ add-in ของ Excel

    > [!TIP]
    > วิธีง่ายๆ ในการเปิดเอนทิตี้คือ การเปิดใช้งานโหมด **การออกแบบ** ใน add-in ของ Excel และจากนั้น เพิ่ม **DualWriteProjectConfigurationEntity** ไปยังแผ่นงาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปิดข้อมูลเอนทิตี้ใน Excel และปรับปรุงโดยใช้ add-in ของ Excel](../../office-integration/use-excel-add-in.md)

2. ตั้งค่าคุณสมบัติ **IsDebugMode** เป็น **ใช่** สำหรับโครงการ
3. รันสถานการณ์จำลองที่กำลังสร้างข้อผิดพลาด
4. ล็อก verbose พร้อมใช้งานในตาราง DualWriteErrorLog เมื่อต้องการค้นหาข้อมูลในเบราว์เซอร์ตาราง ให้ใช้ URL ต่อไปนี้ (แทนที่ **XXX** ตามความเหมาะสม):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>ตรวจสอบข้อผิดพลาดของการซิงโครไนส์บนเครื่องเสมือนสำหรับแอป Finance and Operations

**บทบาทที่จำเป็นในการดูข้อผิดพลาด:** ผู้ดูแลระบบ

1. ลงชื่อเข้าใช้ Microsoft Dynamics Lifecycle Services (LCS)
2. เปิดโครงการ LCS ที่คุณเลือกเพื่อทำการทดสอบการรวมแบบสองทิศทาง
3. เลือกไทล์ **สภาพแวดล้อมที่โฮสต์ระบบคลาวด์**
4. ใช้ Remote Desktop เพื่อลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations ใช้บัญชีเฉพาะที่ที่แสดงอยู่ใน LCS
5. เปิดตัวแสดงเหตุการณ์
6. เลือก **ล็อกของแอพลิเคชันและบริการ \> Microsoft \> Dynamics \> AX-DualWriteSync \> การดำเนินงาน**
7. ตรวจทานรายการของข้อผิดพลาดล่าสุด

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>ยกเลิกการเชื่อมโยงและเชื่อมโยงสภาพแวดล้อม Common Data Service อื่นจากแอป Finance and Operations

**ข้อมูลประจำตัวที่จำเป็นในการยกเลิกการเชื่อมโยงสภาพแวดล้อม:** ผู้ดูแลระบบผู้เช่า Azure AD

1. ลงชื่อเข้าใช้แอป Finance and Operations
2. ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **การรวมแบบสองทิศทาง**
3. เลือกการแม็ปที่กำลังรันทั้งหมด และจากนั้น เลือก **หยุด**
4. เลือก **ยกเลิกการเชื่อมโยงสภาพแวดล้อม**
5. เลือก **ใช่** เพื่อยืนยันการดำเนินงาน

ขณะนี้คุณสามารถเชื่อมโยงสภาพแวดล้อมใหม่
