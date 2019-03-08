---
title: การสร้างการชำระเงินภาษีขาย
description: งานชำระและลงรายการบัญชีภาษีขายจะชำระยอดภาษีขายในบัญชีภาษีขาย และออฟเซ็ตไปยังบัญชีการชำระภาษีขายสำหรับรอบระยะเวลาที่กำหนด
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d72c88d6ba851e96ca07b896630549690e9396
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "321765"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="3c712-103">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3c712-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c712-104">งานชำระและลงรายการบัญชีภาษีขายจะชำระยอดภาษีขายในบัญชีภาษีขาย และออฟเซ็ตไปยังบัญชีการชำระภาษีขายสำหรับรอบระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="3c712-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="3c712-105">ไปที่ ภาษี > การรายงาน > ภาษีขาย > ชำระและลงรายการภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3c712-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="3c712-106">ในฟิลด์รอบระยะเวลาการจ่ายเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3c712-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3c712-107">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3c712-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3c712-108">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c712-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="3c712-109">ถ้าไม่มีการเลือกตัวเลือกการแก้ไขรวมบนหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป การชำระบัญชีจะมีการประมวลผลเป็นเวอร์ชันต่างๆ </span><span class="sxs-lookup"><span data-stu-id="3c712-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="3c712-110">ต้นฉบับเป็นการชำระบัญชีแรกสำหรับช่วงรอบระยะเวลาและมีการประมวลผลเพียงครั้งเดียวสำหรับช่วงรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="3c712-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="3c712-111">การแก้ไขครั้งล่าสุดจะเป็นการชำระธุรกรรมภาษีขายซึ่งมีการลงรายการบัญชีไว้หลังจากสร้างเวอร์ชันต้นฉบับแล้ว</span><span class="sxs-lookup"><span data-stu-id="3c712-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="3c712-112">ในฟิลด์วันที่ทำธุรกรรม ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c712-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="3c712-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="3c712-113">Click OK.</span></span>

