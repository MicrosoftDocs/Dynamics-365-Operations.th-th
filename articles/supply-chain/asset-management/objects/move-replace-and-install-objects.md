---
title: ย้าย แทนที่ และติดตั้งสินทรัพย์
description: หัวข้อนี้จะอธิบายวิธีการย้าย แทนที่ และติดตั้งสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f5eff3cc1bcf85e1541917edf525d83c124edb7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253241"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="536a9-103">ย้าย แทนที่ และติดตั้งสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="536a9-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="536a9-104">หัวข้อนี้จะอธิบายวิธีการย้าย แทนที่ และติดตั้งสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="536a9-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="536a9-105">คุณสามารถสร้างสินทรัพย์แต่ละรายการที่ไม่มีความสัมพันธ์กับสินทรัพย์อื่น หรือคุณสามารถสร้างโครงสร้างสินทรัพย์ที่มีสินทรัพย์หลัก (สินทรัพย์ระดับสูงสุด) และสินทรัพย์รองที่เกี่ยวข้อง (สินทรัพย์ย่อย)</span><span class="sxs-lookup"><span data-stu-id="536a9-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="536a9-106">ในการจัดการสินทรัพย์ มีวิธีการสามวิธีในการย้ายและการเปลี่ยนตำแหน่งของสินทรัพย์:</span><span class="sxs-lookup"><span data-stu-id="536a9-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="536a9-107">**ย้าย** – ย้ายสินทรัพย์ไปยังโครงสร้างสินทรัพย์อื่น หรือไปยังสถานที่อื่น ในโครงสร้างสินทรัพย์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="536a9-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="536a9-108">**แทนที่** – ลบสินทรัพย์ออกจากโครงสร้างสินทรัพย์อย่างชั่วคราว เพื่อให้สามารถซ่อมแซมหรือตกแต่งใหม่ และจากนั้น เพิ่มสินทรัพย์ที่ตกแต่งใหม่กลับไปยังโครงสร้างสินทรัพย์ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="536a9-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="536a9-109">อีกวิธีหนึ่งคือ แทนที่สินทรัพย์ที่ใช้ด้วยสินทรัพย์ใหม่อย่างถาวร</span><span class="sxs-lookup"><span data-stu-id="536a9-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="536a9-110">**ติดตั้ง** – ติดตั้งสินทรัพย์หลักและสินทรัพย์รองที่เกี่ยวข้องใดๆ ในตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="536a9-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="536a9-111">สินทรัพย์ที่คุณย้าย แทนที่ หรือติดตั้ง อาจเกี่ยวข้องกับตำแหน่งที่ทำงานอื่น</span><span class="sxs-lookup"><span data-stu-id="536a9-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="536a9-112">ในกรณีนั้น สินทรัพย์อาจใช้มิติทางการเงินของตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="536a9-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="536a9-113">บนหน้า **ชนิดตำแหน่งที่ทำงาน** คุณตั้งค่าการจัดการของมิติทางการเงินในตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="536a9-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="536a9-114">ย้ายสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="536a9-114">Move asset</span></span>

