---
title: บันทึกการรับสินค้าในใบสั่งซื้อ
description: บทความนี้แสดงวิธีการบันทึกการรับสินค้าโดยตรงในใบสั่งซื้อ
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22baf6d0f6db04b3c6ce3c09ee8cb286e9a1e590
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882473"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>บันทึกการรับสินค้าในใบสั่งซื้อ

[!include [banner](../../includes/banner.md)]

บทความนี้แสดงวิธีการบันทึกการรับสินค้าโดยตรงในใบสั่งซื้อ นอกจากนี้ ยังสามารถลงทะเบียนใบรับสินค้าในคลังสินค้า และจากนั้น บันทึกบนใบสั่งซื้อในภายหลัง โดยทั่วไปจะมีการทำงานนี้โดยเจ้าหน้าที่จัดซื้อหรือผู้ประสานงานเจ้าหนี้บัญชี ตัวอย่างที่แสดงในคำแนะนำนี้สามารถใช้ในบริษัทข้อมูลสาธิต USMF ตัวอย่างประกอบด้วยขั้นตอนในการสร้างใบสั่งซื้อแบบง่ายเพื่อให้คุณสามารถใช้กระบวนงานเป็นคู่มืองาน ถ้าคุณเคยใช้กระบวนงานในข้อมูลของคุณเอง คุณจะเริ่มต้นที่งานย่อย **บันทึกการรับสินค้า**


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>เตรียมใบสั่งซื้อใหม่สำหรับการรับสินค้า
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดซื้อและการจัดหา > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด**
2. เลือก **ใหม่**
3. ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ป้อน `US-101`
4. เลือก **ตกลง**
5. ในฟิลด์ **หมายเลขสินค้า** ให้ป้อน `M0001`
6. ในฟิลด์ **ปริมาณ** ให้ป้อน `5`
7. บนบานหน้าต่างการดำเนินการ เลือก **ซื้อ**
8. เลือก **ยืนยัน**

## <a name="record-receipt-of-goods"></a>บันทึกการรับสินค้า
1. ในบานหน้าต่างการดำเนินการ เลือก **รับ**
2. เลือก **ใบรับผลิตภัณฑ์** ฟิลด์ **ปริมาณ** ช่วยให้คุณสามารถเลือกตัวเลือกต่างๆ สำหรับปริมาณที่คุณต้องการได้รับ ตัวอย่างเช่น ถ้ามีการลงทะเบียนปริมาณไว้ก่อนหน้านี้ในคลังสินค้า คุณสามารถเลือก **ปริมาณที่ลงทะเบียน** สำหรับตัวอย่างนี้ จะใช้ค่า **ปริมาณที่สั่ง**
3. ขยายส่วน **ภาพรวม**
4. ในฟิลด์ **ใบรับสินค้า** ให้พิมพ์ค่าใดค่าหนึ่ง ฟิลด์นี้จะใช้ในการป้อนข้อมูลอ้างอิงที่จะใช้เป็นใบสำคัญสำหรับมุดรายวันใบรับสินค้าจากใบสั่งซื้อ  
5. ขยายส่วน **รายการ**
6. กำหนด **ปริมาณเป็น** '4' ที่นี่คุณจะสามารถระบุปริมาณที่จะได้รับสำหรับแต่ละบรรทัดในใบสั่งด้วยตนเอง  
7. เลือก **ตกลง** ขณะนี้สินค้ามีการบันทึกเป็นได้รับตามใบสั่งส่งคืนสินค้าที่ซื้อ และมีการสร้างมุดรายวันใบรับสินค้าเป็นเอกสารเพื่อแสดงขั้นตอนนี้  คุณสามารถใช้การดำเนินการรับสินค้าเพื่อตรวจสอบสมุดรายวันที่สร้างด้วยใบสั่งซื้อ และดูรายการที่ได้รับและเวลาที่ได้รับ  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]