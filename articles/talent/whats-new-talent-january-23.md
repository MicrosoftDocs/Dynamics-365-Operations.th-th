---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (23 มกราคม 2019)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f27698c257301f52e5c77eaa8a04ca13a0315825
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "859639"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="7671e-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (23 มกราคม 2019)</span><span class="sxs-lookup"><span data-stu-id="7671e-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7671e-104">**สร้าง 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="7671e-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="7671e-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="7671e-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="7671e-106">การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="7671e-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="7671e-107">การนำเข้าของค่าตอบแทนคงที่ของพนักงานที่ไม่ทำงานเมื่อสร้างเรกคอร์ดค่าตอบแทนคงที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="7671e-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="7671e-108">ทำการเปลี่ยนแปลงกับเอนทิตี้ค่าตอบแทนคงที่ของพนักงานในการดึงข้อมูลระดับค่าตอบแทนเมื่อมีการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="7671e-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="7671e-109">ก่อนที่จะมีการนำออกใช้นี้ ข้อความที่แสดงบ่งชี้ว่าจำเป็นต้องมีระดับ</span><span class="sxs-lookup"><span data-stu-id="7671e-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="7671e-110">ลบฟิลด์ยอดดุลต่ำสุดออกจากกล่องโต้ตอบคำขอเวลาหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="7671e-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="7671e-111">ฟิลด์ **ยอดดุลต่ำสุด** ถูกลบออกจากกล่องโต้ตอบ **คำขอเวลาหยุดงาน**</span><span class="sxs-lookup"><span data-stu-id="7671e-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="7671e-112">การเปลี่ยนแปลงนี้มีผลกระทบต่อพื้นที่ทั้งหมดที่สามารถร้องขอเวลาหยุดงานได้</span><span class="sxs-lookup"><span data-stu-id="7671e-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="7671e-113">การอัพเกรดข้อมูลสำหรับระดับค่าตอบแทนที่ไม่มีการปรับปรุงในสถานการณ์จำลองทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7671e-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="7671e-114">มีการเปลี่ยนแปลงเพื่อปรับปรุงระดับค่าตอบแทนในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="7671e-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="7671e-115">การเปลี่ยนแปลงนี้จะเติมระดับค่าตอบแทนสำหรับแผนคงที่สำหรับงานที่กำหนดให้กับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="7671e-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="7671e-116">ข้อมูลค่าจ้างในหน้าจัดการการเปลี่ยนแปลงจะพร้อมใช้งานเมื่อล็อกอินเป็นผู้ดูแลระบบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7671e-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="7671e-117">การเปลี่ยนแปลงนี้อนุญาตให้พนักงานที่มีการเข้าถึงบทบาทของเจ้าหน้าที่ฝ่ายค่าจ้างไปยังข้อมูลค่าจ้างในหน้า **เปลี่ยนแปลงเส้นเวลา > จัดการการเปลี่ยนแปลง** ให้กับตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="7671e-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="7671e-118">ค่าเริ่มต้นฟิลด์งานในตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7671e-118">Job fields default to positions</span></span>
<span data-ttu-id="7671e-119">เมื่อเปลี่ยนตำแหน่งงาน ฟิลด์งานจะเริ่มต้นกับตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="7671e-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="7671e-120">ข้อความแจ้งเตือนจะปรากฏขึ้นเพื่อให้สามารถเลือกที่จะยอมรับค่าเริ่มต้นหรือเก็บค่าที่มีอยู่สำหรับฟิลด์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="7671e-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="7671e-121">ปฏิทินและช่วงทดลองงานจะไม่แสดงขึ้นสำหรับพนักงานที่จ้างไว้สำหรับอนาคต</span><span class="sxs-lookup"><span data-stu-id="7671e-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="7671e-122">ด้วยการเปลี่ยนแปลงนี้ ฟิลด์ **ช่วงทดลองงาน** และ **ปฏิทิน** ถูกเพิ่มไปยังหน้า **จัดการการเปลี่ยนแปลง** เพื่ออนุญาตให้ป้อนข้อมูลสำหรับพนักงานในอดีตและในอนาคต</span><span class="sxs-lookup"><span data-stu-id="7671e-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="7671e-123">แพลตฟอร์ม update 23</span><span class="sxs-lookup"><span data-stu-id="7671e-123">Platform update 23</span></span>
<span data-ttu-id="7671e-124">การแก้ไขบักรองถูกรวมเป็นส่วนหนึ่งของการปรับปรุงแพลตฟอร์ม 23</span><span class="sxs-lookup"><span data-stu-id="7671e-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="7671e-125">ดูข้อมูลเพิ่มเติม ดูที่ [มีอะไรใหม่หรือที่เปลี่ยนแปลงในการปรับปรุงแพลตฟอร์ม Dynamics 365 for Finance and Operations 23 (มกราคม 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23)</span><span class="sxs-lookup"><span data-stu-id="7671e-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
