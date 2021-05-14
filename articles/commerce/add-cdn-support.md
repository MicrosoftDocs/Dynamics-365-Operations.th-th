---
title: เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)
description: หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Microsoft Dynamics 365 Commerce ของคุณ
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936841"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="f665a-103">เพิ่มการสนับสนุนสำหรับเครือข่ายการให้บริการเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="f665a-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f665a-104">หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f665a-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="f665a-105">เมื่อคุณตั้งค่าสภาพแวดล้อมของอีคอมเมิร์ซ ใน Dynamics 365 Commerce คุณสามารถตั้งค่าคอนฟิกให้ทำงานร่วมกับบริการ CDN ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="f665a-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="f665a-106">คุณสามารถเปิดใช้งานโดเมนที่กำหนดเองของคุณในระหว่างกระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="f665a-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="f665a-107">อีกทางหนึ่งคือ คุณสามารถใช้คำขอบริการเพื่อตั้งค่าหลังจากที่กระบวนการเตรียมใช้งานเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="f665a-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="f665a-108">กระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซสร้างชื่อโฮสต์ที่เชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="f665a-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="f665a-109">ชื่อโฮสต์นี้มีรูปแบบต่อไปนี้ โดย \<*e-commerce-tenant-name*\> เป็นชื่อของสภาพแวดล้อมของคุณ:</span><span class="sxs-lookup"><span data-stu-id="f665a-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="f665a-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="f665a-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="f665a-111">ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นในระหว่างกระบวนการจัดเตรียม สนับสนุนใบรับรอง Secure Sockets Layer (SSL) สำหรับ \*.commerce.dynamics.com เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f665a-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="f665a-112">ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="f665a-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="f665a-113">ดังนั้น คุณต้องยกเลิก SSL สำหรับโดเมนที่กำหนดเองใน CDN และส่งต่อข้อมูลจาก CDN ไปยังชื่อโฮสต์หรือปลายทางที่ Commerce ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f665a-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="f665a-114">นอกจากนี้ *สถิติ* (JavaScript หรือไฟล์ Cascading Style Sheets \[CSS\]) จาก Commerce จะถูกส่งจากปลายทางที่ Commerce ถูกสร้าง \*.(commerce.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="f665a-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="f665a-115">สถิตสามารถแคชได้เฉพาะเมื่อชื่อโฮสต์หรือปลายทางที่สร้าง Commerce ถูกวางอยู่หลัง CDN</span><span class="sxs-lookup"><span data-stu-id="f665a-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="f665a-116">ตั้งค่า SSL</span><span class="sxs-lookup"><span data-stu-id="f665a-116">Set up SSL</span></span>

<span data-ttu-id="f665a-117">หลังจากที่คุณจัดเตรียมสภาพแวดล้อม Commerce กับโดเมนแบบกำหนดเองที่ให้ไว้ หรือหลังจากที่คุณระบุโดเมนที่กำหนดเองสำหรับสภาพแวดล้อมของคุณ โดยใช้คำขอการบริการ คุณต้องทำงานกับทีมเตรียมความพร้อมของ Commerce เพื่อวางแผนการเปลี่ยนแปลง DNS</span><span class="sxs-lookup"><span data-stu-id="f665a-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="f665a-118">ดังที่ได้กล่าวถึงก่อนหน้านี้ ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นจะสนับสนุนใบรับรอง SSL สำหรับ \*.commerce.dynamics.com เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f665a-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="f665a-119">ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="f665a-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="f665a-120">การบริการ CDN</span><span class="sxs-lookup"><span data-stu-id="f665a-120">CDN services</span></span>

<span data-ttu-id="f665a-121">บริการ CDN ใดๆ สามารถใช้กับสภาพแวดล้อม Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="f665a-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="f665a-122">นี่คือ สองตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f665a-122">Here are two examples:</span></span>

- <span data-ttu-id="f665a-123">**Microsoft Azure Front Door Service** – โซลูชัน Azure CDN</span><span class="sxs-lookup"><span data-stu-id="f665a-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="f665a-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Front Door Service ของ Azure ดู [Azure Front Door Service Documentation](/azure/frontdoor/)</span><span class="sxs-lookup"><span data-stu-id="f665a-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](/azure/frontdoor/).</span></span>
- <span data-ttu-id="f665a-125">**Akamai Dynamic Site Accelerator** – สำหรับข้อมูลเพิ่มเติม ดู [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp)</span><span class="sxs-lookup"><span data-stu-id="f665a-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="f665a-126">การตั้งค่า CDN</span><span class="sxs-lookup"><span data-stu-id="f665a-126">CDN setup</span></span>

<span data-ttu-id="f665a-127">กระบวนการติดตั้ง CDN ประกอบด้วยขั้นตอนทั่วไปเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f665a-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="f665a-128">เพิ่มโฮสต์ front-end</span><span class="sxs-lookup"><span data-stu-id="f665a-128">Add a front-end host.</span></span>
1. <span data-ttu-id="f665a-129">ตั้งค่าคอนฟิกกลุ่ม back-end</span><span class="sxs-lookup"><span data-stu-id="f665a-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="f665a-130">ตั้งค่ากฎการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="f665a-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="f665a-131">เพิ่มโฮสต์ front-end</span><span class="sxs-lookup"><span data-stu-id="f665a-131">Add a front-end host</span></span>

