---
title: ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน
description: กำหนดพารามิเตอร์ทรัพยากรบุคคลสำหรับการลางานและการขาดงานใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010713"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="21861-103">ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21861-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="21861-104">ก่อนที่คุณจะตั้งค่าการลางานและการขาดงานใน Dynamics 365 Human Resources คุณควรตรวจสอบความถูกต้องของการตั้งค่าสำหรับพารามิเตอร์ทรัพยากรบุคคลที่เกี่ยวข้องทั้งหมดรวมถึงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="21861-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="21861-105">ลำดับหมายเลขสำหรับการร้องขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="21861-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="21861-106">การตั้งค่าการลาดูแลครอบครัว ลาป่วย และลางาน (FMLA)</span><span class="sxs-lookup"><span data-stu-id="21861-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="21861-107">การตั้งค่าระบบบริการตนเองของพนักงานสำหรับการร้องขอการลางานหรือการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21861-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="21861-108">พารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21861-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="21861-109">ดูและเปลี่ยนแปลงพารามิเตอร์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="21861-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="21861-110">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="21861-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="21861-111">ภายใต้ **ตั้งค่า**พารามิเตอร์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="21861-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="21861-112">บนแท็บ **ลำดับหมายเลข** ตรวจสอบความถูกต้องของ **รหัสลำดับหมายเลข** สำหรับ **รหัสคำขอลางาน** และเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="21861-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="21861-113">การตั้งค่านี้จะกำหนดลำดับที่ใช้สำหรับการกำหนดรหัสให้กับการร้องขอโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="21861-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="21861-114">บนแท็บ **FMLA** ให้ตรวจสอบการตั้งค่า FMLA และเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="21861-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="21861-115">บนแท็บ **ระบบบริการตนเองของพนักงาน** ให้ระบุว่าผู้จัดการสามารถป้อนการลางานและการร้องขอการขาดงานในนามของพนักงานได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="21861-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="21861-116">บนแท็บ **การลางานและการขาดงาน** ให้ตรวจสอบการตั้งค่าและเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="21861-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="21861-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="21861-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="21861-118">ตั้งค่าคอนฟิกพารามิเตอร์ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="21861-118">Configure calendar parameters</span></span>

<span data-ttu-id="21861-119">ถ้าคุณได้เปิดใช้งานคุณลักษณะตัวอย่างการลางานและปฏิทินการขาดงานคุณต้องตั้งค่าคอนฟิกพารามิเตอร์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="21861-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="21861-120">สำหรับการเผยแพร่การแสดงตัวอย่างในวันที่ 3 กุมภาพันธ์ 2020 มีเพียง **การร้องขอการลางานที่ค้างอยู่** ที่มีการเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="21861-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="21861-121">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="21861-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="21861-122">ภายใต้ **ตั้งค่า**พารามิเตอร์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="21861-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="21861-123">บนแท็บ **ปฏิทิน** เปลี่ยนแปลงปฏิทินตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="21861-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="21861-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="21861-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="21861-125">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="21861-125">See also</span></span>

- [<span data-ttu-id="21861-126">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21861-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
