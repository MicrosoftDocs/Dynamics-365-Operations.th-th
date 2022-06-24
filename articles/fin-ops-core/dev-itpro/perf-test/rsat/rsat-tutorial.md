---
title: บทช่วยสอน Regression Suite Automation Tool
description: บทความนี้จะแสดงวิธีการใช้ Regression Suite Automation Tool (RSAT) ซึ่งจะอธิบายถึงคุณลักษณะต่างๆ และแสดงตัวอย่างที่ใช้การเขียนสคริปต์ขั้นสูง
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 04c7d7081ece4e077881092534ed061fe2d0e999
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854612"
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

2. บันทึกการบันทึกงานเป็น **การบันทึกของนักพัฒนา** และแนบไปกับกรณีทดสอบของคุณใน Azure DevOps
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

เมื่อคุณรันกรณีทดสอบ RSAT สร้างสแนปช็อต (รูปภาพ) ของขั้นตอนและบันทึกในโฟลเดอร์การเล่นของกรณีทดสอบในไดเรกทอรีการทำงาน ในโฟลเดอร์ชื่ออื่น โฟลเดอร์ย่อยที่แยกต่างหากจะถูกสร้างขึ้นชื่อว่า **StepSnapsdrives** โฟลเดอร์นั้นจะมีสแนปช็อตเกี่ยวกับกรณีการทดสอบที่รันอยู่

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

แสดงรายการคำสั่งทั้งหมดหรือแสดงวิธีใช้ของคำสั่งเฉพาะ พร้อมกับพารามิเตอร์ที่สามารถใช้งานได้

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: พารามิเตอร์ที่ไม่จำเป็นต้องระบุ

`command`: โดยที่ ``[command]`` เป็นหนึ่งในคำสั่งในรายการที่มาก่อนหน้า

#### <a name="about"></a>เกี่ยวกับ

แสดงรุ่นของ RSAT ที่ติดตั้ง

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

ล้างหน้าจอ

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>ดาวน์โหลด

ดาวน์โหลดสิ่งที่แนบ (ไฟล์การบันทึก ปฏิบัติการ และพารามิเตอร์) สำหรับกรณีทดสอบที่ระบุจาก Azure DevOps ไปยังไดเรกทอรีผลลัพธ์ คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีทดสอบที่สามารถใช้งานทั้งหมด และใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>ดาวน์โหลด: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการดาวน์โหลดจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค

##### <a name="download-required-parameters"></a>ดาวน์โหลด: พารามิเตอร์ที่ต้องใช้

+ `test_case_id`: แสดงรหัสกรณีทดสอบ

##### <a name="download-optional-parameters"></a>ดาวน์โหลด: พารามิเตอร์ที่เลือกได้

+ `output_dir`: แสดงถึงไดเรกทอรีการทำงานที่เป็นผลลัพธ์ ต้องมีไดเรกทอรีอยู่ ไดเรกทอรีการทำงานจากการตั้งค่าจะถูกใช้ถ้าไม่ได้ระบุพารามิเตอร์ไว้

##### <a name="download-examples"></a>ดาวน์โหลด: ตัวอย่าง

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

ดาวน์โหลดสิ่งที่แนบ (ไฟล์การบันทึก ปฏิบัติการ และพารามิเตอร์) สำหรับกรณีทดสอบทั้งหมดในชุดการทดสอบที่ระบุจาก Azure DevOps ไปยังไดเรกทอรีผลลัพธ์ คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบที่สามารถใช้งานทั้งหมด และใช้ค่าใดๆ เป็นพารามิเตอร์ **test_suite_name**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการดาวน์โหลดจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค
+ `/byid`: สวิตช์นี้แสดงว่าชุดการทดสอบที่ต้องการระบุโดยรหัส Azure DevOps แทนชื่อชุดการทดสอบ

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: พารามิเตอร์ที่ต้องใช้

+ `test_suite_name`: แสดงชื่อชุดทดสอบ ต้องใช้พารามิเตอร์นี้ถ้าสวิตช์ /byid **ไม่ได้** ระบุไว้ ชื่อนี้เป็นชื่อชุดการทดสอบ Azure DevOps
+ `test_suite_id`: แสดงรหัสชุดทดสอบ ต้องใช้พารามิเตอร์นี้ถ้าสวิตช์ /byid **ได้** ระบุไว้ รหัสนี้เป็นรหัส Azure DevOps ชุดการทดสอบ

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: พารามิเตอร์ที่เลือกได้

