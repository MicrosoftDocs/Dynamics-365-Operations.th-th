---
title: สร้างโพรไฟล์สถานที่
description: 'สถานที่ทุกแห่งในคลังสินค้าจะต้องมีโพรไฟล์สถานที่เกี่ยวข้องกันซึ่งอธิบายคุณสมบัติของสถานที่ดังกล่าว ตัวอย่างเช่น สถานที่แห่งนั้นอนุญาตสำหรับสินค้าผสมหรือไม่ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bc7705b7db46af8fbe8bf9e78a878a53249b452
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560920"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="611db-103">สร้างโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="611db-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="611db-104">สถานที่ทุกแห่งในคลังสินค้าจะต้องมีโพรไฟล์สถานที่เกี่ยวข้องกันซึ่งอธิบายคุณสมบัติของสถานที่ดังกล่าว ตัวอย่างเช่น สถานที่แห่งนั้นอนุญาตสำหรับสินค้าผสมหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="611db-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="611db-105">ในกระบวนงานนี้ เราจะสร้างโพรไฟล์สำหรับสถานที่ที่ไม่จำเป็นต้องควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="611db-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="611db-106">เราจะอนุญาตสำหรับสถานะของสินค้าผสม และสินค้าคงคลังผสม และอนุญาตการตรวจนับตามรอบ </span><span class="sxs-lookup"><span data-stu-id="611db-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="611db-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="611db-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="611db-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="611db-108">Click New.</span></span>
2. <span data-ttu-id="611db-109">ในฟิลด์รหัสโพรไฟล์สถานที่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="611db-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="611db-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="611db-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="611db-111">ในฟิลด์รูปแบบสถานที่ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="611db-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="611db-112">ในฟิลด์ชนิดของสถานที่ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="611db-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="611db-113">ในฟิลด์รหัสโพรไฟล์การจัดการท่าสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="611db-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="611db-114">เลือก ใช่ ในฟิลด์อนุญาตสินค้าผสม</span><span class="sxs-lookup"><span data-stu-id="611db-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="611db-115">เลือก ใช่ ในฟิลด์อนุญาตสถานะสินค้าคงคลังแบบผสม</span><span class="sxs-lookup"><span data-stu-id="611db-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="611db-116">เลือกใช่ในฟิลด์อนุญาตการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="611db-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="611db-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="611db-117">Click Save.</span></span>
11. <span data-ttu-id="611db-118">ไปที่การจัดการคลังสินค้า > การตั้งค่า > คลังสินค้า > โพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="611db-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

