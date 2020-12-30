---
title: การสร้างการชำระเงินภาษีขาย
description: งานชำระและลงรายการบัญชีขั้นตอนงานภาษีขายจะชำระยอดภาษีขายในบัญชีภาษีขาย และออฟเซ็ตไปยังบัญชีการชำระภาษีขายสำหรับรอบระยะเวลาที่กำหนด
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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7aec00c2fb657f0b4074063ef7acad5f4372ebca
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646346"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="5490b-103">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="5490b-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5490b-104">งานชำระและลงรายการบัญชีขั้นตอนงานภาษีขายจะชำระยอดภาษีขายในบัญชีภาษีขาย และออฟเซ็ตไปยังบัญชีการชำระภาษีขายสำหรับรอบระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="5490b-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="5490b-105">ไปที่ **ภาษี > การรายงาน > ภาษีขาย > ชำระและลงรายการภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="5490b-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="5490b-106">ในฟิลด์ **รอบระยะเวลาการจ่ายเงิน** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5490b-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5490b-107">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5490b-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5490b-108">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5490b-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="5490b-109">ถ้าคุณไม่เลือกตัวเลือก **การแก้ไขรวม** บนหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป** การชำระบัญชีจะมีการประมวลผลเป็นเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="5490b-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="5490b-110">ต้นฉบับเป็นการชำระบัญชีแรกสำหรับช่วงรอบระยะเวลาและมีการประมวลผลเพียงครั้งเดียวสำหรับช่วงรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="5490b-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="5490b-111">การแก้ไขครั้งล่าสุดจะเป็นการชำระธุรกรรมภาษีขายซึ่งมีการลงรายการบัญชีไว้หลังจากสร้างเวอร์ชันต้นฉบับแล้ว</span><span class="sxs-lookup"><span data-stu-id="5490b-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="5490b-112">ในฟิลด์ **วันที่ทำธุรกรรม** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5490b-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="5490b-113">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5490b-113">Click **OK**.</span></span>

