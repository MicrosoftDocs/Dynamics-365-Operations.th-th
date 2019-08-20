---
title: ตั้งค่าข้อจำกัดในการขนส่งสำหรับสินค้า
description: กระบวนงานนี้จะตั้งค่าข้อจำกัดในการขนส่ง เพื่อป้องกันสินค่าที่เลือกจากการถูกขนส่งแล้วไปยังฮับที่เลือก
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f686b29151cfbbeeffbf1f8fb98ea6ce5bc51d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836080"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="d87fa-103">ตั้งค่าข้อจำกัดในการขนส่งสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="d87fa-103">Set up transportation constraints for an item</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d87fa-104">กระบวนงานนี้จะตั้งค่าข้อจำกัดในการขนส่ง เพื่อป้องกันสินค่าที่เลือกจากการถูกขนส่งแล้วไปยังฮับที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d87fa-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="d87fa-105">โดยทั่วไปงานนี้จะดำเนินการโดยผู้ประสานงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="d87fa-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="d87fa-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="d87fa-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="d87fa-107">สร้างข้อจำกัดสินค้า</span><span class="sxs-lookup"><span data-stu-id="d87fa-107">Create an item constaint</span></span>
1. <span data-ttu-id="d87fa-108">ไปที่ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="d87fa-108">Go to Constraints.</span></span>
2. <span data-ttu-id="d87fa-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d87fa-109">Click New.</span></span>
3. <span data-ttu-id="d87fa-110">ในฟิลด์ข้อจำกัดสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d87fa-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="d87fa-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d87fa-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d87fa-112">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d87fa-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="d87fa-113">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d87fa-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="d87fa-114">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d87fa-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="d87fa-115">ในฟิลด์ฮับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d87fa-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="d87fa-116">ในฟิลด์การดำเนินการข้อจำกัด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d87fa-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="d87fa-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d87fa-117">Click Save.</span></span>
11. <span data-ttu-id="d87fa-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d87fa-118">Close the page.</span></span>

