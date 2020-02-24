---
title: กำหนดค่าพารามิเตอร์ที่มีผลต่อคำชี้แจงการขายปลีก
description: หัวข้อนี้แสดงให้เห็นถึงการกำหนดค่าสำหรับพารามิเตอร์การค้าที่มีผลต่อการสร้างและโพสต์คำชี้แจง
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
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024184"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="d3ec2-103">กำหนดค่าพารามิเตอร์ที่มีผลต่อคำชี้แจงการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="d3ec2-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d3ec2-104">หัวข้อนี้แสดงให้เห็นถึงการกำหนดค่าสำหรับพารามิเตอร์การค้าที่มีผลต่อการสร้างและโพสต์คำชี้แจง</span><span class="sxs-lookup"><span data-stu-id="d3ec2-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="d3ec2-105">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="d3ec2-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d3ec2-106">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การขายปลีกและการค้า > การตั้งสำนักงานใหญ่ > พารามิเตอร์ > พารามิเตอร์การค้า**</span><span class="sxs-lookup"><span data-stu-id="d3ec2-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="d3ec2-107">เลือกแท็บ **การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d3ec2-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="d3ec2-108">เลือก **ใช่** ถ้าคุณต้องการลงรายการบัญชียอดเงินส่วนลดเป็นครั้งคราวโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d3ec2-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="d3ec2-109">เลือก **มาตรฐาน** เพื่อใช้บัญชีเริ่มต้น หรือเลือก **ประจำงวด** ถ้าคุณต้องการกำหนดบัญชีที่จะใช้สำหรับส่วนลดเป็นครั้งคราวแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="d3ec2-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="d3ec2-110">เลือก **สรุป** ถ้ารายการสินค้าคงคลังควรถูกรวบรวมทุกครั้งที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="d3ec2-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="d3ec2-111">เลือก **ใช่** ถ้าใบแจ้งหนี้และการชำระเงินควรได้รับชำระโดยอัตโนมัติ โดยเป็นส่วนหนึ่งของกระบวนการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="d3ec2-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="d3ec2-112">เลือก **ใช่** ถ้าธุรกรรมการนำเงินฝากเข้าเซฟควรถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="d3ec2-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="d3ec2-113">เลือก **ใช่** ถ้าธุรกรรมการนำเงินฝากเข้าธนาคารควรถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="d3ec2-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="d3ec2-114">เลือก **ใช่** เพื่อเปิดการรวมสำหรับการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="d3ec2-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="d3ec2-115">เลือก **ใช่** เพื่อสร้างและประมวลผลใบสั่งพร้อมกัน เมื่อมีการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="d3ec2-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="d3ec2-116">ป้อนจำนวนใบสั่งสูงสุดที่จะถูกประมวลผลในชุดงานแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="d3ec2-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="d3ec2-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d3ec2-117">Select **Save**.</span></span>

