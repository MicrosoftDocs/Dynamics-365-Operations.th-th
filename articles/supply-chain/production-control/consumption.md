---
title: คำนวณปริมาณการใช้วัสดุ
description: บทความนี้แสดงข้อมูลเกี่ยวกับตัวเลือกต่างๆ ที่เกี่ยวข้องกับการคำนวณปริมาณการใช้วัสดุ
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e62d49b5fa2b26c34106e5bbf3dfbc27145e5c4e9acf798b8faef273d8957e51
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776883"
---
# <a name="calculate-material-consumption"></a>คำนวณปริมาณการใช้วัสดุ

[!include [banner](../includes/banner.md)]

บทความนี้แสดงข้อมูลเกี่ยวกับตัวเลือกต่างๆ ที่เกี่ยวข้องกับการคำนวณปริมาณการใช้วัสดุ 

ตัวเลือกต่อไปนี้ที่สัมพันธ์กับการคำนวณปริมาณการใช้วัสดุจะพร้อมใช้งานในแท็บ **ตั้งค่า** และ **ปริมาณการใช้ขั้นตอน** ในแท็บด่วน **รายละเอียดรายการ** ของหน้า **สูตรการผลิต**

## <a name="variable-and-constant-consumption"></a>ปริมาณการใช้วัสดุแปรผันและคงที่
ในฟิลด์ **ปริมาณการใช้คือ** คุณสามารถเลือกว่าควรคำนวณปริมาณการใช้วัสดุเป็นปริมาณคงหรือผันแปรปริมาณได้ เลือก **คงที่** หากปริมาณหรือปริมาตรคงที่ต้องถูกระบุสำหรับการผลิตโดยไม่คำนึงถึงปริมาณที่มีการผลิต เลือก **ตัวแปร** ซึ่งเป็นการตั้งค่าเริ่มต้น ถ้าจำนวนของวัตถุดิบที่ต้องการในสินค้าสำเร็จรูปเป็นสัดส่วนกับจำนวนสินค้าสำเร็จรูปที่มีการผลิต

## <a name="calculating-consumption-from-a-formula"></a>การคำนวณปริมาณการใช้วัสดุจากสูตร
ในฟิลด์ **สูตร** คุณสามารถตั้งค่าสูตรที่หลากหลายสำหรับการคำนวณปริมาณการใช้วัสดุตได้ ถ้าคุณใช้ค่าเริ่มต้น **มาตรฐาน** ปริมาณการใช้จะไม่ได้คำนวณมาจากสูตร สูตรต่อไปนี้ทำงานร่วมกับฟิลด์ **ความสูง** **ความกว้าง** **ความลึก** **ความหนาแน่น** และ **ค่าคงที่**:

-   ความสูง \* ค่าคงที่
-   ความสูง \* ความกว้าง \* ค่าคงที่
-   ความสูง \* ความกว้าง \* ความลึก \* ค่าคงที่
-   (ความสูง \* ความกว้าง \* ความลึก / ความหนาแน่น) \* ค่าคงที่

## <a name="rounding-up-and-multiples"></a>การปัดเศษขึ้นและการคูณ
ทั้งฟิลด์ **การปัดเศษขึ้น** และ **การคูณ** จะช่วยให้คุณสามารถปัดเศษค่าปริมาณการใช้วัสดุได้ ตัวอย่างเช่น คุณสามารถปัดเศษค่าตามหน่วยจัดการวัสดุที่วัตถุดิบมีการเบิกสินค้าสำหรับการผลิต ตัวเลือกต่อไปนี้พร้อมใช้งานในฟิลด์ **การปัดเศษขึ้น**: **ปริมาณ** **การวัด** และ **ปริมาณการใช้วัสดุ**

### <a name="quantity"></a>ปริมาณ

ถ้าคุณเลือก **ปริมาณ** ให้เป็นกลไกการปัดเศษ ปริมาณต้องเป็นตัวคูณของปริมาณที่ระบุ ตัวอย่างเช่น ถ้าจำเป็นต้องมีตัวเลขจำนวนเต็ม ให้เลือก **1** ในฟิลด์ **การคูณ** จากนั้นหมายเลขจะถูกปัดเศษขึ้นเป็นปริมาณที่สามารถหารด้วย 1 ลงตัว

### <a name="measurement"></a>การวัด

