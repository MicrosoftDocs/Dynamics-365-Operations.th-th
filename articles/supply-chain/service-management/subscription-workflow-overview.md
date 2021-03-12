---
title: ภาพรวมลำดับงานการสั่งซื้อโดยบอกรับเป็นสมาชิก
description: หัวข้อนี้แสดงภาพรวมของลำดับงานการบอกรับเป็นสมาชิก
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc2b2dc724adf53bfc6cb8de79c14c7414cbc40a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974171"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="6fe55-103">ภาพรวมลำดับงานการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="6fe55-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6fe55-104">คุณเป็นผู้ดูแลระบบการบอกรับเป็นสมาชิกของบริษัทที่ให้บริการระบบไฟแห่งหนึ่ง ที่เสนอการบอกรับเป็นสมาชิกสำหรับการซ่อมบำรุงอุปกรณ์ไฟ</span><span class="sxs-lookup"><span data-stu-id="6fe55-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="6fe55-105">ลูกค้าติดต่อบริษัทของคุณเพื่อสมัครเป็นสมาชิกรายปีสำหรับการซ่อมบำรุงอุปกรณ์ไฟ</span><span class="sxs-lookup"><span data-stu-id="6fe55-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="6fe55-106">การตั้งค่าการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="6fe55-106">Setting up subscriptions</span></span>

