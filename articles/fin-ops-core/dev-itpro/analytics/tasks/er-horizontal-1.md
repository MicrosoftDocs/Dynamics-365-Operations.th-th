---
title: ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 1 - ออกแบบรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์เวิร์กชีต OPENXML (Excel) (ส่วนที่ 1)
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab360c259af37ce3995d3cd2560bc2e765e0bceb
ms.sourcegitcommit: e3290eb58ae569a59d6ae2e6922e7d8be8f1980f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2021
ms.locfileid: "7551787"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 1 - ออกแบบรูปแบบ)

[!include [banner](../../includes/banner.md)]

ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน  สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ 

เพื่อทำตามขั้นตอนเหล่านี้ ก่อนอื่นคุณต้องดำเนินการตามคำแนะนำงานสามรายการนี้:

"ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"

"ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1: ออกแบบแบบจำลองข้อมูล)"

"ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2: การแม็ปแบบจำลอง)"

นอกจากนี้ คุณยังต้องดาวน์โหลดและบันทึกสำเนาเฉพาะที่ของเท็มเพลตกับรายงานตัวอย่างที่พบที่นี่ [รายงานเว็บเซอร์วิสของมิติทางการเงินตัวอย่าง](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx)

กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611

## <a name="create-a-new-report-configuration"></a>สร้างการตั้งค่าคอนฟิกรายงานใหม่

1. ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก
2. ในแผนภูมิ ให้เลือก `Financial dimensions sample model`
3. คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง
4. ในฟิลด์ ใหม่ ป้อน `Format based on data model Financial dimensions sample model`
    * ใช้แบบจำลองที่สร้างขึ้นล่วงหน้าเป็นแหล่งข้อมูลสำหรับรายงานใหม่ของคุณ  
5. ในฟิลด์ชื่อ ให้พิมพ์ `Sample report with horizontally expandable ranges`
    * ตัวอย่างรายงานที่มีช่วงที่สามารถขยายได้ในแนวนอน  
6. ในฟิลด์ คำอธิบาย ให้พิมพ์ `To make Excel output with dynamically adding columns`
    * เพื่อสร้างผลลัพธ์ Excel ด้วยการเพิ่มคอลัมน์แบบไดนามิก  
7. ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้เลือก รายการ
8. คลิก สร้างการตั้งค่าคอนฟิก

## <a name="design-the-report-format"></a>ออกแบบรูปแบบรายงาน

1. คลิก ตัวออกแบบ
2. เปิดใช้งานปุ่มสลับ `Show details`
3. ในบานหน้าต่างการดำเนินการ คลิกนำเข้า
4. คลิกนำเข้าจาก Excel
5. คลิกสิ่งที่แนบ
    * นำเข้าเท็มเพลตของรายงาน ใช้ไฟล์ Excel ที่คุณดาวน์โหลดมา  
6. คลิก สร้าง
7. คลิกไฟล์
8. ปิดหน้า
9. ในฟิลด์เท็มเพลต ให้ป้อนหรือเลือกค่า
    * เลือกเท็มเพลตที่ดาวน์โหลด  
10. คลิก ตกลง
    * เพิ่มช่วงใหม่เพื่อสร้างแบบผลลัพธ์ Excel แบบไดนามิกด้วยจำนวนคอลัมน์ที่มากเท่ากับที่คุณเลือก (ในแบบฟอร์มกล่องโต้ตอบผู้ใช้) สำหรับมิติทางการเงิน  แต่ละเซลล์สำหรับทุกคอลัมน์จะแสดงถึงชื่อของมิติทางการเงินเดียว  
11. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
12. ในแผนภูมิ ให้เลือก `Excel\Range`
13. ในฟิลด์ช่วง Excel พิมพ์ `DimNames`
    * DimNames  
14. ในฟิลด์ทิศทางการจำลอง ให้เลือก `Horizontal`
15. คลิก ตกลง 
16. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`
17. คลิกเลื่อนขึ้น
18. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Cell<DimNames>`
19. คลิก ตัด
20. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`
21. คลิก วาง
22. ในแผนภูมิ ให้ขยาย `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`
23. ในแผนภูมิ ให้ขยาย `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`
24. ในแผนภูมิ ให้ขยาย `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`
25. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`
    * เพิ่มช่วงใหม่เพื่อสร้างแบบผลลัพธ์ Excel แบบไดนามิกด้วยจำนวนคอลัมน์ที่มากเท่ากับที่คุณเลือก (ในแบบฟอร์มกล่องโต้ตอบผู้ใช้) สำหรับมิติทางการเงิน  แต่ละเซลล์สำหรับทุกคอลัมน์จะแสดงถึงค่าของมิติทางการเงินเดียวสำหรับธุรกรรมการรายงานแต่ละรายการ  
26. คลิก เพิ่มช่วง
27. ในฟิลด์ช่วง Excel พิมพ์ `DimValues`
    * DimValues  
28. ในฟิลด์ทิศทางการจำลอง ให้เลือก `Horizontal`
29. คลิก ตกลง 
30. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>`
31. คลิก ตัด
32. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`
33. คลิก วาง
34. ในแผนภูมิ ให้ขยาย `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`

## <a name="map-format-elements-to-data-sources"></a>แม็ปองค์ประกอบของรูปแบบไปยังแหล่งข้อมูล

1. คลิกแท็บ การแม็ป
2. ในแผนภูมิ ให้ขยาย `model: Data model Financial dimensions sample model`
3. ในแผนภูมิ ให้ขยาย `model: Data model Financial dimensions sample model\Journal: Record list`
4. ในแผนภูมิ ให้ขยาย `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`
5. ในแผนภูมิ ให้ขยาย `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`
6. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>`
7. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String`
8. คลิก ผูก
9. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`
10. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`
11. คลิก ผูก
12. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>`
13. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real`
14. คลิก ผูก
15. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>`
16. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real`
17. คลิก ผูก
18. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>`
19. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String`
20. คลิก ผูก
21. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>`
22. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date`
23. คลิก ผูก
24. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>`
25. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String`
26. คลิก ผูก
27. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>`
28. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`
29. คลิก ผูก
30. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`
31. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`
32. คลิก ผูก
33. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>`
34. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`
35. คลิก ผูก
36. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`
37. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Journal: Record list`
38. คลิก ผูก
39. ในแผนภูมิ ให้ขยาย `model: Data model Financial dimensions sample model\Dimensions setting: Record list`
40. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String`
41. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>`
42. คลิก ผูก
43. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Dimensions setting: Record list`
44. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`
45. คลิก ผูก
46. ในแผนภูมิ ให้เลือก `Excel = "SampleFinDimWsReport"\Cell<CompanyName>`
47. ในแผนภูมิ ให้เลือก `model: Data model Financial dimensions sample model\Company: String`
48. คลิก ผูก
49. คลิก บันทึก
50. ปิดหน้า

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
