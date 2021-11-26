---
title: บทช่วยสอน Regression Suite Automation Tool
description: หัวข้อนี้จะแสดงวิธีการใช้ Regression Suite Automation Tool (RSAT) ซึ่งจะอธิบายถึงคุณลักษณะต่างๆ และแสดงตัวอย่างที่ใช้การเขียนสคริปต์ขั้นสูง
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 2f31009424629221a8e4f130b0ec1879c6c6e3d4
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781974"
---
# <a name="regression-suite-automation-tool-tutorial"></a>บทช่วยสอน Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> ใช้เครื่องมือเบราว์เซอร์อินเทอร์เน็ตของคุณเพื่อดาวน์โหลดและบันทึกหน้านี้ในรูปแบบ pdf

บทช่วยสอนนี้จะแนะนำคุณลักษณะขั้นสูงบางอย่างของ Regression Suite Automation Tool (RSAT) รวมถึงการกำหนดการสาธิต และอธิบายถึงกลยุทธ์และประเด็นการเรียนรู้ที่สำคัญ

## <a name="notable-features-of-rsat-and-task-recorder"></a>ลักษณะการทำงานที่โดดเด่นของ RSAT และตัวบันทึกงาน

### <a name="validate-a-field-value"></a>ตรวจสอบความถูกต้องของค่าฟิลด์

RSAT ช่วยให้คุณสามารถรวมขั้นตอนการตรวจสอบความถูกต้องภายในกรณีการทดสอบของคุณ เพื่อตรวจสอบความถูกต้องของค่าที่คาดไว้ สำหรับข้อมูลเกี่ยวกับลักษณะการทำงานนี้ โปรดดูบทความ [ตรวจสอบความถูกต้องของค่าที่คาดไว้](rsat-validate-expected.md)

ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าปริมาณคงคลังคงเหลือมากกว่า 0 (ศูนย์) หรือไม่

1. ในข้อมูลสาธิตในบริษัท **USMF** ให้สร้างการบันทึกงานที่มีขั้นตอนต่อไปนี้:

    1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**
    2. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด  ตัวอย่างเช่น ตัวกรองในค่าของ **1000** สำหรับฟิลด์ **หมายเลขสินค้า**
    3. เลือก **ปริมาณสินค้าคงคลังคงเหลือ**
    4. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด  ตัวอย่างเช่น ตัวกรองในค่าของ **1** สำหรับฟิลด์ **ไซต์**
    5. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    6. ตรวจสอบความถูกต้องว่าค่าของฟิลด์ **ทั้งหมดที่พร้อมใช้งาน** คือ **411.0000000000000000**

2. บันทึกการบันทึกงานเป็น **การบันทึกของนักพัฒนา** และแนบไปกับกรณีการทดสอบของคุณใน Azure Devops
3. เพิ่มกรณีการทดสอบไปยังแผนการทดสอบ และโหลดกรณีการทดสอบลงใน RSAT
4. เปิดไฟล์พารามิเตอร์ Excel และไปที่แท็บ **TestCaseSteps**
5. เมื่อต้องการตรวจสอบความถูกต้องว่าปริมาณคงคลังคงเหลือจะมากกว่า **0** ให้ไปที่ขั้นตอน **ตรวจสอบความถูกต้องของผลรวมที่พร้อมใช้งาน** และเปลี่ยนค่าจาก **411** เป็น **0** เปลี่ยนค่าของฟิลด์ **พนักงานปฏิบัติการ** จากเครื่องหมายเท่ากับ (**=**) เป็นเครื่องหมายที่มากกว่า (**\>**)
6. บันทึกและปิดไฟล์พารามิเตอร์ Excel
7. เลือก **อัปโหลด** เพื่อบันทึกการเปลี่ยนแปลงที่คุณทำไว้กับไฟล์พารามิเตอร์ Excel เป็น Azure DevOps

