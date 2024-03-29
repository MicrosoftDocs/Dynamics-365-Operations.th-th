---
title: ตัวเลือกการจัดรูปแบบขั้นสูงในรายงานทางการเงิน
description: บทความนี้จะอธิบายถึงฟังก์ชันการจัดรูปแบบขั้นสูง ซึ่งรวมถึงตัวกรองข้อมูล ข้อจํากัด แถวที่ไม่มีการพิมพ์ และใบแจ้งยอดแบบมีเงื่อนไข ในการคํานวณ
author: panolte
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.form: FinancialReports
ms.openlocfilehash: 0bc0308fc6140a8b45de1b207a12307a6d731639
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291436"
---
# <a name="advanced-formatting-options-in-financial-reporting"></a>ตัวเลือกการจัดรูปแบบขั้นสูงในรายงานทางการเงิน

[!include [banner](../includes/banner.md)]

เมื่อคุณสร้างรายงานในรายงานทางการเงิน ฟังก์ชันการจัดรูปแบบเพิ่มเติมจะพร้อมใช้งาน รวมถึงตัวกรองสำหรับขนาด ข้อจำกัดสำหรับคอลัมน์ และหน่วยการรายงาน แถวที่ไม่มีการพิมพ์ และคำสั่ง IF/THEN/ELSE ในการคำนวณ

ตารางต่อไปนี้อธิบายถึงฟังก์ชันการจัดรูปแบบขั้นสูงที่พร้อมใช้งานเมื่อคุณออกแบบรายงาน

| ฟังก์ชัน                   | คำอธิบาย |
|----------------------------|-------------|
| ตัวกรองข้อมูลมิติ           | เพื่อให้เข้าถึงชุดข้อมูลเฉพาะ คุณสามารถใช้มิติในคำนิยามแถวและคำนิยามคอลัมน์ รายงานหลายฉบับใช้เฉพาะเซกเมนต์ธรรมชาติในรูปแบบแถว อย่างไรก็ตาม สามารถปรับแก้แถวได้จึงได้รวมค่ามิติด้วย จะใช้ตัวกรองมิติในคำนิยามคอลัมน์เพื่อให้เข้าถึงค่ามิติเฉพาะ |
| การรายงานข้อจำกัดในหน่วย | คุณสามารถตั้งค่าแถวรายงาน รายงานจึงแสดงเฉพาะข้อมูลที่เชื่อมโยงกับหน่วยการรายงานที่ระบุไว้ |
| แถวที่ไม่มีการพิมพ์ (NP)     | แถวที่ไม่มีการพิมพ์จะมีประโยชน์ในรายงานหลายฉบับ ถ้าต้องการการคำนวณหลายครั้งในออเดอร์เพื่อให้ได้ค่า คุณสามารถซ่อนการคำนวณเหล่านี้ในรายงานที่พิมพ์ แถวที่ไม่มีการพิมพ์จะมีประโยชน์สำหรับการแก้ไขปัญหาการออกแบบรายงานและสำหรับการจัดวางเซลล์ขั้นสูง |
| ข้อจำกัดของคอลัมน์         | ข้อจำกัดของคอลัมน์ในคำนิยามแถวมีประโยชน์สำหรับการซ่อนค่าที่เกี่ยวข้องเฉพาะในบางแถวของรายงาน เมื่อคำนวณเปอร์เซ็นต์ในแถว ข้อจำกัดของคอลัมน์จะป้องกันไม่ให้พิมพ์คอลัมน์ทั้งหมดหรือคอลัมน์อื่นเมื่อไม่ได้ใช้หมายเลขขอคอลัมน์นั้นๆ |
| ตัวแบ่งคอลัมน์               | คุณสามารถเพิ่มตัวแบ่งคอลัมน์ในคำนิยามแถวเพื่อแสดงข้อมูลรายงานข้างๆกัน คุณสามารถเพิ่มตัวแบ่งคอลัมน์หลายตัวในคำนิยามแถวเดียว และหัวกระดาษของคอลัมน์จะถูกทำซ้ำที่ด้านบนของแต่ละคอลัมน์หลังตัวแบ่งคอลัมน์ ข้อคิดเห็นสำหรับรายงานจะแสดงอยู่ระหว่างตัวแบ่งคอลัมน์ |
| คำสั่ง IF/THEN/ELSE     | คุณสามารถปรับเปลี่ยนการคำนวณในคำนิยามแถวหรือคำนิยามคอลัมน์ |
| ใช้ใบเสนอราคาเดี่ยว ('') และเครื่องหมายและ (&) สำหรับค่ามิติ | คุณสามารถใช้ค่ามิติ ซึ่งรวมถึงเครื่องหมายและ สำหรับการออกแบบรายงานได้ |

## <a name="advanced-cell-placement"></a>การจัดวางเซลล์ขั้นสูง

การจัดวางเซลล์ขั้นสูงหรือ *การบังคับ* เกี่ยวข้องกับการจัดวางค่าเฉพาะลงในเซลล์ที่ระบุ ตัวอย่างเช่น forcing มักใช้ในการย้ายยอดดุลที่ถูกต้องในงบกระแสเงินสด คุณสามารถใช้การบังคับสำหรับวัตถุประสงค์ดังต่อไปนี้:

- ย้ายค่าจาก Microsoft Excel ไปยังเซลล์เฉพาะ
- ค่ารหัสแบบตายตัวเฉพาะไปยังรายงาน
- ปรับเปลี่ยนเครื่องหมายด้วยการคัดลอกค่าจากเซลล์ก่อนหน้าและคูณค่านั้นด้วย -1

