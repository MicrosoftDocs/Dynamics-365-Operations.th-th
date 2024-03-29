---
title: ตั้งค่าคอนฟิกการชำระเงิน
description: วิธีและเวลาที่มีการชำระธุรกรรมอาจเป็นเรื่องซับซ้อน ดังนั้นคุณจำเป็นต้องเข้าใจ และกำหนดพารามิเตอร์เพื่อตอบสนองความต้องการทางธุรกิจของคุณอย่างถูกต้อง บทความนี้อธิบายพารามิเตอร์ที่ใช้สำหรับการชำระบัญชีสำหรับทั้งบัญชีเจ้าหนี้และบัญชีลูกหนี้
author: angelad116
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0aae3d72d35e8c09b2a3dc8d25958be4c523969
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151864"
---
# <a name="configure-settlement"></a>ตั้งค่าคอนฟิกการชำระเงิน

[!include [banner](../includes/banner.md)]

วิธีและเวลาที่มีการชำระธุรกรรมอาจเป็นเรื่องซับซ้อน ดังนั้นคุณจำเป็นต้องเข้าใจ และกำหนดพารามิเตอร์เพื่อตอบสนองความต้องการทางธุรกิจของคุณอย่างถูกต้อง บทความนี้อธิบายพารามิเตอร์ที่ใช้สำหรับการชำระบัญชีสำหรับทั้งบัญชีเจ้าหนี้และบัญชีลูกหนี้ 

พารามิเตอร์ต่อไปนี้ส่งผลต่อวิธีการประมวลผลการชำระบัญชีใน Microsoft Dynamics 365 Finance การชำระเงินเป็นกระบวนการชำระใบแจ้งหนี้เปรียบเทียบกับการชำระเงินหรือใบลดหนี้ พารามิเตอร์เหล่านี้จะอยู่ใน **พื้นที่ชำระ** ของ **หน้าพารามิเตอร์ลูกหนี้** และ **พารามิเตอร์บัญชีเจ้าหนี้**

- **การชำระเงินอัตโนมัติ**– ตั้งค่าตัวเลือกนี้ไปยัง **ใช่** ธุรกรรมหนึ่งควรจะจับคู่โดยอัตโนมัติกับธุรกรรมเปิดอื่นๆ เมื่อมีการลงรายการบัญชี ถ้าตัวเลือกนี้ถูกกำหนดเป็น **ไม่ใช่** ผู้ใช้สามารถชำระธุรกรรมด้วยตนเอง เมื่อพวกเขาป้อนการชำระเงิน หรือภายหลัง โดยการใช้หน้า **ธุรกรรมการชำระเงิน** ได้
- **การจัดการส่วนลดเงินสด** – ระบุวิธีการ [จัดการส่วนลดเงินสดเมื่อมีการชำระใบแจ้งหนี้เกิน](cash-discount-handling-overpayments.md). สำหรับการชำระมากเกิน ก็สามารถหักส่วนลดเงินสด สามารถถือเป็นผลต่าง หรือคงอยู่ในบัญชีสำหรับผู้จัดจำหน่ายหรือลูกค้า
  -   **ไม่ระบุ**– ยอดส่วนลดเงินสดจะลดลงตามยอดเงินชำระมากเกิน ลักษณะการทำงานนี้จะถูกใช้ ไม่ว่ายอดเงินชำระจะมากเกิน หรือต่ำกว่าปริมาณที่ป้อนไว้ใน **ฟิลด์การชำระเงินมากเกินหรือน้อยเกิน**
  -   **ระบุ** – ยอดเงินชำระมากเกินที่ลงรายการบัญชีผลต่างของส่วนลดเงินสด หรือยอดดุลคงเหลือในบัญชีของลูกค้า หรือผู้จัดจำหน่าย ลักษณะการทำงานแบบเจาะจงนั้นขึ้นอยู่กับยอดเงินชำระมากเกินอยู่ระหว่าง 0.00 กับยอดเงินที่ป้อนไว้ในฟิลด์ **การชำระเงินมากเกินหรือน้อยเกินสูงสุด** หรือยอดเงินชำระมากเกินมากกว่ายอดเงินของ **การชำระเงินมากเกินหรือน้อยเกินสูงสุด** หรือไม่
