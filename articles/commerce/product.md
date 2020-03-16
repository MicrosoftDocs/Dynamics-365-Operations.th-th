---
title: คำแนะนำผลิตภัณฑ์บน POS
description: หัวข้อนี้จะอธิบายถึงการใช้คำแนะนำผลิตภัณฑ์บนอุปกรณ์การขายหน้าร้าน (POS)
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bfb13904b774558907b29e74158b1e0a193e17cd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057452"
---
# <a name="product-recommendations-on-pos"></a>คำแนะนำผลิตภัณฑ์ใน POS

[!include [banner](includes/banner.md)]

คามหลัก คำแนะนำผลิตภัณฑ์เป็นแอปพลิเคชันทางธุรกิจเพื่อการเปลี่ยนแปลงที่ครอบคลุมพื้นที่การค้าทั้งหมด เพื่อสร้างประสบการณ์การค้นพบผลิตภัณฑ์ที่หลากหลาย น่าดึงดูด และได้รับการปรับให้เหมาะสม เมื่อต้องการใช้งานลักษณะการทำงานนี้บน[POS ให้ทำตามขั้นตอนเกี่ยวกับวิธีการเพิ่มข้อเสนอแนะให้กับอุปกรณ์ POS ของคุณ](add-recommendations-control-pos-screen.md) 

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน  [คำแนะนำผลิตภัณฑ์ในเอกสารของ POS](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>สถานการณ์จำลอง

คำแนะนำผลิตภัณฑ์ถูกเปิดใช้งานสำหรับสถานการณ์ POS ต่อไปนี้ ซึ่งจะพร้อมใช้งานใน Cloud POS หรือ Modern POS (MPOS)

1. ในหน้า **รายละเอียดผลิตภัณฑ์** :

    - ถ้าการเชื่อมโยงของร้านค้าเยี่ยมชมหน้า **รายละเอียดผลิตภัณฑ์** เมื่อดูที่ธุรกรรมก่อนหน้านี้ผ่านช่องทางต่างๆ บริการคำแนะนำจะแนะนำสินค้าเพิ่มเติมที่มีแนวโน้มที่จะถูกซื้อพร้อมกัน

    [![คำแนะนำเกี่ยวกับหน้ารายละเอียดผลิตภัณฑ์](./media/proddetails.png)](./media/proddetails.png)

2. ในหน้า **ธุรกรรม** :

    - กลไกคำแนะนำสินค้าจะแนะนำสินค้าตามรายการสินค้าทั้งหมดในตระกร้าที่ซื้อพร้อมกันบ่อย

    > [!NOTE]
    > เพื่อแสดงคำแนะนำในหน้า **ธุรกรรม** ผู้ขายปลีกต้องปรับปรุงโครงร่างหน้าจอใน Dynamics 365 Commerce จะต้องปล่อยการควบคุม **คำแนะนำ** ไปยังหน้า **ธุรกรรม**

    [![คำแนะนำเกี่ยวกับหน้าธุรกรรม](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>กำหนดค่าการค้าเพื่อเปิดใช้งานคำแนะนำ POS

ถ้าต้องการตั้งค่าคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ตรวจสอบให้แน่ใจว่ายริการของคุณได้อัพเดทเป็น **10.0.6 บิวด์**
2. ปฏิบัติตามคำแนะนำเกี่ยวกับวิธีการ [เปิดใช้งานคำแนะนำผลิตภัณฑ์](../commerce/enable-product-recommendations.md) สำหรับธุรกิจของคุณ
3. ไม่จำเป็น: เมื่อต้องการแสดงคำแนะนำบนหน้าจอธุรกรรม ไปที่ **โครงร่างหน้าจอ** เลือกโครงร่างหน้าจอของคุณ เปิดใช้ **ตัวออกแบบโครงร่างหน้าจอ** แล้วปล่อยการควบคุม **คำแนะนำ** เมื่อจำเป็น
4. ไปที่ **พารามิเตอร์การค้า** เลือก **การเรียนรู้เกี่ยวกับเครื่อง** เลือก **ใช่** ภายใต้ **คำแนะนำการเปืดใช้งาน POS** 
5. เมื่อต้องการดูคำแนะนำบน POS เรียกใช้งานการตั้งค่าคอนฟิกส่วนกลาง **1110** เมื่อต้องการเปลี่ยนแปลงในตัวออกแบบโครงร่างหน้าจอ POS เรียกใช้งานการตั้งค่าคอนฟิกช่องทาง **1070**

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>แก้ไขปัญหาที่ซึ่งคุณมีคำแนะนำผลิตภัณฑ์ที่เปิดใช้งานอยู่แล้ว

- นำทางไปยัง **พารามิเตอร์การค้า** \> **รายการแนะนำ** \> **ปิดใช้งานคำแนะนำผลิตภัณฑ์** และเรียกใช้ **งานการตั้งค่าส่วนกลาง \[9999\]** 
- ถ้าคุณได้เพิ่ม **ตัวควบคุมคำแนะนำ** ไปยังหน้าจอธุรกรรมของคุณโดยใช้ **โปรแกรมออกแบบโครงร่างหน้าจอ** โปรดลบรายการนั้นเช่นกัน
- หากคุณมีคำถามเพิ่มเติม ให้ดู [คำถามที่พบบ่อยเกี่ยวกับคำแนะนำผลิตภัณฑ์](../commerce/faq-recommendations.md) สำหรับข้อมูลเพิ่มเติม

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[เพิ่มตัวควบคุมคำแนะนำในหน้าจอธุรกรรมบนอุปกรณ์ POS](add-recommendations-control-pos-screen.md)

[ภาพรวมของคำแนะนำผลิตภัณฑ์](../commerce/product-recommendations.md)

[เปิดใช้งานคำแนะนำผลิตภัณฑ์](../commerce/enable-product-recommendations.md) 
