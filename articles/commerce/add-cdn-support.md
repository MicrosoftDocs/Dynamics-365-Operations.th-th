---
title: เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)
description: หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Dynamics 365 Commerce ของคุณ
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 662d26c0157377977bd1031cd7bb13a8e692f37e
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646050"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="fb0ad-103">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="fb0ad-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fb0ad-104">หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb0ad-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="fb0ad-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="fb0ad-105">Overview</span></span>

<span data-ttu-id="fb0ad-106">เมื่อคุณตั้งค่าสภาพแวดล้อมของอีคอมเมิร์ซ ใน Dynamics 365 Commerce คุณสามารถตั้งค่าคอนฟิกให้ทำงานร่วมกับบริการ CDN ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="fb0ad-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="fb0ad-107">คุณสามารถเปิดใช้งานโดเมนที่กำหนดเองของคุณในระหว่างกระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb0ad-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="fb0ad-108">อีกทางหนึ่งคือ คุณสามารถใช้คำขอบริการเพื่อตั้งค่าหลังจากที่กระบวนการเตรียมใช้งานเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="fb0ad-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="fb0ad-109">กระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซสร้างชื่อโฮสต์ที่เชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="fb0ad-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="fb0ad-110">ชื่อโฮสต์นี้มีรูปแบบต่อไปนี้ โดย \<*e-commerce-tenant-name*\> เป็นชื่อของสภาพแวดล้อมของคุณ:</span><span class="sxs-lookup"><span data-stu-id="fb0ad-110">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="fb0ad-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="fb0ad-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="fb0ad-112">ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นในระหว่างกระบวนการจัดเตรียม สนับสนุนใบรับรอง Secure Sockets Layer (SSL) สำหรับ \*.commerce.dynamics.com เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb0ad-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="fb0ad-113">ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="fb0ad-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="fb0ad-114">ดังนั้น คุณต้องยกเลิก SSL สำหรับโดเมนที่กำหนดเองใน CDN และส่งต่อข้อมูลจาก CDN ไปยังชื่อโฮสต์หรือปลายทางที่ Commerce ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fb0ad-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="fb0ad-115">นอกจากนี้ *สถิติ* (JavaScript หรือไฟล์ Cascading Style Sheets \[CSS\]) จาก Commerce จะถูกส่งจากปลายทางที่ Commerce ถูกสร้าง \*.(commerce.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="fb0ad-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="fb0ad-116">สถิตสามารถแคชได้เฉพาะเมื่อชื่อโฮสต์หรือปลายทางที่สร้าง Commerce ถูกวางอยู่หลัง CDN</span><span class="sxs-lookup"><span data-stu-id="fb0ad-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="fb0ad-117">ตั้งค่า SSL</span><span class="sxs-lookup"><span data-stu-id="fb0ad-117">Set up SSL</span></span>

<span data-ttu-id="fb0ad-118">เพื่อช่วยรับประกันว่ามีการตั้งค่า SSL และสถิตที่มีการแคช คุณต้องตั้งค่าคอนฟิก CDN ของคุณเพื่อให้เชื่อมโยงกับชื่อโฮสต์ที่ Commerce สร้างขึ้นสำหรับสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb0ad-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="fb0ad-119">นอกจากนี้คุณต้องแคชรูปแบบต่อไปนี้สำหรับสถิตเท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="fb0ad-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="fb0ad-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="fb0ad-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="fb0ad-121">หลังจากที่คุณจัดเตรียมสภาพแวดล้อม Commerce กับโดเมนแบบกำหนดเองที่ให้ไว้ หรือหลังจากที่คุณระบุโดเมนที่กำหนดเองสำหรับสภาพแวดล้อมของคุณ โดยใช้คำขอการบริการ ให้กำหนดโดเมนที่กำหนดเองของคุณไปยังชื่อโฮสต์หรือปลายทางที่ Commerce สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fb0ad-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="fb0ad-122">ดังที่ได้กล่าวถึงก่อนหน้านี้ ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นจะสนับสนุนใบรับรอง SSL สำหรับ \*.commerce.dynamics.com เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb0ad-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="fb0ad-123">ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="fb0ad-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="fb0ad-124">การบริการ CDN</span><span class="sxs-lookup"><span data-stu-id="fb0ad-124">CDN services</span></span>

<span data-ttu-id="fb0ad-125">บริการ CDN ใดๆ สามารถใช้กับสภาพแวดล้อม Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="fb0ad-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="fb0ad-126">นี่คือ สองตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="fb0ad-126">Here are two examples:</span></span>

- <span data-ttu-id="fb0ad-127">**Microsoft Azure Front Door Service** – โซลูชัน Azure CDN</span><span class="sxs-lookup"><span data-stu-id="fb0ad-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="fb0ad-128">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Front Door Service ของ Azure ดู [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/)</span><span class="sxs-lookup"><span data-stu-id="fb0ad-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="fb0ad-129">**Akamai Dynamic Site Accelerator** – สำหรับข้อมูลเพิ่มเติม ดู [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp)</span><span class="sxs-lookup"><span data-stu-id="fb0ad-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="fb0ad-130">การตั้งค่า CDN</span><span class="sxs-lookup"><span data-stu-id="fb0ad-130">CDN setup</span></span>

<span data-ttu-id="fb0ad-131">กระบวนการติดตั้ง CDN ประกอบด้วยขั้นตอนทั่วไปเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="fb0ad-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="fb0ad-132">เพิ่มโฮสต์ front-end</span><span class="sxs-lookup"><span data-stu-id="fb0ad-132">Add a front-end host.</span></span>
1. <span data-ttu-id="fb0ad-133">ตั้งค่าคอนฟิกกลุ่ม back-end</span><span class="sxs-lookup"><span data-stu-id="fb0ad-133">Configure a backend pool.</span></span>
1. <span data-ttu-id="fb0ad-134">ตั้งค่ากฎสำหรับการกำหนดเส้นทางและการแคช</span><span class="sxs-lookup"><span data-stu-id="fb0ad-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="fb0ad-135">เพิ่มโฮสต์ front-end</span><span class="sxs-lookup"><span data-stu-id="fb0ad-135">Add a front-end host</span></span>

<span data-ttu-id="fb0ad-136">คุณสามารถใช้บริการ CDN ใดๆได้ แต่ตัวอย่างในหัวข้อนี้ จะใช้ Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ad-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="fb0ad-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่า Front Door Service ่ของ Azure [เริ่มต้นแบบด่วน: สร้าง Front Door สำหรับโปรแกรมประยุกต์เว็บสากลที่พร้อมใช้งานอย่างสูง](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)</span><span class="sxs-lookup"><span data-stu-id="fb0ad-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="fb0ad-138">ตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ad-138">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="fb0ad-139">การตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fb0ad-139">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="fb0ad-140">เพิ่ม **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** ไปยังกลุ่ม back-end เพื่อเป็นโฮสต์ที่กำหนดเอง ที่มีส่วนหัวของโฮสต์ back-end ที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="fb0ad-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="fb0ad-141">ภายใต้ **สร้างสมดุลในการโหลด** ให้เว้นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fb0ad-141">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="fb0ad-142">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม back-end** ใน Front Door Service ของ Azure โดยมีการป้อนชื่อโฮสต์ back-end</span><span class="sxs-lookup"><span data-stu-id="fb0ad-142">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![เพิ่มกล่องโต้ตอบกลุ่ม backend](./media/CDN_BackendPool.png)

<span data-ttu-id="fb0ad-144">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม back-end** ใน Front Door Service ของ Azure ด้วยค่าเริ่มต้นการสร้างสมดุลในการโหลด</span><span class="sxs-lookup"><span data-stu-id="fb0ad-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![เพิ่มกล่องโต้ตอบกลุ่ม back-end ต่อไป](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="fb0ad-146">ตั้งค่ากฎใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ad-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="fb0ad-147">การตั้งค่ากฎการกำหนดเส้นทางใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fb0ad-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="fb0ad-148">เพิ่มการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="fb0ad-148">Add a routing rule.</span></span>
1. <span data-ttu-id="fb0ad-149">ในฟิลด์ **ชื่อ** ให้ป้อน **ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="fb0ad-150">ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="fb0ad-151">ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="fb0ad-152">ภายใต้ **รูปแบบที่เข้ากัน** ในฟิลด์ด้านบนให้ป้อน **/\***</span><span class="sxs-lookup"><span data-stu-id="fb0ad-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="fb0ad-153">ภายใต้ **รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="fb0ad-154">ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="fb0ad-155">ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="fb0ad-156">ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="fb0ad-157">ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="fb0ad-158">การตั้งค่ากฎการแคชใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fb0ad-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="fb0ad-159">เพิ่มกฎการแคช</span><span class="sxs-lookup"><span data-stu-id="fb0ad-159">Add a caching rule.</span></span>
1. <span data-ttu-id="fb0ad-160">ในฟิลด์ **ชื่อ** ให้ป้อน **สถิติ**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="fb0ad-161">ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="fb0ad-162">ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="fb0ad-163">ภายใต้ **Patterns to match** ในฟิลด์ด้านบนให้ป้อน **/\_msdyn365/\_scnr/\***</span><span class="sxs-lookup"><span data-stu-id="fb0ad-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="fb0ad-164">ภายใต้ **รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="fb0ad-165">ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="fb0ad-166">ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="fb0ad-167">ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="fb0ad-168">ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="fb0ad-169">ในฟิลด์ **พฤติกรรมแคชสตริงการสอบถาม** เลือก **แคลทุก URL ที่ไม่ซ้ำกัน**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="fb0ad-170">ในกลุ่มฟิลด์ **การบีบอัดแบบไดนามิก** ให้เลือกตัวเลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="fb0ad-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="fb0ad-171">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกฎ** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ad-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![กล่องโต้ตอบกฎ](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="fb0ad-173">หากโดเมนที่คุณจะใช้เปิดใช้งานอยู่และมีอยู่แล้ว ให้สร้างตั๋วการสนับสนุนจากไทล์ **สนับสนุน** ใน [Lifecycle Services ของ Microsoft Dynamics ](https://lcs.dynamics.com/) เพื่อรับความช่วยเหลือสำหรับขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="fb0ad-173">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="fb0ad-174">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การขอความช่วยเหลือสำหรับแอป Finance and Operations หรือ Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)</span><span class="sxs-lookup"><span data-stu-id="fb0ad-174">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="fb0ad-175">หากโดเมนของคุณใหม่และไม่ใช่ไลฟ์โดเมนที่มีอยู่ก่อนหน้านี้ คุณสามารถเพิ่มโดเมนที่กำหนดเองของคุณในการตั้งค่าคอนฟิกสำหรับ Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ad-175">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="fb0ad-176">การทำเช่นนี้จะเปิดใช้งานการรับส่งผ่านเว็บเพื่อให้ตรงกับไซต์ของคุณผ่านทางอินสแตนซ์ Front Door ของ Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ad-176">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="fb0ad-177">การเพิ่มโดเมนแบบกำหนดเอง (ตัวอย่างเช่น `www.fabrikam.com`) คุณต้องตั้งค่าคอนฟิก Canonical Name (CNAME) สำหรับโดเมน</span><span class="sxs-lookup"><span data-stu-id="fb0ad-177">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="fb0ad-178">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **การตั้งค่าคอนฟิก CNAME** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ad-178">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![กล่องโต้ตอบการตั้งค่าคอนฟิก CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="fb0ad-180">คุณสามารถใช้ Front Door Service ของ Azure เพื่อจัดการใบรับรอง หรือคุณสามารถใช้ใบรับรองของคุณเองสำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="fb0ad-180">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="fb0ad-181">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **Custom Domain HTTPS** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ad-181">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![กล่องโต้ตอบ Custom Domain HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="fb0ad-183">สำหรับคำแนะนำโดยละเอียดเกี่ยวกับการเพิ่มโดเมนที่กำหนดเองลงใน Front Door ของ Azure ของคุณ ให้ดูที่ [การเพิ่มโดเมนที่กำหนดเองลงใน Front Door ของคุณ](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain)</span><span class="sxs-lookup"><span data-stu-id="fb0ad-183">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="fb0ad-184">ตอนนี้ CDN ของคุณควรได้รับการตั้งค่าคอนฟิกอย่างถูกต้อง เพื่อให้สามารถใช้กับไซต์ Commerce ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="fb0ad-184">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb0ad-185">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fb0ad-185">Additional resources</span></span>

[<span data-ttu-id="fb0ad-186">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb0ad-186">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fb0ad-187">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="fb0ad-187">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="fb0ad-188">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="fb0ad-188">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="fb0ad-189">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="fb0ad-189">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="fb0ad-190">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="fb0ad-190">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="fb0ad-191">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="fb0ad-191">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="fb0ad-192">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="fb0ad-192">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="fb0ad-193">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="fb0ad-193">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="fb0ad-194">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="fb0ad-194">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="fb0ad-195">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="fb0ad-195">Enable location-based store detection</span></span>](enable-store-detection.md)
