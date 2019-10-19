---
title: ใช้บทช่วยสอน Regression Suite Automation Tool
description: หัวข้อนี้จะแสดงวิธีการใช้ Regression Suite Automation Tool (RSAT) ซึ่งจะอธิบายถึงคุณลักษณะต่างๆ และแสดงตัวอย่างที่ใช้การเขียนสคริปต์ขั้นสูง
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: cf3ca501efb4e540994b01e651eee5b8aab4ddbc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191097"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>ใช้บทช่วยสอน Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

> [!NOTE]
> ใช้เครื่องมือเบราว์เซอร์อินเทอร์เน็ตของคุณเพื่อดาวน์โหลดและบันทึกหน้านี้ในรูปแบบ pdf 

บทช่วยสอนนี้จะแนะนำคุณลักษณะขั้นสูงบางอย่างของ Regression Suite Automation Tool (RSAT) รวมถึงการกำหนดการสาธิต และอธิบายถึงกลยุทธ์และประเด็นการเรียนรู้ที่สำคัญ

## <a name="features-of-rsattask-recorder"></a>คุณลักษณะของ RSAT/ตัวบันทึกงาน

### <a name="validate-a-field-value"></a>ตรวจสอบความถูกต้องของค่าฟิลด์

สำหรับข้อมูลเกี่ยวกับคุณลักษณะนี้ ดู [สร้างการบันทึกงานใหม่ที่มีฟังก์ชันตรวจสอบความถูกต้อง](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function)

### <a name="saved-variable"></a>ตัวแปรที่บันทึกไว้

สำหรับข้อมูลเกี่ยวกับคุณลักษณะนี้ ดู [ปรับเปลี่ยนการบันทึกงานที่มีอยู่เพื่อสร้างตัวแปรที่บันทึกไว้](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable)

### <a name="derived-test-case"></a>กรณีการทดสอบที่สืบทอดมา

1. เปิด Regression Suite Automation Tool (RSAT) และเลือกกรณีการทดสอบทั้งสองกรณีที่คุณสร้างขึ้นใน [ตั้งค่าและติดตั้ง Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md)
2. เลือก **สร้าง \> สร้างกรณีการทดสอบที่สืบทอดมา**

    ![สร้างคำสั่งของกรณีทดสอบที่สืบทอดมาบนเมนูใหม่](./media/use_rsa_tool_01.png)

