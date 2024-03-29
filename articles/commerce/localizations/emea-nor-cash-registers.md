---
title: ฟังก์ชันเครื่องบันทึกเงินสดสำหรับนอร์เวย์
description: บทความนี้แสดงภาพรวมของฟังก์ชันเครื่องบันทึกเงินสดที่พร้อมใช้งานสำหรับใน Microsoft Dynamics 365 Commerce และนําเสนอแนวทางเกี่ยวกับการตั้งค่าฟังก์ชัน
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: 30bd5ad8c1513c3d56cc4aa0a77b70fe38d31e0a
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346030"
---
# <a name="cash-register-functionality-for-norway"></a>ฟังก์ชันเครื่องบันทึกเงินสดสำหรับนอร์เวย์

[!include[banner](../includes/banner.md)]

บทความนี้แสดงภาพรวมของฟังก์ชันเครื่องบันทึกเงินสดที่พร้อมใช้งานสำหรับนอร์เวย์ใน Dynamics 365 Commerce และยังแสดงแนวทางเกี่ยวกับการตั้งค่าฟังก์ชันด้วย ฟังก์ชันประกอบต้วยส่วนต่อไปนี้:

- คุณลักษณะขายหน้าร้าน (POS) ทั่วไปที่พร้อมใช้งานกับลูกค้าในประเทศหรือทุกภูมิภาค ตัวอย่างรวมตัวเลือกที่ช่วยให้คุณสามารถป้องกันไม่ให้มีการพิมพ์สําเนาของใบเสร็จมากกว่าหนึ่งครั้ง
- คุณลักษณะการใช้เฉพาะนอร์เวย์ เช่น ลายเซ็นดิจิทัลของธุรกรรมการขาย

## <a name="overview-of-cash-register-functionality-for-norway"></a>ภาพรวมของฟังก์ชันเครื่องบันทึกเงินสดสำหรับนอร์เวย์

### <a name="common-pos-features"></a>คุณลักษณะ POS ทั่วไป

หากต้องการทราบเกี่ยวกับคุณลักษณะของ POS ที่พร้อมใช้งานกับลูกค้าในประเทศหรือทุกภูมิภาค โปรดดู [ทรัพยากรความช่วยเหลือสำหรับ Dynamics 365 Retail](../index.md)

คุณลักษณะการแปล POS เป็นภาษาท้องถิ่นต่อไปนี้ซึ่งใช้งานก่อนหน้านี้และที่พร้อมใช้งานแก่ลูกค้าในประเทศหรือภูมิภาคทั้งหมดขณะนี้สามารถใช้เฉพาะกับนอร์เวย์ได้:

- **พิมพ์ฟิลด์ข้อความบนใบเสร็จในขนาดแบบอักษรขนาดใหญ่** คุณสามารถใช้พารามิเตอร์ **ขนาดแบบอักษร** ในตัวออกแบบรูปแบบใบเสร็จเพื่อระบุว่าควรใช้ขนาดแบบอักษรขนาดใหญ่กับฟิลด์ในรูปแบบใบเสร็จ (ขนาดแบบอักษรขนาดใหญ่คือประมาณสองเท่าของขนาดแบบอักษรปกติ) ตัวอย่างเช่น คุณสามารถใช้พารามิเตอร์นี้เพื่อพิมพ์ตัวบ่งชี้ "คัดลอก" บนสําเนาของใบเสร็จเป็นอักขระขนาดใหญ่
- **ลงทะเบียนการพิมพ์สำเนาใบเสร็จในล็อกเหตุการณ์การตรวจสอบ POS** คุณสามารถใช้พารามิเตอร์ **การตรวจสอบ** ในโปรไฟล์ฟังก์ชันของ POS เพื่อเปิดใช้งานสำเนาของใบเสร็จที่จะพิมพ์และเหตุการณ์การตรวจสอบ POS อื่นๆ ที่จะลงทะเบียน เหตุการณ์การตรวจสอบลงทะเบียนอยู่ในฐานข้อมูลช่องทางและในศูนย์ควบคุม คุณสามารถดูเหตุการณ์การตรวจสอบได้ในหน้า **เหตุการณ์การตรวจสอบ**
- **ป้องกันสําเนาของใบเสร็จจากการพิมพ์มากกว่าหนึ่งครั้ง** เมื่อเปิดใช้งานพารามิเตอร์ **การตรวจสอบ** ในโปรไฟล์ฟังก์ชันของ POS อนุญาตให้ **พิมพ์สำเนาใบเสร็จ** ของสิทธิ์ POS ควบคุมว่าสามารถพิมพ์สำเนาของใบเสร็จหรือไม่ ยังมีตัวเลือกที่ช่วยให้คุณสามารถป้องกันไม่ให้มีการพิมพ์สําเนาของใบเสร็จมากกว่าหนึ่งครั้ง

