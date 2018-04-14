--- 
title: "การสร้างการชำระเงินภาษีขาย"
description: "งานชำระและลงรายการบัญชีภาษีขายจะชำระยอดภาษีขายในบัญชีภาษีขาย และออฟเซ็ตไปยังบัญชีการชำระภาษีขายสำหรับรอบระยะเวลาที่กำหนด"
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ffd79bbb0178f8639af3cec60b4ef3a20428799f
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="c09ca-103">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="c09ca-103">Create a sales tax payment</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c09ca-104">งานชำระและลงรายการบัญชีภาษีขายจะชำระยอดภาษีขายในบัญชีภาษีขาย และออฟเซ็ตไปยังบัญชีการชำระภาษีขายสำหรับรอบระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="c09ca-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="c09ca-105">ไปที่ ภาษี > การรายงาน > ภาษีขาย > ชำระและลงรายการภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="c09ca-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="c09ca-106">ในฟิลด์รอบระยะเวลาการจ่ายเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c09ca-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c09ca-107">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c09ca-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c09ca-108">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c09ca-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="c09ca-109">ถ้าไม่มีการเลือกตัวเลือกการแก้ไขรวมบนหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป การชำระบัญชีจะมีการประมวลผลเป็นเวอร์ชันต่างๆ </span><span class="sxs-lookup"><span data-stu-id="c09ca-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="c09ca-110">ต้นฉบับเป็นการชำระบัญชีแรกสำหรับช่วงรอบระยะเวลาและมีการประมวลผลเพียงครั้งเดียวสำหรับช่วงรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="c09ca-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="c09ca-111">การแก้ไขครั้งล่าสุดจะเป็นการชำระธุรกรรมภาษีขายซึ่งมีการลงรายการบัญชีไว้หลังจากสร้างเวอร์ชันต้นฉบับแล้ว</span><span class="sxs-lookup"><span data-stu-id="c09ca-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="c09ca-112">ในฟิลด์วันที่ทำธุรกรรม ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c09ca-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="c09ca-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c09ca-113">Click OK.</span></span>


