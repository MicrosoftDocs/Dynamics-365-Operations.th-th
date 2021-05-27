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
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="aae31-103">รายงานต้นทุนทางอ้อมในกระบวนการรวมใบสั่งผลิตที่ถูกลบ</span><span class="sxs-lookup"><span data-stu-id="aae31-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="aae31-104">หมายเลข KB: 4612748</span><span class="sxs-lookup"><span data-stu-id="aae31-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="aae31-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="aae31-105">Symptoms</span></span>

<span data-ttu-id="aae31-106">รายงาน **ต้นทุนทางอ้อมในกระบวนการ** จะแสดงข้อมูลเกี่ยวกับใบสั่งผลิตที่มีการประมวลผลบางส่วนและลบในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="aae31-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="aae31-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="aae31-107">Resolution</span></span>

<span data-ttu-id="aae31-108">เมื่อคุณกลับรายการใบสั่งผลิต คุณจะกลับรายการธุรกรรมทั้งหมดของใบสั่งผลิตนั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="aae31-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="aae31-109">เมื่อคุณลบใบสั่งผลิต ตารางบัญชีแยกประเภทย่อยและบัญชีแยกประเภททั่วไปจะยังคงอยู่ธุรกรรมทั้งหมดที่เกี่ยวข้องด้วย</span><span class="sxs-lookup"><span data-stu-id="aae31-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="aae31-110">รายงานจะแสดงธุรกรรมในตารางบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="aae31-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="aae31-111">สำหรับใบสั่งผลิตเฉพาะ ค่าสุทธิควรเป็น 0.00</span><span class="sxs-lookup"><span data-stu-id="aae31-111">For the specific production order, the net value should be 0.00.</span></span>
