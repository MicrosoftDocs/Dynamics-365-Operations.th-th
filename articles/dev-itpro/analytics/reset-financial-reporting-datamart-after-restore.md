---
title: "รีเซ็ต Data Mart การรายงานทางการเงิน"
description: "หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงิน"
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: th-th
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>รีเซ็ต Data Mart การรายงานทางการเงิน

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงินสำหรับรุ่นต่อไปนี้:

- Microsoft Dynamics 365 for Finance and Operations: Financial reporting รุ่น 7.2.6.0 และรุ่นที่ใหม่กว่า
- Microsoft Dynamics 365 for Finance and Operations: Financial reporting รุ่น 7.0.10000.4 และรุ่นที่ใหม่กว่า
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (แบบ On-premises)

เพื่อรับการรายงานทางการเงินของ Finance and Operations รุ่น 7.2.6.0 คุณสามารถดาวน์โหลด KB 4052514 ได้จาก <https://support.microsoft.com/en-us/help/4052514>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>รีเซ็ต Data Mart การรายงานทางการเงิน สำหรับการรายงานทางการเงินของ Finance and Operations รุ่น 7.2.6.0 และรุ่นที่ใหม่กว่า

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>รีเซ็ตData Mart การรายงานทางการเงินจากตัวออกแบบรายงาน

> [!NOTE]
> ขั้นตอนในกระบวนการนี้จะได้รับการสนับสนุนสำหรับการรายงานทางการเงินของ Finance and Operations รุ่น 7.2.6.0 และรุ่นที่ใหม่กว่า ถ้าคุณมีรุ่นก่อนหน้า ติดต่อทีมงานฝ่ายสนับสนุนเพื่อขอความช่วยเหลือ

ในสถานการณ์เฉพาะ คุณอาจต้องรีเซ็ต data mart สำหรับการรายงานทางการเงิน คุณสามารถทำงานนี้ให้สำเร็จได้ในไคลเอนต์ตัวออกแบบรายงาน นี่คือบางสถานการณ์ที่คุณอาจต้องรีเซ็ต data mart:

- มีการคืนค่าฐานข้อมูล Finance and Operations แต่ไม่ได้รับการคืนค่าฐานข้อมูล data mart
- คุณจะเห็นข้อมูลที่ไม่ถูกต้องสำหรับรอบระยะเวลา
- การสนับสนุนแนะนำให้คุณรีเซ็ต data mart เนื่องจากเป็นส่วนหนึ่งของขั้นตอนการแก้ไขปัญหาเบื้องต้น

การรีเซ็ต data mart ควรเสร็จสิ้นในระหว่างเวลาที่จำนวนของการประมวลผลในฐานข้อมูลมีขนาดเล็กเท่านั้น รายงานทางการเงินจะไม่พร้อมใช้งานในระหว่างกระบวนการตั้งค่าใหม่

#### <a name="reset-the-data-mart"></a>รีเซ็ต data mart

เพื่อรีเซ็ต data mart ในตัวออกแบบรายงาน บนเมนู **เครื่องมือ** เลือก **รีเซ็ต Data Mart** กล่องโต้ตอบที่ปรากฏมีสองส่วน: **สถิติ** และ **รีเซ็ต**

[![รีเซ็ตกล่องโต้ตอบ Data Mart](./media/Statistics.png)](./media/Statistics.png)

##### <a name="integration-attempts"></a>ความพยายามในการรวม

กริด **ความพยายามในการรวม** แสดงจำนวนครั้งที่ระบบได้พยายามที่จะรวมธุรกรรม ระบบพยายามที่จะรวมข้อมูลตลอดรอบระยะเวลาของวันต่อไป ถ้าความพยายามสองสามครั้งแรกไม่ประสบความสำเร็จ คุณจะทราบว่า data mart ต้องถูกรีเซ็ต ถ้าจำนวนครั้งของความพยายามคือ อย่างน้อย 8 ครั้ง และถ้ามีชุดมิติหรือเรกคอร์ดธุรกรรมจำนวนมาก ในสถานการณ์นี้ ข้อมูลจะไม่ถูกรายงาน

##### <a name="data-status"></a>สถานะของข้อมูล

