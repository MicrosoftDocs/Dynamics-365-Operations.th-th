---
title: กำหนดบทบาทผู้ใช้สัญญาเช่า
description: หัวข้อนี้จะอธิบายถึงบทบาทความปลอดภัยที่ใช้สำหรับการเช่าสินทรัพย์ นอกจากนี้ยังอธิบายถึงวิธีการกำหนดผู้ใช้ให้กับบทบาทเหล่านั้น
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: df23e219f5bd859b0072785dfd5f7a0ec63f540e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995404"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="c12f2-104">กำหนดบทบาทผู้ใช้สัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="c12f2-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c12f2-105">หัวข้อนี้จะอธิบายถึงบทบาทความปลอดภัยที่ใช้สำหรับการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="c12f2-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="c12f2-106">นอกจากนี้ยังอธิบายถึงวิธีการกำหนดผู้ใช้ให้กับบทบาทเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="c12f2-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="c12f2-107">สามบทบาทผู้ใช้แยกความแตกต่างของการเข้าถึงในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="c12f2-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="c12f2-108">บทบาทหนึ่งมีความเหมาะสมสำหรับการรักษาสัญญาเช่า หนึ่งมีความเหมาะสมสำหรับการดูสัญญาเช่า และเป็นหนึ่งในความเหมาะสมสำหรับการปฏิบัติหน้าที่ของพนักงานตามสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="c12f2-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="c12f2-109">แต่ละบทบาทมีสิทธิการได้รับอนุญาตเฉพาะสำหรับหน้าสัญญาเช่าทั้งหมด และแต่ละคนจะให้ผู้ใช้ดู สร้าง แก้ไข หรือลบสัญญาเช่า ตามหน้าที่การทำงานของตน</span><span class="sxs-lookup"><span data-stu-id="c12f2-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="c12f2-110">บทบาท</span><span class="sxs-lookup"><span data-stu-id="c12f2-110">Role</span></span>           | <span data-ttu-id="c12f2-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c12f2-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="c12f2-112">รักษาสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="c12f2-112">Maintain Lease</span></span> | <span data-ttu-id="c12f2-113">ผู้ใช้ในบทบาทนี้สามารถเพิ่ม แก้ไข ลบ และดูสัญญาเช่าได้</span><span class="sxs-lookup"><span data-stu-id="c12f2-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="c12f2-114">บทบาทนี้ได้รับการออกแบบสำหรับผู้ใช้ประจำวันที่มีงานรวมถึงการสร้างและการลงรายการบัญชีรายการสมุดรายวันรายเดือนและการเพิ่มสัญญาเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="c12f2-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="c12f2-115">บทบาทนี้ช่วยให้สามารถเข้าถึงฟังก์ชันการเช่าสินทรัพย์ทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="c12f2-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="c12f2-116">ดูสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="c12f2-116">View Lease</span></span>     | <span data-ttu-id="c12f2-117">ผู้ใช้ในบทบาทนี้สามารถดูได้เฉพาะเรกคอร์ดสัญญาเช่า จัดตารางการผลิต และการเรียกใช้รายงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c12f2-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="c12f2-118">พวกเขาไม่สามารถสร้างสัญญาเช่าใหม่ แก้ไขสัญญาเช่าที่มีอยู่ หรือสร้างรายการสมุดรายวันสำหรับสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="c12f2-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="c12f2-119">บทบาทนี้ได้รับการออกแบบมาสำหรับผู้ใช้ที่เพียงแค่ต้องดูสัญญาเช่า กำหนดการสัญญาเช่า และธุรกรรมที่เกิดขึ้นกับสัญญาเช่าเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="c12f2-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="c12f2-120">เสมียนสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="c12f2-120">Lease Clerk</span></span>    | <span data-ttu-id="c12f2-121">ผู้ใช้ในบทบาทนี้สามารถสร้างสัญญาเช่าใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c12f2-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="c12f2-122">พวกเขาไม่สามารถแก้ไขหรือลบสัญญาเช่าที่มีอยู่ ดูกำหนดสัญญาเช่า หรือลงรายการบัญชีสมุดรายวันการเช่า</span><span class="sxs-lookup"><span data-stu-id="c12f2-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="c12f2-123">บทบาทนี้ได้รับการออกแบบมาสำหรับผู้ใช้ที่ทำงานในความจุของการป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c12f2-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="c12f2-124">ทำตามขั้นตอนต่อไปนี้เพื่อกำหนดผู้ใช้ให้กับบทบาทที่ใช้ในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="c12f2-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="c12f2-125">ไปที่ **การจัดการระบบ \> ความปลอดภัย \> กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="c12f2-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="c12f2-126">เลือกรักษาการให้เช่าเจ้า **รักษาสัญญาเช่า** **เสมียนสัญญาเช่า** หรือบทบาท **ดูสัญญาเช่า** แล้วเลือก **กำหนด/ไม่รวมผู้ใช้ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="c12f2-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="c12f2-127">เลือกผู้ใช้ที่จะกำหนดให้กับบทบาท แล้วเลือก **กำหนดให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="c12f2-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
