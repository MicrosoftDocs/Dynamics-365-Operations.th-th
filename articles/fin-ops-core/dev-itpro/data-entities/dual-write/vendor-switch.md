---
title: สลับการออกแบบของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีสลับการรวมข้อมูลของผู้จัดจำหน่ายระหว่างแอป Finance and Operations และ Dataverse
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 78d4c547f544d95c66490e5610374a5c4598b266
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565610"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="8f6f9-103">สลับการออกแบบของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8f6f9-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="8f6f9-104">โฟลว์ข้อมูลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8f6f9-104">Vendor data flow</span></span> 

<span data-ttu-id="8f6f9-105">ถ้าคุณเลือกที่จะใช้ตาราง **บัญชี** เพื่อจัดเก็บผู้จัดจำหน่ายของชนิด **องค์กร** และตาราง **ผู้ติดต่อ** เพื่อจัดเก็บผู้จัดจำหน่ายของชนิด **บุคคล** ให้ตั้งค่าคอนฟิกลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8f6f9-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="8f6f9-106">มิฉะนั้น ไม่จำเป็นต้องมีการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="8f6f9-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="8f6f9-107">ใช้การออกแบบของผู้จัดจำหน่ายแบบขยายสำหรับผู้จัดจำหน่ายชนิดองค์กร</span><span class="sxs-lookup"><span data-stu-id="8f6f9-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="8f6f9-108">แพคเกจโซลูชัน **Dynamics365FinanceExtended** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8f6f9-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="8f6f9-109">คุณจะสร้างลำดับงานสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8f6f9-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="8f6f9-110">สร้างผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="8f6f9-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="8f6f9-111">สร้างผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8f6f9-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="8f6f9-112">อัปเดตผู้จัดจำหน่ายในตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="8f6f9-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="8f6f9-113">อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8f6f9-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="8f6f9-114">เพื่อสร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8f6f9-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="8f6f9-115">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้จัดจำหน่าย** และเลือกแม่แบบกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในตารางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="8f6f9-116">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-116">Then select **OK**.</span></span> <span data-ttu-id="8f6f9-117">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่าย สำหรับตาราง **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![สร้างผู้จัดจำหน่ายในกระบวนการลำดับงานตารางบัญชี](media/create_process.png)

2. <span data-ttu-id="8f6f9-119">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้จัดจำหน่าย** และเลือกแม่แบบกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในตารางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="8f6f9-120">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-120">Then select **OK**.</span></span> <span data-ttu-id="8f6f9-121">ลำดับงานนี้จะจัดการสถานการณ์จำลองการอัปเดตผู้จัดจำหน่าย สำหรับตาราง **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="8f6f9-122">สร้างกระบวนการลำดับงานสำหรับตาราง **บัญชี** และเลือกแม่แบบกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="8f6f9-123">สร้างกระบวนการลำดับงานสำหรับตาราง **บัญชี** และเลือกแม่แบบกระบวนการลำดับงาน **อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="8f6f9-124">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์ หรือลำดับงานพื้นหลัง อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="8f6f9-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="8f6f9-125">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานพื้นหลัง เลือก **แปลงเป็นลำดับงานพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![ปุ่มแปลงเป็นลำดับงานพื้นหลัง](media/background_workflow.png)

6. <span data-ttu-id="8f6f9-127">เปิดใช้ลำดับงานที่คุณสร้างขึ้นสำหรับตาราง **บัญชี** และ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานตาราง **บัญชี** เพื่อจัดเก็บข้อมูลสำหรับผู้จัดจำหน่ายของชนิด **องค์กร**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="8f6f9-128">ใช้การออกแบบของผู้จัดจำหน่ายแบบขยายสำหรับผู้จัดจำหน่ายชนิดบุคคล</span><span class="sxs-lookup"><span data-stu-id="8f6f9-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="8f6f9-129">แพคเกจโซลูชัน **Dynamics365FinanceExtended** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8f6f9-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="8f6f9-130">คุณจะสร้างลำดับงานสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8f6f9-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="8f6f9-131">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8f6f9-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="8f6f9-132">สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="8f6f9-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="8f6f9-133">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="8f6f9-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="8f6f9-134">อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8f6f9-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="8f6f9-135">เพื่อสร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8f6f9-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="8f6f9-136">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้จัดจำหน่าย** และเลือกเท็มเพลตกระบวนการลำดับงาน **สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="8f6f9-137">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-137">Then select **OK**.</span></span> <span data-ttu-id="8f6f9-138">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่ายสำหรับตาราง **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="8f6f9-139">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้จัดจำหน่าย** และเลือกแม่แบบกระบวนการลำดับงาน **อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="8f6f9-140">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-140">Then select **OK**.</span></span> <span data-ttu-id="8f6f9-141">ลำดับงานนี้จะจัดการสถานการณ์จำลองการปรับปรุงผู้จัดจำหน่ายสำหรับตาราง **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="8f6f9-142">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้ติดต่อ** และเลือกแม่แบบ **สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="8f6f9-143">สร้างกระบวนการลำดับงานสำหรับตาราง **ผู้ติดต่อ** และเลือกแม่แบบ **อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="8f6f9-144">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์ หรือลำดับงานพื้นหลัง อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="8f6f9-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="8f6f9-145">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานพื้นหลัง เลือก **แปลงเป็นลำดับงานพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="8f6f9-146">เปิดใช้ลำดับงานที่คุณสร้างขึ้นในเอนทิตี **ผู้ติดต่อ** และเอนทิตี **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานตาราง **ผู้ติดต่อ** เพื่อจัดเก็บข้อมูลสำหรับผู้จัดจำหน่ายของชนิด **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="8f6f9-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]