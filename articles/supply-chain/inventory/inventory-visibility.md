---
title: Add-in การมองเห็นสินค้าคงคลัง
description: หัวข้อนี้จะอธิบายวิธีการติดตั้งและตั้งค่าคอนฟิกAdd-in การมองเห็นสินค้าคงคลังสำหรับ Dynamics 365 Supply Chain Management
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625076"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="8e405-103">Add-in การมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8e405-104">Add-in การมองเห็นสินค้าคงคลังเป็น microservice อิสระและปรับสเกลได้อย่างมาก ซึ่งเปิดใช้งานการติดตามปริมาณคงคลังคงเหลือในเวลาจริง จึงให้มุมมองส่วนกลางของการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="8e405-105">ข้อมูลทั้งหมดที่เกี่ยวข้องกับปริมาณคงคลังคงเหลือจะถูกส่งออกไปยังบริการใกล้เคียงเวลาจริงผ่านการรวม SQL ในระดับต่ำ</span><span class="sxs-lookup"><span data-stu-id="8e405-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="8e405-106">ระบบภายนอกเข้าถึงบริการผ่าน RESTful APIs เพื่อสอบถามข้อมูลปริมาณคงคลังคงเหลือในชุดของมิติที่กำหนด ดังนั้นจึงดึงข้อมูลรายการของตำแหน่งในปริมาณคงคลังคงเหลือที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8e405-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="8e405-107">ความสามารถในการมองเห็นสินค้าคงคลังเป็น microservice ที่สร้างขึ้นบน Common Data Service ซึ่งหมายความว่า คุณสามารถขยายได้โดยการสร้าง Power Apps และการใช้ Power BI เพื่อให้ฟังก์ชันการทำงานที่กำหนดเองตรงกับความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="8e405-108">นอกจากนี้ คุณยังสามารถอัปเกรดดัชนีเพื่อทำการสอบถามสินค้าคงคลังได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8e405-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="8e405-109">ความสามารถในการมองเห็นสินค้าคงคลังจะให้ตัวเลือกการตั้งค่าคอนฟิกซึ่งช่วยให้สามารถรวมกับระบบต่างๆ ของบุคคลที่สามได้</span><span class="sxs-lookup"><span data-stu-id="8e405-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="8e405-110">ซึ่งสนับสนุนมิติสินค้าคงคลังมาตรฐาน ความสามารถที่กำหนดเอง และปริมาณที่มีการคำนวณซึ่งสามารถตั้งค่าคอนฟิกได้แบบมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="8e405-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="8e405-111">หัวข้อนี้จะอธิบายวิธีการติดตั้งและตั้งค่าคอนฟิก Add-in ความสามารถในการมองเห็นสินค้าคงคลังสำหรับ Dynamics 365 Supply Chain Management และวิธีใช้ Application Programming Interface (API)</span><span class="sxs-lookup"><span data-stu-id="8e405-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="8e405-112">ติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="8e405-113">คุณจำเป็นต้องติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลังโดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8e405-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8e405-114">LCS เป็นพอร์ทัลการทำงานร่วมกันที่ให้สภาพแวดล้อมและชุดของบริการที่อัปเดตเป็นประจำ ซึ่งช่วยให้คุณสามารถจัดการวงจรการใช้งานแอปพลิเคชันของแอป Dynamics 365 Finance and Operations ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8e405-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="8e405-115">สำหรับข้อมูลเพิ่มเติม ให้ดู [ทรัพยากร Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs)</span><span class="sxs-lookup"><span data-stu-id="8e405-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8e405-116">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8e405-116">Prerequisites</span></span>

