---
title: สร้างกลุ่มสัญญาเช่า
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่ากลุ่มสัญญาเช่า ต้องใช้กลุ่มสัญญาเช่าเพื่อสร้างการเช่าใหม่
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 88a49e4db868078fd05875df33ca5727363aaa18
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881239"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="b2875-104">สร้างกลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b2875-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2875-105">หัวข้อนี้จะอธิบายวิธีการตั้งค่ากลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b2875-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="b2875-106">ต้องใช้กลุ่มสัญญาเช่าเพื่อสร้างการเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="b2875-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="b2875-107">สมุดบัญชีการเช่าเชื่อมโยงกับแต่ละกลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b2875-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="b2875-108">บัญชีการเช่าจะกำหนดสมุดบัญชีเริ่มต้นที่จะต้องสร้างขึ้นสำหรับแต่ละสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b2875-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="b2875-109">คุณสามารถกำหนดบัญชีหนึ่ง ๆ ให้กับกลุ่มสัญญาเช่าในหน้า **พารามิเตอร์การลงรายการบัญชีสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="b2875-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="b2875-110">สร้างสมุดบัญชีสัญญาเช่าและเพิ่มกลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b2875-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="b2875-111">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> กลุ่มสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="b2875-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="b2875-112">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเพิ่มกลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b2875-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="b2875-113">มีการเพิ่มบรรทัดเข้าในกริด</span><span class="sxs-lookup"><span data-stu-id="b2875-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="b2875-114">บนบรรทัดใหม่ ในฟิลด์ **กลุ่มสัญญาเช่า** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="b2875-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="b2875-115">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="b2875-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="b2875-116">ข้อมูลที่คุณเพิ่งป้อนจะถูกเพิ่มลงในฟิลด์ **กลุ่มสัญญาเช่า** ในหน้า **เพิ่มสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="b2875-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="b2875-117">เชื่อมโยงสมุดบัญชีกับกลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b2875-117">Associate a book with a lease group</span></span>

<span data-ttu-id="b2875-118">หลังจากที่คุณสร้างกลุ่มสัญญาเช่าแล้ว คุณสามารถกำหนดสมุดบัญชีให้กับแต่ละกลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="b2875-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="b2875-119">เมื่อคุณสร้างสัญญาเช่าและกำหนดให้กับกลุ่มสัญญาเช่า ระบบจะสร้างชุดของกำหนดการสำหรับสมุดบัญชีแต่ละเล่มที่สัมพันธ์กับกลุ่มสัญญาเช่านั้น</span><span class="sxs-lookup"><span data-stu-id="b2875-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="b2875-120">ต้องตั้งค่าสมุดบัญชีก่อนจึงจะสามารถกำหนดให้กับกลุ่มสัญญาเช่าได้</span><span class="sxs-lookup"><span data-stu-id="b2875-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="b2875-121">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> กลุ่มสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="b2875-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="b2875-122">เลือกกลุ่มสัญญาเช่า แล้วเลือก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="b2875-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="b2875-123">เลือก **สร้าง** จากนั้นในฟิลด์ **ชนิดสมุดบัญชี** ให้เลือกสมุดบัญชีที่จะกำหนดให้กับกลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b2875-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="b2875-124">คุณสามารถกำหนดหลายเล่มให้กับกลุ่มสัญญาเช่าถ้าต้องการให้สัญญาเช่าอยู่ในรูปแบบที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b2875-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
