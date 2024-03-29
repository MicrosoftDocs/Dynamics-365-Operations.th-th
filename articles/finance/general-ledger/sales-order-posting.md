---
title: การลงรายการบัญชีใบสั่งขาย
description: บทความนี้แสดงข้อมูลเกี่ยวกับแท็บใบสั่งขายของหน้าโพรไฟล์การลงบัญชีสินค้าคงคลัง
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886326"
---
# <a name="sales-order-posting"></a>การลงรายการบัญชีใบสั่งขาย

แท็บ **ใบสั่งขาย** บนหน้า **โพรไฟล์การลงรายการบัยชีสินค้าคงคลัง** ใช้เพื่อควบคุมวิธีการลงรายการบัญชีใบสั่งขายในบัญชีแยกประเภททั่วไป กิจกรรมหลักสองกิจกรรมจะลงรายการบัญชีในบัญชีแยกประเภททั่วไปสำหรับใบสั่งขาย: 

- บันทึกการจัดส่ง
- ใบแจ้งหนี้

เพื่อให้ธุรกรรมที่เกิดขึ้นจริง (บันทึกการจัดส่ง) สามารถลงรายการบัญชีในบัญชีแยกประเภททั่วไปสำหรับใบสั่งขายได้ ต้องเป็นไปตามเงื่อนไขต่อไปนี้

- บนหน้า **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** คุณต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีบันทึกการจัดส่งในบัญชีแยกประเภท**
- บนหน้า **กลุ่มแบบจำลองสินค้า** ของสินค้าที่เลือกในรายการใบสั่งขาย ต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีสินค้าคงคลังที่มีอยู่จริงในบัญชีแยกประเภท**
- บนหน้า **โพรไฟล์การลงบัญชีสินค้าคงคลัง** คุณต้องระบุบัญชีหลักในชนิดการลงรายการบัญชีต่อไปนี้
  - ส่งต้นทุนของหน่วยแล้ว
  - ส่งต้นทุนขายแล้ว

สำหรับธุรกรรมทางการเงิน (ใบแจ้งหนี้) ที่จะลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปสำหรับใบสั่งขาย ต้องเป็นไปตามเงื่อนไขต่อไปนี้:

- บนหน้า **กลุ่มแบบจำลองสินค้า** ของสินค้าที่เลือกในรายการใบสั่งขาย ต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีสินค้าคงคลังทางการเงินในบัญชีแยกประเภท**
- คุณต้องระบุบัญชีหลักในหน้า **โพรไฟล์การลงบัญชีสินค้าคงคลัง** สำหรับชนิดการลงรายการบัญชีต่อไปนี้
  - ต้นทุนของหน่วยที่ออกใบแจ้งหนี้
  - ออกใบแจ้งหนี้ต้นทุนขายแล้ว
  - รายได้
  - ส่วนลด\*

> [!NOTE]
> บัญชีส่วนลดเป็นข้อมูลที่ไม่บังคับ ข้อบังคับด้านบัญชีต่างๆ เช่น GAAP และ IFRS มีข้อต้องให้ส่วนลดลดรายได้ของการขาย และดังนั้นจึงไม่ได้ใช้บัญชีเหล่านี้ในหลายสถานการณ์ หากข้อบังคับท้องถิ่นอนุญาต ให้ใช้บัญชีหลักแยกต่างหากเพื่อลงรายการบัญชีส่วนของราคาขายส่วนที่ให้ส่วนลด

เมื่อต้องการลงรายการบัญชีมูลค่ารายได้ที่รอตัดบัญชี (โดยประมาณ) ไปยังบัญชีแยกประเภททั่วไป เมื่อคุณสร้างบันทึกการจัดส่งให้กับใบสั่งขาย ต้องเป็นไปตามเงื่อนไขต่อไปนี้

