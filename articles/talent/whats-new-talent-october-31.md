---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent - Core HR (31 ตุลาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Talent - Core HR
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897384"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a><span data-ttu-id="74cf5-103">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent - Core HR (31 ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="74cf5-103">What's new or changed in Dynamics 365 Talent - Core HR (October 31, 2018)</span></span>

<span data-ttu-id="74cf5-104">**สร้าง 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="74cf5-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="74cf5-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="74cf5-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance"></a><span data-ttu-id="74cf5-106">สร้างลิงค์จาก Talent ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="74cf5-106">Create links from Talent to Finance</span></span>
<span data-ttu-id="74cf5-107">ฟังก์ชันการนำทางใหม่นี้ช่วยให้คุณสามารถเชื่อมโยงจาก Talent ไปยัง Finance โดยให้การนำทางโดยตรงไปยังหน้า Finance</span><span class="sxs-lookup"><span data-stu-id="74cf5-107">This new navigation functionality allows you to link from Talent to Finance, giving you direct navigation into Finance pages.</span></span> <span data-ttu-id="74cf5-108">เมื่อมีการกำหนดค่าคอนฟิกลิงค์ คุณสามารถระบุชื่อและกลุ่มของลิงค์ ในตำแหน่งที่ลิงค์ควรแสดงใน Talent และหน้าเป้าหมายควรถูกเปิดภายใน Finance</span><span class="sxs-lookup"><span data-stu-id="74cf5-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="74cf5-109">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="74cf5-109">Coming soon</span></span>
<span data-ttu-id="74cf5-110">บริบทของฟิลด์จะถูกเพิ่มในอนาคตเพื่ออนุญาตให้นำทางโดยตรงไปยังเรกคอร์ดที่สอดคล้องกันใน Finance</span><span class="sxs-lookup"><span data-stu-id="74cf5-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance.</span></span> <span data-ttu-id="74cf5-111">ตัวอย่างเช่น คุณสามารถใช้ **ลิงค์ไปยังฟิลด์** เพื่อให้บริบทที่จะนำทางโดยตรงไปยังพนักงานหรือตำแหน่งเฉพาะใน Finance </span><span class="sxs-lookup"><span data-stu-id="74cf5-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="74cf5-112">ตั้งค่าคอนฟิกระบบปลายทาง</span><span class="sxs-lookup"><span data-stu-id="74cf5-112">Configure target systems</span></span>

<span data-ttu-id="74cf5-113">ใน Talent ผู้ดูแลระบบสามารถกำหนดลิงค์ที่จะแสดงถึงพื้นที่ทำงานการดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="74cf5-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="74cf5-114">ส่วนหนึ่งของการตั้งค่าคอนฟิกคือสภาพแวดล้อม Finance ที่คุณต้องการให้นำทางไปเป็น "เป้าหมาย" ของการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="74cf5-114">Part of the configuration is the Finance environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="74cf5-115">คุณดำเนินการนี้ได้โดยการตั้งชื่อระบบปลายทาง และใส่ URL ของสภาพแวดล้อม Finance</span><span class="sxs-lookup"><span data-stu-id="74cf5-115">You do this by giving the target system a name and providing the URL of the Finance environment.</span></span> <span data-ttu-id="74cf5-116">นี่คือตัวอย่าง URL ของ Finance ที่คุณจะต้องระบุ: https://devax00124aos.cloud.test.dynamics.com/</span><span class="sxs-lookup"><span data-stu-id="74cf5-116">Here is an example of a Finance URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="74cf5-117">หลังจากที่คุณตั้งค่าคอนฟิกระบบเป้าหมายของคุณ คุณสามารถกำหนดการเชื่อมโยงของคุณได้</span><span class="sxs-lookup"><span data-stu-id="74cf5-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="74cf5-118">ตั้งค่าคอนฟิกลิงก์</span><span class="sxs-lookup"><span data-stu-id="74cf5-118">Configure links</span></span>

<span data-ttu-id="74cf5-119">การเชื่อมโยงแต่ละรายการที่สร้างขึ้นจะมีการกำหนดข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="74cf5-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="74cf5-120">ลิงค์ - ชื่อของลิงค์ ที่ใช้สำหรับการระบุรหัสประจำตัวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="74cf5-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="74cf5-121">เปิดใช้งานลิงค์นี้ - ตั้งค่าเป็น **ใช่** ถ้าคุณต้องการแสดงลิงค์ต่อผู้ใช้ของ Talent</span><span class="sxs-lookup"><span data-stu-id="74cf5-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="74cf5-122">ชื่อที่แสดง - กำหนดชื่อที่จะปรากฏเป็นลิงค์ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="74cf5-122">Display name - Define the name that will appear as a link to Finance.</span></span> <span data-ttu-id="74cf5-123">ในขณะนี้ ไม่มีการแปลข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="74cf5-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="74cf5-124">แสดงลิงค์บนฟอร์ม - เลือกหน้าที่คุณต้องการแสดงลิงค์</span><span class="sxs-lookup"><span data-stu-id="74cf5-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="74cf5-125">กลุ่ม - ไม่จำเป็นต้องมีกลุ่ม แต่ถ้าคุณต้องการจัดระเบียบลิงค์ของคุณโดยใช้กลุ่ม เลือกกลุ่มที่มีอยู่ หรือสร้างใหม่โดยใช้ฟิลด์ **กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="74cf5-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="74cf5-126">ระบบเป้าหมาย - เลือกระบบเป้าหมายที่สร้างโดยใช้ตัวเลือก **ตั้งค่าคอนฟิกระบบเป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="74cf5-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="74cf5-127">นี่จะเป็นสภาพแวดล้อม Finance ที่จะใช้ เมื่อมีการนำทางโดยใช้การเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="74cf5-127">This will be the Finance environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="74cf5-128">ใช้บริษัทปัจจุบันของผู้ใช้ - เลือก **ใช่** ถ้าคุณต้องการใช้บริบทของบริษัทปัจจุบันของ User เมื่อนำทางไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="74cf5-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance.</span></span> <span data-ttu-id="74cf5-129">ถ้าเลือก **ไม่** จากนั้นคุณจะสามารถเลือกบริษัทที่ควรใช้ได้</span><span class="sxs-lookup"><span data-stu-id="74cf5-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="74cf5-130">รายการเมนูเป้าหมาย - ป้อนรายการเมนูจาก Finance ที่การเชื่อมโยงควรใช้ เมื่อมีการนำทาง</span><span class="sxs-lookup"><span data-stu-id="74cf5-130">Target menu item - Enter the menu item from Finance that the link should use when navigating.</span></span> <span data-ttu-id="74cf5-131">รายการเมนูที่คุณนำทางโดยตรงไป จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74cf5-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="74cf5-132">เพื่อค้นหารายการเมนูที่จำเป็น เปิด Finance และเปิดหน้าซึ่งเป็นเป้าหมายของการนำทาง</span><span class="sxs-lookup"><span data-stu-id="74cf5-132">To find the menu item required, open Finance and open the page that is the target of the navigation.</span></span> <span data-ttu-id="74cf5-133">คัดลอกรายการเมนูจาก URL</span><span class="sxs-lookup"><span data-stu-id="74cf5-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="74cf5-134">ตัวอย่างเช่น ถ้าคุณต้องการให้การเชื่อมโยงนำคุณไปยังรายการพนักงานใน Finance and Operations ป้อนค่าที่ปรากฏหลังจาก "&mi" ใน URL</span><span class="sxs-lookup"><span data-stu-id="74cf5-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="74cf5-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees</span><span class="sxs-lookup"><span data-stu-id="74cf5-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="74cf5-136">รายการเมนูที่จะนำทางไปยังหน้ารายการพนักงานในตัวอย่างนี้คือ: HcmWorkerListPage_Employees</span><span class="sxs-lookup"><span data-stu-id="74cf5-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="74cf5-137">การเชื่อมโยงไปยังแหล่งข้อมูล - เลือกแหล่งที่มาของข้อมูลที่กำลังอ้างอิงการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="74cf5-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="74cf5-138">แหล่งทั่วไปที่สุด เช่น **ผู้ปฏิบัติงาน** และ **ตำแหน่ง** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74cf5-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="74cf5-139">การเชื่อมโยงไปยังฟิลด์ - (เร็วๆ นี้) การเลือกฟิลด์นี้จะอนุญาตสำหรับการนำทางโดยตรงจากเรกคอร์ดเดียวใน Talent ไปยังเรกคอร์ดเดียวใน Finance</span><span class="sxs-lookup"><span data-stu-id="74cf5-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="74cf5-140">การเข้าถึงลิงค์</span><span class="sxs-lookup"><span data-stu-id="74cf5-140">Access to links</span></span>

<span data-ttu-id="74cf5-141">ผู้ดูแลระบบจะมองเห็นการเชื่อมโยงที่สร้างขึ้นใหม่บนหน้าที่กำหนด แม้ว่าตัวเลือก **เปิดใช้งานการเชื่อมโยงนี้** จะถูกตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="74cf5-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="74cf5-142">ซึ่งสามารถใช้ได้สำหรับการทดสอบการเชื่อมโยง ก่อนการแสดงให้กับพนักงานอื่น</span><span class="sxs-lookup"><span data-stu-id="74cf5-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="74cf5-143">บทบาทอื่นๆ ทั้งหมดจะเห็นเฉพาะลิงค์ที่ตั้งค่าคอนฟิก หลังจากตัวเลือก **เปิดใช้งานการเชื่อมโยงนี้** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="74cf5-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="74cf5-144">พนักงานที่มีการเข้าถึงไปยังหน้าที่ซึ่งการเชื่อมโยงจะปรากฏ จะมีการเข้าถึงไปยังการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="74cf5-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="74cf5-145">ผู้ใช้ยังสามารถมีสิทธิ์ความปลอดภัยภายใน Finance ที่กำหนดให้เข้าถึงหน้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="74cf5-145">Users can also have security rights within Finance defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="74cf5-146">ถ้าไม่ จะปรากฏกล่องโต้ตอบความปลอดภัยเมื่อใช้การเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="74cf5-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="74cf5-147">การเปลี่ยนแปลง/การแก้ไขอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="74cf5-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="74cf5-148">ไม่สามารถกำหนดตำแหน่งที่มีวันที่เริ่มต้นในอนาคตให้กับพนักงานใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="74cf5-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="74cf5-149">มีการทำการเปลี่ยนแปลงเพื่ออนุญาตให้มีการกำหนดพนักงานให้กับตำแหน่งที่เป็นวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="74cf5-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="74cf5-150">คุณสามารถเลือกตำแหน่งที่มีวันที่เริ่มต้นในอนาคต และจะมีการกำหนดพนักงานเมื่อมีการบันทึกหรือเสร็จสิ้นลำดับงาน (ถ้ามีการเปิดใช้งานลำดับงาน)</span><span class="sxs-lookup"><span data-stu-id="74cf5-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="74cf5-151">พนักงานใหม่ไม่สามารถถูกกำหนดตำแหน่งที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="74cf5-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="74cf5-152">มีการทำการเปลี่ยนแปลง ดังนั้นจึงสามารถกำหนดการมอบหมายพนักงานใหม่ไปยังตำแหน่งที่มีอยู่ในขณะนี้ได้</span><span class="sxs-lookup"><span data-stu-id="74cf5-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="74cf5-153">ที่ตั้งสำนักงาน/วันอายุงาน จะหายไปเมื่อวันที่เริ่มต้นการจ้างงานอยู่ในอดีต และมีการบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="74cf5-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="74cf5-154">มีการทำการเปลี่ยนแปลงเพื่อแก้ไขการมองเห็นได้ของ **วันที่ของอายุงาน** และ **ที่ตั้งสำนักงาน** เมื่อบันทึกการเปลี่ยนแปลงสำหรับพนักงานในอดีต</span><span class="sxs-lookup"><span data-stu-id="74cf5-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="74cf5-155">ไม่สามารถป้อนข้อมูลสำหรับการจ้างงานที่เป็นวันที่ในอนาคตได้บนหน้าผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="74cf5-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="74cf5-156">ข้อมูลการจ้างงานสำหรับการจ้างงานที่เป็นวันที่ในอนาคตถูกระงับบนหน้าผู้ปฏิบัติงานหลัก</span><span class="sxs-lookup"><span data-stu-id="74cf5-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="74cf5-157">คุณสามารถป้อนข้อมูลการจ้างงานผ่านทางหน้า **ตัวจัดการวันที่** ได้</span><span class="sxs-lookup"><span data-stu-id="74cf5-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="74cf5-158">จะสามารถทำการเปลี่ยนแปลงเพิ่มเติมได้ในการนำออกใช้ในอนาคต เพื่อเปิดใช้งานการป้อนข้อมูลการจ้างงานโดยตรงในระหว่างกระบวนการลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="74cf5-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="74cf5-159">เพิ่ม ValidFrom และ ValidTo ไปยัง HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="74cf5-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="74cf5-160">มีการอัพเดตเอนทิตี Data Management Framework (DMF) HcmPersonalContactPersonEntity เพื่อรวมวันที่ "มีผลบังคับใช้ตั้งแต่" และ "มีผลบังคับใช้จนถึง" เพื่อเปิดใช้งานสถานการณ์การรวมสวัสดิการบางรายการ</span><span class="sxs-lookup"><span data-stu-id="74cf5-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="74cf5-161">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="74cf5-161">Known issue</span></span>
- <span data-ttu-id="74cf5-162">**ปัญหา**: เมื่อเพิ่มสิ่งที่แนบมาใหม่กับผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** จะกลายเป็นสีเทา</span><span class="sxs-lookup"><span data-stu-id="74cf5-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="74cf5-163">**วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่าก FactBoxes บนหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="74cf5-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="74cf5-164">ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74cf5-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="74cf5-165">(ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)</span><span class="sxs-lookup"><span data-stu-id="74cf5-165">(This issue will be fixed in the next platform update.)</span></span>
