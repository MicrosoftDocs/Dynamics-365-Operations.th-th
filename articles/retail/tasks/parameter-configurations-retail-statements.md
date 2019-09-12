---
title: ตั้งค่าคอนฟิกพารามิเตอร์การขายปลีกที่มีผลกับใบแจ้งยอดการขายปลีก
description: หัวข้อนี้จะแสดงการตั้งค่าคอนฟิกสำหรับพารามิเตอร์ของการขายปลีกที่มีผลต่อวิธีการสร้างและลงรายการบัญชีใบแจ้งยอดการขายปลีก
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867283"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="f4870-103">ตั้งค่าคอนฟิกพารามิเตอร์การขายปลีกที่มีผลกับใบแจ้งยอดการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="f4870-103">Configure Retail parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f4870-104">หัวข้อนี้จะแสดงการตั้งค่าคอนฟิกสำหรับพารามิเตอร์ของการขายปลีกที่มีผลต่อวิธีการสร้างและลงรายการบัญชีใบแจ้งยอดการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="f4870-104">This topic demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="f4870-105">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="f4870-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="f4870-106">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การขายปลีกและการค้า > การตั้งค่าศูนย์ควบคุม > พารามิเตอร์ > พารามิเตอร์การขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="f4870-106">In the navigation pane, go to **Modules > Retail and commerce > Headquarters setup  > Parameters > Retail parameters**.</span></span>
2. <span data-ttu-id="f4870-107">เลือกแท็บ **การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="f4870-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="f4870-108">เลือก **ใช่** ถ้าคุณต้องการลงรายการบัญชียอดเงินส่วนลดเป็นครั้งคราวโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="f4870-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="f4870-109">เลือก **มาตรฐาน** เพื่อใช้บัญชีเริ่มต้น หรือเลือก **ประจำงวด** ถ้าคุณต้องการกำหนดบัญชีที่จะใช้สำหรับส่วนลดเป็นครั้งคราวแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="f4870-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="f4870-110">เลือก **สรุป** ถ้ารายการสินค้าคงคลังควรถูกรวบรวมทุกครั้งที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="f4870-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="f4870-111">เลือก **ใช่** ถ้าใบแจ้งหนี้และการชำระเงินควรได้รับชำระโดยอัตโนมัติ โดยเป็นส่วนหนึ่งของกระบวนการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="f4870-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="f4870-112">เลือก **ใช่** ถ้าธุรกรรมการนำเงินฝากเข้าเซฟควรถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="f4870-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="f4870-113">เลือก **ใช่** ถ้าธุรกรรมการนำเงินฝากเข้าธนาคารควรถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="f4870-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="f4870-114">เลือก **ใช่** เพื่อเปิดการรวมสำหรับการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="f4870-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="f4870-115">เลือก **ใช่** เพื่อสร้างและประมวลผลใบสั่งพร้อมกัน เมื่อมีการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="f4870-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="f4870-116">ป้อนจำนวนใบสั่งสูงสุดที่จะถูกประมวลผลในชุดงานแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="f4870-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="f4870-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f4870-117">Select **Save**.</span></span>

