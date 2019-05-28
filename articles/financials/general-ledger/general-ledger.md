---
title: บัญชีแยกประเภททั่วไปและโฮมเพจการรายงานทางการเงิน
description: 'ใช้บัญชีแยกประเภททั่วไปเพื่อกำหนด และจัดการเรกคอร์ดทางการเงินของนิติบุคคล '
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b6683107f4b2dbe36af78749612ce950ea19582
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569301"
---
# <a name="general-ledger"></a>บัญชีแยกประเภททั่วไป 

[!include [banner](../includes/banner.md)]

ใช้บัญชีแยกประเภททั่วไปเพื่อกำหนด และจัดการเรกคอร์ดทางการเงินของนิติบุคคล  บัญชีแยกประเภททั่วไปมีการลงทะเบียนของรายการเดบิตและเครดิต รายการเหล่านี้มีการจัดประเภทโดยใช้บัญชีที่อยู่ในผังบัญชี 

 - [วางแผนชื่อผังบัญชีของคุณ](plan-chart-of-accounts.md)
 - [ประเถทชนิดบัญชีหลัก](main-account-types.md)

คุณสามารถปันส่วนหรือกระจายยอดเงินอย่างน้อยหนึ่งบัญชีหรือชุดบัญชีและมิติตามกฎการปันส่วน  มีอยู่สองชนิดของการปันส่วน: คงที่ และผันแปร นอกจากนี้คุณยังสามารถชำระธุรกรรมระหว่างบัญชีแยกประเภท และการประเมินค่ายอดเงินสกุลเงินใหม่ เมื่อสิ้นสุดปีบัญชี คุณต้องสร้างธุรกรรมปิดปี และจัดเตรียมบัญชีสำหรับปีบัญชีถัดไป คุณสามารถใช้ฟังก์ชันการรวมบัญชีเพื่อรวมผลลัพธ์ทางการเงินสำหรับนิติบุคคลบริษัทในเครือหลายรายเป็นผลลัพธ์สำหรับองค์กรรวมเดียว บริษัทในเครือสามารถอยู่ในฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations เดียวกันหรือต่างฐานข้อมูล

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


## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

#### <a name="whats-new-and-in-development"></a>มีอะไรใหม่และอะไรที่กำลังพัฒนา

ไปที่ [บันทึกย่อประจำรุ่น Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) เพื่อดูว่ามีการวางแผนคุณลักษณะใหม่ใด 

#### <a name="blogs"></a>บล็อก

คุณสามารถค้นหาความคิดเห็น ข่าวสาร และข้อมูลอื่นๆ ได้ใน [บล็อก Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) และ [บล็อก Microsoft Dynamics 365 Finance and Operations - Financials](https://community.dynamics.com/365/financeandoperations/b/financials)

[บล็อกชุมชนคู่ค้า Microsoft Dynamics Operations](https://community.dynamics.com/partner/b/operationspartnercommunityblog) มอบทรัพยากรเดียวให้กับคู่ค้า Microsoft Dynamics สำหรับเรียนรู้สิ่งใหม่และแนวโน้มต่างๆ ใน MBS Operations

### <a name="videos"></a>วิดีโอ

ดูวิดีโอวิธีการที่ตอนนี้มีอยู่บน [ช่อง YouTube ของ Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)

#### <a name="community-blogs"></a>บล็อกของชุมชน

- [สิ่งที่คุณควรทราบเกี่ยวกับบัญชีแยกประเภทใน Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

