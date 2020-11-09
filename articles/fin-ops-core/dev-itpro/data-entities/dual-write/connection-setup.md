---
title: คำแนะนำเกี่ยวกับวิธีการตั้งค่าการรวมแบบสองทิศทาง
description: หัวข้อนี้จะอธิบายสถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088517"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="63226-103">คำแนะนำเกี่ยวกับวิธีการตั้งค่าการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="63226-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="63226-104">คุณสามารถตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างสภาพแวดล้อม Finance and Operations และสภาพแวดล้อม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="63226-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="63226-105">**สภาพแวดล้อม Finance and Operations** มีแพลตฟอร์มพื้นฐานสำหรับ **แอป Finance and Operations** (ตัวอย่างเช่น Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management และ Dynamics 365 Retail)</span><span class="sxs-lookup"><span data-stu-id="63226-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="63226-106">**สภาพแวดล้อม Common Data Service** ให้แพลตฟอร์มพื้นฐานสำหรับ **แอป Customer Engagement** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing และ Dynamics 365 Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="63226-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="63226-107">Human Resources ใน Finance and Operations รองรับการเชื่อมต่อการรวมแบบสองทิศทาง แต่แอป Dynamics 365 Human Resources ไม่รองรับ</span><span class="sxs-lookup"><span data-stu-id="63226-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="63226-108">กลไกการตั้งค่าจะแตกต่างกันไป โดยขึ้นอยู่กับการบอกรับเป็นสมาชิกและสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="63226-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="63226-109">สำหรับอินสแตนซ์ใหม่ของแอป Finance and Operations การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="63226-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="63226-110">ถ้าคุณมีลิขสิทธิ์สำหรับ Power Platform คุณจะได้รับสภาพแวดล้อม Common Data Service ใหม่ ถ้าผู้เช่าของคุณไม่มี</span><span class="sxs-lookup"><span data-stu-id="63226-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="63226-111">สำหรับแอป Finance and Operations ของอินสแตนซ์ที่มีอยู่ การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นในสภาพแวดล้อม Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63226-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="63226-112">ก่อนที่คุณจะเริ่มต้นการรวมแบบสองทิศทางบนเอนทิตี คุณสามารถรันการซิงค์เริ่มต้นเพื่อจัดการกับข้อมูลที่มีอยู่ในทั้งสองด้านของแอป Finance and Operations และแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="63226-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="63226-113">คุณสามารถข้ามการซิงค์เริ่มต้น ถ้าคุณไม่ต้องการซิงโครไนส์ข้อมูลระหว่างสองสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="63226-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="63226-114">การซิงค์เริ่มต้นช่วยให้คุณสามารถคัดลอกข้อมูลที่มีอยู่จากแอปหนึ่งไปยังอีกแอปหนึ่งแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="63226-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="63226-115">มีสถานการณ์จำลองการตั้งค่าที่แตกต่างกันหลายสถานการณ์ โดยขึ้นอยู่กับสภาพแวดล้อมที่คุณมีอยู่แล้วและชนิดของข้อมูลที่อยู่ในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="63226-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="63226-116">มีการสนับสนุนสถานการณ์จำลองของการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="63226-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="63226-117">อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอป Customer Engagement ใหม่</span><span class="sxs-lookup"><span data-stu-id="63226-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="63226-118">อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="63226-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="63226-119">อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูล และอินสแตนซ์ของแอป Customer Engagement ใหม่</span><span class="sxs-lookup"><span data-stu-id="63226-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="63226-120">อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูล และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="63226-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="63226-121">อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอป Customer Engagement ใหม่</span><span class="sxs-lookup"><span data-stu-id="63226-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="63226-122">อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="63226-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="63226-123">อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอป Customer Engagement ใหม่</span><span class="sxs-lookup"><span data-stu-id="63226-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="63226-124">เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่ไม่มีข้อมูล และอินสแตนซ์ใหม่ของแอป Customer Engagement ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md)</span><span class="sxs-lookup"><span data-stu-id="63226-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="63226-125">เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="63226-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="63226-126">สภาพแวดล้อม Finance and Operations ที่ใหม่และว่างเปล่าถูกเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="63226-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="63226-127">อินสแตนซ์ใหม่ที่ว่างเปล่าของแอป Customer Engagement ถูกเตรียมใช้งาน โดยที่มีการติดตั้งโซลูชันหลักของ CRM</span><span class="sxs-lookup"><span data-stu-id="63226-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="63226-128">มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT</span><span class="sxs-lookup"><span data-stu-id="63226-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="63226-129">มีการเปิดใช้งานแผนผังเอนทิตีสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="63226-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="63226-130">จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="63226-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="63226-131">อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="63226-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="63226-132">เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่ไม่มีข้อมูล และอินสแตนซ์ที่มีอยู่ของแอป Customer Engagement ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md)</span><span class="sxs-lookup"><span data-stu-id="63226-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="63226-133">เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="63226-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="63226-134">สภาพแวดล้อม Finance and Operations ที่ใหม่และว่างเปล่าถูกเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="63226-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="63226-135">มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT</span><span class="sxs-lookup"><span data-stu-id="63226-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="63226-136">มีการเปิดใช้งานแผนผังเอนทิตีสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="63226-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="63226-137">จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="63226-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="63226-138">เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="63226-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="63226-139">สร้างบริษัทใหม่ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63226-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="63226-140">เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="63226-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="63226-141">[เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัทองค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) แบบสามตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="63226-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="63226-142">รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63226-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="63226-143">สำหรับตัวอย่างและแนวทางเลือก ให้ดูที่ [ตัวอย่าง](#example)</span><span class="sxs-lookup"><span data-stu-id="63226-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="63226-144">อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูล และอินสแตนซ์ของแอป Customer Engagement ใหม่</span><span class="sxs-lookup"><span data-stu-id="63226-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="63226-145">เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่มีข้อมูล และอินสแตนซ์ใหม่ของแอป Customer Engagement ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอป Finance and Operations ใหม่ อินสแตนซ์ของแอป Customer Engagement ใหม่](#new-new) ก่อนหน้าในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="63226-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="63226-146">เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลไปที่แอป Customer Engagement ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="63226-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="63226-147">เปิดแอป Finance and Operations จากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="63226-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="63226-148">รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63226-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="63226-149">สำหรับตัวอย่างและแนวทางเลือก ให้ดูที่ [ตัวอย่าง](#example)</span><span class="sxs-lookup"><span data-stu-id="63226-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="63226-150">อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูล และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="63226-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="63226-151">เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่มีข้อมูล และอินสแตนซ์ใหที่มีอยู่ของแอป Customer Engagement ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอป Finance and Operations ใหม่ อินสแตนซ์ของแอป Customer Engagement ที่มีอยู่](#new-existing) ก่อนหน้าในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="63226-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="63226-152">เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลไปที่แอป Customer Engagement ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="63226-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="63226-153">เปิดแอป Finance and Operations จากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="63226-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="63226-154">รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63226-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="63226-155">เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="63226-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="63226-156">สร้างบริษัทใหม่ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63226-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="63226-157">เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="63226-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="63226-158">[เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัท ISO แบบสามตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="63226-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="63226-159">รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63226-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="63226-160">สำหรับตัวอย่างและแนวทางเลือก ให้ดูที่ [ตัวอย่าง](#example)</span><span class="sxs-lookup"><span data-stu-id="63226-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="63226-161">อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอป Customer Engagement ใหม่</span><span class="sxs-lookup"><span data-stu-id="63226-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="63226-162">การตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ที่มีอยู่ของแอป Finance and Operations และอินสแตนซ์ใหม่ของแอป Customer Engagement ที่เกิดขึ้นในสภาพแวดล้อม Finance and Operation</span><span class="sxs-lookup"><span data-stu-id="63226-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="63226-163">[ตั้งค่าการเชื่อมต่อจากแอป Finance and Operations](enable-dual-write.md)</span><span class="sxs-lookup"><span data-stu-id="63226-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="63226-164">รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63226-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="63226-165">สำหรับตัวอย่างและแนวทางเลือก ให้ดูที่ [ตัวอย่าง](#example)</span><span class="sxs-lookup"><span data-stu-id="63226-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="63226-166">อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="63226-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="63226-167">การตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ที่มีอยู่ของแอป Finance and Operations และอินสแตนซ์ที่มีอยู่ของแอป Customer Engagement ที่เกิดขึ้นในสภาพแวดล้อม Finance and Operation</span><span class="sxs-lookup"><span data-stu-id="63226-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="63226-168">ตั้งค่าการเชื่อมต่อจากแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63226-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="63226-169">เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัท ISO แบบอักษรสามตัว</span><span class="sxs-lookup"><span data-stu-id="63226-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="63226-170">รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63226-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="63226-171">สำหรับตัวอย่างและแนวทางเลือก ให้ดูที่ [ตัวอย่าง](#example)</span><span class="sxs-lookup"><span data-stu-id="63226-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="63226-172">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="63226-172">Example</span></span>

<span data-ttu-id="63226-173">สำหรับตัวอย่างเช่น ให้ดูที่ [การเปิดใช้งานลูกค้า V3 —แผนผังเอนทิตีของผู้ติดต่อ](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="63226-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="63226-174">สำหรับแนวทางอื่นที่ยึดตามปริมาณข้อมูลในแต่ละเอนทิตีที่ต้องรันการซิงค์เริ่มต้น ให้ดูที่ [ข้อควรพิจารณาสำหรับการซิงโครไนส์เริ่มต้น](initial-sync-guidance.md)</span><span class="sxs-lookup"><span data-stu-id="63226-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
