---
title: เซ็ตมิติทางการเงิน
description: หัวข้อนี้อธิบายเซ็ตมิติทางการเงินและเทคนิคบางอย่างเพื่อเพิ่มประสิทธิภาพการใช้
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021839"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="50fc0-103">เซ็ตมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="50fc0-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50fc0-104">หัวข้อนี้อธิบายเซ็ตมิติทางการเงินและเทคนิคบางอย่างเพื่อเพิ่มประสิทธิภาพการใช้</span><span class="sxs-lookup"><span data-stu-id="50fc0-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="50fc0-105">เซ็ตมิติคือรายการมิติทางการเงินที่สั่ง ซึ่งสามารถใช้ในการสรุปข้อมูลบัญชีแยกประเภททั่วไปในลักษณะที่ผู้ใช้กําหนด</span><span class="sxs-lookup"><span data-stu-id="50fc0-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="50fc0-106">การใช้เซ็ตมิติหลักคือเพื่อกําหนดงบทดลอง</span><span class="sxs-lookup"><span data-stu-id="50fc0-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="50fc0-107">เฉพาะเซ็ตมิติมาตรฐานเท่านั้นคือเซ็ตมิติที่มีเฉพาะบัญชีหลักเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="50fc0-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="50fc0-108">คุณใช้หน้า **เซ็ตมิติทางการเงิน** เพื่อสร้างและจัดการเซ็ตมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="50fc0-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="50fc0-109">ยอดดุลเซ็ตมิติ</span><span class="sxs-lookup"><span data-stu-id="50fc0-109">Dimension set balances</span></span>

<span data-ttu-id="50fc0-110">เซ็ตมิติสามารถมียอดดุลที่ขึ้นอยู่กับมิติทางการเงินได้</span><span class="sxs-lookup"><span data-stu-id="50fc0-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="50fc0-111">ยอดดุลมีอยู่ในบัญชีแยกประเภททั่วไปและเป็นไปตามนิยามเซ็ตมิติ</span><span class="sxs-lookup"><span data-stu-id="50fc0-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="50fc0-112">โดยสรุปยอดดุลจากข้อมูลบัญชีแยกประเภททั่วไป เพื่อช่วยปรับปรุงประสิทธิภาพการผลการปฏิบัติงานเมื่อมีการดึงข้อมูล (ตัวอย่างเช่น เมื่อสร้างงบทดลอง)</span><span class="sxs-lookup"><span data-stu-id="50fc0-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="50fc0-113">สร้างยอดดุล</span><span class="sxs-lookup"><span data-stu-id="50fc0-113">Create balances</span></span>

<span data-ttu-id="50fc0-114">ใช้ปุ่ม **สร้างยอดดุล** เพื่อเริ่มต้นยอดดุลของเซ็ตมิติที่ไม่ได้มียอดดุลอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="50fc0-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="50fc0-115">ขอแนะนำว่าคุณควรจํากัดจํานวนเซ็ตมิติที่มียอดดุล เนื่องจากการอัพเดตยอดดุลจะมีผลกระทบต่อกิจกรรมการลงรายการบัญชีแยกประเภททั่วไปทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="50fc0-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="50fc0-116">อัพเดตยอดดุล</span><span class="sxs-lookup"><span data-stu-id="50fc0-116">Update balances</span></span>

<span data-ttu-id="50fc0-117">ใช้ปุ่ม **อัปเดตยอดดุล** เพื่อรวมกิจกรรมการลงรายการบัญชีแยกประเภททั่วไปล่าสุดในยอดดุล</span><span class="sxs-lookup"><span data-stu-id="50fc0-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="50fc0-118">การอัปเดตยอดดุลคือการดําเนินงานเบา</span><span class="sxs-lookup"><span data-stu-id="50fc0-118">Balance updates are light operations.</span></span> <span data-ttu-id="50fc0-119">ผู้ใช้ต้องประมวลผลเฉพาะกิจกรรมการลงรายการบัญชีแยกประเภททั่วไปที่เกิดขึ้นนับตั้งแต่การอัปเดตครั้งสุดท้ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="50fc0-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="50fc0-120">การแสดงงบทดลองจะบังคับให้การอัปเดตช่วยให้แน่ใจว่ายอดดุลที่แสดงเป็นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="50fc0-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="50fc0-121">พิจารณาการใช้ชุดงานที่เกิดซน เพื่อให้การอัปเดตเซ็ตมิติที่ใช้บ่อยที่สุดของคุณได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="50fc0-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="50fc0-122">ด้วยวิธีนี้ คุณช่วยลดเวลาที่ผู้ใช้งบทดลองต้องรอ</span><span class="sxs-lookup"><span data-stu-id="50fc0-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="50fc0-123">สร้างยอดดุลอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="50fc0-123">Rebuild balances</span></span>

<span data-ttu-id="50fc0-124">ใช้ปุ่ม **สร้างยอดดุลอีกครั้ง** เพื่อสร้างยอดดุลใหม่ตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="50fc0-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="50fc0-125">ด้วยวิธีนี้ คุณช่วยให้มั่นใจว่าข้อมูลตรงกับข้อมูลในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="50fc0-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="50fc0-126">การสร้างยอดดุลใหม่ต้องมีการประมวลผลจำนวนมากและไม่ควรต้องใช้</span><span class="sxs-lookup"><span data-stu-id="50fc0-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="50fc0-127">ถ้าคุณมีสถานการณ์สมทบที่ต้องมีการสร้างยอดดุลใหม่เป็นสมทบ ขอแนะนำว่าคุณควรติดต่อฝ่ายสนับสนุนลูกค้า</span><span class="sxs-lookup"><span data-stu-id="50fc0-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="50fc0-128">ฝ่ายสนับสนุนลูกค้าสามารถช่วยคุณระบุเหตุผลที่ยอดดุลไม่ตรงกับข้อมูลในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="50fc0-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="50fc0-129">ชำระยอดดุล</span><span class="sxs-lookup"><span data-stu-id="50fc0-129">Clear balances</span></span>

<span data-ttu-id="50fc0-130">ใช้ปุ่ม **ล้างข้อมูลยอดดุล** เพื่อลบยอดดุล และหยุดการอัปเดตเพิ่มเติมใดๆ</span><span class="sxs-lookup"><span data-stu-id="50fc0-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="50fc0-131">เซ็ตมิติจะไม่มีผลกระทบต่อกิจกรรมการลงรายการบัญชีแยกประเภททั่วไปอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="50fc0-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="50fc0-132">สำหรับข้อมูลเพิ่มเติม ดู [มิติทางการเงิน](financial-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="50fc0-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
