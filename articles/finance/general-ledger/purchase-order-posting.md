---
title: การลงรายการบัญชีใบสั่งซื้อ
description: บทความนี้อธิบายแท็บใบสั่งซื้อของหน้าโปรไฟล์การลงบัญชีสินค้าคงคลัง
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 38a9e2740232b18255109ba867fcdddd5b890774
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151046"
---
# <a name="purchase-order-posting"></a>การลงรายการบัญชีใบสั่งซื้อ

แท็บ **ใบสั่งซื้อ** บนหน้า **โปรไฟล์การลงรายการบัยชีสินค้าคงคลัง** ใช้เพื่อควบคุมวิธีการลงรายการบัญชีใบสั่งซื้อในบัญชีแยกประเภททั่วไป กิจกรรมหลักสองกิจกรรมจะลงรายการบัญชีในบัญชีแยกประเภททั่วไปสำหรับใบสั่งซื้อ: 

- ใบรับสินค้า
- ใบแจ้งหนี้

เพื่อให้ธุรกรรมที่เกิดขึ้นจริง (ใบรับสินค้า) สามารถลงรายการบัญชีในบัญชีแยกประเภททั่วไปสำหรับใบสั่งซื้อได้ ต้องเลือกกล่องกาเครื่องหมายต่อไปนี้

- กล่องกาเครื่องหมาย **ลงรายการบัญชีใบรับสินค้าในบัญชีแยกประเภท** บนหน้า **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า**
- กล่องกาเครื่องหมาย **ลงรายการบัญชีสินค้าคงคลังที่มีอยู่จริง** และ **บันทึกหนี้สินค้างจ่ายของใบรับสินค้า** บนหน้า **กลุ่มแบบจำลองสินค้า**

คุณต้องระบุบัญชีหลักในหน้า **โปรไฟล์การลงบัญชีสินค้าคงคลัง** สำหรับชนิดการลงรายการบัญชีต่อไปนี้

- ได้รับต้นทุนของวัสดุที่ซื้อแล้ว
- รายจ่ายการซื้อ ยังไม่ได้ออกใบแจ้งหนี้
- การซื้อ, รายการคงค้าง

สำหรับธุรกรรมทางการเงิน (ใบแจ้งหนี้) ที่จะลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปสำหรับใบสั่งซื้อ ต้องเป็นไปตามเงื่อนไขต่อไปนี้:

- ต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีสินค้าคงคลังทางการเงิน** ในหน้า **กลุ่มแบบจำลองสินค้า** ของสินค้าที่เลือกในรายการใบสั่งซื้อ
- คุณต้องระบุบัญชีหลักในหน้า **โปรไฟล์การลงบัญชีสินค้าคงคลัง** สำหรับชนิดการลงรายการบัญชีต่อไปนี้
  - ออกใบแจ้งหนี้ต้นทุนของวัสดุที่ซื้อแล้ว
  - รายจ่ายการซื้อสำหรับผลิตภัณฑ์
  - รายจ่ายการซื้อสำหรับค่าใช้จ่าย
  - ส่วนลด (ไม่บังคับ)

## <a name="fixed-receipt-price-posting"></a>การลงรายการบัญชีราคาการรับสินค้าแบบคงที่

คุณสามารถใช้ราคาการรับสินค้าแบบคงที่เป็นต้นทุนมาตรฐานของผลิตภัณฑ์แทนการเลือกตัวเลือก **ต้นทุนมาตรฐาน** ในฟิลด์ **แบบจำลองสินค้าคงคลัง** ในหน้า **กลุ่มแบบจำลองสินค้า** ของสินค้า ผลต่างหลักคือ เมื่อใช้ **ราคาการรับสินค้าแบบคงที่** ราคาต้นทุนปัจจุบันจะถูกใช้กับสินค้าเมื่อมีการลงรายการบัญชีการรับสินค้าคงคลัง ไม่มีกระบวนการประเมินค่าต้นทุนใหม่สำหรับ **ราคาการรับสินค้าแบบคงที่** เมื่อมีการลงรายการบัญชีการอัปเดตทางการเงิน จะมีการใช้ราคาต้นทุนปัจจุบันเมื่อลงรายการบัญชี ถ้ามีความแตกต่างระหว่างราคาต้นทุนที่ใช้เมื่อรับสินค้าและใบแจ้งหนี้ ผลต่างจะลงรายการบัญชีในบัญชีกําไรขาดทุนของราคาการรับสินค้าแบบคงที่

