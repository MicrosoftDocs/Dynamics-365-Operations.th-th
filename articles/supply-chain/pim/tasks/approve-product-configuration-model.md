---
title: อนุมัติแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'การดำเนินกระบวนงานนี้ต้องใช้อย่างน้อยหนึ่งแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ที่จะพร้อมใช้งาน '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920518"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="bec6e-103">อนุมัติแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bec6e-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bec6e-104">การดำเนินกระบวนงานนี้ต้องใช้อย่างน้อยหนึ่งแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ที่จะพร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="bec6e-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="bec6e-105">กระบวนงานนี้ใช้แบบจำลองลำโพงขั้นสูงในข้อมูลบริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="bec6e-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="bec6e-106">โปรดสังเกตว่า แบบจำลองนี้ได้รับการอนุมัติแล้ว แต่กระบวนงานจะนำคุณผ่านกระบวนการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bec6e-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="bec6e-107">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="bec6e-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="bec6e-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bec6e-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bec6e-109">เลือกแบบจำลองลำโพงขั้นสูงสำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="bec6e-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="bec6e-110">เลือก **เวอร์ชัน**</span><span class="sxs-lookup"><span data-stu-id="bec6e-110">Select **Versions**.</span></span>
1. <span data-ttu-id="bec6e-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bec6e-111">Select **New**.</span></span>
1. <span data-ttu-id="bec6e-112">ในฟิลด์ **หมายเลขผลิตภัณฑ์** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bec6e-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="bec6e-113">การอ้างอิงกับผลิตภัณฑ์แสดงถึงรุ่นของแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="bec6e-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="bec6e-114">เฉพาะผลิตภัณฑ์หลักที่มีเทคโนโลยีการจัดโครงแบบตามข้อจำกัดเท่านั้นที่จะปรากฏในรายการนี้</span><span class="sxs-lookup"><span data-stu-id="bec6e-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="bec6e-115">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="bec6e-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="bec6e-116">เลือกเมื่อรุ่นแบบจำลองผลิตภัณฑ์พร้อมจะใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bec6e-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="bec6e-117">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="bec6e-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="bec6e-118">เลือกวันสิ้นสุดเมื่อรุ่นแบบจำลองผลิตภัณฑ์นี้จะหมดอายุ หรือเลือก ไม่มีการหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="bec6e-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="bec6e-119">เลือก **อนุมัติ** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bec6e-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="bec6e-120">ในฟิลด์ **อนุมัติโดย** ให้ป้อน หรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bec6e-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="bec6e-121">เลือกบุคคลที่จะรับผิดชอบในการอนุมัติรุ่นผลิตภัณฑ์สำหรับการใช้ในการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="bec6e-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="bec6e-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bec6e-122">Select **OK**.</span></span>
1. <span data-ttu-id="bec6e-123">ในฟิลด์ **วิธีการกำหนดราคา** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bec6e-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="bec6e-124">เรียกใช้รุ่นแบบจำลองผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="bec6e-124">Activate the product model version.</span></span> <span data-ttu-id="bec6e-125">เป็นไปได้ว่าอาจมีเพียงแค่หนึ่งผลิตภัณฑ์ที่ใช้ได้สำหรับแบบจำลองผลิตภัณฑ์หนึ่งแบบในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="bec6e-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="bec6e-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bec6e-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]