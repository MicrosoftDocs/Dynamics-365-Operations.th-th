---
title: เตรียมนิติบุคคลสำหรับใช้ในกระบวนการรวมบัญชี
description: ในระหว่างการรวมบัญชี คุณรวบรวมธุรกรรมจากบัญชีนิติบุคคลหลายชุดเข้าในชุดบัญชีนิติบุคคลเดียวกัน หัวข้อนี้อธิบายวิธีการจัดเตรียมนิติบุคคลในการรวมบัญชี
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6f718bef3b1b07d3bb03dbf6acbf1cdf58aa7b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815487"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="a75a0-104">เตรียมนิติบุคคลสำหรับใช้ในกระบวนการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a75a0-105">ในระหว่างการรวมบัญชี คุณรวบรวมธุรกรรมจากบัญชีนิติบุคคลหลายชุดเข้าในชุดบัญชีนิติบุคคลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a75a0-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="a75a0-106">หัวข้อนี้อธิบายวิธีการจัดเตรียมนิติบุคคลในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="a75a0-107">ขอแนะนำว่าคุณควรใช้ Management Reporter for Microsoft Dynamics 365 Finance ในการรวมผลลัพธ์ทางการเงินของนิติบุคคลหลายฉบับในรูปแบบที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="a75a0-108">Management Reporter ช่วยให้คุณสามารถสร้างรายงานทางการเงินที่รวมบัญชีระหว่างนิติบุคคลต่าง ๆ ใช้ Excel เพื่อนําเข้าข้อมูลการรวมบัญชีจากแหล่งที่มาอื่นๆ และแปลยอดเงินเป็นสกุลเงินการรายงานต่าง ๆ โดยไม่ต้องรันกระบวนการรวมบัญชีใน Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="a75a0-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="a75a0-109">คุณสามารถพิมพ์รายงาน เช่น งบการเงิน จากนิติบุคคลที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="a75a0-110">อย่างไรก็ตาม คุณไม่สามารถใช้กับนิติบุคคลที่รวมบัญชีสำหรับธุรกรรมประจำวัน</span><span class="sxs-lookup"><span data-stu-id="a75a0-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="a75a0-111">คุณสามารถรวมข้อมูลจากนิติบุคคลที่ใช้ฐานข้อมูลที่แตกต่างจากนิติบุคคลที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="a75a0-112">กระบวนการรวมบัญชีนี้เรียกว่า *การรวมการนำเข้า*</span><span class="sxs-lookup"><span data-stu-id="a75a0-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="a75a0-113">อีกทางหนึ่งคือ นิติบุคคลที่สามารถใช้ฐานข้อมูลเดียวกับนิติบุคคลที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="a75a0-114">กระบวนการรวมบัญชีนี้จะถูกอ้างถึงเป็น *การรวมบัญชีทางออนไลน์*</span><span class="sxs-lookup"><span data-stu-id="a75a0-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="a75a0-115">นิติบุคคลที่รวมบัญชีรวบรวมผลลัพธ์และยอดดุลของบริษัทในเครือ</span><span class="sxs-lookup"><span data-stu-id="a75a0-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="a75a0-116">เพื่อจัดเตรียมนิติบุคคลที่รวมบัญชีสำหรับการรวมบัญชี ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a75a0-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="a75a0-117">ไปที่ **บัญชีแยกประเภททั่วไป \> การตั้งค่า \> องค์กร \> นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="a75a0-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="a75a0-118">เลือก **สร้าง** เพื่อสร้างนิติบุคคลใหม่ที่จะเป็นนิติบุคคลที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="a75a0-119">เลือกกล่องกาเครื่องหมาย **ใช้เพื่อกระบวนการรวมบัญชีทางการเงิน** แล้วป้อนข้อมูลเกี่ยวกับนิติบุคคลที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="a75a0-120">ตรวจสอบให้แน่ใจว่าได้ป้อนข้อมูลนี้เหมือนกับที่คุณต้องการให้ปรากฏในงบการเงินสำหรับนิติบุคคลที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="a75a0-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a75a0-121">Close the page.</span></span>
5. <span data-ttu-id="a75a0-122">เลือกนิติบุคคลที่รวมบัญชีในฟิลด์ ในมุมด้านขวาบนของหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a75a0-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="a75a0-123">ไปที่ **บัญชีแยกประเภททั่วไป \> การตั้งค่า \> บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="a75a0-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="a75a0-124">เลือกผังบัญชี ปฏิทินทางการเงิน สกุลเงินทางบัญชี สกุลเงินการรายงานเสริม และชนิดอัตราแลกเปลี่ยนเริ่มต้นสำหรับนิติบุคคลที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="a75a0-125">ไปที่ **บัญชีแยกประเภททั่วไป \> การตั้งค่า \> สกุลเงิน \> อัตราแลกเปลี่ยนสกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="a75a0-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="a75a0-126">ตั้งค่าอัตราแลกเปลี่ยนสกุลเงินในรอบระยะเวลาที่เกี่ยวข้องสำหรับสกุลเงินของนิติบุคคลในเครือ</span><span class="sxs-lookup"><span data-stu-id="a75a0-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="a75a0-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a75a0-127">Close the page.</span></span>
11. <span data-ttu-id="a75a0-128">ถ้านิติบุคคลที่รวมบัญชีมีบริษัทในเครือที่ใช้สกุลเงินต่างประเทศ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a75a0-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="a75a0-129">ไปที่ **บัญชีแยกประเภททั่วไป \> การตั้งค่า \> การลงรายการบัญชี \> บัญชีสำหรับธุรกรรมอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="a75a0-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="a75a0-130">ในฟิลด์ **ชนิดการลงรายการบัญชี** ให้เลือกบัญชีที่เหมาะสม:</span><span class="sxs-lookup"><span data-stu-id="a75a0-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="a75a0-131">ถ้านิติบุคคลมีบริษัทในเครือต่างประเทศที่เป็นบริษัทสาขาทางการเงินหรือที่ขึ้นต่อกันระหว่างบริษัทกับนิติบุคคลหลัก ให้เลือกบัญชีที่เหมาะสมสําหรับชนิดการลงรายการบัญชี **บัญชีกำไรขาดทุนสำหรับผลต่างการรวมบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a75a0-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="a75a0-132">ถ้าคุณกำลังรวมบริษัทในเครือที่ไม่พึ่งพานิติบุคคลหลักทางการเงินหรือการดำเนินธุรกิจ หรือนิติบุคคลที่ประกอบด้วยผลลัพธ์ของบริษัทในเครือต่างๆ ไม่พึ่งพานิติบุคคลหลักทางการเงินหรือการดำเนินธุรกิจ และเมื่อคุณใช้วิธีการแปลการรวมข้อมูล เลือกบัญชีที่เหมาะสมสำหรับชนิดการลงรายการบัญชี **บัญชีดุลสำหรับผลต่างการรวมบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a75a0-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="a75a0-133">ในฟิลด์ **บัญชีหลัก** เลือกบัญชีหลักที่ควรใช้สำหรับการปรับปรุงการประเมินค่าใหม่ตามสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="a75a0-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="a75a0-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a75a0-134">Close the page.</span></span>

    <span data-ttu-id="a75a0-135">ถ้าคุณสร้างนิติบุคคลที่รวมบัญชีในช่วงต้นของรอบระยะเวลา คุณสามารถประเมินค่ายอดเงินสกุลเงินต่างประเทศอีกครั้งเป็นอัตราแลกเปลี่ยนในระหว่างรอบระยะเวลาการรวมบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="a75a0-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="a75a0-136">นิติบุคคลที่รวมบัญชีในขณะนี้ได้รับการตั้งค่าสำหรับ **รวมบัญชี** งานประจำงวด</span><span class="sxs-lookup"><span data-stu-id="a75a0-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="a75a0-137">คุณสามารถรวมบัญชีการนําเข้าหรือการรวมบัญชีทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="a75a0-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="a75a0-138">เมื่อต้องการรวมบัญชีการนําเข้า ให้ไปที่ **บัญชีแยกประเภททั่วไป \> ประจำงวด \> รวมบัญชี \> รวมบัญชี \[นำเข้าจาก\]**</span><span class="sxs-lookup"><span data-stu-id="a75a0-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="a75a0-139">เมื่อต้องการรวมบัญชีออนไลน์ ให้ไปที่ **บัญชีแยกประเภททั่วไป \> ประจำงวด \> รวมบัญชี \> รวมบัญชี \[ออนไลน์\]**</span><span class="sxs-lookup"><span data-stu-id="a75a0-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="a75a0-140">ก่อนที่คุณจะสามารถประมวลผลการรวมบัญชี คุณต้องจัดเตรียมนิติบุคคลในเครือสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="a75a0-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="a75a0-141">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่านิติบุคคลบริษัทในเครือไว้สำหรับการรวมบัญชี](set-up-subsidiary-company-for-consolidation.md)</span><span class="sxs-lookup"><span data-stu-id="a75a0-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]