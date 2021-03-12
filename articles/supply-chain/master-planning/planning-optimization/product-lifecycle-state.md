---
title: ไม่รวมผลิตภัณฑ์ที่มีสถานะของวงจรการใช้ผลิตภัณฑ์เฉพาะ
description: หัวข้อนี้อธิบายถึงวิธีการไม่รวมผลิตภัณฑ์ตามสถานะของวงจรการใช้เมื่อมีการใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 02c31aa3862df8dabc2b8c065dc3a94877d237f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992431"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="62847-103">ไม่รวมผลิตภัณฑ์ที่มีสถานะของวงจรการใช้ผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="62847-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62847-104">ผลิตภัณฑ์ที่นำออกใช้และรุ่นของผลิตภัณฑ์ที่นำออกใช้รวมฟิลด์ **สถานะของวงจรการใช้ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="62847-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="62847-105">ฟิลด์นี้จะช่วยให้คุณสามารถควบคุม ระหว่างสิ่งอื่น ๆ ซึ่งผลิตภัณฑ์รวมอยู่ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="62847-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="62847-106">คุณสามารถเพิ่มลบและแก้ไขสถานะของวงจรการใช้ได้ตามความจำเป็นโดยไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> สถานะของวงจรการใช้ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="62847-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="62847-107">สำหรับแต่ละสถานะของวงจรการใช้ผลิตภัณฑ์ ให้ตั้งค่าตัวเลือก **ใช้งานอยู่สำหรับการวางแผน** เป็น *ใช่* ถ้าผลิตภัณฑ์ที่สถานะนั้นควรรวมอยู่ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="62847-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="62847-108">เมื่อมีการตั้งค่าตัวเลือกเป็น *ไม่* ผลิตภัณฑ์ที่เกี่ยวข้องและผลิตภัณฑ์ย่อยจะถูกแยกออกจากการวางแผนหลักทั้งหมด และการคำนวณทั้งหมดที่ระดับสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="62847-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="62847-109">ผลิตภัณฑ์ที่นำออกใช้และผลิตภัณฑ์ย่อยที่ฟิลด์ **สถานะของวงจรการใช้ผลิตภัณฑ์** ถูกปล่อยว่างไว้จะถือว่ามีสถานะของวงจรการใช้ผลิตภัณฑ์ที่ตัวเลือก **ใช้งานอยู่สำหรับการวางแผน** ตั้งค่าเป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="62847-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="62847-110">กล่าวอีกอย่างหนึ่งคื อจะรวมอยู่ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="62847-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="62847-111">เพื่อหลีกเลี่ยงคำแนะนำไม่จำเป็น เราขอแนะนำให้คุณเชื่อมโยงผลิตภัณฑ์ที่นำออกใช้ที่ล้าสมัยและผลิตภัณฑ์ย่อยทั้งหมดที่มีสถานะของวงจรการใช้ผลิตภัณฑ์ที่ตัวเลือก **ใช้งานอยู่สำหรับการวางแผน** กำหนดเป็น *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="62847-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="62847-112">วิธีการนี้มีความสำคัญโดยเฉพาะอย่างยิ่งเมื่อคุณทำงานกับตัวแปรการจัดโครงแบบผลิตภัณฑ์ที่ไม่ได้ใช้งานใหม่ เนื่องจากจะช่วยป้องกันไม่ให้มีของเสีย</span><span class="sxs-lookup"><span data-stu-id="62847-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="62847-113">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="62847-113">Related resources</span></span>

<span data-ttu-id="62847-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสถานะของวงจรการใช้ผลิตภัณฑ์ ดู [ภาพรวมสถานะของวงจรการใช้ผลิตภัณฑ์](../../pim/product-lifecycle.md)</span><span class="sxs-lookup"><span data-stu-id="62847-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="62847-115">สำหรับข้อมูลโดยละเอียดที่รวมขั้นตอนการใช้สถานะของวงจรการใช้ผลิตภัณฑ์ เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลักและการคำนวณระดับ BOM ดูที่ [สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก](../../pim/tasks/exclude-products-master-planning.md)</span><span class="sxs-lookup"><span data-stu-id="62847-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>