<span data-ttu-id="8e405-117">ก่อนที่คุณจะสามารถติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง คุณต้องดำเนินการขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e405-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="8e405-118">รับโครงการสำหรับการใช้งาน LCS โดยมีสภาพแวดล้อมที่ปรับใช้อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="8e405-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="8e405-119">สร้างคีย์เบต้าสำหรับข้อเสนอของคุณใน LCS</span><span class="sxs-lookup"><span data-stu-id="8e405-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="8e405-120">เปิดใช้งานคีย์เบต้าสำหรับข้อเสนอของคุณสำหรับผู้ใช้ของคุณใน LCS</span><span class="sxs-lookup"><span data-stu-id="8e405-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="8e405-121">ติดต่อทีมงานผลิตภัณฑ์ Microsoft Inventory Visibility และระบุรหัสสภาพแวดล้อมที่ซึ่งคุณต้องการปรับใช้ Add-in ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="8e405-122">ถ้าคุณมีคำถามใดๆ เกี่ยวกับข้อกำหนดเบื้องต้นเหล่านี้ โปรดติดต่อทีมงานผลิตภัณฑ์ของความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="8e405-123">ติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="8e405-123">Install the add-in</span></span>

<span data-ttu-id="8e405-124">เพื่อติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง ต้องดำเนินการขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e405-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="8e405-125">ลงชื่อเข้าใช้พอร์ทัล [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)</span><span class="sxs-lookup"><span data-stu-id="8e405-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="8e405-126">บนโฮมเพจ ให้เลือกโครงการที่มีการปรับใช้สภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="8e405-127">บนหน้าโครงการ ให้เลือกสภาพแวดล้อมที่คุณต้องการติดตั้ง add-in</span><span class="sxs-lookup"><span data-stu-id="8e405-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="8e405-128">บนหน้าสภาพแวดล้อม ให้เลื่อนลงจนกว่าคุณจะเห็นส่วน **add-in สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="8e405-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="8e405-129">ถ้าไม่สามารถมองเห็นส่วนนี้ได้ โปรดตรวจสอบให้แน่ใจว่าได้ประมวลผลคีย์รุ่นเบต้าของข้อกำหนดเบื้องต้นเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="8e405-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="8e405-130">ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e405-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="8e405-131">![หน้าสภาพแวดล้อมใน LCS](media/inventory-visibility-environment.png "หน้าสภาพแวดล้อมใน LCS")</span><span class="sxs-lookup"><span data-stu-id="8e405-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="8e405-132">เลือกลิงก์ **ติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e405-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="8e405-133">รายการของ add-in ที่พร้อมใช้งานจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="8e405-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="8e405-134">เลือก **บริการสินค้าคงคลัง** จากรายการ</span><span class="sxs-lookup"><span data-stu-id="8e405-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="8e405-135">(หมายเหตุ ในขณะนี้อาจแสดงรายการเป็น **Add-in ความสามารถในการมองเห็นสินค้าคงคลังสำหรับ Dynamics 365 Supply Chain Management**)</span><span class="sxs-lookup"><span data-stu-id="8e405-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="8e405-136">ป้อนค่าสำหรับฟิลด์ต่อไปนี้สำหรับสภาพแวดล้อมของคุณ:</span><span class="sxs-lookup"><span data-stu-id="8e405-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="8e405-137">**รหัสแอปพลิเคชัน AAD**</span><span class="sxs-lookup"><span data-stu-id="8e405-137">**AAD application ID**</span></span>
    - <span data-ttu-id="8e405-138">**รหัสผู้เช่า AAD**</span><span class="sxs-lookup"><span data-stu-id="8e405-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="8e405-139">![หน้าการตั้งค่าของ Add in](media/inventory-visibility-setup.png "หน้าการตั้งค่าของ Add in")</span><span class="sxs-lookup"><span data-stu-id="8e405-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="8e405-140">ยอมรับข้อกำหนดและเงื่อนไขโดยเลือกกล่องกาเครื่องหมาย **ข้อกำหนดและเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="8e405-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="8e405-141">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="8e405-141">Select **Install**.</span></span> <span data-ttu-id="8e405-142">สถานะของ add-in จะแสดงเป็น **กำลังติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="8e405-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="8e405-143">เมื่อเสร็จสิ้นแล้ว ให้รีเฟรชหน้าเพื่อดูการเปลี่ยนแปลงสถานะเป็น **ติดตั้งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="8e405-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="8e405-144">เรียกใช้โทเคนบริการรักษาความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="8e405-144">Get a security service token</span></span>