> [!NOTE]
> ในหลายกรณี คุณต้องตั้งค่าคอนฟิกข้อกำหนดของรายงานของคุณ เพื่อให้มีการทำการคำนวณคอลัมน์ ก่อนการคำนวณแถว เพื่อให้การตั้งค่าคอนฟิกนี้เสร็จสมบูรณ์ ให้ปฏิบัติดังนี้
>
> 1. ในโปรแกรมออกแบบรายงาน เปิดคำนิยามแถว
> 2. ในแท็บ **การตั้งค่า** ภายใต้ **ลำดับความสำคัญในการคำนวณ** เลือก **ทำการคำนวณคอลัมน์แรกแล้วก็แถว**

## <a name="designing-the-report"></a>การออกแบบรายงาน

เมื่อคุณออกแบบรายงาน คุณควรสร้างแถวรายละเอียดทั้งหมดก่อนเพื่อให้แน่ใจว่า มูลค่าจะถูกดึงมาตามที่คาดไว้ หลังจากนั้น เพิ่ม **NP** (ไม่พิมพ์) รูปแบบการแทนที่เพื่อไม่แสดงรายละเอียดที่รวมค่าสุดท้าย

> [!IMPORTANT]
> เมื่อคุณใช้รหัสรูปแบบ **CAL** ในคำนิยามแถว คุณจะไม่สามารถดูรายละเอียดแนวลึกของธุรกรรมได้

สำหรับการบังคับ ใช้รูปแบบสูตรต่อไปนี้: &lt;คอลัมน์ปลายทาง&gt;=&lt;คอลัมน์เริ่มต้น&gt;.&lt;รหัสแถว&gt; แยกการจัดวางเพิ่มเติมต่างๆ สำหรับแถวโดยเครื่องหมายจุลภาคและช่องว่าง นี่คือตัวอย่าง: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>ตัวอย่างของตัวเลือกการจัดรูปแบบขั้นสูง

ตัวอย่างต่อไปนี้แสดงวิธีการจัดรูปแบบคำนิยามแถวและคำนิยามคอลัมน์เพื่อบังคับรายงานกระแสเงินสดพื้นฐาน (ตัวอย่างที่ 1) และรายงานทางสถิติ (ตัวอย่างที่ 2)

### <a name="example-1-basic-forcing"></a>ตัวอย่างที่ 1: การบังคับพื้นฐาน

ตารางต่อไปนี้แสดงตัวอย่างของคำนิยามแถวที่ใช้การบังคับพื้นฐาน

| รหัสแถว |           คำอธิบาย            | รหัสรูปแบบ | สูตร/แถว/หน่วยที่เกี่ยวข้อง |        ตัวปรับเปลี่ยนแถว        | ลิงก์ที่เชื่อมโยงไปยังมิติทางการเงิน |
|----------|----------------------------------|-------------|-----------------------------|----------------------------|------------------------------|
| 100      | เงินสดในช่วงเริ่มต้นของระยะเวลา (NP) |             |                             | ตัวปรับเปลี่ยนบัญชี = \[/BB\] | +เซกเมนต์2 = \[1100\]         |
| 130      | เงินสด ณ ต้นงวด      | CAL         | C=C.100,F=D.100             |                            |                              |
| 160      |                                  |             |                             |                            |                              |
| 190      |                                  |             |                             |                            |                              |

> [!NOTE]
> คอลัมน์ที่ว่างเปล่าได้ถูกลบออกจากตารางก่อนหน้านี้เพื่องานนำเสนอ: คอลัมน์แทนที่รูปแบบ ยอดดุลปกติ ควบคุมการพิมพ์ ข้อจำกัดของคอลัมน์จะไม่ถูกแสดง

ตารางต่อไปนี้แสดงตัวอย่างของคำนิยามแถวที่ใช้การบังคับพื้นฐานในแถว

|           รูปแบบ             | A   | B    | C        | D      | E      | ศ.    |
|------------------------------|-----|------|----------|--------|--------|------|
| ส่วนหัว 1                     |     |      |          |        |        |      |
| ส่วนหัว 2                     | A   | B    | C        | D      | E      | ศ.    |
| ส่วนหัว 3                     |     |      |          |        |        |      |
| ชนิดคอลัมน์                  | ROW | DESC | ดีมอนตัวกรอง       | ดีมอนตัวกรอง     | ดีมอนตัวกรอง     | การคำนวน |
| รหัสสมุดบัญชี/ประเภทแอตทริบิวต์ |     |      | ค่าจริง   | ค่าจริง | ค่าจริง |      |
| ปีบัญชี                  |     |      | ฐาน     | ฐาน   | ฐาน   |      |
| รอบระยะเวลา                       |     |      | ฐาน     | ฐาน   | ฐาน   |      |
| รอบระยะเวลาที่ครอบคลุม              |     |      | ประจำงวด | YTD/BB | YTD    |      |
| สูตร                      |     |      |          |        |        | E-D  |
| ความกว้างของคอลัมน์                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>ตัวอย่างที่ 2: รายงานเชิงสถิติ

ตารางต่อไปนี้แสดงตัวอย่างของคำนิยามแถวที่ใช้การบังคับพื้นฐานสำหรับรายงานเชิงสถิติ

