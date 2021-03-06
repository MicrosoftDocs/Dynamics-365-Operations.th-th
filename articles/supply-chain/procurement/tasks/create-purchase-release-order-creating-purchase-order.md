---
title: สร้างใบสั่งซื้อที่นำออกใช้เมื่อสร้างใบสั่งซื้อ
description: 'ขั้นตอนนี้แสดงวิธีการใช้ข้อตกลงการซื้อเมื่อคุณสร้างใบสั่งซื้อ '
author: RichardLuan
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f82cabebea5c9e86e898c064c70a0e7a48b49d3
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016614"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a>สร้างใบสั่งซื้อที่นำออกใช้เมื่อสร้างใบสั่งซื้อ

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้แสดงวิธีการใช้ข้อตกลงการซื้อเมื่อคุณสร้างใบสั่งซื้อ  ข้อตกลงการซื้อนั้นจะต้องนำไปใช้เมื่อคุณสร้างใบสั่งซื้อเนื่องจากมีเงื่อนไขทั่วไปที่ควรจะถูกคัดลอกไปยังหัวข้อใบสั่งซื้อ โดยปกติแล้วงานนี้จะถูกดำเนินการโดยตัวแทนจัดซื้อ ตามข้อกำหนดเบื้องต้นสำหรับคำแนะนำนี้ คุณต้องมีข้อตกลงการซื้อที่มีผลบังคับใช้กับข้อผูกมัดเกี่ยวกับปริมาณผลิตภัณฑ์สำหรับผู้จัดจำหน่ายและสินค้า สามารถใช้ขั้นตอนเดียวกันถ้าคุณมีข้อตกลงการซื้อกับชนิดข้อผูกมัดอื่น คุณสามารถรันคำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF ถ้าคุณกำลังใช้ USMF คุณสามารถรันคำแนะนำ "สร้างข้อตกลงการซื้อ" ก่อน เพื่อตั้งค่าเงื่อนไขเบื้องต้นที่จำเป็นสำหรับคำแนะนำนี้


## <a name="create-a-purchase-order"></a>สร้างใบสั่งซื้อ
1. เปิดพื้นที่ทำงานสำหรับการจัดเตรียมใบสั่งซื้อ
2. คลิกใบสั่งซื้อใหม่
3. ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
6. เปิดปิดการขยายของส่วนทั่วไป
7. ในฟิลด์ข้อตกลงการสั่งซื้อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * ข้อตกลงสำหรับผู้จัดจำหน่ายที่มีอยู่ทั้งหมดจะถูกแสดงไว้ที่นี่  ค้นหาข้อตกลงที่มีผลบังคับใช้ตามที่คุณต้องการจะใช้  
8. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
9. คลิก ใช่
10. คลิก ตกลง

## <a name="add-a-line"></a>เพิมรายการ
1. ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า
    * ถ้ามีสินค้าคงคลังหรือขนาดของสถานที่ที่เฉพาะเจาะจงในข้อผูกมัด คุณต้องป้อนข้อมูลเดียวกับรายการใบสั่งซื้อเพื่อให้เป็นไปตามข้อตกลง  
2. ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * ไซต์นั้นอาจถูกเติมข้อมูลด้วยค่าเริ่มต้นจากใบสั่งหรือจากผู้จัดจำหน่ายเป็นที่เรียบร้อยแล้ว  ถ้าเป็นกรณีเช่นนั้นให้ข้ามขั้นตอน  
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
4. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
5. ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข
    * ตรวจสอบความถูกต้องว่าราคานั้นถูกคัดลอกมาจากข้อผูกมัด  

## <a name="look-up-the-commitment"></a>ค้นหาข้อผูกมัด
1. คลิก อัพเดตรายการ
2. คลิก ที่แนบมา
    * คุณสามารถรับรายละเอียดสำหรับข้อตกลงการซื้อได้ที่นี่  ตัวอย่างเช่น คุณสามารถดูราคาและราคาและส่วนลดนั้นคงที่หรือไม่ ซึ่งหมายความว่าถ้าคุณเปลี่ยนแปลงราคาหรือส่วนลดในใบสั่งซื้อไปเป็นค่าอื่นกว่าในข้อผูกมัดนั้น ระบบจะลบลิงค์ ดังนั้นรายการใบสั่งซื้อจะไม่ตอบสนองข้อผูกมัดนั้น  คุณยังสามารถดูถ้าตัวเลือกบังคับใช้ค่าสูงสุดถูกเลือก ซึ่งหมายความว่าปริมาณในข้อผูกมัดนั้นไม่สามารถเกินข้อจำกัดโดยการรวมการซื้อทั้งหมดที่ตอบสนองข้อผูกมัด  
3. ปิดหน้า

## <a name="look-up-the-purchase-agreement"></a>ค้นหาขัอตกลงการซื้อ
1. ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป
2. คลิกข้อตกลงการซื้อ
3. ปิดหน้า
4. ปิดหน้า

