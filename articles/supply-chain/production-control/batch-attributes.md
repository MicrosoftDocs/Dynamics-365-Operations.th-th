---
title: แอททริบิวต์ของชุดงาน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับแอททริบิวต์ของชุดงาน แอททริบิวต์ของชุดงานมีลักษณะของวัตถุดิบและผลิตภัณฑ์สำเร็จรูปที่สร้างชุดงานสินค้าคงคลัง หัวข้อนี้ยังอธิบายวิธีการกำหนดแอททริบิวต์ของชุดงาน และวิธีที่คุณสามารถค้นหาเมื่อคุณจองชุดงานอีกด้วย
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 325e647185e3eb4c0eacdfd00c320804e31ddb48
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555896"
---
# <a name="batch-attributes"></a><span data-ttu-id="b53e3-105">แอททริบิวต์ของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b53e3-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b53e3-106">หัวข้อนี้แสดงข้อมูลเกี่ยวกับแอททริบิวต์ของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b53e3-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="b53e3-107">แอททริบิวต์ของชุดงานมีลักษณะของวัตถุดิบและผลิตภัณฑ์สำเร็จรูปที่สร้างชุดงานสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b53e3-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="b53e3-108">หัวข้อนี้ยังอธิบายวิธีการกำหนดแอททริบิวต์ของชุดงาน และวิธีที่คุณสามารถค้นหาเมื่อคุณจองชุดงานอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="b53e3-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="b53e3-109">แอททริบิวต์ของชุดงานมีลักษณะของวัตถุดิบและผลิตภัณฑ์สำเร็จรูปที่สร้างชุดงานสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b53e3-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="b53e3-110">แอททริบิวต์ของชุดงานอาจแตกต่างกัน ขึ้นอยู่กับปัจจัยต่าง ๆ เช่นสภาพแวดล้อม คุณภาพของวัตถุดิบที่ใช้ในการผลิตชุดงาน หรือผลลัพธ์ของผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="b53e3-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="b53e3-111">จำนวนและชนิดของแอททริบิวต์ของชุดงานที่ใช้อาจแตกต่างจากอุตสาหกรรมหนึ่งไปยังอีกอุตสาหกรรมหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b53e3-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="b53e3-112">นี่คือสองตัวอย่างที่แสดงวิธีการใช้แอททริบิวต์ของชุดงาน:</span><span class="sxs-lookup"><span data-stu-id="b53e3-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="b53e3-113">ในอุตสาหกรรมเนย ผลิตภัณฑ์นม ซึ่งเป็นหนึ่งในวัตถุดิบที่ใช้ในการผลิตเนย สามารถมีแอททริบิวต์ เช่น ปริมาณไขมันและเปอร์เซ็นต์น้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="b53e3-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="b53e3-114">เนยที่ผลิตจากผลิตภัณฑ์นมสามารถมีแอททริบิวต์อื่น ๆ เช่น ความชื้นและอายุ</span><span class="sxs-lookup"><span data-stu-id="b53e3-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="b53e3-115">ในอุตสาหกรรมเหล็ก เหล็กที่ผลิตอาจมีแอททริบิวต์ เช่น เปอร์เซ็นต์ของปริมาณแมกนีเซียม ปริมาณเงิน และปริมาณสังกะสี</span><span class="sxs-lookup"><span data-stu-id="b53e3-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="b53e3-116">เพื่อจัดการหมายเลขและชนิดของแอททริบิวต์ที่ดียิ่งขึ้น คุณสามารถใช้กลุ่มแอททริบิวต์ของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b53e3-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="b53e3-117">ด้วยวิธีนี้ คุณไม่ได้เพิ่มแอททริบิวต์ทีละรายการ</span><span class="sxs-lookup"><span data-stu-id="b53e3-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="b53e3-118">มอบหมายแอททริบิวต์ของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b53e3-118">Assign batch attributes</span></span>
<span data-ttu-id="b53e3-119">คุณสามารถกำหนดแอททริบิวต์ของชุดงานไปยังผลิตภัณฑ์แต่ละรายการที่ถูกระงับในชุดงานสินค้าคงคลัง หรือคุณสามารถกำหนดแอททริบิวต์ให้กับผลิตภัณฑ์ที่เชื่อมโยงกับลูกค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b53e3-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="b53e3-120">ก่อนที่คุณสามารถกำหนดแอททริบิวต์ของชุดงานในระดับลูกค้า คุณต้องกำหนดชุดแอทริบิวต์ที่ระดับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b53e3-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="b53e3-121">ผลิตภัณฑ์ต้องมีมิติชุดงานตั้งค่าเป็น **ใช้งานอยู่** ในกลุ่มมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="b53e3-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="b53e3-122">เพื่อกำหนดแอททริบิวต์ของชุดงานให้กับผลิตภัณฑ์แต่ละรายการ ใช้หน้าผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b53e3-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="b53e3-123">หากแอททริบิวต์เป็นเฉพาะกับผลิตภัณฑ์สำหรับลูกค้า ใช้หน้าลูกค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b53e3-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="b53e3-124">เมื่อคุณเพิ่มแอททริบิวต์ไปที่ผลิตภัณฑ์ คุณกำหนดพารามิเตอร์อื่น ๆด้วย</span><span class="sxs-lookup"><span data-stu-id="b53e3-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="b53e3-125">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="b53e3-125">Here are some examples:</span></span>