+ `output_dir`: แสดงถึงไดเรกทอรีการทำงานที่เป็นผลลัพธ์ ต้องมีไดเรกทอรีอยู่ ไดเรกทอรีการทำงานจากการตั้งค่าจะถูกใช้ถ้าไม่ได้ระบุพารามิเตอร์ไว้

##### <a name="downloadsuite-examples"></a>downloadsuite: ตัวอย่าง

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>แก้ไข

อนุญาตให้คุณเปิดไฟล์พารามิเตอร์ในโปรแกรม Excel และแก้ไขได้

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>แก้ไข: พารามิเตอร์ที่ต้องระบุ

+ `excel_file`: ต้องมีพาธเต็มไปยังไฟล์ Excel ที่มีอยู่

##### <a name="edit-examples"></a>แก้ไข: ตัวอย่าง

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>สร้าง

สร้างการดำเนินการทดสอบและไฟล์พารามิเตอร์สำหรับกรณีทดสอบที่ระบุในไดเรกทอรีผลลัพธ์ คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่ ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการสร้างจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค
+ `/dllonly`: สร้างไฟล์ปฏิบัติการทดสอบเท่านั้น ไม่จำเป็นต้องสร้างไฟล์พารามิเตอร์ Excel ใหม่อีกครั้ง
+ `/keepcustomexcel`: อัปเกรดไฟล์พารามิเตอร์ที่มีอยู่ และสร้างไฟล์ปฏิบัติการใหม่ด้วย

##### <a name="generate-required-parameters"></a>สร้าง: พารามิเตอร์ที่ต้องใช้

+ `test_case_id`: แสดงรหัสกรณีทดสอบ

##### <a name="generate-optional-parameters"></a>สร้าง: พารามิเตอร์ที่เลือกได้

+ `output_dir`: แสดงถึงไดเรกทอรีการทำงานที่เป็นผลลัพธ์ ต้องมีไดเรกทอรีอยู่ ไดเรกทอรีการทำงานจากการตั้งค่าจะถูกใช้ถ้าไม่ได้ระบุพารามิเตอร์ไว้

##### <a name="generate-examples"></a>สร้าง: ตัวอย่าง

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

สร้างกรณีทดสอบใหม่ (กรณีทดสอบย่อย) ของกรณีทดสอบที่ระบุ กรณีทดสอบใหม่จะถูกเพิ่มเข้าไปในชุดการทดสอบที่ระบุด้วย คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีทดสอบที่สามารถใช้งานทั้งหมด และใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการสร้างจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค

##### <a name="generatederived-required-parameters"></a>generatederived: พารามิเตอร์ที่ต้องใช้

+ `parent_test_case_id`: แสดงรหัสกรณีทดสอบหลัก
+ `test_plan_id`: แสดงรหัสแผนทดสอบ
+ `test_suite_id`: แสดงรหัสชุดทดสอบ

##### <a name="generatederived-examples"></a>generatederived: ตัวอย่าง

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

สร้างเฉพาะไฟล์ปฏิบัติการทดสอบสำหรับกรณีทดสอบที่ระบุ ไม่ได้สร้างไฟล์พารามิเตอร์ Excel ไฟล์ถูกสร้างในไดเรกทอรีผลลัพธ์ที่ระบุ คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีทดสอบที่สามารถใช้งานทั้งหมด และใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการสร้างจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: พารามิเตอร์ที่ต้องใช้

+ `test_case_id`: แสดงรหัสกรณีทดสอบ

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: สวิตช์ที่เลือกได้

+ `output_dir`: แสดงถึงไดเรกทอรีการทำงานที่เป็นผลลัพธ์ ต้องมีไดเรกทอรีอยู่ ไดเรกทอรีการทำงานจากการตั้งค่าจะถูกใช้ถ้าไม่ได้ระบุพารามิเตอร์ไว้

##### <a name="generatetestonly-examples"></a>generatetestonly: ตัวอย่าง

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

