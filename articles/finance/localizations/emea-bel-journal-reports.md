---
title: รายงานสมุดรายวัน
description: บทความนี้อธิบายวิธีการใช้งานรายงานสมุดรายวันที่เกี่ยวข้องกับนิติบุคคลที่มีที่อยู่หลักในเบลเยียมโดยเฉพาะ
author: AdamTrukawka
ms.date: 04/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Thailand
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 265924
ms.assetid: 829a101f-e329-48b9-baf8-e36670ff43c8
ms.search.form: TaxTable, VendParameters, CustParameters
ms.openlocfilehash: ee1ce721878013cf7e802559f31c64f4eb03deb6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275900"
---
# <a name="journal-reports-posting-journals"></a>รายงานสมุดรายวัน (การลงรายการบัญชีสมุดรายวัน)

[!include [banner](../includes/banner.md)]

บริษัทเบลเยียมต้องพิมพ์รายงานของแต่ละสมุดรายวันเป็นระยะ รายงานจะแสดงรายการการลงรายการบัญชีทั้งหมดตามลำดับเวลาในบัญชีแยกประเภททั่วไปของแต่ละสมุดรายวัน รายงานเหล่านี้จะพิสูจน์ความถูกต้องของรายการบัญชีและใช้ในการตรวจสอบการเงินเพื่อกระทบยอดการชําระเงิน VAT กับการลงรายการบัญชีในบัญชีแยกประเภททั่วไปที่เกี่ยวข้อง

คุณสามารถสร้างรายงานได้ห้าชนิด

   - **สมุดรายวันการซื้อ**: แสดงภาพรวมของการซื้อทั้งหมด
   - **สมุดรายวันการขาย**: แสดงภาพรวมของการขายทั้งหมด
   - **สมุดรายวันทางการเงิน**: แสดงภาพรวมของรายการทางการเงินทั้งหมด
   - **สมุดรายวันอื่น**: แสดงภาพรวมของการดําเนินงานที่หลากหลายทั้งหมด
   - **ภาพรวมสมุดรายวัน**: แสดงภาพรวมของสมุดรายวันที่พิมพ์ทั้งหมด

รายงานเหล่านี้สามารถใช้ได้เฉพาะกับนิติบุคคลที่มีที่อยู่หลักอยู่ในเบลเยียมเท่านั้น

แต่ละรายงานจะประกอบด้วยส่วนและสรุปต่าง ๆ ดังนี้

   - ภาพรวมโดยละเอียดของการลงรายการบัญชีในบัญชีแยกประเภททั่วไป
   - สรุปของการลงรายการบัญชีในบัญชีแยกประเภททั่วไป
   - ภาพรวมโดยละเอียดของการลงรายการบัญชีภาษี
   - สรุปการลงรายการบัญชีภาษี
   - สรุปกล่องจํานวนเงินภาษีที่ใช้ในสมุดรายวันที่เลือก

คุณสามารถตั้งค่าพารามิเตอร์ต่อไปนี้เมื่อคุณสร้างรายงานได้

