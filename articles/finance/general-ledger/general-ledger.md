---
title: ภาพรวมบัญชีแยกประเภททั่วไปและการรายงานทางการเงิน
description: 'ใช้บัญชีแยกประเภททั่วไปเพื่อกำหนด และจัดการเรกคอร์ดทางการเงินของนิติบุคคล '
author: ShylaThompson
ms.date: 08/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60ebe19d53e87e385af8e32c32b9c0cc43291eba
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832885"
---
# <a name="general-ledger-home-page"></a>โฮมเพจบัญชีแยกประเภททั่วไป

[!include [banner](../includes/banner.md)]

ใช้บัญชีแยกประเภททั่วไปเพื่อกำหนด และจัดการเรกคอร์ดทางการเงินของนิติบุคคล  บัญชีแยกประเภททั่วไปมีการลงทะเบียนของรายการเดบิตและเครดิต รายการเหล่านี้มีการจัดประเภทโดยใช้บัญชีที่อยู่ในผังบัญชี 

 - [วางแผนชื่อผังบัญชีของคุณ](plan-chart-of-accounts.md)
 - [ประเถทชนิดบัญชีหลัก](main-account-types.md)

คุณสามารถปันส่วนหรือกระจายยอดเงินอย่างน้อยหนึ่งบัญชีหรือชุดบัญชีและมิติตามกฎการปันส่วน  มีอยู่สองชนิดของการปันส่วน: คงที่ และผันแปร นอกจากนี้คุณยังสามารถชำระธุรกรรมระหว่างบัญชีแยกประเภท และการประเมินค่ายอดเงินสกุลเงินใหม่ เมื่อสิ้นสุดปีบัญชี คุณต้องสร้างธุรกรรมปิดปี และจัดเตรียมบัญชีสำหรับปีบัญชีถัดไป คุณสามารถใช้ฟังก์ชันการรวมบัญชีเพื่อรวมผลลัพธ์ทางการเงินสำหรับนิติบุคคลบริษัทในเครือหลายรายเป็นผลลัพธ์สำหรับองค์กรรวมเดียว บริษัทในเครือสามารถอยู่ในฐานข้อมูลเดียวกันหรือต่างฐานข้อมูลได้

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

ไปที่ [แผนการเผยแพร่ Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) เพื่อดูว่ามีคุณสมบัติใหม่ใดวางแผนไว้ 

#### <a name="financial-reporting"></a>การรายงานทางการเงิน
ไปที่หัวข้อ [ภาพรวมของ Financial Reporting](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) สำหรับข้อมูลเกี่ยวกับรายงานทางการเงิน

#### <a name="blogs"></a>บล็อก

คุณสามารถดูความคิดเห็น ข่าวสาร และข้อมูลอื่นๆ ได้ใน [บล็อก Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) และ [บล็อก Microsoft Dynamics 365 Finance and Operations - Financials](https://community.dynamics.com/365/financeandoperations/b/financials)

[บล็อกชุมชนคู่ค้า Microsoft Dynamics Operations](https://community.dynamics.com/partner/b/operationspartnercommunityblog) มอบทรัพยากรเดียวให้กับคู่ค้า Microsoft Dynamics สำหรับเรียนรู้สิ่งใหม่และแนวโน้มต่างๆ ใน Dynamics 365

### <a name="videos"></a>วิดีโอ

ดูวิดีโอวิธีการที่ตอนนี้มีอยู่บน [ช่อง YouTube ของ Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)

#### <a name="community-blogs"></a>บล็อกของชุมชน

- [สิ่งที่คุณควรทราบเกี่ยวกับบัญชีแยกประเภทใน Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]