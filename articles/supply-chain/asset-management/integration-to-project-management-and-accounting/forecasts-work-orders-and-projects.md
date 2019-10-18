---
title: การคาดการณ์ ใบสั่งงาน และโครงการ
description: หัวข้อนี้อธิบายการคาดการณ์และการรวมใบสั่งงานกับโมดูลการจัดการและการบัญชีโครงการในการบริหารสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/29/2019
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
ms.openlocfilehash: cc1992326c448ee8dc30a9ad8f8f538ebea83e54
ms.sourcegitcommit: f853c8d46ffc8e578387bac4cd48a948916983ef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/19/2019
ms.locfileid: "2002395"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="31691-103">การคาดการณ์ ใบสั่งงาน และโครงการ</span><span class="sxs-lookup"><span data-stu-id="31691-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="31691-104">ในการบริหารสินทรัพย์ การรวมกับโมดูล **การจัดการและการบัญชีโครงการ** ช่วยเพิ่มประสิทธิภาพของการควบคุมต้นทุน เพื่อให้ผู้ใช้สามารถติดตามต้นทุนในงานการคาดการณ์ชนิดงานบำรุงรักษาและใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="31691-104">In Asset Management, integration with the **Project management and accounting** module helps optimize cost control, so that users can track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="31691-105">การติดตามการคาดการณ์ชนิดงานบำรุงรักษาต้องทำการตั้งค่าสองอย่าง:</span><span class="sxs-lookup"><span data-stu-id="31691-105">Tracking of maintenance job type forecasts requires two settings:</span></span>

1. <span data-ttu-id="31691-106">เลือกโครงการใน **การจัดการสินทรัพย์** > **การตั้งค่า** > **พารามิเตอร์การจัดการสินทรัพย์** แล้วจากนั้น บนแท็บ **สินทรัพย์** > บน FastTab **โครงการ** ในฟิลด์ **โครงการการคาดการณ์การบำรุงรักษา** ให้เลือกโครงการ</span><span class="sxs-lookup"><span data-stu-id="31691-106">Select a project in **Asset management** > **Setup** > **Asset management parameters**, and then, on the **Assets** tab > on the **Project** FastTab, in the **Maintenance forecast project** field, select a project.</span></span>