เมื่อต้องการใช้ราคาการรับสินค้าแบบคงที่กับผลิตภัณฑ์ คุณต้องตั้งค่าคอนฟิกต่อไปนี้

- บนหน้า **กลุ่มแบบจำลองสินค้า** เลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีสินค้าคงคลังที่มีอยู่จริง** และ **ราคาการรับสินค้าแบบคงที่** 
- บนหน้า **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** เลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีบันทึกการจัดส่งในบัญชีแยกประเภท**
- บนหน้า **โปรไฟล์การลงบัญชีสินค้าคงคลัง** ระบุบัญชีหลักในชนิดการลงรายการบัญชีต่อไปนี้
  - กำไรจากราคาการรับสินค้าแบบคงที่
  - ขาดทุนจากราคาการรับสินค้าแบบคงที่
  - ออฟเซ็ตราคาการรับสินค้าแบบคงที่

สำหรับข้อมูลเพิ่มเติม ให้ไปที่ [ราคาการรับสินค้าแบบคงที่](/supply-chain/cost-management/fixed-receipt-price.md)

## <a name="purchase-charges-and-stock-variation-posting"></a>ค่าธรรมเนียมการซื้อและการลงรายการบัญชีการเปลี่ยนแปลงสินค้าคงคลัง

หากคุณวางแผนที่จะลงบัญชีสำหรับค่าธรรมเนียมการซื้อและการเปลี่ยนแปลงของสินค้าคงคลัง ดำเนินการขั้นตอนต่อไปนี้:

- บนหน้า **พารามิเตอร์บัญชีเจ้าหนี้** บนแท็บ **ใบแจ้งหนี้** เลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีค่าใช้จ่ายในบัญชีแยกประเภท**
- บนหน้า **กลุ่มแบบจำลองสินค้า** ของสินค้าที่เลือกบนรายการใบสั่งซื้อ ให้เลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีสินค้าคงคลังที่มีอยู่จริง** **ลงรายการบัญชีสินค้าคงคลังทางการเงิน** และ **บันทึกหนี้สินค้างจ่ายของใบรับสินค้า**
- บนหน้า **พารามิเตอร์การจัดซื้อและการจัดหา** ให้เลือกกล่องกาเครื่องหมาย **สร้างค่าธรรมเนียมบนใบรับสินค้า**
- บนหน้า **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** เลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีบันทึกการจัดส่งในบัญชีแยกประเภท**

บนหน้า **โปรไฟล์การลงบัญชีสินค้าคงคลัง** คุณต้องระบุบัญชีหลักในชนิดการลงรายการบัญชีต่อไปนี้

- รายจ่ายการซื้อ ยังไม่ได้ออกใบแจ้งหนี้
- รายจ่ายการซื้อสำหรับผลิตภัณฑ์
- การเปลี่ยนแปลงสินค้าคงคลัง

> [!NOTE]
> ชนิดการลงรายการบัญชี **ค่าธรรมเนียม** ไม่ได้ใช้เมื่อเลือกพารามิเตอร์ **ลงรายการบัญชีค่าใช้จ่ายในบัญชีแยกประเภท**

สำหรับข้อมูลเพิ่มเติม ไปที่ [หลักการบัญชีสำหรับลงรายการบัญชีค่าใช้จ่าย](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md)

## <a name="sample-posting-profile-configuration"></a>การตั้งค่าคอนฟิกโพรไฟล์การลงรายการบัญชีตัวอย่าง

ตารางต่อไปนี้แสดงตัวอย่างของชนิดการลงรายการบัญชีเริ่มต้นพร้อมด้วยบัญชีหลักและคำอธิบายตัวอย่าง:

