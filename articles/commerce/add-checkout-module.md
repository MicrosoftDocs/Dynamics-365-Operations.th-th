---
title: โมดูลเช็คเอาท์
description: บทความนี้จะอธิบายถึงวิธีการเพิ่มโมดูลการชำระเงินให้กับหน้าและตั้งค่าคุณสมบัติที่จำเป็น
author: anupamar-ms
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 295b99c7012e35a40af34d454ff7082d4100c74a
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746237"
---
# <a name="checkout-module"></a>โมดูลเช็คเอาท์

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

บทความนี้จะอธิบายถึงวิธีการเพิ่มโมดูลการชำระเงินให้กับหน้าและตั้งค่าคุณสมบัติที่จำเป็น

โมดูลการชำระเงินเป็นคอนเทนเนอร์พิเศษที่เป็นโฮสต์สำหรับโมดูลทั้งหมดที่จำเป็นในการสร้างใบสั่ง โดยจะแสดงขั้นตอนแต่ละขั้นตอนของลูกค้าที่ใช้ในการป้อนข้อมูลที่เกี่ยวข้องทั้งหมดเพื่อทำการซื้อ โดยจะรวบรวมข้อมูลที่อยู่ที่จัดส่ง วิธีการจัดส่ง และข้อมูลการเรียกเก็บเงิน นอกจากนี้ยังมีสรุปใบสั่งและข้อมูลอื่น ๆ ที่เกี่ยวข้องกับใบสั่งของลูกค้า

โมดูลการชำระเงินแสดงข้อมูลตามรหัสรถเข็น รหัสรถเข็นนี้ถูกบันทึกเป็นคุกกี้ของเบราว์เซอร์ ต้องระบุรหัสรถเข็นเพื่อแสดงข้อมูลในโมดูลการเช็คเอาท์เช่นสินค้าในใบสั่งยอดเงินรวมและส่วนลด 

รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลเช็คเอาท์ Fabrikam บนหน้าเช็คเอาท์

![ตัวอย่างของโมดูลเช็คเอาท์](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>คุณสมบัติของโมดูลเช็คเอาท์

โมดูลการชำระเงินแสดงสรุปใบสั่ง และแสดงให้เห็นถึงฟังก์ชันสำหรับการวางใบสั่ง เมื่อต้องการรวบรวมข้อมูลลูกค้าทั้งหมดที่จำเป็นต้องใช้ก่อนที่จะสามารถวางใบสั่งได้ ต้องเพิ่มโมดูลเพิ่มเติมที่โมดูลการชำระเงิน ดังนั้น ร้านค้าปลีกมีความยืดหยุ่นในการเพิ่มโมดูลที่กำหนดเองไปยังขั้นตอนการเช็คเอาท์ หรือเพื่อแยกโมดูลตามความต้องการ

| ชื่อคุณสมบัติ | มูลค่า | คำอธิบาย |
|----------------|--------|-------------|
| หัวเรื่องการชำระเงิน | ข้อความหัวเรื่องและแท็กหัวเรื่อง (**H1**, **H2**, **H3**, **H4**, **H5** หรือ **H6**) | หัวเรื่องสำหรับโมดูลเช็คเอาท์ |
| หัวเรื่องสรุปใบสั่ง | ข้อความหัวเรื่อง | หัวเรื่องสำหรับส่วนสรุปข้อมูลใบสั่งของโมดูล |
| หัวเรื่องสินค้าในรายการของรถเข็น | ข้อความหัวเรื่อง | หัวเรื่องสำหรับสินค้าในรายการของรถเข็นที่แสดงอยู่ในโมดูลเช็คเอาท์ |
| แสดงค่าธรรมเนียมการจัดส่งของสินค้าในรายการ | **จริง** หรือ **เท็จ** | ถ้ามีการตั้งค่าคุณสมบัตินี้เป็น **จริง** ค่าธรรมเนียมการจัดส่งที่ใช้กับสินค้าในรายการจะแสดงในรายการของรถเข็น หากไม่ได้เปิด **ค่าธรรมเนียมในส่วนหัวที่ไม่มีการแบ่งตามสัดส่วน** ใน Commerce headquarters ค่าธรรมเนียมการจัดส่งจะนำไปใช้ในระดับส่วนหัวไม่ใช่ระดับรายการ คุณลักษณะนี้มีการเพิ่มใน Commerce รุ่น10.0.13 |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>โมดูลที่สามารถใช้ในโมดูลเช็คเอาท์

- **ที่อยู่จัดส่ง** –โมดูลนี้จะช่วยให้ลูกค้าเพิ่มหรือเลือกที่อยู่จัดส่งสำหรับใบสั่ง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลที่อยู่จัดส่ง](ship-address-module.md)

    รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลที่อยู่การจัดส่งบนหน้าเช็คเอาท์

    ![ตัวอย่างของโมดูลที่อยู่จัดส่ง](./media/ecommerce-shippingaddress.PNG)

