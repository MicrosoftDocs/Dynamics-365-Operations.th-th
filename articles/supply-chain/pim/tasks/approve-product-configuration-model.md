---
title: อนุมัติแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'การดำเนินกระบวนงานนี้ต้องใช้อย่างน้อยหนึ่งแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ที่จะพร้อมใช้งาน '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa0027382e08a23c4dc1e782773a20db441d4f27
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208374"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="6473c-103">อนุมัติแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6473c-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6473c-104">การดำเนินกระบวนงานนี้ต้องใช้อย่างน้อยหนึ่งแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ที่จะพร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="6473c-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="6473c-105">กระบวนงานนี้ใช้แบบจำลองลำโพงขั้นสูงในข้อมูลบริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="6473c-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="6473c-106">โปรดสังเกตว่า แบบจำลองนี้ได้รับการอนุมัติแล้ว แต่กระบวนงานจะนำคุณผ่านกระบวนการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6473c-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="6473c-107">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="6473c-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="6473c-108">คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6473c-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="6473c-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6473c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6473c-110">เลือกแบบจำลองลำโพงขั้นสูงสำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="6473c-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="6473c-111">คลิกรุ่น</span><span class="sxs-lookup"><span data-stu-id="6473c-111">Click Versions.</span></span>
5. <span data-ttu-id="6473c-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6473c-112">Click New.</span></span>
6. <span data-ttu-id="6473c-113">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6473c-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="6473c-114">การอ้างอิงกับผลิตภัณฑ์แสดงถึงรุ่นของแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="6473c-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="6473c-115">เฉพาะผลิตภัณฑ์หลักที่มีเทคโนโลยีการจัดโครงแบบตามข้อจำกัดเท่านั้นที่จะปรากฏในรายการนี้</span><span class="sxs-lookup"><span data-stu-id="6473c-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="6473c-116">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6473c-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="6473c-117">เลือกเมื่อรุ่นแบบจำลองผลิตภัณฑ์พร้อมจะใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6473c-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="6473c-118">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6473c-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="6473c-119">เลือกวันสิ้นสุดเมื่อรุ่นแบบจำลองผลิตภัณฑ์นี้จะหมดอายุ หรือเลือก ไม่มีการหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="6473c-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="6473c-120">คลิกอนุมัติ เพื่อเปิดแบบฟอร์มกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6473c-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="6473c-121">ในฟิลด์อนุมัติโดย ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6473c-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="6473c-122">เลือกบุคคลที่จะรับผิดชอบในการอนุมัติรุ่นผลิตภัณฑ์สำหรับการใช้ในการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="6473c-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="6473c-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6473c-123">Click OK.</span></span>
12. <span data-ttu-id="6473c-124">ในฟิลด์วิธีการกำหนดราคา ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6473c-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="6473c-125">เรียกใช้รุ่นแบบจำลองผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="6473c-125">Activate the product model version.</span></span> <span data-ttu-id="6473c-126">เป็นไปได้ว่าอาจมีเพียงแค่หนึ่งผลิตภัณฑ์ที่ใช้ได้สำหรับแบบจำลองผลิตภัณฑ์หนึ่งแบบในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="6473c-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="6473c-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6473c-127">Close the page.</span></span>

