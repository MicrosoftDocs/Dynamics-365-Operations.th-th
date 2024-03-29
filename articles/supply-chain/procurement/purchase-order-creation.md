---
title: การสร้างใบสั่งซื้อ
description: บทความนี้อธิบายกระบวนการและตัวเลือกเมื่อคุณสร้างใบสั่งซื้อด้วยตนเอง
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70050efb31040f2c7ebfc55681a7145e313d804d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674378"
---
# <a name="create-purchase-orders"></a>การสร้างใบสั่งซื้อ

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายกระบวนการและตัวเลือกเมื่อคุณสร้างใบสั่งซื้อด้วยตนเอง

เมื่อคุณสร้างใบสั่งซื้อ (PO) รายละเอียดทั่วไปเกี่ยวกับใบสั่งทั้งหมดจะถูกระบุในส่วนหัวของ PO และจากนั้นคุณสามารถเพิ่มรายการ PO อย่างน้อยหนึ่งรายการได้ บทความนี้อธิบายเกี่ยวกับตัวเลือกบางตัวเลือกที่ใช้บ่อยที่สุดที่พร้อมใช้งาน  

คุณยังสามารถสร้าง PO ได้โดยการคัดลอกรายการจากเอกสาร PO อื่นหรือใบสั่งขาย ในกรณีนี้ คุณสามารถกลับเครื่องหมายสำหรับสินค้าคงคลัง เนื่องจากคุณจะกลับเครื่องหมายสำหรับใบแจ้งหนี้เพื่อบ่งชี้ใบลดหนี้  

ถึงแม้ว่าคุณสามารถสร้าง PO ด้วยตนเองได้ โดยทั่วไปแล้ว PO จะถูกสร้างขึ้นจากกระบวนการอื่นๆ ใบสั่งสามารถถูกสร้างขึ้นโดยอัตโนมัติโดยยึดตามเอกสารอื่นๆ เช่น ใบขอซื้อ อีกวิธีหนึ่งคือ สามารถสร้างโดยเป็นส่วนหนึ่งของกระบวนการวางแผนหลักผ่าน PO ที่วางแผนไว้ ถ้าคุณใช้ข้อตกลงการซื้อ PO จะสามารถถูกสร้างโดยการดำเนินการ **ใบสั่งที่นำออกใช้** นอกจากนี้ยังมีวิธีการขั้นสูงเพิ่มเติมสำหรับการสร้างใบสั่งซื้อแบบอัตโนมัติ ตัวอย่างเช่น ใบสั่งสามารถสร้างขึ้นเมื่อคุณใช้การจัดส่งโดยตรงหรือกลุ่มใบสั่งระหว่างบริษัท

## <a name="creating-a-purchase-order-header"></a>การสร้างส่วนหัวของใบสั่งซื้อ
เมื่อคุณสร้าง PO ใหม่ กล่องโต้ตอบจะปรากฏขึ้น ซึ่งคุณสามารถป้อนข้อมูลทั่วไปสำหรับส่วนหัวของ PO เมื่อคุณคลิก **ตกลง** เพื่อปิดกล่องโต้ตอบ ใบสั่งจะถูกสร้างขึ้น และจากนั้นคุณสามารถระบุข้อมูลเพิ่มเติมในส่วนหัวนี้  

รายละเอียดแรกที่คุณต้องพิจารณาเมื่อคุณสร้างใบสั่งซื้อคือชนิดของใบสั่ง ชนิด **ใบสั่งซื้อ** จะใช้บ่อยที่สุด อย่างไรก็ตาม ถ้าจำเป็นต้องมีใบแจ้งหนี้เงินเชื่อ คุณสามารถใช้ชนิด **ใบสั่งที่ส่งคืน** ได้  