- คอลัมน์ **บัญชีรอการโอน** แสดงว่าชนิดบัญชีเป็นบัญชีรอการโอน ยอดเงินที่ลงรายการบัญชีในบัญชีนี้จะถูกกลับรายการโดยอัตโนมัติเมื่อลงรายการบัญชีธุรกรรมในภายหลัง 
- คอลัมน์ **P/F** แสดง **P** สำหรับการลงรายการบัญชีและ **F** สำหรับการลงรายการบัญชีทางการเงิน 
- คอลัมน์ **ตามอย่าง** ระบุว่าบัญชีหลักสำหรับการลงรายการบัญชีประเภทใดประเภทหนึ่งมักเหมือนกับการลงรายการบัญชีประเภทอื่นหรือไม่ ค่าในคอลัมน์จะแสดงชนิดของการลงรายการบัญชีที่ใช้กันโดยทั่วไป

> [!NOTE]
> บัญชีหลักและชื่อบัญชีหลักเหล่านี้เป็นการแนะนำเท่านั้น เราแนะนำ<!--note from editor: Via Writing Style Guide.--> ให้คุณทำงานร่วมกับนักบัญชีเพื่อตั้งค่าคอนฟิกที่ดีที่สุดสำหรับความต้องการทางธุรกิจของคุณ


