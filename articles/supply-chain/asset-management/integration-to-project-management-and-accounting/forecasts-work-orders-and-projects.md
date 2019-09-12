---
title: การคาดการณ์ ใบสั่งงาน และโครงการ
description: หัวข้อนี้อธิบายการคาดการณ์และการรวมใบสั่งงานกับโมดูลการจัดการและการบัญชีโครงการในการบริหารสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886827"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="3125f-103">การคาดการณ์ ใบสั่งงาน และโครงการ</span><span class="sxs-lookup"><span data-stu-id="3125f-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3125f-104">ในการบริหารสินทรัพย์ การรวมกับโมดูล **การจัดการและการบัญชีโครงการ** เพื่อเพิ่มประสิทธิภาพของการควบคุมต้นทุน ทำให้ผู้ใช้สามารถติดตามต้นทุนในงานการคาดการ์ชนิดงานบำรุงรักษาและใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="3125f-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="3125f-105">การติดตามการคาดการณ์ชนิดงานบำรุงรักษษ ต้องทำการตั้งค่าสองอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3125f-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="3125f-106">เลือกโครงการในฟิลด์ **การจัดการสินทรัพย์** > **การตั้งค่า** > **พาริมิเตอร์การจัดการสินทรัพย์** > **สินทรัพย์** ลิงก์ > **โครงการ** แท็บด่วน > **โครงการการคาดการณ์ในการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="3125f-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="3125f-107">ใน **ค่าเริ่มต้นของชนิดงานบำรุงรักษา** เมื่อคุณสร้างรายการค่าเริ่มต้นของชนิดงานบำรุงรักษา หมายเลขกิจกรรมจะมีการสร้างขึ้นโดยอัตโนมัติ (**การจัดการสินทรัพย์** > **การตั้งค่า** > **งาน** > **ค่าเริ่มต้นของชนิดงานบำรุงรักษา**)</span><span class="sxs-lookup"><span data-stu-id="3125f-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="3125f-108">การคาดการณ์ชนิดงานการบำรุงรักษามีสองจุดประสงค์: คุณสามารถติดตามต้นทุนการคาดการณ์ชนิดงานการบำรุงรักษาในโมดูล **การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3125f-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="3125f-109">นอกจากนี้ การคาดการณ์จะถูกโอนย้ายไปยังโครงการงานใบสั่งงานโดยอัตโนมัติ เมื่อคุณเลือกชนิดงานการบำรุงรักษาในงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="3125f-110">การติดตามต้นทุนของงานใบสั่งงาน คุณต้องตั้งค่าโครงการใบสั่งงานก่อน</span><span class="sxs-lookup"><span data-stu-id="3125f-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="3125f-111">อ้างอิงถึงส่วน [การตั้งค่าโครงการของใบสั่งงาน](../setup-for-work-orders/work-order-project-setup.md) สำหรับคำอธิบายของขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="3125f-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="3125f-112">โครงการของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-112">Work order job projects</span></span>

<span data-ttu-id="3125f-113">เมื่อคุณสร้างงานใบสั่งงานในใบสั่งงาน โครงการของใบสั่งงานจะขึ้นอยู่กับการตั้งค่าของโครงการหลักสำหรับใบสั่งงาน ใน **การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **การตั้งค่าโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3125f-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="3125f-114">โครงการงานใบสั่งงานจะถูกสร้างขึ้นโดยใช้การรวมกันของข้อมูลใบสั่งงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3125f-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="3125f-115">ชนิดของใบสั่งงานที่เลือกบนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="3125f-116">ตำแหน่งที่ทำงานที่เกี่ยวข้องกับสินทรัพย์บนงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="3125f-117">ชนิดสินทรัพย์ที่เกี่ยวข้องกับสินทรัพย์บนงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="3125f-118">เวลาเริ่มต้นและเวลาสิ้นสุดที่คาดการณ์ที่ตั้งค่าไว้ในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="3125f-119">มีความเป็นไปได้ว่าข้อมูลทั้งหมดที่กล่าวถึงข้างต้นจะพบในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="3125f-120">ดังนั้น การค้นหาสำหรับโครงการหลักของใบสั่งงานจะทำโดยใช้ชุดข้อมูลที่พร้อมใช้งาน และเลือกรหัสโครงการที่สอดคล้องกับข้อมูลใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="3125f-121">ตัวอย่าง: ในรูปด้านล่าง การตั้งค่าชนิดของสินทรัพย์ "เครื่องยนต์รถบรรทุก" หมายความว่างานใบสั่งงานทั้งหมดที่สร้างขึ้นโดยชนิดสินทรัพย์นั้น จะเป็นโครงการย่อยของรหัสโครงการ "000186"</span><span class="sxs-lookup"><span data-stu-id="3125f-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![รูปที่ 1](media/01-integration-to-pma.png)

