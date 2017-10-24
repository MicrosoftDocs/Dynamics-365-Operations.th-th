---
title: "ใช้แค็ตตาล็อกภายนอกสำหรับ PunchOut eProcurement"
description: "หัวข้อนี้อธิบายวิธีการใช้แค็ตตาล็อกภายนอกเพื่อสร้างและส่งใบขอซื้อ"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 035c5d15e5508c78dd66a349defd534bfecc96bb
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="53e12-103">ใช้แค็ตตาล็อกภายนอกสำหรับ PunchOut eProcurement</span><span class="sxs-lookup"><span data-stu-id="53e12-103">Use external catalogs for PunchOut eProcurement</span></span>
<span data-ttu-id="53e12-104">โดยการใช้แค็ตตาล็อกภายนอกสำหรับ PunchOut eProcurement คุณไม่จำเป็นต้องรักษาข้อมูลเกี่ยวกับผลิตภัณฑ์ของผู้จัดจำหน่ายในข้อมูลหลักของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="53e12-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="53e12-105">แทนที่จะทำเช่นนั้น รถเข็นซื้อของบนเว็บไซต์ของผู้จัดจำหน่ายจะถูกแปลงเป็นรายการที่มีข้อมูลผลิตภัณฑ์ที่ถูกต้องของใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="53e12-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="53e12-106">คุณควรหลีกเลี่ยงการรักษาคำอธิบายและราคาของผลิตภัณฑ์ของผู้จัดจำหน่ายในข้อมูลหลักของผลิตภัณฑ์ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="53e12-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="53e12-107">แทนที่จะทำเช่นนั้น ใช้แค็ตตาล็อกภายนอกสำหรับ PunchOut e-procurement</span><span class="sxs-lookup"><span data-stu-id="53e12-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="53e12-108">จากนั้น เมื่อพนักงานสร้างใบขอซื้อ พวกเขาสามารถ "ร้องขอ" ไปยังไซต์แค็ตตาล็อกภายนอกของผู้จัดจำหน่าย (กล่าวคือ พวกเขาจะออกจากระบบของคุณ และไปที่ไซต์ของผู้จัดจำหน่าย)</span><span class="sxs-lookup"><span data-stu-id="53e12-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="53e12-109">ผลิตภัณฑ์ที่เพิ่มไปยังรถเข็นซื้อบนเว็บไซต์ของผู้จัดจำหน่าย สามารถแปลงเป็นรายการใบขอซื้อได้</span><span class="sxs-lookup"><span data-stu-id="53e12-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="53e12-110">ดังนั้น คุณจะได้รับข้อมูลผลิตภัณฑ์ที่ถูกต้อง: รหัสผลิตภัณฑ์ ชื่อ ราคา และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="53e12-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="53e12-111">ในการใช้แค็ตตาล็อกภายนอก พนักงานต้องสร้างใบขอซื้อในหน้า **ใบขอซื้อของฉัน**</span><span class="sxs-lookup"><span data-stu-id="53e12-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="53e12-112">พนักงานที่สร้างใบขอซื้อจะถูกอ้างถึงเป็นผู้จัดเตรียมใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="53e12-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="53e12-113">ในฐานะผู้จัดเตรียม คุณสามารถดำเนินการต่อไปนี้ได้</span><span class="sxs-lookup"><span data-stu-id="53e12-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="53e12-114">ใช้การดำเนินการราายการ **แค็ตตาล็อกภายนอก** เพื่อเปิดหน้าที่รวมแค็ตตาล็อกภายนอกทั้งหมดที่พร้อมใช้งานสำหรับผู้ขอที่ระบุ นิติบุคคลที่จัดซื้อ และหน่วยปฏิบัติงานที่รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="53e12-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="53e12-115">ซึ่งขึ้นอยู่กับสิทธิ์ของคุณ เปลี่ยนผู้ขอ นิติบุคคลที่จัดซื้อ และหน่วยปฏิบัติงานที่รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="53e12-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="53e12-116">การเปลี่ยนแปลงค่าเหล่านั้น อาจเปลี่ยนรายการแค็ตตาล็อกภายนอกที่มีอยู่ไปที่ผู้ขอ</span><span class="sxs-lookup"><span data-stu-id="53e12-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="53e12-117">แค็ตตาล็อกภายนอกที่พร้อมใช้งาน ขึ้นอยู่กับนโยบายการจัดซื้อที่ใช้อยู่ในปัจจุบันสำหรับนิติบุคคลที่จัดซื้อหรือหน่วยปฏิบัติงานรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="53e12-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="53e12-118">นโยบายเหล่านี้สามารถอนุญาต หรือป้องกันการเข้าถึงประเภทของการจัดซื้อเฉพาะอย่าง</span><span class="sxs-lookup"><span data-stu-id="53e12-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="53e12-119">ดังนั้น รายการแค็ตตาล็อกภายนอกที่ได้รับการแม็ปไยังประเภทการจัดซื้อเหล่านี้จะสามารถได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="53e12-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="53e12-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีตั้งค่านโยบาย ให้ดูที่ [นโยบายการจัดซื้อ](../procurement/purchase-policies.md)</span><span class="sxs-lookup"><span data-stu-id="53e12-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="53e12-121">หากต้องการค้นหาแค็ตตาล็อกภายนอกสำหรับประเภทการจัดซื้อเฉพาะ ให้ป้อนข้อความในฟิลด์การค้นหาแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="53e12-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="53e12-122">เมื่อต้องการเพิ่มผลิตภัณฑ์จากผู้จัดจำหน่ายแค็ตตาล็อกภายนอกบนเว็บไซต์ของผู้จัดจำหน่าย ให้คลิกแค็ตตาล็อกภายนอก</span><span class="sxs-lookup"><span data-stu-id="53e12-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="53e12-123">จากนั้นเพิ่มผลิตภัณฑ์ลงในรถเข็นซื้อของและเช็คเอาท์ รายการในรถเข็นซื้อของจะถูกโอนย้ายไปที่ Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="53e12-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="53e12-124">ถ้ามีตัวเลือกสำหรับประเภทการจัดซื้อหลายตัวเลือก ให้เลือกประเภทการจัดซื้อที่ถูกต้องก่อนที่คุณจะเพิ่มรายการในใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="53e12-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="53e12-125">หลังจากที่มีการเพิ่มรายการไปยังใบขอซื้อ คุณสามารถเพิ่มรายการเพิ่มเติมโดยไม่ใช้แค็ตตาล็อกภายนอก</span><span class="sxs-lookup"><span data-stu-id="53e12-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="53e12-126">หรือคุณยังคงสามารถใช้แค็ตตาล็อกภายนอกเพื่อเพิ่มรายการได้</span><span class="sxs-lookup"><span data-stu-id="53e12-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="53e12-127">เมื่อใบขอซื้อพร้อมแล้ว ให้ใช้การดำเนินการ **ลำดับงาน** > **ส่ง** เพื่อที่จะส่งสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="53e12-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

