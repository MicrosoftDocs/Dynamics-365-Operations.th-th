---
title: "รีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล"
description: "หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: c132c04bc64f02201252f03830d3f8309306f19c
ms.contentlocale: th-th
ms.lasthandoff: 06/13/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>รีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล

[!include[banner](../includes/banner.md)]


หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations 

มีหลายสถานการณ์จำลองที่คุณอาจจำเป็นต้องคืนค่าฐานข้อมูล Finance and Operations ของคุณจากสำเนาสำรองหรือคัดลอกฐานข้อมูลจากสภาพแวดล้อมอื่น เมื่อเกิดเหตุการณ์เช่นนี้ขึ้น คุณต้องทำตามขั้นตอนต่าง ๆ ที่เหมาะสมเพื่อให้แน่ใจว่า Data Mart การรายงานทางการเงินกำลังใช้ฐานข้อมูล Finance and Operations ที่คืนค่ามาได้อย่างถูกต้อง ถ้าคุณมีคำถามเกี่ยวกับการรีเซ็ต Data Mart การรายงานทางการเงินสำหรับเหตุผลนอกเหนือจากการคืนค่าฐานข้อมูล Finance and Operations ให้ดูที่ [การรีเซ็ต Data Mart โปรแกรมรายงานการจัดการ](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) สำหรับข้อมูลเพิ่มเติม หมายเหตุว่าขั้นตอนในกระบวนการนี้ได้รับการสนับสนุนสำหรับ Dynamics 365 for Operation การนำออกใช้ในเดือนพฤษภาคม 2016 (การสร้างแอพ 7.0.1265.23014 และการสร้างการรายงานทางการเงิน 7.0.10000.4) และการนำออกใช้ที่ใหม่กว่า ถ้าคุณมี Finance and Operations การนำออกใช้ก่อนหน้า โปรดติดต่อทีมสนับสนุนของเราสำหรับความช่วยเหลือ

## <a name="export-report-definitions"></a>ส่งออกข้อกำหนดของรายงาน
ก่อนอื่น ให้ส่งออกรูปแบบรายงานที่อยู่ในโปรแกรมออกแบบรายงาน โดยทำตามขั้นตอนต่อไปนี้:

1.  ในโปรแกรมออกแบบรายงาน ไปที่ **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**
2.  เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และคลิก **ส่งออก** **หมายเหตุ:** สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**
3.  เลือกข้อกำหนดของรายงานที่จะส่งออก:
    -   เมื่อต้องการส่งออกข้อกำหนดของรายงานและบล็อคส่วนประกอบที่เกี่ยวข้องทั้งหมดของคุณ คลิก **เลือกทั้งหมด**
    -   เมื่อต้องการส่งออกรายงาน แถว คอลัมน์ แผนภูมิ หรือเซ็ตมิติที่เฉพาะ คลิกแท็บที่เหมาะสม และจากนั้นเลือกรายการที่จะส่งออก กดค้างปุ่ม Ctrl เพื่อเลือกหลายรายการในแท็บ เมื่อคุณเลือกรายงานที่จะส่งออก แถว คอลัมน์ แผนภูมิ และเซ็ตมิติที่เกี่ยวข้องจะถูกเลือกไว้

4.  คลิก **ส่งออก**
5.  ป้อนที่ไฟล์และเลือกตำแหน่งที่ปลอดภัยที่คุณต้องการบันทึกข้อกำหนดของรายงานที่ส่งออก
6.  คลิก **บันทึก**

สามารถคัดลอกหรืออัปโหลดไฟล์ไปยังตำแหน่งที่ปลอดภัยได้โดยการยินยอมให้นำเข้าไปยังสภาพแวดล้อมอื่นในเวลาอื่น สามารถดูข้อมูลเกี่ยวกับการใช้บัญชีการจัดเก็บ Microsoft Azure ได้ใน [การถ่ายโอนข้อมูลโดยใช้ยูทิลิตี้บรรทัดคำสั่ง AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy) 
> [!NOTE]
> Microsoft ไม่ได้ให้บัญชีการจัดเก็บโดยเป็นส่วนหนึ่งของข้อตกลงของ Finance and Operations คุณต้องซื้อบัญชีการจัดเก็บหรือใช้บัญชีการจัดเก็บจากการสมัครใช้งาน Azure ที่แยกต่างหาก 
> [!WARNING]
> ระวังลักษณะการทำงานของไดรฟ์ D บนเครื่องเสมือนของ Azure อย่าเก็บกลุ่มบล็อคส่วนประกอบที่ส่งออกแล้วของคุณไว้ที่นี่อย่างถาวร สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไดรฟ์ชั่วคราว ให้ดูที่ [การทำความเข้าใจเกี่ยวกับไดรฟ์ชั่วคราวบนเครื่องเสมือนของ Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)

## <a name="stop-services"></a>หยุดการบริการ
ใช้เดสก์ท็อประยะไกลในการเชื่อมต่อกับคอมพิวเตอร์ทั้งหมดในสภาพแวดล้อมและหยุดการบริการ Windows ต่อไปนี้โดยใช้ services.msc:

