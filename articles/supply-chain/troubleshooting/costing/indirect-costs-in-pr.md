---
title: รายงานต้นทุนทางอ้อมในกระบวนการรวมใบสั่งผลิตที่ถูกลบ
description: รายงานต้นทุนทางอ้อมในกระบวนการจะแสดงข้อมูลเกี่ยวกับใบสั่งผลิตที่มีการประมวลผลบางส่วนและลบในภายหลัง
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026950"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>รายงานต้นทุนทางอ้อมในกระบวนการรวมใบสั่งผลิตที่ถูกลบ

หมายเลข KB: 4612748

## <a name="symptoms"></a>อาการ

รายงาน **ต้นทุนทางอ้อมในกระบวนการ** จะแสดงข้อมูลเกี่ยวกับใบสั่งผลิตที่มีการประมวลผลบางส่วนและลบในภายหลัง

## <a name="resolution"></a>ความละเอียด

เมื่อคุณกลับรายการใบสั่งผลิต คุณจะกลับรายการธุรกรรมทั้งหมดของใบสั่งผลิตนั้นด้วย เมื่อคุณลบใบสั่งผลิต ตารางบัญชีแยกประเภทย่อยและบัญชีแยกประเภททั่วไปจะยังคงอยู่ธุรกรรมทั้งหมดที่เกี่ยวข้องด้วย รายงานจะแสดงธุรกรรมในตารางบัญชีแยกประเภทย่อย สำหรับใบสั่งผลิตเฉพาะ ค่าสุทธิควรเป็น 0.00
