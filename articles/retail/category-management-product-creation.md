---
title: "การจัดการและการสร้างประเภทผลิตภัณฑ์"
description: "หัวข้อนี้อธิบายถึงการปรับปรุงประสบการณ์ใช้งานการจัดการสำหรับประเภทผลิตภัณฑ์เพื่อการขายปลีก การปรับปรุงเหล่านี้ช่วยให้ผู้จัดการฝ่ายจัดซื้อสินค้ามีความสัมพันธ์ระหว่างลำดับชั้นของผลิตภัณฑ์เพื่อการขายปลีกและรายละเอียดผลิตภัณฑ์ที่นำออกใช้"
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 6b9afb40b68b672514c083d99efbc9bd098dd561
ms.openlocfilehash: b158ff5b277c125e0aa158c071007ed8a0f25482
ms.contentlocale: th-th
ms.lasthandoff: 10/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="f8b6d-104">การจัดการและการสร้างประเภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f8b6d-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="f8b6d-105">การปรับปรุงประสบการณ์ใช้งานการจัดการสำหรับประเภทผลิตภัณฑ์เพื่อการขายปลีกช่วยให้ผู้จัดการฝ่ายจัดซื้อสินค้ามีความสัมพันธ์ระหว่างลำดับชั้นของผลิตภัณฑ์เพื่อการขายปลีกและรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="f8b6d-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="f8b6d-106">เมื่อต้องการดูการปรับปรุงเหล่านี้ ในพื้นที่ทำงาน **การจัดการประเภทและผลิตภัณฑ์** เลือก **ลำดับชั้นของผลิตภัณฑ์เพื่อการขายปลีก** เพื่อเปิดหน้า **โครงสร้างใหม่ของประเภทผลิตภัณฑ์เพื่อการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="f8b6d-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="f8b6d-107">ในการนำออกใช้ก่อนหน้านี้ คุณสมบัติผลิตภัณฑ์ถูกแบ่งออกเป็นคุณสมบัติพื้นฐานของผลิตภัณฑ์และคุณสมบัติของผลิตภัณฑ์เพื่อการขายปลีก ตามขอบเขตของการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f8b6d-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="f8b6d-108">คุณสมบัติของผลิตภัณฑ์เพื่อการขายปลีกเป็น *สากล*</span><span class="sxs-lookup"><span data-stu-id="f8b6d-108">Retail product properties were *global*.</span></span> <span data-ttu-id="f8b6d-109">กล่าวคือ สำหรับคุณสมบัติของผลิตภัณฑ์ที่กำหนด ค่าเดียวกันถูกใช้ร่วมกันระหว่างนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f8b6d-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="f8b6d-110">คุณสมบัติพื้นฐานของผลิตภัณฑ์เป็นสิ่ง *เฉพาะนิติบุคคล*</span><span class="sxs-lookup"><span data-stu-id="f8b6d-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="f8b6d-111">กล่าวคือคุณสมบัติของผลิตภัณฑ์ที่กำหนดอาจแตกต่างระหว่างนิติบุคคล ตามความต้องการทางธุรกิจแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="f8b6d-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="f8b6d-112">ด้วยการปรับปรุงเหล่านี้ สำหรับคุณสมบัติของผลิตภัณฑ์ในประเภทผลิตภัณฑ์เพื่อการขายปลีก เรายังคงแบ่งฟิลด์ต่าง ๆ ตามความเกี่ยวข้องภายในกลุ่ม เพื่อสะท้อนโครงสร้างแบบฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="f8b6d-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="f8b6d-113">คุณสามารถสลับระหว่างการจัดการคุณสมบัติเฉพาะนิติบุคคลในนิติบุคคลทั้งหมด และการจัดการสำหรับนิติบุคคลหนึ่ง ๆ</span><span class="sxs-lookup"><span data-stu-id="f8b6d-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="f8b6d-114">เพียงแค่เลือก **ดู/แก้ไขสำหรับนิติบุคคลทั้งหมด** หรือ **ดู/แก้ไขสำหรับนิติบุคคลหนึ่ง ๆ** ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f8b6d-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="f8b6d-115">นอกจากนี้ผู้จัดการฝ่ายจัดซื้อสินค้ายังสามารถกำหนดค่าเริ่มต้นสำหรับชุดเพิ่มเติมของคุณสมบัติของผลิตภัณฑ์ตามระดับของแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="f8b6d-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="f8b6d-116">ค่าคุณสมบัติเหล่านี้จะถูกสืบทอดโดยเรียงตามผลิตภัณฑ์ ตามความเชื่อมโยงกับประเภทในเวลาที่มีการสร้างผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f8b6d-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="f8b6d-117">เลือกคุณสมบัติที่จะอัพเดตผลิตภัณฑ์จากแบบฟอร์มประเภทผลิตภัณฑ์เพื่อการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="f8b6d-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="f8b6d-118">คุณสามารถใช้คุณสมบัติการจัดกลุ่มทางตรรกะเพื่อเลือกคุณสมบัติของผลิตภัณฑ์ที่ปรับปรุงแล้วที่ควรจะผลักดันเป็นผลิตภัณฑ์ที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="f8b6d-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="f8b6d-119">ผู้จัดการฝ่ายจัดซื้อสามารถปรับเปลี่ยนคุณสมบัติของผลิตภัณฑ์ที่สืบทอดมาเหล่านี้สำหรับแต่ละผลิตภัณฑ์ เพื่อให้ตรงกับความต้องการทางธุรกิจแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="f8b6d-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

