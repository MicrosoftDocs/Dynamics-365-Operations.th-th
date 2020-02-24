---
title: จัดการการมอบหมายสำหรับค่าใช้จ่าย
description: ผู้ใช้ที่ได้รับมอบสิทธิ์ในการใช้ค่าใช้จ่ายสามารถสร้างและจัดการรายงานค่าใช้จ่ายในนามของพนักงานอีกคนหนึ่งในองค์กร
author: KimANelson
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2020-01-10
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: d792daa56d468830b56eb395fadda582b3b5bad6
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015406"
---
# <a name="manage-expense-delegation"></a><span data-ttu-id="4ffb9-103">จัดการการมอบหมายสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4ffb9-103">Manage expense delegation</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="4ffb9-104">ผู้ใช้ที่ได้รับมอบสิทธิ์ในการใช้ค่าใช้จ่ายสามารถสร้างและจัดการรายงานค่าใช้จ่ายในนามของพนักงานอีกคนหนึ่งในองค์กร</span><span class="sxs-lookup"><span data-stu-id="4ffb9-104">An expense delegate user can create and manage expense reports on behalf of another employee in the organization.</span></span>

## <a name="configuring-expense-delegation"></a><span data-ttu-id="4ffb9-105">ตั้งค่าคอนฟิกการมอบหมายค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4ffb9-105">Configuring expense delegation</span></span>

<span data-ttu-id="4ffb9-106">หากต้องการตั้งค่าผู้ใช้เป็นผู้ได้มอบหมายได้รับมอบสิทธิ์ในการใช้ค่าใช้จ่าย ให้ไปที่ **การจัดการค่าใช้จ่าย > ตั้งค่า > ทั่วไป > ผู้รับมอบสิทธิ์** เพื่อเปิดหน้า **ผู้รับมอบสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="4ffb9-106">To set up a user as an expense delegate, go to **Expense management > Setup > General > Delegates** to open the **Delegates** page.</span></span> <span data-ttu-id="4ffb9-107">เลือก **สร้าง** แล้วเลือกพนักงานที่จะมีการกำหนดเป็นผู้รับมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="4ffb9-107">Select **New** and then select the employee that will have a delegate defined.</span></span> <span data-ttu-id="4ffb9-108">ป้อนนามแฝงของผู้ใช้ที่เป็นผู้รับมอบสิทธิ์และวันที่เริ่มต้นและสิ้นสุดสำหรับรอบระยะเวลาการรับมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="4ffb9-108">Enter the alias of the delegate user and the start and end date for the delegation period.</span></span>

## <a name="managing-expense-delegation-on-behalf-of-another-employee"></a><span data-ttu-id="4ffb9-109">การจัดการการมอบสิทธิ์ในการใช้ค่าใช้จ่ายในนามของพนักงานอีกคนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4ffb9-109">Managing expense delegation on behalf of another employee</span></span>

<span data-ttu-id="4ffb9-110">ถ้าการจัดการคุณลักษณะที่สำคัญ **เปิดใช้หน้ารายการของผู้รับมอบสิทธิ์การใช้ค่าใช้จ่าย** มีการเปิดใช้ หน้ารายการ **ค่าใช้จ่ายที่มอบหมายให้กับฉัน** จะพร้อมใช้งานโดยการนำทางไปยัง **การจัดการค่าใช้จ่าย > ค่าใช้จ่าของฉัน> ค่าใช้จ่ายที่มอบหมายให้กับฉัน**</span><span class="sxs-lookup"><span data-stu-id="4ffb9-110">If the feature management key **Enable expense delegates list page** is enabled, the **Expenses delegated to me** list page will be available by navigating to **Expense management > My expenses > Expenses delegated to me**.</span></span>

<span data-ttu-id="4ffb9-111">ผู้ใช้ที่เป็นผู้รับมอบสิทธิ์สามารถกรองข้อมูลและค้นหารายงานค่าใช้จ่ายที่มีอยู่ซึ่งได้รับมอบหมายให้กับผู้ใช้ได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="4ffb9-111">A delegate user can quickly filter and search on existing expense reports that hae been delegated to the user.</span></span> <span data-ttu-id="4ffb9-112">ผู้ใช้ยังสามารถสร้างรายงานค่าใช้จ่ายใหม่ในนามของผู้ใช้รายอื่นโดยการคลิก **รายงานค่าใช้จ่ายใหม่** ได้อย่างเร็ว</span><span class="sxs-lookup"><span data-stu-id="4ffb9-112">The user can also quickly create a new expense report on behalf of other users by clicking **New expense report**.</span></span>

<span data-ttu-id="4ffb9-113">ผู้ใช้ที่ได้รับมอบสิทธิ์ยังสามารถสร้างและจัดการรายงานค่าใช้จ่ายในนามของพนักงานอื่นๆได้โดยการนำทางไปยัง **การจัดการค่าใช้จ่าย > ค่าใช้จ่าของฉัน > รายงานค่าใช้จ่าย** และคลิกที่ปุ่ม **เปิดค่าใช้จ่ายของผู้ใช้อื่น**</span><span class="sxs-lookup"><span data-stu-id="4ffb9-113">Delegate users can also create and manage expense reports on behalf of other employees by navigating to **Expense management > My expenses > Expense reports** and clicking the **Open other user's expenses** button.</span></span>