- **ตัวเลือกการจัดส่ง** – โมดูลนี้จะช่วยให้ลูกค้าสามารถเลือกวิธีการจัดส่งสำหรับใบสั่งได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลตัวเลือกการจัดส่ง](delivery-options-module.md)

    รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกการจัดส่งบนหน้าเช็คเอาท์
 
    ![ตัวอย่างของโมดูลตัวเลือกการจัดส่ง](./media/ecommerce-deliveryoptions.PNG)

- **คอนเทนเนอร์ส่วนการเช็คเอาท์** –โมดูลนี้เป็นคอนเทนเนอร์ที่คุณสามารถใส่หลายโมดูลภายใน เพื่อสร้างส่วนภายในขั้นตอนการชำระเงิน ตัวอย่าง เช่น คุณสามารถกำหนดโมดูลที่เกี่ยวข้องกับการชำระเงินทั้งหมด ภายในคอนเทนเนอร์นี้เพื่อให้ปรากฏเป็นส่วนหนึ่ง โมดูลนี้มีผลเฉพาะกับโครงร่างของเวิร์กโฟลว์เท่านั้น

- **บัตรของขวัญ** –โมดูลนี้จะช่วยให้ลูกค้าชำระเงินสำหรับใบสั่ง โดยใช้บัตรของขวัญ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลบัตรของขวัญ](add-giftcard.md)

- **คะแนนสะสมสำหรับสมาชิก** –โมดูลนี้จะช่วยให้ลูกค้าชำระเงินสำหรับใบสั่งโดยใช้คะแนนสะสมสำหรับสมาชิก โดยจะให้ข้อมูลสรุปของคะแนนที่พร้อมใช้งานและคะแนนที่กำลังจะหมดอายุ และให้ลูกค้าสามารถเลือกจำนวนคะแนนเพื่อใช้แลกรางวัล ถ้าลูกค้าไม่ได้ล็อกอินหรือไม่ใช่สมาชิกสมาชิก หรือถ้ายอดเงินรวมในรถเข็นเป็น 0 (ศูนย์) โมดูลนี้จะถูกซ่อนไว้โดยอัตโนมัติ

- **การชำระเงิน** – โมดูลนี้จะช่วยให้ลูกค้าชำระเงินสำหรับใบสั่ง โดยใช้บัตรเครดิตหรือบัตรเดบิต ลูกค้ายังสามารถระบุที่อยู่สำหรับการเรียกเก็บเงินสำหรับตัวเลือกการชำระเงินที่จะเลือกได้ด้วย สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลการชำระเงิน](payment-module.md)

    รูปภาพต่อไปนี้แสดงตัวอย่างโมดูลบัตรของขวัญ คะแนนสะสมสำหรับสมาชิก และการชำระเงินบนหน้าเช็คเอาท์

    ![ตัวอย่างโมดูลบัตรของขวัญ คะแนนสะสมสำหรับสมาชิก และการชำระเงินบนหน้าเช็คเอาท์](./media/ecommerce-payments.PNG)

- **ข้อมูลการติดต่อ** –โมดูลนี้จะช่วยให้ลูกค้าสามารถเพิ่มหรือเปลี่ยนแปลงข้อมูลการติดต่อ (ที่อยู่อีเมล์) สำหรับใบสั่งได้

- **บล็อกข้อความ** – โมดูลนี้มีการส่งข้อความใด ๆ ที่ขับเคลื่อนโดยระบบการจัดการเนื้อหา (CMS) ตัวอย่างเช่น อาจประกอบด้วยข้อความที่ระบุว่า "สำหรับปัญหาต่างๆ เกี่ยวกับใบสั่งของคุณ โปรดติดต่อ 1-800-Fabrikam" 