<span data-ttu-id="f665a-132">คุณสามารถใช้บริการ CDN ใดๆได้ แต่ตัวอย่างในหัวข้อนี้ จะใช้ Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="f665a-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="f665a-133">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่า Front Door Service ่ของ Azure [เริ่มต้นแบบด่วน: สร้าง Front Door สำหรับโปรแกรมประยุกต์เว็บสากลที่พร้อมใช้งานอย่างสูง](/azure/frontdoor/quickstart-create-front-door)</span><span class="sxs-lookup"><span data-stu-id="f665a-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="f665a-134">ตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="f665a-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="f665a-135">การตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f665a-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="f665a-136">เพิ่ม **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** ลงในกลุ่มเสริมเป็นโฮสต์ที่ศุลกากรที่มีส่วนหัวของโฮสต์เสริมที่เหมือนกับ **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**</span><span class="sxs-lookup"><span data-stu-id="f665a-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="f665a-137">ภายใต้ **สร้างสมดุลในการโหลด** ให้เว้นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f665a-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="f665a-138">ปิดใช้งานการตรวจสอบความสมบูรณ์ของกลุ่มเสริม</span><span class="sxs-lookup"><span data-stu-id="f665a-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="f665a-139">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม back-end** ใน Front Door Service ของ Azure โดยมีการป้อนชื่อโฮสต์ back-end</span><span class="sxs-lookup"><span data-stu-id="f665a-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![เพิ่มกล่องโต้ตอบกลุ่ม backend](./media/CDN_BackendPool.png)

<span data-ttu-id="f665a-141">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม back-end** ใน Front Door Service ของ Azure ด้วยค่าเริ่มต้นการสร้างสมดุลในการโหลด</span><span class="sxs-lookup"><span data-stu-id="f665a-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![เพิ่มกล่องโต้ตอบกลุ่ม back-end ต่อไป](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="f665a-143">ตรวจสอบให้แน่ใจว่าได้ปิดใช้งาน **ปัญหาสุขภาพ** เมื่อตั้งค่าบริการ Front Door Service ของ Azure ของคุณเองใน Commerce</span><span class="sxs-lookup"><span data-stu-id="f665a-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="f665a-144">ตั้งค่ากฎใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="f665a-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="f665a-145">การตั้งค่ากฎการกำหนดเส้นทางใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f665a-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="f665a-146">เพิ่มการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="f665a-146">Add a routing rule.</span></span>
1. <span data-ttu-id="f665a-147">ในฟิลด์ **ชื่อ** ให้ป้อน **ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f665a-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="f665a-148">ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**</span><span class="sxs-lookup"><span data-stu-id="f665a-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="f665a-149">ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**</span><span class="sxs-lookup"><span data-stu-id="f665a-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="f665a-150">ภายใต้ **รูปแบบที่เข้ากัน** ในฟิลด์ด้านบนให้ป้อน **/\***</span><span class="sxs-lookup"><span data-stu-id="f665a-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="f665a-151">ภายใต้ **รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**</span><span class="sxs-lookup"><span data-stu-id="f665a-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="f665a-152">ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**</span><span class="sxs-lookup"><span data-stu-id="f665a-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="f665a-153">ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="f665a-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="f665a-154">ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="f665a-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="f665a-155">ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="f665a-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="f665a-156">หากโดเมนที่คุณจะใช้เปิดใช้งานอยู่และมีอยู่แล้ว ให้สร้างตั๋วการสนับสนุนจากไทล์ **สนับสนุน** ใน [Lifecycle Services ของ Microsoft Dynamics ](https://lcs.dynamics.com/) เพื่อรับความช่วยเหลือสำหรับขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f665a-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="f665a-157">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การขอความช่วยเหลือสำหรับแอป Finance and Operations หรือ Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)</span><span class="sxs-lookup"><span data-stu-id="f665a-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="f665a-158">หากโดเมนของคุณใหม่และไม่ใช่ไลฟ์โดเมนที่มีอยู่ก่อนหน้านี้ คุณสามารถเพิ่มโดเมนที่กำหนดเองของคุณในการตั้งค่าคอนฟิกสำหรับ Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="f665a-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="f665a-159">การทำเช่นนี้จะเปิดใช้งานการรับส่งผ่านเว็บเพื่อให้ตรงกับไซต์ของคุณผ่านทางอินสแตนซ์ Front Door ของ Azure</span><span class="sxs-lookup"><span data-stu-id="f665a-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="f665a-160">การเพิ่มโดเมนแบบกำหนดเอง (ตัวอย่างเช่น `www.fabrikam.com`) คุณต้องตั้งค่าคอนฟิก Canonical Name (CNAME) สำหรับโดเมน</span><span class="sxs-lookup"><span data-stu-id="f665a-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="f665a-161">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **การตั้งค่าคอนฟิก CNAME** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="f665a-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![กล่องโต้ตอบการตั้งค่าคอนฟิก CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="f665a-163">คุณสามารถใช้ Front Door Service ของ Azure เพื่อจัดการใบรับรอง หรือคุณสามารถใช้ใบรับรองของคุณเองสำหรับโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="f665a-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="f665a-164">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **Custom Domain HTTPS** ใน Front Door Service ของ Azure</span><span class="sxs-lookup"><span data-stu-id="f665a-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![กล่องโต้ตอบ Custom Domain HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="f665a-166">สำหรับคำแนะนำโดยละเอียดเกี่ยวกับการเพิ่มโดเมนที่กำหนดเองลงใน Front Door ของ Azure ของคุณ ให้ดูที่ [การเพิ่มโดเมนที่กำหนดเองลงใน Front Door ของคุณ](/azure/frontdoor/front-door-custom-domain)</span><span class="sxs-lookup"><span data-stu-id="f665a-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="f665a-167">ตอนนี้ CDN ของคุณควรได้รับการตั้งค่าคอนฟิกอย่างถูกต้อง เพื่อให้สามารถใช้กับไซต์ Commerce ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="f665a-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f665a-168">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f665a-168">Additional resources</span></span>

[<span data-ttu-id="f665a-169">ตัวเลือกการใช้งานเครือข่ายการจัดส่งเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f665a-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]