| รหัสแถว | คำอธิบาย               | จัดรูปแบบรหัส | สูตร/แถว/หน่วยที่เกี่ยวข้อง     | แทนที่รูปแบบ      | ยอดดุลปกติ | ลิงก์ที่เชื่อมโยงไปยังมิติทางการเงิน               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|--------------------------------------------|
| 50       | ข้อมูลเชิงสถิติ   | REM         |                                 |                      |                |                                            |
| 100      | จำนวนพนักงาน - สหรัฐอเมริกา            | CAL         | 4 ชั่วโมง                               | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 115      | จำนวนพนักงาน - สากล | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 130      |                           |             |                                 |                      |                |                                            |
| 190      | การขายของสหรัฐอเมริกา                  |             |                                 |                      | C              | +เซกเมนต์2 = \[41\*\], เซกเมนต์3 = \[00\]    |
| 220      | การขายระหว่างประเทศ       |             |                                 |                      | C              | +เซกเมนต์2 = \[41\*\], เซกเมนต์3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |                                            |
| 280      |                           |             |                                 |                      |                |                                            |
| 310      | การขายของสหรัฐอเมริกา                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |                                            |
| 340      | การขายระหว่างประเทศ       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |                                            |

> [!NOTE]
> คอลัมน์ที่ว่างเปล่าได้ถูกลบออกจากตารางก่อนหน้านี้เพื่องานนำเสนอ: คอลัมน์การควบคุมการพิมพ์ คอลัมน์ข้อจำกัดของคอลัมน์ และคอลัมน์ตัวปรับเปลี่ยนแถว จะไม่ถูกแสดง

ตารางต่อไปนี้แสดงตัวอย่างของคำนิยามคอลัมน์ที่ใช้การบังคับพื้นฐานสำหรับรายงานเชิงสถิติ

|    รูปแบบ                    | A   | B    | C      | D            | E     | ศ.            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| ส่วนหัว 1                     | A   | B    | C      | D            | E     | ศ.            |
| ส่วนหัว 2                     | -   | -    | YTD    | การขายประจำปี | พนักงาน | $ ต่อคน |
| หัวกระดาษ 3                     |     |      |        |              |       |              |
| ชนิดคอลัมน์                  | แถว | DESC | ดีมอนตัวกรอง     | การคำนวน         | การคำนวน  | การคำนวน         |
| รหัสสมุดบัญชี/ประเภทแอตทริบิวต์ |     |      | ค่าจริง |              |       |              |
| ปีบัญชี                  |     |      | ฐาน   |              |       |              |
| รอบระยะเวลา                       |     |      | ฐาน   |              |       |              |
| รอบระยะเวลาที่ครอบคลุม              |     |      | YTD    |              |       |              |
| สูตร                      |     |      |        |              |       | E-D          |
| ความกว้างของคอลัมน์                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>การจำกัดแถวไปยังหน่วยการรายงานเฉพาะ

เมื่อแถวรายงานถูกจำกัดไปยังหน่วยการรายงานเฉพาะ แถวนั้นจะแสดงเฉพาะข้อมูลที่เชื่อมโยงสำหรับชื่อหน่วยการรายงาน และละเว้นข้อมูลสำหรับหน่วยรายงานอื่นๆ ในแผนภูมิการรายงาน ตัวอย่างเช่น คุณสามารถสร้างแถวที่แสดงรายละเอียดสำหรับค่าใช้จ่ายในการดำเนินงานทั้งหมดสำหรับแผนกที่ระบุ รายงานของคุณอาจประกอบด้วยข้อมูลซ้ำถ้ารายงานประกอบด้วยทั้งแผนภูมิการรายงานและคำนิยามแถวที่มีมากกว่าเพียงแค่บัญชีธรรมชาติ ตัวอย่างเช่น คุณมีแผนภูมิการรายงานที่แสดงรายการหกแผนกในองค์กรของคุณ และคุณยังมีคำนิยามแถวที่แสดงรายการเฉพาะเจาะจงซึ่งเป็นการรวมระหว่างบัญชีและแผนกในแถว เมื่อคุณสร้างรายงาน รายการเฉพาะเจาะจงซึ่งเป็นการรวมของบัญชีและแผนกจะถูกพิมพ์ในทุกระดับของแผนภูมิการรายงาน ถึงแม้ว่าอาจจะมีแผนกที่ไม่ตรงกับสิ่งที่อยู่ในแผนภูมิก็ตาม พฤติกรรมนี้เกิดขึ้นเนื่องจากแถวจะแทนที่สิ่งที่ถูกกรองออกไปตามข้อกำหนดของรายงาน วิธีการหนึ่งที่คุณสามารถหลีกเลี่ยงการทำซ้ำของข้อมูลคือ ด้วยการจำกัดแถวไปยังหน่วยการรายงานเฉพาะ

> [!NOTE]
> ถ้าแถวรวมถึงมิติ และคุณจำกัดแถวนั้นไปยังหน่วยรองของการรายงาน จำนวนแถวจะถูกรวมไว้สำหรับหน่วยรองและสำหรับหน่วยหลัก แต่จะไม่มีการทำซ้ำเกิดขึ้น

### <a name="restrict-a-row-to-a-reporting-unit"></a>จำกัดแถวไปยังหน่วยการรายงาน

