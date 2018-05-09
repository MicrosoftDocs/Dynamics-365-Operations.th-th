--- 
title: " สร้าง คำนวณ และลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้าปลีก"
description: "กระบวนการนี้นำไปสู่ขั้นตอนการสร้าง, การคำนวณ, และการลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้าด้วยตนเอง "
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 08a8f937f63b93ad15e489dbc53468af6e3827b4
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="fbf5c-103"> สร้าง คำนวณ และลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="fbf5c-103">Create, calculate, and post a statement for a retail store</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fbf5c-104">กระบวนการนี้นำไปสู่ขั้นตอนการสร้าง, การคำนวณ, และการลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้าด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="fbf5c-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="fbf5c-105">อีกทั้งยังมีชุดงานที่สามารถตั้งค่าคอนฟิกสำหรับงานเดียวกัน </span><span class="sxs-lookup"><span data-stu-id="fbf5c-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="fbf5c-106">คุณจะพบขั้นตอนสำหรับการตั้งค่าคอนฟิกและการรันชุดงานในหัวข้ออื่น </span><span class="sxs-lookup"><span data-stu-id="fbf5c-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="fbf5c-107">การทำงานนี้ให้สำเร็จ คุณต้องมีธุรกรรมที่เสร็จสมบูรณ์ใน POS และจากนั้นดึงมาไว้ใน Dynamics AX </span><span class="sxs-lookup"><span data-stu-id="fbf5c-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="fbf5c-108">การบันทึกข้อมูลนี้ใช้บริษัท USRT ในข้อมูลสาธิต </span><span class="sxs-lookup"><span data-stu-id="fbf5c-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="fbf5c-109">กระบวนงานนี้อาจอ้างถึง Microsoft Dynamics AX </span><span class="sxs-lookup"><span data-stu-id="fbf5c-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="fbf5c-110">โปรดทราบว่าปัจจุบัน Dynamics AX เรียกว่า Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="fbf5c-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="fbf5c-111">ไปที่ พื้นที่ทำงานทั้งหมด > ..</span><span class="sxs-lookup"><span data-stu-id="fbf5c-111">Go to All workspaces > ..</span></span> <span data-ttu-id="fbf5c-112">> การเงินของร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="fbf5c-112">> Retail store financials.</span></span>
2. <span data-ttu-id="fbf5c-113">คลิก สร้างใบแจ้งยอดใหม่</span><span class="sxs-lookup"><span data-stu-id="fbf5c-113">Click New statement.</span></span>
3. <span data-ttu-id="fbf5c-114">ในฟิลด์หมายเลขร้านค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fbf5c-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fbf5c-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fbf5c-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="fbf5c-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fbf5c-116">Click OK.</span></span>
    * <span data-ttu-id="fbf5c-117">กลุ่มการตั้งค่ามีการตั้งค่าที่ควบคุมธุรกรรมต่างๆที่รวมอยู่ในรายงานการเงินและวิธีการจัดกลุ่มลงในรายการใบแจ้งยอด </span><span class="sxs-lookup"><span data-stu-id="fbf5c-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="fbf5c-118">คุณสามารถเปิดกลุ่มการตั้งค่าและเปลี่ยนการตั้งค่าเหล่านี้ หรือคุณสามารถใช้ค่าเริ่มต้นก็ได้</span><span class="sxs-lookup"><span data-stu-id="fbf5c-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="fbf5c-119">ในฟิลด์วิธีการจัดทำใบแจ้งยอด กำหนดวิธีจัดกลุ่มรายการใบแจ้งยอดว่าจะเป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="fbf5c-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="fbf5c-120">เลือกพนักงานหรือเครื่องบันทึกเงินสด ถ้าคุณต้องการคำนวณรายงานการเงินสำหรับพนักงานเฉพาะบางคนเท่านั้นหรือลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="fbf5c-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="fbf5c-121">ในฟิลด์วิธีการปิดบัญชี ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="fbf5c-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="fbf5c-122">คลิกคำนวณใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="fbf5c-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="fbf5c-123">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="fbf5c-123">Click Yes.</span></span>
    * <span data-ttu-id="fbf5c-124">หลังจากการคำนวณรายงานการเงิน ควรมีรายการที่สร้างขึ้นด้วยยอดเงินรวมจากวิธีการชำระเงินแต่ละวิธีและวิธีการการจัดทำใบแจ้งยอดที่ใช้</span><span class="sxs-lookup"><span data-stu-id="fbf5c-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="fbf5c-125">ป้อนยอดเงินที่ตรวจนับในแต่ละบรรทัดถ้าจำเป็นต้องป้อนหรือปรับปรุง </span><span class="sxs-lookup"><span data-stu-id="fbf5c-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="fbf5c-126">ในฟิลด์ตรวจนับนั้นถูกเติมด้วยการตรวจนับเงินใน POS</span><span class="sxs-lookup"><span data-stu-id="fbf5c-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="fbf5c-127">คลิกลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="fbf5c-127">Click Post statement.</span></span>
10. <span data-ttu-id="fbf5c-128">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="fbf5c-128">Click Close.</span></span>
11. <span data-ttu-id="fbf5c-129">ไปที่การขายปลีกและการค้า > ช่องทาง > การเงินของร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="fbf5c-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="fbf5c-130">คลิกแท็บใบแจ้งยอดที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="fbf5c-130">Click the Posted statements tab.</span></span>