สร้างไฟล์ระบบอัตโนมัติทดสอบสำหรับกรณีทดสอบทั้งหมดในชุดการทดสอบที่ระบุ คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบที่สามารถใช้งานทั้งหมด และใช้ค่าใดๆ เป็นพารามิเตอร์ **test_suite_name**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการสร้างจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค
+ `/dllonly`: สร้างไฟล์ปฏิบัติการทดสอบเท่านั้น ไม่จำเป็นต้องสร้างไฟล์พารามิเตอร์ Excel ใหม่อีกครั้ง
+ `/keepcustomexcel`: อัปเกรดไฟล์พารามิเตอร์ที่มีอยู่ และสร้างไฟล์ปฏิบัติการใหม่ด้วย
+ `/byid`: สวิตช์นี้แสดงว่าชุดการทดสอบที่ต้องการระบุโดยรหัส Azure DevOps แทนชื่อชุดการทดสอบ

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: พารามิเตอร์ที่ต้องใช้

+ `test_suite_name`: แสดงชื่อชุดทดสอบ ต้องใช้พารามิเตอร์นี้ถ้าสวิตช์ /byid **ไม่ได้** ระบุไว้ ชื่อนี้เป็นชื่อชุดการทดสอบ Azure DevOps
+ `test_suite_id`: แสดงรหัสชุดทดสอบ ต้องใช้พารามิเตอร์นี้ถ้าสวิตช์ /byid **ได้** ระบุไว้ รหัสนี้เป็นรหัส Azure DevOps ชุดการทดสอบ

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: สวิตช์ที่เลือกได้

+ `output_dir`: แสดงถึงไดเรกทอรีการทำงานที่เป็นผลลัพธ์ ต้องมีไดเรกทอรีอยู่ ไดเรกทอรีการทำงานจากการตั้งค่าจะถูกใช้ถ้าไม่ได้ระบุพารามิเตอร์ไว้

##### <a name="generatetestsuite-examples"></a>generatetestsuite: ตัวอย่าง

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>วิธีใช้