นอกจากนี้ คุณลักษณะ POS ต่อไปนี้ยังถูกปรับใช้กับนอร์เวย์แต่ถูกดําเนินการให้แก่ลูกค้าในประเทศหรือทุกภูมิภาคด้วย

- **ลงทะเบียนเหตุการณ์เพิ่มเติมในล็อกเหตุการณ์การตรวจสอบ POS** หากพารามิเตอร์ **การตรวจสอบ** ในโปรไฟล์ฟังก์ชันของ POS เปิดใช้งาน เหตุการณ์ต่อไปนี้จะถูกลงทะเบียนในล็อกเหตุการณ์การตรวจสอบ POS

    - การตรวจสอบราคา
    - การแทนที่ภาษี
    - การแก้ไขปริมาณในบรรทัด
    - การล้างข้อมูลธุรกรรมจากฐานข้อมูลช่องทาง

### <a name="norway-specific-pos-features"></a>ลักษณะการทำงาน POS เฉพาะนอร์เวย์

คุณลักษณะ POS เฉพาะนอร์เวย์ต่อไปนี้เปิดใช้งานอยู่เมื่อตั้งค่าพารามิเตอร์ **รหัส ISO** ในโปรไฟล์ฟังก์ชันของ POS เป็น **ไม่**

#### <a name="digital-signing-of-sales-transactions"></a>การลงชื่อดิจิทัลของธุรกรรมการขาย

ทุกธุรกรรมการขายมีการลงชื่อแบบดิจิทัล ลายเซ็นจะถูกสร้างขึ้นและบันทึกในสมุดรายวันธุรกรรม POS พร้อมๆ กับที่ธุรกรรมจะถูกสรุป ลายเซ็นยังมีอยู่ในสมุดรายวันที่มีการส่งออกเพื่อวัตถุประสงค์การตรวจสอบบัญชีด้วย

เฉพาะธุรกรรมในการขายด้วยเงินสดเท่านั้นที่มีการลงชื่อ ต่อไปนี้เป็นตัวอย่างธุรกรรมที่ถูกแยกออกจากกระบวนการลงชื่อ:

- การชำระเงินล่วงหน้า (การฝากเงินเข้าบัญชีลูกค้า)
- การชำระเงินล่วงหน้าของใบสั่งขาย (การฝากเงินตามใบสั่งของลูกค้า)
- การออกบัตรของขวัญ
- ธุรกรรมที่ไม่มีการขาย (ป้อนข้อมูลเศษเงินทอน การเอาเงินออก และอื่น ๆ)

ข้อมูลที่ลงชื่อเป็นสตริงข้อความที่ประกอบด้วยฟิลด์ข้อมูลต่อไปนี้ ฟิลด์ข้อมูลจะถูกแยกด้วยเครื่องหมายอัฒภาค

1. ลายเซ็นก่อนหน้านี้ของ POS เดียวกัน (ระบบจะใช้ศูนย์ \[**0**\] ในธุรกรรมแรก)
2. วันที่ธุรกรรม
3. เวลาของธุรกรรม
4. หมายเลขธุรกรรมที่ลงชื่อตามลำดับ
5. ยอดเงินในธุรกรรมรวมภาษี
6. ยอดเงินในธุรกรรมไม่รวมภาษี

กระบวนการลงชื่อดิจิทัลใช้คีย์ RSA 1024 บิตที่มีฟังก์ชันแฮช SHA-1 (RSA-SHA1-1024) ระบบใช้ใบรับรองที่ติดตั้งใน Commerce Scale Unit เพื่อลงชื่อ รหัสเฉพาะของใบรับรอง (footprint) จะถูกบันทึกพร้อมด้วยลายเซ็น

