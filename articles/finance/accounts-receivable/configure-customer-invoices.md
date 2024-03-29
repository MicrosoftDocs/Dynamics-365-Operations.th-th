---
title: สร้างใบแจ้งหนี้ของลูกค้า
description: ใบแจ้งหนี้ของลูกค้าสำหรับใบสั่งขาย คือใบตราที่เกี่ยวข้องกับการขาย และที่ทางองค์กรให้กับลูกค้า
author: ShivamPandey-msft
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0d1221e07f6dc4a5a99aa205c4a7f6fb367f000
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780566"
---
# <a name="create-a-customer-invoice"></a>สร้างใบแจ้งหนี้ของลูกค้า

[!include [banner](../includes/banner.md)]

**ใบแจ้งหนี้ของลูกค้าสำหรับใบสั่งขาย** คือใบตราที่เกี่ยวข้องกับการขาย และที่ทางองค์กรให้กับลูกค้า ชนิดของใบแจ้งหนี้ของลูกค้านี้ถูกสร้างขึ้นตามใบสั่งขาย ซึ่งรวมรายการใบสั่งและหมายเลขสินค้า ต้องมีการระบุและลงรายการบัญชีหมายเลขสินค้าในบัญชีแยกประเภท รายการสมุดรายวันของบัญชีแยกประเภทย่อยไม่พร้อมใช้งานสำหรับใบแจ้งหนี้ของลูกค้าสำหรับใบสั่งขาย สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างใบแจ้งหนี้สำหรับใบสั่งขาย](tasks/create-sales-order-invoices.md)

**ใบแจ้งหนี้ข้อความอิสระ** ไม่เกี่ยวข้องกับใบสั่งขาย ประกอบด้วยรายการใบสั่งที่รวมถึงบัญชีแยกประเภท คำอธิบายข้อความอิสระ และยอดขายที่คุณป้อนด้วยตัวเอง คุณไม่สามารถป้อนหมายเลขสินค้าบนใบแจ้งหนี้ชนิดนี้ คุณต้องป้อนข้อมูลภาษีขายที่เหมาะสม บัญชีหลักสำหรับการขายจะระบุอยู่ในแต่ละรายการใบแจ้งหนี้ ซึ่งคุณสามารถกระจายไปยังบัญชีแยกประเภทหลายบัญชี โดยการคลิก **กระจายยอดเงิน** ในหน้า **ใบแจ้งหนี้ข้อความอิสระ** นอกจากนี้ ยอดดุลลูกค้าจะมีการลงรายการบัญชีไปยังบัญชีสรุปจากโพรไฟล์การลงบัญชีที่ใช้สำหรับใบแจ้งหนี้ข้อความอิสระ

สำหรับข้อมูลเพิ่มเติม ดูที่ 
 - [สร้างใบแจ้งหนี้ข้อความอิสระ](../accounts-receivable/create-free-text-invoice-new.md)
 - [สร้างเทมเพลตใบแจ้งหนี้ข้อความอิสระ](../accounts-receivable/create-free-text-invoice-template-new.md)
 - [กำหนดเทมเพลตใบแจ้งหนี้ข้อความอิสระของลูกค้า](tasks/assign-free-text-invoice-template-customer.md)
 - [สร้างและลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ](tasks/post-recurring-free-text-invoices.md)


**ใบแจ้งหนี้ชั่วคราว** คือใบแจ้งหนี้ซึ่งเตรียมไว้เป็นการประเมินยอดเงินใบแจ้งหนี้จริงก่อนการลงรายการบัญชีใบแจ้งหนี้ คุณสามารถพิมพ์ **ใบแจ้งหนี้ชั่วคราว** สำหรับใบแจ้งหนี้ของลูกค้า สำหรับใบสั่งขาย หรือใบแจ้งหนี้ข้อความอิสระ 

>[!NOTE]
> ในกรณีของการหยุดชะงักของระบบในระหว่างกระบวนการใบแจ้งหนี้ชั่วคราว คุณสามารถทิ้งใบแจ้งหนี้ชั่วคราวได้ คุณสามารถลบใบแจ้งหนี้ชั่วคราวที่ทิ้งโดยการ เรียกใช้งานประจำงวด **ลบใบแจ้งหนี้ชั่วคราวด้วยตนเอง** ไปที่ **การขายและการตลาด > งานประจำงวด > ล้างข้อมูล > ลบใบแจ้งหนี้ชั่วคราวด้วยตนเอง**