-   บริการเผยแพร่เวิลด์ไวด์เว็บ (บนคอมพิวเตอร์ AOS ทั้งหมด)
-   การจัดการชุดงานของ Microsoft Dynamics 365 for Finance and Operations (บนคอมพิวเตอร์ AOS ที่ไม่ใช่แบบส่วนตัวเท่านั้น)
-   บริการกระบวนการ Management Reporter 2012 (บนคอมพิวเตอร์ BI เท่านั้น)

บริการเหล่านี้จะมีการเชื่อมต่อที่เปิดอยู่กับฐานข้อมูล Finance and Operations

## <a name="reset"></a>รีเซ็ต
#### <a name="locate-the-latest-dataupgradezip-package"></a>ค้นหาแพคเกจ DataUpgrade.zip ล่าสุด

ค้นหาแพคเกจ DataUpgrade.zip ล่าสุดโดยใช้คำแนะนำที่พบใน [ดาวน์โหลดสคริปต์ DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md) คำแนะนำอธิบายถึงวิธีการค้นหารุ่นที่ถูกต้องของแพคเกจการอัพเกรดข้อมูลสำหรับสภาพแวดล้อมของคุณ

#### <a name="execute-scripts-against-finance-and-operations-database"></a>เรียกใช้สคริปต์กับฐานข้อมูล Finance and Operations

เรียกใช้สคริปต์ต่อไปนี้เทียบกับฐานข้อมูล Finance and Operations (ไม่ใช่เทียบกับฐานข้อมูลการรายงานทางการเงิน)

-   DataUpgrade.zip\\AosService\\สคริปต์\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\สคริปต์\\GrantAzViewChangeTracking.sql

สคริปต์เหล่านี้ทำให้แน่ใจว่าการตั้งค่าการติดตามการเปลี่ยนแปลง บทบาท และผู้ใช้ถูกต้อง

#### <a name="execute-powershell-command-to-reset-database"></a>ดำเนินการคำสั่ง PowerShell เพื่อรีเซ็ตฐานข้อมูล

ดำเนินการคำสั่งต่อไปนี้โดยตรงบนคอมพิวเตอร์ AOS เพื่อรีเซ็ตการรวมระหว่าง Finance and Operations และการรายงานทางการเงิน:

1.  เปิด Windows PowerShell ในฐานะผู้ดูแลระบบ
2.  ดำเนินการ: F:
3.  ดำเนินการ: cd F:\\MRApplicationService\\MRInstallDirectory
4.  ดำเนินการ: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  ดำเนินการ: Reset-DatamartIntegration -Reason OTHER -ReasonDetail "&lt;เหตุผลของฉันสำหรับการตั้งค่าใหม่&gt;"
    -   คุณจะถูกขอให้ป้อน "Y" เพื่อยืนยัน

คำอธิบายของพารามิเตอร์:

-   ค่าที่ถูกต้องสำหรับเหตุผลคือ: SERVICING, BADDATA, OTHER
-   พารามิเตอร์ -ReasonDetail เป็นข้อความอิสระ
-   เหตุผลและ reasonDetail จะถูกบันทึกในการตรวจสอบ telemetry/environment

## <a name="start-services"></a>เริ่มการบริการ
ใช้ services.msc เพื่อเริ่มการทำงานของบริการที่คุณหยุดการทำงานก่อนหน้านี้ใหม่:

-   บริการเผยแพร่เวิลด์ไวด์เว็บ (บนคอมพิวเตอร์ AOS ทั้งหมด)
-   การจัดการชุดงานของ Microsoft Dynamics 365 for Finance and Operations (บนคอมพิวเตอร์ AOS ที่ไม่ใช่แบบส่วนตัวเท่านั้น)
-   บริการกระบวนการ Management Reporter 2012 (บนคอมพิวเตอร์ BI เท่านั้น)

## <a name="import-report-definitions"></a>นำเข้าข้อกำหนดของรายงาน
นำเข้าการออกแบบรายงานของคุณจากโปรแกรมออกแบบรายงานโดยใช้ไฟล์ที่สร้างขึ้นระหว่างการส่งออก:

1.  ในโปรแกรมออกแบบรายงาน ไปที่ **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**
2.  เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และคลิก **ส่งออก** 
    > [!NOTE]
    > สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**
3.  เลือกบล็อคส่วนประกอบ **เริ่มต้น** และคลิก **นำเข้า**
4.  เลือกไฟล์ที่ประกอบด้วยข้อกำหนดของรายงานที่ส่งออก แล้วคลิก **เปิด**
5.  ในกล่องโต้ตอบ นำเข้า เลือกข้อกำหนดของรายงานที่จะนำเข้า:
    -   เมื่อต้องการนำเข้าข้อกำหนดของรายงานและบล็อคส่วนประกอบสนับสนุนทั้งหมด คลิก **เลือกทั้งหมด**
    -   การนำเข้ารายงาน แถว คอลัมน์ แผนภูมิ หรือ เซ็ตมิติที่เฉพาะ ให้เลือกรายงาน แถว คอลัมน์ แผนภูมิ หรือเซ็ตมิติที่จะนำเข้า

6.  คลิก **นำเข้า**





