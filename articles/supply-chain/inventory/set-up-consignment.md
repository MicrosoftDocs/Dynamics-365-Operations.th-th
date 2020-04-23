---
title: ตั้งค่าการส่งมอบ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกการดำเนินการสินค้าคงคลังที่มีการส่งมอบขาเข้า
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 51f7d6b0402ebbed417554978fc8d927f6b9c606
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207220"
---
# <a name="set-up-consignment"></a><span data-ttu-id="7056e-103">ตั้งค่าการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="7056e-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7056e-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกการดำเนินการสินค้าคงคลังที่มีการส่งมอบขาเข้า</span><span class="sxs-lookup"><span data-stu-id="7056e-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="7056e-105">สินค้าคงคลังที่มีการส่งมอบคือสินค้าคงคลังที่เป็นเจ้าของโดยผู้จัดจำหน่าย แต่เก็บอยู่ที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7056e-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="7056e-106">เมื่อคุณพร้อมที่จะใช้หรือใช้สินค้าคงคลัง คุณจะต้องเป็นเจ้าของสินค้าคงคลังดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="7056e-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="7056e-107">หัวข้อนี้อธิบายเกี่ยวกับการตั้งค่าที่จำเป็นเพื่อเปิดใช้งานกระบวนการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="7056e-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="7056e-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการส่งมอบ ดูที่ [ตั้งค่าการส่งมอบ](consignment.md)</span><span class="sxs-lookup"><span data-stu-id="7056e-108">For more information about consignment processes, see [Set up consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="7056e-109">เจ้าของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7056e-109">Inventory owners</span></span>
<span data-ttu-id="7056e-110">เพื่อบันทึกสินค้าคงคลังที่มีการส่งมอบขาเข้าที่มีอยู่จริง คุณจะต้องกำหนดเจ้าของซึ่งเป็นผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7056e-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="7056e-111">ซึ่งทำได้บนหน้า **เจ้าของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7056e-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="7056e-112">เมื่อคุณเลือก **บัญชีผู้จัดจำหน่าย** ระบบจะสร้างค่าเริ่มต้นสำหรับฟิลด์ **ชื่อ** และ **เจ้าของ**</span><span class="sxs-lookup"><span data-stu-id="7056e-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="7056e-113">ค่าในฟิลด์ **เจ้าของ** จะมองเห็นได้สำหรับผู้จัดจำหน่าย ดังนั้นคุณอาจต้องการเปลี่ยน ถ้าชื่อบัญชีของผู้จัดจำหน่ายจำได้ยากสำหรับบุคคลภายนอก</span><span class="sxs-lookup"><span data-stu-id="7056e-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="7056e-114">คุณสามารถแก้ไขฟิลด์ **เจ้าของ** ได้ แต่เฉพาะก่อนที่คุณจะบันทึกเรกคอร์ด **เจ้าของสินค้าคงคลัง** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7056e-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="7056e-115">ระบบจะเติมข้อมูลในฟิลด์ **ชื่อ** ด้วยชื่อของฝ่ายที่เชื่อมโยงกับบัญชีผู้จัดจำหน่าย และจะไม่สามารถเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="7056e-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="7056e-116">[![เจ้าของสินค้าคงคลัง](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="7056e-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="7056e-117">กลุ่มมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="7056e-117">Tracking dimension group</span></span>
<span data-ttu-id="7056e-118">ต้องเชื่อมโยงสินค้าที่จะใช้ในกระบวนการส่งมอบกับ **กลุ่มมิติการติดตาม** ที่มีการตั้งค่ามิติ **เจ้าของ** เป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="7056e-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="7056e-119">มิติเจ้าของจะมีการเลือกตัวเลือก **สินค้าคงคลังทางกายภาพ** และ **สินค้าคงคลังทางการเงิน** อยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="7056e-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="7056e-120">**วางแผนความครอบคลุมโดยเรียงตามมิติ** ไม่เคยถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="7056e-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="7056e-121">[![กลุ่มมิติการติดตาม](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="7056e-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="7056e-122">สมุดรายวันการเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7056e-122">Inventory ownership change journal</span></span>
<span data-ttu-id="7056e-123">สมุดรายวัน **การเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลัง**ถูกใช้เพื่อบันทึกการโอนย้ายความเป็นเจ้าของของสินค้าคงคลังที่มีการส่งมอบจากผู้จัดจำหน่ายไปยังนิติบุคคลที่จะใช้สมุดรายวันดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="7056e-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="7056e-124">เช่นเดียวกับสมุดรายวันสินค้าคงคลังใดๆ จะต้องมีการระบุชื่อสมุดรายวันสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7056e-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="7056e-125">ชื่อเหล่านี้จะถูกสร้างบนหน้า **ชื่อสมุดรายวันสินค้าคงคลัง** และ **ชนิดสมุดรายวัน** จะต้องถูกตั้งค่าเป็น **การเปลี่ยนแปลงความเป็นเจ้าของ**</span><span class="sxs-lookup"><span data-stu-id="7056e-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="7056e-126">[![สมุดรายวันการเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลัง](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="7056e-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="7056e-127">การทำงานร่วมกันกับผู้จัดจำหน่ายในกระบวนการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="7056e-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="7056e-128">ถ้าผู้จัดจำหน่ายของคุณใช้อินเทอร์เฟสของการทำงานร่วมกันกับผู้จัดจำหน่าย พวกเขาสามารถใช้ข้อมูลนี้เพื่อตรวจสอบปริมาณการใช้สินค้าคงคลังที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7056e-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="7056e-129">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าให้ผู้จัดจำหน่ายใช้การทำงานร่วมกันกับผู้จัดจำหน่าย ดูที่ [ความปลอดภัยผู้ใช้งานพอร์ทัลผู้จัดจำหน่าย](../procurement/configure-security-vendor-portal-users.md)</span><span class="sxs-lookup"><span data-stu-id="7056e-129">For more information about setting up vendors to use vendor collaboration, see [Vendor portal user security](../procurement/configure-security-vendor-portal-users.md).</span></span>
