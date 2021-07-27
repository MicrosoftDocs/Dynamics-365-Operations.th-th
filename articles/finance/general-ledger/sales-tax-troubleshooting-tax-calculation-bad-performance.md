---
title: ประสิทธิภาพการคํานวณภาษีมีผลกระทบต่อธุรกรรม
description: หัวข้อนี้มีข้อมูลการแก้ไขปัญหาที่เกี่ยวข้องกับประสิทธิภาพการคํานวณภาษีและผลกระทบต่อธุรกรรม
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 2bb1f22c33de52f9a7bc00b450ce131d4d58d200
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352845"
---
# <a name="tax-calculation-performance-affects-transactions"></a>ประสิทธิภาพการคํานวณภาษีมีผลกระทบต่อธุรกรรม

[!include [banner](../includes/banner.md)]

ในบางครั้ง ธุรกรรมจะได้รับผลกระทบจากปัญหาด้านประสิทธิภาพการคํานวณภาษี เมื่อต้องการแก้ไขปัญหานี้ ให้ปฏิบัติตามขั้นตอนในส่วนต่อไปนี้ตามต้องการ

## <a name="review-the-transaction-line-count"></a>ตรวจสอบจำนวนรายการธุรกรรม

ระบุว่าธุรกรรมมีรายการจํานวนมาก (ตัวอย่างเช่น มากกว่าหนึ่งร้อย) หรือไม่ หากไม่ เลื่อนไปที่ส่วนถัดไป ถ้าธุรกรรมมีมากกว่าหนึ่งรายการ ให้หน่วงเวลาการคํานวณภาษี สำหรับข้อมูลเพิ่มเติม ให้ดู [เปิดใช้งานการคํานวณภาษีล่าช้าในสมุดรายวัน](enable-delayed-tax-calculation.md) 

จากนั้น คุณสามารถระบุว่าเป็นไปตามเงื่อนไขใดเงื่อนไขหนึ่งต่อไปนี้

- มีธุรกรรมการนําเข้าจากไฟล์ขนาดใหญ่
- รอบเวลาหลายรอบจะประมวลผลการคํานวณภาษีธุรกรรมในเวลาเดียวกัน
- ธุรกรรมมีหลายรายการ และมีการอัปเดตมุมมองในเวลาจริง ตัวอย่างเช่น ฟิลด์ **ยอดภาษีขายที่คํานวณได้** ในหน้า **สมุดรายวันทั่วไป** จะมีการอัปเดตในเวลาจริงเมื่อมีการเปลี่ยนแปลงฟิลด์ของบรรทัด

   [![ฟิลด์จํานวนเงินภาษีขายที่คํานวณได้ในหน้าใบสำคัญสมุดรายวัน](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

หากเป็นไปตามเงื่อนไขใดเงื่อนไขหนึ่ง ให้หน่วงเวลาการคํานวณภาษี

## <a name="review-the-call-stack"></a>ตรวจทานสแต็คการเรียก

ทบทวนสแต็คการเรียกเพื่อระบุว่าจะเรียกการคํานวณภาษีหลายครั้งหรือไม่ หากไม่ เลื่อนไปที่ส่วนถัดไป ถ้าเรียกสแต็คการเรียกหลายครั้ง ให้ปฏิบัติตามขั้นตอนเหล่านี้เพื่อลดเวลาการคํานวณภาษี

1. ถ้าสมุดรายวันพิจารณาว่าเป็นธุรกรรมแล้ว ให้หน่วงเวลาการคํานวณภาษี สำหรับข้อมูลเพิ่มเติม ให้ดู [เปิดใช้งานการคํานวณภาษีล่าช้าในสมุดรายวัน](enable-delayed-tax-calculation.md)
2. ถ้าธุรกรรมเป็นใบสั่งซื้อ และรุ่นของโปรแกรมประยุกต์หลัง 10.0.15 คุณสามารถเลื่อนเวลาการคํานวณภาษีได้จนกว่าจะมีการคํานวณครั้งสุดท้ายโดยเปิดใช้งานเที่ยวบิน **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** ได้

## <a name="review-the-call-stack-timeline"></a>ตรวจทานเส้นเวลาสแต็คการเรียก

ทบทวนเส้นเวลาสแต็คการเรียก เพื่อตัดสินว่ามีปัญหาต่อไปนี้อยู่หรือไม่ หากสินค้าเหล่านั้นเปิดใช้งานเที่ยวบินของ **TaxUncommittedDoSollateSolFsoling** เพื่อแก้ปัญหานี้

- ธุรกรรมจะส่งผลให้ระบบหยุดตอบสนองจนกว่ารอบเวลาจะสิ้นสุดลง ดังนั้น ธุรกรรมจึงไม่สามารถคํานวณผลภาษีได้ ภาพประกอบต่อไปนี้จะแสดงกล่องข้อความ "รอบเวลาสิ้นสุด" ที่คุณได้รับ

    [![ข้อความสิ้นสุดรอบเวลา](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- วิธีการ **TaxUncommitted** จะใช้เวลามากกว่าวิธีการอื่น ๆ ตัวอย่างเช่น ในภาพประกอบต่อไปนี้ วิธีการ **TaxUncommitted::updateTaxUncommitted()** จะใช้เวลา 43,347.42 วินาที แต่วิธีการอื่น ๆ จะใช้เวลา 0.09 วินาที

    [![ระยะเวลาของวิธีการ](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>การปรับแต่งและการคํานวณภาษีที่เรียก

เมื่อคุณกำหนดเอง อย่าเรียกการคํานวณภาษีในวิธีการ **insert()** หรือ **update()** ของแต่ละบรรทัด ควรเรียกการคํานวณภาษีที่ระดับธุรกรรม

## <a name="determine-whether-customization-exists"></a>ระบุว่ามีการเลือกเองอยู่หรือไม่

หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ไม่พบปัญหา ให้ระบุว่ามีการเลือกเองอยู่หรือไม่ ถ้าไม่มีการเลือกเองอยู่ ให้สร้างคำขอบริการของ Microsoft เพื่อขอความช่วยเหลือเพิ่มเติม

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
