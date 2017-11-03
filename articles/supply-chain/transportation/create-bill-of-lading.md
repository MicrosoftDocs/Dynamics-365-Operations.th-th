---
title: "สร้างใบตราส่ง"
description: "หัวข้อนี้อธิบายวิธีการสร้างใบตราส่งเมื่อใช้กระบวนการจัดการคลังสินค้า"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ab5aa60198e442237fd85bb295589ae0ebe9c5f5
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-bill-of-lading"></a><span data-ttu-id="a5c88-103">สร้างใบตราส่ง</span><span class="sxs-lookup"><span data-stu-id="a5c88-103">Create a bill of lading</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a5c88-104">หัวข้อนี้อธิบายวิธีการสร้างใบตราส่งเมื่อใช้กระบวนการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a5c88-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="a5c88-105">ใบตราส่งคือเอกสารทางกฎหมายระหว่างบริษัทที่จัดส่งสินค้าและผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a5c88-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="a5c88-106">เอกสารจะมาพร้อมกับสินค้าที่จัดส่งและจะใช้เป็นใบรับสินค้าของการจัดส่งเมื่อมีการจัดส่งสินค้าที่ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a5c88-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="a5c88-107">ถ้าคุณกำลังใช้การบริหารคลังสินค้า มีสองวิธีในการสร้างใบตราส่ง:</span><span class="sxs-lookup"><span data-stu-id="a5c88-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="a5c88-108">สร้างการรายงานด้วยตนเองโดยใช้หน้า **ใบตราส่ง**</span><span class="sxs-lookup"><span data-stu-id="a5c88-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="a5c88-109">สร้างรายงานจาก **เวิร์กเบนซ์การวางแผนการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="a5c88-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="a5c88-110">ถ้าคุณสร้างใบตราส่งจาก **เวิร์กเบนซ์การวางแผนการบรรทุก**สถานะการบรรทุกจะต้องเป็น **จัดส่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="a5c88-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="a5c88-111">ถ้ามีการจัดส่งมากกว่าหนึ่งครั้งในการบรรทุก จะมีการสร้างใบตราส่งสำหรับแต่ละการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="a5c88-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="a5c88-112">เมื่อใบตราส่งถูกสร้างขึ้นแล้ว คุณสามารถทำการเปลี่ยนแปลงได้ในหน้า **ใบตราส่ง**</span><span class="sxs-lookup"><span data-stu-id="a5c88-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="a5c88-113">ใบตราส่งหลัก</span><span class="sxs-lookup"><span data-stu-id="a5c88-113">Master bill of lading</span></span>
<span data-ttu-id="a5c88-114">ถ้าการจัดส่งมากกว่าหนึ่งรายการในการบรรทุก คุณสามารถสร้างใบตราส่งหลักได้</span><span class="sxs-lookup"><span data-stu-id="a5c88-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="a5c88-115">ซึ่งมีโครงร่างและข้อมูลเช่นเดียวกับใบตราส่ง แต่ประกอบด้วยเนื้อหาสรุปสำหรับการจัดส่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a5c88-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="a5c88-116">ถ้าตัวเลือก **สร้างใบตราส่งหลักเมื่อมีการจัดส่งมากกว่าหนึ่งรายการในการบรรทุก** เป็น **ใช่** ในหน้า **พารามิเตอร์การจัดการขนส่ง** ใบตราส่งหลักจะสร้างขึ้นโดยอัตโนมัติถ้าคุณสร้างใบตราส่งจาก **เวิร์กเบนช์การวางแผนการบรรทุก**และมีการจัดส่งมากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="a5c88-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="a5c88-117">นอกจากนี้คุณยังสามารถดูรายการของใบตราส่งได้โดยคลิกที่ **ข้อมูลที่เกี่ยวข้อง** &gt; **ใบตราส่ง**</span><span class="sxs-lookup"><span data-stu-id="a5c88-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="a5c88-118">ถ้าคุณกำลังสร้างใบตราส่งด้วยตนเอง คุณสามารถสร้างใบตราส่งหลักได้ที่หน้า **ใบตราส่ง**</span><span class="sxs-lookup"><span data-stu-id="a5c88-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>




