---
title: เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce
description: หัวข้อนี้อธิบายวิธีเปิดใช้งานและทดสอบ Azure Data Lake Storage สำหรับสภาพแวดล้อม Dynamics 365 Commerce ซึ่งเป็นข้อกำหนดเบื้องต้นสำหรับการเปิดใช้งานคำแนะนำผลิตภัณฑ์
author: bebeale
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8ec56a260501c0d33145c23cb9656446bc871f7c448bbbf33330ad591c506e49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775373"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีเปิดใช้งานและทดสอบ Azure Data Lake Storage สำหรับสภาพแวดล้อม Dynamics 365 Commerce ซึ่งเป็นข้อกำหนดเบื้องต้นสำหรับการเปิดใช้งานคำแนะนำผลิตภัณฑ์

ในโซลูชัน Dynamics 365 Commerce ข้อมูลผลิตภัณฑ์และธุรกรรมทั้งหมดจะถูกติดตามในที่เก็บเอนทิตีของสภาพแวดล้อม เพื่อทำให้ข้อมูลนี้สามารถเข้าถึงได้จากบริการอื่นๆ ของ Dynamics 365 เช่น การวิเคราะห์ข้อมูล ข่าวกรองทางธุรกิจ และคำแนะนำแบบส่วนตัว จึงจำเป็นต้องเชื่อมต่อสภาพแวดล้อมกับโซลูชัน Azure Data Lake Storage Gen 2 ที่เป็นของลูกค้า

เนื่องจาก Azure Data Lake Storage ถูกตั้งค่าคอนฟิกในสภาพแวดล้อม ข้อมูลที่จำเป็นทั้งหมดจะถูกสะท้อนจากที่เก็บเอนทิตี ในขณะที่ยังคงได้รับการป้องกันและอยู่ภายใต้การควบคุมของลูกค้า

นอกจากนี้ หากมีการเปิดใช้งานคำแนะนำผลิตภัณฑ์หรือคำแนะนำแบบส่วนตัวในสภาพแวดล้อมด้วยแล้ว สแต็คคำแนะนำผลิตภัณฑ์จะได้รับสิทธิ์การเข้าถึงโฟลเดอร์เฉพาะใน Azure Data Lake Storage เพื่อดึงข้อมูลของลูกค้าและคำนวณคำแนะนำตามข้อมูลนั้น

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ลูกค้าจำเป็นต้องตั้งค่าคอนฟิก Azure Data Lake Storage ในการสมัครใช้งาน Azure ที่พวกเขาเป็นเจ้าของ หัวข้อนี้ไม่ครอบคลุมการซื้อของการสมัครใช้งาน Azure หรือการตั้งค่าของบัญชีที่เก็บข้อมูลที่เปิดใช้งาน Azure Data Lake Storage

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Azure Data Lake Storage ดู [เอกสารประกอบอย่างเป็นทางการของ Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake)
  
## <a name="configuration-steps"></a>ขั้นตอนการกำหนดค่า 

