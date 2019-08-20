---
title: เอกสารสินทรัพย์
description: หัวข้อนี้จะอธิบายถึงเอกสารสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1c90788da7ad536fb9978db18160ccf6c158033
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783617"
---
# <a name="asset-documents"></a><span data-ttu-id="ff2de-103">เอกสารสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ff2de-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ff2de-104">หัวข้อนี้จะอธิบายถึงเอกสารสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ff2de-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="ff2de-105">ในการจัดการสินทรัพย์ คุณสามารถตั้งค่าเอกสารเพื่อให้มีความเกี่ยวข้องโดยอัตโนมัติกับ ตัวอย่างเช่น ชนิดงาน ผู้ผลิตสินทรัพย์ ชนิดสินทรัพย์ หรือสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ff2de-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="ff2de-106">ฟังก์ชันนี้มีประโยชน์เมื่อมีการนำออกใช้รุ่นเอกสารที่ปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="ff2de-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="ff2de-107">ในกรณีนั้น คุณเพียงแค่ต้องใส่เอกสารที่ปรับปรุงแล้วในสถานที่มาตรฐานที่คุณใช้สำหรับเอกสาร Microsoft Dynamics 365 for Finance and Operations ของคุณ และแนบเอกสารกับเรกคอร์ดเอกสารสินทรัพย์ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ff2de-107">In that case, you just have to put the updated document in the standard location that you use for your Microsoft Dynamics 365 for Finance and Operations documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="ff2de-108">จากนั้น คุณสามารถเข้าถึงเอกสารที่ปรับปรุงแล้วได้จากรายการเมนู **สินทรัพย์ทั้งหมด** **สินทรัพย์ที่ใช้งานอยู่** **สินทรัพย์ที่ใช้งานอยู่ของฉัน** **ใบสั่งงานทั้งหมด** และ **งานในใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="ff2de-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="ff2de-109">กระบวนการสำหรับการแนบเอกสารกับเรกคอร์ดเอกสารสินทรัพย์ จะใช้ระบบการจัดการเอกสารมาตรฐานใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff2de-109">The process for attaching documents to an asset document record uses the standard document handling system in Finance and Operations.</span></span>

<span data-ttu-id="ff2de-110">**ตัวอย่างที่ 1:** เอกสารที่เกี่ยวข้องกับชนิดงานอาจอธิบายกระบวนงานสำหรับชนิดงานนั้น</span><span class="sxs-lookup"><span data-stu-id="ff2de-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="ff2de-111">**ตัวอย่างที่ 2:** เอกสารที่เกี่ยวข้องกับชุดของชนิดสินทรัพย์ ผู้ผลิต และแบบจำลอง อาจเป็นคู่มือมาตรฐานสำหรับแบบจำลองผู้ผลิตสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff2de-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="ff2de-112">สร้างความสัมพันธ์เอกสารสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ff2de-112">Create asset document relation</span></span>

1. <span data-ttu-id="ff2de-113">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **เอกสารสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="ff2de-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="ff2de-114">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดเอกสารสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ff2de-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="ff2de-115">โดยขึ้นอยู่กับความเฉพาะเจาะจงที่คุณต้องการให้ความสัมพันธ์เอกสารเป็น ทำให้การเลือกที่เกี่ยวข้องในฟิลด์ต่อไปนี้อย่างน้อยหนึ่งฟิลด์: **ชนิดสินทรัพย์** **ผู้ผลิตr** **แบบจำลอง** **สินทรัพย์** **ประเภทชนิดงาน** **ชนิดงาน** **ตัวแปรชนิดงาน** และ **ข้อกำหนดเกี่ยวกับงาน**</span><span class="sxs-lookup"><span data-stu-id="ff2de-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="ff2de-116">ตัวเลือกที่พร้อมใช้งานในฟิลด์ **ตัวแปรชนิดงาน** และฟิลด์ **ข้อกำหนดเกี่ยวกับงาน** ขึ้นอยู่กับการเลือกของคุณในฟิลด์ **ชนิดงาน**</span><span class="sxs-lookup"><span data-stu-id="ff2de-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff2de-117">เมื่อระบบค้นหาเอกสารที่ควรเกี่ยวข้องกับสินทรัพย์หรือใบสั่งงาน การจัดการสินทรัพย์จะผ่านเรกคอร์ดของเอกสารสินทรัพย์ทั้งหมดเพื่อตรวจสอบการจับคู่ที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="ff2de-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="ff2de-118">ซึ่งจะตรวจสอบชุดที่เฉพาะเจาะจงมากที่สุดก่อน</span><span class="sxs-lookup"><span data-stu-id="ff2de-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="ff2de-119">กล่าวคือ อันดับแรกการจัดการสินทรัพย์ตรวจสอบการจับคู่สำหรับฟิลด์ **ข้อกำหนดเกี่ยวกับงาน**</span><span class="sxs-lookup"><span data-stu-id="ff2de-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="ff2de-120">ถ้าไม่พบการจับคู่ จะตรวจสอบการจับคู่สำหรับฟิลด์ **ตัวแปรชนิดงาน**</span><span class="sxs-lookup"><span data-stu-id="ff2de-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="ff2de-121">ถ้าไม่พบการจับคู่ จะตรวจสอบการจับคู่สำหรับฟิลด์ **ชนิดงาน** เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="ff2de-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="ff2de-122">ดังที่คุณสามารถดูได้ในโครงร่างของหน้า **เอกสารสินทรัพย์** ลักษณะการทำงานนี้หมายความว่า การค้นหาชุดที่เฉพาะเจาะจงมากที่สุด การจัดการสินทรัพย์จะตรวจสอบเรกคอร์ดแต่ละรายการจากขวาไปซ้ายสำหรับการจับคู่</span><span class="sxs-lookup"><span data-stu-id="ff2de-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="ff2de-123">เอกสารหลายฉบับอาจเกี่ยวข้องกับสินทรัพย์หรือใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="ff2de-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="ff2de-124">คุณสามารถแก้ไขระดับการบริการในคำขอการบำรุงรักษาหรือใบสั่งงานตามที่คุณต้องการได้</span><span class="sxs-lookup"><span data-stu-id="ff2de-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="ff2de-125">เลือก **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="ff2de-125">Select **Attachments**.</span></span> <span data-ttu-id="ff2de-126">หน้า **การจัดการเอกสาร** มาตรฐานใน Finance and Operations ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="ff2de-126">The standard **Document handling** page in Finance and Operations appears.</span></span>
5. <span data-ttu-id="ff2de-127">ตั้งค่าเอกสารหรือบันทึกย่อที่ควรแนบกับเรกคอร์ดเอกสารสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ff2de-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="ff2de-128">หลังจากที่คุณแนบเอกสาร ฟิลด์ **สิ่งที่แนบมา** จะแสดงจำนวนของเอกสารที่เกี่ยวข้องกับเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="ff2de-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