โดยทั่วไป คุณเลือก **การวัด** ให้เป็นกลไกการปัดเศษขึ้นเมื่อวัตถุดิบอยู่ในมิติเฉพาะ ตัวอย่างเช่น ท่อโลหะยาว 2 เมตรจำนวน 1 ชิ้นที่ต้องใช้สำหรับสินค้าสำเร็จรูป และท่อโลหะถูกจัดเก็บในความยาวที่ 4.5 เมตร ในกรณีนี้ กลไกการปัดเศษ **การวัด** สามารถใช้เพื่อคำนวณจำนวนท่อโลหะที่จำเป็นต่อการผลิตจำนวนชิ้นที่ต้องการของสินค้าสำเร็จรูปได้ สำหรับตัวอย่างนี้ ฟิลด์ **สูตร** ถูกตั้งค่าเป็น **ความสูง \* ค่าคงที่** ฟิลด์ **ความสูง** ถูกตั้งค่าเป็น **2** เพื่อระบุความยาวของท่อที่จำเป็นสำหรับสินค้าสำเร็จรูป ฟิลด์ **การคูณ** ถูกกำหนดเป็น **4.5** เพื่อบ่งชี้ว่ามีการเบิกท่อที่มีความยาว 4.5 เมตร นี่คือการคำนวณ:

1.  จำนวนเของการคูณที่จำเป็นสำหรับสินค้าสำเร็จรูป 10 ชิ้น: 10 ÷ 2 = 5 ชิ้น
2.  ปริมาณการใช้วัสดุรวม: 4.5 × 5 = 22.5 เมตรของท่อโลหะ

มีการสันนิษฐานว่า จะสูญเสียท่อยาว 0.5 เมตรสำหรับการใช้ท่อทุกๆห้าชิ้น

### <a name="consumption"></a>ปริมาณการใช้

โดยทั่วไป คุณเลือก **ปริมาณการใช้วัสดุ** ให้เป็นกลไกการปัดเศษขึ้นเมื่อต้องมีการเบิกวัตถุดิบในปริมาณทั้งหมดของหน่วยจัดการวัสดุที่เฉพาะเจาะจงของผลิตภัณฑ์ ตัวอย่างเช่น สี 2 ควอร์ตจะถูกใช้ในการผลิตสินค้าสำเร็จรูปหนึ่งชิ้น และมีการเบิกสีกระป๋อง 25 ควอร์ต ในกรณีนี้ กลไกการปัดเศษ **ปริมาณการใช้วัสดุ** สามารถใช้เพื่อปัดเศษปริมาณการใช้วัสดุเป็นจำนวนเต็มของกระป๋อง 25 ควอร์ตได้ นี่เป็นการคำนวณจำนวนสีที่ต้องการ ถ้าต้องมีการผลิตสินค้าสำเร็จรูปจำนวน 180 ชิ้น:

1.  สีที่ต้องการ ซึ่งไม่รวมของเสีย: 180 x 2 = 360 ควอร์ต
2.  จำนวนของกระป๋อง: 360 ÷ 25 = 14.4 ซึ่งถูกปัดเศษขึ้นเป็น 15
3.  สีที่ต้องการ ซึ่งรวมของเสีย: 15 x 25 = 375 ควอร์ต

## <a name="step-consumption"></a>ปริมาณการใช้ขั้นตอน
ปริมาณการใช้ขั้นตอนถูกใช้เพื่อคำนวณปริมาณการใช้วัสดุคงที่ในช่วงของปริมาณ ถ้าคุณเลือก **ปริมาณการใช้ขั้นตอน** ในฟิลด์ **สูตร** บนแท็บ **ตั้งค่า** คุณสามารถเพิ่มข้อมูลเกี่ยวกับขั้นตอนต่าง ๆ ได้ในแท็บ **ปริมาณการใช้ขั้นตอน** ปริมาณที่ใช้แบบคงที่สามารถถูกตั้งค่าในช่วงของปริมาณที่มีการผลิต ตัวอย่างเช่น ปริมาณการใช้ขั้นตอนถูกตั้งค่าดังที่แสดงในตารางต่อไปนี้

| จากชุด | ปริมาณ |
|-------------|----------|
| 0.00        | 10.0000  |
| 100.00      | 20.0000  |
| 200.00      | 40.0000  |

ปริมาณของสูตรการผลิต (BOM) คือ 1 และปริมาณการผลิตคือ 110 สูตรสำหรับปริมาณการใช้คือ จากชุด (ปริมาณ) = ปริมาณการใช้ เนื่องจากปริมาณการผลิตคือ 110 จึงอยู่ใน "จาก 100 ชุด" ดังนั้น ปริมาณคือ 20





[!INCLUDE[footer-include](../../includes/footer-banner.md)]