| ชนิดการลงรายการบัญชี | ตัวอย่างบัญชีหลัก | ตัวอย่างชื่อบัญชีหลัก | ชนิดบัญชี | เดบิต/เครดิตหรือไม่ | บัญชีรอการโอน | P/F | ตามอย่าง | คำอธิบาย |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| ได้รับต้นทุนของวัสดุที่ซื้อแล้ว | 140100</br>140101 | สินค้าคงคลังวัสดุ</br>วัสดุที่จัดส่งแล้วแต่ยังไม่ได้ออกใบแจ้งหนี้ | แอสเซท | เดบิต | ใช่ | P | ออกใบแจ้งหนี้ต้นทุนของวัสดุที่ซื้อแล้ว | ใช้เมื่อลงรายการบัญชีใบรับสินค้าตามใบสั่งซื้อ การออฟเซ็ตไปยังบัญชีเป็นรายจ่ายการซื้อ ยังไม่ได้ออกใบแจ้งหนี้ ยอดเงินในบัญชีนี้จะกลับรายการเมื่อมีการลงรายการบัญชีใบแจ้งหนี้ของใบสั่งซื้อ |
| รายจ่ายการซื้อ ยังไม่ได้ออกใบแจ้งหนี้ | 600180 | ใบรับวัสดุ | ค่าใช้จ่าย | เดบิต | ใช่ | P | |ใช้เมื่อมีการลงรายการบัญชีใบรับสินค้าตามใบสั่งซื้อ ใบสำคัญสองใบจะถูกสร้างขึ้นเพื่อให้การรับสินค้าติดตามผลต่างของราคาซื้อเมื่อมีการใช้ต้นทุนมาตรฐาน ออฟเซ็ตของบัญชีในใบสำคัญแรกคือรายการคงค้างของการซื้อ ออฟเซ็ตของใบสำคัญที่สองคือผลรวมของบัญชี ต้นทุนของวัสดุที่ซื้อที่ได้รับ และบัญชีผลต่างราคาซื้อ ยอดเงินที่ลงรายการบัญชีไว้ในบัญชีนี้จะกลับรายการเมื่อมีการลงรายการบัญชีใบแจ้งหนี้ของใบสั่งซื้อ |
| ออกใบแจ้งหนี้ต้นทุนของวัสดุที่ซื้อแล้ว | 140100 | สินค้าคงคลังวัสดุ | แอสเซท | เดบิต | ไม่ | ศ.  |ได้รับต้นทุนของวัสดุที่ซื้อแล้ว | ใช้เมื่อลงรายการบัญชีใบแจ้งหนี้ของใบสั่งซื้อ ออฟเซ็ตของบัญชีนี้คือ รายจ่ายการซื้อสำหรับผลิตภัณฑ์ บัญชีนี้แสดงถึงสินค้าคงคลังในงบดุลของคุณ โดยทั่วไป บัญชีที่ใช้จะเป็นบัญชีเดียวกับที่ใช้กับต้นทุนของหน่วยที่จัดส่งและต้นทุนของหน่วยที่ออกใบแจ้งหนี้แล้วในใบสั่งขาย |
| รายจ่ายการซื้อสำหรับผลิตภัณฑ์ | 600180 | ใบรับวัสดุ | ค่าใช้จ่าย | เครดิต | ใช่ | ศ.  | |ใช้เมื่อลงรายการบัญชีใบแจ้งหนี้ของใบสั่งซื้อ ใบสำคัญสองใบจะถูกสร้างขึ้นเพื่อให้ใบแจ้งหนี้ติดตามผลต่างของราคาซื้อ เมื่อมีการใช้ต้นทุนมาตรฐาน บัญชีตรงข้ามของบัญชีนี้เป็นบัญชีรายจ่ายการซื้อ ซึ่งยังไม่ได้ออกใบแจ้งหนี้ ซึ่งใช้ในการลงรายการบัญชีการรับสินค้า และกลับรายการระหว่างการลงรายการบัญชีใบแจ้งหนี้ แสดงต้นทุนของสินค้าคงคลังที่ซื้อเมื่อออกใบแจ้งหนี้ ซึ่งไม่สะท้อนให้เห็นในบัญชีสินค้าคงคลังในงบดุล นี่เป็นการลงรายการบัญชีกําไรขาดทุนของผลต่างราคาซื้อ ที่โดยทั่วไปพบในการซื้อสินค้าต้นทุนมาตรฐาน|
| กําไรจากราคาการรับสินค้าแบบคงที่ (กําไรจากการซื้อ กําไรจากราคาการรับสินค้าแบบคงที่*) | 510310 | ผลต่างราคาซื้อ | ค่าใช้จ่าย | เครดิต | ไม่ | ศ. | ขาดทุนจากราคาการรับสินค้าแบบคงที่ | ใช้เมื่อลงรายการบัญชีใบแจ้งหนี้ของใบสั่งซื้อ และมีความแตกต่างกันระหว่างราคาที่ออกใบแจ้งหนี้และต้นทุนเริ่มต้นของสินค้า บัญชีนี้จะใช้เมื่อผลต่างสูงกว่า ออฟเซ็ตของบัญชีนี้คือออฟเซ็ตราคาการรับสินค้าแบบคงที่ |
| ขาดทุนจากราคาการรับสินค้าแบบคงที่ (ขาดทุนจากการซื้อ ขาดทุนจากราคาการรับสินค้าแบบคงที่*) | 510310 | ผลต่างราคาซื้อ | ค่าใช้จ่าย | เดบิต | ไม่ | ศ. | กำไรจากราคาการรับสินค้าแบบคงที่ | ใช้เมื่อลงรายการบัญชีใบแจ้งหนี้ของใบสั่งซื้อ และมีความแตกต่างกันระหว่างราคาที่ออกใบแจ้งหนี้และต้นทุนเริ่มต้นของสินค้า บัญชีนี้จะใช้เมื่อผลต่างต่ำกว่า ออฟเซ็ตของบัญชีนี้คือออฟเซ็ตราคาการรับสินค้าแบบคงที่ |
| ออฟเซ็ตจากราคาการรับสินค้าแบบคงที่ (ออฟเซ็ตจากการซื้อ ออฟเซ็ตจากราคาการรับสินค้าแบบคงที่*) | 140900 | การเปลี่ยนแปลงสินค้าคงคลัง | แอสเซท | ทั้งสองรายการ | ไม่ | ศ.  | |ใช้เมื่อลงรายการบัญชีใบแจ้งหนี้ของใบสั่งซื้อ และมีความแตกต่างกันระหว่างราคาที่ออกใบแจ้งหนี้และต้นทุนเริ่มต้นของสินค้า บัญชีนี้คือออฟเซ็ตของบัญชีกำไรและขาดทุนจากราคาการรับสินค้าแบบคงที่ |
| ค่าธรรมเนียม | ไม่ระบุ | ไม่ระบุ | ไม่ระบุ | ไม่ระบุ | ไม่ระบุ | ไม่ระบุ | ไม่ระบุ | บัญชีนี้จะไม่ได้ใช้อีกต่อไป ใช้การเปลี่ยนแปลงสินค้าคงคลังแทน |
| การเปลี่ยนแปลงสินค้าคงคลัง | 600170 | การเปลี่ยนแปลงสินค้าคงคลัง | ค่าใช้จ่าย | เครดิต | ไม่ | ทั้งสองรายการ | | บัญชีนี้จะใช้เมื่อ <ul><li>มีความแตกต่างในราคาต่อหน่วยระหว่างใบรับสินค้าและใบแจ้งหนี้</li><li>มีการลงรายการบัญชีค่าธรรมเนียมไปยังสินค้า</li><li>ต้นทุนทางอ้อม<!--note from editor: Edit okay?--> เพิ่มให้กับสินค้าที่ซื้อแล้ว </li><li>ออฟเซ็ตของบัญชีนี้คือ บัญชีรายจ่ายการซื้อ ยังไม่ได้ออกใบแจ้งหนี้</li></ul> |
| การซื้อ, รายการคงค้าง | 200140 | การซื้อที่คงค้าง | หนี้สิน | เครดิต | Y | P | |ใช้เมื่อลงรายการบัญชีใบรับสินค้าตามใบสั่งซื้อ และเปิดใช้งานตัวเลือกในการรับรู้จํานวนเงินการซื้อ |
| ภาษีขายคงค้างเมื่อรับสินค้า | 250500 | ภาษีขายคงค้าง | หนี้สิน | เครดิต | Y | ทั้งสองรายการ  | |บัญชีนี้จะใช้เมื่อคุณเลือกตัวเลือก **ลงรายการบัญชีภาษีจริง** ใน **พารามิเตอร์การบริหารสินค้าคงคลังและคลังสินค้า** และคุณมีใบสั่งซื้อที่มีภาษี ยอดเงินจะถูกลงรายการบัญชีเมื่อคุณอัปเดตใบสั่งซื้อจริง (ใบรับสินค้า) และกลับรายการเมื่อคุณลงรายการบัญชีใบสั่งซื้อทางการเงิน (ใบแจ้งหนี้) |
| การรับสินทรัพย์ถาวร (เดบิตสินทรัพย์ถาวร*) | 180100 | สินทรัพย์ถาวรที่มีตัวตน | แอสเซท | เดบิต | N | ทั้งสองรายการ | ทั้งสองรายการ | บัญชีนี้จะใช้เมื่อคุณเลือกตัวเลือกในรายการใบสั่งซื้อของสินทรัพย์ถาวร การรวมใบสั่งซื้อได้รับการตั้งค่าคอนฟิกให้ได้รับสินทรัพย์ถาวรเมื่อรับสินค้าหรือใบแจ้งหนี้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรวมใบสั่งซื้อของสินทรัพย์ถาวร ให้ไปที่ [จัดซื้อสินทรัพย์โดยการจัดซื้อ](/fixed-assets/acquire-assets-procurement) |
| รายจ่ายการซื้อสำหรับค่าใช้จ่าย | 618900 | ค่าใช้จ่ายเบ็ดเตล็ด | ค่าใช้จ่าย | เดบิต | N | ทั้งสองรายการ | |ใช้เมื่อลงรายการบัญชีใบรับสินค้าหรือใบแจ้งหนี้ของใบสั่งซื้อที่ไม่ได้เก็บในคลังสินค้า หรือมีการใช้ประเภทการจัดซื้อ |
| การชำระเงินล่วงหน้า | 132190 | ค่าใช้จ่ายที่จ่ายล่วงหน้าแล้ว | แอสเซท | เดบิต | N | ทั้งสองรายการ | | ใช้เมื่อประมวลผลใบแจ้งหนี้การล่วงหน้าในใบสั่งซื้อ |