1. ในโปรแกรมออกแบบรายงาน คลิก **คำนิยามแถว** แล้วจึงเลือกคำนิยามแถวเพื่อแก้ไข
2. ดับเบิลคลิกที่เซลล์ **สูตร/แถว/หน่วยที่เกี่ยวข้อง** ที่เหมาะสม
3. ในกล่องโต้ตอบ **การเลือกหน่วยการรายงาน** ในฟิลด์ **ลำดับการรายงาน** เลือกลำดับที่กำหนดไว้ในข้อกำหนดของรายงาน
4. เลือกหน่วยการรายงาน แล้วจึงคลิก **ตกลง** ข้อจำกัดจะปรากฏขึ้นในเซลล์ของคำนิยามแถว
5. ดับเบิลคลิกเซลล์ใน **ลิงค์ไปยังมิติทางการเงิน** คอลัมน์ของการจำกัดแถว และจากนั้น ป้อนลิงค์ไปยังระบบข้อมูลทางการเงิน

## <a name="selecting-print-control-in-a-row-definition"></a>เลือกตัวควบคุมการพิมพ์ในคำนิยามแถว

คุณสามารถระบุรหัสตัวควบคุมการพิมพ์สำหรับแต่ละคอลัมน์ โดยใช้เซลล์ **ควบคุมการพิมพ์** ได้

### <a name="add-print-control-codes-to-a-report-row"></a>เพิ่มรหัสควบคุมการพิมพ์ไปที่แถวรายงาน

1. ในโปรแกรมออกแบบรายงาน เปิดคำนิยามแถวเพื่อแก้ไข
2. ดับเบิลคลิกเซลล์ **ควบคุมการพิมพ์**
3. ในกล่องโต้ตอบ **ควบคุมการพิมพ์** เลือกรหัสควบคุมการพิมพ์หรือกดปุ่ม Ctrl ค้างไว้เพื่อเลือกหลายรหัส คุณยังสามารถพิมพ์รหัสควบคุมการพิมพ์โดยตรงในเซลล์ **ควบคุมการพิมพ์** ใช้เครื่องหมายจุลภาคแยกรหัสควบคุมการพิมพ์หลายรหัสออกจากกัน
4. เลือกตัวเลือกการพิมพ์แบบมีเงื่อนไขใดๆ
5. คลิก **ตกลง** ระบบจะนำเข้าข้อมูลการชำระเงิน

### <a name="regular-print-control-codes"></a>รหัสควบคุมการพิมพ์แบบปกติ

ตารางต่อไปนี้อธิบายรหัสควบคุมการพิมพ์ปกติสำหรับคำนิยามแถว

| รหัสควบคุมการพิมพ์ | การแปลของรหัสควบคุมการพิมพ์         | คำอธิบาย |
|--------------------|--------------------------------------------------|-------------|
| NP                 | แถวที่ไม่มีการพิมพ์ (NP)                                 | ป้องกันไม่ให้มีการพิมพ์ยอดเงินในแถวลงในรายงาน และไม่รวมยอดเงินจากการคำนวณ เพื่อรวมคอลัมน์ไม่มีการพิมพ์ในการคำนวณ อ้างอิงถึงคอลัมน์ได้โดยตรงในสูตรการคำนวณ ตัวอย่างเช่น มีแถว 240 ที่ไม่มีการพิมพ์รวมอยู่ในการคำนวณต่อไปนี้: **230+240+250** แต่ แถว 240 ที่ไม่มีการพิมพ์จะไม่รวมอยู่ในการคำนวณต่อไปนี้: **230:250** |
| CS                 | สัญลักษณ์สกุลเงิน ใช้รูปแบบสกุลเงินในแถวนี้ | รวมสัญลักษณ์สกุลเงินในทุกยอดเงินที่ไม่ใช่เปอร์เซ็นต์ ค่าเปอร์เซ็นต์ไม่เคยรับสัญลักษณ์สกุลเงิน |
| XD                 | ไม่แสดงแถวในรายงานรายละเอียดบัญชี            | ระงับการแสดงบัญชีในรายงานรายละเอียดบัญชีและรายงานรายละเอียดธุรกรรม ตัวควบคุมการพิมพ์นี้มีประโยชน์เมื่อแถวรวมหลายบัญชีที่ไม่ได้อยู่ในรายการบนรายงานรายละเอียดบัญชีหรือรายงานรายละเอียดธุรกรรม |
| X0                 | ระงับแถวถ้าทั้งหมดเป็นศูนย์                        | ไม่รวมแถวจากรายงาน ถ้าทุกเซลล์ในแถวนั้นว่างเปล่าหรือเป็นเลขศูนย์ ตัวควบคุมการพิมพ์นี้มีความหมายเฉพาะเมื่อไม่ได้เลือกตัวเลือกเพื่อระงับยอดดุลเป็นศูนย์ในข้อกำหนดของรายงาน |
| B0                 | ปล่อยคอลัมน์ศูนย์ให้ว่างไว้                         | ปล่อยคอลัมน์ว่างเปล่าในแถวที่มียอดเงินเป็นศูนย์ |
| XR                 | ระงับการเลื่อนแถวขึ้น                                  | ระงับการสะสม ถ้ารายงานใช้แผนภูมิการรายงาน ไม่เลื่อนยอดเงินในแถวขึ้นไปยังโหนดหลักในอันดับถัดมา |
| SR                 | ระงับการปัดเศษ                                | ป้องกันยอดเงินในแถวนี้จากการถูกปัดเศษ |
| ข้อความ                 | ระงับการแสดงแถวในรายงานรายละเอียดธุรกรรม        | ระงับการแสดงธุรกรรมในรายงานรายละเอียดธุรกรรม ตัวควบคุมการพิมพ์นี้มีประโยชน์เมื่อแถวรวมหลายบัญชีที่ไม่ควรอยู่ในรายการบนรายงานรายละเอียดธุรกรรม |

