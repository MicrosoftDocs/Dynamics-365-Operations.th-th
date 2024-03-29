---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2 - การแม็ปแบบจำลอง)
description: บทความนี้อธิบายวิธีการตั้งค่าคอนฟิกแบบโมเดลการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลของรายงาน ER (ส่วนที่ 2)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 0d2daedd38c93ff17ef39780140c9c28ece82736
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290828"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a>ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2 - การแม็ปแบบจำลอง)

[!include [banner](../../includes/banner.md)]

ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER  สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ 

เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1: แบบจำลองข้อมูล)"


## <a name="add-required-data-sources-to-model-mapping"></a>เพิ่มแหล่งข้อมูลที่จำเป็นไปยังการแม็ปแบบจำลอง
1. ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก
2. ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'
3. คลิก ตัวออกแบบ
4. คลิก แม็ปแบบจำลองกับแหล่งข้อมูล
5. คลิก สร้าง
6. ในฟิลด์คำนิยาม ให้เลือก รายการ
7. ในฟิลด์ ชื่อ ให้พิมพ์ 'การแม็ปข้อมูลมิติ'
8. ในฟิลด์คำนิยาม ให้พิมพ์ 'การแม็ปข้อมูลมิติ'
9. คลิก บันทึก
10. คลิก ตัวออกแบบ
11. ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\ตาราง'
12. คลิก เพิ่มราก
13. ในฟิลด์ชื่อ พิมพ์ 'บริษัท'
14. ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'
15. คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน
16. ในแผนภูมิ เลือก 'ฟังก์ชัน\รายละเอียดมิติทางการเงิน'
17. คลิก เพิ่มราก
    * แหล่งข้อมูลนี้ระบุว่าจะกำหนดขอบเขตของมิติทางการเงินสำหรับรายงานใดๆ ที่จะใช้แบบจำลองนี้เป็นแหล่งข้อมูลอย่างไร  
18. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
19. เลือก ใช่ ในฟิลด์ขอข้อมูลมิติ
    * เลือกใช่เพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติในเวลาที่ใช้ในการผลิตในแบบฟอร์มกล่องโต้ตอบผู้ใช้  ถ้าตั้งค่าเป็นไม่ มิติทางการเงินทั้งหมดของอินสแตนซ์ปัจจุบันจะถูกใช้โดยค่าเริ่มต้น  
20. ในฟิลด์การเลือกมิติทางการเงิน เลือก 'นิติบุคคล'
    * เลือกทั้งหมดเพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติที่ต้องการสำหรับอินสแตนซ์ปัจจุบันในฟิลด์การค้นหา   เลือกนิติบุคคลที่จะอนุญาตให้ผู้ใช้สามารถเลือกมิติสำหรับบริษัทในฟิลด์การค้นหา   เลือกมิติเพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติโดยใช้ชุดมิติเดียว  
21. เลือก ใช่ ในฟิลด์ขอข้อมูลบัญชีหลัก
    * ตั้งค่า 'ขอข้อมูลบัญชีหลัก' เป็น 'ใช่' เพื่ออนุญาตให้ผู้ใช้สามารถเลือกบัญชีหลักเป็นส่วนหนึ่งของรายการของมิติ   ถ้าตั้งค่าเป็น ไม่ บัญชีหลักจะไม่ถูกรวมเข้าในรายการของมิติ และตัวเลือก 'บัญชีหลักเป็นข้อมูลบังคับ' จะถูกเปิดใช้งาน ถ้า 'บัญชีหลักเป็นข้อมูลบังคับ' ถูกตั้งค่าเป็น ใช่ ให้รวมบัญชีหลักในรายการของมิติโดยไม่คำนึงถึงการเลือกของผู้ใช้  
22. คลิก ตกลง 
![Slide out ของคุณสมบัติแหล่งข้อมูลรายละเอียดของมิติทางการเงิน](../media/er-financial-dimensions-guides-model-mapping1.png)
23. ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\เรกคอร์ดตาราง'
24. คลิก เพิ่มราก
25. ในฟิลด์ชื่อ ให้พิมพ์ 'LedgerJournal'
26. เลือก ใช่ในการขอฟิลด์การสอบถาม
27. ในฟิลด์ตาราง พิมพ์ 'LedgerJournalTable'
28. คลิก ตกลง 
![<หน้าตัวออกแบบการแม็ปแบบจำลอง ชนิดแหล่งข้อมูลของเรกคอร์ดตาราง](../media/er-financial-dimensions-guides-model-mapping2.png)

