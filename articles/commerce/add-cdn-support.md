---
title: เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)
description: หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Dynamics 365 Commerce ของคุณ
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: bf5a0da2803f985e6c0c04dd9916977397173d11
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001633"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="d2412-103">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="d2412-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d2412-104">หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2412-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="d2412-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="d2412-105">Overview</span></span>

<span data-ttu-id="d2412-106">เมื่อคุณตั้งค่าสภาพแวดล้อมของอีคอมเมิร์ซ ใน Dynamics 365 Commerce คุณสามารถตั้งค่าคอนฟิกให้ทำงานร่วมกับบริการ CDN ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d2412-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="d2412-107">คุณสามารถเปิดใช้งานโดเมนที่กำหนดเองของคุณในระหว่างกระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2412-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="d2412-108">อีกทางหนึ่งคือ คุณสามารถใช้คำขอบริการเพื่อตั้งค่าหลังจากที่กระบวนการเตรียมใช้งานเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="d2412-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="d2412-109">กระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซสร้างชื่อโฮสต์ที่เชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="d2412-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="d2412-110">ชื่อโฮสต์นี้มีรูปแบบต่อไปนี้ โดย *ชื่อผู้เช่าอีคอมเมิร์ซ* เป็นชื่อของสภาพแวดล้อมของคุณ:</span><span class="sxs-lookup"><span data-stu-id="d2412-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="d2412-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="d2412-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="d2412-112">ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นในระหว่างกระบวนการจัดเตรียม สนับสนุนใบรับรอง Secure Sockets Layer (SSL) สำหรับ \*.commerce.dynamics.com เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d2412-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="d2412-113">ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="d2412-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="d2412-114">ดังนั้น คุณต้องยกเลิก SSL สำหรับโดเมนที่กำหนดเองใน CDN และส่งต่อข้อมูลจาก CDN ไปยังชื่อโฮสต์หรือปลายทางที่ Commerce ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="d2412-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="d2412-115">นอกจากนี้ *สถิติ* (JavaScript หรือไฟล์ Cascading Style Sheets \[CSS\]) จาก Commerce จะถูกส่งจากปลายทางที่ Commerce ถูกสร้าง \*.(commerce.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="d2412-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="d2412-116">สถิตสามารถแคชได้เฉพาะเมื่อชื่อโฮสต์หรือปลายทางที่สร้าง Commerce ถูกวางอยู่หลัง CDN</span><span class="sxs-lookup"><span data-stu-id="d2412-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="d2412-117">ตั้งค่า SSL</span><span class="sxs-lookup"><span data-stu-id="d2412-117">Set up SSL</span></span>

<span data-ttu-id="d2412-118">เพื่อช่วยรับประกันว่ามีการตั้งค่า SSL และสถิตที่มีการแคช คุณต้องตั้งค่าคอนฟิก CDN ของคุณเพื่อให้เชื่อมโยงกับชื่อโฮสต์ที่ Commerce สร้างขึ้นสำหรับสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2412-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="d2412-119">นอกจากนี้คุณต้องแคชรูปแบบต่อไปนี้สำหรับสถิตเท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="d2412-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="d2412-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="d2412-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="d2412-121">หลังจากที่คุณจัดเตรียมสภาพแวดล้อม Commerce กับโดเมนแบบกำหนดเองที่ให้ไว้ หรือหลังจากที่คุณระบุโดเมนที่กำหนดเองสำหรับสภาพแวดล้อมของคุณ โดยใช้คำขอการบริการ ให้กำหนดโดเมนที่กำหนดเองของคุณไปยังชื่อโฮสต์หรือปลายทางที่ Commerce สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="d2412-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="d2412-122">ดังที่ได้กล่าวถึงก่อนหน้านี้ ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นจะสนับสนุนใบรับรอง SSL สำหรับ \*.commerce.dynamics.com เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d2412-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="d2412-123">ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="d2412-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="d2412-124">การบริการ CDN</span><span class="sxs-lookup"><span data-stu-id="d2412-124">CDN services</span></span>

