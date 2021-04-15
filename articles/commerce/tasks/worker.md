---
title: " ตั้งค่าคอนฟิกผู้ปฏิบัติงาน"
description: กระบวนงานนี้อธิบายวิธีการตั้งค่าคอนฟิกผู้ปฏิบัติงานเป็นพนักงานขายที่มีสิทธิ์สำหรับค่าคอมมิชชันในการขายใน POS
author: jblucher
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43e65de1fda223c2d0503848e7e57936898c1b73
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804076"
---
# <a name="configure-a-worker"></a><span data-ttu-id="d3e14-103"> ตั้งค่าคอนฟิกผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="d3e14-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3e14-104">กระบวนงานนี้อธิบายวิธีการตั้งค่าคอนฟิกผู้ปฏิบัติงานเป็นพนักงานขายที่มีสิทธิ์สำหรับค่าคอมมิชชันในการขายใน POS</span><span class="sxs-lookup"><span data-stu-id="d3e14-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="d3e14-105">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="d3e14-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="d3e14-106">สร้างกลุ่มการขายที่มีค่าคอมมิชชันสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="d3e14-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="d3e14-107">ไปที่การขายและการตลาด > ค่าคอมมิชชัน > กลุ่มการขาย</span><span class="sxs-lookup"><span data-stu-id="d3e14-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="d3e14-108">สามารถกำหนดผู้ปฏิบัติงานให้กับกลุ่มการขายอย่างน้อยหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="d3e14-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="d3e14-109">ใน POS คุณสามารถเลือกกลุ่มการขายใดๆ ที่ประกอบด้วยผู้ปฏิบัติงานจากสมุดที่อยู่ของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d3e14-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="d3e14-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d3e14-110">Click New.</span></span>
3. <span data-ttu-id="d3e14-111">ในฟิลด์กลุ่ม ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d3e14-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="d3e14-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d3e14-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d3e14-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d3e14-113">Click Save.</span></span>
6. <span data-ttu-id="d3e14-114">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="d3e14-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="d3e14-115">คลิกพนักงานขาย</span><span class="sxs-lookup"><span data-stu-id="d3e14-115">Click Sales rep.</span></span>
    * <span data-ttu-id="d3e14-116">กลุ่มการขายสามารถประกอบด้วยผู้ปฏิบัติงานมากกว่าหนึ่งคน</span><span class="sxs-lookup"><span data-stu-id="d3e14-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="d3e14-117">สามารถแบ่งค่าคอมมิชชันระหว่างผู้ปฏิบัติงานต่างๆ โดยขึ้นอยู่กับวิธีที่คุณกำหนดส่วนแบ่งค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="d3e14-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="d3e14-118">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d3e14-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="d3e14-119">ในฟิลด์ส่วนแบ่งค่าคอมมิชชัน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d3e14-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="d3e14-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d3e14-120">Click Save.</span></span>
11. <span data-ttu-id="d3e14-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d3e14-121">Close the page.</span></span>
12. <span data-ttu-id="d3e14-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d3e14-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="d3e14-123">กำหนดกลุ่มการขายเริ่มต้นให้กับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="d3e14-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="d3e14-124">ไปที่ Retail และ Commerce > พนักงาน > ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="d3e14-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="d3e14-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d3e14-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d3e14-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d3e14-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d3e14-127">คลิกแท็บ Commerce</span><span class="sxs-lookup"><span data-stu-id="d3e14-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="d3e14-128">สามารถกำหนดผู้ปฏิบัติงานให้กับกลุ่มการขายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d3e14-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="d3e14-129">กลุ่มการขายเริ่มต้นจะถูกเพิ่มลงในบรรทัดการขายใน POS โดยอัตโนมัติ ถ้ามีการเปิดใช้งานตัวเลือกในโพรไฟล์ฟังก์ชันสำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d3e14-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="d3e14-130">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d3e14-130">Click Edit.</span></span>
6. <span data-ttu-id="d3e14-131">ในฟิลด์กลุ่มเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d3e14-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="d3e14-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d3e14-132">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]