---
title: ผู้ปฏิบัติงานที่ไม่มีการจ้างงาน
description: ผู้ปฏิบัติงานที่ไม่มีการจ้างงานในอนาคต ปัจจุบัน หรือในอดีตกับองค์กรของคุณ จะปรากฏในฟอร์มผู้ปฏิบัติงานที่ไม่มีการจ้างงาน
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924582"
---
# <a name="workers-without-employment"></a><span data-ttu-id="68f72-103">ผู้ปฏิบัติงานที่ไม่มีการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="68f72-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="68f72-104">ผู้ปฏิบัติงานที่ไม่มีการจ้างงานในอนาคต ปัจจุบัน หรือในอดีตกับองค์กรของคุณ จะปรากฏในฟอร์ม **ผู้ปฏิบัติงานที่ไม่มีการจ้างงาน**</span><span class="sxs-lookup"><span data-stu-id="68f72-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="68f72-105">ผู้ปฏิบัติงานที่มีสถานะนี้สามารถปรากฏขึ้น เมื่อคุณนําเข้าผู้ปฏิบัติงานที่ไม่มีเรกคอร์ดการจ้างงาน หรือเมื่อคุณลบการจ้างงานของผู้ปฏิบัติงานผ่านทาง **ผู้ปฏิบัติงาน > ประวัติการจ้างงาน**</span><span class="sxs-lookup"><span data-stu-id="68f72-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="68f72-106">โดยค่าเริ่มต้น ฟอร์ม **ผู้ปฏิบัติงานที่ไม่มีการจ้างงาน** จะพร้อมให้ใช้งานกับบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="68f72-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="68f72-107">ผู้ช่วยฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="68f72-107">Human Resources Assistant</span></span>
- <span data-ttu-id="68f72-108">ผู้จัดการฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="68f72-108">Human Resources Manager</span></span>
- <span data-ttu-id="68f72-109">ผู้สรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="68f72-109">Recruiter</span></span>
- <span data-ttu-id="68f72-110">ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="68f72-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="68f72-111">ผู้ดูแลระบบค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="68f72-111">Payroll Administrator</span></span>
- <span data-ttu-id="68f72-112">ผู้จัดการฝ่ายค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="68f72-112">Payroll Manager</span></span>
- <span data-ttu-id="68f72-113">ผู้จัดการฝ่ายฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="68f72-113">Training Manager</span></span>

<span data-ttu-id="68f72-114">ในรายการ **ผู้ปฏิบัติงานที่ไม่มีการจ้างงาน** คุณสามารถลบบุคคลที่แสดงรายการไว้ได้</span><span class="sxs-lookup"><span data-stu-id="68f72-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="68f72-115">โดยค่าเริ่มต้น จะมอบสิทธิ์นี้ให้กับบทบาทผู้ช่วยฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="68f72-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="68f72-116">คุณสามารถให้สิทธิ์นี้แก่บทบาทอื่นโดยใช้ขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="68f72-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="68f72-117">เลือก **การจัดการระบบ** แล้วเลือกแท็บ **การตั้งค่าคอนฟิกด้านความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="68f72-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="68f72-118">ในแท็บ **สิทธิ์** ให้กรองรายการ **สิทธิ์** ไปยัง **รักษาผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="68f72-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="68f72-119">[![รายการสิทธิ์ตัวกรอง](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="68f72-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="68f72-120">ในคอลัมน์ **อ้างอิง** เลือก **รายการเมนูที่แสดง**</span><span class="sxs-lookup"><span data-stu-id="68f72-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="68f72-121">ใน **รายการเมนูที่แสดง** เลือก **HcmWorkersWithoutEmployment**</span><span class="sxs-lookup"><span data-stu-id="68f72-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="68f72-122">[![เลือกแบบฟอร์ม](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="68f72-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="68f72-123">ตั้งค่าสิทธิ์ **ลบ** เพื่อ **มอบสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="68f72-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="68f72-124">เลือกแท็บ **ออบเจ็กต์ที่ยังไม่ได้เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="68f72-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="68f72-125">เลือก **เผยแพร่ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="68f72-125">Select **Publish all**.</span></span>

   <span data-ttu-id="68f72-126">[![เผยแพร่กการเปลี่ยนแปลง](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="68f72-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]