---
title: เพิ่มคำแนะนำผลิตภัณฑ์ใน POS
description: บทความนี้จะอธิบายถึงการใช้คำแนะนำผลิตภัณฑ์บนอุปกรณ์การขายหน้าร้าน (POS)
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460068"
---
# <a name="add-product-recommendations-on-pos"></a>เพิ่มคำแนะนำผลิตภัณฑ์ใน POS

[!include [banner](includes/banner.md)]

คามหลัก คำแนะนำผลิตภัณฑ์เป็นแอปพลิเคชันทางธุรกิจเพื่อการเปลี่ยนแปลงที่ครอบคลุมพื้นที่การค้าทั้งหมด เพื่อสร้างประสบการณ์การค้นพบผลิตภัณฑ์ที่หลากหลาย น่าดึงดูด และได้รับการปรับให้เหมาะสม เมื่อต้องการใช้งานลักษณะการทำงานนี้บน[POS ให้ทำตามขั้นตอนเกี่ยวกับวิธีการเพิ่มข้อเสนอแนะให้กับอุปกรณ์ POS ของคุณ](add-recommendations-control-pos-screen.md) 

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน  [คำแนะนำผลิตภัณฑ์ในเอกสารของ POS](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>สถานการณ์จำลอง

คำแนะนำผลิตภัณฑ์ถูกเปิดใช้งานสำหรับสถานการณ์ POS ต่อไปนี้ ซึ่งจะพร้อมใช้งานใน Cloud POS หรือ Modern POS (MPOS)

1. ในหน้า **รายละเอียดผลิตภัณฑ์** :

    - ถ้าการเชื่อมโยงของร้านค้าเยี่ยมชมหน้า **รายละเอียดผลิตภัณฑ์** เมื่อดูที่ธุรกรรมก่อนหน้านี้ผ่านช่องทางต่างๆ บริการคำแนะนำจะแนะนำสินค้าเพิ่มเติมที่มีแนวโน้มที่จะถูกซื้อพร้อมกัน ทั้งนี้ขึ้นอยู่กับส่วนเพิ่มเติมของบริการ ผู้ค้าปลีกสามารถแสดงคำแนะนำ **เลือกซื้อสินค้าที่คล้ายกัน** และ **เลือกซื้อสินค้าที่มีคำอธิบายคล้ายกัน** ของผลิตภัณฑ์ นอกเหนือจากคำแนะนำแบบส่วนบุคคลของผู้ใช้ที่มีประวัติการซื้อก่อนหน้า

    [![คำแนะนำเกี่ยวกับหน้ารายละเอียดผลิตภัณฑ์](./media/proddetails.png)](./media/proddetails.png)

2. ในหน้า **ธุรกรรม** :

    - กลไกคำแนะนำสินค้าจะแนะนำสินค้าตามรายการสินค้าทั้งหมดในตระกร้าที่ซื้อพร้อมกันบ่อย

    > [!NOTE]
    > เพื่อแสดงคำแนะนำในหน้า **ธุรกรรม** ผู้ขายปลีกต้องปรับปรุงโครงร่างหน้าจอใน Dynamics 365 Commerce จะต้องปล่อยการควบคุม **คำแนะนำ** ไปยังหน้า **ธุรกรรม**

    [![คำแนะนำเกี่ยวกับหน้าธุรกรรม](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>กำหนดค่าการค้าเพื่อเปิดใช้งานคำแนะนำ POS 

เมื่อต้องการตั้งค่าคำแนะนำผลิตภัณฑ์ ให้ยืนยันว่าคุณได้เสร็จสิ้นกระบวนการเตรียมใช้งานไว้ให้กับคำแนะนำผลิตภัณฑ์ Commerce แล้ว โดยการปฏิบัติตามขั้นตอนใน [เปิดใช้งานการแนะนำเกี่ยวกับผลิตภัณฑ์](../commerce/enable-product-recommendations.md) ตามค่าเริ่มต้น จะมีการแนะนำอธิบายปรากฏขึ้นทั้งหน้า **รายละเอียดผลิตภัณฑ์** และหน้า **รายละเอียดลูกค้า** หลังจากที่คุณเสร็จสิ้นขั้นตอนการเตรียมใช้งานและข้อมูลเสร็จเรียบร้อยแล้ว 

## <a name="add-recommendations-to-the-transaction-screen"></a>เพิ่มคำแนะนำในหน้าจอธุรกรรม

1. ในการเพิ่มคำแนะนำลงในหน้าจอธุรกรรม ให้ปฏิบัติตามขั้นตอนต่างๆ ใน [เพิ่มคำแนะนำลงในหน้าจอธุรกรรม](add-recommendations-control-pos-screen.md)
1. เพื่อสะท้อนการเปลี่ยนแปลงที่ถูกสร้างขึ้นในตัวออกแบบโครงร่างหน้าจอ POS ให้รันงานการตั้งค่าคอนฟิกช่องทาง **1070** ใน Commerce headquarters

> [!NOTE] 
> หากคุณต้องการเปิดใช้งานคำแนะนำของ POS โดยใช้ไฟล์ค่าที่คั่นด้วยเครื่องหมายจุลภาคของ RecoMock (CSV) คุณต้องปรับใช้ไฟล์ CSV กับไลบรารีสินทรัพย์ Microsoft Dynamics Lifecycle Services (LCS) ก่อนที่คุณจะตั้งค่าคอนฟิกตัวจัดการโครงร่าง หากคุณใช้ไฟล์ RecoMock CSV คุณจะไม่ต้องเปิดใช้งานคำแนะนำ ไฟล์ CSV พร้อมใช้งานเฉพาะเพื่อวัตถุประสงค์ในการสาธิตเท่านั้น ขอแนะนำลูกค้าหรือสถาปนิกโซลูชันที่ต้องการคัดลอกลักษณะของรายการการแนะนำเพื่อวัตถุประสงค์ในการสาธิตโดยไม่ต้องซื้อหน่วยการเก็บสต็อกเพิ่มเติม (SKU)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของคำแนะนำผลิตภัณฑ์](product-recommendations.md)

[เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce](enable-adls-environment.md)

[เปิดใช้งานคำแนะนำผลิตภัณฑ์](enable-product-recommendations.md)

[เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)

[เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล](personalization-gdpr.md)

[เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"](shop-similar-looks.md)

[เพิ่มคำแนะนำในหน้าจอธุรกรรม](add-recommendations-control-pos-screen.md)

[ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML](modify-product-recommendation-results.md)

[สร้างคำแนะนำที่ระบุด้วยตนเอง](create-editorial-recommendation-lists.md)

[สร้างคำแนะนำที่มีข้อมูลสาธิต](product-recommendations-demo-data.md)

[FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
