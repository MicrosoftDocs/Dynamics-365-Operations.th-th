---
title: จัดการผู้ใช้และบทบาทอีคอมเมิร์ซ
description: หัวข้อนี้จะอธิบายถึงวิธีการให้สิทธิ์แก่ผู้ใช้ในสภาพแวดล้อมการสร้างไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a2235a43fd69adddeaba4c29305435db0fa39d64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255930"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="e15f0-103">จัดการผู้ใช้และบทบาทอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e15f0-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e15f0-104">หัวข้อนี้จะอธิบายถึงวิธีการให้สิทธิ์แก่ผู้ใช้ในสภาพแวดล้อมการสร้างไซต์ Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e15f0-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="e15f0-105">เพื่อช่วยควบคุมการเข้าถึงของผู้ใช้และสิทธิการได้รับอนุญาตของผู้ใช้ในการดำเนินงานที่ระบุ สภาพแวดล้อมการสร้างไซต์ใช้กลุ่มรักษาความปลอดภัยที่คุณสร้างขึ้นใน Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="e15f0-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="e15f0-106">คุณได้กำหนดกลุ่มรักษาความปลอดภัยใหม่หรือที่มีอยู่จาก Azure AD ให้กับแต่ละบทบาทในสภาพแวดล้อมการสร้างเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="e15f0-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="e15f0-107">จากนั้นคุณจะได้รับอนุญาตหรือเพิกถอนสิทธิ์สำหรับผู้ใช้แต่ละคนโดยการเพิ่มผู้ใช้เหล่านั้นไปยังกลุ่มรักษาความปลอดภัยที่เหมาะสมหรือลบออกจากกลุ่มรักษาความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="e15f0-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="e15f0-108">ภาพรวมของบทบาทในสภาพแวดล้อมการสร้าง</span><span class="sxs-lookup"><span data-stu-id="e15f0-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="e15f0-109">สภาพแวดล้อมการสร้าง Dynamics 365 for Commerce สนับสนุนบทบาทต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e15f0-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="e15f0-110">บทบาท</span><span class="sxs-lookup"><span data-stu-id="e15f0-110">Role</span></span>                 | <span data-ttu-id="e15f0-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e15f0-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="e15f0-112">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e15f0-112">System Administrator</span></span> | <span data-ttu-id="e15f0-113">ผู้ใช้ที่มีบทบาทนี้มีสิทธิ์ทั้งหมดสำหรับเครื่องมือทั้งหมด และสำหรับการจัดอันดับและการตรวจทานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e15f0-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="e15f0-114">นอกจากนี้คุณยังสามารถสร้างไซต์ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="e15f0-114">They can also create sites.</span></span> |
| <span data-ttu-id="e15f0-115">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e15f0-115">Administrator</span></span>   | <span data-ttu-id="e15f0-116">ผู้ใช้ที่มีบทบาทนี้มีสิทธิ์ทั้งหมดสำหรับเครื่องมือทั้งหมดและ RnR ในโครงสร้างไซต์ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="e15f0-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="e15f0-117">ผู้ผลิตเว็บ</span><span class="sxs-lookup"><span data-stu-id="e15f0-117">Web Producer</span></span>         | <span data-ttu-id="e15f0-118">ผู้ใช้ที่มีบทบาทนี้สามารถสร้างหน้า ส่วนต่างๆ และเท็มเพลต อัพโหลดและจัดการสินทรัพย์และจัดสรรผลิตภัณฑ์และประเภท</span><span class="sxs-lookup"><span data-stu-id="e15f0-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="e15f0-119">ตัวอ่าน</span><span class="sxs-lookup"><span data-stu-id="e15f0-119">Reader</span></span>               | <span data-ttu-id="e15f0-120">ผู้ใช้ที่มีบทบาทนี้สามารถดูหน้า เท็มเพลต สินทรัพย์ ส่วนประกอบ โครงร่าง และการตั้งค่า แต่ไม่สามารถทำการเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="e15f0-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="e15f0-121">ผู้ควบคุม RnR</span><span class="sxs-lookup"><span data-stu-id="e15f0-121">RnR Moderator</span></span>        | <span data-ttu-id="e15f0-122">ผู้ใช้ที่มีบทบาทนี้สามารถควบคุมความคิดเห็นผลิตภัณฑ์ปานกลางได้</span><span class="sxs-lookup"><span data-stu-id="e15f0-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="e15f0-123">บทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e15f0-123">System Administrator role</span></span>