| **ฟิลด์** | **คำอธิบาย** |
|-------------------------|-------------------------|
| สมุดรายวัน | เลือกชื่อของสมุดรายวันการขายที่จะใช้ลงรายการบัญชีธุรกรรมที่บัญชีแยกประเภททั่วไป |
| วันที่เริ่มต้น | ให้เลือกหรือป้อนวันที่เริ่มต้นของรอบระยะเวลาการรายงาน |
| วันที่สิ้นสุด | ให้เลือกหรือป้อนวันที่สิ้นสุดของรอบระยะเวลาการรายงาน |
| เอกสารพิมพ์สุดท้าย | ตั้งค่าเป็น **ใช่** เพื่อพิมพ์รายงานรุ่นสุดท้าย</br>เมื่อคุณเลือก **เอกสารพิมพ์สุดท้าย** จะเกิดสิ่งต่อไปนี้</br><ol></br><li>**วันที่เริ่มต้น** ที่คุณเลือกต้องเป็นของรอบระยะเวลาที่ตามหลังรอบระยะเวลาของวันที่สิ้นสุดของเอกสารพิมพ์สุดท้าย การตรวจสอบความถูกต้องนี้จะขึ้นอยู่กับค่าที่ป้อนไว้ในฟิลด์ **สมุดรายวัน** ถ้าฟิลด์นี้ว่าง สมุดรายวันการลงรายการบัญชีทั้งหมดที่เป็นของชนิดนี้ (การซื้อ การขาย ทางการเงิน หรืออื่น ๆ) จะมีการตรวจสอบความถูกต้อง</li></br><li>หมายเลขหน้าของรายงานเป็นลำดับ หมายเลขหน้าของรอบระยะเวลาก่อนหน้านี้ +1 จะใช้เป็นข้อมูลพื้นฐานใหม่ในการระบุหมายเลข การระบุหมายเลขหน้าเริ่มต้นเป็นศูนย์สำหรับแต่ละปีบัญชี</li></br><li>รายการใหม่จะถูกเพิ่มในฟอร์มเอกสารพิมพ์สุดท้ายสำหรับแต่ละสมุดรายวันการลงรายการบัญชี</li></br></ol> |
| บีบอัด | เลือกตัวเลือกนี้เพื่อจัดกลุ่มยอดเงินในบัญชีแยกประเภทเดียวกันในใบสำคัญเดียวกันเป็นรายการเดียว</br><ul></br><li>เมื่อตั้งค่าเป็ฯ **ไม่** แต่ละธุรกรรมจะแสดงขึ้นบนรายการแยกต่างหาก</li></br><li>เมื่อตั้งค่าเป็น **ใช่** ธุรกรรมจะถูกจัดกลุ่มตามบัญชีและแสดงเป็นรายการสรุปรายการเดียว</li></br></ul> |


## <a name="setup"></a>ตั้งค่า

รายงานจะเชื่อมโยงกับสมุดรายวันการลงบัญชีในบัญชีแยกประเภททั่วไปตามลำดับหมายเลข สำหรับแต่ละสมุดรายวันการลงรายการบัญชี เลือกชนิดสมุดรายวัน การซื้อ การขาย อื่น ๆ หรือทางการเงิน หรือคุณสามารถปล่อยฟิลด์นี้ว่างไว้ได้

1. ไปที่ **บัญชีแยกประเภททั่วไป** > **การตั้งค่าสมุดรายวัน** > **สมุดรายวันการลงรายการบัญชี**
2. ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างสมุดรายวันการลงรายการบัญชีโดยอัตโนมัติ สมุดรายวันการลงบัญชีจะถูกสร้างขึ้นเพื่อให้สอดคล้องกับรหัสลำดับหมายเลข หากต้องการสร้างสมุดรายวันการลงบัญชีด้วยตนเอง เลือก **ใหม่**
3. เลือกสมุดรายวันการลงรายการบัญชีและในส่วน **รายงานสมุดรายวันภาษาเบลเยียม** ในฟิลด์ **ชนิดสมุดรายวัน** ให้เลือกชนิดสมุดรายวัน
4. ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **กลุ่มภาษีขายตามประเภทสินค้า**
5. เลือกกลุ่มภาษีขายตามประเภทสินค้า และในฟิลด์ **ชนิดการรายงาน** ให้เลือกว่าจํานวนเงินของรายการภาษีขายตามประเภทสินค้าจะรวมอยู่ในรายการขายในสหภาพยุโรป (EU) ที่ใด

    - **ว่างเปล่า**: ยอดเงินรายการภาษีขายรวมอยู่ในคอลัมน์ **ไม่ถูกกำหนด**
    - **สินค้า**: ยอดเงินรายการภาษีขายรวมอยู่ในคอลัมน์ **สินค้า**
    - **บริการ**: ยอดเงินรายการภาษีขายรวมอยู่ในคอลัมน์ **บริการ**
    - **การลงทุน**: ยอดเงินรายการภาษีขายรวมอยู่ในคอลัมน์ **การลงทุน**

## <a name="sales-journals-report"></a>รายงานสมุดรายวันการขาย

รายงานน **สมุดรายวันการขาย** แสดงและพิมพ์สรุปธุรกรรมการขาย เช่น ใบแจ้งหนี้การขาย และใบลดหนี้ ที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป รายงานนี้จะสรุปสิ่งต่อไปนี้:

   - ธุรกรรมการจ่ายต่อใบสำคัญและบัญชีแยกประเภททั่วไป
   - เดบิตและเครดิตโดยรวมต่อบัญชีแยกประเภททั่วไป
   - รายละเอียดภาษีต่อรหัสภาษีและหมายเลขใบสำคัญ รวมทั้งยอดเงินฐานภาษีและการกระจายยอดเงินภาษีโดยเทียบกับสินค้า บริการ และการลงทุน
   - รายการของการลงรายการบัญชีภาษีโดยเรียงลำดับตามรหัสการรายงานภาษีที่ตรงกัน

