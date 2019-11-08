---
title: การสร้างผู้ใช้ใหม่
description: ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570532"
---
# <a name="create-new-users"></a><span data-ttu-id="ee103-103">การสร้างผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="ee103-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee103-104">ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน</span><span class="sxs-lookup"><span data-stu-id="ee103-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="ee103-105">เชื่อมโยงผู้ใช้ที่มีสิทธิ์การใช้งาน (ชนิดใบอนุญาตใหม่เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="ee103-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="ee103-106">สำหรับลูกค้าที่ใช้ใบอนุญาตชนิดใหม่ที่เพิ่งมีการเพิ่มเมื่อเดือนตุลาคม 2019 ผู้ใช้ต้องเชื่อมโยงกับสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ee103-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="ee103-107">ในครั้งแรกที่ลงชื่อเข้าใช้ ผู้ใช้ที่ได้เชื่อมโยงสิทธิ์การใช้งานแล้ว จะถูกเพิ่มเป็นผู้ใช้ของระบบที่ไม่มีบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ee103-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="ee103-108">ผู้ใช้ที่ไม่ได้เชื่อมโยงสิทธิ์การใช้งาน จะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="ee103-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="ee103-109">ผู้ดูแลระบบสามารถ [กำหนดสิทธิ์การใช้งานให้กับผู้ใช้](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) ใน [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="ee103-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="ee103-110">เพิ่มผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="ee103-110">Add a new user</span></span>
1. <span data-ttu-id="ee103-111">ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="ee103-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="ee103-112">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="ee103-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="ee103-113">ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนรหัสเฉพาะสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ee103-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="ee103-114">ต้องมีรหัสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ee103-114">A user ID is required.</span></span>  
4. <span data-ttu-id="ee103-115">ในฟิลด์ **ชื่อผู้ใช้** ให้ป้อนชื่อของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ee103-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="ee103-116">ในฟิลด์  **โดเมน** ให้ป้อนโดเมนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ee103-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="ee103-117">ในฟิลด์ **นามแฝง** ให้ป้อนนามแฝงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ee103-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="ee103-118">ในฟิลด์ **บริษัท** เลือกบริษัทที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ee103-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="ee103-119">บนแท็บด่วน **บทบาทของผู้ใช้** ให้เลือก **กำหนดบทบาท** ที่ [จะกำหนดบทบาทความปลอดภัยให้ผู้ใช้](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="ee103-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="ee103-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ee103-120">Select **OK**.</span></span>
10. <span data-ttu-id="ee103-121">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ee103-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="ee103-122">นำเข้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ee103-122">Import users</span></span>
1. <span data-ttu-id="ee103-123">ในบานหน้าต่างการดำเนินการ ให้เลือก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="ee103-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="ee103-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ee103-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ee103-125">เลือก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="ee103-125">Select **Import users**.</span></span>
4. <span data-ttu-id="ee103-126">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="ee103-126">Select **Close**.</span></span>

