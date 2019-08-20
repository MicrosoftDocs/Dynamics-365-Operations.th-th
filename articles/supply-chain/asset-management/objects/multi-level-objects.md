---
title: สินทรัพย์หลายระดับ
description: หัวข้อนี้อธิบายวิธีการสร้างและลบสินทรัพย์หลายระดับ
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
ms.openlocfilehash: 0f38253317ed8f06318fc501511ca5263a614e20
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783625"
---
# <a name="multi-level-assets"></a><span data-ttu-id="22205-103">สินทรัพย์หลายระดับ</span><span class="sxs-lookup"><span data-stu-id="22205-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="22205-104">หัวข้อนี้อธิบายวิธีการสร้างและลบสินทรัพย์หลายระดับ</span><span class="sxs-lookup"><span data-stu-id="22205-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="22205-105">คุณสามารถสร้างสินทรัพย์และสินทรัพย์ย่อยที่เกี่ยวข้องในโครงสร้างแผนภูมิตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="22205-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="22205-106">ด้วยวิธีนี้ คุณสามารถแสดงความสัมพันธ์และการอ้างอิงระหว่างสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="22205-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="22205-107">สามารถเชื่อมโยงงานบำรุงรักษากับทุกระดับของโครงสร้างแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="22205-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="22205-108">นอกจากนี้ ยังสามารถสร้างสถิติสำหรับแต่ละระดับ หรือเป็นผลรวมของระดับสินทรัพย์ย่อยทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="22205-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="22205-109">ในหน้ารายการ **สินทรัพย์ทั้งหมด** (**การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด**) คอลัมน์ **สินทรัพย์** แสดงรายการสินทรัพย์ตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="22205-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="22205-110">คอลัมน์ **รายการหลัก** แสดงรายการหลักที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="22205-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="22205-111">นอกจากนี้ ถ้ามีการสร้างสินทรัพย์และสินทรัพย์ย่อยแล้ว ส่วน **แผนภูมิสินทรัพย์** ในบานหน้าต่าง **ข้อมูลที่เกี่ยวข้อง** จะแสดงสินทรัพย์ในโครงสร้างแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="22205-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="22205-112">สำหรับข้อมูลเกี่ยวกับวิธีการสร้างสินทรัพย์ ให้ดูที่ [สร้างสินทรัพย์](../objects/create-an-object.md)</span><span class="sxs-lookup"><span data-stu-id="22205-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="22205-113">เมื่อต้องการสร้างสินทรัพย์ย่อย ให้เลือกสินทรัพย์หลักในฟิลด์ **หลัก** บน FastTab **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="22205-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="22205-114">คัดลอกโครงสร้างสินทรัพย์หรือสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="22205-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="22205-115">ถ้าบริษัทของคุณมีโครงสร้างสินทรัพย์ที่คล้ายกันหลายรายการ คุณสามารถใช้ฟังก์ชันคัดลอกในการจัดการสินทรัพย์เพื่อสร้างอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="22205-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="22205-116">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="22205-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="22205-117">บนหน้ารายการ **สินทรัพย์ทั้งหมด** ให้เลือกสินทรัพย์ที่จะคัดลอก</span><span class="sxs-lookup"><span data-stu-id="22205-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="22205-118">ตัวอย่างเช่น ถ้าคุณต้องการคัดลอกโครงสร้างสินทรัพย์ทั้งหมด ซึ่งรวมถึงสินทรัพย์ย่อย ให้เลือกสินทรัพย์หลัก</span><span class="sxs-lookup"><span data-stu-id="22205-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="22205-119">เลือก **คัดลอกสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="22205-119">Select **Copy asset**.</span></span> <span data-ttu-id="22205-120">ในส่วน **คัดลอกจาก** ฟิลด์ **สินทรัพย์** จะถูกตั้งค่าเป็นสินทรัพย์ที่คุณเลือกบนหน้ารายการ</span><span class="sxs-lookup"><span data-stu-id="22205-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="22205-121">ในส่วน **คัดลอกไปยัง** ในฟิลด์ **สินทรัพย์** ให้ป้อนชื่อของสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="22205-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="22205-122">ถ้าสินทรัพย์ที่คุณกำลังสร้างควรเป็นส่วนหนึ่งของโครงสร้างสินทรัพย์ที่มีอยู่ ในส่วน **สินทรัพย์หลัก** ในฟิลด์ **สินทรัพย์** ให้เลือกรหัสหลัก</span><span class="sxs-lookup"><span data-stu-id="22205-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="22205-123">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="22205-123">Select **OK**.</span></span> <span data-ttu-id="22205-124">โครงสร้างสินทรัพย์ใหม่จะแสดงอยู่ในหน้ารายการ **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="22205-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="22205-125">แอททริบิวต์สินทรัพย์ แผนการบำรุงรักษา และรอบการบำรุงรักษาทั้งหมดที่เกี่ยวข้องกับสินทรัพย์ที่คุณคัดลอก จะถูกโอนย้ายไปยังสินทรัพย์หรือโครงสร้างสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="22205-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="22205-126">เมื่อคุณคัดลอกโครงสร้างสินทรัพย์ สินทรัพย์ย่อยในโครงสร้างใหม่จะมีชื่อเดียวกับสินทรัพย์ย่อยที่คุณคัดลอก</span><span class="sxs-lookup"><span data-stu-id="22205-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="22205-127">หลังจากกระบวนงานคัดลอกเสร็จสมบูรณ์แล้ว คุณสามารถเปลี่ยนชื่อและการตั้งค่าอื่นๆ สำหรับสินทรัพย์ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="22205-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="22205-128">เลือกสินทรัพย์ในหน้ารายการ **สินทรัพย์ทั้งหมด** แล้วจากนั้น เลือกปุ่ม **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="22205-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="22205-129">เมื่อคุณคัดลอกสินทรัพย์หรือโครงสร้างสินทรัพย์ สถานะของวงจรการใช้ของสินทรัพย์ใหม่จะถูกรีเซ็ตเป็นสถานะใดก็ตามที่คุณได้กำหนดเป็นสถานะของวงจรการใช้เริ่มต้นสำหรับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="22205-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="22205-130">ตำแหน่งที่ทำงานถูกรีเซ็ตเป็นตำแหน่งที่ทำงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="22205-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="22205-131">ลบโครงสร้างสินทรัพย์หรือสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="22205-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="22205-132">ถ้าสินทรัพย์มีสินทรัพย์ย่อยที่เกี่ยวข้อง คุณสามารถลบได้เฉพาะเมื่อไม่มีคำขอการบำรุงรักษา งานในใบสั่งงาน การลงทะเบียนข้อบกพร่อง หรือการประเมินเงื่อนไข จะถูกลงทะเบียนไว้ในสินทรัพย์ใดๆ</span><span class="sxs-lookup"><span data-stu-id="22205-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="22205-133">บนหน้ารายการ **สินทรัพย์ทั้งหมด** ให้เลือกสินทรัพย์ที่จะลบ</span><span class="sxs-lookup"><span data-stu-id="22205-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="22205-134">เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="22205-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="22205-135">ถ้าคุณไม่สามารถลบสินทรัพย์โดยใช้กระบวนงานนี้ อีกวิธีหนึ่งในการจัดการการลบคือ การตั้งค่าสถานะของวงจรการใช้ของสินทรัพย์สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="22205-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="22205-136">ตัวอย่างเช่น คุณสามารถตั้งค่าสถานะของวงจรการใช้ **ตัดจำหน่ายเป็นเศษซาก** หรือ **ลบ** ในหน้า **สถานะของวงจรการใช้ของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="22205-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
