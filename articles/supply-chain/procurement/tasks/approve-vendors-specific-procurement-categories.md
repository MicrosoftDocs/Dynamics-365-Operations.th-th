---
title: อนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อเฉพาะ
description: หัวข้อนี้จะอธิบายถึงวิธีการอนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อที่เฉพาะเจาะจงใน Dynamics 365 Supply Chain Management
author: RichardLuan
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c337fd6c2c7cea088b2151bebb54cec326c5240d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237336"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="870a3-103">อนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="870a3-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="870a3-104">หัวข้อนี้จะอธิบายถึงวิธีการอนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อที่เฉพาะเจาะจงใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="870a3-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="870a3-105">เมื่อมีการสร้างใบสั่งซื้อ อาจจำเป็นต้องเลือกผู้จัดจำหน่ายที่ได้รับอนุมัติหรือที่ต้องการ โดยขึ้นอยู่กับวิธีตั้งค่านโยบายการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="870a3-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="870a3-106">กระบวนงานนี้แสดงวิธีการระบุว่าผู้จัดจำหน่ายได้รับอนุมัติหรือเป็นที่ต้องการสำหรับประเภทการจัดซื้อเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="870a3-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="870a3-107">งานนี้อาจมักจะถูกดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหา</span><span class="sxs-lookup"><span data-stu-id="870a3-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="870a3-108">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="870a3-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="870a3-109">ในบานหน้าต่างการนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="870a3-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="870a3-110">เลือกผู้จัดจำหน่ายที่คุณต้องการเพื่อกำหนดเป็นผู้จัดจำหน่ายที่ต้องการหรือได้รับอนุมัติสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="870a3-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="870a3-111">ในบานหน้าต่างการดำเนินการ เลือก **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="870a3-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="870a3-112">เลือก **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="870a3-112">Select **Categories**.</span></span>
5. <span data-ttu-id="870a3-113">เลือก **เพิ่มประเภท**</span><span class="sxs-lookup"><span data-stu-id="870a3-113">Select **Add category**.</span></span>
6. <span data-ttu-id="870a3-114">ในฟิลด์ **ประเภท** เลือก **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**</span><span class="sxs-lookup"><span data-stu-id="870a3-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="870a3-115">ในฟิลด์ **สถานะประเภทผู้จัดจำหน่าย** เลือก **เป็นที่ต้องการ**</span><span class="sxs-lookup"><span data-stu-id="870a3-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="870a3-116">สามารถระบุผู้จัดจำหน่ายที่ต้องการได้มากกว่าหนี่งรายสำหรับหนึ่งประเภท</span><span class="sxs-lookup"><span data-stu-id="870a3-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="870a3-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="870a3-117">Select **Save**.</span></span>
9. <span data-ttu-id="870a3-118">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > แค็ตตาล็อกการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="870a3-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="870a3-119">ในแผนภูมิ เลือก **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**</span><span class="sxs-lookup"><span data-stu-id="870a3-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="870a3-120">ขยายส่วน **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="870a3-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="870a3-121">ตรวจสอบว่าผู้จัดจำหน่ายที่คุณเลือกปรากฏเป็นผู้จัดจำหน่ายที่ต้องการสำหรับประเภทสำนักงานและโต๊ะเบ็ดเตล็ดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="870a3-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="870a3-122">ถ้าคุณกำลังรันกระบวนงานนี้เป็นคู่มืองาน คุณอาจต้องเลือกปุ่ม **ปลดล็อก** เพื่อให้สามารถเลื่อนลงไปยังรายการของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="870a3-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="870a3-123">นอกจากนี้ ยังสามารถเพิ่มผู้จัดจำหน่ายที่ต้องการและผู้จัดจำหน่ายที่ได้รับอนุมัติในหน้านี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="870a3-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="870a3-124">ในแผนภูมิ ให้ขยาย **OFFICE AND DESK ACCESSORIES** และเลือก **กรรไกร**</span><span class="sxs-lookup"><span data-stu-id="870a3-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="870a3-125">เลือก **ไม่** ในฟิลด์ **สืบทอดผู้จัดจำหน่ายจากประเภทหลัก:**</span><span class="sxs-lookup"><span data-stu-id="870a3-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="870a3-126">เลือก **ใช่** ในฟิลด์ **สืบทอดผู้จัดจำหน่ายจากประเภทหลัก:**</span><span class="sxs-lookup"><span data-stu-id="870a3-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]