-   <span data-ttu-id="b53e3-126">ช่วงต่ำสุดและสูงสุดสำหรับแอททริบิวต์ของชนิด **จำนวนเต็ม** หรือ **เศษส่วน**</span><span class="sxs-lookup"><span data-stu-id="b53e3-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="b53e3-127">การดำเนินการยอมรับสำหรับแอททริบิวต์ของชนิด **จำนวนเต็ม** หรือ **เศษส่วน**</span><span class="sxs-lookup"><span data-stu-id="b53e3-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="b53e3-128">ถ้าค่าของแอตทริบิวต์อยู่นอกช่วงค่าต่ำสุดและสูงสุด การดำเนินการสามารถมีข้อความเตือนหรือข้อผิดพลาดอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b53e3-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="b53e3-129">ค่าเป้าหมายสำหรับแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="b53e3-129">The target value for the attribute.</span></span> <span data-ttu-id="b53e3-130">ค่านี้เป็นค่าที่เหมาะสมของแอททริบิวต์ และใช้กับชนิดของแอททริบิวต์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b53e3-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="b53e3-131">คุณสามารถเข้าถึงหน้าสำหรับผลิตภัณฑ์ที่คุณเลือกในหน้า **ผลิตภัณฑ์ที่นำออกใช้** ในการจัดการข้อมูลผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="b53e3-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="b53e3-132">หลังจากที่คุณกำหนดแอททริบิวต์ของชุดงานไปยังผลิตภัณฑ์ คุณสามารถเพิ่มค่าเฉพาะไปยังแอททริบิวต์ในหน้า **แอททริบิวต์ชุดงานของสินค้าคงคลัง** ได้</span><span class="sxs-lookup"><span data-stu-id="b53e3-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="b53e3-133">จองชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b53e3-133">Reserve batches</span></span>
<span data-ttu-id="b53e3-134">คุณสามารถค้นหาแอททริบิวต์ของชุดงาน เมื่อคุณทำการจองชุดงานสำหรับใบสั่งขายเพื่อเติมเต็มใบสั่งของลูกค้า หรือเมื่อคุณเบิกสินค้าและจองชุดงานสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="b53e3-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="b53e3-135">การค้นหาช่วยระบุตำแหน่งชุดงานสินค้าคงคลัง ที่ประกอบด้วยผลิตภัณฑ์ที่มีแอททริบิวต์ของชุดงานที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="b53e3-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="b53e3-136">หลังจากที่คุณระบุตำแหน่งชุดงานหรือชุดงานต่างๆ คุณสามารถจองผลิตภัณฑ์ไปยังรายการธุรกรรมสินค้าคงคลังเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b53e3-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>



