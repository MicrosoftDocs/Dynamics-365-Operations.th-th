---
title: สร้างคำแนะนำที่ระบุด้วยตนเอง
description: บทความนี้จะอธิบายวิธีการที่ผู้จัดจำหน่ายสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้าด้วยตนเองสำหรับลูกค้า Microsoft Dynamics 365 Commerce
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e1a1b402165c5cb35696cf1cf6630770ad07508a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892689"
---
# <a name="manually-create-curated-recommendations"></a>สร้างคำแนะนำที่ระบุด้วยตนเอง

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายวิธีการที่ผู้จัดจำหน่ายสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้าด้วยตนเองสำหรับลูกค้า Microsoft Dynamics 365 Commerce

รายการที่อนุรักษ์คือคอลเลกชันของเนื้อหาแต่ละรายการที่สร้างและอนุรักษ์โดยบุคคล  

## <a name="create-a-new-list"></a>สร้างรายการใหม่

เมื่อต้องการสร้างรายการแนะนำผลิตภัณฑ์ที่รวบรวมไว้ ให้ทำตามขั้นตอนเหล่านี้

1. ไปยัง **Retail และ Commerce &gt; คำแนะนำผลิตภัณฑ์ &gt; รายการคำแนะนำ**
1. เลือก **ใหม่**
1. ในฟิลด์ **รหัสรายการ** ให้ป้อนค่า
1. ในฟิลด์ **ชื่อรายการ** ให้ป้อนค่า
    - **ชื่อรายการ** คือชื่อเรื่องของรายการที่จะปรากฏในส่วนรายการที่รวบรวมของโมดูล **การรวบรวมผลิตภัณฑ์**
1. ในการเพิ่มผลิตภัณฑ์ไปยังรายการ ให้เลือก **เพิ่มผลิตภัณฑ์**
1. เมื่อต้องการเปลี่ยนลำดับของผลิตภัณฑ์ในรายการ ให้ป้อนค่าในคอลัมน์ **ใบสั่งที่แสดง**
    - ถ้าผลิตภัณฑ์สองตัวมีมูลค่าของใบสั่งแสดงผลเดียวกัน ใบสั่งสุดท้ายของผลสองอย่างอาจแตกต่างจากฝ่ายสนับสนุน
1. เลือก **บันทึก** เพื่อบันทึกรายการ

## <a name="example-list"></a>รายการตัวอย่าง

![รายการการรวบรวมตัวอย่างในฝ่ายสนับสนุน](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของคำแนะนำผลิตภัณฑ์](product-recommendations.md)

[เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce](enable-adls-environment.md)

[เปิดใช้งานคำแนะนำผลิตภัณฑ์](enable-product-recommendations.md)

[เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)

[เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล](personalization-gdpr.md)

[เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"](shop-similar-looks.md)

[เพิ่มคำแนะนำผลิตภัณฑ์ใน POS](product.md)

[เพิ่มคำแนะนำในหน้าจอธุรกรรม](add-recommendations-control-pos-screen.md)

[ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML](modify-product-recommendation-results.md)

[สร้างคำแนะนำที่มีข้อมูลสาธิต](product-recommendations-demo-data.md)

[FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]