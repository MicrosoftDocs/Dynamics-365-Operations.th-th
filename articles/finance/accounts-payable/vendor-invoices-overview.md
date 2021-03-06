---
title: ภาพรวมใบแจ้งหนี้ของผู้จัดจำหน่าย
description: หัวข้อนี้ให้ข้อมูลทั่วไปเกี่ยวกับใบแจ้งหนี้ของผู้จัดจำหน่าย
author: abruer
manager: AnnBe
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0299eb3470f500bf469c3367f1c426715067a5dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993327"
---
# <a name="vendor-invoices-overview"></a>ภาพรวมของใบแจ้งหนี้ของผู้จัดจำหน่าย

[!include [banner](../includes/banner.md)]

หัวข้อนี้ให้ข้อมูลทั่วไปเกี่ยวกับใบแจ้งหนี้ของผู้จัดจำหน่าย มีการร้องขอใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับการชำระเงินผลิตภัณฑ์และบริการที่ได้รับ ใบแจ้งหนี้ของผู้จัดจำหน่ายจะแสดงบิลสำหรับบริการต่อเนื่อง หรือพวกเขาสามารถยึดตามใบสั่งซื้อสำหรับสินค้าเฉพาะและบริการ

## <a name="vendor-invoices"></a>ใบแจ้งหนี้ของผู้จัดจำหน่าย

ใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบสั่งซื้อที่สร้างขึ้นเมื่อมีการรับผลิตภัณฑ์หรือบริการตามใบสั่งซื้อที่วางไว้กับผู้จัดจำหน่าย ภาพรวมใบแจ้งหนี้ของผู้จัดจำหน่ายประกอบด้วยหัวข้อและหนึ่งรายการขึ้นไปสำหรับสินค้าหรือบริการ ใบแจ้งหนี้ของผู้จัดจำหน่ายทำให้วงจรจากใบสั่งซื้อไปยังใบรับสินค้าไปยังใบแจ้งหนี้ของผู้จัดจำหน่ายเสร็จสมบูรณ์

ถึงแม้ว่าบางใบแจ้งหนี้ของผู้จัดจำหน่ายจะเชื่อมโยงกับใบสั่งซื้อ ใบแจ้งหนี้ของผู้จัดจำหน่ายยังอาจประกอบด้วยรายการที่ไม่เกี่ยวข้องกับรายการใบสั่งซื้อ คุณยังสามารถสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายที่ไม่ได้เชื่อมโยงกับใบสั่งซื้อใด ๆ ใบแจ้งหนี้ผู้จัดจำหน่ายเหล่านี้อาจแสดงถึงบริการที่ต่อเนื่อง เช่น ใบเรียกเก็บเงินยูทิลิตี้ คุณไม่มีสิทธิ์อ้างอิงใบสั่งซื้อเมื่อคุณเพิ่มบริการที่ต่อเนื่อง

มีหลายวิธีในการป้อนใบแจ้งหนี้ของผู้จัดจำหน่าย:

- ทะเบียนใบแจ้งหนี้ของผู้จัดจำหน่ายช่วยให้คุณป้อนใบแจ้งหนี้ที่ไม่ต้องอ้างอิงใบสั่งซื้ออย่างรวดเร็ว เพื่อให้คุณสามารถรับรู้รายได้ของค่าใช้จ่าย โดยการใช้สมุดรายวันการอนุมัติใบแจ้งหนี้ของผู้จัดจำหน่าย คุณสามารถเลือกใบแจ้งหนี้เหล่านั้นและลงรายการบัญชีไปยังยอดดุลผู้จัดจำหน่ายเพื่อการย้อนกลับรายได้ที่รับรู้
- สมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายช่วยให้คุณป้อนใบแจ้งหนี้ที่ไม่ต้องอ้างอิงใบสั่งซื้อได้อย่างรวดเร็ว ในขั้นตอนเดียว
- พร้อมกับกลุ่มใบแจ้งหนี้ของผู้จัดจำหน่าย ทะเบียนใบแจ้งหนี้ของผู้จัดจำหน่ายช่วยให้คุณป้อนใบแจ้งหนี้ไปยังการรับรู้ค่าใช้จ่ายได้อย่างรวดเร็ว คุณสามารถเปิดใบสั่งซื้อที่เกี่ยวข้องในภายหลังเพื่อลงรายการบัญชีใบแจ้งหนี้ในบัญชีค่าใช้จ่าย
- ในหน้า **เปิดใบแจ้งหนี้ของผู้จัดจำหน่าย** และ **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** ช่วยให้คุณสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบสั่งซื้อที่ยืนยันแล้ว

