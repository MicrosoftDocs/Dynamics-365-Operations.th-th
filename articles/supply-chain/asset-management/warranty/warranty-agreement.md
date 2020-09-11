---
title: ข้อตกลงการรับประกัน
description: หัวข้อนี้อธิบายถึงข้อตกลงการรับประกันในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f049165fd12dfae672293e0c30ddb186ad3ed12c
ms.sourcegitcommit: 18c5ef10e311f3dd2dbf45c6439ae6beff921af8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/24/2020
ms.locfileid: "3719249"
---
# <a name="warranty-agreements"></a><span data-ttu-id="3ff9d-103">ข้อตกลงการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="3ff9d-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="3ff9d-104">ในการจัดการสินทรัพย์คุณสามารถตั้งค่าเงื่อนไขการรับประกันซึ่งสามารถเชื่อมโยงกับสินทรัพย์หรือชนิดสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="3ff9d-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="3ff9d-105">เงื่อนไขการรับประกันจะถูกสร้างขึ้นสำหรับรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3ff9d-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="3ff9d-106">คุณสามารถตั้งค่าการรับประกันเพื่อให้ครอบคลุมบางส่วนทั้งหมด และคุณสามารถตั้งค่าเงื่อนไขที่เกี่ยวข้องกับชั่วโมง ค่าใช้จ่าย และสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="3ff9d-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="3ff9d-107">ขั้นตอนแรกคือสร้างข้อตกลงการรับประกันของผู้จัดจำหน่ายที่คุณมีสำหรับอุปกรณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3ff9d-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="3ff9d-108">หลังจากนั้นคุณจะแนบข้อตกลงการรับประกันกับสินทรัพย์หรือชนิดสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="3ff9d-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="3ff9d-109">ข้อตกลงการรับประกันของผู้จัดจำหน่ายจะใช้เพื่อวัตถุประสงค์ในการให้ข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3ff9d-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="3ff9d-110">หากมีการตั้งค่าการรับประกันของผู้จัดจำหน่ายในสินทรัพย์ คุณจะเห็นรอบระยะเวลาที่ครอบคลุมการรับประกันของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="3ff9d-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="3ff9d-111">สร้างข้อตกลงการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="3ff9d-111">Create a warranty agreement</span></span>

<span data-ttu-id="3ff9d-112">ข้อตกลงการรับประกันสามารถรวมรายการข้อตกลงต่างๆ เพื่อครอบคลุมการรับประกันสำหรับชั่วโมงทำงาน ค่าใช้จ่าย และสินค้า</span><span class="sxs-lookup"><span data-stu-id="3ff9d-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="3ff9d-113">เลือก **การจัดการสินทรัพย์** \> **ตั้งค่า** \> **สินทรัพย์** \> **การรับประกัน**</span><span class="sxs-lookup"><span data-stu-id="3ff9d-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="3ff9d-114">เลือก **ใหม่** เพื่อสร้างผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3ff9d-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="3ff9d-115">ในฟิลด์ **การรับประกัน** ป้อนรหัสการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="3ff9d-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="3ff9d-116">ในฟิลด์ **ชื่อ** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3ff9d-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="3ff9d-117">บนแท็บด่วน **รายละเอียด** ฟิลด์ **สินทรัพย์** จะแสดงจำนวนของสินทรัพย์ที่ใช้งานอยู่ที่ใช้ข้อตกลงการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="3ff9d-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="3ff9d-118">บนแท็บด่วน **รายการรับประกัน** ให้ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มรายการที่ควรรวมอยู่ในข้อตกลงการรับประกัน:</span><span class="sxs-lookup"><span data-stu-id="3ff9d-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="3ff9d-119">เลือก **เพิ่มรายการ** เพื่อเพิ่มเงื่อนไขใหม่ไปยังการับประกัน</span><span class="sxs-lookup"><span data-stu-id="3ff9d-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="3ff9d-120">มีการป้อนหมายเลขรายการตามลำดับโดยอัตโนมัติในฟิลด์ **รายการ**</span><span class="sxs-lookup"><span data-stu-id="3ff9d-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="3ff9d-121">ในฟิลด์ **รอบระยะเวลา** ให้เลือกชนิดของรอบระยะเวลาการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="3ff9d-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="3ff9d-122">ในฟิลด์ **ช่วงเวลา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3ff9d-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="3ff9d-123">ฟิลด์นี้จะกำหนดจำนวนของรอบระยะเวลาที่การรับประกันควรมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="3ff9d-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="3ff9d-124">ในฟิลด์ **เปอร์เซ็นต์** ให้ป้อนเปอร์เซ็นต์ความครอบคลุมสำหรับรายการการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="3ff9d-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="3ff9d-125">เปอร์เซ็นต์บ่งชี้ว่าบริษัทของคุณครอบคลุมมากน้อยเพียงใด</span><span class="sxs-lookup"><span data-stu-id="3ff9d-125">The percentage indicates how much is covered by your company.</span></span>

![หน้าการรับประกัน](media/01-warranty.png)
