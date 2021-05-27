---
title: การวางแผนหลักสร้างแผนการใบสั่งสำหรับผลิตภัณฑ์แฝง
description: แผนการใบสั่งสร้างสำหรับผลิตภัณฑ์แฝงหลักจากเรียกใช้การวางแผนหลัก
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026956"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="4eac4-103">การวางแผนหลักสร้างแผนการใบสั่งสำหรับผลิตภัณฑ์แฝง</span><span class="sxs-lookup"><span data-stu-id="4eac4-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="4eac4-104">หมายเลข KB: 4614729</span><span class="sxs-lookup"><span data-stu-id="4eac4-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="4eac4-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="4eac4-105">Symptoms</span></span>

<span data-ttu-id="4eac4-106">แผนการใบสั่งสร้างสำหรับผลิตภัณฑ์แฝงหลักจากเรียกใช้การวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="4eac4-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="4eac4-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="4eac4-107">Resolution</span></span>

<span data-ttu-id="4eac4-108">การตั้งค่าตัวเลือก **รายการแฝง** สำหรับผลิตภัณฑ์ที่นำออกใช้จะระบุชนิดรายการเริ่มต้นบนสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="4eac4-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="4eac4-109">เมื่อตั้งค่าตัวเลือก **รายการแฝง** เป็น *ใช่* ระบบจะยังคงสร้างแผนการใบสั่งให้กับสินค้า แต่ตัวเลือก **ความต้องการที่ได้รับมาโดยตรง** สำหรับแต่ละแผนการใบสั่งจะตั้งค่าเป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="4eac4-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="4eac4-110">ดังนั้น จึงไม่สามารถยืนยันแผนการใบสั่งผลิตด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="4eac4-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="4eac4-111">ซึ่งจะรวมโดยอัตโนมัติเสมอเมื่อมีการยืนยันใบสั่งผลิตหลัก</span><span class="sxs-lookup"><span data-stu-id="4eac4-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="4eac4-112">นอกจากนี้ บรรทัด BOM ของแผนการใบสั่งแฝงจะรวมอยู่ใน BOM ของใบสั่งผลิตหลัก</span><span class="sxs-lookup"><span data-stu-id="4eac4-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