<span data-ttu-id="8e405-145">เมื่อต้องการเรียกใช้โทเคนบริการรักษาความปลอดภัย ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e405-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="8e405-146">เรียกใช้ `aadToken` ของคุณ และเรียกปลายทาง: https://securityservice.operations365.dynamics.com/token</span><span class="sxs-lookup"><span data-stu-id="8e405-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="8e405-147">แทนที่ `client_assertion` ในเนื้อหาด้วย `aadToken` ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="8e405-148">แทนที่บริบทในเนื้อหาด้วยสภาพแวดล้อมที่คุณต้องการปรับใช้ add-in</span><span class="sxs-lookup"><span data-stu-id="8e405-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="8e405-149">แทนที่ขอบเขตในเนื้อหาด้วยข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e405-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="8e405-150">ขอบเขตสำหรับ MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span><span class="sxs-lookup"><span data-stu-id="8e405-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="8e405-151">(คุณสามารถค้นหารหัสแอปพลิเคชัน Azure Active Directory และรหัสผู้เช่าสำหรับ MCK ใน `appsettings.mck.json`)</span><span class="sxs-lookup"><span data-stu-id="8e405-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="8e405-152">ขอบเขตสำหรับ PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span><span class="sxs-lookup"><span data-stu-id="8e405-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="8e405-153">(คุณสามารถค้นหารหัสแอปพลิเคชัน Azure Active Directory และรหัสผู้เช่าสำหรับ PROD ใน `appsettings.prod.json`)</span><span class="sxs-lookup"><span data-stu-id="8e405-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="8e405-154">ผลลัพธ์ควรมีลักษณะคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e405-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="8e405-155">คุณจะได้รับ `access_token` ในการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="8e405-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="8e405-156">นี่คือสิ่งที่คุณต้องการในฐานะโทเคนผู้ถือสิทธิ์เพื่อเรียก API ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="8e405-157">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8e405-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="8e405-158">ถอนการติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="8e405-158">Uninstall the add-in</span></span>

<span data-ttu-id="8e405-159">เมื่อต้องการถอนการติดตั้ง add-in ให้เลือก **ถอนการติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="8e405-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="8e405-160">รีเฟรช LCS และ Add-in ความสามารถในการมองเห็นสินค้าคงคลังจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="8e405-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="8e405-161">กระบวนการถอนการติดตั้งจะลบการลงทะเบียน add-in และยังเริ่มต้นงานเพื่อล้างข้อมูลทางธุรกิจทั้งหมดที่จัดเก็บไว้ในบริการด้วย</span><span class="sxs-lookup"><span data-stu-id="8e405-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="8e405-162">API สาธารณะของ Add-in ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="8e405-163">REST API สาธารณะของ Add-in ความสามารถในการมองเห็นสินค้าคงคลัง แสดงถึงปลายทางเฉพาะของการรวมหลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="8e405-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="8e405-164">ซึ่งสนับสนุนชนิดการโต้ตอบหลักสามชนิด:</span><span class="sxs-lookup"><span data-stu-id="8e405-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="8e405-165">การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปที่ add-in จากระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="8e405-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="8e405-166">การสอบถามปริมาณคงคลังคงเหลือปัจจุบันจากระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="8e405-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="8e405-167">การซิงโครไนส์อัตโนมัติกับ Supply Chain Management คงเหลือ</span><span class="sxs-lookup"><span data-stu-id="8e405-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="8e405-168">การซิงโครไนส์อัตโนมัติไม่ได้เป็นส่วนหนึ่งของ API สาธารณะ แต่จะถูกจัดการในพื้นหลังสำหรับสภาพแวดล้อมที่มีการเปิดใช้งาน Add-in ความสามารถในการมองเห็นสินค้าคงคลังแทน</span><span class="sxs-lookup"><span data-stu-id="8e405-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="8e405-169">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8e405-169">Authentication</span></span>

