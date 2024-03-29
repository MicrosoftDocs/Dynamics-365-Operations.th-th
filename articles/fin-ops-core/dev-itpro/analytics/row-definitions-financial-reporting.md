---
title: คำนิยามแถวในผู้ออกแบบรายงานทางการเงิน
description: คำนิยามแถวคือองค์ประกอบของรายงานหรือบล็อคส่วนประกอบที่ระบุเนื้อหาของแต่ละแถวในรายงานทางการเงิน
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.form: FinancialReports
ms.openlocfilehash: 3325f76f991ea6d2a1b6131f299460e529d63d38
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802457"
---
# <a name="row-definitions-in-financial-report-designer"></a>คำนิยามแถวในผู้ออกแบบรายงานทางการเงิน

[!include [banner](../includes/banner.md)]

คำนิยามแถวคือองค์ประกอบของรายงานหรือบล็อคส่วนประกอบที่ระบุเนื้อหาของแต่ละแถวในรายงานทางการเงิน คำนิยามแถวสามารถรวมกับคำนิยามคอลัมน์ คำนิยามแผนภูมิการรายงาน และข้อกำหนดของรายงาน เพื่อสร้างกลุ่มการสร้างบล็อคที่สามารถใช้โดยบริษัทหลายบริษัท

## <a name="create-a-row-definition"></a>การสร้างคำนิยามแถว

1. ใน Report Designer ในบานหน้าต่างนำทาง คลิก **คำนิยามแถว**
2. บนเมนู **ไฟล์** ให้คลิก **สร้าง** แล้วจึงคลิก **คำนิยามแถว** ดูข้อมูลเพิ่มเติมเกี่ยวกับเนื้อหาของแต่ละเซลล์ ให้ดู [แก้ไขเซลล์คำนิยามแถว](modify-row-definition-cells-financial-reporting.md)

## <a name="open-a-row-definition"></a>เปิดคำนิยามแถว
1. ใน Report Designer ในบานหน้าต่างนำทาง คลิก **คำนิยามแถว**
2. ดับเบิลคลิกชื่อของคำนิยามแถวเพื่อเปิด
3. หากต้องการดูบล็อคส่วนประกอบใดๆ ที่เชื่อมโยงกับคำนิยามแถว ให้คลิกขวาที่คำนิยามแถว จากนั้นเลือก **การเชื่อมโยง**

## <a name="contents-of-a-row-definition"></a> เนื้อหาของคำนิยามแถว
คำนิยามแถวสามารถประกอบด้วยแถวมิติทางการเงินกว่า 20000 แถว และอาจรวมถึงข้อมูลต่อไปนี้:

- ข้อความอธิบายที่เพิ่มความหมายให้กับรายงาน โดยการสร้างหัวข้อส่วนหัว บรรทัด และเว้นวรรค เช่น **เงินสด** หรือ **รายได้รวม**
- ลิงค์ไปยังข้อมูลทางการเงินซึ่งสามารถรวมค่าตัวเลขใน Microsoft Dynamics 365 Finance

    > [!NOTE]
    > คุณสามารถตั้งค่าคำนิยามแถวให้มีการดึงข้อมูลจากระบบมิติทางการเงินทุกครั้งที่มีการสร้างรายงาน

- ผลรวมและสูตรของแถวที่ขึ้นอยู่กับข้อมูลทางการเงินที่เชื่อมโยง

โดยปกติ แต่ละแถวในคำนิยามแถวจะประกอบด้วยชนิดของข้อมูลหนึ่งชนิดดังต่อไปนี้:

- การอ้างอิงไปยังระบบมิติทางการเงิน
- ยอดรวมหรือการคำนวณที่อิงตามข้อมูล
- การจัดรูปแบบ

มีสองวิธีสำหรับการป้อนข้อมูลในคำนิยามแถว:

- ป้อนข้อมูลแถวด้วยตนเองลงในคำนิยามแถวใหม่ ดูข้อมูลเพิ่มเติมที่ [แก้ไขเซลล์คำนิยามแถว](modify-row-definition-cells-financial-reporting.md)
- ใช้ผู้ออกแบบรายงานเพื่อดึงแถวข้อมูลโดยตรงจากมิติทางการเงิน สำหรับข้อมูลเพิ่มเติม ให้ดูส่วน "สูตร/แถว/หน่วย ที่เกี่ยวข้อง" ใน [การแก้ไขเซลล์คำนิยามแถว](modify-row-definition-cells-financial-reporting.md)

