---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154424"
---
# <a name="enable-product-recommendations"></a>เปิดใช้งานคำแนะนำผลิตภัณฑ์

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)

## <a name="recommendations-pre-check"></a>การตรวจสอบคำแนะนำ

ก่อนเปิดใช้งาน โปรดทราบว่าคำแนะนำผลิตภัณฑ์ได้รับการสนับสนุนเฉพาะสำหรับลูกค้าเชิงพาณิชย์ที่โอนย้ายที่เก็บข้อมูลของตนไปใช้ Azure Data Lake Storage (ADLS)  

สำหรับขั้นตอนการเปิดใช้งาน ADLS ดู [ธีเปิดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365](enable-ADLS-environment.md)

นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการวัด RetailSale แล้ว หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับกระบวนการตั้งค่านี้ให้ไปที่ [ที่นี่](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>เปิดคำแนะนำ

ถ้าต้องการเปิดคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ไปยัง **การขายปลีกและการค้า &gt; คำแนะนำผลิตภัณฑ์ &gt; พารามิเตอร์คำแนะนำ**
1. ในรายการของพารามิเตอร์ที่ใช้ร่วมกัน ให้เลือก **รายการคำแนะนำ**
1. ตั้งค่าตัวเลือก **เปิดใช้คำแนะนำ** เป็น **ใช่**

![เปิดใช้งานคำแนะนำผลิตภัณฑ์](./media/enableproductrecommendations.png)

> [!NOTE]
> ขั้นตอนนี้จะเริ่มต้นกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์ อาจจำเป็นต้องใช้หลายชั่วโมงก่อนที่รายการจะพร้อมใช้งาน และสามารถดูได้จากการขายหน้าร้าน (POS) หรือใน Dynamics 365 Commerce

## <a name="configure-recommendation-list-parameters"></a>ตั้งค่าพารามิเตอร์รายการคำแนะนำ

โดยค่าเริ่มต้นรายการคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML จะแสดงค่าที่แนะนำ คุณสามารถเปลี่ยนค่าเริ่มต้นที่แนะนำเพื่อให้เหมาะสมกับกระบวนการทางธุรกิจของคุณ เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนพารามิเตอร์เริ่มต้นให้ไปที่ [การจัดการผลลัพธ์การแนะนำของผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)

## <a name="show-recommendations-on-pos-devices"></a>แสดงคำแนะนำบนอุปกรณ์ POS

หลังจากเปิดใช้งานคำแนะนำในแผนกสนับสนุน (Back Office) เชิงพาณิชย์จะต้องเพิ่มแผงคำแนะนำลงในหน้าจอการควบคุม POS โดยใช้เครื่องมือเค้าโครง หากต้องการเรียนรู้เกี่ยวกับกระบวนการนี้ ให้ดู [เพิ่มการควบคุมคำแนะนำให้กับหน้าจอธุรกรรมบนอุปกรณ์ POS](add-recommendations-control-pos-screen.md) 

## <a name="enable-personalized-recommendations"></a>เปิดใช้งานคำแนะนำแบบส่วนตัว

เรียนรู้เพิ่มเติมเกี่ยวกับวิธีรับคำแนะนำแบบส่วนตัว โปรดดู [เปิดใช้งานคำแนะนำแบบส่วนตัว](personalized-recommendations.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของคำแนะนำผลิตภัณฑ์](product-recommendations.md)

[เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce](enable-adls-environment.md)

[เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)

[เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล](personalization-gdpr.md)

[เพิ่มคำแนะนำผลิตภัณฑ์ใน POS](product.md)

[เพิ่มคำแนะนำในหน้าจอธุรกรรม](add-recommendations-control-pos-screen.md)

[ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML](modify-product-recommendation-results.md)

[สร้างคำแนะนำที่ระบุด้วยตนเอง](create-editorial-recommendation-lists.md)

[สร้างคำแนะนำที่มีข้อมูลสาธิต](product-recommendations-demo-data.md)

[FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์](faq-recommendations.md)