<span data-ttu-id="8e405-170">โทเคนความปลอดภัยของแพลตฟอร์มจะถูกใช้เพื่อเรียก Add-in ความสามารถในการมองเห็นสินค้าคงคลัง ดังนั้นคุณต้องสร้างโทเคน Azure Active Directory โดยใช้แอปพลิเคชัน Azure Active Directory ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="8e405-171">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเรียกใช้โทเคนความปลอดภัย ให้ดูที่ [ติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง](#install-add-in)</span><span class="sxs-lookup"><span data-stu-id="8e405-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="8e405-172">ตั้งค่าคอนฟิก API ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="8e405-173">ก่อนที่จะใช้บริการ คุณต้องทำการตั้งค่าคอนฟิกที่อธิบายไว้ในส่วนย่อยต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8e405-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="8e405-174">การตั้งค่าคอนฟิกอาจแตกต่างกันไปตามรายละเอียดของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="8e405-175">ส่วนใหญ่แล้วประกอบด้วยสี่ส่วน:</span><span class="sxs-lookup"><span data-stu-id="8e405-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="8e405-176">การแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="8e405-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="8e405-177">การตั้งค่าคอนฟิกมิติ</span><span class="sxs-lookup"><span data-stu-id="8e405-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="8e405-178">การจัดทำดัชนี</span><span class="sxs-lookup"><span data-stu-id="8e405-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="8e405-179">การวัดแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8e405-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="8e405-180">การแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="8e405-180">Partitioning</span></span>

<span data-ttu-id="8e405-181">การแบ่งพาร์ติชันสามารถมีผลกระทบต่อประสิทธิภาพการทำงานของ API ความสามารถในการมองเห็นสินค้าคงคลังได้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="8e405-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="8e405-182">ขอแนะนำให้คุณกำหนดโครงร่างที่อนุญาตให้มีการจัดกลุ่มข้อมูลเล็กๆ ในขณะที่ยังคงอนุญาตให้มีการสอบถามข้อมูลที่มีความหมาย</span><span class="sxs-lookup"><span data-stu-id="8e405-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="8e405-183">`organizationId` (`dataAreaId` ใน Supply Chain Management) จะเป็นส่วนหนึ่งของการแบ่งพาร์ติชันเสมอ และตามค่าเริ่มต้น ความสามารถในการมองเห็นสินค้าคงคลังจะถูกตั้งค่าเป็นพาร์ติชันตามมิติเป็น *ไซต์ + สถานที่*</span><span class="sxs-lookup"><span data-stu-id="8e405-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="8e405-184">นี่หมายความว่าบริการต้องมีการสอบถามเสมอด้วยมิติเหล่านี้ที่กำหนดไว้ในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8e405-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="8e405-185">*ไซต์* และ *สถานที่* เป็นมิติเริ่มต้นทั่วไปสองมิติในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="8e405-186">ใน Supply Chain Management มิติเหล่านี้เรียกว่า *ไซต์* (`InventSiteId`) และ *คลังสินค้า* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="8e405-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="8e405-187">การตั้งค่าคอนฟิกมิติ</span><span class="sxs-lookup"><span data-stu-id="8e405-187">Dimension configurations</span></span>

<span data-ttu-id="8e405-188">ความสามารถในการมองเห็นสินค้าคงคลังจะแสดงรายการของมิติเริ่มต้นทั่วไป เพื่อเปิดใช้งานการรวมระบบแหล่งที่มาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="8e405-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="8e405-189">ตารางต่อไปนี้แสดงรายการมิติสินค้าคงคลังที่จะเป็นชื่อมิติเริ่มต้นในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="8e405-190">ชนิดมิติ</span><span class="sxs-lookup"><span data-stu-id="8e405-190">Dimension type</span></span> | <span data-ttu-id="8e405-191">ชื่อมิติ</span><span class="sxs-lookup"><span data-stu-id="8e405-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="8e405-192">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8e405-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="8e405-193">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8e405-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="8e405-194">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8e405-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="8e405-195">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8e405-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="8e405-196">การติดตาม</span><span class="sxs-lookup"><span data-stu-id="8e405-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="8e405-197">การติดตาม</span><span class="sxs-lookup"><span data-stu-id="8e405-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="8e405-198">ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="8e405-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="8e405-199">ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="8e405-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="8e405-200">สถานะของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="8e405-201">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8e405-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="8e405-202">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8e405-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="8e405-203">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8e405-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="8e405-204">ชนิดของมิติที่แสดงรายการอยู่ในตารางก่อนหน้านี้ใช้สำหรับการอ้างอิงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8e405-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="8e405-205">คุณไม่จำเป็นต้องกำหนดชนิดมิติในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="8e405-206">ถ้ามีมิติที่กำหนดเองอยู่และจำเป็นต้องโฟลว์ไปยังค่าเริ่มต้น เมื่อมีการใช้งานโดยความสามารถในการมองเห็นสินค้าคงคลัง คุณสามารถตั้งค่าคอนฟิก **ชื่อมิติที่กำหนดเอง** ในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="8e405-207">ระบบภายนอกเข้าถึงความสามารถในการมองเห็นสินค้าคงคลังผ่าน RESTful APIs ที่เปิดใช้งานข้อมูลปริมาณคงคลังคงเหลือในชุดที่กำหนดของมิติที่จะมีการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="8e405-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="8e405-208">สำหรับการรวม ความสามารถในการมองเห็นสินค้าคงคลังจะช่วยให้คุณสามารถตั้งค่าคอนฟิก *แหล่งข้อมูลช่องทางภายนอก* และมิติแหล่งที่มาเป็น *มิติเป้าหมาย* ในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="8e405-209">มิติเป้าหมายควรเป็นหนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e405-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="8e405-210">มิติเริ่มต้นในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="8e405-211">มิติที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8e405-211">Custom dimensions</span></span>

<span data-ttu-id="8e405-212">วัตถุประสงค์ของการตั้งค่าคอนฟิกมิติคือ การกำหนดมาตรฐานการรวมหลายระบบสำหรับการสอบถามบนมิติและเหตุการณ์การโพสต์กับมิติ</span><span class="sxs-lookup"><span data-stu-id="8e405-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="8e405-213">การจัดทำดัชนี</span><span class="sxs-lookup"><span data-stu-id="8e405-213">Indexing</span></span>

<span data-ttu-id="8e405-214">ส่วนใหญ่การสอบถามปริมาณคงคลังคงเหลือไม่เพียงแค่อยู่ที่ระดับ "ยอดรวม" สูงสุด แต่คุณอาจต้องการดูผลลัพธ์ที่รวมโดยยึดตามมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e405-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="8e405-215">ความสามารถในการมองเห็นสินค้าคงคลังให้ความยืดหยุ่นโดยการอนุญาตให้คุณตั้งค่าดัชนี ซึ่งขึ้นอยู่กับมิติหรือชุดของมิติ</span><span class="sxs-lookup"><span data-stu-id="8e405-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="8e405-216">ในขณะนี้ คุณสามารถตั้งค่าคอนฟิกดัชนีได้สูงสุดห้ารายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8e405-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="8e405-217">คุณต้องคำนึงถึงมิติหรือชุดของมิติที่คุณจะใช้ก่อนที่จะดำเนินการ เพื่อให้มั่นใจว่าจะตอบสนองความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="8e405-218">ตัวอย่างเช่น ถ้าคุณต้องการสอบถามผลิตภัณฑ์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e405-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="8e405-219">สอบถามปริมาณคงคลังคงเหลือของผลิตภัณฑ์แบบรวมตามมิติ *สี* และ *ขนาด*</span><span class="sxs-lookup"><span data-stu-id="8e405-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="8e405-220">ในบางกรณี คุณต้องการสอบถามเกี่ยวกับผลิตภัณฑ์โดยรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8e405-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="8e405-221">คุณจะกำหนดดัชนีสองรายการดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e405-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="8e405-222">วงเล็บที่ว่างเปล่าจะรวมกันตามรหัสผลิตภัณฑ์ภายในการแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="8e405-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="8e405-223">การจัดทำดัชนีจะกำหนดวิธีการที่คุณสามารถจัดกลุ่มผลลัพธ์ของคุณตามการตั้งค่าการสอบถาม `groupBy`</span><span class="sxs-lookup"><span data-stu-id="8e405-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="8e405-224">ในกรณีนี้ ถ้าคุณไม่ได้กำหนดค่า `groupBy` ใดๆ คุณจะได้รับผลรวมตาม `productid`</span><span class="sxs-lookup"><span data-stu-id="8e405-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="8e405-225">มิฉะนั้น ถ้าคุณกำหนด `groupBy` เป็น `groupBy=ColorId&groupBy=SizeId` คุณจะได้รับบรรทัดหลายบรรทัดที่ส่งคืน โดยยึดตามชุดสีและขนาดต่างๆ ในระบบ</span><span class="sxs-lookup"><span data-stu-id="8e405-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="8e405-226">คุณสามารถกำหนดเกณฑ์การสอบถามของคุณในเนื้อหาของคำขอ</span><span class="sxs-lookup"><span data-stu-id="8e405-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="8e405-227">ต่อไปนี้เป็นการสอบถามตัวอย่างเกี่ยวกับผลิตภัณฑ์ที่มีชุดสีและขนาด</span><span class="sxs-lookup"><span data-stu-id="8e405-227">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="8e405-228">การวัดแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8e405-228">Custom measurement</span></span>

<span data-ttu-id="8e405-229">ปริมาณการวัดเริ่มต้นจะเชื่อมโยงกับ Supply Chain Management อย่างไรก็ตาม คุณอาจต้องการมีปริมาณที่ประกอบขึ้นจากชุดของการวัดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8e405-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="8e405-230">เมื่อต้องการดำเนินการนี้ คุณสามารถมีการตั้งค่าคอนฟิกของปริมาณที่กำหนดเอง ซึ่งจะถูกเพิ่มเข้าไปในผลลัพธ์ของการสอบถามปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="8e405-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="8e405-231">ฟังก์ชันนี้จะช่วยให้คุณสามารถกำหนดชุดของการวัดที่จะเพิ่ม และ/หรือชุดของการวัดที่จะถูกลบ เพื่อสร้างการวัดที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8e405-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="8e405-232">ตัวอย่างเช่น ด้วยเงื่อนไขการสอบถามต่อไปนี้ คุณจะตั้งค่าคอนฟิกปริมาณการวัดแบบกำหนดเองเป็น `MyCustomAvailableforReservation` ที่จะใช้โดยระบบปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="8e405-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="8e405-233">ระบบปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="8e405-233">Consumption system</span></span> | <span data-ttu-id="8e405-234">ผู้วัดที่มีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="8e405-234">Calculated measurers</span></span> | <span data-ttu-id="8e405-235">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8e405-235">Data source</span></span> | <span data-ttu-id="8e405-236">ตัวแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8e405-236">Modifier</span></span> | <span data-ttu-id="8e405-237">ชนิดการคำนวณของตัวแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8e405-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="8e405-238">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8e405-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="8e405-239">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8e405-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="8e405-240">การลบ</span><span class="sxs-lookup"><span data-stu-id="8e405-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="8e405-241">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8e405-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="8e405-242">การลบ</span><span class="sxs-lookup"><span data-stu-id="8e405-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="8e405-243">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8e405-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="8e405-244">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8e405-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="8e405-245">การลบ</span><span class="sxs-lookup"><span data-stu-id="8e405-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="8e405-246">การลบ</span><span class="sxs-lookup"><span data-stu-id="8e405-246">Subtraction</span></span> |

<span data-ttu-id="8e405-247">การสอบถามในปริมาณการวัดที่กำหนดเองจะส่งคืนผลลัพธ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e405-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="8e405-248">ผลลัพธ์ `MyCustomAvailableforReservation` จะขึ้นอยู่กับการตั้งค่าการคำนวณในการวัดที่กำหนดเองเป็น:</span><span class="sxs-lookup"><span data-stu-id="8e405-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="8e405-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="8e405-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="8e405-250">การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="8e405-250">Posting on-hand changes</span></span>

<span data-ttu-id="8e405-251">URL ที่แน่นอนซึ่งจะมีการโพสต์เหตุการณ์ จะขึ้นอยู่กับภูมิภาคทางภูมิศาสตร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="8e405-252">ซึ่งจะใช้ฟอร์ม:</span><span class="sxs-lookup"><span data-stu-id="8e405-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="8e405-253">เมื่อมีการพิสูจน์ตัวจริง สามารถใช้ URL นี้พร้อมกับวิธีการ HTTP `POST` เพื่อส่งเหตุการณ์ของการเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปยังบริการ</span><span class="sxs-lookup"><span data-stu-id="8e405-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="8e405-254">ส่วนหัวพิเศษจะถูกใช้สำหรับการสื่อสารกับบริการ Dynamics 365 ผ่านคำขอ HTTP ซึ่งแสดงรหัสสภาพแวดล้อมของอินสแตนซ์ Supply Chain Management ที่ข้อมูลถูกลิงค์ไปถึง</span><span class="sxs-lookup"><span data-stu-id="8e405-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="8e405-255">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="8e405-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="8e405-256">การโพสต์ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือ 1</span><span class="sxs-lookup"><span data-stu-id="8e405-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="8e405-257">ตัวอย่างนี้แสดงสถานการณ์จำลองที่คุณจะตั้งค่าการตั้งค่าคอนฟิกมิติใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="8e405-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="8e405-258">ใช้การสอบถามต่อไปนี้เพื่อตั้งค่าคอนฟิกการแม็ปมิติใน Power Apps:</span><span class="sxs-lookup"><span data-stu-id="8e405-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="8e405-259">ขณะนี้คุณสามารถระบุ `dimensionDataSource` และใช้มิติที่กำหนดเองในการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="8e405-260">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8e405-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="8e405-261">การโพสต์ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือ 2</span><span class="sxs-lookup"><span data-stu-id="8e405-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="8e405-262">ตัวอย่างนี้แสดงสถานการณ์จำลองที่ไม่มีการตั้งค่าการแม็ปสำหรับการตั้งค่าคอนฟิกมิติใน Power Apps ดังนั้นการโพสต์ยังควรใช้มิติพื้นฐานด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8e405-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="8e405-263">มิติทั้งหมดต้องเป็นมิติฐาน เมื่อฟิลด์ `dimensionDataSource` เป็น null ว่างเปล่า หรือช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="8e405-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="8e405-264">คุณสมบัติฟิลด์ของเอกสาร JSON</span><span class="sxs-lookup"><span data-stu-id="8e405-264">JSON document field properties</span></span>

<span data-ttu-id="8e405-265">ฟิลด์จากตัวอย่างการสอบถาม JSON ที่ให้ไว้ก่อนหน้านี้ มีคุณสมบัติที่แสดงรายการอยู่ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e405-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="8e405-266">ฟิลด์ ID</span><span class="sxs-lookup"><span data-stu-id="8e405-266">Field ID</span></span> | <span data-ttu-id="8e405-267">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8e405-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="8e405-268">รหัสเฉพาะสำหรับเหตุการณ์การเปลี่ยนแปลงเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8e405-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="8e405-269">รหัสนี้จะใช้เพื่อให้แน่ใจว่า ถ้าการสื่อสารกับบริการล้มเหลวในระหว่างการโพสต์ การส่งเหตุการณ์อีกครั้งจะไม่มีผลในเหตุการณ์เดียวกันที่ถูกนับสองครั้งในระบบ</span><span class="sxs-lookup"><span data-stu-id="8e405-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="8e405-270">ตัวระบุขององค์กรที่ลิงก์ไปยังเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="8e405-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="8e405-271">นี่จะแม็ปไปยังองค์กร Supply Chain Management หรือรหัสพื้นที่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8e405-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="8e405-272">ตัวระบุของผลิตภัณฑ์ที่สงสัย</span><span class="sxs-lookup"><span data-stu-id="8e405-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="8e405-273">ปริมาณที่ต้องมีการเปลี่ยนแปลงปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="8e405-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="8e405-274">ตัวอย่างเช่น ถ้าตัวอย่างเช่น เบเกิลใหม่ 10 ชิ้นถูกเพิ่มไปยังชั้นวาง ค่านี้จะเป็น 10</span><span class="sxs-lookup"><span data-stu-id="8e405-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="8e405-275">ถ้าเบเกิล 3 ชิ้นถูกเอาออกจากชั้นวางหรือขายแล้ว ค่านี้จะเป็น -3</span><span class="sxs-lookup"><span data-stu-id="8e405-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="8e405-276">แหล่งข้อมูลของมิติที่ใช้ในการโพสต์เหตุการณ์การเปลี่ยนแปลงและการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="8e405-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="8e405-277">ถ้าคุณระบุแหล่งข้อมูล คุณสามารถใช้มิติที่กำหนดเองจากแหล่งข้อมูลที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="8e405-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="8e405-278">ด้วยการตั้งค่าคอนฟิกมิติ ความสามารถในการมองเห็นสินค้าคงคลังสามารถแม็ปมิติที่กำหนดเองกับมิติเริ่มต้นทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8e405-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="8e405-279">ถ้าไม่มีการระบุ `dimensionDataSource` คุณสามารถใช้มิติเริ่มต้นทั่วไปในการสอบถามของคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8e405-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="8e405-280">ถุงแบบไดนามิกของคู่คีย์/ค่า</span><span class="sxs-lookup"><span data-stu-id="8e405-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="8e405-281">การทำเช่นนี้จะแม็ปกับบางมิติใน Supply Chain Management แต่คุณยังสามารถเพิ่มมิติที่กำหนดเองได้ด้วย (เช่น *แหล่งที่มา*) ซึ่งอาจแสดงว่าเหตุการณ์นี้มาจาก Supply Chain Management หรือระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="8e405-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="8e405-282">การสอบถามปริมาณคงคลังคงเหลือปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="8e405-282">Querying current on-hand</span></span>

<span data-ttu-id="8e405-283">ปลายทางสำหรับการสอบถามปริมาณคงคลังคงเหลือปัจจุบันจะมี URL ที่คล้ายกัน:</span><span class="sxs-lookup"><span data-stu-id="8e405-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="8e405-284">ซึ่งจะมีการสอบถามด้วยวิธีการ HTTP `POST`</span><span class="sxs-lookup"><span data-stu-id="8e405-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="8e405-285">ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือปัจจุบัน 1</span><span class="sxs-lookup"><span data-stu-id="8e405-285">Current on-hand query example 1</span></span>

<span data-ttu-id="8e405-286">ตัวอย่างนี้แสดงสถานการณ์จำลองที่คุณดำเนินการการตั้งค่าคอนฟิกมิติเสร็จสมบูรณ์แล้วใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="8e405-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="8e405-287">ใช้การสอบถามต่อไปนี้เพื่อตั้งค่าคอนฟิกการแม็ปมิติใน Power Apps:</span><span class="sxs-lookup"><span data-stu-id="8e405-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="8e405-288">ขณะนี้คุณสามารถระบุ `dimensionDataSource` และใช้มิติที่กำหนดเองในการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e405-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="8e405-289">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8e405-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="8e405-290">คุณสามารถระบุ `DimensionDataSource` ใน `filters` และระบุมิติที่กำหนดเองในทั้ง `filters` และ `groupByValues`</span><span class="sxs-lookup"><span data-stu-id="8e405-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="8e405-291">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8e405-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="8e405-292">ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือปัจจุบัน 2</span><span class="sxs-lookup"><span data-stu-id="8e405-292">Current on-hand query example 2</span></span>

<span data-ttu-id="8e405-293">ตัวอย่างนี้แสดงสถานการณ์จำลองที่ไม่มีการตั้งค่าการแม็ปสำหรับการตั้งค่าคอนฟิกมิติใน Power Apps ดังนั้นการโพสต์ยังควรใช้มิติพื้นฐานด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8e405-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="8e405-294">มิติทั้งหมดต้องเป็นมิติฐาน เมื่อฟิลด์ `dimensionDataSource` ภายใต้ `filters` เป็น null ว่างเปล่า หรือช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="8e405-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="8e405-295">ผลลัพธ์การส่งคืนตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8e405-295">Example return result</span></span>

<span data-ttu-id="8e405-296">การสอบถามที่แสดงในตัวอย่างก่อนหน้านี้ อาจส่งผลให้เกิดผลลัพธ์ดังนี้</span><span class="sxs-lookup"><span data-stu-id="8e405-296">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="8e405-297">โปรดสังเกตว่าฟิลด์ปริมาณมีการจัดโครงสร้างเป็นพจนานุกรมของการวัดและค่าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8e405-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