ลายเซ็นจะจัดเก็บอยู่ในฐานข้อมูลร้านค้าและฐานข้อมูลศูนย์ควบคุม (HQ) พร้อมด้วยข้อมูลธุรกรรม คุณสามารถดูลายเซ็นของธุรกรรมพร้อมข้อมูลธุรกรรมที่ใช้สร้างได้บน FastTab **ธุรกรรมทางบัญชี** ของหน้า **ธุรกรรมร้านค้า**

#### <a name="receipts"></a>การรับสินค้า

คุณสามารถรวมข้อมูลเพิ่มเติมที่ใช้ใบเสร็จของนอร์เวย์โดยใช้ฟิลด์แบบกำหนดเอง:

- **ชื่อใบเสร็จ** – คุณสามารถเพิ่มฟิลด์ในโครงร่างรูปแบบใบเสร็จเพื่อระบุชนิดของใบเสร็จ ตัวอย่างเช่น ใบเสร็จการขายจะรวมข้อความ "ใบเสร็จการขาย" ไว้ด้วย
- **หมายเลขลำดับของธุรกรรมที่ลงชื่อ** – หมายเลขลำดับของธุรกรรมที่ลงชื่อสามารถปรากฏบนใบเสร็จเพื่อเชื่อมโยงใบเสร็จที่พิมพ์กับลายเซ็นดิจิทัลในฐานข้อมูลได้
- **ผลรวมใบเสร็จ** – ฟิลด์ที่ป้อนเองของยอดรวมใบเสร็จจะไม่รวมยอดขายจากยอดเงินรวมของธุรกรรม ยอดเงินที่ไม่รวมยอดขายรวมยอดเงินในการดําเนินงานต่อไปนี้:

    - การชำระเงินล่วงหน้า (การฝากเงินเข้าบัญชีลูกค้า)
    - การชำระเงินล่วงหน้าของใบสั่งขาย (การฝากเงินตามใบสั่งของลูกค้า)
    - การออกบัตรของขวัญ
    - การเพิ่มเงินลงในบัตรของขวัญ

#### <a name="x-and-z-reports"></a>รายงาน X และ Z

ข้อมูลที่ถูกรวมในรายงาน X และ Z เป็นไปตามข้อกำหนดของนอร์เวย์ ตัวอย่างเช่น **ผลรวมยอดขายเงินสด** รวมเฉพาะยอดเงินของธุรกรรมการขายด้วยเงินสด และไม่รวมการดําเนินงานบัตรของขวัญที่ออกและการชำระเงินล่วงหน้า ยอดรวมการขายเงินสดจะแสดงรายการต่อกลุ่มสินค้าและวิธีการชำระเงินด้วย นอกจากนี้ ยอด **การขายรวมทั้งหมด** และ **การส่งคืนทั้งหมด** สะสมจะได้รับการรักษาและพิมพ์

#### <a name="saf-t-cash-register-audit-file"></a>ไฟล์การตรวจสอบเครื่องบันทึกเงินสด SAF-T

คุณสามารถส่งออกสมุดรายวันธุรกรรม POS ในรูปแบบเครื่องบันทึกเงินสดภาษี (SAF-T) - ไฟล์การตรวจสอบมาตรฐานที่กําหนดล่วงหน้า ไฟล์การตรวจสอบจะประกอบด้วยข้อมูลเกี่ยวกับองค์กร ข้อมูลหลักที่เกี่ยวข้อง (เช่น กลุ่มสินค้า สินค้า และรหัสภาษี) ข้อมูลธุรกรรมการขายเงินสดพร้อมด้วยลายเซ็นของธุรกรรมดังกล่าว ข้อมูลเหตุการณ์ที่ไม่ใช่การขาย และข้อมูลรายงานวันที่สิ้นสุด

ไฟล์การตรวจสอบสามารถถูกส่งออกไปยังสถานการณ์ต่อไปนี้:

- ต่อร้านค้า
- ทุกร้าน
- ต่อเทอร์มินัล
- เทอร์มินัลทั้งหมด

คุณยังสามารถส่งรายงานจากนิติบุคคลหนึ่งในนามของนิติบุคคลอื่น ในกรณีนี้ คุณต้องรันการส่งออกจากนิติบุคคลที่ดําเนินงาน และระบุนิติบุคคลที่รายงานเป็นผู้ส่งรายงาน

