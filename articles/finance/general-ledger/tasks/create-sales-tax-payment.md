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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99059a8e5d6f4bf125266ad2a98cb73751529e6b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139941"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="befe4-103">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="befe4-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="befe4-104">งานชำระและลงรายการบัญชีภาษีขายจะชำระยอดภาษีขายในบัญชีภาษีขาย และออฟเซ็ตไปยังบัญชีการชำระภาษีขายสำหรับรอบระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="befe4-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="befe4-105">ไปที่ ภาษี > การรายงาน > ภาษีขาย > ชำระและลงรายการภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="befe4-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="befe4-106">ในฟิลด์รอบระยะเวลาการจ่ายเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="befe4-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="befe4-107">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="befe4-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="befe4-108">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="befe4-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="befe4-109">ถ้าไม่มีการเลือกตัวเลือกการแก้ไขรวมบนหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป การชำระบัญชีจะมีการประมวลผลเป็นเวอร์ชันต่างๆ </span><span class="sxs-lookup"><span data-stu-id="befe4-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="befe4-110">ต้นฉบับเป็นการชำระบัญชีแรกสำหรับช่วงรอบระยะเวลาและมีการประมวลผลเพียงครั้งเดียวสำหรับช่วงรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="befe4-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="befe4-111">การแก้ไขครั้งล่าสุดจะเป็นการชำระธุรกรรมภาษีขายซึ่งมีการลงรายการบัญชีไว้หลังจากสร้างเวอร์ชันต้นฉบับแล้ว</span><span class="sxs-lookup"><span data-stu-id="befe4-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="befe4-112">ในฟิลด์วันที่ทำธุรกรรม ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="befe4-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="befe4-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="befe4-113">Click OK.</span></span>