การสนทนาต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้หน้า **เปิดใบแจ้งหนี้ของผู้จัดจำหน่าย** หรือ **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** เพื่อสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบสั่งซื้อ

## <a name="understanding-invoice-line-quantities"></a>ทำความเข้าใจกับปริมาณของรายการใบแจ้งหนี้

เมื่อคุณเปิดใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบสั่งซื้อที่เกี่ยวข้อง ระบบสร้างรายการใบแจ้งหนี้จากใบสั่งซื้อ โดยค่าเริ่มต้น ระบบนับปริมาณมาจากใบรับสินค้า อย่างไรก็ตาม คุณสามารถใช้ลักษณะการทำงานเริ่มต้นต่อไปนี้:

- **ปริมาณสินค้าที่รับทันที**– ใช้ตัวเลือกนี้สำหรับการจัดส่งสินค้าบางส่วน ระบบตั้งค่าเริ่มต้นในฟิลด์ **ปริมาณ** จากปริมาณที่ถูกระบุในฟิลด์ **รับทันที** ในใบสั่งซื้อ
- **ปริมาณที่สั่ง**– ใช้ตัวเลือกนี้สำหรับการจัดส่งสินค้าทั้งหมด ระบบตั้งค่าเริ่มต้นในฟิลด์ **ปริมาณ** จากปริมาณที่ถูกระบุในฟิลด์ **ที่สั่ง** ในใบสั่งซื้อ
- **ปริมาณที่ลงทะเบียน** – ใช้ตัวเลือกนี้ถ้าสินค้าจำเป็นต้องมีการลงทะเบียน ตามที่ระบุในหน้า **กลุ่มแบบจำลองสินค้า** ค่าเริ่มต้นในฟิลด์ **ปริมาณ** เป็นปริมาณอัปเดตตามจริงที่ลงทะเบียนไว้
- **ปริมาณในใบรับสินค้า** – ใช้ตัวเลือกนี้ถ้าได้รับใบรับสินค้าสำหรับใบสั่งแล้ว ระบบนำค่าเริ่มต้นในฟิลด์ **ปริมาณ** มาจากปริมาณรวมของใบรับสินค้าที่พร้อมใช้งาน
- **ปริมาณและบริการที่ลงทะเบียน** – ใช้ตัวเลือกนี้ถ้ามีการลงทะเบียนปริมาณในสมุดรายวันการมาถึงสำหรับสินค้าที่เก็บในคลังสินค้าหรือสินค้าที่ไม่ได้เก็บในคลังสินค้า ตัวเลือกนี้ยังประกอบด้วยบริการ โดยไม่คำนึงถึงว่ามีการลงทะเบียน

ถ้านิติบุคคลของคุณใช้การจับคู่ใบแจ้งหนี้ คุณสามารถดูผลลัพธ์ของการจับคู่ปริมาณในคอลัมน์ **การจับคู่ปริมาณในใบรับสินค้า** คุณยังสามารถใช้ปุ่ม **รายละเอียดการจับคู่** บนแท็บ **ตรวจทาน** ของบานหน้าต่างการดำเนินการ เพื่อดูผลลัพธ์ของการจับคู่ปริมาณ

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>การเพิ่มรายการที่ไม่ได้อยู่ในใบสั่งซื้อ

คุณสามารถเพิ่มรายการที่ไม่ได้อยู่ในใบสั่งซื้อไปยังใบแจ้งหนี้ของผู้จัดจำหน่ายได้ คุณต้องเลือกหมายเลขสินค้าหรือประเภทการจัดซื้อ จากนั้นคุณสามารถเพิ่มปริมาณ ราคา และยอดเงินลงในรายการ รายการจะรวมอยู่ในนโยบายการจับคู่สำหรับผลรวมใบแจ้งหนี้เท่านั้น

## <a name="submitting-a-vendor-invoice-for-review"></a>การส่งใบแจ้งหนี้ของผู้จัดจำหน่ายเพื่อตรวจทาน