### <a name="conditional-print-control-codes"></a>รหัสควบคุมการพิมพ์แบบมีเงื่อนไข

ตารางต่อไปนี้อธิบายรหัสควบคุมการพิมพ์อย่างมีเงื่อนไขสำหรับคำนิยามแถว

| รหัสควบคุมการพิมพ์ | คำอธิบาย                                  |
|--------------------|----------------------------------------------|
| (ไม่มี)             | ล้างการเลือกการพิมพ์แบบมีเงื่อนไข       |
| DR                 | พิมพ์เฉพาะดุลเดบิตสำหรับแถวนี้  |
| CR                 | พิมพ์เฉพาะดุลเครดิตสำหรับแถวนี้ |

## <a name="column-restriction-cell-in-a-row-definition"></a>คอลัมน์เซลล์ข้อจำกัดในคำนิยามแถว

เซลล์ **จำกัดคอลัมน์** ในคำนิยามแถวมีหลายวัตถุประสงค์ ขึ้นอยู่กับชนิดของแถว คุณสามารถใช้เซลล์ **การจำกัดคอลัมน์** เพื่อระบุหนึ่งฟังก์ชันต่อไปนี้:

- เซลล์สามารถจำกัดการพิมพ์จำนวนแถวไปยังคอลัมน์ที่ระบุได้ ฟังก์ชันนี้มีประโยชน์ถ้าคุณกำลังสร้างตารางงบดุล
- เซลล์สามารถระบุคอลัมน์ยอดเงินในการเรียงลำดับ

## <a name="using-a-calculation-formula-in-a-row-definition"></a>ใช้สูตรการคำนวณในคำนิยามแถว

สูตรการคำนวณในคำนิยามแถวสามารถรวม **+**, **-**, **\**_ และ _*/** ตัวดำเนินการ และยังรวม คำสั่ง **IF/THEN/ELSE** นอกจากนี้ การคำนวณสามารถเกี่ยวข้องกับแต่ละเซลล์และยอดเงินที่แน่นอน (หมายเลขจริงที่จะรวมอยู่ในสูตร) สูตรสามารถมีอักขระได้มากถึง 1024 อักขระ การคำนวณไม่สามารถใช้กับแถวที่มีเซลล์ของชนิด **ลิงค์ไปยังมิติทางการเงิน** (ดีมอนตัวกรอง) ได้ อย่างไรก็ตาม คุณสามารถรวมการคำนวณในแถวที่ต่อเนื่องกัน ระงับการพิมพ์แถวเหล่านั้น แล้วหลังจากนั้นก็รวมแถวการคำนวณ

### <a name="operators-in-a-calculation-formula"></a>ตัวดำเนินการในสูตรการคำนวณ

สูตรการคำนวณใช้ตัวดำเนินการซับซ้อนมากกว่าสูตรแถวผลรวม อย่างไรก็ตาม คุณสามารถใช้ **\**_ และ _*/** ตัวดำเนินการพร้อมกับตัวดำเนินการเพิ่มเติมเพื่อคูณ (/) และหาร (\*) ยอดเงินได้ เมื่อใช้ช่วงหรือผลรวมในสูตรการคำนวณ คุณต้องใส่เครื่องหมาย (@) ไว้หน้ารหัสแถวใดๆ ยกเว้นว่าคุณกำลังใช้คอลัมน์ในคำนิยามแถว ตัวอย่างเช่น เพื่อเพิ่มยอดเงินในแถว 100 ไปที่ยอดเงินในแถว 330 คุณสามารถใช้สูตรรวมแถว **100+330** หรือสูตรการคำนวณ **@100+@330** ได้

> [!NOTE]
> คุณต้องใช้เครื่องหมายที่ (@) ก่อนรหัสแถวทุกรหัสที่คุณใช้ในสูตรการคำนวณ มิฉะนั้น หมายเลขจะถูกอ่านเป็นจำนวนเต็ม ตัวอย่างเช่น สูตร **@100+330** เพิ่มยอดเงิน 330 USD ไปที่แถว 100 เมื่อคุณอ้างอิงคอลัมน์ในสูตรการคำนวณ เครื่องหมาย (@) ก็ไม่จำเป็น

### <a name="create-a-calculation-formula"></a>สร้างสูตรการคำนวณ

1. ในโปรแกรมออกแบบรายงาน คลิก **คำนิยามแถว** แล้วจึงเปิดคำนิยามแถวเพื่อแก้ไข
2. ดับเบิลคลิกเซลล์ **รหัสรูปแบบ** จากนั้นเลือก **CAL**
3. ในเซลล์ **สูตร/แถว/หน่วยที่เกี่ยวข้อง** พิมพ์สูตรการคำนวณ

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>ตัวอย่างของสูตรการคำนวณสำหรับแถวที่ระบุ

ในตัวอย่างนี้ สูตรการคำนวณ **@100+@330** หมายความว่า จำนวนในแถว 100 ถูกเพิ่มไปยังจำนวนในแถว 330 สูตรโดยรวมของแถว **340+370** เพิ่มยอดเงินในแถว 340 ไปที่ยอดเงินในแถว 370 (ยอดเงินในแถว 370 คือ ยอดเงินจากสูตรการคำนวณ)