โดยทั่วไป รายงานนี้จะใช้โดยตัวแทนเรียกเก็บเงิน ผู้จัดการการเรียกเก็บเงิน ประธานเจ้าหน้าที่ฝ่ายการเงิน เจ้าหน้าที่บัญชีลูกหนี้ ผู้จัดการบัญชีลูกหนี้ ผู้ควบคุมการเงิน และผู้ควบคุมการเงิน เพื่อทบทวนสถานะของใบแจ้งหนี้และกระบวนการเงินสด

ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันการขาย** และตั้งค่าพารามิเตอร์เพื่อสร้างรายงาน

## <a name="purchase-journals-report"></a>รายงานสมุดรายวันการซื้อ

รายงาน **สมุดรายวันการซื้อ** แสดงและพิมพ์สรุปของธุรกรรมในสมุดรายวันการซื้อ โดยทั่วไป รายงานนี้จะใช้โดยผู้ประสานงานบัญชีเจ้าหนี้และผู้จัดทำบัญชี

ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันการซื้อ** และตั้งค่าพารามิเตอร์เพื่อสร้างรายงาน

## <a name="financial-journal-report"></a>รายงานสมุดรายวันทางการเงิน

รายงานน **สมุดรายวันทางการเงิน** แสดงและพิมพ์สรุปธุรกรรมทางการเงิน เช่น การชำระเงินของลูกค้า และการชำระเงินของผู้จัดจำหน่าย ที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป รายงานนี้จะสรุปสิ่งต่อไปนี้:

   - ธุรกรรมการจ่ายต่อใบสำคัญและบัญชีแยกประเภททั่วไป
   - เดบิตและเครดิตโดยรวมต่อบัญชีแยกประเภททั่วไป
   - รายละเอียดภาษีต่อรหัสภาษีและหมายเลขใบสำคัญ รวมทั้งยอดเงินฐานภาษีและการกระจายยอดเงินภาษีโดยเทียบกับสินค้า บริการ และการลงทุน
   - รายการของการลงรายการบัญชีภาษีโดยเรียงลำดับตามรหัสการรายงานภาษีที่ตรงกัน

โดยทั่วไป รายงานนี้จะใช้โดยประธานเจ้าหน้าที่บริหาร ประธานเจ้าหน้าที่ฝ่ายการเงิน ผู้จัดการฝ่ายการปฏิบัติตามกฎระเบียบ ผู้จัดการฝ่ายบัญชี ผู้ควบคุมงานบัญชี และผู้ควบคุมการเงิน เพื่อทบทวนสถานะของกระบวนการบัญชีแยกประเภททั่วไป

ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันทางการเงิน** และตั้งค่าพารามิเตอร์เพื่อสร้างรายงาน

## <a name="other-journal-report"></a>รายงานสมุดรายวันอื่นๆ

รายงาน **สมุดรายวันอื่น ๆ** จะแสดงและพิมพ์สรุปของธุรกรรมที่ลงรายการบัญชีแล้ว ซึ่งไม่ได้จัดประเภทภายใต้การขาย การซื้อ หรือทางการเงิน โดยทั่วไป รายงานนี้จะใช้โดยผู้บัญชี ผู้จัดการฝ่ายบัญชี เสมียน ผู้ควบคุมงานบัญชี และผู้จัดการฝ่ายการปฏิบัติตามกฎระเบียบ เพื่อสอบถามเกี่ยวกับธุรกรรมสมุดรายวัน

ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันอื่น** และตั้งค่าพารามิเตอร์เพื่อสร้างรายงาน

## <a name="overview-journal-report"></a>ภาพรวมรายงานสมุดรายวัน

รายงาน **สมุดรายวันภาพรวม** จะแสดงและพิมพ์สรุปของธุรกรรมที่ลงรายการบัญชีแล้ว ซึ่งไม่ได้จัดประเภทภายใต้การขาย การซื้อ หรือทางการเงิน

โดยทั่วไป รายงานนี้จะใช้โดยผู้บัญชี ผู้จัดการฝ่ายบัญชี เสมียน ผู้ควบคุมงานบัญชี และผู้จัดการฝ่ายการปฏิบัติตามกฎระเบียบ เพื่อสอบถามเกี่ยวกับธุรกรรมสมุดรายวัน