รูปแบบเครื่องบันทึกเงินสด SAF-T ใช้ที่ศูนย์ควบคุมโดยใช้ [การรายงานทางอิเล็กทรอนิกส์](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) 

## <a name="setting-up-commerce-for-norway"></a>การตั้งค่า Commerce สำหรับนอร์เวย์

ส่วนนี้อธิบายการตั้งค่าเฉพาะและที่แนะนำให้เลือกสำหรับนอร์เวย์ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ทรัพยากรความช่วยเหลือสำหรับ Dynamics 365 Retail](../index.md)

หากต้องการใช้ฟังก์ชันเฉพาะนอร์เวย์ คุณต้องกรอกข้อมูลงานต่อไปนี้ให้เสร็จสิ้น:

- ให้ตั้งค่าฟิลด์ **ประเทศ/ภูมิภาค** เป็น **NOR** (นอร์เวย์) ในที่อยู่หลักของนิติบุคคล
- ให้ตั้งค่าฟิลด์รหัส **รหัส POS** เป็น **DE** (นอร์เวย์) ในโปรไฟล์ฟังก์ชัน ISO ทุกร้านที่ตั้งอยู่ในนอร์เวย์

คุณต้องระบุการตั้งค่าต่อไปนี้สำหรับนอร์เวย์

### <a name="enable-features-for-norway"></a>เปิดใช้งานคุณลักษณะสำหรับนอร์เวย์

คุณต้องเปิดใช้งานคุณลักษณะต่อไปนี้ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ของ Commerce headquarters:

- (นอร์เวย์) เปิดใช้งานเหตุการณ์การตรวจสอบเพิ่มเติมใน POS
- (นอร์เวย์) เปิดใช้งานข้อมูลเพิ่มเติมในใบแจ้งยอดสิ้นวันใน POS

### <a name="set-up-the-legal-entity"></a>ตั้งค่านิติบุคคล

ตรวจสอบให้แน่ใจว่าระบุชื่อของนิติบุคคล ชื่อนี้จะพิมพ์บนรายงาน X และ Z

หรือบน FastTab **ข้อมูลบัญชีธนาคาร** ในฟิลด์ **หมายเลขการกำหนดเส้นทาง** ให้ระบุหมายเลของค์กร

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>การตั้งค่าภาษีมูลค่าเพิ่ม (VAT) ตามข้อกำหนดของนอร์เวย์


คุณต้องสร้างภาษีขาย กลุ่มภาษีขาย และกลุ่มภาษีขายของสินค้า คุณต้องตั้งค่าข้อมูลภาษีขายเกี่ยวกับผลิตภัณฑ์และบริการด้วย สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าและใช้ภาษีขาย ให้ดูที่ [ภาพรวมของภาษีขาย](../../finance/general-ledger/indirect-taxes-overview.md)

คุณต้องระบุกลุ่มภาษีขายและเปิดใช้งานตัวเลือก **ราคารวมภาษีขาย** ให้กับร้านค้าที่ตั้งอยู่ในนอร์เวย์ด้วย

### <a name="set-up-functionality-profiles"></a>ตั้งค่าโพรไฟล์ฟังก์ชัน

คุณต้องเปิดใช้งานการตรวจสอบและตั้งค่าการป้อนหมายเลขใบเสร็จ

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>อัปเดตกลุ่มสิทธิ์ของ POS และแต่ละการตั้งค่าสิทธิ์ของผู้ปฏิบัติงานที่จัดเก็บ

ตั้งค่าสิทธิ์ **อนุญาตให้พิมพ์สําเนาใบเสร็จ** เป็นค่าที่เหมาะสมดังนี้:

- **อนุญาตเสมอ** – ผู้ปฏิบัติงานสามารถพิมพ์สําเนาของใบเสร็จได้หลายครั้ง
- **อนุญาตเพียงครั้งเดียว** – ผู้ปฏิบัติงานสามารถพิมพ์สําเนาของใบเสร็จได้เพียงครั้งเดียว
- **อนุญาตเพียงครั้งเดียวและหากมีฐานข้อมูล HQ เท่านั้น** – ผู้ปฏิบัติงานสามารถพิมพ์สําเนาของใบเสร็จได้เพียงครั้งเดียว และเฉพาะเมื่อฐานข้อมูล HQ พร้อมใช้งานผ่าน Commerce Data Exchange: บริการแบบเรียลไทม์ เพื่อให้ระบบสามารถตรวจสอบว่าไม่มีสําเนาของใบเสร็จใดที่มีการพิมพ์ก่อนหน้านี้ในร้านค้าใดๆ แล้ว
- **ไม่** – ผู้ปฏิบัติงานไม่สามารถพิมพ์สําเนาของใบเสร็จได้

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>ตั้งค่าคอนฟิกฟิลด์ที่กําหนดเองเพื่อให้สามารถใช้ฟิลด์เหล่านั้นในรูปแบบใบเสร็จของใบเสร็จได้

ในหน้า **ข้อความภาษา** ให้เพิ่มเรกคอร์ดต่อไปนี้ของป้ายชื่อของฟิลด์แบบกำหนดเองเป็นโครงร่างของใบเสร็จ โปรดทราบว่ามีเพียงค่า **รหัสภาษา** **รหัสข้อความ** และ **ข้อความ** ที่แสดงในตารางเท่านั้น คุณสามารถเปลี่ยนเพื่อให้ตรงกับความต้องการของคุณได้

| รหัสภาษา | ข้อความ                   | รหัสข้อความ |
|-------------|------------------------|---------|
| th       | ชื่อใบเสร็จ          | 900011  |
| th       | เป็นบัตรของขวัญ           | 900012  |
| th       | รวม (การขาย)          | 900013  |
| th       | ภาษีรวม (ขาย)      | 900014  |
| th       | รวมภาษี (การขาย) | 900015  |
| th       | ยอดเงินภาษี (การขาย)     | 900016  |
| th       | รหัสธุรกรรมเงินสด    | 900017  |

ในหน้า **ฟิลด์ที่กำหนดเอง** ให้เพิ่มเรกคอร์ดต่อไปนี้ของฟิลด์แบบกำหนดเองเป็นโครงร่างของใบเสร็จ โปรดทราบว่าค่า **รหัสข้อความคำอธิบาย** ต้องสอดคล้องกับค่า **รหัสข้อความ** ที่คุณระบุไว้ในหน้า **ข้อความภาษา**

| ชื่อ                            | ชนิด    | รหัสข้อความของคำอธิบาย |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | ใบเสร็จรับเงิน | 900011          |
| IsGiftCard                      | ใบเสร็จรับเงิน | 900012          |
| SalesTotalExt                   | ใบเสร็จรับเงิน | 900013          |
| TaxTotalExt                     | ใบเสร็จรับเงิน | 900014          |
| TotalWithTaxExt                 | ใบเสร็จรับเงิน | 900015          |
| AmountPerTaxExt                 | ใบเสร็จรับเงิน | 900016          |
| CashTransactionSequentialNumber | ใบเสร็จรับเงิน | 900017          |

> [!NOTE]
> คุณควรระบุชื่อฟิลด์ที่ศุลกากรซึ่งถูกต้อง ตามที่แสดงรายการไว้ในตารางข้างบน ชื่อฟิลด์ที่กำหนดเองไม่ถูกต้องจะทําให้เกิดข้อมูลที่ขาดหายไปในใบเสร็จ

### <a name="configure-receipt-formats"></a>ตั้งค่าคอนฟิกรูปแบบใบเสร็จ

สำหรับรูปแบบใบเสร็จที่จำเป็นทั้งหมด ให้เปลี่ยนค่าของฟิลด์ **ลักษณะการพิมพ์** เป็น **พิมพ์เสมอ** สำหรับรูปแบบใบเสร็จ

ในตัวออกแบบรูปแบบใบเสร็จ ให้เพิ่มฟิลด์ที่กำหนดเองต่อไปนี้ลงในส่วนใบเสร็จที่เหมาะสม โปรดสังเกตว่าชื่อฟิลด์จะตรงกับข้อความภาษาที่คุณกําหนดไว้ในส่วนก่อนหน้านี้

1. ส่วนหัว:

    - **ชื่อใบเสร็จ** – ฟิลด์นี้จะระบุชนิดของใบเสร็จ
    - **รหัสธุรกรรมเงินสด** – ฟิลด์นี้จะพิมพ์หมายเลขลำดับของธุรกรรมเงินสดที่ลงชื่อ