องค์กรของคุณอาจใช้ลำดับงานเพื่อจัดการกระบวนการตรวจทานสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย การตรวจทานลำดับงานอาจจำเป็นสำหรับส่วนหัวของใบแจ้งหนี้ รายการใบแจ้งหนี้ หรือทั้งสองอย่าง ตัวควบคุมลำดับงานใช้กับส่วนหัวหรือรายการ โดยขึ้นอยู่กับตำแหน่งของการโฟกัสเมื่อคุณเลือกตัวควบคุม แทนปุ่ม **ลงรายการบัญชี** ปุ่ม **ส่ง** แสดงส่งใบแจ้งหนี้ของผู้จัดจำหน่ายโดยใช้กระบวนการตรวจทาน

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>การป้องกันไม่ให้มีการส่งใบแจ้งหนี้ไปยังลำดับงาน 

คุณสามารถป้องกันไม่ให้มีการส่งใบแจ้งหนี้ไปยังลำดับงานได้หลายวิธีดังต่อไปนี้

- **ผลรวมในใบแจ้งหนี้และยอดรวมที่ลงทะเบียนไม่เท่ากัน** บุคคลที่ส่งใบแจ้งหนี้จะได้รับข้อความแจ้งเตือนว่าผลรวมไม่เท่ากัน ข้อความแจ้งเตือนจะให้โอกาสที่จะแก้ไขยอดดุลก่อนที่จะส่งใบแจ้งหนี้ไปที่ลำดับงานอีกครั้ง คุณลักษณะนี้จะพร้อมใช้งาน ถ้าพารามิเตอร์ **ไม่อนุญาตให้ส่งไปที่ลำดับงาน เมื่อยอดรวมในใบแจ้งหนี้และยอดรวมในใบแจ้งหนี้ที่ลงทะเบียนไม่เท่ากัน** บนหน้า **การจัดการคุณลักษณะ** ถูกเปิด 

- **ใบแจ้งหนี้มีค่าธรรมเนียมที่ไม่ได้ปันส่วน** บุคคลที่ส่งใบแจ้งหนี้จะได้รับข้อความแจ้งเตือนว่าใบแจ้งหนี้มีค่าธรรมเนียมที่ไม่ได้ปันส่วน ดังนั้นพวกเขาสามารถแก้ไขใบแจ้งหนี้ได้ก่อนที่จะทำการส่งไปยังลำดับงานอีกครั้ง คุณลักษณะนี้จะพร้อมใช้งาน ถ้าพารามิเตอร์ **ไม่อนุญาตให้ส่งไปที่ลำดับงาน เมื่อมีค่าธรรมเนียมที่ไม่ได้ปันส่วนในใบแจ้งหนี้ของผู้จัดจำหน่าย** บนหน้า **การจัดการคุณลักษณะ** ถูกเปิด

- **ใบแจ้งหนี้มีหมายเลขใบแจ้งหนี้เดียวกันกับใบแจ้งหนี้ที่ลงรายการบัญชีอื่น** บุคคลที่ส่งใบแจ้งหนี้จะได้รับข้อความแจ้งเตือนว่าพบใบแจ้งหนี้ที่มีหมายเลขที่ซ้ำกัน และพวกเขาสามารถแก้ไขได้ก่อนที่จะทำการส่งไปยังลำดับงานอีกครั้ง การแจ้งเตือนนี้จะแสดงขึ้น เมื่อพารามิเตอร์ **ตรวจสอบหมายเลขใบแจ้งหนี้ที่ใช้** ในบัญชีเจ้าหนี้ถูกตั้งค่าเป็น **ปฏิเสธรายการซ้ำ** คุณลักษณะนี้จะพร้อมใช้งาน ถ้า **ไม่อนุญาตให้ส่งไปที่ลำดับงาน เมื่อมีหมายเลขใบแจ้งหนี้อยู่ในใบแจ้งหนี้ที่ลงรายการบัญชีอยู่แล้ว และระบบของคุณไม่ได้ตั้งค่าให้ยอมรับพารามิเตอร์หมายเลขใบแจ้งหนี้ที่ซ้ำกัน** บนหน้า **การจัดการคุณลักษณะ** ถูกเปิด  

## <a name="matching-vendor-invoices-to-product-receipts"></a>การจับคู่ใบแจ้งหนี้ของผู้จัดจำหน่ายกับใบรับสินค้า