- บนหน้า **กลุ่มแบบจำลองสินค้า** ของสินค้าที่เลือกในรายการใบสั่งขาย ต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีสินค้าคงคลังที่มีอยู่จริงในบัญชีแยกประเภท**
- บนหน้า **กลุ่มแบบจำลองสินค้า** ต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีไปยังบัญชีรายได้รอตัดบัญชีสำหรับการจัดส่งสินค้าขาย**
- บนหน้า **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** คุณต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีบันทึกการจัดส่งในบัญชีแยกประเภท**
- บนหน้า **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** คุณต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีภาษีขายจริง**
- บนหน้า **พารามิเตอร์บัญชีลูกหนี้** คุณต้องเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชีบันทึกการจัดส่งในบัญชีแยกประเภท**
- บนหน้า **โพรไฟล์การลงบัญชีสินค้าคงคลัง** คุณต้องระบุบัญชีหลักในชนิดการลงรายการบัญชีต่อไปนี้
  - รายได้รอการตัดบัญชีสำหรับการจัดส่ง
  - บัญชีตรงข้ามของรายได้รอการตัดบัญชีสำหรับการจัดส่ง
  - ภาษีขายรอการตัดบัญชีสำหรับการจัดส่ง

> [!NOTE]
> โดยทั่วไป เราขอแนะนำให้คุณเปิดใช้งานตัวเลือก **ลงรายการบัญชีสินค้าคงคลังที่มีอยู่จริง** และ **ลงรายการบัญชีบันทึกการจัดส่งในบัญชีแยกประเภท** การเปิดใช้งานตัวเลือกเหล่านี้สามารถช่วยในการเร่งกระบวนการปิดบัญชีสิ้นเดือน เนื่องจากคุณจะต้องคํานวณและลงรายการบัญชีรายการรอตัดบัญชีด้วยตนเอง นอกจากนี้ งบการเงินจะแสดงถึงยอดเงินที่รอตัดบัญชีโดยอัตโนมัติ โดยไม่ต้องมีการดำเนินการด้วยตนเอง