<span data-ttu-id="536a9-115">ใช้ฟังก์ชัน **ย้ายสินทรัพย์** เพื่อย้ายสินทรัพย์ไปยังโครงสร้างสินทรัพย์อื่น หรือไปยังสถานที่อื่น ในโครงสร้างสินทรัพย์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="536a9-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="536a9-116">นอกจากนี้ คุณยังสามารถย้ายสินทรัพย์ออกจากโครงสร้างสินทรัพย์ เพื่อให้กลายเป็นสินทรัพย์แบบสแตนด์อโลนที่ไม่มีความสัมพันธ์โครงสร้าง</span><span class="sxs-lookup"><span data-stu-id="536a9-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="536a9-117">อย่าใช้ฟังก์ชันนี้ ถ้ามีการซ่อมแซมหรือแทนที่สินทรัพย์โดยชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="536a9-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="536a9-118">แต่ให้ใช้ฟังก์ชัน **แทนที่สินทรัพย์** ที่อธิบายในหัวข้อนี้ในภายหลังแทน</span><span class="sxs-lookup"><span data-stu-id="536a9-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="536a9-119">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด** หรือ **สินทรัพย์ที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="536a9-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="536a9-120">ในรายการ ให้เลือกสินทรัพย์ที่จะย้าย</span><span class="sxs-lookup"><span data-stu-id="536a9-120">In the list, select the asset to move.</span></span> <span data-ttu-id="536a9-121">ถ้าสินทรัพย์มีสินทรัพย์รอง คุณยังสามารถย้ายสินทรัพย์เหล่านั้นได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="536a9-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="536a9-122">เลือก **ย้ายสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="536a9-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="536a9-123">ถ้าต้องการย้ายสินทรัพย์ เพื่อให้กลายเป็นส่วนหนึ่งของโครงสร้างสินทรัพย์ ให้เลือกสินทรัพย์หลักใหม่ในฟิลด์ **สินทรัพย์หลัก**</span><span class="sxs-lookup"><span data-stu-id="536a9-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="536a9-124">ถ้าคุณกำลังย้ายสินทรัพย์รอง และคุณต้องการทำให้เป็นสินทรัพย์แบบสแตนด์อโลนที่ไม่มีความสัมพันธ์ของโครงสร้าง ให้ปล่อยฟิลด์ **สินทรัพย์หลัก** ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="536a9-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="536a9-125">โดยค่าเริ่มต้น ฟิลด์ **มีผลบังคับใช้** ถูกกำหนดเป็นวันที่และเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="536a9-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="536a9-126">อย่างไรก็ตาม คุณสามารถเลือกวันที่และเวลาอื่นที่การติดตั้งในโครงสร้างการย้ายสินทรัพย์มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="536a9-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="536a9-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="536a9-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="536a9-128">แทนที่สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="536a9-128">Replace asset</span></span>

