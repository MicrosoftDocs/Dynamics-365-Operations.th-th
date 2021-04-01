---
title: ตั้งค่าประเภทการจัดซื้อตามลำดับชั้น
description: 'ขั้นตอนนี้แสดงวิธีการสร้างโหนดใหม่ในลำดับชั้นประเภทการจัดซื้อและวิธีการตั้งค่าประเภทการจัดซื้อที่จะใช้ในกระบวนการจัดซื้อ '
author: RichardLuan
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44fd02d37ec4e6431ca25dc980ed1d1785e45fac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239361"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="46dd2-103">ตั้งค่าประเภทการจัดซื้อตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="46dd2-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46dd2-104">ขั้นตอนนี้แสดงวิธีการสร้างโหนดใหม่ในลำดับชั้นประเภทการจัดซื้อและวิธีการตั้งค่าประเภทการจัดซื้อที่จะใช้ในกระบวนการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="46dd2-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="46dd2-105">โดยทั่วไป งานเหล่านี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="46dd2-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="46dd2-106">ก่อนที่คุณจะสามารถเริ่มขั้นตอนนี้ ต้องมีประเภทตามลำดับชั้นของชนิดการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="46dd2-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="46dd2-107">ถ้าคุณกำลังใช้ข้อมูลบริษัทสาธิต คุณสามารถเรียกใช้ขั้นตอนนี้ในบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="46dd2-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="46dd2-108">เพิ่มประเภทการจัดซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="46dd2-108">Add a new procurement category</span></span>
1. <span data-ttu-id="46dd2-109">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดซื้อและการจัดหา > การส่งมอบ > แค็ตตาล็อกการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="46dd2-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="46dd2-110">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="46dd2-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="46dd2-111">ลำดับชั้นประเภทการจัดซื้อปัจจุบันจะแสดงอยู่ทางด้านซ้ายของหน้า </span><span class="sxs-lookup"><span data-stu-id="46dd2-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="46dd2-112">คุณกำลังจะปรับเปลี่ยนลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="46dd2-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="46dd2-113">ในบานหน้าต่างการดำเนินการ ให้เลือก **โหนดประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="46dd2-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="46dd2-114">ระบบจะเลือกโหนดบนสุดตามค่าเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="46dd2-114">The system selects the top node by default.</span></span> <span data-ttu-id="46dd2-115">ถ้าคุณกำลังรันขั้นตอนนี้เป็นคู่มืองาน คุณสามารถคลิกปุ่มปลดล็อค และเลือกโหนดหลักอื่นเพื่อแทรกโหนดของคุณใหม่ลงไป</span><span class="sxs-lookup"><span data-stu-id="46dd2-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="46dd2-116">หลังจากที่เสร็จเรียบร้อย ล็อคคู่มืองานอีกครั้ง จากนั้นคลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="46dd2-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="46dd2-117">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="46dd2-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="46dd2-118">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="46dd2-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="46dd2-119">ในฟิลด์ **ชื่อที่จำง่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="46dd2-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="46dd2-120">ชื่อที่จำง่ายไม่จำเป็น </span><span class="sxs-lookup"><span data-stu-id="46dd2-120">The friendly name is optional.</span></span> <span data-ttu-id="46dd2-121">มันจะปรากฏในประเภทการค้นหาพร้อมด้วยชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="46dd2-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="46dd2-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="46dd2-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="46dd2-123">เพิ่มผลิตภัณฑ์ไปยังประเภทการจัดซื้อใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="46dd2-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="46dd2-124">ไปที่ **การจัดซื้อและการจัดหา > การส่งมอบ > ประเภทการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="46dd2-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="46dd2-125">เลือกโหนดคุณเพิ่งเพิ่มเข้ามา </span><span class="sxs-lookup"><span data-stu-id="46dd2-125">Select the node you just added.</span></span> <span data-ttu-id="46dd2-126">ถ้าคุณกำลังใช้งานกระบวนงานนี้เป็นคู่มืองาน คุณอาจต้องการปลดล็อคคู่มืองานเพื่อเลือกโหนด</span><span class="sxs-lookup"><span data-stu-id="46dd2-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="46dd2-127">เปิด/ปิดการขยายส่วน **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="46dd2-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="46dd2-128">ให้เลือก **เพิ่ม** เพื่อเชื่อมโยงผลิตภัณฑ์กับประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="46dd2-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="46dd2-129">เลือกผลิตภัณฑ์ที่คุณต้องการเพิ่มในประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="46dd2-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="46dd2-130">เลือกลูกศรเพื่อเพิ่มผลิตภัณฑ์ไปยังตาราง **ที่เลือกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="46dd2-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="46dd2-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="46dd2-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]