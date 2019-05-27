---
title: กำหนดการนัดหมายสำหรับสินค้า
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าและวางแผนการนัดหมายที่ท่าสินค้าสำหรับจำนวนงานในศูนย์การผลิต '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSAppointment
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5ede4ab29b5d0c3fcb057049e2abbb9f2bf16f0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560872"
---
# <a name="set-up-an-appointment-for-a-load"></a><span data-ttu-id="8db72-103">กำหนดการนัดหมายสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="8db72-103">Set up an appointment for a load</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8db72-104">กระบวนงานนี้แสดงวิธีการตั้งค่าและวางแผนการนัดหมายที่ท่าสินค้าสำหรับจำนวนงานในศูนย์การผลิต </span><span class="sxs-lookup"><span data-stu-id="8db72-104">This procedure shows how to set up and plan a dock appointment for a load.</span></span> <span data-ttu-id="8db72-105">ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง </span><span class="sxs-lookup"><span data-stu-id="8db72-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="8db72-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="8db72-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-the-load"></a><span data-ttu-id="8db72-107">เลือก จำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="8db72-107">Select the load</span></span>
1. <span data-ttu-id="8db72-108">ไปที่ การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="8db72-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="8db72-109">ล้างข้อมูลกล่องกาเครื่องหมาย ซ่อนสินค้าที่จัดส่งและที่รับ</span><span class="sxs-lookup"><span data-stu-id="8db72-109">Clear the Hide shipped and received check box.</span></span>
3. <span data-ttu-id="8db72-110">ในรายการ เลือกจำนวนงานในศูนย์การผลิตที่มีสถานะเป็นจัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="8db72-110">In the list, select the load that has a status of Shipped.</span></span>
4. <span data-ttu-id="8db72-111">คลิก การขนส่ง</span><span class="sxs-lookup"><span data-stu-id="8db72-111">Click Transportation.</span></span>
5. <span data-ttu-id="8db72-112">คลิก การจัดกำหนดการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="8db72-112">Click Appointment scheduling.</span></span>

## <a name="create-an-appointment"></a><span data-ttu-id="8db72-113">สร้างการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="8db72-113">Create an appointment</span></span>
1. <span data-ttu-id="8db72-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8db72-114">Click New.</span></span>
2. <span data-ttu-id="8db72-115">ในฟิลด์กฎการนัดหมาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="8db72-115">In the Appointment rule field, enter or select a value.</span></span>
3. <span data-ttu-id="8db72-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8db72-116">Click Save.</span></span>
4. <span data-ttu-id="8db72-117">คลิก ปรับปรุงสถานะ</span><span class="sxs-lookup"><span data-stu-id="8db72-117">Click Update status.</span></span>
5. <span data-ttu-id="8db72-118">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="8db72-118">Click Firm.</span></span>
6. <span data-ttu-id="8db72-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8db72-119">Click Save.</span></span>
7. <span data-ttu-id="8db72-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8db72-120">Close the page.</span></span>