กริด **สถานะของข้อมูล** จะแสดงสแนปช็อตของธุรกรรม อัตราแลกเปลี่ยน และค่ามิติใน data mart เรกคอร์ดที่ล้าสมัยจำนวนมากบ่งชี้ว่า มีการอัพเดตจำนวนมากไปยังเรกคอร์ดเกิดขึ้น สถานการณ์นี้อาจทำให้เวลาในการสร้างรายงานช้าลง

##### <a name="misaligned-main-account-categories"></a>ประเภทบัญชีหลักที่ไม่สอดคล้องกัน

ถ้าคุณกำลังใช้รุ่นที่เก่ากว่าการรายงานทางการเงินของ Microsoft Dynamics 365 for Finance and Operations รุ่น7.2.1 คุณอาจต้องรีเซ็ต data mart ถ้าคุณเปลี่ยนชื่อบัญชี และย้ายบัญชีระหว่างประเภทบัญชี การดำเนินการเหล่านี้อาจทำให้ประเภทบัญชีหลักกลายเป็นไม่สอดคล้องกัน ฟิลด์ **ประเภทบัญชีหลักที่ไม่สอดคล้องกัน** แสดงว่าคุณประสบกับปัญหานั้นหรือไม่

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>รีเซ็ต data mart ในการรายงานทางการเงินสำหรับ Finance and Operations รุ่น 7.2.6.0

เพื่อรีเซ็ต data mart ในการรายงานทางการเงินสำหรับ Finance and Operations รุ่น 7.2.6.0 และรุ่นก่อนหน้า ในกล่องโต้ตอบ **รีเซ็ต Data Mart** เลือกกล่องกาเครื่องหมาย **รีเซ็ต data mart** และจากนั้นเลือก **ตกลง** คุณควรรีเซ็ต data mart ในระหว่างการหยุดทำงานตามกำหนดการเท่านั้น