ขณะนี้ ถ้าค่าของฟิลด์ **ทั้งหมดพร้อมใช้งาน** สำหรับสินค้าที่ระบุในสินค้าคงคลังมีมากกว่า 0 (ศูนย์) การทดสอบจะผ่าน โดยไม่คำนึงถึงมูลค่าของปริมาณคงคลังคงเหลือจริง

### <a name="saved-variables-and-chaining-of-test-cases"></a>ตัวแปรที่บันทึกไว้และการเชื่อมโยงของกรณีการทดสอบ

คุณลักษณะที่สำคัญอย่างหนึ่งของ RSAT คือการเชื่อมโยงของกรณีการทดสอบ นั่นคือ ความสามารถของการทดสอบเพื่อส่งผ่านตัวแปรไปยังการทดสอบอื่นๆ สำหรับข้อมูลเพิ่มเติม ให้ดูบทความ [คัดลอกตัวแปรไปยังกรณีทดสอบลำดับ](rsat-chain-test-cases.md)

### <a name="derived-test-case"></a>กรณีการทดสอบที่สืบทอดมา

RSAT ช่วยให้คุณสามารถใช้งานการบันทึกงานเดียวกันกับกรณีการทดสอบหลายตัว ซึ่งช่วยให้งานรันกับการตั้งค่าคอนฟิกข้อมูลต่างๆ ดูที่บทความ [กรณีการทดสอบที่ได้รับมา](rsat-derived-test-cases.md) สำหรับข้อมูลเพิ่ม

### <a name="validate-notifications-and-messages"></a>ตรวจสอบการแจ้งเตือนและข้อความ

สามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าเกิดการดำเนินการขึ้นหรือไม่ ตัวอย่างเช่น เมื่อใบสั่งผลิตถูกสร้าง ประมาณการ จนถึงเริ่มต้นการผลิต แอปจะแสดงข้อความ "การผลิต – เริ่มต้น" เพื่อแจ้งให้คุณทราบว่าใบสั่งผลิตเริ่มดำเนินการแล้ว

![การผลิต – เริ่มการแจ้งเตือน](./media/use_rsa_tool_05.png)

คุณสามารถตรวจสอบความถูกต้องของข้อความนี้ผ่าน RSAT โดยการป้อนข้อความในแท็บ **MessageValidation** ของไฟล์พารามิเตอร์ Excel สำหรับการบันทึกที่เหมาะสม

![แท็บการตรวจสอบความถูกต้องของข้อความ](./media/use_rsa_tool_06.png)

หลังจากรันกรณีการทดสอบ ข้อความในไฟล์พารามิเตอร์ของ Excel จะถูกเปรียบเทียบกับข้อความที่แสดง ถ้าข้อความไม่ตรงกัน กรณีการทดสอบจะล้มเหลว

> [!NOTE]
> คุณสามารถป้อนข้อความมากกว่าหนึ่งข้อความได้บนแท็บ **MessageValidation** ในไฟล์พารามิเตอร์ของ Excel นอกจากนี้ ข้อความอาจเป็นข้อผิดพลาดหรือข้อความเตือน แทนที่จะเป็นข้อความที่ให้ข้อมูล

### <a name="snapshot"></a>สแนปช็อต

คุณลักษณะนี้จะจับภาพหน้าจอของขั้นตอนที่ดำเนินการในระหว่างการบันทึกงาน มีประโยชน์สำหรับการตรวจสอบหรือการดีบักจุดประสงค์

- เมื่อต้องการใช้คุณลักษณะนี้ขณะเรียกใช้ RSAT กับอินเทอร์เฟซผู้ใช้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าในองค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- เมื่อต้องการใช้คุณลักษณะนี้ขณะเรียกใช้ RSAT โดย CLI (ตัวอย่างเช่น Azure DevOps) เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าในองค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

เมื่อคุณรันกรณีการทดสอบ RSAT สร้างสแนปช็อต (รูปภาพ) ของขั้นตอนและบันทึกในโฟลเดอร์การเล่นของกรณีการทดสอบในไดเรกทอรีการทำงาน ในโฟลเดอร์ชื่ออื่น โฟลเดอร์ย่อยที่แยกต่างหากจะถูกสร้างขึ้นชื่อว่า **StepSnapsdrives** โฟลเดอร์นั้นจะมีสแนปช็อตเกี่ยวกับกรณีการทดสอบที่รันอยู่

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