- **ข้อกำหนดและเงื่อนไขการเช็คเอาท์** – โมดูลนี้แสดงข้อความซึ่งประกอบด้วยข้อกำหนดและเงื่อนไขและกล่องกาเครื่องหมายสำหรับข้อมูลที่ลูกค้าป้อน กล่องกาเครื่องหมายนี้ไม่จำเป็นต้องระบุและสามารถตั้งค่าคอนฟิกได้ โมดูลจะบันทึกข้อมูลที่ป้อนไว้และสามารถใช้เมื่อมีการตรวจสอบก่อนที่จะทริกเกอร์การสั่งซื้อ แต่ไม่ได้รวมอยู่ในข้อมูลสรุปใบสั่ง คุณสามารถเพิ่มโมดูลนี้ลงในคอนเทนเนอร์เช็คเอาท์ คอนเทนเนอร์ส่วนเช็คเอาท์ หรือช่องข้อกำหนดและเงื่อนไขได้ตามความต้องการของธุรกิจ ถ้ามีการเพิ่มลงในคอนเทนเนอร์เช็คเอาท์หรือช่องคอนเทนเนอร์ส่วนเช็คเอาท์ โมดูลจะปรากฏขึ้นเป็นขั้นตอนในกระบวนการเช็คเอาท์ หากมีการเพิ่มในช่องข้อกำหนดและเงื่อนไข โมดูลจะปรากฏขึ้นใกล้กับปุ่มการสั่งซื้อ

    รูปภาพต่อไปนี้แสดงตัวอย่างของข้อกำหนดและเงื่อนไขบนหน้าเช็คเอาท์

    ![ตัวอย่างของข้อกำหนดและเงื่อนไขบนหน้าเช็คเอาท์](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>การโต้ตอบ Commerce Scale Unit

ข้อมูลส่วนใหญ่ของการชำระเงิน เช่น ที่อยู่ในการจัดส่ง และวิธีการจัดส่งสินค้า จะถูกจัดเก็บไว้ในรถเข็นและดำเนินการโดยเป็นส่วนหนึ่งของใบสั่ง ข้อยกเว้นเดียวคือข้อมูลบัตรเครดิต ข้อมูลนี้จะถูกประมวลผลโดยตรงโดยใช้ตัวเชื่อมต่อการชำระเงิน Adyen การชำระเงินได้รับอนุมัติแล้ว แต่ยังไม่มีการคิดค่าธรรมเนียมจนกว่าจะมีการดำเนินการตามใบสั่ง

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>เพิ่มโมดูลเช็คเอาท์ไปยังหน้า และตั้งค่าคุณสมบัติที่จำเป็น

การเพิ่มโมดูลเช็คเอาท์ไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่
1. ในกล่องโต้ตอบ **เลือกส่วนย่อย** ให้เลือกโมดูล **เช็คเอาท์**
1. ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับ **ส่วนย่อยการเช็คเอาท์** และจากนั้น เลือก **ตกลง**
1. เลือกช่อง **โมดูลการเช็คเอาท์**
1. ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกสัญลักษณ์ดินสอ ป้อนข้อความหัวข้อในฟิลด์ แล้วเลือกสัญลักษณ์เครื่องหมายถูก
1. ในช่อง **เช็คเอาท์ข้อมูล** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เลือกโมดูล** ให้เลือกโมดูล **ที่อยู่ในการจัดส่ง** **ตัวเลือกการจัดส่ง** **คอนเทนเนอร์ส่วนเช็คเอาท์** และ **ข้อมูลการติดต่อ** แล้วเลือก **ตกลง**
1. ในโมดูล **คอนเทนเนอร์ส่วนเช็คเอาท์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เลือกโมดูล** ให้เลือกโมดูล **บัตรของขวัญ** **สมาชิก** และ **การชำระเงิน** จากนั้นเลือก **ตกลง** ด้วยวิธีนี้ คุณควรตรวจสอบให้แน่ใจว่าวิธีการชำระเงินทั้งหมดจะปรากฏรวมกันในส่วน
1. ในช่อง **ข้อกำหนดและเงื่อนไข** ให้เพิ่มโมดูล **ข้อกำหนดและเงื่อนไขการเช็คเอาท์** หากจำเป็น ในแผงคุณสมบัติของโมดูล ให้ตั้งค่าคอนฟิกข้อความของข้อกำหนดและเงื่อนไขตามความเหมาะสม
1. เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างส่วนย่อย บางโมดูลที่ไม่มีบริบทรถเข็น อาจไม่แสดงในการแสดงตัวอย่าง
1. เลือก **แก้ไขให้เสร็จสิ้น** เพื่อเช็คอินส่วนย่อย และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่
1. สร้างเทมเพลตที่ใช้ส่วนการชำระเงินใหม่
1. สร้างส่วนการชำระเงินที่ใช้เทมเพลตใหม่

> [หมายเหตุ] เมื่อใช้การอนุญาตการชำระเงินครั้งเดียวตามที่อธิบายไว้ใน [การชำระเงินขั้นสูงในขั้นตอนการเช็คเอาท์หน้าร้าน](./dev-itpro/enhanced-sca.md) ในส่วน **ข้อมูลเช็คเอาท์** ในหน้าเช็คเอาท์ ยืนยันว่าคอนเทนเนอร์ส่วนเช็คเอาท์วางอยู่ท้ายสุด ซึ่งช่วยให้มั่นใจว่าข้อมูลที่ต้องใช้ทั้งหมดจะถูกรวบรวมโดยหน้าเช็คเอาท์ก่อนการเช็คเอาท์ การเช็คเอาท์เพื่อการชำระเงินขั้นสุดท้ายและการสั่งซื้อเสร็จสมบูรณ์ 

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[โมดูลรถเข็น](add-cart-module.md)

[โมดูลไอคอนรถเข็น](cart-icon-module.md)

[โมดูลการชำระเงิน](payment-module.md)

[โมดูลที่อยู่ที่จัดส่ง](ship-address-module.md)

[โมดูลตัวเลือกการจัดส่ง](delivery-options-module.md)

[โมดูลข้อมูลการเบิกสินค้า](pickup-info-module.md)

[โมดูลรายละเอียดใบสั่ง](order-confirmation-module.md)

[โมดูลบัตรของขวัญ](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
