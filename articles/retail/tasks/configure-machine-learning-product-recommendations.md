--- 
title: " ตั้งค่าคอนฟิกสำหรับคำแนะนำผลิตภัณฑ์ที่ใช้ Machine Learning"
description: "กระบวนงานนี้จะรีเฟรชข้อมลในที่จัดเก็บเอนทิตี้ซึ่งระบบ Machine Learning นำไปใช้ซึ่งสนับสนุนคำแนะนำผลิตภัณฑ์ และจากนั้นจะเปิดใช้งานคำแนะนำผลิตภัณฑ์บนไคลเอนต์ POS "
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="6af22-103"> ตั้งค่าคอนฟิกสำหรับคำแนะนำผลิตภัณฑ์ที่ใช้ Machine Learning</span><span class="sxs-lookup"><span data-stu-id="6af22-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6af22-104">กระบวนงานนี้จะรีเฟรชข้อมลในที่จัดเก็บเอนทิตี้ซึ่งระบบ Machine Learning นำไปใช้ซึ่งสนับสนุนคำแนะนำผลิตภัณฑ์ และจากนั้นจะเปิดใช้งานคำแนะนำผลิตภัณฑ์บนไคลเอนต์ POS </span><span class="sxs-lookup"><span data-stu-id="6af22-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="6af22-105">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="6af22-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6af22-106">ไปที่ การจัดการระบบ > การตั้งค่า > ที่จัดเก็บเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6af22-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="6af22-107">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ด 'RetailSales'</span><span class="sxs-lookup"><span data-stu-id="6af22-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="6af22-108">คลิก รีเฟรช</span><span class="sxs-lookup"><span data-stu-id="6af22-108">Click Refresh.</span></span>
4. <span data-ttu-id="6af22-109">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6af22-109">Click OK.</span></span>
5. <span data-ttu-id="6af22-110">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6af22-110">Close the page.</span></span>
6. <span data-ttu-id="6af22-111">ไปที่การขายปลีกและการค้า > การตั้งค่าศูนย์ควบคุม > พารามิเตอร์ > พารามิเตอร์การขายปลีก</span><span class="sxs-lookup"><span data-stu-id="6af22-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="6af22-112">คลิกแท็บ Machine Learning</span><span class="sxs-lookup"><span data-stu-id="6af22-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="6af22-113">เลือก 'ใช่' ในฟิลด์ เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6af22-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="6af22-114">ถ้าคุณได้รับข้อความ "ไม่สามารถดึงข้อมูลแบบจำลองคำแนะนำ" อาจเป็นเพราะคุณรีเฟรชที่จัดเก็บเอนทิตี้เมื่อเร็วๆ นี้ และระบบอาจยังปรับข้อมูลใหม่ไม่เสร็จสิ้น </span><span class="sxs-lookup"><span data-stu-id="6af22-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="6af22-115">โปรดรอ 2-3 ชั่วโมงแล้วลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="6af22-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="6af22-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6af22-116">Click Save.</span></span>
10. <span data-ttu-id="6af22-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6af22-117">Close the page.</span></span>


