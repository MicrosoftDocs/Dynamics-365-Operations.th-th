---
title: ข้อผิดพลาดในการซิงโครไนส์ใบสั่งที่เกี่ยวข้องกับบริการจ่ายเงินเริ่มต้น
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยแก้ไขข้อผิดพลาดที่อาจเกิดขึ้นเมื่อซิงค์ใบสั่งออนไลน์
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585549"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="24d28-103">ข้อผิดพลาดในการซิงโครไนส์ใบสั่งที่เกี่ยวข้องกับบริการจ่ายเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="24d28-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24d28-104">หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยแก้ไขข้อผิดพลาดที่อาจเกิดขึ้นเมื่อซิงค์ใบสั่งออนไลน์</span><span class="sxs-lookup"><span data-stu-id="24d28-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="24d28-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="24d28-105">Description</span></span>

<span data-ttu-id="24d28-106">เมื่อคุณซิงค์ใบสั่งออนไลน์ คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ต้องมีบริการจ่ายเงินเริ่มต้นเพื่อประมวลผลธุรกรรมบัตรเครดิต"</span><span class="sxs-lookup"><span data-stu-id="24d28-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![ขาดข้อผิดพลาดของบริการจ่ายเงินเริ่มต้น](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="24d28-108">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="24d28-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="24d28-109">ยืนยันหรือตั้งค่าบริการจ่ายเงินเริ่มต้นในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="24d28-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="24d28-110">ในการยืนยันหรือตั้งค่าบริการจ่ายเงินเริ่มต้นในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="24d28-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="24d28-111">ไปที่ **บัญชีลูกหนี้ \> การตั้งค่าการชำระเงิน \> บริการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="24d28-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="24d28-112">ตรวจสอบให้แน่ใจว่าตัวเลือก **ตัวประมวลผลเริ่มต้นเริ่มต้นของบัตรเครดิตใหม่** ได้รับการตั้งค่าเป็น **ใช่** บริการการชำระเงินหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="24d28-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24d28-113">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="24d28-113">Additional resources</span></span>

[<span data-ttu-id="24d28-114">การตั้งค่า การตรวจสอบ และการรวบรวมข้อมูลบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="24d28-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
