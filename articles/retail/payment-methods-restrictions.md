---
title: จำกัดวิธีการชำระเงินสำหรับการส่งคืนที่ไม่มีใบเสร็จ
description: หัวข้อนี้อธิบายวิธีว่าการชำระเงินบางชนิดอาจถูกจำกัดสำหรับการขอคืนเงินถ้าเงินส่งคืนถูกจัดทำขึ้นโดยไม่มีใบเสร็จ
author: rapraj
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1f84a6382453c0ba7540e618ad90ae1d3c684a2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "315923"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="1599b-103">จำกัดวิธีการชำระเงินสำหรับการส่งคืนที่ไม่มีใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="1599b-103">Restrict payment methods for returns without a receipt</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1599b-104">ต้องกำหนดประเภทการชำระเงินแต่ละชนิดที่ผู้ค้าปลีกยอมรับเมื่อตั้งค่าระบบ</span><span class="sxs-lookup"><span data-stu-id="1599b-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="1599b-105">หัวข้อนี้อธิบายวิธีว่าการชำระเงินบางชนิดอาจถูกจำกัดสำหรับการขอคืนเงินถ้าเงินส่งคืนถูกจัดทำขึ้นโดยไม่มีใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="1599b-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="1599b-106">การตั้งค่าวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1599b-106">Set up payment methods</span></span>

<span data-ttu-id="1599b-107">เพื่อตั้งค่าวิธีการชำระเงิน คุณต้องดำเนินการต่อไปนี้ให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="1599b-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="1599b-108">สร้างวิธีการชำระเงินที่ยอมรับ โดยองค์กรทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1599b-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="1599b-109">สร้างชนิดของบัตรทั่วทั้งองค์กรและหมายเลขบัตร</span><span class="sxs-lookup"><span data-stu-id="1599b-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="1599b-110">ถ้าบัตรเครดิตหรือบัตรเดบิตเป็นที่ยอมรับ คุณต้องสร้างวิธีการชำระเงินอีกหนึ่งรายการสำหรับบัตรบัตรเครดิตหรือบัตรเดบิต จากนั้น ให้สร้างชนิดของบัตรทั่วทั้งองค์กรและหมายเลขบัตร</span><span class="sxs-lookup"><span data-stu-id="1599b-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="1599b-111">ตั้งค่าวิธีการชำระเงินของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="1599b-111">Set up store payment methods.</span></span> <span data-ttu-id="1599b-112">วิธีการชำระเงินการเชื่อมโยงกับร้านค้าแต่ละ และจากนั้น ป้อนการตั้งค่าร้านค้าเฉพาะสำหรับแต่ละวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1599b-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="1599b-113">ตั้งค่าวิธีการชำระเงินด้วยบัตรสำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="1599b-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="1599b-114">สำหรับวิธีการชำระเงินใดๆที่เป็นที่ยอมรับในการจัดเก็บ ดำเนินการตั้งค่าบัตร</span><span class="sxs-lookup"><span data-stu-id="1599b-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="1599b-115">![การตั้งค่าร้านค้าปลีก](media/NoReceiptReturns1.png "การตั้งค่าร้านค้าปลีก")</span><span class="sxs-lookup"><span data-stu-id="1599b-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="1599b-116">จำกัดวิธีการชำระเงินสำหรับการส่งคืนที่ไม่มีใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="1599b-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="1599b-117">สำหรับวิธีการชำระเงินของแต่ละร้านค้า บนหน้า **การจัดการร้านค้าปลีก** ภายใต้ **ไม่มีการส่งใบเสร็จคืน** ตั้งค่า **จำกัดสำหรับการขอคืนเงินโดยไม่มีใบเสร็จ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="1599b-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="1599b-118">ค่าเริ่มต้นของสลับคือ **ไม่ใช่** ซึ่งช่วยให้มั่นใจว่าวิธีการชำระเงินได้รับอนุญาตสำหรับการขอคืนเงิน</span><span class="sxs-lookup"><span data-stu-id="1599b-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="1599b-119">เมื่อ **จำกัดสำหรับการขอคืนเงินโดยไม่มีใบเสร็จ** ถูกตั้งค่าเป็น **ใช่** วิธีการชำระเงินที่เลือกจะไม่ได้รับอนุญาตสำหรับการขอคืนเงิน</span><span class="sxs-lookup"><span data-stu-id="1599b-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="1599b-120">![วิธีการชำระเงินของร้านค้าปลีก](media/NoReceiptReturns3.png "วิธีการชำระเงินของร้านค้าปลีก")</span><span class="sxs-lookup"><span data-stu-id="1599b-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="1599b-121">เมื่อพนักงานเก็บเงินเลือกวิธีการชำระเงินที่จำกัดสำหรับการขอคืนเงินโดยไม่มีใบเสร็จ ข้อความจะแสดงขึ้นเพื่อตรวจสอบวิธีการชำระเงินที่ยอมรับได้</span><span class="sxs-lookup"><span data-stu-id="1599b-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="1599b-122">![วิธีการชำระเงินที่ยอมรับได้](media/NoReceiptReturns4.png "วิธีการชำระเงินที่ยอมรับได้")</span><span class="sxs-lookup"><span data-stu-id="1599b-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="1599b-123">ถ้าธุรกรรมมีทั้งการส่งคืนแบบมีใบเสร็จและการส่งคืนแบบไม่มีใบเสร็จ เงื่อนไขข้อจำกัดจะไม่ถูกบังคับ เนื่องจากธุรกรรมจะเป็นลำดับงานส่งคืนสินค้าที่มีใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="1599b-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

