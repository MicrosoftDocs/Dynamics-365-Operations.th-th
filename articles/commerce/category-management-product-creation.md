---
title: จัดการประเภทผลิตภัณฑ์และผลิตภัณฑ์
description: หัวข้อนี้อธิบายวิธีการที่ผู้จัดการฝ่ายจัดซื้อสามารถใช้ประเภทผลิตภัณฑ์ เพื่อจัดการความสัมพันธ์ระหว่างลำดับชั้นของผลิตภัณฑ์เพื่อการค้า และรายละเอียดผลิตภัณฑ์ที่นำออกใช้
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6e0c6a8048b5a2ef9a48495cd5e2609a1324a6e2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024162"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="e8c46-103">จัดการประเภทผลิตภัณฑ์และผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e8c46-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="e8c46-104">หัวข้อนี้อธิบายวิธีขั้นสูงในการจัดการประเภทผลิตภัณฑ์ และผลิตภัณฑ์ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e8c46-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e8c46-105">การปรับปรุง ช่วยให้ผู้จัดการฝ่ายจัดซื้อสินค้าสามารถดูโครงสร้างของคุณสมบัติของผลิตภัณฑ์ ที่ใช้ร่วมกันระหว่างลำดับชั้นของผลิตภัณฑ์และรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="e8c46-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="e8c46-106">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการจัดการกับประเภทผลิตภัณฑ์ ในพื้นที่ทำงาน **การจัดการประเภทและผลิตภัณฑ์** เลือกไทล์ **ลำดับชั้นของผลิตภัณฑ์การค้า**</span><span class="sxs-lookup"><span data-stu-id="e8c46-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="e8c46-107">โปรดสังเกตโครงสร้างขั้นสูงของหน้า **ลำดับชั้นของผลิตภัณฑ์การค้า** ซึ่งปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="e8c46-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="e8c46-108">ในรุ่นก่อนหน้านี้ของแอป คุณสมบัติผลิตภัณฑ์ถูกแบ่งออกเป็น *คุณสมบัติของผลิตภัณฑ์พื้นฐาน* และ *คุณสมบัติของผลิตภัณฑ์เพื่อการขายปลีก* โดยยึดตามขอบเขตของการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e8c46-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="e8c46-109">คุณสมบัติของผลิตภัณฑ์ขายปลีกเป็น *แบบสากล* ในขอบเขตของการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e8c46-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="e8c46-110">กล่าวคือ สำหรับคุณสมบัติของผลิตภัณฑ์ที่กำหนด ค่าเดียวกันถูกใช้ร่วมกันระหว่างนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e8c46-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="e8c46-111">ในทางตรงกันข้าม คุณสมบัติของผลิตภัณฑ์พื้นฐานเป็น *แบบเฉพาะนิติบุคคล*</span><span class="sxs-lookup"><span data-stu-id="e8c46-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="e8c46-112">กล่าวคือ สำหรับคุณสมบัติของผลิตภัณฑ์พื้นฐานที่กำหนด ค่าอาจแตกต่างกันระหว่างนิติบุคคล โดยยึดตามความต้องการทางธุรกิจแต่ละรายการของนิติบุคคลแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="e8c46-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="e8c46-113">ในโครงสร้างประเภทผลิตภัณฑ์ขั้นสูง คุณสมบัติของผลิตภัณฑ์ถูกแบ่งออกทางตรรกะตามการใช้งานในกลุ่ม เพื่อสะท้อนโครงสร้างของโครงสร้างแบบฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="e8c46-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![ฟิลด์ถูกจัดกลุ่มตามขอบเขตคุณสมบัติของการใช้งาน](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="e8c46-115">คุณสามารถสลับระหว่างการจัดการคุณสมบัติเฉพาะนิติบุคคลในนิติบุคคลทั้งหมด และการจัดการสำหรับนิติบุคคลหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="e8c46-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="e8c46-116">เมื่อต้องการจัดการคุณสมบัตินิติบุคคลทั้งหมด เลือก **ดูสำหรับนิติบุคคลทั้งหมด** (หรือ **แก้ไขสำหรับนิติบุคคลทั้งหมด**)</span><span class="sxs-lookup"><span data-stu-id="e8c46-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![ดู/แก้ไขสำหรับนิติบุคคลทั้งหมด](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="e8c46-118">เมื่อต้องการจัดการคุณสมบัติสำหรับนิติบุคคลหนึ่งๆ เลือก **ดูสำหรับนิติบุคคลหนึ่งๆ** (หรือ **แก้ไขสำหรับนิติบุคคลหนึ่งๆ**)</span><span class="sxs-lookup"><span data-stu-id="e8c46-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![ดู/แก้ไขสำหรับนิติบุคคลหนึ่งๆ](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="e8c46-120">นอกจากนี้ ในโครงสร้างประเภทผลิตภัณฑ์ขั้นสูง ขณะนี้ผู้จัดการฝ่ายจัดซื้อสินค้าสามารถกำหนดค่าเริ่มต้นสำหรับชุดเพิ่มเติมของคุณสมบัติของผลิตภัณฑ์ที่แต่ละระดับประเภทได้</span><span class="sxs-lookup"><span data-stu-id="e8c46-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="e8c46-121">จากนั้น เมื่อมีการสร้างผลิตภัณฑ์ ค่าคุณสมบัติของผลิตภัณฑ์ค่าเริ่มต้นเหล่านี้จะถูกสืบทอดโดยผลิตภัณฑ์ โดยยึดตามการเชื่อมโยงของคุณสมบัติเหล่านั้นกับประเภทแต่ละประเภทในลำดับชั้นของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e8c46-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="e8c46-122">คุณสมบัติของผลิตภัณฑ์ที่สืบทอดมาเหล่านี้ยังสามารถถูกปรับเปลี่ยนได้สำหรับแต่ละผลิตภัณฑ์ เพื่อให้ตรงกับความต้องการทางธุรกิจแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="e8c46-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="e8c46-123">การเลือกคุณสมบัติเพื่ออัพเดตผลิตภัณฑ์ในหน้าลำดับชั้นผลิตภัณฑ์เพื่อการค้า</span><span class="sxs-lookup"><span data-stu-id="e8c46-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="e8c46-124">คุณสามารถใช้โครงสร้างขั้นสูงใหม่นี้ได้สำหรับคุณสมบัติของผลิตภัณฑ์ เพื่อเลือกคุณสมบัติของผลิตภัณฑ์ที่ปรับปรุงที่ต้องถูกส่งไปยังผลิตภัณฑ์ที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="e8c46-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="e8c46-125">ในหน้า **ลำดับชั้นของผลิตภัณฑ์การค้า** บนบานหน้าต่างการดำเนินการ เลือก **ประเภท** แล้วจากนั้น เลือก **อัพเดตผลิตภัณฑ์** เพื่อเปิดกล่องโต้ตอบ **อัพเดตผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="e8c46-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![กล่องโต้ตอบการปรับปรุงผลิตภัณฑ์](media/NewUpdateProductsEnhancedView.PNG)