## <a name="using-sales-order-customer-invoice-data-entities"></a>การใช้เอนทิตีข้อมูลใบแจ้งหนี้ของลูกค้าใบสั่งขาย
คุณสามารถใช้เอนทิตีข้อมูลเพื่อนําเข้าและส่งออกข้อมูลเกี่ยวกับใบแจ้งหนี้ของลูกค้าให้กับใบสั่งขายได้ มีเอนทิตีที่แตกต่างกันสำหรับข้อมูลในส่วนหัวของใบแจ้งหนี้การขายและรายการใบแจ้งหนี้การขาย

เอนทิตีต่อไปนี้สามารถใช้สำหรับข้อมูลเกี่ยวกับส่วนหัวของใบแจ้งหนี้การขายได้

- เอนทิตี **ส่วนหัวของสมุดรายวันใบแจ้งหนี้การขาย** (SalesInvoiceJournalHeaderEntity)
- เอนทิตี **ส่วนหัวของใบแจ้งหนี้การขาย V2** (SalesInvoiceHeaderV2Entity)

ขอแนะนําให้คุณใช้เอนทิตี **ส่วนหัวของสมุดรายวันใบแจ้งหนี้การขาย** เนื่องจากจะให้ประสบการณ์ที่มีประสิทธิภาพมากกว่าการนําเข้าและส่งออกส่วนหัวการขาย เอนทิตีนี้ไม่มีคอลัมน์ **ยอดเงินภาษีขาย** (INVOICEHEADERTAXAMOUNT) ซึ่งแสดงมูลค่าภาษีขายบนส่วนหัวของใบแจ้งหนี้การขาย หากสถานการณ์ทางธุรกิจของคุณต้องการข้อมูลนี้ โปรดใช้เอนทิตี **ส่วนหัวของใบแจ้งหนี้การขาย V2** เพื่อนําเข้าและส่งออกข้อมูลส่วนหัวของใบแจ้งหนี้การขาย

เอนทิตีต่อไปนี้สามารถใช้สำหรับข้อมูลเกี่ยวกับรายการใบแจ้งหนี้การขายได้

- เอนทิตี **รายการใบแจ้งหนี้ของลูกค้า** (BusinessDocumentSalesInvoiceLineItemEntity)
- เอนทิตี **รายการใบแจ้งหนี้การขาย V3** (SalesInvoiceLineV3Entity)

เมื่อคุณกําหนดว่าเอนทิตีรายการใดที่จะใช้ในการส่งออก ให้พิจารณาว่าจะใช้การส่งข้อมูลทั้งหมดหรือการส่งข้อมูลส่วนเพิ่ม นอกจากนี้ ให้พิจารณาส่วนประกอบข้อมูลด้วย เอนทิตี **รายการใบแจ้งหนี้การขาย V3** รองรับสถานการณ์สถานการณ์ที่ซับซ้อนมากขึ้น (ตัวอย่างเช่น การแมปกับฟิลด์สินค้าคงคลัง) และยังรองรับกรณีการส่งออกเป็นการส่งข้อมูลทั้งหมดด้วย สำหรับการส่งข้อมูลส่วนเพิ่ม เราขอแนะนำให้คุณใใช้เอนทิตี **รายการใบแจ้งหนี้ของลูกค้า** เอนทิตีนี้มีส่วนประกอบข้อมูลที่ง่ายกว่าเอนทิตี **รายการใบแจ้งหนี้การขาย V3** และเป็นที่ต้องการ โดยเฉพาะอย่างยิ่งถ้าไม่ต้องการการรวมฟิลด์สินค้าคงคลัง เนื่องจากความแตกต่างในการรองรับการแมประหว่างเอนทิตีรายการ โดยทั่วไปเอนทิตี **รายการใบแจ้งหนี้ของลูกค้า** จึงทำงานเร็วกว่าเอนทิตี **รายการใบแจ้งหนี้การขาย V3**

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>ลงรายการบัญชีและพิมพ์ใบแจ้งหนี้ของลูกค้าแต่ละใบตามใบสั่งขาย
ใช้ขั้นตอนนี้เพื่อสร้างใบแจ้งหนี้ตามใบสั่งขาย คุณอาจดำเนินการนี้ถ้าคุณตัดสินใจที่จะออกใบแจ้งหนี้ลูกค้าก่อนที่คุณจัดส่งสินค้าหรือบริการ 

เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** สำหรับสินค้าแต่ละรายการมีการอัปเดตด้วยยอดรวมของปริมาณใบแจ้งหนี้จากใบสั่งขายที่เลือก ถ้าทั้งทั้งคู่ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** และปริมาณ **ยอดค้างส่ง** สำหรับสินค้าทั้งหมดในใบสั่งขายเป็น 0 (ศูนย์) สถานะของใบสั่งขายจะเปลี่ยนเป็น **ออกใบแจ้งหนี้แล้ว** ถ้าปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** ไม่ใช่ 0 (ศูนย์) สถานะของใบสั่งขายยังคงไม่เปลี่ยนแปลง และสามารถป้อนใบแจ้งหนี้เพิ่มเติม

คุณสามารถดูสถานะของใบสั่งขายในหน้ารายการ **ใบสั่งขายทั้งหมด** ใช้หน้ารายการ **ใบแจ้งหนี้ของลูกค้าที่เปิด** เพื่อดูใบแจ้งหนี้ที่คุณลงรายการบัญชี

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>การลงรายการบัญชีและพิมพ์ใบแจ้งหนี้ของลูกค้าแต่ละใบตามบันทึกการจัดส่งและวันที่
ใช้กระบวนการนี้เมื่อบันทึกการจัดส่งอย่างน้อยหนึ่งได้ถูกลงรายการบัญชีสำหรับใบสั่งขาย ใบแจ้งหนี้ของลูกค้าจะขึ้นอยู่กับบันทึกการจัดส่งเหล่านี้และจะสะท้อนถึงปริมาณจากบันทึกเหล่านั้น ข้อมูลทางการเงินสำหรับใบแจ้งหนี้จะขึ้นอยู่กับข้อมูลที่ป้อนเมื่อคุณลงรายการบัญชีใบแจ้งหนี้ 

คุณสามารถสร้างใบแจ้งหนี้ของลูกค้าที่ยึดตามรายการบันทึกการจัดส่งสินค้าที่ได้มีการส่งจนถึงวันนี้ แม้ว่าสินค้าทั้งหมดสำหรับใบสั่งขายหนึ่ง ๆ ยังไม่ได้จัดส่งได้ คุณอาจดำเนินการนี้ถ้า ตัวอย่างเช่น นิติบุคคลของคุณออกใบแจ้งหนี้หนึ่งต่อลูกค้าต่อเดือนที่ครอบคลุมการจัดส่งทั้งหมดที่คุณส่งระหว่างเดือน แต่ละบันทึกการจัดส่งแสดงถึงการจัดส่งสินค้าบางส่วนหรือทั้งหมดของสินค้าในใบสั่งขาย 

เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** สำหรับสินค้าแต่ละรายการมีการอัปเดตด้วยยอดรวมของปริมาณที่จัดส่งจากบันทึกการจัดส่งที่เลือก ถ้าทั้งคู่ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** และปริมาณ **ยอดค้างส่ง** สำหรับสินค้าทั้งหมดในใบสั่งขายเป็น 0 (ศูนย์) สถานะของใบสั่งขายจะเปลี่ยนเป็น **ออกใบแจ้งหนี้แล้ว** ถ้าปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** ไม่ใช่ 0 (ศูนย์) สถานะของใบสั่งขายยังคงไม่เปลี่ยนแปลง และสามารถป้อนใบแจ้งหนี้เพิ่มเติม 

ธุรกรรมสินค้าคงคลังมีการอัปเดตด้วยหมายเลขใบแจ้งหนี้ และสถานะฟิลด์ **สถานะของรายการ** ในใบสั่งขายจะเปลี่ยนเป็น **ออกใบแจ้งหนี้แล้ว** 

ดูสถานะของใบสั่งขายในหน้ารายการ **ใบสั่งขายทั้งหมด**

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>รวมใบสั่งขายหรือบันทึกการจัดส่งสำหรับการลงรายการบัญชี
ใช้ขั้นตอนนี้เมื่อใบสั่งขายหนึ่งรายการขึ้นไปพร้อมจะออกใบแจ้งหนี้แล้ว และคุณต้องการรวมไว้ในใบแจ้งหนี้เดียว 