\*ค่าที่แสดงในเครื่องหมายวงเล็บแสดงถึงค่าที่ใช้ในฟิลด์ **ชนิดการลงรายการบัญชี** บนหน้า **ธุรกรรมใบสำคัญ** คุณสามารถดู **ชนิดการลงรายการบัญชี** ในหน้า **ธุรกรรมใบสำคัญ** บนแท็บ **ทั่วไป**

## <a name="fixed-asset-posting-with-purchase-orders"></a>การลงรายการบัญชีสินทรัพย์ถาวรพร้อมด้วยใบสั่งซื้อ

ถ้าคุณใช้โมดูล **สินทรัพย์ถาวร** และวางแผนที่จะซื้อสินทรัพย์ถาวรผ่านใบสั่งซื้อ คุณต้องตั้งค่าคอนฟิกชนิดการลงรายการบัญชี **การรับสินทรัพย์ถาวร** บนแท็บ **ใบสั่งซื้อ** ของหน้า **โปรไฟล์การลงรายการบัญชีสินค้าคงคลัง** สำหรับข้อมูลเพิ่มเติม ให้ไปที่ [การรวมสินทรัพย์ถาวร](/fixed-assets/fixed-asset-integration.md) และ [สร้างและรับสินทรัพย์จากบัญชีเจ้าหนี้](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md)