ส่วนนี้ครอบคลุมขั้นตอนการตั้งค่าคอนฟิกที่จำเป็นสำหรับการเปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม เนื่องจากเกี่ยวข้องกับคำแนะนำผลิตภัณฑ์
สำหรับภาพรวมเชิงลึกเพิ่มเติมเกี่ยวกับขั้นตอนต่างๆ ที่จำเป็นในการเปิดใช้งาน Azure Data Lake Storage ให้ดูที่ [ทำให้ที่จัดเก็บเอนทิตีพร้อมใช้งานเป็น Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม

1. ล็อกอินเข้าสู่พอร์ทัลสนับสนุนของสภาพแวดล้อม
1. ค้นหา **พารามิเตอร์ระบบ** และนำทางไปที่แท็บ **การเชื่อมโยงข้อมูล** 
1. ตั้งค่า **เปิดใช้งานการรวม Data Lake** เป็น **ใช่**
1. ตั้งค่า **เปิดใช้งานการปรับปรุงทริกเกิล Data Lake** เป็น **ใช่**
1. จากนั้นป้อนข้อมูลที่จำเป็นต่อไปนี้:
    1. **รหัสแอปพลิเคชัน** // **ข้อมูลลับของแอปพลิเคชัน** // **ชื่อ DNS** - จำเป็นต้องเชื่อมต่อกับ KeyVault ที่ซึ่งข้อมูลลับ Azure Data Lake Storage ถูกจัดเก็บไว้
    1. **ชื่อลับ** - ชื่อลับที่เก็บไว้ใน KeyVault และใช้เพื่อรับรองความถูกต้องกับ Azure Data Lake Storage
1. บันทึกการเปลี่ยนแปลงของคุณในหน้าที่อยู่มุมบนซ้าย

ภาพต่อไปนี้แสดงการตั้งค่าคอนฟิก Azure Data Lake Storage ตัวอย่าง

![ตัวอย่างของการตั้งค่าคอนฟิก Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>ทดสอบการเชื่อมต่อ Azure Data Lake Storage

1. ทดสอบการเชื่อมต่อกับ KeyVault โดยใช้ลิงก์ **ทดสอบ Azure Key Vault**
1. ทดสอบการเชื่อมต่อกับ Azure Data Lake Storage โดยใช้ลิงก์ **ทดสอบที่เก็บข้อมูล Azure**

> [!NOTE]
> หากการทดสอบไม่ประสบผลสำเร็จ ตรวจสอบอีกครั้งว่าข้อมูล KeyVault ทั้งหมดที่เพิ่มข้างต้นถูกต้อง จากนั้นลองอีกครั้ง

เมื่อการทดสอบการเชื่อมต่อสำเร็จ คุณต้องเปิดใช้งานการรีเฟรชอัตโนมัติสำหรับที่เก็บเอนทิตี

เพื่อเปิดใช้งานที่เก็บเอนทิตีสำหรับการรีเฟรชอัตโนมัติ ให้ทำตามขั้นตอนเหล่านี้

1. ค้นหา **ที่เก็บเอนทิตี**
1. ในรายการด้านซ้าย นำทางไปยังรายการ **RetailSales** และเลือก **แก้ไข**
1. ตรวจสอบให้แน่ใจว่า **ได้เปิดใช้งานการรีเฟรชอัตโนมัติ** ซึ่งถูกตั้งค่าเป็น **ใช่** เลือก **รีเฟรช** แล้วจึงเลือก **บันทึก**

เพื่อเปิดใช้งานที่เก็บเอนทิตีสำหรับการรีเฟรชอัตโนมัติ ให้ทำตามขั้นตอนเหล่านี้ รูปภาพต่อไปนี้แสดงตัวอย่างของที่เก็บเอนทิตีพร้อมกับการเปิดใช้งานการรีเฟรชอัตโนมัติ

![ตัวอย่างของที่เก็บเอนทิตีที่เปิดใช้งานการรีเฟรชอัตโนมัติ](./media/exampleADLSConfig2.png)

Azure Data Lake Storage ขณะนี้ถูกตั้งค่าคอนฟิกสำหรับสภาพแวดล้อม 

หากยังไม่เสร็จสิ้น ให้ทำตามขั้นตอนสำหรับ [การเปิดใช้งานคำแนะนำผลิตภัณฑ์และการตั้งค่าส่วนบุคคล](enable-product-recommendations.md) สำหรับสภาพแวดล้อม

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ทำให้ที่จัดเก็บเอนทิตี้พร้อมใช้งานเป็น Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[ภาพรวมของคำแนะนำผลิตภัณฑ์](product-recommendations.md)

[เปิดใช้งานคำแนะนำผลิตภัณฑ์](enable-product-recommendations.md)

[เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)

[เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล](personalization-gdpr.md)

[เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"](shop-similar-looks.md)

[เพิ่มคำแนะนำผลิตภัณฑ์ใน POS](product.md)

[เพิ่มคำแนะนำในหน้าจอธุรกรรม](add-recommendations-control-pos-screen.md)

[ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML](modify-product-recommendation-results.md)

[สร้างคำแนะนำที่ระบุด้วยตนเอง](create-editorial-recommendation-lists.md)

[สร้างคำแนะนำที่มีข้อมูลสาธิต](product-recommendations-demo-data.md)

[FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
