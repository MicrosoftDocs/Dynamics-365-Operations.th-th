---
title: การสร้างผู้ใช้ใหม่
description: ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916495"
---
# <a name="create-new-users"></a><span data-ttu-id="38226-103">การสร้างผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="38226-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38226-104">ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน</span><span class="sxs-lookup"><span data-stu-id="38226-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="38226-105">ผู้ดูแลระบบสามารถทำขั้นตอนนี้เพื่อเพิ่มผู้ใช้ในระบบ </span><span class="sxs-lookup"><span data-stu-id="38226-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="38226-106">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="38226-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="38226-107">เพิ่มผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="38226-107">Add a new user</span></span>
1. <span data-ttu-id="38226-108">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การดูแลระบบ > ผู้ใช้ > ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="38226-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="38226-109">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="38226-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="38226-110">ในฟิลด์ **รหัสผู้ใช้** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="38226-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="38226-111">ป้อนรหัสเฉพาะสำหรับผู้ใช้ </span><span class="sxs-lookup"><span data-stu-id="38226-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="38226-112">ต้องมีรหัสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="38226-112">A user ID is required.</span></span>  
4. <span data-ttu-id="38226-113">ในฟิลด์ **ชื่อผู้ใช้** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="38226-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="38226-114">ป้อนชื่อของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="38226-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="38226-115">ในฟิลด์ **โดเมน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="38226-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="38226-116">ป้อนโดเมนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="38226-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="38226-117">ในฟิลด์ **นามแฝง** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="38226-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="38226-118">ป้อนนามแฝงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="38226-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="38226-119">ในฟิลด์ **บริษัท** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="38226-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="38226-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="38226-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="38226-121">ในส่วน **บทบาทของผู้ใช้** ให้คลิก **กำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="38226-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="38226-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="38226-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="38226-123">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="38226-123">Click **OK**.</span></span>
12. <span data-ttu-id="38226-124">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="38226-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="38226-125">นำเข้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="38226-125">Import users</span></span>
1. <span data-ttu-id="38226-126">ใน **บานหน้าต่างการดำเนินการ** คลิก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="38226-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="38226-127">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="38226-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="38226-128">คลิก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="38226-128">Click **Import users**.</span></span>
4. <span data-ttu-id="38226-129">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="38226-129">Click **Close**.</span></span>