- **ผลต่างเศษสตางค์สูงสุด**– ป้อนผลต่างเศษสตางค์สูงสุดที่อนุญาตสำหรับธุรกรรมที่ชำระบัญชีแล้ว ถ้าผลต่างเศษสตางค์เท่ากับหรือน้อยกว่าผลต่างเศษสตางค์ที่ระบุไว้ในฟิลด์นี้ ผลต่างนี้จะถูกนำมาลงในรายการบัญชีแยกประเภทซึ่งระบุไว้ในหน้า **บัญชีเพื่อการทำธุรกรรมโดยอัตโนมัติ** ได้
- **ยอดชำระเงินมากเกินหรือน้อยเกินสูงสุด**– ป้อนยอดเงินที่ยอมรับสำหรับการชำระเงินมากเกินหรือน้อยเกินไป เพื่อคำนวณภาษีของการชำระเงินมากเกินหรือน้อยเกิน **ในหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป** คลิก **ภาษีขาย** แล้ว เลือก **ภาษีขายด้วยตัวเลือกการชำระเงินมากเกินหรือน้อยเกิน**
  -   ถ้าการชำระเงินมากเกินหรือน้อยเกินก่อให้เกิดผลต่างที่น้อยกว่าผลต่างที่กำหนดไว้ในฟิลด์ **ผลต่างษสตางค์** ยอดเงินผลต่างเศษสตางค์นั้นจะถูกลงไว้ในบัญชีผลต่างเศษสตางค์
  -   ถ้าการชำระเงินมากเกินหรือน้อยเกินก่อให้เกิดผลต่างเศษสตางค์ที่มากกว่าผลต่างที่กำหนดไว้ใน **ฟิลด์ยอดเงินผลต่างเศษสตางค์** ยอดเงินผลต่างนั้นจะนำมาลงไว้ในบัญชีผลต่างที่เลือกเพื่อ **การลงรายการบัญชีของลูกค้า** หรือ **ส่วนลดเงินสดของผู้จัดจำหน่าย** ใน **บัญชีสำหรับหน้าธุรกรรมอัตโนมัติ** นั้น
- **คำนวณส่วนลดเงินสดสำหรับการชำระเงินบางส่วน** – ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อเปิดใช้งานส่วนลดเงินสดซึ่งจะถูกคำนวณการชำระเงินบางส่วนโดยอัตโนมัติ
  -   ผลกระทบของตัวเลือกนี้ขึ้นอยู่กับค่าของ **การใช้ส่วนลดเงินสด** ใน **หน้าฟิลด์ธุรกรรมการชำระเงิน** นั้น ถ้าตัวเลือกนี้ถูกกำหนดเป็น **ใช่** ส่วนลดจะได้มาเมื่อ **การใช้ฟิลด์ส่วนลดเงินสด** ถูกตั้งค่าเป็น **ปกติ** เมื่อการ **ใช้ฟิลด์ส่วนลดเงินสด** ถูกกำหนดเป็น **เสมอ** ส่วนลดเงินสดจะใช้เสมอ โดยไม่คำนึงถึงการตั้งค่าฟิลด์นี้ เมื่อฟิลด์ **ใช้ส่วนลดเงินสด** ถูกตั้งเป็น **ไม่เคย** หมายความว่าไม่เคยใช้ส่วนลดเงินสด โดยไม่เกี่ยวข้องกับการตั้งค่าในฟิลด์นี้
  -   ถ้าตัวเลือกนี้ตั้งค่าไปยัง **ใช่** และผู้ใช้เปลี่ยนค่า **ยอดเงินที่จะชำระ** เพื่อตั้งค่าฟิลด์ **ในหน้าธุรกรรมการชำระเงิน** ส่วนลดจะถูกคำนวณ และแสดงเป็นรายการเริ่มต้นในการใช้ **ฟิลด์ยอดส่วนลดเงินสด** โดยอัตโนมัติ
  -   ถ้าตัวเลือกนี้ตั้งค่าไปยัง **ไม่** และผู้ใช้เปลี่ยนค่า **ยอดเงินที่จะชำระ** เพื่อตั้งค่าฟิลด์ **ในหน้าธุรกรรมการชำระเงิน** ส่วนลดจะถูกคำนวณ และแสดงเป็นรายการเริ่มต้นในการใช้ **ฟิลด์ยอดส่วนลดเงินสด** เป็น **0** (ศูนย์)