คุณต้องระบุซัพพลายเออร์ในฟิลด์ **บัญชีผู้จัดจำหน่าย** สำหรับฟิลด์นี้ คุณสามารถค้นหาบัญชีผู้ใช้หรือชื่อของผู้จัดจำหน่าย ถ้าผู้จัดจำหน่ายจัดส่งสินค้าจากที่ตั้งหลายแห่ง แต่ใช้บัญชีใบแจ้งหนี้เดียว คุณสามารถเลือกบัญชีใบแจ้งหนี้นั้นในฟิลด์ **บัญชีใบแจ้งหนี้** และใช้กับบัญชีผู้จัดจำหน่ายอื่นได้ ถ้าคุณต้องสร้าง PO สำหรับผลิตภัณฑ์ที่จะไม่มีการสั่งซื้อซ้ำๆ คุณสามารถใช้ตัวเลือก **ซัพพลายเออร์ขาจร** ตัวเลือกนี้จะสร้างบัญชีผู้จัดจำหน่ายใหม่ที่ถูกทำเครื่องหมายเป็นบัญชีการสั่งซื้อครั้งเดียว เพื่อสนับสนุนกระบวนการล้างข้อมูลในภายหลังสำหรับบัญชีการสั่งซื้อครั้งเดียวในโมดูล **บัญชีเจ้าหนี้** เมื่อคุณเลือกบัญชีผู้จัดจำหน่าย ฟิลด์หลายรายการในส่วนหัวของ PO จะสืบทอดค่าเริ่มต้นจากข้อมูลที่เกี่ยวข้องกับบัญชีผู้จัดจำหน่าย ตัวอย่างเช่น ไซต์การจัดส่งเริ่มต้นและคลังสินค้าจะถูกคัดลอกจากข้อมูลผู้จัดจำหน่าย อย่างไรก็ตาม คุณสามารถแทนค่าเริ่มต้นเหล่านี้ถ้าการซื้อมีไว้สำหรับตำแหน่งที่ตั้งอื่น  

หากซัพพลายเออร์ได้ระบุหมายเลขอ้างอิงสำหรับใบสั่ง คุณสามารถบันทึกข้อมูลนี้ในฟิลด์ **การอ้างอิงผู้จัดจำหน่าย** สำหรับใบสั่งที่ส่งคืน คุณต้องระบุค่าในฟิลด์ **RMA** เพื่ออ้างอิงการตรวจสอบของผู้จัดจำหน่ายสำหรับการประมวลผลการส่งคืน  

ถ้าข้อตกลงการซื้อเชื่อมโยงกับใบสั่ง คุณต้องระบุข้อมูลนี้ในฟิลด์ **ข้อตกลงการซื้อ**  

ส่วนหัวของ PO ยังประกอบด้วยข้อมูลเกี่ยวกับค่าธรรมเนียมที่ใช้กับคำสั่งทั้งหมดแทนรายการเดียว ค่าธรรมเนียมสามารถถูกเพิ่มโดยอัตโนมัติไปยังใบสั่งถ้ามีการตั้งค่าค่าธรรมเนียมอัตโนมัติสำหรับผู้จัดจำหน่ายหรือกลุ่มค่าธรรมเนียมของผู้จัดจำหน่าย คุณยังสามารถเพิ่มค่าธรรมเนียมด้วยตนเองไปยังส่วนหัวของใบสั่งโดยการคลิก **รักษาค่าธรรมเนียม** บนบานหน้าต่างการดำเนินการได้

## <a name="adding-purchase-order-lines"></a>การเพิ่มรายการใบสั่งซื้อ
PO สามารถใช้สำหรับผลิตภัณฑ์ที่มีอยู่จริงหรือสำหรับการบริการได้ การตั้งค่าบนกลุ่มโมเดลสินค้าคงคลังเป็นตัวกำหนดว่าหมายเลขสินค้าเฉพาะจะใช้กับผลิตภัณฑ์หรือการบริการหรือไม่ โดยปกติ มีการระบุสินค้าที่ซื้อด้วยหมายเลขสินค้า อย่างไรก็ตาม ถ้าใบสั่งมีไว้สำหรับผลิตภัณฑ์หรือการบริการที่ถูกใช้โดยตรง คุณยังสามารถระบุสินค้าโดยใช้ประเภทการจัดซื้อ  

รายการ PO ประกอบด้วยฟิลด์จำนวนมาก แต่ฟิลด์ส่วนใหญ่เหล่านี้มีค่าเริ่มต้นหรือค่าที่ได้รับมาจากส่วนหัวของใบสั่ง ฟิลด์เพิ่มเติมจะถูกตั้งค่าเมื่อคุณเลือกผลิตภัณฑ์หรือบริการ ฟิลด์ที่ถูกตั้งค่าด้วยตนเองบ่อยที่สุดประกอบด้วยฟิลด์สำหรับหมายเลขสินค้า ปริมาณ และวันที่จัดส่งที่ร้องขอ ข้อมูลเกี่ยวกับหน่วยราคาและส่วนลดก็มีความสำคัญมากเช่นกัน แต่ค่าของฟิลด์เหล่านั้นมักถูกกำหนดโดยข้อตกลงทางการค้าหรือข้อตกลงการซื้อ  