## <a name="add-dimensions-in-a-row-definition"></a> เพิ่มมิติในคำนิยามแถว
มิติคือส่วนร่วมของข้อมูลและค่า คุณสามารถจัดกลุ่มข้อมูลและค่าด้วยกันในผู้ออกแบบรายงาน จากนั้นคุณสามารถจัดประเภทและวิเคราะห์ธุรกรรมโดยละเอียดมากขึ้น คุณสามารถใช้กล่องโต้ตอบ **แทรกแถวจากมิติ** เพื่อเพิ่มแถวหลายแถวที่มีคำนิยามแถวในเวลาเดียวกัน กล่องโต้ตอบแสดงคอลัมน์หนึ่งคอลัมน์สำหรับแต่ละมิติ ตารางต่อไปนี้อธิบายข้อมูลที่คุณสามารถระบุสำหรับแต่ละมิติ

| ตัวเลือก                | คำอธิบาย |
|-----------------------|-------------|
| มิติ             | รูปแบบซึ่งจะระบุมิติที่จะเพิ่มไปยังคำนิยามแถว รูปแบบนี้จะประกอบด้วยเครื่องหมาย (&) หรือเครื่องหมายตัวเลข (\#) สำหรับแต่ละตำแหน่งในมิติ โดยทั่วไป จะใช้เครื่องหมายทั้งหมดสำหรับมิติบัญชีหลักและเครื่องหมายตัวเลขทั้งหมดสำหรับมิติอื่นๆ |
| เริ่มช่วงมิติ | ค่าแรกสำหรับมิตินี้ที่ต้องการเพิ่มไปที่คำนิยามแถว |
| สิ้นสุดช่วงมิติ   | ค่าสุดท้ายสำหรับมิตินี้เพื่อเพิ่มคำนิยามแถว |

เมื่อต้องการเพิ่มมิติลงในคำนิยามแถว ทำตามขั้นตอนต่อไปนี้

1. ใน Report Designer คลิก **คำนิยามแถว** แล้วจึงเปิดคำนิยามแถวเพื่อแก้ไข
2. ในเมนู **แก้ไข** คลิก **แทรกแถวจากมิติ**
3. ในกล่องโต้ตอบ **แทรกแถวจากมิติ** ในแถว **มิติ** เลือกเซลล์สำหรับมิติที่จะถูกโอนย้ายไปยังคำนิยามแถว แล้วจึงคลิก **ทั้งหมด &&&**
4. เมื่อต้องการจำกัดคำนิยามแถวให้กับช่วงเฉพาะของค่ามิติ ป้อนค่ามิติเริ่มต้นในเซลล์ **เริ่มต้นช่วงมิติ** จากนั้นป้อนค่ามิติสิ้นสุดในเซลล์ **สิ้นสุดช่วงมิติ** หากต้องการรวมค่าทั้งหมดสำหรับมิติที่เลือก ให้ปล่อยเซลล์เหล่านี้ให้ว่างไว้

    > [!NOTE]
    > อักขระตัวแทน (\* or ?) ในช่วงมิติอาจไม่ส่งคืนผลลัพธ์ทั้งหมดที่คุณต้องการ โดยขึ้นอยู่กับวิธีการที่ฐานข้อมูล ERP สอบทานข้อมูล

5. ในฟิลด์ **เริ่มต้นรหัสแถว** ระบุรหัสแถวสำหรับค่ามิติแรกที่จะเพิ่มไปยังคำนิยามแถว
6. ในฟิลด์ **เพิ่มแต่ละแถวโดย** ระบุความแตกต่างระหว่างรหัสแถวที่ต่อเนื่องกัน ตัวอย่างเช่น ถ้ารหัสแถวแรกเป็น 100 และค่าที่เพิ่มขึ้นคือ 30 แถวใหม่แถวแรกๆ จะมีรหัส 100, 130, 160, 190 และ 220 ใช้ค่าเพิ่มขึ้นที่มีช่องว่างสำหรับการแทรกแถวรูปแบบและสูตรใหม่
7. คลิก **ตกลง** ระบบจะนำเข้าข้อมูลการชำระเงิน สำหรับค่ามิติที่เลือกแต่ละค่า บรรทัดหนึ่งบรรทัดจะถูกเพิ่มไปยังคำนิยามแถว

## <a name="adjust-rounding-in-a-row-definition"></a> ปรับปรุงการปัดเศษในคำนิยามแถว
ถ้าคุณมีงบดุลที่ยอดเงินถูกปัดเศษแล้ว ยอดรวมอาจมีการเสียดุล ปัญหานี้อาจเกิดขึ้นได้ถ้า ตัวอย่างเช่น คุณใช้ตัวเลือกการปัดเศษในรายงานงบดุล และข้อกำหนดของรายงานยังระบุการปัดเศษอีกด้วย คุณสามารถใช้ตัวเลือก **การปรับปรุงการปัดเศษ** ในคำนิยามแถวเพื่อให้ยอดเงินในงบดุลสมดุล คุณสามารถปิดหรือแก้ไขการปัดเศษบนแท็บ **การตั้งค่า** ของข้อกำหนดของรายงานได้ ตารางต่อไปนี้แสดงวิธีการปัดเศษยอดเงิน ในตารางนี้ ผลรวมของแถว 100 และ 200 แตกต่างกันเมื่อการปัดเศษถูกเปิดอยู่

| รหัสแถว | ยอดเงินโดยไม่มีการปัดเศษ | ยอดเงินที่มีการปัดเศษเป็นหลักพันทั้งหมด |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4 ชั่วโมง                                       |
| 200      | 3,700                    | 4 ชั่วโมง                                       |
| ยอดรวม    | 7,300                    | 8                                       |

หากต้องการปรับปรุงการปัดเศษในงบดุล ให้ทำตามขั้นตอนต่อไปนี้

1. ใน Report Designer คลิก **คำนิยามแถว** แล้วจึงเปิดคำนิยามแถวเพื่อแก้ไข
2. บนเมนู **แก้ไข** คลิก **ยอดปรับปรุงรายการที่ปัดเศษ**
3. ในกล่องโต้ตอบ **ยอดปรับปรุงรายการที่ปัดเศษ** ป้อนค่าต่อไปนี้:

    - **แถวการปรับปรุงการปัดเศษ** – รหัสแถวสำหรับแถวที่ควรถูกปรับปรุงเพื่อปรับดุลแก่งบดุล
    - **แถวสินทรัพย์รวม** – รหัสแถวสำหรับแถวในงบดุลที่ประกอบด้วยสินทรัพย์รวม
    - **แถวหนี้สินและส่วนของผู้ถือหุ้นรวม** – รหัสแถวสำหรับแถวในงบดุลที่ประกอบด้วยหนี้สินและส่วนของผู้ถือหุ้นรวม
    - **ขีดจำกัดยอดเงินการปรับปรุง** – จำนวนเต็มบวกที่ระบุขีดจำกัดในการปรับปรุงโดยอัตโนมัติ ยอดเงินนี้จะถูกเปรียบเทียบกับค่าจำนวนเต็มของค่าเบี่ยงเบนจากการปัดเศษที่แท้จริง

    > [!NOTE]
    > รหัสแถวเหล่านี้ต้องเชื่อมโยงกับข้อมูลการเงินของคุณ หรืออีกนัยหนึ่งคือ แถวต้องมีค่ามิติในเซลล์ **ลิงก์ไปยังมิติทางการเงิน** . **อย่า** อ้างอิงคำอธิบาย (**DESC**), คำนวณ (**CALC**), หรือรวมแถว (**TOT**)

ขณะนี้ยอดเงินในงบดุลของคุณจะสมดุลอย่างสม่ำเสมอเมื่อการปัดเศษเปิดใช้งานอยู่

> [!NOTE]
> ขีดจำกัดการปรับปรุงจะถูกปรับใช้ตามตัวเลือก **ความแม่นยำในการปัดเศษ** ที่ระบุสำหรับข้อกำหนดของรายงาน ตัวอย่างเช่น ถ้าคุณปัดเศษรายงานของคุณเป็นหน่วยพัน และป้อน **2** ในฟิลด์ **ขีดจำกัดยอดเงินการปรับปรุง** คุณจะได้รับข้อความแจ้งเตือนเมื่อค่าในฟิลด์ **แถวการปรับปรุงการปัดเศษ** เพิ่มหรือลดมากกว่า $2000

## <a name="format-row-and-column-text"></a>จัดรูปแบบข้อความแถวและคอลัมน์
คุณสามารถเลือกกำหนดรูปลักษณ์ของรายงานของคุณ โดยการเปลี่ยนแบบอักษร และการจัดรูปแบบข้อความ ส่วนต่อไปนี้จะอธิบายวิธีการจัดรูปแบบลักษณะของแถวและคอลัมน์ในรายงาน

### <a name="manage-font-styles"></a>จัดการลักษณะตัวอักษร

คุณสามารถสร้างและปรับเปลี่ยนลักษณะแบบอักษรสำหรับรายงานของคุณ จากนั้นคุณสามารถใช้ลักษณะเหล่านั้นกับเอกสาร หรือกับแถวหรือคอลัมน์ที่เฉพาะเจาะจงบนรายงาน

<table>
<tbody>
<tr>
<td><strong>สร้างลักษณะตัวอักษร</strong></td>
<td>
<ol>
<li>ใน Report Designer บนเมนู <strong>รูปแบบ</strong> คลิก <strong>ลักษณะและการจัดรูปแบบ</strong></li>
<li>ในกล่องโต้ตอบ <strong>ลักษณะและการจัดรูปแบบ</strong> คลิก <strong>สร้าง</strong> จากนั้นจึงป้อนชื่อเฉพาะสำหรับลักษณะใหม่</li>
<li>ทำการเลือกตัวอักษรของคุณ แล้วจึงคลิก <strong>ตกลง</strong></li>
</ol>
</td>
</tr>
<tr>
<td><strong>แก้ไขลักษณะแบบอักษร</strong></td>
<td>
<ol>
<li>ใน Report Designer บนเมนู <strong>รูปแบบ</strong> คลิก <strong>ลักษณะและการจัดรูปแบบ</strong></li>
<li>ในกล่องโต้ตอบ <strong>ลักษณะและการจัดรูปแบบ</strong> เลือกลักษณะเพื่อแก้ไข แล้วจึงคลิก <strong>ปรับเปลี่ยน</strong></li>
<li>ทำการเลือกตัวอักษรของคุณ แล้วจึงคลิก <strong>ตกลง</strong></li>
</ol>
</td>
</tr>
<tr>
<td><strong>ใช้ลักษณะตัวอักษร</strong></td>
<td>
<ol>
<li>ใน Report Designer ในคำนิยามหรือคำนิยามคอลัมน์ หรือในส่วนหัวและส่วนท้าย เลือกตั้งแต่หนึ่งเซลล์แถวขึ้นไป</li>
<li>ในรายการบนแถบเครื่องมือ <strong>ลักษณะ</strong> เลือกลักษณะตัวอักษร</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>จัดรูปแบบข้อความแถว

การจัดรูปแบบที่ระบุไว้ในแถวคำนิยามแทนการจัดรูปแบบที่ระบุในคำนิยามคอลัมน์และข้อกำหนดของรายงาน คุณสามารถปรับเปลี่ยนรูปแบบข้อความได้โดยใช้ตัวควบคุมต่างๆ บนแถบเครื่องมือการจัดรูปแบบ ตัวควบคุมเหล่านี้เป็นตัวควบคุม Microsoft Windows มาตรฐาน

1. ใน Report Designer เปิดคำนิยามแถวเพื่อแก้ไข
2. เลือกเซลล์เพื่อจัดรูปแบบ หากต้องการเลือกหลายๆ เซลล์ ให้กดปุ่ม Ctrl ค้างไว้ในขณะที่คุณเลือกเซลล์
3. คลิกปุ่มแถบเครื่องมือของรูปแบบที่ต้องการเพื่อนำไปใช้ ตัวอย่างเช่น ในแถวที่ย่อหน้า เลือกแถว แล้วจึงคลิก **เพิ่มระยะย่อหน้า** ![เพิ่มระยะย่อหน้า](media/indent.gif "เพิ่มระยะย่อหน้า") บนแถบเครื่องมือ

### <a name="adjust-columns-while-you-design-reports"></a>ปรับปรุงคอลัมน์ในขณะที่คุณออกแบบรายงาน

หากต้องการให้การดูคอลัมน์ที่คุณกำลังทำงานอยู่ในคำนิยามแถวง่ายขึ้น คุณสามารถปรับปรุงความกว้างของคอลัมน์และยังสามารถซ่อน (ย่อเล็กสุด) หรือแสดงคอลัมน์ในบานหน้าต่างมุมมองได้ การปรับเปลี่ยนที่คุณทำมีผลกระทบต่อลักษณะของคอลัมน์ที่ปรากฏบนหน้าจอเท่านั้น จะไม่มีผลกับการจัดรูปแบบคอลัมน์ในรายงาน

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>เปลี่ยนความกว้างของคอลัมน์ในบานหน้าต่างมุมมอง

1. ใน Report Designer เปิดคำนิยามแถวเพื่อแก้ไข
2. ในเมนู **รูปแบบ** เลือก **ความกว้างของคอลัมน์**
3. ในกล่องโต้ตอบ **ความกว้างของคอลัมน์** ป้อนค่าและจากนั้น คลิก **ตกลง** หรือกคุณสามารถลากขอบขวาของเซลล์ส่วนหัวของคอลัมน์เพื่อเปลี่ยนความกว้างของคอลัมน์

### <a name="hide-columns-in-the-view-pane"></a>ซ่อนคอลัมน์ในบานหน้าต่างมุมมอง

1. ใน Report Designer เปิดคำนิยามแถวเพื่อแก้ไข
2. เลือกคอลัมน์อย่างน้อยหนึ่งคอลัมน์เพื่อย่อขนาด
3. คลิกขวา แล้วจึงคลิก **ซ่อน**

### <a name="show-all-hidden-columns-in-the-view-pane"></a>แสดงคอลัมน์ที่ซ่อนอยู่ทั้งหมดในบานหน้าต่างมุมมอง

1. ใน Report Designer เปิดคำนิยามแถวเพื่อแก้ไข
2. คลิกขวาที่คอลัมน์ที่ถูกย่อเพื่อให้แสดงผล แล้วจึงคลิก **ยกเลิกซ่อน**


## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การรายงานทางการเงิน](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
