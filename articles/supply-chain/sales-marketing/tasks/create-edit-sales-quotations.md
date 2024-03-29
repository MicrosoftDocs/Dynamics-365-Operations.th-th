---
title: สร้างและแก้ไขใบเสนอราคาขาย
description: 'กระบวนงานนี้อธิบายวิธีการสร้างและปรับปรุงใบเสนอราคาขาย '
author: Henrikan
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c409d294565f89eac95e42f6207573d22859100
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578955"
---
# <a name="create-and-edit-sales-quotations"></a>สร้างและแก้ไขใบเสนอราคาขาย

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้อธิบายวิธีการสร้างและปรับปรุงใบเสนอราคาขาย  คุณสามารถทำตามขั้นตอนเหล่านี้กับข้อมูลของคุณ หรือกับบริษัทข้อมูลสาธิต USMF


## <a name="create-a-sales-quotation"></a>สร้างใบเสนอราคาขาย
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > การขายและการตลาด > ใบสั่งขาย– > ใบสั่งขายทั้งหมด**
2. คลิก **สร้าง**
3. ในฟิลด์ **ประเภทบัญชี** ให้เลือก 'ผู้ที่มีแนวโน้มจะเป็นลูกค้า'
4. ในฟิลด์ **ผู้ที่มีแนวโน้มจะเป็นลูกค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
5. ขยายส่วน **ทั่วไป** เนื่องจากคุณเลือกที่จะสร้างใบเสนอราคาจากข้อมูลของฝ่ายขายและการตลาด ดังนั้นประเภทของใบเสนอราคานี้จะถูกกำหนดเป็น 'ใบเสนอราคาขาย' โดยอัตโนมัติ หากคุณต้องการสร้างใบเสนอราคาสำหรับโครงการ คุณสามารถเข้าถึงได้จากโมดูล **การจัดการและการบัญชีโครงการ**
6. คลิก **ตกลง** ฟิลด์และการดำเนินการต่างๆบนรายการใบเสนอราคาจะคล้ายกันมากกับในรายการใบสั่งขาย    เช่นเดียวกับใบสั่งขาย ใบเสนอราคาสามารถสร้างขึ้นได้สำหรับสินค้าหนึ่งๆ หรือเมื่อไม่ทราบหมายเลขสินค้า หรือไม่ปรากฏอยู่ในเวลาการสร้างใบเสนอราคา ใบเสนอราคาจะสามารถสร้างขึ้นได้สำหรับประเภทการขาย     
7. ในฟิลด์ **สินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
8. ในฟิลด์ **ไซต์** ให้พิมพ์ค่า
9. ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข ถ้ามีข้อตกลงทางการค้าที่ถูกต้องสำหรับสินค้าที่เลือกไว้ในรายการ ราคาและส่วนลดที่เกี่ยวข้องจะถูกคัดลอกโดยอัตโนมัติไปยังรายการใบเสนอราคา  ตรวจสอบให้แน่ใจว่า ฟิลด์ราคาต่อหน่วยประกอบด้วยค่าและคุณยังสามารถป้อนมูลค่าส่วนลดได้ด้วยถ้าคุณต้องการ 
10. คลิก **บันทึก**
11. ใน **บานหน้าต่างการดำเนินการ** ให้คลิก **ใบเสนอราคาขาย**.
12. คลิก **ผลรวม**
13. คลิก **ตกลง**
14. ให้เลือก ใบเสนอราคาขาย
15. ใน **บานหน้าต่างการดำเนินการ** ให้คลิก **ใบเสนอราคา**
16. ให้คลิก **การจำลองราคา**
    - ในหน้า **เริ่มต้นการจำลองราคา** คุณสามารถจำลองราคาได้โดยการใส่ตัวเลขรายได้ที่คาดหวัง หรือความเป็นไปได้ในการทำกำไรจากใบเสนอราคาของคุณ โดยขึ้นอยู่กับค่าตัวเลขของราคาต่อหน่วย ส่วนลดราคา ส่วนลดแบบร้อยละ จำนวนรวม จำนวนขั้นต้น หรืออัตราส่วนเงินสมทบตามที่คุณต้องการ เมื่อคุณพอใจกับตัวเลขเป้าหมาย คุณนำคำแนะนำไปใช้กับรายการใบเสนอราคา และฟิลด์ที่เกี่ยวข้องกับราคานั้นจะถูกอัพเดตให้สอดคล้องกัน  
    - คุณสามารถสร้างการจำลองราคาได้มากเท่าที่คุณต้องการ เมื่อคุณคลิกที่ **สร้าง** เงื่อนไขราคาเดิมจากใบเสนอราคาปัจจุบันจะถูกคัดลอกไปที่หน้านั้น จากนั้นคุุณจะสามารถแก้ไขค่าในฟิลด์ใดๆของที่เกี่ยวข้องกับราคาเป็นราคาเป้าหมาย  การเปลี่ยนแปลงในฟิลด์ใดฟิลด์หนึ่งจะทริกเกอร์การคำนวณใหม่ในการคำนวณอื่นๆ ทั้งหมด  เพื่อให้ระบบคำนวณกำไรการขายและอัตราส่วนกำไรผันแปร ต้นทุนต่อหน่วยของผลิตภัณฑ์ได้จะต้องถูกแจ้งให้ทราบ  ใช้แท็บการจำลองราคาสำหรับมุมมองโดยละเอียดของราคาเดิม การเปลี่ยนแปลงที่ถูกเสนอ และผลกระทบต่อผลรวมของใบเสนอราคา  ตามกฎทั่วไป เมื่อการจำลองที่กำหนดยอดเงินใหม่ได้นำมาใช้กับรายการใบเสนอราคา ระบบจะคำนวณใหม่อีกครั้งและป้อนค่าใหม่ในฟิลด์ราคาต่อหน่วย  เมื่อมีการจำลองตามกำไรเบื้องต้นใหม่หรืออัตราส่วนกำไรผันแปรใหม่ เฉพาะฟิลด์ยอดเงินสุทธิเท่านั้นที่จะได้รับการอัพเดต และราคาต่อหน่วยเป็นจะเป็นช่องว่าง  ในทั้งสองกรณี ส่วนลดใดๆที่เคยอยู่บนรายการใบเสนอราคาก่อนการจำลองจะถูกลบออก