คุณสามารถเลือกใบแจ้งหนี้หลายใบในหน้ารายการ **ใบสั่งขาย** และจากนั้นใช้ **สร้างใบแจ้งหนี้** เพื่อรวม ในหน้า  **การลงรายการบัญชีใบแจ้งหนี้** คุณสามารถเปลี่ยนการตั้งค่า **ใบสั่งโดยสรุป** เพื่อสรุปตามหมายเลขใบสั่ง (ที่มีหลายบันทึกการจัดส่งสำหรับใบสั่งขายหนึ่ง ๆ) หรือตามบัญชีใบแจ้งหนี้ (ที่มีใบสั่งขายหลายใบสำหรับบัญชีใบแจ้งหนี้เดียว) ใช้ปุ่ม **จัดเรียง** เพื่อรวมใบสั่งขายลงในใบแจ้งหนี้เดียว ตามการตั้งค่า **ใบสั่งโดยสรุป**

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>แบ่งใบแจ้งหนี้ของใบสั่งขายตามข้อมูลไซต์และการจัดส่ง
คุณสามารถตั้งค่าคอนฟิกการแบ่งใบแจ้งหนี้ของลูกค้าตามไซต์หรือที่อยู่ที่จัดส่งบนแท็บ **การอัปเดตสรุป** ของหน้า **พารามิเตอร์บัญชีลูกหนี้** 
 - เลือกตัวเลือก **แบ่งตามไซต์ใบแจ้งหนี้** เพื่อสร้างใบแจ้งหนี้หนึ่งใบต่อไซต์เมื่อลงรายการบัญชี 
 - เลือกตัวเลือก **แบ่งตามข้อมูลการจัดส่งของใบแจ้งหนี้** เพื่อสร้างใบแจ้งหนี้หนึ่งใบต่อที่อยู่ที่จัดส่งในรายการใบสั่งขายเมื่อลงรายการบัญชี 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>ลงรายการบัญชีไปยังบัญชีรายได้สำหรับรายการใบสั่งขายที่ไม่มีราคาและไม่มีต้นทุน
คุณจะมีตัวเลือกในการอัปเดตบัญชี **รายได้** ใน **บัญชีแยกประเภททั่วไป** สำหรับรายการบัญชีใบสั่งขายที่ไม่มีราคาและไม่มีต้นทุน 

เมื่อต้องการตั้งค่าหรือดูข้อมูลนี้:
1. ไปที่ **ลงรายการบัญชีไปยังบัญชีรายได้สำหรับรายการใบแจ้งหนี้ใบสั่งขายที่มีราคาเป็นศูนย์และต้นทุนเป็ฯศูนย์** บนแท็บ **บัญชีแยกประเภทและภาษีขาย** ของหน้า **พารามิเตอร์บัญชีลูกหนี้** (**บัญชีลูกหนี้ > การตั้งค่า > พารามิเตอร์บัญชีลูกหนี้**) 
2. เลือก **ใช่** เพื่ออัปเดตบัญชี **รายได้** สำหรับรายการใบแจ้งหนี้ใบสั่งขายที่ไม่มีราคาและไม่มีต้นทุน 
 - ถ้าเลือกตัวเลือกนี้ ใบส่วนลดจะประกอบด้วยรายการ 0.00 รายการ ในชนิดการลงรายการบัญชี **ยอดดุลลูกค้า** และ **รายได้** บัญชีรายได้จะถูกกําหนดบนหน้าพารามิเตอร์ **การลงรายการบัญชีสินค้าคงคลัง** บนแท็บข้อกําหนดบัญชี **ใบสั่งขาย** 
 - ถ้าไม่ได้เลือกตัวเลือกนี้ รายการที่ไม่มีข้อมูลราคาหรือต้นทุนจะไม่ลงรายการบัญชีที่บัญชี **รายได้** ใบส่วนลดจะประกอบด้วยข้อมูล 0.00 รายการ ในชนิดการลงรายการบัญชี **ยอดดุลลูกค้า**