<span data-ttu-id="6fe55-107">ในการตั้งค่าการบอกรับเป็นสมาชิก อันดับแรกคุณต้องสร้างประเภทของการบอกรับเป็นสมาชิกสำหรับข้อตกลงการให้บริการใหม่ หรือตรวจสอบว่ามีกลุ่มการบอกรับเป็นสมาชิกอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6fe55-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="6fe55-108">หากมีกลุ่มการบอกรับเป็นสมาชิกอยู่ คุณต้องตั้งค่าเพื่อออกใบแจ้งหนี้แก่ลูกค้าเป็นรายปี และเพื่อให้มีการรับรู้รายได้ทุกเดือนของปี</span><span class="sxs-lookup"><span data-stu-id="6fe55-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="6fe55-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าการบอกรับเป็นสมาชิก ให้ดูที่ [ตั้งค่ากลุ่มการบอกรับเป็นสมาชิก](set-up-subscription-groups.md)</span><span class="sxs-lookup"><span data-stu-id="6fe55-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="6fe55-110">เมื่อสร้างประเภทการบอกรับเป็นสมาชิกแล้ว คุณจะสามารถสร้างการบอกรับเป็นสมาชิกได้ </span><span class="sxs-lookup"><span data-stu-id="6fe55-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="6fe55-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างการบอกรับเป็นสมาชิกการบริการ ดู [สร้างการบอกรับเป็นสมาชิกการบริการจากกลุ่มการบอกรับเป็นสมาชิก](create-service-subscriptions-from-subscription-group.md)</span><span class="sxs-lookup"><span data-stu-id="6fe55-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="6fe55-112">สร้างและปรับเปลี่ยนธุรกรรมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="6fe55-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="6fe55-113">หลังจากที่คุณตั้งค่าการบอกรับเป็นสมาชิก คุณสร้างธุรกรรมค่าธรรมเนียมการบอกรับเป็นสมาชิกสำหรับรอบระยะเวลาการออกใบแจ้งหนี้ครั้งแรก ซึ่งก็คือหนึ่งปี</span><span class="sxs-lookup"><span data-stu-id="6fe55-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="6fe55-114">ธุรกรรมเป็นชนิด **ปกติ**</span><span class="sxs-lookup"><span data-stu-id="6fe55-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="6fe55-115">ดังนั้น คุณจะสามารถสร้างได้เฉพาะธุรกรรมการบอกรับเป็นสมาชิก ที่ซึ่งวันที่เริ่มต้นและวันที่สิ้นสุดสอดคล้องกับรอบระยะเวลาที่ถูกสร้างขึ้นก่อนหน้าในแบบฟอร์ม **ชนิดรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="6fe55-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="6fe55-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับธุรกรรมค่าธรรมเนียม ให้ดูที่ [สร้างธุรกรรมค่าธรรมเนียมสำหรับการบอกรับเป็นสมาชิก](create-subscription-fee-transactions.md)</span><span class="sxs-lookup"><span data-stu-id="6fe55-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="6fe55-117">หลังจากคุณตั้งค่าการบอกรับเป็นสมาชิกสำหรับลูกค้าของคุณแล้ว คุณต้องจำไว้ว่า พวกเขาได้เจรจาขอส่วนลด 10 เปอร์เซ็นต์ จากรายการราคาทั้งหมดสำหรับบริการที่เสนอ</span><span class="sxs-lookup"><span data-stu-id="6fe55-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="6fe55-118">ดังนั้น คุณต้องลดราคาค่าธรรมเนียมธุรกรรมที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6fe55-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="6fe55-119">ต่อมา ผู้ติดต่อลูกค้าของคุณโทรมาแจ้งว่า แม้ว่าพวกเขายังต้องการข้อตกลงการให้บริการสำหรับอุปกรณ์ไฟอยู่ แต่เขามีแผนที่จะออกอุปกรณ์ไฟใหม่ปลายปี</span><span class="sxs-lookup"><span data-stu-id="6fe55-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="6fe55-120">ดังนั้น พวกเขาต้องการความครอบคลุมการบำรุงรักษาจนถึงเดือน 2013 ตุลาคมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6fe55-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="6fe55-121">เพื่อเป็นการลดจำนวนเดือนการบอกรับเป็นสมาชิกของลูกค้า คุณจึงสร้างธุรกรรมค่าธรรมเนียมการบอกรับเป็นสมาชิกใหม่ชนิด **จำนวนวันที่ลด**</span><span class="sxs-lookup"><span data-stu-id="6fe55-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="6fe55-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการลดจำนวนวัน ดู [ลดจำนวนวันของค่าธรรมเนียมการบอกรับเป็นสมาชิก](reduce-the-days-on-subscription-fees.md)</span><span class="sxs-lookup"><span data-stu-id="6fe55-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="6fe55-123">ออกใบแจ้งหนี้และรับรู้ธุรกรรมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="6fe55-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="6fe55-124">ตอนนี้ คุณได้ตั้งค่าการบอกรับเป็นสมาชิกเรียบร้อยแล้ว และคุณพร้อมที่จะออกใบแจ้งหนี้แก่ลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="6fe55-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="6fe55-125">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการออกใบแจ้งหนี้การบอกรับเป็นสมาชิก ให้ดูที่ [ออกใบแจ้งหนี้ธุรกรรมการบอกรับเป็นสมาชิก](invoice-subscription-transactions.md)</span><span class="sxs-lookup"><span data-stu-id="6fe55-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="6fe55-126">สองวันต่อมา ลูกค้าของคุณโทรมาแจ้งว่า ควรออกใบแจ้งหนี้การบอกรับเป็นสมาชิกเป็นดอลลาร์สหรัฐฯ ไม่ใช่ยูโร</span><span class="sxs-lookup"><span data-stu-id="6fe55-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="6fe55-127">ดังนั้น คุณจึงสร้างใบลดหนี้ และคุณยังสร้างธุรกรรมการบอกรับเป็นสมาชิกใหม่โดยใช้สกุลเงินที่ถูกต้องด้วย</span><span class="sxs-lookup"><span data-stu-id="6fe55-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="6fe55-128">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการลงเครดิตธุรกรรมการบอกรับเป็นสมาชิก ให้ดูที่ [ลงเครดิตธุรกรรมการบอกรับเป็นสมาชิก](credit-subscription-transactions.md)</span><span class="sxs-lookup"><span data-stu-id="6fe55-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="6fe55-129">ทุกสิ้นเดือน จะรับรู้รายได้หนึ่งเดือนจากการบอกรับเป็นสมาชิกของลูกค้าลงในบัญชีกำไรขาดทุน และบัญชี WIP</span><span class="sxs-lookup"><span data-stu-id="6fe55-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="6fe55-130">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการรับรู้รายได้สำหรับการบอกรับเป็นสมาชิก ดู [รับรู้รายได้การบอกรับเป็นสมาชิก](accrue-subscription-revenue.md)</span><span class="sxs-lookup"><span data-stu-id="6fe55-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