คุณสามารถป้อนและบันทึกข้อมูลสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย และคุณสามารถจับคู่รายการใบแจ้งหนี้กับรายการใบรับสินค้า นอกจากนี้คุณยังสามารถจับคู่ปริมาณบางส่วนสำหรับรายการ

คุณสามารถสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายที่ยึดตามสินค้าในรายการใบรับผลิตภัณฑ์ที่ได้รับแล้วถึงวันที่ในปัจจุบัน แม้ว่ายังไม่ได้รับสินค้าทั้งหมดสำหรับใบสั่งซื้อใบใดใบหนึ่ง ตัวอย่างเช่น คุณอาจใช้ตัวเลือกนี้ ถ้าผู้จัดจำหน่ายส่งใบแจ้งหนี้หนึ่งรายการต่อเดือนเพื่อครอบคลุมการจัดส่งทั้งหมดที่ส่งในระหว่างเดือนนั้น แต่ละใบรับสินค้าแสดงถึงการจัดส่งสินค้าบางส่วนหรือทั้งหมดของสินค้าในใบสั่งซื้อ

เมื่อใบแจ้งหนี้อยู่ในลำดับงาน วันที่ผู้อนุมัติสามารถอัพเดตปริมาณในใบแจ้งหนี้ เพื่อให้ใบแจ้งหนี้ตรงกับค่าในฟิลด์ **ปริมาณที่จะจับคู่ระหว่างใบรับสินค้า** โดยให้เลือกคุณลักษณะ **อัปเดตปริมาณในใบแจ้งหนี้เพื่อให้ตรงกับปริมาณในใบรับสินค้าในลำดับงาน** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** และเลือก **เปิดใช้งาน** หากผู้อนุมัติในกระบวนการลำดับงาน ลบการจับคู่ทั้งหมดออกจากใบรับสินค้าทั้งหมดออกจากรายการใบแจ้งหนี้ รายการใบแจ้งหนี้จะถูกลบออก เมื่อไม่ได้เปิดใช้งานคุณลักษณะนี้ ปริมาณในใบแจ้งหนี้จะไม่อัพเดตใบแจ้งหนี้ในลำดับงาน

เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** สำหรับสินค้าแต่ละรายการมีการอัพเดตด้วยยอดรวมของปริมาณที่ได้รับจากใบรับสินค้าที่เลือก ถ้าทั้งคู่ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** และปริมาณ **ยอดค้างส่ง** สำหรับสินค้าทั้งหมดในใบสั่งซื้อเป็น 0 (ศูนย์) สถานะของใบสั่งซื้อจะเปลี่ยนเป็น **ออกใบแจ้งหนี้แล้ว** ถ้าปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** ไม่ใช่ 0 (ศูนย์) สถานะของใบสั่งซื้อยังคงไม่เปลี่ยนแปลง และสามารถป้อนใบแจ้งหนี้เพิ่มเติม

ในตัวเลือกนี้จะสมมุติว่ามีการลงรายการใบรับสินค้าอย่างน้อยหนึ่งรายการในใบสั่งซื้อ ใบแจ้งหนี้ของผู้จัดจำหน่ายจะขึ้นอยู่กับใบรับสินค้าเหล่านี้และจะสะท้อนถึงปริมาณจากเหล่านั้น ข้อมูลด้านการเงินสำหรับใบแจ้งหนี้ยึดตามข้อมูลที่ป้อนเมื่อคุณลงรายการบัญชีใบแจ้งหนี้

