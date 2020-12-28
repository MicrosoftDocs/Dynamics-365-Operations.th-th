---
title: การตั้งค่าช่วงการบริการ
description: ช่วงการให้บริการบ่งชี้ความถี่พร้อมกับรายการใบสั่งบริการถูกสร้างสำหรับรายการข้อตกลงการให้บริการ เมื่อคุณสร้างใบสั่งบริการ
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54eba378548e1bef8ae9c3f4e7b202cf06aeff2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438158"
---
# <a name="set-up-service-intervals"></a><span data-ttu-id="717ed-103">การตั้งค่าช่วงการบริการ</span><span class="sxs-lookup"><span data-stu-id="717ed-103">Set up service intervals</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="717ed-104">ช่วงการให้บริการบ่งชี้ความถี่พร้อมกับรายการใบสั่งบริการถูกสร้างสำหรับรายการข้อตกลงการให้บริการ เมื่อคุณสร้างใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="717ed-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="717ed-105">คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **ข้อตกลงการให้บริการ** \> **ช่วงการบริการ**</span><span class="sxs-lookup"><span data-stu-id="717ed-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="717ed-106">สร้างช่วงเวลาการให้บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="717ed-106">Create a new service interval.</span></span>
3. <span data-ttu-id="717ed-107">ป้อนรหัสและคำอธิบายของช่วงเวลาการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="717ed-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="717ed-108">ในฟิลด์ **ช่วง** เลือกช่วง</span><span class="sxs-lookup"><span data-stu-id="717ed-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="717ed-109">ในฟิลด์ **ความถี่** ให้พิมพ์ความถี่</span><span class="sxs-lookup"><span data-stu-id="717ed-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="717ed-110">ความถี่เป็นปัจจัยที่ซึ่งคุณต้องคูณช่วงเพื่อให้ได้ช่วงเวลาสำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="717ed-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="717ed-111">กด **Alt+S** เพื่อบันทึกช่วงเวลาการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="717ed-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="717ed-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="717ed-112">Example</span></span>

<span data-ttu-id="717ed-113">คุณต้องสร้างช่วงเวลาการให้บริการ 10 วัน</span><span class="sxs-lookup"><span data-stu-id="717ed-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="717ed-114">**การสร้างช่วงเวลาการให้บริการ 10 วัน**</span><span class="sxs-lookup"><span data-stu-id="717ed-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="717ed-115">คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **ข้อตกลงการให้บริการ** \> **ช่วงการบริการ**</span><span class="sxs-lookup"><span data-stu-id="717ed-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="717ed-116">สร้างช่วงเวลาการให้บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="717ed-116">Create a new service interval.</span></span>
3. <span data-ttu-id="717ed-117">ป้อนรหัสและคำอธิบายของช่วงเวลาการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="717ed-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="717ed-118">ในฟิลด์ **ช่วง** เลือก **รายวัน**</span><span class="sxs-lookup"><span data-stu-id="717ed-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="717ed-119">ในฟิลด์ **ความถี่** พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="717ed-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="717ed-120">กด **Alt+S** เพื่อบันทึกช่วงเวลาการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="717ed-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="717ed-121">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="717ed-121">Related topics</span></span>

[<span data-ttu-id="717ed-122">ช่วงการบริการ</span><span class="sxs-lookup"><span data-stu-id="717ed-122">Service intervals</span></span>](service-intervals.md)  
