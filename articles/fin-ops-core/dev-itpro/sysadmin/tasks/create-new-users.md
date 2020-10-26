---
title: การสร้างผู้ใช้ใหม่
description: ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e84130ff2b1cf83b7d2b95eefc72175dc57743c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982513"
---
# <a name="create-new-users"></a><span data-ttu-id="3ea75-103">การสร้างผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="3ea75-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ea75-104">ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน</span><span class="sxs-lookup"><span data-stu-id="3ea75-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="3ea75-105">เชื่อมโยงผู้ใช้ที่มีสิทธิ์การใช้งาน (ชนิดใบอนุญาตใหม่เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="3ea75-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="3ea75-106">สำหรับลูกค้าที่ใช้ใบอนุญาตชนิดใหม่ที่เพิ่งมีการเพิ่มเมื่อเดือนตุลาคม 2019 ผู้ใช้ต้องเชื่อมโยงกับสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3ea75-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="3ea75-107">ในครั้งแรกที่ลงชื่อเข้าใช้ ผู้ใช้ที่ได้เชื่อมโยงสิทธิ์การใช้งานแล้ว จะถูกเพิ่มเป็นผู้ใช้ของระบบที่ไม่มีบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3ea75-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="3ea75-108">ผู้ดูแลระบบสามารถ [กำหนดสิทธิ์การใช้งานให้กับผู้ใช้](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) ใน [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="3ea75-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="3ea75-109">เชื่อมโยงผู้ใช้ภายนอกกับสิทธิ์การใช้งาน (ชนิดของสิทธิ์การใช้งานใหม่เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="3ea75-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="3ea75-110">ผู้ใช้ที่อยู่ภายนอกผู้เช่าที่มีการปรับใช้สภาพแวดล้อมจำเป็นต้องแสดงในไดเรกทอรีผู้เช่าโฮสต์ (Azure Active Directory (Azure AD)) เพื่อให้สามารถมอบสิทธิ์การใช้งานให้ได้</span><span class="sxs-lookup"><span data-stu-id="3ea75-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="3ea75-111">ควรเพิ่มผู้ใช้ภายนอกเหล่านั้นในผู้เช่าใน Azure AD ให้เป็นผู้ใช้ที่เป็นผู้เยี่ยมชม แล้วจึงมอบสิทธิ์การใช้งานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3ea75-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="3ea75-112">สำหรับข้อมูลเพิ่มเติม ดู [เพิ่ม Azure Active Directory ผู้ใช้ที่ทำงานร่วมกันแบบ B2B ในพอร์ทัล Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator)</span><span class="sxs-lookup"><span data-stu-id="3ea75-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="3ea75-113">เพิ่มผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="3ea75-113">Add a new user</span></span>
1. <span data-ttu-id="3ea75-114">ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3ea75-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="3ea75-115">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="3ea75-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="3ea75-116">ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนรหัสเฉพาะสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3ea75-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="3ea75-117">ต้องมีรหัสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3ea75-117">A user ID is required.</span></span>  
4. <span data-ttu-id="3ea75-118">ในฟิลด์ **ชื่อผู้ใช้** ให้ป้อนชื่อของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3ea75-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="3ea75-119">ในฟิลด์  **โดเมน** ให้ป้อนโดเมนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3ea75-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="3ea75-120">ในฟิลด์ **นามแฝง** ให้ป้อนนามแฝงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3ea75-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="3ea75-121">ในฟิลด์ **บริษัท** เลือกบริษัทที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3ea75-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="3ea75-122">ใน FastTab **บทบาทผู้ใช้** เลือก **มอบหมายบทบาท** เพื่อมอบหมายผู้ใช้ไปยัง Security role </span><span class="sxs-lookup"><span data-stu-id="3ea75-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="3ea75-123">สำหรับข้อมูลเพิ่มเติม ดู [มอบหมาย Security role ให้กับผู้ใช้](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="3ea75-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="3ea75-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3ea75-124">Select **OK**.</span></span>
10. <span data-ttu-id="3ea75-125">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3ea75-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="3ea75-126">นำเข้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3ea75-126">Import users</span></span>
1. <span data-ttu-id="3ea75-127">ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3ea75-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="3ea75-128">ในบานหน้าต่างการดำเนินการ ให้เลือก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3ea75-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="3ea75-129">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3ea75-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3ea75-130">เลือก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3ea75-130">Select **Import users**.</span></span>
5. <span data-ttu-id="3ea75-131">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="3ea75-131">Select **Close**.</span></span>