## <a name="line-creation-sequence-number-information"></a>ข้อมูลหมายเลขลดับการสร้างรายการ
เมื่อคุณลงรายการบัญชีบรรทัดใบแจ้งหนี้ของลูกค้า คุณจะมีตัวเลือกในการสร้างหมายเลขลำดับของการสร้างบรรทัดตามลำดับ มีการมอบหมายหมายเลขลดับการสร้างรายการในระหว่างกระบวนการลงรายการบัญชี คุณสามารถปรับปรุงประสิทธิภาพการลงรายการบัญชีใบแจ้งหนี้ของลูกค้าได้ โดยการอนุญาตให้กำหนดหมายเลขแบบไม่ต่อเนื่อง หมายเลขลำดับการสร้างรายการสามารถใช้โดยการรวมของบุคคลที่สาม ที่คาดว่าจะมีการเรียงลดับ โปรดปรึกษาแผนก IT ของคุณ เกี่ยวกับส่วนขยายใดๆ ที่อาจรวมกับหมายเลขลำดับการสร้างรายการ

เมื่อต้องการตั้งค่าหรือดูข้อมูลนี้ บนหน้า **พารามิเตอร์บัญชีลูกหนี้** บนแท็บ **อัปเดต** ให้ตั้งค่าตัวเลือก **กําหนดหมายเลขบรรทัดตามลำดับเมื่อลงรายการบัญชีบรรทัดใบแจ้งหนี้ของลูกค้า**:

- ตั้งค่าตัวเลือกเป็น **ไม่** เพื่อใช้การเรียงลดับหมายเลขแบบไม่ต่อเนื่อง สำหรับหมายเลขลำดับการสร้างบรรทัด
- ตั้งค่าตัวเลือกเป็น **ใช่** เพื่อใช้การกำหนดหมายเลขตามลำดับ คุณต้องตั้งค่าตัวเลือกเป็น **ใช่** ให้กับเอนทิตีที่มีที่อยู่หลักในอิตาลี คุณต้องตั้งค่าเป็น **ใช่** เช่นกัน เมื่อเที่ยวบิน **CustInvoiceTransRandLineCreationSeqNumFlight** ถูกปิดใช้งาน