2. <span data-ttu-id="31691-107">เมื่อคุณสร้าง รายการค่าเริ่มต้นของชนิดงานบำรุงรักษา หมายเลขกิจกรรมจะมีการสร้างขึ้นโดยอัตโนมัติสำหรับรายการในหน้า **ค่าเริ่มต้นของชนิดงานบำรุงรักษา** (**การจัดการสินทรัพย์** > **การตั้งค่า** > **งาน** > **ค่าเริ่มต้นของชนิดงานบำรุงรักษา**)</span><span class="sxs-lookup"><span data-stu-id="31691-107">When you create a maintenance job type default line, an activity number is automatically created for the line on the **Maintenance job type defaults** page (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="31691-108">การคาดการณ์ชนิดงานการบำรุงรักษาใช้สองจุดประสงค์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="31691-108">Maintenance job type forecasts serve two purposes:</span></span> 

- <span data-ttu-id="31691-109">คุณสามารถติดตามต้นทุนในการคาดการณ์ชนิดงานบำรุงรักษาได้ในโมดูล **การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="31691-109">You can track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> 
- <span data-ttu-id="31691-110">การคาดการณ์จะถูกโอนย้ายไปยังโครงการงานใบสั่งงานโดยอัตโนมัติ เมื่อคุณเลือกชนิดงานบำรุงรักษาในงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-110">Forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="31691-111">การติดตามต้นทุนของงานใบสั่งงาน คุณต้องตั้งค่าโครงการใบสั่งงานก่อน</span><span class="sxs-lookup"><span data-stu-id="31691-111">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="31691-112">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การตั้งค่าโครงการใบสั่งงาน](../setup-for-work-orders/work-order-project-setup.md)</span><span class="sxs-lookup"><span data-stu-id="31691-112">For more information, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="31691-113">โครงการของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-113">Work order job projects</span></span>

<span data-ttu-id="31691-114">เมื่อคุณสร้างงานใบสั่งงานในใบสั่งงาน โครงการของใบสั่งงานจะขึ้นอยู่กับการตั้งค่าของโครงการหลักสำหรับใบสั่งงานในหน้า **การตั้งค่าโครงการใบสั่งงาน** (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **การตั้งค่าโครงการ**)</span><span class="sxs-lookup"><span data-stu-id="31691-114">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders on the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>

<span data-ttu-id="31691-115">โครงการงานใบสั่งงานจะถูกสร้างขึ้นโดยใช้การรวมกันของข้อมูลใบสั่งงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="31691-115">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="31691-116">ชนิดของใบสั่งงานที่เลือกบนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-116">The work order type selected on the work order</span></span> 
- <span data-ttu-id="31691-117">ตำแหน่งที่ทำงานที่เกี่ยวข้องกับสินทรัพย์บนงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-117">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="31691-118">ชนิดสินทรัพย์ที่เกี่ยวข้องกับสินทรัพย์บนงานในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-118">The asset type that is related to the asset on the work order job</span></span>  
- <span data-ttu-id="31691-119">เวลาเริ่มต้นและเวลาสิ้นสุดที่คาดการณ์ที่ตั้งค่าไว้ในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-119">The expected start and end times that are set on the work order</span></span>  

<span data-ttu-id="31691-120">อาจไม่พบข้อมูลบางอย่างในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-120">Some of this information might not be found on a work order.</span></span> <span data-ttu-id="31691-121">ดังนั้น การค้นหาสำหรับโครงการหลักของใบสั่งงานจะทำโดยการใช้ชุดข้อมูลที่พร้อมใช้งาน และการเลือกรหัสโครงการที่สอดคล้องกับข้อมูลใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-121">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds to work order data.</span></span>

<span data-ttu-id="31691-122">ตัวอย่างเช่น ในภาพประกอบต่อไปนี้ เนื่องจากวิธีที่ชนิดของสินทรัพย์ **เครื่องยนต์รถบรรทุก** ถูกตั้งค่า งานในใบสั่งงานทั้งหมดที่สร้างขึ้นด้วยชนิดสินทรัพย์ **เครื่องยนต์รถบรรทุก** จะเป็นโครงการย่อยของรหัสโครงการ 000186</span><span class="sxs-lookup"><span data-stu-id="31691-122">For example, in the following illustration, because of the way that the **Truck Engine** asset type is set up, every work order job that is created with the **Truck Engine** asset type will be a sub-project of project ID 000186.</span></span>

![รูปที่ 1](media/01-integration-to-pma.png)

<span data-ttu-id="31691-124">วัตถุประสงค์ของรหัสโครงการบนงานในใบสั่งงานและหมายเลขกิจกรรมที่เกี่ยวข้องคือ การติดตามต้นทุนที่เกี่ยวข้องกับงานในใบสั่งงานและสินทรัพย์ที่เลือกไว้ ในโมดูล **การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="31691-124">The purpose of the project ID on the work order job, and the related activity number, is to track costs that are related to the work order job, and the asset that is selected on it, in the **Project management and accounting** module.</span></span> <span data-ttu-id="31691-125">(ถ้าต้องการดูรหัสโครงการและหมายเลขกิจกรรม ให้เลือก **การบริหารสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** แล้วจากนั้น เลือกใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-125">(To view the project ID and activity number, select **Asset management** > **Common** > **Work orders** > **All work orders**, and then select the work order.</span></span> <span data-ttu-id="31691-126">บน FastTab **รายละเอียดของรายการ** ฟิลด์ **รหัสโครงการ** แสดงรหัสโครงการและฟิลด์ **หมายเลขกิจกรรม** จะแสดงหมายเลขกิจกรรม) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการควบคุมต้นทุนในการบริหารสินทรัพย์ โปรดดู [การควบคุมต้นทุนและวันที่](../controlling-and-reporting/cost-and-date-control.md)</span><span class="sxs-lookup"><span data-stu-id="31691-126">On the **Line details** FastTab, the **Project ID** field shows the project ID, and the **Activity number** field shows the activity number.) For more information about cost control in Asset Management, see [Cost and date control](../controlling-and-reporting/cost-and-date-control.md).</span></span>

<span data-ttu-id="31691-127">ภาพประกอบต่อไปนี้แสดงภาพรวมแบบกราฟิกของโครงการใบสั่งงานและกิจกรรมโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="31691-127">The following illustration shows a graphical overview of work order projects and related project activities.</span></span>

![รูปที่ 2](media/02-integration-to-pma.png)

<span data-ttu-id="31691-129">เมื่อสร้างงานใบสั่งงานใหม่ในใบสั่งงาน โครงการของใบสั่งงานสำหรับงานจะถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="31691-129">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="31691-130">มิติทางการเงินสำหรับสินทรัพย์ที่เกี่ยวข้องกับงานในใบสั่งงาน จะถูกโอนย้ายโดยอัตโนมัติไปยังโครงการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-130">The financial dimensions for the asset that is related to the work order job are automatically transferred to the work order project.</span></span>

<span data-ttu-id="31691-131">กิจกรรมโครงการที่สร้างขึ้นสำหรับงานในใบสั่งงานมีข้อมูลที่เกี่ยวข้องแนบอยู่</span><span class="sxs-lookup"><span data-stu-id="31691-131">The project activity that is created for a work order job has related information attached to it.</span></span> <span data-ttu-id="31691-132">ข้อมูลนี้เกี่ยวกับชนิดงานบำรุงรักษา ตัวแปรชนิดงานบำรุงรักษา และการค้า</span><span class="sxs-lookup"><span data-stu-id="31691-132">This information is about the maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="31691-133">ข้อมูลเหล่านี้มีประโยชน์ หากว่า ตัวอย่างเช่น คุณสร้างใบสั่งซื้อจากใบสั่งงาน (ดู [การจัดซื้อ](../work-orders/procurement.md)) หรือหากคุณใช้โมดูล **การจัดการและการบัญชีโครงการ** สำหรับการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="31691-133">It's useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>

<span data-ttu-id="31691-134">ถ้ามีการติดตั้งสินทรัพย์ในตำแหน่งที่ทำงาน แต่มีการติดตั้งในตำแหน่งที่ทำงานอื่นในภายหลัง มิติทางการเงินที่เกี่ยวข้องกับตำแหน่งที่ทำงานใหม่จะมีการอัพเดตโดยอัตโนมัติในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="31691-134">If the asset was installed on a functional location but is later installed on a different functional location, the financial dimensions that are related to the new functional location are automatically updated on the asset.</span></span> <span data-ttu-id="31691-135">จากนั้น เมื่อคุณสร้างงานในใบสั่งงานสำหรับสินทรัพย์ โครงการของใบสั่งงานสำหรับงานในใบสั่งงาน จะได้รับมิติทางการเงินที่เกี่ยวข้องกับสินทรัพย์นี้โดยอัตโนมัติในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="31691-135">Then, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="31691-136">ดังนั้น เมื่อคุณใช้ตำแหน่งที่ทำงาน สามารถติดตามต้นทุนได้จากตำแหน่งที่ทำงานที่มีการติดตั้งสินทรัพย์ตามเวลาที่กำหนดไว้เมื่อใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="31691-136">Therefore, when you use functional locations, costs can always be tracked on the functional locations that an asset was installed on at any given time.</span></span> <span data-ttu-id="31691-137">การอัพเดตอัตโนมัติของมิติทางการเงินจะช่วยรับประกันการตรวจสอบความถูกต้องของต้นทุนที่สมบูรณ์ สำหรับการควบคุมและการรายงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="31691-137">The automatic update of financial dimensions helps guarantee complete traceability of costs for project control and reporting.</span></span>

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="31691-138">โครงการใบสั่งงาน สถานะวงจรของใบสั่งงาน ขั้นโครงการ และชนิดโครงการ</span><span class="sxs-lookup"><span data-stu-id="31691-138">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="31691-139">เพื่อช่วยรับประกันว่ามีการใช้สถานะวงจรของใบสั่งงานและขั้นโครงการที่เกี่ยวข้องในใบสั่งงานอย่างถูกต้อง ให้พิจารณาการอ้างอิงที่เกี่ยวข้องกับโมดูล **การจัดการและการบัญชีโครงการ** :</span><span class="sxs-lookup"><span data-stu-id="31691-139">To help guarantee that work order lifecycle states and related project stages on work orders are used correctly, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="31691-140">ในโมดูล **การจัดการและการบัญชีโครงการ** ขั้นโครงการจะถูกตั้งค่าบนชนิดโครงการในหน้า **พารามิเตอร์การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="31691-140">In the **Project management and accounting** module, project stages are set up on project types on the **Project management and accounting parameters** page.</span></span>  
- <span data-ttu-id="31691-141">ในหน้า **พารามิเตอร์การจัดการและการบัญชีโครงการ** ใช้กล่องกาเครื่องหมายเพื่อเลือกขั้นโครงการที่เกี่ยวข้องสำหรับชนิดโครงการทั้งหมดที่คุณจะใช้</span><span class="sxs-lookup"><span data-stu-id="31691-141">On the **Project management and accounting parameters** page, use the check boxes to select relevant project stages for all the project types that you will use.</span></span> <span data-ttu-id="31691-142">ในภาพประกอบต่อไปนี้ ห้าขั้น (**สร้างแล้ว** **ประเมินแล้ว** **จัดกำหนดการแล้ว** **อยู่ระหว่างดำเนินการ** และ **เสร็จสิ้นแล้ว**) ได้ถูกเลือกสำหรับชนิดโครงการ **เวลาและวัสดุ** และชนิดโครงการ **ภายใน**</span><span class="sxs-lookup"><span data-stu-id="31691-142">In the following illustrations, five stages (**Created**, **Estimated**, **Scheduled**, **In process**, and **Finished**) have been selected for the **Time and material** and **Internal** project types.</span></span> <span data-ttu-id="31691-143">ขั้นห้าขั้นเหล่านี้เกี่ยวข้องกับทั้งงานบำรุงรักษาภายในและงานบำรุงรักษาของบริการ</span><span class="sxs-lookup"><span data-stu-id="31691-143">Those five stages are relevant to both internal maintenance jobs and service maintenance jobs.</span></span>
- <span data-ttu-id="31691-144">ในโมดูล **การจัดการสินทรัพย์** ชนิดโครงการจะถูกกำหนดโดยกลุ่มโครงการที่คุณตั้งค่าไว้ในหน้า **การตั้งค่าโครงการของใบสั่งงาน** > แท็บ **กลุ่มโครงการ** (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **การตั้งค่าโครงการ**)</span><span class="sxs-lookup"><span data-stu-id="31691-144">In the **Asset Management** module, project types are defined by the project groups that you set up on the **Work order project setup** page > **Project group** tab (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  
- <span data-ttu-id="31691-145">กลุ่มโครงการที่ถูกตั้งค่าในหน้า **การตั้งค่าโครงการของใบสั่งงาน** จะถูกใช้เมื่อคุณสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-145">The project groups that are set up on the **Work order project setup** page are used when you create work orders.</span></span> <span data-ttu-id="31691-146">เมื่อใบสั่งงานถูกสร้าง โครงการของใบสั่งงานจะถูกสร้างขึ้นโดยอัตโนมัติสำหรับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-146">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="31691-147">สถานะวงจรใบสั่งงานทั้งหมดต้องมีขั้นโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="31691-147">Every work order lifecycle state must have a related project stage.</span></span>  
- <span data-ttu-id="31691-148">ขั้นโครงการที่เกี่ยวข้องกับสถานะวงจรของใบสั่งงาน ต้องถูกกำหนดเป็นขั้นที่ใช้งานอยู่สำหรับกลุ่มโครงการที่ถูกกำหนดไว้ในโครงการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-148">The project stage that is related to a work order lifecycle state must be defined as an active stage for the project group that is defined in the work order project.</span></span> <span data-ttu-id="31691-149">โครงการของใบสั่งงานจะถูกสร้างขึ้นโดยอัตโนมัติบนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-149">The work order project is automatically created on a work order.</span></span>
- <span data-ttu-id="31691-150">เมื่อคุณสร้างใบสั่งงานใหม่ การปันส่วนโดยอัตโนมัติของโครงการของใบสั่งงานจะขึ้นอยู่กับการตั้งค่าในหน้า **การตั้งค่าโครงการของใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="31691-150">When you create a new work order, the automatic allocation of a work order project is based on the setup on the **Work order project setup** page.</span></span>  

<span data-ttu-id="31691-151">ภาพประกอบต่อไปนี้แสดงความสัมพันธ์ระหว่างกลุ่มโครงการของใบสั่งงาน ชนิดโครงการที่เกี่ยวข้อง ขั้นโครงการ และสถานะวงจรใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="31691-151">The following illustrations show the associations between work order project groups, related project types, project stages, and work order lifecycle states.</span></span>

![รูปที่ 3](media/03-integration-to-pma.png)

![รูปที่ 4](media/04-integration-to-pma.png)

![รูปที่ 5](media/05-integration-to-pma.png)

<span data-ttu-id="31691-155">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าโครงการใบสั่งงาน ดู [การตั้งค่าโครงการใบสั่งงาน](../setup-for-work-orders/work-order-project-setup.md)</span><span class="sxs-lookup"><span data-stu-id="31691-155">For information about how to set up work order projects, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span> <span data-ttu-id="31691-156">สำหรับข้อมูลเกี่ยวกับวิธีการสร้างสถานะวงจรของใบสั่งงาน และดู [สถานะวงจรของใบสั่งงาน](../setup-for-work-orders/work-order-lifecycle-states.md)</span><span class="sxs-lookup"><span data-stu-id="31691-156">For information about how to create work order lifecycle states, see [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md).</span></span>

<span data-ttu-id="31691-157">ภาพประกอบต่อไปนี้แสดงภาพรวมแบบกราฟิกของโครงการต่างๆ ที่สร้างขึ้นในโมดูล **การจัดการสินทรัพย์** เพื่อเปิดใช้งานการรวมกับโมดูล **การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="31691-157">The following illustration shows a graphical overview of the various projects that are created in the **Asset management** module to enable integration with the **Project management and accounting** module.</span></span> <span data-ttu-id="31691-158">นอกจากนี้ ยังแสดงกระบวนการทำงานที่โครงการเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="31691-158">It also shows the work processes that the projects are related to.</span></span>

![รูปที่ 6](media/06-integration-to-pma.png)

