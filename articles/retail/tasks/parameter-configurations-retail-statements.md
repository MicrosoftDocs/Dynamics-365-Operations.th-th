--- 
title: " การตั้งค่าคอนฟิกพารามิเตอร์สำหรับใบแจ้งยอดการขายปลีก"
description: "กระบวนการนี้จะแสดงการตั้งค่าคอนฟิกสำหรับพารามิเตอร์ของการขายปลีกที่มีผลต่อวิธีการสร้างและลงรายการบัญชีการขายปลีก "
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 0c93633e92221264cc6a67c74d62edaa59bdbd2f
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="15d86-103"> การตั้งค่าคอนฟิกพารามิเตอร์สำหรับใบแจ้งยอดการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="15d86-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="15d86-104">กระบวนการนี้จะแสดงการตั้งค่าคอนฟิกสำหรับพารามิเตอร์ของการขายปลีกที่มีผลต่อวิธีการสร้างและลงรายการบัญชีการขายปลีก </span><span class="sxs-lookup"><span data-stu-id="15d86-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="15d86-105">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="15d86-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="15d86-106">ไปที่ การขายปลีกและการค้า > การตั้งค่าศูนย์ควบคุม > พารามิเตอร์ > พารามิเตอร์การขายปลีก</span><span class="sxs-lookup"><span data-stu-id="15d86-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="15d86-107">คลิกแท็บการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="15d86-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="15d86-108">เลือก "ใช่" ถ้าคุณต้องการลงรายการบัญชียอดเงินส่วนลดเป็นครั้งคราวโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="15d86-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="15d86-109">เลือก "มาตรฐาน" เพื่อใช้บัญชีเริ่มต้น หรือเลือก "ประจำงวด" ถ้าคุณต้องการกำหนดบัญชีที่จะใช้สำหรับแต่ละส่วนลดเป็นครั้งคราว</span><span class="sxs-lookup"><span data-stu-id="15d86-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="15d86-110">เลือก "สรุป" ถ้ารายการสินค้าคงคลังควรถูกรวบรวมทุกครั้งที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="15d86-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="15d86-111">เลือก "ใช่" ถ้าใบแจ้งหนี้และการชำระเงินควรได้รับชำระโดยอัตโนมัติโดยเป็นส่วนหนึ่งของกระบวนการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="15d86-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="15d86-112">เลือก "ใช่" ถ้าธุรกรรมการนำเงินฝากเข้าเซฟควรถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="15d86-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="15d86-113">เลือก "ใช่" ถ้าธุรกรรมการนำเงินฝากเข้าธนาคารควรถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="15d86-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="15d86-114">เลือก "ใช่" เพื่อเปิดการทำงานการรวมสำหรับการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="15d86-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="15d86-115">เลือก "ใช่" เพื่อสร้างและประมวลผลใบสั่งพร้อมกันเมื่อรายการบัญชีใบแจ้งยอดถูกลงรายการ</span><span class="sxs-lookup"><span data-stu-id="15d86-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="15d86-116">ป้อนจำนวนใบสั่งสูงสุดที่จะถูกประมวลผลในชุดงานแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="15d86-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="15d86-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="15d86-117">Click Save.</span></span>


