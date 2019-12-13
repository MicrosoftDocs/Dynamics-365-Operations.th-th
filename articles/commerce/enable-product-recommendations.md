---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770150"
---
# <a name="enable-product-recommendations"></a>เปิดใช้งานคำแนะนำผลิตภัณฑ์

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)

## <a name="recommendations-pre-check"></a>การตรวจสอบคำแนะนำ
ก่อนที่จะเปิดใช้งาน โปรดทราบว่าคำแนะนำของผลิตภัณฑ์สนับสนุนเฉพาะสำหรับลูกค้า F&O ซึ่งสนับสนุนเวอร์ชัน 10.0.6 และโยกย้ายพื้นที่จัดเก็บของตนไว้เพื่อใช้ BDL 

นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการวัด RetailSale แล้ว หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับขั้นตอนการตั้งค่านี้ให้ไป [ที่นี่](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>เปิดคำแนะนำ

ถ้าต้องการเปิดคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ไปที่ **การขายปลีก** &gt; **คำแนะนำของผลิตภัณฑ์** &gt; **พารามิเตอร์คำแนะนำ**
1. ในรายการพารามิเตอร์ที่ใช้ร่วมกันของการขายปลีก เลือก **รายการแนะนำ**
1. ตั้งค่าตัวเลือก **เปิดใช้คำแนะนำ** เป็น **ใช่**

![เปิดใช้งานคำแนะนำผลิตภัณฑ์](./media/enableproductrecommendations.png)

> [!NOTE]
> ขั้นตอนนี้จะเริ่มต้นกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์ อาจจำเป็นต้องใช้หลายชั่วโมงก่อนที่รายการจะพร้อมใช้งาน และสามารถดูได้จากการขายหน้าร้าน (POS) หรือใน Dynamics 365 for Commerce

## <a name="configure-recommendation-list-parameters"></a>ตั้งค่าพารามิเตอร์รายการคำแนะนำ
โดยค่าเริ่มต้นรายการคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML จะแสดงค่าที่แนะนำ คุณสามารถเปลี่ยนค่าเริ่มต้นที่แนะนำเพื่อให้เหมาะสมกับกระบวนการทางธุรกิจของคุณ เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนพารามิเตอร์เริ่มต้นให้ไปที่ [การจัดการผลลัพธ์การแนะนำของผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)

## <a name="show-recommendations-on-pos-devices"></a>แสดงคำแนะนำบนอุปกรณ์ POS
หลังจากเปิดใช้งานคำแนะนำในฝ่ายสนับสนุน แล้วคุณต้องเพิ่มแผงคำแนะนำให้กับหน้าจอ POS ควบคุมผ่านทางเครื่องมือโครงร่าง หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับขั้นตอนนี้ให้ไป [ที่นี่](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของคำแนะนำผลิตภัณฑ์](product-recommendations.md)

[เพิ่มรายการคำแนะนำผลิตภัณฑ์ลงในหน้า](add-reco-list-to-page.md)

[เพิ่มแผงคำแนะนำลงในอุปกรณ์ POS](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


