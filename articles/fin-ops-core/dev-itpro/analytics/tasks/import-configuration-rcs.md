---
title: (ER) นำเข้าการตั้งค่าคอนฟิกจาก RCS
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการที่ผู้ใช้สามารถนำเข้าการตั้งค่าคอนฟิก ER รุ่นใหม่จาก RCS
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32c9c17d8b63e4c0806559c2dcc2e11ae9825a53
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184634"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="bbb36-103">(ER) นำเข้าการตั้งค่าคอนฟิกจาก RCS</span><span class="sxs-lookup"><span data-stu-id="bbb36-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbb36-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) รุ่นใหม่จาก Microsoft Regulatory Configuration Services (RCS)</span><span class="sxs-lookup"><span data-stu-id="bbb36-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="bbb36-105">ในตัวอย่างนี้ คุณจะเลือกรุ่นของการตั้งค่าคอนฟิก ER ที่ได้รับการตั้งค่าคอนฟิกในอินสแตนซ์ RCS และนำเข้าไปยังอินสแตนซ์ปัจจุบันสำหรับบริษัทตัวอย่าง Litware, Inc ขั้นตอนเหล่านี้สามารถดำเนินการได้ในบริษัทใดๆ เนื่องจากมีการใช้การตั้งค่าคอนฟิก ER ร่วมกันระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="bbb36-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="bbb36-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในหัวข้อให้เสร็จสมบูรณ์ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="bbb36-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="bbb36-107">เมื่อต้องการทำขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ คุณยังต้องมีสิทธิเข้าถึงอินสแตนซ์ RCS ที่มีการตั้งค่าคอนฟิก ER อย่างน้อยหนึ่งรายการในสถานะ **เสร็จสมบูรณ์** หรือ **ที่ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="bbb36-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="bbb36-108">ไปที่ **การจัดการองค์กร** > **พื้นที่ทำงาน** > **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="bbb36-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="bbb36-109">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="bbb36-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="bbb36-110">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในหัวข้อให้สำเร็จ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="bbb36-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="bbb36-111">ถ้าคุณไม่มีสภาพแวดล้อม RCS ที่จัดสรรให้กับบริษัทของคุณ ให้คลิกที่ลิงค์ภายนอก **Regulatory services – การตั้งค่าคอนฟิก** และทำตามคำแนะนำเพื่อจัดเตรียมสภาพแวดล้อม RCS</span><span class="sxs-lookup"><span data-stu-id="bbb36-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="bbb36-112">คลิกที่ **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="bbb36-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="bbb36-113">คลิกแท็บ **RCS**</span><span class="sxs-lookup"><span data-stu-id="bbb36-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="bbb36-114">ถ้ามีการจัดสรรสภาพแวดล้อม RCS ให้กับบริษัทของคุณแล้ว ให้ใช้รายการที่แสดงบน URLs ของหน้าเพื่อเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="bbb36-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="bbb36-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bbb36-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="bbb36-116">ลงทะเบียนที่จัดเก็บ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="bbb36-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="bbb36-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bbb36-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="bbb36-118">เลือกผู้ให้บริการ Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="bbb36-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="bbb36-119">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="bbb36-119">Click Repositories.</span></span> 
4. <span data-ttu-id="bbb36-120">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bbb36-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="bbb36-121">ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก ป้อน 'RCS'</span><span class="sxs-lookup"><span data-stu-id="bbb36-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="bbb36-122">คลิกสร้างที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="bbb36-122">Click Create repository.</span></span> 
7. <span data-ttu-id="bbb36-123">ในฟิลด์ชื่อที่แสดงสภาพแวดล้อม RCS ให้ป้อน หรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bbb36-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="bbb36-124">เลือกอินสแตนซ์ RCS ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bbb36-124">Select the desired RCS instance.</span></span> <span data-ttu-id="bbb36-125">โปรดทราบว่าคุณสามารถมีได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="bbb36-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="bbb36-126">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="bbb36-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="bbb36-127">นำเข้าการตั้งค่าคอนฟิก ER จากที่เก็บที่ยึดตาม RCS</span><span class="sxs-lookup"><span data-stu-id="bbb36-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="bbb36-128">คลิก **แสดงตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="bbb36-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="bbb36-129">ป้อนค่าตัวกรองของ "RCS" ในฟิลด์ **ชื่อ** โดยใช้ตัวดำเนินการกรอง **เริ่มต้นด้วย**</span><span class="sxs-lookup"><span data-stu-id="bbb36-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="bbb36-130">เมื่อคุณเปิดที่เก็บที่เลือกบนหน้า **เชื่อมต่อกับ Regulatory Configuration Services** คลิกที่ลิงค์ **คลิกที่นี่เพื่อเชื่อมต่อกับ Regulatory Configuration Services**</span><span class="sxs-lookup"><span data-stu-id="bbb36-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="bbb36-131">คลิก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bbb36-131">Click **Open**.</span></span> 
5. <span data-ttu-id="bbb36-132">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bbb36-132">Click **Close**.</span></span> 
6. <span data-ttu-id="bbb36-133">เลือกการตั้งค่าคอนฟิก ER รุ่นที่ต้องการ และคลิก **นำเข้า** เพื่อนำมาใช้ในอินสแตนซ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bbb36-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

