---
title: "ความปลอดภัยของผู้ใช้พอร์ทัลของผู้จัดจำหน่าย"
description: "บทความนี้อธิบายวิธีการตั้งค่าความปลอดภัยสำหรับผู้จัดจำหน่ายภายนอกที่ใช้เว็บไซต์ของผู้จัดจำหน่าย ข้อมูลนี้ใช้กับ Dynamics AX เวอร์ชันกุมภาพันธ์ 2016 &amp; พฤษภาคม 2016 เท่านั้น"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ab096bcc7003f60851077d9c7e03b16c5d46ce2a
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="41839-104">ความปลอดภัยของผู้ใช้พอร์ทัลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41839-104">Vendor portal user security</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="41839-105">บทความนี้อธิบายวิธีการตั้งค่าความปลอดภัยสำหรับผู้จัดจำหน่ายภายนอกที่ใช้เว็บไซต์ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41839-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="41839-106">ข้อมูลนี้ใช้กับ Dynamics AX เวอร์ชันกุมภาพันธ์ 2016 &amp; พฤษภาคม 2016 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="41839-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="41839-107">ฟังก์ชันพอร์ทัลของผู้จัดจำหน่ายถูกแทนที่โดยฟังก์ชันการทำงานร่วมกันกับผู้จัดจำหน่ายแบบขยายใน Dynamics 365 for Operations เวอร์ชัน 1611</span><span class="sxs-lookup"><span data-stu-id="41839-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="41839-108">ดูข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าการรักษาความปลอดภัยสำหรับการทำงานร่วมกันกับผู้จัดจำหน่าย ดู [ตั้งค่าและรักษาการทำงานร่วมกันกับผู้จัดจำหน่าย](set-up-maintain-vendor-collaboration.md)</span><span class="sxs-lookup"><span data-stu-id="41839-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="41839-109">พอร์ทัลผู้จัดจำหน่ายแสดงถึงชุดที่จำกัดของข้อมูลเกี่ยวกับใบสั่งซื้อ (POs) กับผู้จัดจำหน่ายภายนอก</span><span class="sxs-lookup"><span data-stu-id="41839-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="41839-110">เป็นสิ่งสำคัญที่คุณตั้งค่าสิทธิ์ผู้ใช้อย่างถูกต้องสำหรับพอร์ทัลผู้จัดจำหน่ายใน Microsoft Dynamics AX เพื่อที่ผู้จัดจำหน่ายจะได้ไม่มีการเข้าถึงข้อมูลเพิ่มเติมในการติดตั้ง Dynamics AX ของคุณโดยไม่ได้ตั้งใจ</span><span class="sxs-lookup"><span data-stu-id="41839-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="41839-111">**สิ่งสำคัญ:** ไม่เหมือนกับผู้ใช้รายอื่น ผู้จัดจำหน่ายภายนอกไม่ควรมีบทบาท **SystemUser**</span><span class="sxs-lookup"><span data-stu-id="41839-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="41839-112">บทบาท **SystemUser** ช่วยให้มีการเข้าถึงชุดของสิทธิ์ที่ไม่เหมาะสมสำหรับผู้ใช้ภายนอก</span><span class="sxs-lookup"><span data-stu-id="41839-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="41839-113">การตั้งค่าผู้ใช้พอร์ทัลผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41839-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="41839-114">ก่อนที่คุณจะสร้างบัญชีผู้ใช้สำหรับบุคคลที่จะใช้พอร์ทัลผู้จัดจำหน่าย คุณต้องตั้งค่าผู้จัดจำหน่ายเพื่ออนุญาตให้มีการทำงานร่วมกันของพอร์ทัลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41839-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="41839-115">ใช้ฟิลด์ **การทำงานร่วมกันกับใบสั่งซื้อ** บนแท็บ **ทั่วไป** ในหน้า **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="41839-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="41839-116">ผู้จัดจำหน่ายภายนอกที่ใช้พอร์ทัลผู้จัดจำหน่าย ต้องมีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="41839-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="41839-117">ต้องมีการลงทะเบียนบัญชีผู้ใช้ Microsoft Azure Active Directory (AAD) สำหรับผู้จัดจำหน่ายในหน้า **ผู้ใช้** ใน Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="41839-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="41839-118">ผู้จัดจำหน่ายต้องมีบทบาทความปลอดภัย **ผู้จัดจำหน่าย (ภายนอก)** ไม่ใช่บทบาท **SystemUser**</span><span class="sxs-lookup"><span data-stu-id="41839-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="41839-119">**หมายเหตุ:** บทบาท **SystemUser** ได้รับอนุญาตโดยอัตโนมัติเมื่อคุณสร้างบัญชีผู้ใช้ใหม่ใน Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="41839-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="41839-120">ดังนั้น คุณต้องลบบทบาทนั้นและรับทราบข้อความเตือนที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="41839-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="41839-121">ผู้ใช้ผู้จัดจำหน่ายไม่ควรได้รับสิทธิ์ในการเพิ่มฟิลด์เพิ่มเติมจากตารางใบสั่งซื้อไปยังมุมมองของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="41839-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="41839-122">บนแท็บ **การตั้งค่าส่วนบุคคล** บนแท็บ **ผู้ใช้** ให้ตั้งค่าตัวเลือก **อนุญาตการกำหนดเป็นแบบส่วนบุคคลแบบชัดแจ้ง** สำหรับผู้ใช้เป็น **ไม่ใช่**</span><span class="sxs-lookup"><span data-stu-id="41839-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="41839-123">บัญชีผู้ใช้ต้องเชื่อมโยงกับผู้ติดต่อที่ลงทะเบียนแล้ว</span><span class="sxs-lookup"><span data-stu-id="41839-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="41839-124">ในหน้า **ผู้ใช้** ให้เลือกผู้ติดต่อในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="41839-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="41839-125">บุคคลที่คุณเลือกควรมีบทบาท **ผู้ติดต่อ** สำหรับผู้จัดจำหน่ายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="41839-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="41839-126">ถ้าบุคคลเดียวกันต้องการเข้าถึงพอร์ทัลผู้จัดจำหน่ายสำหรับบัญชีผู้จัดจำหน่ายหลายบัญชี (อาจจะสำหรับนิติบุคคลอื่น) บัญชีผู้ใช้ของบุคคลนั้นแต่ละบัญชีต้องเชื่อมโยงกับผู้ติดต่อจดทะเบียนเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="41839-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="41839-127">บทบาท **ผู้จัดจำหน่าย (ภายนอก)** รวมความสามารถพื้นฐานทั้งหมดที่จำเป็นเพื่อให้สามารถใช้ฟังก์ชันที่พร้อมใช้งานในพอร์ทัลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41839-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="41839-128">การตั้งค่านี้ช่วยรับประกันว่า อินเทอร์เฟสผู้ใช้ที่ผู้ใช้ภายนอกมองเห็นจะถูกโฟกัสไปที่สถานการณ์จำลองที่กำหนดไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="41839-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="41839-129">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="41839-129">See also</span></span>
--------

[<span data-ttu-id="41839-130">การทำงานร่วมกันกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41839-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