| รหัสแถว | คำอธิบาย                 | รหัสรูปแบบ | สูตร/แถว/หน่วย ที่เกี่ยวข้อง | ควบคุมการพิมพ์ | ตัวแก้ไขแถว | ลิงค์ไปยังมิติทางการเงิน |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | เงินสด ณ ต้นงวด |             |                            | NP            | BB           | +บัญชี=\[1100:1110\]       |
| 370      | เงินสด ณ ต้นปี   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | เงินสด ณ ต้นงวด | TOT         | 340+370                    |               |              |                              |

เมื่อแถวในคำนิยามแถวมีรหัสรูปแบบของ **CAL** และคุณป้อนการคำนวณทางคณิตศาสตร์ในเซลล์ **สูตร/แถว/หน่วยที่เกี่ยวข้อง** คุณยังต้องป้อนหนังสือเชื่อมโยงคอลัมน์และแถวในรายงานด้วย ตัวอย่างเช่น ป้อน **A.120** เพื่อแสดงคอลัมน์ A แถว 120 อีกทางหนึ่งคือ คุณสามารถใช้เครื่องหมาย (@) เพื่อบ่งชี้คอลัมน์ทั้งหมดได้ ตัวอย่างเช่น ป้อน **@120** เพื่อแสดงถึงคอลัมน์ทั้งหมดในแถว 120 การคำนวณทางคณิตศาสตร์ใดๆ ที่ไม่มีตัวอักษรคอลัมน์ หรือมีเครื่องหมาย (@) จะถือว่าเป็นตัวเลขจริง

> [!NOTE]
> ถ้าคุณใช้รหัสแถวป้ายชื่อเพื่ออ้างอิงแถว คุณต้องใช้เครื่องหมายมหัพภาค (.) เป็นตัวแบ่งระหว่างตัวอักษรในคอลัมน์และป้ายชื่อ (ตัวอย่างเช่น **A.GROSS\_MARGIN/A.SALES**) ถ้าคุณใช้ at sign (@) ไม่จำเป็นต้องมีตัวแบ่ง (ตัวอย่างเช่น **\@GROSS\_MARGIN/@SALES**)

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>ตัวอย่างของสูตรการคำนวณสำหรับคอลัมน์ที่ระบุ

ในตัวอย่างนี้ สูตรการคำนวณ **E=C.340** หมายความว่าระบบจะคำนวณในเซลล์ในคอลัมน์ C แถว 340 เฉพาะบนคอลัมน์ E

> [!NOTE]
> เมื่อคุณอ้างอิงคอลัมน์ในสูตรการคำนวณ เครื่องหมาย (@) ก็ไม่จำเป็น

| รหัสแถว | คำอธิบาย                 | รหัสรูปแบบ | สูตร/แถว/หน่วย ที่เกี่ยวข้อง | ควบคุมการพิมพ์ | ตัวแก้ไขแถว | ลิงค์ไปยังมิติทางการเงิน |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | เงินสดในช่วงเริ่มต้นของระยะเวลา |             |                            | NP            | BB           | +บัญชี=\[1100:1110\]       |
| 370      | เงินสดในช่วงเริ่มต้นปี   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | เงินสดในช่วงเริ่มต้นของระยะเวลา | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>การปรับเปลี่ยนตัวเลขในคอลัมน์ที่เลือก

เมื่อคุณปรับเปลี่ยนตัวเลขการคำนวณในคอลัมน์หนึ่งของแถวเฉพาะแต่ไม่ต้องการให้มีผลกับคอลัมน์อื่นๆ ในรายงาน คุณสามารถระบุ **CAL** (คำนวณ) ใน **รูปแบบรหัส** คอลัมน์ของคำนิยามแถว

- เพื่อดำเนินการคำนวณบนรายงานทั้งหมด (**ดีมอนตัวกรอง**) คอลัมน์ อย่าป้อนการกำหนดคอลัมน์
- เพื่อจำกัดสูตรไปยังคอลัมน์ที่ระบุ ป้อนจดหมายคอลัมน์ เครื่องหมายเท่ากับ (**=**) แล้วก็สูตร
- คุณสามารถระบุหลายคอลัมน์ เมื่อคุณใช้เครื่องหมาย (@) กับการจัดวางคอลัมน์ที่ระบุ เครื่องหมาย(@) จะเชื่อมโยงกับแถว
- คุณสามารถป้อนหลายสูตรคอลัมน์ในหนึ่งแถว แยกสูตรโดยใช้เครื่องหมายจุลภาค

### <a name="calculation-examples"></a>ตัวอย่างของการคำนวณ

| การคำนวณ            | การดำเนินการที่ถูกสร้างขึ้น                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | สำหรับทุกคอลัมน์ ค่าในแถว 130 จะคูณ ด้วย 0.75. ผลลัพธ์มีแล้ววางในแถวปัจจุบันของทุกคอลัมน์ |
| B=@130\*.75            | ทำการคำนวณเดียวเท่านั้นในคอลัมน์ b                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>คำสั่ง IF/THEN/ELSE ในคำนิยามแถว

**สามารถเพิ่มคำสั่ง IF/THEN/ELSE** เพื่อคำนวณใดๆ ที่ถูกต้อง และใช้กับรูปแบบ **CAL** ได้ คุณป้อน **IF/THEN/ELSE** สูตรการคำนวณในเซลล์ในคอลัมน์ **สูตร/แถว/หน่วยที่เกี่ยวข้อง** สูตรคำนวณ **IF/THEN/ELSE** ใช้รูปแบบต่อไปนี้: IF &lt;งบจริง/เท็จ&gt; THEN &lt;สูตร&gt; ELSE &lt;สูตร&gt; **ELSE &lt;สูตร&gt;** ส่วนหนึ่งของคำสั่งเป็นตัวเลือก

