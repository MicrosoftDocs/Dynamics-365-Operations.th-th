---
title: ชนิดการชำระเงินต้องเป็นข้อผิดพลาดเกี่ยวกับบัตรเครดิตในหน้าใบสั่งขาย
description: หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการแสดงข้อความแสดงข้อผิดพลาดบนหน้าใบสั่งขายหลังจากการซิงค์ใบสั่งแล้ว
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
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018421"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="e18f8-103">"ชนิดการชำระเงินต้องเป็นข้อผิดพลาดเกี่ยวกับบัตรเครดิต" ในหน้าใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="e18f8-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e18f8-104">หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการแสดงข้อความแสดงข้อผิดพลาดบนหน้าใบสั่งขายหลังจากการซิงค์ใบสั่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="e18f8-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="e18f8-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e18f8-105">Description</span></span>

<span data-ttu-id="e18f8-106">เมื่อคุณเปิดหน้าใบสั่งขายหลังจากที่คุณซิงค์ใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ชนิดการชำระเงินต้องเป็นบัตรเครดิต เนื่องจากมีการระบุหมายเลขบัตรเครดิตแล้ว"</span><span class="sxs-lookup"><span data-stu-id="e18f8-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![ชนิดการชำระเงินต้องเป็นข้อผิดพลาดเกี่ยวกับบัตรเครดิต](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="e18f8-108">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="e18f8-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="e18f8-109">ตั้งค่าชนิดการชำระเงินในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="e18f8-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="e18f8-110">ไปที่ **บัญชีลูกหนี้ \> การตั้งค่าการชำระเงิน \> เงื่อนไขการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="e18f8-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="e18f8-111">ในการนําทางด้านซ้าย ให้เลือกเงื่อนไขการชำระเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="e18f8-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="e18f8-112">ในฟิลด์ **ชนิดการชำระเงิน** ให้ตรวจสอบให้แน่ใจว่ามีการเลือก **บัตรเครดิต** แล้ว</span><span class="sxs-lookup"><span data-stu-id="e18f8-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e18f8-113">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e18f8-113">Additional resources</span></span>

[<span data-ttu-id="e18f8-114">การลงรายการบัญชีการขายออนไลน์และการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e18f8-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