<span data-ttu-id="536a9-129">ใช้ฟังก์ชัน **แทนที่สินทรัพย์** ในการเชื่อมต่อกับการซ่อมแซม การปรับปรุงใหม่ หรือการแทนที่ถาวรของสินทรัพย์ที่มีการสึกหรอโดยสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="536a9-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="536a9-130">ฟังก์ชันนี้ถูกใช้ในการแทนที่สินทรัพย์รองในโครงสร้างสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="536a9-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="536a9-131">สำหรับสินทรัพย์หลัก (นั่นคือ สินทรัพย์ที่ไม่มีสินทรัพย์หลักในปัจจุบัน) จะมีการดำเนินการแทนที่นี้บนตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="536a9-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="536a9-132">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการแทนที่สินทรัพย์หลักในตำแหน่งที่ทำงาน ดู [ติดตั้งสินทรัพย์ในตำแหน่งที่ทำงาน](../functional-locations/install-objects-on-functional-locations.md)</span><span class="sxs-lookup"><span data-stu-id="536a9-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="536a9-133">ถ้าศูนย์บริการซ่อมเกี่ยวข้องกับแผนกการผลิตของคุณ คุณสามารถสร้างตำแหน่งที่ทำงาน เช่น **ซ่อมแซม** **เศษซาก** และ **ที่จัดเก็บ** เพื่อจัดการกับการซ่อมแซมและการแทนที่สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="536a9-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="536a9-134">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด** หรือ **สินทรัพย์ที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="536a9-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="536a9-135">ในรายการ ให้เลือกสินทรัพย์รองที่จะแทนที่</span><span class="sxs-lookup"><span data-stu-id="536a9-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="536a9-136">ถ้าสินทรัพย์มีสินทรัพย์รอง คุณยังสามารถแทนที่สินทรัพย์เหล่านั้นได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="536a9-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="536a9-137">เลือก **แทนที่สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="536a9-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="536a9-138">ฟิลด์ **การเปลี่ยนโครงสร้าง** แสดงวันที่และเวลาสุดท้ายที่สินทรัพย์ที่เลือกและสินทรัพย์รองที่เกี่ยวข้องถูกย้ายในโครงสร้างสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="536a9-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="536a9-139">ในส่วน **สินทรัพย์ที่เลือก** ในฟิลด์ **ตำแหน่งที่ทำงานเป้าหมาย** ให้เลือกตำแหน่งที่ทำงานที่จะย้ายสินทรัพย์ไป</span><span class="sxs-lookup"><span data-stu-id="536a9-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="536a9-140">ตัวอย่างเช่น เลือกสถานที่ **ซ่อมแซม** หรือ **เศษซาก**</span><span class="sxs-lookup"><span data-stu-id="536a9-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="536a9-141">ในส่วน **สินทรัพย์หลัก** ฟิลด์ **มีผลบังคับใช้** แสดงวันที่และเวลาล่าสุดที่มีการติดตั้งสินทรัพย์หลักและสินทรัพย์รองที่เกี่ยวข้อง หรือมีการย้ายในตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="536a9-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="536a9-142">ในส่วน **สินทรัพย์ใหม่** ในฟิลด์ **สินทรัพย์** ให้เลือกสินทรัพย์ที่จะแทรกเป็นการแทนที่แบบชั่วคราวหรือแบบถาวรสำหรับสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="536a9-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="536a9-143">ในปัจจุบัน สินทรัพย์นี้อาจอยู่ในตำแหน่งที่ทำงานอื่น เช่น **ที่เก็บข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="536a9-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="536a9-144">ในส่วน **มีผลบังคับใช้ตั้งแต่** ฟิลด์ **มีผลบังคับใช้** ถูกกำหนดเป็นวันที่และเวลาปัจจุบันตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="536a9-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="536a9-145">อย่างไรก็ตาม คุณสามารถเลือกวันที่และเวลาอื่นที่การแทนที่สินทรัพย์มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="536a9-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="536a9-146">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="536a9-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="536a9-147">ติดตั้งสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="536a9-147">Install asset</span></span>

<span data-ttu-id="536a9-148">ใช้ฟังก์ชัน **ติดตั้งสินทรัพย์** เพื่อติดตั้งโครงสร้างสินทรัพย์บนตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="536a9-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="536a9-149">เลือกสินทรัพย์หลักเสมอ</span><span class="sxs-lookup"><span data-stu-id="536a9-149">Always select a parent asset.</span></span> <span data-ttu-id="536a9-150">สินทรัพย์หลักและสินทรัพย์รองที่เกี่ยวข้องจะถูกย้ายไปยังตำแหน่งที่ทำงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="536a9-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="536a9-151">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด** หรือ **สินทรัพย์ที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="536a9-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="536a9-152">ในรายการ ให้เลือกสินทรัพย์หลักที่จะติดตั้งในตำแหน่งที่ทำงานอื่น</span><span class="sxs-lookup"><span data-stu-id="536a9-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="536a9-153">เลือก **ติดตั้งสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="536a9-153">Select **Install asset**.</span></span>

    <span data-ttu-id="536a9-154">ส่วน **แอททริบิวต์** จะแสดงแอททริบิวต์สินทรัพย์ที่ตั้งค่าไว้ในสินทรัพย์หลัก</span><span class="sxs-lookup"><span data-stu-id="536a9-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="536a9-155">ในฟิลด์ **ตำแหน่งที่ทำงาน** เลือกสถานที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="536a9-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="536a9-156">โดยค่าเริ่มต้น ฟิลด์ **มีผลบังคับใช้** ถูกกำหนดเป็นวันที่และเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="536a9-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="536a9-157">อย่างไรก็ตาม คุณสามารถเลือกวันที่และเวลาอื่นที่การติดตั้งในโครงสร้างสินทรัพย์มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="536a9-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="536a9-158">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="536a9-158">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]