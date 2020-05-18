---
title: การวินิจฉัยความปลอดภัยสำหรับการบันทึกงาน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการวิเคราะห์และจัดการข้อกําหนดสิทธิ์ด้านความปลอดภัยตามการบันทึกงาน
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: fada3abb9362426c7c9ec33f5d25552edf3ef630
ms.sourcegitcommit: 71fec2553158c332ce4d4bfcedc2c1ab58c1a1a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/06/2020
ms.locfileid: "3340686"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="bc385-103">การวินิจฉัยความปลอดภัยสำหรับการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="bc385-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="bc385-104">ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bc385-104">Before you begin</span></span>

<span data-ttu-id="bc385-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการวิเคราะห์และจัดการข้อกําหนดสิทธิ์ด้านความปลอดภัยตามการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="bc385-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="bc385-106">ก่อนที่คุณจะดําเนินการขั้นตอนต่างๆ ในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องมีการบันทึกงานของกระบวนการทางธุรกิจที่คุณต้องการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="bc385-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="bc385-107">เมื่อต้องการบันทึกกระบวนการทางธุรกิจ ให้ดูที่ [ทรัพยากรตัวบันทึกงาน](../../user-interface/task-recorder.md)</span><span class="sxs-lookup"><span data-stu-id="bc385-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="bc385-108">จัดการความปลอดภัยสําหรับการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="bc385-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="bc385-109">ไปที่ **การจัดการระบบ** > **ความปลอดภัย** > **การวินิจฉัยความปลอดภัยสําหรับการบันทึกงาน**</span><span class="sxs-lookup"><span data-stu-id="bc385-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="bc385-110">เปิดการบันทึกงานจากตําแหน่งที่ตั้งของงาน</span><span class="sxs-lookup"><span data-stu-id="bc385-110">Open the task recording from its location.</span></span> <span data-ttu-id="bc385-111">เลือก **เปิดจากพีซีเครื่องนี้** หรือ **เปิดจาก Lifecycle Services** แล้วเลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bc385-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="bc385-112">การดําเนินการนี้จะเปิดหน้า **รายละเอียดรายการเมนูความปลอดภัย** ที่แสดงวัตถุประสงค์ความปลอดภัยที่จําเป็นสําหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="bc385-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="bc385-113">รายการเมนู **การดำเนินการ** และ **ผลลัพธ์** จะไม่รวมอยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="bc385-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="bc385-114">ในฟิลด์ **รหัสผู้ใช้** เลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bc385-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="bc385-115">ถ้าผู้ใช้ไม่มีสิทธิ์สําหรับรายการเมนูบางรายการ ฟิลด์ **สิทธิ์ที่ขาดหายไป** จะอัพเดทเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="bc385-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![หน้ารายละเอียดรายการเมนูความปลอดภัย](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="bc385-117">เลือก **เพิ่มการอ้างอิง** เพื่อดูรายการของจุดประสงค์ความปลอดภัย รวมถึงบทบาท หน้าที่ และสิทธิ์ที่สิทธิ์ขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="bc385-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="bc385-118">เลือกจุดประสงค์ความปลอดภัยจากรายการ</span><span class="sxs-lookup"><span data-stu-id="bc385-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="bc385-119">ถ้า **บทบาท** ถูกเลือก ให้เลือก **เพิ่มบทบาทให้กับผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="bc385-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="bc385-120">ซึ่งจะเปิดหน้า **มอบหมายผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="bc385-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="bc385-121">สำหรับข้อมูลเพิ่มเติม ดูที่หน้า [มอบหมาบทบาทความปลอดภัยให้กับผู้ใช้](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="bc385-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="bc385-122">ถ้า **หน้าที่** ถูกเลือก ให้เลือก **เพิ่มหน้าที่ให้กับบทบาท** เลือกบทบาทที่ควรเพิ่มหน้าที่ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bc385-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="bc385-123">ถ้า **สิทธิ์** ถูกเลือก ให้เลือก **เพิ่มสิทธิ์ให้กับหน้าที่** เลือกบทบาทที่ควรเพิ่มหน้าที่ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bc385-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