เมื่อคุณเลือกผลิตภัณฑ์ คุณสามารถค้นหาในชื่อผลิตภัณฑ์ทั้งหมดหรือบางส่วนแทนการใช้หมายเลขสินค้า ถ้าผลิตภัณฑ์มีตัวแปรหลายรายการ เช่น ขนาดที่แตกต่างกัน คุณสามารถดูภาพรวมของตัวแปรที่พร้อมใช้งานได้โดยใช้ฟังก์ชัน **เพิ่มบรรทัด** หรือโดยการใช้การค้นหาที่มีอยู่ในฟิลด์ **หมายเลขตัวแปร**  

บ่อยครั้ง คุณจะต้องระบุมิติต่างๆ สำหรับสินค้าที่เลือกในรายการ PO แต่ละรายการ มิติที่คุณต้องระบุขึ้นอยู่กับกลุ่มมิติที่ได้รับมอบหมายให้กับคำนิยามผลิตภัณฑ์หลัก ตัวอย่างเช่น คุณมักจะต้องระบุไซต์และคลังสินค้าเพื่อบ่งชี้สถานที่ที่ควรจะจัดส่งผลิตภัณฑ์ คุณระบุผลิตภัณฑ์ย่อยได้โดยการระบุหมายเลขตัวแปร หรือโดยการป้อนค่าสำหรับมิติของผลิตภัณฑ์อย่างน้อยหนี่งชนิด เช่น สี ขนาด โครงแบบ หรือลักษณะ มิติการติดตาม เช่น ชุดงานและหมายเลขชุด ช่วยให้คุณสามารถระบุล็อตสินค้าคงคลังแต่ละรายการได้ หลังจากที่คุณได้สร้างใบสั่ง คุณสามารถรวบรวมค่ามิติในใบสั่งโดยใช้การดำเนินการ **การลงทะเบียน** ตัวอย่างเช่น คุณได้สั่งซื้อสินค้าปริมาณ 5 ชิ้น ในภายหลัง คุณลงทะเบียนให้สินค้าสามชิ้นเป็นสีดำ และสองชิ้นเป็นสีน้ำเงิน วิธีนี้เป็นทางเลือกในการรวบรวมข้อมูลมิติในระหว่างการลงทะเบียนการมาถึง  

คุณสามารถตรวจสอบรายละเอียดของสถานะของธุรกรรมสินค้าคงคลังสำหรับผลิตภัณฑ์ที่เก็บในคลัง ตัวอย่างเช่น คุณอาจต้องการตรวจสอบปริมาณคงคลังคงเหลือที่จะช่วยให้คุณตัดสินใจว่าจะสั่งจำนวนเท่าใด อีกวิธีหนึ่งคือ คุณอาจต้องการตรวจสอบสถานะสินค้าคงคลังของปริมาณที่สั่งเพื่อดูว่าการลงทะเบียนการมาถึงขาเข้าเกิดขึ้นหรือไม่  

รายการ PO ที่ใช้ในการส่งคืนผลิตภัณฑ์ไปยังผู้จัดจำหน่ายจะมีปริมาณติดลบ คุณสามารถเลือกล็อตการส่งคืนสินค้าพิเศษได้โดยใช้การดำเนินการ **การจอง**  

บางครั้ง คุณอาจต้องการแบ่งปริมาณที่คุณสั่ง เพื่อให้ส่วนต่างๆ เหล่านั้นถูกส่งในวันที่แตกต่างกัน คุณสามารถตั้งค่าการจัดส่งเหล่านี้โดยใช้การดำเนินการ **กำหนดการจัดส่ง** ซึ่งจะพร้อมใช้งานบนเมนู **รายการใบสั่งซื้อ** ในมุมมอง **รายการ**  