[![รีเซ็ตกล่องโต้ตอบ Data Mart](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>รีเซ็ต data mart และเลือกเหตุผลในการรายงานทางการเงินสำหรับ Microsoft Dynamics 365 for Finance and Operations รุ่น 7.3.0

ถ้าคุณกำหนดว่าการรีเซ็ต data mart จำเป็น ให้เลือกกล่องกาเครื่องหมาย **รีเซ็ต data mart** และจากนั้น เลือกเหตุผลในฟิลด์ **เหตุผล** โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้

- **ข้อมูลที่ขาดหายไปหรือไม่ถูกต้อง** – ขึ้นอยู่กับสถิติ คุณได้กำหนดว่าข้อมูลอาจหายไป ก่อนที่คุณดำเนินการต่อ เราขอแนะนำให้คุณทำงานกับฝ่ายสนับสนุนเพื่อกำหนดสาเหตุราก
- **คืนค่าฐานข้อมูล** – มีการคืนค่าฐานข้อมูล Finance and Operations แต่ไม่มีการคืนค่าฐานข้อมูล สำหรับ data mart ของการรายงานทางการเงิน
- **อื่น ๆ** – คุณกำลังรีเซ็ต data mart เพราะเหตุผลอื่น ถ้าคุณเป็นกังวลว่าจะมีปัญหา ติดต่อฝ่ายสนับสนุนเพื่อระบุปัญหา

> [!NOTE]
> ตรวจสอบว่างานที่มีอยู่ทั้งหมดเสร็จสิ้น ก่อนที่คุณดำเนินขั้นตอนต่างๆ จนเสร็จสิ้น คุณสามารถดูสถานะของการรวมได้ ด้วยการเลือก **เครื่องมือ** &gt; **สถานะการรวม**

#### <a name="clear-users-and-companies"></a>ล้างผู้ใช้และบริษัท

เลือกกล่องกาเครื่องหมาย **ล้างผู้ใช้และบริษัท** ถ้าคุณคืนค่าฐานข้อมูลของคุณ แต่จากนั้นคุณได้ทำการเปลี่ยนแปลงไปยังผู้ใช้หรือบริษัท คุณแทบจะไม่ต้องเลือกกล่องกาเครื่องหมายนี้เลย

เมื่อคุณพร้อมที่จะเริ่มต้นกระบวนการรีเซ็ต เลือก **ตกลง** คุณได้รับพร้อมท์ให้ยืนยันว่า คุณพร้อมที่จะเริ่มต้นกระบวนการ โปรดทราบว่า การรายงานทางการเงินจะไม่พร้อมใช้งานในระหว่างการรีเซ็ต และการรวมข้อมูลเริ่มต้นที่เกิดขึ้นในภายหลัง

ถ้าคุณต้องการตรวจสอบสถานะของการรวม เลือก **เครื่องมือ** &gt; **สถานะการรวม** เพื่อดูครั้งล่าสุดที่การรวมถูกเรียกใช้และสถานะ

[![ดูสถานะของการรวม](./media/Integration.png)](./media/Integration.png)

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>รีเซ็ต Data Mart ของการรายงานทางการเงินสำหรับการรายงานทางการเงินของ Finance and Operations รุ่น 7.0.10000.4 และรุ่นที่ใหม่กว่า

ถ้าคุณเคยคืนค่าฐานข้อมูล Finance and Operations ของคุณจากการสำรองข้อมูล หรือคัดลอกฐานข้อมูลจากสภาพแวดล้อมอื่น คุณต้องทำตามขั้นตอนในส่วนนี้ เพื่อช่วยรับรองว่า Data Mart การรายงานทางการเงินใช้ฐานข้อมูล Finance and Operations ที่คืนค่าได้อย่างถูกต้อง

> [!NOTE]
> ขั้นตอนในกระบวนการนี้ได้รับการสนับสนุนสำหรับแอพลิเคชัน Microsoft Dynamics รุ่น 7.0.1 (พฤษภาคม 2016) (การสร้างแอพลิเคชัน 7.0.1265.23014 และการสร้างการรายงานทางการเงิน 7.0.10000.4) และรุ่นที่ใหม่กว่า ถ้าคุณมี Finance and Operations รุ่นก่อนหน้า ให้ติดต่อทีมสนับสนุนของเราสำหรับความช่วยเหลือ

### <a name="export-report-definitions"></a>ส่งออกข้อกำหนดของรายงาน

ลำดับแรก ให้ทำตามขั้นตอนเหล่านี้เพื่อส่งออกแบบรายงานจากตัวออกแบบรายงาน

1. ในตัวออกแบบรายงาน เลือก **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**
2. เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และจากนั้นเลือก **ส่งออก**

    > [!NOTE]
    > สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**

3. เลือกข้อกำหนดของรายงานที่จะส่งออก:

    - หากต้องการส่งออกข้อกำหนดของรายงานและบล็อคส่วนประกอบที่เกี่ยวข้องทั้งหมดของคุณ เลือก **เลือกทั้งหมด**
    - เมื่อต้องการส่งออกรายงาน แถว คอลัมน์ แผนภูมิ หรือชุดมิติเฉพาะ เลือกแท็บที่เหมาะสม และจากนั้นเลือกรายการที่จะส่งออก กดปุ่ม Ctrl และค้างไว้ เพื่อเลือกหลายรายการบนแท็บ เมื่อคุณเลือกรายงานที่จะส่งออก แถว คอลัมน์ ลำดับ หรือชุดมิติที่เกี่ยวข้อง จะถูกเลือกด้วย

4. เลือก **ส่งออก**
5. ป้อนชื่อไฟล์ และเลือกตำแหน่งที่ปลอดภัยที่คุณต้องการบันทึกข้อกำหนดของรายงานที่ส่งออก
6. เลือก **บันทึก**

คุณสามารถคัดลอกหรืออัปโหลดไฟล์ไปยังตำแหน่งที่ปลอดภัยได้ ในวิธีนี้ ไฟล์สามารถถูกนำเข้าลงในสภาพแวดล้อมที่แตกต่างกันในภายหลังได้ สำหรับข้อมูลเกี่ยวกับวิธีใช้บัญชีการจัดเก็บ Microsoft Azure ดู [ถ่ายโอนข้อมูลโดยใช้ยูทิลิตี้บรรทัดคำสั่ง AzCopy](/azure/storage/storage-use-azcopy)

> [!NOTE]
> Microsoft ไม่ได้ให้บัญชีการจัดเก็บ เนื่องจากเป็นส่วนหนึ่งของข้อตกลงของ Finance and Operations คุณต้องซื้อบัญชีการจัดเก็บหรือใช้บัญชีการจัดเก็บจากการสมัครใช้งาน Azure ที่แยกต่างหาก

> [!WARNING]
> ระวังลักษณะการทำงานของไดรฟ์ D บนเครื่องเสมือนของ Azure (VMs) ห้ามจัดเก็บกลุ่มบล็อคส่วนประกอบที่ส่งออกของคุณอย่างถาวรบนไดรฟ์ D สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไดรฟ์ชั่วคราว ดู [การทำความเข้าใจไดรฟ์ชั่วคราวบน Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)

### <a name="stop-services"></a>หยุดการบริการ

บริการ Microsoft Windows ต่อไปนี้จะมีการเชื่อมต่อแบบเปิดกับฐานข้อมูล Finance and Operations ดังนั้น คุณต้องใช้ Microsoft Remote Desktop ในการเชื่อมต่อกับคอมพิวเตอร์ทั้งหมดในสภาพแวดล้อม และจากนั้นใช้ services.msc เพื่อหยุดการบริการเหล่านี้

- บริการเผยแพร่เวิลด์ไวด์เว็บ (บนคอมพิวเตอร์ Application Object Servers [AOS] ทั้งหมด)
- การจัดการชุดงานของ Microsoft Dynamics 365 for Finance and Operations (บนคอมพิวเตอร์ AOS ที่ไม่ใช่แบบส่วนตัวเท่านั้น)
- บริการประมวลผลของ Management Reporter 2012 (บนคอมพิวเตอร์ข่าวกรองธุรกิจ [BI] เท่านั้น)

### <a name="reset"></a>รีเซ็ต

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>ดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip ล่าสุด

ดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip ล่าสุด สำหรับคำแนะนำเกี่ยวกับวิธีการค้นหาและดาวน์โหลดรุ่นที่ถูกต้องของแพคเกจการอัพเกรดข้อมูล ดู[ดาวน์โหลดแพคเกจสามารถปรับใช้ได้ในการอัพเกรดข้อมูลล่าสุด](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages) ไม่จำเป็นต้องอัพเกรดเพื่อที่จะดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip ดังนั้น คุณเพิ่งได้ทำตามขั้นตอนในส่วน "ดาวน์โหลดแพคเกจสามารถปรับใช้ได้ในการอัพเกรดข้อมูลล่าสุด" ของหัวข้อดังกล่าว คุณสามารถข้ามขั้นตอนอื่นๆ ทั้งหมดในหัวข้อได้

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>เรียกใช้สคริปต์เทียบกับฐานข้อมูล Finance and Operations

เรียกใช้สคริปต์ต่อไปนี้เทียบกับฐานข้อมูล Finance and Operations (ไม่ใช่เทียบกับฐานข้อมูลการรายงานทางการเงิน)

- DataUpgrade.zip\\AosService\\สคริปต์\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\สคริปต์\\GrantAzViewChangeTracking.sql

สคริปต์เหล่านี้ช่วยรับรองว่าการตั้งค่าผู้ใช้ บทบาท และการติดตามการเปลี่ยนแปลง ถูกต้อง

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>เรียกใช้คำสั่ง Windows PowerShell เพื่อรีเซ็ตฐานข้อมูล

บนคอมพิวเตอร์ AOS เริ่มต้น Microsoft Windows PowerShell ให้เป็นผู้ดูแลระบบ และรันคำสั่งต่อไปนี้เพื่อรีเซ็ตการรวมระหว่าง Finance and Operations และการรายงานทางการเงิน:

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

นี่เป็นคำอธิบายเกี่ยวกับพารามิเตอร์ในคำสั่ง **รีเซ็ต DatamartIntegration** :

- ค่าที่ถูกต้องสำหรับ **-เหตุผล** คือ **SERVICING** **BADDATA** และ **OTHER**
- พารามิเตอร์  **-ReasonDetail** เป็นข้อความอิสระ
- เหตุผลและรายละเอียดเหตุผล จะถูกบันทึกในการตรวจสอบการตรวจวัดระยะไกล/สภาพแวดล้อม

> [!NOTE]
> หลังจากที่คุณรันคำสั่ง ระบบจะขอให้คุณป้อน **Y** เพื่อยืนยันว่า คุณต้องรีเซ็ตฐานข้อมูล

#### <a name="restart-services"></a>เริ่มการบริการอีกครั้ง

ใช้ services.msc เพื่อเริ่มการทำงานของบริการที่คุณหยุดการทำงานก่อนหน้านี้ใหม่:

- บริการเผยแพร่เวิลด์ไวด์เว็บ (บนคอมพิวเตอร์ AOS ทั้งหมด)
- การจัดการชุดงานของ Microsoft Dynamics 365 for Finance and Operations (บนคอมพิวเตอร์ AOS ที่ไม่ใช่แบบส่วนตัวเท่านั้น)
- บริการกระบวนการ Management Reporter 2012 (บนคอมพิวเตอร์ BI เท่านั้น)

#### <a name="import-report-definitions"></a>นำเข้าข้อกำหนดของรายงาน

นำเข้าการออกแบบรายงานของคุณจากตัวออกแบบรายงาน โดยใช้ไฟล์ที่ถูกสร้างขึ้นระหว่างการส่งออก:

1. ในตัวออกแบบรายงาน เลือก **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**
2. เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และจากนั้นเลือก **ส่งออก**

    > [!NOTE]
    > สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**

3. เลือกบล็อคส่วนประกอบ **เริ่มต้น** และจากนั้นเลือก **นำเข้า**
4. เลือกไฟล์ที่ประกอบด้วยข้อกำหนดของรายงานที่ส่งออก แล้วจากนั้นเลือก **เปิด**
5. ในกล่องโต้ตอบ **นำเข้า** เลือกข้อกำหนดของรายงานที่จะนำเข้า:

    - หากต้องการนำเข้าข้อกำหนดของรายงานและบล็อคส่วนประกอบที่เกี่ยวข้องทั้งหมด เลือก **เลือกทั้งหมด**
    - หากต้องการนำเข้ารายงาน แถว คอลัมน์ ลำดับ หรือชุดมิติที่เฉพาะเจาะจง เลือกรายงาน แถว คอลัมน์ ลำดับ หรือชุดมิติที่จะนำเข้า

6. เลือก **นำเข้า**

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>รีเซ็ต data mart การรายงานทางการเงินสำหรับ Finance and Operations (on-premises)

1. แนะนำให้ผู้ใช้ทั้งหมดออกจากตัวออกแบบรายงานและพื้นที่การรายงานทางการเงินของ Finance and Operations
2. รันสคริปต์ต่อไปนี้โดยเทียบกับฐานข้อมูลการรายงานทางการเงิน (MRDB)

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. ตัดให้สั้นลงหรือลบเรกคอร์ดทั้งหมดจากตาราง FINANCIALREPORTS ในฐานข้อมูล Finance and Operations (AXDB)
4. ตัดให้สั้นลงหรือลบเรกคอร์ดทั้งหมดจากตาราง FINANCIALREPORTVERSION ถ้ามีตารางนี้อยู่ในฐานข้อมูล Finance and Operations ถ้าไม่มีตารางนี้อยู่ในฐานข้อมูล Finance and Operations ให้ข้ามขั้นตอนนี้
5. รันสคริปต์ **ResetDatamart.sql** โดยเทียบกับฐานข้อมูลการรายงานทางการเงิน สคริปต์นี้ปิดใช้งานการรวม data mart ลบข้อมูล data mart ทั้งหมด และเปิดใช้งานการรวม data mart อีกครั้ง

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. หลังจากการรีเซ็ต คุณสามารถตรวจสอบการรีโหลดข้อมูลด้วยตนเองได้ โดยการรันการสอบถามต่อไปนี้เทียบกับฐานข้อมูลการรายงานทางการเงิน

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    ยืนยันว่า แถวทั้งหมดมีค่า **LastRunTime** และ **StateType** ถูกตั้งค่าเป็น **5** ค่า **StateType** เท่ากับ **5** บ่งชี้ว่า ข้อมูลถูกรีโหลดเสร็จเรียบร้อยแล้ว ค่าเท่ากับ **7** บ่งชี้สถานะที่มีข้อผิดพลาด บางครั้ง แผนผังลำดับชั้นขององค์กรมีสถานะนี้ในครั้งแรกที่รัน อย่างไรก็ตาม สถานะที่มีข้อบกพร่อง แต่ควรได้รับการแก้ไขโดยอัตโนมัติ

