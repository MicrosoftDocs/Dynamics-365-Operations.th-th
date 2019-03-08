---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (1 ตุลาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97820cd25ece48dc0b8045d9ba509d0971ca5aad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306397"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a><span data-ttu-id="b03f2-103">มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (1 ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="b03f2-103">What's new or changed in Dynamics 365 for Talent Core HR (October 1, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b03f2-104">**สร้าง 8.1.1035.0**</span><span class="sxs-lookup"><span data-stu-id="b03f2-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="b03f2-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="b03f2-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="b03f2-106">ปิดการตรวจสอบความถูกต้องของการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b03f2-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="b03f2-107">การตรวจสอบความถูกต้องของข้อมูลการชำระเงินทางอิเล็กทรอนิกส์จะเกิดขึ้น ถ้าคุณตั้งค่าการเบิกจ่ายเงินโดยตรงสำหรับการฝากเงินเข้าบัญชีธนาคาร ผ่านทางพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน** (ESS) หรือในแบบฟอร์มพนักงานโดยตรง</span><span class="sxs-lookup"><span data-stu-id="b03f2-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="b03f2-108">ตัวเลือกนี้ช่วยให้คุณมีความยืดหยุ่นเพื่อลบการตรวจสอบนั้น ถ้าคุณไม่ต้องการการตรวจสอบความถูกต้องสำหรับยอดเงินและค่าที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="b03f2-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="b03f2-109">คุณลักษณะนี้มีประโยชน์ ถ้าคุณกำลังรวมกับระบบค่าจ้างภายนอกที่มีข้อกำหนดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b03f2-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="b03f2-110">การบริการตนเองของผู้จัดการ - เพิ่มเป้าหมายสำหรับสมาชิกในทีม ผ่านไทล์เป้าหมายประสิทธิภาพของทีมงาน</span><span class="sxs-lookup"><span data-stu-id="b03f2-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="b03f2-111">ก่อนการนำออกใช้นี้ ผู้จัดการสามารถเพิ่มเป้าหมายไปยังพนักงานของพวกเขาทีละรายการ โดยใช้เป้าหมายผลการปฏิบัติงานที่เกี่ยวข้องกับพนักงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="b03f2-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="b03f2-112">ด้วยการอัพเดตนี้ ผู้จัดการสามารถเข้าถึงไทล์ **เป้าหมายผลการปฏิบัติงานของทีม** และสร้างเป้าหมายใหม่ โดยการเลือกผู้ใต้บังคับบัญชาโดยตรงของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="b03f2-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="b03f2-113">การบริการตนเองของผู้จัดการ - เพิ่มรีวิวสำหรับสมาชิกในทีม ผ่านไทล์รีวิวประสิทธิภาพของทีมงาน</span><span class="sxs-lookup"><span data-stu-id="b03f2-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="b03f2-114">ก่อนการนำออกใช้นี้ ผู้จัดการสามารถเพิ่มรีวิวไปยังพนักงานของพวกเขาทีละรายการ โดยใช้รีวิวที่เกี่ยวข้องกับพนักงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="b03f2-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="b03f2-115">ด้วยการอัพเดตนี้ ผู้จัดการสามารถเข้าถึงไทล์ **รีวิวผลการปฏิบัติงานของทีม** และสร้างรีวิวใหม่ โดยการเลือกผู้ใต้บังคับบัญชาโดยตรงของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="b03f2-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="b03f2-116">ตั้งค่าคอนฟิกตัวเลือกการแบ่งตามสัดส่วนตามแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="b03f2-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="b03f2-117">องค์กรให้รางวัลเวลาหยุดพักแตกต่างกัน ตามเวลาที่พนักงานเข้า และออกจากบริษัท</span><span class="sxs-lookup"><span data-stu-id="b03f2-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="b03f2-118">สำหรับองค์กรบางแห่ง พนักงานได้รับการปันส่วนทั้งหมดตามวันที่เริ่มต้นของพวกเขา ในขณะที่องค์กรอื่นๆ คิดค่ารางวัล</span><span class="sxs-lookup"><span data-stu-id="b03f2-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="b03f2-119">มีการระบุตัวเลือกใหม่ในรุ่นนี้เพื่อเลือกวิธีคิดค่ารางวัลและค้างรับค้างจ่ายสำหรับพนักงานที่เข้าและพนักงานที่ลาออกในองค์กร</span><span class="sxs-lookup"><span data-stu-id="b03f2-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="b03f2-120">ตัวเลือกได้แก่: แบ่งตามส่วน ค้างรับค้างจ่ายทั้งหมด และไม่มีการค้างรับค้างจ่าย</span><span class="sxs-lookup"><span data-stu-id="b03f2-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="b03f2-121">การเปลี่ยนแปลงอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b03f2-121">Other changes</span></span>

-   <span data-ttu-id="b03f2-122">เอนทิตีของพนักงานที่ปรับปรุง - ตำแหน่ง **ส่วนบุคคล** ขณะนี้สามารถได้รับการปรับปรุงได้โดยใช้การจัดการ add-in/ข้อมูล Excel</span><span class="sxs-lookup"><span data-stu-id="b03f2-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="b03f2-123">การเปลี่ยนแปลงความปลอดภัยเพื่ออนุญาตให้มีการลบปุ่ม **ลบ** และ **ปิดการใช้งาน** ในการบริการตนเองของพนักงานสำหรับข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b03f2-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="b03f2-124">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="b03f2-124">Known issue</span></span>

-   <span data-ttu-id="b03f2-125">**ปัญหา:** เมื่อเพิ่มสิ่งที่แนบมาใหม่ไปยังผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** ถูกแรเงา **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่า FactBoxes ในหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="b03f2-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="b03f2-126">ถ้า FactBoxes ถูกปิด เมื่อหน้า**ผู้ปฏิบัติงาน** ถูกโหลด ปุ่ม **เอกสารแนบ** จะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b03f2-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="b03f2-127">(ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)</span><span class="sxs-lookup"><span data-stu-id="b03f2-127">(This issue will be fixed in the next platform update.)</span></span>
