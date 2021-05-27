---
title: มีการชำระเงินโดยอัตโนมัติก่อนออกใบแจ้งหนี้หรือจัดส่งสินค้าตามใบสั่ง
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อมีการจ่ายเงินในพอร์ทัล Adyen ทันทีหลังจากที่วางใบสั่ง ถึงแม้ว่าใบสั่งขายจะยังไม่ได้ออกใบแจ้งหนี้หรือจัดส่งสินค้า
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018271"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="5b9b3-103">มีการชำระเงินโดยอัตโนมัติก่อนออกใบแจ้งหนี้หรือจัดส่งสินค้าตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="5b9b3-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b9b3-104">หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อมีการจ่ายเงินในพอร์ทัล Adyen ทันทีหลังจากที่วางใบสั่ง ถึงแม้ว่าใบสั่งขายจะยังไม่ได้ออกใบแจ้งหนี้หรือจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b9b3-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="5b9b3-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b9b3-105">Description</span></span>

<span data-ttu-id="5b9b3-106">หลังจากสั่งซื้อแล้ว การชำระเงินจะชำระทันทีในพอร์ทัล Adyen ถึงแม้ว่าใบสั่งขายจะยังไม่ได้ออกใบแจ้งหนี้หรือจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b9b3-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="5b9b3-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="5b9b3-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="5b9b3-108">ตั้งค่าคอนฟิกการรวบรวมข้อมูลด้วยตนเองสำหรับการชำระเงินอีคอมเมิร์ซ ในพอร์ทัล Adyen</span><span class="sxs-lookup"><span data-stu-id="5b9b3-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="5b9b3-109">ตั้งค่าคอนฟิกการรวบรวมข้อมูลด้วยตนเองสำหรับการชำระเงินอีคอมเมิร์ซ ในพอร์ทัล Adyen ให้ทำตามขั้นตอนดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5b9b3-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="5b9b3-110">ลงชื่อเข้าใช้ พอร์ทัล Adyen</span><span class="sxs-lookup"><span data-stu-id="5b9b3-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="5b9b3-111">ในมุมขวาบน ให้เลือกบัญชีผู้ขายของคุณให้กับช่องทางอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="5b9b3-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="5b9b3-112">บนแถบนำทางบนสุด ให้เลือก **บัญชี** แล้วจากนั้นเลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="5b9b3-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="5b9b3-113">ในฟิลด์ **ความล่าช้าในการรวบรวมข้อมูล** ให้เลือก **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="5b9b3-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![จัดให้มีการตั้งค่าความล่าช้าในการรวบรวมข้อมูลในพอร์ทัล Adyen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="5b9b3-115">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5b9b3-115">Additional resources</span></span>

[<span data-ttu-id="5b9b3-116">การรวบรวมข้อมูลการชำระเงิน Adyen</span><span class="sxs-lookup"><span data-stu-id="5b9b3-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="5b9b3-117">ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="5b9b3-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="5b9b3-118">ตั้งค่าตัวเชื่อมต่อการชำระเงิน Adyen สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5b9b3-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
