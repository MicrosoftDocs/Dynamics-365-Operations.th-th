---
title: การสร้างผู้ใช้ใหม่
description: ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 89e492ef5030dd28020094152259b615010aa676
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851322"
---
# <a name="create-new-users"></a><span data-ttu-id="531f9-103">การสร้างผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="531f9-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="531f9-104">ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน</span><span class="sxs-lookup"><span data-stu-id="531f9-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="531f9-105">ผู้ดูแลระบบสามารถทำขั้นตอนนี้เพื่อเพิ่มผู้ใช้ในระบบ </span><span class="sxs-lookup"><span data-stu-id="531f9-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="531f9-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="531f9-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="531f9-107">เพิ่มผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="531f9-107">Add a new user</span></span>
1. <span data-ttu-id="531f9-108">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="531f9-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="531f9-109">Click New.</span></span>
3. <span data-ttu-id="531f9-110">ในฟิลด์รหัสผู้ใช้ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="531f9-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="531f9-111">ป้อนรหัสเฉพาะสำหรับผู้ใช้ </span><span class="sxs-lookup"><span data-stu-id="531f9-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="531f9-112">ต้องมีรหัสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-112">A user ID is required.</span></span>  
4. <span data-ttu-id="531f9-113">ในฟิลด์ชื่อผู้ใช้ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="531f9-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="531f9-114">ป้อนชื่อของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="531f9-115">ในฟิลด์โดเมน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="531f9-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="531f9-116">ป้อนโดเมนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="531f9-117">ในฟิลด์นามแฝง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="531f9-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="531f9-118">ป้อนนามแฝงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="531f9-119">ในฟิลด์บริษัท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="531f9-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="531f9-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="531f9-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="531f9-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="531f9-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="531f9-122">เลือกบริษัทของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-122">Select the user's company</span></span>  
10. <span data-ttu-id="531f9-123">คลิกการกำหนดบทบาท</span><span class="sxs-lookup"><span data-stu-id="531f9-123">Click Assign roles.</span></span>
11. <span data-ttu-id="531f9-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="531f9-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="531f9-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="531f9-125">Click OK.</span></span>
13. <span data-ttu-id="531f9-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="531f9-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="531f9-127">นำเข้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-127">Import users</span></span>
1. <span data-ttu-id="531f9-128">คลิกการนำเข้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-128">Click Import users.</span></span>
2. <span data-ttu-id="531f9-129">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="531f9-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="531f9-130">คลิกการนำเข้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="531f9-130">Click Import users.</span></span>
4. <span data-ttu-id="531f9-131">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="531f9-131">Click Close.</span></span>