2. รายการ:

    - **บัตรของขวัญ** – ฟิลด์นี้จะเลือกรายการรับสินค้าที่เกี่ยวข้องกับการดําเนินงาน ออกบัตรของขวัญ หรือ เพิ่มลงในบัตรของขวัญ

3. ส่วนท้าย:

    - **ยอดรวม (การขาย)** – ฟิลด์นี้จะพิมพ์ยอดขายเงินสดรวมของใบเสร็จรับเงิน จำนวนเงินไม่รวมภาษี การชำระเงินล่วงหน้าและการดําเนินงานบัตรของขวัญจะไม่รวม
    - **ภาษีรวม (การขาย)** – ฟิลด์นี้จะพิมพ์ยอดภาษีรวมของใบเสร็จสำหรับการขายเงินสด การชำระเงินล่วงหน้าและการดําเนินงานบัตรของขวัญจะไม่รวม
    - **ยอดรวมภาษี (การขาย)** – ฟิลด์นี้จะพิมพ์ยอดขายเงินสดรวมของใบเสร็จรับเงิน จำนวนเงินรวมภาษี การชำระเงินล่วงหน้าและการดําเนินงานบัตรของขวัญจะไม่รวม
    - **ยอดภาษี (การขาย)** – ฟิลด์นี้จะพิมพ์ยอดภาษีของใบเสร็จต่อรหัสภาษี การชำระเงินล่วงหน้าและการดําเนินงานบัตรของขวัญจะไม่รวม

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้งานรูปแบบใบเสร็จ โปรดดูที่ [การตั้งค่าและออกแบบรูปแบบใบเสร็จ](../receipt-templates-printing.md)

### <a name="configure-the-saf-t-cash-register-export-format"></a>ตั้งค่าคอนฟิกรูปแบบการส่งออกเครื่องบันทึกเงินสด SAF-T

การตั้งค่าคอนฟิกเครื่องบันทึกเงินสด SAF-T สามารถดาวน์โหลดได้จาก Microsoft Dynamics Lifecycle Services (LCS) สำหรับข้อมูลเพิ่มเติม โปรดดู [นำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md) คุณต้องดาวน์โหลดการตั้งค่าคอนฟิกต่อไปนี้:

- **ข้อมูลช่องทางการขายปลีก.รุ่น.1** – การตั้งค่าคอนฟิกรูปแบบข้อมูล
- **ข้อมูลช่องทางการขายปลีก DMM.รุ่น.1.14** – การตั้งค่าคอนฟิกการแม็ปรูปแบบข้อมูล
- **เครื่องบันทึกเงินสด NO SAF T รุ่น.1.20** – การตั้งค่าคอนฟิกรูปแบบ

หลังจากที่คุณนําเข้าการตั้งค่าคอนฟิกบนหน้า **พารามิเตอร์ Commerce** บนแท็บ **เอกสารอิเล็กทรอนิกส์** ในฟิลด์ **รูปแบบการส่งออกเครื่องบันทึกเงินสด SAF-T** ให้เลือกชื่อของการตั้งค่าคอนฟิกรูปแบบที่นําเข้า

คุณต้องแม็ปข้อมูลหลักที่กําหนดให้กับรหัสมาตรฐาน SAF-T ที่กําหนดล่วงหน้าด้วย สำหรับข้อมูลเพิ่มเติม ดูคู่มือเครื่องบันทึกเงินสด SAF-T ที่จัดเตรียมให้โดยหน่วยงานจัดเก็บภาษีนอร์เวย์ เมื่อต้องการสร้างการแม็ป คุณต้องตั้งค่าฟิลด์ **รหัสเครื่องบันทึกเงินสด SAF-T** ใหม่บนหน้าต่อไปนี้:

- กลุ่มสินค้า
- วิธีการชำระเงิน
- รหัสภาษีขาย

### <a name="configure-channel-components"></a>ตั้งค่าคอนฟิกส่วนประกอบช่องทาง

เมื่อต้องการเปิดใช้งานฟังก์ชันเฉพาะนอร์เวย์ คุณต้องตั้งค่าคอนฟิกส่วนประกอบช่องทาง สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [คำแนะนำการปรับใช้งาน](emea-nor-fi-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