ค่าธรรมเนียมสามารถถูกเพิ่มโดยอัตโนมัติไปยังรายการ PO ถ้ามีการตั้งค่าค่าธรรมเนียมอัตโนมัติสำหรับผู้จัดจำหน่ายหรือกลุ่มค่าธรรมเนียมของผู้จัดจำหน่าย และสำหรับสินค้าหรือกลุ่มค่าธรรมเนียมสินค้า อย่างไรก็ตาม โดยทั่วไปแล้ว ค่าธรรมเนียมจะถูกเพิ่มด้วยตนเองในระดับรายการใบสั่ง เมื่อต้องการเพิ่มค่าธรรมเนียม เปิดหน้า **รักษาค่าธรรมเนียม** โดยใช้การดำเนินการ **รักษาค่าธรรมเนียม** บนเมนู **การเงิน** ในมุมมอง **รายการ** ข้อได้เปรียบของการเพิ่มค่าธรรมเนียมโดยตรงในระดับรายการใบสั่งคือสามารถปันส่วนค่าธรรมเนียมเป็นต้นทุนสินค้าคงคลังได้ เมื่อต้องการตั้งค่ารหัสค่าธรรมเนียมเป็นต้นทุนผลิตภัณฑ์บัญชี ใช้ตัวเลือกเดบิต **สินค้า** ชนิดของค่าธรรมเนียมเหล่านี้ต้องได้รับการแบ่งส่วนจากส่วนหัวของ PO ไปยังรายการต่างๆ ก่อนที่จะได้รับการยืนยันใบสั่ง ตัวอย่างเช่น คุณอาจต้องการปันส่วนค่าธรรมเนียมโดยขึ้นอยู่กับปริมาณในแต่ละรายการ ประเภทของค่าธรรมเนียมยังมีผลต่อวิธีการลงบัญชีค่าธรรมเนียม ตัวอย่างเช่น ค่าธรรมเนียมคงที่จะระบุยอดเงินคงที่ และเปอร์เซ็นต์ค่าธรรมเนียมจะถูกคำนวณเป็นเปอร์เซ็นต์ของยอดเงินสุทธิสำหรับรายการใบสั่ง PO สามารถถูกกำหนดให้กับการบรรทุก และการบรรทุกอาจรวมการประเมินค่าใช้จ่ายที่คาดไว้สำหรับต้นทุนการขนส่ง คุณสามารถปันส่วนค่าใช้จ่ายนี้จากการบรรทุกกลับไปยังรายการ PO

## <a name="purchase-order-actions"></a>การดำเนินการกับใบสั่งซื้อ
หลังจากที่คุณได้เพิ่มส่วนหัวและรายการไปยัง PO แล้ว คุณจะต้องดำเนินการขั้นตอนเพิ่มเติมให้เสร็จสิ้นก่อนที่ใบสั่งดังกล่าวจะพร้อมสำหรับการยืนยัน เนื่องจากมีตัวเลือกหลายตัวเลือก คุณอาจพบว่ามีประโยชน์เมื่อต้องการใช้ [การค้นหาการดำเนินการ](../../fin-ops-core/fin-ops/get-started/action-search.md) เพื่อค้นหารายการเมนูที่เกี่ยวข้อง  

คุณสามารถตั้งค่าคอนฟิกผลิตภัณฑ์ในใบสั่งเพื่อให้มีสินค้าเสริม สินค้าเสริมคือผลิตภัณฑ์ที่ต้องหรือสามารถซื้อร่วมกับผลิตภัณฑ์อื่น สินค้าเสริมอาจถูกเพิ่มโดยไม่มีค่าธรรมเนียมเป็นผลิตภัณฑ์ที่มาพร้อมกัน หรือคุณสามารถตัดสินใจว่าจะเพิ่มลงในใบสั่งหรือไม่ก็ได้ คุณสามารถตรวจทานสินค้าเสริมหลังจากที่แต่ละรายการใบสั่งถูกเพิ่ม อย่างไรก็ตาม คุณอาจพบว่าสะดวกมากกว่าที่จะตรวจทานและเพิ่มสินค้าเสริมที่เกี่ยวข้องสำหรับรายการใบสั่งทั้งหมดโดยใช้หน้า **สินค้าเสริม** ซึ่งคุณสามารถเปิดได้จากบานหน้าต่างการดำเนินการ  

ส่วนลดจะถูกเพิ่มไปยังรายการเมื่อถูกสร้าง อย่างไรก็ตาม จะมีการนำส่วนลดสองสามรายการไปใช้กับใบสั่งทั้งหมด:

-   การดำเนินการ **ส่วนลดรวม** จะคำนวณเปอร์เซ็นต์ส่วนลดรวมที่ใช้กับใบสั่งทั้งหมด อย่าสับสนส่วนลดนี้กับเปอร์เซ็นต์ส่วนลดเงินสด ส่วนลดเงินสดจะถูกใช้เมื่อมีการชำระใบแจ้งหนี้ และขึ้นอยู่กับการชำระเงินตามวันที่ระบุ
-   ถ้าส่วนลดหลายรายการถูกนำไปใช้ คุณจะต้องใช้การดำเนินการ **ส่วนลดต่อสินค้าหลายรายการ** เพื่อคำนวณและกำหนดให้กับใบสั่ง ส่วนลดต่อสินค้าหลายรายการคือส่วนลดที่สามารถเสนอได้ถ้าผลิตภัณฑ์ที่คละกันในใบสั่งเกินกว่าขีดจำกัดร่วมกัน มีเพียงไม่กี่บริษัทที่ใช้ส่วนลดชนิดนี้

ค่าธรรมเนียมที่มีรหัสค่าธรรมเนียมที่ใช้ชนิดเดบิต **สินค้า** ต้องถูกกำหนดให้กับระดับรายการก่อนที่ใบสั่งจะได้รับการยืนยัน คุณอาจพบว่าเป็นเรื่องที่สะดวกที่จะกำหนดค่าธรรมเนียมเหล่านี้ในระดับส่วนหัวของใบสั่ง เพื่อให้คุณสามารถระบุยอดเงินรวมของค่าธรรมเนียม อย่างไรก็ตาม ในกรณีนี้ ค่าธรรมเนียมจะต้องถูกปันส่วนไปยังแต่ละรายการก่อนที่ใบสั่งจะได้รับการยืนยัน คุณสามารถใช้การดำเนินการ **ปันส่วนค่าธรรมเนียม** เพื่อแบ่งยอดเงินจากค่าธรรมเนียมที่จะถูกกำหนดที่ระดับส่วนหัวไปยังรายการใบสั่ง สามารถแบ่งค่าธรรมเนียมตามยอดเงินสุทธิของแต่ละรายการตามปริมาณที่ได้สั่งซื้อหรือข้ามรายการใบสั่งเท่าๆ กัน หลังจากที่คุณได้ปันส่วนค่าธรรมเนียมให้กับรายการต่างๆ แล้ว ค่าธรรมเนียมจะถูกนำออกจากส่วนหัวของใบสั่ง  

PO สามารถถูกกำหนดค่าเพื่อกำหนดให้เงินงบประมาณถูกปันส่วนไปยังใบสั่งก่อนที่จะสามารถประมวลผลได้ ในกรณีนี้ คุณสามารถใช้การดำเนินการ **การตรวจสอบงบประมาณ** เพื่อปันส่วนงบประมาณ  

คุณอาจต้องการให้การดำเนินการกับ PO เสร็จสิ้นล่าช้า ตัวอย่างเช่น คุณอาจต้องการข้อมูลเพิ่มเติมเกี่ยวกับผลิตภัณฑ์หรือการบริการ หรือคุณอาจจำเป็นต้องได้รับการตรวจสอบสำหรับการใช้จ่าย มีหลายวิธีเพื่อเก็บใบสั่งคืน ตัวอย่างเช่น คุณสามารถรอเพื่อยืนยันใบสั่ง อีกวิธีหนึ่งคือ ถ้ามีการใช้ลำดับงานการจัดการการเปลี่ยนแปลง อย่าส่งใบสั่งเพื่อรอการอนุมัติ ถ้าคุณต้องการบล็อคใบสั่งทั้งหมดสำหรับผู้จัดจำหน่ายเฉพาะ คุณสามารถทำเครื่องหมายผู้จัดจำหน่ายเป็น **คงค้าง** สำหรับการประมวลผลในข้อมูลหลักของผู้จัดจำหน่ายได้ นอกจากนี้ยังมีสถานการณ์ที่อาจป้องกันไม่ให้ใบสั่งถูกประมวลผล ตัวอย่างเช่น คุณสามารถป้องกันไม่ให้มีการประมวลผลได้ถ้าเกินวงเงินสินเชื่อหรือถ้าไม่มีเงินงบประมาณที่จำเป็น

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมใบสั่งซื้อ](purchase-order-overview.md)

[อนุมัติและยืนยันใบสั่งซื้อ](purchase-order-approval-confirmation.md)

[ใบรับสินค้า - ใบสั่งซื้อ](product-receipt-against-purchase-orders.md)

[ภาพรวมของใบแจ้งหนี้ของผู้จัดจำหน่าย](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]