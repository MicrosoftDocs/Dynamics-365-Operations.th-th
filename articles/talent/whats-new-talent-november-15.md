---
title: "มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (15 พฤศจิกายน 2018)"
description: "หัวข้อนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent Core HR"
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: th-th
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a><span data-ttu-id="37d27-103">มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (15 พฤศจิกายน 2018)</span><span class="sxs-lookup"><span data-stu-id="37d27-103">What's new or changed in Dynamics 365 for Talent Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="37d27-104">**สร้าง 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="37d27-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="37d27-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="37d27-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="37d27-106">การเปลี่ยนแปลง/การแก้ไขอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="37d27-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="37d27-107">ไม่สามารถเปลี่ยนตำแหน่งปัจจุบันของพนักงานเป็นตำแหน่งที่เปิดในอนาคตได้</span><span class="sxs-lookup"><span data-stu-id="37d27-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="37d27-108">มีการเปลี่ยนแปลงเพื่อเปิดใช้งานการโอนย้ายตำแหน่ง เมื่อตำแหน่งพร้อมใช้งานเฉพาะในอนาคต</span><span class="sxs-lookup"><span data-stu-id="37d27-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="37d27-109">ตำแหน่งไม่แสดง เมื่อสร้างพนักงานใหม่</span><span class="sxs-lookup"><span data-stu-id="37d27-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="37d27-110">มีการทำการเปลี่ยนแปลงเพื่อแสดงตำแหน่งที่เปิดทั้งหมดที่พร้อมใช้งานสำหรับการกำหนด เมื่อจ้างพนักงานใหม่ใน Talent</span><span class="sxs-lookup"><span data-stu-id="37d27-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="37d27-111">ซึ่งรวมถึงตำแหน่งในอดีต หรือถ้าตำแหน่งได้ถูกกำหนดวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="37d27-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="37d27-112">ขณะนี้ ตำแหน่งจะปรากฏอย่างถูกต้องตามวันที่เริ่มต้นการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="37d27-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="37d27-113">วันที่สิ้นสุดการจ้างงานกำลังแสดงตามการตั้งค่าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="37d27-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="37d27-114">มีการทำการเปลี่ยนแปลงไปยังรายการพนักงานในอดีตไปยังบัญชีสำหรับการออฟเซ็ตโซนเวลาใดๆ สำหรับโซนเวลาที่ต้องการของพนักงาน เมื่อดูวันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="37d27-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="37d27-115">ลิงค์รายการงานที่กำหนดให้กับฉันไม่แสดงข้อมูลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="37d27-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="37d27-116">ด้วยการเปลี่ยนแปลงนี้ การนำทางไปยังรายละเอียดของรายการงานแต่ละรายการในรายการ จะแสดงข้อมูลที่ถูกต้องสำหรับสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="37d27-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="37d27-117">ปัญหานี้เกิดขึ้นกับตัวเลือกความปลอดภัยขั้นสูงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="37d27-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="37d27-118">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="37d27-118">Known issue</span></span>

- <span data-ttu-id="37d27-119">**ปัญหา**: เมื่อเพิ่มสิ่งที่แนบมาใหม่กับผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** จะกลายเป็นสีเทา</span><span class="sxs-lookup"><span data-stu-id="37d27-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="37d27-120">**วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่าก FactBoxes บนหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="37d27-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="37d27-121">ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="37d27-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="37d27-122">(ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)</span><span class="sxs-lookup"><span data-stu-id="37d27-122">(This issue will be fixed in the next platform update.)</span></span>