#### <a name="if-statements"></a>คำสั่ง IF

คำสั่งที่เป็นไปตาม **IF** อาจเป็นคำสั่งใดๆ ที่สามารถประเมินเป็นจริงหรือเท็จได้ คำสั่งที่เป็นไปตาม **IF** คำสั่งอาจเกี่ยวข้องกับการประเมินอย่างง่าย หรืออาจเป็นคำสั่งที่ซับซ้อนซึ่งสามารถประกอบด้วยหลายนิพจน์ ยกตัวอย่างเช่น

- **IF A.200&gt;0** (การประเมินอย่างง่าย)
- **IF A.200&gt;0 AND A.200&lt;10,000** (คำสั่งที่ซับซ้อน)
- **IF A.200&gt;10000 หรือ ((A.340/B.1200)\*2 &lt;1200)** (คำสั่งซับซ้อนที่ประกอบด้วยหลายนิพจน์)

คำ **ระยะเวลา** ใน **IF** คำสั่งแสดงจำนวนของระยะเวลาสำหรับรายงาน คำนี้นี้โดยปกติจะใช้ในการคำนวณเป็นค่าเฉลี่ยของปีจนถึงวันที่ ตัวอย่างเช่น เมื่อคุณรันรายงานสำหรับรอบระยะเวลา 7 YTD คำสั่ง **B.150/Periods** หมายความว่าค่าในแถว 150 ของคอลัมน์ B จะถูกหาร ด้วย 7

#### <a name="then-and-else-formulas"></a>สูตร THEN และ ELSE

**THEN** และ **ELSE** สูตรสามารถคำนวณใดๆ ถูกต้อง จากการกำหนดค่าไปยังสูตรที่ซับซ้อนได้ ตัวอย่างเช่น คำสั่ง **IF A.200&gt;0 THEN A=B.200** หมายถึง "ถ้าค่าในเซลล์ในคอลัมน์ A ของแถว 200 จะมากกว่า 0 (ศูนย์), วางค่าจากเซลล์ในคอลัมน์ B ของแถว 200 ลงในเซลล์ในคอลัมน์ A แถวปัจจุบัน" คำสั่ง **IF/THEN** ก่อนหน้าใส่ค่าในคอลัมน์หนึ่งของแถวปัจจุบัน อย่างไรก็ตาม คุณยังสามารถใช้เครื่องหมาย (@) ในการประเมินจริง/เท็จหรือสูตรเพื่อแสดงคอลัมน์ทั้งหมดได้ นี่คือตัวอย่างอื่นๆ ที่อธิบายไว้ในส่วนต่อไปนี้:

- **IF A.200 &gt;0 THEN B.200**: ถ้าค่าในเซลล์ A.200 เป็นบวก ค่าจากเซลล์ B.200 จะถูกใส่ไว้ในทุกคอลัมน์ของแถวปัจจุบัน
- **IF A.200 &gt;0 THEN @200**: ถ้าค่าในเซลล์ A.200 เป็นบวก ค่าจากแต่ละคอลัมน์ในแถว 200 จะถูกใส่ลงในคอลัมน์ที่สอดคล้องกันในแถวปัจจุบัน
- **IF @200 &gt;0 THEN @200**: ถ้าค่าในแถว 200 ของคอลัมน์ปัจจุบันเป็นบวก ค่าจากแถว 200 จะถูกใส่ลงในคอลัมน์เดียวกันในแถวปัจจุบัน

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>การจำกัดการคำนวณให้กับหน่วยการรายงานในคำนิยามแถว

การจำกัดการคำนวณเพื่อรายงานหน่วยเดียวในแผนภูมิการรายงาน เพื่อให้ยอดเงินเป็นผลลัพธ์ไม่ได้เลื่อนแถวขึ้นไปยังหน่วยที่ระดับสูงกว่า คุณสามารถใช้ **\@Unit** รหัสใน **สูตร/แถว/หน่วยที่เกี่ยวข้อง** เซลล์ในคำนิยามแถวได้ รหัส **\@Unit** แสดงในคอลัมน์ B ของแผนภูมิการรายงาน **ชื่อหน่วย** เมื่อคุณใช้รหัส **\@Unit** ค่าไม่เลื่อนแถวขึ้น แต่การคำนวณจะถูกประเมินในทุกระดับของแผนภูมิการรายงาน

> [!NOTE]
> ในการใช้ฟังก์ชั่นนี้ แผนภูมิการรายงานต้องเชื่อมโยงกับคำนิยามแถว