<span data-ttu-id="3125f-123">วัตถุประสงค์ของรหัสโครงการบนงานใบสั่งงานและหมายเลขกิจกรรมที่เกี่ยวข้อง (**การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** > เลือกใบสั่งงานในรายการฟิลด์ > **รายละเอียดของรายการ** แท็บด่วน > **รหัสโครงการ** และฟิลด์ **หมายเลขกิจการรม**) คือการติดตามต้นทุนที่เกี่ยวข้องกับงานใบสั่งงาน และสินทรัพย์ที่เลือกบนงานใบสั่งงานในโมดูล **การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3125f-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="3125f-124">ในรูปด้านล่าง คุณจะเห็นภาพรวมของโครงการใบสั่งงานและกิจกรรมโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3125f-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![รูปที่ 2](media/02-integration-to-pma.png)

<span data-ttu-id="3125f-126">เมื่อสร้างงานใบสั่งงานใหม่ในใบสั่งงาน โครงการของใบสั่งงานสำหรับงานจะถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3125f-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="3125f-127">มิติทางการเงินสำหรับสินทรัพย์ที่เกี่ยวข้องกับงานของใบสั่งงาน จะถูกโอนย้ายโดยอัตโนมัติไปยังโครงการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="3125f-128">กิจกรรมโครงการที่สร้างขึ้นสำหรับงานใบสั่งงานมีข้อมูลที่เกี่ยวข้องแนบไปด้วย เกี่ยวข้องกับชนิดงานการบำรุงรักษา ตัวแปรชนิดงานบำรุงรักษาและการค้า</span><span class="sxs-lookup"><span data-stu-id="3125f-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="3125f-129">ข้อมูลเหล่านี้มีประโยชน์หากว่า ตัวอย่างเช่น คุณสร้างใบสั่งซื้อจากใบสั่งงาน (ดู [การจัดซื้อ](../work-orders/procurement.md)) หรือหากคุณใช้โมดูล **การจัดการและการบัญชีโครงการ** สำหรับการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="3125f-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="3125f-130">ถ้ามีการติดตั้งสินทรัพย์ในตำแหน่งที่ทำงาน และมีการติดตั้งสินทรัพย์ดังกล่าวในตำแหน่งที่ทำงานอื่นในภายหลัง มิติทางการเงินที่เกี่ยวข้องกับตำแหน่งที่ทำงานใหม่จะมีการอัพเดตโดยอัตโนมัติในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="3125f-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="3125f-131">หลังจากนั้น เมื่อคุณสร้างงานในใบสั่งงานสำหรับสินทรัพย์ โครงการของใบสั่งงานสำหรับงานใบสั่งงานจะได้รับมิติทางการเงินที่เกี่ยวข้องกับสินทรัพย์นี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3125f-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="3125f-132">ซึ่งหมายความว่าเมื่อคุณใช้ตำแหน่งที่ทำงาน ต้นทุนสามารถติดตามจากตำแหน่งที่ทำงานที่มีการติดตั้งสินทรัพย์ที่ไหนก็ได้ตามเวลาที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="3125f-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="3125f-133">การอัพเดทอัตโนมัติของมิติทางการเงินจะช่วยให้การตรวจสอบความถูกต้องของต้นทุนที่สมบูรณ์ สำหรับการควบคุมและการรายงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="3125f-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="3125f-134">โครงการใบสั่งงาน สถานะวงจรของใบสั่งงาน ขั้นโครงการ และชนิดโครงการ</span><span class="sxs-lookup"><span data-stu-id="3125f-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="3125f-135">การตรวจสอบให้แน่ใจว่ามีการใช้สถานะวงจรของใบสั่งงานและขั้นโครงการที่เกี่ยวข้องในใบสั่งงานอย่างถูกต้อง ให้พิจารณาการอ้างอิงที่เกี่ยวข้องกับโมดูล **การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3125f-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="3125f-136">ในโมดูล **การจัดการและการบัญชีโครงการ** ขั้นโครงการจะมีการตั้งค่าบนชนิดโครงการใน **พารามิเตอร์การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3125f-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="3125f-137">ใน **พารามิเตอร์การจัดการและการบัญชีโครงการ** อย่าลืมเลือกกล่องกาเครื่องหมายขั้นโครงการที่เกี่ยวข้อง สำหรับชนิดโครงการทั้งหมดที่คุณกำลังจะใช้</span><span class="sxs-lookup"><span data-stu-id="3125f-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="3125f-138">ในรูปด้านล่าง ห้าขั้นที่ **สร้างขึ้น** - **โดยประมาณ** - **กำหนดการ** - **ในกระบวนการ** - **เสร็จสิ้น** ได้ถูกเลือกสำหรับชนิดโครงการ "เวลาและวัสดุ" และ "ภายใน"</span><span class="sxs-lookup"><span data-stu-id="3125f-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="3125f-139">ขั้นห้าเหล่านี้เกี่ยวข้องกับทั้งงานบำรุงรักษาภายในและการบริการงานบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="3125f-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="3125f-140">ใน **การบริหารสินทรัพย์**ชนิดโครงการจะถูกกำหนดโดยกลุ่มโครงการที่คุณตั้งค่าไว้ใน ฟอร์ม **การตั้งค่าโครงการ** > **กลุ่มโครงการ** ลิงค์</span><span class="sxs-lookup"><span data-stu-id="3125f-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="3125f-141">การตั้งค่ากลุ่มโครงการ ใน **การตั้งค่าโครงการของใบสั่งงาน** จะถูกใช้เมื่อคุณสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="3125f-142">เมื่อใบสั่งงานถูกสร้าง โครงการของใบสั่งงานจะถูกสร้างขึ้นโดยอัตโนมัติสำหรับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="3125f-143">แต่ละสถานะวงจรใบสั่งงานต้องมีขั้นโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3125f-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="3125f-144">ขั้นโครงการที่เกี่ยวข้องกับสถานะวงจรของใบสั่งงาน ต้องถูกกำหนดเป็นขั้นที่ใช้งานอยู่สำหรับกลุ่มโครงการที่กำหนดไว้ในโครงการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="3125f-145">โครงการของใบสั่งงานจะถูกสร้างขึ้นโดยอัตโนมัติบนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="3125f-146">เมื่อคุณสร้างใบสั่งงานใหม่ การจัดสรรโดยอัตโนมัติของโครงการของใบสั่งงานจะขึ้นอยู่กับการตั้งค่า ใน **การตั้งค่าโครงการของใบสั่งงาน** (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **การตั้งค่าโครงการ**)</span><span class="sxs-lookup"><span data-stu-id="3125f-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="3125f-147">ความสัมพันธ์ระหว่างกลุ่มโครงการของใบสั่งงาน ชนิดโครงการที่เกี่ยวข้อง ขั้นโครงการ และสถานะวงจรใบสั่งงาน จะแสดงอยู่ในรูปด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="3125f-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![รูปที่ 3](media/03-integration-to-pma.png)

![รูปที่ 4](media/04-integration-to-pma.png)

![รูปที่ 5](media/05-integration-to-pma.png)

<span data-ttu-id="3125f-151">อ้างถึง [การตั้งค่าโครงการของใบสั่งงาน](../setup-for-work-orders/work-order-project-setup.md) ที่เกี่ยวข้องกับวิธีการตั้งค่าโครงการของใบสั่งงาน และ [สถานะวงจรของใบสั่งงาน](../setup-for-work-orders/work-order-lifecycle-states.md) เกี่ยวกับวิธีการสร้างสถานะวงจรของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3125f-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="3125f-152">รูปด้านล่างแสดงภาพรวมของโครงการต่างๆ ที่สร้างขึ้นในโมดูล **การจัดการสินทรัพย์** เพื่ออนุญาตให้มีการรวมกับโมดูล **การจัดการและการบัญชีโครงการ** รวมถึงกระบวนการทำงานที่ โครงการเกี่ยวข้องด้วย</span><span class="sxs-lookup"><span data-stu-id="3125f-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![รูปที่ 6](media/06-integration-to-pma.png)

