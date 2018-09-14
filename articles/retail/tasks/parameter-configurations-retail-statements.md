--- 
title: " การตั้งค่าคอนฟิกพารามิเตอร์สำหรับใบแจ้งยอดการขายปลีก"
description: "กระบวนการนี้จะแสดงการตั้งค่าคอนฟิกสำหรับพารามิเตอร์ของการขายปลีกที่มีผลต่อวิธีการสร้างและลงรายการบัญชีการขายปลีก "
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="07f44-103"> การตั้งค่าคอนฟิกพารามิเตอร์สำหรับใบแจ้งยอดการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="07f44-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="07f44-104">กระบวนการนี้จะแสดงการตั้งค่าคอนฟิกสำหรับพารามิเตอร์ของการขายปลีกที่มีผลต่อวิธีการสร้างและลงรายการบัญชีการขายปลีก </span><span class="sxs-lookup"><span data-stu-id="07f44-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="07f44-105">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="07f44-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="07f44-106">ไปที่ การขายปลีกและการค้า > การตั้งค่าศูนย์ควบคุม > พารามิเตอร์ > พารามิเตอร์การขายปลีก</span><span class="sxs-lookup"><span data-stu-id="07f44-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="07f44-107">คลิกแท็บการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="07f44-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="07f44-108">เลือก "ใช่" ถ้าคุณต้องการลงรายการบัญชียอดเงินส่วนลดเป็นครั้งคราวโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="07f44-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="07f44-109">เลือก "มาตรฐาน" เพื่อใช้บัญชีเริ่มต้น หรือเลือก "ประจำงวด" ถ้าคุณต้องการกำหนดบัญชีที่จะใช้สำหรับแต่ละส่วนลดเป็นครั้งคราว</span><span class="sxs-lookup"><span data-stu-id="07f44-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="07f44-110">เลือก "สรุป" ถ้ารายการสินค้าคงคลังควรถูกรวบรวมทุกครั้งที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="07f44-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="07f44-111">เลือก "ใช่" ถ้าใบแจ้งหนี้และการชำระเงินควรได้รับชำระโดยอัตโนมัติโดยเป็นส่วนหนึ่งของกระบวนการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="07f44-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="07f44-112">เลือก "ใช่" ถ้าธุรกรรมการนำเงินฝากเข้าเซฟควรถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="07f44-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="07f44-113">เลือก "ใช่" ถ้าธุรกรรมการนำเงินฝากเข้าธนาคารควรถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="07f44-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="07f44-114">เลือก "ใช่" เพื่อเปิดการทำงานการรวมสำหรับการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="07f44-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="07f44-115">เลือก "ใช่" เพื่อสร้างและประมวลผลใบสั่งพร้อมกันเมื่อรายการบัญชีใบแจ้งยอดถูกลงรายการ</span><span class="sxs-lookup"><span data-stu-id="07f44-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="07f44-116">ป้อนจำนวนใบสั่งสูงสุดที่จะถูกประมวลผลในชุดงานแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="07f44-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="07f44-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="07f44-117">Click Save.</span></span>


