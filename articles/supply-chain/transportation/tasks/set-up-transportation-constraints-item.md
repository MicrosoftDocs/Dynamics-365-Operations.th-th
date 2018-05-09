--- 
title: "ตั้งค่าข้อจำกัดในการขนส่งสำหรับสินค้า"
description: "กระบวนงานนี้จะตั้งค่าข้อจำกัดในการขนส่ง เพื่อป้องกันสินค่าที่เลือกจากการถูกขนส่งแล้วไปยังฮับที่เลือก"
author: BibiSp
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 92ad8afe8eb2943377a1a130f466b0dd833b8015
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="2f368-103">ตั้งค่าข้อจำกัดในการขนส่งสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="2f368-103">Set up transportation constraints for an item</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f368-104">กระบวนงานนี้จะตั้งค่าข้อจำกัดในการขนส่ง เพื่อป้องกันสินค่าที่เลือกจากการถูกขนส่งแล้วไปยังฮับที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2f368-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="2f368-105">โดยทั่วไปงานนี้จะดำเนินการโดยผู้ประสานงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="2f368-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="2f368-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="2f368-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constraint"></a><span data-ttu-id="2f368-107">สร้างข้อจำกัดสินค้า</span><span class="sxs-lookup"><span data-stu-id="2f368-107">Create an item constraint</span></span>
1. <span data-ttu-id="2f368-108">ไปที่ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="2f368-108">Go to Constraints.</span></span>
2. <span data-ttu-id="2f368-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2f368-109">Click New.</span></span>
3. <span data-ttu-id="2f368-110">ในฟิลด์ข้อจำกัดสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2f368-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="2f368-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="2f368-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2f368-112">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2f368-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="2f368-113">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2f368-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="2f368-114">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2f368-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="2f368-115">ในฟิลด์ฮับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2f368-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="2f368-116">ในฟิลด์การดำเนินการข้อจำกัด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2f368-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="2f368-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2f368-117">Click Save.</span></span>
11. <span data-ttu-id="2f368-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2f368-118">Close the page.</span></span>