- **คำนวณส่วนลดเงินสดสำหรับใบลดหนี้**– ตั้งค่าตัวเลือกนี้ไปยัง **ใช่** เพื่อคำนวณส่วนลดเงินสดสำหรับใบลดหนี้โดยอัตโนมัติ ในบัญชีลูกหนี้ ใบลดหนี้ธุรกรรมเป็นธุรกรรมค่าลบที่มีค่าใน **ฟิลด์ใบแจ้งหนี้** ใน **หน้าใบแจ้งหนี้ข้อความอิสระ** หรือส่งคืนไปยัง **หน้าใบสั่งขาย**
  - ผลกระทบของตัวเลือกนี้ขึ้นอยู่กับค่าของ <strong>การใช้ส่วนลดเงินสด</strong> ใน <strong>หน้าฟิลด์ธุรกรรมการชำระเงิน</strong> นั้น ถ้าตัวเลือกนี้ถูกกำหนดเป็น <strong>ใช่</strong> ส่วนลดจะได้มาเมื่อฟิลด์ *<strong><em>ใช้ส่วนลดเงินสด</em></strong>* ถูกตั้งค่าเป็น <strong>ปกติ</strong> เมื่อฟิลด์ *<strong><em>ใช้ส่วนลดเงินสด</em></strong>* ถูกกำหนดเป็น <strong>เสมอ</strong> จะมีการใช้ส่วนลดเงินสดเสมอ โดยไม่เกี่ยวข้องกับการตั้งค่าในฟิลด์นี้ เมื่อฟิลด์ *<strong><em>ใช้ส่วนลดเงินสด</em></strong>* ถูกกำหนดเป็น <strong>ไม่เคย</strong> หมายความว่าไม่เคยใช้ส่วนลดเงินสด โดยไม่เกี่ยวข้องกับการตั้งค่าในฟิลด์นี้
  - ถ้าตัวเลือกนี้ตั้งค่าไปยัง **ใช่** และใบลดหนี้ถูกทำเครื่องหมายใน **หน้าธุรกรรมการชำระเงิน** ส่วนลดจะคำนวณ และจะแสดงเป็นรายการเริ่มต้นใน **ฟิลด์ยอดส่วนลดเงินสดที่จะใช้** ได้
  - ถ้าตัวเลือกนี้ตั้งค่าไปยัง **ไม่** และใบลดหนี้ถูกทำเครื่องหมายใน **หน้าธุรกรรมการชำระเงิน** ส่วนลดจะคำนวณและจะแสดงเป็นรายการเริ่มต้นใน **ฟิลด์ยอดส่วนลดเงินสดที่ใช้** จะเป็น **0** (ศูนย์)

- **บัญชีตรงข้ามส่วนลด (AP เท่านั้น)** – กำหนดรหัสบัญชีส่วนลดเงินสดเริ่มต้นที่ควรใช้สำหรับรายการบัญชีส่วนลดเงินสด
  -   **ใช้บัญชีหลักสำหรับส่วนลดของผู้จัดจำหน่าย** – ส่วนลดเงินสดลงรายการบัญชีไปยังบัญชีหลักที่กำหนดไว้ใน **หน้าการตั้งค่าส่วนลดเงินสด**
  -   **บัญชีในรายการใบแจ้งหนี้**– ส่วนลดเงินสดจะถูกลงรายการบัญชีในบัญชีแยกประเภทในใบแจ้งหนี้ต้นฉบับ