## <a name="prepayment-purchase-order-invoice-posting"></a>การลงรายการบัญชีใบแจ้งหนี้ของใบสั่งซื้อการชำระเงินล่วงหน้า

ถ้าคุณวางแผนที่จะใช้คุณลักษณะ **ใบแจ้งหนี้สำหรับการชำระเงินล่วงหน้า** ของใบสั่งซื้อ ต้องเลือกชนิดการลงรายการบัญชี **การชำระเงินล่วงหน้า** บนแท็บ **ใบสั่งซื้อ** บนหน้า **โปรไฟล์การลงบัญชีสินค้าคงคลัง** สำหรับข้อมูลเพิ่มเติม ให้ไปที่ [ใบแจ้งหนี้สำหรับการชำระเงินล่วงหน้าเปรียบเทียบกับการชำระเงินล่วงหน้า](/accounts-payable/prepayments-invoices-vs-prepayments.md)

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>การลงรายการบัญชีการยืนยันใบขอซื้อและใบสั่งซื้อ

การยืนยันใบขอซื้อและใบสั่งซื้อยังสามารถตั้งค่าคอนฟิกให้ลงรายการบัญชีภาระผูกพันที่เกิดขึ้นก่อนและภาระผูกพันไปที่บัญชีแยกประเภททั่วไป การลงรายการบัญชีเหล่านี้ควบคุมโดยข้อกำหนดการลงรายการบัญชี สำหรับข้อมูลเพิ่มเติม ไปที่ [เกี่ยวกับภาระผูกพันของใบสั่งซื้อ](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances)

## <a name="procurement-category-posting"></a>การลงรายการบัญชีประเภทการจัดซื้อ

