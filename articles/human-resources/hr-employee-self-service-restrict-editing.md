---
title: จํากัดการแก้ไขข้อมูลส่วนบุคคล
description: จํากัดพนักงานจากการแก้ไขรายละเอียดผู้ติดต่อใน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e3eeb66d4f32b1fea1a43fff9f5b09d87d1f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018720"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="2aa8a-103">จํากัดการแก้ไขข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="2aa8a-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="2aa8a-104">หัวข้อนี้อธิบายวิธีการจํากัดพนักงานจากการแก้ไขรายละเอียดผู้ติดต่อใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="2aa8a-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2aa8a-105">คุณอาจต้องการป้องกันไม่ให้พนักงานแก้ไขรายละเอียดผู้ติดต่อบางอย่าง เช่น ที่ตั้งธุรกิจหรือที่อยู่อีเมลของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="2aa8a-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="2aa8a-106">การใช้คุณลักษณะนี้ ก่อนอื่นคุณต้องเปิดใช้งาน **(พรีวิว) จํากัดพนักงานจากการเพิ่มหรือแก้ไขที่อยู่และข้อมูลผู้ติดต่อ เพื่อเลือกวัตถุประสงค์** ในการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="2aa8a-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="2aa8a-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะรุ่นพรีวิว ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)</span><span class="sxs-lookup"><span data-stu-id="2aa8a-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="2aa8a-108">![เปิดใช้งานคุณลักษณะการแสดงตัวอย่าง](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="2aa8a-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="2aa8a-109">เลือกข้อมูลที่พนักงานสามารถเพิ่มหรือแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="2aa8a-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="2aa8a-110">ในทรัพยากรบุคคล ให้เลือก **การจัดการบุคลากร** เลือก **ลิงค์** แล้วจากนั้น เลือก **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="2aa8a-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![ไปที่พารามิเตอร์ทรัพยากรบุคคล](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="2aa8a-112">บนหน้า **พารามิเตอร์ทรัพยากรบุคคล** ให้เลือกแท็บ **ระบบบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="2aa8a-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![เลือก ระบบบริการตนเองของพนักงาน](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="2aa8a-114">บนแท็บ **ระบบบริการตนเองของพนักงาน** ให้ยกเลิกการเลือกข้อมูลทั้งหมดในส่วน **ที่อยู่และข้อมูลการติดต่อ** ที่คุณไม่ต้องการให้พนักงานเพิ่มหรือแก้ไข</span><span class="sxs-lookup"><span data-stu-id="2aa8a-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="2aa8a-115">ในตัวอย่างนี้ เราได้ยกเลิกการเลือกข้อมูลการติดต่อ **ธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="2aa8a-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![จํากัดการแก้ไขข้อมูลการติดต่อทางธุรกิจ](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="2aa8a-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2aa8a-117">Select **Save**.</span></span>

   ![บันทึกการเปลี่ยนแปลง](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="2aa8a-119">ประสบการณ์พนักงาน</span><span class="sxs-lookup"><span data-stu-id="2aa8a-119">Employee experience</span></span>

<span data-ttu-id="2aa8a-120">หลังจากที่คุณได้จำกัดพนักงานจากการเพิ่มหรือแก้ไขรายละเอียดผู้ติดต่อแล้ว พนักงานสามารถดูข้อมูลได้ แต่ไม่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="2aa8a-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="2aa8a-121">ในตัวอย่างนี้ พนักงานที่ถูกจำกัดจากการแก้ไขรายละเอียดผู้ติดต่อ **ธุรกิจ** พนักงานยังคงสามารถดูข้อมูลในระบบบริการตนเองของพนักงาน:</span><span class="sxs-lookup"><span data-stu-id="2aa8a-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![ดูรายละเอียดผู้ติดต่อทางธุรกิจ](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="2aa8a-123">อย่างไรก็ตาม เมื่อเลือกรายละเอียดผู้ติดต่อทางธุรกิจ บานหน้าต่าง **แก้ไขที่อยู่** จะปรากฏเป็นแบบอ่านอย่างเดียว และไม่สามารถเปลี่ยนแปลงฟิลด์ใดๆ ได้</span><span class="sxs-lookup"><span data-stu-id="2aa8a-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![การแสดงรายละเอียดผู้ติดต่อทางธุรกิจเป็นแบบอ่านอย่างเดียว](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="2aa8a-125">นอกจากนี้ หากลูกค้าเลือก **เพิ่ม** เพื่อเพิ่มที่อยู่ใหม่ พวกเขาจะไม่สามารถเลือก **ธุรกิจ** จากกล่องรายการแบบหล่นลง **วัตถุประสงค์**</span><span class="sxs-lookup"><span data-stu-id="2aa8a-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![พนักงานไม่สามารถเพิ่มที่อยู่ทางธุรกิจ](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="2aa8a-127">พนักงานได้รับประสบการณ์ที่เหมือนกัน เมื่อพวกเขาเลือก **รายละเอียดผู้ติดต่อ** บนหน้า **ข้อมูลส่วนตัว** และเพิ่มที่อยู่ใหม่</span><span class="sxs-lookup"><span data-stu-id="2aa8a-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="2aa8a-128">กล่องรายการแบบหล่นลง **วัตถุประสงค์** จะแสดงเฉพาะชนิดของข้อมูลที่ผู้ใช้สามารถเพิ่มได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2aa8a-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![พนักงานไม่สามารถเลือก ธุรกิจ ในรายการแบบหล่นลงของวัตถุประสงค์](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="2aa8a-130">ขณะนี้ **รายละเอียดผู้ติดต่อ** แสดง **วัตถุประสงค์** ในกริด</span><span class="sxs-lookup"><span data-stu-id="2aa8a-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![วัตถุประสงค์แสดงในกริดรายละเอียดผู้ติดต่อ](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="2aa8a-132">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="2aa8a-132">See also</span></span>

[<span data-ttu-id="2aa8a-133">ภาพรวมของระบบบริการตนเองของพนักงานและผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="2aa8a-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="2aa8a-134">ตั้งค่าคอนฟิกพารามิเตอร์ Human Resources</span><span class="sxs-lookup"><span data-stu-id="2aa8a-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="2aa8a-135">แก้ไขข้อมูลส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="2aa8a-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)