- **เครื่องหมายรายการในใบแจ้งหนี้ข้อความอิสระและดอกเบี้ยตั๋วเงิน (AR เท่านั้น)** – ตั้งค่าตัวเลือกนี้ไปยัง **ใช่** เพื่อเปิดใช้งาน **ปุ่มเครื่องหมายรายการใบแจ้งหนี้** ใน **หน้าการป้อนการชำระเงินของลูกค้า** , **ใบสำคัญสมุดรายวันการชำระเงิน** และ **ธุรกรรมการชำระเงิน** ปุ่มนี้ช่วยให้ผู้ใช้ทำเครื่องหมายสำหรับการชำระเงินแต่ละรายการ
- **จัดระดับความสำคัญของการชำระเงิน (AR เท่านั้น)** – ตั้งค่าตัวเลือกนี้ไปยัง **ใช่** เพื่อเปิดใช้งาน **ปุ่มทำเครื่องหมายตามระดับความสำคัญ** ใน **หน้าการป้อนการชำระเงินลูกค้า** และ **ธุรกรรมการชำระเงิน** ปุ่มนี้ช่วยให้ผู้ใช้ที่กำหนดใบสั่งการชำระเงินล่วงหน้ากับธุรกรรม  หลังจากที่มีการใช้ใบสั่งชำระเงินของธุรกรรมแล้ว ใบสั่งและการปันส่วนการชำระเงินสามารถปรับเปลี่ยนได้ก่อนการลงรายการบัญชี
- **ใช้ระดับความสำคัญสำหรับการชำระเงินอัตโนมัติ** – ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อลำดับความสำคัญที่กำหนดเมื่อธุรกรรมต่างๆได้ชำระโดยอัตโนมัติ ฟิลด์นี้จะพร้อมใช้งานได้ถ้าตัวเลือก **การจัดระดับความสำคัญของการชำระเงิน** และ **การชำระเงินอัตโนมัติ** ถูกกำหนดให้เป็น **ใช่**

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>มิติคงที่ในบัญชีหลักของบัญชีลูกหนี้/บัญชีเจ้าหนี้

เมื่อมีการใช้มิติคงที่ในบัญชีหลักของบัญชีลูกหนี้/บัญชีเจ้าหนี้ รายการบัญชีเพิ่มเติม และธุรกรรมผู้จัดจำหน่ายเพิ่มเติมสองรายการ จะถูกลงรายการบัญชีตามกระบวนการชำระเงิน การชำระเงินเปรียบเทียบบัญชีแยกประเภทของบัญชีลูกหนี้/บัญชีเจ้าหนี้จากใบแจ้งหนี้ และการชำระเงิน  เมื่อการชำระเงินและการตัดจ่ายใบแจ้งหนี้เสร็จสมบูรณ์พร้อมกัน ซึ่งเป็นสถานการณ์ทั่วไป รายการบัญชีของการชำระเงินไม่ได้ถูกลงรายการไปยังบัญชีแยกประเภททั่วไป จนถึงหลังจากกระบวนการตัดจ่ายใบแจ้งหนี้เสร็จสมบูรณ์เช่นกัน เนื่องจากใบสั่งของเหตุการณ์การประมวลผล การชำระเงินไม่สามารถกำหนดบัญชีแยกประเภทของบัญชีลูกหนี้/บัญชีเจ้าหนี้จริงจากรายการบัญชีของการชำระเงินได้ การชำระเงินปรับโครงสร้างบัญชีแยกประเภทที่จะใช้สำหรับการชำระเงิน นี่จะกลายเป็นปัญหา เมื่อมีการใช้มิติคงที่สำหรับบัญชีหลักของบัญชีลูกหนี้/บัญชีเจ้าหนี้

