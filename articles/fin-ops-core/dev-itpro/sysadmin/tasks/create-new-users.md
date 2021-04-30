---
title: การสร้างผู้ใช้ใหม่
description: ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88d3f1fba05d944e78e4595018d190c3dc41e076
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907922"
---
# <a name="create-new-users"></a><span data-ttu-id="b4d0b-103">สร้างผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="b4d0b-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4d0b-104">ก่อนที่คุณจะสามารถเข้าถึงแอป Finance and Operations ได้ คุณต้องถูกเพิ่มลงในหน้า **ผู้ใช้** ก่อน (**การจัดการ \> ผู้ใช้ \> ผู้ใช้**)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="b4d0b-105">ผู้ใช้รวมพนักงานภายในขององค์กร หรือลูกค้าและผู้จัดจำหน่ายภายนอก</span><span class="sxs-lookup"><span data-stu-id="b4d0b-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="b4d0b-106">คุณสามารถนําเข้าหรือเพิ่มผู้ใช้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b4d0b-106">Users can be imported or added manually.</span></span> <span data-ttu-id="b4d0b-107">ผู้ใช้ทั้งหมดต้องมีสิทธิ์ถูกต้องสำหรับการใช้งานตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="b4d0b-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="b4d0b-108">สำหรับข้อมูลเกี่ยวกับวิธีการการซื้อและมอบสิทธิ์สำหรับแอป Finance and Operations โปรดดูที่ [คู่มือการให้สิทธิ์การใช้งาน Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="b4d0b-109">กำหนดสิทธิ์ให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-109">Assign a license to a user</span></span>
<span data-ttu-id="b4d0b-110">ผู้ดูแลระบบสามารถ [กำหนดสิทธิ์การใช้งานให้กับผู้ใช้](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) ใน [Microsoft 365 admin center](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-110">System admins can [assign licenses to users](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="b4d0b-111">เพิ่มผู้ใช้ภายนอกใน Azure AD และกําหนดสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="b4d0b-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="b4d0b-112">ผู้ใช้ภายนอกต้องถูกแสดงในไดเรกทอรีผู้เช่าของคุณ (Azure Active Directory (Azure AD)) เพื่อให้มีการกำหนดสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="b4d0b-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="b4d0b-113">ควรเพิ่มผู้ใช้ภายนอกเหล่านั้นในผู้เช่าใน Azure AD ให้เป็นผู้ใช้ที่เป็นผู้เยี่ยมชม แล้วจึงมอบสิทธิ์การใช้งานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="b4d0b-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="b4d0b-114">ความต้องการสำหรับแอป Finance and Operations คือบริษัทของผู้ใช้ที่เป็นแขกจะต้องใช้ Azure AD</span><span class="sxs-lookup"><span data-stu-id="b4d0b-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="b4d0b-115">สำหรับข้อมูลเพิ่มเติม ดู [เพิ่ม Azure Active Directory ผู้ใช้ที่ทำงานร่วมกันแบบ B2B ในพอร์ทัล Azure](/azure/active-directory/b2b/add-users-administrator)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="b4d0b-116">นำเข้าผู้ใช้ใหม่จาก Azure AD</span><span class="sxs-lookup"><span data-stu-id="b4d0b-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="b4d0b-117">ไปที่ **การจัดการระบบ** \> **ผู้ใช้** \> **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="b4d0b-118">ในบานหน้าต่างการดำเนินการ ให้เลือก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="b4d0b-119">เลือกผู้ใช้ที่จะถูกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="b4d0b-119">Select the users to be imported.</span></span> <span data-ttu-id="b4d0b-120">รายการประกอบด้วยผู้ใช้ Azure AD ที่ในขณะนี้ไม่ใช่ผู้ใช้ในสภาพแวดล้อมนี้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="b4d0b-121">เลือก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-121">Select **Import users**.</span></span>
5. <span data-ttu-id="b4d0b-122">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="b4d0b-123">ค่าของฟิลด์ **บริษัท** จะถูกตั้งค่าตามบริษัทในรอบเวลาปัจจุบันของผู้ดูแลระบบ หลังจากการนําเข้า คุณต้องกําหนดบทบาทและองค์กรตามที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b4d0b-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="b4d0b-124">สำหรับข้อมูลเพิ่มเติม ดู [มอบหมาย Security role ให้กับผู้ใช้](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="b4d0b-125">นอกจากนี้ ยังอาจต้องเชื่อมโยงผู้ใช้กับ **บุคคล** และอัพเดตตัวเลือกผู้ใช้ เช่น ภาษา แบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="b4d0b-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="b4d0b-126">เพิ่มผู้ใช้ใหม่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b4d0b-126">Manually add a new user</span></span>
1. <span data-ttu-id="b4d0b-127">ไปที่ **การจัดการระบบ** \> **ผู้ใช้** \> **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="b4d0b-128">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="b4d0b-129">ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนรหัสเฉพาะสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="b4d0b-130">ในฟิลด์ **ชื่อผู้ใช้** ให้ป้อนชื่อของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="b4d0b-131">ในฟิลด์ **ผู้ให้บริการ**:</span><span class="sxs-lookup"><span data-stu-id="b4d0b-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="b4d0b-132">สำหรับผู้ใช้ภายใน ให้ใช้ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b4d0b-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="b4d0b-133">ตัวอย่างเช่น ผู้เช่า Azure AD ของคุณที่นําหน้าด้วย https://sts.windows.net/</span><span class="sxs-lookup"><span data-stu-id="b4d0b-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="b4d0b-134">สำหรับผู้ใช้ที่ไม่ใช่ Azure AD เช่น บัญชี Service-2-Service ให้ป้อนค่าข้อความพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="b4d0b-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="b4d0b-135">ตัวอย่างเช่น NA</span><span class="sxs-lookup"><span data-stu-id="b4d0b-135">For example, NA.</span></span> <span data-ttu-id="b4d0b-136">ค่านี้จะช่วยหลีกเลี่ยงการเรียกการรับรองความถูกต้องที่ไม่ถูกต้อง ซึ่งอาจส่งผลให้เกิดข้อผิดพลาด ถ้ามีการใช้ค่าผู้ให้บริการข้อมูลประจำตัวที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b4d0b-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="b4d0b-137">สำหรับผู้ใช้ภายนอกหรือผู้ใช้ที่เป็นแขก ให้เพิ่มชื่อผู้เช่า Azure AD หลังจาก https://sts.windows.net/</span><span class="sxs-lookup"><span data-stu-id="b4d0b-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="b4d0b-138">ในฟิลด์ **อีเมล** ป้อนอยู่อีเมลแบบเต็มของผู้ใช้/ชื่อหลักการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="b4d0b-139">ในฟิลด์ **บริษัท** ให้เลือกบริษัทเริ่มต้นสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="b4d0b-140">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-140">Select **Save**.</span></span>

<span data-ttu-id="b4d0b-141">ค่าต่างๆ สำหรับผู้ให้บริการข้อมูลประจำตัวและรหัสการวัดและส่งข้อมูลทางไกล จะได้รับการอัพเดตตามการเรียก [กราฟ Microsoft](/graph/overview) เมื่อมีการบันทึกเรกคอร์ดผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="b4d0b-142">รหัสการวัดและส่งข้อมูลทางไกลจะขึ้นอยู่กับรหัสออบเจ็กต์/รหัสความปลอดภัย (SID) ของผู้ใช้ใน Azure AD</span><span class="sxs-lookup"><span data-stu-id="b4d0b-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="b4d0b-143">หลังจากที่คุณเพิ่มผู้ใช้แล้ว คุณต้องกําหนดบทบาทและองค์กรตามที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b4d0b-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="b4d0b-144">สำหรับข้อมูลเพิ่มเติม ดู [มอบหมาย Security role ให้กับผู้ใช้](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="b4d0b-145">นอกจากนี้ ยังอาจต้องเชื่อมโยงผู้ใช้กับ **บุคคล** และอัพเดต **ตัวเลือกผู้ใช้** เช่น ภาษา แบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="b4d0b-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="b4d0b-146">เปลี่ยนรหัสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-146">Change a user ID</span></span>
<span data-ttu-id="b4d0b-147">เมื่อต้องการเปลี่ยนแปลงรหัสผู้ใช้ คุณต้องเปลี่ยนชื่อคีย์ในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b4d0b-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="b4d0b-148">เมื่อคุณเปลี่ยนรหัสผู้ใช้โดยใช้กระบวนงานนี้ การตั้งค่าของผู้ใช้ที่เกี่ยวข้องทั้งหมดจะถูกแก้ไขเพื่อใช้รหัสผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="b4d0b-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="b4d0b-149">ตัวอย่างเช่น ข้อมูลการใช้ในตาราง **SysLastValuy** จะถูกอัพเดตเพื่ออ้างอิงรหัสผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="b4d0b-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="b4d0b-150">รหัสผู้ใช้เป็นคีย์หลักของตารางข้อมูลผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4d0b-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="b4d0b-151">การเปลี่ยนชื่อคีย์หลักอาจใช้เวลาสักพักสำหรับผู้ใช้ที่มีอยู่ เนื่องจากมีการอัพเดตการอ้างอิงทั้งหมดไปยังคีย์ในฐานข้อมูลด้วย</span><span class="sxs-lookup"><span data-stu-id="b4d0b-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="b4d0b-152">ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="b4d0b-153">เลือกผู้ใช้ในรายการ และเลือก **ตัวเลือก\> ข้อมูลเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="b4d0b-154">เลือก **เปลี่ยนชื่อ**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-154">Select **Rename**.</span></span>
4. <span data-ttu-id="b4d0b-155">ป้อนค่าใหม่และค่าที่ไม่ซ้ำกันสำหรับรหัสผู้ใช้ และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b4d0b-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="b4d0b-156">เลือก **ใช่** เพื่อยืนยัน</span><span class="sxs-lookup"><span data-stu-id="b4d0b-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4d0b-157">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b4d0b-157">Additional resources</span></span>

<span data-ttu-id="b4d0b-158">สำหรับตัวเลือกเพิ่มเติมเพื่อปรับใช้ผู้ใช้ B2B โปรดดูที่ [ส่งออกผู้ใช้ B2B ไปยัง Azure AD](../implement-b2b.md)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="b4d0b-159">สำหรับข้อมูลเกี่ยวกับบัญชีของระบบที่ตั้งค่าคอนฟิกไว้ล่วงหน้า โปรดดูที่ [บัญชีของระบบที่ตั้งค่าคอนฟิกไว้ล่วงหน้า](../pre-configured-system-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]