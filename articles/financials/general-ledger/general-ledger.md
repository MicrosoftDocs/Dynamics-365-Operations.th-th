---
title: "บัญชีแยกประเภททั่วไปและโฮมเพจการรายงานทางการเงิน"
description: "ใช้บัญชีแยกประเภททั่วไปเพื่อกำหนด และจัดการเรกคอร์ดทางการเงินของนิติบุคคล "
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e544c592429d00b1ce464740f4e82cb75d10412b
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="general-ledger"></a>บัญชีแยกประเภททั่วไป 

[!include[banner](../includes/banner.md)]


ใช้บัญชีแยกประเภททั่วไปเพื่อกำหนด และจัดการเรกคอร์ดทางการเงินของนิติบุคคล  บัญชีแยกประเภททั่วไปมีการลงทะเบียนของรายการเดบิตและเครดิต รายการเหล่านี้มีการจัดประเภทโดยใช้บัญชีที่อยู่ในผังบัญชี 

 - [วางแผนชื่อผังบัญชีของคุณ](plan-chart-of-accounts.md)
 - [ประเถทชนิดบัญชีหลัก](main-account-types.md)

คุณสามารถปันส่วนหรือกระจายยอดเงินอย่างน้อยหนึ่งบัญชีหรือชุดบัญชีและมิติตามกฎการปันส่วน  มีอยู่สองชนิดของการปันส่วน: คงที่ และผันแปร นอกจากนี้คุณยังสามารถชำระธุรกรรมระหว่างบัญชีแยกประเภท และการประเมินค่ายอดเงินสกุลเงินใหม่ เมื่อสิ้นสุดปีบัญชี คุณต้องสร้างธุรกรรมปิดปี และจัดเตรียมบัญชีสำหรับปีบัญชีถัดไป คุณสามารถใช้ฟังก์ชันการรวมบัญชีเพื่อรวมผลลัพธ์ทางการเงินสำหรับนิติบุคคลบริษัทในเครือหลายรายเป็นผลลัพธ์สำหรับองค์กรรวมเดียว บริษัทในเครืออาจอยู่ภายในฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations เดียวกันหรือในฐานข้อมูลที่แยกต่างจากกันก็ได้

- [ภาพรวมของการรวมบัญชีและการตัดออก](../budgeting/consolidation-elimination-overview.md)
- [ยอดดุลบัญชีแยกประเภททั่วไป](general-ledger-account-balances.md)
- [มิติทางการเงิน](financial-dimensions.md)

[![กระบวนการทางธุรกิจ](./media/GL-process.PNG)](./media/GL-process.PNG)

## <a name="sales-tax"></a>ภาษีขาย
บริษัททุกแห่งจัดเก็บและชำระภาษีให้กับหน่วยงานจัดเก็บภาษีต่างๆ  กฎและอัตราแตกต่างกันไปตามประเทศ/ภูมิภาค รัฐ เขต และเมือง
นอกจากนี้ กฎต้องมีการอัพเดเป็นระยะ ๆ เมื่อหน่วยงานจัดเก็บภาษีเปลี่ยนแปลงข้อกำหนด รหัสภาษีการขายประกอบด้วยข้อมูลพื้นฐานเกี่ยวกับยอดภาษีที่คุณรวบรวมและชำระแก่หน่วยงานจัดเก็บภาษี เมื่อคุณตั้งค่ารหัสภาษีขาย คุณจะกำหนดจำนวนเงินหรือเปอร์เซ็นต์ที่ต้องรวบรวมไว้ คุณยังสามารถกำหนดวิธีการต่าง ๆ ที่จำนวนเงินหรือเปอร์เซ็นต์ดังกล่าวจะใช้กับจำนวนเงินธุรกรรม หัวข้อในส่วนนี้แสดงข้อมูลเกี่ยวกับวิธีการตั้งค่ารหัสภาษีขาย สำหรับวิธีการและอัตราที่หน่วยงานจัดเก็บภาษีของคุณกำหนด

 - [ภาพรวมของภาษีขาย](indirect-taxes-overview.md)
 - [อัตราภาษีขายที่ขึ้นอยู่กับฐานกำไรเบื้องต้นและวิธีการคำนวณ](marginal-base-field.md)
 - [การชำระภาษีขายและกฎการปัดเศษ](round-sales-tax-payments.md)


## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

### <a name="whats-new-and-in-development"></a>มีอะไรใหม่และอะไรที่กำลังพัฒนา

ไปที่ [แผนการทำงาน Microsoft Dynamics 365](https://roadmap.dynamics.com/) เพื่อดูว่ามีการนำคุณลักษณะใหม่ใดออกใช้ และมีคุณลักษณะใหม่ใดบ้างที่กำลังพัฒนา 

### <a name="blogs"></a>บล็อก

คุณสามารถค้นหาความคิดเห็น ข่าวสาร และข้อมูลอื่นๆ เกี่ยวกับบัญชีเจ้าหนี้และการแก้ไขปัญหาอื่นๆ ได้ใน [บล็อก Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise)

มีโพสต์ต่างๆ เกี่ยวกับบัญชีแยกประเภททั่วไปใน [บล็อกทีมผลิตภัณฑ์ Microsoft Dynamics AX](https://blogs.msdn.microsoft.com/dax/) แม้ว่าโพสต์เหล่านี้บางอย่างถูกเขียนขึ้นสำหรับเวอร์ชันก่อนหน้านี้ของบัญชีแยกประเภททั่วไป แต่ยังคงใช้แนวคิดเดียวกัน และกระบวนงานยังคงเหมือนกันในเวอร์ชันปัจจุบัน

[บล็อกชุมชนคู่ค้า Microsoft Dynamics Operations](https://community.dynamics.com/partner/b/operationspartnercommunityblog) มอบทรัพยากรเดียวให้กับคู่ค้า Microsoft Dynamics สำหรับเรียนรู้สิ่งใหม่และแนวโน้มต่างๆ ใน MBS Operations

### <a name="task-guides"></a>คู่มืองาน
วิธีใช้เพิ่มเติมพร้อมใช้เป็นคู่มืองานภายใน Finance and Operations ในการเข้าถึงคู่มืองาน ให้คลิกปุ่มวิธีใช้บนหน้าใดๆ

### <a name="videos"></a>วิดีโอ

ดูวิดีโอวิธีการที่ตอนนี้มีอยู่บน [ช่อง YouTube ของ Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)


