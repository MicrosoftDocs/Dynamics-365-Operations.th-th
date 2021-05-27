---
title: ตัวเลือกการใช้งานเครือข่ายการจัดส่งเนื้อหา
description: หัวข้อนี้จะทบทวนเกี่ยวกับตัวเลือกต่างๆ ของการใช้งานเครือข่ายการจัดส่งเนื้อหา (CDN) ที่สามารถใช้ได้กับสภาพแวดล้อม Microsoft Dynamics 365 Commerce ตัวเลือกเหล่านี้รวมถึงอินสแตนซ์ดั้งเดิมของ Azure Front Door และอินสแตนซ์ที่ลูกค้าเป็นเจ้าของของ Azure Front Door
author: BrianShook
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f6e8fb2baf85be0eaecfffcc7ec6cbb457c3bb04
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021901"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="ed3f6-104">ตัวเลือกการใช้งานเครือข่ายการจัดส่งเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="ed3f6-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed3f6-105">หัวข้อนี้จะทบทวนเกี่ยวกับตัวเลือกต่างๆ ของการใช้งานเครือข่ายการจัดส่งเนื้อหา (CDN) ที่สามารถใช้ได้กับสภาพแวดล้อม Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ed3f6-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="ed3f6-106">ตัวเลือกเหล่านี้รวมถึงอินสแตนซ์ดั้งเดิมของ Azure Front Door และอินสแตนซ์ที่ลูกค้าเป็นเจ้าของของ Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="ed3f6-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="ed3f6-107">ลูกค้าเชิงพาณิชย์มีตัวเลือกหลายตัวเลือกเมื่อพิจารณาบริการ CDN ที่จะใช้กับสภาพแวดล้อมเชิงพาณิชย์ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="ed3f6-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="ed3f6-108">การพาณิชย์จะถูกเปิดตัวพร้อมการสนับสนุน Azure Front Door ขั้นพื้นฐานที่ครอบคลุมโฮสติ้งพื้นฐานและข้อกำหนดโดเมนที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="ed3f6-109">สำหรับบริษัทที่ต้องการการควบคุมเพิ่มมากขึ้นและความสามารถด้านความปลอดภัยที่เฉพาะเจาะจงมากขึ้น เช่น ไฟร์วอลล์เว็บแอพลิเคชัน (WAF) ตัวเลือกที่ดีที่สุดอาจใช้อินสแตนซ์ Azure Front Door ที่ลูกค้าเป็นเจ้าของหรือบริการ CDN ภายนอก</span><span class="sxs-lookup"><span data-stu-id="ed3f6-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="ed3f6-110">ตัวเลือกการใช้งาน CDN สามตัวเลือกต่อไปนี้สามารถใช้ได้กับสภาพแวดล้อมเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="ed3f6-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="ed3f6-111">อินสแตนซ์ Commerce-provided ของ Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="ed3f6-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="ed3f6-112">อินสแตนซ์ Azure Front Door ที่ลูกค้าเป็นเจ้าของ (เพื่อการควบคุมที่เพิ่มขึ้นและคุณสมบัติด้านความปลอดภัยเพิ่มเติม)</span><span class="sxs-lookup"><span data-stu-id="ed3f6-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="ed3f6-113">บริการ CDN ภายนอก</span><span class="sxs-lookup"><span data-stu-id="ed3f6-113">An external CDN service</span></span>

