---
title: ย้ายข้อมูลผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจากตัวรวมข้อมูลไปที่การรวมแบบสองทิศทาง
description: บทความนี้อธิบายวิธีย้ายข้อมูลผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจากตัวรวมข้อมูลไปที่การรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: bbf5a7c2f409003816e2becf1a58ee7d7d5aafb2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289094"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>ย้ายข้อมูลผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจากตัวรวมข้อมูลไปที่การรวมแบบสองทิศทาง

[!include [banner](../../includes/banner.md)]

โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าไปถึงเงินสดที่สามารถใช้งานกับตัวรวมข้อมูลเข้ากันไม่ได้กับการรวมแบบสองทิศทาง เหตุผลสำหรับการเป็นดัชนี msdynce_AccountNumber ในตารางบัญชีที่มาจากโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าไปถึงเงินสด ถ้ามีดัชนีนี้อยู่ คุณจะไม่สามารถสร้างหมายเลขบัญชีลูกค้าเดียวกันในนิติบุคคลที่แตกต่างกันสองราย คุณสามารถเลือกที่จะเริ่มต้นใหม่ด้วยการรวมแบบสองทิศทางได้โดยการย้ายข้อมูลผู้ที่มีแนวโน้มจะเป็นลูกค้าไปถึงเงินสดจากตัวรวมข้อมูลไปยังการรวมแบบสองทิศทาง หรือคุณสามารถติดตั้งรุ่น "dorman" ล่าสุดของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าไปถึงเงินสด บทความนี้จะกล่าวถึงวิธีการทั้งคู่นี้

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>ติดตั้งรุ่น "dorman" ล่าสุดของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าไปถึงเงินสดของตัวรวมข้อมูล

**P2C รุ่น 15.0.0.2** ถือเป็นรุ่น "dorman" ล่าสุดของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าไปถึงเงินสดของตัวรวมข้อมูล คุณสามารถดาวน์โหลดจาก [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C)

คุณต้องติดตั้งด้วยตนเอง หลังจากการติดตั้ง ทุกอย่างยังคงเหมือนเดิมทุกอย่างถูกต้อง ยกเว้นดัชนี msdynce_AccountNumber จะถูกลบออก

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>ขั้นตอนในการย้ายข้อมูลผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจากตัวรวมข้อมูลไปที่การรวมแบบสองทิศทาง

หากต้องการย้ายข้อมูลผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจากตัวรวมข้อมูลไปที่การรวมแบบสองทิศทาง ให้ทำตามขั้นตอนต่อไปนี้

