---
title: ไม่ปรากฏตัวเลือกบันทึกการชำระเงินถัดไปของฉัน
description: หัวข้อนี้แสดงการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเมื่อกล่องกาเครื่องหมาย บันทึกสําหรับการชำระเงินถัดไปของฉัน ไม่ปรากฏขึ้นภายใต้วิธีการจ่ายเงินในหน้าเช็คเอาท์ของไซต์อีคอมเมิร์ซ
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
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585557"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="d7621-103">ไม่ปรากฏตัวเลือก "บันทึกการชำระเงินถัดไปของฉัน"</span><span class="sxs-lookup"><span data-stu-id="d7621-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7621-104">หัวข้อนี้แสดงการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเมื่อกล่องกาเครื่องหมาย  **บันทึกสําหรับการชำระเงินถัดไปของฉัน** ไม่ปรากฏขึ้นภายใต้ **วิธีการจ่ายเงิน** ในหน้าเช็คเอาท์ของไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="d7621-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="d7621-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d7621-105">Description</span></span>

<span data-ttu-id="d7621-106">กล่องกาเครื่องหมาย  **บันทึกสำหรับการชำระเงินครั้งถัดไปของฉัน** ไม่ปรากฏในส่วน **วิธีการชำระเงิน** ในหน้าเช็คเอาท์ของไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="d7621-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="d7621-107">รูปภาพประกอบต่อไปนี้จะแสดงตัวอย่างของหน้าเช็คเอาท์ที่รวมกล่องกาเครื่องหมาย **บันทึกสำหรับการชำระเงินครั้งถัดไปของฉัน**</span><span class="sxs-lookup"><span data-stu-id="d7621-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![กล่องกาเครื่องหมายบันทึกสำหรับการชำระเงินครั้งถัดไปของฉันในโมดูลการชำระเงิน](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="d7621-109">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="d7621-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="d7621-110">ตรวจสอบว่า Dynamics 365 Payment Connector สำหรับ Adyen ได้รับการตั้งค่าคอนฟิกอย่างถูกต้องในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="d7621-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="d7621-111">ให้ทำตามขั้นตอนดังต่อไปนี้ เพื่อตรวจสอบว่า Dynamics 365 Payment Connector สำหรับ Adyen ได้รับการตั้งค่าคอนฟิกอย่างถูกต้องในศูนย์ควบคุม Commerce </span><span class="sxs-lookup"><span data-stu-id="d7621-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d7621-112">ไปที่การ **Retail และ Commerce \> ช่องทาง \>ร้านค้าออนไลน์**</span><span class="sxs-lookup"><span data-stu-id="d7621-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="d7621-113">เลือกร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="d7621-113">Select the online store.</span></span>
1. <span data-ttu-id="d7621-114">บนแท็บด่วน **บัญชีการชำระเงิน** ตรวจสอบให้แน่ใจว่าได้ตั้งค่าฟิลด์ **อนุญาตให้บันทึกข้อมูลการชำระเงินในอีคอมเมิร์ซ** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="d7621-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![อนุญาตให้บันทึกข้อมูลการชำระเงินในฟิลด์อีคอมเมิร์ซในศูนย์ควบคุม Commerce](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="d7621-116">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d7621-116">Additional resources</span></span>

[<span data-ttu-id="d7621-117">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="d7621-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="d7621-118">การบันทึกเครื่องมือการชำระเงินออนไลน์ด้วยตัวเชื่อมต่อ Adyen</span><span class="sxs-lookup"><span data-stu-id="d7621-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
