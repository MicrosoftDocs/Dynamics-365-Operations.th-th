---
title: "การจัดการประเภทผลิตภัณฑ์"
description: "หัวข้อนี้อธิบายวิธีการที่ผู้จัดการฝ่ายจัดซื้อสามารถใช้ประเภทผลิตภัณฑ์เพื่อการขายปลีก เพื่อจัดการความสัมพันธ์ระหว่างลำดับชั้นของผลิตภัณฑ์เพื่อการขายปลีก และรายละเอียดผลิตภัณฑ์ที่นำออกใช้"
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: th-th
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="62b41-103">การจัดการประเภทและผลิตภัณฑ์ขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="62b41-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="62b41-104">หัวข้อนี้อธิบายวิธีการขั้นสูงในการจัดการประเภทผลิตภัณฑ์เพื่อการขายปลีก และผลิตภัณฑ์ใน Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="62b41-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="62b41-105">การปรับปรุงเหล่านี้ช่วยให้ผู้จัดการฝ่ายจัดซื้อสินค้าสามารถดูโครงสร้างทั่วไปของคุณสมบัติของผลิตภัณฑ์ ระหว่างลำดับชั้นของผลิตภัณฑ์เพื่อการขายปลีกและรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="62b41-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="62b41-106">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการจัดการประเภทผลิตภัณฑ์เพื่อการขายปลีก ไปที่ **ลำดับชั้นของผลิตภัณฑ์เพื่อการขายปลีก** จากพื้นที่ทำงาน **การจัดการประเภทและผลิตภัณฑ์** และบันทึกโครงสร้างขั้นสูงของหน้า **ประเภทผลิตภัณฑ์เพื่อการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="62b41-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![พื้นที่ทำงานการจัดการประเภท & ผลิตภัณฑ์](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="62b41-108">ในรุ่นก่อนหน้านี้ คุณสมบัติผลิตภัณฑ์ถูกแบ่งออกเป็น **คุณสมบัติของผลิตภัณฑ์พื้นฐาน** และ **คุณสมบัติของผลิตภัณฑ์เพื่อการขายปลีก** โดยยึดตามขอบเขตของการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="62b41-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="62b41-109">**คุณสมบัติของผลิตภัณฑ์เพื่อการขายปลีก** เป็น *แบบส่วนกลาง* ตามขอบเขตของการใช้งาน ซึ่งหมายความว่า สำหรับ **คุณสมบัติของผลิตภัณฑ์เพื่อการขายปลีก** ที่กำหนดให้ ค่าเดียวกันจะถูกแบ่งปันให้กับนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="62b41-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="62b41-110">**คุณสมบัติของผลิตภัณฑ์พื้นฐาน** เป็น *เฉพาะนิติบุคคล*</span><span class="sxs-lookup"><span data-stu-id="62b41-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="62b41-111">กล่าวคือ สำหรับ **คุณสมบัติของผลิตภัณฑ์พื้นฐาน** ที่กำหนด ค่าอาจแตกต่างกันระหว่างนิติบุคคล โดยยึดตามความต้องการทางธุรกิจแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="62b41-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="62b41-112">ในโครงสร้างประเภทผลิตภัณฑ์เพื่อการขายปลีกขั้นสูง คุณสมบัติของผลิตภัณฑ์ถูกแบ่งออกทางตรรกะตามการใช้งานภายในกลุ่ม เพื่อสะท้อนโครงสร้างแบบฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="62b41-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![การจัดกลุ่มของฟิลด์ตามขอบเขตของการใช้งาน](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="62b41-114">คุณสามารถสลับระหว่างการจัดการคุณสมบัติเฉพาะนิติบุคคลในนิติบุคคลทั้งหมด และการจัดการสำหรับนิติบุคคลหนึ่ง ๆ</span><span class="sxs-lookup"><span data-stu-id="62b41-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="62b41-115">เมื่อต้องการทำเช่นนี้ ให้เลือก **ดู/แก้ไขสำหรับนิติบุคคลทั้งหมด** หรือ **ดู/แก้ไขสำหรับนิติบุคคลหนึ่งๆ** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="62b41-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![สลับมุมมองระหว่างนิติบุคคลแต่ละราย และนิติบุคคลทั้งหมด](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![สลับมุมมองระหว่างนิติบุคคลแต่ละราย และนิติบุคคลทั้งหมด](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="62b41-118">เมื่อเปรียบเทียบกับรุ่นก่อนหน้า ในโครงประเภทผลิตภัณฑ์เพื่อการขายปลีกใหม่ ผู้จัดการฝ่ายจัดซื้อสินค้ายังสามารถกำหนดค่าเริ่มต้นสำหรับชุดเพิ่มเติมของคุณสมบัติของผลิตภัณฑ์ที่แต่ละระดับประเภทได้</span><span class="sxs-lookup"><span data-stu-id="62b41-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="62b41-119">ในเวลาสร้างผลิตภัณฑ์ ค่าคุณสมบัติของผลิตภัณฑ์ค่าเริ่มต้นเหล่านี้จะถูกสืบทอดโดยผลิตภัณฑ์ โดยยึดตามการเชื่อมโยงกับประเภทการแต่ละประเภทจากลำดับชั้นของผลิตภัณฑ์เพื่อการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="62b41-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="62b41-120">คุณสมบัติของผลิตภัณฑ์ที่สืบทอดมาเหล่านี้ยังสามารถถูกปรับเปลี่ยนได้สำหรับแต่ละผลิตภัณฑ์ เพื่อให้ตรงกับความต้องการทางธุรกิจแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="62b41-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="62b41-121">เลือกคุณสมบัติที่จะอัพเดตผลิตภัณฑ์จากแบบฟอร์มประเภทผลิตภัณฑ์เพื่อการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="62b41-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="62b41-122">คุณสามารถใช้โครงสร้างขั้นสูงใหม่นี้ได้สำหรับคุณสมบัติของผลิตภัณฑ์ เพื่อเลือกว่าคุณสมบัติของผลิตภัณฑ์ที่ปรับปรุงใดต้องถูกส่งไปยังผลิตภัณฑ์ที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="62b41-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![มุมมองขั้นสูงใหม่ของผลิตภัณฑ์ที่ปรับปรุง](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="62b41-124">ผู้จัดการฝ่ายจัดซื้อสามารถปรับเปลี่ยนคุณสมบัติของผลิตภัณฑ์ที่สืบทอดมาเหล่านี้สำหรับแต่ละผลิตภัณฑ์ เพื่อให้ตรงกับความต้องการทางธุรกิจแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="62b41-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


