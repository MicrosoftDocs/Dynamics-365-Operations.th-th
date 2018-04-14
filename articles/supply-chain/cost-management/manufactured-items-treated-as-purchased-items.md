---
title: "ตั้งค่าผลิตภัณฑ์ที่สามารถถูกผลิตหรือจัดซื้อ"
description: "ผลิตภัณฑ์สามารถเป็นต้นทางในหลายๆ วิธี - สามารถผลิต (ที่ผลิต) หรือการจัดซื้อ (ซื้อ) บทความนี้อธิบายคะแนนทั่วไปที่ควรพิจารณาเมื่อคุณตั้งค่าคอนฟิกผลิตภัณฑ์เพื่อสนับสนุนการจัดหาหลายรายการ"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 81f556dca0bfa17623bb1a0f1c712bfa5a4a2a9b
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="fc773-104">ตั้งค่าผลิตภัณฑ์ที่สามารถถูกผลิตหรือจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="fc773-104">Set up products that can be produced or procured</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="fc773-105">ผลิตภัณฑ์สามารถเป็นต้นทางในหลายๆ วิธี - สามารถผลิต (ที่ผลิต) หรือการจัดซื้อ (ซื้อ)</span><span class="sxs-lookup"><span data-stu-id="fc773-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="fc773-106">บทความนี้อธิบายคะแนนทั่วไปที่ควรพิจารณาเมื่อคุณตั้งค่าคอนฟิกผลิตภัณฑ์เพื่อสนับสนุนการจัดหาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="fc773-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="fc773-107">โดยทั่วไปจะใช้จัดหาจากหลายแหล่งสำหรับสินค้าที่ซื้อที่จะผลิตบางครั้ง หรือเมื่อมีการเปลี่ยนแปลงสินค้าที่เริ่มแรกมาการผลิตเพื่อให้เริ่มแรกเป็นสินค้าที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="fc773-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="fc773-108">เริ่มแรกสินค้าจะถูกกำหนดเป็นสินค้าที่ผลิต เพื่อให้คุณสามารถกำหนดรายการวัสดุและส่วนประกอบ (BOM) และข้อมูลกระบวนการผลิต และเพื่อสนับสนุนการผลิตของใบสั่งสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc773-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="fc773-109">ชนิดการผลิตควรถูกกำหนดเป็น **BOM** (หรือ สำหรับกระบวนการผลิต **สูตร** หรือ **สินค้าร่วม**)</span><span class="sxs-lookup"><span data-stu-id="fc773-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="fc773-110">เมื่อคุณใช้ต้นทุนมาตรฐาน เรกคอร์ดต้นทุนสินค้าสามารถคำนวณได้สำหรับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="fc773-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="fc773-111">อย่างไรก็ตาม เรกคอร์ดต้นทุนสินค้าอาจไม่ตรงกับต้นทุนมาตรฐานที่คุณต้องการสำหรับวัตถุประสงค์ในการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="fc773-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="fc773-112">ในกรณีนี้ ต้นทุนมาตรฐานต้องถูกป้อนด้วยตนเอง และเรียกใช้สำหรับเรกคอร์ดต้นทุนสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc773-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="fc773-113">การคำนวณต้นทุน ให้พิจารณาการใช้ BOM และกระบวนการผลิตที่แสดงถึงการซื้อคละกันของการจัดหาวัสดุของผลิตภัณฑ์พิเศษ ขณะดำเนินการรอบระยะเวลาบัญชี เพื่อลดผลต่างตามช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fc773-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="fc773-114">นอกจากนี้ สินค้าที่ผลิตที่ไซต์เดียวสามารถโอนย้ายไปที่ไซต์อื่น</span><span class="sxs-lookup"><span data-stu-id="fc773-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="fc773-115">ดังนั้น ต้นทุนของสินค้าต้องถูกป้อนด้วยตนเอง และเรียกใช้สำหรับไซต์ที่จะใช้ในการโอนย้ายสินค้าไป</span><span class="sxs-lookup"><span data-stu-id="fc773-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="fc773-116">เมื่อคุณใช้สินค้าที่ผลิตเป็นส่วนประกอบในผลิตภัณฑ์ระดับที่สูงกว่า ส่วนประกอบของต้นทุนควรถือเป็นสินค้าที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="fc773-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="fc773-117">คำแนะนำนี้ใช้ โดยไม่คำนึงถึงว่าส่วนประกอบของต้นทุนได้ถูกคำนวณหรือป้อนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="fc773-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="fc773-118">กล่าวอีกอย่างหนึ่งคือ การคำนวณ BOM ควรถือต้นทุนของสินค้าเป็นส่วนประกอบการซื้อแทนการใช้ของ BOM ของสินค้า และข้อมูลกระบวนการผลิตเพื่อคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="fc773-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="fc773-119">การป้องกันไม่ให้มีการคำนวณเกิดขึ้น เลือกแฟล็ก **หยุดกระจาย** ที่ฝังอยู่ในกลุ่มการคำนวณ BOM ที่กำหนดให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc773-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="fc773-120">เพื่อป้องกันไม่ให้มีการคำนวณการจัดกำหนดการหลักจากการกระจายความต้องการสินค้า ตั้งค่ากรอบการกระจายเป็น 0 (ศูนย์) วัน ในความครอบคลุมสินค้า หรือ ในกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="fc773-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="fc773-121">การคำนวณการจัดกำหนดการหลักจะถูกถือว่าสินค้านั้นเป็นสินค้าที่ซื้อ และจะไม่ทำการคำนวณเพิ่มเติมสำหรับ BOM ของสินค้าและข้อมูลกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="fc773-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






