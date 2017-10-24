--- 
title: "สร้างกลุ่มการรวมบัญชีและบัญชีหลักในการรวมบัญชีเพิ่มเติม"
description: "ขั้นตอนนี้แสดงวิธีการสร้างกลุ่มบัญชีการรวมบัญชี และเพิ่มบัญชีให้กับกลุ่มนั้น "
author: aprilolson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ee28b91d21050b08909ef701901398043d32abce
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="98815-103">สร้างกลุ่มการรวมบัญชีและบัญชีหลักในการรวมบัญชีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="98815-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98815-104">ขั้นตอนนี้แสดงวิธีการสร้างกลุ่มบัญชีการรวมบัญชี และเพิ่มบัญชีให้กับกลุ่มนั้น </span><span class="sxs-lookup"><span data-stu-id="98815-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="98815-105">ขั้นตอนนี้ใช้ข้อมูลบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="98815-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="98815-106">สร้างกลุ่มบัญชีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="98815-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="98815-107">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > กลุ่มบัญชีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="98815-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="98815-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="98815-108">Click New.</span></span>
3. <span data-ttu-id="98815-109">ในฟิลด์กลุ่มบัญชีการรวมบัญชี ให้ป้อนรหัสเฉพาะตัวระบุสำหรับกลุ่มบัญชีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="98815-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="98815-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="98815-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="98815-111">เพิ่มบัญชีลงในกลุ่มบัญชีหลักในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="98815-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="98815-112">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="98815-112">Close the page.</span></span>
2. <span data-ttu-id="98815-113">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > บัญชีการรวมบัญชีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="98815-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="98815-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="98815-114">Click New.</span></span>
4. <span data-ttu-id="98815-115">ในฟิลด์บัญชีหลัก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="98815-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="98815-116">ในรายการ ให้คลิกบัญชีหลักที่คุณต้องการแม็ป </span><span class="sxs-lookup"><span data-stu-id="98815-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="98815-117">ในฟิลด์บัญชีหลักในการรวมบัญชี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="98815-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="98815-118">ในรายการ ให้คลิกบัญชีหลักในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="98815-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="98815-119">ในฟิลด์บัญชีหลักในการรวมบัญชี ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="98815-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="98815-120">ในฟิลด์ชื่อบัญชีหลักในการรวมบัญชี ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="98815-120">In the Consolidation account name field, type a value.</span></span>