สำหรับข้อมูลเพิ่มเติม โปรดดู [บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายและจับคู่กับปริมาณที่ได้รับ](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>ตั้งค่าคอนฟิกงานอัตโนมัติสำหรับลำดับงานในใบแจ้งหนี้ของผู้จัดจำหน่าย เพื่อลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายโดยใช้ชุดงาน

คุณสามารถเพิ่มงานการลงรายการบัญชีอัตโนมัติให้กับลำดับงานใบแจ้งหนี้ของผู้จัดจำหน่าย เพื่อให้มีการประมวลผลใบแจ้งหนี้ในชุดงาน การลงรายการบัญชีใบแจ้งหนี้ในชุดงานจะช่วยให้กระบวนการของลำดับงานดำเนินการต่อไปได้โดยไม่ต้องรอให้มีการลงรายการบัญชีเสร็จสิ้น ซึ่งจะช่วยปรับปรุงประสิทธิภาพโดยรวมของงานทั้งหมดที่ส่งไปยังลำดับงาน

เมื่อต้องการลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายในชุดงาน บนหน้า **การจัดการคุณลักษณะ** เปิดพารามิเตอร์ **การลงรายการบัญชีชุดงานในใบแจ้งหนี้ของผู้จัดจำหน่าย** จะมีการตั้งค่าคอนฟิกลำดับงานในใบแจ้งหนี้ของผู้จัดจำหน่ายโดยไปที่ **บัญชีเจ้าหนี้ > การตั้งค่า > ลำดับงานบัญชีเจ้าหนี้**

คุณสามารถดูการงาน **ลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายโดยใช้ชุดงาน** ในโปรแกรมแก้ไขลำดับงาน โดยไม่คำนึงว่ามีการเปิดใช้งานพารามิเตอร์ **การลงรายการบัญชีชุดงานใบแจ้งหนี้ของผู้จัดจำหน่าย** หรือไม่ เมื่อไม่มีการเปิดใช้งานพารามิเตอร์คุณลักษณะ ใบแจ้งหนี้ที่มี **ลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายโดยใช้ชุดงาน** จะไม่ประมวลผลในลำดับงานจนกว่าจะมีการเปิดใช้งานพารามิเตอร์ งาน **ลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายโดยใช้ชุดงาน** ต้องไม่มีการใช้ในลำดับงานเดียวกันกับงานอัตโนมัติของ **ลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย** นอกจากนี้ งาน **ลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายโดยใช้ชุดงาน** ควรจะเป็นองค์ประกอบสุดท้ายในการตั้งค่าคอนฟิกลำดับงาน

คุณสามารถระบุจำนวนของใบแจ้งหนี้ที่จะรวมไว้ในชุดงาน และจำนวนชั่วโมงที่จะรอก่อนที่จะจัดกำหนดการชุดงานใหม่ โดยไปที่ **บัญชีเจ้าหนี้ > การตั้งค่า > พารามิเตอร์บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > ลำดับงานในใบแจ้งหนี้** 

## <a name="working-with-multiple-invoices"></a>การทำงานกับใบแจ้งหนี้หลายใบ

คุณสามารถทำงานกับใบแจ้งหนี้หลายใบพร้อมกันและลงรายการบัญชีทั้งหมดในเวลาเดียวกัน ถ้าคุณต้องสร้างใบแจ้งหนี้หลายใบ ใช้หน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** ถ้าคุณต้องลงรายการบัญชีและพิมพ์ใบแจ้งหนี้ของผู้จัดจำหน่ายหลายใบ ใช้สมุดรายวันการอนุมัติใบแจ้งหนี้ ถ้าคุณกำลังใช้สมุดรายวันการอนุมัติใบแจ้งหนี้ ใบรับสินค้าอย่างน้อยหนึ่งต้องถูกลงรายการบัญชีสำหรับใบสั่งซื้อ และใบแจ้งหนี้สำหรับใบสั่งซื้อต้องถูกลงรายการบัญชีในทะเบียนใบแจ้งหนี้ ข้อมูลทางการเงินสำหรับใบแจ้งหนี้นั้นมาจากใบแจ้งหนี้ที่ลงรายการบัญชีไว้ในทะเบียน

## <a name="recovering-vendor-invoices-that-are-being-used"></a>การกู้คืนใบแจ้งหนี้ของผู้จัดจำหน่ายที่ใช้งานอยู่

ขณะที่มีการใช้ใบแจ้งหนี้ของผู้จัดจำหน่าย ผู้ใช้อื่นจะไม่สามารถแก้ไขได้ อย่างไรก็ตาม สถานะของใบแจ้งหนี้บางครั้งอาจบ่งชี้ว่ามีการใช้ใบแจ้งหนี้อยู่ แม้ว่าจะไม่มีการแก้ไขอยู่ก็ตาม ตัวอย่างเช่น แอพลิเคชันอาจหยุดตอบสนองในขณะที่ใบแจ้งหนี้กำลังถูกแก้ไข หรือผู้ใช้อาจเผลอเปิดใบแจ้งหนี้อยู่ในแอพลิเคชัน

คุณสามารถใช้หน้า **กู้คืนใบแจ้งหนี้ของผู้จัดจำหน่าย** เพื่อกู้คืนหรือนำใบแจ้งหนี้ของผู้จัดจำหน่ายออกใช้ ที่ได้ถูกใช้มากกว่าสี่ชั่วโมง เพื่อให้สามารถแก้ไขได้ คุณสามารถเปิดหน้านี้ได้จากการนำทาง **งานประจำงวด** หรือไทล์ในพื้นที่ทำงาน **รายการใบแจ้งหนี้ของผู้จัดจำหน่าย** หลังจากการกู้คืนใบแจ้งหนี้ จะพร้อมใช้งานสำหรับการแก้ไขในหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่าย**

คุณสามารถเข้าถึงหน้า **กู้คืนใบแจ้งหนี้ของผู้จัดจำหน่าย** ก็ต่อเมื่อหน้าที่และสิทธิ์ด้านความปลอดภัย **ใช้กู้คืนใบแจ้งหนี้ของผู้จัดจำหน่าย** ถูกกำหนดให้กับคุณ นอกจากนี้ พารามิเตอร์ **อนุญาตการกู้คืนใบแจ้งหนี้ของผู้จัดจำหน่าย** ในหน้า **พารามิเตอร์บัญชีเจ้าหนี้** ต้องถูกเปิด

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>การรีเซ็ตสถานะลำดับงานสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายจาก ไม่สามารถกู้คืนได้เป็นแบบร่าง

อินสแตนซ์ลำดับงานที่หยุดดำเนินการ เนื่องจากมีข้อผิดพลาดที่ไม่สามารถกู้คืนได้จะมีสถานะลำดับงานเป็น **ไม่สามารถกู้คืนได้** เมื่อสถานะของลำดับงานในใบแจ้งหนี้ของผู้จัดจำหน่ายคือ **ไม่สามารถกู้คืนได้** คุณสามารถรีเซ็ตเป็น **แบบร่าง** โดยการเลือก **เรียกคืน** จากนั้น คุณสามารถแก้ไขใบแจ้งหนี้ของผู้จัดจำหน่ายได้ คุณลักษณะนี้จะพร้อมใช้งาน ถ้าพารามิเตอร์ **การรีเซ็ตสถานะลำดับงานของใบแจ้งหนี้ของผู้จัดจำหน่ายจากไม่สามารถกู้คืนได้เป็นแบบร่าง** ในหน้า **การจัดการคุณลักษณะ** ถูกเปิด

คุณสามารถใช้หน้า **ประวัติลำดับงาน** เพื่อรีเซ็ตสถานะของลำดับงานเป็น **แบบร่าง** คุณสามารถเปิดหน้านี้จาก **ใบแจ้งหนี้ของผู้จัดจำหน่าย**  หรือจากการนำทาง **ทั่วไป > การสอบถาม > ลำดับงาน** หากต้องการรีเซ็ตสถานะลำดับงานเป็น **แบบร่าง** เลือก **เรียกคืน** นอกจากนี้ คุณยังสามารถรีเซ็ตสถานะลำดับงานเป็นแบบร่างได้โดยเลือกการดำเนินการ **เรียกคืน** ในหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่าย** หรือ **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** หลังจากที่มีการรีเซ็ตสถานะของลำดับงานเป็น **แบบร่าง** จะกลายเป็นพร้อมใช้งานสำหรับการแก้ไขบนหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่าย**

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>การดูผลรวมในใบแจ้งหนี้บนหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่
คุณสามารถดูผลรวมในใบแจ้งหนี้บนหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** โดยการเปิดใช้งานพารามิเตอร์ **ผลรวมของใบแจ้งหนี้ที่ค้างอยู่บนรายการใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** บนหน้า **พารามิเตอร์บัญชีเจ้าหนี้** 



## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [ข้อมูลใบแจ้งหนี้ที่สำคัญในระบบบัญชีเจ้าหนี้โดยใช้ใบแจ้งหนี้ของผู้จัดจำหน่าย](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [ข้อมูลใบแจ้งหนี้ที่สำคัญในบัญชีเจ้าหนี้โดยใช้สมุดรายวันการอนุมัติ](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [ข้อมูลใบแจ้งหนี้ที่สำคัญในระบบบัญชีเจ้าหนี้โดยใช้กลุ่มใบแจ้งหนี้](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายในสมุดรายวันใบแจ้งหนี้](tasks/record-vendor-invoice-invoice-journal.md)