ภาพประกอบต่อไปนี้แสดงลำดับชั้นกระบวนการทางธุรกิจสำหรับสถานการณ์จำลองนี้ใน LCS Business Process Modeler

![กระบวนการทางธุรกิจสำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>กลยุทธ์ – การเรียนรู้ที่สำคัญ

### <a name="data"></a>ข้อมูล

- ตรวจสอบให้แน่ใจว่าคุณมีปริมาณข้อมูลของตัวแทน (สำเนาของข้อมูลการตั้งค่าคอนฟิกการผลิต/แบบ golden รวมถึงข้อมูลที่ถูกย้าย)
- เมื่อคุณสร้างข้อมูลใหม่ผ่านตัวบันทึกงาน ให้สร้างชื่อการทดสอบที่จะไม่ขัดแย้งกับชื่อที่มีอยู่ (ตัวอย่างเช่น ใช้คำนำหน้า เช่น **RSATxxx**)
- ใช้การคืนค่า Azure Point-In-Time เพื่อรันการทดสอบในสภาพแวดล้อมที่ไม่ใช่ระดับ 1 อีกครั้ง
- ถึงแม้ว่าคุณจะสามารถใช้ฟังก์ชัน Excel **RANDOM** และ **NOW** เพื่อสร้างชุดที่ไม่ซ้ำกันได้ แต่ความพยายามจะสูงอย่างมาก นี่คือตัวอย่าง

    ```Excel
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

### <a name="cli"></a>CLI

RSAT สามารถถูกเรียกจากหน้าต่าง **พร้อมต์คำสั่ง** หรือ **PowerShell**

> [!NOTE]
> ตรวจสอบว่าตัวแปรของสภาพแวดล้อม **TestRoot** ถูกตั้งค่าเป็นพาธการติดตั้ง RSAT (ใน Microsoft Windows เปิด **แผงควบคุม** เลือก **ระบบและการรักษาความปลอดภัย \> ระบบ \> การตั้งค่าระบบขั้นสูง** และจากนั้น เลือก **ตัวแปรของสภาพแวดล้อม** )

1. เปิดหน้าต่าง **พร้อมต์คำสั่ง** หรือ **PowerShell** เป็นผู้ดูแลระบบ
2. นำทางไปยังไดเรกทอรีการติดตั้ง RSAT

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. แสดงรายการคำสั่งทั้งหมด

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

แสดงวิธีใช้เกี่ยวกับคำสั่งที่มีอยู่ทั้งหมดและพารามิเตอร์

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: พารามิเตอร์ที่ไม่จำเป็นต้องระบุ

`command`: ที่ซึ่ง ``[command]`` เป็นหนึ่งในคำสั่งที่ระบุไว้ด้านล่าง

#### <a name="about"></a>เกี่ยวกับ

แสดงรุ่นปัจจุบัน

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

ล้างหน้าจอ

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>ดาวน์โหลด

ดาวน์โหลดเอกสารแนบสำหรับกรณีทดสอบที่ระบุไปยังไดเรกทอรีผลลัพธ์
คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>ดาวน์โหลด: พารามิเตอร์ที่ต้องใช้

+ `test_case_id`: แสดงรหัสกรณีทดสอบ
+ `output_dir`: แสดงถึงไดเรกทอรีผลลัพธ์ ต้องมีไดเรกทอรีอยู่

##### <a name="download-examples"></a>ดาวน์โหลด: ตัวอย่าง

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>แก้ไข

อนุญาตให้คุณเปิดไฟล์พารามิเตอร์ในโปรแกรม Excel และแก้ไขได้

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>แก้ไข: พารามิเตอร์ที่ต้องระบุ

+ `excel_file`: ต้องมีพาธเต็มไปยังไฟล์ Excel ที่มีอยู่

##### <a name="edit-examples"></a>แก้ไข: ตัวอย่าง

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>สร้าง

สร้างการดำเนินการทดสอบและไฟล์พารามิเตอร์สำหรับกรณีทดสอบที่ระบุในไดเรกทอรีผลลัพธ์ คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>สร้าง: พารามิเตอร์ที่ต้องใช้

+ `test_case_id`: แสดงรหัสกรณีทดสอบ
+ `output_dir`: แสดงถึงไดเรกทอรีผลลัพธ์ ต้องมีไดเรกทอรีอยู่

##### <a name="generate-examples"></a>สร้าง: ตัวอย่าง

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

สร้างกรณีการทดสอบใหม่ซึ่งสืบทอดมาจากกรณีการทดสอบที่ระบุ คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: พารามิเตอร์ที่ต้องใช้

+ `parent_test_case_id`: แสดงรหัสกรณีทดสอบหลัก
+ `test_plan_id`: แสดงรหัสแผนทดสอบ
+ `test_suite_id`: แสดงรหัสชุดทดสอบ

##### <a name="generatederived-examples"></a>generatederived: ตัวอย่าง

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

สร้างเฉพาะไฟล์การดำเนินการทดสอบและกรณีทดสอบที่ระบุในไดเรกทอรีผลลัพธ์ คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: พารามิเตอร์ที่ต้องใช้

+ `test_case_id`: แสดงรหัสกรณีทดสอบ
+ `output_dir`: แสดงถึงไดเรกทอรีผลลัพธ์ ต้องมีไดเรกทอรีอยู่

##### <a name="generatetestonly-examples"></a>generatetestonly: ตัวอย่าง

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

สร้างกรณีการทดสอบทั้งหมดสำหรับชุดที่ระบุในไดเรกทอรีผลลัพธ์ คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์เป็นพารามิเตอร์ **test_suite_name**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: พารามิเตอร์ที่ต้องใช้

+ `test_suite_name`: แสดงชื่อชุดทดสอบ
+ `output_dir`: แสดงถึงไดเรกทอรีผลลัพธ์ ต้องมีไดเรกทอรีอยู่

##### <a name="generatetestsuite-examples"></a>generatetestsuite: ตัวอย่าง

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>วิธีใช้

เหมือนกับ [?](#section) คำสั่ง

#### <a name="list"></a>รายการ

แสดงรายการกรณีที่มีการทดสอบทั้งหมดที่มีอยู่

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

แสดงรายการแผนการทดสอบทั้งหมดที่มีอยู่

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

แสดงรายการกรณีทดสอบสำหรับชุดการทดสอบที่ระบุ คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **suite_name**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: พารามิเตอร์ที่ต้องใช้

+ `suite_name`: ชื่อของชุดที่ต้องการ

##### <a name="listtestsuite-examples"></a>listtestesite: ตัวอย่าง

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

แสดงรายการชุดการทดสอบทั้งหมดที่มีอยู่

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>ย้อนกลับ

ย้อนกลับกรณีการทดสอบโดยใช้ไฟล์ Excel

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>ย้อนกลับ: พารามิเตอร์ที่ต้องใช้

+ `excel_file`: พาธแบบเต็มไปที่ไฟล์ Excel ต้องมีไฟล์อยู่

##### <a name="playback-examples"></a>ย้อนกลับ: ตัวอย่าง

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

ย้อนกลับกรณีการทดสอบหลายกรณีพร้อมกัน คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: พารามิเตอร์ที่ต้องใช้

+ `test_case_id1`: รหัสของกรณีทดสอบที่มีอยู่
+ `test_case_id2`: รหัสของกรณีทดสอบที่มีอยู่
+ `test_case_idN`: รหัสของกรณีทดสอบที่มีอยู่

##### <a name="playbackbyid-examples"></a>playbackbyid: ตัวอย่าง

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

ย้อนกลับกรณีทดสอบหลายกรณีพร้อมกันโดยใช้ไฟล์ Excel

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany: พารามิเตอร์ที่ต้องใช้

+ `excel_file1`: พาธแบบเต็มไปที่ไฟล์ Excel ต้องมีไฟล์อยู่
+ `excel_file2`: พาธแบบเต็มไปที่ไฟล์ Excel ต้องมีไฟล์อยู่
+ `excel_fileN`: พาธแบบเต็มไปที่ไฟล์ Excel ต้องมีไฟล์อยู่

##### <a name="playbackmany-examples"></a>playbackmany: ตัวอย่าง

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

ย้อนกลับกรณีทดสอบทั้งหมดจากชุดทดสอบที่ระบุ
คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **suite_name**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: พารามิเตอร์ที่ต้องใช้

+ `suite_name`: ชื่อของชุดที่ต้องการ

##### <a name="playbacksuite-examples"></a>playbacksuite: ตัวอย่าง

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>ออก

ปิดแอพลิเคชัน

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>อัพโหลด

อัพโหลดไฟล์ทั้งหมดที่เป็นของชุดทดสอบหรือกรณีการทดสอบที่ระบุ

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>อัปโหลด: พารามิเตอร์ที่ต้องใช้

+ `suite_name`: ไฟล์ทั้งหมดที่เป็นของชุดทดสอบที่ระบุจะถูกอัปโหลด
+ `testcase_id`: ไฟล์ทั้งหมดที่เป็นของกรณีทดสอบที่ระบุจะถูกอัปโหลด

##### <a name="upload-examples"></a>อัปโหลด: ตัวอย่าง

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

อัพโหลดเฉพาะไฟล์การบันทึกที่เป็นของกรณีการทดสอบที่ระบุ

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: พารามิเตอร์ที่ต้องใช้

+ `testcase_id`: ไฟล์การบันทึกที่เป็นของกรณีการทดสอบที่ระบุจะถูกอัปโหลด

##### <a name="uploadrecording-examples"></a>uploadrecording: ตัวอย่าง

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>การใช้

แสดงวิธีสองวิธีในการเรียกใช้แอพลิเคชันนี้: วิธีหนึ่งโดยใช้ไฟล์การตั้งค่าเริ่มต้น อีกวิธีหนึ่งให้ไฟล์การตั้งค่า

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>ตัวอย่างของ Windows PowerShell

#### <a name="run-a-test-case-in-a-loop"></a>รันกรณีการทดสอบในลูป

คุณมีสคริปต์การทดสอบที่สร้างลูกค้าใหม่ โดยการเขียนสคริปต์ อาจมีการรันกรณีการทดสอบนี้ในลูปโดยการสุ่มข้อมูลต่อไปนี้ ก่อนที่จะมีการรันการเกิดซ้ำแต่ละครั้ง:

- รหัสลูกค้า
- ชื่อลูกค้า
- ที่อยู่ลูกค้า

รหัสลูกค้าจะอยู่ในรูปแบบ *ATCUS\<number\>* โดยที่ \<number\> อยู่ระหว่าง **000000001** และ **999999999**

ตัวอย่างต่อไปนี้ใช้พารามิเตอร์ **เริ่มต้น** เพื่อกำหนดหมายเลขแรกที่จะใช้ ใช้พารามิเตอร์ที่สอง **nr** เพื่อกำหนดจำนวนของลูกค้าที่ต้องสร้างขึ้น สำหรับการเกิดซ้ำแต่ละครั้ง จะมีการเปลี่ยนแปลงพารามิเตอร์ในไฟล์พารามิเตอร์ Excel โดยใช้ฟังก์ชัน UpdateCustomer จากนั้น รายการคำสั่ง RSAT ถูกเรียกในฟังก์ชัน RunTestCase

เปิด Microsoft Windows PowerShell Integrated Scripting Environment (ISE) ในโหมดผู้ดูแลระบบ และวางรหัสต่อไปนี้ลงในหน้าต่างที่ชื่อ **Untitled1.ps1**

```powershell
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
$excelFilename = "full path to Excel parameter file"
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

```powershell
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