3. คุณได้รับข้อความที่แจ้งว่าจะมีการสร้างกรณีการทดสอบที่สืบทอดมาสำหรับกรณีการทดสอบที่เลือกแต่ละกรณีในชุดการทดสอบปัจจุบัน และกรณีการทดสอบที่สืบทอดมาแต่ละกรณีจะมีสำเนาของไฟล์พารามิเตอร์ Excel ของตนเอง เลือก **ตกลง**

    > [!NOTE]
    > เมื่อคุณรันกรณีการทดสอบที่สืบทอดมา จะใช้การบันทึกงานของกรณีการทดสอบหลักและสำเนาของไฟล์พารามิเตอร์ Excel ของตนเอง ด้วยวิธีนี้ คุณสามารถรันการทดสอบเดียวกันด้วยพารามิเตอร์ต่างๆ ได้ โดยไม่ต้องมีการรักษาการบันทึกงานมากกว่าหนึ่งรายการ กรณีการทดสอบที่สืบทอดมาไม่จำเป็นต้องเป็นส่วนหนึ่งของชุดการทดสอบเดียวกันกับกรณีการทดสอบหลัก

    ![กล่องข้อความ](./media/use_rsa_tool_02.png)

    มีการสร้างกรณีการทดสอบที่สืบทอดมาเพิ่มเติมสองกรณี และกล่องกาเครื่องหมาย **ได้รับมาหรือไม่?** จะถูกเลือกสำหรับกรณีเหล่านั้น

    ![มีการสร้างกรณีการทดสอบที่สืบทอดมา](./media/use_rsa_tool_03.png)

    มีการสร้างกรณีการทดสอบที่สืบทอดมาโดยอัตโนมัติใน Azure DevOps นี่เป็นรายการรองของกรณีการทดสอบ **สร้างผลิตภัณฑ์ใหม่** และมีการติดแท็กด้วยคำสำคัญพิเศษ: **RSAT: DerivedTestSteps** นอกจากนี้ กรณีการทดสอบเหล่านี้จะถูกเพิ่มเข้าไปในแผนการทดสอบโดยอัตโนมัติใน Azure DevOps

    ![คำสำคัญ RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > ถ้า เนื่องจากสาเหตุใดๆ กรณีการทดสอบที่สืบทอดมาที่ถูกสร้างนั้นไม่ได้อยู่ในลำดับที่ถูกต้อง ไปที่ Azure DevOps และจัดลำดับกรณีการทดสอบใหม่ในชุดการทดสอบ เพื่อให้ RSAT สามารถรันได้ในลำดับที่ถูกต้อง

4. เลือกกรณีการทดสอบที่สืบทอดมา แล้วจากนั้น เลือก **แก้ไข** เพื่อเปิดไฟล์พารามิเตอร์ Excel ที่สอดคล้องกัน
5. แก้ไขไฟล์พารามิเตอร์ของ Excel เหล่านี้ในลักษณะเดียวกับที่คุณแก้ไขไฟล์หลัก กล่าวอีกอย่างหนึ่งคือ ตรวจสอบให้แน่ใจว่ามีการตั้งค่ารหัสผลิตภัณฑ์ เพื่อให้มีการสร้างขึ้นโดยอัตโนมัติ นอกจากนี้ ตรวจสอบให้แน่ใจว่าตัวแปรที่บันทึกไว้ถูกคัดลอกไปยังฟิลด์ที่เกี่ยวข้อง
6. บนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel ให้ปรับปรุงค่าของฟิลด์ **บริษัท** เป็น **USSI** เพื่อให้กรณีการทดสอบที่สืบทอดมาจะถูกรันเทียบกับนิติบุคคลอื่นที่ไม่ใช่กรณีการทดสอบหลัก เมื่อต้องการรันกรณีการทดสอบเทียบกับผู้ใช้ที่ระบุ (หรือบทบาทที่สัมพันธ์กับผู้ใช้ที่ระบุ) คุณสามารถปรับปรุงค่าของฟิลด์ **ผู้ใช้การทดสอบ** ได้
7. เลือก **รัน** และตรวจสอบความถูกต้องว่าผลิตภัณฑ์ถูกสร้างขึ้นในทั้งนิติบุคคล USMF และนิติบุคคล USSI

### <a name="validate-notifications"></a>ตรวจสอบความถูกต้องของการแจ้งเตือน

สามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าเกิดการดำเนินการขึ้นหรือไม่ ตัวอย่างเช่น เมื่อใบสั่งผลิตถูกสร้าง ประมาณการ จนถึงเริ่มต้นการผลิต แอปจะแสดงข้อความ "การผลิต – เริ่มต้น" เพื่อแจ้งให้คุณทราบว่าใบสั่งผลิตเริ่มดำเนินการแล้ว

![การผลิต – เริ่มการแจ้งเตือน](./media/use_rsa_tool_05.png)

คุณสามารถตรวจสอบความถูกต้องของข้อความนี้ผ่าน RSAT โดยการป้อนข้อความในแท็บ **MessageValidation** ของไฟล์พารามิเตอร์ Excel สำหรับการบันทึกที่เหมาะสม

![แท็บการตรวจสอบความถูกต้องของข้อความ](./media/use_rsa_tool_06.png)

หลังจากรันกรณีการทดสอบ ข้อความในไฟล์พารามิเตอร์ของ Excel จะถูกเปรียบเทียบกับข้อความที่แสดง ถ้าข้อความไม่ตรงกัน กรณีการทดสอบจะล้มเหลว

> [!NOTE]
> คุณสามารถป้อนข้อความมากกว่าหนึ่งข้อความได้บนแท็บ **MessageValidation** ในไฟล์พารามิเตอร์ของ Excel นอกจากนี้ ข้อความอาจเป็นข้อผิดพลาดหรือข้อความเตือน แทนที่จะเป็นข้อความที่ให้ข้อมูล

### <a name="validate-values-by-using-operators"></a>ตรวจสอบความถูกต้องของค่าโดยใช้ตัวดำเนินการ

ในรุ่นก่อนหน้าของ RSAT คุณสามารถตรวจสอบความถูกต้องของค่าได้ เฉพาะเมื่อค่าการควบคุมเท่ากับค่าที่คาดไว้เท่านั้น คุณลักษณะใหม่ช่วยให้คุณสามารถตรวจสอบตัวแปรที่ไม่เท่ากับ น้อยกว่า หรือมากกว่า ค่าที่ระบุ

- เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าในองค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    ในไฟล์พารามิเตอร์ Excel ฟิลด์ **ผู้ปฏิบัติงาน** ใหม่ จะปรากฏขึ้น

    > [!NOTE]
    > ถ้าคุณได้ใช้เวอร์ชันที่เก่ากว่าของ RSAT คุณต้องสร้างไฟล์พารามิเตอร์ Excel ใหม่

    ![ฟิลด์ตัวดำเนินงาน](./media/use_rsa_tool_07.png)

ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าปริมาณคงคลังคงเหลือมากกว่า 0 (ศูนย์) หรือไม่

1. ในข้อมูลสาธิตในบริษัท **USMF** ให้สร้างการบันทึกงานที่มีขั้นตอนต่อไปนี้:

    1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**
    2. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด  ตัวอย่างเช่น ตัวกรองในค่าของ **1000** สำหรับฟิลด์ **หมายเลขสินค้า**
    3. เลือก **ปริมาณสินค้าคงคลังคงเหลือ**
    4. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด  ตัวอย่างเช่น ตัวกรองในค่าของ **1** สำหรับฟิลด์ **ไซต์**
    5. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    6. ตรวจสอบความถูกต้องว่าค่าของฟิลด์ **ทั้งหมดที่พร้อมใช้งาน** คือ **411.0000000000000000**

2. บันทึกการบันทึกงานไปยังไลบรารี BPM และซิงค์กับ Azure DevOps
3. เพิ่มกรณีการทดสอบไปยังแผนการทดสอบ และโหลดกรณีการทดสอบลงใน RSAT
4. เปิดไฟล์พารามิเตอร์ของ Excel บนแท็บ **InventOnhandItem** คุณจะเห็นส่วน **ตรวจสอบความถูกต้องของ InventOnhandItem** ที่มีฟิลด์ **ผู้ปฏิบัติงาน**

    ![ฟิลด์ตัวดำเนินงาน](./media/use_rsa_tool_08.png)

5. เมื่อต้องการตรวจสอบว่าปริมาณคงคลังคงเหลือจะมากกว่า 0 เสมอหรือไม่ ให้เปลี่ยนค่าของฟิลด์ **ค่า** จาก **411** เป็น **0** และค่าของฟิลด์ **ผู้ปฏิบัติงาน** จากเครื่องหมายเท่ากับ (**=**) เป็นเครื่องหมายมากกว่า (**\>**)

    ![ค่าของฟิลด์มูลค่าและผู้ปฏิบัติงานเปลี่ยนแปลง](./media/use_rsa_tool_09.png)

6. บันทึกและปิดไฟล์พารามิเตอร์ Excel
7. เลือก **อัปโหลด** เพื่อบันทึกการเปลี่ยนแปลงที่คุณทำไว้กับไฟล์พารามิเตอร์ Excel เป็น Azure DevOps

ขณะนี้ ถ้าค่าของฟิลด์ **ทั้งหมดพร้อมใช้งาน** สำหรับสินค้าที่ระบุในสินค้าคงคลังมีมากกว่า 0 (ศูนย์) การทดสอบจะผ่าน โดยไม่คำนึงถึงมูลค่าของปริมาณคงคลังคงเหลือจริง

### <a name="generator-logs"></a>ล็อกตัวสร้าง

คุณลักษณะนี้สร้างโฟลเดอร์ที่มีล็อกของกรณีการทดสอบที่มีการรัน

- เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าในองค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**

    ```
    <add key="LogGeneration" value="false" />
    ```

หลังจากที่มีการรันกรณีการทดสอบแล้ว คุณสามารถค้นหาไฟล์ล็อกภายใต้ **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**

![โฟลเดอร์ GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> ถ้ามีกรณีทดสอบที่มีอยู่ ก่อนที่คุณจะเปลี่ยนแปลงค่าในไฟล์ .config จะไม่มีการสร้างล็อกสำหรับกรณีการทดสอบดังกล่าวจนกว่าคุณจะสร้างไฟล์การดำเนินการทดสอบใหม่
> 
> ![คำสั่งสร้างไฟล์การดำเนินการข้อความเท่านั้น บนเมนูใหม่](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>สแนปช็อต

คุณลักษณะนี้จะจับภาพหน้าจอของขั้นตอนที่ดำเนินการในระหว่างการบันทึกงาน

- เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าขององค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

ภายใต้ **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** โฟลเดอร์ที่แยกต่างหากจะถูกสร้างขึ้นสำหรับกรณีการทดสอบแต่ละกรณีที่มีการรัน

![โฟลเดอร์สแนปช็อตสำหรับกรณีการทดสอบ](./media/use_rsa_tool_12.png)

ในโฟลเดอร์เหล่านี้แต่ละโฟลเดอร์ คุณสามารถค้นหาสแนปช็อตของขั้นตอนต่างๆ ที่ดำเนินการ ในขณะที่มีการรันกรณีการทดสอบ

![ไฟล์สแนปช็อต](./media/use_rsa_tool_13.png)

## <a name="assignment"></a>การกำหนด

### <a name="scenario"></a>สถานการณ์จำลอง

1. โปรแกรมออกแบบผลิตภัณฑ์จะสร้างผลิตภัณฑ์ที่นำออกใช้ใหม่
2. ผู้จัดการฝ่ายผลิตเริ่มต้นใบสั่งผลิตเพื่อนำระดับสินค้าคงคลังไปที่สองชิ้น
3. การผลิตจะเริ่มต้นและสิ้นสุดใบสั่งผลิต และตรวจสอบว่าปริมาณคงคลังคงเหลือคือสองชิ้น
4. ทีมงานขายได้รับใบสั่งสำหรับผลิตภัณฑ์ใหม่สี่ชิ้น ดังนั้น ทีมขายจึงปรับปรุงความต้องการสุทธิผ่านแผนแบบไดนามิก เนื่องจากไม่มีกำลังการผลิตเพิ่มเติม จะมีการตั้งค่านโยบายใบสั่งเริ่มต้นเป็น "ซื้อแทนที่จะทำ" ดังนั้น แผนการใบสั่งซื้อจะถูกสร้างขึ้น
5. ผู้ซื้อจะเพิ่มผู้จัดจำหน่าย ยืนยันแผนการใบสั่งซื้อ แล้วจากนั้น ยืนยันใบสั่งซื้อ
6. เมื่อสินค้าที่ซื้อมาถึงที่ร้านค้า ผู้ปฏิบัติงานร้านค้าจะค้นหาใบสั่งซื้อที่เกี่ยวข้อง และรับสินค้า เนื่องจากใบสั่งนี้เสร็จสมบูรณ์แล้วในขณะนี้ คุณสามารถเบิกสินค้าและบรรจุสินค้าตามใบสั่งขายได้
7. การเงินลงรายการบัญชีใบแจ้งหนี้การซื้อและใบแจ้งหนี้การขาย

ภาพประกอบต่อไปนี้แสดงโฟลว์สำหรับสถานการณ์นี้

![โฟลว์สำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_14.png)

ภาพประกอบต่อไปนี้แสดงกระบวนการทางธุรกิจสำหรับสถานการณ์จำลองนี้ใน RSAT

![กระบวนการทางธุรกิจสำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>กลยุทธ์ – การเรียนรู้ที่สำคัญ

### <a name="data"></a>ข้อมูล

- ตรวจสอบให้แน่ใจว่าคุณมีปริมาณข้อมูลของตัวแทน (สำเนาของข้อมูลการตั้งค่าคอนฟิกการผลิต/แบบ golden รวมถึงข้อมูลที่ถูกย้าย)
- เมื่อคุณสร้างข้อมูลใหม่ผ่านตัวบันทึกงาน ให้สร้างชื่อการทดสอบที่จะไม่ขัดแย้งกับชื่อที่มีอยู่ (ตัวอย่างเช่น ใช้คำนำหน้า เช่น **RSATxxx**)
- ใช้การคืนค่า Azure Point-In-Time เพื่อรันการทดสอบในสภาพแวดล้อมที่ไม่ใช่ระดับ 1 อีกครั้ง
- ถึงแม้ว่าคุณจะสามารถใช้ฟังก์ชัน Excel **RANDOM** และ **NOW** เพื่อสร้างชุดที่ไม่ซ้ำกันได้ แต่ความพยายามจะสูงอย่างมาก นี่คือตัวอย่าง

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>ตัวบันทึกงาน

- กำหนดสถานการณ์จำลอง ก่อนที่คุณจะเริ่มการบันทึก โครงการที่มีการจัดการอย่างดีมีสถานการณ์จำลองการทดสอบที่กำหนดไว้ล่วงหน้า เมื่อต้องการสร้างกรณีการทดสอบ ให้พิจารณาว่าผลลัพธ์ของสถานการณ์จำลองของการทดสอบดังกล่าวสามารถคาดการณ์ได้อย่างไร
- แบ่งการบันทึก ถ้ามีการดำเนินการโดยบทบาทต่างๆ หรือหากมีเวลารอ หรือเหตุการณ์ภายนอกก่อนขั้นตอนถัดไป
- หลีกเลี่ยงการเลือกค่าในรายการ แต่ใช้รูปแบบข้อความ เช่น **FIFO** **AudioRM** และ **SiteWH** แทน เมื่อคุณเลือกในรายการ จะมีการบันทึกตำแหน่งของค่าในรายการ ไม่ใช่ตัวค่าเอง ถ้ามีการเพิ่มสินค้าลงในรายการดังกล่าว ตำแหน่งของมูลค่าอาจเปลี่ยนแปลงได้ ดังนั้น การบันทึกของคุณจะใช้พารามิเตอร์ที่แตกต่างกัน และส่วนที่เหลือของสถานการณ์จำลองดังกล่าวอาจได้รับผลกระทบ
- ลองนึกถึงลักษณะการทำงานของผู้ใช้หลายราย ตัวอย่างเช่น อย่าสันนิษฐานว่าใบสั่งขายที่สร้างขึ้นใหม่ของคุณจะถูกเลือกโดยอัตโนมัติเสมอ แต่ใช้ตัวกรองเพื่อค้นหาใบสั่งที่ถูกต้องแทนเสมอ
- ใช้ฟังก์ชันคัดลอกในตัวบันทึกงานเพื่อบันทึกชื่อของผลิตภัณฑ์ที่สร้างขึ้นใหม่ เพื่อให้สามารถใช้งานได้ในกรณีการทดสอบที่เชื่อมโยง
- ใช้ฟังก์ชันตรวจสอบความถูกต้องในตัวบันทึกงาน เพื่อตั้งค่าจุดตรวจสอบว่ามีการรันขั้นตอนอย่างถูกต้อง

### <a name="rsat"></a>RSAT

- เมื่อต้องการรันการทดสอบในบริษัทอื่น คุณสามารถเปลี่ยนบริษัทบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel ตรวจสอบให้แน่ใจว่าการตั้งค่าและข้อมูลพร้อมใช้งานในบริษัทที่เลือกใหม่
- คุณสามารถเปลี่ยนผู้ใช้การทดสอบบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel ระบุรหัสอีเมลของผู้ใช้ที่จะรันกรณีการทดสอบ ในลักษณะนี้ อาจมีการรันกรณีการทดสอบโดยใช้สิทธิ์การรักษาความปลอดภัยของผู้ใช้ที่ระบุ
- เมื่อต้องการรอก่อนที่จะเริ่มต้นการทดสอบ คุณสามารถกำหนดการหยุดชั่วคราวบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel สามารถใช้การหยุดชั่วคราวนี้ในชุดงาน (ตัวอย่างเช่น ถ้าต้องรันลำดับงานก่อนที่จะสามารถดำเนินการขั้นตอนต่อไป)

## <a name="advanced-scripting"></a>การเขียนสคริปต์ขั้นสูง

### <a name="command-line"></a>รายการคำสั่ง

RSAT สามารถถูกเรียกจากหน้าต่าง **พร้อมต์คำสั่ง**

> [!NOTE]
> ตรวจสอบว่าตัวแปรของสภาพแวดล้อม **TestRoot** ถูกตั้งค่าเป็นพาธการติดตั้ง RSAT (ใน Microsoft Windows เปิด **แผงควบคุม** เลือก **ระบบและการรักษาความปลอดภัย \> ระบบ \> การตั้งค่าระบบขั้นสูง** และจากนั้น เลือก **ตัวแปรของสภาพแวดล้อม** )

1. เปิดหน้าต่าง **พร้อมต์คำสั่ง** เป็นผู้ดูแลระบบ
2. รันเครื่องมือจากไดเรกทอรีการติดตั้ง

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. แสดงรายการคำสั่งทั้งหมด

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>ตัวอย่างของ Windows PowerShell

#### <a name="run-a-test-case-in-a-loop"></a>รันกรณีการทดสอบในลูป

คุณมีสคริปต์การทดสอบที่สร้างลูกค้าใหม่ โดยการเขียนสคริปต์ อาจมีการรันกรณีการทดสอบนี้ในลูปโดยการสุ่มข้อมูลต่อไปนี้ ก่อนที่จะมีการรันการเกิดซ้ำแต่ละครั้ง:

- รหัสลูกค้า
- ชื่อลูกค้า
- ที่อยู่ลูกค้า

รหัสลูกค้าจะอยู่ในรูปแบบ *ATCUS\<หมายเลข\>* โดยที่ \<หมายเลข\> อยู่ระหว่าง **000000001** และ **999999999**

ตัวอย่างต่อไปนี้ใช้พารามิเตอร์ **เริ่มต้น** เพื่อกำหนดหมายเลขแรกที่จะใช้ ใช้พารามิเตอร์ที่สอง **nr** เพื่อกำหนดจำนวนของลูกค้าที่ต้องสร้างขึ้น สำหรับการเกิดซ้ำแต่ละครั้ง จะมีการเปลี่ยนแปลงพารามิเตอร์ในไฟล์พารามิเตอร์ Excel โดยใช้ฟังก์ชัน UpdateCustomer จากนั้น รายการคำสั่ง RSAT ถูกเรียกในฟังก์ชัน RunTestCase

เปิด Microsoft Windows PowerShell Integrated Scripting Environment (ISE) ในโหมดผู้ดูแลระบบ และวางรหัสต่อไปนี้ลงในหน้าต่างที่ชื่อ **Untitled1.ps1**

```
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>รันสคริปต์ที่ขึ้นอยู่กับข้อมูลใน Microsoft Dynamics 365

ตัวอย่างต่อไปนี้ใช้การเรียก Open Data Protocol (OData) ในการค้นหาสถานะใบสั่งของใบสั่งซื้อ ถ้าสถานะยังไม่ได้ **ออกใบแจ้งหนี้** คุณสามารถ ตัวอย่างเช่น เรียกใช้กรณีการทดสอบ RSAT ที่ลงรายการบัญชีใบแจ้งหนี้ได้

```
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
