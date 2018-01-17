---
title: "กฎโครงแบบ"
description: "บทความนี้ให้ข้อมูลทั่วไปเกี่ยวกับกฎโครงแบบ กฎโครงแบบกำหนดความสัมพันธ์ระหว่างสินค้าในรายการวัสดุและส่วนประกอบ (BOM) สำหรับผลิตภัณฑ์ที่ใช้เทคโนโลยีการจัดโครงแบบตามมิติ"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 6dff0abbcc9cf4138dec58c11b59cb9b19d81ce3
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="configuration-rules"></a><span data-ttu-id="d47df-104">กฎโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="d47df-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d47df-105">บทความนี้ให้ข้อมูลทั่วไปเกี่ยวกับกฎโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="d47df-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="d47df-106">กฎโครงแบบกำหนดความสัมพันธ์ระหว่างสินค้าในรายการวัสดุและส่วนประกอบ (BOM) สำหรับผลิตภัณฑ์ที่ใช้เทคโนโลยีการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="d47df-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="d47df-107">กฎโครงแบบพร้อมใช้งานเมื่อคุณกำหนดแบบจำลองการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="d47df-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="d47df-108">กฎโครงแบบถูกใช้เพื่อบังคับใช้ หรือไม่อนุญาตในการรวมสินค้าเฉพาะในสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="d47df-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="d47df-109">หลัง BOM ได้ถูกสร้างแล้วและสินค้าเกี่ยวข้องได้ถูกกำหนดให้กับกลุ่มการกำหนดค่าที่สอดคล้องกันของพวกเขา มากกว่าหนึ่งกฎโครงแบบสามารถถูกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="d47df-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="d47df-110">ถ้าสินค้าสองรายการอยู่ร่วมกัน ตัวดำเนินการ **ที่เลือก** ถูกใช้เพื่อให้แน่ใจว่าเป็นการรวม</span><span class="sxs-lookup"><span data-stu-id="d47df-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="d47df-111">ถ้าสินค้าสองรายการเป็นแบบเฉพาะร่วมกัน ตัวดำเนินการ **ที่ยกเลิกการเลือก** ถูกใช้เพื่อให้แน่ใจว่าเป็นข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="d47df-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="d47df-112">**หมายเหตุ:** ข้อมูลนี้ใช้กับผลิตภัณฑ์หลักเท่านั้นที่ใช้เทคโนโลยีการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="d47df-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="d47df-113">โครงแบบที่มีอยู่ไม่ได้รับผลกระทบจากการเปลี่ยนแปลงในเวลาต่อมากับกฎโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="d47df-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="d47df-114">อย่างไรก็ตาม เป็นสิ่งสำคัญที่คุณได้ตั้งค่ากฎก่อนที่คุณกำหนดโครงแบบใหม่ และให้คุณตรวจสอบกฎถ้าคุณคิดว่ากฏได้ถูกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="d47df-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="d47df-115">**หมายเหตุ:** สำหรับวิธี **ที่เลือก** กลุ่มการปรับเปลี่ยนที่ได้รับ หมายเลขสินค้า และโครงแบบที่ถูกเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d47df-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="d47df-116">สำหรับวิธี **ที่ยกเลิกการเลือก** กลุ่มการปรับเปลี่ยนที่ได้รับ หมายเลขสินค้า และโครงแบบไม่สามารถเลือกได้</span><span class="sxs-lookup"><span data-stu-id="d47df-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="d47df-117">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d47df-117">See also</span></span>
--------

[<span data-ttu-id="d47df-118">การจัดโครงแบบของผลิตภัณฑ์ตามมิติ</span><span class="sxs-lookup"><span data-stu-id="d47df-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




