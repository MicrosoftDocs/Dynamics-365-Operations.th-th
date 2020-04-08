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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5832c10e038b7853e9cdf37400a703a1a5e0341
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146295"
---
# <a name="set-up-an-appointment-for-a-load"></a><span data-ttu-id="fb443-103">กำหนดการนัดหมายสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fb443-103">Set up an appointment for a load</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb443-104">กระบวนงานนี้แสดงวิธีการตั้งค่าและวางแผนการนัดหมายที่ท่าสินค้าสำหรับจำนวนงานในศูนย์การผลิต </span><span class="sxs-lookup"><span data-stu-id="fb443-104">This procedure shows how to set up and plan a dock appointment for a load.</span></span> <span data-ttu-id="fb443-105">ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง </span><span class="sxs-lookup"><span data-stu-id="fb443-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="fb443-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="fb443-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-the-load"></a><span data-ttu-id="fb443-107">เลือก จำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="fb443-107">Select the load</span></span>
1. <span data-ttu-id="fb443-108">ไปที่ การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="fb443-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="fb443-109">ล้างข้อมูลกล่องกาเครื่องหมาย ซ่อนสินค้าที่จัดส่งและที่รับ</span><span class="sxs-lookup"><span data-stu-id="fb443-109">Clear the Hide shipped and received check box.</span></span>
3. <span data-ttu-id="fb443-110">ในรายการ เลือกจำนวนงานในศูนย์การผลิตที่มีสถานะเป็นจัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="fb443-110">In the list, select the load that has a status of Shipped.</span></span>
4. <span data-ttu-id="fb443-111">คลิก การขนส่ง</span><span class="sxs-lookup"><span data-stu-id="fb443-111">Click Transportation.</span></span>
5. <span data-ttu-id="fb443-112">คลิก การจัดกำหนดการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="fb443-112">Click Appointment scheduling.</span></span>

## <a name="create-an-appointment"></a><span data-ttu-id="fb443-113">สร้างการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="fb443-113">Create an appointment</span></span>
1. <span data-ttu-id="fb443-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fb443-114">Click New.</span></span>
2. <span data-ttu-id="fb443-115">ในฟิลด์กฎการนัดหมาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="fb443-115">In the Appointment rule field, enter or select a value.</span></span>
3. <span data-ttu-id="fb443-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fb443-116">Click Save.</span></span>
4. <span data-ttu-id="fb443-117">คลิก ปรับปรุงสถานะ</span><span class="sxs-lookup"><span data-stu-id="fb443-117">Click Update status.</span></span>
5. <span data-ttu-id="fb443-118">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="fb443-118">Click Firm.</span></span>
6. <span data-ttu-id="fb443-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fb443-119">Click Save.</span></span>
7. <span data-ttu-id="fb443-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fb443-120">Close the page.</span></span>