## <a name="map-data-model-elements-to-added-data-sources"></a>แม็ปองค์ประกอบแบบจำลองข้อมูลไปยังแหล่งข้อมูลที่เพิ่ม
1. ในแผนภูมิ ให้ขยาย 'สมุดบัญชี'
2. ในแผนภูมิ ให้ขยาย 'สมุดรายวัน\ธุรกรรม'
3. ในแผนภูมิ ให้ขยาย 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ'
4. ในแผนภูมิ ขยาย 'การตั้งค่ามิติ'
5. ในแผนภูมิ ขยาย 'LedgerJournal'
6. ในแผนภูมิ ขยาย 'LedgerJournal\<Relations'
7. ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans'
8. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'
9. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ใบสำคัญ'
10. คลิก ผูก
11. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'
    * โปรดทราบว่าสำหรับการอ้างอิงใดๆ ของมิติทางการเงินที่ตั้งค่าเป็น ตัวอย่างเช่น LedgerDimension รายการแหล่งข้อมูลที่เกี่ยวข้องจะพร้อมใช้งาน (LedgerDimension.Dimension)  รายการแหล่งข้อมูลนี้เสนอให้ตั้งค่ามิติทางการเงินของมิตินั้นเป็นรายการของเรกคอร์ด  
12. ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'
13. ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ'
14. ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า'
15. ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\การกำหนด'
16. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\การกำหนด\ชื่อ'
17. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\ชื่อ'
18. คลิก ผูก
19. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า\คำอธิบาย'
20. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\คำอธิบาย'
21. คลิก ผูก
22. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า\รหัส'
23. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\รหัส'
24. คลิก ผูก
25. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ'
26. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ'
27. คลิก ผูก
!หน้าตัวออกแบบการแม็ปแบบจำลอง แท็บการแม็ป แผนภูมิแหล่งข้อมูล](../media/er-financial-dimensions-guides-model-mapping3.png)
28. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'
29. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\เดบิต'
30. คลิก ผูก
31. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'
32. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\วันที่'
33. คลิก ผูก
34. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'
35. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\สกุลเงิน'
36. คลิก ผูก
37. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'
38. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\เครดิต'
39. คลิก ผูก
40. ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans'
41. ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม'
42. คลิก ผูก
43. ในแผนภูมิ เลือก 'LedgerJournal\Journal batch number(JournalNum)'
44. ในแผนภูมิ เลือก 'สมุดรายวัน\ชุดงาน'
45. คลิก ผูก
46. ในแผนภูมิ ให้เลือก 'LedgerJournal'
47. ในแผนภูมิ ให้เลือก 'สมุดบัญชี'
48. คลิก ผูก
49. ในแผนภูมิ ขยาย 'มิติ'
50. ในแผนภูมิ ขยาย 'มิติ\บัญชีหลักและมิติ'
51. ในแผนภูมิ ขยาย 'มิติ\บัญชีหลักและมิติ'\การกำหนด'
52. ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'\การกำหนด\ชื่อ'
53. ในแผนภูมิ เลือก 'การตั้งค่ามิติ\รหัส'
54. คลิก ผูก
55. ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'\การกำหนด\ชื่อคอลัมน์รายงาน'
56. ในแผนภูมิ เลือก 'การตั้งค่ามิติ\ชื่อ'
57. คลิก ผูก
58. ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'
59. ในแผนภูมิ เลือก 'การตั้งค่ามิติ'
60. คลิก ผูก
61. ในแผนภูมิ ให้เลือก 'บริษัท'
62. คลิก แก้ไข
63. ในฟิลด์ expressionAsStringText ให้ป้อน 'Company.'find()'.'name()''
    * Company.'find()'.'name()'  
64. คลิก บันทึก
![หน้าตัวออกแบบการแม็ปแบบจำลอง ER](../media/er-financial-dimensions-guides-model-mapping4.png)
65. ปิดหน้า
66. คลิก บันทึก
67. ปิดหน้า

## <a name="complete-this-draft-models-version"></a>ทำรุ่นของแบบจำลองร่างนี้ให้เสร็จสมบูรณ์
1. ปิดหน้า
2. ปิดหน้า
3. คลิก เปลี่ยนแปลงสถานะ
4. คลิกเสร็จสมบูรณ์
5. คลิก ตกลง 
![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-model-mapping5.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