<span data-ttu-id="ed3f6-114">ตัวเลือกการใช้งาน CDN ทั้งสามจะแสดงเฉพาะเนื้อหา HTML แบบไดนามิกจากโดเมนที่กำหนดเองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ed3f6-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="ed3f6-115">การพาณิชย์จะจัดการ JavaScript Cascading Style Sheets (CSS) รูปภาพ วิดีโอ และเนื้อหาแบบคงที่อื่นๆ โดยอัตโนมัติผ่านทาง CDN ที่จัดการโดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="ed3f6-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="ed3f6-116">ตัวเลือกที่คุณเลือกจะระบุความสามารถในการปฏิบัติงาน ความสามารถในการควบคุม และความสามารถด้านความปลอดภัยเพิ่มเติมที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ed3f6-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="ed3f6-117">ภาพประกอบต่อไปนี้จะแสดงภาพรวมของสถาปัตยกรรมเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="ed3f6-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![ภาพรวมของสถาปัตยกรรมเชิงพาณิชย์](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="ed3f6-119">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีตั้งค่าอินสแตนซ์ของ Azure Front Door สำหรับหน้าเว็บไซต์ Commerce ของคุณ โปรดดูที่ [เพิ่ม CDN Support](add-cdn-support.md)</span><span class="sxs-lookup"><span data-stu-id="ed3f6-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="ed3f6-120">ใช้อินสแตนซ์ Commerce-provided ของ Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="ed3f6-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="ed3f6-121">ตารางต่อไปนี้จะแสดงรายการข้อดีและข้อเสียของการใช้อินสแตนซ์ Commerce-provided ของ Azure Front Door เพื่อจัดการเนื้อหาปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="ed3f6-122">ข้อดี</span><span class="sxs-lookup"><span data-stu-id="ed3f6-122">Pros</span></span> | <span data-ttu-id="ed3f6-123">ข้อเสีย</span><span class="sxs-lookup"><span data-stu-id="ed3f6-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="ed3f6-124">อินสแตนซ์ที่ถูกรวมอยู่ในต้นทุนเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="ed3f6-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="ed3f6-125">เนื่องจากอินสแตนซ์มีการจัดการโดยทีมงาน Commerce จึงต้องมีการบํารุงรักษาน้อยลง และมีขั้นตอนการตั้งค่าที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="ed3f6-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="ed3f6-126">โครงสร้างพื้นฐานที่ Azure เป็นโฮสต์ สามารถปรับสเกล ปลอดภัย และไว้ใจได้</span><span class="sxs-lookup"><span data-stu-id="ed3f6-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="ed3f6-127">ใบรับรอง Secure Sockets Layer (SSL) ต้องมีการตั้งค่าแบบใช้ครั้งเดียวและต่ออายุโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ed3f6-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="ed3f6-128">อินสแตนซ์จะถูกตรวจสอบหาข้อผิดพลาดและความผิดปกติโดยทีมงาน Commerce</span><span class="sxs-lookup"><span data-stu-id="ed3f6-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="ed3f6-129">ไม่รองรับ A WAF</span><span class="sxs-lookup"><span data-stu-id="ed3f6-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="ed3f6-130">ไม่มีการปรับแต่งหรือปรับตั้งค่าใดๆ โดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ed3f6-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="ed3f6-131">อินสแตนซ์จะขึ้นอยู่กับทีมงาน Commerce ในการอัพเดตหรือการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="ed3f6-132">จำเป็นต้องใช้อินสแตนซ์ Azure Front Door แยกต่างหากสำหรับโดเมน apex และจำเป็นต้องมีงานเพิ่มเติมเพื่อรวมโดเมน apex กับ Azure DNS</span><span class="sxs-lookup"><span data-stu-id="ed3f6-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="ed3f6-133">ไม่มีการส่งข้อมูลทางไกลเกี่ยวกับการตอบสนองต่อวินาที (RPS) หรืออัตราข้อผิดพลาดที่ให้ไว้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ed3f6-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="ed3f6-134">ภาพประกอบต่อไปนี้จะแสดงสถาปัตยกรรมของอินสแตนซ์ Commerce-provided ของ Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="ed3f6-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![อินสแตนซ์ Commerce-provided ของ Azure Front Door](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="ed3f6-136">ใช้อินสแตนซ์ Azure Front Door ที่ลูกค้าเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="ed3f6-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="ed3f6-137">ตารางต่อไปนี้จะแสดงรายการข้อดีและข้อเสียของการใช้อินสแตนซ์ที่ลูกค้าเป็นเจ้าของของ Azure Front Door เพื่อจัดการเนื้อหาปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="ed3f6-138">ข้อดี</span><span class="sxs-lookup"><span data-stu-id="ed3f6-138">Pros</span></span> | <span data-ttu-id="ed3f6-139">ข้อเสีย</span><span class="sxs-lookup"><span data-stu-id="ed3f6-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="ed3f6-140">การตั้งค่ามีความปลอดภัยและจัดการได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="ed3f6-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="ed3f6-141">โครงสร้างพื้นฐานที่ Azure เป็นโฮสต์ สามารถปรับสเกล ปลอดภัย และไว้ใจได้</span><span class="sxs-lookup"><span data-stu-id="ed3f6-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="ed3f6-142">อินสแตนซ์อนุญาตให้รวม WAF และตัวควบคุมกฎแบบ Granular เพื่อให้ความปลอดภัยมีระดับการปรับปรุงซึ่งปรับแต่งมาโดยเฉพาะกับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ed3f6-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="ed3f6-143">อินสแตนซ์ชช่วยให้สามารถควบคุมใบรับรอง SSL ได้ละเอียดยิ่งขึ้น (ทั้งที่ลูกค้าเป็นเจ้าของและจัดการ Azure Front Door) และการเชื่อมโยงโดเมน</span><span class="sxs-lookup"><span data-stu-id="ed3f6-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="ed3f6-144">อินสแตนซ์จะเสนอโซลูชันของโดเมน apex ถ้าจับคู่กับ Azure DNS ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="ed3f6-145">มีบริการการส่งข้อมูลทางไกลและการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="ed3f6-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="ed3f6-146">ใบรับรอง SSL ต้องมีการตั้งค่าแบบใช้ครั้งเดียวและต่ออายุโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ed3f6-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="ed3f6-147">อินสแตนซ์เป็นแบบจัดการตัวเอง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="ed3f6-148">จำเป็นต้องมีการเพิ่มความรู้เบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="ed3f6-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="ed3f6-149">ภาพประกอบต่อไปนี้จะแสดงโครงสร้างพื้นฐานของ Commerce ที่มีอินสแตนซ์ Azure Front Door ที่ลูกค้าเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="ed3f6-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![โครงสร้างพื้นฐานของ Commerce ที่มีอินสแตนซ์ Azure Front Door ที่ลูกค้าเป็นเจ้าของ](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="ed3f6-151">ใช้บริการ CDN ภายนอก</span><span class="sxs-lookup"><span data-stu-id="ed3f6-151">Use an external CDN service</span></span>

<span data-ttu-id="ed3f6-152">ตารางต่อไปนี้จะแสดงรายการข้อดีและข้อเสียของการใช้บริการ CDN ภายนอกเพื่อจัดการเนื้อหาปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="ed3f6-153">ข้อดี</span><span class="sxs-lookup"><span data-stu-id="ed3f6-153">Pros</span></span> | <span data-ttu-id="ed3f6-154">ข้อเสีย</span><span class="sxs-lookup"><span data-stu-id="ed3f6-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="ed3f6-155">ตัวเลือกนี้มีประโยชน์เมื่อโดเมนที่มีอยู่โฮสต์บน CDN ภายนอกแล้ว</span><span class="sxs-lookup"><span data-stu-id="ed3f6-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="ed3f6-156">CDN คู่แข่ง (ตัวอย่างเช่น Akamai) อาจมีความสามารถ WAF มากกว่า</span><span class="sxs-lookup"><span data-stu-id="ed3f6-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="ed3f6-157">จำเป็นต้องระบุสัญญาที่แยกต่างหากและการคิดต้นทุนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ed3f6-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="ed3f6-158">SSL อาจก่อให้เกิดต้นทุนเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="ed3f6-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="ed3f6-159">เนื่องจากบริการนี้แยกต่างหากจากโครงสร้าง Cloud ของ Azure ต้องมีการจัดการโครงสร้างพื้นฐานเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ed3f6-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="ed3f6-160">บริการอาจต้องการใช้เวลาการลงทุนนานขึ้นในการตั้งค่าปลายทางและการรักษาความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="ed3f6-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="ed3f6-161">บริการเป็นแบบจัดการตัวเอง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-161">The service is self-managed.</span></span></li><li><span data-ttu-id="ed3f6-162">บริการเป็นแบบตรวจสอบตัวเอง</span><span class="sxs-lookup"><span data-stu-id="ed3f6-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="ed3f6-163">ภาพประกอบต่อไปนี้จะแสดงโครงสร้างพื้นฐานของ Commerce ที่รวมบริการ CDN ภายนอก</span><span class="sxs-lookup"><span data-stu-id="ed3f6-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![โครงสร้างพื้นฐานของ Commerce ที่รวมบริการ CDN ภายนอก](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="ed3f6-165">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ed3f6-165">Additional resources</span></span>

[<span data-ttu-id="ed3f6-166">เพิ่มการสนับสนุนสำหรับเครือข่ายการให้บริการเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="ed3f6-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