1. เรียกใช้งานตัวรวมข้อมูลผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดเพื่อซิงโครไนส์แบบสมบูรณ์ครั้งสุดท้ายหนึ่งรายการ ด้วยวิธีนี้ คุณจึงมั่นใจว่าทั้งระบบ (แอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้า) มีข้อมูลทั้งหมด
2. เพื่อช่วยป้องกันการสูญเสียข้อมูลที่อาจเกิดขึ้น ให้ส่งออกข้อมูลผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจาก Microsoft Dynamics 365 Sales ไปยังไฟล์ Excel หรือไฟล์ค่าที่แบ่งด้วยเครื่องหมายจุลภาค (CSV) ส่งออกข้อมูลจากเอนทิตีต่อไปนี้:

    - [บัญชี](#account-table)
    - [การติดต่อ](#contact-table)
    - [ใบแจ้งหนี้](#invoice-table)
    - ผลิตภัณฑ์ในใบแจ้งหนี้
    - [ใบสั่ง](#order-table)
    - [สั่งซื้อผลิตภัณฑ์](#order-products-table)
    - [ผลิตภัณฑ์](#products-table)
    - [ใบเสนอราคา](#quote-and-quote-product-tables)
    - [ผลิตภัณฑ์ในใบเสนอราคา](#quote-and-quote-product-tables)

3. ถอนการติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจากสภาพแวดล้อมการขาย ขั้นตอนนี้จะลบคอลัมน์และข้อมูลที่สอดคล้องกันที่แนะนำโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด
4. ติดตั้งโซลูชันการรวมแบบสองทิศทาง
5. สร้างการเชื่อมต่อการรวมแบบสองทิศทางระหว่างแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้า สำหรับนิติบุคคลหนึ่งรายหรือมากกว่า
6. เปิดใช้งานแผนผังตารางการรวมแบบสองทิศทาง และเรียกใช้การซิงโครไนส์เริ่มแรกด้วยข้อมูลอ้างอิงที่ต้องใช้ (สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ข้อควรพิจารณาในการซิงโครไนส์เริ่มแรก](initial-sync-guidance.md)) ตัวอย่างของข้อมูลที่ต้องใช้ ได้แก่ กลุ่มลูกค้า เงื่อนไขการชำระเงิน และกำหนดการชำระเงิน อย่าเปิดใช้งานแผนผังการรวมแบบสองทิศทางของตารางที่ต้องมีการเริ่มต้น เช่น บัญชี ใบเสนอราคา บรรทัดใบเสนอราคา ใบสั่ง และตารางบรรทัดใบสั่ง
7. ในแอปการมีส่วนร่วมของลูกค้า ไปที่ **การตั้งค่าขั้นสูง \> การตั้งค่าระบบ \> การจัดการข้อมูล \> การทำสำเนากฎการตรวจหา** และปิดใช้งานกฎทั้งหมด
8. เริ่มต้นตารางที่แสดงรายการอยู่ในขั้นตอนที่ 2 สำหรับคำแนะนำ ให้ดูที่ส่วนที่เหลือของบทความนี้
9. เปิดแอปการเงินและการดำเนินงาน และเปิดใช้งานแผนผังตาราง เช่น บัญชี ใบเสนอราคา บรรทัดใบเสนอราคา ใบสั่ง และแผนผังตารางบรรทัดใบสั่ง จากนั้นทำการซิงโครไนส์เริ่มแรก (สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ข้อควรพิจารณาในการซิงโครไนส์เริ่มแรก](initial-sync-guidance.md)) กระบวนการนี้จะซิงค์ข้อมูลเพิ่มเติมจากแอปการเงินและการดำเนินงาน เช่น สถานะการประมวลผล ที่อยู่จัดส่งและการเรียกเก็บเงิน ไซต์ และคลังสินค้า

## <a name="account-table"></a>ตารางบัญชี

1. ในคอลัมน์ **บริษัท** ให้ป้อนชื่อบริษัท เช่น **USMF**
2. ในคอลัมน์ **ชนิดความสัมพันธ์** ให้ป้อน **ลูกค้า** เป็นค่าคงที่ คุณอาจไม่ต้องการจัดประเภทเรกคอร์ดบัญชีทุกเรกคอร์ดเป็นลูกค้าในตรรกะธุรกิจของคุณ
3. ในคอลัมน์ **รหัสกลุ่มลูกค้า** ให้ป้อนหมายเลขกลุ่มลูกค้าจากแอปการเงินและการดำเนินงาน ค่าเริ่มต้นจากโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดเป็น **10**
4. ถ้าคุณใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดโดยไม่มีการกำหนดเองของ **หมายเลขบัญชี** ป้อนค่า **หมายเลขบัญชี** ในคอลัมน์ **หมายเลขฝ่าย** หากมีการเลือกกำหนด และคุณไม่ทราบหมายเลขฝ่าย ให้ดึงข้อมูลนี้จากแอปการเงินและการดำเนินงาน

## <a name="contact-table"></a>ตารางผู้ติดต่อ

1. ในคอลัมน์ **บริษัท** ให้ป้อนชื่อบริษัท เช่น **USMF**
2. ตั้งค่าคอลัมน์ต่อไปนี้ ตามค่า **IsActiveCustomer** ในไฟล์ CSV

    - ถ้า **IsActiveCustomer** ได้รับการตั้งค่าเป็น **ใช่** ในไฟล์ CSV ให้ตั้งค่าคอลัมน์ **ที่สามารถขายได้** เป็น **ใช่** ในคอลัมน์ **รหัสกลุ่มลูกค้า** ให้ป้อนหมายเลขกลุ่มลูกค้าจากแอปการเงินและการดำเนินงาน ค่าเริ่มต้นจากโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดเป็น **10**
    - ถ้า **IsActiveCustomer** ได้รับการตั้งค่าเป็น **ไม่** ในไฟล์ CSV ให้ตั้งค่าคอลัมน์ **ที่สามารถขายได้** เป็น **ไม่** และตั้งค่าคอลัมน์ **ผู้ติดต่อสำหรับ** เป็น **ลูกค้า**

3. ถ้าคุณจะใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดโดยไม่มีการกำหนดเองของ **หมายเลขผู้ติดต่อ** ให้ตั้งค่าคอลัมน์ต่อไปนี้

    - ย้ายหมายเลขผู้ติดต่อจากไฟล์ CSV (**msdynce\_contactnumber**) ไปยังหมายเลขผู้ติดต่อในตาราง **ผู้ติดต่อ** (**msdyn\_contactnumber**)
    - ใช้ค่าจากตาราง **หมายเลขผู้ติดต่อ** ในคอลัมน์ **หมายเลขฝ่าย**
    - ใช้ค่าจากตาราง **หมายเลขผู้ติดต่อ** ในคอลัมน์ **หมายเลขบัญชี/รหัสผู้ติดต่อ**

## <a name="invoice-table"></a>ตารางใบแจ้งหนี้

เนื่องจากข้อมูลจากตาราง **ใบแจ้งหนี้** ได้รับการออกแบบมาเพื่อส่งทางเดียวจากแอปการเงินและการดำเนินงานไปยังแอปการมีส่วนร่วมของลูกค้า การเริ่มต้นไม่จำเป็นต้องใช้ เรียกใช้การซิงโครไนส์แรกเริ่มเพื่อย้ายข้อมูลที่ต้องใช้ทั้งหมดจากแอปการเงินและการดำเนินงานไปยังแอปการมีส่วนร่วมของลูกค้า สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ข้อควรพิจารณาสำหรับการซิงโครไนส์เริ่มแรก](initial-sync-guidance.md)

## <a name="order-table"></a>ตารางใบสั่ง

1. ในคอลัมน์ **บริษัท** ให้ป้อนชื่อบริษัท เช่น **USMF**
2. คัดลอกค่าของคอลัมน์ **รหัสใบสั่ง** ในไฟล์ CSV ไปยังคอลัมน์ **หมายเลขใบสั่งขาย**
3. คัดลอกค่าของคอลัมน์ **ลูกค้า** ในไฟล์ CSV ไปยังคอลัมน์ **หมายเลขลูกค้าในใบแจ้งหนี้**
4. คัดลอกค่าของคอลัมน์ **จัดส่งไปยังประเทศ/ภูมิภาค** ในไฟล์ CSV ในคอลัมน์ **จัดส่งไปยังประเทศ/ภูมิภาค** ตัวอย่างของค่านี้ ได้แก่ **สหรัฐอเมริกา** และ **สหรัฐอเมริกา**
5. ตั้งค่าคอลัมน์ **วันที่ขอรับสินค้า** ถ้าคุณไม่ได้ใช้วันที่รับสินค้า ให้ใช้คอลัมน์ **วันที่จัดส่งที่ร้องขอ** **วันที่ปฏิบัติตาม** และ **วันที่ส่ง** ในไฟล์ CSV ตัวอย่างของค่านี้ได้แก่ **2020-03-27T00:00:00Z**
6. ตั้งค่าคอลัมน์ **ภาษา** ตัวอย่างของค่านี้ได้แก่ **en-us**
7. ตั้งค่าคอลัมน์ **ชนิดของใบสั่ง** โดยใช้คอลัมน์ **ตามสินค้า**

## <a name="order-products-table"></a>ตารางผลิตภัณฑ์ในใบสั่ง

- ในคอลัมน์ **บริษัท** ให้ป้อนชื่อบริษัท เช่น **USMF**

## <a name="products-table"></a>ตารางผลิตภัณฑ์

เนื่องจากข้อมูลจากตาราง **ผลิตภัณฑ์** ได้รับการออกแบบมาเพื่อส่งทางเดียวจากแอปการเงินและการดำเนินงานไปยังแอปการมีส่วนร่วมของลูกค้า การเริ่มต้นไม่จำเป็นต้องใช้ เรียกใช้การซิงโครไนส์แรกเริ่มเพื่อย้ายข้อมูลที่ต้องใช้ทั้งหมดจากแอปการเงินและการดำเนินงานไปยังแอปการมีส่วนร่วมของลูกค้า สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ข้อควรพิจารณาสำหรับการซิงโครไนส์เริ่มแรก](initial-sync-guidance.md)

## <a name="quote-and-quote-product-tables"></a>ตารางใบเสนอราคาและผลิตภัณฑ์ในใบเสนอราคา

สำหรับตาราง **ใบเสนอราคา** ให้ปฏิบัติตามคําแนะนําในส่วน [ตารางใบสั่ง](#order-table) ซึ่งอธิบายไว้ก่อนหน้านี้ในบทความนี้ สำหรับตาราง **ผลิตภัณฑ์ในใบเสนอราคา** ให้ปฏิบัติตามคําแนะนําในส่วน [ตารางผลิตภัณฑ์ในใบเสนอราคา](#order-products-table)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