> [!IMPORTANT]
> ตัวเลือก **ลงรายการบัญชีไปยังบัญชีรายได้รอตัดบัญชีสำหรับการจัดส่งสินค้าขาย** ไม่ได้ใช้กับการรับรู้รายได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรับรู้รายได้ ให้ไปที่ [ภาพรวมของการรับรู้รายได้](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>การตั้งค่าคอนฟิกโพรไฟล์การลงรายการบัญชีตัวอย่าง 

ตารางต่อไปนี้แสดงตัวอย่างของชนิดการลงรายการบัญชีเริ่มต้นพร้อมด้วยบัญชีหลักและคำอธิบายตัวอย่าง:
 
- คอลัมน์ **บัญชีรอการโอน** แสดงว่าชนิดบัญชีเป็นบัญชีรอการโอน ยอดเงินที่ลงรายการบัญชีในบัญชีนี้จะถูกกลับรายการโดยอัตโนมัติเมื่อลงรายการบัญชีธุรกรรมในภายหลัง 
- คอลัมน์ **P/F** แสดง **P** สำหรับการลงรายการบัญชีและ **F** สำหรับการลงรายการบัญชีทางการเงิน 
- คอลัมน์ **ตามอย่าง** ระบุว่าบัญชีหลักสำหรับการลงรายการบัญชีประเภทใดประเภทหนึ่งมักเหมือนกับการลงรายการบัญชีประเภทอื่นหรือไม่ ค่าในคอลัมน์จะแสดงชนิดของการลงรายการบัญชีที่ใช้กันโดยทั่วไป

> [!NOTE]
> บัญชีหลักและชื่อบัญชีหลักเหล่านี้เป็นการแนะนำเท่านั้น เราขอแนะนำให้คุณทำงานร่วมกับนักบัญชีเพื่อตั้งค่าคอนฟิกที่ดีที่สุดสำหรับความต้องการทางธุรกิจของคุณ


| ชนิดการลงรายการบัญชี | ตัวอย่างบัญชีหลัก | ตัวอย่างชื่อบัญชีหลัก | ชนิดบัญชี | เดบิต/เครดิตหรือไม่ | บัญชีรอการโอน | P/F | ตามอย่าง | คำอธิบาย |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| ส่งต้นทุนของหน่วยแล้ว | 140100</br>140101 | สินค้าคงคลังวัสดุ</br>วัสดุที่จัดส่งแล้วแต่ยังไม่ได้ออกใบแจ้งหนี้ | แอสเซท | เครดิต | ใช่ | P | ต้นทุนของหน่วยที่ออกใบแจ้งหนี้ | ใช้เมื่อลงรายการบัญชีบันทึกการจัดส่งของใบสั่งขาย ออฟเซ็ตของบัญชีคือ ต้นทุนขายที่จัดส่งแล้ว ยอดเงินในบัญชีนี้จะกลับรายการเมื่อมีการลงรายการบัญชีใบแจ้งหนี้ของใบสั่งขาย คุณอาจต้องการใช้บัญชีวัสดุที่จัดส่งที่ยังไม่ได้ออกใบแจ้งหนี้เพื่อแสดงสินค้าคงคลังจริง และจองบัญชีสินค้าคงคลังวัสดุสำหรับการปรับปรุงทางการเงิน |
| ส่งต้นทุนขายแล้ว | 500150 | COGS ที่รอการตัดบัญชี | ค่าใช้จ่าย | เดบิต | ใช่ | P  | ใช้เมื่อลงรายการบัญชีบันทึกการจัดส่งของใบสั่งขาย ออฟเซ็ตของบัญชีคือ ต้นทุนของหน่วยที่จัดส่งแล้ว ยอดเงินในบัญชีนี้จะกลับรายการเมื่อมีการลงรายการบัญชีใบแจ้งหนี้ของใบสั่งขาย |
| ต้นทุนของหน่วยที่ออกใบแจ้งหนี้ | 140100 | สินค้าคงคลังวัสดุ | แอสเซท | เครดิต | ไม่ | ศ. | ส่งต้นทุนของหน่วยแล้ว | ใช้เมื่อลงรายการบัญชีใบแจ้งหนี้ของใบสั่งขาย ออฟเซ็ตของบัญชีนี้คือ ต้นทุนขายที่ออกใบแจ้งหนี้แล้ว บัญชีนี้แสดงถึงสินค้าคงคลังในงบดุลของคุณ |
| ออกใบแจ้งหนี้ต้นทุนขายแล้ว | 500100 | วัสดุ COGS | ค่าใช้จ่าย | เดบิต | ไม่ | ศ.  | ใช้เมื่อลงรายการบัญชีใบแจ้งหนี้ของใบสั่งขาย ออฟเซ็ตของบัญชีนี้คือ ต้นทุนของหน่วยที่ออกใบแจ้งหนี้แล้ว บัญชีนี้แสดงถึง COGS ในรายงาน P&amp;L ของคุณ |
| รายได้ (รายได้ของใบสั่งขาย*) | 400100 | วัสดุรายได้ | รายได้ | เครดิต | ไม่ | ศ.   | ใช้เมื่อลงรายการบัญชีใบแจ้งหนี้ของใบสั่งขาย ออฟเซ็ตของบัญชีนี้เป็นบัญชีสรุป (ยอดดุลลูกค้า*) ใน **โพรไฟล์การลงรายการบัญชีบัญชีลูกหนี้** |
| ค่าคอมมิชชัน (การขาย, ค่าคอมมิชชัน*) | 602150 | ค่าคอมมิชชัน | ค่าใช้จ่าย | เดบิต | ไม่ | ศ.  | ใช้เมื่อเปิดใช้งานและคำนวณค่าคอมมิชชันสำหรับการขายและลงรายการบัญชีระหว่างกระบวนการใบแจ้งหนี้ของใบสั่งขาย ออฟเซ็ตของบัญชีนี้เป็นค่าคอมมิชชันที่ต้องชำระ |
| ออฟเซ็ตค่าคอมมิชชัน (การขาย, ออฟเซ็ตค่าคอมมิชชัน*) | 201110 | ค่าคอมมิชชันที่ต้องชำระ | หนี้สิน | เครดิต | ใช่ | ศ. | ใช้เมื่อเปิดใช้งานและคำนวณค่าคอมมิชชันสำหรับการขายและลงรายการบัญชีระหว่างกระบวนการใบแจ้งหนี้ของใบสั่งขาย ออฟเซ็ตของบัญชีนี้เป็นค่าใช้จ่ายที่เป็นค่าคอมมิชชัน |
| รายได้รอตัดบัญชีเมื่อมีการจัดส่ง (การขาย – รายได้ในบันทึกการจัดส่ง*) | 401400 | ยอดขายค้างรับ | รายได้ | เครดิต | ใช่ | P  | ใช้เมื่อเปิดใช้งานรายได้รอตัดบัญชีสำหรับการจัดส่ง และถูกลงรายการบัญชีเมื่อคุณประมวลผลบันทึกการจัดส่งของใบสั่งขาย ออฟเซ็ตของบัญชีนี้คือออฟเซ็ตรายได้รอตัดบัญชี ยอดเงินในบัญชีนี้จะถูกกลับรายการโดยอัตโนมัติเมื่อคุณลงรายการบัญชีใบแจ้งหนี้ของใบสั่งขาย |
| ออฟเซ็ตรายได้รอตัดบัญชีเมื่อมีการจัดส่ง (การขาย – ออฟเซ็ตรายได้ในบันทึกการจัดส่ง)* | 130400 | บัญชีลูกหนี้ – ยังไม่ได้ออกใบแจ้งหนี้ | แอสเซท | เดบิต | ใช่ | P  | ใช้เมื่อเปิดใช้งานรายได้รอตัดบัญชีสำหรับการจัดส่ง และลงรายการบัญชีเมื่อคุณประมวลผลบันทึกการจัดส่งของใบสั่งขาย ออฟเซ็ตของบัญชีนี้คือรายได้รอตัดบัญชีเมื่อมีการจัดส่ง ยอดเงินในบัญชีนี้จะถูกกลับรายการโดยอัตโนมัติเมื่อคุณลงรายการบัญชีใบแจ้งหนี้ของใบสั่งขาย |
| ภาษีขายรอตัดบัญชีเมื่อมีการจัดส่ง (การขาย, ภาษีในบันทึกการจัดส่ง*) | 250500 | ภาษีขายรอตัดบัญชี | หนี้สิน | เครดิต | ใช่ | P  | ใช้เมื่อเปิดใช้งานรายได้รอตัดบัญชีสำหรับการจัดส่งและเปิดใช้งานลงรายการบัญชีภาษีขายจริง มีการลงรายการบัญชียอดภาษีเมื่อคุณประมวลผลบันทึกการจัดส่งของใบสั่งขาย |

\*ค่าที่แสดงในเครื่องหมายวงเล็บในตารางนี้แสดงถึงค่าที่ใช้ในฟิลด์ **ชนิดการลงรายการบัญชี** บนหน้า **ธุรกรรมใบสำคัญ** คุณสามารถดู **ชนิดการลงรายการบัญชี** ในหน้า **ธุรกรรมใบสำคัญ** บนแท็บ **ทั่วไป**

## <a name="sales-category-posting"></a>การลงรายการบัญชีประเภทการขาย

แทนที่จะตั้งค่าการลงรายการบัญชีสินค้าคงคลังสำหรับสินค้าทั้งหมด กลุ่มสินค้า หรือสินค้ารายการเดียว คุณสามารถตั้งค่าประเภทและควบคุมการลงรายการบัญชีในบัญชีแยกประเภทตามประเภทการขาย สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าลำดับชั้นของประเภทและการกำหนดประเภทให้กับสินค้า ไปที่ [สร้างลำดับขั้นของการจัดประเภทผลิตภัณฑ์](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) และ [จัดประเภทผลิตภัณฑ์โดยใช้ลำดับชั้นประเภท](/supply-chain/pim/tasks/classify-product-category-hierarchies.md)

หลังจากที่คุณสร้างการจัดประเภทตามลำดับชั้นแล้ว คุณต้องกำหนดลำดับชั้นให้กับประเภทอย่างน้อยหนึ่งประเภท เมื่อต้องการใช้การจัดประเภทตามลำดับชั้นในใบสั่งขาย คุณต้องกําหนดประเภทให้กับชนิดการจัดประเภทตามลำดับชั้นของการขาย สำหรับข้อมูลเพิ่มเติม ไปที่ [เกี่ยวกับการจัดประเภทตามลำดับชั้น](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>สร้างการลงรายการบัญชีรายได้โดยเรียงตามประเภทการขาย

เมื่อต้องการกําหนดการลงรายการบัญชีแยกประเภทให้กับใบสั่งขายตามประเภทการขาย ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการสินค้างคงคลัง** > **การตั้งค่า** > **การลงรายการบัญชี** > **การลงรายการบัญชี**
2. เลือกแท็บ **การขาย**
3. เลือกปุ่มตัวเลือกให้กับชนิดการลงรายการบัญชีที่คุณต้องการตั้งค่าคอนฟิก (ตัวอย่างเช่น **รายได้**)
4. เลือก **ใหม่**
5. ในฟิลด์ **รหัสสินค้า** ให้เลือก **ประเภท**
6. ใช้ฟิลด์ **ความสัมพันธ์ของประเภท** เพื่อเลือกประเภทสำหรับโพรไฟล์การลงรายการบัญชี
7. ในฟิลด์ **รหัสบัญชี** ให้เลือกตัวเลือกสำหรับ **ตาราง**, **กลุ่ม** หรือ **ทั้งหมด** ตัวอย่างเช่น เมื่อต้องการใช้โพรไฟล์การลงรายการบัญชีกับลูกค้าทั้งหมด ให้เลือก **ทั้งหมด**
   - ถ้าคุณเลือก **ตาราง** ในขั้นตอนที่ 6 ให้เลือก **หมายเลขผู้จัดจำหน่าย** เฉพาะให้กับโพรไฟล์การลงรายการบัญชีในฟิลด์ **ความสัมพันธ์ของบัญชี**
   - ถ้าคุณเลือก **กลุ่ม** ในขั้นตอนที่ 6 ให้เลือก **กลุ่มผู้จัดจำหน่าย** ให้กับโพรไฟล์การลงรายการบัญชีในฟิลด์ **ความสัมพันธ์ของบัญชี**
   - หากคุณเลือก **ทั้งหมด** ในขั้นตอนที่ 6 ฟิลด์ **ความสัมพันธ์ของบัญชี** จะเว้นว่างไว้

8. เมื่อต้องการเชื่อมโยงกลุ่มภาษีเฉพาะกับชนิดการลงรายการบัญชีที่เลือก ให้เลือก **กลุ่มภาษีขาย** ถ้าคุณปล่อยฟิลด์นี้ว่างไว้ ชนิดการลงรายการบัญชีจะใช้กับกลุ่มภาษีที่มีอยู่ทั้งหมด  การลงรายการบัญชีที่ระบุไว้สำหรับกลุ่มภาษีจะใช้กับธุรกรรมที่ทำไว้สำหรับการขายและการซื้อเท่านั้น

9. ในฟิลด์ **บัญชีหลัก** ให้ระบุหมายเลขบัญชีที่จะลงรายการบัญชีเป็นชนิดบัญชี เลือกหมายเลขบัญชีหนึ่งหมายเลขที่มีอยู่ในผังบัญชี 