เหมือนกับ [?](#section) คำสั่ง

#### <a name="list"></a>รายการ

แสดงรายการกรณีทดสอบที่สามารถใช้งานทั้งหมดในแผนทดสอบปัจจุบัน

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

แสดงรายการแผนการทดสอบทั้งหมดที่มีอยู่

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

แสดงรายการกรณีทดสอบสำหรับชุดการทดสอบที่ระบุ คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบที่พร้อมใช้งานทั้งหมด และใช้ค่าใดๆ จากรายการเป็นพารามิเตอร์ **suite_name**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: พารามิเตอร์ที่ต้องใช้

+ `test_suite_name`: ชื่อของชุดที่ต้องการ

##### <a name="listtestsuite-examples"></a>listtestesite: ตัวอย่าง

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

แสดงรายการกรณีทดสอบสำหรับชุดการทดสอบที่ระบุ

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: พารามิเตอร์ที่ต้องใช้

+ `test_suite_id`: รหัสของชุดที่ต้องการ

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: ตัวอย่าง

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

แสดงรายการชุดการทดสอบที่สามารถใช้งานทั้งหมดในแผนทดสอบปัจจุบัน

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>ย้อนกลับ

ย้อนกลับกรณีทดสอบที่เชื่อมโยงกับไฟล์พารามิเตอร์ Excel ที่ระบุ คำสั่งนี้ใช้ไฟล์ระบบอัตโนมัติเฉพาะที่ที่มีอยู่และไม่ได้ดาวน์โหลดไฟล์จาก Azure DevOps คำสั่งนี้ไม่รองรับกรณีทดสอบ POS Commerce

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการเล่นจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค
+ `/comments[="comment"]`: ระบุสตริงข้อมูลที่กำหนดเองซึ่งจะรวมอยู่ในฟิลด์ **ข้อคิดเห็น** หน้าสรุปและผลการทดสอบสำหรับการเรียกใช้กรณีทดสอบ Azure DevOps

##### <a name="playback-required-parameters"></a>ย้อนกลับ: พารามิเตอร์ที่ต้องใช้

+ `excel_parameter_file`: พาธเต็มของไฟล์พารามิเตอร์ Excel ต้องมีไฟล์อยู่

##### <a name="playback-examples"></a>ย้อนกลับ: ตัวอย่าง

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

ย้อนกลับกรณีทดสอบหลายกรณีพร้อมกัน กรณีทดสอบจะระบุโดยรหัสของกรณีทดสอบ คำสั่งนี้จะดาวน์โหลดไฟล์จาก Azure DevOps คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีทดสอบที่สามารถใช้งานทั้งหมด และใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการเล่นจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค
+ `/comments[="comment"]`: ระบุสตริงข้อมูลที่กำหนดเองซึ่งจะรวมอยู่ในฟิลด์ **ข้อคิดเห็น** หน้าสรุปและผลการทดสอบสำหรับการเรียกใช้กรณีทดสอบ Azure DevOps

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: พารามิเตอร์ที่ต้องใช้

+ `test_case_id1`: รหัสของกรณีทดสอบที่มีอยู่
+ `test_case_id2`: รหัสของกรณีทดสอบที่มีอยู่
+ `test_case_idN`: รหัสของกรณีทดสอบที่มีอยู่

##### <a name="playbackbyid-examples"></a>playbackbyid: ตัวอย่าง

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

ย้อนกลับกรณีทดสอบหลายกรณีพร้อมกัน กรณีทดสอบจะระบุโดยไฟล์พารามิเตอร์ Excel คำสั่งนี้ใช้ไฟล์ระบบอัตโนมัติเฉพาะที่ที่มีอยู่และไม่ได้ดาวน์โหลดไฟล์จาก Azure DevOps

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการเล่นจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค
+ `/comments[="comment"]`: ระบุสตริงข้อมูลที่กำหนดเองซึ่งจะรวมอยู่ในฟิลด์ **ข้อคิดเห็น** หน้าสรุปและผลการทดสอบสำหรับการเรียกใช้กรณีทดสอบ Azure DevOps

##### <a name="playbackmany-required-parameters"></a>playbackmany: พารามิเตอร์ที่ต้องใช้

+ `excel_parameter_file1`: พาธเต็มของไฟล์พารามิเตอร์ Excel ต้องมีไฟล์อยู่
+ `excel_parameter_file2`: พาธเต็มของไฟล์พารามิเตอร์ Excel ต้องมีไฟล์อยู่
+ `excel_parameter_fileN`: พาธเต็มของไฟล์พารามิเตอร์ Excel ต้องมีไฟล์อยู่

##### <a name="playbackmany-examples"></a>playbackmany: ตัวอย่าง

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

ย้อนกลับกรณีทดสอบทั้งหมดจากชุดการทดสอบที่ระบุอย่างน้อยหนึ่งชุด ถ้ามีการระบุสวิตช์ /local จะมีการใช้สิ่งที่แนบเฉพาะที่กับการย้อนกลับ มิฉะนั้นสิ่งที่แนบจะถูกดาวน์โหลดจาก Azure DevOps คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบที่สามารถใช้งานทั้งหมด และใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **suite_name**

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: สวิตช์ที่เลือกได้

+ `/updatedriver`: ถ้ามีการระบุสวิตช์นี้ โปรแกรม WebDriver ของอินเทอร์เน็ตเบราว์เซอร์จะอัปเดตตามความจำเป็นก่อนที่จะเรียกใช้กระบวนการเล่น
+ `/local`: สวิตช์นี้แสดงว่าควรใช้สิ่งที่แนบเฉพาะที่สำหรับการเล่นแทนการดาวน์โหลดไฟล์จาก Azure DevOps
+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการเล่นจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค
+ `/comments[="comment"]`: ระบุสตริงข้อมูลที่กำหนดเองซึ่งจะรวมอยู่ในฟิลด์ **ข้อคิดเห็น** หน้าสรุปและผลการทดสอบสำหรับการเรียกใช้กรณีทดสอบ Azure DevOps
+ `/byid`: สวิตช์นี้แสดงว่าชุดการทดสอบที่ต้องการระบุโดยรหัส Azure DevOps แทนชื่อชุดการทดสอบ

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: พารามิเตอร์ที่ต้องใช้

+ `test_suite_name1`: แสดงชื่อชุดทดสอบ ต้องใช้พารามิเตอร์นี้ถ้าสวิตช์ /byid **ไม่ได้** ระบุไว้ ชื่อนี้เป็นชื่อชุดการทดสอบ Azure DevOps
+ `test_suite_nameN`: แสดงชื่อชุดทดสอบ ต้องใช้พารามิเตอร์นี้ถ้าสวิตช์ /byid **ไม่ได้** ระบุไว้ ชื่อนี้เป็นชื่อชุดการทดสอบ Azure DevOps
+ `test_suite_id1`: แสดงรหัสชุดทดสอบ ต้องใช้พารามิเตอร์นี้ถ้าสวิตช์ /byid **ได้** ระบุไว้ รหัสนี้เป็นรหัส Azure DevOps ชุดการทดสอบ
+ `test_suite_idN`: แสดงรหัสชุดทดสอบ ต้องใช้พารามิเตอร์นี้ถ้าสวิตช์ /byid **ได้** ระบุไว้ รหัสนี้เป็นรหัส Azure DevOps ชุดการทดสอบ

##### <a name="playbacksuite-examples"></a>playbacksuite: ตัวอย่าง

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

เรียกใช้กรณีทดสอบทั้งหมดในชุดการทดสอบ Azure DevOps ที่ระบุ

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: สวิตช์ที่เลือกได้

+ `/retry[=seconds]`: ถ้ามีการระบุสวิตช์นี้ และกรณีทดสอบถูกบล็อคโดยอินสแตนซ์ RSAT อื่นๆ กระบวนการเล่นจะรอตามจํานวนวินาทีที่ระบุแล้วลองอีกครั้ง ค่าเริ่มต้นสำหรับ \[วินาที\] คือ 120 วินาที ถ้าไม่มีสวิตช์นี้ กระบวนการจะถูกยกเลิกทันทีถ้ากรณีทดสอบถูกบล็อค
+ `/comments[="comment"]`: ระบุสตริงข้อมูลที่กำหนดเองซึ่งจะรวมอยู่ในฟิลด์ **ข้อคิดเห็น** หน้าสรุปและผลการทดสอบสำหรับการเรียกใช้กรณีทดสอบ Azure DevOps
+ `/byid`: สวิตช์นี้แสดงว่าชุดการทดสอบที่ต้องการระบุโดยรหัส Azure DevOps แทนชื่อชุดการทดสอบ

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: พารามิเตอร์ที่ต้องใช้

+ `test_suite_id`: แสดงรหัสชุดการทดสอบตามที่มีอยู่ใน Azure DevOps

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: ตัวอย่าง

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>ออก

ปิดแอปพลิเคชัน คำสั่งนี้มีประโยชน์เฉพาะเมื่อแอปพลิเคชันทำงานในโหมดเชิงโต้ตอบเท่านั้น

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: ตัวอย่าง

`quit`

#### <a name="upload"></a>อัพโหลด

อัปโหลดไฟล์สิ่งที่แนบ (ไฟล์การบันทึก การปฏิบัติการ และพารามิเตอร์) ที่เป็นของชุดการทดสอบหรือกรณีทดสอบที่ระบุไปยัง Azure DevOps

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>อัปโหลด: พารามิเตอร์ที่ต้องใช้

+ `test_suite_name`: ไฟล์ทั้งหมดที่เป็นของชุดการทดสอบที่ระบุจะถูกอัปโหลด
+ `test_case_id1`: แสดงรหัสกรณีทดสอบแรกที่ควรอัปโหลด ใช้พารามิเตอร์นี้เฉพาะเมื่อไม่ได้ระบุชื่อชุดการทดสอบไว้เท่านั้น
+ `test_case_idN`: แสดงรหัสกรณีทดสอบสุดท้ายที่ควรอัปโหลด ใช้พารามิเตอร์นี้เฉพาะเมื่อไม่ได้ระบุชื่อชุดการทดสอบไว้เท่านั้น

##### <a name="upload-examples"></a>อัปโหลด: ตัวอย่าง

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

อัปโหลดเฉพาะไฟล์การบันทึกที่เป็นของกรณีทดสอบที่ระบุอย่างน้อยหนึ่งรายการไปยัง Azure DevOps

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: พารามิเตอร์ที่ต้องใช้

+ `test_case_id1`: แสดงรหัสกรณีทดสอบแรกสำหรับการบันทึกที่ควรอัปโหลดไปยัง Azure DevOps
+ `test_case_idN`: แสดงรหัสกรณีทดสอบสุดท้ายสำหรับการบันทึกที่ควรอัปโหลดไปยัง Azure DevOps

##### <a name="uploadrecording-examples"></a>uploadrecording: ตัวอย่าง

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>การใช้

แสดงโหมดการใช้งานของแอปพลิเคชันนี้สามโหมด

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

การเรียกใช้แอปพลิเคชันในแบบโต้ตอบ:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

การเรียกใช้แอปพลิเคชันโดยระบุคำสั่ง:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

การเรียกใช้แอปพลิเคชันในโดยระบุไฟล์การตั้งค่า:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

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
