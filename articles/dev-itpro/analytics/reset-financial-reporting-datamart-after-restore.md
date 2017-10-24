---
title: "รีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล"
description: "หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations"
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>รีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล

[!include[banner](../includes/banner.md)]


หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations

ถ้าคุณเคยคืนค่าฐานข้อมูล Finance and Operations ของคุณจากการสำรองข้อมูล หรือคัดลอกฐานข้อมูลจากสภาพแวดล้อมอื่น คุณต้องทำตามขั้นตอนในหัวข้อนี้เพื่อให้แน่ใจว่า Data Mart การรายงานทางการเงินใช้ฐานข้อมูล Finance and Operations ที่คืนค่าได้อย่างถูกต้อง 
> [!Note] 
> ขั้นตอนในกระบวนการนี้ได้รับการสนับสนุนสำหรับ Dynamics 365 for Operation การนำออกใช้ในเดือนพฤษภาคม 2016 (การสร้างแอพ 7.0.1265.23014 และการสร้างการรายงานทางการเงิน 7.0.10000.4) และการนำออกใช้ที่ใหม่กว่า ถ้าคุณมี Finance and Operations การนำออกใช้ก่อนหน้า ให้ติดต่อทีมสนับสนุนของเราสำหรับความช่วยเหลือ

## <a name="export-report-definitions"></a>ส่งออกข้อกำหนดของรายงาน
ก่อนอื่น ให้ส่งออกรูปแบบรายงานที่อยู่ในโปรแกรมออกแบบรายงาน โดยทำตามขั้นตอนต่อไปนี้:

1.  ในโปรแกรมออกแบบรายงาน ไปที่ **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**
2.  เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และคลิก **ส่งออก** 

    > [!Note] 
    > สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**
    
3.  เลือกข้อกำหนดของรายงานที่จะส่งออก:
    -   เมื่อต้องการส่งออกข้อกำหนดของรายงานและบล็อคส่วนประกอบที่เกี่ยวข้องทั้งหมดของคุณ คลิก **เลือกทั้งหมด**
    -   เมื่อต้องการส่งออกรายงาน แถว คอลัมน์ แผนภูมิ หรือเซ็ตมิติที่เฉพาะ คลิกแท็บที่เหมาะสม และจากนั้นเลือกรายการที่จะส่งออก กดค้างปุ่ม Ctrl เพื่อเลือกหลายรายการในแท็บ เมื่อคุณเลือกรายงานที่จะส่งออก แถว คอลัมน์ ลำดับ หรือชุดมิติที่เกี่ยวข้องจะถูกเลือกด้วย

4.  คลิก **ส่งออก**
5.  ป้อนที่ไฟล์และเลือกตำแหน่งที่ปลอดภัยที่คุณต้องการบันทึกข้อกำหนดของรายงานที่ส่งออก
6.  คลิก **บันทึก**

สามารถคัดลอกหรืออัปโหลดไฟล์ไปยังตำแหน่งที่ปลอดภัยได้โดยการยินยอมให้นำเข้าไปยังสภาพแวดล้อมอื่นในเวลาอื่น สามารถดูข้อมูลเกี่ยวกับการใช้บัญชีการจัดเก็บ Microsoft Azure ได้ใน [การถ่ายโอนข้อมูลโดยใช้ยูทิลิตี้บรรทัดคำสั่ง AzCopy](/azure/storage/storage-use-azcopy) 
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
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>ค้นหาและดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip ล่าสุด

ค้นหาแพคเกจ MinorVersionDataUpgrade.zip ล่าสุดโดยใช้คำแนะนำที่พบใน [ดาวน์โหลดล่าสุดข้อมูลการอัพเกรดสามารถปรับใช้ได้แพคเกจ](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages) คำแนะนำอธิบายถึงวิธีการค้นหาและดาวน์โหลดรุ่นที่ถูกต้องของแพคเกจการอัพเกรดข้อมูล ไม่จำเป็นต้องอัพเกรดเพื่อดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip คุณเพียงต้องทำตามขั้นตอนในส่วน "ดาวน์โหลดแพคเกจที่สามารถปรับใช้ได้ในการอัพเกรดข้อมูลล่าสุด" โดยไม่ต้องดำเนินขั้นตอนอื่น ๆ ในบทความเพื่อดึงข้อมูลสำเนาของแพคเกจ MinorVersionDataUpgrade.zip

### <a name="execute-scripts-against-finance-and-operations-database"></a>เรียกใช้สคริปต์กับฐานข้อมูล Finance and Operations

เรียกใช้สคริปต์ต่อไปนี้เทียบกับฐานข้อมูล Finance and Operations (ไม่ใช่เทียบกับฐานข้อมูลการรายงานทางการเงิน)

-   DataUpgrade.zip\\AosService\\สคริปต์\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\สคริปต์\\GrantAzViewChangeTracking.sql

สคริปต์เหล่านี้ทำให้แน่ใจว่าการตั้งค่าการติดตามการเปลี่ยนแปลง บทบาท และผู้ใช้ถูกต้อง

### <a name="execute-powershell-command-to-reset-database"></a>ดำเนินการคำสั่ง PowerShell เพื่อรีเซ็ตฐานข้อมูล

บนคอมพิวเตอร์ AOS ดำเนินการคำสั่งต่อไปนี้ใน PowerShell โดยเป็นผู้ดูแลระบบเพื่อรีเซ็ตการรวมระหว่าง Finance and Operations และการรายงานทางการเงิน:

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> หลังจากดำเนินการคำสั่ง คุณจะถูกขอให้ป้อน "Y" เพื่อยืนยัน

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





