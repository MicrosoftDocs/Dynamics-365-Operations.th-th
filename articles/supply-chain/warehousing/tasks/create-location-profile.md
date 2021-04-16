---
title: สร้างโพรไฟล์สถานที่
description: หัวข้อนี้อธิบายวิธีการสร้างโพรไฟล์สถานที่ใน Dynamics 365 Supply Chain Management
author: ShylaThompson
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 101d80216f786eb8edb687031e4deac8cc3033ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831037"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="19af4-103">สร้างโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="19af4-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19af4-104">หัวข้อนี้อธิบายวิธีการสร้างโพรไฟล์สถานที่ใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="19af4-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="19af4-105">สถานที่ทุกแห่งในคลังสินค้าจะต้องมีโพรไฟล์สถานที่เกี่ยวข้องกันซึ่งอธิบายคุณสมบัติของสถานที่ดังกล่าว ตัวอย่างเช่น สถานที่แห่งนั้นอนุญาตสำหรับสินค้าผสมหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="19af4-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="19af4-106">ในกระบวนงานนี้ เราจะสร้างโพรไฟล์สำหรับสถานที่ที่ไม่จำเป็นต้องควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="19af4-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="19af4-107">เราจะเปิดใช้งานสินค้าผสม และสถานะของสินค้าคงคลังผสม และอนุญาตการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="19af4-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="19af4-108">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="19af4-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="19af4-109">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > คลังสินค้า > โพรไฟล์สถานที่**</span><span class="sxs-lookup"><span data-stu-id="19af4-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="19af4-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="19af4-110">Select **New**.</span></span>
3. <span data-ttu-id="19af4-111">ในฟิลด์ **รหัสโพรไฟล์สถานที่** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="19af4-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="19af4-112">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="19af4-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="19af4-113">ในฟิลด์ **รูปแบบสถานที่** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="19af4-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="19af4-114">ในฟิลด์ **ชนิดของสถานที่** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="19af4-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="19af4-115">ในฟิลด์ **รหัสโพรไฟล์การจัดการท่าสินค้า** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="19af4-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="19af4-116">เลือก **ใช่** ในฟิลด์ **อนุญาตสินค้าผสม**</span><span class="sxs-lookup"><span data-stu-id="19af4-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="19af4-117">เลือก **ใช่** ในฟิลด์ **อนุญาตสถานะสินค้าคงคลังแบบผสม**</span><span class="sxs-lookup"><span data-stu-id="19af4-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="19af4-118">เลือก **ใช่** ในฟิลด์ **อนุญาตการตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="19af4-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="19af4-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="19af4-119">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]