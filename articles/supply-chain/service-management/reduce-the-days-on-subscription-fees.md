---
title: การลดจำนวนวันของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก
description: ถ้าต้องการลดจำนวนวันของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิกปัจจุบัน คุณสามารถสร้างธุรกรรมใหม่ซึ่งคุณลบรอบระยะเวลาที่ไม่ควรอยู่ในช่วงเวลาของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04b183d8fc8083c630bcb4e0e69fb755f8a50f95
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569741"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="e618b-103">การลดจำนวนวันของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="e618b-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e618b-104">ถ้าต้องการลดจำนวนวันของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิกปัจจุบัน คุณสามารถสร้างธุรกรรมใหม่ซึ่งคุณลบรอบระยะเวลาที่ไม่ควรอยู่ในช่วงเวลาของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="e618b-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="e618b-105">การลดจำนวนวัดของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="e618b-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="e618b-106">คลิก **การจัดการงานบริการ** \> **ทั่วไป** \> **การบอกรับเป็นสมาชิกการบริการ** \> **การบอกรับเป็นสมาชิกการบริการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e618b-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="e618b-107">เลือกการบอกรับเป็นสมาชิกการบริการ และในบานหน้าต่างการดำเนินการ ให้คลิก **ค่าธรรมเนียมการบอกรับเป็นสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="e618b-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="e618b-108">ในฟิลด์ **ชนิดของการบอกรับเป็นสมาชิก** เลือก **จำนวนวันที่ลด**</span><span class="sxs-lookup"><span data-stu-id="e618b-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="e618b-109">ใช้ฟิลด์ **วันที่เริ่มต้น** และฟิลด์ **วันที่สิ้นสุด** เพื่อระบุช่วงวันที่ของค่าธรรมเนียมการบอกรับเป็นสมาชิกที่คุณต้องการลบออกจากรอบระยะเวลาของค่าธรรมเนียมการบอกรับเป็นสมาชิก แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e618b-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="e618b-110">หากต้องการดูธุรกรรมที่สร้างขึ้น ในแบบฟอร์ม **การบอกรับเป็นสมาชิก** คลิก **ธุรกรรมค่าธรรมเนียม**</span><span class="sxs-lookup"><span data-stu-id="e618b-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="e618b-111">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e618b-111">Example</span></span>

<span data-ttu-id="e618b-112">หากรอบระยะเวลาของธุรกรรมการบอกรับเป็นสมาชิกเริ่มต้นตั้งแต่วันที่ 1 มกราคม ถึง 31 มกราคม และคุณต้องการลดระยะเวลาลง 10 วัน ให้คุณสร้างธุรกรรมใหม่ซึ่งมีรอบระยะเวลาการลดเป็น 1 มกราคม ถึง 10 มกราคม</span><span class="sxs-lookup"><span data-stu-id="e618b-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="e618b-113">(รอบระยะเวลาการลดยังอาจเป็นวันที่ 5 มกราคมถึง 15 มกราคม หรือระยะเวลาสิบวันใดก็ได้)</span><span class="sxs-lookup"><span data-stu-id="e618b-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="e618b-114">นอกจากนี้ หาก **วันที่เริ่มต้น** ในรอบระยะเวลาการลดเป็น 21 มกราคม (31 ลบ 10) คุณสามารถตั้ง **วันที่สิ้นสุด** เป็นวันที่ใดก็ได้หลังจาก 31 มกราคมเป็นต้นไป และเวลา 10 วันจะยังคงถูกลบออกจากรอบระยะเวลาของธุรกรรมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e618b-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="e618b-115">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="e618b-115">See also</span></span>

[<span data-ttu-id="e618b-116">ตัวอย่างวันในการลด</span><span class="sxs-lookup"><span data-stu-id="e618b-116">Reduction days example</span></span>](reduction-days-example.md)

  


