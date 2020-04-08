---
title: สร้างคำแนะนำที่ระบุด้วยตนเอง
description: หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดซื้อสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้า Microsoft Dynamics 365 Commerce ได้ด้วยตนเอง
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b00c83355850f6249068749096b011f805b37e3c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154329"
---
# <a name="manually-create-curated-recommendations"></a>สร้างคำแนะนำที่ระบุด้วยตนเอง

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดซื้อสามารถสร้างและจัดการรายการคำแนะนำผลิตภัณฑ์สำหรับลูกค้า Microsoft Dynamics 365 Commerce ได้ด้วยตนเอง

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

[เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce](enable-adls-environment.md)

[เปิดใช้งานคำแนะนำผลิตภัณฑ์](enable-product-recommendations.md)

[เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)

[เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล](personalization-gdpr.md)

[เพิ่มคำแนะนำผลิตภัณฑ์ใน POS](product.md)

[เพิ่มคำแนะนำในหน้าจอธุรกรรม](add-recommendations-control-pos-screen.md)

[ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML](modify-product-recommendation-results.md)

[สร้างคำแนะนำที่มีข้อมูลสาธิต](product-recommendations-demo-data.md)

[FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์](faq-recommendations.md)