แทนที่จะตั้งค่าการลงรายการบัญชีสินค้าคงคลังสำหรับสินค้าทั้งหมด กลุ่มสินค้า หรือสินค้ารายการเดียว คุณสามารถตั้งค่าประเภทและควบคุมการลงรายการบัญชีในบัญชีแยกประเภทตามประเภทการจัดซื้อ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าประเภทและการกําหนดประเภทให้กับผลิตภัณฑ์ ให้ไปที่ [การตั้งค่าคอนฟิกโปรไฟล์การลงรายการบัญชีตัวอย่าง](#sample-posting-profile-configuration) ก่อนหน้านี้ในบทความนี้

เมื่อใช้ประเภทที่มีใบสั่งซื้อหรือใบแจ้งหนี้ของผู้จัดจำหน่าย การจัดประเภทตามลำดับชั้นต้องมอบหมายให้กับชนิด **ประเภทการจัดซื้อตามลำดับชั้น** บนหน้า **การกำหนดบทบาทของการจัดประเภทตามลำดับชั้น**

### <a name="vendor-invoices-with-procurement-categories"></a>ประเภทใบแจ้งหนี้ของผู้จัดจำหน่ายพร้อมการจัดซื้อ

ถ้าองค์กรของคุณใช้ใบสั่งซื้อกับการซื้อบางรายการ ไม่ใช่ใบสั่งซื้ออื่น คุณสามารถประมวลผลใบแจ้งหนี้ที่เกี่ยวข้องกับใบสั่งซื้อแบบอื่นได้หลายวิธี ซึ่งรวมถึงการใช้สมุดรายวันใน **บัญชีเจ้าหนี้** หรือโดยหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** ซึ่งใช้ในการสร้างใบแจ้งหนี้ของใบสั่งซื้อ เมื่อสร้างใบแจ้งหนี้ให้กับใบแจ้งหนี้ที่เกี่ยวข้องกับใบสั่งที่ไม่ใช่ใบสั่งซื้อ คุณจะต้องสร้างประเภทการจัดซื้อให้กับค่าใช้จ่ายแต่ละชนิด คุณจะต้องแม็ปประเภทกับบัญชีค่าใช้จ่ายที่ถูกต้องในหน้า **โปรไฟล์การลงรายการบัญชีสินค้าคงคลัง**

จํานวนประเภทที่แน่นอนจะแตกต่างกันไปตามจํานวนบัญชีค่าใช้จ่ายที่คุณใช้ในการลงรายการบัญชีใบแจ้งหนี้ของคุณ คุณจะต้องมีประเภทการจัดซื้ออย่างน้อยหนึ่งประเภทต่อบัญชีหลักแต่ละบัญชีที่คุณจะออกใบแจ้งหนี้ตามใบสั่งที่ไม่ใช่ใบสั่งซื้อ คุณสามารถใช้ประเภทได้หลายประเภทในหนึ่งบัญชีหลัก ซึ่งสามารถมีประโยชน์ต่อการใช้งาน ความสามารถในการค้นหา และการรายงานชนิดของค่าใช้จ่ายที่คุณใช้

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>ประโยชน์ของการใช้ประเภทการจัดซื้อสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย

บางประโยชน์ของการใช้ประเภทการจัดซื้อสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายรวมถึง:

- ประสบการณ์ของผู้ใช้ที่สอดคล้องกัน: เมื่อคุณตั้งค่าคอนฟิกประเภทการจัดซื้อให้กับค่าใช้จ่ายที่เกี่ยวข้องกับใบสั่งที่ไม่ใช่ใบสั่งซื้อทั้งหมด ผู้ใช้สามารถได้รับการฝึกอบรมในกระบวนการหนึ่งกระบวนการของการออกใบแจ้งหนี้โดยใช้หน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่**
- ประสบการณ์การรายงานที่ปรับปรุงแล้ว: เมื่อคุณตั้งค่าคอนฟิกประเภทการจัดซื้อให้กับสินค้าทั้งหมดและค่าใช้จ่ายที่เกี่ยวข้องกับใบสั่งที่ไม่ใช่ใบสั่งซื้อ รายงานการใช้จ่ายการจัดซื้อจะวิเคราะห์การใช้จ่ายโดยเรียงตามผู้จัดจำหน่าย ประเภท และอื่นๆ
- เวิร์กโฟลว์ที่สอดคล้องกัน: เมื่อคุณใช้ **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** เพื่อประมวลผลใบแจ้งหนี้ทั้งหมด คุณสามารถสร้างเวิร์กโฟลว์ที่สอดคล้องกันและกระบวนการอนุมัติได้โดยใช้เวิร์กโฟลว์เดียว

## <a name="consignment-inventory-posting"></a>การลงรายการบัญชีสินค้าคงคลังที่มีการส่งมอบ

สินค้าคงคลังที่มีการส่งมอบใช้การลงรายการบัญชีแยกประเภทเดียวกันกับสินค้าที่ซื้ออื่นๆ ผลต่างที่สำคัญคือ เมื่อได้รับสินค้าคงคลัง จะไม่มีการบันทึกธุรกรรมบัญชีแยกประเภท เมื่อต้องการโอนย้ายความเป็นเจ้าของไปยังองค์กร เมื่อลงรายการบัญชีสมุดรายวัน **การเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลัง** ใบสำคัญจะถูกสร้างขึ้นเพื่อบันทึกต้นทุนของสินค้า สำหรับข้อมูลเพิ่มเติม ไปที่ [ตั้งค่าการส่งมอบ](/supply-chain/inventory/consignment.md)