<span data-ttu-id="d2412-125">บริการ CDN ใดๆ สามารถใช้กับสภาพแวดล้อม Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="d2412-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="d2412-126">นี่คือ สองตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="d2412-126">Here are two examples:</span></span>

- <span data-ttu-id="d2412-127">**Microsoft Azure Front Door Service** – โซลูชัน Azure CDN</span><span class="sxs-lookup"><span data-stu-id="d2412-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="d2412-128">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Front Door Service ของ Azure ดู [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/)</span><span class="sxs-lookup"><span data-stu-id="d2412-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="d2412-129">**Akamai Dynamic Site Accelerator** – สำหรับข้อมูลเพิ่มเติม ดู [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp)</span><span class="sxs-lookup"><span data-stu-id="d2412-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="d2412-130">การตั้งค่า CDN</span><span class="sxs-lookup"><span data-stu-id="d2412-130">CDN setup</span></span>

<span data-ttu-id="d2412-131">กระบวนการติดตั้ง CDN ประกอบด้วยขั้นตอนทั่วไปเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="d2412-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="d2412-132">เพิ่มโฮสต์ front-end</span><span class="sxs-lookup"><span data-stu-id="d2412-132">Add a front-end host.</span></span>
1. <span data-ttu-id="d2412-133">ตั้งค่าคอนฟิกกลุ่ม back-end</span><span class="sxs-lookup"><span data-stu-id="d2412-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="d2412-134">ตั้งค่ากฎสำหรับการกำหนดเส้นทางและการแคช</span><span class="sxs-lookup"><span data-stu-id="d2412-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="d2412-135">เพิ่มโฮสต์ front-end</span><span class="sxs-lookup"><span data-stu-id="d2412-135">Add a front-end host</span></span>