## <a name="example"></a>ตัวอย่าง

ตัวอย่างต่อไปนี้แสดงวิธีที่คุณสามารถตั้งค่าการลงรายการบัญชีสมุดรายวัน และสร้างและพิมพ์รายงานสมุดรายวันการลงรายการบัญชี ตัวอย่างนี้ใช้นิติบุคคล FRRT

1. ไปที่ **การจัดการองค์กร** > **องค์กร**> **นิติบุคคล** และเลือกนิติบุคคล FRRT
2. บนแท็บด่วน **ที่อยู่** ให้เลือก **แก้ไข** ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก BEL (เบลเยียม)
3. ไปที่ **บัญชีแยกประเภททั่วไป** > **การตั้งค่าสมุดรายวัน** > **สมุดรายวันการลงรายการบัญชี**
4. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง**
5. ตั้งค่า **ชนิดสมุดรายวัน** ของสมุดรายวันตามตารางต่อไปนี้

    | **สมุดรายวัน** | **ชนิดสมุดรายวัน** |
    |-------------------------|-------------------------|
    | Acco_46 | ใบสั่งขาย |
    | Acco_67 | การซื้อ |
    | JourNdF | การเงิน |
    | ODComptabl | อื่นๆ |

6. ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **กลุ่มภาษีขายตามประเภทสินค้า**
7. เลือกกลุ่มภาษีขายตามประเภทสินค้า **ปกติ** และในฟิลด์ **ชนิดการรายงาน** ให้เลือก **สินค้า**
8. ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **หน่วยงานจัดเก็บภาษีขาย**
9. เลือก **TAXFRA** และบนแท็บด่วน **ทั่วไป** ในฟิลด์ **โครงร่างรายงาน** เลือก **โครงร่างรายงานเบลเยียม**
10. ไปที่ **ภาษี** > **การตั้งค่า** > **ภาษีขาย** > **รหัสการรายงานภาษีขาย** และสร้างรหัสการรายงานต่อไปนี้

    | **โครงร่างรายงาน** | **รหัสการรายงาน** | **ข้อความในรายงาน** |
    |-------------------------|-------------------------|-------------------------|
    | โครงร่างรายงานเบลเยียม | 03 | ภาษีวัสดุและบริการที่คิดภาษีในอัตราภาษีขาย 21 เปอร์เซ็นต์</br>การจัดส่งธุรกรรมผลิตภัณฑ์หรือการบริการที่อัตราภาษีขาย 21 เปอร์เซ็นต์ |
    | โครงร่างรายงานเบลเยียม | 54 | VAT ที่ค้างจ่ายในอัตราหมุนเวียนที่รวมอยู่ในรหัส **01** **02** และ **03** |
    | โครงร่างรายงานเบลเยียม | 81 | ยอดเงินของการซื้อสินค้า วัตถุดิบ และต้นทุนการซื้อวัสดุทั้งหมด และต้นทุนการซื้อที่เกี่ยวข้อง ไม่รวม VAT ที่สามารถหักได้ |
    | โครงร่างรายงานเบลเยียม | 59 | จำนวนของ VAT ที่ไม่สามารถหักลดได้ |


    สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่ารหัสการรายงานภาษีขาย](./emea-bel-intervat-tax-declaration.md#set-up-sales-tax-reporting-codes)

11. ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **รหัสภาษีขาย**
12. เลือก **INA19.6** และบนแท็บด่วน **การตั้งค่ารายงาน** ในส่วน **การขาย** ให้เลือกสิ่งต่อไปนี้

     - ในฟิลด์ **การขายที่ต้องเสียภาษี** เลือก 03
     - ในฟิลด์ **เจ้าหนี้ภาษีขาย** เลือก 54

13. ในส่วน **การซื้อ** ให้เลือกสิ่งต่อไปนี้:

    - ในฟิลด์ **ภาษีซื้อ** เลือก 81
    - ใน **ลูกหนี้ภาษีขาย** เลือก 59

### <a name="print-the-sales-journal-report"></a>พิมพ์รายงานสมุดรายวันการขาย

เมื่อต้องการพิมพ์รายงาน **สมุดรายวันการขาย** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

1. ไปที่ **บัญชีลูกหนี้** > **ใบแจ้งหนี้** > **ใบแจ้งหนี้ข้อความอิสระทั้งหมด**
2. เลือก **สร้าง** และสร้างใบแจ้งหนี้ข้อความอิสระใหม่ด้วยข้อมูลต่อไปนี้

    - ในฟิลด์ **บัญชี** **ลูกค้า** เลือก US-1001
    - ใน **ฟิลด์วันที่** เลือก 4/15/2021
    - บนแท็บ **บรรทัดใบแจ้งหนี้** ในฟิลด์ **บัญชีหลัก** ให้เลือก **701000**
    - ในฟิลด์ **กลุ่มภาษีขาย** ให้เลือก VE-DOM
    - ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** เลือก ปกติ
    - ในฟิลด์ **คุณภาพ** ป้อน 1
    - ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อน 100

3. ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ
4. ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันการขาย**
5. ในส่วน **เงื่อนไข** ในฟิลด์ **สมุดรายวัน** ให้เลือก Acco\_46
6. ในฟิลด์ **วันที่เริ่มต้น** เลือก 4/1/2021
7. ในฟิลด์ **วันที่สิ้นสุด** เลือก 4/30/2021
8. ในฟิลด์ **เอกสารพิมพ์สุดท้าย** เลือก **ใช่** เลือก **ตกลง** เพื่อตรวจทานรายงาน

    ![รายงานสมุดรายวันการขาย](media/emea-bel-journal-reports-sales-journal-report.png)

### <a name="print-the-purchase-journal-report"></a>พิมพ์รายงานสมุดรายวันการซื้อ

เมื่อต้องการพิมพ์รายงาน **สมุดรายวันการซื้อ** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

1. ไปที่ **บัญชีเจ้าหนี้** &gt; **ใบสั่งซื้อ** &gt; **ใบสั่งซื้อทั้งหมด**
2. เลือก **สร้าง** และสร้างใบสั่งซื้อใหม่ด้วยข้อมูลต่อไปนี้

    - ในฟิลด์ **บัญชีผู้จัดจำหน่าย** เลือก **1001**
    - ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **0001**
    - ในฟิลด์ **คุณภาพ** ป้อน 3
    - บนแท็บด่วน **รายละเอียดรายการ** บนแท็บ **การตั้งค่า** ในส่วน **ภาษีขาย** ใน **กลุ่มภาษีขายตามประเภทสินค้า** ให้เลือก **ปกติ** ใน **กลุ่มภาษีขาย** ให้เลือก **VE-DOM**

3. ไปที่ **การซื้อ** > **การดำเนินการ** > **ยืนยัน**
4. ไปที่ **ใบแจ้งหนี้** > **สร้าง** > **ใบแจ้งหนี้**
5. ในส่วน **รหัสใบแจ้งหนี้** ในฟิลด์ **หมายเลข** ให้ป้อน INVNUM\_001
6. ในส่วน **วันที่ในใบแจ้งหนี้** ในฟิลด์ **วันที่ของใบแจ้งหนี้** ให้เลือก 4/12/2021
7. ในฟิลด์ **วันที่ลงรายการบัญชี** เลือก 4/12/2021
8. ลงรายการบัญชีใบสั่ง
9. ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันการซื้อ**
10. ในส่วน **เงื่อนไข** ในฟิลด์ **สมุดรายวัน** ให้เลือก **Acco\_67**
11. ในฟิลด์ **วันที่เริ่มต้น** เลือก 4/1/2021
12. ในฟิลด์ **วันที่สิ้นสุด** เลือก 4/30/2021
13. ในฟิลด์ **เอกสารพิมพ์สุดท้าย** เลือก **ใช่** เลือก **ตกลง** เพื่อดูรายงาน

![รายงานสมุดรายวันการซื้อหน้า 1](media/emea-bel-journal-reports-purchase-journal-report-1.png)
![รายงานสมุดรายวันการซื้อหน้า 2](media/emea-bel-journal-reports-purchase-journal-report-2.png)
![หน้ารายงานสมุดรายวันการซื้อ 3](media/emea-bel-journal-reports-purchase-journal-report-3.png)
![รายงานสมุดรายวันการซื้อหน้า 4](media/emea-bel-journal-reports-purchase-journal-report-4.png)

### <a name="print-the-financial-journal-report"></a>พิมพ์รายงานสมุดรายวันทางการเงิน

เมื่อต้องการพิมพ์รายงาน **สมุดรายวันทางการเงิน** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

1. ไปที่ **บัญชีแยกประเภททั่วไป** > **รายการสมุดรายวัน** > **สมุดรายวันทั่วไป**
2. สร้างสมุดรายวันใหม่ ในฟิลด์ **ชื่อ** ให้เลือก **JourNdF**
3. เลือก **รายการ** และป้อนข้อมูลต่อไปนี้:

    - ในฟิลด์ **วันที่** เลือก **4/15/2021**
    - ในฟิลด์ **ชนิดบัญชี** เลือก **ลูกค้า**
    - ในฟิลด์ **บัญชี** เลือก **1001**
    - ในฟิลด์ **เครดิต** ป้อน 100
    - ในฟิลด์ **ชนิดบัญชีตรงข้าม** เลือก **ธนาคาร**
    - ในฟิลด์ **บัญชีตรงข้าม** เลือก **FRRT OPER**
    - ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** เลือก **ปกติ**
    - ในฟิลด์ **กลุ่มภาษีขาย ให้เลือก** เลือก **VE-DOM**

4. ลงรายการบัญชีสมุดรายวัน
5. ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันทางการเงิน**
6. ในส่วน **เงื่อนไข** ในฟิลด์ **สมุดรายวัน** ให้เลือก **JourNdF**
7. ในฟิลด์ **วันที่เริ่มต้น** เลือก 4/1/2021
8. ในฟิลด์ **วันที่สิ้นสุด** เลือก 4/30/2021
9. ในฟิลด์ **เอกสารพิมพ์สุดท้าย** เลือก **ใช่** เลือก **ตกลง** เพื่อตรวจทานรายงาน

![รายงานสมุดรายวันทางการเงินหน้า 1](media/emea-bel-journal-reports-financial-journal-report.png)

![รายงานสมุดรายวันทางการเงินหน้า 2](media/emea-bel-journal-reports-financial-journal-report-2.png)

### <a name="print-the-other-journal-report"></a>พิมพ์รายงานสมุดรายวันอื่น

เมื่อต้องการพิมพ์รายงาน **สมุดรายวันอื่น** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

1. ไปที่ **บัญชีแยกประเภททั่วไป** > **รายการสมุดรายวัน** > **สมุดรายวันทั่วไป**
2. สร้างสมุดรายวันใหม่ ในฟิลด์ **ชื่อ** ให้เลือก ODComptabl
3. ไปที่ **รายการ** และป้อนข้อมูลต่อไปนี้:

    - ในฟิลด์ **วันที่** เลือก 4/15/2021
    - ในฟิลด์ **ชนิดบัญชี** เลือก **ลูกค้า**
    - ในฟิลด์ **บัญชี** เลือก **1001**
    - ในฟิลด์ **เดบิต** ป้อน 100
    - ในฟิลด์ **ชนิดบัญชีตรงข้าม** เลือก **ธนาคาร**
    - ในฟิลด์ **บัญชีตรงข้าม** เลือก **FRRT OPER**
    - ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** เลือก **ปกติ**
    - ในฟิลด์ **กลุ่มภาษีขาย ให้เลือก** เลือก **VE-DOM**

4. ลงรายการบัญชีสมุดรายวัน
5. ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันอื่น**
6. ในส่วน **เงื่อนไข** ในฟิลด์ **สมุดรายวัน** ให้เลือก ODComptabl
7. ในฟิลด์ **วันที่เริ่มต้น** เลือก 5/1/2021
8. ในฟิลด์ **วันที่สิ้นสุด** เลือก 5/31/2021
9. ในฟิลด์ **เอกสารพิมพ์สุดท้าย** เลือก **ใช่**
10. เลือก **ตกลง** และตรวจทานผลลัพธ์รายงาน

![รายงานสมุดรายวันอื่นหน้า 1](media/emea-bel-journal-reports-other-journal-report-1.png)
![รายงานสมุดรายวันอื่นหน้า 2](media/emea-bel-journal-reports-other-journal-report-2.png)

### <a name="print-overview-journal-report"></a>พิมพ์รายงานสมุดรายวันภาพรวม

เมื่อต้องการพิมพ์รายงาน **สมุดรายวันภาพรวม** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

1. ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันภาพรวม**
2. ในฟิลด์ **วันที่เริ่มต้น** เลือก 4/1/2021
3. ในฟิลด์ **วันที่สิ้นสุด** เลือก 5/31/2021
4. เลือก **ตกลง** และตรวจทานผลลัพธ์รายงาน

![ภาพรวมรายงานสมุดรายวัน](media/emea-bel-journal-reports-overview-journal-report.png)
