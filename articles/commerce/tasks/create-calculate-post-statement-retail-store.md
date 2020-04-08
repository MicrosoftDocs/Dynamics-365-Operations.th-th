---
title: สร้าง คำนวณ และลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้าปลีก
description: หัวข้อนี้อธิบายขั้นตอนที่ต้องดำเนินการด้วยตนเองสำหรับการสร้าง การคำนวณ และการลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้า
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21f1b0a34205e192957405bc9d298c45c8bb4d25
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141025"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="2697c-103">สร้าง คำนวณ และลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="2697c-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2697c-104">หัวข้อนี้อธิบายขั้นตอนที่ต้องดำเนินการด้วยตนเองสำหรับการสร้าง การคำนวณ และการลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="2697c-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="2697c-105">อีกทั้งยังมีชุดงานที่สามารถตั้งค่าคอนฟิกสำหรับงานเดียวกัน </span><span class="sxs-lookup"><span data-stu-id="2697c-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="2697c-106">คุณจะพบขั้นตอนสำหรับการตั้งค่าคอนฟิกและการรันชุดงานในหัวข้ออื่น </span><span class="sxs-lookup"><span data-stu-id="2697c-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="2697c-107">เพื่อทำให้กระบวนงานนี้เสร็จสมบูรณ์ คุณต้องมีธุรกรรมที่เสร็จสมบูรณ์แล้วใน POS และจากนั้นถูกดึงเข้าสู่ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2697c-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="2697c-108">การบันทึกข้อมูลนี้ใช้บริษัท USRT ในข้อมูลสาธิต </span><span class="sxs-lookup"><span data-stu-id="2697c-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2697c-109">เลือก **การเงินของร้านค้า** จากโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="2697c-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="2697c-110">เลือก **สร้างใบแจ้งยอด**</span><span class="sxs-lookup"><span data-stu-id="2697c-110">Select **New statement**.</span></span>
3. <span data-ttu-id="2697c-111">ในฟิลด์ **หมายเลขร้านค้า** ให้เลือกตัวเลือกจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="2697c-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="2697c-112">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2697c-112">Select **OK**.</span></span>
5. <span data-ttu-id="2697c-113">กลุ่ม **การตั้งค่า** มีการตั้งค่าที่ควบคุมธุรกรรมต่างๆ ที่รวมอยู่ในใบแจ้งยอด และวิธีการจัดกลุ่มลงในรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="2697c-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="2697c-114">คุณสามารถเปิดกลุ่ม **การตั้งค่า** และเปลี่ยนการตั้งค่าเหล่านี้ หรือคุณสามารถใช้ค่าเริ่มต้นได้</span><span class="sxs-lookup"><span data-stu-id="2697c-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="2697c-115">ในฟิลด์ **วิธีการจัดทำใบแจ้งยอด** กำหนดวิธีการที่จะจัดกลุ่มรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="2697c-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="2697c-116">เลือกพนักงานหรือเครื่องบันทึกเงินสดในฟิลด์ **พนักงาน/เครื่องบันทึกเงินสด** ถ้าคุณต้องการคำนวณใบแจ้งยอดเท่านั้นสำหรับพนักงานหรือเครื่องบันทึกเงินสดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2697c-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="2697c-117">ในฟิลด์ **วิธีการปิดบัญชี** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2697c-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="2697c-118">เลือก **คำนวณใบแจ้งยอด** จากบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="2697c-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="2697c-119">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="2697c-119">Select **Yes**.</span></span>
    - <span data-ttu-id="2697c-120">หลังจากการคำนวณรายงานการเงิน ควรมีรายการที่สร้างขึ้นด้วยยอดเงินรวมจากวิธีการชำระเงินแต่ละวิธีและวิธีการการจัดทำใบแจ้งยอดที่ใช้</span><span class="sxs-lookup"><span data-stu-id="2697c-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="2697c-121">ป้อนยอดเงินที่ตรวจนับในแต่ละบรรทัดถ้าจำเป็นต้องป้อนหรือปรับปรุง </span><span class="sxs-lookup"><span data-stu-id="2697c-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="2697c-122">ในฟิลด์ตรวจนับนั้นถูกเติมด้วยการตรวจนับเงินใน POS</span><span class="sxs-lookup"><span data-stu-id="2697c-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="2697c-123">เลือก **ลงรายการบัญชีใบแจ้งยอด** จากบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="2697c-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="2697c-124">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="2697c-124">Select **Close**.</span></span>
11. <span data-ttu-id="2697c-125">ปิดบานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="2697c-125">Close the pane.</span></span>
12. <span data-ttu-id="2697c-126">ที่โฮมเพจ เลือก **การเงินของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="2697c-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="2697c-127">เลือกแท็บ **ใบแจ้งยอดที่ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2697c-127">Select the **Posted statements** tab.</span></span>