<span data-ttu-id="d2412-136">คุณสามารถใช้บริการ CDN ใดๆได้ แต่ตัวอย่างในหัวข้อนี้ จะใช้ Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="d2412-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="d2412-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่า Front Door Service ่ของ Azure [เริ่มต้นแบบด่วน: สร้าง Front Door สำหรับโปรแกรมประยุกต์เว็บสากลที่พร้อมใช้งานอย่างสูง](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)</span><span class="sxs-lookup"><span data-stu-id="d2412-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="d2412-138">ตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="d2412-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="d2412-139">การตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d2412-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="d2412-140">เพิ่ม **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** ไปยังกลุ่ม back-end เป็นโฮสต์ที่กำหนดเอง ที่มีส่วนหัวของโฮสต์ back-end ที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="d2412-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="d2412-141">ภายใต้ **ปัญหาสุขภาพ** ในฟิลด์ **พาธ** ให้ป้อน **/keepalive**</span><span class="sxs-lookup"><span data-stu-id="d2412-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="d2412-142">ในฟิลด์ **ช่วง (วินาที)** ให้ป้อน **255**</span><span class="sxs-lookup"><span data-stu-id="d2412-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="d2412-143">ภายใต้ **สร้างสมดุลในการโหลด** ให้เว้นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2412-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="d2412-144">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม Backend** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="d2412-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![เพิ่มกล่องโต้ตอบกลุ่ม backend](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="d2412-146">ตั้งค่ากฎใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="d2412-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="d2412-147">การตั้งค่ากฎการกำหนดเส้นทางใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d2412-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="d2412-148">เพิ่มการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="d2412-148">Add a routing rule.</span></span>
1. <span data-ttu-id="d2412-149">ในฟิลด์ **ชื่อ** ให้ป้อน **ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="d2412-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="d2412-150">ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**</span><span class="sxs-lookup"><span data-stu-id="d2412-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="d2412-151">ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**</span><span class="sxs-lookup"><span data-stu-id="d2412-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="d2412-152">ภายใต้ **รูปแบบที่เข้ากัน** ในฟิลด์ด้านบนให้ป้อน **/\***</span><span class="sxs-lookup"><span data-stu-id="d2412-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="d2412-153">ภายใต้ **รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**</span><span class="sxs-lookup"><span data-stu-id="d2412-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="d2412-154">ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**</span><span class="sxs-lookup"><span data-stu-id="d2412-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="d2412-155">ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="d2412-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="d2412-156">ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d2412-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="d2412-157">ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d2412-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="d2412-158">การตั้งค่ากฎการแคชใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d2412-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="d2412-159">เพิ่มกฎการแคช</span><span class="sxs-lookup"><span data-stu-id="d2412-159">Add a caching rule.</span></span>
1. <span data-ttu-id="d2412-160">ในฟิลด์ **ชื่อ** ให้ป้อน **สถิติ**</span><span class="sxs-lookup"><span data-stu-id="d2412-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="d2412-161">ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**</span><span class="sxs-lookup"><span data-stu-id="d2412-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="d2412-162">ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**</span><span class="sxs-lookup"><span data-stu-id="d2412-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="d2412-163">ภายใต้ **Patterns to match** ในฟิลด์ด้านบนให้ป้อน **/\_msdyn365/\_scnr/\***</span><span class="sxs-lookup"><span data-stu-id="d2412-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="d2412-164">ภายใต้ **รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**</span><span class="sxs-lookup"><span data-stu-id="d2412-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="d2412-165">ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**</span><span class="sxs-lookup"><span data-stu-id="d2412-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="d2412-166">ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="d2412-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="d2412-167">ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d2412-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="d2412-168">ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d2412-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="d2412-169">ในฟิลด์ **พฤติกรรมแคชสตริงการสอบถาม** เลือก **แคลทุก URL ที่ไม่ซ้ำกัน**</span><span class="sxs-lookup"><span data-stu-id="d2412-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="d2412-170">ในกลุ่มฟิลด์ **การบีบอัดแบบไดนามิก** ให้เลือกตัวเลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d2412-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="d2412-171">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกฎ** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="d2412-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![กล่องโต้ตอบกฎ](./media/CDN_CachingRule.png)

<span data-ttu-id="d2412-173">หลังจากที่มีการปรับใช้การตั้งค่าคอนฟิกนี้แล้ว คุณต้องเพิ่มโดเมนที่กำหนดเองของคุณในการตั้งค่าคอนฟิกสำหรับ Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="d2412-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="d2412-174">การเพิ่มโดเมนแบบกำหนดเอง (ตัวอย่างเช่น `www.fabrikam.com`) คุณต้องตั้งค่าคอนฟิก Canonical Name (CNAME) สำหรับโดเมน</span><span class="sxs-lookup"><span data-stu-id="d2412-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="d2412-175">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **การตั้งค่าคอนฟิก CNAME** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="d2412-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![กล่องโต้ตอบการตั้งค่าคอนฟิก CNAME](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="d2412-177">ถ้าโดเมนที่คุณจะใช้มีการใช้งานและใช้ได้ยู่แล้ว โปรดติดต่อฝ่ายสนับสนุนเพื่อเปิดใช้งานโดเมนนี้ กับ Front Door Service ของ Azure เพื่อตั้งค่าการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="d2412-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="d2412-178">คุณสามารถใช้ Front Door Service ของ Azure เพื่อจัดการใบรับรอง หรือคุณสามารถใช้ใบรับรองของคุณเองสำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="d2412-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="d2412-179">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **Custom Domain HTTPS** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="d2412-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![กล่องโต้ตอบ Custom Domain HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="d2412-181">ตอนนี้ CDN ของคุณควรได้รับการตั้งค่าคอนฟิกอย่างถูกต้อง เพื่อให้สามารถใช้กับไซต์ Commerce ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d2412-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2412-182">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d2412-182">Additional resources</span></span>

[<span data-ttu-id="d2412-183">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2412-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="d2412-184">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="d2412-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="d2412-185">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="d2412-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="d2412-186">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="d2412-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="d2412-187">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="d2412-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="d2412-188">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d2412-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="d2412-189">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="d2412-189">Enable location-based store detection</span></span>](enable-store-detection.md)
