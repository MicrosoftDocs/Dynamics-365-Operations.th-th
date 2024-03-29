---
title: สร้างคำขอใบเสนอราคา
description: 'กระบวนงานนี้แสดงให้คุณเห็นถึงวิธีการสร้างคำขอใบเสนอราคา '
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aed08083d83a47d914ecd6c9421825163c5c467a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673844"
---
# <a name="create-a-request-for-quotation"></a>สร้างคำขอใบเสนอราคา

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงให้คุณเห็นถึงวิธีการสร้างคำขอใบเสนอราคา  โดยทั่วไปจะถูกดำเนินการโดยตัวแทนขาย คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเองได้ คุณต้องตั้งค่าชนิดการร้องขอ ก่อนที่คุณจะเริ่ม เมื่อคุณได้ดำเนินงานนี้เสร็จสมบูรณ์แล้ว และคุณได้สร้างและส่ง RFQ แล้ว จากนั้นคุณสามารถป้อนการตอบต่อหนึ่งผู้จัดจำหน่าย เปรียบเทียบ และให้สัญญา


## <a name="prepare-a-new-rfq"></a>เตรียม RFQ ใหม่
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดซื้อและการจัดหา > คำขอใบเสนอราคา > คำขอใบเสนอราคาทั้งหมด**
2. คลิก **สร้าง**
    ชนิดการซื้อที่พร้อมใช้งานมีดังนี้: ใบสั่งซื้อ (เป็นค่าเริ่มต้น): เอกสารที่ยืนยันข้อเสนอการซื้อผลิตภัณฑ์ หรือการยอมรับข้อเสนอการขายผลิตภัณฑ์ในการแลกเปลี่ยนกับการชำระเงิน ข้อตกลงการซื้อ: ชนิดนี้ถูกเลือกโดยอัตโนมัติถ้าคุณสร้าง RFQ โดยตรงจากใบขอซื้อ ถ้าคุณเลือกตัวเลือกนี้ด้วยตนเอง คุณจะได้รับข้อผิดพลาด ข้อตกลงการซื้อ: ข้อตกลงเพื่อการซื้อปริมาณเฉพาะหรือมูลค่าของผลิตภัณฑ์ตลอดช่วงเวลา ถ้าคุณเลือกตัวเลือกนี้ คุณต้องเลือกช่วงวันที่ใช้กับข้อตกลงการซื้อ  
3. ในฟิลด์ **หัวข้อเอกสาร** ให้พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ **ชนิดการร้องขอ** ให้ป้อนหรือเลือกค่า
    + ถ้าวิธีการให้คะแนนเชื่อมโยงกับชนิดการร้องขอ นี่จะเป็นวิธีการให้คะแนนเริ่มต้นสำหรับ RFQ ที่คุณกำลังสร้าง คุณสามารถเปลี่ยนวิธีการให้คะแนนได้ในภายหลัง  
    + ในฟิลด์ **วันที่จัดส่ง** ให้ป้อนวันที่  
    + เลือกวันที่ที่คุณต้องการได้รับสินค้าที่ร้องขอ  
    + ในฟิลด์ **วันที่และเวลาหมดอายุ** ให้ป้อนวันที่และเวลา  
    + ระบุวันที่และเวลา โดยที่ผู้จัดจำหน่ายต้องตอบสนองต่อ RFQ  
5. ในฟิลด์ **คลังสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง ที่อยู่การจัดส่งจะเป็นค่าเริ่มต้นให้กับที่อยู่คลังสินค้า  
6. คลิก **ตกลง**

## <a name="add-lines"></a>เพิ่มรายการ

หลังจากที่คุณได้ระบุข้อมูลพื้นฐานเกี่ยวกับ RFQ ของคุณ คุณระบุสินค้าหรือบริการที่คุณต้องการให้ผู้จัดจำหน่ายประมูล สินค้าเป็นชนิดรายการเริ่มต้น

1. ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'T0020' ได้  
2. ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข
3. คลิก **เพิ่มรายการ**
4. ในฟิลด์ **ชนิดรายการ** เลือก 'ประเภท' คุณสามารถใช้ชนิดรายการของประเภท เพื่อสร้าง RFQ สำหรับสินค้าหรือบริการที่ไม่มีสินค้าคงคลัง  จากนั้นคุณต้องเลือกชนิดของสินค้าหรือบริการจากลำดับของประเภทการจัดซื้อ  
5. ในฟิลด์ **ประเภทการจัดซื้อ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
6. ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้พิมพ์ค่า
7. ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข
8. ในฟิลด์ **หน่วย** ให้ป้อนหรือเลือกค่า

## <a name="add-vendors"></a>เพิ่มผู้จัดจำหน่าย
1. คลิก **ส่วนหัว** เพื่อเปลี่ยนจากมุมมองรายการ เป็นมุมมองส่วนหัว 
2. ขยายส่วน **ผู้จัดจำหน่าย**
3. คลิก **เพิ่มผู้จัดจำหน่ายโดยอัตโนมัติ** คุณสามารถเพิ่มผู้จัดจำหน่ายไปยัง RFQ ได้โดยอัตโนมัติ ตามประเภทการจัดซื้อของสินค้าที่ร้องขอได้  ถ้าไม่มีผู้จัดจำหน่ายใดได้รับอนุมัติสำหรับชนิด ซึ่งรวมถึงรายการที่คุณเพิ่มให้กับผู้จัดจำหน่ายโดยอัตโนมัติ  
4. คลิก **เพิ่ม**
5. ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
6. คลิก **เพิ่ม**
7. ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง เมื่อคุณได้เลือกผู้จัดจำหน่าย สถานะจะเป็น สร้างแล้ว ซึ่งหมายความว่า ข้อมูลของผู้จัดจำหน่ายที่ได้รับการบันทึกใน RFQ แล้ว แต่คุณยังไม่ได้ส่ง RFQ ไปยังผู้จัดจำหน่าย คุณสามารถเพิ่มผู้จัดจำหน่ายให้กับ RFQ ได้โดยไม่ต้องคำนึงถึงสถานะของผู้จัดจำหน่าย  

## <a name="send-the-rfq-to-vendors"></a>ส่ง RFQ ไปยังผู้จัดจำหน่าย
1. บน **บานหน้าต่างการดำเนินการ** คลิก **ส่ง** ในหน้าการส่งคำขอใบเสนอราคา คลิกผู้จัดจำหน่ายในรายการซึ่งเป็นผู้จัดจำหน่ายที่คุณต้องการได้รับ RFQ  
2. คลิก **พิมพ์** กล่องโต้ตอบนี้อนุญาตให้คุณพิมพ์ RFQ ได้  ถ้าคุณเลือกที่จะพิมพ์แผ่นงานการตอบ เนื้อหาของแผ่นงานนี้จะถูกกำหนดไว้ในพารามิเตอร์การจัดซื้อและการจัดหา  เพื่อเลือกวิธีการพิมพ์แผ่นงานการตอบ หลังจากที่คุณได้เปิดกล่องโต้ตอบการพิมพ์ คลิกตัวเลือกการพิมพ์ขั้นสูง หนึ่งรายการจะถูกพิมพ์สำหรับผู้จัดจำหน่ายแต่ละราย ซึ่งประกอบด้วยรายการที่มีสถานะเป็น สร้างแล้วหรือถูกส่ง ระบบจะไม่พิมพ์บรรทัดที่ถูกยกเลิกและบรรทัดที่มีการตอบที่ลงทะเบียนแล้ว   
3. คลิก **ยกเลิก**
4. คลิก **ตกลง**
5. ปิดหน้า
6. ปิดหน้า

## <a name="view-the-rfq-journal"></a>ดูสมุดรายวัน RFQ
1. ไปที่ **การจัดซื้อและการจัดหา > คำขอใบเสนอราคา > การติดตามผลคำขอใบเสนอราคา > สมุดรายวันคำขอใบเสนอราคา**
2. คลิก **ตัวอย่างก่อนพิมพ์/พิมพ์**
3. คลิก **ตัวอย่างก่อนพิมพ์ของต้นฉบับ**
4. ปิดหน้า
5. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]