## <a name="additional-settings-that-change-the-posting-behavior"></a>การตั้งค่าเพิ่มเติมที่เปลี่ยนแปลงพฤติกรรมการลงรายการบัญชี
ฟิลด์ต่อไปนี้เปลี่ยนแปลงกระบวนการพฤติกรรมการลงรายการบัญชี

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>ฟิลด์</th>
<th>คำอธิบาย</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ปริมาณ</td>
<td>เลือกปริมาณเพื่อใช้เป็นพื้นฐานของการลงรายการบัญชีของเอกสาร ตัวเลือกที่พร้อมใช้งานจะแตกต่างกันไป ขึ้นอยู่กับชนิดของเอกสารที่คุณกำลังลงรายการบัญชี เช่นบันทึกการจัดส่งหรือใบแจ้งหนี้
<ul>
<li><strong>จัดส่งทันที</strong> – เลือกปริมาณทั้งหมดที่ป้อนในฟิลด์ <strong>จัดส่งทันที</strong> ใช้ตัวเลือกนี้เพื่อยืนยันหรือส่งใบสั่งเป็นบางส่วน</li>
<li><strong>เบิกสินค้าแล้ว</strong> – เลือกปริมาณทั้งหมดที่มีการเบิกสินค้า</li>
<li><strong>ทั้งหมด</strong> – เลือกปริมาณทั้งหมดในใบสั่งขายที่ยังไม่ได้รับการปรับปรุงโดยชนิดเอกสารปัจจุบัน</li>
<li><strong>บันทึกการจัดส่ง</strong> – เลือกปริมาณทั้งหมดที่อัปเดตแล้วตามบันทึกการจัดส่ง</li>
<li><strong>ปริมาณที่เลือกและผลิตภัณฑ์ที่ไม่ได้สต็อค</strong> – เลือกปริมาณทั้งหมดที่ได้ถูกเลือกและปริมาณผลิตภัณฑ์ทั้งหมดที่ไม่ได้ถูกสต็อค</li>
</ul></td>
</tr>
<tr class="even">
<td>การลงรายการบัญชี</td>
<td><ul>
<li>เลือกตัวเลือกนี้เพื่อบันทึกบัญชีใบสั่งขาย</li>
<li>ล้างตัวเลือกนี้เพื่อพิมพ์ใบสั่งขายชั่วคราว <strong>หมายเหตุ:</strong> ถ้าคุณทำข้อตกลงสำหรับกำหนดการชำระเงิน กำหนดการชำระเงินจะไม่ถูกแสดงบนใบสั่งขาย pro forma กำหนดการชำระเงินจะแสดงบนใบสั่งขายจริงเท่านั้น</li>
</ul></td>
</tr>
<tr class="odd">
<td>การเลือกหลังสุด</td>
<td>เลือกตัวเลือกนี้เพื่อใช้การสอบถามที่เลือกในภายหลัง ตัวเลือกนี้ใช้สำหรับชุดงาน แบบสอบถามจะเรียกใช้เมื่อชุดงานเรียกใช้</td>
</tr>
<tr class="even">
<td>ลดปริมาณ</td>
<td>เลือกตัวเลือกนี้เพื่อลดปริมาณที่จัดส่งเมื่อเอกสารถูกลงรายการบัญชีอัตโนมัติ เพื่อให้ปริมาณที่ส่งเท่ากับสินค้าคงคลังที่มี</td>
</tr>
<tr class="odd">
<td>พิมพ์</td>
<td>เลือกเวลาที่จะพิมพ์เอกสาร
<ul>
<li><strong>ปัจจุบัน</strong> – พิมพ์เอกสารหลังจากแต่ละใบแจ้งหนี้มีการอัปเดตแล้ว</li>
<li><strong>หลังจาก</strong> – พิมพ์เอกสารหลังจากกใบแจ้งหนี้ทั้งหมดมีการอัปเดตแล้ว</li>
</ul>
<strong>หมายเหตุ:</strong> ฟิลด์ <strong>พิมพ์</strong> จะพร้อมใช้งานเมื่อคุณเลือกเท่านั้นการพิมพ์ <strong>พิมพ์ใบแจ้งหนี้</strong> <strong>พิมพ์การยืนยัน</strong> <strong>พิมพ์รายการเบิกสินค้า</strong> หรือตัวเลือก <strong>พิมพ์บันทึกการจัดส่ง</strong> ตัวอย่างเช่น ในหน้า <strong>การเรียงลำดับแบบฟอร์ม</strong> คุณตั้งค่าระบบให้เรียงลำดับข้อมูลตามบัญชีใบแจ้งหนี้ คุณสามารถเลือก <strong>หลังจาก</strong> การพิมพ์เอกสารในชุดงานที่จะเรียงลำดับตามบัญชีใบแจ้งหนี้ มิฉะนั้น เอกสารจะถูกพิมพ์ก่อนการประมวลผลเสร็จสิ้น และเอกสารจะไม่ถูกจัดเรียงตามลำดับที่ระบุในหน้า <strong>การจัดเรียงฟอร์ม</strong></td>
</tr>
<tr class="even">
<td>พิมพ์ใบแจ้งหนี้</td>
<td>เลือกตัวเลือกนี้เพื่อพิมพ์ใบแจ้งหนี้ ถ้าตัวเลือกนี้ปิดอยู่ คุณสามารถลงรายการใบแจ้งหนี้โดยไม่พิมพ์</td>
</tr>
<tr class="odd">
<td>ส่งอีเมล</td>
<td>เลือกตัวเลือกนี้เพื่อส่งใบแจ้งหนี้สำหรับใบสั่งขายไปยังลูกค้าตามอีเมลที่แนบหลังจากมีการลงรายการบัญชีใบแจ้งหนี้แล้ว สิ่งที่แนบจะมีการส่งเป็นไฟล์ PDF และ XML ตัวเลือกนี้จะพร้อมใช้งานเมื่อคุณเลือกเท่านั้นตัวเลือก <strong>เปิดใช้งาน CFD (ใบแจ้งหนี้อิเล็กทรอนิกส์)</strong> หน้า <strong>พารามิเตอร์ใบแจ้งหนี้อิเล็กทรอนิกส์ </strong> <strong>หมายเหตุ:</strong> (MEX) ตัวควบคุมนี้สามารถใช้ได้เฉพาะกับนิติบุคคลที่มีที่อยู่หลักอยู่ในเม็กซิโกเท่านั้น</td>
</tr>
<tr class="even">
<td>ใช้ปลายทางการจัดการงานพิมพ์</td>
<td>เลือกตัวเลือกนี้เพื่อใช้การตั้งค่าการพิมพ์ที่ระบุไว้สำหรับธุรกรรม เอกสาร หรือโมดูลใน ในหน้า <strong>การตั้งค่าการจัดการพิมพ์</strong></td>
</tr>
<tr class="odd">
<td>ตรวจสอบวงเงินสินเชื่อ</td>
<td>เลือกข้อมูลที่ควรจะวิเคราะห์ เมื่อดำเนินการตรวจสอบวงเงินสินเชื่อ
<ul>
<li><strong>ไม่มี</strong> – ไม่มีข้อกำหนดสำหรับการตรวจสอบวงเงินสินเชื่อ</li>
<li><strong>ยอดดุล</strong> – มีการตรวจสอบวงเงินสินเชื่อเทียบกับยอดดุลลูกค้า</li>
<li><strong>ยอดดุล + บันทึกการจัดส่งหรือใบรับสินค้า</strong>– มีการตรวจสอบวงเงินสินเชื่อเทียบกับยอดดุลลูกค้า การจัดส่ง</li>
<li><strong>ยอดดุล+ทั้งหมด</strong> – มีการตรวจสอบวงเงินสินเชื่อเทียบกับยอดดุลลูกค้า การจัดส่ง และใบสั่งที่เปิด</li>
</ul></td>
</tr>
<tr class="even">
<td>การแก้ไขสินเชื่อ</td>
<td>เลือกตัวเลือกนี้ เพื่อแสดงใบลดหนี้เป็นเดบิตในธุรกรรมใบสำคัญ</td>
</tr>
<tr class="odd">
<td>ลงเครดิตปริมาณที่เหลือ</td>
<td>ถ้าคุณกำลังลงรายการบัญชีใบลดหนี้ เลือกตัวเลือกนี้เพื่อรักษาปริมาณคงเหลือในใบสั่ง ถ้าไม่ได้เลือกตัวเลือกนี้ ปริมาณคงเหลือจะตั้งเป็น 0 (ศูนย์)</td>
</tr>
<tr class="even">
<td>อัปเดตบทสรุปสำหรับ</td>
<td>เลือกวิธีใบสั่งขายหลายใบที่ควรสรุป
<ul>
<li><strong>ไม่มี</strong> – ห้ามสรุปใบสั่งขาย ตัวอย่างเช่น ใบแจ้งหนี้ที่แยกต่างหากจะถูกสร้างสำหรับแต่ละใบสั่งขาย</li>
<li><strong>บัญชีใบแจ้งหนี้</strong> – สรุปใบสั่งที่เลือกทั้งหมด ตามเงื่อนไขที่ตั้งค่าในหน้า <strong>พารามิเตอร์การอัปเดตบทสรุป</strong></li>
<li><strong>ใบสั่ง</strong> – สรุปช่วงของใบสั่งที่เลือกเป็นใบสั่งเดียวที่คุณระบุ มีการสรุปใบสั่งตามเงื่อนไขที่ตั้งค่าในหน้า <strong>พารามิเตอร์การอัปเดตบทสรุป</strong> ถ้าคุณเลือกตัวเลือกนี้ คุณต้องเลือกค่าในฟิลด์ <strong>ใบสั่งขาย</strong></li>
<li><strong>สรุปอัตโนมัติ</strong>– ถ้ามีการระบุการอัปเดตบทสรุปในหน้า <strong>การอัปเดตบทสรุป</strong> สรุปใบสั่งที่เลือกทั้งหมด ตามเงื่อนไขที่ตั้งค่าในหน้า <strong>พารามิเตอร์การอัปเดตบทสรุป</strong> ถ้าการปรับปรุงสรุปไม่ได้ถูกระบุ ลงรายการบัญชีใบสั่งแยกต่างหาก</li>
<li><strong>บันทึกการจัดส่ง</strong> – สรุปช่วงของใบสั่งที่เลือกเป็นใบแจ้งหนี้หนึ่งฉบับสำหรับบันทึกการจัดส่งแต่ละฉบับ ตัวเลือกนี้จะพร้อมใช้งานเมื่อถ้า <strong>บันทึกการจัดส่ง</strong> มีการเลือกในฟิลด์ <strong>ปริมาณ</strong> เท่านั้น</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
