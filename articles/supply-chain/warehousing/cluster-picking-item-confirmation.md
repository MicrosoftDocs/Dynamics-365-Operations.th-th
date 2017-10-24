---
title: "การยืนยันผลิตภัณฑ์สำหรับการเลือกคลัสเตอร์"
description: "หัวข้อนี้อธิบายวิธีตั้งค่าการตรวจสอบสินค้าพร้อมทั้งการเบิกสินค้าคลัสเตอร์"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17f5761df4294abfea28e7cb8d50c86f1e3e136f
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

[!include[banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="e4fda-103">การยืนยันผลิตภัณฑ์สำหรับการเลือกคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="e4fda-103">Product confirmation for cluster picking</span></span>
<span data-ttu-id="e4fda-104">การเบิกสินค้าคลัสเตอร์ช่วยให้คุณสามารถเบิกสินค้าสำหรับใบสั่งหลายใบพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="e4fda-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="e4fda-105">เมื่อมีการนำการเบิกสินค้าคลัสเตอร์มาใช้ การยืนยันสินค้าเป็นสิ่งสำคัญยิ่งในการตรวจสอบสินค้าที่ถูกเพิ่มลงในคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="e4fda-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="e4fda-106">คุณสามารถตรวจสอบสินค้าในการเบิกสินค้าคลัสเตอร์ในระหว่างกระบวนการเบิกสินค้าคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="e4fda-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="e4fda-107">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="e4fda-107">Where it applies</span></span>
<span data-ttu-id="e4fda-108">การตรวจสอบสินค้าสำหรับการเบิกสินค้าคลัสเตอร์มีลักษณะเดียวกับเมื่อคุณตรวจสอบสินค้าในกระบวนการเบิกสินค้าที่ไม่ใช่คลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="e4fda-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="e4fda-109">การตั้งค่าขึ้นอยู่กับการตั้งค่าบาร์โค้ดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e4fda-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="e4fda-110">ตั้งค่าการตรวจสอบสินค้าที่มีการเบิกสินค้าคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="e4fda-110">Set up item verification with cluster picking</span></span>
1.  <span data-ttu-id="e4fda-111">บนรายการเมนูอุปกรณ์เคลื่อนที่ เปิดแบบฟอร์มการตั้งค่าสำหรับการยืนยันงาน: **การบริหารคลังสินค้า** > **การบริหารคลังสินค้า** > **การตั้งค่า** > **อุปกรณ์เคลื่อนที่** > **รายการเมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="e4fda-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
2.  <span data-ttu-id="e4fda-112">จากรายการเมนูบนอุปกรณ์เคลื่อนที่ เปิด **การตั้งค่าการยืนยันงาน**</span><span class="sxs-lookup"><span data-stu-id="e4fda-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

| <span data-ttu-id="e4fda-113">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e4fda-113">Option</span></span>        | <span data-ttu-id="e4fda-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e4fda-114">Description</span></span>   | 
| ------------- | ------------- |
|<span data-ttu-id="e4fda-115">การยืนยันผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e4fda-115">Product confirmation</span></span> | <span data-ttu-id="e4fda-116">ช่วยให้คุณสามารถตรวจสอบสินค้าคงคลังแต่ละรายการได้จากอุปกรณ์เคลื่อนที่เมื่อมีการสแกน</span><span class="sxs-lookup"><span data-stu-id="e4fda-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span>|