แถวการคำนวณสามารถอ้างอิงถึงแถวการคำนวณหรือแถวข้อมูลทางการเงิน การคำนวณจะถูกบันทึกในเซลล์ **สูตร/แถว/หน่วยที่เกี่ยวข้อง** ของคำนิยามแถวและการจำกัดชนิดข้อมุลทางการเงิน การคำนวณต้องใช้เงื่อนไขการคำนวณที่เริ่มต้นด้วยโครงสร้าง **IF \@Unit** นี่เป็นตัวอย่าง: IF@Unit(SALES)THEN@100 ELSE 0 การคำนวณนี้รวมถึงยอดเงินจากแถว 100 ในทุกคอลัมน์ของรายงาน แต่เฉพาะสำหรับหน่วยการขาย ถ้าหลายหน่วยถูกเรียกว่าการขาย ยอดเงินจะปรากฏในแต่ละหน่วยเหล่านั้น นอกจากนี้ แถว 100 สามารถเป็นแถวข้อมูลทางการเงิน และสามารถกำหนดเป็นไม่มีการพิมพ์ได้ ในกรณีนี้ ยอดเงินถูกป้องกันไม่ให้ปรากฏในหน่วยทั้งหมดในแผนภูมิ คุณยังสามารถจำกัดจำนวนคอลัมน์เดี่ยวของรายงาน เช่นคอลัมน์ H โดยใช้ข้อจำกัดในคอลัมน์ที่จะพิมพ์ค่าเฉพาะในคอลัมน์ของรายงานนั้น คุณสามารถรวม **หรือ** ชุดรวมในคำสั่ง **IF** ได้ ต่อไปนี้เป็นตัวอย่าง **IF @Unit(SALES) หรือ @Unit(SALESWEST) THEN 5 ELSE @100** คุณสามารถระบุหน่วยในการจำกัดชนิดของการคำนวณในวิธีใดวิธีหนึ่งต่อไปนี้:

- ป้อนชื่อหน่วยเพื่อรวมหน่วยที่ตรงกัน ตัวอย่างเช่น **IF \@Unit(SALES)** สามารถใช้ในการคำนวณสำหรับหน่วยใดๆ ที่มีชื่อว่า SALES ก็ได้ ถึงแม้ว่าจะมี SALESหลายหน่วยในแผนภูมิการรายงาน
- ป้อนชื่อบริษัทและหน่วยเพื่อจำกัดการคำนวณไปยังหน่วยที่ระบุในบริษัทที่ระบุ ตัวอย่างเช่น ป้อน **IF @Unit (ACME:SALES)** เพื่อจำกัดการคำนวณไปยังหน่วยการขายในบริษัท ACME
- ป้อนรหัสลำดับชั้นแบบเต็มจากแผนภูมิการรายงานเพื่อจำกัดการคำนวณหน่วยที่ระบุ ตัวอย่างเช่น ป้อน **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)**

> [!NOTE]
> หากต้องการค้นหารหัสลำดับชั้นแบบเต็ม คลิกขวาในคำนิยามลำดับการรายงาน แล้วเลือก **คัดลอกตัวระบุหน่วยการรายงาน (รหัส H)**

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>จำกัดการคำนวณสำหรับหน่วยการรายงาน

1. ในโปรแกรมออกแบบรายงาน คลิก **คำนิยามแถว** แล้วเปิดคำนิยามแถวเพื่อแก้ไข
2. ดับเบิลคลิกเซลล์ **รหัสรูปแบบ** จากนั้นเลือก **CAL**
3. คลิกเซลล์ **สูตร/แถว/หน่วยที่เกี่ยวข้อง** และจากนั้นป้อนการคำนวณแบบมีเงื่อนไขที่ขึ้นต้นด้วยโครงสร้าง **IF \@Unit**

### <a name="ifthenelse-statements-in-a-column-definition"></a>คำสั่ง IF/THEN/ELSE ในคำนิยามแถว

คำสั่ง **IF/THEN/ELSE** ช่วยในการคำนวณใดๆ เพื่อจะขึ้นอยู่กับผลลัพธ์จากคอลัมน์อื่น คุณสามารถอ้างอิงไปยังคอลัมน์อื่น แต่คุณไม่สามารถอ้างอิงไปยังเซลล์รายงานในคำสั่ง **IF** การคำนวณใดๆ ต้องถูกใช้กับคอลัมน์ทั้งหมด ตัวอย่างเช่น คำสั่ง **IF B&gt;100 THEN B ELSE C\*1.25** หมายถึง "ถ้ายอดเงินในคอลัมน์ B มากกว่า 100 วางค่าจากคอลัมน์ B ในคอลัมน์ **CALC** ถ้ายอดเงินในคอลัมน์ B ไม่เกิน 100 คูณค่าในคอลัมน์ C ด้วย1.25 และวางผลลัพธ์ในคอลัมน์ **คำนวณ** " ตามคำสั่ง **IF** ด้วยคำสั่งตรรกะที่สามารถประเมินเป็นจริงหรือเท็จได้เสมอ สูตรที่คุณใช้สำหรับทั้งคำสั่ง **THEN** และคำสั่ง **ELSE** สามารถประกอบด้วยข้อมูลอ้างอิงถึงจำนวนคอลัมน์ และสูตรเหล่านี้สามารถเป็นแบบซับซ้อน ตามที่คุณสร้าง

> [!NOTE]
> คุณไม่สามารถใส่ผลลัพธ์ของการคำนวณในคอลัมน์อื่นใดได้ ผลลัพธ์ต้องอยู่ในคอลัมน์ที่มีสูตร

#### <a name="use-single-quotes-and-an-ampersand-for-dimension-values-in-a-row-column-or-tree"></a>ใช้ใบเสนอราคาเดี่ยวและเครื่องหมายและสำหรับค่ามิติในแถว คอลัมน์ และแผนภูมิ

คุณสามารถออกแบบรายงานได้โดยใช้ค่ามิติที่มีเครื่องหมายและ (&)

ภายในฟิลด์ **ลิงค์ไปยังมิติทางการเงิน** ใดๆ คุณสามารถป้อนค่าได้ เช่น **'P&L'** การรวมถึงใบเสนอราคาเดี่ยว (' ') ในทั้งสองด้านของค่ามิติ บ่งชี้ว่าคุณกำลังใช้ค่าตัวอักษร เช่น การรวมถึงเครื่องหมายและ

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
