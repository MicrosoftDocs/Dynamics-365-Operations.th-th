---
title: สถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง
description: หัวข้อนี้จะอธิบายสถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112528"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="a406b-103">สถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a406b-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a406b-104">คุณสามารถตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างสภาพแวดล้อม Finance and Operations และสภาพแวดล้อม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a406b-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="a406b-105">**สภาพแวดล้อม Finance and Operations** ให้แพลตฟอร์มพื้นฐานสำหรับ **แอป Finance and Operations** (ตัวอย่างเช่น Microsoft Dynamics 365 Finance Dynamics 365 Supply Chain Management Dynamics 365 Retail และ Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="a406b-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="a406b-106">**สภาพแวดล้อม Common Data Service** ให้แพลตฟอร์มพื้นฐานสำหรับ **แอปที่เป็นแบบโมเดลใน Dynamics 365** (Dynamics 365 Sales Dynamics 365 Customer Service Dynamics 365 Field Service Dynamics 365 Marketing และ Dynamics 365 Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="a406b-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="a406b-107">กลไกการตั้งค่าจะแตกต่างกันไป โดยขึ้นอยู่กับการบอกรับเป็นสมาชิกและสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="a406b-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="a406b-108">สำหรับอินสแตนซ์ใหม่ของแอป Finance and Operations การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a406b-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a406b-109">ถ้าคุณมีลิขสิทธิ์สำหรับ Microsoft Power Platform คุณจะได้รับสภาพแวดล้อม Common Data Service ใหม่ ถ้าผู้เช่าของคุณไม่มี</span><span class="sxs-lookup"><span data-stu-id="a406b-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="a406b-110">สำหรับแอป Finance and Operations ของอินสแตนซ์ที่มีอยู่ การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นในสภาพแวดล้อม Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a406b-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="a406b-111">มีการสนับสนุนสถานการณ์จำลองของการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a406b-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="a406b-112">อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่</span><span class="sxs-lookup"><span data-stu-id="a406b-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="a406b-113">อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a406b-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="a406b-114">อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูลสาธิต และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่</span><span class="sxs-lookup"><span data-stu-id="a406b-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="a406b-115">อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูลสาธิต และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a406b-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="a406b-116">อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่หรือที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a406b-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="a406b-117">อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่</span><span class="sxs-lookup"><span data-stu-id="a406b-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="a406b-118">เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่ไม่มีข้อมูลและอินสแตนซ์ใหม่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md)</span><span class="sxs-lookup"><span data-stu-id="a406b-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="a406b-119">เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="a406b-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="a406b-120">สภาพแวดล้อม Finance and Operations ที่ใหม่และว่างเปล่าถูกเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a406b-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="a406b-121">อินสแตนซ์ใหม่ที่ว่างเปล่าของแอปที่เป็นแบบโมเดลถูกเตรียมใช้งาน โดยที่มีการติดตั้งโซลูชันหลักของ CRM</span><span class="sxs-lookup"><span data-stu-id="a406b-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="a406b-122">มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT</span><span class="sxs-lookup"><span data-stu-id="a406b-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="a406b-123">มีการเปิดใช้งานแผนผังเอนทิตีสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="a406b-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="a406b-124">จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="a406b-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="a406b-125">อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a406b-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="a406b-126">เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่ไม่มีข้อมูลและอินสแตนซ์ที่มีอยู่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md)</span><span class="sxs-lookup"><span data-stu-id="a406b-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="a406b-127">เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="a406b-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="a406b-128">สภาพแวดล้อม Finance and Operations ที่ใหม่และว่างเปล่าถูกเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a406b-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="a406b-129">มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT</span><span class="sxs-lookup"><span data-stu-id="a406b-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="a406b-130">มีการเปิดใช้งานแผนผังเอนทิตีสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="a406b-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="a406b-131">จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="a406b-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="a406b-132">เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a406b-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a406b-133">สร้างบริษัทใหม่ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a406b-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="a406b-134">เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a406b-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="a406b-135">[เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัทองค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) แบบสามตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="a406b-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="a406b-136">เนื่องจากการรวมแบบสองทิศทางอยู่ในโหมดการซิงโครไนส์ที่เริ่มใช้งานจริง ข้อมูลจาก Common Data Service จะเริ่มต้นโฟลว์ไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a406b-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="a406b-137">อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูลสาธิต และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่</span><span class="sxs-lookup"><span data-stu-id="a406b-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="a406b-138">เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่มีข้อมูลสาธิต และอินสแตนซ์ใหม่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอป Finance and Operations ใหม่ อินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่](#new-new) ก่อนหน้าในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="a406b-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="a406b-139">เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลสาธิตไปที่แอปที่เป็นแบบโมเดล ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a406b-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="a406b-140">เปิดแอป Finance and Operations จากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="a406b-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="a406b-141">รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a406b-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="a406b-142">อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูลสาธิต และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a406b-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="a406b-143">เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่มีข้อมูลสาธิตและอินสแตนซ์ที่มีอยู่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่](#new-existing) ก่อนหน้าในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="a406b-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="a406b-144">เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลสาธิตไปที่แอปที่เป็นแบบโมเดล ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a406b-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="a406b-145">เปิดแอป Finance and Operations จากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="a406b-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="a406b-146">รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a406b-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="a406b-147">เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a406b-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a406b-148">สร้างบริษัทใหม่ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a406b-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="a406b-149">เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a406b-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="a406b-150">[เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัท ISO แบบสามตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="a406b-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="a406b-151">เนื่องจากการรวมแบบสองทิศทางอยู่ในโหมดการซิงโครไนส์ที่เริ่มใช้งานจริง ข้อมูลจาก Common Data Service จะเริ่มต้นโฟลว์ไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a406b-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="a406b-152">อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่หรือที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a406b-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="a406b-153">การตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ที่มีอยู่ของแอป Finance and Operations และอินสแตนซ์ใหม่หรืออินสแตนซ์ที่มีอยู่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 เกิดขึ้นในสภาพแวดล้อม Finance and Operation</span><span class="sxs-lookup"><span data-stu-id="a406b-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="a406b-154">ตั้งค่าการเชื่อมต่อจากแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a406b-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="a406b-155">เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัท ISO แบบอักษรสามตัว</span><span class="sxs-lookup"><span data-stu-id="a406b-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="a406b-156">เนื่องจากการรวมแบบสองทิศทางอยู่ในโหมดการซิงโครไนส์ที่เริ่มใช้งานจริง ข้อมูลจาก Common Data Service จะเริ่มต้นโฟลว์ไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a406b-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
