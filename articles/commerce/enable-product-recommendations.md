---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce
author: bebeale
ms.date: 08/18/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 59d6b298896c92cbc0f6bbae17096ee1f027b922
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799166"
---
# <a name="enable-product-recommendations"></a>เปิดใช้งานคำแนะนำผลิตภัณฑ์

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)

## <a name="recommendations-pre-check"></a>การตรวจสอบคำแนะนำ

ก่อนการเปิดใช้งาน โปรดทราบว่าคำแนะนำผลิตภัณฑ์ได้รับการสนับสนุนเฉพาะสำหรับลูกค้า Commerce ที่โอนย้ายที่เก็บข้อมูลของตนไปโดยใช้ Azure Data Lake Storage 

ต้องเปิดใช้งานการตั้งค่าคอนฟิกต่อไปนี้ในฝ่ายสนับสนุนก่อนเปิดใช้งานคำแนะนำ:

1. ตรวจสอบให้แน่ใจว่ามีการซื้อ Azure Data Lake Storage และตรวจสอบความถูกต้องในสภาพแวดล้อมเรียบร้อยแล้ว สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบให้แน่ใจว่ามีการซื้อ Azure Data Lake Storage และตรวจสอบความถูกต้องในสภาพแวดล้อมเรียบร้อยแล้ว](enable-ADLS-environment.md)
2. ตรวจสอบให้แน่ใจว่ามีการรีเฟรชที่จัดเก็บเอนทิตี้โดยอัตโนมัติ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบให้แน่ใจว่ามีการรีเฟรชที่จัดเก็บเอนทิตี้โดยอัตโนมัติ](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)
3. ยืนยันว่าการตั้งค่าคอนฟิกข้อมูลเฉพาะตัว Azure AD มีรายการสำหรับคำแนะนำ ข้อมูลเพิ่มเติมเกี่ยวกับวิธีการดำเนินการนี้อยู่ด้านล่าง

นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการวัด RetailSale แล้ว เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับขั้นตอนการตั้งค่านี้ ให้ดูที่ [การทำงานกับการวัด](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)

## <a name="azure-ad-identity-configuration"></a>การตั้งค่าคอนฟิกข้อมูลประจำตัวของ Azure AD

ขั้นตอนนี้จำเป็นสำหรับลูกค้าทั้งหมดที่ใช้โครงสร้างแบบอินฟราเรดเป็นการตั้งค่าคอนฟิกการบริการ (IaaS) สำหรับลูกค้าที่ทำงานบน Service Fabric (SF) ขั้นตอนนี้ควรเป็นแบบอัตโนมัติ และเราขอแนะนำให้ตรวจสอบว่ามีการตั้งค่าคอนฟิกการตั้งค่าตามที่คาดไว้

### <a name="setup"></a>การตั้งค่า

1. จากฝ่ายสนับสนุน ให้ค้นหาหน้า **แอปพลิเคชัน Azure Active Directory**
2. ตรวจสอบว่ามีรายการสำหรับ "RecommendationSystemApplication-1" หรือไม่

ถ้าไม่มีรายการอยู่ ให้เพิ่มรายการใหม่ที่มีข้อมูลต่อไปนี้:

- **รหัสไคลเอนต์ ASP** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **ชื่อ** - RecommendationSystemApplication-1
- **รหัสผู้ใช้** - RetailServiceAccount

บันทึกและปิดหน้า 

## <a name="turn-on-recommendations"></a>เปิดคำแนะนำ

ถ้าต้องการเปิดคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ในศูนย์ควบคุม Commerce ให้ค้นหา **การจัดการคุณลักษณะ**
1. เลือก **ทั้งหมด** เพื่อดูรายการของคุณลักษณะที่มีอยู่ 
1. ในกล่องค้นหา ให้ป้อน **คำแนะนำ**
1. เลือกคุณลักษณะ **คำแนะนำผลิตภัณฑ์**
1. ในบานหน้าต่างคุณสมบัติ **คำแนะนำผลิตภัณฑ์** ให้เลือก **เปิดใช้งานเดี๋ยวนี้**

![กำลังเปิดคำแนะนำ](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> ขั้นตอนนี้จะเริ่มต้นกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์ อาจจำเป็นต้องใช้หลายชั่วโมงก่อนที่รายการจะพร้อมใช้งาน และสามารถดูได้จากการขายหน้าร้าน (POS) หรือใน Dynamics 365 Commerce

## <a name="configure-recommendation-list-parameters"></a>ตั้งค่าพารามิเตอร์รายการคำแนะนำ

โดยค่าเริ่มต้นรายการคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML จะแสดงค่าที่แนะนำ คุณสามารถเปลี่ยนค่าเริ่มต้นที่แนะนำเพื่อให้เหมาะสมกับกระบวนการทางธุรกิจของคุณ เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนพารามิเตอร์เริ่มต้นให้ไปที่ [การจัดการผลลัพธ์การแนะนำของผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)

## <a name="show-recommendations-on-pos-devices"></a>แสดงคำแนะนำบนอุปกรณ์ POS

หลังจากเปิดใช้งานคำแนะนำในแผนกสนับสนุน (Back Office) เชิงพาณิชย์จะต้องเพิ่มแผงคำแนะนำลงในหน้าจอการควบคุม POS โดยใช้เครื่องมือเค้าโครง หากต้องการเรียนรู้เกี่ยวกับกระบวนการนี้ ให้ดู [เพิ่มการควบคุมคำแนะนำให้กับหน้าจอธุรกรรมบนอุปกรณ์ POS](add-recommendations-control-pos-screen.md) 

## <a name="enable-personalized-recommendations"></a>เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล

ใน Dynamics 365 Commerce ผู้ค้าปลีกสามารถทำให้คำแนะนำผลิตภัณฑ์แบบส่วนตัวพร้อมใช้งาน (หรืออีกชื่อหนึ่งว่า การตั้งค่าส่วนบุคคล) ด้วยวิธีนี้ คำแนะนำแบบส่วนตัวสามารถรวมเข้ากับประสบการณ์ของลูกค้าออนไลน์และในระบบขายหน้าร้าน เมื่อเปิดใช้งานฟังก์ชั่นการตั้งค่าส่วนบุคคล ระบบจะสามารถเชื่อมโยงข้อมูลการซื้อและผลิตภัณฑ์ของผู้ใช้เพื่อสร้างคำแนะนำผลิตภัณฑ์เฉพาะบุคคล

หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคำแนะนำแบบส่วนตัว โปรดดูที่ [เปิดใช้งานคำแนะนำแบบส่วนตัว](personalized-recommendations.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของคำแนะนำผลิตภัณฑ์](product-recommendations.md)

[เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce](enable-adls-environment.md)

[เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)

[เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"](shop-similar-looks.md)

[เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล](personalization-gdpr.md)

[เพิ่มคำแนะนำผลิตภัณฑ์ใน POS](product.md)

[เพิ่มคำแนะนำในหน้าจอธุรกรรม](add-recommendations-control-pos-screen.md)

[ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML](modify-product-recommendation-results.md)

[สร้างคำแนะนำที่ระบุด้วยตนเอง](create-editorial-recommendation-lists.md)

[สร้างคำแนะนำที่มีข้อมูลสาธิต](product-recommendations-demo-data.md)

[FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]