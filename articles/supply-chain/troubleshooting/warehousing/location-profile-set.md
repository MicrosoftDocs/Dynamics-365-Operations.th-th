---
title: โปรไฟล์สถานที่ตั้งไม่อนุญาตให้มีสินค้าคงคลังค่าลบ แต่อนุญาตให้ใช้ปริมาณคงคลังคงเหลือค่าลบได้
description: ตัวเลือกอนุญาตให้สินค้าคงคลังค่าลบได้ถูกตั้งค่าไว้เป็น ไม่ แต่ระบบยังคงอนุญาตปริมาณคงคลังคงเหลือที่เป็นค่าลบได้
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026947"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="629b8-103">โปรไฟล์สถานที่ตั้งไม่อนุญาตให้มีสินค้าคงคลังค่าลบ แต่อนุญาตให้ใช้ปริมาณคงคลังคงเหลือค่าลบได้</span><span class="sxs-lookup"><span data-stu-id="629b8-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="629b8-104">หมายเลข KB: 4613622</span><span class="sxs-lookup"><span data-stu-id="629b8-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="629b8-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="629b8-105">Symptoms</span></span>

<span data-ttu-id="629b8-106">ตัวเลือก **อนุญาตให้สินค้าคงคลังค่าลบ** ได้ถูกตั้งค่าไว้เป็น *ไม่* แต่ระบบยังคงอนุญาตปริมาณคงคลังคงเหลือที่เป็นค่าลบได้</span><span class="sxs-lookup"><span data-stu-id="629b8-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="629b8-107">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="629b8-107">Example scenario</span></span>

<span data-ttu-id="629b8-108">สำหรับธุรกรรมที่ควบคุมโดยรัฐบาล ระบบต้องสามารถบันทึกสินค้าคงคลังค่าลบเพื่อทำบัญชีรายการขาดทุน</span><span class="sxs-lookup"><span data-stu-id="629b8-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="629b8-109">คุณต้องการให้สินค้าสามารถแสดงสินค้าคงคลังค่าลบได้ แต่แสดงเฉพาะสถานที่ที่กำหนดไว้เท่านั้น เช่น แท้งค์</span><span class="sxs-lookup"><span data-stu-id="629b8-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="629b8-110">อย่างไรก็ตาม หากกลุ่มแบบจำลองสินค้าอนุญาตสินค้าคงคลังค่าลบ คุณพบว่าไม่สำคัญว่าจะตั้งค่าสถานที่เก็บเพื่ออนุญาตสินค้าคงคลังค่าลบหรือไม่</span><span class="sxs-lookup"><span data-stu-id="629b8-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="629b8-111">ถ้ามีการตั้งค่าสินค้าเพื่อให้ไม่อนุญาตให้มีสินค้าคงคลังค่าลบ ไม่สำคัญว่าโปรไฟล์สถานที่เก็บจะถูกตั้งค่าไว้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="629b8-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="629b8-112">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="629b8-112">Resolution</span></span>

<span data-ttu-id="629b8-113">การตั้งค่า **อนุญาตสินค้าคงคลังค่าลบ** จากโปรไฟล์สถานที่เก็บจะใช้กับกระบวนการคลังสินค้าเท่านั้น เช่น การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="629b8-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="629b8-114">อย่างไรก็ตาม กลุ่มแบบจำลองสินค้าที่ตั้งค่าไว้เพื่ออนุญาตสินค้าคงคลังค่าลบที่มีผลกระทบต่อกระบวนการทั้งหมดจากโมดูลการบริหารสินค้าคงคลังและโมดูลการจัดการคลังสินค้า และโปรไฟล์สถานที่เก็บจะไม่แทนที่การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="629b8-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="629b8-115">คุณสามารถควบคุมได้ว่าอนุญาตให้คลังสินค้ามีสินค้าคงคลังค่าลบหรือไม่</span><span class="sxs-lookup"><span data-stu-id="629b8-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="629b8-116">ตั้งค่ากลุ่มแบบจำลองสินค้าของคุณเป็นไม่อนุญาตให้มีสินค้าคงคลังที่มีอยู่จริงแบบติดลบ และตั้งค่าเฉพาะคลังสินค้าที่เกี่ยวข้องเพื่ออนุญาตสินค้าคงคลังค่าลบ</span><span class="sxs-lookup"><span data-stu-id="629b8-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
