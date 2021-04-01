---
title: สร้างโพรไฟล์สถานที่
description: หัวข้อนี้อธิบายวิธีการสร้างโพรไฟล์สถานที่ใน Dynamics 365 Supply Chain Management
author: ShylaThompson
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9be25004452ab0a0e2af0ac552a69f805d301d8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239073"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="886c2-103">สร้างโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="886c2-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="886c2-104">หัวข้อนี้อธิบายวิธีการสร้างโพรไฟล์สถานที่ใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="886c2-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="886c2-105">สถานที่ทุกแห่งในคลังสินค้าจะต้องมีโพรไฟล์สถานที่เกี่ยวข้องกันซึ่งอธิบายคุณสมบัติของสถานที่ดังกล่าว ตัวอย่างเช่น สถานที่แห่งนั้นอนุญาตสำหรับสินค้าผสมหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="886c2-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="886c2-106">ในกระบวนงานนี้ เราจะสร้างโพรไฟล์สำหรับสถานที่ที่ไม่จำเป็นต้องควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="886c2-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="886c2-107">เราจะเปิดใช้งานสินค้าผสม และสถานะของสินค้าคงคลังผสม และอนุญาตการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="886c2-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="886c2-108">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="886c2-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="886c2-109">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > คลังสินค้า > โพรไฟล์สถานที่**</span><span class="sxs-lookup"><span data-stu-id="886c2-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="886c2-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="886c2-110">Select **New**.</span></span>
3. <span data-ttu-id="886c2-111">ในฟิลด์ **รหัสโพรไฟล์สถานที่** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="886c2-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="886c2-112">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="886c2-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="886c2-113">ในฟิลด์ **รูปแบบสถานที่** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="886c2-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="886c2-114">ในฟิลด์ **ชนิดของสถานที่** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="886c2-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="886c2-115">ในฟิลด์ **รหัสโพรไฟล์การจัดการท่าสินค้า** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="886c2-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="886c2-116">เลือก **ใช่** ในฟิลด์ **อนุญาตสินค้าผสม**</span><span class="sxs-lookup"><span data-stu-id="886c2-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="886c2-117">เลือก **ใช่** ในฟิลด์ **อนุญาตสถานะสินค้าคงคลังแบบผสม**</span><span class="sxs-lookup"><span data-stu-id="886c2-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="886c2-118">เลือก **ใช่** ในฟิลด์ **อนุญาตการตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="886c2-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="886c2-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="886c2-119">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]