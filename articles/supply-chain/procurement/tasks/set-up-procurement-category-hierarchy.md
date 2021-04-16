---
title: ตั้งค่าประเภทการจัดซื้อตามลำดับชั้น
description: 'ขั้นตอนนี้แสดงวิธีการสร้างโหนดใหม่ในลำดับชั้นประเภทการจัดซื้อและวิธีการตั้งค่าประเภทการจัดซื้อที่จะใช้ในกระบวนการจัดซื้อ '
author: kamaybac
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 206dd5dc8f332268fe7665d84b005b5a7bfd1f9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837716"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="c2a5a-103">ตั้งค่าประเภทการจัดซื้อตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="c2a5a-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2a5a-104">ขั้นตอนนี้แสดงวิธีการสร้างโหนดใหม่ในลำดับชั้นประเภทการจัดซื้อและวิธีการตั้งค่าประเภทการจัดซื้อที่จะใช้ในกระบวนการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="c2a5a-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="c2a5a-105">โดยทั่วไป งานเหล่านี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c2a5a-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="c2a5a-106">ก่อนที่คุณจะสามารถเริ่มขั้นตอนนี้ ต้องมีประเภทตามลำดับชั้นของชนิดการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c2a5a-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="c2a5a-107">ถ้าคุณกำลังใช้ข้อมูลบริษัทสาธิต คุณสามารถเรียกใช้ขั้นตอนนี้ในบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="c2a5a-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="c2a5a-108">เพิ่มประเภทการจัดซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="c2a5a-108">Add a new procurement category</span></span>
1. <span data-ttu-id="c2a5a-109">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดซื้อและการจัดหา > การส่งมอบ > แค็ตตาล็อกการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="c2a5a-110">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="c2a5a-111">ลำดับชั้นประเภทการจัดซื้อปัจจุบันจะแสดงอยู่ทางด้านซ้ายของหน้า </span><span class="sxs-lookup"><span data-stu-id="c2a5a-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="c2a5a-112">คุณกำลังจะปรับเปลี่ยนลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="c2a5a-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="c2a5a-113">ในบานหน้าต่างการดำเนินการ ให้เลือก **โหนดประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="c2a5a-114">ระบบจะเลือกโหนดบนสุดตามค่าเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="c2a5a-114">The system selects the top node by default.</span></span> <span data-ttu-id="c2a5a-115">ถ้าคุณกำลังรันขั้นตอนนี้เป็นคู่มืองาน คุณสามารถคลิกปุ่มปลดล็อค และเลือกโหนดหลักอื่นเพื่อแทรกโหนดของคุณใหม่ลงไป</span><span class="sxs-lookup"><span data-stu-id="c2a5a-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="c2a5a-116">หลังจากที่เสร็จเรียบร้อย ล็อคคู่มืองานอีกครั้ง จากนั้นคลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="c2a5a-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="c2a5a-117">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2a5a-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c2a5a-118">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2a5a-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="c2a5a-119">ในฟิลด์ **ชื่อที่จำง่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2a5a-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="c2a5a-120">ชื่อที่จำง่ายไม่จำเป็น </span><span class="sxs-lookup"><span data-stu-id="c2a5a-120">The friendly name is optional.</span></span> <span data-ttu-id="c2a5a-121">มันจะปรากฏในประเภทการค้นหาพร้อมด้วยชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="c2a5a-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="c2a5a-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="c2a5a-123">เพิ่มผลิตภัณฑ์ไปยังประเภทการจัดซื้อใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c2a5a-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="c2a5a-124">ไปที่ **การจัดซื้อและการจัดหา > การส่งมอบ > ประเภทการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="c2a5a-125">เลือกโหนดคุณเพิ่งเพิ่มเข้ามา </span><span class="sxs-lookup"><span data-stu-id="c2a5a-125">Select the node you just added.</span></span> <span data-ttu-id="c2a5a-126">ถ้าคุณกำลังใช้งานกระบวนงานนี้เป็นคู่มืองาน คุณอาจต้องการปลดล็อคคู่มืองานเพื่อเลือกโหนด</span><span class="sxs-lookup"><span data-stu-id="c2a5a-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="c2a5a-127">เปิด/ปิดการขยายส่วน **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="c2a5a-128">ให้เลือก **เพิ่ม** เพื่อเชื่อมโยงผลิตภัณฑ์กับประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c2a5a-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="c2a5a-129">เลือกผลิตภัณฑ์ที่คุณต้องการเพิ่มในประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c2a5a-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="c2a5a-130">เลือกลูกศรเพื่อเพิ่มผลิตภัณฑ์ไปยังตาราง **ที่เลือกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="c2a5a-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c2a5a-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]