<span data-ttu-id="e15f0-124">เมื่อคุณเตรียมใช้งาน Dynamics 365 Commerce ใน Microsoft Dynamics Lifecycle Services (LCS) คุณจะได้รับการร้องขอให้กำหนดกลุ่มรักษาความปลอดภัยสำหรับ **บทบาทผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="e15f0-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="e15f0-125">จะมีการใช้บทบาทนี้โดยอัตโนมัติกับไซต์ทั้งหมดที่คุณสร้างขึ้นในสภาพแวดล้อมที่คุณกำลังตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="e15f0-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="e15f0-126">กลุ่มรักษาความปลอดภัยสำหรับบทบาทนี้สามารถอัพเดตได้ใน LCS เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e15f0-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="e15f0-127">บนหน้า **การดูแลไซต์** สำหรับไซต์ทั้งหมดจะปรากฏเป็นแบบอ่านอย่างเดียวและใช้เพื่อวัตถุประสงค์ในการให้ข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e15f0-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="e15f0-128">บทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e15f0-128">Administrator role</span></span>

<span data-ttu-id="e15f0-129">เมื่อคุณสร้างไซต์ใหม่ในคอมเมิร์ซ ระบบจะขอให้คุณระบุกลุ่มรักษาความปลอดภัยสำหรับบทบาท **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="e15f0-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="e15f0-130">ดูตารางก่อนหน้านี้ในหัวข้อนี้สำหรับภาพรวมของสิทธิการได้รับอนุญาตของบทบาทนี้</span><span class="sxs-lookup"><span data-stu-id="e15f0-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="e15f0-131">เพิ่มหรืออัพเดตกลุ่มความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="e15f0-131">Add or update security groups</span></span>

<span data-ttu-id="e15f0-132">หลังจากที่สร้างไซต์ของคุณแล้ว เฉพาะผู้ใช้ที่อยู่ในกลุ่มรักษาความปลอดภัยที่เกี่ยวข้องกับ **ผู้ดูแลระบบ** และบทบาท **ผู้ดูแลระบบ** เท่านั้นที่สามารถเข้าถึงสภาพแวดล้อมการสร้างไซต์นั้นได้</span><span class="sxs-lookup"><span data-stu-id="e15f0-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="e15f0-133">เมื่อต้องการกำหนดผู้ใช้ให้กับบทบาท **ผู้ผลิตเว็บ** **ผู้ดูแล RnR** และ **ผู้อ่าน** คุณต้องกำหนดกลุ่มรักษาความปลอดภัยให้กับบทบาทเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="e15f0-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="e15f0-134">เมื่อต้องการเพิ่มกลุ่มรักษาความปลอดภัยให้กับบทบาทหรือเพื่ออัพเดตกลุ่มความปลอดภัยที่กำหนดให้กับบทบาท ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e15f0-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="e15f0-135">ไปที่ไซต์ที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="e15f0-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="e15f0-136">ใน **การจัดการไซต์** ให้เปิดหน้า **ความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="e15f0-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="e15f0-137">เลือกบทบาทที่จะปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="e15f0-137">Select the role to modify.</span></span>
1. <span data-ttu-id="e15f0-138">เพิ่มกลุ่มรักษาความปลอดภัยให้กับบทบาทหรือลบกลุ่มรักษาความปลอดภัยออกจากบทบาท</span><span class="sxs-lookup"><span data-stu-id="e15f0-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e15f0-139">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e15f0-139">Additional resources</span></span>

[<span data-ttu-id="e15f0-140">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="e15f0-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="e15f0-141">ข้อควรพิจารณาเกี่ยวกับการเพิ่มประสิทธิภาพโปรแกรมค้นหา (SEO) สำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e15f0-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="e15f0-142">จัดการนโยบายความปลอดภัยของเนื้อหา (CSP)</span><span class="sxs-lookup"><span data-stu-id="e15f0-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]