เมื่อต้องการปรับโครงสร้างบัญชีแยกประเภท บัญชีหลักของบัญชีลูกหนี้/บัญชีเจ้าหนี้จะถูกดึงมาจากโพรไฟล์การลงรายการบัญชี และมิติทางการเงินจะถูกดึงมาจากเรกคอร์ดธุรกรรมผู้จัดจำหน่ายสำหรับการชำระเงิน ตามที่กำหนดไว้ในสมุดรายวันการชำระเงิน มิติคงที่ไม่ได้เป็นค่าเริ่มต้นในสมุดรายวันการชำระเงิน แต่จะใช้กับบัญชีหลักเป็นขั้นตอนสุดท้ายของกระบวนการลงรายการบัญชีแทน ดังนั้น ค่ามิติคงที่เป็นไปได้ที่จะไม่มีอยู่ในธุรกรรมผู้จัดจำหน่าย ยกเว้นว่าเป็นค่าเริ่มต้นจากแหล่งอื่น เช่น ผู้จัดจำหน่าย บัญชีที่ปรับโครงสร้างจะไม่รวมมิติคงที่ การประมวลผลการชำระเงินจะกำหนดว่า การปรับปรุงรายการต้องถูกสร้าง เนื่องจากใบแจ้งหนี้ลงรายการบัญชีด้วยค่ามิติคงที่ และบัญชีการชำระเงินที่ปรับโครงสร้างไม่มี  เนื่องจากการชำระเงินยังคงมีการลงรายการบัญชีการปรับปรุงรายการต่อไป ขั้นตอนสุดท้ายในการลงรายการบัญชีคือ สำหรับสำหรับมิติคงที่ที่จะถูกนำไปใช้ โดยการเพิ่มมิติคงที่ไปยังการปรับปรุงรายการ จะมีการลงรายการบัญชีด้วยเดบิตและเครดิตในบัญชีแยกประเภทเดียวกัน การชำระเงินไม่สามารถย้อนกลับรายการบัญชีได้

เพื่อหลีกเลี่ยงรายการบัญชีเพิ่มเติม เดบิตและเครดิตในบัญชีแยกประเภทเดียวกัน การแก้ปัญหาต่างๆ ต่อไปนี้ควรได้รับการพิจารณา โดยขึ้นอยู่กับความต้องการทางธุรกิจของคุณ 

-   องค์กรมักจะใช้มิติคงที่เพื่อเติมศูนย์ในมิติทางการเงินที่ไม่จำเป็น นี่เป็นกรณีทั่วไปสำหรับบัญชีงบดุล เช่น บัญชีลูกหนี้/บัญชีเจ้าหนี้ โครงสร้างทางบัญชีสามารถใช้ในการติดตามมิติทางการเงิน ซึ่งโดยปกติแล้วจะถูกเติมเป็นศูนย์  คุณสามารถลบมิติทางการเงินสำหรับบัญชีงบดุลได้ โดยไม่จำเป็นต้องใช้มิติคงที่
-   ถ้าองค์กรของคุณต้องใช้มิติคงที่ในบัญชีหลักของบัญชีลูกหนี้/บัญชีเจ้าหนี้ ค้นหาวิธีในการตั้งค่ามิติคงที่เริ่มต้นในการชำระเงิน เพื่อให้มีการจัดเก็บค่ามิติคงที่ในธุรกรรมผู้จัดจำหน่ายสำหรับการชำระเงิน ซึ่งจะอนุญาตให้ระบบสร้างบัญชีหลักของบัญชีลูกหนี้/บัญชีเจ้าหนี้เพื่อรวมค่ามิติคงที่ คุณสามารถกำหนดค่ามิติคงที่เป็นค่าเริ่มต้นในผู้จัดจำหน่ายหรือชื่อสมุดรายวัน อย่างใดอย่างหนึ่ง สำหรับสมุดรายวันการชำระเงิน


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
