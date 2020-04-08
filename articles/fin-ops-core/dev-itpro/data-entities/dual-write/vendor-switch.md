---
title: สลับการออกแบบของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีสลับการรวมข้อมูลของผู้จัดจำหน่ายระหว่างแอป Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173050"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="2022d-103">สลับการออกแบบของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2022d-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="2022d-104">โฟลว์ข้อมูลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2022d-104">Vendor data flow</span></span> 

<span data-ttu-id="2022d-105">ถ้าคุณเลือกที่จะใช้เอนทิตี้ **บัญชี** เพื่อจัดเก็บผู้จัดจำหน่ายของชนิด **องค์กร** และเอนทิตี้ **ผู้ติดต่อ** เพื่อจัดเก็บผู้จัดจำหน่ายของชนิด **บุคคล** ให้ตั้งค่าคอนฟิกลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2022d-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="2022d-106">มิฉะนั้น ไม่จำเป็นต้องมีการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="2022d-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="2022d-107">ใช้การออกแบบของผู้จัดจำหน่ายแบบขยายสำหรับผู้จัดจำหน่ายชนิดองค์กร</span><span class="sxs-lookup"><span data-stu-id="2022d-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="2022d-108">แพคเกจโซลูชัน **Dynamics365FinanceExtended** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2022d-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="2022d-109">คุณจะสร้างลำดับงานสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="2022d-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="2022d-110">สร้างผู้จัดจำหน่ายในเอนทิตี้บัญชี</span><span class="sxs-lookup"><span data-stu-id="2022d-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="2022d-111">สร้างผู้จัดจำหน่ายในเอนทิตีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2022d-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="2022d-112">ปรับปรุงผู้จัดจำหน่ายในเอนทิตี้บัญชี</span><span class="sxs-lookup"><span data-stu-id="2022d-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="2022d-113">ปรับปรุงผู้จัดจำหน่ายในเอนทิตีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2022d-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="2022d-114">เพื่อสร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2022d-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="2022d-115">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในเอนทิตี้บัญชี**</span><span class="sxs-lookup"><span data-stu-id="2022d-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="2022d-116">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2022d-116">Then select **OK**.</span></span> <span data-ttu-id="2022d-117">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="2022d-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![สร้างผู้จัดจำหน่ายในกระบวนการลำดับงานเอนทิตี้บัญชี](media/create_process.png)

2. <span data-ttu-id="2022d-119">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **ปรับปรุงผู้จัดจำหน่ายในเอนทิตี้บัญชี**</span><span class="sxs-lookup"><span data-stu-id="2022d-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="2022d-120">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2022d-120">Then select **OK**.</span></span> <span data-ttu-id="2022d-121">ลำดับงานนี้จะจัดการสถานการณ์จำลองการอัปเดตผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="2022d-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="2022d-122">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **บัญชี** และเลือกเท็มเพลตกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในเอนทิตี้ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="2022d-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="2022d-123">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **บัญชี** และเลือกเท็มเพลตกระบวนการลำดับงาน **ปรับปรุงผู้จัดจำหน่ายในเอนทิตี้ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="2022d-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="2022d-124">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์ หรือลำดับงานพื้นหลัง อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="2022d-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="2022d-125">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานพื้นหลัง เลือก **แปลงเป็นลำดับงานพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="2022d-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![ปุ่มแปลงเป็นลำดับงานพื้นหลัง](media/background_workflow.png)

6. <span data-ttu-id="2022d-127">เปิดใช้ลำดับงานที่คุณสร้างขึ้นสำหรับเอนทิตี้ **บัญชี** และ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานเอนทิตี้ **บัญชี** เพื่อจัดเก็บข้อมูลสำหรับผู้จัดจำหน่ายของชนิด **องค์กร**</span><span class="sxs-lookup"><span data-stu-id="2022d-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="2022d-128">ใช้การออกแบบของผู้จัดจำหน่ายแบบขยายสำหรับผู้จัดจำหน่ายชนิดบุคคล</span><span class="sxs-lookup"><span data-stu-id="2022d-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="2022d-129">แพคเกจโซลูชัน **Dynamics365FinanceExtended** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2022d-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="2022d-130">คุณจะสร้างลำดับงานสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="2022d-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="2022d-131">สร้างผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2022d-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="2022d-132">สร้างผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2022d-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="2022d-133">ปรับปรุงผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2022d-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="2022d-134">ปรับปรุงผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2022d-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="2022d-135">เพื่อสร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2022d-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="2022d-136">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="2022d-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="2022d-137">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2022d-137">Then select **OK**.</span></span> <span data-ttu-id="2022d-138">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่ายสำหรับเอนทิตี **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="2022d-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="2022d-139">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **ปรับปรุงผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="2022d-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="2022d-140">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2022d-140">Then select **OK**.</span></span> <span data-ttu-id="2022d-141">ลำดับงานนี้จะจัดการสถานการณ์จำลองการปรับปรุงผู้จัดจำหน่ายสำหรับเอนทิตี้ **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="2022d-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="2022d-142">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้ติดต่อ** และเลือกเท็มเพลต **สร้างผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="2022d-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="2022d-143">สร้างกระบวนการลำดับงานสำหรับเอนทิตี้ **ผู้ติดต่อ** และเลือกเท็มเพลต **ปรับปรุงผู้จัดจำหน่ายชนิดบุคคลในเอนทิตี้ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="2022d-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="2022d-144">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์ หรือลำดับงานพื้นหลัง อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="2022d-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="2022d-145">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานพื้นหลัง เลือก **แปลงเป็นลำดับงานพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="2022d-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="2022d-146">เปิดใช้ลำดับงานที่คุณสร้างขึ้นในเอนทิตี้ **ผู้ติดต่อ** และเอนทิตี้ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานเอนทิตี้ **ผู้ติดต่อ** เพื่อจัดเก็บข้อมูลสำหรับผู้จัดจำหน่ายของชนิด **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="2022d-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