17. ใน **บานหน้าต่างการดำเนินการ** ให้คลิก **ใบเสนอราคา**
18. คลิก **ส่งใบเสนอราคา**
19. เลือก 'ใช่' ในช่อง **พิมพ์ใบเสนอราคา**
20. คลิก **ตกลง** รายงานอาจใช้เวลาสักครู่เพื่อที่สร้าง  อย่าปิดหน้าจนกว่าจะเสร็จสิ้น

## <a name="update-a-sales-quotation"></a>อัพเดตใบเสนอราคาขาย
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > การขายและการตลาด > ใบสั่งขาย– > ใบสั่งขายทั้งหมด**
2. ใบ **บานหน้าต่างการดำเนินการ** ให้คลิก **ติดตาม**
3. ให้คลิก **แปลงเป็นลูกค้า**
4. ในฟิลด์ **บัญชีลูกค้า** ให้พิมพ์ค่าใดค่าหนึ่ง
5. คลิก **ตรวจสอบ** ตรวจสอบให้แน่ใจว่า คุณเห็นข้อความที่ว่าหมายเลขบัญชีที่คุณพิมพ์สามารถใช้ได้โดยอิสระ  
6. คลิก **ตกลง** ขณะนี้ระบบได้สร้างบัญชีลูกค้าใหม่สำหรับผู้ที่มีแนวโน้มจะเป็นลูกค้าบนใบเสนอราคา  
7. ปิดหน้า
8. ใบ **บานหน้าต่างการดำเนินการ** ให้คลิก **ติดตาม**
9. คลิก **ยืนยัน**
10. ในฟิลด์ **เหตุผล** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
11. คลิก **ตกลง**
12. บน **หน้าต่างการดำเนินการ** คลิก **ทั่วไป**
13. คลิก **ใบสั่งขาย**
14. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]