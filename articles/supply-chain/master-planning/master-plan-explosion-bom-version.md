---
title: การกระจายเวอร์ชัน BOM
description: บทความนี้อธิบายถึงสถานการณ์จำลองการวางแผนหลักที่เกี่ยวข้องกับการกระจายเวอร์ชันของสูตรการผลิต (BOM)
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220859"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="b079f-103">การกระจายเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="b079f-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b079f-104">บทความนี้อธิบายถึงสถานการณ์จำลองการวางแผนหลักที่เกี่ยวข้องกับการกระจายเวอร์ชันของสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="b079f-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="b079f-105">การขยายความต้องการของเวอร์ชันสูตรการผลิต (BOM) สร้างความต้องการสำหรับสินค้าในบรรทัด BOM แต่ละรายการที่ไซต์เฉพาะ และอาจจะเกิดความต้องการที่คลังสินค้าเฉพาะด้วย</span><span class="sxs-lookup"><span data-stu-id="b079f-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="b079f-106">ใน BOM ไซต์เฉพาะ คลังสินค้าเฉพาะสามารถถูกกำหนดสำหรับบรรทัด BOM แต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="b079f-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="b079f-107">นอกจากนี้ สำหรับบรรทัด BOM แต่ละบรรทัด การตั้งค่ามิติของสินค้าเป็นตัวกำหนดว่าคลังสินค้าเป็นสิ่งจำเป็นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b079f-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="b079f-108">ความต้องการสำหรับสินค้าในบรรทัด BOM แต่ละรายการกลายเป็นจุดเริ่มต้นสำหรับการขยายความต้องการเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b079f-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="b079f-109">สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b079f-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b079f-110">มิติไซต์เป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="b079f-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b079f-111">มิติไซต์ไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="b079f-111">The site dimension is consistent.</span></span> <span data-ttu-id="b079f-112">ดังนั้น ไซต์สำหรับความต้องการระดับล่างจึงเหมือนกับไซต์บนธุรกรรมความต้องการแรกเริ่ม</span><span class="sxs-lookup"><span data-stu-id="b079f-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="b079f-113">ภาพประกอบต่อไปนี้แสดงกระบวนการสำหรับการขยายความต้องการของการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="b079f-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![ความต้องการกระจายโดยใช้ BOM เวอร์ชัน](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="b079f-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b079f-115">Additional resources</span></span>
--------

[<span data-ttu-id="b079f-116">กำหนดเวอร์ชันสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="b079f-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="b079f-117">ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="b079f-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]