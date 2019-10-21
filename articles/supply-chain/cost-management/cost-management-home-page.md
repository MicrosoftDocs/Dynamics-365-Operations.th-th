---
title: โฮมเพจการจัดการต้นทุน
description: การจัดการต้นทุนช่วยให้คุณสามารถจัดการวิธีการประเมินค่าและการบัญชีของวัตถุดิบ สินค้ากึ่งสำเร็จรูป สินค้าสำเร็จรูป และสินทรัพย์ที่อยู่ระหว่างดำเนินการ
author: AndersGirke
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd51fa667fd48b7bab64c3566b616631c6f9bcd1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249643"
---
# <a name="cost-management-home-page"></a>โฮมเพจการจัดการต้นทุน

[!include [banner](../includes/banner.md)]

[การจัดการต้นทุน (วิดีโอ)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) ช่วยให้คุณสามารถทำงานได้กับวิธีการประเมินค่าและการบัญชีของวัตถุดิบ สินค้ากึ่งสำเร็จรูป สินค้าสำเร็จรูป และสินทรัพย์ที่อยู่ระหว่างดำเนินการ เป็นกระบวนการในการกำหนด การจัดการ และการรายงาน [การบัญชีสินค้าคงคลัง](cost-object.md) และ [การบัญชีการผลิต](bom-calculations.md)

คุณสามารถกำหนดนโยบายต้นทุนได้ในพื้นที่ต่อไปนี้: 
-  [ต้นทุนที่กำหนดไว้ล่วงหน้า](costing-versions.md)
-  [การบัญชีสินค้าคงคลัง](cost-object.md)
-  [การบัญชีการผลิต](bom-calculations.md)
-  [การบัญชีต้นทุนทางอ้อม](costing-sheets.md)
-  [การรวมบัญชีแยกประเภท](production-order-cost-analysis.md)

ตัวอย่างเช่น คุณสามารถกำหนดวิธีการประเมินค่าสินค้าคงคลังได้ เช่น [FIFO](fifo-physical-value-marking.md) [ค่าเฉลี่ยถ่วงน้ำหนัก](weighted-average-physical-value-marking.md) [ต้นทุนมาตรฐาน](prerequisites-standard-costs.md) หรือ [ค่าเฉลี่ยเคลื่อนที่](moving-average.md) ที่คุณต้องการนำไปใช้กับผลิตภัณฑ์ใน [กลุ่มแบบจำลองสินค้า](../inventory/reserve-inventory-quantities.md) ในการบัญชีสินค้าคงคลัง

คุณสามารถเข้าถึงการบัญชีสินค้าคงคลังและการบัญชีการผลิตจากพื้นที่ทำงาน **การจัดการต้นทุน** และ **การวิเคราะห์ต้นทุน** ได้ พื้นที่ทำงานเหล่านี้ให้ภาพรวมที่มีรายละเอียดครบถ้วนของสถานะปัจจุบัน ตัวบ่งชี้ประสิทธิภาพหลัก (KPIs) และการตรวจพบความเบี่ยงเบน 

การบัญชีการผลิตช่วยให้คุณสามารถจัดการกับ [การคิดต้นทุนตามใบสั่งงาน](production-order-cost-analysis.md) ในใบสั่งผลิตและใบสั่งชุดงานได้ รวมทั้ง [การคิดต้นทุนแบบย้อนกลับ](backflush-costing.md) ใน lean manufacturing

[เนื้อหา Power BI ของการจัดการต้นทุน](../../dev-itpro/analytics/cost-management-content-pack.md) ให้ข้อมูลเชิงลึกด้านการจัดการลงในคลังสินค้าและคลังสินค้างานที่กำลังดำเนินการ (WIP) และวิธีการที่เงินสดไหลเวียนผ่านตามประเภทตามเวลา นอกจากนี้ยังสามารถใช้ข้อมูลเป็นรายละเอียดภาคผนวกสำหรับงบการเงิน

### <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

#### <a name="whats-new-and-in-development"></a>มีอะไรใหม่และอะไรที่กำลังพัฒนา

ไปที่ [แผนการทำงาน Microsoft Dynamics 365](https://roadmap.dynamics.com/) เพื่อดูว่ามีการนำคุณลักษณะใหม่ใดออกใช้ และมีคุณลักษณะใหม่ใดบ้างที่กำลังพัฒนา 

#### <a name="white-paper"></a>เอกสารทางเทคนิค
[การคำนวณ BOM โดยใช้แผ่นงานการคิดต้นทุน](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) อธิบายถึงวิธีการตั้งค่าแผ่นงานคำนวณต้นทุนที่มีวัสดุและการผลิต และวิธีที่การตั้งค่ามีผลกับผลลัพธ์การคำนวณ BOM เพื่อให้อธิบายหัวข้อได้ดีขึ้น จะแสดงสถานการณ์รูปธรรมและข้อมูลที่แสดงผลกระทบของการตั้งค่าและตั้งค่าคอนฟิกที่หลากหลาย เราไม่ได้คาดหวังให้คุณปฏิบัติตามสถานการณ์เหล่านี้ทั้งหมด เนื่องจากเอกสารนี้ไม่มีรายละเอียดเพียงพอสำหรับการตั้งค่าคอนฟิกเหล่านั้น อย่างไรก็ตาม ถ้าคุณมีความรู้พื้นฐาน คุณอาจลองเล่นคู่มืองานที่แสดงรายการด้านล่างในลำดับที่ปรากฏ ใช้ความรู้ที่คุณเคยได้รับจากการอ่านเอกสารนี้เพื่อทำการวิเคราะห์การคำนวณ BOM 

-  [สร้างผลิตภัณฑ์สำเร็จรูป](tasks/create-finished-product-2016-02.md)
-  [สร้างผลิตภัณฑ์กึ่งสำเร็จรูป](tasks/create-semi-finished-product-2016-02.md)
-  [สร้างวัตถุดิบ](tasks/create-raw-materials-2016-02.md)
-  [สร้าง BOM](tasks/create-boms-2016-02.md)
-  [สร้างกระบวนการผลิต](tasks/create-routes-2016-02.md)
-  [คำนวณ BOM โดยใช้โครงสร้างระดับเดียว](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [คำนวณ BOM โดยใช้โครงสร้างหลายระดับ](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>บล็อก
คุณสามารถค้นหาความคิดเห็น ข่าว และข้อมูลอื่นเกี่ยวกับการจัดการต้นทุนใน [บล็อกทีม R&D การผลิตของ Dynamics AX](https://blogs.msdn.microsoft.com/axmfg) และ [การจัดการห่วงโซ่อุปทานในบล็อกทีม R&D ของ Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm) แม้ว่าโพสต์เหล่านี้บางโพสต์ถูกเขียนขึ้นสำหรับการจัดการต้นทุนเวอร์ชันก่อนหน้านี้ แต่ยังคงใช้แนวคิดเดียวกัน และกระบวนงานยังคงคล้ายกันในเวอร์ชันปัจจุบันอีกด้วย

#### <a name="task-guides"></a>คู่มืองาน
วิธีใช้เพิ่มเติมพร้อมใช้งานเป็นคำแนะนำงาน ในการเข้าถึงคู่มืองาน ให้คลิกปุ่มวิธีใช้บนหน้าใดๆ

